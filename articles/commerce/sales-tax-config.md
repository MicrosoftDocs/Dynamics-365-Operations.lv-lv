---
title: Konfigurēt PVN tiešsaistes pasūtījumiem
description: Šajā tēmā sniegts pārskats par PVN grupas atlasi dažādiem tiešsaistes pasūtījumu veidiem risinājumā Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 36dd3e8a3d47f02eed5b9c8bb79d773d98069376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254845"
---
# <a name="configure-sales-tax-for-online-orders"></a>Konfigurēt PVN tiešsaistes pasūtījumiem

[!include [banner](includes/banner.md)]

Šajā tēmā sniegts pārskats par PVN grupas atlasi dažādiem tiešsaistes pasūtījumu veidiem risinājumā. 

Jūsu e-tirdzniecības kanāls var vēlēties atbalstīt opcijas, piemēram, piegādāšanu vai saņemšanu tiešsaistes pasūtījumiem. PVN piemērojamība ir balstīta uz opciju, ko atlasa tiešsaistes lietotāji. Kad vietnes klients izvēlas nopirkt preci tiešsaistē un saņem to ar sūtīšanu pa pastu, PVN tiek noteikts, pamatojoties uz klienta piegādes adreses nodokļu grupas iestatījumu. Kad klients vēlas saņemt nopirkto preci veikalā, PVN tiek noteikts, pamatojoties uz saņemšanas veikala nodokļu grupas iestatījumu. 

## <a name="orders-shipped-to-a-customer-address"></a>Pasūtījumi, kas nosūtīti uz klienta adresi 

Parasti nodokļus tiešsaistes pasūtījumiem, kas nosūtāmi uz klienta adresēm, definē adresāts. Katrai PVN grupai ir mazumtirdzniecības mērķa nodokļu konfigurācija, kurā jūsu uzņēmums var definēt adresāta informāciju, piemēram, apgabals/reģions, rajons, apgabals un pilsēta hierarhiskā formā. Kad tiek veikts tiešsaistes pasūtījums, Commerce nodokļu programma izmanto katra pasūtījuma rindas krājuma piegādes adresi un atrod PVN grupas, kas atbilst ar mērķi balstītus nodokļu kritērijus. Piemēram, tiešsaistes pasūtījumam ar rindas krājuma piegādes adresi uz Sanfrancisko, Kalifornijā, nodokļu programma atradīs PVN grupu un PVN kodu Kalifornijā un tad aprēķiniet nodokli katram rindas krājumam atbilstoši.  

## <a name="customer-based-tax-groups"></a>Uz klientu balstītas nodokļu grupas

Commerce Headquarters ir divas vietas, kur ir konfigurētas klientu nodokļu grupas:

- **Klienta profils**
- **Klienta sūtīšanas adrese**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>Ja klienta profilam ir konfigurēta nodokļu grupa

Klienta profila ierakstam galvenajā birojā var būt konfigurēta PVN grupa, tomēr tiešsaistes pasūtījumiem PVN grupa, kas konfigurēta klienta profilā, netiks izmantota nodokļu programmai. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>Ja klienta sūtīšanas adresei ir konfigurēta nodokļu grupa

Ja klienta piegādes adreses ierakstam ir konfigurēta nodokļu grupa un tiešsaistes pasūtījums (vai rindas vienums) tiek nosūtīts uz klienta sūtīšanas adresi, nodokļu grupa, kas konfigurēta klienta adreses ierakstā, tiks izmantota nodokļu aprēķinam.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>Konfigurēt nodokļu grupu klienta sūtīšanas adreses ierakstam

Lai konfigurētu nodokļu grupu klienta sūtīšanas adreses ierakstam sadaļā Commerce Headquarters, veiciet šādas darbības.

1. Dodieties uz **Visi klienti** un pēc tam atlasiet vēlamo klientu. 
1. Kopsavilkuma cilnē **Adreses** atlasiet vēlamo adresi un pēc tam atlasiet **Papildu opcijas \> Papildus**. 
1. Cilnes **Vispārīgi** lapā **Pārvaldīt adreses** iestatiet PVN vērtību pēc nepieciešamības.

> [!NOTE]
> Nodokļu grupa ir definēta, izmantojot pasūtījuma rindas sūtīšanas adresi, un ar mērķi balstīti nodokļi ir konfigurēti pašā nodokļu grupā. Lai iegūtu papildu informāciju, skatiet sadaļu [Nodokļu iestatīšana tiešsaistes veikaliem, kas balstīti uz mērķi](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="order-pickup-in-store"></a>Pasūtījuma saņemšana veikalā

Pasūtījuma rindām ar saņemšanu veikalā vai saņemšanu pa ceļam tiek lietota atlasītā saņemšanas veikala nodokļu grupa. Papildinformāciju par to, kā konfigurēt nodokļu grupu noteiktam veikalam, skatiet sadaļā [Citu nodokļu opciju iestatīšana veikaliem](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

> [!NOTE]
> Kad pasūtījuma rinda tiek saņemta veikalā, tiek lietots klienta adreses nodokļa iestatījums (ja iestatīts), un tiks izmantota saņemšanas veikala nodokļa konfigurācija. 

## <a name="additional-resources"></a>Papildu resursi

[PVN pārskats](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[PVN aprēķināšanas metodes laukā Izcelsme](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[PVN piešķire un pārrakstīšana](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Visas summas un intervāla aprēķināšanas opcijas PVN kodiem](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Nodokļa atbrīvojuma aprēķināšana](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]