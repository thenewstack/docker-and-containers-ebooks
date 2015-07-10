# Adopting Containers in the Enterprise

by Vivek Juneja

---  
  
New technologies and practices follow a common adoption process in large enterprises. The process typically begins with elaborate presentations and discussions, followed by various proofs-of-concept. This leads to small-scale adoption within teams building non-critical systems, and mostly for development and test workloads. By the time this technology reaches production, a significant amount of time and opportunity has passed, leading to friction between the development team’s productivity and organizational processes. 

  
Containers, and the notion of containerizing enterprise workloads, are going through this process right now, in a great many enterprises, fueled by the promise that containers offer to help them address the varied issues that plague developer productivity and application delivery in enterprises. 

  
Enterprise Motivations

  
Enterprises are beginning the process of adopting Docker and containers for a variety of reasons, including:

  
Process Efficiency

Different teams within the enterprise often have their own standards for developing and releasing software. Outsourced development, unfortunately often accompanied by limited governance and transparency, often exacerbates this problem. Many enterprises have turned to containers as the basis upon which to standardize the software release process across teams.

  
Legacy Applications

Legacy applications and systems are  commonplace in the enterprise. These systems create constant operational and maintenance issues. Project teams struggle to allocate resources to operate on-demand test infrastructure, and frequently forgo testing in favor of releasing new functionality on time. Teams working on legacy applications are attracted to containers for their ability to help make more efficient use of infrastructure.

  
Collaboration

Development teams working on large projects have to coordinate software releases, a process that often takes a long time. The multiple teams working on continuously maintained and developed legacy applications, for example, appreciate the ability of containers to help them synchronize software releases more easily. 

  
Dev/Prod Parity

Production, development and test environments often have parity issues, drifting apart in ways that lead to constant “runs-on-my-machine” issues. Containers help ensure a consistent runtime environment across various infrastructures, a feature enterprise development teams find extremely attractive.

  
VM Sprawl 

As enterprises adopt virtual machines, VM sprawl often sets in, leading to less efficient utilization of the infrastructure and resulting in the need to establish governance rules, like approvals and workflows, to limit the sprawl. These rules, however, reverse the benefits of elasticity and self-service for developers. Because the overhead associated with containers is so much lower than that of VMs, many enterprises are exploring containers as a way to mitigate sprawl.

  
Cloud-Native Applications

Microservices and other cloud-native application architectures require a different view of infrastructure than is traditionally assumed. In containers, enterprise development teams see an opportunity to more easily build cloud-native applications and more easily take advantage of emerging trends.


1. Process efficiency:. Different teams within the enterprise often have their own standards for developing and releasing software. Outsourced development, unfortunately often accompanied by limited governance and transparency, often exacerbates this problem. Many enterprises have turned to containers as the basis upon which to standardize the software release process across teams.



  

1. Legacy applications:. Legacy applications and systems are  commonplace in the enterprise. These systems create constant operational and maintenance issues. Project teams struggle to allocate resources to operate on-demand test infrastructure, and frequently forgo testing in favor of releasing new functionality on time. Teams working on legacy applications are attracted to containers for their ability to help make more efficient use of infrastructure.



  

1. Collaboration:. Development teams working on large projects have to coordinate software releases, a process that often takes a long time. The multiple teams working on continuously maintained and developed legacy applications, for example, appreciate the ability of containers to help them synchronize software releases more easily. 



  

1. Dev/prod parity:. Production, development and test environments often have parity issues, drifting apart in ways that lead to constant “runs-on-my-machine” issues. Containers help ensure a consistent runtime environment across various infrastructures, a feature enterprise development teams find extremely attractive.



  

1. VM sprawl:. As enterprises adopt virtual machines, VM sprawl often sets in, leading to less efficient utilization of the infrastructure and resulting in the need to establish governance rules, like approvals and workflows, to limit the sprawl. These rules, however, reverse the benefits of elasticity and self-service for developers. Because the overhead associated with containers is so much lower than that of VMs, many enterprises are exploring containers as a way to mitigate sprawl.



  

