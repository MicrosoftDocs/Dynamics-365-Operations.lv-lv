---
title: Tukšs nodokļu līdzekļu saraksts nodokļu aprēķina parametros
description: Šajā tēmā skaidrots, kā novērst problēmu, kad nodokļu funkciju saraksts lapā Nodokļu aprēķina parametri ir tukšs.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: ef8158c2ada18e7d132eebbedef559b3f80ab19f
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612294"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Tukšs nodokļu līdzekļu saraksts nodokļu aprēķina parametros

[!include [banner](../includes/banner.md)]


## <a name="symptom"></a>Simptoms

Esat publicējis līdzekli regulēšanas konfigurācijas pakalpojumā (RCS), lai to varētu izmantot Microsoft Dynamics 365 Finanses. Tomēr, atverot finanses, **·** \> **·** \> **·** \> **dodieties uz nodokļu iestatījumu nodokļa konfigurācijas nodokļa aprēķina** **parametrus un mēģiniet atlasīt vērtību laukā Līdzekļa iestatījuma** nosaukums, vērtību saraksts ir tukšs.

## <a name="reason"></a>Pamatojums

Šī problēma parasti rodas, jo finanšu vide un RCS vide nav zem viena un tā paša nomnieka.

### <a name="rcs-tenant"></a>RCS nomnieks

Izpildiet šīs darbības, lai atrastu sava RCS nomnieka ID.

1. Kopējiet pilnu RCS URL. Piemēram, URL varētu būt `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. Atveriet InPrivate pārlūka logu, ielīmēt RCS URL adreses joslā un pēc tam atlasiet **Ievadīt**. Jūs esat novirzīts uz pierakstīšanās lapu, kur varat atrast RCS nomnieka ID. Piemēram, ja pieteikšanās lapas URL ir `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d`, nomnieka ID ir informācija, kas parādās pēc `https://login.microsoftonline.com/` vai **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>Finanšu vides nomnieka ID

Lai atrastu nomnieka ID jūsu finanšu videi, izpildiet tās pašas darbības, ko esat sekojis, lai atrastu RCS nomnieku. Tomēr kopējiet un ielīmējiet pilnu jūsu finanšu vides URL, nevis pilnu RCS URL.

## <a name="resolution"></a>Novēršana

Ja abi nomnieku šķiro, jūs saskaraties ar šajā tēmā aprakstīto problēmu. Ja tās ir vienādas, jūs saskaraties ar nesaistītu problēmu. Šajā gadījumā ieteicams sazināties ar Microsoft atbalsta dienestu.

### <a name="solution-1"></a>1. risinājums

Parakstiet savu RCS vidi tam pašam nomniekam, kurā ir pieteicies jūsu finanšu vide. Pēc tam izveidojiet un publicējiet nodokļu līdzekli.

### <a name="solution-2"></a>2. risinājums

Kopīgojiet nodokļu līdzekli ar finanšu nomnieku RCS.

1. RcS, dodieties uz globalizācijas **funkcijām** \> **nodokļu aprēķins.**
2. Atlasiet līdzekli, kuru koplietot, un pēc tam **cilnē Organizācijas** atlasiet Kopīgot **ar**.
3. Laukā **Organizācijas domēna** nosaukums ievadiet nosaukumu. Piemēram, ievadiet **contoso.onmicrosoft.com**.
4. Atlasiet **Koplietot**.

![Nolaižamais dialoglodziņš Kopīgot ar ārējo organizāciju.](media/ShareTaxFeature.png)
