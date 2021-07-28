---
title: Izmaksu elementu dimensijas
description: Kā viens no pamatelementiem Izmaksu uzskaitē, izmaksu elementa dimensijas tiek izmantotas, lai sadalītu kategorijās un izsekotu, uz kurieni plūst izmaksas.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2fa602d01cadecbf24c2433360f7b2a8ebb0854a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355159"
---
# <a name="cost-element-dimensions"></a>Izmaksu elementu dimensijas

[!include [banner](../includes/banner.md)]

Kā viens no pamatelementiem Izmaksu uzskaitē, izmaksu elementa dimensijas tiek izmantotas, lai sadalītu kategorijās un izsekotu, uz kurieni plūst izmaksas. 

Izmaksu elements atbilst izmaksu atbilstošajam krājumam kontu plānā. Būtībā tas var būt jebkura veida elements, kam ir zemākais līmenis uzņēmumā, kur var plūst izmaksas. Izmaksu elementi kā koncepcijas diapazons no virsgrāmatas kontiem uz visiem izmaksu atbilstošajiem resursiem. Pašlaik Izmaksu uzskaite atbalsta virsgrāmatas kontus.

## <a name="two-types-of-cost-elements"></a>Divu veidu izmaksu elementi
Ir divu veidu izmaksu elementi: primāro izmaksu elementi un sekundāro izmaksu elementi. Šajā tabulā ir parādīta atšķirība starp abiem veidiem.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Primāro izmaksu elementi</strong></td>
<td><strong>Sekundāro izmaksu elementi</strong></td>
</tr>
<tr class="even">
<td>Primāro izmaksu elementi pārstāv izmaksu plūsmu no finanšu uzskaites uz izmaksu uzskaiti. Izmaksu elementu struktūra atbilst peļņas un zaudējumu konta struktūrai virsgrāmatā, kur izmaksu elements var atbilst galvenajam kontam. Ne visi galvenie konti vienmēr var tikt pārstāvēti kā izmaksu elementi atkarībā no biznesa vajadzībām. Primāro izmaksu elementu piemēri:
<ul>
<li>Pārdoto preču pašizmaksa</li>
<li>Netiešās materiālu izmaksas</li>
<li>Personāla izmaksas</li>
<li>Enerģijas izmaksas</li>
</ul></td>
<td>Sekundāro izmaksu elementi, kas pārstāv plūsmas izmaksas iekšēji, jo šīs izmaksas tiek izveidotas un izmantotas tikai Izmaksu uzskaitē. Tās tiek izmantotas, lai nodrošinātu, ka izmaksu avotu var izsekot. Šos izmaksu elementus izmanto izmaksu sadalījumos un pieskaitāmo izmaksu aprēķinos. Sekundāro izmaksu elementu piemēri:
<ul>
<li>Ražošanas izmaksas</li>
<li>Ražošanas, materiālu un mārketinga pieskaitāmās izmaksas</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>Izmaksu elementu dimensijas un izmaksu elementu dimensijas dalībnieki
Izmaksu elementi, kas tiek saukti par *izmaksu elementu dimensijas*. Atsevišķas dimensiju vērtības tiek sauktas par *izmaksu elementu dimensijas dalībnieki*. Piemēram, jums ir ASV kontu plāna struktūra (COA), kas ir pamats ar likumu noteikto pārskatu veidošanai. Šī COA tiek izmantota kā izmaksu elementa dimensija. Konti, kas ir primāro izmaksu elementi, tiek attēloti kā izmaksu elementu dimensijas dalībnieki Izmaksu uzskaitē. Šajā ekrānuzņēmumā parādīts Galveno kontu kā izmaksu elementu dimensijas piemērs, ar tā faktiskajiem galvenajiem kontiem kā izmaksu elementa dimensijas dalībniekiem. 

[![Galveno kontu ekrānuzņēmums kā izmaksu elementa dimensija.](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>Importējiet izmaksu elementu dimensijas dalībniekus, izmantojot datu savienotājus
Lai vienkāršotu izmaksu elementa dimensijas dalībnieku iestatīšanu Izmaksu uzskaitē, jūs varat izmantot datu savienotājus, kas ir vai nu iepriekš izveidoti vai jūsu izveidoti, lai izgūt primāro izmaksu elementus no vienas vai vairākām avota sistēmām.

## <a name="implementation-considerations"></a>Ieviešanas apsvērumi
Tā kā izmaksu elementi pārstāv izmaksu informācijas zemāko līmeni, jums nepieciešams pārliecināties, ka visi izmaksu elementi, kas ir nepieciešami vadības pārskata izveidei, ir iekļauti, īstenojot izmaksu elementu struktūru. Var būt sarežģīti atrast atbilstošu izmaksu elementu skaitu izmaksu kontrolei. Tā kā pastāv tūkstošiem izmaksu elementu, var būt sarežģīti kontrolēt katru izmaksu elementu. Alternatīva metode - jūs varat grupēt izmaksu elementus un pārvaldīt izmaksu kontroli uzkrātajā līmenī.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]