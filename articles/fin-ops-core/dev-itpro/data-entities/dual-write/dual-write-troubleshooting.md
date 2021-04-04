---
title: Vispārējā problēmu novēršana
description: Šajā rakstā ir sniegta informācija par vispārējo problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 4b97fffce6d1c3ea143e0d8445769e794d0c46a4
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566104"
---
# <a name="general-troubleshooting"></a>Vispārējā problēmu novēršana

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Šajā rakstā ir sniegta informācija par vispārējo problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Mēģinot instalēt duālā ieraksta pakotni, izmantojot pakotnes izvietošanas rīku, netiek rādīti pieejami risinājumi

Dažas pakotnes izvietošanas rīka versijas nav saderīgas ar duālā ieraksta risinājuma pakotni. Lai veiksmīgi instalētu pakotni, pārliecinieties, vai izmantojat pakotnes izvietošanas rīka [versiju 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) vai jaunāku.

Pēc pakotnes izvietošanas rīka instalēšanas, instalējiet risinājumu pakotni, izpildot šīs darbības.

1. Lejupielādējiet jaunāko risinājumu pakotnes failu no Yammer.com. Kad pakotnes ZIP fails ir lejupielādēts, ar peles labo pogu noklikšķiniet uz tā un atlasiet **Rekvizīti**. Atzīmējiet izvēles rūtiņu **Atbloķēt** un pēc tam atlasiet **Piemērot**. Ja nav redzama izvēles rūtiņa **Atbloķēt**, ZIP fails jau ir atbloķēts, un šo darbību var izlaist.

    ![Rekvizītu dialoglodziņš](media/unblock_option.png)

2. Izvelciet pakotnes ZIP failu un iekopējiet visus failus mapē **Dynamics365FinanceAndOperationsCommon. ackageDeployer. 2.0.438**.

    ![Mapes Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 saturs](media/extract_package.png)

