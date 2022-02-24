---
title: Preču kolekcijas moduļi
description: Šajā tēmā sniegts pārskats par preču kolekcijas moduļiem Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2d19cac142b870d8ecc677665443602b0a8837d2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413921"
---
# <a name="product-collection-modules"></a>Preču kolekcijas moduļi


[!include [banner](includes/banner.md)]

Šajā tēmā sniegts pārskats par preču kolekcijas moduļiem Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Preču atklāšana ir primārais rīks, ko mazumtirgotāji izmanto, lai piesaistītu klientu uzmanību e-tirdzniecības tīmekļa lapā. Preces kolekcijas moduļi palīdz mazumtirgotājiem veidot pārliecinošu iepirkšanās pieredzi, nodrošinot intuitīvu vizuālo interfeisu, ko var izmantot, lai ātri autorētu preču kolekcijas.

Preču kolekcijas moduļi attēlo fiziskas preces un pakalpojumus vietnē. Preču kolekcijas modulis parasti ir saistīts ar detalizētas informācijas lapu, kur klienti var iegādāties preci vai pakalpojumu vai uzzināt vairāk par to. 

Preču kolekciju avoti var būt tālāk minēto četru veidu saraksti:

- To preču redakcionālie saraksti, kas Dynamics 365 Commerce ir manuāli definētas kā ar preci vai preču sarakstu saistītās preces.
- Algoritmiskie saraksti, piemēram, jaunu, vispirktāko vai populāro preču saraksti.
- Ieteikumu saraksti, kas balstīti uz mašīnmācību.
- Personalizācijas saraksti, kas atbalsta personalizētus rezultātus klientam. Lai skatītu personalizētus rezultātus, klientiem ir jāpiesakās e-komercijas vietnē. Lietotāji-viesi neredz personalizētus rezultātus. Klienti var atteikties no personalizēšanas no [konta pārvaldības lapas](account-management.md).

Tālāk redzamajā attēlā parādīti dažādi preču kolekciju veidi, kas tiek izmantoti e-tirdzniecības vietnē.

