= REST =

Client -> HTTP Request (verbs, headers, content)
Server -> HTTP Response (status code, headers, content)
HTTP is stateless


# HTTP Verbs:
- GET
retrieves a resource
- POST
adds a new resource
- PUT
updates an existing resource
- PATCH
update an existing resource with set of changes
- DELETE
remove an existing resource


# Headers:
Content Length: <integer>
Content Tyep: text

# Status Codes
- 200 : OK
- 201 : Created
- 202 : Accepted
- 302 : Found
- 304 : Not Modified
- 307 : Temp Redirect
- 308 : Perm Redirect
- 400 : Bad Request
- 401 : Not Authorized
- 403 : Forbidden
- 404 : Not Found
- 405 : Method Not Allowed
- 409 : Conflict
- 500 : Server error

# REST: REpresentational State Transfer
- Separation of Client and Server
- Cacheable response
- URI

Resource: things that represent objects in your system
(domain model / entities)

# api design
http://.../api/entity
http://.../api/entity/key
http://.../api/entity/key/entity-child
http://.../api/entity/key/entity-child?childProperty=value
http://.../api/entity/key/entity-child/childKey





