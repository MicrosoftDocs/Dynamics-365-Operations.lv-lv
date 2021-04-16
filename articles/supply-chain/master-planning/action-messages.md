---
title: Darbību ziņojumi
description: Darbības ziņojums ir sistēmas izveidots priekšlikums mainīt esošu plānotu vai apstiprinātu pasūtījumu.
author: ChristianRytt
ms.date: 10/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea565a8935151235e4c3b103dd86b7131711a4a2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816584"
---
# <a name="action-messages"></a>Darbību ziņojumi

[!include [banner](../includes/banner.md)]

Darbības ziņojums ir sistēmas izveidots priekšlikums mainīt esošu plānotu vai apstiprinātu pasūtījumu.

## <a name="introduction"></a>Ievads

Darbību ziņojumus ģenerē vispārējās plānošanas aprēķins, reaģējot uz prasību izmaiņām. Piemēram, nosūtīšanas datums vai daudzums var tikt mainīts pārdošanas pasūtījumā, kuram jau esat izveidojis pirkšanas pasūtījumu, lai izpildītu pieprasījumu. Šādā gadījumā vispārējās plānošanas aprēķins ģenerē vienu vai vairākus darbību ziņojumus, lai atjauninātu šo pirkšanas pasūtījumu. Jūs izlemjat, vai veikt ierosinātās izmaiņas.

Varat iestatīt veidu, kā ziņojumi tiek aprēķināti seguma grupai, kuru piesaistāt krājumam.

## <a name="select-action-messages"></a>Darbību ziņojumu atlasīšana

Lapā **Seguma grupas** varat atlasīt darbību ziņojumus, kurus vēlaties, lai sistēma ģenerē, kā arī atlasīt, uz kurām vajadzību grupām vai elementiem šie ziņojumi attiecas. Varat atlasīt šādus darbību ziņojumus.

| Ziņojums             | Apraksts                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Avanss**         | Ja atlasāt šo ziņojumu, sistēma ģenerē darbību ziņojumus, kad nepieciešams, lai pasūtījumus pārvietotu uz agrāku datumu. Laukā **Avansa dienu skaits** varat arī norādīt maksimālo dienu skaitu starp ieejas un izejas plūsmām, kad netiek veikta avansa darbība. |
| **Atlikt**        | Ja atlasāt šo ziņojumu, sistēma ģenerē darbību ziņojumus, kad nepieciešams, lai pasūtījumus pārvietotu uz vēlāku datumu. Laukā **Atlikšanas dienu skaits** varat norādīt maksimālo dienu skaitu starp ieejas un izejas plūsmām, kad netiek veikta atlikšanas darbība.       |
| **Samazināt**        | Ja atlasāt šo ziņojumu, tad ražošanas pasūtījumi, pirkšanas pasūtījumi un citas ieejas plūsmas transakcijas ir jāsamazina, lai novērstu pārliekus krājumu līmeņus.                                                                                                   |
| **Pieaugums**        | Ja atlasāt šo ziņojumu, tad ražošanas pasūtījumi, pirkšanas pasūtījumi un citas ieejas plūsmas transakcijas ir jāpalielina, lai novērstu krājumu iztrūkumus.                                                                                                    |
| **Atvasinātās darbības** | Ja atlasāt šo ziņojumu, darbību ziņojumi tiek izveidoti atvasinātajām prasībām, piemēram, darbības komponentu pasūtījumiem, lai izpildītu ražošanu.                                                                                                   |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]