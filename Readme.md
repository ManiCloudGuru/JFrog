Repository Types
Repository Types
Overview
Artifactory hosts four repository types: Local, Remote, Virtual and Federated. Local and remote repositories are true physical repositories, while a virtual repository is actually an aggregation of them used to create controlled domains for search and resolution of artifacts. The Federated repository functions similarly to a local repository on the JFrog Platform Deployments (JPDs), but is grouped together logically with other Federated members located on other JPDs, to create a Federation.
Local repositories
Local repositories are physical, locally managed repositories into which you can deploy artifacts.
Typically, these are used to deploy internal and external releases as well as development builds, but they can also be used to store binaries that are not widely available on public repositories such as 3rd party commercial components.
Using local repositories, all of your internal resources can be made available from a single access point across your organization from one common URL
Artifacts in a local repository can be accessed directly using the following URL:
http://<host>:<port>/artifactory/<local-repository-name>/<artifact-path>


Remote Repositories
A remote repository serves as a caching proxy for a repository managed at a remote site such as ConanCenter.
Artifacts are stored and updated in remote repositories according to various configuration parameters that control the caching and proxying behavior. 
The URL for the remote repository.
Currently only HTTP and HTTPS URLs are supported.


Virtual Repositories
A virtual repository encapsulates any number of local and remote repositories, and represents them as a unified repository accessed from a single URL.
It gives you a way to manage which repositories are accessed by developers since you have the freedom to mix, match and modify the actual repositories included within the virtual repository.
You can also optimize artifact resolution by defining the underlying repository order so that Artifactory will first look through local repositories, then remote repository caches, and only then Artifactory will go through the network and request the artifact directly from the remote resource.
For the developer it’s simple. Just request the package, and Artifactory will safely and optimally access it according to your organization policies.



