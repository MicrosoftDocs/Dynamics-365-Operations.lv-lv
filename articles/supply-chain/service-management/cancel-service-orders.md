---
title: Pakalpojumu pasūtījumu atcelšana
description: Pakalpojuma pasūtījumu vai pakalpojuma pasūtījuma rindu ir iespējams dzēst no paša pakalpojuma pasūtījuma vai arī atcelt vairākus pakalpojumu pasūtījumus veicot periodisko uzdevumu.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 779f535ac617d3f3940cc1b226fa53dc72e3411a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831606"
---
# <a name="cancel-service-orders"></a><span data-ttu-id="6fe7d-103">Pakalpojumu pasūtījumu atcelšana</span><span class="sxs-lookup"><span data-stu-id="6fe7d-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6fe7d-104">Pakalpojuma pasūtījumu vai pakalpojuma pasūtījuma rindu ir iespējams dzēst no paša pakalpojuma pasūtījuma vai arī atcelt vairākus pakalpojumu pasūtījumus veicot periodisko uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6fe7d-105">Pakalpojumu pasūtījumus nav iespējams atcelt, ja pakalpojuma pasūtījuma posms neļauj atcelšanu, ja pakalpojuma pasūtījumam ir krājuma vajadzības, vai arī ja pakalpojuma pasūtījums jau ir ticis iegrāmatots.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="6fe7d-106">Pakalpojuma pasūtījuma atcelšana formā Pakalpojumu pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="6fe7d-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="6fe7d-107">Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="6fe7d-108">Atlasiet pakalpojuma pasūtījumu un pēc tam noklikšķiniet uz **Atcelt pasūtījumu** darbību rūtī.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="6fe7d-109">Pakalpojuma pasūtījuma rindas atcelšana</span><span class="sxs-lookup"><span data-stu-id="6fe7d-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="6fe7d-110">Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="6fe7d-111">Veiciet dubultklikšķi uz pakalpojuma pasūtījumu, kas satur rindu, kuru vēlaties atcelt.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="6fe7d-112">Atlasiet pakalpojuma pasūtījuma rindu, kuru vēlaties atcelt, un pēc tam noklikšķiniet uz **Atcelt pasūtījuma rindu**, lai mainītu rindas statusu uz **Atcelta**.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="6fe7d-113">Lai atsauktu pakalpojuma pasūtījuma rindas atcelšanu un mainītu statusu atpakaļ uz <STRONG>Izveidota</STRONG>, noklikšķiniet uz <STRONG>Atsaukt atcelšanu</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="6fe7d-114">Vairāku pakalpojuma pasūtījumu atcelšana</span><span class="sxs-lookup"><span data-stu-id="6fe7d-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="6fe7d-115">Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Periodiskie** \> **Pakalpojuma pasūtījumi** \> **Atcelt pakalpojuma pasūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="6fe7d-116">Noklikšķiniet uz pogas **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="6fe7d-117">Veidlapā **Pieprasījums** slejā **Kritēriji** atlasiet pakalpojumu pasūtījumus, kurus vēlaties atcelt.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="6fe7d-118">Klikšķiniet **Labi**, lai aizvērtu veidlapu **Pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="6fe7d-119">Atlasiet izvēles rūtiņu **Rādīt informācijas žurnālu**, lai izveidotu informācijas žurnālu, kas parāda atceltos pakalpojuma pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="6fe7d-120">Atlasiet izvēles rūtiņu **Atsaukt atcelšanu**, ja pakalpojuma pasūtījumu vēlaties atkal statusā **Atcelts**.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="6fe7d-121">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-121">Click **OK**.</span></span>

<span data-ttu-id="6fe7d-122">Atlasītie pakalpojumu pasūtījumi tiek atcelti vai arī to progresa statuss tiek mainīts atpakaļ no **Atcelts** uz **Procesā**.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6fe7d-123">Ja ir tikusi atlasīta izvēles rūtiņa <STRONG>Atsaukt atcelšanu</STRONG>, pakalpojuma pasūtījumi ar progresa statusu <STRONG>Atcelts</STRONG> tiek mainīti atpakaļ un nenotiek pakalpojuma pasūtījumu atcelšana ar progresa statusu <STRONG>Procesā</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="6fe7d-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]