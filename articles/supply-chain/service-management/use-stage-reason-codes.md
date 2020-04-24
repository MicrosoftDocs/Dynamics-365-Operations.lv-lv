---
title: Stadiju iemeslu kodu izmantošana
description: Jāizmanto iemesla kods, lai norādītu, kādēļ pakalpojuma līmeņa līgums (SLA) ir atcelts vai kādēļ pakalpojuma pasūtījums ir pārsniedzis laika ierobežojumu, kas ir definēts SLA.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54dae6edb6681e1ba29709ebeeea2e5094262257
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206477"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="d1536-103">Stadiju iemeslu kodu izmantošana</span><span class="sxs-lookup"><span data-stu-id="d1536-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d1536-104">Jāizmanto iemesla kods, lai norādītu, kādēļ pakalpojuma līmeņa līgums (SLA) ir atcelts vai kādēļ pakalpojuma pasūtījums ir pārsniedzis laika ierobežojumu, kas ir definēts SLA.</span><span class="sxs-lookup"><span data-stu-id="d1536-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="d1536-105">Varat arī norādīt, ka iemesla kods ir nepieciešams, ja SLA tiek atcelts vai ja laika ierobežojums pārsniedz laiku, kas pakalpojuma pasūtījumam norādīts SLA.</span><span class="sxs-lookup"><span data-stu-id="d1536-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="d1536-106">Ja ir norādīts, ka iemesla kods ir nepieciešams, iemesla kods ir jāievada tālāk minētajās situācijās.</span><span class="sxs-lookup"><span data-stu-id="d1536-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="d1536-107">Ja pakalpojuma pasūtījums tiek pārvietots uz stadiju, kur tiek apturēta laika ierakstīšana attiecībā uz pakalpojuma pasūtījuma SLA.</span><span class="sxs-lookup"><span data-stu-id="d1536-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="d1536-108">Kad pakalpojuma pasūtījums ir parakstīts.</span><span class="sxs-lookup"><span data-stu-id="d1536-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="d1536-109">Kad laika ierakstīšana tiek apturēta manuāli.</span><span class="sxs-lookup"><span data-stu-id="d1536-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="d1536-110">Iestatiet cēloņa kodus</span><span class="sxs-lookup"><span data-stu-id="d1536-110">Set up reason codes</span></span>

1.  <span data-ttu-id="d1536-111">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu pasūtījumi** \> **Posmu pamatojuma kodi**.</span><span class="sxs-lookup"><span data-stu-id="d1536-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="d1536-112">Formā **Stadiju iemeslu kodi** noklikšķiniet uz **Jauns**, lai izveidotu jaunu iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="d1536-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="d1536-113">Laukā **Stadijas iemesla kods** ievadiet unikālu stadijas iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="d1536-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="d1536-114">Laukā **Apraksts** ievadiet stadijas iemesla koda aprakstu.</span><span class="sxs-lookup"><span data-stu-id="d1536-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="d1536-115">Aizveriet formu, lai saglabātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="d1536-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="d1536-116">Pieprasiet cēloņa kodus, ja pakalpojuma līmeņa juridiskais līgums ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="d1536-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="d1536-117">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="d1536-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="d1536-118">Formā **Pakalpojumu pārvaldības parametri** noklikšķiniet uz saites **Vispārīgi** un pēc tam atzīmējiet izvēles rūtiņu **Atcelšanas iemesla kods**.</span><span class="sxs-lookup"><span data-stu-id="d1536-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="d1536-119">Pieprasiet iemeslu kodus, ja pakalpojuma līmeņa līgumam iestatītais laika ierobežojums tiek pārsniegts</span><span class="sxs-lookup"><span data-stu-id="d1536-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="d1536-120">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="d1536-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="d1536-121">Formā **Pakalpojumu pārvaldības parametri** noklikšķiniet uz saites **Vispārīgi** un pēc tam atzīmējiet izvēles rūtiņu **Laika pārsniegšanas iemesla kods**.</span><span class="sxs-lookup"><span data-stu-id="d1536-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1536-122">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="d1536-122">See also</span></span>

[<span data-ttu-id="d1536-123">Laika ierakstīšanas sākšana un apturēšana pakalpojuma pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="d1536-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  


