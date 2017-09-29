---
title: "Finanšu pārskata data mart atiestatīšana pēc datu bāzes atjaunošanas"
description: "Šajā tēmā ir aprakstīts, kā atiestatīt finanšu pārskatu data mart pēc Microsoft Dynamics 365 for Finance and Operations datu bāzes atjaunošanas."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: lv-lv
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Finanšu pārskata data mart atiestatīšana pēc datu bāzes atjaunošanas

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kā atiestatīt finanšu pārskatu data mart pēc Microsoft Dynamics 365 for Finance and Operations datu bāzes atjaunošanas.

Ja atjaunojat Finance and Operations datu bāzi no dublējuma vai kopējat datu bāzi no citas vides, ir jāizpilda šajā tēmā norādītās darbības, lai nodrošinātu, ka finanšu pārskata data mart ir pareizi, izmantojot atjaunoto Finance and Operations datu bāzi. 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> Šī procesa darbības tiek atbalstītas Dynamics 365 for Operations 2016. gada maija laidienā (programmas būvējums 7.0.1265.23014 un finanšu pārskatu būvējums 7.0.10000.4) un jaunākos laidienos. Ja lietojat vecāku Dynamics 365 for Finance and Operations laidienu, sazinieties ar mūsu atbalsta dienestu, lai saņemtu palīdzību.

## <a name="export-report-definitions"></a>Pārskatu definīciju eksportēšana
Vispirms eksportējiet pārskatu dizainus no pārskatu veidotāja, veicot tālāk norādītās darbības.

1.  Pārskatu veidotājā pārejiet uz sadaļu **Uzņēmums** &gt; **Veidošanas bloku grupas**.
2.  Atlasiet eksportējamo veidošanas bloku grupu un noklikšķiniet uz **Eksportēt**. 
    > [!Note] 
    > Programmatūrā Dynamics 365 for Finance and Operations tiek atbalstīta tikai viena veidošanas bloku grupa **Noklusējuma**.
3.  Atlasiet eksportējamās pārskatu definīcijas, veicot tālāk norādītās darbības.
    -   Lai eksportētu visas pārskatu definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.
    -   Lai eksportētu noteiktas atskaites, rindas, kolonnas, koku struktūras vai dimensiju kopas, noklikšķiniet uz atbilstošās cilnes un pēc tam atlasiet eksportējamos vienumus. Lai atlasītu vairākas cilnes vienības, piespiediet un turiet taustiņu Ctrl. Atlasot eksportējamos pārskatus, tiek atlasītas saistītās rindas, kolonnas, koku struktūras un dimensiju kopas.

4.  Noklikšķiniet uz **Eksportēt**.
5.  Ievadiet faila nosaukumu un atlasiet drošu atrašanās vietu, kur vēlaties saglabāt eksportētās pārskatu definīcijas.
6.  Noklikšķiniet uz **Saglabāt**.

