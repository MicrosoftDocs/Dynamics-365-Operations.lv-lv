---
title: "Ražošanas pasūtījuma izveide"
description: "Šajā procedūrā ir parādīts, kā izveidot ražošanas pasūtījumu."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 4db56f76c7f8ce0cccf85ab04024d9a1e88a8822
ms.contentlocale: lv-lv
ms.lasthandoff: 02/06/2018

---
# <a name="create-a-production-order"></a>Ražošanas pasūtījuma izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot ražošanas pasūtījumu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī ir pirmā procedūra no septiņām, kurā ir paskaidrots ražošanas pasūtījuma cikls.


## <a name="create-a-production-order"></a>Ražošanas pasūtījuma izveide
1. Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.
2. Noklikšķiniet uz Jauns ražošanas pasūtījums.
3. Laukā Krājuma kods ierakstiet D0001.
4. Laukā Piegāde ierakstiet datumu.
    * Piegādes datums norāda, kad ir jābeidzas ražošanas pasūtījumam, lai piegāde notiktu laikā. Šo datumu var izmantot plānošanas procesā. Piemēram, pasūtījumu varat plānot atpakaļ no piegādes datuma.  
5. Daudzuma laukā iestatiet vērtību 20.
    * Piezīme: MK numura laukā automātiski tiek rādīts jebkura pašreizējam krājumam aktīvā MK numurs, bet ražošanas pasūtījumam šo MK varat mainīt, apstiprināto MK versiju sarakstā atlasot kādu aktīvu MK.    Laukā Maršruta numurs automātiski tiek rādīts jebkura pašreizējam krājumam aktīvā maršruta numurs, bet ražošanas pasūtījumam šo vērtību Maršruts varat mainīt, apstiprināto maršrutu versiju sarakstā atlasot kādu aktīvu maršrutu.  
6. Noklikšķiniet uz Izveidot.

## <a name="validate-the-production-order"></a>Pārbaudīt ražošanas pasūtījumu
1. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Noklikšķiniet uz saites tam ražošanas pasūtījuma numuram, ko tikko izveidojāt. Šādi tiek atvērta lapa ar detalizētu informāciju par pasūtījumu.  
2. Noklikšķiniet uz Rediģēt.
3. Laukā Piegāde ierakstiet datumu.
    * Piemēram, ražošanas pasūtījumam varat mainīt piegādes datumu.  
4. Noklikšķiniet uz Saglabāt.
5. Aizvērt lapu.

## <a name="update-the-bom"></a>Atjaunināt MK
1. Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.
2. Noklikšķiniet uz MK.
    * Atveriet MK lapu, lai pārbaudītu MK datus, kas tika kopēti no noklusējuma datiem, kad tika izveidots ražošanas pasūtījums. Šajā procedūrā jums ir jāatjaunina MK daudzums.  
3. Noklikšķiniet uz Rediģēt.
4. Laukā Daudzums ievadiet skaitli.
    * Mainot daudzumu MK rindā, ražošanas pasūtījumam tiek ietekmēta materiālu patēriņa izmaksu prognoze.  
5. Noklikšķiniet uz Saglabāt.
6. Aizvērt lapu.

## <a name="update-the-production-route"></a>Atjaunināt ražošanas maršrutu
1. Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.
2. Noklikšķiniet uz Maršruts.
    * Atveriet lapu Maršruts, lai pārbaudītu ražošanas maršruta datus, kas tika kopēti no noklusējuma datiem, kad tika izveidots pasūtījums. Šajā procedūrā jums ir jāatjaunina daudzums vienai no operācijām ražošanas maršrutā.  
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Noklikšķiniet uz Rediģēt.
5. Laukā Apstrādes daudz. ievadiet kādu skaitli.
    * Mainot apstrādes laiku, tiek ietekmēts ražošanas pasūtījuma prognozētais maršruta patēriņš un izmaksas.  
6. Noklikšķiniet uz Saglabāt.
7. Aizvērt lapu.

