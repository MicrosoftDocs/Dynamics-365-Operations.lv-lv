---
title: "Organizācijas administrēšanas sākumlapa"
description: "Šajā tēmā ir norādīti resursi, kas jums palīdzēs izmantot programmatūru Microsoft Dynamics 365 for Finance and Operations savā organizācijā."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: a2c1d846527eac4db0a043c7f1c51da0e73bd796
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="organization-administration-home-page"></a>Organizācijas administrēšanas sākumlapa

[!INCLUDE [banner](../includes/banner.md)]

Šajā tēmā ir norādīts saturs, kas prasmīgiem lietotājiem un administratoriem palīdzēs konfigurēt programmatūru Microsoft Dynamics 365 for Finance and Operations. Šis saturs viņiem palīdzēs sistēmu konfigurēt tā, lai jūsu organizācijai un komercdarbībai tā darbotos efektīvi un bez traucējumiem.

Liela daļa no šeit uzskaitītā satura attiecas uz līdzekļiem modulī **Organizācijas administrēšana**. Taču ir pāris uzdevumu, piemēram, ieraksta veidņu izveidošana un lietošana, ko var veikt jebkurā modulī, lai palīdzētu jūsu organizācijai darboties efektīvāk. 

<a name="number-sequences"></a>Numuru sērijas
----------------
Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus identifikatorus pamatdatu ierakstiem un transakciju ierakstiem, kam ir nepieciešami identifikatori. Pamatdatu ieraksts vai darījuma ieraksts, kam nepieciešams identifikators, tiek saukts par *atsauci*. Pirms atsaucei varat izveidot jaunus ierakstus, ir jāiestata numuru sērija un tā jāsaista ar atsauci.

-   [Numuru sēriju apskats](number-sequence-overview.md)
-   [Numuru sēriju iestatīšana, izmantojot vedni](tasks/set-up-number-sequences-wizard.md) (uzdevuma ceļvedis)
-   [Atsevišķu numuru sēriju iestatīšana](tasks/set-up-number-sequences-individual-basis.md) (uzdevuma ceļvedis)

## <a name="organizations"></a>Organizācijas
Organizācija ir cilvēku grupa, kas strādā kopā, lai nodrošinātu biznesa procesu vai sasniegtu mērķi. Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu.

Pirms organizāciju un organizāciju hierarhiju iestatīšanas programmatūrā Finance and Operations noteikti izplānojiet sava uzņēmuma modelēšanas veidu. Organizācijas modelis būtiski ietekmē Finance and Operations ieviešanu un biznesa procesus.

-   [Organizācijas un organizāciju hierarhijas](organizations-organizational-hierarchies.md)
-   [Organizācijas hierarhijas plānošana](plan-organizational-hierarchy.md)
-   [Organizācijas hierarhijas izveide](tasks/create-organization-hierarchy.md) (uzdevuma ceļvedis)
-   [Juridiskas personas izveide](tasks/create-legal-entity.md) (uzdevuma ceļvedis)
-   [Pārvaldības struktūrvienības izveide](tasks/create-operating-unit.md) (uzdevuma ceļvedis)

## <a name="address-books"></a>Adrešu grāmatas
Globālā adrešu grāmata ir centralizēts repozitorijs pamatdatiem, kas jāglabā par visām iekšējām un ārējām personām un organizācijām, ar kurām uzņēmums mijiedarbojas. Ar pušu ierakstiem saistītie dati ietver personas nosaukumu/vārdu un uzvārdu, adresi un kontaktinformāciju. 

Pēc globālās adrešu grāmatas izveidošanas pēc nepieciešamības varat izveidot papildu adrešu grāmatas, piemēram, atsevišķu adrešu grāmatu katram uzņēmumam jūsu organizācijā vai katrai biznesa jomai. 

