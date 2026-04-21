# Disig S/MIME Certificate Policy and Certification Practice Statement (CP/CPS)
 
 
**Disig, a.s.**  
**Version 2.1**  
**Valid from April 21, 2026**  
**OID 1.3.158.35975946.0.0.0.1.11**

Copyright © 2026 Disig, a.s. 
This work is licensed under the [CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0/) license.

This document has not been proofread.
Trademarks: Product names mentioned herein may be trademarks of the firms.
   
 
# 1. Introduction

This document is a combined Certificate Policy and Certification Practice Statement (CP/CPS) of the company Disig, a.s., with its registered office at Galvaniho 17/C, 821 04 Bratislava - mestská časť Ružinov, National Trade Register number: 35975946, registered in the Business Register of the Municipal Court Bratislava III Section: Sa Insert No.: 3749/B, as a Trusted Service Provider (hereinafter referred to as "Provider") and applies to the root certification authorities and their subordinate certification authorities listed in Section 1.4.1 operated by the Provider, through which it provides trusted services for issuing publicly trusted S/MIME Certificates (hereinafter referred to as the "Certificate").  
It defines:  
Certificate Policy (CP) - the policies and rules under which Certificates are issued, managed, and used, and  
Certification Practice Statement (CPS) - the detailed procedures and practices that the Provider implements.

The Certificate issued for the end user (hereinafter referred to as the "Subscriber" or "Holder" or "Subscriber/Holder") uniquely identifies the entity to which the certificate is issued and binds this entity to the corresponding pair of keys. Unless it is explicitly stated in this CP/CPS that it refers to the certificate of the root certification authority or subordinate certification authority, then the word "Certificate" means the S/MIME certificate of the end entity.

The Provider's website for the provided trusted services is available here:
[https://eidas.disig.sk](https://eidas.disig.sk)
 
## 1.1 Overview
 
This CP/CPS defines the creation and management of public key certificates (X.509 version 3), in accordance with the Baseline Requirements for the Issuance and Management of Publicly-Trusted S/MIME Certificates [1] (hereinafter referred to as "SMIME BR").   
It also takes into account the requirements of RFC 5280 "Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile" [2], Regulation (EU) No. 910/2014 of 23 July 2014 on electronic identification and trustworthy services for electronic transactions in the internal market and repealing Directive 1999/93/EC as amended by Regulation No. 1183/2025 (hereinafter referred to as the "eIDAS Regulation") [3], and ETSI TS 119 411-6 "Electronic Signatures and Infrastructures (ESI); Policy and security requirements for Trust Service Providers issuing certificates; Part 6: Requirements for Trust Service Providers issuing publicly trusted S/MIME certificates [4]. Certificates are issued in accordance with requirements of the ETSI EN 319 401 [5]  and ETSI EN 319 411-1 [6] standards.

This CP/CPS is structured in accordance with RFC 3647 [7].
 
The Provider confirms that this CP/CPS takes account of all requirements of the current version of the SMIME BR [1], which is published at [https://cabforum.org/working-groups/smime/documents/](https://cabforum.org/working-groups/smime/documents/).

In the event of any inconsistency between these requirements and this CP/CPS, the requirements of the current version of the SMIME BR [1] prevail.
 
## 1.2 Document Name and Identification
 
|  | |
|:--- | :--- |
|Document Name:|**Disig S/MIME Certificate Policy and <br>Certification Practice Statement (CP/CPS)** |
|Skratka názvu: | **SMIME CP/CPS** |
|Version:|  **2.1** |
|Approved on:| **April 16, 2026**   |
|Valid from:| **April 21, 2026**    |  
|This document is assigned<br> to an object identifier (OID):|**1.3.158.35975946.0.0.0.1.11** |  
 
 
Description of the object identifier (OID):  
 1\.  - ISO assigned OIDs  
 1.3.  ISO Identified Organization  
 1.3.158.  -  Identification number (Company ID - ICO)    
 1.3.158.35975946. - Disig, a. s.  
 1.3.158.35975946.0.0.0.1.  - CA Disig  
 1.3.158.35975946.0.0.0.1.11 - CA Disig S/MIME CP/CPS  
 
This OID (1.3.158.35975946.0.0.0.1.11) is also listed in issued Certificates and covers these policies from standard [6]:
 
|Policy name|OID|Description/ETSI policy|  
|-----------|---|----------------------|
|LCP:  Lightweight Certificate Policy|0.4.0.2042.1.3|ETSI EN 319 411-1 LCP|
|OVCP:   Organizational Validation  Certificate Policy|0.4.0.2042.1.7|ETSI EN 319 411-1 OVCP|
|NCP:    Normalized Certificate Policy|0.4.0.2042.1.1|ETSI EN 319 411-1 NCP|  
 
###  1.2.1 Revisions
 
|Revision|Revision date|Description; Reviewer|  
|--------|-------------|---------------------|
|1.0|2023/09/01|First version; Miskovic|  
|1.1|2024/02/01|Addition of the possibility of online cancellation of the certificate (4.9.3); Miskovic|  
|1.2|2024/07/18|Change of headquarters of Disig, a.s.; Miskovic|  
|1.3|2024/09/16|Addition of part 4.2 in accordance with the requirements of part 2.2 of the current version of SMIME BR; Miskovic|  
|1.4|2025/03/15|Modification of sections 4.2.2 and 4.2.3 in accordance with the requirements of the current version of SMIME BR v. 1.0.8.|Miskovic|  
|2.0|2026/03/05|Transformation of the document into a new form of a combined policy for providing the service of issuing publicly trusted SMIME Certificates, which also includes the rules for providing this service, which were originally the subject of a separate document.; Miskovic|
|2.1|2026/04/21|Addition of information about the issued subordinate CA Disig R4I1 SMIME Certification Service (1.3.1.12); Miškovič|

##  1.3 PKI Participants

###  1.3.1 Certification Authorities
Root CA is the top-level Certification Authority whose Root certificate is distributed by Application Software Suppliers. Root CA issues Subordinate CA certificates.
Subordinate CA is a Certification Authority whose Certificate is signed by Root CA, or another Subordinate CA.
SMIME CP/CPS (herain after only "CP/CPS") relates to the provision of trust services by subordinate certification authorities that fall under one of the CA hierarchies operated by the Provider for issuing publicly trusted Certificates as described below.

####  1.3.1.1 Multi-purpose CA Hierarchy

This hierarchy includes root CA and issuing subordinate CA, which represents the legacy CA structure operated by the Provider since its acceptance as a publicly trusted Certificate provider under the corresponding root CA programs accepted by Microsoft, Mozilla, Google, and Apple.   
The hierarchy will be used to issue Certificates to end users only until it is replaced by a new single-purpose hierarchy (see 1.3.1.2).


| | |
|:--- |:--- |
|Name:                     |**CA Disig Root R2**|
|Certificate serial number:|**0092B888DBB08AC163**|
|Thumbprint (sha1) (DER):  |**B561EBEAA4DEE4254B691A98A55747C234C7D971**|
|Thumbprint (sha256) (DER):|**E23D4A036D7B70E9F595B1422079D2B91EDFBB1FB651A0633EAA8A9DC5F80703**|
|Comment:                  |**It issues Certificates only for subordinate certification authorities of the Provider.**|  


| | |
|:--- |:--- |
|Name:                       | **CA Disig R2I5 Certification Service**|
|Certificate serial number:  | **081B06DF4C7965509D000000000000000E**|
|Issuer:|**CA Disig Root R2**|
|Thumbprint (sha1) (DER):    | **8A189E4E6222B3B16D98EABE88687B39F82827A4**|
|Thumbprint (sha256) (DER):  | **90BA720B376FB9FDCF8A1037A5316FB493B5ACF656AD79C6839008BD43343FDD**|
|Comment:                    | **It issues SMIME signature/seal certificates to end users in accordance with the requirements set out <br> in the “Baseline Requirements for the Issuance and Management of Publicly‐Trusted S/MIME Certificates [1]**|


####  1.3.1.2 Single-purpose SMIME CA

This CA hierarchy replaces the legacy CA hierarchy (see 1.3.1.1) currently used to issue Certificates to end users. This single-purpose SMIME CA hierarchy is now fully compliant with the requirements of the current version SMIME BR [1], where new root CAs are required to have a separate CA hierarchy for issuing certificates to end users and are restricted to issuing certificates containing only the id-kp-emailProtection extension  (OID: 1.3.6.1.5.5.7.3.4) in the EKU.  


|  | |
| :--- | :--- |
| Name:                     | **CA Disig SMIME Root R4**|
| Certificate serial number:| **3F0CFAFD63A38C10294A0579F5457825**|
| Thumbprint (sha1)(DER):   | **33F3820A9838680BF90DA57815019E9FFDF31718**|
| Thumbprint (sha256)(DER): | **6AF177B41E97D40C9EA25203533E55C408632E9BD8A4809551001DFF2DC9479B**|
| Valid from:               | **September 18, 2025**|
| Valid to:                 | **septamber 14, 2043**| 
| Comment:                  | **It issues certificates only for the Provider's subordinate certification authorities reserved for issuing SMIME certificates.**|  

 
|  | |
| :--- | :--- |
| Name:                     | **CA Disig R4I1 SMIME Certification Service** |
| Issuer:                   | **CA Disig SMIME Root R4**|
| Certificate serial number:| **0AC7948B6549813D0E0000000000000001**|
| Thumbprint (sha1)(DER):   | **41253D3546812F46FAA7DC97933373E241134F61**|
| Thumbprint (sha256)(DER): | **855998FAB845C2C1CF0D6F62852C6B9A3C659DFDFA434D405C134C240E4534B5**|
| Valid from:               | **April 13, 2026**|
| Valid to:                 | **April 11, 2033**| 
| Comment:                  | **It only issues SMIME Certificates to end users (see 3.1.4.3).**| 

###  1.3.2	Registration Authorities

The Registration Authority ("RA") is an entity that under contract conducts certain selected activities in the provision of trusted services on behalf of the Provider.
The RA shall conduct its activities in accordance with this approved CP/CPS.
Provider may establish following types of RA:
* Commercial RA - is intended to mediate selected trustworthy services of the Provider to the general public and is operated by a third party, on the basis of a written agreement with the Provider see list at [https://eidas.disig.sk/sk/kontakt/registracne-autority/](https://eidas.disig.sk/sk/kontakt/registracne-autority/);
* Enterprise RA - is intended to mediate selected trustworthy services exclusively for the own needs of a particular legal body, For the needs of its operated systems requiring the use of certificates and is operated on the basis of a written contract with the Provider;
* Internal RA - is operated by the Provider and is intended to provide trusted services for all interested parties. This RA is not a separate legal body.
If the term "RA of the Provider" is used in the text, it refers to all types of RA mentioned above.

#### 1.3.2.1 Enterprise RA

The Provider can delegate to the Enterprise RA the verification of Certificate requests for natural persons within their own organization. The Provider will not accept requests for a Certificate authorized by an Enterprise RA unless the following requirements are met:
* If the Certificate Request is for an "Organization-validated" or "Sponsor-validated" profile, the Provider shall confirm that the Enterprise RA has authorization or control of the requested email domain(s) in accordance with Section 3.2.2.1 or Section 3.2.2.3. 
* The Provider shall confirm that the "_subject:organizationName_" name is either that of the delegated enterprise, or an Affiliate of the delegated enterprise, or that the delegated enterprise is an agent of the named Subject. The Provider shall impose these limitations as a contractual requirement on Enterprise RA and monitor compliance by the Enterprise RA in accordance with Section 8.8.

###  1.3.3	Subscribers 

Subscriber is understood to be a natural person or a legal person that is entitled to request for Certificate on behalf of an entity whose name appears as the subject in the Certificate - Certificate holder.
The Certificate Holder may be:
* **A natural person** - apply for Certificate;
* **A natural person** identified in **association with a legal person** - apply for Certificate;
* **A legal person** (that can be an Organization or a unit, or a department identified in association with an Organization) - apply for Certificate for seal.  

When a subscriber is the subject, it will be held solely responsible if its obligations are not correctly fulfilled.  
When the subscriber is acting on behalf of one or more distinct subjects to whom it is linked (e.g. the Subscriber is a company requiring Certificates for its employees to allow them to participate in electronic business on behalf of the company), responsibilities of the subscriber and of the subject are addressed in the General Terms of Service and Use of the Trusted Certificate Issuance and Verification Service " (the "General Terms") [8] published at the Provider's website (see Chapter 1).  

This CP/CPS defines the requirement that the Subscriber/Holder meet.
Formal Certificate Holder means a natural person who undertakes to use a corresponding private key and a Certificate in accordance with this CP/CPS.
The link between the subscriber and the subject is one of the following:  
* To request a Certificate the subscriber is:
   * The natural person itself;
   * A legal person mandated to represent the subject; or
   * Any entity with which the natural person is associated (such as the company employing the natural person or a non-profit legal person the natural person is member of).
* To request Certificate for seal the subscriber is:
   * Any entity as allowed under the relevant legal system to represent the legal person; or
   * A legal representative of a legal person subscribing to his subsidiaries, units, or departments.

###  1.3.4	Relying Parties 
Relying parties are a natural or legal person who relies, in their proceedings, on the electronic identification or trusted services of the Provider.

###  1.3.5	Other Participants 

#### 1.3.5.1 Policy Management Authority
Policy Management Authority - PMA is a component provided for the purpose:
* Supervising the CP/CPS creation and updating including the evaluation of plans to implement any of the changes.
* Reviewing CP/CPS to ensure that the Provider's practice complies with its requirements 
* Reviewing of audits findings, to determine whether Provider adequately comply with approved CP/CPS.
* Giving recommendations for Provider regarding corrective actions and other appropriate measures.
* Giving advice regarding the suitability of the Certificates associated with the CP/CPS for specific management applications and managing activities of the certification authority and registration authority.
* Interpretation of the CP/CPS and its instructions for RA and CA.
* Performing the internal audit of the Provider, by assigning this to an independent employee.
* Ensuring that the adopted and approved CP/CPS are implemented duly and properly implemented.

PMA represents the top component, which shall decide finally on all matters and aspects related to the Provider and its activities.

#### 1.3.5.2 Conformity assessors (auditors)
Conformity assessors are independent organizations that, based on accreditation, assess the Provider's compliance with:
* relevant standards (e.g. ETSI EN 319 401[5], ETSI EN 319 411-1[6], or other relevant standards),
* this CP/CPS and related internal policies of the Provider,
* requirements of the Trusted Root CA and/or CCADB programs.
Conformity assessors:
* have the right to request access to the necessary documents, records, and systems from the Provider to the extent necessary to conduct the audit;
* are bound by a confidentiality obligation to the extent agreed in the contract with the Provider and in accordance with the applicable law;
* do not provide any Certificate issuance services, key management, or CA/RA functions.  

The provider shall ensure that relations with conformity assessors are regulated by a written contract and that there is no conflict of interest.

####  1.3.5.3 Supervisory bodies and operators of trusted root programs
Supervisory bodies and operators of trusted root programs are entities that exercise statutory or programmatic supervision over the activities of the Provider, for example:
* a national supervisory authority for trust services or electronic identification;
* operators of trusted root CA programs (e.g. browser and OS manufacturers) who decide on the inclusion/removal of root CAs in the relevant program;
* administrators and operators of CCADB.
These entities:
* may request information, documents, and explanations from the Provider regarding the operation of the CA and compliance with requirements;
* may require the adoption of corrective measures, restrictions, or termination of Certificate issuance;
* are not a contracting party or relying party but may affect the trustworthiness of issued Certificates (e.g. by removing the root CA from the program).  

The Provider shall cooperate with these entities to the extent required by applicable law, applicable program rules, and these CP/CPS.

##  1.4	Certificate Usage 

###  1.4.1	Appropriate Certificate Uses 
Certificates issued under this CP/CPS are issued for purpose of identifying the public key holder from a cryptographic keys pair (public and private) which is used within the PKI infrastructure.
The cryptographic key pair (private and public) and the Certificate issued by the Provider can generally be used primarily for:
* E-mail security (signing and / or encryption of e-mails);
* Signing of electronic documents with advanced electronic signature;
* Creating an electronic seal.

CAs of the Provider issue following types of Certificates to the Subscribers: 
* S/MIME digital signature certificate or S/MIME digital certificate for seal - include public key associated with the email address and can also include the identity of natural person or legal person, which has control of the requested email address. The cryptographic keys associated with this type of Certificate are primarily intended for the security of electronic mail, the creation of an advanced electronic signature.   
The issued Certificate will include, in accordance with SMIME BR [1], the following certification policy identifiers: 
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) organization-validated(2) multipurpose (2)} (2.23.140.1.5.2.2); 
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) organization-validated (2) strict (3)} (2.23.140.1.5.2.3);
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) sponsor-validated (3) multipurpose (2)} (2.23.140.1.5.3.2); and
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) sponsor-validated (3) strict (3)} (2.23.140.1.5.3.3); and
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) individual-validated (4) multipurpose (2)} (2.23.140.1.5.4.2); and
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) individual-validated (4) strict (3)} (2.23.140.1.5.4.3).

The Provider issues management certificates for its needs (certificate for Subordinate CA, and certificate for OCSP Responders).

###  1.4.2	Prohibited Certificate Uses 
Certificates issued under this CP/CPS are not EU Qualified certificates according to the eIDAS Regulation [3] and cannot be used where EU Qualified certificates are required.
Certificates issued under this CP/CPS shall not be used for:
* securing TLS communications
* code signing;
* issuing additional certificates (non-CA certificates);
* any use that is not in accordance with the Key Usage and EKU extensions;
* any use that is unlawful, in violation of applicable law, or in violation of this CP/CPS or the trust service agreement.  

Relying Parties should not rely on Certificates for purposes other than unless such use is expressly permitted by the applicable certificate policy and clearly indicated in the Certificate extensions.

##  1.5	Policy administration 
###  1.5.1	Organization Administering the Document 
Table 1 contains the data of the Provider who is responsible for the preparation, creation, and maintenance of this document.  

