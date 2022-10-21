---
title: Commerce Tērzēšana ar moduli Power Virtual Agents
description: Šajā rakstā ir aprakstīta Commerce Tērzēšana ar moduli Power Virtual Agents, kas integrē programmu Microsoft Power Virtual Agents ar vietnēm Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690962"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Commerce Tērzēšana ar moduli Power Virtual Agents

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīta Commerce Tērzēšana ar moduli Power Virtual Agents, kas integrē programmu Microsoft Power Virtual Agents ar vietnēm Dynamics 365 Commerce.

Commerce Tērzēšana ar līdzekli Power Virtual Agents sniedz iespēju Dynamics 365 e-commerce Power Virtual Agents debitoriem izmantot tērzētavas iespējas, lai rīkotos ar saviem vaicājumiem. Dynamics 365 Commerce No 10.0.30 laidiena šis līdzeklis var tikt iekļauts e-komercijas vietnēs, izmantojot Commerce Chat ar Power Virtual Agents moduli, kas ir daļa no Commerce moduļu bibliotēkas.

Komercijas tērzēšana ar Power Virtual Agents funkciju palīdz uzņēmumiem sasniegt šādus mērķus:

- Palieliniet personalizētās saistības ar saviem patērētājiem un uzlabot aizturēšanu.
- Palieliniet debitoru pakalpojumu, integrējot pašapkalpošanās tērzēšanu.
- Palieliniet klientu apmierinātību kopumā, tādējādi palielinot pārdošanas apjomu.

> [!NOTE]
> Lai uzzinātu par atšķirībām starp Dynamics 365 For Customer Service Power Virtual Agents un programmām, skatiet Commerce pakalpojumā lietoto [moduļu apskatu](/commerce-chat-modules-overview.md).

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a> Izmantošanas priekšnosacījumi Power Virtual Agents

Lai izmantotu līdzekli Commerce Chat ar Power Virtual Agents, vispirms izveidojiet Power Virtual Agents tērzēšanu jūsu e-komercijas vietnei. Norādījumus skatiet šeit: Virtuālo [aģentu bota izveide](/power-virtual-agents/authoring-first-bot).

Pēc tērzētāja konfigurācijas ir jākopē Bot ID un īrnieka **ID** **parametros tērzētavas parametru vērtības,** lai konfigurētu Commerce tērzēšanas pieredzi. Informāciju par to, kā kopēt šīs vērtības, skatiet Izgūt jūsu [bota Power Virtual Agents parametrus](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>Konfigurēt jūsu e-commerce vietni 

Viens ieteiktais veids, kā izmantot tērzēšanu jūsu e-komercijas vietnē, ir pievienot Commerce Chat ar Power Virtual Agents moduli kopīgotam virsraksta fragmentam, kas tiek izmantots jūsu vietnes lapās.

Lai pievienotu tērzētavas moduli jūsu vietnes virsraksta fragmentam Commerce Site Builder, sekojiet šiem soļiem.

1. Commerce Site Builder jūsu vietā dodieties uz **Fragments**.
1. Atlasiet **Jauna**.
1. Dialoglodziņā Atlasīt **fragmentu atlasiet** moduli **Commerce Tērzēšana Power Virtual Agents** ar, ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Izklāsta skatā atlasiet **Msdstruktūras365 pva tērzēšanas savienotāja slotu**.
1. Rekvizītu rūtī labajā pusē veiciet šādas darbības:

    1. Zem **Bot parametriem** laukā **Bot Framework Webhotel Cdn URL** atstājiet noklusējuma vērtību (piemēram, `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. Laukā **Bot Framework Direct Line Autentifikācijas URL** atstājiet noklusējuma vērtību (piemēram, `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. Laukā **Bot ID** ievadiet bota Power Virtual Agents **ID** vērtību, kas tika kopēta sadaļas [Lietošanas priekšnosacījumi Power Virtual Agents](#prereq).
    1. Laukā **Nomnieka ID** ievadiet kopēto **nomnieka ID** vērtību.

1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Fragmenti** un atveriet jūsu vietnes virsraksta fragmentu.
1. Noklusējuma konteinera **slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **fragmentu**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet iepriekš izveidoto tērzēta fragmentu un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="proactive-chat-parameters"></a>Proaktīvās tērzēšanas parametri

Pilnīgu proaktīvās tērzētavas konfigurācijas parametru sarakstu skatiet Commerce [Tērzēšanas moduļa proaktīvās sarakstlodziņa parametros](chat-proactive-chat-parameters.md).

> [!NOTE]
> Pašlaik neatbalsta Power Virtual Agents Azure Active Directory B2C (Azure AD B2C) autentifikāciju. Tas atbalsta tikai anonīmus Retail Cloud Scale Unit (RCSU) izsaukumus, lai iegūtu preču pieejamību vai mijiedarbotos ar citiem anonīmiem API. Autentificētu API izsaukumi, izmantojot Power Virtual Agents tērzētajus, pieprasa precīzi formulētu debitora piereģistrēšanos.

## <a name="additional-resources"></a>Papildu resursi

[Commerce tērzēšanas līdzekļu pārskats](commerce-chat-overview.md)

[Commerce Tērzēšana ar Debitorachannel klientu pakalpojuma modulim](commerce-chat-module.md)

[Commerce tērzēšanas moduļa proaktīvās tērzētavas parametri](chat-proactive-chat-parameters.md)
