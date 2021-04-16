---
title: ES ieraksta sertifikāti
description: Šajā rakstā ir sniegta informācija par Eiropas Savienības (ES) ierakstu sertifikātiem.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bf074f54448dd10f190263c09e731c4f4b7a61c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839776"
---
# <a name="eu-entry-certificates"></a><span data-ttu-id="3123d-103">ES ievešanas sertifikāti</span><span class="sxs-lookup"><span data-stu-id="3123d-103">EU entry certificates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3123d-104">Šajā rakstā ir sniegta informācija par Eiropas Savienības (ES) ierakstu sertifikātiem.</span><span class="sxs-lookup"><span data-stu-id="3123d-104">This article provides information about European Union (EU) entry certificates.</span></span>

<span data-ttu-id="3123d-105">Eiropas Savienības (ES) ieraksta sertifikātam varat veikt šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="3123d-105">You can complete the following tasks for a European Union (EU) entry certificate:</span></span>

-   <span data-ttu-id="3123d-106">Izveidot un izsniegt ES ieraksta sertifikātu kopā ar pavadzīmi vai debitora rēķinu par preču vai pakalpojumu piegādi uz ES valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="3123d-106">Create and issue an EU entry certificate together with a packing slip or customer invoice for the delivery of items or services to EU countries/regions.</span></span>
-   <span data-ttu-id="3123d-107">Saņemt ES ieraksta sertifikātu, ko parakstījis ES debitors.</span><span class="sxs-lookup"><span data-stu-id="3123d-107">Receive the EU entry certificate that is signed by an EU customer.</span></span>
-   <span data-ttu-id="3123d-108">Augšupielādēt parakstīto ES ieraksta sertifikātu, kas ir saņemts no debitora vai no trešās puses, kura ir atbildīga par krājumu piegādi debitoram.</span><span class="sxs-lookup"><span data-stu-id="3123d-108">Upload the signed EU entry certificate that is received either from the customer or from a third party who is responsible for delivering items to the customer.</span></span>
-   <span data-ttu-id="3123d-109">Piesaistīt augšupielādēto ES ieraksta sertifikātu debitora rēķinam.</span><span class="sxs-lookup"><span data-stu-id="3123d-109">Associate the uploaded EU entry certificate with a customer invoice.</span></span>
-   <span data-ttu-id="3123d-110">Atjaunināt augšupielādētā ES ieraksta sertifikāta statusu.</span><span class="sxs-lookup"><span data-stu-id="3123d-110">Update the status of the uploaded EU entry certificate.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3123d-111">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="3123d-111">Prerequisites</span></span>
<span data-ttu-id="3123d-112">Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darba sākšanas.</span><span class="sxs-lookup"><span data-stu-id="3123d-112">The following table shows the prerequisites that must be in place before you start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3123d-113">Kategorija</span><span class="sxs-lookup"><span data-stu-id="3123d-113">Category</span></span></th>
<th><span data-ttu-id="3123d-114">Priekšnosacījums</span><span class="sxs-lookup"><span data-stu-id="3123d-114">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3123d-115">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="3123d-115">Country/region</span></span></td>
<td><span data-ttu-id="3123d-116">Juridiskās personas primārajai adresei ir jāatrodas ES dalībvalstī.</span><span class="sxs-lookup"><span data-stu-id="3123d-116">The primary address of the legal entity must be in a EU member state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3123d-117">Saistītie iestatīšanas uzdevumi</span><span class="sxs-lookup"><span data-stu-id="3123d-117">Related set up tasks</span></span></td>
<td><ul>
<li><span data-ttu-id="3123d-118">Lapā <strong>Debitoru moduļa parametri</strong> atzīmējiet opcijas <strong>Iespējot ieraksta sertifikāta pārvaldību</strong> un <strong>Iespējot ieraksta sertifikāta izsniegšanu</strong>.</span><span class="sxs-lookup"><span data-stu-id="3123d-118">On the <strong>Accounts receivable parameters</strong> page, select the <strong>Enable entry certificate management</strong> and <strong>Enable entry certificate issuing</strong> options.</span></span></li>
<li><span data-ttu-id="3123d-119">Lapā <strong>Debitori</strong>, kopsavilkuma cilnē <strong>Rēķins un piegāde</strong> atzīmējiet opciju <strong>Nepieciešams ieraksta sertifikāts</strong> , lai norādītu, ka ES ieraksta sertifikāts šim debitoram ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="3123d-119">On the <strong>Customers</strong> page, on the <strong>Invoice and delivery</strong> FastTab, select the <strong>Entry certificate required</strong> option to indicate that an EU entry certificate is mandatory for the customer.</span></span> <span data-ttu-id="3123d-120">Atzīmējiet opciju <strong>Izsniegt ieraksta sertifikātu</strong>, lai debitoram izdotu juridiskās personas ES ieraksta sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="3123d-120">Select the <strong>Issue entry certificate</strong> option to issue an EU entry certificate of the legal entity to the customer.</span></span></li>
<li><span data-ttu-id="3123d-121">Lapā <strong>Debitoru moduļa parametri</strong> atzīmējiet numuru secības kodu atsaucei <strong>Ieraksta sertifikāts</strong>.</span><span class="sxs-lookup"><span data-stu-id="3123d-121">On the <strong>Accounts receivable parameters</strong> page, select a number sequence code for the <strong>Entry certificate</strong> reference.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3123d-122">Saistītās transakcijas</span><span class="sxs-lookup"><span data-stu-id="3123d-122">Related transactions</span></span></td>
<td><ul>
<li><span data-ttu-id="3123d-123">Izveidojiet debitora kontu.</span><span class="sxs-lookup"><span data-stu-id="3123d-123">Create a customer account.</span></span></li>
<li><span data-ttu-id="3123d-124">Izveidojiet pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="3123d-124">Create a sales order.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a><span data-ttu-id="3123d-125">ES ieraksta sertifikāta izveidošana, reģistrēšana un augšupielādēšana</span><span class="sxs-lookup"><span data-stu-id="3123d-125">Creating, registering, and uploading an EU entry certificate</span></span>
<span data-ttu-id="3123d-126">ES ieraksta sertifikātu var izveidot automātiski vai manuāli.</span><span class="sxs-lookup"><span data-stu-id="3123d-126">You can create an EU entry certificate automatically or manually.</span></span> <span data-ttu-id="3123d-127">ES ieraksta sertifikāts tiek izveidots un izdrukāts automātiski, kad pavadzīmi vai rēķinu debitoram grāmatojat, izmantojot lapu **Pavadzīmes grāmatošana** vai **Rēķina grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="3123d-127">An EU entry certificate is created and printed automatically when you post a packing slip or invoice for a customer by using the **Packing slip posting** page or the **Posting invoice** page.</span></span> <span data-ttu-id="3123d-128">Lai ES ieraksta sertifikātu izveidotu vai atkārtoti drukātu manuāli, izmantojiet lapu **Rēķinu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="3123d-128">To manually create or reprint an EU entry certificate for a customer invoice, use the **Invoice journal** page.</span></span> <span data-ttu-id="3123d-129">Turklāt varat izmantot lapu **Ierakstu sertifikātu žurnāls**, lai ievadītu detalizētu informāciju par ES ieraksta sertifikātu, ko izsniedza trešā puse.</span><span class="sxs-lookup"><span data-stu-id="3123d-129">Additionally, you can use the **Entry certificate journal** page to enter details about an EU entry certificate that is issued by a third party.</span></span>

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a><span data-ttu-id="3123d-130">ES ieraksta sertifikātu automātiska vai manuāla izveidošana</span><span class="sxs-lookup"><span data-stu-id="3123d-130">Creating an EU entry certificate automatically or manually</span></span>

