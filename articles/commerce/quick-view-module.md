---
title: Ātrā skata modulis
description: Šajā tēmā tiek stāstīts par ātrā skata moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 5ba42806d8f77f41ab9c5cf5e26b20ecb647aadf
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780822"
---
# <a name="quick-view-module"></a>Ātrā skata modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par ātrā skata moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

Ātrā skata modulis ļauj lietotājiem ātri skatīt preču informāciju, kad tie pārlūko preces saraksta lapā, un pievienot vienu vai vairākas preces grozam no saraksta lapas, bez nepieciešamības atvērt preču informācijas lapu (PDP). Ātrā skata modulis nodrošina preču informācijas pārskatu, kas lietotājiem nepieciešams, lai veiktu “pievienot grozam” lēmumu. Tas nodrošina arī saiti uz PDP, lai lietotāji varētu skatīt preces papildu informāciju un pirkšanas opcijas.

Ātrā skata modulis tiek atbalstīts [preču kolekcijas](product-collection-module-overview.md) un [meklēšanas rezultātu](search-result-module.md) moduļos.

> [!IMPORTANT]
> Ātrā skata modulis ir pieejams no Commerce versijas 10.0.17 laidiena.

Tālāk esošajā ilustrācijā redzams ātrā skata moduļa piemērs preču saraksta lapā.

![Ātrā skata moduļa piemērs preču saraksta lapā.](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>Moduļa rekvizīti

Ātrā skata modulis atbalsta dažas no tām pašām funkcijām, ko iegādes lodziņa modulis. Tādēļ ātrā skata moduļa rekvizīti ir līdzīgi iegādes lodziņa moduļa rekvizītiem.

| Rekvizīts | Vērtības | Apraksts |
|----------------|--------|-------------|
| Virsraksta atzīme | **H1**, **H2**, **H3**, **H4**, **H5** vai **H6** | Šis rekvizīts definē virsraksta atzīmi preces nosaukumam. Ja ātrā skata modulis atrodas lapas augšā, šis rekvizīts ir jāiestata uz **H1**, lai atbilstu pieejamības standartiem. |
| Atļaut pielāgotu cenu | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, lietotājs var ievadīt pielāgoto cenu. |
| Minimālā cena | Vesels skaitlis | Šis rekvizīts ir piemērojams tikai tad, ja rekvizīts **Atļaut pielāgotu cenu** ir iestatīts kā **Patiess**. Tas definē minimālo cenu, ko lietotājs var ievadīt (piemēram, 1 $). |
| Maksimālā cena | Vesels skaitlis | Šis rekvizīts ir piemērojams tikai tad, ja rekvizīts **Atļaut pielāgotu cenu** ir iestatīts kā **Patiess**. Tas definē maksimālo cenu, ko lietotājs var ievadīt (piemēram, 1 000 $). |

## <a name="commerce-site-builder-settings"></a>Commerce vietnes veidotāja iestatījumi

Tāpat kā iegādes lodziņa modulī, ātrā skata modulī tiek ievēroti iestatījumi no **Vietnes iestatījumi \> Paplašinājumi \> Pievienot preci grozam**. Tomēr iestatījums **Doties uz lapu Grozs** tiek ignorēts, jo tas neatbilst ātrā skata moduļa mērķim, proti, lai lietotāji varētu pārlūkot vairākas preces saraksta lapā un pievienot tās grozam, neizejot no saraksta lapas.

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>Ātrā skata moduļa pievienošana preču kolekcijas modulim

Ātrā skata modulis var tikt pievienots preču kolekciju un meklēšanas rezultātu moduļiem.

Lai pievienotu ātrā skata moduli preču kolekciju modulim programmā Commerce vietnes veidotājs, veiciet tālāk norādītās darbības.

1. Dodieties uz **Lapas** un pēc tam atlasiet Fabrikam vietnes sakumlapu.
1. Dodieties uz **jebkuru mājas** lapas produktu kolekcijas moduli, atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet Ātro skatu **moduli un** pēc tam atlasiet **Labi**.
1. Moduļa **Ātrais skats** rekvizītu rūtī atlasiet **Virsraksts**. Dialoglodziņā **Virsraksts** iestatiet lauka **Virsraksta līmenis** vērtību uz **H2** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Iegādes lodziņa modulis](add-buy-box.md)

[Preču kolekciju modulis](product-collection-module-overview.md)

[Meklēšanas rezultātu modulis](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
