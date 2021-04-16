---
title: Pirkšanas pasūtījumu apstiprināšana un ratificēšana
description: Šajā tēmā ir aprakstīti statusi, kas pirkšanas pasūtījumam tiek piešķirti pēc tam, kad tas ir izveidots, un pirkšanas pasūtījumu izmaiņu pārvaldības iespējošanas sekas.
author: kamaybac
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchOrderInReview, PurchOrderApproved, PurchOrderInDraft, PurchOrderAssignedToMe, VendPurchOrderJournalListPage, PurchTableWorkflowDropDialog, VendPurchOrderJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95f1f6971e645a0aae8679c94a4bbd4cba946dc3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825426"
---
# <a name="approve-and-confirm-purchase-orders"></a>Pirkšanas pasūtījumu apstiprināšana un ratificēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti statusi, kas pirkšanas pasūtījumam (PP) tiek piešķirti pēc tam, kad tas ir izveidots, un pirkšanas pasūtījumu izmaiņu pārvaldības iespējošanas sekas.

Kad ir izveidots pirkšanas pasūtījums (PP), iespējams, tam ir jāizpilda apstiprināšanas process. Kad kreditors pasūtījumam ir piekritis, pirkšanas pasūtījumam tiek iestatīts statuss **Ratificēts**.

## <a name="approval-of-purchase-orders"></a>Pirkšanas pasūtījumu apstiprināšana
Pirkšanas pasūtījumiem, kas nelieto izmaiņu pārvaldību, statuss **Apstiprināts** ir jau uzreiz pēc to izveidošanas, bet pirkšanas pasūtījumiem, kas lieto izmaiņu pārvaldību, pēc izveidošanas ir statuss **Melnraksts**. Pirkšanas pasūtījumam, kas ir izveidots, apstiprinot plānotu pasūtījumu no vispārējās plānošanas, neatkarīgi no izmaiņu pārvaldības iestatījumiem vienmēr ir iestatīts statuss **Apstiprināts**. Pirkšanas pasūtījums izveido krājumu transakcijas tikai tad, kad tas sasniedz statusu **Apstiprināts**. Tāpēc līdz brīdim, kad pasūtījums ir pieņemts, šie krājumi netiek rādīti kā pieejami rezervēšanai vai marķēšanai.

Izmaiņu pārvaldību pirkšanas pasūtījumiem jūs iespējojat, iestatot opciju **Aktivizēt izmaiņu pārvaldību** lapā **Sagādes un avotu parametri**. Kad izmaiņu pārvaldība ir iespējota, pirkšanas pasūtījumiem pēc to pabeigšanas ir jāizpilda apstiprināšanas darbplūsma. Programmatūrā Supply Chain Management ir darbplūsmas procesu redaktors, kurā varat definēt darbplūsmu atbilstoši savam apstiprināšanas procesam. Šajā darbplūsmā var ietvert kārtulas automātiskai apstiprināšanai, kārtulas, kas nosaka, kurš tiks norīkots konkrētu pirkšanas pasūtījumu apstiprināšanai, kā arī kārtulas tādu darbplūsmu eskalēšanai, kas ilgi gaida apstiprinājumu. Izmaiņu pārvaldības procesu varat iespējot visiem kreditoriem vai atsevišķiem kreditoriem. Šo procesu varat arī iestatīt tā, lai atsevišķiem pirkšanas pasūtījumiem to varētu ignorēt.

Kad ir iespējota izmaiņu pārvaldība, pirkšanas pasūtījumi tiek vadīti cauri sešiem apstiprināšanas statusiem, no **Melnraksts** līdz **Pabeigts**. Kad pasūtījums ir apstiprināts, lietotājiem, kuri vēlas to modificēt, ir jāizmanto darbība **Pieprasīt izmaiņas**.

