---
title: Finanšu ieskatu konfigurācija
description: Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finance Insights.
author: ShivamPandey-msft
ms.date: 11/19/2021
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
ms.openlocfilehash: 6183e8a7500e9deff0ebf6b5dec8842ad4ca94cb
ms.sourcegitcommit: 6a9f068b59b62c95a507d1cc18b23f9fd80a859b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/20/2021
ms.locfileid: "7827032"
---
# <a name="configuration-for-finance-insights"></a>Finanšu ieskatu konfigurācija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights apvieno Microsoft Dynamics 365 Finance funkcionalitāti ar Dataverse, Azure un AI Builder, lai nodrošinātu jaudīgus prognozēšanas rīkus jūsu organizācijai. Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finance Insights. Lai veiksmīgi pabeigtu šīs tēmas procedūras, jums jābūt sistēmas administratoram un sistēmas pielāgotāja piekļuvei [Power Portal administrēšanas centrā ](https://admin.powerplatform.microsoft.com/), sistēmas administratora piekļuvei un piekļuvei, lai izveidotu videsDynamics 365 Finance pakalpojumos Microsoft Dynamics Lifecycle Services (LCS).

> [!NOTE]
> Tālāk norādītās procedūras Finanšu ieskatu iestatīšanai ir derīgas versijā Dynamics 365 Finance 10.0.21 vai jaunākās versijās.

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance izvietošana

Lai izvietotu vides, veiciet tālāk norādītās darbības.

1. LCS izveidojiet vai atjauniniet Dynamics 365 Finance vidi. Videi nepieciešama programmas versija 10.0.21 vai jaunāka.

    > [!NOTE]
    > Videi jābūt augsta pieejamības (MAKS) videi. (Šis vides veids ir pazīstams arī kā 2. līmeņa vide.) Lai iegūtu papildu informāciju, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Ja finanšu ieskatu konfigurēšana tiek konfigurēta kastu vidē, iespējams, ražošanas dati jākopē šajā vidē pirms prognozēšanas darbosies. Prognozēšanas modelī tiek izmantoti vairāki datu gadi, lai izveidotu prognozes. Contoso demonstrācijas dati neietver pietiekamus vēsturiskos datus, lai nodrošinātu to, ka prognozēšanas modelis tiek sagatavots. 

## <a name="configure-your-azure-ad-tenant"></a>Konfigurēt savu Azure AD nomnieku

Azure Active Directory() Azure AD jābūt konfigurētam tā, lai to varētu izmantot kopā ar Dataverse lietojumprogrammu un Microsoft Power Platform lietojumprogrammām. Šai konfigurācijai ir nepieciešams, lai **lietotājam** **·** **LCS** laukā Projekta drošības loma būtu piešķirta loma Projekta īpašnieks vai Vides vadītājs.

Pārbaudiet, vai ir pabeigta šāda iestatīšana:

- Biznesa portāla **administratora centrā jums ir piekļuve Sistēmas** **administratoram** un Sistēmas pielāgotājam.
- Vai Dynamics 365 Finance ekvivalenta licence tiek lietota lietotājam, kurš instalē Finanšu ieskatu pievienojumprogrammu.

Tālāk norādītās Azure AD programmas ir Azure AD reģistrētas.

|  Pieteikums                             | Programmas ID                               |
|------------------------------------------|--------------------------------------|
| Microsoft Dynamics ERP apakšpakalpojumi CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    
## <a name="configure-dataverse"></a>Dataverse konfigurēšana

Sekojiet tālāk norādītajām darbībām, lai konfigurētu Dataverse programmai Finance Insights.

- Atveriet vides lapu LCS un pārbaudīt, vai sadaļa **Power Platform integrācija** jau ir instalēta.

    - Ja Dataverse tas jau ir iestatīts, ir Dataverse jāuzskaita ar Finanšu vidi saistītais vides nosaukums.
    - Ja Dataverse vēl nav iestatīts, atlasiet **Iestatījumi**. Vides Dataverse iestatījums var ilgt stundu. Kad uzstādīšana ir veiksmīgi pabeigta, ir jāuzskaita vides nosaukums, kas Dataverse saistīts ar Finanšu vidi.
    - Ja šī integrācija tika iestatīta ar esošu vidi, sazinieties ar savu administratoru, lai pārliecinātos, vai saistītā vide Microsoft Power Platform nav atspējotā stāvoklī.

        Papildinformāciju skatiet sadaļā [Integrācijas Power Platform](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md) iespējošana. 

        Lai piekļūtu Microsoft Power Platform administratora vietnei, dodieties <https://admin.powerplatform.microsoft.com/environments> uz.

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights pievienojumprogrammas konfigurēšana

Ja iepriekš instalējāt pievienojumprogrammu Finanšu ieskati, atinstalējiet to pirms tālāk norādītās procedūras pabeigšanas.

> [!NOTE]
> Ja datu pievienojumprogramma LCS jau ir instalēta, finanšu ieskati to izmantos, lai saglabātu prognozēm nepieciešamos datus. Ja vēl neesat instalējis datu in in LCS pievienojumprogrammu, Finanšu ieskatu pievienojumprogramma izveidos pārvaldītu datu summu jūsu vietā.

Izpildiet šīs darbības, lai instalētu Finance Insights pievienojumprogrammu.

1. Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.
2. Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.
3. Atlasiet pievienojumprogrammu **Finance Insights**.
4. Piekrītiet noteikumiem un nosacījumiem un pēc tam atlasiet **Instalēt**.

Pievienojumprogrammas instalēšana var ilgt vairākas minūtes.

## <a name="one-last-thing"></a>Viena pēdējā iespēja...

Pēc pievienojumprogrammas veiksmīgas instalēšanas tā var ilgt kādu stundu, pirms finanšu ieskatu līdzekļus var iespējot programmas **Līdzekļu pārvaldības** Dynamics 365 Finance darbvietā. Ja nevēlaties gaidīt šo ilgu laiku, varat manuāli palaist ieskatu **nodrošinājuma statusa pārbaudes** procesu. 

1. Dodieties Dynamics 365 Finance uz Sistēmas **administrēšanas iestatīšanas \> procesa \> automatizāciju.**
2. Cilnē Fona **procesi** atrodiet **ieskatu nodrošinājuma statusa pārbaudi un atlasiet** **Rediģēt**.
3. Iestatiet lauku **Nākamā** izpilde 30 minūtes pirms pašreizējā laika.

   Šai izmaiņai ir **jāpārtrauc uzkrājumu nodrošinājuma statusa** pārbaudes process.

   Kad **ieskatu nodrošinājuma statusa pārbaudes process ir veiksmīgi palaists, finanšu ieskatu līdzekļus var** iespējot līdzekļu **pārvaldības** darbvietā.

## <a name="feedback-and-support"></a>Atsauksmes un atbalsts

Ja interesējaties par atsauksmju sniegšanu vai ja nepieciešams atbalsts, sūtiet e-pasta ziņojumu uz [Finanšu ieskati (priekšskatījums)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
