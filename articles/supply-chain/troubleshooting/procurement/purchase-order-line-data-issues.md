---
title: Pirkšanas pasūtījuma rindas datu neatbilstības
description: Pirkšanas pasūtījumu rindās jūs redzat datu neatbilstības vai datu bojāšanu.
author: SmithaNataraj
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: PurchLineManualCorrection, PurchTable, PurchLine, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ee2cb9a07c8a00a92c71e3e99d8ec20aa27fb20e
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100783"
---
# <a name="purchase-order-line-data-discrepancies"></a>Pirkšanas pasūtījuma rindas datu neatbilstības

## <a name="symptoms"></a>Simptomi

Pārbaudot pirkšanas pasūtījuma rindas, ievērojat vienu vai vairākas no šīm problēmām:

- Pirkšanas pasūtījuma rindas atgādinājumos (piegāde vai rēķins) ir datu neatbilstība vai bojājums.
- Pirkšanas pasūtījuma rindā vai virsraksta statusā ir bojāts virsraksts.
- Nevar izrakstīt rēķinu pirkšanas pasūtījumam, jo, piemēram, jūs saņemat vienu vai vairākus no šiem kļūdu ziņojumiem:

    - "Apturēts (kļūda): darbība jau ir grāmatota."
    - "Daudzumu nevar iekļaut rēķinā, jo krājumu darbības ar statusu Saņemts ir nepietiekamas."
    - "Nepietiek krājumu darbību ar statusu "Nopirkts" krājuma daudzumam%0%1.

- Nevar pabeigt vai slēgt pirkšanas pasūtījumu, piemēram, dēļ kāda no šīm problēmām:

    - Poga **Pabeigt** nav pieejama.
    - Pirkšanas pasūtījuma rindas pasūtīto daudzumu pirkšanas pasūtījumam, kas ir apstiprināts un saņemts stāvoklī, nevar atcelt.

## <a name="cause"></a>Iemesls

Šīs problēmas parasti izraisa datu bojāšana vai neatbilstība atgādinājuma daudzumos vienai vai vairākām pirkšanas pasūtījuma rindām.

## <a name="resolution"></a>Novēršana

Šīs problēmas parasti var labot, atjauninot pirkšanas statusu, piegādes atgādinājumus un/vai rēķina atlikumus attiecīgajām pirkšanas pasūtījuma rindām, kā aprakstīts šādā procedūrā.

1. Manuāli dodieties **uz Sagādes un avotu \> periodisko \> uzdevumu tīrīšanai \> labojiet pirkšanas pasūtījuma rindas**.
1. Laukā **Pirkšanas** pasūtījums atrodiet un atlasiet pirkšanas pasūtījumu, kas sniedz problēmas.
1. Sadaļā Pirkšanas **pasūtījuma** rindas atlasiet rindu, kurā tika atrasta neatbilstība.
1. **Sadaļā Krājumu darbības** pārbaudiet parādītos datus. Ja jūs ievērojat jebkādas neatbilstības starp pirkšanas pasūtījuma rindu un tās krājumu darbībām, izvēlieties vienu no šīm komandām darbību rūtī atkarībā no tā, kur redzat neatbilstības:

    - **Pārrēķināt \> piegādes atlikumu pārrēķinu** – automātiski atjaunināt pirkšanas pasūtījuma rindu un virsraksta statusus. Šī funkcija darbojas tikai uzkrāto pirkšanas pasūtījumu rindām (t.i., rindām, kurās krājums ir uzkrāts krājums). Pašlaik netiek atbalstītas krājumus, kas nav uzkrātas, un pieļaujamā svara krājumus.
    - **Pārrēķināt \> rēķina atlikumu** - automātiski atjaunināt pirkšanas pasūtījuma rindu un virsraksta statusus. Šī funkcija darbojas tikai uzkrāto pirkšanas pasūtījumu rindām (t.i., rindām, kurās krājums ir uzkrāts krājums). Pašlaik netiek atbalstītas krājumus, kas nav uzkrātas, un pieļaujamā svara krājumus.
    - **Pārrēķināt \> statusu** Pārrēķināt - pārrēķināt atlasītās rindas statusu. Šis aprēķins ir balstīts uz esošo loģiku. Tāpēc pirkšanas pasūtījuma virsraksta statuss tiks atjaunināts pēc vajadzības, pamatojoties uz jaunā pirkšanas pasūtījuma rindas statusu.

1. Ja joprojām redzat neatbilstības atgādinājuma daudzumos, varat izmantot šādus laukus, lai tos rediģētu tieši pēc vajadzības:

    - Atlicis piegādāt
    - Krājuma piegādes atlikums
    - Rēķina atlikums
    - Krājuma rēķina atlikums
