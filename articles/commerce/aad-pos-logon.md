---
title: Iespējot Azure Active Directory autentifikāciju, lai pierakstītos POS
description: Šajā tēmā paskaidrots, kā konfigurēt Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) pierakstīšanās pieredzi, lai tā izmantotu Azure Active Directory autentifikāciju.
author: boycezhu
manager: annbe
ms.date: 03/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: dfc49585434383385b6b993893d93b95ef888384
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248944"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>Iespējot Azure Active Directory autentifikāciju, lai pierakstītos POS
[!include [banner](includes/banner.md)]


Daudzi klienti, kuri lieto Microsoft Dynamics 365 Commerce, izmanto arī citus Microsoft mākoņpakalpojumu pakalpojumus, un viņi var izmantot Azure Active Directory (Azure AD), lai pārvaldītu lietotāju akreditācijas datus šiem pakalpojumiem. Šādos gadījumos klienti varētu vēlēties izmantot vienu un to pašu Azure AD kontu dažādās lietojumprogrammās. Šajā tēmā paskaidrots, kā konfigurēt Commerce pārdošanas punkta (POS) pierakstīšanās pieredzi, lai izmantotu Azure AD autentifikāciju.

## <a name="configure-azure-ad-authentication"></a>Azure AD autentifikācijas konfigurēšana

Lai padarītu Azure AD pieejamu kā autentifikācijas metodi POS pierakstīšanās sistēmai veikalā, ir jākonfigurē veikala funkcionalitātes profila iestatījumi un pēc tam šie iestatījumi jāpiemēro POS klientiem.

Lai konfigurētu funkcionalitātes profilu, veiciet šādas darbības.

1. Dodieties uz sadaļu **Retail un Commerce** \> **Kanāla iestatīšana** \> **POS iestatīšana** \> **POS profili** \> **Funkcionalitātes profili**.
1. Atlasiet maināmo funkcionalitātes profilu.
1. Kopsavilkuma cilnes **Funkcijas** sadaļā **POS personāla pieteikšanās** mainiet lauka **Pieteikšanās autentifikācijas metodes** vērtību no **Personāla ID un parole** uz **Azure Active Directory**.

Pēc noklusējuma visi funkcionalitātes profili izmanto vērtību **Personāla ID un parole** kā POS autentifikācijas metodi. Tāpēc ir jāmaina lauka **Pieteikšanās autentifikācijas metode** vērtība, ja vēlaties lietot Azure AD. Visus mazumtirdzniecības veikalus, kas ir saistīti ar izvēlēto funkcionalitātes profilu, ietekmēs šīs izmaiņas.

Lai piemērotu iestatījumus POS klientiem, veiciet šīs darbības.

1. Pārejiet uz **Retail un Commerce** \> **Retail un Commerce IT** \> **Sadales grafiks**.
1. Palaidiet sadales grafiku **1070** (**Kanāla konfigurācija**).

> [!NOTE]
> Azure AD autentifikācijai ir nepieciešams interneta savienojums. Tā nedarbosies, ja POS būs bezsaistes režīmā.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Saistīt Azure AD kontu ar darbinieku

Pirms veikala darbinieks var izmantot Azure AD kontu, lai pieteiktos POS programmā, Azure AD kontam jābūt saistītam ar šo darbinieku.

Lai saistītu Azure AD kontu ar darbinieku, veiciet tālāk aprakstītās darbības.

1. Dodieties uz **Retail un Commerce** \> **Darbinieki** \> **Nodarbinātie**.
1. Atveriet darbinieka detalizētas informācijas lapu.
1. Darbību rūts cilnē **Commerce** grupā **Ārējā identitāte** atlasiet **Saistīt esošo identitāti**.
1. Dialoglodziņā **Izmantot esošo ārējo identitāti** atlasiet opciju **Meklēt, izmantojot e-pastu**, ievadiet Azure AD e-pasta adresi un pēc tam atlasiet **Meklēt**.
1. Atlasiet Azure AD kontu, kas tiek atgriezts, un pēc tam atlasiet **Labi**.

Darbinieka detalizētas informācijas lapas cilnē **Commerce** tiks ievadīti lauki **Aizstājvārds**, **UPN** un **Ārējais apakšidentifikators**.

## <a name="additional-resources"></a>Papildu resursi

[Paplašinātās pieteikšanās funkcionalitātes iestatīšana MPOS un Cloud POS](extended-logon.md)

[Izveidot mazumtirdzniecības funkcionalitātes profilu](retail-functionality-profile.md)

[ Nodarbinātā konfigurēšana](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
