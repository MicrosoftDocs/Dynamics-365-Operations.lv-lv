---
title: Elektronisko parakstu apskats
description: "Šajā rakstā ir sniegts pārskats par elektroniskajiem parakstiem un ir aprakstīts, kā tos var izmantot programmatūrā Microsoft Dynamics 365 for Finance and Operations."
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 698b938e515ff4755c2f111279cda244577ac9f3
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="electronic-signature-overview"></a><span data-ttu-id="55762-103">Elektronisko parakstu apskats</span><span class="sxs-lookup"><span data-stu-id="55762-103">Electronic signature overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="55762-104">Šajā rakstā ir sniegts pārskats par elektroniskajiem parakstiem un ir aprakstīts, kā tos var izmantot programmatūrā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="55762-104">This article provides an overview of electronic signatures and describes how they can be used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-an-electronic-signature"></a><span data-ttu-id="55762-105">Kas ir elektronisks paraksts?</span><span class="sxs-lookup"><span data-stu-id="55762-105">What is an electronic signature?</span></span>
--------------------------------

<span data-ttu-id="55762-106">Elektroniskais paraksts apstiprina personas identitāti, kas gatavojas sākt vai apstiprināt skaitļošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="55762-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="55762-107">Dažās nozarēs elektroniskais paraksts ir tikpat juridiski saistošs kā ar roku veikts paraksts.</span><span class="sxs-lookup"><span data-stu-id="55762-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> 

<span data-ttu-id="55762-108">Vairākās regulētas nozarēs, piemēram, farmācijas, pārtikas un dzērienu un aviācijas un aizsardzības nozarēs, elektronisko parakstu izmantošana ir normatīva prasība.</span><span class="sxs-lookup"><span data-stu-id="55762-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="55762-109">Tie ir arī nepieciešami, lai izpildītu ASV Pārtikas un zāļu pārvaldes (FDA) izdotā standarta 21 CFR 11. daļas normatīvās prasības.</span><span class="sxs-lookup"><span data-stu-id="55762-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span> 

<span data-ttu-id="55762-110">**Piezīme.** Elektroniskais paraksts pats par sevi nav tas pats kas ciparparaksts.</span><span class="sxs-lookup"><span data-stu-id="55762-110">**Note:** An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="55762-111">Elektroniskais paraksts ir vienkārši ar roku rakstīta paraksta aizstājējs, bet ciparparaksts sniedz papildu drošības pasākumus.</span><span class="sxs-lookup"><span data-stu-id="55762-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="55762-112">Ciparparaksts var palīdzēt identificēt, vai cits lietotājs vai process ir darbojies ar datiem.</span><span class="sxs-lookup"><span data-stu-id="55762-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="55762-113">Ciparparakstu var arī verificēt, un šo verifikāciju nevar atspēkot datu parakstīšanai izmantotā sertifikāta īpašnieks.</span><span class="sxs-lookup"><span data-stu-id="55762-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="55762-114">Kā tas ir aprakstīts tālāk, elektroniskajiem parakstiem programmatūrā Microsoft Dynamics 365 for Finance and Operations ir iebūvēta ciparparaksta funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="55762-114">As described below, electronic signatures in Microsoft Dynamics 365 for Finance and Operations have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="55762-115">Elektroniskie paraksti programmatūrā Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="55762-115">Electronic signatures in Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="55762-116">Programmatūrā Dynamics 365 for Finance and Operations varat izmantot elektroniskos parakstus īpaši svarīgiem biznesa procesiem.</span><span class="sxs-lookup"><span data-stu-id="55762-116">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="55762-117">Dažiem procesiem ir iebūvētas elektronisko parakstu iespējas.</span><span class="sxs-lookup"><span data-stu-id="55762-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="55762-118">Varat arī izveidot pielāgotas parakstu prasības jebkurai datu bāzes tabulai un laukam.</span><span class="sxs-lookup"><span data-stu-id="55762-118">You can also create custom signature requirements for any database table and field.</span></span> 

