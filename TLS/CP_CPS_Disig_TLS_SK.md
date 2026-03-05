# Politika a pravidlá poskytovania dôveryhodnej služby vyhotovovania a overovania verejne dôveryhodných TLS certifikátov
 
 
**Disig, a.s.**  
**Verzia 7.0**  
**Platné od 5. 3. 2026**  
**OID 1.3.158.35975946.0.0.0.1.1**  


# 1. Úvod
Tento dokument predstavuje kombinovaný dokument, ktorý zahŕňa politiku poskytovania dôveryhodných služieb a pravidlá poskytovania dôveryhodných služieb (ďalej aj „CP/CPS“) spoločnosti Disig, a.s., so sídlom Galvaniho 17/C, 821 04 Bratislava, IČO: 35975946, zapísanú v Obchodnom registri Mestského súdu Bratislava III, odd. Sa, vložka č. 3794/B, ako poskytovateľa dôveryhodných služieb (ďalej len „Poskytovateľ“) a platí pre koreňové certifikačné autority a k nim podriadené certifikačné autority uvedené v kapitole 1.4.1, prevádzkované Poskytovateľom, prostredníctvom ktorých poskytuje dôveryhodnú službu vyhotovovania verejne dôveryhodných TLS certifikátov (ďalej len „TLS certifikát“).  

Definuje:
 	Politiku (CP) – politiky a pravidlá, za ktorých sú TLS certifikáty vydávané, spravované a používané, a   
 	Pravidlá (CPS) – podrobné postupy a praktiky, ktoré Poskytovateľ implementuje na dodržanie tejto CP.

TLS certifikát vydaný pre koncového používateľa jednoznačne identifikuje entitu, ktorej je vydávaný a túto entitu zväzuje s príslušným párom kľúčov. Pokiaľ v CP/CPS nie je vyslovene uvedené, že sa to týka certifikátu koreňovej certifikačnej autority resp. podriadenej certifikačnej autority, tak slovo „TLS certifikát“ znamená TLS certifikát koncovej entity.
Webové sídlo Poskytovateľa k poskytovaným dôveryhodným službám je dostupné na adrese:
[https://eidas.disig.sk](https://eidas.disig.sk)

## 1.1 Prehľad

Tento CP/CPS definuje vytváranie a správu verejne dôveryhodných certifikátov servera TLS podľa X.509 verzie 3 [1] v súlade s RFC 5280 „Profil certifikátu infraštruktúry verejných kľúčov a zoznamu zrušených certifikátov (CRL) pre internet X.509“ [2] a požiadavkami aktuálnych verzií týchto dokumentov a noriem:
* Základné požiadavky na vydávanie a správu verejne dôveryhodných TLS certifikátov (ďalej len „TLS BR“) [3]
* Požiadaviek jednotlivých programov koreňových certifikátov distribuovaných spotrebiteľmi TLS certifikátov, ako sú Microsoft [4], Mozilla [5], Apple [6], Google [7]
* Politika spoločnej databázy CA (CCADB) [24],
* Nariadenia (EÚ) č. 910/2014 z 23. júla 2014 o elektronickej identifikácii a dôveryhodných službách pre elektronické transakcie na vnútornom trhu a o zrušení smernice 1999/93/ES, zmenené a doplnené nariadením (EÚ) č. 1183/2025 (ďalej len „TLS BR“) „eIDAS“) [8] a
* ETSI EN 319 401 [9] a ETSI EN 319 411-1. [10].

Tieto CP/CPS sú štruktúrované v súlade s RFC 3647 [11].

