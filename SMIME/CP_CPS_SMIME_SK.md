# Politika a pravidlá poskytovania dôveryhodnej služby vyhotovovania a overovania S/MIME certifikátov

 
 
**Disig, a.s.**  
**Verzia 2.1**  
**Platná od 21. 4. 2026**  
**OID 1.3.158.35975946.0.0.0.1.11**  

Copyright © 2026 Disig, a.s. 
Tento dokument je zverejnený pod licenciou [CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0/deed.sk).

Tento dokument neprešiel jazykovou korektúrou.
Ochranné známky: Názvy produktov uvedené v tomto dokumente môžu byť ochrannými známkami príslušných firiem.
   
 
# 1. Úvod

Tento dokument predstavuje kombinovaný dokument, ktorý zahŕňa politiku poskytovania dôveryhodných služieb a pravidlá poskytovania dôveryhodných služieb (ďalej aj „CP/CPS“) spoločnosti Disig, a.s., so sídlom Galvaniho 17/C, 821 04 Bratislava, IČO: 35975946, zapísanú v Obchodnom registri Mestského súdu Bratislava III, odd. Sa, vložka č. 3794/B, ako poskytovateľa dôveryhodných služieb (ďalej len „Poskytovateľ“) a platí pre koreňové certifikačné autority a k nim podriadené certifikačné autority uvedené v kapitole 1.4.1, prevádzkované Poskytovateľom, prostredníctvom ktorých poskytuje dôveryhodnú službu vyhotovovania verejne dôveryhodných S/MIME Certificates (ďalej len „Certifikát).  

Definuje:  
Politiku (CP) – politiky a pravidlá, podľa ktorých sú certifikáty vydávané, spravované a používané, a  
Pravidlá (CPS) – podrobné postupy a praktiky, ktoré Poskytovateľ implementuje.

Certifikát vydaný pre koncového používateľa (ďalej len „Odberateľ“ alebo „Držiteľ“ alebo „Odberateľ/Držiteľ“) jedinečným spôsobom identifikuje entitu, ktorej je certifikát vydaný, a viaže túto entitu k príslušnému páru kľúčov. Ak nie je v týchto CP/CPS výslovne uvedené, že sa vzťahujú na certifikát koreňovej certifikačnej autority alebo podriadenej certifikačnej autority, potom slovo „Certifikát“ znamená S/MIME certifikát koncovej entity.

Webové sídlo Poskytovateľa pre poskytované dôveryhodné služby je dostupné tu:
[https://eidas.disig.sk](https://eidas.disig.sk)

## 1.1 Prehľad

Tieto CP/CPS definujú vytváranie a správu certifikátov verejných kľúčov (X.509 verzia 3) v súlade s dokumentom „Baseline Requirements for the Issuance and Management of Publicly-Trusted S/MIME Certificates“ [1] (ďalej len „SMIME BR“).  
Zohľadňujú tiež požiadavky RFC 5280 „Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile“ [2], nariadenia (EÚ) č. 910/2014 z 23. júla 2014 o elektronickej identifikácii a dôveryhodných službách pre elektronické transakcie na vnútornom trhu a o zrušení smernice 1999/93/ES v znení nariadenia č. 1183/2025 (ďalej len „nariadenie eIDAS“) [3] a ETSI TS 119 411-6 „Electronic Signatures and Infrastructures (ESI); Policy and security requirements for Trust Service Providers issuing certificates; Part 6: Requirements for Trust Service Providers issuing publicly trusted S/MIME certificates“ [4]. Certifikáty sú vydávané v súlade s požiadavkami noriem ETSI EN 319 401 [5] a ETSI EN 319 411-1 [6].

Tieto CP/CPS sú štruktúrované v súlade s RFC 3647 [7].

Poskytovateľ potvrdzuje, že tieto CP/CPS zohľadňujú všetky požiadavky aktuálnej verzie SMIME BR [1], ktorá je zverejnená na adrese [https://cabforum.org/working-groups/smime/documents/](https://cabforum.org/working-groups/smime/documents/).

V prípade akéhokoľvek nesúladu medzi týmito požiadavkami a týmito CP/CPS majú prednosť požiadavky aktuálnej verzie SMIME BR [1].

## 1.2 Názov dokumentu a jeho identifikácia
 
| | |
|:--- | :--- |
|Názov:|**Politika a pravidlá poskytovania dôveryhodnej služby vyhotovovania a overovania S/MIME certifikátov** |
|Skratka názvu: | **SMIME CP/CPS** |
|Verzia:|  **2.1** |
|Schválené dňa:| **16. 4. 2026**   |
|Platnosť od:| **21. 4. 2026**    |  
|Tomuto dokumentu je priradený identifikátor objektu (OID):|**1.3.158.35975946.0.0.0.1.11** |  
 
 
Popis použitého identifikátora objektu (OID):    
 1\.  - ISO assigned OIDs  
 1.3.  ISO Identified Organization  
 1.3.158.  -  Identification number (Company ID - ICO)    
 1.3.158.35975946. - Disig, a. s.  
 1.3.158.35975946.0.0.0.1.  - CA Disig  
 1.3.158.35975946.0.0.0.1.11 - CA Disig S/MIME CP/CPS  
 
Tento OID (1.3.158.35975946.0.0.0.1.11) je zároveň uvádzaný aj vo vydávaných Certifikátoch a pokrýva tieto politiky zo štandardu [6]:
 
|Názov politiky|OID|Popis/ETSI štandard|  
|-----------|---|----------------------|
|LCP:  Lightweight Certificate Policy|0.4.0.2042.1.3|ETSI EN 319 411-1 LCP|
|OVCP: Organizational Validation  Certificate Policy|0.4.0.2042.1.7|ETSI EN 319 411-1 OVCP|
|NCP:  Normalized Certificate Policy|0.4.0.2042.1.1|ETSI EN 319 411-1 NCP|  
 
###  1.2.1 História zmien
 
|Verzia  |Dátum revízie|Popis revízie; Revidoval|  
|--------|-------------|------------------------|
|1.0     |01. 09. 2023|Prvá verzia dokumentu; Miškovič|  
|1.1     |01. 02. 2024|Doplnenie možnosti online zrušenia certifikátu (4.9.3); Miškovič|  
|1.2     |18. 07. 2024|Zmena sídla spoločnosti Disig, a.s.; Miškovič|  
|1.3     |16. 09. 2024|Doplnenie časti 4.2 v zmysle požiadaviek časti 2.2 aktuálnej verzie SMIME BR; Miškovič|  
|1.4     |15. 03. 2025|Úprava časti 4.2.2 a 4.2.3 v zmysle požiadaviek aktuálnej verzie SMIME BR v. 1,0.8; Miškovič|  
|2.0     |05. 03. 2026|Transformácia dokumentu na novú formu kombinovanej politiky pre poskytovanie služby vyhotovovanie verejne dôveryhodných S/MIME certifikátov, ktorá zahrňuje aj pravidlá pre poskytovanie tejto služby, ktoré boli pôvodne predmetom samostatného okumentu.|
|2.1     |21. 04. 2026|Pridanie novej single-purpose CA Disig SMIME Root R4 a jej podriadenej CA Disig R4I1 SMIME Certification Service (1.3.1.2);Miškovič|

## 1.3 Účastníci PKI

### 1.3.1 Certifikačné autority
Koreňová CA (Root CA) je najvyššia certifikačná autorita, ktorej koreňový certifikát je distribuovaný dodávateľmi aplikačného softvéru. Koreňová CA vydáva certifikáty podriadených CA.  
Podriadená CA (Subordinate CA) je certifikačná autorita, ktorej certifikát je podpísaný koreňovou CA alebo inou podriadenou CA.  
SMIME CP/CPS (ďalej len „CP/CPS“) sa vzťahuje na poskytovanie dôveryhodných služieb podriadenými certifikačnými autoritami, ktoré spadajú pod jednu z hierarchií CA prevádzkovaných Poskytovateľom na vydávanie verejne dôveryhodných certifikátov, ako je popísané nižšie.

####  1.3.1.1 Viacúčelová hierarchia CA

Táto hierarchia zahŕňa koreňovú CA a vydávajúcu podriadenú CA, ktorá predstavuje pôvodnú (legacy) štruktúru CA prevádzkovanú Poskytovateľom od jeho prijatia za poskytovateľa verejne dôveryhodných certifikátov v rámci príslušných programov koreňových autorít akceptovaných spoločnosťami Microsoft, Mozilla, Google a Apple.
Hierarchia sa bude používať na vydávanie Certifikátov koncovým používateľom iba dovtedy, kým nebude nahradená novou jednoúčelovou hierarchiou (pozri 1.3.1.2).


| | |
|:--- |:--- |
|Názov:|**CA Disig Root R2**|
|Sériové číslo certifikátu: |**0092B888DBB08AC163**|
|Odtlačok (sha1) (DER):|**B561EBEAA4DEE4254B691A98A55747C234C7D971**|
|Odtlačok (sha256) (DER):|**E23D4A036D7B70E9F595B1422079D2B91EDFBB1FB651A0633EAA8A9DC5F80703**|
|Poznámka:|**Vydáva certifikáty len pre podriadené certifikačné autority Poskytovateľa.**|  

   


| | |
|:--- |:--- |
|Názov:|**CA Disig R2I5 Certification Service**|
|Sériové číslo certifikátu: |**081B06DF4C7965509D000000000000000E**|
|Vydavateľ:|**CA Disig Root R2**|
|Odtlačok (sha1) (DER):|**8A189E4E6222B3B16D98EABE88687B39F82827A4**|
|Odtlačok (sha256) (DER):|**90BA720B376FB9FDCF8A1037A5316FB493B5ACF656AD79C6839008BD43343FDD**|
|Poznámka:|**Vydáva koncovým používateľom SMIME certifikáty podpisu/pečate  v súlade s požiadavkami stanovenými v dokumente „Baseline Requirements for the Issuance and Management of Publicly‐Trusted S/MIME Certificates [1]“.**|


####  1.3.1.2 Single-purpose SMIME CA

Táto hierarchia certifikačných autorít (CA) nahrádza staršiu hierarchiu CA (pozri 1.3.1.1), ktorá sa v súčasnosti používa na vydávanie certifikátov koncovým používateľom. Táto jednoúčelová hierarchia SMIME CA je teraz plne v súlade s požiadavkami aktuálnej verzie SMIME BR [1], kde sa od nových koreňových certifikačných autorít vyžaduje samostatná hierarchia CA na vydávanie certifikátov koncovým používateľom a sú obmedzené na vydávanie certifikátov obsahujúcich iba rozšírenie id-kp-emailProtection (OID: 1.3.6.1.5.5.7.3.4) v EKU.

|  | |
| :--- | :--- |
| Názov:                    |**CA Disig SMIME Root R4** |
| Sériové číslo certifikátu:|**3F0CFAFD63A38C10294A0579F5457825**|
| Odtlačok (sha1)(DER):     |**33F3820A9838680BF90DA57815019E9FFDF31718** |
| Odtlačok (sha256)(DER):   |**6AF177B41E97D40C9EA25203533E55C408632E9BD8A4809551001DFF2DC9479B**   |
| Platný od:                |**18. 09, 2025**|
| Platný do:                |**14. 09. 2043**| 
| Poznámka:                 |**Vydáva certifikáty len pre podriadené certifikačné autority Poskytovateľa vyhradené pre SMIME certifikáty.**    |  

   
|  | |
| :--- | :--- |
| Názov:                    |**CA Disig R4I1 SMIME Certification Service** |
| Vydavateľ:                |**CA Disig SMIME Root R4**|
| Sériové číslo certifikátu:|**0AC7948B6549813D0E0000000000000001**|
| Odtlačok (sha1)(DER):     |**41253D3546812F46FAA7DC97933373E241134F61**|
| Odtlačok (sha256)(DER):   |**855998FAB845C2C1CF0D6F62852C6B9A3C659DFDFA434D405C134C240E4534B5**|
| Platný od:                |**13. 04. 2026**|
| Platný do:                |**11. 04. 2033**| 
| Poznámka:                 |**Vydáva SMIME certifikáty iba koncovým používateľom (pozri 3.1.4.3).**| 


### 1.3.2 Registračné autority

Registračná autorita („RA“) je subjekt, ktorý na základe zmluvy vykonáva určité vybrané činnosti pri poskytovaní dôveryhodných služieb v mene Poskytovateľa.
RA vykonáva svoje činnosti v súlade s týmito schválenými CP/CPS.
Poskytovateľ môže zriadiť nasledujúce typy RA:
* Komerčná RA – je určená na sprostredkovanie vybraných dôveryhodných služieb Poskytovateľa širokej verejnosti a je prevádzkovaná treťou stranou na základe písomnej zmluvy s Poskytovateľom, pozri zoznam na [https://eidas.disig.sk/sk/kontakt/registracne-autority/](https://eidas.disig.sk/sk/kontakt/registracne-autority/);
* Enterprise RA – je určená na sprostredkovanie vybraných dôveryhodných služieb výlučne pre vlastné potreby konkrétnej právnickej osoby, pre potreby ňou prevádzkovaných systémov vyžadujúcich použitie certifikátov, a je prevádzkovaná na základe písomnej zmluvy s Poskytovateľom;
* Interná RA – je prevádzkovaná Poskytovateľom a je určená na poskytovanie dôveryhodných služieb pre všetkých záujemcov. Táto RA nie je samostatným právnym subjektom.
Ak sa v texte používa pojem „RA Poskytovateľa“, vzťahuje sa na všetky vyššie uvedené typy RA.

#### 1.3.2.1 Enterprise RA

Poskytovateľ môže delegovať na Enterprise RA overovanie žiadostí o certifikát pre fyzické osoby v rámci ich vlastnej organizácie. Poskytovateľ neprijme žiadosti o certifikát autorizované Enterprise RA, pokiaľ nie sú splnené nasledujúce požiadavky:
* Ak je žiadosť o certifikát pre profil „Organization-validated“ alebo „Sponsor-validated“, Poskytovateľ potvrdí, že Enterprise RA má oprávnenie alebo kontrolu nad požadovanou e-mailovou doménou (doménami) v súlade s časťou 3.2.2.1 alebo časťou 3.2.2.3.
* Poskytovateľ potvrdí, že názov v poli „_subject:organizationName_“ je buď názov delegovaného podniku, alebo pridruženej spoločnosti (Affiliate) delegovaného podniku, alebo že delegovaný podnik je zástupcom menovaného Subjektu. Poskytovateľ uloží tieto obmedzenia ako zmluvnú požiadavku pre Enterprise RA a monitoruje dodržiavanie zo strany Enterprise RA v súlade s časťou 8.8.

### 1.3.3 Odberatelia

Pod Odberateľom sa rozumie fyzická osoba alebo právnická osoba, ktorá je oprávnená požiadať o certifikát v mene entity, ktorej meno sa uvádza ako predmet (subject) v certifikáte – držiteľ certifikátu.
Držiteľom certifikátu môže byť:
* **Fyzická osoba** – žiada o certifikát;
* **Fyzická osoba** identifikovaná v **spojení s právnickou osobou** – žiada o certifikát;
* **Právnická osoba** (ktorou môže byť organizácia alebo jednotka, alebo oddelenie identifikované v spojení s organizáciou) – žiada o certifikát pre pečať.

Ak je odberateľ zároveň subjektom, nesie výhradnú zodpovednosť za nesprávne splnenie svojich povinností.
Ak odberateľ koná v mene jedného alebo viacerých odlišných subjektov, s ktorými je prepojený (napr. Odberateľom je spoločnosť vyžadujúca certifikáty pre svojich zamestnancov, aby im umožnila podieľať sa na elektronickom obchode v mene spoločnosti), zodpovednosti odberateľa a subjektu sú upravené vo „Všeobecných podmienkach poskytovania a používania dôveryhodnej služby vydávania a overovania certifikátov“ („Všeobecné podmienky“) [8] zverejnených na webovom sídle Poskytovateľa (pozri kapitolu 1).

Tieto CP/CPS definujú požiadavky, ktoré musí Odberateľ/Držiteľ spĺňať.
Formálnym držiteľom certifikátu sa rozumie fyzická osoba, ktorá sa zaväzuje používať príslušný súkromný kľúč a certifikát v súlade s týmito CP/CPS.
Prepojenie medzi odberateľom a subjektom je jedno z nasledujúcich:
* Pri žiadosti o certifikát je odberateľom:
   * samotná fyzická osoba;
   * právnická osoba poverená zastupovaním subjektu; alebo
   * akýkoľvek subjekt, s ktorým je fyzická osoba spojená (napríklad spoločnosť zamestnávajúca fyzickú osobu alebo nezisková právnická osoba, ktorej je fyzická osoba členom).
* Pri žiadosti o certifikát pre pečať je odberateľom:
   * akýkoľvek subjekt, ktorému príslušný právny systém umožňuje zastupovať právnickú osobu; alebo
   * štatutárny zástupca právnickej osoby objednávajúci certifikáty pre svoje dcérske spoločnosti, jednotky alebo oddelenia.

### 1.3.4 Spoliehajúce sa strany
Spoliehajúce sa strany sú fyzické alebo právnické osoby, ktoré sa vo svojom konaní spoliehajú na elektronickú identifikáciu alebo dôveryhodné služby Poskytovateľa.

### 1.3.5 Ostatní účastníci

#### 1.3.5.1 Orgán pre správu politík (Policy Management Authority)
Orgán pre správu politík – PMA je zložka určená na účely:
* Dohľadu nad tvorbou a aktualizáciou CP/CPS vrátane vyhodnocovania plánov na implementáciu akýchkoľvek zmien.
* Preskúmavania CP/CPS s cieľom zabezpečiť, aby postupy Poskytovateľa boli v súlade s ich požiadavkami.
* Preskúmavania zistení z auditov s cieľom určiť, či Poskytovateľ primerane dodržiava schválené CP/CPS.
* Poskytovania odporúčaní pre Poskytovateľa týkajúcich sa nápravných opatrení a iných vhodných opatrení.
* Poskytovania poradenstva ohľadom vhodnosti certifikátov spojených s CP/CPS pre konkrétne riadiace aplikácie a riadenia činností certifikačnej autority a registračnej autority.
* Interpretácie CP/CPS a pokynov z nich vyplývajúcich pre RA a CA.
* Vykonávania interného auditu Poskytovateľa priradením tejto úlohy nezávislému zamestnancovi.
* Zabezpečenia, aby prijaté a schválené CP/CPS boli riadne a náležite implementované.

PMA predstavuje najvyššiu zložku, ktorá s konečnou platnosťou rozhoduje o všetkých záležitostiach a aspektoch súvisiacich s Poskytovateľom a jeho činnosťami.

#### 1.3.5.2 Posudzovatelia zhody (audítori)
Posudzovatelia zhody sú nezávislé organizácie, ktoré na základe akreditácie posudzujú súlad Poskytovateľa s:
* príslušnými normami (napr. ETSI EN 319 401 [5], ETSI EN 319 411-1 [6] alebo inými príslušnými normami),
* týmito CP/CPS a súvisiacimi internými politikami Poskytovateľa,
* požiadavkami programov Trusted Root CA a/alebo CCADB.
Posudzovatelia zhody:
* majú právo vyžiadať si od Poskytovateľa prístup k potrebným dokumentom, záznamom a systémom v rozsahu potrebnom na vykonanie auditu;
* sú viazaní povinnosťou mlčanlivosti v rozsahu dohodnutom v zmluve s Poskytovateľom a v súlade s platnými právnymi predpismi;
* neposkytujú žiadne služby vydávania certifikátov, správu kľúčov ani funkcie CA/RA.

Poskytovateľ zabezpečí, aby vzťahy s posudzovateľmi zhody boli upravené písomnou zmluvou a aby nedochádzalo k žiadnemu konfliktu záujmov.

#### 1.3.5.3 Dozorné orgány a prevádzkovatelia dôveryhodných koreňových programov
Dozorné orgány a prevádzkovatelia dôveryhodných koreňových programov sú subjekty, ktoré vykonávajú zákonný alebo programový dohľad nad činnosťami Poskytovateľa, napríklad:
* národný dozorný orgán pre dôveryhodné služby alebo elektronickú identifikáciu;
* prevádzkovatelia programov dôveryhodných koreňových CA (napr. výrobcovia prehliadačov a operačných systémov), ktorí rozhodujú o zaradení/odstránení koreňových CA do príslušného programu;
* správcovia a prevádzkovatelia CCADB.
Tieto subjekty:
* môžu od Poskytovateľa vyžadovať informácie, dokumenty a vysvetlenia týkajúce sa prevádzky CA a dodržiavania požiadaviek;
* môžu vyžadovať prijatie nápravných opatrení, obmedzení alebo ukončenie vydávania certifikátov;
* nie sú zmluvnou stranou ani spoliehajúcou sa stranou, ale môžu ovplyvniť dôveryhodnosť vydaných certifikátov (napr. odstránením koreňovej CA z programu).

Poskytovateľ spolupracuje s týmito subjektmi v rozsahu vyžadovanom platnými právnymi predpismi, platnými pravidlami programov a týmito CP/CPS.

### 1.4 Používanie certifikátu

### 1.4.1 Povolené spôsoby použitia certifikátu
Certifikáty vydávané podľa týchto CP/CPS sa vydávajú na účely identifikácie držiteľa verejného kľúča z páru kryptografických kľúčov (verejný a súkromný), ktorý sa používa v rámci infraštruktúry PKI.
Kryptografický pár kľúčov (súkromný a verejný) a certifikát vydaný Poskytovateľom sa vo všeobecnosti môžu používať predovšetkým na:
* zabezpečenie e-mailu (podpisovanie a/alebo šifrovanie e-mailov);
* podpisovanie elektronických dokumentov zdokonaleným elektronickým podpisom;
* vytváranie elektronickej pečate.

CA Poskytovateľa vydávajú Odberateľom nasledujúce typy certifikátov:
* S/MIME certifikát pre digitálny podpis alebo S/MIME digitálny certifikát pre pečať – obsahujú verejný kľúč spojený s e-mailovou adresou a môžu obsahovať aj identitu fyzickej osoby alebo právnickej osoby, ktorá má kontrolu nad požadovanou e-mailovou adresou. Kryptografické kľúče spojené s týmto typom certifikátu sú primárne určené na zabezpečenie elektronickej pošty a vytváranie zdokonaleného elektronického podpisu.
Vydaný certifikát bude v súlade so SMIME BR [1] obsahovať nasledujúce identifikátory certifikačných politík:
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) organization-validated(2) multipurpose (2)} (2.23.140.1.5.2.2);
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) organization-validated (2) strict (3)} (2.23.140.1.5.2.3);
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) sponsor-validated (3) multipurpose (2)} (2.23.140.1.5.3.2); a
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) sponsor-validated (3) strict (3)} (2.23.140.1.5.3.3); a
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) individual-validated (4) multipurpose (2)} (2.23.140.1.5.4.2); a
   * {joint-iso-itu-t(2) international-organizations(23) ca-browser-forum(140) certificate-policies(1) smime-baseline(5) individual-validated (4) strict (3)} (2.23.140.1.5.4.3).

Poskytovateľ vydáva manažérske certifikáty pre svoje potreby (certifikát pre podriadenú CA a certifikát pre OCSP respondery).

### 1.4.2 Zakázané spôsoby použitia certifikátu
Certifikáty vydávané podľa týchto CP/CPS nie sú kvalifikovanými certifikátmi EÚ podľa nariadenia eIDAS [3] a nemôžu sa používať tam, kde sa vyžadujú kvalifikované certifikáty EÚ.
Certifikáty vydávané podľa týchto CP/CPS sa nesmú používať na:
* zabezpečenie TLS komunikácie;
* podpisovanie kódu (code signing);
* vydávanie ďalších certifikátov (certifikáty iné ako pre CA);
* akékoľvek použitie, ktoré nie je v súlade s rozšíreniami Key Usage a EKU;
* akékoľvek použitie, ktoré je nezákonné, v rozpore s platnými právnymi predpismi alebo v rozpore s týmito CP/CPS alebo zmluvou o dôveryhodnej službe.

Spoliehajúce sa strany by sa nemali spoliehať na certifikáty na iné účely, pokiaľ takéto použitie nie je výslovne povolené príslušnou politikou certifikátov a jasne uvedené v rozšíreniach certifikátu.

### 1.5 Správa politiky

### 1.5.1 Organizácia spravujúca dokument
Tabuľka 1 obsahuje údaje o Poskytovateľovi, ktorý je zodpovedný za prípravu, tvorbu a údržbu tohto dokumentu.

