---
title: Kanālu iestatīšanas priekšnosacījumi
description: Šajā tēmā sniegts pārskats par kanālu iestatīšanas priekšnosacījumiem programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002293"
---
# <a name="channel-setup-prerequisites"></a>Kanālu iestatīšanas priekšnosacījumi


[!include [banner](includes/banner.md)]

Šajā tēmā sniegts pārskats par kanāla iestatīšanas priekšnosacījumiem programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Lai varētu programmā Dynamics 365 Commerce izveidot kanālu, ir jāizpilda vairāki priekšnosacījumu uzdevumi. Šādi priekšnosacījumu uzdevumu saraksti ir organizēti pēc kanāla veida.

> [!NOTE]
> Daži dokumenti joprojām tiek ierakstīti, un saites tiks atjauninātas, kad tiek publicēts jauns saturs.

## <a name="initialization"></a>Inicializēšana

- [Inicializēt sākumdatus](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Visi kanālu veidiem nepieciešami globālie priekšnoteikumi

- [Definēt un konfigurēt juridisko personu struktūru](channels-legal-entities.md) 
- [Konfigurēt savas organizāciju hierarhijas](channels-org-hierarchies.md)
- [Noliktavas iestatīšana](channels-setup-warehouse.md)
- [Konfigurēt PVN](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [E-pasta paziņojumu iestatīšana](email-notification-profiles.md)
- [Numuru sēriju iestatīšana](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [Noklusējuma debitora un adrešu grāmatas iestatīšana](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Mazumtirdzniecības kanāla priekšnosacījumi

- [Informācijas kodi un informācijas kodu grupas](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [Iestatīt mazumtirdzniecības funkcionalitātes profilu](retail-functionality-profile.md)
- [Darbinieku adrešu grāmatas iestatīšana](new-address-book.md)
- [Iestatīt ekrāna izkārtojumu](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [Iestatīt aparatūras staciju](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>Zvanu centra kanāla priekšnosacījumi

- Zvanu centra parametri
- Zvanu centra atmaksas metodes
- Nomas tipi
- Maksājumu pakalpojumi
- Pasūtījumu aizturēšanas kodi

## <a name="online-channel-prerequisites"></a>Tiešsaistes kanāla priekšnosacījumi

- [Izveidot tiešsaistes funkcionalitātes profilu](online-functionality-profile.md)

## <a name="additional-resources"></a>Papildu resursi

[Kanālu apskats](channels-overview.md)

[Organizācijas un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Iestatīt organizāciju hierarhijas](channels-org-hierarchies.md)

[Izveidot juridiskās personas](channels-legal-entities.md)

[Mazumtirdzniecības kanāla iestatīšana](channel-setup-retail.md)
    
[Tiešsaistes veikala iestatīšana](channel-setup-online.md)
