---
title: Projekta līgumu un projektu sinhronizēšana tieši no Project Service Automation uz Finance and Operations
description: Šajā tēmā ir aprakstīta veidne un pamata uzdevumi, kas tiek izmantoti, lai tiešā veidā sinhronizētu programmā Microsoft Dynamics 365 for Project Service Automation ietvertos projekta līgumus un projektus ar programmu Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0889bc233674cb80dd056ac77edb5c936c6633a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "312121"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Projekta līgumu un projektu sinhronizēšana tieši no Project Service Automation uz Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta veidne un pamata uzdevumi, kas tiek izmantoti, lai tiešā veidā sinhronizētu programmā Microsoft Dynamics 365 for Project Service Automation ietvertos projekta līgumus un projektus ar programmu Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE] 
> Ja lietojat Microsoft Dynamics 365 for Finance and Operations Enterprise Edition versiju 7.3.0, ir jāinstalē KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Datu plūsma programmas Project Service Automation sinhronizēšanai ar programmu Finance and Operations

> [!NOTE]
> Pirms varat izmantot risinājumu Project Service Automation integrācijai programmā Finance and Operations, ir jāiepazīst Microsoft Dynamics 365 līdzeklis Datu integrācija.

Risinājums, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance and Operations, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance and Operations instancēs. Integrācijas veidne, kas ir pieejama līdzeklī Datu integrācija, iespējo datu plūsmu par projekta līgumiem, projektiem, projekta līguma rindām un projekta līguma rindas atskaites punktiem no programmas Project Service Automation programmā Finance and Operations.

Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance and Operations.

