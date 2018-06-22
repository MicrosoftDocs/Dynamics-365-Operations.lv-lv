---
title: "Programmā Project Service Automation ietverto projekta faktisko vērtību tieša sinhronizēšana ar projekta integrācijas žurnālu grāmatošanai programmā Finance and Operations"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Project Service Automation ietverto projekta faktisko vērtību tiešai sinhronizēšanai ar programmu Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: lv-lv
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Programmā Project Service Automation ietverto projekta faktisko vērtību tieša sinhronizēšana ar projekta integrācijas žurnālu grāmatošanai programmā Finance and Operations

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Project Service Automation ietverto projekta faktisko vērtību tiešai sinhronizēšanai ar programmu Dynamics 365 for Finance and Operations.

Veidne sinhronizē programmā Project Service Automation ietvertās transakcijas ar sagatavošanas tabulu programmā Finance and Operations. Pēc tam, kad sinhronizācija ir pabeigta, jāveic importēšana no sagatavošanas tabulas integrācijas žurnālā.

> [!NOTE]
> Projekta faktisko vērtību integrācija ir pieejama programmas Dynamics 365 for Finance and Operations versijā 8.01.

> [!NOTE]
> Ja ievadāt PVN summas laika vai izdevumu transakcijās programmā Project Service Automation, ir jāinstalē Project Service Automation 7. atjauninājums. Ja šis atjauninājums nav instalēts, nodokļu faktiskās vērtības netiks saistītas ar attiecīgajām laika vai izdevumu faktiskajām vērtībām un netiks sinhronizētas ar programmu Finance and Operations. Lai iegūtu papildu informāciju, sazinieties ar atbalsta dienestu.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Datu plūsma programmas Project Service Automation sinhronizēšanai ar programmu Finance and Operations

Risinājums, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance and Operations, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance and Operations instancēs. Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo datu plūsmu par projekta faktiskajām vērtībām no programmas Project Service Automation uz programmu Finance and Operations.

Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance and Operations.

