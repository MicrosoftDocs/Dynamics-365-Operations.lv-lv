---
title: Pārskats par kravu plānošanu, izmantojot konsolidēšanu pārkraušanas punktā
description: Šajā rakstā ir aprakstīts līdzeklis sūtījumu konsolidēšanai pārkraušanas punktā, kad preces no dažādām noliktavām piegādājat tam pašam debitoram vai kad preces no vairākiem kreditoriem saņemat tajā pašā noliktavā.
author: MarkusFogelberg
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f0e7ae8db62ce374b991ac5f117e3d1d33534df
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828470"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>Pārskats par kravu plānošanu, izmantojot konsolidēšanu pārkraušanas punktā

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts līdzeklis sūtījumu konsolidēšanai pārkraušanas punktā, kad preces no dažādām noliktavām piegādājat tam pašam debitoram vai kad preces no vairākiem kreditoriem saņemat tajā pašā noliktavā.

Kad preces no dažādām noliktavām piegādājat tam pašam debitoram vai kad preces no vairākiem kreditoriem tiek piegādātas uz to pašu noliktavu, var būt noderīgi sūtījumus konsolidēt vienā pārkraušanas punktā.

## <a name="building-loads"></a>Kravu plānošana
Lai varētu izmantot pārkraušanas punkta konsolidāciju, ir jāiespējo opcija **Tranzīta plānošana** lapā **Transportēšanas pārvaldības parametri**. Jums ir arī jāizveido pārkraušanas punkti, kur notiks konsolidēšana. Nākamajā diagrammā ir parādīts pārkraušanas punkta konsolidācijas piemērs. Šajā gadījumā pārdošanas pasūtījumi no dažādām noliktavām tiek piegādāti vienam un tam pašam debitoram. Pamata kravas tiek veidotas, pamatojoties uz pārdošanas pasūtījumiem parastajā veidā, izmantojot lapu **Kravu plānošanas rīks**. Lai divas kravas konsolidētu vienā pārkraušanas punktā, pirms tās tiek piegādātas debitoram, lapas **Kravu plānošanas rīks** laukā **Transportēšana** atlasiet vienumu **Pārkraušanas punktu konsolidācija**. Kad katrai kravai atlasāt pareizo pārkraušanas punktu, kravām šis pārkraušanas punkts tiek norādīts kā “nodošanas” galamērķis. Jums būs arī divas “transportēšanas pieprasījuma rindas” sadaļā **Piedāvājums un pieprasījums**, lapā **Kravu plānošanas rīks**. Pēc tam šīs abas rindas varat pievienot jaunai kravai. Šai jaunajai kravai būs abas pārdošanas pasūtījuma rindas, kā arī būs pārkraušanas punkts kā “saņemšanas” adrese un debitors A kā “nodošanas” galamērķis. Pēc tam šīs trīs kravas ir gatavas vērtēšanai un maršrutēšanai kā jebkura cita krava. Jūs varat norādīt jebkādu sūtījumu pārvadātāju, ko sistēma ierosina katrai kravai. [![Pārkraušanas punktu konsolidācija](./media/hubconsol.jpg)](./media/hubconsol.jpg) Šo pašu metodi varat arī izmantot, lai konsolidētu kravas no vairākiem pārsūtīšanas pasūtījumiem. Šajā gadījumā debitors A iepriekšējā diagrammā ir noliktava. Vai varat konsolidēt kravas no vairākiem pirkšanas pasūtījumiem, kur kravas no dažādiem kreditoriem tiek piegādātas uz to pašu noliktavu. Jums var būt vairāki konsolidācijas pārkraušanas punkti, un varat konsolidēt vairākos pārkraušanas punktos vairākām kravām, kas tiek piegādātas no dažādām noliktavām. Kad esat izveidojis savas pamata kravas un izmantojis pārkraušanas punktu konsolidēšanas opciju, jūs veidojat jaunu kravas, izmantojot konsolidēto transportēšanas pieprasījumu rindas. Pēc tam jūs vērtējat un maršrutējat savas kravas.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]