---
title: Kredītkartes iestatīšana, autorizācija un nolasīšana
description: Šajā rakstā sniegts pārskats par kredītkartes autorizāciju Microsoft Dynamics 365 Finansēs. Šeit ir iekļauta arī informācija par to, kā iestatīt maksājumu pakalpojumu, pievienot kredītkarti pārdošanas pasūtījumam un anulēt autorizāciju.
author: ShivamPandeymsft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b84fe90e6c01d06ecbb3a1e13a9f018d385c22c0
ms.sourcegitcommit: 346a9ca833237836d5e4ca496aeb2b5b24bdb27b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2022
ms.locfileid: "9583783"
---
# <a name="credit-card-setup-authorization-and-capture"></a>Kredītkartes iestatīšana, autorizācija un nolasīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā sniegts pārskats par kredītkartes autorizāciju Microsoft Dynamics 365 Finansēs. Šeit ir iekļauta arī informācija par to, kā iestatīt maksājumu pakalpojumu, pievienot kredītkarti pārdošanas pasūtījumam un anulēt autorizāciju.

## <a name="setting-up-the-credit-card-payment-service"></a>Kredītkartes maksājumu pakalpojuma iestatīšana

Lai izmantotu kredītkartes, ir jāiestata un jāaktivizē maksājumu pakalpojums lapā Maksājumu pakalpojumi. Maksājumu pakalpojums nodrošina starpniecību starp jūsu juridisko personu un banku, kas apstrādā debitora maksājumus ar kredītkarti. Jums ir jāsadarbojas ar kredītkartes nodrošinātāju, kas ir norādīts laukā Maksājumu savienotājs, un jāiestata šī nodrošinātāja konts. Pēc tam jums ir jāiesta citas opcijas lapā Maksājumu pakalpojumi, jāiestata kredītkaršu veidi American Express, Discover, MasterCard un Discover lapā Kredītkaršu veidi un jāaktivizē maksājuma nodrošinātājs kā noklusējuma nodrošinātājs. Lai pabeigtu iestatīšanu, ir jāveic arī tālāk norādītās darbības.
-   Lapā Debitoru parādu parametri norādiet kredītkaršu autorizācijas izmantošanas parametrus.
-   Lapā Apmaksas nosacījumi iestatiet kredītkaršu maksājumu nosacījumus. Laukā Maksājuma veids atlasiet opciju Kredītkarte.
-   Lapā Debitora kredītkartes ievadiet debitoru kredītkaršu informāciju.

## <a name="adding-a-new-credit-card"></a>Jaunas kredītkartes pievienošana
Varat izveidot jaunus kredītkaršu ierakstus lapā Debitori izmantojot opcijas Debitors, Iestatīt, Kredītkarte. Varat arī izveidot kredītkaršu ierakstus, kad ievadāt pārdošanas pasūtījumus lapā Pārdošanas pasūtījums, izmantojot opcijas Pārvaldīt, Debitors, Kredītkarte, Reģistrēt.

## <a name="adding-a-credit-card-to-a-sales-order"></a>Kredītkartes pievienošana pārdošanas pasūtījumam

Varat pievienot kredītkarti pārdošanas pasūtījumam, atlasot kredītkarti kredītkartes uzmeklēšanas laukā lapas Pārdošanas pasūtījums kopsavilkuma cilnē Debitora kredītkartes. Lai sāktu autorizācijas procesu, cilnes Pārvaldīt darbību rūtī atlasiet opcijas Kredītkarte un Autorizēt.

## <a name="authorizing-a-credit-card"></a>Kredītkartes autorizācija

Autorizējot kredītkarti, tiek pārbaudīts kartes numurs un kartes īpašnieka vārds un tiek apstiprināta pieejamā kredīta bilance. Pēc izvēles tiek pārbaudīta kartes verificēšanas vērtība un kartes īpašnieka adrese. Pēc tam debitora pieejamā kredīta bilance tiek samazināta par rēķina summu. Maksājumu pakalpojums nosūta informāciju par to, ka kredītkarte ir apstiprināta vai noraidīta. Kad pārdošanas pasūtījums tiek iekļauts rēķinā, no kredītkartes konta tiek iekasēta (nolasīta) rēķina summa.

### <a name="card-verification-value"></a>Kartes verificēšanas vērtība

Varat pieprasīt kartes verificēšanas vērtību, kas dažreiz tiek saukta par kartes drošības kodu. American Express kartei tā ir četrciparu vērtība. Discover, MasterCard un Visa kartēm tā ir trīsciparu vērtība.

### <a name="address-verification"></a>Adreses pārbaude

Maksājuma nodrošinātājam vienmēr tiek nosūtīta adreses pārbaudes informācija. Varat izlemt, cik daudz informācijas ir nepieciešams, lai transakciju pieņemtu. Noteikti sazinieties ar savu nodrošinātāju, lai noteiktu, vai tas pieņem šo informāciju. Tālāk ir norādītas adreses pārbaudes opcijas.
-   **Vienmēr pieņemt transakciju** — pieņemt transakciju neatkarīgi no adreses pārbaudes rezultātiem.
-   **Konta īpašnieks** — salīdzināt transakcijā norādīto kartes īpašnieka vārdu ar kredītkartes nodrošinātājam pieejamo informāciju.
-   **Rēķina adrese** — salīdzināt transakcijā norādīto kartes īpašnieka vārdu un rēķina adresi ar kredītkartes nodrošinātājam pieejamo informāciju.
-   **Rēķina pasta kods** — salīdzināt transakcijā norādīto kartes īpašnieka vārdu, rēķina adresi un pasta indeksu ar kredītkartes nodrošinātājam pieejamo informāciju.

## <a name="data-support"></a>Datu atbalsts
Katram atbalstītajam kredītkartes veidam varat norādīt datu atbalsta līmeni. Izmantojot šo līmeni, tiek kontrolēts, cik daudz informācijas par transakciju tiek pārsūtīts uz maksājumu pakalpojumu. Noteikti sazinieties ar savu maksājumu nodrošinātāju, lai noteiktu, vai nodrošinātājs var sniegt šo informāciju. Tālāk ir norādītas datu atbalsta līmeņa opcijas.
-   **1. līmenis** — pārsūtīt transakcijas datumu, transakcijas summu un aprakstu.
-   **2. līmenis** — pārsūtīt visu 1. līmeņa informāciju, kā arī piegādes un tirgotāja adreses un nodokļu informāciju.
-   **3. līmenis** — pārsūtīt visu 2. līmeņa informāciju, kā arī pasūtījuma rindas informāciju.

## <a name="partial-payments"></a>Daļēji maksājumi
Ja nosūtāt daļu pasūtījuma, tiek nolasīta daļējā pasūtījuma summa un tiek slēgta autorizācija, kas attiecas uz visa pasūtījuma summu. Pēc tam tiek iesniegta jauna autorizācija, kas attiecas uz atlikušo nenosūtītas pasūtījuma daļas summu.

## <a name="voiding-an-authorization"></a>Autorizācijas anulēšana
Lai anulētu kredītkartes autorizāciju, varat mainīt maksājuma metodi, izvēloties citu metodi, kuras vieds nav Kredītkarte.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
