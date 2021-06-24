---
title: Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) krātuves novecošana
description: Šajā tēmā ir sniegta informācija par Microsoft Dynamics Lifecycle Services (LCS) krātuves novecošanu, kas ir plānots kā daļa no Regulatory Configuration Service (RCS) globālā repozitorija izlaides.
author: JaneA07
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: abaeb34db1d209fa8e5cc83a98c333f42e91f2d2
ms.sourcegitcommit: 7cda434becd198c1cd405e001289777ae7a24fe1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/01/2021
ms.locfileid: "6127923"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) — Lifecycle Services (LCS) krātuves novecošana

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) izmantošana kā elektronisko pārskatu (ER) konfigurāciju krātuve repozitorijā ir novecojusi. Šis novecošana ietvers šādas izmaiņas:

- Microsoft ražotās konfigurācijas, kas tiek izmantotas Microsoft Dynamics 365 lietojumprogrammās, vairs netiks publicētas LCS koplietojamo līdzekļu bibliotēkā. Tā vietā tās publicēs tikai ar RCS globālā repozitorija starpniecību. Tomēr konfigurācijas, kas paredzētas Dynamics AX 2012, tiks publicētas LCS koplietojamo līdzekļu bibliotēkā līdz AX 2012 atbalsta dzīves cikla beigām.
- Tiks deaktivizēta funkcionalitāte, kas ļauj augšupielādēt konfigurācijas LCS projekta līdzekļu bibliotēkā no Finance and Operations programmām un RCS. Tomēr joprojām varēsit izmantot pārlūkprogrammu, kas atrodas LCS, lai augšupielādētu konfigurācijas projekta līdzekļu bibliotēkā. Tādēļ joprojām var pievienot konfigurācijas LCS, lai tās varētu ietvert risinājumu pakotnēs.
- Konfigurāciju importēšana no LCS vēl kādu laiku būs pieejama un atbalstīta Finance and Operations programmās un RCS. Tomēr funkcionalitāte galu galā novecos. (Precīzs novecošanas datums tiks paziņots vēlāk.)

## <a name="deprecation-notice"></a>Paziņojums par novecošanu

LCS kā krātuves izmantošanas novecošana tika paziņota sadaļā [Noņemtie vai novecojušie līdzekļi Dynamics 365 Finance – paziņojums par LCS novecošanu](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Plānotais novecošanas datums ir 2022. gada 1. aprīlis.

## <a name="key-features"></a>Galvenie līdzekļi

- Varat izmantot RCS, lai izveidotu un rediģētu konfigurācijas. Pēc tam šīs konfigurācijas var pārvietot tieši no noformētāja uz pievienoto programmu. Tādēļ konfigurācijas var ātri mainīt un pārbaudīt.
- Globālais repozitorijs ir visu ER konfigurāciju centralizēta krātuve.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Norādījumi vienreizējām un notiekošām darbībām

Šajā sadaļā ir aprakstīta darbību kopa, kas jāveic vienu reizi. Šeit aprakstītas arī darbības, kas pēc tam jāveic pastāvīgi.

### <a name="one-time-action"></a>Vienreizēja darbība

Importējiet visas nepieciešamās konfigurācijas no LCS uz RCS un pēc tam publicējiet tās no RCS globālajā repozitorijā. Ja izmantojat projektam raksturīgās līdzekļu bibliotēkas, lai glabātu atvasinātās konfigurācijas LCS, tad ir jāveic turpmākās darbības, kamēr LCS joprojām ir pieejams.

1. Ja RCS instance vairs nav pieejama, lai to nodrošinātu. Papildinformāciju skatiet [RCS pārskatā](rcs-overview.md).
2. Nodrošinātajā RCS instancē katram līdzekļu bibliotēkā esošajam LCS projektam, kas ietver atvasinātās ER konfigurācijas, reģistrējiet atbilstošo LCS repozitoriju.
3. Importējiet ER konfigurācijas no LCS repozitorija uz RCS. Papildinformāciju skatiet [Konfigurāciju importēšana no LCS](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md).
4. Ja globālais repozitorijs netiek nodrošināts automātiski, reģistrējiet to RCS.
5. Augšupielādējiet visas atvasinātās konfigurācijas no pašreizējās RCS instances globālajā repozitorijā. Izmantojiet līdzekli **Konfigurācijas pakotnes, kas ļauj lietotājam vienā operācijā augšupielādēt visas konfigurācijas GR**, lai saņemtu palīdzību augšupielādes laikā. Papildinformāciju skatiet [RCS augšupielāde globālajā repositorijā](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Turpmāk

Izmantojiet vizuālos noformētājus RCS, lai izveidotu visas jaunās konfigurācijas. Pēc tam augšupielādējiet konfigurācijas globālā repozitorija krātuvē. Papildinformāciju skatiet [ER konfigurāciju izveidošana RCS un augšupielāde globālajā repozitorijā](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Vai šīs izmaiņas nozīmē, ka LCS nevar izmantot kā konfigurāciju centrālo krātuvi?

Jā. Tiks deaktivizēta funkcionalitāte, kas ļauj augšupielādēt konfigurācijas LCS projekta līdzekļu bibliotēkā no Finance and Operations programmām. Tomēr joprojām varat izmantot pārlūkprogrammu, kas atrodas LCS, lai augšupielādētu konfigurācijas projekta līdzekļu bibliotēkā, pēc nepieciešamības.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Es domāju, ka RCS bija globālo veidņu failu importēšanas aizstāšanas repozitorijs. Es nedomāju, ka tas tiek izmantots konfigurāciju glabāšanai. Kā ir pareizi?

RCS ir noformēšanas pakalpojums ER konfigurāciju izveidošanai un rediģēšanai. RCS ir savs repozitorijs, kas zināms kā globālais repozitorijs. Šis repozitorijs tiek izmantots, lai glabātu RCS izveidotās konfigurācijas. Pēc tam, kad LCS kā krātuve būs novecojusi, globālais repozitorijs būs vienīgais Microsoft konfigurāciju avots. Jums ir jāveic vienreizēja darbība, lai importētu visas konfigurācijas, kas jums nepieciešamas no LCS uz RCS, un tad tās jāpublicē no RCS uz globālo repozitoriju.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Bez LCS, kāds ir ieteicamais konfigurāciju glabāšanas veids, lai “testa” un “ražošanas” konfigurācijas varētu viegli pārvaldīt un pārnest?

RCS izmanto *savienoto programmu* konceptu. Saistīta programma veido savienojumu starp RCS un jebkuru Finance and Operations programmu instanci. Tā kā RCS var izmantot konfigurāciju rediģēšanai, savienoto programmu var izmantot, lai pārvietotu konfigurācijas tieši no noformētāja uz Finance and Operations programmu vidi. Tādēļ varat ātri mainīt un testēt savas konfigurācijas, neizmantojot LCS projekta līmeņa krātuvi.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Vai ir kādi piemēri, kas parāda iestatīšanu un pārvaldību?

Piemēru nav, tomēr šajā tēmā varat izpildīt iepriekš aprakstītās darbības, lai migrētu savas konfigurācijas uz RCS globālo repozitoriju.
