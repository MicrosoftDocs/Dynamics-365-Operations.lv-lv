---
title: Izmaksu sadales politikas izveide un piešķiršana izmaksu vadības ierīcei
description: Izmaksu sadales kārtulas tiek izmantotas, lai sadalītu izmaksas, kas ir finansiāli aprēķinātas uz kolektīvo izmaksu centru.
author: kfend
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: CAMCostDistributionRule
ms.openlocfilehash: 23adea279cad3fcf69cc6926d6f8dee485150221
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272404"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Izmaksu sadales politikas izveide un piešķiršana izmaksu vadības ierīcei

[!include [banner](../../includes/banner.md)]

Izmaksu sadales kārtulas tiek izmantotas, lai sadalītu izmaksas, kas ir finansiāli aprēķinātas uz kolektīvo izmaksu centru. Izmaksu grāmatvedis nodrošina, ka izmaksas tiek sadalītas izmaksu centros, pamatojoties uz atlasīto sadalījuma pamatu. Izmaksu vadības ierīcei tiek piešķirta politika un atbilstošas kārtulas. Šis uzdevuma ceļvedis izmanto piemēru, lai parādītu, kā izveidot izmaksu sadales politiku un atbilstošas kārtulas.


## <a name="create-a-policy"></a>Politikas izveide
1. Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu sadales politikas.
2. Noklikšķiniet uz Jauns.
3. Laukā Politikas nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Organizācija.  
6. Laukā Izmaksu elementa dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.
    * Atlasiet CDS P/L.  
7. Laukā Statistiskā dimensija ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Statistiskie elementi.  
8. Noklikšķiniet uz Saglabāt.

## <a name="create-rules-for-the-policy"></a>Politikas kārtulu izveide
1. Noklikšķiniet uz Jauns.
2. Sarakstā atzīmējiet atlasīto rindu.
3. Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Izvērsiet hierarhiju, lai atlasītu 094.  
4. Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Citi saimnieciskās darbības izdevumi un pēc tam atlasiet 605110 Tīrīšana.  
5. Laukā Izmaksu izturēšanās atlasiet opciju.
    * Atlasiet Fiksētās izmaksas.  
6. Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.
7. Noklikšķiniet uz Jauns.
8. Sarakstā atzīmējiet atlasīto rindu.
9. Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Izvērsiet hierarhiju, lai atlasītu 094.  
10. Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Citi saimnieciskās darbības izdevumi un pēc tam atlasiet 605150 Īre.  
11. Laukā Izmaksu izturēšanās atlasiet opciju.
    * Atlasiet Fiksētās izmaksas.  
12. Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.
13. Noklikšķiniet uz Saglabāt.

## <a name="assign-rules-to-a-cost-control-unit"></a>Kārtulu piešķiršana izmaksu vadības ierīcei
1. Noklikšķiniet uz Izmaksu vadības ierīces politikas piešķires.
2. Noklikšķiniet uz Jauns.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Derīgs no uzskaites datuma ievadiet datumu.
    * Atlasiet 1. septembris derīgā finanšu gadā.  
5. Laukā Izmaksu vadības ierīce ievadiet vai atlasiet kādu vērtību.
6. Noklikšķiniet uz Saglabāt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
