---
title: "Bieži uzdotie jautājumi par tulkojumiem, kas saistīti ar precēm"
description: "Šajā tēmā aprakstīts, kā pārvaldīt preču tulkojumus, preču dimensiju vērtības un preču īpašības."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d232473a1df0b821c6f39553ad826c61ff9ecff8
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="product-related-translations-faq"></a>Bieži uzdotie jautājumi par tulkojumiem, kas saistīti ar precēm

[!include[banner](../includes/banner.md)]


Šajā tēmā aprakstīts, kā pārvaldīt preču tulkojumus, preču dimensiju vērtības un preču īpašības. 

<a name="what-product-related-data-can-be-translated"></a>Kādi preču dati var tikt tulkoti?
--------------------------------------------

Jūs varat izveidot tulkojumus šādai preču informācijai:
-   Preču nosaukumiem un aprakstiem.
-   Aprakstiem, piemērotiem nosaukumiem un preces īpašību vērtību palīdzības tekstiem.
-   Preces dimensijas vērtību nosaukumiem un aprakstiem.

Varat tulkot ar precēm saistīto informāciju jebkurā valodā, kas ir pieejama lapā **Teksta tulkojums**. Papildinformāciju skatiet sadaļā **Kā izveidot tulkojumu preču informācijai**.

## <a name="where-can-i-view-the-translated-information"></a>Kurā es varu skatīt tulkoto informāciju?
Preču tulkoto informāciju varat apskatīt jebkurā ārējā pirmdokumentā, piemēram, rēķinā, kas izmanto valodu ar pieejamiem tulkojumiem.

## <a name="how-do-i-create-translations-for-productrelated-information"></a>Kā izveidot tulkojumu preču informācijai?
Lai izveidotu preces tulkojumu, izpildiet tālāk aprakstītās darbības:
1.  Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Vispārīgi** &gt; **Izlaistās preces**.
2.  Atlasiet preci un darbību rūtī grupā **Valodas** noklikšķiniet uz **Tulkojumi**.
3.  Lapas **Teksta tulkojums** laukā **Valoda** atlasiet valodu. Lai pievienotu vairāk valodu, izvērsiet lauku **Valoda** un pēc tam noklikšķiniet uz **Labi**.
4.  Grupā **Tulkotais teksts** ievadiet tulkojumus laukos **Apraksts** un **Preces nosaukums**.

Lai izveidotu preču īpašību tulkojumu, izpildiet tālāk aprakstītās darbības:
1.  Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Vispārīgi** &gt; **Izlaistās preces**.
2.  Sadaļā **Iestatījumi** noklikšķiniet uz **Atribūti** un pēc tam noklikšķiniet uz **Atribūti**.
3.  Lapā **Atribūti** noklikšķiniet uz **Tulkot**.
4.  Lapas **Teksta tulkojums** laukā **Valoda** atlasiet valodu. Lai pievienotu vairāk valodu, izvērsiet lauku **Valoda** un pēc tam noklikšķiniet uz **Labi**.
5.  Grupā **Tulkotais teksts** ievadiet tulkojumus laukos **Apraksts**, **Draudzīgais nosaukums** un **Palīdzības teksts**.

Lai izveidotu preces dimensijas tulkojumu, izpildiet tālāk aprakstītās darbības:
1.  Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Vispārīgi** &gt; **Izlaistās preces**.
2.  Atlasiet preci un pēc tam noklikšķiniet uz **Preces dimensijas**.
3.  Atlasiet vienu no preču dimensiju saitēm: **Konfigurācijas**, **Izmēri**, **Krāsas** vai **Stils**.
4.  Atlasiet dimensijas vērību un pēc tam noklikšķiniet uz **Tulkot**.
5.  Lapas **Teksta tulkojums** laukā **Valoda** atlasiet valodu. Lai pievienotu vairāk valodu, izvērsiet lauku **Valoda** un pēc tam noklikšķiniet uz **Labi**.
6.  Grupā **Tulkotais teksts** ievadiet tulkojumus laukos **Nosaukums** un **Apraksts**.

## <a name="can-the-names-of-product-variants-be-translated"></a>Vai var tulkot preču variantu nosaukumus?
Preces varianti ir balstīti uz izlaisto preču dimensijas. Preces variantu nosaukumi ir balstīti uz dimensiju vērtību kombināciju. Kad dimensiju vērtības, kas ir saistītas ar preces variantu, tiek tulkotas, preces varianta nosaukums parādās tulkojuma versijā.  

**Piemērs**  

