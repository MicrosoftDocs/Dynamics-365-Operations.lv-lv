---
title: Stornēt žurnāla grāmatošanu
description: Šajā tēmā ir aprakstītas iespējas, kas ļauj stornēt dokumentus no dokumentu darbību saraksta vai finanšu žurnāliem.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3244d857a9135249130672501f8b766ff9a0680
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445599"
---
# <a name="reverse-journal-posting"></a>Stornēt žurnāla grāmatošanu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas iespējas Microsoft Dynamics 365 Finance, kas ļauj stornēt visu žurnālu vai stornēt vienu vai vairākus dokumentus no dokumentu darbību saraksta neatkarīgi no to izcelsmes. 

## <a name="reversing-journals"></a>Stornējot žurnālus

Varat stornēt žurnāla rindas atsevišķi. Ar stornēto žurnāla grāmatošanu, var arī stornēt visu finanšu žurnālu. Stornēt žurnālu: 

- Atveriet finanšu žurnālu un filtrējiet grāmatotos žurnālus.
- Atlasiet **Stornēt** izvēlnes lapas augšdaļā.
- Jūs redzēsiet kopējo dokumentu un dokumentu rindu skaitu, kā arī kopējo stornēto rindu daudzumu
- Atlasiet **Jā**, lai izmantotu esošos darbību datumus, vai **Nē**, lai ievadītu jaunu datumu. Dažos gadījumos sākotnējās darbības periods var būt slēgts, un jums vajadzēs ievadīt jaunu darbības datumu stornēšanai.
- Ja jūs atlasījāt **Nē**, ievadiet darbības datumu stornēšanai. 
- Ievadiet komentārā, ko vēlaties pievienot stornētai darbībai.
- Atlasiet pogu **Stornēt**.

Darbības tiks stornētās. 

Ja dokuments pārsniedz 100 rindas, stornēšanas process tiks izpildīts, izmantojot pakešveida apstrādi. Rezultātus varat pārskatīt, apskatot komentārus pakešuzdevumā. Jebkuras darbības, kuras nevarēja atcelt, tiks uzskaitītas pakešuzdevuma vēsturē.

Ja dokuments sastāv no 100 rindām vai mazāk, stornēšanas process tiks izpildīts nekavējoties. Rezultāti tiks parādīti dialoga lodziņā, kur var ieraudzīt jebkuru dokumentu, kuru nevar stornēt, kopā ar iemeslu, kāpēc to nevarēja stornēt. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Stornējot dokumentus no dokumentu darbību saraksta. 

Jūs varat arī atsaukt dokumentus no **Dokumentu darbību saraksta** visās apakšgrāmatās. Turklāt vienlaicīgi var stornēt vairāk nekā vienu dokumentu. 

Lai stornētu vienu vai vairākus dokumentus: 

- Atlasiet **Stornēt** izvēlnes lapas augšdaļā.
- Jūs redzēsiet kopējo dokumentu un dokumentu rindu skaitu, kā arī kopējo stornēto rindu daudzumu.
- Atlasiet **Jā**, lai izmantotu esošos darbību datumus, vai **Nē**, lai ievadītu jaunu datumu. Dažos gadījumos sākotnējās darbības periods var būt slēgts, un jums vajadzēs ievadīt jaunu darbības datumu, lai to stornētu.
- Ja jūs atlasījāt **Nē**, ievadiet darbības datumu stornēšanai. 
- Ievadiet komentāru, lai aprakstītu stornēšanas darbību.
- Atlasiet pogu **Stornēt**.

Darbības tiks stornētās. 

Ja dokuments pārsniedz 100 rindas, stornēšanas process tiks izpildīts, izmantojot pakešveida apstrādi. Rezultātus varat pārskatīt, apskatot komentārus pakešuzdevumā. Jebkuras darbības, kuras nevarēja atcelt, tiks atzīmētas pakešuzdevuma vēsturē.

Ja dokumenta rindu skaits ir 100 rindas vai mazāk, stornēšanas process tiks izpildīts nekavējoties. Rezultāti tiks parādīti dialoga lodziņā, kur var ieraudzīt jebkuru dokumentu, kuru nevar stornēt, kopā ar iemeslu, kāpēc to nevarēja stornēt. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

Darbības var apgriezt tikai tad, ja tās atbilst biznesa noteikumiem, lai tos stornētu. Kreditoru maksājumus nevar atcelt, izmantojot šajā tēmā aprakstītās iespējas. Kreditoru maksājumi ir jāstornē, izpildot darbības, kas norādītas [Stornēt kreditora maksājumu](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).