Poskytovateľ potvrdzuje, že tieto CP/CPS zohľadňujú všetky požiadavky aktuálnej verzie dokumentu [3], ktorý je zverejnený na adrese [https://cabforum.org/working-groups/server/baseline-requirements/documents/](https://cabforum.org/working-groups/server/baseline-requirements/documents/).

V prípade akéhokoľvek nesúladu medzi týmito požiadavkami a týmito CP/CPS majú prednosť požiadavky aktuálnej verzie dokumentu [3].

## 1.2	Názov dokumentu a jeho identifikácia

|  | |
| :--- | :--- |
|Názov:|**Politika a pravidlá poskytovania dôveryhodnej služby vyhotovovania a overovania verejne dôveryhodných TLS certifikátov** |
|Skratka názvu: | **CA Disig TLS CP/CPS** |
|Verzia:|  **7.0** |
|Schválené dňa:| **2. 3. 2026**   |
|Platnosť od:| **5. 3. 2026**    |  
|Tomuto dokumentu je priradený identifikátor objektu (OID):|**1.3.158.35975946.0.0.0.1.1** |  
 
Popis použitého identifikátora objektu (OID):  
 1\.  - ISO assigned OIDs  
 1.3.  ISO Identified Organization  
 1.3.158.  -  Identification number (Company ID - ICO)    
 1.3.158.35975946. - Disig, a. s.  
 1.3.158.35975946.0.0.0.1.  - CA Disig  
 1.3.158.35975946.0.0.0.1.1 - CA Disig TLS CP/CPS  

Tento OID (1.3.158.35975946.0.0.0.1.1) je zároveň uvádzaný aj vo vydávaných TLS certifikátoch a pokrýva tieto politiky zo štandardu [10]:

|Názov politiky|OID|ETSI štandard|  
|-----------|---|----------------------|
|LP: 	Lightweight Certificate Policy|0.4.0.2042.1.3|ETSI EN 319 411-1 LCP|
|OVCP: 	Organizational Validation 	Certificate Policy|0.4.0.2042.1.7|ETSI EN 319 411-1 OVCP|
|NCP: 	Normalized Certificate Policy|0.4.0.2042.1.1|ETSI EN 319 411-1 NCP|  

###  1.2.1 História zmien

|Verzia |Dátum revízie  |Popis revízie; Revidoval|  
|:-:|:----------:|-------------------------------|
|1.0|25. 03. 2006|Prvá verzia dokumentu; Miškovič|  
|1.5|20. 12. 2006|Formálne úpravy textu dokumentu – formátovanie, opravy odkazov, úpravy textu v kapitole 4 „Prevádzkové požiadavky“; Miškovič|  
|2.0|23. 01. 2007|Rozšírenie CP/CPS v súvislosti s novým typom vydávaných certifikátov pre zmluvného klienta. Doplnenie kapitoly 7 „Profily certifikátov“; Miškovič.|  
|2.1|29. 03. 2007|Opravy textu v kap. 2.8 a kap. 4.9 Úpravy textu v súvislosti s minoritnou zmenou v certifikáte pre zmluvného partnera; Miškovič|  
|3.0|19. 03. 2008|Celková revízia CP/CPS vzhľadom k jednotlivým typom certifikátov; Ďurišová, Miškovič|  
|3.1|26. 04. 2008|Pridanie nového typu certifikátu; Miškovič|
|3.2|10. 11. 2008|Zmena dĺžky platnosti certifikátov pre doménového používateľa PKI VšZP Zrušenie prevádzky na Záhradníckej 153.; Miškovič|
|3.3|25. 11. 2008|Úprava znenia: ods. 3.1.9 - overovanie vlastníctva domény ods. 4.1.1, 4.1.2, - overovanie platnosti e-mail adresy žiadateľa; Miškovič|  
|3.4|02. 06. 2009|Úprava v súvislosti s požiadavkou na minimálnu dĺžku verejného kľúča, na ktorý CA Disig vydá certifikát (ods.5.1.3; 6.1.2); Zmena umiestnenia e-mail adresy v profile certifikátu<br> (ods. 3.1.2; 6.1.2); Miškovič|
|4.0|10. 10. 2009|Úprava v súvislosti s požiadavkami Mozilla Foundation pri uchádzaní sa o umiestnenie certifikátu CA Disig do Mozilla Root Certificate Store; Miškovič|
|4.1|11. 05. 2010|Zapracovanie navrhnutých nápravných opatrení z auditu zo dňa 13.11.2009 (audit podľa ETSI TS 102042 V1.3.4); Miškovič|
|4.2|03. 03. 2011|Zmena dĺžky platnosti certifikátov; zapracovanie požiadaviek novej bezpečnostnej politiky Mozilla Foundation a požiadaviek Microsoft (code signing); formálne úpravy tabuliek a textov; Miškovič|
|4.3|25. 01. 2012|Doplnenie možnosti vydávania podriadených CA, doplnenie podpisových algoritmov a pravidelná ročná revízia obsahu; Miškovič|
|4.4|22. 06. 2012|Zapracovanie požiadaviek dokumentu „Baseline Requirements for the Issuance and Management of Publicly-Trusted Certificates, v.1.0, ktorý vydala CA/Browser Forum; Miškovič|
|4.5|15. 08. 2013|Spresnenie profilu certifikátov koreňových certifikačných autorít CA Disig a ostatných vydávaných typov certifikátov; Miškovič|
|4.6|21. 06. 2013|Spresnenie OID dokumentu – vypustenie verzie dokumentu z OID (kap. 1.2). Úprava profilov pre vydávanie podriadených CA – certificatePolicies Identifier (kap.7.1.2); <br>Povolenie vydávania „wildcard“ TLS/SSL certifikátov na tretej úrovni doménového mena; (3.1.2 Miškovič)|
|4.7|02. 02. 2015|Zapracovanie požiadaviek aktuálnej verzie dokumentu „Baseline Requirements for the Issuance and Management of Publicly-Trusted Certificates, v.1.2.3; Revízia CP/CPS <br>v súvislosti s novelou zákona o elektronickom podpise v zmysle zákona č. 305/2013 Z. z.; Miškovič|
|4.8|22. 05. 2015|Overovanie CAA záznamov (4.1.5)|
|4.9|21. 10. 2016|Vykonané zmeny v súvislosti s Nariadením eIDAS a v súvislosti s ukončením platnosti zákona č. 215/2002 Z. z. a nadobudnutím účinnosti zákona č. 272/2016 Z. z.; <br>Zapracovanie požiadaviek Baseline Requirements for the Issuance and Management of Publicly-Trusted Certificates, do verzie v.1.4.1; Miškovič|
|5.0|25. 09. 2017|Konverzia CP/CPS do formátu v zmysle RFC 3647; Zapracovanie požiadaviek nariadenia eIDAS [8] a zapracovanie požiadaviek aktuálnej verzie Baseline Requirements <br>for the Issuance and Management of Publicly-Trusted Certificates, v.1.5.2; Miškovič|
|5.1|23. 05. 2018|Nadobudnutie účinnosti Nariadenia č. 2016/679 – GDPR; Úprava znenia bodu 1.3.3; zmena znenia bodu 3.2.2.4 (nový spôsob overenia); doplnenie kapitoly 4.2.2 (gTLD);<br> doplnenie bodu 4.9.11 (OCSP stapling); Miškovič|
|5.2|17. 05. 2019|Úprava bodu 4.9 v zmysle Baseline Requirements for the Issuance and Management of Publicly-Trusted Certificates, v.1.6.1; Úprava bodu 8.4 v zmysle Baseline Requirements<br> for the Issuance and Management of Publicly-Trusted Certificates, v.1.6.5; Spresnenie definícii v bode 1.3.1; Doplnenie bodu 3.1,4; Miškovič|
|5.3|02. 12. 2019|Úprava profilu certifikátu pre elektronický podpis (3.1.4.1.); úprava dĺžky platnosti vydávaných certifikátov pre podpis/pečať (7.1.4); Aktualizácia odkazov (1.6.3.); <br>Doplnenie skratiek a drobné úpravy textu.; Miškovič|
|5.4|01. 09. 2020|Úprava platnosti TLS/SSL certifikátov v zmysle požiadaviek [3] verzia 1.6.6 časť 6.3.2 a 7.1.4. Doplnenie sha256RSA odtlačku pre koreňovú Disig Root R2 a podriadene <br>CA Disig R2I2 a VCA Disig R2I3 v časti 1.4.1. Spresnenie metód overovania vlastníctva domény v časti 3.2.2.4; Vypustenie povinného podporovania OCSP Stapling v časti 4.9.11 Miškovič|
|5.5|20. 05. 2021|Doplnenie spôsobu oznamovania incidentov (2.2); Čas použiteľnosti údajov použitých pri overovaní vlastníctva domény (3.2.2.4); Spôsob nahlasovania kompromitácie súkromného kľúča<br> CA tretími stranami (4.9.12); Miškovič|
|5.6|20. 05. 2022|Vypustenie položky OU z profilu TLS certifikátu (3.1.4.3);  úprava požiadaviek postupov získavania auditných záznamov v zmysle požiadaviek [3] verzia 1.8.4 (5.4); zmena označenia<br> typu certifikátu TLS/SSL na TLS; Miškovič|
|5.7|01. 10. 2022|Zmeny v súvislosti s požiadavkou uvádzania dôvodov zrušenia pri rušení vydaných TLS certifikátov (4.9.1.1; 4.9.2; 4.9.3;7.2.2)|
|5.8|20. 04. 2023|Zmeny v súvislosti s vytvorením novej podriadenej CA Disig R2I5; Miškovič|
|5.9|01. 09. 2023|Zmeny v súvislosti s nadobudnutím účinnosti „Baseline Requirements for the Issuance and Management of Publicly‐Trusted S/MIME Certificates“; Miškovič|
|6.0|01. 02. 2024|Vyčlenenie CP/CPS výhradne pre politiku vyhotovovanie verejne dôveryhodných TLS certifikátov doplnenie Miškovič|
|6.1|18. 07. 2024|Zmena sídla spoločnosti Disig, a.s., Doplnenie požiadavky na použitie „zlint“ (4.3.1), Úprava rozsahu rozšírení v časti 7.1.2.7; Miškovič| 
|6.2|15. 08. 2024|Rozšírenie metód na overenie domény o metódu Zmena DNS v zmysle TLS Baseline Requirements časť 3.2.2.4.7; Miškovič|
|6.3|10. 01. 2025|Ukončenie používania metód na overenie domény v zmysle časti 3.2.2.4.2 a 3.2.4.15 k 15.1.2025;. zavedenie do používania nových metód  na overovanie domény<br> (3.2.2.4.13 a 3.2.2.4.14); doplnenie dokumentu o časť „Multiperspektívne potvrdenie vydania“ (3.2.2.9); Úprava časti 4.9.9;  Miškovič|
|6.4|01. 09. 2025|Zmena v používaných metódach pre overenie domény (3.2.2.4); Zohľadnenie požiadaviek časti 6.1.3 Mozilla Root Store Policy v. 3.0 (4.9.5); Plány hromadného rušenia (5.7.1.2); Miškovič|
|7.0|05. 03. 2026|Transformácia dokumentu na novú formu kombinovanej politiky pre poskytovanie služby vyhotovovanie verejne dôveryhodných TLS certifikátov, ktorá zahrňuje aj  pravidlá pre poskytovanie<br> tejto služby, ktoré boli pôvodne predmetom samostatného dokumentu. Pridanie novej single-purpose CA Disig TLS Root R3 a jej podriadenej CA Disig R3I1 TLS Certificate Service (1.3.1.2); <br>Doplnenie informácii a profilov týkajúcich sa cross-certifikátov. ( 7); Doplnenie novej metódy overovanie vlastníctva domény- ACME (3.2.2.4.19); Miškovič|
  
## 1.3 Účastníci PKI

### 1.3.1 Certifikačné autority

Koreňová CA (Root CA) je certifikačná autorita najvyššej úrovne, ktorej koreňový certifikát distribuujú dodávatelia aplikačného softvéru. Koreňová CA vydáva certifikáty podriadeným certifikačným autoritám.
Podriadená CA (Subordinate CA) je certifikačná autorita, ktorej certifikát je podpísaný koreňovou CA alebo inou podriadenou CA.
Tieto CP/CPS sa vzťahujú na poskytovanie dôveryhodných služieb podriadenými certifikačnými autoritami, ktoré patria do jednej z hierarchií CA prevádzkovaných Poskytovateľom na vydávanie verejne dôveryhodných TLS certifikátov, ako je opísané nižšie.

#### 1.3.1.1 Viacúčelová hierarchia CA
Táto hierarchia zahŕňa koreňovú CA a vydávajúcu podriadenú CA, čo predstavuje pôvodnú štruktúru CA prevádzkovanú Poskytovateľom od jeho prijatia za poskytovateľa verejne dôveryhodných TLS certifikátov v rámci príslušných programov koreňových CA akceptovaných spoločnosťami Microsoft, Mozilla, Google a Apple.
Táto hierarchia sa bude používať na vydávanie TLS certifikátov koncovým používateľom len dovtedy, kým nebude nahradená novou jednoúčelovou hierarchiou (pozri 1.3.1.2).

| | |
|:--- |:--- |
|Názov:|**CA Disig Root R2**|
|Sériové číslo certifikátu: |**0092b888dbb08ac163**|
|Odtlačok (sha1)(DER):|**B561EBEAA4DEE4254B691A98A55747C234C7D971**|
|Odtlačok (sha256)(DER):|**E23D4A036D7B70E9F595B1422079D2B91EDFBB1FB651A0633EAA8A9DC5F80703**|
|Poznámka:|**Vydáva certifikáty len pre podriadené certifikačné autority Poskytovateľa.**|  

 

| | |
|:--- |:--- |
|Názov:|**CA Disig R2I2 Certification Service**|
|Sériové číslo certifikátu: |**081792523668f5c8500000000000000003**|
|Vydavateľ:|**CA Disig Root R2**|
|Odtlačok (sha1)(DER):|**19F2783DEDD8561A61C682932EE9D5B4D86B00CE**|
|Odtlačok (sha256)(DER):|**C96F24C45113FD91AE2F9E40E106653BFA0FFBCFA07E209524C844E7C8DA4148**|
|Poznámka:|**Vydáva len TLS certifikáty pre koncových používateľov (pozri 3.1.4.3).**|


#### 1.3.1.2 Single-purpose TLS CA  
Táto hierarchia CA predstavuje náhradu „legacy“ hierarchie CA (pozri 1.3.1.1), ktorá je v súčasnosti využívaná na vydávanie TLS certifikátov pre koncových zákazníkov. Táto „single-purpose“ TLS CA hierarchia už plne spĺňa aktuálne požiadavky BR pre TLS [3], kde je pri nových koreňových CA vyžadovaná samostatná hierarchia CA pre účely vydávania TLS certifikátov koncovým zákazníkom a je obmedzená len na vydávanie certifikátov obsahujúcich v rozšírení EKU len id-kp-serverAuth (1.3.6.1.5.5.7.3.1)  
Reálne vydávanie TLS certifikátov pre koncových zákazníkov prostredníctvom tejto hierarchie sa predpokladá až po úplnej akceptácii „single-purpose“ CA Disig TLS Root R3 v programoch pre koreňové certifikačné autority  spoločností Microsoft, Mozilla, Google a Apple.  

|  | |
| :--- | :--- |
| Názov:|**CA Disig Root R3**|
| Sériové číslo certifikátu:| **5b99abc2b008cf8441d62e523909b41b**|
| Thumbprint (sha1)(DER):   |  **AF250F267724C554652607D70985DE93DD33AFC0**|
| Thumbprint (sha256)(DER): | **6248199FEA4811FD34AA96EF0A26DE52134B73A9A2A99678F0C2EBADF8663EF8**|
| Poznámka:                  | **Vydáva certifikáty len pre podriadené certifikačné autority Poskytovateľa vyhtradené pre TLS certifikáty.**|  

   

|  | |
| :--- | :--- |
| Názov:| **CA Disig R3I1 TLS Certification Service** |
| Vydavateľ:|**CA Disig Root R3**|
| Poznámka:| **Vydáva len TLS certifikáty pre koncových používateľov (pozri 3.1.4.1).**|


### 1.3.2 Registračné autority
Registračná autorita („RA“) je subjekt, ktorý na základe zmluvy vykonáva určité vybrané činnosti pri poskytovaní dôveryhodných služieb v mene Poskytovateľa.
RA vykonáva svoju činnosť v súlade s týmito CP/CPS.

Poskytovateľ môže zriadiť nasledujúce typy RA:
* **Interná RA** – je prevádzkovaná Poskytovateľom a je určená na poskytovanie dôveryhodných služieb pre všetky zainteresované strany. Táto RA nie je samostatným právnym subjektom.

Generovanie prístupových kľúčov a vydávanie autentifikačných TLS certifikátov vo formáte X.509 pre pracovníka internej RA (ďalej len „pracovník RA“) vykonávajú oprávnení zamestnanci Poskytovateľa. Prístupové kľúče každého pracovníka RA sú uložené na hardvérovom zariadení (čipová karta), kde je prístup ku kľúčom chránený prístupovým heslom, ktoré si zvolí samotný pracovník RA. Tým sa zabezpečuje dvojfaktorová autentifikácia pri vydávaní TLS certifikátu prostredníctvom IS Poskytovateľa.

### 1.3.3 Odberatelia (Subscribers)
Pod odberateľom sa rozumie fyzická osoba alebo právnická osoba, ktorá je oprávnená žiadať o TLS certifikát v mene subjektu, ktorého meno je uvedené ako predmet (subject) v TLS certifikáte – držiteľ certifikátu.

Držiteľom certifikátu môže byť:
* Zariadenie alebo systém prevádzkovaný fyzickou alebo právnickou osobou, alebo prevádzkovaný v mene fyzickej alebo právnickej osoby.

Ak je Odberateľ zároveň subjektom, nesie osobnú zodpovednosť v prípade, že jeho povinnosti nie sú správne splnené.
Zodpovednosti Odberateľa a subjektu sú upravené vo „Všeobecných podmienkach poskytovania a používania služby vydávania a overovania dôveryhodných certifikátov“ (ďalej len „Všeobecné podmienky“) [12] uverejnených na webovom sídle Poskytovateľa (pozri časť 1).
Tieto CP/CPS definujú požiadavky, ktoré Odberateľ spĺňa.

Formálnym držiteľom certifikátu sa rozumie fyzická osoba, ktorá sa zaväzuje používať príslušný súkromný kľúč a TLS certifikát v súlade s týmito CP/CPS.

Pri žiadosti o TLS certifikát pre zariadenie alebo systém prevádzkovaný fyzickou alebo právnickou osobou alebo v ich mene, je Odberateľom:
* Fyzická alebo právnická osoba prevádzkujúca zariadenie alebo systém.
* Akýkoľvek subjekt, ktorému príslušný právny systém umožňuje zastupovať právnickú osobu; alebo
* Právny zástupca právnickej osoby, ktorý objednáva služby pre svoje dcérske spoločnosti.

### 1.3.4 Spoliehajúce sa strany (Relying Parties)
Spoliehajúce sa strany sú fyzické alebo právnické osoby, ktoré sa vo svojom konaní spoliehajú na elektronickú identifikáciu alebo dôveryhodné služby Poskytovateľa.

### 1.3.5 Ostatní účastníci
Kategória „ostatní účastníci“ zahŕňa subjekty, ktoré nie sú CA Poskytovateľa, Registračnou autoritou (RA), Odberateľmi ani spoliehajúcimi sa stranami, ale majú vplyv na poskytovanie alebo využívanie služieb podľa týchto CP/CPS. Medzi tieto subjekty patria najmä:

#### 1.3.5.1 Orgán pre správu politík (Policy Management Authority)
Orgán pre správu politík – PMA je zložka zriadená za účelom:
* Dohľadu nad tvorbou a aktualizáciou CP/CPS vrátane vyhodnocovania plánov na implementáciu akýchkoľvek zmien.
* Preskúmavania CP/CPS s cieľom zabezpečiť, aby prax Poskytovateľa bola v súlade s jeho požiadavkami.
* Preskúmavania výsledkov auditov s cieľom určiť, či Poskytovateľ primerane dodržiava schválené CP/CPS.
* Poskytovania odporúčaní pre Poskytovateľa týkajúcich sa nápravných opatrení a iných vhodných opatrení.
* Poskytovania poradenstva ohľadom vhodnosti TLS certifikátov spojených s CP/CPS pre konkrétne riadiace aplikácie a riadenie činností certifikačnej autority a registračnej autority.
* Interpretácie CP/CPS a pokynov pre RA a CA.
* Vykonávania interného auditu Poskytovateľa poverením nezávislého zamestnanca.
* Zabezpečenia riadnej a náležitej implementácie prijatých a schválených CP/CPS.

PMA predstavuje najvyšší orgán, ktorý s konečnou platnosťou rozhoduje o všetkých záležitostiach a aspektoch súvisiacich s Poskytovateľom a jeho činnosťou.

#### 1.3.5.2 Posudzovatelia zhody (auditori)
Posudzovatelia zhody sú nezávislé organizácie, ktoré na základe akreditácie posudzujú súlad Poskytovateľa s:
* príslušnými normami (napr. ETSI EN 319 401, ETSI EN 319 411-1 alebo iné relevantné normy),
* týmito CP/CPS a súvisiacimi internými politikami Poskytovateľa,
* požiadavkami programov Trusted Root CA a/alebo CCADB.

Posudzovatelia zhody:
* majú právo požadovať od Poskytovateľa prístup k potrebným dokumentom, záznamom a systémom v rozsahu potrebnom na vykonanie auditu;
* sú viazaní povinnosťou mlčanlivosti v rozsahu dohodnutom v zmluve s Poskytovateľom a v súlade s platnými právnymi predpismi;
* neposkytujú žiadne služby vydávania TLS certifikátov, správu kľúčov ani funkcie CA/RA.

Poskytovateľ zabezpečí, aby vzťahy s posudzovateľmi zhody boli upravené písomnou zmluvou a aby nedochádzalo ku konfliktu záujmov.

#### 1.3.5.3 Dozorné orgány a operátori politík root programov 
Dozorné orgány a operátori politík root programov sú subjekty, ktoré vykonávajú zákonný alebo programový dohľad nad činnosťou Poskytovateľa, napríklad:
* národný dozorný orgán pre dôveryhodné služby alebo elektronickú identifikáciu;
* operátori politík root programov (napr. výrobcovia prehliadačov a OS), ktorí rozhodujú o zaradení/odstránení koreňových CA do príslušného programu;
* správcovia a operátori CCADB.

Tieto subjekty:
* môžu od Poskytovateľa vyžadovať informácie, dokumenty a vysvetlenia týkajúce sa prevádzky CA a dodržiavania požiadaviek;
* môžu vyžadovať prijatie nápravných opatrení, obmedzení alebo ukončenie vydávania TLS certifikátov;
* nie sú zmluvnou stranou ani spoliehajúcou sa stranou, ale môžu ovplyvniť dôveryhodnosť vydaných TLS certifikátov (napr. odstránením koreňovej CA z programu).

Poskytovateľ spolupracuje s týmito subjektmi v rozsahu vyžadovanom platnými právnymi predpismi, platnými pravidlami programov a týmito CP/CPS.

## 1.4 Používanie certifikátov

### 1.4.1 Povolené spôsoby použitia certifikátov
Certifikáty vydávané podľa týchto CP/CPS sa vydávajú na účely identifikácie držiteľa verejného kľúča z kryptografického páru kľúčov (verejný a súkromný), ktorý sa používa v rámci infraštruktúry PKI.
Kryptografický pár kľúčov (súkromný a verejný) a TLS certifikát vydaný Poskytovateľom sa vo všeobecnosti môžu používať na:
* zabezpečenie TLS komunikácie (autentifikácia webových sídiel) v rámci verejných sietí vrátane verejného internetu (WebPKI).

Poskytovateľ vydáva Odberateľom nasledujúce typy TLS certifikátov:
* Verejne dôveryhodný TLS certifikát (TLS certifikát) – kryptografické kľúče spojené s týmto typom TLS certifikátu sú určené na autentifikáciu serverov prístupných cez internet; Verejne dôveryhodné certifikáty sú dôveryhodné vďaka tomu, že ich zodpovedajúci koreňový certifikát je distribuovaný v bežne dostupnom aplikačnom softvéri. Vydaný TLS certifikát bude okrem iného obsahovať nasledujúce identifikátory certifikačných politík pre overenie organizácie (OV):
    * (4) etsi (0) other-TLS Certificate-policies (2042) policy-identifiers (1) ovcp (7) joint-iso-itu-t (2) international-organizations (23) ca-browser-forum (140) certified-polcies (1) baselinerequirements (2) t. j. 2.23.140.1.2.2 v zmysle TLS BR [3].
* Poskytovateľ vydáva certifikáty pre vlastné potreby správy (certifikát pre podriadenú CA alebo certifikát pre OCSP respondery).

### 1.4.2 Zakázané spôsoby použitia certifikátov
TLS certifikáty vydávané podľa týchto CP/CPS nie sú kvalifikovanými certifikátmi EÚ pre autentifikáciu webových síd podľa nariadenia eIDAS [8] a nemôžu sa používať tam, kde sa vyžadujú kvalifikované TLS certifikáty EÚ pre autentifikáciu webových sídiel.
Certifikáty vydávané podľa týchto CP/CPS sa nesmú používať na:
* podpisovanie kódu, dokumentov alebo e-mailov;
* vydávanie iných TLS certifikátov (netýka sa certifikátov pre CA);
* akékoľvek použitie, ktoré nie je v súlade s rozšíreniami Key Usage (Použitie kľúča) a EKU (Rozšírené použitie kľúča);
* akékoľvek použitie, ktoré je nezákonné, v rozpore s platnými právnymi predpismi alebo v rozpore s týmito CP/CPS alebo zmluvou o dôveryhodných službách.

Spoliehajúce sa strany by sa nemali spoliehať na TLS certifikáty na iné účely ako na autentifikáciu TLS servera, pokiaľ takéto použitie nie je výslovne povolené príslušnou politikou TLS certifikátov a jasne uvedené v rozšíreniach TLS certifikátu.

## 1.5 Správa politiky

### 1.5.1 Organizácia spravujúca dokument
Nasledujúca tabuľka obsahuje údaje o Poskytovateľovi, ktorý je zodpovedný za prípravu, tvorbu a údržbu tohto dokumentu.

|  | |
| :--- | :--- |
| Spoločnosť:| **Disig, a. s.** |
| Adresa sídla: | **Galvaniho 17/C, 821 08 Bratislava**|
| IČO:|  **359 75 946** |
| telefón:| **+421 2 20850140**   |
| e-mail:| **disig@disig.sk**    |
| webové sídlo:| **[https://www.disig.sk](https://www.disig.sk)**    |

### 1.5.2 Kontaktná osoba
Na účel tvorby politík má Poskytovateľ vytvorenú autoritu pre správu politík (PMA), ktorá plne zodpovedá za jej obsah, a ktorá je pripravená odpovedať na všetky otázky týkajúce sa politík Poskytovateľa (pozri časť 1.3.5).
Nasledujúca tabuľka obsahuje kontaktné údaje na zložku zodpovednú za prevádzku certifikačných autorít Poskytovateľa.
|  | |
| :--- | :--- |
| Certifikačná Autorita CA Disig:|  |
| Adresa sídla: | **Galvaniho 17/C, 821 08 Bratislava**|
| IČO:|  **359 75 946** |
| telefón:| **+421 2 20850150, +421 2 20820157**   |
| e-mail:| **caoperator@disig.sk**    |
| webové sídlo:| **[https://eidas.disig.sk](https://eidas.disig.sk)**    |
| Oznamovanie incidentov:| **[tspnotify@disig.sk](tspnotify@disig.sk)**    |
| |  viac pozri: **[https://eidas.disig.sk/pdf/incident_reporting.pdf](https://eidas.disig.sk/pdf/incident_reporting.pdf)**|

### 1.5.3 Osoba určujúca vhodnosť CP/CPS
Osobou zodpovednou za rozhodovanie o súlade postupov Poskytovateľa tak, ako sú uvedené v týchto CP/CPS, je PMA (pozri 1.3.5).

### 1.5.4 Postupy schvaľovania CP/CPS
Ešte pred začatím prevádzky by mal Poskytovateľ schváliť svoje CP/CPS a musí spĺňať všetky ich požiadavky. Obsah CP/CPS schvaľuje osoba menovaná orgánom PMA.
Po schválení orgánom PMA sa príslušný dokument zverejní v súlade s politikou zverejňovania a oznamovania.
PMA musí o svojich rozhodnutiach informovať takým spôsobom, aby boli tieto informácie dobre prístupné spoliehajúcim sa stranám.
Tieto CP/CPS schvaľuje osoba vymenovaná do roly PMA.
CP/CPS sú zverejnené v súlade s politikou zverejňovania a oznamovania na webovom sídle Poskytovateľa (pozri časť 1).

## 1.6 Definície a skratky

### 1.6.1 Definície
**TLS certifikát pre autentifikáciu webových sídel** znamená potvrdenie, ktoré umožňuje autentifikovať webové sídlo a prepojiť ho s fyzickou alebo právnickou osobou, ktorej bol TLS certifikát vydaný.

**Dôveryhodná služba** znamená elektronickú službu bežne poskytovanú za odplatu, ktorá pozostáva z:
  **a|** vyhotovovania, overovania a potvrdzovania elektronických podpisov, elektronických pečatí alebo elektronických časových pečiatok, služieb elektronického doporučeného doručovania a TLS certifikátov súvisiacich s týmito službami,
  **b|** vyhotovovania, overovania a potvrdzovania TLS certifikátov pre autentifikáciu webových síd,
  **c|** uchovávania elektronických podpisov, pečatí alebo TLS certifikátov súvisiacich s týmito službami.

**Držiteľ certifikátu** znamená subjekt identifikovaný v TLS certifikáte ako držiteľ súkromného kľúča patriaceho k verejnému kľúču obsiahnutému v TLS certifikáte.

**Pár kľúčov** znamená časť systému PKI, ktorý využíva asymetrickú kryptografiu a pozostáva z verejného kľúča a súkromného kľúča.

**Viacúčelová CA** – Koreňová CA alebo podriadená CA, ktorá sa nachádza v hierarchii bez obmedzení na typ TLS certifikátu vydaného koncovému držiteľovi, t. j. v hierarchii je možné koncovým používateľom vydávať TLS certifikáty, ako aj S/MIME TLS certifikáty alebo iné typy TLS certifikátov.

**Doménový kontakt** znamená registrátora doménového mena, technický kontakt alebo administratívny kontakt (alebo ekvivalent v rámci ccTLD), ako je uvedený v zázname WHOIS základného doménového mena alebo v zázname DNS SOA.

**Poskytovateľ dôveryhodných služieb** znamená fyzickú alebo právnickú osobu, ktorá poskytuje jednu alebo viac dôveryhodných služieb buď ako kvalifikovaný, alebo ako nekvalifikovaný poskytovateľ dôveryhodných služieb.

**Pracovník RA** znamená zamestnanca Poskytovateľa alebo inej právnickej osoby, ktorá má s Poskytovateľom uzatvorenú zmluvu o poskytovaní certifikačných služieb.

**Spoliehajúca sa strana** znamená fyzickú alebo právnickú osobu, ktorá sa spolieha na elektronickú identifikáciu alebo dôveryhodnú službu.

**Verejne dôveryhodný certifikát** znamená TLS certifikát, ktorý je dôveryhodný vďaka tomu, že jeho zodpovedajúci koreňový TLS certifikát je distribuovaný ako „kotva dôvery“ (trust anchor) v bežne dostupnom aplikačnom softvéri.

**Jednoúčelová CA** – Koreňová CA alebo podriadená CA, ktorá sa nachádza v hierarchii, ktorá je striktne obmedzená na vydávanie práve jedného typu TLS certifikátu koncovému používateľovi, t. j. v hierarchii môžu byť koncovému používateľovi vydávané len TLS certifikáty.

**Odberateľ (Subscriber)** znamená fyzickú osobu alebo právnickú osobu, ktorej je vydaný TLS certifikát a ktorá je právne viazaná zmluvou o poskytovaní služieb alebo podmienkami používania.

**Zmluvný partner (Contractor)** znamená právnickú osobu, s ktorou spoločnosť Disig uzatvorila písomnú zmluvu o poskytovaní dôveryhodných služieb.

**PKCS#10** znamená formát správ posielaných certifikačnej autorite so žiadosťou o certifikáciu verejného kľúča.

**PEM** znamená formát súboru na ukladanie a odosielanie kryptografických kľúčov, TLS certifikátov a iných údajov, ako je formalizované organizáciou IETF v RFC 746.

**SAN** znamená rozšírenie X.509, ktoré umožňuje priradiť rôzne hodnoty k bezpečnostnému TLS certifikátu pomocou poľa subjectAltName.

**TLS** sú kryptografické protokoly navrhnuté na zabezpečenie komunikácie v počítačovej sieti.

### 1.6.2 Skratky
| | |
| :--- | :--- |
| CA | Certifikačná autorita (Certification Authority) |
| CAA | Autorizácia certifikačnej autority (Certification Authority Authorization) |
| CMA | Orgán pre správu certifikátov (Certificate Management Authority) |
| CP/CPS | Certifikačná politika a vyhlásenie o certifikačných postupoch (CP/CPS) |
| CRL | Zoznam zrušených certifikátov (Certification Revocation List) |
| DNS | Systém doménových mien (Domain Name System) |
| FQDN | Plne kvalifikované doménové meno (Fully Qualified Domain Name) |
| HSM | Hardvérový bezpečnostný modul (Hardware Security Module) |
| IČO | Identifikačné číslo organizácie |
| NBÚ | Národný bezpečnostný úrad |
| OID | Identifikátor objektu (Object Identifier) |
| PKI | Infraštruktúra verejných kľúčov (Public Key Infrastructure) |
| PMA | Orgán pre správu politík (Policy Management Authority) |
| RA | Registračná autorita (Registration Authority) |
| TLS | Zabezpečenie transportnej vrstvy (Transport Layer Security) |
| SSL | Vrstva bezpečných soketov (Secure Sockets Layer) |

### 1.6.3 Referencie  
 **[1]** Recommendation ITU-T X.509; Information technology - Open Systems Interconnection - The Directory: Public-key and attribute TLS Certificate frameworks.   
 **[2]** RFC5280, Request for Comments: 5280, Internet X.509 Public Key Infrastructure: Certificate and Certificate Revocation List (CRL) Profile.   
 **[3]** Baseline Requirements for the Issuance and Management of Publicly-Trusted TLS Certificates [https://cabforum.org/baseline-requirements-documents/](https://cabforum.org/baseline-requirements-documents/).  
 **[4]** Program Requirements - Microsoft Trusted Root Program [https://learn.microsoft.com/en-us/security/trusted-root/program-requirements](https://learn.microsoft.com/en-us/security/trusted-root/program-requirements).    
 **[5]** Mozilla Root Store Policy [https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/policy/](https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/policy/)    
 **[6]** Apple Root Certificate Program [https://www.apple.com/certificateauthority/ca_program.html](https://www.apple.com/certificateauthority/ca_program.html).   
 **[7]** Chrome Root Program Policy [https://www.chromium.org/Home/chromium-security/root-ca-policy/](https://www.chromium.org/Home/chromium-security/root-ca-policy/).    
 **[8]** Nariadenie Európskeho parlamentu a Rady (EÚ) č. 910/2014 z 23. júla 2014 o elektronickej identifikácii a dôveryhodných službách pre elektronické transakcie na vnútornom trhu a o zrušení smernice 1999/93/ES, v znení Natiadenia EP a Rady (EÚ) č. 1183/2024.   
 **[9]** ETSI EN 319 401 Electronic Signatures and Infrastructures (ESI); General Policy Requirements for Trust Service Providers.   
 **[10]** ETSI EN 319 411-1 Electronic Signatures and Infrastructures (ESI); Policy and security requirements for Trust Service Providers issuing TLS Certificates; Part 1: General requirements.   
 **[11]** RFC 3647, Request for Comments: 3647, Internet X.509 Public Key Infrastructure: Certificate Policy and Certification Practices Framework, Chokhani, et al, November 2003.   
 **[12]** Všeobecné podmienky poskytovania a používania dôveryhodnej služby vyhotovovania a overovania certifikátov Disig, a.s.   
 **[13]** RFC 8659 DNS Certification Authority Authorization (CAA) Resource Record.   
 **[14]** RFC 8555 Automatic Certificate Management Environment (ACME).   
 **[15]** RFC 7231 Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content.   
 **[16]** RFC 7538 The Hypertext Transfer Protocol Status Code 308 (Permanent Redirect).   
 **[17]** RFC 6454 The Web Origin Concept.   
 **[18]** Informácia o spracúvaní osobných údajov, Disig, a.s. [https://eidas.disig.sk/pdf/info_oou_gdpr.pdf](https://eidas.disig.sk/pdf/info_oou_gdpr.pdf)  
 **[19]** RFC 6960 "X.509 Internet Public Key Infrastructure Online Certificate Status Protocol - OCSP".  
 **[20]** RFC 5019 The Lightweight Online Certificate Status Protocol (OCSP) Profile.   
 **[21]** RFC 8954 Online Certificate Status Protocol (OCSP) Nonce Extension.   
 **[22]** Network and Certificate System Security Requirements [https://cabforum.org/working-groups/netsec/documents/](https://cabforum.org/working-groups/netsec/documents/)  
 **[23]** RFC 6962 Certificate Transparency.  
 **[24]** CCADB Policy [https://www.ccadb.org/policy](https://www.ccadb.org/policy). 

### 1.6.4 Konvencie 
Kľúčové slová „MUSÍ“, „NESMIE“, „POVINNÉ“, „MAL BY“, „NEMALO BY“, „ODPORÚČANÉ“, „MÔŽE“ a „VOLITEĽNÉ“ v týchto CP/CPS sa musia interpretovať v súlade s RFC 2119.

# 2. Povinnosti pri zverejňovaní a úložiská

## 2.1 Úložiská
Úložisko musí byť umiestnené takým spôsobom, aby bolo prístupné Odberateľovi a Spoliehajúcim sa stranám a v súlade s celkovými bezpečnostnými požiadavkami.
Webové sídlo Poskytovateľa je verejne prístupné Odberateľom, Držiteľom TLS certifikátov, Spoliehajúcim sa stranám a verejnosti prostredníctvom internetu.

Poskytovateľ prevádzkuje jedno verejne prístupné úložisko (pozri časť 1), ktoré poskytuje aktuálne informácie relevantné pre tieto CP/CPS, vrátane:
* týchto CP/CPS a ich predchádzajúcich verzií;
* príslušných všeobecných obchodných podmienok poskytovania dôveryhodných služieb;
* certifikátov CA a ich odtlačkov (thumbprints);
* zoznamov zrušených certifikátov (CRL).  

Verejne dostupné informácie poskytované na webovom sídle Poskytovateľa majú charakter kontrolovaného prístupu.

## 2.2 Zverejňovanie informácií
Poskytovateľ poskytne on-line úložisko prístupné Zmluvným partnerom, Odberateľom a Spoliehajúcim sa stranám, ktoré bude obsahovať minimálne nasledujúce informácie:
* TLS certifikáty vydané v súlade s týmito CP/CPS,
* aktuálny zoznam CRL, ako aj všetky zoznamy CRL vydané od začiatku činnosti vydávania TLS certifikátov,
* certifikáty koreňových CA a podriadených certifikačných autorít prislúchajúce k ich verejným kľúčom, ku ktorým sa používajú zodpovedajúce súkromné kľúče pri podpisovaní TLS certifikátov a CRL,
* aktuálnu verziu CP/CPS,
* informácie o výsledku pravidelného auditu výkonu poskytovaných dôveryhodných služieb podľa časti 8.

Ak CA nedodrží akúkoľvek požiadavku aktuálnej verzie politiky „Mozilla Root Store Policy“ [5], či už ide o chybné vydanie certifikátu, procesný alebo prevádzkový problém, alebo akýkoľvek iný druh nesúladu – táto udalosť sa klasifikuje ako incident. Poskytovateľ je povinný bezodkladne nahlásiť všetky incidenty spoločnosti Mozilla vo forme Správy o incidente (Incident Report) a musí pravidelne aktualizovať túto správu, až kým zástupca spoločnosti Mozilla neoznačí príslušnú chybu (bug) za vyriešenú v systéme Bugzilla spoločnosti mozilla.org. Poskytovateľ by mal pozastaviť vydávanie certifikátov, kým sa nezabráni opätovnému výskytu problému.

Ak nie sú splnené podmienky stanovené v aktuálnej politike „Mozilla Root Store Policy“, za nahlásenie incidentu zodpovedá manažér certifikačnej autority Poskytovateľa vymenovaný do roly PMA.
Poskytovateľ zverejňuje vo svojom verejnom úložisku nasledujúce informácie, pričom zabezpečuje ich dostupnosť v režime 24x7:

### 2.2.1 Politiky a pravidlá 
Aktuálne a predchádzajúce verzie CP a CPS alebo kombinovaných CP/CPS sú zverejnené na adrese:

[https://eidas.disig.sk/en/provider/policies-and-documents/](https://eidas.disig.sk/en/provider/policies-and-documents/) - EN/SK verzia  
[https://eidas.disig.sk/sk/poskytovatel/politiky-a-dokumenty/](https://eidas.disig.sk/sk/poskytovatel/politiky-a-dokumenty/) - SK verzia

### 2.2.2 CA Certifikáty
Certifikáty pre koreňové certifikačné autority, podriadené certifikačné autority (vydávajúce certifikačné autority) a všetky príslušné krížové certifikáty sú zverejnené na adrese:

[https://eidas.disig.sk/en/certificates/ca/](https://eidas.disig.sk/en/certificates/ca/) - EN verzia  
[https://eidas.disig.sk/sk/certifikaty/ca/](https://eidas.disig.sk/sk/certifikaty/ca/) - SK verzia

### 2.2.3 Zoznamy zrušených certifikátov (CRLs) 
Zoznamy CRL sú k dispozícii na nasledujúcich URL adresách HTTP, aby sa predišlo cyklickým závislostiam počas overovania:

|CA        |CRL distribučný bod  |
|----------|:----------------------|
|CA Disig Root R2|http://cdp1.disig.sk/rootcar2/crl/rootcar2.crl<br>http://cdp2.disig.sk/rootcar2/crl/rootcar2.crl|
|CA Disig R2I2 Certification Service|http://cdp.disig.sk/subcar2i2/crl/subcar2i2.crl|
|CA Disig TLS Root R3|http://cdp.disig.sk/rootcar3/crl/rootcar3.crl|
|CA Disig R3I1 TLS Certification Service|http://cdp.disig.sk/subcar3i1/crl/subcar3i1.crl|

### 2.2.4 Testovacie webové stránky 
Na demonštráciu funkčnosti vydaných certifikátov na účely zaradenia do koreňového úložiska certifikačná autorita udržiava nasledujúce testovacie lokality:
|CA                                 |Typ stránky       |Adresa                                       |
|-----------------------------------|:---------------|---------------------------------------------------|
|CA Disig R2I2 Certification Service|Platná TLS Stránka  |https://testssl-valid-r2i2.disig.sk/index.en.html  |
|                                   |Exspirovaná TLS Stránka|https://testssl-expire-r2i2.disig.sk/index.en.html |
|                                   |Zrušená TLS Stránka|https://testssl-revoked-r2i2.disig.sk/index.en.html|

## 2.3 Čas alebo periodicita zverejňovania
TLS certifikát musí byť zverejnený ihneď po jeho vydaní. Informácie o vydanom TLS certifikáte musia byť dostupné na webovom sídle Poskytovateľa.

TLS certifikát sa zverejňuje okamžite po jeho vydaní a Odberateľ/Držiteľ certifikátu si ho môže ihneď prevziať. Informácie o vydaní TLS certifikátu sú dostupné v úložisku Poskytovateľa – pozri časť 1.

Zoznam zrušených certifikátov (CRL) sa zverejňuje spôsobom uvedeným v časti 4.9.7. Informácie o zrušenom TLS certifikáte musia byť dostupné na webovom sídle Poskytovateľa (pozri časť 1), ktoré slúži ako jeho úložisko.

Všetky informácie, ktoré sa majú zverejniť v úložisku, sa zverejnia v čo najkratšom možnom čase.

CRL sa zverejňuje spôsobom uvedeným v časti 4.9.8. Informácie o zrušenom TLS certifikáte možno nájsť v úložisku Poskytovateľa.

## 2.4 Kontrola prístupu k úložiskám
Poskytovateľ musí chrániť všetky informácie uložené v úložisku, ktoré nie sú prístupné verejnosti. Poskytovateľ vynaloží maximálne úsilie na zabezpečenie integrity, dôvernosti a dostupnosti údajov súvisiacich s poskytovaním dôveryhodných služieb. Musí tiež prijať logické a bezpečnostné opatrenia, aby zabránil neoprávnenému prístupu k úložisku osobám, ktoré by mohli údaje uložené v úložisku akýmkoľvek spôsobom zmeniť, poškodiť, pridať, odstrániť alebo vymazať.

Poskytovateľ chráni všetky informácie uložené v úložisku, ktoré nie sú určené na verejné šírenie, prostredníctvom technických a organizačných opatrení. Na tento účel vypracoval presné pravidlá obsiahnuté v bezpečnostnom projekte Poskytovateľa a súvisiacich usmerneniach.

Verejne dostupné informácie uvedené v úložisku Poskytovateľa majú charakter kontrolovaného prístupu.

# 3. Identifikácia a autentifikácia

## 3.1 Pomenovanie (Naming)
Poskytovateľ prijíma iba žiadosti o TLS certifikát, ktoré sú v súlade so štandardom PKCS #10 alebo SPKAC a sú vo formáte PEM, pokiaľ nebolo s Odberateľom vopred dohodnuté inak.

### 3.1.1 Typy mien
Žiadne ustanovenia.

### 3.1.2 Potreba zmysluplnosti mien
Žiadne ustanovenia.

### 3.1.3 Anonymita alebo pseudonym odberateľov
Žiadne ustanovenia.

### 3.1.4 Pravidlá interpretácie rôznych foriem mien
Interpretácia jednotlivých mien v TLS certifikátoch vydaných Poskytovateľom musí byť v súlade s profilmi TLS certifikátov opísanými v časti 7 týchto CP/CPS.

Jedinečné meno (distinguished name) použité v TLS certifikáte vydanom Poskytovateľom sa môže skladať z položiek, ktoré sú opísané v nasledujúcej časti.

#### 3.1.4.1 Nahrádzanie ne-ASCII znakov
Poskytovateľ umožňuje Žiadateľovi nahradiť slovenské diakritické znaky, ktoré sa môžu nachádzať v predmete TLS certifikátu (položky organizácia, lokalita), ich ekvivalentom v základnej tabuľke ASCII takto:

| Znak | ASCII ekvivalent || Znak | ASCII ekvivalent |
|:---:|:---:|:---:|:---:|:---:|
| á,ä | a || Á, Ä | A |
| č | c || Č | C |
| ď | d || Ď | D |
| dž | dz || DŽ | DZ |
| é | e || É | E |
| í | i || Í | I |
| ľ,ĺ | l || Ľ, Ĺ | L |
| ň | n || Ň | N |
| ó,ô | o || Ó,Ô | O |
| ŕ | r || Ŕ | R |
| š | s || Š | S |
| ť | t || Ť | T |
| ú | u || Ú | U |
| ý | y || Ý | Y |
| ž | z || Ž | Z |

#### 3.1.4.2 Certifikát
Tabuľka 1 obsahuje zoznam polí, ktoré môžu byť obsiahnuté v rovnakom poradí v predmete TLS certifikátu typu „Organization Validated“ (OV) vydaného Poskytovateľom.

Každý TLS certifikát musí obsahovať rozšírenie „subjectAltName“ (SAN) obsahujúce aspoň jeden záznam s plne kvalifikovaným doménovým menom (FQDN), pre ktoré je TLS certifikát určený.

Ako plne kvalifikované doménové meno bude akceptované aj meno obsahujúce hviezdičku (*) na tretej a vyššej pozícii v rámci FQDN (napr. *.disig.sk; *.mail.disig.sk atď.) a tento typ TLS certifikátu sa bude označovať ako „wildcard“ TLS certifikát.

Plne kvalifikované doménové meno nesmie byť obsiahnuté v žiadnom inom poli okrem CommonName (CN) a rozšírenia SubjectAlternativeName (SAN).

Tabuľka 1: Polia predmetu TLS certifikátu „Organization Validated“ a ich popis

| Názov položky | OID | Skr. | Popis | Poznámka |
|:---|:---:|:---:|:---|:---|
| countryName | 2.5.4.6 | C | Dvojznaková skratka názvu krajiny podľa ISO 3166-1 prislúchajúca k Subjektu. SK pre Slovenskú republiku | Povinné pole |
| localityName | 2.5.4.7 | L | Informácie o lokalite Subjektu | Povinné pole |
| organizationName| 2.5.4.10| O | Názov Subjektu alebo obchodné meno (DBA) | Povinné pole |
| commonName | 2.5.4.3 | CN | Plne kvalifikované doménové meno (FQDN), pre ktoré je TLS certifikát vydaný, uvedené v zázname SAN certifikátu | Povinné pole |

Znaky podčiarkovníka („_“ ASCII kód 0x5F) sa nesmú nachádzať v záznamoch dNSName.

### 3.1.5 Jedinečnosť mien
Žiadne ustanovenia.

### 3.1.6 Rozpoznávanie, autentifikácia a rola ochranných známok
Žiadne ustanovenia.

## 3.2 Prvotné overenie identity
Táto časť obsahuje politiky a postupy identifikácie a autentifikácie pre jednotlivé subjekty.

### 3.2.1 Metóda preukázania držby súkromného kľúča
Žiadne ustanovenia.

### 3.2.2 Autentifikácia identity organizácie a domény

#### 3.2.2.1 Autentifikácia identity
Právnická osoba (organizácia) so sídlom v Slovenskej republike preukazuje svoju totožnosť výpisom z Obchodného registra Slovenskej republiky alebo iného existujúceho registra právnických osôb. RA vyžaduje originál alebo úradne osvedčenú kópiu originálu, nie staršiu ako tri mesiace. Dôkazy musia obsahovať úplný názov spoločnosti, identifikátor (zvyčajne IČO), sídlo, meno osoby konajúcej za právnickú osobu a spôsob podpisovania za právnickú osobu.

V prípade, že sa právnická osoba nenachádza v Slovenskej republike, jej totožnosť sa overuje rovnakým spôsobom, ako je opísané vyššie. Výpis z aktuálneho registra právnických osôb musí byť úradne preložený do slovenského jazyka (okrem organizácií so sídlom v Českej republike).

Ak právnická osoba nemôže preukázať svoju totožnosť výpisom z obchodného registra, preukáže svoju existenciu písomne s odkazom na zákon alebo iné právne predpisy. Týka sa to len nepodnikateľských subjektov, ako sú obce, cirkev, občianske združenia, nadácie, orgány verejnej moci a pod. V prípade vydania TLS certifikátu právnická osoba preukáže pravdivosť identifikačných údajov uvedených v žiadosti o TLS certifikát predložením originálu dokumentu preukazujúceho túto skutočnosť k nahliadnutiu.
U Odberateľa/Držiteľa, ktorý žiada o TLS certifikát pre právnickú osobu, RA kontroluje predložené doklady preukazujúce existenciu danej právnickej osoby, ktorými je zvyčajne výpis z obchodného registra alebo iný ekvivalentný výpis z iného oficiálneho platného registra právnických osôb.

Fyzická osoba, ktorá na základe predloženého výpisu z obchodného registra koná v RA v mene danej právnickej osoby vo veci získania TLS certifikátu, preukáže svoju totožnosť podľa časti 3.2.3.
V mene právnickej osoby môže v RA konať len oprávnená osoba užívateľa, t. j. osoba, ktorá je jej štatutárnym orgánom (alebo viac takýchto osôb súčasne, ak to vyžaduje predložený výpis z obchodného registra), alebo môže byť právnická osoba zastúpená fyzickou osobou alebo inou právnickou osobou.

Ak je právnická osoba v RA zastúpená, zastupujúca fyzická alebo právnická osoba vždy predloží k nahliadnutiu overený výpis z obchodného registra zastupovanej právnickej osoby nie starší ako tri mesiace.
Ak právnickú osobu v RA zastupuje fyzická osoba, zastupujúca fyzická osoba preukáže svoju totožnosť v súlade s časťou 3.2.3 a preukáže sa aj úradne osvedčeným (notárom alebo matrikou) plnomocenstvom, z textu ktorého jasne vyplýva, že zastupujúca fyzická osoba bola splnomocnená zastupovanou právnickou osobou konať v danej veci v jej mene.

Ak právnickú osobu v RA zastupuje iná právnická osoba, táto zastupujúca právnická osoba okrem príslušného plnomocenstva (pozri predchádzajúci odsek) preukáže svoju totožnosť rovnakým spôsobom ako zastupovaná právnická osoba, ako sa vyžaduje vyššie.
Subjekt (fyzická alebo právnická osoba) zastupujúca právnickú osobu nesmie za žiadnych okolností dovoliť inému subjektu, aby zastupoval právnickú osobu, ktorú zastupuje, vo veciach týkajúcich sa ním zastupovanej právnickej osoby.

#### 3.2.2.2 DBA/Obchodné meno
Ak je obsahom TLS certifikátu identifikujúceho subjekt, ktorému je certifikát vydaný, obchodné meno (DBA) alebo obchodná značka, Poskytovateľ overí, či má Odberateľ právo používať dané DBA/obchodné meno, a to s využitím aspoň:  
**[1]** Dokumentácie poskytnutej vládnym orgánom alebo komunikácie s ním v jurisdikcii vzniku, existencie alebo uznania Žiadateľa;  
**[2]** Spoľahlivého zdroja údajov;  
**[3]** Komunikácie s vládnym orgánom zodpovedným za správu takýchto mien DBA alebo obchodných mien;  
**[4]** Potvrdzujúceho listu (Attestation Letter) sprevádzaného dokumentárnou podporou; alebo  
**[5]** Účtu za služby, bankového výpisu, výpisu z kreditnej karty, vládneho daňového dokladu alebo inej formy identifikácie, ktorú CA určí za dôveryhodnú.

#### 3.2.2.3 Overenie krajiny
Ak TLS certifikát obsahuje pole countryName, Poskytovateľ overí krajinu priradenú k Odberateľovi/Držiteľovi jedným z nasledujúcich spôsobov:  
**a)** Informáciami poskytnutými registrátorom domény;  
**b)** Jednou z metód uvedených v časti 3.2.2.1.  

U položky subjektu TLS certifikátu countryName overuje pracovník RA oprávnenosť spojenia uvedeného kódu krajiny so Zákazníkom/Držiteľom na základe informácií poskytovaných registrátorom domény resp. na základe iných predkladaných dokumentov uvedených vyššie.

#### 3.2.2.4 Overenie autorizácie alebo kontroly domény
Ak sa používa doménové meno (FQDN), predpokladom je, že príslušné domény druhého a vyššieho stupňa patria Odberateľovi žiadajúcemu o TLS certifikát.  
Poskytovateľ potvrdzuje, že v čase vydania TLS certifikátu overil všetky FQDN v certifikáte.  
Overenie sa vykoná v stanovenom čase pred vydaním TLS certifikátu.  
Overenie, že Odberateľ je vlastníkom domény alebo má kontrolu nad doménou, ktorej FQDN je v zázname CN alebo bude uvedené v Subject Alternative Name (SAN), vykoná Poskytovateľ pomocou jednej z metód špecifikovaných v tomto odseku.

##### 3.2.2.4.1 Overenie Žiadateľa ako doménového kontaktu
Táto metóda bola zrušená a nesmie sa používať.

##### 3.2.2.4.2 E-mail, fax, SMS alebo poštová zásielka doménovému kontaktu
Táto metóda bola zrušená a nesmie sa používať.

##### 3.2.2.4.3 Telefonický kontakt s doménovým kontaktom
Táto metóda bola zrušená a nesmie sa používať.

##### 3.2.2.4.4 Konštruovaný e-mail doménovému kontaktu
Poskytovateľ túto metódu nepoužíva.

##### 3.2.2.4.5 Dokument o autorizácii domény
Táto metóda bola zrušená a nesmie sa používať.

##### 3.2.2.4.6 Dohodnutá zmena na webovom sídle
Táto metóda bola zrušená a nesmie sa používať.

##### 3.2.2.4.7 Zmena v DNS
Potvrdenie kontroly Odberateľa nad FQDN potvrdením prítomnosti náhodnej hodnoty (Random Value) v zázname DNS TXT buď   
**1)** autorizačného doménového mena; alebo  
**2)** autorizačného doménového mena, ktoré má predponu s označením domény začínajúcim znakom podčiarkovníka.

Ak sa použije náhodná hodnota, Poskytovateľ poskytne náhodnú hodnotu jedinečnú pre žiadosť o certifikát a nesmie túto hodnotu použiť po uplynutí:  
**i)** 30 dní alebo  
**ii)** ak Žiadateľ predložil žiadosť o certifikát, časového rámca povoleného na opätovné použitie overených informácií relevantných pre certifikát (napríklad v časti 4.2.1 TLS BR [3]).  

Po overení FQDN touto metódou MÔŽE CA vydávať certifikáty aj pre iné FQDN, ktoré končia všetkými označeniami domén overeného FQDN. Táto metóda je vhodná na overovanie Wildcard doménových mien.

Táto metóda je k dispozícii pre RA ako automatizovaný spôsob overovania vlastníctva a kontroly nad doménou, kde systém používaný na generovanie TLS certifikátov posiela jedinečnú náhodne vygenerovanú hodnotu pre každé FQDN, u ktorého sa očakáva, že bude v SAN vydaného certifikátu, s podmienkou, že táto hodnota musí byť zaregistrovaná v zázname DNS TXT pre každé FQDN a musí byť zaregistrovaná aj pre všetky nižšie úrovne až po druhú úroveň daných FQDN.

Následne systém CA automaticky skontroluje prítomnosť TXT hodnoty v záznamoch DNS. Overenie náhodne vygenerovanej jedinečnej hodnoty pre dané FQDN sa použije na overenie maximálne do 30 dní od jej odoslania. Údaje o overení získané touto metódou možno použiť na overenie vlastníctva a kontroly nad rovnakým FQDN, ak nie sú staršie ako 398 dní.

##### 3.2.2.4.8 IP adresa
Poskytovateľ túto metódu nepoužíva.

##### 3.2.2.4.9 Testovací certifikát
Táto metóda bola zrušená a nesmie sa používať.

##### 3.2.2.4.10 TLS s použitím náhodnej hodnoty
Táto metóda bola zrušená a nesmie sa používať.

##### 3.2.2.4.11 Akákoľvek iná metóda
Táto metóda bola zrušená a nesmie sa používať.

##### 3.2.2.4.12 Overenie Žiadateľa ako doménového kontaktu
Poskytovateľ túto metódu nepoužíva.

##### 3.2.2.4.13 E-mail na kontakt v DNS CAA
Potvrdenie kontroly Odberateľa nad FQDN zaslaním náhodnej hodnoty e-mailom a následným prijatím potvrdzujúcej odpovede s použitím tejto náhodnej hodnoty. Náhodná hodnota musí byť zaslaná na e-mailový kontakt uvedený v DNS CAA zázname. Príslušný súbor zdrojových záznamov CAA sa vyhľadá pomocou vyhľadávacieho algoritmu definovaného v RFC 8659, časť 3 [13].

Každý e-mail môže potvrdiť kontrolu nad viacerými FQDN za predpokladu, že každá e-mailová adresa je kontaktom DNS CAA pre každé overované autorizačné doménové meno. Ten istý e-mail môže byť zaslaný viacerým príjemcom, pokiaľ sú všetci príjemcovia kontaktmi DNS CAA pre každé overované doménové meno.

Náhodná hodnota MUSÍ byť v každom e-maile jedinečná. E-mail môže byť preposlaný v celom rozsahu, vrátane opätovného použitia náhodnej hodnoty, za predpokladu, že jeho celý obsah a príjemca(ovia) zostanú nezmenení. Náhodná hodnota zostáva platná pre použitie v potvrdzujúcej odpovedi najviac 30 dní od jej vytvorenia.

Autority používajúce túto metódu MUSIA implementovať viacperspektívne potvrdzovanie vydávania (Multi-Perspective Issuance Corroboration) podľa časti 3.2.2.9.
Po overení FQDN touto metódou môže CA vydávať TLS certifikáty aj pre iné FQDN, ktoré končia všetkými označeniami domén overeného FQDN (vhodné pre Wildcard).

##### 3.2.2.4.14 E-mail na kontakt v DNS TXT
Potvrdenie kontroly Žiadateľa nad FQDN zaslaním náhodnej hodnoty e-mailom a následným prijatím potvrdzujúcej odpovede. Náhodná hodnota sa zasiela na e-mailový kontakt zo záznamu DNS TXT pre vybrané doménové meno.
Ostatné podmienky (jedinečnosť, platnosť 30 dní, viacperspektívne overovanie) sú rovnaké ako v bode 3.2.2.4.13.

##### 3.2.2.4.15 Telefonický kontakt s doménovým kontaktom
Táto metóda bola zrušená a nesmie sa používať.

##### 3.2.2.4.16 Telefonický kontakt s kontaktom v DNS TXT zázname
Poskytovateľ túto metódu nepoužíva.

##### 3.2.2.4.17 Telefonický kontakt s kontaktom v DNS CAA zázname
Poskytovateľ túto metódu nepoužíva.

##### 3.2.2.4.18 Dohodnutá zmena na webovom sídle v2
Poskytovateľ túto metódu nepoužíva.

##### 3.2.2.4.19 Dohodnutá zmena na webovom sídle – ACME
Potvrdenie kontroly žiadateľa nad FQDN sa vykonáva overením kontroly domény FQDN pomocou metódy ACME HTTP Challenge definovanej v časti 8.3 RFC 8555 [14], s nasledujúcimi dodatočnými požiadavkami:  
* Poskytovateľ musí prijať úspešnú HTTP odpoveď (stavový kód 2xx);  
* Token sa nesmie používať viac ako 30 dní od jeho vytvorenia;  
* Ak Poskytovateľ používa presmerovania, platia nasledujúce podmienky:
   **1.** Presmerovania musia byť iniciované na úrovni protokolu HTTP.  
      **a.** Presmerovania musia byť výsledkom odpovede so stavovým kódom HTTP 301, 302 alebo 307, ako je definované v RFC 7231 [15], časť 6.4, alebo odpovede so stavovým kódom HTTP 308, ako je definované v RFC 7538 [16], časť 3. Presmerovania musia smerovať na konečnú hodnotu hlavičky odpovede HTTP Location, ako je definované v RFC 7231 [15], časť 7.1.2;  
   **2.** presmerovania musia smerovať na URL adresy zdrojov so schémou „http“ alebo „https“;  
   **3.** presmerovania musia smerovať na URL adresy zdrojov, ku ktorým sa pristupuje cez Autorizované porty.  

Okrem doménových mien .onion musia CA vykonávajúce overenie touto metódou implementovať viacperspektívne potvrdzovanie vydávania podľa časti 3.2.2.9.
Táto metóda nie je vhodná na overovanie wildcard doménových mien.

##### 3.2.2.4.20 TLS s použitím ALPN
Poskytovateľ túto metódu nepoužíva.

##### 3.2.2.4.21 DNS označené Account ID – ACME
Poskytovateľ túto metódu nepoužíva.

##### 3.2.2.4.22 Záznam DNS TXT s perzistentnou hodnotou
Poskytovateľ túto metódu nepoužíva.

#### 3.2.2.5 Autentifikácia pre IP adresu
Poskytovateľ nevydáva TLS certifikáty, ak je v poli commonName alebo v rozšírení subjectAlternativeName IP adresa.

#### 3.2.2.6 Overenie Wildcard domény
Pred vydaním TLS certifikátu s hviezdičkou (\*) v CN alebo SAN typu DNS-ID Poskytovateľ stanoví a dodržiava zdokumentovaný postup, ktorý určí, či sa hviezdička nachádza na prvej pozícii vľavo od označenia kontrolovaného registrom alebo či ide o „verejnú príponu“ (public suffix, napr. „*.com“, „*.co.uk“).

Pracovník RA overí žiadosť o wildcard certifikát kontrolou, či je hviezdička na prvej pozícii zľava a či za ňou nasleduje bodka. Zároveň skontroluje, či je certifikát vydávaný pre doménu tretej a vyššej úrovne (napr. *.domena.sk). Overenie domény sa vykoná podľa 3.2.2.4.

#### 3.2.2.7 Presnosť zdroja údajov
Pred použitím akéhokoľvek zdroja údajov ako dôveryhodného zdroja Poskytovateľ overí jeho spoľahlivosť, presnosť a odolnosť voči zmenám alebo falšovaniu.

#### 3.2.2.8 Záznamy CAA
Ako súčasť procesu vydania certifikátu musí Poskytovateľ skontrolovať záznam CAA pre každý dNSName uvedený v prípone subjectAltName vydaného certifikátu TLS v súlade s postupom v RFC 8659 a pokynmi na spracovanie uvedenými v RFC 8659 [13] pre všetky nájdené záznamy.

Niektoré metódy, ktoré sa spoliehajú na overenie vlastníctva alebo kontroly Žiadateľa nad predmetnou doménou (doménami) (pozri časť 3.2.2.4), aby boli uvedené v certifikáte TLS, vyžadujú, aby boli záznamy CAA pred vydaním certifikátu načítané a spracované z ďalších vzdialených sieťových perspektív (pozri časť 3.2.2.9). Na potvrdenie primárnej sieťovej perspektívy sa odpoveď na kontrolu CAA od vzdialenej sieťovej perspektívy interpretuje ako povolenie na vydanie bez ohľadu na to, či sú odpovede z oboch perspektív bajt po bajte identické. Okrem toho môže CA považovať odpoveď zo vzdialenej sieťovej perspektívy za potvrdzujúcu, ak jedna alebo obe perspektívy zaznamenajú prijateľné zlyhanie vyhľadávania záznamu CAA, ako je definované v časti 3.2.2.8 TLS BR. [3]

Ak Poskytovateľ vydá certifikát, musí tak urobiť do TTL záznamu CAA alebo do 8 hodín, podľa toho, ktorá doba je vyššia.

Zamestnanec RA musí pred vydaním certifikátu TLS skontrolovať zverejnený záznam CAA. Ak zistí, že takýto záznam existuje, nesmie vydať certifikát TLS, kým sa nepotvrdí, že žiadosť o certifikát TLS je v súlade s príslušným záznamom v CAA.
Overenie záznamu sa vykonáva pre každé FQDN uvedené v CN žiadosti alebo to, ktoré má byť uvedené v SAN takým spôsobom, že strom mien postupuje zľava doprava, napr. pri kontrole záznamu CAA žiadosti, ktorá obsahuje FQDN vo formáte X.Y.X, sa kontrola vykonáva v poradí X.Y.X -> Y.Z -> Z, pokiaľ Z nie je národná úroveň, napr. ".sk".

#### 3.2.2.9 Viacperspektívne potvrdzovanie vydávania (Multi-Perspective Issuance Corroboration)
Viacperspektívna korektorácia vydania certifikátu sa pokúša overiť určenia (t. j. úspešnosť/neúspech overenia domény, povolenie/zákaz CAA) vykonané primárnou sieťovou perspektívou z viacerých vzdialených sieťových perspektív pred vydaním certifikátu TLS. Tento proces môže zlepšiť ochranu pred útokmi alebo únosmi protokolu BGP (Border Gateway Protocol) s rovnako špecifickým prefixom.  

CA môže použiť buď rovnakú sadu, alebo rôzne sady sieťových perspektív pri vykonávaní viacperspektívnej korektorácie vydania certifikátu pre požadované:
* Autorizáciu alebo kontrolu domény; a    
* Kontroly záznamov CAA.  

Súbor odpovedí zo sieťových perspektív, na ktoré sa spolieha, poskytne CA potrebné informácie, aby mohla pozitívne posúdiť:

**a)** prítomnosť očakávanej:    
* Náhodnej hodnoty;    
* Tokenu požiadavky;    
* IP adresy; alebo    
* Kontaktnej adresy;  

ako to vyžaduje overovacia metóda uvedená v oddieloch 3.2.2.4 a

**b)** oprávnenie Poskytovateľa vydávať pre požadovanú(é) doménu(y), ako je uvedené v oddiele 3.2.2.8.  

Oddiel 3.2.2.4 opisuje overovacie metódy, ktoré vyžadujú použitie viacperspektívnej korekcie vydania, a ako môže sieťová perspektíva potvrdiť výsledky určené primárnou sieťovou perspektívou.

Výsledky alebo informácie získané z jednej sieťovej perspektívy sa nesmú opätovne použiť ani uložiť do vyrovnávacej pamäte pri vykonávaní overovania prostredníctvom následných sieťových perspektív (napr. rôzne sieťové perspektívy sa nemôžu spoliehať na zdieľanú vyrovnávaciu pamäť DNS, aby zabránili protivníkovi s kontrolou prevádzky z jednej sieťovej perspektívy znehodnotiť vyrovnávaciu pamäť DNS používanú inými sieťovými perspektívami). Sieťová infraštruktúra poskytujúca internetové pripojenie k sieťovej perspektíve môže byť spravovaná tou istou organizáciou, ktorá poskytuje výpočtové služby potrebné na prevádzku sieťovej perspektívy. Všetka komunikácia medzi vzdialenou sieťovou perspektívou a Poskytovateľom sa musí uskutočňovať cez overený a šifrovaný kanál, ktorý sa opiera o moderné protokoly (napr. cez HTTPS).

Sieťová perspektíva môže používať rekurzívny DNS resolver, ktorý nie je umiestnený spolu so sieťovou perspektívou. DNS resolver používaný sieťovou perspektívou však musí spadať do rovnakého regiónu regionálnej služby internetového registra ako sieťová perspektíva, ktorá sa naň spolieha. Okrem toho, pre akýkoľvek pár DNS resolverov použitých pri pokuse o Multi-Perspective Issuance Corroboration (Multi-Perspektívna korektorová služba), musí byť priama vzdialenosť medzi dvoma štátmi, provinciami alebo krajinami, v ktorých sa DNS resolvery nachádzajú, aspoň 500 km. Poloha DNS resolvera je určená bodom, kde sa nezapuzdrené odchádzajúce DNS dotazy zvyčajne najprv odovzdávajú sieťovej infraštruktúre, ktorá poskytuje internetové pripojenie tomuto DNS resolveru.

Poskytovateľ môže okamžite zopakovať Multi-Perspective Issuance Corroboration (Multi-Perspektívna korektorová služba) pomocou rovnakej metódy overenia alebo alternatívnej metódy (napr. Poskytovateľ môže okamžite zopakovať overenie pomocou „Email to DNS TXT Contact“ (E-mail na DNS TXT kontakt), ak „Agreed-Upon Change to Website - ACME“ (Dohodnutá zmena webovej stránky - ACME) nepotvrdzuje výsledok Multi-Perspective Issuance Corroboration (Multi-Perspektívna korektorová služba). Pri opakovanom pokuse o potvrdenie vydania z viacerých perspektív sa poskytovateľ nebude spoliehať na potvrdenia z predchádzajúcich pokusov. Neexistuje žiadne ustanovenie týkajúce sa maximálneho počtu pokusov o validáciu, ktoré je možné vykonať v akomkoľvek časovom období.

Tabuľka „Požiadavky na kvórum“ popisuje požiadavky na kvórum súvisiace s potvrdením vydania z viacerých perspektív. Ak sa poskytovateľ nespolieha na rovnaký súbor sieťových perspektív pre kontroly autorizácie alebo kontroly domény aj záznamov CAA, požiadavky na kvórum musia byť splnené pre oba súbory sieťových perspektív (t. j. súbor autorizácie alebo kontroly domény a súbor kontrol záznamov CAA). Sieťové perspektívy sa považujú za odlišné, keď je priama vzdialenosť medzi dvoma štátmi, provinciami alebo krajinami, v ktorých sa nachádzajú, aspoň 500 km. Sieťové perspektívy sa považujú za „vzdialené“, keď sú odlišné od primárnej sieťovej perspektívy a ostatných sieťových perspektív zastúpených v kvóre.

Poskytovateľ môže opätovne použiť potvrdzujúce dôkazy pre súlad s kvórom záznamov CAA maximálne 398 dní. Po vydaní certifikátu pre doménu môže vzdialená spoločnosť Network Perspectives v nasledujúcich žiadostiach o certifikát od toho istého žiadateľa vynechať načítanie a spracovanie záznamov CAA pre tú istú doménu alebo jej poddomény, a to maximálne na 398 dní.

Tabuľka 2: Požiadavky na kvórum
| Počet použitých samostatných<br>vzdialených perspektív | Počet povolených nepotvrdení |
|:---:|:---:|
| 2 - 5 | 1 |
| 6+ | 2 |

S účinnosťou od 15. marca 2025 Poskytovateľ implementuje viacperspektívne potvrdzovanie vydávania (Multi-Perspective Issuance Corroboration) s použitím aspoň dvoch (2) vzdialených sieťových perspektív (Network Perspectives). Poskytovateľ môže pokračovať vo vydávaní TLS certifikátu, ak je počet vzdialených sieťových perspektív, ktoré nepotvrdia rozhodnutia prijaté primárnou sieťovou perspektívou („nepotvrdenia“), vyšší, než je povolené v tabuľke 4 Požiadavky na kvórum.  

S účinnosťou od 15. septembra 2025 Poskytovateľ implementuje viacperspektívne potvrdzovanie vydávania s použitím aspoň dvoch (2) vzdialených sieťových perspektív. Poskytovateľ nesmie pokračovať vo vydávaní TLS certifikátu, ak je počet nepotvrdení vyšší, než je povolené v tabuľke 4 Požiadavky na kvórum.  

S účinnosťou od 15. marca 2026 Poskytovateľ implementuje viacperspektívne potvrdzovanie vydávania s použitím aspoň troch (3) vzdialených sieťových perspektív. Poskytovateľ nesmie pokračovať vo vydávaní TLS certifikátu, ak je počet nepotvrdení vyšší, než je povolené v požiadavkách na kvórum v tabuľke 4 a ak vzdialené sieťové perspektívy, ktoré potvrdzujú rozhodnutia prijaté primárnou sieťovou perspektívou, nespadajú do servisných regiónov aspoň dvoch (2) samostatných regionálnych internetových registrov (Regional Internet Registries).  

S účinnosťou od 15. júna 2026 Poskytovateľ implementuje viacperspektívne potvrdzovanie vydávania s použitím aspoň štyroch (4) vzdialených sieťových perspektív. Poskytovateľ nesmie pokračovať vo vydávaní TLS certifikátu, ak je počet nepotvrdení vyšší, než je povolené v požiadavkách na kvórum v tabuľke 4 a ak vzdialené sieťové perspektívy, ktoré potvrdzujú rozhodnutia prijaté primárnou sieťovou perspektívou, nespadajú do servisných regiónov aspoň dvoch (2) samostatných regionálnych internetových registrov. 

S účinnosťou od 15. decembra 2026 Poskytovateľ implementuje viacperspektívne potvrdzovanie vydávania s použitím aspoň piatich (5) vzdialených sieťových perspektív. Poskytovateľ nesmie pokračovať vo vydávaní TLS certifikátu, ak je počet nepotvrdení vyšší, než je povolené v tabuľke 4 Požiadavky na kvórum a ak vzdialené sieťové perspektívy, ktoré potvrdzujú rozhodnutia prijaté primárnou sieťovou perspektívou, nespadajú do servisných regiónov aspoň dvoch (2) samostatných regionálnych internetových registrov.

### 3.2.3 Autentifikácia identity jednotlivca 
Poskytovateľ zaručí v prípade, že je TLS certifikát vydaný pre zariadenie alebo systém, ktorý môže používať TLS certifikát, aby identita zariadenia alebo systému bola s jeho verejným kľúčom zodpovedajúcim spôsobom prepojená.  

Z tohto dôvodu musí byť zariadenie systémom priradeným fyzickej osobe alebo fyzickej osobe konajúcej v mene právnickej osoby (Odberateľ), ktorá ich spravuje.
Táto fyzická osoba poskytne CMA nasledujúce informácie:  
* Identifikáciu zariadenia alebo systému;  
* Verejné kľúče zariadenia alebo systému (zahrnuté v žiadosti o TLS certifikát);  
* Autorizáciu zariadenia alebo systému (ak má byť nejaká zahrnutá v TLS certifikáte);  
* Kontaktné údaje, ktoré Poskytovateľovi umožnia v prípade potreby komunikovať s touto fyzickou osobou.  

Poskytovateľ overí presnosť všetkých informácií (hodnoty polí rozlišovacieho mena), ktoré majú byť uvedené v TLS certifikáte.
Metódy na vykonávanie overovania údajov zahŕňajú:  
* Overenie identity fyzickej osoby v súlade s požiadavkami tejto časti;  
* Overenie identity osoby, ktorej komponent patrí, v súlade s požiadavkami časti 3.2.2; 
* Overenie oprávnenosti údajov, ktoré majú byť uvedené v každom poli TLS certifikátu, s dôrazom na obsah poľa commonName;
Poznámka: Typickou hodnotou tohto poľa je plne kvalifikované doménové meno (FQDN).  
Poskytovateľ špecifikuje postupy na autentifikáciu identity Držiteľa certifikátu. Poskytovateľ zaznamená tento proces pre každý TLS certifikát v písomnej alebo elektronickej forme. Dokumentácia o autentifikácii musí obsahovať aspoň:
* identitu osoby vykonávajúcej autentifikáciu;  
* jednoznačné identifikačné údaje z dokumentov preukazujúcich identitu Držiteľa TLS certifikátu;  
* dátum identifikácie.  

Overenie identity vykoná pracovník RA na základe dokumentu obsahujúceho nasledujúce údaje Držiteľa:  
* úplné meno a priezvisko;  
* adresu trvalého pobytu;  
* rodné číslo (osoby, ktoré ho majú pridelené);  
* dátum narodenia (osoby, ktoré nemajú pridelené rodné číslo).  

Zároveň Odberateľ/Držiteľ poskytne ďalší dokument, ktorý obsahuje aspoň meno a priezvisko Držiteľa a ďalšie osobné údaje (dátum narodenia, rodné číslo). Toto neplatí, ak ide o služobný preukaz.
Poskytovateľ zaznamená z dokumentov aj nasledujúce údaje:  
* číslo občianskeho preukazu;
* vydavateľa občianskeho preukazu;  
* dátum platnosti občianskeho preukazu, ak je vyznačený.  

Poskytovateľ pri overovaní identity Držiteľa akceptuje nasledujúce dokumenty:  
* občiansky preukaz;  
* cestovný pas;  
* vodičský preukaz; 
* rodný list;  
* služobný preukaz;  
* preukaz poistenca verejného zdravotného poistenia; 
* zbrojný preukaz.  

V prípade predloženia rodného listu, zbrojného preukazu, služobného preukazu alebo preukazu poistenca verejného zdravotného poistenia musí byť predložený aj jeden z nasledujúcich dokumentov: občiansky preukaz, cestovný pas.
Ak fyzická osoba zastupuje inú fyzickú osobu, predloží aj úradne overené plnomocenstvo, z textu ktorého je jasne zrejmé, že zastupujúca fyzická osoba bola splnomocnená splnomocňujúcou fyzickou osobou konať v danej veci v jej mene.
Súčasťou autentifikácie Držiteľa je povinné poskytnutie vybranej e-mailovej adresy, ktorá bude uložená spolu s jeho osobnými údajmi v IS Poskytovateľa, a ktorá bude slúžiť výslovne na komunikáciu medzi Poskytovateľom a Držiteľom certifikátu a nebude súčasťou vydaného TLS certifikátu. Poskytovateľ nebude overovať, či zadaná e-mailová adresa skutočne patrí Držiteľovi.  

Všetky dokumenty poskytnuté RA Odberateľmi musia byť buď originály, alebo úradne overené kópie originálov. Nesmú do nich byť pridávané žiadne informácie, nesmú byť menené, prečiarkované atď. Dokumenty, na ktorých je vyznačená doba ich platnosti, musia byť platné.
Ak má pracovník RA pochybnosti o identite potenciálneho Odberateľa (napr. zjavný nesúlad medzi fotografiou v osobnom doklade a vzhľadom Odberateľa, rozpor medzi dvoma predloženými dokladmi atď.), môže jeho registráciu odmietnuť.
Akékoľvek dokumenty v cudzom jazyku (okrem češtiny) musia byť preložené do slovenčiny úradným prekladateľom - znalcom.  

Na žiadosť Odberateľa alebo RA sa akékoľvek sporné prípady pri preukazovaní identity vyriešia postupom podľa časti 9.13.
Pri predkladaní dokumentov sa vyžaduje, aby boli RA poskytnuté originály týchto dokumentov k nahliadnutiu a kópie originálov (nemusia byť overené), s výnimkou osobných dokladov identifikujúcich identitu Odberateľa, ktoré sa používajú na archiváciu pre potreby Poskytovateľa.  

Poskytnutie výpisu z obchodného registra získaného z internetu Odberateľom nie je postačujúce, keďže tento výpis je len informatívny a nemôže byť použitý na právne úkony.
Pracovník RA skontroluje na dokumentoch nasledujúce skutočnosti:  
* Osobné doklady fyzickej osoby:  
   **a)** súlad údajov uvedených v žiadosti s údajmi uvedenými v osobných dokladoch;  
   **b)** platnosť predloženého dokumentu;  
   **c)** plnoletosť fyzickej osoby (t. j. vek 18 rokov);  
   **d)** zhodu medzi fotografiou v osobnom doklade a vzhľadom majiteľa osobného dokladu;  
   **e)** zhodu v predložených dokumentoch, t. j. či údaje na jednom dokumente nie sú v rozpore s údajmi na inom dokumente.  

* Výpisy z obchodného registra alebo z iného registra právnických osôb:  
   **a)** platnosť výpisu – nesmie byť starší ako 3 mesiace;  
   **b)** konanie v mene právnickej osoby – t. j. či fyzická osoba (osoby), ktorá predložila daný výpis, má právo konať (podpisovať) v mene danej právnickej osoby;  
   **c)** forma výpisu – originál alebo úradne (notársky/matrikou) overená kópia výpisu.  

