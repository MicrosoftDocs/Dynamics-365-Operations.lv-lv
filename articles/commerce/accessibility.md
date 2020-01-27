---
title: Pieejamības līdzekļi un iespējas
description: Šajā tēmā ir sniegta informācija par pieejamības funkcijām un iespējām pakalpojumā Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e667f89ffbc5496cc93f83fd3e7b29ba6ffa979
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946047"
---
# <a name="accessibility-features-and-capabilities"></a>Pieejamības līdzekļi un iespējas

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir sniegta informācija par pieejamības funkcijām un iespējām pakalpojumā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Pieejamības funkcijas un iespējas nodrošina funkcionālus līdzekļus visiem lietotājiem, lai piekļūtu un veiktu darbības, lai viņi varētu sasniegt savus mērķus. Šim plašajam lietotāju lokam var būt nepieciešami dzirdes, redzes, mobilitātes vai neirodaudzveidības palīgrīki.

Dažādās funkcijas pakalpojumā Dynamics 365 Commerce ļauj veidot savu vietni, lai tā ietver palīdzības funkcionalitāti. Noformējot vietni, ir jāapsver pieejamības funkcionalitātes apgabali, kas minēti [Microsoft pieejamības centrā](https://www.microsoft.com/accessibility). 

Šajā tēmā ir aprakstīti daži pieejamības funkcionalitātes papildu apgabali, kas jāņem vērā, lietojot pakalpojumu Dynamics 365 Commerce.

## <a name="image-alt-text"></a>Attēlu alternatīvais teksts

Pakalpojumam Dynamics 365 Commerce ir iebūvēta digitālu līdzekļu pārvaldības sistēma, lai izsekotu attēlu un video līdzekļus, kas tiek izmantoti jūsu vietnē. Attēlu parakstus, aprakstus un alternatīvo tekstu var pievienot rekvizītu rūtī, kad attēls ir atlasīts vai augšupielādēts.

## <a name="video-accessibility"></a>Video pieejamība

Dynamics 365 Commerce digitālo līdzekļu pārvaldības sistēma atbalsta vairākus video satura pieejamības līdzekļus. Tālāk esošajā tabulā ir uzskaitīti daži piemēri.

| Video funkcija               | Apraksts |
|-----------------------------|-------------|
| Slēgta parakstīšana (CC)      | Teksts, ko var parādīt videoklipa audio un audio aprakstošiem elementiem, lai palīdzētu lietotājiem ar dzirdes traucējumiem |
| Titri                   | Parakstiet failus, kas parāda konteksta norāžu tekstu vai dialogu ekrānā |
| Audio atšifrējumi           | Runāto vārdu tekstuālais atšifrējums, kas tiek ģenerēts no videoklipa līdzekļa audio |
| Aprakstošais audio           | Sekundārais audio kanāls, kas apraksta saturu vai kontekstu, kas norisinās ekrānā |
| Minimālais vecuma diapazons            | Atribūts, kas var saglabāt minimālo vecumu, kurā skatītājam ir jābūt video skatīšanai (tikai metadatiem) |

### <a name="configure-video-accessibility-elements"></a>Video pieejamības elementu konfigurēšana

Dynamics 365 Commerce jūsu vietnes sadaļā **Līdzekļi** varat augšupielādēt video līdzekļus, kuriem ir atsevišķi faili slēgtiem parakstiem, parastiem audio un aprakstošiem audio. Slēgtie paraksti var arī tikt ģenerēti automātiski, augšupielādējot video līdzekli.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Video līdzekļa augšupielādes laikā ģenerējiet vai augšupielādējiet parakstus

Lai, augšupielādējot videoklipu, automātiski tiktu ģenerēts slēgto parakstu fails, izpildiet tālāk norādīto darbību.

- Dialoglodziņā **Līdzekļa augšupielāde** atlasiet **Automātiski ģenerēt slēgtos parakstus**. Ja veidojat slēgtā paraksta failu, failu atlasītājs slēgto parakstu failiem dialoglodziņā nebūs pieejams.

Lai manuāli augšupielādētu slēgto parakstu failu, kad augšupielādējat videoklipu, veiciet tālāk norādīto darbību.

- Dialoglodziņā **Līdzekļa augšupielāde** noņemiet **Automātiski ģenerēt slēgtos parakstus**.

Lai videoklipam augšupielādētu parastus audio vai aprakstošus audio failus, izmantojiet failu atlasītāju dialoglodziņā **Līdzekļa augšupielāde**.

> [!NOTE]
> Pēc videoklipa līdzekļa augšupielādes var pievienot arī slēgto parakstu, parastus audio un aprakstošus audio līdzekļus. Pārejiet uz sadaļu **Līdzekļi**, atlasiet videoklipa līdzekli un pārbaudiet to, pēc tam video līdzekļa rekvizītu rūtī augšupielādējiet papildu līdzekļus.

#### <a name="edit-cc-and-audio-transcript-files"></a>Rediģēt CC un audio atšifrējuma failus

CC un audio atšifrējuma failus var rediģēt tieši autorēšanas rīkā. Video atskaņošana ir pieejama rediģēšanas laikā.

Lai rediģētu CC un audio atšifrējuma failus, rīkojieties, kā norādīts tālāk.

1. Pārejiet uz sadaļu **Līdzekļi**, atlasiet video līdzekli un pēc tam atlasiet **Rediģēt CC/atšifrējumu**. Tiek parādīts slēgto parakstu un atšifrējuma satura redaktors.
1. Atlasiet **Izrakstīt**.
1. Rediģējiet slēgto parakstu vai atšifrējuma tekstu.
1. Kad esat pabeidzis, atlasiet **Saglabāt** un pēc tam atlasiet **Atdot**.
1. Kad esat gatavs publicēt, atlasiet **Publicēt**.

#### <a name="set-the-minimum-age-attribute"></a>Iestatiet minimālā vecuma atribūtu

Metadatu atribūts **Minimālais vecums** var būt saistīts ar video līdzekļiem.

Lai uzstādītu atribūtu **Minimālais vecums** video līdzeklim, veiciet tālāk norādītās darbības.

1. Pārejiet uz sadaļu **Līdzekļi** un atlasiet video līdzekli.
1. Atlasiet **Izrakstīt**.
1. Video līdzekļa rekvizītu rūtī iestatiet atribūtu **Minimālais vecums**.

> [!NOTE]
> Rekvizītu rūts tiek izmantota tikai metadatu atribūta vērtības iestatīšanai un saglabāšanai. Ir jāizveido pielāgoti moduļi, lai izmantotu šo atribūtu atskaņošanai.

## <a name="additional-resources"></a>Papildu resursi

[Pieejamība formās, produktos un vadīklās](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Microsoft pieejamības centrs](https://www.microsoft.com/accessibility)

[Dynamics 365 pieejamības centrs](https://docs.microsoft.com/dynamics365/get-started/accessibility/index)

[Atbilstības pārskats](compliance-overview.md)

[Sīkfailu atbilstība](cookie-compliance.md)

[Konfidencialitātes politikas lapas pievienošana](add-privacy-page.md)
