---
title: Finanšu ieskatu konfigurācija
description: Šajā rakstā skaidroti konfigurācijas soļi, kas iespējos jūsu sistēmu izmantot iespējas, kas ir pieejamas Finanšu ieskatos.
author: ShivamPandey-msft
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 07edea234839a477802e5cd875620509c8f92d69
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644119"
---
# <a name="configuration-for-finance-insights"></a>Finanšu ieskatu konfigurācija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finanšu ieskatījumi apvieno funkcionalitāti no Microsoft Dynamics 365 Finansēm ar Dataverse, Azure AI Builder un nodrošina jaudīgus prognozēšanas rīkus jūsu organizācijai. Šajā rakstā skaidroti konfigurācijas soļi, kas iespējos jūsu sistēmu izmantot iespējas, kas ir pieejamas Finanšu ieskatos. Lai veiksmīgi pabeigtu šī raksta procedūras, [jums ir jābūt sistēmas administratoram un sistēmas pielāgotāja piekļuvei Power Portal](https://admin.powerplatform.microsoft.com/) administrēšanas Microsoft Dynamics centrā, sistēmas administratora piekļuvei Dynamics 365 finansēm un piekļuvei, lai izveidotu vides lifecycle Services (LCS).

> [!NOTE]
> Tālāk norādītās procedūras finanšu ieskatu iestatīšanai ir derīgas Dynamics 365 Finanšu versijas 10.0.21 vai jaunākai versijai.

## <a name="deploy-dynamics-365-finance"></a>Izvietojiet Dynamics 365 finanses

Lai izvietotu vides, veiciet tālāk norādītās darbības.

1. LCS izveidojiet vai atjauniniet Dynamics 365 finanšu vidi. Videi nepieciešama programmas versija 10.0.21 vai jaunāka.

    > [!NOTE]
    > Videi jābūt augsta pieejamības (MAKS) videi. (Šis vides veids ir pazīstams arī kā 2. līmeņa vide.) Lai iegūtu papildu informāciju, skatiet [Vides plānošana](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

2. Ja finanšu ieskatu konfigurēšana tiek konfigurēta kastu vidē, iespējams, ražošanas dati jākopē šajā vidē pirms prognozēšanas darbosies. Prognozēšanas modelī tiek izmantoti vairāki datu gadi, lai izveidotu prognozes. Contoso demonstrācijas dati neietver pietiekamus vēsturiskos datus, lai nodrošinātu to, ka prognozēšanas modelis tiek sagatavots. 

## <a name="configure-your-azure-ad-tenant"></a>Konfigurēt savu Azure AD nomnieku

Azure Active Directory(Azure AD) jābūt konfigurētam tā, lai to varētu izmantot kopā ar Dataverse lietojumprogrammu un Microsoft Power Platform lietojumprogrammām. Šai konfigurācijai ir nepieciešams **, lai lietotājam LCS laukā Projekta drošības loma būtu piešķirta loma Projekta** **·** **īpašnieks** vai Vides vadītājs.

Pārbaudiet, vai ir pabeigta šāda iestatīšana:

- Biznesa portāla **administratora centrā** jums **ir piekļuve Sistēmas** administratoram un Sistēmas pielāgotājam.
- Dynamics 365 finanses vai ekvivalenta licence tiek lietota lietotājam, kurš instalē finanšu ieskatu pievienojumprogrammu.
- Tālāk norādītās Azure AD programmas ir reģistrētas Azure AD.

    |  Pieteikums                             | Programmas ID                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP apakšpakalpojumi CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |

    Lai pārbaudītu, vai pieteikums ir reģistrēts Azure AD, pārbaudiet visu **pieteikumu** sarakstu. Papildinformāciju skatiet sadaļā Uzņēmuma [lietojumprogrammu skatīšana](/azure/active-directory/manage-apps/view-applications-portal).
  
    Ja programma nav reģistrēta, sazinieties ar Azure AD atbalsta dienestu.
  
## <a name="configure-dataverse"></a>Dataverse konfigurēšana

Sekojiet tālāk norādītajām darbībām, lai konfigurētu Dataverse programmai Finance Insights.

- Atveriet vides lapu LCS un pārbaudīt, vai sadaļa **Power Platform integrācija** jau ir instalēta.

    - Ja Dataverse tas jau ir iestatīts, ir Dataverse jāuzskaita ar Finanšu vidi saistītais vides nosaukums.
    - Ja Dataverse vēl nav iestatīts, atlasiet **Iestatījumi**. Vides iestatījums Dataverse var ilgt stundu. Kad uzstādīšana ir veiksmīgi pabeigta, ir Dataverse jāuzskaita vides nosaukums, kas saistīts ar Finanšu vidi.
    - Ja šī integrācija tika iestatīta ar esošu vidi Microsoft Power Platform, sazinieties ar savu administratoru, lai pārliecinātos, vai saistītā vide nav atspējotā stāvoklī.

        Papildinformāciju skatiet sadaļā [Integrācijas Power Platform iespējošana](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Lai piekļūtu administratora Microsoft Power Platform vietnei, dodieties uz <https://admin.powerplatform.microsoft.com/environments>.

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

Kad pievienojumprogramma ir veiksmīgi instalēta, var paiet stunda, **pirms** Dynamics 365 Finanses līdzekļu pārvaldības darbvietā varat iespējot Finanšu ieskatu līdzekļus. Ja nevēlaties gaidīt šo ilgu laiku, varat manuāli palaist ieskatu **nodrošinājuma statusa pārbaudes** procesu. 

1. Programmā Dynamics 365 Finanses dodieties uz sistēmas administrēšanas iestatīšanas **procesa \>\> automatizāciju**.
2. Cilnē Fona **procesi atrodiet** ieskatu **nodrošinājuma statusa pārbaudi un** atlasiet **Rediģēt**.
3. Iestatiet lauku **Nākamā izpilde** 30 minūtes pirms pašreizējā laika.

   Šai izmaiņai ir jāpārtrauc **uzkrājumu nodrošinājuma statusa** pārbaudes process.

   Kad ieskatu **nodrošinājuma statusa pārbaudes process** ir veiksmīgi palaists, finanšu ieskatu līdzekļus var iespējot līdzekļu pārvaldības **darbvietā**.

> [!NOTE]
> Ja ieskatu **nodrošinājuma statusa pārbaudes process** nedarbojas, pārejiet uz sadaļu Sistēmas **administrēšanas** > **uzziņu pakešuzdevumi** > **·**. Laukā Procesa **automatizācijas aptauju** sistēma mainiet vērtību uz **Gaida**, lai sāktu procesu. 
> 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
