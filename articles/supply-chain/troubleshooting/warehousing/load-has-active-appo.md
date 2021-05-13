---
title: Nevar apstiprināt sūtījumu, jo kalendārā radās problēma
description: Nevar apstiprināt sūtījumu, jo kalendārā radās problēma
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938513"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="4ac57-103">Nevar apstiprināt sūtījumu, jo kalendārā radās problēma</span><span class="sxs-lookup"><span data-stu-id="4ac57-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="4ac57-104">Kļūdas kods: TRX2716</span><span class="sxs-lookup"><span data-stu-id="4ac57-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="4ac57-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="4ac57-105">Symptoms</span></span>

<span data-ttu-id="4ac57-106">Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="4ac57-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="4ac57-107">Kalendāra tipam %1 ir nepieciešams paņemt un atdot norīkojumu %2.</span><span class="sxs-lookup"><span data-stu-id="4ac57-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="4ac57-108">Tādēļ kravas nosūtīšanu nevar apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="4ac57-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="4ac57-109">Iemesls</span><span class="sxs-lookup"><span data-stu-id="4ac57-109">Cause</span></span>

<span data-ttu-id="4ac57-110">Kravai pastāv aktīvie norīkojumi.</span><span class="sxs-lookup"><span data-stu-id="4ac57-110">Active appointments for the load exist.</span></span> <span data-ttu-id="4ac57-111">Piemēram, pastāv kārtula, saskaņā ar kuru ir pieprasīta autovadītāja atdošana.</span><span class="sxs-lookup"><span data-stu-id="4ac57-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="4ac57-112">Tādēļ noslodze pašlaik ir stāvoklī, kad sūtījuma apstiprināšana neizdodas.</span><span class="sxs-lookup"><span data-stu-id="4ac57-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="4ac57-113">Novēršana</span><span class="sxs-lookup"><span data-stu-id="4ac57-113">Resolution</span></span>

<span data-ttu-id="4ac57-114">Jums ir jāizpēta un jāizlabo problēmas ar aktīvajiem norīkojumi, kas ir saistītas ar krāvu.</span><span class="sxs-lookup"><span data-stu-id="4ac57-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="4ac57-115">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="4ac57-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4ac57-116">Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.</span><span class="sxs-lookup"><span data-stu-id="4ac57-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="4ac57-117">Darbību rūts cilnes **Transportācija** grupā **Norīkojumi** atlasiet **Norīkojumu plānošana**.</span><span class="sxs-lookup"><span data-stu-id="4ac57-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="4ac57-118">Izpildiet kādu no šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="4ac57-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="4ac57-119">Pārliecinieties, vai norīkojuma laikā ir pabeigta autovadītāja atdošana/paņemšana.</span><span class="sxs-lookup"><span data-stu-id="4ac57-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="4ac57-120">Pabeidziet vai atceliet norīkojumu.</span><span class="sxs-lookup"><span data-stu-id="4ac57-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="4ac57-121">Atspējot opciju **Pieprasītā autovadītāja atdošana** saistītajā norīkojuma kārtulā.</span><span class="sxs-lookup"><span data-stu-id="4ac57-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
