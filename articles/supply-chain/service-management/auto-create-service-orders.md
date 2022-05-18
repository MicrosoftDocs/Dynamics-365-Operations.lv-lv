---
title: Automātiski izveidot pakalpojuma pasūtījumus
description: Varat izveidot pakalpojuma pasūtījumus, kas balstīti uz pakalpojumu līgumu, tā darbības periodā.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41f48e2156ea5f57e600cc5dec09a78a91992d60
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675800"
---
# <a name="automatically-create-service-orders"></a>Automātiski izveidot pakalpojuma pasūtījumus 

[!include [banner](../includes/banner.md)]


Varat izveidot pakalpojuma pasūtījumus, kas balstīti uz pakalpojumu līgumu, tā darbības periodā.

Pakalpojumu līgumam ir piesaistīti visi pakalpojuma pasūtījumi, ko izveidojāt no šī pakalpojumu līguma.

Pakalpojuma pasūtījumi tiek izveidoti automātiski no šādiem iestatījumiem:

  - Pakalpojumu līguma rindās iestatītais pakalpojumu līguma intervāls. Pakalpojumu līguma intervāls norāda biežumu, kādā tiek izveidotas pakalpojuma pasūtījuma rindas. Vairāk informācijas skatiet [Pakalpojumu intervāli](service-intervals.md).

  - Periods, ko norādāt, lai noteiktu pakalpojuma periodu laukos **Datums no** un **Datums līdz** veidlapā **Izveidot pakalpojuma pasūtījumus**. Vairāk informācijas skatiet [Automātiska pakalpojuma pasūtījuma izveide](create-service-orders-automatically.md).

  - **Pakalpojuma pasūtījumu kombinēšana** opcija pakalpojumu līguma galvenē. Opcija norāda, vai no pakalpojumu līguma izveidotās pakalpojuma pasūtījuma rindas kombinē pakalpojuma pasūtījumus pēc darbinieka, pakalpojumu uzdevuma, pakalpojumu objekta vai pakalpojumu līguma. Vairāk informācijas skatiet tēmā [Pakalpojuma pasūtījumu kombinēšana](combine-service-orders.md).

  - Pakalpojumu līguma rindas opcija **Laika logs**. Laika logs nosaka, cik tālu pakalpojuma pasūtījuma rinda var pārvietoties attiecībā pret tās aprēķina datumu. Vairāk informācijas skatiet tēmā [Laika logi](time-windows.md).


> [!NOTE]
> <P>Ja pakalpojuma pasūtījumā minētā diena nav atvērta kalendārā, ko atlasījāt veidlapā <STRONG>Pakalpojuma pārvaldības parametri</STRONG>, saņemat paziņojumu, ka radies kalendāra konflikts. Varat droši ignorēt šo paziņojumu, un pakalpojuma pasūtījums tiek izveidots, lai arī šī diena kalendārā ir slēgta.</P>

## <a name="example-1"></a>1. piemērs

Pakalpojumu līgums ilgst no 2012. gada 1. janvāra līdz 2012. gada 31. decembrim. Ja pakalpojuma periods, ko norādāt veidlapā **Pakalpojuma pasūtījumu izveide** ir no 2012. gada 1. novembra līdz 2013. gada 1. februārim, pakalpojuma pasūtījumi tiek veidoti no 2012. gada 1. novembra līdz 2012. gada 31. decembrim.

## <a name="example-2"></a>2. piemērs

Pakalpojumu līgums ilgst no 2012. gada 1. janvāra līdz 2012. gada 31. decembrim. Pakalpojumu līgumam tiek pievienotas divas pakalpojumu līguma rindas. Pirmās pakalpojumu līguma rindas sākuma datums ir 2012. gada 2. janvārī un beigu datums ir 2012. gada 1. marts. Otrās pakalpojumu līguma rindas sākuma datums ir 2012. gada 1. aprīlī un beigu datums ir 2012. gada 31. decembris. Jūs norādāt periodu veidlapā **Pakalpojuma pasūtījumu izveide** no 2012. gada 1. oktobra līdz 2012. gada 31. decembrim. Tāpēc pakalpojuma pasūtījumi tiek ģenerēti tikai otrai līguma rindai, jo pirmās līguma rindas sākuma un beigu datums ir pirms pakalpojuma pasūtījumam jūsu norādītā perioda.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]