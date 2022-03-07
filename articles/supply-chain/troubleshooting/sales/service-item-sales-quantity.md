---
title: Nevar iestatīt pakalpojumu krājumu daudzumu pārdošanas piedāvājuma rindā
description: Strādājot ar pārdošanas piedāvājumiem, nevar iestatīt pārdošanas daudzumu precēm, kas ir pakalpojumu krājumi, jo nav neviena fiziska krājuma, ko skaitīt.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477025"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Nevar izmainīt pakalpojumu krājuma pārdošanas daudzumu pārdošanas piedāvājuma rindā

## <a name="symptoms"></a>Simptomi

Mēģinot iestatīt pārdošanas daudzumu (**SalesQty** lauks) pārdošanas piedāvājuma rindas krājuma tipam *Pakalpojums*, tiks parādīts šāds ziņojums:

> Laukam Daudzums nav atļauts veikt atjaunināšanu.

## <a name="cause"></a>Iemesls

Tas tiek darīts ar nolūku. Pārdošanas daudzumu nevar iestatīt precēm, kas ir pakalpojumu krājumi. Piemēram, ja piedāvājat krājuma instalēšanas pakalpojumu, nav jēgas ierakstīt daudzumu, jo nav fiziska krājuma, ko skaitīt. Ir tikai pakalpojums.