Table 1: Contact details of the Provider
|  | |
| :--- | :--- |
| Company:|**Disig, a. s.** |
| Address: | **Galvaniho 17/C, 821 04 Bratislava, Slovakia** |
| Company ID:|  **359 75 946** |
| Phone:| **+421 2 20850140**   |
| e-mail:| **<disig@disig.sk>**    | 
| Web site:| **[https//www.disig.sk](https//www.disig.sk)**    |   

###  1.5.2	Contact Person 
For creating policies, the Provider has a PMA that is fully responsible for its content and is ready to answer any questions regarding the Provider's policies (see 1.3.5).
Table 2 contains the contact details of the person responsible for the operation of the Certification Authorities of the Provider.  

Table 2: Contact details of the Certification Authority
|  | |
| :--- | :--- |
| Certificate Authority:|**CA Disig** |
| Address: | **Galvaniho 17/C, 821 04 Bratislava, Slovakia** |
| Phone:| **+421 2 20850150, +421 2 20820157**   |
| e-mail:| **<caoperator@disig.sk>**    | 
| Web site:| **[https//eidas.disig.sk](https//eidas.disig.sk)**    |

###  1.5.3	Person Determining CP/CPS Suitability for the policy 
The person who is responsible for deciding on the compliance of the Provider's practices with this CP/CPS is the PMA (see 1.3.5).

###  1.5.4	CPS approval procedures 
Even prior to the start of operation, the Provider should have approved of its CP/CPS and shall meet all of its requirements.   
A person named by PMA approves the content of CP/CPS.  
Upon approval by the PMA, the relevant document is published in accordance with the publication and notification policy.  
The PMA has to inform its decisions in such a way that this information is well accessible to the Relying Parties.

This CP/CPS is approved by the person appointed to the PMA role.  
The CP/CPS is published in accordance with the publication and notification policy on the Provider's website (see section 1).

###  1.6	Definitions and Acronyms 

###  1.6.1	Definitions 
**Advanced electronic seal** means an electronic seal, which meets the requirements set out in Article 36 of eIDAS Regulation; [3];

**Advanced electronic signature** means an electronic signature, which meets the requirements set out in Article 26 of eIDAS Regulation; [3];  

**CA of the Provider** - certification authorities of the Provider that are used to issue Certificates;  

**Trust service** means an electronic service normally provided for remuneration, which consists of  
   **a)** the creation, verification, and validation of electronic signatures, electronic seals or electronic time stamps, electronic registered delivery services and certificates related to those services, or  
   **b)** the creation, verification, and validation of certificates for website authentication; or  
   **c)** the preservation of electronic signatures, seals or certificates related to those services;  

**Certificate Holder** means the entity identified in the Certificate as the holder of the private key belonging to the public key contained in the Certificate;  

**Certificate for website authentication** means an attestation that makes it possible to authenticate a website and links the website to the natural or legal person to whom the certificate is issued;  

**Contractor** means a legal entity with whom Disig has entered into a written agreement to provide trusted services;  

**Electronic signature** means data in electronic form which is attached to or logically associated with other data in electronic form, and which is used by the signatory to sign;  

**Electronic seal** means data in electronic form, which is attached to or logically associated with other data in electronic form to ensure the latter origin and integrity;  

**Key pair** means a part of a PKI system that uses an asymmetric cryptography and consists of a public key and a private key;  

**Multi-purpose CA** - A root CA or subordinate CA that is in a hierarchy without restrictions on the type of certificate issued to the end holder, i.e. in the hierarchy it is possible to issue Certificates, TLS certificate, or other types of certificates, to end users;  

**PKCS#10*** means a format of messages sent to a Certification Authority to request certification of a public key;  

**PEM** means file format for storing and sending cryptography keys, certificates, and other data as is formalized by the IETF in RFC 746;  

**RA staff member** means an employee of the Provider or other legal entity that has a contract with the Provider for the provision of certification services;  

**RA of the Provider** - a term that includes all types of RA (commercial, enterprise, 
internal);  

**Relying party** means a natural or legal person that relies upon an electronic identification or a trust service;

**S/MIME Certificate** - contains a Public Key bound to a Mailbox Address and may also contains the identity of a Natural Person or Legal Entity that controls such email address.  

**S/MIME STRICT profile** - profiles for S/MIME Certificates with "extKeyUsage" limited to "_id-kp-emailProtection_" and stricter use of Subject DN attributes and other extensions;  

**S/MIME MULTIPURPOSE profile** - profiles are aligned with the more defined Strict Profiles, but with additional options for extKeyUsage and other extensions. This is intended to allow flexibility for crossover use cases between document signing and secure email.  

**Publicly-Trusted Certificate** |means a certificate that is trusted by virtue of the fact that its corresponding root certificate is distributed as a trust anchor in widely-available application software.  

**Single-purpose CA** - A root CA or subordinate CA that is in a hierarchy that is strictly limited to issuing exactly one type of certificate to an end user, i.e. in the hierarchy, only SMIME Certificates can be issued to end user;  

**Subscriber** means a natural person or legal entity to whom a Certificate is issued and who is legally bound by a subscriber agreement or terms of use.  

**Trust service provider** means a natural or a legal person who provides one or more trust services either as a qualified or as a non-qualified trust service provider;  

**SAN** means an extension to X.509 that allows various values to be associated with a security certificate using a subjectAltName field.  

**TLS** are cryptographic protocols designed to provide communications security over a computer network.  

###  1.6.2	Acronyms 

|  | |
| :--- | :--- |
|ASCII |American Standard Code for Information Interchange|  
|CA    |Certification Authority| 
|CMA   |Certificate Management Authority|  
|CP/CPS|Certificate Policy and Certification Practice Statement (CP/CPS)|  
|CRL   |Certification Revocation List|  
|FQDN  |Fully Qualified Domain Name|  
|HSM   |Hardware Security Module|  
|IČO   |Organization identification number|  
|LEI   |Legal Entity Identifier|  
|OCSP  |Online Certificate Status Protocol|  
|OID   |Object Identifier|  
|PKCS#10|Certificate request format based on Public Key Cryptographic Standards (RFC 2986)   
|PKI   |Public Key Infrastructure|  
|PMA   |Policy Management Authority|  
|RA    |Registration Authority|  
|RFC   |Request for Comments|  
|S/MIME|Secure MIME (Multipurpose Internet Mail Extensions)|  
|TSA   |Time Stamp Authority|  
|URL   |Uniform Resource Locator|  
|UTC   |Coordinated Universal Time|  

