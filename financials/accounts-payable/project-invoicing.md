---
title: "Projekta rēķinu izrakstīšana"
description: "Šajā rakstā ir sniegts pārskats par projekta rēķinu izrakstīšanu laika un materiālu projektiem, kā arī fiksētas cenas projektiem. Tajā ir ietverta informācija par rēķinu priekšlikumiem (rēķinus sagatavēm), rēķinu kontroli, starpkontu rēķinu izrakstīšanu, rēķinu izrakstīšanu kreditoriem un kredīta notām."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8ab09d19cf22f3c57fbb92de283d9a05f38b11ff
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="project-invoicing"></a>Projekta rēķinu izrakstīšana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts pārskats par projekta rēķinu izrakstīšanu laika un materiālu projektiem, kā arī fiksētas cenas projektiem. Tajā ir ietverta informācija par rēķinu priekšlikumiem (rēķinus sagatavēm), rēķinu kontroli, starpkontu rēķinu izrakstīšanu, rēķinu izrakstīšanu kreditoriem un kredīta notām.

Projekta veids nosaka pielietojamo rēķina izrakstīšanas procedūru. Rēķinu var izrakstīt tikai par abiem ārējiem projektu tipiem — Laiks un materiāli un Fiksēta cena. Laika un materiālu projekti, kā arī fiksētas cenas projekti vienmēr ir piesaistīti projekta līgumam.

-   **Fiksētas cenas projekti** — debitora rēķina summa ir balstīta uz rēķina norēķinu grafikiem. Rēķina izrakstīšana tiek veikta ar starpkonta iestatīšanu, kas tiek saukta arī par norēķinu grafiku. Fiksētas cenas projektiem rēķinu var izrakstīt par projektu vai par projekta līgumu.
-   **Laika un materiālu projekti** — debitora rēķina summa ir balstīta uz projektos ievadītajām transakciju rindām. Transakciju rēķinus var izrakstīt par projektu vai par projekta līgumu.

Laika un materiālu projektus un fiksētas cenas projektus rēķinu projektiem var piesaistīt trīs veidos:

-   **Starpkonta rēķina izrakstīšana** — laika un materiālu projektiem, kā arī fiksētas cenas projektiem var veikt starpkonta rēķina izrakstīšanu. Ir nepieciešami divi starpkontu iestatījumi — viens katram projekta tipam.
-   **Rēķinu izrakstīšana periodiskajā sadaļā** — izmantojot periodiskās funkcijas, rēķinus var izrakstīt par transakcijām dažādos projektos. Periodiskās funkcijas sniedz apskatu par rēķinā iekļaujamajām transakcijām.
-   **Lietojot kredīta notas rēķina izrakstīšanai** — kredīta notu var izveidot gan laika un materiālu projektiem, gan fiksētas cenas projektiem.

## <a name="invoice-proposals"></a>Rēķinu priekšlikumi
Lai projektam varētu izveidot debitora rēķinu, varat izveidot sākotnējo rēķinu jeb rēķina priekšlikumu. Rēķina priekšlikumā varat atlasīt projekta transakcijas, ko iekļaut projekta rēķinā. Pēc tam varat pārskatīt rēķina detaļas, pirms šo projekta rēķinu grāmatojat un nosūtāt debitoram vai citam finansējuma avotam.

### <a name="creating-invoice-proposals"></a>Rēķinu priekšlikumu izveidošana

Rēķinu priekšlikumus varat izveidot, darījumu sarakstā manuāli atlasot norādītajam projektam. Varat arī iestatīt norēķinu kārtulas, kurās norādīts, kad rēķina priekšlikumu izveidot automātiski. Varat, piemēram, izveidot norēķinu kārtulu, lai rēķina priekšlikumu izveidotu, kad izpildīti 25 procenti, 50 procenti, 75 procenti un 100 procenti no projekta darba. 

Rēķinu priekšlikumus varat izveidot tālāk uzskaitītajām transakcijām.

-   Stundu, izdevumu un citas projekta transakcijas
-   Summas, ko debitori ietur iepriekšējos projekta rēķinos
-   Kredīta notas
-   Summas, ko debitors jums samaksāja pirms projekta uzsākšanas

Rēķina priekšlikumā varat izveidot papildmaksu transakcijas. Varat arī modificēt pārdošanas cenu par stundu, izdevumiem, krājumu un maksas darījumiem. Kad grāmatojat rēķina priekšlikumu, atjauninātās cenas un transakcijas tiek pievienotas projekta atskaitēm un transakciju vēsturei. 

