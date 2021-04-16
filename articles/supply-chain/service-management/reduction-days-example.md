---
title: Piemērs dienu skaita samazināšanai
description: Piemērs dienu skaita samazināšanai.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90a2efff0add508ddb3d750bb3ca27ea35bf113a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836066"
---
# <a name="reduction-days-example"></a>Piemērs dienu skaita samazināšanai 

[!include [banner](../includes/banner.md)]


Jūs esat izveidojis abonementa darījumu klienta uzturēšanas abonementam, kā aprakstīts šajā tabulā.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>No datuma</p></th>
<th><p>Līdz datumam</p></th>
<th><p>Abonements</p></th>
<th><p>Abonementa tips</p></th>
<th><p>Project</p></th>
<th><p>Kategorija</p></th>
<th><p>Pārdošanas valūta</p></th>
<th><p>Pārdošanas cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2011. gada 01. marts</p></td>
<td><p>2011. gada 31. marts</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Regulārs</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>


Klients ziņo, ka tam nav nepieciešams pakalpojumu nodrošinājums uz divām dienām (10. marts un 11. marts). Jūs piekrītat samazināt abonementu par šīm divām dienām.

Jūs izveidojat jaunu darbību, kuras tips ir **Dienu skaita samazināšana**, kā aprakstīts šajā tabulā.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>No datuma</p></th>
<th><p>Līdz datumam</p></th>
<th><p>Abonements</p></th>
<th><p>Abonementa tips</p></th>
<th><p>Project</p></th>
<th><p>Kategorija</p></th>
<th><p>Pārdošanas valūta</p></th>
<th><p>Pārdošanas cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2011. gada 10. marts</p></td>
<td><p>2011. gada 11. marts</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Dienu skaita samazināšana</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>


Kad par 2011. gada darbībām tiek sagatavots rēķins, pārdošanas cena EUR 200 tiek samazināta par EUR 12,90. Tādējādi atskaitāmā summa par abonementa darbību ir EUR 187,10, un tiks izsūtīti rēķini par divām darbībām ar kopējo summu EUR 187,10.

## <a name="see-also"></a>Skatiet arī

[Abonementa apmaksas dienu samazināšana](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]