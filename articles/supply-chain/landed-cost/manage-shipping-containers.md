---
title: Pārvaldīt nosūtīšanas konteinerus
description: Šajā tēmā ir aprakstīts, kā strādāt ar nosūtīšanas konteineriem. Nosūtīšanas konteineri tiek izmantoti, lai grupētu preces, kas ir fiziski sagrupētas kopā. Tās lieto arī gadījumos, kad izmaksas koplieto tikai šīm precēm, parasti tāpēc, ka tās ir fiziski apvienotas.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9b42292194d40f6b0cc6203130bedc1fbb45eec8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833813"
---
# <a name="manage-shipping-containers"></a>Pārvaldīt nosūtīšanas konteinerus

[!include [banner](../../includes/banner.md)]

Nosūtīšanas konteineri tiek izmantoti, lai grupētu preces, kas ir fiziski sagrupētas kopā. Tās lieto arī gadījumos, kad izmaksas koplieto tikai šīm precēm, parasti tāpēc, ka tās ir fiziski apvienotas.

Lai skatītu un apstrādātu preces, izmantojot pārvadāšanas konteinera lapu, dodieties uz **Kopējās izmaksas \> Nosūtīšanas konteineri \> Visi nosūtīšanas konteineri**. Lapā **Visi nosūtīšanas konteineri** ir parādīts visu pieejamo nosūtīšanas konteineru saraksts. Jūs varat izmantot pogas Darbību rūtī, lai izveidotu, dzēstu un darbotos ar nosūtīšanas konteineriem. Sarakstā atlasiet jebkuru nosūtīšanas konteineri, lai apskatītu tā detaļas lapā **Nosūtīšanas konteineri**.

Nosūtīšanas konteinera detalizētas informācijas lapas augšējā daļā ir norādīts nosūtīšanas konteiners un izmaksu informācija. Sadaļā **Rindas** ir parādīti konteineri, krājumi un pirkšanas pasūtījumi vai pārsūtīšanas pasūtījumi, kas ir pievienoti konteineram.

## <a name="action-pane"></a>Darbības rūts

Darbību rūts lapās **Visi pārvadāšanas konteineri** un **Pārvadāšanas konteineri** nodrošina pogas, kas ļauj strādāt ar atlasīto nosūtīšanas konteineru. Katra poga veic vienu darbību. Darbību rūtī ir ietvertas arī cilnes, katra no tām savukārt sniedz saistītu pogu kopu. Izņemot, ja atzīmēts, visas pogas un cilnes, kas ir aprakstītas tālākminošajos apakšsadaļās, ir pieejamas gan saraksta skatījumā (t.i., lapā **Visi nosūtīšanas konteineri**), gan detalizētajā skatā (t.i., lapā **Nosūtīšanas konteineri**).

### <a name="buttons-on-the-manage-tab"></a>Pogas cilnē Pārvaldīt

Šajā tabulā ir aprakstītas pogas, kas ir pieejamas darbību rūts cilnē **Pārvaldīt**.

