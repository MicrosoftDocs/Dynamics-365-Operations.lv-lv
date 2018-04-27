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


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="8a856-103">Integrācija ar Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="8a856-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8a856-104">Microsoft Dynamics 365 for Finance and Operations ļauj sinhronizēt biznesa procesus risinājumos Finance and Operations un Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="8a856-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="8a856-105">Integrācijas scenārijus konfigurē, izmantojot paplašināmas datu integrētāja veidnes un Common Data Service (CDS), lai iespējotu biznesa procesu sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="8a856-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="8a856-106">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="8a856-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="8a856-107">Pirmā integrācijas fāze risinājumos Field Service un Finance and Operations attiecas uz to, lai darba pasūtījumus un līgumus risinājumā Field Service varētu iekļaut rēķinos risinājumā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a856-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="8a856-108">Atbalstītā plūsma sākas risinājumā Field Service, kur informācija no darba pasūtījumiem tiek sinhronizēta risinājumā Finance and Operations kā pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="8a856-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="8a856-109">Risinājumā Finance and Operations pārdošanas pasūtījumi tiek iekļauti rēķinos, lai izveidotu rēķinu dokumentus.</span><span class="sxs-lookup"><span data-stu-id="8a856-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="8a856-110">Turklāt informācija no Field Service līguma rēķiniem tiek sinhronizēta risinājumā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a856-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="8a856-111">Microsoft Dynamics 365 datu integrētājs sinhronizē datus, izmantojot pielāgojamus projektus.</span><span class="sxs-lookup"><span data-stu-id="8a856-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="8a856-112">Standarta veidnes var izmantot, lai izveidotu pielāgotus integrācijas projektus, kuros var kartēt papildu standarta un pielāgotus laukus, kā arī entītijas, lai pielāgotu integrāciju un nodrošinātu īpašu prasību izpildi.</span><span class="sxs-lookup"><span data-stu-id="8a856-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="8a856-113">Pirmā integrācijas fāze risinājumos Field Service un Finance and Operations ļauj sinhronizēt šādus vienumus:</span><span class="sxs-lookup"><span data-stu-id="8a856-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="8a856-114">Risinājumā Finance and Operations ietvertās preces ar precēm risinājumā Field Service, kuras ietver informāciju par preces tipu</span><span class="sxs-lookup"><span data-stu-id="8a856-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="8a856-115">Risinājumā Field Service ietvertie darba pasūtījumi ar pārdošanas pasūtījumiem risinājumā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8a856-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="8a856-116">Risinājumā Field Service ietvertie rēķini ar brīva teksta rēķiniem risinājumā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8a856-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="8a856-117">Sistēmas prasības programmai Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8a856-117">System requirements for Finance and Operations</span></span>
<span data-ttu-id="8a856-118">Field Service integrācija atbalsta šādas versijas.</span><span class="sxs-lookup"><span data-stu-id="8a856-118">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="8a856-119">Dynamics 365 for Finance and Operations, versija 8.0 (2018. gada aprīlis) vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="8a856-119">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="8a856-120">Dynamics 365 for Finance and Operations versija 8.0 (2018. gada aprīlis) tika izlaista 2018. gada aprīlī, un tās programmas būvējuma numurs ir 8.0.30.8020 ar 15. platformas atjauninājumu (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="8a856-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="8a856-121">Sistēmas prasības risinājumam Field Service</span><span class="sxs-lookup"><span data-stu-id="8a856-121">System requirements for Field Service</span></span>
<span data-ttu-id="8a856-122">Lai lietotu Field Service integrācijas risinājumu, ir jābūt instalētiem tālāk minētajiem komponentiem.</span><span class="sxs-lookup"><span data-stu-id="8a856-122">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="8a856-123">Microsoft Dynamics 365 for Field Service 9.0 vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="8a856-123">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="8a856-124">Dynamics 365 for Field Service 1612 (9.0.1.733) (DB 9.0.1.733) tiešsaistes versija vai jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="8a856-124">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="8a856-125">Risinājums “No potenciālā klienta līdz skaidrai naudai” (P2C) programmai Dynamics 365, versija 1.15.0.1 vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="8a856-125">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="8a856-126">Risinājumu var lejupielādēt no pakalpojuma [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="8a856-126">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="8a856-127">Field Service integrācijas risinājums programmai Dynamics 365, versija 1.0.0.0 vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="8a856-127">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="8a856-128">Risinājumu var lejupielādēt no pakalpojuma AppSource.</span><span class="sxs-lookup"><span data-stu-id="8a856-128">The solution is available for download from AppSource.</span></span> <span data-ttu-id="8a856-129">**(GAIDA IZLAIŠANU)**</span><span class="sxs-lookup"><span data-stu-id="8a856-129">**(PENDING RELEASE)**</span></span>

