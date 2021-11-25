---
title: Finance ieskatu konfigurācija
description: Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finance Insights.
author: ShivamPandey-msft
ms.date: 1/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5668d3ddff777645b4f1c6608f025d0c5a63208a
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752982"
---
# <a name="configuration-for-finance-insights"></a>Finance ieskatu konfigurācija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights apvieno Microsoft Dynamics 365 Finance funkcionalitāti ar Dataverse, Azure un AI Builder, lai nodrošinātu jaudīgus prognozēšanas rīkus jūsu organizācijai. Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finance Insights. Lai veiksmīgi pabeigtu šajā tēmā dotās procedūras, jums ir nepieciešama sistēmas administratora un sistēmas pielāgotāja piekļuve [Power Portal administrēšanas centrā, Sistēmas administratora piekļuve programmā un piekļuve vides izveidei dzīves cikla](https://admin.powerplatform.microsoft.com/)Dynamics 365 Finance Microsoft Dynamics pakalpojumos (LCS).

> [!NOTE]
> Tālāk norādītās finanšu ieskatu iestatīšanas procedūras ir derīgas Dynamics 365 Finance versijas 10.0.21 versijām un jaunākām versijām.

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance izvietošana

Lai izvietotu vides, veiciet tālāk norādītās darbības.

1. LCS izveidojiet vai atjauniniet Dynamics 365 Finance vidi. Videi ir nepieciešama lietotnes versija 10.0.21 vai jaunāka versija.

    > [!NOTE]
    > Videi jābūt augstas pieejamības (HA) videi. (Šis vides veids ir pazīstams arī kā 2. līmeņa vide.) Lai iegūtu papildu informāciju, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Ja konfigurējat Finance ieskatus smilškastes vidē, iespējams, ražošanas dati ir jākopē šajā vidē, pirms darbosies prognozes. Prognozēšanas modelī tiek izmantoti vairāki datu gadi, lai izveidotu prognozes. Contoso demonstrācijas datos nav pietiekami daudz vēsturisko datu, lai atbilstoši apmācītu prognozēšanas modeli. 

## <a name="configure-dataverse"></a>Dataverse konfigurēšana

Sekojiet tālāk norādītajām darbībām, lai konfigurētu Dataverse programmai Finance Insights.

- Atveriet vides lapu LCS un pārbaudīt, vai sadaļa **Power Platform integrācija** jau ir instalēta.

    - Ja tā jau ir iestatīta, jāuzskaita ar Finance vidi saistītais Dataverse vides nosaukums.
    - Ja tas vēl nav iestatīts, atlasiet **Uzstādīšana**. Vides iestatīšana Dataverse var ilgt līdz pat stundai. Kad iestatīšana ir veiksmīgi pabeigta, Dataverse jānorāda vides nosaukums, kas saistīts ar finanšu vidi.

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights pievienojumprogrammas konfigurēšana

Ja iepriekš instalējāt finance ieskatu pievienojumprogrammu, atinstalējiet to pirms šīs darbības pabeigšanas.

> [!NOTE]
> Ja jau esat instalējis datu ezera pievienojumprogrammu LCS, Finance ieskati to izmantos, lai saglabātu datus, kas nepieciešami prognozēm. Ja vēl neesat instalējis datu ezera pievienojumprogrammu LCS, pievienojumprogramma Finance insights izveidos jums pārvaldītu datu ezeru.

Izpildiet šīs darbības, lai instalētu Finance Insights pievienojumprogrammu.

1. Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.
2. Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.
3. Atlasiet pievienojumprogrammu **Finance Insights**.
4. Piekrītu noteikumiem un nosacījumiem un pēc tam atlasiet **Instalēt**.

Pievienojumprogrammas instalēšana var ilgt vairākas minūtes.

## <a name="one-last-thing"></a>Vēl viena lieta...

Kad pievienojumprogramma ir veiksmīgi instalēta, var paiet līdz pat stundai, līdz programmā var iespējot Finance Insights līdzekļus **līdzekļu pārvaldības** Dynamics 365 Finance darbvietā. Ja nevēlaties tik ilgi gaidīt, varat manuāli palaist **ieskatu nodrošināšanas statusa pārbaudes** procesu. 

1. Sadaļā Dynamics 365 Finance dodieties uz **Sistēmas administrēšanas \>\> iestatīšanas procesa automatizācija**.
2. Cilnē **Fona procesi** atrodiet **ieskatu nodrošināšanas statusa pārbaudi un** atlasiet Rediģēt **·**.
3. Iestatiet **lauku Nākamā izpilde** 30 minūtes pirms pašreizējā laika.

   Šīm izmaiņām vajadzētu likt **nekavējoties palaist ieskatu nodrošināšanas statusa pārbaudes** procesu.

   Kad **ieskatu nodrošināšanas statusa pārbaudes** process ir veiksmīgi palaists, līdzekļu pārvaldības darbvietā varat iespējot Finance insights **·** līdzekļus.

## <a name="feedback-and-support"></a>Atsauksmes un atbalsts

Ja vēlaties sniegt atsauksmes vai ja jums ir nepieciešams atbalsts, sūtiet e-pasta [ziņojumus Finance insights (Preview)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
