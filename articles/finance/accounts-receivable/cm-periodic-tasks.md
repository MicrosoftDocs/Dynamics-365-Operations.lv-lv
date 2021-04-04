---
title: Kredīta pārvaldības periodiskie uzdevumi
description: Šajā tēmā aprakstīti periodiskie uzdevumi, kas ir nepieciešami kā debitoru kredīta limitu pārvaldības procesa daļa.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a034d563c12c4ba8b99e13b30ea2683555a01276
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254491"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="42db2-103">Periodiski kredītu pārvaldības uzdevumi</span><span class="sxs-lookup"><span data-stu-id="42db2-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42db2-104">Šajā tēmā aprakstīti periodiskie uzdevumi, kas ir nepieciešami kā debitoru kredīta limitu pārvaldības procesa daļa.</span><span class="sxs-lookup"><span data-stu-id="42db2-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="42db2-105">Atjaunināt riska rādītājus</span><span class="sxs-lookup"><span data-stu-id="42db2-105">Update risk scores</span></span>

<span data-ttu-id="42db2-106">Uzņēmējdarbībai attīstoties un mainoties apstākļiem, var mainīties arī attiecīgā debitora kredīta riski.</span><span class="sxs-lookup"><span data-stu-id="42db2-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="42db2-107">Lai palīdzētu uzturēt attiecīgos kredīta limitus saviem debitoriem, jums periodiski jāpārbauda katra riska rezultāta kritēriji un jāatjaunina rādītāji katram debitoram.</span><span class="sxs-lookup"><span data-stu-id="42db2-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="42db2-108">Varat atjaunināt šādus rezultātus, izmantojot lapu **Atjaunināt riska rezultātus** (**Kredīts un iekasēšana \> Periodiskie uzdevumi \> Kredīta pārvaldība \> Atjaunināt riska rezultātus**).</span><span class="sxs-lookup"><span data-stu-id="42db2-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="42db2-109">Visi lietotāja definētie aprēķini arī tiek apstrādāti.</span><span class="sxs-lookup"><span data-stu-id="42db2-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="42db2-110">**Vidējais apmaksas dienu skaits** — šis rezultāts ir vidējais dienu skaits, kad debitors veic rēķinu apmaksu.</span><span class="sxs-lookup"><span data-stu-id="42db2-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="42db2-111">**Debitors kopš** — šis rezultāts ir gadu skaits, kad debitors ir bijis jūsu organizācijas debitors.</span><span class="sxs-lookup"><span data-stu-id="42db2-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="42db2-112">**Uzņēmējdarbībā kopš** — šis rezultāts ir gadu skaits, cik debitors ir darbojies uzņēmējdarbībā.</span><span class="sxs-lookup"><span data-stu-id="42db2-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="42db2-113">Tas izmanto lauka **Uzņēmējdarbības sākums** vērtību lapā **Debitori**.</span><span class="sxs-lookup"><span data-stu-id="42db2-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="42db2-114">**Vidējais maksājuma saņemšanas laiks** — šis rezultāts ir balstīts uz debitoru parādu bilanci, pārdošanas ieņēmumiem un dienu skaitu iepriekšējā 12 mēnešu periodā.</span><span class="sxs-lookup"><span data-stu-id="42db2-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="42db2-115">**Vidējā bilance** — šis rezultāts ir balstīts uz debitoru parādu bilanci par iepriekšējo 12 mēnešu periodu.</span><span class="sxs-lookup"><span data-stu-id="42db2-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="42db2-116">**Kredīta pārvaldības grupa**, **Konta statuss** un **Valsts** — šie rezultāti izmanto informāciju no debitora.</span><span class="sxs-lookup"><span data-stu-id="42db2-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="42db2-117">Klienta bilances statistikas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="42db2-117">Update customer balance statistics</span></span>

<span data-ttu-id="42db2-118">Varat palaist procesu **Atjaunināt debitora bilances statistikas**, lai atjauninātu bilances statistiku, kas tiek rādīta lapā **Bilances statistikas pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="42db2-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="42db2-119">Šī informācija tiek izmantota, lai aprēķinātu riska rādītājus un vērtības, kas tiek rādītas kredīta statistikas papildinformācijas lapā **Debitors**.</span><span class="sxs-lookup"><span data-stu-id="42db2-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="42db2-120">Palaižot procesu, tas atjaunina debitora bilances statistiku vienam debitoram.</span><span class="sxs-lookup"><span data-stu-id="42db2-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="42db2-121">Lai iestatītu pakešuzdevumu vairāku debitoru procesa izpildei, varat izmantot lapu **Aprēķināt bilances statistiku** (**Kredīta pārvaldība \> Periodiskie uzdevumi \> Aprēķināt bilances statistiku**).</span><span class="sxs-lookup"><span data-stu-id="42db2-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]