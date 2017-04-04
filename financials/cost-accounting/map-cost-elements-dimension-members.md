---
title: "Karti dažādu izmaksu elementu dimensiju biedriem kopīgo dimensiju dalībnieku kopu"
description: "Kartējot dažādu izmaksu elementa dimensiju dalībniekus vienotā izmaksu elementa dimensijas dalībnieku kopā, jūs sapludināt datus vispārējā formātā analīzes nolūkiem."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-11-01 13 - 45 - 07
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a1e9817b6ee596ad516531d7597a2a39e115749c
ms.lasthandoff: 03/31/2017


---

# <a name="map-different-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Karti dažādu izmaksu elementu dimensiju biedriem kopīgo dimensiju dalībnieku kopu

Kartējot dažādu izmaksu elementa dimensiju dalībniekus vienotā izmaksu elementa dimensijas dalībnieku kopā, jūs sapludināt datus vispārējā formātā analīzes nolūkiem.

Ja jūs esat globāla kompānija un atbilstat likumā noteiktajām grāmatvedības prasībām, jūs varat izmantot vairākus kontu plānus. Importējot izmaksu elementa dimensijas dalībniekus no dažādiem kontu plāniem, jūs varat nonākt līdz kontu sajaukumam. Tomēr šie konti varētu būt tāda paša rakstura, un jūs varētu vēlēties izanalizēt un sadalīt tiem izmaksas, izmantojot vienotu formātu.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Kartēt izmaksu elementa dimensijas dalībniekus vienotā formātā
Šajā piemērā ir parādīts, kā jūs kā izmaksu kontrolieris varat izveidot jaunu izmaksu elementa dimensiju Izmaksu uzskaitē, kas kartē izmaksu elementa dimensijas dalībniekus no ASV kontu plāna struktūras, un Francijas kontu plāna struktūras vienotā izmaksu elementa dimensijas dalībnieku izmaksu uzskaites kopā. Jūs varat izmantot vienoto izmaksu elementa dimensijas dalībnieku kopu, lai analizētu izmaksu datus no divām juridiskām personām izmaksu uzskaites virsgrāmatā.

| Avots: ASV kontu plāns                                          | Avots: Francijas kontu plāns                                          | Jauna vienota izmaksu elementa dimensijas dalībnieku kopa                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Importēto izmaksu elementa dimensijas dalībnieki no ASV kontu plāna | Importēto izmaksu elementa dimensijas dalībnieki no Francijas kontu plāna | ASV un Francijas izmaksu elementa dimensijas dalībnieku kartēšana vienotā kopā |
| 5001: Pārdošana                                                           | 5001: Pārdošana un reklāma                                               | 5000: Pārdošana un reklāma                                             |
| 5030: Reklāma                                                     | 6390: akciju pirkšanas\*                                                    | 7000: Tīrīšanas izdevumi                                                 |
| 7001: Tīrīšanas izdevumi                                               | 7001: Komandējuma izdevumi                                                      | 7001: Komandējuma izdevumi                                                   |

\*Dimensiju dalībvalstu akciju pirkšanas Francijas izmaksu elements nav kartēts.

## <a name="currency-conversion"></a>Valūtas konvertācija
Dažādus kontu plānus, ko jūs izmantojat iespējams iestatīt izmantošanai dažādās valūtās. Šajā gadījumā noteikti norādiet valūtas konvertāciju, lai izmaksu dati tiek apstrādāti, izmantojot pareizo valūtu, kā definēts izmaksu uzskaites virsgrāmatā, kur tiek izmantoti izmaksu elementa dimensijas dalībnieki. Iepriekšējā piemērā, ja izmaksu uzskaites virsgrāmatā tiek izmantoti ASV dolāri (USD), nepieciešams izveidot valūtas konvertāciju no USD uz eiro (EUR), lai apstrādātu darījumus kartētajiem izmaksu elementa dimensijas dalībniekiem.

## <a name="update-mappings-at-any-time"></a>Atjaunināt kartējumus jebkurā laikā
Jūs varat jebkurā laikā atjaunināt izmaksu elementa dimensijas definīcijas. Tā kā kartējumiem nav stāšanās spēkā datuma, izmaiņas tiek pielietotas nākamajā reizē, kad apstrādājat izmaksu darbības vai izpildot izmaksu aprēķinus.


