---
title: Izveidot pakalpojumu uzdevuma attiecības
description: Jūs varat saistīt pakalpojumu uzdevumus ar pakalpojumu līgumiem vai pakalpojumu pasūtījumiem, lai aprakstītu līgumam vai pasūtījumam izpildāmo pakalpojuma uzdevumu.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e50b4322c65097ab4f8aba9c36e4d5e6cc4c01b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978634"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="687b0-103">Izveidot pakalpojumu uzdevuma attiecības</span><span class="sxs-lookup"><span data-stu-id="687b0-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="687b0-104">Jūs varat saistīt pakalpojumu uzdevumus ar pakalpojumu līgumiem vai pakalpojumu pasūtījumiem, lai aprakstītu līgumam vai pasūtījumam izpildāmo pakalpojuma uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="687b0-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="687b0-105">Šī informācija ir pieejama pakalpojuma tehniskajiem speciālistiem un debitoriem.</span><span class="sxs-lookup"><span data-stu-id="687b0-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="687b0-106">Saistības izveidošana ar pakalpojuma līgumu</span><span class="sxs-lookup"><span data-stu-id="687b0-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="687b0-107">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.</span><span class="sxs-lookup"><span data-stu-id="687b0-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="687b0-108">Atlasiet eksistējošu pakalpojumu līgumu un izveidojiet jaunu pakalpojumu līgumu</span><span class="sxs-lookup"><span data-stu-id="687b0-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="687b0-109">Darbību rūts noklikšķiniet uz pogas **Pakalpojumu uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="687b0-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="687b0-110">Veidlapā **Pakalpojumu uzdevumi** nospiediet taustiņu kombināciju CTRL + N, lai izveidotu jaunu rindu, un pēc tam atlasiet pakalpojuma uzdevumu sarakstā **Pakalpojumu uzdevumi**, lai pakalpojumu līgumam pievienotu pakalpojuma uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="687b0-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="687b0-111">Cilnes **Apraksts** brīvā teksta laukos ievadiet jebkuru iekšēju vai ārēju notu aprakstus.</span><span class="sxs-lookup"><span data-stu-id="687b0-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="687b0-112">Aizveriet formu, lai saglabātu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="687b0-112">Close the form to save the record.</span></span>

<span data-ttu-id="687b0-113">Atkārtojiet šo procedūru, līdz esat izveidojis visas nepieciešamās pakalpojumu uzdevumu relācijas šim pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="687b0-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="687b0-114">Tagad ir iespējams noteikt šos pakalpojumu uzdevumus jebkurai no pievienotā līguma rindām.</span><span class="sxs-lookup"><span data-stu-id="687b0-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="687b0-115">Pakalpojuma līgumā izveidotā pakalpojumu uzdevumu saistība ir pieejama no visiem pakalpojumu pasūtījumiem, kas pievienoti pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="687b0-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="687b0-116">Saistības izveidošana ar pakalpojuma pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="687b0-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="687b0-117">Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="687b0-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="687b0-118">Atlasiet eksistējošu pakalpojumu pasūtījumu un izveidojiet jaunu pakalpojumu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="687b0-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="687b0-119">Darbību rūts noklikšķiniet uz pogas **Pakalpojumu uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="687b0-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="687b0-120">Veidlapā **Pakalpojumu uzdevumi** nospiediet taustiņu kombināciju CTRL + N, lai izveidotu jaunu rindu, un pēc tam atlasiet pakalpojuma uzdevumu sarakstā **Pakalpojumu uzdevumi**, lai pakalpojumu pasūtījumam pievienotu pakalpojuma uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="687b0-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="687b0-121">Cilnes **Apraksts** brīvā teksta laukos ievadiet jebkuru iekšēju vai ārēju notu aprakstus.</span><span class="sxs-lookup"><span data-stu-id="687b0-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="687b0-122">Aizveriet formu, lai saglabātu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="687b0-122">Close the form to save the record.</span></span>

<span data-ttu-id="687b0-123">Atkārtojiet šo procedūru līdz esat izveidojis visas nepieciešamās pakalpojumu uzdevumu relācijas šim pakalpojumu pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="687b0-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="687b0-124">Tagad ir iespējams atlasīt pakalpojumu uzdevumu, kuram jūs izveidojāt relāciju, veidojot pakalpojumu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="687b0-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="687b0-125">Pakalpojumu uzdevuma saistības, kas iz izveidotas pakalpojumu pasūtījumā, ir pieejamas noteiktā pakalpojumu pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="687b0-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="687b0-126">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="687b0-126">See also</span></span>

[<span data-ttu-id="687b0-127">Pakalpojumu uzdevumu pārskats</span><span class="sxs-lookup"><span data-stu-id="687b0-127">Service tasks overview</span></span>](service-tasks.md)


  


