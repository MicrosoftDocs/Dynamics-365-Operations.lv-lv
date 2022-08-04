---
title: Kopēt saturu citā darbības vietā
description: Šajā rakstā ir aprakstīts, kā kopēt esošo saturu citā vietā vietas veidotājā Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: bcfa3c7cb2ea8018422803d85df6b6761b8d1145
ms.sourcegitcommit: d719d0a549aecac231fad0abb42250eab9dd0ded
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/07/2022
ms.locfileid: "9126469"
---
# <a name="copy-content-to-another-locale"></a>Kopēt saturu citā darbības vietā

[!include[banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā kopēt esošo saturu citā vietā vietas veidotājā Microsoft Dynamics 365 Commerce.

Kad izveidojat saturu Commerce Site Builder, tas vienmēr tiek saistīts ar atrašanās vietas identifikatoru, piemēram, "en-us". Varat kopēt atsevišķas lapas un līdzekļus uz citu darbības vietu tajā pašā e-komercijas vietnē, pārslēdzot darbības vietu, kad rediģējat satura krājumu un pēc tam izveidojot jaunu preces variantu. Dažos gadījumos, piemēram, palaižot pilnīgi jaunu darbības vietu savā StoreFront, ir jēga dublēt visus satura vienumus esošajā darbības vietā jaunajā darbības vietā. Ja jaunajai atrašanās vietai ir tāda pati pamatvaloda kā vienai no esošajām lokalizācijām, varat izmantot esošo atrašanās vietas nosaukumu kā avota darbības atrašanās vietas nosaukumu atrašanās vietas kopēšanai. (Piemēram, "en-us" un "en-au" lokāļi abi lieto angļu valodu.) Šādā veidā jūs palīdziet samazināt darbu, kas ir nepieciešams, lai lokalizētu saturu jaunā atrašanās vietā.

Šīs procedūras skaidro veidu, kā pievienot jaunu vietējo kanālu esošam kanālam, pārkopēt visus satura elementus no esošās atrašanās vietas uz jaunu atrašanās vietu un pārraudzīt atrašanās vietas kopijas operācijas statusu.

## <a name="add-a-new-locale"></a>Pievienot jaunu darbības vietu

Lai pievienotu jaunu darbības vietu Commerce Site Builder, sekojiet šiem soļiem.

1. Vietņu veidotājā dodieties uz jūsu vietni.
1. Kreisajā navigācijas rūtī atlasiet Vietnes iestatījumi **un pēc** tam atlasiet **Kanāli**.
1. Sadaļā **Kanāls** atlasiet kanālu, lai pievienotu tam jaunu atrašanās laiku.
1. Kanāla dialoglodziņā, kas parādās labajā pusē, atlasiet **Pievienot darbības vietu**.
1. **Dialoglodziņa Pievienot atrašanās vietu** laukā **Lokāle, lai atbalstītu**, atlasiet darbības vietu.
1. Apstipriniet, ka **domēna** vērtība ir pareiza.
1. **Ceļā ievadiet unikālu URL ceļu (piemēram,** en-us vai **english**-us **·**).
1. Atlasiet **Labi**.
1. Aizveriet kanāla dialoglodziņu.
1. Sadaļā **Kanāls** apstipriniet, ka jaunā atrašanās vietas informācija ir uzskaitīta blakus pareizajam kanālam.
1. Atlasiet **Saglabāt un publicēt**.

> [!NOTE]
> Pirms jauno darbības vietu var konfigurēt vietas veidotājā, tā ir jāpievieno saistītam tiešsaistes veikala kanālam programmā Commerce Headquarters.

## <a name="copy-all-content-items-to-a-new-locale"></a>Kopēt visus satura vienumus jaunā atrašanās sarakstā

Lai kopētu visus satura vienumus jaunā uzņēmuma vietnes veidotājā, sekojiet šiem soļiem.

1. Vietņu veidotājā dodieties uz jūsu vietni.
1. Kreisajā navigācijas rūtī atlasiet Vietnes iestatījumi **un pēc** tam atlasiet **Kanāli**.
1. Komandjoslā atlasiet Izveidot lokalizācijas **kopiju**.
1. Dialoglodziņā Izveidot **lokalizācijas kopiju**, kas parādās labajā pusē, **sadaļā Avota** vietne apstipriniet, ka ir atlasīta pareizā vieta.
1. **Avota kanāla** laukā atlasiet avota kanālu.
1. Mērķa kanāla **laukā** atlasiet to pašu avota kanālu.
1. Laukā **Avota atrašanās** vietas atlasiet avota atrašanās vietu.
1. Laukā **Mērķa atrašanās** vieta atlasiet jauno darbības vietu.
1. Atlasiet **Kopēt darbības vietas**. Paziņojums apstiprina, ka tika sākta lokalizācijas kopēšanas operācija.

> [!NOTE]
> Var arī kopēt saturu starp dažādiem kanāliem.

## <a name="monitor-the-status-of-the-locale-copy"></a>Pārraudzīt atrašanās vietas kopijas statusu

Lai pārraudzītu atrašanās vietas kopēšanas operācijas statusu, sekojiet šiem soļiem.

1. Vietņu veidotājā dodieties uz jūsu vietni.
1. Kreisajā navigācijas rūtī atlasiet Vietnes iestatījumi **un** pēc tam atlasiet **Darbi**.
1. Zem **Pašreizējie darbi** atlasiet darbu, kas jāpārrauga. Darba detaļas ir parādītas dialoglodziņā, kas redzams labajā pusē.