3. Ielīmējiet visus kopētos failus pakotnes izvietošanas rīka mapē **Rīki**. 
4. Palaidiet **PackageDeployer.exe**, lai atlasītu Dataverse vidi un instalētu risinājumus.

    ![Rīku mapes saturs](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Spraudņa trasēšanas žurnāla iespējošana un skatīšana Dataverse, lai skatītu kļūdas informāciju

**Nepieciešamā loma, lai ieslēgtu trasēšanas žurnālu un skatītu kļūdas:** sistēmas administrators

Lai aktivizētu trasēšanas žurnālu, veiciet tālāk minētās darbības.

1. Piesakieties ar modeli vadītā programmā Dynamics 365, atveriet lapu **Iestatījumi** un pēc tam sadaļā **Sistēma** atlasiet **Administrēšana**.
2. Lapā **Administrēšana** atlasiet opciju **Sistēmas iestatījumi**.
3. Cilnes **Pielāgošana** laukā **Spraudņa un pielāgotās darbplūsmas aktivitātes izsekošana** atlasiet **Visi**, lai iespējotu spraudņa izsekošanas žurnālu. Ja vēlaties izsekot trasēšanas žurnāliem tikai tad, ja rodas izņēmumi, varat tā vietā izvēlēties opciju **Izņēmums**.


Lai skatītu trasēšanas žurnālu, veiciet tālāk minētās darbības.

1. Piesakieties ar modeli vadītā programmā Dynamics 365, atveriet lapu **Iestatījumi** un pēc tam sadaļā **Pielāgošana** atlasiet **Spraudņa izsekošanas žurnāls**.
2. Atrodiet trasēšanas žurnālus, kur lauks **Veida nosaukums** ir iestatīts uz **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Veiciet dubultklikšķi uz elementa, lai apskatītu pilno žurnālu, un pēc tam kopsavilkuma cilnē **Izpilde** pārskatiet **Ziņojuma bloka** tekstu.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Atkļūdošanas režīma iespējošana, lai novērstu tiešsaistes sinhronizācijas problēmas Finance and Operations programmās

**Nepieciešamās lomas, lai apskatītu kļūdas:** sistēmas administratora duālās rakstīšanas kļūdas, kas radušās programmā Dataverse, var parādīties Finance and Operations programmā. Dažos gadījumos pilns kļūdas ziņojuma teksts nav pieejams, jo ziņojums ir pārāk garš vai satur personu identificējošu informāciju (PII). Varat ieslēgt izvērsto kļūdu reģistrēšanu, izpildot tālāk aprakstītās darbības.

1. Visām projekta konfigurācijām Finance and Operations programmās ir **IsDebugMode** rekvizīts tabulā **DualWriteProjectConfiguration**. Atveriet elementu **DualWriteProjectConfiguration**, izmantojot Excel pievienojumprogrammu.

    > [!TIP]
    > Vienkāršs veids, kā atvērt tabulu, ir ieslēgt režīmu **Noformēšana** Excel pievienojumprogrammā un pēc tam darblapai pievienot **DualWriteProjectConfigurationEntity**. Papildinformāciju skatiet rakstā [Elementa datu atvēršana programmā Excel un to atjaunināšana, izmantojot Excel pievienojumprogrammu](../../office-integration/use-excel-add-in.md).

2. Iestatiet rekvizītu **IsDebugMode** projektam uz **Jā**.
3. Palaidiet scenāriju, kas ģenerē kļūdas.
4. Izvērstie žurnāli ir pieejami DualWriteErrorLog tabulā. Lai meklētu datus tabulas pārlūkā, izmantojiet tālāk minēto vietrādi URL (ja nepieciešams, nomainiet **XXX**):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Sinhronizācijas kļūdu pārbaude Finance and Operations programmas virtuālajā mašīnā

**Kļūdu skatīšanai nepieciešamā loma:** Sistēmas administrators

1. Pierakstieties portālā Microsoft Dynamics Lifecycle Services (LCS).
2. Atveriet LCS projektu, kuram izvēlējāties veikt duālā ieraksta pārbaudi.
3. Atlasiet elementu **Mākoņvides**.
4. Izmantojiet attālo darbvirsmu, lai pieteiktos Finance and Operations programmas virtuālajā mašīnā (VM). Izmantojiet lokālo kontu, kas tiek parādīts LCS.
5. Atveriet Notikumu skatītāju,
6. Atlasiet **Lietojumprogrammu un pakalpojumu žurnāli \> Microsoft \> Dynamics \> AX-DualWriteSync \> Darbību**.
7. Pārskatiet neseno kļūdu sarakstu.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Atsaistīt un saistīt citu Dataverse vidi no Finance and Operations programmas

**Nepieciešamā loma, lai atsaistītu vidi:** sistēmas administrators vai nu Finance and Operations programmai, vai Dataverse.

1. Piesakieties Finance and Operations programmā.
2. Dodieties uz **Darbvietas \>Datu pārvaldība** un atlasiet elementu **Duālais ieraksts**.
3. Atlasiet visus darbojošos kartējumus, pēc tam atlasiet **Apturēt**.
4. Atlasiet **Atsaistīt vidi**.
5. Atlasiet **Jā**, lai apstiprinātu darbību.

Tagad varat saistīt jaunu vidi.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Nevar skatīt pārdošanas pasūtījuma rindas informācijas veidlapu 

Veidojot pārdošanas pasūtījumu Dynamics 365 Sales, noklikšķinot uz **+ pievienot preces**, varat tikt novirzīts uz Dynamics 365 Project Operations pasūtījuma rindas veidlapu. No šīs veidlapas nav iespējams skatīt pārdošanas pasūtījuma rindas **Informācijas** veidlapu. **Informācijas** opcija neparādās nolaižamajā sarakstā zem **Jaunas pasūtījuma rindas**. Tas notiek tāpēc, ka projekta operācijas ir uzstādītas jūsu vidē.

Lai atkārtoti iespējotu **Informācijas** veidlapas opciju, rīkojieties šādi:
1. Pārejiet uz **Pasūtījuma rindas** tabulu.
2. Atrodiet **Informācijas** veidlapu zem veidlapas zara. 
3. Atlasiet **Informācijas** veidlapu un noklikšķiniet uz **Iespējot drošības lomas**. 
4. Mainiet drošības iestatījumu uz **Parādīt visiem**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]