Tabuľka 1: Kontaktné údaje Poskytovateľa
| | |
| :--- | :--- |
| Spoločnosť: | **Disig, a. s.** |
| Adresa: | **Galvaniho 17/C, 821 04 Bratislava, Slovensko** |
| IČO: | **359 75 946** |
| Telefón: | **+421 2 20850140** |
| e-mail: | **<disig@disig.sk>** |
| Webové sídlo: | **[https://www.disig.sk](https://www.disig.sk)** |

### 1.5.2 Kontaktná osoba
Pre tvorbu politík má Poskytovateľ PMA, ktorý je plne zodpovedný za ich obsah a je pripravený odpovedať na akékoľvek otázky týkajúce sa politík Poskytovateľa (pozri 1.3.5).
Tabuľka 2 obsahuje kontaktné údaje osoby zodpovednej za prevádzku certifikačných autorít Poskytovateľa.

Tabuľka 2: Kontaktné údaje certifikačnej autority
| | |
| :--- | :--- |
| Certifikačná autorita: | **CA Disig** |
| Adresa: | **Galvaniho 17/C, 821 04 Bratislava, Slovensko** |
| Telefón: | **+421 2 20850150, +421 2 20820157** |
| e-mail: | **<caoperator@disig.sk>** |
| Webové sídlo: | **[https://eidas.disig.sk](https://eidas.disig.sk)** |

### 1.5.3 Osoba určujúca vhodnosť CP/CPS pre politiku
Osobou zodpovednou za rozhodovanie o súlade postupov Poskytovateľa s týmito CP/CPS je PMA (pozri 1.3.5).

### 1.5.4 Postupy schvaľovania CPS
Ešte pred začatím prevádzky by mal mať Poskytovateľ schválené svoje CP/CPS a musí spĺňať všetky ich požiadavky.
Osoba menovaná PMA schvaľuje obsah CP/CPS.
Po schválení PMA je príslušný dokument zverejnený v súlade s politikou zverejňovania a oznamovania.
PMA musí oznamovať svoje rozhodnutia takým spôsobom, aby tieto informácie boli dobre prístupné spoliehajúcim sa stranám.

Tieto CP/CPS sú schválené osobou menovanou do roly PMA.
CP/CPS sú zverejnené v súlade s politikou zverejňovania a oznamovania na webovom sídle Poskytovateľa (pozri časť 1).

### 1.6 Definície a skratky

### 1.6.1 Definície
**Zdokonalená elektronická pečať** znamená elektronickú pečať, ktorá spĺňa požiadavky stanovené v článku 36 nariadenia eIDAS [3];

**Zdokonalený elektronický podpis** znamená elektronický podpis, ktorý spĺňa požiadavky stanovené v článku 26 nariadenia eIDAS [3];

**CA Poskytovateľa** – certifikačné autority Poskytovateľa, ktoré sa používajú na vydávanie certifikátov;

**Dôveryhodná služba** znamená elektronickú službu bežne poskytovanú za odplatu, ktorá pozostáva z:
   **a)** vyhotovovania, overovania a potvrdzovania elektronických podpisov, elektronických pečatí alebo elektronických časových pečiatok, služieb elektronického doporučeného doručovania a certifikátov súvisiacich s týmito službami, alebo
   **b)** vyhotovovania, overovania a potvrdzovania certifikátov na autentifikáciu webových sídiel; alebo
   **c)** uchovávania elektronických podpisov, pečatí alebo certifikátov súvisiacich s týmito službami;

**Držiteľ certifikátu** znamená subjekt identifikovaný v certifikáte ako držiteľ súkromného kľúča patriaceho k verejnému kľúču obsiahnutému v certifikáte;

**Certifikát na autentifikáciu webových sídiel** znamená potvrdenie, ktoré umožňuje autentifikovať webové sídlo a spája webové sídlo s fyzickou alebo právnickou osobou, ktorej je certifikát vydaný;

**Zmluvný partner** znamená právnickú osobu, s ktorou spoločnosť Disig uzatvorila písomnú zmluvu o poskytovaní dôveryhodných služieb;

**Elektronický podpis** znamená údaje v elektronickej forme, ktoré sú pripojené alebo logicky spojené s inými údajmi v elektronickej forme a ktoré používa podpisovateľ na podpisovanie;

**Elektronická pečať** znamená údaje v elektronickej forme, ktoré sú pripojené alebo logicky spojené s inými údajmi v elektronickej forme s cieľom zabezpečiť pôvod a integritu týchto údajov;

**Pár kľúčov** znamená súčasť systému PKI, ktorý využíva asymetrickú kryptografiu a pozostáva z verejného kľúča a súkromného kľúča;

**Viacúčelová CA (Multi-purpose CA)** – koreňová CA alebo podriadená CA, ktorá je v hierarchii bez obmedzení na typ certifikátu vydávaného koncovému držiteľovi, t. j. v hierarchii je možné vydávať certifikáty, TLS certifikáty alebo iné typy certifikátov koncovým používateľom;

**PKCS#10** znamená formát správ odosielaných certifikačnej autorite so žiadosťou o certifikáciu verejného kľúča;

**PEM** znamená formát súboru na ukladanie a odosielanie kryptografických kľúčov, certifikátov a iných údajov, ako je formalizovaný organizáciou IETF v RFC 746;

**Pracovník RA** znamená zamestnanca Poskytovateľa alebo inej právnickej osoby, ktorá má s Poskytovateľom uzavretú zmluvu o poskytovaní certifikačných služieb;

**RA Poskytovateľa** – pojem, ktorý zahŕňa všetky typy RA (komerčnú, enterprise, internú);

**Spoliehajúca sa strana** znamená fyzickú alebo právnickú osobu, ktorá sa spolieha na elektronickú identifikáciu alebo dôveryhodnú službu;

**S/MIME certifikát** – obsahuje verejný kľúč viazaný na e-mailovú adresu (Mailbox Address) a môže obsahovať aj identitu fyzickej osoby alebo právnickej osoby, ktorá má pod kontrolou túto e-mailovú adresu.

**Profil S/MIME STRICT** – profily pre S/MIME certifikáty s rozšírením „extKeyUsage“ obmedzeným na „_id-kp-emailProtection_“ a prísnejším používaním atribútov Subject DN a iných rozšírení;

**Profil S/MIME MULTIPURPOSE** – profily sú zosúladené s definovanejšími Strict profilmi, ale s ďalšími možnosťami pre extKeyUsage a iné rozšírenia. Účelom je umožniť flexibilitu pre prípady použitia na rozhraní medzi podpisovaním dokumentov a bezpečným e-mailom.

**Verejne dôveryhodný certifikát (Publicly-Trusted Certificate)** znamená certifikát, ktorý je dôveryhodný vďaka skutočnosti, že jeho zodpovedajúci koreňový certifikát je distribuovaný ako kotva dôvery (trust anchor) v bežne dostupnom aplikačnom softvéri.

**Jednoúčelová CA (Single-purpose CA)** – koreňová CA alebo podriadená CA, ktorá je v hierarchii prísne obmedzená na vydávanie práve jedného typu certifikátu koncovému používateľovi, t. j. v hierarchii môžu byť koncovému používateľovi vydávané iba S/MIME certifikáty;

**Odberateľ** znamená fyzickú osobu alebo právnickú osobu, ktorej je certifikát vydaný a ktorá je právne viazaná zmluvou s odberateľom alebo podmienkami používania.

**Poskytovateľ dôveryhodných služieb** znamená fyzickú alebo právnickú osobu, ktorá poskytuje jednu alebo viacero dôveryhodných služieb buď ako kvalifikovaný

###  1.6.2	Skratky 

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

