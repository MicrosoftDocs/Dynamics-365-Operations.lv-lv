---
title: Izmaksu apkopošanas politikas izveide
description: Šī procedūra parāda, kā izveidot izmaksu apkopošanas politiku un izveidot kārtulas politikai.
author: panolte
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfadde13c4bed494f6cd7ef63ed0ed6bf996ac61
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714234"
---
# <a name="create-a-cost-rollup-policy"></a>Izmaksu apkopošanas politikas izveide

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
