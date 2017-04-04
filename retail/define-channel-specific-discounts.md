---
title: "Kanālam raksturīgo atlaižu definēšana"
description: "Bieži vien mazumtirgotāji dažādos kanālos iestata dažādas atlaides. Šajā tēmā ir pārskatītas koncepcijas, kas jums ir jāzina, lai izveidotu atlaidi noteiktam kanālam."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>Kanālam raksturīgo atlaižu definēšana

Bieži vien mazumtirgotāji dažādos kanālos iestata dažādas atlaides. Šajā tēmā ir pārskatītas koncepcijas, kas jums ir jāzina, lai izveidotu atlaidi noteiktam kanālam. 

<a name="channel-specific-discounts"></a>Kanālam raksturīgās atlaides
--------------------------

Mazumtirgotāji bieži piedāvā dažādas atlaides dažādos kanālos. Tas var izdarīt adresi vietējiem tirgus apstākļiem vai tikt galā ar konkurējošu mazumtirgotājiem.

Mazumtirdzniecības un komercijas Microsoft Dynamics 365 operācijām izmanto cenu grupas, lai definētu kanālam raksturīgo atlaides. Cenu grupas var piešķirt vienam vai vairākiem no šiem elementiem: kanāli, katalogi, piederības un lojalitātes programmas. Šajā rakstā ir aprakstīti kanāli, bet šie paši principi attiecas uz katalogu atlaidēm, piederības atlaidēm un lojalitātes atlaidēm.

## <a name="price-groups"></a>Cenu grupas
\[Caption id = "pielikumu\_256084" izlīdzināt = "alignnone" width = "640"\][![cenu grupas](./media/price-groups-1024x608.png)](./media/price-groups.png) mazumtirdzniecības cenu grupas saites\[/parakstu\]

Iepriekš diagramma ilustrē attiecības starp entītijām, kas var būt (kanāls, katalogu, piederību, klientu, klienta karšu) darbību un dažādu atlaižu tipus, kas var konfigurēt. Visas darbības notiek kanālu, lai kanāls ir garantēta šā darījuma. Atlikušie elementi nav obligāti. Katrā pamatdatu lapā ir saite uz saistīto cenu grupu lapu, kur pēc nepieciešamības var apskatīt un pievienot cenu grupas. Cenu grupa tiek lietota, lai attiecinātu četru dažādu veidu entītijām atlaides, cenu korekcijas un tirdzniecības nolīgumiem. Mēs iesakām jums plānot stratēģiju, kā tu nosauksi cenu grupas, lai saglabātu tos organizē. Viena iespēja būtu izmantot burtu vai ciparu prefiksa vai sufiksa atšķirt dažāda. Piemēram, 1-xxxxx kanāls cenu grupām un 2-xxxxx kataloga cenu grupām. Pastāv četras pieprasījumu lapas, kas ir koncentrētas uz katru no mazumtirdzniecības elementiem, ar kuriem var būt saistītas atlaides.

-   **Mazumtirdzniecības kanāla cenu grupas** — šajā lapā katrai cenu grupai tiek rādīts saistīts kanālu un atlaižu saraksts.
-   **Kataloga cenu grupas** — šajā lapā katrai cenu grupai tiek rādīts saistīts katalogu un atlaižu saraksts.
-   **Lojalitātes programmas cenu grupas** — šajā lapā katrai cenu grupai tiek rādīts saistīts lojalitātes programmu un atlaižu saraksts.
-   **Piederības cenu grupas** — šajā lapā katrai cenu grupai tiek rādīts saistīts piederību un atlaižu saraksts.

## <a name="example-channel-discount-set-up"></a>Kanāla atlaižu iestatīšanas piemērs
Nākamajā piemērā ir parādīti kanāla atlaižu iestatīšanas procedūrā iesaistītie uzdevumi.

1.  Šim piemēram jums ir kanāls ar nosaukumu **Houston**, un jūs grasāties izveidot jaunu atlaidi ar nosaukumu **Back-to-School.**
2.  Tā kā cenu noteikšanas un atlaižu stratēģija ietver kanāla atlaižu iespēju, kad veidojat kanālu, vienmēr varat izveidot kanālam raksturīgu cenu grupu.
3.  Jums ir cenu grupa **Houston-PG**, un tā ir piešķirta kanālam **Houston**.
4.  Kad ir izveidota jaunā atlaide **Back-to-School**, jums ir jānoklikšķina uz vienuma **Cenu grupas**, kas atrodas lapas **Atlaide** augšpusē. Tiek atvērta lapa **Atlaides cenu grupas**. Pēc tam noklikšķiniet uz **Jauns** un atlasiet cenu grupu **Houston-PG**.
5.  Tagad šo atlaidi varat iespējot un sākt to izmantot kanālā.

 

<a name="see-also"></a>Skatiet arī
--------

[Price adjustments and discounts](price-adjustments-discounts.md)


