---
title: Veidnes MK
description: "Veidnes materiālu komplekti (MK) nodrošina standartizētu komponentu sarakstu tiem pakalpojumu objektiem, kas tiek apkalpoti regulāri."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6e3a16b9938f6d4222e0a95078356f457e71a1bb
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="template-boms"></a><span data-ttu-id="5fe81-103">Veidnes MK</span><span class="sxs-lookup"><span data-stu-id="5fe81-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5fe81-104">Veidnes materiālu komplekti (MK) jums nodrošina standartizētu komponentu sarakstu tiem pakalpojumu objektiem, kas tiek apkalpoti regulāri.</span><span class="sxs-lookup"><span data-stu-id="5fe81-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="5fe81-105">Komponenti, kas ir uzskaitīti veidnes MK, pārstāv pakalpojumu objekta atsevišķos apakškomponentus.</span><span class="sxs-lookup"><span data-stu-id="5fe81-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="5fe81-106">Pakalpojumu objektam lietojot veidnes MK, varat reģistrēt apakškomponentus, kas ir aizstāti šim pakalpojumu objektam.</span><span class="sxs-lookup"><span data-stu-id="5fe81-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="5fe81-107">Lai pielietotu veidnes MK pakalpojumu līgumam vai pakalpojumu pasūtījumam, pievienojiet to pakalpojumu objektu attiecībām.</span><span class="sxs-lookup"><span data-stu-id="5fe81-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5fe81-108">Katram pakalpojumu objektam varat lietot tikai vienu veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="5fe81-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="5fe81-109">Veidnes MK izveidošana</span><span class="sxs-lookup"><span data-stu-id="5fe81-109">Create a template BOM</span></span>

<span data-ttu-id="5fe81-110">Nākamajā tabulā ir informācija par dažādajām metodēm, kuras varat izmantot, lai izveidotu veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="5fe81-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fe81-111">Metode</span><span class="sxs-lookup"><span data-stu-id="5fe81-111">Method</span></span></p></th>
<th><p><span data-ttu-id="5fe81-112">Apraksts</span><span class="sxs-lookup"><span data-stu-id="5fe81-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fe81-113">Ražošana</span><span class="sxs-lookup"><span data-stu-id="5fe81-113">Production</span></span></p></td>
<td><p><span data-ttu-id="5fe81-114">Šis veidnes MK ir balstīts uz ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="5fe81-115">Šī opcija ir piemērojama tikai tad, ja darbojaties ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="5fe81-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="5fe81-116">Šīs metodes priekšrocība ir tā, ka jums ir pašreizējs, detalizēts saraksts ar sastāvdaļām, kas aizvieto krājumu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe81-117">Krājuma MK</span><span class="sxs-lookup"><span data-stu-id="5fe81-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="5fe81-118">Veidnes MK ir balstīts uz krājuma MK.</span><span class="sxs-lookup"><span data-stu-id="5fe81-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="5fe81-119">Krājuma MK, atšķirībā no ražošanas MK, ir statisks saraksts ar komponentiem, kas veido kādu krājumu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe81-120">Pastāvoša veidne</span><span class="sxs-lookup"><span data-stu-id="5fe81-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="5fe81-121">Veidne ir balstīta uz pastāvošu veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="5fe81-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe81-122">Manuāli</span><span class="sxs-lookup"><span data-stu-id="5fe81-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="5fe81-123">Ja jūs zināt, kuras rezerves daļas parasti tiek aizvietotas kādā pakalpojumu objektā, savu veidnes MK varat izveidot manuāli.</span><span class="sxs-lookup"><span data-stu-id="5fe81-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="5fe81-124">Šī metode noder, lai nodrošinātu, ka veidnē ietvertie komponenti ataino faktiskās vajadzības jūsu darba vietā.</span><span class="sxs-lookup"><span data-stu-id="5fe81-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="5fe81-125">Veidnes MK lietošana pakalpojumu līgumam vai pakalpojumu pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="5fe81-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="5fe81-126">Veidnes MK varat lietot kādam pakalpojumu līgumam, pakalpojumu pasūtījumam vai abiem.</span><span class="sxs-lookup"><span data-stu-id="5fe81-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="5fe81-127">Pakalpojumu līgums parasti sedz ilgtermiņa attiecības ar klientu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="5fe81-128">Pakalpojumu materiālu komplektā (MK) ierakstītā aizvietojumu vēsture ir pakalpojumu līgumam noderīgi dati.</span><span class="sxs-lookup"><span data-stu-id="5fe81-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="5fe81-129">Veidnes materiālu komplektu (MK) varat lietot arī pakalpojumu pasūtījumam, lai ierakstītu pakalpojumu objektam izpildīto pakalpojumu vēsturi.</span><span class="sxs-lookup"><span data-stu-id="5fe81-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="5fe81-130">Pakalpojumu MK vēstures kopēšana</span><span class="sxs-lookup"><span data-stu-id="5fe81-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="5fe81-131">Pakalpojumu MK rindas vēsturi varat kopēt no viena pakalpojumu līguma uz citu pakalpojumu līgumu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="5fe81-132">Kopējot pakalpojumu vēsturi starp pakalpojumu līgumiem, varat saglabāt ierakstu par kāda krājuma aizvietošanu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="5fe81-133">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="5fe81-133">**Example**</span></span>

