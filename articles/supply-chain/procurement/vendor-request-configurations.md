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
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: d238e0dbb754e88dcffa171456aa0a2336238cab
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="vendor-request-configurations"></a><span data-ttu-id="52418-103">Piegādātāja pieprasījuma konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="52418-103">Vendor request configurations</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="52418-104">Lai izpildītu piegādātāja pieprasījumu, piegādātāja kontaktpersonai ir jāizpilda potenciālā piegādātāja reģistrēšanas vednis.</span><span class="sxs-lookup"><span data-stu-id="52418-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="52418-105">Formā **Piegādātāja pieprasījuma konfigurācijas** varat izveidot profilus, kas potenciālā piegādātāja reģistrācijas vednī norāda obligātos laukus un redzamos laukus.</span><span class="sxs-lookup"><span data-stu-id="52418-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="52418-106">Kreditora reģistrācijas vednis sākas, jautājot potenciālā piegādātāja lietotājam par valsti/reģionu, kurā piegādātājs darbojas.</span><span class="sxs-lookup"><span data-stu-id="52418-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="52418-107">Šī informācija nosaka piemērojamo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="52418-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="52418-108">Ja kādai valstij/reģionam nav definēta īpaša konfigurācija, tiek izmantota noklusējuma konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="52418-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="52418-109">Piegādātāja pieprasījuma konfigurācijas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="52418-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="52418-110">Kreditora konfigurācija pēc noklusējuma ir pieejama formā “Kreditora pieprasījuma konfigurācija”.</span><span class="sxs-lookup"><span data-stu-id="52418-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="52418-111">Noklusējuma konfigurācijai nav iespējams atlasīt valsti/reģionus, tādēļ sadaļu **Valstis/reģioni** nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="52418-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="52418-112">Noklikšķiniet uz **Sagāde un avoti** > **Iestatīšana** > **Kreditori** un pēc tam noklikšķiniet uz **Piegādātāja pieprasījuma konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="52418-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="52418-113">Noklikšķiniet uz cilnes **Lauki**, lai iestatītu uzskaitīto lauku statusu.</span><span class="sxs-lookup"><span data-stu-id="52418-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="52418-114">Slēpts (nav redzams)</span><span class="sxs-lookup"><span data-stu-id="52418-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="52418-115">Parādīts (redzams, bet nav obligāts)</span><span class="sxs-lookup"><span data-stu-id="52418-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="52418-116">Obligāts (redzams un obligāts)</span><span class="sxs-lookup"><span data-stu-id="52418-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="52418-117">Noklikšķiniet uz cilnes **Saturs**, lai norādītu, vai teksts būs redzams vednī un vai ir nepieciešams apliecinājums, ka potenciālā piegādātāja lietotājam ir jāsniedz piekrišana par šo, pirms notiek pāriešana uz nākamo vedņa posmu.</span><span class="sxs-lookup"><span data-stu-id="52418-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="52418-118">Apstiprinājums tiks pieprasīts par visiem noteikumiem un nosacījumiem, kas lietotājam ir jāpieņem, lai varētu turpināt.</span><span class="sxs-lookup"><span data-stu-id="52418-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="52418-119">Varat arī ievadīt apstiprinājuma ziņojumu, kas tiek parādīts, kad vednis ir pabeigts, un varat pievienot vienu vai vairākas anketas.</span><span class="sxs-lookup"><span data-stu-id="52418-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="52418-120">Piegādātāja konfigurācijas izveidošana noteiktai valstij/reģionam</span><span class="sxs-lookup"><span data-stu-id="52418-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="52418-121">Noklikšķiniet uz **Sagāde un avoti** > **Iestatīšana** > **Kreditori** un pēc tam noklikšķiniet uz **Piegādātāja pieprasījuma konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="52418-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="52418-122">Noklikšķiniet uz **Jauns**, lai izveidotu jaunu konfigurāciju, un norādiet šīs konfigurācijas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="52418-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="52418-123">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="52418-123">Click **Save**.</span></span>
4.  <span data-ttu-id="52418-124">Atveriet cilni **Valsts/reģioni**, lai atlasītu valsti/reģionu, kuriem šī konfigurācija ir jāizmanto.</span><span class="sxs-lookup"><span data-stu-id="52418-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="52418-125">Pabeidziet konfigurēšanu, ievērojot vadlīnijas par noklusējuma konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="52418-125">Complete the configuration by following the guidelines for the default configuration.</span></span>


