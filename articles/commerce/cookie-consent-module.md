---
title: Sīkfailu piekrišanas modulis
description: Šajā rakstā ir ietverti sīkfaila atļaujas moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 514f54ea6ff05dc3e0885f21af176453dd604848
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878599"
---
# <a name="cookie-consent-module"></a>Sīkfailu piekrišanas modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir ietverti sīkfaila atļaujas moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.

Sīkfailu piekrišanas modulis liek vietnes lietotājiem skaidri sniegt piekrišanu, lai atļautu sīkfailus jebkuram līdzeklim vai modulim, kas izseko pārlūka sīkfailus. Piekrišana ir nepieciešama pirmoreiz, kad vietnes lietotājs pārlūko vietni jaunā pārlūka sesijā. Kad tiek saņemts piekrišana, tā tiek izsekota, un vietnes lietotājs vairs netiks brīdināts par piekrišanu. Lai iegūtu papildinformāciju, skatiet [Sīkfailu piekrišana](cookie-compliance.md).

Ja vietnes lietotāja sīkfailu piekrišana netiek saņemta, tad visi līdzekļi vai moduļi, kuriem nepieciešama sīkfailu piekrišana, netiks renderēti lapā. Piemēram, izrakstīšanās modulis, sociālās koplietošanas modulis un vēlamās krātuves līdzeklis prasa sīkfailu piekrišanu un netiks renderēti, ja vietnes lietotāja piekrišana nav saņemta. 

Sīkdatņu piekrišanas moduli var konfigurēt lapas galvenes fragmentā, lai to varētu ieviest, kad tiek ielādēta lapa. Sīkfaila piekrišanas modulim ir jābūt skaidram ziņojumam, kas informē vietnes lietotāju par sīkfailu izmantošanu vietnē, un tam jāsniedz saite uz vietnes konfidencialitātes lapu.

Sekojošajā attēlā ir parādīts sīkfailu piekrišanas ziņojuma piemērs ar saiti uz vietnes konfidencialitātes politikas lapu, kas tiek rādīta vietnes lapas galvenē.
![Sīkfailu piekrišanas moduļa piemērs.](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Sīkfailu piekrišanas moduļa rekvizīti

| Rekvizīta nosaukums             | Vērtība                 | Apraksts |
|---------------------------|-----------------------|-------------|
| Bagātināts teksts                  | Bagātināts teksts | Norāda bagātināta teksta paziņojumu vietnes lietotājiem, ka vietne izmanto pārlūkprogrammas sīkfailus un ka lietotājiem ir jāakceptē sīkfailu izmantošana vietnei, lai tā būtu pilnībā funkcionāla. |
| Saites | Vietrādis URL | Vienu vai vairākas saites var pievienot vietnes konfidencialitātes lapai, kas apraksta sīkfailus, kas tiek izsekoti vietnē. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Pievienot sīkfailu piekrišanas moduli vietnes lapām

Lai efektīvi pievienotu sīkfailu piekrišanas moduli vairākām vietnes lapām, to var pievienot koplietojamās lapas galvenes fragmentam. Kad galvenes fragments ir pievienots visām vietnes lapām, sīkfailu piekrišanas paziņojums tiks automātiski atveidots, pirmoreiz, kad vietnes lietotājs naviģē uz jebkuru vietnes lapu.

Papildinformāciju par galveņu fragmentiem un moduļiem skatiet šeit: [Galvenes modulis](author-header-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Galvenes modulis](author-header-module.md) 

[Sīkfailu atbilstība](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]