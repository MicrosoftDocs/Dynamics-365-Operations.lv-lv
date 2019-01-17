---
title: "Integrācija ar Microsoft Dynamics 365 for Field Service"
description: "Šajā tēmā ir sniegts apskats par integrāciju ar Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 673ab2a101cee1a3dbbb1249f582d959cecc7f7f
ms.contentlocale: lv-lv
ms.lasthandoff: 12/23/2018

---

# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integrācija ar Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations ļauj sinhronizēt biznesa procesus risinājumos Finance and Operations un Microsoft Dynamics 365 for Field Service. Integrācijas scenārijus konfigurē, izmantojot paplašināmas datu integrētāja veidnes un Common Data Service (CDS), lai iespējotu biznesa procesu sinhronizāciju.
Standarta veidnes var izmantot, lai izveidotu pielāgotus integrācijas projektus, kuros var kartēt papildu standarta un pielāgotus laukus, kā arī entītijas, lai pielāgotu integrāciju un nodrošinātu īpašu biznesa prasību izpildi. 

Papildus jau esošajai funkcionalitātei “No potenciālā klienta līdz skaidrai naudai” veidojas Field Service integrācija.

![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/field-service-integration.png)

Pirmā integrācijas fāze risinājumos Field Service un Finance and Operations attiecas uz to, lai darba pasūtījumus un līgumus risinājumā Field Service varētu iekļaut rēķinos risinājumā Finance and Operations. Atbalstītā plūsma sākas risinājumā Field Service, kur informācija no darba pasūtījumiem tiek sinhronizēta risinājumā Finance and Operations kā pārdošanas pasūtījumi. Risinājumā Finance and Operations pārdošanas pasūtījumi tiek iekļauti rēķinos, lai izveidotu rēķinu dokumentus. Turklāt informācija no Field Service līguma rēķiniem tiek sinhronizēta risinājumā Finance and Operations. Microsoft Dynamics 365 datu integrētājs sinhronizē datus, izmantojot pielāgojamus projektus. Standarta veidnes var izmantot, lai izveidotu pielāgotus integrācijas projektus, kuros var kartēt papildu standarta un pielāgotus laukus, kā arī entītijas, lai pielāgotu integrāciju un nodrošinātu īpašu prasību izpildi.

Pirmā integrācijas fāze risinājumos Field Service un Finance and Operations ļauj sinhronizēt šādus vienumus:

- [Risinājumā Finance and Operations ietvertās preces ar precēm risinājumā Field Service, kuras ietver informāciju par preces tipu](field-service-product.md)
- [Risinājumā Field Service ietvertie darba pasūtījumi ar pārdošanas pasūtījumiem risinājumā Finance and Operations](field-service-work-order.md)
- [Risinājumā Field Service ietvertie rēķini ar brīva teksta rēķiniem risinājumā Finance and Operations](field-service-invoice.md)