| Apstiprināšanas statuss | Apraksts                                                                      | Izmaiņu pieprasīšana ir iespējota |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Melnraksts           | Šis pirkšanas pasūtījums ir melnraksts, un tas nav iesniegts PP darbplūsmā apstiprināšanai.     | Nē                        |
| Pārskatīšanā       | Šis pirkšanas pasūtījums tika iesniegts PP darbplūsmā apstiprināšanai. Apstiprinājums tiek gaidīts.       | Nē                        |
| Atteikts        | Šis pirkšanas pasūtījums apstiprināšanas procesa laikā tika noraidīts.                                 | Nē                        |
| Apstiprināts        | Šis pirkšanas pasūtījums tika apstiprināts.                                                             | Jā                       |
| Akceptēts       | Šis pirkšanas pasūtījums tika ratificēts. Pirkšanas pasūtījumu var ratificēt tikai pēc tam, kad tas ir apstiprināts.        | Jā                       |
| Pabeigtie       | Šis pirkšanas pasūtījums ir galīgs. Tagad tas ir finansiāli slēgts, un to vairs nav mainīt. | Nē                        |

## <a name="confirming-purchase-orders"></a>Pirkšanas pasūtījumu ratificēšana
Pirkšanas pasūtījumiem, kuru apstiprinājuma statuss ir **Apstiprināts**, pirms to ratificēšanas var izpildīt papildu darbības. Piemēram, iespējams, jums kāds pirkšanas pieprasījums ir jāsūta kreditoram, lai uzzinātu informāciju par cenām, atlaidēm vai piegādes datumiem. Šādā gadījumā pirkšanas pasūtījumam varat iestatīt statusu **Tiek pārskatīts ārēji**, izmantojot darbību **Pirkšanas pieprasījums**.

Kreditori, kas ir iestatīti kreditoru portāla lietošanai, var pārskatīt portālā esošos pasūtījumus un tos apstiprināt vai noraidīt. Šī pārskatīšanas procesa laikā pirkšanas pasūtījuma statuss ir **Tiek pārskatīts ārēji**. Kreditoru portālu var konfigurēt tā, lai ratificēšana no kreditora automātiski ratificētu šo pasūtījumu programmatūrā Supply Chain Management. Pirkšanas pasūtījumu varat arī ratificēt manuāli, kad esat saņēmis ratifikāciju no kreditora. Ja kreditors kādu pirkšanas pasūtījumu noraida, tad noraidījums tiek saņemts kopā ar noraidīšanas iemeslu un izmaiņu ierosinājumiem. Šajā gadījumā pirkšanas pasūtījuma statuss saglabājas kā **Tiek pārskatīts ārēji**.

Pastāv arī iespēja ģenerēt pasūtījuma pro forma ratifikāciju, pirms ir apstrādāta faktiskā ratifikācija. Šī opcija tikai izveido atskaiti, kuru var koplietot ar kreditoru. Tā neizveido nekādu žurnāla informāciju.

Kad kreditors ir piekritis pasūtījumam, pēc tam šis pirkšanas pasūtījums ir jāreģistrē kā fiksēts. Šo darbību varat izpildīt, izmantojot darbību **Ratifikācija** vai darbību **Ratificēt**. Abas šīs darbības pasūtījuma apstiprinājuma statusu iestata uz **Ratificēts**. Pasūtījuma ratificēšana uzsāk divus papildu procesus:

-   Tiek izveidots žurnāls, lai glabātu precīzu sistēmā ratificētās informācijas kopiju. Reizēm pasūtījumos ir jāveic izmaiņas, un pēc atjauninātā pasūtījuma ratificēšanas tiek izveidoti papildu žurnāli. Šie žurnāli jums ļauj apskatīt pasūtījuma dažādo ratificēto versiju vēsturi.
-   Tiek izveidotas uzskaites sadales, un notiek pasūtījuma pārbaudes un budžeta pārbaudes, ja šī funkcionalitāte ir iespējota. Ja kāda no pārbaudēm ir nesekmīga, jūs saņemat kļūdas ziņojumu, kurā teikts, ka pirkšanas pasūtījumā ir jāveic izmaiņas, pirms to var atkal ratificēt.

Kreditors var pieprasīt kaut kādu apliecinājumu, ka par pirkumu tiks sniegts maksājums. Šādas garantijas sniegšanai kreditoriem maksājamo parādu procesos ir dažādas metodes. Piemēram, darbība **Priekšapmaksa** rezervē līdzekļus attiecīgajam pirkšanas pasūtījumam, un šī priekšapmaksa tiek reģistrēta pirkšanas pasūtījumā.

