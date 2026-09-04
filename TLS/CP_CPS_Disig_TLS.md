
# Disig TLS Certificate Policy and Certification Practice Statement (CP/CPS)


**Disig, a.s.**  
**Version 7.4**  
**Valid from September 4, 2026**  
**OID 1.3.158.35975946.0.0.0.1.1**

Copyright © 2026 Disig, a.s. 
This work is licensed under the [CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0/) license.

This document has not been proofread.
Trademarks: Product names mentioned herein may be trademarks of the firms.

## Table of contents
- [1. Introduction](#1-introduction)
  - [1.1 Overview](#11-overview)
  - [1.2 Document Name and Identification](#12-document-name-and-identification)
  - [1.3 PKI Participants](#13-pki-participants)
  - [1.4 Certificate Usage](#14-certificate-usage)
  - [1.5 Policy administration](#15-policy-administration)
  - [1.6 Definitions and Acronyms](#16-definitions-and-acronyms)
- [2. Publication and Repository Responsibilities](#2-publication-and-repository-responsibilities)
  - [2.1 Repositories](#21-repositories)
  - [2.2 Publication of information](#22-publication-of-information)
  - [2.3 Time or frequency of publication](#23-time-or-frequency-of-publication)
  - [2.4 Access controls on repositories](#24-access-controls-on-repositories)
- [3. Identification and Authentication](#3-identification-and-authentication)
  - [3.1 Naming](#31-naming)
  - [3.2 Initial identity validation](#32-initial-identity-validation)
  - [3.3 Identification and authentication for re-key requests](#33-identification-and-authentication-for-re-key-requests)
  - [3.4 Identification and authentication for revocation request](#34-identification-and-authentication-for-revocation-request)
- [4. Certificate Life-Cycle Operational Requirements](#4-certificate-life-cycle-operational-requirements)
  - [4.1 Certificate Application](#41-certificate-application)
  - [4.2 Certificate application processing](#42-certificate-application-processing)
  - [4.3 Certificate issuance](#43-certificate-issuance)
  - [4.4 Certificate acceptance](#44-certificate-acceptance)
  - [4.5 Key pair and Certificate usage](#45-key-pair-and-certificate-usage)
  - [4.6 Certificate renewal](#46-certificate-renewal)
  - [4.7 Certificate re-key](#47-certificate-re-key)
  - [4.8 Certificate modification](#48-certificate-modification)
  - [4.9 Certificate revocation and suspension](#49-certificate-revocation-and-suspension)
  - [4.10 Certificate status services](#410-certificate-status-services)
  - [4.11 End of subscription](#411-end-of-subscription)
  - [4.12 Key escrow and recovery](#412-key-escrow-and-recovery)
- [5. MANAGEMENT, OPERATIONAL, AND PHYSICAL CONTROLS](#5-management-operational-and-physical-controls)
  - [5.1 Physical security controls](#51-physical-security-controls)
  - [5.2 Procedural controls](#52-procedural-controls)
  - [5.3 Personnel controls](#53-personnel-controls)
  - [5.4 Audit logging procedures](#54-audit-logging-procedures)
  - [5.5 Records archival](#55-records-archival)
  - [5.6 Key changeover](#56-key-changeover)
  - [5.7 Compromise and disaster recovery](#57-compromise-and-disaster-recovery)
  - [5.8 CA or RA termination](#58-ca-or-ra-termination)
- [6. Technical Security Controls](#6-technical-security-controls)
  - [6.1 Key pair generation and installation](#61-key-pair-generation-and-installation)
  - [6.2 Private Key Protection and Cryptographic Module Engineering](#62-private-key-protection-and-cryptographic-module-engineering)
  - [6.3 Other aspects of key pair management](#63-other-aspects-of-key-pair-management)
  - [6.4 Activation data](#64-activation-data)
  - [6.5 Computer security controls](#65-computer-security-controls)
  - [6.6 Life cycle technical controls](#66-life-cycle-technical-controls)
  - [6.7 Network security controls](#67-network-security-controls)
  - [6.8 Time-stamping](#68-time-stamping)
- [7. Certificate, CRL, and OCSP profiles](#7-certificate-crl-and-ocsp-profiles)
  - [7.1 Certificate profile](#71-certificate-profile)
  - [7.2 CRL profile](#72-crl-profile)
  - [7.3 OCSP profile](#73-ocsp-profile)
- [8. Compliance Audit and Other Assessments](#8-compliance-audit-and-other-assessments)
  - [8.1 Frequency or circumstances of assessment](#81-frequency-or-circumstances-of-assessment)
  - [8.2 Identity/qualifications of assessor](#82-identityqualifications-of-assessor)
  - [8.3 Assessor's relationship with assessed entity](#83-assessors-relationship-with-assessed-entity)
  - [8.4 Topics covered by assessment](#84-topics-covered-by-assessment)
  - [8.5 Actions taken as a result of deficiency](#85-actions-taken-as-a-result-of-deficiency)
  - [8.6 Communication of results](#86-communication-of-results)
  - [8.7 Self-Audits](#87-self-audits)
- [9. Other Business and Legal Matters](#9-other-business-and-legal-matters)
  - [9.1 Fees](#91-fees)
  - [9.2 Financial responsibility](#92-financial-responsibility)
  - [9.3 Confidentiality of business information](#93-confidentiality-of-business-information)
  - [9.4 Privacy of personal information](#94-privacy-of-personal-information)
  - [9.5 Intellectual property rights](#95-intellectual-property-rights)
  - [9.6 Representations and warranties](#96-representations-and-warranties)
  - [9.7 Disclaimers of warranties](#97-disclaimers-of-warranties)
  - [9.8 Limitations of Liability](#98-limitations-of-liability)
  - [9.9 Indemnities](#99-indemnities)
  - [9.10 Term and termination](#910-term-and-termination)
  - [9.11 Individual notices and communications with participants](#911-individual-notices-and-communications-with-participants)
  - [9.12 Amendments](#912-amendments)
  - [9.13 Dispute resolution provisions](#913-dispute-resolution-provisions)
  - [9.14 Governing law](#914-governing-law)
  - [9.15 Compliance with applicable law](#915-compliance-with-applicable-law)
  - [9.16 Miscellaneous provisions](#916-miscellaneous-provisions)
  - [9.17 Other provisions](#917-other-provisions)
  

# 1. Introduction
This document is a combined Certificate Policy and Certification Practice Statement (CP/CPS) of the company Disig, a.s., with its registered office at Galvaniho 17/C, 821 04 Bratislava - mestská časť Ružinov, National Trade Register number: 35975946, registered in the Business Register of the City Court Bratislava III Section: Sa Insert No.: 3749/B, as a Trusted Service Provider (hereinafter referred to as "Provider") and applies to the root certification authorities and their subordinate certification authorities listed in Section 1.4.1 operated by the Provider, through which it provides trusted services for issuing publicly trusted TLS server Certificates (hereinafter referred to as the "TLS Certificate").  
It defines:  
Certificate Policy (CP) - the policies and rules under which TLS Certificates are issued, managed, and used, and  
Certification Practice Statement (CPS) - the detailed procedures and practices that the Provider implements to comply with this CP.

Publicly‐Trusted TLS Server Certificates issued to end users uniquely identify the entity to which the TLS Certificate is issued and bind this entity to the corresponding key pair. Unless the CP/CPS explicitly states that it refers to a root certification authority or subordinate certification authority TLS Certificate, the word "TLS Certificate" means the Publicly‐Trusted TLS Server Certificate of the end entity.

The Provider's website for the provided trusted services is available here:
[https://eidas.disig.sk](https://eidas.disig.sk)

## 1.1 Overview

This CP/CPS defines the creation and management of publicly trusted TLS Server Certificates in accordance with the current versions of the applicable requirements identified below:  
* the Baseline Requirements for the Issuance and Management of   Publicly-Trusted TLS Server Certificates (hereinafter referred to as  the “TLS BR”) [3];   
* the Microsoft Trusted Root Program Requirements [4], Mozilla Root  Store Policy [5], Apple Root Program Policy [6], and Chrome Root Program Policy [7];    
* the CCADB Policy [24];  
* Regulation (EU) No 910/2014, as amended (hereinafter referred to as ‘eIDAS’)[8]; and  
* ETSI EN 319 401 [9] and ETSI EN 319 411-1 standards. [10]. 

This CP/CPS is structured in accordance with RFC 3647 [11].

The Provider confirms that this CP/CPS takes account of all requirements of the current version of TLS BR [3], which is published at [https://cabforum.org/working-groups/server/baseline-requirements/documents/](https://cabforum.org/working-groups/server/baseline-requirements/documents/).

In the event of any inconsistency between these requirements and this CP/CPS, the requirements of the current version of TLS BR [3] prevail.

The Provider explicitly states that the publicly-trusted CA hierarchies covered under this CP/CPS are not used for enterprise-only or locally-trusted use cases. For internal, enterprise, or non-public deployment, the CA offers and maintains dedicated private PKI hierarchies that are operationally and logically segregated from its publicly-trusted hierarchies.

The Provider explicitly states that the publicly trusted CA hierarchies covered by this CP/CPS adhere to the latest published versions of the Chrome Root Program Policy [7] and the CCADB Policy [24].

## 1.2 Document Name and Identification

|  | |
| :--- | :--- |
| Document Name:|**Disig TLS Certificate Policy and Certification Practice Statement (CP/CPS)** |
| Name abbreviation: | **CA Disig TLS CP/CPS** |
| Version:|  **7.4** |
| Approved on:| **August 25, 2026**   |
| Valid from:| **September 4, 2026**    |  
|This document is assigned to an object identifier (OID):|**1.3.158.35975946.0.0.0.1.1** |  
 

Description of the object identifier (OID):  
 1\.  - ISO assigned OIDs  
 1.3.  ISO Identified Organization  
 1.3.158.  -  Identification number (Company ID - ICO)    
 1.3.158.35975946. - Disig, a. s.  
 1.3.158.35975946.0.0.0.1.  - CA Disig  
 1.3.158.35975946.0.0.0.1.1 - CA Disig TLS CP/CPS  

This OID (1.3.158.35975946.0.0.0.1.1) is also listed in issued TLS Certificates and covers these policies from the standard [10]:

|Policy name|OID|Description/ETSI policy|  
|-----------|---|----------------------|
|LP: 	Lightweight Certificate Policy|0.4.0.2042.1.3|ETSI EN 319 411-1 LCP|
|OVCP: 	Organizational Validation 	Certificate Policy|0.4.0.2042.1.7|ETSI EN 319 411-1 OVCP|
|NCP: 	Normalized Certificate Policy|0.4.0.2042.1.1|ETSI EN 319 411-1 NCP|  

###  1.2.1 Revisions

|Revision  |Revision date  |Description; Reviewer|  
|:--------:|:-------------:|---------------------|
|1.0|2006/03/25|First version; Miskovic|  
|1.5|2006/12/20|Formal text editing - Formatting, correcting links, editing text in section 4 "Operational requirements"; Miskovic|  
|2.0|2007/01/23|CP expansion in relation to the new type of TLS Certificate issued to the contracted client. Addition of section 7 "Certificate Profiles"; MiSkovic|  
|2.1|2007/03/29|Correcting text in chap. 2.8 and Chap. 4.9; Text editing related to a minor change in a partner's TLS Certificate; Miskovic|  
|3.0|2008/03/19|Overall revision of the CP for each type of TLS Certificate; Durisova, Miskovic|  
|3.1|2008/06/24|A new type of TLS Certificate adding.; Miskovic|
|3.2|2008/11/10|Change TLS Certificate validity for domain user PKI VsZP; Termination of operation at Zahradnicka 153; Miskovic|
|3.3|2008/11/25|Editing the wording:section 3.1.9 - Domain ownership verification: section 4.1.1; 4.1.2, - validation of the Applicant's e-mail address; Miskovic|  
|3.4|2009/06/02|Modification regarding the requirement for the minimum length of the public key to be issued by CA Disig (section 5.1.3; 6.1.2);Change the email address location in the TLS Certificate<br> profile (section 3.1.2; 6.1.2); Miskovic|
|4.0|2009/10/10|Editing in connection with Mozilla Foundation requirements when applying for a CA Disig TLS Certificate to the Mozilla Root Certificate Store; Miskovic|
|4.1|2010/05/11|Inclusion of proposed audit corrective actions of 13.11.2009 (audit according ETSI TS 102042 V1.3.4); Miskovic|
|4.2|2011/03/03|Changing the validity of TLS Certificates; incorporating Mozilla Foundation's new security policy requirements and Microsoft code signing requirements; formal edits of tables and texts; Miskovic|
|4.3|2012/01/25|Supplementing the possibility to issue TLS Certificate for subordinate CAs, adding signature algorithms, and regular annual review of content; Miskovic|
|4.4|2012/06/22|Incorporating Requirements for the Baseline Requirements for Issuing and Managing Publicly-Trusted Certificates, v.1.0, issued by the CA / Browser Forum;  Miskovic|
|4.5|2013/08/15|Refining of CA Disig CA root CA Certificate Profile and other Certified Types of Certificates; Miskovic|
|4.6|2013/06/21|Correction of the OID of the document - deleting the version of the document from the OID (section 1.2). Editing Profiles for subordinate CAs - TLS Certificate Policies Identifier (section 7.1.2);<br> Enable issuing "wildcard" TLS/SSL TLS Certificates to be issued at the third level of the domain name (3.1.2); Miskovic|
|4.7|2015/02/02|Z Inclusion of the requirements of the current version of the Baseline Requirements for the Issue and Management of Publicly-Trusted Certificates, v.1.2.3; Revision of the CP in connection with<br> the amendment to the Electronic Signature Act, pursuant to Act no. 305/2013 Coll.; Miskovic|
|4.8|2015/05/22|Verification of CAA records (4.1.5); Miskovic|
|4.9|2016/10/10|Changes made in connection with the eIDAS Regulation and in connection with the expiry of Act no. 215/2002 Coll. and the entry into force of Act no. 272/2016 Z. z.; Inclusion of Baseline Requirements<br> for Issuance and Management of Publicly-Trusted Certificates, to Version v.1.4.1; Miskovic|
|5.0|2017/09/25|Conversion of CP to RFC 3647 format; Inclusion of eIDAS requirements and incorporation of the requirements of the current version of Baseline Requirements for the Issuance and Management<br> of Publicly-Trusted Certificates, v.1.5.2; Miskovic|
|5.1|2018/05/23|Entry into force of Regulation no. 2016/679 - GDPR; Modification of the wording of point 1.3.3; amendment of the wording of point 3.2.2.4 (new verification method); addition of clause 4.2.2 (gTLD);<br> addition of item 4.9.11 (OCSP stapling); Miskovic|
|5.2|2019/05/17|Modifying section 4.9 in accordance with the Baseline Requirements for Issuance and Management of Publicly-Trusted Certificates, v.1.6.1; Modifying section 8.4 in accordance with<br> the Baseline Requirements for Issuance and Management of Publicly-Trusted Certificates, v.1.6.5; Clarification of the definition in section 1.3.1; Addition of section 3.1.4; Miskovic|
|5.3|2019/12/02|Editing the TLS Certificate profile for electronic signature (3.1.4.1.); modification of the validity of issued TLS Certificates for signature / seal (7.1.4); Update links (1.6.3.);<br> Shortcuts and minor text edits; Miskovic|
|5.4|2020/09/01|Modification of the validity of TLS / SSL TLS Certificates in accordance with the requirements [3]. Specification of domain ownership verification methods in section 3.2.2.4;<br> Changing the titles of sections according to their titles in [3]; Miskovic|
|5.5|2021/05/20|Addition of the method of reporting incidents (2.2); Shelf life of data used to verify domain ownership (3.2.2.4); Method of reporting compromise of the CA private key by third parties (4.9.12); Miskovic|
|5.6|2022/05/20|Removing an OU field from the TLS Certificate profile (3.1.4.3); Modification of the requirements for obtaining audit records in accordance with the requirements [3] version 1.8.4 (5.4);<br> changing the TLS / SSL TLS Certificate type designation to TLS; Miskovic|
|5.7|2022/10/01|Changes in connection with the requirement to publish revocation reasons in CRL when revoking issued TLS Certificates (4.9.1.1; 4.9.2; 4.9.3; 7.2.2)|
|5.8|2023/04/20|Changes in connection with the creation of a new subordinate CA Disig R2I5; Miskovic|
|5.9|2023/09/01|Changes in connection with the entry into force of "Baseline Requirements for the Issuance and Management of Publicly-Trusted S/MIME Certificates"; Miskovic|
|6.0|2024/02/01|Allocation of CP exclusively for the policy of issuing Publicly-Trusted TLS Certificates; Miskovic|
|6.1|2024/07/18|Change of headquarters of Disig, a.s., Addition of the requirement for the use of "zlint" (4.3.1), Modification of the scope of extensions in section 7.1.2.7; Miskovic|
|6.2|2024/08/15|Extension of domain validation methods by DNS Change method in accordance with TLS Baseline Requirements section 3.2.2.4.7; Miskovic|
|6.3|2025/01/10|Termination of use of domain verification methods in accordance with sections 3.2.2.4.2 and 3.2.4.15 as of 15.1.2025;. introduction of new domain verification methods (3.2.2.4.13 and 3.2.2.4.14);<br> addition of the document to the section "Multi-perspective release confirmation" (3.2.2.9); Modification of section 4.9.9; Miskovic|
|6.4|2025/09/01|Change in the methods used for domain validation (3.2.2.4); Consideration of the requirements of section 6.1.3 Mozilla Root Store Policy v. 3.0 (4.9.5); Mass Revocation Plans (5.7.1.2); Miskovic|
|7.0|2026/03/05|Transformation of the document into a new form of a combined policy for providing the service of issuing publicly trusted TLS Certificates, which also includes the rules for providing this service,<br> which were originally the subject of a separate document. Addition of a new single-purpose CA Disig TLS Root R3 and its subordinate CA Disig R3I1 TLS Certificate Service (1.3.1.2);<br> Addition of information and profiles related to cross-TLS Certificates. (7); Miskovic|
|7.1|2026/04/21|Addition of information about the issued subordinate CA Disig R3I1 TLS Certification Service and Cross Certificate CA Disig TLS Root R3 - CA Disig Root R2 (1.3.1.12); Addition of links to the test web site for valid, expired and revoked TLS certificates (2.2.4); Addition of time frames to chapter 4.2.1; Updates to the validity period of TLS certificates for end users (6.3.2); Miškovič|
|7.2|2026/06/15|Addition of information regarding automatic issuance of TLS certificates via the ACME protocol (1.3.1;1.3.3; 2.2; 3.2.2.8; 4.1.2; 4.1.2.1; 4.1.2.2; 4.1.2.3; 4.2.1; 4.6.1) Miškovič|
|7.3|2026/07/20| Change of "Key Usage" for Subscriber (Server) Certificate Profile to Critical (7.1.2.7); Miškovič|
|7.4|2026/09/04| CP/CPS Update Based on Apple Review; Miškovič|

##  1.3 PKI Participants  

###  1.3.1 Certification Authorities  

Root CA is the top-level Certification Authority whose Root Certificate is distributed by Application Software Suppliers. Root CA issues Subordinate CA Certificates.
Subordinate CA is a Certification Authority whose Certificate is signed by Root CA, or another Subordinate CA.    
This CP/CPS applies to the provision of trust services by subordinate certification authorities that fall under one of the CA hierarchies operated by a provider for issuing publicly trusted TLS certificates, as described below.  
Issuing subordinate certification authorities support automated certificate lifecycle management. The Provider operates an automated Application Programming Interface (API) based on the ACME protocol in strict compliance with RFC 8555 for the exclusive issuance of Organization Validated (OV) TLS certificates.   
Anonymous account registration is prohibited; the Provider strictly enforces External Account Binding (EAB) to ensure that automated issuance is restricted solely to pre-vetted and authorized subscriber organizations.

####  1.3.1.1 Multi-purpose CA Hierarchy  
This hierarchy includes root CA and issuing subordinate CA, which represents the legacy CA structure operated by the Provider since its acceptance as a publicly trusted TLS Certificate provider under the corresponding root CA programs accepted by Microsoft, Mozilla, Google, and Apple.   
The hierarchy will be used to issue TLS Certificates to end users only until it is replaced by a new single-purpose hierarchy (see 1.3.1.2).


| | |
|:--- |:--- |
|Name:                     |**CA Disig Root R2**|
|Certificate serial number:|**0092B888DBB08AC163**|
|Thumbprint (sha1) (DER):  |**B561EBEAA4DEE4254B691A98A55747C234C7D971**|
|Thumbprint (sha256) (DER):|**E23D4A036D7B70E9F595B1422079D2B91EDFBB1FB651A0633EAA8A9DC5F80703**|
|Comment:                  |**It issues Certificates only for subordinate certification authorities of the Provider.**|  

 

| | |
|:--- |:--- |
|Name:                       |**CA Disig R2I2 Certification Service**|
|Certificate serial number:  |**081792523668f5c8500000000000000003**|
|Issuer:|**CA Disig Root R2**|
|Thumbprint (sha1) (DER):    |**19F2783DEDD8561A61C682932EE9D5B4D86B00CE**|
|Thumbprint (sha256) (DER):  |**C96F24C45113FD91AE2F9E40E106653BFA0FFBCFA07E209524C844E7C8DA4148**|
|Comment:                    |**It issues only TLS Certificates to end users (see 3.1.4.3)**|

| | |
|:--- |:--- |
|Type:                       |**Cross-Certificate**|
|Name:                       |**CA Disig TLS Root R3**|
|Certificate serial number:  |**0864417EE567132EBA0000000000000011**|
|Issuer:|**CA Disig Root R2**|
|Thumbprint (sha1) (DER):    |**469EDA6B6A016F30617D8504883C1E39C21188FD**|
|Thumbprint (sha256) (DER):  |**1E4CF8FA6ADA4DB81C33BB8E4BF73B8D29E99C119FF0B7A42D58032366F56509**|
|Comment:                    |**It is Cross-Certificate between CA Disig TLS Root R3 and CA Disig Root R2**|


#### 1.3.1.2 Single-purpose TLS CA  
This CA hierarchy replaces the legacy CA hierarchy (see 1.3.1.1) currently used to issue TLS Certificates to end users. This single-purpose TLS CA hierarchy already fully complies with the current TLS BR [3], where new root CAs are required to have a separate CA hierarchy for issuing TLS Certificates to end users and are limited to issuing Certificates containing only id-kp-serverAuth in the EKU extension (1.3.6.1.5.5.7.3.1).  

|  | |
| :--- | :--- |
| Name:                     |**CA Disig TLS Root R3**|
| Certificate serial number:|**5B99ABC2B008CF8441D62E523909B41B**|
| Thumbprint (sha1)(DER):   |**AF250F267724C554652607D70985DE93DD33AFC0**|
| Thumbprint (sha256)(DER): |**6248199FEA4811FD34AA96EF0A26DE52134B73A9A2A99678F0C2EBADF8663EF8**|  
| Valid from:               |**September 18, 2025**|
| Valid to:                 |**September 14, 2040**| 
| Comment:                  |**It issues certificates only for the Provider's subordinate certification authorities reserved for issuing TLS certificates.**|  

 
|  | |
| :--- | :--- |
| Name:                     |**CA Disig R3I1 TLS Certification Service** |
| Issuer:                   |**CA Disig TLS Root R3**|
| Certificate serial number:|**09B6A42D17F4DEBBEE0000000000000001**|
| Thumbprint (sha1)(DER):   |**A7AABAD5DCA33457B5D3A4C62BBEA377096CE898**|
| Thumbprint (sha256)(DER): |**285C50885D41DF6BB1632B78E979750D89F5DBB995D8EA3496CEF40A446397E7**|
| Valid from:               |**April 13, 2026**|
| Valid to:                 |**April 12, 2029**| 
| Comment:                  |**It issues only TLS Certificates to end users (see 3.1.4.3).**|  

###  1.3.2 Registration Authorities ### 
The Registration Authority ("RA") is an entity that under contract conducts certain selected activities in the provision of trusted services on behalf of the Provider.
The RA shall conduct its activities in accordance with this CP/CPS.    

Provider may establish following types of RA:  
* **Internal RA** - is operated by the Provider and is intended to provide trusted services for all interested parties. This RA is not a separate legal body.  

The generation of access keys and the issuance of authentication TLS Certificates in X.509 format for internal RA staff member (hereinafter referred to as the "RA staff member") are performed by authorized employees of the Provider. The access keys of each RA staff member are stored on a hardware device (smart card), where access to the keys is protected by an access password chosen by the RA staff member himself. This ensures two-factor authentication when issuing a TLS Certificate through the Provider's IS.  

### 1.3.3 Subscribers
The subscriber is understood to be a natural person or a legal person that is entitled to request a TLS Certificate on behalf of an entity whose name appears as the subject in the TLS Certificate - Certificate holder.  

The Certificate holder may be:
* A device or system operated by a natural or legal person or operated on behalf of a natural or legal person.  

When a Subscriber is the subject, it will be held personally responsible if its obligations are not correctly fulfilled.
Responsibilities of the Subscriber and of the subject are addressed in the General Terms of Service and Use of the Trusted Certificate Issuance and Verification Service " (the "General Terms") [12] published at the Provider's website (see Section 1).
This CP/CPS defines the requirements that the Subscriber shall meet.  

Formal Certificate holder means a natural person who undertakes to use a corresponding private key and a TLS Certificate in accordance with this CP/CPS.  

When applying for a TLS certificate for a device or system operated by or on behalf of a natural or legal person, the Subscriber is:
* The natural or legal person operating the device or system.
* Any entity as allowed under the relevant legal system to represent the legal person; or
* A legal representative of a legal person subscribing to his subsidiaries.  

Subscribers permitted to utilize the ACME automated issuance workflow are strictly limited to legally established organizations that have successfully completed the out-of-band identity validation process with the Provider and have been provisioned with valid EAB credentials.

### 1.3.4 Relying Parties  
Relying party is a natural or legal person who relies, in their proceedings, on the electronic identification or trusted services of the Provider.  

### 1.3.5  Other Participants   
The category of "other participants" includes entities that are not the Provider's CA, Registration Authority (RA), Subscribers or relying party, but have an impact on the provision or use of services under this CP/CPS. These entities include in particular:  

#### 1.3.5.1 Policy Management Authority  
Policy Management Authority - PMA is a component provided for the purpose:  
* Supervising the CP/CPS creation and updating including the evaluation of plans to implement any of the changes.
* Reviewing CP/CPS to ensure that the Provider's practice complies with its requirements 
* Reviewing of audits findings, to determine whether Provider adequately complies with approved CP/CPS.
* Giving recommendations for Provider regarding corrective actions and other appropriate measures.
* Giving advice regarding the suitability of the TLS Certificates associated with the CP/CPS for specific management applications and managing activities of the certification authority and registration authority.
* Interpretation of the CP/CPS and its instructions for RA and CA.
* Performing the internal audit of the Provider, by assigning this to an independent employee.
* Ensuring that the adopted and approved CP/CPS are implemented duly and properly implemented.

PMA represents the top component, which shall decide finally on all matters and aspects related to the Provider and its activities.  

#### 1.3.5.2 Conformity assessors (auditors)
Conformity assessors are independent organizations that, based on accreditation, assess the Provider's compliance with:
* relevant standards (e.g. ETSI EN 319 401, ETSI EN 319 411-1, or other relevant standards),
* this CP/CPS and related internal policies of the Provider,
* requirements of the Trusted Root CA and/or CCADB programs.  

Conformity assessors:
* have the right to request access to the necessary documents, records, and systems from the Provider to the extent necessary to conduct the audit;
* are bound by a confidentiality obligation to the extent agreed in the contract with the Provider and in accordance with the applicable law;
* do not provide any TLS Certificate issuance services, key management, or CA/RA functions.  

The provider shall ensure that relations with conformity assessors are regulated by a written contract and that there is no conflict of interest.  

#### 1.3.5.3 Supervisory bodies and operators of trusted root programs
Supervisory bodies and operators of trusted root programs are entities that exercise statutory or programmatic supervision over the activities of the Provider, for example:
* a national supervisory authority for trust services or electronic identification;
* operators of trusted root CA programs (e.g. browser and OS manufacturers) who decide on the inclusion/removal of root CAs in the relevant program;
* administrators and operators of CCADB.  

These entities:
* may request information, documents, and explanations from the Provider regarding the operation of the CA and compliance with requirements;
* may require the adoption of corrective measures, restrictions, or termination of TLS Certificate issuance;
* are not a contracting party or relying party but may affect the trustworthiness of issued TLS Certificates (e.g. by removing the root CA from the program).  

The Provider shall cooperate with these entities to the extent required by applicable law, applicable program rules, and this CP/CPS.  

## 1.4 Certificate Usage

### 1.4.1 Appropriate Certificate Uses

This CP/CPS is strictly scoped to the **"Server Authentication"** Trust Purpose. 

Certificates issued under this CP/CPS are issued for the purpose of identifying the public key holder from a cryptographic key pair (public and private) used within the PKI infrastructure. 

The cryptographic key pairs and TLS Certificates issued under this hierarchy are restricted to web server authentication within public networks (including the public Internet) and shall include the mandatory Extended Key Usage (EKU) `id-kp-serverAuth` (`1.3.6.1.5.5.7.3.1`). Certificates issued under this CP/CPS shall not be used for any other trust purposes (e.g., S/MIME, Code Signing) or for enterprise-only / locally-trusted internal use cases.

The Provider issues the following types of TLS Certificates to Subscribers:

* **Publicly-Trusted TLS Server Certificate (Organization Validated - OV):** Cryptographic keys associated with this type of TLS Certificate are designed for the authentication of internet-accessible servers. These certificates are publicly trusted by virtue of their corresponding Root Certificate being distributed in widely-available application software.

  Issued TLS Certificates include the following Certificate Policy Identifiers asserted in the `certificatePolicies` extension:
  * **CA/Browser Forum Baseline Requirements (OV Policy):** `2.23.140.1.2.2` *(joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) baseline-requirements(2) organization-validated(2))*
  * **Provider's Internal Policy OID:** `1.3.158.35975946.0.0.0.1.1` *(governing Organization Validated TLS Certificate issuance)*

  *Note: The Provider's internal Policy OID and the CA/Browser Forum OV Policy OID incorporated in the certificate correspond to and fulfill the requirements of the ETSI OVCP policy (ETSI EN 319 411-1 policy identifier `0.4.0.2042.1.7`).*

* **Infrastructure & Support Certificates:** The Provider issues management certificates necessary for its operational needs, limited exclusively to Subordinate CA Certificates (Issuing CAs) and TLS/OCSP Responder Certificates operating strictly within this Server Authentication hierarchy.

### 1.4.2 Prohibited Certificate Uses 
TLS Certificates issued under this CP/CPS are not EU qualified TLS Certificates for website authentication according to the eIDAS Regulation [8] and cannot be used where EU qualified TLS Certificates for website authentication are required.  
Certificates issued under this CP/CPS may not be used for:  
* signing a code, documents, or emails;
* issuing other TLS Certificates (non-CA TLS Certificates);
* any use that is not in accordance with the Key Usage and EKU extensions;
* any use that is unlawful, in violation of applicable law, or in violation of this CP/CPS or the trust service agreement.  

Relying Parties should not rely on TLS Certificates for purposes other than TLS server authentication unless such use is expressly permitted by the applicable TLS Certificate policy and clearly indicated in the TLS Certificate extensions.

## 1.5 Policy administration

### 1.5.1 Organization Administering the Document
Next table contains the data of the Provider who is responsible for the preparation, creation, and maintenance of this document.  

|  | |
| :--- | :--- |
| Company:| **Disig, a. s.** |
| Address: | **Galvaniho 17/C, 821 08 Bratislava**|
| Company ID:|  **359 75 946** |
| Phone:| **+421 2 20850140**   |
| e-mail:| **disig@disig.sk**    |
| Web site:| **[https://www.disig.sk](https://www.disig.sk)**    |


### 1.5.2 Contact Person  
For creating policies, the Provider has a PMA that is fully responsible for its content and is ready to answer any questions regarding the Provider's policies (see 1.3.5).  

Next table contains the contact details of the person responsible for the operation of the Certification Authorities of the Provider.

|  | |
| :--- | :--- |
| Certificate Authority CA Disig:|  |
| Address: | **Galvaniho 17/C, 821 08 Bratislava**|
| Company ID:|  **359 75 946** |
| Phone:| **+421 2 20850150, +421 2 20820157**   |
| e-mail:| **caoperator@disig.sk**    |
| Web site:| **[https://eidas.disig.sk](https://eidas.disig.sk)**    |
| Incident reporting:| **[tspnotify@disig.sk](tspnotify@disig.sk)** <br> see more at **[https://eidas.disig.sk/pdf/incident_reporting.pdf](https://eidas.disig.sk/pdf/incident_reporting.pdf)**|


### 1.5.3 Person Determining CP/CPS Suitability    
The person responsible for deciding on the compliance of the Provider's procedures as set out in this CP/CPS is the PMA (see 1.3.5).  

### 1.5.4 CP/CPS approval procedures  
Even prior to the start of operation, the Provider should have approved of its CP/CPS and shall meet all of its requirements. A person named by PMA approves the content of CP/CPS.  
Upon approval by the PMA, the relevant document is published in accordance with the publication and notification policy.  
The PMA has to inform its decisions in such a way that this information is well accessible to the Relying Parties.  
This CP/CPS is approved by the person appointed to the role of PMA.  
The CP/CPS is published in accordance with the publication and notification policy on the Provider's website (see Section 1).  

## 1.6 Definitions and Acronyms

### 1.6.1 Definitions
**TLS Certificate for website authentication** means an attestation that makes it possible to authenticate a website and links the website to the natural or legal person to whom the TLS Certificate is issued.  

**Trust service** means an electronic service normally provided for remuneration, which consists of  
  **a|** the creation, verification, and validation of electronic signatures, electronic seals or electronic time stamps, electronic registered delivery services and TLS Certificates related to those services,   
  **b|** the creation, verification, and validation of TLS Certificates for website authentication,  
  **c|** the preservation of electronic signatures, seals or TLS Certificates related to those services.  

**Certificate holder** means the entity identified in the TLS Certificate as the holder of the private key belonging to the public key contained in the TLS Certificate.  

**Key pair** means a part of a PKI system that uses an asymmetric cryptography and consists of a public key and a private key.  

**Multi-purpose CA** - A root CA or subordinate CA that is in a hierarchy without restrictions on the type of TLS Certificate issued to the end holder, i.e. in the hierarchy it is possible to issue TLS Certificates as well as S/MIME TLS Certificates, or other types of TLS Certificates, to end users;

**Domain Contact** means the Domain Name Registrant, technical contact, or administrative contact (or the equivalent under a ccTLD) as listed in the WHOIS record of the Base Domain Name or in a DNS SOA record.

**Trust service provider** means a natural or a legal person who provides one or more trust services either as a qualified or as a non-qualified trust service provider.  

**RA staff member** means an employee of the Provider or other legal entity that has a contract with the Provider for the provision of certification services.  

**Relying party** means a natural or legal person that relies upon an electronic identification or a trust service.  

**Publicly Trusted Certificate** means a TLS Certificate that is trusted by virtue of the fact that its corresponding root TLS Certificate is distributed as a trust anchor in widely available application software.  

**Single-purpose CA** - A root CA or subordinate CA that is in a hierarchy that is strictly limited to issuing exactly one type of TLS Certificate to an end user, i.e. in the hierarchy, only TLS Certificates can be issued to end user;  

**Subscriber** means a natural person or legal entity to whom a TLS Certificate is issued and who is legally bound by a subscriber agreement or terms of use.  

**Contractor** means a legal entity with whom Disig has entered into a written agreement to provide trusted services.  

**PKCS#10** means a format of messages sent to a Certification Authority to request certification of a public key.  

**PEM** means file format for storing and sending cryptography keys, TLS Certificates, and other data as is formalized by the IETF in RFC 746.  

**SAN** means an extension to X.509 that allows various values to be associated with a security TLS Certificate using a subjectAltName field.  

**TLS** are cryptographic protocols designed to provide communications security over a computer network.  

### 1.6.2 Acronyms
|  | |
| :--- | :--- |
|CA| Certification Authority |
|CAA | Certification Authority Authorization |
|CMA | Certificate Management Authority|
|CP/CPS|Certificate Policy and Certification Practice Statement (CP/CPS)  |
|CRL |Certificate Revocation List  |
|DNS |Domain Name System  |
|FQDN |Fully Qualified Domain Name   |
|HSM |Hardware Security Module  |
|ICO |Organization identification number  |
|NBU |National Security Authority  |
|OID |Object Identifier |
|PKI |Public Key Infrastructure |
|PMA |Policy Management Authority |
|RA |Registration Authority |
|TLS |Transport Layer Security |
|SSL |Secure Sockets Layer |

### 1.6.3 References  
 **[1]** Recommendation ITU-T X.509; Information technology - Open Systems Interconnection - The Directory: Public-key and attribute TLS Certificate frameworks.   
 **[2]** RFC5280, Request for Comments: 5280, Internet X.509 Public Key Infrastructure: Certificate and Certificate Revocation List (CRL) Profile.   
 **[3]** Baseline Requirements for the Issuance and Management of Publicly-Trusted TLS Server Certificates [https://cabforum.org/baseline-requirements-documents/](https://cabforum.org/baseline-requirements-documents/).  
 **[4]** Program Requirements - Microsoft Trusted Root Program: [https://learn.microsoft.com/en-us/security/trusted-root/program-requirements](https://learn.microsoft.com/en-us/security/trusted-root/program-requirements).  
 **[5]** Mozilla Root Store Policy: [https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/policy/](https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/policy/)  
 **[6]** Apple Root Certificate Program, [https://www.apple.com/certificateauthority/ca_program.html](https://www.apple.com/certificateauthority/ca_program.html).  
 **[7]** Chrome Root Program Policy [https://www.chromium.org/Home/chromium-security/root-ca-policy/](https://www.chromium.org/Home/chromium-security/root-ca-policy/).  
 **[8]** Regulation (EU) No 910/2014 of the European Parliament and of the Council of 23 July 2014 on electronic identification and trust services for electronic transactions in the internal market as amended by Regulation 1183/2024.   
 **[9]** ETSI EN 319 401 Electronic Signatures and Infrastructures (ESI); General Policy Requirements for Trust Service Providers.   
 **[10]** ETSI EN 319 411-1 Electronic Signatures and Infrastructures (ESI); Policy and security requirements for Trust Service Providers issuing Certificates; Part 1: General requirements.   
 **[11]** RFC3647, Request for Comments: 3647, Internet X.509 Public Key Infrastructure: Certificate Policy and Certification Practices Framework, Chokhani, et al, November 2003.   
 **[12]** General terms and conditions of provision and use of a trusted services Disig, a.s.   
 **[13]** RFC 8659 DNS Certification Authority Authorization (CAA) Resource Record.   
 **[14]** RFC8555 Automatic Certificate Management Environment (ACME).   
 **[15]** RFC 7231 Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content.   
 **[16]** RFC 7538 The Hypertext Transfer Protocol Status Code 308 (Permanent Redirect).   
 **[17]** RFC 6454 The Web Origin Concept.   
 **[18]** Information about the Processing of Personal Data, Disig, a.s. [https://eidas.disig.sk/pdf/info_oou_gdpr_en.pdf](https://eidas.disig.sk/pdf/info_oou_gdpr_en.pdf)  
 **[19]** RFC 6960 "X.509 Internet Public Key Infrastructure Online Certificate Status Protocol - OCSP".  
 **[20]** RFC 5019 The Lightweight Online Certificate Status Protocol (OCSP) Profile.   
 **[21]** RFC 8954 Online Certificate Status Protocol (OCSP) Nonce Extension.   
 **[22]** Network and Certificate System Security Requirements [https://cabforum.org/working-groups/netsec/documents/](https://cabforum.org/working-groups/netsec/documents/)  
 **[23]** RFC 6962 Certificate Transparency.  
 **[24]** CCADB Policy [https://www.ccadb.org/policy](https://www.ccadb.org/policy).
 **[25]** RFC 9733 ACME Renewal Information (ARI) Extension  
 
### 1.6.4 Conventions 
The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this CP/CPS shall be interpreted in accordance with RFC 2119.

# 2. Publication and Repository Responsibilities

## 2.1 Repositories
Repository shall be located in such a way that they are accessible to the Subscriber and the Relying Parties and in accordance with the overall safety requirements.
The Provider's Web Site is publicly accessible to the Subscribers, the TLS Certificate Holder, the Relying Parties, and the public at all through the Internet.  

The Provider operates a single publicly accessible repository (see Section 1) that provides up-to-date information relevant to this CP/CPS, including:
* this CP/CPS and previous versions;
* the relevant general terms and conditions for the provision of trusted services;
* CA Certificates and their thumbprints;
* TLS Certificate revocation lists (CRLs);
The publicly available information provided at the Provider's website has a controlled access character.

## 2.2 Publication of information
The Provider shall provide on-line storage that is accessible to the Contractors, Subscribers and Relying Parties that will include at least the following information
* TLS Certificates issued in accordance with this CP/CPS,
* current CRL as well as all CRLs issued since the beginning of the TLS Certificate issuance activity,
* Certificates of Root CAs, Cross-Certified SubCAs and subordinate certification authorities that belong to its public key to which corresponding private keys are used when signing TLS Certificates and CRL
* current version of CP/CPS,
* information on the outcome of a regular audit of the performance of the trusted services provided according to Section 8.  

When a CA fails to comply with any requirement of the current version of "Mozilla Root Store Policy" [5], whether it is a misissuance, a procedural or operational issue, or any other variety of non-compliance - the event is classified as an incident. At a minimum, Provider shall promptly report all incidents to Mozilla in the form of an Incident Report and shall regularly update the Incident Report until a Mozilla representative mark the corresponding bug as resolved in the mozilla.org Bugzilla system. The Provider should cease issuance until the problem has been prevented from reccurring.

If the conditions set out in the current "Mozilla Root Store Policy" are not met, the Provider's certification authority manager appointed to the PMA role is responsible for reporting the incident.

Provider publicly discloses the availability and configuration of its automated lifecycle management interfaces. 
The ACME API directory endpoint URL is officially published and maintained at
* For CA Disig R2I2 Certification Service: [https://onlineissue.disig.sk/r2i2/tls/acme/v2/OV/directory](https://onlineissue.disig.sk/r2i2/tls/acme/v2/OV/directory);
* For CA Disig R3I1 TLS Certification Service: [https://onlineissue.disig.sk/r3i1/tls/acme/v2/OV/directory](https://onlineissue.disig.sk/r3i1/tls/acme/v2/OV/directory).

Any updates, technical specifications, or designated maintenance windows regarding the ACME infrastructure are published via the CA’s repository in accordance with this Section.

The Provider publishes the following information in its public Repository, ensuring availability on a 24x7 basis:

### 2.2.1 Policies and Practice Statements 
The current and previous versions of the CP and CPS or combined CP/CPS are published at:  
[https://eidas.disig.sk/en/provider/policies-and-documents/](https://eidas.disig.sk/en/provider/policies-and-documents/) - EN/SK versions  
[https://eidas.disig.sk/sk/poskytovatel/politiky-a-dokumenty/](https://eidas.disig.sk/sk/poskytovatel/politiky-a-dokumenty/) - SK versions

### 2.2.2 CA Certificates
The public key certificates for the Root CAs, Subordinate CAs (Issuing CAs), and any applicable Cross-Certificates are published at:

[https://eidas.disig.sk/en/certificates/ca/](https://eidas.disig.sk/en/certificates/ca/) - EN version  
[https://eidas.disig.sk/sk/certifikaty/ca/](https://eidas.disig.sk/sk/certifikaty/ca/) - SK version

### 2.2.3 Certificate Revocation Lists (CRLs) 
Provider CRLs are available at the following HTTP URLs to avoid circular dependencies during validation:

|CA        |CRL distribution point  |
|----------|:----------------------|
|CA Disig Root R2|http://cdp1.disig.sk/rootcar2/crl/rootcar2.crl<br>http://cdp2.disig.sk/rootcar2/crl/rootcar2.crl|
|CA Disig R2I2 Certification Service|http://cdp.disig.sk/subcar2i2/crl/subcar2i2.crl|
|CA Disig TLS Root R3|http://cdp.disig.sk/rootcar3/crl/rootcar3.crl|
|CA Disig R3I1 TLS Certification Service|http://cdp.disig.sk/subcar3i1/crl/subcar3i1.crl|


### 2.2.4 Test Web Sites 
To demonstrate the functionality of the issued certificates for Root Store inclusion purposes, the CA maintains the following test sites:
|CA                                 |Site type       |Site address                                       |
|-----------------------------------|:---------------|---------------------------------------------------|
|CA Disig R2I2 Certification Service|Valid TLS Site  |https://testssl-valid-r2i2.disig.sk/index.en.html  |
|                                   |Expired TLS Site|https://testssl-expire-r2i2.disig.sk/index.en.html |
|                                   |Revoked TLS Site|https://testssl-revoked-r2i2.disig.sk/index.en.html|

|CA                                 |Site type       |Site address                                       |
|-----------------------------------|:---------------|---------------------------------------------------|
|CA Disig R3I1 Certification Service|Valid TLS Site  |https://testssl-valid-r3i1.disig.sk/index.en.html  |
|                                   |Expired TLS Site|https://testssl-expire-r3i1.disig.sk/index.en.html |
|                                   |Revoked TLS Site|https://testssl-revoked-r3i1.disig.sk/index.en.html|


## 2.3 Time or frequency of publication
The TLS Certificate shall be published as soon as it is issued. Information on the TLS Certificate issued shall be available on the Provider's website. 

The TLS Certificate is published immediately after its issuance and can be immediately taken over by the Subscriber/Certificate Holder. Information about the TLS Certificate is available in the Provider's repository - see Section 1.  

The Certificate Revocation List (CRL) shall be published as specified in Section 4.9.7. Information about the revoked TLS Certificate shall be available on the Provider's website (see Section 1), which serves as its repository.

All information to be published in the repository shall be published as soon as possible.

The CRL is published as specified in Section 4.9.8. Information about the revoked TLS Certificate can be found in the Provider's repository.

This CP/CPS is reviewed and updated at least once per year in accordance with section 9.12.1.

## 2.4 Access controls on repositories
The Provider shall protect any information stored in a repository that is not available to the public. The Provider shall make every effort to ensure the integrity, confidentiality and availability of data related to the provision of trusted services. It also has to take logical and security measures to prevent unauthorized access to the repository for people, who could change, damage, add, remove them, or delete data stored in the repository in any way.  

The Provider protects any information stored in the repository, which is not intended for public dissemination, through technical and organizational measures. For this purpose, it has developed precise rules included in the Provider's security project and related guidelines.

Publicly available information listed in the Provider's repository has a controlled access nature.

# 3. Identification and Authentication

## 3.1 Naming
The provider only accepts TLS Certificate requests that comply with the PKCS #10 or SPKAC standard and are in PEM format, unless otherwise agreed with the Subscriber in advance.

### 3.1.1 Types of names
No stipulation.

### 3.1.2 Need for names to be meaningful
No stipulation.

### 3.1.3 Anonymity or pseudonym of subscribers 
No stipulation.

### 3.1.4 Rules for interpreting various name forms
The interpretation of the individual names of the TLS Certificates issued by the Provider shall be in accordance with the TLS Certificate profiles described in Section 7 of this CP/CPS.  

The distinguished name used in TLS Certificate issued by the Provider may consist of items that are described in the following Section.
#### 3.1.4.1 Replacement of non-ASCII characters
The Provider allows the Applicant to replace diacritical SK characters that might be found in the TLS certificate subject (organization, location items) with their equivalent in the basic ASCII table as follows:


|Character|ASCII<br>equivalent||Character|ASCII<br> equivalent|  
|:-----------:|:---:|:----------------------:|:--------:|:------:|
|á,ä|a||Á, Ä|A|
|č|c||Č|C|
|ď|d||Ď|D|
|dž|dz||DŽ|DZ|
|é|e||É|E|
|í|i||Í|I|
|ľ,ĺ|l||Ľ, Ĺ|L|
|ň|n||Ň|N|
|ó,ô|o||Ó,Ô|O
|ŕ|r||Ŕ|R|
|š|s||Š|S|
|ť|t||Ť|T|
|ú|u||Ú|U|
|ý|y||Ý|Y|
|ž|z||Ž|Z|


#### 3.1.4.2 Certificate

Table 1 contains a list of fields that may be contained in the relative order in the subject of TLS Certificate type "Organization Validated" issued by Provider  
  
Each TLS Certificate shall contain a "subjectAltName" extension containing at least one entry with the Fully-Qualified Domain Name for which the TLS Certificate is intended.  
  
As a Fully-Qualified Domain Name will be accepted also name containing the asterisk (\*) in the third and higher position in the Fully-Qualified Domain Name (e.g., \*.disig.sk; \*.mail.disig.sk etc.) and this type of TLS Certificate will be referred to as a "wildcard" TLS Certificate.  
  
Fully-Qualified Domain Name cannot be contained in any other field except CommonName (CN) and Extension of SubjectAlternativeName.  
  
Table 1: "Organization Validated" TLS Certificate subject fields and their description  

|Itemname|OID  |Abb.  |Description|Note|
|--------|:---:|:----:|-----------|----|
|countryName|2.5.4.6|C|Two-character abbreviation for country name according to ISO 3166-1 associated with the Subject. SK for Slovak republic|Mandatory field|
|localityName|2.5.4.7|L|Subject's locality information|Mandatory field|
|organizationName|2.5.4.10|O|The Subject's name or DBA.|Mandatory field|
|commonName|2.5.4.3|CN|The fully qualified domain name (FQDN) for which the TLS Certificate is issued, which is listed in the SAN entry of the TLS Certificate|Mandatory field|  

Underscore characters (:"_"(ASCII code 0x5F) shall not be present in dNSName entries. 

### 3.1.5 Uniqueness of names
No stipulation.  

### 3.1.6 Recognition, authentication, and role of trademarks
No stipulation.  

## 3.2 Initial identity validation
This Section includes identification and authentication policies and practices for individual entities.  

### 3.2.1 Method to prove possession of private key
No stipulation.  

### 3.2.2 Authentication of Organization and Domain Identity

#### 3.2.2.1 Authentication of Identity   

Legal person (organization) established in the Slovak Republic is proving its identity by extract from the Companies Register of Slovak republic or other existing register of legal persons. RA will require the original or certified copy of the original, not older than three months. Evidence shall include full company name, identifier (usually company ID - ICO), seat, country, name of person acting as a legal person and the signing procedure of a legal person.  

In the event that a legal person not located in the Slovak Republic, its identity is verified in the same manner as described above. Extract from the current register of legal entities shall be officially translated into Slovak language (except to organizations based in the Czech Republic).  

If the legal entity cannot prove its identity by a statement from the commercial register, this legal entity shall prove its existence in writing with a reference to law or other legal regulations. This applies only to non-commercial entities such as the community, the church, civic associations, foundations, public authorities, etc. In the case of issuing a TLS Certificate, the legal person shall prove the truth of the identification data given in the TLS Certificate application by submitting to view the original document proving this fact.
For a Subscriber/Holder who applies for a TLS Certificate for a legal entity, the RA checks the submitted documents proving the existence of the given legal entity, which is usually an extract from the commercial register or another equivalent extract from another official valid register of legal entities.  

Natural person who, based on the submitted extract from the commercial register, act at the RA on behalf of the given legal entity in the matter of obtaining a TLS Certificate shall prove their identity according to section 3.2.3.
Only an authorized person of the user may act at the RA on behalf of the legal entity, i.e. a person who is its statutory member (or more such persons simultaneously, if required by the submitted extract from the commercial register), or the legal entity may be represented by a natural person or another legal entity.  

If a legal entity is represented at the RA, the representing natural person or legal entity shall always submit for inspection a verified extract from the commercial register of the represented legal entity not older than three months.
If a legal entity is represented at the RA by a natural person, the representing natural person shall prove his/her identity in accordance with section 3.2.3 and shall also prove his/her identity with an officially certified (notary or registry office) power of attorney, the text of which clearly states that the representing natural person has been authorized by the authorizing legal entity to act in the given matter on its behalf.  

If a legal entity is represented at the RA by another legal entity, this representing legal entity, in addition to the relevant power of attorney (see the previous paragraph), shall prove his/her identity in the same way as the represented legal entity, as required above.
An entity (natural or legal entity) representing a legal entity may not under any circumstances allow another entity to represent the legal entity it represents in the matter of the legal entity it represents.  

**Legal Status Verification Requirement:** For all verifications  of legal person conducted under this section (including verifications via OR SR, RPO SR, other official state registers, as well as via supporting documentation or attestations), the Provider's RA shall verify that the status of the legal person is not designated by labels such as "ceased," "inactive," "invalid," "in liquidation," "in bankruptcy," "dissolved," "not current," or the equivalent indicating a non-current, suspended, or terminated status of the verified legal person.

#### 3.2.2.2 DBA/Tradename  
If the content of the TLS Certificate identifying the entity to which the TLS Certificate is issued is a DBA or trade name, the Provider shall verify whether the Subscriber has the right to use the given DBA/trade name by using at least:  
**[1]** Documentation provided by, or communication with, a government agency in the jurisdiction of the Applicant's legal creation, existence, or recognition;  
**[2]** A Reliable Data Source;  
**[3]** Communication with a government agency responsible for the management of such DBAs or tradenames;   
**[4]** An Attestation Letter accompanied by documentary support; or 
**[5]** A utility bill, bank statement, credit card statement, government-issued tax document, or other form of identification that the CA determines to be dependable.  

#### 3.2.2.3 Verification of Country  
If the TLS Certificate contains the countryName field, the Provider shall verify the country associated with the Subscriber/Holder in one of the following ways:   
**a)** Information provided by the domain registrar;  
**b)** One of the methods listed in Section 3.2.2.1.  

#### 3.2.2.4 Validation of Domain Authorization or Control

#### 3.2.2.4 Validation of Domain Authorization or Control

If a domain name (FQDN) is used, the Provider shall confirm that the respective second and higher-level domains belong to, or are authorized for use by, the Subscriber requesting a TLS Certificate.

The Provider shall confirm that at the time of issuance of the TLS Certificate, it has validated all FQDNs in the TLS Certificate. Validation shall be performed within the specified timeframe before the TLS Certificate is issued.

Validation that the Subscriber has control over the domain whose FQDN is in the Subject Common Name (CN) entry or listed under the Subject Alternative Name (SAN) extension shall be performed by the Provider using one of the authorized methods specified in this section.

**Authorization Domain Name (ADN) Determination Procedure:**

For each FQDN or Wildcard Domain Name requested in the Certificate, the Provider shall determine the Authorization Domain Name (ADN) by initializing a variable A to the applied-for domain name and executing the following steps:

1. **Method Selection**: The Provider shall choose a validation method. If A is a Wildcard Domain Name, the Provider must choose a validation method permitted for Wildcard Domain Names (as specified in the table below).
2. **Processing FQDNs**: If A is an FQDN:
   - **a) CNAME Lookup**: If the chosen validation method permits CNAME lookups, the Provider may replace A with the result of a DNS CNAME lookup of A. This step may be repeated.
   - **b) Pruning**: If the chosen validation method permits pruning and A is not equal to the Base Domain Name of A, the Provider may replace A with the result of pruning the leftmost Domain Label from A. This step may be repeated.
3. **Processing Wildcard Domain Names**: If A is a Wildcard Domain Name:
   - **a)** Remove `*.` from the leftmost portion of A.
   - **b)** If the chosen validation method permits pruning and A is not equal to the Base Domain Name of A, the Provider may replace A with the result of pruning the leftmost Domain Label from A. This step may be repeated.
4. **Final ADN**: The resulting value A shall be used as the Authorization Domain Name (ADN) for domain control verification.

**Validation Methods Applicability Matrix:**

The Provider exclusively uses the following validation methods under Section 3.2.2.4, subject to the constraints below:

| Section | Validation Method Name | Wildcard Allowed? | CNAME Lookup Allowed? | Pruning Allowed? |
| :--- | :--- | :---: | :---: | :---: |
| **3.2.2.4.7** | DNS Change | YES | YES | YES |
| **3.2.2.4.13** | Email to DNS CAA Contact | YES | YES | YES |
| **3.2.2.4.14** | Email to DNS TXT Contact | YES | YES | YES |
| **3.2.2.4.19** | Agreed-Upon Change to Website - ACME | NO | NO | NO |

The Provider does not issue TLS Certificates for `.onion` Special-Use Domain Names.

**DNSSEC Validation Requirements:**

DNSSEC validation back to the IANA DNSSEC root trust anchor must be performed on all DNS queries associated with the validation of domain authorization or control by the Primary Network Perspective, including CNAME lookups performed while choosing the Authorization Domain Name (ADN).

The DNS resolver used for all DNS queries associated with the validation of domain authorization or control by the Primary Network Perspective must:
1. Perform DNSSEC validation using the algorithm defined in RFC 4035, Section 5;
2. Support NSEC3 as defined in RFC 5155;
3. Support SHA-2 as defined in RFC 4509 and RFC 5702; and
4. Properly handle the security concerns enumerated in RFC 6840, Section 4.

**E-mail Domain Validation Methods (Sections 3.2.2.4.13, 3.2.2.4.14):**
DNSSEC validation back to the IANA DNSSEC root trust anchor must be performed on all DNS CNAME, CAA, and TXT queries attempting to obtain the Authorization Domain Name associated with the validation of domain authorization or control by the Primary Network Perspective, and the Provider must not use local policy to disable DNSSEC validation. For all other DNS queries under these methods, DNSSEC validation back to the IANA DNSSEC root trust anchor should be performed, and the Providershould not use local policy to disable DNSSEC validation.

**All Other Domain Validation Methods (Sections 3.2.2.4.7, 3.2.2.4.19):**
For all other Domain Validation methods, DNSSEC validation back to the IANA DNSSEC root trust anchor must be performed on all DNS queries associated with the validation of domain authorization or control by the Primary Network Perspective, and the Provider must not use local policy to disable DNSSEC validation on any DNS query associated with the validation of domain authorization or control.

**Enforcement:**
Any failed DNSSEC validation during domain validation must result in a failed domain validation, and no TLS Certificate shall be issued until DNSSEC validation is successful.

##### 3.2.2.4.1 Validating the Applicant as Domain Contact  
This method has been retired and shall not be used. 

##### 3.2.2.4.2 Email, Fax, SMS, or Postal Mail to Domain Contact  
This method has been retired and shall not be used.  

##### 3.2.2.4.3 Phone Contact with Domain Contact  
This method has been retired and shall not be used.  

##### 3.2.2.4.4 Constructed Email to Domain Contact   
The Provider does not use this method.  

##### 3.2.2.4.5 Domain Authorization Document  
This method has been retired and shall not be used.  

##### 3.2.2.4.6 Agreed-Upon Change to Website  
This method has been retired and shall not be used.  

##### 3.2.2.4.7 DNS Change  
Confirming the Subscriber control over the FQDN by confirming the presence of a Random Value in a DNS TXT either  
**1)** an Authorization Domain Name; or  
**2)** an Authorization Domain Name that is prefixed with a Domain Label that begins with an underscore character.  

If a Random Value is used, the Provider shall provide a Random Value unique to the Certificate request and shall not use the Random Value after  
**i)**	30 days or  
**ii)**	if the Applicant submitted the Certificate request, the time frame permitted for reuse of validated information relevant to the Certificate (such as in Section 4.2.1 of TLS BR [3])  

Once the FQDN has been validated using this method, the CA may also issue Certificates for other FQDNs that end with all the Domain Labels of the validated FQDN. This method is suitable for validating Wildcard Domain Names.

This method is available to the RA as an automated method of verifying ownership and control over a domain, where the system used to generate TLS Certificates sends a unique randomly generated value for each FQDN that is expected to be in the SAN of the issued TLS Certificate, with the proviso that this unique value shall be registered in the DNS TXT record for each FQDN and shall also be registered for all lower levels, up to the second level, of the given FQDNs.

Subsequently, the CA system automatically checks for the presence of the TXT value in the DNS records. Verification of the randomly generated unique value for the given FQDN will be used for verification within a maximum of 30 days from its submission. Verification data obtained using this method can be used to verify ownership and control over the same FQDN if it is not older than 398 days.  

##### 3.2.2.4.8 IP Address  
The Provider does not use this method.  

##### 3.2.2.4.9 Test Certificate  
This method has been retired and shall not be used.  

##### 3.2.2.4.10 TLS Using Random Value  
This method has been retired and shall not be used.  

##### 3.2.2.4.11 Any Other Method  
This method has been retired and shall not be used.  

##### 3.2.2.4.12 Validating Applicant as a Domain Contact  
The Provider does not use this method.  

##### 3.2.2.4.13 Email to DNS CAA Contact  

Confirming the Applicant's control over the FQDN is performed by sending a Random Value via email to a DNS CAA Email Contact and receiving a confirming response utilizing the Random Value.

1. **DNS CAA Contact Determination**: The relevant CAA Resource Record Set must be found using the search algorithm defined in RFC 8659 (or RFC 6844). The `contactemail` property must take an email address as its parameter, and the entire parameter value MUST be a valid email address as defined in RFC 6532, Section 3.2, with no additional padding or structure.
2. **Random Value Generation & Unique Use**: The Random Value MUST be unique in each email and MUST remain valid for use in a confirming response for no more than 30 days from its creation.
3. **Email Resending**: The email MAY be re-sent in its entirety, including the re-use of the Random Value, provided that its entire contents and recipient(s) SHALL remain unchanged.
4. **Multi-Perspective Issuance Corroboration (MPIC)**: The Provider MUST perform Multi-Perspective Issuance Corroboration as specified in Section 3.2.2.9. To count as corroborating, each Network Perspective MUST observe the same selected DNS CAA Email Contact address used for domain validation as the Primary Network Perspective.

##### 3.2.2.4.14 Email to DNS TXT Contact

Confirming the Applicant's control over the FQDN is performed by sending a Random Value via email to a DNS TXT Email Contact and receiving a confirming response utilizing the Random Value.

1. **DNS TXT Contact Determination**: The Provider MUST query DNS for TXT records on the `_validation-contactemail` subdomain of the Authorization Domain Name (ADN) selected. The RDATA value of the TXT record MUST be a valid email address as defined in RFC 6532, Section 3.2, with no additional padding or structure.
2. **Random Value Generation & Unique Use**: The Random Value MUST be unique in each email and MUST remain valid for use in a confirming response for no more than 30 days from its creation.
3. **Email Resending**: The email MAY be re-sent in its entirety, including the re-use of the Random Value, provided that its entire contents and recipient(s) SHALL remain unchanged.
4. **Multi-Perspective Issuance Corroboration (MPIC)**: The Provider MUST perform Multi-Perspective Issuance Corroboration as specified in Section 3.2.2.9. To count as corroborating, each Network Perspective MUST observe the same selected DNS TXT Email Contact address used for domain validation as the Primary Network Perspective.  

##### 3.2.2.4.15 Phone Contact with Domain Contact  
This method has been retired and shall not be used.  

##### 3.2.2.4.16 Phone Contact with DNS TXT Record Phone Contact    
The Provider does not use this method.  

##### 3.2.2.4.17 Phone Contact with DNS CAA Phone Contact  
The Provider does not use this method.  

##### 3.2.2.4.18 Agreed-Upon Change to Website v2  
The Provider does not use this method.  

##### 3.2.2.4.19 Agreed-Upon Change to Website - ACME

Confirmation of the Applicant's control over the FQDN is performed by verifying domain control of the FQDN using the ACME HTTP Challenge method defined in RFC 8555, Section 8.3, subject to the following requirements:

1. **Challenge Location & Response**: The Provider MUST verify that the request to `http://<FQDN>/.well-known/acme-challenge/<TOKEN>` returns the expected key authorization value, accompanied by a successful HTTP response (HTTP status code 2xx).
2. **Token Validity**: The token (as defined in RFC 8555, Section 8.3) MUST NOT be used for more than 30 days from its creation.
3. **Redirect Handling**: If the Provider follows redirects while requesting the challenge response:
   - **a. HTTP Protocol Layer**: Redirects MUST be initiated at the HTTP protocol layer as the result of a 301, 302, or 307 HTTP status code response (RFC 7231, Section 6.4) or a 308 HTTP status code response (RFC 7538, Section 3). Redirects MUST be to the final value of the `Location` HTTP response header.
   - **b. Scheme Restriction**: Redirects MUST be to resource URLs with either the "http" or "https" scheme.
   - **c. Authorized Ports**: Redirects MUST be to resource URLs accessed via Authorized Ports (Port 80 for http, Port 443 for https).
4. **Multi-Perspective Issuance Corroboration (MPIC)**: The Provider MUST perform Multi-Perspective Issuance Corroboration as specified in Section 3.2.2.9. To count as corroborating, each Network Perspective MUST observe the same challenge information (i.e., token/key authorization) as the Primary Network Perspective.
5. **Wildcard Restriction**: This method MUST NOT be used for validating Wildcard Domain Names.

##### 3.2.2.4.20 TLS Using ALPN  
The Provider does not use this method.  

##### 3.2.2.4.21 DNS Labeled with Account ID - ACME  
The Provider does not use this method.  

##### 3.2.2.4.22 DNS TXT Record with Persistent Value  
The Provider does not use this method.  

#### 3.2.2.5 Authentication for an IP Address  
The Provider does not issue TLS Certificates if the commonName or subjectAlernativeName extension is an IP address.  

#### 3.2.2.6 Wildcard Domain Validation

Before issuing a TLS Certificate with a wildcard character (`*`) in a CN or SAN of type `dNSName`, the Provider MUST establish and follow a documented procedure that determines whether the wildcard character occurs in the first label position to the left of a "registry-controlled" label or a "public suffix" (e.g., `*.com`, `*.co.uk`, see RFC 6454 Section 8.2).

If the wildcard character occurs in the first label position to the left of a registry-controlled label or a public suffix, the Provider MUST NOT issue the TLS Certificate unless the Applicant proves its ownership or control of the entire registry-controlled label or public suffix.

The Provider SHALL verify that:
1. The wildcard character (`*`) appears only as the leftmost label in the FQDN (e.g., `*.example.com`); and
2. The wildcard character is immediately followed by a period (`.`).

Verification of domain authorization or control for the Authorization Domain Name (ADN) associated with the wildcard request MUST be performed in accordance with Section 3.2.2.4 using a validation method explicitly permitted for Wildcard Domain Names.  

#### 3.2.2.7 Data Source Accuracy  

Before using any data source as a trusted source, the Provider shall verify the reliability, accuracy, resistance to change or counterfeiting of such resource. It may consider, for example, the timeliness of the data, the frequency of updating the data source, the data provider, and the public availability, the low probability of the possibility of changing or falsifying the data.  

#### 3.2.2.8 CAA Records  
As part of the issuance process, the Provider shall check the CAA record for each dNSName specified in the subjectAltName extension of the issued TLS Certificate in accordance with the procedure in RFC 8659 and the processing instructions provided in RFC 8659[13] for all records found.  

Some methods relied upon validating the Applicant's ownership or control of the subject domain(s) (see Section 3.2.2.4) to be listed in a TLS Certificate require CAA records to be retrieved and processed from additional remote Network Perspectives before Certificate issuance (see Section 3.2.2.9). To corroborate the Primary Network Perspective, a remote Network Perspective's CAA check response shall be interpreted as permission to issue, regardless of whether the responses from both Perspectives byte-for-byte are identical. Additionally, a CA may consider the response from a remote Network Perspective as corroborating if one or both of the Perspectives experience an acceptable CAA record lookup failure, as defined in the Section 3.2.2.8 TLS BR. [3]  

If the Provider issues, they shall do so within the TTL of the CAA record, or 8 hours, whichever is greater.
The RA staff member must check the published CAA record before issuing a TLS Certificate. If he finds that such a record exists, he must not issue the TLS Certificate until it is confirmed that the TLS Certificate application is in accordance with the relevant set of records in the CAA.
The verification of the record is performed for each FQDN specified in the CN of the application or that which is to be specified in the SAN in such a way that the name tree is progressed from left to right, e.g. for checking the CAA record of an application that contains an FQDN in the form X.Y.X, the check is performed in the order X.Y.X -> Y.Z -> Z, unless Z is a national level, e.g. ".sk".  

A written record of the CAA record check is created, containing all checked FQDNs and the result of the check. 

The Provider verifies DNS CAA records for the requested domain names prior to issuing any TLS certificate. The processing of CAA records is enforced based on the issuance method as follows:  

1.  Manual Issuance Workflow
For certificates issued through the manual workflow, the CA checks the CAA records to ensure that the Provider's CA designated domain name is explicitly authorized for issuance (e.g., issue "disig.sk"). If no CAA record is present, issuance is permitted. If a CAA record is present but does not authorize the CA, the request is rejected or flagged for manual compliance review.

2.  Automated Issuance Workflow (ACME)
For certificates issued through the automated ACME API, the CA strictly enforces standard CAA checks in conjunction with the extended cryptographic parameters defined in RFC 8657 to mitigate the risk of unauthorized multi-tenant issuance:  
__Account URI__ (accounturi): If the CAA record contains the accounturi parameter, the automated issuance workflow will only proceed if the specified URI strictly matches the EAB-linked ACME account ID of the verified organization. If a mismatch is detected, the certificate application is automatically rejected.  
__ACME Method Binding__ (validationmethods): If the CAA record restricts issuance via the validationmethods parameter, domain validation shall exclusively be permitted through the explicitly authorized ACME challenge methods (e.g., dns-01 only). Any validation attempts using methods not listed in the parameter will fail automatically.

#### 3.2.2.9 Multi-Perspective Issuance Corroboration

Multi-Perspective Issuance Corroboration attempts to corroborate the determinations (i.e., domain validation pass/fail, CAA permission/prohibition) made by the Primary Network Perspective from multiple remote Network Perspectives before TLS Certificate issuance. This process improves protection against equally-specific prefix Border Gateway Protocol (BGP) attacks or hijacks.

The Provider MAY use either the same set, or different sets of Network Perspectives when performing Multi-Perspective Issuance Corroboration for the required:
* Domain Authorization or Control; and
* CAA Record checks.

The set of responses from the Network Perspectives relied upon SHALL provide the Provider with the necessary information to allow it to affirmatively assess:
**a)** the presence of the expected Random Value, Request Token, IP Address, or Contact Address, as required by the relied upon validation method specified in Section 3.2.2.4; and
**b)** the Provider's authority to issue to the requested domain(s), as specified in Section 3.2.2.8.

Results or information obtained from one Network Perspective MUST NOT be reused or cached when performing validation through subsequent Network Perspectives. The network infrastructure providing Internet connectivity to a Network Perspective MAY be administered by the same organization providing the computational services required to operate the Network Perspective. All communications between a remote Network Perspective and the Provider MUST take place over an authenticated and encrypted channel relying on modern protocols (e.g., over HTTPS).

A Network Perspective MAY use a recursive DNS resolver that is not co-located with the Network Perspective. However, the DNS resolver used by the Network Perspective MUST fall within the same Regional Internet Registry (RIR) service region as the Network Perspective relying upon it. Furthermore, for any pair of DNS resolvers used on a Multi-Perspective Issuance Corroboration attempt, the straight-line distance between the two States, Provinces, or Countries the DNS resolvers reside in MUST be at least 500 km.

The Provider MAY immediately retry Multi-Perspective Issuance Corroboration using the same validation method or an alternative method. When retrying Multi-Perspective Issuance Corroboration, the Provider MUST NOT rely on corroborations from previous attempts. There is no stipulation regarding the maximum number of validation attempts that may be performed in any period of time.

Network Perspectives are considered distinct when the straight-line distance between the two States, Provinces, or Countries they reside in is at least 500 km. Network Perspectives are considered "remote" when they are distinct from the Primary Network Perspective and the other Network Perspectives represented in a quorum.

The Provider MAY reuse corroborating evidence for CAA record quorum compliance for a maximum of 398 days. After issuing a Certificate to a domain, remote Network Perspectives MAY omit retrieving and processing CAA records for the same domain or its subdomains in subsequent Certificate requests from the same Applicant for up to a maximum of 398 days.

**Table 2: Quorum Requirements**
| # of Distinct Remote Network Perspectives Used | # of Allowed Non-Corroborations |
| :---: | :---: |
| 2–5 | 1 |
| 6+ | 2 |

**Current Requirement and Phased Implementation:**

The Provider MUST implement Multi-Perspective Issuance Corroboration using at least four (4) remote Network Perspectives. The Provider MUST NOT proceed with TLS Certificate issuance if:
1. The number of non-corroborations is greater than allowed in Table 2; or
2. The remote Network Perspectives that do corroborate the determinations made by the Primary Network Perspective do not fall within the service regions of at least two (2) distinct Regional Internet Registries (RIRs).

*Effective December 15, 2026:* The Provider MUST implement Multi-Perspective Issuance Corroboration using at least five (5) remote Network Perspectives. The Provider MUST NOT proceed with TLS Certificate issuance if the number of non-corroborations is greater than allowed in Table 2 and if the remote Network Perspectives that do corroborate the determinations made by the Primary Network Perspective do not fall within the service regions of at least two (2) distinct Regional Internet Registries (RIRs).

### 3.2.3 Authentication of individual identity 
The Provider shall guarantee, in the event that the TLS Certificate is issued for a device or system that can use the TLS Certificate, that the identity of the device or of the system with its public key is linked accordingly.  

For this reason, the device shall be a system assigned to a natural person or a natural person acting on behalf of a legal entity (Subscriber) that manages them.
This natural person shall provide the CMA with the following information:  
* Device or system identification;  
* Device or system public keys (included in the TLS Certificate request);  
* Device or system authorization (if any should be included in the TLS Certificate);  
* Contact details to enable the Provider to communicate with that natural person, if necessary.  

The Provider shall verify the accuracy of any information (the values of the distinguishing name fields) to be listed in the TLS Certificate.
Methods for performing data verification include:  
* Verifying the identity of a natural person in accordance with the requirements of this section;  
* Verifying the identity of the person to whom the component belongs, in accordance with the requirements of Section 3.2.2; 
* Verifying the eligibility of the data to be listed in each TLS Certificate field, with emphasis on the contents of the commonName field;
Note The typical value of this field shall be the Full Qualified Domain Name (FQDN).  
The Provider shall specify the procedures for authenticating the identity of the Certificate Holder. Provider shall record this process for each TLS Certificate in written or electronic form. Documentation on authentication shall contain at least:
* the identity of the person performing the authentication;  
* unambiguous identification data from documents proving the identity of the TLS Certificate Holder;  
* date of identification.  

Identity verification shall be conducted by the RA staff member based on a document containing the following data of the Holder:  
*  full name and surname;  
*  address of permanent residence;  
*  social security number (persons who have it assigned);  
*  date of birth (persons who have not been assigned a birth number).  

At the same time, the Subscriber/Holder shall provide another document that contains at least the name and surname of the Holder and other personal data (date of birth, social security number). This does not apply if it is a service card.
The Provider shall also record the following data from the documents:  
*  identity card number;
*  identity card issuer;  
*  the date of validity of the identity card, if marked.  

The Provider shall accept the following documents when verifying the Holder's identity:  
* ID card;  
* passport;  
* driver's license; 
* birth TLS Certificate;  
* service card;  
* public health insurance policyholder's card; 
* weapon license.  

In the case of providing a birth TLS Certificate, firearms license, service license, or public health insurance policyholder's card, one of the following documents shall also be provided: identity card, passport.
If a natural person represents another natural person, he shall also present an officially verified power of attorney, from the text of which it is clearly clear that the representing natural person was authorized by the authorizing natural person to act in the given matter on his behalf.
Part of the Holder's authentication is the mandatory provision of the selected e-mail address, which will be stored together with his personal data in the Provider's IS, and which will serve expressly for communication between the Provider and the Certificate Holder and will not be part of the issued TLS Certificate. The Provider will not verify whether the specified e-mail address really belongs to the Holder.  

All documents provided to RA by Subscribers shall be either original or officially certified copies of originals. No information may be added, changed, crossed out, etc. to them. Documents on which their validity period is marked shall be valid.
If the RA staff member has doubts about the identity of the potential Subscriber (e.g., an obvious discrepancy between the photo in the personal document and the appearance of the Subscriber, contradiction between the two submitted documents, etc.), he can refuse his registration.
Any documents in a foreign language (except Czech) shall be translated into Slovak by an official translator - an expert.  

At the request of the Subscriber or the RA, any disputed cases in the proof of identity shall be resolved by the procedure according to Section 9.13.
When providing documents, it is required that the originals of these documents for inspection and copies of the originals (do not have to be verified), except for personal documents identifying the Subscriber's identity, used for archiving for the Provider's needs, shall be provided to the RA.   

Provision of an extract from the commercial register obtained from the Internet by the Subscriber is not sufficient, as this extract is only informative and cannot be used for legal actions.
The RA staff member shall check the following on the documents:    
* Personal documents of a natural person:  
   **a)** compliance of the data specified in the application with the data specified in the personal documents;  
   **b)** validity of the submitted document;  
   **c)** coming of age of a natural person (i.e., age 18);  
   **d)** correspondence between the photo in the personal document and the appearance of the owner of the personal document;  
   **e)** conformity in the submitted documents t. j. whether the data on one document does not contradict the data on another document.  

* Extracts from the commercial register or of another register of legal entities:  
   **a)** validity of the statement - shall not be older than 3 months;  
   **b)** proceeding on behalf of a legal entity - i.e., whether the natural person(s) who submitted the given statement has the right to act (sign) on behalf of the given legal entity;  
   **c)** statement form - original or officially (notary/registered) certified copy of the statement.  

*  Consent to issue a TLS Certificate:  
   **a)** authorization to act on behalf of the company - the person signing the consent shall be authorized to represent the Subscriber. Eligibility is checked according to the extract from the trade register or other register specified by law (or the establishment document, power of attorney, appointment decree). If the signing person is not entered into this statement, he shall provide another document on the basis of which he can act on behalf of the Subscriber (usually the power of attorney certified by a notary);  
   **b)** Validity - if the validity period of the consent is stated in the consent, this information is also checked.  

*  Powers of Attorney:  
   **a)** verification of power of attorney (by a notary/registry); 
   **b)** matching of the data specified in the power of attorney, which defines the representative physical or legal entity, with the data indicated on the personal documents of the representing natural person or with the data indicated on the statement from the business or another register of the representing legal entity;  
   **c)** extent of power of attorney - i.e., j. whether the power of attorney authorizes the authorized natural or legal person to perform the required action on the RA on behalf of the authorizing natural or legal person;  
   **d)** time limit or another condition stated in the power of attorney. 

The Provider can also accept documents submitted by the Subscriber in electronic form, signed with a valid qualified electronic signature or a qualified electronic seal (extract from the commercial register, power of attorney, declaration, authorization, etc.).
A natural person may be an adult citizen of the Slovak Republic or a foreign national.  
A natural person must prove his or her identity with two of the following personal documents:
* temporary residence permit (or permanent residence) in the case of a foreigner;  
* firearms license;  
* service card. 

It is required that at least one of the documents be submitted is a document that includes a photograph of the person in question. In the case of submitting a birth TLS Certificate, firearms license, or service card, one of the following documents must also be submitted: identity card or passport.
If a natural person represents another natural person at the RA, he or she must also prove his or her identity with an officially verified (notary or registry office) power of attorney, the text of which clearly states that the representing natural person has been authorized by the authorizing natural person to act in the given matter on his or her behalf.  

If a legal entity represents a natural person, in addition to the power of attorney (see previous paragraph), the authorized legal entity must prove its identity in accordance with section 3.2.2.  

An entity (natural or legal entity) representing a natural person may not, under any circumstances, be represented by another entity in matters concerning the natural person it represents.  

### 3.2.4 Non-verified subscriber information  

The email address is not verified. 

### 3.2.5 Validation of authority  

If the Applicant for a TLS Certificate containing Subject Identity Information is an organization, the Provider shall use a reliable method of communication to verify the authenticity of the Applicant Representative's TLS Certificate request.
The Provider may use the resources listed in Section 3.2.2.1 as a reliable method of communication. Provided that the Provider uses a reliable method of communication, the Provider may establish the authenticity of the TLS Certificate request directly with the Applicant representative or with an authoritative source within the Applicant's organization, such as the Applicant's main business offices, corporate offices, human resource offices, information technology offices, or other department that the CA deems appropriate.  

In addition, the Provider shall establish a process that allows an Applicant to specify the individuals who may request TLS Certificates. If an Applicant specifies, in writing, the individuals who may request a TLS Certificate, then the Provider shall not accept any TLS Certificate requests that are outside this specification. The Provider shall provide an Applicant with a list of its authorized TLS Certificate requesters upon the Applicant's verified written request.  

### 3.2.6 Criteria for Interoperation or Certification  
The Provider shall disclose all cross-certified Subordinate CA Certificates that identify the Provider as the subject, provided that the CA arranged for or accepted the establishment of the trust relationship.  

## 3.3 Identification and authentication for re-key requests  

### 3.3.1 Identification and authentication for routine re-key  
No stipulation.  

### 3.3.2 Identification and authentication for re-key after revocation  
After the TLS Certificate is revoked, the applicant for a subsequent TLS Certificate must undergo all the requirements of the initial registration. 

## 3.4 Identification and authentication for revocation request  
No stipulation.  

# 4. Certificate Life-Cycle Operational Requirements   

## 4.1 Certificate Application  

### 4.1.1 Who can submit a Certificate application  
A TLS Certificate may be requested by a natural or legal person operating a device or system, who demonstrates in the TLS Certificate request that they are eligible to request a TLS Certificate with an FQDN and that all FQDNs which are listed in the SAN of TLS Certificate.
The Provider shall maintain an internal database of all revoked TLS Certificates and rejected requests due to suspicion of phishing or other fraudulent activity.  

### 4.1.2 Enrollment process and responsibilities  

#### 4.1.2.1 Preparation
For Manual Enrollment:   
The Contractor/Subscriber shall take the following steps to prepare for a visit to the Provider:    
* Familiarize yourself with the "Všeobecné podmienky poskytovania a používania dôveryhodnej služby vydávania a overovania certifikátov (General Terms and Conditions for Providing and Using a Trusted Certificate Issuance and Verification Service)" [12] and "Informáciou o spracúvaní osobných údajov (Information on Personal Data Processing)" [18], which shall be accessible in a durable communication channel (see [https//eidas.disig.sk/sk/documents/](https//eidas.disig.sk/sk/documents/));  
* To get acquainted with this procedure, possibly with the principles and instructions for obtaining the TLS Certificate;  
* To have ready the values of each TLS Certificate request field so that these values are consistent with this CP/CPS (see paragraph 3.1.4); 
* To have prepared a TLS Certificate request in form of PKCS #10 or SPKAC, which will be sent in advance to the Provider (see paragraph 4.1.4);  
* To have prepared the selected identity documents and other necessary documents, i.e., Extract from business register, Power of Attorney, etc.;
* To arrange a date for the visit.  

For Automated Enrollment (ACME)
Prior to initiating automated certificate issuance, the Subscriber must complete the organization validation process. Upon successful verification, the Provider provisions the Subscriber with External Account Binding (EAB) credentials.  
The Subscriber must configure their ACME client with these credentials to bind their ACME account to the vetted organizational identity. 

The Provider supports automated Account Key Rollover in compliance with the procedures set forth in Section 7.3.5 of RFC 8555. Verified organization subscribers are entitled to associate their existing, EAB-bound ACME account with a new cryptographic key pair at any time by submitting a valid keyChange request. This request must be concurrently signed by both the old (existing) and the new private keys to verify account ownership without disrupting the pre-vetted organization mapping

#### 4.1.2.2 Request generation  
For Manual Enrollment: 
When requesting a TLS Certificate, the Subscriber shall generate a cryptographic key pair (private and public) using their software (typically Microsoft IIS or Apache / OpenSSL, for example) and shall create a new TLS Certificate request and save it on suitable medium. 
The Provider issues TLS Certificates exclusively at the company's headquarters in Bratislava. 

Notes and warnings: Please note that the request for a TLS Certificate or the public key in it, for which a TLS Certificate has already been issued, cannot be used repeatedly to issue another TLSA Certificate for security reasons and will be rejected at the RA! The request for a TLS Certificate shall include the <subject:commonName> (the so-called entity name) item, filled in appropriately. The individual items shall be filled in so that the entered values are in accordance with this document, with an emphasis on its Section 3.1.2, and to clearly identify the entity that will use the given TLS Certificate (typically the fully qualified domain name (FQDN)). If item O (subject:organizationName) is filled in the application, item L (subject:localityName) shall also be filled in. It is also necessary to maintain the order of items in the application as stated in Section 3.1.4.2 Table 1.

For Automated Enrollment (ACME):
The Subscriber's ACME client programmatically generates a cryptographic key pair and a standard Certificate Signing Request (CSR) matching the approved organizational details. The ACME client must secure the private key and format the request in compliance with RFC 8555 technical specifications. 

#### 4.1.2.3 Sending a Certificate request  
For Manual Enrollment:
The request for the issuance of a TLS Certificate is sent by the Applicant/Subscriber to the RA address ([radisig@disig.sk](radisig@disig.sk)) which shall perform all actions related to the TLS Certificate issuance process.

For Automated Enrollment (ACME):
The ACME client securely transmits the signed request to the Provider’s designated directory endpoint 
[https://onlineissue.disig.sk/r2i2/tls/acme/v2/OV/directory](https://onlineissue.disig.sk/r2i2/tls/acme/v2/OV/directory) or
[https://onlineissue.disig.sk/r3i1/tls/acme/v2/OV/directory](https://onlineissue.disig.sk/r3i1/tls/acme/v2/OV/directory).  

The transmission and subsequent challenge-response validation (e.g., via HTTP-01 or DNS-01 validation methods) are executed fully through the ACME protocol without human intervention.  

## 4.2 Certificate application processing  

### 4.2.1 Performing identification and authentication functions  
The Provider issues exclusively Organization Validation (OV) TLS Certificates. Before issuing an OV TLS Certificate, the RA staff or automated system (e.g., ACME protocol) representing the Provider shall:  
* Inform the attender natural person about the General Terms and Conditions [12];  
* Check the completeness and accuracy of the data in the accepted TLS Certificate request.    
* Verify the identity of the Subscriber and insert his/her personal data into the IS of the Provider, obliging him to fill in all required items required by the Provider's system.    
* Verify other documents to verify any identifying information to be entered into the TLS Certificate.  

RA staff member shall verify the identity and authenticity of the Subscriber within the meaning of the Section 3.2.    
The Subscribers shall show to the RA staff member in a satisfactory manner all the data he / she has entered into each item of the TLS Certificate request.  
RA staff member shall insert a TLS Certificate request and other required data into the Provider's information system. 

In the case of automated certificate issuance (e.g., via ACME protocol), automated issuance is strictly permitted only for FQDNs that have been pre-verified, approved, and assigned to a pre-validated legal entity within the Provider's internal system.

**High Risk Certificate Requests**

The Provider maintains, documents, and implements procedures to identify High Risk Certificate Requests and high-risk FQDNs prior to TLS Certificate approval. High risk requests and FQDNs include, but are not limited to, those containing high-profile domain names, names vulnerable to phishing or typosquatting, high-risk domains, or FQDNs flagged as suspicious by internal risk scoring systems.

As part of the pre-validation process and prior to registering and assigning any FQDN to a pre-validated legal entity in the Provider's internal system, a high-risk evaluation of the FQDN is conducted. All identified High Risk Requests / FQDNs shall require additional verification activity (e.g., secondary manual review by an independent verification officer, additional validation checks, or mandatory authorization by Provider security management) before the FQDN is registered in the system and enabled for automated issuance.

**Delegated Third Parties**

The Provider does not use, nor does it intend to use, Delegated Third Parties to perform identification and authentication functions under this section for TLS Certificates. All verification processes are performed exclusively by the Provider.

Provider obtained the data or document from a source specified under Section 3.2 or completed the validation itself within the maximum number of days prior to issuing the TLS Certificate, as defined in the following table:  

|Certificate issued on or after| Maximum data reuse period|
|:----------------------------:|:------------------------:|
|2026‐03‐15                    |398 days                  |

For validation of Domain Names according to Section 3.2.2.4, any data, document, or completed validation used shall be obtained within the maximum number of days prior to issuing the TLS Certificate, as defined in the following table:  

|Certificate issued on or after|Certificate issued before|Maximum data reuse period|
|:----------------------------:|:-----------------------:|:------------------------:|
|2026‐03‐15                    |2027‐03‐15               |200 days                  |      
|2027‐03‐15                    |2029‐03‐15               |100 days                  | 
|2029‐03‐15                    |                         |10 days                   | 

The Provider programmatically processes each incoming ACME TLS certificate request by executing the identification and authentication functions required by this CP/CPS. This includes the automated verification of domain control and the strict enforcement of DNS CAA records, including the accounturi and validation methods parameters, in accordance with the procedures and specifications defined in Section 3.2.2.8.

### 4.2.2 Approval or rejection of Certificate applications  
In the event of any reasonable doubt as to the identity of the Subscriber, also in case of deficiencies in the documents, providing incomplete documents, the RA staff member shall refuse the Subscriber's registration.
The application shall also be rejected if its format or Content does not meet the requirements set out in Section 3.1.4.  

The Provider may not issue Certificates for FQDN that contains the highest domain (gTLD) that is not listed and in the "Root Zone Database" maintained by the Internet Assigned Numbers Authority (IANA) ([https://www.iana.org/domains/root/db](https://www.iana.org/domains/root/db)).
Any request meeting the requirements of this CP/CPS shall be processed without delay if the issue is made in the presence of the Subscriber or at the latest at the time agreed with the Subscriber in the TLS Certificate application process.  

The Provider shall not issue TLS Certificates containing internal names or reserved IP addresses.
The Provider may not issue a TLS Certificate on a request containing a domain name if, when verifying the CAA DNS record pursuant to Section 3.2.2.8, it is determined that such a record exists and does not authorize the Provider as authorized to issue TLS Certificates.
However, if the "issue" and/or "issuewild" record contains an authorization in the form of "disig.sk", the Provider is authorized to issue the relevant TLS Certificate based on the submitted request.  

The results of the CAA record check shall be recorded and stored by the Provider.

#### 4.2.2.1 CAA Record Processing

The Provider MUST check for Certification Authority Authorization (CAA) records for each FQDN in the Certificate Request prior to issuance, in accordance with RFC 8659. The search algorithm defined in RFC 8659 Section 3 MUST be used. CAA checking MUST be performed no more than eight (8) hours prior to Certificate issuance.

##### 4.2.2.1.1 CAA Multi-Perspective Issuance Corroboration
The Provider MUST perform Multi-Perspective Issuance Corroboration for CAA lookups as specified in Section 3.2.2.9 of this CP/CPS. 

To count as corroborating, each Network Perspective MUST observe the same CAA record set (or absence thereof) as the Primary Network Perspective when searching for CAA records for the target FQDN.

##### 4.2.2.1.2 CAA Parameters
The Provider MUST evaluate the `issue` and `issuewild` CAA properties found in the CAA record set:
1. **Property Support**: 
   - The `issue` property authorizes the Provider to issue a Certificate for the specified domain name.
   - The `issuewild` property authorizes the Provider to issue a Wildcard Certificate for the specified domain name.
2. **Authorized Domain Identifiers**: The Provider's authorized domain identifiers that MUST be matched in the CAA record parameter value are: `disig.sk`.
3. **Issuance Restrictions**:
   - If a CAA record set exists and contains an `issue` or `issuewild` property, the Provider MUST NOT issue the Certificate unless the property explicitly authorizes the Provider.
   - If no CAA record set is found (e.g., NOERROR with 0 records or NXDOMAIN), the Provider MAY issue the Certificate.
   - If a CAA record contains an unknown critical flag, the Provider MUST NOT issue the Certificate.

##### 4.2.2.1.3 DNSSEC Validation of CAA Records
1. **Primary Network Perspective**: DNSSEC validation back to the IANA DNSSEC root trust anchor MUST be performed on all DNS queries attempting to check CAA records associated with the validation of domain authorization or control by the Primary Network Perspective.
2. **Local Policy Restriction**: The Provider MUST NOT use local policy to disable DNSSEC validation on any DNS CAA query.
3. **Validation Failure**: Any failed DNSSEC validation encountered during CAA lookup by the Primary Network Perspective MUST result in a failed CAA check, and no Certificate shall be issued until CAA record processing is successfully completed with valid DNSSEC.e issuance.
2. **Exceptions**: The Provider MAY rely on a previously performed CAA check only if the check was executed within the 8-hour timeframe prior to Certificate issuance and no relevant DNS configuration changes have occurred.

### 4.2.3 Time to process Certificate issuance  
No stipulation. 

## 4.3 Certificate issuance  
### 4.3.1 CA Actions During Certificate Issuance

Upon receiving a TLS Certificate request from the Registration Authority (RA), the CA system MUST verify the request to ensure that:
1. It was submitted by an authorized RA staff member or an authenticated automated interface;
2. It complies with standard certificate request formats, specifically PKCS #10 or SPKAC; and
3. The Public Key contained in the request has not been used in a previously issued TLS Certificate by the CA where duplicate key usage is prohibited by policy or standard.

If all validation and operational requirements are successfully met, the CA system shall proceed with Certificate issuance.

Prior to issuing the final TLS Certificate to the Subscriber, the CA system MUST create a Precertificate and submit it to CT log servers in accordance with RFC 6962 to obtain Signed Certificate Timestamps (SCTs), which are subsequently embedded into the final TLS Certificate.

#### 4.3.1.1 Manual Authorization of Certificate Issuance for Root CAs
Certificate issuance by a Root CA MUST require an individual authorized by the Provider (e.g., the CA system operator, system officer, or PKI administrator) to deliberately issue a direct command in order for the Root CA to perform a certificate signing operation.

#### 4.3.1.2 Linting of To-Be-Signed Certificate Content
The Provider MUST implement an automated Linting process (using industry-standard tools such as `zlint`, `ctlint`, `certlint`, or `cablint`) to test the technical conformity of each to-be-signed artifact (`tbsCertificate` and Precertificate) prior to signing, ensuring strict compliance with applicable standards, Certificate Profiles, and TLS Baseline Requirements.

When a Precertificate has undergone Linting, it is not necessary for the corresponding to-be-signed Certificate to also undergo Linting, provided that the Provider employs technical controls to verify that the to-be-signed Certificate corresponds to the Precertificate in the manner described by RFC 6962, Section 3.2.

Methods used by the Provider to produce a certificate containing the to-be-signed Certificate content for Linting purposes MAY include, but are not limited to:
1. Signing the `tbsCertificate` with a "dummy" Private Key whose Public Key component is not certified by a Certificate that chains to a publicly-trusted CA Certificate; or
2. Specifying a static value for the `signature` field of the Certificate ASN.1 `SEQUENCE`.

The Provider MAY implement its own certificate Linting tools, but SHOULD use Linting tools that have been widely adopted by the industry. The Provider is encouraged to contribute to open-source Linting projects.

#### 4.3.1.3 Linting of Issued Certificates
The Provider MAY use a Linting process to test each issued Certificate post-issuance to ensure ongoing compliance with applicable Certificate Profiles and standards.

### 4.3.2 Notification to subscriber by the CA of issuance of TLS Certificate  
The issuing RA staff member informs the Subscriber/Holder about the issuance of the TLS Certificate by sending an email message to the email address specified in the Certificate Holder's personal data.
Email notification is not sent for TLS Certificate issued by ACME service.

## 4.4 Certificate acceptance  

### 4.4.1 Conduct constituting Certificate acceptance  
TLS Certificates will be created and issued in the Provider system automated and on a continuous basis. The holder will be able to take the issued TLS Certificate immediately after its issuing.  
After the TLS Certificate is issued, the RA staff member and the Subscriber shall sign the relevant documentation related to the issuance of the TLS Certificate.  

The TLS Certificate is available for download via the Provider's repository at:
[https://eidas.disig.sk/sk/poskytovatel/certifikacna-autorita/vyhladavanie-certifikatov/](https://eidas.disig.sk/sk/poskytovatel/certifikacna-autorita/vyhladavanie-certifikatov/)
or is provided to him via email or by submitting it on a portable medium.  

TLS Certificate issued by ACME service are made available to Subscriber via the ACME protocol.

### 4.4.2 Publication of the Certificate by the CA  
Each TLS Certificate issued is published in the Provider's repository immediately after issuance unless its non-disclosure has been agreed with the Subscriber/Holder.

### 4.4.3 Notification of Certificate issuance by the CA to other entities  
The preliminary TLS Certificate is automatically sent to the default CT log servers in order to obtain the CT log record, which will then be included in the resulting TLS Certificate. 

## 4.5 Key pair and Certificate usage  
This Section describes responsibilities for using keys and TLS Certificates.

### 4.5.1 Subscriber private key and Certificate usage   
The Subscriber in relation to the private key and TLS Certificate shall:
* Provide the Provider with the exact and complete information required by this CP/CPS when applying for a TLS Certificate;  
* Use a key pair in accordance with the limitations that have been notified by the Provider;  
* Continually protect his/her private keys in accordance with this CP/CPS, and in accordance with the provisions of the General Conditions [12];  
* Use a private key only after obtaining a public key TLS Certificate with which they create unique pairs;  
* Immediately notify the Provider, if the TLS Certificate has not yet been expired, of suspecting that his/her private key was lost, stolen, or compromised;  
* Immediately request the TLS Certificate to be revoked in the event that any information on the entity's TLS Certificate becomes invalid;  
* Comply with any terms, conditions and limitations imposed on your private key and TLS Certificate i.e., to stop use of a private key after an expiration or revocation of a public key TLS Certificate.  

The Subscriber who will fail to comply with his obligations is not entitled to compensation for any damage.

### 4.5.2 Relying party public key and Certificate usage  
The relying party that relies on the TLS Certificate issued under this CP/CPS and in accordance with the General Terms and Conditions [12] shall:  
* Assess whether the use of the TLS Certificate is in accordance with its purpose and is appropriate for a particular purpose;  
* Check that the use of the TLS Certificate is consistent with the restrictions of the TLS Certificate, which are contained in the TLS Certificate itself, the General Terms and Conditions [12], or this CP/CPS;  
* When working with the TLS Certificate, including its validation, use only the intended and appropriate hardware or software;  
* Verify the validity of the TLS Certificate in question by checking that  
* The TLS Certificate was valid at the time the relying party had confidence that the signature / seal had been created.  
* Before the time stated in the previous point, the TLS Certificate was not revoked via checking current CRL and, if applicable, via the OCSP provided by the Provider - reference to the address of the CRL and, optionally, to the OCSP service is mentioned in TLS Certificate.   
* Make any further verifications that may be required in the context of this CP/CPS or standards for a particular type of TLS Certificate or its use and verify the other TLS Certificates in the certification path as described in the previous way e.g., "trust anchor".

## 4.6 Certificate renewal  

### 4.6.1 Circumstance for Certificate renewal  

Certificate renewal refers to the issuance of a new certificate to a Subscriber with a validity period that overlaps or extends the validity period of an existing certificate, utilizing  a new cryptographic key pair. The Provider will not allow the TLS Certificate to be renewed (issued) to a public key to which TLS Certificate has already been issued by the same CA of the Provider.  

The Provider supports both manual and automated renewal processes:

1. Manual Renewal Workflow
For certificates managed outside the ACME ecosystem, renewal notices are electronically transmitted to the authorized Subscriber representatives prior to expiration. The renewal process must be manually initiated and confirmed by an RA .

2. Automated Renewal Workflow (ACME ARI)
For certificates issued and managed via the automated ACME API, the Provider supports and implements the ACME Renewal Information (ARI) extension in accordance with RFC 9773.

Suggested Renewal Window: The Provider’s ACME server dynamically calculates and publishes a specific, automated renewal window for each active TLS certificate. Compliant ACME client software is expected to periodically check this endpoint and automatically initiate the renewal process within the designated timeframe.

Mass Revocation and Agility Scaling: In exceptional circumstances, force majeure, or mandatory mass revocation scenarios (e.g., due to a delayed compliance issue or a validation anomaly), the Provider will programmatically adjust the suggested renewal window via the ARI extension. This mechanism forces all active, compliant client software to immediately and automatically initiate TLS certificate renewal prior to the effective date of the scheduled revocation, preventing service disruption for the verified organization.

### 4.6.2 Who may request renewal  
No stipulation.

### 4.6.3 Processing Certificate renewal requests  
No stipulation.

### 4.6.4 Notification of new Certificate issuance to subscriber  
No stipulation.

### 4.6.5 Conduct constituting acceptance of a renewal  Certificate  
No stipulation.

### 4.6.6 Publication of the renewal Certificate by the CA  
No stipulation.

### 4.6.7 Notification of Certificate issuance by the CA to other entities  
No stipulation.

## 4.7 Certificate re-key  
No stipulation.
### 4.7.1 Circumstance for Certificate re-key  
No stipulation.

### 4.7.2 Who may request certification of a new public key  
No stipulation.

### 4.7.3 Processing Certificate re-keying requests  
No stipulation. 

### 4.7.4 Notification of new Certificate issuance to subscriber  
No stipulation.

### 4.7.5 Conduct constituting acceptance of a re-keyed Certificate  
No stipulation.

### 4.7.6 Publication of the re-keyed  Certificate by the CA  
See Section 4.4.2.

### 4.7.7 Notification of Certificate issuance by the CA to other entities  
No stipulation.

## 4.8 Certificate modification  

### 4.8.1 Circumstance for Certificate modification   
No stipulation.

### 4.8.2 Who may request Certificate modification  
No stipulation.

### 4.8.3 Processing Certificate modification requests   
No stipulation.

### 4.8.4 Notification of new Certificate issuance to subscriber  
No stipulation.

### 4.8.5 Conduct constituting acceptance of modified Certificate  
No stipulation.

### 4.8.6 Publication of the modified Certificate by the CA  
No stipulation.

### 4.8.7 Notification of Certificate issuance by the CA to other entities  
No stipulation.

## 4.9 Certificate revocation and suspension  

### 4.9.1 Circumstances for revocation   
The TLS Certificate shall be revoked when the relationship between the entity and its public key defined in the TLS Certificate is no longer considered valid.
#### 4.9.1.1 Reasons for Revoking a Subscriber/Subject Certificate  
The Provider shall revoke a TLS Certificate within 24 hours if one or more of the following occurs  
* The Subscriber/Subject requests in writing that the Provider revokes the TLS Certificate.  
* The Subscriber/Subject notifies the Provider that the original TLS Certificate request was not authorized and does not retroactively grant authorization.  
* The Provider obtains evidence that the Subscriber's/Subject's Private Key corresponding to the Public Key in the TLS Certificate suffered a Key Compromise; or  
* The Provider obtains evidence that the validation of domain authorization or control for any Fully-Qualified Domain Name in the TLS Certificate should not be relied upon.  

The Provider should revoke a TLS Certificate within 24 hours and shall revoke a TLS Certificate within 5 days if one or more of the following occurs  
* The TLS Certificate no longer complies with the requirements of Sections 6.1.5 and 6.1.6.  
* The Provider obtains evidence that the TLS Certificate was misused.  
* The Provider is made aware that a Subscriber has violated one or more of its material obligations under the Subscriber Agreement or Terms of Use.  
* There is a suspicion that the TLS Certificate was not issued in accordance with this CP/CPS;  
* The Provider is made aware of any circumstance indicating that use of a Fully-Qualified Domain Name in the TLS Certificate is no longer legally permitted (e.g. a court or arbitrator has revoked a Domain Name Registrant's right to use the Domain Name, a relevant licensing or services agreement between the Domain Name Registrant and the Applicant has terminated, or the Domain Name Registrant has failed to renew the Domain Name);  
* The Provider is made aware that a wildcard TLS Certificate has been used to authenticate a fraudulently misleading subordinate Fully-Qualified Domain Name.  
* The Provider's right to issue TLS Certificates under TLS BR [3] expires or is revoked or terminated unless the Provider has made arrangements to continue maintaining the CRL/OCSP Repository.  
* The Provider is made aware of a demonstrated or proven method that exposes the Subscriber's/Subject's Private Key to compromise, methods have been developed that can easily calculate it based on the Public Key (such as a Debian weak key, see [http//wiki.debian.org/SSLkeys](http//wiki.debian.org/SSLkeys)), or if there is clear evidence that the specific method used to generate the Private Key was flawed.  
* The Provider is made aware of a material change in the information contained in the TLS Certificate.  
* The CA determines or is made aware that any of the information appearing in the TLS Certificate is inaccurate.  
* The Provider terminates the business for any reason and does not arrange that another CA will provide information on revoked TLS Certificates on its behalf.  
* Technical parameters or TLS Certificate format could lead to an unacceptable risk from the point of view of software vendors or relying parties (change of cryptographic algorithms for signing, length of cryptographic keys, etc.).  
* Subscriber/Subject died in the case of a natural person or extinct in case of legal person and the Provider will be informed of this fact,  
* Revocation is required by this CP/CPS.  

Whenever the Provider becomes aware of any of the above circumstances, the TLS Certificate shall be revoked and placed on the Certificate Revocation List ("CRL").  
The revoked TLS Certificate shall be present in all new CRLs, at least until the TLS Certificate expires.  
Revoked TLS Certificate cannot be restored in any circumstances.  
When an end entity TLS Certificate is revoked for one of the reasons below, the specified CRLReason shall be included in the reasonCode extension of the CRL entry corresponding to the end entity TLS Certificate. When the CRLReason code is not one of the following, then the reasonCode extension shall not be provided:  
* keyCompromise (RFC 5280 CRLReason #1).  
* privilegeWithdrawn (RFC 5280 CRLReason #9);**  
* cessationOfOperation (RFC 5280 CRLReason #5).  
* affiliationChanged (RFC 5280 CRLReason #3); or  
* superseded (RFC 5280 CRLReason #4).  

#### 4.9.1.2 Reasons for Revoking a Subordinate CA Certificate  
The Provider shall revoke a Subordinate CA Certificate within seven (7) days if one or more of the following occurs  
* receives a written request for revocation of the Subordinate CA,  
* Subordinate CA notifies the issuing CA Provider that the original request was not authorized and will not provide additional authorization,  
* the Provider obtains evidence that the private key corresponding to the public key in the Subordinate CA TLS Certificate has been compromised or no longer meets the requirements in accordance with Section 6.1.5 and 6.1.6,  
* the Provider obtains evidence that the Subordinate CA Certificate has been misused,  
* the Provider is aware that the Subordinate CA Certificate was not issued in accordance with this CP/CPS,  
* the Provider determines that any of the information provided in the Subordinate CA Certificate is inaccurate or misleading,  
* the CA ceases operating and there is no possibility that another CA will provide data on revoked TLS Certificates,  
* revocation is required by this CP/CPS,  
* if the right expires or is revoked or the right to issue TLS Certificates under TLS BR [3] has been terminated and the Provider has not taken measures to continue providing information from the CRL/OCSP repository.  

### 4.9.2 Who can request revocation  
Subscriber (or a natural or legal person authorized by him / her) can request the revocation of the TLS Certificate at any time, even without specifying the reason for the revocation of the TLS Certificate, with the exception of the reasons that shall be published in the CRL, while the Subscriber/Hoder shall indicate them in his request.  
RA shall revoke the TLS Certificate of Subscriber if it becomes aware of any of the circumstances listed in Section 4.9.1.
Certificate revocation may also be requested by:
* Provider - the RA staff member shall document this fact in writing, including the reason for his/her proceedings,
* the court, by means of its judgment or interim measure (a copy of the relevant court decision shall be attached to the TLS Certificate revocation documents).  
Additionally, Subscribers, relying parties, application software suppliers, and other third parties may submit Certificate Problem Reports informing the Provider of reasonable cause to revoke the TLS Certificate.

Revocation of TLS Certificate issued by ACME service can be requested via the certificate revocation interface of the ACME Protocol.

### 4.9.3 Procedure for revocation request  
If the Subscriber's authentication requirements are met, which requests the revocation of the TLS Certificate (see Section 3.2.3 or 3.2.3); the TLS Certificate revocation request can be submitted  
* Personally, at the RA branch, through the "Certificate Revocation Request" form available to the RA. RA staff member may request a password to revoke the TLS Certificate if the person requesting the TLS Certificate revocation is not the Subscriber but the person authorized to do so by Subscriber.  
* By e-mail - by sending an e-mail message (it does not need to be signed). The content of the message shall be a clear wish to revoke the TLS Certificate, expressed in the phrase "I hereby request to revoke my TLS Certificate with the serial number XXXXXX". his message must also include the TLS certificate revocation password specified in the TLS certificate issuance confirmation.   
* Postcards sent to the Provider's address or of the relevant RA together with a password specified in the TLS certificate issuance confirmation.  
* In the case of a request to revoke a TLS Certificate for the reasons listed in Section 4.9.1.1, the TLS Certificate holder shall submit/deliver a "Request for TLS Certificate Revocation", which is available on the Provider's website: [https://dsrv.disig.sk/download/forms/tls_revoke_form.pdf](https://dsrv.disig.sk/download/forms/tls_revoke_form.pdf).  

The TLS Certificate that expired cannot be revoked.  

Reporting and incident reporting procedures for possible compromise of a private key, misuse of a TLS Certificate or other type of fraud, unauthorized release or other matter related to a issued TLS Certificate are listed in 1.5.2.
The person requesting the revocation of a TLS Certificate must either undergo the same authentication process at the RA as is required during the initial registration of the applicant for a TLS Certificate or must prove in a credible manner that he is an authorized person who can request the revocation of the given TLS Certificate.  

If the TLS Certificate Subscriber/Holder is represented at the RA in the matter of revocation of the TLS Certificate, the representing entity must prove himself with a verified power of attorney (notary or registry office), from the text of which the will of the TLS Certificate Subscriber/Holder to revoke his TLS Certificate is clearly evident. The representing entity is obliged to leave a document confirming his power of attorney or a copy thereof at the RA (it does not have to be verified). The RA staff member will take over and keep this document, in the case of an unverified copy, compare it with the original and write on it the text "I confirm compliance with the original" translated to the Slovak language and add the date and his signature.  

The RA staff member will assess the validity of the request for TLS Certificate revocation and if it is clear that the applicant for revocation is not an authorized person, the RA may reject the request for revocation.  

The RA staff member will reject the request if the applicant does not meet the conditions for authenticating his/her identity (see sections 3.2.2 or 3.2.2.3).  

The reporting contacts and the incident reporting procedure in the event of possible compromise of the private key, misuse of the TLS Certificate or other type of fraud, unauthorized issuance or other matter related to the issued TLS Certificate are listed in chapter 1.5.2.  
In the event of a request to revoke a TLS Certificate for any of the reasons listed in section 4.9.1.1 (keyCompromise (RFC 5280 CRLReason #1), privilegeWithdrawn (RFC 5280 CRLReason #9), cessationOfOperation (RFC 5280 CRLReason #5), affiliationChanged (RFC 5280 CRLReason #3), or superseded (RFC 5280 CRLReason #4), the RA must require a written request to be sent, as specified earlier in this section.  

Revocation requests submitted via the ACME Protocol are processed automatically.

### 4.9.4 Revocation request grace period  
No stipulation.

### 4.9.5 Time within which CA shall process the revocation request  
Provider shall  
* Within 24 hours after receiving a Certificate Problem Report, the Provider shall investigate the facts and circumstances related to a Certificate Problem Report and provide a preliminary report on its findings to both the Subscriber and the entity who filed the Certificate Problem Report;  
* After reviewing the facts and circumstances, the Provider shall collaborate with the Subscriber/Holder and any entity reporting the Certificate Problem Report or other revocation-related notice to establish whether or not the TLS Certificate will be revoked, and if so, a date on which the Provider will revoke the TLS Certificate;  
* The period from receipt of the Certificate Problem Report or revocation-related notice to published revocation shall not exceed the time frame set forth in Section 4.9.1.1 or 4.9.1.2;  
* The date selected by the Provider should consider the following criteria   
   * The nature of the alleged problem (scope, context, severity, magnitude, risk of harm);  
   * The consequences of revocation (direct and collateral impacts to Subscribers and Relying Parties);  
   * The number of Certificate Problem Reports received about a particular Certificate or Subscriber;  
   * The entity making the complaint (for example, a complaint from a law enforcement official that a Web site is engaged in illegal activities should carry more weight than a complaint from a consumer alleging that she did not receive the goods she ordered); and  
   * Relevant legislation.  
* Publish the current CRL and all previous CRLs on its website (see Section 1);  
* Publish all revoked TLS Certificates in the CRL. i.e. even those that have expired in the meantime;  
* Archive all CRLs it has released.  

The Provider shall automatically inform the TLS Certificate Subscriber/Holder about revocation of TLS Certificate by sending an email to the email address provided by the Subscriber/Holder during registration to the RA.  

Upon receipt of a TLS Certificate revocation request that the RA staff member considers to be legitimate (i.e., that complies with the relevant provisions of these CP/CPS), the RA staff member shall enter the received TLS Certificate revocation request via the RA Client application into the Provider's information system so that the TLS Certificate in question can be automatically revoked. Revocation shall be conducted no later than 24 hours after verification of the legitimacy of the revocation request.  

CRL shall be published in the repository as quickly as possible after issuing.

Due to the fact that Root Store operators do not grant exemptions from TLS Certificate revocation requirements under this CP/CPS, Provider shall:  
* engage in proactive communication and advise Subscribers well in advance about the revocation timelines and explicitly warn them against using publicly-trusted TLS Certificates on systems that cannot tolerate timely revocation;  
* include appropriate language in Subscriber agreements requiring Subscriber timely cooperation in meeting revocation timelines and acknowledging the Provider's obligations to adhere to applicable policies and standards; and  
* prepare and maintain comprehensive and actionable plans to address mass revocation events, including detailed procedures for handling mass revocations effectively, including rapid communication with affected parties and conducting annual plan testing through tabletop exercises, simulations, parallel testing, or use of test environments, which do not involve the revocation of active TLS Certificates - see. 5.7.1.2.

### 4.9.6 Revocation checking requirement for relying parties  
When relying on the TLS Certificate the relying party is obliged to verify its validity under the General Terms and Conditions [12].  

Between submitting a valid TLS Certificate revocation request and publishing the revoked TLS Certificate to the CRL, the Subscriber / Holder bears all responsibility for any damage caused by the misuse of TLS Certificate. After publishing the TLS Certificate in the CRL, it bears all responsibility for any damage caused using the revoked TLS Certificate, the party that has relied on the revoked TLS Certificate.  

Non-verification of TLS Certificate using the CRL is considered a gross violation of this CP/CPS.	

### 4.9.7 CRL issuance frequency   
The frequency of the CRLs varies depending on whether it concerns root CA, a subordinate CA. The table below contains information about the maximum of CRL issuance.   


|CRL issuer|Issuing frequency  |nextUpdate vs.<br> thisUpdate  | Notes |
|----------|:-----------------:|:-----------------------------:|-------|
|Root CA|max 365 days|< 365 days|Whenever to 24 hours after revoking a subordinate CA|
|Subordinate CA|max 7 days|< 10 days||

Subordinate CAs of the Provider issuing TLS Certificates to end users shall issue CRLs
* At least every 24 hours, even if no TLS Certificate has been revoked for the last 24 hours and the nextUpdate shall have the value of 24 hours.  

Root CA issuing Certificates to subordinate CAs shall issue CRLs
* At least every 7 days with nextUpdate for 14 days.  
* Always within 24 hours of revoking a CA subordinate TLS Certificate.  

CRLs are available via a publicly-accessible HTTP URL. 

### 4.9.8 Maximum latency for CRLs   
No stipulation.  

### 4.9.9 On-line revocation/status checking availability   

The Provider may provide the OCSP service for issued TLS Certificate. In the case of the OCSP service, the addresses of the OSCP responders units shall be included in the Authority Information Access extension of TLS Certificate.  
OCSP responses shall conform to RFC6960 [19] and/or RFC5019 [20]. OCSP responses shall either be signed by:  
   **[1]** the CA that issued the TLS Certificates whose revocation status is being checked; or  
   **[2]** an OCSP Responder whose TLS Certificate is signed by the CA that issued the TLS Certificate whose revocation status is being checked.  

In the latter case, the OCSP signing TLS Certificate shall contain an extension of type id-pkix-ocsp-nocheck, as defined by RFC6960 [19].  
Third parties interested in using OCSP shall send a request to the appropriate OCSP responder unit, which URI is published in the TLS Certificate. The request submitted shall comply with the requirements of RFC 6960 [19].  
OCSP responders operated by the Provider shall support the HTTP GET method, as described in RFC 6960 [19] and/or RFC 5019 [20]. The Provider may process the Nonce extension (1.3.6.1.5.5.7.48.1.2) in accordance with RFC 8954 [21].  
The validity interval of an OCSP response is the difference in time between the thisUpdate and nextUpdate field, inclusive. For purposes of computing differences, a difference of 3,600 seconds shall be equal to one hour, and a difference of 86,400 seconds shall be equal to one day, ignoring leap-seconds.  

For the status of Subscriber TLS Certificates:  
   **[1]** OCSP responses shall have a validity interval greater than or equal to eight hours;  
   **[2]** OCSP responses shall have a validity interval less than or equal to ten days;  
   **[3]** For OCSP responses with validity intervals less than sixteen hours, then the Provider shall update the information provided via an OCSP prior to one-half of the validity period before the nextUpdate;  
   **[4]** For OCSP responses with validity intervals greater than or equal to sixteen hours, then the Provider shall update the information provided via an OCSP at least eight hours prior to the nextUpdate, and no later than four days after the thisUpdate;  
   **[5]** An authoritative OCSP response shall be available (i.e. the responder shall not respond with the 'unknown' status) starting no more than 15 minutes after the Certificate or TLS Precertificate is first published or otherwise made available.  

For the status of Subordinate CA Certificates:
* The Provider shall update information provided via an OCSP:    
   * at least every twelve months; and  
   * within 24 hours after revoking a Subordinate CA Certificate.   

### 4.9.10 On-line revocation/status checking requirements  
No stipulation.  

### 4.9.11 Other forms of revocation advertisements available  
No stipulation.  

### 4.9.12 Special requirements re-key compromise  
See Section 4.9.1.  

### 4.9.13 Circumstances for suspension  
The Provider does not provide such a service.  

### 4.9.14 Who can request suspension  
No stipulation.  

### 4.9.15 Procedure for suspension request  
No stipulation.  

### 4.9.16 Limits on suspension period  
No stipulation.  

## 4.10 Certificate status services  

### 4.10.1 Operational characteristics  

The CRL shall be available on the Provider's website (see Section 1) and shall be accessible through the HTTP protocol on port 80.  
The OCSP shall be available at the URL specified in the issued TLS Certificate and the applicant for TLS Certificate status shall send a request in the sense of the 4.9.10.  

Revocation entries on a CRL or OCSP Response shall not be removed until after the expiry date of the revoked TLS Certificate.  
The current CRL is available on the Provider's website (see Section 1) and is accessible via HTTP protocol on port 80.  
The OCSP service is available at the URL specified in the TLS Certificate issued.  

### 4.10.2 Service availability  
The Provider operates and maintains its CRL and OCSP with resources sufficient to provide a response time of ten seconds or less under normal operating conditions.

The distribution points on which CRLs are published shall be available in 24x7 mode.  
OCSP shall be available in 24x7 mode.  
The Provider shall maintain a continuous 24x7 ability to respond internally to a high-priority TLS Certificate problem report, and where appropriate, forward such a complaint to law enforcement authorities, and/or revoke a Certificate that is the subject of such a complaint.
Reporting TLS Certificate issues is available 24x7 at [support@disig.sk](support@disig.sk).  

### 4.10.3 Optional features  
No stipulation.  

## 4.11 End of subscription  
The Provider's service to the Subscriber/Holder of the TLS Certificate will be terminated upon expiration of the contract under which the TLS Certificate was issued.  
Either party based on the agreement, even before its expiry may terminate the agreement. The cancellation of the contract shall result in the immediate revocation of valid TLS Certificate issued based on the contract.  

## 4.12 Key escrow and recovery  

### 4.12.1 Key escrow and recovery policy and practices  
No stipulation.  

### 4.12.2 Session key encapsulation and recovery policy and practices  
No stipulation.  

# 5. MANAGEMENT, OPERATIONAL, AND PHYSICAL CONTROLS  
The security of the Provider shall be based on a set of security measures in Physical, Object, Personnel and Operational Security. These security measures shall be designed, documented, and applied based on security rules and approved by the Provider's management.
Security measures shall be available to the staff concerned.  
Provider shall
* Take full responsibility for the compliance of its activities with the procedures defined in the security policy, including their fulfilling by his registration authorities;
* Define the responsibility of registration authorities and oblige them to comply with established safety measures;
* Have a list of all their assets with their classification from the point of view of the risk assessment conducted.  

The Security Policy of the Provider and the Summary of Security Assets shall be reviewed at regular intervals and always when significant changes are made to ensure their continuity, suitability, sufficiency, and effectiveness.
The Provider's management shall approve any changes that may affect the level of security provided.  
The setting up of the Provider's systems shall be regularly reviewed for changes that threaten the Provider's security policy.  

## 5.1 Physical security controls  

### 5.1.1 Site location and construction  
Technological facilities in which the Provider's basic infrastructure is located shall be in protected areas accessible only to authorized persons and separated from other areas by appropriate security features (security doors, grilles, fixed walls, etc.). The equipment provided should consist only of equipment reserved for certification authority functions and should not serve any purpose that does not apply to this function.
The Provider's basic infrastructure is located in protected areas that are accessible only to authorized persons and are separated from other areas by appropriate security features (security doors, bars, solid walls, etc.). The Provider's equipment consists only of equipment reserved for the provision of trusted services and does not serve any purposes unrelated to these services. The Provider operates its core CA infrastructure, including key-holding, signing, and certificate-status systems, exclusively within the geographic region and jurisdiction of the Slovak Republic.

### 5.1.2 Physical access  
Access Control Mechanisms for Provider's Protected Areas e. g. the areas of the highest security zone shall be secured in such a way that these spaces are protected by a security alarm and are only accessible to persons holding a security token and listed in the list of authorized persons to enter the Provider's protected areas. Provider equipment shall be permanently protected from unauthorized access, even from unauthorized physical access.  
The access control mechanisms to the Provider's protected areas, i.e. to the areas of the highest security zone, are ensured in such a way that the areas are protected by a security alarm and entry is allowed only to persons who own a security token and are listed on the list of persons authorized to enter the Provider's protected areas (multi-factor authentication).   
The Provider's equipment is constantly protected from unauthorized access, including unauthorized physical access.  

### 5.1.3 Power and air conditioning  
The spaces in which the Provider's equipment is located are adequately supplied with electricity and air-conditioned to provide a reliable operating environment.  

### 5.1.4 Water exposures  
The spaces in which the Provider's equipment is located shall be located so that they cannot be endangered by water from any source. If this is not entirely possible, measures shall be taken to minimize the risk of water hazard on the premises.  
The premises on which the Provider's equipment is located are located in such a way that the risk of water from any sources is unlikely.  

### 5.1.5 Fire prevention and protection  
The spaces in which the Provider's equipment is located shall be reliably protected from direct fire sources, heat that could cause fire in the premises.  

### 5.1.6 Media storage  
Media shall be stored in rooms that are protected against accidental, unintentional damage (water, fire, and electromagnetism). Media containing security audits, archives, or backed up information should be stored on a site separate from CMA.  
Media is stored in a location that is protected from accidental, unintentional damage (water, fire, electromagnetic). Media containing information related to security audits, archives, or backup information is stored in a location separate from CMA equipment.

### 5.1.7 Waste disposal  
With the waste arising from the operation of the Provider it shall be managed in such a way that no environmental pollution is involved.  
Waste generated in connection with the Provider's operations is managed in such a way that it cannot, under any circumstances, pollute the environment.  

### 5.1.8 Off-site backup  
In the event of irreversible damage to the main site spaces where the Provider's infrastructure is located, it is necessary to have at least copies of the Provider's most important assets backed up outside this principal location.  
In the event of irreversible damage to the premises of the main location where the Provider's infrastructure is located, the Provider has a copy of all the most important assets at a backup location that is geographically distant from the main location.  

## 5.2 Procedural controls  
When selecting persons to fill the role of RA staff member, emphasis is placed on their responsibility and trustworthiness, as this role requires trustworthiness. The functions performed by this role are among the functions that form the basis of trust in the Provider at the personnel level.  
Every RA that operates in accordance with these CP/CPS is obliged to comply with their provisions. The RA staff member responsibility is primarily:
* verifying identity either through personal contact or through a representative entity;  
* recording information from TLS Certificate applicants and verifying its accuracy;  
* secure communication with the Provider;  
* communication with the Subscriber/Holder and documenting this communication.  

### 5.2.1 Trusted roles  
Within CAs we shall be defined as trustworthy roles responsible for individual aspects of trusted activities such as, for example, system administrator, security manager, internal auditor, policy maker, etc., which form the basis of trust in the whole PKI.  
At the same time, responsibilities for individual roles shall be defined. Persons selected to hold roles that require credibility shall be accountable and trusted. 

All persons in trusted roles shall have no conflict of interest to ensure the impartiality of the services provided by the Provider.  
Within the Provider's CA, trusted roles are defined that are responsible for individual aspects of the trusted services provided, and the responsibilities of each role are also defined.
Persons selected to hold roles that require trust are responsible and trustworthy.  

All persons in trusted roles are free from conflicts of interest to ensure the impartiality of the services provided by the Provider.  

### 5.2.2 Number of Individual Required per Task  
For each task, the number of individuals assigned to perform each task shall be identified (rule K of N).  

### 5.2.3 Identification and authentication for each role  
Each role has a defined way of identifying and authenticating when accessing the IS of the Provider.  

### 5.2.4 Roles requiring separation of duties  
Each role shall have set criteria that consider the need for separation of functions in terms of the role itself, i.e., there shall be roles that cannot be performed by the same individuals.   

## 5.3 Personnel controls  
Provider staff shall be formally appointed to the trusted role by executive management responsible for security.  
Personnel for the RA staff member role is selected on the basis of reliability, loyalty, and trustworthiness.  

All persons holding the RA staff member role are properly instructed and trained to the extent necessary for the performance of the RA staff member's activities and always have available the current versions of the Provider's documents intended for the performance of the RA staff member's activities, which are available on the website.  

The RA staff member's access to the Provider's IS via the RA Client application, which the RA uses in its activities. RA staff member is protected from unauthorized access by the RA using its own RA Certificate for authentication, through which it identifies and authorizes itself.
An important security measure that significantly limits the possibility of misuse of the RA staff member's electronic identity (the RA Certificate and, in particular, the private key belonging to it) is that the given RA key pair is stored on a smart card. Access to the private key stored on the card is password protected.  

Additional security measures appropriate to the threat level in the RA equipment environment will also be used to protect the RA equipment.  

### 5.3.1 Qualifications, experience, and clearance requirements  
Employees in trusted roles shall meet the qualification requirements, professional experience requirements, and have security clearance at the specified level or shall be in the process of requesting a security clearance, respectively. Requirements for each role are described in separate sheets used to recruit new staff.
Persons in managerial positions shall  
* Have appropriate training or experience in the field of trusted services provided by the Provider;  
* Be familiar with security measures for safety roles;       
* Have experience of information security and risk assessment to the extent necessary for the performance of managerial functions.

Provider is responsible for the identity and trustworthiness of personnel, and performs  background checks, training, and regular monitoring and review.

### 5.3.2 Background check procedures  
An employee can only be included in the trusted role of the Provider if he/she has a security clearance of the specified level i.e., at least to the "Confidential" classification level or is in the process of requesting such a review, respectively.
Security clearance is not required for the RA staff member role.   

### 5.3.3 Training Requirements and Procedures  
Verification duties and issuance functions for TLS Certificates are strictly performed in-house by a small, highly specialized group of the Provider's internal personnel. The Provider does not delegate any validation or verification functions to any third party or external Registration Authority (RA).
Before allowing any internal RA Staff memeber - Validation Specialist to perform verification tasks, the Provider shall provide comprehensive skills-training. The training program shall cover:
*  Basic Public Key Infrastructure (PKI) knowledge and principles;
*	Authentication and vetting policies and procedures (including this CP/CPS);
*	Common threats to the information verification process, including phishing, typosquatting, and other social engineering tactics;
*	The full scope of the TLS Baseline Requirements.

The Provider shall maintain complete records of all training sessions and qualifications. The Provider shall formally document that each RA staff - Validation Specialists possesses the skills required by a task before allowing theRA Staff memeber - Validation Specialists possesses the necessary skills and expertise required for a task before authorizing them to perform that task, ensuring they maintain a high skill level to execute their duties satisfactorily.
 
Prior to being authorized to perform validation duties, all RA Staff memeber - Validation Specialists shall be required to pass a formal examination provided by the Provider testing their knowledge on the information verification requirements outlined in the TLS Baseline Requirements and this CP/CPS.   

### 5.3.4 Retraining frequency and requirements  
For roles where the requirements for passing the prescribed training are set, it is possible to determine the need to repeat them after completing the primary training.  
Renewal training for RA staff member is conducted based on a decision by the PMA in cases where significant changes occur, whether in legislation or in RA software.   

### 5.3.5 Job rotation frequency and sequence   
No stipulation.  

### 5.3.6 Sanctions for unauthorized actions  
Any employee failure whose result is a situation that is not in accordance with the provisions of this CP/CPS, whether it concerns negligence or bad intent, will be the subject of appropriate administrative and disciplinary proceedings by the Provider.  

### 5.3.7 Independent Contractor Controls  
Where independent contractors are assigned to implement trusted roles, they shall be subject to the obligations and specific requirements for these roles within the meaning of Section 5.3 and are equally subject to the sanctions referred to in point 5.3.6.  

### 5.3.8 Documentation supplied to personnel  
Employees in trusted roles shall have the documents needed to perform the function they are assigned to, including a copy of this CP/CPS and all technical and operational documentation necessary to maintain the integrity of operation of the Provider's.  
RA staff member has at their disposal the necessary documents necessary for the performance of the function to which they are assigned, including a copy of this CP/CPS on the [razona.disig.sk](razona.disig.sk) portal.  

## 5.4 Audit logging procedures  
The Provider shall record and have available all-important information regarding the issued TLS Certificates during the necessary time and even after termination of operation.  
The Provider shall record accurate time in the trust service concerning key management and clock synchronization. The time recorded for each event shall be synchronized with UTC at least every 24 hours.  

### 5.4.1 Types of events recorded  
The Provider shall records at least the following events:
* CA Certificate and key lifecycle events, including:  
   * Key generation, backup, storage, recovery, archival, and destruction;  
   * Certificate requests, renewal, and re-key requests, and revocation;  
   * Approval and rejection of CA Certificate requests;  
   * Cryptographic device lifecycle management events;  
   * Generation of Certificate Revocation Lists;  
   * Signing of OCSP Responses (as described in Section 4.9 and Section 4.10); and  
   * Introduction of new Certificate Profiles and retirement of existing Certificate Profiles;
* Subscriber TLS Certificate lifecycle management events, including:  
   * TLS Certificate requests, renewal, and re-key requests, and revocation;  
   * All verification activities stipulated in TLS BR [3] and CP/CPS;  
   * Approval and rejection of TLS Certificate requests;
   * Issuance of TLS Certificates;
   * Generation of Certificate Revocation Lists; and
   * Signing of OCSP Responses in accordance with TLS BR [3] Section 4.9 and 4.10;
* Security events, including:
   * Successful and unsuccessful PKI system access attempts;
   * PKI and security system actions performed;
   * Security profile changes;
   * Installation, update, and removal of software on a Certificate System;
   * System crashes, hardware failures, and other anomalies;
   * Firewall and router activities; and
   * Entries to and exit from the CA facility;
Log records shall include the following elements:
* Date and time of event;
* Identity of the person making the journal record (or system process identifier for automated events); and
* Description of the event;  

For all verification activities, log records shall additionally include at a minimum:

1. The information being validated (e.g., the applied-for FQDN or the organization name);
2. The Appointed Domain Name (ADN) used (if applicable and different from the applied-for FQDN); and
3. The validation method used (e.g., the specific TLS BR section number or the registered label of an ACME validation method).

All events related to operations performed in the RA Client application are recorded directly by the application. Likewise, all information sent from the RA Client application is recorded on the server side of the Service Provider.  

Events related to the life cycle of TLS Certificates for end users in the scope of:
* request for issuance of a TLS Certificate;  
* approval of the issuance request;  
* issuance of a TLS Certificate;  
* revocation of a TLS Certificate;  

are recorded in the SWACA database;  

#### 5.4.1.1 Router and firewall activities logs

Logging of router and firewall activities necessary to meet the requirements of Section 5.4.1, Subsection 3.6 shall at a minimum include:  
**1.**  Successful and unsuccessful login attempts to routers and firewalls; and  
**2.**  Logging of all administrative actions performed on routers and firewalls, including configuration changes, firmware updates, and access control modifications; and  
**3.**  Logging of all changes made to firewall rules, including additions, modifications, and deletions; and  
**4.**  Logging of all system events and errors, including hardware failures, software crashes, and system restarts.  

### 5.4.2 Frequency of processing audit log  
No stipulation.  

### 5.4.3 Retention Period for Audit Logs  
The Provider and each Delegated Third Party shall retain, for at least two (2) years:
* CA Certificate and key lifecycle management event records in the meaning of 5.4.1 after the later occurrence of:  
   * the destruction of the CA Private Key; or  
   * the revocation or expiration of the final CA Certificate in that set of TLS Certificates that have an X.509v3 basicConstraints extension with the cA field set to true and which share a common public key corresponding to the CA private key;  
* Subscriber TLS Certificate lifecycle management event records (see 5.4.1) after the expiration of the Subscriber TLS Certificate;  
* Any security event records (as set forth in Section 5.4.1) after the event occurred.  

### 5.4.4 Protection of Audit Log  
All records are stored and protected to prevent their deterioration.  

### 5.4.5 Audit Log Backup Procedure  
No stipulation.  

### 5.4.6  Audit collection System (internal vs. external)  
The Provider has built its own system for backing up logs.  

### 5.4.7 Notification to event-causing subject  
No stipulation.  

### 5.4.8 Vulnerability assessments  
Additionally, the Provider's security program shall include an annual risk assessment that:  
**1.** Identifies foreseeable internal and external threats that could result in unauthorized access, disclosure, misuse, alteration, or destruction of any TLS Certificate data or TLS Certificate management processes.  
**2.** Assesses the likelihood and potential damage of these threats, taking into consideration the sensitivity of the TLS Certificate data and TLS Certificate management processes; and  
**3.** Assesses the sufficiency of the policies, procedures, information systems, technology, and other arrangements that the Provider has in place to counter such threats.  

## 5.5 Records archival  

### 5.5.1 Types of records archived  
Provider shall keep all records of the TLS Certificates issued as well as the TLS Certificates themselves according to the requirements of the current legislation during the period specified in 5.5.2.  
The records can be kept in paper form or in electronic form. All records that shall be submitted by the Subscriber / Holder for the issuing of required type of TLS Certificate (e.g., business listing, power of attorney etc.) shall also be part of the retained records.  
The Provider shall also keep all audit records (logs), written records of CA events (CA key generation, subordinate CA, TSA Certificate issuance, and OCSP responder Certificates).  

Viewing records with partial authorization can be allowed to specific units of the Provider, full authorization is allowed for PMA and to the persons performing the compliance audit.  

### 5.5.2 Retention period for archive  
The Provider is obliged to keep the contract with the Subscriber/Holder and the confirmation of the issuance of the TLS certificate issued pursuant to this contract for at least 7 years from the expiration of the TLS certificate.    
In addition, the Provider shall keep for at least two (2) years:  
**1.** all archived documentation related to the security of CA systems, TLS Certificate management systems, root CA systems (as specified in Section 5.5.1); and  
**2.** all archived documentation related to TLS Certificate application verification, TLS Certificate issuance and TLS Certificate revocation, and TLS Certificates themselves (as specified in Section 5.5.1), whichever occurs later.  

### 5.5.3 Protection of archive
The archive records of the Provider shall be stored in a safe off-premises location and shall be maintained in a manner that prevents unauthorized modification, replacement, or destruction.  

### 5.5.4 Archive backup procedures  
No stipulation.  

### 5.5.5 Requirements for time-stamping of records  
No stipulation.  

### 5.5.6 Archive collection system (internal or external)  
No stipulation.  

### 5.5.7 Procedures to obtain and verify archive information  
No stipulation.  

## 5.6 Key changeover  
The Provider shall use his signature (private) keys only for the purpose for which they are intended. Private subordinate CA keys can only be used for the purpose for which they are intended i.e., signing end-user TLS Certificates, or signing certificates issued for technological purposes (timestamp, OSCP responder, etc.). Root CA private keys can only be used when signing certificates for subordinate CAs or technology certificates belonging to Root CA (OCSP responder).  

A new Provider's certificate (Root CA, Cross CA, subordinate CA) shall be published at the Provider's Web site after creating it.  

## 5.7 Compromise and disaster recovery   

### 5.7.1 Incident and compromise handling procedures   

#### 5.7.1.1 Incident Response and Disaster Recovery Plans  
To ensure the integrity of services, the Provider shall implement data backup and recovery procedures.  
The Provider shall have developed emergency procedures and recovery plans for the performance of trusted services in accordance with the requirements of Section 5.7.1 of TLS BR [3].  

Trusted services should be provided from two geographically separated CA systems, one of which is led as master and the other as backup for the case of failure or disaster of master one.  
Disaster recovery procedures shall be regularly reviewed and assessed (at least on an annual basis) and reviewed and updated, as necessary.  

The Provider is not obliged to publish its business continuity plans but shall provide its business continuity plan and security plan upon request to the auditor of the Provider's services.  

#### 5.7.1.2 Mass Revocation Plans  
The Provider has a mass TLS Certificate revocation plan in place that includes the provisions set out in Section 5.7.1.2 of the TLS BR [3] and maintains it for mass TLS Certificate revocation events. Starting on December 1,  2025, it will conduct annual testing of this mass TLS Certificate revocation plan, gradually incorporating the lessons learned into the existing plan to continuously improve its preparedness for mass TLS Certificate revocation events over time.  

### 5.7.2 Recovery Procedures if Computing resources, software, an/or data are corrupted  
No stipulation.  

### 5.7.3 Recovery Procedures after Key Compromise  
No stipulation.  

### 5.7.4 Business continuity capabilities after a disaster  
No stipulation.  

## 5.8 CA or RA termination  
Upon termination of the Provider's activities for reasons other than those caused by force majeure (e.g. natural disaster, state of war, state power, etc.), the procedure shall be followed in accordance with section 5.7.  
Before terminating providing the services, the Provider shall:  
* At least 6 months in advance notify the supervisory Authority, all Subscribers/Holders of valid TLS Certificates, the Relying Parties and to the public planned closure of its activities. This notice shall be made through the Provider's website, electronic mail, ordinary mail, registration authorities, or electronic media and printing.
* Terminate all existing mandate contracts, powers of attorney under which other legal persons could act on behalf of the Provider.  
* To conclude a contract with another CA that would ensure continuity in providing trusted services, if possible.  
* To collect and prepare all documents associated with the trusted services provided for archiving according to the PMA guidelines.  
* To check compliance with privacy rules e. g. Regulation (EU) 2016/679 of the European Parliament and of the Council - General Data Protection Regulation and Act No. 18/2018 Z. z. on the Protection of Personal Data (hereinafter referred to as "Personal Data Protection Regulations") [18].  
* Eliminate all private keys, including all their copies, in such a way that they can no longer be restored.  

Upon termination of its activity, the Provider will not issue any certificate and will guarantee impossibility to re-use the Provider's private keys.  
Before terminating their activities, each RA will provide all archived data to the Provider as instructed by the PMA.  
The Provider shall have a solution to cover all the costs associated with meeting the minimum termination requirements in the event of bankruptcy or any other cause when it will be unable to cover the costs by its own means, in accordance with applicable bankruptcy legislation.

# 6. Technical Security Controls   
The technical part of the Provider's infrastructure (hardware and software) shall consist only of secure systems and official software. The infrastructure architecture of the Provider shall be designed with components that meet safety standards at the level of current knowledge.  

Particular attention shall be paid to the cryptographic module (HSM), which serves to generate, store, and use the Provider's private keys and is one of the most vulnerable assets. The private keys of the Provider shall be stored in an HSM module that is certified at least according to the FIPS 140-2 Level 3 standard. 

The Provider shall use a combination of physical, logical, and procedural measures to ensure its security to protect its private key. These measures shall be described, for example, in the published CP/CPS.  
The Provider's system shall contain a device for the continuous detection, monitoring, and signaling of unauthorized and unusual attempts to access its resources.  
Publishing applications shall provide access control before trying to add or delete a TLS Certificate or modify other associated data.  

Revocation status reporting shall provide access control before attempts to modify revocation status information.  
All Provider features that use a computer network shall be secured against unauthorized access and other malicious activities.  

## 6.1 Key pair generation and installation  

### 6.1.1 CA Key Pair Generation 

#### 6.1.1.1 Certificate issuer
Generating and installing a Provider's key pair shall be done in a standardized way detailed in the Provider's documentation in accordance with the requirements in Section 6.1.1.1 of TLS BR [3].   
The key pair generating shall provide sufficient confidence in the process and the entire process shall be recorded in writing. Authorized staff in trusted roles who are eligible to participate in the key generation and request generation process shall ensure key generation. Key generation shall be done in a secure cryptographic module.  
The Provider CA key pairs are generated in a formal "key ceremony" that:
* takes place in a secure environment that meets the physical security requirements of Section 5.1;  
* uses hardware security modules (HSMs) that meet the requirements of [FIPS 140-2 Level 3 or higher / EN 419 221-5 or equivalent];  
* involves the necessary number of individuals in trusted roles acting according to the K/N principle;  
* is documented in detail, including participants, devices, date and time, and resulting key and TLS Certificate fingerprints;  
* the key ceremony is performed according to a written procedure approved by senior management.  

#### 6.1.1.2 RA Key Pair Generation  
No stipulation.

#### 6.1.1.3 Subscriber Key Pair Generation
Key pair generation is performed by the user (applicant) himself, using appropriate software or hardware that meets the minimum requirements for key length and required algorithms.  
The Provider shall reject a TLS Certificate request if one or more of the following conditions are met:  

**1.** The Key Pair does not meet the requirements set forth in Section 6.1.5 and/or Section 6.1.6;  
**2.** There is clear evidence that the specific method used to generate Private Key was flawed;  
**3.** The Provider is aware of a demonstrated or proven method that exposes the Applicant's private Key to compromise;  
**4.** The Provider has previously been made aware that the Applicant's private key has suffered a key compromise, such as through the provisions of Section 4.9.1.1;  
**5.** The Provider is aware of a demonstrated or proven method to easily compute the Applicant's Private Key based on the Public Key (such as a Debian weak key, see [https://wiki.debian.org/SSLkeys](https://wiki.debian.org/SSLkeys)).  

The Provider does not generate a Key Pair on behalf of a Subscriber.

### 6.1.2 Private key delivery to subscriber   
The public key delivery is done usually via email or ACME protocol. 

### 6.1.3 Public key delivery to Certificate issuer  
The public key is delivered to the certification authority securely via the RA Client application in online mode during the TLS Certificate issuance process. Communication between the RA Client application and the issuing CA is authorized by signing all sent data by an RA staff member, where the issuance authorization of the given RA staff member is checked on the CA side in automatic mode.  

### 6.1.4 CA public key delivery to relying parties  
Relying Parties can download the CA certificates from the Provider website: [https://eidas.disig.sk/en/certificates/ca/](https://eidas.disig.sk/en/certificates/ca/). 


### 6.1.5 Key sizes   
Only RSA key pairs are permitted under this CP/CPS.

For RSA key pairs, the Provider shall:

- ensure that the modulus size, when encoded, is at least 2048 bits; and
- ensure that the modulus size, in bits, is evenly divisible by 8.

ECDSA and all other public-key algorithms are not permitted.
No RSA modulus size that does not meet the requirements above is permitted. 

### 6.1.6 Public key parameters generation and quality checking   
The parameters and quality of the Provider's public key (root, subordinate CA, cross-certified CA) are determined by the PMA and quality control is checked during the key generation ceremony.

The Provider shall use cryptographic hardware modules that meet the requirements of FIPS 186-2 to generate and store keys, which ensure the random generation of RSA keys with a size of at least 2048 bits.

RSA: The Provider shall confirm that the value of the public exponent is an odd number equal to 3 or more. Additionally, the public exponent should be in the range between 2^16+1 and 2^256-1.  

The modulus should also have the following characteristics: an odd number, not the power of a prime, and have no factors smaller than 752. [Source: Section 5.3.3, NIST SP 800-89] .   

### 6.1.7 Key usage purposes (as per X.509 v3 key usage field) 
Private keys corresponding to Root Certificates shall not be used to sign Certificates except in the following cases:  
**1.** Self-signed Certificates to represent Root CA itself;  
**2.** Certificates for Subordinate CAs and Cross-Certified Subordinate CA Certificates;  
**3.** Certificates for infrastructure purposes (administrative role Certificates, internal CA operational device Certificates); and  
**4.** Certificates for OCSP Response verification.  

The keys issued by RA staff member can only be used to access the Provider's IS via the RA Client application and also to sign the data sent in the TLS Certificate issuance process by the RA Client application. They can also be used to access the razona.disig.sk portal, where all necessary information for RA staff member is available.  

## 6.2 Private Key Protection and Cryptographic Module Engineering  

### 6.2.1 Cryptographic module standards and controls  
To protect their private keys (root CAs, subordinate CAs) Provider shall use hardware cryptographic modules certified to FIPS 140-2 level 3. Modules shall be stored in secured spaces accessible only to people in trusted roles. 

Provider's CA private keys can only be used to sign TLS Certificates and CRLs issued by the Provider.  
CA equipment shall be permanently protected from unauthorized access, even from unauthorized physical access.  
The HSM module shall meet the protection against electromagnetic radiation capture.

The Provider CA's private keys:
* are stored and used exclusively in HSMs that meet the relevant security requirements;  
* are activated only by authorized personnel in K/N mode;  
* are never exported from the HSM in unencrypted form.  

### 6.2.2 Private key (K out of N) multi-person control   
In the case of operations with the Provider's private keys (e.g. generation, backup, liquidation), the appropriate number of authorized persons will participate. always on the "K" of "N" principle.   

### 6.2.3 Private key escrow  
No stipulation.  

### 6.2.4 Private key backup  
Private keys of Provider shall be generated and stored inside hardware cryptographic modules.   
Private keys shall always be encrypted in case authorized personnel within the meaning of Section 6.2.2 perform transfer them for backup and recovery purposes, transferring private keys and restoring them to another hardware cryptographic module may only.  

### 6.2.5 Private key archival  
No stipulation.  

### 6.2.6 Private key transfer into or from a cryptographic module  
See Section 6.2.4.  

### 6.2.7 Private key storage on cryptographic module  
Private keys of subordinate CA used to sign TLS Certificates issuing to end-users shall be stored in the HSM. Private keys may leave the module only in encrypted form that will not allow their to restore without the appropriate number of authorized persons on the principal "K" out of "N".  
All The HSM Modules of the Provider shall be operated in secure environment with access control.  

### 6.2.8 Activating Private Keys  
Authorized persons according to the Section 6.2.2 can only activate the private keys of the Provider.  
Upon activation, shall each authorized person from the required number of eligible persons insert his smart card into the HSM module and enter a password.  

The protection of private key by the Subscriber/Holder whom Provider issued TLS Certificate is sole responsibility pf Subscriber/Holder. The Provider shall advise all Subscribers/Holders to protect their private keys by using a strong password to prevent their private key being misused.  

### 6.2.9 Deactivating Private Keys  
Deactivation of the private key in the HSM module can only be done by an authorized person (CA administrator) or the private keys can be deactivated automatically in the event of a session failure or the power supply failure of the HSM module.  

### 6.2.10 Destroying Private Keys  
The Provider shall ensure by technical and organizational measures that the Provider's Private Key cannot be used after the end of his life cycle. The end of the life cycle of the CA private key and the technical and organizational measures taken shall be done with a record signed by all the actors present.  

### 6.2.11 Cryptographic Module Rating  
See Section 6.2.1.  

## 6.3 Other aspects of key pair management  

### 6.3.1 Public key archival  
No stipulation.  
### 6.3.2 Certificate operational periods and key pair usage periods  

The validity of the Certificate issued by the Provider and the usability of the key pair shall not exceed the following  
|Certificate type|Validity (minimum)|Validity (maximum)|
|----------------|:------------------:|:------------------:|
|Root CA|2922 days |9132 days |
|Subordinate CA||1095 days|
|TLS Certificate|-| 200 days from 15.3.2026 to 14.3.2027<br> 100 days from 15.3.2027 to 14.3.2029<br> 47 days from 15.3.2029|

To calculations, a day is measured as 86,400 seconds. Any amount of time greater than this, including fractional seconds and/or leap seconds, shall represent an additional day.  

## 6.4 Activation data  

### 6.4.1 Activation data generation and installation  
The activation data for the RA staff member's private key is selected by the RA staff member himself immediately after receiving the hardware device, before its first use to access the Provider's IS via the RA Client application.  

### 6.4.2 Activation data protection  
The RA staff member is solely responsible for protecting the RA staff member's private keys.  
When issuing a TLS Certificate, each RA staff member is notified by the Provider's responsible person of the need to protect the private key with a strong password to prevent its misuse throughout the entire period of its use.  

### 6.4.3 Other aspects of activation data  
No stipulation.  

## 6.5 Computer security controls  

### 6.5.1 Specific computer security technical requirements  
The Provider shall perform all the functions of a trusted service Provider using a trusted system that shall meet the requirements defined in its Security Project for information systems.  
Provider issuing TLS Certificates shall meet the specific information security requirements of a trusted service Provider as defined in ETSI EN 319 411-1 "Electronic Signatures and Infrastructures (ESI); Policy and security requirements for Trust Service Providers issuing Certificates; Part 1 General requirements" [10] 
 
All systems shall be regularly verified for malicious code and protected against spyware and viruses.  
The Provider shall enforce multi-factor authentication for all accounts capable of directly causing TLS Certificate issuance.  

### 6.5.2 Computer security rating  
No stipulation.  

## 6.6 Life cycle technical controls  

### 6.6.1 System development controls  
Provider uses strict guidelines and methods when building software for CA operations to make sure it is safe and reliable. 
Every code change MUST be reviewed by another person. Only approved and trusted developers can commit code.
Updates of third party software, e.g. linting tools, are monitored and should be updated nolater than three months from the latest update.  

### 6.6.2 Security management controls  
No stipulation.  

### 6.6.3 Life cycle security controls  
No stipulation.  

## 6.7 Network security controls  
The Provider protects its CA systems and infrastructure from unauthorized access by implementing strong network security controls. 
The Provider complies with the CA/Browser Forum's Network and Certificate System Security Requirements [22].  

## 6.8 Time-stamping  
No stipulation.  

# 7. Certificate, CRL, and OCSP profiles  
TLS Certificate profiles and Certificate Revocation Lists are set centrally - RA staff member cannot change the structure of TLS Certificates.  

## 7.1 Certificate profile  

### 7.1.1 Version number  
This CP/CPS only allows issuing TLS Certificates conforming to X.509 version 3.  

### 7.1.2 Certificate Content and Extensions  

#### 7.1.2.1 Root CA Certificate Profile
Algorithms and key lengths applied in the Root Certificate of the Provider:  

|  | |
| :--- | :--- |
| Signature AlgorithmName:|**sha256RSA**|
| Public key:|**RSA, length 4 096 bits**|

Table 3 Content of items in the Root CA Certificate subject   

|Name abbr.|OID     |Name       |Content  |
|:-----:   |:------:|:---------:|:-------:|
|C         |2.5.4.6 |countryName|SK       |
|L         |2.5.4.7 |localityName|Bratislava|
|O         |2.5.4.10|organizationName|Disig a.s.|
|CN        |2.5.4.3 |commonName  |depending on the CA type ¹ |

¹ The CN shall contain the business name of the certification authority t. j. CA Disig complemented as required root distinguishing name of CA Disig with e.g., Root R3 etc.  

From 15.9.2023, the subject of the root CA Certificate can only contain items given in Section 7.1.2.10.2 of TLS BR [3].  


Table 4 Certificate extensions in the Root CA Certificate  

|Extension / OID|Presence  |Critical  |
|---------------|:--------:|:--------:|
|basicConstraints / 2.5.29.19|YES|YES|
|keyUsage / 2.5.29.15|YES|YES|
|subjectKeyIdentifier / 2.5.29.14|YES|NO|

From 15.9.2023, the certificate extensions of the root CA Certificate can only contain items given in Section 7.1.2.1.2 of TLS BR [3].  

#### 7.1.2.2 Cross-Certified Subordinate CA Certificate Profile  
This profile applies to the cross-certificate issued by the CA Disig Root R2 to the CA Disig TLS Root R3 for the purpose of bridging trust during the transition to a single-purpose TLS hierarchy.  
This certificate is intended for the issuance of Organization Validated (OV) TLS certificates and shall not be used to issue end-entity certificates directly.

The certificate profile complies with the TLS BR [3] and the root program policies of Google, Apple, Mozilla, and Microsoft. 
The certificate shall be technically constrained to the serverAuth Extended Key Usage (EKU). 

The keyUsage extension shall be marked as critical with keyCertSign and cRLSign bits set.   
The signature algorithm shall be SHA-256 or stronger. The public key shall be an RSA key with a minimum length of 4096 bits. 
The certificatePolicies extension shall contain the OV policy identifier (2.23.140.1.2.2) to signal compliance with the TLS Baseline Requirements for Organization Validation.

Algorithms and key lengths applied in the Cross-Certified Subordinate CA:   
|  | |
| :--- | :--- |
| Signature AlgorithmName:|**sha256RSA**|
| Public key:|**RSA, length 4 096 bit**|

Table 5 The content of the items in the Cross-Certified Subordinate CA subject 
|Name abbr.|OID|Name|Content|
|:----------:|:---:|:----:|:-------:|
|C|2.5.4.6|countryName|SK|
|L|2.5.4.7|localityName|Bratislava|
|O|2.5.4.10|organizationName|Disig a.s.|
|CN|2.5.4.3|commonName|CA Disig TLS Root R3|


Table 6 Certificate extensions in Cross-Certified Subordinate CA  
|Extension / OID|Presence|Severity|
|---------------|:--------:|:--------:|
|subjectKeyIdentifier / 2.5.29.14|YES|NO|
|authorityKeyIdentifier / 2.5.29.35|YES|NO|
|authorityInfoAccess / 1.3.6.1.5.5.7.1.1|YES|NO| 
|crlDistributionPoints / 2.5.29.31|YES|NO|
|certificatePolicies / 2.5.29.32|YES|NO|
|extKeyUsage /  2.5.29.37|YES|NO|
|basicConstraints / 2.5.29.19|YES|YES|
|keyUsage / 2.5.29.15|YES|YES|

#### 7.1.2.3 Technically Constrained Non-TLS Subordinate CA Certificate Profile  
No stipulation.  

#### 7.1.2.4 Technically Constrained TLS Precertificate Signing CA Certificate Profile  
No stipulation.  

#### 7.1.2.5 Technically Constrained TLS Subordinate CA Certificate Profile  
No stipulation.  

#### 7.1.2.6 TLS Subordinate CA Certificate Profile  
Algorithms and key lengths applied in the TLS Subordinate CA:  
|  | |
| :--- | :--- |
| Signature AlgorithmName:|**sha256RSA**|
| Public key:|**RSA, length 2 048 bit**|
|Validity of subordinate CA|maximum 3 years|

Table 7 The content of the items in the TLS Subordinate CA subject 
|Name abbr.|OID|Name|Content|
|:----------:|:---:|:----:|:-------:|
|C|2.5.4.6|countryName|SK|
|L|2.5.4.7|localityName|Bratislava|
|O|2.5.4.10|organizationName|Disig a.s.|
|CN|2.5.4.3|commonName|depending on the CA type ²|

² The CN shall contain the business name of the certification authority e. g. CA Disig complemented as required root distinguishing name of CA Disig with e.g., R2I2 Certification Service etc.  

From 15.9.2023, the subject of the TLS Subordinate CA Certificate can only contain items given in Section 7.1.2.10.2 TLS BR [3].  

Table 8 Certificate extensions in TLS Subordinate CA  
|Extension / OID|Presence|Severity|
|---------------|:--------:|:--------:|
|authorityKeyIdentifier / 2.5.29.35|YES|NO|
|basicConstraints / 2.5.29.19|YES|YES|
|certificatePolicies / 2.5.29.32|YES|NO|
|keyUsage / 2.5.29.15|YES|YES|
|subjectKeyIdentifier / 2.5.29.14|YES|NO|
|crlDistributionPoints / 2.5.29.31|YES|NO|
|extKeyUsage /  2.5.29.37|YES|NO|
|authorityInfoAccess / 1.3.6.1.5.5.7.1.1|YES|NO|  

From 15.9.2023, the TLS Subordinate CA Certificate can only contain the extensions given in Section 7.1.2.6.1 TLS BR [3].  

The cRLDistributionPoints extension contains the HTTP URL of the CA’s CRL service as specified in Section 2.2.3 of this CP/CPS. 

#### 7.1.2.7 Subscriber (Server) Certificate Profile  
Details on the content of the subject of TLS Certificates issued pursuant to this CP/CPS are given in Section 3.1.4.  

Next table lists the extensions used in issued TLS Certificates.  

|Extension name|ASN.1 name and OID / Description|Presence  |Critical  |
|--------------|--------------------------------|:--------:|:--------:|
|AuthorityInfoAccess|{id-pe-authorityInfoAccess}<br>{1.3.6.1.5.5.7.1.1}<br>Specifies the address (http// ...p7c, TLS Certificate or ldap//...) <br>where is possible to obtain the Certificates issued to the publisher of this TLS Certificate and the address of the OCSP.|YES|NO|
|Authority Key Identifier|{id-ce-authorityKeyIdentifier}<br>{2.5.29.35}<br>It identifies the public key to be used to verify the signature on this <br>TLS Certificate or CRL.|YES|NO|
|Certificate Policies|{id-ce-TLS CertificatePolicies}<br>{2.5.29.32}<br>This extension lists TLS Certificate policies, recognized by the issuing CA, <br>which apply to the TLS Certificate,<br> together with optional qualifier information pertaining to these TLS Certificate policies.|YES|NO|
|Extended Key Usage|{id-ce-extKeyUsage}<br>[2.5.29.37]<br>This field indicates one or more purposes for which the certified public key may be used, <br>in addition to or in place of the basic purposes indicated in the key usage extension field.|YES|NO|
|subjectAltName|id-ce-subjectAltName<br>[2.5.29.17]<br>This extension contains one or more alternative names, using any of a variety of name forms, <br>for the entity that is bound by the CA to the certified public key.|YES|NO|
|Key Usage|{id-ce-keyUsage}<br>{2.5.29.15}<br>This extension indicates the purpose for which the certified public key is used.|YES|YES|
|CRL Distribution Points|{id-ce-CRLDistributionPoints}<br>{2.5.29.31}<br>This field identifies the CRL distribution point or points to which a <br>TLS Certificate user should refer to ascertain if the TLS Certificate has been revoked|YES|NO|  

The cRLDistributionPoints extension contains the HTTP URL of the CA’s CRL service as specified in Section 2.2.3 of this CP/CPS. 

##### 7.1.2.7.1 Subscriber Certificate Types  
Pursuant to this CP/CPS, the Provider only issues "Organization Validated (OV)" type TLS Certificates.  

##### 7.1.2.7.2 Domain Validated  
The Provider does not issue this type of TLS Certificate.  

##### 7.1.2.7.3 Individual Validated  
The Provider does not issue this type of TLS Certificate.  

##### 7.1.2.7.4 Organization Validated  
The "Organization Validated" profile of the TLS Certificate shall meet the requirements given in Section 7.1.2.7.4 of TLS BR [3].  

##### 7.1.2.7.5 Extended Validation  
The Provider does not issue this type of TLS Certificate.  

##### 7.1.2.7.6 Subscriber Certificate Extensions  
Certificates issued to the end user may only contain the extensions given in Section 7.1.2.7.6 TLS BR [3].  

##### 7.1.2.7.7 Subscriber Certificate Authority Information Access  
The "Authority Information Access" entry in the end-user TLS Certificate shall comply with the requirements given in Section 7.1.2.7.7 of the TLS BR [3].  

##### 7.1.2.7.8 Subscriber Certificate Basic Constraints  
The end-user TLS Certificate does not contain this item. 

##### 7.1.2.7.9 Subscriber Certificate Policies  
The "Certificate Policies" entry in the end-user TLS Certificate shall comply with the requirements given in Section 7.1.2.7.9 of the TLS BR [3].  

##### 7.1.2.7.10 Subscriber Certificate Extended Key Usage
The "Extended Key Usage" entry in the end-user TLS Certificate shall comply with the requirements given in Section 7.1.2.7.10 of the TLS BR [3].  
The "Extended Key Usage" entry in the end-user TLS certificate contains only the id-kp-serverAuth (1.3.6.1.5.5.7.3.1) Key Purpose.  

##### 7.1.2.7.11 Subscriber Certificate Key Usage  
The "Key Usage" entry in the end-user TLS Certificate shall comply with the requirements given in Section 7.1.2.7.11 of the TLS BR [3].
The "Key Usage" entry in the Provider-issued end-user TLS certificate shall contain only `digitalSignature` and `keyEncipherment`.  

##### 7.1.2.7.12 Subscriber Certificate Subject Alternative Name  
The "Subject Alternative Name" entry in the end-user TLS Certificate shall comply with the requirements given in Section 7.1.2.7.12 of the TLS BR [3].  

#### 7.1.2.8 OCSP Responder Certificate Profile  
If the Provider does not directly sign OCSP responses, it may make use of an OCSP authorized responder, as defined by RFC 6960 [19]. The issuing CA of the responder shall be the same as the issuing CA for the TLS Certificates it provides responses for.  
The OCSP responder's TLS Certificate profile shall comply with the requirements given in Section 7.1.2.8 of TLS BR [3].  

##### 7.1.2.8.1 OCSP Responder Validity  
The validity of the OCSP responder's TLS Certificate shall comply with the requirements given in Section 7.1.2.8.1 of TLS BR [3].  

##### 7.1.2.8.2 OCSP Responder Extensions  
The extensions in the responder's OCSP TLS Certificate shall comply with the requirements given in Section 7.1.2.8.2 of TLS BR [3].  

##### 7.1.2.8.3 OCSP Responder Authority Information Access  
The "Authority Information Access" in the responder's OCSP TLS Certificate shall comply with the requirements given in Section 7.1.2.8.3 of TLS BR [3].  

##### 7.1.2.8.4 OCSP Responder Basic Constraints
"Basic Constraints" in the responder's OCSP TLS Certificate shall comply with the requirements given in Section 7.1.2.8.4 of TLS BR [3].  


##### 7.1.2.8.5 OCSP Responder Extended Key Usage  
"Extended Key Usage" in the responder's OCSP TLS Certificate shall comply with the requirements given in Section 7.1.2.8.5 of TLS BR [3].  

##### 7.1.2.8.6 OCSP Responder id-pkix-ocsp-nocheck
"id-pkix-ocsp-nocheck" in the responder's OCSP TLS Certificate shall comply with the requirements given in Section 7.1.2.8.6 of TLS BR [3].  

##### 7.1.2.8.7 OCSP Responder Key Usage  
"Key Usage" in the responder's OCSP TLS Certificate shall comply with the requirements given in Section 7.1.2.8.7 of TLS BR [3].  

##### 7.1.2.8.8 OCSP Responder Certificate Policies  
"Certificate Policies" in the responder's OCSP TLS Certificate shall comply with the requirements given in Section 7.1.2.8.8 of TLS BR [3].  

#### 7.1.2.9 Precertificate profile  
A precertificate is a signed data structure that can be submitted to a Certificate Transparency log, as defined by RFC 6962 [23].  
A TLS Precertificate appears structurally identical to a TLS Certificate, except for a special critical poison extension in the extensions field, with the OID of 1.3.6.1.4.1.11129.2.4.3.  
This extension ensures that the TLS Precertificate will not be accepted as a TLS Certificate by clients conforming to RFC 5280. The existence of a signed TLS Precertificate can be treated as evidence of a corresponding TLS Certificate also existing, as the signature represents a binding commitment by the Provider that it may issue such a TLS Certificate.  

A TLS Precertificate was created after the Provider has decided to issue a TLS Certificate, but prior to the actual signing of the TLS Certificate. The Provider may construct and sign a TLS Precertificate corresponding to the TLS Certificate, for the purpose of submitting to Certificate Transparency Logs.  
The Provider may use the returned signed Certificate Timestamps to then alter the Certificate's extensions field, adding a Signed Certificate Timestamp List, as defined in Section 7.1.2.11.3, and as permitted by the relevant profile, prior to signing the TLS Certificate.  

TLS Precertificate profile describes the transformations that are permitted to a TLS Certificate to construct a TLS Precertificate. The Provider shall not issue a TLS Precertificate unless they are willing to issue a corresponding TLS Certificate, regardless of whether they have done so.   Similarly, the Provider shall not issue a TLS Precertificate unless the corresponding TLS Certificate conforms to the TLS BR [3], regardless of whether the Provider signs the corresponding TLS Certificate.  
A TLS Precertificate may be issued either directly by the Issuing CA or by a technically constrained TLS Precertificate signing CA, as defined in Section 7.1.2.4 TLS BR [3].  

##### 7.1.2.9.1 TLS Precertificate Profile Extensions - Directly Issued  
Extensions shall comply with the requirements given in Section 7.1.2.9.1 of the TLS BR [3].  

##### 7.1.2.9.2 TLS Precertificate Profile Extensions - TLS Precertificate CA Issued  
No stipulation.  

##### 7.1.2.9.3 TLS Precertificate Poison  
The TLS Precertificate shall contain the TLS Precertificate poison extension (OID: 1.3.6.1.4.1.11129.2.4.3).  
This extension shall have an extnValue OCTET STRING which is exactly the hex-encoded bytes 0500, the encoded representation of the ASN.1 NULL value, as specified in RFC 6962 [23], Section 3.1.  

##### 7.1.2.9.4 TLS Precertificate Authority Key Identifier  
No stipulation.  	

#### 7.1.2.10 Common CA Fields  
Before issuing a CA Certificate, the Provider shall ensure that the content of the CA Certificate, including the content of each item, fully meets all the requirements of at least one CA Certificate profile documented in Section 7.1.2 in accordance with the description of items in Section 7.1.2.1 of TLS BR [3].  

#### 7.1.2.11 Common Certificate Fields  
Before issuing a TLS Certificate, the Provider shall ensure that the content of the TLS Certificate, including the content of each item, fully meets all the requirements of at least one TLS Certificate profile documented in Section 7.1.2 in accordance with the description of items for certificate type in Section 7.1.2.7 of TLS BR [3].  

#### 7.1.3 Algorithm object identifiers  

#### 7.1.3.1 SubjectPublicKeyInfo  
The following requirements apply to the subjectPublicKeyInfo field within a TLS Certificate or TLS Precertificate. No other encoding is allowed.  

##### 7.1.3.1.1 RSA  
The Provider shall mark the RSA key with the algorithm identifier rsaEncryption (OID: 1.2.840.113549.1.1.1). Parameters shall be present and shall be explicitly NULL.

The Provider shall not use another algorithm, such as the algorithm identifier id-RSASSA-PSS (OID: 1.2.840.113549.1.1.10), to mark the RSA key.  

When encoded, the AlgorithmIdentifier for RSA keys shall be byte-for-byte identical to the following hexadecimal-encoded bytes:  
`300d06092a864886f70d0101010500`

##### 7.1.3.1.2 ECDSA  
No stipulation.  

#### 7.1.3.2 Signature AlgorithmIdentifier  
All objects signed using the Provider's CA Private Keys shall comply with the requirements of Section 7.1.3.2 of the TLS BR [3] concerning the use and encoding of an AlgorithmIdentifier or an AlgorithmIdentifier-derived type in the context of signatures.

The Provider shall use only RSASSA-PKCS1-v1_5 with SHA-256 for signing Subscriber Certificates and all other objects signed using the applicable CA Private Key.

When encoded, the AlgorithmIdentifier shall be byte-for-byte identical to the following hexadecimal value:`300d06092a864886f70d01010b0500`

No other signature algorithm or AlgorithmIdentifier encoding is permitted under this CP/CPS.

##### 7.1.3.2.1 RSA  
The Provider shall use a single signature algorithm and encoding in accordance with the requirements specified in Section 7.1.3.2.1 of TLS BR [3].  
The encoded "AlgorithmIdentifier" shall be byte-for-byte identical to the specified hex-encoded bytes as specified in Section 7.1.3.2 of TLS BR [3].  

##### 7.1.3.2.2 ECDSA  
No stipulation.  

### 7.1.4 Name Forms  
For all TLS Certificates issued by the Provider in terms of this CP/CPS, the encoding of the names shall be in accordance with the requirements given in Section 7.1.4 TLS BR [3].  

### 7.1.5 Name constraints  
No stipulation.  

### 7.1.6 Certificate policy object identifier  

#### 7.1.6.1  Reserved Certificate Policy Identifiers  
Issued TLS Server Certificates contain a non-critical `certificatePolicies` extension with the following policy identifiers:

* `2.23.140.1.2.2` (CA/Browser Forum Baseline Requirements for Organization Validated Certificates)
* `1.3.158.35975946.0.0.0.1.1` (Provider's internal policy identifier for OV TLS issuance)

These identifiers assert compliance with both the CA/Browser Forum Baseline Requirements and the ETSI OVCP policy framework as documented within this CP/CPS.

 *Note: The Provider's internal Policy OID (`1.3.158.35975946.0.0.0.1.1`) and the CA/Browser Forum OV Policy OID incorporated in the certificate correspond to and fulfill the requirements of the ETSI OVCP policy (ETSI EN 319 411-1 policy identifier `0.4.0.2042.1.7`).*

### 7.1.7 Usage of Policy Constraints extension  
No stipulation.  

### 7.1.8 Policy qualifiers syntax and semantics  
No stipulation.  

### 7.1.9 Processing semantics for the critical Certificate Policies extension  
No stipulation.  

## 7.2 CRL profile  
With effect from 15.3.2024, the Provider shall issue CRLs in accordance with the profile specified in Section 7.2 of TLS BR [3]. 

### 7.2.1 Version number  
All CRLs issued by the Provider shall conform to RFC 5280 and shall be Version 2.

### 7.2.2 CRL and CRL entry extensions  
The CRL shall contain the AuthorityKeyIdentifier, CRLNumber, and IssuingDistributionPoint extensions as specified in RFC 5280. The CRLs are published in the Repository at the locations defined in Section 2.2.3.  

#### 7.2.2.1 CRL Issuing Distribution Point
We issuing full and complete CRLs only.

## 7.3 OCSP profile  
If the OCSP response refers to a root CA or a subordinate CA TLS Certificate, including cross-certified CA TLS Certificates, and this TLS Certificate has been revoked, then the reason for the revocation shall be specified in the RevokedInfo CertStatus field.  
The specified revocation reason CRLReason shall contain a value allowed for CRLs as specified in Section 7.2.2 of TLS BR [3].  

### 7.3.1 Version number  
No stipulation.  

### 7.3.2 OCSP extensions  
The singleExtensions of an OCSP response shall not contain the reasonCode (OID 2.5.29.21) CRL entry extension.  

# 8. Compliance Audit and Other Assessments  
The purpose of the compliance audit is to ensure that the Provider has a satisfactory system of work that guarantees the quality of the trusted services provided by the Provider and guarantees that he is acting in compliance with all the requirements of this CP/CPS, eIDAS Regulation [8] and CA/Browser forum [3]. All aspects of the CA operation relating to this CP/CPS are to be subject to compliance audits.  

## 8.1 Frequency or circumstances of assessment  
The Provider shall undergo an audit of compliance of the trusted services provided within the meaning of the Section 1.4.1 at least once a year. In addition, each CA has the right to request regular and irregular reviews of the activities of its subordinate CMAs to confirm that subordinate CMAs operate in accordance with the security practices and procedures described in this CP/CPS.  

## 8.2 Identity/qualifications of assessor  
The auditor shall be competent in the field of compliance audits and shall be thoroughly acquainted with the audited CPS/CPS and meet the qualification requirements described in Section 8.2 TLS BR [3].  

## 8.3 Assessor's relationship with assessed entity  
No stipulation.  

## 8.4 Topics covered by assessment  
The Provider will be audited in accordance with a national scheme that assesses compliance with the latest versions of ETSI EN 319 411-1 [10], including normative references from ETSI EN 319 401 [9].  
The audit shall be conducted by a qualified auditor within the meaning of paragraph 8.2.  

## 8.5 Actions taken as a result of deficiency  
When the auditor finds a discrepancy between the CMA's operation and the CP/CPS provisions, the following actions shall be taken   
* The auditor records a discrepancy;  
* The auditor notifies the entities defined in Section 8.6;  
* The Provider will propose the PMA appropriate correction actions, including the expected time for its implementation.  

The PMA will determine the appropriate correction actions, even up to possibly revocation of the CA Certificate.   

## 8.6 Communication of results  
The audit report shall state explicitly that it covers the relevant systems and processes used in the issuance of all TLS Certificates that assert one or more of the policy identifiers listed in Section 7.1.6.1 The Provider makes the audit report publicly available.  

The Provider makes its audit report publicly available no later than three months after the end of the audit period. In the event of a delay greater than three months, the Provider shall provide an explanatory letter signed by the qualified auditor.  

The audit report shall contain at least the following clearly-labelled information:  
1. name of the organization being audited;  
2. name and address of the organization performing the audit;  
3. the SHA-256 fingerprint of all roots and subordinate CA TLS Certificates, including cross-certified subordinate CA TLS Certificates, which were in-scope of the audit;  
4. audit criteria, with version number(s), that were used to audit each of the TLS Certificates (and associated keys);  
5. a list of the Provider policy documents, with version numbers, referenced during the audit;  
6. whether the audit assessed a period of time or a point in time;  
7. the start date and end date of the audit period, for those that cover a period of time;  
8. the point in time date, for those that are for a point in time;  
9. the date the report was issued, which will necessarily be after the end date or point in time date; and  
10. or audits conducted in accordance with any of the ETSI standards - a statement to indicate if the audit was a full audit or a surveillance audit, and which portions of the criteria were applied and evaluated,  e.g. DVCP/CPS, OVCP/CPS, NCP/CPS, NCP/CPS+, LCP/CPS, EVCP/CPS, EVCP/CPS+, QCP/CPS-w, Part 1 (General Requirements), and/or Part 2 (Requirements for Trust Service Providers);  
11. for audits conducted in accordance with any of the ETSI standards - a statement to indicate that the auditor referenced the applicable CA/Browser Forum criteria, such as TLS BR [3], and the version used.  

An authoritative English language version of the publicly available audit information shall be provided by the qualified auditor, and the Provider shall ensure it is publicly available.  
The audit report shall be available as a PDF and shall be text searchable for all information required. Each SHA-256 fingerprint within the audit report shall be uppercase letters and shall not contain colons, spaces, or line feeds.  

## 8.7 Self-Audits
### 8.7.1  Certificate Sample Audits 
During the period in which the Provider issues TLS Certificates, the Provider shall monitor compliance with its CP/CPS and the requirements specified in TLS BR and control the services provided by conducting internal audits at least on a quarterly basis on a randomly selected sample of issued TLS Certificates in a number higher than one and at most in the number of three percent of the issued TLS Certificates in the period since the previous internal audit.

Certificate linting is used as part of self-audit.

### 8.7.2   Delegated Third Party Audits
The Provider does not use any Delegated Third Parties to perform verification functions or other duties under the TLS Baseline Requirements for TLS Certificates. All verification and issuance operations for TLS Certificates are performed directly by the Provider. 

# 9. Other Business and Legal Matters  

## 9.1 Fees  
There is duty of the Provider to publish a valid price list of trusted services and information under which these services can be ordered.   
The price list of trusted services or information on the contractual terms under which these services can be ordered is published on the Provider's website (see Section 1).  

### 9.1.1 Certificate issuance or renewal fees  
Fee for TLS Certificates shall be paid on the terms agreed with the Subscriber / Holder.   
Provider has to publish a valid price list of his services on its company's web site (see Section 1).  
In the case of the provision of its services only to the contractual partner, the price list need not be published.  

### 9.1.2 Certificate access fees   
See Section 9.1.1.  

### 9.1.3 Revocation or status information access fees   
These services are provided free of charge.  

### 9.1.4 Fees for other services  
See Section 9.1.1  

### 9.1.5 Refund policy  
In justified cases, the Provider can reimburse the payment for the services provided based on an individual assessment.   

## 9.2 Financial responsibility   
The Provider shall have sufficient resources to perform the trust services in order to remain solvent and be able to pay indemnities in the case of a court decision or settlement of claims arising from the provision of these services.  
The Provider has sufficient resources to perform the trusted services it provides.  

### 9.2.1 Insurance coverage  
The Provider shall be insured of possible damage that may be caused to the Holder of Certificates or third parties in relation to the provision of trusted services.  
The Provider shall be liable for damages arising from the use of a TLS Certificate issued by him under applicable legislation (e.g., Commercial Code, Civil Code). The assumption is that the relevant provisions of this CP/CPS have been complied with. 

Liability for damage and the resulting settlement can only be accepted provided that 
* The Holder has not violated his / her obligations (especially protection of his / her private key)ô  
* Anyone who relied on a TLS Certificate issued by the Provider has done everything to prevent any damage, in particular by having verified the status of the TLS Certificate in question i.e., whether the TLS Certificate was not revoked at the decisive time when it was relied upon.   

The Provider does not have any financial responsibility for any damages that would arise to the Certificate Holder or the relying party in connection with the use of the TLS Certificate in a specific software application or in connection with the fact that the TLS Certificate cannot be used with the specific application or hardware.  

Any claim for damages shall be filed in writing.  
The Provider is insured against possible damages that may be caused to the Subscriber/Certificate Holder or third parties in connection with the provision of trusted services.  

### 9.2.2 Other assets  
No stipulation.  

### 9.2.3 Insurance or warranty coverage for end-entities  
No stipulation.  

## 9.3 Confidentiality of business information  

### 9.3.1 Scope of confidential information  
Confidential information subject to appropriate protection shall be  
* private keys of the Provider used to sign TLS Certificates issued to subordinate Cas;   
* private keys of subordinate CAs used to sign TLS Certificates issued to end-users;  
* private keys of OCSP services;  
* private keys belonging to the executive components of the Provider (RA Staff memeber);  
* infrastructure (e.g., documents, procedures, procedures, files, scripts, passwords, etc.) serving to ensure the operation of the Provider's CA;  
* Personal data of holders of TLS Certificates subject to protection under the Personal Data Protection Regulations [18].   

The TLS Certificate may only contain the information that is important and necessary for performing secure communication with the TLS Certificate.  
A list of revoked TLS Certificates (CRLs) is not considered confidential.  

### 9.3.2 Information not within the scope of confidential information  
The Provider may not disclose information relating to the Subscriber or the Certificate Holder to any third party. Disclosure is possible only if:
 it is permitted by this CP/CPS; it is required by law or by the order of the Competent Court or given in contract between the Provider and his Subscriber. Each requirement for the release of information shall be authenticated and documented. 

The Provider shall treat the Subscriber's personal data in accordance with applicable laws and shall not provide it to any third party except for entities legally entitled to assess the activity of the Provider or competent governmental bodies such as the police, court, or prosecutor, respectively.  

### 9.3.3 Responsibility to protect confidential information  
Participants who receive confidential information are responsible for their protection against disclosure and shall refrain from providing it to a third party.  

## 9.4 Privacy of personal information  

### 9.4.1 Privacy plan   

The Provider shall process the Personal Data of the Subscribers / Certificate Holders or authorized persons respectively in accordance with the requirements of Personal Data Protection Regulations [15].   

### 9.4.2 Information treated as private  
The Provider shall have a defined scope of personal data that is processed when providing qualified trusted services.  

### 9.4.3 Information not deemed private
The Provider may, in accordance with the Personal Data Protection Regulations [18] define the types of information he conducts in providing trusted services and are not considered personal data.  

### 9.4.4 Responsibility to protect private information  
Participants who obtain personal data are responsible for their protection against disclosure and shall refrain from providing it to a third party.  

### 9.4.5 Notice and consent to use private information  
The Provider is obliged to proceed in accordance with the Personal Data Protection Regulations in fulfilling the information obligation towards the persons concerned and in obtaining their consent to the processing of personal data [18].  

### 9.4.6 Disclosure pursuant to judicial or administrative process  
The Provider may also provide these data to third parties if the relevant legislation is imposed or permitted to do this.  

### 9.4.7 Other information disclosure circumstances  
No stipulation.  

## 9.5 Intellectual property rights  
This CP/CPS and the related documents represent important Provider's expertise and are protected by copyright.  
The Provider is the holder of the exclusive rights to the IS of the Provider and to the content of its web site.  

## 9.6 Representations and warranties  
Provider through this CP/CPS, General terms and conditions [12] and, where applicable, the TLS Certificate issuance agreement expresses legal assumptions regarding the use of issued TLS Certificates by the Subscriber/Holder and the relying party.  

### 9.6.1 CA Representations and Warranties

By issuing an Organization Validated (OV) TLS Certificate, the Provider makes the certificate warranties listed herein to the following Certificate Beneficiaries:
1. The Subscriber that is a party to the Subscriber Agreement or Terms of Use for the Certificate;
2. All Application Software Suppliers with whom the Root CA has entered into a contract for inclusion of its Root Certificate in software distributed by such Application Software Supplier (Root Store Operators); and
3. All Relying Parties who reasonably rely on a Valid Certificate.

The Provider represents and warrants to the Certificate Beneficiaries that, during the period when the Certificate is valid, the Provider has complied with the CA/Browser Forum Baseline Requirements and its CP/CPS in issuing and managing the Certificate.

The Certificate Warranties specifically include, but are not limited to, the following:

1. **Right to Use Domain Name**: That, at the time of issuance, the Provider:
   - **i.** implemented a procedure for verifying that the Applicant either had the right to use, or had control of, the Domain Name(s) listed in the Certificate's subject field and `subjectAltName` extension (or was delegated such right or control by someone who had such right to use or control);
   - **ii.** followed the procedure when issuing the Certificate; and
   - **iii.** accurately described the procedure in Section 3.2.2.4 of this CP/CPS.
   *(Note: The Provider does not issue TLS Certificates for IP addresses).*

2. **Authorization for Certificate**: That, at the time of issuance, the Provider:
   - **i.** implemented a procedure for verifying that the Subject authorized the issuance of the Certificate and that the Applicant Representative is authorized to request the Certificate on behalf of the Subject;
   - **ii.** followed the procedure when issuing the Certificate; and
   - **iii.** accurately described the procedure in this CP/CPS.

3. **Accuracy of Information**: That, at the time of issuance, the Provider:
   - **i.** implemented a procedure for verifying the accuracy of all of the information contained in the OV TLS Certificate;
   - **ii.** followed the procedure when issuing the Certificate; and
   - **iii.** accurately described the procedure in this CP/CPS.

4. **Identity of Applicant (Organization Validation)**: That, as the Certificate contains Subject Identity Information, the Provider:
   - **i.** implemented a procedure to verify the identity and legal existence of the Applicant/Subject in accordance with Section 3.2 and Section 7.1.2;
   - **ii.** followed the procedure when issuing the Certificate; and
   - **iii.** accurately described the procedure in this CP/CPS.

5. **Subscriber Agreement / Terms of Use**: That, if the Provider and Subscriber are not Affiliated, the Subscriber and Provider are parties to a legally valid and enforceable Subscriber Agreement that satisfies these Requirements, or, if the Provider and Subscriber are the same entity or are Affiliated, the Applicant Representative acknowledged the Terms of Use.

6. **Status Repository**: That the Provider maintains a 24x7 publicly-accessible Repository with current information regarding the status (valid or revoked) of all unexpired Certificates.

7. **Revocation**: That the Provider will revoke the Certificate for any of the reasons specified in these Requirements and Section 4.9 of this CP/CPS.

The Provider SHALL is responsible for the performance and warranties of any Subordinate CA operating within the hierarchy of its Root CA, for the Subordinate CA's compliance with these requirements, and for all obligations and indemnities of the Subordinate CA under these requirements, as if the Root CA were the Subordinate CA issuing the certificates.

### 9.6.2 RA representations and warranties  
The Provider does not operate any external RAs for issuing TLS certificates.  

### 9.6.3 Subscriber Representations and Warranties

The Provider MUST require, as part of the Subscriber Agreement or Terms of Use, that the Applicant make the commitments and warranties in this section for the benefit of the Provider and the Certificate Beneficiaries.

Prior to the issuance of a TLS Certificate, the Provider MUST obtain, for the express benefit of the Provider and the Certificate Beneficiaries, either:
1. The Applicant’s agreement to the Subscriber Agreement with the Provider; or
2. The Applicant’s acknowledgement of the Terms of Use.

The Provider MUST implement a process to ensure that each Subscriber Agreement or Terms of Use is legally enforceable against the Applicant. In either case, the Agreement MUST apply to the TLS Certificate to be issued pursuant to the certificate request. 

The Provider MAY use an electronic or “click-through” Agreement provided that the Provider has determined that such agreements are legally enforceable. A separate Agreement MAY be used for each certificate request, or a single Agreement MAY be used to cover multiple future certificate requests and the resulting TLS Certificates, so long as each TLS Certificate that the Provider issues to the Applicant is clearly covered by that Subscriber Agreement or Terms of Use.

The Subscriber Agreement or Terms of Use MUST contain provisions imposing on the Applicant itself the following obligations and warranties:

1. **Accuracy of Information**: An obligation and warranty to provide accurate and complete information at all times to the Provider, both in the certificate request and as otherwise requested by the Provider in connection with the issuance of the TLS Certificate(s) to be supplied by the Provider;
2. **Protection of Private Key**: An obligation and warranty by the Applicant to take all reasonable measures to assure control of, keep confidential, and properly protect at all times the Private Key that corresponds to the Public Key to be included in the requested TLS Certificate(s) (and any associated activation data or device, e.g., password or hardware token);
3. **Acceptance of Certificate**: An obligation and warranty that the Subscriber will review and verify the TLS Certificate contents for accuracy upon receipt;
4. **Use of Certificate**: An obligation and warranty to install the TLS Certificate only on servers that are accessible at the `subjectAltName`(s) listed in the TLS Certificate, and to use the TLS Certificate solely in compliance with all applicable laws and solely in accordance with the Subscriber Agreement or Terms of Use;
5. **Reporting and Revocation**: An obligation and warranty to:
   - **a.** promptly request revocation of the TLS Certificate, and cease using it and its associated Private Key, if there is any actual or suspected misuse or compromise of the Subscriber’s Private Key associated with the Public Key included in the TLS Certificate; and
   - **b.** promptly request revocation of the TLS Certificate, and cease using it, if any information in the TLS Certificate is or becomes incorrect or inaccurate;
6. **Termination of Use of Certificate**: An obligation and warranty to promptly cease all use of the Private Key corresponding to the Public Key included in the TLS Certificate upon revocation of that TLS Certificate for reasons of Key Compromise;
7. **Responsiveness**: An obligation to respond to the Provider’s instructions concerning Key Compromise or TLS Certificate misuse within a specified time period; and
8. **Acknowledgment and Acceptance**: An acknowledgment and acceptance that the Provider is entitled to revoke the TLS Certificate immediately if the Applicant violates the terms of the Subscriber Agreement or Terms of Use, or if revocation is required by the Provider’s CP/CPS or the CA/Browser Forum Baseline Requirements.  

### 9.6.4 Relying Party Representations and Warranties

Prior to relying on a TLS Certificate issued by the Provider, a Relying Party MUST represent and warrant that it:

1. **Reasonable Reliance**: Assumes full responsibility for determining whether to rely on a TLS Certificate and relies on the Certificate only to the extent that such reliance is reasonable under the circumstances;
2. **Status Verification**: Checks the validity and revocation status of the TLS Certificate prior to relying on it, by examining the current Certificate Revocation List (CRL) or Online Certificate Status Protocol (OCSP) response provided by the Provider;
3. **Chain Validation**: Validates the entire TLS Certificate chain back to the Provider’s trusted Root Certificate;
4. **Key Usage & Purpose**: Evaluates and respects the Key Usage, Extended Key Usage, and any operational limitations or constraints specified in the TLS Certificate and this CP/CPS; and
5. **Knowledge of Terms**: Has read, understood, and agreed to be bound by the relevant provisions of this CP/CPS and any applicable limitations of liability.  

### 9.6.5 Representations and warranties of other participants  
No stipulation.  

## 9.7 Disclaimers of warranties  
The Provider makes no other warranties, either express or implied, except as expressly set forth in this document and related agreements. To the maximum extent permitted by law, all other warranties – including merchantability and fitness for a particular purpose – are excluded.
Use of the Provider’s services is voluntary and at the Subscriber’s own risk.   

## 9.8 Limitations of Liability  
The Provider is not liable for indirect or contingent losses or damages incurred to the Subscribers or to the Relying Parties in connection with the use of trusted services.  
The Provider is not liable for any damages (including lost profits) incurred by the Subscriber / Holder of the TLS Certificate, relying party or to any third party due to  
**a)** violation of the obligations by the Subscriber / Holder or by the relying party under the legal, contractual, General Terms or Provider's obligations, including the obligation to exercise reasonable care when relying on the TLS Certificates;
**b)** failure to provide the necessary cooperation on the part of the Subscriber/Holder;  
**c)** by the technical features, configuration, incompatibility, inadequacy or other defects in software or hardware means used by them;  
**d)** use or reliance on the expired or revoked TLS Certificate;  
**e)** Use of the TLS Certificate by the Subscriber / Holder of the TLS Certificate in violation of the contract, the General Terms, or the Provider's policies;  
**f)** that the TLS Certificate was used contrary to its purpose or limitations stated in the TLS Certificate, in General Terms or in the CP, respectively;  
**g)** delay or non-delivery of request about Certificate status to the Provider for reasons not on the Provider's side (in particular in cases of unavailability or overloading of the Internet or defects in the equipment or technical equipment used by the verifier);  
**h)** failure to provide any of the trusted services or their unavailability during the scheduled maintenance or reorganization announced at the Provider's web site;  
**i)** due to Force Majeure.  

The Provider is not liable for damages incurred to the Relying party because, when relying on the TLS Certificate and trustworthy services of the Provider or relying on the electronic signature or seal made on their basis, did not proceed according to Section 10 of the General terms and conditions [12] or according to the requirements of this policy.  

## 9.9 Indemnities  
### 9.9.1 Liability
Any person who violates his or her obligation or any obligation under this CP/CPS, The Agreement, and the General Terms shall be liable to compensate for damage caused to the other party, except in cases where the liability of the entity is excluded for damages. The damage shall be deemed actual damage, loss of earnings and costs incurred by the injured party in respect of the damage event. Whoever violates his or her obligation or any obligation under this CP/CPS, The Contract, and the General Terms, may be relieved of liability for damages only if it proves that a breach of duty or any obligation has occurred as a result of circumstances excluding responsibility e.g., Force Majeure.

### 9.9.2 Indemnification of Application Software Suppliers
The Provider  shall defend, indemnify, and hold harmless each Application Software Supplier for any and all claims, damages, and losses suffered by such Application Software Supplier related to a TLS Certificate issued by the CA, regardless of the cause of action or legal theory involved.

## 9.10 Term and termination  

### 9.10.1 Term  
This version of the CP/CPS is effective from the date of its entry into force and is valid until replaced by a new version. For details on the history of changes to this CP/CPS, see the "Revision" Section 1.2.1.  

### 9.10.2 Termination  
This CP/CPS version will expire on the date of publication of a new version, or termination of the Provider's trusted service.   

### 9.10.3 Effect of termination and survival  
In the event that this document is not replaced by a new version and its validity expires after the finishing of providing trustworthy service by Provider, all provisions of this CP relating to the Provider, which he is obliged to observe after termination of his activity shall be fulfilled. (See Section 9).  

## 9.11 Individual notices and communications with participants  
No stipulation.  

## 9.12 Amendments  

### 9.12.1 Procedure for amendment  
The CP/CPS update is based on its review, which shall be done at least once a year from the approval of the current valid version. An authorized person of Provider who, based on the results of the review, shall prepare a written proposal for any proposed changes shall perform the review.

An authorized PMA member shall do approval of proposed changes. The proposed changes shall be considered within 14 days of their delivery. After the deadline for reviewing the change proposal, the PMA has to accept the proposed change, accept it, or refuse it.

Errors, update requests, or proposed CP/CPS changes shall be communicated to the contact listed on 1.5.2. Such communication shall include a description of the change, the reason for the change, and the contact details of the person requesting the change or suggesting the change, respectively.   

All approved CP/CPS changes shall be notified of the entities concerned within one week prior to their entry into force through the channel for publishing and notifying (see Section 2).  
Each modified version of this CP/CPS shall be numbered and registered, so the newer version shall have a higher version number than the one it replaces.  
Corrections of clutter, grammar and stylistic errors are not considered as changes initiating a change to the version of this CP/CPS.  

### 9.12.2 Notification mechanism and period  
Provider shall publish information about the current version of CP/CPS through its website (see Section 1.5.2).   
Internal employees (RA staff member) issuing TLS Certificates shall be fully informed about the new version of this CP/CPS.   

### 9.12.3 Circumstances under which OID shall be changed  
Every policy shall have its OID assigned by the Provider. The OID of this CP/CPS is listed in Section1.2 and for each new CP/CPS version remains unchanged.  

## 9.13 Dispute resolution provisions  
The Subscriber / Holder has the right to send to the Provider a complaint about the provided trusted service by email to [radisig@disig.sk](radisig@disig.sk). 

The Provider shall process the complaint no later than 30 days after its receipt, unless otherwise agreed by the parties. The complaint process refers only to a description of the defect referred to by the Subscriber.  
The Provider has to respond within 30 days of complaint receipt. The Provider reserves the right to extend this period in case of more complicated complaints.  

The courts of the Slovak Republic have exclusive jurisdiction to settle any disputes between the Provider and the Subscriber / Holder of the TLS Certificate. If the Subscriber / Holder is a consumer, any dispute may also be settled out of court. In such a case, it is entitled to contact an out-of-court dispute resolution body, Slovak trade inspection or other legal entity registered in the list pursuant to Article 5 2 of Act no. 391/2015 Coll. on alternative dispute resolution of consumer disputes, as amended. Prior to joining a court or out-of-court dispute settlement, the parties are required to try to resolve this dispute by mutual agreement first.   

## 9.14 Governing law  
The laws of the Slovak Republic govern legal relations between the Provider and the Subscribe / Holder of the TLS Certificate.   
The rights and obligations of the parties which are not governed by the General Terms, or by The Agreement are governed, in particular, by the relevant provisions of Act No. 513/1991 Coll., Commercial Code, as amended, Act no. 40/1964 Coll., The Civil Code in the wording of later regulations and other generally binding legal regulations of the Slovak Republic.  

## 9.15 Compliance with applicable law  
Provider provides trustworthy services in accordance with valid legal regulations in force in the Slovak Republic.  

## 9.16 Miscellaneous provisions  

### 9.16.1 Entire agreement  
No stipulation.  

### 9.16.2 Assignment  
The Subscriber / Holder may not assign, transfer or transfer (or otherwise deal with) any third party's rights, obligations or claims under the Agreement or the General Conditions without the written consent of the Provider.    

### 9.16.3 Severability and Conflict of Law
#### 9.16.3.1 Severability  
If any provision of this CP/CPS is or becomes invalid or unenforceable, this shall not render the entire CP/CPS invalid or unenforceable if it is completely severable from the other provisions of this CP/CPS. The Provider shall immediately replace the invalid or unenforceable provision of the CP/CPS with a new valid and enforceable provision, the subject matter of which shall correspond as closely as possible to the subject matter of the original provision and at the same time the purpose of this CP/CPS and the content of the individual provisions of this CP/CPS shall be preserved.

#### 9.16.3.2 Conflict with Law
In the event of a conflict between the TLS Baseline Requirements and a law, regulation, or government order (hereinafter "Law") of any jurisdiction in which the Provider operates or issues TLS Certificates, the Provider may modify any conflicting requirement to the minimum extent necessary to make the requirement valid and legal in that jurisdiction. This applies only to operations or TLS certificate issuances that are subject to that Law.  

In such event, the Provider shall:
1. Immediately (and prior to issuing a TLS Certificate under the modified requirement) include in Section 9.16.3 of this CP/CPS a detailed reference to the Law requiring a modification of these Requirements, and the specific modification implemented by the Provider.  
2. Prior to issuing a TLS Certificate under the modified requirement, notify the CA/Browser Forum by sending a message to [questions@cabforum.org](questions@cabforum.org) and receive confirmation that it has been posted to the Public Mailing List and indexed in the Public Mail Archives.
3. Discontinue any modification enabled under this section if and when the Law no longer applies, or the TLS Baseline Requirements are modified to permit simultaneous compliance. An appropriate change in practice, modification to the CP/CPS, and notice to the CA/Browser Forum shall be made within 90 days.

As of the date of the current revision of this CP/CPS, no such conflict or modification exists.

### 9.16.4 Enforcement  
In the event that a certain right is not exercised during the duration of the contractual relationship between the parties, this right shall not be terminated due to its non-application unless otherwise stated.
Because of the cancellation of contractual relationship between the Contracting Parties, The parties are not deprived of the obligation to fulfill all the obligations arising from the rights exercised so far and to take all necessary legal acts which do not delay the delay, and which are indispensable to prevent damage.  

### 9.16.5 Force Majeure  
Provider, Subscriber, and Holder are not responsible for delaying the fulfillment of their obligations due to circumstances excluding liability (Force Majeure).   
Circumstance for excluding is an impediment that occurs independently of the will of the obligated party and prevents it from fulfilling its duty if it is impracticable to assume that the obligated party will avert or overcome this impediment or its consequences and that, at the time of the occurrence of obstacle could foresee the obstacle or not.   

If the circumstances for excluding the liability arise, then the party on which such circumstances occur shall immediately inform the other of the nature, the beginning, and the end of such an obstacle to the fulfillment of its obligations. Provider, Subscriber, and Holder are committed to doing their utmost to avert and overcome circumstances that exclude liability.   

However, liability is not excluded if such a circumstance has occurred only when the obligated party has been late in fulfilling its obligation or if the party concerned fails to fulfill its obligation immediately inform the other of the nature and the beginning of the duration of the obstacle or if it originated from economic conditions. Effects that exclude liability are limited only to the period that an obstacle with which these effects are associated.  

## 9.17 Other provisions  
No stipulation.  