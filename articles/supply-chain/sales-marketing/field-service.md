---
title: Pārskats par integrāciju ar Microsoft Dynamics 365 Field Service
description: Šajā tēmā ir sniegts apskats par integrāciju ar Microsoft Dynamics 365 Field Service.
author: Henrikan
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 23661bca91ccd7b7a04c763e60cfca9a99d62bfa
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566459"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Pārskats par integrāciju ar Microsoft Dynamics 365 Field Service

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Supply Chain Management nodrošina biznesa procesu sinhronizāciju programmās Dynamics 365 Supply Chain Management un Dynamics 365 Field Service. Integrācijas scenāriji tiek konfigurēti, izmantojot paplašināmas datu integrētāja veidnes un Microsoft Dataverse , lai iespējotu biznesa procesu sinhronizāciju.
Standarta veidnes var izmantot, lai izveidotu pielāgotus integrācijas projektus, kuros var kartēt papildu standarta un pielāgotas kolonnas, kā arī tabulas, lai pielāgotu integrāciju un nodrošinātu īpašu biznesa prasību izpildi. 

Papildus jau esošajai funkcionalitātei “No potenciālā klienta līdz skaidrai naudai” veidojas Field Service integrācija.

![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/field-service-integration.png)

Pirmā integrācijas fāze risinājumos Field Service un Supply Chain Management attiecas uz to, lai darba pasūtījumus un līgumus risinājumā Field Service varētu iekļaut rēķinos risinājumā Supply Chain Management. Atbalstītā plūsma sākas risinājumā Field Service, kur informācija no darba pasūtījumiem tiek sinhronizēta risinājumā Supply Chain Management kā pārdošanas pasūtījumi. Supply Chain Management pārdošanas pasūtījumi tiek iekļauti rēķinā, lai ģenerētu rēķinu dokumentus. Turklāt informācija no Field Service līguma rēķiniem tiek sinhronizēta risinājumā Supply Chain Management. Microsoft Dynamics 365 datu integrētājs sinhronizē datus, izmantojot pielāgojamus projektus. Standarta veidnes var izmantot, lai izveidotu pielāgotus integrācijas projektus, kuros var kartēt papildu standarta un pielāgotas kolonnas, kā arī tabulas, lai pielāgotu integrāciju un nodrošinātu īpašu prasību izpildi.

Pirmā integrācijas fāze risinājumos Field Service un Supply Chain Management ļauj sinhronizēt šādus vienumus:

- [Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Field Service](field-service-product.md)
- [Sinhronizējiet darba pasūtījumus risinājumā Field Service ar pārdošanas pasūtījumiem risinājumā Supply Chain Management](field-service-work-order.md)
- [Sinhronizējiet līguma rēķinus risinājumā Field Service ar brīva teksta rēķiniem risinājumā Supply Chain Management](field-service-invoice.md)

Piemēru tam, kā varat sinhronizēt darba pasūtījumu programmās Field Service un Supply Chain Management, noskatieties īsajā YouTube video [Darba pasūtījuma sinhronizēšana, izmantojot Microsoft Dynamics 365 integrāciju](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Integrācija ar Field Service, ietverot krājumu un projekta informāciju

Papildu funkcionalitātes pievienošana šajā otrajā posmā bija koncentrēta uz to, lai nozares speciālistiem sniegtu ieskatu par Supply Chain Management krājumu informāciju, kas ļautu atjaunināt krājumu līmeņus un veikt izejmateriālu pārsūtīšanu. Turklāt uzņēmumi, kas nodarbojas ar pārdoto preču uzstādīšanu vai apkalpošanu, gūs tādas priekšrocības kā labāku pārvaldību un redzamību, kā arī pilnīgu pārdošanas un pakalpojumu procesu ar integrāciju no projektiem.

### <a name="functionality-includes-integration-of"></a>Funkcionalitāte ietver integrāciju ar šādiem elementiem:
- Noliktavas informācija
- Rīcībā esošo krājumu informācija
- Krājumu pārsūtīšana
- Krājumu pārrēķini
- Supply Chain Management projekti, kas ir saistīti ar Dynamics 365 Field Service darba pasūtījumiem
- Dynamics 365 Field Service darba pasūtījumi ar saiti uz Supply Chain Management projektiem — lietot šo projekta numuru pārdošanas pasūtījumam, lai iespējotu rēķinu izrakstīšanu projekta ietvaros. 

![Biznesa procesu sinhronizācija starp Supply Chain Management un Field Service, tai skaitā inventāra un projekta informāciju.](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Otrais integrācijas posms risinājumos Field Service un Supply Chain Management ļauj sinhronizēt šādas veidnes:
- Noliktavas (Supply Chain Management uz Field Service) — Noliktavas no Supply Chain Management uz Field Service [Paplašinātais vaicājums] 
- Preču krājumi (Supply Chain Management uz Field Service) — Krājumu līmeņa informācija no Supply Chain Management uz Field Service [Paplašinātais vaicājums] 
- Krājumu korekcija (Field Service uz Supply Chain Management) — Krājumu korekcijas no Field Service uz Supply Chain Management [Paplašinātais vaicājums] 
- Krājumu pārsūtīšana (Field Service uz Supply Chain Management) — Krājumu pārsūtīšana no Field Service uz Supply Chain Management [Paplašinātais vaicājums] 
- Projekti (Supply Chain Management uz Field Service) — Projektu saraksts no Supply Chain Management uz Field Service 
- Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management) — darba pasūtījumi no Field Service uz Pārdošanas pasūtījumiem programmā Supply Chain Management ar atbalstu projektam [Paplašinātais vaicājums] 
- Field Service preces ar krājumu uzskaites vienību (no Supply Chain Management uz Sales) — Supply Chain Management 'Pārdodamo izlaisto preču' sinhronizācija ar Field Service pārdošanas precēm, ieskaitot krājuma uzskaites vienības 

## <a name="system-requirements"></a>Sistēmas prasības

### <a name="system-requirements-for-supply-chain-management"></a>Supply Chain Management sistēmas prasības
Field Service integrācija atbalsta šādas versijas.

- Dynamics 365 for Finance and Operations versija 8.1.2 (2018. gada decembris), kas ir izlaista 2018. gada decembrī, ar lietojumprogrammas būvējuma Nr. 8.1.195 ar platformas atjauninājumu 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Sistēmas prasības risinājumam Field Service
Lai lietotu Field Service integrācijas risinājumu, ir jābūt instalētiem tālāk minētajiem komponentiem.

- Field Service (versija 8.2.0.286) vai jaunāka versija programmā Dynamics 365 9.1.x — izlaista 2018. gada novembrī
- Risinājums “No potenciālā klienta līdz skaidrai naudai” (P2C) programmai Dynamics 365, versija 1.15.0.1 vai jaunāka. Risinājumu var lejupielādēt no pakalpojuma [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Risinājums “Field Service integrācija, projekts un krājumi” programmai Dynamics 365, versija 2.0.0.0 vai jaunāka. Risinājumu var lejupielādēt no pakalpojuma [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]