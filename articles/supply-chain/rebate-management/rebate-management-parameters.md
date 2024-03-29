---
title: Atlaižu pārvaldības parametri
description: Šajā rakstā ir aprakstīta lapa Atlaižu pārvaldības parametri. Šī lapa satur iestatījumus, kas ietekmē grāmatošanu, statusa atjauninājumus, numuru secības un citu uzvedību.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 218c54d97f3ac204e8613f5efdda0cc9d713ee04
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895530"
---
# <a name="rebate-management-parameters"></a>Atlaižu pārvaldības parametri

[!include [banner](../includes/banner.md)]

**Atlaižu pārvaldības parametru** lapa tiek izmantota, lai definētu iestatījumus, kas ir spēkā **Atlaižu pārvaldības** modulī. Šie iestatījumi ietekmē grāmatošanu, statusa atjauninājumus, numuru secības un citu uzvedību. Šīs lapas iestatījums tiek koplietots visām juridiskajām personām, un to var modificēt lietotāji, kuriem ir atbilstošās drošības atļaujas.

Lai atvērtu lapu **Atlaižu pārvaldības parametri**, atveriet lapu **Atlaižu pārvaldība \> Iestatījumi \> Atlaižu pārvaldības parametri**. Pēc tam iestatiet laukus, kā aprakstīts sekojošās apakšsadaļās.

## <a name="rebate-management-tab"></a>Atlaižu pārvaldības cilne

Sekojošajā tabulā ir aprakstīti lauki, kas ir pieejami cilnes **Atlaižu pārvaldība** lapā **Atlaižu pārvaldības paramentri**.

| Lauks | Apraksts |
|---|---|
| Noklusētais statuss | Atlasiet noklusēto statusu visiem jaunajiem darījumiem. Lai definētu atlasei pieejamo statusa vērtību kopu, izmantojiet [**Atlaižu statusi** lapa](rebate-statuses.md). |
| Apstrādāt pēc dimensijas | Atlasiet, vai nodrošinājuma, atlaides un norakstīšanas darbības jāapstrādā pēc finanšu dimensijas. Ja šī opcija ir ieslēgta, sistēma izmanto finanšu dimensijas no avota darījumiem mērķa darījumos. |
| Pārbaudīt, vai ir iepriekš grāmatots | <p>Atlasiet sistēmas darbību, ja vienā periodā negrāmatoti atlaižu darījumi ir apstrādāti vairāk nekā vienu reizi:</p><ul><li>**Brīdinājums** – sistēma ļauj lietotājiem ignorēt oriģinālās darbību rindas, bet tiek parādīts brīdinājums.</li><li>**Kļūda** – sistēma neļauj lietotājiem ignorēt sākotnējās darbību rindas un tiek parādīts kļūdas ziņojums. |
| Automātiski grāmatot žurnālus | Atlasiet, vai sistēmai automātiski jāgrāmato piedāvātie žurnāli. Šie žurnāli ietver ikdienas žurnālus, kas tiek izmantoti uzkrājumiem un debitoru ieturējumiem, kā arī kreditoru nodokļu rēķinu žurnālus. |
| Automātiska brīvā teksta rēķinu grāmatošana | Atlasiet, vai sistēmai automātiski jāgrāmato brīvā teksta rēķini. Šī opcija attiecas tikai uz brīvā teksta rēķiniem, kur maksājuma veids ir iestatīts kā *Nodokļu rēķina debitora ieturējumi*. |
| Atlaides krājuma pasūtījuma atsauce | Atlasiet atlaides atsauci, ko izmantot pārdošanas pasūtījumiem un pirkšanas pasūtījumiem, kas tiek ģenerēti no atlaides procesa (*Nav*, *Atlaides pārvaldības darījums*, *Alaides pārvaldības numurs*, *Atlaides darījuma numurs* vai *Dokumenta piezīmes*). |
| Prasību apstrādes izmantošana | <p>Iestatiet šo opciju kā *Jā*, lai izmantotu prasību apstrādi. Šādā veidā varat atzīmēt darījumus, kurus Atlaižu pārvaldība izveido kā pieprasītu vai kā nepieprasītu, un pēc tam grāmatot tikai pieprasītās darbības.</p><p>Piemēram, jūs aprēķināt atlaides mēneša transakciju vērtībai, bet debitors divas dienas nav pieprasījis. Šajā gadījumā nepieprasītas darbības tiks atkārtoti izveidotas nākamajā reizē, kad būs palaista *Procesa* funkcija nākamajam periodam.</p><p>Ja iestatāt šo opciju kā *Nē*, visas prasības darbības tiek grāmatotas.</p> |
| Iekļaut pasūtījuma tipa žurnālu | Darījumiem vai darījuma rindām, kur darbības tips ir iestatīts uz *Pasūtījums*, šī opcija kontrolē, vai jāiekļauj *Žurnāla* tipa pārdošanas pasūtījums. Tas nodrošina elastību, ja šie pasūtījumu veidi tiek izmantoti scenārijos, kuros atlaide vēl nav jāpiemēro. |

