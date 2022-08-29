---
title: Konfigurēt preču dimensiju vērtības, lai tās tiktu rādītas kā paraugi
description: Šajā rakstā ir aprakstīts, kā konfigurēt preču dimensiju vērtības kā ieejas ieejas punktus Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: e81c1f03eb6387176ca5ce8f751ce53aa0261679
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271995"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>Konfigurēt preču dimensiju vērtības, lai tās tiktu rādītas kā paraugi

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā konfigurēt preču dimensiju vērtības kā ieejas ieejas punktus Microsoft Dynamics 365 Commerce. Lai iegūtu informāciju par produktu dimensijām, skatiet [Produktu dimensijas](../../supply-chain/pim/product-dimensions.md).

Dynamics 365 Commerce atbalsta izmēru, stilu un krāsu dimensiju izmantošanu, lai attēlotu preces variantus. Preču dimensijām ir draudzīgi nosaukumi, kas tiek rādīti preču informācijas lapās (PDP), lai varētu atlasīt preces variantus. Šo draudzīgo nosaukumu piemēri ir "Mazs", "Vidējs" un "Liels" izmēriem un "Melns" un "Brūns" krāsām. Tomēr, ja prece atbalsta daudzas variācijas, ir nepieciešamas vairākas atlases, lai skatītu attēlu preces variantam. Tāpēc klientiem tas var būt lēns un garlaicīgs process pārlūkot un atlasīt preces variantus.

Ja PDP dimensijas tiek rādītas kā paraugi, klienti saņem preču variāciju vizuālu priekšskatījumu. Viņi var viegli pārlūkot dažādas krāsas, rakstus un faktūras, kā arī ātri apskatīt dažādas preču variāciju kombinācijas.

Displeja dimensijas kā paraugu funkcija ļauj Commerce izmantot heksadecimālos kodus un attēlus, lai dimensijas parādītu kā paraugus. Turklāt līdzīgas dimensijas, piemēram, krāsas, var grupēt preču saraksta lapās. Piemēram, klients meklē preces zila krāsā. Ja dažādas zilās dimensijas vērtības ir sagrupētas kopā, meklēšanas rezultātu saraksta lapā tiek rādītas preces ar dažādiem zilās krāsas toņiem. Dimensiju grupēšana ievērojami uzlabo preču uzlabošanas iespējas un palīdz klientiem atrast vairāk preču, izmantojot vienas preces meklēšanas vaicājumu.

> [!NOTE]
> Displeja izmēri kā paraugu funkcija ir pieejama no programmas Dynamics 365 Commerce 10.0.20 versijas laidiena.

Nākamajā attēlā ir parādīts piemērs, kur e-komercijas vietnes PDP krāsas parādās kā paraugi.

![Krāsu piemērs, kas preces informācijas lapā tiek rādītas kā paraugi.](../dev-itpro/media/swatch_pdp.png)

Nākamajā attēlā ir parādīts piemērs, kur e-komercijas vietnes meklēšanas rezultātu saraksta lapā krāsas parādās kā paraugi.

