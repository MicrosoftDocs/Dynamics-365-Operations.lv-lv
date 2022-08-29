---
title: Apgrieztā žurnāla grāmatošana
description: Šajā rakstā ir aprakstītas iespējas, kas ļauj atsaukt dokumentus no dokumentu darbību saraksta vai finanšu žurnāliem.
author: kweekley
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.form: LedgerTransVoucher, LedgerJournalTable
ms.openlocfilehash: 7e3a22f43bcc312fe60b77db2fc3bc94d15950c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284857"
---
# <a name="reverse-journal-posting"></a>Apgrieztā žurnāla grāmatošana

[!include [banner](../includes/banner.md)]

Šis raksts apraksta iespējas Microsoft Dynamics 365 Finanses, kas ļauj atsaukt visu žurnālu vai atgriezt vienu vai vairākus dokumentus no dokumentu darbību saraksta, neatkarīgi no to izcelsmes. 

Pirms varat lietot vienu no šajā rakstā aprakstītajām funkcijām, sistēmā ir jābūt ieslēgtam. Administratori var izmantot **Līdzekļu pārvaldības** darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:
 - Modulis: Virsgrāmata
 - Funkcionalitātes nosaukums: **Masveida apgriešana vairākiem dokumentiem**

## <a name="reversing-journals"></a>Stornējot žurnālus

Varat stornēt žurnāla rindas atsevišķi. Ar stornēto žurnāla grāmatošanu, var arī stornēt visu finanšu žurnālu. Stornēt žurnālu: 

- Filtrēt grāmatotos žurnālus un atvērt žurnālā skatu **Rindas**.
- Atlasiet **Stornēt** izvēlnes lapas augšdaļā.
- Jūs redzēsiet kopējo dokumentu un dokumentu rindu skaitu, kā arī kopējo stornēto rindu daudzumu.
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

- Atlasiet **Stornēt visu žurnāla nolaižamo sarakstu** izvēlnes lapas augšdaļā.
- Kopējo dokumentu un dokumentu rindu skaits tiek paradīts, kā arī kopējo stornēto rindu daudzumu.
- Atlasiet **Jā**, lai izmantotu esošos darbību datumus, vai **Nē**, lai ievadītu jaunu datumu. Dažos gadījumos sākotnējās darbības periods var būt slēgts, un jums vajadzēs ievadīt jaunu darbības datumu, lai to stornētu.
- Ja jūs atlasījāt **Nē**, ievadiet darbības datumu stornēšanai. 
- Ievadiet komentāru, lai aprakstītu stornēšanas darbību.
- Atlasiet pogu **Stornēt**.

Darbības tiks stornētās. 

Ja dokuments pārsniedz 100 rindas, stornēšanas process tiks izpildīts, izmantojot pakešveida apstrādi. Rezultātus varat pārskatīt, apskatot komentārus pakešuzdevumā. Jebkuras darbības, kuras nevarēja atcelt, tiks atzīmētas pakešuzdevuma vēsturē.

Ja dokumenta rindu skaits ir 100 rindas vai mazāk, stornēšanas process tiks izpildīts nekavējoties. Rezultāti tiks parādīti dialoga lodziņā, kur var ieraudzīt jebkuru dokumentu, kuru nevar stornēt, kopā ar iemeslu, kāpēc to nevarēja stornēt. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

Darbības var apgriezt tikai tad, ja tās atbilst biznesa noteikumiem, lai tos stornētu. Kreditoru maksājumus nevar atcelt, izmantojot šajā rakstā aprakstīto iespēju. Kreditoru maksājumi ir jāstornē, izpildot darbības, kas norādītas [Stornēt kreditora maksājumu](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