1. Cloud-native applications:. Microservices and other cloud-native application architectures require a different view of infrastructure than is traditionally assumed. In containers, enterprise development teams see an opportunity to more easily build cloud-native applications and more easily take advantage of emerging trends.



  
By providing abstraction around the workload, and making it portable, containers become the foundation for supporting a variety of more efficient development processes and application architectures.

  
Container Adoption Strategies

  
When virtual machines started getting popular inside the enterprise, a major selling point to the IT department was the opportunity to consolidate underutilized infrastructure as a way to reduce the operational footprint and, hence, costs. Adoption of containers and the ecosystem surrounding them, however, is being driven by agility, not cost reduction. Enterprise IT organizations are looking to containers to help them adopt more modern application architectures and development processes, in the process allowing them to innovate more quickly. 

  
As we say with VMs though, container adoption typically begins in development and test environments. Ideally, greenfield projects take the first plunge, but some curious users also try to containerize existing projects in order to deal with critical infrastructure availability or process issues that plague their ability to execute. In addition, ramping up new development teams with project environments that are already containerized is far easier than traditional approaches. This helps get the teams started with container technology quickly, without the complexity of transitioning existing project processes. 

  
  
There are a handful of common strategies that enterprises take when evaluating and adopting container technologies:

  

1. Solving infrastructure availability crunches in development and testing is often a good driver for making the leap to containers. When development teams have to struggle to get test environments provisioned and operational, they lose a lot of time, and frustration mounts. If dedicated instances are not needed, then reusing IT infrastructure for hosting test environments as linked containers is a great way to get started, and can provide important operational knowledge of the technology.



  

1. Build and deployment infrastructure needs to be modified for the enterprise to take full advantage of modern infrastructure. To deploy to public and private clouds, some enterprises deploy the end application as a set of machine images, reducing the time required to set up newly provisioned on-demand infrastructure. The same practice can be extended to container images. The build step can generate the new container image using a pre-existing base image for the environment. The deployment step can take this image and run it on any infrastructure supporting the chosen container technology. 



  

1. Adopting a “container-first” approach for all new projects is another common way to drive the adoption of containers. This means that all new projects will leverage containers for their build and release processes. This approach encourages the development teams to consider containers as a first-class design element of their application topology and thereby spurs the development of container-native applications.



  

1. It’s important for operations teams to formalize and release standard container images that all projects can use. These customized base images can be hosted on a private registry used by development teams when building projects. Changes to the standardized base images could mean new releases on the registry, which can then be transparently used in the development process. Enterprises are accustomed to hosting private repositories for firewall rules and other digital IT assets, so this will not be a strange adoption step for them. A development approach based on container images also helps encourage closer interaction between the development and operations teams, thereby encouraging DevOps.



  
Key Issues Faced

  
Enterprises face two key challenges when incorporating containers into their overall IT strategy: [security and the lack of mature tools in the container ecosystem](http://www.theregister.co.uk/2015/01/12/docker_security_immature_but_not_scary_says_gartner/). 

  
While web-scale companies like Google and Twitter have been using containers in production for years, it’s still early days for both open source and proprietary products. The issue of tool maturity is largely one of time and experience. With more adoption and demand, the tools will inevitably stabilize and improve. 

  
Security, on the other hand, has been a dominant focus among early adopters. While a concern for all firms using containers in production, it is an even greater worry for companies using containers in multi-tenant environments for their production workloads.

  
The issue at hand is one of container isolation. To date, containers don’t exhibit the strong and tested ability to isolate disparate workloads that has become assumed of the various virtual machine hypervisors. 

  
Last year, Canonical introduced [LXD](http://www.ubuntu.com/cloud/tools/lxd) as a way to implement ideas around stronger container security and make it mainstream with its Ubuntu and Openstack integration. New Projects like [Hyper](https://hyper.sh/), which uses a minimalist Linux kernel, called a HyperKernel, to load and run containers — are also emerging as interesting alternative to containers alone.

  
Containers in Practice

  
As organizations seek to drive agility and innovation, they naturally aim to eliminate inefficiencies, such as resource constraints and process bottlenecks. At the same time, they are turning to modern application  architecture styles like microservices, and development processes like continuous delivery, which together allow developers to iterate more quickly. 

  
Last year, the chief architect of [ING spoke at Dockercon Europe ](https://blog.docker.com/2014/12/dockercon-europe-keynote-continuous-delivery-in-the-enterprise-by-henk-kolk-ing/)about how they are using Docker to enable continuous delivery. [BBC News](https://blog.docker.com/2014/12/dockercon-eu-enterprise-ci-problems-and-our-solutions-by-simon-thulbourne/) also highlighted how they architected their continuous integration solution around Docker, and shared the caveats and compromises that they had to deal with. The presentations by these two large companies is a sign of how quickly the enterprise is getting serious about container technologies.

  
By taking one or more of the approaches outlined in this article, enterprises new to the container game can take their first steps down the path of enlightenment, knowing that they’re following a trail that has been trod many times before.
