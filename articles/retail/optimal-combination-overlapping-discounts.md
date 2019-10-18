---
title: Optimālās pārklāto atlaižu kombinācijas noteikšana
description: Ja atlaides pārklājas, ir jānosaka pārklāto atlaižu kombinācija, kas rada vismazāko transakcijas kopsummu vai lielāko kopējo atlaidi. Ja atlaides summa mainās atbilstoši nopirkto preču cenai, piemēram, parastās mazumtirdzniecības atlaides “pērc 1, saņem 1 X procentu atlaidi” (BOGO) gadījumā, šim procesam ir jāveic kombināciju optimizēšana.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount,
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 555098a7d11cb0b4c0f90357ff260598e80108f5
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017924"
---
# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Optimālās pārklāto atlaižu kombinācijas noteikšana

[!include [banner](includes/banner.md)]

Ja atlaides pārklājas, ir jānosaka pārklāto atlaižu kombinācija, kas rada vismazāko transakcijas kopsummu vai lielāko kopējo atlaidi. Ja atlaides summa mainās atbilstoši nopirkto preču cenai, piemēram, parastās mazumtirdzniecības atlaides “pērc 1, saņem 1 X procentu atlaidi” (BOGO) gadījumā, šim procesam ir jāveic kombināciju optimizēšana.

Šis raksts attiecas uz programmu Microsoft Dynamics AX 2012 R3 ar KB 3105973 (2015. gada 2. novembra laidiens) vai jaunāku tās versiju un programmu Dynamics 365 Retail. Lai noteiktu kombinācijas atlaides, kas pārklājas, un tās laicīgi piemērotu, esam ieviesuši metodi, kā lietot atlaides, kas pārklājas. Šī metode tiek dēvēta par **robežvērtības ranžēšanu**. Robežvērtības ranžēšana tiek izmantota, ja iespējamo pārklāto atlaižu kombināciju novērtēšanai nepieciešamais laiks pārsniedz sliekšņvērtību, ko var konfigurēt lapā **Mazumtirdzniecības parametri**. Robežvērtības ranžēšanas metodes ietvaros tiek aprēķināta katras pārklātās atlaides vērtība, izmantojot kopīgo preču atlaides vērtību. Pēc tam pārklātās atlaides tiek lietotas secībā no lielākās relatīvās vērtības līdz mazākajai relatīvajai vērtībai. Detalizētu informāciju par jauno metodi skatiet sadaļā “Robežvērtība” šī raksta turpinājumā. Robežvērtības ranžēšana netiek lietota, ja citas transakcijā ietvertās preces neietekmē preces atlaides summas. Piemēram, šī metode netiek lietota divām parastajām atlaidēm vai parastajai atlaidei un vienas preces daudzuma atlaidei.

## <a name="discount-examples"></a>Atlaižu piemēri

Vienai preču kopai varat izveidot neierobežotu skaitu mazumtirdzniecības atlaižu. Taču, tā kā nepastāv nekāds ierobežojums, mēģinot aprēķināt dažādām precēm lietojamās atlaides, var rasties veiktspējas problēmas. Tālāk sniegtajā piemērā ir detalizētāk atainota šī problēma. 1. piemēra ietvaros tiek apstrādātas divas preces un divas pārklātas atlaides. 2. piemērā ir atainots, kā problēma attīstās, ja tiek pievienotas papildu preces.

### <a name="example-1-two-products-and-two-discounts"></a>1. piemērs: divas preces un divas atlaides

Šī piemēra ietvaros, lai varētu saņemt katru atlaidi, ir nepieciešamas divas preces, un atlaides nevar kombinēt. Piemēra ietvaros izmantoto atlaižu veids ir **Labākā cena**. Abas preces ir piemērotas abām atlaidēm. Tālāk ir norādītas abas atlaides.

![Divu labāko cenas atlaižu piemērs](./media/overlapping-discount-combo-01.jpg)

Jebkurām divām precēm labākā no šīm divām atlaidēm ir atkarīga no abu preču cenas. Ja abu preču cenas ir vienādas vai gandrīz vienādas, 1. atlaide ir labāka. Ja vienas preces cena ir daudz mazāka par otras preces cenu, 2. atlaide ir labāka. Lūk, matemātiskā kārtula šo divu atlaižu savstarpējai novērtēšanai.

![Kārtula atlaižu novērtēšanai](./media/overlapping-discount-combo-02.jpg)