Lai projektam izveidotu vairākus debitora rēķinus, ir jāizveido rēķina priekšlikums katram rēķinam. Varat izveidot rēķinus, piemēram, atkarībā no darījuma tipa. Lai vienā debitora rēķinā norādītu stundu skaitu, bet citā rēķinā norādītu krājumus, ir jāizveido atsevišķi rēķinu priekšlikumi stundu transakcijām un papildmaksas transakcijām. 

Ja projektam ir vairāki finansējuma avoti, varat izveidot atsevišķu rēķina priekšlikumu katram finansējuma avotam. Lapā **Finansējuma nosacījumu sadalījumi** varat definēt, kādu procentuālo daudzumu no transakcijas summas piešķirt katram finansējuma avotam, kā arī avotu noapaļošanas atšķirību grāmatošanai.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Debitoru rēķinu veidošana no rēķinu priekšlikumiem

Pēc rēķina priekšlikuma izveidošanas un iegrāmatošanas šajā rēķina priekšlikumā iekļautajiem darījumiem automātiski tiek izveidots debitora rēķins. 

Pirms rēķina priekšlikuma grāmatošanas varat tam pievienot transakcijas vai no tā dzēst transakcijas. Varat, piemēram, noņemt izdevumu transakcijas, kas bija iegrāmatotas projektā, bet par ko debitoram nav jāmaksā. 

Ja jūsu organizācija pieprasa, ka rēķinu priekšlikumi pirms grāmatošanas tiek pārskatīti, tad rēķina priekšlikums, iespējams, pirms grāmatošanas ir jāapstiprina, izmantojot darbplūsmu “Pārskatīt projekta rēķinu priekšlikumus”.

## <a name="on-account-invoicing"></a>Starpkonta rēķinu izrakstīšana
Projektam starpkonta rēķinā ievadītā summa tiek noteikta, pamatojoties uz grafiku, pabeigtību un citiem norēķinu nosacījumiem, kas ir norādīti saistītajā projekta līgumā. Šī summa netiek aprēķināta, pamatojoties uz stundām, krājumiem, izdevumiem vai papildmaksām, kas tiek grāmatotas projektā. 

Lai projekta rēķinam varētu pievienot starpkontu darījumu, jums vispirms ir jāizveido starpkontu transakcija laika un materiālu projektam vai fiksētas cenas projektam. Starpkontu transakcijā ievadiet summu, par ko debitoram ir jāizraksta rēķins. Lai izveidotu projekta rēķinu par šo summu, izveidojiet sākotnējo rēķinu (rēķina priekšlikumu). Rēķina priekšlikumā atlasiet starpkontu transakciju. Pirms projekta rēķina izveidošanas starpkontu informāciju varat pārskatīt rēķina priekšlikumā.

### <a name="fixed-price-projects"></a>Fiksētas cenas projekti

Fiksētas cenas projektiem starpkontu darījumu pamatā ir iepriekš noteikts atskaites punkts, piegādes vienība vai apmaksa atbilstoši progresam, kas ir norādīta projekta līgumā. Katram maksājumam, kas ir jāsaņem no projekta debitora, tiek izveidota viena rinda. Nav nepieciešami nekādi ieturējumi.

### <a name="time-and-material-projects"></a>Laika un materiālu projekti

Laika un materiālu projektiem varat izrakstīt rēķinu debitoram vai citam finansējuma avotam par priekšapmaksas summu, izmantojot starpkontu rēķina priekšlikumu. Starpkontu darījumu ievadīšana vienā rindā. Pēc izvēles varat ievadīt papildu rindas kā ieturējumus, lai izlīdzinātu debitora jau veikto priekšapmaksu nobīdes. Lai izveidotu ieturējumu rindas, summas priekšā ierakstiet mīnus zīmi.

## <a name="invoice-control"></a>Rēķinu kontrole
Rēķinu kontroli var izmantot, lai sekotu līdzi gan rēķinā iekļautajām, gan neiekļautajām transakcijām, un lai šīs transakcijas analizētu pret piedāvājumiem attiecībā uz savu projektu visu dzīves ciklu no piedāvājuma stadijas līdz pabeigšanai. Varat redzēt, par kurām transakcijām tika iekasēta maksa konkrētā projektā un kuras rindas ir iekļautas rēķinā. Varat arī redzēt atsevišķas transakcijas, tāpēc pēc grāmatošanas varat tās koriģēt.

