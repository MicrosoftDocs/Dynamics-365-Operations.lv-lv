---
title: Pārskats par elektroniskajiem parakstiem
description: Šajā rakstā sniegts apskats par elektroniskajiem parakstiem un ir aprakstīts, kā tos var izmantot.
author: maertenm
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 547ab10dabb6bb3f8ea41d0f80db227fc24411a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747715"
---
# <a name="electronic-signatures-overview"></a><span data-ttu-id="5892e-103">Elektronisko parakstu pārskats</span><span class="sxs-lookup"><span data-stu-id="5892e-103">Electronic signatures overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5892e-104">Šajā rakstā sniegts apskats par elektroniskajiem parakstiem un ir aprakstīts, kā tos var izmantot.</span><span class="sxs-lookup"><span data-stu-id="5892e-104">This article provides an overview of electronic signatures and describes how they can be used.</span></span>

## <a name="what-is-an-electronic-signature"></a><span data-ttu-id="5892e-105">Kas ir elektronisks paraksts?</span><span class="sxs-lookup"><span data-stu-id="5892e-105">What is an electronic signature?</span></span>

<span data-ttu-id="5892e-106">Elektroniskais paraksts apstiprina personas identitāti, kas gatavojas sākt vai apstiprināt skaitļošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="5892e-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="5892e-107">Dažās nozarēs elektroniskais paraksts ir tikpat juridiski saistošs kā ar roku veikts paraksts.</span><span class="sxs-lookup"><span data-stu-id="5892e-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span>

<span data-ttu-id="5892e-108">Vairākās regulētas nozarēs, piemēram, farmācijas, pārtikas un dzērienu un aviācijas un aizsardzības nozarēs, elektronisko parakstu izmantošana ir normatīva prasība.</span><span class="sxs-lookup"><span data-stu-id="5892e-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="5892e-109">Tie ir arī nepieciešami, lai izpildītu ASV Pārtikas un zāļu pārvaldes (FDA) izdotā standarta 21 CFR 11. daļas normatīvās prasības.</span><span class="sxs-lookup"><span data-stu-id="5892e-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span>

> [!NOTE]
> <span data-ttu-id="5892e-110">Elektroniskais paraksts pats par sevi nav tas pats, kas ciparparaksts.</span><span class="sxs-lookup"><span data-stu-id="5892e-110">An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="5892e-111">Elektroniskais paraksts ir vienkārši ar roku rakstīta paraksta aizstājējs, bet ciparparaksts sniedz papildu drošības pasākumus.</span><span class="sxs-lookup"><span data-stu-id="5892e-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="5892e-112">Ciparparaksts var palīdzēt identificēt, vai cits lietotājs vai process ir darbojies ar datiem.</span><span class="sxs-lookup"><span data-stu-id="5892e-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="5892e-113">Ciparparakstu var arī verificēt, un šo verifikāciju nevar atspēkot datu parakstīšanai izmantotā sertifikāta īpašnieks.</span><span class="sxs-lookup"><span data-stu-id="5892e-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="5892e-114">Kā tālāk aprakstīts, elektroniskajiem parakstiem ir iebūvēta ciparparaksta funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="5892e-114">As described below, electronic signatures have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures"></a><span data-ttu-id="5892e-115">Elektroniskie paraksti</span><span class="sxs-lookup"><span data-stu-id="5892e-115">Electronic signatures</span></span>

<span data-ttu-id="5892e-116">Būtiskiem biznesa procesiem varat izmantot elektroniskos parakstus.</span><span class="sxs-lookup"><span data-stu-id="5892e-116">You can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="5892e-117">Dažiem procesiem ir iebūvētas elektronisko parakstu iespējas.</span><span class="sxs-lookup"><span data-stu-id="5892e-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="5892e-118">Varat arī izveidot pielāgotas parakstu prasības jebkurai datu bāzes tabulai un laukam.</span><span class="sxs-lookup"><span data-stu-id="5892e-118">You can also create custom signature requirements for any database table and field.</span></span>

