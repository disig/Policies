
# Disig TLS Certificate Policy and Certification Practice Statement (CP/CPS)


**Disig, a.s.**  
**Version 7.0**  
**Valid from March 5, 2026**  
**OID 1.3.158.35975946.0.0.0.1.1**
    

# 1. Introduction
This document is a combined Certificate Policy and Certification Practice Statement (CP/CPS) of the company Disig, a.s., with its registered office at Galvaniho 17/C, 821 04 Bratislava - mestská časť Ružinov, National Trade Register number: 35975946, registered in the Business Register of the City Court Bratislava III Section: Sa Insert No.: 3749/B, as a Trusted Service Provider (hereinafter referred to as "Provider") and applies to the root certification authorities and their subordinate certification authorities listed in Section 1.4.1 operated by the Provider, through which it provides trusted services for issuing publicly trusted TLS server Certificates (hereinafter referred to as the "TLS Certificate").  
It defines:  
Policy (CP) - the policies and rules under which TLS Certificates are issued, managed, and used, and  
Policy (CPS) - the detailed procedures and practices that the Provider implements to comply with this CP.

Publicly‐Trusted TLS Server Certificates issued to end users uniquely identify the entity to which the TLS Certificate is issued and bind this entity to the corresponding key pair. Unless the CP/CPS explicitly states that it refers to a root certification authority or subordinate certification authority TLS Certificate, the word "TLS Certificate" means the Publicly‐Trusted TLS Server Certificate of the end entity.

