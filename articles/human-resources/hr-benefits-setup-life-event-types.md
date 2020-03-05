---
title: Konfigurēt dzīves notikumu veidus
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 93c4285a1918cb625a01b4523195cacdee1170b4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009866"
---
# <a name="configure-life-event-types"></a><span data-ttu-id="38680-102">Konfigurēt dzīves notikumu veidus</span><span class="sxs-lookup"><span data-stu-id="38680-102">Configure life event types</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="38680-103">Microsoft Dynamics 365 Human Resources izmanto dzīves notikumu veidus, lai definētu notikumus, kas ir atļauts atjaunināt darbinieku atvieglojumu reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="38680-103">Microsoft Dynamics 365 Human Resources uses life event types to define events where it is valid to update employee benefits enrollment.</span></span> <span data-ttu-id="38680-104">Piemēram, darbinieks apprecas vai ģimenē ir pieaugums.</span><span class="sxs-lookup"><span data-stu-id="38680-104">For example, getting married or having a child.</span></span> <span data-ttu-id="38680-105">Katru dzīves notikuma veida ID var saistīt tikai ar vienu dzīves notikuma veidu.</span><span class="sxs-lookup"><span data-stu-id="38680-105">Each life event type ID may only be associated with one life event type.</span></span> <span data-ttu-id="38680-106">Piemēram, ja izveidojat dzīves notikuma ID, sauktu par adreses maiņu, kas saistīts ar dzīves notikuma veidu Darbinieka adreses maiņa, nevar izveidot citu ID ar nosaukumu Darbinieka adreses maiņa un saistīt to ar dzīves notikuma veidu Darbinieka adreses maiņa.</span><span class="sxs-lookup"><span data-stu-id="38680-106">For example, if you create a life event ID called Address change that is associated with the life event type Employee address change, you can’t create another ID labeled Employee address change and associate it with the life event type Employee address change.</span></span> 

<span data-ttu-id="38680-107">Kad dzīves notikumu veidi ir izveidoti, tie ir jāsaista ar plānu veidiem.</span><span class="sxs-lookup"><span data-stu-id="38680-107">After you create life event types, you need to associate them with plan types.</span></span> <span data-ttu-id="38680-108">Papildu informāciju skatiet sadaļā [Plānu veidu izveide](hr-benefits-setup-plan-types.md).</span><span class="sxs-lookup"><span data-stu-id="38680-108">For more information, see [Create plan types](hr-benefits-setup-plan-types.md).</span></span>

   > [!NOTE]
   > <span data-ttu-id="38680-109">Pēc dzīves notikuma izveidošanas tas ir jāsaista ar plāna veidu.</span><span class="sxs-lookup"><span data-stu-id="38680-109">When you create a life event, you need to associate it with a plan type.</span></span> <span data-ttu-id="38680-110">Papildu informāciju skatiet sadaļā [Plānu veidu izveide](hr-benefits-setup-life-event-types.md).</span><span class="sxs-lookup"><span data-stu-id="38680-110">For more information, see [Create plan types](hr-benefits-setup-life-event-types.md).</span></span>

## <a name="create-a-life-event-type"></a><span data-ttu-id="38680-111">Izveidot dzīves notikuma veidu</span><span class="sxs-lookup"><span data-stu-id="38680-111">Create a life event type</span></span>

1. <span data-ttu-id="38680-112">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Dzīves notikumu veidi**.</span><span class="sxs-lookup"><span data-stu-id="38680-112">In the **Benefits management** workspace, under **Setup**, select **Life event types**.</span></span>

2. <span data-ttu-id="38680-113">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="38680-113">Select **New**.</span></span>

