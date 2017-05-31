---
title: "Reģistrācijas ID"
description: "Šajā tēmā ir sniegta informācija par reģistrācijas ID iestatīšanu un lietošanu."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: fc4a56eceb75673b7a044bd8392f8d0cc675e869
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="registration-ids"></a>Reģistrācijas ID

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegta informācija par reģistrācijas ID iestatīšanu un lietošanu.

Daudzām valstīm un reģioniem ir atšķirīgi noteikumi un prasības par ID reģistrācijas numuriem. Šajā tēmā ir sniegts apskats par atbalstīto reģistrācijas tipu nepieciešamajiem iestatījumiem un apstrādi personām dažādās Eiropas valstīs/reģionos. Visās valstīs/reģionos ir to prasības par dažādu valstij specifisku funkcionalitāšu atbalstu saistībā ar dažādu valsts iestāžu piešķirtajiem reģistrācijas numuriem. Reģistrācijas numuri ir, piemēram, sociālās apdrošināšanas numurs (SAN), nodokļa identifikācijas kods (NIK) un Eiropas PVN identifikācija (ES PVN ID). Šis līdzeklis sniedz vienotu struktūru visām valstīm visos reģionos, ņemot vērā valstij specifiskās prasības, kādas pastāv noteiktās Eiropas valstīs. Nākamajās sadaļās ir aprakstīta vispārējā informācijas plūsma, kas tiek izmantota reģistrācijas ID iestatīšanai un apstrādei.

## <a name="registration-type-creation"></a>Reģistrācijas tipa izveidošana
Lai varētu ievadīt reģistrācijas ID, ir jāiestata reģistrācijas tipi dažādajiem reģistrācijas numuru tipiem, kas katrai pusei ir jāievēro. Dodieties uz lapu **Organizācijas administrēšana** &gt; **Globālā adrešu grāmata** &gt; **Reģistrācijas tipi** &gt; **Reģistrācijas tipi**, lai izveidotu un pārvaldītu reģistrācijas tipus kreditoriem, debitoriem, darbiniekiem un juridiskajām personām dažādās valstīs/reģionos.

|Lauks                 |Apraksts      |
|------------------------------|----------------------------|                                                                           
| Nosaukums                | Reģistrācijas tipa nosaukums. |                                                                           
| Apraksts         | Reģistrācijas tipa apraksts. |
| Valsts/reģions      | Unikālais valsts/reģiona identifikators.|
| Nodokļu iestāde       | Nodokļu iestāde, kas ir saistīta ar šo reģistrācijas tipu.|
| Iekļaut       | Ierobežojuma veids, kas attiecas uz šo nodokļa reģistrācijas tipu: Nav, Persona, Organizācija.|
| Formāts              | Reģistrācijas tipa apstiprināšanas formāts.|
| Var atjaunināt      | Definē, vai šim reģistrācijas tipam reģistrācijas numuru pēc ievadīšanas var atjaunināt.|
| Unikāls              | Definē, vai reģistrācijas numurs šim reģistrācijas tipam ir unikāls. |
| Primārā valstij | Ja puse attiecīgajā valstī ir saistīta ar vienu vai vairākām adresēm un šis reģistrācijas ID ir derīgs visām šīm adresēm, jums šai valstij viena adrese ir jānorāda kā primārā. Tikai vienu ID var reģistrēt kā primāro. Definē, vai reģistrācijas numuru var ievadīt tikai primārajai valsts adresei. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Piešķirt reģistrācijas tipu kādai reģistrācijas kategorijai
Reģistrācijas kategorija ir valsts/reģiona reģistrācijas identifikators, kas ir attiecīgajā valstī/reģionā apstiprināts lietošanai attiecībā uz nodokļiem, muitu un citiem nolūkiem. Šī kategorija definē kārtulas konkrēta reģistrācijas ID validēšanai (tostarp kontrolciparus un citas) un reģistrācijas ID iekļaušanai dažādos pārskatos. Lai konkrētas valsts reģistrācijas tipu piešķirtu atbalstītai reģistrācijas kategorijai, izmantojiet lapu **Organizācijas administrēšana** &gt; **Globālā adrešu grāmata** &gt; **Reģistrācijas tipi** &gt; **Reģistrācijas kategorijas**.

| Lauks            | Apraksts|
|-----------------------|----------------|
| Reģistrācijas tips     | Reģistrācijas tips konkrētajā valstī/reģionā.|
| Iekļaut         | Ierobežojuma veids, kas attiecas uz nodokļa reģistrācijas tipu: Nav, Persona, Organizācija.|
| Reģistrācijas kategorija | Unikālais reģistrācijas identifikators, kurš ir apstiprināts lietošanai attiecīgajā valstī. Tālāk ir sniegts pilns saraksts ar versijā AX7.1 atbalstītajām kategorijām. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Ievadīt reģistrācijas ID globālās adrešu grāmatas ierakstiem
Globālā adrešu grāmata programmatūrā Microsoft Dynamics 365 for Operations satur konsolidētu adrešu informāciju debitoriem, kreditoriem, kontaktpersonām, biznesa attiecībām un juridiskajām personām. Papildinformāciju skatiet rakstā, [Globālās adrešu grāmatas apskats](/dynamics365/operations/organization-administration/overview-global-address-book). Puses ierakstos, kas saglabāti globālajā adrešu grāmatā, var būt viens vai vairāki adrešu ieraksti. Šīs adreses tiek izmantotas dažādiem nolūkiem, piemēram, norēķiniem vai piegādēm. Adrešu informācijai reģistrācijas ID varat iestatīt debitoriem, kreditoriem, darbiniekiem un juridiskajām personām. Atrodiet puses (juridiskās personas, kreditora, debitora, darbinieka) ierakstu, kuram vēlaties ievadīt reģistrācijas ID, un pēc tam ar šo pusi, juridisko personu, kreditoru, debitoru, darbinieku saistītajās formās noklikšķiniet uz **Reģistrācijas ID**, lai atvērtu lapu **Pārvaldīt adreses**. Cilnē **Nodokļa reģistrācija** noklikšķiniet uz **Pievienot** un ievadiet tālāk norādīto informāciju par šo reģistrācijas ID.