[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, Microsoft PowerApps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Project Service Automation ietverto projekta faktisko vērtību sinhronizēšanai ar programmu Finance and Operations tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

-  **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta faktiskās vērtības (no PSA uz Fin and Ops)

-  **Projekta uzdevumu nosaukums:** 
    - Faktiskās izmaksas 
    - TransactionConnections

## <a name="entity-set"></a>Elementu kopa

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| Faktiskās izmaksas                         | Integrācijas elements projekta faktiskajām summām                      |
| Transakciju savienojumi         | Integrēšanas elements projekta transakciju attiecībām    |

## <a name="entity-flow"></a>Elementu plūsma

Projekta faktiskās vērtības tiek pārvaldītas programmā Project Service Automation, un tās tiek sinhronizētas ar programmu Finance and Operations projekta integrācijas žurnālā. Uzskaite tiks izmantota, pamatojoties uz noklusējuma finanšu dimensijām un grāmatošanas iestatījumiem.

## <a name="preconditions"></a>Priekšnosacījumi

Pirms faktisko vērtību sinhronizācijas ir jākonfigurē programmas Project Service Automation integrācijas parametri un jāsinhronizē projektu, projekta uzdevumu un projekta izdevumu transakciju kategorijas.

## <a name="power-query"></a>Power Query

Ir jāizmanto Microsoft Power Query projekta faktisko vērtību veidnē, lai veiktu šādas darbības:
- Pārveidot programmas Project Service Automation **transakcijas veidu** par pareizo **transakcijas veidu** programmā Finance and Operations. Veidnē Projekta faktiskās vērtības (no PSA uz Fin and Ops) jau ir definēta šī pārveidošana.
- Pārveidot programmas Project Service Automation **norēķinu veidu** par pareizo **norēķinu veidu** programmā Finance and Operations. Veidnē Projekta faktiskās vērtības (no PSA uz Fin and Ops) jau ir definēta šī pārveidošana. Pēc tam norēķinu veids tiek kartēts uz **rindas rekvizītu**, pamatojoties uz konfigurāciju Dynamics 365 for Project Service Automation integrācijas parametru veidlapā.
- Filtrējiet noteiktas **Resursu organizācijas vienības**, kuras paredzēs sinhronizēt ar šo veidni.
- Ja **starpuzņēmumu laika vai starpuzņēmumu izdevumu faktiskās vērtības** tiks sinhronizētas ar programmu Finance and Operations, **līguma organizācijas vienība** ir jāpārveido par pareizo **juridisko personu** programmā Finance and Operations. Veidnē Projekta faktiskās vērtības (no PSA uz Fin and Ops) ir nosacījuma kolonna, kas definēta, pamatojoties uz demonstrācijas datiem. Ir jāatjaunina pēdējā ievietotā nosacījuma kolonna atbilstoši pareizajām juridiskajām personām. Pretējā gadījumā tas var izraisīt integrācijas kļūdu vai nepareizu faktisko vērtību transakciju importēšanu programmā Finance and Operations.
- Ja **starpuzņēmumu laika vai starpuzņēmumu izdevumu faktiskās vērtības** netiks sinhronizētas programmā Finance and Operations, ir jāizdzēš pēdējā ievietotā kolonna no veidnes. Pretējā gadījumā tas var izraisīt integrācijas kļūdu vai nepareizu faktisko vērtību transakciju importēšanu programmā Finance and Operations.

### <a name="contract-organizational-unit"></a>Līguma organizācijas vienība
Lai atjauninātu ievietoto nosacījuma kolonnu veidnē, noklikšķiniet uz bultiņas **Kartēt**, lai atvērtu kartēšanu. Atlasiet, lai atvērtu izvērstos vaicājumus un filtrēšanu.
- Ja izmantojat Microsoft noklusējuma veidni Projekta faktiskās vērtības (no PSA uz Fin and Ops), atlasiet pēdējo vienumu **Ievietotais nosacījums** sadaļā **Lietotie soļi**. Ierakstā **Funkcija** aizstājiet **USSI** ar vienuma **Juridiska persona** nosaukumu, kas jāizmanto integrācijai. Pievienojiet nepieciešamos papildu nosacījumus ierakstam **Funkcija** un atjauniniet nosacījumu **else** no **USMF** uz pareizo **Juridisko personu**.
- Ja veidojat jaunu veidni, ir jāpievieno šī kolonna, lai atbalstītu starpuzņēmumu laika un izdevumu vērtības. Atlasiet **Pievienot nosacījuma kolonnu** un piešķiriet kolonnai nosaukumu, piemēram, “LegalEntity”. Ievadiet kolonnas nosacījumu, kurš paredz, ka gadījumā, ja msdyn_contractorganizationalunitid.msdyn_name ir <organizational unit>, tad <enter the Legal entity>; pretējā gadījumā vērtība ir Null.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda programmā Project Service Automation ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Finance and Operations.

[![Veidnes kartēšana](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Veidnes kartēšana](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Importēt no sagatavošanas tabulas

Periodiskais process Importēt no sagatavošanas tabulas ir jāpalaiž pēc programmā Project Service Automation ietverto faktisko vērtību sinhronizēšanas ar programmu Finance and Operations. Šis process importēs projekta transakcijas no sagatavošanas tabulas Project Service Automation integrācijas žurnālā, kur tiks izmantota uzskaite un varēs grāmatot importētās transakcijas. Ieteicams palaist šo procesu pakešveida režīmā, un pēc izvēles tā palaišanu var iestatīt kā periodisku pakešapstrādi.

## <a name="update-actuals"></a>Faktisko vērtību atjaunināšana

Programmā Finance and Operations ietvertā grāmatoto projekta transakciju dokumenta numura un PVN sinhronizēšanai ar programmu Project Service Automation tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

-  **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta faktisko vērtību atjauninājums (no Fin and Ops uz PSA)
-  **Projekta uzdevumu nosaukums:** 
     - Faktiskās izmaksas 
     - TransactionConnections

## <a name="entity-set"></a>Elementu kopa

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| Integrācijas elements projekta faktiskajām summām                         | Faktiskās izmaksas                           |
| Integrēšanas elements projekta transakciju attiecībām       | Transakciju savienojumi           |

## <a name="entity-flow"></a>Elementu plūsma

Projekta faktiskās vērtības tiek pārvaldītas programmā Project Service Automation, un tās tiek sinhronizētas ar programmu Finance and Operations projekta integrācijas žurnālā. Pēc grāmatošanas programmā Finance and Operations faktiskās vērtības tiek atjauninātas programmā Project Service Automation ar dokumenta numuru no programmas Finance and Operations. Ja programmā Finance and Operations tika pievienots PVN, programmā Project Service Automation tiks izveidotas jaunas PVN faktiskās vērtības.

## <a name="power-query"></a>Power Query

Ir jāizmanto Microsoft Power Query projekta faktisko vērtību atjauninājuma veidnē, lai veiktu šādas darbības:
- Pārveidot programmas Finance and Operations **transakcijas veidu** par pareizo **transakcijas veidu** programmā Project Service Automation. Veidnē Projekta faktisko vērtību atjauninājums (no Fin and Ops uz PSA) jau ir definēta šī pārveidošana.
- Pārveidot programmas Finance and Operations **norēķinu veidu** par pareizo **norēķinu veidu** programmā Project Service Automation. Veidnē Projekta faktisko vērtību atjauninājums (no Fin and Ops uz PSA) jau ir definēta šī pārveidošana.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzami piemēri veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda programmā Finance and Operations ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Project Service Automation.

[![Veidnes kartēšana](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Veidnes kartēšana](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




