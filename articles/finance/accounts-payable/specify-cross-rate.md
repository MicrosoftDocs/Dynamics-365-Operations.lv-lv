---
title: Norādīt starpkursu
description: Šajā tēmā ir sniegta informācija par starpkursiem programmā Microsoft Dynamics 365 Finance.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 317cad877cec4d9f02f53762af65f0b226d0aad6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979392"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="fc98a-103">Norādīt starpkursu</span><span class="sxs-lookup"><span data-stu-id="fc98a-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc98a-104">Šajā tēmā skaidrots starpkursa nolūks un tas, kā norādīt starpkursu, ja sedzat maksājumu ar rēķinu.</span><span class="sxs-lookup"><span data-stu-id="fc98a-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="fc98a-105">Izmantojiet starpkursu, kad ir spēkā visi šie kritēriji:</span><span class="sxs-lookup"><span data-stu-id="fc98a-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="fc98a-106">Jūs sedzat maksājumu ar rēķinu.</span><span class="sxs-lookup"><span data-stu-id="fc98a-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="fc98a-107">Maksājuma rinda un rēķina rinda izmanto dažādas valūtas.</span><span class="sxs-lookup"><span data-stu-id="fc98a-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="fc98a-108">Neviena no valūtām nav uzskaites valūta.</span><span class="sxs-lookup"><span data-stu-id="fc98a-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="fc98a-109">Starpkurss netiek izmantots, lai veiktu maksājuma transakcijas valūtas pārrēķināšanu maksājuma uzskaites valūtā.</span><span class="sxs-lookup"><span data-stu-id="fc98a-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="fc98a-110">Tā vietā maiņas kursi no maiņas kursu tabulām tiek izgūti, lai aprēķinātu maksājuma transakcijas valūtas summas un maksājuma uzskaites valūtas summas vērtību.</span><span class="sxs-lookup"><span data-stu-id="fc98a-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="fc98a-111">Piemēram, uzskaites valūta ir USD, rēķina valūta ir CAD, un maksājuma valūta ir EUR.</span><span class="sxs-lookup"><span data-stu-id="fc98a-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="fc98a-112">Starpkurss ļauj ievadīt maiņas kursu tieši starp CAD un EUR, neveicot konvertāciju caur USD.</span><span class="sxs-lookup"><span data-stu-id="fc98a-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="fc98a-113">Ja izvēlaties rēķinu un primāro maksājumu, varat ievadīt starpkursu rēķina rindai.</span><span class="sxs-lookup"><span data-stu-id="fc98a-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="fc98a-114">Starpkurss ir maiņas kurss starp norēķinu datuma transakciju valūtām.</span><span class="sxs-lookup"><span data-stu-id="fc98a-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="fc98a-115">Atveriet kādu no šādām lapām:</span><span class="sxs-lookup"><span data-stu-id="fc98a-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="fc98a-116">**Debitoru parādi > Vispārīgi > Debitori > Visi debitori**</span><span class="sxs-lookup"><span data-stu-id="fc98a-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="fc98a-117">**Parādi kreditoriem > Vispārīgi > Kreditori > Visi kreditori**</span><span class="sxs-lookup"><span data-stu-id="fc98a-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="fc98a-118">**Sagāde un avoti > Vispārīgi > Kreditori > Visi kreditori**</span><span class="sxs-lookup"><span data-stu-id="fc98a-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="fc98a-119">Izvēlieties klientu vai kreditoru, kurš atvērs Jūsu nokārtoto transakciju.</span><span class="sxs-lookup"><span data-stu-id="fc98a-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="fc98a-120">Debitora gadījumā saraksta lapā **Visi debitori** dodieties uz **Apkopot > Nosegt atvērtās darbības**.</span><span class="sxs-lookup"><span data-stu-id="fc98a-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="fc98a-121">Kreditora gadījumā saraksta lapā **Visi kreditori** dodieties uz **Rēķins > Nosegt atvērtās darbības**.</span><span class="sxs-lookup"><span data-stu-id="fc98a-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="fc98a-122">Izvēlieties transakciju, kas ir primārais maksājums, un pēc tam noklikšķiniet uz **Atzīmēt maksājumu**.</span><span class="sxs-lookup"><span data-stu-id="fc98a-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="fc98a-123">Tiek atzīmēta izvēles rūtiņa kolonnā **Atzīmēt**, un kolonnā **Primārais maksājums** tiek parādīta informācijas ikona.</span><span class="sxs-lookup"><span data-stu-id="fc98a-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="fc98a-124">Laukā **Starpkurss** ievadiet norēķina dienā spēkā esošo apmaiņas kursu starp rēķina valūtu un maksājuma valūtu.</span><span class="sxs-lookup"><span data-stu-id="fc98a-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