![Dažāda veida preču kolekciju piemērs e-tirdzniecības vietnē](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Vienmēr izmantojiet preču kolekcijas moduļus, lai parādītu līdzīga veida preču grupu.

## <a name="product-collection-modules-and-types"></a>Preču kolekcijas moduļi un veidi

Tālāk redzamajā tabulā aprakstīti dažādi preču kolekcijas moduļu veidi Dynamics 365 Commerce.

| Preču kolekcijas modulis  | Tips | Apraksts |
|----------------------------|------|-------------|
| Kategorija                   | Kategorija | Šis modulis parāda preču sarakstu kategorijā, kā tas definēts navigācijas kategoriju hierarhijā, kuru mazumtirgotājs izveidoja kanālam. |
| Saistītie produkti           | Rediģēšana | Šis modulis parāda to preču sarakstu, ko pārdošanas vadītājs ir konfigurējis kā saistītās preces Commerce relāciju veidam, ko atlasījis autors. |
| Meklēšanas rezultāti             | Meklēšanas vaicājums | Šis preču kolekcijas moduļa veids parāda to preču sarakstu, kas vislabāk atbilst klienta ievadītajam meklēšanas vaicājumam. |
| Pārraudzīti preču saraksti      | Rediģēšana | Šis modulis rāda pielāgotus sarakstus, ko preču pārdevēji un redaktori ir izveidojuši programmā Commerce. |
| Jaunās                        | Algoritmisks | Šis modulis rāda sarakstu ar jaunākajām precēm, kas ir sašķirotas kanālos un katalogos. Šajā sarakstā var parādīt lietotāja, kas ir pierakstījies, personalizētus rezultātus, ja vietnes autors izvēlas šo opciju. |
| Vispirktākais               | Algoritmisks | Šis modulis rāda preču sarakstu, kas ir sarindotas pēc lielākā pārdošanas apjoma. Šajā sarakstā var parādīt lietotāja, kas ir pierakstījies, personalizētus rezultātus, ja vietnes autors izvēlas šo opciju. |
| Populāri                   | Algoritmisks | Šis modulis rāda visaugstākās veiktspējas preču sarakstu dotajā periodā. Šajā sarakstā var parādīt lietotāja, kas ir pierakstījies, personalizētus rezultātus, ja vietnes autors izvēlas šo opciju. |
| Bieži iegādāti kopā | Mākslīgais intelekts / mašīnmācība | Šis modulis izmanto mašīnmācību, lai analizētu patērētāju iepirkšanās veidu un ieteiktu saistītās preces, kas tiek bieži iegādātas kopā ar norādīto preci. Šajā sarakstā var parādīt lietotāja, kas ir pierakstījies, personalizētus rezultātus, ja vietnes autors izvēlas šo opciju. |
| Cilvēkiem patīk arī           | Mākslīgais intelekts / mašīnmācība | Šis modulis izmanto mašīnmācību, lai analizētu patērētāju iepirkšanās veidu un ieteiktu preces, kas ir saistītas ar norādīto preci. Šajā sarakstā var parādīt lietotāja, kas ir pierakstījies, personalizētus rezultātus, ja vietnes autors izvēlas šo opciju. |
| Ieteikumi              | Mākslīgais intelekts / mašīnmācība | Šis modulis izmanto mašīnmācīšanos, lai analizētu pierakstītā lietotāja pirkuma modeļus un sniegtu personalizētus ieteikumus, kas balstīti uz šiem pirkumu modeļiem. Lietotājam-viesim šis saraksts tiks sakļauts. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Preču kolekcijas moduļa pievienošana kategorijas lapai

Lai preču kolekcijas moduli pievienotu kategorijas lapai, veiciet tālāk minētās darbības.

1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet to pašu veidni, kas izmantota noklusējuma kategorijas lapā. Sadaļā **Lapas nosaukums** ievadiet atbilstošo nosaukumu un pēc tam atlasiet **Labi**.
1. Slotā **Apakšvirsraksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Preču kolekcija** un pēc tam atlasiet **Labi**.  
1. Preču kolekcijas moduļa rekvizītu rūtī atlasiet **Pievienot preču sarakstu**.
1. Dialoglodziņā **Atlasīt preču saraksta konfigurāciju** atlasiet saraksta veidu, saraksta avotu un ievadiet preču skaitu. Konfigurējiet visas citas opcijas, kas ir pieejamas saraksta tipam. Lai iegūtu vairāk informācijas par sarakstu veidiem, skatiet tālāk redzamo tabulu. 
1. Atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Tālāk redzamā tabula parāda sarakstu veidus, kas ir pieejami atlasei dialoglodziņā **Atlasīt preču saraksta konfigurāciju**.

| Tips                       | Apraksts | Lietojums | Lapas konteksts | Noteikts konteksts | Personalizēšana |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Preces pēc kategorijas       | Preču saraksts, kas pieder noteiktai kategorijai. Šī kategorija tiek noteikta vai nu no lapas konteksta, vai autora nodrošinātā konteksta. | Šo saraksta tipu var izmantot jebkurā lapā (piemēram, sākumlapā, kategorijas lapā, mārketinga lapā vai produkta detalizētas informācijas lapā \[PDP\]), lai reklamētu noteiktu kategoriju produktus. | Kategorija no lapas konteksta, ja tas ir pieejams (piemēram, kategorijas lapa) | Autors var nodrošināt konkrētu kategoriju kā konteksta sarakstu. | Nav attiecināms |
| Saistītie produkti           | Preču saraksts, ko pārdošanas vadītājs ir konfigurējis kā saistītās preces Commerce relāciju veidam. | Šis saraksta veids galvenokārt tiek izmantots PDP, bet to var izmantot jebkurā lapā, ja tiek nodrošināta pamatprece. | Produkts no lapas, relāciju tips (obligāts) | Produktu var atlasīt atlasītājā, un tiek izmantots relāciju veids. | Nav attiecināms |
| Pārraudzīts                    | Pielāgots saraksts, ko preču pārdevēji un redaktori ir izveidojuši programmā Commerce. | Kategorijas lapas, sākumlapas, izrakstīšanas un groza lapas, kā arī preču lapas papildināšana | Nav attiecināms | Nav attiecināms | Nav attiecināms |
| Algoritmisks                | <ul><li>**Jauns** — saraksts ar jaunākajām precēm, kas ir sašķirotas kanālos un katalogos.</li><li>**Vispirktākais** — preču saraksts, kas ir sarindotas pēc lielākā pārdošanas apjoma.</li><li>**Populārs** — visaugstākās veiktspējas preču saraksts dotajā periodā.</li></ul> | Sākumlapa, papildināta kategorijas lapa un izrakstīšanas un groza lapas | Kategorija no lapas konteksta, ja tas ir pieejams (piemēram, kategorijas lapa) | Kategorija, ko nosaka vietnes autors | Tiek atbalstīts |
| Bieži iegādāti kopā | Saraksts, kas izmanto mašīnmācību, lai analizētu patērētāju iepirkšanās veidu un ieteiktu saistītās preces, kas tiek bieži iegādātas kopā ar norādīto preci. | Šis saraksta veids ir attiecināms tikai uz groza lapu. | Grozs | Nav attiecināms | Tiek atbalstīts |
| Cilvēkiem patīk arī           | Saraksts, kas izmanto mašīnmācību, lai analizētu patērētāju iepirkšanās veidu un ieteiktu preces, kas ir saistītas ar norādīto preci. | Šis saraksta tips tiek izmantots PDP, lai parādītu preces, ko ir nopirkuši citi klienti. | Produkta konteksts no lapas | Prece, ko nodrošina vietnes autors | Tiek atbalstīts |
| Ieteikumi              | Saraksts, kas izmanto mašīnmācīšanos, lai noteiktu klientu preferences. | Šāda veida sarakstu var izmantot jebkurā lapā. | Nav attiecināms| Nav attiecināms | Tiek atbalstīts | 

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Karuseļa modulis](add-carousel.md)

[Satura bagātinātā bloka modulis](add-content-rich-block.md)

[Konteinera modulis](add-container-module.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Preču ieteikumu apskats](product-recommendations.md)
