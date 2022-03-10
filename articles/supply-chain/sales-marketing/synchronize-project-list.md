---
title: Programmatūrā Supply Chain Management ietvertā projektu saraksta sinhronizēšana ar Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto projektu sinhronizēšanai ar programmu Dynamics 365 Field Service.
author: Henrikan
ms.date: 03/13/2019
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
ms.openlocfilehash: b825e2fce61e96b963ba0d41f8db49ca9ba646f6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571597"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Programmatūrā Supply Chain Management ietvertā projektu saraksta sinhronizēšana ar Field Service

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto projektu sinhronizēšanai ar programmu Dynamics 365 Field Service.

[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi
Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai palaistu projektu sinhronizāciju no programmatūras Supply Chain Management uz Field Service.

**Veidne līdzeklī Datu integrācija**
- Projekti (no Supply Chain Management uz Field Service)

**Uzdevums datu integrācijas projektā**
- Projekti

Lai varētu veikt projektu saraksta sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.
- Konti (no Sales uz Supply Chain Management) 

## <a name="entity-set"></a>Elementu kopa
| Field Service           | Supply Chain Management  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekti                |

## <a name="entity-flow"></a>Elementu plūsma
Projekti tiek veidoti programmatūrā Supply Chain Management. Projekti, kuriem vienumam **Projekta tips** atlasīts iestatījums **Laiks un materiāli** un vienumam **Projekta posms** atlasīts iestatījums **Apstrāde**, tiks sinhronizēti uz entītiju **Ārējais projekts** programmā Field Service, ieskaitot šādu informāciju: Projekta numurs, Projekta nosaukums, Projekta posms un Debitora konts. Entītijas **Ārējais projekts** saraksts tiek izmantots, lai savienotu pārī Field Service darba pasūtījumus ar Supply Chain Management projektiem.

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM
Entītija **Ārējais projekts** iegūst visus projektus no Supply Chain Management. Entītijai **Darba pasūtījums** ir pievienots lauks **Ārējais projekts**. Tas ir uzmeklēšanas lauks, tādēļ, marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums tiks savienots ar projektu programmatūrā Supply Chain Management. Pēc tam, kad vienumam **Sistēmas statuss** iestatījums **Atvērts - Notiek izpilde(690,970,000)** tiek mainīts uz augstāku statusu, lauks **Ārējais projekts** tiks slēgts un vairs nebūs iespējams pievienot, noņemt vai mainīt vērtību.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums
### <a name="supply-chain-management"></a>Supply Chain Management
Iespējojiet izmaiņu izsekošanu datu elementu projektiem.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Projekti (no Supply Chain Management uz Field Service): Projekti

[![Veidņu kartēšana līdzeklī Datu integrācija.](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]