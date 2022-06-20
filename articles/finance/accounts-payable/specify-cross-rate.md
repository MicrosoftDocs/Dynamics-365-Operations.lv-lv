---
title: Starpkursa norādīšana
description: Šajā rakstā ir sniegta informācija par krusteniskām likmēm Microsoft Dynamics 365 Finansēs.
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb01948af2bcba9ca740e8bd0e12584cf021fce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889966"
---
# <a name="specify-the-cross-rate"></a>Starpkursa norādīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots starplikmis nolūks un kā norādīt starplikmi, kad kārtojams maksājums ar rēķinu. Lietojiet starplikmi, ja lietojat šādus kritērijus: 
-   Jūs sedzat maksājumu ar rēķinu. 
-   Maksājuma rinda un rēķina rinda izmanto dažādas valūtas. 
-   Neviena no valūtām nav uzskaites valūta. 

Starpkurss netiek izmantots, lai veiktu maksājuma transakcijas valūtas pārrēķināšanu maksājuma uzskaites valūtā. Tā vietā maiņas kursi no maiņas kursu tabulām tiek izgūti, lai aprēķinātu maksājuma transakcijas valūtas summas un maksājuma uzskaites valūtas summas vērtību. 

Piemēram, uzskaites valūta ir USD, rēķina valūta ir CAD, un maksājuma valūta ir EUR. Starpkurss ļauj ievadīt maiņas kursu tieši starp CAD un EUR, neveicot konvertāciju caur USD. Ja izvēlaties rēķinu un primāro maksājumu, varat ievadīt starpkursu rēķina rindai. Starpkurss ir maiņas kurss starp norēķinu datuma transakciju valūtām.

1.  Atveriet kādu no šādām lapām:
- **Debitoru parādi > Vispārīgi > Debitori > Visi debitori** 
- **Parādi kreditoriem > Vispārīgi > Kreditori > Visi kreditori** 
- **Sagāde un avoti > Vispārīgi > Kreditori > Visi kreditori**
2.  Izvēlieties klientu vai kreditoru, kurš atvērs Jūsu nokārtoto transakciju. 
3.  Debitora gadījumā saraksta lapā **Visi debitori** dodieties uz **Apkopot > Nosegt atvērtās darbības**. Kreditora gadījumā saraksta lapā **Visi kreditori** dodieties uz **Rēķins > Nosegt atvērtās darbības**. 
4.  Izvēlieties transakciju, kas ir primārais maksājums, un pēc tam noklikšķiniet uz **Atzīmēt maksājumu**. Tiek atzīmēta izvēles rūtiņa kolonnā **Atzīmēt**, un kolonnā **Primārais maksājums** tiek parādīta informācijas ikona. 
5.  Laukā **Starpkurss** ievadiet norēķina dienā spēkā esošo apmaiņas kursu starp rēķina valūtu un maksājuma valūtu. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
