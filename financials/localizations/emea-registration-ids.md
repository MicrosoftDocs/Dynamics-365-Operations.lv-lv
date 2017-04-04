---
title: "Reģistrācijas ID"
description: "Šajā tēmā ir sniegta informācija par iestatīšanu un lietošanu reģistrācijas ID."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>Reģistrācijas ID

Šajā tēmā ir sniegta informācija par iestatīšanu un lietošanu reģistrācijas ID.

Daudzām valstīm un reģioniem ir atšķirīgi noteikumi un prasības attiecībā uz ieraksta ID vai reģistrācijas numurus. Šajā tēmā ir sniegts pārskats par nepieciešamos uzstādījumus un atbalstīto reģistrācijas tipu apstrāde personām dažādās Eiropas valstīs/reģionos. Visās valstīs/reģionos ir savas prasības atbalstam dažādās valstij funkcijām saistībā ar valsts reģistrācijas numuri, ko dažādās valsts iestādēs. Reģistrācijas numuru piemēri, sociālās apdrošināšanas numurs (SAN), nodokļu identifikācijas numurs (DDIN) un Eiropas PVN identifikators (ES PVN ID). Šis līdzeklis nodrošina vienotu regulējumu visās valstīs, visos reģionos, ņemot vērā valsts specifiskās prasības dažās Eiropas valstīs. Nākamajās sadaļās ir aprakstīts, informāciju, kas tiek izmantots iestatīšanas un apstrādes reģistrācijas ID kopējā plūsma.

## <a name="registration-type-creation"></a>Reģistrācijas tipa izveide
Lai varētu ievadīt reģistrācijas ID, jāuzstāda reģistrācijas tipiem dažāda veida reģistrācijas numuri, ko katra puse ir pakļauta. Dodieties uz **organizācijas administrācija**&gt;**globālajā adrešu grāmatā**&gt;**reģistrācijas tipiem**&gt;**reģistrācijas tipiem** lapu, lai izveidotu un pārvaldītu tipus, reģistrācija, piegādātājiem, klientiem, darbiniekiem un juridiskām vienībām dažādās valstīs/reģionos.

|Lauks                 |apraksts      |
|------------------------------|----------------------------|                                                                           
| Vārds, uzvārds                | Reģistrācijas tipa nosaukums. |                                                                           
| apraksts         | Reģistrācijas tipa apraksts. |
| Valsts/reģions      | Valsts/reģiona unikālais identifikators.|
| Nodokļu iestāde       | Nodokļu iestādei, kas ir saistīta ar reģistrācijas tips.|
| Iekļaut       | Tāda veida ierobežojums, kas attiecas uz nodokļu reģistrācijas tipu: neviena persona, organizācija.|
| Formāts              | Reģistrācijas tipa apstiprināšanas formātā.|
| Var atjaunināt      | Definē, vai reģistrācijas numurs, reģistrācijas veidam var atjaunināt pēc to ievadīšanas.|
| Unikāls              | Definē, vai reģistrācijas tipa reģistrācijas numurs ir unikāls. |
| Primārā valstij | Ja puse ir saistīta ar vienu vai vairākas adreses īpaši valsts un reģistrācijas ID nav derīgs visām šīm adresēm, viena adrese jānorāda kā primāro valsts. Viens ID var reģistrēt tikai kā primāro. Definē, vai reģistrācijas numuru var ievadīt tikai primāro valsts adreses. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Piešķirt kategorijai reģistrācijas reģistrācijas tips
Reģistrācijas kategorijas ir valsts/reģiona reģistrācijas identifikators, kas apstiprinātas lietošanai, īpaši valsts/reģiona nodokļu, muitas un citiem mērķiem. Šai kategorijai nosaka apstiprināšanas noteikumiem ar īpašu reģistrācijas ID (tajā skaitā pārbaudes cipari u.c.) un iekļaušanu reģistrācijas ID dažādas atskaites. Lietojiet lapu **organizācijas administrācija**&gt;**globālajā adrešu grāmatā**&gt;**reģistrācijas tipiem**&gt;**reģistrācijas kategorijas** reģistrācijas veidu konkrētai valstij jāpiešķir atbalstīto reģistrācijas kategorijas.

| Lauks            | apraksts|
|-----------------------|----------------|
| Reģistrācijas veids     | Reģistrācijas tipa īpaši valstij/reģionam.|
| Iekļaut         | Tāda veida ierobežojums attiecas uz nodokļu reģistrācijas tips: neviena persona, organizācija.|
| Reģistrācijas kategorija | Unikāls reģistrācijas identifikatoru, kas apstiprinātas lietošanai šajā valstī. Pilnu sarakstu atbalstīja AX7.1 kategorijām ir zemāk. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Ievadiet reģistrācijas ID globālajā adrešu kataloga ierakstus
Globālajā adrešu grāmatā (GAB.), Microsoft Dynamics 365 operācijām ir Konsolidēts adreses informāciju klientiem, piegādātājiem, kontaktpersonām biznesa attiecības un juridiskajām personām. Lai iegūtu vairāk informācijas, skatiet [globālo adrešu grāmatu apskats](/dynamics365/operations/organization-administration/overview-global-address-book). Puse ieraksti, kas tiek glabāti globālajā adrešu grāmatā var būt viens vai vairāki adrešu ierakstus. Šīs adreses tiek izmantotas dažādiem nolūkiem, piemēram, norēķiniem vai piegādēm. Var iestatīt reģistrācijas ID adrešu informāciju klientiem, piegādātājiem, darbiniekiem un juridiskajām personām. Persona (juridiska persona, piegādātāju, klientu, darbinieku) ierakstu, kuram ievadiet reģistra ID un pēc tam noklikšķiniet uz atrast **reģistrācijas ID** par formām, kas saistītas ar puse, juridiska persona, piegādātāju, klientu, darbinieku, lai atvērtu **pārvaldīt adreses** lapā. Par **nodokļu reģistrācijas** cilni, noklikšķiniet uz **pievienot**, un ievadiet šādu informāciju par reģistrācijas ID.