<span data-ttu-id="55762-119">Elektroniskajiem parakstiem ir iebūvēta ciparparaksta funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="55762-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="55762-120">Katram lietotājam, kas paraksta dokumentus, ir jāiegūst derīgs šifrēšanas sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="55762-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="55762-121">Kad dokuments ir parakstīts, tiek validēta ar šo sertifikātu saistītā privātā atslēga.</span><span class="sxs-lookup"><span data-stu-id="55762-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="55762-122">Programmatūrā Dynamics 365 for Finance and Operations elektroniskā paraksta informācija tiek reģistrēta žurnālā, lai nodrošinātu auditācijas pierakstus.</span><span class="sxs-lookup"><span data-stu-id="55762-122">Finance and Operations records electronic signature information in a log to provide an audit trail.</span></span> <span data-ttu-id="55762-123">Lai iestatītu elektroniskos parakstus, skatiet rakstu [Iestatīt elektroniskos parakstus (uzdevuma ceļvedis)](tasks/set-up-electronic-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="55762-123">To set up electronic signatures, see [Set up electronic signatures (Task guide)](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="55762-124">Lietotāji, kuriem ir nepieciešama piekļuve elektroniskajiem parakstiem</span><span class="sxs-lookup"><span data-stu-id="55762-124">Users who require access to electronic signatures</span></span>
<span data-ttu-id="55762-125">Elektroniskajiem parakstiem drošības piekļuve parasti ir nepieciešama trīs veidu lietotājiem: elektronisko parakstu administratoriem, parakstītājiem un elektronisko parakstu auditoriem.</span><span class="sxs-lookup"><span data-stu-id="55762-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="55762-126">Elektronisko parakstu administrators</span><span class="sxs-lookup"><span data-stu-id="55762-126">Electronic signature administrator</span></span>

<span data-ttu-id="55762-127">Elektronisko parakstu administrators iestata parakstu prasības, vispārējos parametrus un apstiprinātājus, kā arī saņem brīdinājumus, kad parakstus neizdodas verificēt.</span><span class="sxs-lookup"><span data-stu-id="55762-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="55762-128">Lietotājam, kuram ir piešķirta drošības loma **Informācijas tehnoloģiju vadītājs**, pēc noklusējuma ir atļauts administrēt elektroniskos parakstus.</span><span class="sxs-lookup"><span data-stu-id="55762-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="55762-129">Parakstītājs</span><span class="sxs-lookup"><span data-stu-id="55762-129">Signer</span></span>

<span data-ttu-id="55762-130">Parakstītājs sniedz elektroniskos parakstus dokumentiem un procesiem, kam ir nepieciešami paraksti.</span><span class="sxs-lookup"><span data-stu-id="55762-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="55762-131">Lietotājam, kuram ir piešķirta drošības loma **Sistēmas lietotājs**, pēc noklusējuma ir atļauts elektroniski parakstīt dokumentus.</span><span class="sxs-lookup"><span data-stu-id="55762-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span> 

<span data-ttu-id="55762-132">**Piezīme.** Parakstītājam var būt nepieciešamas papildu atļaujas, pirms tiek nodrošināta piekļuve datiem, kas ir saistīti ar parakstāmo dokumentu vai procesu.</span><span class="sxs-lookup"><span data-stu-id="55762-132">**Note:** The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="55762-133">Lietotājam, kas veic izmaiņas datos un kam pēc tam ir jāparakstās par šīm izmaiņām, ir nepieciešama atļauja mainīt šos datus.</span><span class="sxs-lookup"><span data-stu-id="55762-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="55762-134">Lietotājam, kurš parakstās cita lietotāja vārdā, var nebūt nepieciešama piekļuve datiem.</span><span class="sxs-lookup"><span data-stu-id="55762-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="55762-135">Šāda lietotāja piemērs ir supervizors, kas parakstās par darbinieka veiktajām izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="55762-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="55762-136">Elektronisko parakstu auditors</span><span class="sxs-lookup"><span data-stu-id="55762-136">Electronic signature auditor</span></span>

<span data-ttu-id="55762-137">Elektronisko parakstu auditors pārskata datu bāzes žurnālu un parakstu pārskata žurnālu, kas ir pieejams no datu bāzes žurnāla.</span><span class="sxs-lookup"><span data-stu-id="55762-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="55762-138">Lietotājam, kuram ir piešķirta drošības loma **Informācijas tehnoloģiju vadītājs**, pēc noklusējuma ir atļauts auditēt elektroniskos parakstus.</span><span class="sxs-lookup"><span data-stu-id="55762-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span> 

