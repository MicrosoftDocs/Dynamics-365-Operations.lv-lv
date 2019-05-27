---
title: Izdevumu pārvaldības konfigurēšana
description: Šajā rakstā ir aprakstīti apsvērumi un lēmumi, kas ir jāņem vērā un jāpieņem plānošanas procesa laikā pirms moduļa Izdevumu pārvaldība konfigurēšanas programmā Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ac9959a4ee66e52ead5050897403602e407ca10
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570626"
---
# <a name="configure-expense-management"></a>Izdevumu pārvaldības konfigurēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti apsvērumi un lēmumi, kas ir jāņem vērā un jāpieņem plānošanas procesa laikā pirms moduļa Izdevumu pārvaldība konfigurēšanas programmā Microsoft Dynamics 365 for Finance and Operations. Modulī Izdevumu pārvaldība jūs tostarp varat glabāt informāciju par maksāšanas metodēm, komandējumu pieprasījumiem, izdevumu pārskatiem, politikām un citiem faktoriem.

Tā kā daudzi lēmumi, ko pieņemat, kad plānojat savu izdevumu pārvaldības konfigurāciju, ir atkarīgi no jūsu organizācijas hierarhijas un finanšu struktūras, jums ir nepieciešams skatīt plānošanas dokumentus šiem apgabaliem.

## <a name="intercompany-expenses"></a>Starpuzņēmumu izdevumi

Kad iespējojat starpuzņēmumu izdevumus, jūs juridiskajām personām un darbiniekiem ļaujat radīt izdevumus citas juridiskās personas vārdā un iekasēt maksājumus no citas nodarbinātības juridiskās personas jūsu organizācijas ietvaros. Piemēram, kāds darbinieks juridiskajā personā A pabeidz projektu juridiskajai personai B un projekta gaitā rodas ar komandējumu saistīti izdevumi. Ja ir aktivizēti starpuzņēmumu izdevumi, tad darbinieks var iesniegt izdevumu pārskatu, kurā ir grāmatoti izdevumi juridiskajai personai B, un pēc tam šie izdevumi ir jāapmaksā juridiskajai personai A. Ja jūsu organizācijai nav vairākas juridiskās personas, tad starpuzņēmumu izdevumus nav nepieciešams iespējot.

**Lēmums:** Vai vēlaties iespējot starpuzņēmumu izdevumus?

## <a name="financial-management"></a>Finanšu pārvaldība

Izdevumu pārvaldība ir cieši integrēta jūsu organizācijas finanšu pārvaldībā. Liela daļa jūsu konfigurācijas attiecībā uz moduli Izdevumu pārvaldība būs atkarīga no lēmumiem, ko esat pieņēmis par savas organizācijas finansēm. Nākamajās sadaļās ir aprakstīti dažādie apgabali, kuriem ir nepieciešama plānošana un lēmumi, balstoties uz jūsu organizācijas finanšu lēmumiem un norādījumiem no vadības grupas.

### <a name="per-diems"></a>Dienasnauda

Ir nepieciešams definēt darbinieku dienasnaudas, ko nodrošina jūsu organizācija. Tā kā dienasnaudas parasti tiek izmantotas, lai segtu tādus izdevumus kā maltītes, izmitināšana un citi gadījuma izdevumi, varat izveidot kārtulas attiecībā uz dienasnaudas piemaksām, jūsu organizācija piedāvā. Dienasnaudas likmes var būt balstītas uz gada laiku, komandējuma vietu vai uz abiem. Kad definējat dienasnaudas kārtulu, varat norādīt, ka tiek ieturēts procentuāls daudzums no dienas naudas, ja darbinieks saņem brīvpusdienas vai bezmaksas pakalpojumus. Varat arī definēt dienasnaudas likmju pakāpes, lai iestatītu minimālo un maksimālo stundu skaitu, kādam dienasnaudas likmes var lietot attiecībā uz darbinieka komandējumu.

**Lēmumi:**