###  1.6.3	References 
**[1]**    Baseline Requirements for the Issuance and Management of Publicly-Trusted S/MIME Certificates [https://cabforum.org/working-groups/smime/documents/](https://cabforum.org/working-groups/smime/documents/)    
**[2]**    RFC 5280 "Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile"    
**[3]**    Regulation (EU) No 910/2014 of the European Parliament and of the Council of 23 July 2014 on electronic identification and trust services for electronic transactions in the internal market in the wording of Regulation (EU) No1183/2024 of the European.  
**[4]**    ETSI TS 119 411-6 "Electronic Signatures and Infrastructures (ESI); Policy and security requirements for Trust Service Providers issuing certificates; Part 6: Requirements for Trust Service Providers issuing publicly trusted S/MIME certificates."  
**[5]**    ETSI EN 319 401 "Electronic Signatures and Infrastructures (ESI); General Policy Requirements for Trust Service Providers."   
**[6]**    ETSI EN 319411-1 "Electronic Signatures and Infrastructures (ESI); Policy and security requirements for Trust Service Providers issuing certificates; Part 1: General requirements."   
**[7]**    RFC3647  "Request for Comments: 3647, Internet X.509 Public Key Infrastructure: Certificate Policy and Certification Practices Framework"   
**[8]**    General Terms of Service and Use of the Trusted Certificate Issuance and Verification Service [https://eidas.disig.sk/pdf/vp_tsp_disig.pdf](https://eidas.disig.sk/pdf/vp_tsp_disig.pdf)      
**[9]**    X.500 "Information technology - Open Systems Interconnection - The Directory: Overview of concepts, models and services", 10/2012, ITU-T.  
**[10]**   X.501 "Information technology - Open Systems Interconnection - The Directory: Models.", 10/2012,  ITU-T.  
**[11]**   X.520 "Information technology - Open Systems Interconnection - The Directory: Selected attribute types", 10/2016, ITU-T.     
**[12]**   RFC 5322 "Internet Message Format".   
**[13]**   Baseline Requirements for the Issuance and Management of Publicly-Trusted TLS certificates [https://cabforum.org/baseline-requirements-documents/](https://cabforum.org/baseline-requirements-documents/).  
**[14]**   Information about the Processing of Personal Data, Disig, a.s. [https://eidas.disig.sk/pdf/info_oou_gdpr_en.pdf](https://eidas.disig.sk/pdf/info_oou_gdpr_en.pdf)     
**[15]**   RFC 9495 "Certification Authority Authorization (CAA) Processing for Email Addresses."    
**[16]**   RFC 6960 "X.509 Internet Public Key Infrastructure Online Certificate Status Protocol - OCSP".   
**[17]**   RFC 5019 "The Lightweight Online Certificate Status Protocol (OCSP) Profile."   
**[18]**   NIST 800-89 "Recommendation for Obtaining Assurances for Digital Signature Applications."   
**[19]**   Network and Certificate System Security Requirements [https://cabforum.org/working-groups/netsec/documents/](https://cabforum.org/working-groups/netsec/documents/)     
**[20]**   RFC 6818 "Updates to the Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile"   
**[21]**   ETSI EN 319 412-1 "Electronic Signatures and Infrastructures (ESI);Certificate Profiles; Part 1: Overview and common data structures."     
**[22]**   ISO 3166-1 "Codes for the representation of names of countries and their subdivisions - Part 1: Country code."   

### 1.6.4 Conventions
The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this CP/CPS shall be interpreted in accordance with RFC 2119.

# 2.	PUBLICATION AND REPOSITORY RESPONSIBILITIES 
The Provider shall create, implement, enforce, and update (at least once per year) its CP/CPS describing in detail how the legislative requirements and the requirements of the applicable document are implemented. 

##  2.1	Repositories 
Repositories shall be located so that they are accessible to Certificate Holders and Relying Parties and are consistent with the overall security requirements.
The Provider's website is publicly accessible via the Internet to Subscribers, Certificate Holders, Relying Parties, and the public at large.

The Provider operates one publicly accessible repository (see Section 1) that provides current information relevant to this CP/CPS, including:
* this CP/CPS and previous versions;
* the applicable general terms and conditions for the provision of trust services;
* CA certificates and their fingerprints;
* Certificate Revocation Lists (CRLs).  

Publicly accessible information published in the Provider's repository is subject to managed access controls.

##  2.2	Publication of information 
The Provider shall provide an online repository accessible to Subscribers, Certificate Holders, and Relying Parties on a 24x7 basis, containing at least the following information:
* Certificates issued in accordance with this CP/CPS;
* the current CRL, as well as all CRLs issued since the start of Certificate issuance operations;
* the certificates of Root CAs and Subordinate CAs correspond to the public keys whose associated private keys are used to sign issued Certificates and CRLs;
* the current version of the CP/CPS;
* information on the outcome of regular audits of the performance of the trust services provided.  

The Provider is not required to publish information about issued Certificates where such Certificates are issued for internal needs of contractual partners and non-publication has been contractually agreed with the partner.  

The Provider confirms that this CP/CPS reflects all requirements of the current version of SMIME BR [1], published at [https://cabforum.org/smime-br/](https://cabforum.org/smime-br/).

In the event of any inconsistencies between those requirements and this CP/CPS, the requirements of the current version of SMIME BR [1] shall prevail.

### 2.2.1 Policies and Practice Statements 
The current and previous versions of the CP and CPS or combined CP/CPS are published at:  
[https://eidas.disig.sk/en/provider/policies-and-documents/](https://eidas.disig.sk/en/provider/policies-and-documents/) - EN versions  
[https://eidas.disig.sk/sk/poskytovatel/politiky-a-dokumenty/](https://eidas.disig.sk/sk/poskytovatel/politiky-a-dokumenty/) - SK/EN versions

### 2.2.2 CA Certificates
The public key certificates for the Root CAs, Subordinate CAs (Issuing CAs), and any applicable Cross-Certificates are published at:

[https://eidas.disig.sk/en/certificates/ca/](https://eidas.disig.sk/en/certificates/ca/) - EN version  
[https://eidas.disig.sk/sk/certifikaty/ca/](https://eidas.disig.sk/sk/certifikaty/ca/) - SK version

### 2.2.3 Certificate Revocation Lists (CRLs) 
Provider CRLs at the following HTTP URLs to avoid circular dependencies during validation:

|CA        |CRL distribution point  |
|----------|:----------------------|
|CA Disig Root R2|[http://cdp1.disig.sk/rootcar2/crl/rootcar2.crl](https://cdp1.disig.sk/rootcar2/crl/rootcar2.crl)<br>[http://cdp2.disig.sk/rootcar2/crl/rootcar2.crl](http://cdp2.disig.sk/rootcar2/crl/rootcar2.crl)|
|CA Disig R2I5 Certification Service|[http://cdp.disig.sk/subcar2i5/crl/subcar2i5.crl](https://cdp.disig.sk/subcar2i5/crl/subcar2i5.crl)|
|CA Disig SMIME Root R4|[http://cdp.disig.sk/rootcar4/crl/rootcar4.crl](https://cdp.disig.sk/rootcar4/crl/rootcar4.crl)|
|CA Disig R4I1 SMIME Certification Service|[http://cdp.disig.sk/subcar4i1/crl/subcar4i1.crl](https://cdp.disig.sk/subcar4i1/crl/subcar4i1.crl)|


##  2.3	Time or frequency of publication 
A Certificate shall be published as soon as possible after it is issued. Information about the Certificate issued shall be available on the Provider's website (see Section 1). Certificates issued for closed systems or for the Provider's internal purposes need not be publicly available. 

A Certificate is published immediately upon issuance, and the Subscriber/Holder can retrieve it immediately. Information about the Certificate issue is available in the Provider's repository (see Section 2.1).  
The CRL shall be published as specified in Section 4.9.7. Information about a revoked Certificate shall be available on the Provider's website (see Section 1), which serves as its repository.

All information required to be published in the repository shall be published, where possible, as soon as possible.    
The CRL is published as specified in Section 4.9.8. Information about a revoked Certificate can be found in the Provider's repository.  

##  2.4	Access controls on repositories
The Provider shall protect any information stored in the repository that is not intended for public dissemination. The Provider shall use best efforts to ensure the integrity, confidentiality, and availability of data related to the provision of trust services. The Provider shall also implement logical and security measures to prevent unauthorized access to the repository by persons who could in any way modify, damage, add, or delete data stored in the repository.    
Through technical and adopted organizational measures, the Provider protects any information stored in the repository that is not intended for public dissemination. For this purpose, it has established precise rules included in the Provider's security project and related internal policies. 

Publicly accessible information published in the Provider's repository is subject to managed access controls.

#  3.	IDENTIFICATION AND AUTHENTICATION 

##  3.1	Naming 

###  3.1.1	Types of names
Each CA must be able to create Certificates that contain Distinguished Names in the sense of X.500 (X.500 Distinguished Name, hereinafter "Distinguished Name") [9] - specifically in accordance with X.501 [10] and X.520 [11] and names in the sense of RFC 5322 (Internet Message Format) [12].  
Subscribers must choose for themselves the Distinguished Name that is to be included in their Certificate. 

###  3.1.2	Need for names to be meaningful
The term "meaningfulness" means that the form of the name must have a commonly used format for determining the identity of the Holder (natural person, legal person/organization).

###  3.1.3	Anonymity or pseudonym of subscribers 
The Provider does not support the use of pseudonyms, nicknames, code names, aliases, and similar (so-called "nicknames") in Certificates.

###  3.1.4	Rules for interpreting various name forms
#### 3.1.4.1 Replacement of non-ASCII characters
Slovak diacritical characters that are not part of the basic ASCII character set can be used in Certificate.  
If necessary, Slovak diacritical characters can be replaced with their equivalents in the basic ASCII table as follows.

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

#### 3.1.4.2 Geographic names
No stipulation.

###  3.1.5	Uniqueness of names
No stipulation. 

###  3.1.6	Recognition, authentication, and role of trademarks
No stipulation. 

##  3.2	Initial identity validation
The Provider shall authenticate all identity attributes of the Subject that will be included in the Certificate and the Subject's control over the email address, according to the following requirements:
| Certificate type                                             | Mailbox Control | Organization Identity | Individual Identity|
|--------------------------------------------------------------|:---------------:|:---------------------:|:-------------------|
| S/MIME digital signature certificate [Individual-validated]  | Section 3.2.2   | NA                    | Section 3.2.4      |
| S/MIME digital signature certificate [Sponsor-validated]     | Section 3.2.2   | Section 3.2.3         | Section 3.2.4      |
| S/MIME digital signature certificate [Organization-validated]| Section 3.2.2   | Section 3.2.3         | NA                 |

Authentication and verification on behalf of the Provider shall be performed by an RA staff member prior to Certificate issuance.

###  3.2.1	Method to prove possession of private key 
No stipulation.

###  3.2.2	Validation of mailbox authorization or control 
This section defines the processes and procedures for confirming the Applicant's control over the email address that is to be included in the issued Certificate.    
The Provider's RA must verify that the Applicant controls the email address referenced in the Certificate application.      

The Provider may not delegate email-address control verification to a third party (this does not apply to contractually bound RAs providing trusted services on behalf of the Provider).  
The Provider's RA must keep records of which method was used to verify the email address, including the version of the SMIME BR [1] used during verification.     

The Provider's RA may reuse a completed verification to issue multiple Certificates, provided the time intervals in section 4.2.1 are respected.  
_Note: The email address may be included in the Holder's Certificate as rfc822Name or as otherName of type id-on-SmtpUTF8Mailbox in the subjectAltName extension._

#### 3.2.2.1 Validating authority over mailbox via domain
When issuing a sponsor-validated Certificate for a contractual partner, where verification is not performed individually for each Applicant's email address, control may be verified by confirming that the contractual partner controls the domain part of the email address to be used in the Certificate.  

For this verification, the Provider shall use only the approved methods listed in section 3.2.2.4 of document BR TLS [13].  
The RA staff member performs the verification using one of these methods from document [13]:  
* Email to the contact listed in DNS CAA (chapter 3.2.2.4.13),
* Email to the contact listed in DNS TXT (chapter 3.2.2.4.14),    

by sending a random text string of at least 20 characters, containing upper and lowercase letters, numbers, and special characters. 
For each verification, the RA staff member records the method used, the date used, and the email address used.

#### 3.2.2.2 Validating control over mailbox via email
The Provider's RA may verify control of the mailbox for each email address to be included in the issued Certificate by sending a random value by email and then receiving a confirming response using that random value.
Control over each email address must be confirmed using a unique random value. The random value must be sent only to the verified email address and must not be shared in any other way.  

The random value must be unique in every email sent and may remain valid for use in the confirming response for a maximum of 24 hours from its creation. The random value must change after each email sent by the Provider to the mailbox address; however, all relevant random values sent to the same mailbox address may remain valid for confirming responses during the validity period stated in this section.

The RA staff member performs the verification via the RA Client application by sending the random value to the email address in the Certificate application. Sending is performed automatically after loading the Certificate profile and the corresponding issuance request into RA Client and selecting the email verification option (verify Email).

The Applicant has 24 hours to confirm the random value.   
The RA staff member checks the verification status in RA Client under "Search" and the "Email verification" tab; if the status is "approved", the verification was successful.

#### 3.2.2.3 Validating applicant as operator of associated mail server(s)
The Provider does not support this method.

#### 3.2.2.4 Verification of mailbox control using ACME extensions 
The Provider does not support this method.

###  3.2.3	Authentication of organization identity

When verifying the identity of a legal entity included in the Certificate profiles for an employee of a legal entity and seal Certificate, the requirements defined in the following subchapters must be met.

#### 3.2.3.1 Attribute collection of organization identity
The Provider's RA must obtain and retain evidence of the organization's (legal entity's) identity, if included in the Certificate::
* Formal name
* Assumed name
* Organizational unit
* Registered office address
* Jurisdiction of incorporation or registration
* Unique identifier and its type.  

The unique identifier must be stated in the Certificate Subject as organizationIdentifier in accordance with Article 7.1.4.2.2 and Annex A of SMIME BR [1]. 
Additionally (if included in the Certificate), the RA obtains and retains evidence for:
* Formal name
* Unique identifier and its type

#### 3.2.3.2 Validation of organization identity

##### 3.2.3.2.1 Verification of name, address, and unique identifier
The Provider's RA verifies the full name and address (if included in the Certificate Subject) of the Applicant legal entity using provided documentation or by communication with at least one of the following:  
**1.**  A government agency within the jurisdiction of incorporation, existence, or recognition of the legal entity;  
**2.**  A reference to Legal Entity Identifier (LEI) data;  
**3.**  Verification by the Provider's RA (or its representative) at the Applicant's premises; or  
**4.**  An attestation that includes a copy of supporting documentation proving the Applicant's legal existence (e.g., certificate of registration, articles, operating agreement, statute, or regulatory act).  

The RA may use the documentation/communication described in items 1-4 to verify the Applicant's identity and address.
For an organization based in the Slovak Republic, the RA verifies the organization's full name and unique identifier based on:
* an original extract from the Slovak Commercial Register (OR SR), or
* if the Applicant is not recorded in OR SR, an original extract from the Register of Legal Entities, Entrepreneurs and Public Authorities maintained by the Statistical Office of the Slovak Republic (RPO SR).
 
If a legal entity cannot prove its identity via an extract from the commercial register or register of legal entities, it must also prove in writing (in addition to identity) the legality / "reason" for its existence, by referencing the relevant law or other regulation, deed of foundation, etc.  

If the legal entity is not based in the Slovak Republic, its identity is verified by submitting an extract from a governmental register in the jurisdiction of incorporation/existence/recognition; the RA then confirms existence via the website "Business registers - search for a company in the EU".
An original document (or an officially certified copy of the original) must not be older than three months and must contain the full business name/title and an identification value. 
The RA also accepts an electronic extract from the used register if it is authorized by a qualified electronic seal of the government authority responsible for maintaining the register. 

#### 3.2.3.3 Verification of assumed name
Provider supports only issuing Certificates under a duly registered name.

#### 3.2.3.4 Disclosure of verification sources
Provider's RA must verify the unique identifier used in the Certificate in a register maintained or authorized by the competent government authority. The Provider must publish this authorized source via appropriate and easily accessible online means (see chapter 3.2.3.2.1).

###  3.2.4	Authentication of individual identity 
 Provider must ensure that the Certificate Holder's identity and public key are appropriately bound, and must specify authentication procedures in its CP/CPS. The Provider's CA must record this process for each Certificate in written or electronic form. The authentication documentation must include at least:
* the identity of the person performing the authentication,
* unambiguous identification data from identity documents proving the Certificate Holder's identity,
* the date the identification was performed.  

Identity verification must be performed by the Provider's RA based on a document containing these Holder details:
* full given name and surname,
* permanent residence address,
* national ID number (for persons to whom it is assigned),
* date of birth (for persons without a national ID number),
* additional data specified in section 3.2.4.1.  

The RA must process and retain personal data in accordance with applicable laws and the provisions in section 9.4.

#### 3.2.4.1 Attribute collection of individual identity 
The Provider must document and publish the methods it uses and collects for verifying natural person identity.

##### 3.2.4.1.1 From a physical identity document
For identity verification, the Provider's RA currently accepts the following documents presented by the Holder in person:
* eID (issued by government authority), or residence permit in the Slovak republic (in case of foreigners); or
* Passport.  

The Subscriber/Holder must also present an additional document containing at least the Holder's name and another personal attribute (date of birth, national ID number), such as: 
* Driving license;
* Birth certificate;
* Service card;
* Health insurance card;
* Firearm license;
* Passport.  

The Provider's RA must also record the following data from the documents:
* Full name and surname;
* Permanent residence (if it is listed in the document);
* Birth registration number (applicants who have it assigned);
* Date of birth (applicants without birth registration number);
* Serial number of identity document;
* Issuer of identity document;
* Validity of identity document.  

If a birth certificate, firearms licence, service ID card, or public health insurance card is provided, the Holder must also provide one of the following: identity card or passport.
If a natural person represents another natural person, they must additionally present an officially certified power of attorney clearly authorizing the representative to act on behalf of the represented person, and containing all data listed in section 3.2.4.1.

##### 3.2.4.1.2 From a digital identity document
The Provider currently does not support this method for initial natural-person identity verification. 

##### 3.2.4.1.3 Using electronic identification schemes 
The Provider currently does not support this method for initial natural-person identity verification. 

##### 3.2.4.1.4 From a certificate supporting a digital signature applied by the Applicant
The Provider does not use this method of initial identity authentication at this moment. 

##### 3.2.4.1.5 Enterprise RA records
An Enterprise RA issuing a sponsor-validated signing Certificate shall verify all natural-person identity attributes to be included in the Certificate. During verification, the Enterprise RA may rely on existing internal records and does not have to require physical presentation of an identity document, provided the internal records contain all personal data required by the Provider and the data that will be written into the Certificate.

##### 3.2.4.1.6 Affiliation from company attestation 
In the case of Sponsor-validated Certificates not approved by an Enterprise RA, the RA may verify the authority or affiliation of an Individual to represent an Organization to be included in the "subject:organizationName" of the Certificate using an Attestation provided by the Organization RA shall verify natural person identity according to section 3.2.4 and verify company identity according to section 3.2.3

#### 3.2.4.2 Validation of individual identity
The RA of the Provider shall validate all identity attributes of the Individual to be included in the Certificate.
If the evidence has an explicit validity period, the CA shall verify that the time of the identity validation is within this validity period. In context this can include the "validFrom" and "validTo" attributes of a digital signature Certificate or the date of expiry of an identity document.  
The RA of the Provider may reuse existing evidence to validate Individual identity subject to the age restrictions in Section 4.2.1.  

##### 3.2.4.2.1 Validation of a physical identity document
The physical identity document shall be presented in its original form. The RA of the Provider only accepts a personally submitted document and does not support its remote verification, e.g. through the video.  
The RA registration agent shall make a visual comparison of the physical appearance of the Applicant and the face photo and/or other information on the physical identity document.
The RA registration agent shall have access to authoritative sources of information on document appearance.  
The Provider or RA of the Provider retains information sufficient to evidence the fulfillment of the identity validation process and the verified attributes. In addition to identity attributes, the Provider record the following information: issuer, validity period, and the document's unique identification number.

##### 3.2.4.2.2 Validation of a digital identity document
The Provider does not use this method of initial identity authentication at this moment. 

##### 3.2.4.2.3 Validation of eID 
The Provider does not use this method of initial identity authentication at this moment. 

##### 3.2.4.2.4 Validation of digital signature with certificate 
The Provider does not use this method of initial identity authentication at this moment. 

##### 3.2.4.2.5 Validation of an Attestation
If the Attestation is used as evidence to validate the identity attributes of a natural person, then its reliability must be verified according to the section 3.2.8.

##### 3.2.4.2.6 Validation using an Enterprise RA record 
An Enterprise RA issuing a sponsor-validated signing Certificate must verify all natural-person identity attributes to be included in the Certificate. During verification, the Enterprise RA may rely on existing internal records and does not have to require physical presentation of an identity document, provided the internal records contain all personal data required by the Provider and the data that will be written into the Certificate.

###  3.2.5	Non-verified subscriber information 
Information about an Applicant that has not been verified in accordance with this CP/CPS must not be included in Certificates.

###  3.2.6	Validation of authority 
Before commencing to issue Organization-validated and Sponsor-validated Certificates for an Applicant, the Provider shall use a Reliable Method of Communication to verify the authority and approval of an Applicant Representative to perform one or more of the following:
* act as the Enterprise RA,
* request issuance or revocation of Certificates, or
* assign duties to others to act in these roles.  

The Provider may implement a process allowing the Applicant to designate individuals who may continuously act as Applicant representatives; likewise, the Provider will provide the Applicant with a list of its authorized Applicant Representatives based on a verified written request from the Applicant.
The Provider may use the sources listed in section 3.2.3.2.1 to verify a reliable communication method. If a reliable communication method is used, the Provider may verify the authenticity of the Certificate request directly with the Applicant's representative or with a trusted source within the Applicant's organization (e.g., business units, HR, IT, or another department the Provider considers appropriate)..

###  3.2.7	Criteria for Interoperation
The Provider must publish all cross-certificates that identify the Provider as the certificate Subject.

###  3.2.8	Reliability of verification sources 
Before the Provider's RA relies on a source of verification data when verifying a Certificate application, it must verify that the source is suitable as a reliable data source.
Enterprise RA records are a reliable source for natural-person attributes included in sponsor-validated signing Certificates issued within an organization that is the Provider's Enterprise RA.
The Provider's RA may rely on a confirmation letter that information or another fact is correct if it verifies that the letter was written by an accountant, lawyer, government official, or another reliable third party in the Applicant's jurisdiction that is typically relied upon when obtaining such information.
The confirmation must include a copy of the document evidencing the fact to be attested.
The Provider's RA will use a reliable method of communication to contact the sender and confirm the authenticity of the attestation.

##  3.3	Identification and authentication for re-key requests 

###  3.3.1	Identification and authentication for routine re-key 
No stipulation.

###  3.3.2	Identification and authentication for re-key after revocation 
No stipulation.

##  3.4	Identification and authentication for revocation request
No stipulation. 

#  4.	CERTIFICATE LIFE-CYCLE OPERATIONAL REQUIREMENTS 

##  4.1	Certificate Application 
This section describes the operational requirements of the Certificate life cycle starting with applying for issuance.

###  4.1.1	Who can submit a Certificate application
The Provider may be requested to issue::
* A signing Certificate for a natural person (Individual-validated):
   * The natural person
*  A signing Certificate for an employee of a legal entity (Sponsor-validated):
   * a natural person authorized by Subscriber, 
   * any entity with which the natural person is associated (e.g., the employer, a non-profit organization of which the person is a member, etc.)
* A seal Certificate for a legal entity (Organization-validated):
   * any entity that, under applicable national legislation, acts on behalf of the given legal entity (organization).  

###  4.1.2	Enrollment process and responsibilities

#### 4.1.2.1 Preparation
As preparation for visiting the Provider's RA, the Subscriber/Holder shall
* Familiarize themselves with the "General Terms and Conditions for the Provision and Use of the Trusted Service for Issuance and Verification of Certificates" ("General Terms and Conditions") [8] and with the personal data protection regulations, i.e., Regulation (EU) 2016/679 of the European Parliament and of the Council (GDPR) and Act No. 18/2018 Coll. on personal data protection and Act No. 18/2018 Coll. on the Protection of Personal Data (hereinafter referred to as the "Regulations on the Protection of Personal Data") [14] , which must be available in readable form via a durable communication channel (see [https://eidas.disig.sk/sk/documents/](https://eidas.disig.sk/sk/documents/));  
* Familiarize themselves with this procedure and/or the principles and instructions for obtaining a Certificate;;  
* Prepare a Certificate request in PKCS#10 format and send it in advance by email to the Provider's RA (see paragraph 4.1.2.3);  
* Prepare the selected identity documents and/or other required supporting documents (e.g., extract from the commercial register, powers of attorney, etc.);  
* Arrange an appointment date.

#### 4.1.2.2 Request generation 

##### 4.1.2.2.1 Certificate Request generation 
A request for a Certificate for a natural person or a legal entity may be submitted only on the basis of a PKCS#10 request. The Subscriber/Holder must generate the request on their computer using a suitable browser and the Provider's website (see the URL in Section 1) and save it to an appropriate medium.  
A Certificate request for a natural person must be sent to the relevant RA of the Provider in advance by email from the email address that is stated in the Certificate request in the email field "subject:emailAddress". 

A Certificate request for a legal entity must also be sent to the relevant RA of the Provider in advance by email from the email address that is stated in the Certificate request in the email field "subject:emailAddress". The email address in a legal-entity Certificate request must not be an individual's email address. The Provider's RA accepts only a general/shared email address of the legal entity, such as <obchod@disig.sk>, <faktury@disig.sk> etc.

The Provider's RA reserves the right to reject an application for a legal-entity Certificate if this requirement is not met.
Email addresses of the Provider's individual RAs are available on the Provider's website (see section 1).  
For security reasons, a Certificate request (and the public key contained in it) for which a Certificate has already been issued must not be reused for issuance of another Certificate and must be rejected by the RA.  
When entering values into the fields of the Certificate request, the Subscriber/Holder must consider that, at the RA, they will have to satisfactorily demonstrate entitlement to all data stated in the individual fields of the Certificate request.

A Certificate request for an employee of a contractual partner may also be generated by another method than via the Provider's website (e.g., the contractual partner's own web portal, etc.). This method must be agreed in advance with the contractual partner, and individual applicants must be informed about the method of request generation and submission both by the contractual partner and by the Provider.

#### 4.1.2.3 Sending a Certificate request
The Subscriber/Holder submits the Certificate issuance request to the relevant RA of the Provider ([https://eidas.disig.sk/en/contact/registration-authorities/](https://eidas.disig.sk/en/contact/registration-authorities/)) which must perform all procedures related to the Certificate issuance process. 

##  4.2	Certificate application processing 

###  4.2.1	Performing identification and authentication functions
Before issuing a Certificate, the Provider's RA shall:
* inform the present natural person about the General Terms and Conditions [8];
* check the completeness and correctness of the data in the received Certificate application;
* verify the identity of the future Certificate Holder and enter their personal data into the Provider's information system (IS), while completing all mandatory fields required by the Provider's system;
* verify additional documents supporting any identification data to be included in the Certificate.. 

If the Certificate is for a natural person or a legal entity where the cryptographic keys are not in a QSCD, the Provider's RA staff member shall, before verifying the Certificate Holder's identity, review the delivered Certificate request, which may be in PKCS#10 format. For the content of the request fields and the obligation to complete them, see Section 7.  
The Provider's RA staff member shall verify that the electronically submitted Certificate request of a given Subscriber/Holder does include "subject:emailAddress" field and that it was sent from the same e-mail address as stated in the Certificate request. If differences are found, the RA personnel may refuse to issue the Certificate.

Before issuing the Certificate, the Provider's RA will perform the following via the RA Client application:
* check that the e-mail address stated in the application corresponds to the e-mail address from which the application was sent;
* check the completeness and correctness of the data in the received Certificate application, including that it contains only permitted fields in accordance with Section 7.1.4.2.2 of this CP/CPS;
* verify the Applicant's ownership and control of the e-mail address in accordance with Section 4.2.1.1;
* check that the verification of ownership/control of the Applicant's e-mail address was successful and that the Certificate may be issued.
In case of an in-person visit of the Applicant or an authorized representative to the Provider's RA, the RA personnel:
* informs the present natural person about the General Terms and Conditions [8];
* verifies the identity of the future Certificate Holder in accordance with Section 3.2.4.2 and, via the RA Client application, enters their personal data into the Provider's IS while filling in all mandatory fields required by the Provider's system, 
* verifies additional documents supporting any identification data to be included in the Certificate, e.g., the identity of an organization in accordance with Section 3.2.3.2. 

If differences are found, the RA stuff member may refuse to issue the Certificate. 
When verifying the identity of a natural person or a legal entity, existing identity verification may be reused, provided it meets the time limits specified in Sections 4.2.1.3 and 4.2.1.2 respectively.

#### 4.2.1.1 Validation of mailbox authorization or control
Verification of ownership and control of the email address via the domain, or verification of the Applicant as the operator of the corresponding mail servers, successfully completed in accordance with the requirements of Section 3.2.2.1 or Section 3.2.2.3, may be obtained no earlier than 398 days prior to Certificate issuance.
Verification of ownership and control of the email address, successfully completed in accordance with the requirements of Section 3.2.2, may be obtained no earlier than 30 days prior to Certificate issuance.

#### 4.2.1.2 Authentication of organization identity 
Verification of control, successfully completed in accordance with the requirements of Section 3.2.3, may be obtained no earlier than 825 days prior to Certificate issuance.
Confirmation of authority in accordance with the requirements of Section 3.2.6 may be obtained no earlier than 825 days prior to Certificate issuance, unless the contract between the Provider and the Subscriber/Holder specifies a different period. 

#### 4.2.1.3 Authentication of individual identity 
Full verification of a natural person's identity in accordance with Article 3.2.4 may be obtained no earlier than 825 days prior to Certificate issuance. A previous validation must not be reused if any data or documents used in the previous validation were obtained earlier than the permitted reuse period.

###  4.2.2	Approval or rejection of Certificate applications 
The RA staff member will begin processing the Certificate issuance request immediately upon its receipt, in accordance with the procedures set out in Section 4.2.1. The Certificate will be issued provided that all issuance conditions are met and it is also verified that the Provider is authorized to issue the Certificate in accordance with Section 4.2.2.1.  
The RA staff member shall reject the Certificate issuance request if they have reasonable doubt about the identity of the Holder, and also if deficiencies in identification documents are identified, incomplete information has been provided, or if the Provider has previously issued a Certificate for the given public key, or if the Provider is not authorized to issue the Certificate..

#### 4.2.2.1 Certification authority authorization
Subscribers who wish to restrict ("reserve") Certificate issuance providers and wish Disig, a.s. to be among the selected providers should enter the value "disig.sk" in their DNS record for the "issuemail" property.

As of 15 March 2025, the Provider performs a CAA record check of the domain name stated in the email address in the Certificate issuance request, in accordance with Section 4 of RFC 9495 [15].
Some methods relied upon to verify the Holder's control over the domain portion of the mailbox address to be used in the Certificate (see Sections 3.2.2.1 and 3.2.2.3) require that CAA records be fetched and processed from additional remote network perspectives prior to Certificate issuance (see Section 4.2.2.2).   

To confirm the primary network perspective, the response to the remote network perspective CAA check must be interpreted as authorization to issue regardless of whether the responses from both perspectives byte-for-byte are identical.

If the Provider issues a Certificate after a CAA check, it must do so within the TTL of the CAA record or within 8 hours, whichever is longer. This provision does not prevent the CA from checking CAA records at any other time.

The Provider must document in sufficient detail potential issuances prevented by an existing CAA record in order to provide feedback to the CA/Browser Forum about the circumstances, and should send reports about such issuance requests to the contacts listed in the CAA iodef records, if present.
The Provider is not expected to support URL schemes in the iodef record other than mailto: or https:.

#### 4.2.2.2 Multi-perspective issuance corroboration
The Provider has implemented MPIC in accordance with item 3.2.2.9 of the TLS Baseline Requirements (BR TLS) [13].

###  4.2.3	Time to process Certificate issuance 
No stipulation.

##  4.3	Certificate issuance 

###  4.3.1	CA actions during Certificate issuance

#### 4.3.1.1 Manual authorization of Certificate issuance for Root CAs
Issuance of a certificate by a Root CA requires the presence of at least two persons in trusted roles (e.g., CA system administrator, CA administrator, CA manager), one of whom issues an unambiguous command instructing the CA Disig root to perform the certificate signing.

#### 4.3.1.2 Linting of to-be-signed Certificate content
Prior to Certificate issuance, an automated validation of the Certificate to be issued is performed for compliance with the SMIME BR and this CP/CPS. If non-compliance is detected during the validation, Certificate issuance will be rejected by the Provider's issuing system.

#### 4.3.1.3 Linting of issued Certificates
The Provider uses the validation process to test compliance with these requirements for every Certificate it issues.
After issuance of an Certificate, an automated validation of the issued Certificate is performed for compliance with the SMIME BR and this CP/CPS. If non-compliance is detected during the validation, an analysis of the causes of the non-compliance must be performed.

###  4.3.2	Notification to subscriber by the CA of issuance of Certificate 
Subscriber is notified when the certificate is issued. Basic information about the certificate and instructions how to download and install it are in the notification. 

##  4.4	Certificate acceptance 

###  4.4.1	Conduct constituting Certificate acceptance 
No stipulation.

###  4.4.2	Publication of the Certificate by the CA 
No stipulation.

###  4.4.3	Notification of Certificate issuance by the CA to other entities 
No stipulation.
##  4.5	Key pair and Certificate usage 

###  4.5.1	Subscriber private key and Certificate usage 
See Section 9.6.3, provisions 2. and 4.

###  4.5.2	Relying party public key and Certificate usage 
No stipulation.

##  4.6	Certificate renewal 
Every Certificate is issued for newly generated keys, and the procedure is carried out in accordance with the provisions set out in Sections 4.1 to 4.5.

###  4.6.1	Circumstance for Certificate renewal 
No stipulation.

###  4.6.2	Who may request renewal 
No stipulation.

###  4.6.3	Processing Certificate renewal requests 
No stipulation.

###  4.6.4	Notification of new Certificate issuance to subscriber 
No stipulation.

###  4.6.5	Conduct constituting acceptance of a renewal Certificate 
No stipulation.

###  4.6.6	Publication of the renewal Certificate by the CA 
No stipulation.

###  4.6.7	Notification of Certificate issuance by the CA to other entities 
No stipulation.

##  4.7	Certificate re-key 
Every Certificate is always issued as new Certificate for newly generated keys and Certificate request, where the procedure is in accordance with the provisions stated in sections 4.1 to 4.5.

###  4.7.1	Circumstance for Certificate re-key 
No stipulation.

###  4.7.2	Who may request certification of a new public key 
No stipulation.

###  4.7.3	Processing Certificate re-keying requests 
No stipulation.

###  4.7.4	Notification of new Certificate issuance to subscriber 
No stipulation.

###  4.7.5	Conduct constituting acceptance of a re-keyed Certificate 
No stipulation.

###  4.7.6	Publication of the re-keyed Certificate by the CA 
No stipulation.

###  4.7.7	Notification of Certificate issuance by the CA to other entities 
No stipulation.

##  4.8	Certificate modification 

###  4.8.1	Circumstance for Certificate modification 
No stipulation.

###  4.8.2	Who may request Certificate modification 
No stipulation.

###  4.8.3	Processing Certificate modification requests 
No stipulation.

###  4.8.4	Notification of new Certificate issuance to subscriber 
No stipulation.

###  4.8.5	Conduct constituting acceptance of modified Certificate 
No stipulation.

###  4.8.6	Publication of the modified Certificate by the CA 
No stipulation.

###  4.8.7	Notification of Certificate issuance by the CA to other entities 
No stipulation.

##  4.9	Certificate revocation and suspension 

###  4.9.1	Circumstances for revocation 
A Certificate shall be revoked when the binding between the Subject and its public key, as defined in the Certificate, is no longer considered valid.

#### 4.9.1.1 Reasons for Revoking a Subscriber/Subject Certificate
The Provider must revoke a Certificate within 24 hours if any of the following occurs:
* the Subscriber/Holder or another authorized party submits a written request for revocation,
* the Subscriber/Holder notifies the Provider that the original issuance request was not authorized by them and does not provide subsequent authorization for issuance,
* the Provider obtains evidence that the private key corresponding to the public key in the Certificate has been compromised,
* the Provider obtains evidence, by a demonstrable or validated method, that the private key can be easily computed from knowledge of the Certificate's public key (e.g., the Debian weak key issue),
* the Provider obtains evidence that it can no longer rely on the verification of ownership and control of the email address stated in the Certificate.  

The Provider should revoke the Certificate within 24 hours and must revoke it within five (5) days if any of the following occurs:
* the Certificate no longer meets the requirements set out in sections 6.1.5 and 6.1.6,
* the Provider obtains evidence that the Certificate has been misused,
* the Provider determines that the Certificate Holder is not complying with their Certificate Holder obligations to which they are contractually bound,
* the Provider is informed of circumstances indicating that use of the email address or fully qualified domain name (FQDN) in the Certificate is no longer legally permitted (e.g., a court or arbitrator has revoked the right to use the email address or domain name; the relevant license or service agreement between the Subscriber has been terminated; or the account holder has failed to meet the conditions for maintaining the email address or domain name in an active state),
* the Provider becomes aware of material changes to the information stated in the Certificate,
* the Provider becomes aware that the Certificate was not issued in accordance with this CP/CPS,
* the Provider determines that any information stated in the Certificate is inaccurate,
* the Provider terminates its activities for any reason and does not contractually ensure that another CA will provide information about revoked Certificates on its behalf,
* the Provider's right to issue Certificates under this CP/CPS has ceased, or has been revoked, or issuance has been terminated, unless the Provider has taken measures to ensure continuity of CRL/OCSP repository services,
* revocation is required by the provisions of this CP/CPS,
* the Provider is informed, based on a demonstrable or validated method, that the Holder's private key is exposed to compromise, or there is clear evidence that the specific key generation method used was faulty.  

Whenever the Provider becomes aware of any of the circumstances listed above, the Certificate must be revoked and added to the Certificate Revocation List ("CRL").
A revoked Certificate must not be reinstated under any circumstances.

#### 4.9.1.2 Reasons for Revoking a Subordinate CA Certificate
The Provider must revoke a subordinate CA certificate within 7 days if:
* it receives a written request to revoke the subordinate CA certificate,
* the subordinate CA informs the Provider's issuing CA that the original request was not authorized and does not provide subsequent authorization,
* the Provider obtains evidence that the private key corresponding to the public key in the subordinate CA certificate has been compromised, or it no longer meets the requirements set out in sections 6.1.5 and 6.1.6,
* the Provider obtains evidence that the subordinate CA certificate has been misused,
* the Provider becomes aware that the subordinate CA certificate was not issued in accordance with this CP/CPS,
* the Provider determines that any information stated in the subordinate CA certificate is inaccurate or misleading,
* the CA's operation is terminated and there is no possibility that another CA will provide revoked Certificate status information,
* the right of the Provider's issuing CA or subordinate CA to issue Certificates under this CP/CPS has ceased, has been revoked, or issuance has been terminated, unless the Provider has taken measures to ensure continuity of CRL/OCSP repository services,
* revocation is required by this CP/CPS.

###  4.9.2	Who can request revocation 
The Certificate Holder (or a natural or legal person authorized by the Holder) may request revocation of their own Certificate at any time, including without stating a reason for the revocation request.
A revocation request may also be submitted by:
* the Provider - the relevant staff member must document this fact in writing, including the reason for their action,
* a court by means of its judgment or interim measure (a copy of the relevant court decision must be attached to the revocation documentation),
* an entity (natural or legal person) based on inheritance proceedings (a copy of the documents evidencing the entity's right to request revocation must be attached to the revocation documentation).  

Subscribers, Relying Parties, application software suppliers, and other third parties may submit problem reports relating to a Certificate that inform the issuing CA of a reasonable cause for revocation.

###  4.9.3	Procedure for revocation request 
If the authentication requirements for the Certificate Holder requesting revocation are met, a Certificate revocation request may be submitted as follows:
* In person at an RA office, using the "Certificate Revocation Request" form available at the RA - the RA staff member may request the Certificate revocation password if the person requesting revocation is not the Certificate Holder but an authorized representative;
* By email - by sending an signed email message using the private key that forms the key pair with the Certificate being revoked. The message must contain an unambiguous intent to revoke the Certificate expressed by the sentence: "I hereby request revocation of my certificate with serial number XXXXXX";
* By email - by sending an email message (it does not have to be signed). The message must contain an unambiguous intent to revoke the certificate expressed by the sentence:
"I hereby request revocation of my certificate with serial number XXXXXX".
For a message submitted in this way, the email must also include the Certificate revocation password;
* By postal mail, together with the Certificate revocation password, sent to the Provider's address or to the relevant Provider RA that mediated issuance of the Certificate being revoked;
* Via the online service available on the Provider's website. The link to the online certificate revocation service is provided in the certificate receipt confirmation that the Holder receives when collecting the Certificate. Online revocation requires providing the serial number of the relevant Certificate and the revocation password.  

A revocation request for a Certificate issued for the purposes of a contractual partner may be submitted either directly to the Provider or only to the Provider's RA specified in the relevant contract and acting on behalf of the Provider at the contractual partner.
A Certificate that has expired cannot be revoked.
Contacts for incident reporting and the procedure for reporting incidents in the event of possible private-key compromise, Certificate misuse, or other types of fraud, unauthorized issuance, or any other matter relating to an issued Certificate are provided in Section 1.5.2.

###  4.9.4	Revocation request grace period 
No stipulation.

###  4.9.5	Time within which CA must process the revocation request 
Within 24 hours of notification of a problem with a Certificate, the Provider shall review the facts relating to the reported issue and shall provide the Subscriber/Holder and Relying Parties with preliminary information about its findings.
After reviewing the facts and circumstances, the Provider, in cooperation with the Subscriber/Holder and the end entity that reported the problem, shall decide whether the Certificate will be revoked and, if so, within what timeframe.

The time between receiving the report of a Certificate problem and publishing the revocation information must not exceed the timeframe specified in Section 4.9.1.1. 
When determining the deadline, the Provider shall take into account the following:
* the nature of the alleged problem (scope, context, severity, risk of harm to affected parties),
* the consequences of revocation (direct and indirect impacts on Subscribers/Holders),
* the number of reported problems relating to the Certificate in question,
* the entity that reported the problem,
* applicable legal regulations.

###  4.9.6	Revocation checking requirement for relying parties 
When relying on a Certificate, the Relying Party must verify its validity in accordance with the General Terms and Conditions.  
During the period between submission of an authorized request for Certificate revocation and publication of the revoked Certificate on the CRL, the Subscriber/Holder bears full responsibility for any damages caused by misuse of their Certificate. After the Certificate is published on the CRL, full responsibility for any damages caused by the use of the revoked Certificate is borne by the party that relied on the revoked Certificate.  
Failure to validate a Certificate using the CRL is considered a material breach of this CP/CPS.	

###  4.9.7	CRL issuance frequency 
The frequency of issuing the Certificate Revocation List (CRL) varies depending on whether it relates to a Root CA or a Subordinate CA. Table No. 3 contains information on the maximum issuance requirements.  

Table 3: CRL issuance frequency  
| CRL issuer        | Issuance frequency    | nextUpdate vs. thisUpdate  |  Notes |
|--------------|:---------------:|:-------------:|:-------------:|
|   Root CA | max 365 days |  < 365 days | Always within 24 hours after revoking a subordinate CA |
|   Subordinate CA | max 7 days |  < 10 days |  |  

Subordinate CAs of the Provider that issue Certificates to end users must issue CRLs:
* at least every 24 hours, even if no Certificate has been revoked during the previous 24 hours, and with a nextUpdate value of 24 hours.
* Root CAs of the Provider that issue certificates to subordinate CAs must issue CRLs:
* at least every 7 days, with a nextUpdate value of no more than 10 days,
* always within 24 hours after revocation of a subordinate CA certificate.

###  4.9.8	Maximum latency for CRLs 
The maximum CRL latency from its issuance to its publication in the repository must not exceed 90 seconds.

###  4.9.9	On-line revocation/status checking availability 
The OCSP service is provided in accordance with the requirements of RFC 6960, and the OCSP response is signed by:
* an OCSP responder whose Certificate is signed by the CA that issued the Certificate whose revocation status is being checked.  

The OCSP responder's signing certificate contains the ocspSigning EKU (1.3.6.1.5.5.7.3.9) and the id-pkix-ocsp-nocheck extension, as defined in RFC 6960 [16].

###  4.9.10	On-line revocation/status checking requirements 
The Provider's OCSP responders support the HTTP GET method in accordance with RFC 6960 [16] and/or RFC 5019 [17].
For the status of S/MIME Certificates:
* the OCSP response validity interval is greater than or equal to 8 hours,
* the OCSP response validity interval is less than or equal to 8 days,
* the Provider updates information provided via OCSP immediately after a Certificate status change in IS.

For the status of subordinate CA certificates, the information provided via OCSP is updated:
* at least every twelve (12) months,
* within twenty-four (24) hours after revocation of a subordinate CA certificate.

If an OCSP responder receives a request to check the status of a Certificate with a serial number that was not issued by the relevant issuing CA, the OCSP responder must not return a response with the status "good". The Provider monitors the OCSP responder for requests containing serial numbers that were not issued by the given CA, as part of its OCSP-related security processes.

###  4.9.11	Other forms of revocation advertisements available 
No stipulation.

###  4.9.12	Special requirements re-key compromise
A compromise of the private key of the Certification Authorities (Root and Subordinate) operated by the Provider (see Section 1.5.1) under this Certification Policy may be reported to the Provider by third parties using the contact details listed in Section 1.5.1 or 1.5.2, at the reporter's discretion (by phone, email, postal mail, etc.). The reporter may also choose any other method they consider appropriate for such a notification.

###  4.9.13	Circumstances for suspension 
Provider does not provide such a service.

###  4.9.14	Who can request suspension
No stipulation. 

###  4.9.15	Procedure for suspension request
No stipulation. 

###  4.9.16	Limits on suspension period
No stipulation. 

##  4.10	Certificate status services 

###  4.10.1	Operational characteristics 
The CRL must be available at the Provider's website (see section 1) and shall be accessible through the HTTP protocol on port 80.
The OCSP shall be available at the URL specified in the issued certificate and the applicant for Certificate status must send a request in accordance with the 4.9.10.
Revocation entries on a CRL or OCSP Response shall not be removed until after the Expiry Date of the revoked Certificate.

###  4.10.2	Service availability 
The Provider shall operate and maintain its CRL and OCSP capability with resources sufficient to provide a response time of ten seconds or less under normal operating conditions.
The distribution points on which CRLs are published shall be available in 24x7 mode.
OCSP shall be available in 24x7 mode.

###  4.10.3	Optional features 
No stipulation.

##  4.11	End of subscription 
Provision of services to the Certificate Holder by the Provider shall terminate upon expiry of the agreement under which the Certificate was issued.
The agreement may be terminated by either party by mutual agreement even before its expiry. Termination of the agreement must result in the immediate revocation of the Certificate issued under that agreement.

##  4.12	Key escrow and recovery 

###  4.12.1	Key escrow and recovery policy and practices 
The Provider does not escrow or recover the Subscriber's Private Key.

###  4.12.2	Session key encapsulation and recovery policy and practices
No stipulation. 

#  5.	MANAGEMENT, OPERATIONAL, AND PHYSICAL CONTROLS
The security of the Provider must be based on a set of security measures in the area of Physical, Object, Personnel and Operational Security. These security measures must be designed, documented, and applied based on security rules and approved by the Provider's management.  
Security measures shall be available to staff concerned.  
Provider shall
* Take full responsibility for the compliance of its activities with the procedures defined in the security policy, including their fulfilling by his registration authorities;  
* Define the responsibility of registration authorities and to oblige them to comply with established safety measures;  
* Have a list of all their assets with their classification from the point of view of the risk assessment conducted.  

The Security Policy of the Provider and the Summary of Security Assets shall be reviewed at regular intervals and always when significant changes are made to ensure their continuity, suitability, sufficiency and effectiveness.  
The Provider's management shall approve any changes that may affect the level of security provided.  
The setting up of the Provider's systems shall be regularly reviewed for changes that threaten the Provider's security policy. 

##  5.1	Physical security controls 

###  5.1.1	Site location and construction 
Technological facilities in which the Provider's basic infrastructure is located shall be located in protected areas accessible only to authorized persons and separated from other areas by appropriate security features (security doors, grilles, fixed walls, etc.). Provider equipment should consist only of equipment reserved for certification authority functions and should not serve any purpose that does not apply to this function.

###  5.1.2	Physical access 
Access Control Mechanisms for Provider's Protected Areas e. g. the areas of the highest security zone shall be secured in such a way that these spaces are protected by a security alarm and are only accessible to persons holding a security token and listed in the list of authorized persons to enter the Provider's protected areas. Provider equipment must be permanently protected from unauthorized access, even from unauthorized physical access.

###  5.1.3	Power and air conditioning 
The spaces in which the Provider's equipment is located shall be adequately supplied with electricity and air-conditioned to provide a reliable operating environment.

###  5.1.4	Water exposures 
The spaces in which the Provider's equipment is located shall be located so that they cannot be endangered by water from any source. If this is not entirely possible, measures must be taken to minimize the risk of water hazard to the premises.

###  5.1.5	Fire prevention and protection 
The spaces in which the Provider's equipment is located shall be reliably protected from direct fire sources, heat that could cause fire in the premises.

###  5.1.6	Media storage 
Media must be stored in rooms that are protected against accidental, unintentional damage (water, fire, and electromagnetism). Media containing security audit, archive, or backed up information should be stored in a site separate from CMA.

###  5.1.7	Waste disposal 
The waste arising from the operation of the Provider shall be managed in such a way that no environmental pollution is involved.

###  5.1.8	Off-site backup 
In the event of irreversible damage to the main site spaces where the Provider's infrastructure is located, it is necessary to have at least copies Provider's most important assets backed up outside this principal location.

##  5.2	Procedural controls 

###  5.2.1	Trusted roles 
Within CAs shall be defined as trustworthy roles responsible for individual aspects of trusted activities such as, for example, system administrator, security manager, internal auditor, policy maker, etc., which form the basis of trust in the whole PKI.
At the same time, responsibilities for individual roles shall be defined. 
Persons selected to hold roles that require credibility must be accountable and trusted. 
All persons in trusted roles must have no conflict of interest to ensure the impartiality of the services provided by the Provider.

###  5.2.2	Number of Individual Required per Task
For each task, the number of individuals assigned to perform each task must be identified (rule K of N). 

###  5.2.3	Identification and authentication for each role 
Each role must have a defined way of identifying and authenticating when accessing the IS of the Provider.

###  5.2.4	Roles requiring separation of duties 
Each role must have set criteria that take into account the need for separation of functions in terms of the role itself i.e. there must be roles that cannot be performed by the same individuals. 

##  5.3	Personnel controls 
Provider personnel shall be formally appointed to the trusted role by executive management responsible for security.

###  5.3.1	Qualifications, experience, and clearance requirements 
Employees in trusted roles must meet the qualification requirements, professional experience requirements, and have security clearance at the specified level or shall be in the process of requesting a security clearance respectively. Requirements for each role are described in separate sheets used to recruit new staff.
Persons in managerial positions shall
* Have appropriate training or experience in the field of trusted services provided by the Provider;  
* Be familiar with security measures for safety roles;  
* Have experience of information security and risk assessment to the extent necessary for the performance of managerial functions.  

###  5.3.2	Background check procedures 
Employee can only be included in the trusted role of the Provider if he/she has a security clearance of the specified level i.e. at least to the "Confidential" classification level or is in the process of requesting such a review respectively. 

###  5.3.3	Training Requirements and Procedures 
Some special training requirements may be specified for certain trustworthy roles of the Provider, which should be completed before or during the assignment. Topics should include the functioning of CMA software and hardware, operating and security procedures, the provisions of this CP/CPS, and so on.

###  5.3.4	Retraining frequency and requirements 
For roles where the requirements for passing the prescribed training are set, it is possible to determine the need to repeat them after completing the primary training.

###  5.3.5	Job rotation frequency and sequence 
There is no job rotation for trusted roles.

###  5.3.6	Sanctions for unauthorized actions 
Any employee failure whose result is a situation that is not in accordance with the provisions of this CP/CPS, whether it concerns negligence or bad intent, will be the subject of appropriate administrative and disciplinary proceedings by the Provider.

###  5.3.7	Independent Contractor Controls 
Where independent contractors are assigned to implement trusted roles, they must be subject to the obligations and specific requirements for these roles within the meaning of section 5.3 and are equally subject to the sanctions referred to in point 5.3.6.

###  5.3.8	Documentation supplied to personnel 
Employees in trusted roles must have the documents needed to perform the function they are assigned to, including a copy of this CP/CPS and all technical and operational documentation necessary to maintain the integrity of operation of the Provider's.

##  5.4	Audit logging procedures 
The Provider must record and have available all-important information regarding the issued Certificates during the necessary time and even after termination of operation.
Provider has to record accurate time in the trust service concerning key management, and clock synchronization. The time recorded for each event must be synchronized with UTC at least every 24 hours.

###  5.4.1	Types of events recorded 
The CA shall record at least the following events.

#### 5.4.1.1 CA certificate and key lifecycle events, including:
* Key generation, backup, storage, recovery, archival, and destruction;
* Certificate requests, renewal, and re-key requests, and revocation;
* Approval and rejection of Certificate requests;
* Cryptographic device lifecycle management events;
* Generation of Certificate Revocation Lists;
* Signing of OCSP Responses (as described in Section 4.9 and Section 4.10); and
* Introduction of new Certificate Profiles and retirement of existing Certificate Profiles.

#### 5.4.1.2 Subscriber Certificate lifecycle management events, including:
* Certificate requests, renewal, and re-key requests, and revocation;
* All verification activities stipulated in this CP and the CA's Certification Practice Statement;
* Approval and rejection of Certificate requests;
* Issuance of Certificates;
* Generation of Certificate Revocation Lists; and
* Signing of OCSP Responses (as described in Section 4.9 and Section 4.10).

#### 5.4.1.3 Security events, including:
* Successful and unsuccessful PKI system access attempts;
* PKI and security system actions performed;
* Security profile changes;
* Installation, update, and removal of software on a Certificate System;
* System crashes, hardware failures, and other anomalies;
* Firewall and router activities; and
* Entries to and exits from the CA facility.  

Log records MUST include the following elements:
* Date and time of event;
* Identity of the person making the journal record; and
* Description of the event.

###  5.4.2	Frequency for Processing and Archiving Audit Logs 
No stipulation.

###  5.4.3	Retention Period for Audit Logs 
The CA and each Delegated Third Party shall retain, for at least two (2) years:
* CA certificate and key lifecycle management event records (as set forth in Section 5.4.1) after the later occurrence of:  
   * the destruction of the CA Private Key; or
   * the revocation or expiration of the final CA Certificate in that set of Certificates that have an X.509v3 "basicConstraints" extension with the "cA" field set to "true" and which share a common Public Key corresponding to the CA Private Key;   
* Subscriber Certificate lifecycle management event records (as set forth in Section 5.4.1) after the expiration of the Subscriber Certificate;  
* Any security event records (as set forth in Section 5.4.1 ) after the event occurred.  

###  5.4.4	Protection of Audit Log 
No stipulation.

###  5.4.5	Audit Log Backup Procedure 
No stipulation.

###  5.4.6	Audit Log Accumulation System 
No stipulation.

###  5.4.7	Notification to event-causing subject 
No stipulation.

###  5.4.8	Vulnerability assessments 
The Provider's security program shall include an annual Risk Assessment that:
* Identifies foreseeable internal and external threats that could result in unauthorized access, disclosure, misuse, alteration, or destruction of any Certificate Data or Certificate Management Processes;
* Assesses the likelihood and potential damage of these threats, taking into consideration the sensitivity of the Certificate Data and Certificate Management Processes; and
* Assesses the sufficiency of the policies, procedures, information systems, technology, and other arrangements that the Provider has in place to counter such threats.

##  5.5	Records archival 

###  5.5.1	Types of records archived 
The Provider shall archive all audit logs (as set forth in Section 5.4.1).
Additionally, the Provider shall archive:
* Documentation related to the security of their Certificate Systems, Certificate Management Systems, Root CA Systems, and Delegated Third Party Systems; and
* Documentation related to their verification, issuance, and revocation of Certificate Requests and Certificates.  

Provider must also keep all audit records (logs), written records of CA events (CA key generation, subordinate CA, TSA certificate issuance, and OCSP responder certificates).
Viewing records can be allowed individual components of the Provider fully of the PMA and to the persons performing the compliance audit.

###  5.5.2	Retention period for archive 
The Provider is obliged to retain the agreement with the Holder and/or the Subscriber, and the confirmation of Certificate issuance under that agreement, for at least 7 years from the expiry of the Certificate issued under that agreement.
The Provider must archive records for at least two (2) years from the time of their creation, or for as long as required to be archived under Section 5.4.3, whichever is longer.
In addition, the Provider shall archive for at least two (2) years:
* all archived documentation relating to the security of the certification authority systems, certificate management systems, and Root CA systems,
* all archived documentation relating to the verification of Certificate issuance and revocation requests and the Certificates themselves.

###  5.5.3	Protection of archive 
No stipulation.

###  5.5.4	Archive backup procedures 
No stipulation.

###  5.5.5	Requirements for time-stamping of records 
No stipulation.

###  5.5.6	Archive collection system (internal or external) 
No stipulation.

###  5.5.7	Procedures to obtain and verify archive information 
No stipulation.

##  5.6	Key changeover 
The Provider must use its signing (private) keys only for the purpose for which they are intended. Subordinate CA private keys may be used only for signing Certificates for end users, and only for the purpose for which they are intended, or for signing certificates issued for technical purposes (e.g., OCSP responder certificates). 
The Root CA private key may be used only for signing certificates for subordinate CAs and/or technical certificates (e.g., OCSP responder certificates).

##  5.7	Compromise and disaster recovery 

###  5.7.1	Incident and compromise handling procedures 
Provider shall have an Incident Response Plan and a Disaster Recovery Plan.  
The Provider shall document business continuity and disaster recovery procedures designed to notify and reasonably protect Application Software Suppliers, Subscribers, and Relying Parties in the event of a disaster, security compromise, or business failure. The Provider is not required to publicly disclose its business continuity plans but shall make its business continuity plan and security plans available to the Provider 's auditors upon request. The Provider shall annually evaluate, review, and update these procedures.
The business continuity plan shall include:
1. The conditions for activating the plan;
2. Emergency procedures;
3. Fallback procedures;
4. Resumption procedures;
5. A maintenance schedule for the plan;
6. Awareness and education requirements;
7. The responsibilities of the individuals;
8. Recovery time objective (RTO);
9. Regular testing of contingency plans;
10. The CA's plan to maintain or restore the CA's business operations in a timely manner following interruption to or failure of critical business processes;
11. A requirement to store critical cryptographic materials (i.e., secure cryptographic device and activation materials) at an alternate location;
12. What constitutes an acceptable system outage and recovery time;
13. How frequently backup copies of essential business information and software are taken;
14. The distance of recovery facilities to the CA's main site; and
15. Procedures for securing its facility to the extent possible during the period of time following a disaster and prior to restoring a secure environment either at the original or a remote site.

###  5.7.2	Recovery Procedures if Computing resources, software, an/or data are corrupted 
No stipulation.

###  5.7.3	Recovery Procedures after Key Compromise 
No stipulation.

###  5.7.4	Business continuity capabilities after a disaster 
No stipulation.

##  5.8	CA or RA termination 
If the Provider terminates its operations for reasons other than force majeure events (e.g., natural disaster, state of war, decision of a public authority, etc.), the procedure set out in Section 5.7 shall be followed.

Before terminating the provision of services, the Provider must:

* In an appropriate manner, at least 6 months in advance, notify the supervisory authority, the Holders of all valid Certificates it has issued, Relying Parties, and the public of the planned termination of its activities. This notification must be made via the Provider's website, email, regular mail, Registration Authorities, and/or electronic media and the press.
* Terminate any mandate agreements, authorizations, powers of attorney, etc., under which other legal entities could act on behalf of the Provider.
* Conclude an agreement with another CA to ensure continuity in the provision of trust services, where possible.
* In accordance with the PMA's instructions, collect and prepare for archiving all documents related to the provided trust services.
* Perform a compliance check with personal data protection regulations [14].
* Decommission all private keys, including all copies thereof, in such a manner that they cannot be restored in any way.  

After termination of its activities, the Provider shall not issue any Certificates and shall ensure demonstrably that the Provider's private keys cannot be reused.  
Before termination of its activities, each RA shall provide archived data to the Provider's designated unit in accordance with the PMA's instructions.  
The Provider must have a solution in place to cover all costs associated with meeting the minimum termination requirements in the event of bankruptcy or another cause where it is unable to cover the costs from its own resources, in accordance with applicable bankruptcy legislation.

#  6.	TECHNICAL SECURITY CONTROLS 
The technical part of the Provider's infrastructure (hardware and software) must consist only of secure systems and official software. The infrastructure architecture of the provider must be designed with components that meet safety standards at the level of current knowledge.  
Particular attention must be paid to the cryptographic module (HSM), which serves to generate, store and use the Provider's private keys and is one of the most vulnerable assets. The private keys of the provider must be stored in an HSM module that is certified at least according to the FIPS 140-2 Level 3 standard.  
The Provider must use a combination of physical, logical and procedural measures to ensure its security to protect its private key.  
The Provider's system must contain a device for the continuous detection, monitoring, and signaling of unauthorized and unusual attempts to access its resources.  
Publishing applications must provide access control before trying to add or delete a Certificate or modifying other associated data.  
Revocation status reporting must provide access control before attempts to modify revocation status information.  
All Provider features that use a computer network must be secured against unauthorized access and other malicious activities.


##  6.1	Key pair generation and installation 

###  6.1.1	Key pair generation 

#### 6.1.1.1	CA key pair generation
Generation and installation of the Provider’s key pair must be performed in a standardized manner, which is described in detail in the Provider’s documentation in accordance with the requirements in Section 6.1.1.1 of the SMIME BR [1]. 
The generation method must provide sufficient assurance in the generation procedure, and the entire process must be recorded in writing. Key generation must be conducted by authorized persons of the Provider assigned to roles that are authorized to participate in the key and request generation ceremony. Key generation must be performed in a secure device for the storage of cryptographic keys.

For key pairs intended for the operator of the Root CA, the Provider must:
* prepare and follow a script for generating the key pair,
* ensure either that:
  *  the key pair is generated in the presence of a qualified auditor, or
  *  the entire key pair generation process is video-recorded for subsequent auditor review.

The Provider must further ensure that it:
* generates the CA key pair in a physically secured environment, as described in this CP/CPS, applying the K/N principle;
* generates the CA key pair using persons in trusted roles according to the principles of multi-person control and split knowledge — the K/N principle;
* generates the CA key pair within cryptographic modules that meet the relevant technical and commercial requirements set out in this CP/CPS;
* records the CA key pair generation activities; and
* maintains effective controls to provide reasonable assurance that the private key was generated and protected in accordance with the procedures described in this CP/CPS and, where applicable, in its key generation script.

#### 6.1.1.2	RA key pair generation
No stipulation. 

#### 6.1.1.3 Subscriber key pair generation
The Provider’s RA must reject a Certificate issuance request if one or more of the following conditions are met:
* the key pair does not meet the requirements set out in Section 6.1.5 and/or Section 6.1.6;
* there is clear evidence that the method used to generate the key pair is flawed;
* the Provider has been informed that the private key has been compromised, for example as described in Section 4.9.1.1.

The Provider’s RA does not generate a key pair on behalf of the Holder.

###  6.1.2	Private key delivery to subscriber
Parties other than the Subscriber shall not archive the Subscriber Private Key without authorization by the Subscriber.

If the CA or any of its designated RAs become aware that a Subscriber's Private Key has been communicated to a person or organization not authorized by the Subscriber, then the CA shall revoke all Certificates that include the Public Key corresponding to the communicated Private Key.

###  6.1.3	Public key delivery to Certificate issuer 
No stipulation.

###  6.1.4	CA public key delivery to relying parties 
No stipulation.

###  6.1.5	Key sizes 
For RSA key pairs the Provider shall:
* Ensure that the modulus size, when encoded, is at least 2048 bits; and
* Ensure that the modulus size, in bits, is evenly divisible by 8.


###  6.1.6	Public key parameters generation and quality checking
The parameters and quality of the Provider’s public keys (Root and Subordinate CAs, cross-certificates) are determined by the PMA, and quality assurance is performed during the key generation ceremony. The Provider must use cryptographic hardware modules for key generation and storage that meet the requirements of FIPS 186-2, ensuring random generation of RSA keys with a minimum size of 2048 bits.

For an RSA key pair, the Provider must confirm that the public exponent value is an odd number equal to 3 or greater. In addition, the public exponent should be in the range between 2^16 + 1 and 2^256 − 1. The module should also have the following characteristics: it is an odd number, not a prime power, and has no factors smaller than 752 (see NIST SP 800-89, Section 5.3.3) [18]. 


###  6.1.7	Key usage purposes (as per X.509 v3 key usage field) 
Private Keys corresponding to Root CA Certificates shall not be used to sign Certificates except in the following cases:
* Self-signed Certificates to represent the Root CA itself;
* Certificates for Subordinate CAs and Cross Certificates;
* Certificates for infrastructure purposes (administrative role certificates, internal CA operational device certificates); and
* Certificates for OCSP Response verification.

##  6.2	Private Key Protection and Cryptographic Module Engineering Controls 
The Provider shall implement physical and logical safeguards to prevent unauthorized Certificate issuance. Protection of the CA Private Key outside the validated system or device specified above shall consist of physical security, encryption, or a combination of both, implemented in a manner that prevents disclosure of the Private Key. 

The Provider shall encrypt its Private Key with an algorithm and key-length that, according to the state of the art, are capable of withstanding cryptanalytic attacks for the residual life of the encrypted key or key part.

###  6.2.1	Cryptographic module standards and controls 
The Provider must use hardware cryptographic modules to protect its private keys (Root CAs, Subordinate CAs) that are certified at least to FIPS 140-2 Level 3. The modules must be stored in secure areas accessible only to persons in trusted roles.
The Provider’s private keys may be used exclusively for signing Certificates and CRLs issued by the Provider.

CA equipment must be continuously protected against unauthorized access, including unauthorized physical access.
The HSM module must provide protection against the interception of electromagnetic emissions.

The Provider’s CA private keys:
* are stored and used exclusively within an HSM that meets the applicable security requirements;
* are activated only by authorized personnel under the K/N control mode;
* are never exported from HSM in unencrypted form. 

###  6.2.2	Private key (K out of N) multi-person control
For operations involving the Provider’s private keys (e.g., generation, backup, destruction), the required number of authorized persons must always be present in accordance with the “K of N” principle.

###  6.2.3	Private key escrow
No stipulation.

###  6.2.4	Private key backup 
The Provider’s private keys must be generated and stored within hardware cryptographic modules. Where transfer is necessary for backup and recovery purposes, private keys must always be transferred in encrypted form. Transfer of private keys and their recovery into another hardware cryptographic module may be performed only by authorized staff members in accordance with the rules set out in Section 6.2.2.

###  6.2.5	Private key archival 
Parties other than the Provider shall not archive the Subordinate CA Private Keys without authorization by the Provider.

###  6.2.6	Private key transfer into or from a cryptographic module 
If the Issuing CA of the Provider generated the Private Key on behalf of the Subordinate CA, then the Issuing CA shall encrypt the Private Key for transport to Subordinate CA.

If the Issuing CA becomes aware that Subordinate CA's Private Key has been communicated to an unauthorized person or an organization not Affiliated with the Subordinate CA, then the Issuing CA shall revoke all Certificates that include the Public Key corresponding to the communicated Private Key.

###  6.2.7	Private key storage on cryptographic module 
The Provider shall protect its Private Key in a system or device that has been validated as meeting at least FIPS 140-2 level 3, FIPS 140-3 level 3, or an appropriate Common Criteria Protection Profile or Security Target, EAL 4 (or higher), which includes requirements to protect the Private Key and other assets against known threats.

###  6.2.8	Method of Activating Private Key
The Provider’s private keys may be activated only by authorized persons in accordance with Section 6.2.2.

During activation, each authorized person, from the required number of authorized persons, must insert their smart card into the HSM module and enter the corresponding password.

The Certificate Holders to whom the Provider has issued a Certificate for the relevant public key are solely responsible for protecting their private keys. The Provider must recommend to all Certificate Holders that they protect their private keys by using a strong password to prevent misuse of their private key.

###  6.2.9	Method of Deactivating Private Key 
Deactivation of a private key in the HSM module may be performed only by an authorized person (CA administrator), or the keys may be deactivated automatically upon session termination or loss of electrical power to the HSM module.

###  6.2.10	Method of Destroying Private Key 
The Provider must, through technical and organizational measures, ensure that the Provider’s private key cannot be used after the end of its life cycle. A record of the termination of the CA private key life cycle and the adopted technical and organizational measures must be created and signed by all actors present.

###  6.2.11	Cryptographic Module rating 
No stipulation.

##  6.3	Other aspects of key pair management 

###  6.3.1	Public key archival 
No stipulation.

###  6.3.2	Certificate operational periods and key pair usage periods 
The validity of the Certificate issued by the Provider and the usability of the key pair shall not exceed the following:
| Certificate type| Validity <br> (minimum)    | Validity<br>(maximum)|
|-----------------|:--------------------------:|:--------------------:|
| Root CA         | 2922 days                  |  9132 days           |
| Subordinate CA  | -                          |  2560 days           |
| STRICT or MULTIPURPOSE<br> S/MIME certificate |-|825 days            |

For the purpose of calculations, a day is measured as 86,400 seconds. Any amount of time greater than this, including fractional seconds and/or leap seconds, shall represent an additional day.


##  6.4	Activation data 
###  6.4.1	Activation data generation and installation 
The activation data for the RA staff member’s private key is chosen by the RA staff member themselves immediately after taking over the device, before its first use for accessing the Provider’s IS via the RA Client application. 

###  6.4.2	Activation data protection 
The RA staff member is solely responsible for protecting the RA staff member’s private keys.

When issuing the Certificate, each RA staff member is informed by the Provider’s responsible person of the need to protect the private key with a strong password in order to prevent its misuse throughout the entire period of its use.

###  6.4.3	Other aspects of activation data
No stipulation.

##  6.5	Computer security controls

###  6.5.1	Specific computer security technical requirements 
The Provider must perform all trust service provider functions using a trusted system that meets the requirements defined in the security project of the Provider’s IS.

A Provider issuing Certificates must meet the specific information security requirements for a trust service provider as defined in ETSI EN 319 411-1 [6].

All systems must be regularly checked for the presence of malicious code and protected against spyware and viruses.
The Provider has implemented multi-factor authentication for all RA staff members who are able to directly cause a Certificate to be issued.

###  6.5.2	Computer security rating
No stipulation.

##  6.6	Life cycle technical controls

###  6.6.1	System development controls 
No stipulation.

###  6.6.2	Security management controls 
No stipulation.

###  6.6.3	Life cycle security controls
No stipulation.

##  6.7	Network security controls
The CA/Browser Forum's Network and Certificate System Security Requirements [19] are incorporated by reference as if fully set forth herein.

###  6.8	Time-stamping 
No stipulation.

##  7.	CERTIFICATE, CRL, AND OCSP PROFILES 

##  7.1	Certificate profile 
The Provider shall meet the technical requirements set forth in Section 2.2 , Section 6.1.5, and Section 6.1.6.

The Provider shall generate non-sequential Certificate serial numbers greater than zero (0) and less than 2^159 containing at least 64 bits of output.

###  7.1.1	Version number 
This CP/CPS only allows issuing Certificates conforming to X.509 version 3.

###  7.1.2	Certificate content and extensions; application of RFC 6818 
This section specifies the additional requirements for Certificate content and extensions for Certificates, taking into account the wording of RFC 6818 [20]

#### 7.1.2.1 Root CA certificates
Algorithms and key lengths applied in the Root Certificate of the Provider

|  | |
| :--- | :--- |
| Signature AlgorithmName:|**sha256RSA**|
| Public key:|**RSA, length 4 096 bits**|

Table 4: Content of items in the Root Certificate of the Provider     

|Name abbr.|OID     |Name       |Content  |
|:-----:   |:------:|:---------:|:-------:|
|C         |2.5.4.6 |countryName|SK       |
|L         |2.5.4.7 |localityName|Bratislava|
|O         |2.5.4.10|organizationName|Disig a.s.|
|CN        |2.5.4.3 |commonName  |depending on the CA type ¹ |

¹ The CN shall contain the business name of the certification authority t. j. CA Disig complemented as required root distinguishing name of CA Disig with e.g. Root R4 etc.

Table 5: Certificate extensions in root CA SMIME Certificates  

|Extension / OID|Presence  |Critical  |
|---------------|:--------:|:--------:|
|basicConstraints / 2.5.29.19|YES|YES|
|keyUsage / 2.5.29.15|YES|YES|
|subjectKeyIdentifier / 2.5.29.14|YES|NO|

#### 7.1.2.2 Subordinate CA certificates

Algorithms and key lengths applied in the subordinate CA  
|  | |
| :--- | :--- |
| Signature AlgorithmName:|**sha256RSA**|
| Public key:|**RSA, minimal length 2 048 bit**|
|Validity of subordinate CA|maximum 7 years|

Table 6: The content of the items in the SMIME Certificate of the Subordinate CA  
|Name abbr.|OID|Name|Content|
|:----------:|:---:|:----:|:-------:|
|C|2.5.4.6|countryName|SK|
|L|2.5.4.7|localityName|Bratislava|
|O|2.5.4.10|organizationName|Disig a.s.|
|CN|2.5.4.3|commonName|depending on the CA type ²|

² The CN shall contain the business name of the certification authority e. g. CA Disig complemented as required root distinguishing name of CA Disig with e.g., R4I1 SMIME Certification Service etc.
 
Table 7: Certificate extensions in subordinate CA  
|Extension / OID|Presence|Severity|
|---------------|:--------:|:--------:|
|certificatePolicies / 2.5.29.32|YES|NO|
|crlDistributionPoints / 2.5.29.31|YES|NO|
|authorityInfoAccess / 1.3.6.1.5.5.7.1.1|YES (SHOULD)|NO| 
|basicConstraints / 2.5.29.19|YES|YES|
|keyUsage / 2.5.29.15|YES|YES|
|extKeyUsage /  2.5.29.37|YES|NO|
|authorityKeyIdentifier / 2.5.29.35|YES|NO| 
|subjectKeyIdentifier / 2.5.29.14|YES|NO|

The cRLDistributionPoints extension contains the HTTP URL of the CA’s CRL service as specified in Section 2.2.3 of this CP/CPS.

#### 7.1.2.3	Subscriber Certificates
For details on the content of the distinguishing name (DN) of each type of Certificate issued under this CP/CPS, refer to the section 7.1.4.2.

The extensions used in all types of issued certificates are listed in Table 8.

Table 8: Basic extensions in subscriber Certificates   
|Extension name / <br>ASN.1 name and OID|Description|Presence|Critical |
|-----------------------------|:---------|:------:|:-------:|
|Certificate Policies<br>{id-ce-certificatePolicies}<br>{2.5.29.32}|It shall include exactly one of the reserved policyIdentifiers listed in Section 7.1.6.1.|SHALL|NO|
|CRL Distribution Points<br>{id-ce-CRLDistributionPoints}<br>{2.5.29.31}|Strict and Multipurpose profiles shall contain at least one distributionPoint <br> whose fullName value includes a GeneralName of type uniformResourceIdentifier <br> that includes a URI where the Issuing CA's CRL can be retrieved.<br>Every uniformResourceIdentifier shall have the URI scheme HTTP. Other schemes shall not be present.|SHALL|NO|
|AuthorityInfoAccess<br>{id-pe-authorityInfoAccess}<br>{1.3.6.1.5.5.7.1.1}|1.	id-ad-ocsp<br> The extension may contain one or more accessMethod values of type id-ad-ocsp that specifies the URI<br> of the Issuing CA's OCSP responder. Strict and Multipurpose profiles shall for every accessMethod<br> have the URI scheme HTTP. Other schemes shall not be present.<br> 2.	id-ad-caIssuers<br> The extension should contain at least one accessMethod value of type id-ad-caIssuers that specifies<br> the URI of the Issuing CA's Certificate. Strict and Multipurpose profiles shall for every accessMethod<br> have the URI scheme HTTP. Other schemes shall not be present.|SHOULD|NO|
|basicConstraints<br>{id-ce-basicConstraints}<br>{2.5.29.19}|This extension may be present. The cA field shall not be true. pathLenConstraint field shall not be present.|SHOULD|NO|
|Key Usage<br>{id-ce-keyUsage}<br>{2.5.29.15}|Strict profile: For signing only, bit positions shall be set for digitalSignature and may be set<br> for nonRepudiation. For key management only, bit positions shall be set for keyEncipherment.<br> For dual use, bit positions shall be set for digitalSignature and keyEncipherment and may be<br> set for nonRepudiation.<br> Multipurpose profile: applies same as for Strict profil with modification that for key<br> management and dual use may be set for dataEncipherment. Other bit positions shall not be set.|SHALL|SHOULD|
|Extended Key Usage<br>{id-ce-extKeyUsage}<br>{2.5.29.37}|Strict profile: id-kp-emailProtection shall be present. Other values shall not be present<br>Multipurpose profile: id-kp-emailProtection shall be present. Other values may be present.<br>Any profile: The values id-kp-serverAuth, id-kp-codeSigning, id-kp-timeStamping,<br> and anyExtendedKeyUsage shall not be present.|SHALL|NO|
|Authority Key Identifier<br>{id-ce-authorityKeyIdentifier}<br>{2.5.29.35}|The keyIdentifier field shall be present. authorityCertIssuer and authorityCertSerialNumber<br> fields shall not be present.|SHALL|NO|
|subjectAltName<br>id-ce-subjectAltName<br>{2.5.29.32}|The value of this extension shall be encoded as specified in Section 7.1.4.2.1.|SHALL|NO|
|Subject Key Identifier<br>{id-ce-subjectKeyIdentifier}<br>{2.5.29.14}|It should contain a value that is derived from the Public Key included in the Subscriber Certificate.|SHOULD|NO|

#### 7.1.2.4	All Certificates
All fields and extensions shall be set in accordance with RFC 5280 [2]. The Provider shall not issue a Certificate that contains a keyUsage flag, extKeyUsage value, Certificate extension, or other data not specified in Section 7.1.2.1, Section 7.1.2.2, or Section 7.1.2.3 unless the Provider is aware of a reason for including the data in the Certificate. 
If the Provider includes fields or extensions in a Certificate that are not specified but are otherwise permitted by these Requirements, then the Provider shall document the processes and procedures that the Provider employs for the validation of information contained in such fields and extensions in its CP/CPS.

Provider shall not issue a Certificate with:
* Extensions that do not apply in the context of the public Internet 
* Field or extension values which have not been validated according to the processes and procedures described in this CP/CPS.

###  7.1.3	Algorithm object identifiers 

#### 7.1.3.1	SubjectPublicKeyInfo
The following requirements apply to the “subjectPublicKeyInfo” field within a Certificate. No other encodings are permitted.

##### 7.1.3.1.1	RSA
The Provider shall indicate an RSA key using the “rsaEncryption (OID: 1.2.840.113549.1.1.1)” algorithm identifier. The parameters shall be present and shall be an explicit “NULL”.

The Provider shall not use a different algorithm, such as the “id-RSASSA-PSS (OID: 1.2.840.113549.1.1.10)” algorithm identifier, to indicate an RSA key.

When encoded, the AlgorithmIdentifier for RSA keys shall be byte-for-byte identical with the following hex-encoded bytes: 300d06092a864886f70d0101010500

##### 7.1.3.1.2	ECDSA
The Provider does not issue Certificates for this type of keys.

##### 7.1.3.1.3	EdDSA
The Provider does not issue Certificates for this type of keys.

##### 7.1.3.2	Signature AlgorithmIdentifier
All objects signed by a CA Private Key shall conform to these requirements on the use of the “AlgorithmIdentifier” or “AlgorithmIdentifier” -derived type in the context of signatures.

In particular, it applies to all of the following objects and fields:
*	The “signatureAlgorithm” field of a Certificate.
*	The “signature” field of a “TBSCertificate” (for example, as used by a Certificate).
*	The “signatureAlgorithm” field of a “CertificateList”
*	The “signature” field of a “TBSCertList”
*	The “signatureAlgorithm” field of a “BasicOCSPResponse”.  

No other encodings are permitted for these fields.

##### 7.1.3.2.1	RSA
The CA of the provider shall use one of the following signature algorithms and encodings. When encoded, the “AlgorithmIdentifier” shall be byte-for-byte identical with the specified hex-encoded bytes.
|AlgorithmIdentifier|Encoding|
|-------------------------------|:---------|
|RSASSA-PKCS1-v1_5 with SHA-256|300d06092a864886f70d01010b0500|
|RSASSA-PKCS1-v1_5 with SHA-384|300d06092a864886f70d01010c0500|
|RSASSA-PKCS1-v1_5 with SHA-512|300d06092a864886f70d01010d0500|
|RSASSA-PSS with SHA-256, <br>MGF-1 with SHA-256, and<br> a salt length of 32 bytes|304106092a864886f70d01010a3034a00<br>f300d06096086480165030402010500a11<br>c301a06092a864886f70d010108300d0<br>6096086480165030402010500a203020120|
|RSASSA-PSS with SHA-384, <br>MGF-1 with SHA-384, and<br>a salt length of 48 bytes|304106092a864886f70d01010a3034a00<br>f300d06096086480165030402020500a11<br>c301a06092a864886f70d010108300d06096<br>086480165030402020500a203020130|
|RSASSA-PSS with SHA-512, <br>MGF-1 with SHA-512, and<br> a salt length of 64 bytes|304106092a864886f70d01010a3034a00<br>f300d06096086480165030402030500a11<br>c301a06092a864886f70d010108300d06096<br>086480165030402030500a203020140|

##### 7.1.3.2.2	ECDSA
The Provider does not use this type of signature algorithm. 

##### 7.1.3.2.3	EdDSA
The Provider does not use this type of signature algorithm. 

###  7.1.4	Name Forms 
Attribute values shall be encoded according to RFC 5280 [2].

#### 7.1.4.1	Name encoding
For every valid Certification Path (as defined by RFC 5280 [2], Section 6):
* For each Certificate in the Certification Path, the encoded content of the “Issuer Distinguished Name” field of a Certificate shall be byte-for-byte identical with the encoded form of the “Subject Distinguished Name” field of the Issuing CA Certificate.
* For each CA Certificate in the Certification Path, the encoded content of the “Subject Distinguished Name” field of a Certificate shall be byte-for-byte identical among all Certificates whose “Subject Distinguished Names” can be compared as equal according to RFC 5280 [2], Section 7.1, and including expired and revoked Certificates.

#### 7.1.4.2	Subject information - subscriber Certificates
By issuing the Certificate, the CA of the Provider represents that it followed the procedure set forth in this CP/CPS to verify that, as of the Certificate's issuance date, all of the Subject Information was accurate.

The Provider shall not include a Mailbox Address in a Mailbox Field except as verified in accordance with Section 3.2.2.
Subject attributes shall not contain only metadata such as '.', '-', and ' ' (i.e., space) characters, and/or any other indication that the value is absent, incomplete, or not applicable.

##### 7.1.4.2.1	Subject alternative name extension
|Certificate field|Required / Optional|Contents| 
|-------------------------------|:---------:|:---------|
|extensions: subjectAltName|shall be present|This extension shall contain at least one GeneralName entry of the following types:<br>• Rfc822Name and/or <br>• otherName of type id-on-SmtpUTF8Mailbox, encoded in accordance with RFC 8398|

##### 7.1.4.2.2	Subject distinguished name fields
The Provider issues these types of SMIME Certificates:
* S/MIME digital signature certificate
* Individual-validated (STRICT and MULTIPURPOSE)
* Sponsor-validated (STRICT and MULTIPURPOSE)
* S/MIME digital certificate for seal (STRICT and MULTIPURPOSE).

The following subject distinguished name fields are included in the specified types of Certificates: 

|Subject distinguished<br> name field | |SMIME digital signature certificate| | | S/MIME digital certificate for seal| |
|-------------------------------|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|
| | Individual-validated| Individual-validated|Sponsor-validated |Sponsor-validated |Organization-validated|Organization-validated |
| |Multipurpose|Strict|Multipurpose|Strict|Multipurpose|Strict|
|commonName   |YES|YES|YES|YES|YES|YES|
|givenName    |YES|YES|YES|YES| | |
|surname      |YES|YES|YES|YES| | |
|serialNumber |YES|YES|YES|YES| | |
|countryName  |YES|YES|YES|YES|YES|YES|
|organizationName| | |YES|YES|YES|YES|
|organizationIdentifier| | |YES|YES|YES|YES|
|localityName | | |YES|YES|YES|YES|
|emailAddress |YES|YES|YES|YES|YES|YES|

**a)** Certificate Field: “_subject:commonName (OID 2.5.4.3)_”    
This attribute shall contain one of the following values verified in accordance with Section 3.2.
|Certificate type      |Contents                                    |
|----------------------|:------------------------------------------:|
|Organization-validated|subject:organizationName Mailbox Address    |
|Sponsor-validated     |Personal Name, Pseudonym, or Mailbox Address|
|Individual-validated  |Personal Name, Pseudonym, or Mailbox Address|

The Personal Name should be presented as “_subject:givenName_” and/or “_subject:surname_”. The Personal Name may be in the Subject's preferred presentation format or a format preferred by the CA or Enterprise RA but shall be a meaningful representation of the Subject’s name as verified under Section 3.2.4.

If present, the Mailbox Address shall contain a rfc822Name or otherName value of type id-on-SmtpUTF8Mailbox from extensions:subjectAltName.

Like all other Certificate attributes, “_subject:commonName_” and “_subject:emailAddress_” shall comply with the attribute upper bounds defined in RFC 5280 [2].  

**b)** Certificate Field: “_subject:commonName (OID 2.5.4.3)_”  
If present, field shall contain the Subject's full legal organization (legal person) name as verified under Section 3.2.3. 
RA of the provider may include information in this field that differs slightly from the verified name, such as common variations or abbreviations, or removing character “,” (comma) or character substitutions according to section 3.1.4.1. 

**c)** Certificate Field: “_subject:organizationalUnitName (OID: 2.5.4.11)_”   
The provider does not include this field in SMIME Certificates.

**d)** Certificate Field: “_subject:organizationIdentifier (2.5.4.97)_”  
If present, the field shall contain a Registration Reference for a Legal Entity assigned in accordance to the identified Registration Scheme.

The “_subject:organizationIdentifier_” shall be encoded as a PrintableString or UTF8String.

The Registration Scheme identified in the Certificate shall be the result of the verification performed in accordance with Section 3.2.3. 

The Registration Scheme shall be identified using the following structure in the presented order:
* 3-character Registration Scheme identifier (e.g. NTR);
* 2-character ISO 3166 country code for the nation in which the Registration Scheme is operated, or if the scheme is operated globally ISO 3166 code "XG" shall be used.

The following Registration Schemes are recognized as valid under SMIME BR [1]  for use in the “subject:organizationIdentifier” attribute :
* NTR: For an identifier allocated by a national or state trade register to the Legal Entity named in the subject:organizationName.
* VAT: For an identifier allocated by the national tax authorities to the Legal Entity named in the subject:organizationName.
* PSD: For a national authorization number allocated to the payment service provider named in the subject:organizationName under Payments Services Directive (EU) 2015/2366. This shall use the extended structure as defined in ETSI TS 119 495, clause 5.2.1.
* LEI: For a Legal Entity Identifier as specified in ISO 17442 for the entity named in the subject:organizationName. The 2-character ISO 3166 country code shall be set to 'XG'.

The country code used in the Registration Scheme identifier shall match that of the “subject:countryName” in the Certificate as specified in Section 7.1.4.2.2.  

**e)** Certificate Field: “_subject:givenName (2.5.4.42)_” and/or “_subject:surname (2.5.4.4)_”  
If present, the “_subject:givenName_” field and “_subject:surname_” field shall contain a Natural Person Subject’s name as verified under Section 3.2.4. Subjects with a single legal name shall provide the name in the “_subject:surname_” attribute. The “_subject:givenName_” and/or “_subject:surname_” shall not be present if the “_subject:pseudonym_” is present.

**f)** Certificate Field: “_subject:pseudonym (2.5.4.65)_”  
The Provider does not include this field in SMIME Certificates.  

**g)** Certificate Field: “_subject:serialNumber (2.5.4.5)_”  
If present, it may be used to contain an identifier assigned by the CA or RA to identify and/or to disambiguate the Subscriber.

In addition, the "_subject:serialNumber_" may be used in the Sponsor-validated and Individual-validated profiles to contain a Natural Person Identifier as described in ETSI EN 319 412-1 Section 5.1.3 [21].

The Provider shall confirm that the Individual represented by the Natural Person Identifier is the same as the Certificate Subject.

**h)** Certificate Field: “_subject:emailAddress (1.2.840.113549.1.9.1)_”  
It shall contain a single Mailbox Address as verified under Section 3.2.2.  

**i)** Certificate Field: “_subject:title (2.5.4.12)_”
The Provider does not include this field in SMIME Certificates.  

**j)** Certificate Field: Number and street: “_subject:streetAddress (OID: 2.5.4.9)_”
The Provider does not include this field in SMIME Certificates.  

**k)** Certificate Field: “_subject:localityName (OID: 2.5.4.7)_”
If present, it shall contain the Subject's locality information as verified under Section 3.2.3 for “Organization-validated” and “Sponsor-validated” Certificate Types or Section 3.2.4 for “Individual-validated” Certificate Types.  

**l)** Certificate Field: “_subject:stateOrProvinceName (OID: 2.5.4.8)_”
The Provider does not include this field in SMIME Certificates.  

**m)** Certificate Field: “_subject:postalCode (OID: 2.5.4.17)_”  
The Provider does not include this field in SMIME Certificates.  

**n)** Certificate Field: “_subject:countryName (OID: 2.5.4.6)_”  
If present, it shall contain the two-letter ISO 3166-1 country code associated with the location of the Subject verified under Section 3.2.3 for “Organization-validated” and “Sponsor-validated” Certificate Types or Section 3.2.4 for “Individual-validated” Certificate Types.

#### 7.1.4.3	Subject information - root certificates and subordinate CA certificates
By issuing a Subordinate CA Certificate, the Provider represents that it followed the procedure set forth in this CP/CPS to verify that, as of the Certificate's issuance date, all of the Subject Information was accurate.  

##### 7.1.4.3.1	Subject distinguished name fields  
**a)** Certificate Field: “_subject:commonName (OID 2.5.4.3)_”  
This field shall be present and it should contain an identifier for the Certificate such that the Certificate's Name is unique across all Certificates issued by the Issuing CA.   

**b)** Certificate Field: “_subject:organizationName (OID 2.5.4.10)_”  
This field shall be present and it shall contain either the Subject CA's name or DBA as verified under Section 3.2.3.2.2. The Provider may include information in this field that differs slightly from the verified name, such as common variations or abbreviations.  

**c)** Certificate Field: “_subject:countryName (OID: 2.5.4.6)_”  
This field shall be present and it shall contain the two‐letter ISO 3166‐1 [22] country code for the country in which the Provider's place of business is located.  

**d)** Other Subject Attributes  
Other attributes may be present within the subject field. If present, other attributes shall contain information that has been verified by the Provider

###  7.1.5	Name constraints 
For a Subordinate CA Certificate to be considered Technically Constrained, the Certificate shall include an Extended Key Usage (EKU) extension specifying all extended key usages for which the Subordinate CA Certificate is authorized to issue Certificates.

The anyExtendedKeyUsage KeyPurposeId shall not appear within this extension.

###  7.1.6	Certificate policy object identifier 
This section describes the content requirements for the Root CA, Subordinate CA, and Subscriber Certificates as they relate to the identification of Certificate Policy.

#### 7.1.6.1	Reserved Certificate policy identifiers
These certificate policy identifiers defined by the CA/Browser Forum are reserved for use by the Provider to confirm that the Certificate complies with these requirements:
|Certificate type                                                    |Subtype          |Policy Identifier|
|----------------------|:-------------------------------------------:|:---------------------------------:|
|S/MIME digital signature certificate type <br>„Individual-validated“|STRICT           |2.23.140.1.5.4.3 |
|S/MIME digital signature certificate type <br>„Individual-validated“|MULTIPURPOSE     |2.23.140.1.5.4.2 |
|S/MIME digital signature certificate type <br>Sponsor-validated“    |STRICT           |2.23.140.1.5.3.3 |
|S/MIME digital signature certificate type <br>Sponsor-validated“    |MULTIPURPOSE     |2.23.140.1.5.3.2 |
|S/MIME digital certificate for seal                                 |STRICT           |2.23.140.1.5.2.3 |
|S/MIME digital certificate for seal                                 |MULTIPURPOSE     |2.23.140.1.5.2.2 |

#### 7.1.6.2	Root CA certificates
A Root CA Certificate should not contain the certificatePolicies extension. If present, the extension shall conform to the requirements set forth for Certificates issued to Subordinate CAs in Section 7.1.6.3.  

#### 7.1.6.3	Subordinate CA certificates
A Certificate issued to a Subordinate CA that is an Affiliate of the Issuing CA shall include a set of policy identifiers from one of the two options below:
* One or more explicit policy identifiers defined in Section 7.1.6.1 that indicate Subordinate CA's adherence to and compliance with SMIME BR [1] and may contain one or more identifiers documented by the Subordinate CA in this CP/CPS; or  
* The “anyPolicy (2.5.29.32.0)” identifier.

The Subordinate CA and the Issuing CA shall represent, in their CP/CPS, that all Certificates containing a policy identifier indicating compliance with SMIME BR [1] are issued and managed in accordance with these Requirements.

#### 7.1.6.4	Subscriber certificates
A Certificate issued to an end user must contain, in the certificatePolicies extension, one of the policy identifiers listed in Section 7.1.6.1.  
In addition, the Certificate will also contain the identifier of this CP/CPS defined by the Provider in the form OID=1.3.158.35975946.0.0.0.1.11, as well as the URI address where the applicable policy is available.

###  7.1.7	Usage of Policy Constraints extension 
No stipulation.

###  7.1.8	Policy qualifiers syntax and semantics 
No stipulation.

###  7.1.9	Processing semantics for the critical Certificate Policies extension 
No stipulation.

##  7.2	CRL profile 

###  7.2.1	Version number 
All CRLs issued by the Provider shall conform to RFC 5280 and shall be Version 2.

###  7.2.2	CRL and CRL entry extensions 
Table 9 lists the CRL extensions that were issued by the CAs of the Provider to which this CP applies, along with information on their presence and criticality.  

Table 9: CRL extensions 
|Extension name                             |Required|Critical|
|-------------------------------------------|:------:|:------:|
|Authority Key Identifier<br>(OID 2.5.29.35)|YES     |NO      |
|CRL Number<br>(OID 2.5.29.20)              |YES     |NO      |
|ReasonCode<br>(OID 2.5.29.21)              |YES*    |NO      |

 *If a CRL entry is for a Root CA or Subordinate CA Certificate, including Cross Certificates, this CRL entry extension shall be present. If a CRL entry is for a Certificate not technically capable of causing issuance, this CRL entry extension should be present, but may be omitted, subject to the following requirements.

The CRLreason of certificateHold (6) SHALL NOT be used for Root CA or Subordinate CA Certificates.
The CRLReason indicated shall not be unspecified (0). If the reason for revocation is unspecified, CAs shall omit the reasonCode entry extension.

The Repository may include CRL entries that have a CRLreason of certificateHold (6) for Certificates that include the Certificate Policy identifiers for Legacy or Multipurpose Generations. The Repository shall not include CRL entries that have a CRLreason of certificateHold (6) for Certificates that include the Certificate Policy identifiers for the Strict Generation.

If a reasonCode CRL entry extension is present, the CRLReason SHALL indicate the most appropriate reason for revocation of the Certificate, as defined by the CA within this CP/CPS.
If present, the reasonCode (OID 2.5.29.21) extension shall not be marked critical.  
The CRLs are published in the Repository at the locations defined in Section 2.2.3.  

##  7.3	OCSP profile 
If an OCSP response is for a Root CA or Subordinate CA Certificate, including Cross Certificates, and that Certificate has been revoked, then the revocationReason field within the RevokedInfo of the CertStatus SHALL be present.
The CRLReason indicated SHALL contain a value permitted for CRLs, as specified in Section 7.2.2.

###  7.3.1	Version number 
No stipulation.

###  7.3.2	OCSP extensions 
Table 10 contains possible extensions in the OCSP responses of the Provider's OCSP Responder, their reporting obligation, and their criticality.

Table 10: OCSP response extensions
|Extension name                                  |Required|Critical|
|------------------------------------------------|:------:|:------:|
|id-pkix-ocsp-nonce<br>(OID 1.3.6.1.5.5.7.48.1.2)|YES     |NO      |

The “singleExtensions” of an OCSP response shall not contain the “reasonCode” (OID 2.5.29.21) CRL entry extension.

#  8.	COMPLIANCE AUDIT AND OTHER ASSESSMENTS 
The purpose of the compliance audit is to ensure that the Provider has a satisfactory system of work that guarantees the quality of the trusted services provided by the Provider and guarantees that he is acting in compliance with all the requirements of this CP/CPS, eIDAS Regulation [3] and SMIME BR [1]. All aspects of the CA operation relating to this CP are to be subject to compliance audits.
The Provider shall at all times:  
* Issue Certificates and operates its PKI in accordance with all law applicable to its business and the Certificates it issues in every jurisdiction in which it operates;  
* Comply with Requirements of this CP/CPS;  
*	Comply with the audit requirements set forth in this section; and  
* Be licensed as a trust services provider (CA) in each jurisdiction where it operates, if licensing is required by the law of such jurisdiction for the issuance of Certificates.

##  8.1	Frequency or circumstances of assessment 
Certificates that are capable of being used to issue new Certificates shall either be Technically Constrained in line with Section 7.1.5 and audited in line with Section 8.8 only, or unconstrained and fully audited in line with all remaining requirements from this section. A Certificate is deemed as capable of being used to issue new Certificates if it contains an X.509v3 “basicConstraints” extension, with the “cA Boolean” set to “true” and is therefore by definition a Root CA Certificate or a Subordinate CA Certificate.

The period during which the Provider issues Certificates shall be divided into an unbroken sequence of audit periods. An audit period shall not exceed one year in duration.

If the Provider has a currently valid Audit Report indicating compliance with an audit scheme listed in Section 8.4, then no pre-issuance readiness assessment is necessary.

If the Provider does not have a currently valid Audit Report indicating compliance with one of the audit schemes listed in Section 8.4, then, before issuing Publicly-Trusted S/MIME Certificates, the Provider shall successfully complete a point-in-time readiness assessment performed in accordance with applicable standards under one of the audit schemes listed in Section 8.4. The point-in-time readiness assessment shall be completed no earlier than twelve (12) months prior to issuing Publicly-Trusted S/MIME Certificates and shall be followed by a complete audit under such scheme within ninety (90) days of issuing the first Publicly-Trusted S/MIME Certificate.

##  8.2	Identity/qualifications of assessor 
The Provider's audit shall be performed by a Qualified Auditor. A Qualified Auditor means a Natural Person, Legal Entity, or group of Natural Persons or Legal Entities that collectively possess the following qualifications and skills:
* Independence from the subject of the audit;  
* The ability to conduct an audit that addresses the criteria specified in an Eligible Audit Scheme (see Section 8.4);  
* Employs individuals who have proficiency in examining Public Key Infrastructure technology, information security tools and techniques, information technology and security auditing, and the third-party attestation function;  
* For audits conducted in accordance with any one of the ETSI standards accredited in accordance with ISO 17065 applying the requirements specified in ETSI EN 319 403 or ETSI EN 319 403-1;  
* Bound by law, government regulation, or professional code of ethics; and  
* Except in the case of an Internal Government Auditing Agency, it maintains Professional Liability/Errors & Omissions insurance with policy limits of at least one million US dollars in coverage.  

##  8.3	Assessor's relationship to assessed entity 
No stipulation.

##  8.4	Topics covered by assessment 
For Audit Periods starting after the Effective Date defined in Section 1.2.1 of the SMIME BR [1] the Provider shall undergo an audit in accordance with the following scheme:  
* ETSI EN 319 411-1 v1.3.1 [6] or newer, which includes normative references to ETSI EN 319 401 [5] (the latest version of referenced ETSI documents should be applied).  

The audit shall be conducted by a Qualified Auditor, as specified in Section 8.2.

##  8.5	Actions taken as a result of deficiency 
When an auditor identifies a discrepancy between the CA’s operations and the provisions of its CP/CPS, the following actions must be taken:  
* the auditor records the discrepancy,
* the auditor notifies the entities defined in Section 8.6 of the discrepancy,
* the CA proposes to the PMA appropriate corrective action, including the expected time required for its implementation.

The PMA shall determine the appropriate corrective action, potentially up to and including revocation of the CA’s certificate.

##  8.6	Communication of results 
The Audit Report shall states explicitly that it covers the relevant systems and processes used in the issuance of all Certificates that assert one or more of the policy identifiers listed in Section 7.1.6.1. The Provider shall make the Audit Report publicly available.

The Provider shall make its Audit Report publicly available no later than three months after the end of the audit period. In the event of a delay greater than three months, the Provider shall provide an explanatory letter signed by the Qualified Auditor.

The Audit Report shall contain at least the following clearly-labelled information:  
*  Name of the organization being audited;
* Name and address of the organization performing the audit;
* The SHA-256 fingerprint of all Roots and Subordinate CA Certificates, including Cross Certificates, which were in-scope of the audit;
* Audit criteria, with version number(s), that were used to audit each of the Certificates (and associated keys);
* A list of the Provider policy documents, with version numbers, referenced during the audit;
* Whether the audit assessed a period of time or a point in time;
* The start date and end date of the Audit Period, for those that cover a period of time;
* The point in time date, for those that are for a point in time;
* The date the report was issued, which will necessarily be after the end date or point in time date;
* For audits conducted in accordance with any of the ETSI standards a statement to indicate if the audit was a full audit or a surveillance audit, and which portions of the criteria were applied and evaluated, e.g., ETSI EN 319 401, ETSI EN 319 411-1 policy LCP, NCP or NCP+, ETSI EN 319 411-2 policy QCP-n, QCP-n-qscd, QCP-l or QCP-l-qscd; and
* For audits conducted in accordance with any of the ETSI standards a statement to indicate that the auditor referenced the applicable CA/Browser Forum criteria, such as this document, and the version used.

An authoritative English language version of the publicly available audit information shall be provided by the Qualified Auditor, and the Provider shall ensure that it is publicly available.

The Audit Report shall be available as a PDF and shall be text searchable for all information required. Each SHA-256 fingerprint within the Audit Report shall be uppercase letters and shall not contain colons, spaces, or line feeds.

##  8.7	Self audits 
During the period in which the Provider issues Certificates, it monitors the Provider’s RA compliance with this CP/CPS and assesses the quality of their services by conducting its own audits at least once per year on a randomly selected sample equal to the greater of thirty (30) Certificates or three percent (3%) of the Certificates it issued during the period starting immediately after the previous sample was taken for the internal audit.

##  8.8	Review of delegated parties 
No stipulation.

#  9.	OTHER BUSINESS AND LEGAL MATTERS 

##  9.1	Fees 
There is duty of the Provider to publish a valid price list of trusted services and information under which these services can be ordered. 

###  9.1.1	Certificate issuance or renewal fees 
Fee for Certificates must be paid on the terms agreed with the Subscriber/Holder. 

The Provider shall publish a valid price list on company's web site (see section 1).

In the case of the provision of its services only to the contractual partner, the price list does not need to be published.

###  9.1.2	Certificate access fees 
No stipulation.

###  9.1.3	Revocation or status information access fees 
No stipulation.

###  9.1.4	Fees for other services 
No stipulation.

###  9.1.5	Refund policy 
In justified cases, the Provider can reimburse the payment for the services provided based on an individual assessment.

##  9.2	Financial responsibility

###  9.2.1	Insurance coverage 
No stipulation.

###  9.2.2	Other assets 
No stipulation.

###  9.2.3	Insurance or warranty coverage for end-entities 
No stipulation.

##  9.3	Confidentiality of business information 

###  9.3.1	Scope of confidential information 
No stipulation.

###  9.3.2	Information not within the scope of confidential information 
No stipulation.

###  9.3.3	Responsibility to protect confidential information 
No stipulation.

##  9.4	Privacy of personal information 

###  9.4.1	Privacy plan 
The Provider shall process the Personal Data of the Subscriber/Holder or authorized persons respectively in accordance with the requirements of Regulations on the Protection of Personal Data [14]. 

The Provider shall publish a Privacy Policy that provides information on the Provider 's data protection practices. The Privacy Policy should include information on how the Provider collects, uses, shares, store, and deletes or retains data, as well as contact information for the exercise of privacy rights. 

The data protection practices are available on: [https://eidas.disig.sk/pdf/info_oou_gdpr.pdf](https://eidas.disig.sk/pdf/info_oou_gdpr.pdf).

###  9.4.2	Information treated as private
The Provider shall treat all personal information about an Individual that is not publicly available in the contents of a Certificate as private information. This includes information that links a “subject:pseudonym” to the real identity of the Subject Individual.

###  9.4.3	Information not deemed private 
No stipulation.

###  9.4.4	Responsibility to protect private information 
The Provider shall protect private information using appropriate safeguards and a reasonable degree of care. The Provider shall require the same from any service providers who manage private information on behalf of the Provider.

###  9.4.5	Notice and consent to use private information 
The Provider is obliged to proceed in accordance with the Personal Data Protection Regulations in fulfilling the information obligation towards the persons concerned and in obtaining their consent to the processing of personal data [14].

###  9.4.6	Disclosure pursuant to judicial or administrative process 
No stipulation.

###  9.4.7	Other information disclosure circumstances 
No stipulation.

##  9.5	Intellectual property rights 
No stipulation.

##  9.6	Representations and warranties 

###  9.6.1	CA representations and warranties 
By issuing a Certificate, the Provider makes the warranties listed herein to the following Certificate Beneficiaries:  
* The Subscriber that is a party to the Subscriber Agreement or Terms of Use for the Certificate;
* All Application Software Suppliers with whom Root CA has entered into a contract for inclusion of its Root CA Certificate in software distributed by such Application Software Supplier; and
* All Relying Parties who reasonably rely on a Valid Certificate.
The Provider represents and warrants to the Certificate Beneficiaries that, during the period when the Certificate is valid, the Provider has complied with this CP/CPS in issuing and managing the Certificate.

The Certificate Warranties specifically include, but are not limited to, the following:

**[1]** Right to Use Mailbox Address: That, at the time of issuance, the Provider:  
**i.)** 	implemented a procedure for verifying that the Applicant either had the right to use, or had control of, the Mailbox Addresses listed in the Certificate's subject field and subjectAltName extension (or was delegated such right or control by someone who had such right to use or control);  
**ii.)** 	followed the procedure when issuing the Certificate; and  
**iii.)** 	accurately described the procedure in the Provider 's CP/CPS;

