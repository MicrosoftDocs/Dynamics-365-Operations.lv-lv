---
title: Programmā Field Service ietverto krājumu pārsūtīšanas un korekcijas darbību sinhronizēšana ar programmatūru Supply Chain Management
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto krājumu korekciju un pārsūtīšanas darbību sinhronizēšanai ar programmu Dynamics 365 Field Service.
author: Henrikan
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: cfa7f617cbc4cd75d669972b35f8d33ba3cbcc56
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061683"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Programmā Field Service ietverto krājumu pārsūtīšanas un korekcijas darbību sinhronizēšana ar programmatūru Supply Chain Management

[!include[banner](../includes/banner.md)]



Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto krājumu korekciju un pārsūtīšanas darbību sinhronizēšanai ar programmu Dynamics 365 Field Service.

[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi
Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai sinhronizētu krājumu korekciju un pārsūtīšanu no programmas Field Service uz Supply Chain Management.

**Veidnes līdzeklī Datu integrācija**
- Krājumu korekcija (no Field Service uz Supply Chain Management)
- Krājumu pārsūtījumi (no Field Service uz Supply Chain Management)

**Uzdevumi datu integrācijas projektos**
- Krājumu korekcijas
- Krājumu pārsūtīšana

## <a name="table-set"></a>Tabulu kopa
| Field Service                     | Supply Chain Management                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts | Dataverse Krājumu korekciju žurnālu virsraksti un rindas |
| msdyn_inventoryadjustmentproducts | Dataverse Krājumu pārsūtīšanas žurnālu virsraksti un rindas   |

## <a name="table-flow"></a>Tabulu plūsma
Programmā Field Service veiktās krājumu korekcijas un pārsūtīšanas darbības tiks sinhronizētas ar programmatūru Supply Chain Management pēc tam, kad vienumam **Grāmatošanas statuss** iestatījums tiek mainīts no **Izveidots** uz **Grāmatots**. Kad tas notiek, korekcijas vai pārsūtīšanas pasūtījums tiks slēgts un kļūs tikai lasāms. Tas nozīmē, ka korekcijas un pārsūtīšanas darbības var tikt grāmatotas programmatūrā Supply Chain Management, bet tās nevar modificēt. Programmatūrā Supply Chain Management var iestatīt pakešuzdevumu, lai automātiski grāmatotu korekcijas un pārsūtītu krājumu žurnālus, kuri ģenerēti integrācijas laikā. Skatiet tālāk norādītos priekšnosacījumus, lai iegūtu informāciju par to, kā iespējot pakešuzdevumu.

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM 
Tabulai **Prece** ir pievienota kolonna **Krājumu uzskaites vienība**. Šī kolonna ir nepieciešama, jo pārdošanas un krājumu uzskaites vienības ne vienmēr sakrīt programmatūrā Supply Chain Management, un noliktavas krājumiem programmatūrā Supply Chain Management ir nepieciešama krājumu uzskaites vienība.
Atlasot preci vienumam Krājumu korekcijas prece gan krājumu korekcijām, gan krājumu pārsūtīšanai, vienība tiks iegūta no krājumu preces vērtības. Ja vērtība tiek atrasta, kolonnā **Vienība** tiek fiksēts iestatījums Krājumu korekcijas prece.

Kolonna **Grāmatošanas statuss** ir pievienota gan tabulai **Krājumu korekcija**, gan tabulai **Krājumu pārvietošana**. Šo kolonnu izmanto kā filtru, ja korekcija vai pārsūtīšana tiek nosūtīta uz programmatūru Supply Chain Management. Šīs kolonnas noklusējuma iestatījums ir Izveidots (1), taču tas netiek nosūtīts uz programmatūru Supply Chain Management. Atjauninot vērtību uz Grāmatots (2), tas tiek sūtīts uz programmatūru Supply Chain Management, bet pēc tam vairs nevarēsit mainīt korekciju un pārsūtīšanas darbību vai pievienot jaunas rindas.

Tabulai **Krājumu korekcijas prece** ir pievienota kolonna **Numuru sērija**. Šī kolonna nodrošina to, ka integrācijai ir unikāls numurs, tādējādi integrācija var izveidot un atjaunināt korekciju. Veidojot pirmo krājumu korekcijas preci, tiks izveidots jauns ieraksts tabulā **P2C AutoNumber**, lai uzturētu izmantoto numuru sēriju un prefiksu.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

### <a name="supply-chain-management"></a>Supply Chain Management
Integrācijas krājumu žurnālus, kas ģenerēti integrācijas ietvaros, var automātiski grāmatot, izmantojot pakešuzdevumu. To iespējo šādi: **Krājumu vadība > Periodiskie uzdevumi > Dataverse integrācija > Grāmatot integrācijas krājumu žurnālus**.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Krājumu korekcija (no Field Service uz Supply Chain Management): Krājumu korekcija

[![Krājumu kartēšana datu integrācijā, krājumu pielāgošana (no Field Service uz Supply Chain Management): Krājumu pielāgošana.](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Krājumu pārsūtīšana (no Field Service uz Supply Chain Management): Krājumu pārsūtīšana

[![Krājumu kartēšana datu integrācijā, krājumu pārsūtīšana (no Field Service uz Supply Chain Management): Krājumu pārsūtīšana.](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]