![Krāsu piemērs, kas meklēšanas rezultātu saraksta lapā tiek rādītas kā paraugi.](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>Commerce Headquarters iespējojiet displeja izmērus kā paraugus

Lai iespējotu displeja dimensiju kā paraugu līdzekli programmā Commerce Headquarters, dodieties uz **Darbvietas \> Līdzekļu pārvaldība** un ieslēdziet līdzekli **Iespējot attēlu atbalstu preču dimensiju vērtībām**. Ja šis līdzekļa karodziņš ir iespējots, atbilstošajās Commerce Headquarters tabulās katrai dimensijai tiek pievienoti trīs jauni lauki: **Heksadecimālais kods**, **URL** (attēliem) un **RefinerGroup**.

## <a name="configure-dimension-values-in-commerce-headquarters"></a>Dimensiju vērtību konfigurēšana programmā Commerce Headquarters

Displeja izmēri kā paraugu līdzeklis tiek atbalstīts izmēram, stilam un krāsu dimensijām. Heksadecimālā koda un attēla URL vērtības atbilstošajām dimensijām var norādīt programmā Commerce Headquarters. Pēc noklusējuma, ja dimensijai nav norādītas heksadecimālā koda un attēla URL vērtības, sistēma rādīs dimensijas draudzīgā nosaukuma tekstu.

Konfigurāciju var veikt jebkurā no šiem līmeņiem:

- **Dimensija** - programmā Commerce Headquarters atveriet dimensijas lapu, meklējot **Krāsu**, **Izmēru** vai **Stilu**. Katrā lappusē režģis uzskaita dimensiju vērtības. Varat pārvaldīt rādīšanas secību, heksadecimālo kodu un attēla URL vērtības. Tālāk redzamajā attēlā ir parādīts lapas **Krāsas** konfigurācijas piemērs.

    ![Dimensiju konfigurācijas piemērs lapā Krāsas.](../dev-itpro/media/swatch_Color.PNG)

- **Dimensiju grupa** - programmā Dynamics 365 Commerce var izmantot rekvizītu **RefinerGroup**, lai izveidotu dimensiju grupas. Ja ir definētas dimensiju grupas, atveriet atbilstošo lappusi, meklējot **Krāsu grupu**, **Izmēru grupu** vai **Stila grupu**. Katrā lapā varat pārvaldīt heksadecimālo kodu, attēla URL un precizētāju grupas vērtības. Tālāk redzamajā attēlā ir parādīts lapas **Krāsu grupas** konfigurācijas piemērs.

    ![Dimensiju konfigurācijas piemērs lapā Krāsu grupas.](../dev-itpro/media/swatch_colorGroup.PNG)

- **Preces dimensija (preces izveides laikā)** – veidojot jaunu preci, dimensiju vērtību ievadīšanai var izmantot lapu **Preču dimensijas**. Esošajām precēm lauki **Heksadecimālais kods**, **URL** (attēliem) un **RefinerGroup**, iespējams, jau ir iestatīti. Tomēr, jūs varat mainīt vērtības pēc nepieciešamības. Tālāk redzamajā attēlā ir parādīts lapas **Preču dimensijas** konfigurācijas piemērs.

    ![Dimensiju konfigurācijas piemērs lapā Preču dimensijas.](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> Heksadecimālā koda un attēla URL konfigurāciju pārvaldības process atbilst tam pašam modelim, kas tiek izmantots, lai pārvaldītu dimensiju parādīšanas secību.

## <a name="configure-dimension-values-by-using-hex-codes"></a>Dimensiju vērtību konfigurēšana, izmantojot heksadecimālos kodus

Lielākajai daļai krāsu dimensiju programmā Commerce Headquarters dimensiju lapās jānorāda heksadecimālā koda krāsas vērtība. Piemēram, melnās krāsas heksadecimālā koda vērtībai jābūt **#00000**. Kad Commerce atveido vietnes lapu, heksadecimālais kods tiek attēlots ar krāsainu paraugu.

Nākamajā attēlā ir parādīts piemērs, kur krāsu dimensijas tiek konfigurētas, izmantojot heksadecimālā koda vērtības.

![Dimensiju konfigurācijas piemērs, kas izmanto heksadecimālos kodus.](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>Dimensiju vērtību konfigurēšana, izmantojot attēlu URL

Dažas krāsu dimensijas attēlo rakstus, nevis tīrtoņa krāsas. Piemēram, krāsu dimensiju var raksturot kā "leopardu". Šādos gadījumos jūs varat efektīvāk attēlot krāsu izmērus, izmantojot publicētus attēlus, nevis heksadecimālos kodus.

Katrs attēls ir jāaugšupielādē Commerce vietņu veidotājā un jāpublicē. Pēc tam ievadiet publicētā attēla URL atbilstošajā dimensiju lapā programmā Commerce Headquarters. Ja dimensija ir atlasīta parādīšanai kā paraugs, bet heksadecimālais kods nav definēts, Commerce veiks attēla meklēšanu, atveidojot lapu. Ja attēla uzmeklēšana neizdodas, Commerce rādīs dimensijas nosaukuma tekstu.

Tālāk redzamajā attēlā ir parādīts piemērs, kur attēla URL tiek izmantoti konfigurācijai lapā **Krāsas**.

![Dimensiju konfigurācijas piemērs, kas izmanto attēla URL.](../dev-itpro/media/swatch_color_urls.PNG)

Varat izmantot multivides veidni, lai definētu attēlu URL, tāpat kā preču un kategoriju attēlus. Augšupielādējot attēlus vietņu veidotājā, failu nosaukumu konvencijām un failu ceļiem jābūt saskanīgiem.

Tālāk redzamajā attēlā ir parādīts piemērs, kur attēla URL tiek izmantoti multivides veidnes konfigurācijai.

![Multivides veidnes konfigurācijas piemērs.](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>Dimensiju vērtību konfigurēšana, izmantojot gan heksadecimālos kodus, gan attēlu URL

Lielākajai daļai krāsu dimensiju var konfigurēt gan heksadecimālos kodus, gan attēla URL. Commerce atveidošanas rezerves loģika automātiski meklēs heksadecimālos kodus vai attēla URL, lai parādītu krāsu paraugu. Izmantojot gan heksadecimālos kodus, gan attēla URL, krāsu dimensiju konfigurēšanai var vienkāršot attēlu pārvaldību, ja ir liels krāsu skaits.

Tālāk redzamajā attēlā ir parādīts piemērs, kur lapā **Krāsas** konfigurācijai tiek izmantoti gan heksadecimālie kodi, gan attēla URL.

![Dimensiju konfigurācijas piemērs, kas izmanto gan heksadecimālos kodus, gan attēla URL.](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>Konfigurēt precizētāju grupas

Definējot heksadecimālo kodu vai attēla URL dimensijas vērtībai, var norādīt arī lauka **RefinerGroup** vērtību. Šis lauks definē dimensiju, kas jāizmanto, lai grupētu līdzīgas dimensiju vērtības precizētāju pieredzē.

Piemēram, ja krāsu dimensiju vērtības ir "blue", "blue plaid", "blue wash" un "dark blue", katra vērtība tiek kartēta uz citu heksadecimālo kodu vai attēla URL. Tādēļ katra vērtība atbilstošo preču PDP un preču kartēs parādīsies kā atšķirīga krāsa. Tomēr, ja visas šīs krāsu dimensiju vērtības kartējat uz **Blue** vērtību **RefinerGroup**, meklējot "blue" preces tiks ģenerēti saraksta lapu meklēšanas rezultāti produktiem, kuru izmēru krāsu vērtības ir "blue," "blue plaid," "blue wash" un "dark blue".

Nākamajā attēlā redzamajā piemērā ir parādīta attiecība starp rekvizītiem **Krāsa** un **RefinerGroup** programmā Commerce Headquarters.

![Precizētāju grupas pārvaldības piemērs.](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>Pārvaldīt attēlus Commerce vietnes veidotājā

Ja attēlu URL tiek izmantoti jebkurām dimensiju vērtībām, atbilstošie attēli ir jāaugšupielādē Commerce vietnes veidotājā. Katra attēla atrašanās vietai jāatbilst faila nosaukumam un mapes ceļam, kas attēlam ir definēts programmā Commerce Headquarters. Attēlu faili ir jāaugšupielādē atbilstošajās vietņu veidotāja kategoriju atrašanās vietās. Piemēram, krāsu attēli ir jāaugšupielādē **Krāsu** kategorijas mapē. Papildinformāciju par to, kā augšupielādēt attēlus vietnes veidotājā, skatiet [Augšupielādēt attēlus](../dam-upload-images.md).

Nākamajā attēlā ir parādīts piemērs, kur dialoglodziņš **Augšupielādēt attēlus** tiek izmantots, lai augšupielādētu attēlus vietnes veidotāja multivides bibliotēkā. Tajā ir iezīmētas kategorijas **Izmērs**, **Krāsa** un **Stils**, kas ir pieejamas atlasei.

![Attēlu failu kategoriju piemērs augšupielādes laikā vietņu veidotāja multivides bibliotēkā.](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>Iespējot paraugu parādīšanu e-komercijas vietnes lapās

Lai paraugi varētu parādīties e-komercijas vietnes lapās, kurām nepieciešama dimensiju atlase, piemēram, PDP un saraksta lapās, programmā Commerce Headquarters ir jākonfigurē dimensiju vietnes iestatījumi. Papildinformāciju skatiet sadaļā [Lietot dimensijas vietnes iestatījumus](../dimension-settings.md).

Turklāt meklēšanas rezultātu moduļiem ir jāiespējo rekvizīts **Iekļaut preces atribūtus meklēšanas rezultātos**. Ja vietne izmanto pielāgotas kategoriju lapas, ir jāatjaunina šajās lapās izmantotie meklēšanas rezultātu moduļi, lai būtu iespējots rekvizīts **Iekļaut preču atribūtus meklēšanas rezultātos**. Plašāku informāciju skatiet sadaļā [Meklēšanas rezultātu modulis](../search-result-module.md).

## <a name="inventory-awareness-on-swatches"></a>Krājumu apzināšana attiecībā uz krājumiem

Funkcijai Krājumi ir izvēles iespēja rādīt preces varianta krāsas vai dimensijas krājumu pieejamību. Piemēram, prece tiek pārdota vairākos izmēros, bet daži izmēri nav noliktavā. Šajā gadījumā preces, kas nav krājumā, tiek renderētas atšķirīgi, lai norādītu, ka tās nav pieejamas. Šī iespēja palīdz samazināt klientu noklikšķināto skaitu, kas nepieciešams preču pieejamības noteikšanai.

Krājuma pieejamības līdzekli var konfigurēt lietošanai gan PDP, gan meklēšanas vai kategoriju saraksta lapās, kur tiek parādīti krājumi. Lai to aktivizētu, šis dimensiju atlases rekvizīts **Atjaunināt datu nesēju** jāiestata uz **Patiess** [plašsaziņas nesēja modulī](../media-gallery-module.md). Šis iestatījums iespējo mediju galerijas attēlu atjaunināšanu, kad tiek atlasītas dimensijas. 

> [!IMPORTANT]
> Rekvizīts Iespējot vieslietotājiem ir pieejams kā Commerce 10.0.21 laidiena versijā. Nepieciešams, lai būtu instalēta Commerce moduļa bibliotēkas pakotnes versija 9.31.

Šajā attēlā parādīts PDP lieluma pārzzināšanas piemērs par krājumu apzināšanos.

![Piemērs krājumu apzināšanai PDP izmēra darbībās](../dev-itpro/media/swatch_inventory.png)

## <a name="display-swatches-in-pos-and-other-channels"></a>Rādīt paraugus POS un citos kanālos

Pakalpojumā Commerce pašlaik nav pieejama "out-of-box" ieviešana, kas atbalsta paraugu parādīšanu pārdošanas punktos (POS) un citos kanālos. Tomēr varat ieviest parauga parādīšanas funkcionalitāti kā paplašinājumu, kas kanāla API liek atgriezt heksadecimālos kodus un attēlu URL, kas nepieciešami, lai atveidotu paraugus.

## <a name="additional-resources"></a>Papildu resursi

[Meklēšanas rezultātu modulis](../search-result-module.md)

[Lietot vietnes iestatījumus dimensijām](../dimension-settings.md)

[Preces dimensijas](../../supply-chain/pim/product-dimensions.md)

[Augšupielādēt attēlu](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
