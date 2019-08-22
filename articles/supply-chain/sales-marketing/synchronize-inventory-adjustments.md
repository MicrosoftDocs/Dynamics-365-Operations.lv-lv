---
title: Programmā Field Service ietverto krājumu pārsūtīšanas un korekcijas darbību sinhronizēšana ar programmu Finance and Operations
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto krājumu korekciju un pārsūtīšanas darbību sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 145c9c06635aa6518fd1f76324a8bd6e4cc07d16
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835722"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto krājumu korekciju un pārsūtīšanas darbību sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi
Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu programmā Microsoft Dynamics 365 for Field Service ietverto krājumu korekciju un pārsūtīšanas darbību sinhronizēšanu ar programmu Microsoft Dynamics 365 for Finance and Operations.

**Veidnes līdzeklī Datu integrācija**
- Krājumu korekcija (no Field Service uz Fin and Ops)
- Krājumu pārsūtīšana (no Field Service uz Fin and Ops)

**Uzdevumi datu integrācijas projektos**
- Krājumu korekcijas
- Krājumu pārsūtīšana

## <a name="entity-set"></a>Elementu kopa
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS krājumu korekciju žurnālu virsraksti un rindas |
| msdyn_inventoryadjustmentproducts | CDS krājumu pārsūtīšanas žurnālu virsraksti un rindas   |

## <a name="entity-flow"></a>Elementu plūsma
Programmā Field Service veiktās krājumu korekcijas un pārsūtīšanas darbības tiks sinhronizētas ar programmu Finance and Operations pēc tam, kad vienumam **Grāmatošanas statuss** iestatījums tiek mainīts no **Izveidots** uz **Grāmatots**. Kad tas notiek, korekcijas vai pārsūtīšanas pasūtījums tiks slēgts un kļūs tikai lasāms. Tas nozīmē, ka korekcijas un pārsūtīšanas darbības var tikt grāmatotas programmā Finance and Operations, bet tās nevar modificēt. Programmā Finance and Operations var iestatīt pakešuzdevumu, lai automātiski grāmatotu korekcijas un pārsūtītu krājumu žurnālus, kuri ģenerēti integrācijas laikā. Skatiet tālāk norādītos priekšnosacījumus, lai iegūtu informāciju par to, kā iespējot pakešuzdevumu.

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM 
Entītijai **Prece** ir pievienots lauks **Krājumu uzskaites vienība**. Šis lauks ir nepieciešams, jo pārdošanas un krājumu uzskaites vienības ne vienmēr sakrīt programmā Finance and Operations, un noliktavas krājumiem programmā Finance and Operations ir nepieciešama krājumu uzskaites vienība.
Atlasot preci vienumam Krājumu korekcijas prece gan krājumu korekcijām, gan krājumu pārsūtīšanai, vienība tiks iegūta no krājumu preces vērtības. Ja vērtība tiek atrasta, laukā **Vienība** tiek fiksēts iestatījums Krājumu korekcijas prece.

Lauks **Grāmatošanas statuss** ir pievienots gan entītijai **Krājumu korekcija**, gan entītijai **Krājumu pārvietošana**. Šo lauku izmanto kā filtru, ja korekcija vai pārsūtīšana tiek nosūtīta uz programmu Finance and Operations. Šī lauka noklusējuma iestatījums ir Izveidots (1), taču tas netiek nosūtīts uz programmu Finance and Operations. Atjauninot vērtību uz Grāmatots (2), tas tiek sūtīts uz programmu Finance and Operations, bet pēc tam vairs nevarēsit mainīt korekciju un pārsūtīšanas darbību vai pievienot jaunas rindas.

Entītijai **Krājumu korekcijas prece** ir pievienots lauks **Numuru sērija**. Šis lauks nodrošina to, ka integrācijai ir unikāls numurs, tādējādi integrācija var izveidot un atjaunināt korekciju. Veidojot pirmo krājumu korekcijas preci, tiks izveidots jauns ieraksts entītijā **P2C automātiska numerācija**, lai uzturētu izmantoto numuru sēriju un prefiksu.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

### <a name="finance-and-operations"></a>Finance and Operations
Integrācijas krājumu žurnālus, kas ģenerēti integrācijas ietvaros, var automātiski grāmatot, izmantojot pakešuzdevumu. To iespējo šādi: **Krājumu vadība > Periodiskie uzdevumi > CDS integrācija > Grāmatot integrācijas krājumu žurnālus**.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a>Krājumu korekcija (no Field Service uz Fin and Ops): Krājumu korekcija

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a>Krājumu pārsūtīšana (no Field Service uz Fin and Ops): Krājumu pārsūtīšana

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSTrans1.png)](./media/FSTrans1.png)
