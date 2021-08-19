---
title: Sliekšņa ierobežojums un izņēmuma sliekšņa ierobežojums
description: Šajā tēmā ir aprakstīts No kopējo ienākumu summas atskaitītā nodokļa (TDS) slieksnis un izņēmuma ierobežojumi.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 510a8904cc36821dbb22d2affab5aa32c269e6d8c57144cc1f4ef3e1ac448334
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774259"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>Sliekšņa ierobežojums un izņēmuma sliekšņa ierobežojums

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts No kopējo ienākumu summas atskaitītā nodokļa (TDS) slieksnis un izņēmuma ierobežojumi. TDS rēķinos un maksājumos vienmēr tiek aprēķināts, ņemot vērā sliekšņa ierobežojumu un izņēmuma sliekšņa ierobežojumu, kas definēti TDS nodokļa komponentiem lapā **ieturētā nodokļa komponenti**. TDS nodokļu komponenti ir pievienoti TDS nodokļu kodiem, kas ir iekļauti TDS nodokļu grupās. TDS nodokļu grupas ir pievienotas kreditoriem un debitoriem, lai aprēķinātu TDS rēķina līmenī vai maksājuma līmenī.

TDS tiek aprēķināts, ja summa darījumam vai kumulatīvajiem darījumiem, kas grāmatotas ar noteiktu TDS grupu kreditoram, pārsniedz sliekšņa ierobežojumu, kas norādīts lapā **ieturētā nodokļa komponenti**. TDS netiks aprēķināts, kamēr kumulatīvā darījuma summa nepārsniedz norādīto sliekšņa ierobežojumu.

Ja kopā ar TDS komponenta sliekšņa ierobežojumu tiek norādīts izņēmuma sliekšņa ierobežojums, TDS tiek aprēķināts, ja noteikta darījuma summa pārsniedz izņēmuma sliekšņa ierobežojumu pat tad, ja kopējā darījuma summa nepārsniedz norādīto sliekšņa ierobežojumu.

### <a name="example"></a>Paraugs
Nodokļu komponents ar nosaukumu TDS ir iestatīts un pievienots TDS nodokļu grupai ar nosaukumu Līgumdarbinieks. Slieksnis ir definēts kā 50 000, un TDS nodokļa komponentam izņēmuma slieksnis ir definēts kā 20 000. TDS grupas līgumdarbinieks ir definēts kā noklusējuma TDS grupa 1. kreditoram.

Pirkšanas rēķins 001 ir grāmatots 1. kreditoram par 10 000. TDS netiek aprēķināts rēķinam, jo rēķina summa nav pārsniegusi sliekšņa ierobežojumu vai izņēmumu sliekšņa ierobežojumu. Pirkšanas rēķins 002 ir grāmatots 1. kreditoram par 25 000. TDS tiek aprēķināts rēķinam, jo rēķina summa ir pārsniegusi izņēmumu sliekšņa ierobežojumu. Pirkšanas rēķins 003 ir grāmatots 1. kreditoram par 20 000. TDS tiek aprēķināts rēķinam, jo trīs kreditoram izsniegto rēķinu kopējā rēķina summa ir pārsniegusi sliekšņa ierobežojumu. TDS tiek aprēķināts visiem rēķiniem, kas tiek izsniegti kreditoram, kuram TDS nav aprēķināts iepriekš. Tādējādi TDS tiek aprēķināts summai 30 000, kas ir kopējā summa rēķiniem 001 un 003.

Sliekšņa ierobežojums un izņēmuma sliekšņa ierobežojums netiek pielietoti TDS aprēķinam, ja izvēles rūtiņa **Ignorēt slieksni** TDS nodokļu kodiem ir atzīmēta darījumam pievienotajā TDS grupā. Sliekšņa ierobežojums netiks izmantots TDS nodokļu kodiem TDS grupā, kurai paredzēta izvēles rūtiņa **Ignorēt slieksni**.

Ja noteiktai TDS grupai dažiem rēķiniem ir atzīmēta izvēles rūtiņa **Ignorēt slieksni**, taču nav atlasīta citiem rēķiniem, kas tika izveidoti noteiktam kreditoram/debitoram, TDS aprēķins, neņemot vērā sliekšņa ierobežojumu dažiem rēķiniem, iespējams, tiks ņemta vērā visu to rēķinu kopējā summa, kuriem TDS nav aprēķināts iepriekš.

Piemēram, sliekšņa ierobežojums ir 25 000. Kreditoram A tiek izveidoti šādi rēķini.

- 1. rēķins – 20 000 – (izvēles rūtiņa **Ignorēt slieksni** nav atzīmēta): TDS netiek aprēķināts.

- 2. rēķins – 4000 – (izvēles rūtiņa **Ignorēt slieksni** ir atzīmēta): TDS tiek aprēķināts uz summu 4000.

- 2. rēķins – 3000 – (izvēles rūtiņa **Ignorēt slieksni** nav atzīmēta): TDS tiek aprēķināts kopējai rēķina summai, t.i., 27 000 (20000+4000+3000), kas pārsniedz sliekšņa ierobežojumu. TDS tiek aprēķināts, pamatojoties uz to rēķinu kopējo summu, kuriem TDS nav aprēķināts iepriekš, t.i., 23 000 (20 000+3000).
