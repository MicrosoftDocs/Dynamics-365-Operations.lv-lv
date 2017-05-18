---
title: "nedokumentēts"
description: "Optimizācijas priekšlikums ir sistēmas izveidots priekšlikums mainīt esošu plānotu vai apstiprinātu pasūtījumu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c011ac5dbba5e98ff9f743237b02a69ea2b36a9d
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="action-messages"></a>Darbību ziņojumi

[!include[banner](../includes/banner.md)]


Optimizācijas priekšlikums ir sistēmas izveidots priekšlikums mainīt esošu plānotu vai apstiprinātu pasūtījumu.

## <a name="introduction"></a>Ievads

Darbību ziņojumus ģenerē vispārējās plānošanas aprēķins, reaģējot uz prasību izmaiņām. Piemēram, nosūtīšanas datums vai daudzums var tikt mainīts pārdošanas pasūtījumā, kuram jau esat izveidojis pirkšanas pasūtījumu, lai izpildītu pieprasījumu. Šādā gadījumā vispārējās plānošanas aprēķins ģenerē vienu vai vairākus darbību ziņojumus, lai atjauninātu šo pirkšanas pasūtījumu. Jūs izlemjat, vai veikt ierosinātās izmaiņas.

Varat iestatīt veidu, kā ziņojumi tiek aprēķināti seguma grupai, kuru piesaistāt krājumam.

## <a name="select-action-messages"></a>Darbību ziņojumu atlasīšana

Lapā **Seguma grupas** varat atlasīt darbību ziņojumus, kurus vēlaties, lai sistēma ģenerē, kā arī atlasīt, uz kurām vajadzību grupām vai krājumiem šie ziņojumi attiecas. Varat atlasīt no tālāk uzskaitītajiem darbību ziņojumiem.

| Ziņojums             | Apraksts                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Avanss**         | Ja atlasāt šo ziņojumu, sistēma ģenerē darbību ziņojumus, kad nepieciešams, lai pasūtījumus pārvietotu uz agrāku datumu. Laukā **Avansa dienu skaits** varat arī norādīt maksimālo dienu skaitu starp ieejas un izejas plūsmām, kad netiek veikta avansa darbība. |
| **Atlikt**        | Ja atlasāt šo ziņojumu, sistēma ģenerē darbību ziņojumus, kad nepieciešams, lai pasūtījumus pārvietotu uz vēlāku datumu. Laukā **Atlikšanas dienu skaits** varat norādīt maksimālo dienu skaitu starp ieejas un izejas plūsmām, kad netiek veikta atlikšanas darbība.       |
| **Samazināt**        | Ja atlasāt šo ziņojumu, tad ražošanas pasūtījumi, pirkšanas pasūtījumi un citas ieejas plūsmas transakcijas ir jāsamazina, lai novērstu pārliekus krājumu līmeņus.                                                                                                   |
| **Pieaugums**        | Ja atlasāt šo ziņojumu, tad ražošanas pasūtījumi, pirkšanas pasūtījumi un citas ieejas plūsmas transakcijas ir jāpalielina, lai novērstu krājumu iztrūkumus.                                                                                                    |
| **Atvasinātās darbības** | Ja atlasāt šo ziņojumu, darbību ziņojumi tiek izveidoti atvasinātajām prasībām, piemēram, darbības komponentu pasūtījumiem, lai izpildītu ražošanu.                                                                                                   |






