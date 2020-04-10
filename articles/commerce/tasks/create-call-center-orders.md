---
title: " Zvanu centra pasūtījumu izveide"
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
ms.openlocfilehash: 4ec10e0f79e4eca7f51ba48c679dcf6fe745eb29
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141434"
---
# <a name="create-call-center-orders"></a> Zvanu centra pasūtījumu izveide

[!include [banner](../includes/banner.md)]

Šajā procedūrā parādīts, kā meklēt debitoru, izveidot jaunu pasūtījumu, meklēt preci un iekasēt maksājumu no debitora. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati, un to paredzēts izmantot darbiniekam, kurš izstrādā pārdošanas pasūtījumu. Priekšnosacījumi: lietotājs, kas izpilda procedūru, ir iestatīts kā zvanu centra lietotājs, un Fabrikam pusgada katalogs ir publicēts ar vismaz vienu avota kodu.

1. Dodieties uz Retail un Commerce > Debitori > Debitoru apkalpošana.
2. Laukā SearchText ievadiet meklēšanas kritērijus, lai atrastu debitoru.
    * Lai veiktu šo procedūru, ierakstiet “karen” un nospiediet tabulēšanas taustiņu.  
3. Noklikšķiniet uz Meklēt.
    * Demonstrācijas datos ir tikai viens debitors ar nosaukumu Karen, tādēļ tas tiks automātiski atlasīts.  
4. Noklikšķiniet uz Jauns pārdošanas pasūtījums.
5. Izvērsiet vai sakļaujiet sadaļas Pārdošanas pasūtījums galveni.
6. Atlasiet kataloga avota kodu.
    * Ja nav aktīvu avota kodu, varat aizvērt lauku Avots un izlaist šo darbību.  
7. Noklikšķiniet uz Pievienot rindu.
8. Laukā Krājuma numurs ievadiet ar krājumu saistīto meklējamo terminu.
    * Lai veiktu šo procedūru, ievadiet daļēju krājuma numuru “8111” un nospiediet tabulēšanas taustiņu. Tas tiks parādīts krājuma meklēšanas logā.  
9. Atlasiet preci, ko pievienot pārdošanas pasūtījumam.
10. Ievadiet pārdodamo daudzumu.
11. Noklikšķiniet uz Izveidot.
12. Noklikšķiniet uz Pabeigt, lai iekasētu no debitora maksājumu.
13. Noklikšķiniet uz Pievienot.
    * Sadaļa Pievienot saiti ir pieejama cilnē Maksājumi. Izvērsiet cilni Maksājumi, ja tā ir sakļauta.  
14. Atlasiet maksāšanas metodi.
    * Lai veiktu šo procedūru, atlasiet skaidras naudas maksāšanas metodi.  
15. Aizvērt lapu.
16. Ievadiet summu.
    * Lai veiktu šo procedūru, ievadiet summu, kas ir vienāda ar pasūtījuma bilanci, ko var redzēt lapā Pārdošanas pasūtījumu kopsavilkums pa kreisi no summas lauka. Tādējādi varēsit izpildīt pasūtījumu kā pilnībā apmaksātu.  
17. Noklikšķiniet uz OK.
18. Klikšķiniet Iesniegt.

