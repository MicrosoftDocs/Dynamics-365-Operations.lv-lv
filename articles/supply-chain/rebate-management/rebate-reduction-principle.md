---
title: Atlaižu samazināšanas principi
description: Šajā tēmā ir aprakstīts, kā iestatīt samazināšanas profilus. Samazināšanas principi kontrolē darbību, ja uz vienu krājumu vai darījumu attiecas vairākas atlaides.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fec7f94aba46f8b1853e0520169dd628fd940a56
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685944"
---
# <a name="rebate-reduction-principles"></a>Atlaižu samazināšanas principi

[!include [banner](../includes/banner.md)]

Jūs varat grupēt atlaižu pārvaldības darījumus *samazināšanas principiem*, lai samazinātu citus ar krājumu saistītos nosacījumus un/vai lai samazinātu atlaižu aprēķinu iegūtās vērtības. Pēc atlaižu samazināšanas principu iestatīšanas jūs pēc izvēles varat tos piešķirt atlaižu pārvaldības darījumu rindām, ja nepieciešams.

Atlaides samazināšanas principa noteikumi ir spēkā tikai tad, ja atlaides darījumi pārklājas. Tāpēc viņi var piešķirt vairākas atlaides gadījumos, kad nav pienākas vairākas atlaides.

## <a name="manage-rebate-reduction-principles"></a>Pārvaldīt atlaižu samazināšanas principus

Lai strādātu ar atlaižu samazināšanas principiem, pārejiet uz sadaļu **Atlaižu pārvaldība \> Iestatījumi \> Atlaižu samazināšanas principi**. Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un samazināšanas principus, ja nepieciešams. Iiestatiet laukus katram principam, kā aprakstīts sekojošajā tabulā.

| Lauks | Apraksts |
|---|---|
| Atlaižu samazināšanas princips | Ievadiet unikālu atlaides samazināšanas principa nosaukumu. |
| Apraksts | Ievadiet unikālu atlaides samazināšanas principa aprakstu. |
| Lietot samazinājumu | Atzīmējiet šo izvēles rūtiņu, lai atlaides, kas pieder šim atlaides samazināšanas principam, piemērotu samazinājuma bāzi. |
| Samazināšanas bāze | Ja ir atlasīta izvēles rūtiņa **Lietot samazinājumu**, atlasiet samazināšanas bāzi (*Uzkrājumi*, *Atlaides* vai *Abi*). Ja izvēlaties *Abi* un ja uzkrājums, gan atlaide ir iegrāmatota iepriekšējam darījumam, tikai atlaide tiks piemērota. |
| Izslēgt no samazināšanas | Ja ir atzīmēta šī izvēles rūtiņa, uzkrājumi un atlaides, kas pieder šim atlaižu samazināšanas principam, tiks izslēgti no turpmākajiem samazinājumiem. Lauka **Samazināšanas bāzes** iestatīšana neattiecas uz šo iestatījumu. |

## <a name="examples-of-rebate-reduction-principle-setups"></a>Atlaides samazināšanas principa iestatījumu piemēri

Tālāk sniegtajā tabulā ir norādīti daži tipiski atlaižu samazināšanas principa iestatījumu piemēri. Katram no šiem atlaižu samazināšanas principiem lauka **Apraksts** vērtība apraksta atlaides samazināšanas principa nolūku.

| Atlaižu samazināšanas princips | Apraksts | Lietot samazinājumu | Samazināšanas bāze | Izslēgt no samazināšanas |
|---|---|---|---|---|
| Atlikts | Samazināt atlaidi | Jā | Abi | Nē |
| Exclreb | Izslēgt atlaidi | Jā | Atlaide | Jā |
| Vairāki | Vairākas atlaides | Jā | Abi | Jā |
| Neviens | Tikai noteikumi un atlaide | Nē | Abi | Jā |
| Noteikums | Tikai noteikums | Jā | Noteikums | Nē |
| Atlaide | Tikai atlaide | Jā | Atlaide | Jā |

## <a name="examples-of-rebate-reduction-principle-calculations"></a>Atlaides samazināšanas principa aprēķinu piemēri

Jums ir pārdošanas pasūtījums, kam ir viena pārdošanas pasūtījuma rinda. Šai rindai ir rindas $1000. Uz pasūtījumu attiecas šādi darījumi:

- **1. darījums:** 10 procenti no $1000
- **2. darījums:** 15 procenti no $1000
- **3. darījums:** 20 procenti no $1000
- **4. darījums:** 25 procenti no $1000

