---
title: Rēķinu automatizācija skenētajiem dokumentiem
description: Šis raksts skaidro funkcijas, kas pieejamas kreditoru rēķinu beigu automatizācijai, pat rēķinus, kas ietver pielikumus.
author: abruer
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0449a13989bad45cf0456a2678e5724036d2af3d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070700"
---
# <a name="invoice-automation-for-scanned-documents"></a>Rēķinu automatizācija skenētajiem dokumentiem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidroti datu elementi, kas ir pieejami kreditoru rēķinu beigu automatizācijai, ieskaitot rēķinus ar pielikumiem.

Organizācijas, kast vēlas uzlabot savus kreditoru procesus, rēķinu apstrādi bieži norāda kā vienu no galvenajiem procesiem, kura efektivitāti ir nepieciešams palielināt. Daudzos gadījumos šīs organizācijas papīra rēķinu apstrādi uztic trešās puses optiskās rakstzīmju pazīšanas (OCR) pakalpojumu sniedzējam. Viņi saņem ar mašīnu lasāmus rēķina metadatus kopā ar skenētu katra rēķina attēlu. Automatizācijas nolūkos tiek izveidots “pēdējās jūdzes” risinājums, lai iespējotu šo artefaktu patēriņu rēķinu apstrādes sistēmā. Tagad ir iespējota šī pēdējā soļa automatizācija, izmantojot rēķinu automatizācijas risinājumu.

## <a name="solution-context"></a>Risinājuma konteksts

Rēķinu automatizācijas risinājums nodrošina standarta interfeisu, kas var pieņemt rēķina metadatus rēķina virsrakstam un rēķina rindām, kā arī pielikumiem, kas attiecas uz rēķinu. Jebkura ārējā sistēma, kas var ģenerēt šim interfeisam atbilstošus artefaktus, varēs nosūtīt plūsmu automātiskai rēķinu un pielikumu apstrādei.

Tālāk esošajā attēlā ir parādīts parauga integrācijas scenārijs, kurā uzņēmums Contoso kopā ar OCR pakalpojumu sniedzēju izmanto kreditora rēķinu apstrādi. Uzņēmuma Contoso kreditori pakalpojumu sniedzējam sūta rēķinus, izmantojot e-pastu. Izmantojot OCR apstrādi, pakalpojumu sniedzējs ģenerē rēķina metadatus (virsrakstu un/vai rindas) un skenēto rēķina attēlu. Pēc tam integrācijas slānis šos artefaktus pārveido tā, lai tos varētu patērēt.

![Parauga integrācijas scenārijs.](media/vendor_invoice_automation_01.png)

Ja ir nepieciešama rēķinu integrācija, ir iespējamas vairākas iepriekšējā scenārija variācijas. Datu migrācija ir cits lietošanas gadījums, kurā šo interfeisu var izmantot rēķinu un pielikumu izveidei.

### <a name="solution-components"></a>Risinājuma komponenti

Risinājuma pēdas nospiedums sastāv no tālāk norādītajiem komponentiem.

+ Datu elementi rēķina virsrakstam, rēķina rindām un rēķina pielikumiem
+ Izņēmumu apstrāde rēķiniem
+ Līdzās novietotu pielikumu skatītājs rēķinos

Pārējā šajā rakstā ir sniegti detalizēti šo risinājuma komponentu apraksti.

## <a name="data-entities"></a>Datu elementi

Datu pakotne ir darba vienība, kas ir jānosūta, lai varētu izveidot rēķina virsrakstus, rēķina rindas un rēķina pielikumus. Artefaktiem, kas veido datu pakotni, ir izmantoti tālāk norādītie datu elementi.

+ Kreditora rēķina virsraksts
+ Kreditora rēķina rinda
+ Kreditora rēķina dokumenta pielikums

Kreditora rēķina dokumenta pielikums ir jauns datu elements, kas ir ieviests kā daļa no šī līdzekļa. Kreditora rēķina virsraksta elements ir modificēts tā, lai tas atbalstītu pielikumus. Kreditora rēķina rindas elements nav modificēts šim līdzeklim.

