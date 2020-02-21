---
title: Pakāpeniskas plūsmas pasūtījumu izveide mazumtirdzniecības veikala transakcijām
description: Šajā tēmā ir aprakstīta pakāpeniskas plūsmas pasūtījumu izveide mazumtirdzniecības veikala transakcijām risinājumā Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3f691017ad06d3416e4ba0e86d7a0bc207aba5bd
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004278"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="87596-103">Pakāpeniskas plūsmas pasūtījumu izveide mazumtirdzniecības veikala transakcijām (publisks priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="87596-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="87596-104">Dynamics 365 Retail versijā 10.0.4 un vecākās versijās pārskatu grāmatošana ir dienas beigās veicama operācija. Dienas beigās visas transakcijas tiek grāmatotas grāmatās.</span><span class="sxs-lookup"><span data-stu-id="87596-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="87596-105">Apjomīgas transakcijas ir jāapstrādā ierobežotā laika posmā, kas dažkārt rada ievērojamu noslodzi un pārskatu grāmatošanas kļūmes.</span><span class="sxs-lookup"><span data-stu-id="87596-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="87596-106">Mazumtirgotāji nevar arī atpazīt dienas ieņēmumus un maksājumus savās grāmatās.</span><span class="sxs-lookup"><span data-stu-id="87596-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="87596-107">Izmantojot pakāpeniskas plūsmas pasūtījumu izveides publisko priekšskatījumu, kas ieviests Retail versijā 10.0.5, transakcijas tiek apstrādātas visas dienas garumā, un dienas beigās tiek veikta tikai norēķinu un citu naudas pārvaldības transakciju finanšu saskaņošana.</span><span class="sxs-lookup"><span data-stu-id="87596-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="87596-108">Šī funkcionalitāte sadala pārdošanas pasūtījumu, rēķinu un maksājumu izveides noslodzi visas dienas garumā, nodrošinot labāku veiktspēju un spēju atpazīt ieņēmumus un maksājumus grāmatās gandrīz reālajā laikā.</span><span class="sxs-lookup"><span data-stu-id="87596-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="87596-109">Pakāpeniskas plūsmas grāmatošanas izmantošana</span><span class="sxs-lookup"><span data-stu-id="87596-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="87596-110">Lai iespējotu transakciju pakāpeniskas plūsmas grāmatošanu, dodieties uz **Sistēmas administrēšana > Iestatīt > Licences konfigurācija** un atspējojiet atslēgu **Pārskati**.</span><span class="sxs-lookup"><span data-stu-id="87596-110">To enable trickle feed-based posting of transactions, go to **System administration > Set up > License configuration** and disable the the **Statements** key.</span></span>

