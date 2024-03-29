---
title: Piekļuves ierobežošana vitrīnai testēšanas vai izstrādes laikā
description: Šajā rakstā ir skaidrots, kā ierobežot Microsoft Dynamics 365 Commerce piekļuvi StoreFront iekšējās testēšanas vai izstrādes laikā.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: e382f01f82b368ad89f7abf122bf806dca4f0340
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292032"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Piekļuves ierobežošana vitrīnai testēšanas vai izstrādes laikā

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir skaidrots, kā ierobežot Microsoft Dynamics 365 Commerce piekļuvi StoreFront iekšējās testēšanas vai izstrādes laikā.

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
