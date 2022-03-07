---
title: Izdotais darbs bloķēts nepabeigta papildināšanas darba dēļ
description: Izdotais darbs varētu būt bloķēts pakārtotā papildināšanas darba dēļ. Pabeidziet papildināšanas darbu un pēc tam apstrādājiet izdoto darbu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477030"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>Izdoto darbu nevar atbloķēt nepabeigta papildināšanas darba dēļ

## <a name="symptoms"></a>Simptomi

Lietojiet kopuma pieprasījuma papildināšanu, izdoto darbu var bloķēt pakārtota papildināšanas darba dēļ. Ja izdošanas vieta ir jāpapildina, lai aizpildītu avota pasūtījuma prasību, sistēma izveidot gan papildinājuma darbu, gan izdoto darbu. Taču tādējādi izdotais darbs tiek bloķēts līdz brīdim, kad ir pabeigts papildināšanas darbs un jūs saņemat šādu kļūdas ziņojumu:

> Darbu %1 nevar atbloķēt, jo tam ir nepabeigts papildināšanas darbs.

## <a name="resolution"></a>Novēršana

Šāda darbība ir apzināta, jo izdošanas vietai nebūs pietiekami daudz krājuma, kamēr netiek pabeigts papildināšanas darbs. Pabeidziet papildināšanas darbu un pēc tam apstrādājiet izdoto darbu.
