---
title: Gada beigu slēgšanas trūkstošās sākuma bilances
description: Šajā tēmā skaidrots, kādēļ, slēdzot gadu, var būt trūkstošas sākuma bilances, un kā atjaunot šīs bilances, ja tās iztrūkst.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 582363ba6c5f6e63e695d41e73ee2f0b382cf26e
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727177"
---
# <a name="year-end-close-missing-opening-balances"></a>Gada beigu slēgšanas trūkstošās sākuma bilances

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kādēļ, slēdzot gadu, var būt trūkstošas sākuma bilances, un kā atjaunot šīs bilances, ja tās iztrūkst.

### <a name="symptom"></a>Simptoms

Kādēļ pēc virsgrāmatas gada beigu slēgšanas nav sākuma bilanču? 

### <a name="resolution"></a>Novēršana

Ja virsgrāmatā gads ir slēgts un pēc tam ģenerēta apgrozījuma bilance, kas nerāda sākuma bilances nākamajam finanšu gadam, ir jāveic pārbaudes.

Ja laukā **Atsaukt iepriekšējo slēgšanu** ir norādīta vērtība **Jā**, tiek stornēta iepriekšējā gada beigu slēgšana tam pašam finanšu gadam. Ja tiek izpildīta gada beigu slēgšanas stornēšanas darbība, visi beigu bilances un sākuma bilances ieraksti tiks dzēsti, it kā gads nebūtu ticis slēgts. Arī dokumenti tiks dzēsti. Gada beigu slēgšanas process vairs netiks automātiski atkārtoti izpildīts. Šis process ir jāsāk vēlreiz, šoreiz atjauninot opcijas **Atsaukt iepriekšējo slēgšanu** vērtību uz **Nē**.

Šis scenārijs ir iekļauts gada beigu bieži uzdoto jautājumu tēmā. Papildinformāciju skatiet dokumentā [Bieži uzdotie jautājumi par darbībām gada beigās](faq-year-end-activities.md).

### <a name="symptom"></a>Simptoms

Es izpildīju gada beigu slēgšanu, opcijai **Atsaukt iepriekšējo slēgšanu** norādot vērtību **Nē**, un joprojām nav sākuma bilanču manam finanšu gadam.

### <a name="resolution"></a>Novēršana

Vispirms pārbaudiet pakešuzdevuma statusu. Gada slēgšana ietver vairākus atsevišķus uzdevumus, bet vissvarīgākā darbība ir pakešuzdevums ar uzdevuma aprakstu **Darbība 5.0.0**. Šīs darbības laikā tiek veikta sākuma transakciju grāmatošana un pēc izvēles arī slēgšanas transakciju grāmatošana virsgrāmatā. 

[![Pakešuzdevumu vēstures saraksts.](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

Ja šī darbība ir sekmīgi pabeigta, bet jūs neredzat sākuma bilances lapā **Apgrozījuma bilances vaicājums** (**Virsgrāmata > Vaicājumi un pārskati > Apgrozījuma bilance**), pārskatiet gada beigu slēgšanas pakešuzdevuma rezultātus, lai redzētu, vai bilances atjaunošanas darbība ir sekmīgi pabeigta.

[![Gada beigu slēgšanas pakešuzdevuma rezultāti.](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

Ja šī darbība kāda iemesla dēļ nav izdevusies, sākuma (un pēc izvēles arī slēgšanas) transakcijas, visticamāk, ir sekmīgi iegrāmatotas. Varat pārbaudīt, vai virsgrāmatas darbības ir sekmīgi grāmatotas, izmantojot lapu **Dokumentu transakciju vaicājums** un norādot dokumenta numuru un datumu, kas norādīts noslēgtā gada beigu slēgšanas dialogā (**Virsgrāmata > Vaicājumi un pārskati > Dokumentu transakcijas**).

[![Dokumentu transakciju vaicājums.](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

Ja ir sākuma (un pēc izvēles arī slēgšanas) dokumenti ir klātesoši, gada beigu slēgšana nav jāizpilda vēlreiz. Tā vietā skatiet nākamo sadaļu, lai uzzinātu, kā turpināt darbu.

### <a name="symptom"></a>Simptoms

Gada beigu slēgšanas darbība “Atjaunot bilances” neizdevās — vai vēlreiz jāizpilda viss gada beigu slēgšanas process?

### <a name="resolution"></a>Novēršana

Veicot bilanču atjaunošanas darbību, tiek atjauninātas virsgrāmatas bilances, kas tiek izmantotas, ģenerējot apgrozījuma bilances vaicājumu.  Tā ir pēdējā darbība gada beigu slēgšanas procesā.  Ja šī darbība ir vienīgā nesekmīgā darbība, virsgrāmatas transakcijas ir sekmīgi iegrāmatotas.  Gada beigu slēgšana nav jāizpilda atkārtoti. Varat izpildīt procesu bilanču manuālai atjaunošanai, izmantojot lapu **Finanšu dimensiju kopas** (**Virsgrāmata > Kontu plāns > Dimensijas > Finanšu dimensiju kopas**).

[![Bilanču atjaunošanas poga lapā Finanšu dimensiju kopas.](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

Ja šī darbība prasa ilgāku laiku, ieteicams pārskatīt finanšu dimensiju kopu paraugpraksi, kā aprakstīts dokumentā [Finanšu dimensiju kopu atjaunināšanas paraugprakse](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets). 