3. <span data-ttu-id="38680-114">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="38680-114">Specify values for the following fields:</span></span>

   | <span data-ttu-id="38680-115">Lauks</span><span class="sxs-lookup"><span data-stu-id="38680-115">Field</span></span> | <span data-ttu-id="38680-116">Apraksts</span><span class="sxs-lookup"><span data-stu-id="38680-116">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="38680-117">Dzīves notikuma veida ID</span><span class="sxs-lookup"><span data-stu-id="38680-117">Life event type ID</span></span> | <span data-ttu-id="38680-118">Dzīves notikuma veida unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="38680-118">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="38680-119">Apraksts</span><span class="sxs-lookup"><span data-stu-id="38680-119">Description</span></span> | <span data-ttu-id="38680-120">Dzīves notikuma veida apraksts.</span><span class="sxs-lookup"><span data-stu-id="38680-120">A description of the life event type.</span></span> |
   | <span data-ttu-id="38680-121">Dzīves notikuma veids</span><span class="sxs-lookup"><span data-stu-id="38680-121">Life event type</span></span> | <span data-ttu-id="38680-122">Katalizators, lai atjauninātu darbinieka atvieglojumu reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="38680-122">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="38680-123">Lai skatītu dzīves notikumu sarakstu, skatiet zemāk esošo sadaļu [Dzīves notikumi](hr-benefits-setup-payment-frequencies.md?life-events).</span><span class="sxs-lookup"><span data-stu-id="38680-123">For a list of life events, see [Life events](hr-benefits-setup-payment-frequencies.md?life-events) below.</span></span> |

4. <span data-ttu-id="38680-124">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="38680-124">Select **Save**.</span></span>

## <a name="view-attached-plans"></a><span data-ttu-id="38680-125">Skatiet pievienotos plānus</span><span class="sxs-lookup"><span data-stu-id="38680-125">View attached plans</span></span>

<span data-ttu-id="38680-126">Varat redzēt sarakstu ar plānie, kas ir pievienoti atlasītajam dzīves notikuma veidam.</span><span class="sxs-lookup"><span data-stu-id="38680-126">You can see a list of plans that are attached to the selected life event type.</span></span> <span data-ttu-id="38680-127">Dzīves notikumi ir pievienoti plāna veidam, un plāna veidi ir saistīti ar plānu.</span><span class="sxs-lookup"><span data-stu-id="38680-127">Life events are attached to a plan type, and plan types are associated with a plan.</span></span> 

1. <span data-ttu-id="38680-128">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Dzīves notikumu veidi**.</span><span class="sxs-lookup"><span data-stu-id="38680-128">In the **Benefits management** workspace, under **Setup**, select **Life event types**.</span></span>

2. <span data-ttu-id="38680-129">Atlasiet **Darbības**.</span><span class="sxs-lookup"><span data-stu-id="38680-129">Select **Actions**.</span></span>

3. <span data-ttu-id="38680-130">Atlasiet **Pievienotie plāni**.</span><span class="sxs-lookup"><span data-stu-id="38680-130">Select **Attached plans**.</span></span>

## <a name="life-events"></a><span data-ttu-id="38680-131">Dzīves notikumi</span><span class="sxs-lookup"><span data-stu-id="38680-131">Life events</span></span>

<span data-ttu-id="38680-132">Kad izveidojat dzīves notikuma veidu, varat izvēlēties kādu no tālāk norādītajiem dzīves notikumiem:</span><span class="sxs-lookup"><span data-stu-id="38680-132">You can choose from the following life events when you create a life event type:</span></span>