###  1.6.3	Referencie 
**[1]**   Baseline Requirements for the Issuance and Management of Publicly-Trusted S/MIME Certificates [https://cabforum.org/working-groups/smime/documents/](https://cabforum.org/working-groups/smime/documents/)      
**[2]**   RFC 5280 "Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile"    
**[3]**   Regulation (EU) No 910/2014 of the European Parliament and of the Council of 23 July 2014 on electronic identification and trust services for electronic transactions in the internal market in the wording of Regulation (EU) No1183/2024 of the European.  
**[4]**   ETSI TS 119 411-6 "Electronic Signatures and Infrastructures (ESI); Policy and security requirements for Trust Service Providers issuing certificates; Part 6: Requirements for Trust Service Providers issuing publicly trusted S/MIME certificates."  
**[5]**   ETSI EN 319 401 "Electronic Signatures and Infrastructures (ESI); General Policy Requirements for Trust Service Providers."   
**[6]**   ETSI EN 319411-1 "Electronic Signatures and Infrastructures (ESI); Policy and security requirements for Trust Service Providers issuing certificates; Part 1: General requirements."   
**[7]**   RFC 3647  "Request for Comments: 3647, Internet X.509 Public Key Infrastructure: Certificate Policy and Certification Practices Framework"   
**[8]**   Všeobecné podmienky poskytovania a používania dôveryhodnej služby vyhotovovania a overovania certifikátov Disig, a.s. [https://eidas.disig.sk/pdf/vp_tsp_disig.pdf](https://eidas.disig.sk/pdf/vp_tsp_disig.pdf)         
**[9]**   X.500 "Information technology - Open Systems Interconnection - The Directory: Overview of concepts, models and services", 10/2012, ITU-T.  
**[10]**  X.501 "Information technology - Open Systems Interconnection - The Directory: Models.", 10/2012,  ITU-T.  
**[11]**  X.520 "Information technology - Open Systems Interconnection - The Directory: Selected attribute types", 10/2016, ITU-T.     
**[12]**  RFC 5322 "Internet Message Format".   
**[13]**  Baseline Requirements for the Issuance and Management of Publicly-Trusted TLS certificates [https://cabforum.org/baseline-requirements-documents/](https://cabforum.org/baseline-requirements-documents/).  
**[14]**  Informácia o spracúvaní osobných údajov, Disig, a.s. [https://eidas.disig.sk/pdf/info_oou_gdpr.pdf](https://eidas.disig.sk/pdf/info_oou_gdpr.pdf)   
**[15]**  RFC 9495 "Certification Authority Authorization (CAA) Processing for Email Addresses."    
**[16]**  RFC 6960 "X.509 Internet Public Key Infrastructure Online Certificate Status Protocol - OCSP".   
**[17]**  RFC 5019 "The Lightweight Online Certificate Status Protocol (OCSP) Profile."   
**[18]**  NIST 800-89 "Recommendation for Obtaining Assurances for Digital Signature Applications."   
**[19]**  Network and Certificate System Security Requirements [https://cabforum.org/working-groups/netsec/documents/](https://cabforum.org/working-groups/netsec/documents/)   
**[20]**  RFC 6818 "Updates to the Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile"   
**[21]**  ETSI EN 319 412-1 "Electronic Signatures and Infrastructures (ESI);Certificate Profiles; Part 1: Overview and common data structures."     
**[22]**  ISO 3166-1 "Codes for the representation of names of countries and their subdivisions - Part 1: Country code."   

### 1.6.4 Konvencie
Kľúčové slová „MUSÍ“, „NESMIE“, „POVINNÉ“, „MAL BY“, „NEMALO BY“, „ODPORÚČANÉ“, „MÔŽE“ a „VOLITEĽNÉ“ v týchto CP/CPS sa musia interpretovať v súlade s RFC 2119.

# 2. ZODPOVEDNOSŤ ZA ZVEREJŇOVANIE A ÚLOŽISKO
Poskytovateľ vytvorí, implementuje, presadzuje a aktualizuje (aspoň raz ročne) svoje CP/CPS podrobne opisujúce spôsob implementácie legislatívnych požiadaviek a požiadaviek príslušného dokumentu.

## 2.1 Úložiská
Úložiská musia byť umiestnené tak, aby boli prístupné Držiteľom certifikátov a Spoliehajúcim sa stranám a boli v súlade s celkovými bezpečnostnými požiadavkami.
Webové sídlo Poskytovateľa je verejne prístupné prostredníctvom internetu Odberateľom, Držiteľom certifikátov, Spoliehajúcim sa stranám a širokej verejnosti.

Poskytovateľ prevádzkuje jedno verejne prístupné úložisko (pozri časť 1), ktoré poskytuje aktuálne informácie relevantné pre tieto CP/CPS, vrátane:
* týchto CP/CPS a ich predchádzajúcich verzií;
* platných všeobecných obchodných podmienok pre poskytovanie dôveryhodných služieb;
* certifikátov CA a ich odtlačkov (fingerprints);
* zoznamov zrušených certifikátov (CRL).

Verejne prístupné informácie publikované v úložisku Poskytovateľa podliehajú riadeným kontrolám prístupu.

## 2.2 Zverejňovanie informácií
Poskytovateľ poskytne online úložisko prístupné Odberateľom, Držiteľom certifikátov a Spoliehajúcim sa stranám v režime 24x7, ktoré obsahuje aspoň nasledujúce informácie:
* certifikáty vydané v súlade s týmito CP/CPS;
* aktuálny zoznam CRL, ako aj všetky zoznamy CRL vydané od začiatku operácií vydávania certifikátov;
* certifikáty koreňových CA a podriadených CA zodpovedajúce verejným kľúčom, ktorých prislúchajúce súkromné kľúče sa používajú na podpisovanie vydaných certifikátov a zoznamov CRL;
* aktuálnu verziu CP/CPS;
* informácie o výsledkoch pravidelných auditov výkonu poskytovaných dôveryhodných služieb.

Poskytovateľ nie je povinný zverejňovať informácie o vydaných certifikátoch v prípadoch, keď sú takéto certifikáty vydané pre interné potreby zmluvných partnerov a nezverejnenie bolo so zmluvným partnerom dohodnuté.

Poskytovateľ potvrdzuje, že tieto CP/CPS odrážajú všetky požiadavky aktuálnej verzie SMIME BR [1], zverejnenej na [https://cabforum.org/smime-br/](https://cabforum.org/smime-br/).

V prípade akýchkoľvek rozporov medzi týmito požiadavkami a týmito CP/CPS majú prednosť požiadavky aktuálnej verzie SMIME BR [1].

### 2.2.1 Politiky a vyhlásenia o praktikách
Aktuálne a predchádzajúce verzie CP a CPS alebo kombinovaných CP/CPS sú zverejnené na:
[https://eidas.disig.sk/en/provider/policies-and-documents/](https://eidas.disig.sk/en/provider/policies-and-documents/) – EN/SK verzie
[https://eidas.disig.sk/sk/poskytovatel/politiky-a-dokumenty/](https://eidas.disig.sk/sk/poskytovatel/politiky-a-dokumenty/) – SK verzie

### 2.2.2 Certifikáty CA
Certifikáty verejných kľúčov pre koreňové CA, podriadené CA (vydávajúce CA) a akékoľvek príslušné krížové certifikáty (Cross-Certificates) sú zverejnené na:

[https://eidas.disig.sk/en/certificates/ca/](https://eidas.disig.sk/en/certificates/ca/) – EN verzia
[https://eidas.disig.sk/sk/poskytovatel/certifikacna-autorita/certifikaty-ca/](https://eidas.disig.sk/sk/poskytovatel/certifikacna-autorita/certifikaty-ca/) – SK verzia

### 2.2.3 Zoznamy zrušených certifikátov (CRL)
Poskytovateľ zverejňuje CRL na nasledujúcich HTTP URL adresách, aby sa predišlo cyklickým závislostiam počas validácie:

| CA | Bod distribúcie CRL (CRL distribution point) |
| :--- | :--- |
| CA Disig Root R2 | [http://cdp1.disig.sk/rootcar2/crl/rootcar2.crl](https://cdp1.disig.sk/rootcar2/crl/rootcar2.crl)|<br>[http://cdp2.disig.sk/rootcar2/crl/rootcar2.crl](http://cdp2.disig.sk/rootcar2/crl/rootcar2.crl)|
| CA Disig R2I5 Certification Service | [http://cdp.disig.sk/subcar2i5/crl/subcar2i5.crl](https://cdp.disig.sk/subcar2i5/crl/subcar2i5.crl)|
| CA Disig SMIME Root R4 | [http://cdp.disig.sk/rootcar4/crl/rootcar4.crl](https://cdp.disig.sk/rootcar4/crl/rootcar4.crl)|
| CA Disig R4I1 SMIME Certification Service | [http://cdp.disig.sk/subcar4i1/crl/subcar4i1.crl](https://cdp.disig.sk/subcar4i1/crl/subcar4i1.crl)|

## 2.3 Čas alebo periodicita zverejňovania
Certifikát musí byť zverejnený čo najskôr po jeho vydaní. Informácie o vydanom certifikáte musia byť dostupné na webovom sídle Poskytovateľa (pozri časť 1). Certifikáty vydané pre uzavreté systémy alebo pre interné účely Poskytovateľa nemusia byť verejne dostupné.

Certifikát je zverejnený ihneď po vydaní a Odberateľ/Držiteľ si ho môže okamžite vyzdvihnúť. Informácie o vydaní certifikátu sú dostupné v úložisku Poskytovateľa (pozri časť 2.1).
Zoznam CRL sa zverejňuje podľa špecifikácie v časti 4.9.7. Informácie o zrušenom certifikáte musia byť dostupné na webovom sídle Poskytovateľa (pozri časť 1), ktoré slúži ako jeho úložisko.

Všetky informácie, ktoré sa vyžadujú zverejniť v úložisku, sa zverejnia, ak je to možné, čo najskôr.
Zoznam CRL sa zverejňuje podľa špecifikácie v časti 4.9.8. Informácie o zrušenom certifikáte možno nájsť v úložisku Poskytovateľa.

## 2.4 Kontroly prístupu k úložiskám
Poskytovateľ chráni všetky informácie uložené v úložisku, ktoré nie sú určené na verejné šírenie. Poskytovateľ vynaloží maximálne úsilie na zabezpečenie integrity, dôvernosti a dostupnosti údajov súvisiacich s poskytovaním dôveryhodných služieb. Poskytovateľ tiež implementuje logické a bezpečnostné opatrenia na zabránenie neoprávnenému prístupu k úložisku osobám, ktoré by mohli akýmkoľvek spôsobom upravovať, poškodzovať, pridávať alebo mazať údaje uložené v úložisku.
Prostredníctvom technických a prijatých organizačných opatrení Poskytovateľ chráni všetky informácie uložené v úložisku, ktoré nie sú určené na verejné šírenie. Na tento účel zaviedol presné pravidlá zahrnuté v bezpečnostnom projekte Poskytovateľa a súvisiacich interných politikách.

Verejne prístupné informácie publikované v úložisku Poskytovateľa podliehajú riadeným kontrolám prístupu.

# 3.  IDENTIFIKÁCIA A AUTENTIFIKÁCIA

## 3.1 Pomenovanie (Naming)

### 3.1.1 Typy mien
Každá CA musí byť schopná vytvárať certifikáty, ktoré obsahujú rozlišovacie mená (Distinguished Names) v zmysle X.500 (ďalej len „rozlišovacie meno“) [9] – konkrétne v súlade s X.501 [10] a X.520 [11] a mená v zmysle RFC 5322 (Internet Message Format) [12].  
Odberatelia si musia sami zvoliť rozlišovacie meno, ktoré má byť zahrnuté v ich certifikáte.

### 3.1.2 Potreba zmysluplnosti mien
Pojem „zmysluplnosť“ znamená, že forma mena musí mať bežne používaný formát na určenie identity Držiteľa (fyzická osoba, právnická osoba/organizácia).

### 3.1.3 Anonymita alebo pseudonym odberateľov
Poskytovateľ nepodporuje používanie pseudonymov, prezývok, krycích mien, aliasov a podobne (tzv. „nicknames“) v certifikátoch.

### 3.1.4 Pravidlá interpretácie rôznych foriem mien

#### 3.1.4.1 Nahrádzanie ne-ASCII znakov
Slovenské diakritické znaky, ktoré nie sú súčasťou základnej sady znakov ASCII, môžu byť v certifikáte použité.  
V prípade potreby môžu byť slovenské diakritické znaky nahradené ich ekvivalentmi v základnej tabuľke ASCII nasledovne:

| Znak | ASCII ekvivalent | | Znak | ASCII ekvivalent |
| :---: | :---: | :---: | :---: | :---: |
| á, ä | a | | Á, Ä | A |
| č | c | | Č | C |
| ď | d | | Ď | D |
| dž | dz | | DŽ | DZ |
| é | e | | É | E |
| í | i | | Í | I |
| ľ, ĺ | l | | Ľ, Ĺ | L |
| ň | n | | Ň | N |
| ó, ô | o | | Ó, Ô | O |
| ŕ | r | | Ŕ | R |
| š | s | | Š | S |
| ť | t | | Ť | T |
| ú | u | | Ú | U |
| ý | y | | Ý | Y |
| ž | z | | Ž | Z |

#### 3.1.4.2 Geografické názvy
Žiadne ustanovenia.

### 3.1.5 Jedinečnosť mien
Žiadne ustanovenia.

### 3.1.6 Rozpoznávanie, autentifikácia a rola ochranných známok
Žiadne ustanovenia.

## 3.2 Počiatočné overenie identity
Poskytovateľ autentifikuje všetky atribúty identity Subjektu, ktoré budú zahrnuté v certifikáte, a kontrolu Subjektu nad e-mailovou adresou podľa nasledujúcich požiadaviek:

| Typ certifikátu | Kontrola schránky (Mailbox) | Identita organizácie | Identita jednotlivca |
| :--- | :---: | :---: | :---: |
| S/MIME certifikát pre digitálny podpis [Individual-validated] | Časť 3.2.2 | NA | Časť 3.2.4 |
| S/MIME certifikát pre digitálny podpis [Sponsor-validated] | Časť 3.2.2 | Časť 3.2.3 | Časť 3.2.4 |
| S/MIME certifikát pre digitálny podpis [Organization-validated] | Časť 3.2.2 | Časť 3.2.3 | NA |

Autentifikáciu a overenie v mene Poskytovateľa vykonáva pracovník RA pred vydaním certifikátu.

### 3.2.1 Metóda preukázania držby súkromného kľúča
Žiadne ustanovenia.

### 3.2.2 Overenie autorizácie alebo kontroly e-mailovej schránky
Táto časť definuje procesy a postupy na potvrdenie kontroly Žiadateľa nad e-mailovou adresou, ktorá má byť zahrnutá vo vydanom certifikáte.  
RA Poskytovateľa musí overiť, že Žiadateľ kontroluje e-mailovú adresu uvedenú v žiadosti o certifikát.

Poskytovateľ nesmie delegovať overenie kontroly e-mailovej adresy na tretiu stranu (toto sa nevzťahuje na zmluvne viazané RA poskytujúce dôveryhodné služby v mene Poskytovateľa).  
RA Poskytovateľa musí viesť záznamy o tom, ktorá metóda bola použitá na overenie e-mailovej adresy, vrátane verzie SMIME BR [1] použitej pri overovaní.

RA Poskytovateľa môže opätovne použiť dokončené overenie na vydanie viacerých certifikátov, za predpokladu, že sú dodržané časové intervaly v časti 4.2.1.  
*Poznámka: E-mailová adresa môže byť v certifikáte Držiteľa zahrnutá ako rfc822Name alebo ako otherName typu id-on-SmtpUTF8Mailbox v rozšírení subjectAltName.*

#### 3.2.2.1 Overenie autorizácie nad schránkou prostredníctvom domény
Pri vydávaní certifikátu typu „sponsor-validated“ pre zmluvného partnera, kde sa overenie nevykonáva individuálne pre každú e-mailovú adresu Žiadateľa, môže byť kontrola overená potvrdením, že zmluvný partner kontroluje doménovú časť e-mailovej adresy, ktorá sa má použiť v certifikáte.

Pre toto overenie Poskytovateľ použije iba schválené metódy uvedené v časti 3.2.2.4 dokumentu TLS BR [13].  
Pracovník RA vykoná overenie pomocou jednej z týchto metód z dokumentu [13]:  
* E-mail na kontakt uvedený v DNS CAA (kapitola 3.2.2.4.13),  
* E-mail na kontakt uvedený v DNS TXT (kapitola 3.2.2.4.14),  

odoslaním náhodného textového reťazca s dĺžkou aspoň 20 znakov, obsahujúceho veľké a malé písmená, čísla a špeciálne znaky.  
Pre každé overenie pracovník RA zaznamená použitú metódu, dátum použitia a použitú e-mailovú adresu.

#### 3.2.2.2 Overenie kontroly nad schránkou prostredníctvom e-mailu
RA Poskytovateľa môže overiť kontrolu schránky pre každú e-mailovú adresu, ktorá má byť zahrnutá vo vydanom certifikáte, zaslaním náhodnej hodnoty e-mailom a následným prijatím potvrdzujúcej odpovede s použitím tejto náhodnej hodnoty.  
Kontrola nad každou e-mailovou adresou musí byť potvrdená pomocou jedinečnej náhodnej hodnoty. Náhodná hodnota musí byť zaslaná iba na overovanú e-mailovú adresu a nesmie byť zdieľaná žiadnym iným spôsobom.

Náhodná hodnota musí byť jedinečná v každom odoslanom e-maile a môže zostať platná na použitie v potvrdzujúcej odpovedi maximálne 24 hodín od jej vytvorenia. Náhodná hodnota sa musí zmeniť po každom e-maile odoslanom Poskytovateľom na adresu schránky; všetky príslušné náhodné hodnoty odoslané na tú istú adresu schránky však môžu zostať platné pre potvrdzujúce odpovede počas doby platnosti uvedenej v tejto časti.

Pracovník RA vykonáva overenie prostredníctvom aplikácie RA Client odoslaním náhodnej hodnoty na e-mailovú adresu v žiadosti o certifikát. Odoslanie sa vykoná automaticky po načítaní profilu certifikátu a príslušnej žiadosti o vydanie do RA Client a zvolení možnosti overenia e-mailu (verify Email).

Žiadateľ má 24 hodín na potvrdenie náhodnej hodnoty.  
Pracovník RA kontroluje stav overenia v RA Client v časti „Search“ a záložke „Email verification“; ak je stav „approved“, overenie bolo úspešné.

#### 3.2.2.3 Overenie žiadateľa ako operátora pridruženého e-mailového servera (serverov)
Poskytovateľ túto metódu nepodporuje.

#### 3.2.2.4 Overenie kontroly e-mailovej schránky pomocou rozšírení ACME
Poskytovateľ túto metódu nepodporuje.

### 3.2.3 Autentifikácia identity organizácie

Pri overovaní identity právnickej osoby zahrnutej v profiloch certifikátov pre zamestnanca právnickej osoby a certifikátu pre pečať musia byť splnené požiadavky definované v nasledujúcich podkapitolách.

#### 3.2.3.1 Zber atribútov identity organizácie
RA Poskytovateľa musí získať a uchovať dôkaz o identite organizácie (právnickej osoby), ak je zahrnutá v certifikáte:
* Oficiálny názov
* Predpokladaný názov (Assumed name)
* Organizačná jednotka
* Adresa registrovaného sídla
* Právna príslušnosť založenia alebo registrácie
* Jedinečný identifikátor a jeho typ.

Jedinečný identifikátor musí byť uvedený v predmete (Subject) certifikátu ako organizationIdentifier v súlade s článkom 7.1.4.2.2 a prílohou A dokumentu SMIME BR [1].  
Dodatočne (ak sú zahrnuté v certifikáte), RA získa a uchová dôkaz pre:
* Oficiálny názov
* Jedinečný identifikátor a jeho typ

#### 3.2.3.2 Validácia identity organizácie

#### 3.2.3.2.1 Overenie názvu, adresy a jedinečného identifikátora
RA Poskytovateľa overuje úplný názov a adresu (ak sú zahrnuté v predmete certifikátu) žiadajúcej právnickej osoby pomocou poskytnutej dokumentácie alebo komunikáciou s aspoň jedným z nasledujúcich subjektov:  
**1.** Štátny orgán v rámci jurisdikcie založenia, existencie alebo uznania právnickej osoby;  
**2.** Odkaz na údaje identifikátora právnickej osoby (LEI);  
**3.** Overenie pracovníkom RA Poskytovateľa (alebo jeho zástupcom) v priestoroch Žiadateľa; alebo  
**4.** Potvrdenie (attestation), ktoré obsahuje kópiu podpornej dokumentácie preukazujúcej právnu existenciu Žiadateľa (napr. osvedčenie o registrácii, stanovy, zriaďovacia zmluva, štatút alebo regulačný akt).

RA môže použiť dokumentáciu/komunikáciu popísanú v bodoch 1-4 na overenie identity a adresy Žiadateľa.  
U organizácie so sídlom v Slovenskej republike RA overuje úplný názov a jedinečný identifikátor organizácie na základe:
* originálu výpisu z Obchodného registra Slovenskej republiky (OR SR), alebo
* ak Žiadateľ nie je zapísaný v OR SR, originálu výpisu z Registra právnických osôb, podnikateľov a orgánov verejnej moci vedeného Štatistickým úradom Slovenskej republiky (RPO SR).

Ak právnická osoba nemôže preukázať svoju identitu výpisom z obchodného registra alebo registra právnických osôb, musí písomne preukázať (okrem identity) aj zákonnosť / „dôvod“ svojej existencie odkazom na príslušný zákon alebo iný predpis, zakladaciu listinu a pod.

Ak právnická osoba nemá sídlo v Slovenskej republike, jej identita sa overuje predložením výpisu zo štátneho registra v jurisdikcii založenia/existencie/uznania; RA následne potvrdí existenciu prostredníctvom webovej stránky „Business registers - vyhľadávanie spoločnosti v EÚ“.  
Originálny dokument (alebo úradne overená kópia originálu) nesmie byť starší ako tri mesiace a musí obsahovať úplné obchodné meno/názov a identifikačnú hodnotu.  
RA akceptuje aj elektronický výpis z použitého registra, ak je autorizovaný kvalifikovanou elektronickou pečaťou štátneho orgánu zodpovedného za vedenie registra.

#### 3.2.3.3 Overenie predpokladaného názvu (Assumed name)
Poskytovateľ podporuje iba vydávanie certifikátov pod riadne registrovaným názvom.

#### 3.2.3.4 Zverejnenie zdrojov overovania
RA Poskytovateľa musí overiť jedinečný identifikátor použitý v certifikáte v registri vedenom alebo autorizovanom príslušným štátnym orgánom. Poskytovateľ musí tento autorizovaný zdroj zverejniť vhodnými a ľahko dostupnými online prostriedkami (pozri kapitolu 3.2.3.2.1).

### 3.2.4 Autentifikácia identity jednotlivca
Poskytovateľ musí zabezpečiť, aby identita Držiteľa certifikátu a verejný kľúč boli náležite prepojené, a musí vo svojich CP/CPS špecifikovať autentifikačné postupy. CA Poskytovateľa musí tento proces zaznamenať pre každý certifikát v písomnej alebo elektronickej forme. Dokumentácia o autentifikácii musí obsahovať aspoň:
* identitu osoby vykonávajúcej autentifikáciu,
* jednoznačné identifikačné údaje z dokladov totožnosti preukazujúcich identitu Držiteľa certifikátu,
* dátum vykonania identifikácie.

Overenie identity musí vykonať RA Poskytovateľa na základe dokladu obsahujúceho tieto údaje Držiteľa:
* úplné meno a priezvisko,
* adresu trvalého pobytu,
* rodné číslo (u osôb, ktoré ho majú pridelené),
* dátum narodenia (u osôb bez prideleného rodného čísla),
* ďalšie údaje uvedené v časti 3.2.4.1.

RA musí spracovávať a uchovávať osobné údaje v súlade s platnými zákonmi a ustanoveniami v časti 9.4.

#### 3.2.4.1 Zber atribútov identity jednotlivca
Poskytovateľ musí zdokumentovať a zverejniť metódy, ktoré používa a zhromažďuje na overenie identity fyzickej osoby.

##### 3.2.4.1.1 Z fyzického dokladu totožnosti
Pre overenie identity RA Poskytovateľa v súčasnosti akceptuje nasledujúce doklady predložené Držiteľom osobne:
* občiansky preukaz (eID vydaný štátnym orgánom) alebo povolenie na pobyt v Slovenskej republike (v prípade cudzincov); alebo
* cestovný pas.

Odberateľ/Držiteľ musí predložiť aj ďalší doklad obsahujúci aspoň meno Držiteľa a ďalší osobný atribút (dátum narodenia, rodné číslo), ako napríklad:
* vodičský preukaz;
* rodný list;
* služobný preukaz;
* preukaz poistenca;
* zbrojný preukaz;
* cestovný pas.

RA Poskytovateľa musí z dokladov zaznamenať aj nasledujúce údaje:
* úplné meno a priezvisko;
* trvalý pobyt (ak je uvedený v doklade);
* rodné číslo (žiadatelia, ktorí ho majú pridelené);
* dátum narodenia (žiadatelia bez rodného čísla);
* sériové číslo dokladu totožnosti;
* vydavateľa dokladu totožnosti;
* platnosť dokladu totožnosti.

V prípade predloženia rodného listu, zbrojného preukazu, služobného preukazu alebo preukazu poistenca musí Držiteľ predložiť aj jeden z nasledujúcich dokladov: občiansky preukaz alebo cestovný pas.  
Ak fyzická osoba zastupuje inú fyzickú osobu, musí navyše predložiť úradne overené plnomocenstvo jasne oprávňujúce zástupcu konať v mene zastupovanej osoby, ktoré obsahuje všetky údaje uvedené v časti 3.2.4.1.

##### 3.2.4.1.2 Z digitálneho dokladu totožnosti
Poskytovateľ v súčasnosti nepodporuje túto metódu pre počiatočné overenie identity fyzickej osoby.

##### 3.2.4.1.3 Použitie schém elektronickej identifikácie
Poskytovateľ v súčasnosti nepodporuje túto metódu pre počiatočné overenie identity fyzickej osoby.

##### 3.2.4.1.4 Z certifikátu podporujúceho digitálny podpis vyhotovený Žiadateľom
Poskytovateľ v súčasnosti túto metódu počiatočnej autentifikácie identity nepoužíva.

##### 3.2.4.1.5 Záznamy Enterprise RA
Enterprise RA vydávajúca „sponsor-validated“ podpisový certifikát overí všetky atribúty identity fyzickej osoby, ktoré majú byť zahrnuté v certifikáte. Pri overovaní sa Enterprise RA môže spoliehať na existujúce interné záznamy a nemusí vyžadovať fyzické predloženie dokladu totožnosti za predpokladu, že interné záznamy obsahujú všetky osobné údaje vyžadované Poskytovateľom a údaje, ktoré budú zapísané do certifikátu.

##### 3.2.4.1.6 Príslušnosť (Affiliation) z potvrdenia spoločnosti
V prípade certifikátov typu „Sponsor-validated“, ktoré nie sú schválené prostredníctvom Enterprise RA, môže RA overiť oprávnenie alebo príslušnosť jednotlivca k organizácii, ktorá má byť zahrnutá v „subject:organizationName“ certifikátu, pomocou potvrdenia (Attestation) poskytnutého organizáciou. RA overí identitu fyzickej osoby podľa časti 3.2.4 a overí identitu spoločnosti podľa časti 3.2.3.

#### 3.2.4.2 Validácia identity jednotlivca
RA Poskytovateľa validuje všetky atribúty identity jednotlivca, ktoré majú byť zahrnuté v certifikáte.  
Ak má dôkaz explicitnú dobu platnosti, CA overí, či čas validácie identity spadá do tejto doby platnosti. V kontexte to môže zahŕňať atribúty „validFrom“ a „validTo“ certifikátu pre digitálny podpis alebo dátum exspirácie dokladu totožnosti.  
RA Poskytovateľa môže opätovne použiť existujúce dôkazy na validáciu identity jednotlivca s ohľadom na vekové obmedzenia v časti 4.2.1.

##### 3.2.4.2.1 Validácia fyzického dokladu totožnosti
Fyzický doklad totožnosti musí byť predložený v origináli. RA Poskytovateľa akceptuje iba osobne predložený doklad a nepodporuje jeho vzdialené overenie, napr. prostredníctvom videa.  
Registračný pracovník RA vykoná vizuálne porovnanie fyzického vzhľadu Žiadateľa a fotografie tváre a/alebo iných informácií na fyzickom doklade totožnosti.  
Registračný pracovník RA musí mať prístup k autoritatívnym zdrojom informácií o vzhľade dokladov.  
Poskytovateľ alebo RA Poskytovateľa uchováva informácie dostatočné na preukázanie splnenia procesu validácie identity a overených atribútov. Okrem atribútov identity Poskytovateľ zaznamenáva nasledujúce informácie: vydavateľ, doba platnosti a jedinečné identifikačné číslo dokladu.

##### 3.2.4.2.2 Validácia digitálneho dokladu totožnosti
Poskytovateľ v súčasnosti túto metódu počiatočnej autentifikácie identity nepoužíva.

##### 3.2.4.2.3 Validácia eID
Poskytovateľ v súčasnosti túto metódu počiatočnej autentifikácie identity nepoužíva.

##### 3.2.4.2.4 Validácia digitálneho podpisu s certifikátom
Poskytovateľ v súčasnosti túto metódu počiatočnej autentifikácie identity nepoužíva.

##### 3.2.4.2.5 Validácia potvrdenia (Attestation)
Ak sa potvrdenie (Attestation) používa ako dôkaz na validáciu atribútov identity fyzickej osoby, musí byť jeho spoľahlivosť overená podľa časti 3.2.8.

##### 3.2.4.2.6 Validácia s použitím záznamu Enterprise RA
Enterprise RA vydávajúca „sponsor-validated“ podpisový certifikát musí overiť všetky atribúty identity fyzickej osoby, ktoré majú byť zahrnuté v certifikáte. Pri overovaní sa Enterprise RA môže spoliehať na existujúce interné záznamy a nemusí vyžadovať fyzické predloženie dokladu totožnosti za predpokladu, že interné záznamy obsahujú všetky osobné údaje vyžadované Poskytovateľom a údaje, ktoré budú zapísané do certifikátu.

### 3.2.5 Neoverené informácie o odberateľovi
Informácie o Žiadateľovi, ktoré neboli overené v súlade s týmito CP/CPS, nesmú byť zahrnuté v certifikátoch.

### 3.2.6 Validácia oprávnenia
Pred začatím vydávania certifikátov typu „Organization-validated“ a „Sponsor-validated“ pre Žiadateľa Poskytovateľ použije spoľahlivú metódu komunikácie na overenie oprávnenia a schválenia zástupcu žiadateľa (Applicant Representative) vykonávať jednu alebo viacero z nasledujúcich činností:
* pôsobiť ako Enterprise RA,
* žiadať o vydanie alebo zrušenie certifikátov, alebo
* priraďovať povinnosti iným osobám na konanie v týchto rolách.

Poskytovateľ môže implementovať proces umožňujúci Žiadateľovi určiť jednotlivcov, ktorí môžu nepretržite konať ako zástupcovia žiadateľa; rovnako Poskytovateľ poskytne Žiadateľovi zoznam jeho autorizovaných zástupcov žiadateľa na základe overenej písomnej žiadosti Žiadateľa.  
Poskytovateľ môže použiť zdroje uvedené v časti 3.2.3.2.1 na overenie spoľahlivej metódy komunikácie. Ak sa použije spoľahlivá metóda komunikácie, Poskytovateľ môže overiť autenticitu žiadosti o certifikát priamo u zástupcu Žiadateľa alebo u dôveryhodného zdroja v rámci organizácie Žiadateľa (napr. obchodné jednotky, personálne oddelenie, IT alebo iné oddelenie, ktoré Poskytovateľ považuje za vhodné).

### 3.2.7 Kritériá pre interoperabilitu
Poskytovateľ musí zverejniť všetky krížové certifikáty, ktoré identifikujú Poskytovateľa ako predmet (Subject) certifikátu.

### 3.2.8 Spoľahlivosť zdrojov overovania
Predtým, ako sa RA Poskytovateľa pri overovaní žiadosti o certifikát spoľahne na zdroj overovacích údajov, musí overiť, či je zdroj vhodný ako spoľahlivý zdroj údajov.  
Záznamy Enterprise RA sú spoľahlivým zdrojom pre atribúty fyzickej osoby zahrnuté v „sponsor-validated“ podpisových certifikátoch vydávaných v rámci organizácie, ktorá je Enterprise RA Poskytovateľa.  
RA Poskytovateľa sa môže spoliehať na potvrdzujúci list, že informácia alebo iná skutočnosť je správna, ak overí, že list bol napísaný účtovníkom, právnikom, štátnym úradníkom alebo inou spoľahlivou treťou stranou v jurisdikcii Žiadateľa, na ktorú sa bežne spolieha pri získavaní takýchto informácií.  
Potvrdenie musí obsahovať kópiu dokumentu preukazujúceho potvrdzovanú skutočnosť.  
RA Poskytovateľa použije spoľahlivú metódu komunikácie na kontaktovanie odosielateľa a potvrdenie autenticity potvrdenia (attestation).

## 3.3 Identifikácia a autentifikácia pri žiadostiach o nový kľúč (re-key)

### 3.3.1 Identifikácia a autentifikácia pri rutinnom re-key
Žiadne ustanovenia.

### 3.3.2 Identifikácia a autentifikácia pri re-key po zrušení
Žiadne ustanovenia.

## 3.4 Identifikácia a autentifikácia pre žiadosť o zrušenie
Žiadne ustanovenia.

# 4.  PREVÁDZKOVÉ POŽIADAVKY NA ŽIVOTNÝ CYKLUS CERTIFIKÁTU

## 4.1 Žiadosť o certifikát
Táto časť popisuje prevádzkové požiadavky na životný cyklus certifikátu počnúc žiadosťou o vydanie.

### 4.1.1 Kto môže podať žiadosť o certifikát
Poskytovateľ môže byť požiadaný o vydanie:
* podpisového certifikátu pre fyzickú osobu (Individual-validated):
   * samotná fyzická osoba
* podpisového certifikátu pre zamestnanca právnickej osoby (Sponsor-validated):
   * fyzická osoba splnomocnená Odberateľom,
   * akýkoľvek subjekt, s ktorým je fyzická osoba spojená (napr. zamestnávateľ, nezisková organizácia, ktorej je osoba členom atď.)
* certifikátu pre pečať pre právnickú osobu (Organization-validated):
   * akýkoľvek subjekt, ktorý podľa príslušnej národnej legislatívy koná v mene danej právnickej osoby (organizácie).

### 4.1.2 Proces registrácie a zodpovednosti

#### 4.1.2.1 Príprava
Ako prípravu na návštevu RA Poskytovateľa, Odberateľ/Držiteľ:
* oboznámi sa so „Všeobecnými podmienkami poskytovania a používania dôveryhodnej služby vydávania a overovania certifikátov“ („Všeobecné podmienky“) [8] a s predpismi o ochrane osobných údajov, t. j. nariadením Európskeho parlamentu a Rady (EÚ) 2016/679 (GDPR) a zákonom č. 18/2018 Z. z. o ochrane osobných údajov a zákonom č. 18/2018 Z. z. o ochrane osobných údajov (ďalej len „Predpisy o ochrane osobných údajov“) [14], ktoré musia byť dostupné v čitateľnej forme prostredníctvom trvalého komunikačného kanála (pozri [https://eidas.disig.sk/sk/documents/](https://eidas.disig.sk/sk/documents/));
* oboznámi sa s týmto postupom a/alebo zásadami a pokynmi na získanie certifikátu;
* pripraví si žiadosť o certifikát vo formáte PKCS#10 a zašle ju vopred e-mailom na RA Poskytovateľa (pozri bod 4.1.2.3);
* pripraví si vybrané doklady totožnosti a/alebo iné požadované podporné dokumenty (napr. výpis z obchodného registra, plnomocenstvá atď.);
* dohodne si termín stretnutia.

#### 4.1.2.2 Generovanie žiadosti

##### 4.1.2.2.1 Generovanie žiadosti o certifikát
Žiadosť o certifikát pre fyzickú osobu alebo právnickú osobu môže byť podaná len na základe žiadosti PKCS#10. Odberateľ/Držiteľ musí vygenerovať žiadosť vo svojom počítači pomocou vhodného prehliadača a webového sídla Poskytovateľa (pozri URL v časti 1) a uložiť ju na vhodné médium.
Žiadosť o certifikát pre fyzickú osobu musí byť zaslaná príslušnej RA Poskytovateľa vopred e-mailom z e-mailovej adresy, ktorá je uvedená v žiadosti o certifikát v poli e-mailu „subject:emailAddress“.

Žiadosť o certifikát pre právnickú osobu musí byť tiež zaslaná príslušnej RA Poskytovateľa vopred e-mailom z e-mailovej adresy, ktorá je uvedená v žiadosti o certifikát v poli e-mailu „subject:emailAddress“. E-mailová adresa v žiadosti o certifikát právnickej osoby nesmie byť e-mailovou adresou jednotlivca. RA Poskytovateľa akceptuje len všeobecnú/zdieľanú e-mailovú adresu právnickej osoby, ako napríklad <obchod@disig.sk>, <faktury@disig.sk> atď.

RA Poskytovateľa si vyhradzuje právo zamietnuť žiadosť o certifikát právnickej osoby, ak táto požiadavka nie je splnená.
E-mailové adresy jednotlivých RA Poskytovateľa sú dostupné na webovom sídle Poskytovateľa (pozri časť 1).
Z bezpečnostných dôvodov žiadosť o certifikát (a v nej obsiahnutý verejný kľúč), pre ktorú už bol certifikát vydaný, nesmie byť opätovne použitá na vydanie ďalšieho certifikátu a RA ju musí zamietnuť.
Pri zadávaní hodnôt do polí žiadosti o certifikát musí Odberateľ/Držiteľ zvážiť, že na RA bude musieť uspokojivo preukázať oprávnenosť na všetky údaje uvedené v jednotlivých poliach žiadosti o certifikát.

Žiadosť o certifikát pre zamestnanca zmluvného partnera môže byť vygenerovaná aj inou metódou ako cez webové sídlo Poskytovateľa (napr. vlastný webový portál zmluvného partnera atď.). Táto metóda musí byť vopred dohodnutá so zmluvným partnerom a jednotliví žiadatelia musia byť o spôsobe generovania a podávania žiadosti informovaní zmluvným partnerom aj Poskytovateľom.

#### 4.1.2.3 Odoslanie žiadosti o certifikát
Odberateľ/Držiteľ predkladá žiadosť o vydanie certifikátu príslušnej RA Poskytovateľa ([https://eidas.disig.sk/sk/kontakt/registracne-autority/](https://eidas.disig.sk/sk/kontakt/registracne-autority/)), ktorá musí vykonať všetky postupy súvisiace s procesom vydávania certifikátu.

## 4.2 Spracovanie žiadosti o certifikát

### 4.2.1 Vykonávanie identifikačných a autentifikačných funkcií
Pred vydaním certifikátu RA Poskytovateľa:
* informuje prítomnú fyzickú osobu o Všeobecných podmienkach [8];
* skontroluje úplnosť a správnosť údajov v prijatej žiadosti o certifikát;
* overí identitu budúceho Držiteľa certifikátu a vloží jeho osobné údaje do informačného systému (IS) Poskytovateľa, pričom vyplní všetky povinné polia vyžadované systémom Poskytovateľa;
* overí dodatočné dokumenty podporujúce akékoľvek identifikačné údaje, ktoré majú byť zahrnuté v certifikáte.

Ak je certifikát určený pre fyzickú osobu alebo právnickú osobu, kde kryptografické kľúče nie sú v QSCD, pracovník RA Poskytovateľa pred overením identity Držiteľa certifikátu skontroluje doručenú žiadosť o certifikát, ktorá môže byť vo formáte PKCS#10. Pre obsah polí žiadosti a povinnosť ich vyplnenia pozri časť 7.
Pracovník RA Poskytovateľa overí, že elektronicky podaná žiadosť o certifikát daného Odberateľa/Držiteľa obsahuje pole „subject:emailAddress“ a že bola zaslaná z rovnakej e-mailovej adresy, aká je uvedená v žiadosti o certifikát. V prípade zistenia rozdielov môže personál RA odmietnuť vydanie certifikátu.

Pred vydaním certifikátu vykoná RA Poskytovateľa prostredníctvom aplikácie RA Client nasledujúce:
* skontroluje, či e-mailová adresa uvedená v žiadosti zodpovedá e-mailovej adrese, z ktorej bola žiadosť odoslaná;
* skontroluje úplnosť a správnosť údajov v prijatej žiadosti o certifikát, vrátane toho, že obsahuje len povolené polia v súlade s časťou 7.1.4.2.2 týchto CP/CPS;
* overí vlastníctvo a kontrolu Žiadateľa nad e-mailovou adresou v súlade s časťou 4.2.1.1;
* skontroluje, či overenie vlastníctva/kontroly nad e-mailovou adresou Žiadateľa bolo úspešné a či certifikát môže byť vydaný.
V prípade osobnej návštevy Žiadateľa alebo splnomocneného zástupcu na RA Poskytovateľa, personál RA:
* informuje prítomnú fyzickú osobu o Všeobecných podmienkach [8];
* overí identitu budúceho Držiteľa certifikátu v súlade s časťou 3.2.4.2 a prostredníctvom aplikácie RA Client vloží jeho osobné údaje do IS Poskytovateľa, pričom vyplní všetky povinné polia vyžadované systémom Poskytovateľa,
* overí dodatočné dokumenty podporujúce akékoľvek identifikačné údaje, ktoré majú byť zahrnuté v certifikáte, napr. identitu organizácie v súlade s časťou 3.2.3.2.

V prípade zistenia rozdielov môže pracovník RA odmietnuť vydanie certifikátu.
Pri overovaní identity fyzickej osoby alebo právnickej osoby môže byť existujúce overenie identity opätovne použité, za predpokladu, že spĺňa časové limity uvedené v častiach 4.2.1.3 a 4.2.1.2.

#### 4.2.1.1 Validácia autorizácie alebo kontroly e-mailovej schránky
Overenie vlastníctva a kontroly e-mailovej adresy prostredníctvom domény, alebo overenie Žiadateľa ako operátora príslušných poštových serverov, úspešne dokončené v súlade s požiadavkami časti 3.2.2.1 alebo časti 3.2.2.3, môže byť získané najskôr 398 dní pred vydaním certifikátu.
Overenie vlastníctva a kontroly e-mailovej adresy, úspešne dokončené v súlade s požiadavkami časti 3.2.2, môže byť získané najskôr 30 dní pred vydaním certifikátu.

#### 4.2.1.2 Autentifikácia identity organizácie
Overenie kontroly, úspešne dokončené v súlade s požiadavkami časti 3.2.3, môže byť získané najskôr 825 dní pred vydaním certifikátu.
Potvrdenie oprávnenia v súlade s požiadavkami časti 3.2.6 môže byť získané najskôr 825 dní pred vydaním certifikátu, pokiaľ zmluva medzi Poskytovateľom a Odberateľom/Držiteľom neurčuje iné obdobie.

#### 4.2.1.3 Autentifikácia identity jednotlivca
Úplné overenie identity fyzickej osoby v súlade s článkom 3.2.4 môže byť získané najskôr 825 dní pred vydaním certifikátu. Predchádzajúca validácia nesmie byť opätovne použitá, ak akékoľvek údaje alebo dokumenty použité v predchádzajúcej validácii boli získané skôr, ako je povolené obdobie opätovného použitia.

### 4.2.2 Schválenie alebo zamietnutie žiadostí o certifikát
Pracovník RA začne spracovávať žiadosť o vydanie certifikátu ihneď po jej prijatí, v súlade s postupmi stanovenými v časti 4.2.1. Certifikát bude vydaný za predpokladu, že sú splnené všetky podmienky vydania a je tiež overené, že Poskytovateľ je oprávnený vydať certifikát v súlade s časťou 4.2.2.1.
Pracovník RA zamietne žiadosť o vydanie certifikátu, ak má dôvodnú pochybnosť o identite Držiteľa, a tiež ak sú zistené nedostatky v identifikačných dokladoch, boli poskytnuté neúplné informácie, alebo ak Poskytovateľ predtým vydal certifikát pre daný verejný kľúč, alebo ak Poskytovateľ nie je oprávnený vydať certifikát.

#### 4.2.2.1 Autorizácia certifikačnej autority (CAA)
Odberatelia, ktorí si želajú obmedziť („rezervovať“) poskytovateľov vydávajúcich certifikáty a želajú si, aby Disig, a. s. bol medzi vybranými poskytovateľmi, by mali do svojho DNS záznamu pre vlastnosť „issuemail“ zadať hodnotu „disig.sk“.

Od 15. marca 2025 Poskytovateľ vykonáva kontrolu záznamu CAA doménového mena uvedeného v e-mailovej adrese v žiadosti o vydanie certifikátu, v súlade s časťou 4 RFC 9495 [15].
Niektoré metódy, na ktoré sa spolieha pri overovaní kontroly Držiteľa nad doménovou časťou adresy schránky, ktorá sa má použiť v certifikáte (pozri časti 3.2.2.1 a 3.2.2.3), vyžadujú, aby boli záznamy CAA pred vydaním certifikátu získané a spracované z ďalších vzdialených sieťových perspektív (pozri časť 4.2.2.2).

Na potvrdenie primárnej sieťovej perspektívy musí byť odpoveď na kontrolu CAA zo vzdialenej sieťovej perspektívy interpretovaná ako autorizácia na vydanie bez ohľadu na to, či sú odpovede z oboch perspektív bit po bite identické.

Ak Poskytovateľ vydá certifikát po kontrole CAA, musí tak urobiť v rámci TTL záznamu CAA alebo do 8 hodín, podľa toho, čo je dlhšie. Toto ustanovenie nebráni CA kontrolovať záznamy CAA v akomkoľvek inom čase.

Poskytovateľ musí dostatočne podrobne dokumentovať potenciálne vydania, ktorým zabránil existujúci záznam CAA, aby mohol poskytnúť spätnú väzbu CA/Browser fóru o okolnostiach, a mal by zasielať správy o takýchto žiadostiach o vydanie na kontakty uvedené v záznamoch CAA iodef, ak sú prítomné.
Od Poskytovateľa sa neočakáva, že bude podporovať iné schémy URL v zázname iodef okrem mailto: alebo https:.

#### 4.2.2.2 Viacperspektívne potvrdzovanie vydávania (MPIC)
Poskytovateľ implementoval MPIC v súlade s bodom 3.2.2.9 dokumentu TLS Baseline Requirements (BR TLS) [13].

### 4.2.3 Čas na spracovanie vydania certifikátu
Žiadne ustanovenia.

## 4.3 Vydanie certifikátu

### 4.3.1 Kroky CA počas vydávania certifikátu

#### 4.3.1.1 Manuálna autorizácia vydávania certifikátov pre koreňové CA
Vydanie certifikátu koreňovou CA (Root CA) vyžaduje prítomnosť aspoň dvoch osôb v dôveryhodných rolách (napr. správca systému CA, administrátor CA, manažér CA), z ktorých jedna vydá jednoznačný príkaz inštruujúci koreňovú CA Disig vykonať podpísanie certifikátu.

#### 4.3.1.2 Kontrola (linting) obsahu certifikátu pred podpisom
Pred vydaním certifikátu sa vykonáva automatizovaná validácia vydávaného certifikátu na súlad so SMIME BR a týmito CP/CPS. Ak sa počas validácie zistí nesúlad, vydávací systém Poskytovateľa vydanie certifikátu zamietne.

#### 4.3.1.3 Kontrola (linting) vydaných certifikátov
Poskytovateľ používa proces validácie na testovanie súladu s týmito požiadavkami pre každý certifikát, ktorý vydá.
Po vydaní certifikátu sa vykonáva automatizovaná validácia vydaného certifikátu na súlad so SMIME BR a týmito CP/CPS. Ak sa počas validácie zistí nesúlad, musí sa vykonať analýza príčin nesúladu.

### 4.3.2 Informovanie odberateľa zo strany CA o vydaní certifikátu
Odberateľ je informovaný po vydaní certifikátu. Oznámenie obsahuje základné informácie o certifikáte a pokyny, ako ho stiahnuť a nainštalovať.

## 4.4 Prevzatie certifikátu

### 4.4.1 Konanie predstavujúce prevzatie certifikátu
Žiadne ustanovenia.

### 4.4.2 Zverejnenie certifikátu autoritou CA
Žiadne ustanovenia.

### 4.4.3 Informovanie iných subjektov zo strany CA o vydaní certifikátu
Žiadne ustanovenia.

## 4.5 Používanie páru kľúčov a certifikátu

### 4.5.1 Používanie súkromného kľúča a certifikátu odberateľom
Pozri časť 9.6.3, ustanovenia 2. a 4.

### 4.5.2 Používanie verejného kľúča a certifikátu spoliehajúcou sa stranou
Žiadne ustanovenia.

## 4.6 Obnova certifikátu (Renewal)
Každý certifikát sa vydáva pre nanovo vygenerované kľúče a postup sa vykonáva v súlade s ustanoveniami uvedenými v častiach 4.1 až 4.5.

### 4.6.1 Okolnosti pre obnovu certifikátu
Žiadne ustanovenia.

### 4.6.2 Kto môže žiadať o obnovu
Žiadne ustanovenia.

### 4.6.3 Spracovanie žiadostí o obnovu certifikátu
Žiadne ustanovenia.

### 4.6.4 Informovanie odberateľa o vydaní nového certifikátu
Žiadne ustanovenia.

### 4.6.5 Konanie predstavujúce prevzatie obnoveného certifikátu
Žiadne ustanovenia.

### 4.6.6 Zverejnenie obnoveného certifikátu autoritou CA
Žiadne ustanovenia.

### 4.6.7 Informovanie iných subjektov zo strany CA o vydaní certifikátu
Žiadne ustanovenia.

## 4.7 Výmena kľúčov certifikátu (Re-key)
Každý certifikát sa vždy vydáva ako nový certifikát pre nanovo vygenerované kľúče a žiadosť o certifikát, pričom postup je v súlade s ustanoveniami uvedenými v častiach 4.1 až 4.5.

### 4.7.1 Okolnosti pre výmenu kľúčov certifikátu
Žiadne ustanovenia.

### 4.7.2 Kto môže žiadať o certifikáciu nového verejného kľúča
Žiadne ustanovenia.

### 4.7.3 Spracovanie žiadostí o výmenu kľúčov certifikátu
Žiadne ustanovenia.

### 4.7.4 Informovanie odberateľa o vydaní nového certifikátu
Žiadne ustanovenia.

### 4.7.5 Konanie predstavujúce prevzatie certifikátu s vymenenými kľúčmi
Žiadne ustanovenia.

### 4.7.6 Zverejnenie certifikátu s vymenenými kľúčmi autoritou CA
Žiadne ustanovenia.

### 4.7.7 Informovanie iných subjektov zo strany CA o vydaní certifikátu
Žiadne ustanovenia.

## 4.8 Modifikácia certifikátu

### 4.8.1 Okolnosti pre modifikáciu certifikátu
Žiadne ustanovenia.

### 4.8.2 Kto môže žiadať o modifikáciu certifikátu
Žiadne ustanovenia.

### 4.8.3 Spracovanie žiadostí o modifikáciu certifikátu
Žiadne ustanovenia.

### 4.8.4 Informovanie odberateľa o vydaní nového certifikátu
Žiadne ustanovenia.

### 4.8.5 Konanie predstavujúce prevzatie modifikovaného certifikátu
Žiadne ustanovenia.

### 4.8.6 Zverejnenie modifikovaného certifikátu autoritou CA
Žiadne ustanovenia.

### 4.8.7 Informovanie iných subjektov zo strany CA o vydaní certifikátu
Žiadne ustanovenia.

## 4.9 Zrušenie a pozastavenie certifikátu

### 4.9.1 Okolnosti pre zrušenie
Certifikát bude zrušený, keď sa väzba medzi Subjektom a jeho verejným kľúčom, ako je definovaná v certifikáte, už nepovažuje za platnú.

#### 4.9.1.1 Dôvody na zrušenie certifikátu Odberateľa/Subjektu
Poskytovateľ musí zrušiť certifikát do 24 hodín, ak nastane niektorá z nasledujúcich skutočností:
* Odberateľ/Držiteľ alebo iná oprávnená strana podá písomnú žiadosť o zrušenie,
* Odberateľ/Držiteľ oznámi Poskytovateľovi, že pôvodná žiadosť o vydanie nebola ním autorizovaná a neposkytne následnú autorizáciu na vydanie,
* Poskytovateľ získa dôkaz, že súkromný kľúč prislúchajúci k verejnému kľúču v certifikáte bol kompromitovaný,
* Poskytovateľ získa dôkaz, preukázateľnou alebo overenou metódou, že súkromný kľúč sa dá ľahko vypočítať zo znalosti verejného kľúča certifikátu (napr. problém slabých kľúčov Debian),
* Poskytovateľ získa dôkaz, že sa už nemôže spoliehať na overenie vlastníctva a kontroly e-mailovej adresy uvedenej v certifikáte.

Poskytovateľ by mal zrušiť certifikát do 24 hodín a musí ho zrušiť do piatich (5) dní, ak nastane niektorá z nasledujúcich skutočností:
* certifikát už nespĺňa požiadavky stanovené v častiach 6.1.5 a 6.1.6,
* Poskytovateľ získa dôkaz, že certifikát bol zneužitý,
* Poskytovateľ zistí, že Držiteľ certifikátu neplní svoje povinnosti Držiteľa certifikátu, ku ktorým je zmluvne viazaný,
* Poskytovateľ je informovaný o okolnostiach naznačujúcich, že používanie e-mailovej adresy alebo plne kvalifikovaného doménového mena (FQDN) v certifikáte už nie je legálne povolené (napr. súd alebo rozhodca zrušil právo používať e-mailovú adresu alebo doménové meno; príslušná licencia alebo zmluva o poskytovaní služieb s Odberateľom bola ukončená; alebo držiteľ účtu nesplnil podmienky na udržanie e-mailovej adresy alebo doménového mena v aktívnom stave),
* Poskytovateľ sa dozvie o podstatných zmenách informácií uvedených v certifikáte,
* Poskytovateľ sa dozvie, že certifikát nebol vydaný v súlade s týmito CP/CPS,
* Poskytovateľ zistí, že akákoľvek informácia uvedená v certifikáte je nepresná,
* Poskytovateľ ukončí svoju činnosť z akéhokoľvek dôvodu a zmluvne nezabezpečí, aby iná CA poskytovala informácie o zrušených certifikátoch v jeho mene,
* právo Poskytovateľa vydávať certifikáty podľa týchto CP/CPS zaniklo, bolo zrušené alebo bolo vydávanie ukončené, pokiaľ Poskytovateľ neprijal opatrenia na zabezpečenie kontinuity služieb úložiska CRL/OCSP,
* zrušenie vyžadujú ustanovenia týchto CP/CPS,
* Poskytovateľ je informovaný, na základe preukázateľnej alebo overenej metódy, že súkromný kľúč Držiteľa je vystavený kompromitácii, alebo existuje jasný dôkaz, že špecifická metóda generovania kľúčov bola chybná.

Vždy, keď sa Poskytovateľ dozvie o ktorejkoľvek z vyššie uvedených okolností, certifikát musí byť zrušený a pridaný do zoznamu zrušených certifikátov („CRL“).
Zrušený certifikát nesmie byť za žiadnych okolností obnovený (reinstated).

#### 4.9.1.2 Dôvody na zrušenie certifikátu podriadenej CA
Poskytovateľ musí zrušiť certifikát podriadenej CA do 7 dní, ak:
* dostane písomnú žiadosť o zrušenie certifikátu podriadenej CA,
* podriadená CA informuje vydávajúcu CA Poskytovateľa, že pôvodná žiadosť nebola autorizovaná a neposkytne následnú autorizáciu,
* Poskytovateľ získa dôkaz, že súkromný kľúč prislúchajúci k verejnému kľúču v certifikáte podriadenej CA bol kompromitovaný, alebo už nespĺňa požiadavky stanovené v častiach 6.1.5 a 6.1.6,
* Poskytovateľ získa dôkaz, že certifikát podriadenej CA bol zneužitý,
* Poskytovateľ sa dozvie, že certifikát podriadenej CA nebol vydaný v súlade s týmito CP/CPS,
* Poskytovateľ zistí, že akákoľvek informácia uvedená v certifikáte podriadenej CA je nepresná alebo zavádzajúca,
* činnosť CA je ukončená a neexistuje možnosť, že iná CA poskytne informácie o stave zrušených certifikátov,
* právo vydávajúcej CA Poskytovateľa alebo podriadenej CA vydávať certifikáty podľa týchto CP/CPS zaniklo, bolo zrušené alebo bolo vydávanie ukončené, pokiaľ Poskytovateľ neprijal opatrenia na zabezpečenie kontinuity služieb úložiska CRL/OCSP,
* zrušenie vyžadujú tieto CP/CPS.

### 4.9.2 Kto môže žiadať o zrušenie
Držiteľ certifikátu (alebo ním poverená fyzická alebo právnická osoba) môže kedykoľvek požiadať o zrušenie svojho vlastného certifikátu, a to aj bez uvedenia dôvodu žiadosti o zrušenie.
Žiadosť o zrušenie môže podať aj:
* Poskytovateľ – príslušný pracovník musí túto skutočnosť písomne zdokumentovať vrátane dôvodu svojho konania,
* súd prostredníctvom svojho rozsudku alebo predbežného opatrenia (k dokumentácii o zrušení musí byť priložená kópia príslušného súdneho rozhodnutia),
* subjekt (fyzická alebo právnická osoba) na základe dedičského konania (k dokumentácii o zrušení musí byť priložená kópia dokladov preukazujúcich právo subjektu žiadať o zrušenie).

Odberatelia, spoliehajúce sa strany, dodávatelia aplikačného softvéru a iné tretie strany môžu podávať správy o problémoch týkajúcich sa certifikátu, ktoré informujú vydávajúcu CA o primeranom dôvode na zrušenie.

### 4.9.3 Postup pri žiadosti o zrušenie
Ak sú splnené požiadavky na autentifikáciu Držiteľa certifikátu žiadajúceho o zrušenie, žiadosť o zrušenie certifikátu môže byť podaná nasledovne:
* osobne v kancelárii RA pomocou formulára „Žiadosť o zrušenie certifikátu“ dostupného v RA – pracovník RA môže vyžiadať heslo na zrušenie certifikátu, ak osobou žiadajúcou o zrušenie nie je Držiteľ certifikátu, ale splnomocnený zástupca;
* e-mailom – zaslaním podpísanej e-mailovej správy s použitím súkromného kľúča, ktorý tvorí pár s certifikátom, ktorý sa ruší. Správa musí obsahovať jednoznačný úmysel zrušiť certifikát vyjadrený vetou: „Týmto žiadam o zrušenie môjho certifikátu so sériovým číslom XXXXXX“;
* e-mailom – zaslaním e-mailovej správy (nemusí byť podpísaná). Správa musí obsahovať jednoznačný úmysel zrušiť certifikát vyjadrený vetou: „Týmto žiadam o zrušenie môjho certifikátu so sériovým číslom XXXXXX“. Pri správe podanej týmto spôsobom musí e-mail obsahovať aj heslo na zrušenie certifikátu;
* poštou spolu s heslom na zrušenie certifikátu, zaslanou na adresu Poskytovateľa alebo príslušnej RA Poskytovateľa, ktorá sprostredkovala vydanie rušeného certifikátu;
* prostredníctvom online služby dostupnej na webovom sídle Poskytovateľa. Odkaz na online službu zrušenia certifikátu je uvedený v potvrdení o prevzatí certifikátu, ktoré Držiteľ dostane pri preberaní certifikátu. Online zrušenie vyžaduje zadanie sériového čísla príslušného certifikátu a hesla na zrušenie.

Žiadosť o zrušenie certifikátu vydaného pre potreby zmluvného partnera môže byť podaná buď priamo Poskytovateľovi, alebo len tej RA Poskytovateľa, ktorá je uvedená v príslušnej zmluve a koná v mene Poskytovateľa u zmluvného partnera.
Certifikát, ktorého platnosť vypršala, nemôže byť zrušený.
Kontakty na nahlasovanie incidentov a postup pri nahlasovaní incidentov v prípade možnej kompromitácie súkromného kľúča, zneužitia certifikátu alebo iných typov podvodov, neoprávneného vydania alebo akejkoľvek inej záležitosti týkajúcej sa vydaného certifikátu sú uvedené v časti 1.5.2.

### 4.9.4 Lehota na podanie žiadosti o zrušenie
Žiadne ustanovenia.

### 4.9.5 Čas, v ktorom CA musí spracovať žiadosť o zrušenie
Do 24 hodín od oznámenia problému s certifikátom Poskytovateľ prešetrí skutočnosti týkajúce sa nahláseného problému a poskytne Odberateľovi/Držiteľovi a spoliehajúcim sa stranám predbežné informácie o svojich zisteniach.
Po preskúmaní skutočností a okolností Poskytovateľ v spolupráci s Odberateľom/Držiteľom a koncovou entitou, ktorá problém nahlásila, rozhodne o tom, či bude certifikát zrušený a ak áno, v akom časovom rámci.

Čas medzi prijatím správy o probléme s certifikátom a zverejnením informácie o zrušení nesmie presiahnuť časový rámec uvedený v časti 4.9.1.1.
Pri určovaní lehoty Poskytovateľ zohľadní nasledovné:
* povahu údajného problému (rozsah, kontext, závažnosť, riziko škody pre dotknuté strany),
* dôsledky zrušenia (priame a nepriame dopady na Odberateľov/Držiteľov),
* počet nahlásených problémov týkajúcich sa predmetného certifikátu,
* subjekt, ktorý problém nahlásil,
* platné právne predpisy.

### 4.9.6 Požiadavka na kontrolu zrušenia pre spoliehajúce sa strany
Pri spoliehaní sa na certifikát musí spoliehajúca sa strana overiť jeho platnosť v súlade so Všeobecnými podmienkami.
Počas obdobia medzi podaním autorizovanej žiadosti o zrušenie certifikátu a zverejnením zrušeného certifikátu v CRL nesie Odberateľ/Držiteľ plnú zodpovednosť za akékoľvek škody spôsobené zneužitím ich certifikátu. Po zverejnení certifikátu v CRL nesie plnú zodpovednosť za akékoľvek škody spôsobené použitím zrušeného certifikátu strana, ktorá sa na zrušený certifikát spoliehala.
Neoverenie certifikátu pomocou CRL sa považuje za podstatné porušenie týchto CP/CPS.

### 4.9.7 Periodicita vydávania CRL
Periodicita vydávania zoznamu zrušených certifikátov (CRL) sa líši v závislosti od toho, či sa týka koreňovej CA alebo podriadenej CA. Tabuľka č. 3 obsahuje informácie o maximálnych požiadavkách na vydávanie.

Tabuľka 3: Periodicita vydávania CRL
| Vydavateľ CRL | Periodicita vydávania | nextUpdate vs. thisUpdate | Poznámky |
| :--- | :---: | :---: | :--- |
| Koreňová CA | max 365 dní | < 365 dní | Vždy do 24 hodín po zrušení podriadenej CA |
| Podriadená CA | max 7 dní | < 10 dní | |

Podriadené CA Poskytovateľa, ktoré vydávajú certifikáty koncovým používateľom, musia vydávať CRL:
* aspoň každých 24 hodín, aj keď počas predchádzajúcich 24 hodín nebol zrušený žiadny certifikát, a s hodnotou nextUpdate 24 hodín.
* Koreňové CA Poskytovateľa, ktoré vydávajú certifikáty podriadeným CA, musia vydávať CRL:
* aspoň každých 7 dní, s hodnotou nextUpdate nie viac ako 10 dní,
* vždy do 24 hodín po zrušení certifikátu podriadenej CA.

### 4.9.8 Maximálne oneskorenie CRL
Maximálne oneskorenie CRL od jeho vydania po jeho zverejnenie v úložisku nesmie presiahnuť 90 sekúnd.

### 4.9.9 Dostupnosť on-line overovania stavu (OCSP)
Služba OCSP je poskytovaná v súlade s požiadavkami RFC 6960 a odpoveď OCSP je podpísaná:
* OCSP responderom, ktorého certifikát je podpísaný CA, ktorá vydala certifikát, ktorého stav zrušenia sa kontroluje.

Podpisový certifikát OCSP respondera obsahuje EKU ocspSigning (1.3.6.1.5.5.7.3.9) a rozšírenie id-pkix-ocsp-nocheck, ako je definované v RFC 6960 [16].

### 4.9.10 Požiadavky na on-line overovanie stavu
OCSP respondery Poskytovateľa podporujú metódu HTTP GET v súlade s RFC 6960 [16] a/alebo RFC 5019 [17].
Pre stav S/MIME certifikátov:
* interval platnosti odpovede OCSP je väčší alebo rovný 8 hodinám,
* interval platnosti odpovede OCSP je menší alebo rovný 8 dňom,
* Poskytovateľ aktualizuje informácie poskytované prostredníctvom OCSP okamžite po zmene stavu certifikátu v IS.

Pre stav certifikátov podriadených CA sa informácie poskytované prostredníctvom OCSP aktualizujú:
* aspoň každých dvanásť (12) mesiacov,
* do dvadsiatich štyroch (24) hodín po zrušení certifikátu podriadenej CA.

Ak OCSP responder prijme žiadosť o kontrolu stavu certifikátu so sériovým číslom, ktoré nebolo vydané príslušnou vydávajúcou CA, OCSP responder nesmie vrátiť odpoveď so stavom „good“. Poskytovateľ monitoruje OCSP responder z hľadiska žiadostí obsahujúcich sériové čísla, ktoré neboli vydané danou CA, ako súčasť svojich bezpečnostných procesov súvisiacich s OCSP.

### 4.9.11 Iné formy oznamovania zrušenia
Žiadne ustanovenia.

### 4.9.12 Špeciálne požiadavky pri kompromitácii kľúča
Kompromitácia súkromného kľúča certifikačných autorít (koreňovej a podriadenej) prevádzkovaných Poskytovateľom (pozri časť 1.5.1) podľa tejto certifikačnej politiky môže byť nahlásená Poskytovateľovi tretími stranami pomocou kontaktných údajov uvedených v časti 1.5.1 alebo 1.5.2, podľa uváženia oznamovateľa (telefonicky, e-mailom, poštou atď.). Oznamovateľ si tiež môže zvoliť akúkoľvek inú metódu, ktorú považuje za vhodnú pre takéto oznámenie.

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
CRL musí byť k dispozícii na webovom sídle Poskytovateľa (pozri časť 1) a musí byť prístupné cez protokol HTTP na porte 80.
OCSP musí byť k dispozícii na URL špecifikovanej vo vydanom certifikáte a žiadateľ o stav certifikátu musí zaslať požiadavku v súlade s časťou 4.9.10.
Záznamy o zrušení v CRL alebo odpovedi OCSP nebudú odstránené skôr ako po dátume exspirácie zrušeného certifikátu.

### 4.10.2 Dostupnosť služby
Poskytovateľ prevádzkuje a udržiava svoju kapacitu CRL a OCSP so zdrojmi dostatočnými na poskytnutie času odozvy desať sekúnd alebo menej za bežných prevádzkových podmienok.
Distribučné body, na ktorých sú zverejňované CRL, sú dostupné v režime 24x7.
OCSP je dostupné v režime 24x7.

### 4.10.3 Voliteľné funkcie
Žiadne ustanovenia.

## 4.11 Ukončenie odberu
Poskytovanie služieb Držiteľovi certifikátu Poskytovateľom zaniká uplynutím platnosti zmluvy, na základe ktorej bol certifikát vydaný.
Zmluva môže byť ukončená ktoroukoľvek stranou po vzájomnej dohode aj pred jej uplynutím. Ukončenie zmluvy musí mať za následok okamžité zrušenie certifikátu vydaného na základe tejto zmluvy.

## 4.12 Úschova kľúčov (Key Escrow) a obnova

### 4.12.1 Politika a postupy úschovy a obnovy kľúčov
Poskytovateľ nevykonáva úschovu (escrow) ani obnovu súkromného kľúča Odberateľa.

### 4.12.2 Politika a postupy zapuzdrenia a obnovy kľúčov relácie
Žiadne ustanovenia.

# 5.  MANAŽÉRSKE, PREVÁDZKOVÉ A FYZICKÉ KONTROLY
Bezpečnosť Poskytovateľa musí byť založená na súbore bezpečnostných opatrení v oblasti fyzickej bezpečnosti, bezpečnosti objektov, personálnej a prevádzkovej bezpečnosti. Tieto bezpečnostné opatrenia musia byť navrhnuté, zdokumentované a aplikované na základe bezpečnostných pravidiel a schválené manažmentom Poskytovateľa.  
Bezpečnostné opatrenia musia byť dostupné príslušným pracovníkom.  
Poskytovateľ:
* preberá plnú zodpovednosť za súlad svojich činností s postupmi definovanými v bezpečnostnej politike, vrátane ich plnenia svojimi registračnými autoritami;  
* definuje zodpovednosť registračných autorít a zaviaže ich k dodržiavaniu stanovených bezpečnostných opatrení;  
* musí mať zoznam všetkých svojich aktív s ich klasifikáciou z hľadiska vykonaného posúdenia rizík.  

Bezpečnostná politika Poskytovateľa a Súhrn bezpečnostných aktív sa musia v pravidelných intervaloch a vždy pri vykonaní významných zmien preskúmať, aby sa zabezpečila ich kontinuita, vhodnosť, dostatočnosť a účinnosť.  
Manažment Poskytovateľa schvaľuje všetky zmeny, ktoré môžu ovplyvniť úroveň poskytovanej bezpečnosti.  
Nastavenie systémov Poskytovateľa sa musí pravidelne kontrolovať z hľadiska zmien, ktoré ohrozujú bezpečnostnú politiku Poskytovateľa. 

## 5.1 Fyzické bezpečnostné kontroly 

### 5.1.1 Umiestnenie a konštrukcia priestorov 
Technologické zariadenia, v ktorých sa nachádza základná infraštruktúra Poskytovateľa, sa musia nachádzať v chránených priestoroch prístupných len oprávneným osobám a oddelených od ostatných priestorov vhodnými bezpečnostnými prvkami (bezpečnostné dvere, mreže, pevné steny a pod.). Vybavenie Poskytovateľa by malo pozostávať len zo zariadení vyhradených pre funkcie certifikačnej autority a nemalo by slúžiť na žiadny účel, ktorý sa netýka tejto funkcie.

### 5.1.2 Fyzický prístup 
Mechanizmy kontroly prístupu do chránených priestorov Poskytovateľa, napr. do priestorov s najvyššou zónou bezpečnosti, musia byť zabezpečené tak, aby tieto priestory boli chránené bezpečnostným alarmom a boli prístupné len osobám, ktoré sú držiteľmi bezpečnostného tokenu a sú uvedené v zozname osôb oprávnených na vstup do chránených priestorov Poskytovateľa. Zariadenia Poskytovateľa musia byť trvalo chránené pred neoprávneným prístupom, a to aj pred neoprávneným fyzickým prístupom.

### 5.1.3 Napájanie a klimatizácia 
Priestory, v ktorých sa nachádzajú zariadenia Poskytovateľa, musia byť primerane zásobované elektrickou energiou a klimatizované, aby poskytovali spoľahlivé prevádzkové prostredie.

### 5.1.4 Ohrozenie vodou 
Priestory, v ktorých sa nachádzajú zariadenia Poskytovateľa, musia byť umiestnené tak, aby nemohli byť ohrozené vodou z akéhokoľvek zdroja. Ak to nie je úplne možné, musia sa prijať opatrenia na minimalizáciu rizika ohrozenia priestorov vodou.

### 5.1.5 Prevencia a ochrana pred požiarom 
Priestory, v ktorých sa nachádzajú zariadenia Poskytovateľa, musia byť spoľahlivo chránené pred priamymi zdrojmi požiaru a teplom, ktoré by mohlo spôsobiť požiar v priestoroch.

### 5.1.6 Skladovanie médií 
Médiá sa musia skladovať v miestnostiach, ktoré sú chránené proti náhodnému, neúmyselnému poškodeniu (voda, oheň a elektromagnetizmus). Médiá obsahujúce bezpečnostný audit, archív alebo zálohované informácie by sa mali uchovávať na mieste oddelenom od CMA.

### 5.1.7 Likvidácia odpadu 
S odpadom vznikajúcim pri prevádzke Poskytovateľa sa musí nakladať tak, aby nedochádzalo k znečisťovaniu životného prostredia.

### 5.1.8 Zálohovanie mimo pracoviska (Off-site backup) 
V prípade nevratného poškodenia priestorov hlavného miesta, kde sa nachádza infraštruktúra Poskytovateľa, je potrebné mať aspoň kópie najdôležitejších aktív Poskytovateľa zálohované mimo tohto hlavného miesta.

## 5.2 Procesné kontroly 

### 5.2.1 Dôveryhodné roly 
V rámci CA musia byť definované dôveryhodné roly zodpovedné za jednotlivé aspekty dôveryhodných činností, ako napríklad správca systému, bezpečnostný manažér, interný audítor, tvorca politiky atď., ktoré tvoria základ dôvery v celé PKI.  
Zároveň musia byť definované zodpovednosti pre jednotlivé roly.  
Osoby vybrané do rolí, ktoré vyžadujú dôveryhodnosť, musia byť zodpovedné a dôveryhodné.  
Všetky osoby v dôveryhodných rolách nesmú mať žiadny konflikt záujmov, aby sa zabezpečila nestrannosť služieb poskytovaných Poskytovateľa.

### 5.2.2 Počet osôb vyžadovaných na úlohu 
Pre každú úlohu sa určí počet osôb pridelených na vykonanie každej úlohy (pravidlo K z N). 

### 5.2.3 Identifikácia a autentifikácia pre každú rolu 
Každá rola musí mať definovaný spôsob identifikácie a autentifikácie pri prístupe do IS Poskytovateľa.

### 5.2.4 Roly vyžadujúce oddelenie povinností 
Každá rola musí mať stanovené kritériá, ktoré zohľadňujú potrebu oddelenia funkcií z hľadiska samotnej roly, t. j. musia existovať roly, ktoré nemôžu byť vykonávané tými istými osobami. 

## 5.3 Personálne kontroly 
Zamestnanci Poskytovateľa musia byť do dôveryhodnej roly formálne vymenovaní výkonným vedením zodpovedným za bezpečnosť.

### 5.3.1 Požiadavky na kvalifikáciu, skúsenosti a preverenie 
Zamestnanci v dôveryhodných rolách musia spĺňať požiadavky na kvalifikáciu, požiadavky na odbornú prax a mať bezpečnostnú previerku na určenej úrovni, resp. byť v procese žiadosti o bezpečnostnú previerku. Požiadavky na každú rolu sú popísané v samostatných listoch používaných pri nábore nových zamestnancov.  
Osoby v riadiacich pozíciách musia:
* mať príslušné vzdelanie alebo skúsenosti v oblasti dôveryhodných služieb poskytovaných Poskytovateľom;  
* byť oboznámené s bezpečnostnými opatreniami pre bezpečnostné roly;  
* mať skúsenosti s informačnou bezpečnosťou a posudzovaním rizík v rozsahu potrebnom na výkon riadiacich funkcií.  

### 5.3.2 Postupy preverovania minulosti 
Zamestnanec môže byť zaradený do dôveryhodnej roly Poskytovateľa len vtedy, ak má bezpečnostnú previerku na určenej úrovni, t. j. aspoň na stupeň utajenia „Vyhradené“ (Confidential), resp. je v procese žiadosti o takéto preskúmanie. 

### 5.3.3 Požiadavky na odbornú prípravu a postupy 
Pre určité dôveryhodné roly Poskytovateľa môžu byť špecifikované niektoré špeciálne požiadavky na školenia, ktoré by mali byť absolvované pred priradením alebo počas neho. Témy by mali zahŕňať fungovanie softvéru a hardvéru CMA, prevádzkové a bezpečnostné postupy, ustanovenia týchto CP/CPS a tak ďalej.

### 5.3.4 Periodicita a požiadavky na preškoľovanie 
Pre roly, kde sú stanovené požiadavky na absolvovanie predpísaného školenia, je možné určiť potrebu ich opakovania po ukončení primárneho školenia.

### 5.3.5 Periodicita a poradie rotácie pracovných miest 
Pre dôveryhodné roly nie je stanovená žiadna rotácia pracovných miest.

### 5.3.6 Sankcie za neoprávnené konanie 
Akékoľvek zlyhanie zamestnanca, ktorého výsledkom je situácia, ktorá nie je v súlade s ustanoveniami týchto CP/CPS, či už ide o nedbalosť alebo zlý úmysel, bude predmetom príslušného administratívneho a disciplinárneho konania zo strany Poskytovateľa.

### 5.3.7 Kontroly nezávislých dodávateľov 
Ak sú na implementáciu dôveryhodných rolí pridelení nezávislí dodávatelia, musia sa na nich vzťahovať povinnosti a špecifické požiadavky na tieto roly v zmysle časti 5.3 a rovnako podliehajú sankciám uvedeným v bode 5.3.6.

### 5.3.8 Dokumentácia poskytovaná personálu 
Zamestnanci v dôveryhodných rolách musia mať k dispozícii dokumenty potrebné na výkon funkcie, na ktorú sú pridelení, vrátane kópie týchto CP/CPS a všetkej technickej a prevádzkovej dokumentácie nevyhnutnej na zachovanie integrity prevádzky Poskytovateľa.

## 5.4 Postupy protokolovania auditov 
Poskytovateľ musí zaznamenávať a mať k dispozícii všetky dôležité informácie týkajúce sa vydaných certifikátov počas nevyhnutnej doby a to aj po ukončení prevádzky.  
Poskytovateľ musí zaznamenávať presný čas v dôveryhodnej službe týkajúci sa správy kľúčov a synchronizácie hodín. Čas zaznamenaný pre každú udalosť musí byť synchronizovaný s UTC aspoň každých 24 hodín.

### 5.4.1 Typy zaznamenávaných udalostí 
CA zaznamenáva aspoň nasledujúce udalosti.

#### 5.4.1.1 Udalosti životného cyklu certifikátu CA a kľúča, vrátane:
* generovanie kľúča, zálohovanie, uchovávanie, obnova, archivácia a likvidácia;
* žiadosti o certifikát, žiadosti o obnovu a výmenu kľúča (re-key) a zrušenie;
* schválenie a zamietnutie žiadostí o certifikát;
* udalosti správy životného cyklu kryptografických zariadení;
* generovanie zoznamov zrušených certifikátov (CRL);
* podpisovanie odpovedí OCSP (ako je popísané v časti 4.9 a časti 4.10); a
* zavedenie nových profilov certifikátov a vyradenie existujúcich profilov certifikátov.

#### 5.4.1.2 Udalosti správy životného cyklu certifikátu Odberateľa, vrátane:
* žiadosti o certifikát, žiadosti o obnovu a výmenu kľúča a zrušenie;
* všetky overovacie činnosti stanovené v tejto CP a v dokumente CPS danej CA;
* schválenie a zamietnutie žiadostí o certifikát;
* vydávanie certifikátov;
* generovanie zoznamov zrušených certifikátov; a
* podpisovanie odpovedí OCSP (ako je popísané v časti 4.9 a časti 4.10).

#### 5.4.1.3 Bezpečnostné udalosti, vrátane:
* úspešné a neúspešné pokusy o prístup k systému PKI;
* vykonané akcie systému PKI a bezpečnostného systému;
* zmeny bezpečnostného profilu;
* inštalácia, aktualizácia a odstránenie softvéru v systéme certifikátov;
* pády systému, poruchy hardvéru a iné anomálie;
* aktivity firewallu a routera; a
* vstupy do priestorov CA a výstupy z nich.  

Protokolové záznamy MUSIA obsahovať nasledujúce prvky:
* dátum a čas udalosti;
* identitu osoby vykonávajúcej záznam do denníka; a
* popis udalosti.

### 5.4.2 Periodicita spracovania a archivácie auditných protokolov 
Žiadne ustanovenia.

### 5.4.3 Doba uchovávania auditných protokolov 
CA a každá poverená tretia strana uchovávajú po dobu najmenej dvoch (2) rokov:
* záznamy o udalostiach správy životného cyklu certifikátu CA a kľúča (ako je stanovené v časti 5.4.1) po neskoršom výskyte:  
   * zničenia súkromného kľúča CA; alebo
   * zrušenia alebo exspirácie finálneho certifikátu CA v danej sade certifikátov, ktoré majú rozšírenie X.509v3 „basicConstraints“ s poľom „cA“ nastaveným na „true“ a ktoré zdieľajú spoločný verejný kľúč zodpovedajúci súkromnému kľúču CA;  
* záznamy o udalostiach správy životného cyklu certifikátu Odberateľa (ako je stanovené v časti 5.4.1) po exspirácii certifikátu Odberateľa;  
* akékoľvek záznamy o bezpečnostných udalostiach (ako je stanovené v časti 5.4.1) po tom, čo k udalosti došlo.  

### 5.4.4 Ochrana auditného protokolu 
Žiadne ustanovenia.

### 5.4.5 Postup zálohovania auditného protokolu 
Žiadne ustanovenia.

### 5.4.6 Systém akumulácie auditných protokolov 
Žiadne ustanovenia.

### 5.4.7 Oznámenie subjektu, ktorý udalosť spôsobil 
Žiadne ustanovenia.

### 5.4.8 Posudzovanie zraniteľností 
Bezpečnostný program Poskytovateľa musí obsahovať ročné posúdenie rizík, ktoré:
* identifikuje predvídateľné vnútorné a vonkajšie hrozby, ktoré by mohli viesť k neoprávnenému prístupu, zverejneniu, zneužitiu, pozmeneniu alebo zničeniu akýchkoľvek údajov o certifikátoch alebo procesov správy certifikátov;
* posudzuje pravdepodobnosť a potenciálnu škodu týchto hrozieb, pričom berie do úvahy citlivosť údajov o certifikátoch a procesov správy certifikátov; a
* posudzuje dostatočnosť politík, postupov, informačných systémov, technológií a iných opatrení, ktoré má Poskytovateľ zavedené na potlačenie takýchto hrozieb.

## 5.5 Archivácia záznamov 

### 5.5.1 Typy archivovaných záznamov 
Poskytovateľ archivuje všetky auditné protokoly (ako je stanovené v časti 5.4.1).  
Okrem toho Poskytovateľ archivuje:
* dokumentáciu súvisiacu s bezpečnosťou svojich systémov certifikátov, systémov správy certifikátov, systémov koreňových CA a systémov poverených tretích strán; a
* dokumentáciu súvisiacu s overovaním, vydávaním a zrušením žiadostí o certifikát a certifikátov.  

Poskytovateľ musí tiež uchovávať všetky auditné záznamy (logy), písomné záznamy o udalostiach CA (generovanie kľúčov CA, podriadená CA, vydávanie certifikátov TSA a certifikáty OCSP responderov).  
Prezeranie záznamov môže byť umožnené jednotlivým zložkám Poskytovateľa plne v kompetencii PMA a osobám vykonávajúcim audit zhody.

### 5.5.2 Doba uchovávania archívu 
Poskytovateľ je povinný uchovávať zmluvu s Držiteľom a/alebo Odberateľom a potvrdenie o vydaní certifikátu vydaného podľa tejto zmluvy po dobu najmenej 7 rokov od exspirácie certifikátu vydaného podľa tejto zmluvy.  
Poskytovateľ musí archivovať záznamy najmenej po dobu dvoch (2) rokov od času ich vytvorenia, alebo po dobu vyžadovanú na archiváciu podľa časti 5.4.3, podľa toho, čo je dlhšie.  
Okrem toho Poskytovateľ uchováva po dobu najmenej dvoch (2) rokov:
* všetku archivovanú dokumentáciu týkajúcu sa bezpečnosti systémov certifikačnej autority, systémov správy certifikátov a systémov koreňových CA,
* všetku archivovanú dokumentáciu týkajúcu sa overovania žiadostí o vydanie a zrušenie certifikátov a samotné certifikáty.

### 5.5.3 Ochrana archívu 
Žiadne ustanovenia.

### 5.5.4 Postupy zálohovania archívu 
Žiadne ustanovenia.

### 5.5.5 Požiadavky na časové pečiatkovanie záznamov 
Žiadne ustanovenia.

### 5.5.6 Systém zberu archívu (interný alebo externý) 
Žiadne ustanovenia.

### 5.5.7 Postupy na získanie a overenie archívnych informácií 
Žiadne ustanovenia.

## 5.6 Výmena kľúčov 
Poskytovateľ musí používať svoje podpisové (súkromné) kľúče len na účel, na ktorý sú určené. Súkromné kľúče podriadenej CA môžu byť použité len na podpisovanie certifikátov koncových používateľov, a to len na účel, na ktorý sú určené, alebo na podpisovanie certifikátov vydaných na technické účely (napr. certifikáty OCSP responderov).  
Súkromný kľúč koreňovej CA môže byť použitý len na podpisovanie certifikátov pre podriadené CA a/alebo technických certifikátov (napr. certifikáty OCSP responderov).

## 5.7 Kompromitácia a obnova po havárii 

### 5.7.1 Postupy pri incidentoch a kompromitácii 
Poskytovateľ musí mať vypracovaný plán odozvy na incidenty a plán obnovy po havárii.  
Poskytovateľ zdokumentuje postupy kontinuity činností a obnovy po havárii navrhnuté tak, aby informovali a primerane chránili dodávateľov aplikačného softvéru, Odberateľov a spoliehajúce sa strany v prípade havárie, kompromitácie bezpečnosti alebo zlyhania podnikania. Poskytovateľ nie je povinný verejne zverejňovať svoje plány kontinuity činností, ale na požiadanie sprístupní svoj plán kontinuity činností a bezpečnostné plány audítorom Poskytovateľa. Poskytovateľ tieto postupy každoročne vyhodnocuje, preskúmava a aktualizuje.  
Plán kontinuity činností obsahuje:
1. podmienky pre aktiváciu plánu;
2. núdzové postupy;
3. náhradné postupy;
4. postupy pre obnovenie činnosti;
5. plán údržby pre samotný plán;
6. požiadavky na povedomie a vzdelávanie;
7. zodpovednosti jednotlivcov;
8. cieľový čas obnovy (RTO);
9. pravidelné testovanie pohotovostných plánov;
10. plán CA na udržanie alebo obnovenie obchodných operácií CA v včasnom termíne po prerušení alebo zlyhaní kritických obchodných procesov;
11. požiadavku na uloženie kritických kryptografických materiálov (t. j. bezpečné kryptografické zariadenie a aktivačné materiály) na náhradnom mieste;
12. čo predstavuje prijateľný výpadok systému a čas obnovy;
13. ako často sa vykonávajú záložné kópie nevyhnutných obchodných informácií a softvéru;
14. vzdialenosť zariadení na obnovu od hlavného miesta CA; a
15. postupy na zabezpečenie svojho zariadenia v maximálnej možnej miere počas obdobia po havárii a pred obnovením bezpečného prostredia buď na pôvodnom, alebo na vzdialenom mieste.

### 5.7.2 Postupy obnovy v prípade poškodenia výpočtových zdrojov, softvéru a/alebo údajov 
Žiadne ustanovenia.

### 5.7.3 Postupy obnovy po kompromitácii kľúča 
Žiadne ustanovenia.

### 5.7.4 Schopnosti kontinuity činností po havárii 
Žiadne ustanovenia.

## 5.8 Ukončenie činnosti CA alebo RA 
Ak Poskytovateľ ukončí svoju činnosť z iných dôvodov než v dôsledku udalostí vyššej moci (napr. prírodná katastrofa, vojnový stav, rozhodnutie verejného orgánu atď.), postupuje sa podľa postupu stanoveného v časti 5.7.

Pred ukončením poskytovania služieb Poskytovateľ musí:

* vhodným spôsobom, najmenej 6 mesiacov vopred, oznámiť dozornému orgánu, Držiteľom všetkých platných certifikátov, ktoré vydal, Spoliehajúcim sa stranám a verejnosti plánované ukončenie svojej činnosti. Toto oznámenie musí byť vykonané prostredníctvom webového sídla Poskytovateľa, e-mailu, bežnej pošty, registračných autorít a/alebo elektronických médií a tlače.
* ukončiť všetky mandátne zmluvy, poverenia, plnomocenstvá atď., na základe ktorých by mohli za Poskytovateľa konať iné právnické osoby.
* uzavrieť dohodu s inou CA na zabezpečenie kontinuity pri poskytovaní dôveryhodných služieb, ak je to možné.
* v súlade s pokynmi PMA zhromaždiť a pripraviť na archiváciu všetky dokumenty súvisiace s poskytovanými dôveryhodnými službami.
* vykonať kontrolu súladu s predpismi o ochrane osobných údajov [14].
* vyradiť z prevádzky všetky súkromné kľúče vrátane všetkých ich kópií takým spôsobom, aby ich nebolo možné žiadnym spôsobom obnoviť.  

Po ukončení svojej činnosti Poskytovateľ nebude vydávať žiadne certifikáty a preukázateľne zabezpečí, aby súkromné kľúče Poskytovateľa nemohli byť opätovne použité.  
Pred ukončením svojej činnosti každá RA poskytne archivované údaje určenej jednotke Poskytovateľa v súlade s pokynmi PMA.  
Poskytovateľ musí mať zavedené riešenie na pokrytie všetkých nákladov spojených so splnením minimálnych požiadaviek na ukončenie v prípade bankrotu alebo inej príčiny, kedy nebude schopný pokryť náklady z vlastných zdrojov, v súlade s platnou legislatívou o bankrote.

# 6.   TECHNICKÉ BEZPEČNOSTNÉ KONTROLY
Technická časť infraštruktúry Poskytovateľa (hardvér a softvér) musí pozostávať len z bezpečných systémov a oficiálneho softvéru. Architektúra infraštruktúry Poskytovateľa musí byť navrhnutá z komponentov, ktoré spĺňajú bezpečnostné štandardy na úrovni súčasných poznatkov.  
Osobitná pozornosť sa musí venovať kryptografickému modulu (HSM), ktorý slúži na generovanie, uchovávanie a používanie súkromných kľúčov Poskytovateľa a je jedným z najzraniteľnejších aktív. Súkromné kľúče Poskytovateľa musia byť uložené v module HSM, ktorý je certifikovaný aspoň podľa štandardu FIPS 140-2 Level 3.  
Poskytovateľ musí použiť kombináciu fyzických, logických a procesných opatrení na zabezpečenie svojej bezpečnosti pri ochrane svojho súkromného kľúča.  
Systém Poskytovateľa musí obsahovať zariadenie na nepretržitú detekciu, monitorovanie a signalizáciu neoprávnených a neobvyklých pokusov o prístup k jeho zdrojom.  
Aplikácie na zverejňovanie musia poskytovať kontrolu prístupu pred pokusom o pridanie alebo vymazanie certifikátu alebo modifikáciu iných súvisiacich údajov.  
Hlásenie stavu zrušenia musí poskytovať kontrolu prístupu pred pokusmi o modifikáciu informácií o stave zrušenia.  
Všetky funkcie Poskytovateľa, ktoré využívajú počítačovú sieť, musia byť zabezpečené proti neoprávnenému prístupu a iným škodlivým aktivitám.


## 6.1 Generovanie a inštalácia páru kľúčov

### 6.1.1 Generovanie páru kľúčov

#### 6.1.1.1 Generovanie páru kľúčov CA
Generovanie a inštalácia páru kľúčov Poskytovateľa sa musí vykonať štandardizovaným spôsobom, ktorý je podrobne popísaný v dokumentácii Poskytovateľa v súlade s požiadavkami v časti 6.1.1.1 dokumentu SMIME BR [1].  
Metóda generovania musí poskytovať dostatočnú istotu v postupe generovania a celý proces musí byť písomne zaznamenaný. Generovanie kľúčov musia vykonávať autorizované osoby Poskytovateľa priradené k rolám, ktoré sú oprávnené zúčastniť sa ceremoniálu generovania kľúčov a žiadostí. Generovanie kľúčov sa musí vykonať v bezpečnom zariadení na uchovávanie kryptografických kľúčov.

Pre páry kľúčov určené pre operátora koreňovej CA (Root CA) musí Poskytovateľ:
* pripraviť a dodržiavať scenár (script) na generovanie páru kľúčov,
* zabezpečiť buď:
  * že pár kľúčov je generovaný v prítomnosti kvalifikovaného audítora, alebo
  * že celý proces generovania páru kľúčov je zaznamenaný na video pre následné preskúmanie audítorom.

Poskytovateľ musí ďalej zabezpečiť, že:
* generuje pár kľúčov CA v fyzicky zabezpečenom prostredí, ako je opísané v týchto CP/CPS, pri uplatnení princípu K z N;
* generuje pár kľúčov CA pomocou osôb v dôveryhodných rolách podľa princípov viacosobovej kontroly a rozdelenia znalostí – princíp K z N;
* generuje pár kľúčov CA v rámci kryptografických modulov, ktoré spĺňajú príslušné technické a komerčné požiadavky stanovené v týchto CP/CPS;
* zaznamenáva činnosti generovania páru kľúčov CA; a
* udržiava účinné kontroly na poskytnutie primeranej istoty, že súkromný kľúč bol vygenerovaný a chránený v súlade s postupmi opísanými v týchto CP/CPS a prípadne v jeho scenári generovania kľúčov.

#### 6.1.1.2 Generovanie páru kľúčov RA
Žiadne ustanovenia.

#### 6.1.1.3 Generovanie páru kľúčov Odberateľa
RA Poskytovateľa musí zamietnuť žiadosť o vydanie certifikátu, ak je splnená jedna alebo viacero z nasledujúcich podmienok:
* pár kľúčov nespĺňa požiadavky stanovené v časti 6.1.5 a/alebo časti 6.1.6;
* existuje jasný dôkaz, že metóda použitá na generovanie páru kľúčov je chybná;
* Poskytovateľ bol informovaný, že súkromný kľúč bol kompromitovaný, napríklad spôsobom opísaným v časti 4.9.1.1.

RA Poskytovateľa negeneruje pár kľúčov v mene Držiteľa.

### 6.1.2 Doručenie súkromného kľúča Odberateľovi
Iné strany ako Odberateľ nesmú archivovať súkromný kľúč Odberateľa bez autorizácie Odberateľom.

Ak sa CA alebo ktorákoľvek z jej určených RA dozvie, že súkromný kľúč Odberateľa bol sprístupnený osobe alebo organizácii, ktorá nie je autorizovaná Odberateľom, potom CA zruší všetky certifikáty, ktoré obsahujú verejný kľúč zodpovedajúci sprístupnenému súkromnému kľúču.

### 6.1.3 Doručenie verejného kľúča vydavateľovi certifikátu
Žiadne ustanovenia.

### 6.1.4 Doručenie verejného kľúča CA spoliehajúcim sa stranám
Žiadne ustanovenia.

### 6.1.5 Veľkosti kľúčov
Pre páry kľúčov RSA Poskytovateľ:
* zabezpečí, aby veľkosť modulu (modulus) pri zakódovaní bola aspoň 2048 bitov; a
* zabezpečí, aby veľkosť modulu v bitoch bola rovnomerne deliteľná 8.


### 6.1.6 Generovanie parametrov verejného kľúča a kontrola kvality
Parametre a kvalita verejných kľúčov Poskytovateľa (koreňové a podriadené CA, krížové certifikáty) sú určované PMA a kontrola kvality sa vykonáva počas ceremoniálu generovania kľúčov. Poskytovateľ musí na generovanie a uchovávanie kľúčov používať hardvérové kryptografické moduly, ktoré spĺňajú požiadavky FIPS 186-2, čím sa zabezpečí náhodné generovanie kľúčov RSA s minimálnou veľkosťou 2048 bitov.

Pre pár kľúčov RSA musí Poskytovateľ potvrdiť, že hodnota verejného exponentu je nepárne číslo rovné 3 alebo viac. Okrem toho by mal byť verejný exponent v rozsahu medzi 2^16 + 1 a 2^256 − 1. Modul by mal mať tiež nasledujúce charakteristiky: je to nepárne číslo, nie mocnina prvočísla a nemá žiadne faktory menšie ako 752 (pozri NIST SP 800-89, časť 5.3.3) [18].


### 6.1.7 Účely použitia kľúčov (podľa poľa key usage v X.509 v3)
Súkromné kľúče zodpovedajúce certifikátom koreňovej CA sa nesmú používať na podpisovanie certifikátov okrem nasledujúcich prípadov:
* self-signed certifikáty na reprezentáciu samotnej koreňovej CA;
* certifikáty pre podriadené CA a krížové certifikáty;
* certifikáty na infraštruktúrne účely (certifikáty administratívnych rolí, certifikáty interných prevádzkových zariadení CA); a
* certifikáty na overenie odpovede OCSP.

## 6.2 Ochrana súkromného kľúča a inžinierstvo kryptografického modulu
Poskytovateľ zavedie fyzické a logické zábrany na zabránenie neoprávnenému vydávaniu certifikátov. Ochrana súkromného kľúča CA mimo vyššie uvedeného validovaného systému alebo zariadenia musí pozostávať z fyzickej bezpečnosti, šifrovania alebo kombinácie oboch, implementovaných spôsobom, ktorý zabráni odhaleniu súkromného kľúča.

Poskytovateľ zašifruje svoj súkromný kľúč algoritmom a dĺžkou kľúča, ktoré sú podľa súčasného stavu techniky schopné odolať kryptoanalytickým útokom počas zostávajúcej životnosti šifrovaného kľúča alebo jeho časti.

### 6.2.1 Štandardy a kontroly kryptografického modulu
Poskytovateľ musí na ochranu svojich súkromných kľúčov (koreňové CA, podriadené CA) používať hardvérové kryptografické moduly certifikované aspoň na úrovni FIPS 140-2 Level 3. Moduly musia byť uložené v zabezpečených priestoroch prístupných len osobám v dôveryhodných rolách.
Súkromné kľúče Poskytovateľa sa môžu používať výhradne na podpisovanie certifikátov a zoznamov CRL vydaných Poskytovateľom.

Vybavenie CA musí byť nepretržite chránené proti neoprávnenému prístupu, vrátane neoprávneného fyzického prístupu.
HSM modul musí poskytovať ochranu proti zachyteniu elektromagnetických emisií.

Súkromné kľúče CA Poskytovateľa:
* sú uložené a používané výhradne v rámci HSM, ktorý spĺňa príslušné bezpečnostné požiadavky;
* sú aktivované len autorizovaným personálom v režime kontroly K z N;
* nikdy sa neexportujú z HSM v nezašifrovanej forme.

### 6.2.2 Kontrola súkromného kľúča viacerými osobami (K z N)
Pri operáciách zahŕňajúcich súkromné kľúče Poskytovateľa (napr. generovanie, zálohovanie, likvidácia) musí byť vždy prítomný požadovaný počet autorizovaných osôb v súlade s princípom „K z N“.

### 6.2.3 Úschova súkromného kľúča (Private key escrow)
Žiadne ustanovenia.

### 6.2.4 Zálohovanie súkromného kľúča
Súkromné kľúče Poskytovateľa musia byť generované a uložené v hardvérových kryptografických moduloch. Tam, kde je prenos nevyhnutný na účely zálohovania a obnovy, súkromné kľúče musia byť vždy prenášané v zašifrovanej forme. Prenos súkromných kľúčov a ich obnova do iného hardvérového kryptografického modulu môžu vykonávať len autorizovaní zamestnanci v súlade s pravidlami stanovenými v časti 6.2.2.

### 6.2.5 Archivácia súkromného kľúča
Iné strany ako Poskytovateľ nesmú archivovať súkromné kľúče podriadenej CA bez autorizácie Poskytovateľom.

### 6.2.6 Prenos súkromného kľúča do alebo z kryptografického modulu
Ak vydávajúca CA Poskytovateľa vygenerovala súkromný kľúč v mene podriadenej CA, potom vydávajúca CA zašifruje súkromný kľúč pre prenos do podriadenej CA.

Ak sa vydávajúca CA dozvie, že súkromný kľúč podriadenej CA bol sprístupnený neoprávnenej osobe alebo organizácii, ktorá nie je pridružená k podriadenej CA, potom vydávajúca CA zruší všetky certifikáty, ktoré obsahujú verejný kľúč zodpovedajúci sprístupnenému súkromnému kľúču.

### 6.2.7 Uloženie súkromného kľúča v kryptografickom module
Poskytovateľ chráni svoj súkromný kľúč v systéme alebo zariadení, ktoré bolo validované ako spĺňajúce aspoň FIPS 140-2 level 3, FIPS 140-3 level 3, alebo príslušný Common Criteria Protection Profile alebo Security Target, EAL 4 (alebo vyšší), ktorý zahŕňa požiadavky na ochranu súkromného kľúča a iných aktív proti známym hrozbám.

### 6.2.8 Metóda aktivácie súkromného kľúča
Súkromné kľúče Poskytovateľa môžu byť aktivované len autorizovanými osobami v súlade s časťou 6.2.2.

Počas aktivácie musí každá autorizovaná osoba, z požadovaného počtu autorizovaných osôb, vložiť svoju čipovú kartu do modulu HSM a zadať zodpovedajúce heslo.

Držitelia certifikátov, ktorým Poskytovateľ vydal certifikát pre príslušný verejný kľúč, sú výhradne zodpovední za ochranu svojich súkromných kľúčov. Poskytovateľ musí všetkým Držiteľom certifikátov odporučiť, aby si chránili svoje súkromné kľúče použitím silného hesla, aby zabránili zneužitiu svojho súkromného kľúča.

### 6.2.9 Metóda deaktivácie súkromného kľúča
Deaktiváciu súkromného kľúča v module HSM môže vykonať len autorizovaná osoba (administrátor CA), alebo kľúče môžu byť deaktivované automaticky po ukončení relácie alebo strate elektrického napájania modulu HSM.

### 6.2.10 Metóda likvidácie súkromného kľúča
Poskytovateľ musí prostredníctvom technických a organizačných opatrení zabezpečiť, aby súkromný kľúč Poskytovateľa nebolo možné po skončení jeho životného cyklu použiť. O ukončení životného cyklu súkromného kľúča CA a prijatých technických a organizačných opatreniach musí byť vyhotovený záznam podpísaný všetkými prítomnými aktérmi.

### 6.2.11 Hodnotenie kryptografického modulu
Žiadne ustanovenia.

## 6.3 Ostatné aspekty správy párov kľúčov

### 6.3.1 Archivácia verejného kľúča
Žiadne ustanovenia.

### 6.3.2 Prevádzkové obdobia certifikátu a obdobia používania páru kľúčov
Platnosť certifikátu vydaného Poskytovateľom a použiteľnosť páru kľúčov nesmie presiahnuť nasledujúce:
| Typ certifikátu | Platnosť (minimum) | Platnosť (maximum) |
| :--- | :---: | :---: |
| Koreňová CA (Root CA) | 2922 dní | 9132 dní |
| Podriadená CA (Subordinate CA) | 1825 dní | 2560 dní |
| STRICT alebo MULTIPURPOSE S/MIME certifikát | - | 825 dní |

Na účely výpočtov sa deň meria ako 86 400 sekúnd. Akékoľvek množstvo času väčšie ako toto, vrátane zlomkov sekúnd a/alebo priestupných sekúnd, predstavuje ďalší deň.


## 6.4 Aktivačné údaje
### 6.4.1 Generovanie a inštalácia aktivačných údajov
Aktivačné údaje pre súkromný kľúč pracovníka RA si volí pracovník RA sám ihneď po prevzatí zariadenia, pred jeho prvým použitím na prístup k IS Poskytovateľa cez aplikáciu RA Client.

### 6.4.2 Ochrana aktivačných údajov
Pracovník RA je výhradne zodpovedný za ochranu súkromných kľúčov pracovníka RA.

Pri vydávaní certifikátu je každý pracovník RA informovaný zodpovednou osobou Poskytovateľa o potrebe chrániť súkromný kľúč silným heslom, aby sa zabránilo jeho zneužitiu počas celého obdobia jeho používania.

### 6.4.3 Ostatné aspekty aktivačných údajov
Žiadne ustanovenia.

## 6.5 Počítačové bezpečnostné kontroly

### 6.5.1 Špecifické technické požiadavky na počítačovú bezpečnosť
Poskytovateľ musí vykonávať všetky funkcie poskytovateľa dôveryhodných služieb pomocou dôveryhodného systému, ktorý spĺňa požiadavky definované v bezpečnostnom projekte informačného systému Poskytovateľa.

Poskytovateľ vydávajúci certifikáty musí spĺňať špecifické požiadavky na informačnú bezpečnosť pre poskytovateľa dôveryhodných služieb definované v ETSI EN 319 411-1 [6].

Všetky systémy musia byť pravidelne kontrolované na prítomnosť škodlivého kódu a chránené proti spywaru a vírusom.
Poskytovateľ implementoval viacfaktorovú autentifikáciu pre všetkých pracovníkov RA, ktorí sú schopní priamo spôsobiť vydanie certifikátu.

### 6.5.2 Hodnotenie počítačovej bezpečnosti
Žiadne ustanovenia.

## 6.6 Technické kontroly životného cyklu

### 6.6.1 Kontroly vývoja systému
Žiadne ustanovenia.

### 6.6.2 Kontroly správy bezpečnosti
Žiadne ustanovenia.

### 6.6.3 Kontroly bezpečnosti životného cyklu
Žiadne ustanovenia.

## 6.7 Kontroly sieťovej bezpečnosti
Požiadavky CA/Browser fóra „Network and Certificate System Security Requirements“ [19] sú zahrnuté odkazom, akoby boli v plnom rozsahu uvedené v tomto dokumente.

## 6.8 Časové pečiatkovanie
Žiadne ustanovenia.

# 7. PROFILY CERTIFIKÁTOV, CRL A OCSP

## 7.1 Profil certifikátu
Poskytovateľ musí spĺňať technické požiadavky stanovené v časti 2.2, časti 6.1.5 a časti 6.1.6.

Poskytovateľ musí generovať nesekvenčné sériové čísla certifikátov väčšie ako nula (0) a menšie ako 2^159, ktoré obsahujú aspoň 64 bitov výstupu.

### 7.1.1 Číslo verzie
Tieto CP/CPS povoľujú iba vydávanie certifikátov zodpovedajúcich štandardu X.509 verzie 3.

### 7.1.2 Obsah a rozšírenia certifikátu; aplikácia RFC 6818
Táto časť špecifikuje dodatočné požiadavky na obsah certifikátu a rozšírenia certifikátov, pričom zohľadňuje znenie RFC 6818 [20].

#### 7.1.2.1 Certifikáty koreňovej CA (Root CA)
Algoritmy a dĺžky kľúčov aplikované v koreňovom certifikáte Poskytovateľa:

| | |
| :--- | :--- |
| Názov algoritmu podpisu:|**sha256RSA**|
| Verejný kľúč:|**RSA, dĺžka 4 096 bitov**|

Tabuľka 4: Obsah položiek v koreňovom certifikáte Poskytovateľa

|Skratka názvu|OID     |Názov       |Obsah |
|:-----:   |:------:|:---------:|:-------:|
|C         |2.5.4.6 |countryName|SK       |
|L         |2.5.4.7 |localityName|Bratislava|
|O         |2.5.4.10|organizationName|Disig a.s.|
|CN        |2.5.4.3 |commonName  |depending on the CA type ¹ |

¹ CN musí obsahovať obchodné meno certifikačnej autority, t. j. CA Disig doplnené podľa potreby o koreňové rozlišovacie meno CA Disig, napr. Root R4 atď.

Tabuľka 5: Rozšírenia certifikátu v certifikátoch koreňovej CA

| Rozšírenie / OID | Prítomnosť | Kritické |
|:---|:---:|:---:|
| basicConstraints / 2.5.29.19 | ÁNO | ÁNO |
| keyUsage / 2.5.29.15 | ÁNO | ÁNO |
| subjectKeyIdentifier / 2.5.29.14 | ÁNO | NIE |

#### 7.1.2.2 Podriadená certifikačná autorita Poskytovateľa

Algoritmy a dĺžky kľúčov použité v podriadenej CA:

|  | |
| :--- | :--- |
| Názov algoritmu podpisu:|**sha256RSA**|
| Verejný kľúč:|**RSA, minimálna dĺžka 2 048 bit**|
| Platnosť podriadenej CA:|maximálne 7 rokov|

Tabuľka 6: Obsah položiek v SMIME certifikáte podriadenej CA

|Skratka názvu |OID|Názov|Obsah|
|:----------:|:---:|:----:|:-------:|
|C|2.5.4.6|countryName|SK|
|L|2.5.4.7|localityName|Bratislava|
|O|2.5.4.10|organizationName|Disig a.s.|
|CN|2.5.4.3|commonName|depending on the CA type ²|

² ² CN musí obsahovať obchodné meno certifikačnej autority, napr. CA Disig doplnené o rozlišovacie meno, napr. R4I1 SMIME Certification Service atď.
 

Tabuľka 7: Rozšírenia certifikátov v podriadenej CA  

|Rozšírenie / OID|Prítomnosť|Kritickosť|
|---------------|:--------:|:--------:|
|certificatePolicies / 2.5.29.32|ÁNO|NIE|
|crlDistributionPoints / 2.5.29.31|ÁNO|NIE|
|authorityInfoAccess / 1.3.6.1.5.5.7.1.1|ÁNO (MÁ BYŤ)|NIE| 
|basicConstraints / 2.5.29.19|ÁNO|ÁNO|
|keyUsage / 2.5.29.15|ÁNO|ÁNO|
|extKeyUsage / 2.5.29.37|ÁNO|NIE|
|authorityKeyIdentifier / 2.5.29.35|ÁNO|NIE| 
|subjectKeyIdentifier / 2.5.29.14|ÁNO|NIE|

Rozšírenie cRLDistributionPoints obsahuje HTTP URL adresu služby CRL danej CA, ako je špecifikované v časti 2.2.3 týchto CP/CPS.

#### 7.1.2.3 Certifikáty Odberateľov
Podrobnosti o obsahu rozlišovacieho mena (DN) každého typu certifikátu vydávaného podľa týchto CP/CPS nájdete v časti 7.1.4.2.

Rozšírenia použité vo všetkých typoch vydaných certifikátov sú uvedené v tabuľke 8.

Tabuľka 8: Základné rozšírenia v certifikátoch Odberateľov  
|Názov rozšírenia / <br>ASN.1 názov a OID|Popis|Prítomnosť|Kritické |
|-----------------------------|:---------|:------:|:-------:|
|Certificate Policies<br>{id-ce-certificatePolicies}<br>{2.5.29.32}|Musí obsahovať presne jeden z vyhradených policyIdentifiers uvedených v časti 7.1.6.1.|MUSÍ BYŤ|NIE|
|CRL Distribution Points<br>{id-ce-CRLDistributionPoints}<br>{2.5.29.31}|Profily Strict a Multipurpose musia obsahovať aspoň jeden distributionPoint, <br> ktorého hodnota fullName obsahuje GeneralName typu uniformResourceIdentifier, <br> ktorý zahŕňa URI, kde je možné získať CRL vydávajúcej CA.<br>Každý uniformResourceIdentifier musí mať URI schému HTTP. Iné schémy nesmú byť prítomné.|MUSÍ BYŤ|NIE|
|AuthorityInfoAccess<br>{id-pe-authorityInfoAccess}<br>{1.3.6.1.5.5.7.1.1}|1. id-ad-ocsp<br> Rozšírenie môže obsahovať jednu alebo viac hodnôt accessMethod typu id-ad-ocsp, ktoré špecifikujú URI<br> OCSP respondera vydávajúcej CA. Profily Strict a Multipurpose musia mať pre každú accessMethod<br> URI schému HTTP. Iné schémy nesmú byť prítomné.<br> 2. id-ad-caIssuers<br> Rozšírenie by malo obsahovať aspoň jednu hodnotu accessMethod typu id-ad-caIssuers, ktorá špecifikuje<br> URI certifikátu vydávajúcej CA. Profily Strict a Multipurpose musia mať pre každú accessMethod<br> URI schému HTTP. Iné schémy nesmú byť prítomné.|MÁ BYŤ|NIE|
|basicConstraints<br>{id-ce-basicConstraints}<br>{2.5.29.19}|Toto rozšírenie môže byť prítomné. Pole cA nesmie byť true. Pole pathLenConstraint nesmie byť prítomné.|MÁ BYŤ|NIE|
|Key Usage<br>{id-ce-keyUsage}<br>{2.5.29.15}|Profil Strict: Len pre podpisovanie musia byť nastavené bity pre digitalSignature a môžu byť nastavené<br> pre nonRepudiation. Len pre správu kľúčov musia byť nastavené bity pre keyEncipherment.<br> Pre duálne použitie musia byť nastavené bity pre digitalSignature a keyEncipherment a môžu byť<br> nastavené pre nonRepudiation.<br> Profil Multipurpose: platí rovnako ako pre profil Strict s modifikáciou, že pre správu<br> kľúčov a duálne použitie môže byť nastavený bit pre dataEncipherment. Iné bity nesmú byť nastavené.|MUSÍ BYŤ|MÁ BYŤ|
|Extended Key Usage<br>{id-ce-extKeyUsage}<br>{2.5.29.37}|Profil Strict: id-kp-emailProtection musí byť prítomný. Iné hodnoty nesmú byť prítomné.<br>Profil Multipurpose: id-kp-emailProtection musí byť prítomný. Iné hodnoty môžu byť prítomné.<br>Akýkoľvek profil: Hodnoty id-kp-serverAuth, id-kp-codeSigning, id-kp-timeStamping,<br> a anyExtendedKeyUsage nesmú byť prítomné.|MUSÍ BYŤ|NIE|
|Authority Key Identifier<br>{id-ce-authorityKeyIdentifier}<br>{2.5.29.35}|Pole keyIdentifier musí byť prítomné. Polia authorityCertIssuer a authorityCertSerialNumber<br> nesmú byť prítomné.|MUSÍ BYŤ|NIE|
|subjectAltName<br>id-ce-subjectAltName<br>{2.5.29.32}|Hodnota tohto rozšírenia musí byť zakódovaná podľa špecifikácie v časti 7.1.4.2.1.|MUSÍ BYŤ|NIE|
|Subject Key Identifier<br>{id-ce-subjectKeyIdentifier}<br>{2.5.29.14}|Malo by obsahovať hodnotu, ktorá je odvodená od verejného kľúča zahrnutého v certifikáte Odberateľa.|MÁ BYŤ|NIE|

#### 7.1.2.4 Všetky certifikáty
Všetky polia a rozšírenia musia byť nastavené v súlade s RFC 5280 [2]. Poskytovateľ nevydá certifikát, ktorý obsahuje príznak keyUsage, hodnotu extKeyUsage, rozšírenie certifikátu alebo iné údaje, ktoré nie sú špecifikované v častiach 7.1.2.1, 7.1.2.2 alebo 7.1.2.3, pokiaľ si Poskytovateľ nie je vedomý dôvodu na zahrnutie týchto údajov do certifikátu. 
Ak Poskytovateľ zahrnie do certifikátu polia alebo rozšírenia, ktoré nie sú špecifikované, ale sú inak povolené týmito požiadavkami, potom Poskytovateľ vo svojich CP/CPS zdokumentuje procesy a postupy, ktoré používa na validáciu informácií obsiahnutých v takýchto poliach a rozšíreniach.

Poskytovateľ nevydá certifikát s:
* Rozšíreniami, ktoré sa neaplikujú v kontexte verejného internetu. 
* Hodnotami polí alebo rozšírení, ktoré neboli validované podľa procesov a postupov opísaných v týchto CP/CPS.

### 7.1.3 Identifikátory objektov algoritmov (Algorithm object identifiers)

#### 7.1.3.1 SubjectPublicKeyInfo
Nasledujúce požiadavky sa vzťahujú na pole „subjectPublicKeyInfo“ v rámci certifikátu. Žiadne iné kódovania nie sú povolené.

##### 7.1.3.1.1 RSA
Poskytovateľ označí kľúč RSA pomocou identifikátora algoritmu „rsaEncryption (OID: 1.2.840.113549.1.1.1)“. Parametre musia byť prítomné a musia byť explicitné „NULL“.

Poskytovateľ nesmie použiť iný algoritmus, ako napríklad identifikátor algoritmu „id-RSASSA-PSS (OID: 1.2.840.113549.1.1.10)“, na označenie kľúča RSA.

Pri zakódovaní musí byť AlgorithmIdentifier pre kľúče RSA bajt po bajte identický s nasledujúcimi hexadecimálne kódovanými bajtmi: 300d06092a864886f70d0101010500

##### 7.1.3.1.2 ECDSA
Poskytovateľ nevydáva certifikáty pre tento typ kľúčov.

##### 7.1.3.1.3 EdDSA
Poskytovateľ nevydáva certifikáty pre tento typ kľúčov.

##### 7.1.3.2 Signature AlgorithmIdentifier
Všetky objekty podpísané súkromným kľúčom CA musia spĺňať tieto požiadavky na používanie „AlgorithmIdentifier“ alebo typu odvodeného od „AlgorithmIdentifier“ v kontexte podpisov.

Konkrétne sa to vzťahuje na všetky nasledujúce objekty a polia:
* Pole „signatureAlgorithm“ certifikátu.
* Pole „signature“ v „TBSCertificate“ (napríklad ako sa používa v certifikáte).
* Pole „signatureAlgorithm“ v „CertificateList“.
* Pole „signature“ v „TBSCertList“.
* Pole „signatureAlgorithm“ v „BasicOCSPResponse“.

Pre tieto polia nie sú povolené žiadne iné kódovania.

##### 7.1.3.2.1 RSA
CA poskytovateľa použije jeden z nasledujúcich podpisových algoritmov a kódovaní. Pri zakódovaní musí byť „AlgorithmIdentifier“ bajt po bajte identický so špecifikovanými hexadecimálne kódovanými bajtmi.
|AlgorithmIdentifier|Kódovanie|
|-------------------------------|:---------|
|RSASSA-PKCS1-v1_5 s SHA-256|300d06092a864886f70d01010b0500|
|RSASSA-PKCS1-v1_5 s SHA-384|300d06092a864886f70d01010c0500|
|RSASSA-PKCS1-v1_5 s SHA-512|300d06092a864886f70d01010d0500|
|RSASSA-PSS s SHA-256, <br>MGF-1 s SHA-256 a<br> dĺžkou soli (salt) 32 bajtov|304106092a864886f70d01010a3034a00<br>f300d06096086480165030402010500a11<br>c301a06092a864886f70d010108300d0<br>6096086480165030402010500a203020120|
|RSASSA-PSS s SHA-384, <br>MGF-1 s SHA-384 a<br>dĺžkou soli 48 bajtov|304106092a864886f70d01010a3034a00<br>f300d06096086480165030402020500a11<br>c301a06092a864886f70d010108300d06096<br>086480165030402020500a203020130|
|RSASSA-PSS s SHA-512, <br>MGF-1 s SHA-512 a<br> dĺžkou soli 64 bajtov|304106092a864886f70d01010a3034a00<br>f300d06096086480165030402030500a11<br>c301a06092a864886f70d010108300d06096<br>086480165030402030500a203020140|

##### 7.1.3.2.2 ECDSA
Poskytovateľ nepoužíva tento typ podpisového algoritmu. 

##### 7.1.3.2.3 EdDSA
Poskytovateľ nepoužíva tento typ podpisového algoritmu. 

### 7.1.4 Formy mien (Name Forms)
Hodnoty atribútov musia byť kódované podľa RFC 5280 [2].

#### 7.1.4.1 Kódovanie mien
Pre každú platnú certifikačnú cestu (ako je definovaná v RFC 5280 [2], časť 6):
* Pre každý certifikát v certifikačnej ceste musí byť zakódovaný obsah poľa „Issuer Distinguished Name“ certifikátu bajt po bajte identický so zakódovanou formou poľa „Subject Distinguished Name“ certifikátu vydávajúcej CA.
* Pre každý certifikát CA v certifikačnej ceste musí byť zakódovaný obsah poľa „Subject Distinguished Name“ certifikátu bajt po bajte identický medzi všetkými certifikátmi, ktorých „Subject Distinguished Names“ sa dajú porovnať ako rovnaké podľa RFC 5280 [2], časť 7.1, a to vrátane exspirovaných a zrušených certifikátov.

#### 7.1.4.2 Informácie o subjekte – certifikáty Odberateľov
Vydaním certifikátu CA Poskytovateľa vyhlasuje, že dodržala postup stanovený v týchto CP/CPS na overenie toho, že k dátumu vydania certifikátu boli všetky informácie o subjekte presné.

Poskytovateľ nezahrnie e-mailovú adresu (Mailbox Address) do polí určených pre e-mail (Mailbox Field) okrem prípadov overených v súlade s časťou 3.2.
Atribúty subjektu nesmú obsahovať iba metadáta, ako sú znaky „.“, „-“ a „ “ (t. j. medzera), a/alebo akúkoľvek inú indikáciu, že hodnota chýba, je neúplná alebo sa nepoužíva.

##### 7.1.4.2.1 Rozšírenie Subject Alternative Name
|Pole certifikátu|Povinné / Voliteľné|Obsah| 
|-------------------------------|:---------:|:---------|
|extensions: subjectAltName|musí byť prítomné|Toto rozšírenie musí obsahovať aspoň jednu položku GeneralName nasledujúcich typov:<br>• Rfc822Name a/alebo <br>• otherName typu id-on-SmtpUTF8Mailbox, kódované v súlade s RFC 8398|

##### 7.1.4.2.2 Polia Subject Distinguished Name
Poskytovateľ vydáva tieto typy S/MIME certifikátov:
* S/MIME certifikát pre digitálny podpis
* Individual-validated (STRICT a MULTIPURPOSE)
* Sponsor-validated (STRICT a MULTIPURPOSE)
* S/MIME digitálny certifikát pre pečať (STRICT a MULTIPURPOSE).

V špecifikovaných typoch certifikátov sú zahrnuté nasledujúce polia Subject Distinguished Name: 

|Pole Subject Distinguished<br> Name | |S/MIME certifikát pre digitálny podpis| | | S/MIME digitálny certifikát pre pečať| |
|-------------------------------|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|
| | Individual-validated| Individual-validated|Sponsor-validated |Sponsor-validated |Organization-validated|Organization-validated |
| |Multipurpose|Strict|Multipurpose|Strict|Multipurpose|Strict|
|commonName |ÁNO|ÁNO|ÁNO|ÁNO|ÁNO|ÁNO|
|givenName |ÁNO|ÁNO|ÁNO|ÁNO| | |
|surname |ÁNO|ÁNO|ÁNO|ÁNO| | |
|serialNumber |ÁNO|ÁNO|ÁNO|ÁNO| | |
|countryName |ÁNO|ÁNO|ÁNO|ÁNO|ÁNO|ÁNO|
|organizationName| | |ÁNO|ÁNO|ÁNO|ÁNO|
|organizationIdentifier| | |ÁNO|ÁNO|ÁNO|ÁNO|
|localityName | | |ÁNO|ÁNO|ÁNO|ÁNO|
|emailAddress |ÁNO|ÁNO|ÁNO|ÁNO|ÁNO|ÁNO|

**a) Pole certifikátu: „_subject:commonName (OID 2.5.4.3)_“** Tento atribút musí obsahovať jednu z nasledujúcich hodnôt overených v súlade s časťou 3.2.
|Typ certifikátu |Obsah |
|----------------------|:------------------------------------------:|
|Organization-validated|subject:organizationName e-mailová adresa schránky |
|Sponsor-validated |Meno osoby, pseudonym alebo e-mailová adresa schránky|
|Individual-validated |Meno osoby, pseudonym alebo e-mailová adresa schránky|

Meno osoby by malo byť uvedené ako „_subject:givenName_“ a/alebo „_subject:surname_“. Meno osoby môže byť v preferovanom formáte zobrazenia Subjektu alebo vo formáte preferovanom CA alebo Enterprise RA, ale musí byť zmysluplným vyjadrením mena Subjektu, ako bolo overené podľa časti 3.2.4.

Ak je prítomná e-mailová adresa schránky (Mailbox Address), musí obsahovať hodnotu rfc822Name alebo otherName typu id-on-SmtpUTF8Mailbox z rozšírenia extensions:subjectAltName.

Podobne ako všetky ostatné atribúty certifikátu, „_subject:commonName_“ a „_subject:emailAddress_“ musia spĺňať horné limity atribútov definované v RFC 5280 [2].

**b) Pole certifikátu: „_subject:organizationName (OID 2.5.4.10)_“** Ak je prítomné, pole musí obsahovať úplný oficiálny názov organizácie (právnickej osoby) Subjektu, ako bol overený podľa časti 3.2.3. 
RA poskytovateľa môže do tohto poľa zahrnúť informácie, ktoré sa mierne líšia od overeného názvu, ako sú bežné variácie alebo skratky, alebo odstránenie znaku „,“ (čiarka) alebo náhrady znakov podľa časti 3.1.4.1. 

**c) Pole certifikátu: „_subject:organizationalUnitName (OID: 2.5.4.11)_“** Poskytovateľ nezahrňuje toto pole do S/MIME certifikátov.

**d) Pole certifikátu: „_subject:organizationIdentifier (2.5.4.97)_“** Ak je prítomné, pole musí obsahovať registračný odkaz (Registration Reference) pre právnickú osobu pridelený v súlade s identifikovanou schémou registrácie.

„_subject:organizationIdentifier_“ musí byť kódovaný ako PrintableString alebo UTF8String.

Schéma registrácie identifikovaná v certifikáte musí byť výsledkom overenia vykonaného v súlade s časťou 3.2.3. 

Schéma registrácie musí byť identifikovaná pomocou nasledujúcej štruktúry v uvedenom poradí:
* 3-znakový identifikátor schémy registrácie (napr. NTR);
* 2-znakový kód krajiny podľa ISO 3166 pre štát, v ktorom je schéma registrácie prevádzkovaná, alebo ak je schéma prevádzkovaná globálne, použije sa kód ISO 3166 „XG“.

Nasledujúce schémy registrácie sú uznané ako platné podľa SMIME BR [1] pre použitie v atribúte „subject:organizationIdentifier“:
* NTR: Pre identifikátor pridelený národným alebo štátnym obchodným registrom právnickej osobe uvedenej v subject:organizationName.
* VAT: Pre identifikátor pridelený národnými daňovými orgánmi právnickej osobe uvedenej v subject:organizationName.
* PSD: Pre národné autorizačné číslo pridelené poskytovateľovi platobných služieb uvedenému v subject:organizationName podľa Smernice o platobných službách (EÚ) 2015/2366. Toto musí používať rozšírenú štruktúru definovanú v ETSI TS 119 495, článok 5.2.1.
* LEI: Pre identifikátor právnickej osoby (Legal Entity Identifier), ako je špecifikovaný v ISO 17442 pre entitu uvedenú v subject:organizationName. 2-znakový kód krajiny ISO 3166 musí byť nastavený na „XG“.

Kód krajiny použitý v identifikátore schémy registrácie sa musí zhodovať s kódom v poli „subject:countryName“ v certifikáte, ako je špecifikované v časti 7.1.4.2.2.

**e) Pole certifikátu: „_subject:givenName (2.5.4.42)_“ a/alebo „_subject:surname (2.5.4.4)_“** Ak sú prítomné, polia „_subject:givenName_“ a „_subject:surname_“ musia obsahovať meno fyzickej osoby (Subjektu), ako bolo overené podľa časti 3.2.4. Subjekty s jediným oficiálnym menom uvedú toto meno v atribúte „_subject:surname_“. Polia „_subject:givenName_“ a/alebo „_subject:surname_“ nesmú byť prítomné, ak je prítomné pole „_subject:pseudonym_“.

**f) Pole certifikátu: „_subject:pseudonym (2.5.4.65)_“** Poskytovateľ nezahrňuje toto pole do S/MIME certifikátov.

**g) Pole certifikátu: „_subject:serialNumber (2.5.4.5)_“** Ak je prítomné, môže byť použité na uloženie identifikátora prideleného CA alebo RA na identifikáciu a/alebo jednoznačné rozlíšenie Odberateľa.

Okrem toho sa „_subject:serialNumber_“ môže použiť v profiloch Sponsor-validated a Individual-validated na uloženie identifikátora fyzickej osoby (Natural Person Identifier), ako je popísané v ETSI EN 319 412-1 časť 5.1.3 [21].

Poskytovateľ potvrdí, že fyzická osoba reprezentovaná týmto identifikátorom je rovnaká ako Subjekt certifikátu.

**h) Pole certifikátu: „_subject:emailAddress (1.2.840.113549.1.9.1)_“** Musí obsahovať jednu e-mailovú adresu schránky (Mailbox Address), ako bola overená podľa časti 3.2.2.

**i) Pole certifikátu: „_subject:title (2.5.4.12)_“** Poskytovateľ nezahrňuje toto pole do S/MIME certifikátov.

**j) Pole certifikátu: Číslo a ulica: „_subject:streetAddress (OID: 2.5.4.9)_“** Poskytovateľ nezahrňuje toto pole do S/MIME certifikátov.

**k) Pole certifikátu: „_subject:localityName (OID: 2.5.4.7)_“** Ak je prítomné, musí obsahovať informáciu o lokalite Subjektu overenú podľa časti 3.2.3 pre typy certifikátov „Organization-validated“ a „Sponsor-validated“ alebo podľa časti 3.2.4 pre typy certifikátov „Individual-validated“.

**l) Pole certifikátu: „_subject:stateOrProvinceName (OID: 2.5.4.8)_“** Poskytovateľ nezahrňuje toto pole do S/MIME certifikátov.

**m) Pole certifikátu: „_subject:postalCode (OID: 2.5.4.17)_“** Poskytovateľ nezahrňuje toto pole do S/MIME certifikátov.

**n) Pole certifikátu: „_subject:countryName (OID: 2.5.4.6)_“** Ak je prítomné, musí obsahovať dvojpísmenový kód krajiny ISO 3166-1 priradený k umiestneniu Subjektu overenému podľa časti 3.2.3 pre typy certifikátov „Organization-validated“ a „Sponsor-validated“ alebo podľa časti 3.2.4 pre typy certifikátov „Individual-validated“.

#### 7.1.4.3 Informácie o subjekte – koreňové certifikáty a certifikáty podriadenej CA
Vydaním certifikátu podriadenej CA (Subordinate CA) Poskytovateľ vyhlasuje, že dodržal postup stanovený v týchto CP/CPS na overenie toho, že k dátumu vydania certifikátu boli všetky informácie o subjekte presné.

##### 7.1.4.3.1 Polia Subject Distinguished Name
**a) Pole certifikátu: „_subject:commonName (OID 2.5.4.3)_“** Toto pole musí byť prítomné a malo by obsahovať identifikátor certifikátu tak, aby názov certifikátu bol jedinečný v rámci všetkých certifikátov vydaných vydávajúcou CA.

**b) Pole certifikátu: „_subject:organizationName (OID 2.5.4.10)_“** Toto pole musí byť prítomné a musí obsahovať buď názov Subjektu CA alebo DBA (názov, pod ktorým podniká), ako bol overený podľa časti 3.2.3.2.2. Poskytovateľ môže do tohto poľa zahrnúť informácie, ktoré sa mierne líšia od overeného názvu, ako sú bežné variácie alebo skratky.

**c) Pole certifikátu: „_subject:countryName (OID: 2.5.4.6)_“** Toto pole musí byť prítomné a musí obsahovať dvojpísmenový kód krajiny ISO 3166-1 [22] pre krajinu, v ktorej sa nachádza miesto podnikania Poskytovateľa.

**d) Iné atribúty subjektu** V poli subjektu môžu byť prítomné ďalšie atribúty. Ak sú prítomné, iné atribúty musia obsahovať informácie, ktoré boli overené Poskytovateľom.

