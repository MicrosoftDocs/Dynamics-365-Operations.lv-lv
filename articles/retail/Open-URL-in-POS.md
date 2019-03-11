---
title: URL atvērš. POS
description: Šajā tēmā ir sniegts apskats par preču un debitoru meklēšanas funkcionalitātes uzlabojumiem programmā Microsoft Dynamics 365 for Retail.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b07406b4e218b45bdde87c4a579814fe0edbc286
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "327094"
---
# <a name="open-url-in-pos"></a>URL atvēršana POS

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā konfig. pogu sistēmā Retail POS (pārdošanas punkts), lai atvērtu URL. Šim līdzeklim nav nepieciešama koda pielāgošana, un to var konfigurēt persona, kurai nav izstrādātāja lomas. Šis līdzeklis ir ietverts programmas Dynamics 365 for Finance and Operations versijas 8.1.3 laidienā (būvējums 8.1.227.10014) un jaunākās tās versijās. 

Šis līdzeklis ļauj konfigurēt pogu sistēmā POS, izmantojot pogu režģa veidotāju, lai atvērtu URL. Pašlaik tas tiek atbalstīts šādās konfigurācijās:

- Atvērt jaunā logā.
- Atvērt ar POS.
- Atv. iekš. progr.

## <a name="open-in-new-window"></a>Atvērt jaunā logā

Šī konfigurācija nosaka, vai atvērt URL jaunā logā vai programmā. Ja ir konfigurēts, lai tīmekļa URL tiktu atvērts programmā, POS sānu navigācijas panelis un augšējā josla ir redzami un pieejami lietotājiem. Ja konfigurēta atvērš. jaunā logā, URL tiks atvērts jaunā logā programmā Modern POS operētājsist. Windows un jaunā pārlūkprogr. cilnē pārējos POS klientos. Lai to iespējotu, ir jākonfigurē URL, atlasot opciju **Atvērt jaunā logā**.

## <a name="open-within-pos"></a>Atvērt ar POS

Tīm. URL atvērš. ar POS tiek atbalst. tikai progr. Modern POS operētājs. Windows. Citos klientos šī iespēja ir izstrādes stadijā, un to plānots izlaist turpmākajos atjauninājumos. Lai to iespējotu, ir jākonfigurē URL, neatlasot opciju **Atvērt jaunā logā**.

## <a name="open-a-native-app"></a>Atv. iekš. progr.

Šis līdzeklis arī ļauj norādīt ne tīmekļa URL, lai atv. iekš. programmu. Piemēram, varat norādīt tādus URL protokolus kā MailTo, SIP, IM vai MSTEAMS, kurus pēc tam var apstrādāt attiecīgās iekšējās programmas resursierīcē. Lai to iespējotu, ir jākonfigurē URL, atlasot opciju **Atvērt jaunā logā**.

- Windows datoru gadījumā sk. sadaļu [Eksportēt vai importēt noklus. progr. asociācijas](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), lai iestatītu noklus. protokola asociācijas, ja iestatāt datoru, lietojot Deployment Image Servicing and Management (DISM).
- Ja lietojat MDM, piem., Intune, lai pārvaldītu Windows datorus, sk. sad. [Polit. CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).
- Ja esat izstrādātājs, kas veido pielāg. tīm. vietni, sk. sad. [Palaist nokl. progr. URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).

## <a name="open-a-native-app-seamlessly"></a>Integrēti atv. iekš. progr.

Turklāt operētājsistēmas Windows, iOS un Android nodrošina nemanāmāku programmu atvēršanu, pamatojoties uz programmu protokola saistību. Ja progr. vēl nav konfig., lai veiktu atvēršanu no tīm. pārlūkprogr., var būt vajadzīgs izstrād., lai to konfigurētu.

- Windows — sk. [Iesp. progr. vietnēm, lietojot progr. URI apstrād.](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).
- iOS — sk. [Universālās saites izstrādātājiem](https://developer.apple.com/ios/universal-links/).
- Informāciju par operētājsistēmu Android skatiet rakstā [Android programmu saišu apstrāde](https://developer.android.com/training/app-links/).

| Debitors                | Atvērt jaunā logā | Atv. iekš. pr. | Atvērt ar POS | Detalizēta                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Modern POS Windows | ✓\*                | ✓               | ✓              | \* Atveras jaunā Modern POS logā |
| Cloud POS             | ✓\*                | ✓               | X              | \* Atveras jaunā pārlūkprogrammas cilnē        |
| Modern POS iOS     | ✓\*                | ✓               | X              | \* Atveras jaunā pārlūkprogrammas cilnē        |
| Modern POS operētājsistēmā Android | ✓\*                | ✓               | X              | \* Atveras jaunā pārlūkprogrammas cilnē        |

## <a name="before-you-begin"></a>Pirms sākšanas

Pirms sākat, pārskatiet, kā konfigurēt, — [Pārdošanas punkta (POS) ekrāna izkārtojumi](pos-screen-layouts.md).

## <a name="open-url-in-pos"></a>URL atvērš. POS

Lai konfigurētu URL, kas tiks atvērts POS, veiciet šādas darbības.

1. Galv. birojā atv. sad. **Mazumt. \>. Kan. iestat. \> POS iestat. \> POS \> Ekr. izk.**.
2. Atlasiet **Pogu režģi \> Veidotājs**.
3. Izveid. jaunu pogu.
4. Atl. vienuma **Poga** rekviz.
5. Atl. **Atvērt URL** kā darbību.
6. Ievadiet URL, kuru gribat izmantot.
7. Konfigurējiet, vai atvērt URL jaunā logā.