## <a name="number-sequences-tab"></a>Cilne Numuru sērijas

Izmantojiet lapas **Atlaižu pārvaldības parametri** cilni **Numuru sērijas**, lai piešķirtu numuru sērijas kodus dažādām numuru sērijām, kuras izmanto Atlaižu pārvaldība. Tabulā ir aprakstīts katras šīs numuru sērijas nolūks. Papildinformāciju par numuru sērijām skatiet [sadaļā Numuru sēriju apskats](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) un saistītie dokumenti.

| Atsauce | Apraksts |
|---|---|
| Atlaižu pārvaldības darījums | Numuru sērija piešķir unikālu atslēgas vērtību katram atlaides darījumam. Šī atslēga tiek izmantota, kad tiek izveidoti darījumi. |
| Atlaižu pārvaldības numurs | Numuru sērija piešķir unikālu atslēgas vērtību katram atlaides darījumam. Šī atslēga tiek izmantota, lai identificētu atlaižu attiecības. |
| Atlaides darījuma numurs | Numuru sērija piešķir unikālu atslēgas vērtību katram atlaides darījumam. Šī atslēga tiek izmantota, lai identificētu atlaižu darījumus. |
| Nodokļu rēķins | Numuru sērija piešķir unikālu atslēgas vērtību katram atlaides darījumam. Šo atslēgu izmanto, automātiski grāmatojot atlaižu žurnālus. |

## <a name="feature-visibility-tab"></a>Līdzekļu redzamības cilne

Atlaižu pārvaldība pievieno funkcijas (lauki un funkcijas) vairākām bieži izmantotajām Microsoft Dynamics 365 Supply Chain Management lapām. Šīs lapas ietver lapas, kas ir saistītas ar pārdošanas pasūtījumiem un pārdošanas darījumiem. Ja izmantojat Atlaižu pārvaldību, šīs funkcijas ir jāizveido redzamās visur, kur var gūt labumu no tām. Ja neizmantojat Atlaižu pārvaldību, ir iespējams paslēpt funkcijas, lai novērstu to izgāšanu.

Lapas **Atlaižu pārvaldības parametri** cilnē **Līdzekļu redzamība** iestatiet opciju **Aktivizēt** uz *Jā*, lai redzētu Atlaižu pārvaldības funkcijas vienmēr, kad tās ir pieejamas. Iestatiet uz *Nē*, lai paslēptu iezīmes kopējās lapās ārpus **Atlaižu pārvaldības** moduļa. Tomēr, pat ja opcija ir iestatīta uz *Nē*, pats modulis, tostarp lapa **Atlaižu pārvaldības parametri**, būs pieejams lietotājiem ar pareizām atļaujām, lai piekļūtu tam.
