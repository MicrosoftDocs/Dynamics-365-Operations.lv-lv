---
title: "Kreditoru rēķinu izrakstīšanas automatizācija"
description: "Šajā tēmā ir paskaidrots, kādi līdzekļi ir pieejami kreditoru rēķinu (arī to rēķinu, kam ir pielikumi) automatizācijai visā procesa garumā."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 00de566dcfbd3eb8c72816f66599863fa6cd1a41
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---
# <a name="vendor-invoice-automation"></a>Kreditoru rēķinu izrakstīšanas automatizācija

Šajā tēmā ir paskaidrots, kādi līdzekļi ir pieejami kreditoru rēķinu (arī to rēķinu, kam ir pielikumi) automatizācijai visā procesa garumā.

Organizācijas, kast vēlas uzlabot savus kreditoru procesus, rēķinu apstrādi bieži norāda kā vienu no galvenajiem procesiem, kura efektivitāti ir nepieciešams palielināt. Daudzos gadījumos šīs organizācijas papīra rēķinu apstrādi uztic trešās puses optiskās rakstzīmju pazīšanas (OCR) pakalpojumu sniedzējam. Viņi saņem ar mašīnu lasāmus rēķina metadatus kopā ar skenētu katra rēķina attēlu. Automatizācijas nolūkos tiek izveidots “pēdējās jūdzes” risinājums, lai iespējotu šo artefaktu patēriņu rēķinu apstrādes sistēmā. Microsoft Dynamics 365 for Finance and Operations Enterprise izdevums tagad komplektācijā nodrošina šo “pēdējās jūdzes” automatizāciju ar rēķinu automatizācijas risinājuma palīdzību.

## <a name="solution-context"></a>Risinājuma konteksts

Rēķinu automatizācijas risinājums nodrošina standarta interfeisu, kas var pieņemt rēķina metadatus rēķina virsrakstam un rēķina rindām, kā arī pielikumiem, kas attiecas uz rēķinu. Jebkura ārējā sistēma, kas var ģenerēt šim interfeisam atbilstošus artefaktus, varēs programmatūrā Finance and Operations nosūtīt plūsmu automātiskai rēķinu un pielikumu apstrādei.

Tālāk esošajā attēlā ir parādīts parauga integrācijas scenārijs, kurā uzņēmums Contoso kopā ar OCR pakalpojumu sniedzēju izmanto kreditora rēķinu apstrādi. Uzņēmuma Contoso kreditori pakalpojumu sniedzējam sūta rēķinus, izmantojot e-pastu. Izmantojot OCR apstrādi, pakalpojumu sniedzējs ģenerē rēķina metadatus (virsrakstu un/vai rindas) un skenēto rēķina attēlu. Pēc tam integrācijas slānis šos artefaktus pārveido tā, lai programmatūra Finance and Operations varētu tos patērēt.

![Parauga integrācijas scenārijs](media/vendor_invoice_automation_01.png)

Ja ir nepieciešama rēķinu integrācija, ir iespējamas vairākas iepriekšējā scenārija variācijas. Datu migrācija ir cits lietošanas gadījums, kurā šo interfeisu var izmantot rēķinu un pielikumu izveidei programmatūrā Finance and Operations.

### <a name="solution-components"></a>Risinājuma komponenti

Risinājuma pēdas nospiedums sastāv no tālāk norādītajiem komponentiem.

+ Datu elementi rēķina virsrakstam, rēķina rindām un rēķina pielikumiem
+ Izņēmumu apstrāde rēķiniem
+ Līdzās novietotu pielikumu skatītājs rēķinos

Atlikusī daļa šajā tēmā veltīta detalizētiem aprakstiem par šiem risinājuma komponentiem.

## <a name="data-entities"></a>Datu elementi

Datu pakotne ir darba vienība, kas ir jānosūta uz programmatūru Finance and Operations, lai varētu izveidot rēķina virsrakstus, rēķina rindas un rēķina pielikumus. Artefaktiem, kas veido datu pakotni, ir izmantoti tālāk norādītie datu elementi.

+ Kreditora rēķina virsraksts
+ Kreditora rēķina rinda
+ Kreditora rēķina dokumenta pielikums

Kreditora rēķina dokumenta pielikums ir jauns datu elements, kas ir ieviests kā daļa no šī līdzekļa. Kreditora rēķina virsraksta elements ir modificēts tā, lai tas atbalstītu pielikumus. Kreditora rēķina rindas elements nav modificēts šim līdzeklim.

Šajā tēmā nav sniegta detalizēta datu pakotnes definīcija. Tajā arī nav izskaidrots, kā izveidot datu pakotnes. Šo informāciju skatiet sadaļā [Datu elementi un pakotņu struktūra](../../dev-itpro/data-entities/data-entities-data-packages.md).

Lai ātri ģenerētu testa datus, kas ietver rēķinus un pielikumus, veiciet tālāk norādītās darbības.

