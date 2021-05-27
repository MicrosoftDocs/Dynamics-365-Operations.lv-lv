---
title: Nevar lietot veidni izlaistai precei
description: Nevar lietot veidni izlaistai precei.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026704"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="8b1fc-103">Nevar lietot veidni, lai izveidotu izlaistu preci</span><span class="sxs-lookup"><span data-stu-id="8b1fc-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="8b1fc-104">KB numurs: 4612097</span><span class="sxs-lookup"><span data-stu-id="8b1fc-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="8b1fc-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="8b1fc-105">Symptoms</span></span>

<span data-ttu-id="8b1fc-106">Kad izveidojat jaunu izlaisto preci, izmantojot dialoglodziņu **Jauna izlaistā prece**, var atlasīt veidni.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="8b1fc-107">Veidnei jānodrošina noklusējuma iestatījumi daudziem jaunās izlaistās preces laukiem.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="8b1fc-108">Tomēr pēc veidnes atlases daži vai visi lauki nav iestatīti.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="8b1fc-109">Iemesls</span><span class="sxs-lookup"><span data-stu-id="8b1fc-109">Cause</span></span>

<span data-ttu-id="8b1fc-110">Daudzas Microsoft Dynamics 365 Supply Chain Management lapas ļauj izveidot veidni, kas nosaka sākotnējos iestatījumus ierakstiem, kas tiek rādīti šajās lapās.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="8b1fc-111">Vienu no šīm veidnēm varat izveidot, Darbību rūtī atlasot **Ieraksta informāciju** cilnē **Opcijas**.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="8b1fc-112">Tomēr izlaistās preces ir daudz sarežģītākas nekā vairums citu ierakstu veidu.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="8b1fc-113">Lai gan jūs varat atlasīt **Ieraksta informāciju** lapā **Izlaistās preces** lai izveidotu veidni, un, lai gan varat atlasīt šo veidni, kad izveidojat izlaisto preci, veidne neļaus sniegt prognozētās lauka vērtības jaunajai izlaistajai precei.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="8b1fc-114">Tādēļ izlaistajām precēm nevar izmantot "ieraksta informācijas" veidnes.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="8b1fc-115">Tā vietā ir jāizveido atvēlētas preču veidnes.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="8b1fc-116">Novēršana</span><span class="sxs-lookup"><span data-stu-id="8b1fc-116">Resolution</span></span>

<span data-ttu-id="8b1fc-117">Lai izveidotu preces veidni, darbību rūts cilnē **Produkts** izmantojiet izvēlni **Veidne**, nevis pogu **Ieraksta informācija** cilnē **Opcijas**.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="8b1fc-118">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8b1fc-119">Darbību rūts cilnes **Produkts** grupā **Jauns** atlasiet **Veidne**, un pēc tam, ja nepieciešams, atlasiet **Izveidot personisko veidni** vai **Izveidot koplietotu veidni**.</span><span class="sxs-lookup"><span data-stu-id="8b1fc-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
