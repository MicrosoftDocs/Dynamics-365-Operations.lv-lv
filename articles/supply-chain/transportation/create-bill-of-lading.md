---
title: Izveidot preču transporta pavadzīmi
description: Šajā tēmā ir aprakstīts, kā izveidot preču transporta pavadzīmi, izmantojot noliktavas vadības procesus.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b001ef8936e7e35db89163683c023211f79b24c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996474"
---
# <a name="create-a-bill-of-lading"></a>Izveidot preču transporta pavadzīmi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot preču transporta pavadzīmi, izmantojot noliktavas vadības procesus.  

Preču transporta pavadzīme ir juridisks dokuments, kas noslēgts starp uzņēmumu, kurš nosūta preces, un pārvadātāju. Dokuments ir pievienots nosūtītajām precēm, un tas kalpo kā sūtījuma saņemšanas apliecinājums, kad preces tiek piegādātas galamērķī. Ja lietojat noliktavas vadību, ir divi veidi, kā izveidot preču transporta pavadzīmi:

  -   Izveidojiet pārskatu manuāli, izmantojot lapu **Preču transporta pavadzīme**.
  -   Ģenerējiet pārskatu no sadaļas **Kravu plānošanas rīks**.

Ja ģenerējat preču transporta pavadzīmi no sadaļas **Kravu plānošanas rīks**, kravas statusam jābūt **Nosūtīts.** Ja kravā ir vairāki sūtījumi, preču transporta pavadzīme tiek izveidota katram sūtījumam. Pēc preču transporta pavadzīmes izveidošanas izmaiņas tai varat veikt lapā **Preču transporta pavadzīme**.

## <a name="master-bill-of-lading"></a>Apvienotā preču transporta pavadzīme
Ja kravā ir vairāki sūtījumi, varat ģenerēt apvienotu preču transporta pavadzīmi. Tai ir tāds pats izkārtojums un informācija kā preču transporta pavadzīmei, bet tā satur apkopotu visu sūtījumu saturu. Ja opcijai **Izveidot apvienoto preču transporta pavadzīmi, ja kravā ir vairāki sūtījumi** ir iestatīts vienums **Jā** lapā **Transportēšanas pārvaldības parametri**, apvienotā preču transporta pavadzīme tiek ģenerēta automātiski, ja tiek izveidota preču transporta pavadzīme no sadaļas **Kravu plānošanas rīks** un ja ir vairāk nekā viens sūtījums. Varat arī skatīt preču transporta pavadzīmju sarakstu, noklikšķinot uz **Saistītā informācija** &gt; **Preču transporta pavadzīme**. Ja veidojat preču transporta pavadzīmes manuāli, varat izveidot pvienotu preču transporta pavadzīmi lapā **Preču transporta pavadzīme**.