Apstrādes secība ir ļoti svarīga. Apstrādes pasūtījums ir balstīts uz veidu, kādā strādājat, kā aprakstīts [Apstrādāt, pārskatīt un grāmatot atlaides](process-review-post.md).

Piemēram, tabulā ir apkopots rezultāts, ja izmantojat pasūtījumu *1, 2, 3, 4* un ja apstrādāsit tikai nosacījumus.

| Akcija | Apraksts un iestatījumi | Nodrošinājumu rezultāts |
|---|---|---|
| 1 | <p>Klasifikācija nepārbauda citus samazinājumu darījumus. Pārbaude tiek veikta gan uzkrājumiem, gan atlaidēm.</p><ul><li>**Lietot samazinājumu:** *No*</li><li>**Samazināšanas bāze:** *Abi*</li><li>**Izslēgt no samazināšanas:** *Nē*</li></ul> | $1000 × 10% = $100 |
| 2 | <p>Klasifikācija citos darījumos pārbauda samazināšanas darījumus, bet tiek atzīmēta ar karodziņu, lai ignorētu sevi. Pārbaude tiek veikta tikai atlaidēm.</p><ul><li>**Lietot samazinājumu:** *Jā*</li><li>**Samazināšanas bāze:** *Atlaide*</li><li>**Izslēgt no samazināšanas:** *Jā*</li></ul> | $1000 × 15% = $150 |
| 3 | <p>Klasifikācija pārbauda citus samazinājumu darījumus. Pārbaude tiek veikta gan uzkrājumiem, gan atlaidēm.</p><ul><li>**Lietot samazinājumu:** *Jā*</li><li>**Samazināšanas bāze:** *Abi*</li><li>**Izslēgt no samazināšanas:** *Nē*</li></ul> | ($1000 – 1. darījums) × 20% = $180 |
| 4 | <p>Klasifikācija pārbauda citus samazinājumu darījumus. Pārbaude tiek veikta gan uzkrājumiem, gan atlaidēm.</p><ul><li>**Lietot samazinājumu:** *Jā*</li><li>**Samazināšanas bāze:** *Abi*</li><li>**Izslēgt no samazināšanas:** *Nē*</li></ul> | ($1000 – 1. darījums – 3. darījums) × 25% = $180 |

Tabulā redzami daži piemēri, kad uzkrājumi tiek apstrādāti dažādos pasūtījumos un kur tāpēc tiek sasniegtas dažādas kopsummas. Uzkrājumu novirze ir atkarīga no pasūtījuma, kurā sistēma apstrādā darījumus. Ir svarīgi saprast, kā apstrādes pasūtījums ietekmē gala atlaides summu.

| Sērija | Aprēķins |
|---|---|
| 1<br>(1, 2, 3, 4) | <ul><li>**1. darījums:** $1000 × 10% = $100</li><li>**2. darījums:** $1000 × 15% = $150</li><li>**3. darījums:** ($1000 – 1. darījums) × 20% = $180</li><li>**4. darījums:** ($1000 – 1. darījums – 2. darījums) × 25% = $180</li><li>**Kopējie uzkrājumi:** $610</li></ul> |
| 2<br>(4, 3, 2, 1) | <ul><li>**4. darījums:** $1000 x 25% = $250</li><li>**3. darījums:** ($1000 – 4. darījums) × 20% = $150</li><li>**2. darījums:** $1000 x 15% = $150</li><li>**1. darījums:** $1000 x 10% = $100</li><li>**Kopējais nodrošinājums:** $650</li></ul> |
| 3<br>(3, 2, 1, 4) | <ul><li>**3. darījums:** $1000 x 20% = $200</li><li>**2. darījums:** $1000 x 15% = $150</li><li>**1. darījums:** $1000 x 10% = $100</li><li>**4. darījums:** ($1000 – 3. darījums – 1. darījums) × 25% = $175</li><li>**Kopējais nodrošinājums:** $625</li></ul> |
| 4<br>(2, 4, 1, 3) | <ul><li>**2. darījums:** $1000 × 15% = $150</li><li>**4. darījums:** $1000 × 25% = $250</li><li>**1. darījums:** $1000 × 10% = $100</li><li>**3. darījums:** ($1000 – 4. darījums – 1. darījums) × 20% = $130</li><li>**Kopējais nodrošinājums:** $630</li></ul> |
