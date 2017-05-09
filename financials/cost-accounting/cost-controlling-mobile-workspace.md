---
title: "Mobilā darbvieta Izmaksu kontrole Microsoft Dynamics 365 for Operations programmai"
description: "Izmantojot mobilo darbvietu Izmaksu kontrole, izmaksu centru vadītāji izmaksu centra veiktspēju var redzēt jebkurā laikā un jebkurā vietā."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilā darbvieta Izmaksu kontrole Microsoft Dynamics 365 for Operations programmai

Izmantojot mobilo darbvietu Izmaksu kontrole, izmaksu centru vadītāji izmaksu centra veiktspēju var redzēt jebkurā laikā un jebkurā vietā. 

<a name="prerequisites"></a>Priekšnosacījumi
-------------

| Priekšnoteikumi                                                         | Apraksts                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lasīt par Microsoft Dynamics 365 for Operations mobilo platformu | [Dynamics 365 for Operations mobilā platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Pārliecinieties, ka izmantojat vidi, kurā ir instalēta Microsoft Dynamics 365 for Operations versija 1611 un Microsoft Dynamics for Operations 3. platformas atjauninājums (2016. gada novembra versija). |
| Labojumfails KB 3215650                                                    | Instalējiet labojumfailu, lai iespējotu programmatūrā Microsoft Dynamics 365 for Operations nodrošinātās darbvietas.                                                                       |
| Mobilā ierīce, kurā ir instalēta Dynamics 365 for Operations programma | Lejupielādējiet Dynamics 365 for Operations programmu no mobilo programmu veikala.                                                                                                      |

## <a name="introduction"></a>Ievads
Mobilā darbvieta Izmaksu kontrole sniedz tūlītēju skatu uz izmaksu centru pašreizējo veiktspēju, faktiskās izmaksas salīdzinot ar budžetā paredzētajām izmaksām. Varat skatīt detalizētāku informāciju līdz pat atsevišķu izmaksu elementu statusiem.

### <a name="example"></a>Piemērs

Kāds darbinieks saņem uzaicinājumu uz starptautisku konferenci. Organizācijai būs jāsedz visi ceļojuma izdevumi. Darbinieks savam vadītājam vaicā, vai ir iespējams apmeklēt šo konferenci. Vadītājs savā mobilajā tālrunī ātri atver mobilo darbvietu Izmaksu kontrole, lai apskatītu, vai ir pieejams budžets, lai darbinieks šo konferenci varētu apmeklēt.

### <a name="data-security"></a>Datu drošība

Darbvietā Izmaksu kontrole datus aizsargā lietotāja akreditācijas dati. Izmaksu centra vadītājam ir atļauts apskatīt tikai datus par viņa paša izmaksu centru. Piekļuves līmeņa drošība tiek pārvaldīta modulī Izmaksu uzskaite. Izmaksu grāmatveži mobilās darbvietas Izmaksu kontrole konfigurāciju definē modulī Izmaksu uzskaite. Kad šī darbvieta ir publicēta Microsoft Dynamics 365 for Operations programmā, tā ir pieejama Dynamics 365 for Operations mobilajā programmā. Tādējādi tiek nodrošināts, ka visi organizācijas izmaksu centra vadītāji datus redz vienādā formātā.

### <a name="actions-views-and-links"></a>Darbības, skati un saites

Mobilajā darbvietā Izmaksu kontrole Dynamics 365 for Operations programmai ir pieejamas tālāk uzskaitītās darbības, skati un saites.

-   Darbības 
    -   Atlasiet vienumu **Konfigurācijas**, lai izvēlētos kādu izkārtojumu.
    -   Atlasiet vienumu **Izmaksu objekti**, lai izvēlētos izmaksu centrus, par kuriem vēlaties filtrēt datus. **Piezīme.** Šis saraksts tiek rādīts atbilstoši izmaksu uzskaites modulī piešķirtajai piekļuvei.

<!-- -->

-   Atkarībā no sadaļā **Darbības** veiktās atlases un atkarībā no konfigurējuma izmaksu uzskaites modulī, kartēs varat skatīt tālāk aprakstīto informāciju. Ņemiet vērā, ka summa tiek rādīta tādā pašā formātā: Faktiski, Budžets, Novirze un Novirze %. 
    -   Faktiski pret budžetu (pašreizējais periods)
    -   Faktiski pret pārskatīto budžetu (pašreizējais periods)
    -   Faktiski pret budžetu (iepriekšējais periods)
    -   Faktiski pret pārskatīto budžetu (iepriekšējais periods)
    -   Faktiski pret budžetu (no gada sākuma)
    -   Faktiski pret pārskatīto budžetu (no gada sākuma)

<!-- -->

-   Saites
    -   Informācija pašreizējam periodam.
    -   Informācija iepriekšējam periodam.
    -   Informācija līdzšinējam gadam.

Kad atlasāt kādu no saitēm, tiek parādīta Karte katram izmaksu elementam. Summa kartēs tiek rādīta šādā formātā: Faktiski, Budžets, Budžeta novirze, Budžeta novirze %, Pārskatītais budžets, Pārskatītā budžeta novirze un Pārskatītā budžeta novirze %.  [![cost-controlling](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Darba sākšana
Lai savā mobilajā ierīcē sāktu lietot izmaksu kontroles mobilo programmu, izpildiet tālāk aprakstītos norādījumus.

1.  Savā mobilo programmu veikalā lejupielādējiet programmu Microsoft Dynamics 365 for Operations un instalējiet to.
2.  Palaidiet programmu savā mobilajā ierīcē.
3.  Ievadiet savu Dynamics 365 vietrādi URL.
4.  Ievadiet uzņēmumu, kurā pierakstīties. Ievadiet, piemēram, **USMF**.
5.  Pirmajā pierakstīšanās reizē ir jāievada Microsoft Dynamics 365 for Operations konta lietotājvārds un parole. Ievadiet savus akreditācijas datus. Pēc pierakstīšanās ir redzamas jūsu uzņēmumam pieejamās darbvietas.

Lai darbvietas skatītu savā mobilajā programmā, jums šīs nepieciešamās darbvietas vispirms ir jāpublicē Dynamics 365 for Operations programmā.

1.  Palaidiet Dynamics 365 for Operations.
2.  Dodieties uz **Sistēmas administrēšana** &gt; **Iestatīšana** &gt; **Sistēmas parametri**.
3.  Atlasiet vienumu **Pārvaldīt mobilo programmu**.
4.  Atlasiet darbvietu **Izmaksu kontrole**, kas ir jāpublicē mobilajā platformā.
5.  Atlasiet vienumu **Publicēt darbvietu**.
6.  Atsvaidziniet ierīci, lai redzētu publicētās darbvietas.

## <a name="view-the-performance-of-your-cost-center"></a>Skatīt sava izmaksu centra veiktspēju
1.  Mobilajā ierīcē atlasiet darbvietu **Izmaksu kontrole**.
2.  Atlasiet vienumu **Izmaksu objektu kontrole**.
3.  Noklikšķiniet uz **Darbības**.
4.  Noklikšķiniet uz **Atlasīt konfigurāciju**, lai atlasītu izmaksu kontroles izkārtojumu.
5.  Noklikšķiniet uz **Gatavs**.
6.  Noklikšķiniet uz **Darbības**.
7.  Noklikšķiniet uz **Atlasīt izmaksu objektu**, lai atlasītu izmaksu centrus, attiecībā uz kuriem jums ir piešķirta piekļuve.
8.  Noklikšķiniet uz **Gatavs**.
9.  Skatiet vispārēju sava izmaksu centra veiktspēju.
10. Noklikšķiniet uz **Informācija pašreizējam periodam**.
11. Skatiet atsevišķu izmaksu elementu veiktspēju.
12. Varat arī meklēt konkrētus izmaksu elementus.



