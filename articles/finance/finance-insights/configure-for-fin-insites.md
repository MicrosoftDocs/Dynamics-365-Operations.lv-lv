---
title: Finance ieskatu konfigurācija
description: Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finance Insights.
author: ShivamPandey-msft
ms.date: 01/27/2022
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
ms.openlocfilehash: b9bad6445e9e77688f66c6c4186422d7a898edd7
ms.sourcegitcommit: 7fc0a9a6440ac087292e9e76c26c67f56154b9e6
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/28/2022
ms.locfileid: "8051374"
---
# <a name="configuration-for-finance-insights"></a>Finance ieskatu konfigurācija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finanšu ieskati apvieno Microsoft Dynamics 365 Finance funkcionalitāti ar Dataverse, Azure un AI Builder nodrošina jaudīgus prognozēšanas rīkus jūsu organizācijai. Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finance Insights. Lai veiksmīgi pabeigtu šajā tēmā dotās procedūras, power portal administrēšanas centrā [ir nepieciešama sistēmas administratora un sistēmas pielāgotāja piekļuve](https://admin.powerplatform.microsoft.com/), sistēmas administratora piekļuve Dynamics 365 Finance programmā un piekļuve vides izveidei dzīves cikla pakalpojumos Microsoft Dynamics (LCS).

> [!NOTE]
> Tālāk norādītās finanšu ieskatu iestatīšanas procedūras ir derīgas versijas 10.0.21 versijām Dynamics 365 Finance un jaunākām versijām.

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance izvietošana

Lai izvietotu vides, veiciet tālāk norādītās darbības.

1. LCS izveidojiet vai atjauniniet Dynamics 365 Finance vidi. Videi ir nepieciešama lietotnes versija 10.0.21 vai jaunāka versija.

    > [!NOTE]
    > Videi jābūt augstas pieejamības (HA) videi. (Šis vides veids ir pazīstams arī kā 2. līmeņa vide.) Lai iegūtu papildu informāciju, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Ja konfigurējat Finance ieskatus smilškastes vidē, iespējams, ražošanas dati ir jākopē šajā vidē, pirms darbosies prognozes. Prognozēšanas modelī tiek izmantoti vairāki datu gadi, lai izveidotu prognozes. Contoso demonstrācijas datos nav pietiekami daudz vēsturisko datu, lai atbilstoši apmācītu prognozēšanas modeli. 

## <a name="configure-your-azure-ad-tenant"></a>Nomnieka konfigurēšana Azure AD

Azure Active Directory(Azure AD) jākonfigurē tā, lai to varētu izmantot kopā ar Dataverse lietojumprogrammām un ar Microsoft Power Platform to. Šai konfigurācijai ir nepieciešams, **lai lietotājam** LCS laukā Projekta drošības loma **tiktu piešķirta loma Projekta īpašnieks** vai **vides pārvaldnieks**.

Pārbaudiet, vai ir pabeigta šāda iestatīšana:

- Power Portal administrēšanas centrā ir **sistēmas administratora** un **sistēmas pielāgotāja** piekļuve.
- Lietotājam Dynamics 365 Finance, kurš instalē finance insights pievienojumprogrammu, tiek lietota vai līdzvērtīga licence.

Tiek reģistrētas Azure AD šādas Azure AD programmas.

|  Pieteikums                             | Programmas ID                               |
|------------------------------------------|--------------------------------------|
| Microsoft Dynamics ERP apakšpakalpojumi CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    
## <a name="configure-dataverse"></a>Dataverse konfigurēšana

Sekojiet tālāk norādītajām darbībām, lai konfigurētu Dataverse programmai Finance Insights.

- Atveriet vides lapu LCS un pārbaudīt, vai sadaļa **Power Platform integrācija** jau ir instalēta.

    - Ja Dataverse tas jau ir iestatīts, Dataverse jānorāda vides nosaukums, kas saistīts ar finanšu vidi.
    - Ja Dataverse vēl nav iestatīts, atlasiet **Uzstādīšana**. Dataverse Vides iestatīšana var ilgt līdz pat stundai. Kad iestatīšana ir veiksmīgi pabeigta, jānorāda vides nosaukums, Dataverse kas ir saistīts ar vidē Finanses.
    - Ja šī integrācija ir iestatīta ar esošu Microsoft Power Platform vidi, sazinieties ar administratoru, lai pārliecinātos, vai saistītā vide nav atspējotā stāvoklī.

        Papildinformāciju skatiet rakstā [Integrācijas Power Platform iespējošana](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Lai piekļūtu Microsoft Power Platform administrēšanas vietnei, dodieties uz <https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights pievienojumprogrammas konfigurēšana

Ja iepriekš instalējāt finance ieskatu pievienojumprogrammu, atinstalējiet to pirms šīs darbības pabeigšanas.

> [!NOTE]
> Ja jau esat instalējis datu ezera pievienojumprogrammu LCS, Finance ieskati to izmantos, lai saglabātu datus, kas nepieciešami prognozēm. Ja vēl neesat instalējis datu ezera pievienojumprogrammu LCS, pievienojumprogramma Finance insights izveidos jums pārvaldītu datu ezeru.

Izpildiet šīs darbības, lai instalētu Finance Insights pievienojumprogrammu.

1. Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.
2. Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.
3. Atlasiet pievienojumprogrammu **Finance Insights**.
4. Piekrītiet noteikumiem un nosacījumiem un pēc tam atlasiet **Instalēt**.

Pievienojumprogrammas instalēšana var ilgt vairākas minūtes.

## <a name="one-last-thing"></a>Vēl viena lieta...

Kad pievienojumprogramma ir veiksmīgi instalēta, var paiet līdz pat stundai, līdz programmā var iespējot Finance Insights līdzekļus **līdzekļu pārvaldības** darbvietā.Dynamics 365 Finance Ja nevēlaties tik ilgi gaidīt, varat manuāli palaist **ieskatu nodrošināšanas statusa pārbaudes** procesu. 

1. Sadaļā Dynamics 365 Finance dodieties uz **Sistēmas administrēšanas \> iestatīšanas \> procesa automatizācija**.
2. Cilnē **Fona procesi** atrodiet **ieskatu nodrošinājuma statusa pārbaudi** un atlasiet **Rediģēt**.
3. **Iestatiet lauku Nākamā izpilde** 30 minūtes pirms pašreizējā laika.

   Šīm izmaiņām vajadzētu likt **nekavējoties palaist ieskatu nodrošināšanas statusa pārbaudes** procesu.

   **Kad ieskatu nodrošināšanas statusa pārbaudes** process ir veiksmīgi palaists, līdzekļu pārvaldības **darbvietā** varat iespējot Finance insights līdzekļus.

> [!NOTE]
> **Ja ieskatu nodrošināšanas statusa pārbaudes** process netiek palaists, dodieties uz **Sistēmas administrēšanaInquiriesBatch** > **·** > **darbiem**. Laukā **Procesu automatizācijas aptaujas sistēma** mainiet vērtību uz **Gaida**, lai sāktu procesu. 
> 
## <a name="feedback-and-support"></a>Atsauksmes un atbalsts

Ja vēlaties sniegt atsauksmes vai ja jums ir nepieciešams atbalsts, sūtiet e-pasta ziņojumus Finance [insights (Preview)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
