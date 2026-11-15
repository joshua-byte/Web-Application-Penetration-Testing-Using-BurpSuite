# Web Shell Upload via Content-Type Restriction Bypass

## Summary

The server rejected uploads based on the `Content-Type` header declared in
the request, but never checked the actual file content. Since that header
is client-controlled, relabeling the PHP payload as an image was enough to
get past the filter.

## Steps

1. Uploaded `payload.php` with its real `Content-Type`
   (`application/x-php`) — rejected: "Only image/jpeg and image/png are
   allowed."
2. Intercepted the request in Burp, kept the same PHP file and `.php`
   filename, but changed the part's `Content-Type` header to `image/jpeg`.
3. Forwarded the request — accepted this time, since only the header was
   checked.
4. Requested the uploaded file directly; it executed and returned carlos's
   secret.
5. Submitted the secret to solve the lab.

## Fix
Never trust client-supplied headers for validation — check the real file
content (e.g. magic bytes) server-side instead.
