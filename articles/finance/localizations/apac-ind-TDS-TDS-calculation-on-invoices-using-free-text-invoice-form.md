---
title: TDS aprēķins rēķinos no Brīva teksta rēķina lapas
description: Šajā tēmā skaidrots, kā aprēķināt No kopējo ienākumu summas atskaitīto nodokli (TDS) rēķinos, izmantojot Brīvā teksta rēķina lapu.
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
ms.openlocfilehash: c543876c48eca55eaaa6fd67585ec357dfea276ffbf8abad3c28c6f4cf29f782
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750368"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>TDS aprēķins rēķinos no Brīva teksta rēķina lapas

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā aprēķināt No kopējo ienākumu summas atskaitīto nodokli (TDS) rēķinos, izmantojot **Brīvā teksta rēķina** lapu.

1. Dodieties uz **Debitoru parādi \> Rēķini \> Visi brīva teksta rēķini**.

    [![Brīva teksta rēķinu lapa.](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. Atlasiet **Jauns**, lai izveidotu brīvā teksta rēķinu, un pēc tam ievadiet nepieciešamo informāciju.
3. Atlasiet cilni **Rēķins**. Sadaļā **Ieturētā nodokļa grupa** lauks **Vērtētāja raksturs** parāda klienta atzīmju kategorijas veidu.
4. **TDS grupas** laukā pārskatiet vai mainiet noklusējuma TDS grupu, kas noteikta debitoram.

    > [!NOTE]
    > **TCS grupas** lauks nav pieejams, kad atlasāt vērtību laukā **TDS grupa**. TDS tiek aprēķināts tikai tad, ja opcija **Aprēķināt ieturēto nodokli** ir iestatīta uz **Jā** debitoram lapā **Visi debitori**.

5. Cilnē **Informācija par nodokļiem**, sadaļā **Informācija par uzņēmumu**, laukā **Nosaukums** atlasiet uzņēmuma nosaukumu alternatīvai adresei, kas ir iestatīta uzņēmumam.

    Sadaļā **Ieturētais nodoklis** lauks **Nodokļu konta numurs (TAN)** rāda atlasītā uzņēmuma nodokļu konta numuru (TAN).

6. Cilnē **Rēķina rindas** izveidojiet rēķina rindas un ievadiet nepieciešamo informāciju.

    Sadaļas **Ieturēto nodokļu grupa** laukā **Nodokļu konta numurs (TAN)** ir redzams TAN, un **TDS grupas** laukā ir redzama TDS grupa.

7. Atlasiet **Ieturētais nodokli**, lai atvērtu **Pagaidu ieturētā nodokļa darījumu** lapu. Šīs lapas augšējai daļai ir šādi lauki:

    - **Ieturētā nodokļa kopsumma** - TDS kopsumma, kas tika aprēķināta darījumam TDS grupai.
    - **Vērtība** - kopējā procentuālā vērtība, kas tika izmantota darījuma TDS aprēķinam. Kopējā procentuālā vērtība ir balstīta uz formulu, kas noteikta TDS nodokļu kodiem un pievienota TDS grupai.
    - **Koriģētā ieturētā nodokļa kopsumma** - kopējā koriģētā TDS summa visiem nodokļu kodiem TDS grupā.
    - **TDS** - atlasītā izvēles rūtiņa norāda, ka TDS grupa ir pievienota darījumam.

    Lauki cilnēs **Pārskats**, **Vispārīgi** un **Korekcija** parāda aprēķināto TDS summu un pielāgoto TDS summas informāciju par katru TDS nodokļa kodu, kas pievienots TDS grupai.

8. Atlasiet **Slieksni**, lai atvērtu lapu **Slieksnis**, kur varat pārskatīt sliekšņa ierobežojumu, kas ir definēts TDS nodokļu komponentam, kas ir piesaistīts konkrētam TDS nodokļa kodam.
9. Select **Formulas veidotāju**, lai atvērtu **Formulas veidotāja** lapu, kurā varat pārskatīt noteiktam TDS nodokļa kodam definēto formulu.
10. Grāmatot brīva teksta rēķinu. TDS summa, kas tiek aprēķināta brīvā teksta rēķinam, tiek grāmatota debitoru kontā, kas katrai TDS nodokļu kodam ir definēts TDS grupā. TDS nodokļu kodu debitoru konti ir definēti **Ieturētā nodokļa kodu** lapā.
11. Atlasiet **Grāmatoto ieturēto nodokli**, lai atvērtu **Ieturētā nodokļa darījumu** lapu. **Vērtība** - lauks parāda kopējo procentuālo vērtību, kas tika izmantota darījuma TDS aprēķinam.

    Cilņu **Pārskats**, **Vispārīgi** un **Summa** laukos rāda TDS summas, kas aprēķinātas rēķina rindās.

12. Pārskatiet TDS aprēķina informāciju par katru TDS nodokļu kodu, kas ir pievienots TDS grupai.
