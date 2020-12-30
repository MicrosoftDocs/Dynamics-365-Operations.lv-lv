---
title: Konsolidācijas kontu grupas un papildu konsolidācijas konti
description: Šajā tēmā ir sniegta informācija par konsolidācijas kontu grupām un papildu konsolidācijas kontiem, kā arī paskaidrota to lietošana programmā Microsoft Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8db7a60656434aafd8114b08c2c0e9493140f27b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445712"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolidācijas kontu grupas un papildu konsolidācijas konti

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par konsolidācijas kontu grupām un papildu konsolidācijas kontiem, kā arī paskaidrota to lietošana programmā Microsoft Dynamics 365 Finance.

<a name="consolidation-account-groups"></a>Konsolidācijas kontu grupas
----------------------------

Konsolidācijas kontu grupas jums ļauj veidot grupas no kontiem, kurus vēlaties izmantot datu konsolidēšanai. Parasti konsolidācijas kontu grupa pārstāv likumā noteiktu kontu plānu vai kartē kontus uz uzņēmuma vadības definētu grupu. Konsolidācijas kontu grupas ir atrodamas moduļa **Konsolidācijas** apgabalā **Iestatīšana**. Kad pievienojat jaunu grupu, šai kontu grupai ir jāievada unikāls identifikators un nosaukums.

## <a name="additional-consolidation-accounts"></a>Papildu konsolidācijas konti
Papildu konsolidācijas konti jums ļauj konsolidācijas kontu grupai piešķirt kontu no jau esoša kontu plāna. Pēc tam varat norādīt konsolidācijas konta vērtību un nosaukumu. 

Papildu konsolidācijas konti ir atrodami moduļa **Konsolidācijas** apgabalā **Iestatīšana**. Kad veidojat jaunu konsolidācijas kontu, ir jānorāda tālāk uzskaitītā informācija.

-   **Galvenais konts** — šis lauks ir uzmeklēšana, kas rāda visus galvenos kontus, kuri ir balstīti uz lapā atlasīto kontu plānu. Kad atlasāt kādu kontu, šis nosaukums tiek automātiski ievadīts laukā **Galvenā konta nosaukums**.
-   **Konsolidācijas kontu grupa** — izmantojiet šo lauku, lai norādītu grupu, kurai kontu piešķirt. Ja konsolidēšanu veicat divos dažādos veidos, tad tas pats konts jums ir jāpievieno visām četrām konsolidācijas kontu grupām.
-   **Konsolidācijas konts** — ievadiet konsolidācijas konta vērtību. Šai vērtībai nav jābūt kontam no kontu plāna. Tā var būt jebkāda jums nepieciešama vērtība.
-   **Konsolidācijas konta nosaukums** — ievadiet nosaukumu kontam, kuru vēlaties rādīt pieprasījumos un pārskatos.
-   **SAT līmenis** — šis laiks tiek izmantots, lai iesniegtu kontu izrakstus Meksikas nodokļu iestādēm. 

Kad esat beidzis veidot savas konsolidācijas kontu grupas un papildu konsolidācijas kontus, varat atlasīt grupu procesā Konsolidēt tiešsaistē.


Plašāku informāciju skatiet šeit: [Izveidot konsolidācijas grupas un papildu konsolidācijas kontus](../general-ledger/tasks/create-consolidation-groups.md) 



