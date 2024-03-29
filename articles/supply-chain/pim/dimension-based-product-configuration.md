---
title: No dimensijām atkarīgas preču konfigurācijas pārskats
description: No dimensijām atkarīga preču konfigurācija ir vienkāršs risinājums, kā no viena preces šablona un tā materiālu komplekta izveidot daudzus preču variantus.
author: t-benebo
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19821"
- intro-internal
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba11a561f320a7f4e787e4fe3f4e6f4fb88bbfb
ms.sourcegitcommit: ca73177dedf40df16860eaf88b1c701c61992028
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2022
ms.locfileid: "9754115"
---
# <a name="dimension-based-product-configuration-overview"></a>No dimensijām atkarīgas preču konfigurācijas pārskats

[!include [banner](../includes/banner.md)]

No dimensijām atkarīga preču konfigurācija ir vienkāršs risinājums, kā no viena preces šablona un tā materiālu komplekta izveidot daudzus preču variantus.

Preces konfigurācija atbilstoši dimensijām ir viena no trim preču konfigurācijas tehnoloģijām. Pārējās divas tehnoloģijas ir šādas: Iepriekš definēti varianti un Konfigurācija atbilstoši ierobežojumam. Visas trīs tehnoloģijas kā sākuma punktu izmanto preces šablonu un ļauj lietotājam izveidot daudz preču variantus vienam preces šablonam.

## <a name="key-concepts"></a>Galvenie principi
Preces konfigurācijas atbilstoši dimensijām pamatā ir tālāk minētie galvenie principi.

-   Preces šabloni
-   Preces dimensijas konfigurācija
-   Konfigurācijas grupas
-   Materiālu komplekts (BOM)
-   Konfigurācijas maršruts
-   Konfigurācijas noteikumi

### <a name="product-masters"></a>Preces šabloni

Preces šablons ir sākuma punkts jebkurā preces konfigurācijas procesā. Preces konfigurācijai atbilstoši dimensijām jāizmanto preces šablons ar konkrēto konfigurācijas tehnoloģiju un preces dimensiju grupa, kurā ietverta konfigurējamās preces dimensija.

### <a name="configuration-product-dimension"></a>Preces dimensijas konfigurācija

Konfigurējamās preces dimensija tiek izmantota, lai identificētu preces variantus preces šablonā, izmantojot konfigurācijas atbilstoši dimensijām tehnoloģiju. Konfigurācijas dimensijas vērtību ievada lietotājs, un tai būtu jāpalīdz identificēt atsevišķus preces variantus.

### <a name="configuration-groups"></a>Konfigurācijas grupas

Konfigurācijas grupas tiek definētas centrālajā repozitorijā un var tikt izmantotas visos no dimensijām atkarīgajos konfigurācijas modeļos. Konfigurācijas grupas tiek saistītas ar atsevišķam MK rindām un ietver tādu rindu grupu, kuras ir savstarpēji izslēdzošas. Tas nozīmē, ka katram preces variantam var atlasīt tikai vienu grupas rindu.

### <a name="bill-of-materials-bom"></a>Materiālu komplekts (BOM)

MK atspoguļo no dimensijam atkarīgas preces konfigurācijas veidošanas blokus. Tajā ir jāietver visas dažādās preces, ko var izmantot visiem preces variantiem. Katrai MK rinda var būt atsauce uz konfigurāciju grupu. Ja rindai nav atsauces uz konfigurāciju grupu, tā tiks iekļauta visos preces variantos.

### <a name="configuration-route"></a>Konfigurācijas maršruts

Konfigurācijas maršruts nosaka konfigurāciju grupu secību, kādā tās tiks parādītas lietotājam preces konfigurēšanas procesā.

### <a name="configuration-rules"></a>Konfigurācijas noteikumi

Konfigurācijas nosacījumi ir mehānisms, kas nodrošina, ka vienā MK konfigurāciju grupā iekļautā prece īsteno preces iekļaušanu vai izslēgšanu viena MK dažādās konfigurāciju grupās.

## <a name="product-modeling-process"></a>Preces modelēšanas process
Veidojot no dimensijas atkarīgas preces modeli, parastā darbību secība sākas ar saistīto konfigurāciju grupu definēšanu. Ir svarīgi pārliecināties, ka visas preces, kas tiks izmantotas MK, ir izlaistas uzņēmumam, kuram tiek veidots preces modelis. Izmantojot šos veidošanas blokus, lietotājs var izveidot MK un piešķirt konfigurāciju grupas visiem saistītajām MK rindām. Kad MK ir pabeigts, var definēt konfigurācijas maršrutu konfigurāciju grupu kārtošanai pareizā secībā. [![Uz dimensijām balstīts preču modelēšanas process.](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Ja dažādās konfigurāciju grupās ir noteiktas preces, kas ir jālieto kopā vai kuras nedrīkst lietot kopā, tad varat izveidot konfigurācijas nosacījumus, kas liks ievērot šo preču attiecības. Pēc tam, kad MK tiek saistīts ar no dimensijām atkarīgs preces šablonu, izmantojot MK versiju, un abi ir apstiprināti un aktivizēti, varat izveidot preces konfigurācijas un ievadīt nosaukumu katrai konfigurācijai. Konfigurācijas var definēt pirms tiek ģenerētas jebkādas transakcijas, vai arī to var izdarīt tad, kad rodas vajadzība pēc noteiktas konfigurācijas.

### <a name="suggested-use"></a>Ieteiktais pielietojums

Tehnoloģiju Konfigurācija atbilstoši dimensijām ieteicams lietot precēm ar ierobežotu mainīgumu, un noteikta preces varianta identificēšanai ir piemērota standarta preces dimensijs izmēru, krāsas, stila un konfigurācijas kombinācija. Piemēram, velosipēds ar rāmja augstumu, riteņu diametru, bremžu veidu un vairākiem pārnesumiem.

### <a name="next-step"></a><a name="sequence"></a>Nākošais solis

Nākamie astoņi uzdevumu ceļveži ir uzskaitīti tādā secībā, kādā jums tie ir jāizpilda. 

1.  [Uz dimensijas balstītas preces šablona izveide](tasks/create-dimension-based-product-master.md)
2.  [Uz dimensijas balstītas preces šablona izlaišana](tasks/release-dimension-based-product-master.md)
3.  [Pilnīga izlaistās preces šablona pamata iestatīšana](tasks/complete-basic-setup-released-product-master.md)
4.  [Konfigurācijas grupu definēšana](tasks/define-configuration-groups.md)
5.  [Materiālu komplekta izveide uz dimensiju balstītas preces šablonam](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Konfigurācijas maršrutu definēšana](tasks/define-configuration-route.md)
7.  [Konfigurācijas kārtulu izveide](tasks/create-configuration-rules.md)
8.  [Konfigurāciju izveide atbilstoši dimensijām](tasks/create-dimension-based-configurations.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]