Detalizētu informāciju par datu pakotnēm skatiet [datu pārvaldības pārskatā](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md). Papildinformāciju par to, kā izveidot datu pakotnes, izmantojot datu pārvaldības darbvietu, [skatiet Sadaļā Datu pakotņu apstrāde un patērēšana dynamics 365 finanšu un operāciju programmu risinājumā](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).

Lai ātri ģenerētu testa datus, kas ietver rēķinus un pielikumus, veiciet tālāk norādītās darbības.

1. Pierakstieties savā instancē.
1. Dodieties uz **Kreditori** > **Rēķini** > **Gaidošie kreditoru rēķini**.
1. Izveidojiet rēķinus ar rindām un pielikumiem.

    > [!NOTE]
    > Pielikumiem ir jābūt virsraksta pielikumiem. Pašlaik elements Kreditora rēķina dokumenta pielikums neatbalsta rindas pielikumus.

1. Atveriet darbvietu **Datu pārvaldība**.
1. Izveidojiet eksportēšanas darbu, kas ietver elementus Kreditora rēķina virsraksts, Kreditora rēķina rinda un Kreditora rēķina dokumenta pielikums.
1. Eksportējiet datus.
1. Lejupielādējiet eksportētos datus kā pakotni. Tagad pakotni varat izmantot datu importēšanai mērķa instancēs testēšanas nolūkos.

### <a name="determining-the-legal-entity-for-an-invoice"></a>Juridiskās personas noteikšana rēķinam

Rēķini, kas tiek importēti, izmantojot datu pakotnes, ar juridisko personu, kam tie pieder, var būt saistīti divos veidos.

+ Importēšanas darbs, kas apstrādā rēķinu, importē to tajā pašā uzņēmumā, kurā darbs tika plānots darbvietā **Datu pārvaldība**. Citiem vārdiem sakot, darba uzņēmums nosaka uzņēmumu, kam pieder rēķins.
+ Kad datu pakotne, kas ietver rēķinus, ir nosūtīta uz programmu Finance, izsaucējs (t.i., integrācijas programma, kas darbojas ārpus Finance) var HTTP pieprasījumā skaidri norādīt uzņēmuma ID. Šajā gadījumā uzņēmuma konteksts, kurā apstrādes darbs tiek izpildīts programmā Finance, tiek ignorēts, un rēķini tiek importēti uzņēmumā, kas tika nodots, izmantojot HTTP pieprasījumu.

> [!NOTE]
> Šī izturēšanās ir standarta datu pārvaldības izturēšanās. Tā ir izskaidrota šeit saistībā ar rēķiniem.

## <a name="exception-processing"></a>Izņēmumu apstrāde

Scenārijos, kuros kreditoru rēķini tiek ņemti vērā finansēs un operācijās, izmantojot integrāciju, kreditoru grupas dalībniekam ir jābūt viegls veids, kā apstrādāt izņēmumus vai neizdevušos rēķinus un izveidot neizlemto rēķinus, kas nav izrakstīti. Šī izņēmuma apstrāde kreditoru rēķiniem tagad ir daļa no finansēm un operācijām.

### <a name="vendor-invoices-that-failed-to-import-list-page"></a>Piegādātāju rēķini, kuriem neizdevās importēt saraksta lapu

Jaunā rēķinu izņēmumu saraksta lapa ir pieejama šeit: **Kreditori** > **Rēķini** > **Importēšanas kļūmes** > **Kreditoru rēķini, kuru importēšana bija nesekmīga**. Šajā lapā ir parādīti visi kreditora rēķina virsraksta ieraksti no datu elementa Kreditora rēķina virsraksts izstādīšanas tabulas. Ievērojiet, ka varat skatīt tos pašus ierakstus no darbvietas **Datu pārvaldība**. Varat arī veikt tās pašas darbības, kas tiek nodrošinātas izņēmumu apstrādes līdzeklī no darbvietas **Datu pārvaldība**. Izņēmuma apstrādes līdzeklis ir optimizēts funkcionālam lietotājam, kas atvieglo lietošanu.

