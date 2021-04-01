---
title: Atbilstības izveide un apstrāde
description: Šajā tēmā ir paskaidrots, kā veikt neatbilstības pārvaldību, balstoties uz esošu kvalitātes pasūtījumu.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef9c3a06aed1d26e7f5648427178a5638027ec04
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218685"
---
# <a name="create-and-process-a-conformance"></a>Atbilstības izveide un apstrāde

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā veikt neatbilstības pārvaldību, balstoties uz esošu kvalitātes pasūtījumu. Šo ierakstu var palaist USMF demonstrācijas uzņēmumā un var izmantot ieteiktās vērtības. Parasti šo procedūru veic kvalitātes darbinieks.  Vispirms jums jāizpilda prasības tēmā [Preču kvalitātes inspekcija](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) Lai apstrādātu neatbilstības apstiprinājumu, lietotājam, kurš palaiž uzdevumu ierakstu, lapā Lietotāji jābūt piešķirtai vērtībai "Nosaukums". Lai lietotu dokumentu piezīmes, lietotājam jābūt aktivizētai Dokumentu apstrāde lietotāja opcijās.


## <a name="select-a-quality-order"></a>Atlasiet kvalitātes pārbaudes pasūtījumu.
1. Navigācijas rūtī dodieties uz **Moduļi > Krājumu vadība > Periodiskie uzdevumi > Kvalitātes vadība > Kvalitātes pārbaudes pasūtījumi**.
2. Sarakstā atlasiet kvalitātes pasūtījumu, kas tika izveidots tēmā [Preču kvalitātes inspekcija](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).  

## <a name="create-a-nonconformance"></a>Neatbilstības izveide
1. Darbību rūtī atlasiet **Pieprasījumi**.
2. Atlasiet **Neatbilstības**.
3. Atlasiet **Jauns**.
4. Lauka **Problēmas veids** nolaižamajā izvēlnē atlasiet problēmu, kas tika atrasta inspekcijā.  
5. Atlasiet **Labi**.

## <a name="approvereject-a-nonconformance"></a>Neatbilstības apstiprināšana/noraidīšana
1. Atlasiet **Funkcijas**.
2. Atlasiet **Apstiprināt neatbilstību**. Šim piemēram apstipriniet neatbilstību. Apstiprinātas neatbilstības var saistīt ar saistītām darbībām, lai reģistrētu darbu, kas veikts kā daļa no neatbilstības apstrādes un, kā šajā tēmā aprakstīts, labojošo darbību apstrādi.  
3. Atlasiet **Jā**.

## <a name="create-a-correction-action"></a>Labojuma darbības izveide
1. Atlasiet **Labojumi**.
2. Atlasiet **Jauns**.
3. Jaunās rindas laukā **Personāla numura** atlasiet vēlamo ierakstu nolaižamajā izvēlnē.
4. Noklikšķiniet uz **Atlasīt**.
5. Atlasiet **Pievienot**. Izveidojiet piezīmi par šo labojumu. Šajā piemērā darbība ir sazināties ar kreditoru, lai apspriestu neatbilstības gadījumu.  
6. Atlasiet **Jauns**.
7. Atlasiet **Piezīme**. Atkarībā no pārskata iestatījumiem iestatījumiem, kas saistīti ar neatbilstību pārvaldību, var izdrukāt dažādus dokumentu veidus.  
8. Laukā **Apraksts** ierakstiet kādu vērtību.
9. Aizvērt lapu.

## <a name="maintain-a-correction"></a>Labojuma uzturēšana
1. Atlasiet **Atzīmēt kā pabeigtu**.
2. Atlasiet **Labi**.
3. Aizvērt lapu.

## <a name="close-a-nonconformance"></a>Neatbilstības aizvēršana
1. Atlasiet **Funkcijas**.
2. Atlasiet **Aizvērt neatbilstību**.
3. Atlasiet **Jā**.
4. Aizveriet lapas.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]