<span data-ttu-id="5892e-119">Elektroniskajiem parakstiem ir iebūvēta ciparparaksta funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="5892e-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="5892e-120">Katram lietotājam, kas paraksta dokumentus, ir jāiegūst derīgs šifrēšanas sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="5892e-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="5892e-121">Kad dokuments ir parakstīts, tiek validēta ar šo sertifikātu saistītā privātā atslēga.</span><span class="sxs-lookup"><span data-stu-id="5892e-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="5892e-122">Elektroniskā paraksta informācija tiek reģistrēta žurnālā, lai sniegtu auditācijas pierakstus.</span><span class="sxs-lookup"><span data-stu-id="5892e-122">Electronic signature information is recorded in a log to provide an audit trail.</span></span> <span data-ttu-id="5892e-123">Lai iestatītu elektroniskos parakstus, skatiet rakstu [Iestatīt elektroniskos parakstus](tasks/set-up-electronic-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="5892e-123">To set up electronic signatures, see [Set up electronic signatures](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="5892e-124">Lietotāji, kuriem ir nepieciešama piekļuve elektroniskajiem parakstiem</span><span class="sxs-lookup"><span data-stu-id="5892e-124">Users who require access to electronic signatures</span></span>

<span data-ttu-id="5892e-125">Elektroniskajiem parakstiem drošības piekļuve parasti ir nepieciešama trīs veidu lietotājiem: elektronisko parakstu administratoriem, parakstītājiem un elektronisko parakstu auditoriem.</span><span class="sxs-lookup"><span data-stu-id="5892e-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="5892e-126">Elektronisko parakstu administrators</span><span class="sxs-lookup"><span data-stu-id="5892e-126">Electronic signature administrator</span></span>

<span data-ttu-id="5892e-127">Elektronisko parakstu administrators iestata parakstu prasības, vispārējos parametrus un apstiprinātājus, kā arī saņem brīdinājumus, kad parakstus neizdodas verificēt.</span><span class="sxs-lookup"><span data-stu-id="5892e-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="5892e-128">Lietotājam, kuram ir piešķirta drošības loma **Informācijas tehnoloģiju vadītājs**, pēc noklusējuma ir atļauts administrēt elektroniskos parakstus.</span><span class="sxs-lookup"><span data-stu-id="5892e-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="5892e-129">Parakstītājs</span><span class="sxs-lookup"><span data-stu-id="5892e-129">Signer</span></span>

<span data-ttu-id="5892e-130">Parakstītājs sniedz elektroniskos parakstus dokumentiem un procesiem, kam ir nepieciešami paraksti.</span><span class="sxs-lookup"><span data-stu-id="5892e-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="5892e-131">Lietotājam, kuram ir piešķirta drošības loma **Sistēmas lietotājs**, pēc noklusējuma ir atļauts elektroniski parakstīt dokumentus.</span><span class="sxs-lookup"><span data-stu-id="5892e-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span>

> [!NOTE]
> <span data-ttu-id="5892e-132">Parakstītājam var būt nepieciešamas papildu atļaujas, lai tiktu nodrošināta piekļuve datiem, kas ir saistīti ar parakstāmo dokumentu vai procesu.</span><span class="sxs-lookup"><span data-stu-id="5892e-132">The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="5892e-133">Lietotājam, kas veic izmaiņas datos un kam pēc tam ir jāparakstās par šīm izmaiņām, ir nepieciešama atļauja mainīt šos datus.</span><span class="sxs-lookup"><span data-stu-id="5892e-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="5892e-134">Lietotājam, kurš parakstās cita lietotāja vārdā, var nebūt nepieciešama piekļuve datiem.</span><span class="sxs-lookup"><span data-stu-id="5892e-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="5892e-135">Šāda lietotāja piemērs ir supervizors, kas parakstās par darbinieka veiktajām izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="5892e-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="5892e-136">Elektronisko parakstu auditors</span><span class="sxs-lookup"><span data-stu-id="5892e-136">Electronic signature auditor</span></span>

