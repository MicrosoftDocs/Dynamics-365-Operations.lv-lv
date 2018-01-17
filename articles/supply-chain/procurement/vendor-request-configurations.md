---
title: "Piegādātāja pieprasījuma konfigurācijas"
description: "Šajā tēmā ir aprakstīti lauki, kuri jaunā piegādātāja pieprasījumā ir jāaizpilda obligāti."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 57297a5798004f959a53513b88750866083beee7
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---

# <a name="vendor-request-configurations"></a><span data-ttu-id="e6969-103">Piegādātāja pieprasījuma konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="e6969-103">Vendor request configurations</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="e6969-104">Lai izpildītu piegādātāja pieprasījumu, piegādātāja kontaktpersonai ir jāizpilda potenciālā piegādātāja reģistrēšanas vednis.</span><span class="sxs-lookup"><span data-stu-id="e6969-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="e6969-105">Formā **Piegādātāja pieprasījuma konfigurācijas** varat izveidot profilus, kas potenciālā piegādātāja reģistrācijas vednī norāda obligātos laukus un redzamos laukus.</span><span class="sxs-lookup"><span data-stu-id="e6969-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="e6969-106">Kreditora reģistrācijas vednis sākas, jautājot potenciālā piegādātāja lietotājam par valsti/reģionu, kurā piegādātājs darbojas.</span><span class="sxs-lookup"><span data-stu-id="e6969-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="e6969-107">Šī informācija nosaka piemērojamo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="e6969-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="e6969-108">Ja kādai valstij/reģionam nav definēta īpaša konfigurācija, tiek izmantota noklusējuma konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="e6969-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="e6969-109">Piegādātāja pieprasījuma konfigurācijas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e6969-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="e6969-110">Kreditora konfigurācija pēc noklusējuma ir pieejama formā “Kreditora pieprasījuma konfigurācija”.</span><span class="sxs-lookup"><span data-stu-id="e6969-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="e6969-111">Noklusējuma konfigurācijai nav iespējams atlasīt valsti/reģionus, tādēļ sadaļu **Valstis/reģioni** nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="e6969-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1.  <span data-ttu-id="e6969-112">Noklikšķiniet uz **Sagāde un avoti** > **Iestatīšana** > **Kreditori** un pēc tam noklikšķiniet uz **Piegādātāja pieprasījuma konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="e6969-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="e6969-113">Noklikšķiniet uz cilnes **Lauki**, lai iestatītu uzskaitīto lauku statusu.</span><span class="sxs-lookup"><span data-stu-id="e6969-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
-   <span data-ttu-id="e6969-114">Slēpts (nav redzams)</span><span class="sxs-lookup"><span data-stu-id="e6969-114">Hidden (Not visible)</span></span>
-   <span data-ttu-id="e6969-115">Parādīts (redzams, bet nav obligāts)</span><span class="sxs-lookup"><span data-stu-id="e6969-115">Displayed (Visible but not mandatory)</span></span>
-   <span data-ttu-id="e6969-116">Obligāts (redzams un obligāts)</span><span class="sxs-lookup"><span data-stu-id="e6969-116">Required (Visible and mandatory)</span></span>
3.  <span data-ttu-id="e6969-117">Noklikšķiniet uz cilnes **Saturs**, lai norādītu, vai teksts būs redzams vednī un vai ir nepieciešams apliecinājums, ka potenciālā piegādātāja lietotājam ir jāsniedz piekrišana par šo, pirms notiek pāriešana uz nākamo vedņa posmu.</span><span class="sxs-lookup"><span data-stu-id="e6969-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="e6969-118">Apstiprinājums tiks pieprasīts par visiem noteikumiem un nosacījumiem, kas lietotājam ir jāpieņem, lai varētu turpināt.</span><span class="sxs-lookup"><span data-stu-id="e6969-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="e6969-119">Varat arī ievadīt apstiprinājuma ziņojumu, kas tiek parādīts, kad vednis ir pabeigts, un varat pievienot vienu vai vairākas anketas.</span><span class="sxs-lookup"><span data-stu-id="e6969-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="e6969-120">Piegādātāja konfigurācijas izveidošana noteiktai valstij/reģionam</span><span class="sxs-lookup"><span data-stu-id="e6969-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="e6969-121">Noklikšķiniet uz **Sagāde un avoti** > **Iestatīšana** > **Kreditori** un pēc tam noklikšķiniet uz **Piegādātāja pieprasījuma konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="e6969-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="e6969-122">Noklikšķiniet uz **Jauns**, lai izveidotu jaunu konfigurāciju, un norādiet šīs konfigurācijas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e6969-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="e6969-123">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e6969-123">Click **Save**.</span></span>
4.  <span data-ttu-id="e6969-124">Atveriet cilni **Valsts/reģioni**, lai atlasītu valsti/reģionu, kuriem šī konfigurācija ir jāizmanto.</span><span class="sxs-lookup"><span data-stu-id="e6969-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="e6969-125">Pabeidziet konfigurēšanu, ievērojot vadlīnijas par noklusējuma konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="e6969-125">Complete the configuration by following the guidelines for the default configuration.</span></span>


