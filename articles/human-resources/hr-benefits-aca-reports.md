---
title: Pieejamās aprūpes akta (ACA) pārskatu ģenerēšana
description: Pieejamās aprūpes akta (ACA) pārskatu sniegšana ģenerē formas 1095-B un 1095-C, atbalstot Pieejamās aprūpes akta daļu **Darba devēja mandāts**.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 498705b86b705c70e7e84e3a03e459d02dfcb88f5cfbd4b7ef27e18173c2a1e0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774178"
---
# <a name="generate-aca-reports"></a>ACA pārskatu ģenerēšana

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Pieejamās aprūpes akta (ACA) pārskatu sniegšana ģenerē formas 1095-B un 1095-C, atbalstot Pieejamās aprūpes akta daļu **Darba devēja mandāts**.

> [!NOTE]
> ACA pārskatu sniegšana ir iespējota tikai juridiskajām personām Amerikas Savienotajās Valstīs.

## <a name="getting-started"></a>Darba sākšana

Lai sekotu līdzi informācijai formām 1095-B un 1095-C, jums vispirms ir jāizveido viena vai vairākas pieejamās aprūpes seguma grupas. Pieejamās aprūpes seguma grupas norāda:

- Darbinieka seguma piedāvājumu
- Darbinieka daļa no zemāko mēneša prēmiju izmaksām, ja izmaksas pārsniedz federālo nabadzības slieksni
- Darba devēja izmantoto drošo patvērumu, ja piemērojams

Pieejamās aprūpes seguma grupas ļauj pārvaldīt informāciju par šiem laukiem, un nav nepieciešamības mainīt katra darbinieka ierakstu, kur nosacījumi ir vienādi. Varat viegli piešķirt pieejamās aprūpes seguma grupas vienam vai vairākiem darbiniekiem, izmantojot lapas funkcionalitāti **Piešķirt masveidā**.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Segumu grupas vairāku versiju uzturēšana

Varat uzturēt jebkuras segumu grupas vairākas versijas. Šī funkcionalitāte ļauj veikt izmaiņas, neveidojiet jaunu grupu un atkārtoti nepiešķirot tai darbiniekus. 

Kad esat izveidojis ACA seguma grupas, varat masveidā piešķirt grupas darbiniekiem ar opciju **Piešķirt masveidā**. Varat arī atsevišķi norādīt, vai izsekot un ziņot ACA informāciju, un piešķirt darbinieku pieejamās aprūpes grupai.

Jums nav jāizseko noteikta ACA seguma informācija, piemēram, nepilna laika darbiniekiem. Šajā gadījumā iestatiet lauku **Pārskata segums** uz **Nē**. Lai gan katram darbiniekam ir jāpiešķir izsekošanas ACA informācija pieejamās aprūpes seguma grupai, tomēr mēnešiem varat mainīt tālāk norādītās opcijas ar dažādām vērtībām:

- **Vajadzību piedāvājums**
- **Darbinieka izmaksu daļa**
- **Drošais patvērums**

Lai jebkurai no pieejamās aprūpes seguma grupas vērtībām ievadītu izņēmumus, atlasiet saiti **Pieejamās aprūpes segums** lapā **Detalizēta informācija par nodarbināto**, kas atrodas cilnes **Nodarbinātība** sadaļā **Papildinformācija**.

## <a name="reporting-health-care-coverage"></a>Veselības aprūpes seguma ziņošana

Papildus iespējai sekot līdzi tam, vai pilnas slodzes darbiniekiem tika piedāvāts jebkāds veselības apdrošināšanas segums, ja darba devējs piedāvā darba devēja sponsorētu paša apdrošināšanu veselības segumu, kuram darbinieks ir reģistrējies (neatkarīgi no tā, vai tas ir pilna laika vai nepilna laika darbinieks), tad ir jāziņo papildu informācija formā 1095-C. Katrs darbinieks (tostarp apgādājamie), uz ko attiecas darba devēja sponsorētie atvieglojumu plāni, ir jāietver pārskatā par tiem mēnešiem, kuros viņiem bija spēkā šis segums. 

