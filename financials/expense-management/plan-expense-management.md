---
title: "Izdevumu pārvaldības konfigurēšana"
description: "Šajā rakstā ir aprakstīti apsvērumi un lēmumi, kas jums ir jāpieņem plānošanas procesa laikā, pirms programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise konfigurējat izdevumu pārvaldību. Apgabalā Izdevumu pārvaldība tostarp varat glabāt informāciju par maksāšanas metodēm, ceļošanas pieprasījumiem, izdevumu atskaitēm un politikām."
author: KimANelson
manager: AnnBe
ms.date: 06/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: edd3d8ca760c1453ae7cf8d5ff2fdfdedbb022c4
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="configure-expense-management"></a>Izdevumu pārvaldības konfigurēšana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīti apsvērumi un lēmumi, kas jums ir jāpieņem plānošanas procesa laikā, pirms programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise konfigurējat izdevumu pārvaldību. Apgabalā Izdevumu pārvaldība tostarp varat glabāt informāciju par maksāšanas metodēm, ceļošanas pieprasījumiem, izdevumu atskaitēm un politikām. 

Tā kā daudzi lēmumi, ko pieņemat, kad plānojat savu izdevumu pārvaldības konfigurāciju, ir atkarīgi no jūsu organizācijas hierarhijas un finanšu struktūras, jums ir nepieciešams skatīt plānošanas dokumentus šiem apgabaliem.

## <a name="intercompany-expenses"></a>Starpuzņēmumu izdevumi
Kad iespējojat starpuzņēmumu izdevumus, jūs juridiskajām personām un darbiniekiem ļaujat radīt izdevumus citas juridiskās personas vārdā vai iekasēt maksājumus no citas juridiskās personas jūsu organizācijas ietvaros. Piemēram, darbinieks juridiskajā personā A izpilda projektu juridiskai personai B. Ja ir aktivizēti starpuzņēmumu izdevumi, pēc tam šis darbinieks darba laika uzskaites tabulu var iesniegt juridiskajai personai B un saņemt samaksu. Ja jūsu organizācijai nav vairākas juridiskās personas, jums nav nepieciešams iespējot starpuzņēmumu izdevumus. **Lēmums:** Vai vēlaties iespējot starpuzņēmumu izdevumus?

## <a name="financial-management"></a>Finanšu pārvaldība
Izdevumu pārvaldība ir cieši integrēta jūsu organizācijas finanšu pārvaldībā. Liela daļa jūsu konfigurācijas attiecībā uz izdevumu pārvaldību būs pamatota ar lēmumiem, ko esat pieņēmis par savas organizācijas finansēm. Nākamajās sadaļās ir aprakstīti dažādie apgabali, kuriem ir nepieciešama plānošana un lēmumi, balstoties uz jūsu organizācijas finanšu lēmumiem un norādījumiem no vadības grupas.

### <a name="per-diems"></a>Dienasnauda

Ir nepieciešams definēt darbinieku dienasnaudas, ko nodrošina jūsu organizācija. Tā kā dienasnaudas parasti tiek izmantotas, lai segtu tādus izdevumus kā maltītes, izmitināšana un citi gadījuma izdevumi, varat izveidot kārtulas attiecībā uz dienasnaudas piemaksām, jūsu organizācija piedāvā. Dienasnaudas likmes var būt balstītas uz komandējuma gada laiku, komandējuma vietu vai uz abiem. Kad definējat dienasnaudas kārtulu, varat norādīt, ka tiek ieturēts procentuāls daudzums no dienas naudas, ja darbinieks saņem brīvpusdienas vai bezmaksas pakalpojumus. Varat arī definēt dienasnaudas likmju pakāpes, lai iestatītu minimālo un maksimālo stundu skaitu, kādam dienasnaudas likmes var lietot attiecībā uz darbinieka komandējumu. **Lēmumi:**

-   Noklusējuma dienasnaudas kārtulas pirmajai un pēdējai dienai:
    -   Kāds ir minimālais stundu skaits, ko darbinieks var pieprasīt vienai dienai un joprojām saņemt dienasnaudu?
    -   Vai tiek samazināta summa, kas tiek piedāvāta par ēdināšanu pirmajā un pēdējā dienā? Ja tā — kāds ir samazinājuma procentuālais daudzums?
    -   Vai tiek samazināta summa, kas tiek piedāvāta par viesnīcas izdevumiem pirmajā un pēdējā dienā? Ja tā — kāds ir samazinājuma procentuālais daudzums?
    -   Vai tiek samazināta summa, kas tiek piedāvāta par citiem izdevumiem pirmajā un pēdējā dienā? Ja tā — kāds ir samazinājuma procentuālais daudzums?
