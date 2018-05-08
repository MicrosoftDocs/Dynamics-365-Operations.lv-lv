---
title: "Pieejamās aprūpes akta pārskatu ģenerēšana"
description: "Ir pieejama funkcionalitāte, kura palīdz darba devējiem, kam ir nepieciešams sekot līdzi formās 1095-B un 1095-C ziņotajai informācijai, ievērojot pieejamās aprūpes akta (Affordable Care Act — ACA) prasības daļā Darba devēja mandāts. Ņemiet vērā, ka šī funkcionalitāte ir iespējota tikai juridiskajām personām Amerikas Savienotajās Valstīs."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 1994edc5d6c932be3a285f9bb328a05504c90f07
ms.contentlocale: lv-lv
ms.lasthandoff: 03/08/2018

---
# <a name="generate-affordable-care-act-reports"></a>Pieejamās aprūpes akta pārskatu ģenerēšana

[!include [banner](includes/banner.md)]

Ir pieejama funkcionalitāte, kura palīdz darba devējiem, kam ir nepieciešams sekot līdzi formās 1095-B un 1095-C ziņotajai informācijai, ievērojot pieejamās aprūpes akta (Affordable Care Act — ACA) prasības daļā **Darba devēja mandāts**. Ņemiet vērā, ka šī funkcionalitāte ir iespējota tikai juridiskajām personām Amerikas Savienotajās Valstīs.

## <a name="getting-started"></a>Darba sākšana
Uzsākot sekot līdzi informācijai, ko ziņot formās 1095-B un 1095-C, jums vispirms ir jāizveido viena vai vairākas pieejamās aprūpes seguma grupas. Šīs pieejamās aprūpes seguma grupas tiks izmantotas, lai norādītu darbiniekam nodrošināto seguma piedāvājumu, darbinieka zemāko ikmēneša iemaksu daļu (ja izmaksas pārsniedz federālās nabadzības slieksni), kā arī darba devēja izmantoto drošo patvērumu, ja piemērojams. Izmantojot pieejamās aprūpes akta grupas, jūs varat pārvaldīt informāciju par šiem laukiem, un nav nepieciešamības aiztikt katra darbinieka ierakstu, kur nosacījumi ir vienādi. Turklāt pieejamās aprūpes seguma grupas var ērti piešķirt vienam vai vairākiem darbiniekiem, izmantojot lapas funkcionalitāti Piešķirt masveidā.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Segumu grupas vairāku versiju uzturēšana
Jebkurai seguma grupai varat uzturēt vairākas versijas, tādējādi varat veikt izmaiņas, kas uztur aktuālu grupas informāciju, bez nepieciešamības izveidot jaunu grupu un atkārtoti piešķirt tai darbiniekus, ja kaut kas mainās jūsu organizācijā vai piedāvātajās priekšrocībās. 

Kad esat izveidojis nepieciešamās pieejamās aprūpes seguma grupas, varat izlemt šim grupām masveidā piešķirt darbiniekus, izmantojot lapas funkcionalitāti **Masveida piešķiršana**, vai varat doties uz katra darbinieka ierakstu un norādīt, vai ir jāseko līdzi ACA informācijai un vai tā ir jāziņo par attiecīgo darbinieku, kā arī piešķirt šo darbinieku kādai pieejamās aprūpes seguma grupai.

Ja kādam darbiniekam informācija par pieejamās aprūpes segumu nav jāizseko vai jāziņo, piemēram, ja tas ir nepilnas slodzes darbinieks, tad lauka **Pārskata segums** vērtība ir jāiestata uz Nē. Lai gan katrs darbinieks, kura ACA informācija ir jāizseko, ir jāpiešķir kādai pieejamās aprūpes seguma grupai, opcijas **Seguma piedāvājums**, **Darbinieka izmaksu daļa** un **Drošais patvērums** joprojām varat mainīt jebkuram mēnesim — vai mēnešiem —, kuriem varētu būt nepieciešamas atšķirīgas vērtības nekā pieejamās aprūpes seguma grupā ierakstītās.

Lai jebkurai no pieejamās aprūpes seguma grupas vērtībām ievadītu izņēmumus, noklikšķiniet uz pieejamās aprūpes seguma saites lapā Detalizēta informācija par nodarbināto, kas atrodas cilnes Nodarbinātība sadaļā Papildinformācija.

## <a name="reporting-health-care-coverage"></a>Veselības aprūpes seguma ziņošana
Papildus iespējai sekot līdzi tam, vai pilnas slodzes darbiniekam tika piedāvāts jebkāds veselības apdrošināšanas segums, ja darba devējs piedāvā darba devēja sponsorētu paša apdrošināšanu veselības segumu, kuram darbinieks ir reģistrējies (neatkarīgi no tā, vai tas ir pilna laika vai nepilna laika darbinieks), tad ir jāziņo papildu informācija formā 1095-C. Katrs darbinieks (tostarp apgādājamie), uz ko attiecas darba devēja sponsorētie atvieglojumu plāni, ir jāietver pārskatā par tiem mēnešiem, kuros viņiem bija spēkā šis segums. 

