## Metrics in Secure Development Process: Challenges and Open Research Questions 

### Contributors


- [Akond Rahman](https://akondrahman.github.io/) [Contact: akond.rahman.buet@gmail.com] 
- [Daniela Cruzes](https://www.ntnu.edu/employees/daniela.s.cruzes) [Contact: daniela.s.cruzes@ntnu.no]


### Introduction


Metrics here, metrics there, metric everywhere! Metrics play a pivotal role in empirical software engineering research to systematically evaluate proposed techniques and methodologies. Furthermore, both practitioner and researchers use software metrics to systematically understand software artifacts and software development processes, which in turn can is used to improve developed software products and software development processes [3]. Despite their prevalence, metrics usage in the context of secure software development processes remain under-explored. `The goal of this chapter is to help researchers in gaining an understanding of metrics usage in the context of secure development processes by providing a list of challenges, opportunities, and open research questions that are associated with metrics used in secure software development processes.` The book chapter summarizes discussion conducted at a breakout group as part of the Dagstuhl 23181 seminar.       

### Challenges 

The breakout group discussion started off with participants discussing the challenges that they faced or aware about when using metric for security. These challenges can be roughly divided into the following themes: sharing of metrics and metric-related data and disconnect between academia and industry on using metrics generated from research. We describe each of these themes briefly as follows: 

##### Challenge-1: Sharing of metrics and metric-related data

The first challenge related to metrics usage is sharing of metrics in a format accessible to practitioners and researchers. Due to lack of such a platform, even if practitioners and/or researchers are interested in using and evaluating a set fo metrics, collecting necessary data remains a challenge. The research community overall has started to realize this problem, and have started initiatives, such as the open science policy that allows practitioners and researchers to use metrics and metric-related data. The domain of secure software development process can also benefit from these initiatives. The participants realized that the in the case of industry-driven metrics, sharing of data can eb challenging. In that case, researchers need come up with a strategy on how to allow industry practitioners to share their data without revealing the identity. 

Another manifestation of this challenge is related to metrics usage is differences in data collection between academia and industry. Academics heavily rely on data sources that are publicly available through social coding websites, such as GitHub, and other research data sharing platforms, such as Zendoo. However, getting access to industry data especially in the context of secure software development remains a challenge. So far, one common practice amongst researchers is sign a non-disclosure agreement (NDA) contract, and access and analyze provided by the company by obliging to the NDA. Unlike open source data, industry data, therefore is harder to get access to, even if they are well-structured.     


##### Challenge-2: Disconnect between academia and industry on metrics usage 

The second challenge related to metric usage is inherent to the differences between academia and industry with respect to metric usage. In the case of academics, metrics are often used to evaluate a technique or a methodology for the publication. However, according to the breakout session participants, industry practitioners consider multiple factors while using metrics. For example, industry practitioners prefer `simpler` metrics, which will halp them to assess any evaluation criteria quickly. Expert opinion is also a consideration while using a metric. If an industry expert is supportive of a metric's usage, then that metric is likely to be adopted and used. Another factor is vocabulary differences for metrics. The meaning and implication of a metric can change when used in an industry setting.    


The consensus amongst the participants was that academic research has generated a plethora of metrics but many of these metrics are not reused in research and industry. Such notion questions the impact of prior security-related research that have proposed metrics. While research conducted by Morrisson et al. [1] and Meneely et al. [3] is a good step in this direction, participants emphasized on more research that will systematically investigate the reuse and potential of impact of proposed metrics in peer-reviewed publications. 

Participants also provided possible explanations on why proposed metrics are not reused. In the case of industry-based research, researchers often must oblige to non-disclosure agreements (NDAs), which prevents researchers to publicly disclose any information. Another possible explanation is that practitioners prefer to use simpler metrics, and often abandon complex metrics, i.e., metrics that require complex calculations. Furthermore, prior to using a metric, practitioners rely on expert opinion, and could abandon usage if there is lack of expert-driven evaluation or unavailability of an expert themselves. In all, reuse of metrics remains an unresolved issue, which has a lot of practitioner relevance.       

### Opportunities 


The discussion of the challenges also revealed opportunities for research. Participants in the breakout group mentioned metrics required to measure the attack surface of a software system. Recent work from Theisen et al. [2] came into discussion, which participants felt as a good starting point for metrics needed to measure attack surface. Metrics needed to measure secure development process as a whole for the constituting components, such as continuous integration, continuous deployment, and infrastructure as code. For automated computing infrastructure management these practices play a pivotal role, and there are research opportunities in collecting, curating, and validating a set of novel metrics that can advance the state of the art for secure development and operations (DevSecOps) research [4]. Metrics related to the evaluation of bypassing vulnerability mitigation strategies, and effectiveness of security static analysis tools also were discussed and identified as important.  

At the beginning of the discussion process, the discussion leads discussed a paper from Pendleton et al. [5], which provides a survey of existing security metrics. The authors of the paper [5] provided a framework to categorize system-level security metrics that included the following categories: (i) system vulnerabilities; (ii) metrics of defense power; (iii) metrics of attack or threat severity; and (iv) metrics of situations. The participants found the paper useful, and felt some of these metrics can be used in the domain of secure software development process. Some participants stressed the importance of re-applying a similar survey design of existing software security metrics.   


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

The participants believed that this set of research questions have not been addressed in research, and provides ample opportunities for graduate students who are interested to do research in this field.   

References: 
1.	Morrison, P., Moye, D., Pandita, R., & Williams, L. (2018). Mapping the field of software life cycle security metrics. Information and Software Technology, 102, 146-159. 
2.	Theisen, C., Munaiah, N., Al-Zyoud, M., Carver, J. C., Meneely, A., & Williams, L. (2018). Attack surface definitions: A systematic literature review. Information and Software Technology, 104, 94-103.
3.	Andrew Meneely, Ben Smith, and Laurie Williams. 2013. Validating software metrics: A spectrum of philosophies. ACM Trans. Softw. Eng. Methodol. 21, 4, Article 24 (November 2012), 28 pages. https://doi.org/10.1145/2377656.2377661 
4. A. A. U. Rahman and L. Williams, "Software Security in DevOps: Synthesizing Practitioners’ Perceptions and Practices," 2016 IEEE/ACM International Workshop on Continuous Software Evolution and Delivery (CSED), Austin, TX, USA, 2016, pp. 70-76.
5. Pendleton, M., Garcia-Lebron, R., Cho, J. H., & Xu, S. (2016). A survey on systems security metrics. ACM Computing Surveys (CSUR), 49(4), 1-35.