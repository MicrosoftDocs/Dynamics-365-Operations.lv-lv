---
title: Lietotāja neatrašana programmas Attract vai Onboard personu atlasītājā
description: Šajā tēmā ir paskaidrots, kā rīkoties, ja uzņēmuma nomnieka lietotāji netiek rādīti Dynamics 365 Talent - Attract vai Onboard personu atlasītājā.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
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
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d84dd9c22738a1b4fc5edb5331d4aa213b82facb
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551937"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a><span data-ttu-id="5c0da-103">Lietotāja neatrašana programmas Attract vai Onboard personu atlasītājā</span><span class="sxs-lookup"><span data-stu-id="5c0da-103">User not found in People Picker in Attract or Onboard</span></span>
[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="5c0da-104">Izejas plūsma</span><span class="sxs-lookup"><span data-stu-id="5c0da-104">Issue</span></span>

<span data-ttu-id="5c0da-105">Daži derīgi Microsoft Azure Active Directory (Azure AD) nomnieka lietotāji netiek parādīti, meklējot vārdu Dynamics 365 Talent: Attract vai Dynamics 365 Talent: Onboard personu atlasītājā.</span><span class="sxs-lookup"><span data-stu-id="5c0da-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in Dynamics 365 Talent: Attract or Dynamics 365 Talent: Onboard.</span></span>

## <a name="cause"></a><span data-ttu-id="5c0da-106">Iemesls</span><span class="sxs-lookup"><span data-stu-id="5c0da-106">Cause</span></span>

<span data-ttu-id="5c0da-107">Noteikti lietotāju tipi pašlaik netiek atbalstīti Attract un Onboard.</span><span class="sxs-lookup"><span data-stu-id="5c0da-107">Certain user types are not currently supported in Attract and Onboard.</span></span> <span data-ttu-id="5c0da-108">Pārbaudiet, vai lietotājs nav Azure AD biznesa biznesam (B2B) vieslietotājs.</span><span class="sxs-lookup"><span data-stu-id="5c0da-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="5c0da-109">Informācija par lietotāja viedu ir pieejama Azure portāla panelī Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5c0da-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="5c0da-110">Papildinformāciju par Azure B2B skatiet rakstā [Par vieslietotāja piekļuvi Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="5c0da-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="5c0da-111">Ja lietotājs nav B2B lietotājs, viņam, iespējams, ir iestatīts nepilnīgs objekta **Lietotājs** rekvizīts Lietotāja veids.</span><span class="sxs-lookup"><span data-stu-id="5c0da-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="5c0da-112">To var pārbaudīt un novērst, izmantojot moduli Azure AD Powershell.</span><span class="sxs-lookup"><span data-stu-id="5c0da-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="5c0da-113">Lai iegūtu papildus informāciju, skatiet [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="5c0da-113">For more information, see [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="5c0da-114">Novēršana</span><span class="sxs-lookup"><span data-stu-id="5c0da-114">Resolution</span></span>

<span data-ttu-id="5c0da-115">Lai veiktu tālāk norādītās darbības un novērstu problēmu, jums ir vajadzīgas lomas Globālais administrators atļaujas Azure Active Directory nomniekā vai atļaujas **User.ReadWrite.All**.</span><span class="sxs-lookup"><span data-stu-id="5c0da-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="5c0da-116">Lai pārbaudītu ietekmētā lietotāja rekvizītu Lietotāja veids.</span><span class="sxs-lookup"><span data-stu-id="5c0da-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="5c0da-117">Komanda atgriež tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="5c0da-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="5c0da-118">Pievērsiet uzmanību lietotāja rekvizītam **UserType**.</span><span class="sxs-lookup"><span data-stu-id="5c0da-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="5c0da-119">Ja rekvizīts **UserType** ir tukšs, piemēram, tā vērtība nav Dalībnieks vai Viesis, atjauniniet rekvizītu **UserType**, izmantojot tālāk norādīto komandu.</span><span class="sxs-lookup"><span data-stu-id="5c0da-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
