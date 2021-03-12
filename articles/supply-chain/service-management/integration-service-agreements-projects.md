---
title: Integrācija pakalpojumu līgumiem un projektiem
description: Kad jūs strādājat ar pakalpojumu līgumiem un pakalpojumu līgumu rindām, jūs lietojat datus, kas ir iestatīti sadaļas Projektu pārvaldība un uzskaite apgabalos.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eab6125dbca1568c06818c8528d1bee4ce6bf53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974464"
---
# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="5cdb4-103">Integrācija pakalpojumu līgumiem un projektiem</span><span class="sxs-lookup"><span data-stu-id="5cdb4-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5cdb4-104">Kad jūs strādājat ar pakalpojumu līgumiem un pakalpojumu līgumu rindām, jūs lietojat datus, kas ir iestatīti sadaļas **Projektu pārvaldība un uzskaite** apgabalos.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="5cdb4-105">Projekta cenas</span><span class="sxs-lookup"><span data-stu-id="5cdb4-105">Project prices</span></span>

<span data-ttu-id="5cdb4-106">Pakalpojuma līguma darbības izmaksas un pārdošanas cena izriet no izmaksu cenu iestatījumiem, kas attiecas uz pakalpojuma līgumam pievienoto projektu.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="5cdb4-107">Izmaksu un pārdošanas cenas var tikt iestatītas projektam, darbiniekam un kategorijai.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="5cdb4-108">Projekta pārbaude</span><span class="sxs-lookup"><span data-stu-id="5cdb4-108">Project validation</span></span>

<span data-ttu-id="5cdb4-109">Pakalpojuma līguma rindā atlasei pieejamie projekti, darbinieki un kategorijas var tikt ierobežoti ar apstiprināšanas iestatījumu palīdzību sadaļā **Projektu pārvaldība un uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="5cdb4-110">Izmantojot apstiprināšanas iestatījumus, varat kombinēt darbiniekus, projektus un kategorijas piekļuves kontrolei.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="5cdb4-111">Projekta rindas statuss</span><span class="sxs-lookup"><span data-stu-id="5cdb4-111">Project line properties</span></span>

<span data-ttu-id="5cdb4-112">Pakalpojuma līguma rindai rindas statuss tiek ievadīts automātiski.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="5cdb4-113">Rindas rekvizīti tiek izveidoti veidlapā **Rindas rekvizīti**, sadaļā **Projektu pārvaldība un uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="5cdb4-114">Rindas rekvizīts, kas ir ievadīts pakalpojumu līgumā, ir pievienots pakalpojumu līgumam atlasītajam projektam, un to manto pakalpojumu līguma rinda.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="5cdb4-115">Noklusētie korespondējošie konti</span><span class="sxs-lookup"><span data-stu-id="5cdb4-115">Default offset accounts</span></span>

<span data-ttu-id="5cdb4-116">Ja jūs ievadīsit izmaksu darbību, attiecīgajai darbībai automātiski tiek atlasīts noklusētais korespondējošais konts.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="5cdb4-117">Noklusētais izdevumu konts tiek iestatīts projektam, kas piesaistīts pašreizējam pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="5cdb4-118">Projektu kategorijas</span><span class="sxs-lookup"><span data-stu-id="5cdb4-118">Project categories</span></span>

<span data-ttu-id="5cdb4-119">Pakalpojumu līgumu rindām pieejamās kategorijas ir iestatītas veidlapā **Projektu kategorijas**, kas atrodas sadaļā **Projektu pārvaldība un uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="5cdb4-120">Kategorijas, kurām ir atzīmēta izvēles rūtiņa <STRONG>Aktīvs žurnālos</STRONG> veidlapas <STRONG>Projektu kategorijas</STRONG> cilnē <STRONG>Projekts</STRONG>, ir pieejamas atlasei.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="5cdb4-121">Tomēr, ja ir atlasīta izvēles rūtiņa <STRONG>Neaktīvās kategorijas</STRONG> veidlapas <STRONG>Projektu vadības un uzskaites parametri</STRONG> cilnē <STRONG>Žurnāli</STRONG>, visas kategorijas ir pieejamas atlasei.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="5cdb4-122">Projektu parametri</span><span class="sxs-lookup"><span data-stu-id="5cdb4-122">Project parameters</span></span>

<span data-ttu-id="5cdb4-123">Ja ir atlasīts lauks **Nodarbinātie, ar kuriem ir pārtrauktas darba attiecības** veidlapas **Projektu vadības un uzskaites parametri** cilnē **Žurnāli**, jūs varat atlasīt neaktīvos darbiniekus papildus aktīvajiem darbiniekiem veidlapās **Pakalpojumu līgumi** un **Pakalpojumu pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="5cdb4-124">Jūs varat arī iespējot laukus **Sākuma laiks** un **Beigu laiks** veidlapas **Pakalpojumu pasūtījumi** cilnē **Projekts**, lai ievadītu sākuma un beigu laikus pakalpojumu pasūtījumu rindās.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="5cdb4-125">Sākuma un beigu laika iespējas iespējošana pakalpojumu pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="5cdb4-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="5cdb4-126">Noklikšķiniet uz **Projektu vadība un uzskaite** \> **Iestatīšana** \> **Projektu vadības un uzskaites parametri**.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="5cdb4-127">Noklikšķiniet uz cilnes **Žurnāli** un pēc tam atzīmējiet izvēles rūtiņu **Parādīt sākuma/beigu laikus**.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="5cdb4-128">Noklikšķiniet uz **Projektu pārvaldība un uzskaite** \> **Iestatījumi** \> **Žurnāli** \> **Žurnālu nosaukumi**.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="5cdb4-129">Atlasiet pakalpojuma pasūtījumam pievienotā žurnāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="5cdb4-130">Noklikšķiniet uz cilnes **Vispārīgi** un pēc tam atzīmējiet izvēles rūtiņu **Parādīt sākuma/beigu laikus**.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5cdb4-131">Atlasiet žurnāla nosaukumu pakalpojumu pasūtījumam laukā <STRONG>Stunda</STRONG> veidlapas <STRONG>Pakalpojumu pārvaldības parametri</STRONG> cilnē <STRONG>Žurnāli</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5cdb4-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>





