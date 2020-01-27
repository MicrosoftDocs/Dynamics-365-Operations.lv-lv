---
title: Konfidencialitātes politikas lapas pievienošana
description: Šajā tēmā ir aprakstīts, kā pievienot konfidencialitātes politikas lapu savai vietnei programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd39ff5f8c5d97f2d524043b65627dc7e87fcf64
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946049"
---
# <a name="add-a-privacy-policy-page"></a>Konfidencialitātes politikas lapas pievienošana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pievienot konfidencialitātes politikas lapu savai vietnei programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Konfidencialitātes ievērošana ietver organizatoriskus pasākumus, kas informē vietnes lietotājus par to, kā tiek apkopoti un apstrādāti viņu dati. Pēc tam lietotāji var izlemt, kā viņi vēlas, lai viņu personas dati tiktu apstrādāti, un var veikt atbilstošas darbības.

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>Pārskatiet Microsoft paziņojumu par konfidencialitāti pakalpojumā Dynamics 365 Commerce

Lai pārskatītu Microsoft paziņojumu par konfidencialitāti, kamēr esat pieteicies Dynamics 365 Commerce autorēšanas rīkos, augšējā labajā stūrī atlasiet pogu **Palīdzība** (**?**) un pēc tam atlasiet **Konfidencialitāte un sīkfaili**. Tiek atvērta jauna cilne, kurā ir saite uz [Microsoft paziņojumu par konfidencialitāti](https://privacy.microsoft.com/privacystatement).

## <a name="build-a-privacy-policy-page-for-your-site"></a>Konfidencialitātes politikas lapas izveide jūsu vietnei

Pakalpojumā Dynamics 365 Commerce ir iespējami vairāki veidi, kā vietnes lietotājiem sniegt piekļuvi jūsu konfidencialitātes politikai. Šajā sadaļā ir parādīts, kā izveidot konfidencialitātes politikas lapu un pēc tam atsaukties uz lapu, izmantojot kājenes fragmentu.

Vadlīnijas, kas redzamas tālāk piemērā, parāda, kā veidot vispārēju konfidencialitātes lapu Commerce vietnē. Jūs esat atbildīgs par to, lai izstrādātu un ieviestu tādu konfidencialitātes politikas lapas risinājumu, kas vislabāk atbilst jūsu uzņēmuma juridiskajām prasībām.

Lai sāktu, autorēšanas rīkos dodieties uz vietni, kurai vēlaties izveidot konfidencialitātes politikas lapu.

### <a name="create-a-template"></a>Izveidot veidni

> [!NOTE]
> Ja veidne, ko var izmantot konfidencialitātes politikas lapā, jau ir izveidota, pārejiet uz priekšu uz sadaļu [Konfidencialitātes politikas izveide](#build-a-privacy-policy-page).

Lai izveidotu veidni, veiciet tālāk norādītās darbības.

1. Dodieties uz sadaļu **Veidnes \> Jauna veidne**.
1. Ievadiet veidnes nosaukumu un pēc tam atlasiet **Labi**.
1. Veidnē pievienojiet nepieciešamos moduļus nepieciešamajiem lapas slotiem. Lai iegūtu norādījumus, virziet kursoru virs sarkanajām izsaukuma zīmēm.

    Piemēram, **HTML galvenais** slotam var būt nepieciešams **noklusējuma ārējā skripta** modulis.

1. Slotā **Pamatteksts** pievienojiet moduli **Noklusējuma lapa**.
1. Moduļa **Noklusējuma lapa** slotā **Galvenais** pievienojiet moduli **Bagātinātā satura bloks**.
1. Modulī **Bagātinātā satura bloks** pievienojiet moduli **Bagātinātā satura bloka vienums**.
1. Pārbaudiet veidni un publicējiet to.

### <a name="build-a-privacy-policy-page"></a>Konfidencialitātes politikas lapas izveide

Lai izveidotu konfidencialitātes politikas lapu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Lapas \>Jauna lapa**.
1. Atlasiet konfidencialitātes politikas lapas veidni.
1. Ievadiet lapas nosaukumu un vietrādi URL pēc tam atlasiet **Labi**. 
1. Jaunās lapas slotā **Galvenais** pievienojiet moduli **Bagātinātā satura bloks**.
1. Modulī **Bagātinātā satura bloks** pievienojiet moduli **Bagātinātā satura bloka vienums**.
1. Moduļa **Bagātinātā satura bloks** rekvizītu rūtī atlasiet **Pievienot datu avotu** un tad atlasiet **Bagātinātā satura bloks**.
1. Bagātinātā teksta redaktorā ievadiet konfidencialitātes politikas lapas saturu. Izvērsiet bagātinātā teksta redaktoru uz pilnekrāna režīmu, kā jums nepieciešams.
1. Kad esat pabeidzis satura ievadīšanu, atlasiet **Priekšskatījums**, lai priekšskatītu lapu tīmekļa pārlūkprogrammā.
1. Aizpildiet visus atlikušos lapas un moduļa rekvizītu papildinājumus.
1. Pārbaudiet konfidencialitātes politikas lapu un publicējiet to.

Lai publicētu vietrādi URL konfidencialitātes politikas lapai, veiciet šādas darbības.

1. Pārejiet uz sadaļu **URL** un atlasiet konfidencialitātes politikas lapas vietrādi URL.
1. Publicējiet atlasīto vietrādi URL.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Saites, ka novirza uz konfidencialitātes politiku lapu, izveide kājenē

Varat pievienot saiti uz konfidencialitātes politikas lapu fragmentam. Šādā veidā varat kopīgot saiti un atjaunināt to vairākās vietnes lapās, atsaucoties uz fragmentu. Šajā piemērā parādīts, kā pievienot saiti uz konfidencialitātes politikas lapu kājenes fragmentam.

Lai fragmentam pievienotu saiti, veiciet tālāk norādīto.

1. Dodieties uz **Lapas fragmenti \> Jauns lapas fragments**.
1. Atlasiet moduli **Kājene** un pēc tam ievadiet nosaukumu laukā **Lapas fragmenta nosaukums**.
1. Slotā **Kājene kategorija** pievienojiet moduli **Kājenes vienums**.
1. Rekvizītu rūts labajā pusē atlasiet **Saites teksts**.
1. Dialoglodziņā **Saites teksts** ievadiet konfidencialitātes politikas lapas saites tekstu un saites mērķi un pēc tam noklikšķiniet uz **Labi**.

    Lai iegūtu konfidencialitātes politikas lapas vietrādi URL, atveriet **Lapas**, dodieties uz konfidencialitātes politikas lapu un kopējiet vietrādi URL no rekvizītu rūts.

1. Saglabājiet fragmentu, pārbaudiet un publicējiet to.
1. Priekšskatiet fragmentu un pārbaudiet saiti uz konfidencialitātes politikas lapu.

Uz fragmentu tagad var atsaukties veidnē citām vietnes lapām. Ja uz šo fragmentu ir atsauce veidnes modulī **Kājene**, saites atsauce tiks parādīta visās lapās, kas ir veidotas, izmantojot šo veidni.

## <a name="additional-resources"></a>Papildu resursi

[Atbilstības pārskats](compliance-overview.md)

[Pieejamības līdzekļi un iespējas](accessibility.md)

[Sīkfailu atbilstība](cookie-compliance.md)
