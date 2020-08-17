---
title: Atpakaļceļa modulis
description: Šajā tēmā tiek stāstīts par atpakaļceļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 38efc3a60ae0ba49db2036dc84c49e4896727d94
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621064"
---
# <a name="breadcrumb-module"></a>Atpakaļceļa modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par atpakaļceļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Atpakaļceļa moduļi tiek izmantoti, lai nodrošinātu sekundāro navigāciju vietas lapās. Parasti tie tiek parādīti lapas augšmalā zem virsraksta. Kaut arī atpakaļceļa moduļus var pievienot jebkurai lapai, tie visbiežāk tiek izmantoti produktu informācijas lapās (PDP), lai parādītu preču kategoriju hierarhiju un nodrošinātu ātru veidu, kā pārvietoties vietnē. Atpakaļceļa moduli var izmantot arī, lai parādītu saiti "Atgriezties pie rezultātiem", kad lietotāji atver PDP no meklēšanas vai saraksta lapas. Šādā veidā lietotāji var ātri atgriezties filtrētā saraksta lapā, lai turpinātu iepirkšanos.

Lapās, kurās ir preču kategorijas konteksts, piemēram, PDP un kategoriju lapas, atpakaļceļa moduļi rāda kategoriju hierarhiju. Lapās, kurām nav kategorijas konteksta, atpakaļceļa moduļi pēc noklusējuma rāda **&lt;Vietnes sakne&gt; / &lt;Pašreizējā lapa&gt;**. Atpakaļceļa moduļus var arī manuāli konfigurēt citos vietņu lapu veidos, lai parādītu saites uz noteiktām lapām attiecīgajā vietnē.

Attēlā zemāk parādīts atpakaļceļa moduļa piemērs, kas parāda kategoriju hierarhiju PDP.

![Atpakaļceļa moduļa piemērs](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>Atpakaļceļa moduļa iestatījumi

Atpakaļceļa modulis balstās uz iestatījumu **Atpakaļceļa rādīšanas veids PDP**, kas ir definēts vietnes vietņu veidotājā **Vietnes iestatījumi \> Paplašinājumi**. Šim iestatījumam ir pieejamas trīs vērtības.

- **Rādīt kategoriju hierarhiju** — ja ir atlasīta šī vērtība, atpakaļceļa modulis parāda pilnu kategoriju hierarhiju precei, kas tiek skatīta PDP.
- **Rādīt atpakaļ pie rezultātiem** — ja atlasīta šī vērtība, atpakaļceļa modulis rādīs "Atpakaļ pie rezultātiem" saiti PDP, ja lietotājs ir atvēris PDP no moduļa, kas ļauj izveidot saiti "Atpakaļ pie rezultātiem". Šī funkcionalitāte ir pieejama, ja lietotāji veic navigāciju no kategorijas, meklēšanas, saraksta un rekomendāciju saraksta lapas. Lai atbalstītu šo funkcionalitāti, preču kolekciju un meklēšanas rezultātu moduļiem ir rekvizīts, kas ir nosaukts **Atļaut atgriešanos pie rezultātiem PDP**. Šis rekvizīts sniedz jums elastību, lai definētu, kuriem moduļiem jāatbalsta "Atpakaļ pie rezultātiem" saites funkcionalitāte PDP. Piemēram, kad tiek atlasīta opcija **Rādīt atgriešanos pie rezultātiem** atpakaļceļa moduļa iestatījumam **Atpakaļceļa rādīšanas veids PDP**, un opcija **Ļaut atgriezties pie rezultātiem PDP** ir atlasīta meklēšanas lapas meklēšanas rezultātu modulim, saite "Atpakaļ pie rezultātiem" tiks parādīta, kad lietotāji no meklēšanas lapas pāriet uz PDP.
- **Rādīt kategoriju hierarhiju un atgriezties pie rezultātiem** — šī vērtība ir iepriekšējo divu vērtību kombinācija. Atlasot šo vērtību, atpakaļceļa modulis parāda gan pilnu kategoriju hierarhiju, gan saiti "Atgriezties pie rezultātiem" (ja tā ir konfigurēta) PDP.

## <a name="breadcrumb-module-properties"></a>Atpakaļceļa moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | apraksts |
|---------------|--------|-------------|
| Sakne | Teksts vai saite| Šis neobligātais rekvizīts norāda saites tekstu un saites mērķi atpakaļceļa vietas saknei. Ja šis rekvizīts nav konfigurēts, sakne netiks definēta. |
| Atpakaļceļa saite | Saistīt | Šis neobligātais rekvizīts norāda saites manuāli konfigurētam atpakaļceļam, ja šīs saites ir nepieciešamas. Saites parādās tādā secībā, kādā tās ir uzskaitītas. |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>Atpakaļceļa moduļa pievienošana jaunā lapā

Lai pievienotu atpakaļceļa moduli PDP un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Vietnes iestatījumi/> paplašinājumi** un pēc tam atlasiet **Rādīt kategoriju hierarhiju** iestatījumam **Atpakaļceļa rādīšanas veids PDP**.
1. Atveriet **Veidnes** un atlasiet PDP veidni.
1. Slotā **Konteiners**, kas satur lodziņu pirkšanas lodziņu, atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Atpakaļceļs** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atveriet PDP, kas izmanto PDP veidni. Ja PDP vēl nepastāv, izveidojiet to.
1. Slotā **Konteiners**, kas satur lodziņu pirkšanas lodziņu, atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Atpakaļceļs** un pēc tam atlasiet **Labi**.
1. Slota **Atpakaļceļš** rekvizītu rūtī sadaļā **Saknes** atlasiet **Saites teksts**.
1. Dialoglodziņā **Saites teksts** ievadiet **Sākums** un pēc tam sadaļā **Saites mērķis** atlasiet **Pievienot saiti**.
1. Dialoglodziņā **Pievienot saiti** atlasiet saiti atpakaļceļa saknei un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Noklusējuma kategorijas ielādes lapas un meklēšanas rezultātu lapas apskats](category-search-page-overview.md)

[Preču kolekcijas moduļi](product-collection-module-overview.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)
