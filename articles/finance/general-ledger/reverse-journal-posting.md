---
title: Stornēt žurnāla grāmatošanu
description: Šajā tēmā ir aprakstītas iespējas, kas ļauj stornēt dokumentus no dokumentu darbību saraksta vai finanšu žurnāliem.
author: MikeFalkner
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a4fd7c242fc2d857cb35f8ef8c08567c758b768
ms.sourcegitcommit: b294840b8e12aaa2775dd73b2ba9481ecc3d91d5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463593"
---
# <a name="reverse-journal-posting"></a>Stornēt žurnāla grāmatošanu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas iespējas Microsoft Dynamics 365 Finance, kas ļauj stornēt visu žurnālu vai stornēt vienu vai vairākus dokumentus no dokumentu darbību saraksta neatkarīgi no to izcelsmes. 

Lai varētu izmantot vienu no šajā tēmā aprakstītiem līdzekļiem, tie ir jāieslēdz jūsu sistēmā. Administratori var izmantot **Līdzekļu pārvaldības** darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:
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

Darbības var apgriezt tikai tad, ja tās atbilst biznesa noteikumiem, lai tos stornētu. Kreditoru maksājumus nevar atcelt, izmantojot šajā tēmā aprakstītās iespējas. Kreditoru maksājumi ir jāstornē, izpildot darbības, kas norādītas [Stornēt kreditora maksājumu](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