> [!NOTE]
> Kad 1. preces cena ir vienāda ar divām trešdaļām no 2. preces cenas, tad abas atlaides ir vienādas. Šī piemēra ietvaros 1. atlaides faktiskā procentuālā vērtība mainās diapazonā no dažiem procentiem (ja abu preču cenas ļoti atšķiras) līdz 25 procentiem (ja abu preču cenas ir vienādas). 2. atlaides faktiskā procentuālā vērtība ir nemainīga. Tā vienmēr ir 20 procenti. Tā kā 1. atlaides faktiskā procentuālā vērtība var būt lielāka vai mazāka nekā 2. atlaide, tas, labākā atlaide ir atkarīga no abu preču cenas pirms atlaides lietošanas. Šī piemēra ietvaros aprēķinu var veikt ātri, jo tiek lietotas tikai divas atlaides un tikai divām precēm. Pastāv tikai divas iespējamās kombinācijas: viens 1. atlaides lietojums vai viens 2. atlaides lietojums. Nav jāaprēķina nekādas permutācijas. Katras atlaides vērtība tiek aprēķināta, izmantojot abas preces, un tiek lietota labākā atlaide.

### <a name="example-2-four-products-and-two-discounts"></a>2. piemērs: četras preces un divas atlaides

Turpinājumā tiek lietotas četras preces un tās pašas divas atlaides. Visas četras preces ir piemērotas abām atlaidēm. Pastāv divpadsmit iespējamās kombinācijas. Piemēra beigās transakcijai tiek lietotas divas atlaides vienā no trim kombinācijām: divi 1. atlaides lietojumi, divi 2. atlaides lietojumi vai viens 1. atlaides un viens 2. atlaides lietojums. Lai atainotu iespējamās kombinācijas, tiek aplūkotas divas dažādas četru preču kopas ar dažādām cenām.

- Visām četrām precēm ir viena cena $ 15,00. Šādā gadījumā labākā atlaižu kombinācija ir divi 1. atlaides lietojumi. Divām precēm ir pilna cena, un divām ir 50 procentu atlaide. Transakcijas kopsumma ar atlaidi ir $ 45 (15 + 15 + 7,50 + 7,50), kas ir par $ 15 (25 procentiem) mazāka nekā kopsumma bez atlaides $ 60. 2. atlaide ir tikai $ 12 (20 procenti).
- Divas preces maksā $ 20 katra, viena prece maksā $ 15 un viena prece maksā $ 5. Šādā gadījumā labākā atlaižu kombinācija ir viens 2. atlaides lietojums un viens 1. atlaides lietojums. Tālāk esošajās tabulās ir norādītas atlaides.

Lai nolasītu tabulās sniegto informāciju, izmantojiet vienu preci no rindas un vienu preci no kolonnas. Piemēram, 1. atlaides tabulā, kombinējot divas preces ar cenu $ 20, iegūstat atlaidi $ 10. 2. atlaides tabulā, kombinējot preci ar cenu $ 15 un preci ar cenu $ 5, iegūstat atlaidi $ 4.

![Piemērs, kur ir izmantotas četras preces tām pašam divām atlaidēm](./media/overlapping-discount-combo-03.jpg)

Vispirms ir jānosaka vislielākā atlaide, ko var iegūt jebkurām divām precēm, lietojot jebkuru atlaidi. Divās tabulās ir norādītas atlaides summas visām divi preču kombinācijām. Tabulu kopējās daļas atbilst gadījumiem, kad prece tiek kombinēta pati ar sevi, kas nav iespējams, vai divu preču apgrieztajai kombinēšanai, kas rada tādu pašu atlaides summu un ko var ignorēt. Aplūkojot tabulas, varat konstatēt, ka 1. atlaide divām precēm ar cenu $ 20 ir lielākā atlaide, kas ir pieejama, lietojot jebkuru atlaidi visām četrām precēm. (Šī atlaide pirmajā tabulā ir iezīmēta zaļā krāsā.) Tādējādi atliek tikai prece ar cenu $ 15 un prece ar cenu $ 5. Vēlreiz aplūkojot abas tabulas, varat konstatēt, ka, šīm divām precēm lietojot 1. atlaidi, tiek iegūta atlaide $ 2,50, bet, tām lietojot 2. atlaidi, tiek iegūta atlaide $ 4. Tāpēc tiek izvēlēta 2. atlaide. Kopējā atlaide ir $ 14. Lai atvieglotu šī piemēra vizualizēšanu, tālāk ir sniegtas divas papildu tabulas, kurās ir redzamas visu iespējamo divu preču kombināciju faktiskās atlaides procentuālās vērtības gan 1., gan 2. atlaidei. Ir ietverta tikai puse no kombināciju saraksta, jo šīm divām atlaidēm nav svarīgi, kādā secībā abām precēm tiek lietota atlaide. Lielākā faktiskā atlaide (25 procenti) ir iezīmēta zaļā krāsā, un mazākā faktiskā atlaide (10 procenti) ir iezīmēta sarkanā krāsā.