* Súhlas s vydaním TLS certifikátu:  
   **a)** oprávnenie konať v mene spoločnosti – osoba podpisujúca súhlas musí byť oprávnená zastupovať Odberateľa. Oprávnenosť sa kontroluje podľa výpisu zo živnostenského registra alebo iného registra stanoveného zákonom (alebo zakladateľskej listiny, plnomocenstva, menovacieho dekrétu). Ak podpisujúca osoba nie je zapísaná v tomto výpise, musí poskytnúť iný dokument, na základe ktorého môže konať v mene Odberateľa (zvyčajne plnomocenstvo overené notárom);     
   **b)** Platnosť – ak je v súhlase uvedená doba platnosti súhlasu, kontroluje sa aj táto informácia.  

* Plnomocenstvá:  
   **a)** overenie plnomocenstva (notárom/matrikou);   
   **b)** zhodu údajov uvedených v plnomocenstve, ktoré definuje zastupujúcu fyzickú alebo právnickú osobu, s údajmi uvedenými v osobných dokladoch zastupujúcej fyzickej osoby alebo s údajmi uvedenými vo výpise z obchodného alebo iného registra zastupujúcej právnickej osoby;  
   **c)** rozsah plnomocenstva – t. j. či plnomocenstvo oprávňuje splnomocnenú fyzickú alebo právnickú osobu na vykonanie požadovaného úkonu na RA v mene splnomocňujúcej fyzickej alebo právnickej osoby;  
   **d)** časové obmedzenie alebo inú podmienku uvedenú v plnomocenstve. 

