---
title: Talent paplašināšana ar Power Apps un Power Automate
description: Šajā rakstā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Human Resources, kuros tiek izmantota programmatūra Microsoft Power Apps un Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1c5bc0776174960af6cb8a62f00e3fd7d56b1676
ms.sourcegitcommit: 58d7133ae9909fa205730e3cf4c7fd5a1d5d0b75
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/10/2020
ms.locfileid: "3793615"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="6c38b-103">Paplašināšana ar Power Apps un Power Automate</span><span class="sxs-lookup"><span data-stu-id="6c38b-103">Extend with Power Apps and Power Automate</span></span>

<span data-ttu-id="6c38b-104">Šajā rakstā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Human Resources, kuros tiek izmantota programmatūra Microsoft Power Apps un Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="6c38b-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="6c38b-105">Varat importēt ar katru piemēru saistīto risinājumu pakotni savā Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="6c38b-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="6c38b-106">Pēc tam varat izmantot pakotnes kā vadlīnijas vai kā sākumpunktu, lai īstenotu scenārijus, kas attiecas uz jūsu organizāciju.</span><span class="sxs-lookup"><span data-stu-id="6c38b-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c38b-107">Ja vēlaties izmantot šajā tēmā aprakstītās veidnes un programmas nemainītā veidā, pārbaudiet tās un pārliecinieties, ka tās aptver visus scenārijus, kas raksturīgi jūsu ieviešanai.</span><span class="sxs-lookup"><span data-stu-id="6c38b-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6c38b-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="6c38b-108">Prerequisites</span></span>

- <span data-ttu-id="6c38b-109">Lai importētu pakotnes, lietotājiem ir jābūt atļaujai **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="6c38b-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="6c38b-110">Lai eksportētu vai importētu programmas, lietotājiem jābūt Power Apps 2. plāna licencei vai Power Apps 2. plāna izmēģinājuma licencei.</span><span class="sxs-lookup"><span data-stu-id="6c38b-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-office-365-power-automate"></a><span data-ttu-id="6c38b-111">Integrācija ar Office 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="6c38b-111">Integration with Office 365, Power Automate</span></span>

<span data-ttu-id="6c38b-112">Programmu **Integrācija ar Office 365** var izmantot, lai iegūtu grupas informāciju lietotājiem, kuri ir pierakstījušies, no programmas Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="6c38b-112">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="6c38b-113">Tajā ir atsauces uz Human Resources darbiniekiem, lai izvilktu darbinieka identifikācijas veidus.</span><span class="sxs-lookup"><span data-stu-id="6c38b-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="6c38b-114">Vadītāji var pārbaudīt darbinieku ID veidu beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="6c38b-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="6c38b-115">Ja darbinieka ID veida termiņš drīz beigsies, viņi var arī nosūtīt atgādinājumu pa e-pastu.</span><span class="sxs-lookup"><span data-stu-id="6c38b-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="6c38b-116">Power Automate integrējas Power Apps, lai nosūtītu šo atgādinājumu.</span><span class="sxs-lookup"><span data-stu-id="6c38b-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="6c38b-117">Apstiprinājums tiks nosūtīts atpakaļ Power Apps no Power Automate, kad atgādinājums ir nosūtīts.</span><span class="sxs-lookup"><span data-stu-id="6c38b-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="6c38b-118">Identifikācijas veidi ietver autovadītāja apliecību, pasi un citus pieņemamus ID veidus.</span><span class="sxs-lookup"><span data-stu-id="6c38b-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="6c38b-119">Šo programmu varat paplašināt citos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="6c38b-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="6c38b-120">Piemēram, to var izmantot, lai rādītu darba grupas atvaļinājumu informāciju, kalendāra notikumus un ar darba grupu saistītus notikumus.</span><span class="sxs-lookup"><span data-stu-id="6c38b-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="6c38b-121">Lai lejupielādētu programmu **Integrācija ar Office 365, Power Automate**, dodieties uz [Integrācija ar Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) Microsoft Lejupielāžu centrā.</span><span class="sxs-lookup"><span data-stu-id="6c38b-121">To download the **Integration with Office 365, Power Automate** app, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="6c38b-122">Power Automate – SQL savienojums un izpilde</span><span class="sxs-lookup"><span data-stu-id="6c38b-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="6c38b-123">Veidne **Power Automate – SQL savienojums un izpilde** izveido savienojumu ar Microsoft SQL Server un nodrošina SQL vaicājumu izpildi.</span><span class="sxs-lookup"><span data-stu-id="6c38b-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="6c38b-124">Lai arī šī veidne lasa un atjaunina SQL tabulas, varat to izvērst un izmantot citos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="6c38b-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="6c38b-125">Piemēram, to var izmantot, lai aizpildītu sagatavošanas tabulu pakalpojumā Common Data Service ar ierakstiem no SQL Server un periodiski sinhronizētu sagatavošanas tabulu, izmantojot inkrementālu sadali no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6c38b-125">For example, you can use it to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="6c38b-126">Detalizēts vaicājums ir integrēts ar plūsmu, lai iespējotu datu transformāciju un inkrementālo sadali.</span><span class="sxs-lookup"><span data-stu-id="6c38b-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="6c38b-127">Lai lejupielādētu veidni **Power Automate – SQL savienojums un izpilde**, ejiet uz [Power Automate – SQL savienojums un izpilde](https://go.microsoft.com/fwlink/?linkid=2081789) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="6c38b-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c38b-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6c38b-128">Additional resources</span></span>

[<span data-ttu-id="6c38b-129">Risinājums Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="6c38b-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>