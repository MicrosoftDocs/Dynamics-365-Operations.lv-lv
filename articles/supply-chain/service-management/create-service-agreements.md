---
title: Pakalpojumu līgumu izveide
description: Šajā tēmā ir aprakstīts, kā lietot līdzekļus moduļos Pakalpojumu pārvaldība un Projektu pārvaldība un uzskaite, lai izveidotu pakalpojumu līgumus.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f883d5b312c042a995e30998fc24da5b1c02f22a
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470861"
---
# <a name="create-service-agreements"></a>Pakalpojumu līgumu izveide

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā lietot līdzekļus moduļos Pakalpojumu pārvaldība un Projektu pārvaldība un uzskaite, lai izveidotu pakalpojumu līgumus.

## <a name="create-a-service-agreement-from-service-management"></a>Izveidot pakalpojumu līgumu no pakalpojumu pārvaldības

1. Pārejiet uz **Pakalpojumu vadība**.
2. Noklikšķiniet uz **Pakalpojumu līgumi**, lai izveidotu jaunu pakalpojumu līguma rindu lapas galvenē. 
3. Atlasiet **Jauns**. Ievadiet aprakstu, atlasiet atsauci uz projektu laukā **Projekta ID** un aizpildiet atlikušos laukus un rindas pakalpojumu līgumam. Atlasiet **Saglabāt**.
4. Cilnē **Relācijas** atlasiet **Pakalpojumu objekti** vai **Pakalpojumu uzdevumi**, lai izveidotu pakalpojumu objektu relācijas vai pakalpojumu uzdevumu relācijas pakalpojumu līgumam. Pakalpojuma objekti un uzdevumi ar izveidotām saistībām var tikt pievienoti pakalpojumu līguma rindām.
5. Lapas apakšējā pusē izveidojiet pakalpojumu līguma rindas nokopējot rindas no pakalpojuma veidnes vai arī pašrocīgi izveidojot pakalpojumu līguma rindas.

> [!NOTE]
> Ja pakalpojumu līgumā rindas tiek iekopētas no cita pakalpojumu līguma, ir iespējams norādīt vai vēlaties kopēt arī pakalpojuma objekta un pakalpojuma uzdevumu relācijas. Ja šīs saistības tiek kopētas, tās tiek pievienotas esošajām saistībām pakalpojumu līgumā. Ja pakalpojumu līguma rindas tiek kopētas no pakalpojuma veidnes, tad pakalpojuma objekta un pakalpojumu uzdevuma saistības tiek automātiski pārkopētas kā pakalpojumu objekta saistības un pakalpojumu uzdevuma saistības jaunā pakalpojumu līguma rindās.

## <a name="create-service-agreement-lines-manually"></a>Pakalpojuma līguma rindu manuāla izveide

1. Lapā **Pakalpojumu līgumi** rindu režģī pievienojiet pakalpojumu līguma rindu. 
2. Ievadiet attiecīgu informāciju par pakalpojumu līgumu rindu. 
3. Atlasiet **Saglabāt**, lai saglabātu rindu, tad aizveriet lapu.

## <a name="create-a-service-agreement-from-project"></a>Pakalpojumu līguma izveide no formas Projekts

1. Atlasiet **Projektu pārvaldība un uzskaite**.
2. Atlasiet **Visi projekti**.
3. Atlasiet projektu no saraksta.
4. **Darbību rūtī** atlasiet **Pārvaldīt**. Darbību grupā **Jauns** atlasiet **Pakalpojums** un atlasiet **Pakalpojuma līgums**.
5. Lai ievadītu projekta atsauci, izpildiet sadaļā **Pakalpojumu līguma izveidošana** sniegtos norādījumus, kā tika aprakstīts iepriekš šajā tēmā.


## <a name="related-topics"></a>Saistītās tēmas

[Izstrādes un veidošanas pakalpojumu līgumu pārskats](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]