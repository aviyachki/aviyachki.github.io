+++
title = "Documentation Template"
weight = 19
draft = false
+++


Template should be used to standardize the detection content and create a knowledge base

## Detection Summary

| Status | **(developing/active/decommissioned)** |
| ----------- | ----------- |
| `Goal (Why)` | *The goal of the detection* |
| `TTP (What)` | *Mitre attack link*|
| `Strategy (How)` | *Query or short explanation about it* |
| `Automation (When)` | *Schedule and automation details*|
| `Sources (Where)` | *Data sources used for the detection* |
| `Severity` | *high/medium/low*|
| `Priority` | *high/medium/low*|

<details><summary><b>Research</b></summary>
<p>

### Goal

The goal section provides the intended purpose of the alert. It is a simple, plaintext description of the type of behavior you're attempting to detect and why.

#

### Categorization

The categorization is a mapping of the detection to the relevant entry in the MITRE ATT&CK. This is used in reporting with tools such as Mitre Att&CK Navigator to visualize coverage of TTPs and provide assurance. Additionally when a TTP is mapped to MITRE it can be used to perform attacker cyber attributed.  

#

### Technical Context

Technical Context provides detailed information and background needed for a responder or an engineer to understand all components of the detection.The goal of the section is to include technical research for the TTP and additionally how it relates to the environment. It can help incident responders to understand better the alert and also security engineers in order to address a technical security gap.

#

### Detection Summary

Is a high-level walkthrough of how the detection/hunt works. This describes what the alert is looking for, what technical data sources are used, any enrichment that occurs, and any false positive minimization steps.

#

### Severity

Severity is a measurement of impact. How much impact does an incident have on the overall security of the business? Some TTPs are clear indicator for attacker present in the environment, those will have higher severity than others. For example detection for dcsynch vs detection for received phishing email(without any confirmation for clicked link).

#

### Priority  

Priority should be based on the detection severity. The goal of prioritization is to allow your SOC analyst and Incident Responders to focus on the most pressing issues first.

#

</p>
</details>

<details><summary><b>Prepare</b></summary>
<p>

### Dataset

Identify the appropriate source of information which will be used in the detection and document it here.

#

### Visibility Check

Ensure there is sufficient logging, retention and visibility. Provide evidence (screenshots, json files etc) that prove that there is sufficient visibility and logging to collect and build detection logic.

#

</p>
</details>

<details><summary><b>Build & Enrich</b></summary>
<p>

### Detection Creation

Create a detection query against the identified dataset. Document the queries used here and provide details of the logic.

#

### Manual Testing

Perform manual testing against production data and ensure minimal False Positives. Document your test searches.

#

### Baseline development

Based on the results from your *manual testing* you may or may not need to develop a baseline. Baseline is a set of normal behaviours which are excluded from the detection to minimize noise and increase fidelity

#

### Blind Spots and Assumptions

Think about issues which could prevent your detection from alerting. For example, lack of visibility due to missing endpoint agent, or particular string which, in case is modified, the detection will not work etc.

#

### Unittest  Development

Create automated unittest that will cover:

1. Changes or missing data
2. Syntax errors
3. To confirm detection logic by performing true positive detection

#

### Enrich

Utilize or develop enrichment capability to support the detection if needed. There are external and internal sources of enrichment. In your pipeline or SIEM you should be able to interact with these sources and collect data as needed. For example, consider user behavioral analytic use case which requires to know when a user is on vacation - this would require access to an up-to-date HR database.

#

</p>
</details>

<details><summary><b>Validate</b></summary>
<p>

Validation are the steps required to generate a representative true positive event which triggers this alert. This can be a walkthrough of steps used to generate an alert, a script to trigger the detection (such as Red Canary's Atomic Red Team Tests), or a scenario used in an alert testing and orchestration platform.

Each alert / detection strategy must have true positive validation. This is a testing process designed to prove the true positives are detected.

#

### True positive validation

To perform positive validation:

* Generate a scenario where a true positive would be generated.
* Document the process of your testing scenario.
* From a testing device, generate a true positive alert.
* Validate the true positive alert was detected by the strategy.

### False positive validation

FP validation is yet another confirmation that when ran in production the detection is not producing excessive number of alerts from standard events in the organization - for example software compilation etc.

#

</p>
</details>

<details><summary><b>Automate</b></summary>
<p>

The idea of the section is to provide information on how the query is automated and what is the schedule of execution. Document any interaction between the different environments or applications that may be involved. For example, if your detection uses api calls to enrich from an HR database and then utilizes a scoring model from a micro service are interactions that should be documented here.  

#

</p>
</details>

<details><summary><b>Share</b></summary>
<p>

### Socialize the detection

Follow the process for socializing the detection with the receiving team/s (Fraud, SOC&IR, Engineering, Hunting etc). The receiving team should acknowledge and accept the new detection after performing a quality check.

#

### Response

The SOC and Incident Response teams should align the response to any alerts from the detection to their standard response playbooks - for malware, insiders etc. In case of absence of IR playbooks - the response plan can be documented here.
</p>
</details>

<details><summary><b>Appendix</b></summary>
Include any external links and references.
<p>

</p>
</details>