-   Noklusējuma dienasnaudas kārtulas:
    -   Vai notiek procentuāla dienasnaudas piemaksas samazināšana par katru maltīti, ja, piemēram, maltītes ir bez maksas? Ja tā — kāds ir samazinājuma procentuālais daudzums par katru maltīti?
    -   Vai ēdināšanas samazinājums tiek rēķinātas par dienu, pa braucienu vai par maltīšu skaitu dienā?
    -   Vai dienasnaudas summas tiek noapaļots parastajā veidā vai uz augšu?
    -   Vai dienasnaudas tiek rēķinātas 24 stundu periodam vai kalendārajai dienai?
-   No atrašanās vietas atkarīgās dienasnaudas kārtulas:
    -   Vai dienasnaudas likmes atšķiras atkarībā no atrašanās vietas, un kādas atrašanās vietas ir iekļautas?
    -   Ja dienasnaudas likme ir atkarīga no atrašanās vietas, kāda procentuālā summa katrai atrašanās vietai tiek nodrošināta attiecībā uz:
        -   maltītēm
        -   viesnīcu
        -   citiem izdevumiem

### <a name="expense-management-journals-and-accounts"></a>Izdevumu pārvaldības žurnāli un konti

Izdevumu pārvaldībai ir nepieciešams, lai jūs izmantotu vairākus žurnālus un kontus. Jums ir jāizlemj, piemēram, vai to pašu kontu izmantot naudas avansiem un kredītkaršu domstarpībām. **Lēmumi:**

-   Kurā virsgrāmatas žurnālā tiek grāmatotas apstiprināto izdevumu atskaites?
-   Kurš konts tiek izmantots naudas avansiem?
-   Vai naudas avansi ir jāgrāmato nekavējoties?

### <a name="payment-methods"></a>Maksājuma metodes

Kad darbiniekiem ļaujat radīt izdevumus jūsu uzņēmuma vārdā, jums ir nepieciešams definēt maksājumu metodes, ko darbiniekiem ir atļauts lietot. Piemēram, darbiniekiem varat ļaut izmantot skaidru naudu vai korporatīvo kredītkarti. Tāpat darbiniekiem varat ļaut arī izmantot personiskās kredītkartes un pēc tam šiem darbiniekiem kompensēt izdevumus. Attiecībā uz katru maksājumu metodi, kuru atļaujat, jums ir jāpieņem tālāk norādītie lēmumi. **Lēmumi:**

-   Kādas maksāšanas metodes ir atļautas?
-   Kam pieder maksāšanas metodes izdevumi?
-   Vai pastāv korespondējošā konta tips? Ja tā — kas tas ir?
-   Ja pastāv korespondējošais konts — kas ir šis konts?
-   Ja maksāšanas metode ir kredītkarte, vai maksāšanas metode ir jāizmanto tikai ar importētajām transakcijām?

### <a name="expense-categories-and-shared-categories"></a>Izdevumu kategorijas un koplietojamās kategorijas

Kad darbinieki izveido izdevumu atskaiti, katram viņu reģistrētajam izdevumam ir jābūt saistītam ar kādu izdevumu kategoriju. Izdevumu kategorijas tiek atvasinātas no koplietojamajām kategorijām, kuras var kopīgot dažādās juridiskajās personās jūsu organizācijas ietvaros. Atkarībā no tā, kā jūsu organizācija ir definēta, šīs kategorijas ir iespējams kopīgot arī modulī Projektu vadība un uzskaite. Pamatojoties uz jūsu organizācijas definīciju un norādījumiem no ieviešanas grupas, nosakiet, vai izdevumu pārvaldībā izmantotās kategorijas ir jālieto tikai izdevumos, vai tās ir nepieciešams koplietot starp moduli Projekts un Izdevumi. Ņemiet vērā, ka šīs kategorijas var koplietot starp moduļiem Projekts un Izdevumi vai Projekts un Ražošana, bet ne starp Izdevumi un Ražošana. Par katru izdevumu kategoriju jums ir jāpieņem tālāk norādītie lēmumi. **Lēmumi:**

