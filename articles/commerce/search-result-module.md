---
title: Meklēšanas rezultātu modulis
description: Šajā tēmā tiek stāstīts par meklēšanas rezultātu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3409e9e99329def55b173eb78cf03db4a6764c92
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794119"
---
# <a name="search-results-module"></a>Meklēšanas rezultātu modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par meklēšanas rezultātu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

Meklēšanas rezultātu modulis atgriež preču meklēšanas rezultātus un piemērojamo preču rafinētāju sarakstu. Meklēšanas rezultātu moduļus Dynamics 365 Commerce vietnēs var izmantot, lai atveidotu lapas šādiem scenārijiem:

- Meklēšanas rezultāti, ko uzsāka lietotāja meklēšana
- Meklēšanas rezultāti, kas norāda noteiktu preču kopu, piemēram, "Pirkt līdzīgas preces"
- Preču saraksti, kas pieder noteiktai kategorijai

Papildinformāciju par kategoriju un meklēšanas rezultātu lapām skatiet [Noklusējuma kategorijas ielādes lapa un meklēšanas rezultātu lapas apskats](category-search-page-overview.md).

Sekojošajā attēlā redzams kategorijas meklēšanas rezultātu lapas piemērs Fabrikam vietnē.

![Meklēšanas rezultātu lapas piemērs Fabrikam vietnē](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Meklēšanas rezultātu moduļa rekvizīti

Tabulā zemāk uzskaitīti meklēšanas rezultātu moduļu rekvizīti un to vērtības un apraksti.

| Rekvizīts | Vērtības | Apraksts |
|----------|--------|-------------|
| Vienumi lapā | Vesels skaitlis | Krājumu skaits, kas jāparāda katrā lapā. |
| Atļaut balstīties uz PDP | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts uz **Patiess**, kad lietotājs atlasa preci meklēšanas rezultātu lapā, atpakaļceļa navigācija uz preces informācijas lapu, kas ir atvērta, parādīs saiti "Atpakaļ uz rezultātiem". |
| Izvērst precizētājus | **Viss**, **1**, **2**, **3**, or **4** | Galveno rafinētāju skaits, kas jāizvērš, kad lapa ir ielādēta. Piemēram, ja šis rekvizīts ir iestatīts uz **3**, tiks izvērsti pirmie trīs rafinētāji lapā. |
| Paslēpt kategoriju hierarhijas attēlojumu | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts uz **Patiess**, lapā parādītā kategoriju hierarhija tiks paslēpta. Šis rekvizīts būtu jāiestata uz **Patiess**, ja izmantojat [atpakaļceļa moduli](add-breadcrumb.md), lai rādītu kategoriju hierarhiju.|
| Meklēšanas rezultātos iekļaut produkta atribūtus | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts uz **Patiess**, meklēšanas rezultātos precēm tiks atgriezti atribūti. Lai arī šos atribūtus var parādīt Commerce vietnē, nepieciešams paplašinājums.|
| Rādīt piederības cenas | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts uz **Patiess**, preču piederības cenas tiks rādītas meklēšanas rezultātos, kad lietotājs, kurš ir pierakstījies, pārlūko lapu. |

> [!IMPORTANT]
> Dynamics 365 Commerce 10.0.16 laidienā un jaunākos laidienos konfigurāciju **Rādīt piederības cenas** var izmantot, lai lapā parādītu piederības cenas lapā.

## <a name="supported-modules"></a>Atbalstītie moduļi

Meklēšanas rezultātu modulis atbalsta [ātro skatu moduli](quick-view-module.md), kas ļauj lietotājiem skatīt preces informāciju un pievienot vienumus grozam no meklēšanas rezultātu lapas.

## <a name="add-a-search-results-module-to-a-category-page"></a>Pievienot meklēšanas rezultātu moduli kategorijas lapai

Lai pievienotu meklēšanas rezultātu moduli kategorijas lapai, veiciet tālāk minētās darbības.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** ievadiet nosaukumu **Meklēt rezultātus** un pēc tam atlasiet **Labi**.
1. Slotā **Pamatteksts** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.
1. Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Slotā **Konteiners** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Atpakaļceļs** un pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī **Atpakaļceļš** ievadiet vērtību **1** opcijai **Min. atkārtošanās skaits**.
1. Slotā **Konteiners** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Meklēšanas rezultāti** un pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī **Meklēšanas rezultāti** ievadiet vērtību **1** opcijai **Min. atkārtošanās skaits** un pēc tam iestatiet visus citus nepieciešamos meklēšanas rezultātu modulim. Iestatot šos rekvizītus veidnē, pārliecinieties, ka visi konkrētas kategorijas lapas pielāgojumi automātiski ietvers šos iestatījumus.
1. Atlasiet **Pabeigt rediģēšanu** un pēc tam atlasiet **Publicēt**, lai publicētu veidni.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet iepriekš izveidoto veidni **Meklēšanas rezultāti**, ievadiet **Kategorijas lapa** opcijai **Lapas nosaukums** un pēc tam atlasiet **Labi**. Tā kā visas vērtības ir iestatītas veidnē, lapa ir gatava publicēšanai.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Noklusējuma kategorijas reklāmas mērķlapas un meklēšanas rezultātu lapas pārskats](category-search-page-overview.md)

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Ātrā skata modulis](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