1. Pierakstieties savā Finance and Operations instancē.
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
+ Kad datu pakotne, kas ietver rēķinus, ir nosūtīta uz programmatūru Finance and Operations, izsaucējs (t.i., integrācijas programma, kas darbojas ārpus programmatūras Finance and Operations) var HTTP pieprasījumā skaidri norādīt uzņēmuma ID. Šajā gadījumā uzņēmuma konteksts, kurā apstrādes darbs tiek izpildīts programmatūrā Finance and Operations, tiek ignorēts, un rēķini tiek importēti uzņēmumā, kas tika nodots, izmantojot HTTP pieprasījumu.

> [!NOTE]
> Šī izturēšanās ir standarta datu pārvaldības izturēšanās. Tā ir izskaidrota šeit saistībā ar rēķiniem.

## <a name="exception-processing"></a>Izņēmumu apstrāde

Scenārijos, kuros kreditora rēķini programmatūrā Finance and Operations nonāk, izmantojot integrāciju, ir nepieciešams viegls veids, kā kreditoru grupas dalībniekam apstrādāt izņēmumus vai neizdevušos rēķinus un izveidot gaidošos rēķinus no rēķiniem, kas neizdevās. Šī izņēmumu apstrāde kreditoru rēķiniem tagad ir daļa no Finance and Operations.

### <a name="exceptions-list-page"></a>Izņēmumu saraksta lapa

Jaunā rēķinu izņēmumu saraksta lapa ir pieejama šeit: **Kreditori** > **Rēķini** > **Importēšanas kļūmes** > **Kreditoru rēķini, kuru importēšana bija nesekmīga**. Šajā lapā ir parādīti visi kreditora rēķina virsraksta ieraksti no datu elementa Kreditora rēķina virsraksts izstādīšanas tabulas. Ņemiet vērā, ka tos pašus ierakstus varat skatīt no darbvietas **Datu pārvaldība**, kurā varat arī veikt tās pašas darbības, kas ir nodrošinātas izņēmumu apstrādes līdzeklī. Tomēr izņēmumu apstrādes līdzekļa nodrošinātais lietotāja interfeiss ir optimizēts funkcionālajam lietotājam.

![Izņēmumu saraksta lapa](media/vendor_invoice_automation_02.png)

Šajā saraksta lapā ir tālāk norādītie lauki, kas tajā nonāk ar plūsmu.

+ **Uzņēmums** — uzņēmums, kam pieder rēķins
+ **Kļūdas ziņojums** — kļūdas ziņojums, ko sniedz datu pārvaldības struktūra, lai izskaidrotu, kādēļ nevarēja izveidot rēķinu
+ **Numurs** — rēķina numurs
+ **Rēķina konts**
+ **Nosaukums** — kreditora nosaukums
+ **Kreditora konts**
+ **Pirkšanas pasūtījums** — rēķina pirkšanas pasūtījuma (PP) numurs
+ **Grāmatošanas datums**
+ **Rēķina datums**
+ **Rēķina apraksts**
+ **Valūta**
+ **Žurnāls**
+ **Rindas atsauce** — identifikators, kas ir no ārējās sistēmas

    > [!NOTE]
    > Rindas atsauce nav rēķina ID.

Šajā saraksta lapā ir arī priekšskatījuma rūts, kuru var izmantot tālāk norādītajos veidos.

+ Skatiet visu kļūdas ziņojumu, lai jums nebūtu jāizvērš kolonna **Kļūdas ziņojums** režģī.
+ Skatiet visu rēķina pielikumu sarakstu, ja rēķinam tādi ir.

Saraksta lapa atbalsta arī tālāk norādītās darbības.

+ **Rediģēt** — atveriet izņēmumu ierakstu rediģēšanas režīmā, lai labotu problēmas.
+ **Opcijas** — piekļūstiet standarta opcijām, kas ir pieejamas saraksta lapās. Varat izmantot opciju **Pievienot darbvietai**, lai izņēmumu saraksta lapu piespraustu savai darbvietai kā sarakstu vai elementu.

### <a name="exception-details-page"></a>Detalizētas informācijas par izņēmumu lapa

Kad sākat rediģēšanas režīmu, tiek parādīta detalizētās informācijas par izņēmumu lapa rēķinam, kuram ir problēmas. Ja rēķinam ir pielikumi, rēķins un noklusējuma pielikums tiek rādīti līdzās detalizētās informācijas par izņēmumu lapā.

![Detalizētas informācijas par izņēmumu lapa](media/vendor_invoice_automation_03.png)

Iepriekšējā attēlā ienākošajam kreditora rēķina virsrakstam nebija nevienas rindas. Tāpēc rindu sadaļa ir tukša.

Detalizētās informācijas par izņēmumu lapa atbalsta tālāk norādīto operāciju.

+ **Izveidot gaidošu rēķinu** — kad būsit labojis problēmas rēķinā kā daļu no izņēmumu apstrādes, varat noklikšķināt uz šīs pogas, lai izveidotu gaidošo rēķinu. Gaidošo rēķinu izveide notiek fonā (kā asinhrona operācija).

