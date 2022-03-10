---
title: Izmēģināt mēroga vienības izkliedētā hibrīda topoloģijā
description: Šajā tēmā ir sniegta informācija par to, kā izmēģināt mākoņa un malu skalas vienības ražošanas un noliktavas pārvaldības darba slodzei.
author: perlynne
ms.date: 03/03/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 04fd79f3c582ae9ac51882f73410477efaa35496
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376258"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Izmēģināt mēroga vienības izkliedētā hibrīda topoloģijā

[!include [banner](../includes/banner.md)]

Izplatītās hibrīda topoloģijas izmēģināšanas process ir vienkāršs. Pirmajā posmā ir jāpārbauda pielāgojumi, lai nodrošinātu, ka tie darbojas izkliedētajā topoloģijā. Jums ir divas iespējas.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>1. iespēja: pielāgojumu novērtēšana izstrādes vidēs

Pirms sākat iebūvēt smilškastes vidēs, ieteicams izpētīt mēroga vienības izstrādes iestatījumos, piemēram, vienas kastes vidē (kas pazīstama arī kā 1. līmeņa vide), lai varētu validēt procesus, pielāgojumus un risinājumus. Šā posma laikā dati un pielāgojumi tiks pielietoti vienas kastes vidēm. Jūs varat darboties vienā vidē, kas var uzņemties gan uzņēmuma centra, gan mēroga vienības lomu. Alternatīvi, jums var būt divas attīstības vides, no kurām viena ieņem centra lomu, bet otra uzņemas mēroga vienības lomu. Šis iestatījums nodrošina labāko veidu, kā identificēt un risināt problēmas. Lai pabeigtu šo posmu, var izmantot arī jaunāko [agrīnās piekļuves (PEAP) būvi](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxURUFWTjQzTzg0UUk5RkJHMDFEMVlSSDFEQy4u).

Lai instalētu un uzturētu vidi, [izmantojiet skalas bloku izvietošanas rīkus](https://github.com/microsoft/SCMScaleUnitDevTools) vienas kastes izstrādes vidēm. Šie rīki ļauj konfigurēt centrmezgla un mēroga vienības vienā vai divās viena lodziņa vidēs. Rīki tiek nodrošināti gan kā binārs laidiens, gan GitHub pirmkodā. Izpētiet projekta vikivietni, kurā ir [iekļauta detalizēta lietošanas pamācība](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide), kurā aprakstīts, kā izmantot rīkus. Ja izvietojat [malu mēroga vienības pielāgotā aparatūrā, izmantojot vietējos biznesa datus (LBD),](cloud-edge-edge-scale-units-lbd.md) jums ir jāievēro cits process.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>2. iespēja: iegūstiet pievienojumprogrammas un izvietojiet smilškastes vidēs

Lai izmēģinātu izplatīto hibrīdo topoloģiju, jums ir jābūt divām smilškastes vidēm (2. līmenis), no kurām vienā ir jūsu dati (uzņēmuma centrmezgls), bet otrā - skalas vienībai un ir "tukši dati".

Jāpievienojumprogrammas vismaz vienai mākoņa vai malu skalas vienībai. Pēc tam dzīves cikla pakalpojumos (LKS) tiks piešķirtas [Microsoft Dynamics atbilstošas projektu un vides laika nišas, lai skalas vienības vides varētu izvietot, izmantojot](https://lcs.dynamics.com/) Mēroga vienības pārvaldnieka portālu [.](https://aka.ms/SCMSUM)

Sazinieties ar Microsoft atbalsta dienestu, lai pieprasītu iespējot smilškastes vides.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
