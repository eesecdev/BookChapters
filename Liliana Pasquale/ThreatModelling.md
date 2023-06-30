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
As a proactive approach, threat modeling helps identify potential security risks early in the software development lifecycle (SDLC). It is a structured technique for identifying, assessing, and planning to mitigate potential threats and vulnerabilities in software systems. By systematically analyzing the architecture of an application, data flows, and potential attack vectors, developers can gain a deeper understanding of the security threats they face. Integrating threat modeling into the SDLC promotes a security-first mindset from the beginning, ensuring that security is not an afterthought.

However, to ensure the security of the final product, threat modeling must be systematically integrated into all phases of the SDLC to ensure that the identified threats are appropriately addressed in later development phases. Such integration of threat modeling into the SDLS helps prioritize security efforts and provides the basis for security analysis throughout the SDLC. Overall, it facilitates the development of robust security controls that reduce the likelihood of vulnerabilities and mitigate potential risks. However, this integration is currently largely implicit, potentially preventing the systematic consideration of identified threats in later phases of the SDLC.

Impact of threat modeling in the SDLC

The software development lifecycle has several phases, including requirements engineering, design, implementation, testing, deployment, and maintenance. Connecting threat modeling to each of these phases, rather than considering it as a single task in one phase, ensures that security is considered throughout the process. Overall, by integrating threat modeling into the SDLC, we strive for a continuous and iterative process that spans every development phase.

In the early planning and requirements engineering phase, developers should conduct a preliminary threat assessment by identifying potential threats, risks, and security objectives. This step provides a foundation for subsequent activities. It enables developers to systematically define security requirements, such as authentication, authorization, and data protection, right from the start. Currently, threat modeling is often solely coupled with this phase.

In the design phase, threat modeling influences architectural decisions and helps determine appropriate security controls. Developers should analyze the system architecture and data flows concerning the threats identified in threat modeling to identify potential more detailed threats and attack vectors. This way, developers can design systems with built-in security measures. The information taken from threat modeling informs the secure structuring of the system as well as the selection and implementation of appropriate security controls in the detailed system architecture.

During the implementation phase, threat modeling guides secure coding practices. Developers can proactively address potential vulnerabilities and incorporate security best practices. It guides the implementation of a secure system concerning the realized measures for mitigating the identified threats, including input validation, secure session management, and encryption. It also incorporates code analysis tools to identify and rectify potential security flaws by systematically checking the implementation for measures against the threats identified in threat modeling.

The testing phase involves comprehensive security testing, including penetration testing, vulnerability scanning, and security code reviews. In this phase, threat modeling supports these activities by providing knowledge that can be leveraged to validate the effectiveness of security controls in security testing. Further, threat modeling serves as a prioritization of testing activities. For example, by simulating relevant real-world attack scenarios identified in threat modeling, organizations can identify and address security weaknesses before deployment.

Organizations must also consider secure deployment practices and protect sensitive data during transmissions outside of the system itself, e.g., using virtual private networks. Accordingly, threat modeling also plays a crucial role in the deployment phase. It ensures secure configurations, including proper access controls and the protection of sensitive data. 

Lastly, threat modeling should be an ongoing process during the maintenance phase. As new threats emerge, developers must continuously monitor and update security measures to maintain secure software systems. Regular security updates, patch management, and proactive monitoring help maintain secure software. Here, threat modeling provides information on the impact of observed low-level vulnerabilities and helps in identifying other vulnerable system variants.

Challenges in integrating threat modeling into the SDLC

The integration of threat modeling into the SDLC as outlined above is primarily a traceability problem. The pure forward propagation and detailing of the identified threats in terms of planning appropriate mitigation measures is straightforward in most cases. The output artifacts of each step are passed to the next expert, who then tailors them according to his domain. For example, based on the list of identified and ranked threats, mitigation measures are incorporated into the system design. This design is then realized by developers by selecting appropriate libraries or implementing custom code to implement the mitigations in the implementation. 

The integration gets complicated as soon as the implementation has to be checked for compliance with the planned security design and whether all identified threats are mitigated in an appropriate way in the implementation. In this case, every identified threat has to be traced through multiple artifacts to the implementation to verify that it is mitigated there. When security violations are detected in the implementation, this tracing has to be performed in the opposite direction to assess the impact and consequences of the violation concerning the threat model. Manually, tracing is a labor-intensive and error-prone task that relies on much expert knowledge about the system. While one could systematically capture such knowledge in trace models, it has been shown that maintaining these models comes with a huge overhead that makes such approaches practically infeasible. In conclusion, we have to find lightweight means to systematically trace security-relevant aspects from threat modeling throughout the entire SDLC.

Another challenge is the different granularities at which security is considered in the phases of the SDLC. In threat modeling, security is often considered at a relatively coarse-grained level. Traditional threat modeling frameworks such as STRIDE consider high-level security aspects like spoofing or tampering with data. In contrast to this, security considerations on the implementation level often consider detailed low-level properties such as the secure usage of cryptographic APIs or buffer overflows. To relate such security aspects to the security properties considered in threat modeling, usually one has to bridge a huge gap. 
Usually, a mapping between the different security aspects is manually done in code reviews based on implicit expert knowledge and experiences. Currently, we lack the systematic coupling of security aspects across the SDLC that is necessary to integrate threat modeling with all phases of the SDLC.

Integration approaches in the literature

In the literature, various approaches have been proposed for systematically integrating threat modeling with different phases of the SDLC. Such approaches comprise the creation, maintenance, and recovery of traceability between threat models and other artifacts from the SDLC as well as means to check artifacts for compliance with threat models. In what follows, we give an overview of such approaches and discuss which aspects of the identified challenges these address, what are their limitations, as well as what is still unsolved.

* Empirical methodological challenges (Daniel +Sam) 
* Repeatability (Mehdi)
* Literature search dump (Sam)

