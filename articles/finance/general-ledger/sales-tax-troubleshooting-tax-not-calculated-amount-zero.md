---
title: Nodoklis nav aprēķināts vai nodokļa summa ir nulle
description: Šajā tēmā ir sniegta traucējummeklēšanas informācija, kas var palīdzēt, kad nodokļa summa ir 0 (nulle) vai nodoklis nav aprēķināts.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 45aa5931b5d958dd32bd165b414957fa7b366d077cef67621221ce19b56b67d8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772807"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>Nodoklis nav aprēķināts vai nodokļa summa ir nulle

[!include [banner](../includes/banner.md)]

Transakcijai, iespējams, ir rindas summa, kas nav 0 (nulle), bet vai nu nodoklis nav aprēķināts, vai aprēķinātā nodokļa summa ir 0. Lai novērstu šo problēmu, ja nepieciešams, veiciet tālāk norādītās darbības.

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>Pārbaudiet, vai transakcija pareizi atlasīja nodokļu kodus

Ja transakcija neatlasa pareizos nodokļu kodus vai neatlasa nodokļu kodus, tai netiks aprēķināti nodokļi. Lai pārbaudītu, vai darbība pareizi atlasa nodokļu kodus, veiciet šādas darbības. 

1. Transakciju rindā kopsavilkuma cilnē **Rindas informācija**, cilnē **Iestatījums** sadaļā **PVN** pārbaudiet, vai pareizās PVN grupas ir atlasītas laukos **Krājumu PVN grupa** un **PVN grupa**. Ja nav atlasītas pareizās nodokļu grupas, atlasiet tās.

    [![Krājumu PVN grupas un PVN grupas lauki.](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. Dodieties uz **Nodokļi** \> **Netiešie nodokļi** \> **Pārdošanas nodoklis** \> **Pārdošanas nodokļa grupas**.
3. Atlasiet atbilstošo PVN grupu un pēc tam kopsavilkuma cilnē **Iestatījumi** atzīmējiet PVN kodu laukā **PVN kods**.

    [![PVN grupu lapa.](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. Dodieties uz **Nodokļi** \> **Netiešie nodokļi** \> **PVN** \> **Krājuma PVN grupas**.
5. Atlasiet atbilstošo krājumu PVN grupu un pēc tam kopsavilkuma cilnē **Iestatījumi** pārbaudiet, vai PVN kods laukā **PVN kods** atbilst PVN grupas PVN kodam.

    [![Krājuma PVN grupu lapa.](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. Ja nodokļu kodi neatbilst, atjauniniet PVN kodu vienai no grupām.

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>Pārbaudiet, vai atlasītie nodokļu kodi nav neapliekajami un tiem ir pareizā nodokļu likmes vērtība

Ja nodokļu kodi ir neapliekami vai arī nodokļa likme ir 0 (nulle), nodokļu aprēķina rezultāts būs 0. Veiciet šīs darbības, lai noteiktu, vai atlasītie nodokļu kodi ir neapliekami un vai tiem tiek piemērota pareizā nodokļu likme.

1. Dodieties uz **Nodokļi** \> **Netiešie nodokļi** \> **Pārdošanas nodoklis** \> **Pārdošanas nodokļa grupas**.
2. Atlasiet atbilstošo PVN grupu un pēc tam kopsavilkuma cilnē **Iestatījumi** pārbaudiet, vai izvēles rūtiņa **Neapliekams** ir notīrīta. Ja tas ir atlasīts, notīriet to.

    [![Neapliekamā izvēles rūtiņa PVN grupu lapā.](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. Dodieties uz **Nodoklis** \> **Netiešie nodokļi** \> **PVN** \> **PVN kodi**.
4. Atlasiet atbilstošo PVN kodu un pēc tam pārbaudiet, ka nodokļa likmes vērtība laukā **Vērtība** nav 0 (nulle). Ja tā ir 0, atjauniniet lauku tā, lai tas būtu iestatīts uz pareizo nodokļa likmi.

    [![Vērtības lauks lapā PVN kodu vērtības.](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>Noteikt, vai nulle ir pareizā nodokļa summa

Dažos scenārijos nodokļa summa 0 (nulle) ir pareiza. Veiciet šīs darbības, lai noteiktu, vai 0 ir pareizā nodokļu summa jūsu transakcijai.

1. Dodieties uz **Virsgrāmata** \> **Virsgrāmatas iestatīšana** \> **Virsgrāmatas parametri**.
2. Cilnē **PVN** laukā **Aprēķina metode** pārbaudiet, vai ir atlasīta **Kopsumma**.

    [![Aprēķina metodes lauks virsgrāmatas parametru lapā.](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. Dodieties uz **Nodoklis** \> **Netiešie nodokļi** \> **PVN** \> **PVN kodi**.
4. Atlasiet atbilstošo PVN kodu, atlasiet **Aprēķins** \> **Robežbāze** un pārbaudiet, vai aprēķina pamatā ir iestatīta **Rēķina bilances neto summa** vai **rēķina kopsumma, iekļaujot citas PVN summas**. Plašāku informāciju skatiet [Rēķina kopsumma, iekļaujot citas PVN summas](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).
5. Ja pareizās vērtības ir iestatītas 2. un 4. darbībā, nosakiet, vai transakcijas kopsumma ir 0 (nulle). Ja kopējā summa ir 0, nodokļa summa 0 ir paredzamais rezultāts. Tā kā nodokļa aprēķins ir balstīts uz rēķina bilances kopsummu un šī summa nav rinda pa rindai, nodokļa summa 0 tiks piešķirta katrai rindai pēc nodokļu aprēķina.

## <a name="determine-whether-customization-exists"></a>Noteikt, vai pielāgojums pastāv

Ja esat pabeidzis iepriekšējās sadaļās norādītās darbības, bet nav atraduši nekādu problēmu, nosakiet, vai pielāgošana eksistē. Ja pielāgošana nepastāv, izveidojiet Microsoft pakalpojuma pieprasījumu turpmākam atbalstam.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
