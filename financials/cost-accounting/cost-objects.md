---
title: Izmaksu objekta dimensijas
description: "Analizējot izmaksas, jūs izmantojat izmaksu elementa dimensijas, lai noteiktu, kur plūst izmaksas. Izmaksu objekta dimensijas tiek izmantotas, lai noteiktu, kur var piešķirt izmaksas. Šajā tēmā ir sniegta informācija par izmaksas objekta dimensijām."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d38f0aa1c3272d5361e6fcca57d693cfa0042f3c
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="cost-object-dimensions"></a>Izmaksu objekta dimensijas

[!include[banner](../includes/banner.md)]


Analizējot izmaksas, jūs izmantojat izmaksu elementa dimensijas, lai noteiktu, kur plūst izmaksas. Izmaksu objekta dimensijas tiek izmantotas, lai noteiktu, kur var piešķirt izmaksas. Šajā tēmā ir sniegta informācija par izmaksas objekta dimensijām.

Izmaksu objekts var būt jebkura veida objekts, kuru vēlaties novērtēt, iedalīt izmaksas vai mērīt pa tiešo. Tipiski izmaksu objekti ietver preces, projektus, resursus, nodaļas, izmaksu centrus un ģeogrāfiskus reģionus. Vadība izmanto izmaksu objektus, lai aprēķinātu izmaksu daudzumu, kā arī veiktu ienesīguma analīzi.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Izmaksu objekta dimensijas un izmaksu objekta dimensijas dalībnieki
Izmaksu objekti tiek saukti par *izmaksu objekta dimensijas*. Pēc tam, kad esat izlēmis, uz kuru elementu jāattiecas izmaksu objekta dimensijai, norādiet atsevišķas dimensijas vērtības, vai arī importējiet tas Izmaksu uzskaitē no citām avota sistēmām. Šīs atsevišķās dimensiju vērtības tiek sauktas par *izmaksu objekta dimensijas dalībnieki*. Piemēram, jūs vēlaties izmantot finanšu dimensiju, kas ir nosaukta Izmaksu centrs kā izmaksu objekta dimensiju. Lai apskatītu, kā izmaksas plūst uz atsevišķiem izmaksu centriem, nepieciešams importēt izmaksu objekta dimensijas dalībniekus. Šajā gadījumā izmaksu objekta dimensijas dalībnieki ir faktiskie izmaksu centri, piemēram, Pārdošana, Ražošana, Administrēšana un Ģeogrāfiskas vietas. Šajā ekrānuzņēmumā parādīts Izmaksu centru kā izmaksu objekta dimensijas piemērs, ar tā faktiskajiem izmaksu centriem kā izmaksu objekta dimensijas dalībniekiem. 

[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Importējiet izmaksu objekta dimensijas dalībniekus, izmantojot datu savienotājus
Lai atvieglotu izmaksu objekta dimensijas dalībnieku importēšanu, izmantojiet datu savienotājus, lai izgūtu vērtības no elementiem, kurus vēlaties izmantot kā izmaksu objekta dimensijas. Jūs varat izmantot iepriekš izveidotus datu savienotājus vai pielāgotus datu savienotājus, ko esat izveidojis.



