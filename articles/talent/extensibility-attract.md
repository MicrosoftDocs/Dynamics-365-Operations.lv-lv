---
title: Paplašināmība programmā Attract
description: Šajā tēmā ir aprakstīts, kā varat paplašināt lietojumprogrammu Dynamics 365 for Talent - Attract, izmantojot platformu Microsoft Power.
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichsew
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 52790fbe500d9f55bc9cc86fba5d54f30b11e559
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/12/2019
ms.locfileid: "949970"
---
# <a name="extensibility-in-attract"></a>Paplašināmība pakalpojumā Attract

[!include[banner](../includes/banner.md)]

Programma Microsoft Dynamics 365 for Talent ir būvēta, izmantojot platformu Common Data Service, un to var dažādos veidos paplašināt, izmantojot Microsoft Power Platform un iespējas, ko sniedz Common Data Service. Tāpēc varat konfigurēt un personalizēt sistēmu, izmantojot Microsoft PowerApps un Microsoft Flow. Varat arī iegūt papildu analīzes datus par personām, izmantojot Microsoft Power BI. Turklāt jaunās pielāgotās aktivitātes, piemēram, PowerApps un Tīmekļa satura (iframe) aktivitātes, ļauj jums adaptēt darbā pieņemšanas procesu labāk kā jebkad. Izmantojot šīs aktivitātes, varat pielāgot darbā pieņemšanas procesu atbilstoši sava uzņēmuma vajadzībām un procedūrām, un varat nodrošināt, lai gan darbā pieņemšanas grupai, gan kandidātiem būtu vienota un pielāgota funkcionalitāte.

## <a name="extending-option-sets-in-attract"></a>Opciju kopu paplašināšana programmā Attract

**Opciju kopa** (salasīšanas saraksts) ir lauka veids, kuru var iekļaut elementā. Tas nosaka opciju kopu. Opciju kopas parādīšanai veidlapā izmanto nolaižamā saraksta vadīklu.  Programmā Attract ir vairāki lauki, kas ir opciju kopas.  Mēs sākam ieviest iespēju opciju kopas paplašināšanai, ietverot lauku Noraidīšanas pamatojums, lauku Nodarbinātības veids un lauku Darba stāža veids.   Pievienot var arī to opciju lokalizētās parādīšanas etiķetes opcijas, kuras tiek pievienotas. Papildinformāciju skatiet tēmā [Opciju kopas etiķetes pielāgošana](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/customize-labels-support-multiple-languages).

> [!NOTE]
> Lai izmantotu darba publicēšanas pakalpojumā LinkedIn funkcionalitāti, ir jāizmanto lauks **Nodarbinātības veids** un **Darba stāžs veids** lapā **Darba informācija**. Šo lauku noklusējuma vērtības nodrošina pakalpojums LinkedIn, un tās tiek rādītas, kad darbs tiek publicēts. Tāpēc, ja darbs tiek publicēts pakalpojumā LinkedIn un mainīts šo lauku esošās opciju kopas vērtības, darbs joprojām tiek publicēts, taču pakalpojumā LinkedIn netiek parādītas pielāgotās lauka **Nodarbinātības veids** un **Darba stāža veids** vērtības.  

Tālāk ir norādītas darbības, kas jāveic, lai atjauninātu lauku **Noraidīšanas iemesls** ar vērtībām, kas ir raksturīgi jūsu biznesam.  

