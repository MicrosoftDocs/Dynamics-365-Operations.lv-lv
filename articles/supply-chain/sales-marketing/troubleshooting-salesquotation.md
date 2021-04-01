---
title: Pārdošanas piedāvājumu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas piedāvājumiem.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9a9cc821d2fe9accad1dae210271682cdd2ce4ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232210"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="053b9-103">Pārdošanas piedāvājumu problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="053b9-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="053b9-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas piedāvājumiem.</span><span class="sxs-lookup"><span data-stu-id="053b9-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="053b9-105">Nevar izmainīt pārdošanas piedāvājuma pārdošanas daudzumu pakalpojumu krājumam.</span><span class="sxs-lookup"><span data-stu-id="053b9-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="053b9-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="053b9-106">Issue description</span></span>

<span data-ttu-id="053b9-107">Mēģinot iestatīt pārdošanas daudzumu (**SalesQty** lauks) pārdošanas piedāvājuma rindas krājuma tipam *Pakalpojums*, tiks parādīts šāds ziņojums: “Lauka Daudzums atjaunināšana nav atļauta.”</span><span class="sxs-lookup"><span data-stu-id="053b9-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="053b9-108">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="053b9-108">Issue resolution</span></span>

<span data-ttu-id="053b9-109">Pārdošanas daudzumu nevar iestatīt precēm, kas ir pakalpojumu krājumi.</span><span class="sxs-lookup"><span data-stu-id="053b9-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="053b9-110">Piemēram, ja piedāvājat krājuma instalēšanas pakalpojumu, nav jēgas ierakstīt daudzumu, jo fiziska krājuma nav.</span><span class="sxs-lookup"><span data-stu-id="053b9-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="053b9-111">Ir tikai pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="053b9-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]