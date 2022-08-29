---
title: Meklētājprogrammas optimizēšanas (SEO) apsvērumi jūsu vietnei
description: Šajā rakstā ir ietverti meklēšanas programmas optimizācijas (ARĪ) apsvērumi par jūsu vietni no izstrādes līdz ražošanai.
author: josaw1
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 77bbc04e849cf1cdeb7ce19226f43354635ddbe0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275624"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Meklētājprogrammas optimizēšanas (SEO) apsvērumi jūsu vietnei


[!include [banner](includes/banner.md)]

Šajā rakstā ir ietverti meklēšanas programmas optimizācijas (ARĪ) apsvērumi par jūsu vietni no izstrādes līdz ražošanai.

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