Poskytovateľ môže prijať aj dokumenty predložené Odberateľom v elektronickej forme, podpísané platným kvalifikovaným elektronickým podpisom alebo kvalifikovanou elektronickou pečaťou (výpis z obchodného registra, plnomocenstvo, vyhlásenie, poverenie atď.).
Fyzickou osobou môže byť dospelý občan Slovenskej republiky alebo cudzí štátny príslušník.  
Fyzická osoba musí preukázať svoju totožnosť dvoma z nasledujúcich osobných dokladov:
* povolenie na prechodný pobyt (alebo trvalý pobyt) v prípade cudzinca;  
* zbrojný preukaz;  
* služobný preukaz. 

Vyžaduje sa, aby aspoň jeden z predložených dokladov bol doklad, ktorý obsahuje fotografiu danej osoby. V prípade predloženia rodného listu, zbrojného preukazu alebo služobného preukazu musí byť predložený aj jeden z nasledujúcich dokladov: občiansky preukaz alebo cestovný pas.
Ak fyzická osoba zastupuje inú fyzickú osobu v RA, musí preukázať svoju totožnosť aj úradne overeným (notárom alebo matrikou) plnomocenstvom, z textu ktorého jasne vyplýva, že zastupujúca fyzická osoba bola splnomocnená splnomocňujúcou fyzickou osobou konať v danej veci v jej mene.  

Ak právnická osoba zastupuje fyzickú osobu, musí splnomocnená právnická osoba okrem plnomocenstva (pozri predchádzajúci odsek) preukázať svoju totožnosť v súlade s časťou 3.2.2.  

Subjekt (fyzická alebo právnická osoba) zastupujúca fyzickú osobu nesmie byť za žiadnych okolností zastúpený iným subjektom vo veciach týkajúcich sa ním zastupovanej fyzickej osoby.  

### 3.2.4 Neoverené informácie o odberateľovi  

Počas počiatočného vydania sa e-mailová adresa neoveruje. 

### 3.2.5 Overenie oprávnenia  

Ak je Žiadateľom o TLS certifikát obsahujúci informácie o identite subjektu organizácia, Poskytovateľ použije spoľahlivú metódu komunikácie na overenie autenticity žiadosti o TLS certifikát zástupcu žiadateľa.
Poskytovateľ môže použiť zdroje uvedené v časti 3.2.2.1 ako spoľahlivú metódu komunikácie. Za predpokladu, že Poskytovateľ použije spoľahlivú metódu komunikácie, môže Poskytovateľ overiť autenticitu žiadosti o TLS certifikát priamo u zástupcu Žiadateľa alebo u autoritatívneho zdroja v rámci organizácie Žiadateľa, ako sú hlavné obchodné kancelárie Žiadateľa, administratívne kancelárie, personálne oddelenia, oddelenia informačných technológií alebo iné oddelenie, ktoré CA považuje za vhodné.  

Okrem toho Poskytovateľ zavedie proces, ktorý Žiadateľovi umožní špecifikovať jednotlivcov, ktorí môžu žiadať o TLS certifikáty. Ak Žiadateľ písomne špecifikuje jednotlivcov, ktorí môžu žiadať o TLS certifikát, potom Poskytovateľ neprijme žiadne žiadosti o TLS certifikát, ktoré sú mimo tejto špecifikácie. Poskytovateľ poskytne Žiadateľovi zoznam ním autorizovaných žiadateľov o TLS certifikát na základe overenej písomnej žiadosti Žiadateľa.  

### 3.2.6 Kritériá pre interoperabilitu alebo certifikáciu  
Poskytovateľ zverejní všetky krížovo certifikované TLS certifikáty podriadených CA, ktoré identifikujú Poskytovateľa ako subjekt, za predpokladu, že CA dohodla alebo akceptovala vytvorenie vzťahu dôvery.  

## 3.3 Identifikácia a autentifikácia pri žiadostiach o nový kľúč (re-key)  

### 3.3.1 Identifikácia a autentifikácia pri rutinnom re-key  
Žiadne ustanovenia.  

### 3.3.2 Identifikácia a autentifikácia pri re-key po zrušení  
Po zrušení TLS certifikátu musí žiadateľ o následný TLS certifikát absolvovať všetky požiadavky počiatočnej registrácie. 

## 3.4 Identifikácia a autentifikácia pre žiadosť o zrušenie 
Žiadne ustanovenia.  

# 4. Prevádzkové požiadavky na životný cyklus certifikátu  

## 4.1 Žiadosť o certifikát  

### 4.1.1 Kto môže podať žiadosť o TLS certifikát  
O TLS certifikát môže požiadať fyzická alebo právnická osoba prevádzkujúca zariadenie alebo systém, ktorá v žiadosti o TLS certifikát preukáže, že je oprávnená žiadať o TLS certifikát s FQDN a že všetky FQDN sú uvedené v SAN TLS certifikátu.
Poskytovateľ vedie internú databázu všetkých zrušenýchatnených TLS certifikátov a zamietnutých žiadostí z dôvodu podozrenia z phishingu alebo inej podvodnej aktivity.  

### 4.1.2 Proces registrácie a zodpovednosti  

