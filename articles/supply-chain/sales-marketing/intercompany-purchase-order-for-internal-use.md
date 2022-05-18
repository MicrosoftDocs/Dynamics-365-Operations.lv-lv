---
title: Starpuzņēmumu pirkšanas pasūtījuma izveide un rēķina izrakstīšanai iekšējai lietošanai
description: Šajā tēmā skaidrots, kā izveidot un izrakstīt rēķinu starpuzņēmumu pārdošanas pasūtījumam iekšējai lietošanai
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 52b58b2dcecd5d9a83a47b425d6fb13b36c40b60
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675884"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>Starpuzņēmumu pirkšanas pasūtījuma izveide un rēķina izrakstīšanai iekšējai lietošanai

[!include [banner](../../includes/banner.md)]

Varat izveidot starpuzņēmumu pirkšanas pasūtījumu starpuzņēmumu kreditoram. Tā automātiski tiek izveidots starpuzņēmumu pārdošanas pasūtījums starpuzņēmumu kreditoram.

![Starpuzņēmumu iekšējās pirkšanas process](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>Starpuzņēmumu pārdošanas pasūtījuma un atbilstoša starpuzņēmumu pārdošanas pasūtījuma izveide

Izpildiet attēlā parādītās darbības juridiskajā personā AAA.

1. Atlasiet **Kreditori** \> **Pirkšanas pasūtījumi** \> **Visi pirkšanas pasūtījumi**.
1. Saraksta lapā **Visi pirkšanas pasūtījumi** izveidojiet pirkšanas pasūtījumu starpuzņēmumu kreditoram. Lauka vērtības tiek kopētas no kreditora konta uz pirkšanas pasūtījumu.

    Tā kā jūs strādājat ar starpuzņēmumu kreditoru, kreditoram atbilstošajā juridiskajā personā tiek izveidots starpuzņēmumu pārdošanas pasūtījums. Starpuzņēmumu pārdošanas pasūtījuma numurs var būt tāds pats kā starpuzņēmumu pirkšanas pasūtījumam, un tajā var būt iekļauts juridiskās personas ID. Izmantotā numura struktūra ir atkarīga no atlases laukā **Pārdošanas pasūtījuma secība** lapā **Starpuzņēmums**. Piemēram, ja izveidojat pirkšanas pasūtījumu 00029\_064 juridiskajā personā AAA, pārdošanas pasūtījuma numurs juridiskajā personā BBB ir AAA00029\_64.

    Informatīvs ziņojums pavēsta, ka starpuzņēmumu pirkšanas pasūtījums un starpuzņēmumu pārdošanas pasūtījums ir izveidots. Ziņojums ietver starpuzņēmumu pārdošanas pasūtījuma numuru.

1. Pievienojiet rindas krājumus pirkšanas pieprasījumam. Atbilstošie rindas krājumi tiek automātiski pievienoti starpuzņēmumu pārdošanas pasūtījumam. Ja krājums nepastāv citā juridiskajā personā, tiek parādīts ziņojums, un krājumu nevar pievienot pirkšanas pasūtījumam. Lai novērstu šo problēmu, pārejiet uz citu juridisko personu un nododiet preci izpildei šai juridiskajai personai. Krājums būs pieejams, lai to pievienotu šīs juridiskās personas pārdošanas pasūtījumiem. Pēc tam pārslēdzieties atpakaļ uz pirkšanas pasūtījuma juridisko personu un turpiniet pievienot rindu krājumus.
1. Kad esat beidzis ievadīt informāciju par pirkšanas pasūtījumu, apstipriniet to.

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>Starpuzņēmumu pavadzīmes un debitora rēķina apstrāde

Izpildiet attēlā parādītās darbības juridiskajā personā BBB.

1. Doties uz **Debitoru parādi \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atgriezieties lapā **Visi pārdošanas pasūtījumi** un vēlreiz atlasiet starpuzņēmumu pārdošanas pasūtījumu.
1. Darbību rūtī atlasiet cilni **Izdot un iepakot** un pēc tam atlasiet **Pavadzīme**.
1. Atzīmējiet izvēles rūtiņu **Grāmatot**.
1. Atlasiet **Labi**. Juridiskajā personā BBB tiek iegrāmatota pavadzīme.
1. Atgriezieties lapā **Visi pārdošanas pasūtījumi** un vēlreiz atlasiet starpuzņēmumu pārdošanas pasūtījumu.
1. Darbības rūtī atlasiet cilni **Rēķins** un pēc tam vēlreiz atlasiet **Rēķins**.
1. Atzīmējiet izvēles rūtiņu **Grāmatot**.
1. Atlasiet **Labi**.

    Debitora rēķins starpuzņēmumu pārdošanas pasūtījumam tiek iegrāmatots juridiskajā personā BBB.

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>Starpuzņēmumu produktu ieejas plūsmas un kreditora rēķina apstrāde

Izpildiet attēlā parādītās darbības juridiskajā personā AAA.

1. Dodieties uz **Kreditori \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Atgriezieties lapā **Visi pārdošanas pasūtījumi** un vēlreiz atlasiet starpuzņēmumu pārdošanas pasūtījumu.
1. Darbības rūtī atlasiet **Saņemt** un pēc tam vēlreiz atlasiet **Produktu ieejas plūsma**. Produktu ieejas plūsma ir izveidota. Produktu ieejas plūsmas numurs ir tāds pats kā starpuzņēmumu pavadzīmes numurs.
1. Atzīmējiet izvēles rūtiņu **Grāmatot**.
1. Atlasiet **Labi**.
1. Atgriezieties lapā **Visi pārdošanas pasūtījumi** un vēlreiz atlasiet starpuzņēmumu pārdošanas pasūtījumu.
1. Darbības rūtī atlasiet **Rēķins** un pēc tam vēlreiz atlasiet **Rēķins**. Kreditora rēķins ir izveidots. Kreditora rēķina numurs ir tāds pats kā starpuzņēmumu debitora rēķina numurs.
1. Pabeidziet ievadīt kreditora rēķinu, un pēc tam iegrāmatojiet to.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
