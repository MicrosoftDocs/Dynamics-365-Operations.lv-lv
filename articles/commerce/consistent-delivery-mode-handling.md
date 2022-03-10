---
title: Atļaut konsekventu piegādes režīmu apstrādi e-komercijas kanālos
description: Šajā tēmā ir aprakstīts, kā iespējot konsekventu piegādes veida apstrādi, lai novērstu iespējamas problēmas, kas saistītas ar maksu plūsmām Microsoft Dynamics 365 Commerce e-komercijas kanālos.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 4cecd70dacd72572afc8e6cb65530bf2be4cc93d
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349927"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Atļaut konsekventu piegādes režīmu apstrādi e-komercijas kanālos 

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iespējot konsekventu piegādes veida apstrādi, lai novērstu iespējamas problēmas, kas saistītas ar maksu plūsmām Microsoft Dynamics 365 Commerce e-komercijas kanālos.

Nestandarta Dynamics 365 Commerce virsraksta līmeņa maksas netiek piemērotas pēc noklusējuma e-komercijas kanālos. Šī uzvedība var radīt vienu vai abus no šiem jautājumiem e-komercijas kanālos:

- Netiek parādītas nestandarta virsraksta līmeņa maksas.
- Piegādes veidu maksas neatbilst piegādes atlases režīmam un pārbaudes pasūtījuma kopsavilkumam.

Lai novērstu šos jautājumus, ir jāaktivizē Iespējot **konsekventu piegādes veida apstrādi kanāla funkcijai**. Šī funkcija nodrošina, ka neatkārtotas virsraksta līmeņa maksas tiek parādītas e-komercijas kanālos un ka pārdošanas pasūtījuma piegādes informācija tiek pastāvīgi apstrādāta ar to pašu pieprasījuma darbplūsmu.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Ieslēgt iespējot saskaņotās piegādes režīma apstrādi kanāla funkcijai

Lai iespējotu saskaņoto **piegādes režīmu apstrādi commerce** headquarters kanāla līdzeklī, izpildiet šīs darbības.

1. Atveriet līdzekļu pārvaldības **darbvietu** (sistēmas administrēšanas **darbalauku \> līdzekļu \> pārvaldība**).
1. Pieejamo līdzekļu sarakstā meklējiet un atlasiet Iespējot konsekventu **piegādes veida apstrādi kanālā**.
1. Labās puses rūtī izvēlieties Aktivizēt **tagad**.
