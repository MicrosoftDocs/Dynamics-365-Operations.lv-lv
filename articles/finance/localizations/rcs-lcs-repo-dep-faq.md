---
title: Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) krātuves novecošana
description: Šajā rakstā ir Microsoft Dynamics sniegta informācija par Lifecycle Services (LCS) krātuves nolietojumu, kas ir plānota kā daļa no regulēšanas konfigurācijas pakalpojuma (RCS) globālā repozitorija atrites.
author: kfend
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
ms.openlocfilehash: 717a2b9b00e137631a7cb9a188bdcf1b33e6af02
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277220"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) — Lifecycle Services (LCS) krātuves novecošana

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) izmantošana kā elektronisko pārskatu (ER) konfigurāciju krātuve repozitorijā ir novecojusi. Šis novecošana ietvers šādas izmaiņas:

- Microsoft ražotās konfigurācijas, kas tiek izmantotas Microsoft Dynamics 365 lietojumprogrammās, vairs netiks publicētas LCS koplietojamo līdzekļu bibliotēkā. Tā vietā tās publicēs tikai ar RCS globālā repozitorija starpniecību. Tomēr konfigurācijas, kas paredzētas Dynamics AX 2012, tiks publicētas LCS koplietojamo līdzekļu bibliotēkā līdz AX 2012 atbalsta dzīves cikla beigām.
- Funkcionalitāte, kas ļauj jums augšupielādēt konfigurācijas projekta līdzekļu bibliotēkā LCS no finanšu un operāciju programmām, un no RCS, tiks deaktivizēta. Tomēr joprojām varēsit izmantot pārlūkprogrammu, kas atrodas LCS, lai augšupielādētu konfigurācijas projekta līdzekļu bibliotēkā. Tādēļ joprojām var pievienot konfigurācijas LCS, lai tās varētu ietvert risinājumu pakotnēs.
- Konfigurāciju imports no LCS turpinās būt pieejams un atbalstīts finanšu un operāciju programmās, kā arī RCS jau kādu laiku. Tomēr funkcionalitāte galu galā novecos. (Precīzs novecošanas datums tiks paziņots vēlāk.)

## <a name="deprecation-notice"></a>Paziņojums par novecošanu

