---
title: Kanāla iestatīšanas priekšnosacījumi
description: Šajā rakstā ir sniegts kanālu iestatīšanas priekšnosacījumu apskats Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 98ca2dc4691534853467c1680890199d08bc4e79
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282300"
---
# <a name="channel-setup-prerequisites"></a>Kanāla iestatīšanas priekšnosacījumi

[!include [banner](includes/banner.md)]

Šajā rakstā ir sniegts kanāla iestatīšanas priekšnosacījumu apskats Microsoft Dynamics 365 Commerce.

Lai varētu programmā Dynamics 365 Commerce izveidot kanālu, ir jāizpilda vairāki priekšnosacījumu uzdevumi. Šādi priekšnosacījumu uzdevumu saraksti ir organizēti pēc kanāla veida.

> [!NOTE]
> Daži dokumenti joprojām tiek ierakstīti, un saites tiks atjauninātas, kad tiek publicēts jauns saturs.

## <a name="initialization"></a>Inicializēšana

- [Inicializēt sākumdatus](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Visi kanālu veidiem nepieciešami globālie priekšnoteikumi

- [Definēt un konfigurēt juridisko personu struktūru](channels-legal-entities.md) 
- [Konfigurēt savas organizāciju hierarhijas](channels-org-hierarchies.md)
- [Noliktavas iestatīšana](channels-setup-warehouse.md)
- [Konfigurēt PVN](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [E-pasta paziņojumu iestatīšana](email-notification-profiles.md)
- [Numuru sēriju iestatīšana](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [Noklusējuma debitora un adrešu grāmatas iestatīšana](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Mazumtirdzniecības kanāla priekšnosacījumi

- [Informācijas kodi un informācijas kodu grupas](info-codes-retail.md)
- [Iestatīt mazumtirdzniecības funkcionalitātes profilu](retail-functionality-profile.md)
- [Darbinieku adrešu grāmatas iestatīšana](new-address-book.md)
- [Iestatīt ekrāna izkārtojumu](pos-screen-layouts.md)
- [Iestatīt aparatūras staciju](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>Zvanu centra kanāla priekšnosacījumi

- Zvanu centra parametri
- [Zvanu centra pasūtījums un atmaksas maksājuma metodes](work-with-payments.md)
- [Zvanu centra piegādes veidi un maksas](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>Tiešsaistes kanāla priekšnosacījumi

- [Izveidot tiešsaistes funkcionalitātes profilu](online-functionality-profile.md)

## <a name="additional-resources"></a>Papildu resursi

[Kanālu apskats](channels-overview.md)

[Organizācijas un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Iestatīt organizāciju hierarhijas](channels-org-hierarchies.md)

[Izveidot juridiskās personas](channels-legal-entities.md)

[Mazumtirdzniecības kanāla iestatīšana](channel-setup-retail.md)
    
[Tiešsaistes veikala iestatīšana](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