1. Lai paplašinātu opciju kopu **Noraidīšanas iemesls**, dodieties uz [PowerApps administratora tīmekļa vietni](https://admin.powerapps.com).
2. Iespējams, tiek parādīta uzvedne ar norādi pierakstīties savā kontā. Ierakstiet savu lietotāja ID un paroles akreditācijas datus, kurus izmantojat, lai pieteiktos programmā Dynamics365 un/vai Office365 un pēc tam noklikšķiniet uz **Tālāk**.
3. Cilnē **Vides** atlasiet vidi, kuru vēlaties pārvaldīt, un veiciet dubultklikšķi, lai parādītu cilni **Detalizēta informācija**.
4. Cilnē **Detalizēta informācija** atlasiet **Dynamics 365 administrācijas centrs**.
5. Atlasiet instanci, kuru vēlaties pārveidot un atlasiet **Atvērt**.
6. Pārejiet uz sadaļu **Iestatījumi**, pēc tam uz sadaļu **Pielāgojumi** un izvēlieties **Pielāgot sistēmu**.
7. Atrodiet elementu, kura opciju kopu vēlaties paplašināt, atlasot opciju **Elementi** un paplašinot grupu. Šajā piemērā tas būs **Darba pieteikuma elements**.
8. Dodieties uz lauku, kura opciju kopu vēlaties paplašināt, atlasot opciju **Lauki**. Šajā piemērā tas būs **msdyn_rejectionreason**. Veiciet dubultklikšķi uz attiecīgā lauka.
9. Laukā **Opciju kopa** izvēlieties **Rediģēt**.
10. Atlasiet ikonu **+**.
11. Ievadiet vērtību laukā **Etiķete**.  (Tai ir jābūt unikālai vērtībai, tā nedrīkst atkārtoties.)
12. Atlasiet **Saglabāt**.
13. Atlasiet **Publicēt** lapas augšdaļā.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Microsoft Power Platform pilnvērtīga izmantošana 

Tā kā visi programmas Attract dati tiek glabāti platformā Common Data Service, varat izmantot Microsoft Power Platform rīkus, lai programmā Attract ieviestu savas unikālās uzņēmējdarbības vajadzības.

### <a name="powerapps"></a>PowerApps

Varat izmantot platformu PowerApps, lai vienkārši izveidotu programmas, kurās tiek veidots savienojums ar jūsu Attract datiem un loģikas pievienošanai tiek izmantotas tādas pašas izteiksmes, kādas tiek izmantotas programmā Microsoft Excel. Programmas, ko izveidojat, izmantojot platformu PowerApps, var tikt darbinātas tīmeklī, kā arī Apple iOS un Google Android ierīcēs.

Piemēram, universitāšu karjeras iespēju izstādes varat padarīt vienkāršākas personāla atlases darbiniekiem, uzbūvējot maz resursu patērējošu programmu, kas šiem darbiniekiem ļauj skenēt CV un padot kandidātus uz kādu amatu programmā Attract. Ja vēlaties, varat izveidot programmu, kas palīdz nodrošināt jūsu organizācijas atbilstības vajadzības. Papildinformāciju par platformu PowerApps un to, kā to var izmantot programmu izveidei, skatiet tēmā [Datu integrēšana platformā Common Data Service](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Varat izmantot Microsoft Flow, lai izveidotu automatizētas darbplūsmas, kas tiek izpildītas, izmantojot Attract datus. Varat ērti izveidot savienojumu ar simtiem populāru programmu un pakalpojumu, nerakstot nekādu kodu. Izveidojot plūsmas, kas mijiedarbojas ar Attract elementiem Darbs, Kandidāts un Pieteikums platformā Common Data Service, varat automatizēt dažādas darbības. Piemēram, kad kandidāts pieņem kādu piedāvājumu, var tikt nosūtīts paziņojums personāla atlases darba grupai vai šīs ziņas var tikt paziņotas vietnē Twitter. Papildinformāciju par plūsmām skatiet rakstā [Microsoft Flow dokumentācija](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Power BI sniedz iespēju izveidot un skatīt pielāgotus pārskatus un informācijas paneļus, kas sniedz dziļāku ieskatu par jūsu Attract datiem. Papildinformāciju par pakalpojumu Power BI un to, kā izveidot interaktīvus pārskatus un informācijas paneļus, skatiet rakstā[Power BI dokumentācija](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Pielāgotas darbības 

Varat pievienot pielāgotas aktivitātes, piemēram, PowerApps programmu un tīmekļa satura (iframe) aktivitātes, darba procesa veidnes līmenī vai laikā, kamēr veidojat jaunu darbu. Šīs aktivitātes ļauj jums pielāgot darbā pieņemšanas procesu un savas organizācijas unikālo biznesa loģiku ieviest programmā Attract.

#### <a name="powerapps-activity"></a>PowerApps aktivitāte 

PowerApps aktivitāte dod iespēju darba vai darba procesa veidnes veidotājam iegult PowerApps programmu darbā pieņemšanas plūsmā. Pēc programmas izveidošanas un publicēšanas šīs programmas ID varat ievadīt aktivitāšu konfigurācijās. Izmantojot PowerApps programmu, varat lasīt datus no platformas Common Data Service un rakstīt datus tajā. Programmu varat pat saistīt ar kādu plūsmu. Piemēram, jums ir programma, ko darbā pieņemšanas darbinieki izmanto, lai aizpildītu formas, veicot intervijas pa tālruni. Tādā gadījumā šo programmu varat saistīt ar plūsmu, kas novērtē, vai attiecīgais kandidāts var tikt pārcelts uz nākamo darbā pieņemšanas procesa atlases kārtu. Šāda tipa aktivitāti var skatīt tikai darbā pieņemšanas grupas dalībnieki. Plašāku informāciju par veidu, kā konfigurēt PowerApps aktivitāti, skatiet šeit: [Aktivitātes programmā Attract](./activities-attract.md).

> [!NOTE]
> Aktivitāte PowerApps ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.

#### <a name="web-content-iframe-activity"></a>Tīmekļa satura (iframe) aktivitāte

Tīmekļa satura (iframe) aktivitāte dod iespēju iegult pielāgotu tīmekļa risinājumu, ko izveidojāt darbā pieņemšanas procesā vai kandidātu portālā. Varat tiešā veidā lasīt datus no platformas Common Data Service un ierakstīt datus tajā. Varat arī pielāgot risinājumu tā, lai tas aktivizētu plūsmas vai izmantotu Microsoft Azure funkcijas. Plašāku informāciju par veidu, ka konfigurēt tīmekļa satura aktivitāti, skatiet šeit: [Aktivitātes programmā Attract](./activities-attract.md).

> [!NOTE]
> Aktivitāte Tīmekļa aktivitāte ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums
