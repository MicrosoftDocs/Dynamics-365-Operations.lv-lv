---
title: "Finanšu pārskata datu mart reset pēc datu bāzes atjaunošanu"
description: "Šajā tēmā ir aprakstīts, kā atiestatīt finanšu atskaišu datu mart pēc atjaunošanas Microsoft Dynamics 365 operācijas datu bāzei."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Finanšu pārskata datu mart reset pēc datu bāzes atjaunošanu

Šajā tēmā ir aprakstīts, kā atiestatīt finanšu atskaišu datu mart pēc atjaunošanas Microsoft Dynamics 365 operācijas datu bāzei. 

Pastāv vairāki scenāriji, kur iespējams atjaunot no dublējuma Dynamics 365, datu bāzes operācijas vai kopēt datu bāzi no cita vide. Šādā gadījumā nepieciešams ievērot attiecīgus pasākumus, lai nodrošinātu, ka finanšu atskaišu datu mart pareizi izmantojot atjaunotā dinamika 365 operāciju bāzi. Ja jums ir jautājumi par finanšu atskaišu datu mart atiestatīšanu iemeslu dēļ ārpus Dynamics 365 operācijas datu bāzes atjaunošana, skatiet [atiestatīt vadības reportieris datu mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) plašāku informāciju. Piezīme soļi šajā procesā ir piemērota Dynamics 365 operācijai maija 2016 release (App veidot 7.0.1265.23014 un finanšu atskaišu izveides 7.0.10000.4) un jaunākas releases. Ja jums ir iepriekšējā laidiena Dynamics 365 operācijām, sazinieties ar mūsu atbalsta komandas palīdzību.

## <a name="export-report-definitions"></a>Eksportēt pārskatu definīcijas
Vispirms eksportējiet pārskatu dizainu atrodas Report Designer, veicot šādas darbības:

1.  Report Designer, lai nokļūtu **Company**&gt;**veidošanas bloku grupām**.
2.  Atlasiet eksportēt, un noklikšķiniet uz veidošanas bloku grupu **eksporta**. **Piezīme:** Dynamics 365 operācijām, tikai vienu veidošanas bloku grupa atbalsta, **Default**.
3.  Atlasiet eksportēt atskaiti definīcijas:
    -   Lai eksportētu visas pārskatu definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.
    -   Lai eksportētu noteiktas atskaites, rindas, kolonnas, koku struktūras vai dimensiju kopas, noklikšķiniet uz atbilstošās cilnes un pēc tam atlasiet eksportējamos vienumus. Lai atlasītu vairākas cilnes vienības, piespiediet un turiet taustiņu Ctrl. Kad izvēlaties eksportēt atskaites, atlasītas saistītās rindas, kolonnas, koki un dimensiju kopas.

4.  Noklikšķiniet uz **eksporta**.
5.  Ievadiet faila nosaukumu un izvēlieties drošā vietā, kur vēlaties saglabāt eksportēto ziņojumu definīcijas.
6.  Click **Save**.

