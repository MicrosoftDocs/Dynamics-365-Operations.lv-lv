---
title: URL atvēršana punktā POS
description: Šajā rakstā ir apskatīti uzlabojumi, kas veikti preču un debitoru meklēšanas funkcijai sistēmā Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 529908df866c71ea84d90bbb5d46b23311ed74d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853966"
---
# <a name="open-url-in-pos"></a>URL atvēršana punktā POS

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā var konfigurēt pogu Dynamics 365 Commerce pārdošanas punktā (POS), lai atvērtu vietrādi URL. Šim līdzeklim nav nepieciešama koda pielāgošana, un to var konfigurēt persona, kurai nav izstrādātāja lomas. 

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

- Windows datoru gadījumā sk. sadaļu [Eksportēt vai importēt noklus. progr. asociācijas](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), lai iestatītu noklus. protokola asociācijas, ja iestatāt datoru, lietojot Deployment Image Servicing and Management (DISM).
- Ja lietojat MDM, piem., Intune, lai pārvaldītu Windows datorus, sk. sad. [Polit. CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).
- Ja esat izstrādātājs, kas veido pielāg. tīm. vietni, sk. sad. [Palaist nokl. progr. URI](/windows/uwp/launch-resume/launch-default-app).

## <a name="open-a-native-app-seamlessly"></a>Integrēti atv. iekš. progr.

Turklāt operētājsistēmas Windows, iOS un Android nodrošina nemanāmāku programmu atvēršanu, pamatojoties uz programmu protokola saistību. Ja progr. vēl nav konfig., lai veiktu atvēršanu no tīm. pārlūkprogr., var būt vajadzīgs izstrād., lai to konfigurētu.

- Windows — sk. [Iesp. progr. vietnēm, lietojot progr. URI apstrād.](/windows/uwp/launch-resume/web-to-app-linking).
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

1. Galvenajā birojā atveriet **Retail and Commerce\>Kanāla iestatījumi \> POS iestatījumi \> POS \> Ekrāna izkārtojumi**.
2. Atlasiet **Pogu režģi \> Veidotājs**.
3. Izveid. jaunu pogu.
4. Atl. vienuma **Poga** rekviz.
5. Atl. **Atvērt URL** kā darbību.
6. Ievadiet URL, kuru gribat izmantot.
7. Konfigurējiet, vai atvērt URL jaunā logā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
