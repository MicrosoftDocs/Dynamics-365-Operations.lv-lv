---
title: Preču kolekcijas moduļi
description: Šajā tēmā sniegts pārskats par preču kolekcijas moduļiem Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785471"
---
# <a name="product-collection-modules"></a>Preču kolekcijas moduļi  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā sniegts pārskats par preču kolekcijas moduļiem Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Preču atklāšana ir primārais rīks, ko mazumtirgotāji izmanto, lai piesaistītu klientu uzmanību e-tirdzniecības tīmekļa lapā. Preces kolekcijas moduļi palīdz mazumtirgotājiem veidot pārliecinošu iepirkšanās pieredzi, nodrošinot intuitīvu vizuālo interfeisu, ko var izmantot, lai ātri autorētu preču kolekcijas.

Preču kolekcijas moduļi attēlo fiziskas preces un pakalpojumus vietnē. Preču kolekcijas modulis parasti ir saistīts ar detalizētas informācijas lapu, kur klienti var iegādāties preci vai pakalpojumu vai uzzināt vairāk par to. 

Preču kolekciju avoti var būt tālāk minēto trīs veidu saraksti.

- To preču redakcionālie saraksti, kas Dynamics 365 Retail ir manuāli definētas kā ar preci vai preču sarakstu saistītās preces.
- Algoritmiskie saraksti, piemēram, jaunu, vispirktāko vai populāro preču saraksti.
- Ieteikumu saraksti, kas balstīti uz mašīnmācību.

Tālāk redzamajā attēlā parādīti dažādi preču kolekciju veidi, kas tiek izmantoti e-tirdzniecības vietnē.

