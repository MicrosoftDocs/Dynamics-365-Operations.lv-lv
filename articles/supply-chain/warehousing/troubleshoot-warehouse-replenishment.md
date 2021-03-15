---
title: Noliktavas papildināšanas problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu papildināšanu programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7748a18d2b6f612b3ac9ac1a75efb6ae5f13859a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993891"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Noliktavas papildināšanas problēmu novēršana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu papildināšanu programmā Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Es saņemu sekojošu brīdinājuma ziņojumu: "Darbu %1 nevar atbloķēt, jo tam ir nepabeigts papildināšanas darbs."

### <a name="issue-description"></a>Problēmas apraksts

Izdošanas darbs ir bloķēts atkarīgā papildināšanas darba dēļ.

### <a name="issue-resolution"></a>Problēmas risinājums

Kad izmantojat kopuma pieprasījuma papildināšanu, ja izdošanas vieta ir jāpapildina, lai izpildītu avota pasūtījuma pieprasījumu, sistēma izveido gan papildināšanas darbu, gan izdošanas darbu. Tomēr tas bloķē izdošanas darbu, līdz papildināšanas darbs ir pabeigts. Šī darbība ir tīša, jo izdošanas vietai nav pietiekami daudz krājumu, ja vien papildināšanas darbs nav pabeigts. Pabeidziet papildināšanas darbu un pēc tam apstrādājiet izdošanas darbu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]