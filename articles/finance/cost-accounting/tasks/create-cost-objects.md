---
title: Izmaksu objektu izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734135"
---
# <a name="create-cost-objects"></a>Izmaksu objektu izveide 

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir aprakstīts, kā izveidot izmaksu objektus, importējot izmaksu centra finanšu dimensijas izmaksu uzskaitē, izmantojot datu savienotāju. Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF. 


## <a name="create-new-cost-objects"></a>Izveidot jaunus izmaksu objektus
1. Pārejiet uz **sadaļu Izmaksu >, kas > izmaksu objektu dimensijām**.
2. Klikšķiniet **Jauns**.
3. Laukā **Nosaukums** ierakstiet kādu vērtību.
4. Datu savienotājā **dimensijas dalībnieku** laukam ievadiet vai atlasiet vērtību.
5. Laukā **Apraksts** ierakstiet kādu vērtību.
6. Noklikšķiniet uz **Saglabāt**.

## <a name="configure-the-data-connector"></a>Konfigurēt datu savienotāju
1. Noklikšķiniet uz **Konfigurēt dimensiju dalībnieku nodrošinātāju**.
    * Atlasiet CostCenter, lai importētu CostCenter dimensijas izmaksu uzskaitē.  
2. Laukā **Dimensijas** nosaukums atlasiet Izmaksu centrs.
3. Noklikšķiniet uz **Labi**.

## <a name="import-cost-centers"></a>Importēt izmaksu centrus
1. Noklikšķiniet uz **Importēt dimensiju dalībniekus**.
2. Noklikšķiniet uz **Labi**.

## <a name="view-the-imported-cost-centers"></a>Skatīt importēto izmaksu centrus
1. Noklikšķiniet uz **Skatīt dimensiju dalībniekus**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
