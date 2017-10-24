--- 
title: "Nodokļu iestāžu iestatīšana"
description: "PVN iestādes ir iestādes, kurām jāziņo par iekasēto PVN un tas jāiemaksā."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f75ee28343161026a73dd889b345d65ecc345884
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="56dd5-103">Nodokļu iestāžu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="56dd5-103">Set up sales tax authorities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56dd5-104">PVN iestādes ir iestādes, kurām jāziņo par iekasēto PVN un tas jāiemaksā.</span><span class="sxs-lookup"><span data-stu-id="56dd5-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="56dd5-105">Iestādei PVN var maksāt tieši vai caur nodokļu iestādei izveidotu kreditora kontu.</span><span class="sxs-lookup"><span data-stu-id="56dd5-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="56dd5-106">Ja šo iespēju izmantojat, uzņēmums laicīgai PVN nomaksai nodokļu iestādei var izmantot savas parastās maksāšanas procedūras.</span><span class="sxs-lookup"><span data-stu-id="56dd5-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="56dd5-107">Ja nodokļu iestādi neiestatāt kā kreditoru, kādam ir jāsagatavo manuāls maksājums nodokļu iestādei līdz atbilstošajam termiņa beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="56dd5-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="56dd5-108">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="56dd5-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="56dd5-109">Pārejiet uz sadaļu Nodokļi > Netiešie nodokļi > PVN > PVN iestādes.</span><span class="sxs-lookup"><span data-stu-id="56dd5-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="56dd5-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="56dd5-110">Click New.</span></span>
3. <span data-ttu-id="56dd5-111">Ierakstiet vērtību laukā Iestāde.</span><span class="sxs-lookup"><span data-stu-id="56dd5-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="56dd5-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="56dd5-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="56dd5-113">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="56dd5-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="56dd5-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="56dd5-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="56dd5-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="56dd5-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="56dd5-116">Atlasiet pārskata izkārtojumu savai valstij/reģionam, ja tāds ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="56dd5-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="56dd5-117">Ja pārskata izkārtojumi neatbilst nodokļu iestādes prasībām, izmantojiet noklusēto izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="56dd5-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="56dd5-118">Ievadiet vērtības Noapaļošanas veidlapā un Noapaļošanas laukos, lai norādītu, kā noapaļot maksājamo nodokļa kopsummu.</span><span class="sxs-lookup"><span data-stu-id="56dd5-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="56dd5-119">Noapaļošanas starpības tiks grāmatotas Automātisko transakciju kontos, kas izveidoti Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="56dd5-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="56dd5-120">Ievadiet skaitli Noapaļošanas laukā.</span><span class="sxs-lookup"><span data-stu-id="56dd5-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="56dd5-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="56dd5-121">Click Save.</span></span>


