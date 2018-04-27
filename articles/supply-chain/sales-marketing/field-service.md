---
title: "Integrācija ar Microsoft Dynamics 365 for Field Service"
description: "Šajā tēmā ir sniegts apskats par integrāciju ar Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d32a4e376770fc73c79b94924d5ae062d201d84a
ms.openlocfilehash: a224962152e80293f6cf3425dea74d73a283e31a
ms.contentlocale: lv-lv
ms.lasthandoff: 04/12/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integrācija ar Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations ļauj sinhronizēt biznesa procesus risinājumos Finance and Operations un Microsoft Dynamics 365 for Field Service. Integrācijas scenārijus konfigurē, izmantojot paplašināmas datu integrētāja veidnes un Common Data Service (CDS), lai iespējotu biznesa procesu sinhronizāciju.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

Pirmā integrācijas fāze risinājumos Field Service un Finance and Operations attiecas uz to, lai darba pasūtījumus un līgumus risinājumā Field Service varētu iekļaut rēķinos risinājumā Finance and Operations. Atbalstītā plūsma sākas risinājumā Field Service, kur informācija no darba pasūtījumiem tiek sinhronizēta risinājumā Finance and Operations kā pārdošanas pasūtījumi. Risinājumā Finance and Operations pārdošanas pasūtījumi tiek iekļauti rēķinos, lai izveidotu rēķinu dokumentus. Turklāt informācija no Field Service līguma rēķiniem tiek sinhronizēta risinājumā Finance and Operations. Microsoft Dynamics 365 datu integrētājs sinhronizē datus, izmantojot pielāgojamus projektus. Standarta veidnes var izmantot, lai izveidotu pielāgotus integrācijas projektus, kuros var kartēt papildu standarta un pielāgotus laukus, kā arī entītijas, lai pielāgotu integrāciju un nodrošinātu īpašu prasību izpildi.

Pirmā integrācijas fāze risinājumos Field Service un Finance and Operations ļauj sinhronizēt šādus vienumus:

- [Risinājumā Finance and Operations ietvertās preces ar precēm risinājumā Field Service, kuras ietver informāciju par preces tipu](field-service-product.md)
- [Risinājumā Field Service ietvertie darba pasūtījumi ar pārdošanas pasūtījumiem risinājumā Finance and Operations](field-service-work-order.md)
- [Risinājumā Field Service ietvertie rēķini ar brīva teksta rēķiniem risinājumā Finance and Operations](field-service-invoice.md)

## <a name="system-requirements-for-finance-and-operations"></a>Sistēmas prasības programmai Finance and Operations
Field Service integrācija atbalsta šādas versijas.

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations, versija 8.0 (2018. gada aprīlis) vai jaunāka versija

- Dynamics 365 for Finance and Operations versija 8.0 (2018. gada aprīlis) tika izlaista 2018. gada aprīlī, un tās programmas būvējuma numurs ir 8.0.30.8020 ar 15. platformas atjauninājumu (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Sistēmas prasības risinājumam Field Service
Lai lietotu Field Service integrācijas risinājumu, ir jābūt instalētiem tālāk minētajiem komponentiem.

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 vai jaunāka versija

- Dynamics 365 for Field Service 1612 (9.0.1.733) (DB 9.0.1.733) tiešsaistes versija vai jaunāka versija.
- Risinājums “No potenciālā klienta līdz skaidrai naudai” (P2C) programmai Dynamics 365, versija 1.15.0.1 vai jaunāka. Risinājumu var lejupielādēt no pakalpojuma [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Field Service integrācijas risinājums programmai Dynamics 365, versija 1.0.0.0 vai jaunāka. Risinājumu var lejupielādēt no pakalpojuma AppSource. **(GAIDA IZLAIŠANU)**

