---
title: "Pirkšanas pasūtījumu apstiprināšana un ratificēšana"
description: "Šajā rakstā ir aprakstīti statusi, kas pirkšanas pasūtījumam (PP) tiek piešķirti pēc tam, kad tas ir izveidots, un pirkšanas pasūtījumu izmaiņu pārvaldības iespējošanas sekas."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 0ec91bcf0ab334585eefae2fe54750c45419682e
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017

---

# <a name="approve-and-confirm-purchase-orders"></a>Pirkšanas pasūtījumu apstiprināšana un ratificēšana

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Šajā rakstā ir aprakstīti statusi, kas pirkšanas pasūtījumam (PP) tiek piešķirti pēc tam, kad tas ir izveidots, un pirkšanas pasūtījumu izmaiņu pārvaldības iespējošanas sekas.

Kad ir izveidots pirkšanas pasūtījums (PP), iespējams, tam ir jāizpilda apstiprināšanas process. Kad kreditors pasūtījumam ir piekritis, pirkšanas pasūtījumam tiek iestatīts statuss **Ratificēts**.

## <a name="approval-of-purchase-orders"></a>Pirkšanas pasūtījumu apstiprināšana
Pirkšanas pasūtījumiem, kas nelieto izmaiņu pārvaldību, statuss **Apstiprināts** ir jau uzreiz pēc to izveidošanas, bet pirkšanas pasūtījumiem, kas lieto izmaiņu pārvaldību, pēc izveidošanas ir statuss **Melnraksts**. Pirkšanas pasūtījumam, kas ir izveidots, apstiprinot plānotu pasūtījumu no vispārējās plānošanas, neatkarīgi no izmaiņu pārvaldības iestatījumiem vienmēr ir iestatīts statuss **Apstiprināts**. Pirkšanas pasūtījums izveido krājumu transakcijas tikai tad, kad tas sasniedz statusu **Apstiprināts**. Tāpēc līdz brīdim, kad pasūtījums ir pieņemts, šie krājumi netiek rādīti kā pieejami rezervēšanai vai marķēšanai.  

Izmaiņu pārvaldību pirkšanas pasūtījumiem jūs iespējojat, iestatot opciju **Aktivizēt izmaiņu pārvaldību** lapā **Sagādes un avotu parametri**. Kad izmaiņu pārvaldība ir iespējota, pirkšanas pasūtījumiem pēc to pabeigšanas ir jāizpilda apstiprināšanas darbplūsma. Programmatūrā Microsoft Dynamics 365 for Finance and Operations ir darbplūsmas procesu redaktors, kur varat definēt darbplūsmu savam apstiprināšanas procesam. Šajā darbplūsmā var ietvert kārtulas automātiskai apstiprināšanai, kārtulas, kas nosaka, kurš tiks norīkots konkrētu pirkšanas pasūtījumu apstiprināšanai, kā arī kārtulas tādu darbplūsmu eskalēšanai, kas ilgi gaida apstiprinājumu. Izmaiņu pārvaldības procesu varat iespējot visiem kreditoriem vai atsevišķiem kreditoriem. Šo procesu varat arī iestatīt tā, lai atsevišķiem pirkšanas pasūtījumiem to varētu ignorēt.  

Kad ir iespējota izmaiņu pārvaldība, pirkšanas pasūtījumi tiek vadīti cauri sešiem apstiprināšanas statusiem, no **Melnraksts** līdz **Pabeigts**. Kad pasūtījums ir apstiprināts, lietotājiem, kuri vēlas to modificēt, ir jāizmanto darbība **Pieprasīt izmaiņas**.

| Apstiprināšanas statuss | Apraksts                                                                      | Izmaiņu pieprasīšana ir iespējota |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Melnraksts           | Šis pirkšanas pasūtījums ir melnraksts, un tas nav iesniegts PP darbplūsmā apstiprināšanai.     | Nē                        |
| Tiek pārskatīts       | Šis pirkšanas pasūtījums tika iesniegts PP darbplūsmā apstiprināšanai. Apstiprinājums tiek gaidīts.       | Nē                        |
| Atteikts        | Šis pirkšanas pasūtījums apstiprināšanas procesa laikā tika noraidīts.                                 | Nē                        |
| Apstiprināts        | Šis pirkšanas pasūtījums tika apstiprināts.                                                             | Jā                       |
| Apstiprināts       | Šis pirkšanas pasūtījums tika ratificēts. Pirkšanas pasūtījumu var ratificēt tikai pēc tam, kad tas ir apstiprināts.        | Jā                       |
| Pabeigts       | Šis pirkšanas pasūtījums ir galīgs. Tagad tas ir finansiāli slēgts, un to vairs nav mainīt. | Nē                        |

## <a name="confirming-purchase-orders"></a>Pirkšanas pasūtījumu ratificēšana
Pirkšanas pasūtījumiem, kuru apstiprinājuma statuss ir **Apstiprināts**, pirms to ratificēšanas var izpildīt papildu darbības. Piemēram, iespējams, jums kāds pirkšanas pieprasījums ir jāsūta kreditoram, lai uzzinātu informāciju par cenām, atlaidēm vai piegādes datumiem. Šādā gadījumā pirkšanas pasūtījumam varat iestatīt statusu **Tiek pārskatīts ārēji**, izmantojot darbību **Pirkšanas pieprasījums**.  