#### 4.1.2.1 Príprava  
Zmluvný partner/Odberateľ podnikne nasledujúce kroky na prípravu návštevy u Poskytovateľa:     
* Oboznámi sa s dokumentmi „Všeobecné podmienky poskytovania a používania dôveryhodnej služby vydávania a overovania certifikátov“ [12] a „Informácia o spracúvaní osobných údajov“ [18], ktoré musia byť prístupné na trvalom komunikačnom kanáli (pozri [https//eidas.disig.sk/sk/documents/](https//eidas.disig.sk/sk/documents/));  
* Oboznámi sa s týmto postupom, prípadne so zásadami a pokynmi na získanie TLS certifikátu;  
* Pripraví si hodnoty každého poľa žiadosti o TLS certifikát tak, aby tieto hodnoty boli v súlade s týmito CP/CPS (pozri odsek 3.1.4); 
* Pripraví si žiadosť o TLS certifikát vo forme PKCS #10 alebo SPKAC, ktorá bude vopred zaslaná Poskytovateľovi (pozri odsek 4.1.4);  
* Pripraví si vybrané doklady totožnosti a ďalšie potrebné dokumenty, t. j. výpis z obchodného registra, plnomocenstvo atď.;
* Dohodne si termín návštevy.  

#### 4.1.2.2 Generovanie žiadosti  
Pri žiadosti o TLS certifikát si Odberateľ vygeneruje pár kryptografických kľúčov (súkromný a verejný) pomocou svojho softvéru (typicky napríklad Microsoft IIS alebo Apache / OpenSSL) a vytvorí novú žiadosť o TLS certifikát, ktorú uloží na vhodné médium. 
Poskytovateľ vydáva TLS certifikáty výlučne v sídle spoločnosti v Bratislave. 

Poznámky a varovania: Upozorňujeme, že žiadosť o TLS certifikát alebo verejný kľúč v nej, pre ktorý už bol TLS certifikát vydaný, nemôže byť z bezpečnostných dôvodov použitá opakovane na vydanie ďalšieho TLS certifikátu a bude na RA odmietnutá! Žiadosť o TLS certifikát musí obsahovať vhodne vyplnenú položku <subject:commonName> (tzv. meno entity). Jednotlivé položky sa vypĺňajú tak, aby zadané hodnoty boli v súlade s týmto dokumentom, s dôrazom na jeho časť 3.1.2, a aby jasne identifikovali entitu, ktorá bude daný TLS certifikát používať (typicky plne kvalifikované doménové meno (FQDN)). Ak je v žiadosti vyplnená položka O (<subject:organizationName>), musí byť vyplnená aj položka L (<subject:localityName>). Je tiež potrebné dodržať poradie položiek v žiadosti, ako je uvedené v časti 3.1.4.1 tabuľka 3.  

#### 4.1.2.3 Odoslanie žiadosti o TLS certifikát  
Žiadosť o vydanie TLS certifikátu zasiela žiadateľ/Odberateľ na adresu RA ([radisig@disig.sk](mailto:radisig@disig.sk)), ktorá vykoná všetky úkony súvisiace s procesom vydávania TLS certifikátu.

## 4.2 Spracovanie žiadosti o certifikát  

### 4.2.1 Vykonávanie identifikačných a autentifikačných funkcií  
Pred vydaním TLS certifikátu zamestnanec zastupujúci Poskytovateľa:  
* Informuje prítomnú fyzickú osobu o Všeobecných podmienkach [12];  
* Skontroluje úplnosť a správnosť údajov v prijatej žiadosti o TLS certifikát.     
* Overí identitu Odberateľa a vloží jeho osobné údaje do IS Poskytovateľa, pričom ho zaviaže vyplniť všetky požadované položky vyžadované systémom Poskytovateľa.     
* Overí ďalšie dokumenty na overenie akýchkoľvek identifikačných informácií, ktoré majú byť vložené do TLS certifikátu.  

Pracovník RA overí identitu a autenticitu Odberateľa v zmysle časti 3.2.     
Odberatelia uspokojivým spôsobom preukážu RA všetky údaje, ktoré zadali do každej položky žiadosti o TLS certifikát.   
Pracovník RA vloží žiadosť o TLS certifikát a ďalšie požadované údaje do informačného systému Poskytovateľa.  

### 4.2.2 Schválenie alebo zamietnutie žiadostí o TLS certifikát  
V prípade akejkoľvek opodstatnenej pochybnosti o identite Odberateľa, tiež v prípade nedostatkov v dokumentoch, poskytnutia neúplných dokumentov, pracovník RA odmietne registráciu Odberateľa.
Žiadosť sa zamietne aj vtedy, ak jej formát alebo obsah nespĺňa požiadavky uvedené v časti 3.1.4.  

Poskytovateľ nesmie vydávať certifikáty pre FQDN, ktoré obsahuje najvyššiu doménu (gTLD), ktorá nie je uvedená v databáze „Root Zone Database“ spravovanej úradom IANA (Internet Assigned Numbers Authority) ([https://www.iana.org/domains/root/db](https://www.iana.org/domains/root/db)).
Akákoľvek žiadosť spĺňajúca požiadavky týchto CP/CPS bude spracovaná bezodkladne, ak sa vydanie uskutoční v prítomnosti Odberateľa alebo najneskôr v čase dohodnnutom s Odberateľom v procese žiadosti o TLS certifikát.  

Poskytovateľ nebude vydávať TLS certifikáty obsahujúce interné mená alebo rezervované IP adresy.  
Poskytovateľ nesmie vydať TLS certifikát na žiadosť obsahujúcu doménové meno, ak sa pri overovaní DNS záznamu CAA podľa časti 3.2.2.8 zistí, že takýto záznam existuje a neoprávňuje Poskytovateľa ako oprávneného na vydávanie TLS certifikátov.
Ak však záznam „issue“ a/alebo „issuewild“ obsahuje autorizáciu vo forme „disig.sk“, Poskytovateľ je oprávnený vydať príslušný TLS certifikát na základe predloženej žiadosti.  

Výsledky kontroly záznamu CAA Poskytovateľ zaznamená a uloží.

### 4.2.3 Čas na spracovanie vydania TLS certifikátu  
Žiadne ustanovenia. 

## 4.3 Vydanie certifikátu  

### 4.3.1 Kroky CA počas vydávania TLS certifikátu  
Po odoslaní žiadosti o TLS certifikát z RA na CA systém CA overí prijatú žiadosť s cieľom overiť, či:  
* Bola odoslaná autorizovaným pracovníkom RA;  
* Zodpovedá štandardu pre PKCS #10 resp. SPKAC;  
* K verejnému kľúču nachádzajúcemu sa v predloženej žiadosti o TLS certifikát nebol v minulosti vydaný žiadny TLS certifikát.  

Ak sú splnené všetky požiadavky na TLS certifikát, CA vydá TLS certifikát.  

Pred vydaním TLS certifikátu, ktorý bude poskytnutý koncovému používateľovi, systém CA zabezpečí, aby bol zodpovedajúci predbežný TLS certifikát odoslaný na predvolené CT log servery s cieľom získať záznam CT logu, ktorý bude následne zahrnutý do TLS certifikátu. Zároveň systém vykoná automatizovanú kontrolu vydaného predbežného TLS certifikátu a TLS certifikátu pomocou aplikácie „zlint“ a "ctlint", či ich parametre zodpovedajú požiadavkám špecifikovaným v [3], [4], [5], [6] a [7].  

Vydanie certifikátu koreňovou CA (Root CA) vyžaduje, aby jednotlivec autorizovaný Poskytovateľom (t. j. operátor systému CA, systémový administrátor alebo PKI manažér) vedome vydal priamy príkaz, aby koreňová CA vykonala operáciu podpisu TLS certifikátu.  

### 4.3.2 Informovanie odberateľa zo strany CA o vydaní TLS certifikátu  
Vydávajúci pracovník RA informuje Odberateľa/Držiteľa o vydaní TLS certifikátu zaslaním e-mailovej správy na e-mailovú adresu uvedenú v osobných údajoch Držiteľa certifikátu.

## 4.4 Prevzatie certifikátu  

### 4.4.1 Konanie predstavujúce prevzatie TLS certifikátu  
TLS certifikáty budú vytvárané a vydávané v systéme Poskytovateľa automatizovane a priebežne. Držiteľ si bude môcť prevziať vydaný TLS certifikát ihneď po jeho vydaní.  
Po vydaní TLS certifikátu pracovník RA a Odberateľ podpíšu príslušnú dokumentáciu súvisiacu s vydaním TLS certifikátu.  

TLS certifikát je k dispozícii na stiahnutie prostredníctvom úložiska Poskytovateľa na adrese:
[https://eidas.disig.sk/sk/poskytovatel/certifikacna-autorita/vyhladavanie-certifikatov/](https://eidas.disig.sk/sk/poskytovatel/certifikacna-autorita/vyhladavanie-certifikatov/)
alebo je mu poskytnutý e-mailom alebo odovzdaním na prenosnom médiu.  

### 4.4.2 Zverejnenie TLS certifikátu autoritou CA  
Každý vydaný TLS certifikát je zverejnený v úložisku Poskytovateľa ihneď po vydaní, pokiaľ nebolo s Odberateľom/Držiteľom dohodnuté jeho nezverejnenie.

### 4.4.3 Informovanie iných subjektov zo strany CA o vydaní TLS certifikátu  
Predbežný TLS certifikát je automaticky odosielaný na predvolené CT log servery s cieľom získať záznam CT logu, ktorý bude následne zahrnutý do výsledného TLS certifikátu. 

## 4.5 Používanie páru kľúčov a TLS certifikátu  
Táto časť popisuje zodpovednosti za používanie kľúčov a TLS certifikátov.

### 4.5.1 Používanie súkromného kľúča a TLS certifikátu odberateľom  
Odberateľ vo vzťahu k súkromnému kľúču a TLS certifikátu:
* Poskytne Poskytovateľovi presné a úplné informácie vyžadované týmito CP/CPS pri žiadosti o TLS certifikát;  
* Používa pár kľúčov v súlade s obmedzeniami, ktoré mu oznámil Poskytovateľ;  
* Neustále chráni svoje súkromné kľúče v súlade s týmito CP/CPS a v súlade s ustanoveniami Všeobecných podmienok [12];  
* Používa súkromný kľúč až po získaní TLS certifikátu k verejnému kľúču, s ktorým tvoria jedinečné páry;  
* Okamžite informuje Poskytovateľa, ak TLS certifikát ešte neexpiroval, pri podozrení, že jeho súkromný kľúč bol stratený, odcudzený alebo kompromitovaný;  
* Okamžite požiada o zrušenie TLS certifikátu v prípade, že sa akákoľvek informácia v TLS certifikáte entity stane neplatnou;  
* Dodržiava všetky termíny, podmienky a obmedzenia kladené na jeho súkromný kľúč a TLS certifikát, t. j. prestane používať súkromný kľúč po exspirácii alebo zrušení TLS certifikátu k verejnému kľúču.  

Odberateľ, ktorý si nesplní svoje povinnosti, nemá nárok na náhradu žiadnej škody. 

### 4.5.2 Používanie verejného kľúča a TLS certifikátu spoliehajúcou sa stranou  
Spoliehajúca sa strana, ktorá sa spolieha na TLS certifikát vydaný podľa týchto CP/CPS a v súlade so Všeobecnými obchodnými podmienkami [12]:  
* Posúdi, či je použitie TLS certifikátu v súlade s jeho účelom a či je vhodné na konkrétny účel;  
* Skontroluje, či je použitie TLS certifikátu v súlade s obmedzeniami TLS certifikátu, ktoré sú obsiahnuté v samotnom TLS certifikáte, vo Všeobecných podmienkach [12] alebo v týchto CP/CPS;  
* Pri práci s TLS certifikátom, vrátane overovania, používa iba určený a vhodný hardvér alebo softvér;  
* Overí platnosť predmetného TLS certifikátu kontrolou, či:  
* TLS certifikát bol platný v čase, keď mala spoliehajúca sa strana dôveru, že podpis / pečať bola vytvorená.  
* Pred časom uvedeným v predchádzajúcom bode nebol TLS certifikát zrušený kontrolou aktuálneho CRL a prípadne prostredníctvom OCSP poskytovaného Poskytovateľom - odkaz na adresu CRL a voliteľne na službu OCSP je uvedený v TLS certifikáte.  
* Vykoná akékoľvek ďalšie overenia, ktoré môžu byť vyžadované v kontexte týchto CP/CPS alebo štandardov pre konkrétny typ TLS certifikátu alebo jeho použitie a overí ostatné TLS certifikáty v certifikačnej ceste, ako je opísané predchádzajúcim spôsobom, napr. „kotva dôvery“.

## 4.6 Obnova certifikátu (Renewal)  
Žiadne ustanovenia.  

### 4.6.1 Okolnosti pre obnovu TLS certifikátu  
Poskytovateľ nepovolí obnovu (vydanie) TLS certifikátu k verejnému kľúču, ku ktorému už bol vydaný TLS certifikát tou istou CA Poskytovateľa.  

### 4.6.2 Kto môže žiadať o obnovu  
Žiadne ustanovenia.

### 4.6.3 Spracovanie žiadostí o obnovu TLS certifikátu  
Žiadne ustanovenia.

### 4.6.4 Informovanie odberateľa o vydaní nového TLS certifikátu  
Žiadne ustanovenia.

### 4.6.5 Konanie predstavujúce prevzatie obnoveného TLS certifikátu  
Žiadne ustanovenia.

### 4.6.6 Zverejnenie obnoveného TLS certifikátu autoritou CA  
Žiadne ustanovenia.

### 4.6.7 Informovanie iných subjektov zo strany CA o vydaní TLS certifikátu  
Žiadne ustanovenia.

## 4.7 Výmena kľúčov certifikátu (Re-key)  
Žiadne ustanovenia.

### 4.7.1 Okolnosti pre výmenu kľúčov TLS certifikátu  
Žiadne ustanovenia.

### 4.7.2 Kto môže žiadať o certifikáciu nového verejného kľúča  
Žiadne ustanovenia.

### 4.7.3 Spracovanie žiadostí o výmenu kľúčov TLS certifikátu  
Žiadne ustanovenia. 

### 4.7.4 Informovanie odberateľa o vydaní nového TLS certifikátu  
Žiadne ustanovenia.

### 4.7.5 Konanie predstavujúce prevzatie TLS certifikátu s vymenenými kľúčmi  
Žiadne ustanovenia.

### 4.7.6 Zverejnenie TLS certifikátu s vymenenými kľúčmi autoritou CA  
Pozri časť 4.4.2.

### 4.7.7 Informovanie iných subjektov zo strany CA o vydaní TLS certifikátu  
Žiadne ustanovenia.

## 4.8 Modifikácia certifikátu  

### 4.8.1 Okolnosti pre modifikáciu TLS certifikátu  
Žiadne ustanovenia.

### 4.8.2 Kto môže žiadať o modifikáciu TLS certifikátu  
Žiadne ustanovenia.

### 4.8.3 Spracovanie žiadostí o modifikáciu TLS certifikátu  
Žiadne ustanovenia.

### 4.8.4 Informovanie odberateľa o vydaní nového TLS certifikátu  
Žiadne ustanovenia.

### 4.8.5 Konanie predstavujúce prevzatie modifikovaného TLS certifikátu  
Žiadne ustanovenia.

### 4.8.6 Zverejnenie modifikovaného TLS certifikátu autoritou CA  
Žiadne ustanovenia.

### 4.8.7 Informovanie iných subjektov zo strany CA o vydaní TLS certifikátu  
Žiadne ustanovenia.

## 4.9 Zneplatnenie a pozastavenie certifikátu  

### 4.9.1 Okolnosti pre zrušenie  
TLS certifikát bude zrušený, keď sa vzťah medzi entitou a jej verejným kľúčom definovaný v TLS certifikáte už nepovažuje za platný.

#### 4.9.1.1 Dôvody na zrušenie certifikátu Odberateľa/Subjektu  
Poskytovateľ zruší TLS certifikát do 24 hodín, ak nastane jedna alebo viac z nasledujúcich skutočností:  
* Odberateľ/Subjekt písomne požiada Poskytovateľa o zrušenie TLS certifikátu.  
* Odberateľ/Subjekt oznámi Poskytovateľovi, že pôvodná žiadosť o TLS certifikát nebola autorizovaná a spätne neudeľuje autorizáciu.  
* Poskytovateľ získa dôkaz, že súkromný kľúč Odberateľa/Subjektu prislúchajúci k verejnému kľúču v TLS certifikáte bol kompromitovaný (Key Compromise); alebo  
* Poskytovateľ získa dôkaz, že na overenie autorizácie alebo kontroly domény pre akékoľvek plne kvalifikované doménové meno (FQDN) v TLS certifikáte sa už nemožno spoliehať.  

Poskytovateľ by mal zrušiť TLS certifikát do 24 hodín a musí zrušiť TLS certifikát do 5 dní, ak nastane jedna alebo viac z nasledujúcich skutočností:  
* TLS certifikát už nespĺňa požiadavky častí 6.1.5 a 6.1.6.  
* Poskytovateľ získa dôkaz, že TLS certifikát bol zneužitý.  
* Poskytovateľ sa dozvie, že Odberateľ porušil jednu alebo viacero svojich podstatných povinností vyplývajúcich zo Zmluvy s Odberateľom alebo Podmienok používania.  
* Existuje podozrenie, že TLS certifikát nebor vydaný v súlade s týmito CP/CPS;  
* Poskytovateľ sa dozvie o akejkoľvek okolnosti naznačujúcej, že používanie plne kvalifikovaného doménového mena (FQDN) v TLS certifikáte už nie je legálne povolené (napr. súd alebo rozhodca zrušil právo registrátora doménového mena používať doménové meno, príslušná licenčná zmluva alebo zmluva o službách medzi registrátorom doménového mena a žiadateľom bola ukončená, alebo registrátor doménového mena neobnovil doménové meno);  
* Poskytovateľ sa dozvie, že wildcard TLS certifikát bol použitý na autentifikáciu podvodne zavádzajúceho podriadeného plne kvalifikovaného doménového mena (FQDN).  
* Právo Poskytovateľa vydávať TLS certifikáty podľa TLS BR [3] vyprší alebo je zrušené alebo ukončené, pokiaľ Poskytovateľ neprijal opatrenia na ďalšie udržiavanie úložiska CRL/OCSP.  
* Poskytovateľ sa dozvie o demonštrovanej alebo preukázanej metóde, ktorá vystavuje súkromný kľúč Odberateľa/Subjektu kompromitácii, boli vyvinuté metódy, ktoré ho dokážu ľahko vypočítať na základe verejného kľúča (napríklad slabý kľúč Debian, pozri [http//wiki.debian.org/SSLkeys](http//wiki.debian.org/SSLkeys)), alebo ak existuje jasný dôkaz, že špecifická metóda použitá na generovanie súkromného kľúča bola chybná.  
* Poskytovateľ sa dozvie o podstatnej zmene informácií obsiahnutých v TLS certifikáte.  
* CA určí alebo sa dozvie, že akákoľvek informácia uvedená v TLS certifikáte je nepresná.  
* Poskytovateľ ukončí činnosť z akéhokoľvek dôvodu a nezabezpečí, aby iná CA poskytovala informácie o zzrušených TLS certifikátoch v jeho mene.  
* Technické parametre alebo formát TLS certifikátu by mohli viesť k neprijateľnému riziku z pohľadu predajcov softvéru alebo spoliehajúcich sa strán (zmena kryptografických algoritmov na podpisovanie, dĺžka kryptografických kľúčov atď.).  
* Odberateľ/Subjekt zomrel v prípade fyzickej osoby alebo zanikol v prípade právnickej osoby a Poskytovateľ bude o tejto skutočnosti informovaný,  
* Zneplatnenie je vyžadované týmito CP/CPS.  

Vždy, keď sa Poskytovateľ dozvie o niektorej z vyššie uvedených okolností, TLS certifikát bude zrušený a zaradený do zoznamu zzrušených certifikátov („CRL“).  
Zneplatnený TLS certifikát bude prítomný vo všetkých nových CRL aspoň dovtedy, kým nevyprší platnosť TLS certifikátu.  
Zneplatnený TLS certifikát nemôže byť za žiadnych okolností obnovený.  

Keď je TLS certifikát koncovej entity zrušený z jedného z nižšie uvedených dôvodov, v rozšírení reasonCode položky CRL zodpovedajúcej TLS certifikátu koncovej entity sa uvedie špecifikovaný dôvod CRLReason. Ak kód CRLReason nie je jedným z nasledujúcich, rozšírenie reasonCode sa neposkytne:  
* keyCompromise (RFC 5280 CRLReason #1).  
* privilegeWithdrawn (RFC 5280 CRLReason #9);
* cessationOfOperation (RFC 5280 CRLReason #5).  
* affiliationChanged (RFC 5280 CRLReason #3); alebo  
* superseded (RFC 5280 CRLReason #4),

tak tento špecifický dôvod zrušenia (CRLReason) musí byť uvedený v položke reasonCode zoznamu zrušených certifikátov (CRL), ktorý je zverejňovaný po zrušení certifikátu. V prípade, že je certifikát zrušený z iných dôvodov ako sú vyššie uvedené, tak sa položka reasonCode v CRL nebude vyskytovať.

#### 4.9.1.2 Dôvody na zrušenie certifikátu podriadenej CA  
Poskytovateľ zruší certifikát podriadenej CA do siedmich (7) dní, ak nastane jedna alebo viac z nasledujúcich skutočností:  
* prijme písomnú žiadosť o zrušenie podriadenej CA,  
* podriadená CA oznámi vydávajúcemu Poskytovateľovi CA, že pôvodná žiadosť nebola autorizovaná a neposkytne dodatočnú autorizáciu,  
* Poskytovateľ získa dôkaz, že súkromný kľúč prislúchajúci k verejnému kľúču v TLS certifikáte podriadenej CA bol kompromitovaný alebo už nespĺňa požiadavky v súlade s časťami 6.1.5 a 6.1.6,  
* Poskytovateľ získa dôkaz, že certifikát podriadenej CA bol zneužitý,  
* Poskytovateľ si je vedomý, že certifikát podriadenej CA nebor vydaný v súlade s týmito CP/CPS,  
* Poskytovateľ určí, že akákoľvek informácia poskytnutá v certifikáte podriadenej CA je nepresná alebo zavádzajúca,  
* CA ukončí prevádzku a neexistuje možnosť, že iná CA poskytne údaje o zrušených TLS certifikátoch,  
* zrušenie je vyžadované týmito CP/CPS,  
* ak právo vyprší alebo je zrušené alebo právo vydávať TLS certifikáty podľa TLS BR [3] bolo ukončené a Poskytovateľ neprijal opatrenia na ďalšie poskytovanie informácií z úložiska CRL/OCSP.  

### 4.9.2 Kto môže žiadať o zrušenie  
Odberateľ (alebo ním poverená fyzická alebo právnická osoba) môže požiadať o zrušenie TLS certifikátu kedykoľvek, aj bez uvedenia dôvodu zrušenia TLS certifikátu, s výnimkou dôvodov, ktoré musia byť zverejnené v CRL, pričom Odberateľ/Držiteľ ich vo svojej žiadosti uvedie.  
RA zruší TLS certifikát Odberateľa, ak sa dozvie o ktorejkoľvek z okolností uvedených v časti 4.9.1.
Zneplatnenie certifikátu môže vyžiadať aj:
* Poskytovateľ – pracovník RA túto skutočnosť písomne zdokumentuje vrátane dôvodu svojho konania,
* súd prostredníctvom svojho rozsudku alebo predbežného opatrenia (k dokumentom o zrušení TLS certifikátu sa priloží kópia príslušného súdneho rozhodnutia).  

Okrem toho môžu Odberatelia, spoliehajúce sa strany, dodávatelia aplikačného softvéru a iné tretie strany podávať správy o problémoch s certifikátmi (Certificate Problem Reports), ktoré informujú Poskytovateľa o primeranom dôvode na zrušenie TLS certifikátu.  

### 4.9.3 Postup pri žiadosti o zrušenie  
Ak sú splnené požiadavky na autentifikáciu Odberateľa, ktorý žiada o zrušenie TLS certifikátu (pozri časť 3.2.3 alebo 3.2.3); žiadosť o zrušenie TLS certifikátu môže byť podaná:  
* Osobne v pobočke RA prostredníctvom formulára „Žiadosť o zrušenie certifikátu“ dostupného v RA. Pracovník RA môže požiadať o heslo na zrušenie TLS certifikátu, ak osobou žiadajúcou o zrušenie TLS certifikátu nie je Odberateľ, ale osoba ním na to splnomocnená.  
* E-mailom – zaslaním e-mailovej správy (nemusí byť podpísaná). Obsahom správy musí byť jasné želanie zrušiť TLS certifikát vyjadrené frázou „Týmto žiadam o zrušenie môjho TLS certifikátu so sériovým číslom XXXXXX“. Táto správa musí obsahovať aj heslo na zrušenie TLS certifikátu uvedené v potvrdení o vydaní TLS certifikátu.  
* Poštou zaslanou na adresu Poskytovateľa alebo príslušnej RA spolu s heslom uvedeným v potvrdení o vydaní TLS certifikátu.  
* V prípade žiadosti o zrušenie TLS certifikátu z dôvodov uvedených v časti 4.9.1.1, držiteľ TLS certifikátu predloží/doručí „Žiadosť o zrušenie TLS certifikátu“, ktorá je dostupná na webovom sídle Poskytovateľa: [https://dsrv.disig.sk/download/forms/tls_revoke_form.pdf](https://dsrv.disig.sk/download/forms/tls_revoke_form.pdf).  

TLS certifikát, ktorého platnosť vypršala, nemôže byť zrušený.  

Postupy nahlasovania incidentov pri možnej kompromitácii súkromného kľúča, zneužití TLS certifikátu alebo inom type podvodu, neoprávnenom vydaní alebo inej záležitosti súvisiacej s vydaným TLS certifikátom sú uvedené v 1.5.2.
Osoba žiadajúca o zrušenie TLS certifikátu musí buď absolvovať rovnaký proces autentifikácie v RA, aký sa vyžaduje pri počiatočnej registrácii žiadateľa o TLS certifikát, alebo musí hodnoverným spôsobom preukázať, že je oprávnenou osobou, ktorá môže žiadať o zrušenie daného TLS certifikátu.  

Ak je Odberateľ/Držiteľ TLS certifikátu zastúpený v RA vo veci zrušenia TLS certifikátu, zastupujúci subjekt sa musí preukázať overeným plnomocenstvom (notárom alebo matrikou), z textu ktorého je jasne zrejmá vôľa Odberateľa/Držiteľa TLS certifikátu zrušiť svoj TLS certifikát. Zastupujúci subjekt je povinný ponechať v RA doklad potvrdzujúci jeho plnomocenstvo alebo jeho kópiu (nemusí byť overená). Pracovník RA tento doklad prevezme a uschová, v prípade neoverenej kópie ju porovná s originálom a napíše na ňu text „Potvrdzujem zhodu s originálom“ a pridá dátum a svoj podpis.  

Pracovník RA posúdi oprávnenosť žiadosti o zrušenie TLS certifikátu a ak je zrejmé, že žiadateľ o zrušenie nie je oprávnenou osobou, môže RA žiadosť o zrušenie zamietnuť.  

Pracovník RA zamietne žiadosť, ak žiadateľ nesplní podmienky na autentifikáciu svojej identity (pozri časti 3.2.2 alebo 3.2.2.3).  

Kontakty na nahlasovanie a postup pri nahlasovaní incidentov v prípade možnej kompromitácie súkromného kľúča, zneužitia TLS certifikátu alebo inom type podvodu, neoprávneného vydania alebo inej záležitosti súvisiacej s vydaným TLS certifikátom sú uvedené v kapitole 1.5.2.  
V prípade žiadosti o zrušenie TLS certifikátu z ktoréhokoľvek z dôvodov uvedených v časti 4.9.1.1 keyCompromise (RFC 5280 CRLReason #1), privilegeWithdrawn (RFC 5280 CRLReason #9), cessationOfOperation (RFC 5280 CRLReason #5), affiliationChanged (RFC 5280 CRLReason #3), alebo superseded (RFC 5280 CRLReason #4), musí RA vyžadovať zaslanie písomnej žiadosti, ako je špecifikované vyššie v tejto časti.  

### 4.9.4 Lehota na podanie žiadosti o zrušenie  
Žiadne ustanovenia.

### 4.9.5 Čas, v ktorom CA spracuje žiadosť o zrušenie  
Poskytovateľ:  
* Do 24 hodín po prijatí správy o probléme s certifikátom (Certificate Problem Report) Poskytovateľ prešetrí skutočnosti a okolnosti súvisiace so správou a poskytne predbežnú správu o svojich zisteniach Odberateľovi aj subjektu, ktorý správu podal;  
* Po preskúmaní skutočností a okolností Poskytovateľ spolupracuje s Odberateľom/Držiteľom a akýmkoľvek subjektom nahlasujúcim správu alebo iné oznámenie súvisiace so zrušením s cieľom určiť, či bude TLS certifikát zrušený alebo nie, a ak áno, dátum, ku ktorému Poskytovateľ TLS certifikát zruší;  
* Obdobie od prijatia správy alebo oznámenia do zverejneného zrušenia nepresiahne časový rámec stanovený v časti 4.9.1.1;  
* Dátum vybraný Poskytovateľom by mal zohľadňovať nasledujúce kritériá:  
    * Povahu údajného problému (rozsah, kontext, závažnosť, veľkosť, riziko škody);  
    * Dôsledky zrušenia (priame a vedľajšie dopady na Odberateľov a Spoliehajúce sa strany);  
    * Počet prijatých správ o problémoch týkajúcich sa konkrétneho certifikátu alebo Odberateľa;  
    * Subjekt podávajúci sťažnosť (napríklad sťažnosť od predstaviteľa orgánu činného v trestnom konaní, že webová stránka sa zapája do nezákonných činností, by mala mať väčšiu váhu ako sťažnosť od spotrebiteľa tvrdiaceho, že nedostal objednaný tovar); a  
    * Príslušnú legislatívu.  
* Zverejní aktuálne CRL a všetky predchádzajúce CRL na svojom webovom sídle (pozri časť 1);  
* Zverejní všetky zrušené TLS certifikáty v CRL, t. j. aj tie, ktorých platnosť medzitým vypršala;  
* Archivuje všetky CRL, ktoré vydal.  

Poskytovateľ automaticky informuje Odberateľa/Držiteľa TLS certifikátu o zrušení TLS certifikátu zaslaním e-mailu na e-mailovú adresu poskytnutú Odberateľom/Držiteľom pri registrácii v RA.  

Po prijatí žiadosti o zrušenie TLS certifikátu, ktorú pracovník RA považuje za oprávnenú (t. j. ktorá je v súlade s príslušnými ustanoveniami týchto CP/CPS), pracovník RA vloží prijatú žiadosť o zrušenie cez aplikáciu RA Client do informačného systému Poskytovateľa, aby mohol byť predmetný TLS certifikát automaticky zrušený. Zneplatnenie sa vykoná najneskôr do 24 hodín po overení oprávnenosti žiadosti.  

CRL bude zverejnené v úložisku čo najrýchlejšie po vydaní.

Vzhľadom na skutočnosť, že Mozilla neudeľuje výnimky z požiadaviek na zrušenie TLS certifikátov podľa týchto CP/CPS, Poskytovateľ:  
* zapojí sa do proaktívnej komunikácie a v dostatočnom predstihu poradí Odberateľom o časových harmonogramoch zrušenia a výslovne ich varuje pred používaním verejne dôveryhodných TLS certifikátov v systémoch, ktoré nemôžu tolerovať včasné zrušenie;  
* zahrnie do zmlúv s Odberateľmi vhodný jazyk vyžadujúci včasnú spoluprácu Odberateľa pri dodržiavaní časových harmonogramov zrušenia a potvrdzujúci povinnosti Poskytovateľa dodržiavať platné politiky a štandardy; a  
* pripraví a udržiava komplexné a realizovateľné plány na riešenie udalostí hromadného zrušenia, vrátane podrobných postupov na efektívne zvládnutie hromadných zrušení, vrátane rýchlej komunikácie s dotknutými stranami a vykonávania každoročného testovania plánu prostredníctvom cvičení, simulácií, paralelného testovania alebo použitia testovacích prostredí, ktoré nezahŕňajú zrušenie aktívnych TLS certifikátov - pozri 5.7.1.2.

### 4.9.6 Požiadavka na kontrolu zrušenia pre spoliehajúce sa strany  
Pri spoliehaní sa na TLS certifikát je spoliehajúca sa strana povinná overiť jeho platnosť podľa Všeobecných podmienok [12].  

Medzi podaním platnej žiadosti o zrušenie TLS certifikátu a zverejnením zrušeného TLS certifikátu v CRL nesie Odberateľ/Držiteľ všetku zodpovednosť za akúkoľvek škodu spôsobenú zneužitím TLS certifikátu. Po zverejnení TLS certifikátu v CRL nesie všetku zodpovednosť za akúkoľvek škodu spôsobenú použitím zrušeného TLS certifikátu strana, ktorá sa na zrušený TLS certifikát spoliehala.  

Neoverenie TLS certifikátu pomocou CRL sa považuje za hrubé porušenie týchto CP/CPS.  

### 4.9.7 Periodicita vydávania CRL  
Frekvencia CRL sa líši v závislosti od toho, či sa týka koreňovej CA alebo podriadenej CA.  


|Vydavateľ CRL|Frekvencia vydávania |nextUpdate vs.<br> thisUpdate | Poznámky |
|----------|:-----------------:|:-----------------------------:|-------|
|Root CA|max 365 dní|< 365 dní|Kedykoľvek do 24 hodín po zrušení podriadenej CA|
|Subordinate CA|max 7 dní|< 10 dní||

Podriadené CA Poskytovateľa vydávajúce TLS certifikáty koncovým používateľom vydávajú CRL:
* Aspoň každých 24 hodín, aj keď za posledných 24 hodín nebor zrušený žiadny TLS certifikát, pričom nextUpdate bude mať hodnotu 24 hodín.  

Koreňová CA vydávajúca certifikáty podriadeným CA vydáva CRL:
* Aspoň každých 7 dní s nextUpdate na 14 dní.  
* Vždy do 24 hodín od zrušenia podriadeného certifikátu CA.  

### 4.9.8 Maximálne oneskorenie CRL  
Žiadne ustanovenia.  

### 4.9.9 Dostupnosť on-line overovania stavu (OCSP)  

Poskytovateľ môže poskytovať službu OCSP pre vydaný TLS certifikát. V prípade služby OCSP budú adresy jednotiek OCSP responderov zahrnuté v rozšírení Authority Information Access TLS certifikátu.  
Odpovede OCSP musia byť v súlade s RFC 6960 [19] a/alebo RFC 5019 [20]. Odpovede OCSP musia byť podpísané buď:  
   **[1]** CA, ktorá vydala TLS certifikáty, ktorých stav zrušenia sa kontroluje; alebo  
   **[2]** OCSP responderom, ktorého TLS certifikát je podpísaný CA, ktorá vydala TLS certifikát, ktorého stav zrušenia sa kontroluje.  

V druhom prípade musí podpisový TLS certifikát OCSP obsahovať rozšírenie typu id-pkix-ocsp-nocheck, ako je definované v RFC 6960 [19].  
Tretie strany so záujmom o používanie OCSP zašlú požiadavku príslušnej jednotke OCSP respondera, ktorej URI je zverejnené v TLS certifikáte. Predložená požiadavka musí byť v súlade s požiadavkami RFC 6960 [19].  
OCSP respondery prevádzkované Poskytovateľom podporujú metódu HTTP GET, ako je popísané v RFC 6960 [19] a/alebo RFC 5019 [20]. Poskytovateľ môže spracovať rozšírenie Nonce (1.3.6.1.5.5.7.48.1.2) v súlade s RFC 8954 [21].  
Interval platnosti odpovede OCSP je časový rozdiel medzi poľami thisUpdate a nextUpdate vrátane. Na účely výpočtu rozdielov sa rozdiel 3 600 sekúnd rovná jednej hodine a rozdiel 86 400 sekúnd sa rovná jednému dňu, pričom sa ignorujú priestupné sekundy.  

Pre stav TLS certifikátov Odberateľa:  
   **[1]** Odpovede OCSP musia mať interval platnosti väčší alebo rovný ôsmim hodinám;  
   **[2]** Odpovede OCSP musia mať interval platnosti menší alebo rovný desiatim dňom;  
   **[3]** Pre odpovede OCSP s intervalmi platnosti kratšími ako šestnásť hodín Poskytovateľ aktualizuje informácie poskytované prostredníctvom OCSP pred uplynutím polovice doby platnosti pred nextUpdate;  
   **[4]** Pre odpovede OCSP s intervalmi platnosti väčšími alebo rovnými šestnástim hodinám Poskytovateľ aktualizuje informácie poskytované prostredníctvom OCSP aspoň osem hodín pred nextUpdate a najneskôr štyri dni po thisUpdate;  
   **[5]** Autoritatívna odpoveď OCSP musí byť dostupná (t. j. responder nesmie odpovedať stavom „unknown“) najneskôr 15 minút po prvom zverejnení alebo inom sprístupnení certifikátu alebo TLS precertifikátu.  

Pre stav certifikátov podriadenej CA:
* Poskytovateľ aktualizuje informácie poskytované prostredníctvom OCSP:     
   * aspoň každých dvanásť mesiacov; a  
   * do 24 hodín po zrušení certifikátu podriadenej CA.  

### 4.9.10 Požiadavky na on-line overovanie stavu  
Žiadne ustanovenia.  

### 4.9.11 Iné formy oznamovania zrušenia  
Žiadne ustanovenia.  

### 4.9.12 Špeciálne požiadavky pri kompromitácii kľúča  
Pozri časť 4.9.1.  

### 4.9.13 Okolnosti pre pozastavenie (Suspension)  
Poskytovateľ takúto službu neposkytuje.  

### 4.9.14 Kto môže žiadať o pozastavenie  
Žiadne ustanovenia.  

### 4.9.15 Postup pri žiadosti o pozastavenie  
Žiadne ustanovenia.  

### 4.9.16 Obmedzenia doby pozastavenia  
Žiadne ustanovenia.  

## 4.10 Služby overovania stavu certifikátov  

### 4.10.1 Prevádzkové vlastnosti  

CRL bude dostupné na webovom sídle Poskytovateľa (pozri časť 1) a bude prístupné cez HTTP protokol na porte 80.  
Služba OCSP bude dostupná na URL špecifikovanej vo vydanom TLS certifikáte a žiadateľ o stav TLS certifikátu zašle požiadavku v zmysle 4.9.10.  

Záznamy o zrušení v CRL alebo odpovedi OCSP nebudú odstránené skôr ako po dátume exspirácie zrušeného TLS certifikátu.  
Aktuálne CRL je k dispozícii na webovom sídle Poskytovateľa (pozri časť 1) a je prístupné cez HTTP protokol na porte 80.  
Služba OCSP je dostupná na URL špecifikovanej vo vydanom TLS certifikáte.  

### 4.10.2 Dostupnosť služby  
Poskytovateľ prevádzkuje a udržiava svoje CRL a voliteľnú kapacitu OCSP so zdrojmi dostatočnými na poskytnutie času odozvy desať sekúnd alebo menej za bežných prevádzkových podmienok.
Distribučné body, na ktorých sú zverejňované CRL, sú dostupné v režime 24x7.  
OCSP je dostupné v režime 24x7.  
Poskytovateľ udržiava nepretržitú schopnosť 24x7 interne reagovať na správu o probléme s TLS certifikátom s vysokou prioritou a v prípade potreby postúpiť takúto sťažnosť orgánom činným v trestnom konaní a/alebo zrušiť certifikát, ktorý je predmetom takejto sťažnosti.
Nahlasovanie problémov s TLS certifikátmi je dostupné 24x7 na [support@disig.sk](mailto:support@disig.sk).  

### 4.10.3 Voliteľné funkcie  
Žiadne ustanovenia.  

## 4.11 Ukončenie odberu  
Služba Poskytovateľa Odberateľovi/Držiteľovi TLS certifikátu bude ukončená uplynutím platnosti zmluvy, na základe ktorej bol TLS certifikát vydaný.  
Ktorákoľvek strana na základe dohody aj pred jej uplynutím môže zmluvu ukončiť. Zrušenie zmluvy má za následok okamžité zrušenie TLS certifikátu vydaného na základe zmluvy.  

## 4.12 Úschova kľúčov (Key Escrow) a obnova  

### 4.12.1 Politika a postupy úschovy a obnovy kľúčov  
Žiadne ustanovenia.  

### 4.12.2 Politika a postupy zapuzdrenia a obnovy kľúčov relácie  
Žiadne ustanovenia.

# 5. MANAŽÉRSKE, PREVÁDZKOVÉ A FYZICKÉ KONTROLY
Bezpečnosť Poskytovateľa je založená na súbore bezpečnostných opatrení v oblasti fyzickej bezpečnosti, bezpečnosti objektov, personálnej a prevádzkovej bezpečnosti. Tieto bezpečnostné opatrenia musia byť navrhnuté, zdokumentované a aplikované na základe bezpečnostných pravidiel a schválené manažmentom Poskytovateľa.
Bezpečnostné opatrenia musia byť dostupné príslušným pracovníkom.

Poskytovateľ je povinný:
* prevziať plnú zodpovednosť za súlad svojich činností s postupmi definovanými v bezpečnostnej politike, vrátane ich plnenia svojimi registračnými autoritami;
* definovať zodpovednosť registračných autorít a zaviazať ich k dodržiavaniu stanovených bezpečnostných opatrení;
* mať zoznam všetkých svojich aktív s ich klasifikáciou z hľadiska vykonaného posúdenia rizík.

Bezpečnostná politika Poskytovateľa a Súhrn bezpečnostných aktív sa musia v pravidelných intervaloch a vždy pri vykonaní významných zmien preskúmať, aby sa zabezpečila ich kontinuita, vhodnosť, dostatočnosť a účinnosť.
Manažment Poskytovateľa schvaľuje všetky zmeny, ktoré môžu ovplyvniť úroveň poskytovanej bezpečnosti.
Nastavenie systémov Poskytovateľa sa musí pravidelne kontrolovať z hľadiska zmien, ktoré ohrozujú bezpečnostnú politiku Poskytovateľa.

## 5.1 Fyzické bezpečnostné kontroly

### 5.1.1 Umiestnenie a konštrukcia priestorov
Technologické zariadenia, v ktorých sa nachádza základná infraštruktúra Poskytovateľa, sa musia nachádzať v chránených priestoroch prístupných len oprávneným osobám a oddelených od ostatných priestorov vhodnými bezpečnostnými prvkami (bezpečnostné dvere, mreže, pevné steny a pod.). Poskytnuté vybavenie by malo pozostávať len zo zariadení vyhradených pre funkcie certifikačnej autority a nemalo by slúžiť na žiadny účel, ktorý sa netýka tejto funkcie.

### 5.1.2 Fyzický prístup
Mechanizmy kontroly prístupu do chránených priestorov Poskytovateľa, napr. do priestorov s najvyššou zónou bezpečnosti, musia byť zabezpečené tak, aby tieto priestory boli chránené bezpečnostným alarmom a boli prístupné len osobám, ktoré sú držiteľmi bezpečnostného tokenu a sú uvedené v zozname osôb oprávnených na vstup. Zariadenia Poskytovateľa musia byť trvalo chránené pred neoprávneným prístupom, a to aj pred neoprávneným fyzickým prístupom.

### 5.1.3 Napájanie a klimatizácia
Priestory, v ktorých sa nachádzajú zariadenia Poskytovateľa, musia byť primerane zásobované elektrickou energiou a klimatizované, aby poskytovali spoľahlivé prevádzkové prostredie.

### 5.1.4 Ohrozenie vodou
Priestory, v ktorých sa nachádzajú zariadenia Poskytovateľa, musia byť umiestnené tak, aby nemohli byť ohrozené vodou z akéhokoľvek zdroja. Ak to nie je úplne možné, prijmú sa opatrenia na minimalizáciu rizika ohrozenia priestorov vodou.

### 5.1.5 Prevencia a ochrana pred požiarom
Priestory, v ktorých sa nachádzajú zariadenia Poskytovateľa, musia byť spoľahlivo chránené pred priamymi zdrojmi požiaru a teplom, ktoré by mohlo spôsobiť požiar v priestoroch.

### 5.1.6 Skladovanie médií
Médiá sa skladujú v miestnostiach, ktoré sú chránené proti náhodnému, neúmyselnému poškodeniu (voda, oheň a elektromagnetizmus). Médiá obsahujúce bezpečnostné audity, archívy alebo zálohované informácie by sa mali uchovávať na mieste oddelenom od CMA.

### 5.1.7 Likvidácia odpadu
S odpadom vznikajúcim pri prevádzke Poskytovateľa sa musí nakladať tak, aby nedochádzalo k znečisťovaniu životného prostredia.

### 5.1.8 Zálohovanie mimo pracoviska (Off-site backup)
V prípade nevratného poškodenia priestorov hlavného miesta, kde sa nachádza infraštruktúra Poskytovateľa, je potrebné mať aspoň kópie najdôležitejších aktív Poskytovateľa zálohované mimo tohto hlavného miesta na geograficky vzdialenom záložnom mieste.

## 5.2 Procesné kontroly
Pri výbere osôb na obsadenie roly pracovníka RA sa kladie dôraz na ich zodpovednosť a dôveryhodnosť. Funkcie vykonávané touto rolou patria medzi funkcie, ktoré tvoria základ dôvery v Poskytovateľa na personálnej úrovni.
Každá RA, ktorá pôsobí v súlade s týmito CP/CPS, je povinná dodržiavať ich ustanovenia. Zodpovednosťou pracovníka RA je predovšetkým:
* overovanie identity buď prostredníctvom osobného kontaktu, alebo prostredníctvom zastupujúceho subjektu;
* zaznamenávanie informácií od žiadateľov o TLS certifikát a overovanie ich správnosti;
* bezpečná komunikácia s Poskytovateľom;
* komunikácia s Odberateľom/Držiteľom a dokumentovanie tejto komunikácie.

### 5.2.1 Dôveryhodné roly
V rámci CA musia byť definované dôveryhodné roly zodpovedné za jednotlivé aspekty dôveryhodných činností, ako napríklad správca systému, bezpečnostný manažér, interný audítor, tvorca politiky atď., ktoré tvoria základ dôvery v celé PKI.
Zároveň musia byť definované zodpovednosti pre jednotlivé roly. Osoby vybrané do rolí, ktoré vyžadujú dôveryhodnosť, musia byť zodpovedné a dôveryhodné. Všetky osoby v dôveryhodných rolách nesmú byť v konflikte záujmov, aby sa zabezpečila nestrannosť služieb poskytovaných Poskytovateľom.

### 5.2.2 Počet osôb vyžadovaných na úlohu
Pre každú úlohu sa určí počet osôb pridelených na jej vykonanie (pravidlo K z N).

### 5.2.3 Identifikácia a autentifikácia pre každú rolu
Každá rola má definovaný spôsob identifikácie a autentifikácie pri prístupe do IS Poskytovateľa.

### 5.2.4 Roly vyžadujúce oddelenie povinností
Každá rola musí mať stanovené kritériá, ktoré zohľadňujú potrebu oddelenia funkcií z hľadiska samotnej roly, t. j. musia existovať roly, ktoré nemôžu vykonávať tie isté osoby.

## 5.3 Personálne kontroly
Zamestnanci Poskytovateľa musia byť do dôveryhodnej roly formálne vymenovaní výkonným vedením zodpovedným za bezpečnosť. Personál pre rolu pracovníka RA sa vyberá na základe spoľahlivosti, lojality a dôveryhodnosti.

Všetky osoby zastávajúce rolu pracovníka RA sú riadne poučené a vyškolené v rozsahu potrebnom na výkon činností pracovníka RA a majú vždy k dispozícii aktuálne verzie dokumentov Poskytovateľa určených na výkon činností pracovníka RA, ktoré sú dostupné na webovom sídle.

Prístup pracovníka RA do IS Poskytovateľa cez aplikáciu RA Client je chránený pred neoprávneným prístupom použitím vlastného TLS certifikátu RA na autentifikáciu. Dôležitým bezpečnostným opatrením je, že daný pár kľúčov RA je uložený na čipovej karte (smart card), pričom prístup k súkromnému kľúču je chránený heslom.

### 5.3.1 Požiadavky na kvalifikáciu, skúsenosti a preverenie
Zamestnanci v dôveryhodných rolách musia spĺňať požiadavky na kvalifikáciu, odbornú prax a mať bezpečnostnú previerku na určenej úrovni. Osoby v riadiacich pozíciách musia:
* mať príslušné vzdelanie alebo skúsenosti v oblasti dôveryhodných služieb;
* byť oboznámené s bezpečnostnými opatreniami pre bezpečnostné roly;
* mať skúsenosti s informačnou bezpečnosťou a posudzovaním rizík.

### 5.3.2 Postupy preverovania minulosti
Zamestnanec môže byť zaradený do dôveryhodnej roly Poskytovateľa len vtedy, ak má bezpečnostnú previerku aspoň na stupeň utajenia „Vyhradené“ (Confidential) alebo je v procese žiadosti o takéto preskúmanie. Pre rolu pracovníka RA sa bezpečnostná previerka nevyžaduje.

### 5.3.3 Požiadavky na odbornú prípravu a postupy
Pre určité dôveryhodné roly môžu byť špecifikované osobitné požiadavky na školenia (softvér CMA, bezpečnostné postupy, ustanovenia CP/CPS atď.). Každý pracovník RA musí pred začatím vykonávania svojej funkcie absolvovať povinné školenie.

### 5.3.4 Periodicita a požiadavky na preškoľovanie
PMA rozhoduje o potrebe opakovania školení pre pracovníkov RA v prípadoch významných zmien v legislatíve alebo v softvéri RA.

### 5.3.5 Periodicita a poradie rotácie pracovných miest
Žiadne ustanovenia.

### 5.3.6 Sankcie za neoprávnené konanie
Akékoľvek zlyhanie zamestnanca, ktorého výsledkom je situácia, ktorá nie je v súlade s ustanoveniami týchto CP/CPS (nedbalosť alebo zlý úmysel), bude predmetom príslušného administratívneho a disciplinárneho konania.

### 5.3.7 Kontroly externých dodávateľov
Ak sú na výkon dôveryhodných rolí pridelení externí dodávatelia, vzťahujú sa na nich rovnaké povinnosti a sankcie ako na kmeňových zamestnancov.

### 5.3.8 Dokumentácia poskytovaná personálu
Zamestnanci v dôveryhodných rolách musia mať k dispozícii dokumenty potrebné na výkon funkcie, vrátane kópie týchto CP/CPS a technickej dokumentácie.

## 5.4 Postupy protokolovania auditov (Audit logging)
Poskytovateľ zaznamenáva všetky dôležité informácie týkajúce sa vydaných TLS certifikátov. Čas zaznamenaný pre každú udalosť musí byť synchronizovaný s UTC aspoň každých 24 hodín.

### 5.4.1 Typy zaznamenávaných udalostí
Zaznamenávajú sa udalosti životného cyklu kľúčov a certifikátov CA, udalosti životného cyklu certifikátov odberateľov (žiadosti, schválenia, vydania, zrušenia) a bezpečnostné udalosti (pokusy o prístup, systémové chyby, aktivity firewallu, vstupy do priestorov CA).
Záznamy musia obsahovať:
* dátum a čas udalosti;
* identitu osoby vykonávajúcej záznam;
* popis udalosti.

### 5.4.3 Doba uchovávania auditných záznamov
Poskytovateľ uchováva záznamy o životnom cykle kľúčov a certifikátov CA a bezpečnostné záznamy najmenej dva (2) roky po zničení súkromného kľúča CA alebo exspirácii certifikátu.

### 5.4.8 Posudzovanie zraniteľností
Bezpečnostný program Poskytovateľa zahŕňa ročné posúdenie rizík, ktoré identifikuje hrozby, posudzuje pravdepodobnosť škôd a dostatočnosť politík na ich potlačenie.

## 5.5 Archivácia záznamov

### 5.5.1 Typy archivovaných záznamov
Archivujú sa všetky dokumenty predložené Odberateľom (výpisy z OR, plnomocenstvá), auditné záznamy, záznamy o generovaní kľúčov CA a vydané certifikáty.

### 5.5.2 Doba uchovávania archívu
Zmluva s Odberateľom a potvrdenie o vydaní certifikátu sa uchovávajú najmenej 7 rokov od exspirácie certifikátu. Ostatná dokumentácia sa uchováva najmenej 2 roky.

## 5.7 Kompromitácia a obnova po havárii

### 5.7.1 Postupy pri incidentoch a kompromitácii
#### 5.7.1.1 Plány obnovy po havárii a riešenie incidentov
Na zabezpečenie integrity služieb musí Poskytovateľ implementovať postupy zálohovania a obnovy údajov.
Poskytovateľ musí mať vypracované núdzové postupy a plány obnovy pre výkon dôveryhodných služieb v súlade s požiadavkami časti 5.7.1 TLS BR [3].
Dôveryhodné služby by mali byť poskytované z dvoch geograficky oddelených systémov CA, z ktorých jeden je vedený ako hlavný a druhý ako záložný pre prípad zlyhania alebo katastrofy hlavného systému.
Postupy obnovy po havárii sa musia pravidelne kontrolovať a hodnotiť (aspoň raz ročne) a podľa potreby kontrolovať a aktualizovať.
Poskytovateľ nie je povinný zverejňovať svoje plány kontinuity podnikania, ale na požiadanie poskytne svoj plán kontinuity podnikania a bezpečnostný plán audítorovi.

#### 5.7.1.2 Plány pre hromadné zrušenie (Mass Revocation)
Poskytovateľ má vypracovaný plán hromadného zrušenia TLS certifikátov, ktorý zahŕňa ustanovenia uvedené v časti 5.7.1.2 TLS BR [3] a udržiava ho pre prípady hromadného zrušenia TLS certifikátov. Od 1. decembra 2025 bude vykonávať každoročné testovanie tohto plánu hromadného zrušenia TLS certifikátov  a postupne začleňovať získané poznatky do existujúceho plánu s cieľom neustále zlepšovať svoju pripravenosť na hromadné zrušenie TLS certifikátov v priebehu času.

### 5.7.2 Postupy obnovy v prípade poškodenia výpočtových zdrojov, softvéru a/alebo údajov
Žiadne ustanovenia.
### 5.7.3 Postupy obnovy po kompromitácii kľúča
Žiadne ustanovenia.
### 5.7.4 Schopnosti zabezpečiť kontinuitu podnikania po katastrofe
Žiadne ustanovenia.

## 5.8 Ukončenie činnosti CA alebo RA
Pri ukončení činnosti musí Poskytovateľ aspoň 6 mesiacov vopred informovať dozorný orgán, Odberateľov a verejnosť. Musia byť zlikvidované všetky súkromné kľúče tak, aby ich nebolo možné obnoviť.

Pri ukončení činnosti Poskytovateľa z iných dôvodov, ako sú tie, ktoré sú spôsobené vyššou mocou (napr. prírodná katastrofa, vojnový stav, štátna moc a pod.), sa postupuje v súlade s bodom 5.7.
Pred ukončením poskytovania služieb Poskytovateľ:

* Najmenej 6 mesiacov vopred oznámi dozornému orgánu, všetkým Predplatiteľom/Držiteľom platných TLS certifikátov, Spoliehajúcim sa stranám a verejnosti plánované ukončenie svojej činnosti. Toto oznámenie sa uskutoční prostredníctvom webovej stránky Poskytovateľa, elektronickou poštou, bežnou poštou, registračnými orgánmi alebo elektronickými médiami a tlačou.
* Ukončí všetky existujúce mandátne zmluvy, plné moci, na základe ktorých by iné právnické osoby mohli konať v mene Poskytovateľa.
* Uzavrie zmluvu s inou CA, ktorá by zabezpečila kontinuitu v poskytovaní dôveryhodných služieb, ak je to možné.    
* Podľa pokynov PMA musí sústrediť a pripraviť na archiváciu všetky dokumenty spojené s poskytovanými dôveryhodnými službami.  
* Vykoná kontrolu dodržania predpisov o ochrane osobných údajov t. j. Nariadenie Európskeho Parlamentu a Rady (EÚ) 2016/679 o ochrane fyzických osôb pri spracúvaní osobných údajov a o voľnom pohybe takýchto údajov a zákon č. 18/2018 Z. z. o ochrane osobných údajov (ďalej len „Predpisy o ochrane osobných údajov“) [18].  
* Vyradí z používania všetky súkromné kľúče, vrátane všetkých ich kópií, takým spôsobom, že už nemôžu byť žiadnym spôsobom obnovené.

Po ukončení svojej činnosti Poskytovateľ nevydá žiadny certifikát a zabezpečí preukázateľné znemožnenie opätovného využitia súkromných kľúčov Poskytovateľa.  
Pred ukončením svojej činnosti každá RA poskytne archivované dáta zložke Poskytovateľa podľa pokynu PMA.  
Poskytovateľ musí mať riešenie na pokrytie všetkých nákladov spojených so splnením minimálnych požiadaviek pri ukončení činnosti v prípade bankrotu alebo inej príčiny, kedy nebude schopná pokryť náklady vlastnými prostriedkami, a to v súlade s platnou legislatívou o bankrote.

# 6. Technické bezpečnostné kontroly
Technická časť infraštruktúry Poskytovateľa (hardvér a softvér) bude pozostávať iba z bezpečných systémov a oficiálneho softvéru. Architektúra infraštruktúry Poskytovateľa bude navrhnutá s komponentmi, ktoré spĺňajú bezpečnostné štandardy na úrovni súčasných poznatkov.

Zvláštna pozornosť sa bude venovať kryptografickému modulu (HSM), ktorý slúži na generovanie, ukladanie a používanie súkromných kľúčov Poskytovateľa a je jedným z najzraniteľnejších aktív. Súkromné ​​kľúče Poskytovateľa budú uložené v module HSM, ktorý je certifikovaný minimálne podľa štandardu FIPS 140-2 Level 3.

Poskytovateľ použije kombináciu fyzických, logických a procedurálnych opatrení na zaistenie bezpečnosti a ochranu svojho súkromného kľúča. Tieto opatrenia budú opísané napríklad v publikovanom CP/CPS.
Systém Poskytovateľa bude obsahovať zariadenie na nepretržitú detekciu, monitorovanie a signalizáciu neoprávnených a nezvyčajných pokusov o prístup k jeho zdrojom.
Publikačné aplikácie musia poskytovať kontrolu prístupu pred pokusom o pridanie alebo odstránenie certifikátu TLS alebo úpravu iných súvisiacich údajov.

Hlásenie stavu zrušenia musí poskytovať kontrolu prístupu pred pokusmi o zmenu informácií o stave zrušenia.
Všetky funkcie Poskytovateľa, ktoré využívajú počítačovú sieť, musia byť zabezpečené pred neoprávneným prístupom a inými škodlivými aktivitami.

## 6.1 Generovanie a inštalácia páru kľúčov

### 6.1.1 Generovanie páru kľúčov

#### 6.1.1.1 Vydavateľ certifikátu
Generovanie a inštalácia páru kľúčov poskytovateľa sa musí vykonávať štandardizovaným spôsobom podrobne opísaným v dokumentácii poskytovateľa v súlade s požiadavkami v oddiele 6.1.1.1 normy TLS BR [3].
Generovanie páru kľúčov musí poskytovať dostatočnú dôveru v proces a celý proces sa musí písomne ​​zaznamenať. Generovanie kľúčov zabezpečia oprávnení zamestnanci v dôveryhodných rolách, ktorí sú oprávnení zúčastniť sa procesu generovania kľúčov a generovania požiadaviek. Generovanie kľúčov sa musí vykonávať v zabezpečenom kryptografickom module.
Páry kľúčov CA poskytovateľa sa generujú vo formálnom „ceremoniáli kľúčov“, ktorý:

* sa uskutočňuje v zabezpečenom prostredí, ktoré spĺňa požiadavky na fyzické zabezpečenie uvedené v oddiele 5.1;
* používa hardvérové ​​bezpečnostné moduly (HSM), ktoré spĺňajú požiadavky normy [FIPS 140-2 úroveň 3 alebo vyššia / EN 419 221-5 alebo ekvivalent];
* zahŕňa potrebný počet osôb v dôveryhodných rolách konajúcich podľa princípu K/N;
* je podrobne zdokumentovaný vrátane účastníkov, zariadení, dátumu a času a výsledných odtlačkov kľúčov a certifikátov TLS;
* ceremoniál kľúčov sa vykonáva podľa písomného postupu schváleného vrcholovým manažmentom.

#### 6.1.1.2 Generovanie páru kľúčov koncového používateľa
Generovanie páru kľúčov vykonáva samotný používateľ (žiadateľ) pomocou vhodného softvéru alebo hardvéru, ktorý spĺňa minimálne požiadavky na dĺžku kľúča a požadované algoritmy.
Poskytovateľ zamietne žiadosť o TLS certifikát, ak je splnená jedna alebo viacero z nasledujúcich podmienok:

1. Pár kľúčov nespĺňa požiadavky stanovené v časti 6.1.5 a/alebo časti 6.1.6;
2. Existuje jasný dôkaz o tom, že konkrétna metóda použitá na generovanie súkromného kľúča bola chybná;
3. Poskytovateľ si je vedomý preukázanej alebo overenej metódy, ktorá vystavuje súkromný kľúč žiadateľa riziku kompromitácie;
4. Poskytovateľ bol predtým upozornený na to, že súkromný kľúč žiadateľa utrpel kompromitáciu kľúča, napríklad prostredníctvom ustanovení časti 4.9.1.1;
5. Poskytovateľ si je vedomý preukázanej alebo overenej metódy na jednoduchý výpočet súkromného kľúča žiadateľa na základe verejného kľúča (ako napríklad Debian weak key, pozri https://wiki.debian.org/SSLkeys).

### 6.1.2 Doručenie súkromného kľúča žiadateľovi/predplatiteľovi
Iné strany ako Predplatiteľ nesmú archivovať súkromný kľúč Predplatiteľa bez jeho súhlasu.
Ak Poskytovateľ zistí, že súkromný kľúč Predplatiteľa bol oznámený neoprávnenej osobe alebo organizácii, ktorá nie je prepojená s Predplatiteľom, Poskytovateľ zruší všetky certifikáty TLS, ktoré obsahujú verejný kľúč zodpovedajúci oznámenému súkromnému kľúču.

### 6.1.3 Doručenie verejného kľúča vydavateľovi certifikátu
Verejný kľúč je bezpečne doručený certifikačnej autorite prostredníctvom aplikácie RA Client v online režime počas procesu vydávania TLS certifikátu. Komunikácia medzi aplikáciou RA Client a vydávajúcou CA je autorizovaná podpisom všetkých odoslaných údajov zamestnancom RA, pričom autorizácia vydania daného zamestnanca RA je na strane CA kontrolovaná v automatickom režime.

### 6.1.4 Doručenie verejného kľúča CA spoliehajúcim sa stranám
Žiadne ustanovenia.

### 6.1.5 Veľkosti kľúčov
Pre RSA kľúče musí byť veľkosť modulu aspoň 2048 bitov a musí byť deliteľná 8.

### 6.1.6 Generovanie parametrov verejného kľúča a kontrola kvality
Parametre a kvalita verejného kľúča Poskytovateľa (koreňový, podriadený, krížový) sú určené PMA a kontrola kvality sa kontroluje počas obradu generovania kľúčov.

Poskytovateľ musí na generovanie a ukladanie kľúčov používať kryptografické hardvérové ​​moduly, ktoré spĺňajú požiadavky normy FIPS 186-2, čo zabezpečuje náhodné generovanie kľúčov RSA s veľkosťou najmenej 2048 bitov.

RSA: Poskytovateľ musí potvrdiť, že hodnota verejného exponentu je nepárne číslo rovné 3 alebo viac. Okrem toho by verejný exponent mal byť v rozsahu medzi 2^16+1 a 2^256-1.

Modul by mal mať aj nasledujúce charakteristiky: nepárne číslo, nie mocnina prvočísla, a nemať žiadne deliteľa menšie ako 752. [Zdroj: Časť 5.3.3, NIST SP 800-89].

### 6.1.7 Účely použitia kľúčov
Súkromné ​​kľúče zodpovedajúce koreňovým certifikátom sa nesmú použiť na podpisovanie certifikátov, s výnimkou nasledujúcich prípadov:
1. Self-signed certifikáty reprezentujúce samotnú koreňovú CA;
2. Certifikáty pre podriadené CA a krížové certifikáty podriadených CA;
3. Certifikáty pre infraštruktúrne účely (certifikáty pre administratívne role, certifikáty pre interné operačné zariadenia CA); a
4. Certifikáty na overenie odpovede OCSP.

Kľúče vydané zamestnancom RA sa môžu použiť iba na prístup do IS poskytovateľa prostredníctvom aplikácie RA Client a tiež na podpisovanie údajov odoslaných v procese vydávania TLS certifikátu aplikáciou RA Client. Môžu sa použiť aj na prístup na portál razona.disig.sk, kde sú k dispozícii všetky potrebné informácie pre zamestnanca RA.

## 6.2 Ochrana súkromného kľúča a inžinierstvo kryptografického modulu

### 6.2.1 Štandardy a kontroly kryptografického modulu
Na ochranu svojich súkromných kľúčov (koreňových certifikačných autorít, podriadených certifikačných autorít) musí Poskytovateľ používať hardvérové ​​kryptografické moduly certifikované podľa normy FIPS 140-2 úrovne 3. Moduly musia byť uložené v zabezpečených priestoroch, ku ktorým majú prístup iba osoby s dôveryhodnými rolami.

Súkromné ​​kľúče certifikačnej autority Poskytovateľa možno použiť iba na podpisovanie TLS certifikátov a zoznamov CRL vydaných Poskytovateľom.
Zariadenia certifikačnej autority musia byť trvalo chránené pred neoprávneným prístupom, a to aj pred neoprávneným fyzickým prístupom.
Modul HSM musí spĺňať požiadavky na ochranu pred zachytením elektromagnetickým žiarením.

Súkromné ​​kľúče certifikačnej autority Poskytovateľa:

* sú uložené a používané výlučne v moduloch HSM, ktoré spĺňajú príslušné bezpečnostné požiadavky;
* sú aktivované iba oprávnenými osobami v režime K/N;
* nie sú nikdy exportované z HSM v nešifrovanej forme.

### 6.2.2 Súkromný kľúč (K z N) kontrola viacerými osobami
V prípade operácií so súkromnými kľúčmi Poskytovateľa (napr. generovanie, zálohovanie, likvidácia) sa zúčastní príslušný počet oprávnených osôb, vždy na princípe „K“ z „N“.

### 6.2.3 Úschova súkromného kľúča
Žiadne ustanovenie.

### 6.2.4 Zálohovanie súkromného kľúča
Súkromné ​​kľúče Poskytovateľa sa generujú a ukladajú v hardvérových kryptografických moduloch.
Súkromné ​​kľúče sa vždy šifrujú v prípade, že oprávnení pracovníci v zmysle článku 6.2.2 vykonávajú ich prenos na účely zálohovania a obnovy, prenos súkromných kľúčov a ich obnovenie do iného hardvérového kryptografického modulu je možné len týmto spôsobom.

### 6.2.5 Archivácia súkromného kľúča
Žiadne ustanovenie.

### 6.2.6 Prenos súkromného kľúča do alebo z kryptografického modulu
Pozri článok 6.2.4.

### 6.2.7 Úložisko súkromného kľúča v kryptografickom module
Súkromné ​​kľúče podriadenej CA používané na podpisovanie certifikátov TLS vydávaných koncovým používateľom musia byť uložené v HSM. Súkromné ​​kľúče môžu opustiť modul iba v zašifrovanej forme, ktorá neumožní ich obnovenie bez príslušného počtu oprávnených osôb na hlavnom "K" z "N".
Všetky HSM moduly Poskytovateľa musia byť prevádzkované v zabezpečenom prostredí s kontrolou prístupu.

### 6.2.8 Aktivácia súkromných kľúčov
Oprávnené osoby podľa článku 6.2.2 môžu aktivovať iba súkromné ​​kľúče Poskytovateľa.

Po aktivácii musí každá oprávnená osoba z požadovaného počtu oprávnených osôb vložiť svoju čipovú kartu do modulu HSM a zadať heslo.

Ochrana súkromného kľúča Predplatiteľom/Držiteľom, ktorému Poskytovateľ vydal certifikát TLS, je výhradnou zodpovednosťou Predplatiteľa/Držiteľa. Poskytovateľ odporučí všetkým Predplatiteľom/Držiteľom, aby si chránili svoje súkromné ​​kľúče pomocou silného hesla, aby sa predišlo zneužitiu ich súkromného kľúča.

### 6.2.9 Deaktivácia súkromných kľúčov
Deaktiváciu súkromného kľúča v module HSM môže vykonať iba oprávnená osoba (správca CA) alebo sa súkromné ​​kľúče môžu deaktivovať automaticky v prípade výpadku relácie alebo výpadku napájania modulu HSM.

### 6.2.10 Likvidácia súkromných kľúčov
Poskytovateľ zabezpečí technickými a organizačnými opatreniami, aby sa súkromný kľúč Poskytovateľa nedal použiť po skončení jeho životného cyklu. Ukončenie životného cyklu súkromného kľúča CA a prijaté technické a organizačné opatrenia sa vyhotovia so záznamom podpísaným všetkými prítomnými stranami.

### 6.2.11 Možnosti kryptografického modulu
Pozri časť 6.2.1.

## 6.3 Ostatné aspekty správy párov kľúčov
### 6.3.1 Archivácia verejného kľúča
Žiadne ustanovenie.

### 6.3.2 Obdobia platnosti certifikátov a používania párov kľúčov

| Typ certifikátu | Platnosť (minimum) | Platnosť (maximum) |
| :--- | :---: | :---: |
| Koreňová CA (Root CA) | 2922 dní | 9132 dní |
| Podriadená CA (Subordinate CA) | | 1095 dní |
| TLS certifikát | - | 395 dní do 14. 3. 2026<br> 200 dní od 15. 3. 2026 do 14. 3. 2027<br> 100 dní od 15. 3. 2027 do 14.3.2029<br> 47 dní od 15. 3. 2029|

Pri výpočtoch sa deň počíta ako 86 400 sekúnd.

## 6.4 Aktivačné údaje
### 6.4.1 Generovanie a inštalácia aktivačných údajov
Aktivačné údaje pre súkromný kľúč zamestnanca RA si vyberá samotný zamestnanec RA bezprostredne po prevzatí hardvérového zariadenia, pred jeho prvým použitím na prístup do IS Poskytovateľa prostredníctvom aplikácie RA Client.

### 6.4.2 Ochrana aktivačných údajov
Zamestnanec RA je výhradne zodpovedný za ochranu súkromných kľúčov zamestnanca RA.
Pri vydávaní TLS certifikátu je každý zamestnanec RA zodpovednou osobou Poskytovateľa upozornený na potrebu ochrany súkromného kľúča silným heslom, aby sa zabránilo jeho zneužitiu počas celej doby jeho používania.
### 6.4.3 Ďalšie aspekty aktivačných údajov
Žiadne ustanovenie.

## 6.5 Počítačové bezpečnostné kontroly
### 6.5.1 Špecifické technické požiadavky na počítačovú bezpečnosť
Poskytovateľ vykonáva všetky funkcie dôveryhodného poskytovateľa služieb pomocou dôveryhodného systému, ktorý spĺňa požiadavky definované v jeho Bezpečnostnom projekte pre informačné systémy.
Poskytovateľ vydávajúci TLS certifikáty spĺňa špecifické požiadavky na informačnú bezpečnosť dôveryhodného poskytovateľa služieb, ako je definované v norme ETSI EN 319 411-1 „Elektronické podpisy a infraštruktúry (ESI); Požiadavky na politiku a bezpečnosť pre poskytovateľov dôveryhodných služieb vydávajúcich certifikáty; Časť 1 Všeobecné požiadavky“ [10]

Všetky systémy musia byť pravidelne overované na prítomnosť škodlivého kódu a chránené pred spyware a vírusmi.
Poskytovateľ musí presadzovať viacfaktorové overovanie pre všetky účty, ktoré môžu priamo spôsobiť vydanie TLS certifikátu.

### 6.5.2 Hodnotenie počítačovej bezpečnosti
Žiadne ustanovenie.

## 6.6 Technické kontroly životného cyklu
### 6.6.1 Kontroly vývoja systému
Žiadne ustanovenie.

### 6.6.2 Kontroly riadenia bezpečnosti
Žiadne ustanovenie.

### 6.6.3 Kontroly bezpečnosti životného cyklu
Žiadne ustanovenie.

## 6.7 Kontroly sieťovej bezpečnosti
Poskytovateľ zabezpečí implementáciu požiadaviek dokumentu „Network and Certificate System Security Requirements“[22].

## 6.8 Časové pečiatky
Žiadne ustanovenie.

# 7. Profily certifikátov, CRL a OCSP
Profily TLS certifikátov a zoznamy zrušených certifikátov (CRL) sú nastavené centrálne – pracovník RA nemôže meniť štruktúru TLS certifikátov.

## 7.1 Profil certifikátu

### 7.1.1 Číslo verzie
Tieto CP/CPS povoľujú vydávanie iba TLS certifikátov zodpovedajúcich verzii 3 štandardu X.509.

### 7.1.2 Obsah a rozšírenia certifikátu

#### 7.1.2.1 Certifikáty koreňovej CA Poskytovateľa
Algoritmy a dĺžky kľúčov použité v koreňovom certifikáte Poskytovateľa:

| | |
| :--- | :--- |
| Názov algoritmu podpisu:| **sha256RSA** |
| Verejný kľúč:| **RSA, dĺžka 4 096 bitov** |

Tabuľka 3: Obsah položiek v koreňovom certifikáte Poskytovateľa

| Skratka názvu | OID | Názov | Obsah |
|:---:|:---:|:---:|:---:|
| C | 2.5.4.6 | countryName | SK |
| L | 2.5.4.7 | localityName | Bratislava |
| O | 2.5.4.10 | organizationName | Disig a.s. |
| CN | 2.5.4.3 | commonName | v závislosti od typu CA ¹ |

¹ CN musí obsahovať obchodné meno certifikačnej autority, t. j. CA Disig doplnené podľa potreby o koreňové rozlišovacie meno CA Disig, napr. Root R3 atď.

Od 15. 9. 2023 môže predmet (subject) certifikátu koreňovej CA obsahovať len položky uvedené v časti 7.1.2.10.2 TLS BR [3].

Tabuľka 4: Rozšírenia certifikátu v certifikátoch koreňovej CA

| Rozšírenie / OID | Prítomnosť | Kritické |
|:---|:---:|:---:|
| basicConstraints / 2.5.29.19 | ÁNO | ÁNO |
| keyUsage / 2.5.29.15 | ÁNO | ÁNO |
| subjectKeyIdentifier / 2.5.29.14 | ÁNO | NIE |

Od 15. 9. 2023 môžu rozšírenia certifikátu koreňovej CA obsahovať len položky uvedené v časti 7.1.2.1.2 TLS BR [3].

#### 7.1.2.2	Profil certifikátu podriadenej Cross‑Certified CA
Tento profil sa vzťahuje na cross-certifikát vydaný CA Disig Root R2 pre CA Disig TLS Root R3 za účelom preklenutia dôvery počas prechodu na jednoúčelovú TLS hierarchiu.   
Tento certifikát je určený na podporu vydávania TLS certifikátov s overením organizácie (OV) a nesmie sa používať na priame vydávanie certifikátov pre koncové entity.

Profil certifikátu je v súlade s TLS BR [3] a požiadavkami root programov spoločností Google, Apple, Mozilla a Microsoft.   
Certifikát musí byť technicky obmedzený na Extended Key Usage (EKU) serverAuth. 
Rozšírenie keyUsage musí byť označené ako kritické s nastavenými bitmi keyCertSign a cRLSign.  
Na zabezpečenie integrity hierarchie je pathLenConstraint nastavený na 0. Podpisový algoritmus musí byť SHA-256 alebo silnejší.  
Verejný kľúč musí byť typu RSA s minimálnou dĺžkou 4096 bitov. Rozšírenie certificatePolicies musí obsahovať identifikátor politiky OV (2.23.140.1.2.2), aby signalizovalo súlad s TLS Baseline Requirements pre overovanie organizácií.  

Algoritmy a dĺžky kľúčov použité v krížovom (cross) certifikáte Poskytovateľa:

|  | |
| :--- | :--- |
| Názov algoritmu podpisu:|**sha256RSA**|
| Verejný kľúč:|**RSA, length 4 096 bit**|

Tabuľka 5: Obsah položiek v certifikáte podriadenej Cross‑Certified CA

|Skratka názvu |OID|Názov |Obsah|
|:----------:|:---:|:----:|:-------:|
|C|2.5.4.6|countryName|SK|
|L|2.5.4.7|localityName|Bratislava|
|O|2.5.4.10|organizationName|Disig a.s.|
|CN|2.5.4.3|commonName|CA Disig TLS Root R3|


Tabuľka 6: Rozšírenia certifikátu v certifikáte podriadenej Cross‑Certified CA 

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

#### 7.1.2.3	Profil certifikátu podriadenej technicky obmedzenej CA bez TLS
Žiadne ustanovenia.

#### 7.1.2.4	Profil certifikátu technicky obmedzenej CA na podpisovanie predbežného certifikátu	
Žiadne ustanovenia.

#### 7.1.2.5	Profil certifikátu podriadenej technicky obmedzenej TLS CA
Žiadne ustanovenia.	

#### 7.1.2.6 Podriadená certifikačná autorita Poskytovateľa
Algoritmy a dĺžky kľúčov použité v podriadenej CA:

| | |
| :--- | :--- |
| Názov algoritmu podpisu:| **sha256RSA** |
| Verejný kľúč:| **RSA, dĺžka 2 048 bitov** |
| Platnosť podriadenej CA:| maximálne 7 rokov |

Tabuľka 7: Obsah položiek v certifikáte podriadenej CA

| Skratka názvu | OID | Názov | Obsah |
|:---:|:---:|:---:|:---:|
| C | 2.5.4.6 | countryName | SK |
| L | 2.5.4.7 | localityName | Bratislava |
| O | 2.5.4.10 | organizationName | Disig a.s. |
| CN | 2.5.4.3 | commonName | v závislosti od typu CA ² |

² CN musí obsahovať obchodné meno certifikačnej autority, napr. CA Disig doplnené o rozlišovacie meno, napr. R2I2 Certification Service atď.

Tabuľka 8: Rozšírenia certifikátu v podriadenej CA

| Rozšírenie / OID | Prítomnosť | Kritické |
|:---|:---:|:---:|
| authorityKeyIdentifier / 2.5.29.35 | ÁNO | NIE |
| basicConstraints / 2.5.29.19 | ÁNO | ÁNO |
| certificatePolicies / 2.5.29.32 | ÁNO | NIE |
| keyUsage / 2.5.29.15 | ÁNO | ÁNO |
| subjectKeyIdentifier / 2.5.29.14 | ÁNO | NIE |
| crlDistributionPoints / 2.5.29.31 | ÁNO | NIE |
| extKeyUsage / 2.5.29.37 | ÁNO | NIE |
| authorityInfoAccess / 1.3.6.1.5.5.7.1.1 | ÁNO | NIE |

Rozšírenie cRLDistributionPoints obsahuje HTTP URL adresu služby CRL danej CA, ako je špecifikované v časti 2.2.3 týchto CP/CPS.

#### 7.1.2.7 TLS certifikáty koncových používateľov
Podrobnosti o obsahu predmetu TLS certifikátov vydávaných podľa týchto CP/CPS sú uvedené v časti 3.1.4.

Nasledujúca tabuľka uvádza rozšírenia použité vo vydaných TLS certifikátoch:

| Názov rozšírenia | ASN.1 názov a OID / Popis | Prítomnosť | Kritické |
|:---|:---|:---:|:---:|
| AuthorityInfoAccess | {id-pe-authorityInfoAccess} {1.3.6.1.5.5.7.1.1} Špecifikuje adresu (HTTP), kde je možné získať certifikáty vydavateľa a adresu OCSP. | ÁNO | NIE |
| Authority Key Identifier | {id-ce-authorityKeyIdentifier} {2.5.29.35} Identifikuje verejný kľúč použitý na overenie podpisu na tomto certifikáte alebo CRL. | ÁNO | NIE |
| Certificate Policies | {id-ce-certificatePolicies} {2.5.29.32} Uvádza politiky certifikátu platné pre tento certifikát. | ÁNO | NIE |
| Extended Key Usage | {id-ce-extKeyUsage} {2.5.29.37} Indikuje účely, na ktoré sa môže certifikovaný verejný kľúč použiť nad rámec základných účelov. | ÁNO | NIE |
| subjectAltName | {id-ce-subjectAltName} {2.5.29.17} Obsahuje jedno alebo viac alternatívnych mien entity (napr. FQDN). | ÁNO | NIE |
| Key Usage | {id-ce-keyUsage} {2.5.29.15} Indikuje účel, na ktorý sa používa certifikovaný verejný kľúč. | ÁNO | NIE |
| CRL Distribution Points | {id-ce-cRLDistributionPoints} {2.5.29.31} Identifikuje body distribúcie CRL pre zistenie, či certifikát nebol zrušený. | ÁNO | NIE |

##### 7.1.2.7.1 Typy certifikátov odberateľov
Podľa týchto CP/CPS Poskytovateľ vydáva iba TLS certifikáty typu „Organization Validated“ (OV).

##### 7.1.2.7.2 Overenie domény (Domain Validated)
Poskytovateľ nevydáva tento typ TLS certifikátu.

##### 7.1.2.7.3 Overenie osoby (Individual Validated)
Poskytovateľ nevydáva tento typ TLS certifikátu.

##### 7.1.2.7.4 Overenie organizácie (Organization Validated)
Profil certifikátu TLS „Overené organizáciou“ musí spĺňať požiadavky uvedené v časti 7.1.2.7.4 TLS BR [3].

##### 7.1.2.7.5 Rozšírené overenie (Extended Validation)
Poskytovateľ nevydáva tento typ TLS certifikátu.

##### 7.1.2.7.6 Rozšírenia certifikátu predplatiteľa
Certifikáty vydané koncovému používateľovi môžu obsahovať iba rozšírenia uvedené v časti 7.1.2.7.6 TLS BR [3].

##### 7.1.2.7.7 Prístup k informáciám o autorite certifikátu predplatiteľa
Položka „Prístup k informáciám o autorite“ v TLS certifikáte koncového používateľa musí byť v súlade s požiadavkami uvedenými v časti 7.1.2.7.7 TLS BR [3].

##### 7.1.2.7.8 Základné obmedzenia certifikátu predplatiteľa
TLS certifikát koncového používateľa túto položku neobsahuje.

##### 7.1.2.7.9 Zásady certifikátu predplatiteľa
Položka „Zásady certifikátov“ v TLS certifikáte koncového používateľa musí byť v súlade s požiadavkami uvedenými v časti 7.1.2.7.9 TLS BR [3].

##### 7.1.2.7.10 Rozšírené použitie kľúča certifikátu predplatiteľa
Položka „Rozšírené použitie kľúča“ v TLS certifikáte koncového používateľa musí byť v súlade s požiadavkami uvedenými v časti 7.1.2.7.10 TLS BR [3].

##### 7.1.2.7.11 Použitie kľúča certifikátu predplatiteľa
Položka „Použitie kľúča“ v TLS certifikáte koncového používateľa musí byť v súlade s požiadavkami uvedenými v časti 7.1.2.7.11 normy TLS BR [3].

##### 7.1.2.7.12 Alternatívny názov subjektu certifikátu predplatiteľa
Položka „Alternatívny názov subjektu“ v TLS certifikáte koncového používateľa musí byť v súlade s požiadavkami uvedenými v časti 7.1.2.7.12 normy TLS BR [3].

#### 7.1.2.8 Profil certifikátu OCSP respondera
Ak poskytovateľ priamo nepodpisuje odpovede OCSP, môže použiť autorizovaného OCSP respondera, ako je definované v RFC 6960 [19]. Vydávajúca certifikačná autorita odpovedajúceho musí byť rovnaká ako vydávajúca certifikačná autorita pre TLS certifikáty , pre ktoré poskytuje odpovede.
Profil certifikátu OCSP respondera musí spĺňať požiadavky uvedené v časti 7.1.2.8 dokumentu TLS BR [3].

##### 7.1.2.8.1 Platnosť OCSP respondera
Platnosť certifikátu OCSP respondera  musí spĺňať požiadavky uvedené v časti 7.1.2.8.1 dokumentu TLS BR [3].

##### 7.1.2.8.2 Rozšírenia OCSP respondera
Rozšírenia v certifikáte OCSP respondera musia spĺňať požiadavky uvedené v časti 7.1.2.8.2 dokumentu TLS BR [3].

##### 7.1.2.8.3 Prístup k informáciám o autorite OCSP respondera
Položka „Prístup k informáciám o autorite“ v certifikáte OCSP respondera musí spĺňať požiadavky uvedené v časti 7.1.2.8.3 dokumentu TLS BR [3].

##### 7.1.2.8.4 Základné obmedzenia OCSP respondera
„Základné obmedzenia“ v certifikáte OCSP respondera musia spĺňať požiadavky uvedené v časti 7.1.2.8.4 dokumentu TLS BR [3].

##### 7.1.2.8.5 Použitie rozšíreného kľúča OCSP respondera
„Rozšírené použitie kľúča“ v certifikáte OCSP respondera musí byť v súlade s požiadavkami uvedenými v časti 7.1.2.8.5 normy TLS BR [3].

##### 7.1.2.8.6 OCSP responder id-pkix-ocsp-nocheck
„id-pkix-ocsp-nocheck“ v certifikáte OCSP respondera a musí byť v súlade s požiadavkami uvedenými v časti 7.1.2.8.6 normy TLS BR [3].

##### 7.1.2.8.7 Použitie kľúča OCSP respondera
„Použitie kľúča“ v certifikáte OCSP respondera musí byť v súlade s požiadavkami uvedenými v časti 7.1.2.8.7 normy TLS BR [3].

##### 7.1.2.8.8 Zásady certifikátov odpovedajúceho OCSP
„Zásady certifikátov“ v certifikáte OCSP respondera musia byť v súlade s požiadavkami uvedenými v časti 7.1.2.8.8 dokumentu TLS BR [3].

#### 7.1.2.9 Profil TLS predcertifikátu
Predcertifikát je podpísaná dátová štruktúra, ktorú je možné odoslať do protokolu Certificate Transparency (CT log), ako je definované v RFC 6962 [23].
Predcertifikát TLS sa štrukturálne javí ako identický s TLS certifikátom, s výnimkou špeciálneho kritického rozšírenia „poison“ s OID 1.3.6.1.4.1.11129.2.4.3.
Toto rozšírenie zabezpečuje, že predcertifikát TLS nebude akceptovaný ako certifikát TLS klientmi, ktorí spĺňajú RFC 5280. Existencia podpísaného predcertifikátu TLS sa môže považovať za dôkaz existencie zodpovedajúceho certifikátu TLS, pretože podpis predstavuje záväzný záväzok poskytovateľa, že môže vydať takýto certifikát TLS.

Predcertifikát TLS bol vytvorený po tom, čo sa poskytovateľ rozhodol vydať TLS certifikát, ale pred skutočným podpísaním TLS certifikátu. Poskytovateľ môže vytvoriť a podpísať predcertifikát TLS zodpovedajúci TLS certifikátu na účely odoslania do protokolov transparentnosti certifikátov.
Poskytovateľ môže použiť vrátené podpísané časové pečiatky certifikátov na následnú zmenu poľa rozšírení certifikátu pridaním zoznamu časových pečiatok podpísaných certifikátov, ako je definované v časti 7.1.2.11.3 a ako to povoľuje príslušný profil, pred podpísaním TLS certifikátu.

Profil predcertifikátu TLS popisuje transformácie, ktoré sú povolené pre TLS certifikát na vytvorenie predcertifikátu TLS. Poskytovateľ nevydá predcertifikát TLS, pokiaľ nie je ochotný vydať zodpovedajúci TLS certifikát, bez ohľadu na to, či tak urobil. Podobne poskytovateľ nevydá predcertifikát TLS, pokiaľ zodpovedajúci certifikát TLS nie je v súlade s TLS BR [3], bez ohľadu na to, či poskytovateľ podpíše zodpovedajúci certifikát TLS.
Predcertifikát TLS môže byť vydaný buď priamo vydávajúcou certifikačnou autoritou, alebo technicky obmedzenou certifikačnou autoritou podpisujúcou predcertifikát TLS, ako je definované v časti 7.1.2.4 TLS BR [3].

##### 7.1.2.9.1 Rozšírenia profilu predcertifikátu TLS – vydané priamo
Rozšírenia musia spĺňať požiadavky uvedené v časti 7.1.2.9.1 TLS BR [3].

##### 7.1.2.9.2 Rozšírenia profilu predcertifikátu TLS – vydaný CA predcertifikátu TLS
Žiadne ustanovenie.

##### 7.1.2.9.3 Poison rozšírenie predcertifikátu TLS
Predcertifikát TLS musí obsahovať rozšírenie poison predcertifikátu TLS (OID: 1.3.6.1.4.1.11129.2.4.3).
Toto rozšírenie musí mať reťazec extnValue OCTET, ktorý je presne hexadecimálne kódovaný počet bajtov 0500, kódovaná reprezentácia hodnoty ASN.1 NULL, ako je uvedené v RFC 6962 [23], časť 3.1.

##### 7.1.2.9.4 Identifikátor kľúča autority predcertifikátu TLS
Žiadne ustanovenie.

#### 7.1.2.10 Spoločné polia CA 
Pred vydaním CA certifikátu poskytovateľ zabezpečí, aby obsah CA certifikátu vrátane obsahu každej položky spĺňal všetky požiadavky aspoň jedného profilu CA certifikátu zdokumentovaného v časti 7.1.2 v súlade s popisom položiek v časti 7.1.2.10 TLS BR [3].

#### 7.1.2.11 Spoločné polia certifikátu
Pred vydaním certifikátu TLS poskytovateľ zabezpečí, aby obsah certifikátu TLS vrátane obsahu každej položky plne spĺňal všetky požiadavky aspoň jedného profilu certifikátu TLS zdokumentovaného v časti 7.1.2 v súlade s popisom položiek pre typ certifikátu v časti 7.1.2.7 TLS BR [3].

### 7.1.3 Identifikátory objektov algoritmov (Algorithm OIDs)
#### 7.1.3.1 SubjectPublicKeyInfo
Nasledujúce požiadavky sa vzťahujú na pole subjectPublicKeyInfo v rámci TLS certifikátu alebo predcertifikátu TLS. Nie je povolené žiadne iné kódovanie.

##### 7.1.3.1.1 RSA
Poskytovateľ označuje kľúč RSA identifikátorom algoritmu rsaEncryption (OID: 1.2.840.113549.1.1.1). Parametre musia byť prítomné a explicitne nastavené na NULL. 
Poskytovateľ nesmie použiť iný algoritmus, ako napríklad identifikátor algoritmu id-RSASSA-PSS (OID: 1.2.840.113549.1.1.10), na označenie kľúča RSA. 
Zakódovaný AlgorithmIdentifier pre RSA kľúče musí byť identický s nasledujúcimi hexadecimálnymi bajtmi:
*300d06092a864886f70d0101010500*

##### 7.1.3.1.2 ECDSA  
Žiadne ustanovenie.

#### 7.1.3.2 Identifikátor algoritmu podpisu
Všetky objekty podpísané súkromným kľúčom poskytovateľa CA musia spĺňať požiadavky na používanie „Identifikátora algoritmu“ alebo typu odvodeného od „Identifikátora algoritmu“ v kontexte podpisov, ak je to uvedené v časti 7.1.3.2 TLS BR [3].

##### 7.1.3.2.1 RSA
Poskytovateľ musí používať algoritmus a kódovanie jedného podpisu v súlade s požiadavkami uvedenými v časti 7.1.3.2.1 TLS BR [3].
Zakódovaný „Identifikátor algoritmu“ musí byť bajt po bajte identický so zadanými hexadecimálne kódovanými bajtami, ako je uvedené v časti 7.1.3.2 TLS BR [3].

##### 7.1.3.2.2 ECDSA
Žiadne ustanovenie.

### 7.1.4 Formy mien
Pre všetky TLS certifikáty vydané poskytovateľom v súlade s týmto CP/CPS musí byť kódovanie mien v súlade s požiadavkami uvedenými v časti 7.1.4 TLS BR [3].

### 7.1.5 Obmedzenia mien
Žiadne ustanovenie.

### 7.1.6 Objektový identifikátor politiky certifikátu
#### 7.1.6.1 Vyhradené identifikátory certifikačnej politiky
OID politiky 2.23.140.1.2.2 je vyhradený pre typ TLS certifikátu „Organization Validated“ (OV).

### 7.1.7 Použitie rozšírenia Policy Constraints (Obmedzenia politík)
Žiadne ustanovenie.

### 7.1.8 Syntax a sémantika kvalifikátorov politík
Žiadne ustanovenie.

### 7.1.9 Spracovanie sémantiky pre kritické rozšírenie Certificate Politics (Politiky certifikátov)
Žiadne ustanovenie.


## 7.2 Profil CRL
S účinnosťou od 15. 3. 2024 Poskytovateľ vydáva zoznamy CRL v súlade s profilom špecifikovaným v časti 7.2 TLS BR [3]. 

### 7.2.1 Číslo verzie
Všetky zoznamy CRL vydané poskytovateľom musia byť v súlade s RFC 5280 a musia byť verzie 2.

### 7.2.2 Zoznam CRL a rozšírenia záznamov CRL
Zoznam CRL musí obsahovať rozšírenia a , ako je uvedené v RFC 5280. Zoznamy CRL sú zverejnené v úložisku na miestach definovaných v časti 2.2.3.

#### 7.2.2.1 Distribučný bod CRL
Vydávame iba úplné a kompletné zoznamy CRL.

## 7.3 Profil OCSP

Ak sa odpoveď OCSP vzťahuje na koreňový CA certifikát  alebo podriadený CA certifikát vrátane krížového CA certifikátu a tento certifikát bol zrušený, dôvod zrušenia sa musí uviesť v poli RevokedInfo CertStatus.
Uvedený dôvod zrušenia CRLReason musí obsahovať hodnotu povolenú pre CRL, ako je uvedené v časti 7.2.2 TLS BR [3].

### 7.3.1 Číslo verzie
Žiadne ustanovenie.

### 7.3.2 Rozšírenia OCSP
Rozšírenia singleExtensions v odpovedi OCSP nesmú obsahovať reasonCode (OID 2.5.29.21) rozšírenie CRL.

# 8. Audit zhody a iné posudzovania  
Účelom auditu zhody je zabezpečiť, aby mal Poskytovateľ uspokojivý systém práce, ktorý zaručuje kvalitu dôveryhodných služieb poskytovaných Poskytovateľom, a zaručuje, že koná v súlade so všetkými požiadavkami týchto CP/CPS, nariadenia eIDAS [8] a CA/Browser fóra [3]. Všetky aspekty prevádzky CA týkajúce sa týchto CP/CPS musia byť predmetom auditov zhody.  

## 8.1 Periodicita alebo okolnosti posudzovania  
Poskytovateľ sa podrobí auditu zhody poskytovaných dôveryhodných služieb v zmysle časti 1.4.1 najmenej raz ročne. Okrem toho má každá CA právo vyžiadať si pravidelné a mimoriadne preskúmania činností svojich podriadených CMA, aby potvrdila, že podriadené CMA fungujú v súlade s bezpečnostnými praktikami a postupmi opísanými v týchto CP/CPS.  

## 8.2 Identita/kvalifikácia posudzovateľa  
Audítor musí byť kompetentný v oblasti auditov zhody a musí byť dôkladne oboznámený s auditovanými CP/CPS a spĺňať požiadavky na kvalifikáciu opísané v časti 8.2 TLS BR [3].  

## 8.3 Vzťah posudzovateľa k posudzovanému subjektu  
Žiadne ustanovenia.  

## 8.4 Témy zahrnuté v posudzovaní  
Poskytovateľ bude auditovaný v súlade s národnou schémou, ktorá posudzuje zhodu s najnovšími verziami ETSI EN 319 411-1 [10], vrátane normatívnych odkazov z ETSI EN 319 401 [9].  
Audit musí byť vykonaný kvalifikovaným audítorom v zmysle odseku 8.2.  

## 8.5 Opatrenia prijaté v dôsledku nedostatku  
Ak audítor zistí nesúlad medzi prevádzkou CMA a ustanoveniami CP/CPS, prijmú sa nasledujúce opatrenia:   
* Audítor zaznamená nesúlad;  
* Audítor informuje subjekty definované v časti 8.6;  
* Poskytovateľ navrhne PMA príslušné nápravné opatrenia, vrátane predpokladaného času na ich implementáciu.  

PMA určí vhodné nápravné opatrenia, až po prípadné zrušenie TLS certifikátu CA.   

## 8.6 Oznamovanie výsledkov  
Správa z auditu musí výslovne uvádzať, že pokrýva príslušné systémy a procesy používané pri vydávaní všetkých TLS certifikátov, ktoré uvádzajú jeden alebo viac identifikátorov politík uvedených v časti 7.1.6.1. Poskytovateľ správu z auditu verejne sprístupní.  

Poskytovateľ zverejní svoju správu z auditu najneskôr tri mesiace po skončení auditovaného obdobia. V prípade oneskorenia dlhšieho ako tri mesiace Poskytovateľ poskytne vysvetľujúci list podpísaný kvalifikovaným audítorom.  

Správa z auditu musí obsahovať aspoň nasledujúce jasne označené informácie:  
1. názov auditovanej organizácie;  
2. názov a adresu organizácie vykonávajúcej audit;  
3. SHA-256 odtlačok všetkých koreňových a podriadených TLS certifikátov CA, vrátane krížovo certifikovaných podriadených TLS certifikátov CA, ktoré boli v rozsahu auditu;  
4. kritériá auditu, s číslom (číslami) verzií, ktoré boli použité na audit každého z TLS certifikátov (a súvisiacich kľúčov);  
5. zoznam dokumentov politiky Poskytovateľa, s číslami verzií, na ktoré sa počas auditu odkazovalo;  
6. či audit posudzoval časové obdobie alebo časový okamih;  
7. dátum začiatku a dátum konca auditovaného obdobia pre tie, ktoré pokrývajú časové obdobie;  
8. dátum časového okamihu pre tie, ktoré sú k časovému okamihu;  
9. dátum vydania správy, ktorý bude nevyhnutne po dátume ukončenia alebo dátume časového okamihu; a  
10. pre audity vykonané v súlade s ktorýmkoľvek zo štandardov ETSI - vyhlásenie indikujúce, či bol audit plným auditom alebo dozorným auditom, a ktoré časti kritérií boli aplikované a vyhodnotené, napr. DVCP/CPS, OVCP/CPS, NCP/CPS, NCP/CPS+, LCP/CPS, EVCP/CPS, EVCP/CPS+, QCP/CPS-w, Časť 1 (Všeobecné požiadavky) a/alebo Časť 2 (Požiadavky na poskytovateľov dôveryhodných služieb);  
11. pre audity vykonané v súlade s ktorýmkoľvek zo štandardov ETSI - vyhlásenie indikujúce, že audítor odkazoval na príslušné kritériá CA/Browser fóra, ako napríklad TLS BR [3], a použitú verziu.  

Autoritatívnu verziu verejne dostupných informácií o audite v anglickom jazyku poskytne kvalifikovaný audítor a Poskytovateľ zabezpečí, aby bola verejne dostupná.  
Správa z auditu musí byť k dispozícii ako PDF a musí v nej byť možné vyhľadávať text pre všetky požadované informácie. Každý odtlačok SHA-256 v správe z auditu musí byť veľkými písmenami a nesmie obsahovať dvojbodky, medzery ani odsadzovania.  

## 8.7 Vlastné audity  
Počas obdobia, v ktorom CA vydáva TLS certifikáty, Poskytovateľ monitoruje zhodu so svojimi CP/CPS a požiadavkami špecifikovanými v TLS BR [3] a kontroluje poskytované služby vykonávaním interných auditov aspoň na štvrťročnej báze na náhodne vybranej vzorke vydaných TLS certifikátov v počte vyššom ako jeden a maximálne v počte troch percent vydaných TLS certifikátov v období od predchádzajúceho interného auditu.  

# 9. Ostatné obchodné a právne záležitosti  

## 9.1 Poplatky  
Poskytovateľ má povinnosť zverejniť platný cenník dôveryhodných služieb a informácie, za akých je možné tieto služby objednať.   
Cenník dôveryhodných služieb alebo informácie o zmluvných podmienkach, za ktorých je možné tieto služby objednať, sú zverejnené na webovom sídle Poskytovateľa (pozri časť 1).  

### 9.1.1 Poplatky za vydanie alebo obnovu certifikátu  
Poplatok za TLS certifikáty sa platí za podmienok dohodnutých s Odberateľom / Držiteľom.   
Poskytovateľ musí zverejniť platný cenník svojich služieb prostredníctvom webového sídla svojej spoločnosti (pozri časť 1).  
V prípade poskytovania svojich služieb len zmluvnému partnerovi cenník nemusí byť zverejnený.  

### 9.1.2 Poplatky za prístup k certifikátu   
Pozri časť 9.1.1.  

### 9.1.3 Poplatky za zrušenie alebo prístup k informáciám o stave   
Tieto služby sa poskytujú bezplatne.  

### 9.1.4 Poplatky za ostatné služby  
Pozri časť 9.1.1  

### 9.1.5 Politika vrátenia peňazí  
V odôvodnených prípadoch môže Poskytovateľ na základe individuálneho posúdenia vrátiť platbu za poskytnuté služby.   

## 9.2 Finančná zodpovednosť   
Poskytovateľ musí mať dostatočné zdroje na vykonávanie dôveryhodných služieb, aby zostal solventný a bol schopný vyplatiť odškodné v prípade súdneho rozhodnutia alebo vyrovnania nárokov vyplývajúcich z poskytovania týchto služieb.  
Poskytovateľ má dostatočné zdroje na vykonávanie dôveryhodných služieb, ktoré poskytuje.  

### 9.2.1 Poistné krytie  
Poskytovateľ musí byť poistený pre prípad možnej škody, ktorá môže byť spôsobená Držiteľovi certifikátov alebo tretím stranám v súvislosti s poskytovaním dôveryhodných služieb.  
Poskytovateľ zodpovedá za škody vzniknuté použitím ním vydaného TLS certifikátu podľa platnej legislatívy (napr. Obchodný zákonník, Občiansky zákonník). Predpokladom je, že boli dodržané príslušné ustanovenia týchto CP/CPS. 

Zodpovednosť za škodu a výsledné vyrovnanie možno prijať len za predpokladu, že: 
* Držiteľ neporušil svoje povinnosti (najmä ochranu svojho súkromného kľúča);  
* ktokoľvek, kto sa spoliehal na TLS certifikát vydaný Poskytovateľom, urobil všetko pre to, aby zabránil akejkoľvek škode, najmä tým, že overil stav predmetného TLS certifikátu, t. j. či TLS certifikát nebol zrušený v rozhodujúcom čase, kedy sa naň spoliehal.   

Poskytovateľ nenesie žiadnu finančnú zodpovednosť za akékoľvek škody, ktoré by vznikli Držiteľovi certifikátu alebo spoliehajúcej sa strane v súvislosti s použitím TLS certifikátu v konkrétnej softvérovej aplikácii alebo v súvislosti so skutočnosťou, že TLS certifikát nie je možné použiť s konkrétnou aplikáciou alebo hardvérom.  

Akýkoľvek nárok na náhradu škody musí byť podaný písomne.  
Poskytovateľ je poistený proti možným škodám, ktoré môžu byť spôsobené Odberateľovi / Držiteľovi certifikátu alebo tretím stranám v súvislosti s poskytovaním dôveryhodných služieb.  

### 9.2.2 Ostatné aktíva  
Žiadne ustanovenia.  

### 9.2.3 Poistenie alebo záručné krytie pre koncové entity  
Žiadne ustanovenia.  

## 9.3 Dôvernosť obchodných informácií  

### 9.3.1 Rozsah dôverných informácií  
Dôvernými informáciami podliehajúcimi príslušnej ochrane sú:  
* súkromné kľúče Poskytovateľa používané na podpisovanie TLS certifikátov vydaných podriadeným CA;   
* súkromné kľúče podriadených CA používané na podpisovanie TLS certifikátov vydaných koncovým používateľom;  
* súkromné kľúče služieb OCSP;  
* súkromné kľúče patriace výkonným zložkám Poskytovateľa (personál RA);  
* infraštruktúra (napr. dokumenty, postupy, procedúry, súbory, skripty, heslá atď.) slúžiaca na zabezpečenie prevádzky CA Poskytovateľa;  
* osobné údaje držiteľov TLS certifikátov podliehajúce ochrane podľa Predpisov o ochrane osobných údajov [15].   

TLS certifikát môže obsahovať len informácie, ktoré sú dôležité a nevyhnutné na vykonávanie bezpečnej komunikácie s TLS certifikátom.  
Zoznam zzrušených TLS certifikátov (CRL) sa nepovažuje za dôverný.  

### 9.3.2 Informácie, ktoré nespadajú do rozsahu dôverných informácií  
Poskytovateľ nesmie zverejniť informácie týkajúce sa Odberateľa alebo Držiteľa certifikátu žiadnej tretej strane. Zverejnenie je možné len vtedy, ak:
je to povolené týmito CP/CPS; je to vyžadované zákonom alebo príkazom kompetentného súdu alebo uvedené v zmluve medzi Poskytovateľom a jeho Odberateľom. Každá požiadavka na uvoľnenie informácií musí byť autentifikovaná a zdokumentovaná. 

Poskytovateľ bude s osobnými údajmi Odberateľa nakladať v súlade s platnými zákonmi a neposkytne ich žiadnej tretej strane s výnimkou subjektov legálne oprávnených posudzovať činnosť Poskytovateľa alebo príslušných vládnych orgánov, ako je polícia, súd alebo prokurátor.  

### 9.3.3 Zodpovednosť za ochranu dôverných informácií  
Účastníci, ktorí dostanú dôverné informácie, sú zodpovední za ich ochranu pred zverejnením a zdržia sa ich poskytovania tretej strane.  

## 9.4 Súkromie osobných informácií  

### 9.4.1 Plán ochrany súkromia   

Poskytovateľ bude spracúvať osobné údaje Odberateľov / Držiteľov certifikátov alebo oprávnených osôb v súlade s požiadavkami Predpisov o ochrane osobných údajov [15].   

### 9.4.2 Informácie považované za súkromné  
Poskytovateľ musí mať definovaný rozsah osobných údajov, ktoré sú spracúvané pri poskytovaní kvalifikovaných dôveryhodných služieb.  

### 9.4.3 Informácie, ktoré sa nepovažujú za súkromné
Poskytovateľ môže v súlade s Predpismi o ochrane osobných údaj [15] definovať typy informácií, ktoré vedie pri poskytovaní dôveryhodných služieb a ktoré sa nepovažujú za osobné údaje.  

### 9.4.4 Zodpovednosť za ochranu súkromných informácií  
Účastníci, ktorí získajú osobné údaje, sú zodpovední za ich ochranu pred zverejnením a zdržia sa ich poskytovania tretej strane.  

### 9.4.5 Oznámenie a súhlas s používaním súkromných informácií  
Poskytovateľ je povinný postupovať v súlade s Predpismi o ochrane osobných údajov pri plnení informačnej povinnosti voči dotknutým osobám a pri získavaní ich súhlasu so spracovaním osobných údajov [15].  

### 9.4.6 Zverejnenie na základe súdneho alebo správneho konania  
Poskytovateľ môže tieto údaje poskytnúť aj tretím stranám, ak mu to ukladá alebo povoľuje príslušná legislatíva.  

### 9.4.7 Iné okolnosti zverejnenia informácií  
Žiadne ustanovenia.  

## 9.5 Práva duševného vlastníctva  
Tieto CP/CPS a súvisiace dokumenty predstavujú dôležité odborné znalosti (expertise) Poskytovateľa a sú chránené autorským právom.  
Poskytovateľ je držiteľom výhradných práv k IS Poskytovateľa a k obsahu svojho webového sídla.  

## 9.6 Vyhlásenia a záruky  
Poskytovateľ prostredníctvom týchto CP/CPS, Podmienok služby [12] a prípadne zmluvy o vydaní TLS certifikátu vyjadruje právne predpoklady týkajúce sa používania vydaných TLS certifikátov Odberateľom/Držiteľom a spoliehajúcou sa stranou.  

### 9.6.1 Vyhlásenia a záruky CA  
Pokiaľ ide o dôveryhodné služby, Poskytovateľ neposkytuje žiadne vyhlásenia ani záruky okrem tých, ktoré sú uvedené v týchto CP/CPS a Všeobecných podmienkach [12].  

### 9.6.2 Vyhlásenia a záruky RA  
Všetky externé registračné autority subjektov budú poskytovať dôveryhodné služby na základe zmluvného vzťahu s Poskytovateľom a v súlade s týmito CP/CPS.  

### 9.6.3 Vyhlásenia a záruky Odberateľa  
Odberateľ alebo Držiteľ certifikátu využíva dôveryhodné služby Poskytovateľa na vlastnú zodpovednosť a znáša všetky náklady na prostriedky diaľkovej komunikácie alebo iné technické prostriedky potrebné na využívanie týchto služieb (napr. softvér potrebný na vyhotovenie elektronického podpisu / pečate, softvér na autentifikáciu webovej stránky atď.).  

### 9.6.4 Vyhlásenia a záruky spoliehajúcej sa strany  
Spoliehajúca sa strana berie na vedomie, že sa môže slobodne rozhodnúť, či bude dôverovať a spoliehať sa na TLS certifikát vydaný Poskytovateľom a tým aj na informácie v ňom obsiahnuté. Spoliehajúca sa strana je povinná dodržiavať povinnosti opísané v časti 10 Všeobecných podmienok [12] v prípade rozhodnutia dôverovať TLS certifikátom Poskytovateľa; v opačnom prípade nesie výhradnú zodpovednosť za tým spôsobené právne následky.  

### 9.6.5 Vyhlásenia a záruky ostatných účastníkov  
Žiadne ustanovenia.  

## 9.7 Vylúčenie záruk  
Poskytovateľ je výhradne zodpovedný za škody spôsobené nedodržaním povinností podľa článku 13 nariadenia eIDAS [8] a nesplnením povinností v súlade s týmito CP/CPS.   

## 9.8 Obmedzenie zodpovednosti  
Poskytovateľ nezodpovedá za nepriame alebo podmienené straty alebo škody vzniknuté Odberateľom alebo spoliehajúcim sa stranám v súvislosti s používaním dôveryhodných služieb.  
Poskytovateľ nezodpovedá za žiadne škody (vrátane ušlého zisku) vzniknuté Odberateľovi / Držiteľovi TLS certifikátu, spoliehajúcej sa strane alebo akejkoľvek tretej strane v dôsledku:  
**a)** porušenia povinností Odberateľom / Držiteľom alebo spoliehajúcou sa stranou podľa právnych, zmluvných, Všeobecných podmienok alebo povinností Poskytovateľa, vrátane povinnosti vykonávať primeranú starostlivosť pri spoliehaní sa na TLS certifikáty;
**b)** neposkytnutia nevyhnutnej súčinnosti zo strany Odberateľa/Držiteľa;  
**c)** technických vlastností, konfigurácie, nekompatibility, neadekvátnosti alebo iných chýb v softvérových alebo hardvérových prostriedkoch nimi používaných;  
**d)** použitia alebo spoliehania sa na exspirovaný alebo zrušený TLS certifikát;  
**e)** použitia TLS certifikátu Odberateľom / Držiteľom TLS certifikátu v rozpore so zmluvou, Všeobecnými podmienkami alebo politikami Poskytovateľa;  
**f)** že TLS certifikát bol použitý v rozpore s jeho účelom alebo obmedzeniami uvedenými v TLS certifikáte, vo Všeobecných podmienkach alebo v CP;  
**g)** oneskorenia alebo nedoručenia žiadosti o stav certifikátu Poskytovateľovi z dôvodov, ktoré nie sú na strane Poskytovateľa (najmä v prípadoch nedostupnosti alebo preťaženia internetu alebo chýb v zariadeniach alebo technickom vybavení používanom overovateľom);  
**h)** neposkytnutia ktorejkoľvek z dôveryhodných služieb alebo ich nedostupnosti počas plánovanej údržby alebo reorganizácie oznámenej na webovom sídle Poskytovateľa;  
**i)** vyššej moci (Force Majeure).  

Poskytovateľ nezodpovedá za škody vzniknuté spoliehajúcej sa strane preto, že pri spoliehaní sa na TLS certifikát a dôveryhodné služby Poskytovateľa alebo spoliehaní sa na elektronický podpis alebo pečať vyhotovenú na ich základe nepostupovala podľa časti 10 Všeobecných podmienok [12] alebo podľa požiadaviek tejto politiky.  

## 9.9 Odškodnenie  
Každá osoba, ktorá poruší svoju povinnosť alebo akúkoľvek povinnosť podľa týchto CP/CPS, Zmluvy a Všeobecných podmienok, je povinná nahradiť škodu spôsobenú druhej strane, okrem prípadov, kedy je zodpovednosť subjektu za škody vylúčená. Za škodu sa považuje skutočná škoda, ušlý zisk a náklady vynaložené poškodenou stranou v súvislosti so škodovou udalosťou.  
Ktokoľvek, kto poruší svoju povinnosť alebo akúkoľvek povinnosť podľa týchto CP/CPS, Zmluvy a Všeobecných podmienok, môže byť zbavený zodpovednosti za škody len vtedy, ak preukáže, že k porušeniu povinnosti alebo akejkoľvek povinnosti došlo v dôsledku okolností vylučujúcich zodpovednosť, napr. vyššia moc (Force Majeure).  

## 9.10 Doba platnosti a ukončenie  

### 9.10.1 Doba platnosti  
Táto verzia CP/CPS je účinná od dátumu jej nadobudnutia účinnosti a platí až kým nebude nahradená novou verziou. Podrobnosti o histórii zmien týchto CP/CPS nájdete v časti „Revízia“ 1.2.1.  

### 9.10.2 Ukončenie  
Platnosť tejto verzie CP/CPS zanikne dňom zverejnenia novej vyššej verzie alebo ukončením poskytovania dôveryhodnej služby Poskytovateľom.   

### 9.10.3 Účinok ukončenia a pretrvanie  
V prípade, že tento dokument nebude nahradený novou verziou a jeho platnosť zanikne po skončení poskytovania dôveryhodnej služby Poskytovateľom, musia byť splnené všetky ustanovenia tejto CP týkajúce sa Poskytovateľa, ktoré je povinný dodržiavať po ukončení svojej činnosti (pozri časť 9).  

## 9.11 Individuálne oznámenia a komunikácia s účastníkmi  
Žiadne ustanovenia.  

## 9.12 Zmeny a doplnenia  

### 9.12.1 Postup pri zmenách a doplneniach  
Aktualizácia CP/CPS vychádza z jej preskúmania, ktoré sa vykonáva aspoň raz ročne od schválenia aktuálne platnej verzie. Preskúmanie vykoná oprávnená osoba Poskytovateľa, ktorá na základe výsledkov preskúmania pripraví písomný návrh prípadných navrhovaných zmien.

Schválenie navrhovaných zmien vykoná oprávnený člen PMA. Navrhované zmeny sa zvážia do 14 dní od ich doručenia. Po lehote na posúdenie návrhu zmeny musí PMA navrhovanú zmenu prijať, prijať s podmienkami alebo odmietnuť.

Chyby, žiadosti o aktualizáciu alebo navrhované zmeny CP/CPS sa oznamujú kontaktu uvedenému v 1.5.2. Takáto komunikácia musí obsahovať popis zmeny, dôvod zmeny a kontaktné údaje osoby žiadajúcej o zmenu alebo navrhujúcej zmenu.   

Všetky schválené zmeny CP/CPS sa oznámia dotknutým subjektom jeden týždeň pred ich nadobudnutím účinnosti prostredníctvom kanála na zverejňovanie a oznamovanie (pozri časť 2).  
Každá upravená verzia tejto CP/CPS musí byť očíslovaná a registrovaná, pričom novšia verzia musí mať vyššie číslo verzie ako tá, ktorú nahrádza.  
Opravy gramatických a štylistických chýb sa nepovažujú za zmeny vyvolávajúce zmenu verzie tejto CP/CPS.  

### 9.12.2 Mechanizmus a lehota oznamovania  
Poskytovateľ zverejní informácie o aktuálnej verzii CP/CPS prostredníctvom svojho webového sídla (pozri časť 1.5.2).   
Interní zamestnanci (personál RA) vydávajúci TLS certifikáty musia byť plne informovaní o novej verzii tejto CP/CPS.   

### 9.12.3 Okolnosti, za ktorých sa mení OID  
Každej politike musí byť Poskytovateľom priradené jej OID. OID tejto CP/CPS je uvedené v časti 1.2 a pre každú novú verziu CP/CPS zostáva nezmenené.  

## 9.13 Ustanovenia o riešení sporov  
Odberateľ / Držiteľ má právo zaslať Poskytovateľovi sťažnosť na poskytovanú dôveryhodnú službu e-mailom na radisig@disig.sk. 

Poskytovateľ vybaví sťažnosť najneskôr do 30 dní od jej prijatia, ak sa strany nedohodnú inak. Proces sťažnosti sa vzťahuje len na popis nedostatku, na ktorý Odberateľ poukazuje.  
Poskytovateľ musí odpovedať do 30 dní od prijatia sťažnosti. Poskytovateľ si vyhradzuje právo predĺžiť túto lehotu v prípade zložitejších sťažností.  

Súdy Slovenskej republiky majú výhradnú právomoc riešiť akékoľvek spory medzi Poskytovateľom a Odberateľom / Držiteľom TLS certifikátu. Ak je Odberateľ / Držiteľ spotrebiteľom, akýkoľvek spor môže byť riešený aj mimosúdne. V takom prípade je oprávnený obrátiť sa na orgán mimosúdneho riešenia sporov, Slovenskú obchodnú inšpekciu alebo inú právnickú osobu zapísanú v zozname podľa článku 5 ods. 2 zákona č. 391/2015 Z. z. o alternatívnom riešení spotrebiteľských sporov v znení neskorších predpisov. Pred podaním na súdne alebo mimosúdne riešenie sporov sú strany povinné pokúsiť sa vyriešiť tento spor najskôr vzájomnou dohodou.   

## 9.14 Rozhodné právo  
Právne vzťahy medzi Poskytovateľom a Odberateľom / Držiteľom TLS certifikátu sa riadia zákonmi Slovenskej republiky.   
Práva a povinnosti strán, ktoré nie sú upravené Všeobecnými podmienkami alebo Zmluvou, sa riadia najmä príslušnými ustanoveniami zákona č. 513/1991 Zb., Obchodný zákonník, v znení neskorších predpisov, zákona č. 40/1964 Zb., Občiansky zákonník v znení neskorších predpisov a inými všeobecne záväznými právnymi predpismi Slovenskej republiky.  

## 9.15 Súlad s platnými zákonmi  
Poskytovateľ poskytuje dôveryhodné služby v súlade s platnými právnymi predpismi účinnými v Slovenskej republike.  

## 9.16 Rôzne ustanovenia  

### 9.16.1 Celistvosť zmluvy  
Žiadne ustanovenia.  

### 9.16.2 Postúpenie  
Odberateľ / Držiteľ nesmie postúpiť, previesť alebo inak nakladať s právami, povinnosťami alebo nárokmi tretej strany podľa Zmluvy alebo Všeobecných podmienok bez písomného súhlasu Poskytovateľa.    

### 9.16.3 Oddeliteľnosť  
Ak sa akékoľvek ustanovenie tejto CP/CPS stane neplatným alebo nevymáhateľným, nespôsobuje to neplatnosť alebo nevymáhateľnosť celej CP/CPS, ak je úplne oddeliteľné od ostatných ustanovení tejto CP/CPS. Poskytovateľ okamžite nahradí neplatné alebo nevymáhateľné ustanovenie CP/CPS novým platným a vymáhateľným ustanovením, ktorého predmet bude čo najviac zodpovedať predmetu pôvodného ustanovenia a zároveň bude zachovaný účel tejto CP/CPS a obsah jednotlivých ustanovení tejto CP/CPS.  

### 9.16.4 Vymáhateľnosť  
V prípade, že určité právo nie je uplatnené počas trvania zmluvného vzťahu medzi stranami, toto právo nezaniká z dôvodu jeho neuplatnenia, ak nie je uvedené inak.
Z dôvodu zrušenia zmluvného vzťahu medzi zmluvnými stranami nie sú strany zbavené povinnosti splniť všetky záväzky vyplývajúce z doteraz uplatnených práv a vykonať všetky potrebné právne úkony, ktoré neznesú odklad a ktoré sú nevyhnutné na zabránenie škode.  

### 9.16.5 Vyššia moc (Force Majeure)  
Poskytovateľ, Odberateľ a Držiteľ nezodpovedajú za omeškanie plnenia svojich povinností v dôsledku okolností vylučujúcich zodpovednosť (Vyššia moc).   
Okolnosťou vylučujúcou zodpovednosť je prekážka, ktorá nastala nezávisle od vôle povinnej strany a bráni jej v splnení jej povinnosti, ak nemožno rozumne predpokladať, že povinná strana túto prekážku alebo jej následky odvráti alebo prekoná a že v čase vzniku prekážky mohla prekážku predvídať.   

Ak nastanú okolnosti vylučujúce zodpovednosť, potom strana, u ktorej takéto okolnosti nastanú, okamžite informuje druhú stranu o povahe, začiatku a konci takejto prekážky plnenia svojich povinností. Poskytovateľ, Odberateľ a Držiteľ sa zaväzujú urobiť maximum pre odvrátenie a prekonanie okolností vylučujúcich zodpovednosť.   

Zodpovednosť však nie je vylúčená, ak takáto okolnosť nastala až v čase, keď už bola povinná strana v omeškaní so splnením svojej povinnosti, alebo ak dotknutá strana nesplní svoju povinnosť okamžite informovať druhú stranu o povahe a začiatku trvania prekážky, alebo ak vznikla z hospodárskych pomerov. Účinky vylučujúce zodpovednosť sú obmedzené len na obdobie, počas ktorého trvá prekážka, s ktorou sú tieto účinky spojené.  

## 9.17 Ostatné ustanovenia  
Žiadne ustanovenia.