<span data-ttu-id="5892e-137">Elektronisko parakstu auditors pārskata datu bāzes žurnālu un parakstu pārskata žurnālu, kas ir pieejams no datu bāzes žurnāla.</span><span class="sxs-lookup"><span data-stu-id="5892e-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="5892e-138">Lietotājam, kuram ir piešķirta drošības loma **Informācijas tehnoloģiju vadītājs**, pēc noklusējuma ir atļauts auditēt elektroniskos parakstus.</span><span class="sxs-lookup"><span data-stu-id="5892e-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span>

<span data-ttu-id="5892e-139">Ja izmantojat citu lomu, nevis **Informācijas tehnoloģiju vadītā**, pārliecinieties, ka lomai ir piešķirtas tālāk norādītās privilēģijas.</span><span class="sxs-lookup"><span data-stu-id="5892e-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

- <span data-ttu-id="5892e-140">Skatīt elektroniskā paraksta kļūmes</span><span class="sxs-lookup"><span data-stu-id="5892e-140">View electronic signature failures</span></span>
- <span data-ttu-id="5892e-141">Skatīt datu bāzes žurnālu</span><span class="sxs-lookup"><span data-stu-id="5892e-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="5892e-142">Elektroniska dokumentu parakstīšana</span><span class="sxs-lookup"><span data-stu-id="5892e-142">Signing documents electronically</span></span>

### <a name="get-a-certificate"></a><span data-ttu-id="5892e-143">Sertifikāta iegūšana</span><span class="sxs-lookup"><span data-stu-id="5892e-143">Get a certificate</span></span>

<span data-ttu-id="5892e-144">Pirms dokumentus parakstāt elektroniski, jums ir jāpieprasa sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="5892e-144">Before you sign documents electronically, you must request a certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="5892e-145">Microsoft SQL Server līdzekļi tiek izmantoti, lai izveidotu sertifikātus un iespējotu elektronisko parakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="5892e-145">Microsoft SQL Server features are used to create certificates and enable electronic signing.</span></span> <span data-ttu-id="5892e-146">Nav nepieciešami nekādi papildu sertifikāti vai publisku atslēgu infrastruktūra (PKI).</span><span class="sxs-lookup"><span data-stu-id="5892e-146">No additional certificate or public key infrastructure (PKI) is required.</span></span>

<span data-ttu-id="5892e-147">Kad pieprasāt sertifikātu, jums izveido publisko atslēgu un privāto atslēgu.</span><span class="sxs-lookup"><span data-stu-id="5892e-147">When you request a certificate, a public key and a private key are created for you.</span></span> <span data-ttu-id="5892e-148">Privātā atslēga ir šifrēta, izmantojot tikai jums zināmu paroli.</span><span class="sxs-lookup"><span data-stu-id="5892e-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="5892e-149">Kad parakstāt dokumentu elektroniski, jūsu identitāti verificē, kad ievadāt paroli.</span><span class="sxs-lookup"><span data-stu-id="5892e-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span>

<span data-ttu-id="5892e-150">Lai pieprasītu sertifikātu, lapas **Opcijas** cilnē **Konti** noklikšķiniet uz **Iegūt sertifikātu**.</span><span class="sxs-lookup"><span data-stu-id="5892e-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span>

<span data-ttu-id="5892e-151">Jums ir jāievada un jāapstiprina parole, ko izmantosiet parakstīšanai.</span><span class="sxs-lookup"><span data-stu-id="5892e-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="5892e-152">Šo paroli izmanto, lai aizsargātu jūsu privāto atslēgu un autorizētu jūsu sertifikāta lietošanu.</span><span class="sxs-lookup"><span data-stu-id="5892e-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="5892e-153">Šī parole netiek glabāta datu bāzē, un tā nav pieejama nevienam citam, pat ne administratoram.</span><span class="sxs-lookup"><span data-stu-id="5892e-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the administrator.</span></span>

