---
title: Stornēt žurnāla grāmatošanu
description: Šajā tēmā ir aprakstītas iespējas, kas ļauj stornēt dokumentus no dokumentu darbību saraksta vai finanšu žurnāliem.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248589"
---
# <a name="reverse-journal-posting"></a>Stornēt žurnāla grāmatošanu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas iespējas Microsoft Dynamics 365 Finance , kas ļauj stornēt visu žurnālu vai stornēt vienu vai vairākus dokumentus no dokumentu darbību saraksta neatkarīgi no to izcelsmes. 

## <a name="reversing-journals"></a>Stornējot žurnālus

Varat stornēt žurnāla rindas atsevišķi. Ar stornēto žurnāla grāmatošanu, var arī stornēt visu finanšu žurnālu. Stornēt žurnālu: 
- Atvēriet finanšu žurnālu un filtrējiet grāmatotos žurnālus
- Noklikšķiniet uz Stornēt izvēlnes lapas augšdaļā
- Jūs redzēsiet kopējo dokumentu un dokumentu rindu skaitu, kā arī kopējo stornēto rindu daudzumu
- Atlasiet Jā, lai izmantotu esošos darbību datumus, vai Nē, lai ievadītu jaunu datumu. Dažos gadījumos, sākotnējās darbības periods var būt slēgts, un jums vajadzēs ievadīt jaunu darbības datumu stornēšanai.
- Ja jūs atlasījāt Nē, ievadiet darbības datumu stornēšanai. 
- Ievadiet komentārā, ko vēlaties pievienot stornētai darbībai
- Noklikšķināt uz pogas Stornēt.

Darbības tiks stornētās. 

Ja dokumenta rindu skaits pārsniedz 100 rindas, stornēšanas process tiks izpildīts, izmantojot pakešveida apstrādi. Stornēšanas rezultātus var pārskatīt, apskatot komentārus palaistajā pakešuzdevumā. Visas kļūmes tiks atzīmētas pakešuzdevuma vēsturē.

Ja dokumenta rindu skaits ir 100 rindas vai mazāk, stornēšanas process tiks izpildīts nekavējoties. Rezultāti tiks parādīti dialogā, kur var ieraudzīt jebkuru dokumentu, kuru nevar stornēt, un iemeslu, kāpēc to nevarēja stornēt. Noklikšķiniet uz Labi, lai aizvērtu dialogu.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Stornējot dokumentus no dokumentu darbību saraksta. 

Jūs varat arī atsaukt dokumentus no **Dokumentu darbību saraksta** visās apakšgrāmatās. Turklāt vienlaicīgi var stornēt vairāk nekā vienu dokumentu. 

Lai stornētu vienu vai vairākus dokumentus: 
- Noklikšķiniet uz Stornēt izvēlnes lapas augšdaļā
- Jūs redzēsiet kopējo dokumentu un dokumentu rindu skaitu, kā arī kopējo stornēto rindu daudzumu
- Atlasiet Jā, lai izmantotu esošos darbību datumus, vai Nē, lai ievadītu jaunu datumu. Dažos gadījumos, sākotnējās darbības periods var būt slēgts, un jums vajadzēs ievadīt jaunu darbības datumu stornēšanai.
- Ja jūs atlasījāt Nē, ievadiet darbības datumu stornēšanai. 
- Ievadiet komentārā, ko vēlaties pievienot stornētai darbībai
- Noklikšķināt uz pogas Stornēt.

Darbības tiks stornētās. 

Ja dokumenta rindu skaits pārsniedz 100 rindas, stornēšanas process tiks izpildīts, izmantojot pakešveida apstrādi. Stornēšanas rezultātus var pārskatīt, apskatot komentārus palaistajā pakešuzdevumā. Visas kļūmes tiks atzīmētas pakešuzdevuma vēsturē.

Ja dokumenta rindu skaits ir 100 rindas vai mazāk, stornēšanas process tiks izpildīts nekavējoties. Rezultāti tiks parādīti dialogā, kur var ieraudzīt jebkuru dokumentu, kuru nevar stornēt, un iemeslu, kāpēc to nevarēja stornēt. Noklikšķiniet uz Labi, lai aizvērtu dialogu.