The Provider's website for the provided trusted services is available here:
[https://eidas.disig.sk](https://eidas.disig.sk)

## 1.1 Overview

This CP/CPS defines the creation and management of publicly trusted TLS server certificates according to X.509 version 3 [1] in accordance with RFC 5280 “Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile for the X.509 Internet” [2] and the requirements of the current versions of these documents and standards:  
* Baseline Requirements for the Issuance and Management of Publicly‐Trusted TLS Server Certificates (hereinafter referred to as “TLS BR”) [3]   
* Individual TLS root program policies requirements distributed by TLS certificate consumers such as Microsoft [4], Mozilla [5], Apple [6], Google [7]    
* Common CA Database (CCADB) policy [24],  
* Regulation (EU) No. 910/2014 of 23 July 2014 on electronic identification and trust services for electronic transactions in the internal market and repealing Directive 1999/93/EC, as amended by Regulation (EU) No 1183/2025 (hereinafter referred to as ‘eIDAS’) [8] and  
* ETSI EN 319 401 [9] and ETSI EN 319 411-1 standards. [10].  

This CP/CPS is structured in accordance with RFC 3647 [11].

The Provider confirms that this CP/CPS takes account of all requirements of the current version of TLS BR [3], which is published at [https://cabforum.org/working-groups/server/baseline-requirements/documents/](https://cabforum.org/working-groups/server/baseline-requirements/documents/).

In the event of any inconsistency between these requirements and this CP/CPS, the requirements of the current version of TLS BR [3] prevail.

## 1.2 Document Name and Identification

|  | |
| :--- | :--- |
| Document Name:|**Disig TLS Certificate Policy and <br>Certification Practice Statement (CP/CPS)** |
| Name abbreviation: | **CA Disig TLS CP/CPS** |
| Version:|  **7.0** |
| Approved on:| **March 2, 2026**   |
| Valid from:| **March 5, 2026**    |  
|This document is assigned<br> to an object identifier (OID):|**1.3.158.35975946.0.0.0.1.1** |  
 

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
|7.0|2026/03/05|Transformation of the document into a new form of a combined policy for providing the service of issuing publicly trusted TLS Certificates, which also includes the rules for providing this service,<br> which were originally the subject of a separate document. Addition of a new single-purpose CA Disig TLS Root R3 and its subordinate CA Disig R3I1 TLS Certificate Service (1.3.1.2);<br> Addition of information and profiles related to cross-TLS Certificates. ( 7); Miskovic|


##  1.3 PKI Participants  

###  1.3.1 Certification Authorities  

Root CA is the top-level Certification Authority whose Root Certificate is distributed by Application Software Suppliers. Root CA issues Subordinate CA Certificates.
Subordinate CA is a Certification Authority whose Certificate is signed by Root CA, or another Subordinate CA.    
This CP/CPS applies to the provision of trust services by subordinate certification authorities that fall under one of the CA hierarchies operated by a provider for issuing publicly trusted TLS certificates, as described below.  

####  1.3.1.1 Multi-purpose CA Hierarchy  
This hierarchy includes root CA and issuing subordinate CA, which represents the legacy CA structure operated by the Provider since its acceptance as a publicly trusted TLS Certificate provider under the corresponding root CA programs accepted by Microsoft, Mozilla, Google, and Apple.   
The hierarchy will be used to issue TLS Certificates to end users only until it is replaced by a new single-purpose hierarchy (see 1.3.1.2).


| | |
|:--- |:--- |
|Name:|**CA Disig Root R2**|
|Certificate serial number: |**0092b888dbb08ac163**|
|Thumbprint (sha1) (DER):|**B561EBEAA4DEE4254B691A98A55747C234C7D971**|
|Thumbprint (sha256) (DER):|**E23D4A036D7B70E9F595B1422079D2B91EDFBB1FB651A0633EAA8A9DC5F80703**|
|Comment:|**It issues Certificates only for subordinate certification authorities of the Provider.**|  

 

| | |
|:--- |:--- |
|Name:|**CA Disig R2I2 Certification Service**|
|Certificate serial number: |**081792523668f5c8500000000000000003**|
|Issuer:|**CA Disig Root R2**|
|Thumbprint (sha1) (DER):|**19F2783DEDD8561A61C682932EE9D5B4D86B00CE**|
|Thumbprint (sha256) (DER):|**C96F24C45113FD91AE2F9E40E106653BFA0FFBCFA07E209524C844E7C8DA4148**|
|Comment:|**It issues only TLS Certificates to end users (see 3.1.4.3)**|


#### 1.3.1.2 Single-purpose TLS CA  
This CA hierarchy replaces the legacy CA hierarchy (see 1.3.1.1) currently used to issue TLS Certificates to end users. This single-purpose TLS CA hierarchy already fully complies with the current TLS BR [3], where new root CAs are required to have a separate CA hierarchy for issuing TLS Certificates to end users and are limited to issuing Certificates containing only id-kp-serverAuth in the EKU extension (1.3.6.1.5.5.7.3.1).  
The actual issuance of TLS Certificates to end users via this hierarchy is expected to occur only after the full acceptance of the Disig TLS Root R3 single-purpose CA in the root certification authority programs of Microsoft, Mozilla, Google, and Apple.  

|  | |
| :--- | :--- |
| Name:|**CA Disig Root R3**|
| Certificate serial number:| **5b99abc2b008cf8441d62e523909b41b**|
| Thumbprint (sha1)(DER):   | **AF250F267724C554652607D70985DE93DD33AFC0**|
| Thumbprint (sha256)(DER): | **6248199FEA4811FD34AA96EF0A26DE52134B73A9A2A99678F0C2EBADF8663EF8**|
| Comment:                  | **It issues certificates only for the Provider's subordinate certification authorities reserved for issuing TLS certificates.**|  

   


|  | |
| :--- | :--- |
| Name:| **CA Disig R3I1 TLS Certification Service** |
| Issuer:|**CA Disig Root R3**|
| Comment:| **It issues only TLS Certificates to end users (see 3.1.4.3).**|  

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
Certificates issued under this CP/CPS are issued for the purpose of identifying the public key holder from a cryptographic key pair (public and private) which is used within the PKI infrastructure.  
The cryptographic key pair (private and public) and the TLS Certificate issued by the Provider can generally be used for:  
* TLS communication security (web site authentication) within public networks, including the public Internet.

Provider issues the following types of TLS Certificates to the Subscribers:   
* Publicly-Trusted TLS Server Certificate (TLS Certificate) - cryptographic keys associated with this type of TLS Certificate are designed for authentication of internet accessible servers; Publicly-Trusted Certificates are trusted by virtue of the fact that their corresponding Root Certificate is distributed in widely-available application software. The issued TLS Certificate will include, inter alia, the following certification policy identifiers for organization validation:
    * (4) etsi (0) other-TLS Certificate-policies (2042) policy-identifiers (1) ovcp (7) joint-iso-itu-t (2) international-organizations (23) ca-browser-forum (140) certified-polcies (1) baselinerequirements (2) i.e. 2.23.140.1.2.2 in the meaning of TLS BR [3].
* The Provider issues management TLS Certificates for its needs (Certificate for Subordinate CA or TLS Certificate for OCSP Responders).  

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


## 2.3 Time or frequency of publication
The TLS Certificate shall be published as soon as it is issued. Information on the TLS Certificate issued shall be available on the Provider's website. 

The TLS Certificate is published immediately after its issuance and can be immediately taken over by the Subscriber/Certificate Holder. Information about the TLS Certificate is available in the Provider's repository - see Section 1.  

The Certificate Revocation List (CRL) shall be published as specified in Section 4.9.7. Information about the revoked TLS Certificate shall be available on the Provider's website (see Section 1), which serves as its repository.

All information to be published in the repository shall be published as soon as possible.

The CRL is published as specified in Section 4.9.8. Information about the revoked TLS Certificate can be found in the Provider's repository.

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
If a domain name (FQDN) is used, it is a prerequisite that the respective second and higher-level domains belong, respectively, to the Subscriber requesting a TLS Certificate.  
The Provider shall confirm that at the time of issue of the TLS Certificate, it has verified all FQDNs in the TLS Certificate.  
Verification shall be performed at the specified time before the TLS Certificate is issued.  
Verify that the Subscriber is the domain owner or has control over the domain whose FQDN is in the CN entry or will be listed under Subject Alternative Name (SAN), shall be performed by the Provider using one of the methods specified in this paragraph.  

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

This method is available to the RA as an automated method of verifying ownership and control over a domain, where the system used to generate TLS Certificates sends a unique randomly generated value for each FQDN that is expected to be in the SAN of the issued TLS Certificate, with the proviso that this unique value must be registered in the DNS TXT record for each FQDN and must also be registered for all lower levels, up to the second level, of the given FQDNs.

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
Confirming the Subscriber control over the FQDN by sending a Random Value via email and then receiving a confirming response utilizing the Random Value. Random Value shall be sent to a DNS CAA Email Contact. The relevant CAA Resource Record Set shall be found using the search algorithm defined in RFC 8659, Section 3. [13]  

Each email may confirm control of multiple FQDNs, provided that each email address is a DNS CAA Email Contact for each Authorization Domain Name being validated. The same email may be sent to multiple recipients as long as all recipients are DNS CAA Email Contacts for each Authorization Domain Name being validated.  

The Random Value shall be unique in each email. The email may be re-sent in its entirety, including the re-use of the Random Value, provided that its entire contents and recipient(s) shall remain unchanged. The Random Value shall remain valid for use in a confirming response for no more than 30 days from its creation. The CP/CPS may specify a shorter validity period for Random Values.  

CAs using this method shall implement Multi-Perspective Issuance Corroboration as specified in Section 3.2.2.9. To count as corroborating, a Network Perspective shall observes the selected contact address used for domain validation observed by the Primary Network Perspective.
Once the FQDN has been validated using this method, the CA may also issue TLS Certificates for other FQDNs that end with all the Domain Labels of the validated FQDN. This method is suitable for validating Wildcard Domain Names.  

##### 3.2.2.4.14 Email to DNS TXT Contact  
Confirming the Applicant's control over the FQDN by sending a Random Value via email and then receiving a confirming response utilizing the Random Value. The Random Value shall be sent to a DNS TXT Record Email Contact for the Authorization Domain Name selected to validate the FQDN.
Each email may confirm control of multiple FQDNs, provided that each email address is DNS TXT Record Email Contact for each Authorization Domain Name being validated. The same email may be sent to multiple recipients as long as all recipients are DNS TXT Record Email Contacts for each Authorization Domain Name being validated.  

The Random Value shall be unique in each email. The email may be re-sent in its entirety, including the re-use of the Random Value, provided that its entire contents and recipient(s) shall remain unchanged. The Random Value shall remain valid for use in a confirming response for no more than 30 days from its creation. The CP/CPS may specify a shorter validity period for Random Values.  

CAs using this method shall implement Multi-Perspective Issuance Corroboration as specified in Section 3.2.2.9. To count as corroborating, a Network Perspective shall observes the selected contact address used for domain validation observed by the Primary Network Perspective. 
Once the FQDN has been validated using this method, the CA may also issue Certificates for other FQDNs that end with all the Domain Labels of the validated FQDN. This method is suitable for validating Wildcard Domain Names.  

##### 3.2.2.4.15 Phone Contact with Domain Contact  
This method has been retired and shall not be used.  

##### 3.2.2.4.16 Phone Contact with DNS TXT Record Phone Contact    
The Provider does not use this method.  

##### 3.2.2.4.17 Phone Contact with DNS CAA Phone Contact  
The Provider does not use this method.  

##### 3.2.2.4.18 Agreed-Upon Change to Website v2  
The Provider does not use this method.  

##### 3.2.2.4.19 Agreed-Upon Change to Website - ACME  
Confirmation of the requester's control over the FQDN is performed by verifying the domain control of the FQDN using the ACME HTTP Challenge method defined in section 8.3 of RFC 8555 [14], with the following additional requirements:    
* The Provider must receive a successful HTTP response from the request (meaning a 2xx HTTP status code must be received);  
* The token (as defined in RFC 8555 [14], Section 8.3) must not be used for more than 30 days from its creation;   
* If the Provider follows redirects, the following apply:  
   **1.** Redirects must be initiated at the HTTP protocol layer.  
        **a.** redirects must be the result of a 301, 302, or 307 HTTP status code response, as defined in RFC 7231 [15], Section 6.4, or a 308 HTTP status code response, as defined in RFC 7538 [16], Section 3. Redirects MUST be to the final value of the Location HTTP response header, as defined in RFC 7231 [15], Section 7.1.2;  
   **2.** redirects must be to resource URLs with either the "http" or "https" scheme;  
   **3.** redirects must be to resource URLs accessed via Authorized Ports.  

Except for Onion Domain Names, CAs performing validations using this method must implement Multi-Perspective Issuance Corroboration as specified in Section 3.2.2.9 of this CP/CPS.  
To be considered correct, a network perspective must respect the same challenge information (i.e. token) as the primary network perspective.  
This method is not suitable for validating wildcard domain names.  

##### 3.2.2.4.20 TLS Using ALPN  
The Provider does not use this method.  

##### 3.2.2.4.21 DNS Labeled with Account ID - ACME  
The Provider does not use this method.  

##### 3.2.2.4.22 DNS TXT Record with Persistent Value  
The Provider does not use this method.  

#### 3.2.2.5 Authentication for an IP Address  
The Provider does not issue TLS Certificates if the commonName or subjectAlernativeName extension is an IP address.  

#### 3.2.2.6 Wildcard Domain Validation  

Before issuing a TLS Certificate with a wildcard character (\*) in a CN or subjectAltName of type DNS-ID, the Provider shall establish and follow a documented procedure [^pubsuffix] that determines if the wildcard character occurs in the first label position to the left of a "registry-controlled" label or is a "public suffix" (e.g. "*.com", "*.co.uk", see RFC 6454 [14] Section 8.2 for further explanation).  

The RA staff member will validate the request for the issuance of a "wildcard" TLS Certificate by checking whether the wildcard asterisk ("\*") is in the first position from the left in the CN or SAN item, and whether it is immediately followed by a dot ("."). At the same time, he will check whether the "wildcard" TLS Certificate is issued for a third-level domain and higher, where the first level can only be the national domain level ".sk", i.e. an acceptable request must have the form of a "wildcard" domain name for the third level "*.domainname.sk". Verification of domain authorization will be performed in accordance with Section 3.2.2.4.  

#### 3.2.2.7 Data Source Accuracy  

Before using any data source as a trusted source, the Provider shall verify the reliability, accuracy, resistance to change or counterfeiting of such resource. It may consider, for example, the timeliness of the data, the frequency of updating the data source, the data provider, and the public availability, the low probability of the possibility of changing or falsifying the data.  

#### 3.2.2.8 CAA Records  
As part of the issuance process, the Provider shall check the CAA record for each dNSName specified in the subjectAltName extension of the issued TLS Certificate in accordance with the procedure in RFC 8659 and the processing instructions provided in RFC 8659[13] for all records found.  

Some methods relied upon validating the Applicant's ownership or control of the subject domain(s) (see Section 3.2.2.4) to be listed in a TLS Certificate require CAA records to be retrieved and processed from additional remote Network Perspectives before Certificate issuance (see Section 3.2.2.9). To corroborate the Primary Network Perspective, a remote Network Perspective's CAA check response shall be interpreted as permission to issue, regardless of whether the responses from both Perspectives byte-for-byte are identical. Additionally, a CA may consider the response from a remote Network Perspective as corroborating if one or both of the Perspectives experience an acceptable CAA record lookup failure, as defined in the Section 3.2.2.8 TLS BR. [3]  

If the Provider issues, they shall do so within the TTL of the CAA record, or 8 hours, whichever is greater.
The RA staff member must check the published CAA record before issuing a TLS Certificate. If he finds that such a record exists, he must not issue the TLS Certificate until it is confirmed that the TLS Certificate application is in accordance with the relevant set of records in the CAA.
The verification of the record is performed for each FQDN specified in the CN of the application or that which is to be specified in the SAN in such a way that the name tree is progressed from left to right, e.g. for checking the CAA record of an application that contains an FQDN in the form X.Y.X, the check is performed in the order X.Y.X -> Y.Z -> Z, unless Z is a national level, e.g. ".sk".  

A written record of the CAA record check is created, containing all checked FQDNs and the result of the check.  

#### 3.2.2.9 Multi-Perspective Issuance Corroboration  
Multi-Perspective Issuance Corroboration attempts to corroborate the determinations (i.e., domain validation pass/fail, CAA permission/prohibition) made by the Primary Network Perspective from multiple remote Network Perspectives before TLS Certificate issuance. This process can improve protection against equally-specific prefix Border Gateway Protocol (BGP) attacks or hijacks.  

The CA may use either the same set, or different sets of Network Perspectives when performing Multi-Perspective Issuance Corroboration for the required:    
* Domain Authorization or Control; and   
* CAA Record checks.   

The set of responses from the Network Perspectives relied upon shall provide the CA with the necessary information to allow it to affirmatively assess:  
**a)** the presence of the expected:
   * Random Value; 
   * Request Token; 
   * IP Address; or 
   * Contact Address;   

as required by the relied upon validation method specified in Sections 3.2.2.4 and

**b)** the Provider's authority to issue to the requested domain(s), as specified in Section 3.2.2.8.  

