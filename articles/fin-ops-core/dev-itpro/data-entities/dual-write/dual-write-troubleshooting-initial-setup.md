---
title: Problēmu novēršana sākotnējās iestatīšanas laikā
description: Šajā tēmā ir sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas var rasties, veicot sākotnējo iestatīšanu duālā ieraksta integrācijai.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2b75155aac12d79b9d68cce3e066acaaf80d6764
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380192"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Problēmu novēršana sākotnējās iestatīšanas laikā

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse. Konkrēti, šajā tēmā ir sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas var rasties, veicot sākotnējo iestatīšanu duālā ieraksta integrācijai.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Finance and Operations programmu nevar saistīt ar Dataverse

**Nepieciešamās lomas, lai iestatītu duālo rakstīšanu:** sistēmas administrators abās Finance and Operations lietojumprogrammās un Dataverse.

Kļūdas lapā **Iestatīt saiti uz Dataverse** parasti izraisa nepilnīgas iestatīšanas vai atļauju problēmas. Pārliecinieties, ka visa darbspējas pārbaude iet uz lapu **Iestatīt saiti uz Dataverse**, kā parādīts nākamajā attēlā. Nevarat saistīt duālo ierakstu, ja vien nav izieta pilnīga darbspējas pārbaude.

![Veiksmīga darbspējas pārbaude.](media/health_check.png)

Jums ir jābūt Azure AD nomnieka administratora akreditācijas datiem, lai saistītu Finance and Operations un Dataverse vides. Pēc vides saistīšanas lietotāji var pieteikties, izmantojot sava konta akreditācijas datus un atjauninot esošo tabulas karti.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Atrodiet ierobežojumu attiecībā uz to juridisko personu vai uzņēmumu skaitu, kurus var saistīt duālajam ierakstam

Mēģinot iespējot kartes, jūs varētu saņemt šādu kļūdas ziņojumu:

*Duālā ieraksta kļūda - spraudņa reģistrācija neizdevās: [(Nevar iegūt nodalījuma karti projektam DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Kļūda pārsniedz kartēšanai atļauto maksimālo nodalījumu skaitu DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], radās viena vai vairākas kļūdas.*

Saistot vides, pašreizējais ierobežojums ir aptuveni 40 juridiskās personas. Šī kļūda rodas, ja mēģināt iespējot kartes un starp vidēm ir saistītas vairāk nekā 40 juridiskās personas.

## <a name="connection-set-failed-while-linking-environment"></a>Saistot vidi, neizdevās iestatīt savienojumu

Saistot duālās rakstīšanas vidi, darbība neizdodas ar šādu kļūdas ziņojumu:

*Savienojuma kopas saglabāšana neizdevās! Vienums ar tādu pašu atslēgu jau ir pievienots.*

Duālais ieraksts neatbalsta vairākas juridiskas personas/uzņēmumus ar vienādu nosaukumu. Piemēram, ja jums ir divi uzņēmumi ar nosaukumu "DAT", Dataverse saņems šo kļūdas ziņojumu.

Lai atbloķētu debitoru, noņemiet Dataverse tabulā **cdm_company** esošos ierakstu dublikātus. Ari tad, ja tabulā **cdm_company** ir tukši ieraksti, noņemiet vai izlabojiet tos.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Atverot duālā ieraksta lapu Finance and Operations programmās, radās kļūda

Mēģinot saistīt Dataverse vidi duālajam ierakstam, jūs varētu saņemt šādu kļūdas ziņojumu:

*Atbildes statusa kods nenorāda uz veiksmi: 404 (nav atrasts)*

Šī kļūda rodas, ja programmas piekrišanas solis nav pabeigts. Varat pārbaudīt, vai ir sniegta atļauja, piesakoties `portal.azure.com`, izmantojot nomnieka administratora kontu, un pārbaudot, vai trešās puses programma ar ID `33976c19-1db5-4c02-810e-c243db79efde` ir redzama AAD uzņēmuma lietojumprogrammu sarakstā. Ja tā nav redzama, tad atkārtoti izpildiet atļaujas soli, kā aprakstīts nākamajā sadaļā.

### <a name="providing-app-consent"></a>Programmas atļaujas sniegšana

+ Atveriet tālāk minēto vietrādi URL, izmantojot administratora akreditācijas datus.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Atlasiet **Akceptēt**, lai akceptētu. Jūs dodat atļauju instalēt programmu (ar `id=33976c19-1db5-4c02-810e-c243db79efde`) nomniekā.
+ Šī programma ir nepieciešama, lai Dataverse varētu sazināties ar Finance and Operations programmām.

    ![Problēmu novēršana sākotnējās iestatīšanas laikā.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Ja tas nedarbojas, palaidiet vietrādi URL privātā režīmā pārlūkā Microsoft Edge vai inkognito režīmā pārlūkā Chrome.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finance and Operations vide nav atklājama

Jūs varētu saņemt šādu kļūdas ziņojumu:

*Finance and Operations programmu vide \*\*\* .cloudax.dynamics.com nav atklājama.*

Problēmai, kad vide nav atklājama, var būt divi iemesli.

+ Lietotājs, kurš tiek izmantots pieteikšanās laikā, nav tas pats nomnieks, kas Finance and Operations instancei.
+ Ir dažas mantotās Finance and Operations instances, kas bija Microsoft viesotas un kam bija problēma ar atklāšanu. Lai to labotu, atjauniniet Finance and Operations instanci. Vide kļūst atklājama ar jebkādu atjauninājumu.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
