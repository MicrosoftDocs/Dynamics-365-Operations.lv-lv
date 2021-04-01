---
title: Uzturēšanas grafika izmaksas
description: Šajā tēmā ir paskaidrotas uzturēšanas grafika izmaksas programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9686efb228e123671ba93a37480d2daac8d038a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252970"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="2cf9d-103">Uzturēšanas grafika izmaksas</span><span class="sxs-lookup"><span data-stu-id="2cf9d-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2cf9d-104">Programmā Asset Management jūs varat aprēķināt budžeta izmaksas uzturēšanas grafika rindām.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="2cf9d-105">Tas ir noderīgi, ja vēlaties iegūt pārskatu par paredzamajām izmaksām, piemēram, izmaksām, kas attiecas uz plānotiem preventīviem uzturēšanas darbiem nākamajam gadam.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="2cf9d-106">Aprēķini ir balstīti esošās uzturēšanas grafika rindās tipiem "Uzturēšanas plāni" un "Uzturēšanas cikli" un "Uzturēšanas pieprasījumi"</span><span class="sxs-lookup"><span data-stu-id="2cf9d-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="2cf9d-107">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Uzturēšanas grafika izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="2cf9d-108">Dialoglodziņā **Uzturēšanas grafika izmaksas** jūs varat atlasīt opciju **Finansiālā dimensija iestatīta**, ja vēlaties redzēt izmaksas grupētas finansiālās dimensijās.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="2cf9d-109">Finansiālās dimensijas tiek uzstādītas **Virsgrāmata** > **Kontu plāns** > **Dimensijas** > **Finansiālo dimensiju kopas**.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="2cf9d-110">Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties uzturēšanas grafika rindas attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="2cf9d-111">Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas uzturēšanas grafika rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="2cf9d-112">Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas grafika rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="2cf9d-113">Ja vēlaties veikt aprēķinus par konkrētiem līdzekļiem, kopsavilkuma cilnē **Iekļaujamie ieraksti** noklikšķiniet uz **Filtrēt** un atlasiet atbilstošos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="2cf9d-114">Ja nepieciešams, jūs varat arī konkretizēt **Paredzamo sākuma** datumu izmaksu aprēķinam vai atlasīt atšķirīgu **Statusu** izmaksu aprēķinam</span><span class="sxs-lookup"><span data-stu-id="2cf9d-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="2cf9d-115">Noklikšķiniet uz **Labi**, lai sāktu izmaksu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="2cf9d-116">Cilnē **Uzturēšanas grafika izmaksas** darbību rūts grupās **Grupēt pēc...** noklikšķiniet uz attiecīgajām pogām, lai uzrādītu nepieciešamo izmaksu aprēķina informācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="2cf9d-117">Atlasītās darbību rūts grupas pogas ir izceltas.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="2cf9d-118">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="2cf9d-119">Noklikšķiniet uz pogas **Aprēķināt izmaksas**, ja vēlaties veikt jaunu izmaksu aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="2cf9d-120">Nākamajā attēlā ir redzami uzturēšanas grafika izmaksu aprēķina rezultāti.</span><span class="sxs-lookup"><span data-stu-id="2cf9d-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![1. attēls](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]