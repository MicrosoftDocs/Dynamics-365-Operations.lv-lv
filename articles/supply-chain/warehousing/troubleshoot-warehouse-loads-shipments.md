---
title: Kravu veidošanas un nosūtīšanas problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar kravu veidošanu un nosūtīšanu programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994035"
---
# <a name="troubleshoot-load-building-and-shipments"></a>Kravu veidošanas un nosūtīšanas problēmu novēršana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar kravu veidošanu un nosūtīšanu programmā Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>Tiek parādīts šāds kļūdas ziņojums: "Nevar izveidot noslodzes rindu šai pasūtījuma rindai, jo tā ietver nederīgas krājumu dimensijas..."

### <a name="issue-description"></a>Problēmas apraksts

Tiek parādīts šāds kļūdas ziņojums, mēģinot izlaist atgriešanas pārdošanas pasūtījumu uz noliktavu:

> Nevar izveidot noslodzes rindu šai pasūtījuma rindai, jo tā ietver nederīgas krājumu dimensijas. Nevar atsaukties uz krājumu dimensijām, kas atrodas zem novietojuma dimensijas rezervāciju hierarhijā. Noņemiet nederīgās dimensijas no pasūtījuma rindas.

### <a name="issue-resolution"></a>Problēmas risinājums

Diemžēl prece pārdošanas atgriešanas procesam neatbalsta noslodzes apstrādi. Tāpēc nevar nodot atgriešanas pārdošanas pasūtījumu noliktavai.

Pārdošanas pasūtījumu transakcijās nevar atsaukties uz krājumu dimensijām, kas atrodas zem **Novietojuma** dimensijas rezervāciju hierarhijā. Risinājums ir noņemt nederīgās dimensijas no pasūtījuma rindas.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>Tiek parādīts šāds kļūdas ziņojums: "Viena no rindām jau ir kravā. Nevar izlaist uz noliktavu. "

### <a name="issue-description"></a>Problēmas apraksts

Ja manuāli izveidojat kravas vai iestatāt procesu tā, ka krava jau ir izveidota, pirms tiek veikta pārdošanas pasūtījuma rindas ievade, pieņēmums ir tāds, ka nākamā izpilde tiks veikta manuāli, un tiks izmantota maršruta un vērtējums no kravas.

Citā iespējamajā scenārijā jūs mēģināt veikt automātisku izlaišanu noliktavā, bet kopuma procesam neizdevās izveidot darbu. Tāpēc atvērts sūtījums vai krava joprojām tiek izveidota. Šis atvērtais sūtījums vai krava pēc tam bloķē sekojošos mēģinājumus automātiski nodot pasūtījumu, līdz jūs vai nu dzēšat atvērto sūtījumu vai kravu, vai manuāli pārstrādājiet kopumu.

### <a name="issue-resolution"></a>Problēmas risinājums

Var veikt izlaišanu no pārdošanas pasūtījuma lapas vai automātiski izlaist no izlaišanas pārdošanas pasūtījuma lapas, tikai tad, ja pirms nodošanas noliktavai neeksistē neviena krava. Krava tiks automātiski izveidota pēc kopuma apstrādes.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>Tiek parādīts šāds kļūdas ziņojums: "Nevar apstrādāt piegādes pavadzīmes labojumu. Piegādes pavadzīmē ir ietverti tikai tie krājumi, kas ir pakļauti noliktavas pārvaldības procesiem, jo tie netiek atbalstīti ar Piegādes pavadzīmes labojumu."

### <a name="issue-description"></a>Problēmas apraksts

Pēc tam, kad ir iegrāmatota piegādes pavadzīme, to nevar atcelt, jo poga **Atcelt** nav pieejama. Jūs arī nevarat labot piegādes pavadzīmi. Ja mēģināt, tiek parādīts šis kļūdas ziņojums.

### <a name="issue-resolution"></a>Problēmas risinājums

Lai labotu grāmatotās pavadzīmes krājumiem, kas ir iespējoti papildu noliktavas pārvaldībai (WMS), jāveic grāmatošana no kravas, nevis tieši no pasūtījuma.

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>Kā var izveidot darbu no izejošajām kravām, nevis no kopumiem?

### <a name="issue-description"></a>Problēmas apraksts

Lūk, viens no veidiem, kā reproducēt šo problēmu.

1. izveidojiet izejošo kravu, izmantojot pārdošanas pasūtījumu vai pārsūtīšanas pasūtījumu.
2. Izlaiž noslodzi nosūtīšanai uz noliktavu.
3. Ievērojiet, ka izdošanas darbs vēl nav izveidots.

### <a name="issue-resolution"></a>Problēmas risinājums

Ja, izlaižot noslodzi, darbs ir jāveido nekavējoties, ir attiecīgi jākonfigurē laidiena veidne. Laidiena veidnē iestatiet šādas opcijas uz *Jā*:

- Automatizēt kopuma izveidi
- Apstrādāt kopumu, to pārvietojot uz noliktavu
- Automatizēt kopuma izlaidi

## <a name="i-cant-re-release-a-partially-shipped-load"></a>Nav iespējams atkārtoti izlaist daļēji nosūtītu noslodzi.

### <a name="issue-description"></a>Problēmas apraksts

Nevar izlaist daļēji nosūtītu kravu uz noliktavu. Kad veicat izlaišanu uz noliktavu, parādās ziņojums "Operācija pabeigta", bet nekas nenotiek, un atlikušajam daudzumam netiek izveidots neviens darbs. Šī problēma rodas, kad izmantojat transportēšanas noslodzes funkcionalitāti un ir nepilnīga rezervācija.

### <a name="issue-resolution"></a>Problēmas risinājums

[KB problēma 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Daļēji nosūtītas kravas var atkārtoti ielikt kopumā un atkārtoti apstrādāt") ir fiksēta [laidienā 10.0.15](../get-started/whats-new-scm-10-0-15.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]