Failu var kopēt vai augšupielādēts drošā vietā, pieļaujot to ieved citā vidē, citā reizē. Var atrast informāciju par Microsoft Azure glabāšanas kontu [pārsūtīt datus ar AzCopy komandrindas utilīta](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Piezīme:** Microsoft nesniedz glabāšanas kontu ietvaros Dynamics 365 nolīgums operācijām. Ir pirkšanas krātuves kontam vai izmantot krātuves kontam no debeszils atsevišķs abonements. **Svarīgi:** jāapzinās D disku Azure virtuālās mašīnas uzvedība. Nevar saglabāt savu eksportēto veidošanas bloku grupām šeit pastāvīgi. Plašāku informāciju par pagaidu diskiem skatiet [izpratne pagaidu diska Windows Azure virtuālās mašīnas](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Apturētu pakalpojumus
Izmantot attālās darbvirsmas savienojumu ar visiem datoriem vidē un apturēt šādus Windows pakalpojumus, izmantojot Services. msc:

-   Globālā tīmekļa publicēšanas pakalpojumu (no visiem AOS datoriem)
-   Microsoft Dynamics 365 darbību partijas vadības pakalpojumu (datoros un privātā sektora AOS tikai)
-   Pārvaldības reportieris 2012 apstrādes pakalpojumi (tikai BI datoros)

Šie pakalpojumi būs atvērta savienojumus ar Dynamics 365 operāciju bāzes.

## <a name="reset"></a>Atcelt izmaiņas
#### <a name="locate-the-latest-dataupgradezip-package"></a>Atrodiet jaunākos DataUpgrade.zip pakete

Atrodiet jaunākos DataUpgrade.zip pakete virzienos, kas atrodams, izmantojot [lejupielādēt DataUpgrade.zip script](..\migration-upgrade\upgrade-data-to-latest-update.md). Virzieni ir paskaidrots, kā atrast pareizo versiju datu jaunināšanas pakotni jūsu videi.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Izpildīt skriptus pret Dynamics 365 operācijas datu bāzei

Palaist šādu skriptu pret Dynamics 365 operāciju bāzes (nevis pret finanšu atskaišu veidošanas datu bāzē).

-   DataUpgrade.zip\\AosService\\skripti\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\skripti\\GrantAzViewChangeTracking.sql

Šie skripti nodrošina lietotājiem, lomas un izmaiņu reģistrēšanas iestatījumi ir pareizi.

#### <a name="execute-powershell-command-to-reset-database"></a>Izpildīt komandu PowerShell, lai atjaunotu datu bāzi

Izpildīt komandu, tieši AOS datorā, lai atiestatītu Dynamics 365 operācijām un finanšu atskaišu integrāciju:

1.  Atveriet Windows PowerShell kā administrators.
2.  Izpildīt: f
3.  Izpildīt: cd f:\\MRApplicationService\\MRInstallDirectory
4.  Izpildīt: Imports-modulis. \\Servera\\MRDeploy\\MRDeploy.psd1
5.  Izpildīt: Reset DatamartIntegration-cits iemesls - ReasonDetail "&lt;mans iemesls atgriešanai&gt;"
    -   Jums tiks lūgts ievadīt "Y", lai apstiprinātu.

Parametru skaidrojums:

-   Derīgas vērtības - iemesls ir: apkope, BADDATA, citi.
-   -ReasonDetail parametrs ir brīvā tekstā.
-   Iemesls un reasonDetail tiks ierakstīti telemetrijas/vides monitoringu.

## <a name="start-services"></a>Startēt pakalpojumu
Services. msc izmantot lai restartētu pakalpojumus, kuri jums agrāk apturēta:

-   Globālā tīmekļa publicēšanas pakalpojumu (no visiem AOS datoriem)
-   Microsoft Dynamics 365 darbību partijas vadības pakalpojumu (datoros un privātā sektora AOS tikai)
-   Pārvaldības reportieris 2012 apstrādes pakalpojumi (tikai BI datoros)

## <a name="import-report-definitions"></a>Importēt definīcijas atskaiti
Report Designer, izmantojot failu, kas izveidots laikā eksporta importētu jūsu dizainparaugu atskaite:

1.  Report Designer, lai nokļūtu **Company**&gt;**veidošanas bloku grupām**.
2.  Atlasiet eksportēt, un noklikšķiniet uz veidošanas bloku grupu **eksporta**. **Piezīme:** Dynamics 365 operācijām, tikai vienu veidošanas bloku grupa atbalsta, **Default**.
3.  Atlasiet **Default** celtniecības bloku un noklikšķiniet **importa**.
4.  Atlasiet failu, kurā eksportētā atskaite definīcijas un noklikšķiniet **Open**.
5.  Dialoglodziņā Importēt atlasiet importējamās pārskatu definīcijas.
    -   Lai importētu visas atskaites definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.
    -   Lai importētu atsevišķus pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas, atlasiet importējamos pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas.

6.  Click **Import**.



