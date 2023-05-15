Book Chapter
* Threat Model VS Threat Modelling - grey lit references (Alex + Sam)
* Missing Features: Attacker Model (Fabio),
 measures of outcome (Fabio, possibly seeking Alex input)

* Adaptability and Evolution of Threat Model (Liliana -> Done)
There is no common agreement on how threat modelling should be performed in practice and at the moment threat modelling is based on expert judgement. More precisely, reasoning about what failed in the past helps practitioners identify relevant threats, using Flow Hypothesis Model (FHM). Security experts look at the system and create hypotheses about potential threats and test them out on the actual system by looking at the source code or test attacks. Security boundaries [1] are usually defined by a set of systems that are under a single administrative control. Vulnerabilities can become apparent as data crosses each boundary.
In practice security boundaries are defined at the architectural level (solution space) before threat modelling starts.  Data-Flow-Diagrams have been used in research to elicit potential threats. However, in practice security boundaries are expressed in the form of architectural drawings. Scaling such architectural drawings to complex systems is an open problem and engineering teams defining security boundaries may have limited security expertise and introduce mistakes.
Besides these difficulties it is hard to perform threat modelling for products, such as mobile device processors or IoT devices, where the security boundaries can change both during system deployment and also at runtime. On the one hand, during deployment, threats can be highly dependent on the environment where a specific product will be put into operation. For example, in a smart home IoT devices developed by different vendors will interact and work  together. Also, a mobile device processor can be installed in different types of devices. Variability in a product security boundary can demand the need of developing different threat models for the same type of product. On the other hand, when a security incident happens, security experts need to revise the security boundaries and select the products where it is relevant to fix the vulnerabilities leading to the incident. This section will discuss relevant related work on threat model variability and adaptation of threat models and security boundaries at runtime.










* Skillset for threat modeling (Tamara)
* Integration with software development process (Sven)
* Empirical methodological challenges (Daniel +Sam) 
* Repeatability (Mehdi)
* Literature search dump (Sam)