### 7.1.5 Obmedzenia mien (Name constraints)
Aby sa certifikát podriadenej CA (Subordinate CA) považoval za technicky obmedzený (Technically Constrained), musí certifikát obsahovať rozšírenie Extended Key Usage (EKU) špecifikujúce všetky rozšírené použitia kľúčov, pre ktoré je certifikát podriadenej CA autorizovaný vydávať certifikáty.

Hodnota anyExtendedKeyUsage KeyPurposeId sa v tomto rozšírení nesmie objaviť.

### 7.1.6 Identifikátor objektu politiky certifikátov
Táto časť popisuje požiadavky na obsah pre certifikáty koreňovej CA, podriadenej CA a Odberateľa vo vzťahu k identifikácii politiky certifikátov.

#### 7.1.6.1 Vyhradené identifikátory politík certifikátov
Tieto identifikátory politík certifikátov definované CA/Browser fórom sú vyhradené na použitie Poskytovateľom na potvrdenie, že certifikát spĺňa tieto požiadavky:
|Typ certifikátu |Subtyp |Identifikátor politiky|
|----------------------|:-------------------------------------------:|:---------------------------------:|
|S/MIME certifikát pre digitálny podpis typu <br>„Individual-validated“|STRICT |2.23.140.1.5.4.3 |
|S/MIME certifikát pre digitálny podpis typu <br>„Individual-validated“|MULTIPURPOSE |2.23.140.1.5.4.2 |
|S/MIME certifikát pre digitálny podpis typu <br>„Sponsor-validated“ |STRICT |2.23.140.1.5.3.3 |
|S/MIME certifikát pre digitálny podpis typu <br>„Sponsor-validated“ |MULTIPURPOSE |2.23.140.1.5.3.2 |
|S/MIME digitálny certifikát pre pečať |STRICT |2.23.140.1.5.2.3 |
|S/MIME digitálny certifikát pre pečať |MULTIPURPOSE |2.23.140.1.5.2.2 |

