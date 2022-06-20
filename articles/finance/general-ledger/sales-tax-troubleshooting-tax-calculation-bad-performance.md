---
title: Nodokļu aprēķina veiktspēja ietekmē darījumus
description: Šajā rakstā ir sniegta traucējummeklēšanas informācija, kas saistīta ar nodokļu aprēķina veiktspēju un tās ietekmi uz darbībām.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3ee0e3a0f8d9c06760776719fbe49e684cb882cf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894911"
---
# <a name="tax-calculation-performance-affects-transactions"></a>Nodokļu aprēķina veiktspēja ietekmē transakcijas

[!include [banner](../includes/banner.md)]

Dažreiz transakciju ietekmē veiktspējas problēmas, kas saistītas ar nodokļu aprēķināšanu. Lai novērstu šo problēmu, ja nepieciešams, veiciet tālāk norādītās darbības.

## <a name="review-the-transaction-line-count"></a>Pārskatītiet transakcijas rindu skaitu

Nosakiet, vai transakcijai ir liels rindu skaits (piemēram, vairāk nekā vairāki simti). Ja tā nav, pārejiet uz nākamo sadaļu. Ja transakcijai ir vairāki simti rindu, aizturiet nodokļu aprēķinu. Papildinformācijai skatiet [Iespējot kavētu nodokļu aprēķinu žurnāliem](enable-delayed-tax-calculation.md). 

Pēc tam varat noteikt, vai ir spēkā kāds no šiem nosacījumiem:

- Pastāv importa transakcijas no lieliem failiem.
- Vairākas sesijas vienlaicīgi apstrādā vienu un to pašu transakciju nodokļu aprēķinu.
- Transakcijai ir vairākas rindas, un skati tiek atjaunināti reāllaikā. Piemēram, lauks **Aprēķinātā PVN summa** lapā **Virsgrāmatas žurnāls** tiek atjaunināts reāllaikā, mainot rindas laukus.

   [![Aprēķinātās PVN summas lauks Žurnāla dokumenta lapā.](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

Ja ir izpildīts kāds no šiem nosacījumiem, nodokļu aprēķins tiek atlikts.

## <a name="review-the-call-stack"></a>Pārskatīt izsaukumu steku

Pārskatīt izsaukumu steku, lai noteiktu, vai nodokļu aprēķins tiek izsaukts vairākas reizes. Ja tas nav, pārejiet uz nākamo sadaļu. Ja izsaukuma steks tiek izsaukts vairākas reizes, rīkojieties šādi, lai palīdzētu samazināt nodokļu aprēķināšanas laikus.

1. Ja žurnāls ir apsvēris transakciju, atlieciet nodokļu aprēķinu. Papildinformācijai skatiet [Iespējot kavētu nodokļu aprēķinu žurnāliem](enable-delayed-tax-calculation.md).
2. Ja transakcija ir pirkšanas pasūtījums un pieteikuma versija ir vēlāka par 10.0.15, nodokļu aprēķinu var atlikt līdz beigu aprēķinam, iespējojot **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** testējamā varianta sniegšanu.

## <a name="review-the-call-stack-timeline"></a>Pārskatīt izsaukumu steku laika skalu

Pārskatiet izsaukumu steka laika skalu, lai noteiktu, vai pastāv šādas problēmas. Ja tā ir, iespējojiet **TaxUncommittedDoIsolateScopeFlighting** testējamā varianta sniegšanu, lai novērstu šo problēmu.

- Transakcijas dēļ sistēma pārstāj reaģēt līdz sesijas beigām. Tādējādi transakcija nevar aprēķināt nodokļu rezultātu. Šajā attēlā parādīts saņemtā ziņojuma lodziņš "Sesija pabeigta".

    [![Ziņojums Sesija pabeigta.](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- Metodes **TaxUncommitted** aizņem vairāk laika nekā citas metodes. Piemēram, šajā ilustrācijā **TaxUncommitted::updateTaxUncommitted()** metode aizņem 43 347,42 sekundes, bet citas metodes aizņem 0,09 sekundes.

    [![Metodes ilgums.](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>Nodokļu aprēķina pielāgošana un izsaukšana

Pielāgojot netiek izsaukts nodokļu aprēķins katras rindas metodē **ievietot()** vai **atjaunināt()**. Nodokļu aprēķins jāizsauc transakciju līmenī.

## <a name="determine-whether-customization-exists"></a>Noteikt, vai pielāgojums pastāv

Ja esat pabeidzis iepriekšējās sadaļās norādītās darbības, bet nav atraduši nekādu problēmu, nosakiet, vai pielāgošana eksistē. Ja pielāgošana nepastāv, izveidojiet Microsoft pakalpojuma pieprasījumu turpmākam atbalstam.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
