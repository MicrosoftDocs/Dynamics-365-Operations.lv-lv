---
title: Regulatory Configuration Service
description: Šajā tēmā sniegts pārskats par Regulatory Configuration Service (RCS) iespējām un skaidrots, kā piekļūt šim pakalpojumam.
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216566"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) ir savrups veidotājs un dzīves cikla pārvaldības pakalpojums bezkoda/zema koda globalizācijas funkcionalitātei. RCS ļauj globalizācijas ieinteresētajām personām paplašināt un pielāgot galvenās globalizācijas jomas, proti, nodokļu, e-rēķinu, regulatīvo ziņojumu, banku un uzņēmējdarbības dokumentus, nepiesaistot izstrādātājus. Šī bezkoda/zema koda globalizācijas pieeja padara globalizāciju vieglāku, ātrāku un izmaksu ziņā efektīvāku, lai to izveidotu vai paplašinātu.

RCS nodrošina šādas iespējas:

- Atbalsts visai funkcionalitātei, ko nodrošina elektronisko pārskatu izrakstīšana (ER).
- Jaunu globalizācijas mikropakalnu konfigurēšanas priekšnosacījums.
- Atbalsts elektroniskajai rēķinu izrakstīšanai. Plašāku informāciju skatiet [Elektronisko rēķinu izrakstīšana](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Atbalsts nodokļu aprēķināšanai. Papildinformāciju skatiet sadaļā [Nodokļu pakalpojums](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Atbalsts jaunajai globalizācijas līdzekļa funkcionalitātei, kas vienkāršo vairāku komponentu līdzekļu dzīves cikla pārvaldību un nodrošina papildu spēju konfigurēt darbības un iestatīt funkcionalitātes parametrus. Plašāku informāciju skatiet [Regulatory Configuration Service - vienkāršota globalizācijas līdzekļu pārvaldība globalizācijas pakalpojumiem](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Atbalsts pielāgotu konfigurāciju centralizētai publicēšanai, uzglabāšanai un koplietošanai globālajā repozitorijā, lai atvieglotu konfigurācijas pārvaldību, neprasot Microsoft Dynamics Lifecycle Services (LCS) lietošanu.

## <a name="access-rcs"></a>Piekļuve RCS

Varat pierakstīties uz RCS vai pieteikties RCS no [Regulatory Configuration Service lapas](https://marketing.configure.global.dynamics.com/).

![Pierakstīties/pieteikties RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

Lapā **Regulatory Configuration Service** pārskatiet un akceptējiet pakalpojuma papildu noteikumus un nosacījumus un pēc tam atlasiet vienu no šīm pogām:

- **Pierakstīties**, ja esat pakalpojuma pirmreizējs lietotājs un izmantojat uzņēmuma e-pasta adresi, lai nodrošinātu uzņēmumam pakalpojumu vidi
- **Pieteikties**, ja iepriekš esat pierakstījies pakalpojumam un vēlaties piekļūt savas organizācijas videi

## <a name="regional-availability"></a>Reģionālā pieejamība

RCS ir pieejams šādos reģionos:

- ASV
- Indija
- Francija
- Eiropa

Pilnīgu reģionu sarakstu skatiet [Dynamics 365 un Power Platform: pieejamība, datu atrašanās vieta, valoda un lokalizācija](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="rcs-default-company"></a>RCS noklusējuma uzņēmums

Noformēšanas laika funkcionalitāte, kas tiek izmantota RCS, tiek koplietota visos uzņēmumos. Nav uzņēmumam raksturīgu funkcionalitāšu. Tāpēc ieteicams izmantot vienu uzņēmumu, **DAT** ar savu RCS vidi.

Tomēr dažos scenārijos, iespējams, vēlēsities izveidot ER formātus, izmantojot parametrus, kas saistīti ar noteiktu juridisku personu. Tikai šajos scenārijos ir jāizmanto noklusējuma uzņēmuma pārslēdzējs. Piemēru skatiet sadaļā [Elektronisko pārskatu formātu konfigurēšana, lai izmantotu parametrus, kas norādīti juridiskajai personai](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).

## <a name="related-rcs-documentation"></a>Saistītā RCS dokumentācija

Papildinformāciju par saistītiem komponentiem skatiet tālāk norādītajās tēmās.

- **RCS:**

    - [Elektronisko pārskatu konfigurāciju izveide pakalpojumā RCS un to augšupielāde globālajā repozitorijā](rcs-global-repo-upload.md)

- **Globālais repozitorijs:**

    - [Izveidot ER konfigurāciju & augšupielādēt globālajā repozitorijā](rcs-global-repo-upload.md)
    - [Kopīgot konfigurāciju globālajā repozitorijā](rcs-global-repo-share-configuration.md)
    - [Uzlabota filtrēšana globālajā repozitorijā](enhanced-filtering-global-repo.md)
    - [Elektronisko pārskatu konfigurāciju lejupielāde no globālā repozitorija](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Pārtraukt konfigurācijas globālajā repozitorijā](discontinuing-configurations-rcs-global-repo.md)
    - [Regulatory Configuration Service (RCS) — Lifecycle Services (LCS) krātuves nolietojums](rcs-lcs-repo-dep-faq.md)

- **Globalizācijas līdzeklis:**

    - [Regulatory Configuration Service (RCS) — globalizācijas līdzeklis](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>RCS reģistrēšanās problēmu novēršana

Pierakstoties RCS no pakalpojuma lapas, varat saskarties ar problēmu, kas ir saistīta ar Azure Active Directory (Azure AD). Saņemtais kļūdas ziņojums norāda, ka pierakstīšanās RCS pašlaik ir izslēgta un tā ir jāieslēdz pirms pierakstīšanās procesa pabeigšanas.

![RCS pierakstīšanās procesa kļūdas ziņojums](media/01_RCSSignUpError.jpg)

Problēma rodas, jo esat bloķēts pierakstīties ekspromta abonementiem, un šim `AllowAdHocSubscriptions` rekvizītam ir jābūt iespējotam nomniekā. 

- Ja IT nodaļa pārvalda jūsu organizācijas Azure nomniekus, sazinieties ar šo nodaļu, lai ziņotu par problēmu.
- Ja pats esat atbildīgs par Azure nomnieku pārvaldību, tad varat novērst problēmas, izpildot darbības, kas norādītas sadaļā [Kas ir patstāvīgi izmantojama pierakstīšanās Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).
