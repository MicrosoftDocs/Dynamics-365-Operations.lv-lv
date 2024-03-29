---
title: Kreditoru sadarbība ar debitoriem
description: Šajā rakstā ir aprakstīts, kā var izmantot kreditoru sadarbības, lai strādātu ar PREČU pirkšanas pasūtījumiem un pārraudzītu sūtījumu krājumus.
author: GalynaFedorova
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart, VendVendorProfileCard, PurchVendorPortalAllResponse, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4e5748f2368376ee03f280f1487d1de65250d3a4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859174"
---
# <a name="vendor-collaboration-with-customers"></a>Kreditoru sadarbība ar debitoriem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā var izmantot kreditoru sadarbības, lai strādātu ar debitoriem programmā Microsoft Dynamics 365 Supply Chain Management. Kreditori var izpildīt biznesa procesu virknes no tālāk uzskaitītajām darbvietām.

- **Pirkšanas pasūtījuma akceptēšana** — pārraudzīt un atbildēt uz pirkšanas pasūtījumiem (purchase order — PO).
- **Piegādātāja piedāvājuma izteikšana** — skatīt piedāvājumu pieprasījumus (request for quotation — RFQ) un reaģēt uz tiem, ievadot piedāvājumus.
- **Kreditora informācija** — skatīt un atjaunināt kreditora pamatdatus.
- **Rēķinu izrakstīšana** — strādāt ar rēķiniem. Šajā rakstu nevar izmantot rēķinu izrakstīšanas **darbvietai**. Papildinformāciju par šo darbvietu skatiet šeit: [Kreditoru sadarbības rēķinu izrakstīšanas darbvieta](../../finance/accounts-payable/vendor-portal-invoicing-workspace.md).

Kreditori var pārraudzīt arī informāciju par sūtījumu krājumiem.

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a>Darbs ar pirkšanas pasūtījumiem darbvietā Pirkšanas pasūtījumu akceptēšana

Darbvieta **Pirkšanas pasūtījuma akceptēšana** jums ļauj atbildēt uz pirkšanas pasūtījumiem (PO), kas jums ir nosūtīti pārskatīšanai. Tā jums ļauj skatīt arī informāciju par pirkšanas pasūtījumiem, kas gaida rīcību no debitora, un par pirkšanas pasūtījumiem, kas ir akceptēti, bet joprojām ir atvērti.

Darbvietā **Pirkšanas pasūtījuma akceptēšana** pastāv trīs tālāk aprakstītie saraksti.

- **Pārskatāmie pirkšanas pasūtījumi** — šajā sarakstā ir redzami pirkšanas pasūtījumi, kas ir jums nosūtīti un gaida atbildi no jums. Kad esat atbildējis, šie pirkšanas pasūtījumi pazūd no saraksta. Ja debitors jums nosūta jaunu pirkšanas pasūtījuma versiju, pirms esat atbildējis uz iepriekšējo versiju, tiek rādīta tikai jaunākā versija.
- **Tiek gaidīta debitora darbība** — šajā sarakstā jums tiek rādīti visi pirkšanas pasūtījumi, uz kuriem esat atbildējis, bet kurus debitors vēl nav akceptējis. Ja pieņemat kādu pirkšanas pasūtījumu, varat to uzraudzīt šajā sarakstā, līdz tā statuss mainās uz **Akceptēts**. Ja kādu pirkšanas pasūtījumu noraidījāt vai pieņēmāt to ar izmaiņām, šeit šo pirkšanas pasūtījumu varat uzraudzīt, līdz debitors sūta jaunu versiju.
- **Atvērtie akceptētie pirkšanas pasūtījumi** — šajā sarakstā tiek rādīti visi pirkšanas pasūtījumi jūsu kontam, kuru statuss ir **Akceptēts**. Kad preces vai pakalpojumi ir pilnīgi saņemti pret pirkšanas pasūtījumu, šis pirkšanas pasūtījums pazūd no saraksta.

