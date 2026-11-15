# Lab 3: Web Shell Upload via Path Traversal

**Status:** Solved
**Severity:** High

## Summary

The avatars folder didn't execute `.php` files, but the server built the
save path from the attacker-supplied filename without sanitising it. Adding
a URL-encoded `../` to the filename moved the uploaded file one directory
up, into a location that does execute PHP.

## Steps

1. Uploaded `payload.php` normally and requested it back — it was returned
   as plaintext, confirming the avatars folder doesn't execute PHP.
2. Intercepted the upload in Burp and changed the filename to
   `..%2fpayload.php` (encoded `../payload.php`).
3. Forwarded the request — server confirmed: "The file
   avatars/../payload.php has been uploaded."
4. Requested `/files/avatars/../payload.php` — this time the PHP executed
   and returned carlos's secret.
5. Submitted the secret to solve the lab.

## Evidence

See `upload_path_traversal_evidence/`:
- `returns_plaintext.png` — payload returned as plaintext from the normal
  avatars path.
- `encoding_path.png` — upload request with the encoded traversal filename.
- `carlos_secret.png` — the request/response that leaks the secret after
  traversal.
- `solved.png` — lab solved confirmation.

## Fix

Strip/reject traversal sequences in filenames, generate the stored filename
server-side, and canonicalise + verify the final path stays inside the
intended directory.
