---
title: Paplašināmība pakalpojumā Attract
description: Šajā tēmā ir aprakstīts, kā varat paplašināt Microsoft Dynamics 365 Talent - Attract, izmantojot Microsoft Power Platform.
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ddc6593431585ed79cc15f7ede5daf856f11b959
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527246"
---
# <a name="extensibility-in-attract"></a>Paplašināmība pakalpojumā Attract

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Programma Microsoft Dynamics 365 Talent ir būvēta, izmantojot Common Data Service, un to var dažādos veidos paplašināt, izmantojot Microsoft Power Platform un iespējas, ko sniedz Common Data Service. Tāpēc varat konfigurēt un personalizēt sistēmu, izmantojot Microsoft Power Apps un Microsoft Power Automate. Varat arī iegūt papildu analīzes datus par personām, izmantojot Microsoft Power BI. Turklāt jaunās pielāgotās aktivitātes, piemēram, Power Apps un Tīmekļa satura (iframe) aktivitātes, ļauj jums adaptēt darbā pieņemšanas procesu labāk kā jebkad. Izmantojot šīs aktivitātes, varat pielāgot darbā pieņemšanas procesu atbilstoši sava uzņēmuma vajadzībām un procedūrām, un varat nodrošināt, lai gan darbā pieņemšanas grupai, gan kandidātiem būtu vienota un pielāgota funkcionalitāte.

## <a name="extending-option-sets-in-attract"></a>Opciju kopu paplašināšana programmā Attract

