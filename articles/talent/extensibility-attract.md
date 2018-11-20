---
title: "Paplašināmība programmā Attract"
description: "Šajā tēmā ir aprakstīts, kā varat paplašināt programmu Microsoft Dynamics 365 for Talent - Attract, izmantojot platformu Microsoft Power Platform."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 0af60a0aea0f7a5de793631445aaebb37dbb0d74
ms.contentlocale: lv-lv
ms.lasthandoff: 10/22/2018

---

# <a name="extensibility-in-attract"></a>Paplašināmība programmā Attract

[!include[banner](../includes/banner.md)]

Programma Microsoft Dynamics 365 for Talent ir būvēta uz platformas Common Data Service (CDS) for Apps, un to var dažādi paplašināt, izmantojot platformu Microsoft Power Platform un iespējas, ko sniedz Common Data Service programmām. Tādēļ sistēmu varat konfigurēt un personalizēt, izmantojot Microsoft PowerApps un Microsoft Flow. Pie tam varat iegūt personu papildu analīzes iespējas, izmantojot Microsoft Power BI. Turklāt jaunās pielāgotās aktivitātes, piemēram, PowerApps un Tīmekļa satura (iframe) aktivitātes, ļauj jums adaptēt darbā pieņemšanas procesu labāk kā jebkad. Izmantojot šīs aktivitātes, varat pielāgot darbā pieņemšanas procesu atbilstoši sava uzņēmuma vajadzībām un procedūrām, un varat nodrošināt, lai gan darbā pieņemšanas grupai, gan kandidātiem būtu vienota un pielāgota funkcionalitāte.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Microsoft Power Platform pilnvērtīga izmantošana 

Tā kā visi dati no Attract tiek glabāti pakalpojumā Common Data Service programmām, varat izmantot rīkus no Microsoft Power Platform, lai programmā Attract ieviestu savas unikālās uzņēmējdarbības vajadzības.

### <a name="powerapps"></a>PowerApps

Varat izmantot platformu PowerApps, lai vienkārši uzbūvētu programmas, kurām ir savienojums ar jūsu Attract datiem un kuras loģikas pievienošanai izmanto tādas pašas izteiksmes, kādas tiek izmantotas programmā Microsoft Excel. Programmas, ko izveidojat, izmantojot platformu PowerApps, var darboties tīmeklī, Apple iOS ierīcēs un Google Android ierīcēs.

Piemēram, universitāšu karjeras iespēju izstādes varat padarīt vienkāršākas personāla atlases darbiniekiem, uzbūvējot maz resursu patērējošu programmu, kas šiem darbiniekiem ļauj skenēt CV un padot kandidātus uz kādu amatu programmā Attract. Ja vēlaties, varat izveidot programmu, kas palīdz nodrošināt jūsu organizācijas atbilstības vajadzības. Plašāku informāciju par platformu PowerApps un veidu, kā to izmantot programmu veidošanai, skatiet šeit: [Datu integrēšana Common Data Service programmām](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Pakalpojumu Microsoft Flow varat izmantot, lai izveidotu automatizētas darbplūsmas, ko darbināt ar Attract datiem. Varat ērti izveidot savienojumu ar simtiem populāru programmu un pakalpojumu, nerakstot nekādu kodu. Būvējot plūsmas, kas mijiedarbojas ar Attract entītijām Darbs, Kandidāts un Pieteikums pakalpojumā Common Data Service programmām, varat automatizēt dažādas darbības. Piemēram, kad kandidāts pieņem kādu piedāvājumu, var tikt nosūtīts paziņojums personāla atlases darba grupai vai šīs ziņas var tikt paziņotas vietnē Twitter. Plašāku informāciju par plūsmām skatiet šeit: [Microsoft Flow dokumentācija](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Power BI ļauj jums būvēt un skatīt pielāgotus pārskatus un informācijas paneļus, kas sniedz dziļāku ieskatu jūsu Attract datos. Plašāku informāciju par Power BI un veidu, kā būvēt interaktīvus pārskatus un informācijas paneļus, skatiet šeit: [Power BI dokumentācija](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Pielāgotas darbības 

Varat pievienot pielāgotas aktivitātes, piemēram, PowerApps programmu un tīmekļa satura (iframe) aktivitātes, darba procesa veidnes līmenī vai laikā, kamēr veidojat jaunu darbu. Šīs aktivitātes ļauj jums pielāgot darbā pieņemšanas procesu un savas organizācijas unikālo biznesa loģiku ieviest programmā Attract.

#### <a name="powerapps-activity"></a>PowerApps aktivitāte 

PowerApps aktivitāte dod iespēju darba vai darba procesa veidnes veidotājam iegult PowerApps programmu darbā pieņemšanas plūsmā. Pēc programmas izveidošanas un publicēšanas šīs programmas ID varat ievadīt aktivitāšu konfigurācijās. Izmantojot PowerApps programmu, varat lasīt un rakstīt datus pakalpojumā Common Data Service programmām. Programmu varat pat saistīt ar kādu plūsmu. Piemēram, jums ir programma, ko darbā pieņemšanas darbinieki izmanto, lai aizpildītu formas, veicot intervijas pa tālruni. Tādā gadījumā šo programmu varat saistīt ar plūsmu, kas novērtē, vai attiecīgais kandidāts var tikt pārcelts uz nākamo darbā pieņemšanas procesa atlases kārtu. Šāda tipa aktivitāti var skatīt tikai darbā pieņemšanas grupas dalībnieki. Plašāku informāciju par veidu, kā konfigurēt PowerApps aktivitāti, skatiet šeit: [Aktivitātes programmā Attract](./activities-attract.md).

> [!NOTE]
> Aktivitāte PowerApps ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.

#### <a name="web-content-iframe-activity"></a>Tīmekļa satura (iframe) aktivitāte

Tīmekļa satura (iframe) aktivitāte dod iespēju iegult pielāgotu tīmekļa risinājumu, ko izveidojāt darbā pieņemšanas procesā vai kandidātu portālā. Datus varat lasīt un rakstīt tieši no pakalpojuma Common Data Service for programmām. Varat arī pielāgot risinājumu, lai tas aktivizētu plūsmas ir izmantotu Microsoft Azure funkcijas. Plašāku informāciju par veidu, ka konfigurēt tīmekļa satura aktivitāti, skatiet šeit: [Aktivitātes programmā Attract](./activities-attract.md).

> [!NOTE]
> Aktivitāte Tīmekļa aktivitāte ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums

