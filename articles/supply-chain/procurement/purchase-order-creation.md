---
title: Pirkšanas pasūtījuma izveidošana
description: Šajā rakstā ir izklāstīts process un opcijas, kad manuāli veidojat pirkšanas pasūtījumu.
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5454b9003105e4b44ec7577e5f8989c75554aeb9
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572219"
---
# <a name="create-purchase-orders"></a>Pirkšanas pasūtījuma izveidošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izklāstīts process un opcijas, kad manuāli veidojat pirkšanas pasūtījumu.

Kad veidojat pirkšanas pasūtījumu (PP), vispārīgā informācija par visu pasūtījumu tiek norādīta PP virsrakstā, un pēc tam jūs pievienojat vienu vai vairākas PP rindas. Šajā rakstā ir aprakstītas dažas no visbiežāk lietotajām opcijām, kas ir pieejamas.  

Pirkšanas pasūtījumu varat arī izveidot, kopējot rindas no cita pirkšanas pasūtījuma dokumenta vai pārdošanas pasūtījuma. Tādā gadījumā varat krājumiem mainīt zīmi uz pretējo, kā jūs rēķinā mainītu zīmi uz pretējo, lai norādītu kredītu.  

Lai gan pirkšanas pasūtījumus varat izveidot manuāli, tie parasti tiek ģenerēti no citiem procesiem. Pasūtījumus var izveidot automātiski, pamatojoties uz citiem dokumentiem, piemēram, uz pieprasījumiem. Tos var arī izveidot galvenās plānošanas procesa ietvaros, izmantojot ieplānotos pirkšanas pasūtījumus. Ja lietojat pirkšanas līgumus, pirkšanas pasūtījumus var izveidot, izmantojot darbību **Izpildīt pasūtījumu**. Automātiskai pirkšanas pasūtījuma izveidošanai pastāv arī uzlabotākas metodes. Piemēram, pasūtījumus varat izveidot, kad lietojat tiešo piegādi vai starpuzņēmumu pasūtījumu ķēdes.

## <a name="creating-a-purchase-order-header"></a>Pirkšanas pasūtījuma virsraksta izveidošana
Kad veidojat jaunu pirkšanas pasūtījumu, tiek atvērts dialoglodziņš, kurā varat ievadīt pirkšanas pasūtījuma virsrakstā visbiežāk izmantoto informāciju. Kad noklikšķināt uz **Labi**, lai aizvērtu šo dialoglodziņu, pasūtījums tiek izveidots, un pēc tam virsrakstā varat norādīt papildu informāciju.  

Pirmā informācija, kas jums ir jāapsver, kad veidojat pirkšanas pasūtījumu, ir šī pasūtījuma tips. Visbiežāk tiek izmantots tips **Pirkšanas pasūtījums**. Taču, ja ir nepieciešams kredītrēķins, varat izmantot tipu **Atgrieztais pasūtījums**.  

Laukā **Kreditora konts** ir jānorāda piegādātājs. Šim laukam varat meklēt pēc konta vai kreditora nosaukuma. Ja kreditors piegādā no vairākām vietām, bet izmanto vienu rēķina kontu, laukā **Rēķina konts** varat atlasīt šo rēķina kontu un pēc tam to izmantot ar dažādiem kreditora kontiem. Ja ir jāizveido pirkšanas pasūtījums precēm, kas netiks pasūtītas atkārtoti, varat izmantot opciju **Vienreizējs piegādātājs**. Šī opcija automātiski izveido jaunu kreditora kontu, kas ir atzīmēts kā vienreizējs konts, lai atbalstītu vēlāku tīrīšanas procesu vienreizējiem kontiem modulī **Kreditori**. Kad atlasāt kādu kreditora kontu, daudzi lauki pirkšanas pasūtījuma virsrakstā pārmanto noklusējuma vērtības no informācijas, kas ir saistīta ar šo kreditora kontu. No šī kreditora informācijas tiek kopēta, piemēram, noklusējuma piegādes vieta un noliktava. Taču šīs noklusējuma vērtības varat ignorēt, ja pirkums ir paredzēts citai vietai.  

Ja piegādātājs pasūtījumam ir norādījis atsauces numuru, šo informāciju varat ierakstīt laukā **Kreditora atsauce**. Atgrieztajiem pasūtījumiem jums ir jānorāda vērtība laukā **AKA**, lai atsauktos uz piegādātāja autorizāciju atgriešanas apstrādei.  

Ja ar pasūtījumu ir saistīts kāds pirkšanas līgums, jums šī informācija ir jānorāda laukā **Pirkšanas līgums**.  

Pirkšanas pasūtījuma virsraksts satur arī informāciju par maksām, kas attiecas uz visu pasūtījumu, nevis tikai atsevišķām rindām. Maksas var automātiski pievienot pasūtījumam, ja šim kreditoram vai kreditoru maksu grupai ir iestatītas automātiskās maksas. Maksas pasūtījuma virsrakstam varat pievienot arī manuāli, darbību rūtī noklikšķinot uz **Uzturēt maksas**.

## <a name="adding-purchase-order-lines"></a>Pirkšanas pasūtījuma rindu pievienošana
Pirkšanas pasūtījumi var būt par fiziskām precēm vai par pakalpojumiem. Krājumu modeļu grupas iestatījums nosaka, vai konkrētais krājuma kods attiecas uz preci vai uz pakalpojumu. Parasti iegādātais krājums tiek norādīts ar krājuma kodu. Taču, ja pasūtījums ir par precēm vai pakalpojumiem, kas tiek patērēti tieši, krājumu varat arī norādīt, izmantojot sagādes kategoriju.  

Pirkšanas pasūtījuma rindās ir daudz lauku, bet daudziem no šiem laukiem ir noklusējuma vērtība vai vērtība, kas ir pārmantota no pasūtījuma virsraksta. Papildu lauki tiek iestatīti, kad atlasāt kādu preci vai pakalpojumu. Lauki, kas visbiežāk tiek iestatīti manuāli, ietver laukus krājuma kodam, daudzumam un pieprasītajam piegādes datumam. Arī informācija par vienības cenu un atlaidēm ir ļoti svarīga, bet vērtības šajos laukos bieži nosaka tirdzniecības līgumi vai pirkšanas līgumi.  

Kad atlasāt kādu preci, varat meklēt visu preces nosaukumu vai tā daļu, nevis izmantojot šī krājuma kodu. Ja precei ir vairāki varianti, piemēram, dažādi lielumi, varat redzēt apskatu par pieejamajiem variantiem, izmantojot funkciju **Pievienot rindas** vai izmantojot uzmeklēšanu, kas ir pieejama laukā **Varianta numurs**.  

Bieži vien jums ir jānorāda vairākas dimensijas krājumam, kas ir atlasīts katrā pirkšanas pasūtījuma rindā. Norādāmas dimensijas ir atkarīgas no dimensiju grupām, kas ir piešķirtas preces šablona definīcijai. Piemēram, bieži vien jums ir jānorāda vieta un noliktava, lai norādītu vietu, uz kuru prece ir jāpiegādā. Preces variantus jūs identificējat, norādot varianta numuru vai ievadot vērtības vienai vai vairākām preces dimensijām, piemēram, krāsai, lielumam, konfigurācijai vai stilam. Dimensiju, piemēram, partijas un sērijas numuru, izsekošana jums ļauj unikāli identificēt katru krājumu laidienu. Kad ir izveidots pasūtījums, varat tvert dimensiju vērtības šajā pasūtījumā, izmantojot darbību **Reģistrācija**. Piemēram, esat pasūtījis piecus gabalus kāda krājuma. Vēlāk jūs reģistrējat, ka trīs no šiem gabaliem būs melni un divi no tiem būs zili. Šo pieeju var izmantot kā alternatīvu dimensiju informācijas tveršanai saņemšanas reģistrēšanas laikā.  

Varat apskatīt detalizētu informāciju par krājumu transakcijas statusu attiecībā uz preču krājumu rezervēm. Piemēram, varat vēlēties pārbaudīt rīcībā esošos krājumus, lai palīdzētu izlemt, cik daudz pasūtīt. Vai varat vēlēties pārskatīt krājumu statusu kādam pasūtītam daudzumam, lai redzētu, vai ir notikusi ienākošā saņemšanas reģistrācija.  

Pirkšanas pasūtījuma rindai, kas tiek lietota, lai preci atgrieztu kreditoram, ir negatīvs daudzums. Atgriešanai varat atlasīt konkrētu laidienu, izmantojot darbību **Rezervācija**.  

Reizēm var būt nepieciešamība sadalīt pasūtīto daudzumu, lai dažādas daļas tiktu piegādātas dažādos datumos. Šādas piegādes var iestatīt, izmantojot darbību **Piegādes grafiks**, kas ir pieejama izvēlnē **Pirkšanas pasūtījuma rinda**, skatā **Rindas**.  

Maksas var automātiski pievienot pirkšanas pasūtījuma rindām, ja šim kreditoram vai kreditoru maksu grupai un krājumam vai krājumu maksu grupai ir iestatītas automātiskās maksas. Taču parasti maksas tiek manuāli pievienotas pasūtījuma rindas līmenī. Lai pievienotu maksu, atveriet lapu **Uzturēt maksas**, izmantojot darbību **Uzturēt maksas** izvēlnē **Finanšu dati**, skatā **Rindas**. Priekšrocība maksu pievienošanai tieši pasūtījuma rindas līmenī ir tāda, ka šo maksu var piešķirt kā krājuma maksu. Lai iestatītu maksu kodus preces maksu uzskaitīšanas nolūkos, izmantojiet debeta opciju **Krājums**. Šāda tipa maksas no pirkšanas pasūtījuma virsraksta ir jāpiešķir rindām, un tikai pēc tam pasūtījumu var apstiprināt. Piemēram, jūs vēlaties piešķirt maksas, pamatojoties uz daudzumu katrā rindā. Maksu kategorija arī ietekmē veidu, kādā maksas tiek iekļautas uzskaitē. Piemēram, fiksētas maksas norāda fiksētu summu, bet procentu maksas tiek aprēķinātas kā procentuāls daudzums no neto summas pasūtījuma rindai. Pirkšanas pasūtījumus var piešķirt kravai, un krava var ietvert paredzamo izdevumu novērtējumu par transportēšanas maksu. Šos izdevumus no kravas varat piešķirt atpakaļ pirkšanas pasūtījuma rindām.

## <a name="purchase-order-actions"></a>Pirkšanas pasūtījuma darbības
Kad pirkšanas pasūtījumam esat pievienojis virsrakstu un rindas, bieži vien ir nepieciešams izpildīt papildu darbības, pirms pasūtījums ir gatavs apstiprināšanai. Tā kā ir pieejams daudz iespēju, var būt noderīgi izmantot funkciju [Darbību meklēšana](../../fin-and-ops/get-started/action-search.md), lai atrastu atbilstošo izvēlnes vienumu.  

Pasūtījumos preces varat konfigurēt tā, lai tām būtu papildu krājumi. Papildu krājumi ir preces, kas ir jāiegādājas kopā vai kuras var iegādāties kopā ar citām precēm. Papildu preces var pievienot bez maksas kā pavadošās preces, kā arī jums var būt iespēja izlemt, vai kādu preci pievienot pasūtījumam vai ne. Papildu krājumus varat pārskatīt pēc katras pievienotās pasūtījuma rindas. Taču droši vien jums būs ērtāk atbilstošos papildu krājumus pārskatīt un pievienot visām pasūtījuma rindām, izmantojot lapu **Papildu krājumi**, kuru varat atvērt no darbību rūts.  

Atlaides parasti tiek pievienotas rindām to izveidošanas laikā. Taču dažas atlaides attiecas uz visu pasūtījumu.

-   Darbība **Kopējā atlaide** aprēķina kopējo atlaides procentuālo daudzumu, kas tiek lietots pilnajam pasūtījumam. Nejauciet šo atlaidi ar termiņatlaides procentiem. Termiņatlaides tiek lietotas, kad rēķins ir samaksāts, un tās ir atkarīgas no maksājuma nosegšanas līdz noteiktam datumam.
-   Ja ir spēkā daudzrindu atlaide, jums ir jālieto darbība **Daudzrindu atlaide**, lai to aprēķinātu un piešķirtu pasūtījumam. Daudzrindu atlaides ir atlaides, ko var piedāvāt, ja pasūtīto dažādo preču apjoms pārsniedz kopīgu slieksni. Šāda tipa atlaidi izmanto tikai daži uzņēmumi.

Maksas ar tādu maksas kodu, kas izmanto debeta tipu **Krājums**, ir jāpiešķir rindas līmenim, pirms pasūtījumu var apstiprināt. Jums var būt ērtāk šīs maksas piešķirt pasūtījuma virsraksta līmenī, lai varētu norādīt maksas kopējo summu. Taču šādā gadījumā maksa pēc tam ir jāsadala uz leju katrai rindai, pirms pasūtījumu var apstiprināt. Varat izmantot darbību **Sadalīt maksas**, lai summas no virsraksta līmenī piešķirtajām maksām sadalītu līdz pasūtījuma rindām. Maksas var sadalīt atbilstoši katras rindas neto summai, atbilstoši pasūtītajam daudzumam vai vienmērīgi sadalīt visām pasūtījuma rindām. Kad maksas ir piešķirtas rindām, šī maksa tiek noņemta no pasūtījuma virsraksta.  

Pirkšanas pasūtījumus var konfigurēt tā, lai budžeta līdzekļi tiktu piešķirti pasūtījumam, pirms to var apstrādāt. Šādā gadījumā varat izmantot darbību **Budžeta pārbaudīšana**, lai piešķirtu budžetu.  

Iespējams, pirkšanas pasūtījuma izpildi ir nepieciešams aizkavēt. Piemēram, jums var būt nepieciešama papildu informācija par precēm vai pakalpojumiem, vai jums ir nepieciešams saņemt autorizāciju tēriņiem. Pasūtījumu var aizturēt vairākos veidos. Piemēram, varat gaidīt, pirms apstiprināt šo pasūtījumu. Vai, ja tiek izmantota izmaiņu pārvaldības darbplūsma, varat šo pasūtījumu neiesniegt apstiprināšanai. Ja ir nepieciešams bloķēt visus pasūtījumus kādam noteiktam kreditoram, kreditoru šablonā šo kreditoru varat arī atzīmēt apstrādei kā **Aizturēts**. Pastāv arī apstākļi, kas varētu novērst pasūtījuma apstrādāšanu. Piemēram, pārstrādāšana varētu tikt novērsta, ja ir pārsniegts kredīta limits vai ja nav pieejami nepieciešamie budžeta līdzekļi.

<a name="additional-resources"></a>Papildu resursi
--------

[Pirkšanas pasūtījumu apskats](purchase-order-overview.md)

[Pirkšanas pasūtījumu apstiprināšana un ratificēšana](purchase-order-approval-confirmation.md)

[Produktu ieejas plūsma pret pirkšanas pasūtījumiem](product-receipt-against-purchase-orders.md)

[Apskats par kreditoru rēķiniem](../../finance/accounts-payable/vendor-invoices-overview.md)



