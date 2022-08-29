---
title: Konsekventa piegādes režīma apstrādes iespējošana e-komercijas kanālos
description: Šajā rakstā ir aprakstīts, kā iespējot konsekventu piegādes veida apstrādi, lai novērstu iespējamas problēmas, kas saistītas ar maksu plūsmām Microsoft Dynamics 365 Commerce e-komercijas kanālos.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 43450c9d380bd57c234bb1c9acfbe296ab115f14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279655"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Konsekventa piegādes režīma apstrādes iespējošana e-komercijas kanālos 

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā iespējot konsekventu piegādes veida apstrādi, lai novērstu iespējamas problēmas, kas saistītas ar maksu plūsmām Microsoft Dynamics 365 Commerce e-komercijas kanālos.

Nestandarta Dynamics 365 Commerce virsraksta līmeņa maksas netiek piemērotas pēc noklusējuma e-komercijas kanālos. Šī uzvedība var radīt vienu vai abus no šiem jautājumiem e-komercijas kanālos:

- Netiek parādītas nestandarta virsraksta līmeņa maksas.
- Piegādes veidu maksas neatbilst piegādes atlases režīmam un pārbaudes pasūtījuma kopsavilkumam.

Lai novērstu šos jautājumus, ir jāaktivizē Iespējot **konsekventu piegādes veida apstrādi kanāla funkcijai**. Šī funkcija nodrošina, ka neatkārtotas virsraksta līmeņa maksas tiek parādītas e-komercijas kanālos un ka pārdošanas pasūtījuma piegādes informācija tiek pastāvīgi apstrādāta ar to pašu pieprasījuma darbplūsmu.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Ieslēgt iespējot saskaņotās piegādes režīma apstrādi kanāla funkcijai

Lai iespējotu saskaņoto **piegādes režīmu apstrādi commerce** headquarters kanāla līdzeklī, izpildiet šīs darbības.

1. Atveriet līdzekļu pārvaldības **darbvietu** (sistēmas administrēšanas **darbalauku \> līdzekļu \> pārvaldība**).
1. Pieejamo līdzekļu sarakstā meklējiet un atlasiet Iespējot konsekventu **piegādes veida apstrādi kanālā**.
1. Labās puses rūtī izvēlieties Aktivizēt **tagad**.
