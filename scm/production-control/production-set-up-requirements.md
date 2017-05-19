---
title: "Ražošanas iestatījumu prasības"
description: "Šajā rakstā ir sniegta informācija par iestatīšanas prasībām, kas jāievēro, lai varētu strādāt ar ražošanas kontroli."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 469cf4513a970effb34a857b71a89fd0a5499e25
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="production-setup-requirements"></a>Ražošanas iestatījumu prasības

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par iestatīšanas prasībām, kas jāievēro, lai varētu strādāt ar ražošanas kontroli. 

Modulis Ražošanas kontrole ir integrēts citu moduļu līdzekļos. Šīs savstarpējās saistīšanas iespējas jums ļauj mainīt ražošanas pasūtījumus un nodrošināt, ka tie automātiski tiek atjaunināti visos pārējos sistēmas saistītajos procesos un aprēķinos. Nākamās iestatīšanas procedūras ir uzskaitītas tādā secībā, kādā jums tās ir jāizpilda.

## <a name="required-baseline-setup-in-other-modules"></a>Nepieciešamais bāzlīnijas iestatījums citos moduļos
Lai varētu strādāt ar ražošanas kontroli, ir jāiestata informācija pārējos moduļos. Šajā iestatīšanā ir iekļauti tālāk minētie uzdevumi.

-   Iestatiet vispārējo uzņēmuma informāciju.
-   Iestatiet Virsgrāmatu.
-   Definējiet krājumu grupas.
-   Iestatiet krājumu grupām Virsgrāmatas kontus.
-   Iestatiet krājuma vienību tabulu sadaļā Krājumu vadība.
-   Izveidojiet materiālu komplektus (MK) un MK versijas sadaļa Krājumu vadība.

## <a name="required-calendar-and-resource-setup"></a>Nepieciešamais kalendāra un resursu iestatījums
Pirms lietojat ražošanas kontroli, atveriet sadaļu Organizācijas administrēšana, un izveidojiet un definējiet kalendāru un operācijas resursus tālāk norādītajā secībā.

1.  **Darba laika veidnes** — iestatiet darba laiku veidnes, lai definētu ražošanas plānošanai pieejamos laikus.
2.  **Kalendāri** — iestatiet darba laika kalendārus, lai definētu tās gada dienas, kas ir pieejamas ražošanas plānošanai.
3.  **Resursu grupas** — iestatiet resursu grupas, lai grupētu operāciju resursus — šādi varat gūt pārskatu par visu brīvo noslodzi, kad izpildāt plānošanu. Nav nepieciešams iestatīt resursu grupas, pirms esat iestatījis operācijas resursus. Taču iesakām izprast veidu, ka grupēt resursus, kad iestatāt ražošanas kontroli.
4.  **Resursi** — iestatiet operācijas resursus, lai definētu resursus, ko izmantot ražošanas procesu veikšanai un noslodzes plānošanai.

## <a name="required-production-parameters-setup"></a>Nepieciešamais ražošanas parametru iestatījums
**Ražošanas kontroles parametri** — iestatiet ražošanas pamata parametrus, lai definētu, kā sistēmā tiek izmantoti un apstrādāti ražošanas pasūtījumi. Definējiet veidu, kā ražošanas pasūtījumi tiek izveidoti, novērtēti, plānoti un patērēti. Varat arī atlasīt, kāda veida atsauksmes vēlaties un kā veikt izmaksu uzskaiti.

## <a name="required-journal-name-identification"></a>Nepieciešamā žurnāla nosaukuma identifikācija
**Ražošanas žurnāla nosaukumi** — norādiet ražošanas žurnālu nosaukumus, kas tiek izmantoti, lai ierakstītu un grāmatotu transakcijas.

## <a name="setup-if-you-use-operations"></a>Iestatījums, ja izmantojat operācijas
Operācijas pārstāv specifiskās aktivitātes, kas tiek izpildītas, lai ražotu pabeigtās preces. **Piezīme.** Jums ir jāzina, kāda tipa aktivitātes ir nepieciešamas, lai saražotu jūsu krājumu, kā arī jāzina šo aktivitāšu secība un prioritātes. Jums ir arī jāzina, kuri resursi ir iesaistīti un to daudzums.

1.  **Operācijas** — iestatiet operācijas, lai parādītu uzdevumus, kas ir jāizpilda, lai saražotu pabeigto krājumu.
2.  **Relācijas** — iestatiet operāciju relācijas, lai izveidotu detalizētus rekvizītus. Lai definētu operāciju relācijas, noklikšķiniet uz**Relācijas** lapā **Operācijas**.

## <a name="setup-if-you-use-routes"></a>Iestatījums, ja izmantojat maršrutus
Ja strādājat ar maršrutiem, tad operācijas ir nepieciešams definēt katram ražošanas maršrutam, ko iestatāt. Maršruts parāda ceļu, ko krājums veic no vienas operācijas uz citu, no ražošanas procesa sākuma līdz pat beigām.

1.  **Izmaksu kategorijas** — iestatiet izmaksu kategorijas, lai definētu stundas izmaksas noteiktiem procesiem un sagatavošanas laikiem.
2.  **Izmaksu grupas** — iestatiet izmaksu grupas, lai izveidotu un uzturētu dažādus izmaksu aprēķināšanas tipus.
3.  **Maršrutu grupas** — iestatiet maršrutu grupas, lai definētu parametrus, kas ir saistīti ar maršrutu grupām. Maršrutu grupas ir jāiestata pirms ražošanas maršrutu izveidošanas.
4.  **Maršruti** — iestatiet ražošanas maršrutus un definējiet noklusējuma iestatījumus, lai kontrolētu plānošanu, izmaksu aprēķināšanu, un maršruta operāciju cenu noteikšanu, kā arī lai kontrolētu progresa atskaišu izveidi.
5.  **Maršruti** — iestatiet maršruta versijas, lai ražošanā iespējotu krājumu variācijas.

## <a name="optional-advanced-settings"></a>Neobligātie papildu iestatījumi
1.  **Ražošanas grupas** — iestatiet ražošanas grupas, lai izveidotu relācijas starp ražošanas pasūtījumu un virsgrāmatas kontiem. Virsgrāmatas konti tiek izmantoti, lai pasūtījumus grāmatotu vai tos grupētu atskaišu veidošanai.
2.  **Ražošanas kopas** — izveidojiet ražošanas pūlus, lai grupētu ražošanas pasūtījumus; šādi varat apstrādāt steidzamus ražošanas pasūtījumus vai dzēst un grāmatot pasūtījumu grupas.
3.  **Rekvizīti** — definējiet rekvizītus, lai izveidotu īpašus atribūtus, kurus varat piešķirt saviem resursiem, lai kontrolētu ražošanas secību. Šie atribūti ir savienoti ar darba laiku veidni.





