---
title: Nevar atcelt krājumu rezervēšanu pārdošanas pasūtījuma rindā
description: Ja ir atvērts darbs pret pārdošanas rindu un rindā mēģināt atcelt krājumu rezervēšanu, saņemat kļūdas ziņojumu. Pabeidziet vai dzēsiet darbu, lai atbrīvotu rezervēšanu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476993"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>Nevar atcelt krājumu rezervēšanu pārdošanas pasūtījuma rindā

## <a name="symptoms"></a>Simptomi

Ja ir atvērts darbs ar pārdošanas pasūtījuma rindu un jūs mēģināt šajā rindā norezervēt krājumus, tiek parādīts šāds kļūdas ziņojums:

> Nevar noņemt rezervācijas, jo ir izveidots darbs, kuram šīs rezervācijas ir nepieciešamas.

## <a name="resolution"></a>Novēršana

Izpētiet, vai ir atvērts pakošanas grupas darbs, lai atgrieztu krājumu no iepakošanas stacijas uz citu vietu (piemēram, *Baydoor*). Pārskatiet ierakstus lapās **Darba izveides vēstures žurnāls** un **Darba informācija**, lai noteiktu, kas fiziski rezervē krājumus, un pēc tam pabeidziet vai dzēsiet darbu, lai atbrīvotu rezervāciju.
