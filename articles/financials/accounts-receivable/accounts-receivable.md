---
title: "Moduļa “Debitoru parādi” sākumlapa"
description: "Izmantojiet debitoru parādu moduli, lai izsekotu debitoru rēķinus un ienākošos maksājumus."
author: twheeloc
manager: AnnBe
ms.date: 08/18/2017
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustomerInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 20671
ms.assetid: 1040678e-ffcb-47fb-a1bc-626db8046504
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b8f2f3a33dc19c2ebc941d1a504eae0c276f3cdf
ms.openlocfilehash: 9fcf106b03cd1abdd135681ceefbb7877f07c773
ms.contentlocale: lv-lv
ms.lasthandoff: 06/25/2018

---

# <a name="accounts-receivable-home-page"></a>Moduļa “Debitoru parādi” sākumlapa

[!include [banner](../includes/banner.md)]

Izmantojiet debitoru parādu moduli, lai izsekotu debitoru rēķinus un ienākošos maksājumus. 

Jūs varat izveidot debitoru rēķinus, kuru pamatā ir pārdošanas pasūtījumi vai pavadzīmes. Turklāt varat ievadīt brīvā teksta rēķinus, kas nav saistīti ar pārdošanas pasūtījumiem. Jūs varat saņemt maksājumus, izmantojot vairākus dažādus maksājuma veidus. Tie ietver vekseļus, skaidru naudu, čekus, kredītkartes un elektroniskos maksājumus. Ja jūsu organizācijā ietilpst vairākas juridiskās personas, varat izmantot centralizētos maksājumus, lai reģistrētu maksājumus vienā juridiskajā personā pārējo juridisko personu vārdā.


**Biznesa procesi**

[![Biznesa process](./media/AR-process.PNG)](./media/AR-process.PNG)

## <a name="set-up-accounts-receivable"></a>Moduļa Debitori iestatīšana

Lai izsekotu debitoru rēķinus un maksājumus, ko saņemat no debitoriem, izmantojiet moduli Debitori. Varat iestatīt debitoru grupas, debitorus, grāmatošanas metodes, procentu paziņojumus, atgādinājuma vēstules, komisijas un ar debitoriem saistītos parametrus, maksas, piegādes un adresātus, kā arī vekseļus un citu veidu debitoru informāciju. 

:::row::: :::column::: - [Uzskaites sadales un apakšgrāmatas žurnāla ieraksti brīva teksta rēķiniem](accounting-distributions-subledger-journal-entries-free-text-invoices.md)
        - [Debitoru grāmatošanas metodes](customer-posting-profiles.md)
        - [Kredītkartes iestatīšana, autorizēšana un nolasīšana](credit-card-authorizations.md)
        - [Debitora rēķinu veidošana](configure-customer-invoices.md)
        - [Periodisku rēķinu iestatīšana un apstrādāšana](set-up-process-recurring-invoices.md)
        - [Brīva teksta rēķina labošana](correct-free-text-invoice.md) :::column-end::: :::column::: - [Vekseļu iestatīšana](set-up-bills-exchange.md)
        - [Procentu koda procentu likmes iestatīšana](set-up-interest-rates-interest-code.md)
        - [Procentu maksu atcelšana, atjaunošana vai anulēšana](waive-reinstate-reverse-interest-fees.md)
        - [SEPA tiešā debeta apskats](sepa-direct-debit-overview.md)
        - [SEPA tiešā debeta pilnvarojuma iestatīšana](sepa-direct-debit-mandate.md)
        - [Debitoru parādu slēgšana](close-accounts-receivable.md) :::column-end::: :::row-end:::


## <a name="set-up-credit-and-collections"></a>Kredīta un iekasēšanas iestatīšana

