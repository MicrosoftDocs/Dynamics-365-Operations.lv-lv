---
title: Sākotnējās izvietošanas laikā Commerce vietnes veidotājā nevar konfigurēt drošības grupu
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad Microsoft Azure Active Directory (Azure AD) drošības grupa Commerce vietnes veidotājam neparādās kā opcija, kad izveidojat e-komercijas komponentus Microsoft Dynamics Lifecycle Services (LCS) jauna e-komercijas nomnieka sākotnējās izvietošanas laikā.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585432"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="75441-103">Sākotnējās izvietošanas laikā Commerce vietnes veidotājā nevar konfigurēt drošības grupu</span><span class="sxs-lookup"><span data-stu-id="75441-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75441-104">Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad Microsoft Azure Active Directory (Azure AD) drošības grupa Commerce vietnes veidotājam neparādās kā opcija, kad izveidojat e-komercijas komponentus Microsoft Dynamics Lifecycle Services (LCS) jauna e-komercijas nomnieka sākotnējās izvietošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="75441-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="75441-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="75441-105">Description</span></span>

<span data-ttu-id="75441-106">Kad izveidojat e-komercijas komponentus kā daļu no jauna e-komercijas nomnieka, kas ietver Commerce vietnes veidotāja komponentu, izvietošanas procesa ietvaros drošības grupa neparādīsies kā Azure AD opcija dialoglodziņā.</span><span class="sxs-lookup"><span data-stu-id="75441-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="75441-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="75441-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="75441-108">E-komercijas vietnes nodrošināšana ar lietotāju pareizajā nomniekā</span><span class="sxs-lookup"><span data-stu-id="75441-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="75441-109">Dodieties uz [Azure portālu](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="75441-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="75441-110">Zem nomnieka, kam tika nodrošināts LCS projekts jūsu e-komercijas vietnei, izpildiet norādes sadaļā [Pamata grupas izveide un dalībnieku pievienošana, izmantojot Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="75441-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="75441-111">Dodieties uz [LCS](https://lcs.dynamics.com/) un pierakstieties, izmantojot kontu, kam ir tāds pats nomnieks kā Azure AD drošības grupai, kuru tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="75441-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="75441-112">Kontam jābūt piekļuvei, lai skatītu Azure AD drošības grupu.</span><span class="sxs-lookup"><span data-stu-id="75441-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="75441-113">Izpildiet iestatīšanas darbības, lai konfigurētu e-komercijas vietni.</span><span class="sxs-lookup"><span data-stu-id="75441-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="75441-114">Izveidojot e-komercijas komponentus, drošības grupai tagad ir jāparādās kā opcijai dialoglodziņā.</span><span class="sxs-lookup"><span data-stu-id="75441-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="75441-115">Lai nodrošinātu, ka lauks dialoglodziņā ir aizpildīts ar drošības grupu sarakstu, jums jāatlasa **Ievadīt**, kad esat ievadījis izveidotās Azure AD drošības grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="75441-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="75441-116">Meklēšanas rezultātos tiks uzskaitītas visas Azure AD drošības grupas, kuras sākas ar meklēšanas tekstu un kurām lietotājam ir piekļuve.</span><span class="sxs-lookup"><span data-stu-id="75441-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="75441-117">Lai panāktu plašākus meklēšanas rezultātus, varat izmantot īsāku meklējamo terminu.</span><span class="sxs-lookup"><span data-stu-id="75441-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75441-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="75441-118">Additional resources</span></span>

[<span data-ttu-id="75441-119">Pamatgrupas izveide un dalībnieku pievienošana, izmantojot Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="75441-119">Create a basic group and add members using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="75441-120">Jauna e-komercijas nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="75441-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)