Section 3.2.2.4 describes the validation methods that require the use of Multi-Perspective Issuance Corroboration and how a Network Perspective can corroborate the outcomes determined by the Primary Network Perspective.  

Results or information obtained from one Network Perspective shall not be reused or cached when performing validation through subsequent Network Perspectives (e.g., different Network Perspectives cannot rely on a shared DNS cache to prevent an adversary with control of traffic from one Network Perspective from poisoning the DNS cache used by other Network Perspectives). The network infrastructure providing Internet connectivity to a Network Perspective may be administered by the same organization providing the computational services required to operate the Network Perspective. All communications between a remote Network Perspective and the Provider shall take place over an authenticated and encrypted channel relying on modern protocols (e.g., over HTTPS).  

A Network Perspective may use a recursive DNS resolver that is not co-located with the Network Perspective. However, the DNS resolver used by the Network Perspective shall fall within the same Regional Internet Registry service region as the Network Perspective relying upon it. Furthermore, for any pair of DNS resolvers used on a Multi-Perspective Issuance Corroboration attempt, the straight-line distance between the two States, Provinces, or Countries the DNS resolvers reside in shall be at least 500 km. The location of a DNS resolver is determined by the point where unencapsulated outbound DNS queries are typically first handed off to the network infrastructure providing Internet connectivity to that DNS resolver.  

