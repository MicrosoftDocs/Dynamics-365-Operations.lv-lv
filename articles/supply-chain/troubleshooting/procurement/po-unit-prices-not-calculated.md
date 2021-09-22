---
title: Vienību cenas pirkumu pasūtījumos netiek aprēķinātas, balstoties vienību pārveidošanas definīcijās
description: Vienību cenas pirkumu pasūtījumos netiek aprēķinātas, balstoties vienību pārveidošanas definīcijās
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476979"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Vienību cenas pirkumu pasūtījumos netiek aprēķinātas, balstoties vienību pārveidošanas definīcijās

## <a name="symptoms"></a>Simptomi

Mainot vienību pirkšanas pasūtījumā, tirdzniecības līguma cenas netiek pārrēķinātas atbilstoši vienības pārveidošanas definīcijām.

## <a name="cause"></a>Iemesls

Cenas vienmēr tiek iegūtas no tirdzniecības līgumiem (vai citiem cenas iestatījumiem sistēmā, piemēram, pārdošanas līgumiem vai krājuma cenām), un tās tiek noteiktas vienībai.

Ja pasūtījuma rindā ir mainīta vienība, sistēma meklē jaunās vienības cenu un to piemēro. Ja vienības cena netiek atrasta, sistēma cenu nepiemēro. Vienības pārveidošanu nevar izmantot, lai pārrēķinātu cenu citā vienībā. Teorētiski desmit kastes par vienas kastes cenu var nebūt vienāds ar vienas kastes desmitkārtīgu cenu.

## <a name="workaround"></a>Kļūdas apiešanas risinājums

Viens no veidiem, kā atrisināt šo problēmu, ir pārliecināties, vai tiks izmantoti tirdzniecības līgumi vienībām, kuras, iespējams, tiks izmantotas krājuma pasūtījuma rindās.
