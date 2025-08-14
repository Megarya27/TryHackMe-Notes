# HTTP Methods Overview

### `GET`
Fetches data from the server without modifying it.  
**Reminder:** Only expose data the user is allowed to access. Avoid including sensitive information like tokens or passwords, as GET requests can appear in plaintext.

### `POST`
Sends data to the server, typically to create or update resources.  
**Reminder:** Always validate and sanitize input to prevent attacks such as SQL injection or XSS.

### `PUT`
Replaces or updates an existing resource on the server.  
**Reminder:** Ensure the user has permission to make changes before accepting the request.

### `DELETE`
Removes a resource from the server.  
**Reminder:** Only authorized users should be able to delete resources.

---

### Other HTTP Methods

### `PATCH`
Updates part of a resource. Useful for partial modifications without replacing the entire resource.  
**Reminder:** Validate input to maintain data consistency.

### `HEAD`
Retrieves only the headers of a resource, not the full content.  
**Use case:** Checking metadata without downloading the full response.

### `OPTIONS`
Returns the HTTP methods supported by a resource.  
**Use case:** Helps clients understand what actions are allowed on the server.

### `TRACE`
Shows which HTTP methods are allowed, primarily for debugging.  
**Reminder:** Often disabled on servers for security reasons.

### `CONNECT`
Establishes a secure tunnel, typically for HTTPS connections.  
**Use case:** Enables encrypted communication, though less commonly used directly.
