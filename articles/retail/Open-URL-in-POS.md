---
title: "URL atvērš. POS"
description: "Šajā tēmā ir sniegts apskats par uzlabojumiem, kas ir ieviesti programmas Microsoft Dynamics 365 for Retail preču un debitoru meklēšanas funkcionalitātē."
author: AamirAllaq
manager: AnnBe
ms.date: 11/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: d2b692ac86244eca31780a558112167391fc6d77
ms.contentlocale: lv-lv
ms.lasthandoff: 01/04/2019

---

# <a name="open-url-in-pos"></a>URL atvērš. POS

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā konfig. pogu sistēmā Retail POS (pārdošanas punkts), lai atvērtu URL. Šim līdzeklim nav nepieciešama koda pielāgošana, un to var konfigurēt persona, kurai nav izstrādātāja lomas.

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

Windows, iOS un Android arī ļauj integrētāk atv. programmas, balstoties uz progr. protokola asociāciju. Ja progr. vēl nav konfig., lai veiktu atvēršanu no tīm. pārlūkprogr., var būt vajadzīgs izstrād., lai to konfigurētu.

- Windows — sk. [Iesp. progr. vietnēm, lietojot progr. URI apstrād.](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).
- iOS — sk. [Universālās saites izstrādātājiem](https://developer.apple.com/ios/universal-links/).
- Android — sk. [Android progr. saišu apstrāde](https://developer.android.com/training/app-links/).

| Klients                | Atvērt jaunā logā | Atv. iekš. pr. | Atvērt ar POS | Detalizēta                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Modern POS Windows | ✓\*                | ✓               | ✓              | \* Atveras jaunā Modern POS logā |
| Cloud POS             | ✓\*                | ✓               | X              | \* Atveras jaunā pārlūkprogrammas cilnē        |
| Modern POS iOS     | ✓\*                | ✓               | X              | \* Atveras jaunā pārlūkprogrammas cilnē        |
| Modern POS Android | ✓\*                | ✓               | X              | \* Atveras jaunā pārlūkprogrammas cilnē        |

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