<span data-ttu-id="5fe81-134">Jūs esat iestatījis trīs gadu ilgu pakalpojumu līgumu klienta mašīnai.</span><span class="sxs-lookup"><span data-stu-id="5fe81-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="5fe81-135">Šajā laikā klients pierod pie uzņēmuma sniegtajiem labajiem pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="5fe81-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="5fe81-136">Tādēļ pēc līguma beigām klients vēlas iestatīt jaunu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="5fe81-137">Tagad jūs varat vienoties par uzņēmumam izdevīgāku līgumu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="5fe81-138">Tā kā ieraksti par aizvietotajiem komponentiem var noderēt arī turpmāk, šī pakalpojumu MK vēsturi jūs kopējat uz jauno līgumu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="5fe81-139">Veidnes MK modificēšana</span><span class="sxs-lookup"><span data-stu-id="5fe81-139">Modify the template BOM</span></span>

<span data-ttu-id="5fe81-140">Ja kāds veidnes MK nav pievienots nevienam pakalpojumu objektam, tajā varat modificēt vai dzēst rindas.</span><span class="sxs-lookup"><span data-stu-id="5fe81-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="5fe81-141">Pēc veidnes MK pievienošanas kādam pakalpojumu objektam varat modificēt tikai MK lokālo versiju.</span><span class="sxs-lookup"><span data-stu-id="5fe81-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="5fe81-142">Ja vēlaties dublēt veidnes MK lokālās versijas iestatījumus, jūs varat izveidot jaunu veidnes MK, kas balstās uz lokālo versiju.</span><span class="sxs-lookup"><span data-stu-id="5fe81-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="5fe81-143">Plašāku informāciju skatiet tēmā [Pakalpojumu MK modificēšana](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="5fe81-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="5fe81-144">Ja aizvietojat kādu materiālu komplektā (MK) ietvertu krājumu, šo aizvietošanu varat iereģistrēt MK veidotāja MK rindā.</span><span class="sxs-lookup"><span data-stu-id="5fe81-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="5fe81-145">Ja vēlaties, aizvietošanas objektam varat izveidot pakalpojumu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="5fe81-146">Ja izveidojat pakalpojumu pasūtījuma rindu, varat izrakstīt rēķinu par aizvietošanas krājumu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="5fe81-147">Ja aizvietošanai neizveidojat pakalpojumu pasūtījuma rindu, aizvietošanas reģistrācija tiek paturēta, lai varētu izsekot pakalpojumu objekta vēsturi.</span><span class="sxs-lookup"><span data-stu-id="5fe81-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="5fe81-148">MK rindas informācijas rādīšanas veida mainīšana</span><span class="sxs-lookup"><span data-stu-id="5fe81-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="5fe81-149">Varat mainīt veidu, kā visiem veidņu un pakalpojumu MK tiek rādīta MK rindas informācija.</span><span class="sxs-lookup"><span data-stu-id="5fe81-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="5fe81-150">Šīs izmaiņas attiecas uz visiem veidņu MK un pakalpojumu MK.</span><span class="sxs-lookup"><span data-stu-id="5fe81-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="5fe81-151">Tostarp arī tādiem, kas ir pievienoti pakalpojumu objektiem.</span><span class="sxs-lookup"><span data-stu-id="5fe81-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="5fe81-152">Veidņu MK numuru sēriju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5fe81-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="5fe81-153">Lai izmantotu veidņu MK, ir jāiestata divas numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="5fe81-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="5fe81-154">Iestatiet vienu numuru sēriju veidnes materiālu komplektam (MK) un vienu — MK vēstures rindas numuram.</span><span class="sxs-lookup"><span data-stu-id="5fe81-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5fe81-155">Numuru sērijas tiek izmantotas visā sistēmā Microsoft Dynamics AX, lai piešķirtu identifikatorus ierakstiem, kam tie ir nepieciešami.</span><span class="sxs-lookup"><span data-stu-id="5fe81-155">Number sequences are used throughout Microsoft Dynamics AX to allocate identifiers to records that require them.</span></span> <span data-ttu-id="5fe81-156">Lai numuru sēriju varētu piešķirt veidnes MK vai MK vēstures rindas numuram, ir jāiestata numuru sēriju kodi.</span><span class="sxs-lookup"><span data-stu-id="5fe81-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="5fe81-157">Numuru sēriju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5fe81-157">Set up number sequences</span></span>

1.  <span data-ttu-id="5fe81-158">Saraksta lapā **Numuru sērijas** izveidojiet numuru sērijas veidņu materiālu komplektu (MK) un MK vēstures rindu numuram.</span><span class="sxs-lookup"><span data-stu-id="5fe81-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="5fe81-159">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="5fe81-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="5fe81-160">Noklikšķiniet uz **Numuru sērijas** un pēc tam atlasiet kādu numuru sērijas kodu numuru sēriju atsaucēm, kuras izveidojāt formā **Numuru sērijas**.</span><span class="sxs-lookup"><span data-stu-id="5fe81-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="5fe81-161">Aizveriet formu, lai saglabātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="5fe81-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5fe81-162">MK vēstures rindas numuru sistēma izmanto, lai transakcijas MK vēsturē saistītu ar pakalpojumu līgumu vai pakalpojumu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5fe81-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="5fe81-163">Šis numurs netiek rādīts lietotāja interfeisā.</span><span class="sxs-lookup"><span data-stu-id="5fe81-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="5fe81-164">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="5fe81-164">See also</span></span>

[<span data-ttu-id="5fe81-165">Veidnes MK izveide</span><span class="sxs-lookup"><span data-stu-id="5fe81-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="5fe81-166">Veidņu MK pārvaldīšana objektu attiecībās.</span><span class="sxs-lookup"><span data-stu-id="5fe81-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="5fe81-167">Pakalpojuma MK modificēšana</span><span class="sxs-lookup"><span data-stu-id="5fe81-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 



