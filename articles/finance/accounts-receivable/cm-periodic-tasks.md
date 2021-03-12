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
ms.openlocfilehash: b41b87cd3e2e80b87318c5c771d45a4d0e5d4b85
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971707"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="9544c-103">Periodiski kredītu pārvaldības uzdevumi</span><span class="sxs-lookup"><span data-stu-id="9544c-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9544c-104">Šajā tēmā aprakstīti periodiskie uzdevumi, kas ir nepieciešami kā debitoru kredīta limitu pārvaldības procesa daļa.</span><span class="sxs-lookup"><span data-stu-id="9544c-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="9544c-105">Atjaunināt riska rādītājus</span><span class="sxs-lookup"><span data-stu-id="9544c-105">Update risk scores</span></span>

<span data-ttu-id="9544c-106">Uzņēmējdarbībai attīstoties un mainoties apstākļiem, var mainīties arī attiecīgā debitora kredīta riski.</span><span class="sxs-lookup"><span data-stu-id="9544c-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="9544c-107">Lai palīdzētu uzturēt attiecīgos kredīta limitus saviem debitoriem, jums periodiski jāpārbauda katra riska rezultāta kritēriji un jāatjaunina rādītāji katram debitoram.</span><span class="sxs-lookup"><span data-stu-id="9544c-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="9544c-108">Varat atjaunināt šādus rezultātus, izmantojot lapu **Atjaunināt riska rezultātus** (**Kredīts un iekasēšana \> Periodiskie uzdevumi \> Kredīta pārvaldība \> Atjaunināt riska rezultātus**).</span><span class="sxs-lookup"><span data-stu-id="9544c-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="9544c-109">Visi lietotāja definētie aprēķini arī tiek apstrādāti.</span><span class="sxs-lookup"><span data-stu-id="9544c-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="9544c-110">**Vidējais apmaksas dienu skaits** — šis rezultāts ir vidējais dienu skaits, kad debitors veic rēķinu apmaksu.</span><span class="sxs-lookup"><span data-stu-id="9544c-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="9544c-111">**Debitors kopš** — šis rezultāts ir gadu skaits, kad debitors ir bijis jūsu organizācijas debitors.</span><span class="sxs-lookup"><span data-stu-id="9544c-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="9544c-112">**Uzņēmējdarbībā kopš** — šis rezultāts ir gadu skaits, cik debitors ir darbojies uzņēmējdarbībā.</span><span class="sxs-lookup"><span data-stu-id="9544c-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="9544c-113">Tas izmanto lauka **Uzņēmējdarbības sākums** vērtību lapā **Debitori**.</span><span class="sxs-lookup"><span data-stu-id="9544c-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="9544c-114">**Vidējais maksājuma saņemšanas laiks** — šis rezultāts ir balstīts uz debitoru parādu bilanci, pārdošanas ieņēmumiem un dienu skaitu iepriekšējā 12 mēnešu periodā.</span><span class="sxs-lookup"><span data-stu-id="9544c-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="9544c-115">**Vidējā bilance** — šis rezultāts ir balstīts uz debitoru parādu bilanci par iepriekšējo 12 mēnešu periodu.</span><span class="sxs-lookup"><span data-stu-id="9544c-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="9544c-116">**Kredīta pārvaldības grupa**, **Konta statuss** un **Valsts** — šie rezultāti izmanto informāciju no debitora.</span><span class="sxs-lookup"><span data-stu-id="9544c-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="9544c-117">Klienta bilances statistikas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="9544c-117">Update customer balance statistics</span></span>

<span data-ttu-id="9544c-118">Varat palaist procesu **Atjaunināt debitora bilances statistikas**, lai atjauninātu bilances statistiku, kas tiek rādīta lapā **Bilances statistikas pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="9544c-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="9544c-119">Šī informācija tiek izmantota, lai aprēķinātu riska rādītājus un vērtības, kas tiek rādītas kredīta statistikas papildinformācijas lapā **Debitors**.</span><span class="sxs-lookup"><span data-stu-id="9544c-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="9544c-120">Palaižot procesu, tas atjaunina debitora bilances statistiku vienam debitoram.</span><span class="sxs-lookup"><span data-stu-id="9544c-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="9544c-121">Lai iestatītu pakešuzdevumu vairāku debitoru procesa izpildei, varat izmantot lapu **Aprēķināt bilances statistiku** (**Kredīta pārvaldība \> Periodiskie uzdevumi \> Aprēķināt bilances statistiku**).</span><span class="sxs-lookup"><span data-stu-id="9544c-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>
