---
title: Amati
description: Šajā tēmā aprakstīti konceptuāli elementi, kurus pozīcija var iekļaut. Tajā sniegti arī piemēri, kas parāda, kā varat izmantot šos elementus savā organizācijā.
author: twheeloc
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bb7582165f49c40d294acd3cf804fe89782936c4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689443"
---
# <a name="positions"></a>Amati


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīti konceptuāli elementi, kurus pozīcija var iekļaut. Tajā sniegti arī piemēri, kas parāda, kā varat izmantot šos elementus savā organizācijā.

Pirms amata izveides ir jāiestata darbs. Detalizēta informācija par amatu, piemēram, atlīdzības reģions, darbinieku piešķiršana, pozīcijas ilgums un pārskata attiecības, ir spēkā stāšanās datums.

## <a name="general-information"></a>Vispārīgā informācija

Izveidojot pozīciju, jums ir jāatlasa darbs. Šī informācija automātiski tiks aizpildīta no atlasītā darba:

- Apraksts
- Amats
- Pilnas slodzes ekvivalents
- Amatu saime

Amata nosaukums tiek izmantots, lai atsaukties uz darbinieka amatu. (Netiek lietots darbinieka sarakstā iekļautais amats.) Tāpēc amatu nosaukumi jāstandarta pēc iespējas vairāk.

> [!NOTE]
> Darbinieku nevar piešķirt amatam datumā, kas ir pirms piešķiramā pieejamā datuma.
>
> Parametrs cilnē **Pozīcijas** lapā **Cilvēkresursu kopīgie parametri** kontrolē darbinieka piešķires uzvedību. Atlasiet vienu no šīm vērtībām:
>
> - **Vienmēr** — darbiniekus jauniem amatiem var piešķirt amatu izveides brīdī. Izveidojot amatus, datums un laiks **Pieejams piešķirei** cilnē **Vispārīgi** lapā **Amati** tiek automātiski iestatīti uz izveides datumu un laiku.
> - **Nekad** — darbiniekus jauniem amatiem nevar piešķirt amatu izveides brīdī. Ja izvēlaties šo opciju, jums jāatver lapa **Pozīcija** katrai jaunai pozīcijai, kad tā ir pieejama. Pēc tam cilnē **Vispārīgi** ievadiet datumu **Pieejams piešķirei**, lai iespējotu darbinieka piešķiri. Atlasot šo opciju, darbinieka piešķires datums pēc noklusējuma tiks iestatīts uz **Nekad**, kad mēģināsiet piešķirt darbinieku.

## <a name="position-duration"></a>Amata ieņemšanas ilgums

Katrs amats ir efektīvs noteiktam laika daudzumam, kas tiek saukts par ilgumu. Piemēram, vasaras amatu ieņemšanas ilgums var būt no 2021. gada 1. maija līdz 2021. gada 31. augustam. Aktivizēšanas datums ir datums, kad pozīcija sistēmā ir aktīva. Pensionēšanās datums ir datums, kad pozīcija sistēmā vairs nav aktīva.

Ievērojiet, ka ne pieejamais norīkojuma datums, ne darbinieka piešķires datums nevar būt pirms aktivizēšanas datuma. Pozīcija nav uzskatīta par aktīvu, kamēr nav sasniegts aktivizēšanas datums. Turklāt darbinieka piešķiri nevar pagarināt pēc amata aiziešanas pensijā datumu.

## <a name="reports-to-position"></a>Pārskati par amatu

Amati ir nozīmīgi organizācijas hierarhijas zemāko līmeņu elementi. Lapā **Pozīcija** varat norādīt amatu, kuram ir pakļauts šis amats. Kad piešķirat darbinieku amatam, kas ir pakļauts citam amatam, tiek izveidotas pakļautības attiecības starp darbiniekiem, kas ir piešķirti šiem diviem amatiem. Piemēram, pozīciju 000220 par pozīciju 000300. Kims Akers ir piešķirts amatam 000220, un Sandžejs Patels ir piešķirts amatam 000300. Tādēļ Kim Akers ziņo Sanjay Patel.

> [!TIP]
> Pārskati par ziņojumiem tiek izmantoti visā sistēmā, lai noteiktu, kas ir darbinieka vadītājs. Iepriekšējā piemērā, ja vadītāja loma sistēmā ir piešķirta Sanjay Patel, viņš redzēs Kim Akers kā tiešo pārskatu vadītāja pašapkalpošanās sistēmā. Pārskata attiecības var izmantot arī darbplūsmas maršrutēšanas noteikumu un kontrolsaraksta uzdevumu veidojiet.

## <a name="relationships"></a>Saistības

Ja jūsu organizācija izmanto matricas hierarhiju vai citu pielāgotu hierarhiju, varat iestatīt pozīciju hierarhiju tipus. Pēc tam varat pievienot pārskatu attiecības pozīcijām katram iestatītā hierarhijas tipam. Piemēram, Lorija Penora ir uzņēmuma Adventure Works ģenerāldirektore un ir piešķirta amatam **Ģenerāldirektors**. Lorija vada logrīku notīrīšanai paredzēta produkta izstrādi. Viņa prasa, lai grāmatvedis palīdz viņai ar finansēm. Tāpēc viņa ir pieņēmusi Kimu Akersu kā grāmatvedi. Kims ir tieši pakļauts Sandžajam Patelam, taču strādā arī kopā ar Loriju Penori darbā, kas saistīts ar logrīku notīrīšanas produkta izstrādes finanšu datiem.

Iepriekšējam piemēram ir jāveic tālāk norādītie uzdevumi, lai iestatītu darba attiecības starp Kimu Akersu un Loriju Penori.

1. Izveidojiet pielāgotu amatu hierarhijas tipu, tas ir nosaukts **Logrīks**, lai izveidotu hierarhiju, kurā ir ietverti amati, kas ir saistīti ar logrīku notīrīšanas produkta izstrādi.
2. Norādiet, ka Kima amats ir pakļauts amatam **Ģenerāldirektors** hierarhijā **Logrīks**.
3. Izmantojiet amatu hierarhiju, lai skatītu amatu pakļautības struktūru. Ja jums ir vairākas amatu hierarhijas, varat skatīt katra hierarhijas tipa hierarhiju amatu hierarhijā. Varat arī meklēt amatu pēc amata ID vai tā darbinieka vārda, kurš ir piešķirts šim amatam. Amatu hierarhija ir organizācijas hierarhija.

## <a name="labor-union"></a>Arodbiedrība

Varat ierakstīt, vai pozīcijai ir nepieciešams arodbiedrības līgums un kāda arodbiedrība tiek izmantota. Varat arī saistīt līgumu ar juridisku personu.

## <a name="financial-dimensions"></a>Finanšu dimensijas

Izveidojot amata finanšu dimensiju, jānorāda juridiskā persona. Varat atlasīt noklusējuma dimensijas katrai dimensijai atsevišķi. Alternatīvi varat arī atlasīt sadales veidni, lai automātiski aizpildītu noklusējuma dimensijas. Sadales veidne sniedz arī opciju sadalīt summas starp vairākām dimensiju vērtībām.
