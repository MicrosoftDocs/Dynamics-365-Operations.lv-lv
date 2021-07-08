---
title: Iespējot Power BI Globālajai krājumu uzskaitei
description: Šajā tēmā ir aprakstīts, kā iespējot Microsoft Power BI Globālajai krājumu uzskaiti.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273191"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="095a9-103">Iespējot Power BI Globālajai krājumu uzskaitei</span><span class="sxs-lookup"><span data-stu-id="095a9-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="095a9-104">Varat piespraust jūsu uzņēmuma [PowerBI.com](https://powerbi.com/) informācijas paneļus un pārskatus savai Microsoft Dynamics 365 lietojumprogrammas darbvietai.</span><span class="sxs-lookup"><span data-stu-id="095a9-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="095a9-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="095a9-105">Prerequisites</span></span>

<span data-ttu-id="095a9-106">Pirms Power BI pārskatu iespējošanas jābūt šādiem priekšnosacījumiem:</span><span class="sxs-lookup"><span data-stu-id="095a9-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="095a9-107">Jums ir jābūt sistēmas administratoram Dynamics 365 programmā.</span><span class="sxs-lookup"><span data-stu-id="095a9-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="095a9-108">Jums jābūt [PowerBI.com](https://powerbi.com/) kontam.</span><span class="sxs-lookup"><span data-stu-id="095a9-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="095a9-109">Jūsu Power BI kontā ir jābūt vismaz vienam informācijas panelim un vienam pārskatam.</span><span class="sxs-lookup"><span data-stu-id="095a9-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="095a9-110">Jums jābūt sava Azure Active Directory (Azure AD) konta administratoram.</span><span class="sxs-lookup"><span data-stu-id="095a9-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="095a9-111">Domēnam Azure AD jābūt tam pašam domēnam, ko izmantojāt savam [PowerBI.com](https://powerbi.com/) kontam.</span><span class="sxs-lookup"><span data-stu-id="095a9-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="095a9-112">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="095a9-112">Setup</span></span>

<span data-ttu-id="095a9-113">Lai iestatītu Power BI integrāciju, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="095a9-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="095a9-114">Pierakstieties portālā [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="095a9-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="095a9-115">Dodieties uz **Koplietojamo līdzekļu bibliotēku**, atlasiet **Power BI pārskata modeli** kā līdzekļu tipu un lejupielādējiet pakotni **Globālā krājumu uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="095a9-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="095a9-116">Piesakieties [PowerBI.com](https://app.powerbi.com/) un augšupielādējiet **Globālās krājumu uzskaites** Power BI pārskata failu, veicot šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="095a9-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="095a9-117">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="095a9-117">Select **New**.</span></span>
    1. <span data-ttu-id="095a9-118">Atlasiet **Augšupielādēt failu**.</span><span class="sxs-lookup"><span data-stu-id="095a9-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="095a9-119">Atlasiet **Globālās krājumu uzskaites** Power BI pārskata failu.</span><span class="sxs-lookup"><span data-stu-id="095a9-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="095a9-120">Konfigurējiet **Globālās krājumu uzskaites** Power BI pārskatu, izpildot šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="095a9-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="095a9-121">Dodieties uz **Manu darbvietu**, atrodiet Globālās krājumu uzskaites datu kopu un pēc tam izvēlnē **Opcijas** atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="095a9-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="095a9-122">Sadaļā **Globālās krājumu uzskaites iestatījumi** izvērsiet **Parametri** un pēc vajadzības atjauniniet visus parametrus.</span><span class="sxs-lookup"><span data-stu-id="095a9-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="095a9-123">Reģistrējiet programmu atbilstoši aprakstam sadaļā [Konfigurēt PowerBI.com integrāciju](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span><span class="sxs-lookup"><span data-stu-id="095a9-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="095a9-124">Integrējiet **Globālās krājumu uzskaites** Power BI pārskata failu programmā Dynamics 365 Supply Chain Management, izpildot šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="095a9-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="095a9-125">Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> PowerBI.com konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="095a9-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="095a9-126">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="095a9-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="095a9-127">Atlasiet **Aktivizēt PowerBI.Com integrāciju**.</span><span class="sxs-lookup"><span data-stu-id="095a9-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="095a9-128">Laukā **Programmas ID** ievadiet pieteikuma ID.</span><span class="sxs-lookup"><span data-stu-id="095a9-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="095a9-129">Laukā **Pieteikuma atslēga** ievadiet pieteikuma atslēgu.</span><span class="sxs-lookup"><span data-stu-id="095a9-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="095a9-130">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="095a9-130">Select **Save**.</span></span>

1. <span data-ttu-id="095a9-131">Atsvaidziniet lapu, lai parādās Power BI pierakstīšanās dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="095a9-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="095a9-132">Cilnē **Opcijas** atlasiet **Atvērt pārskatu katalogu** un pēc tam atlasiet agrāk augšupielādēto **Globālās krājuma uzskaites** Power BI pārskata failu.</span><span class="sxs-lookup"><span data-stu-id="095a9-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="095a9-133">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="095a9-133">Refresh the page.</span></span> <span data-ttu-id="095a9-134">Jums vajadzētu redzēt, ka jūsu pārskats ir pievienots.</span><span class="sxs-lookup"><span data-stu-id="095a9-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="095a9-135">Sadaļā **Power BI pārskati** atlasiet saiti **Globālā krājumu uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="095a9-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="095a9-136">Papildinformāciju skatiet tēmā [PowerBI.com integrācijas konfigurēšana](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="095a9-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