Dynamics 365 Finanšu - LCS nolietojuma paziņojumā par nolietojumu tika izmantota LCS [lietošana kā krātuve](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Plānotais novecošanas datums ir 2022. gada 1. aprīlis.

## <a name="key-features"></a>Galvenie līdzekļi

- Izmantojiet RCS, lai izveidotu un rediģētu ER konfigurācijas un globalizācijas funkcijas.
- Spiež konfigurācijas tieši no RCS veidotāja uz savienotu programmu, piemēram, Dynamics 365 finanšu vidi, lai jūs varētu ātri veikt un pārbaudīt izmaiņas jūsu konfigurācijās.
- Centralizēti saglabājiet, koplietojiet un pārvaldiet dzīves ciklu gan ER konfigurācijām, gan globalizācijas funkcijām ar globalizētā repozitorija centralizēto krātuvi.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Norādījumi vienreizējām un notiekošām darbībām

Šajā sadaļā ir aprakstīta darbību kopa, kas jāveic vienu reizi. Šeit aprakstītas arī darbības, kas pēc tam jāveic pastāvīgi.

### <a name="one-time-action"></a>Vienreizēja darbība

Importējiet visas nepieciešamās konfigurācijas no LCS uz RCS un pēc tam publicējiet tās no RCS globālajā repozitorijā. Ja izmantojat projektam raksturīgās līdzekļu bibliotēkas, lai glabātu atvasinātās konfigurācijas LCS, tad ir jāveic turpmākās darbības, kamēr LCS joprojām ir pieejams.

1. Ja RCS instance vairs nav pieejama, lai to nodrošinātu. Papildinformāciju skatiet [RCS pārskatā](rcs-overview.md).
2. Nodrošinātajā RCS instancē katram līdzekļu bibliotēkā esošajam LCS projektam, kas ietver atvasinātās ER konfigurācijas, reģistrējiet atbilstošo LCS repozitoriju.
3. Importējiet ER konfigurācijas no LCS repozitorija uz RCS. Papildinformāciju skatiet [Konfigurāciju importēšana no LCS](/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services).
4. Ja globālais repozitorijs netiek nodrošināts automātiski, reģistrējiet to RCS.
5. Augšupielādējiet visas atvasinātās konfigurācijas no pašreizējās RCS instances globālajā repozitorijā. Lai saņemtu palīdzību saistībā ar augšupielādi, izmantojiet līdzekli **Konfigurācijas pakotnes**. Papildinformāciju skatiet [RCS augšupielāde globālajā repositorijā](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Turpmāk

Izmantojiet vizuālos veidotājus RCS šādiem nolūkiem:

- Paplašināt Microsoft sniegtās veidnes.
- Izveidojiet jaunas konfigurācijas, kuras pieprasa jūsu organizācija.
- Pielāgojiet globalizācijas līdzekļus elektronisko rēķinu izrakstīšanai un nodokļu aprēķina pakalpojumam.

Izmantojiet Globalizācijas repozitoriju šādiem nolūkiem:

- Piekļūstiet Microsoft saražotajām konfigurācijām un globalizācijas funkcijām.
- Augšupielādējiet izveidotās vai paplašinātās konfigurācijas globālajā repozitorijā glabāšanai un kopīgojiet tās organizācijas Dynamics 365 lietojumprogrammas vidēs vai ar ārējām organizācijām. Papildinformāciju skatiet [ER konfigurāciju izveidošana RCS un augšupielāde globālajā repozitorijā](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Vai šīs izmaiņas nozīmē, ka LCS nevar izmantot kā konfigurāciju centrālo krātuvi?

Jā. Funkcionalitāte, kas ļauj jums augšupielādēt konfigurācijas projekta līdzekļu bibliotēkā LCS no finanšu un operāciju programmām, tiks novecojusi. Tomēr joprojām varat izmantot pārlūkprogrammu, kas atrodas LCS, lai augšupielādētu konfigurācijas projekta līdzekļu bibliotēkā, pēc nepieciešamības.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Es domāju, ka RCS bija globālo veidņu failu importēšanas aizstāšanas repozitorijs. Es nedomāju, ka tas tiek izmantots konfigurāciju glabāšanai. Kā ir pareizi?

RCS ir noformēšanas pakalpojums ER konfigurāciju izveidošanai un rediģēšanai. RCS ir savs repozitorijs, kas zināms kā globālais repozitorijs. Šis repozitorijs tiek izmantots, lai glabātu RCS izveidotās konfigurācijas. Pēc tam, kad LCS kā krātuve būs novecojusi, globālais repozitorijs būs vienīgais Microsoft konfigurāciju avots. Jums ir jāveic vienreizēja darbība, lai importētu visas konfigurācijas, kas jums nepieciešamas no LCS uz RCS, un tad tās jāpublicē no RCS uz globālo repozitoriju.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Bez LCS, kāds ir ieteicamais konfigurāciju glabāšanas veids, lai “testa” un “ražošanas” konfigurācijas varētu viegli pārvaldīt un pārnest?

RCS izmanto *savienoto programmu* konceptu. Savienots pieteikums veido savienojumu starp RCS un jebkuru finanšu un operāciju programmu gadījumu. Tā kā RCS var izmantot konfigurāciju rediģēšanai, pievienoto programmu var izmantot, lai konfigurācijas virzītu tieši no veidotāja uz finanšu un operāciju lietojumprogrammu vidēm. Tādēļ varat ātri mainīt un testēt savas konfigurācijas, neizmantojot LCS projekta līmeņa krātuvi.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Vai ir kādi piemēri, kas parāda iestatīšanu un pārvaldību?

Nav piemēru, bet varat veikt šajā rakstā iepriekš norādītās darbības, lai migrētu konfigurācijas uz RCS globālo repozitoriju.

### <a name="is-rcs-a-prerequisite-to-configure-electronic-reporting"></a>Vai RCS ir priekšnoteikums elektronisko pārskatu konfigurēšanai?

Jā. RCS ietver iespējas, kas atbalsta iestatījuma globalizācijas līdzekļus, ko izmanto globalizācijas pakalpojumi, piemēram, elektronisko rēķinu izrakstīšana un nodokļu aprēķina pakalpojums. Tomēr pakalpojumam ir tāda pati vizuāla veidotāja funkcionalitāte, kas ļauj paplašināt vai izveidot jaunas ER konfigurācijas. RCS nodrošina arī dzīves cikla pārvaldību gan ER konfigurācijām, gan globalizācijas funkcijām.

### <a name="which-regions-can-rcs-be-deployed-in"></a>Kuros reģionos RCS var izvietot?

RCS ir pieejams šādos Azure reģionos:

- ASV
- Indija
- Francija
- Eiropa

Papildinformāciju par produktu atbalstu skatiet [Dynamics globalizācijas pakalpojumu pārskatā](globalization-services-overview.md). Informāciju par ģeogrāfisko atbalstu skatiet [Dynamics 365 un Power Platform: pieejamība, datu atrašanās vieta, valoda un lokalizācija](https://aka.ms/rcs/D365Productavailabilityguide).

### <a name="whats-the-cost-of-using-rcs"></a>Kādas ir RCS izmantošanas izmaksas?

RCS un globalizācijas repozitorijs tiek nodrošināts par bezmaksas maksu kā daļa no esošajām finanšu un operāciju programmas licencēm. Izmantojot RCS dizaina pakalpojumu vai glabājot konfigurācijas globālajā repozitorijā, nav saistītas nekādas atsevišķas izmaksas. Pašlaik nav ierobežojuma konfigurāciju vai pievienoto pieteikumu skaitam.
