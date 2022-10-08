---
title: Preču salīdzinājuma moduļi
description: Šajā rakstā ir aprakstīti preču salīdzinājuma moduļi un veids, kā tos ieviest, lai debitori varētu veikt preču salīdzinājumus Microsoft Dynamics 365 Commerce e-komercijas vietnēs.
author: ashishmsft
ms.date: 10/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 9ff45f3fbcc86b21f336d580582adef586417de4
ms.sourcegitcommit: 66b954827826706ea2ba00c2afd5d694ad92148d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2022
ms.locfileid: "9618390"
---
# <a name="product-comparison-modules"></a>Preču salīdzinājuma moduļi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti preču salīdzinājuma moduļi un veids, kā tos ieviest, lai debitori varētu veikt preču salīdzinājumus Microsoft Dynamics 365 Commerce e-komercijas vietnēs.

> [!NOTE]
> Preču salīdzināšanas un preču salīdzinājuma pogu moduļi ir pieejami no Dynamics 365 Commerce versijas 10.0.29 versijas versijas izlaides. Tos var izmantot gan bizness-patērētājam (B2C), gan "bizness-biznesam" (B2B) vietnēm.

Produktu salīdzinājuma funkcionalitāte ļauj veikalam salīdzināt preču detaļas preču salīdzinājuma lapā, lai palīdzētu veikt labākus pirkuma lēmumus. Šī funkcionalitāte ir konfigurēta Commerce Site Builder, izmantojot preču salīdzināšanas moduli. Produktu saraksta lapās (PLP), piemēram, kategoriju rezultātos, meklēšanas rezultātos un produktu kolekciju lapās, varat konfigurēt pogu preču salīdzināšanai, kas ļauj pircējiem pievienot preces salīdzinājuma teknim. Šī funkcionalitāte tiek konfigurēta vietas veidotājā, izmantojot preču salīdzinājuma pogas moduli, kas darbojas kā ātrā [skata modulis](quick-view-module.md).

Kad vietas lietotāji pievieno preces salīdzināšanai, atlasot tās produktu pie cenas, lapas apakšā tiek parādīts salīdzinājuma teknis. Salīdzinājuma teknis parāda preces, ko pircējs pašlaik salīdzina kopā ar īsu preču priekšskatījumu. Vietnes lietotāji var arī pievienot preces no preču informācijas lapām (PDP), un viņi var pievienot specifiskus preces variantus, lai tos salīdzinātu ar preču šabloniem.

Kad debitori salīdzinājuma teknim pievienojat dažas preces, viņi var atlasīt Salīdzināt, **lai** novirzītu uz preču salīdzinājuma lapu. Preču salīdzinājuma lapā ir redzama detalizēta informācija par katras atlasītās preces precēm, lai debitori varētu salīdzināt attēlus, cenas, preču dimensijas (izmēru, stilu un krāsu), apkopoto novērtējumu informāciju un citas preces īpašības.

Šajā attēlā redzami salīdzināšanas preču pogas piemēri, salīdzinājuma pogas noņemšana no salīdzinājuma, salīdzinājuma tekni un preču salīdzinājuma lapa.

