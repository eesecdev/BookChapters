## Metrics in Secure Development Process: Challenges and Open Research Questions 


### Introduction


Metrics here, metrics there, metric everywhere! Metrics play a pivotal role in empirical software engineering research to systematically evaluate proposed techniques and methodologies. Furthermore, both practitioner and researchers use software metrics to systematically understand software artifacts and software development processes, which in turn can is used to improve developed software products and software development processes [3]. Despite their prevalence metrics in the context of secure software development processes remain under-explored. `The goal of this chapter is to help researchers in gaining an understanding of metrics usage in the context of secure development processes by providing a list of challenges, opportunities, and open research questions that are associated with metrics used in secure software development processes.` The book chapter summarizes discussion conducted at a breakout group as part of the Dagstuhl 23181 seminar.       

### Challenges 

The breakout group discussion started off with participants discussing the challenges that they faced or aware about when using metric for security. These challenges can be roughly divided into the following themes: sharing of metrics and metric-related data without revealing the identify of the sharing entity, disconnect between academia and industry on using metrics generated from research, and the implications of data collection differences between academia and industry. The consensus amongst the participants was that academic research has generated a plethora of metrics but many of these metrics are not reused in research and industry. Such notion questions the impact of prior security-related research that have proposed metrics. While research conducted by Morrisson et al. [1] and Meneely et al. [3] is a good step in this direction, participants emphasized on more research that will systematically investigate the reuse and potential of impact of proposed metrics in peer-reviewed publications. 

Participants also provided possible explanations on why proposed metrics are not reused. In the case of industry-based research, researchers often must oblige to non-disclosure agreements (NDAs), which prevents researchers to publicly disclose any information. Another possible explanation is that practitioners prefer to use simpler metrics, and often abandon complex metrics, i.e., metrics that require complex calculations. Furthermore, prior to using a metric, practitioners rely on expert opinion, and could abandon usage if there is lack of expert-driven evaluation or unavailability of an expert themselves. In all, reuse of metrics remains an unresolved issue, which has a lot of practitioner relevance.       


The discussion of the challenges also revealed opportunities for research. Participants in the breakout group mentioned metrics required to measure the attack surface of a software system. Recent work from Theisen et al. [2] came into discussion, which participants felt as a good starting point for metrics needed to measure attack surface. Metrics needed to measure secure development process as a whole for the constituting components, such as continuous integration, continuous deployment, and infrastructure as code. Metrics related to the evaluation of bypassing vulnerability mitigation strategies, and effectiveness of security static analysis tools also were discussed and identified as important.  


### Research Questions 


The discussion led to derivation of research questions that are related with metrics needed to empirically evaluate secure software development processes: 

- What strategies can we use to evaluate metrics when the ground truth is not available? 
- How can we determine the usefulness of metrics? 
- What metrics can we use to measure risk for interface designs? 
- How much evidence is required to demonstrate initial viability of a security metric? 
- What approaches can be used to incentivize use of security metrics? 
- How can we measure attack resilience of software-based systems? 
- What is the correlation between the count of layers for defense in depth and perceived security? 
- How does metric usefulness correlate with expertise and maturity? 

References: 
1.	Morrison, P., Moye, D., Pandita, R., & Williams, L. (2018). Mapping the field of software life cycle security metrics. Information and Software Technology, 102, 146-159. 
2.	Theisen, C., Munaiah, N., Al-Zyoud, M., Carver, J. C., Meneely, A., & Williams, L. (2018). Attack surface definitions: A systematic literature review. Information and Software Technology, 104, 94-103.
3.	Andrew Meneely, Ben Smith, and Laurie Williams. 2013. Validating software metrics: A spectrum of philosophies. ACM Trans. Softw. Eng. Methodol. 21, 4, Article 24 (November 2012), 28 pages. https://doi.org/10.1145/2377656.2377661 
