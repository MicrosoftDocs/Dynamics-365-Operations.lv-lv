---
title: Meklētājprogrammas optimizēšanas (SEO) apsvērumi jūsu vietnei
description: Šī tēma attiecas uz meklēšanas programmas optimizācijas (SEO) apsvērumiem jūsu vietnē no izstrādes līdz ražošanai.
author: psimolin
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: df92aeae967bbf248b90dffc6bc2239a8d2959183acb9e9181bc344b9e3eff8d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716861"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Meklētājprogrammas optimizēšanas (SEO) apsvērumi jūsu vietnei


[!include [banner](includes/banner.md)]

Šī tēma attiecas uz meklēšanas programmas optimizācijas (SEO) apsvērumiem jūsu vietnē no izstrādes līdz ražošanai.

## <a name="a-site-that-is-under-development"></a>Vietne, kas tiek izstrādāta

Kamēr vietne tiek izstrādāta, visām vietnes lapām jābūt **NOINDEX** un **NOFOLLOW** meta tagiem, lai meklēšanas programmas neatzīmē jūs vietnes lapas un veikala izstrādes versijas jūsu savā kešatmiņā. Lai veiktu šo konfigurāciju, ir jāpievieno noklusējuma meta tagu modulis vietnes lapas veidnei. Noklusējuma meta tagu rekvizīti tad būs pieejami SEO rekvizītu sadaļā lapas redaktorā. Varat izmantot šos rekvizītus, lai pārvaldītu meta tagus.

## <a name="soft-launch-of-a-site"></a>Vietnes viegla palaišana

“Vieglas palaišanas” laikā vietne ir pieejama ierobežotai auditorijai vai tirgum, pirms tiek veikta pilna palaišana. Ja jūs veicat savas tīmekļa vietnes vieglo palaišanu, jums vajadzētu apsvērt iespēju atstāt **NOINDEX** meta tagus. Šādā veidā jūs palīdzēsiet nodrošināt, ka vieglā palaišana joprojām ir ierobežota ar ierobežotu auditoriju, ko vēlaties sasniegt.

## <a name="a-site-that-is-in-production"></a>Vietne, kas ir ražošanā

Kad vietne ir ražošanā, jums jāpārliecinās, ka visas vietnes lapas ir pareizi atzīmētas. Programma Microsoft Dynamics 365 Commerce izmanto informāciju, kas ievadīta lapā, lai padarītu visu SEO informāciju šajā lapā. Šie moduļi nodrošina šo funkcionalitāti: kategorijas lapas kopsavilkumu, saraksta lapas kopsavilkumu un preces lapas kopsavilkumu.

Lai optimizētu meklēšanas programmas indeksēšanu, atveidošanas struktūra izmanto gan informāciju no SEO rekvizītiem, kas konfigurēti Dynamics 365 Commerce modulī, gan moduļa specifisko informāciju. Attiecībā uz vietni, kas ir ražošanā, jums jāpārliecinās, ka fails robots.txt ļauj indeksēt visu jūsu vietni un ka tā satur saites uz jūsu publicēto vietnes kartes dokumentu. Jums ir jāieslēdz vietnes kartes ģenerēšanas funkcionalitāte **Vietnes iestatījumi \> Vietnes kartes iespējotas**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Lapas SEO iestatījumi iekšējam priekšskatījumam, ierobežotas auditorijas un visas auditorijas

Tā kā Dynamics 365 Commerce atbalsta “ko redzat, to iegūstat”(WYSIWYG) autentificētus priekšskatījumus vizuālo lapu veidotājā, autori var sagatavot savu lapas saturu, neuztraucoties, ka šī informācija tiks rādīta vietnes apmeklētājiem. Ja lapa ir jāpublicē, bet tās pieejamībai jābūt ierobežotai, tai jābūt **NOINDEX** meta tagam, lai meklēšanas programmas to neindeksētu. Pēc tam, kad lapa ir gatava visām auditorijām, visiem pamata SEO metadatiem ir jābūt klātesošiem, lai palielinātu meklēšanas programmu indeksācijas efektivitāti. Turklāt **NOLIMIT** meta tags ir jānoņem.

## <a name="additional-resources"></a>Papildu resursi

[Lietotāju un lomu pārvaldība E-tirdzniecībā](manage-ecommerce-users-roles.md)

[Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju](add-telemetry.md)

[Satura drošības politikas (CSP) pārvaldība](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]