Katram atvieglojumu plānam varat norādīt, vai tas ir jāziņo, atzīmējot izvēles rūtiņu **Norādāms ACA pārskatā**.

Turklāt, ja darbinieks ir izvēlējies atvieglojumu plānā ietvert kādus no saviem apgādājamiem, tad jūs katram darbiniekam lapā **Atvieglojumu uzturēšana** varat norādīt datumus, kad apgādājamais bija ietverts. Lai norādītu, ka atvieglojumu plānā ir ietverts apgādājamais, kopsavilkuma cilnes **Apgādājamie** darbību rūtī izvēlieties pogu **Rediģēt**.

Lapā **Apgādājamā seguma datumu pārvaldnieks** varat norādīt datumus, kad apgādājamais bija ietverts atvieglojumu plānā. Ievadot datumus šajā lapā, lapā **Atvieglojumu uzturēšana** tiek automātiski atzīmēta izvēles rūtiņa **Segts**.

## <a name="generate-1095-b-and-1095-c-forms"></a>Formu 1095-B un 1095-C ģenerēšana

Šī produkta ietvaros varat arī ģenerēt formas 1095-B un 1095-C un tās izdalīt katram no saviem darbiniekiem. Sistēma var arī elektroniski ģenerēt 1095-C formas un 1094-C IRS pārsūtāmos failus.  

Ģenerējot formu 1095-C, ievadiet attiecīgo taksācijas gadu un norādiet, vai ir jāaizklāj sociālās apdrošināšanas numurs. Ja drukājat formas 1095-C vairāk nekā 500 darbiniekiem, jūs saņemsiet vairāk nekā vienu PDF failu. Ir ieteicams palielināt loga **Dokumentu pārvaldības parametri** iestatījuma **Maksimālais faila lielums** vērtību līdz 150 MB.

## <a name="viewing-information"></a>Informācijas skatīšana

Lapu **Pieejamās aprūpes segums nodarbinātajam** varat izmantot, lai redzētu, kuri darbinieki ir piešķirti kurai seguma grupai, kuri darbinieki nav jāietver pārskatā, un kuri darbinieki nav piešķirti.

Ja kāda no pieejamās aprūpes seguma grupas noklusējuma vērtībām ir pārrakstīta, pie mainītās vērtības tiek rādīta zvaigznīte. Ja vērtības visiem 12 mēnešiem ir vienādas un nav tikušas pārrakstītas, tad vērtība tiks drukāta kolonnā **Visi 12 mēneši**.

Varat izmantot arī uzziņu logu, lai saprastu, kuri darbinieki ir atzīmēti kā tādi, kas nav jānorāda ACA pārskatā. Nav nepieciešams izsekot, vai tiem tika piedāvāts segums, un gada beigās tiem nebūs jāizsniedz 1095-C. Lai ģenerētu sarakstu ar visiem darbiniekiem, kuri nesaņems 1095-C, laukā **Filtrēt pēc** atlasiet **Nav norādāms ACA pārskatā**.

Papildus tam varat apskatīt jebkuru darbinieku, kuri nav piešķirti (lauks **ACA pārskata segums** ir tukšs) vai kuri ir piešķirti kādai pieejamās aprūpes seguma grupai, kuras darbība ir beigusies tajā gadā, kas ir atlasīts laukā **Gads**.

Sarakstus ar darbiniekiem, kas tika ģenerēti, izmantojot filtrēšanas opcijas, varat eksportēt uz programmu Excel.

Ja jums ir jāsniedz pārskats par iekļautajām personām, jo jūs nodrošināt paša apdrošinātu segumu, varat apskatīt visus apgādājamos, kas ietverti atvieglojumu plānos, kuri atzīmēti kā **Norādāmi ACA pārskā**. Darbību rūtī atlasiet **Skatīt apgādājamā segumu**.

> [!NOTE]
> Pieprasījuma logā tiek rādīti tikai atvieglojumu plāni, kas atzīmēti kā **Norādāms ACA pārskatā**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]