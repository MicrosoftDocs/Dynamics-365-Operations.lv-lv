---
title: Piekļuves ierobežošana vitrīnai testēšanas vai izstrādes laikā
description: Šajā tēmā paskaidrots, kā ierobežot piekļuvi Microsoft Dynamics 365 Commerce vitrīnai laikā, kad notiek iekšējā testēšana vai izstrāde.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: db3317c01cab2e123f3c2927c359f9e00b98bd8a2d5e851c2c20cb4763db1c49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716787"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Piekļuves ierobežošana vitrīnai testēšanas vai izstrādes laikā

[!include [banner](../../includes/banner.md)]

Šajā tēmā paskaidrots, kā ierobežot piekļuvi Microsoft Dynamics 365 Commerce vitrīnai laikā, kad notiek iekšējā testēšana vai izstrāde.

## <a name="description"></a>Apraksts

Iekšējās testēšanas vai aktīvas izstrādes laikā, iespējams, vēlēsities ierobežot piekļuvi jūsu vietnei, lai neļautu ārējiem lietotājiem piekļūt publicētajām vitrīnas lapām.

## <a name="resolution"></a>Novēršana

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>Azure AD B2C iestatīšana, izmantojot standarta lietotāju plūsmas

Informāciju par to, kā konfigurēt Azure Active Directory B2C (Azure AD B2C) jūsu e-komercijas vietnei, skatiet sadaļu [B2C nomnieka iestatīšana programmā Commerce](../set-up-b2c-tenant.md).

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>Lietotāju piekļuves vitrīnas lapām ierobežošana un jaunu lietotāju izveides bloķēšana

Lai ierobežotu lietotāju piekļuvi vitrīnas lapām Commerce vietnes veidotājā, veiciet tālāk minētās darbības.

1. Dodieties uz savu vietni.
1. Atlasiet **Lapas** un pēc tam atlasiet lapu, kurai ierobežot lietotāju piekļuvi.
1. Atlasiet moduli vai fragmenta slotu un pēc tam atlasiet **Rediģēt**.
1. Rekvizītu rūtī atlasiet **Nepieciešama pierakstīšanās?** un pēc tam atlasiet **Beigt rediģēšanu**.
1. Atlasiet **Publicēt**.

Lai bloķētu jaunu lietotāju izveidošanu Azure AD, izpildiet tālāk minētās darbības.

1. Dodieties uz [Azure portālu](https://portal.azure.com/).
1. Atlasiet Azure AD B2C programmu, ko izveidojāt jūsu vietnes piekļuvei.
1. Kreisās puses navigācijā atlasiet **Lietotāju plūsmas**.
1. Lapas **Lietotāju plūsmas** augšpusē atlasiet **Jauna lietotāja plūsma**.
1. Lapā **Atlasīt lietotāja plūsmas veidu** atlasiet **Priekšskatījums**.
1. Lapas vidū atlasiet **Pierakstīties v2**. Pēc tam izpildiet darbības sadaļā [B2C nomnieka iestatīšana programmā Commerce](../set-up-b2c-tenant.md), lai konfigurētu plūsmu kā jūsu vietnes standarta lietotāju plūsmu Azure AD B2C testēšanas vai izstrādes laikā.

## <a name="additional-resources"></a>Papildu resursi

[B2C nomnieka iestatīšana programmā Commerce](../set-up-b2c-tenant.md)

[Pielāgotu lapu iestatīšana lietotāja pierakstīšanās gadījumiem](../custom-pages-user-logins.md)