Provider may immediately retry Multi-Perspective Issuance Corroboration using the same validation method or an alternative method (e.g., the Provider can immediately retry validation using "Email to DNS TXT Contact" if "Agreed-Upon Change to Website - ACME" does not corroborate the outcome of Multi-Perspective Issuance Corroboration). When retrying Multi-Perspective Issuance Corroboration, Provider shall not rely on corroborations from previous attempts. There is no stipulation regarding the maximum number of validations attempts that may be performed in any period of time.

The "Quorum Requirements" Table describes quorum requirements related to Multi-Perspective Issuance Corroboration. If the Provider does not rely on the same set of Network Perspectives for both Domain Authorization or Control and CAA Record checks, the quorum requirements shall be met for both sets of Network Perspectives (i.e., the Domain Authorization or Control set and the CAA record check set). Network Perspectives are considered distinct when the straight-line distance between the two States, Provinces, or Countries they reside in is at least 500 km. Network Perspectives are considered "remote" when they are distinct from the Primary Network Perspective and the other Network Perspectives represented in a quorum.  

Provider may reuse corroborating evidence for CAA record quorum compliance for a maximum of 398 days. After issuing a Certificate to a domain, remote Network Perspectives may omit retrieving and processing CAA records for the same domain or its subdomains in subsequent Certificate requests from the same Applicant for up to a maximum of 398 days.  

Table 2: Quorum Requirements
|# of Distinct Remote<br> Network Perspectives Used|# of Allowed<br> non-Corroborations|
|:----------------------------------------------:|:-------------------------------:|
|2-5|1|
|6+|2|  

Effective March 15, 2025, the Provider shall implement Multi-Perspective Issuance Corroboration using at least two (2) remote Network Perspectives. The Provider may proceed with TLS Certificate issuance if the number of remote Network Perspectives that do not corroborate the determinations made by the Primary Network Perspective ("non-corroborations") is greater than allowed in the Quorum Requirements Table 2.  

Effective September 15, 2025, the Provider shall implement Multi-Perspective Issuance Corroboration using at least two (2) remote Network Perspectives. The Provider shall not proceed with TLS Certificate issuance if the number of non-corroborations is greater than allowed in the Quorum Requirements Table 2  

Effective March 15, 2026, the Provider shall implement Multi-Perspective Issuance Corroboration using at least three (3) remote Network Perspectives. The Provider shall not proceed with TLS Certificate issuance if the number of non-corroborations is greater than allowed in the Quorum Requirements  

Table 2 and if the remote Network Perspectives that do corroborate the determinations made by the Primary Network Perspective do not fall within the service regions of at least two (2) distinct Regional Internet Registries.  

Effective June 15, 2026, the Provider shall implement Multi-Perspective Issuance Corroboration using at least four (4) remote Network Perspectives. The Provider shall not proceed with TYLS Certificate issuance if the number of non-corroborations is greater than allowed in the Quorum Requirements   Table 2 and if the remote Network Perspectives that do corroborate the determinations made by the Primary Network Perspective do not fall within the service regions of at least two (2) distinct Regional Internet Registries. 

Effective December 15, 2026, the Provider shall implement Multi-Perspective Issuance Corroboration using at least five (5) remote Network Perspectives. The Provider shall not proceed with TLS Certificate issuance if the number of non-corroborations is greater than allowed in the Quorum Requirements Table 2 and if the remote Network Perspectives that do corroborate the determinations made by the Primary Network Perspective do not fall within the service regions of at least two (2) distinct Regional Internet Registries.

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

### 4.1.1 Who can submit a TLS Certificate application  
A TLS Certificate may be requested by a natural or legal person operating a device or system, who demonstrates in the TLS Certificate request that they are eligible to request a TLS Certificate with an FQDN and that all FQDNs which are listed in the SAN of TLS Certificate.
The Provider shall maintain an internal database of all revoked TLS Certificates and rejected requests due to suspicion of phishing or other fraudulent activity.  

### 4.1.2 Enrollment process and responsibilities  