**[2]** Authorization for Certificate: That, at the time of issuance, the Provider:  
**i.)** 	implemented a procedure for verifying that the Subject authorized the issuance of the Certificate and that the Applicant Representative is authorized to request the Certificate on behalf of the Subject;   
**ii.)** 	followed the procedure when issuing the Certificate; and   
**iii.)** 	accurately described the procedure in the Provider 's CP/CPS;

**[3]** Accuracy of Information: That, at the time of issuance, the Provider:  
**i.)** 	implemented a procedure for verifying the accuracy of all of the information contained in the Certificate (with the exception of the “subject:serialNumber” attribute);   
**ii.)** 	followed the procedure when issuing the Certificate; and   
**iii.)** 	accurately described the procedure in the Provider 's CP/CPS;  

**[4]** Identity of Applicant: That, if the Certificate contains Subject Identity Information, the Provider:
**i.)** 	implemented a procedure to verify the identity of the Applicant in accordance with Section 3.2 and Section 7.1.4.2.2;   
**ii.)** 	followed the procedure when issuing the Certificate; and   
**iii.)** 	accurately described the procedure in the Provider 's CP/CPS;  

**[5]** Subscriber Agreement: That, if the Provider and Subscriber are not Affiliated, the Subscriber and Provider are parties to a legally valid and enforceable Subscriber Agreement that satisfies these   Requirements, or, if the Provider and Subscriber are the same entity or are Affiliated, the       Applicant Representative acknowledged the Terms of Use;  

