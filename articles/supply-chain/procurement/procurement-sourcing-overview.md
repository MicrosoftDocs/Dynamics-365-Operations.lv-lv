---
title: Sagādes un avotu apskats
description: Šajā rakstā ir sniegts pārskats par funkcionalitāti, kas ir pieejama Sagādes un plānošanas modulī.
author: Henrikan
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogListPage, CatVendorCatalogListPage, PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "58021"
- intro-internal
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d1e127fe96b29520022f18a5b02369d3593c46b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569533"
---
# <a name="procurement-and-sourcing-overview"></a>Sagādes un avotu apskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par funkcionalitāti, kas ir pieejama Sagādes un plānošanas modulī.

Sagāde un avoti aptver visas darbības no preces un pakalpojumus nepieciešamības noteikšanas līdz preces sagādei, saņemšanai, rēķinu izrakstīšanai un maksājuma apstrādei ar kreditoriem. Sagādes procesu var konfigurēt atbilstoši noteiktām biznesa vajadzībām, definējot iepirkuma politikas un darbplūsmas.

## <a name="identifying-a-need-for-product-and-services"></a>Preces un pakalpojumus nepieciešamības noteikšana

*Pieprasījumi* var rādīt nepieciešamību pēc precēm vai pakalpojumiem, piemēram, ja darbiniekam ir nepieciešama kāda prece. *Preču katalogus* var iestatīt, lai organizētu pieejamo preču atlasi vai katalogā vēl nepieejamo preču pieprasījumu veikšanu, kas ļauj pirkšanas struktūrvienībai apsvērt, kā preces var piegādāt.  

*Tēriņu limitus* var izmantot, lai ierobežotu pieprasījuma izdevumus, un *pirkšanas darbplūsma* pievieno iespēju prasīt apstiprinājumu pirms pasūtīšanas. Ir iespējams arī norādīt budžeta līdzekļu sadalījumu, ja tas ir nepieciešams.  

Sagādes nodaļa identificē nepieciešamo preču un pakalpojumu piegādātājus un tas var iekļaut *piedāvājuma pieprasījumu* nosūtīšanu vairākiem iespējamiem piegādātājiem. Ir iespējams koplietot pieprasītās preces specifikācijas un potenciālie kreditori var tos skatīt, lai redzētu, vai viņi var piegādāt preces, kas tām atbilst. Kreditori atgriež savus piedāvājumus, kurus pēc tam pārskata sagādes nodaļa pirms tā atlasa piegādātāju, no kura vēlas iegādāties preces.  

Pirkšanas pasūtījums iekļauj opciju izsūtīt *pirkšanas pieprasījumu* kreditoram kā alternatīvu plašākam piedāvājuma pieprasījuma procesam. Pirkšanas pieprasījumu var izmantot, lai palīdzētu izveidot noteikumus, piemēram, cenas, atlaides un pasūtījuma piegādes datumu. Ja kreditori ir iestatīti portāla **Kreditors** lietošanai, tad pirkšanas pieprasījuma funkcionalitāte ir atspējota. Tā vietā pasūtījums ir koplietots **Kreditoru** portālā, un, kad tiek nosūtīts *apstiprinājuma pieprasījums*, kreditors var tieši apstiprināt šo pasūtījumu.  

*Piegādātāju katalogus* var izmantot, lai apkopotu informāciju par preču klāstu, ko var piegādāt kreditori. Kreditori var publicēt savu katalogu, lai katalogu būtu vieglāk atjaunināt. Ir iespējams pievienot *apstiprināto kreditoru sarakstu* precei, un tas var palīdzēt organizēt kreditora izvēli, kad tiek atvērti jauni pirkšanas pasūtījumi, un novērst neparedzētu kreditoru izmantošanu.

## <a name="procurement"></a>Sagāde

*Pirkšanas pasūtījumus* var izveidot daudzos dažādos veidos, ieskaitot:

