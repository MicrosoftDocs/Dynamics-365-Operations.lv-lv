---
title: Talent paplašināšana ar Power Apps un Power Automate
description: Šajā tēmā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Human Resources, kuros tiek izmantota programmatūra Microsoft Power Apps un Microsoft Power Automate.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b5032c0996ef0dfb80a129deb32b4526794ca228
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892157"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="c8754-103">Paplašināšana ar Power Apps un Power Automate</span><span class="sxs-lookup"><span data-stu-id="c8754-103">Extend with Power Apps and Power Automate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c8754-104">Šajā tēmā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Human Resources, kuros tiek izmantota programmatūra Microsoft Power Apps un Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="c8754-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="c8754-105">Varat importēt ar katru piemēru saistīto risinājumu pakotni savā Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="c8754-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="c8754-106">Pēc tam varat izmantot pakotnes kā vadlīnijas vai kā sākumpunktu, lai īstenotu scenārijus, kas attiecas uz jūsu organizāciju.</span><span class="sxs-lookup"><span data-stu-id="c8754-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8754-107">Ja vēlaties izmantot šajā tēmā aprakstītās veidnes un programmas nemainītā veidā, pārbaudiet tās un pārliecinieties, ka tās aptver visus scenārijus, kas raksturīgi jūsu ieviešanai.</span><span class="sxs-lookup"><span data-stu-id="c8754-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c8754-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="c8754-108">Prerequisites</span></span>

- <span data-ttu-id="c8754-109">Lai importētu pakotnes, lietotājiem ir jābūt atļaujai **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="c8754-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="c8754-110">Lai eksportētu vai importētu programmas, lietotājiem jābūt Power Apps 2. plāna licencei vai Power Apps 2. plāna izmēģinājuma licencei.</span><span class="sxs-lookup"><span data-stu-id="c8754-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="c8754-111">Integrācija ar Microsoft 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="c8754-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="c8754-112">Programmu **Integrācija ar Microsoft 365** var izmantot, lai iegūtu grupas informāciju lietotājiem, kuri ir pierakstījušies, no programmas Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c8754-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="c8754-113">Tajā ir atsauces uz Human Resources darbiniekiem, lai izvilktu darbinieka identifikācijas veidus.</span><span class="sxs-lookup"><span data-stu-id="c8754-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="c8754-114">Vadītāji var pārbaudīt darbinieku ID veidu beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="c8754-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="c8754-115">Ja darbinieka ID veida termiņš drīz beigsies, viņi var arī nosūtīt atgādinājumu pa e-pastu.</span><span class="sxs-lookup"><span data-stu-id="c8754-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="c8754-116">Power Automate integrējas Power Apps, lai nosūtītu šo atgādinājumu.</span><span class="sxs-lookup"><span data-stu-id="c8754-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="c8754-117">Apstiprinājums tiks nosūtīts atpakaļ Power Apps no Power Automate, kad atgādinājums ir nosūtīts.</span><span class="sxs-lookup"><span data-stu-id="c8754-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="c8754-118">Identifikācijas veidi ietver autovadītāja apliecību, pasi un citus pieņemamus ID veidus.</span><span class="sxs-lookup"><span data-stu-id="c8754-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="c8754-119">Šo programmu varat paplašināt citos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="c8754-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="c8754-120">Piemēram, to var izmantot, lai rādītu darba grupas atvaļinājumu informāciju, kalendāra notikumus un ar darba grupu saistītus notikumus.</span><span class="sxs-lookup"><span data-stu-id="c8754-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="c8754-121">Lai lejupielādētu programmu **Integrācija ar Microsoft 365, Power Automate**, dodieties uz [Integrācija ar Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) Microsoft lejupielāžu centrā.</span><span class="sxs-lookup"><span data-stu-id="c8754-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="c8754-122">Power Automate – SQL savienojums un izpilde</span><span class="sxs-lookup"><span data-stu-id="c8754-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="c8754-123">Veidne **Power Automate – SQL savienojums un izpilde** izveido savienojumu ar Microsoft SQL Server un nodrošina SQL vaicājumu izpildi.</span><span class="sxs-lookup"><span data-stu-id="c8754-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="c8754-124">Lai arī šī veidne lasa un atjaunina SQL tabulas, varat to izvērst un izmantot citos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="c8754-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="c8754-125">Piemēram, to var izmantot, lai aizpildītu sagatavošanas tabulu pakalpojumā Dataverse ar ierakstiem no SQL Server un periodiski sinhronizētu sagatavošanas tabulu, izmantojot inkrementālu sadali no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c8754-125">For example, you can use it to fill a staging table in Dataverse with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="c8754-126">Detalizēts vaicājums ir integrēts ar plūsmu, lai iespējotu datu transformāciju un inkrementālo sadali.</span><span class="sxs-lookup"><span data-stu-id="c8754-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="c8754-127">Lai lejupielādētu veidni **Power Automate – SQL savienojums un izpilde**, ejiet uz [Power Automate – SQL savienojums un izpilde](https://go.microsoft.com/fwlink/?linkid=2081789) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="c8754-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8754-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c8754-128">Additional resources</span></span>

[<span data-ttu-id="c8754-129">Risinājums Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="c8754-129">The Microsoft Power Platform</span></span>](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]