**[6]** Status: That the Provider maintains a 24 x 7 publicly-accessible Repository with current information regarding the status (Valid or Revoked) of all unexpired Certificates; and  

**[7]** Revocation: That the Provider will revoke the Certificate for any of the reasons specified in these Requirements.

###  9.6.2	RA representations and warranties 
No stipulation.

###  9.6.3	Subscriber representations and warranties 
Subscriber/Holder uses the trusted services of the Provider on his own responsibility and carries all the costs of remote means of communication or other technical means necessary for the use of these services (e.g. the software needed for making the electronic signature / seal, software for the authentication of the website etc.);

Subscriber/Holder comply with all provisions regarding commitments and warranties as stated in Terms of Use [8].

Prior to the issuance of a Certificate, the Provider shall obtain, for the express benefit of the Provider and the Certificate Beneficiaries, either the Applicant's:  
* Agreement to the Subscriber Agreement with the Provider; or
* Acknowledgement of the Terms of Use [8].

The Provider shall implement a process to ensure that each Subscriber Agreement or Terms of Use is legally enforceable against the Applicant. In either case, the Agreement shall apply to the Certificate to be issued pursuant to the Certificate Request. The Provider may use an electronic or "click-through" Agreement provided that the Provider has determined that such agreements are legally enforceable. A separate Agreement may be used for each Certificate Request, or a single Agreement may be used to cover multiple future Certificate Requests and the resulting Certificates, so long as each Certificate that the Provider issues to the Applicant is clearly covered by that Subscriber Agreement or Terms of Use.

