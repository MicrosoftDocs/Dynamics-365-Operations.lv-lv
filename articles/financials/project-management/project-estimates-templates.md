---
title: "Programmā Project Service Automation ietverto projekta novērtējumu tieša sinhronizēšana ar projekta prognozēm programmā Finance and Operations"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Project Service Automation ietverto projekta stundu novērtējumu un projekta izdevumu novērtējumu tiešai sinhronizēšanai ar programmu Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: lv-lv
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Programmā Project Service Automation ietverto projekta novērtējumu tieša sinhronizēšana ar projekta prognozēm programmā Finance and Operations

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Project Service Automation ietverto projekta stundu novērtējumu un projekta izdevumu novērtējumu tiešai sinhronizēšanai ar programmu Dynamics 365 for Finance and Operations.

> [!NOTE]
> Projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana ir pieejama programmas Dynamics 365 for Finance and Operations versijā 8.0.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Datu plūsma programmas Project Service Automation sinhronizēšanai ar programmu Finance and Operations

Risinājums, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance and Operations, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance and Operations instancēs. Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo datu plūsmu par projekta stundu novērtējumiem un projekta izdevumu novērtējumiem no programmas Project Service Automation uz programmu Finance and Operations.

Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance and Operations.

[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, Microsoft PowerApps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Project Service Automation ietverto projekta stundu novērtējumu sinhronizēšanai ar programmu Finance and Operations tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

-  **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta stundu novērtējumi (no PSA uz Fin and Ops)

-  **Projekta uzdevumu nosaukums:** 
    - Transakciju attiecības 
    - Izdevumu novērtējumi

## <a name="entity-set"></a>Elementu kopa

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| Projekta uzdevumi                   | Integrēšanas elements projekta stundu novērtējumiem   |

## <a name="entity-flow"></a>Elementu plūsma

Projekta stundu novērtējumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance and Operations kā projekta stundu prognozes.

## <a name="preconditions"></a>Priekšnosacījumi

Pirms projekta stundu novērtējumu sinhronizēšanas ir jāsinhronizē projektu, projekta uzdevumu un projekta izdevumu transakciju kategorijas.

## <a name="power-query"></a>Power Query

Ir jāizmanto Microsoft Power Query projekta stundu novērtējumu veidnē, lai veiktu šādas darbības:
- Iestatīt **Budžeta modeļa ID**, kas tiks izmantots, kad integrācija izveido jaunas stundu prognozes.
- Filtrēt visus tādus resursu ierakstus uzdevumā, kuriem nevarēs veikt integrēšanu stundu prognozēs.
- Filtrēt visas tukšo transakcijas kategoriju rindas. Pretējā gadījumā stundu prognozes var būt nepareizas.

### <a name="forecast-model-id"></a>Budžeta modeļa ID
Lai atjauninātu noklusējuma budžeta modeļa ID veidnē, noklikšķiniet uz bultiņas **Kartēt**, lai atvērtu kartēšanu. Atlasiet, lai atvērtu izvērstos vaicājumus un filtrēšanu.
- Ja izmantojat Microsoft noklusējuma veidni Projekta stundu novērtējumi (no PSA uz Fin and Ops), atlasiet vienumu **Ievietotais nosacījums** sadaļā **Lietotie soļi**. Ierakstā **Funkcija** aizstājiet **O_forecast** ar vienuma **Budžeta modeļa ID** nosaukumu, kas jāizmanto integrācijai. Noklusējuma veidnei ir budžeta modeļa ID no demonstrācijas datiem.
- Ja veidojat jaunu veidni, ir jāpievieno šī kolonna. Atlasiet **Pievienot nosacījuma kolonnu** un piešķiriet kolonnai nosaukumu, piemēram, “ModelID”. Ievadiet kolonnas nosacījumu, kurš paredz, ka gadījumā, ja projekta uzdevuma vērtība nav Null, tad <enter the forecast model ID>; pretējā gadījumā vērtība ir Null.

### <a name="filter-out-resource-specific-records"></a>Resursu ierakstu filtrēšana
Veidnē Projekta stundu novērtējumi (no PSA uz Fin and Ops) ir noklusējuma filtrs, kas noņem visus resursu ierakstus. Ja izveidojat savu veidni, ir jāpievieno šis filtrs. Izvērsto vaicājumu un filtrēšanas veidlapā atlasiet filtrēšanu kolonnai **msdyn_islinetask**, lai tiktu iekļauti tikai ieraksti ar vērtību **Aplams**.

### <a name="filter-out-empty-transaction-category-rows"></a>Tukšo transakcijas kategoriju rindu filtrēšana
Ir jāpievieno filtrs, lai noņemtu visas rindas ar tukšām transakciju kategorijām. Tas ir vajadzīgs neatkarīgi no tā, vai izmantojat noklusējuma veidni vai izveidojat savu veidni. Šis filtrs noņems kopsavilkuma rindas no programmas Project Service Automation, kuras var izraisīt to, ka stundu prognozes programmā Finance and Operations nebūs pareizas. Izvērsto vaicājumu un filtrēšanas veidlapā atlasiet Null ierakstu izfiltrēšanu kolonnā **msdyn_transactioncategory_value**.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda programmā Project Service Automation ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Finance and Operations.

[![Veidnes kartēšana](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

Programmā Project Service Automation ietverto projekta izdevumu novērtējumu sinhronizēšanai ar programmu Finance and Operations tiek izmantota tālāk norādītā veidne un pamata uzdevums.

-  **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu novērtējumi (no PSA uz Fin and Ops)
-  **Projekta uzdevumu nosaukums:** 
     - Transakciju attiecības 
     - Izdevumu novērtējumi

## <a name="entity-set"></a>Elementu kopa

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| Transakciju savienojumi         | Integrēšanas elements projekta transakciju attiecībām.   |
| Novērtēšanas rindas                  | Integrēšanas elements projekta izdevumu prognozēm.           |

## <a name="entity-flow"></a>Elementu plūsma

Projekta izdevumu novērtējumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance and Operations kā projekta izdevumu prognozes.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms projekta izdevumu novērtējumu sinhronizēšanas ir jāsinhronizē projektu, projekta uzdevumu un projekta izdevumu transakciju kategorijas.

## <a name="power-query"></a>Power Query

Ir jāizmanto Microsoft Power Query projekta izdevumu novērtējumu veidnē, lai veiktu šādas darbības:
- Filtrēt, lai iekļautu tikai izdevumu novērtējumu rindas ierakstus.
- Iestatīt **Budžeta modeļa ID**, kas tiks izmantots, kad integrācija izveido jaunas stundu prognozes.
- Pārveidot norēķinu veidus.
- Pārveidot transakciju veidus.

### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrēšana, lai iekļautu tikai izdevumu novērtējumu rindas
Veidnē Projekta izdevumu novērtējumi (no PSA uz Fin and Ops) ir noklusējuma filtrs, lai integrācijā iekļautu tikai izdevumu rindas. Ja izveidojat savu veidni, ir jāpievieno šis filtrs. Atlasiet uzdevumu Transakciju attiecības un noklikšķiniet uz bultiņas **Kartēt**. Atlasiet **Izvērsts vaicājums un filtrēšana**. Filtrējiet kolonnu **msdyn_transactiontype1**, lai iekļautu tikai **msdyn_estimateline**.

### <a name="forecast-model-id"></a>Budžeta modeļa ID
Lai atjauninātu noklusējuma budžeta modeļa ID veidnē uzdevumam Izdevumu novērtējumi, noklikšķiniet uz bultiņas **Kartēt**, lai atvērtu kartēšanu. Atlasiet, lai atvērtu izvērstos vaicājumus un filtrēšanu.
- Ja izmantojat Microsoft noklusējuma veidni Projekta izdevumu novērtējumi (no PSA uz Fin and Ops), atlasiet pirmo vienumu **Ievietotais nosacījums** sadaļā **Lietotie soļi**. Ierakstā **Funkcija** aizstājiet **O_forecast** ar vienuma **Budžeta modeļa ID** nosaukumu, kas jāizmanto integrācijai. Noklusējuma veidnei ir budžeta modeļa ID no demonstrācijas datiem.
- Ja veidojat jaunu veidni, ir jāpievieno šī kolonna. Atlasiet **Pievienot nosacījuma kolonnu** un piešķiriet kolonnai nosaukumu, piemēram, “ModelID”. Ievadiet kolonnas nosacījumu, kurš paredz, ka gadījumā, ja Novērtēšanas rindas ID vērtība nav Null, tad < ievadiet budžeta modeļa ID >; pretējā gadījumā vērtība ir Null.

### <a name="transform-the-billing-types"></a>Norēķinu veidu pārveidošana
Veidnei Projekta izdevumu novērtējumi (no PSA uz Fin and Ops) pievieno nosacījuma kolonnu, lai pārveidotu norēķinu veidus, kas saņemti no programmas Project Service Automation integrācijas laikā.
- Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna. Izvērsto vaicājumu un filtrēšanas veidlapā atlasiet **Pievienot nosacījuma kolonnu**. Piešķiriet kolonnai nosaukumu, piemēram “BillingType”. Jāievada šāds nosacījums:

    “If **msdyn_billingtype** = 192350000, then **NonChargeable** else if **msdyn_billingtype** = 192350001, then **Chargeable** else if **msdyn_billingtype** = 192350002, then **Complimentary** else **NotAvailable**”

### <a name="transform-the-transaction-types"></a>Transakciju veidu pārveidošana
Veidnei Projekta izdevumu novērtējumi (no PSA uz Fin and Ops) pievieno nosacījuma kolonnu, lai pārveidotu transakciju veidus, kas saņemti no programmas Project Service Automation integrācijas laikā.
- Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna. Izvērsto vaicājumu un filtrēšanas veidlapā atlasiet **Pievienot nosacījuma kolonnu**. Piešķiriet kolonnai nosaukumu, piemēram “TransactionType”. Jāievada šāds nosacījums: “If **msdyn_transactiontypecode** = 192350000, then **Cost** else if **msdyn_transactiontypecode** = 192350005, then **Sales** else **null**”

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzami piemēri veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda programmā Project Service Automation ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Finance and Operations.

[![Veidnes kartēšana](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Veidnes kartēšana](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