[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, Microsoft PowerApps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Project Service Automation ietverto projekta līgumu un projektu sinhronizēšanai ar programmu Finance and Operations tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekti un līgumi (no PSA uz Fin and Ops)
- **Projekta uzdevumu nosaukums:**

    - Projekta līgumi (no PSA uz Fin and Ops)
    - Projekti (no PSA uz Fin and Ops)
    - Projekta līguma rindas (no PSA uz Fin and Ops)
    - Projekta līguma rindas atskaites punkti (no PSA uz Fin and Ops)

Pirms projekta līgumu un projektu sinhronizēšanas ir jāveic kontu sinhronizēšana.

## <a name="entity-set"></a>Elementu kopa

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| Pasūtījumi                           | Integrācijas elements projekta līgumam                |
| Projekti                         | Integrācijas elements projektam                         |
| Pasūtījuma rindas                      | Integrācijas elements projekta līguma rindai           |
| Projekta līguma rindas atskaites punkti | Integrācijas elements projekta līguma rindas atskaites punktam |

## <a name="entity-flow"></a>Elementu plūsma

Projekta līgumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance and Operations kā projekta līgumi. Integrācijas veidnes ietvaros varat iestatīt integrācijas avotu programmā Finance and Operations projekta līgumam.

Laika un materiālu projekti un fiksētas cenas projekti tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance and Operations kā projekti. Veidnes integrācijas ietvaros varat iestatīt integrācijas avotu programmā Finance and Operations projektam.

Projekta līguma rindas tiek pārvaldītas programmā Project Service Automation, un tās tiek sinhronizētas ar programmu Finance and Operations kā projekta līguma norēķinu kārtulas. Ja rēķinu izrakstīšanas metode atšķiras no noklusējuma projekta tipa, sinhronizēšana atjaunina projekta tipu līguma rindas projektam un projektu grupai.

Projekta līguma rindas atskaites punkti tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance and Operations kā projekta līguma norēķinu kārtulas atskaites punkti.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Risinājums, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance and Operations

Lapā **Projekta līgumi** ir pieejams lauks **Projekta līguma ID**. Šis lauks ir iestatīts kā parasta un unikāla atslēga, lai nodrošinātu integrācijas atbalstu.

Kad tiek izveidots jauns projekta līgums un ja lauka **Projekta līguma ID** vērtība vēl nepastāv, to automātiski ģenerē, izmantojot numuru sēriju. Šī vērtība sastāv no **ORD**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes. Tālāk minēts piemērs: **ORD-01022-Z4M9Q0**.

Lapā **Projekti** ir pieejams lauks **Projekta numurs**. Šis lauks ir iestatīts kā parasta un unikāla atslēga, lai nodrošinātu integrācijas atbalstu.

Kad tiek izveidots jauns projekts un ja lauka **Projekta numurs** vērtība vēl nepastāv, to automātiski ģenerē, izmantojot numuru sēriju. Šī vērtība sastāv no **PRJ**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes. Tālāk minēts piemērs: **PRJ-01049-CCNID0**.

Izmantojot risinājumu, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance and Operations<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, atjaunināšanas skripts iestata lauku **Projekta līguma ID** esošajiem projekta līgumiem un lauku **Projekta numurs** esošajiem projektiem programmā Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

- Pirms projekta līgumu un projektu sinhronizēšanas ir jāveic kontu sinhronizēšana.
- Savienojumu kopā pievienojiet integrācijas atslēgas lauka kartēšanu vienumam **msdyn\_organizationalunits** uz **msdyn\_name \[Name\]**. Iespējams, projekts vispirms ir jāpievieno savienojumu kopai. Papildinformāciju skatiet rakstā [Datu integrēšana pakalpojumā Common Data Service programmām](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- Savienojumu kopā pievienojiet integrācijas atslēgas lauka kartēšanu vienumam **msdyn\_projects** uz **msdynce\_projectnumber \[Project Number\]**. Iespējams, projekts vispirms ir jāpievieno savienojumu kopai. Papildinformāciju skatiet rakstā [Datu integrēšana pakalpojumā Common Data Service programmām](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- Entītiju **SourceDataID** projekta līgumiem un projektiem var atjaunināt uz citu vērtību vai noņemt no kartējuma. Noklusējuma veidnes vērtība ir **Project Service Automation**.
- Kartējums **PaymentTerms** ir jāatjaunina, lai tas norādītu derīgus maksāšanas noteikumus programmā Finance and Operations. Varat arī noņemt kartējumu no projekta uzdevuma. Noklusējuma vērtību kartē ir norādītas demonstrācijas datu noklusējuma vērtības. Nākamajā tabulā ir parādītas vērtības programmā Project Service Automation.

    | Vērtība | apraksts   |
    |-------|---------------|
    | 1     | Neto 30        |
    | 2     | 2%10, neto 30 |
    | 3     | Neto 45        |
    | 4.     | Neto 60        |

## <a name="power-query"></a>Power Query

Ja ir izpildīti tālāk norādītie nosacījumi, datu filtrēšanai ir jāizmanto Microsoft Power Query programmai Excel.

- Programmā Microsoft Dynamics 365 for Sales ir izveidoti pārdošanas pasūtījumi.
- Jums ir vairākas organizācijas vienības programmā Project Service Automation, un šīs organizācijas vienības tiek kartētas uz vairākām juridiskajām personām programmā Finance and Operations.

Ja ir jāizmanto Power Query, ievērojiet tālāk minētos norādījumus.

- Veidnē “Projekti un līgumi” (no PSA uz Fin and Ops) ir noklusējuma filtrs, kas ietver tikai pārdošanas pasūtījumus, kuru tips ir **Darba vienums (msdyn\_ordertype = 192350001)**. Šis filtrs palīdz nodrošināt, ka projekta līgumi netiek izveidoti pārdošanas pasūtījumiem programmā Finance and Operations. Ja izveidojat savu veidni, ir jāpievieno šis filtrs.
- Ir jāizveido Power Query filtrs, kas ietver tikai līguma organizācijas, kuras jāsinhronizē ar integrācijas savienojumu kopas juridisko personu. Piemēram, projekta līgumi, kuri izveidoti ar Contoso ASV līguma organizācijas vienību, jāsinhronizē ar USSI juridisko personu, bet projekta līgumi, kuri izveidoti ar Contoso Global līguma organizācijas vienību, jāsinhronizē ar USMF juridisko personu. Ja šo filtru nepievienojat uzdevumu kartēšanai, visi projekta līgumi tiks sinhronizēti ar juridisko personu, kas ir definēta savienojumu kopai, neatkarīgi no līguma organizatoriskās vienības.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

> [!NOTE] 
> Lauki **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** un **AddressZipCode** nav iekļauti projekta līgumu noklusējuma kartējumā. Varat pievienot kartējumus, ja nepieciešams sinhronizēt šos datus attiecīgajiem projekta līgumiem.
>
> Lauki **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** un **ProjectType** nav iekļauti projektu noklusējuma kartējumā. Varat pievienot kartējumus, ja nepieciešams sinhronizēt šos datus attiecīgajiem projektiem.

Tālāk esošajos attēlos ir redzami piemēri veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda programmā Project Service Automation ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Finance and Operations.

[![Veidnes kartēšana](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Veidnes kartēšana](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Veidnes kartēšana](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Veidnes kartēšana](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)
