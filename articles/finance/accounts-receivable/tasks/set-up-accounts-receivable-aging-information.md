---
title: Debitoru vecumstruktūras informācijas iestatīšana un ģenerēšana
description: Šis ceļvedis jums palīdzēs iestatīt vecumstruktūras perioda definīciju, novecot debitoru bilances un skatīt bilances sarakstā Vecas bilances un lapā Iekasēšanas.
author: abruer
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b67c33f73a33721167cedde1a8d83a81aa77db3
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735407"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Debitoru vecumstruktūras informācijas iestatīšana un ģenerēšana

[!include [banner](../../includes/banner.md)]

Šī rokasgrāmata palīdzēs iestatīt vecumstruktūras perioda definīciju, debitora vecuma bilances un skatīt **bilances** **bilanču sarakstā Vecuma bilance un Iekasēšanas** lapa. Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.


## <a name="create-an-aging-period-definition"></a>Izveidot vecumstruktūras perioda definīciju
1. Dodieties uz **Navigācijas rūts > Moduļi > Kredīts un iekasēšana > Iestatīšana > Vecumstruktūras perioda definīcijas**.
2. Klikšķiniet **Jauns**.
3. Laukā **Vecumstruktūras perioda definīcija** ierakstiet kādu vērtību.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Noklikšķiniet uz **Pievienot zemāk**, lai ievietotu jaunu vecumstruktūras periodu.
6. Laukā **Periods** ievadiet aprakstu, ko rādīt vecumstruktūras atskaitēs.
7. Laukā **Vienība** ievadiet kādu skaitli.
8. Laukā **Intervāls** atlasiet kādu opciju. Virsgrāmatas periods saskaņo periodu ar jūsu virsgrāmatas kalendāru. Diena, nedēļa, mēnesis, ceturksnis un gadi definē intervāla lielumu pēc datuma tipa. Ar vērtību Neierobežots tiek atlasītas visas transakcijas pirms vai pēc iepriekšējā perioda, atkarībā no tā, vai tas ir pirmais vai pēdējais periods.  
9. Laukā **Vecumstruktūras indikators** atlasiet kādu opciju.
10. Atlasiet periodu režģa augšpusē. Atjaunināt aprakstu, lai aprakstītu visvecāko periodu vecumstruktūras perioda definīcijā
11. Laukā **Periods** ievadiet jaunu vecumstruktūras perioda aprakstu.
12. Aizvērt lapu.

## <a name="age-the-balances"></a>Novecot bilances
1. Pārejiet uz sadaļu **Kredīts un iekasēšana > Periodiskie uzdevumi > Vecas debitoru bilances**.
2. Laukā **Vecumstruktūras perioda definīcija** atlasiet savu izveidoto vecumstruktūras perioda definīciju.
    + Katrai vecumstruktūras perioda definīcijai jums var būt viens aktīvs momentuzņēmums.  
    + Visi debitori tiek apstrādāti pēc noklusējuma. Šo atlasi varat izmantot, lai aprēķinātu vienu debitoru iekasēšanas pūlu.  
    + Atlasiet datumu no transakcijas, kas tiks izmantots vecumstruktūrai.  
    + Vecumstruktūrai atlasiet datumu “kopš”. Noklusējuma vērtība ir šodiena, bet, ja šo lauku maināt uz Atlasītais datums, varēsiet izvēlēties nepieciešamo datumu. Pakešapstrādei lietojiet Šodienas datums.  
3. Izvērsiet diapazonu **Uzņēmums**. Varat atlasīt uzņēmumus, kas tiks iekļauti momentuzņēmumā. Pašreizējais uzņēmums tiek atlasīts pēc noklusējuma.
4. Noklikšķiniet uz **Labi**, lai apstrādātu šo momentuzņēmumu. Tas aizņems kādu laiku, tāpēc pagaidiet, līdz slīdnis izzūd, un pārbaudiet, vai ziņojumu centrā ir kāds ziņojums.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Skatīt bilances sarakstā Vecas bilances un lapā Iekasēšana
1. Pārejiet uz sadaļu **Kredīts un iekasēšana > Iekasēšana > Vecas bilances**. Saraksta lapā tiek rādītas bilances šim debitoram. Vecumstruktūras ikona rāda vecumstruktūras periodu vecākajai transakcijai.  
2. Atlasiet debitoru ar bilanci.
3. Izvērsiet apgabala lodziņu **Vecumstruktūras fakts**, lai skatītu vecās bilances. Vecumstruktūras perioda definīcija šai papildinformācijai tiek ņemta no parametros norādītās noklusējuma vecumstruktūras perioda definīcijas. Varat to mainīt, izmantojot izvēlni Iekasēt.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
