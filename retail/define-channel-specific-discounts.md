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
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 6e52ba4bdb8e879959ff886010092914332e6e12
ms.contentlocale: lv-lv
ms.lasthandoff: 04/26/2017


---

# <a name="define-channel-specific-discounts"></a>Kanālam raksturīgo atlaižu definēšana

[!include[banner](includes/banner.md)]


Bieži vien mazumtirgotāji dažādos kanālos iestata dažādas atlaides. Šajā tēmā ir pārskatītas koncepcijas, kas jums ir jāzina, lai izveidotu atlaidi noteiktam kanālam. 

<a name="channel-specific-discounts"></a>Kanālam raksturīgās atlaides
--------------------------

Bieži vien mazumtirgotāji dažādos kanālos piedāvā dažādas atlaides. Iespējams, tas tiek darīts ar mērķi strādāt atbilstoši vietējā tirgus apstākļiem vai tikt galā ar konkurējošiem mazumtirgotājiem.

Lai definētu kanālam specifiskās atlaides, mazumtirdzniecība un komercija sistēmā Microsoft Dynamics 365 for Operations lieto cenu grupas. Cenu grupas var piešķirt vienam vai vairākiem no šiem elementiem: kanāli, katalogi, piederības un lojalitātes programmas. Šajā rakstā ir aprakstīti kanāli, bet šie paši principi attiecas uz katalogu atlaidēm, piederības atlaidēm un lojalitātes atlaidēm.

## <a name="price-groups"></a>Cenu grupas

[![Cenu grupas](./media/price-groups-1024x608.png)](./media/price-groups.png)

Iepriekšējā diagrammā ir parādītas attiecības starp elementiem, kas var būt transakcijā (kanāls, katalogs, piederība, debitors, lojalitātes programmas karte), un dažādiem atlaižu tipiem, kurus iespējams konfigurēt. Visas transakcijas notiek kādā kanālā, tāpēc ir garantēts, ka transakcijā atrodas kanāls. Atlikušie elementi nav obligāti. Katrā pamatdatu lapā ir saite uz saistīto cenu grupu lapu, kur pēc nepieciešamības var apskatīt un pievienot cenu grupas. Cenu grupa tiek lietota, lai četru dažādu tipu elementus saistītu ar atlaidēm, cenu korekcijām un tirdzniecības līgumiem. Iesakām plānot stratēģiju veidam, kā piešķirt nosaukumu savām cenu grupām, lai tās uzturētu kārtībā. Viena iespēja — izmantot burtu vai numuru prefiksu vai sufiksu, lai atšķirtu dažādus tipus. Piemēram, izmantot nosaukumu 1-xxxxx kanāla cenu grupām un izmantot nosaukumu 2-xxxxx kataloga cenu grupām. Pastāv četras pieprasījumu lapas, kas ir koncentrētas uz katru no mazumtirdzniecības elementiem, ar kuriem var būt saistītas atlaides.

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

[Cenu korekcijas un atlaides](price-adjustments-discounts.md)



