---
title: E-pasta veidņu pārvaldība
description: Šajā tēmā ir paskaidrots, kā pārvaldīt e-pasta veidnes.
author: andreabichsel
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41777436a624f9b98956553243056b92a00c1ed6
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693874"
---
# <a name="manage-email-templates"></a><span data-ttu-id="e2073-103">E-pasta veidņu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="e2073-103">Manage email templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2073-104">Varat pārsūtīt informāciju no uzņēmuma datu bāzes uz jauna dokumenta grāmatzīmēm un izmantot to veidnēs, kuras izmantojat efektīvai saziņai ar kandidātiem.</span><span class="sxs-lookup"><span data-stu-id="e2073-104">You can transfer information from your organization's database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="e2073-105">Lai to paveiktu, izveidojiet veidni, kas satur standarta tekstu un dažas grāmatzīmes, kur paredzēts ievietot sistēmas datus.</span><span class="sxs-lookup"><span data-stu-id="e2073-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="e2073-106">Piemēram, varat ievietot kandidāta adresi un kontaktinformāciju Microsoft Word dokumentā, ko varat izmantot, kad sazināties ar šo kandidātu.</span><span class="sxs-lookup"><span data-stu-id="e2073-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="e2073-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="e2073-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="e2073-108">Izvēlieties grāmatzīmes, kuras nepieciešams izmantot e-pasta veidnēs</span><span class="sxs-lookup"><span data-stu-id="e2073-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="e2073-109">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Cilvēkresursi > Personāla atlase >Saziņa > Pieteikumu grāmatzīmes**.</span><span class="sxs-lookup"><span data-stu-id="e2073-109">In the navigation pane, go to **Modules > Human Resources > Recruitment > Communication > Application bookmarks**.</span></span>
2. <span data-ttu-id="e2073-110">Sarakstā atrodiet un atlasiet vajadzīgo saziņas darbību.</span><span class="sxs-lookup"><span data-stu-id="e2073-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="e2073-111">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="e2073-111">Select **Edit**.</span></span>
4. <span data-ttu-id="e2073-112">Atlasiet laukus, kurus vēlaties spēt izmantot atlasītās saziņas darbības e-pasta veidnē, un pārvietojiet tos uz grāmatzīmju laukiem.</span><span class="sxs-lookup"><span data-stu-id="e2073-112">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="e2073-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e2073-113">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="e2073-114">E-pasta veidnes izveidošana</span><span class="sxs-lookup"><span data-stu-id="e2073-114">Create an email template</span></span>
1. <span data-ttu-id="e2073-115">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Cilvēkresursi > Personāla atlase >Saziņa > Pieteikumu e-pastu veidnes**.</span><span class="sxs-lookup"><span data-stu-id="e2073-115">In the navigation pane, go to **Modules > Human resources > Recruitment > Communication > Application e-mail templates**.</span></span>
2. <span data-ttu-id="e2073-116">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e2073-116">Select **New**.</span></span>
3. <span data-ttu-id="e2073-117">Laukā **Atbilstošā darbība** atlasiet **Intervija**.</span><span class="sxs-lookup"><span data-stu-id="e2073-117">In the **Correspondence action** field, select **Interview**.</span></span> <span data-ttu-id="e2073-118">Atlasiet saziņas darbību, kas satur grāmatzīmes, kuras jāizmanto šāda veida e-pasta saziņai.</span><span class="sxs-lookup"><span data-stu-id="e2073-118">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="e2073-119">Laukā **E-pasta veidne** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2073-119">In the **E-mail template** field, type a value.</span></span>
5. <span data-ttu-id="e2073-120">Laukā **Temats** ievadiet vērtību. </span><span class="sxs-lookup"><span data-stu-id="e2073-120">In the **Subject** field, type a value.</span></span>
6. <span data-ttu-id="e2073-121">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2073-121">In the **Text** field, type a value.</span></span>
7. <span data-ttu-id="e2073-122">Sarakstā atrodiet un atlasiet vajadzīgo grāmatzīmes lauku.</span><span class="sxs-lookup"><span data-stu-id="e2073-122">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="e2073-123">Turpiniet rakstīt e-pasta ziņojumu, ievietojot grāmatzīmju laukus vietās, kur tie nepieciešami.</span><span class="sxs-lookup"><span data-stu-id="e2073-123">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
9. <span data-ttu-id="e2073-124">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e2073-124">Select **Save**.</span></span>

