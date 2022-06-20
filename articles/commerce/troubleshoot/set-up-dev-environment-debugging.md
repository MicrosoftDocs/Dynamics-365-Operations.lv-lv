---
title: E-komercijas izstrādes vides iestatīšana, lai atkļūdotu, izmantojot 1. līmeņa Retail Server virtuālo mašīnu
description: Šajā rakstā ir izskaidrots, kā iestatīt e-komercijas izstrādes vidi, lai atkļūdotu no 1. pakāpes Retail Server virtuālās mašīnas (VM).
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7cc6c936c67bc82da1a237341ac07fb69d4ac233
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855706"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>E-komercijas izstrādes vides iestatīšana, lai atkļūdotu, izmantojot 1. līmeņa Retail Server virtuālo mašīnu

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā iestatīt e-komercijas izstrādes vidi, lai atkļūdotu no 1. pakāpes Retail Server virtuālās mašīnas (VM).

## <a name="description"></a>Apraksts

Microsoft Dynamics 365 Commerce 1. līmeņa vides parasti tiek izvietotas Commerce Runtime (CRT) un pārdošanas punkta (POS) paplašinājuma izstrādei. Tās ir savrupas vides. Programmatūras kā pakalpojuma (SAA) arhitektūras rakstura dēļ tās neietver e-komercijas komponentus.

Dažos scenārijos, iespējams, vēlēsities testēt izsaukumus paplašinājumiem 1. līmeņa vidē, lai varētu atkļūdot paplašinājumus no e-komercijas komponentiem. Vispārīgiem norādījumiem skatiet sadaļu [Atkļūdošana, izmantojot 1. līmeņa Commerce izstrādes vidi](../e-commerce-extensibility/debug-tier-1.md).

Kad atkļūdojat, izmantojot 1. līmeņa vidi, jo vietne tagad izsauc citu Retail Server, starpservera izsaukumi var izraisīt dažādas kļūdas, kas saistītas ar satura drošības politiku.

Attēlā zemāk parādīts kļūdas piemērs, kura var rasties, ja preču informācijas lapā ir atlasīts variants.

![Kļūda, ja preču informācijas lapā ir atlasīts variants.](media/unhandled-rejection-error.jpg)

Attēlā zemāk ir parādīts līdzīgas kļūdas piemērs pārlūka atkļūdotāja rīkos (F12 izstrādātāja rīki). Kļūdas ziņojumā minēts satura drošības politikas direktīvas pārkāpums.

![Atkļūdotāja rīku kļūda.](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Novēršana

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Vietnes satura drošības politikas atspējošana Commerce vietnes veidotājam

1. Atlasiet vietni, pie kuras strādājat.
1. Atlasiet **Iestatījumi** un pēc tam atlasiet **Paplašinājumi**.
1. Cilnē **Satura drošības politika** atlasiet **Atspējot satura drošības politiku**.
1. Atlasiet **Saglabāt un publicēt**.

> [!NOTE]
> Pierakstīšanās "uzņēmums-patērētājs" (B2C) nedarbosies vietējā izstrādes vidē. Tomēr, ja nepieciešams, varat izmantot viesa norēķinu vai veidot lapas pārbaudes objektus, lai simulētu lietotāja pierakstīšanu.

## <a name="additional-resources"></a>Papildu resursi

[Darba sākšana ar e-komercijas tiešsaistes paplašināmības izstrādi](../e-commerce-extensibility/sdk-getting-started.md)

[Satura drošības politikas (CSP) pārvaldība e-komercijas vietnē](../manage-csp.md)
