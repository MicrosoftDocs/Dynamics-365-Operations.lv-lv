---
title: BUJ par sagādi
description: Šjā tēmā ir sniegtas atbildes uz bieži uzdotiem jautājumiem (BUJ) par sagādes funkciju programmā Supply Chain Management
author: Henrikan
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 99d44f2409d8207ed7a0fb1fc92a99de42240e86
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577196"
---
# <a name="procurement-faq"></a>BUJ par sagādi

[!include [banner](../includes/banner.md)]

Šjā tēmā ir sniegtas atbildes uz bieži uzdotiem jautājumiem (BUJ) par sagādes funkciju programmā Supply Chain Management.

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Vai var parādīt tikai manis izveidotos pirkšanas pasūtījumus?

Šī funkcionalitāte pašlaik nav pieejama.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Vai var rezervēt krājumus un izveidot darījumus saistībā ar pirkšanas pasūtījumā reģistrētajiem krājumiem?

### <a name="issue-description"></a>Problēmas apraksts

Pat ja vienības pirkšanas pasūtījumā ir ar stāvokli *Reģistrēts*, krājumus joprojām var rezervēt. Citiem vārdiem, varat izveidot darbības saistībā ar reģistrētajiem krājumiem.

### <a name="reproduce-the-issue"></a>Problēmas atveide

Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.

1. Izveidojiet pirkšanas pasūtījumu.
2. Reģistrējiet pirkšanas pasūtījuma rindas.
3. Ievērojiet, ka varat veikt rezervācijas vai darbības saistībā ar reģistrētajiem krājumiem.

### <a name="issue-resolution"></a>Problēmas risinājums

Tas tiek darīts ar nolūku. Sagaidāmais rezultāts ir reģistrēto krājumu fiziska saņemšana noliktavā vai krājumos, lai tādējādi tie būtu pieejami rezervēšanai.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Vai ir iespējams atrast lietotāju, kurš atcēla pirkšanas pasūtījumu?

Šī informācija tiek izsekota tikai tad, ja pirkšanas pasūtījums ir pakļauts izmaiņu pārvaldībai. Ja izmantojat izmaiņu pārvaldību, jūs varat redzēt, kurš iesniedzis izmaiņas (atcelšanu) un kurš tās apstiprinājis.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>Kāpēc nevaru saistīt pirkuma līgumu ar esošu pirkuma pasūtījumu?

Pirkšanas līgums ar pirkšanas pasūtījumu ir jāsaista pirkšanas pasūtījuma izveides laikā. Pretējā gadījumā pirkšanas pasūtījuma rindas nevar saistīt ar pirkšanas līguma rindām.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Kāda pārbaude parāda ziņojumu “Atjauniniet cenas un atlaides, kas ievadītas manuāli vai ārējā dokumentā”?

Mainot nosūtīšanas datumu, var saņemt ziņojumu ar tekstu “Atjauniniet cenas un atlaides, kas ievadītas manuāli vai ārējā dokumentā.” Šis ziņojums tiek parādīts, jo, mainot nosūtīšanas datumu, var rasties cits tirdzniecības vai pārdošanas līgums un tas var izraisīt cenu izmaiņas. Nosūtīšanas datuma maiņa var ietekmēt arī noliktavas grafikus un citu saistīto informāciju.

Ziņojums tiek parādīts katru reizi, kad tiek mainīti datumi vai citi parametri. Ziņojuma mērķis ir pārliecināties, vai esat informēts par cenu izmaiņām, kas var rasties šo izmaiņu dēļ.

Ziņojums ir tirdzniecības līguma novērtēšanas (TAE) uzvedne. Pilnu aprakstu skatiet [Tirdzniecības līguma novērtēšanas politikas](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Kāpēc nevaru grāmatot vairāk nekā vienu pirkuma pasūtījuma rindu, kurai ir kategorijas vienumi?

Grāmatojot rēķinus, daudzums ir obligāts. Tāpēc, ja pilnam rindas daudzumam ir izrakstīts rēķins par tikai daļēju summu, jūs nevarēsit izrakstīt rēķinu atlikušajai summai citā rēķinā.
