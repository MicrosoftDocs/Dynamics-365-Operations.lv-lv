---
title: Automātiska pakalpojumu pasūtījumu izveide
description: Varat veidot pakalpojumu pasūtījumus vienam pakalpojuma līgumam vai vairākiem pakalpojumu līgumiem.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 790c9007b4387b31e65cac650a57b873a37a70d0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234853"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="985dd-103">Automātiska pakalpojumu pasūtījumu izveide</span><span class="sxs-lookup"><span data-stu-id="985dd-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="985dd-104">Varat veidot pakalpojumu pasūtījumus vienam pakalpojuma līgumam vai vairākiem pakalpojumu līgumiem.</span><span class="sxs-lookup"><span data-stu-id="985dd-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="985dd-105">Pēc pakalpojumu pasūtījumu izveides varat tos skatīt veidlapā **Pakalpojumu pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="985dd-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="985dd-106">Pakalpojumu pasūtījumi ir izveidoti tikai derīgajam pakalpojuma līguma periodam.</span><span class="sxs-lookup"><span data-stu-id="985dd-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="985dd-107">Ja veidlapā **Pakalpojumu pasūtījumu izveide** norādītais intervāls ir pirms pakalpojuma līguma sākuma datuma vai pēc pakalpojuma līguma beigu datuma, pakalpojumu pasūtījumi tiek veidoti tikai intervāla daļai, kas ir periodā starp pakalpojuma līguma sākuma un beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="985dd-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="985dd-108">Ja izveidojat pakalpojumu pasūtījumus manuāli vai automātiski no pakalpojuma līguma rindas, pakalpojuma pasūtījumam jāsakrīt ar laika intervālu, kas definēts ar šīs rindas sākuma un beigu datumiem, izņemot gadījumus, kad nenosakāt rindas beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="985dd-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="985dd-109">Automātiska pakalpojumu pasūtījumu izveide pakalpojumu līgumam</span><span class="sxs-lookup"><span data-stu-id="985dd-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="985dd-110">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.</span><span class="sxs-lookup"><span data-stu-id="985dd-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="985dd-111">Izvēlieties pakalpojumu līgumu.</span><span class="sxs-lookup"><span data-stu-id="985dd-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="985dd-112">Noklikšķiniet uz cilnes **Piegāde** un pēc tam noklikšķiniet uz **Plānotie pakalpojumu pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="985dd-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="985dd-113">Lai definētu pakalpojumu periodu, laukā **Sākuma datums** un **Beigu datums** norādiet datumus.</span><span class="sxs-lookup"><span data-stu-id="985dd-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="985dd-114">Lai parādītu izveidoto pakalpojumu pasūtījumu sarakstu, atzīmējiet izvēles rūtiņu **Rādīt informācijas žurnālu**.</span><span class="sxs-lookup"><span data-stu-id="985dd-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="985dd-115">Atlasiet transakciju veidus lauku grupā **Iekļaut transakciju veidus**.</span><span class="sxs-lookup"><span data-stu-id="985dd-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="985dd-116">Darbību tipi attēlo rindas, kas izveidotas pakalpojumu līgumā, un katrs atlasītais darbības tips atkarībā no pakalpojumu intervāla, kas norādīts pakalpojumu līguma rindā, ģenerē vairākus pakalpojumu pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="985dd-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="985dd-117">Lai izveidotu kādu pakalpojumu pasūtījumu, kura nav pastāvīgajā pakalpojumu pasūtījumu sērijā, atzīmējiet izvēles rūtiņu **Pastāvīgie**.</span><span class="sxs-lookup"><span data-stu-id="985dd-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="985dd-118">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="985dd-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="985dd-119">Automātiska pakalpojumu pasūtījumu izveide vairākiem pakalpojumu līgumiem</span><span class="sxs-lookup"><span data-stu-id="985dd-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="985dd-120">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Periodiskie** \> **Pakalpojumu pasūtījumi** \> **Izveidot pakalpojumu pasūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="985dd-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="985dd-121">Noklikšķiniet uz **Atlasīt**, lai atlasītu, vai pievienot vai noņemt kritērijus, kuri jāizmanto pakalpojumu pasūtījumu izveidei.</span><span class="sxs-lookup"><span data-stu-id="985dd-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="985dd-122">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="985dd-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="985dd-123">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="985dd-123">See also</span></span>

[<span data-ttu-id="985dd-124">Pakalpojumu pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="985dd-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="985dd-125">Automātiska pakalpojumu pasūtījumu izveide</span><span class="sxs-lookup"><span data-stu-id="985dd-125">Automatically create service orders</span></span>](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]