![Izņēmumu saraksta lapa.](media/vendor_invoice_automation_02.png)

Šajā saraksta lapā ir tālāk norādītie lauki, kas tajā nonāk ar plūsmu.

+ **Uzņēmums** — uzņēmums, kam pieder rēķins
+ **Kļūdas ziņojums** — kļūdas ziņojums, ko sniedz datu pārvaldības struktūra, lai izskaidrotu, kādēļ nevarēja izveidot rēķinu
+ **Numurs** — rēķina numurs
+ **Rēķina konts**
+ **Nosaukums** — kreditora nosaukums
+ **Kreditora konts**
+ **Pirkšanas pasūtījums** — rēķina pirkšanas pasūtījuma (PP) numurs
+ **Grāmatošanas datums**
+ **Rēķina datums**
+ **Rēķina apraksts**
+ **Valūta**
+ **Žurnāls**
+ **Rindas atsauce** — identifikators, kas ir no ārējās sistēmas

    > [!NOTE]
    > Rindas atsauce nav rēķina ID.

Šajā saraksta lapā ir arī priekšskatījuma rūts, kuru var izmantot tālāk norādītajos veidos.

+ Skatiet visu kļūdas ziņojumu, lai jums nebūtu jāizvērš kolonna **Kļūdas ziņojums** režģī.

Saraksta lapa atbalsta arī tālāk norādītās darbības.

+ **Rediģēt** — atveriet izņēmumu ierakstu rediģēšanas režīmā, lai labotu problēmas.
+ **Opcijas** — piekļūstiet standarta opcijām, kas ir pieejamas saraksta lapās. Varat izmantot opciju **Pievienot darbvietai**, lai izņēmumu saraksta lapu piespraustu savai darbvietai kā sarakstu vai elementu.

### <a name="vendor-invoices-that-failed-to-import-details-page"></a>Piegādātāju rēķini, kuriem neizdevās importēt detālizētas informacijas lapu

Startējot rediģēšanas režīmu, tiks atvērta lapa **Kreditora rēķini, kam neizdevās importēt detalizētu informāciju** rēķinam, kuram ir izejas plūsma. Ja ir problēmas ar rēķinu, kam ir pielikums, pielikums netiks parādīts. Pielikums ir vēlreiz jāpievieno rēķinam.

Lapa **Kreditoru rēķini, kam neizdevās importēt detalizētu informāciju** ļauj izveidot gaidošo rēķinu. Kad rēķina izejas plūsmas ir fiksētas kā daļa no izņēmumu apstrādes, atlasiet pogu **Izveidot gaidošu rēķinu**, lai izveidotu gaidošo rēķinu. Gaidošais rēķins tiks izveidots fonā. 

### <a name="shared-service-vs-organization-based-exception-processing"></a>Koplietoto pakalpojumu izņēmumu apstrāde salīdzinājumā ar apstrādi, kuras pamatā ir organizācija

Izņēmumu saraksta lapa atbalsta standarta drošības struktūras, kuras darbvieta **Datu pārvaldība** atbalsta izstādīšanas ierakstu apstrādei. Rēķinu importēšanas darbu var nodrošināt tālāk norādītajos veidos.

+ Pēc lietotāja lomas
+ Pēc lietotāja
+ Pēc juridiskās personas

![Importēšanas darbs, kas ir nodrošināts pēc lietotāja lomas un juridiskās personas.](media/vendor_invoice_automation_04.png)

Ja rēķina importēšanas darbam ir konfigurēta drošība, izņēmumu saraksta lapa respektē šos iestatījumus. Lietotāji varēs redzēt tikai tos rēķinu izņēmumu ierakstus, ko šis iestatījums ļauj viņiem skatīt.

