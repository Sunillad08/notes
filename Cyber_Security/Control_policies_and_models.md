# Control policies and models
[index](./index.md)
- --
## DAC
**Discretionary Access Control**
Gives total control to owner 
Security totally depended on owners wish and practices
![DAC|700](https://www.ekransystem.com/sites/default/files/mac_dac/graph3.jpg)
- --
## MAC
**Mandatory Access Control**
Restricts the ability of owners to grant or deny access
Rules are defined by system administrator and enforced by OS
Considered most secure
![MAC|700](https://community.aras.com/resized-image/__size/640x480/__key/communityserver-blogs-components-weblogfiles/00-00-00-00-04/6278.pastedimage1552931178963v6.png)
- --
## RBAC
**Role based access control**
assigning permissions to users based on role within organisation
Simple , manageable and roll based responsibilities
![RBAC|700](https://www.dnsstuff.com/wp-content/uploads/2019/10/role-based-access-control.jpg)
- --
Check [CIA_Triad](CIA_Triad.md)!
- --
## BIBA
Invented by Kenneth J. Biba
Used to maintain **Integrity**
Data and subjects grouped into ordered levels
Read and write on own level
No read down
No write up

3 Integrity Rules:

- SIMPLE INTEGRITY RULE:  **NO READ DOWN**
- STAR INTEGRITY RULE: **NO WRITE-UP**
- STRONG STAR INTEGRITY RULE : **NO READ WRITE UP DOWN**

![biba|700](https://media.geeksforgeeks.org/wp-content/uploads/20200709152715/Biba.png)
- --
## Bell-LaPadula
Invented by David Elliot Bell and Leonard J. LaPadula
Used to maintain **Confidentiality**
Read and write on own level
No read up
No write down

3 Confidentiality Rules:

- SIMPLE CONFIDENTIALITY RULE:  **NO READ UP**
- STAR CONFIDENTIALITY RULE: **NO WRITE DOWN **
- STRONG STAR CONFIDENTIALITY RULE:  **NO READ WRITE UP DOWN**

![bell-lapadula|700](https://media.geeksforgeeks.org/wp-content/uploads/20200709152516/BellLaPadula.png)
- --
### Source:
- Lecture notes from IT Infra
- [DAC](https://csrc.nist.gov/glossary/term/discretionary_access_control)
- [MAC](https://en.wikipedia.org/wiki/Mandatory_access_control)
- [geekforgeeks](https://www.geeksforgeeks.org/introduction-to-classic-security-models/)