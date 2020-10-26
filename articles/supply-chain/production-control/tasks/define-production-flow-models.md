---
title: Ražošanas plūsmas modeļu definēšana
description: Ražošanas plūsmas modeļi apraksta, kā tiek aprēķināta un uzturēta lean manufacturing darba šūnu noslodze.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlowModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 511c466d6019cb182c9ada0b02172b8eeb3725e6
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975828"
---
# <a name="define-production-flow-models"></a>Ražošanas plūsmas modeļu definēšana

[!include [banner](../../includes/banner.md)]

Ražošanas plūsmas modeļi apraksta, kā tiek aprēķināta un uzturēta lean manufacturing darba šūnu noslodze. Tādēļ ražošanas plūsmas modeļa definēšana ir darba šūnu definēšanas priekšnosacījums. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="define-a-production-flow-model"></a>Definējiet ražošanas plūsmas modeli. 
1. Dodieties uz Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas modeļi.
2. Noklikšķiniet uz Jauns.
3. Laukā Ražošanas plūsmas modelis ievadiet ražošanas plūsmas modeļa ID.
4. Laukā Modeļa tips atlasiet opciju.
    * Ir divi modeļu tipi: tips Caurlaide un tips Stundas. Tipam Caurlaide tādu darba šūnu noslodze, kuras izmanto šo ražošanas plūsmas modeli, tiks izteikta un aprēķināta preču daudzumā. Tipam Stundas tādu darba šūnu noslodze, kuras izmanto šo ražošanas plūsmas modeli, tiks izteikta un aprēķināta stundās. Ņemiet vērā, ka šo rekvizītu nevar mainīt esošajam ražošanas plūsmas modelim. Pēc tam, kad darba šūnai ir izveidotas noslodzes rezervācijas, ražošanas plūsmas modeļa tipu nevar mainīt.  
5. Ievadiet dienu skaitu EPE ciklā.
    * Intervāls norāda periodu, kad katra ražošanas plūsmas vai darba šūnas ražotā daļa tiks saražota vismaz vienu reizi. Jo īsāks ir EPE cikls, jo elastīgāks ir ražošanas process. Ja EPE cikls = 0, visu pieprasījumu var saražot tajā pašā dienā. EPE cikls tiek izmantots, lai plānotu racionāla procesa darbus. Plānojot darbu darba šūnai, ja EPE cikls = 5, plānošanas procesa ietvaros tiks pievērsta uzmanība darba šūnas noslodzei izpildes datumā, no kura atņemts EPE cikla garums (5 dienas pirms izpildes datums), lai nodrošinātu, ka preci var saražot attiecīgajā ciklā. Preces krājumu izpildes laiks parasti ir vienāds ar vai lielāks par saistītā ražošanas procesa EPE ciklu.  
6. Laukā Plānošanas perioda tips atlasiet kādu opciju.
    * Pēc tam, kad darba šūnai ir izveidotas noslodzes rezervācijas, plānošanas perioda tipu nevar mainīt. Var izvēlēties tikai ražošanas plūsmas modeļus ar tādu pašu perioda tipu attiecīgajai darba šūnai.  
7. Laukā Plānošanas laika periods ievadiet skaitli.
    * Plānošanas laika periods norāda dienu skaitu, kurā var veikt noslodzes rezervācijas saistītajām darba šūnām. Plānošanas laika periodā ievadiet dienu skaitu.   Kanban procesa darbi, kuri atrodas ārpus šī perioda, netiek plānoti, izmantojot automātisko plānošanu. Plānošanas laika periods parasti ir divas reizes ilgāks par ražošanas plūsmā vai darba šūnā saražoto preču vidējo krājumu izpildes laiku. EPE cikls nedrīkst būt garāks par pusi no plānošanas laika perioda.     
8. Laukā Noslodzes nepietiekamības sekas atlasiet kādu opciju.
    * Opcijas ir šādas: Atlikt — plānošanas notikuma viss pieprasījums tiek atlikts līdz nākamajai pieejamajai ražošanas dienai ar pieejamu caurlaidi. Atcelt — plānošanas notikuma automātiskā plānošana tiek pārtraukta un saistītie darbi tiek atstāti neplānoti.   Pievienot pieprasītajai dienai — pieprasītie darbi tiek plānoti pieprasītajā periodā. Tas rada šūnas pārslodzi attiecīgajai dienai, plānotājam ir jāveic pārskatīšana un ir nepieciešama manuāla iejaukšanās.   Sadalīt pieejamajos periodos — dažādi plānošanas notikuma darbi tiek sadalīti visās pieejamajās ražošanas dienās, sākot ar pirmo pieejamo dienu. Minimālais sadales daudzums ir Kanban darba daudzums. Sadalē tiek piešķirts minimālais plānošanas daudzums (Kanban daudzums) katrai dienai, kurā ir pieejama pietiekama caurlaide.  