- Galvenās plānošanas rezultātā, ja ir noteikts pieprasījums, kam ir nepieciešama pirkšana. Šī procesa ietvaros tiek ģenerēti plānotie pirkšanas pasūtījumi, un to izlaišanas laikā tiek ģenerēti pirkšanas pasūtījumi.
- Izmantojot pirkšanas pieprasījumu apstrādi, kas beidzas ar sagādi.
- Izmantojot pirkšanas līgumu apstrādi, kur pirkšanas pasūtījumi tiek izveidoti kā izpildei nodotie pasūtījumi no līgumiem. Parasti to izmanto, kad pirkšanas līgumi tiek izmantoti, lai attēlotu virspasūtījumus.
- Manuāli, kad izveidojamais pirkšanas pasūtījums nav balstīts uz citu dokumentu.

Pirkšanas pasūtījumi, kas ir konfigurēti ar *pirkšanas apstiprinājuma darbplūsmām*, pieprasa apstiprinājumu pirms tie tiek reģistrēti kā apstiprināti, un tas ir nepieciešams pirms pasūtījuma tālākas apstrādes.

Pirkšanas pasūtījumi tiek *apstiprināti*, lai norādītu, ka ar kreditoru ir izveidots līgums. Pēc tam pirkšanas pasūtījums pakāpeniski izies cauri dažādiem stāvokļiem līdz galu galā tiks izrakstīts rēķins vai tas tiks atcelts.  

Kad veidojat pirkšanas pasūtījumu, daudzi lauki ir iepriekš aizpildīti ar vērtībām, kas pēc noklusējuma tiek ņemtas no lapā **Kreditori** glabātās informācijas par kreditoru. Tas nozīmē, ka ir ierobežots lauku skaits, ko nepieciešams aizpildīt pirkšanas pasūtījumā, lai gan var izvēlēties ignorēt noklusējuma vērtības.

### <a name="prices-and-discounts"></a>Cenas un atlaides

Cenas un atlaides ietver informāciju par cenām, atlaidēm un piedāvātajiem atlaides nosacījumiem. Cenas un atlaides var tikt attēlotas kā *tirdzniecības līgumi*. Tirdzniecības līgumi ir kreditoru cenrāži ar cenām vai atlaidēm, kā arī tiem ir norādīti specifiski līguma derīguma datumi. Cenas un atlaides var apspriest un parādīt, izmantojot *pirkšanas līgumus* ar nosacījumiem, piemēram, apņemšanos pirkt noteiktus apjomus vai iztērēt noteiktas naudas summas kā priekšnoteikumu norunātajiem nosacījumiem. *Atlaižu līgumus* var izveidot ar kreditoriem, kad īpašu preču vai preču grupu sagāde var sniegt atlaides no kreditora atkarībā no pirkuma summas vai apjoma.

### <a name="delivery-options"></a>Piegādes iespējas

Ir dažādas piegādes procesa iespējas, kas ir saistītas ar pirkšanas pasūtījumu. Pasūtītās preces var sadalīt *piegādes* grafikos, kur pasūtīto daudzumu daļas var plānot piegādei dažādos datumos. Piegādes var iekļaut arī *tiešo piegādi*, kas iniciēta no pārdošanas pasūtījuma, kas automatizē pavadzīmes ģenerēšanu pārdošanas pasūtījumā tajā pašā brīdī, kad preču ieejas plūsma tiek reģistrēta pirkšanas pasūtījumā. Pirkšanas pasūtījumus var iekļaut *starpuzņēmumu pasūtījumu* ķēdē, ko sauc arī par starpuzņēmumu pirkšanas pasūtījumiem, kur preces tiek pasūtītas no atbilstoša starpuzņēmumu pārdošanas pasūtījuma. Šādā gadījumā dažas darbības tiek automatizētas divos saistītajos starpuzņēmumu pasūtījumos.

