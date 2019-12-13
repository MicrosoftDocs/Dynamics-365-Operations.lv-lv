---
title: Projekta līgumu un projektu sinhronizēšana tieši no Project Service Automation uz Finance and Operations
description: Šajā tēmā ir aprakstīta veidne un pamata uzdevumi, kas tiek izmantoti, lai tiešā veidā sinhronizētu programmā Microsoft Dynamics 365 Project Service Automation ietvertos projekta līgumus un projektus ar programmu Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b44fc116f1dcaa1275b2262487ef9114bce639c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773858"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Projekta līgumu un projektu sinhronizēšana tieši no Project Service Automation uz Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta veidne un pamata uzdevumi, kas tiek izmantoti, lai tiešā veidā sinhronizētu programmā Dynamics 365 Project Service Automation ietvertos projekta līgumus un projektus ar programmu Dynamics 365 Finance.

> [!NOTE] 
> Ja lietojat Enterprise Edition versiju 7.3.0, ir jāinstalē KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation datu plūsma uz programmu Finance

> [!NOTE]
> Pirms varat izmantot risinājumu Project Service Automation integrācijai programmā Finance, ir jāiepazīst Dynamics 365 līdzeklis Datu integrācija.

Risinājums, lai veiktu integrēšanu no programmas Project Service Automation uz programmu Finance, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance instancēs. Integrācijas veidne, kas ir pieejama līdzeklī Datu integrācija, iespējo datu plūsmu par projekta līgumiem, projektiem, projekta līguma rindām un projekta līguma rindas atskaites punktiem no programmas Project Service Automation programmā Finance.

Nākamajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance.

