---
title: Formulas un formulu versijas
description: Šajā tēmā ir sniegta informācija par formulām un formulu versijām. Formula procesa ražošanā nosaka konkrētu procesu materiālus, sastāvdaļas un rezultātus. Formulas tiek izmantotas, lai procesa ražošanā plānotu un ražotu preces.
author: cvocph
manager: tfehr
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a67fa0409226432d2068c7ed4f6a876a9278d365
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202058"
---
# <a name="formulas-and-formula-versions"></a>Formulas un formulu versijas

[!include [banner](../includes/banner.md)]

Formula procesa ražošanā nosaka konkrētu procesu materiālus, sastāvdaļas un rezultātus. Kopā ar atbilstošo maršrutu formula nosaka visu procesa ražošanas procesu. Formulas tiek izmantotas, lai procesa ražošanā plānotu un ražotu preces.

Forma sastāv no sastāvdaļām un daudzumiem, kas ir nepieciešami, lai iegūtu konkrētu formulas krājuma daudzumu. Atkarībā no jūsu veiktā uzdevuma formulas funkcionalitātei varat piekļūt no moduļa Krājumu un noliktavas vadība vai no moduļa Preču informācijas vadība.

## <a name="formulas-and-formula-lines"></a>Formulas un formulas rindas
Formula sastāv no vienas vai vairākām formulas rindām, kas identificē sastāvdaļas jeb krājumus, kuri veido formulu. Formulas rinda var ietvert materiālu komplektu (MK) krājumus, formulas krājumus, pieļaujamā svara krājumus, iegādātos krājumus, līdzproduktus vai blakusproduktus. Tā kā daudzi krājumi tiek izmantoti vairākās precēs, vienu krājumu var izmantot vairākās formulās.

Formula ir, piemēram, formula cepumiem ar šokolādes gabaliņiem. Šajā formulā kā sastāvdaļas tiek izmantotas vairākas rindas, piemēram, milti, cukurs, olas, sviests un šokolādes gabaliņi. Formula cepumiem ar šokolādes gabaliņiem ietver sastāvdaļas, kuras, visticamāk, tiek izmantotas arī citās formulās. Gatavojot cepumus ar šokolādes gabaliņiem, var rasties pārpalikumi, piemēram, drupatas, vai daži no cepumiem var piedegt vai nepietiekami izcepties. Atkarībā no ražošanas operācijām šos krājumus var iestatīt kā līdzproduktus vai blakusproduktus.

Veidojot formulas rindu, ir jāizmanto rindas tips, lai norādītu, kā sistēmai šī rinda ir jāapstrādā, kad palaižat vispārējo plānošanu un veidojat partijas pasūtījumus. Katrs rindas tips sniedz atšķirīgu rezultātu. Nākamajā tabulā ir aprakstīti rindu tipi, ko varat atlasīt. 

| Rindas tips     | Apraksts  |
|---------------|--------------|
| Krājums          | Atlasiet **Krājums**, ja krājums ir izejmateriāls vai daļēji pabeigts krājums, kas tiek paņemts no inventāra, vai ja krājums ir kāds pakalpojums. |
| Fantoms       | Atlasiet **Fantoms**, ja vēlaties izvērst jebkurus formulas rindās ietvertos zemāka līmeņa formulas krājumus. Kad novērtējat partijas pasūtījumu un formulas krājumi ir izvērsti, tad komponentu krājumi partijas pasūtījumā ir uzskaitīti kā formulas rindas. Turklāt ražošanas maršrutam tiek pievienoti atbilstošie maršruti. Formulas krājumi tiek izvērsti, izmantojot pašreizējo konfigurāciju. Izmantojot rindas tipu **Fantoms**, varat apstrādāt ražošanas un mērījumu konfigurācijas, kas tiek izmantotas dažādos formulas līmeņos. Ja kādai precei lapas **Nodoto preču papildinformācija** kopsavilkuma cilnē **Inženieris** atlasāt vienumu **Fantoms** un pēc tam šo preci izmantojat kādā formulā, tad šīs formulas rindas tips mainās uz **Fantoms**. Vienumu **Fantoms** nevar atlasīt pieļaujamā svara krājumam un krājumiem, kuru ražošanas tips ir **Līdzprodukts**, **Blakusprodukts** vai **Plānošanas krājums**. |
| Pieprasīta piegāde | Atlasiet **Piesaistītā piegāde**, lai veidotu partijas pasūtījumu, ražošanas pasūtījumu, Kanban darbu, pārsūtīšanas pasūtījumu vai pirkšanas pasūtījumu sastāvdaļai, kas ir ietverta šajā formulas rindā. Saistītais pasūtījums tiek noteikts, pamatojoties uz pasūtījuma noklusējuma iestatījumiem un sastāvdaļas ražošanas tipu, un tas tiek izveidots, kad veicat partijas pasūtījuma novērtējumu. Nepieciešamie sastāvdaļu daudzumi tiek rezervēti partijas pasūtījumam. |
| Kreditors        | Atlasiet vienumu **Kreditors**, ja ražošanas procesā tiek izmantots apakšuzņēmējs un šim apakšuzņēmējam vēlaties izveidot apakšražošanas vai pirkšanas pasūtījumu. Pakalpojums vai darbs, ko izpilda apakšuzņēmējs, ir jāizveido, izmantojot formulas krājumu vai pakalpojuma krājumu. Šo krājumu varat pievienot pamata krājumam kā formulas rindu. Maršrutam jāsatur operācija, kas piešķirta apakšuzņēmēja operāciju resursiem. Šī operācija tiek piesaistīta formulas rindai, izmantojot lauku **Oper. nr.** . |

