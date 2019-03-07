---
title: Abonementu pārdošanas cenas
description: Kad veidojot abonementu, pārdošanas cena tiek atvasināta no pārdošanas cenas iestatījuma, kas bija izveidots formā Pārdošanas cena (abonements).
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2019
ms.locfileid: "352164"
---
# <a name="subscription-sales-prices"></a>Abonementu pārdošanas cenas   

[!include [banner](../includes/banner.md)]


Kad veidojot abonementu, pārdošanas cena tiek atvasināta no pārdošanas cenas iestatījuma, kas bija izveidots formā **Pārdošanas cena (abonements)**.

Formā **Pārdošanas cena (abonements)** varat izveidot pārdošanas cenas konkrētam abonementam vai plašāk izmantojamas pārdošanas cenas. Lai pārdošanas cenu lietotu kādam abonementam, šī abonementa perioda kodam un valūtai ir jābūt identiskiem ar attiecīgās pārdošanas cenas perioda kodu un valūtu.

Ja perioda kods un valūta gan abonementam, gan pārdošanas cenai ir identiski, abonementa pārdošanas cenas tiek atlasītas atkarībā no nākamajā tabulā norādītajām prioritātēm. Tukša šūna tabulā nozīmē tukšu lauku, un atzīme X nozīmē, ka vērtība ir vienāda ar vērtību abonementā, no kura transakcija tiek ģenerēta.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prioritāte</p></th>
<th><p><strong>Kategorija</strong></p></th>
<th><p><strong>Projekta ID</strong></p></th>
<th><p><strong>Abonements</strong></p></th>
<th><p><strong>Pārdošanas valūta</strong></p></th>
<th><p><strong>Perioda kods</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
</tbody>
</table>


Kad tiek izveidota abonēšanas maksa, par abonementa pārdošanas cenu tiek atlasīta pārdošanas cena ar augstāko detalizācijas līmeni (kā norādīts iepriekš redzamajā tabulā).

## <a name="update-and-index-subscription-sales-prices"></a>Abonementu pārdošanas cenu atjaunināšana un indeksēšana

Abonementa pārdošanas cenu var atjaunināt, atjauninot pamatcenu vai indeksu. Atjaunināt var par procentuālu daudzumu vai uz jaunu vērtību.

## <a name="subscription-fee-sales-prices"></a>Abonēšanas maksas pārdošanas cenas

Veidojot abonēšanas maksu, pārdošanas cena ir atkarīga no abonementam iestatītās pārdošanas cenas. Varat izmantot pamatcenu no abonementa cenas iestatījuma vai izveidot indeksētas pārdošanas cenas.

## <a name="example"></a>Piemērs

Jūs jaunam projektam 9030 vēlaties iestatīt abonementa pārdošanas cenas EUR 500 vērtībā. Formā **Pārdošanas cena (abonements)** jūs izveidojat abonementa pārdošanas cenas rindu, kā noradīts nākamajā tabulā.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Derīgs no</p></th>
<th><p>Kategorija</p></th>
<th><p>Projekts</p></th>
<th><p>Abonements</p></th>
<th><p>Perioda kods</p></th>
<th><p>Pārdošanas valūta</p></th>
<th><p>Pārdošanas cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Mēnesis</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Pievērsiet uzmanību, ka lauki **Kategorija** un **Abonements** ir tukši.

Pēc tam jūs izveidojat tālāk norādītos abonementus.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Pakalpojuma abonements</p></th>
<th><p>Projekts</p></th>
<th><p>Abonementu grupa</p></th>
<th><p>Kategorija</p></th>
<th><p>Valūta</p></th>
<th><p>Perioda kods</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat1</p></td>
<td><p>EUR</p></td>
<td><p>Reizi mēnesī</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR</p></td>
<td><p>Reizi mēnesī</p></td>
</tr>
</tbody>
</table>


Tagad jūs izveidojat abonēšanas maksas abiem abonementiem abonementu grupā Sub1:

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu abonementi** \> **Abonementu grupas**.

2.  Formā **Abonementu grupas** noklikšķiniet uz **Funkcija** \> **Izveidot abonēšanas maksu**.

3.  Formā **Izveidot abonēšanas maksu** ievadiet atbilstošo informāciju. Plašāku informāciju skatiet tēmā [Abonēšanas maksu transakciju izveidošana](create-subscription-fee-transactions.md).

Abiem abonementiem tiek izveidotas abonēšanas maksas, kam ir pārdošanas cena 500 EUR, kā parādīts nākamajā tabulā.

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
<th><p>Projekta datums</p></th>
<th><p>Pakalpojuma abonements</p></th>
<th><p>Projekts</p></th>
<th><p>Kategorija</p></th>
<th><p>Sākuma datums</p></th>
<th><p>Beigu datums</p></th>
<th><p>Pārdošanas valūta</p></th>
<th><p>Pārdošanas cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>01-01-2007</p></td>
<td><p>31-03-2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2006</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>01-01-2007</p></td>
<td><p>31-03-2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Vēlāk jūs izlemjat, ka vēlaties norādīt pārdošanas cenas projekta 9030 kategorijai SubCat1. Tāpēc jūs izveidojat jaunu pārdošanas cenu rindu, kuras pārdošanas cena ir 550 EUR projekta 9030 un maksu kategorijas SubCat1 kombinācijai. Tagad projektam 9030 ir divas abonementa pārdošanas cenu rindas, kā parādīts nākamajā tabulā.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Derīgs no</p></th>
<th><p>Kategorija</p></th>
<th><p>Projekts</p></th>
<th><p>Abonements</p></th>
<th><p>Perioda kods</p></th>
<th><p>Valūta</p></th>
<th><p>Pārdošanas cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2007</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Mēnesis</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2007</p></td>
<td><p>SubCat1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>Mēnesis</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>


Jūs atkārtojat iepriekš aprakstīto procedūru, lai izveidotu abonēšanas maksas abiem abonementiem abonementu grupā Sub1. Nākamajā tabulā ir parādītas transakcijas, kas tiek izveidotas katram abonementam, kurš ir pievienots abonementu grupai.

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
<th><p>Projekta datums</p></th>
<th><p>Abonements</p></th>
<th><p>Projekts</p></th>
<th><p>Kategorija</p></th>
<th><p>Sākuma datums</p></th>
<th><p>Beigu datums</p></th>
<th><p>Pārdošanas valūta</p></th>
<th><p>Pārdošanas cena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-07-2007</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>28-07-2008</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Pirmajā transakcijā abonementam 00020\_135 pārdošanas cena 550 EUR tiek atvasināta no abonementa pārdošanas cenas, kas ir iestatīta konkrētā projekta un kategorijas kombinācijai. Otrajā transakcijā abonementam 00021\_135 pārdošanas cena 500 EUR tiek izmantota kā projekta abonementa pārdošanas cena, jo projekta 9030 un kategorijas SubCat2 kombinācijai pārdošanas cena nav iestatīta.

## <a name="see-also"></a>Skatiet arī

[Abonementu pārdošanas cenu atjaunināšana un indeksēšana](update-and-index-subscription-sales-prices.md)

  