<span data-ttu-id="3123d-131">ES ieraksta sertifikātu varat izveidot automātiski, izmantojot pavadzīmi lapā **Visi pārdošanas pasūtījumi** vai izmantojot rēķinu lapā **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="3123d-131">You can create an EU entry certificate automatically by using a packing slip on the **All sales orders** page or by using an invoice on the **Sales order** page.</span></span> <span data-ttu-id="3123d-132">Lai ES ieraksta sertifikātu izveidotu manuāli, varat lietot rēķinu lapā **Rēķinu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="3123d-132">To manually create an EU entry certificate, you can use an invoice on the **Invoice journal** page.</span></span> <span data-ttu-id="3123d-133">Taču pirms ES ieraksta sertifikāta manuālas izveidošanas ir jāmaina rēķina sertifikācijas statuss.</span><span class="sxs-lookup"><span data-stu-id="3123d-133">However, you must change the certification status of the invoice before you manually create an EU entry certificate.</span></span>

### <a name="registering-an-eu-entry-certificate"></a><span data-ttu-id="3123d-134">ES ieraksta sertifikāta reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="3123d-134">Registering an EU entry certificate</span></span>

<span data-ttu-id="3123d-135">Ja ir nepieciešama reģistrēšana, varat izmantot lapu **Ierakstu sertifikātu žurnāls**, lai reģistrētu ES ieraksta sertifikātu, ko izsniedza trešā puse.</span><span class="sxs-lookup"><span data-stu-id="3123d-135">If registration is required, you can use the **Entry certificate journal** page to register an EU entry certificate that is issued by a third party.</span></span>

