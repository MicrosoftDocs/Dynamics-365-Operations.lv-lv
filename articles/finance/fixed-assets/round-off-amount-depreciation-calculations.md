---
title: Noapaļotas nolietojuma aprēķinu summas
description: Šajā rakstā ir izskaidrots lauks Nolietojuma noapaļošana, kas redzams lapā Grāmatas iestatīšana.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: kfend
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a93842f7cca483df89188695c945edf77e118cef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870109"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Noapaļotas nolietojuma aprēķinu summas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir apskatīts **noapaļošanas nolietojuma lauks**, kas ir atrodams grāmatas **iestatījuma lapās**.

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
