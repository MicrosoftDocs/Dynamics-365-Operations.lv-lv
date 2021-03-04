---
title: Moduļa “Debitoru parādi” sākumlapa
description: Izmantojiet moduli “Debitoru parādi”, lai izsekotu debitoru rēķinus un ienākošos maksājumus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/18/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 20671
ms.assetid: 1040678e-ffcb-47fb-a1bc-626db8046504
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c47fc9e3627e5ecb41ecba6854729ef340493c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993142"
---
# <a name="accounts-receivable-home-page"></a>Moduļa “Debitoru parādi” sākumlapa

[!include [banner](../includes/banner.md)]

Izmantojiet moduli “Debitoru parādi”, lai izsekotu debitoru rēķinus un ienākošos maksājumus. 

Jūs varat izveidot debitoru rēķinus, kuru pamatā ir pārdošanas pasūtījumi vai pavadzīmes. Turklāt varat ievadīt brīvā teksta rēķinus, kas nav saistīti ar pārdošanas pasūtījumiem. Jūs varat saņemt maksājumus, izmantojot vairākus dažādus maksājuma veidus. Tie ietver vekseļus, skaidru naudu, čekus, kredītkartes un elektroniskos maksājumus. Ja jūsu organizācijā ietilpst vairākas juridiskās personas, varat izmantot centralizētos maksājumus, lai reģistrētu maksājumus vienā juridiskajā personā pārējo juridisko personu vārdā.


**Biznesa procesi**

[![Biznesa process](./media/AR-process.PNG)](./media/AR-process.PNG)

## <a name="set-up-accounts-receivable"></a>Moduļa “Debitoru parādi” iestatīšana

Lai izsekotu debitoru rēķinus un maksājumus, ko saņemat no debitoriem, izmantojiet moduli Debitori. Varat iestatīt debitoru grupas, debitorus, grāmatošanas metodes, procentu paziņojumus, atgādinājuma vēstules, komisijas un ar debitoriem saistītos parametrus, maksas, piegādes un adresātus, kā arī vekseļus un citu veidu debitoru informāciju. 

:::row:::
    :::column:::
        - [Uzskaites sadales un apakšgrāmatas žurnālu ieraksti brīva teksta rēķiniem](accounting-distributions-subledger-journal-entries-free-text-invoices.md)
        - [Debitoru grāmatošanas metodes](customer-posting-profiles.md)
        - [Kredītkartes iestatīšana, autorizēšana un nolasīšana](credit-card-authorizations.md)
        - [Debitora rēķina izveide](configure-customer-invoices.md)
        - [Periodisku rēķinu iestatīšana un apstrādāšana](set-up-process-recurring-invoices.md)
        - [Brīva teksta rēķina labošana](correct-free-text-invoice.md)
    :::column-end:::
    :::column:::
        - [Vekseļu iestatīšana](set-up-bills-exchange.md)
        - [Procentu likmju iestatīšana interešu kodam](set-up-interest-rates-interest-code.md)
        - [Procentu maksu atcelšana, atjaunošana vai anulēšana](waive-reinstate-reverse-interest-fees.md)
        - [SEPA tiešā debeta apskats](sepa-direct-debit-overview.md)
        - [SEPA tiešā debeta pilnvarojuma iestatīšana](sepa-direct-debit-mandate.md)
        - [Moduļa “Debitoru parādi” slēgšana](close-accounts-receivable.md)
    :::column-end:::
:::row-end:::


## <a name="set-up-credit-and-collections"></a>Kredīta un iekasēšanas iestatīšana

Debitoru iekasēšanas informācija tiek pārvaldīta vienā centrālā skatā — lapā Iekasēšana. Kredīta un iekasēšanas vadītāji šo centrālo skatu var izmantot, lai pārvaldītu iekasēšanu. Iekasēšanas aģenti var uzsākt iekasēšanas procesu, izmantojot debitoru sarakstus, kas tiek ģenerēti, izmantojot iepriekš definētus iekasēšanas kritērijus, vai lapu Debitori.

[Kredīts un iekasēšana modulī “Debitoru parādi”](collections-credit-accounts-receivable.md)

[Moduļu Debitori un Kredīts un iekasēšana konfigurēšana](accounts-receivables-set-up-overview.md)

[Kredīta un iekasēšanas iestatīšana](set-up-collections.md)

## <a name="set-up-payments-and-settlements"></a>Maksājumu un segšanas iestatīšana

Pieņemiet dažādu veidu maksājumus no debitoriem, piemēram, vekseļus, skaidru naudu, čekus, kredītkartes un elektroniskos maksājumus. 

:::row:::
    :::column:::
        - [Lietot viena debitora maksājumu, lai nosegtu vairākus rēķinus ar vairākiem atlaižu periodiem](customer-payment-settle-multiple-invoices-multiple-discount-periods.md)
        - [Centralizētie maksājumi modulim “Debitoru parādi”](centralized-payments-accounts-receivable.md)
        - [Daļēja debitora maksājuma un gala maksājuma pilnā apmērā segšana pirms atlaižu piemērošanas datuma](../accounts-payable/settle-partial-customer-payment-or-final-payment-before-discount.md)
        - [Daļēja debitora maksājuma segšana pirms atlaižu piemērošanas datuma ar gala maksājumu pēc atlaižu piemērošanas datuma](settle-partial-customer-payment-before-discount-or-final-payment-after.md)
    :::column-end:::
    :::column:::
        - [Nosegt daļēju debitora maksājumu, kam ir atlaides kredīta notām](settle-partial-customer-payment-discounts-credit-notes.md)
        - [Nosegt daļēju debitora maksājumu, kam ir vairāki atlaižu periodi](settle-partial-customer-payment-multiple-discount-periods.md)
        - [Atlīdzināšana debitoriem](reimburse-customers.md)
        - [Debitoru maksājumi par daļēju summu](customer-payments-partial-amount.md)
    :::column-end:::
:::row-end:::


### <a name="additional-resources"></a>Papildu resursi

#### <a name="whats-new-and-in-development"></a>Jaunumi un drīzumā gaidāmais

Lai uzzinātu, kādus jaunus līdzekļus plānots ieviest, skatiet [Microsoft Dynamics 365 rīcības plānu](https://go.microsoft.com/fwlink/?linkid=2010158). 

#### <a name="blogs"></a>Emuāri

Viedokļi, ziņas un cita informācija par moduli Kreditori un citiem risinājumiem ir pieejama [Microsoft Dynamics 365 emuārā](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) un [Microsoft Dynamics 365 Finance and Operations — Financials emuārā](https://community.dynamics.com/365/financeandoperations/b/financials).

[Microsoft Dynamics Operations partneru kopienas emuārā](https://community.dynamics.com/partner/b/operationspartnercommunityblog) Microsoft Dynamics partneriem tiek nodrošināts vienots resurss, kur uzzināt par jaunumiem un tendencēm risinājumā Dynamics 365.

#### <a name="task-guides"></a>Uzdevumu ceļveži
Papildu palīdzībai lietojumprogrammā ir pieejami uzdevumu ceļveži. Lai piekļūtu uzdevumu ceļvežiem, jebkurā lapā noklikšķiniet uz pogas Palīdzība.

#### <a name="videos"></a>Videoklipi

Apskatiet video pamācības, kas tagad ir pieejamas [Microsoft Dynamics 365 YouTube kanālā](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).







