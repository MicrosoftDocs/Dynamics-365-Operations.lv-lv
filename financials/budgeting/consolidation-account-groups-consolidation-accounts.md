---
title: "Konsolidācijas konts grupas un papildu konsolidācijas konti"
description: "Šajā tēmā ir sniegta informācija par konsolidāciju kontu grupas un papildu konsolidācijas konti, un skaidro, kā viņi izmanto Microsoft Dynamics 365 operācijām."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f9c5aaa389c9c2f85d1ab91cbf3d2222cbebef55
ms.lasthandoff: 03/31/2017


---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolidācijas konts grupas un papildu konsolidācijas konti

Šajā tēmā ir sniegta informācija par konsolidāciju kontu grupas un papildu konsolidācijas konti, un skaidro, kā viņi izmanto Microsoft Dynamics 365 operācijām.

<a name="consolidation-account-groups"></a>Konsolidācijas kontu grupas
----------------------------

Konsolidācijas konts grupām ļauj izveidot kontus, kurus vēlaties izmantot datu konsolidācijas grupas. Visbie āk konsolidācijas kontu grupu pārstāv valdība pilnvaroja kontu plāna kontiem vai kartes kontu grupā, ko definē uzņēmuma galveno mītni. Jūs varat atrast konsolidācijas grupas konta **Setup** jomā **konsolidācijas** moduli. Kad jūs pievienojat jaunu grupu, kontu grupu un nosaukumu ievadiet unikālo identifikatoru.

## <a name="additional-consolidation-accounts"></a>Papildu konsolidācijas konti
Papildu konsolidācijas konti ļauj piešķirt konts esošo kontu plāna kontiem konsolidācijas kontu grupu. Pēc tam varat norādīt konsolidācijas konts vērtībai, gan nosaukumam. 

Jūs varat atrast papildu konsolidācijas konti **Setup** jomā **konsolidācijas** moduli. Veidojot jaunu konsolidācijas kontu, ir jānorāda šāda informācija:

-   **Galvenais konta** -šis lauks ir uzmeklēšanas, kas parāda visu galveno kontiem, kas ir balstīti uz kontu atlasītajā lapā. Kad atlasāt konts, nosaukums tiek automātiski ievadīta **galvenā konta nosaukums** lauks.
-   **Konsolidācijas konts grupa** – Lietojiet šo lauku, lai norādītu grupu, lai kontam piešķirtu. Ja jūs konsolidējat divos dažādos veidos, visi četri konsolidācijas kontu grupas jāpievieno vienu un to pašu kontu.
-   **Konsolidācijas konts** -ievadiet konsolidācijas konts vērtība. Šī vērtība nav kontu no kontu plāna kontiem. Tas var būt jebkura vērtība, kas jums nepieciešams.
-   **Konsolidācijas konts nosaukums** -ievadiet konta nosaukumu, kā vēlaties to redzēt izdrukā uz vaicājumiem un atskaitēm.
-   **SAT līmenī** -šis lauks tiek izmantots, lai ziņo konta izrakstus Meksikas nodokļu iestādēm. 

Kad esat pabeidzis, radot konsolidācijas kontu grupas un papildu konsolidācijas konti, iespējams atlasīt visu grupu konsolidēt tiešsaistes procesā.



