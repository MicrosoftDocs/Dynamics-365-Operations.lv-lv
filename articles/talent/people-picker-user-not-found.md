---
title: Lietotāja neatrašana programmas Attract vai Onboard personu atlasītājā
description: Šajā tēmā ir paskaidrots, kā rīkoties, ja uzņēmuma nomnieka lietotāji netiek rādīti lietojumprogrammas Dynamics 365 for Talent Attract vai Onboard personu atlasītājā.
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
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "859509"
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
