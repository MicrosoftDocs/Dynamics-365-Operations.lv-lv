---
title: Kanālam raksturīgo atlaižu definēšana
description: Bieži vien mazumtirgotāji dažādos kanālos iestata dažādas atlaides. Šis raksts pārskata koncepcijas, kas jums ir jāzina, lai izveidotu atlaidi noteiktam kanālam.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.industry: Retail
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
ms.openlocfilehash: f426503a6897a73010b77082f4277b65545bfcc3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273559"
---
# <a name="define-channel-specific-discounts"></a>Kanālam raksturīgo atlaižu definēšana

[!include [banner](includes/banner.md)]

Šis raksts pārskata koncepcijas, kas jums ir jāzina, lai izveidotu atlaidi noteiktam kanālam.

## <a name="channel-specific-discounts"></a>Kanālam raksturīgās atlaides

Bieži vien mazumtirgotāji dažādos kanālos piedāvā dažādas atlaides. Iespējams, tas tiek darīts ar mērķi strādāt atbilstoši vietējā tirgus apstākļiem vai tikt galā ar konkurējošiem mazumtirgotājiem.

Commerce izmanto cenu grupas, lai definētu kanālam raksturīgās atlaides. Cenu grupas var piešķirt vienam vai vairākiem no šiem elementiem: kanāli, katalogi, piederības un lojalitātes programmas. Šajā rakstā ir aprakstīti kanāli, bet šie paši principi attiecas uz katalogu atlaidēm, piederības atlaidēm un lojalitātes atlaidēm.

## <a name="price-groups"></a>Cenu grupas

[![Cenu grupas.](./media/price-groups-1024x608.png)](./media/price-groups.png)

Iepriekšējā diagrammā ir parādītas attiecības starp elementiem, kas var būt transakcijā (kanāls, katalogs, piederība, debitors, lojalitātes programmas karte), un dažādiem atlaižu tipiem, kurus iespējams konfigurēt. Visas transakcijas notiek kādā kanālā, tāpēc ir garantēts, ka transakcijā atrodas kanāls. Atlikušie elementi nav obligāti. Katrā pamatdatu lapā ir saite uz saistīto cenu grupu lapu, kur pēc nepieciešamības var apskatīt un pievienot cenu grupas. Cenu grupa tiek lietota, lai četru dažādu tipu elementus saistītu ar atlaidēm, cenu korekcijām un tirdzniecības līgumiem. Iesakām plānot stratēģiju veidam, kā piešķirt nosaukumu savām cenu grupām, lai tās uzturētu kārtībā. Viena iespēja — izmantot burtu vai numuru prefiksu vai sufiksu, lai atšķirtu dažādus tipus. Piemēram, izmantot nosaukumu 1-xxxxx kanāla cenu grupām un izmantot nosaukumu 2-xxxxx kataloga cenu grupām. Pastāv četras pieprasījumu lapas, kas ir koncentrētas uz katru no komercijas elementiem, ar kuriem var būt saistītas atlaides.

- **Channel kanāla cenu grupas** – šajā lapā katrai cenu grupai tiek rādīts saistīts kanālu un atlaižu saraksts.
- **Kataloga cenu grupas** — šajā lapā katrai cenu grupai tiek rādīts saistīts katalogu un atlaižu saraksts.
- **Lojalitātes programmas cenu grupas** — šajā lapā katrai cenu grupai tiek rādīts saistīts lojalitātes programmu un atlaižu saraksts.
- **Piederības cenu grupas** — šajā lapā katrai cenu grupai tiek rādīts saistīts piederību un atlaižu saraksts.

## <a name="example-channel-discount-set-up"></a>Kanāla atlaižu iestatīšanas piemērs

Nākamajā piemērā ir parādīti kanāla atlaižu iestatīšanas procedūrā iesaistītie uzdevumi.

1. Šim piemēram jums ir kanāls ar nosaukumu **Houston**, un jūs grasāties izveidot jaunu atlaidi ar nosaukumu **Back-to-School.**
2. Tā kā cenu noteikšanas un atlaižu stratēģija ietver kanāla atlaižu iespēju, kad veidojat kanālu, vienmēr varat izveidot kanālam raksturīgu cenu grupu.
3. Jums ir cenu grupa **Houston-PG**, un tā ir piešķirta kanālam **Houston**.
4. Kad ir izveidota jaunā atlaide **Back-to-School**, jums ir jānoklikšķina uz vienuma **Cenu grupas**, kas atrodas lapas **Atlaide** augšpusē. Tiek atvērta lapa **Atlaides cenu grupas**. Pēc tam noklikšķiniet uz **Jauns** un atlasiet cenu grupu **Houston-PG**.
5. Tagad šo atlaidi varat iespējot un sākt to izmantot kanālā.

## <a name="additional-resources"></a>Papildu resursi

[Cenu korekcijas un atlaides](price-adjustments-discounts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
