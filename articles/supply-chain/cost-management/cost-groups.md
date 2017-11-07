---
title: Izmaksu grupas
description: "Izmaksu grupas sniedz pamatu izmaksu seguma segmentēšanai un analīzei ražotā krājuma aprēķinātajā izmaksā, kā, piemēram, materiālu, darba un papildus atbalsta izmaksu segumus. Izmaksu grupu segmentācijai ir vairāki sinonīmi, kā, piemēram, izmaksu sadalīšana, izmaksu dekompozīcija vai izmaksu klasifikācija."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCostGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 022cca99bc5ad1f4c023b0b7aba748a2ef6b1d60
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="cost-groups"></a>Izmaksu grupas

[!include[banner](../includes/banner.md)]


Izmaksu grupas sniedz pamatu izmaksu seguma segmentēšanai un analīzei ražotā krājuma aprēķinātajā izmaksā, kā, piemēram, materiālu, darba un papildus atbalsta izmaksu segumus. Izmaksu grupu segmentācijai ir vairāki sinonīmi, kā, piemēram, izmaksu sadalīšana, izmaksu dekompozīcija vai izmaksu klasifikācija. 

Izmaksu grupu segmentācijai ir vairāki sinonīmi, kā, piemēram, izmaksu sadalīšana, izmaksu dekompozīcija vai izmaksu klasifikācija. Izmaksu grupu segmentāciju var izmantot vairākiem mērķiem. Daži piemēri:

-   Var tikt veiktas segmenta izmaksas dažādiem materiāla tipiem, piemēram, sastāvdaļas un iepakojuma materiāls konservētam produktam, balstīts uz krājumiem piešķirtajām izmaksu grupām.
-   Var tikt veiktas segmenta izmaksas operācijas resursiem, piemēram, dažādiem darba un mašinērijas tipiem, pamatojoties uz izmaksu grupām, kas piešķirtas ar operācijas resursiem un maršrutēšanas darbībām saistītām izmaksu kategorijām.
-   Var tikt veiktas segmenta izmaksas maršrutēšanas operāciju laika iestatīšanai un izpildes laikam, pamatojoties uz izmaksu grupām, kas piešķirtas ar maršrutēšanas darbībām saistītām cenu kategorijām.
-   Var tikt veiktas segmenta izmaksas dažādiem papildu atbalsta tipiem, piemēram, ar darbu saistītam un ar mašinēriju saistītam atbalstam, pamatojoties uz izmaksu grupām, kas piešķirtas netiešām izmaksām izmaksu lapas iestatīšanā.
-   Var tikt izmantots dažādu ražošanas veidu pieskaitāmo izmaksu aprēķināšanai izmaksu aprēķināšanas lapas iestatīšanā. Var ietvert dažādu veidu pieskaitāmās izmaksas, kas saistītas ar maršrutēšanas informāciju par darbību resursiem vai ar informāciju par iestatīšanas un izpildes laiku. Ražošanas papildu atbalsts var tikt saistīts arī ar sastāvdaļas materiālu izmaksu segumu, atspoguļojot bezatlikumu ražošanas filozofiju, kas izslēdz nepieciešamību pēc maršrutēšanas informācijas.

Izmaksu grupu segmentācija attiecas arī uz ražotā krājuma aprēķinātajām izmaksām neatkarīgi no tā, vai izmaksu pamatā bija standarta vai plānotās izmaksas. Lapa **Kopsavilkums** parāda šo segmentāciju, vadoties pēc izmaksu grupas, pēc līmeņa vai abiem. 

Spēja saglabāt izmaksas grupu segmentāciju vairākos produktu struktūras līmeņos tiek dēvēta par *sadalīšanu*. Sadalīšana attiecas tikai uz ražotajiem krājumiem, kas izmanto standarta izmaksu inventarizācijas modeli. Ja sadalīšanu neizmanto, ražoto sastāvdaļu izmaksas tiek uzskatītas par materiāla izmaksu segumu. Uzkrājumu parametrs izmaksu sadalījumam pēc apakšgrāmatas norāda, ka standarta izmaksu aprēķinos izmaksu grupu segmentācija tiks saglabāta vairākos līmeņos. Turpretim, ja politikai nav līmeņu, izmaksu grupu segmentācija attiecas tikai uz viena līmeņa aprēķiniem. Piemēram, lapā **Izmaksu izvērsums pa izmaksu grupām** ir parādīta cenu grupu segmentācija starp vairākiem līmeņiem standarta cenu krājumiem. 

Izmaksu grupas segmentācija var attiekties uz krājuma standarta izmaksu novirzēm. Otrs krājumu parametrs nosaka, vai novirzes tiks identificētas pēc izmaksu grupas vai vienkārši apkopotas. 

Izmaksu grupai var tikt piešķirts izmaksu grupas tips un uzvedība papildus segmentācijas mērķiem.

-   **Izmaksu grupas tips** — katrai izmaksu grupai ir jāpiešķir izmaksu grupas tips, lai norādītu, ka izmaksu grupa attiecas uz tiešu materiālu, tiešu ražošanu, tiešiem ārpakalpojumiem vai attiecas uz netiešu vai nedefinētu materiālu, ražošanu un ārpakalpojumiem. Izmaksu grupa, kas norādīta kā tiešs materiāls, var tikt piešķirta krājumiem. Tiešas ražošanas izmaksu grupa var tikt piešķirta izmaksu kategorijām. Tiešā ārpakalpojumu izmaksu grupa var tikt piešķirta pakalpojuma preces veidam, kas ļauj klasificēt ar pakalpojuma iegādi saistītas izmaksas ar pakalpojumu apakšlīgumu slēgšanas darbībām. Netieša izmaksu grupa var tikt piešķirta papildizdevumu vai nodokļu netiešajām izmaksām. Izmaksu grupa, kas norādīta kā netieša, var tikt piešķirta krājumiem, izmaksu kategorijām vai netiešajām izmaksām. Izmaksu grupu veida piešķiršana kalpo vairākiem mērķiem. Pirmkārt, tā ierobežo iespēju piešķirt izmaksu grupu un skatīt piemēroto izmaksu grupu sarakstu. Otrkārt, tā sniedz papildus segmentāciju pārskatīšanas mērķiem. Treškārt, tā var tikt izmantota, lai piešķirtu virsgrāmatas kontus novirzēm.
-   **Darbība** — katrai izmaksu grupai neobligāti var tikt piešķirta darbība, lai norādītu uz izmaksu grupu kā piederošu fiksētajām vai mainīgām izmaksām. Izmaksu grupa, kuras uzvedības vērtība ir nulle, tiek pieskaitīta pie mainīgajām izmaksām. Darbības piešķiršanu izmanto tikai atskaites mērķiem. Piemēram: izmaksas var tikt parādītas ar fiksēto un mainīgo izmaksu segmentāciju izmaksu lapā un lapā**Izmaksu izvērsums pa izmaksu grupām**. Peļņas procentu iestatījumu piešķiršana katrai izmaksu grupai padara iespējamu materiālu komplekta (MK) aprēķinu, kas nodrošina ieteicamo pārdošanas cenu, kas pamatojas uz pieeju izmaksas-plus-uzcenojums.





