---
title: Vairāku pasūtījumu operāciju laikā sistēma nevar atrast plānotu pasūtījumu
description: Kļūda "Plānotais pasūtījums nepastāv", kad veicat operācijas vairākiem plānotiem pasūtījumiem un vismaz divi pasūtījumi pieder vienam krājuma ID.
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920856"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>Vairāku pasūtījumu operāciju laikā sistēma nevar atrast plānotu pasūtījumu

Kļūdas kods: SYS24774

## <a name="symptoms"></a>Simptomi

Mēģinot veikt operāciju vairākiem plānotiem pasūtījumiem vienlaicīgi, tiek parādīts šāds kļūdas ziņojums, un vismaz divi pasūtījumi pieder vienam krājuma ID. Piemēram, kļūda var rasties, kad pasūtījumi ir apstiprināti vai to pasūtījuma tips tiek mainīts.

> Plānotais pasūtījums %1 nepastāv.

## <a name="cause"></a>Iemesls

Kad sistēma atbalsta vai maina pasūtījuma tipu, ir jāņem vērā esošie plānotie krājuma pasūtījumi, lai pārliecinātos, ka plānotā piegāde atbilst pieprasījumam un esošajai piegādei. Kā daļu no šī procesa sistēma atkārtoti izveido plānotos pasūtījumus krājumam. Tādēļ otrais plānotais pasūtījums, ko sistēma plāno apstrādāt, vairs nepastāv.

## <a name="workaround"></a>Kļūdas apiešanas risinājums

Apstipriniet pasūtījumus pirms to apstrādes. Šādā veidā pasūtījumi netiks dzēsti, kad sistēma apstrādā pirmo krājuma pasūtījumu.
