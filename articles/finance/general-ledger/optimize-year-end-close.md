---
title: Gada beigu slēgšanas optimizācija
description: Šajā rakstā ir aprakstīta gada beigu slēgšanas pakalpojuma pievienojumprogramma, kas pieejama Virsgrāmatas gada beigu slēgšanas procesam.
author: moaamer
ms.date: 11/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 41d0c2975341cf3d612cc36be348326e24e94f1b
ms.sourcegitcommit: 707957bb7bcd98faf2600eff1c98067901a0fb73
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/08/2022
ms.locfileid: "9749997"
---
# <a name="optimize-year-end-close"></a>Gada beigu slēgšanas optimizācija

Gada beigu slēgšanas Microsoft Dynamics pakalpojuma pievienojumprogrammas optimizēšana 365 finanšu līdzekļiem ļauj gada beigu slēgšanas apstrādi palaist ārpus Dynamics 365 finanšu resursu Application Object Server (AOS) instances. Tas izmanto mikropakpakaundu tehnoloģiju. Atvieglojumi, kas tiek saistīti ar gada beigu slēgšanas funkcionalitāti, ietver uzlabotu veiktspēju un minimizētu ietekmi uz SQL datu bāzi gada beigu slēgšanas apstrādes laikā.

Lai lietotu gada beigu slēgšanas optimizācijas funkcionalitāti, ir jāveic šādi uzdevumi:

1. Instalējiet gada beigu slēgšanas pakalpojuma pievienojumprogrammu no sava projekta pakalpojumā Microsoft Dynamics Lifecycle Service.
2. Iespējot gada **beigu slēgšanas līdzekli līdzekļu** pārvaldībā.

> [!NOTE]
> Joprojām var izmantot finanšu resursu pašreizējā gada beigu **slēgšanas funkcionalitāti, atspējojot līdzekļu pārvaldības gada beigu** slēgšanas iespēju.

## <a name="improved-performance"></a>Uzlabota veiktspēja

Gada **beigu slēgšanas optimizācijas funkcija** ir izveidota, lai paātrinātu gada beigu slēgšanas apstrādi, it īpaši klientiem, kuriem ir liels datu apjoms. Kad gada beigu aizvēršana darbojas pakalpojumā, liela apstrāde tiek izlādēta no finanšu resursiem, lai palīdzētu samazināt apstrādes laiku un atbrīvot resursus, kas varētu ietekmēt citu lietotāju ikdienas operācijas.

Gada **beigu slēgšanas optimizācijas** funkcija var palīdzēt sasniegt šādus mērķus:

- Uzlabot gada beigu slēgšanas veiktspēju, samazinot izpildlaiku.
- Samaziniet ietekmi uz citiem procesiem gada beigu slēgšanas procesa laikā.
- Uzlabot pārskatus un korekcijas gada beigu rezultātiem, jo gada beigu slēgšanas palaišanai nepieciešams mazāk laika.

## <a name="new-options-and-visibility"></a>Jaunas opcijas un redzamība

Kad ir **iespējota gada beigu slēgšanas optimizēšanas** funkcija, divās jaunās kolonnās – **·** **rezultāti** un statuss tiek pievienotas šādās vietās:

- **Gada beigu slēgšanas** lapā
- **Gada beigu slēgšanas rezultātu** dialoglodziņā
- **Bilances finanšu dimensiju pārsūtīšanas** opcijās **gada beigu slēgšanas veidnes** lapā

Šajā attēlā parādīts rezultātu **un statusa** **kolonnu** piemērs gada **beigu slēgšanas** lapā. Lai atvērtu gada beigu **slēgšanas** rezultātus **,** kolonnā Rezultāti varat atlasīt saiti Skatīt rezultātus. **Statusa** kolonna parāda gada beigu slēgšanas procesa pašreizējo stāvokli. Tāpēc jaunās kolonnas nodrošina redzamību gada beigu slēgšanas procesa norisei.

[![Rezultāti un statusa kolonnas gada beigu slēgšanas lapā.](./media/Yearendclose.jpg)](./media/Yearendclose.jpg)

Turklāt, kad **ir iespējota gada** beigu slēgšanas optimizēšanas funkcija, **·** **kopsavilkuma cilne Bilances finanšu dimensijas kļūst pieejama gada beigu slēgšanas veidnes** lapā. Varat izmantot šo kopsavilkuma cilni, lai norādītu detalizētās bilances finanšu dimensijas, kad aizverat gadu. Šī iespēja ir paralēla spējai, kas jau ir pieejama peļņas un zaudējumu kontiem.

## <a name="architecture-and-data-flow"></a>Arhitektūra un datu plūsma

Lai lietotu **gada** beigu slēgšanas līdzekli un palaistu gada beigu slēgšanas līdzekli mikropakāpē, ir jāinstalē gada beigu slēgšanas pakalpojuma pievienojumprogramma no Lifecycle Services **un** pēc tam jāiespējo līdzekļu pārvaldības gada beigu slēgšanas funkcija.

Kā parādīts šajā ilustrācijā, gada beigu slēgšanas apstrāde pārbauda, vai ir instalēta pievienojumprogramma un funkcionalitāte ir aktivizēta. Ja ir izpildīti abi priekšnosacījumi, gada beigu aizvēršana darbojas mikropakānikā.

[![Datu plūsmas diagramma.](./media/Lifecycle-services.jpg)](./media/Lifecycle-services.jpg)

## <a name="high-level-flow-for-year-end-close-processing"></a>Augsta līmeņa plūsma gada beigu slēgšanas apstrādei

1. Gada beigu slēgšanas process sākas finansēs, **Virsgrāmatas perioda \>\> slēgšanas gada beigās**. Process izveido slēguma pakešuzdevumus un uzdevumus juridiskajām personām, kas tiek slēgtas.
2. Gada beigu slēgšana nosaka, vai gada beigu slēgšana ir jāveic mikropakal šā pakalpojuma vai pašreizējā slēgšanas loģikā.

    - Ja pakalpojumā Lifecycle Services ir instalēta gada beigu slēgšanas pakalpojuma pievienojumprogramma optimizēšana un **līdzekli** Gada beigu slēgšanas optimizēšana ir iespējota līdzekļu pārvaldībā, mikropakošanā tiks palaista gada beigu aizvēršana.

        1. Optimizējiet gada beigu slēgšanas funkcionalitāti izveido gada beigu slēgšanas pakalpojuma darbu katrai juridiskajai personai, kas tiek slēgta, un pēc tam palaiž gada beigu slēgšanas loģiku. Microservice veic gada beigu aizvēršanu.
        2. Finanses noklausās gada beigu slēgšanas par mikropakauti, lai noteiktu, kad mikropakojumā ir pabeigts. Pēc tam gada beigu slēgšanas rezultāti tiek atjaunināti **finanšu gada beigu slēgšanas** lapā.

    - Pretējā gadījumā gada beigu slēgšana tiks izpildīta ar pašreizējo slēgšanas loģiku.