### <a name="shared-service-vs-organization-based-exception-processing"></a>Koplietoto pakalpojumu izņēmumu apstrāde salīdzinājumā ar apstrādi, kuras pamatā ir organizācija

Izņēmumu saraksta lapa atbalsta standarta drošības struktūras, kuras darbvieta **Datu pārvaldība** atbalsta izstādīšanas ierakstu apstrādei. Rēķinu importēšanas darbu var nodrošināt tālāk norādītajos veidos.

+ Pēc lietotāja lomas
+ Pēc lietotāja
+ Pēc juridiskās personas

![Importēšanas darbs, kas ir nodrošināts pēc lietotāja lomas un juridiskās personas](media/vendor_invoice_automation_04.png)

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

### <a name="security"></a>Drošība

Tālāk norādītās pielikumu skatītāja darbības tiek kontrolētas, izmantojot no lomas atkarīgu drošību.

+ Iezīmēšana
+ Bloķēts
+ Anotēšana

### <a name="pending-vendor-invoices-page"></a>Lapa Gaidošie kreditoru rēķini

Tālāk norādītās privilēģijas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi vai lasīšanas/rakstīšanas piekļuvi iezīmēšanas, bloķēšanas un anotēšanas darbībām.

+ **Uzturēt kreditora rēķina attēlu** — šī privilēģija nodrošina lasīšanas/rakstīšanas piekļuvi.
+ **Skatīt kreditora rēķina attēlu** — šī privilēģija nodrošina tikai lasīšanas piekļuvi.

Tālāk norādītie pienākumi pielikumu skatītājam nodrošina tikai lasīšanas vai lasīšanas/rakstīšanas piekļuvi tālāk aprakstītajām darbībām.

+ **Uzturēt kreditoru rēķinus** — šim pienākumam ir piešķirta privilēģija Uzturēt kreditora rēķina attēlu.
+ **Iegūt informāciju par kreditora rēķina statusu** — šim pienākumam ir piešķirta privilēģija Skatīt kreditora rēķina attēlu.

Tālāk norādītās lomas pielikumu skatītājam nodrošina tikai lasīšanas vai lasīšanas/rakstīšanas piekļuvi tālāk aprakstītajām darbībām.

+ **Kreditoru darbinieks** un **Kreditoru vadītājs** — šīm lomām ir piešķirts pienākums Uzturēt kreditoru rēķinus.
+ **Kreditoru darbinieks**, **Kreditoru vadītājs**, **Darbinieks, kas ir atbildīgs par kreditoru centralizētajiem maksājumiem**, un **Darbinieks, kas ir atbildīgs par kreditoru maksājumiem** — šīm lomām ir piešķirts pienākums Iegūt informāciju par kreditora rēķina statusu.

### <a name="invoice-exception-details-page"></a>Detalizētas informācijas par rēķina izņēmumu lapa

Tālāk norādītās privilēģijas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi vai lasīšanas/rakstīšanas piekļuvi iezīmēšanas, bloķēšanas un anotēšanas darbībām.

> [!NOTE]
> Šajā sadaļā minētās komplektācijā iekļautās lomas rēķina attēliem pielikumu skatītājā nodrošina tikai lasīšanas piekļuvi. Ja lomai ir jābūt arī rakstīšanas piekļuvei attēliem, varat piešķirt rakstīšanas piekļuvi šai lomai, izmantojot šeit aprakstīto privilēģiju un pienākumu.

+ **Uzturēt kreditora rēķina virsraksta elementa attēlu** — šī privilēģija rēķina attēliem pielikumu skatītājā nodrošina lasīšanas/rakstīšanas piekļuvi.
+ **Skatīt kreditora rēķina virsraksta elementa attēlu** — šī privilēģija rēķina attēlam pielikumu skatītājā nodrošina tikai lasīšanas piekļuvi.

Tālāk norādītie pienākumi pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi tālāk aprakstītajām darbībām.

+ **Uzturēt kreditoru rēķinus** — šim pienākumam ir piešķirta privilēģija Uzturēt kreditora rēķina virsraksta elementa attēlu.

Tālāk norādītās lomas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi tālāk aprakstītajām darbībām.

+ **Kreditoru darbinieks** un **Kreditoru vadītājs** — šīm lomām ir piešķirts pienākums Uzturēt kreditoru rēķinus.

Pēc noklusējuma, ja lietotāja loma sniedz rediģēšanas tiesības jebkurā lapā, lietotājam rediģēšanas tiesības būs arī pielikumu skatītājā iezīmēšanas, bloķēšanas un anotēšanas darbībām. Tomēr, ja pastāv scenāriji, kuros noteiktai lomai ir nepieciešamas rediģēšanas tiesības lapā, bet ne pielikumu skatītājā, to var panākt, izmantojot atbilstošās privilēģijas no iepriekšējā saraksta.

