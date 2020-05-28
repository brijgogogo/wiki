= vim projectionist =
Allows to define navigation command.

Allows you to open files by thinking about their naming semantics, rather than thinking about their location.



* .projections.json file contains the directives
{

"app/app.js" : { "type" : "main" },

"app/models/*.js" : { "type" : "model" },

"app/adapters/*.js" : { "type" : "adapter" },

"app/serializers/*.js" : { "type" : "serializer" }

}

* accessing files:
➾ :Emain  : opens app.js
➾ :Eadapter post : opens post.js in app/adapters directory
➾ :Emodel author
➾ :Eserializer comment

* has tab completion: for eg. type Es<Tab>, it will complete it to Eserializers
* wildcards: eg. :Emodel *nt<Tab> : expands *nt to comment (file).
* :Emodel <C-d> : shows list of possible completions

Etype - open type in current window
Stype - opens in horizontal split
Vtype - opens in vertical split
Ttype - opens in new tab

* Alternate file - like unit test files

"app/models/*.js" : { "type" : "model" , "alternate" : "tests/unit/models/{}-test.js" }

{} will be replaced by the portion of the glob matched by the * wildcard.

Emodel author : opens author.js
:A - opens unit test file

