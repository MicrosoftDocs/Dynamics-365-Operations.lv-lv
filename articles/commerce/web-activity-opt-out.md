---
title: Atteikšanās no tīmekļa aktivitāšu notikumu apkopošanas
description: Šajā tēmā skaidrots, kā varat ļaut vietnes apmeklētājiem atteikties no tīmekļa aktivitāšu notikumu kolekcijas programmā Microsoft Dynamics 365 Commerce.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b0e48307527a8fea729d8dfdcdbc6337be0faf1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414069"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Atteikšanās no tīmekļa aktivitāšu notikumu apkopošanas
[!include [banner](includes/banner.md)]

Šajā tēmā izskaidrots, kā varat ļaut klientiem atteikties no tīmekļa aktivitāšu notikumu kolekcijas Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Dynamics 365 Commerce ļauj vietņu administratoriem analizēt lietotāju tīmekļa aktivitātes viņu e-komercijas vietnēs. Tādā veidā viņi var labāk izprast, kā tiek izmantotas viņu vietnes, un viņi var optimizēt vietnes, lai nodrošinātu labāku lietotāja pieredzi un atbilstību biznesa mērķiem.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Veidi, kā administratoriem ieviest atteikšanās iespēju

Administratoriem ir trīs veidi, kādos ieviest atteikšanās iespēju.

### <a name="opt-out-on-behalf-of-users"></a>Atteikšanās lietotāju vārdā

Kontu pārvaldībā Commerce Headquarters (HQ) administratori var atteikties lietotāju vārdā.

1. HQ klientā, lapā **Visi debitori** meklējiet un atlasiet debitoru.
1. Lapā Informācija par klientu, kopsavilkuma cilnes **Retail** sadaļā **Privātums** iestatiet opciju **Neizsekot tīmekļa aktivitātes** uz **Jā**.

    ![Konfidencialitātes iestatījumi](media/Disablepersonalizationpart2.png)

1. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

### <a name="module-based-opt-out-experience"></a>Modulī balstīta atteikšanās iespēja

Administratori var ļaut autentificētajiem lietotājiem pašiem atteikties no tīmekļa aktivitāšu notikumu apkopošanas. Lai nodrošinātu šo atteikšanās iespēju, pievienojiet lietotāja atteikšanās moduli klienta konta profila lapām.

### <a name="custom-extensions"></a>Pielāgoti paplašinājumi

Administratori var izveidot savus paplašinājumus, lai pārvaldītu lietotāju atteikšanās pieredzi. Papildinformāciju skatiet šeit [Retail Server API izsaukšana](e-commerce-extensibility/call-retail-server-apis.md) un [Tiešsaistes kanāla paplašināšana](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]