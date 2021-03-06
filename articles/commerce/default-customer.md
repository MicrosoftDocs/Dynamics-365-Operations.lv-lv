---
title: Noklusējuma debitora izveide
description: Šajā tēmā aprakstīts, kā izveidot noklusējuma klientu, kuru lietot, veidojot kanālu risinājumā Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ecdf4e5618d3397527bf83977857fbe3f8dbb265
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799183"
---
# <a name="create-a-default-customer"></a>Noklusējuma debitora izveide

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot noklusējuma klientu, kuru lietot, veidojot kanālu risinājumā Microsoft Dynamics 365 Commerce.

Veidojot kanālu, būs jānorāda noklusējuma debitors. Noklusējuma debitoru var viegli izveidot, vispirms izveidojot debitoru grupu un debitoru adrešu grāmatu.

## <a name="create-a-customer-group"></a>Debitoru grupas izveidošana

Ja debitoru grupas vēl nepastāv, varat to izveidot. Iespējams izveidot grupas, kas pārstāv dažādas debitoru grupas, piemēram, vairumtirdzniecību, mazumtirdzniecību, inbternetu, darbiniekus u. tml.

Lai izveidotu debitoru grupu, izpildiet tālāk aprakstītās darbības.

1. Navigācijas rūtī ejiet uz **Moduļi \> Mazumtirdzniecība un tirdzniecība \> Debitori \> Debitoru grupas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Lodziņā **Debitoru grupa** ievadiet debitoru grupas ID.
1. Lodziņā **Apraksts** ievadiet atbilstošu aprakstu.
1. Lodziņā **Apmaksas nosacījumi** ievadiet atbilstošu vērtību.
1. Ievadiet atbilstošu vērtību lodziņā **Laiks no rēķina apmaksas datuma līdz maksājuma datumam**.
1. Lodziņā **Noklusējuma nodokļu grupa** ievadiet nodokļu grupu, ja piemērojams.
1. Atlasiet izvēles rūtiņu **Cenā iekļauts PVN**, ja piemērojams.
1. Lodziņā **Noklusējuma norakstīšanas iemesls** ievadiet atbilstošu vērtību, ja piemērojams.

Tālāk redzamajā attēlā ir parādītas vairākas konfigurētās debitoru grupas.

![Debitoru grupas](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>Jaunas debitoru adrešu grāmatas izveide

Debitoram jābūt saistītam ar adrešu grāmatu. Ja tā vēl nav izveidota, tā jāizveido.

Lai izveidotu debitoru grupas adrešu grāmatu, izpildiet tālāk aprakstītās darbības.

1. Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Adrešu grāmatas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Lodziņā **Nosaukums** ievadiet nosaukumu.
1. Lodziņā **Apraksts** ievadiet aprakstu.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā ir parādīts adresu gramatas piemērs.

![Adrešu grāmata](media/address-book.png)

## <a name="create-a-default-customer&quot;></a>Noklusējuma debitora izveide

Lai izveidotu noklusējuma debitoru, izpildiet tālāk aprakstītās darbības.

1. Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Debitori \> Visi debitori**.
1. Darbību rūtī atlasiet **Jauns**.
1. Nolaižamajā sarakstā **Tips** atlasiet &quot;Persona&quot;.
1. Nolaižamajā sarakstā **Debitora konts** atlasiet vai ievadiet konta numuru (piemēram, &quot;100001").
1. Nolaižamajā sarakstā **Vārds** atlasiet vai ievadiet vārdu (piemēram, "Noklusējums").
1. Nolaižamajā sarakstā **Otrais vārds** atlasiet vai ievadiet vārdu (piemēram, "Mazumtirdzniecība").
1. Nolaižamajā sarakstā **Uzvārds** atlasiet vai ievadiet vārdu (piemēram, "Debitors").
1. Nolaižamajā sarakstā **Valūta** atlasiet vai ievadiet valūtu (piemēram, "USD").
1. Nolaižamajā sarakstā **Valūta** atlasiet iepriekš izveidoto debitoru grupu.
1. Nolaižamajā srakstā **Adrešu grāmatas**  atlasiet esošu debitoru adrešu grāmatu.
1. Atlasiet **Saglabāt**, lai saglabātu un atgrieztos debitoru detalizētās informācijas ekrānā pēc jauna debitora.

> [!NOTE]
> Noklusējuma debitoram adrese nav jāpievieno.

Tālāk redzamajā attēlā parādīts debitoru izveides piemērs.

![Noklusējuma debitora izveide](media/default-customer-creation.png)

Tālāk redzamajā attēlā parādīta noklusējuma debitora konfigurācija.

![Debitora konfigurācijas paraugs](media/default-customer-configuration1.png)

Lielākā daļa noklusējuma vērtību debitora detalizētās informācijas ekrānā var palikt, bet ir divas vērtības ir jāmaina.

1. Debitoru detalizētas informācijas ekrānā izvērsiet **Pārdošanas pasūtījuma noklusējumi**.
1. Nolaižamajā sarakstā **Vieta** atlasiet vai ievadiet iepriekš konfigurētu vietu.
1. Nolaižamajā sarakstā **Noliktava** atlasiet vai ievadiet iepriekš konfigurētu noliktavu.

Tālāk redzamajā attēlā parādīts debitoru konfigurācijas piemērs.

![Debitora konfigurācijas piemērs](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>Papildu resursi

[Kanālu apskats](channels-overview.md)

[Uzstādīt kanālu priekšnosacījumus](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
