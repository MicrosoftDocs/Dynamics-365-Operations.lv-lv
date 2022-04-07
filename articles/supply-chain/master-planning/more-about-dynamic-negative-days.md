---
title: Negatīvās dienas un dinamiskās negatīvās dienas
description: Šajā tēmā ir sniegta informācija par negatīvām dienām un dinamiskām negatīvām dienām, un to, kā varat tās izmantot, lai palīdzētu savam uzņēmumam.
author: t-benebo
ms.date: 05/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d88517c99a274911e8abd8de4bcd318139822a5
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469874"
---
# <a name="negative-days-and-dynamic-negative-days"></a>Negatīvās dienas un dinamiskās negatīvās dienas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par negatīvām dienām un dinamiskām negatīvām dienām, un to, kā varat tās izmantot, lai palīdzētu savam uzņēmumam. *Negatīvo dienu periods* norāda dienu skaitu, ko esat gatavs gaidīt, pirms veicat jaunu papildināšanas pasūtījumu, ja ir negatīvs krājumu daudzums.

Šajā tēmā ir norādīta šāda informācija:

- Kā tiek izveidoti plānotie pasūtījumi
- Saistība starp negatīvo dienu periodu un krājuma izpildes laiku
- Kā tiek aprēķināts dinamisko negatīvo dienu periods un kā aprēķinā tiek ņemts vērā krājuma izpildes laiks
- Kā interpretēt [ieteikumus attiecībā uz izpildes laika uzlabošanu materiālu vajadzību plānošanai (MRP) (vispārējā plānošana)](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx), kas ir saistīti ar negatīvām dienām

Šajā tēmā ir izmantoti trīs hipotētiski scenāriji, lai palīdzētu jums izprast šo informāciju. Scenāriju atšķirība ir brīdis, kurā tiek saņemts pieprasījums: pirms krājuma izpildes laika perioda, tā laikā vai pēc tā.

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>1. scenārijs. Pieprasījums rodas pirms krājuma izpildes laika perioda

Pieprasījums var rasties vai nu salīdzinoši agri krājuma izpildes laikā, vai tieši pirms izpildes laika perioda sākuma. Tālāk minēts šī scenārija piemērs:

- Demonstrācijas preces krājumam ir sešu dienu pirkšanas izpildes laiks.
- Nulles dienā (1. janvārī) demonstrācijas preces krājumu līmenis ir 0 (nulle).
- Nulles dienā (1. janvārī) tiek saņemts pārdošanas pasūtījums par 10 demonstrācijas preces vienībām.
- Septītajā dienā (8. janvārī) ir esošs pirkšanas pasūtījums par 10 demonstrācijas preces vienībām.

Nākamajā attēlā ir parādīts šī scenārija grafisks skats.