Lai redzētu piemēru tam, kā var sinhronizēt darba pasūtījumu starp programmu Field Service un programmu Finance and Operations, noskatieties īsu YouTube video [Darba pasūtījuma sinhronizēšana ar Microsoft Dynamics 365 integrāciju](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="system-requirements-for-finance-and-operations"></a>Sistēmas prasības programmai Finance and Operations
Field Service integrācija atbalsta šādas versijas.

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations, versija 8.0 (2018. gada aprīlis) vai jaunāka versija

- Dynamics 365 for Finance and Operations versija 8.0 (2018. gada aprīlis) tika izlaista 2018. gada aprīlī, un tās programmas būvējuma numurs ir 8.0.30.8020 ar 15. platformas atjauninājumu (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Sistēmas prasības risinājumam Field Service
Lai lietotu Field Service integrācijas risinājumu, ir jābūt instalētiem tālāk minētajiem komponentiem.

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 vai jaunāka versija

- Dynamics 365 for Field Service 1612 (9.0.1.733) (DB 9.0.1.733) tiešsaistes versija vai jaunāka versija.
- Risinājums “No potenciālā klienta līdz skaidrai naudai” (P2C) programmai Dynamics 365, versija 1.15.0.1 vai jaunāka. Risinājumu var lejupielādēt no pakalpojuma [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Field Service integrācijas risinājums programmai Dynamics 365, versija 1.0.0.0 vai jaunāka. Risinājumu var lejupielādēt no pakalpojuma [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration).

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Integrācija ar Microsoft Dynamics 365 for Field Service, iekļaujot informāciju par krājumiem un projektiem

Papildu funkcionalitātes pievienošana šajā otrajā posmā bija koncentrēta uz to, lai nozares speciālistiem sniegtu ieskatu par Finance and Operations krājumu informāciju, kas ļautu atjaunināt krājumu līmeņus un veikt izejmateriālu pārsūtīšanu. Turklāt uzņēmumi, kas nodarbojas ar pārdoto preču uzstādīšanu vai apkalpošanu, gūs tādas priekšrocības kā labāku pārvaldību un redzamību, kā arī pilnīgu pārdošanas un pakalpojumu procesu ar integrāciju no projektiem.

### <a name="functionality-includes-integration-of"></a>Funkcionalitāte ietver integrāciju ar šādiem elementiem:
- Noliktavas informācija
- Rīcībā esošo krājumu informācija
- Krājumu pārsūtīšana
- Krājumu pārrēķini
- Ar Dynamics 365 for Field Service darba pasūtījumiem saistītie Dynamics 365 for Finance and Operations projekti
- Dynamics 365 for Field Service darba pasūtījumi ar saiti uz Dynamics 365 for Finance and Operations projektiem: jāpiemēro attiecīgā projekta numurs Dynamics 365 for Finance and Operations pārdošanas pasūtījumam, lai atļautu izrakstīt rēķinu par projektu. 

![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Otrais integrācijas posms risinājumos Field Service un Finance and Operations ļauj sinhronizēt šādas veidnes:
- Noliktavas (no risinājuma Finance and Operations risinājumā Field Service) — noliktavu informācijas sinhronizācija no risinājuma Finance and Operations risinājumā Field Service [Paplašinātais vaicājums] 
- Preču krājumi (no risinājuma Finance and Operations risinājumā Field Service) — krājumu līmeņa informācijas sinhronizācija no risinājuma Finance and Operations risinājumā Field Service [Paplašinātais vaicājums] 
- Krājumu korekcija (no risinājuma Field Service risinājumā Finance and Operations) — krājumu korekcijas informācijas sinhronizācija no risinājuma Field Service risinājumā Finance and Operations [Paplašinātais vaicājums] 
- Krājumu pārsūtīšana (no risinājuma Field Service risinājumā Finance and Operations) — krājumu pārsūtīšanas informācijas sinhronizācija no risinājuma Field Service risinājumā Finance and Operations [Paplašinātais vaicājums] 
- Projekti (no risinājuma Finance and Operations risinājumā Field Service) — projektu informācijas sinhronizācija no risinājuma Finance and Operations risinājumā Field Service 
- Darba pasūtījumi ar projektu (no risinājuma Field Service risinājumā Finance and Operations) — darba pasūtījumu informācijas no risinājuma Field Service sinhronizācija ar pārdošanas pasūtījumu informāciju risinājumā Finance and Operations ar atbalstu projektam [Paplašinātais vaicājums] 
- Field Service preces ar krājumu uzskaites vienību (no risinājuma Finance and Operations uz pārdošanu) — risinājuma Finance and Operations pārdodamo izlaisto preču sinhronizācija ar risinājuma Field Service pārdošanas precēm, ieskaitot krājuma uzskaites vienības 

## <a name="system-requirements-for-finance-and-operations"></a>Sistēmas prasības programmai Finance and Operations
Field Service integrācija atbalsta šādas versijas.

- Dynamics 365 for Finance and Operations versija 8.1.2 (2019. gada decembris) tika izlaista 2019. gada decembrī, un tās programmas būvējuma numurs ir 8.1.195 ar 22. platformas atjauninājumu (7.0.5095). 

## <a name="system-requirements-for-field-service"></a>Sistēmas prasības risinājumam Field Service
Lai lietotu Field Service integrācijas risinājumu, ir jābūt instalētiem tālāk minētajiem komponentiem.

- Field Service for Dynamics 365 (versija 8.2.0.286) vai jaunāka Dynamics 365 9.1.x versija — izlaista 2018. gada novembrī
- Risinājums “No potenciālā klienta līdz skaidrai naudai” (P2C) programmai Dynamics 365, versija 1.15.0.1 vai jaunāka. Risinājumu var lejupielādēt no pakalpojuma [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Risinājums “Field Service integrācija, projekts un krājumi” programmai Dynamics 365, versija 2.0.0.0 vai jaunāka. Risinājumu var lejupielādēt no pakalpojuma [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).

