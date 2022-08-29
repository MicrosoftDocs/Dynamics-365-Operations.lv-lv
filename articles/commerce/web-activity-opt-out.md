---
title: Atteikšanās no tīmekļa aktivitāšu notikumu apkopošanas
description: Šajā rakstā skaidrots, kā varat ļaut jūsu vietnei izvēlēties no web aktivitāšu notikumu kolekcijas Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 81343f5033366484140f73fcc313ecd9f35e7d47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286730"
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
