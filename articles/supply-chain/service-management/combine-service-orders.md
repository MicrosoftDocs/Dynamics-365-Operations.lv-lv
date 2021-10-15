---
title: Kombinēt pakalpojumu pasūtījumus
description: Varat kombinēt pakalpojuma pasūtījumus.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5df9571cb1330489651a28462b747cacd7ac7e46
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580460"
---
# <a name="combine-service-orders"></a>Kombinēt pakalpojumu pasūtījumus   

[!include [banner](../includes/banner.md)]


Kad veidojat pakalpojuma pasūtījuma rindas automātiski veidlapā **Pakalpojumu līgumi**, var izvēlēties vienu no šīm opcijām, lai norādītu, kā grupēt tās.

  - **Pa pakalpojumu līgumiem**

  - **Pa pakalpojumu uzdevumiem**

  - **Pa darbiniekiem**

  - **Pa pakalpojumu objektiem**

## <a name="example"></a>Paraugs

Jūs izveidojat pakalpojuma līgumu, kam ir sākuma datums 03.31.2007. Laukā **Kombinēt pakalpojumu pasūtījumus** atlasiet **Pēc pakalpojuma objekta**. Pēc tam izveidojat šādas pakalpojumu līguma rindas:

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Līguma rindas numurs</p></th>
<th><p>Darbības veids</p></th>
<th><p>apraksts</p></th>
<th><p>Intervāls</p></th>
<th><p>Pakalpojumu objekts</p></th>
<th><p>Pieņemšanas datums</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Stundas</strong></p></td>
<td><p>SAL1</p></td>
<td><p>Katru nedēļu</p></td>
<td><p>X-1</p></td>
<td><p>04.01.2007.</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Stundas</strong></p></td>
<td><p>SAL2</p></td>
<td><p>Katru otro nedēļu</p></td>
<td><p>X-2</p></td>
<td><p>04.01.2007.</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Stundas</strong></p></td>
<td><p>SAL3</p></td>
<td><p>Katru nedēļu</p></td>
<td><p>X-2</p></td>
<td><p>04.01.2007.</p></td>
</tr>
</tbody>
</table>


Laika logu nenorāda nevienai pakalpojumu līguma rindai. Tādēļ pakalpojuma pasūtījuma rindas netiks pārvietotas no aprēķinātā datuma, kurā tās ievietotas.

Pēc tam izveidojiet pakalpojuma pasūtījumu rindas no veidlapas **Pakalpojuma pasūtījumu izveide** no 01.04.2007. līdz 30.04.2007.

Kopā tiek izveidoti 10 pakalpojuma pasūtījumi. Tā kā atlasījāt kombinēto iestatījumu **Pēc pakalpojuma objekta**, visiem izveidotajiem pakalpojuma pasūtījumiem ir tikai pakalpojuma pasūtījuma rindas ar vienu noteiktu pakalpojuma objektu. Pakalpojuma pasūtījuma rindas, kas izveidotas no viena pakalpojumu līguma un kurām ir viens pakalpojuma datums un objekts, tiek kombinētas vienā pakalpojuma pasūtījumā.


> [!NOTE]
> <P>Šajā piemērā veidlapā <STRONG>Pakalpojumu līgumu parametri</STRONG> norādītajā kalendārā nav slēgtu dienu.</P>



Papildu pakalpojumu pasūtījumu rindu grupēšana pakalpojumu pasūtījumos notiek saskaņā ar jebkuru laika logu, ko nosakāt pakalpojuma līguma rindās.

## <a name="see-also"></a>Skatiet arī

[Automātiska pakalpojuma pasūtījumu izveide](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]