-   [Globālā adrešu grāmata](overview-global-address-book.md)
-   [Globālās adrešu grāmatas un papildu adrešu grāmatu konfigurācijas plānošana](plan-configuration-global-address-book-additional-address-books.md)
- [Globālās adrešu grāmatas konfigurēšana](tasks/configure-global-address-book.md)
-   [Bieži uzdotie jautājumi par adrešu grāmatām](qa-address-books.md)


## <a name="workflow"></a>Darbplūsma
Darbplūsma ir sistēma, kas tiek instalēta ar programmatūru Finance and Operations, un to jūs var izmantot, lai izveidotu atsevišķas darbplūsmas vai biznesa procesus. Kad izveidojat darbplūsmu, jūs norādāt veidu, kā dokuments plūst jeb pārvietojas caur sistēmu, norādot, kam ir jāizpilda uzdevums, jāpieņem lēmums vai jāapstiprina dokuments. 

-   [Darbplūsmas pārskats](overview-workflow-system.md)
-   [Darbplūsmas elementi](workflow-elements.md)
-   [Darbplūsmas darbības](workflow-actions.md)
-   [Izveidot darbplūsmu](create-workflow.md)

## <a name="electronic-signatures"></a>Elektroniskie paraksti
Elektroniskais paraksts apstiprina personas identitāti, kas gatavojas sākt vai apstiprināt skaitļošanas procesu. Dažās nozarēs elektroniskais paraksts ir tikpat juridiski saistošs kā ar roku veikts paraksts. Vairākās regulētas nozarēs, piemēram, farmācijas, pārtikas un dzērienu un aviācijas un aizsardzības nozarēs, elektronisko parakstu izmantošana ir normatīva prasība.

Programmatūrā Dynamics 365 for Finance and Operations varat izmantot elektroniskos parakstus īpaši svarīgiem biznesa procesiem. Dažiem procesiem ir iebūvētas elektronisko parakstu iespējas. Varat arī izveidot pielāgotas parakstu prasības jebkurai datu bāzes tabulai un laukam.

-   [Elektronisko parakstu apskats](electronic-signature-overview.md)
-   [Elektronisko parakstu iestatīšana](tasks/set-up-electronic-signatures.md) (uzdevuma ceļvedis)

## <a name="case-management"></a>Pieteikumu pārvaldība
Veicot gadījumu plānošanu, izsekošanu un analīzi, var izstrādāt efektīvus risinājumus, ko var izmantot līdzīgām problēmām. Piemēram, kad klientu apkalpošanas pārstāvji vai cilvēkresursu nodaļas darbinieki veido gadījumus, zināšanu dokumentos viņi var atrast informāciju, kura viņiem palīdz efektīvāk strādāt ar gadījumiem vai tos atrisināt. 

-   [Pieteikumu pārvaldības apskats](cases.md)
-   [Konfigurēt pieteikumu drošību, procesus un kategorijas](plan-case-management.md)

## <a name="record-templates"></a>Ierakstu veidnes
Ierakstu veidnes var jums palīdzēt izveidot ierakstus ātrāk. Varat izveidot ierakstu veidnes, lai katram jaunajam ierakstam nevajadzētu atkārtoti ievadīt bieži izmantotās lauku vērtības. 

-   [Ierakstu veidnes](record-templates.md)
- [Ieraksta veidnes izveidošana, lai atvieglotu datu ievadi](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (uzdevuma ceļvedis)
- [Ieraksta veidnes izmantošana, lai izveidotu jaunu ierakstu](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (uzdevuma ceļvedis)

## <a name="general-organization-administration"></a>Vispārīgā organizācijas administrēšana
-   [Reklāmkaroga vai logotipa maiņa](../get-started/tasks/change-banner-or-logo.md) (uzdevuma ceļvedis)
- [Dokumentu pārvaldības konfigurēšana](configure-document-management.md)
- [Konfigurēt un sūtīt e-pastu](configure-email.md)
-   [Datuma/laika dati un laika joslas](date-time-zones.md)