The Subscriber Agreement or Terms of Use shall contain provisions imposing on the Applicant itself (or made by the Applicant on behalf of its principal or agent under a subcontractor or hosting service relationship) the following obligations and warranties:  
* Accuracy of Information: An obligation and warranty to provide accurate and complete information at all times to the Provider, both in the Certificate Request and as otherwise requested by the Provider in connection with the issuance of the Certificate(s) to be supplied by the Provider;
* Protection of Private Key: An obligation and warranty by the Applicant to take all reasonable measures to assure control of, keep confidential, and properly protect at all times the Private Key that corresponds to the Public Key to be included in the requested Certificate(s) (and any associated activation data or device such as a password or token);
* Acceptance of Certificate: An obligation and warranty that the Subscriber will review and verify the Certificate contents for accuracy;
* Use of Certificate: An obligation and warranty to use the Certificate only on MailBox Addresses listed in the Certificate, and to use the Certificate solely in compliance with all applicable laws and solely in accordance with the Subscriber Agreement or Terms of Use;
* Reporting and Revocation: An obligation and warranty to:  
**i.)** 	promptly request revocation of the Certificate, and cease using it and its associated Private Key, if there is any actual or suspected misuse or compromise of the Subscriber’s Private Key associated with the Public Key included in the Certificate, and   
 **ii.)** 	promptly request revocation of the Certificate, and cease using it, if any information in the Certificate is or becomes incorrect or inaccurate;  
