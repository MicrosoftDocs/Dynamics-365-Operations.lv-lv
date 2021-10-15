---
title: Programmā Supply Chain Management ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietvertās krājumu līmeņu informācijas sinhronizēšanai ar programmu Dynamics 365 Field Service.
author: Henrikan
ms.date: 05/07/2019
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
ms.openlocfilehash: 31674b2be3deb52277cbf79e1e076da13bf94404
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566363"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Programmā Supply Chain Management ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietvertās krājumu līmeņu informācijas sinhronizēšanai ar programmu Dynamics 365 Field Service.

[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi
Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu programmā Supply Chain Management ietverto rīcībā esošo krājumu līmeņu sinhronizēšanu ar programmu Field Service.

**Veidne līdzeklī Datu integrācija**
- Preču krājumi (no Supply Chain Management uz Field Service)
  
**Uzdevums datu integrācijas projektā**
- Preču krājumi

Lai varētu veikt krājumu līmeņu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.
- Noliktavas (no Supply Chain Management uz Field Service) 
- Field Service preces ar Krājumu uzskaites vienību (no Supply Chain Management uz Sales) 

## <a name="entity-set"></a>Elementu kopa

| Field Service                      | Supply Chain Management                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Dataverse Rīcībā esošie krājumi pēc noliktavas     |

## <a name="entity-flow"></a>Elementu plūsma
Programmā Finance and Operations ietvertā krājumu līmeņu informācija tiek nosūtīta uz programmu Field Service atlasītām precēm. Krājumu līmeņa informācija ietver tālāk minētos datus. 
- Rīcībā esošais daudzums (pašreiz reģistrētais fiziskais daudzums, kas atrodas noliktavā)
- Pasūtījumā iekļautais daudzums (kopējais pasūtījumā iekļautais daudzums, piemēram, pārdošanas pasūtījumi)
- Pasūtītais daudzums (kopējais reģistrētais pasūtītais daudzums, piemēram, pirkšanas pasūtījumi)

Šī informācija ir iegūta par katru izlaisto preci katrai noliktavai un sinhronizēta, pamatojoties uz izmaiņu izsekošanu, mainoties krājumu līmenim.

Programmā Field Service integrācijas risinājums izveido krājumu žurnālus starpībai, lai līmeņi programmā Field Service atbilstu līmeņiem programmā Supply Chain Management.

Programma Supply Chain Management darbosies kā šablons krājumu līmeņiem. Tādēļ ir svarīgi iestatīt integrāciju darba pasūtījumiem, pārsūtīšanām un korekcijām no programmas Field Service programmā Supply Chain Management, ja šī funkcionalitāte tiek izmantota programmā Field Service, kopā ar krājumu līmeņu sinhronizāciju no programmas Supply Chain Management.

Preces un noliktavas, kurās krājumu līmeņi tiek pārvaldīti no programmas Supply Chain Management, var kontrolēt, izmantojot vienumu Izvērsts vaicājums un filtrēšana (Power Query).

> [!NOTE]
> Ir iespējams izveidot vairākas noliktavas programmā Field Service (ja atlasīts iestatījums **Tiek ārēji uzturēts= Nē**) un pēc tam kartēt tās uz vienu noliktavu programmā Supply Chain Management, izmantojot funkcionalitāti Izvērsts vaicājums un filtrēšana. Tas tiek izmantots gadījumos, ja vēlaties, lai programma Field Service pārvalda detalizētu krājumu līmeni un tikai nosūta atjauninājumus uz programmu Supply Chain Management. Šajā gadījumā programma Field Service nesaņems krājumu līmeņu atjauninājumus no programmas Supply Chain Management. Papildinformāciju skatiet sadaļā [Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) un [Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM
Elements **Ārējie preču krājumi** tiek izmantots tikai integrācijas iekšējos procesos. Šis elements saņem krājumu līmeņu vērtības no programmas Supply Chain Management integrācijā un pārveido šīs vērtības manuālos krājumu žurnālos, kuri pēc tam maina krājumu preces noliktavā.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

### <a name="data-integration"></a>Datu integrācija
Lai projekts darbotos, ir jānodrošina, ka tiek atjaunināta msdynce_externalproductinventories integrācijas atslēga.
1.  Dodieties uz **Datu integrācija > Savienojumu kopas**.
2.  Atlasiet lietoto savienojuma kopu.
3.  Cilnē **Integrācijas atslēga** nodrošiniet, lai msdynce_externalproductinventories tiktu pievienotas šādas atslēgas:
      - msdynce_productnumber (preces numurs)
      - msdynce_warehouseid (noliktavas ID)
      
### <a name="data-integration-project"></a>Datu integrācijas projekts
Varat lietot filtrus ar funkcionalitāti Izvērsts vaicājums un filtrēšana, lai tikai noteiktas preces un noliktavas sūta krājumu līmeņu informāciju no programmas Supply Chain Management uz programmu Field Service.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Preču krājumi (no Supply Chain Management uz Field Service): Preču krājumi

[![Veidņu kartēšana līdzeklī Datu integrācija.](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]