## <a name="invoicing-fixed-price-projects"></a>Fiksētas cenas projektu rēķinu izrakstīšana
Lai izrakstītu rēķinu par fiksētas cenas projektu, ir nepieciešams definēt norēķinu grafiku un izpildīt rēķinu izrakstīšanas procedūru.

### <a name="billing-schedule"></a>Norēķinu grafiks

Fiksētas cenas projektiem rēķinus varat izrakstīt atbilstoši norēķinu grafikam. Norēķinu grafiks tiek definēts pēc viena vai vairākiem projekta atskaites punktiem. Katram atskaites punktam varat definēt noteiktu datumu, pārdošanas valūtu, pārdošanas cena un aktivitāti. 

Piemēram, varat iestatīt tālāk norādīto norēķinu grafiku.

-   20 procenti, kas tiek parakstīts projekta līgums
-   30 procenti pirmās piegādes laikā
-   15 procenti otrās piegādes laikā
-   35 procenti pēdējās piegādes laikā

### <a name="invoicing-procedure"></a>Rēķinu piestādīšanas procedūra

Kad atskaites punktu maksājumi ir gatavi rēķina izrakstīšanai, izmantojiet šo procedūru rēķinu izrakstīšanai par starpkontu summām.

## <a name="vendor-invoicing"></a>Kreditora rēķini
Kad pasūtāt kādu krājumu no kreditora un piešķirat šo krājumu kādam projektam, tad rindas rekvizīts, ko šim krājumam atlasījāt no pirkšanas pasūtījuma rindas, nosaka, vai iegādātais krājums tiek iekļauts debitoram izrakstītajā rēķinā. Ja iestatāt noklusējuma rindu rekvizītus, tie tiek rādīti šim krājumam pirkšanas pasūtījuma rindā (Detalizēta informācija par rindu &gt; Projekts &gt; Rindas rekvizīts). Rindas rekvizītu var mainīt divējādi:

-   Izrakstiet rēķinu projekta debitoram par šo krājumu: pirkšanas pasūtījumā iestatiet krājuma rindas rekvizītu uz apmaksājamu vērtību, un pēc tam izrakstiet rēķinu debitoram, izmantojot pareizo projektu rēķinu izrakstīšanas metodi.
-   Neizrakstiet rēķinu projekta debitoram par šo krājumu: pirkšanas pasūtījuma rindā šim krājumam neatlasiet rindas rekvizītu **Apmaksājams**. Pēc tam varat izrakstīt rēķinu par pirkšanas pasūtījumu, un nav nepieciešams veikt turpmākas darbības.

## <a name="credit-notes"></a>Kredīta notas
Ja debitora rēķina summas vērtība ir negatīva, rēķins tiek klasificēts kā kredīta nota. Kad dokuments tiek drukāts, tā virsraksts ir “Kredīta nota”. 

Kad izveidojat kredīta notu, lai kreditētu summu, kas iepriekš ir tikusi uzrādīta rēķinā, vispirms ir jāatlasa rēķinā uzrādītā summa kreditēšanai. Pēc tam jums ir jāizveido kredīta nota, vadoties pēc tās pašas procedūras, ko lietotu parasta debitora rēķina izveidošanai. Citiem vārdiem — atlasiet transakcijas, kas iepriekš tika grāmatotas debitora rēķinam, un pēc tam izveidojiet un grāmatojiet kredīta notas priekšlikumu. 

Viens un tas pats dokuments var ietvert transakcijas, kas ir atlasītas kreditēšanai, kredīta transakcijas un transakcijas, kas ir grāmatotas. Šis dokuments tiek klasificēts kā rēķins vai kredīta nota — atkarībā no tā, vai kopsumma ir pozitīva vai negatīva. 

Lai kreditētu rēķinā iekļautu summu, jums vispirms ir jāatlasa rēķinā iekļautā summa, kuru vēlaties kreditēt, un pēc tam jāizveido kredīta nota. Kredīta nota ir jāizveido, vadoties pēc tās pašas procedūras, ko jūs izmantotu debitora rēķina izveidošanai. 

Varat izveidot rēķinu ar negatīvu summu — šāds rēķins kļūst par rēķinu, kurš tiek klasificēts kā kredīta nota. Lai izveidotu un drukātu kredīta notu, jums ir jāatlasa transakcijas, kas iepriekš tika grāmatotas debitora rēķinam, un pēc tam jāmaina šīs transakcijas. Izņemot gadījumus, kad juridiskās personas primārā adrese ir Vācijā, rēķina nosaukums ir “Labojošs rēķins”.



