---
title: "Programmā Field Service ietverto krājumu pārsūtīšanas un korekcijas darbību sinhronizēšana ar programmu Finance and Operations"
description: "Šajā tēmā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu krājumu korekcijas un pārsūtīšanas darbības programmā Microsoft Dynamics 365 for Finance and Operations ar programmu Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: lv-lv
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu krājumu korekcijas un pārsūtīšanas darbības programmā Microsoft Dynamics 365 for Finance and Operations ar programmu Microsoft Dynamics 365 for Field Service.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi
Tālāk norādītā veidne un pamata uzdevumi tiek izmantoti, lai veiktu krājumu korekcijas un pārsūtīšanas darbības sinhronizēšanu programmā Microsoft Dynamics 365 for Field Service un programmā Microsoft Dynamics 365 for Finance and Operations.

**Veidņu nosaukums līdzeklī Datu integrācija:**
- Krājumu korekcija (no programmas Field Service programmā Finance and Operations)
- Krājumu pārsūtīšana (no programmas Field Service programmā Finance and Operations)

**Uzdevumu nosaukumi datu integrācijas projektos:**
- Krājumu korekcijas
- Krājumu pārsūtīšana

## <a name="entity-set"></a>Elementu kopa
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS krājumu korekciju žurnālu virsraksti un rindas |
| msdyn_inventoryadjustmentproducts | CDS krājumu pārsūtīšanas žurnālu virsraksti un rindas   |

## <a name="entity-flow"></a>Elementu plūsma
Programmā Field Service veiktās krājumu korekcijas un pārsūtīšanas darbības tiks sinhronizētas ar programmu Finance and Operations, kad vienumam **Grāmatošanas statuss** iestatījums tiek mainīts no Izveidots uz Grāmatots. Kad tas notiek, korekcijas vai pārsūtīšanas pasūtījums tiks slēgts un kļūs tikai lasāms, jo korekcijas un pārsūtīšanas darbības var tikt grāmatotas programmā Finance and Operations un tādēļ tās nevar modificēt.
Programmā Finance and Operations var iestatīt pakešuzdevumu, lai automātiski grāmatotu korekcijas un pārsūtītu krājumu žurnālus, kas ģenerēti, veicot integrāciju. Skatiet tālāk norādīto priekšnosacījumu, lai iegūtu informāciju par to, kā iespējot pakešuzdevumu.

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM 
Entītijai Prece ir pievienots lauks Krājumu uzskaites vienība. Šis lauks ir nepieciešams, jo pārdošanas un krājumu uzskaites vienības ne vienmēr sakrīt programmā Operations, un noliktavas krājumiem programmā Operations ir nepieciešama krājumu uzskaites vienība.
Atlasot iestatījumu Prece vienumam Krājumu korekcijas prece gan krājumu korekcijām, gan krājumu pārsūtīšanai, vienība tiks iegūta no preču krājumu preces vērtības. Ja vērtība tiek atrasta, laukā Vienība tiek fiksēts iestatījums Krājumu korekcijas prece

Lauks Grāmatošanas statuss ir pievienots gan entītijai Krājumu korekcija, gan entītijai Krājumu pārvietošana. Šo lauku izmanto kā filtru, ja korekcija vai pārsūtīšana tiek nosūtīta uz programmu Operations. Laukam tiek iestatīta noklusējuma vērtība Izveidots (1), un pēc tam tas netiek nosūtīts uz programmu Operations. Mainot vērtību uz Grāmatots (2), tas tiek sūtīts uz programmu Operations, bet pēc tam vairs nevarēsit neko mainīt sadaļā Korekcija vai Pārsūtīšana vai pievienot jaunas rindas.
Entītijai Krājumu korekcijas prece ir pievienots lauks Numuru sērija. Šis lauks palīdz nodrošināt integrācijai unikālu numuru, lai integrācijas process zina, kad veikt izveidošanu un kad veikt atjaunināšanu. Veidojot pirmo Krājumu korekcijas preci, tiks izveidots jauns ieraksts entītijā P2C automātiska numerācija, lai uzturētu izmantoto numuru sēriju un prefiksu.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

### <a name="in-finance-and-operations"></a>Programmā Finance and Operations
Integrācijas krājumu žurnālus, kas ģenerēti integrācijas ietvaros, var automātiski grāmatot, izmantojot pakešuzdevumu. To iespējo šādi: Krājumu vadība > Periodiskie uzdevumi > CDS integrācija > Grāmatot integrācijas krājumu žurnālus

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Krājumu korekcija (no programmas Field Service programmā Finance and Operations): Krājumu korekcija

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Krājumu pārsūtīšana (no programmas Field Service programmā Finance and Operations): Krājumu pārsūtīšana

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSTrans1.png)](./media/FSTrans1.png)

