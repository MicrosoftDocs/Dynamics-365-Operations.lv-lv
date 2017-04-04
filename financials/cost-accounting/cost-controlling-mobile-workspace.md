---
title: "Izmaksas, kontrolējot mobilo darbvietu Microsoft Dynamics 365 app darbības"
description: "Ar izmaksu kontrolēt mobilo darbvietu, izmaksu centra vadītāji var redzēt izmaksu centra darbību jebkurā laikā un jebkurā vietā."
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

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Izmaksas, kontrolējot mobilo darbvietu Microsoft Dynamics 365 app darbības

Ar izmaksu kontrolēt mobilo darbvietu, izmaksu centra vadītāji var redzēt izmaksu centra darbību jebkurā laikā un jebkurā vietā. 

<a name="prerequisites"></a>Priekšnosacījumi
-------------

| Priekšnoteikumi                                                         | apraksts                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lasiet par Microsoft Dynamics 365 operācijas mobilā platforma | [Dinamika 365 operācijas mobilā platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dinamika 365 operācijām                                          | Pārliecinieties, ka jūs izmantojat vidē, kas ir Microsoft Dynamics 365 darbību versija 1611 un Microsoft Dynamics darbības platformu atjaunināt 3 (2016. gada novembrī). |
| Labojumfailu KB 3215650                                                    | Jāinstalē labojumfails, lai iespējotu darbvietu, ar kurām ir norādītas Microsoft Dynamics 365 operācijām.                                                                       |
| Mobilā ierīce, kurā ir dinamika 365 operācijas app uzstādīta | Lejupielādējiet Dynamics 365 operācijas app no mobilo app store.                                                                                                      |

## <a name="introduction"></a>Ievads
Izmaksas kontrolēt mobilo darbvietu nodrošina tūlītēju skatu pašreizējā darbības izmaksu centriem, salīdzinot faktiskās izmaksas attiecībā pret budžetā paredzētajām izmaksām. Var detalizēti statusi individuālo izmaksu elementus.

### <a name="example"></a>Paraugs

Darbinieks saņem ielūgumu uz starptautisku konferenci. Organizācija būs ceļa izdevumu segšanai. Darbinieka lūdz viņa silītē, ja viņš var apmeklēt konferenci. Pārvaldnieks atver ātri izmaksas kontrolēt mobilo darbvietu savā mobilajā telefonā, lai redzētu, vai viņš ir budžeta darbiniekam piedalīties konferencē.

### <a name="data-security"></a>Datu drošība

Izmaksu kontrole darbvietas datiem aizsargā lietotāja akreditācijas datus. Izmaksu centra vadītājs drīkst tikai redzēt savu izmaksu centra dati. Piekļuves drošības līmenī pārvalda izmaksu uzskaites moduļa. Grāmatvežu izmaksas norādīt izmaksas kontrolēt mobilo darbvietu konfigurāciju izmaksu uzskaites modulī. Pēc tam, kad darbvieta ir publicēts Microsoft Dynamics 365 app operācijām, tā ir pieejama Dynamics 365 operāciju mobilo app. Tas nodrošina, ka visu izmaksu centra vadītāji uzņēmumā apskatīt datus tādā pašā formātā.

### <a name="actions-views-and-links"></a>Darbību, viedokli un saites

Kontrolējot mobilo darbvietu Dynamics 365 app darbības izmaksas nodrošina šādu darbību, viedokli un saites:

-   Darbības 
    -   Atlasiet **konfigurācijas** izvēlēties izkārtojumu.
    -   Atlasiet **objektu izmaksas** izvēlēties izmaksu centriem, pēc kuras vēlaties filtrēt datus. **Piezīme:** saskaņā ar izmaksu uzskaites modulī piešķirta piekļuve tiek parādīts saraksts.

<!-- -->

-   Atkarībā no tā, kas izvēlēts saskaņā ar **darbības** un kas ir konfigurēta izmaksu uzskaites moduli, var apskatīt šādu informāciju kartes. Ņemiet vērā, ka summa tiek parādīta tādā pašā formātā: faktiskās, budžeta, dispersiju un dispersiju %. 
    -   Budžets (perioda) faktisko vs
    -   Faktisko vs pārskatītais budžets (periodā)
    -   Faktisko vs budžeta (iepriekšējā periodā)
    -   Faktisko vs pārskatītais budžets (iepriekšējā periodā)
    -   Faktisko vs budžeta (gads, datums)
    -   Faktisko vs pārskatītais budžets (gads, datums)

<!-- -->

-   Saites
    -   Detalizētu informāciju par pašreizējo periodu.
    -   Informācija par iepriekšējo periodu.
    -   Datus no gada sākuma.

Atlasot vienu no saitēm, tiek parādīta karte katram izmaksu elements. Kartes summa tiek parādīta šādā formātā: budžeta starpība faktiskās, budžeta, budžeta starpība %, pārskatītais budžets, pārskatītais budžets dispersiju un pārskatītais budžets dispersijas %.  [![izmaksu kontrole](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Darba sākšana
Lai sāktu izmantot izmaksu kontroles mobilo app savā mobilajā ierīcē, rīkojieties šādi.

1.  Mobilo app Store, lejupielādējiet un instalējiet Microsoft Dynamics 365 operācijas app.
2.  Savā ierīcē palaidiet app.
3.  Ievadiet savu dinamiku 365 URL.
4.  Ievadiet uzņēmuma pieteikties. Piemēram, ievadiet **USMF**.
5.  Pirmo reizi piesakoties, jums tiek lūgts ievadīt lietotājvārdu un paroli par jūsu Microsoft Dynamics 365 operāciju kontam. Ievadiet savus akreditācijas datus. Pēc tam, kad jūs piesakāties sistēmā, jūs redzēt pieejams darbvietā savam uzņēmumam.

Lai skatītu darbvietu mobilo app, vispirms jāpublicē vajadzīgo darbvietu Dynamics 365 operācijas app.

1.  Dynamics 365 sākt operāciju.
2.  Dodieties uz **sistēmas administrēšanu**&gt;**Setup**&gt;**sistēmas parametru**.
3.  Atlasiet **Manage mobilo app**.
4.  Atlasīt darbvietas * * izmaksu kontrole * * publicēt mobilā platforma.
5.  Atlasiet **publicēt darbvietu**.
6.  Atsvaidzinātu ierīces redzēt publicēto darbvietām.

## <a name="view-the-performance-of-your-cost-center"></a>Skatiet izmaksu centru darbības
1.  Mobilajā ierīcē, atlasiet **izmaksu kontrolei** darbvietu.
2.  Atlasiet **izmaksas, objektu kontrolei**.
3.  Noklikšķiniet uz **darbības**.
4.  Noklikšķiniet uz **Select configuration**, lai atlasītu izmaksu kontroles izkārtojumu.
5.  Click **Done**.
6.  Noklikšķiniet uz **darbības**.
7.  Noklikšķiniet uz **atlasiet izmaksu objektam** uz atlasiet izmaksu centru, kas jums ir piešķirta pieeja.
8.  Click **Done**.
9.  Skatiet izmaksu centru vispārējo veiktspēju.
10. Noklikšķiniet uz **sīkāku informāciju par pašreizējo periodu**.
11. Skatīt atsevišķu izmaksu elementu izpildi.
12. Varat arī meklēt konkrētu izmaksu elementus.



