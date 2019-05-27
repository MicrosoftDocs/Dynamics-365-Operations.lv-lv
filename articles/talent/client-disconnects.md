---
title: Talent klients atvienojas
description: Šajā tēmā paskaidrots, kā rīkoties, ja debitors tiek atvienots no vides un nav zināms, kāpēc.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 885e2d743cd2b01588546327840508f6f7e95958
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518517"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="edb15-103">Talent klients atvienojas</span><span class="sxs-lookup"><span data-stu-id="edb15-103">Talent client disconnects</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="edb15-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="edb15-104">**Environment details**</span></span> 

<span data-ttu-id="edb15-105">Šāda problēma var rasties visās vidēs.</span><span class="sxs-lookup"><span data-stu-id="edb15-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="edb15-106">**Simptoms**</span><span class="sxs-lookup"><span data-stu-id="edb15-106">**Symptom**</span></span> 

<span data-ttu-id="edb15-107">Debitors tiek atvienots no vides un nav zināms, kāpēc.</span><span class="sxs-lookup"><span data-stu-id="edb15-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="edb15-108">Debitors saņem vienu no šādiem kļūdu ziņojumiem:</span><span class="sxs-lookup"><span data-stu-id="edb15-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="edb15-109">Savienojums tika zaudēts.</span><span class="sxs-lookup"><span data-stu-id="edb15-109">We've lost your connection.</span></span> <span data-ttu-id="edb15-110">Nokl. uz Aizv., lai turp. darbu.</span><span class="sxs-lookup"><span data-stu-id="edb15-110">Click Close to continue working.</span></span>
- <span data-ttu-id="edb15-111">Šķiet, ka ir zaudēts savienojums ar tīklu; lai mēģinātu vēlreiz, noklikšķiniet uz Mēģināt vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="edb15-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="edb15-112">**Sarkans karodziņš**</span><span class="sxs-lookup"><span data-stu-id="edb15-112">**Red flag**</span></span>

<span data-ttu-id="edb15-113">Šī problēma parasti rodas, ja lietotāji ir ieviešanas posmā, salīdzina informāciju ražošanas un testēšanas vidēs un aizmirst, ka tie pārslēdzas starp sesijām.</span><span class="sxs-lookup"><span data-stu-id="edb15-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="edb15-114">Ja lietotāji ir šajā posmā, viņiem, visticamāk, rodas šī problēmu.</span><span class="sxs-lookup"><span data-stu-id="edb15-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="edb15-115">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="edb15-115">**Issue**</span></span> 

<span data-ttu-id="edb15-116">**Pārlūkprogrammu veidi:** Google Chrome, Internet Explorer un Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="edb15-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="edb15-117">Lietotāji tiek atvienoti no platformas Microsoft Dynamics 365 for Talent, ja vienlaicīgi ir atvērtas divas dažādas sesijas ar vienu un to pašu lietotāju un vienu un to pašu pārlūkprogrammas veidu.</span><span class="sxs-lookup"><span data-stu-id="edb15-117">The Microsoft Dynamics 365 for Talent platform disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="edb15-118">(Piemēram, lietotājs A skata gan 1. vidi, gan 2. vidi pārlūkprogrammā Chrome.) Nav svarīgi, vai lietotāji atver citus pārlūkprogrammas logus vai dažādas cilnes.</span><span class="sxs-lookup"><span data-stu-id="edb15-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="edb15-119">Ja tiek izmantoti tie paši lietotāja akreditāc. dati, lai vienlaicīgi pierakstītos gan 1. vidē, gan 2. vidē tajā pašā pārlūkprogrammas tipā, Talent atvieno vienu no sesijām.</span><span class="sxs-lookup"><span data-stu-id="edb15-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="edb15-120">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="edb15-120">**Solution**</span></span>

<span data-ttu-id="edb15-121">Pārliec., ka vienlaicīgi ir atvērta tikai viena vide konkrētam pārlūkpr. tipam.</span><span class="sxs-lookup"><span data-stu-id="edb15-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="edb15-122">Lietotāji var atvērt vairākas sesijas tajā pašā vidē (t.i., vairākas cilnes tajā pašā pārlūkprogr.).</span><span class="sxs-lookup"><span data-stu-id="edb15-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="edb15-123">Lietotājiem, kuri vienlaicīgi vēlas pārvietoties starp divām vidēm, ir jāatver katra vide, izmantojot citu pārlūkpr. tipu.</span><span class="sxs-lookup"><span data-stu-id="edb15-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="edb15-124">(Piemēram, lietotājs A var skatīt 1. vidi pārlūkprogrammā Chrome un 2. vidi pārlūkprogrammā Microsoft Edge.)</span><span class="sxs-lookup"><span data-stu-id="edb15-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
