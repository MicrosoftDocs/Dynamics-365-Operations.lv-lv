---
title: Problēmu novēršana saistībā ar risinājuma apzināšanos
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar risinājumu apzināšanos.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 86dd8803f7560ea337f2452e9722fe0151466daf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748877"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="0ff5d-103">Problēmu novēršana saistībā ar risinājuma apzināšanos</span><span class="sxs-lookup"><span data-stu-id="0ff5d-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="0ff5d-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="0ff5d-105">Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar risinājuma apzināšanos.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0ff5d-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="0ff5d-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="0ff5d-108">Kļūda duālā ieraksta lapā</span><span class="sxs-lookup"><span data-stu-id="0ff5d-108">Error on the Dual-write page</span></span>

<span data-ttu-id="0ff5d-109">Lapā **Duālais ieraksts** var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram:</span><span class="sxs-lookup"><span data-stu-id="0ff5d-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="0ff5d-110">*Elements ar nosaukumu 'msdyn\_dualwriteentitymap' ar namemapping = 'Loģisks' netika atrasts MetadataCache.*</span><span class="sxs-lookup"><span data-stu-id="0ff5d-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="0ff5d-111">Lai novērstu šo problēmu, pārliecinieties, vai programmā Dataverse ir instalēts duālā ieraksta pamata risinājums.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-111">To fix the issue, make sure that the dual-write core solution is installed in Dataverse.</span></span> <span data-ttu-id="0ff5d-112">Risinājumu apzināšanai duālais ieraksts ir priekšnoteikums.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]