Piemēram, uzņēmums Contoso ir izlēmis apstrādāt rēķinu izņēmumus pēc juridiskās personas. Tādēļ drošība rēķina importēšanas darbā ir konfigurēta tā, lai lietotājs juridiskajā personā A varētu redzēt tikai juridiskās personas A rēķinu izņēmumus, savukārt lietotājs juridiskajā personā B varētu redzēt tikai juridiskās personas B izņēmumus. Šis iestatījums rēķinu izņēmumu pārvaldībai nodrošina pienākumu sadali.

Contoso var arī izlemt nelietot nekādu drošību, lai tie paši lietotāji varētu apstrādāt rēķinu izņēmumus visām juridiskajām personām. Šis iestatījums rēķinu izņēmumu pārvaldībai nodrošina koplietoto pakalpojumu scenāriju.

## <a name="side-by-side-attachment-viewer"></a>Līdzās novietotu pielikumu skatītājs

Lai palīdzētu jums viegli skatīt kreditoru rēķinu pielikumus, tālāk norādītajās lapās, kas tiek izmantotas rēķinu apstrādes procesā, tagad ir pieejams pielikumu skatītājs.

+ **Izņēmumu apstrāde**
+ Lapa **Gaidošie kreditoru rēķini** (pieejama arī rēķinu pārskatīšanas procesā)
+ Uzziņu lapa **Rēķinu žurnāls** (grāmatotajiem rēķiniem)

Tālāk norādīta galvenā funkcionalitāte, ko nodrošina pielikumu skatītājs.

+ Skatiet visus pielikumu tipus, ko atbalsta dokumentu pārvaldība (failus, attēlus, vietrāžus URL un piezīmes).
+ Skatiet vairāklapu TIFF failus.
+ Veiciet tālāk norādītās darbības attēlu failiem.
  + Iezīmējiet attēla daļas.
  + Bloķējiet attēla daļas.
  + Pievienojiet attēlam anotācijas.
  + Tuviniet un tāliniet attēlu.
  + Bīdiet attēlu.
  + Atsauciet darbības un atceltiem atsaukšanu tām.
  + Pielāgojiet attēla lielumu.

> [!NOTE]
> Šīs darbības ir pieejama tikai attēlu failiem (JPEG, TIFF, PNG u.c.). Visas izmaiņas, ko veicat attēlā, izmantojot šīs darbības, tiek saglabātas attēla failā. Pašlaik pielikumu skatītājs neietver versiju izveides un auditēšanas iespējas.

### <a name="default-attachment"></a>Noklusējuma pielikums

Ja kreditora rēķinā ir vairāk nekā viens pielikums, lapā **Pielikumi** vienu no dokumentiem varat iestatīt kā noklusējuma pielikumu. Opcija **Ir noklusējuma pielikums** ir jauna opcija, kas tika pievienota kā daļa no šī līdzekļa. Šī opcija ir parādīta arī datu elementā Kreditora rēķina dokumenta pielikums. Tādējādi noklusējuma pielikumu var iestatīt, izmantojot integrācijas.

Kā noklusējuma pielikumu var iestatīt tikai vienu dokumentu. Kad dokumentu esat iestatījis kā noklusējuma pielikumu, atverot rēķinu, tas tiek automātiski parādīts pielikumu skatītājā. Ja kā noklusējuma pielikumu neiestatāt nevienu dokumentu, atverot rēķinu, pielikumu skatītājs neparāda nevienu pielikumu.

### <a name="showhide-invoice-attachments"></a>Rēķinu pielikumu rādīšana/paslēpšana

Izmantojot uzziņu lapās **Izņēmumu apstrāde**, **Gaidošs rēķins** un **Rēķinu žurnāls** pieejamo jauno pogu, varat rādīt vai paslēpt pielikumu skatītāju.

## <a name="security"></a>Drošība

Tālāk norādītās pielikumu skatītāja darbības tiek kontrolētas, izmantojot no lomas atkarīgu drošību.

