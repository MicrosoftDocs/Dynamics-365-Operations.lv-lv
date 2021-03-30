---
title: Noapaļotas nolietojuma aprēķinu summas
description: Šajā rakstā ir izskaidrots lauks Nolietojuma noapaļošana, kas redzams lapā Grāmatas iestatīšana.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 378fa9498018f9ca0e99e04d04cbf6a28620e308
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210147"
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