![Dažāda veida preču kolekciju piemērs e-tirdzniecības vietnē](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Vienmēr izmantojiet preču kolekcijas moduļus, lai parādītu līdzīga veida vai tēmas preču grupu.

## <a name="product-collection-modules-and-types"></a>Preču kolekcijas moduļi un veidi

Tālāk redzamajā tabulā aprakstīti dažādi preču kolekcijas moduļu veidi Dynamics 365 Commerce.

| Preču kolekcijas modulis  | Tips | Apraksts |
|----------------------------|------|-------------|
| Kategoriju pārlūkošana            | Rediģēšana | Šis preču kolekcijas moduļa veids izmanto navigācijas kategoriju hierarhiju, ko mazumtirgotājs izveidojis mazumtirdzniecības kanālam, lai parādītu tādu preču pārlūkošanas plūsmu, kas tiek piedāvātas noteiktā vietnes kategorijā. |
| Meklēšanas rezultāti             | Meklēšanas vaicājums | Šis preču kolekcijas moduļa veids parāda to preču sarakstu, kas vislabāk atbilst klienta ievadītajam meklēšanas vaicājumam. |
| Saistītie produkti           | Rediģēšana | Šis preču kolekcijas moduļa veids parāda to preču sarakstu, ko pārdošanas vadītājs ir konfigurējis kā saistītās preces Retail relāciju veidam, ko atlasījis autors. |
| Pārraudzīti preču saraksti      | Rediģēšana | Šis preču kolekcijas moduļa veids parāda pielāgotus sarakstus, kurus preču pārdevēji un redaktori ir izveidojuši Retail. |
| Jaunās                        | Algoritmisks | Šis preču kolekcijas moduļa veids parāda jaunāko preču sarakstu, kas ir sašķirotas kanālos un katalogos. |
| Vispirktākais               | Algoritmisks | Šis preču kolekcijas moduļa veids parāda to preču sarakstu, kas ir sarindotas pēc lielākā pārdošanas apjoma. |
| Populāri                   | Algoritmisks | Šis preču kolekcijas moduļa veids parāda preču ar augstāku veiktspēju sarakstu noteiktā periodā. |
| Bieži iegādāti kopā | Mākslīgais intelekts / mašīnmācība | Šis preču kolekcijas modulis izmanto mašīnmācību, lai analizētu patērētāju iepirkšanās veidu un ieteiktu saistītās preces, kas tiek bieži iegādātas kopā ar norādīto preci. |
| Cilvēkiem patīk arī           | Mākslīgais intelekts / mašīnmācība | Šis preču kolekcijas modulis izmanto mašīnmācību, lai analizētu patērētāju iepirkšanās veidu un ieteiktu saistītās preces, kas ir saistīti ar norādīto preci. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Preču kolekcijas moduļa pievienošana kategorijas lapai

Lai preču kolekcijas moduli pievienotu kategorijas lapai, veiciet tālāk minētās darbības.

1. Dynamics 365 Commerce dodieties uz savu vietni un izveidojiet lapu, kas izmanto to pašu veidni, ko jūsu noklusējuma kategorijas lapa.
1. Lapas strukturējumā atlasiet slotu **Apakškājene**, atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet **Konteiners** un tad atlasiet **Labi**.
1. Konteinera modulī atlasiet daudzpunktes pogu un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet **Preču kolekcija** un tad atlasiet **Labi**.
1. Konfigurējiet iestatījumus, atlasot atbilstošu datu avotu un preču kolekcijas ievadi.
1. Preču kolekcijas moduļa rekvizītu rūtī atlasiet **Pievienot preču sarakstu**.
1. Dialoglodziņā **Atlasīt preču saraksta konfigurāciju** atlasiet saraksta veidu, ievadiet preču skaitu un atlasiet visas citas opcijas, kas ir pieejamas saraksta veidam. Lai iegūtu vairāk informācijas par sarakstu veidiem, skatiet tālāk redzamo tabulu. 
1. Atlasiet **Labi**.
1. Saglabājiet lapu un reģistrējiet to.

Tālāk redzamā tabula parāda sarakstu veidus, kas ir pieejami atlasei dialoglodziņā **Atlasīt preču saraksta konfigurāciju**.
   
| Tips                       | Apraksts | Vispārējā prakse | Konteksts, ko var iegūt no lapas konteksta | Konteksts, ar ko autors var ignorēt lapas kontekstu |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| Preces pēc kategorijas       | Preču saraksts, kas pieder noteiktai kategorijai. Šī kategorija tiek noteikta vai nu no lapas konteksta, vai autora nodrošinātā konteksta. | Kategorijas lapas, sākumlapas, izrakstīšanas un groza lapas, kā arī preču lapas papildināšana | Kategorija | Kategorija, ko nosaka autors |
| Saistītie produkti           | Preču saraksts, ko pārdošanas vadītājs ir konfigurējis kā saistītās preces Retail relāciju veidam. | Preču lapas, izrakstīšanas un groza lapas, vēlmju saraksta lapa un klienta konta lapa | Prece, relāciju veids (obligāts)  | Prece, relāciju veids |
| Pārraudzīts                    | Pielāgots saraksts, ko preču pārdevēji un redaktori ir izveidojuši Retail. | Kategorijas lapas, sākumlapas, izrakstīšanas un groza lapas, kā arī preču lapas papildināšana | Nav attiecināms | Lapas izvēlētājs |
| Algoritmisks                | <ul><li>**Jauns** — saraksts ar jaunākajām precēm, kas ir sašķirotas kanālos un katalogos.</li><li>**Vispirktākais** — preču saraksts, kas ir sarindotas pēc lielākā pārdošanas apjoma.</li><li>**Populārs** — visaugstākās veiktspējas preču saraksts dotajā periodā.</li></ul> | Sākumlapa, papildināta kategorijas lapa un izrakstīšanas un groza lapas | Kategorija | Kategorija, ko nosaka autors |
| Bieži iegādāti kopā | Saraksts, kas izmanto mašīnmācību, lai analizētu patērētāju iepirkšanās veidu un ieteiktu saistītās preces, kas tiek bieži iegādātas kopā ar norādīto preci. | Preču lapas un izrakstīšanās un groza lapas | Prece, grozs | Iekļaut grozu |
| Cilvēkiem patīk arī           | Saraksts, kas izmanto mašīnmācību, lai analizētu patērētāju iepirkšanās veidu un ieteiktu preces, kas ir saistītas ar norādīto preci. | Preču lapas un izrakstīšanās un groza lapas | Prece, grozs | Nav attiecināms |

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Karuseļa modulis](add-carousel.md)

[Bagātinātā satura bloka modulis](add-content-rich-block.md)

[Satura izvietojuma modulis](add-content-placement-modules.md)

[Container modulis](add-container-module.md)

[Iegādes lodziņa modulis](add-buy-box.md)