## <a name="changing-purchase-orders"></a>Pirkšanas pasūtījumu mainīšana
Reizēm jums var rasties nepieciešamība mainīt pirkšanas pasūtījumu pēc tam, kad tas ir sasniedzis apstiprinājuma statusu **Apstiprināts** vai **Ratificēts**.

Ja pirkšanas pasūtījums tika izveidots, izmantojot izmaiņu pārvaldības procesu, tad izmaiņas varat veikt, atsaucot pasūtījumu vai — ja pasūtījums jau ir apstiprināts — izmantojot darbību **Pieprasīt izmaiņas**. Šādā gadījumā apstiprinājuma statuss tiek mainīts atpakaļ uz **Melnraksts**, un pēc tam šo pasūtījumu varat modificēt. Kad esat beidzis izmaiņu veikšanu, iespējams, pirkšanas pasūtījums ir jāiesniedz atkārtotai apstiprināšanai. Varat konfigurēt, kāda tipa izmaiņām ir nepieciešama atkārtota apstiprināšana, izmantojot ierobežojuma nosacījumu **Atkārtotas apstiprināšanas kārtula pirkšanas pasūtījumiem** lapā **Pirkšanas ierobežojumi**.

Ja daļa no pasūtītā daudzuma kādai pirkšanas pasūtījuma rindai ir piegādāta, tad pasūtīto daudzumu mainīt nevar, kad pirkšanas pasūtījums ir **Melnrakstā**. Tomēr jūs varat mainīt **Piegādātā atlikuma** daudzumu rindas pirkšanas pasūtījumam, kas ir **Melnraksta** statusā.

Kad pasūtījums ir ratificēts, to vairs nevar izdzēst. Taču varat atcelt kopējo daudzumu vai jebkuru atlikušo daudzumu pasūtījumā, ja vien šis daudzums vēl nav saņemts vai iekļauts rēķinā. Pēc tam varat izmantot darbību **Pabeigt**, lai novērstu turpmāku apstrādāšanu. 


## <a name="canceling-purchase-orders"></a>Pirkšanas pasūtījumu atcelšana

PP var tikt atcelts, izmantojot galvenes darbību **Atcelt**.

Ja daudzums ir daļēji reģistrēts, saņemts vai iekļauts rēķinā, varat atcelt tikai atlikušo daudzumu, kas nav reģistrēts, saņemts vai iekļauts rēķinā. Pēc tam pasūtījuma daudzums attiecīgi tiek samazināts. Kad rindas daudzums ir atjaunināts, tiek atjaunināts arī rindas statuss. Piemēram, sākotnējais daudzums rindā ir 5, un tiek saņemts 3.  Šādā gadījumā var atcelt tikai divas. Pēc tam rinda tiek atjaunināta uz statusu **Saņemts**.

Ja pasūtījuma rindai ir pievienots saņemšanas atlikums un tas pārsniedz pasūtījuma rindā norādīto daudzumu, darbība **Atcelt** neatceļ lieko daudzumu. Tā vietā rinda paliek statusā **Atvērts pasūtījums**, jo tai ir atlikušais daudzums. Piemēram, sākotnējais daudzums rindā ir 5, un saņemšanas atlikums ir 7. Ja pasūtījums ir atcelts, tiek atceltas piecas, un divas paliek, kā tas redzams krājumu transakcijās.

Lai atceltu visu daudzumu PP rindā, ir jāatceļ sūtījuma atlikuma daudzums rindā. Pēc tam rinda tiks atjaunināta uz **Atcelts** statusu.

Ja PP ir izmaiņu vadībā, jebkādas izmaiņas, piemēram, pasūtījuma atcelšana vai piegādes atlikums, ir jāiesniedz darbplūsmas sistēmā un jāapstiprina pirms procesa pabeigšanas, un krājumu transakcijas var atjaunināt kā atceltas.

<a name="additional-resources"></a>Papildu resursi
--------

[Pirkšanas pasūtījumu apskats](purchase-order-overview.md)

[Pirkšanas pasūtījumu izveidošana](purchase-order-creation.md)

[Produktu ieejas plūsma pret pirkšanas pasūtījumiem](product-receipt-against-purchase-orders.md)

[Kreditoru rēķinu pārskats](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]