<span data-ttu-id="55762-139">Ja izmantojat citu lomu, nevis **Informācijas tehnoloģiju vadītā**, pārliecinieties, ka lomai ir piešķirtas tālāk norādītās privilēģijas.</span><span class="sxs-lookup"><span data-stu-id="55762-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

-   <span data-ttu-id="55762-140">Skatīt elektroniskā paraksta kļūmes</span><span class="sxs-lookup"><span data-stu-id="55762-140">View electronic signature failures</span></span>
-   <span data-ttu-id="55762-141">Skatīt datu bāzes žurnālu</span><span class="sxs-lookup"><span data-stu-id="55762-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="55762-142">Elektroniska dokumentu parakstīšana</span><span class="sxs-lookup"><span data-stu-id="55762-142">Signing documents electronically</span></span>
### <a name="get-a-certificate"></a><span data-ttu-id="55762-143">Sertifikāta iegūšana</span><span class="sxs-lookup"><span data-stu-id="55762-143">Get a certificate</span></span>

<span data-ttu-id="55762-144">Pirms dokumentu elektroniskas parakstīšanas programmatūrā Dynamics 365 for Finance and Operations ir jāpieprasa sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="55762-144">Before you sign documents electronically in Finance and Operations, you must request a certificate.</span></span> 

<span data-ttu-id="55762-145">**Piezīme.** Sertifikātu izveidei un elektroniskās parakstīšanas iespējošanai programmatūrā Dynamics 365 for Finance and Operations tiek izmantoti Microsoft SQL Server līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="55762-145">**Note:** Finance and Operations uses Microsoft SQL Server features to create certificates and enable electronic signing.</span></span> <span data-ttu-id="55762-146">Nav nepieciešami nekādi papildu sertifikāti vai publisku atslēgu infrastruktūra (PKI).</span><span class="sxs-lookup"><span data-stu-id="55762-146">No additional certificate or public key infrastructure (PKI) is required.</span></span> 

<span data-ttu-id="55762-147">Kad pieprasāt sertifikātu, programmatūras Dynamics 365 for Finance and Operations datu bāzē jums tiek izveidota publiskā atslēga un privātā atslēga.</span><span class="sxs-lookup"><span data-stu-id="55762-147">When you request a certificate, a public key and a private key are created for you in the Finance and Operations database.</span></span> <span data-ttu-id="55762-148">Privātā atslēga ir šifrēta, izmantojot tikai jums zināmu paroli.</span><span class="sxs-lookup"><span data-stu-id="55762-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="55762-149">Kad parakstāt dokumentu elektroniski, jūsu identitāti verificē, kad ievadāt paroli.</span><span class="sxs-lookup"><span data-stu-id="55762-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span> 

<span data-ttu-id="55762-150">Lai pieprasītu sertifikātu, lapas **Opcijas** cilnē **Konti** noklikšķiniet uz **Iegūt sertifikātu**.</span><span class="sxs-lookup"><span data-stu-id="55762-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span> 

<span data-ttu-id="55762-151">Jums ir jāievada un jāapstiprina parole, ko izmantosiet parakstīšanai.</span><span class="sxs-lookup"><span data-stu-id="55762-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="55762-152">Šo paroli izmanto, lai aizsargātu jūsu privāto atslēgu un autorizētu jūsu sertifikāta lietošanu.</span><span class="sxs-lookup"><span data-stu-id="55762-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="55762-153">Šī parole netiek glabāta datu bāzē un nav pieejama nevienam citam, tostarp Dynamics 365 for Finance and Operations administratoram.</span><span class="sxs-lookup"><span data-stu-id="55762-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the Finance and Operations administrator.</span></span> 