#### 7.1.6.2 Certifikáty koreňovej CA
Certifikát koreňovej CA (Root CA) by nemal obsahovať rozšírenie certificatePolicies. Ak je prítomné, rozšírenie musí spĺňať požiadavky stanovené pre certifikáty vydávané podriadeným CA v časti 7.1.6.3.

#### 7.1.6.3 Certifikáty podriadenej CA
Certifikát vydaný podriadenej CA (Subordinate CA), ktorá je pridruženou spoločnosťou (Affiliate) vydávajúcej CA, musí obsahovať súbor identifikátorov politík z jednej z dvoch nižšie uvedených možností:
* Jeden alebo viac explicitných identifikátorov politík definovaných v časti 7.1.6.1, ktoré indikujú dodržiavanie a súlad podriadenej CA so SMIME BR [1], a môže obsahovať jeden alebo viac identifikátorov zdokumentovaných podriadenou CA v týchto CP/CPS; alebo
* Identifikátor „anyPolicy (2.5.29.32.0)“.

Podriadená CA aj vydávajúca CA vyhlásia vo svojich CP/CPS, že všetky certifikáty obsahujúce identifikátor politiky indikujúci súlad so SMIME BR [1] sú vydávané a spravované v súlade s týmito požiadavkami.

#### 7.1.6.4 Certifikáty Odberateľov
Certifikát vydaný koncovému používateľovi musí obsahovať v rozšírení certificatePolicies jeden z identifikátorov politík uvedených v časti 7.1.6.1.
Okrem toho bude certifikát obsahovať aj identifikátor týchto CP/CPS definovaný Poskytovateľom vo forme OID=1.3.158.35975946.0.0.0.1.11, ako aj URI adresu, kde je príslušná politika dostupná.