Lai strādātu ar pirkšanas pasūtījumiem, varat izmantot tālāk norādītās lapas.

- **Pārskatāmie pirkšanas pasūtījumi** — šajā lapā ir tāda pati informācija, kāda tiek radīta darbvietas sarakstā **Pārskatāmie pirkšanas pasūtījumi**. Skatiet aprakstu šajā rakstā agrāk.
- **Pirkšanas pasūtījuma kreditora akceptēšanas vēsture** — šajā lapā ir visi šim kreditoram sūtītie pirkšanas pasūtījumi un visas pirkšanas pasūtījumu versijas. Tajā ir arī visas no kreditora saņemtās atbildes.
- **Atvērtie akceptētie pirkšanas pasūtījumi** — šajā lapā ir tāda pati informācija, kāda tiek radīta darbvietas sarakstā **Atvērtie akceptētie pirkšanas pasūtījumi**. Skatiet aprakstu šajā rakstā agrāk.
- **Visi akceptētie pirkšanas pasūtījumi** — šajā lapā ir visi pirkšanas pasūtījumi, kas tika akceptēti. Šajā lapā parādīto esošo pirkšanas pasūtījumu klāstā tostarp ir arī tādi, kur ir saņemtas preces vai pakalpojumi. Šo sarakstu varat izmantot, lai uzraudzītu pirkšanas pasūtījumus, par kuriem varat sūtīt rēķinus.

### <a name="responding-to-pos"></a>Atbildēšana uz pirkšanas pasūtījumiem

Pirkšanas pasūtījumi, ko debitors jums nosūta izskatīšanai, ir redzami darbvietā **Pirkšanas pasūtījuma akceptēšana** un lapā **Pārskatāmie pirkšanas pasūtījumi**. Pēc pirkšanas pasūtījuma atvēršanas varat to pieņemt, to noraidīt vai pieņemt ar izmaiņām. Pirkšanas pasūtījuma virsrakstā vai atsevišķās rindās var būt pielikumi. Turklāt varat pievienot informāciju savai atbildei attiecīgā pirkšanas pasūtījuma virsrakstā vai atsevišķās rindās. Piemēram, varat ierosināt aizstāšanas krājumu kādai no rindām.

Pirkšanas pasūtījumu varat priekšskatīt un izdrukāt kā PDF failu, izmantojot opciju **Priekšskatīt/Drukāt**. Varat arī izmantot darbību **Parādīt dimensijas**, lai slēptu vai rādītu šādu dimensiju kolonnas: **Vieta**, **Noliktava**, **Krāsa**, **Lielums**, **Stils** un **Konfigurācija**. 

Ja lietojat opciju **Pieņemt ar izmaiņām**, varat pieņemt vai noraidīt atsevišķas rindas. Rindās varat veikt tālāk norādītās izmaiņas.

- Mainīt datumus vai daudzumus. Lai atjauninātu akceptēto piegādes datumu visās rindās, izmantojiet opciju **Atjaunināt piegādes datumu** pirkšanas pasūtījuma virsrakstā.
- Sadalīt rindas dažādiem piegādes datumiem vai daudzumiem.
- Aizstāt kādu krājumu. Ievadiet krājuma aprakstu un krājuma numuru sadaļas **Detalizēta rindas informācija** laukā **Ārējais**.

Jūs nevarat mainīt izcenojuma informāciju vai maksas, bet varat izmantot piezīmes, lai ierosinātu šādas izmaiņas.

Ja debitors jums nosūta jaunu pirkšanas pasūtījuma versiju, tai būs versijas sufikss, tādējādi norādot, ka tā ir iepriekš nosūtīta pirkšanas pasūtījuma mainīta versija. Lapā **Pirkšanas pasūtījuma kreditora akceptēšanas vēsture** varat izsekot katra pasūtījuma vēsturi.

## <a name="monitoring-consignment-inventory"></a>Sūtījuma krājumu uzraudzīšana