![1. scenārija grafisks skats.](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>A gadījums. Negatīvo dienu vērtība ir mazāka par krājuma izpildes laiku

Iestatot vienumam Dienas(-) skaitli, kas ir mazāks par krājuma izpildes laiku, MRP meklē demonstrācijas preces ieejas plūsmas negatīvo dienu periodā. Nevarot atrast ieejas plūsmas, MRP izveido jaunu plānoto pirkšanas pasūtījumu. Šim plānotajam pasūtījumam uzreiz tiek piemērota aizkave par sešām dienām (izpildes laiks). Tādējādi tas tiks piegādāts 7. janvārī. Esošajam pirkšanas pasūtījumam tiks parādīts darbības ziņojums **Atcelt**, jo jauna plānotā pirkšanas pasūtījuma izveide to ir padarījusi nevajadzīgu.

Nākamajā attēlā ir redzams šī gadījuma ekrānuzņēmums.

![1. scenārija A gadījuma ekrānuzņēmums.](./media/negative-days-2.png)

Nākamajā attēlā ir parādīts šā gadījuma grafisks skats.

![1. scenārija A gadījuma grafisks skats.](./media/negative-days-3.png)

Ņemot vērā MRP veiktspēju un plāna nestabilitāti, šis gadījums nenodrošina labus rezultātus. MRP ir jāizveido jauns plānotais pasūtījums un ir jāaprēķina kavējumi un darbības. Šie uzdevumi ir laikietilpīgi. Šis gadījums arī pievieno plānam divas papildu transakcijas. No otras puses, pārdošanas pasūtījums tiek aizkavēts tikai par sešām, nevis septiņām dienām.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>B gadījums. Negatīvo dienu vērtība ir lielāka par krājuma izpildes laiku

Lai palīdzētu uzlabot MRP veiktspēju, vienumam Dienas(-) var iestatīt skaitli, kas ir lielāks par krājuma izpildes laiku. Tā kā šajā scenārijā nevar nodrošināt piegādi izpildes laikā, varat meklēt ieejas plūsmas visā lietderīgajā periodā. Lai gan MRP izpildes laiks būs īsāks, ir jāuzmanās no pasūtījumu papildu aizkavēm.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>C gadījums. Automātiski saistīt krājuma izpildes laiku ar negatīvo dienu periodu

Lai automātiski saistītu krājuma izpildes laiku ar negatīvo dienu periodu, izmantojiet dinamiskās negatīvās dienas. Lai izmantotu dinamiskās negatīvās dienas, atveriet **Vispārējā plānošana \> Iestatījumi \> Vispārējās plānošanas parametri** un pēc tam cilnē **Vispārīgi**, sadaļā **Vajadzība** iestatiet opcijai **Lietot dinamiskās negatīvās dienas** vienumu **Jā**. Pēc tam MRP meklē ieejas plūsmas dinamisko negatīvo dienu periodā. Šajā gadījumā periods tiek aprēķināts, izmantojot šādu formulu:

Dinamisko negatīvo dienu periods = Pirkšanas izpildes laiks + Negatīvo dienu periods + (Pašreizējais datums – Vajadzības datums)

(Ja demonstrācijas preces krājuma noklusējuma pasūtījuma tips ir **Ražošana** vai **Pārsūtīšana**, izpildes laiks ir **krājumu** izpildes laiks.)

Lietojot dinamiskās negatīvās dienas, periods, kuru ņem vērā MRP attiecībā uz ieejas plūsmām, tagad ir 6 + 2 + 0 = 8 dienas. MRP atrod esošo pirkšanas pasūtījumu un piesaista tam pārdošanas pasūtījumu. Netiek izveidoti jauni plānotie pasūtījumi. Tādēļ MRP izpildes laiks ir īsāks. Nākamajā attēlā ir parādītas demonstrācijas preces krājuma neto vajadzības.

![1. scenārija C gadījuma neto vajadzības.](./media/negative-days-4.png)

Nākamajā attēlā ir parādīts šā gadījuma grafisks skats.

![1. scenārija C gadījuma grafisks skats.](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>D gadījums. Izmantot tikai dinamiskās negatīvās dienas

Iestatot vienumam Dienas(-) vērtību **0** (nulle) un izmantojot tikai dinamisko negatīvo dienu periodu, dinamisko negatīvo dienu periods ir 6 + 0 + 0 = 6 dienas. Šādā gadījumā rezultāts ir tāds pats kā rezultāts šī scenārija A gadījumā. MRP ir jāizveido jauns plānotais pasūtījums un ir jāaprēķina kavējumi un darbības. Šie uzdevumi ir laikietilpīgi un var arī radīt sarežģījumus. Turklāt ir jāapstrādā divas papildu transakcijas. Tā kā krājumam, kuram paredzēta piegāde, pieprasījumu nevar izpildīt laikā, šajā gadījumā plāns tiek padarīts nevajadzīgi sarežģīts.

Nākamajā attēlā ir redzams šī gadījuma ekrānuzņēmums.

![1. scenārija D gadījuma ekrānuzņēmums.](./media/negative-days-6.png)

Nākamajā attēlā ir parādīts šā gadījuma grafisks skats.

![1. scenārija D gadījuma grafisks skats.](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>E gadījums. Izmantot gan negatīvās dienas, kas pārsniedz krājuma izpildes laiku, gan dinamisko negatīvo dienu periodu

Iestatot vienumam Dienas(-) skaitli, kas ir lielāks par krājuma izpildes laiku, un izmantojot arī dinamisko negatīvo dienu periodu, dinamisko negatīvo dienu periods ir 6 + 6 + 0 = 12 dienas. Lietojot šo pieeja, var tikt iegūts ļoti ilgs periods, kurā MRP ir jāmeklē rezultāti. Informāciju par to, kā E gadījums ir saistīts ar situāciju, kad iestatāt ilgu negatīvo dienu periodu, skatiet šīs tēmas sadaļā [Secinājumi](#conclusion).

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>2. scenārijs. Pieprasījums rodas krājuma izpildes laika periodā

Pieprasījums var rasties krājuma izpildes laikā. Tālāk minēts šī scenārija piemērs:

- Demonstrācijas preces krājumam ir sešu dienu pirkšanas izpildes laiks. 
- Nulles dienā (1. janvārī) demonstrācijas preces krājumu līmenis ir 0 (nulle).
- Ceturtajā dienā (5. janvārī), kas ir krājuma izpildes laikā, tiek saņemts pārdošanas pasūtījums par 10 demonstrācijas preces vienībām.
- Septītajā dienā (8. janvārī) ir pirkšanas pasūtījums par 10 demonstrācijas preces vienībām.

Nākamajā attēlā ir parādīts šī scenārija grafisks skats.

![2. scenārija grafisks skats.](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>A gadījums. Negatīvo dienu vērtība ir mazāka par krājuma izpildes laiku

Iestatot vienumam Dienas(-) skaitli, kas ir mazāks par krājuma izpildes laiku, MRP meklē demonstrācijas preces ieejas plūsmas negatīvo dienu periodā. Tā kā MRP neatrod ieejas plūsmas, tā izveido jaunu plānoto pirkšanas pasūtījumu, kas izmanto pašreizējo datumu kā pasūtījuma datumu. Šim plānotajam pasūtījumam uzreiz tiek piemērota aizkave par sešām dienām (izpildes laiks). Tādējādi tas tiks piegādāts 7. janvārī. Esošajam pirkšanas pasūtījumam tiks parādīts darbības ziņojums **Atcelt**, jo jauna plānotā pirkšanas pasūtījuma izveide to ir padarījusi nevajadzīgu.

Nākamajā attēlā ir redzams šī gadījuma ekrānuzņēmums.

![2. scenārija A gadījuma ekrānuzņēmums.](./media/negative-days-9.png)

Nākamajā attēlā ir parādīts šā gadījuma grafisks skats.

![2. scenārija A gadījuma grafisks skats.](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>B gadījums. Negatīvo dienu vērtība ir lielāka par krājuma izpildes laiku

Šis gadījums līdzinās 1. scenārija B gadījumam. Iestatot vienumam Dienas(-) skaitli, kas ir lielāks nekā krājuma izpildes laiks, netiek iegūts jauns plānotais pasūtījums. Pārdošanas pasūtījums ir pievienots esošajam pirkšanas pasūtījumam.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>C gadījums. Automātiski saistīt krājuma izpildes laiku ar negatīvo dienu periodu

Šis gadījums līdzinās 1. scenārija C gadījumam, jo dinamiskās negatīvās dienas nodrošina tikpat labu rezultātu kā attiecīgajā gadījumā. Dinamisko negatīvo dienu periods tagad ir 6 + 2 – 4 = 4 dienas. Ja izmantojat šo pieeju, MRP atrod esošo pirkšanas pasūtījumu un pievieno tam pārdošanas pasūtījumu. Tā kā netiek izveidoti jauni plānotie pasūtījumi, MRP izpildes laiks ir īsāks.

Nākamajā attēlā ir redzams šī gadījuma ekrānuzņēmums.

![2. scenārija C gadījuma ekrānuzņēmums.](./media/negative-days-11.png)

Nākamajā attēlā ir parādīts šā gadījuma grafisks skats.

![2. scenārija C gadījuma grafisks skats.](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>D gadījums. Izmantot tikai dinamiskās negatīvās dienas

Iestatot vienumam Dienas(-) vērtību **0** (nulle) un izmantojot tikai dinamisko negatīvo dienu periodu, dinamisko negatīvo dienu periods tagad ir 6 + 0 – 4 = 2 dienas. Šādā gadījumā rezultāts ir tāds pats kā rezultāts šī scenārija A gadījumā. Procesa grafisku attēlojumu skatiet šī scenārija A gadījuma aprakstā.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>E gadījums. Izmantot gan negatīvās dienas, kas pārsniedz krājuma izpildes laiku, gan dinamisko negatīvo dienu periodu

Iestatot vienumam Dienas(-) skaitli, kas ir lielāks par krājuma izpildes laiku, un izmantojot arī dinamisko negatīvo dienu periodu, dinamisko negatīvo dienu periods ir 6 + 6 – 4 = 8 dienas. Lietojot šo pieeja, var tikt iegūts ļoti ilgs periods, kurā MRP ir jāmeklē rezultāti. Informāciju par to, kā E gadījums ir saistīts ar situāciju, kad iestatāt ilgu negatīvo dienu periodu, skatiet šīs tēmas sadaļā [Secinājumi](#conclusion).

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>3. scenārijs. Pieprasījums rodas pēc krājuma izpildes laika perioda

Pieprasījums var rasties pēc krājuma izpildes laika. Tālāk minēts šī scenārija piemērs:

- Demonstrācijas preces krājumam ir sešu dienu pirkšanas izpildes laiks.
- Nulles dienā (1. janvārī) demonstrācijas preces krājumu vērtība ir 0 (nulle).
- Septītajā dienā (8. janvārī), kas ir ārpus krājuma izpildes laika, tiek saņemts pārdošanas pasūtījums par 10 demonstrācijas preces vienībām.
- Desmitajā dienā (11. janvārī) ir pirkšanas pasūtījums par 10 demonstrācijas preces vienībām.

Nākamajā attēlā ir parādīts šī scenārija grafisks skats.

![3. scenārija grafisks skats.](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>A gadījums. Negatīvo dienu vērtība ir mazāka par krājuma izpildes laiku

Iestatot vienumam Dienas(-) skaitli, kas ir mazāks par krājuma izpildes laiku, MRP veic meklēšanu divas dienas pirms pārdošanas pasūtījuma vajadzības datuma. Nevarot neko atrast, MRP izveido plānoto pirkšanas pasūtījumu 2. janvārī. Šis plānotais pirkšanas pasūtījums tiks nosūtīts tieši laikā, lai izpildītu pārdošanas pasūtījuma pieprasījumu. Esošajam pirkšanas pasūtījumam tiek parādīts darbības paziņojums **Atcelt**, jo tas nav nepieciešams.

Nākamajā attēlā ir redzams šī gadījuma ekrānuzņēmums.

![3. scenārija A gadījuma ekrānuzņēmums.](./media/negative-days-14.png)

Nākamajā attēlā ir parādīts šā gadījuma grafisks skats.

![3. scenārija A gadījuma grafisks skats.](./media/negative-days-15.png)

> [!NOTE]
> Iepriekšējā ekrānuzņēmumā pirkšanas pasūtījuma vajadzības datums ir 12. janvāris. Tā kā šis ekrānuzņēmums tika izveidots 2015. gadā, kad 11. janvāris bija svētdiena, MRP pārcēla vajadzības datumu uz nākamo darba dienu, kas bija pirmdiena, 12. janvāris. Tomēr pirkšanas pasūtījuma piegādes datums ir 11. janvāris.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>B gadījums. Negatīvo dienu vērtība ir lielāka par krājuma izpildes laiku

Iestatot vienumam Dienas(-) skaitli, kas ir lielāks nekā krājuma izpildes laiks, netiek iegūts jauns plānotais pasūtījums. Pārdošanas pasūtījums ir piesaistīts esošajam pirkšanas pasūtījumam. Tāpēc pārdošanas pasūtījuma izpilde aizkavējas. Ja izveidojat plānoto pasūtījumu, varat nosūtīt pārdošanas pasūtījumu laikā.

Nākamajā attēlā ir redzams šī gadījuma ekrānuzņēmums.

![3. scenārija B gadījuma ekrānuzņēmums.](./media/negative-days-16.png)

Nākamajā attēlā ir parādīts šā gadījuma grafisks skats.

![3. scenārija B gadījuma grafisks skats.](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>C gadījums. Automātiski saistīt krājuma izpildes laiku ar negatīvo dienu periodu

Šis gadījums līdzinās 1. scenārija C gadījumam, jo dinamiskās negatīvās dienas nodrošina tikpat labu vai pat labāku rezultātu kā šī scenārija B gadījumā.

Dinamisko negatīvo dienu periods ir 6 + 2 – 7 = 1 diena. Tomēr šajā gadījumā sistēma joprojām ņem vērā negatīvo dienu izpildes laiku (2), jo MRP ņem vērā maksimālo vērtību starp negatīvo dienu izpildes laiku un dinamisko negatīvo dienu izpildes laiku. Tādēļ šajā gadījumā rezultāts ir tāds pats kā rezultāts šī scenārija A gadījumā.

Nākamajā attēlā ir parādīts šā gadījuma grafisks skats.

![3. scenārija C gadījuma grafisks skats.](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>D gadījums. Izmantot tikai dinamiskās negatīvās dienas

Iestatot vienumam Dienas(-) vērtību **0** (nulle) un izmantojot tikai dinamisko negatīvo dienu periodu, dinamisko negatīvo dienu periods tagad ir 6 + 0 – 7 = –1 diena. Šādā gadījumā sistēma joprojām ņem vērā negatīvo dienu izpildes laiku (2). Tādēļ šajā gadījumā rezultāts ir tāds pats kā rezultāts šī scenārija A gadījumā, un tam ir visi tie paši trūkumi. Procesa grafisku attēlojumu skatiet 2. scenārija A gadījuma aprakstā.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>E gadījums. Izmantot gan negatīvās dienas, kas pārsniedz krājuma izpildes laiku, gan dinamisko negatīvo dienu periodu

Šis gadījums ir tāds pats kā 1. un 2. scenārija E gadījums. Tam ir gandrīz tādas pašas priekšrocības un trūkumi.

## <a name="conclusion"></a>Nobeigums

Kā liecina trīs šajā tēmā aprakstītie scenāriji, vienumam Dienas(-) ieteicams iestatīt skaitli, kas ir lielāks par vajadzību grupā esošo krājumu izpildes laiku. Ieteicams arī izmantot tikai dinamiskās negatīvās dienas un iestatīt vienumam Dienas(-) dienu skaitu, ko esat gatavs gaidīt, pirms jauna papildināšanas pasūtījuma veikšanas, ja ir negatīvi krājumi (citiem vārdiem sakot, dienu skaitu, par kuru esat gatavs papildus aizkavēt pieprasījumu). Turklāt krājumiem vienā vajadzību grupā ir jābūt līdzīgiem izpildes laikiem.

Iestatot vienumam Dienas(-) vērtību **0** (nulle) un neizmantojot dinamiskās negatīvās dienas, MRP vienmēr izveido jaunu plānoto pasūtījumu, lai izpildītu pieprasījumu. Šādā gadījumā ir svarīgi darbā izmantot darbību ziņojumus, lai nodrošinātu, ka neizveidojas pārāk liels krājumu atlikums.

Varat iestatīt ilgu negatīvo dienu periodu un pēc tam strādāt ar darbību ziņojumiem. Šī pieeja sniedz labus plānošanas rezultātus, bet tā ir arī mazliet lēnāka. To arī var būt grūtāk analizēt, jo ir jāanalizē un jālieto darbību ziņojumi. Tas ir piemērs:

- Demonstrācijas preces krājumam ir sešu dienu pirkšanas izpildes laiks.
- Nulles dienā (1. janvārī) demonstrācijas preces krājumu vērtība ir 0 (nulle).
- Nulles dienā (1. janvārī) tiek saņemts pārdošanas pasūtījums par 10 demonstrācijas preces vienībām.
- Devītajā dienā (10. janvārī) tiek saņemts pārdošanas pasūtījums par 10 demonstrācijas preces vienībām.
- Vienpadsmitajā dienā (12. janvārī) ir pirkšanas pasūtījums par 10 demonstrācijas preces vienībām.
- Vienumam Dienas(-) ir iestatīta vērtība **20**, kas ir daudz lielāka par krājuma izpildes laiku.

Nākamajā attēlā ir parādīts procesa grafisks skats.

![Piemēra grafisks pārskats.](./media/negative-days-19.png)

MRP sniedz šādus rezultātus.

![1. rezultātu piemērs.](./media/negative-days-20.png)

Iepriekšējā ekrānuzņēmumā pārdošanas pasūtījuma vajadzības datums ir 9. janvāris, nevis 10. janvāris. Tā kā šis ekrānuzņēmums tika izveidots 2015. gadā, kad 10. janvāris bija sestdiena, pasūtījuma vajadzības datumam ir jābūt iepriekšējai darba dienai, kas bija piektdiena, 9. janvāris.

MRP izveido plānoto pirkšanas pasūtījumu, lai izpildītu pieprasījumu, kas ir noteikts pirmajā pārdošanas pasūtījumā, bet pēc tam arī iesaka atcelt plānoto pasūtījumu, jo varat turpināt esošo pirkšanas pasūtījumu un palielināt tā daudzumu.

Rezultāti nav nepareizi, bet MRP izpildes laiks var būt ilgāks, jo MRP ir jāizveido visas aizkaves un ieteikumi. Turklāt plānotājam var būt nepieciešams vairāk laika, lai saprastu MRP rezultātus. Vissvarīgākais šajā gadījumā ir tas, ka plānotājam ir jāsaprot un jāizmanto darbību ziņojumi.

Samazinot negatīvo dienu skaitu līdz vērtībai, kas ir tuvāka krājuma izpildes laikam, un izmantojot dinamiskās negatīvās dienas, MRP nodrošina tālāk redzamos rezultātus.

![2. rezultātu piemērs.](./media/negative-days-21.png)

MRP izveido plānoto pasūtījumu, kas piesaistīts pirmajam pārdošanas pasūtījumam. Pēc tam, kā paredzēts, otrais pārdošanas pasūtījums tiek piesaistīts esošajam pirkšanas pasūtījumam, pamatojoties uz negatīvo dienu iestatījumiem. Arī šis plānošanas rezultāts ir pareizs, un MRP izpildes laiks var būt īsāks. Šādā gadījumā nav svarīgi, lai jūs saprastu darbības ziņojumus un zinātu, kā ar tiem strādāt.

Lai palīdzētu nodrošināt, ka jūsu uzņēmumam tiek ievadītas pareizas vērtības, ir jāņem vērā gan funkcionalitāte, gan MRP izpildes laiks. Tādēļ var būt nepieciešami daži izmēģinājumi, lai noteiktu optimālās vērtības.

## <a name="see-also"></a>Skatiet arī

Plašāku informāciju skatiet oriģinālajā emuāra ierakstā [Vairāk par (dinamiskajām) negatīvajām dienām](/archive/blogs/axmfg/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
