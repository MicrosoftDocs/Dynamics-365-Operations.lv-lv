---
title: Noapaļotas nolietojuma aprēķinu summas
description: Šajā rakstā ir izskaidrots lauks Nolietojuma noapaļošana, kas redzams lapā Grāmatas iestatīšana.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf7cf68c98b14fb6c206c99673168153b32a449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830427"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Noapaļotas nolietojuma aprēķinu summas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots lauks Nolietojuma noapaļošana, kas redzams lapā Grāmatas iestatīšana.

Katrai grāmatai tiek iestatītas noapaļotas nolietojuma summas. Noapaļotās nolietojuma summas tiek izmantotas pamatlīdzekļa nolietojuma profilā, kurā ir norādīts turpmākais pamatlīdzekļa nolietojums un vērtība, kā arī nolietojuma aprēķināšanas piedāvājumos. Ievadiet mazāko nolietojuma summu, kura ir atļauta šai grāmatai. 

Neatkarīgi no iestatītajiem noapaļošanas kritērijiem, nolietojuma summa pēdējā nolietojuma periodā netiek noapaļota. Pēdējā nolietojuma perioda beigās pamatlīdzekļa vērtībai jābūt 0 (nulle) vai jāsasniedz lūžņu vērtība, ja tā tiek izmantota.

### <a name="example"></a>Piemērs

Nolietojums bez noapaļošanas ir aprēķināts par summu 2444,44. Saskaņā ar nākamās tabulas datiem ieteiktās summas atkarībā no iestatītajiem noapaļošanas kritērijiem mainās.

| Noapaļošanas metode | Nolietojuma summa |
|-----------------|---------------------|
| Noapaļoš 0,1    | 2444,40            |
| Noapaļoš 1,00   | 2444,00            |
| Noapaļoš 10,00  | 2440,00            |
| Noapaļoš 100,00 | 2400,00            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]