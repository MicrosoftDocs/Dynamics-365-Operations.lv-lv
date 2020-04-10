---
title: Maksājuma metodes iestatīšana ISO20022 pārvietošanai kredītā
description: Šajā procedūrā parādīts, kā iestatīt kreditoru maksājumu metodes ISO20022 kredīta pārsūtīšanai vai kādam citam maksāšanas veidam, izmantojot elektronisko pārskatu veidošanu, lai ģenerētu failu.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d60502cd7f749b71cf39cc38d8a39dcbb7b108
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140121"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="eca2c-103">Maksājuma metodes iestatīšana ISO20022 pārvietošanai kredītā</span><span class="sxs-lookup"><span data-stu-id="eca2c-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eca2c-104">Šajā procedūrā parādīts, kā iestatīt kreditoru maksājumu metodes ISO20022 kredīta pārsūtīšanai vai kādam citam maksāšanas veidam, izmantojot elektronisko pārskatu veidošanu, lai ģenerētu failu.</span><span class="sxs-lookup"><span data-stu-id="eca2c-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="eca2c-105">Pirms uzdevuma pabeigšanas, ir jāiestata eksporta formāta konfigurācijas un maksājumu konti.</span><span class="sxs-lookup"><span data-stu-id="eca2c-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="eca2c-106">Šajā uzdevumā izmantots demonstrācijas datu uzņēmums DEMF.</span><span class="sxs-lookup"><span data-stu-id="eca2c-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="eca2c-107">Šī ir trešā procedūra no piecām, kas parāda kreditoru maksājumu procesu, izmantojot elektronisko pārskatu veidošanas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="eca2c-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="eca2c-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="eca2c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="eca2c-109">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="eca2c-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="eca2c-110">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="eca2c-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="eca2c-111">Piemēram, filtrējiet pēc lauka Maksāšanas metodes, izmantojot vērtību SEPA CT.</span><span class="sxs-lookup"><span data-stu-id="eca2c-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="eca2c-112">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="eca2c-112">Click Edit.</span></span>
4. <span data-ttu-id="eca2c-113">Laukā Periods atlasiet vērtību Kopā.</span><span class="sxs-lookup"><span data-stu-id="eca2c-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="eca2c-114">Laukā Maksājuma veids atlasiet Elektronisks maksājums.</span><span class="sxs-lookup"><span data-stu-id="eca2c-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="eca2c-115">Izvērsiet sadaļu Failu formāti.</span><span class="sxs-lookup"><span data-stu-id="eca2c-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="eca2c-116">Laukā Vispārīga elektronisko pārskatu veidošana atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="eca2c-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="eca2c-117">Ievadiet vai atlasiet vērtību laukā Eksporta formāta konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="eca2c-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="eca2c-118">Sarakstā atlasiet vērtību ISO20022 pārvietošana kredītā (DE).</span><span class="sxs-lookup"><span data-stu-id="eca2c-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="eca2c-119">Ja saraksts ir tukšs, tas nozīmē, ka nav importēta un aktīva kreditora maksājuma eksporta formāta konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="eca2c-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="eca2c-120">Laukā Konta tips atlasiet Banka.</span><span class="sxs-lookup"><span data-stu-id="eca2c-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="eca2c-121">Laukā Maksājumu konts norādiet vērtības DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="eca2c-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="eca2c-122">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="eca2c-122">Click Save.</span></span>