Kreditori, kas ir iestatīti kreditoru portāla lietošanai, var pārskatīt portālā esošos pasūtījumus un tos apstiprināt vai noraidīt. Šī pārskatīšanas procesa laikā pirkšanas pasūtījuma statuss ir **Tiek pārskatīts ārēji**. Kreditoru portālu var konfigurēt tā, lai ratificēšana no kreditora automātiski ratificētu šo pasūtījumu programmatūrā Finance and Operations. Pirkšanas pasūtījumu varat arī ratificēt manuāli, kad esat saņēmis ratifikāciju no kreditora. Ja kreditors kādu pirkšanas pasūtījumu noraida, tad noraidījums tiek saņemts kopā ar noraidīšanas iemeslu un izmaiņu ierosinājumiem. Šajā gadījumā pirkšanas pasūtījuma statuss saglabājas kā **Tiek pārskatīts ārēji**.  

Pastāv arī iespēja ģenerēt pasūtījuma pro forma ratifikāciju, pirms ir apstrādāta faktiskā ratifikācija. Šī opcija tikai izveido atskaiti, kuru var koplietot ar kreditoru. Tā neizveido nekādu žurnāla informāciju.  

Kad kreditors ir piekritis pasūtījumam, pēc tam šis pirkšanas pasūtījums ir jāreģistrē kā fiksēts. Šo darbību varat izpildīt, izmantojot darbību **Ratifikācija** vai darbību **Ratificēt**. Abas šīs darbības pasūtījuma apstiprinājuma statusu iestata uz **Ratificēts**. Pasūtījuma ratificēšana uzsāk divus papildu procesus:

-   Tiek izveidots žurnāls, lai glabātu precīzu sistēmā ratificētās informācijas kopiju. Reizēm pasūtījumos ir jāveic izmaiņas, un pēc atjauninātā pasūtījuma ratificēšanas tiek izveidoti papildu žurnāli. Šie žurnāli jums ļauj apskatīt pasūtījuma dažādo ratificēto versiju vēsturi.
-   Tiek izveidotas uzskaites sadales, un notiek pasūtījuma pārbaudes un budžeta pārbaudes, ja šī funkcionalitāte ir iespējota. Ja kāda no pārbaudēm ir nesekmīga, jūs saņemat kļūdas ziņojumu, kurā teikts, ka pirkšanas pasūtījumā ir jāveic izmaiņas, pirms to var atkal ratificēt.

Kreditors var pieprasīt kaut kādu apliecinājumu, ka par pirkumu tiks sniegts maksājums. Šādas garantijas sniegšanai kreditoriem maksājamo parādu procesos ir dažādas metodes. Piemēram, darbība **Priekšapmaksa** rezervē līdzekļus attiecīgajam pirkšanas pasūtījumam, un šī priekšapmaksa tiek reģistrēta pirkšanas pasūtījumā.

## <a name="changing-purchase-orders"></a>Pirkšanas pasūtījumu mainīšana
Reizēm jums var rasties nepieciešamība mainīt pirkšanas pasūtījumu pēc tam, kad tas ir sasniedzis apstiprinājuma statusu **Apstiprināts** vai **Ratificēts**.  

Ja pirkšanas pasūtījums tika izveidots, izmantojot izmaiņu pārvaldības procesu, tad izmaiņas varat veikt, atsaucot pasūtījumu vai — ja pasūtījums jau ir apstiprināts — izmantojot darbību **Pieprasīt izmaiņas**. Šādā gadījumā apstiprinājuma statuss tiek mainīts atpakaļ uz **Melnraksts**, un pēc tam šo pasūtījumu varat modificēt. Kad esat beidzis izmaiņu veikšanu, iespējams, pirkšanas pasūtījums ir jāiesniedz atkārtotai apstiprināšanai. Varat konfigurēt, kāda tipa izmaiņām ir nepieciešama atkārtota apstiprināšana, izmantojot ierobežojuma nosacījumu **Atkārtotas apstiprināšanas kārtula pirkšanas pasūtījumiem** lapā **Pirkšanas ierobežojumi**.  

Ja daļa no pasūtītā daudzuma kādai pirkšanas pasūtījuma rindai ir piegādāta, tad pasūtīto daudzumu mainīt nevar. Taču varat mainīt daudzumu **Atlicis piegādāt** šajā rindā. Pēc tam varat izmantot darbību **Pabeigt**, lai atceltu rindas un novērstu turpmāku apstrādāšanu. 

Kad pasūtījums ir ratificēts, to vairs nevar izdzēst. Taču varat atcelt kopējo daudzumu vai jebkuru atlikušo daudzumu pasūtījumā, ja vien šis daudzums vēl nav saņemts vai iekļauts rēķinā.

<a name="see-also"></a>Skatiet arī
--------

[Pārskats par pirkšanas pasūtījumu](purchase-order-overview.md)

[Pirkšanas pasūtījuma izveide](purchase-order-creation.md)

[Produktu ieejas plūsma pret pirkšanas pasūtījumiem](product-receipt-against-purchase-orders.md)

[Apskats par kreditoru rēķiniem](/dynamics365/unified-operations/financials/accounts-payable/vendor-invoices-overview)