Katram atvieglojumu plānam varat norādīt, vai tas ir jāziņo, atzīmējot izvēles rūtiņu **Norādāms ACA pārskatā**.

Turklāt, ja darbinieks ir izvēlējies atvieglojumu plānā ietvert kādus no saviem apgādājamiem, tad jūs katram darbiniekam lapā Atvieglojumu uzturēšana varat norādīt datumus, kad apgādājamais bija ietverts. Lai norādītu, ka atvieglojumu plānā ir ietverts apgādājamais, kopsavilkuma cilnes Apgādājamie darbību rūtī izvēlieties pogu Rediģēt.

Lapā **Apgādājamā seguma datumu pārvaldnieks** varat norādīt datumus, kad apgādājamais bija ietverts atvieglojumu plānā. Ievadot datumus šajā lapā, lapā **Atvieglojumu uzturēšana** tiek automātiski atzīmēta izvēles rūtiņa **Segts**.

## <a name="generate-1095b-and-1095c-forms"></a>Ģenerēt formas 1095B un 1095C
Šī produkta ietvaros varat arī ģenerēt formas 109-B un 1095-C un tās izdalīt katram no saviem darbiniekiem. No sistēmas var arī elektroniski ģenerēt 1095-C un atbilstošos 1094-C pārsūtīšanas failus, kurus var izmantot, lai sūtītu uz IRS.  

Kad ģenerējat 1095-C formu, ievadiet arī atbilstošo kalendāro vai taksācijas gadu, it kā vēlētos izdrukāt divu lapu vai trīs lapu formu. Trīs lapu forma ir nepieciešama tikai tad, ja darba devējs nodrošināja paša apdrošinātu segumu un darbiniekam ir vairāk par sešiem ietvertajiem apgādājamajiem, ieskaitot pašu darbinieku. Ģenerējot divu lapu formu, sistēma automātiski konstatē, vai darbiniekam ir vairāk par 6 ietvertajiem apgādājamajiem, un neietver šo darbinieku, ģenerējot formu. Turklāt, ģenerējot trīs lapu formu, sistēmas ietver tikai tos darbiniekus, kuriem ir vairāk par sešiem ietvertajiem apgādājamajiem.

## <a name="viewing-information"></a>Informācijas skatīšana
Lapu **Pieejamās aprūpes segums nodarbinātajam** varat izmantot, lai redzētu, kuri darbinieki ir piešķirti kurai seguma grupai, kuri darbinieki nav jāietver pārskatā, un kuri darbinieki nav piešķirti.

Ja kāda no pieejamās aprūpes seguma grupas noklusējuma vērtībām ir pārrakstīta, pie mainītās vērtības tiek rādīta zvaigznīte. Ja vērtības visiem 12 mēnešiem ir vienādas un nav tikušas pārrakstītas, tad vērtība tiks drukāta kolonnā **Visi 12 mēneši**.

Varat arī izmantot uzziņu logu, lai saprastu, kuri darbinieki ir atzīmēti kā ACA pārskatos nenorādāmi — tas nozīmē, ka jums nav nepieciešams sekot līdzi tam, vai šiem darbiniekiem ir piedāvāts segums, un viņiem nav nepieciešams izsniegt 1095-C formas gada beigās. Laukā **Filtrēt pēc** atlasot vērtību **Nav norādāms ACA pārskatā**, varat ģenerēt sarakstu ar visiem darbiniekiem, kas ir atzīmēti kā tādi, kuriem nav jāsaņem 1095-C forma.

Papildus tam, ka varat apskatīt sarakstu ar darbiniekiem, kas nav norādāmi ACA pārskatā, varat arī skatīt darbiniekus, kuri nav piešķirti (lauks **ACA pārskata segums** ir tukšs) vai kuri ir piešķirti kādai pieejamās aprūpes seguma grupai, kuras darbība ir beigusies tajā gadā, kas ir atlasīts laukā **Gads**.

Sarakstus ar darbiniekiem, kas tika ģenerēti, izmantojot filtrēšanas opcijas, varat eksportēt uz programmu Excel.

Ja nepieciešams ziņot par ietvertajām personām, jo kā darba devējs jūsu nodrošināt paša apdrošinātu segumu, tad varat skatīt arī jebkurus apgādājamos, kuri ir iekļauti atvieglojumu plānos, kas ir atzīmēti kā **Norādāms ACA pārskatā**, darbību rūts joslā atlasot darbību Skatīt apgādājamo segumu.

**Piezīme.** Uzziņu lokā tiek rādīti tikai atvieglojumi, kuru plāns ir atzīmēts kā **Norādāms ACA pārskatā**.

