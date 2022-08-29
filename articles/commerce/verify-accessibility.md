---
title: Lapas satura pieejamības pārbaude
description: Šajā rakstā ir aprakstīts, kā pārbaudīt lapas satura pieejamību Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 686ec37f24cf68902c4dd918c0ca8aea7612e1a9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291978"
---
# <a name="verify-page-content-accessibility"></a>Lapas satura pieejamības pārbaude

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā pārbaudīt lapas satura pieejamību Microsoft Dynamics 365 Commerce.

Kad esat pabeidzis izmainīt lapu, nepieciešams pārliecinieties, vai saturs ir pieejams ikvienam tīmekļa lietotājam. Commerce autorēšanas rīkos varat viegli pārbaudīt lapas satura pieejamību, izmantojot integrēto pakalpojumu [Microsoft Accessibility Insights](https://accessibilityinsights.io/). Šis pakalpojums pārbauda jūsu lapas saturu, izmantojot jaunākās [Globālā tīmekļa konsorcija (World Wide Web Consortium — W3C) pieejamības](https://www.w3.org/standards/webdesign/accessibility) vadlīnijas.

Lai varētu to izmantot, jāieslēdz [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integrācija nomnieka vai vietnes līmenī.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Microsoft Accessibility Insights ieslēgšana visām jūsu nomnieka vietnēm

Lai ieslēgtu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integrāciju visām jūsu nomnieka Commerce vietnēm, veiciet tālāk minētās darbības.

> [!NOTE]
> Lai piekļūtu nomnieka iestatījumiem, jums ir jāpierakstās Commerce kā sistēmas administratoram.

1. Pierakstieties Commerce kā sistēmas administrators.
1. Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.
1. **Nomnieka iestatījumi** atlasiet **Līdzekļi**.
1. Iestatiet opciju **Pieejamības pārbaude** kā **Ieslēgts**.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Microsoft Accessibility Insights ieslēgšana vienai vietnei

Lai ieslēgtu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integrāciju vienai Commerce vietnei, veiciet tālāk minētās darbības.

1. Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Kreisās puses navigācijas rūtī atlasiet **Vietnes iestatījumi**, lai to izvērstu.
1. **Vietnes iestatījumi** atlasiet **Līdzekļi**.
1. Iestatiet opciju **Pieejamības pārbaude** kā **Ieslēgts**.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>Sākumlapas satura pieejamības pārbaude

Lai izmantotu integrēto [Microsoft Accessibility Insights](https://accessibilityinsights.io/) pakalpojumu sākumlapas satura skenēšanai un pārbaudei Commerce, veiciet tālāk minētās darbības.

1. Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Kreisās puses navigācijas rūtī atlasiet **Lapas**.
1. Atrodiet un atlasiet sākumlapu, lai to atvērtu to lapas redaktorā.
1. Komandjoslā atlasiet **Pārbaudīt pieejamību**. Tiek parādīta lapa **Pārbaudīt pieejamību**.
1. Pēc skenēšanas pabeigšanas apskatiet pārskata saturu.
1. Ja kāda pārbaude nav izdevusies, atlasiet katru neizdevušos pārbaudes vienumu, lai to izvērstu un varētu skatīt detalizētu informāciju.
1. Lai pēc pārskata apskatīšanas to aizvērtu, ritiniet līdz lapas **Pārbaudīt pieejamību** apakšai un atlasiet **Labi**.

## <a name="additional-resources"></a>Papildu resursi

[Esošās vietnes lapas modificēšana](modify-existing-page.md)

[Jaunas vietnes lapas pievienošana](add-new-page.md)

[Lapas izkārtojumu atlase](select-page-layouts.md)

[SEO metadatu pārvaldība](manage-seo-metadata.md)

[Lapas saglabāšana, priekšskatīšana un publicēšana](save-preview-publish-page.md)

[Preces lapas papildināšana](enrich-product-page.md)

[Kategorijas ielādes lapas papildināšana](enrich-category-page.md)

[Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
