---
title: Norādīt starpkursu
description: Šajā tēmā ir sniegta informācija par starpkursiem programmā Microsoft Dynamics 365 for Finance and Operations.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9c2cba3ed655e2b4b1ada75bdbb5f01c300b25a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834539"
---
# <a name="specify-the-cross-rate"></a>Norādīt starpkursu

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots starpkursa nolūks un tas, kā norādīt starpkursu, ja sedzat maksājumu ar rēķinu. Izmantojiet starpkursu, kad ir spēkā visi šie kritēriji: 
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
