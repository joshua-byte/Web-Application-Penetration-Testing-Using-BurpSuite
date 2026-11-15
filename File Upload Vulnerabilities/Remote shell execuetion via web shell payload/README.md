# Remote Shell Execution via Web Shell Payload

**Status:** Solved
**Severity:** High

## Summary

The avatar upload feature on the My Account page didn't validate the
uploaded file's type at all. A PHP file could be uploaded directly, and
since the avatars folder executes PHP, requesting the uploaded file ran the
code on the server.

## Steps

1. Uploaded a normal image to see how/where avatars are stored.
2. Intercepted the upload in Burp and swapped the file for `payload.php`:
   ```php
   <?php echo file_get_contents('/home/carlos/secret'); ?>
   ```
3. Forwarded the request — no validation, upload accepted.
4. Requested `/files/avatars/payload.php` directly. The PHP executed and
   returned carlos's secret.
5. Submitted the secret to solve the lab.


## Fix

Validate file content server-side, use an extension allow-list, and don't
let the upload directory execute scripts.