|Lauks                |Apraksts                                                |
|---------------------|-----------------------------------------------------------|
| Reģistrācijas tips   | Reģistrācijas tips atlasītajā valstī/reģionā.     |
| Reģistrācijas numurs | Puses reģistrācijas ID.                                |
| Apraksts         | Reģistrācijas numura apraksts.               |
| Sadaļa             | Papildinformācija par šo reģistrācijas numuru. |
| Izdevējiestāde      | Nodokļu iestāde, kas izsniedza šo reģistrācijas numuru.        |
| Izdošanas datums         | Reģistrācijas numura izsniegšanas datums.              |
| Ir spēkā           | Reģistrācijas numura spēkā stāšanās datums.           |
| Termiņa beigas          | Reģistrācijas numura derīguma beigu datums.          |

> [!NOTE]
> Juridiskās personas, kreditora, debitora PVN reģistrācijas numuru var atlasīt no reģistrācijas ID, kuri ir saistīti ar PVN ID, un ievadīt attiecīgajai pusei.

## <a name="search-for-records-by-registration-id"></a>Meklēt ierakstus pēc reģistrācijas ID
Iespēja meklēt puses ierakstus, pamatojoties uz reģistrācijas ID, ir pieejama ar pusi, juridisko personu, kreditoru, debitoru un darbinieku saistītajās formās. Noklikšķiniet uz **Reģistrācijas ID meklēšana**, lai atvērtu lapu **Reģistrācijas ID meklēšanas kritēriji**. Norādiet meklēšanas kritērijus un noklikšķiniet uz **Atrast**. Sistēma parāda atlasītos ierakstus no globālās adrešu grāmatas un saistītos pušu ierakstu tipus.

## <a name="supported-registration-categories"></a>Atbalstītās reģistrācijas kategorijas
Nākamajā tabulā ir uzskaitīti programmatūrā Dynamics 365 for Operations atbalstītie reģistrācijas tipi. Ja pārzināt Microsoft Dynamics AX 2012 laukus, kas paredzēti reģistrācijas ID, tabulā šie lauki ir kartēti arī uz Dynamics 365 for Operations reģistrācijas kategorijām.

| Dynamics 365 for Operations reģistrācijas kategorija         |Valsts/reģions  | Dynamics AX 2012 termins/lauks|
|---------------------------------------------------------------|---------------------|---------------------------------|
| PVN ID                                                        | Visas Eiropas Savienības (ES) valstis|  PVN reģistrācijas numurs (Tiesību aktos noteiktais nodokļa ID versijā AX2012 R3)|
| Uzņēmuma ID (COID)                                          | Beļģija Čehija Igaunija Ungārija Latvija Lietuva Polija Šveice | Uzņēmuma numurs (EnterpriseNumber) Reģistrācijas numurs (RegNum\_W) Reģistrācijas numurs (RegNum\_W) Reģistrācijas numurs (RegNum\_W) Reģistrācijas numurs (RegNum\_W) Uzņēmuma kods (EnterpriseCode) Reģistrācijas numurs (RegNum\_W) UID (Tiesību aktos noteiktais UID versijā AX2012 R3) |
| Filiāles ID                                                     | Beļģija            | Filiāles numurs (BranchNumber)|
| Spisová značka (Reģistrācijas numurs, Izdevējiestāde, Sadaļa) | Čehija     | Iekļaušanas numurs (CommercialRegisterInsetNumber) Glabājas komercreģistrā (CommercialRegister) Komercreģistra sadaļa (CommercialRegisterSection)|
| Debitora muitas ID                                           | Somija | Debitora muitas numurs (CustomsCustomerNumber\_FI)|
| INN                                                           | Krievijas Federācija| INN (Tiesību aktos noteiktā tipa INN versijā AX2012 R3)|
| RRC                                                           | Krievijas Federācija| RRC (Tiesību aktos noteiktā tipa RRC versijā AX2012 R3)|
| OKDP                                                          | Krievijas Federācija| OKDP (Tiesību aktos noteiktā tipa OKDP versijā AX2012 R3)|
| OKPO                                                          | Krievijas Federācija| OKPO (Tiesību aktos noteiktā tipa OKPO versijā AX2012 R3)|
| RCOAD                                                         | Krievijas Federācija| RCOAD (Tiesību aktos noteiktā tipa RCOAD versijā AX2012 R3)|
| OGRN                                                          | Krievijas Federācija| OGRN (Tiesību aktos noteiktā tipa OGRN versijā AX2012 R3) |
| SNILS                                                         | Krievijas Federācija| SNILS (Tiesību aktos noteiktā tipa SNILS versijā AX2012 R3)|
| CIFTS                                                         | Krievijas Federācija| CIFTS (Tiesību aktos noteiktā tipa CIFTS versijā AX2012 R3)|

Papildinformāciju par reģistrācijas ID apstrādāšanu, tostarp nepieciešamajiem priekšnosacījumiem, skatiet tālāk norādītajos uzdevumu ierakstos, kas paredzēti PVN ID pakalpojumā Lifecycle Services (LCS).

-   Iestatīt PVN ID
-   Kreditora PVN ID reģistrācija
-   Pušu meklēšana pēc PVN ID





