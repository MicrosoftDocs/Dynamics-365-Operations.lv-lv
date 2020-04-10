---
title: Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus
description: Šajā tēmā ir paskaidrots, kā lietotājs, kuram ir piešķirta loma “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs”, var izveidot konfigurācijas nodrošinātāju elektroniskajiem pārskatiem (Electronic reporting — ER).
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5f238a492dbc3f9318b1bd1d3ea5657e92b33fb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142113"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā lietotājs, kuram ir piešķirta loma “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs”, var izveidot konfigurācijas nodrošinātāju elektroniskajiem pārskatiem (Electronic reporting — ER). Katra ER konfigurācija atsauksies uz nodrošinātāju kā konfigurācijas autoru. Šajā piemērā tiek izveidots konfigurēšanas pakalpojuma sniedzējs parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurēšanas pakalpojuma sniedzēji ir kopīgi visiem uzņēmumiem.

## <a name="create-a-provider"></a>Nodrošinātāja izveide
1. Dodieties uz sadaļu **Navigācijas rūts** augšējā kreisajā stūrī un atlasiet **Organizācijas administrēšana.**
2. Dodieties uz **Darbvietas > Elektroniskie pārskati**.
3. Dodieties uz **Saistītās saites > Konfigurācijas nodrošinātāji**.
4. Atlasiet **Jauns**.
    - Nodrošinātāja ierakstam ir unikāls nosaukums un URL. Pārskatiet šīs lapas saturu un izlaidiet šo procedūru, ja “Litware, Inc.” (https://www.litware.com) ieraksts jau pastāv.  
5. Laukā Nosaukums ierakstiet `Litware, Inc.`.
6. Laukā Interneta adrese ierakstiet `https://www.litware.com`.
7. Atlasiet **Saglabāt**.
8. Aizvērt lapu.

## <a name="select-as-an-active-provider"></a>Atlasiet kā aktīvu nodrošinātāju
1. Atlasiet pakalpojumu sniedzēju Litware, Inc.
2. Atlasiet **Iestatīt kā aktīvu**.

![Elektronisko pārskatu darbvietas lapa](../media/GER-Task-ActiveProvider-1.png)