### <a name="uploading-a-received-eu-entry-certificate"></a><span data-ttu-id="3123d-136">Saņemta ES ieraksta sertifikāta augšupielādēšana</span><span class="sxs-lookup"><span data-stu-id="3123d-136">Uploading a received EU entry certificate</span></span>

<span data-ttu-id="3123d-137">Izmantojiet lapu **Pielikumi**, lai augšupielādētu saņemtu ES ieraksta sertifikātu, ko parakstījis ES debitors.</span><span class="sxs-lookup"><span data-stu-id="3123d-137">Use the **Attachments** page to upload a received EU entry certificate that is signed by an EU customer.</span></span> <span data-ttu-id="3123d-138">Kad sertifikāts ir augšupielādēts, varat to saistīt ar rēķinu kā pierādījumu, ka krājumi tika piegādāti.</span><span class="sxs-lookup"><span data-stu-id="3123d-138">After the certificate is uploaded, you can associate it with an invoice as proof that the items were delivered.</span></span> <span data-ttu-id="3123d-139">Šāds pierādījums ir nepieciešams, ja jums ir jāizsniedz rēķins, kas neietver pievienotās vērtības nodokli (PVN), un tas tiek izmantots arī auditēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="3123d-139">This proof is required if you must issue an invoice that doesn't include value-added tax (VAT), and it's also used during auditing.</span></span>

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a><span data-ttu-id="3123d-140">Nav obligāti: sertifikāta statusa atjaunināšana un rēķina statusa drukāšana</span><span class="sxs-lookup"><span data-stu-id="3123d-140">Optional: Updating the certification status and printing status of an invoice</span></span>

<span data-ttu-id="3123d-141">Ieraksta sertifikācijas statusu un debitora rēķina drukāšanas statusu varat atjaunināt, izmantojot lapu **Rēķinu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="3123d-141">You can update the entry certification status and printing status of a customer invoice by using the **Invoice journal** page.</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="3123d-142">Tehniskā informācija sistēmas administratoriem</span><span class="sxs-lookup"><span data-stu-id="3123d-142">Technical information for system administrators</span></span>
<span data-ttu-id="3123d-143">Ja nevarat piekļūt lapām, kas tiek izmantotas šī uzdevuma izpildīšanai, sazinieties ar sistēmas administratoru un sniedziet nākamajā tabulā redzamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="3123d-143">If you don't have access to the pages that are used to complete this task, contact your system administrator, and provide the information that is shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3123d-144">Kategorija</span><span class="sxs-lookup"><span data-stu-id="3123d-144">Category</span></span></th>
<th><span data-ttu-id="3123d-145">Priekšnosacījums</span><span class="sxs-lookup"><span data-stu-id="3123d-145">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3123d-146">Drošības lomas un pienākumi</span><span class="sxs-lookup"><span data-stu-id="3123d-146">Security roles and duties</span></span></td>
<td><span data-ttu-id="3123d-147">Lai iestatītu un izveidotu ES ieraksta sertifikātu krājumiem vai pakalpojumiem, jums ir jābūt tādas drošības lomas dalībniekam, kurā ietverti tālāk norādītie pienākumi.</span><span class="sxs-lookup"><span data-stu-id="3123d-147">To set up and create EU entry certificates for items or services, you must be a member of a security role that includes the following duties:</span></span>
<ul>
<li><span data-ttu-id="3123d-148"><strong>Debitoru parādu darbinieks</strong> (CustInvoiceAccountsReceivableClerk)</span><span class="sxs-lookup"><span data-stu-id="3123d-148"><strong>Accounts receivable clerk</strong> (CustInvoiceAccountsReceivableClerk)</span></span></li>
<li><span data-ttu-id="3123d-149"><strong>Klientu apkalpošanas pārstāvis</strong> (TradeCustomerServiceRepresentative)</span><span class="sxs-lookup"><span data-stu-id="3123d-149"><strong>Customer service representative</strong> (TradeCustomerServiceRepresentative)</span></span></li>
<li><span data-ttu-id="3123d-150"><strong>Pārdošanas darbinieks</strong> (TradeSalesClerk)</span><span class="sxs-lookup"><span data-stu-id="3123d-150"><strong>Sales clerk</strong> (TradeSalesClerk)</span></span></li>
<li><span data-ttu-id="3123d-151"><strong>Nosūtīšanas darbinieks</strong> (InventShippingClerk)</span><span class="sxs-lookup"><span data-stu-id="3123d-151"><strong>Shipping clerk</strong> (InventShippingClerk)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]