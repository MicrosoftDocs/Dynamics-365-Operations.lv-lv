---
title: "Skatīt nosegšanas transakcijas Austrumeiropai"
description: "Šajā tēmā ir sniegta informācija par lapu Nosegšanas transakcijas debitoriem un kreditoriem."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustVendTransPostingLog_RU
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 270544
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5ac75d1900a428777374dcc9d7eea10ce4d15b1e
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="view-transactions-on-settlement-for-eastern-europe"></a><span data-ttu-id="a9f48-103">Skatīt nosegšanas transakcijas Austrumeiropai</span><span class="sxs-lookup"><span data-stu-id="a9f48-103">View transactions on settlement for Eastern Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a9f48-104">Šajā tēmā ir sniegta informācija par lapu Nosegšanas transakcijas debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="a9f48-104">This topic provides information about the Transactions on settlement page for customers and vendors.</span></span>

<span data-ttu-id="a9f48-105">Izmantojiet lapu **Nosegšanas transakcijas**, lai skatītu informāciju par kompleksām nosegšanas transakcijām kādam debitoram vai kreditoram.</span><span class="sxs-lookup"><span data-stu-id="a9f48-105">Use the **Transactions on settlement** page to view information about complex settlement transactions for a customer or a vendor.</span></span> <span data-ttu-id="a9f48-106">Šis līdzeklis ir pieejams tikai juridiskām personām, kuru primārā adrese ir Lietuvā, Latvijā, Igaunijā, Čehijā, Ungārijā vai Polijā.</span><span class="sxs-lookup"><span data-stu-id="a9f48-106">This feature is available only for legal entities that have their primary address in Lithuania, Latvia, Estonia, Czech Republic, Hungary, or Poland.</span></span> <span data-ttu-id="a9f48-107">Lapa **Nosegšanas transakcijas** ir atrodama tālāk norādītajās vietās.</span><span class="sxs-lookup"><span data-stu-id="a9f48-107">You can find the **Transactions on settlement** page at the following locations:</span></span>

-   <span data-ttu-id="a9f48-108">**Parādi kreditoriem** &gt; **Kreditori** &gt; **Visi kreditori**.</span><span class="sxs-lookup"><span data-stu-id="a9f48-108">**Accounts payable** &gt; **Vendors** &gt; **All vendors**.</span></span> <span data-ttu-id="a9f48-109">Darbības rūts cilnē **Kreditors** noklikšķiniet uz **Transakcijas** &gt; **Transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="a9f48-109">On the Action Pane, on the **Vendor** tab, click **Transactions** &gt; **Transactions**.</span></span> <span data-ttu-id="a9f48-110">Lapā **Kreditoru transakcijas** atlasiet kādu transakciju un pēc tam noklikšķiniet uz **Nosegšanas transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="a9f48-110">On the **Vendor transactions** page, select a transaction, and then click **Transactions on settlement**.</span></span>
-   <span data-ttu-id="a9f48-111">**Debitoru parādi** &gt; **Debitori** &gt; **Visi debitori**.</span><span class="sxs-lookup"><span data-stu-id="a9f48-111">**Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span> <span data-ttu-id="a9f48-112">Darbības rūts cilnē **Debitors** noklikšķiniet uz **Transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="a9f48-112">On the Action Pane, on the **Customer** tab, click **Transactions**.</span></span> <span data-ttu-id="a9f48-113">Lapā **Debitoru transakcijas** atlasiet kādu transakciju un pēc tam noklikšķiniet uz **Nosegšanas transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="a9f48-113">On the **Customer transactions** page, select a transaction, and then click **Transactions on settlement**.</span></span>

<span data-ttu-id="a9f48-114">Ar nosegšanu saistītā informācija tiek tverta un to var parādīt lapā **Nosegšanas transakcijas** attiecībā uz transakcijām, kuras tika izveidotas tālāk uzskaitītajos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="a9f48-114">Settlement-related information is captured and can be shown on the **Transactions on settlement** page for transactions that were created in the following scenarios:</span></span>

-   <span data-ttu-id="a9f48-115">**Valūtas pārrēķins** — rēķina un maksājuma nosegšana ģenerē realizētu vai nerealizētu valūtas maiņas kursa starpību.</span><span class="sxs-lookup"><span data-stu-id="a9f48-115">**Exchange adjustment** – Settlement of an invoice and a payment generates a realized or unrealized exchange rate difference.</span></span>
-   <span data-ttu-id="a9f48-116">**Grāmatošanas metodes izmaiņas** — tiek nosegti divi ieraksti, piemēram, rēķins un kredītrēķins, kuriem ir dažādas grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="a9f48-116">**Posting profile change** – Two entries, such as an invoice and a credit memo, that have different posting profiles are settled.</span></span>
-   <span data-ttu-id="a9f48-117">Priekšapmaksa tiek pārveidota par maksājumu, vai maksājums tiek pārveidots par priekšapmaksu.</span><span class="sxs-lookup"><span data-stu-id="a9f48-117">A prepayment is converted to a payment, or a payment is converted to a prepayment.</span></span>
-   <span data-ttu-id="a9f48-118">**Termiņatlaide** — rēķins tiek nosegts ar maksājumu, no kura ir atņemta atlaides summa.</span><span class="sxs-lookup"><span data-stu-id="a9f48-118">**Cash discount** – An invoice is settled with a payment that a discount amount has been deducted from.</span></span>
-   <span data-ttu-id="a9f48-119">**Sīknaudas starpība** — rēķins tiek nosegts ar maksājumu, kura summa nedaudz atšķiras no rēķina summas.</span><span class="sxs-lookup"><span data-stu-id="a9f48-119">**Penny difference** – An invoice is settled with a payment that has a slightly different amount than the invoice.</span></span>
-   <span data-ttu-id="a9f48-120">**Nosacījuma nodokļu grāmatošana** — rēķins tiek nosegts ar maksājumu, kuram tiek lietots nosacījuma nodoklis.</span><span class="sxs-lookup"><span data-stu-id="a9f48-120">**Conditional tax posting** – An invoice is settled with a payment that conditional tax has been applied to.</span></span>
-   <span data-ttu-id="a9f48-121">**Starpuzņēmumu nosegšana** — lai rēķinu nosegtu ar maksājumu no kādas organizācijas, tiek lietota starpuzņēmumu funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="a9f48-121">**Cross-company settlement** – Intercompany functionality is used to settle an invoice with a payment from an organization.</span></span>





