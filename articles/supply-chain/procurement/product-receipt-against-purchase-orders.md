---
title: Produktu saņemšana pret pirkšanas pasūtījumiem
description: Šajā tēmā ir aprakstītas dažādas opcijas, lai prod. reģistrētu kā saņemtus.
author: GalynaFedorova
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, VendPackingSlipJournalListPage, VendPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ea22357b4d966f50ef2021ba7534ae633859455
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674398"
---
# <a name="product-receipt-against-purchase-orders"></a>Produktu saņemšana pret pirkšanas pasūtījumiem

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas dažādas opcijas, lai prod. reģistrētu kā saņemtus.

Produktu ieejas plūsma ir process, kas paredzēts, lai reģistrētu, kādi pasūtītie produkti tika saņemti, lai pēc tam pirkšanas pasūtījumu (PP) rindas varētu apstrādāt rēķinu izrakstīšanai. Reizēm produktiem ir jāizpilda sākotnējā reģistrēšana, kur tiek ierakstīta papildu informācija no piegādātāja, pirms produkti tiek saņemti. Kad produkti tiek piegādāti, tie vispirms tiek atzīmēti kā **Reģistrēts**. Produktiem var būt nepieciešams izpildīt papildu procesus, piemēram, kvalitātes pārvaldību, pirms tie visbeidzot tiek atzīmēti kā **Saņemts**.

## <a name="preregistration-asn"></a>Sākotnējā reģistrēšana (IPPN)
Piegādātāji varētu dalīties ar informāciju par produktiem, kas tiks nosūtīti. Šādā gadījumā varat produktus reģistrēt jau sākotnēji, lai ierakstītu šo informāciju, pirms produkti tiek saņemti. Veicot produktu sākotnējo reģistrēšanu, jūs mazināt darba apjomu, kas ir jāveic krājumu reģistrēšanas un saņemšanas laikā. Piegādātāji produktu informāciju var sniegt elektroniski, izmantojot iepriekšēju paziņojumu par nosūtīšanu (IPPN), kurš pēc tam automātiski tiek ierakstīts sistēmā. Informācija šādā IPPN ietver produktu daudzumu, kas tiks nosūtīts, kā arī datumu, kad produkti tiks nosūtīti. IPPN var ietvert arī tādu informāciju kā partijas vai sērijas numuri. IPPN reģistrēšana notiek modulī **Transportēšanas pārvaldība**.

## <a name="registration"></a>Reģistrācija
Produktu ieejas plūsmas reģistrēšana bieži notiek noliktavas saņemšanas dokos. Tā tiek izpildīta, izmantojot pārnēsājamu ierīci vai saņemšanas žurnālus. Produktu ieejas plūsmu varat arī reģistrēt manuāli, izmantojot darbību **Reģistrācija** lapā **Pirkšanas pasūtījums**. Abos gadījumos produkti tiek atzīmēti kā **Reģistrēts**. Ņemiet vērā, ka produkti vēl nav atzīmēti kā **Saņemts**.  

Produktiem, kas tiek saņemti noliktavā, var tikt izpildīta kvalitātes pārbaude, pirms šie produkti tiek izvietoti krājumos. Kvalitātes pārbaudes izpildīšanai var izmantot kvalitātes pārbaudes pasūtījumus vai karantīnas pasūtījumus. Ja izmantojat kvalitātes pārbaudes pasūtījumus, šo procesu varat konfigurēt šos produktus uz laiku bloķēt, izmantojot rezervēšanu, kamēr tie ir pārbaudīti. Ja izmantojat karantīnas pasūtījumus, produkti tiek pārvietoti uz citu noliktavu, lai veiktu pārbaudi. Šī noliktava tiek saukta par karantīnas noliktavu. Abos kvalitātes pārbaudes procesos dažas preces var tikt norakstītas, jo tās neatbilst kvalitātes prasībām vai to kvalitātes pārbaude ietver produkta parauga iznīcinošo pārbaudi.

## <a name="product-receipt"></a>Produktu ieejas plūsma
Vairumā gadījumu darbība **Produktu ieejas plūsma** lapā **Pirkšanas pasūtījumi** tiek izmantota, lai produktus pirkšanas pasūtījuma atzīmētu kā **Saņemts**. Lapā **Produktu ieejas plūsmas grāmatošana** ir dažādas opcijas daudzumam, kas uzskaitē tiek norādīts kā saņemts. Piemēram, lauku **Daudzums** varat iestatīt uz **Pasūtītais daudzums** vai **Tagad saņemamais daudzums**. Ja tiek izmantots process ar saņemšanu noliktavā, šo lauku varat arī iestatīt uz **Reģistrētais daudzums**. Varat modificēt daudzumus katrā pasūtījuma rindā, kas tiks atzīmēta kā **Saņemts**, lai uzskaitē norādītu visas neatbilstības, piemēram, nepietiekamu vai pārmērīgu piegādi. Produktu saņemšanas laikā jums ir jānorāda produkta ieejas plūsmas identifikators, kas parasti ir atsauce uz pavadzīmi no piegādātāja. Šis identifikators ir nepieciešama uzskaitei, jo tas ļauj pārbaudīt vai auditēt piegādātāju pavadzīmes salīdzinājumā ar faktiski saņemto, un uzskaitē iekļautajiem krājumiem vai izdevumiem.  