Ja izmantojat sūtījuma krājumus, varat izmantot kreditoru sadarbības interfeisu, lai skatītu informāciju tālāk norādītajās lapās.

- **Pirkšanas pasūtījumi, kuros tiek patērēti sūtījuma krājumi** — pirkšanas pasūtījumi par sūtījuma krājumiem tiek ģenerēti, kad debitors pārņem krājumu īpašumtiesības. Šie sūtījuma pirkšanas pasūtījumi tiek rādīti tikai šajā lapā. Tie nav ietverti lapā **Visi akceptētie pirkšanas pasūtījumi**.
- **No sūtījuma krājumiem saņemtās preces** — šajā lapā ir uzskaitītas visas transakcijas, kur preces īpašumtiesības tiek nodotas uzņēmumam, kurš šo krājumu patērē. Varat izmantot šo informāciju, lai debitoram izrakstītu rēķinu.
- **Rīcībā esošie sūtījuma krājumi** — šajā lapā tiek rādīti rīcībā esošie sūtījuma krājumi, kas pieder jūsu uzņēmumam, bet kas ir rīcībā esoši debitora noliktavā.

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a>Darbs ar piedāvājumu pieprasījumiem darbvietā Piegādātāja piedāvājuma izteikšana

Darbvietā **Piegādātāja piedāvājuma izteikšana** jums ļauj apskatīt piedāvājumu pieprasījumus (RFQ), uz kuriem jūsu uzņēmums tika aicināts atbildēt. Uz šiem piedāvājumu pieprasījumiem varat arī atbildēt.

Darbvietā tiek rādīti arī visi piedāvājumu pieprasījumi, kurus esat zaudējis vai ieguvis. Turklāt, ja sistēma ir konfigurēta publiskajam sektoram, darbvietā tiek rādīti publiski pieejamie piedāvājumu pieprasījumi.

### <a name="viewing-rfqs"></a>Piedāvājumu pieprasījumu skatīšana

Atveriet darbvietu **Piegādātāja piedāvājuma izteikšana**, lai piekļūtu tālāk norādītajai informācijai.

- Atlasiet **Jauni aicinājumi izteikt piedāvājumus**, lai redzētu piedāvājumu pieprasījumus, uz kuriem jūsu uzņēmums tika aicināts atbildēt. No šejienes varat apskatīt piedāvājuma pieprasījumu un sākt piedāvājuma izteikšanas procesu. Varat arī redzēt grozītos piedāvājumu pieprasījumus, par kuriem ir jāiesniedz jauns piedāvājums.
- Atlasiet **Atgrieztie piedāvājumi**, lai redzētu piedāvājumu pieprasījumus, kurus debitors jums ir atgriezis, lai jūs varētu norādīt papildinformāciju vai atjaunināt savu piedāvājumu.
- Atlasiet **Notiekošie piedāvājumi**, lai redzētu piedāvājumu pieprasījumus, ar kuriem strādājāt jūs vai kāda kontaktpersona, kas pārstāv jūsu uzņēmumu, bet kuri vēl nav iesniegti.
- Atlasiet **Piešķirtie piedāvājumi**, lai redzētu, kad debitors ir piešķīris vismaz vienu rindas vienumu jūsu piedāvājumā.
- Atlasiet **Zaudētie piedāvājumi**, lai redzētu piedāvājumus, kur ir noraidītas visas rindas.
- Atlasiet saiti **Piedāvājumu pieprasījumi**, lai redzētu sarakstu ar visiem piegādātāju piedāvājumu pieprasījumu uzaicinājumiem un visiem iesniegtajiem piedāvājumiem. Lapā **Piedāvājumu pieprasījumi** ir uzskaitīti visi piedāvājumu pieprasījumi, kuros ir iesaistīts kāds piegādātājs. Varat meklēt pēc statusa.
- Atlasiet saiti **Noraidītie piedāvājumi**, lai skatītu sarakstu ar visiem piedāvājumu pieprasījumiem, kur piegādātāja kontaktpersona piedāvājumu ir noraidījusi.