<span data-ttu-id="5892e-154">Ja aizmirstat ar savu sertifikātu saistīto paroli, šo sertifikātu ir nepieciešams atiestatīt.</span><span class="sxs-lookup"><span data-stu-id="5892e-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="5892e-155">Ja atiestatāt šo sertifikātu, jūs neietekmējat ar iepriekšējo sertifikātu parakstītos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="5892e-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="5892e-156">Lai atiestatītu sertifikātu, lapā **Opcijas** noklikšķiniet uz **Atiestatīt sertifikātu**.</span><span class="sxs-lookup"><span data-stu-id="5892e-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="5892e-157">Elektroniska dokumentu parakstīšana</span><span class="sxs-lookup"><span data-stu-id="5892e-157">Sign a document electronically</span></span>

<span data-ttu-id="5892e-158">Lapa **Parakstīt dokumentu** tiek parādīta, kad veicat izmaiņas, kurām nepieciešams elektroniskais paraksts.</span><span class="sxs-lookup"><span data-stu-id="5892e-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1. <span data-ttu-id="5892e-159">Lapā **Parakstīt dokumentu** noklikšķiniet uz cilnes **Dokuments**, lai pārskatītu dokumentā veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="5892e-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2. <span data-ttu-id="5892e-160">Cilnē **Paraksts** atlasiet pamatojuma kodu.</span><span class="sxs-lookup"><span data-stu-id="5892e-160">On the **Signature** tab, select a reason code.</span></span>
3. <span data-ttu-id="5892e-161">Ievadiet komentāru, ja ir nepieciešami kādi komentāri.</span><span class="sxs-lookup"><span data-stu-id="5892e-161">Enter a comment, if a comment is required.</span></span>
4. <span data-ttu-id="5892e-162">Ja jūsu lietotāja ID netiek rādīts laukā **Parakstītājs**, tad atlasiet to sarakstā.</span><span class="sxs-lookup"><span data-stu-id="5892e-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5. <span data-ttu-id="5892e-163">Ievadiet savu atrašanās vietu, ja šāda informācija ir nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="5892e-163">Enter your location, if this information is required.</span></span>
6. <span data-ttu-id="5892e-164">Noklikšķiniet uz **OK**.</span><span class="sxs-lookup"><span data-stu-id="5892e-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="5892e-165">Parakstīties par cita lietotāja veiktām izmaiņām</span><span class="sxs-lookup"><span data-stu-id="5892e-165">Sign for another user's changes</span></span>

<span data-ttu-id="5892e-166">Iespējams, reizēm jūs vēlaties, lai lietotājs parakstītos par cita lietotāja veiktajām izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="5892e-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="5892e-167">Piemēram, supervizoram varētu būt jāparakstās par izmaiņām, ko kāds darbinieks ir veicis materiālu komplektā (MK).</span><span class="sxs-lookup"><span data-stu-id="5892e-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="5892e-168">Izmantojiet šo procedūru, lai norīkotu lietotāju kā parakstītāju citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="5892e-168">Use this procedure to designate a user as a signer for another user.</span></span>

> [!NOTE]
> <span data-ttu-id="5892e-169">Kad kāds lietotājs parakstās par cita lietotāja veiktajām izmaiņām, paraksts ir jāsniedz izmaiņas veikušā lietotāja darbstacijā.</span><span class="sxs-lookup"><span data-stu-id="5892e-169">When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="5892e-170">Lietotājs nevar saglabāt izmaiņas, pirms ir sniegts paraksts.</span><span class="sxs-lookup"><span data-stu-id="5892e-170">The user can't save the change until the signature has been provided.</span></span>

<span data-ttu-id="5892e-171">Lai norādītu apstiprinātājus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="5892e-171">To designate approvers, follow these steps.</span></span>

1. <span data-ttu-id="5892e-172">Lapas **Opcijas** cilnē **Konti** noklikšķiniet uz **Norādīt apstiprinātāju**.</span><span class="sxs-lookup"><span data-stu-id="5892e-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2. <span data-ttu-id="5892e-173">Laukā **Apstiprinātāja lietotāja ID** atlasiet tā lietotāja ID, kuram ir jāparakstās par cita lietotāja veiktajām izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="5892e-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3. <span data-ttu-id="5892e-174">Laukā **Parakstīties par lietotāja ID** atlasiet tā lietotāja ID, par kura veiktajām izmaiņām ir jāparakstās.</span><span class="sxs-lookup"><span data-stu-id="5892e-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]