[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, Microsoft Power Apps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Project Service Automation ietverto projekta līgumu un projektu sinhronizēšanai ar programmu Finance tiek izmantota tālāk norādītās veidnes un pamata uzdevumi.

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrēšana ar Dynamics 365 Project Service Automation v2. x
- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekti un līgumi (no PSA uz Fin and Ops)
- **Projekta uzdevumu nosaukums:**

    - Projekta līgumi (no PSA uz Fin and Ops)
    - Projekti (no PSA uz Fin and Ops)
    - Projekta līguma rindas (no PSA uz Fin and Ops)
    - Projekta līguma rindas atskaites punkti (no PSA uz Fin and Ops)
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrēšana ar Dynamics 365 Project Service Automation v3. x
Project Service Automation ir shēmas izmaiņas, kas ietekmē Project contract rindas atskaites punkta veidni un izmanto veidnes v2 versiju, lai integrētu Project Service Automation v3. x ar Dynamics 365.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekti un Līgumi (no PSA 3.x uz Fin and Ops) - v2
- **Projekta uzdevumu nosaukums:**

    - Projekta līgumi (no PSA uz Fin and Ops)
    - Projekti (no PSA uz Fin and Ops)
    - Projekta līguma rindas (no PSA uz Fin and Ops)
    - Projekta līguma rindas atskaites punkti (no PSA uz Fin and Ops)

Pirms projekta līgumu un projektu sinhronizēšanas ir jāveic kontu sinhronizēšana.

## <a name="entity-set"></a>Elementu kopa

| Project Service Automation       | Finansēt                                                |
|----------------------------------|--------------------------------------------------------|
| Pasūtījumi                           | Integrācijas elements projekta līgumam                |
| Projekti                         | Integrācijas elements projektam                         |
| Pasūtījuma rindas                      | Integrācijas elements projekta līguma rindai           |
| Projekta līguma rindas atskaites punkti | Integrācijas elements projekta līguma rindas atskaites punktam |

## <a name="entity-flow"></a>Elementu plūsma

Projekta līgumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance kā projekta līgumi. Integrācijas veidnes ietvaros varat iestatīt integrācijas avotu programmā Finance projekta līgumam.

Laika un materiālu projekti un fiksētas cenas projekti tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance kā projekti. Veidnes integrācijas ietvaros varat iestatīt integrācijas avotu programmā Finance projektam.

Projekta līguma rindas tiek pārvaldītas programmā Project Service Automation, un tās tiek sinhronizētas ar programmu Finance kā projekta līguma norēķinu kārtulas. Ja rēķinu izrakstīšanas metode atšķiras no noklusējuma projekta tipa, sinhronizēšana atjaunina projekta tipu līguma rindas projektam un projektu grupai.

Projekta līguma rindas atskaites punkti tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance kā projekta līguma norēķinu kārtulas atskaites punkti.

## <a name="project-service-automation-to-finance-integration-solution"></a>Risinājums, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance

Lapā **Projekta līgumi** ir pieejams lauks **Projekta līguma ID**. Šis lauks ir iestatīts kā parasta un unikāla atslēga, lai nodrošinātu integrācijas atbalstu.

Kad tiek izveidots jauns projekta līgums un ja lauka **Projekta līguma ID** vērtība vēl nepastāv, to automātiski ģenerē, izmantojot numuru sēriju. Šī vērtība sastāv no **ORD**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes. Tālāk minēts piemērs: **ORD-01022-Z4M9Q0**.

Lapā **Projekti** ir pieejams lauks **Projekta numurs**. Šis lauks ir iestatīts kā parasta un unikāla atslēga, lai nodrošinātu integrācijas atbalstu.

Kad tiek izveidots jauns projekts un ja lauka **Projekta numurs** vērtība vēl nepastāv, to automātiski ģenerē, izmantojot numuru sēriju. Šī vērtība sastāv no **PRJ**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes. Tālāk minēts piemērs: **PRJ-01049-CCNID0**.

Izmantojot risinājumu, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance, atjaunināšanas skripts iestata lauku **Projekta līguma ID** esošajiem projekta līgumiem un lauku **Projekta numurs** esošajiem projektiem programmā Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

- Pirms projekta līgumu un projektu sinhronizēšanas ir jāveic kontu sinhronizēšana.
- Savienojumu kopā pievienojiet integrācijas atslēgas lauka kartēšanu vienumam **msdyn\_organizationalunits** uz **msdyn\_name \[Name\]**. Iespējams, projekts vispirms ir jāpievieno savienojumu kopai. Papildinformāciju skatiet rakstā [Datu integrēšana pakalpojumā Common Data Service programmām](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Savienojumu kopā pievienojiet integrācijas atslēgas lauka kartēšanu vienumam **msdyn\_projects** uz **msdynce\_projectnumber \[Project Number\]**. Iespējams, projekts vispirms ir jāpievieno savienojumu kopai. Papildinformāciju skatiet rakstā [Datu integrēšana pakalpojumā Common Data Service programmām](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Entītiju **SourceDataID** projekta līgumiem un projektiem var atjaunināt uz citu vērtību vai noņemt no kartējuma. Noklusējuma veidnes vērtība ir **Project Service Automation**.
- Kartējums **PaymentTerms** ir jāatjaunina, lai tas norādītu derīgus maksāšanas noteikumus programmā Finance. Varat arī noņemt kartējumu no projekta uzdevuma. Noklusējuma vērtību kartē ir norādītas demonstrācijas datu noklusējuma vērtības. Nākamajā tabulā ir parādītas vērtības programmā Project Service Automation.

    | Vērtība | apraksts   |
    |-------|---------------|
    | 1     | Neto 30        |
    | 2     | 2% 10, neto 30 |
    | 3     | Neto 45        |
    | 4.     | Neto 60        |

## <a name="power-query"></a>Power Query

Ja ir izpildīti tālāk norādītie nosacījumi, datu filtrēšanai ir jāizmanto Microsoft Power Query programmai Excel.

- Jums ir pārdošanas pasūtījumi programmā Dynamics 365 Sales.
- Jums ir vairākas organizācijas vienības programmā Project Service Automation, un šīs organizācijas vienības tiek kartētas uz vairākām juridiskajām personām programmā Finance.

Ja ir jāizmanto Power Query, ievērojiet tālāk minētos norādījumus.

- Veidnē “Projekti un līgumi” (no PSA uz Fin and Ops) ir noklusējuma filtrs, kas ietver tikai pārdošanas pasūtījumus, kuru tips ir **Darba vienums (msdyn\_ordertype = 192350001)**. Šis filtrs palīdz nodrošināt, ka projekta līgumi netiek izveidoti pārdošanas pasūtījumiem programmā Finance. Ja izveidojat savu veidni, ir jāpievieno šis filtrs.
- Ir jāizveido Power Query filtrs, kas ietver tikai līguma organizācijas, kuras jāsinhronizē ar integrācijas savienojumu kopas juridisko personu. Piemēram, projekta līgumi, kuri izveidoti ar Contoso ASV līguma organizācijas vienību, jāsinhronizē ar USSI juridisko personu, bet projekta līgumi, kuri izveidoti ar Contoso Global līguma organizācijas vienību, jāsinhronizē ar USMF juridisko personu. Ja šo filtru nepievienojat uzdevumu kartēšanai, visi projekta līgumi tiks sinhronizēti ar juridisko personu, kas ir definēta savienojumu kopai, neatkarīgi no līguma organizatoriskās vienības.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

> [!NOTE] 
> Lauki **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** un **AddressZipCode** nav iekļauti projekta līgumu noklusējuma kartējumā. Varat pievienot kartējumus, ja nepieciešams sinhronizēt šos datus attiecīgajiem projekta līgumiem.
>
> Lauki **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** un **ProjectType** nav iekļauti projektu noklusējuma kartējumā. Varat pievienot kartējumus, ja nepieciešams sinhronizēt šos datus attiecīgajiem projektiem.

Tālāk esošajos attēlos ir redzami piemēri veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda lauku informāciju, kas tiks sinhronizēta no programmas Project Service Automation uz programmu Finance.

[![Veidnes kartēšana](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Veidnes kartēšana](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Veidnes kartēšana](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Veidnes kartēšana](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Projekta līguma rindas atskaites punkta kartēšana Projektos un Līgumos (PSA 3. x līdz Dynamics) - v2 veidne:

[![Veidnes kartēšana](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
