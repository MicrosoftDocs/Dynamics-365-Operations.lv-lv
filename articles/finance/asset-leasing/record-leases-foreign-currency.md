---
title: Nomu reģistrēšana ārvalstu valūtās
description: Šajā rakstā ir izskaidrots, kā ierakstīt nomas naudu valūtā, kas nav uzskaites vai pārskata valūta.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 56c15e648d6aa515192a6f41ba06df6405ca79f2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878107"
---
# <a name="record-leases-in-foreign-currencies"></a>Nomu reģistrēšana ārvalstu valūtās

[!include [banner](../includes/banner.md)]

Līdzekļu līzinga konti nomai, kas ir valūtās, kas nav uzskaites valūta vai pārskata valūta, ir izveidoti **Virsgrāmatas iestatīšanas** lapā. Visas nomas jāievada to darījumu valūtā. Citiem vārdiem sakot, tie jāievada valūtā, kas norādīta nomas līgumā. Šajā rakstā ir izskaidrots, kā ierakstīt nomas naudu valūtā, kas nav uzskaites vai pārskata valūta.

Ja ievadāt nomu ārvalstu valūtā, LLT tiek nolietots gan uzskaites valūtā, gan pārskata valūtā. Šīs valūtas tiek konfigurētas lapā **Virsgrāmatas iestatījumi**. Šo darbību izmanto arī pamatlīdzekļos. Kad jūs izveidojat nomu ārzemju valūtā, laukā **Valūta** atlasiet darījumu valūtu.

Uzskaites valūtas maiņas kurss ir noklusējuma vērtība **uzskaites valūtas maiņas kursa** laukā. Pārskata valūtas maiņas kurss ir noklusējuma vērtība **pārskata valūtas maiņas kursa** laukā. Šie maiņas kursi bija spēkā nomas sākuma datumā. Lauki **Uzskaites valūtas maiņas kurss** un **Pārskata valūtas maiņas kurss** ir kopsavilkuma cilnē **Finanšu un pārskatu maiņas informācija**, kas atrodas lapā **Nomas informācija**.

1. Atzīmējiet izvēles rūtiņu **Fiksēts kurss**, lai ignorētu automātiski ievadīto maiņas kursu, un pēc tam ievadiet jauno kursu.
2. Citos laukos ievadiet informāciju, kas nepieciešama nomai, un pēc tam atlasiet **Izveidot grafikus**.
3. Jaunajā lapā **Nomas informācija** atlasiet **Grāmatas**.
4. Lapas **Nomas grāmata** cilnē **Finanšu un pārskatu maiņas kursa informācija** pārbaudiet lauku **Uzskaites valūtas vērtības sākotnējās līdzekļa lietošanas tiesības** un **Pārskata valūtas sākotnējās līdzekļa lietošanas tiesības**. Katrs no šiem laukiem parāda tulkoto LLT bilanci atbilstošajā valūtā. Šie lauki tiek atjaunināti ik reizi, kad maināt finansiālu informāciju. Atlasiet **Izveidot grafikus**, pirms apstiprināt maksājumu grafiku.

    Sākotnējais atzīšanas žurnāla ieraksts reģistrē LLT, kas izmanto nomas maksai norādītos valūtas maiņas kursus. Žurnāla ierakstā ir iekļautas arī lauku **Uzskaites valūtas sākotnējās līdzekļa lietošanas tiesības** un **Pārskata valūtas sākotnējās līdzekļa lietošanas tiesības**.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Ārvalstu valūtas nomu turpmākā novērtēšana

Nolietojuma grafiks parāda prognozēto nolietojuma izdevumu summas pārskata valūtā, uzskaites valūtā un darījuma valūtā.

Lai skatītu LLT bilances un nolietojuma summas pārskata valūtā vai uzskaites valūtā, atveriet lapu **Līdzekļa nolietojuma grafiks** un atzīmējiet izvēles rūtiņu **Rādīt uzskaites valūtas summas** vai **Rādīt pārskata valūtas summas**.

Kad tiek veidoti nolietojuma izdevumu žurnāla ieraksti nomai, kas izteikta ārzemju valūtā, ieraksts izmanto valūtas maiņas kursus, kas norādīti nomā. Tas izmanto arī lauku **Uzskaites valūtas sākotnējās līdzekļa lietošanas tiesības** un **Pārskata valūtas sākotnējās līdzekļa lietošanas tiesības** vērtības.

Galīgo nolietojuma izdevumu summu var aprēķināt, izmantojot nedaudz atšķirīgu maiņas kursu, lai LLT būtu pilnībā nolietots gan uzskaites valūtā, gan pārskata valūtā.

Ja noma pārklasificēta kā **Atliktā nomas maksa**, sistēma automātiski notīra uzskaites un pārskata valūtas maiņas kursus, ja tie jau ir definēti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