### <a name="working-with-rfqs-that-are-publicly-available"></a>Darbs ar publiski pieejamiem piedāvājumu pieprasījumiem

Cilvēki, kas strādā publiskā sektorā, var redzēt atvērtus un novecojušus PP, kas padarīti pieejami publiskam.

- Atlasiet saiti **Atvērt publicētos piedāvājumu pieprasījumus**, lai redzētu sarakstu ar atvērtajiem piedāvājumu pieprasījumiem, kas ir publiski pieejami. Atvērts piedāvājuma pieprasījums ir piedāvājuma pieprasījums, kas vēl nav beidzies. Piedāvājuma pieprasījuma beigu datums un laiks ir atrodami piedāvājuma pieprasījuma virsrakstā.

    Ja esat uzaicināts izteikt piedāvājumu, to pašu piedāvājuma pieprasījumu varat atrast lapā **Jauni aicinājumi izteikt piedāvājumus**. Reizēm, iespējams, vēlaties izteikt piedāvājumu par kādu atvērtu piedāvājuma pieprasījumu, bet neesat uzaicināts izteikt piedāvājumus par to. Tādā gadījumā, iespējams, varat uzaicināt pats sevi, ja vien debitors šī piedāvājuma pieprasījuma gadījumā ir aktivizējis pašuzaicināšanu. 

    Jaunā **piedāvājuma uzaicinājumu lapa var nodrošināt filtru, kas ļauj skatīt atvērtos PP un identificēt tos**, kas satur rindas, kas atbilst jūsu apstiprinātajām sagādes kategorijām. Lai padarītu šo filtru pieejamu, *sistēmā ir jāieslēdz iespēja Ļaut kreditoriem* meklēt PP pēc sagādes kategorijas funkcionalitātes. Administratori var izmantot līdzekļu **pārvaldības darbvietu**, lai pārbaudītu šī līdzekļa statusu un ieslēgtu to, ja nepieciešams. Tur šis līdzeklis ir uzskaitīts šādā veidā:

    - **Modulis:** *parādi kreditoriem*
    - **Funkcionalitātes nosaukums:** *ļauj kreditoriem meklēt PP pēc sagādes kategorijas* <!-- KFM: I don't see this here, is this right? -->

    Ir iespējams uzlabot saites Atvērt **publicētos piedāvājumu pieprasījumus pieejamību, ieslēdzot saiti "Atvērt publicētus piedāvājuma pieprasījumus** *" kā elementa* elementu. Šī funkcija pārvērš saiti par elementu un pārvieto to uz izcilu atrašanās vietu, lai to būtu viegli atrast. Administratori var izmantot līdzekļu **pārvaldības darbvietu**, lai pārbaudītu šī līdzekļa statusu un ieslēgtu to, ja nepieciešams. (No Piegādes ķēdes pārvaldības versijas 10.0.21, funkcija ir ieslēgta pēc noklusējuma.) Tur šis līdzeklis ir uzskaitīts šādā veidā:

    - **Modulis:** *Sagāde un ieguve*
    - **Līdzekļa nosaukums:** *rādīt saiti "Atvērt publicētus piedāvājuma pieprasījumus" kā elementu*

- Atlasiet saiti **Slēgtie publicētie piedāvājumu pieprasījumi**, lai redzētu sarakstu ar slēgtajiem piedāvājumu pieprasījumiem, kas ir publiski pieejami. Slēgts piedāvājuma pieprasījums ir piedāvājuma pieprasījums, kas ir beidzies. Piedāvājuma pieprasījuma beigu datums un laiks ir atrodami piedāvājuma pieprasījuma virsrakstā.

    Slēgtā piedāvājuma pieprasījumā tiek rādīti visi piegādātāju piedāvājumi līdz pat rindu līmenim. Kad piedāvājumi tiek piešķirti vai noraidīti, šī informācija tiek atspoguļota slēgtajā piedāvājuma pieprasījumā. Tāpat ir pieejami arī visi piedāvājumā ietvertie pielikumi.

