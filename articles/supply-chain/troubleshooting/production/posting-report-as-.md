---
title: Kļūda pabeigtās ražošanas žurnāla grāmatošanas laikā
description: Kad grāmatojat žurnālu Ziņot kā pabeigtu, saņemat kļūdas ziņojumu, ka pasūtīto daudzumu nevar samazināt.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026700"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="b5cca-103">Kļūda pabeigtās ražošanas žurnāla grāmatošanas laikā</span><span class="sxs-lookup"><span data-stu-id="b5cca-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="b5cca-104">KB numurs: 4612891</span><span class="sxs-lookup"><span data-stu-id="b5cca-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="b5cca-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="b5cca-105">Symptoms</span></span>

<span data-ttu-id="b5cca-106">Kad jūs iegrāmatojiet žurnālu **Ziņot kā pabeigtu**, parādās kļūda un saņemat šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="b5cca-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="b5cca-107">Pasūtīto daudzumu nav iespējams samazināt, jo atvērtās krājumu darbības ar statusu Pasūtīts nav pietiekamas.</span><span class="sxs-lookup"><span data-stu-id="b5cca-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="b5cca-108">Krājumi ir Nopirkti, Saņemti vai Reģistrēti.</span><span class="sxs-lookup"><span data-stu-id="b5cca-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="b5cca-109">Šī kļūda rodas tikai tad, ja lauks **Kļūdu daudzums** ir iestatīts **Ziņot kā pabeigtu** žurnāla pirmajā rindā, un lauks **Labs daudzums** ir iestatīts pēdējā rindā.</span><span class="sxs-lookup"><span data-stu-id="b5cca-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="b5cca-110">Ja pēdējā rindā ir iestatīts lauks **Kļūdu daudzums**, kļūdas nenotiek.</span><span class="sxs-lookup"><span data-stu-id="b5cca-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="b5cca-111">Novēršana</span><span class="sxs-lookup"><span data-stu-id="b5cca-111">Resolution</span></span>

<span data-ttu-id="b5cca-112">Lai novērstu šo kļūdu, atveriet lapu **Ražošanas kontroles parametri** un pēc tam cilnē **Vispārīgi** iestatiet **Palielināt atlikušo daudz. ar kļūdu daudz.** opciju uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="b5cca-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
