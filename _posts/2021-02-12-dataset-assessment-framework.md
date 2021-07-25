---
layout: single
title: "Dataset Assessment Framework"
categories:
  - Biometric compliance
tags:
  - biometric
  - compliance
  - gdpr
  - ccpa
---

<p align="center">
  <img src="/assets/images/GDPR_CCPA.jpeg" title="GDPR and CCPA" alt="accessibility text">
</p>

<figure class="align-left">
  <img src="/assets/images/GDPR_CCPA.jpeg" alt="">
</figure>

*With GDPR and CCPA, enforced cloud companies needs to comply data for fair usage. This is brief framework to get started …*

*For all those data science developer and companies who are are under the ambit of compliance, are the potential consumer of this framework.*

> **Risk = Asset (individual’s data) + Vulnerability + Threat**

Therefore, we need risk management, assessment and treatment with organisation defined ‘controls’.

*Formal definitions:*

Risk Management : The coordinated activities to direct and control an organisation with regards to risk.

Risk Assessment : The overall process of risk identification, risk analysis and risk evaluation.

Risk Treatment : The process to modify risk, using defined controls.

Let us consider how we capture natural person’s information. A practical approach to risk management for such dataset would be, a three step process:

## Step 1 :
**1. Asses Risk** — Data must NOT be:
Inaccurate, Insufficient or Out-Of-Date data,
Kept for too long (dormant account),
Excessive or Irrelevant information,
Disclosed to the wrong people,
Insecurely transmitted or stored,
Used in ways that are unacceptable or unexpected.

**2. Identify Risk** — Likelihood and level of severity must be set as Low, Medium and High.

<figure class="align-left">
  <img src="/assets/images/RiskAndCountermeasures.png" alt="">
</figure>

FIG-2 : Risk and countermeasures

<figure class="align-left">
  <img src="/assets/images/AssessTheCostsAndValue.png" alt="">
</figure>

FIG-3 : Assess the costs and value

## Step 2:
**1. Classify Data** — Data must have sufficient meta information and labeling, eg. : personal data, minor data, gender, special category like high-net-worth individuals, etc.

**2. Take Action Control** — The kind of treatment an organisation may deploy to take effective control over its dataset are:
- Reduce collected data,
- Pseudonyme information,
- Retention policy,
- Secure destruction of information, and purge mechanism,
- Access control,
- Training and awareness,
- Contracts or data-sharing agreements with 3rd party of Processor,
- Acceptable use policy in the SDK or APP,
- Subject access request process,

**3. Implement incident, management response** - Report the data breach to the supervising authority. This needs to be formally structured.

## Step 3:
Demonstrate ongoing risk and incident monitoring. Data protection is not a destiny, it’s a journey and hence embedding data protection should be the end goal. People, Process and Technology can enable it.

### Scenario

Let us consider we have a facial images dataset of natural persons and we would like to protect it:

Images of a natural person is biometric information, and it is considered to be sensitive data under Privacy Impact Assessment (PIA). Biometric verification must be consent based and hence the natural person MUST be aware of, what is it being used for. The adapted technology should make their lives more secure and easy and not the other way around.

With Anonymization, facial images coming from natural persons will be dis-associated from their identity and this is an irreversible process. But this process complies with the standards and such data can be utilized to make the models more robust. After all, real world facial images are hard to collect.

On the other hand, Pseudonymization is a process whereby a data cannot be attributed to a natural person without the use of additional information, but it will be considered Pseudonymized when this additional information (secret) is kept separately in a strongly secured place. This additional information is called tokenization. Such a technique is useful to store user biometric data for future validation.

To further mitigate the risk, natural persons facial images shall be converted to embeddings (e.g.: 128, 152 bytes long) and stored rather than raw images, this is done using facial AI models. The advantage here is that you can keep the user identity intact using Pseudonymization, but embedding data would be of no use unless the model that created it is unknown to the unauthorised person.

*Please leave a comment if you feel we can better this framework and yet keep it simple.*