![Preču salīdzinājuma pārskats, kas rāda salīdzinājuma preces pogu, izņemamu no salīdzinājuma pogas, salīdzinājuma tekni paneli un preču salīdzinājuma lapu.](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - Preču salīdzinājuma lapa salīdzina noklusējuma preču rekvizītu kopu un visas īpašības, ko var skatīt konkrētā produkta PDP.
> - Preču salīdzinājuma lapā nevar skatīt tādus rekvizītus kā piegādes veids, rīcībā esošie krājumi un mērvienība.
> - Debitori var salīdzinājuma teknim pievienot preces no dažādām kategorijām, ja preces ir no viena kataloga.
> - Preču salīdzinājuma funkcionalitāte pašlaik ir ierobežota, lai salīdzinātu preces atsevišķā katalogā. Vietas lietotāji nevar veikt katalogu salīdzinājumus.
> - Vajadzētu nodrošināt, ka visiem **preču salīdzināšanas moduļiem** tiek notīrīts renderēšanas moduļa klienta puses rekvizīts.
> - Jums jānodrošina, lai lapu līmeņa kešatmiņa tiktu atspējota visām lapām, kur tiek izmantots preču salīdzinājuma modulis. Šīs lapas ietver PDP, PLP un preču salīdzinājuma lapas. Papildinformāciju skatiet lapās kešdarbes [konfigurēšana](e-commerce-extensibility/page-caching.md).

Šajā attēlā parādīts preču salīdzinājuma lapas piemērs.

![Preču salīdzinājuma lapa.](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>Pievienot preču salīdzinājuma moduli jaunai preču salīdzinājuma lapai

Jūs varat izveidot atvēlētu preču salīdzinājuma lapu, lapas pamattekstam pievienojot preču salīdzinājuma moduli. Papildus klientu iespējošanai, lai salīdzinātu dažādu preču preču detaļas, varat konfigurēt preču salīdzinājuma moduli, lai sniegtu debitoriem opciju ātri pabeigt pirkumu pēc preču salīdzināšanas. Preču salīdzinājuma modulī ir arī **tukšs** salīdzinājuma slots, kur varat pievienot satura bloka moduli, kas apraksta tukšu stāvokli (piemēram, "Preču salīdzinājums ir tukšs").

Lai pievienotu preču salīdzinājuma moduli jaunai preču salīdzinājuma lapai, sekojiet šiem soļiem.

1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā Izveidot **jaunu lapas dialoglodziņu ar** lapas nosaukumu ievadiet **atbilstošu** lapas nosaukumu (piemēram, **Preču** salīdzinājums) un pēc tam atlasiet **Tālāk**.
1. Zem **Izvēlēties veidni**, atlasiet atbilstošu veidni (piemēram, veidni, kas tiek izmantota ar noklusējuma kategorijas lapu), un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Izvēlēties izkārtojumu atlasiet** lapas izkārtojumu (piemēram, Elastīgs **izkārtojums**) un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Pārskatīt un pabeigt** pārskatiet lapas konfigurāciju. Ja jārediģē lapas informācija, atlasiet **Atpakaļ**. Ja lapas informācija ir pareiza, atlasiet Izveidot **lapu**.
1. Galvenajā slotā **atlasiet** daudzpunkti (**...) un** pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Konteiners **un** pēc tam atlasiet **Labi**.
1. Konteinera slotā **atlasiet** daudzpunkti (**...) un** pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet preču salīdzinājuma **moduli** un pēc tam atlasiet **Labi**.
1. Ātrā skata **pogu slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet preces ātrās skatīšanas **moduli** un pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī labajā pusē konfigurējiet preces ātrās skatīšanas **moduļa** rekvizītus.
1. Tukšajā **salīdzinājuma slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet satura bloķēšanas **moduli** un pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī labajā pusē konfigurējiet satura bloka **moduļa** rekvizītus. 
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Šajā attēlā parādīts tukšas salīdzinājuma lapas piemērs vietu veidotājā.

![Preču salīdzināšanas modulis.](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Meklēšanas un kategorijas rezultātu lapās pievienot preces salīdzinājuma pogu

Preču salīdzinājuma poga ļauj lietotājiem ātri pievienot preci salīdzinājuma teknim, pārlūkojot preces saraksta lapā. Viņi var pievienot vienu vai vairākas preces salīdzinājuma tekni no saraksta lapas bez nepieciešamības doties uz PDP.

Preču salīdzinājuma pogu atbalsta preču kolekcija, meklēšanas rezultāti un PDP pirkšanas kastē moduļi.

Lai meklēšanas un kategorijas rezultātu lapām pievienotu preču salīdzinājuma pogu, rīkojieties šādi.

1. Vietas veidotājā atveriet sadaļu **Lapas** un atveriet kategorijas lapu, kurai vēlaties pievienot preču salīdzinājuma pogu.
1. Galvenajā slotā **atlasiet** daudzpunkti (**...) un** pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet meklēšanas rezultātu **moduli** un pēc tam atlasiet **Labi**.
1. Meklēšanas rezultātu **moduļa** Preču salīdzinājuma pogu **slotā** atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet preču salīdzinājuma **pogu moduli un** pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī labajā pusē konfigurējiet Preču salīdzinājuma **pogas moduļa** rekvizītus.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="add-a-product-comparison-preview-panel-module-to-pages-on-your-website"></a>Pievienot preču salīdzinājuma priekšskatījuma paneļa moduli jūsu vietnes lapām

Preču salīdzinājuma priekšskatījuma paneļa modulis nodrošina debitoriem ar iespēju pārskatīt produktus, ko tie pievieno salīdzinājumam vai izņemiet no tā. Priekšskatījuma panelis nodrošina arī opcijas tiešai navigācijai uz salīdzinājuma lapu vai notīrīt visu preču sarakstu. 

Priekšskatījuma paneli ieteicams iespējot visās lapās, kurās ir **iespējota preču salīdzināšanas** poga. Moduli var pievienot **preču** salīdzinājuma pogai kā slotu, vai to var izmantot kā savrupu moduli, ko varat konfigurēt jebkurā lapā, pat ja nav funkcionalitātes, ko pievienot vai noņemt salīdzināšanai preces. 

Jums lapai manuāli jāpievieno preču salīdzinājuma priekšskatījuma paneļa modulis. Jums jāpievieno tikai viens priekšskatījuma paneļa modulis lapā. Ja pievienojat lapai vairākas moduļa instances, tiks atveidots pirmais modulis, un pārējie tiks ignorēti.

![Preču salīdzinājuma priekšskatījuma panelis](./media/product-comparison-preview-panel-2.png)

Ja norādāt preču salīdzinājuma ierobežojumu, priekšskatījuma panelī varat iespējot Vietturus, kas norāda, cik daudz preču var pievienot salīdzinājumam. Vietturi vietturi tiek aizvietoti ar precēm, kad tās tiek pievienotas salīdzināšanai. Lai konfigurētu preču salīdzinājuma limitu un iespējotu vietturus, **vietas veidotājā dodieties uz vietnes iestatījumiem > paplašinājumiem** **un veiciet izmaiņas preču salīdzinājumu sadaļā**. Konfigurācija tiks piemērota visiem priekšskatījuma panelīm visām lapām. 


## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Norādīt maksimālo preču skaitu, kas ir jārāda salīdzinājuma tekni

Varat norādīt maksimālo preču skaitu, ko rādīt salīdzinājuma tekni, dodoties uz **vietas iestatījumu \> paplašinājumiem** vietu veidotājā. Varat konfigurēt atsevišķus maksimālos ierobežojumus darbvirsmas un mobilo/planšetdatoru skatiem. Pēc noklusējuma ierobežojums netiks ieviests, ja nav noteikts maksimālais ierobežojums.

> [!NOTE]
> Lai nodrošinātu optimālu pārlūkošanas pieredzi, ieteicams iestatīt maksimālo preču skaitu salīdzinājuma tekni uz 2 **mobilā** skata portam un 4 **darbvirsmas skatam,** lai samazinātu nepieciešamo horizontālās ritināšanas daudzumu.

Lai norādītu maksimālo preču skaitu salīdzinājuma tekni, sekojiet šiem soļiem.

1. Vietas veidotājā dodieties uz sadaļu **Vietnes \> iestatījumu paplašinājumi**.
1. **Salīdzināšanas ierobežojumam** — darbvirsmas ierīču rekvizītam ievadiet maksimālo preču skaitu, kas ir jārāda salīdzinājuma tekni darbvirsmas skatījumu atrašanās vietām.
1. Salīdzinājuma ierobežojuma **precēm** — mobilās ierīces un planšetdatora ierīces rekvizītam ievadiet maksimālo preču skaitu, kas salīdzinājuma teknim jārāda mobilajās ierīcēs un planšetdatoros skatītajām precēm.
1. Komandjoslā atlasiet Saglabāt **un publicēt**.

![Vietnes iestatījumi, lai ierobežotu preces salīdzinājuma tekni.](./media/Site-settings-to-limit-products-in-comparison-tray.png)
