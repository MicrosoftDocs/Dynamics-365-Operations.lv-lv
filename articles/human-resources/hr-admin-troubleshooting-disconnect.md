---
title: Debitora atvienošanās
description: Šajā rakstā paskaidrots, kā rīkoties, ja debitors tiek atvienots no vides un nav zināms, kāpēc.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: d02916283bbd4cee6502942020df1b275a0242b3
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113439"
---
# <a name="client-disconnects"></a><span data-ttu-id="2354d-103">Debitora atvienošanās</span><span class="sxs-lookup"><span data-stu-id="2354d-103">Client disconnects</span></span>

<span data-ttu-id="2354d-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="2354d-104">**Environment details**</span></span> 

<span data-ttu-id="2354d-105">Šāda problēma var rasties visās vidēs.</span><span class="sxs-lookup"><span data-stu-id="2354d-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="2354d-106">**Simptoms**</span><span class="sxs-lookup"><span data-stu-id="2354d-106">**Symptom**</span></span> 

<span data-ttu-id="2354d-107">Debitors tiek atvienots no vides un nav zināms, kāpēc.</span><span class="sxs-lookup"><span data-stu-id="2354d-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="2354d-108">Debitors saņem vienu no šādiem kļūdu ziņojumiem:</span><span class="sxs-lookup"><span data-stu-id="2354d-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="2354d-109">Savienojums tika zaudēts.</span><span class="sxs-lookup"><span data-stu-id="2354d-109">We've lost your connection.</span></span> <span data-ttu-id="2354d-110">Nokl. uz Aizv., lai turp. darbu.</span><span class="sxs-lookup"><span data-stu-id="2354d-110">Click Close to continue working.</span></span>
- <span data-ttu-id="2354d-111">Šķiet, ka ir zaudēts savienojums ar tīklu; lai mēģinātu vēlreiz, noklikšķiniet uz Mēģināt vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="2354d-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="2354d-112">**Sarkans karodziņš**</span><span class="sxs-lookup"><span data-stu-id="2354d-112">**Red flag**</span></span>

<span data-ttu-id="2354d-113">Šī problēma parasti rodas, ja lietotāji ir ieviešanas posmā, salīdzina informāciju ražošanas un testēšanas vidēs un aizmirst, ka tie pārslēdzas starp sesijām.</span><span class="sxs-lookup"><span data-stu-id="2354d-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="2354d-114">Ja lietotāji ir šajā posmā, viņiem, visticamāk, rodas šī problēmu.</span><span class="sxs-lookup"><span data-stu-id="2354d-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="2354d-115">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="2354d-115">**Issue**</span></span> 

<span data-ttu-id="2354d-116">**Pārlūkprogrammu veidi:** Google Chrome, Internet Explorer un Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2354d-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="2354d-117">Lietotāji tiek atvienoti no Microsoft Dynamics 365 Human Resources, ja vienlaicīgi ir atvērtas divas dažādas sesijas ar vienu un to pašu lietotāju un vienu un to pašu pārlūkprogrammas veidu.</span><span class="sxs-lookup"><span data-stu-id="2354d-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="2354d-118">(Piemēram, lietotājs A skata gan 1. vidi, gan 2. vidi pārlūkprogrammā Chrome.) Nav svarīgi, vai lietotāji atver citus pārlūkprogrammas logus vai dažādas cilnes.</span><span class="sxs-lookup"><span data-stu-id="2354d-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="2354d-119">Ja tiek izmantoti tie paši lietotāja akreditācijas dati, lai vienlaicīgi pierakstītos gan 1. vidē, gan 2. vidē un tā paša veida pārlūkprogrammā, Human Resources atvieno vienu no sesijām.</span><span class="sxs-lookup"><span data-stu-id="2354d-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="2354d-120">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="2354d-120">**Solution**</span></span>

<span data-ttu-id="2354d-121">Pārliec., ka vienlaicīgi ir atvērta tikai viena vide konkrētam pārlūkpr. tipam.</span><span class="sxs-lookup"><span data-stu-id="2354d-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="2354d-122">Lietotāji var atvērt vairākas sesijas tajā pašā vidē (t.i., vairākas cilnes tajā pašā pārlūkprogr.).</span><span class="sxs-lookup"><span data-stu-id="2354d-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="2354d-123">Lietotājiem, kuri vienlaicīgi vēlas pārvietoties starp divām vidēm, ir jāatver katra vide, izmantojot citu pārlūkpr. tipu.</span><span class="sxs-lookup"><span data-stu-id="2354d-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="2354d-124">(Piemēram, lietotājs A var skatīt 1. vidi pārlūkprogrammā Chrome un 2. vidi pārlūkprogrammā Microsoft Edge.)</span><span class="sxs-lookup"><span data-stu-id="2354d-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
