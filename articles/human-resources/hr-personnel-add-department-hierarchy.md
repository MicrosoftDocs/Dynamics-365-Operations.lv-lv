---
title: Nodaļu izveide un ietveršana nodaļu hierarhijā
description: Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu. Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību. Nodaļas var izmantot, lai ziņotu par funkcionālām jomām. Nodaļām var būt peļņas un zaudējumu atbildība.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 99ecdb936071c2c71dbfae1277d20aa6dc9ef0ca
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009844"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a><span data-ttu-id="84cb8-106">Nodaļu izveide un ietveršana nodaļu hierarhijā</span><span class="sxs-lookup"><span data-stu-id="84cb8-106">Create departments and include them in the department hierarchy</span></span>

<span data-ttu-id="84cb8-107">Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="84cb8-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="84cb8-108">Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību.</span><span class="sxs-lookup"><span data-stu-id="84cb8-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="84cb8-109">Nodaļas var izmantot, lai ziņotu par funkcionālām jomām.</span><span class="sxs-lookup"><span data-stu-id="84cb8-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="84cb8-110">Nodaļām var būt peļņas un zaudējumu atbildība.</span><span class="sxs-lookup"><span data-stu-id="84cb8-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="84cb8-111">Nodaļu var ietvert izmaksu centru grupā.</span><span class="sxs-lookup"><span data-stu-id="84cb8-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="84cb8-112">Pozīcijas var piešķirt nodaļām.</span><span class="sxs-lookup"><span data-stu-id="84cb8-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="84cb8-113">Lai izveidotu nodaļu, noklikšķiniet uz **Personāla vadība** &gt; **Nodaļas** &gt; **Nodaļa**.</span><span class="sxs-lookup"><span data-stu-id="84cb8-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="84cb8-114">Nākamajā tabulā ir aprakstīti pieejamie lauki.</span><span class="sxs-lookup"><span data-stu-id="84cb8-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="84cb8-115">Lauks</span><span class="sxs-lookup"><span data-stu-id="84cb8-115">Field</span></span>               | <span data-ttu-id="84cb8-116">Apraksts</span><span class="sxs-lookup"><span data-stu-id="84cb8-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84cb8-117">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="84cb8-117">Name</span></span>                | <span data-ttu-id="84cb8-118">Ievadiet struktūrvienības nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="84cb8-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="84cb8-119">Nodaļas numurs</span><span class="sxs-lookup"><span data-stu-id="84cb8-119">Department number</span></span>   | <span data-ttu-id="84cb8-120">Noklusējuma vērtība var tikt automātiski ģenerēta, ja numuru sērijas kods ir piešķirts atsaucei **Organizācijas numurs** lapā **Numuru sērijas**.</span><span class="sxs-lookup"><span data-stu-id="84cb8-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="84cb8-121">Meklēšanas nosaukums</span><span class="sxs-lookup"><span data-stu-id="84cb8-121">Search name</span></span>         | <span data-ttu-id="84cb8-122">Ievadiet nosaukumu vai akronīmu, ko var izmantot nodaļas meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="84cb8-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="84cb8-123">Atgādne</span><span class="sxs-lookup"><span data-stu-id="84cb8-123">Memo</span></span>                | <span data-ttu-id="84cb8-124">Ievadiet papildinformāciju šeit.</span><span class="sxs-lookup"><span data-stu-id="84cb8-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="84cb8-125">Hierarhijā</span><span class="sxs-lookup"><span data-stu-id="84cb8-125">In hierarchy</span></span>        | <span data-ttu-id="84cb8-126">Atzīmētā izvēles rūtiņa nozīmē, ka nodaļa ir iekļauta nodaļu hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="84cb8-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="84cb8-127">Informāciju par to, kā pievienot nodaļu nodaļu hierarhijai, skatiet tālāk šajā rakstā.</span><span class="sxs-lookup"><span data-stu-id="84cb8-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="84cb8-128">Universālās datu numerācijas sistēmas (DUNS) numurs</span><span class="sxs-lookup"><span data-stu-id="84cb8-128">DUNS number</span></span>         | <span data-ttu-id="84cb8-129">DUNS nozīmē universālo datu numerācijas sistēmu.</span><span class="sxs-lookup"><span data-stu-id="84cb8-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="84cb8-130">Tas ir deviņu ciparu numurs, ko piešķir Dun & Bradstreet.</span><span class="sxs-lookup"><span data-stu-id="84cb8-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="84cb8-131">Vadītājs</span><span class="sxs-lookup"><span data-stu-id="84cb8-131">Manager</span></span>             | <span data-ttu-id="84cb8-132">Ievadiet personu, kas pārvalda nodaļu.</span><span class="sxs-lookup"><span data-stu-id="84cb8-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="84cb8-133">Adreses</span><span class="sxs-lookup"><span data-stu-id="84cb8-133">Addresses</span></span>           | <span data-ttu-id="84cb8-134">Pievienojiet nodaļai adreses informāciju.</span><span class="sxs-lookup"><span data-stu-id="84cb8-134">Add the address information for the department.</span></span> <span data-ttu-id="84cb8-135">Piemēram, pievienojiet pasta adresi ēkai, kas atrodas struktūrvienība.</span><span class="sxs-lookup"><span data-stu-id="84cb8-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="84cb8-136">Kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="84cb8-136">Contact information</span></span> | <span data-ttu-id="84cb8-137">Pievienojiet nodaļai kontaktinformāciju.</span><span class="sxs-lookup"><span data-stu-id="84cb8-137">Add contact information for the department.</span></span> <span data-ttu-id="84cb8-138">Piemēram, pievienojiet struktūrvienības informācijas nodaļas tālruņa numuru.</span><span class="sxs-lookup"><span data-stu-id="84cb8-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="84cb8-139">Lai pievienotu nodaļu nodaļu hierarhijai, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="84cb8-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="84cb8-140">Noklikšķiniet uz **Personāla vadība** &gt; **Nodaļas** &gt; **Nodaļu hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="84cb8-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="84cb8-141">Noklikšķiniet uz **Rediģēt** un pēc tam atlasiet organizāciju, kurā jābūt nodaļai.</span><span class="sxs-lookup"><span data-stu-id="84cb8-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="84cb8-142">Noklikšķiniet uz **Iespraust** un sarakstā atlasiet **Nodaļa**.</span><span class="sxs-lookup"><span data-stu-id="84cb8-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="84cb8-143">Nodaļu sarakstā, kas parādās, atlasiet nodaļu, ko pievienot hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="84cb8-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="84cb8-144">Saglabājiet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="84cb8-144">Save your changes.</span></span> <span data-ttu-id="84cb8-145">Jūs saņemsiet ziņojumu, ka ir izveidota hierarhijas melnraksta versija.</span><span class="sxs-lookup"><span data-stu-id="84cb8-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="84cb8-146">Kad esat pabeidzis, hierarhijas veidotājā noklikšķiniet uz **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="84cb8-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="84cb8-147">Varat ievadīt spēkā stāšanās datumu, kas norāda, kad šī hierarhija ir jāpublicē.</span><span class="sxs-lookup"><span data-stu-id="84cb8-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="84cb8-148">Piemēram, lai pievienotu jaunu nodaļu nākamā kalendārā gada sākumā, iestatiet spēkā stāšanās datumu uz jaunā kalendāra gada 1. janvāri.</span><span class="sxs-lookup"><span data-stu-id="84cb8-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="84cb8-149">Hierarhijas izmaiņas stāsies spēkā šajā datumā.</span><span class="sxs-lookup"><span data-stu-id="84cb8-149">The changes to the hierarchy will take effect on that date.</span></span>

## <a name="steps-for-creating-a-department"></a><span data-ttu-id="84cb8-150">Norādījumi par nodaļas izveidi</span><span class="sxs-lookup"><span data-stu-id="84cb8-150">Steps for creating a department</span></span>
<span data-ttu-id="84cb8-151">Sīku jaunas nodaļas izveides procedūras aprakstu skatiet rakstā [Jaunu nodaļu definēšana](../fin-and-ops/hr/tasks/define-new-departments.md).</span><span class="sxs-lookup"><span data-stu-id="84cb8-151">Refer to the [Define new departments](../fin-and-ops/hr/tasks/define-new-departments.md) article for the step-by-step procedure for creating a new department.</span></span> 