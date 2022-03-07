---
title: Zvanu centra pasūtījumu izveide
description: Šajā procedūrā parādīts, kā meklēt debitoru, izveidot jaunu pasūtījumu, meklēt preci un iekasēt maksājumu no debitora.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 78cccabb206d938b850e70b7e8057e20cc6158e1d154fc4876de7918dbe44d87
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730663"
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]