| Poga | Apraksti |
|---|---|
| Grāmatot saņemšanas sarakstu | Grāmatojiet saņemšanas sarakstu vai skatiet produktu ieejas plūsmu sarakstus visām pirkšanas pasūtījuma rindām nosūtīšanas konteinerā. Ja tiek izmantotas vairāku uzņēmumu kravas, katram uzņēmumam tiek atvērts jauns saņemšanas saraksta grāmatošanas dialoglodziņš. |
| Grāmatot produktu ieejas plūsmu | Grāmatojiet saņemto preču pavadzīmi visām pirkšanas pasūtījuma rindām nosūtīšanas konteinerā. |
| Grāmatot rēķinu | Grāmatojiet rēķinu visām pirkšanas pasūtījuma rindām nosūtīšanas konteinerā. Ja tiek izmantotas vairāku uzņēmumu kravas, katram uzņēmumam tiek atvērts jauns rēķina grāmatošanas dialoglodziņš. |
| Nosūtīšanas pārsūtīšanas pasūtījums | Grāmatojiet pārsūtīšanas pasūtījuma sūtījumu visām pirkšanas pasūtījuma rindām nosūtīšanas konteinerā. Dialoglodziņā tiek parādītas tikai tās sūtījuma konteinera rindas, kas ir pārsūtīšanas pasūtījuma tips. |
| Saņemt pārsūtīšanas pasūtījumu | Grāmatojiet pārsūtīšanas pasūtījuma pavadzīmi visām pirkšanas pasūtījuma rindām nosūtīšanas konteinerā. Saņemšanas dialoglodziņš ir vienkāršākais veids, kā saņemt preces nosūtīšanas konteinerā vai reisā, un ir viena no trim pieejamām opcijām. Varat arī saņemt saņemšanas žurnālos vai mobilās ierīces apstrādē. |
| Izveidot saņemšanas žurnālu | Jūs varat izveidot organizāciju saņemšanas žurnālu, izmantojot papildu noliktavas funkcijas. Opcijas ir _Inicializēt daudzumu (ieteicams)_, vai _Izveidot no tranzīta precēm_, vai _Izveidot no pirkšanas pasūtījumiem_. Pēdējās divas opcijas ir atkarīgas no tā, vai tiek lietota tranzīta preču apstrāde. |
| Pārdēvēt | Atveriet dialoglodziņu, kur varat pārdēvēt atlasīto nosūtīšanas konteineru. |
| Mainīt maršruta veidni | Reisa veidnes maiņa. Pēc ceļojuma veidnes maiņas, iespējams, būs atkal jāizvēlas **Atrast automātiskās izmaksas** vai manuāli pievienot izmaksas, jo sūtījuma izmaksas tiks dzēstas. |
| Pārvērst par nomas līgumu | Konvertējiet atlasīto nosūtīšanas konteineru par nomas pārvadāšanas konteineru. |

### <a name="buttons-on-the-general-tab"></a>Pogas cilnē Vispārīgi

Šajā tabulā ir aprakstītas pogas, kas ir pieejamas darbību rūts cilnē **Vispārīgi**.

| Poga | Apraksti |
|---|---|
| Saņemšanas saraksts | Grāmatojiet saņemšanas sarakstu visām pirkšanas pasūtījuma rindām nosūtīšanas konteinerā. Ja tiek izmantotas vairāku uzņēmumu kravas, katram uzņēmumam tiek atvērts jauns saņemšanas saraksta grāmatošanas dialoglodziņš. |
| Produkta saņemšana | Skatiet produktu ieejas plūsmas ierakstu, ja tas tiek izmantots. Produktu ieejas plūsmas process tiks izmantots tikai tad, ja preces neizmanto tranzīta funkcionalitāti. |
| Krājumu saņemšana | Skatiet sūtījuma konteinera krājumu saņemšanas žurnālu, ja šis žurnāls tiek izmantots. |
| Fāzes | Fāzes tiek izmantotas, lai identificētu atsevišķas ceļojuma daļas. Izpildes laikus var saistīt ar katru fāzi, lai palīdzētu izsekot kravu. Papildinformāciju skatiet [Vairākfāžu reisa iestatījumi](multi-leg-journey-setup.md). |
| Izsekošana | Skatīt vai atjaunināt kravas izsekošanu. |
| Tranzītpreču pasūtījumi | Lapu **Tranzīta preces** var atvērt tieši no konteinera. Šajā lapā redzami tikai atlasītā nosūtīšanas konteinera tranzīta preču ieraksti. |

## <a name="header-view"></a>Virsraksta skatījums

Lai atvērtu **Galvenes** skatu, atveriet nosūtīšanas konteineri un pēc tam atlasiet cilni **Galvene** nosūtīšanas konteinera galvenes augšējā labajā stūrī.

### <a name="settings-on-the-general-fasttab"></a>Kopsavilkuma cilnes Vispārīgi iestatījumi

Šajā tabulā ir aprakstīti lauki, kas ir pieejami nosūtīšanas konteinera **Galvenes** skata kopsavilkuma cilnē **Vispārīgi**.

