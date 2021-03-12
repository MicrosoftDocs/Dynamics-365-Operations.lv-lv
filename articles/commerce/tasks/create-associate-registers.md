---
title: Reģistru izveide un sasaiste
description: Šajā procedūrā ir parādīts, kā izveidot pārdošanas punkta (POS) reģistru.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2415945c5a8f73e095627d638fcc572c50ffe8ca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964899"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="b9acd-103">Reģistru izveide un sasaiste</span><span class="sxs-lookup"><span data-stu-id="b9acd-103">Create and associate registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9acd-104">Šajā procedūrā ir parādīts, kā izveidot pārdošanas punkta (POS) reģistru.</span><span class="sxs-lookup"><span data-stu-id="b9acd-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="b9acd-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma USRT dati.</span><span class="sxs-lookup"><span data-stu-id="b9acd-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="b9acd-106">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāla iestatīšana > POS iestatīšana > Reģistri.</span><span class="sxs-lookup"><span data-stu-id="b9acd-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="b9acd-107">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="b9acd-107">Click New.</span></span>
3. <span data-ttu-id="b9acd-108">Laukā Reģistra numurs ierakstiet jaunā reģistra ID.</span><span class="sxs-lookup"><span data-stu-id="b9acd-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="b9acd-109">Reģistra ID parasti ietver kodus, kas palīdz reģistru kartēt uz veikalu, kuram tas pieder, un uz novietojumiem šajā veikalā.</span><span class="sxs-lookup"><span data-stu-id="b9acd-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="b9acd-110">Laukā Nosaukums ievadiet aprakstošu reģistra nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b9acd-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="b9acd-111">Laukā Veikala numurs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b9acd-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="b9acd-112">Laukā Aparatūras profils ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b9acd-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="b9acd-113">Aparatūras profili tiek izmantoti, lai norādītu perifērijas ierīces, kas tiks savienotas ar reģistru, piemēram, naudas kasti un kvītīm paredzēto printeri.</span><span class="sxs-lookup"><span data-stu-id="b9acd-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="b9acd-114">Laukā Vizuālais profils ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b9acd-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="b9acd-115">Vizuālie profili tiek izmantoti, lai norādītu POS fonā un pieteikšanās lapā izmantotos attēlus, kā arī dizainus šim POS.</span><span class="sxs-lookup"><span data-stu-id="b9acd-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="b9acd-116">Laukā EFT POS reģistra numurs ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b9acd-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="b9acd-117">EFT POS reģistra numurs tiek izmantots, lai informētu maksājumu apstrādātāju par to, kurš maksājumu terminālis sūta autorizācijas pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="b9acd-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="b9acd-118">Šī vērtība bieži tiek saukta par “Termināļa ID” vai “TID”.</span><span class="sxs-lookup"><span data-stu-id="b9acd-118">This value is often called the "Terminal ID" or "TID".</span></span> <span data-ttu-id="b9acd-119">Vērtība TID parasti ir atrodama uz maksājumu ierīces uzlīmes.</span><span class="sxs-lookup"><span data-stu-id="b9acd-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="b9acd-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b9acd-120">Click Save.</span></span>