Debitoru iekasēšanas informācija tiek pārvaldīta vienā centrālā skatā — lapā Iekasēšana. Kredīta un iekasēšanas vadītāji šo centrālo skatu var izmantot, lai pārvaldītu iekasēšanu. Iekasēšanas aģenti var uzsākt iekasēšanas procesu, izmantojot debitoru sarakstus, kas tiek ģenerēti, izmantojot iepriekš definētus iekasēšanas kritērijus, vai lapu Debitori.

[Kredīts un iekasēšana modulī Debitori](collections-credit-accounts-receivable.md)

[Moduļu Debitori un Kredīts un iekasēšana konfigurēšana](accounts-receivables-set-up-overview.md)

[Moduļa Kredīts un iekasēšana iestatīšana](set-up-collections.md)

## <a name="set-up-payments-and-settlements"></a>Maksājumu un segšanas iestatīšana

Pieņemiet dažādu veidu maksājumus no debitoriem, piemēram, vekseļus, skaidru naudu, čekus, kredītkartes un elektroniskos maksājumus. 

:::row::: :::column::: - [Viena debitora maksājuma izmantošana, lai nosegtu vairākus rēķinus ar vairākiem atlaižu periodiem](customer-payment-settle-multiple-invoices-multiple-discount-periods.md)
        - [Centralizēti maksājumi debitoriem](centralized-payments-accounts-receivable.md)
        - [Daļēja debitora maksājuma nosegšana ar galīgo maksājumu par pilnu summu pirms atlaižu piemērošanas datuma](../accounts-payable/settle-partial-customer-payment-or-final-payment-before-discount.md)
        - [Daļēja debitora maksājuma nosegšana pirms atlaižu piemērošanas datuma ar gala maksājumu pēc atlaižu piemērošanas datuma](settle-partial-customer-payment-before-discount-or-final-payment-after.md) :::column-end::: :::column::: - [Tāda daļēja debitora maksājuma segšana, kam ir atlaides debitora kredīta notām](settle-partial-customer-payment-discounts-credit-notes.md)
        - [Daļēju debitora maksājumu nosegšana, kam ir vairāki atlaižu periodi](settle-partial-customer-payment-multiple-discount-periods.md)
        - [Kompensācijas debitoriem](reimburse-customers.md)
        - [Debitoru maksājumi par daļēju summu](customer-payments-partial-amount.md) :::column-end::: :::row-end:::


### <a name="additional-resources"></a>Papildu resursi

#### <a name="whats-new-and-in-development"></a>Jaunumi un drīzumā

Lai apskatītu, kādi jauni līdzekļi ir izlaisti un kādi līdzekļi vēl tiek izstrādāti, dodieties uz [Microsoft Dynamics 365 rīcības plānu](https://roadmap.dynamics.com/). 

#### <a name="blogs"></a>Emuāri

Viedokļi, ziņas un cita informācija par moduli Debitori un citiem risinājumiem ir pieejama [Microsoft Dynamics 365 emuārā](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).

[Microsoft Dynamics AX produktu darba grupas emuārā](https://blogs.msdn.microsoft.com/dax/) ir daudz rakstu par moduli Debitori. Lai gan daži no šiem rakstiem tika rakstīti iepriekšējai moduļa Debitori versijai, joprojām ir spēkā tie paši jēdzieni, un procedūras pašreizējā versijā ir līdzīgas.

[Microsoft Dynamics Operations partneru kopienas emuārā](https://community.dynamics.com/partner/b/operationspartnercommunityblog) Microsoft Dynamics partneriem tiek sniegts vienots resurss, kur uzzināt par jaunumiem un tendencēm risinājumā MBS Operations.

#### <a name="task-guides"></a>Uzdevumu ceļveži
Papildu palīdzībai programmā Finance and Operations ir pieejami uzdevumu ceļveži. Lai piekļūtu uzdevumu ceļvežiem, jebkurā lapā noklikšķiniet uz pogas Palīdzība.

#### <a name="videos"></a>Videoklipi

Skatiet video pamācības, kas tagad ir pieejamas [Microsoft Dynamics 365 YouTube kanālā](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).








