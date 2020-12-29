---
title: Problēmu novēršana saistībā ar jaunināšanu un migrāciju uz uzlaboto noliktavu pārvaldību
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, jauninot un migrējot uz uzlaboto noliktavu pārvaldību.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d50c6d75ec7cc98109cf81c38ff42b4d2b105b0c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645821"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="5ee3d-103">Problēmu novēršana saistībā ar jaunināšanu un migrāciju uz uzlaboto noliktavu pārvaldību</span><span class="sxs-lookup"><span data-stu-id="5ee3d-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ee3d-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, jauninot un migrējot uz uzlaboto noliktavu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="5ee3d-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="5ee3d-105">Tiek parādīts šāds kļūdas ziņojums: "java.security.cert.certPathValidatorException: sertifikācijas ceļa uzticamības enkurs nav atrasts."</span><span class="sxs-lookup"><span data-stu-id="5ee3d-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5ee3d-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5ee3d-106">Issue description</span></span>

<span data-ttu-id="5ee3d-107">Šis kļūdas ziņojums tiek parādīts noliktavu programmā, jo pašparakstītie sertifikāti nav uzticami Android 8+ lokālā vidē.</span><span class="sxs-lookup"><span data-stu-id="5ee3d-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5ee3d-108">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5ee3d-108">Issue resolution</span></span>

<span data-ttu-id="5ee3d-109">Izmantojiet ārēju (publisku) sertificēšanas iestādi (CA).</span><span class="sxs-lookup"><span data-stu-id="5ee3d-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="5ee3d-110">Šīs problēmas labojums ir pieejams noliktavu programmas 1.9.0.0 versijā.</span><span class="sxs-lookup"><span data-stu-id="5ee3d-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="5ee3d-111">Plašāku informāciju par šo problēmu un to, kā to novērst, skatiet šeit: [Noliktavu programmas savienojuma problēmu novēršana](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5ee3d-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="5ee3d-112">Kāds ir apstiprinātais process pārejai no pamata noliktavas uz papildu noliktavu?</span><span class="sxs-lookup"><span data-stu-id="5ee3d-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="5ee3d-113">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5ee3d-113">Issue description</span></span>

<span data-ttu-id="5ee3d-114">Jūs pašlaik darbojaties ar krājumu pārvaldību un izmantojat pamata krājumu funkcionalitāti, un jūs vēlaties pārvietoties uz papildu noliktavu, lai varētu izmantot mobilās ierīces, viļņus un darbu.</span><span class="sxs-lookup"><span data-stu-id="5ee3d-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="5ee3d-115">Tomēr, mēģinot veikt šo pārvietošanos, rodas problēmas.</span><span class="sxs-lookup"><span data-stu-id="5ee3d-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="5ee3d-116">Piemēram, preces nevar mainīt, jo tās izmanto noliktavas dimensijas (vietne, noliktava un atrašanās vieta), jo precēm ir darījumi ar tiem.</span><span class="sxs-lookup"><span data-stu-id="5ee3d-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="5ee3d-117">Tāpēc jums jāiemācās, kāds ir apstiprinātais process pārejai no pamata noliktavas uz papildu noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5ee3d-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5ee3d-118">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5ee3d-118">Issue resolution</span></span>

<span data-ttu-id="5ee3d-119">Lai iegūtu vairāk informācijas par procesu pārejai no pamata noliktavas uz papildu noliktavu, skatiet sekojošos emuāra ierakstos un dokumentācijā:</span><span class="sxs-lookup"><span data-stu-id="5ee3d-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="5ee3d-120">Iespējot noliktavas pārvaldības procesu esošajām precēm un noliktavām</span><span class="sxs-lookup"><span data-stu-id="5ee3d-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="5ee3d-121">Microsoft Dynamics AX WMS migrācija uz jaunu R3 noliktavu un transportēšanas funkcionalitāti</span><span class="sxs-lookup"><span data-stu-id="5ee3d-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="5ee3d-122">WMSI/WMS2 krājumu migrācija</span><span class="sxs-lookup"><span data-stu-id="5ee3d-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="5ee3d-123">Jaunināt noliktavas pārvaldību no Microsoft Dynamics AX 2012 uz Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ee3d-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
