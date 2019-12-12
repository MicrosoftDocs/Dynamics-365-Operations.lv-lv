---
title: Izmaksu apkopošanas politikas izveide
description: Šī procedūra parāda, kā izveidot izmaksu apkopošanas politiku un izveidot kārtulas politikai.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: facffeaf8d880bad01877b420197e29b6791ebbf
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187778"
---
# <a name="create-a-cost-rollup-policy"></a>Izmaksu apkopošanas politikas izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra parāda, kā izveidot izmaksu apkopošanas politiku un izveidot kārtulas politikai. Demonstrācijas dati, kas tiek izmantoti, lai izveidotu šo procedūru, ir USP2.


## <a name="create-a-policy"></a>Politikas izveide
1. Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu apkopojuma politikas.
2. Noklikšķiniet uz Jauns.
3. Laukā Politikas nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Izmaksu apkopojums CC.  
6. Laukā Izmaksu elementa dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Izmaksu apkopojums CC.  
7. Noklikšķiniet uz Saglabāt.

## <a name="create-rules-for-the-cost-rollup-policy"></a>Kārtulu izveide izmaksu apkopošanas politikai
1. Noklikšķiniet uz Jauns.
2. Sarakstā atzīmējiet atlasīto rindu.
3. Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Atlasiet 007.  
4. Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Izmaksu apkopojums CE.  
5. Laukā Sekundārais izmaksu elements ievadiet vai atlasiet kādu vērtību.
    * Šim piemēram kartējiet sekundāro izmaksu elementu CC-007 uz izmaksu centru.  
6. Noklikšķiniet uz Jauns.
7. Sarakstā atzīmējiet atlasīto rindu.
8. Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Atlasiet 008.  
9. Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Izmaksu apkopojums CE.  
10. Laukā Sekundārais izmaksu elements ievadiet vai atlasiet kādu vērtību.
    * Šim piemēram kartējiet sekundāro izmaksu elementu CC-008 uz izmaksu centru.  
11. Noklikšķiniet uz Jauns.
12. Sarakstā atzīmējiet atlasīto rindu.
13. Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Atlasiet 009.  
14. Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Izmaksu apkopojums CE.  
15. Laukā Sekundārais izmaksu elements ievadiet vai atlasiet kādu vērtību.
    * Šim piemēram kartējiet sekundāro izmaksu elementu CC-009 uz izmaksu centru.  
    * Turpiniet, līdz visi izmaksu centri tiek kartēti uz to attiecīgajiem sekundārajiem izmaksu elementiem.  
16. Noklikšķiniet uz Saglabāt.