|Lauks                |apraksts                                                |
|---------------------|-----------------------------------------------------------|
| Reģistrācijas veids   | Reģistrācijas tips atlasītā valsts/reģions.     |
| Reģistrācijas numurs | Personu reģistrācijas ID.                                |
| apraksts         | Reģistrācijas numura aprakstu.               |
| Sadaļa             | Papildu informāciju par reģistrācijas numurs. |
| Izdevējiestāde      | Iestādi, kas izsniegusi reģistrācijas numurs.        |
| Izdošanas datums         | Izdots datums reģistrācijas numurs.              |
| Ir spēkā           | Spēkā stāšanās datuma attiecībā uz reģistrācijas numurs.           |
| Termiņa beigas          | Reģistrācijas numura derīguma termiņu.          |

> [!NOTE]
> Nodokļu reģistrācijas numurs juridiskai personai, kreditoru, debitoru var atlasīt no reģistrācijas ID, kas saistīti ar PVN ID un puse ir ievadīts.

## <a name="search-for-records-by-registration-id"></a>Meklēt ierakstus reģistrācijas ID
Meklēt personu ierakstus, kas balstās uz reģistrācijas ID būtu pieejams par formām, kas saistītas ar personu, juridisku personu, kreditoru, klientu un strādnieku. Noklikšķiniet uz **reģistrācijas ID meklēšana** atvērt **reģistrācijas ID meklēšanas kritērijus** lapā. Norādiet meklēšanas kritērijus un noklikšķiniet uz **atrast**. Sistēma parādīs atlasītos ierakstus no globālā adrešu grāmata un saistīto personu ieraksta veidu.

## <a name="supported-registration-categories"></a>Atbalstīto reģistrācijas kategorijas
Šajā tabulā ir atbalstīts reģistrācijas tipiem programmā Dynamics 365 operācijām. Ja jūs esat iepazinušies ar Microsoft Dynamics AX 2012 laukus reģistrācijas ID, šī tabula arī kartes šajās jomās Dynamics 365 operācijas reģistrācijas kategorijas.

| Dinamika 365 operācijas reģistrācijas kategorijas         |Valsts/reģions  | Dynamics AX 2012 terminu/lauku|
|---------------------------------------------------------------|---------------------|---------------------------------|
| PVN ID                                                        | Visām valstīm Eiropas Savienības (ES)|  PVN maksātāja reģistrācijas numurs (likumdošanas tipa TAX ID AX2012 R3)|
| Uzņēmuma ID (COID)                                          | Beļģija Čehijas Republika Igaunija Ungārija Latvija Lietuva Polija Šveice | Uzņēmuma numurs (EnterpriseNumber) reģistrācijas numurs (RegNum\_W) reģistrācijas numurs (RegNum\_W) reģistrācijas numurs (RegNum\_W) reģistrācijas numurs (RegNum\_W) uzņēmuma kods (EnterpriseCode) reģistrācijas numurs (RegNum\_W) UID (likumdošanas tipa UID AX2012 R3) |
| Filiāles ID                                                     | Beļģija            | Filiāles numuru (BranchNumber)|
| Spisová značka (reģistrācijas numurs, izdevēja aģentūra, sadaļa) | Čehijas Republika     | Gravējums numuru (CommercialRegisterInsetNumber) tur tirdzniecības reģistrā komercreģistrā (CommercialRegisterSection) (CommercialRegister) sadaļā|
| Pielāgotais debitora ID                                           | Somija | Muitas klientu skaits (CustomsCustomerNumber\_FI)|
| Nodokļu maksātāja kods                                                           | Krievijas Federācija| INN (likumdošanas tipa INN AX2012 R3)|
| RIK                                                           | Krievijas Federācija| Rik (likumdošanas tipa Rik AX2012 R3)|
| OKDP                                                          | Krievijas Federācija| OKDP (likumdošanas tipa OKDP AX2012 R3)|
| OKPO                                                          | Krievijas Federācija| OKPO (likumdošanas tipa OKPO AX2012 R3)|
| VATIOK                                                         | Krievijas Federācija| RCOAD (likumdošanas tipa RCOAD AX2012 R3)|
| OGRN                                                          | Krievijas Federācija| OGRN (likumdošanas tipa OGRN AX2012 R3) |
| SNILS                                                         | Krievijas Federācija| SNILS (likumdošanas tipa SNILS AX2012 R3)|
| CIFTS                                                         | Krievijas Federācija| CIFTS (likumdošanas tipa CIFTS AX2012 R3)|

Plašāku informāciju par reģistrācijas ID apstrāde, ieskaitot nepieciešamo priekšnoteikumu, skatīt šādu uzdevumu ierakstus par PVN ID Lifecycle Services (LCS):

-   Iestatīt PVN ID
-   Kreditoru reģistrācija PVN ID
-    Pušu meklēšana pēc PVN ID