> [!NOTE]
> Šī funkcionalitāte ir pieejama tikai tad, ja ir ieslēgta publiskā sektora konfigurācija.

### <a name="bidding"></a>Piedāvājumu izteikšana

- Atlasiet **Piedāvājums**, lai sāktu izteikt piedāvājumu par kādu piedāvājuma pieprasījumu.

    Kad piedāvājuma laukiem ir iespējota rediģēšana kāda piedāvājuma pieprasījuma virsrakstos un rindās, savu piedāvājumu varat ievadīt tieši rindiņu režģī. Tāpat jums ir jāņem vērā visa piedāvājuma papildinformācija, kas ir jāpievieno rindas detalizētajai informācijai.

    Kad sākat strādāt ar kādu piedāvājumu, tas tiek rādīts sadaļā **Notiekošie piedāvājumi**.

    Piedāvājumu varat saglabāt jebkurā laikā pirms beigu datuma. Pēc tam varat atgriezties, lai šo piedāvājumu vēlāk pabeigtu un iesniegtu. Pēc piedāvājuma iesniegšanas līdz pat beigu datumam varat šo piedāvājumu atsaukt un atjaunināt.

- Atlasiet **Atiestatīt no piedāvājuma pieprasījuma**, lai atiestatītu kādam piedāvājumam ievadītos datus un atgrieztos pie sākotnējā piedāvājuma pieprasījuma. Varat atiestatīt virsrakstu vai rindu.
- Rindu režģī atlasiet **Pievienot alternatīvu** vai **Noņemt alternatīvu**, lai strādātu ar alternatīvām.

    Dažos piedāvājumu pieprasījumos ir atļauti alternatīvi piedāvājumi. Alternatīvus piedāvājumus varat norādīt tikai rindām ar veidu **Kategorija**, jo konkrētus krājumus nevar pievienot kā alternatīvas. 

- Atlasiet **Piedāvājuma pieprasījuma pielikums** vai **Piedāvājuma pieprasījuma rindas pielikums**, lai atvērtu jebkādu pielikumu, ko debitors ir pievienojis kādam piedāvājuma pieprasījumam. Atlasiet **Piedāvājumu pielikumi** vai **Piedāvājumu rindu pielikumi**, lai kopā ar piedāvājumu augšupielādētu pielikumus.

    Lai varētu iesniegt kādu piedāvājumu, iespējams, jums vispirms ir jāaizpilda anketas.

- Atlasiet **Noraidīt**, ja nevēlaties izteikt piedāvājumu. Kad ir atlasīts **Noraidīt**, šo darbību nevarat atsaukt un nevarat ievadīt nekādu piedāvājumu.

Ja piedāvājuma pieprasījums ir grozīts, jums ir jāievada jauns piedāvājums. Informācija par grozījumu ir atrodama piedāvājuma pieprasījuma lapas cilnē **Grozījumi**. Grozītie piedāvājumu pieprasījumi ir redzami lapā **Jauni aicinājumi izteikt piedāvājumus**.

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a>Piekļūšana kreditora pamatdatiem darbvietā Kreditora informācija

Jūs kā kreditors varat piekļūt daļai no informācijas, ko debitors uztur kreditora šablona ierakstā. Tādēļ jūs varat nodrošināt šīs informācijas atbilstību jaunākajām izmaiņām. Lai atjauninātu informāciju, jums ir nepieciešama kreditora administratora (ārējā) loma.

Ir pieejama šāda informācija: kreditora nosaukums, adreses, kontaktinformācija, kontaktpersonas un viņu kontaktinformācija, identifikācijas numuri, nodokļu maksātāju reģistrācijas numuri, sagādes kategorijas, kādās ir apstiprināta kreditora pārdošana debitoram, un informācija par sertifikācijām.

## <a name="additional-resources"></a>Papildu resursi

[Pārvaldīt kreditoru sadarbības lietotājus](manage-vendor-collaboration-users.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
