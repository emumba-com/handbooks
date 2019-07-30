Unless there is a good reason, you should follow the branching model given below. 

*  `master` represents the code deployed in production. After each release, the branch should be tagged. `Tag` should follow format `major_version.minor_version.build_number` e.g. `1.0.0` would denote first release to production. If a minor fix is released afterwards, tag should be 1.0.1. Similarly increment the major and minor versions according to releases.
* `staging` (pulled from `master`) represents the code that can be moved to production anytime as next release. QA team will use this for testing.
* `dev` (pulled from `staging`) represents the branch where developers can push code on day to day basis. 
*  `feature` (pulled from `dev`) feature specific branch can be pulled out of `dev` if a major chuck of functionality (a feature) needs to be developed. This feature will be merged into `dev` once it is complete. 