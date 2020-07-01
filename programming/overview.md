== Programming ==

* [[javascript/overview|javascript]]
* [[dotnet/.net|.net framework]]
* [[java/index|java]]
* [[elk/overview|elk]]

* [[git/overview|git]]

= web =
* [[html/overview|html]]
* [[css/overview|css]]
* [[web_development]]

* [[tools]]

* [[web_servers/overview|web_servers]]
* [[encryption]]

* [[continuous_integration]]
* [[powershell/overview|powershell]]
* [[batch_scripting/overview|batch_scripting]]
* [[shell_scripting/overview|shell scripts]]
* z-shell
* fish-shell
* [[bash/overview|bash]]

= databases =
* [[mongodb/overview|mongodb]]
* [[oracle/index|Oracle]]
* [[caches]]
* [[postgresql]]
* [[neo4j]] (graph database)


* [[postgresql_vs_mysql]]
* [[db_terms]]




* [[cloud/overview|cloud_computing]]

= programming languages =
* [[python/overview|python]]
* [[elm/overview|elm]]
* [[golang/overview|golang]]
* [[php]]
* [[kotlin/overview|kotlin]]
* [[ruby/index|ruby]]

= content management =
* [[jekyll/index|jekyll]]

= search =
* [[elastic_search/overview|elastic search]]
* [[solr/overview|solr]]

* [[development_methods]]
* [[coding_practices]]
* [[programming_concepts]]
* [[design_patterns/overview|design patterns]]
* [[algorithms/overview|algorithms]]
* [[programming_tips]]
* [[programming_jargons]]

* ssh
* [[kafka/overview|kafka]]
* [[security/overview|security]]
* [[wordpress/overview|wordpress]]
* [[terms]]

* [[tools]]

= general concepts =
* [[rest]]


== tools ==
* [[sql-developer]]
* [[markdown]]

== rnd ==
* [[rnd/overview|rnd]]


* [[data_attributes]]
* [[starter_kit]]
* [[qa]]
* [[information_architecture]]
* [[CORS]]
* [[Authentication]]

= Micro Frontends =
An architectural style where independently deliverable frontend applications are composed into a greater whole.
https://martinfowler.com/articles/micro-frontends.html
- container application - dynamic integration with other frontends
- cross-app communication: as little as possible
- common styles for consistent UI across apps
- consumer-driven contracts: each micro frontend can specify what it requires of other micro frontends
- Authentication/Authorization: cross-cutting concern, should be owned by container application. Container app can inject the login token into other micro frontends.
- Each micro frontend should have its own automated tests to test business logic and rendering logic.
- Integration testing - function/end-to-end testing tool - Selenium or Cypress. Functional tests just to validate that the page is assembled correctly.

Pit-of-success : make bad decisions hard and good ones easy

= Test Pyramid =
Functional tests should only cover aspects that cannot be tested at a lower level of the Test Pyramid.

== Frameworks ==
- Harvested Framework
https://martinfowler.com/bliki/HarvestedFramework.html
-  Foundation Framework
https://martinfowler.com/bliki/FoundationFramework.html

https://www.martinkysel.com/codility-permmissingelem-solution/

= Code Quality =
- Static Analysis
- Linting
- Coding Style
- Code Coverage


* pending
- https://martinfowler.com/articles/consumerDrivenContracts.html
- https://samnewman.io/patterns/architectural/bff/
- https://martinfowler.com/bliki/TestPyramid.html
- https://martinfowler.com/articles/microservices.html
- https://www.thoughtworks.com/radar/techniques
- https://www.joelonsoftware.com/2000/04/06/things-you-should-never-do-part-i/
- https://martinfowler.com/bliki/StranglerFigApplication.html
- https://martinfowler.com/bliki/BoundedContext.html
- https://blog.codinghorror.com/falling-into-the-pit-of-success/
- https://medium.com/@dabit3/the-prosperous-software-consultant-5dc8d705c5dd