### 7.1.7 Použitie rozšírenia Policy Constraints
Žiadne ustanovenia.

### 7.1.8 Syntax a sémantika kvalifikátorov politík (Policy qualifiers)
Žiadne ustanovenia.

### 7.1.9 Sémantika spracovania pre kritické rozšírenie Certificate Policies
Žiadne ustanovenia.

## 7.2 Profil CRL

### 7.2.1 Číslo verzie
Všetky zoznamy CRL vydávané Poskytovateľom musia byť v súlade s RFC 5280 a musia byť vo verzii 2.

### 7.2.2 Rozšírenia CRL a položiek CRL
Tabuľka 9 uvádza rozšírenia CRL, ktoré boli vydané autoritami CA Poskytovateľa, na ktoré sa vzťahujú tieto CP, spolu s informáciami o ich prítomnosti a kritickosti.

Tabuľka 9: Rozšírenia CRL 
|Názov rozšírenia |Povinné|Kritické|
|-------------------------------------------|:------:|:------:|
|Authority Key Identifier<br>(OID 2.5.29.35)|ÁNO |NIE |
|CRL Number<br>(OID 2.5.29.20) |ÁNO |NIE |
|ReasonCode<br>(OID 2.5.29.21) |ÁNO* |NIE |

*Ak je položka CRL pre certifikát koreňovej CA alebo podriadenej CA, vrátane krížových certifikátov, toto rozšírenie položky CRL musí byť prítomné. Ak je položka CRL pre certifikát, ktorý nie je technicky schopný spôsobiť vydanie (vydávať iné certifikáty), toto rozšírenie položky CRL by malo byť prítomné, ale môže byť vynechané pri dodržaní nasledujúcich požiadaviek.

