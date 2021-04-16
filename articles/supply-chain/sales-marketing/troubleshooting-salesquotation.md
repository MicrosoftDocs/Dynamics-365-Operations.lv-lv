---
title: Pārdošanas piedāvājumu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas piedāvājumiem.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824754"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="0da73-103">Pārdošanas piedāvājumu problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="0da73-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="0da73-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas piedāvājumiem.</span><span class="sxs-lookup"><span data-stu-id="0da73-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="0da73-105">Nevar izmainīt pārdošanas piedāvājuma pārdošanas daudzumu pakalpojumu krājumam.</span><span class="sxs-lookup"><span data-stu-id="0da73-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0da73-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="0da73-106">Issue description</span></span>

<span data-ttu-id="0da73-107">Mēģinot iestatīt pārdošanas daudzumu (**SalesQty** lauks) pārdošanas piedāvājuma rindas krājuma tipam *Pakalpojums*, tiks parādīts šāds ziņojums: “Lauka Daudzums atjaunināšana nav atļauta.”</span><span class="sxs-lookup"><span data-stu-id="0da73-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0da73-108">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="0da73-108">Issue resolution</span></span>

<span data-ttu-id="0da73-109">Pārdošanas daudzumu nevar iestatīt precēm, kas ir pakalpojumu krājumi.</span><span class="sxs-lookup"><span data-stu-id="0da73-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="0da73-110">Piemēram, ja piedāvājat krājuma instalēšanas pakalpojumu, nav jēgas ierakstīt daudzumu, jo fiziska krājuma nav.</span><span class="sxs-lookup"><span data-stu-id="0da73-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="0da73-111">Ir tikai pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="0da73-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]