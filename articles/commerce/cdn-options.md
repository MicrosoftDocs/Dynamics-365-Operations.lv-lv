---
title: Satura pieg'ades tīkla ieviešanas opcijas
description: Šis raksts pārskata dažādas opcijas satura piegādes tīkla (CDN) ieviešanai, ko var izmantot Microsoft Dynamics 365 Commerce ar vidēm. Šīs opcijas ietver vietējās, Commerce nodrošinātās Azure Front Door instances un klientam piederošās Azure Front Door instances.
author: BrianShook
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: de2ecab86809af3ace64ba06956f00137d254ab7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275152"
---
# <a name="content-delivery-network-implementation-options"></a>Satura pieg'ades tīkla ieviešanas opcijas

[!include [banner](includes/banner.md)]

Šis raksts pārskata dažādas opcijas satura piegādes tīkla (CDN) ieviešanai, ko var izmantot Microsoft Dynamics 365 Commerce ar vidēm. Šīs opcijas ietver vietējās, Commerce nodrošinātās Azure Front Door instances un klientam piederošās Azure Front Door instances.

Commerce klientiem ir vairākas opcijas, kad viņi lemj, kuru CDN pakalpojumu izmantot savā Commerce vidē. Commerce tiek izlaista ar Azure Front Door pamata atbalstu, kas ietver pamata mitināšanu un pielāgoto domēnu prasības. Uzņēmumiem, kuri vēlas vairāk kontroles un konkrētākas drošības iespējas, piemēram, tīmekļa lietojumprogrammas ugunsmūri (WAF), vislabāk varētu būt lietot vai nu klientam piederošu Azure Front Door instanci vai ārēju CDN pakalpojumu.

Ar Commerce vidēm var izmantot šādas trīs CDN ieviešanas opcijas:

- Commerce nodrošināta Azure Front Door instance
- Klientam piederoša Azure Front Door instance (paaugstinātai kontrolei un papildu drošības līdzekļiem)
- Ārējs CDN pakalpojums

Trīs CDN ieviešanas opcijas nodrošina tikai dinamisku HTML saturu no pielāgotiem domēniem. Commerce automātiski apstrādā visus JavaScript, Stila lapu kaskadēšanu (CSS), attēlus, videoklipus un citu statisku saturu, izmantojot Microsoft pārvaldītus CDN. Jūsu izvēlētā opcija nosaka pieejamās darbības iespējas, vadības iespējas un papildu drošības iespējas.

Šajā attēlā parādīts Commerce arhitektūras pārskats.

![Commerce arhitektūras pārskats.](media/Commerce_CDN-Option_ComparisonModels.png)

Papildu informāciju par to, kā iestatīt Azure Front Door instanci savai Commerce vietnei, skatiet tēmā [CDN atbalsta pievienošana](add-cdn-support.md).

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>Commerce nodrošinātas Azure Front Door instances izmantošana

Šajā tabulā uzskaitītas Commerce nodrošinātas Azure Front Door instances lietošanas priekšrocības un trūkumi satura galapunktu pārvaldībā.

| Priekšrocības | Trūkumi |
|------|------|
| <ul><li>Instance ir iekļauta Commerce izmaksās.</li><li>Tā kā instanci pārvalda Commerce darba grupa, ir nepieciešama mazāka uzturēšana un ir kopīgas iestatīšanas darbības.</li><li>Azure viesotā infrastruktūra ir mērogojama, droša un uzticama.</li><li>Drošligzdu slāņa (SSL) sertifikātam ir nepieciešama vienreizēja iestatīšana, un tas tiek atjaunināts automātiski.</li><li>Instances kļūdas un novirzes no normas uzrauga Commerce darba grupa.</li></ul> | <ul><li>MK netiek atbalstīts.</li><li>Nav konkrētu pielāgojumu vai iestatīšanas pielāgojumu.</li><li>Instances atjauninājumi vai izmaiņas ir atkarīgas no Commerce darba grupas.</li><li>Apex domēniem ir vajadzīga atsevišķa Azure Front Door instance, lai tos integrētu ar Azure DNS.</li><li>Klientam netiek nodrošināta telemetrija par atbildēm sekundē (RPS) vai kļūdu rādītāju.</li></ul> |

Šajā attēlā parādīta Commerce nodrošinātas Azure Front Door instances arhitektūra.

![Commerce nodrošinātas Azure Front Door instance.](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>Izmantojiet klientam piederošu Azure Front Door instanci

Šajā tabulā uzskaitītas klientam piederošas Azure Front Door instances lietošanas priekšrocības un trūkumi satura galapunktu pārvaldībā.

| Priekšrocības | Trūkumi |
|------|------|
| <ul><li>Iestatīšana ir droša un viegli pārvaldāma.</li><li>Azure viesotā infrastruktūra ir mērogojama, droša un uzticama.</li><li>Instance atļauj WAF intergrāciju un detalizētas kārtulas vadīklas detalizētākai drošībai, kura ir pielāgota konkrēti jūsu vietnes vajadzībām.</li><li>Instance nodrošina detalizētāku SSL sertifikātu vadību (kā klientiem piederošu, tā arī Azure Front Door pārvaldītu) un domēnu saistīšanu.</li><li>Instance nodrošina Apex domēna risinājumu, ja tam tiek izveidots tiešs pāra savienojums ar Azure DNS.</li><li>Tiek nodrošināta telemetrija un brīdināšana.</li><li>Drošligzdu slāņa (SSL) sertifikātam ir nepieciešama vienreizēja iestatīšana, un tas tiek atjaunināts automātiski.</li></ul> | <ul><li>Instance ir pašpārvaldīta.</li><li>Ir nepieciešama sākotnējā zināšanu uzņemšana.</li></ul> |

Šajā attēlā parādīta Commerce infrastruktūra, kas ietver klientam piederošu Azure Front Door instanci.

![Commerce infrastruktūra, kas ietver klientam piederošu Azure Front Door instanci.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>Ārēja CDN pakalpojuma izmantošana

Šajā tabulā uzskaitītas ārēja CDN pakalpojuma lietošanas priekšrocības un trūkumi satura galapunktu pārvaldībā.

| Priekšrocības | Trūkumi |
|------|------|
| <ul><li>Šī opcija ir noderīga, ja esošais domēns jau tiek viesots ārējā CDN.</li><li>MK: atkarīgs no ārējā nodrošinātāja.</li></ul> | <ul><li>Ir nepieciešams atsevišķs līgums un papildu izmaksas.</li><li>SSL var radīt papildu izmaksas.</li><li>Tā kā pakalpojums ir šķirts no Azure mākoņa struktūras, ir jāpārvalda papildu infrastruktūra.</li><li>Pakalpojumam var būt nepieciešamas ilgākas investīcijas galapunkta un drošības iestatīšanā.</li><li>Pakalpojums tiek pašpārvaldīts.</li><li>Pakalpojums tiek pašuzraudzīts.</li></ul> |

Šajā attēlā parādīta Commerce infrastruktūra, kas ietver klientam ārēju CDN pakalpojumu.

![Commerce infrastruktūra, kas ietver klientam ārēju CDN pakalpojumu.](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>Papildu resursi

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)
