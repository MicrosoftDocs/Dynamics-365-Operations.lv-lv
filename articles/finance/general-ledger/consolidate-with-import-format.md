---
title: Formāta importēšana konsolidēšanai
description: Šajā tēmā sniegta detalizēta informācija par importa formātu, kas tiek izmantots, konsolidējot finanšu datus no vairākām juridiskām personām.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 5bea69d72ac93d29ae67dd6d762e1376d9a282f0
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735788"
---
# <a name="import-format-for-consolidation"></a>Formāta importēšana konsolidēšanai

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegta detalizēta informācija par importa formātu, kas tiek izmantots, konsolidējot finanšu datus no vairākām juridiskām personām. Importa formāts ir jāsaglabā kā teksta (.txt) fails.

## <a name="import-format"></a>Importa formāts

Šajā tabulā uzskaitīts importa formāts, kas importa laikā jāizmanto, veicot konsolidāciju.

| Ierakstu tabula | Formāts | Piezīmes |
|--------------|---------|-------|
| 1            | 170150, Goodwill, 4 | <ul><li>Ieraksta tabula</li><li>Avota galvenā konta ID</li><li>Galvenā konta rinda</li><li>Galvenā konta tips</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Galvenā konta ID</li><li>Darījuma datums</li><li>Finanšu perioda tips (**0** = atvēršana, **1** = darbībā un **2** = slēgšana)</li><li>Transakcijas valūta</li><li>Debets vai kredīts (**0** = debets un **1** = kredīts)</li><li>Grāmatošanas līmenis</li><li>Darbības summas</li><li>Daudzums</li><li>Vietējais RecID (nenoteikta, unikāla int64 vērtība darbībai)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>Ieraksta numurs (budžeta virsraksta darbības numurs)</li><li>Budžeta virsraksta noklusējuma datums</li><li>Budžeta modeļa ID</li><li>Budžeta veids (**1** – Sākotnējais budžets, **2** – Pārskaitījums, **3** – Pārskatījums, **4** – Apgrūtinājums, **5** – Iepriekšējs apgrūtinājums, **6** – Pārnestais budžets, **7** – Projekts, **8** – Pamatlīdzeklis, **9** – Pieprasījuma apjoma prognoze, **10** – Piegādes apjoma prognoze, **11** – Norīkojumi, **12** – Provizoriskais budžets.)</li><li>Rindas datums</li><li>Rindas galvenā konta ID</li><li>Rindas valūtas kods</li><li>Rindas summa darbības valūtā</li><li>Vesela skaitļa vērtība budžeta veida rindai (izdevumi vai ieņēmumi)</li></ul> |
| 4            | DEMF | RecordCompany ir avota juridiskā persona. |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Galvenā konta ID</li><li>Darījuma datums</li><li>Finanšu perioda tips (0 atvēršana, 1 darbībā, 2 slēgšana)</li><li>Darbības valūta</li><li>Debets vai kredīts (0 debets , 1 kredīts)</li><li>Grāmatošanas līmenis</li><li>Transakciju summa</li><li>Daudzums</li><li>Vietējais RecID (nenoteikta, unikāla int64 vērtība darbībai)</li></ul>  |
| 6            | BusinessUnit, 1 Nodaļa, 2 | Finanšu dimensijas atribūti, kas ir definēti segmenta secībā.<p>Varat izmantot **Eksporta** lapu, lai pārbaudītu, kā atribūti ir definēti.</p> |
| 7            | 002,1,658 | <ul><li>Finanšu dimensijas vērtība</li><li>Finanšu dimensija kā indekss, kas norādīts RecordDimensions</li><li>Nenoteikts, unikāls ieraksta ID, kas ir saistīts ar unikālo ieraksta ID no RecordTrans vai RecordTrans2</li></ul> |
| 8            | 002,1,1 | <ul><li>Dimensijas vērtības, kas ir saistītas ar darījumu no RecordBudget</li><li>Finanšu dimensija kā indekss, kas norādīts RecordDimensions</li><li>Nenoteikts rindas ieraksta ID, kas ir saskaņots ar darījumu rindu secību failā</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