### <a name="supplementary-items"></a>Papildu krājumi

Preces var iestatīt, lai tās iekļautu *papildu krājumus*. Tas ir preču piedāvājums, kas ir saistītas ar preci, kas tiek pasūtīta. Papildu preces var būt vai nebūt obligātas. Dažos gadījumos, papildu krājumus var pievienot kā bezmaksas preces, kas tiek pievienotas citu preču pirkšanas laikā.

### <a name="purchase-order-charges"></a>Pirkšanas pasūtījuma maksas

Pirkšanas pasūtījumam var piešķirt maksas. Tas var notikt automātiski, izmantojot automātisko maksu iestatīšanu vai pievienojot maksas manuāli. Maksas var būt piešķirtas pasūtījumam virsraksta līmenī vai pasūtījuma rindu līmenī. Maksu uzskaiti var iestatīt dažādos veidos. Piemēram, varat iestatīt maksas kā preces izmaksu uzskaiti. Ja to darāt, maksas ir jāpiešķir pasūtījuma rindu līmenī pirms pasūtījuma apstiprināšanas. Pastāv iespēja, kas var palīdzēt piešķirt maksas no pasūtījuma virsraksta rindām.

## <a name="product-receipt-and-invoicing"></a>Preču ieejas plūsma un rēķinu izrakstīšana

Pirkšanas pasūtījumiem, kas ietver fiziskas preces, parasti nepieciešama *saņemšanas reģistrācija*, kas notiek noliktavā, un pēc tam *preču ieejas plūsma* tiek reģistrēta pasūtījumam. Pirkšanas pasūtījumus ar precēm, kas apmierina pieprasījumus, var konfigurēt, lai darbiniekam, kurš ir pieprasījis preces, arī būtu jāsniedz *saņemšanas apstiprinājums*.  

Daži pirkšanas pasūtījumi ietver preces, kas ir pakalpojumi vai citas nefiziskas preces, kuru saņemšana noliktavā nav nepieciešama. Preces var veidot kā pakalpojumus vai *sagādes kategorijas* var izmantot tieši šādu pasūtījumu pirkšanas pasūtījumā. Ar šiem pasūtījumiem, preču ieejas plūsmas uzskaite dažreiz tiek izlaista un pasūtījums ir iekļauts rēķinā tieši vai alternatīvi preču saņemšanas reģistrācija tiek veikta pirkšanas pasūtījumā bez iepriekšējas saņemšanas reģistrācijas.  

Preču saņemšana var beigties ar automātisko patēriņu noteiktiem mērķiem. Tas ietver netiešo patēriņu ar tiešo piegādi, patēriņu projektam vai preces uzskaiti kā pamatlīdzekli.  

Kad *kreditora rēķini* tiek saņemti no kreditora, tos var reģistrēt vispirms *rēķinu reģistrā* neatkarīgi no pirkšanas pasūtījuma, un vēlāk apstiprināt kā ierakstu pret pirkšanas pasūtījumu. Kreditora rēķina ar pirkšanas pasūtījumu reģistrācija iekļauj preču ieejas plūsmas saskaņošanu ar rēķinu.  

*Uzskaites sadales* var norādīt pirkšanas pasūtījumā, lai aprakstītu kā jāveic uzskaite Virsgrāmatā, un var arī definēt, kā budžeta līdzekļu sadalījums tiek iegūts, kad tas ir iekļauts jūsu konfigurācijā.  

Rēķinos iekļautie pirkšanas pasūtījumi tiek reģistrēti kā kreditori kreditora kontā, no kurienes *kreditora maksājumu* var apstrādāt.

## <a name="vendor-performance"></a>Kreditora veiktspēja

Pirkšanas veiktspēja un pārskatīšana tiek atbalstīta, izmantojot *sagādes un kreditoru pārskatus*, kuri ietver tēriņu analīzi un kreditora veiktspējas analīzi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]