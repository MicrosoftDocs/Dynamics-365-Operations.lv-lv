---
title: Pārskats par integrāciju ar Microsoft Dynamics 365 for Field Service
description: Šajā tēmā ir sniegts apskats par integrāciju ar Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 22abe83f06b7fc57c73fb82ccafc4b426667e7c6
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865207"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service-overview"></a>Pārskats par integrāciju ar Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations nodrošina biznesa procesu sinhronizāciju programmās Finance and Operations un Microsoft Dynamics 365 for Field Service. Integrācijas scenāriji tiek konfigurēti, izmantojot paplašināmas datu integrētāja veidnes un Common Data Service (CDS), lai iespējotu biznesa procesu sinhronizāciju.
Standarta veidnes var izmantot, lai izveidotu pielāgotus integrācijas projektus, kuros var kartēt papildu standarta un pielāgotus laukus, kā arī entītijas, lai pielāgotu integrāciju un nodrošinātu īpašu biznesa prasību izpildi. 

Papildus jau esošajai funkcionalitātei “No potenciālā klienta līdz skaidrai naudai” veidojas Field Service integrācija.

![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/field-service-integration.png)

Pirmā integrācijas fāze risinājumos Field Service un Finance and Operations attiecas uz to, lai darba pasūtījumus un līgumus risinājumā Field Service varētu iekļaut rēķinos risinājumā Finance and Operations. Atbalstītā plūsma sākas risinājumā Field Service, kur informācija no darba pasūtījumiem tiek sinhronizēta risinājumā Finance and Operations kā pārdošanas pasūtījumi. Risinājumā Finance and Operations pārdošanas pasūtījumi tiek iekļauti rēķinos, lai izveidotu rēķinu dokumentus. Turklāt informācija no Field Service līguma rēķiniem tiek sinhronizēta risinājumā Finance and Operations. Microsoft Dynamics 365 datu integrētājs sinhronizē datus, izmantojot pielāgojamus projektus. Standarta veidnes var izmantot, lai izveidotu pielāgotus integrācijas projektus, kuros var kartēt papildu standarta un pielāgotus laukus, kā arī entītijas, lai pielāgotu integrāciju un nodrošinātu īpašu prasību izpildi.

Pirmā integrācijas fāze risinājumos Field Service un Finance and Operations ļauj sinhronizēt šādus vienumus:

- [Risinājumā Finance and Operations ietvertās preces ar precēm risinājumā Field Service, kuras ietver informāciju par preces tipu](field-service-product.md)
- [Risinājumā Field Service ietvertie darba pasūtījumi ar pārdošanas pasūtījumiem risinājumā Finance and Operations](field-service-work-order.md)
- [Risinājumā Field Service ietvertie rēķini ar brīva teksta rēķiniem risinājumā Finance and Operations](field-service-invoice.md)

Piemēru tam, kā varat sinhronizēt darba pasūtījumu programmās Field Service un Finance and Operations, noskatieties īsajā YouTube video [Darba pasūtījuma sinhronizēšana, izmantojot Microsoft Dynamics 365 integrāciju](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Integrācija ar Microsoft Dynamics 365 for Field Service, ietverot krājumu un projekta informāciju

Papildu funkcionalitātes pievienošana šajā otrajā posmā bija koncentrēta uz to, lai nozares speciālistiem sniegtu ieskatu par Finance and Operations krājumu informāciju, kas ļautu atjaunināt krājumu līmeņus un veikt izejmateriālu pārsūtīšanu. Turklāt uzņēmumi, kas nodarbojas ar pārdoto preču uzstādīšanu vai apkalpošanu, gūs tādas priekšrocības kā labāku pārvaldību un redzamību, kā arī pilnīgu pārdošanas un pakalpojumu procesu ar integrāciju no projektiem.

### <a name="functionality-includes-integration-of"></a>Funkcionalitāte ietver integrāciju ar šādiem elementiem:
- Noliktavas informācija
- Rīcībā esošo krājumu informācija
- Krājumu pārsūtīšana
- Krājumu pārrēķini
- Dynamics 365 for Finance and Operations projekti, kas ir saistīti ar Dynamics 365 for Field Service darba pasūtījumiem
- Dynamics 365 for Field Service darba pasūtījumi ar saiti uz Dynamics 365 for Finance and Operations projektiem — lietot šo projekta numuru Dynamics 365 for Finance and Operations pārdošanas pasūtījumam, lai iespējotu rēķinu izrakstīšanu projekta ietvaros. 

![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Otrais integrācijas posms risinājumos Field Service un Finance and Operations ļauj sinhronizēt šādas veidnes:
- Noliktavas (no risinājuma Finance and Operations risinājumā Field Service) — noliktavu informācijas sinhronizācija no risinājuma Finance and Operations risinājumā Field Service [Paplašinātais vaicājums] 
- Preču krājumi (no risinājuma Finance and Operations risinājumā Field Service) — krājumu līmeņa informācijas sinhronizācija no risinājuma Finance and Operations risinājumā Field Service [Paplašinātais vaicājums] 
- Krājumu korekcija (no risinājuma Field Service risinājumā Finance and Operations) — krājumu korekcijas informācijas sinhronizācija no risinājuma Field Service risinājumā Finance and Operations [Paplašinātais vaicājums] 
- Krājumu pārsūtīšana (no risinājuma Field Service risinājumā Finance and Operations) — krājumu pārsūtīšanas informācijas sinhronizācija no risinājuma Field Service risinājumā Finance and Operations [Paplašinātais vaicājums] 
- Projekti (no risinājuma Finance and Operations risinājumā Field Service) — projektu informācijas sinhronizācija no risinājuma Finance and Operations risinājumā Field Service 
- Darba pasūtījumi ar projektu (no risinājuma Field Service risinājumā Finance and Operations) — darba pasūtījumu informācijas no risinājuma Field Service sinhronizācija ar pārdošanas pasūtījumu informāciju risinājumā Finance and Operations ar atbalstu projektam [Paplašinātais vaicājums] 
- Field Service preces ar krājumu uzskaites vienību (no risinājuma Finance and Operations uz pārdošanu) — risinājuma Finance and Operations pārdodamo izlaisto preču sinhronizācija ar risinājuma Field Service pārdošanas precēm, ieskaitot krājuma uzskaites vienības 

## <a name="system-requirements"></a>Sistēmas prasības

### <a name="system-requirements-for-finance-and-operations"></a>Sistēmas prasības programmai Finance and Operations
Field Service integrācija atbalsta šādas versijas.

- Dynamics 365 for Finance and Operations versija 8.1.2 (2018. gada decembris), kas ir izlaista 2018. gada decembrī, ar lietojumprogrammas būvējuma Nr. 8.1.195 un 22. platformas atjauninājumu (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Sistēmas prasības risinājumam Field Service
Lai lietotu Field Service integrācijas risinājumu, ir jābūt instalētiem tālāk minētajiem komponentiem.

- Field Service for Dynamics 365 (versija 8.2.0.286) vai jaunāka versija programmā Dynamics 365 9.1.x — izlaista 2018. gada novembrī
- Risinājums “No potenciālā klienta līdz skaidrai naudai” (P2C) programmai Dynamics 365, versija 1.15.0.1 vai jaunāka. Risinājumu var lejupielādēt no pakalpojuma [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Risinājums “Field Service integrācija, projekts un krājumi” programmai Dynamics 365, versija 2.0.0.0 vai jaunāka. Risinājumu var lejupielādēt no pakalpojuma [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).