- Noklusējuma dienasnaudas kārtulas pirmajai un pēdējai dienai:

    - Kāds ir minimālais stundu skaits, ko darbinieks var pieprasīt vienai dienai un joprojām saņemt dienasnaudu?
    - Vai tiek samazināta summa, kas tiek piedāvāta par ēdināšanu pirmajā dienā un pēdējā dienā? Ja pastāv samazinājums — kāds ir samazinājuma procentuālais daudzums?
    - Vai tiek samazināta summa, kas tiek piedāvāta par viesnīcas izdevumiem pirmajā dienā un pēdējā dienā? Ja pastāv samazinājums — kāds ir samazinājuma procentuālais daudzums?
    - Vai tiek samazināta summa, kas tiek piedāvāta par citiem izdevumiem, kas ir radušies pirmajā dienā un pēdējā dienā? Ja pastāv samazinājums — kāds ir samazinājuma procentuālais daudzums?

- Noklusējuma dienasnaudas kārtulas:

    - Vai notiek procentuāla dienasnaudas piemaksas samazināšana par katru maltīti, ja, piemēram, maltītes ir bez maksas? Ja pastāv samazinājums — kāds ir samazinājuma procentuālais daudzums katrai maltītei?
    - Vai ēdināšanas samazinājums tiek rēķinātas par dienu, pa braucienu vai par maltīšu skaitu dienā?
    - Vai dienasnaudas summas ir jānoapaļo parastajā veidā vai uz augšu?
    - Vai dienasnaudas tiek rēķinātas 24 stundu periodam vai kalendārajai dienai?

- No atrašanās vietas atkarīgās dienasnaudas kārtulas:

    - Vai dienasnaudas likmes atšķiras atkarībā no atrašanās vietas? Kādas atrašanās vietas ir ietvertas?
    - Ja dienasnaudas likmes atšķiras atkarībā no atrašanās vietas, tad kāds procentuālais daudzums katrai atrašanās vietai tiek nodrošināts par tālāk norādītajiem izdevumu tipiem.

        - Maltītes
        - Viesnīca
        - Citi izdevumi

### <a name="expense-management-journals-and-accounts"></a>Izdevumu pārvaldības žurnāli un konti

Izdevumu pārvaldībai ir nepieciešams, lai jūs izmantotu vairākus žurnālus un kontus. Jums ir jāizlemj, piemēram, vai to pašu kontu izmantot naudas avansiem un kredītkaršu domstarpībām.

**Lēmumi:**

- Kurā virsgrāmatas žurnālā tiek grāmatotas apstiprināto izdevumu atskaites?
- Kurš konts tiek izmantots naudas avansiem?
- Vai naudas avansi ir jāgrāmato nekavējoties?

### <a name="payment-methods"></a>Maksājuma metodes

Kad darbiniekiem ļaujat radīt izdevumus jūsu uzņēmuma vārdā, jums ir nepieciešams definēt maksājumu metodes, ko darbiniekiem ir atļauts lietot. Piemēram, darbiniekiem varat ļaut izmantot skaidru naudu vai korporatīvo kredītkarti. Tāpat darbiniekiem varat ļaut arī izmantot personiskās kredītkartes un pēc tam šiem darbiniekiem kompensēt izdevumus. Attiecībā uz katru maksājumu metodi, kuru atļaujat, jums ir jāpieņem tālāk norādītie lēmumi.

**Lēmumi:**

- Kādas maksāšanas metodes ir atļautas?
- Kam pieder maksāšanas metodes izdevumi?
- Vai pastāv korespondējošā konta tips? Ja pastāv korespondējošā konta tips — kāds tas ir?
- Ja pastāv korespondējošais konts — kas ir šis konts?
- Ja maksāšanas metode ir kredītkarte, vai maksāšanas metode ir jāizmanto tikai ar importētajām transakcijām?

### <a name="expense-categories-and-shared-categories"></a>Izdevumu kategorijas un koplietojamās kategorijas

Kad darbinieki izveido izdevumu atskaiti, katram viņu reģistrētajam izdevumam ir jābūt saistītam ar kādu izdevumu kategoriju. Izdevumu kategorijas tiek atvasinātas no koplietojamajām kategorijām, kuras var koplietot dažādās juridiskajās personās jūsu organizācijā. Atkarībā no veida, kā jūsu organizācija ir definēta, šīs kategorijas ir iespējams kopīgot arī modulī Projektu vadība un uzskaite. Pamatojoties uz jūsu organizācijas definīciju un norādījumiem no ieviešanas grupas, nosakiet, vai kategorijas, kuras tiek izmantotas modulī Izdevumu pārvaldība, ir jāizmanto tikai modulī Izdevumu pārvaldība, vai arī tās ir nepieciešams koplietot starp moduli Projektu vadība un uzskaite un moduli Izdevumu pārvaldība. Ņemiet vērā, ka šīs kategorijas var koplietot starp moduļiem Projekts un Izdevumi vai Projekts un Ražošana, bet ne starp Izdevumi un Ražošana. Par katru izdevumu kategoriju jums ir jāpieņem tālāk norādītie lēmumi.

