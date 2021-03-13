---
title: Līdzekļu patapinājumi
description: Šajā tēmā aprakstīts, kā reģistrēt patapinātos līdzekļus Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 355e3d3e0e952db14a03810145528f9701804ca2
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022336"
---
# <a name="asset-loans"></a><span data-ttu-id="05d80-103">Līdzekļu patapinājumi</span><span class="sxs-lookup"><span data-stu-id="05d80-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="05d80-104">Ja jūsu uzņēmums saņem līdzekļus remonta vai uzturēšanas darbiem no iekšējām atrašanās vietām vai debitoriem, un, ja jūs īslaicīgi patapināt līdzekļus šīm atrašanās vietām vai debitoriem, Līdzekļu pārvaldība var izsekot līdzekļu patapinājumus.</span><span class="sxs-lookup"><span data-stu-id="05d80-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="05d80-105">Reģistrēt līdzekļu patapinājumus uzturēšanas pieprasījumā</span><span class="sxs-lookup"><span data-stu-id="05d80-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="05d80-106">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Uzturēšanas pieprasījumi** \> **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="05d80-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="05d80-107">Atlasiet uzturēšanas pieprasījumu, lai reģistrētu līdzekļa patapinājumu un pēc tam atlasiet **Rediģēt.**</span><span class="sxs-lookup"><span data-stu-id="05d80-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="05d80-108">Lapā **Pieprasījums** atlasiet **Nosūtīt patapinājuma līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="05d80-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="05d80-109">Atlasiet līdzekli un ievadiet plānoto atgriešanas datumu.</span><span class="sxs-lookup"><span data-stu-id="05d80-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="05d80-110">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="05d80-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="05d80-111">Varat nosūtīt patapinājuma līdzekli tikai tad, ja ir pieejams tā paša līdzekļu tipa aktīvs.</span><span class="sxs-lookup"><span data-stu-id="05d80-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="05d80-112">Līdzeklim, kuru patapināt, ir jābūt līdzekļa dzīves cikla statusam, kas ļauj to izmantot kā patapinājuma līdzekli, piemēram, **InStorage**.</span><span class="sxs-lookup"><span data-stu-id="05d80-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="05d80-113">Kad līdzekļa patapinājums ir reģistrēts, līdzekļa dzīves cikla statuss automātiski tiek atjaunināts uz, piemēram, **OnLoan**.</span><span class="sxs-lookup"><span data-stu-id="05d80-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="05d80-114">Lai skatītu sarakstu ar visiem līdzekļiem, kurus esat patapinājis citai atrašanās vietai vai debitoriem, atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļa patapinājums** \> **Visi līdzekļu patapinājumi**.</span><span class="sxs-lookup"><span data-stu-id="05d80-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="05d80-115">Ja līdzeklim ir atzīmēta izvēles rūtiņa **Pabeigts**, līdzeklis ir reģistrēts kā atgriezts jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="05d80-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Uzturēšanas pieprasījumu pārvaldība](media/06-manage-maintenance-requests.png)

<span data-ttu-id="05d80-117">Lapā **Aktīvie līdzekļu patapinājumi** varat skatīt visu to patapinājuma līdzekļu sarakstu, kas vēl nav atgriezti jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="05d80-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="05d80-118">Reģistrēt patapinājuma līdzekļus kā atgrieztus</span><span class="sxs-lookup"><span data-stu-id="05d80-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="05d80-119">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļa patapinājums** \> **Aktīvie līdzekļu patapinājumi**.</span><span class="sxs-lookup"><span data-stu-id="05d80-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="05d80-120">Atlasiet līdzekļa patapinājumu, lai reģistrētu kā atgrieztu, un pēc tam atlasiet **Atgriezt līdzekļa patapinājumu**.</span><span class="sxs-lookup"><span data-stu-id="05d80-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="05d80-121">Laukā **Atgriezts** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="05d80-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="05d80-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="05d80-122">Select **OK**.</span></span>
5. <span data-ttu-id="05d80-123">Atsvaidziniet saraksta **Aktīvie līdzekļu patapinājumi** lapu un pievērsiet uzmanību, ka līdzekļa patapinājums vairs nav redzams sarakstā.</span><span class="sxs-lookup"><span data-stu-id="05d80-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
