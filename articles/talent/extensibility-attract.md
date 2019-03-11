---
title: Paplašināmība programmā Attract
description: Šajā tēmā ir aprakstīts, kā varat paplašināt lietojumprogrammu Dynamics 365 for Talent - Attract, izmantojot platformu Microsoft Power.
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: d9e1dd3a67c5f64b5d05f0f171226085138e0b44
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305293"
---
# <a name="extensibility-in-attract"></a>Paplašināmība programmā Attract

[!include[banner](../includes/banner.md)]

Programma Dynamics 365 for Talent ir būvēta, izmantojot platformu Common Data Service (CDS) programmām, un to var dažādos veidos paplašināt, izmantojot platformu Microsoft Power un iespējas, ko sniedz Common Data Service programmām. Tāpēc varat konfigurēt un personalizēt sistēmu, izmantojot Microsoft PowerApps un Microsoft Flow. Varat arī iegūt papildu analīzes datus par personām, izmantojot Microsoft Power BI. Turklāt jaunās pielāgotās aktivitātes, piemēram, PowerApps un Tīmekļa satura (iframe) aktivitātes, ļauj jums adaptēt darbā pieņemšanas procesu labāk kā jebkad. Izmantojot šīs aktivitātes, varat pielāgot darbā pieņemšanas procesu atbilstoši sava uzņēmuma vajadzībām un procedūrām, un varat nodrošināt, lai gan darbā pieņemšanas grupai, gan kandidātiem būtu vienota un pielāgota funkcionalitāte.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Microsoft Power Platform pilnvērtīga izmantošana 

Tā kā visi programmas Attract dati tiek glabāti platformā Common Data Service programmām, varat izmantot platformas Microsoft Power rīkus, lai programmā Attract ieviestu savas unikālās uzņēmējdarbības vajadzības.

### <a name="powerapps"></a>PowerApps

Varat izmantot platformu PowerApps, lai vienkārši izveidotu programmas, kurās tiek veidots savienojums ar jūsu Attract datiem un loģikas pievienošanai tiek izmantotas tādas pašas izteiksmes, kādas tiek izmantotas programmā Microsoft Excel. Programmas, ko izveidojat, izmantojot platformu PowerApps, var tikt darbinātas tīmeklī, kā arī Apple iOS un Google Android ierīcēs.

Piemēram, universitāšu karjeras iespēju izstādes varat padarīt vienkāršākas personāla atlases darbiniekiem, uzbūvējot maz resursu patērējošu programmu, kas šiem darbiniekiem ļauj skenēt CV un padot kandidātus uz kādu amatu programmā Attract. Ja vēlaties, varat izveidot programmu, kas palīdz nodrošināt jūsu organizācijas atbilstības vajadzības. Papildinformāciju par platformu PowerApps un to, kā to var izmantot programmu izveidei, skatiet rakstā [Datu integrēšana platformā Common Data Service programmām](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Varat izmantot Microsoft Flow, lai izveidotu automatizētas darbplūsmas, kas tiek izpildītas, izmantojot Attract datus. Varat ērti izveidot savienojumu ar simtiem populāru programmu un pakalpojumu, nerakstot nekādu kodu. Izveidojot plūsmas, kas mijiedarbojas ar Attract elementiem Darbs, Kandidāts un Pieteikums platformā Common Data Service programmām, varat automatizēt dažādas darbības. Piemēram, kad kandidāts pieņem kādu piedāvājumu, var tikt nosūtīts paziņojums personāla atlases darba grupai vai šīs ziņas var tikt paziņotas vietnē Twitter. Papildinformāciju par plūsmām skatiet rakstā [Microsoft Flow dokumentācija](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Power BI sniedz iespēju izveidot un skatīt pielāgotus pārskatus un informācijas paneļus, kas sniedz dziļāku ieskatu par jūsu Attract datiem. Papildinformāciju par pakalpojumu Power BI un to, kā izveidot interaktīvus pārskatus un informācijas paneļus, skatiet rakstā[Power BI dokumentācija](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Pielāgotas darbības 

Varat pievienot pielāgotas aktivitātes, piemēram, PowerApps programmu un tīmekļa satura (iframe) aktivitātes, darba procesa veidnes līmenī vai laikā, kamēr veidojat jaunu darbu. Šīs aktivitātes ļauj jums pielāgot darbā pieņemšanas procesu un savas organizācijas unikālo biznesa loģiku ieviest programmā Attract.

#### <a name="powerapps-activity"></a>PowerApps aktivitāte 

PowerApps aktivitāte dod iespēju darba vai darba procesa veidnes veidotājam iegult PowerApps programmu darbā pieņemšanas plūsmā. Pēc programmas izveidošanas un publicēšanas šīs programmas ID varat ievadīt aktivitāšu konfigurācijās. Izmantojot PowerApps programmu, varat lasīt datus no platformas Common Data Service programmām un rakstīt datus tajā. Programmu varat pat saistīt ar kādu plūsmu. Piemēram, jums ir programma, ko darbā pieņemšanas darbinieki izmanto, lai aizpildītu formas, veicot intervijas pa tālruni. Tādā gadījumā šo programmu varat saistīt ar plūsmu, kas novērtē, vai attiecīgais kandidāts var tikt pārcelts uz nākamo darbā pieņemšanas procesa atlases kārtu. Šāda tipa aktivitāti var skatīt tikai darbā pieņemšanas grupas dalībnieki. Plašāku informāciju par veidu, kā konfigurēt PowerApps aktivitāti, skatiet šeit: [Aktivitātes programmā Attract](./activities-attract.md).

> [!NOTE]
> Aktivitāte PowerApps ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.

#### <a name="web-content-iframe-activity"></a>Tīmekļa satura (iframe) aktivitāte

Tīmekļa satura (iframe) aktivitāte dod iespēju iegult pielāgotu tīmekļa risinājumu, ko izveidojāt darbā pieņemšanas procesā vai kandidātu portālā. Varat tiešā veidā lasīt datus no platformas Common Data Service programmām un ierakstīt datus tajā. Varat arī pielāgot risinājumu tā, lai tas aktivizētu plūsmas vai izmantotu Microsoft Azure funkcijas. Plašāku informāciju par veidu, ka konfigurēt tīmekļa satura aktivitāti, skatiet šeit: [Aktivitātes programmā Attract](./activities-attract.md).

> [!NOTE]
> Aktivitāte Tīmekļa aktivitāte ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums
