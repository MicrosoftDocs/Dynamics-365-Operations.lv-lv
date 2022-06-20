---
title: Izmaksu objekta dimensijas
description: Analizējot izmaksas, jūs izmantojat izmaksu elementa dimensijas, lai noteiktu, kur plūst izmaksas. Izmaksu objekta dimensijas tiek izmantotas, lai noteiktu, kur var piešķirt izmaksas. Šajā rakstā ir sniegta informācija par izmaksu objektu dimensijām.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3ee481b9dafe202e0a850a31b6ab036d52a20547
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874643"
---
# <a name="cost-object-dimensions"></a>Izmaksu objekta dimensijas

[!include [banner](../includes/banner.md)]

Analizējot izmaksas, jūs izmantojat izmaksu elementa dimensijas, lai noteiktu, kur plūst izmaksas. Izmaksu objekta dimensijas tiek izmantotas, lai noteiktu, kur var piešķirt izmaksas. Šajā rakstā ir sniegta informācija par izmaksu objektu dimensijām.

Izmaksu objekts var būt jebkura veida objekts, kuru vēlaties novērtēt, iedalīt izmaksas vai mērīt pa tiešo. Tipiski izmaksu objekti ietver preces, projektus, resursus, nodaļas, izmaksu centrus un ģeogrāfiskus reģionus. Vadība izmanto izmaksu objektus, lai aprēķinātu izmaksu daudzumu, kā arī veiktu ienesīguma analīzi.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Izmaksu objekta dimensijas un izmaksu objekta dimensijas dalībnieki
Izmaksu objekti tiek saukti par *izmaksu objekta dimensijas*. Pēc tam, kad esat izlēmis, uz kuru elementu jāattiecas izmaksu objekta dimensijai, norādiet atsevišķas dimensijas vērtības, vai arī importējiet tas Izmaksu uzskaitē no citām avota sistēmām. Šīs atsevišķās dimensiju vērtības tiek sauktas par *izmaksu objekta dimensijas dalībnieki*. Piemēram, jūs vēlaties izmantot finanšu dimensiju, kas ir nosaukta Izmaksu centrs kā izmaksu objekta dimensiju. Lai apskatītu, kā izmaksas plūst uz atsevišķiem izmaksu centriem, nepieciešams importēt izmaksu objekta dimensijas dalībniekus. Šajā gadījumā izmaksu objekta dimensijas dalībnieki ir faktiskie izmaksu centri, piemēram, Pārdošana, Ražošana, Administrēšana un Ģeogrāfiskas vietas. Šajā ekrānuzņēmumā parādīts Izmaksu centru kā izmaksu objekta dimensijas piemērs, ar tā faktiskajiem izmaksu centriem kā izmaksu objekta dimensijas dalībniekiem. 

[![Ekrānuzņēmums, kurā izmaksu centri parādīti kā izmaksu objekta dimensija.](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Importējiet izmaksu objekta dimensijas dalībniekus, izmantojot datu savienotājus
Lai atvieglotu izmaksu objekta dimensijas dalībnieku importēšanu, izmantojiet datu savienotājus, lai izgūtu vērtības no elementiem, kurus vēlaties izmantot kā izmaksu objekta dimensijas. Jūs varat izmantot iepriekš izveidotus datu savienotājus vai pielāgotus datu savienotājus, ko esat izveidojis.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
