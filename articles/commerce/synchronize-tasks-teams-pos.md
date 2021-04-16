---
title: Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS
description: Šajā tēmā ir aprakstīts, kā sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce pārdošanas punktu un pārdošanas punktu (POS).
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ca0cb32ac3ee508ddcd5346a895fb9904fa92517
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842706"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā ir aprakstīts, kā sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce pārdošanas punktu un pārdošanas punktu (POS).

Viens no Teams integrācijas galvenajiem nolūkiem ir iespējot uzdevumu pārvaldības sinhronizāciju starp POS programmu un Teams. Šādā veidā veikala darbinieki uzdevumu pārvaldīšanai var izmantot vai nu POS programmu, vai Teams, un programmas nav jāpārslēdz.

Tā kā Plānotājs tiek izmantots kā brigādes uzdevumu repozitorijs, ir jābūt saitei starp Teams un Dynamics 365 Commerce. Šī saite ir izveidota, izmantojot noteiktai veikala grupai noteiktu plāna ID.

Šīs procedūras parāda, kā iestatīt uzdevumu pārvaldības sinhronizāciju starp POS un Teams programmām.

## <a name="publish-a-test-task-list-in-teams"></a>Publicēt pārbaudes uzdevumu sarakstu Teams

Šajā procedūrā tiek pieņemts, ka jūsu veikalu grupas Microsoft Teams pirmo reizi izmanto uzdevumu pārvaldības integrāciju ar Commerce.

Lai publicētu pārbaudes uzdevumu sarakstu Teams, sekojiet šiem soļiem.

1. Piesakieties Teams kā saziņas pārvaldītājs. Parasti saziņas vadītāji ir lietotāji, kuriem ir Loma **Reģionā pārvaldnieka** programmā Commerce.
1. Navigācijas rūtī pa kreisi atlasiet **Uzdevumi pēc plānotāja**.
1. Cilnē **Publicētie saraksti** apakšējā kreisajā pusē atlasiet **Jauns saraksts** un nosauciet jauno sarakstu **Testa uzdevumu saraksts**.
1. Atlasiet **Izveidot**. Jaunais saraksts tiek parādīts zem **Melnraksti**.
1. Zem **Uzdevuma nosaukums** piešķiriet pirmajam uzdevumam nosaukumu **Teams integrācijas testēšana**. Pēc tam atlasiet **Ievadīt**.
1. **Melnrakstu** sarakstā izvēlieties uzdevumu sarakstu. Pēc tam augšējā labajā stūrī atlasiet  **Publicēt** .
1. Dialoglodziņā **Atlasīt, kas tiks publicēts** dialoglodziņā atlasiet grupas, kurām jāsaņem testa uzdevumu saraksts.
1. Atlasiet **Tālāk**, lai pārskatītu publicēšanas plānu. Ja jāveic izmaiņas, atlasiet  **Atpakaļ**. 
1. Atlasiet **Apstiprināt**, lai turpinātu, un pēc tam atlasiet **Publicēt**.
1. Pēc publicēšanas pabeigšanas ziņojums **Publicēto sarakstu** cilnes augšpusē norāda, vai uzdevumu saraksts ir veiksmīgi piegādāts.

Papildinformāciju skatiet sadaļā [Uzdevumu sarakstu publicēšana, lai izveidotu un izsekotu darbu uzņēmumā](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).

## <a name="link-pos-and-teams-for-task-management"></a>Saistīt POS un Teams uzdevumu pārvaldībai

Lai programmā Commerce Headquarters saistītu POS un Microsoft Teams uzdevumu pārvaldībai, rīkojieties šādi.

1. Ejiet uz **Mazumtirdzniecība un komercija \> Uzdevumu pārvaldība \> Uzdevumu integrācija ar Microsoft Teams**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Iestatiet opciju **Iespējot Uzdevumu pārvaldības integrāciju** uz **Jā**.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Iestatīšanas uzdevumu pārvaldība**. Jums jāsaņem paziņojums, kas norāda, ka tiek izveidots pakešuzdevums ar nosaukumu **Teams nodrošināšana**.
1. Dodieties uz **Sistēmas administrēšana \> Uzziņas \> Pakešdarbi** un atrodiet pēdējo darbu ar aprakstu **Teams nodrošināšana**. Uzgaidiet, kamēr šis darbs tiks pabeigts.
1. Palaidiet **CDX darbu 1070**, lai publicētu plāna ID un veikala atsauces uz mazumtirdzniecības serveri.

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats](commerce-teams-integration.md)

[Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju](enable-teams-integration.md)

[Nodrošināt Microsoft Teams no Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Lietotāju lomu pārvaldība Microsoft Teams](manage-user-roles-teams.md)

[Kartējiet veikalus un grupas, ja programmā ir iepriekšējas darba grupas Microsoft Teams](map-stores-existing-teams.md)

[Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ](teams-integration-faq.md)
