---
title: Problēmu novēršana sākotnējās iestatīšanas laikā
description: Šajā tēmā ir sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas var rasties, veicot sākotnējo iestatīšanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 76e104c9ebd7db7ebcbaf214e84be6c4353e8a73
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275445"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Problēmu novēršana sākotnējās iestatīšanas laikā

[!include [banner](../../includes/banner.md)]



Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service. Konkrēti, šajā tēmā ir sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas var rasties, veicot sākotnējo iestatīšanu duālā ieraksta integrācijai.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a>Finance and Operations programmu nevar saistīt ar Common Data Service

**Nepieciešamās lomas, lai iestatītu duālo rakstīšanu:** sistēmas administrators abās Finance and Operations lietojumprogrammās un Common Data Service.

Kļūdas lapā **Iestatīt saiti uz Common Data Service** parasti izraisa nepilnīgas iestatīšanas vai atļauju problēmas. Pārliecinieties, ka visa darbspējas pārbaude iet uz lapu **Iestatīt saiti uz Common Data Service**, kā parādīts nākamajā attēlā. Nevarat saistīt duālo ierakstu, ja vien nav izieta pilnīga darbspējas pārbaude.

![Veiksmīga darbspējas pārbaude](media/health_check.png)

Jums ir jābūt Azure AD nomnieka administratora akreditācijas datiem, lai saistītu Finance and Operations un Common Data Service vides. Pēc vides saistīšanas lietotāji var pieteikties, izmantojot sava konta akreditācijas datus un atjauninot esošo elementa karti.

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a>Kļūda, atverot saiti uz Common Data Service lapu

**Nepieciešamie akreditācijas dati problēmas novēršanai:** Azure AD nomnieka administrators

Atverot lapu **Saite uz Common Data Service** programmā Finance and Operations, jūs varētu saņemt šādu kļūdas ziņojumu:

*Atbildes statusa kods nenorāda uz veiksmi: 404 (nav atrasts)*

Šī kļūda rodas, ja piekrišanas solis nav pabeigts. Lai pārbaudītu, vai piekrišanas darbība ir izpildīta, piesakieties portal.Azure.com, izmantojot Azure AD nomnieka administratora kontu, un skatiet, vai trešās puses programma, kurai ir ID **33976c19-1db5-4c02-810e-c243db79efde**, parādās Azure AD sarakstā **Uzņēmuma lietojumprogrammas**. Ja tā nenotiek, jums ir jāsniedz programmas piekrišana.

Lai nodrošinātu programmas piekrišanu, veiciet tālāk norādītās darbības.

1. Atveriet šo vietrādi URL, izmantojot administratora akreditācijas datus. Jūs virzīs uz piekrišanas sniegšanu.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Atlasiet **Piekrist**, lai norādītu, ka dodat piekrišanu savā nomniekā instalēt programmu, kuras ID ir **33976c19-1db5-4c02-810e-c243db79efde**.

    > [!TIP]
    > Šī programma ir nepieciešama, lai Common Data Service saistītu ar Finance and Operations programmām. Ja rodas problēmas ar šo darbību, atveriet pārlūkprogrammu inkognito režīmā (pārlūkā Google Chrome) vai InPrivate režīmā (in Microsoft Edge).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Pārbaudiet, vai uzņēmuma datu un duālā ieraksta komandas saistīšanas laikā ir pareizi iestatītas.

Lai nodrošinātu, ka duālais ieraksts darbojas pareizi, uzņēmumi, kurus atlasāt konfigurēšanas laikā, tiek izveidoti Common Data Service vidē. Pēc noklusējuma šie uzņēmumi ir tikai lasāmi un rekvizīts **IsDualWriteEnable** ir iestatīts uz **True**. Turklāt tiek izveidots noklusējuma piederošās biznesa vienība īpašnieks un komanda un ietverts uzņēmuma nosaukums. Pirms iespējojat kartes, pārbaudiet, vai ir norādīts noklusējuma grupas īpašnieks. Lai atrastu elementu **Uzņēmumi (CDM\_uzņēmums)**, veiciet tālāk norādītās darbības.

1. Modeļa vadītā programmā pakalpojumā Dynamics 365 augšējā labajā stūrī atlasiet filtru.
2. Nolaižamajā sarakstā atlasiet **Uzņēmums**.
3. Atlasiet **Palaist**, lai skatītu rezultātus.
4. Atlasiet uzņēmumu, kas bija saistīts, konfigurējot duālo ierakstu.
5. Pārbaudiet, vai laukam **Noklusējuma atbildīgā grupa** ir vērtība. Šajā attēlā lauks **Noklusējuma atbildīgā grupa** ir iestatīts uz **USMF Dual Write**.

    ![Noklusējuma atbildīgās grupas pārbaude](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a>Atrodiet ierobežojumu attiecībā uz to juridisko personu vai uzņēmumu skaitu, kurus var saistīt duālajam ierakstam

Mēģinot iespējot kartes, jūs varētu saņemt šādu kļūdas ziņojumu:

*Duālā ieraksta kļūda - Spraudņa reģistrācija neizdevās: \[(Nevar iegūt nodalījuma karti projektam DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-.7f12cb89-1550-42e2-858e-4761fc1443ea Kļūda pārsniedz kartēšanai atļauto maksimālo nodalījumu skaitu DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Radās viena vai vairākas kļūdas*

Saistot vides, pašreizējais ierobežojums ir aptuveni 40 juridiskās personas. Šī kļūda rodas, ja mēģināt iespējot kartes un starp vidēm ir saistītas vairāk nekā 40 juridiskās personas.
