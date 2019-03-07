---
title: Lietotāja neatrašana programmas Attract vai Onboard personu atlasītājā
description: Šajā tēmā ir paskaidrots, kā rīkoties, ja uzņēmuma nomnieka lietotāji netiek rādīti lietojumprogrammas Dynamics 365 for Talent Attract vai Onboard personu atlasītājā.
author: ChrisChua
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: chrichua
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2d4a74ee2cc65153c1f9fdc1b42c2fc440d188d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305376"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>Azure Active Directory lietotāju neatrašana personu atlasītājā

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Izejas plūsma

Daži derīgi Microsoft Azure Active Directory (Azure AD) nomnieka lietotāji netiek parādīti, meklējot vārdu lietojumprogrammas Dynamics 365 for Talent Attract vai Onboard personu atlasītājā.

## <a name="cause"></a>Iemesls

Noteikti lietotāju tipi pašlaik netiek atbalstīti lietojumprogrammās Attract un Onboard. Pārbaudiet, vai lietotājs nav Azure AD biznesa biznesam (B2B) vieslietotājs. Informācija par lietotāja viedu ir pieejama Azure portāla panelī Azure Active Directory.

Papildinformāciju par Azure B2B skatiet rakstā [Par vieslietotāja piekļuvi Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).

Ja lietotājs nav B2B lietotājs, viņam, iespējams, ir iestatīts nepilnīgs objekta **Lietotājs** rekvizīts Lietotāja veids. To var pārbaudīt un novērst, izmantojot moduli Azure AD Powershell. Lai iegūtu papildus informāciju, skatiet [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).

## <a name="resolution"></a>Novēršana

Lai veiktu tālāk norādītās darbības un novērstu problēmu, jums ir vajadzīgas lomas Globālais administrators atļaujas Azure Active Directory nomniekā vai atļaujas **User.ReadWrite.All**.

Lai pārbaudītu ietekmētā lietotāja rekvizītu Lietotāja veids.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
Komanda atgriež tālāk norādīto informāciju.
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Pievērsiet uzmanību lietotāja rekvizītam **UserType**. Ja rekvizīts **UserType** ir tukšs, piemēram, tā vērtība nav Dalībnieks vai Viesis, atjauniniet rekvizītu **UserType**, izmantojot tālāk norādīto komandu.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```