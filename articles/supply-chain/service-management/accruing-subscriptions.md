---
title: Abonementu uzkrāšana
description: Ar pakalpojumu abonementu, periodos, kas seko maksājuma darbības rēķina izrakstīšanas datumam, jūs manuāli uzkrājat ieņēmumus.
author: kamaybac
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d17737c415f6204359dae3ea4b2a0cb4ebb5d65
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580484"
---
# <a name="accruing-subscriptions"></a>Abonementu uzkrāšana 

[!include [banner](../includes/banner.md)]


Ar pakalpojumu abonementu, periodos, kas seko maksājuma darbības rēķina izrakstīšanas datumam, jūs manuāli uzkrājat ieņēmumus.

Uzkrājumu periodi tiek izveidoti rēķina periodam, ko jūs iestatāt abonementa maksājumam, uzkrājumu periodi ir balstīti uz abonementa perioda kodu.

Jūs varat uzkrāt un atcelt uzkrāto ieņēmumu.

## <a name="reverse-accruals-of-credit-amounts"></a>Kredīta summu uzkrājumu reversēšana

Ja kreditējat rēķinos ierakstītos abonementu apjomus, jūs varat izmantot divas metodes uzkrāto apjomu reversēšanai.

  - Varat reversēt katru uzkrāto ienākumu darījumu individuāli, pirms izveidojat kredīta notas piedāvājumu darījumam. Šī ir manuālā metode. (manuāli)

  - Jūs varat reversēt visus uzkrātos apjomus kredīta notas iegrāmatošanas datumā vai uzkrājuma iegrāmatošanas datumā.

Vairāk informācijas var atrast [Abonēšanas parametri (veidlapa)](/dynamicsax-2012//subscription-parameters-form).

## <a name="setup-requirements"></a>Uzstādīšanas prasības

Lai uzkrātu ieņēmumus, pārliecinieties, vai šīs datu prasības ir ievērotas:

## <a name="account-setup"></a>Konta iestatīšana

**NP - abonements** un **Uzkrātie ieņēmumi - abonements** kontiem ir jābūt iestatītiem modulī **Projekts**.

Iegrāmatojot uzkrāto ieņēmumu, konts **NP - abonements** tiek debitēts ar uzkrāto apjomu, bet konts **Uzkrātie ieņēmumi - abonements** tiek kreditēts ar uzkrāto apjomu.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Iestatīt kontus abonementa ieņēmumu uzkrāšanai

1.  Noklikšķiniet uz **Projektu vadība un uzskaite** \> **Iestatījumi** \> **Grāmatošana** \> **Virsgrāmatas grāmatojumu iestatīšana**.

2.  Noklikšķiniet uz cilnes **Ieņēmumu konti** cilnes un atlasiet **NP - abonements** vai **Uzkrātie ieņēmumi - abonements**, lai iestatītu kontus.

## <a name="subscription-group-setup"></a>Abonementa grupas iestatīšana

Lai varētu uzkrāt ieņēmumus abonementiem, jābūt atzīmētai izvēles rūtiņai **Uzkrāt ieņēmumus**. Tā ir atrodama veidlapā **Abonementu grupas** grupai, kas piesaistīta abonementam. Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu abonementi** \> **Abonementu grupas**.

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Iespējot ieņēmumu uzkrāšanu abonementa grupai

Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu abonementi** \> **Abonementu grupas**.

## <a name="periods"></a>Periodi

Jums ir jāiestata rēķina izrakstīšanas perioda kods. Ja vien nevēlaties uzkrāt ieņēmumus ar tiem pašiem laika intervāliem, kas tiek izmantoti rēķinu izrakstīšanā, jums ir jāiestata arī uzkrāšanas periods.

Šajā tabulā ir pārskats par uzkrāšanas periodiem, ko varat iestatīt katram rēķinu izrakstīšanas periodam.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Maksāšanas termiņš</p></th>
<th><p>Uzkrāšanas periods</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Gadi</strong></p></td>
<td><ul>
<li><p><strong>Gadi</strong></p></li>
<li><p><strong>Ceturksnis</strong></p></li>
<li><p><strong>Mēnesis;</strong></p></li>
<li><p><strong>Diena;</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Ceturksnis</strong></p></td>
<td><ul>
<li><p><strong>Ceturksnis</strong></p></li>
<li><p><strong>Mēnesis;</strong></p></li>
<li><p><strong>Diena;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Mēnesis;</strong></p></td>
<td><ul>
<li><p><strong>Mēnesis;</strong></p></li>
<li><p><strong>Diena;</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Nedēļa</strong></p></td>
<td><ul>
<li><p><strong>Diena;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Diena;</strong></p></td>
<td><ul>
<li><p><strong>Diena;</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

Rēķina perioda iestatīšana ir obligāta daļa no abonementu grupas vispārīgajiem iestatījumiem. Varat izlemt, vai arī iestatīt uzkrāšanas periodu abonementu grupai. Ja iestatāt uzkrāšanas periodu abonementu grupai, šis periods tiks norādīts laukā **Perioda kods**. Šis lauks ir veidlapā **Uzkrāt abonementu ieņēmumus**, ja jūs uzkrājat abonementu ieņēmumus. Tomēr uzkrāšanas periods ir papildu informācija par abonementa grupu.


> [!NOTE]
> <P>Izmantojiet šādu ceļu, lai atvērtu veidlapu <STRONG>Uzkrāt abonementu ieņēmumus</STRONG>. Noklikšķiniet uz <STRONG>Pakalpojumu pārvaldība</STRONG> &gt; <STRONG>Periodiski</STRONG> &gt; <STRONG>Pakalpojumu abonementi</STRONG> &gt; <STRONG>Uzkrāt abonementu ieņēmumus</STRONG>.</P>


## <a name="transactions"></a>Darbības

Jūs varat kontrolēt virsgrāmatas darījumu skaitu, kas tiek izveidoti, grāmatojot uzkrāto ieņēmumu. Abonementiem nosakiet, vai virsgrāmatas darījumi jāveido kā kopums vai pa rindām.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Norādiet grāmatošanas detaļu līmeni, ko rādīt uzkrātajām darbībām

1.  Noklikšķiniet uz **Projektu vadība un uzskaite** \> **Iestatīšana** \> **Projektu vadības un uzskaites parametri**.

2.  Cilnē **Finanses** laukā **Rēķins** atlasiet **Kopā** vai **Rinda**.


## <a name="see-also"></a>Skatiet arī

[Uzkrāt abonementa ieņēmumus](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]