| Lauks | Apraksts |
|---|---|
| Nosūtīšanas konteiners | Nosūtīšanas konteinera nosaukums. |
| Reiss | Reiss, kas saistīts ar nosūtīšanas konteineru. |
| Nosūtīšanas konteinera veids | Ievadiet pārvadāšanas konteinera veidu. Šim laukam ir jābūt iestatītam. To var izmantot, lai noteiktu kravas pārvadāšanas izmaksas, piemēram, atlasot automātiskās izmaksas, kas saistītas ar pārvadāšanas konteinera tipu. |
| Kuģis | Ievadiet vai atlasiet kuģi. Ja kuģis nav uzskaitīts kā vērtība, kuģa ID varat ievadīt kā brīvu tekstu. Tādā gadījumā galvenā tabula netiek atjaunināta tā, lai vēlāk šajā laukā varētu atlasīt kuģa ID. Papildinformāciju skatiet [Kuģi](shipping-information-setup.md#vessels). |
| Vienības veids | Vienību tipi tiek izmantoti kā papildu nosūtīšanas konteineru grupēšanas un identifikācijas līdzekļi. Tie tiek rādīti un atlasīti pārvadāšanas konteinera lapā. Papildinformācijai skatiet [Iestatīt mērvienību veidus](shipping-container-setup.md#unit-types). |
| Dzesēšanas veids | Refrižeratoru tipi tiek izmantoti kā papildu nosūtīšanas konteineru grupēšanas un identifikācijas līdzekļi, parasti tie ir refrižeratora konteineri. Tie tiek rādīti un atlasīti pārvadāšanas konteinera lapā. Papildinformācijai skatiet [Iestatīt refrižeratoru veidus](shipping-container-setup.md#refrigeration-types). |
| Mērījums | Šis lauks aktivizē mērījumu norādīšanu modulī **Kopējās izmaksas**. Bieži vien mērījumus izmanto organizācijas, kas nezina preču individuālo tilpumu vai svaru, bet pieprasa daudz precīzāku sadali nekā to sniedz daudzums vai skaits. Kravas ekspediators vai aģents nodrošina organizāciju ar svara kilogramos vai kubikmetru krājumu līmenī vai pirkšanas pasūtījuma līmenī. Ja parametrs ir atlasīts, to var atjaunināt automātiski vai ievadīt manuāli. |
| Mērvienība | Mērvienība, kas attiecas uz skaitli laukā **Mērījums**. |
| Faktiskais svars | Varat reģistrēt kartona kārbas vai konteinera faktisko svaru. Šo vērtību var izmantot, lai pārbaudītu maksimālo svaru, kas ir atļauts nosūtīšanas konteinera iestatījumos. |
| Kastu skaits | Ja ir atlasīts parametrs, kartona kārbu skaits tiek automātiski atjaunināts. |
| Preču apraksts | Preču aprakstu var atlasīt pārvadāšanas konteinerā vai folio galvenē. To izmanto, lai palīdzētu identificēt reisu, nosūtīšanas konteineru vai preču folio. Papildinformāciju skatiet sadaļā [Preču apraksts](shipping-information-setup.md#description-of-goods). |
| Sākotnējā gaisa kravas pavadzīme/preču transporta pavadzīme | Kravas konteineram var norādīt mājas gaisa ceļa laiku vai preču transporta pavadzīmi. |
| Atzīmes | Ievadiet papildu informāciju, kas saistīta ar nosūtīšanas konteineru. |
| Atgriežams | Vērtība, kas norāda, vai nosūtīšanas konteineru var atgriezt pēc reisa. |
| Reisa statuss | Reisa statuss, kas ir saistīts ar nosūtīšanas konteineri. |
| Pirkšanas pasūtījuma statuss | Pirkšanas pasūtījuma statuss, kas ir saistīts ar nosūtīšanas konteineri. |

### <a name="settings-on-the-delivery-fasttab"></a>Kopsavilkuma cilnes Dimensijas iestatījumi

Šajā tabulā ir aprakstīti lauki, kas ir pieejami nosūtīšanas konteinera **Galvenes** skata kopsavilkuma cilnē **Piegāde**.

| Lauks | Apraksts |
|---|---|
| Izveidošanas datums un laiks | Datums un laiks, kad tika izveidots konteiners. |
| Produkta izvešanas no rūpnīcas datums | Šis datums parasti tiek nodrošināts fabrikai/kreditoram, lai norādītu, kad paredzams, ka preces atstāj savas telpas. Kad strādājat ar fabriku Āzijā, šis datums bieži ir nepieciešams, nevis datums, kad gaidīt preces. (Pretēji, vietējās piegādes gadījumā ir pieprasīts datums, kad preces tiek gaidītas.) Šo lauku var aizpildīt no pirkšanas pasūtījuma rindām nosūtīšanas konteineru sarakstā. To var arī manuāli ievadīt šeit. |
| Nosūtīšanas datums | Šo datumu var drukāt pirkšanas pasūtījuma dokumentā. Parasti tas informē rūpnīcu/kreditoru par datumu, kad preces jāpiegādā ostā. Šis lauks ir paredzēts tikai informatīviem nolūkiem. Tas netiek izmantots, lai prognozēto preču piegādes datumu novērtētu nosūtīšanas konteinerā. Šo lauku var iestatīt, ka tas tiek automātiski atjaunināts, atjauninot izsekošanas kontroles lapu. |
| Nonākšanas veikalā datums | Agrākais datums, kad pārdošanai būs pieejamas preces no pirkšanas pasūtījumiem, kas ir saistīti ar reisu.|
| Aprēķinātais piegādes datums | Parasti datums, kad precēm jāienāk noliktavā. Šis lauks ir paredzēts tikai informatīviem nolūkiem. Tas netiek izmantots, lai aprēķinātu vispārējo plānošanu nosūtīšanas konteinera pirkšanas pasūtījuma rindās. Paredzamais piegādes datums pirkšanas pasūtījuma rindās tiek atjaunināts, izmantojot izsekošanas kontroli. Šo lauku var iestatīt, ka tas tiek automātiski atjaunināts, atjauninot izsekošanas kontroles lapu. |
| Izbraukšanas datums | Parasti datums, kad lidmašīnu vai kuģis faktiski atstāj aizjūras ostu. |
| ETA nosūtīšanas ostā | Plānotais saņemšanas datums galamērķa ostā ("uz" ostu). |
| Oriģinālais dokuments saņemts | Pēc izvēles: Atjaunināt sākotnējo dokumentu saņemšanas datumu. |
| Brokeris ieteica | Pēc izvēles: Atjaunināt muitas starpnieka ieteikšanas datumu. |
| Sākotnējā preču transporta pavadzīme nosūtīta | Pēc izvēles: Atjaunināt datumu, kad tika nosūtīta sākotnējā preču transporta pavadzīme. |
| Preces izpildītas | Pēc izvēles: Atjaunināt preču izlaides datumu. |
| Norunātā tikšanās ar klientu | Pēc izvēles: Atjaunināt debitora tikšanās datumu. |
| Sūtījums piegādāts noliktavā | Pēc izvēles: Atjaunināt datumu, kad preces tika piegādātas noliktavā. |
| Pārbaudes datums | Pēc izvēles: Atjaunināt pārbaudes datumu. |
| Piegādes instrukcijas | Pēc izvēles: Atjaunināt piegādes instrukciju datumu. |
| No ostas | Osta, no kuras tiks nosūtīti krājumi. |
| Uz ostu | Osta, no kuras tiks nosūtīti krājumi. |
| Vietējais ekspeditors | Šis lauks ir paredzēts tikai informatīviem nolūkiem. Lokālajam ekspeditoram jābūt atlasāmam no kreditoru tabulas. |
| Vietējā transporta datums | Ievadiet datumu, kurā ir rezervēts vietējais transports. Šis lauks var palīdzēt noliktavai veikt tās plānošanu. |
| Vietējā transporta laiks | Ievadiet laiku posmu. Šis lauks var palīdzēt noliktavai veikt tās plānošanu. |
| Maršruta veidne | Ceļojuma veidne, kas ir norādīta reisam. Ceļojuma veidne sniedz detalizētu informāciju par ostām "uz" un "no", kā arī izpildes laikus, kas ir saistīti ar nosūtīšanas konteinera izsekošanas kontroli. |

### <a name="settings-on-the-other-fasttab"></a>Kopsavilkuma cilnes Citi iestatījumi

Šajā tabulā ir aprakstīti lauki, kas ir pieejami nosūtīšanas konteinera **Galvenes** skata kopsavilkuma cilnē **Citi**.

| Lauks | Apraksts |
|---|---|
| Noma | Vērtība, kas norāda, vai nosūtīšanas konteiners ir nomas nosūtīšanas konteiners. Nomas izmaksas var būt saistītas ar nomas konteineriem. |
| Pārvērsts par nomas līgumu | Vērtība, kas norāda, vai nosūtīšanas konteiners tika pārvērsts par nomas nosūtīšanas konteineri. Nomas izmaksas var būt saistītas ar nomas konteineriem. |
| Oriģinālais reiss | Ja nosūtīšanas konteiners tika pārvietots uz jaunu reisu, sākotnējais reiss. |
| Izmantots | Izmantojiet šo, lai ierakstītu, vai tika izmantots nomas nosūtīšanas konteiners. Tā ir paredzēta tikai informatīviem nolūkiem. |
| Paredzamais iekraušanas datums | Plānotais nosūtīšanas konteinera iekraušanas ar precēm datums. |
| Mūsu sērijas numurs | Ievadiet sērijas numuru, ko jūsu uzņēmums nosūtīšanas konteineram izmanto iekšēji. |
| Nosūtīšanas uzņēmuma sērijas numurs | Ievadiet sērijas numuru, ko nosūtīšanas uzņēmums vai aģents norāda nosūtīšanas konteineram. |
| Pārbaudes sertifikāta piemērošanas datums | Datums, kad nosūtīšanas konteineram tika pieprasīta pārbaude. |
| Pārbaudes sertifikāta saņemšanas datums | Pārbaudes sertifikāta saņemšanas datums. |
| Pārbaudes sertifikāta derīguma beigu datums | Pārbaudes sertifikāta termiņa beigu datums. |
| Pārbaudes sertifikāta numurs | Sertifikāta numurs, kas tika izsniegts pēc pārbaudes. |

## <a name="lines-view"></a>Rindu skats

Lai atvērtu **Rindu** skatu, atveriet nosūtīšanas konteineri un pēc tam atlasiet cilni **Rindas** nosūtīšanas konteinera galvenes augšējā labajā stūrī.

### <a name="information-on-the-shipping-container-fasttab"></a>Informācija kopsavilkuma cilnē Pārvadāšanas konteiners

Kopsavilkuma cilne **Nosūtīšanas konteiners** **Rindu** skatā rāda informāciju par folio. Lielākā daļa šīs informācijas parādās arī **Galvenes** skatā, kā aprakstīts iepriekš šajā tēmā.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Kopsavilkuma cilnes Rindas informācija un pogas

Kopsavilkuma cilne **Rindas** skatā **Rindas** rāda detalizētu informāciju par katru pilnu vai daļēju pirkšanas pasūtījuma rindu, kas iekļauta pašreizējā nosūtīšanas konteinerā.

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Rindu** kopsavilkuma cilnes **Rindu** skatā.

| Poga | Apraksts |
|---|---|
| Aizvākt | Noņemt atlasīto pirkšanas pasūtījuma rindu no reisa. |
| Krājumi \> Darbības | Skatiet krājumu darbības atlasītajai pirkšanas pasūtījuma rindai. Ievērojiet, ka, ja izmantojat tranzīta preces, tiek parādīts arī oriģinālais pasūtījums un tranzīta preču pasūtījumi. |
| Krājums \> Dimensiju rādīšana | Atveriet dialoglodziņu, kur var atlasīt krājumu dimensijas, kas parādītas izmaksu darbībām, kuras skatāt. |
| Atsvaidzināt | Atjauniniet informāciju, kas saistīta ar atlasītās pirkšanas pasūtījuma rindas rindas summu, svaru vai tilpumu. |

### <a name="information-on-the-lines-details-fasttab"></a>Kopsavilkuma cilnes Rindas informācija

Kopsavilkuma cilne **Detalizēta informācija par rindām** **Rindu** skatā rāda detalizētu informāciju par pirkšanas pasūtījuma rindu, kas pašlaik ir atlasīta kopsavilkuma cilnē **Rindas**.