![Faktiskās atlaides procentuālais daudzums visām divu preču kombinācijām abām atlaidēm](./media/overlapping-discount-combo-04.jpg)

> [!NOTE]
> Ja cenas atšķiras un ir jāsalīdzina divas atlaides vai vairāk, vienīgais veids, kā garantēt vislabākās atlaižu kombinācijas izvēli, ir novērtēt abas atlaides un tās salīdzināt.

## <a name="total-possible-combinations"></a>Visas iespējamās kombinācijas

Šajā sadaļā tiek turpināts iepriekšējā sadaļā apskatītais piemērs. Tiek pievienotas papildu preces un vēl viena atlaide un noteikts, cik daudz kombināciju ir jāaprēķina un jāsalīdzina. Tālāk esošajā tabulā ir norādīts iespējamo atlaižu kombināciju skaits atbilstoši preču daudzuma palielinājumam. Tabulā ir atainots divu pārklātu atlaižu gadījums, kā tas ir aprakstīts iepriekšējā piemērā, fan trīs pārklātu atlaižu gadījums. Novērtējamo iespējamo atlaižu kombināciju skaits drīz vien kļūst tik liels, ka pat ātrdarbīgs dators nespēj veikt aprēķinu un salīdzinājumu tik ātri, cik ir vajadzīgs, strādājot ar mazumtirdzniecības transakcijām.

![Iespējamo atlaižu kombināciju skaits, palielinoties preču daudzumam](./media/overlapping-discount-combo-05.jpg)

Ja tiek lietots vēl lielāks daudzums vai vēl vairāk pārklāto atlaižu, tad kopējais iespējamo atlaižu kombināciju skaits drīz vien sasniedz miljonus, un kombināciju novērtēšanai un vislabākās iespējamās kombinācijas izvēlei drīz vien ir vajadzīgs daudz ilgāks laiks. Mazumtirdzniecības cenas noteikšanas programmā ir veiktas dažas optimizācijas, lai samazinātu novērtējamo kombināciju skaitu. Taču, tā kā pārklāto atlaižu skaits un transakcijās ietvertais daudzums nav ierobežots, vienmēr, kad pastāv pārklātās atlaides, ir jānovērtē ļoti daudz kombināciju. Šo problēmu palīdz novērst robežvērtības ranžēšanas metode.

## <a name="marginal-value-method"></a>Robežvērtības metode

Lai novērstu eksponenciāli pieaugošā novērtējamo kombināciju daudzuma problēmu, ir pieejama optimizācijas metode, kas nodrošina katras atlaides vērtības aprēķināšanu katrai kopīgajai precei preču kopā, kurai var lietot divas atlaides vai vairāk. Šī vērtība tiek dēvēta par kopīgo preču atlaides **robežvērtību**. Robežvērtība ir vidējais kopējās atlaides summas palielinājums katrai precei, lietojot kopīgajām precēm katru atlaidi. Robežvērtība tiek aprēķināta, aprēķinot kopējo atlaides summu (DTotal), atņemot atlaides summu bez kopīgajām precēm (DMinus\\ Shared) un dalot iegūto starpību ar kopīgo preču skaitu (ProductsShared).

![Formula robežvērtības aprēķināšanai](./media/overlapping-discount-combo-06.jpg)

Kad ir aprēķināta katras atlaides robežvērtība kopīgo preču kopā, tad kopīgajām precēm tiek lietotas visas atlaides secībā no lielākās robežvērtības līdz mazākajai robežvērtībai. Šīs metodes ietvaros ikreiz pēc atsevišķas atlaides instances lietošanas netiek salīdzinātas visas atlikušās atlaižu iespējas. Tā vietā tiek vienu reizi salīdzinātas pārklātās atlaides, kas pēc tam tiek lietotas noteiktajā secībā. Netiek veikta papildu salīdzināšana. Sliekšņvērtību programmatūras pārslēgšanai uz robežvērtības metodi varat konfigurēt lapas **Mazumtirdzniecības parametri** cilnē **Atlaide**. Pieņemamais kopējās atlaides parēķina laiks atšķirtas dažādās mazumtirdzniecības nozarēs. Taču parasti šis laiks ir no dažiem desmitiem milisekunžu līdz vienai sekundei.
