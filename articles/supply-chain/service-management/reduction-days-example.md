---
title: Piemērs dienu skaita samazināšanai
description: Piemērs dienu skaita samazināšanai.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e588273244c88ffa208e88b66800dc7ce20d68
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674818"
---
# <a name="reduction-days-example"></a>Piemērs dienu skaita samazināšanai

[!include [banner](../includes/banner.md)]

Jūs esat izveidojis abonementa darījumu klienta uzturēšanas abonementam, kā aprakstīts šajā tabulā.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
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
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
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