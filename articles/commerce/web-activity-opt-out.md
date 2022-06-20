---
title: Atteikšanās no tīmekļa aktivitāšu notikumu apkopošanas
description: Šajā rakstā skaidrots, kā varat ļaut jūsu vietnei izvēlēties no web aktivitāšu notikumu kolekcijas Microsoft Dynamics 365 Commerce.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 78d3f795820eb36d1a81fb28875456e7471f8971
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878403"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Atteikšanās no tīmekļa aktivitāšu notikumu apkopošanas
[!include [banner](includes/banner.md)]

Šajā rakstā skaidrots, kā ļaut debitoriem izvēlēties no web aktivitāšu notikumu kolekcijas Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce ļauj vietņu administratoriem analizēt lietotāju tīmekļa aktivitātes viņu e-komercijas vietnēs. Tādā veidā viņi var labāk izprast, kā tiek izmantotas viņu vietnes, un viņi var optimizēt vietnes, lai nodrošinātu labāku lietotāja pieredzi un atbilstību biznesa mērķiem.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Veidi, kā administratoriem ieviest atteikšanās iespēju

Administratoriem ir trīs veidi, kādos ieviest atteikšanās iespēju.

### <a name="opt-out-on-behalf-of-users"></a>Atteikšanās lietotāju vārdā

Kontu pārvaldībā Commerce Headquarters (HQ) administratori var atteikties lietotāju vārdā.

1. HQ klientā, lapā **Visi debitori** meklējiet un atlasiet debitoru.
1. Lapā Informācija par klientu, kopsavilkuma cilnes **Retail** sadaļā **Privātums** iestatiet opciju **Neizsekot tīmekļa aktivitātes** uz **Jā**.

    ![Konfidencialitātes iestatījumi.](media/Disablepersonalizationpart2.png)

1. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

### <a name="module-based-opt-out-experience"></a>Modulī balstīta atteikšanās iespēja

Administratori var ļaut autentificētajiem lietotājiem pašiem atteikties no tīmekļa aktivitāšu notikumu apkopošanas. Lai nodrošinātu šo atteikšanās iespēju, pievienojiet lietotāja atteikšanās moduli klienta konta profila lapām.

### <a name="custom-extensions"></a>Pielāgoti paplašinājumi

Administratori var izveidot savus paplašinājumus, lai pārvaldītu lietotāju atteikšanās pieredzi. Papildinformāciju skatiet šeit [Retail Server API izsaukšana](e-commerce-extensibility/call-retail-server-apis.md) un [Tiešsaistes kanāla paplašināšana](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
