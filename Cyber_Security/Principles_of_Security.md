# Principles of Security
[Back to Cyber security page](./index.md)

---

## CIA Triad
[CIA_Triad](CIA_Triad.md)

---

##  Principles of Privileges
**Privileged Identity Management** : create a system role that is based on a users role/responsibilities with an organisation

**Privileged Access Management** : Manage the privileges a system access role had

---

## Security models
[Control_policies_and_models](Control_policies_and_models.md)

---

## Threat Modelling & Incident Response
 ### **STRIDE** 
|Principle|Description|
|:-:|:-|
|Spoofing|This principle requires you to authenticate requests and users accessing a system. Spoofing involves a malicious party falsely identifying itself as another.Access keys (such as API keys) or signatures via encryption helps remediate this threat.|
|Tampering	|By providing anti-tampering measures to a system or application, you help provide integrity to the data. Data that is accessed must be kept integral and accurate.|
|Repudiation|This principle dictates the use of services such as logging of activity for a system or application to track.|
|Information Disclosure|Applications or services that handle information of multiple users need to be appropriately configured to only show information relevant to the owner is shown.|
|Denial of Service|Applications and services use up system resources, these two things should have measures in place so that abuse of the application/service won't result in bringing the whole system down.|
|Elevation of Privilege|This is the worst-case scenario for an application or service. It means that a user was able to escalate their authorization to that of a higher level i.e. an administrator. This scenario often leads to further exploitation or information disclosure.|


### Computer Security Incident Response Team (CSIRT)

|Action|Description|
|:-:|:-|
|Preparation|Do we have the resources and plans in place to deal with the security incident?|
|Identification|Has the threat and the threat actor been correctly identified in order for us to respond to?|
|Containment|Can the threat/security incident be contained to prevent other systems or users from being impacted?|
|Eradication|Remove the active threat.|
|Recovery |Perform a full review of the impacted systems to return to business as usual operations.|
|Lessons Learned|What can be learnt from the incident? I.e. if it was due to a phishing email, employees should be trained better to detect phishing emails.|

---

### Source
- [tryhackme room](https://tryhackme.com/room/principlesofsecurity)