* Termination of Use of Certificate: An obligation and warranty to promptly cease all use of the Private Key corresponding to the Public Key included in the Certificate upon revocation of that Certificate for reasons of Key Compromise.
* Responsiveness: An obligation to respond to the Provider's instructions concerning Key Compromise or Certificate misuse within a specified time period.
* Acknowledgment and Acceptance: An acknowledgment and acceptance that the Provider is entitled to revoke the Certificate immediately if the Applicant were to violate the terms of the Subscriber Agreement or Terms of Use, or if revocation is required by the Provider's CP/CPS.

###  9.6.4	Relying party representations and warranties
No stipulation.

###  9.6.5	Representations and warranties of other participants 
No stipulation.

##  9.7	Disclaimers of warranties
No stipulation.

##  9.8	Limitations of Liability 
For delegated tasks to RA, the Provider and RA may allocate liability between themselves contractually as they determine, but the Provider shall remain fully responsible for the performance of all parties in accordance with this CP/CPS, as if the tasks had not been delegated.

The Provider is not liable for indirect or contingent losses or damages incurred to the Subscriber/Holder or to the Relying Parties in connection with the use of trusted services.

The Provider is not liable for any damages (including lost profits) incurred by the Subscriber/Holder of the Certificate, relying party or to any third party due to:   
**a)**	violation of the obligations by the Subscriber/Holder or by the relying party under the legal, contractual, General Terms or Provider's obligations, including the obligation to exercise reasonable care when relying on the Certificates;  
**b)** failure to provide the necessary cooperation on the part of the Subscriber/Holder;  
**c)** by the technical features, configuration, incompatibility, inadequacy or other defects in software or hardware means used by them;  
**d)** use or reliance on the expired or revoked Certificate;  
**e)** Use of the Certificate by the Subscriber/Holder of the Certificate in violation of the contract, the General Terms or the Provider's policies;  
**f)** that the Certificate was used contrary to its purpose or limitations stated in the Certificate, in General Terms or in the CP respectively;  
**g)** delay or non-delivery of request about Certificate status to the Provider for reasons not on the Provider's side (in particular in cases of unavailability or overloading of the Internet or defects in the equipment or technical equipment used by the verifier);  
**h)** failure to provide any of the trusted services or their unavailability during the scheduled maintenance or reorganization announced at the Provider's web site;  
**i)** due to Force Majeure;