+ Iezīmēšana
+ Bloķēts
+ Anotēšana

### <a name="pending-vendor-invoices-page"></a>Lapa Gaidošie kreditoru rēķini

Tālāk norādītās privilēģijas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi vai lasīšanas/rakstīšanas piekļuvi iezīmēšanas, bloķēšanas un anotēšanas darbībām.

+ **Uzturēt kreditora rēķina attēlu** — šī privilēģija nodrošina lasīšanas/rakstīšanas piekļuvi.
+ **Skatīt kreditora rēķina attēlu** — šī privilēģija nodrošina tikai lasīšanas piekļuvi.

Tālāk norādītie pienākumi pielikumu skatītājam nodrošina tikai lasīšanas vai lasīšanas/rakstīšanas piekļuvi tālāk aprakstītajām darbībām.

+ **Uzturēt kreditoru rēķinus** — šim pienākumam ir piešķirta privilēģija Uzturēt kreditora rēķina attēlu.
+ **Iegūt informāciju par kreditora rēķina statusu** — šim pienākumam ir piešķirta privilēģija Skatīt kreditora rēķina attēlu.

Tālāk norādītās lomas pielikumu skatītājam nodrošina tikai lasīšanas vai lasīšanas/rakstīšanas piekļuvi tālāk aprakstītajām darbībām.

+ **Kreditoru darbinieks** un **Kreditoru vadītājs** — šīm lomām ir piešķirts pienākums Uzturēt kreditoru rēķinus.
+ **Kreditoru darbinieks**, **Kreditoru vadītājs**, **Darbinieks, kas ir atbildīgs par kreditoru centralizētajiem maksājumiem**, un **Darbinieks, kas ir atbildīgs par kreditoru maksājumiem** — šīm lomām ir piešķirts pienākums Iegūt informāciju par kreditora rēķina statusu.

### <a name="vendor-invoice-attachment"></a>Kreditoru rēķinu pielikums

Tālāk norādītās privilēģijas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi vai lasīšanas/rakstīšanas piekļuvi iezīmēšanas, bloķēšanas un anotēšanas darbībām.

> [!NOTE]
> Šajā sadaļā minētās komplektācijā iekļautās lomas rēķina attēliem pielikumu skatītājā nodrošina tikai lasīšanas piekļuvi. Ja lomai ir jābūt arī rakstīšanas piekļuvei attēliem, varat piešķirt rakstīšanas piekļuvi šai lomai, izmantojot šeit aprakstīto privilēģiju un pienākumu.

+ **Uzturēt kreditora rēķina virsraksta elementa attēlu** — šī privilēģija rēķina attēliem pielikumu skatītājā nodrošina lasīšanas/rakstīšanas piekļuvi.
+ **Skatīt kreditora rēķina virsraksta elementa attēlu** — šī privilēģija rēķina attēlam pielikumu skatītājā nodrošina tikai lasīšanas piekļuvi.

Tālāk norādītie pienākumi pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi tālāk aprakstītajām darbībām.

+ **Uzturēt kreditoru rēķinus** — šim pienākumam ir piešķirta privilēģija Uzturēt kreditora rēķina virsraksta elementa attēlu.

Tālāk norādītās lomas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi tālāk aprakstītajām darbībām.

+ **Kreditoru darbinieks** un **Kreditoru vadītājs** — šīm lomām ir piešķirts pienākums Uzturēt kreditoru rēķinus.

Pēc noklusējuma, ja lietotāja loma sniedz rediģēšanas tiesības jebkurā lapā, lietotājam rediģēšanas tiesības būs arī pielikumu skatītājā iezīmēšanas, bloķēšanas un anotēšanas darbībām. Tomēr, ja pastāv scenāriji, kuros noteiktai lomai ir nepieciešamas rediģēšanas tiesības lapā, bet ne pielikumu skatītājā, to var panākt, izmantojot atbilstošās privilēģijas no iepriekšējā saraksta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