Jūsu prece ir dažādu izmēru un krāsu t-krekls, un variantu nosaukumi balstās uz šādu informāciju:
-   Preces numuru: \#3
-   Dimensijām: izmēru un krāsu
-   Izmēru dimensijas vērtībām: mazs, vidējs, liels
-   Krāsu dimensijas vērtībām: sarkana, zaļa, melna

Preces varianta nosaukums, kas ir balstīts uz dimensiju vērtībām Mazs un Sarkans, ir **\#3:Mazs:Sarkans**.  

Ja klients vēlas iegādāties vairākus mazus, sarkanus t-kreklus, tad t-krekla nosaukumam rēķinā jāparādās franču valodā. Pārtulkojot dimensiju vērtības Mazs un Sarkans franču valodā, preces varianta nosaukums būs **\#3:Petit:Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Padoms</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lai iestatītu klienta vēlamo valodu, rīkojieties šādi:
<ol>  
<li>Noklikšķiniet uz <strong>Pārdošana un mārketings</strong> &gt; <strong>Vispārīgi</strong> &gt; <strong>Debitori</strong> &gt; <strong>Visi</strong> <strong>debitori</strong>.</li>
<li>Veiciet dubultklikšķi uz debitora, lai atvērtu lapu <strong>Debitori</strong>. Cilnes <strong>Vispārīgi</strong> laukā <strong>Valoda</strong> atlasiet <strong>valodu</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Kas notiek, ja klienta vēlamajai valodai nav pieejami tulkojumi?
Ja tulkojumi nav pieejami klienta vēlamajai valodai, nosaukumi un apraksti tiek parādīti jūsu uzņēmuma galvenajā valodā.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Vai es vienlaicīgi varu pārvaldīt vairāku dimensiju vērtību tulkojumus?
Dimensijas vērtības ir raksturīgas precei, un jūs varat pārvaldīt tulkojumu katrai preces dimensijas vērtībai. Tomēr, ja izveidojat dimensijas vērtību grupu un izveidojat tulkojumus šīs grupas vērtībām, ir vieglāk pārvaldīt tulkojumus.   

**Piemērs**  

Piemēram, jūsu uzņēmums ražo dažāda modeļa t-kreklus, un katrs modelis ir pieejams izmēros mazs, vidējs un liels. Izmēri tiek apvienoti vienā dimensiju vērtību grupā. Pievienojot jaunu t-krekla modeli, varat to saistīt ar dimensiju vērtību grupu, kas paredzēta izmēriem, tādējādi precei būs pieejami visi izmēri. Jebkurā laikā varat arī pievienot vai mainīt tulkojumus dimensiju vērtību grupā, kas paredzēta izmēriem.  

Dimensijas vērtība, kas ir saistīta ar preci dimensiju variantu grupā, ir jāpārvalda no preču variantu grupas.   
Lai izveidotu dimensijas vērtību grupu, izpildiet tālāk aprakstītās darbības:
1.  Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Iestatījumi** &gt; **Variantu grupas**.
2.  Atlasiet **Izmēru** **grupas**, **Krāsu grupas** vai **Stilu grupas**.
3.  Noklikšķiniet uz **Jauns** un pēc tam ievadiet grupas nosaukumu laukā **Izmēru** **grupa**, **Krāsu grupa** vai **Stilu grupa**. Noklikšķiniet uz **Izmēri**, **Krāsas** vai **Stili**, lai grupām izveidotu rindas.
4.  Lapā **Izmēru** **grupas** rindas, **Krāsu** **grupas** **rindas** vai **Stilu grupas rindas** noklikšķiniet uz **Jauns** un pēc tam izveidojiet grupām izmērus, krāsas un stilus.

Lai pārvaldītu vērtību tulkojumus dimensijas vērtību grupās, rīkojieties šādi:
1.  Izpildiet norādījumus iepriekšējā procedūrā dimensijas vērtību grupas izveidošanai, lai atvērtu lapu **Izmēru grupu rindas**, **Krāsu grupu rindas** vai **Stilu grupu rindas**.
2.  Noklikšķiniet uz **Teksta tulkojums**. Lapas **Teksta tulkojums** grupā **Tulkotais teksts** ievadiet tulkojumus laukos **Nosaukums** un **Apraksts**.

## <a name="when-can-translations-of-productrelated-information-be-managed"></a>Kad var pārvaldīt ar precēm saistītās informācijas tulkojumus?
Jebkurā laikā varat pārvaldīt ar precēm saistītas informācijas tulkojumus. Atjauninot tulkojumus dimensijas vērtībai, kas ir saistīta ar preci, preces informācija tiek atjaunināta neatkarīgi no tā, vai ar preci tiek veikti darījumi.






