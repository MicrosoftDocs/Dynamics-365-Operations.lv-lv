---
title: Pakalpojumu veidnes
description: "Varat definēt pakalpojumu līgumu kā veidni un vēlāk pārkopēt veidnes rindas uz citu pakalpojumu līgumu vai pakalpojuma pasūtījumu."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 09f2da382cd7f3e0e3d4bfa389e9cdf74f00b501
ms.openlocfilehash: ade518095b77141fb31b597a955dd23aaae119d7
ms.contentlocale: lv-lv
ms.lasthandoff: 02/27/2018

---

# <a name="service-templates"></a><span data-ttu-id="e2cbf-103">Pakalpojumu veidnes</span><span class="sxs-lookup"><span data-stu-id="e2cbf-103">Service templates</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e2cbf-104">Varat definēt pakalpojumu līgumu kā veidni un vēlāk pārkopēt veidnes rindas uz citu pakalpojumu līgumu vai pakalpojuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="e2cbf-105">Paraugs</span><span class="sxs-lookup"><span data-stu-id="e2cbf-105">Example</span></span>

<span data-ttu-id="e2cbf-106">Klientam, kam tiek sniegts pakalpojums, ir identiski pakalpojumu elevatori piecās dažādās vietās.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="e2cbf-107">Vēlaties iestatīt piecus pakalpojumu līgumus klientam, pa vienam katrai vietai.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="e2cbf-108">Lai novērstu atkārtotu iestatīšanas darbu veikšanu un pārliecinātos, ka iestatīšanas informācija pakalpojuma līgumā ir identiska, izveidojat pakalpojumu līgumu un norādiet to kā veidni pakalpojuma darbam elevatoros.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="e2cbf-109">Tagad varat pārkopēt veidnes rindas uz pieciem jauniem pakalpojumu līgumiem, tādējādi katrā pakalpojumu līgumā atrodas rindas no veidnes.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="e2cbf-110">Izveidot veidni</span><span class="sxs-lookup"><span data-stu-id="e2cbf-110">Create a template</span></span>

<span data-ttu-id="e2cbf-111">Izveidojot pakalpojumu veidni, jūs izveidojat pakalpojumu līgumu, izveidojat tajā nepieciešamās rindas un pievienojat pakalpojumu līgumu pakalpojumu veidņu grupai.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="e2cbf-112">Pakalpojumu līgumu var definēt kā veidni tikai tad, ja tam nav pievienoti pakalpojuma pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="e2cbf-113">Tāpat arī nevienu pakalpojumu pasūtījumu nevar izveidot no pakalpojumu līguma, kas definēts kā veidne.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="e2cbf-114">Kopēt veidnes rindas</span><span class="sxs-lookup"><span data-stu-id="e2cbf-114">Copy template lines</span></span>

<span data-ttu-id="e2cbf-115">Variet pārkopēt veidnes rindas no pakalpojumu veidnes uz citu pakalpojumu līgumu vai pakalpojumu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="e2cbf-116">Kopējot veidnes rindas savos pakalpojumu pasūtījumos vai pakalpojumu līgumos, veidņu grupas tiek parādītas koka skatā, kur katru grupu var paplašināt.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="e2cbf-117">Šis atainojums ļauj apskatīt katru veidni un veidnes rindu.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="e2cbf-118">Ir vienkāršāk noteikt pakalpojuma veidnes rindas, ko vēlaties pārkopēt, ja veidnes sagrupētas pēc vārdiem, kas atspoguļo to pielietojumu.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2cbf-119">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="e2cbf-119">Related topics</span></span>

[<span data-ttu-id="e2cbf-120">Kopēt pakalpojumu veidņu rindas</span><span class="sxs-lookup"><span data-stu-id="e2cbf-120">Copy service templates lines</span></span>](copy-service-template-lines.md)