CRLreason certificateHold (6) SA NESMIE používať pre certifikáty koreňovej CA alebo podriadenej CA.
Indikovaný CRLReason nesmie byť unspecified (0). Ak je dôvod zrušenia nešpecifikovaný, autority CA vynechajú rozšírenie položky reasonCode.

Úložisko môže obsahovať položky CRL, ktoré majú CRLreason certificateHold (6) pre certifikáty, ktoré obsahujú identifikátory politík certifikátov pre generácie Legacy alebo Multipurpose. Úložisko nesmie obsahovať položky CRL, ktoré majú CRLreason certificateHold (6) pre certifikáty, ktoré obsahujú identifikátory politík certifikátov pre generáciu Strict.

Ak je prítomné rozšírenie položky CRL reasonCode, CRLReason MUSÍ indikovať najvhodnejší dôvod pre zrušenie certifikátu, ako je definovaný autoritou CA v rámci týchto CP/CPS.
Ak je prítomné, rozšírenie reasonCode (OID 2.5.29.21) nesmie byť označené ako kritické.
Zoznamy CRL sú zverejňované v úložisku na miestach definovaných v časti 2.2.3.

## 7.3 Profil OCSP
Ak je odpoveď OCSP pre certifikát koreňovej CA alebo podriadenej CA, vrátane krížových certifikátov, a tento certifikát bol zrušený, potom pole revocationReason v rámci RevokedInfo v CertStatus MUSÍ byť prítomné.
Indikovaný CRLReason MUSÍ obsahovať hodnotu povolenú pre zoznamy CRL, ako je špecifikované v časti 7.2.2.

### 7.3.1 Číslo verzie
Žiadne ustanovenia.

### 7.3.2 Rozšírenia OCSP
Tabuľka 10 obsahuje možné rozšírenia v odpovediach OCSP respondera Poskytovateľa, ich povinnosť hlásenia a ich kritickosť.

Tabuľka 10: Rozšírenia odpovede OCSP
|Názov rozšírenia |Povinné|Kritické|
|------------------------------------------------|:------:|:------:|
|id-pkix-ocsp-nonce<br>(OID 1.3.6.1.5.5.7.48.1.2)|ÁNO |NIE |

Položky „singleExtensions“ odpovede OCSP nesmú obsahovať rozšírenie položky CRL „reasonCode“ (OID 2.5.29.21).

# 8.   AUDIT ZHODY A INÉ POSUDZOVANIA 
Účelom auditu zhody je zabezpečiť, aby mal Poskytovateľ uspokojivý systém práce, ktorý zaručuje kvalitu dôveryhodných služieb poskytovaných Poskytovateľom a zaručuje, že koná v súlade so všetkými požiadavkami týchto CP/CPS, nariadenia eIDAS [3] a SMIME BR [1]. Všetky aspekty prevádzky CA týkajúce sa tejto CP musia byť predmetom auditov zhody.  
Poskytovateľ musí v každom čase:
* vydávať certifikáty a prevádzkovať svoju PKI v súlade so všetkými právnymi predpismi vzťahujúcimi sa na jeho podnikanie a certifikáty, ktoré vydáva, v každej jurisdikcii, v ktorej pôsobí;
* dodržiavať požiadavky týchto CP/CPS;
* dodržiavať požiadavky na audit stanovené v tejto časti; a
* mať licenciu ako poskytovateľ dôveryhodných služieb (CA) v každej jurisdikcii, kde pôsobí, ak sa licencia na vydávanie certifikátov vyžaduje podľa práva takejto jurisdikcie.

## 8.1 Periodicita alebo okolnosti posudzovania 
Certifikáty, ktoré sú schopné vydávať nové certifikáty, musia byť buď technicky obmedzené v súlade s časťou 7.1.5 a auditované len v súlade s časťou 8.8, alebo neobmedzené a plne auditované v súlade so všetkými zostávajúcimi požiadavkami z tejto časti. Certifikát sa považuje za schopný vydávať nové certifikáty, ak obsahuje rozšírenie X.509v3 „basicConstraints“ s poľom „cA Boolean“ nastaveným na „true“ a je teda z definície certifikátom koreňovej CA (Root CA) alebo podriadenej CA (Subordinate CA).

Obdobie, počas ktorého Poskytovateľ vydáva certifikáty, musí byť rozdelené do nepretržitej sekvencie auditných období. Auditné obdobie nesmie presiahnuť dĺžku jedného roka.

Ak má Poskytovateľ aktuálne platnú správu z auditu preukazujúcu súlad so schémou auditu uvedenou v časti 8.4, potom nie je potrebné žiadne posúdenie pripravenosti pred vydávaním.

Ak Poskytovateľ nemá aktuálne platnú správu z auditu preukazujúcu súlad s jednou zo schém auditu uvedených v časti 8.4, potom pred vydávaním verejne dôveryhodných S/MIME certifikátov musí Poskytovateľ úspešne absolvovať posúdenie pripravenosti k časovému okamihu (point-in-time readiness assessment) vykonané v súlade s príslušnými štandardmi podľa jednej zo schém auditu uvedených v časti 8.4. Posúdenie pripravenosti k časovému okamihu musí byť ukončené najskôr dvanásť (12) mesiacov pred vydaním verejne dôveryhodných S/MIME certifikátov a musí po ňom nasledovať úplný audit podľa takejto schémy do deväťdesiatich (90) dní od vydania prvého verejne dôveryhodného S/MIME certifikátu.

## 8.2 Identita/kvalifikácia posudzovateľa 
Audit Poskytovateľa musí vykonať kvalifikovaný audítor. Kvalifikovaný audítor znamená fyzickú osobu, právnickú osobu alebo skupinu fyzických alebo právnických osôb, ktoré spoločne disponujú nasledujúcou kvalifikáciou a zručnosťami:
* nezávislosť od subjektu auditu;
* schopnosť vykonať audit, ktorý sa zaoberá kritériami špecifikovanými v oprávnenej schéme auditu (pozri časť 8.4);
* zamestnáva osoby, ktoré sú odborne zdatné v preverovaní technológie infraštruktúry verejných kľúčov (PKI), nástrojov a techník informačnej bezpečnosti, informačných technológií a auditu bezpečnosti a funkcie potvrdzovania treťou stranou;
* pre audity vykonávané v súlade s ktorýmkoľvek zo štandardov ETSI je akreditovaný v súlade s ISO 17065 pri uplatnení požiadaviek špecifikovaných v ETSI EN 319 403 alebo ETSI EN 319 403-1;
* viazaný zákonom, vládnym nariadením alebo profesionálnym etickým kódexom; a
* s výnimkou vládneho interného auditného orgánu má uzatvorené poistenie profesijnej zodpovednosti za škodu/chyby a opomenutia s limitmi poistného plnenia najmenej jeden milión amerických dolárov.

## 8.3 Vzťah posudzovateľa k posudzovanému subjektu 
Žiadne ustanovenia.

## 8.4 Témy zahrnuté v posudzovaní 
Pre auditné obdobia začínajúce po dátume účinnosti definovanom v časti 1.2.1 dokumentu SMIME BR [1] sa Poskytovateľ podrobí auditu v súlade s nasledujúcou schémou:
* ETSI EN 319 411-1 v1.3.1 [6] alebo novšia, ktorá zahŕňa normatívne odkazy na ETSI EN 319 401 [5] (mala by sa použiť najnovšia verzia odkazovaných dokumentov ETSI).

Audit musí vykonať kvalifikovaný audítor, ako je špecifikované v časti 8.2.

## 8.5 Opatrenia prijaté v dôsledku nedostatku 
Keď audítor zistí nesúlad medzi operáciami CA a ustanoveniami jej CP/CPS, musia sa prijať nasledujúce opatrenia:
* audítor zaznamená nesúlad,
* audítor o nesúlade informuje subjekty definované v časti 8.6,
* CA navrhne PMA príslušné nápravné opatrenie, vrátane predpokladaného času potrebného na jeho implementáciu.

PMA určí vhodné nápravné opatrenie, potenciálne až po zrušenie certifikátu CA.

## 8.6 Oznamovanie výsledkov 
Správa z auditu musí výslovne uvádzať, že pokrýva príslušné systémy a procesy používané pri vydávaní všetkých certifikátov, ktoré uvádzajú jeden alebo viac identifikátorov politík uvedených v časti 7.1.6.1. Poskytovateľ správu z auditu verejne sprístupní.

Poskytovateľ zverejní svoju správu z auditu najneskôr tri mesiace po skončení auditovaného obdobia. V prípade oneskorenia dlhšieho ako tri mesiace Poskytovateľ poskytne vysvetľujúci list podpísaný kvalifikovaným audítorom.

Správa z auditu musí obsahovať aspoň nasledujúce jasne označené informácie:
* názov auditovanej organizácie;
* názov a adresu organizácie vykonávajúcej audit;
* SHA-256 odtlačok (fingerprint) všetkých certifikátov koreňových a podriadených CA, vrátane krížových certifikátov, ktoré boli v rozsahu auditu;
* kritériá auditu s číslom (číslami) verzií, ktoré boli použité na audit každého z certifikátov (a súvisiacich kľúčov);
* zoznam dokumentov politiky Poskytovateľa s číslami verzií, na ktoré sa počas auditu odkazovalo;
* či audit posudzoval časové obdobie alebo časový okamih;
* dátum začiatku a dátum konca auditovaného obdobia pre tie, ktoré pokrývajú časové obdobie;
* dátum časového okamihu pre tie, ktoré sú k časovému okamihu;
* dátum vydania správy, ktorý bude nevyhnutne po dátume ukončenia alebo dátume časového okamihu;
* pre audity vykonané v súlade s ktorýmkoľvek zo štandardov ETSI vyhlásenie indikujúce, či bol audit plným auditom alebo dozorným auditom, a ktoré časti kritérií boli aplikované a vyhodnotené, napr. ETSI EN 319 401, ETSI EN 319 411-1 politika LCP, NCP alebo NCP+, ETSI EN 319 411-2 politika QCP-n, QCP-n-qscd, QCP-l alebo QCP-l-qscd; a
* pre audity vykonané v súlade s ktorýmkoľvek zo štandardov ETSI vyhlásenie indikujúce, že audítor odkazoval na príslušné kritériá CA/Browser fóra, ako je tento dokument, a použitú verziu.

Autoritatívnu verziu verejne dostupných informácií o audite v anglickom jazyku poskytne kvalifikovaný audítor a Poskytovateľ zabezpečí, aby bola verejne dostupná.

Správa z auditu musí byť k dispozícii ako PDF a musí v nej byť možné vyhľadávať text pre všetky požadované informácie. Každý odtlačok SHA-256 v správe z auditu musí byť veľkými písmenami a nesmie obsahovať dvojbodky, medzery ani odriadkovania.

## 8.7 Vlastné audity 
Počas obdobia, v ktorom Poskytovateľ vydáva certifikáty, monitoruje zhodu RA Poskytovateľa s týmito CP/CPS a posudzuje kvalitu ich služieb vykonávaním vlastných auditov aspoň raz ročne na náhodne vybranej vzorke rovnajúcej sa väčšej z hodnôt: tridsať (30) certifikátov alebo tri percentá (3 %) certifikátov vydaných počas obdobia začínajúceho ihneď po odobratí predchádzajúcej vzorky pre interný audit.

## 8.8 Preskúmanie poverených strán 
Žiadne ustanovenia.

# 9.   OSTATNÉ OBCHODNÉ A PRÁVNE ZÁLEŽITOSTI 

## 9.1 Poplatky 
Poskytovateľ má povinnosť zverejniť platný cenník dôveryhodných služieb a informácie, za akých je možné tieto služby objednať. 

### 9.1.1 Poplatky za vydanie alebo obnovu certifikátu 
Poplatok za certifikáty musí byť zaplatený za podmienok dohodnutých s Odberateľom/Držiteľom. 

Poskytovateľ zverejní platný cenník na webovom sídle spoločnosti (pozri časť 1).

V prípade poskytovania svojich služieb len zmluvnému partnerovi cenník nemusí byť zverejnený.

### 9.1.2 Poplatky za prístup k certifikátu 
Žiadne ustanovenia.

### 9.1.3 Poplatky za zrušenie alebo prístup k informáciám o stave 
Žiadne ustanovenia.

### 9.1.4 Poplatky za ostatné služby 
Žiadne ustanovenia.

### 9.1.5 Politika vrátenia peňazí 
V odôvodnených prípadoch môže Poskytovateľ na základe individuálneho posúdenia vrátiť platbu za poskytnuté služby.

## 9.2 Finančná zodpovednosť

### 9.2.1 Poistné krytie 
Žiadne ustanovenia.

### 9.2.2 Ostatné aktíva 
Žiadne ustanovenia.

