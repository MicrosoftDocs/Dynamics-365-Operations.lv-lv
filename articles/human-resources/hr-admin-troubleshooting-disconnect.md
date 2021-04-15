---
title: Debitora atvienošanās
description: Šajā rakstā paskaidrots, kā rīkoties, ja debitors tiek atvienots no vides un nav zināms, kāpēc.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e9ec43ad0a7d121eb247d81d4b506556a0fa2214
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794905"
---
# <a name="client-disconnects"></a><span data-ttu-id="e7083-103">Debitora atvienošanās</span><span class="sxs-lookup"><span data-stu-id="e7083-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e7083-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="e7083-104">**Environment details**</span></span> 

<span data-ttu-id="e7083-105">Šāda problēma var rasties visās vidēs.</span><span class="sxs-lookup"><span data-stu-id="e7083-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="e7083-106">**Simptoms**</span><span class="sxs-lookup"><span data-stu-id="e7083-106">**Symptom**</span></span> 

<span data-ttu-id="e7083-107">Debitors tiek atvienots no vides un nav zināms, kāpēc.</span><span class="sxs-lookup"><span data-stu-id="e7083-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="e7083-108">Debitors saņem vienu no šādiem kļūdu ziņojumiem:</span><span class="sxs-lookup"><span data-stu-id="e7083-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="e7083-109">Savienojums tika zaudēts.</span><span class="sxs-lookup"><span data-stu-id="e7083-109">We've lost your connection.</span></span> <span data-ttu-id="e7083-110">Nokl. uz Aizv., lai turp. darbu.</span><span class="sxs-lookup"><span data-stu-id="e7083-110">Click Close to continue working.</span></span>
- <span data-ttu-id="e7083-111">Šķiet, ka ir zaudēts savienojums ar tīklu; lai mēģinātu vēlreiz, noklikšķiniet uz Mēģināt vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="e7083-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="e7083-112">**Sarkans karodziņš**</span><span class="sxs-lookup"><span data-stu-id="e7083-112">**Red flag**</span></span>

<span data-ttu-id="e7083-113">Šī problēma parasti rodas, ja lietotāji ir ieviešanas posmā, salīdzina informāciju ražošanas un testēšanas vidēs un aizmirst, ka tie pārslēdzas starp sesijām.</span><span class="sxs-lookup"><span data-stu-id="e7083-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="e7083-114">Ja lietotāji ir šajā posmā, viņiem, visticamāk, rodas šī problēmu.</span><span class="sxs-lookup"><span data-stu-id="e7083-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="e7083-115">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="e7083-115">**Issue**</span></span> 

<span data-ttu-id="e7083-116">**Pārlūkprogrammu veidi:** Google Chrome, Internet Explorer un Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e7083-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="e7083-117">Lietotāji tiek atvienoti no Microsoft Dynamics 365 Human Resources, ja vienlaicīgi ir atvērtas divas dažādas sesijas ar vienu un to pašu lietotāju un vienu un to pašu pārlūkprogrammas veidu.</span><span class="sxs-lookup"><span data-stu-id="e7083-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="e7083-118">(Piemēram, lietotājs A skata gan 1. vidi, gan 2. vidi pārlūkprogrammā Chrome.) Nav svarīgi, vai lietotāji atver citus pārlūkprogrammas logus vai dažādas cilnes.</span><span class="sxs-lookup"><span data-stu-id="e7083-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="e7083-119">Ja tiek izmantoti tie paši lietotāja akreditācijas dati, lai vienlaicīgi pierakstītos gan 1. vidē, gan 2. vidē un tā paša veida pārlūkprogrammā, Human Resources atvieno vienu no sesijām.</span><span class="sxs-lookup"><span data-stu-id="e7083-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="e7083-120">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="e7083-120">**Solution**</span></span>

<span data-ttu-id="e7083-121">Pārliec., ka vienlaicīgi ir atvērta tikai viena vide konkrētam pārlūkpr. tipam.</span><span class="sxs-lookup"><span data-stu-id="e7083-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="e7083-122">Lietotāji var atvērt vairākas sesijas tajā pašā vidē (t.i., vairākas cilnes tajā pašā pārlūkprogr.).</span><span class="sxs-lookup"><span data-stu-id="e7083-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="e7083-123">Lietotājiem, kuri vienlaicīgi vēlas pārvietoties starp divām vidēm, ir jāatver katra vide, izmantojot citu pārlūkpr. tipu.</span><span class="sxs-lookup"><span data-stu-id="e7083-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="e7083-124">(Piemēram, lietotājs A var skatīt 1. vidi pārlūkprogrammā Chrome un 2. vidi pārlūkprogrammā Microsoft Edge.)</span><span class="sxs-lookup"><span data-stu-id="e7083-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]