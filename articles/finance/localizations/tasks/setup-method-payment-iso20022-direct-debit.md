---
title: Maksājumu metodes iestatīšana ISO20022 tiešajam debetam
description: Šajā procedūrā parādīts, kā iestatīt debitora maksājumu metodes ISO20022 tiešajam debetam vai kādam citam maksāšanas veidam, izmantojot elektronisko pārskatu veidošanu.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38afbc3a49d9020540a56e58ce51196b53d6a9e1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143436"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="8fa66-103">Maksājumu metodes iestatīšana ISO20022 tiešajam debetam</span><span class="sxs-lookup"><span data-stu-id="8fa66-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fa66-104">Šajā procedūrā parādīts, kā iestatīt debitora maksājumu metodes ISO20022 tiešajam debetam vai kādam citam maksāšanas veidam, izmantojot elektronisko pārskatu veidošanu.</span><span class="sxs-lookup"><span data-stu-id="8fa66-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="8fa66-105">Pirms uzdevuma pabeigšanas, ir jāiestata eksporta formāta konfigurācijas un maksājumu konti.</span><span class="sxs-lookup"><span data-stu-id="8fa66-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="8fa66-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma DEMF dati.</span><span class="sxs-lookup"><span data-stu-id="8fa66-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="8fa66-107">Šī ir trešā no piecām procedūrām, kas demonstrē debitora maksājuma procesu, izmantojot elektronisko atskaišu konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="8fa66-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="8fa66-108">Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="8fa66-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="8fa66-109">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="8fa66-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8fa66-110">Piemēram, filtrējiet pēc lauka Maksāšanas metodes, izmantojot vērtību ELECTRONIC.</span><span class="sxs-lookup"><span data-stu-id="8fa66-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="8fa66-111">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="8fa66-111">Click Edit.</span></span>
4. <span data-ttu-id="8fa66-112">Laukā Maksājumu konts norādiet vērtības DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="8fa66-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="8fa66-113">Izvērsiet sadaļu Failu formāti.</span><span class="sxs-lookup"><span data-stu-id="8fa66-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="8fa66-114">Laukā Vispārīga elektronisko pārskatu veidošana atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="8fa66-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="8fa66-115">Ievadiet vai atlasiet vērtību laukā Eksporta formāta konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="8fa66-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="8fa66-116">Sarakstā atlasiet ISO20022 tiešais debets (DE).</span><span class="sxs-lookup"><span data-stu-id="8fa66-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="8fa66-117">Ja saraksts ir tukšs, tas nozīmē, ka nav importēta un aktīva debitora maksājuma eksporta formāta konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="8fa66-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="8fa66-118">Laukā Pieprasīt pilnvarojumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="8fa66-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="8fa66-119">Atlasiet parametru Pieprasīt pilnvarojumu parametru debitora maksājumu formātiem, kuriem ir nepieciešama informāciju par pilnvarojumu maksājuma ziņojumā, piemēram, SEPA tiešais debets.</span><span class="sxs-lookup"><span data-stu-id="8fa66-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="8fa66-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8fa66-120">Click Save.</span></span>

