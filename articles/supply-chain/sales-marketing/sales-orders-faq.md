---
title: Bieži uzdotie jautājumi par pārdošanas pasūtījumiem
description: Šajā lapā ir apskatīti bieži uzdotie jautājumi, kas tiek uzdoti, strādājot ar pārdošanas pasūtījumiem Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cee75b1d740e7cb414c674157dde0146e8faa50
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571621"
---
# <a name="sales-order-faqs"></a>Bieži uzdotie jautājumi par pārdošanas pasūtījumiem

Šajā lapā ir apskatīti bieži uzdotie jautājumi, kas tiek uzdoti, strādājot ar pārdošanas pasūtījumiem Dynamics 365 Supply Chain Management.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Vai var saistīt pirkšanas pasūtījumu ar pārdošanas pasūtījumu, lai izpildītu pieprasījumu?

Pirkšanas pasūtījumu varat izveidot no pārdošanas pasūtījuma. Papildinformāciju skatiet sadaļā [Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Vai var atcelt vai dzēst pārdošanas pasūtījumu vai atgriešanas pasūtījumu?

Varat atcelt tikai tos pārdošanas pasūtījumus un atgriešanas pasūtījumus, kas ir ar statusu *Izveidots*. Papildinformāciju skatiet sadaļā [Atgriešanas pasūtījuma atcelšana](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Vai var atjaunot rēķinā iekļauto pārdošanas pasūtījumu, kas tika dzēsts?

Ja rēķinā iekļautais pārdošanas pasūtījums tika dzēsts kļūdas dēļ, var to atjaunot vai skatīt tā detalizētu informāciju.

Dodieties uz **Debitora konts \> Darbības \> Oriģinālais dokuments \> Skatīt detaļas**. Atrodiet meklēto rēķinu un atlasiet to, lai skatītu tā detalizētu informāciju. Šīs informācija ietver pārdošanas pasūtījuma atsauci. Pārdošanas pasūtījuma informācijai var piekļūt arī no šīs lapas.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Vai var atcelt vai dzēst pārdošanas pasūtījumu vai atgriezto pasūtījumu?

Lai notīrītu nošķirtos pārdošanas pasūtījumu ierakstus, palaidiet periodisko uzdevumu *Pārdošanas pasūtījumu dzēšana*, dodoties uz vienu no šīm vietām:

- Pārdošana un mārketings \> Periodiskie uzdevumi \> Tīrīt \> Dzēst pārdošanas pasūtījumus
- Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Tīrīt \> Dzēst pārdošanas pasūtījumus

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Vai ir iespējams aprēķināt komisijas maksu rēķiniem, kas jau ir iegrāmatoti?

Supply Chain Management pašlaik neatbalsta komisijas maksu aprēķināšanu iegrāmatotajiem rēķiniem.