**Lēmumi:**

- Kas ir izdevumu kategorija? Piemēri ir kategorijas lidojumiem, viesnīcām vai attālumam.
- Vai izdevumu kategoriju var izmantot arī modulī Projektu vadība un uzskaite?
- Kas ir izdevumu tips?
- Kas ir noklusējuma maksāšanas metode izdevumu kategorijai?
- Vai izdevumi šajā izdevumu kategorijā ir jāuzskaita?
- Kas ir galvenais noklusējuma konts izdevumu kategorijai?
- Kas ir noklusējuma krājumu pārdošanas nodokļu grupa izdevumu kategorijai?
- Vai izdevumu kategorijai ir atļautas papildu maksāšanas metodes? Ja ir atļautas papildu maksāšanas metodes — kādas tās ir?
- Vai šajā izdevumu kategorijā pastāv apakškategorijas? Ja pastāv apakškategorijas, jums ir jāpieņem arī tālāk norādītie lēmumi.

    - Vai kādas apakškategorijas ir izslēgtas no nodokļu atgūšanas?
    - Kas ir apakškategoriju krājuma pārdošanas nodokļu grupa?

Ja izdevumu kategorija tiek izmantota arī modulī Projektu vadība un uzskaite, atbildiet uz atlikušajiem jautājumiem. Pretējā gadījumā pārejiet uz nākamo sadaļu.

- Kuri izmaksu konti tiks izmantoti tālāk norādītajiem izdevumiem?

    - Izmaksas
    - Algu sadalījums
    - NP - Izmaksu vērtība
    - Izmaksas-krājumi
    - NP - Izmaksu vērtība - Krājumi
    - Uzkrātie zaudējumi
    - NP-uzkrātie zaudējumi

- Kuri ieņēmumu konti tiks izmantoti tālāk norādītajiem mērķiem?

    - Rēķinos iekļautie ieņēmumi
    - Uzkrātie ieņēmumi-pārdošanas vērtība
    - NP-pārdošanas vērtība
    - Uzkrātie ieņēmumi-ražošana
    - NP-ražošana
    - Uzkrātie ieņēmumi-peļņa
    - NP-peļņa
    - Uzkrātie ieņēmumi-abonements
    - NP-abonements

### <a name="taxes"></a>Nodokļi

Attiecībā uz nodokļiem, kas saistīti ar izdevumiem, jums ir jānosaka, kas tiek iekļauts vai iespējots izdevumu atskaitēs.

**Lēmumi:**

- Vai pārdošanas nodoklis ir iekļauts izdevumu summās?
- Vai izdevumiem ir jāiespējo nodokļu atgūšana?

    > [!NOTE]
    > Ja virsgrāmatas plānošanas laikā izlēmāt lietot ASV PVN un nodokļu importa nodokļa kārtulas, tad izdevumiem nevar iespējot nodokļu atgūšanu. (Lai lietotu ASV PVN un importa nodokļa kārtulas, opcija **Lietot PVN nodokļu kārtulas** ir jāiestata uz **Jā**.)

## <a name="policies"></a>Politikas

Izveidojot izdevumu pārskatu politikas, varat savai organizācijai palīdzēt taupīt laiku un naudu, kad darbinieki rada izdevumus šīs organizācijas vārdā. Politikas palīdz garantēt, ka darbinieki iekļaujas budžetā, sniedz visu nepieciešamo informāciju un tērē naudu tikai tad, ja nepieciešams. Attiecībā uz katru izdevumu atskaišu politiku un katru izdevumu atskaites apstiprināšanas politiku, ko izveidojat, jums ir jāpieņem tālāk norādītie lēmumi.

**Lēmumi:**

- Kāds ir politikas nosaukums?
- Kam šī izdevumu politika ir paredzēta?
- Ja iepriekš izlēmāt iespējot starpuzņēmumu izdevumus — uz kuriem uzņēmumiem jūsu organizācijas ietvaros šī politika attiecas?
- Kad šī politika stājas spēkā?
- Kad beidzas šīs politikas darbība?
- Kāda ir politikas kārtula?
- Kāds ir politikas kārtulas iznākums?
