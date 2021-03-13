---
title: Organizāciju hierarhiju modelēšanas izveidošana B2B organizācijām
description: Šajā tēmā ir aprakstīts, kā izveidot organizāciju hierarhiju modelēšanu bizness-biznesam (B2B) organizācijām.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 450efd595a1cc1b72b2e62afbdd4518bcca59cb0
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035935"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>Organizāciju hierarhiju modelēšanas izveidošana B2B organizācijām

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot organizāciju hierarhiju modelēšanu bizness-biznesam (B2B) organizācijām Microsoft Dynamics 365 Commerce.

Programmā Commerce Headquarters biznesa partneru organizācijas tiek pārstāvētas ar klientu un klientu hierarhiju entītijām. Biznesa partnera organizācija un tās lietotāji tiek attēloti kā klienti, un klientu hierarhijas tiek izmantotas, lai saistītu šos klientus vienu ar otru.

Kad biznesa partnera pieprasījums pievienoties B2B e-komercijas vietnei ir apstiprināts, tiek veiktas šādas darbības:

- Sistēmā tiek izveidoti divi jauni klientu ieraksti: **Organizācijas tipa** klienta ieraksts biznesa partnera organizācijai un **Personas tipa** klienta ieraksts pieprasītājam (kas ir biznesa partneris, kurš iesniedza pieprasījumu).
- Klientu hierarhijā tiek izveidots jauns ieraksts sadaļā **Klients \> Klientu hierarhijas**. Šim ierakstam ir šādi virsraksta rekvizīti:

    - **Klientu hierarhijas ID** – unikāls klientu hierarhijas ID. Šis ID izmanto numuru sēriju, kas ir definēta Commerce koplietotajos parametros programmā Commerce Headquarters.
    - **Nosaukums** – biznesa partnera organizācijas nosaukums, kā norādīts uzņēmuma pieprasījumā.
    - **Mērķis** – šis rekvizīts ir iestatīts uz iepriekš definētu vērtību **B2B organizācijai**.
    - **Organizācija** – biznesa partnera klienta ID.

Šeit ir detalizēta informācija par klientu hierarhijas ierakstu:

- Pieprasītāja klienta ieraksts ir saistīts ar klientu hierarhiju.
- Administratora loma ir saistīta ar pieprasītāju.

Kad administrators pievieno vairāk lietotāju biznesa partnera organizācijai B2B vietnē, programmā Commerce Headquarters tiek izveidots jauns klienta ieraksts katram lietotājam. Šis klienta ieraksts tiek pievienots arī atbilstošajam biznesa partnera klientu hierarhijas ierakstam, un tam ir “lietotāja” loma.

> [!NOTE]
> Vairumā gadījumu visu hierarhijā esošo klientu ierakstiem ir jāatbilst attiecīgajām rekvizītu vērtībām. Piemēram, tā kā visiem biznesa partneru lietotājiem ir jāsaņem līdzīgas preču cenas, to cenu grupai un saistītajām konfigurācijām ir jāatbilst. Tomēr sistēma šo konsekvenci neievieš. Tāpēc attiecīgie Commerce Headquarters lietotāji ir atbildīgi nodrošināt, ka rekvizītu vērtības un konfigurācijas atbilst visiem attiecīgās hierarhijas klientiem.

Commerce Headquarters lietotāji var skatīt rekvizītu vērtības visiem klientu ierakstiem hierarhijā blakus izvietotajā skatā. Atlasiet atbilstošā klienta ieraksta rekvizītus, nolaižamajā izvēlnē atlasot ciļņu nosaukumus. Lietotāji var tieši skatīt un rediģēt rekvizītu vērtības no šī skata. Vai arī, ja vēlaties lietot visas administratora klienta ieraksta vērtības visiem lietotāja klientu ierakstiem, atlasiet **Pārlabot** klientu hierarhiju informācijā.

## <a name="additional-resources"></a>Papildu resursi

[B2B e-komercijas vietnes iestatīšana](set-up-b2b-site.md)

[Biznesa partneru lietotāju pārvaldīšana B2B e-komercijas vietnēs](manage-b2b-users.md)

[Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs](payment-method.md)

[Preču daudzuma ierobežojumu iestatīšana B2B e-komercijas vietnēs](quantity-limits.md)
