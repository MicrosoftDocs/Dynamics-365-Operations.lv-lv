---
title: Vietnes navigācijas pielāgošana
description: Šajā tēmā aprakstīts, kā izveidot pielāgotu tiešsaistes navigācijas hierarhiju, lai organizētu preces pārlūkošanai jūsu Microsoft Dynamics 365 Commerce vietnē.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 642cb5c145dec68631eb9ab27d926ba8ab75c59b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914914"
---
# <a name="customize-site-navigation"></a>Vietnes navigācijas pielāgošana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot pielāgotu tiešsaistes navigācijas hierarhiju, lai organizētu preces pārlūkošanai jūsu Microsoft Dynamics 365 Commerce vietnē.

## <a name="overview"></a>Pārskats

Tiešsaistes veikala skatlogs parasti ļauj klientiem atklāt un pārlūkot preces, pārvietojoties pa preču kategorijām. Šo iespēju parasti nodrošina cilnes lapas augšpusē vai navigācijas josla kreisajā pusē. Dynamics 365 Commerce varat izveidot un pārvaldīt savas kategoriju navigācijas hierarhijas struktūru un preces, kas ir iekļautas dažādās kategorijās.

## <a name="create-a-retail-channel-navigation-hierarchy"></a>Mazumtirdzniecības kanāla navigācijas hierarhijas izveidošana

Lai izveidotu mazumtirdzniecības kanāla navigācijas hierarhiju, veiciet tālāk minētās darbības.

1. Dodieties uz **Mazumtirdzniecība \> Preces un kategorijas \> Kategorija un preču pārvaldība**.
1. Atlasiet **Kategorijas hierarhijas** un pēc tam atlasiet **Jauns**.
1. Piešķiriet hierarhijai nosaukumu.

    > [!NOTE]
    > Izveidotā augšējā kategorija ir saknes kategorijas mezgls. Tā netiks parādīta jūsu vietnē. Lai izveidotu kategoriju hierarhiju, kur jūsu vietnē tiek parādīts viens augšējā līmeņa mezgls, izveidojiet kategoriju un piešķiriet tai nosaukumu kā saknes apakškategorijai.

1. Atlasiet **Jauns kategorijas mezgls** un piešķiriet kategorijai nosaukumu.
1. Turpiniet veidot nepieciešamās dvīņu un apakškategorijas.

Tagad varat piešķirt preces katrai kategorijai, ko izveidojāt zem augšējā līmeņa kategorijas.

## <a name="customize-the-order-of-categories"></a>Kategoriju secības pielāgošana

Pēc noklusējuma jūsu definētās kategorijas jūsu vietnē parādīsies alfabētiskā secībā. Tomēr varat arī pielāgot kategoriju rādīšanas secību.

## <a name="assign-a-category-hierarchy-type"></a>Kategoriju hierarhijas tipa piešķiršana

1. Dodieties uz **Mazumtirdzniecība \> Preces un kategorijas \> Kategorija un preču pārvaldība**.
1. Atlasiet **Kategorijas hierarhijas**.
1. Darbību rūts cilnē **Kategoriju hierarhija** grupā **Iestatīt** atlasiet **Saistītās hierarhijas veids**.
1. Atlasiet **Jauns**.
1. Laukā **Kategoriju hierarhijas veids** atlasiet **Mazumtirdzniecības kanāla navigācijas hierarhija**.
1. Laukā **Kategoriju hierarhija** atlasiet iepriekš izveidoto kanāla navigācijas hierarhiju.

## <a name="publish-new-or-updated-navigation-hierarchies"></a>Jaunu vai atjauninātu navigācijas hierarhiju publicēšana

Lai navigācijas hierarhiju padarītu pieejamu jūsu tiešsaistes veikala skatlogam, veiciet tālāk minētās darbības.

1. Dodieties uz **Mazumtirdzniecība \> Kanāla iestatīšana \> Kanāla kategorijas un preses īpašības**.
1. Kokā kreisajā pusē atlasiet jūsu tiešsaistes veikalu.
1. Atlasiet **Publicēt kanāla atjauninājumus**.
1. Atveriet sadaļu **Mazumtirdzniecība \> Mazumtirdzniecības IT \> Sadales grafiks**.
1. Sarakstā atrodiet un atlasiet **Darbs 1040**.
1. Atlasiet **Izpildīt tūlīt**.
1. Atkārtojiet 5. un 6. darbību darbiem 1070 un 1150.

## <a name="show-categories-on-your-site"></a>Kategoriju parādīšana jūsu vietnē

Lai parādītu kategoriju hierarhiju jūsu tiešsaistes veikala skatlogā, jums veidnes vai fragmenta atbilstošā vietā jāpievieno navigācijas izvēlnes modulis. Navigācijas izvēlnes modulis tiks parādīts navigācijas hierarhijā, ar nosacījumu, ka publicējāt savu mazumtirdzniecības navigācijas hierarhiju kanālā, ar kuru saistīta jūsu vietne.

> [!NOTE]
> Veikala sākuma komplektā iekļautais navigācijas izvēlnes modulis ļauj lietotājiem pārvietoties tikai uz kategorijām, kurām nav apakškategoriju. Ja jūsu klientiem vajadzētu pārvietoties uz kategorijām, kurām ir apakškategorijas, navigācijas izvēlnes modulis ir jāpielāgo.

## <a name="add-custom-navigation-options"></a>Pielāgoto navigācijas opciju pievienošana

Jūsu navigācijas izvēlnē varat pievienot navigācijas opcijas, kas nav daļa no preču kategoriju hierarhijas. Piemēram, preču kategoriju saraksta beigās varat pievienot elementu **Sazinieties ar mums**, kas norāda uz jūsu vietnei izveidoto kontaktinformācijas lapu.

Lai navigācijas izvēlnei pievienotu pielāgotās navigācijas opcijas, veiciet tālāk minētās darbības.

1. Veidnē vai fragmentā, ko vēlaties pielāgot, atlasiet navigācijas izvēlnes moduli.
1. Rekvizītu rūts cilnē **Dati** atlasiet **Pievienot elementu**, lai izveidotu jaunu satura pārvaldības sistēmas (CMS) navigācijas elementu.
1. Ievadiet saites tekstu un URL.
1. Atkārtojiet 2. un 3. darbību, lai pievienotu vairāk pielāgoto navigācijas opciju.
1. Kad esat pabeidzis, saglabājiet veidni vai fragmentu un reģistrējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Pārskats par veidnēm un izkārtojumiem](templates-layouts-overview.md)

[Darbs ar veidnēm](work-with-templates.md)

[Darbs ar iepriekš iestatītiem izkārtojumiem](work-with-layouts.md)

[Darbs ar fragmentiem](work-with-fragments.md)

[Darbs ar moduļiem](work-with-modules.md)

[Lapas vietrāža URL izveide](create-page-url.md)

[Darbs ar publicēšanas grupām](publish-groups.md)
