---
title: Programmā Project Service Automation ietverto projekta faktisko vērtību tieša sinhronizēšana ar projekta integrācijas žurnālu grāmatošanai programmā Finance and Operations
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 Project Service Automation ietverto projekta faktisko summu tiešai sinhronizēšanai ar programmu Finance and Operations.
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
ms.openlocfilehash: 302ac0f456dd8a24dc02948ee657e359f5a9c844
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770339"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Programmā Project Service Automation ietverto projekta faktisko vērtību tieša sinhronizēšana ar projekta integrācijas žurnālu grāmatošanai programmā Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Project Service Automation ietverto projekta faktisko summu tiešai sinhronizēšanai ar programmu Dynamics 365 Finance.

Veidne sinhronizē programmā Project Service Automation ietvertās transakcijas ar izstādīšanas tabulu programmā Finance. Kad sinhronizācija ir pabeigta, jums ir **jāimportē** dati no izstādīšanas tabulas uz integrācijas žurnālu.

> [!NOTE]
> - Projekta faktisko vērtību integrācija ir pieejama versijā 8.0.1 vai jaunākās versijās.
> - Ja lietojat Enterprise Edition versiju 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un faktiskās vērtības, kā arī konfigurēt funkcionalitātes bloķēšanu. Ja ir nepieciešams atiestatīt uzskaites sadali, ieteicams arī instalēt KB 4131710.
> - Ja izmantojat versiju 7.3.0 un pārceļat maksu transakcijas no programmas Project Service Automation, ir jāinstalē KB 4345320, lai šīs maksas ietvertu projekta rēķinā.
> - Ja ievadāt PVN summas laika vai izdevumu transakcijās programmā Project Service Automation, ir jāinstalē Project Service Automation 7. atjauninājums. Pretējā gadījumā nodokļu faktiskās vērtības netiks saistītas ar attiecīgajām laika vai izdevumu faktiskajām vērtībām un netiks sinhronizētas ar programmu Finance. Lai iegūtu papildinformāciju, sazinieties ar atbalsta dienestu.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation datu plūsma uz programmu Finance

Risinājums, lai veiktu integrēšanu no programmas Project Service Automation uz programmu Finance, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance instancēs. Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo datu plūsmu par projekta faktiskajām vērtībām no programmas Project Service Automation uz programmu Finance.

Nākamajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance.