## <a name="formula-versions"></a>Formulas versijas
Kad veidojat jaunu formulu, pirms formulas rindas krājumu un to specifisko īpašību pievienošanas vispirms ir jāizveido formulas versija. Katrai formulai ir nepieciešama vismaz viena versija. Poga **Apstiprināts** uz formulas versijas kļūst pieejama tikai pēc tam, kad versijas ieraksts ir sekmīgi saglabāts. Katrs formulas versijas ieraksts ir saistīts ar vienu vai vairākiem līdzproduktiem un blakusproduktiem, kurus var saražot, kamēr jūs ražojat pabeigto preci. Daudzas preces var izgatavot no vienām un tām pašām sastāvdaļām atšķirīgu lielumu partijās, komplektos vai ar dažādu ražīgumu. Varat izveidot tik daudz formulas versiju, cik vien nepieciešams.

Lai pārvaldītu vairākas aktīvas formulas versijas, izmantojiet spēkā stāšanās datumu diapazonus vai daudzuma laukus “no”. Vairākas aktīvas formulas versijas var pastāvēt tikai tad, ja datumu diapazons un daudzums “no” nepārklājas.

Atšķirībā no MK, kur viens MK bieži vien ir saistīts ar daudzām MK versijām, katrai formulai parasti pastāv tikai viena formulas versija. Iegaumējiet, ka konkrētas preces vajadzību dimensijām un daudzumam var aktivizēt tikai vienu formulas versiju. Taču daudzas formulas versijas var pastāvēt citu iemeslu dēļ, un tās varat manuāli atlasīt, kad veidojat pasūtījumu partiju.

## <a name="approve-and-activate-formulas-and-formula-versions"></a>Formulu un formulas versiju apstiprināšana un aktivizēšana
Lai formulas un formulas versijas varētu izmantot plānošanai un ražošanai, tās vispirms ir jāapstiprina. Parasti formulas tiek aktivizētas pirms to lietošanas. Taču ražošanas laikā varat atlasīt formulas versiju, kas ir apstiprināta, bet nav aktivizēta.

Lai formulu vai formulas versiju palīdzētu nodrošināt, lapā **Ražošanas kontroles parametri** varat iestatīt parametru **Bloķēt rediģēšanu** un **Bloķēt apstiprinājuma noņemšanu**.

Ja atlasāt **Bloķēt rediģēšanu** un formula ir apstiprināta, tad nevienu formulas rindu lauku nevar dzēst vai rediģēt. Taču, ja noņemat formulas apstiprinājumu, tad formulas rindas varat dzēst un modificēt. Varat arī veidot jaunas formulas un jaunas formulas versijas.

Ja atlasāt **Bloķēt apstiprinājuma noņemšanu**, tad apstiprinātai formulai vai formulas versijai apstiprinājumu noņemt nevar. Taču varat izveidot jaunas formulas un jaunas formulas versijas un varat noņemt formulas versijas aktivizāciju.

Varat pievienot vairāk kontroles līmeņu, izmantojot elektroniskā paraksta funkcionalitāti. Ja lietotājs ir iestatīts tā, ka formulas apstiprināšanas laikā tiek pieprasīts elektroniskais paraksts, tad formulas aktivizēšanas laikā tiek parādīta lapa **Paraksts**. Lai izmaiņas stātos spēkā, lietotājam ir jābūt autorizētam parakstīt elektroniski un sertifikātam ir jātiek sekmīgi validētam. Ja parakstu nevar autentificēt, tad apstiprinājums vai apstiprinājuma noņemšana tiek noraidīta un izmaiņas, kas uzsāka apstiprinājumu vai apstiprinājuma noņemšanu, tiek atgrieztas sākotnējā stāvoklī.

## <a name="use-the-scalable-feature"></a>Līdzekļa Mērogojams lietošana
Līdzeklis Mērogojams ir pieejams tikai tad, ja krājuma komponenti formulā ir iestatīti uz **Mainīgais patēriņš**. Šis līdzeklis nav pieejams, ja krājumu komponenti ir iestatīti uz **Fiksēts patēriņš** vai **Pakāpenisks patēriņš**. Kad tiek lietots līdzeklis Mērogojams, ja formulā maināt kādu sastāvdaļu, tad tiek pielāgots pārējo jūsu atlasīto sastāvdaļu daudzums. Arī formulas lielums tiek pielāgots. Tāpat, ja maināt formulas lielumu, tad tiek mainīts visu mērogojamo sastāvdaļu daudzums. Šis līdzeklis ir speciāli paredzēts formulas izveidošanai un uzturēšanai. Tas nenorāda, vai kādas sastāvdaļas daudzums tiks mērogots uz augšu vai uz leju partijas pasūtījumā.

## <a name="use-step-consumption"></a>Pakāpeniskā patēriņa lietošana
Pakāpeniskais patēriņš likvidē nepieciešamību kādai sastāvdaļai ievadīt daudzumu cilnē **Formulas rinda**. Tā vietā pakāpeniskais patēriņš ir konfigurēts tā, lai tam būtu vērtība **No sērijas** un vērtība **Daudzums**. Tiek atlasīta informācija no pakāpeniskā patēriņa katram sērijas ierakstam, kas apmierina partijas pasūtījuma daudzumu. Pakāpeniskais patēriņš ir noderīgs, ja patēriņa ātrums nav lineārs attiecībā pret partijas pasūtījuma lielumu un tikai palielina vajadzību, kad ir sasniegts noteikts daudzuma slieksnis. Lai iespējotu šo līdzekli jaunai formulai, zem grupas **Patēriņa aprēķins** attiecīgās sastāvdaļas formulas iestatījumu no **Standarta** mainiet uz **Pakāpenisks**. Šo patēriņa metodi varat norādīt lapas **Formulas rinda** cilnē **Iestatījumi**.
