---
title: Zvanu centra pasūtījumu izveide
description: Šajā procedūrā parādīts, kā meklēt debitoru, izveidot jaunu pasūtījumu, meklēt preci un iekasēt maksājumu no debitora.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c875eaa85d9da997b75b296ad9ace99ae1e91798
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594240"
---
# <a name="create-call-center-orders"></a>Zvanu centra pasūtījumu izveide

[!include [banner](../includes/banner.md)]

Šajā procedūrā parādīts, kā meklēt debitoru, izveidot jaunu pasūtījumu, meklēt preci un iekasēt maksājumu no debitora. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati, un to paredzēts izmantot darbiniekam, kurš izstrādā pārdošanas pasūtījumu. Priekšnosacījumi: lietotājs, kas izpilda procedūru, ir iestatīts kā zvanu centra lietotājs, un Fabrikam pusgada katalogs ir publicēts ar vismaz vienu avota kodu.

1. Dodieties uz **Mazumtirdzniecība un komercija \> Debitori \> Debitoru apkalpošana**.
2. Laukā **SearchText** ievadiet meklēšanas kritērijus, lai atrastu debitoru.
    * Lai veiktu šo procedūru, ierakstiet “Karen” un atlasiet **Cilne**.  
3. Atlasiet Meklēt.
    * Demonstrācijas datos ir tikai viens debitors ar nosaukumu "Karen", tādēļ rezultāts tiks automātiski atlasīts.  
4. Atlasiet vienumu **Jauns pārdošanas pasūtījums**.
5. Izvērsiet vai sakļaujiet sadaļas **Pārdošanas pasūtījums** galveni.
6. Atlasiet kataloga avota kodu.
    * Ja nav aktīvu avota kodu, varat izlaist šo darbību.  
7. Atlasiet **Pievienot rindu**.
8. Laukā **Krājuma numurs**  ievadiet ar krājumu saistīto meklējamo terminu.
    * Lai veiktu šo procedūru, ievadiet daļēju krājuma numuru “8111” un nospiediet tabulēšanas taustiņu. Šī darbība parādīs krājuma meklēšanas logu.  
9. Atlasiet preci, ko pievienot pārdošanas pasūtījumam.
10. Ievadiet pārdodamo daudzumu.
11. Atlasiet **Izveidot**.
12. Atlasiet **Pabeigt**, lai iekasētu no debitora maksājumu.
13. Atlasiet **Pievienot**.
    * Sadaļa Pievienot saiti ir pieejama cilnē Maksājumi. Izvērsiet cilni Maksājumi, ja tā ir sakļauta.  
14. Atlasiet maksāšanas metodi.
    * Lai veiktu šo procedūru, atlasiet skaidras naudas maksāšanas metodi.  
15. Aizvērt lapu.
16. Ievadiet summu.
    * Lai veiktu šo procedūru, ievadiet summu, kas ir vienāda ar pasūtījuma bilanci, kuru var redzēt lapā Pārdošanas pasūtījumu kopsavilkums pa kreisi no summas lauka. Šī darbība ļaus izpildīt pasūtījumu kā pilnībā apmaksātu.  
17. Atlasiet **Labi**.
18. Atlasiet **Iesniegt**.

## <a name="additional-resources"></a>Papildu resursi

[Darījumu e-pasta ziņojumu pielāgošana pēc piegādes veida](../customize-email-delivery-mode.md)

[Piegādes veida mainīšana programmā POS](../pos-change-delivery-mode.md)