<span data-ttu-id="55762-154">Ja aizmirstat ar savu sertifikātu saistīto paroli, šo sertifikātu ir nepieciešams atiestatīt.</span><span class="sxs-lookup"><span data-stu-id="55762-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="55762-155">Ja atiestatāt šo sertifikātu, jūs neietekmējat ar iepriekšējo sertifikātu parakstītos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="55762-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="55762-156">Lai atiestatītu sertifikātu, lapā **Opcijas** noklikšķiniet uz **Atiestatīt sertifikātu**.</span><span class="sxs-lookup"><span data-stu-id="55762-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="55762-157">Elektroniska dokumentu parakstīšana</span><span class="sxs-lookup"><span data-stu-id="55762-157">Sign a document electronically</span></span>

<span data-ttu-id="55762-158">Lapa **Parakstīt dokumentu** tiek parādīta, kad veicat izmaiņas, kurām nepieciešams elektroniskais paraksts.</span><span class="sxs-lookup"><span data-stu-id="55762-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1.  <span data-ttu-id="55762-159">Lapā **Parakstīt dokumentu** noklikšķiniet uz cilnes **Dokuments**, lai pārskatītu dokumentā veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="55762-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2.  <span data-ttu-id="55762-160">Cilnē **Paraksts** atlasiet pamatojuma kodu.</span><span class="sxs-lookup"><span data-stu-id="55762-160">On the **Signature** tab, select a reason code.</span></span>
3.  <span data-ttu-id="55762-161">Ievadiet komentāru, ja ir nepieciešami kādi komentāri.</span><span class="sxs-lookup"><span data-stu-id="55762-161">Enter a comment, if a comment is required.</span></span>
4.  <span data-ttu-id="55762-162">Ja jūsu lietotāja ID netiek rādīts laukā **Parakstītājs**, tad atlasiet to sarakstā.</span><span class="sxs-lookup"><span data-stu-id="55762-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5.  <span data-ttu-id="55762-163">Ievadiet savu atrašanās vietu, ja šāda informācija ir nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="55762-163">Enter your location, if this information is required.</span></span>
6.  <span data-ttu-id="55762-164">Noklikšķiniet uz **OK**.</span><span class="sxs-lookup"><span data-stu-id="55762-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="55762-165">Parakstīties par cita lietotāja veiktām izmaiņām</span><span class="sxs-lookup"><span data-stu-id="55762-165">Sign for another user's changes</span></span>

<span data-ttu-id="55762-166">Iespējams, reizēm jūs vēlaties, lai lietotājs parakstītos par cita lietotāja veiktajām izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="55762-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="55762-167">Piemēram, supervizoram varētu būt jāparakstās par izmaiņām, ko kāds darbinieks ir veicis materiālu komplektā (MK).</span><span class="sxs-lookup"><span data-stu-id="55762-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="55762-168">Izmantojiet šo procedūru, lai norādītu Dynamics 365 for Finance and Operations lietotāju, kas parakstās par cita lietotāja veiktajām izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="55762-168">Use this procedure to designate a Finance and Operations user as a signer for another user.</span></span> 

<span data-ttu-id="55762-169">**Piezīme.** Kad viens lietotājs parakstās par cita lietotāja veiktajām izmaiņām, paraksts ir jānodrošina izmaiņas veikušā lietotāja darbstacijā.</span><span class="sxs-lookup"><span data-stu-id="55762-169">**Note:** When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="55762-170">Lietotājs nevar saglabāt izmaiņas, pirms ir sniegts paraksts.</span><span class="sxs-lookup"><span data-stu-id="55762-170">The user can't save the change until the signature has been provided.</span></span> 

<span data-ttu-id="55762-171">Lai norādītu apstiprinātājus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="55762-171">To designate approvers, follow these steps.</span></span>

1.  <span data-ttu-id="55762-172">Lapas **Opcijas** cilnē **Konti** noklikšķiniet uz **Norādīt apstiprinātāju**.</span><span class="sxs-lookup"><span data-stu-id="55762-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2.  <span data-ttu-id="55762-173">Laukā **Apstiprinātāja lietotāja ID** atlasiet tā lietotāja ID, kuram ir jāparakstās par cita lietotāja veiktajām izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="55762-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3.  <span data-ttu-id="55762-174">Laukā **Parakstīties par lietotāja ID** atlasiet tā lietotāja ID, par kura veiktajām izmaiņām ir jāparakstās.</span><span class="sxs-lookup"><span data-stu-id="55762-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>