The Provider is not liable for damages incurred to the Relying party because, when relying on the Certificate and trustworthy services of the Provider or relying on the electronic signature or seal made on their basis, did not proceed according to section 10 of the General Terms [8] or according of requirements of this policy.

##  9.9	Indemnities 
Any person who violates his or her obligation or any obligation under this CP/CPS, The Agreement, and the General Terms shall be liable to compensate for damage caused to the other party, except in cases where the liability of the entity is excluded for damages. Damage shall be deemed actual damage, loss of earnings and costs incurred by the injured party in respect of the damage event.  
Whoever violates his or her obligation or any obligation under this CP/CPS, The Contract, and the General Terms may be relieved of liability for damages only if it proves that a breach of duty or any obligation has occurred as a result of circumstances excluding responsibility e.g. Force Majeure.

Notwithstanding any limitations on its liability to Subscribers and Relying Parties, the Provider understands and acknowledges that the Application Software Suppliers who have agreed to distribute the Root CA Certificate do not assume any obligation or potential liability of the CA under these Requirements or that otherwise might exist because of the issuance or maintenance of Certificates or reliance thereon by Relying Parties or others.   
Thus, except in the case where the Provider is a government entity, the Provider shall defend, indemnify, and hold harmless each Application Software Supplier for any and all claims, damages, and losses suffered by such Application Software Supplier related to a Certificate issued by the Provider, regardless of the cause of action or legal theory involved. This does not apply, however, to any claim, damages, or loss suffered by such Application Software Supplier related to a Certificate issued by the CA where such claim, damage, or loss was directly caused by such Application Software Supplier's software displaying as not trustworthy a Certificate that is still valid, or displaying as trustworthy:   
**(1)** a Certificate that has expired, or   
**(2)** a Certificate that has been revoked (but only in cases where the revocation status is currently available from the CA online, and the application software either failed to check such status or ignored an indication of revoked status).

##  9.10	Term and termination

###  9.10.1	Term 
This version of the CP/CPS is effective from the effective date specified in Section 1.2 and is valid until superseded by a new version. For details on the revision history of this CP/CPS, see the “Revision” section in Section 1.2.1.

###  9.10.2	Termination
This version of the CP/CPS will expire on the date the new version comes into effect (See section 9.10.1) or upon termination of the Provider's trusted service. 

###  9.10.3	Effect of termination and survival
In the event that this document is not replaced by a new version and its validity expires after the finishing of providing trustworthy service by Provider, all provisions of this CP/CPS relating to the Provider, which he is obliged to observe after termination of his activity shall be fulfilled. (See section 9).

##  9.11	Individual notices and communications with participants
No stipulation.

##  9.12	Amendments 

###  9.12.1	Procedure for amendment 
The CP/CPS update is based on its review, which must be done at least once a year from the approval of the current valid version. An authorized person of Provider who, based on the results of the review, must prepare a written proposal for any proposed changes and must perform the review.

An authorized PMA member must do approval of proposed changes. The proposed changes must be considered within 14 days of their delivery. After the deadline for reviewing the change proposal, the PMA has to accept the proposed change, accept it or refuse it.

Errors, update requests, or proposed CP/CPS changes must be communicated to the contact listed in section 1.5.2. Such communication must include a description of the change, the reason for the change, and the contact details of the person requesting the change or suggesting the change respectively.

All approved CP/CPS changes must be notified tby the entities concerned within one week prior to their entry into force through the channel for publishing and notifying (see section 2).
Each modified version of this CP/CPS must be numbered and registered, so the newer version must have a higher version number than the one it replaces.

Corrections of clutter, grammar and stylistic errors are not considered as changes initiating a change to the version of this CP/CPS.

###  9.12.2	Notification mechanism and period 
Provider must publish information about the current version of CP/CPS through its website (see section 1.5.2). 

The Authorized Representative of the Provider must inform all contractually bound RAs of the Provider about the approval of the new version of the CP/CPS, by sending a new version by e-mail before it enters into force in accordance with section 9.12.1. The Provider shall request feedback from the RA in the form of a confirmation e-mail message about the download of the electronic version of the Provider's CP.  
Current version of CP/CPS must be available on each contractually bound RA of the Provider at least in electronic form. Internal employees must be equally informed about the new version of this CP/CPS. 

###  9.12.3	Circumstances under which OID must be changed 
Every policy must have its OID assigned by the Provider. The OID of this policy is listed in section1.2 and for each new CP/CPS version remains unchanged.

##  9.13	Dispute resolution provisions 
The Subscriber/Holder has the right to send to the Provider a complaint about the provided trusted service by email at <radisig@disig.sk>. The Provider shall process the complaint no later than 30 days after its receipt, unless otherwise agreed by the parties. Complaint process refers only to a description of the defect referred to by the Subscriber/Holder. The Provider has to respond within 30 days of complaint receipt. The Provider reserves the right to extend this period in case of more complicated complaints.

The courts of the Slovak Republic have exclusive jurisdiction to settle any disputes between the Provider and the Subscriber/Holder of the Certificate. If the Subscriber/Holder is a consumer, any dispute may also be settled out of court. In such a case, it is entitled to contact an out-of-court dispute resolution body, Slovak trade inspection or other legal entity registered in the list pursuant to Article 5 2 of Act no. 391/2015 Coll. on alternative dispute resolution of consumer disputes, as amended. Prior to joining a court or out-of-court dispute settlement, the parties are required to try to resolve this dispute by mutual agreement first.

##  9.14	Governing law 
The laws of the Slovak Republic govern legal relations between the Provider and the Subscriber/Holder of the Certificate.

The rights and obligations of the parties which are not governed by the General Terms, or by The Agreement are governed, in particular, by the relevant provisions of Act No. 513/1991 Coll., Commercial Code, as amended, Act no. 40/1964 Coll., The Civil Code in the wording of later regulations and other generally binding legal regulations of the Slovak Republic.

##  9.15	Compliance with applicable law 
Provider provides trustworthy services in accordance with valid legal regulations in force in the Slovak Republic.

##  9.16	Miscellaneous provisions 

###  9.16.1	Entire agreement 
No stipulation.

###  9.16.2	Assignment 
The Subscriber/Holder may not assign, transfer or transfer (or otherwise deal with) any third party's rights, obligations or claims under the Agreement or the General Conditions without the written consent of the Provider.

###  9.16.3	Severability 
If any provision of this CP/CPS is, or becomes, invalid or unenforceable, it will not cause invalidity or unenforceability of the entire CP/CPS if it is completely separable from the other provisions of this CP/CPS. The Provider will immediately replace the invalid or unenforceable provision of the CP/CPS with new valid and enforceable provisions, the subject of which will be as close as possible to the subject matter of the original provision while preserving the purpose of this CP/CPS and the content of the individual provisions of this CP/CSP.

###  9.16.4	Enforcement 
In the event that a certain right is not exercised during the duration of the contractual relationship between the parties, this right shall not be terminated due to its non-application unless otherwise stated.

Because of the cancellation of contractual relationship between the Contracting Parties, The parties are not deprived of the obligation to fulfill all the obligations arising from the rights exercised so far and to take all necessary legal acts which do not delay the delay, and which are indispensable to prevent damage.

###  9.16.5	Force Majeure 
Provider, Subscriber/Holder are not responsible for delaying the fulfillment of their obligations due to circumstances excluding liability (Force Majeure).

Circumstance for excluding is an impediment that occurs independently of the will of the obligated party and prevents it from fulfilling its duty if it is impracticable to assume that the obligated party will avert or overcome this impediment or its consequences and that, at the time of the occurrence of obstacle could foresee the obstacle or not. 

If the circumstances for excluding liability arise, then the party on which such circumstances occur shall immediately inform the other of nature, the beginning, and the end of such an obstacle to the fulfillment of its obligations. Provider, Subscriber/Holder are committed to doing their utmost to avert and overcome circumstances that exclude liability. 

However, liability is not excluded if such a circumstance has occurred only when the obligated party has been late in fulfilling its obligation or if the party concerned fails to fulfill its obligation immediately inform the other of the nature and the beginning of the duration of the obstacle or if it originated from economic conditions. Effects that exclude liability are limited only to the period that an obstacle with which these effects are associated.

##  9.17	Other provisions
No stipulation. 