**Opciju kopa** (salasīšanas saraksts) ir lauka veids, kuru var iekļaut elementā. Tas nosaka opciju kopu. Opciju kopas parādīšanai veidlapā izmanto nolaižamā saraksta vadīklu.  Programmā Attract ir vairāki lauki, kas ir opciju kopas.  Mēs sākam ieviest iespēju opciju kopas paplašināšanai, ietverot lauku Noraidīšanas pamatojums, lauku Nodarbinātības veids un lauku Darba stāža veids.   Pievienot var arī to opciju lokalizētās parādīšanas etiķetes opcijas, kuras tiek pievienotas. Papildinformāciju skatiet tēmā [Opciju kopas etiķetes pielāgošana](https://docs.microsoft.com/powerapps/developer/common-data-service/customize-labels-support-multiple-languages).

> [!NOTE]
> Lai izmantotu darba publicēšanas pakalpojumā LinkedIn funkcionalitāti, ir jāizmanto lauks **Nodarbinātības veids** un **Darba stāžs veids** lapā **Darba informācija**. Šo lauku noklusējuma vērtības nodrošina pakalpojums LinkedIn, un tās tiek rādītas, kad darbs tiek publicēts. Tāpēc, ja darbs tiek publicēts pakalpojumā LinkedIn un mainīts šo lauku esošās opciju kopas vērtības, darbs joprojām tiek publicēts, taču pakalpojumā LinkedIn netiek parādītas pielāgotās lauka **Nodarbinātības veids** un **Darba stāža veids** vērtības.  

Tālāk ir norādītas darbības, kas jāveic, lai atjauninātu lauku **Noraidīšanas iemesls** ar vērtībām, kas ir raksturīgi jūsu biznesam.  

1. Lai paplašinātu opciju kopu **Noraidīšanas iemesls**, dodieties uz [Power Apps administratora tīmekļa vietni](https://admin.powerapps.com).
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

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Izmantojiet Microsoft Power Platform sniegtās priekšrocības 

Tā kā visi programmas Attract dati tiek glabāti Common Data Service, varat izmantot Microsoft Power Platform rīkus, lai programmā Attract ieviestu savas unikālās uzņēmējdarbības vajadzības.

### <a name="power-apps"></a>Power Apps

Varat izmantot platformu Power Apps, lai vienkārši izveidotu programmas, kurās tiek veidots savienojums ar jūsu Attract datiem un loģikas pievienošanai tiek izmantotas tādas pašas izteiksmes, kādas tiek izmantotas programmā Microsoft Excel. Programmas, ko izveidojat, izmantojot platformu Power Apps , var tikt darbinātas tīmeklī, kā arī Apple iOS un Google Android ierīcēs.

Piemēram, universitāšu karjeras iespēju izstādes varat padarīt vienkāršākas personāla atlases darbiniekiem, uzbūvējot maz resursu patērējošu programmu, kas šiem darbiniekiem ļauj skenēt CV un padot kandidātus uz kādu amatu programmā Attract. Ja vēlaties, varat izveidot programmu, kas palīdz nodrošināt jūsu organizācijas atbilstības vajadzības. Papildinformāciju par platformu Power Apps un to, kā to var izmantot programmu izveidei, skatiet tēmā [Datu integrēšana platformā Common Data Service](https://docs.microsoft.com/powerapps).

### <a name="microsoft-power-automate"></a>Microsoft Power Automate 

Varat izmantot Microsoft Power Automate, lai izveidotu automatizētas darbplūsmas, kas tiek izpildītas, izmantojot Attract datus. Varat ērti izveidot savienojumu ar simtiem populāru programmu un pakalpojumu, nerakstot nekādu kodu. Izveidojot plūsmas, kas mijiedarbojas ar Attract elementiem Darbs, Kandidāts un Pieteikums platformā Common Data Service, varat automatizēt dažādas darbības. Piemēram, kad kandidāts pieņem kādu piedāvājumu, var tikt nosūtīts paziņojums personāla atlases darba grupai vai šīs ziņas var tikt paziņotas vietnē Twitter. Papildinformāciju par plūsmām skatiet rakstā [Microsoft Power Automate dokumentācija](https://docs.microsoft.com/flow/).

### <a name="power-bi"></a>Power BI

Power BI sniedz iespēju izveidot un skatīt pielāgotus pārskatus un informācijas paneļus, kas sniedz dziļāku ieskatu par jūsu Attract datiem. Papildinformāciju par pakalpojumu Power BI un to, kā izveidot interaktīvus pārskatus un informācijas paneļus, skatiet rakstā [Power BI dokumentācija](https://docs.microsoft.com/power-bi/).

### <a name="custom-activities"></a>Pielāgotas darbības 

Varat pievienot pielāgotas aktivitātes, piemēram, Power Apps programmas un tīmekļa satura (iframe) aktivitātes, darba procesa veidnes līmenī vai laikā, kamēr veidojat jaunu darbu. Šīs aktivitātes ļauj jums pielāgot darbā pieņemšanas procesu un savas organizācijas unikālo biznesa loģiku ieviest programmā Attract.

#### <a name="power-apps-activity"></a>Aktivitāte Power Apps 

Power Apps aktivitāte dod iespēju darba vai darba procesa veidnes veidotājam iegult Power Apps programmu darbā pieņemšanas plūsmā. Pēc programmas izveidošanas un publicēšanas šīs programmas ID varat ievadīt aktivitāšu konfigurācijās. By using a Power Apps programmu, varat lasīt datus no platformas Common Data Service un rakstīt datus tajā. Programmu varat pat saistīt ar kādu plūsmu. Piemēram, jums ir programma, ko darbā pieņemšanas darbinieki izmanto, lai aizpildītu formas, veicot intervijas pa tālruni. Tādā gadījumā šo programmu varat saistīt ar plūsmu, kas novērtē, vai attiecīgais kandidāts var tikt pārcelts uz nākamo darbā pieņemšanas procesa atlases kārtu. Šāda tipa aktivitāti var skatīt tikai darbā pieņemšanas grupas dalībnieki. Plašāku informāciju par veidu, kā konfigurēt Power Apps aktivitāti, skatiet tēmā [Aktivitātes darbā pieņemšanas procesos](./activities-attract.md).

> [!NOTE]
> Aktivitāte Power Apps ir pieejama tikai tad, ja ir pieejams visaptverošais darbā pieņemšanas papildinājums.

#### <a name="web-content-iframe-activity"></a>Tīmekļa satura (iframe) aktivitāte

Tīmekļa satura (iframe) aktivitāte dod iespēju iegult pielāgotu tīmekļa risinājumu, ko izveidojāt darbā pieņemšanas procesā vai kandidātu portālā. Varat tiešā veidā lasīt datus no platformas Common Data Service un ierakstīt datus tajā. Varat arī pielāgot risinājumu tā, lai tas aktivizētu plūsmas vai izmantotu Microsoft Azure funkcijas. Plašāku informāciju par veidu, ka konfigurēt tīmekļa satura aktivitāti, skatiet šeit: [Aktivitātes darbā pieņemšanas procesos](./activities-attract.md).

> [!NOTE]
> Aktivitāte Tīmekļa aktivitāte ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums


[!INCLUDE[footer-include](../includes/footer-banner.md)]