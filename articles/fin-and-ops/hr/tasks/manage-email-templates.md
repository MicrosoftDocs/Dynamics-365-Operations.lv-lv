---
title: E-pasta veidņu pārvaldība
description: Varat pārsūtīt informāciju no uzņēmuma datu bāzes uz jauna dokumenta grāmatzīmēm un izmantot to veidnēs, kuras izmantojat efektīvai saziņai ar kandidātiem.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4667d0506c5ae6bea87b982c7feebab8963797a6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1508037"
---
# <a name="manage-email-templates"></a><span data-ttu-id="cf031-103">E-pasta veidņu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="cf031-103">Manage email templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf031-104">Varat pārsūtīt informāciju no uzņēmuma datu bāzes uz jauna dokumenta grāmatzīmēm un izmantot to veidnēs, kuras izmantojat efektīvai saziņai ar kandidātiem.</span><span class="sxs-lookup"><span data-stu-id="cf031-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="cf031-105">Lai to paveiktu, izveidojiet veidni, kas satur standarta tekstu un dažas grāmatzīmes, kur paredzēts ievietot sistēmas datus.</span><span class="sxs-lookup"><span data-stu-id="cf031-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="cf031-106">Piemēram, varat ievietot kandidāta adresi un kontaktinformāciju Microsoft Word dokumentā, ko varat izmantot, kad sazināties ar šo kandidātu.</span><span class="sxs-lookup"><span data-stu-id="cf031-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="cf031-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="cf031-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="cf031-108">Izvēlieties grāmatzīmes, kuras nepieciešams izmantot e-pasta veidnēs</span><span class="sxs-lookup"><span data-stu-id="cf031-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="cf031-109">Dodieties uz sadaļu Pieteikumu grāmatzīmes.</span><span class="sxs-lookup"><span data-stu-id="cf031-109">Go to Application bookmarks.</span></span>
2. <span data-ttu-id="cf031-110">Sarakstā atrodiet un atlasiet vajadzīgo saziņas darbību.</span><span class="sxs-lookup"><span data-stu-id="cf031-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="cf031-111">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="cf031-111">Click Edit.</span></span>
4. <span data-ttu-id="cf031-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cf031-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cf031-113">Atlasiet laukus, kurus vēlaties spēt izmantot atlasītās saziņas darbības e-pasta veidnē, un pārvietojiet tos uz grāmatzīmju laukiem.</span><span class="sxs-lookup"><span data-stu-id="cf031-113">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="cf031-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cf031-114">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="cf031-115">E-pasta veidnes izveidošana</span><span class="sxs-lookup"><span data-stu-id="cf031-115">Create an email template</span></span>
1. <span data-ttu-id="cf031-116">Dodieties uz Personāla vadība > Personāla atlase > Komunikācija > Pieteikumu e-pasta veidnes.</span><span class="sxs-lookup"><span data-stu-id="cf031-116">Go to Human resources > Recruitment > Communication > Application e-mail templates.</span></span>
2. <span data-ttu-id="cf031-117">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cf031-117">Click New.</span></span>
3. <span data-ttu-id="cf031-118">Laukā Saziņas darbība atlasiet Intervija.</span><span class="sxs-lookup"><span data-stu-id="cf031-118">In the Correspondence action field, select 'Interview'.</span></span>
    * <span data-ttu-id="cf031-119">Atlasiet saziņas darbību, kas satur grāmatzīmes, kuras jāizmanto šāda veida e-pasta saziņai.</span><span class="sxs-lookup"><span data-stu-id="cf031-119">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="cf031-120">Ierakstiet vērtību laukā E-pasta veidne.</span><span class="sxs-lookup"><span data-stu-id="cf031-120">In the E-mail template field, type a value.</span></span>
5. <span data-ttu-id="cf031-121">Ierakstiet vērtību laukā Tēma.</span><span class="sxs-lookup"><span data-stu-id="cf031-121">In the Subject field, type a value.</span></span>
6. <span data-ttu-id="cf031-122">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="cf031-122">In the Text field, type a value.</span></span>
7. <span data-ttu-id="cf031-123">Sarakstā atrodiet un atlasiet vajadzīgo grāmatzīmes lauku.</span><span class="sxs-lookup"><span data-stu-id="cf031-123">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="cf031-124">Turpiniet rakstīt e-pasta ziņojumu, ievietojot grāmatzīmju laukus vietās, kur tie nepieciešami.</span><span class="sxs-lookup"><span data-stu-id="cf031-124">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
    * <span data-ttu-id="cf031-125">Turpiniet rakstīt e-pasta ziņojumu, ievietojot grāmatzīmju laukus vietās, kur tie nepieciešami.</span><span class="sxs-lookup"><span data-stu-id="cf031-125">Continue typing your email message inserting the bookmark fields where desired.</span></span>  
9. <span data-ttu-id="cf031-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cf031-126">Click Save.</span></span>

