# Web Security Headers

## Content-Security-Policy (CSP)
The CSP header provides an extra security layer to protect against attacks like Cross-Site Scripting (XSS).

**Example:**
- **default-src**: Restricts resources to the current website only (`self`).
- **script-src**: Defines allowed script sources, including `self` and `https://cdn.tryhackme.com`.
- **style-src**: Limits CSS stylesheet sources to the current website (`self`).

## Strict-Transport-Security (HSTS)
The HSTS header forces browsers to use HTTPS for all connections.

**Example:**
- **max-age**: Specifies the duration (in seconds) for the HSTS policy.
- **includeSubDomains**: Optionally extends the policy to all subdomains.
- **preload**: Allows inclusion in browser preload lists to enforce HSTS before the first visit.

## X-Content-Type-Options
This header prevents browsers from guessing a resource’s MIME type, enforcing the specified Content-Type.

**Example:**
- **nosniff**: Directs browsers to use the declared MIME type without guessing.

## Referrer-Policy
Controls the information sent to a destination server when a user navigates (e.g., via a hyperlink).

**Examples:**
- **no-referrer**: Blocks all referrer information from being sent.
- **same-origin**: Sends referrer data only for same-origin requests, ideal for internal links.
- **strict-origin**: Sends only the origin as the referrer for same-protocol requests (e.g., HTTPS to HTTPS).
- **strict-origin-when-cross-origin**: Sends the full URL for same-origin requests but only the origin for cross-origin requests with matching protocols.