[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projekta faktiskās vērtības no Project Service Automation

### <a name="template-and-tasks"></a>Veidne un uzdevumi

Lai piekļūtu pieejamajām veidnēm, Microsoft Power Apps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Project Service Automation ietverto projekta faktisko vērtību sinhronizēšanai ar programmu Finance tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta faktiskās vērtības (no PSA uz Fin and Ops)
- **Projekta uzdevumu nosaukums:**

    - Faktiskās izmaksas
    - TransactionConnections

### <a name="entity-set"></a>Elementu kopa

| Project Service Automation | Finansēt                                   |
|----------------------------|----------------------------------------------------------|
| Faktiskās izmaksas                    | Integrācijas elements projekta faktiskajām summām                   |
| Transakciju savienojumi    | Integrēšanas elements projekta transakciju attiecībām |

### <a name="entity-flow"></a>Elementu plūsma

Projekta faktiskās vērtības tiek pārvaldītas programmā Project Service Automation, un tās tiek sinhronizētas ar projekta integrācijas žurnālu programmā Finance. Uzskaite tiks lietota, pamatojoties uz noklusējuma finanšu dimensijām un grāmatošanas iestatījumiem.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms faktisko vērtību sinhronizācijas ir jākonfigurē programmas Project Service Automation integrācijas parametri un jāsinhronizē projektu, projekta uzdevumu un projekta izdevumu transakciju kategorijas.

### <a name="power-query"></a>Power Query

Projekta faktisko vērtību veidnē jums ir jāizmanto pievienojumprogramma Microsoft Power Query programmai Excel, lai izpildītu tālāk norādītos uzdevumus.

- Pārveidojiet Project Service Automation transakcijas veidu par pareizo Finance transakcijas veidu. Šī pārveidošana jau ir definēta veidnē Projekta faktiskās vērtības (no PSA uz Fin and Ops).
- Pārveidojiet Project Service Automation norēķinu veidu par pareizo Finance norēķinu veidu. Šī pārveidošana jau ir definēta veidnē Projekta faktiskās vērtības (no PSA uz Fin and Ops). Pēc tam norēķinu veids tiek kartēts uz rindas rekvizītu, pamatojoties uz lapā **Project Service Automation integrācijas parametri** esošo konfigurāciju.
- Filtrējiet noteiktas resursu organizācijas vienības, kuras ir jāsinhronizē ar šo veidni.
- Ja starpuzņēmumu laika vai starpuzņēmumu izdevumu faktiskās vērtības tiks sinhronizētas ar programmu Finance, līguma organizācijas vienība ir jāpārveido par pareizo juridisko personu programmā Finance. Veidnē Projekta faktiskās vērtības (no PSA uz Fin and Ops) ir nosacījuma kolonna, kas definēta, pamatojoties uz demonstrācijas datiem. Pēdējā ievietotā nosacījuma kolonna ir jāatjaunina uz pareizajām juridiskajām personām. Pretējā gadījumā var rasties integrācijas kļūda vai arī programmā Finance var tikt importētas nepareizas faktisko vērtību transakcijas.
- Ja starpuzņēmumu laika vai starpuzņēmumu izdevumu faktiskās vērtības netiks sinhronizētas programmā Finance, pēdējā ievietotā nosacījuma kolonna ir jāizdzēš no veidnes. Pretējā gadījumā var rasties integrācijas kļūda vai arī programmā Finance var tikt importētas nepareizas faktisko vērtību transakcijas.

#### <a name="contract-organizational-unit"></a>Līguma organizācijas vienība
Lai atjauninātu ievietoto nosacījuma kolonnu veidnē, noklikšķiniet uz bultiņas **Kartēt**, lai atvērtu kartējumu. Atlasiet saiti **Paplašinātais vaicājums un filtrēšana**, lai atvērtu Power Query.

- Ja izmantojat noklusējuma veidni Projekta faktiskās vērtības (no PSA uz Fin and Ops), Power Query sadaļā **Lietotās darbības** atlasiet pēdējo vienumu **Ievietotais nosacījums**. Ierakstā **Funkcija** aizstājiet **USSI** ar integrācijā izmantojamās juridiskās personas nosaukumu. Ierakstam **Funkcija** pievienojiet nepieciešamos papildu nosacījumus un atjauniniet nosacījumu **else** no **USMF** uz pareizo juridisko personu.
- Ja veidojat jaunu veidni, ir jāpievieno šī kolonna, lai atbalstītu starpuzņēmumu laika un izdevumu vērtības. Atlasiet vienumu **Pievienot nosacījuma kolonnu** un ievadiet kolonnas nosaukumu, piemēram, **LegalEntity**. Ievadiet kolonnas nosacījumu, kurš paredz, ka gadījumā, ja **msdyn\_contractorganizationalunitid.msdyn\_name** ir \<organizational unit\>, tad \<enter the legal entity\>; pretējā gadījumā vērtība ir Null.

### <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir sniegts piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda lauku informāciju, kas tiks sinhronizēta no programmas Project Service Automation uz programmu Finance.

[![Veidnes kartēšana](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Veidnes kartēšana](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importēšana no izstādīšanas tabulas pēc integrācijas no programmas Project Service Automation

Periodiskais process Importēt no izstādīšanas tabulas ir jāpalaiž pēc programmā Project Service Automation ietverto faktisko vērtību sinhronizēšanas ar programmu Finance. Šis process importēs projekta transakcijas no sagatavošanas tabulas Project Service Automation integrācijas žurnālā, kur tiks izmantota uzskaite un varēs grāmatot importētās transakcijas. Šo procesu ir ieteicams palaist pakešveida režīmā, un tā palaišanu pēc izvēles var iestatīt kā periodisku pakešapstrādi.

## <a name="update-actuals-from-finance"></a>Atjaunināt faktiskās vērtības no Finance

### <a name="template-and-tasks"></a>Veidne un uzdevumi

Programmā Finance ietvertā grāmatoto projekta transakciju dokumenta numura un PVN sinhronizēšanai ar programmu Project Service Automation tiek izmantota tālāk norādītā veidne un pamata uzdevumi.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta faktisko vērtību atjauninājums (no Fin and Ops uz PSA)
- **Projekta uzdevumu nosaukums:**

    - Faktiskās izmaksas 
    - TransactionConnections

### <a name="entity-set"></a>Elementu kopa

| Finansēt                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integrācijas elements projekta faktiskajām summām                   | Faktiskās izmaksas                    |
| Integrēšanas elements projekta transakciju attiecībām | Transakciju savienojumi    |

### <a name="entity-flow"></a>Elementu plūsma

Projekta faktiskās vērtības tiek pārvaldītas programmā Project Service Automation, un tās tiek sinhronizētas ar projekta integrācijas žurnālu programmā Finance. Pēc faktisko vērtību grāmatošanas programmā Finance and Operations tās tiek atjauninātas programmā Project Service Automation ar dokumenta numuru no programmas Finance. Ja programmā Finance tika pievienots PVN, programmā Project Service Automation tiek izveidotas jaunas PVN faktiskās vērtības.

### <a name="power-query"></a>Power Query

Projekta faktisko vērtību atjauninājuma veidnē jums ir jāizmanto Power Query, lai izpildītu tālāk norādītos uzdevumus.

- Pārveidojiet Finance transakcijas veidu par pareizo Project Service Automation transakcijas veidu. Šī pārveidošana jau ir definēta veidnē Projekta faktisko vērtību atjauninājums (no Fin Ops uz PSA).
- Pārveidojiet Finance norēķinu veidu par pareizo Project Service Automation norēķinu veidu. Šī pārveidošana jau ir definēta veidnē Projekta faktisko vērtību atjauninājums (no Fin Ops uz PSA).

### <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzami piemēri veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda programmā Finance ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Project Service Automation.

[![Veidnes kartēšana](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Veidnes kartēšana](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