-   Kas ir izdevumu kategorija? Piemēram, lidojumi, viesnīcas vai nobrauktais attālums.
-   Vai šo izdevumu kategoriju var izmantot arī modulī Projektu vadība un uzskaite?
-   Kas ir izdevumu tips?
-   Kas ir noklusējuma maksāšanas metode izdevumu kategorijai?
-   Vai izdevumus šajā kategorijā ir nepieciešams uzskaitīt detalizēti?
-   Kas ir galvenais noklusējuma konts izdevumu kategorijai?
-   Kas ir noklusējuma krājumu pārdošanas nodokļu grupa izdevumu kategorijai?
-   Vai izdevumu kategorijai ir atļautas papildu maksāšanas metodes? Ja tā — kādas tās ir?
-   Vai šajā izdevumu kategorijā pastāv apakškategorijas? Ja tā:
    -   Vai kādas apakškategorijas ir izslēgtas no nodokļu atgūšanas?
    -   Kas ir apakškategoriju krājuma pārdošanas nodokļu grupa?

    Ja šī izdevumu kategorija tiek izmantota arī modulī Projektu vadība un uzskaite, atbildiet uz atlikušajiem jautājumiem. Pretējā gadījumā šo sadaļu jūs esat pabeidzis.
-   Kuri izmaksu konti tiks izmantoti tālāk norādītajiem mērķiem?
    -   Izmaksas
    -   Algu sadalījums
    -   NP-izmaksu vērtība
    -   Izmaksas-krājumi
    -   NP-izmaksu vērtība-krājumi
    -   Uzkrātie zaudējumi
    -   NP-uzkrātie zaudējumi
-   Kuri ieņēmumu konti tiks izmantoti tālāk norādītajiem mērķiem?
    -   Rēķinos iekļautie ieņēmumi
    -   Uzkrātie ieņēmumi-pārdošanas vērtība
    -   NP-pārdošanas vērtība
    -   Uzkrātie ieņēmumi-ražošana
    -   NP-ražošana
    -   Uzkrātie ieņēmumi-peļņa
    -   NP-peļņa
    -   Uzkrātie ieņēmumi-abonements
    -   NP-abonements

 

### <a name="taxes"></a>Nodokļi

Attiecībā uz nodokļiem, kas saistīti ar izdevumiem, jums ir jānosaka, kas tiek iekļauts vai iespējots izdevumu atskaitēs. **Lēmumi:**

-   Vai pārdošanas nodoklis ir iekļauts izdevumu summās?
-   Vai izdevumiem ir jāiespējo nodokļu atgūšana?

Ievērojiet — ja virsgrāmatas plānošanas laikā jūs nolēmāt lietot ASV pārdošanas nodokļa un importa nodokļa kārtulas, kas tiek izdarīts, lauka **Lietot pārdošanas nodokļa nodokļu kārtulas** vērtību pārslēdzot uz Jā, tad jūs nevarat nodokļa atgūšanu iespējot izdevumiem.

## <a name="policies"></a>Lietošanas ierobežojumi
Varat izveidot izdevumu atskaišu politikas tā, lai jūsu organizācija varētu ietaupīt laiku un naudu, kad darbinieki rada zaudējumus tās vārdā. Politikas nodrošina, ka darbinieki iekļaujas budžetā, sniedz visu prasīto informāciju un tērē naudu tikai pēc nepieciešamības. Attiecībā uz katru izdevumu atskaišu politiku un katru izdevumu atskaites apstiprināšanas politiku, ko izveidojat, jums ir jāpieņem tālāk norādītie lēmumi. **Lēmumi:**

-   Kāds ir politikas nosaukums?
-   Kam šī izdevumu politika ir paredzēta?
-   Ja iepriekš izlēmāt iespējot starpuzņēmumu izdevumus — uz kuru uzņēmumu jūsu organizācijas ietvaros šī politika attiecas?
-   Kad šī politika stājas spēkā?
-   Kad beidzas šīs politikas darbība?
-   Kāda ir politikas kārtula?
-   Kāds ir politikas kārtulas iznākums?





