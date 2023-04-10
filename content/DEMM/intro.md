+++
title = "Maturity Model"
weight = 15
draft = false
+++


## Introduction

Maturity is a self-evaluation process conducted by the team. ODEF provides guidance and structure and assures that all the relevant areas are covered. The goal of the review process is to give a baseline that helps achieving a common understanding about the organization security posture.

### Dimentions

* Threat Detection Content
* Assurance
* Knowledge sharing

---
{{<mermaid align="left">}}

flowchart RL
    Assurance(Assurance) <--->Threat[Threat Detection Content]
    Knowledge[Knowledge sharing] <---> Assurance(Assurance)
    Knowledge[Knowledge sharing] <---> Threat(Threat Detection Content)
{{< /mermaid >}}

---

## Maturity levels

![demm](/images/demm.png)

### Level 1 - **Partial**

* Threat Detection Content
  * Organizational threat identification practices rely solely on external vendors to provide security content.
  * Assurance and context around alerts and detections is not provided or sufficient.
  * Risk is managed in an ad hoc and often reactive manner by relying on third parties.
* Assurance
  * There is some limited awareness of cybersecurity threat detection capabilities at the organizational level.
  * The organization implements threat validation and verification on an irregular, case-by-case basis due to varied experience or information gained from outside sources.
  * Assurance through continuous validation is not present.
* Knowledge sharing
  * The organization may not have processes to enable cybersecurity information sharing.
  * Documentation is rarely written and shared only on ad-hoc basis and it is scattered across teams.

### Level 2 - **Adequate**

* Threat Detection Content
  * Organizational threat identification practices rely on internal teams and external vendors to provide security content.
  * Context around alerts and detections is provided. Specialized teams are able to introduce new detections and security content.
  * Some security teams have a better understanding of security posture than others.

- Assurance
  * There is some awareness of cybersecurity threat detection capabilities as the organization is now building custom detections to compensate for gaps.
  * The custom detections are use case driven and validated during the detection development process.
  * Continuous validation is not enabled and the organization still relies on suppliers for most of the detection capabilities.
* Knowledge sharing
  * The organization is starting to enable knowledge sharing and promotes documentation efforts.
  * There is a central detection information repository.

### Level 3 - **Enabled (Proactive)**

* Threat Detection Content
  * Organization maintains continuous practices that provide excellent internal insights and knowledge. Context around alerts and detections is provided.
  * Any team is encouraged and capable to introduce new detection components and thus improve the security posture.
  * The security posture of the environment is well understood across the security teams.

- Assurance
  * The organization possesses a detection coverage map and covers a big percentage with in-house built detections. The organization does not rely on vendors to provide security content.
  * Automation is provided to continuously validate and run the detection use cases.
  * Additional assurance is achieved by running red team exercises and automation frameworks.
* Knowledge sharing
  * Organizations possess practices to create and maintain high quality records and appropriately control and manage the access to the information.
  * Processes for socializing detections are automated and teams are informed of the development of new detections.

## Operational Maturity

### Maturity Review Process (MRP)

The process of evaluating the maturity:

  <b>Collect</b> - Collect information about your processes,people and tools. Identify changes to any. The goal is to gain a holistic understanding of the organization's security teams, tools and processes. Based on that information various posture improvements can be identified.

  <b>Analize</b> - Based on the data that you have collected and find the corresponding maturity level. Finding where in the maturity level the organization is important for understanding the impact and importance of each identified security improvement initiative and thus prioritize accordingly.

  <b>Prioritize</b> - Prioritize and decide which is the next low hanging fruit that can be improved. Not all security issues are equally important, prioritization should focus on those initiatives that influence and change the security posture and introduce the most maturity.

  <b>Improve</b> - Create an initiative or a project for improving the identified gap.

### Security Improvement Initiative

Security improvement initiatives are likely outcomes of the MRP process. The goal of the security improvement initiative is to address identified visibility gaps in the organization's security posture. For example, during the review process or detection engineering we may identify that our application is not providing sufficient logging in order to detect particular behavior or ttp of interest. That is a good candidate for a security improvement initiative. The goal of the initiative would be to deliver the visibility needed and notify back the Detection Engineer so that they can proceed with the detection creation. Depending on the size of the organization and internal processes, this process might be driven by the Detection Engineer or completely separate team.

### DEMM Cadence

Evaluating the maturity of the organization and striving to improve it is no one time effort or activity. For that best results can be achieved by:

   Set a regular schedule for reevaluating and revisiting the DEMM.
   Ensure that the security improvement initiatives are targeted with a timeline and aligned with the overall organizational security strategy.