2. <span data-ttu-id="87596-111">Tajā pašā lapā iespējojiet licences atslēgu **Pārskati (pakāpeniska plūsma) — priekšskatījums**.</span><span class="sxs-lookup"><span data-stu-id="87596-111">On the same page, enable the **Statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="87596-112">Iespējojot šo atslēgu, pārliecinieties, vai nav pārskatu, kuri gaida grāmatošanu.</span><span class="sxs-lookup"><span data-stu-id="87596-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

    > [!Important]
    > <span data-ttu-id="87596-113">Pirms licences atslēgas **Pārskati (pakāpeniska plūsma) — priekšskatījums** iespējošanas pārliecinieties, vai nav pārskatu, kuri gaida grāmatošanu.</span><span class="sxs-lookup"><span data-stu-id="87596-113">Before you enable the **Statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="87596-114">Pašreizējais pārskata dokuments tiks sadalīts divos dažādos veidos: transakciju pārskats un finanšu pārskats.</span><span class="sxs-lookup"><span data-stu-id="87596-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="87596-115">Transakciju pārskatā tiks iekļautas visas negrāmatotās un apstiprinātās transakcijas, kā arī tiks izveidoti pārdošanas pasūtījumi, pārdošanas rēķini, maksājumu un atlaižu žurnāli un ieņēmumu un izdevumu transakcijas atbilstoši jūsu konfigurētam ritmam.</span><span class="sxs-lookup"><span data-stu-id="87596-115">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="87596-116">Šim procesam jākonfigurē bieža izpilde, lai dokumenti tiktu izveidoti, kad transakcijas tiek augšupielādētas komponentā Headquarters, izmantojot P-darbu.</span><span class="sxs-lookup"><span data-stu-id="87596-116">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="87596-117">Ar transakciju pārskatu, kurā jau ir izveidoti pārdošanas pasūtījumi un pārdošanas rēķini, nav nepieciešamības konfigurēt pakešuzdevumu **Grāmatot krājumus**.</span><span class="sxs-lookup"><span data-stu-id="87596-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="87596-118">Tomēr to joprojām var izmantot specifiskām uzņēmējdarbības prasībām.</span><span class="sxs-lookup"><span data-stu-id="87596-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="87596-119">Finanšu pārskats ir izstrādāts izveidei dienas beigās, un tas atbalsta tikai slēgšanas metodi **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="87596-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="87596-120">Šis pārskats būs ierobežots līdz finanšu saskaņošanai, un tiks izveidoti tikai žurnāli attiecībā uz starpību starp dažādu norēķinu aprēķināto summu un transakcijas summu kopā ar žurnāliem attiecībā uz citām naudas pārvaldības transakcijām.</span><span class="sxs-lookup"><span data-stu-id="87596-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="87596-121">Lai aprēķinātu transakciju pārskatu, noklikšķiniet uz **Mazumtirdzniecība un tirdzniecība > Mazumtirdzniecības un tirdzniecības IT > POS grāmatošana > Aprēķināt transakciju pārskatus partijā**.</span><span class="sxs-lookup"><span data-stu-id="87596-121">To calculate the transactional statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="87596-122">Lai grāmatotu transakciju pārskatus partijā, noklikšķiniet uz **Mazumtirdzniecība un tirdzniecība > Mazumtirdzniecības un tirdzniecības IT > POS grāmatošana > Grāmatot transakciju pārskatus partijā**.</span><span class="sxs-lookup"><span data-stu-id="87596-122">To post the transactional statement statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="87596-123">Lai aprēķinātu finanšu pārskatu, noklikšķiniet uz **Mazumtirdzniecība un tirdzniecība > Mazumtirdzniecības un tirdzniecības IT > POS grāmatošana > Aprēķināt finanšu pārskatus partijā**.</span><span class="sxs-lookup"><span data-stu-id="87596-123">To calculate the financial statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="87596-124">Lai grāmatotu finanšu pārskatus partijā, noklikšķiniet uz **Mazumtirdzniecība un tirdzniecība > Mazumtirdzniecības un tirdzniecības IT > POS grāmatošana > Grāmatot finanšu pārskatus partijā**.</span><span class="sxs-lookup"><span data-stu-id="87596-124">To post the financial statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="87596-125">Izvēlnes elementi **Mazumtirdzniecība un tirdzniecība > Mazumtirdzniecības un tirdzniecības IT > POS grāmatošana > Aprēķināt pārskatus partijā** un **Mazumtirdzniecība un tirdzniecība > Mazumtirdzniecības un tirdzniecības IT > POS grāmatošana > Grāmatot pārskatus partijā** ir noņemti ar šo jauno līdzekli.</span><span class="sxs-lookup"><span data-stu-id="87596-125">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="87596-126">Transakciju un finanšu pārskatu veidus var izveidot arī manuāli.</span><span class="sxs-lookup"><span data-stu-id="87596-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="87596-127">Dodieties uz **Mazumtirdzniecība un tirdzniecība > Kanāli > Veikali** un noklikšķiniet uz **Pārskati**.</span><span class="sxs-lookup"><span data-stu-id="87596-127">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="87596-128">Noklikšķiniet uz **Jauns** un pēc tam izvēlieties pārskata veidu, ko vēlaties izveidot.</span><span class="sxs-lookup"><span data-stu-id="87596-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="87596-129">Laukos lapā **Pārskati** un darbībās zem lapas **Pārskatu grupa** tiks rādīti atbilstošie dati un darbības, pamatojoties uz atlasīto pārskata veidu.</span><span class="sxs-lookup"><span data-stu-id="87596-129">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
