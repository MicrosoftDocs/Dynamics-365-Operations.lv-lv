---
title: Datu koplietošana starp uzņēmumiem attiecībā uz dāvanu kartēm
description: Šajā rakstā ir aprakstīts, kā izmantot Microsoft Dynamics 365 Commerce Dynamics 365 finanšu datu kopīgošanas funkcionalitāti datu apgabalos, lai sinhronizētu dāvanu kartes datus.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: bc0df6c4aac72907e8523069e3f1ae100780dc3c
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473936"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Datu koplietošana starp uzņēmumiem attiecībā uz dāvanu kartēm

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā konfigurēt tā Microsoft Dynamics 365 Commerce, lai dāvanu kartes datu sinhronizēšanai jāizmanto Dynamics 365 finanšu datu kopīgošanas funkcionalitāte. Datu ierakstu kopīgošanas funkcionalitāti pēc tam var izmantot, lai kopīgotu datu starpuzņēmumu starp divām datu jomām. Šādā veidā Commerce iekšējo dāvanu tabula var kopīgot datus starp diviem uzņēmuma elementiem. Papildinformāciju par Dynamics 365 finanšu starpuzņēmumu datu koplietošanu skatiet starpuzņēmumu [datu koplietošanu](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

## <a name="key-terms"></a>Galvenie termini

| Termiņš | Apraksts |
|---|---|
| Uzņēmums | Juridiskā persona Dynamics 365 finanšu vidē. |
| Dāvanu karte | Iekšējās Dynamics 365 Commerce dāvanu kartes prece |

## <a name="prerequisites"></a>Priekšnosacījumi

Lietotājiem ir jākonfigurē sava vide starpuzņēmumu datu koplietošanai, kā aprakstīts Starpuzņēmumu [datu koplietošanai](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

**Tabulā RetailGiftCardTable** **lauka DataSharingType** **iestatījumam** ir jābūt Dublēt, lai iespējotu ierakstu kopīgošanas dublikātus (DRS) dāvanu karšu tabulai. Papildinformāciju skatiet starpuzņēmumu [datu koplietošanu izstrādātājiem](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev).

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Konfigurēt starpuzņēmumu datu koplietošanu dāvanu kartēm

Lai konfigurētu starpuzņēmumu datu koplietošanu dāvanu kartēm, sekojiet šiem soļiem.

1. Programmā Commerce headquarters atveriet sadaļu Sistēmas administrēšanas **iestatīšanas \>\> konfigurēšana, lai konfigurētu starpuzņēmumu datu koplietošanu**.
1. Darbību rūtī atlasiet Jauns, lai **pievienotu** datu kopīgošanas ierakstu.
1. Laukā **Nosaukums** ievadiet datu kopīgošanas ieraksta nosaukumu (piemēram, Dāvanu **kartes**).
1. Sadaļā Tabulas **un lauki, ko koplietot**, atlasiet **Pievienot**.
1. Dialoglodziņā Kopīgot jaunu **tabulu** laukā **Tabulas** **nosaukums ievadiet RETAILGIFTCARDTABLE** (mazumtirdzniecības dāvanu karšu tabula). Tabulas **etiķetes** laukam automātiski ir jābūt iestatītam uz **dāvanu karšu tabulu**.
1. Nodrošiniet, lai **būtu atzīmētas izvēles rūtiņas** **Saglabāt datus par uzņēmumu,** **Kuram** ir unikāls indekss un izvēles rūtiņas Vēl nav koplietotas. Šīs izvēles rūtiņas atlase izraisa pārbaudes, kas ir saistītas ar datu kopīgošanas funkcionalitāti.
1. Atlasiet **Pievienot tabulu**. Dāvanu **kartes tabulas (RetailGiftCardTable) ierakstam tagad** ir jāparādās koplietojamajā **sadaļā Tabulas un lauki**. Lai skatītu visus tabulas laukus, kas automātiski ir saistīti ar tabulu koplietošanai, atlasiet zīmi Uzmanība (^).
1. Sadaļā Uzņēmumi **, kas koplieto ierakstus šajās tabulās**, atlasiet **Pievienot**, lai pievienotu uzņēmumu, ar kuru koplietot datus.
1. Rindā zem **Uzņēmums** nolaižamajā sarakstā atlasiet uzņēmumu.
1. Laukā **Nosaukums** ievadiet uzņēmuma nosaukumu.
1. Atkārtojiet no 8. līdz 10. solim, lai pievienotu vairāk uzņēmuma rindu.
1. Kad uzņēmuma rindu pievienošana pabeigta, darbību rūtī atlasiet **Iespējot**.
1. Jūs saņemat brīdinājuma ziņojumu, kas norāda, "Ieteicams šo darbību veikt tikai ārpus darba stundām. Visas vienlaicīgas darbības operācijas neatbilst politikas tabulām. Vai vēlaties turpināt?" Lai **piekrītat,** atlasiet Jā.
1. Jūs saņemat brīdinājuma ziņojumu, ka paziņo, "Vai vēlaties kopēt visus esošos datus visos koplietojamos uzņēmumos tagad?" Lai **piekrītat,** atlasiet Jā.

Kad piekrītat abiem ziņojumiem, tabulas sāks kopēt datus konfigurētos uzņēmumos. Tādā gadījumā otram uzņēmumam būs redzamas bilances, kas ir attiecībā pret viena uzņēmuma dāvanu karti.

## <a name="additional-resources"></a>Papildu resursi

[Bieži uzdotie jautājumi par maksājumiem](payments-retail.md)

[Norēķināšanās modulis](../add-checkout-module.md)

[Maksājumu modulis](../payment-module.md)