### 9.2.3 Poistenie alebo záručné krytie pre koncové entity 
Žiadne ustanovenia.

## 9.3 Dôvernosť obchodných informácií 

### 9.3.1 Rozsah dôverných informácií 
Žiadne ustanovenia.

### 9.3.2 Informácie, ktoré nespadajú do rozsahu dôverných informácií 
Žiadne ustanovenia.

### 9.3.3 Zodpovednosť za ochranu dôverných informácií 
Žiadne ustanovenia.

## 9.4 Súkromie osobných informácií 

### 9.4.1 Plán ochrany súkromia 
Poskytovateľ spracúva osobné údaje Odberateľa/Držiteľa alebo oprávnených osôb v súlade s požiadavkami Predpisov o ochrane osobných údajov [14]. 

Poskytovateľ zverejní Politiku ochrany súkromia, ktorá poskytuje informácie o praktikách Poskytovateľa pri ochrane údajov. Politika ochrany súkromia by mala obsahovať informácie o tom, ako Poskytovateľ zhromažďuje, používa, zdieľa, uchováva a vymazáva alebo uchováva údaje, ako aj kontaktné informácie na uplatnenie práv na ochranu súkromia. 

Postupy ochrany údajov sú dostupné na: [https://eidas.disig.sk/pdf/info_oou_gdpr.pdf](https://eidas.disig.sk/pdf/info_oou_gdpr.pdf).

### 9.4.2 Informácie považované za súkromné
Poskytovateľ nakladá so všetkými osobnými informáciami o jednotlivcovi, ktoré nie sú verejne dostupné v obsahu certifikátu, ako so súkromnými informáciami. To zahŕňa informácie, ktoré spájajú „subject:pseudonym“ so skutočnou identitou subjektu (jednotlivca).

### 9.4.3 Informácie, ktoré sa nepovažujú za súkromné 
Žiadne ustanovenia.

### 9.4.4 Zodpovednosť za ochranu súkromných informácií 
Poskytovateľ chráni súkromné informácie pomocou primeraných záruk a primeranej miery starostlivosti. Poskytovateľ vyžaduje to isté od všetkých poskytovateľov služieb, ktorí spravujú súkromné informácie v mene Poskytovateľa.

### 9.4.5 Oznámenie a súhlas s používaním súkromných informácií 
Poskytovateľ je povinný postupovať v súlade s Predpismi o ochrane osobných údajov pri plnení informačnej povinnosti voči dotknutým osobám a pri získavaní ich súhlasu so spracovaním osobných údajov [14].

### 9.4.6 Zverejnenie na základe súdneho alebo správneho konania 
Žiadne ustanovenia.

### 9.4.7 Iné okolnosti zverejnenia informácií 
Žiadne ustanovenia.

## 9.5 Práva duševného vlastníctva 
Žiadne ustanovenia.

## 9.6 Vyhlásenia a záruky 

### 9.6.1 Vyhlásenia a záruky CA 
Vydaním certifikátu Poskytovateľ poskytuje záruky uvedené v tomto dokumente nasledujúcim oprávneným z certifikátu (Certificate Beneficiaries):
* Odberateľovi, ktorý je stranou zmluvy s odberateľom alebo podmienok používania certifikátu;
* Všetkým dodávateľom aplikačného softvéru, s ktorými koreňová CA uzatvorila zmluvu o zahrnutí svojho certifikátu koreňovej CA do softvéru distribuovaného takýmto dodávateľom aplikačného softvéru; a
* Všetkým spoliehajúcim sa stranám, ktoré sa rozumne spoliehajú na platný certifikát.
Poskytovateľ vyhlasuje a zaručuje oprávneným z certifikátu, že počas obdobia platnosti certifikátu Poskytovateľ pri vydávaní a správe certifikátu dodržiaval tieto CP/CPS.

Záruky vyplývajúce z certifikátu konkrétne zahŕňajú, okrem iného, nasledujúce:

**[1] Právo používať e-mailovú adresu:** Že v čase vydania Poskytovateľ:
**i.)** implementoval postup na overenie, či Žiadateľ mal buď právo na používanie, alebo mal pod kontrolou e-mailové adresy uvedené v poli predmetu certifikátu a v rozšírení subjectAltName (alebo mu takéto právo alebo kontrola boli delegované niekým, kto takéto právo na používanie alebo kontrolu mal);
**ii.)** dodržal tento postup pri vydávaní certifikátu; a
**iii.)** presne opísal tento postup v CP/CPS Poskytovateľa;

**[2] Autorizácia certifikátu:** Že v čase vydania Poskytovateľ:
**i.)** implementoval postup na overenie, či Subjekt autorizoval vydanie certifikátu a či zástupca žiadateľa (Applicant Representative) je oprávnený žiadať o certifikát v mene Subjektu;
**ii.)** dodržal tento postup pri vydávaní certifikátu; a
**iii.)** presne opísal tento postup v CP/CPS Poskytovateľa;

**[3] Presnosť informácií:** Že v čase vydania Poskytovateľ:
**i.)** implementoval postup na overenie presnosti všetkých informácií obsiahnutých v certifikáte (s výnimkou atribútu „subject:serialNumber“);
**ii.)** dodržal tento postup pri vydávaní certifikátu; a
**iii.)** presne opísal tento postup v CP/CPS Poskytovateľa;

**[4] Identita žiadateľa:** Že ak certifikát obsahuje identifikačné informácie o subjekte, Poskytovateľ:
**i.)** implementoval postup na overenie identity Žiadateľa v súlade s časťou 3.2 a časťou 7.1.4.2.2;
**ii.)** dodržal tento postup pri vydávaní certifikátu; a
**iii.)** presne opísal tento postup v CP/CPS Poskytovateľa;

**[5] Zmluva s odberateľom:** Že ak Poskytovateľ a Odberateľ nie sú pridruženými osobami, Odberateľ a Poskytovateľ sú stranami právne platnej a vymáhateľnej zmluvy s odberateľom, ktorá spĺňa tieto požiadavky, alebo ak sú Poskytovateľ a Odberateľ tým istým subjektom alebo sú pridruženými osobami, zástupca žiadateľa vzal na vedomie podmienky používania;

**[6] Stav:** Že Poskytovateľ udržiava verejne prístupné úložisko v režime 24 x 7 s aktuálnymi informáciami o stave (platný alebo zrušený) všetkých neexspirovaných certifikátov; a

**[7] Zrušenie:** Že Poskytovateľ zruší certifikát z ktoréhokoľvek z dôvodov špecifikovaných v týchto požiadavkách.

### 9.6.2 Vyhlásenia a záruky RA 
Žiadne ustanovenia.

### 9.6.3 Vyhlásenia a záruky Odberateľa 
Odberateľ/Držiteľ využíva dôveryhodné služby Poskytovateľa na vlastnú zodpovednosť a znáša všetky náklady na prostriedky diaľkovej komunikácie alebo iné technické prostriedky potrebné na využívanie týchto služieb (napr. softvér potrebný na vyhotovenie elektronického podpisu / pečate, softvér na autentifikáciu webového sídla atď.);

Odberateľ/Držiteľ dodržiava všetky ustanovenia týkajúce sa záväzkov a záruk, ako sú uvedené v Podmienkach používania [8].

Pred vydaním certifikátu Poskytovateľ získa, pre výslovný prospech Poskytovateľa a oprávnených z certifikátu, od Žiadateľa buď:
* súhlas so zmluvou s odberateľom s Poskytovateľom; alebo
* potvrdenie o vzatí na vedomie Podmienok používania [8].

Poskytovateľ implementuje proces na zabezpečenie toho, aby každá zmluva s odberateľom alebo podmienky používania boli voči Žiadateľovi právne vymáhateľné. V oboch prípadoch sa zmluva vzťahuje na certifikát, ktorý sa má vydať na základe žiadosti o certifikát. Poskytovateľ môže použiť elektronickú zmluvu alebo zmluvu typu „click-through“ za predpokladu, že Poskytovateľ určil, že takéto zmluvy sú právne vymáhateľné. Pre každú žiadosť o certifikát môže byť použitá samostatná zmluva, alebo môže byť použitá jedna zmluva na pokrytie viacerých budúcich žiadostí o certifikát a výsledných certifikátov, pokiaľ je každý certifikát, ktorý Poskytovateľ Žiadateľovi vydá, jasne pokrytý touto zmluvou s odberateľom alebo podmienkami používania.

Zmluva s odberateľom alebo podmienky používania musia obsahovať ustanovenia ukladajúce samotnému Žiadateľovi (alebo urobené Žiadateľom v mene jeho splnomocniteľa alebo agenta v rámci vzťahu subdodávky alebo hostingovej služby) nasledujúce povinnosti a záruky:
* Presnosť informácií: Povinnosť a záruku poskytovať Poskytovateľovi v každom čase presné a úplné informácie, a to ako v žiadosti o certifikát, tak aj v iných prípadoch vyžiadaných Poskytovateľom v súvislosti s vydaním certifikátu (certifikátov), ktoré má Poskytovateľ dodať;
* Ochrana súkromného kľúča: Povinnosť a záruku Žiadateľa prijať všetky primerané opatrenia na zabezpečenie kontroly, zachovanie dôvernosti a riadnu ochranu súkromného kľúča v každom čase, ktorý zodpovedá verejnému kľúču, ktorý má byť zahrnutý v požadovanom certifikáte (certifikátoch) (a akýchkoľvek súvisiacich aktivačných údajov alebo zariadení, ako je heslo alebo token);
* Prevzatie certifikátu: Povinnosť a záruku, že Odberateľ skontroluje a overí presnosť obsahu certifikátu;
* Používanie certifikátu: Povinnosť a záruku používať certifikát len pre e-mailové adresy uvedené v certifikáte a používať certifikát výhradne v súlade so všetkými platnými zákonmi a výhradne v súlade so zmluvou s odberateľom alebo podmienkami používania;
* Nahlasovanie a zrušenie: Povinnosť a záruku:
**i.)** bezodkladne požiadať o zrušenie certifikátu a prestať ho používať spolu s prislúchajúcim súkromným kľúčom, ak dôjde k akémukoľvek skutočnému alebo podozrivému zneužitiu alebo kompromitácii súkromného kľúča Odberateľa spojeného s verejným kľúčom zahrnutým v certifikáte, a
**ii.)** bezodkladne požiadať o zrušenie certifikátu a prestať ho používať, ak sa akákoľvek informácia v certifikáte stane nesprávnou alebo nepresnou;
* Ukončenie používania certifikátu: Povinnosť a záruku bezodkladne ukončiť akékoľvek používanie súkromného kľúča zodpovedajúceho verejnému kľúču zahrnutému v certifikáte po zrušení tohto certifikátu z dôvodu kompromitácie kľúča.
* Reakcia: Povinnosť reagovať na pokyny Poskytovateľa týkajúce sa kompromitácie kľúča alebo zneužitia certifikátu v špecifikovanom časovom období.
* Uznanie a prijatie: Uznanie a prijatie toho, že Poskytovateľ je oprávnený okamžite zrušiť certifikát, ak by Žiadateľ porušil podmienky zmluvy s odberateľom alebo podmienok používania, alebo ak zrušenie vyžadujú CP/CPS Poskytovateľa.

### 9.6.4 Vyhlásenia a záruky spoliehajúcej sa strany
Žiadne ustanovenia.

### 9.6.5 Vyhlásenia a záruky ostatných účastníkov 
Žiadne ustanovenia.

## 9.7 Vylúčenie záruk
Žiadne ustanovenia.

## 9.8 Obmedzenie zodpovednosti 
Pri úlohách delegovaných na RA si Poskytovateľ a RA môžu zmluvne rozdeliť zodpovednosť podľa vlastného uváženia, ale Poskytovateľ zostáva plne zodpovedný za výkon všetkých strán v súlade s týmito CP/CPS, akoby úlohy neboli delegované.

Poskytovateľ nezodpovedá za nepriame alebo podmienené straty alebo škody vzniknuté Odberateľovi/Držiteľovi alebo spoliehajúcim sa stranám v súvislosti s používaním dôveryhodných služieb.

Poskytovateľ nezodpovedá za žiadne škody (vrátane ušlého zisku) vzniknuté Držiteľovi certifikátu, spoliehajúcej sa strane alebo akejkoľvek tretej strane v dôsledku:
**a)** porušenia povinností Odberateľom/Držiteľom alebo spoliehajúcou sa stranou podľa právnych, zmluvných, Všeobecných podmienok alebo povinností Poskytovateľa, vrátane povinnosti vykonávať primeranú starostlivosť pri spoliehaní sa na certifikáty;
**b)** neposkytnutia nevyhnutnej súčinnosti zo strany Odberateľa/Držiteľa;
**c)** technických vlastností, konfigurácie, nekompatibility, neadekvátnosti alebo iných chýb v softvérových alebo hardvérových prostriedkoch nimi používaných;
**d)** použitia alebo spoliehania sa na exspirovaný alebo zrušený certifikát;
**e)** použitia certifikátu Odberateľom/Držiteľom certifikátu v rozpore so zmluvou, Všeobecnými podmienkami alebo politikami Poskytovateľa;
**f)** že certifikát bol použitý v rozpore s jeho účelom alebo obmedzeniami uvedenými v certifikáte, vo Všeobecných podmienkach alebo v CP;
**g)** oneskorenia alebo nedoručenia žiadosti o stav certifikátu Poskytovateľovi z dôvodov, ktoré nie sú na strane Poskytovateľa (najmä v prípadoch nedostupnosti alebo preťaženia internetu alebo chýb v zariadeniach alebo technickom vybavení používanom overovateľom);
**h)** neposkytnutia ktorejkoľvek z dôveryhodných služieb alebo ich nedostupnosti počas plánovanej údržby alebo reorganizácie oznámenej na webovom sídle Poskytovateľa;
**i)** vyššej moci (Force Majeure).

Poskytovateľ nezodpovedá za škody vzniknuté spoliehajúcej sa strane preto, že pri spoliehaní sa na certifikát a dôveryhodné služby Poskytovateľa alebo spoliehaní sa na elektronický podpis alebo pečať vyhotovenú na ich základe nepostupovala podľa časti 10 Všeobecných podmienok [8] alebo podľa požiadaviek tejto politiky.

## 9.9 Odškodnenie 
Akákoľvek osoba, ktorá poruší svoju povinnosť alebo akúkoľvek povinnosť podľa týchto CP/CPS, zmluvy a Všeobecných podmienok, je povinná nahradiť škodu spôsobenú druhej strane, okrem prípadov, kedy je zodpovednosť subjektu za škody vylúčená. Za škodu sa považuje skutočná škoda, ušlý zisk a náklady vynaložené poškodenou stranou v súvislosti so škodovou udalosťou.
Ktokoľvek, kto poruší svoju povinnosť alebo akúkoľvek povinnosť podľa týchto CP/CPS, zmluvy a Všeobecných podmienok, môže byť zbavený zodpovednosti za škody len vtedy, ak preukáže, že k porušeniu povinnosti alebo akejkoľvek povinnosti došlo v dôsledku okolností vylučujúcich zodpovednosť, napr. vyššia moc (Force Majeure).

Bez ohľadu na akékoľvek obmedzenia svojej zodpovednosti voči Odberateľom a spoliehajúcim sa stranám, Poskytovateľ berie na vedomie, že dodávatelia aplikačného softvéru, ktorí súhlasili s distribúciou certifikátu koreňovej CA, nepreberajú žiadnu povinnosť ani potenciálnu zodpovednosť CA podľa týchto požiadaviek, alebo takú, ktorá by inak mohla existovať z dôvodu vydávania alebo údržby certifikátov alebo spoliehania sa na ne zo strany spoliehajúcich sa strán alebo iných osôb.
Teda, s výnimkou prípadu, kedy je Poskytovateľ vládnym subjektom, Poskytovateľ bude brániť, odškodní a zbaví zodpovednosti každého dodávateľa aplikačného softvéru za akékoľvek nároky, škody a straty utrpené takýmto dodávateľom aplikačného softvéru súvisiace s certifikátom vydaným Poskytovateľom, bez ohľadu na príčinu konania alebo právnu teóriu. To sa však nevzťahuje na akýkoľvek nárok, škodu alebo stratu utrpenú takýmto dodávateľom aplikačného softvéru súvisiacu s certifikátom vydaným CA, kde takýto nárok, škoda alebo strata boli priamo spôsobené softvérom takéhoto dodávateľa aplikačného softvéru zobrazujúcim ako nedôveryhodný certifikát, ktorý je stále platný, alebo zobrazujúcim ako dôveryhodný:
**(1)** certifikát, ktorého platnosť vypršala (exspiroval), alebo
**(2)** certifikát, ktorý bol zrušený (ale len v prípadoch, kedy je stav zrušenia aktuálne dostupný od CA online a aplikačný softvér buď nepreveril takýto stav, alebo ignoroval indikáciu zrušeného stavu).

## 9.10 Doba platnosti a ukončenie

### 9.10.1 Doba platnosti 
Táto verzia CP/CPS je účinná od dátumu účinnosti špecifikovaného v časti 1.2 a je platná, kým nebude nahradená novou verziou. Podrobnosti o histórii revízií týchto CP/CPS nájdete v časti „Revízia“ v časti 1.2.1.

### 9.10.2 Ukončenie
Platnosť tejto verzie CP/CPS zanikne dňom nadobudnutia účinnosti novej verzie (pozri časť 9.10.1) alebo ukončením dôveryhodnej služby Poskytovateľa.

### 9.10.3 Účinok ukončenia a pretrvanie
V prípade, že tento dokument nebude nahradený novou verziou a jeho platnosť zanikne po skončení poskytovania dôveryhodnej služby Poskytovateľom, musia byť splnené všetky ustanovenia týchto CP/CPS týkajúce sa Poskytovateľa, ktoré je povinný dodržiavať po ukončení svojej činnosti (pozri časť 9).

## 9.11 Individuálne oznámenia a komunikácia s účastníkmi
Žiadne ustanovenia.

## 9.12 Zmeny a doplnenia 

### 9.12.1 Postup pri zmenách a doplneniach 
Aktualizácia CP/CPS vychádza z jej preskúmania, ktoré sa musí vykonať aspoň raz ročne od schválenia aktuálne platnej verzie. Preskúmanie musí vykonať autorizovaná osoba Poskytovateľa, ktorá na základe výsledkov preskúmania musí pripraviť písomný návrh prípadných navrhovaných zmien.

Schválenie navrhovaných zmien musí vykonať autorizovaný člen PMA. Navrhované zmeny musia byť zvážené do 14 dní od ich doručenia. Po lehote na posúdenie návrhu zmeny musí PMA navrhovanú zmenu prijať, prijať ju s podmienkami alebo odmietnuť.

Chyby, žiadosti o aktualizáciu alebo navrhované zmeny CP/CPS musia byť oznámené kontaktu uvedenému v časti 1.5.2. Takáto komunikácia musí obsahovať popis zmeny, dôvod zmeny a kontaktné údaje osoby žiadajúcej o zmenu alebo navrhujúcej zmenu.

Všetky schválené zmeny CP/CPS musia byť oznámené dotknutým subjektom v lehote jedného týždňa pred ich nadobudnutím účinnosti prostredníctvom kanála na zverejňovanie a oznamovanie (pozri časť 2).
Každá upravená verzia týchto CP/CPS musí byť očíslovaná a registrovaná, pričom novšia verzia musí mať vyššie číslo verzie ako tá, ktorú nahrádza.

Opravy nejasností, gramatických a štylistických chýb sa nepovažujú za zmeny vyvolávajúce zmenu verzie týchto CP/CPS.

### 9.12.2 Mechanizmus a lehota oznamovania 
Poskytovateľ musí zverejniť informácie o aktuálnej verzii CP/CPS prostredníctvom svojho webového sídla (pozri časť 1.5.2). 

Oprávnený zástupca Poskytovateľa musí informovať všetky zmluvne viazané RA Poskytovateľa o schválení novej verzie CP/CPS zaslaním novej verzie e-mailom pred jej nadobudnutím účinnosti v súlade s časťou 9.12.1. Poskytovateľ vyžiada od RA spätnú väzbu formou potvrdzujúcej e-mailovej správy o stiahnutí elektronickej verzie CP Poskytovateľa.
Aktuálna verzia CP/CPS musí byť k dispozícii u každej zmluvne viazanej RA Poskytovateľa aspoň v elektronickej forme. Interní zamestnanci musia byť o novej verzii týchto CP/CPS informovaní rovnako. 

### 9.12.3 Okolnosti, za ktorých sa musí zmeniť OID 
Každej politike musí byť Poskytovateľom priradené jej OID. OID tejto politiky je uvedené v časti 1.2 a pre každú novú verziu CP/CPS zostáva nezmenené.

## 9.13 Ustanovenia o riešení sporov 
Odberateľ/Držiteľ má právo zaslať Poskytovateľovi sťažnosť na poskytovanú dôveryhodnú službu e-mailom na adresu <radisig@disig.sk>. Poskytovateľ vybaví sťažnosť najneskôr do 30 dní od jej prijatia, ak sa strany nedohodnú inak. Proces sťažnosti sa vzťahuje len na popis nedostatku, na ktorý Odberateľ/Držiteľ poukazuje. Poskytovateľ musí odpovedať do 30 dní od prijatia sťažnosti. Poskytovateľ si vyhradzuje právo predĺžiť túto lehotu v prípade zložitejších sťažností.

Súdy Slovenskej republiky majú výhradnú právomoc riešiť akékoľvek spory medzi Poskytovateľom a Odberateľom/Držiteľom certifikátu. Ak je Odberateľ/Držiteľ spotrebiteľom, akýkoľvek spor môže byť riešený aj mimosúdne. V takom prípade je oprávnený obrátiť sa na orgán mimosúdneho riešenia sporov, Slovenskú obchodnú inšpekciu alebo inú právnickú osobu zapísanú v zozname podľa článku 5 ods. 2 zákona č. 391/2015 Z. z. o alternatívnom riešení spotrebiteľských sporov v znení neskorších predpisov. Pred podaním na súdne alebo mimosúdne riešenie sporov sú strany povinné pokúsiť sa vyriešiť tento spor najskôr vzájomnou dohodou.

## 9.14 Rozhodné právo 
Právne vzťahy medzi Poskytovateľom a Odberateľom/Držiteľom certifikátu sa riadia zákonmi Slovenskej republiky.

Práva a povinnosti strán, ktoré nie sú upravené Všeobecnými podmienkami alebo zmluvou, sa riadia najmä príslušnými ustanoveniami zákona č. 513/1991 Zb., Obchodný zákonník, v znení neskorších predpisov, zákona č. 40/1964 Zb., Občiansky zákonník v znení neskorších predpisov a inými všeobecne záväznými právnymi predpismi Slovenskej republiky.

## 9.15 Súlad s platnými zákonmi 
Poskytovateľ poskytuje dôveryhodné služby v súlade s platnými právnymi predpismi účinnými v Slovenskej republike.

## 9.16 Rôzne ustanovenia 

### 9.16.1 Celistvosť zmluvy 
Žiadne ustanovenia.

### 9.16.2 Postúpenie 
Odberateľ/Držiteľ nesmie postúpiť, previesť alebo inak nakladať s právami, povinnosťami alebo nárokmi tretej strany podľa zmluvy alebo Všeobecných podmienok bez písomného súhlasu Poskytovateľa.

### 9.16.3 Oddeliteľnosť 
Ak sa akékoľvek ustanovenie týchto CP/CPS stane neplatným alebo nevymáhateľným, nespôsobuje to neplatnosť alebo nevymáhateľnosť celých CP/CPS, ak je úplne oddeliteľné od ostatných ustanovení týchto CP/CPS. Poskytovateľ okamžite nahradí neplatné alebo nevymáhateľné ustanovenie CP/CPS novými platnými a vymáhateľnými ustanoveniami, ktorých predmet bude čo najviac zodpovedať predmetu pôvodného ustanovenia a zároveň bude zachovaný účel týchto CP/CPS a obsah jednotlivých ustanovení týchto CP/CPS.

### 9.16.4 Vymáhateľnosť 
V prípade, že určité právo nie je uplatnené počas trvania zmluvného vzťahu medzi stranami, toto právo nezaniká z dôvodu jeho neuplatnenia, ak nie je uvedené inak.

Z dôvodu zrušenia zmluvného vzťahu medzi zmluvnými stranami nie sú strany zbavené povinnosti splniť všetky záväzky vyplývajúce z doteraz uplatnených práv a vykonať všetky potrebné právne úkony, ktoré nesnesú odklad a ktoré sú nevyhnutné na zabránenie škode.

### 9.16.5 Vyššia moc (Force Majeure) 
Poskytovateľ, Odberateľ/Držiteľ nezodpovedajú za omeškanie plnenia svojich povinností v dôsledku okolností vylučujúcich zodpovednosť (vyššia moc).

Okolnosťou vylučujúcou zodpovednosť je prekážka, ktorá nastala nezávisle od vôle povinnej strany a bráni jej v splnení jej povinnosti, ak nemožno rozumne predpokladať, že povinná strana túto prekážku alebo jej následky odvráti alebo prekoná a že v čase vzniku prekážky mohla prekážku predvídať alebo nie. 

Ak nastanú okolnosti vylučujúce zodpovednosť, potom strana, u ktorej takéto okolnosti nastanú, okamžite informuje druhú stranu o povahe, začiatku a konci takejto prekážky plnenia svojich povinností. Poskytovateľ, Odberateľ/Držiteľ sa zaväzujú urobiť maximum pre odvrátenie a prekonanie okolností vylučujúcich zodpovednosť. 

Zodpovednosť však nie je vylúčená, ak takáto okolnosť nastala až v čase, keď už bola povinná strana v omeškaní so splnením svojej povinnosti, alebo ak dotknutá strana nesplní svoju povinnosť okamžite informovať druhú stranu o povahe a začiatku trvania prekážky, alebo ak vznikla z hospodárskych pomerov. Účinky vylučujúce zodpovednosť sú obmedzené len na obdobie, počas ktorého trvá prekážka, s ktorou sú tieto účinky spojené.

## 9.17 Ostatné ustanovenia
Žiadne ustanovenia.
