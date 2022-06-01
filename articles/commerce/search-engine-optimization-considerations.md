---
title: Meklētājprogrammas optimizēšanas (SEO) apsvērumi jūsu vietnei
description: Šī tēma attiecas uz meklēšanas programmas optimizācijas (SEO) apsvērumiem jūsu vietnē no izstrādes līdz ražošanai.
author: psimolin
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 2f90581766dba3d3a671df52ec08339a1a0fd7dc
ms.sourcegitcommit: 9dd2d32fc303023a509d58ec7b5935f89d1e9c6d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/26/2022
ms.locfileid: "8806409"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Meklētājprogrammas optimizēšanas (SEO) apsvērumi jūsu vietnei


[!include [banner](includes/banner.md)]

Šī tēma attiecas uz meklēšanas programmas optimizācijas (SEO) apsvērumiem jūsu vietnē no izstrādes līdz ražošanai.

## <a name="a-site-that-is-under-development"></a>Vietne, kas tiek izstrādāta

Lai nodrošinātu, ka meklēšanas programmas neindeksē vietu izstrādei, **visu vietu lapām jābūt bezindex** **un bezfollow** metadatu etiķetēm. Labā prakse ir izveidot fragmentu [, balstoties uz metatags moduli, kas satur šādu meta taga ierakstu, un nodrošināt, ka fragments](metatags-module.md) tiek pievienots visu vietnē izmantoto veidņu HTML \<head\> sadaļai.

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>Vietnes viegla palaišana

“Vieglas palaišanas” laikā vietne ir pieejama ierobežotai auditorijai vai tirgum, pirms tiek veikta pilna palaišana. Ja tīmekļa vietne tiek palaista viegli, ieteicams atstāt bezindeksu **metadatu** etiķetes vietā. Šādā veidā jūs palīdzēsiet nodrošināt, ka vieglā palaišana joprojām ir ierobežota ar ierobežotu auditoriju, ko vēlaties sasniegt.

## <a name="a-site-that-is-in-production"></a>Vietne, kas ir ražošanā

Kad vietne ir ražošanā, jums jāpārliecinās, ka visas vietnes lapas ir pareizi atzīmētas. Programma Microsoft Dynamics 365 Commerce izmanto informāciju, kas ievadīta lapā, lai padarītu visu SEO informāciju šajā lapā. Šie moduļi nodrošina šo funkcionalitāti: kategorijas lapas kopsavilkumu, saraksta lapas kopsavilkumu un preces lapas kopsavilkumu.

Lai optimizētu meklēšanas programmas indeksēšanu, atveidošanas struktūra izmanto gan informāciju no SEO rekvizītiem, kas konfigurēti Dynamics 365 Commerce modulī, gan moduļa specifisko informāciju. Attiecībā uz vietni, kas ir ražošanā, jums jāpārliecinās, ka fails robots.txt ļauj indeksēt visu jūsu vietni un ka tā satur saites uz jūsu publicēto vietnes kartes dokumentu. Jums ir jāieslēdz vietnes kartes ģenerēšanas funkcionalitāte **Vietnes iestatījumi \> Vietnes kartes iespējotas**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Lapas SEO iestatījumi iekšējam priekšskatījumam, ierobežotas auditorijas un visas auditorijas

Tā kā Dynamics 365 Commerce atbalsta “ko redzat, to iegūstat”(WYSIWYG) autentificētus priekšskatījumus vizuālo lapu veidotājā, autori var sagatavot savu lapas saturu, neuztraucoties, ka šī informācija tiks rādīta vietnes apmeklētājiem. Ja lapa ir jāpublicē, bet tās ietekme ir jāierobežo, **tai jābūt bezindeksēšanas** metadatu etiķetei, lai tā nebūtu indeksēta meklēšanas programmā. Pēc tam, kad lapa ir gatava visām auditorijām, visiem pamata SEO metadatiem ir jābūt klātesošiem, lai palielinātu meklēšanas programmu indeksācijas efektivitāti. Turklāt nolimitinātais **metadatu** tags ir jānoņem.

## <a name="additional-resources"></a>Papildu resursi

[Lietotāju un lomu pārvaldība E-tirdzniecībā](manage-ecommerce-users-roles.md)

[Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju](add-telemetry.md)

[Satura drošības politikas (CSP) pārvaldība](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
