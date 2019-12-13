---
title: Projekta novērtējumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai tiešā veidā sinhronizētu programmā Dynamics 365 Project Service Automation ietvertos projekta stundu novērtējumus un projekta izdevumu prognozes ar programmu Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
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
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770293"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Projekta novērtējumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai tiešā veidā sinhronizētu programmā Dynamics 365 Project Service Automation ietvertos projekta stundu novērtējumus un projekta izdevumu prognozes ar programmu Dynamics 365 Finance.

> [!NOTE]
> - Versijā 8.0 ir pieejama projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana.
> - Faktisko vērtību integrācija ir pieejama versijā 8.0.1 vai jaunākās versijās.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation datu plūsma uz programmu Finance

Risinājums, lai veiktu integrēšanu no programmas Project Service Automation uz programmu Finance, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance instancēs. Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo datu plūsmu par projekta stundu novērtējumiem un projekta izdevumu novērtējumiem no programmas Project Service Automation uz programmu Finance.

Nākamajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance.

[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projekta stundu novērtējumi

### <a name="template-and-tasks"></a>Veidne un uzdevumi

Lai piekļūtu pieejamajām veidnēm, Microsoft Power Apps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Project Service Automation ietverto projekta stundu novērtējumu sinhronizēšanai ar programmu Finance tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta stundu novērtējumi (no PSA uz Fin and Ops)
- **Projekta uzdevumu nosaukums:**

    - Transakciju attiecības
    - Izdevumu novērtējumi

### <a name="entity-set"></a>Elementu kopa

| Project Service Automation | Finansēt                                       |
|----------------------------|-----------------------------------------------|
| Projekta uzdevumi              | Integrēšanas elements projekta stundu novērtējumiem |

### <a name="entity-flow"></a>Elementu plūsma

Projekta stundu novērtējumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance kā projekta stundu prognozes.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms projekta stundu novērtējumu sinhronizēšanas ir jāsinhronizē projektu, projekta uzdevumu un projekta izdevumu transakciju kategorijas.

### <a name="power-query"></a>Power Query

Projekta stundu novērtējumu veidnē jums ir jāizmanto pievienojumprogramma Microsoft Power Query programmai Excel, lai izpildītu tālāk norādītos uzdevumus.

- Iestatīt noklusējuma prognozes modeļa ID, kas tiks izmantots, kad integrācija izveido jaunus stundu novērtējumus.
- Izfiltrēt uzdevumā visus resursiem raksturīgos ierakstus, kuriem nevarēs veikt integrēšanu stundu novērtējumos.
- Filtrēt visas tukšo transakcijas kategoriju rindas. Ja šis uzdevums netiek izpildīts, stundu prognozes var būt nepareizas.

#### <a name="set-the-default-forecast-model-id"></a>Noklusējuma prognozes modeļa ID iestatīšana

Lai atjauninātu noklusējuma budžeta modeļa ID veidnē, noklikšķiniet uz bultiņas **Kartēt**, lai atvērtu kartēšanu. Pēc tam atlasiet saiti **Paplašinātais vaicājums un filtrēšana**.

- Ja izmantojat noklusējuma veidni “Projekta stundu novērtējumi” (no PSA uz Fin and Ops), atlasiet vienumu **Ievietotais nosacījums** sarakstā **Izmantotās darbības**. Ierakstā **Funkcija** uzrakstu **O\_forecast** aizstājiet ar prognozes modeļa ID nosaukumu, kas ir jāizmanto integrācijai. Noklusējuma veidnei ir budžeta modeļa ID no demonstrācijas datiem.
- Ja veidojat jaunu veidni, ir jāpievieno šī kolonna. Pievienojumprogrammā Power Query atlasiet **Pievienot nosacījuma kolonnu** un ievadiet nosaukumu jaunajai kolonnai, piemēram, **ModelID**. Ievadiet nosacījumu šai kolonnai, kurš paredz, ka gadījumā, ja vērtība “Projekta uzdevums” nav Null, tad \<ievadīt prognozes modeļa ID\>; pretējā gadījumā vērtība ir Null.

#### <a name="filter-out-resource-specific-records"></a>Resursam raksturīgo ierakstu izfiltrēšana

Veidnei “Projekta stundu novērtējumi” (no PSA uz Fin and Ops) ir noklusējuma filtrs, kas noņem visus resursam raksturīgos ierakstus. Ja izveidojat savu veidni, ir jāpievieno šis filtrs. Atlasiet saiti **Paplašinātais vaicājums un filtrēšana**, lai filtrētu pēc kolonnas **msdyn\_islinetask**, tādējādi ietverot tikai ierakstus **False** (Aplams).

#### <a name="filter-out-empty-transaction-category-rows"></a>Tukšo transakcijas kategoriju rindu filtrēšana

Ir jāpievieno filtrs, lai noņemtu visas rindas, kurās ir tukšas transakciju kategorijas. Šis uzdevums ir jāveic neatkarīgi no tā, vai izmantojat noklusējuma veidni, vai izveidojat pats savu veidni. Šis filtrs no Project Service Automation noņem visas kopsavilkuma rindas, kuras varētu izraisīt to, ka stundu prognozes programmā Finance ir nepareizas. Atlasiet saiti **Paplašinātais vaicājums un filtrēšana**, lai izfiltrētu Null ierakstus kolonnā **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda lauku informāciju, kas tiks sinhronizēta no programmas Project Service Automation uz programmu Finance.

[![Veidnes kartēšana](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projekta izdevumu novērtējumi

### <a name="template-and-tasks"></a>Veidne un uzdevumi

Programmā Project Service Automation ietverto projekta izdevumu novērtējumu sinhronizēšanai ar programmu Finance tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu novērtējumi (no PSA uz Fin and Ops)
- **Projekta uzdevumu nosaukums:**

    - Transakciju attiecības 
    - Izdevumu novērtējumi

### <a name="entity-set"></a>Elementu kopa

| Project Service Automation | Finansēt                                                  |
|----------------------------|----------------------------------------------------------|
| Transakciju savienojumi    | Integrēšanas elements projekta transakciju attiecībām |
| Novērtēšanas rindas             | Integrēšanas elements projekta izdevumu prognozēm         |

### <a name="entity-flow"></a>Elementu plūsma

Projekta izdevumu novērtējumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance kā projekta izdevumu prognozes.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms projekta izdevumu novērtējumu sinhronizēšanas ir jāsinhronizē projektu, projekta uzdevumu un projekta izdevumu transakciju kategorijas.

### <a name="power-query"></a>Power Query

Projekta izdevumu novērtējumu veidnē ir jāizmanto Power Query, lai izpildītu tālāk norādītos uzdevumus.

- Filtrēt, lai ietvertu tikai izdevumu novērtējumu rindu ierakstus.
- Iestatīt noklusējuma prognozes modeļa ID, kas tiks izmantots, kad integrācija izveido jaunus stundu novērtējumus.
- Pārveidot norēķinu veidus.
- Pārveidot transakciju veidus.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrēšana, lai iekļautu tikai izdevumu novērtējumu rindas

Veidnē “Projekta izdevumu novērtējumi” (no PSA uz Fin and Ops) ir noklusējuma filtrs, kurš integrācijā ietver tikai izdevumu rindas. Ja izveidojat savu veidni, ir jāpievieno šis filtrs. Atlasiet uzdevumu **Transakciju attiecības** un pēc tam noklikšķiniet uz bultiņas **Kartēt**, lai atvērtu kartēšanu. Atlasiet saiti **Paplašinātais vaicājums un filtrēšana**. Filtrējiet kolonnu **msdyn\_transactiontype1**, lai tajā būtu tikai **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Noklusējuma prognozes modeļa ID iestatīšana

Lai veidnē atjauninātu noklusējuma prognozes modeļa ID, atlasiet uzdevumu **Izdevumu novērtējumi** un pēc tam noklikšķiniet uz bultiņas **Kartēt**, lai atvērtu kartēšanu. Atlasiet saiti **Paplašinātais vaicājums un filtrēšana**.

- Ja izmantojat noklusējuma veidni “Projekta izdevumu novērtējumi” (no PSA uz Fin and Ops), pievienojumprogrammā Power Query atlasiet pirmo vienumu **Ievietotais nosacījums** no sadaļas **Izmantotās darbības**. Ierakstā **Funkcija** uzrakstu **O\_forecast** aizstājiet ar prognozes modeļa ID nosaukumu, kas ir jāizmanto integrācijai. Noklusējuma veidnei ir budžeta modeļa ID no demonstrācijas datiem.
- Ja veidojat jaunu veidni, ir jāpievieno šī kolonna. Pievienojumprogrammā Power Query atlasiet **Pievienot nosacījuma kolonnu** un ievadiet nosaukumu jaunajai kolonnai, piemēram, **ModelID**. Ievadiet nosacījumu šai kolonnai, kurš paredz, ka gadījumā, ja Novērtējuma rindas ID vērtība nav Null, tad \<ievadīt prognozes modeļa ID\>; pretējā gadījumā vērtība ir Null.

#### <a name="transform-the-billing-types"></a>Norēķinu veidu pārveidošana

Veidnē “Projekta izdevumu novērtējumi” (no PSA uz Fin and Ops) ir nosacījuma kolonna, kas tiek izmantota, lai pārveidotu norēķinu tipus, kuri integrācijas laikā ir saņemti no Project Service Automation. Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna. Atlasiet saiti **Paplašinātais vaicājums un filtrēšana** un pēc tam atlasiet **Pievienot nosacījuma kolonnu**. Ievadiet jaunās kolonnas nosaukumu, piemēram, **BillingType**. Pēc tam ievadiet tālāk norādīto nosacījumu.

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transakciju veidu pārveidošana

Veidnē “Projekta izdevumu novērtējumi” (no PSA uz Fin and Ops) ir nosacījuma kolonna, kas tiek izmantota, lai pārveidotu transakciju tipus, kuri integrācijas laikā ir saņemti no Project Service Automation. Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna. Atlasiet saiti **Paplašinātais vaicājums un filtrēšana** un pēc tam atlasiet **Pievienot nosacījuma kolonnu**. Ievadiet nosaukumu jaunajai kolonnai, piemēram, **TransactionType**. Pēc tam ievadiet tālāk norādīto nosacījumu.

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzami piemēri veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda lauku informāciju, kas tiks sinhronizēta no programmas Project Service Automation uz programmu Finance.

[![Veidnes kartēšana](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Veidnes kartēšana](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
