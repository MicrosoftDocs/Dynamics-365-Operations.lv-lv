---
title: "Programmā Finance and Operations ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service"
description: "Šajā tēmā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu krājumu līmeņu informāciju programmā Microsoft Dynamics 365 for Finance and Operations ar programmu Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: lv-lv
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Programmā Finance and Operations ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service 

[!include[banner](../includes/banner.md)]

Šajā tēmā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu krājumu līmeņu informāciju programmā Microsoft Dynamics 365 for Finance and Operations ar programmu Microsoft Dynamics 365 for Field Service.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi
Tālāk norādītā veidne un pamata uzdevumi tiek izmantoti, lai veiktu rīcībā esošo krājumu līmeņu sinhronizēšanu programmā Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Field Service.

**Veidnes nosaukums līdzeklī Datu integrācija:**
- Preču krājumi (no programmas Finance and Operations programmā Field Service)
  
**Uzdevumu nosaukumi datu integrācijas projektā**
- Preču krājumi 

Lai varētu veikt krājumu līmeņu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.
- Noliktavas (no programmas Finance and Operations programmā Field Service) 
- Field Service preces ar krājumu uzskaites vienību (no programmas Finance and Operations programmā Sales) 

## <a name="entity-set"></a>Elementu kopa

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Rīcībā esošie CDS krājumi pēc noliktavas     |

## <a name="entity-flow"></a>Elementu plūsma
Programmā Finance and Operations ietverto krājumu līmeņu informācija tiek nosūtīta uz programmu Field Service atlasītām precēm. Krājumu līmeņa informācija ietver tālāk minētos datus. 
- Rīcībā esošais daudzums (pašreiz reģistrētais fiziskais daudzums, kas atrodas noliktavā)
- Pasūtījumā iekļautais daudzums (kopējais pasūtījumā iekļautais daudzums — t. i., pārdošanas pasūtījumi)
- Pasūtītais daudzums (kopējais reģistrētais pasūtītais daudzums — t. i., pirkšanas pasūtījumi)

Šī informācija ir iegūta par katru izlaisto preci katrai noliktavai un sinhronizēta, pamatojoties uz izmaiņu izsekošanu, mainoties krājumu līmenim.

Programmā Field Service integrācijas risinājums izveido krājumu žurnālus starpībai, lai līmeņi programmā Field Service atbilstu līmeņiem programmā Finance and Operations.

Programma Finance and Operations darbosies kā šablons krājumu līmeņiem. Tāpēc ir svarīgi iestatīt integrāciju darba pasūtījumiem, pārsūtīšanām un korekcijām no programmas Field Service programmā Finance and Operations, ja šī funkcionalitāte tiek izmantota programmā Field Service, kopā ar krājumu līmeņu sinhronizāciju no programmas Finance and Operations.

Preces un noliktavas, kurās krājumu līmeņi tiek pārvaldīti no programmas Finance and Operations, var kontrolēt, izmantojot vienumu Izvērsts vaicājums un filtrēšana (Power Query).

Piezīme. Ir iespējams izveidot vairākas noliktavas programmā Field Services (ja atlasīts iestatījums Tiek ārēji uzturēts = Nē) un pēc tam kartēt tās uz vienu noliktavu programmā Finance and Operations, izmantojot funkcionalitāti Izvērsts vaicājums un filtrēšana. Tas tiek izmantots gadījumos, ja vēlaties, lai programma Field Service pārvalda detalizētu krājumu līmeni un vienkārši nosūta atjauninājumus uz programmu Finance and Operations. Šajā gadījumā programma Field Service nesaņems krājumu līmeņu atjauninājumus no programmas Finance and Operations. Papildinformāciju skatiet sadaļā Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations un Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Finance and Operations.

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM
Entītija Ārējie preču krājumi ir jauna entītija, kas tiek izmantota tikai integrācijas iekšējos procesos. Tā saņem krājumu līmeņu vērtības no programmas Finance and Operations integrācijā un pārveido šīs vērtības manuālos krājumu žurnālos, kuri pēc tam maina krājumu preces noliktavā. 

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

### <a name="in-the-data-integration-project"></a>Datu integrācijas projektā
Lietojiet filtrus ar funkcionalitāti Izvērsts vaicājums un filtrēšana, lai kontrolētu, ka tikai nepieciešamās preces un noliktavas sūta krājumu līmeņu informāciju no programmas Finance and Operations uz programmu Field Service.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Preču krājumi (no programmas Finance and Operations programmā Field Service): Preču krājumi

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