#### 4.1.2.1 Preparation  
The Contractor/Subscriber shall take the following steps to prepare for a visit to the Provider:    
* Familiarize yourself with the "Všeobecné podmienky poskytovania a používania dôveryhodnej služby vydávania a overovania certifikátov (General Terms and Conditions for Providing and Using a Trusted Certificate Issuance and Verification Service)" [12] and "Informáciou o spracúvaní osobných údajov (Information on Personal Data Processing)" [18], which shall be accessible in a durable communication channel (see [https//eidas.disig.sk/sk/documents/](https//eidas.disig.sk/sk/documents/));  
* To get acquainted with this procedure, possibly with the principles and instructions for obtaining the TLS Certificate;  
* To have ready the values of each TLS Certificate request field so that these values are consistent with this CP/CPS (see paragraph 3.1.4); 
* To have prepared a TLS Certificate request in form of PKCS #10 or SPKAC, which will be sent in advance to the Provider (see paragraph 4.1.4);  
* To have prepared the selected identity documents and other necessary documents, i.e., Extract from business register, Power of Attorney, etc.;
* To arrange a date for the visit.  

#### 4.1.2.2 Request generation  
When requesting a TLS Certificate, the Subscriber shall generate a cryptographic key pair (private and public) using their software (typically Microsoft IIS or Apache / OpenSSL, for example) and shall create a new TLS Certificate request and save it on suitable medium. 
The Provider issues TLS Certificates exclusively at the company's headquarters in Bratislava. 

Notes and warnings: Please note that the request for a TLS Certificate or the public key in it, for which a TLS Certificate has already been issued, cannot be used repeatedly to issue another TLSA Certificate for security reasons and will be rejected at the RA! The request for a TLS Certificate shall include the <subject:commonName> (the so-called entity name) item, filled in appropriately. The individual items shall be filled in so that the entered values are in accordance with this document, with an emphasis on its Section 3.1.2, and to clearly identify the entity that will use the given TLS Certificate (typically the fully qualified domain name (FQDN)). If item O (subject:organizationName) is filled in the application, item L (subject:localityName) shall also be filled in. It is also necessary to maintain the order of items in the application as stated in Section 3.1.4.2 Table 1.  

#### 4.1.2.3 Sending a TLS Certificate request  
The request for the issuance of a TLS Certificate is sent by the Applicant/Subscriber to the RA address ([radisig@disig.sk](radisig@disig.sk)) which shall perform all actions related to the TLS Certificate issuance process.

## 4.2 Certificate application processing  

### 4.2.1 Performing identification and authentication functions  
Before issuing the TLS Certificate, the employee representing the Provider shall  
* Inform the attender natural person about the General Terms and Conditions [12];  
* Check the completeness and accuracy of the data in the accepted TLS Certificate request.    
* Verify the identity of the Subscriber and insert his/her personal data into the IS of the Provider, obliging him to fill in all required items required by the Provider's system.    
* Verify other documents to verify any identifying information to be entered into the TLS Certificate.  

RA staff member shall verify the identity and authenticity of the Subscriber within the meaning of the Section 3.2.    
The Subscribers shall show to the RA in a satisfactory manner all the data he / she has entered into each item of the TLS Certificate request.  
RA staff member shall insert a TLS Certificate request and other required data into the Provider's information system.  
### 4.2.2 Approval or rejection of TLS Certificate applications  
In the event of any reasonable doubt as to the identity of the Subscriber, also in case of deficiencies in the documents, providing incomplete documents, the RA staff member shall refuse the Subscriber's registration.
The application shall also be rejected if its format or Content does not meet the requirements set out in Section 3.1.4.  

The Provider may not issue Certificates for FQDN that contains the highest domain (gTLD) that is not listed and in the "Root Zone Database" maintained by the Internet Assigned Numbers Authority (IANA) ([https://www.iana.org/domains/root/db](https://www.iana.org/domains/root/db)).
Any request meeting the requirements of this CP/CPS shall be processed without delay if the issue is made in the presence of the Subscriber or at the latest at the time agreed with the Subscriber in the TLS Certificate application process.  

The Provider shall not issue TLS Certificates containing internal names or reserved IP addresses.
The Provider may not issue a TLS Certificate on a request containing a domain name if, when verifying the CAA DNS record pursuant to Section 3.2.2.8, it is determined that such a record exists and does not authorize the Provider as authorized to issue TLS Certificates.
However, if the "issue" and/or "issuewild" record contains an authorization in the form of "disig.sk", the Provider is authorized to issue the relevant TLS Certificate based on the submitted request.  

The results of the CAA record check shall be recorded and stored by the Provider.

### 4.2.3 Time to process TLS Certificate issuance  
No stipulation. 

## 4.3 Certificate issuance  

### 4.3.1 CA actions during TLS Certificate issuance  
After sending the TLS Certificate request from the RA to the CA, the CA system shall verify the received request in order to verify if  
* It was sent by authorized RA staff member;  
* Corresponds to the standard for PKCS # 10 or SPKAC, respectively;  
* No TLS Certificate has been issued in the past to the public key found in the submitted TLS Certificate request.  

If all TLS Certificate requirements are met, CA shall issue the TLS Certificate.  

Before issuing the TLS Certificate that will be provided to the end user, the CA system shall ensure that the corresponding preliminary TLS Certificate is sent to the default CT log servers in order to obtain the CT log record, which will then be included in the TLS Certificate. At the same time, the system shall perform an automated check of the issued preliminary TLS Certificate and the TLS Certificate using the "zlint" and "ctlint" application, whether their parameters correspond to the requirements specified in [3], [4], [5], [6] and [7].  

Certificate issuance by Root CA requires an individual authorized by the Provider (i.e., the CA system operator, system officer, or PKI administrator) to deliberately issue a direct command in order for the Root to perform a TLS Certificate signing operation.  

### 4.3.2 Notification to subscriber by the CA of issuance of TLS Certificate  
The issuing RA staff member informs the Subscriber/Holder about the issuance of the TLS Certificate by sending an email message to the email address specified in the Certificate Holder's personal data.

## 4.4 Certificate acceptance  

### 4.4.1 Conduct constituting TLS Certificate acceptance  
TLS Certificates will be created and issued in the Provider system automated and on a continuous basis. The holder will be able to take the issued TLS Certificate immediately after its issuing.  
After the TLS Certificate is issued, the RA staff member and the Subscriber shall sign the relevant documentation related to the issuance of the TLS Certificate.  

The TLS Certificate is available for download via the Provider's repository at:
[https://eidas.disig.sk/sk/poskytovatel/certifikacna-autorita/vyhladavanie-certifikatov/](https://eidas.disig.sk/sk/poskytovatel/certifikacna-autorita/vyhladavanie-certifikatov/)
or is provided to him via email or by submitting it on a portable medium.  
### 4.4.2 Publication of the TLS Certificate by the CA  
Each TLS Certificate issued is published in the Provider's repository immediately after issuance unless its non-disclosure has been agreed with the Subscriber/Holder.
### 4.4.3 Notification of TLS Certificate issuance by the CA to other entities  
The preliminary TLS Certificate is automatically sent to the default CT log servers in order to obtain the CT log record, which will then be included in the resulting TLS Certificate. 
## 4.5 Key pair and TLS Certificate usage  
This Section describes responsibilities for using keys and TLS Certificates.
### 4.5.1 Subscriber private key and TLS Certificate usage   
The Subscriber in relation to the private key and TLS Certificate shall:
* Provide the Provider with the exact and complete information required by this CP/CPS when applying for a TLS Certificate;  
* Use a key pair in accordance with the limitations that have been notified by the Provider;  
* Continually protect his/her private keys in accordance with this CP/CPS, and in accordance with the provisions of the General Conditions [12];  
* Use a private key only after obtaining a public key TLS Certificate with which they create unique pairs;  
* Immediately notify the Provider, if the TLS Certificate has not yet been expired, of suspecting that his/her private key was lost, stolen, or compromised;  
* Immediately request the TLS Certificate to be revoked in the event that any information on the entity's TLS Certificate becomes invalid;  
* Comply with any terms, conditions and limitations imposed on your private key and TLS Certificate i.e., to stop use of a private key after an expiration or revocation of a public key TLS Certificate.  

The Subscriber who will fail to comply with his obligations is not entitled to compensation for any damage.  
### 4.5.2 Relying party public key and TLS Certificate usage  
The relying party that relies on the TLS Certificate issued under this CP/CPS and in accordance with the General Terms and Conditions [12] shall:  
* Assess whether the use of the TLS Certificate is in accordance with its purpose and is appropriate for a particular purpose;  
* Check that the use of the TLS Certificate is consistent with the restrictions of the TLS Certificate, which are contained in the TLS Certificate itself, the General Terms and Conditions [12], or this CP/CPS;  
* When working with the TLS Certificate, including its validation, use only the intended and appropriate hardware or software;  
* Verify the validity of the TLS Certificate in question by checking that  
* The TLS Certificate was valid at the time the relying party had confidence that the signature / seal had been created.  
* Before the time stated in the previous point, the TLS Certificate was not revoked via checking current CRL and, if applicable, via the OCSP provided by the Provider - reference to the address of the CRL and, optionally, to the OCSP service is mentioned in TLS Certificate.   
* Make any further verifications that may be required in the context of this CP/CPS or standards for a particular type of TLS Certificate or its use and verify the other TLS Certificates in the certification path as described in the previous way e.g., "trust anchor".

## 4.6 Certificate renewal  

### 4.6.1 Circumstance for TLS Certificate renewal  
The Provider will not allow the TLS Certificate to be renewed (issued) to a public key to which TLS Certificate has already been issued by the same CA of the Provider.   

### 4.6.2 Who may request renewal  
No stipulation.

### 4.6.3 Processing TLS Certificate renewal requests  
No stipulation.

### 4.6.4 Notification of new TLS Certificate issuance to subscriber  
No stipulation.

### 4.6.5 Conduct constituting acceptance of a renewal TLS Certificate  
No stipulation.

### 4.6.6 Publication of the renewal TLS Certificate by the CA  
No stipulation.

### 4.6.7 Notification of TLS Certificate issuance by the CA to other entities  
No stipulation.

## 4.7 Certificate re-key  
No stipulation.
### 4.7.1 Circumstance for TLS Certificate re-key  
No stipulation.

### 4.7.2 Who may request certification of a new public key  
No stipulation.

### 4.7.3 Processing TLS Certificate re-keying requests  
No stipulation. 

### 4.7.4 Notification of new TLS Certificate issuance to subscriber  
No stipulation.

### 4.7.5 Conduct constituting acceptance of a re-keyed TLS Certificate  
No stipulation.

### 4.7.6 Publication of the re-keyed TLS Certificate by the CA  
See Section 4.4.2.

### 4.7.7 Notification of TLS Certificate issuance by the CA to other entities  
No stipulation.

## 4.8 Certificate modification  

### 4.8.1 Circumstance for TLS Certificate modification   
No stipulation.

### 4.8.2 Who may request TLS Certificate modification  
No stipulation.

### 4.8.3 Processing TLS Certificate modification requests   
No stipulation.

### 4.8.4 Notification of new TLS Certificate issuance to subscriber  
No stipulation.

### 4.8.5 Conduct constituting acceptance of modified TLS Certificate  
No stipulation.

### 4.8.6 Publication of the modified TLS Certificate by the CA  
No stipulation.

### 4.8.7 Notification of TLS Certificate issuance by the CA to other entities  
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
Certificate revocation may also be requested
* Provider - the RA staff member shall document this fact in writing, including the reason for his/her proceedings,
* the court, by means of its judgment or interim measure (a copy of the relevant court decision shall be attached to the TLS Certificate revocation documents).  
Additionally, Subscribers, relying parties, application software suppliers, and other third parties may submit Certificate Problem Reports informing the Provider of reasonable cause to revoke the TLS Certificate.  

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

### 4.9.4 Revocation request grace period  
No stipulation.

### 4.9.5 Time within which CA shall process the revocation request  
Provider shall  
* Within 24 hours after receiving a Certificate Problem Report, the Provider shall investigate the facts and circumstances related to a Certificate Problem Report and provide a preliminary report on its findings to both the Subscriber and the entity who filed the Certificate Problem Report;  
* After reviewing the facts and circumstances, the Provider shall collaborate with the Subscriber/Holder and any entity reporting the Certificate Problem Report or other revocation-related notice to establish whether or not the TLS Certificate will be revoked, and if so, a date on which the Provider will revoke the TLS Certificate;  
* The period from receipt of the Certificate Problem Report or revocation-related notice to published revocation shall not exceed the time frame set forth in Section 4.9.1.1;  
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

Due to the fact that Mozilla does not grant exemptions from TLS Certificate revocation requirements under this CP/CPS, Provider shall:  
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
The Provider shall operate and maintain its CRL and optional OCSP capability with resources sufficient to provide a response time of ten seconds or less under normal operating conditions.
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
The Provider's basic infrastructure is located in protected areas that are accessible only to authorized persons and are separated from other areas by appropriate security features (security doors, bars, solid walls, etc.). The Provider's equipment consists only of equipment reserved for the provision of trusted services and does not serve any purposes unrelated to these services.  

### 5.1.2 Physical access  
Access Control Mechanisms for Provider's Protected Areas e. g. the areas of the highest security zone shall be secured in such a way that these spaces are protected by a security alarm and are only accessible to persons holding a security token and listed in the list of authorized persons to enter the Provider's protected areas. Provider equipment shall be permanently protected from unauthorized access, even from unauthorized physical access.  
The access control mechanisms to the Provider's protected areas, i.e. to the areas of the highest security zone, are ensured in such a way that the areas are protected by a security alarm and entry is allowed only to persons who own a security token and are listed on the list of persons authorized to enter the Provider's protected areas. The Provider's equipment is constantly protected from unauthorized access, including unauthorized physical access.  

### 5.1.3 Power and air conditioning  
The spaces in which the Provider's equipment is located shall be adequately supplied with electricity and air-conditioned to provide a reliable operating environment.  

### 5.1.4 Water exposures  
The spaces in which the Provider's equipment is located shall be located so that they cannot be endangered by water from any source. If this is not entirely possible, measures shall be taken to minimize the risk of water hazard on the premises.  
The premises on which the Provider's equipment is located are located in such a way that the risk of water from any sources is unlikely.  

### 5.1.5 Fire prevention and protection  
The spaces in which the Provider's equipment is located shall be reliably protected from direct fire sources, heat that could cause fire in the premises.  

### 5.1.6 Media storage  
Media shall be stored in rooms that are protected against accidental, unintentional damage (water, fire, and electromagnetism). Media containing security audits, archives, or backed up information should be stored on a site separate from CMA.  
Media is stored on a location that is protected from accidental, unintentional damage (water, fire, electromagnetic). Media containing information related to security audits, archives, or backup information is stored in a location separate from CMA equipment.

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

### 5.3.2 Background check procedures  
An employee can only be included in the trusted role of the Provider if he/she has a security clearance of the specified level i.e., at least to the "Confidential" classification level or is in the process of requesting such a review, respectively.
Security clearance is not required for the RA staff member role.   

### 5.3.3 Training Requirements and Procedures  
Some special training requirements may be specified for certain trustworthy roles of the Provider, which should be completed before or during the assignment. Topics should include the functioning of CMA software and hardware, operating and security procedures, the provisions of this CP/CPS, and so on.  
Each RA staff member must undergo mandatory training, conducted by authorized personnel of the Provider, before starting to perform their function.   

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
* Identity of the person making the journal record; and
* Description of the event;  

All events related to operations performed in the RA Client application are recorded directly by the application. Likewise, all information sent from the RA Client application is recorded on the server side of the Service Provider.  

Events related to the life cycle of TLS Certificates for end users in the scope of:
* request for issuance of a TLS Certificate;  
* approval of the issuance request;  
* issuance of a TLS Certificate;  
* revocation of a TLS Certificate;  
are recorded in the SWACA database;  

### 5.4.2 Frequency for Processing and Archiving Audit Logs  
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

### 5.4.6  Audit Log Accumulation System  
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
The records are kept in paper form or in electronic form. The records kept also include all documents that the Subscriber / Holder must submit in order for the TLS Certificate (e.g. extract from the commercial register, power of attorney, etc.).  

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

### 5.5.6 Archive collection system  
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
The Provider must have a solution to cover all the costs associated with meeting the minimum termination requirements in the event of bankruptcy or any other cause when it will be unable to cover the costs by its own means, in accordance with applicable bankruptcy legislation.

# 6. Technical Security Controls   
The technical part of the Provider's infrastructure (hardware and software) shall consist only of secure systems and official software. The infrastructure architecture of the Provider shall be designed with components that meet safety standards at the level of current knowledge.  

Particular attention shall be paid to the cryptographic module (HSM), which serves to generate, store, and use the Provider's private keys and is one of the most vulnerable assets. The private keys of the Provider shall be stored in an HSM module that is certified at least according to the FIPS 140-2 Level 3 standard. 

The Provider shall use a combination of physical, logical, and procedural measures to ensure its security to protect its private key. These measures shall be described, for example, in the published CP/CPS.  
The Provider's system shall contain a device for the continuous detection, monitoring, and signaling of unauthorized and unusual attempts to access its resources.  
Publishing applications shall provide access control before trying to add or delete a TLS Certificate or modify other associated data.  

Revocation status reporting shall provide access control before attempts to modify revocation status information.  
All Provider features that use a computer network shall be secured against unauthorized access and other malicious activities.  

## 6.1 Key pair generation and installation  

### 6.1.1 Key pair generation  

#### 6.1.1.1 Certificate issuer
Generating and installing a Provider's key pair shall be done in a standardized way detailed in the Provider's documentation in accordance with the requirements in Section 6.1.1.1 of TLS BR [3].   
The key pair generating shall provide sufficient confidence in the process and the entire process shall be recorded in writing. Authorized staff in trusted roles who are eligible to participate in the key generation and request generation process shall ensure key generation. Key generation shall be done in a secure cryptographic module.  
The Provider CA key pairs are generated in a formal "key ceremony" that:
* takes place in a secure environment that meets the physical security requirements of Section 5.1;  
* uses hardware security modules (HSMs) that meet the requirements of [FIPS 140-2 Level 3 or higher / EN 419 221-5 or equivalent];  
* involves the necessary number of individuals in trusted roles acting according to the K/N principle;  
* is documented in detail, including participants, devices, date and time, and resulting key and TLS Certificate fingerprints;  
* the key ceremony is performed according to a written procedure approved by senior management.  

#### 6.1.1.2 End-user key pair generation  
Key pair generation is performed by the user (applicant) himself, using appropriate software or hardware that meets the minimum requirements for key length and required algorithms.  
The Provider shall reject a TLS Certificate request if one or more of the following conditions are met:  

**1.** The Key Pair does not meet the requirements set forth in Section 6.1.5 and/or Section 6.1.6;  
**2.** There is clear evidence that the specific method used to generate Private Key was flawed;  
**3.** The Provider is aware of a demonstrated or proven method that exposes the Applicant's private Key to compromise;  
**4.** The Provider has previously been made aware that the Applicant's private key has suffered a key compromise, such as through the provisions of Section 4.9.1.1;  
**5.** The Provider is aware of a demonstrated or proven method to easily compute the Applicant's Private Key based on the Public Key (such as a Debian weak key, see [https://wiki.debian.org/SSLkeys](https://wiki.debian.org/SSLkeys)).  

### 6.1.2 Private key delivery to subscriber   
Parties other than the Subscriber shall not archive the Subscriber private key without authorization by the Subscriber.  
If the Provider becomes aware that a Subscriber's private key has been communicated to an unauthorized person or an organization not affiliated with the Subscriber, then the Provider shall revoke all TLS Certificates that include the public key corresponding to the communicated private key. 

### 6.1.3 Public key delivery to TLS Certificate issuer  
The public key is delivered to the certification authority securely via the RA Client application in online mode during the TLS Certificate issuance process. Communication between the RA Client application and the issuing CA is authorized by signing all sent data by an RA staff member, where the issuance authorization of the given RA staff member is checked on the CA side in automatic mode.  

### 6.1.4 CA public key delivery to relying parties  
No stipulation.  

### 6.1.5 Key sizes   
For RSA key pairs the Provider shall ensure that the modulus size:
* when encoded, is at least 2048 bits;   
* in bits, is evenly divisible by 8.  

### 6.1.6 Public key parameters generation and quality checking   
The parameters and quality of the Provider's public key (root, subordinate CA, cross-certified CA) are determined by the PMA and quality control is checked during the key generation ceremony.

The Provider shall use cryptographic hardware modules that meet the requirements of FIPS 186-2 to generate and store keys, which ensure the random generation of RSA keys with a size of at least 2048 bits.

RSA: The Provider shall confirm that the value of the public exponent is an odd number equal to 3 or more. Additionally, the public exponent should be in the range between 2^16+1 and 2^256-1.  

The modulus should also have the following characteristics: an odd number, not the power of a prime, and have no factors smaller than 752. [Source: Section 5.3.3, NIST SP 800-89] .   

### 6.1.7 Key usage purposes  
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

### 6.2.11 Cryptographic Module Capabilities  
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
|TLS Certificate|-|395 days to 14.3.2026<br> 200 days from 15.3.2026 to 14.3.2027<br> 100 days from 15.3.2027 to 14.3.2029<br> 47 days from 15.3.2029|

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
No stipulation.  

### 6.6.2 Security management controls  
No stipulation.  

### 6.6.3 Life cycle security controls  
No stipulation.  

## 6.7 Network security controls  
The provider will ensure the implementation of the requirements of the document "Network and Certificate System Security Requirements" [22]  

## 6.8 Time-stamping  
No stipulation.  

# 7. Certificate, CRL, and OCSP profiles  
TLS Certificate profiles and Certificate Revocation Lists are set centrally - RA staff member cannot change the structure of TLS Certificates.  

## 7.1 Certificate profile  

### 7.1.1 Version number  
This CP/CPS only allows issuing TLS Certificates conforming to X.509 version 3.  

### 7.1.2 Certificate Content and Extensions  

#### 7.1.2.1 Provider's Root CA Certificates
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
The certificate must be technically constrained to the serverAuth Extended Key Usage (EKU). 

The keyUsage extension must be marked as critical with keyCertSign and cRLSign bits set.   
The signature algorithm must be SHA-256 or stronger. The public key must be an RSA key with a minimum length of 4096 bits. 
The certificatePolicies extension must contain the OV policy identifier (2.23.140.1.2.2) to signal compliance with the TLS Baseline Requirements for Organization Validation.

Algorithms and key lengths applied in the Cross-Certified Subordinate CA:   
|  | |
| :--- | :--- |
| Signature AlgorithmName:|**sha256RSA**|
| Public key:|**RSA, length 4 096 bit **|

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
|authorityKeyIdentifier / 2.5.29.35|YES|NO|
|basicConstraints / 2.5.29.19|YES|YES|
|certificatePolicies / 2.5.29.32|YES|NO|
|keyUsage / 2.5.29.15|YES|YES|
|subjectKeyIdentifier / 2.5.29.14|YES|NO|
|crlDistributionPoints / 2.5.29.31|YES|NO|
|extKeyUsage /  2.5.29.37|YES|NO|
|authorityInfoAccess / 1.3.6.1.5.5.7.1.1|YES|NO|  

*#### 7.1.2.3 Technically Constrained Non-TLS Subordinate CA Certificate Profile  
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
| Public key:|**RSA, length 2 048 bit **|
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
|Key Usage|{id-ce-keyUsage}<br>{2.5.29.15}<br>This extension indicates the purpose for which the certified public key is used.|YES|NO|
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

##### 7.1.2.7.11 Subscriber Certificate Key Usage  
The "Key Usage" entry in the end-user TLS Certificate shall comply with the requirements given in Section 7.1.2.7.11 of the TLS BR [3].  

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

#### 7.1.2.9 TLS Precertificate profile  
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
*300d06092a864886f70d0101010500*

##### 7.1.3.1.2 ECDSA  
No stipulation.  

#### 7.1.3.2 Signature AlgorithmIdentifier  
All objects signed with the CA Provider's private key shall meet the requirements for using "AlgorithmIdentifier" or a type derived from "AlgorithmIdentifier" in the context of signatures if specified in Section 7.1.3.2 of TLS BR [3].   

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
The TLS Certificate policy OID 2.23.140.1.2.2 is reserved for the "Organization validated" TLS Certificate type - see 1.4.1 of this CP/CPS.  

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
During the period in which the CA issues TLS Certificates, the Provider shall monitor compliance with its CP/CPS and the requirements specified in TLS BR [3] and control the services provided by conducting internal audits at least on a quarterly basis on a randomly selected sample of issued TLS Certificates in a number higher than one and at most in the number of three percent of the issued TLS Certificates in the period since the previous internal audit.  

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
* private keys belonging to the executive components of the Provider (RA staff);  
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

### 9.6.1 CA representations and warranties  
Regarding Trusted Services, the Provider does not provide any representations or warranties except as provided in this CP/CPS and the General terms and conditions [12].  

### 9.6.2 RA representations and warranties  
All external Entity registration authorities shall provide trusted services based on a contractual relationship with the Provider and in accordance with this CP/CPS.  

### 9.6.3 Subscriber representations and warranties  
Subscriber or Certificate Holder uses the trusted services of the Provider on his own responsibility and carries all the costs of remote means of communication or other technical means necessary for the use of these services (e.g., the software needed for making the electronic signature / seal, software for the authentication of the website etc.).  

### 9.6.4 Relying party representations and warranties  
The Relying party shall note that they are solely free to decide whether to trust and rely on the TLS Certificate issued by the Provider and hence on the information contained therein. The Relying party is required to comply with the obligations described in Section 10 of the General terms and conditions [12],   in the case of a decision to trust the Provider's TLS Certificates; otherwise, it is solely responsible for the legal consequences thereby caused.  

### 9.6.5 Representations and warranties of other participants  
No stipulation.  

## 9.7 Disclaimers of warranties  
The Provider is solely responsible for damages caused by failure to comply with obligations according to Article 13 of eIDAS Regulations [8] and failure to fulfill obligations in accordance with this CP/CPS.   

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
Any person who violates his or her obligation or any obligation under this CP/CPS, The Agreement, and the General Terms shall be liable to compensate for damage caused to the other party, except in cases where the liability of the entity is excluded for damages. The damage shall be deemed actual damage, loss of earnings and costs incurred by the injured party in respect of the damage event.  
Whoever violates his or her obligation or any obligation under this CP/CPS, The Contract, and the General Terms, may be relieved of liability for damages only if it proves that a breach of duty or any obligation has occurred as a result of circumstances excluding responsibility e.g., Force Majeure.  

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
Internal employees (RA staff member) issuing TLS Certificates must be fully informed about the new version of this CP/CPS.   

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

### 9.16.3 Severability  
If any provision of this CP/CPS is or becomes invalid or unenforceable, this shall not render the entire CP/CPS invalid or unenforceable if it is completely severable from the other provisions of this CP/CPS. The Provider shall immediately replace the invalid or unenforceable provision of the CP/CPS with a new valid and enforceable provision, the subject matter of which shall correspond as closely as possible to the subject matter of the original provision and at the same time the purpose of this CP/CPS and the content of the individual provisions of this CP/CPS shall be preserved.  

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




	