Failu var kopēt vai augšupielādēt drošā atrašanās vietā, lai vēlāk to varētu importēt citā vidē. Informācija par Microsoft Azure krātuves konta lietošanu ir pieejama tēmā [Datu pārsūtīšana, izmantojot komandrindas utilītu AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Microsoft krātuves kontu nenodrošina Dynamics 365 for Finance and Operations līguma ietvaros. Jums ir jāiegādājas krātuves konts vai jāizmanto atsevišķa Azure abonementa krātuves konts. 
> [!WARNING]
> Ņemiet vērā D diska darbību Azure virtuālajās mašīnās. Ilgstoši neglabājiet tajā eksportētās veidošanas bloku grupas. Papildinformāciju par pagaidu diskiem skatiet tēmā [Izpratne par pagaidu disku Windows Azure virtuālajās mašīnās](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Pakalpojumu apturēšana
Izmantojiet attālo darbvirsmu, lai izveidotu savienojumu ar visiem vidē ietvertajiem datoriem un apturētu tālāk norādītos Windows pakalpojumus, izmantojot failu services.msc.

-   Globālā tīmekļa publicēšanas pakalpojums (visos AOS datoros)
-   Microsoft Dynamics 365 for Finance and Operations lielapjoma pārvaldības pakalpojums (tikai tajos AOS datoros, kas nav privāti)
-   Management Reporter 2012 apstrādes pakalpojums (tikai BI datoros)

Šiem pakalpojumiem ir atvērti savienojumi ar Dynamics 365 for Finance and Operations datu bāzi.

## <a name="reset"></a>Atcelt izmaiņas
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>Atrodiet un lejupielādējiet jaunāko MinorVersionDataUpgrade.zip pakotni

Atrodiet jaunāko MinorVersionDataUpgrade.zip pakotni, izmantojot norādījumus, kas ir sniegti tēmā [Lejupielādēt jaunāko izvietojamo datu jaunināšanas pakotni](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package). Norādījumos ir paskaidrots, kā noteikt un lejupielādēt pareizo datu jaunināšanas pakotnes versiju. Jauninājums nav nepieciešams, lai lejupielādētu MinorVersionDataUpgrade.zip pakotni. Ir tikai jāizpilda sadaļā "Lejupielādēt jaunāko izvietojamo datu jaunināšanas pakotni" norādītās darbības, neveicot nekādas citas rakstā norādītās darbības MinorVersionDataUpgrade.zip pakotnes kopijas izgūšanai.

#### <a name="execute-scripts-against-finance-and-operations-database"></a>Skripta izpilde ar Dynamics 365 for Finance and Operations datu bāzi

Izpildiet tālāk norādītos skriptus ar Dynamics 365 for Finance and Operations datu bāzi (nevis ar finanšu pārskatu datu bāzi).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Šie skripti nodrošina to, ka lietotāju, lomu un izmaiņu izsekošanas iestatījumi ir pareizi.

#### <a name="execute-powershell-command-to-reset-database"></a>PowerShell komandas izpilde, lai atiestatītu datu bāzi

AOS datorā tiešā veidā izpildiet tālāk norādīto komandu, lai atiestatītu Dynamics 365 for Finance and Operations un finanšu pārskatu integrāciju.

1.  Atveriet čaulu Windows PowerShell, izmantojot lomu Administrators.
2.  Izpildiet šo komandu: F:
3.  Izpildiet šo komandu: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Izpildiet šo komandu: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  Izpildiet šo komandu: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;mans atiestatīšanas iemesls&gt;”
    -   Tiek prasīts ievadīt “Y”, lai apstiprinātu.

Tālāk ir sniegts parametru paskaidrojums.

-   Parametra -Reason derīgās vērtības ir: SERVICING, BADDATA, OTHER.
-   Parametra -ReasonDetail vērtība ir brīvs teksts.
-   Parametru Reason un ReasonDetail vērtības tiek reģistrētas telemetrijas/vides pārraudzības žurnālā.

## <a name="start-services"></a>Pakalpojumu startēšana
Izmantojiet failu services.msc, lai atkal startētu pakalpojumus, ko iepriekš apturējāt.

-   Globālā tīmekļa publicēšanas pakalpojums (visos AOS datoros)
-   Microsoft Dynamics 365 for Finance and Operations lielapjoma pārvaldības pakalpojums (tikai tajos AOS datoros, kas nav privāti)
-   Management Reporter 2012 apstrādes pakalpojums (tikai BI datoros)

## <a name="import-report-definitions"></a>Pārskatu definīciju importēšana
Importējiet pārskatu dizainus no pārskatu veidotāja, izmantojot eksportēšanas laikā izveidoto failu.

1.  Pārskatu veidotājā pārejiet uz sadaļu **Uzņēmums** &gt; **Veidošanas bloku grupas**.
2.  Atlasiet eksportējamo veidošanas bloku grupu un noklikšķiniet uz **Eksportēt**. 

    > [!NOTE]
    > Programmatūrā Dynamics 365 for Finance and Operations tiek atbalstīta tikai viena veidošanas bloku grupa **Noklusējuma**.
    
3.  Atlasiet veidošanas bloku **Noklusējuma** un noklikšķiniet uz **Importēt**.
4.  Atlasiet failu, kurā ir ietvertas eksportētās pārskatu definīcijas, un noklikšķiniet uz **Atvērt**.
5.  Dialoglodziņā Importēt atlasiet importējamās pārskatu definīcijas.
    -   Lai importētu visas atskaites definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.
    -   Lai importētu atsevišķus pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas, atlasiet importējamos pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas.

6.  Noklikšķiniet uz **Importēt**.




