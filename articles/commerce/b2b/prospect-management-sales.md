---
title: Pārvaldīt biznesa partnera lietotājus B2B e-komercijas vietnēs, izmantojot Dynamics 365 Pārdošanu
description: Šajā tēmā ir aprakstīts, kā Microsoft Dynamics izmantot 365 pārdošanu, lai pārvaldītu biznesa partnera apstiprinājumus "bizness-biznesam Dynamics 365 Commerce " vietnēs.
author: shajain
ms.date: 2/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c6ac5409de5101c91b9348de800e3eaea9895c23
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312137"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Pārvaldīt biznesa partnera lietotājus B2B e-komercijas vietnēs, izmantojot Dynamics 365 Pārdošanu

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā Microsoft Dynamics izmantot 365 pārdošanu, lai pārvaldītu biznesa partnera apstiprinājumus "bizness-biznesam Dynamics 365 Commerce " vietnēs. Organizācijas, kas jau ir palīdzēs Dynamics 365 pārdošanas risinājumā, var izmantot tā potenciālo klientu un iespēju koncepcijas B2B e-komercijas biznesa partnera apstiprināšanas procesam.

Pamatinformāciju par B2B biznesa partnera apstiprināšanas procesu skatiet [Sadaļā Biznesa partnera lietotāju pārvaldība B2B e-komercijas vietnēs](manage-b2b-users.md).

Potenciālie biznesa partneri var uzsākt uzņēmumā esošās darbības procesu B2B e-komercijas vietnē, iesniedzot onboarding pieprasījumu, izmantojot saiti B2B vietnē. Pēc pieprasījuma iesniegšanas un programmā Commerce headquarters tiek saglabāti atbilstošie darbi (**piemēram, P-0001** **un** Sinhronizēt pasūtījumus un kanāla pieprasījumus **),** uzņēmuma pieprasījums tiek saglabāts Commerce Headquarters lapā Visi potenciālie klients. Pēc tam biznesa partnera potenciālā klienta apstiprināšanas procesu var pabeigt sadaļā Pārdošana.

Kad pārdošana un komercija ir aktivizēta integrācija, biznesa partnera potenciālā klienta izveide Pārdošanā izraisa potenciālā klienta *izveidi* Pārdošanā.

Šajā attēlā parādīts potenciālā klienta izveides lapas piemērs biznesa partnera paredzamam klientam Pārdošanā.

![Potenciālā klienta izveides lapa sistēmā Dynamics 365 Pārdošana.](../media/LeadInSales.png)

Šajā ilustrācijā kontaktpersonas **sadaļā** parādīta persona, kas iesniedza uzņēmuma pieprasījumu, un sadaļa **Uzņēmums** parāda organizāciju. Piezīme sadaļā Laika skala **norāda**, ka potenciālais klientam tika izveidots, izmantojot duālās rakstīšanas infrastruktūru. Tā kā to izveidoja dubultās rakstīšanas infrastruktūra, tad šis potenciālais klienta saraksts nebūs **redzams nolaižamajā sarakstā Mani** atvērtie potenciālie klienti. Tā vietā tas tiks parādīts jaunā skatījumā, kura nosaukums ir Visi **commerce B2B potenciālie klienti**.

Pēc standarta potenciālā klienta kvalifikācijas procesa pārdošanā, kad lietotājs "kvalificē" potenciālo klientu, *iespējas* ierakstu, *·* *kontaktpersonas* ierakstu un konta ierakstu tiek izveidots. Dubultās rakstīšanas infrastruktūra tiek izmantota, lai ierakstītu kontaktus un konta ierakstus Commerce. Kontaktpersona tiek izveidota kā personas tipa *debitors*, un uzņēmums ir izveidots kā organizācijas tipa *debitors*. Ja lietotājs iespējai atlasa Aizvērt kā uzvarētu **, potenciālais klients tiek apstiprināts** commerce. Potenciālā klienta apstiprināšana liek izveidot debitoru hierarhiju.

Visi atlikušie biznesa procesi parādās Commerce. Šie procesi ietver e-pasta sūtīšanu biznesa partnerim, kredīta limita pārvaldības definēšanu lietotājiem un papildu lietotāju pievienošanu B2B vietnei. Tomēr, ja lietotājs diskvalificē potenciālo klientu vai atzīmē iespēju kā zaudētu, tā vietā, lai kvalificētu potenciālo klientu, Commerce ir atzīmēts kā noraidīts, un pieprasītājam tiek nosūtīts noraidījums uz uzņēmuma e-pastu.

## <a name="enable-integration-between-sales-and-commerce"></a>Iespējot integrāciju starp pārdošanu un commerceu

Integrācija starp pārdošanu un tirdzniecību balstās uz dubulto rakstīšanas infrastruktūru. Tāpēc ir jābūt iespējotai duālām rakstiet un jādarbojas tā, lai vienā sistēmā izveidotie debitori tiktu ierakstīti citā sistēmā. Papildinformāciju par dubultās rakstīšanas infrastruktūru skatiet duālās [rakstīšanas pārskatā](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview).

Kad duālās rakstīšanas iestatīšana ir pabeigta, [Microsoft AppSource](https://appsource.microsoft.com/)[ieviešanas partneris var doties uz un meklēt risinājumu, kas tiek saukts par Dual-write Commerce risinājumiem](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview). Instalējiet pakotni, izmantojot standarta instalācijas vedni, un pēc tam pārbaudiet to, izveidojot potenciālo klientu B2B vietnē. Pēc potenciālā klienta izveidošanas pārbaudiet, **vai pieprasījums ir parādīts uz Visi potenciālie klients, kas redzams Pārdošanā, un pēc tam pārbaudiet, vai potenciālais klients pārdošanā ir rādīts** kā potenciālais klients.

## <a name="additional-resources"></a>Papildu resursi

[Biznesa partneru lietotāju pārvaldīšana B2B e-komercijas tīmekļa vietnēs](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