| <span data-ttu-id="38680-133">Dzīves notikums</span><span class="sxs-lookup"><span data-stu-id="38680-133">Life event</span></span> | <span data-ttu-id="38680-134">Vieta</span><span class="sxs-lookup"><span data-stu-id="38680-134">Location</span></span> | <span data-ttu-id="38680-135">Trigeris</span><span class="sxs-lookup"><span data-stu-id="38680-135">Trigger</span></span> |
| --- | --- | --- |
| <span data-ttu-id="38680-136">Ģimenes stāvokļa maiņa</span><span class="sxs-lookup"><span data-stu-id="38680-136">Marital status change</span></span> | <span data-ttu-id="38680-137">Darbinieks > Profils > Personiskā informācija > Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="38680-137">Worker > Profile > Personal information > Marital status</span></span>| <span data-ttu-id="38680-138">Ģimenes stāvokļa maiņa</span><span class="sxs-lookup"><span data-stu-id="38680-138">Change in marital status</span></span> |
| <span data-ttu-id="38680-139">Nodarbinātības statusa maiņa</span><span class="sxs-lookup"><span data-stu-id="38680-139">Employment status change</span></span> | <ul><li><span data-ttu-id="38680-140">Nodarbinātais > Nodarbinātība</span><span class="sxs-lookup"><span data-stu-id="38680-140">Worker > Employment</span></span></li><li><span data-ttu-id="38680-141">Nodarbinātības vēstures lapa</span><span class="sxs-lookup"><span data-stu-id="38680-141">Employment history page</span></span></li></ul> | <span data-ttu-id="38680-142">Nodarbinātības statusa maiņa</span><span class="sxs-lookup"><span data-stu-id="38680-142">Change in employment status</span></span> |
| <span data-ttu-id="38680-143">Darbinieka adreses maiņa</span><span class="sxs-lookup"><span data-stu-id="38680-143">Employee address change</span></span> | <ul><li><span data-ttu-id="38680-144">Nodarbinātais > Profils > Adreses</span><span class="sxs-lookup"><span data-stu-id="38680-144">Worker > Profile > Addresses</span></span> </li><li><span data-ttu-id="38680-145">Nodarbinātais > Personiskā informācija > Personiskie kontakti > Adrese</span><span class="sxs-lookup"><span data-stu-id="38680-145">Worker > Personal information > Personal contacts > Address</span></span></li></ul> <span data-ttu-id="38680-146">Pievienota, rediģēta vai dzēsta adrese</span><span class="sxs-lookup"><span data-stu-id="38680-146">Added, edited, or deleted address</span></span> |
| <span data-ttu-id="38680-147">Pakārtotā maiņa</span><span class="sxs-lookup"><span data-stu-id="38680-147">Dependent change</span></span> | <ul><li><span data-ttu-id="38680-148">Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Pievienot vai dzēst pakārtoto</span><span class="sxs-lookup"><span data-stu-id="38680-148">Worker > Profile > Personal information > Personal contacts > Add or delete a dependent</span></span></li><li><span data-ttu-id="38680-149">Darbinieku patstāvīgi izmantojamais pakalpojums</span><span class="sxs-lookup"><span data-stu-id="38680-149">Employee self service</span></span></li></ul> | <span data-ttu-id="38680-150">Pievienots vai dzēsts pakārtotais.</span><span class="sxs-lookup"><span data-stu-id="38680-150">Added or deleted dependent.</span></span> <span data-ttu-id="38680-151">Personisko kontaktpersonu attiecībām ir jābūt bērnam, dzīvesbiedram, dzīvesbiedram vai bijušajam dzīvesbiedram.</span><span class="sxs-lookup"><span data-stu-id="38680-151">The personal contact relationship must be child, spouse, domestic partner, or ex-spouse.</span></span> <span data-ttu-id="38680-152">Datuma **Derīgs no** atjaunošana aktivizē dzīves notikumu.</span><span class="sxs-lookup"><span data-stu-id="38680-152">Updating the **Valid from** date triggers the life event.</span></span> <span data-ttu-id="38680-153">Ja neatjaunināsit šo datumu, netiks aktivizēts dzīves notikums.</span><span class="sxs-lookup"><span data-stu-id="38680-153">If you don’t update that date, no life event will trigger.</span></span> |
| <span data-ttu-id="38680-154">Dzimšana vai adopcija (pakārtotais)</span><span class="sxs-lookup"><span data-stu-id="38680-154">Birth or Adoption (dependent)</span></span> | <ul><li><span data-ttu-id="38680-155">Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Informācija par pakārtoto</span><span class="sxs-lookup"><span data-stu-id="38680-155">Worker > Profile > Personal information > Personal contacts > Dependent details</span></span></li><li><span data-ttu-id="38680-156">Darbinieku patstāvīgi izmantojamais pakalpojums</span><span class="sxs-lookup"><span data-stu-id="38680-156">Employee self service</span></span></li></ul> | <span data-ttu-id="38680-157">Ir aizpildīts lauks**Pieņemšanas datums**.</span><span class="sxs-lookup"><span data-stu-id="38680-157">**Adoption date** field populated.</span></span> <span data-ttu-id="38680-158">Ir jānorāda bērna dzimšanas datums.</span><span class="sxs-lookup"><span data-stu-id="38680-158">The birthdate of the child is required.</span></span> |
| <span data-ttu-id="38680-159">Vajadzības zaudēšana (laulātais/dzīvesbiedrs)</span><span class="sxs-lookup"><span data-stu-id="38680-159">Loss of coverage (Spouse / domestic partner)</span></span> | <span data-ttu-id="38680-160">Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Vajadzības zudums</span><span class="sxs-lookup"><span data-stu-id="38680-160">Worker > Profile > Personal information > Personal contacts >  Dependent details > Loss of coverage</span></span> | <span data-ttu-id="38680-161">**Vajadzības zudums** atlasīts personiskajai kontaktpersonai kopā ar **Spēkā stāšanās datumu**</span><span class="sxs-lookup"><span data-stu-id="38680-161">**Loss of coverage** selected for a personal contact, along with **Effective date**</span></span> |
| <span data-ttu-id="38680-162">Dzīvesbiedra nodarbinātības izmaiņas</span><span class="sxs-lookup"><span data-stu-id="38680-162">Domestic partner employment change</span></span> | <span data-ttu-id="38680-163">Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Informācija par pakārtoto > Nodarbināts.</span><span class="sxs-lookup"><span data-stu-id="38680-163">Worker > Profile > Personal information > Personal contacts > Dependent details >Employed.</span></span> | <ul><li><span data-ttu-id="38680-164">Izveidota pakārtotā informācija un lauks **Personiskā kontaktpersona nodarbināta** = Jā</span><span class="sxs-lookup"><span data-stu-id="38680-164">Dependent details record created and **Personal contact employed** box = Yes</span></span></li><li><span data-ttu-id="38680-165">**Personiskā kontaktpersona** lauks ir nomainīts (Jā vai Nē)</span><span class="sxs-lookup"><span data-stu-id="38680-165">**Personal contact employed** box changed (Yes or No)</span></span></li></ul> |
| <span data-ttu-id="38680-166">Atvaļinājums (laulātais/dzīvesbiedrs)</span><span class="sxs-lookup"><span data-stu-id="38680-166">Leave of absence (Spouse/domestic partner)</span></span> | <span data-ttu-id="38680-167">Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Pakārtotā informācija > Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="38680-167">Worker > Profile > Personal information > Personal contacts > Dependent details > Leave of absence</span></span> | <ul><li><span data-ttu-id="38680-168">Ir izveidots pakārtotā informācijas ieraksts un aizpildīts **EhrLOAEffectiveDate**</span><span class="sxs-lookup"><span data-stu-id="38680-168">Dependent details record created and **EhrLOAEffectiveDate** filled in</span></span></li><li><span data-ttu-id="38680-169">**personPrivateDetails.EhrIsLOA** ir mainīts (Jā vai nē)</span><span class="sxs-lookup"><span data-stu-id="38680-169">**personPrivateDetails.EhrIsLOA** is changed (Yes or No)</span></span></li><li><span data-ttu-id="38680-170">**personPrivateDetails.EhrLOAEffectiveDate** ir mainīts</span><span class="sxs-lookup"><span data-stu-id="38680-170">**personPrivateDetails.EhrLOAEffectiveDate** is changed</span></span></li></ul> |
| <span data-ttu-id="38680-171">Vajadzības izmaiņas (amats)</span><span class="sxs-lookup"><span data-stu-id="38680-171">Change in coverage (Position)</span></span> | <ul><li><span data-ttu-id="38680-172">Nodarbinātais > Amata piešķire > Nodarbinātā amata piešķires</span><span class="sxs-lookup"><span data-stu-id="38680-172">Worker > Position Assignment > Worker position assignments</span></span></li><li><span data-ttu-id="38680-173">Amati > Amati</span><span class="sxs-lookup"><span data-stu-id="38680-173">Positions > Positions</span></span></li></ul> | <ul><li><span data-ttu-id="38680-174">Mainīt uz pozīciju darbinieka amata piešķires ierakstos</span><span class="sxs-lookup"><span data-stu-id="38680-174">Change to the position in the worker position assignment records</span></span></li><li><span data-ttu-id="38680-175">Nodarbinātā amata piešķires maiņa</span><span class="sxs-lookup"><span data-stu-id="38680-175">Change of the worker assignment in the position</span></span></li></ul> |
| <span data-ttu-id="38680-176">Vajadzības izmaiņas (alga)</span><span class="sxs-lookup"><span data-stu-id="38680-176">Change in coverage (salary)</span></span> | <span data-ttu-id="38680-177">Nodarbinātais > Atlīdzība > Fiksētais plāns</span><span class="sxs-lookup"><span data-stu-id="38680-177">Worker > Compensation > Fixed plan</span></span> | <span data-ttu-id="38680-178">Gada atvieglojumu alga tiek automātiski pārrēķināta, kad maināt atlīdzību</span><span class="sxs-lookup"><span data-stu-id="38680-178">Annual benefit salary automatically recalculates when you change the compensation</span></span> |
| <span data-ttu-id="38680-179">Medicīniskā aprūpe (darbinieks/pakārtotais)</span><span class="sxs-lookup"><span data-stu-id="38680-179">Medicare (Employee / dependent)</span></span> | <span data-ttu-id="38680-180">Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Pakārtotā informācija > Medicīniskās aprūpes spēkā stāšanās datums</span><span class="sxs-lookup"><span data-stu-id="38680-180">Worker > Profile > Personal information > Personal contacts > Dependent details > Medicare effective date</span></span> | <span data-ttu-id="38680-181">Netiek aktivizēts automātiski, kad personiskā kontaktpersona ievada spēkā stāšanās datumu.</span><span class="sxs-lookup"><span data-stu-id="38680-181">Not automatically triggered when a personal contact enters an effective date.</span></span> |
| <span data-ttu-id="38680-182">Ar tiesu piespriests atbalsts</span><span class="sxs-lookup"><span data-stu-id="38680-182">Court ordered support</span></span> | <span data-ttu-id="38680-183">Nodarbinātais > Profils > Personiskā informācija > Personiskie Kontakti > Pakārtotie > Atbalsts pēc tiesas prasības (QMSCO/QDRO un spēkā stāšanās datumi</span><span class="sxs-lookup"><span data-stu-id="38680-183">Worker > Profile > Personal information > Personal contacts > Dependent > Court ordered support (QMSCO/QDRO and effective dates</span></span> | <span data-ttu-id="38680-184">Neaktivizē nevienu automātisko atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="38680-184">Doesn't trigger any automatic updates.</span></span> <span data-ttu-id="38680-185">Tas neietekmē piemērojamību; tas ieraksta dzīves notikumu.</span><span class="sxs-lookup"><span data-stu-id="38680-185">It doesn't impact eligibility; it records a life event.</span></span> |
| <span data-ttu-id="38680-186">Miris</span><span class="sxs-lookup"><span data-stu-id="38680-186">Deceased</span></span> | <span data-ttu-id="38680-187">Nodarbinātais > Profils > Personiskā informācija > Miršanas datums</span><span class="sxs-lookup"><span data-stu-id="38680-187">Worker > Profile > Personal information > Deceased date</span></span> | <span data-ttu-id="38680-188">Ir ievadīts miršanas datums</span><span class="sxs-lookup"><span data-stu-id="38680-188">A deceased date is entered</span></span> |
| <span data-ttu-id="38680-189">Apliecinājums par apdrošināšanu</span><span class="sxs-lookup"><span data-stu-id="38680-189">Evidence of insurance</span></span> | <ul><li><span data-ttu-id="38680-190">Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture > Datumu pārvaldnieka > Informācija par atvieglojumiem</span><span class="sxs-lookup"><span data-stu-id="38680-190">Worker > Worker > Versions > Employment history > Date manager > Benefit details</span></span></li><li> <span data-ttu-id="38680-191">Nodarbinātais > Nodarbinātība > Informācija par atvieglojumiem > Pārbaudes datums</span><span class="sxs-lookup"><span data-stu-id="38680-191">Worker > Employment > Benefit Details > Verification Date</span></span></li></ul> | <ul><li><span data-ttu-id="38680-192">Nodarbinātais ievada pārbaudes datumu</span><span class="sxs-lookup"><span data-stu-id="38680-192">A worker enters a verification date</span></span></li><li><span data-ttu-id="38680-193">Nodarbinātais iestata EvidenceOfInsurability lauku uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="38680-193">A worker sets the EvidenceOfInsurability field to **Yes**</span></span></li></ul> |
| <span data-ttu-id="38680-194">Saņēmējs</span><span class="sxs-lookup"><span data-stu-id="38680-194">Beneficiary</span></span> | <span data-ttu-id="38680-195">Nodarbinātais >Profils > Personiskā informācija > Personiskie kontakti</span><span class="sxs-lookup"><span data-stu-id="38680-195">Worker > Profile > Personal information > Personal contacts</span></span> | <span data-ttu-id="38680-196">Tiek pievienota personīgā kontaktpersona un ir aizpildīts lauks **Saņēmējs** un **Spēkā stāšanās datums**.</span><span class="sxs-lookup"><span data-stu-id="38680-196">A personal contact is added and the **Beneficiary** box and **Effective date** are populated.</span></span> <span data-ttu-id="38680-197">Personiskajai kontaktpersonai ir jābūt ar veidu **Bērns**, **Laulātais**, **Dzīvesbiedrs**, **Atvase**, **Ģimenes kontaktpersona**, **Cita kontaktpersona**, **Vecāks**,**Saņēmēja īpašums**,**Saņēmēja organizācija** vai **Saņēmēja trests**.</span><span class="sxs-lookup"><span data-stu-id="38680-197">The personal contact must be of type **Child**, **Spouse**, **DomesticPartner**, **Sibling**, **FamilyContact**, **OtherContact**, **Parent**, **BeneficiaryEstate**, **BeneficiaryOrg**, or **BeneficiaryTrust**.</span></span> |
| <span data-ttu-id="38680-198">Darbinieka medicīniskā aprūpe</span><span class="sxs-lookup"><span data-stu-id="38680-198">Employee Medicare</span></span> | <span data-ttu-id="38680-199">Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture > Datumu pārvaldnieka > Informācija par atvieglojumiem</span><span class="sxs-lookup"><span data-stu-id="38680-199">Worker > Worker > Versions > Employment history > Date manager > Benefit details</span></span> | <ul><li><span data-ttu-id="38680-200">**EhrMedicareEligibilityDate** ir mainīts</span><span class="sxs-lookup"><span data-stu-id="38680-200">**EhrMedicareEligibilityDate** is changed</span></span></li><li><span data-ttu-id="38680-201">**MedicareEligibile** ir iestatīts uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="38680-201">**MedicareEligibile** is set to **Yes**</span></span></li></ul> |
| <span data-ttu-id="38680-202">Dzimšanas diena</span><span class="sxs-lookup"><span data-stu-id="38680-202">Birthday</span></span> | <span data-ttu-id="38680-203">Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Informācija par pakārtoto > Informācija par dzimšanu</span><span class="sxs-lookup"><span data-stu-id="38680-203">Worker > Profile > Personal information > Personal contacts > Dependent details > Birth date</span></span> | <span data-ttu-id="38680-204">Tiek pievienots vai atjaunināts dzimšanas datums (ne pēc dzīves notikuma izmaiņu apstrādes).</span><span class="sxs-lookup"><span data-stu-id="38680-204">A birth date is added or updated (not after Life event change processing).</span></span> <span data-ttu-id="38680-205">Piemērs: Ja bērna **Personīgā kontakta piemērojamības opcijas** ir iestatītas uz Vecums: 26 sadaļā Iestatījumi > Atvieglojumi > Personiskās kontaktpersonas piemērojamības opcijas un, ja cilvēkresursu personāls veic dzīves notikuma izmaiņas jebkurā dienā pēc tam, kad pakārtotais kļuvis 26 gadu vecs, parādās ziņojums, ka uz pakārtoto vairs neattiecas nodrošinājums.</span><span class="sxs-lookup"><span data-stu-id="38680-205">Example: If the **Personal contact eligibility options** for a child is set to Age: 26 in Setup > Benefits > Personal contact eligibility options, and if HR personnel run Life event change processing any day after the dependent turns 26, a message appears alerting them that the dependent is no longer eligible for coverage.</span></span> |
| <span data-ttu-id="38680-206">Nodarbinātā piemērojamības izmaiņas (nav noteiktas ASV)</span><span class="sxs-lookup"><span data-stu-id="38680-206">Worker eligibility change (not US-specific)</span></span> | <ul><li><span data-ttu-id="38680-207">Nodarbinātais > Nodarbinātība</span><span class="sxs-lookup"><span data-stu-id="38680-207">Worker > Employment</span></span></li><li><span data-ttu-id="38680-208">Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture</span><span class="sxs-lookup"><span data-stu-id="38680-208">Worker > Worker > Versions > Employment history</span></span></li></ul> | <ul><li><span data-ttu-id="38680-209">Nodarbinātā veida, nodarbinātības kategorijas vai piecu lietotājam definējamu piemērojamības lauku maiņa</span><span class="sxs-lookup"><span data-stu-id="38680-209">Employee type, Employment category, or the five user-definable eligibility fields change</span></span></li><li><span data-ttu-id="38680-210">**HcmEmploymentDetail.EhrEmploymentType** izmaiņas (tiek apstrādātas tikai *mainītiem* nodarbinātības informācijas ierakstiem, bet ne *jauniem* nodarbinātības ierakstiem, piemēram, atkārtotai līgšanai vai pārtraukšanai).</span><span class="sxs-lookup"><span data-stu-id="38680-210">**HcmEmploymentDetail.EhrEmploymentType** changes (only processed for *changed* employment detail records, not processed for *new* employment records, like rehire and termination)</span></span></li></ul> |
| <span data-ttu-id="38680-211">Jaunas piemērojamības labošana (ne ASV)</span><span class="sxs-lookup"><span data-stu-id="38680-211">New eligibility override (not US-specific)</span></span> | <span data-ttu-id="38680-212">Papildu cilvēkresursi > Atvieglojumi > Plāni > Atvieglojumi > Piemērotības nosacījumu labošana</span><span class="sxs-lookup"><span data-stu-id="38680-212">Human resources advanced > Benefits > Plans > Benefits > Eligibility rule override</span></span> | <span data-ttu-id="38680-213">Dzīves notikumu apstrādes lietošana</span><span class="sxs-lookup"><span data-stu-id="38680-213">Using Life event processing</span></span> | <span data-ttu-id="38680-214">EhrBenefitEligibilityRuleOverride.ValidFrom</span><span class="sxs-lookup"><span data-stu-id="38680-214">EhrBenefitEligibilityRuleOverride.ValidFrom</span></span> |
| <span data-ttu-id="38680-215">Piemērojamības kārtulas labošanas maiņa (ne ASV)</span><span class="sxs-lookup"><span data-stu-id="38680-215">Eligibility rule override change (not US-specific)</span></span> | <span data-ttu-id="38680-216">Papildu cilvēkresursi > Atvieglojumi > Plāni > Atvieglojumi > Piemērotības nosacījumu labošana</span><span class="sxs-lookup"><span data-stu-id="38680-216">Human resources advanced > Benefits > Plans > Benefits > Eligibility rule override</span></span> | <span data-ttu-id="38680-217">Dzīves notikumu apstrādes lietošana (tver tikai izmaiņas laukos**ValidFrom** un **ValidTo** Piemērojamības kārtulas labošanā)</span><span class="sxs-lookup"><span data-stu-id="38680-217">Using Life event processing (only catches changes to **ValidFrom** and **ValidTo** fields on the Eligibility rule override)</span></span> |
| <span data-ttu-id="38680-218">Piemērojamības kārtulas labošanas termiņa beigas (ne ASV)</span><span class="sxs-lookup"><span data-stu-id="38680-218">Eligibility rule override expiration (not US-specific)</span></span> | <span data-ttu-id="38680-219">Papildu cilvēkresursi > Atvieglojumi > Plāni > Atvieglojumi > Piemērotības nosacījumu labošana</span><span class="sxs-lookup"><span data-stu-id="38680-219">Human resources advanced > Benefits > Plans > Benefits > Eligibility rule override</span></span> | <span data-ttu-id="38680-220">Dzīves notikumu izmaiņu apstrādes izmantošana.</span><span class="sxs-lookup"><span data-stu-id="38680-220">Using Life event change processing.</span></span> <span data-ttu-id="38680-221">Piemēram, ja rediģējat plāna piemērojamības kārtulas labošanas beigu datumu, lai tas būtu šodien, plkst. 17:00, jebkurā laikā pēc 17:00 vai nākamajās dienās un pēc tam palaižat dzīves notikuma izmaiņu apstrādi, parādās ziņojums, kas apgalvo, ka piemērojamības kārtulas labošanai ir beidzies derīgums.</span><span class="sxs-lookup"><span data-stu-id="38680-221">For example, if you edit a plan’s eligibility rule override expiration date to be today at 5:00 pm, any time after 5:00 pm or the following days, and then run Life event change processing, a message appears saying that the eligibility rule override has expired.</span></span> |
| <span data-ttu-id="38680-222">Jauns atvieglojumu plāns (nav ASV)</span><span class="sxs-lookup"><span data-stu-id="38680-222">New benefit plan (not US-specific)</span></span> | <span data-ttu-id="38680-223">Papildu cilvēkresursi > Atvieglojumi > Plāni > Jauns</span><span class="sxs-lookup"><span data-stu-id="38680-223">Human resources advanced > Benefits > Plans > New</span></span> | <ul><li><span data-ttu-id="38680-224">Piemērojamības opcijas tiek pievienotas pašreizējam plānam</span><span class="sxs-lookup"><span data-stu-id="38680-224">Eligibility options are added to a current plan</span></span></li><li><span data-ttu-id="38680-225">Ir pievienots jauns plāns ar pievienotām piemērojamības opcijām</span><span class="sxs-lookup"><span data-stu-id="38680-225">A new plan with eligibility options attached is added</span></span></li></ul></br></br><span data-ttu-id="38680-226">Cilvēkresursu personālam vajadzētu šajā instancē palaist dzīves notikuma piemērojamības apstrādi</span><span class="sxs-lookup"><span data-stu-id="38680-226">HR personnel should run Life event eligibility processing in this instance.</span></span> |
| <span data-ttu-id="38680-227">Piemērojamības kārtulas maiņa (ne ASV)</span><span class="sxs-lookup"><span data-stu-id="38680-227">Eligibility rule change (not US-specific)</span></span> | <span data-ttu-id="38680-228">Papildu cilvēkresursi > Atvieglojumi > Noteikumi/opcija > Piemērojamības noteikumi</span><span class="sxs-lookup"><span data-stu-id="38680-228">Human resources advanced > Benefits > Rules/options > Eligibility rules</span></span> | <span data-ttu-id="38680-229">Dzīves notikumu piemērojamības apstrādes izmantošana.</span><span class="sxs-lookup"><span data-stu-id="38680-229">Using Life event eligibility processing.</span></span> <span data-ttu-id="38680-230">Reģistrēti, ja**EhrBenefitEligibilityRule** ierakstiem ir mainītas šādas vērtības: **UseEmplCategory**, **UseEmplStatus** vai **UseEmplType**.</span><span class="sxs-lookup"><span data-stu-id="38680-230">Logged when **EhrBenefitEligibilityRule** records have the following values changed: **UseEmplCategory**, **UseEmplStatus**, or **UseEmplType**.</span></span> <span data-ttu-id="38680-231">Atjaunina tikai dzīves notikuma darbības, kas jau pastāv mainītai kārtulai vai piemērojamības kritērijam.</span><span class="sxs-lookup"><span data-stu-id="38680-231">Only updates life event transactions that already exist for a changed rule or eligibility criteria.</span></span> |