Pirkšanas pasūtījumus var izveidot produktiem, ko nav paredzēts izmantot kā krājumus, bet kas tiek uzskatīti par izdevumiem. Šī kategorija ietver pasūtījumu rindas, kur produkti ar to krājumu modeļu grupu tiek atzīmēti kā **Nav krājumā**, kā arī rindas, kas lieto sagādes kategorijas. Šādā gadījumā krājumiem var netikt izpildīta piegādes reģistrēšana un saņemšana noliktavā. To vietā tiek izmantota darbība **Produktu ieejas plūsma**, lai šādu ieejas plūsmu ierakstītu tieši pirkšanas pasūtījumā, un ieejas plūsma ir balstīta uz pasūtīto daudzumu, nevis reģistrēto daudzumu.  

Varat izveidot pirkšanas pasūtījuma rindas, kur ir iespējota opcija **Jauns pamatlīdzeklis**. Šī opcija norāda, ka pirkums ir jāuzskata par pamatlīdzekļiem, nevis krājumiem. Tādā gadījumā konfigurētās pamatlīdzekļu noteikšanas kārtulas nosaka, vai produkta vai kategorijas iegāde pārsniedz noteiktus sliekšņus, un tāpēc tie ir jāiekļauj uzskaitē kā līdzekļi un tiem ir jāizpilda pamatlīdzekļu pārvaldība. Iepirkumus var veikt arī uz esošiem pamatlīdzekļiem. Tādā gadījumā summa pēc vajadzības tiek koriģēta.  

Varat atlasīt vairākus pasūtījumus un apstrādāt ieejas plūsmu visiem šiem pasūtījumiem kopā. Šāda metode netiek izmantota ļoti bieži, bet varat vēlēties to izmantot, ja piegādātājs jūsu sūtījumus ir konsolidējis vienā kravā. Pirkuma produktu ieejas plūsmas laikā ir funkcija kopgrāmatojumu veikšanai. Kopgrāmatojuma jums ļauj no piegādātāja grāmatot vienu pavadzīmi par vairākiem pirkšanas pasūtījumiem.  

Pirkšanas pasūtījumus ir iespējams veidot no pārdošanas pasūtījuma, kur ir atlasīta opcija **Tiešā piegāde**. Ja tiek lietota tiešā piegāde, produkti nekad netiek piegādāti jūsu noliktavā, bet no piegādātāja tiek nosūtīti tieši debitoram. Tādā gadījumā ieejas plūsma parasti tiek ierakstīta tieši pirkšanas pasūtījumā. Ieejas plūsmu var izpildīt automātiski, piemēram, izmantojot elektroniskās datu apmaiņas (EDI) integrāciju ar piegādātāju. Ja pirkšanas pasūtījums ir starpuzņēmumu pirkšanas pasūtījums, tad Supply Chain Management sūtījuma veikšanas laikā var arī automatizēt ieejas plūsmu starpuzņēmumu pārdošanas pasūtījumam. Kad tiek lietota tiešā piegāde, produkti joprojām tiek iekļauti uzskaitē kā krājumi, lai gan tie fiziski netiek piegādāti noliktavā. Tādēļ, kad produktu ieejas plūsmu reģistrējat pirkšanas pasūtījumā, pārdošanas pasūtījums tiek automātiski atjaunināts ar pavadzīmi, tādējādi kopējās krājumu izmaiņas ir 0 (nulle). Tiešās piegādes scenārijos jums nav nepieciešama sākotnējā reģistrēšana. Ja lietojat noliktavas, kurām ir iespējota noliktavas vadība, varat apiet prasību reģistrēt noliktavas vienības identifikatoru, tā vietā norādot virtuālu noliktavu. Šo noliktavu jūs norādāt produkta laukā **Tiešās piegādes noliktava**. 

Kad pirkšanas pasūtījumā ir apstrādāta produkta ieejas plūsma, pirkšanas pasūtījuma statuss tiek mainīts uz **Saņemts**, lai norādītu, ka šim pasūtījumam var apstrādāt rēķinu. Detalizētu informāciju par produktiem, kas jau ir saņemti, varat pārskatīt, izmantojot lapu **Produktu ieejas plūsmu žurnāli**.  

Šai lapai varat piekļūt no darbību grupas **Ieejas plūsma** lapā **Pirkšanas pasūtījums**. Informācija šajos žurnālos ietver informāciju par daudzumiem, datumiem un dimensijām.

## <a name="additional-resources"></a>Papildu resursi

[Pirkšanas pasūtījumu apskats](purchase-order-overview.md)

[Pirkšanas pasūtījumu izveidošana](purchase-order-creation.md)

[Pirkšanas pasūtījumu apstiprināšana un ratificēšana](purchase-order-approval-confirmation.md)

[Apskats par kreditoru rēķiniem](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]