# Chapter on Software Supply Chain Security 

Overall idea: Highlight challenges and contrast with existing efforts from industry/academia to clarify which ones are covered (or at least worked on), and which ones, in our opinion, are not looked at sufficiently.



- Introduction, Motivation and Terminology
    - Roles (developers, suppliers, consumers)
    - Types of dependencies (across the stack and lifecycle, e.g. container deps, library deps or service providers invoked at runtime)
    - High-level challenge: "You got no choice really"
        -  Fabio: the whole point should be you have no choice really. From a security perspective a SBOM is like an arranged marriage. In some cases it is even a "picture-spouse marriage". Adoption reasons are not related to security, sometimes not even to functionality (e.g. the license is wrong or you have a developers team with experience in Java and even if there is something great in Rust you are not going to do a crosslanguage project). So the SBOM is "given".
        - Then, build trustworthy software out of untrusted component (and where are trust boundaries in the 1st place) is a derived challenge for security researchers.
    - Inhibiting innovation through regulation/controls (?)

- Visibility / Context Awareness
    - Lookup and comparison of alternative OSS components is difficult, e.g. to find components with equivalent features
        - See previous point. The point is not the comparison is the audit of a choice already made and what could be the mitigation measures.
    - Architecture comprehension
        - Automated discovery of component capabilities (in general, independent of specific use-cases)
        - Understand how a given component (which features) are used in a specific application context, esp. for transitive components
        - Which features are used, what kind of app data flows into the component and its data sinks, which functions and methods are used, etc.
    - Prioritization of vulns
        - Reachability vs. exploitability
        - Programming languages (?)
        - Different approaches: Shift-left vs. runtime agents
    - Debloating

- Metrics
    - Risk metrics (for better component selection and comparison), e.g. risk of maintainers disappearing or use of sensitive APIs
    - Existing works: Bus factor, OSSF Scorecards, [GUAC](https://github.com/guacsec/guac) (for entire dep trees), [Technical Leverage](https://techleverage.org/)
        - Key problem is that if you want a metric you want it to correlate with some outcome (See Alex talk), could be even be vulnerabilities. Otherwise it is just datascience dazzle. GUAC is an example of pointless datascience vacuum cleaner: gold might be there together with a huge pile of stones.
    - What are differences between metrics for commercial and OSS supply chain components (if any)?

- Benchmarks
    - Consumers can hardly verify security tool results (SBOM generators, or impact assessments based on data or control flow analysis, etc.)
    - Example SBOMs (use food analogy)
        - Define what should be included in SBOMs (cf. [The Minimum Elements For a Software Bill of Materials ](https://www.ntia.doc.gov/files/ntia/publications/sbom_minimum_elements_report.pdf)
        - Do documented checks (and corresponding attestations) make it unnecessary to keep track of every detailed component?
        - This will again result/require trust in private or public sector organizations (and their tools)
    - Increase tool verifiablity (does in-toto fit here?)
    - Creation and maintenance of independent Benchmarks à la https://www.dacapobench.org/ by independent, non-profit organizations

- Cloud Service Providers
    - [Shared Responsiblity Model](https://www.crowdstrike.com/cybersecurity-101/cloud-security/shared-responsibility-model/) for Cloud Security does not apply to OSS consumption. Maybe explain the main differences in a paragraph.
    - Fabio: the shared security model is just a lawyer's model. In the same way that software companies have transferred the blame for the security vulnerabilities that they ship to the users who don't update fast enough, the only purpose of the `shared' responsibility model is to put the blame on users for everything that happens, with the exception of cases in which this would be really outrageous. If you look at the table listing the security elements vs SaaS, PaaS and IaaS and who is to blame for which fault you will count the following occurrences: 10 CSP, 26 User. "Shared" in which sense?
    - Larger orgs follow a multi-cloud strategy to mitigate risks

- Human Factors
    - Summary of existing works (Dominique?)
    - What are the true costs of using open source components (e.g., to assess newly disclosed vulns, vet new component versions or perform updates)
    - What are problems if humans are not properly considered (their motivations, personal risks, ...)
        - Human-driven processes are not well-structured and bring a lot of insecurity
        - Comprimised developers or QA persons (even conctracters) pose a risk (cf. recent attacks)
        - (Non-)Usable tooling that does not fit into workflows, e.g. issue prioritization and documentation
        - Usable and acceptable authentication mechanisms for developers
        - Cognitive biases/conflicts of stakeholders, information needs, etc.
- Organizational Factors
    - are the inside human factors?

 
- The role of private orgs in supply chain security
    - Incentive structure
    - Participation in open source foundations (only strategic projects get a lot of attention)
    - For example, C# is heavily influenced by MS
    - Some can be considered critical infrastructure operators, e.g., package registries
        - Implicit trust assumptions of developers ("it's on npm, thus, it has been checked")
        - Should they be run by private organizations, despite their importance?
        - How comes that few people take decisions for the whole community?
        - How to design a secure package registry?
    - Incentivize information sharing of private orgs to prevent silos (e.g., every SCA vendor has its own public database with vuln info about open source components) 
