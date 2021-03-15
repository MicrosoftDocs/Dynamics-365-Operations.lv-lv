---
title: Virsgrāmatas grāmatošanas grupu izveide pievienotās vērtības nodoklim
description: PVN tiek aprēķināts un iegrāmatots galvenajos kontos, kas ir norādīti Virsgrāmatas grāmatošanas grupās.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6cc96cbdb11f24d727bddfa5fd4aaa579537802a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968458"
---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Virsgrāmatas grāmatošanas grupu izveide pievienotās vērtības nodoklim

[!include [banner](../../includes/banner.md)]

PVN tiek aprēķināts un iegrāmatots galvenajos kontos, kas ir norādīti Virsgrāmatas grāmatošanas grupās. Virsgrāmatas grāmatošanas grupas ir piesaistītas katram PVN kodam. Varat iestatīt atsevišķas Virsgrāmatas grāmatošanas grupas katram PVN kodam, izmantot vienu virsgrāmatas grāmatošanas grupu visiem PVN kodiem vai PVN kodiem piešķirt vairākas Virsgrāmatas grāmatošanas grupas. Šis paraugs izmanto DEMF demonstrācijas uzņēmumu. 

1. Pārejiet uz **Navigācijas rūts > Moduļi > Nodoklis > Iestatīšana > PVN > Virsgrāmatas grāmatošanas grupas**.
2. Klikšķiniet **Jauns**.
3. Laukā **Virsgrāmatas grāmatošanas grupas** ierakstiet vērtību.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Laukā **Maksājamais PVN** izvēlieties galveno kontu izejošajiem PVN, kas jāmaksā nodokļu administrācijai. PVN tiek iekasēts nodokļu iestādes vietā, ja pārdodat ar nodokli apliekamas preces un pakalpojumus.  
6. Laukā **Saņemamais PVN** izvēlieties galveno kontu ienākošajiem PVN, kas jāsaņem no nodokļu administrācijas. Kreditori iekasē nodokli nodokļu iestādes vārdā, ja pērkat ar nodokli apliekamas preces un pakalpojumus. Šis lauks nav pieejams, ja lapā **Virsgrāmatas parametri** ir atlasīta opcija Piemērot PVN nodokļu sistēmas kārtulas. Tā vietā PVN, kas tiek maksāts kreditoriem, tiek debetēts tajā pašā kontā, kurā pirkums.   
7. Laukā **Izmantošanas nodokļa izdevumi** atlasiet galveno kontu atskaitāmo izmantošanas nodokļu grāmatošanai, kurus pārdevēji nepieprasa vai par kuriem nodokļu administrācijai nav ziņots kā par daļu no ES apgrieztās iekasēšanas GST/HST. Opcijai **Izmantošanas nodoklis** ir jābūt atlasītai, lai izmantotu lauku **PVN kods** sadaļā **PVN grupa**, kas tiek izmantota darījumā. Šis lauks nav pieejams, ja lapā **Virsgrāmatas parametri** ir atlasīta opcija **Piemērot PVN nodokļu sistēmas kārtulas**.   
8. Laukā **Maksājamais izmantošanas nodoklis** izvēlieties galveno kontu ienākošo izmantošanas nodokļu grāmatošanai, kuri ir jāmaksā nodokļu administrācijai. Opcijai **Izmantošanas nodoklis** ir jābūt atlasītai, lai izmantotu lauku **PVN kods** sadaļā **PVN grupa**, lai grāmatotu **Izmantošanas nodokli**. Ja opcija **Piemērot PVN nodokļu sistēmas kārtulas** ir atlasīta lapā **Virsgrāmatas parametri** nobīde tiek grāmatota darījuma izdevumu kontā.   
9. Laukā **Norēķinu konts** atlasiet galveno kontu, kas ir virsgrāmatu kontu neto atlikums, kas norādīts laukos **Maksājamais izmantošanas nodoklis** un **Saņemamais PVN**. Atlikums tiks izveidots, kad tiks nokārtots PVN un grāmatošanas uzdevums ir izpildīts.  Ja nodokļu administrācija norēķinu periodā ir saistīta ar pārdevēja kontu, atlikums tiek nosūtīts uz pārdevēja kontu.
10. Laukā **Pārdevēja skaidras naudas atlaide** atlasiet galveno kontu, lai grāmatotu skaidras naudas atlaidi PVN kodiem, kas saistīti ar šīs virsgrāmatas grāmatošanas grupu. Šī ir izvēles opcija, un, ja netiek ievadīts neviens konts, opcijai **Skaidras naudas atlaižu kodi** tiks izmantots galvenais konts. Var būt noderīgi katrai **Virsgrāmatas grāmatošanas grupai** izmantot citu kontu, ja tiek izmantots apgrieztais PVN skaidras naudas atlaides opcijai PVN grupās.  
11. Laukā **Klienta pieteikuma atlaide** atlasiet galveno kontu, lai grāmatotu skaidras naudas atlaidi **PVN kodiem**, kas saistīti ar šīs **Virsgrāmatas grāmatošanas grupu**. Šī ir izvēles opcija, un, ja netiek ievadīts neviens konts, opcijai **Skaidras naudas atlaižu kodi** tiks izmantots galvenais konts. Var būt noderīgi katrai **Virsgrāmatas grāmatošanas grupai** izmantot citu kontu, ja tiek izmantots apgrieztais PVN skaidras naudas atlaides opcijai **PVN grupās**.  
12. Noklikšķiniet uz **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]