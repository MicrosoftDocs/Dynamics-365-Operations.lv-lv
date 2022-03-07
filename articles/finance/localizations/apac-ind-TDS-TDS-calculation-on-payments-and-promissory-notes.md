---
title: TDS aprēķins maksājumiem un parādzīmēm
description: Šajā tēmā sniegta atsauces informācija par dažādiem maksājumu darījumiem, kam tiek aprēķināts No kopējo ienākumu summas atskaitītais nodoklis (TDS).
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
ms.openlocfilehash: 28afd04b1c341985f7ac15e05aba7a9039a59d869dd5bc60b4163d2ba1ae4ec0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750344"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>TDS aprēķins maksājumiem un parādzīmēm

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegta atsauces informācija par dažādiem maksājumu darījumiem, kam tiek aprēķināts No kopējo ienākumu summas atskaitītais nodoklis (TDS).

| Sērijas numurs | Darījuma veids | Transakciju summa | Lapas nosaukums un ceļš | Konta tips un korespondējošā konta tips |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | Avansa maksājums/maksājums attiecībā pret rēķinu (maksājamais TDS) | Debetkarte vai kredītkarte | <ul><li>Virsgrāmatas žurnāls (**Virsgrāmata \> Žurnāla ieraksti \> Virsgrāmatas žurnāli**)</li><li>Rēķinu žurnāls (**Kreditori \> Rēķini \> Rēķinu žurnāls**)</li><li>Maksājumu žurnāls (**Kreditori \> Maksājumi \> Kreditora maksājumu žurnāls**)</li></ul> | Virsgrāmata (dr.), banka (kr.) |
| 2             | Avansa maksājums/maksājums attiecībā pret rēķinu (debitora pirkums - maksājamais TDS) | Debetkarte vai kredītkarte | <ul><li>Virsgrāmatas žurnāls (**Virsgrāmata \> Žurnāla ieraksti \> Virsgrāmatas žurnāli**)</li><li>Rēķinu žurnāls (**Kreditori \> Rēķini \> Rēķinu žurnāls**)</li><li>Maksājumu žurnāls (**Kreditori \> Maksājumi \> Kreditora maksājumu žurnāls**)</li></ul> | Debitors (dr.), banka (kr.) |
| 3             | Parādzīmes | Debetkarte | Parādzīmju izrakstīšanas žurnāls (**Kreditori \> Maksājumi \> Parādzīmes \> Parādzīmju izrakstīšanas žurnāls**) | Kreditors (dr.), virsgrāmata (kr.) |
| 4             | Dažādi ieņēmumi (saņemamie TDS) | Debetkarte vai kredītkarte | Virsgrāmatas žurnāls (**Virsgrāmata \> Žurnāla ieraksti \> Virsgrāmatas žurnāli**) | Banka (dr.), virsgrāmata (kr.) |
| 5             | Citi izdevumi (maksājamie TDS) | Debetkarte vai kredītkarte | Virsgrāmatas žurnāls (**Virsgrāmata \> Žurnāla ieraksti \> Virsgrāmatas žurnāli**) | Banka (dr.), virsgrāmata (kr.) |

Sekojiet šiem soļiem, lai aprēķinātu TDS maksājumiem un parādzīmēm.

1. Žurnāla lapās izveidojiet žurnāla rindas. Atlasiet konta tipu un korespondējošā konta tipu.
2. Atlasiet **Funkcijas \> Norēķini**, lai atvērtu lapu **Atvērt darījumu rediģēšanu**. Pēc tam atlasiet noteiktu rēķinu, kas ir jāsedz. Ja TDS jau ir aprēķināts rēķina līmenī, lauks **Summas izcelsme** rāda pamatsummu, par kuru TDS tika aprēķināts. **TDS summa** – lauks rāda TDS summa, kas tika aprēķināta darījumam. Lauks **Summa** parāda neto maksājuma summu (t.i., maksājuma summu pēc TDS ieturēšanas).

    > [!NOTE]
    > Maksājumam, kas ir veikts pret rēķinu, ir spēkā šādi nosacījumi:
    >
    > - Ja maksājuma summa un rēķina summa ir vienāda, TDS netiek aprēķināts, ja tas jau ir aprēķināts rēķina līmenī.
    > - Ja rēķina summa pēc TDS summas ieturēšanas ir lielāka nekā maksājuma summa, TDS netiek aprēķināts.
    > - Ja rēķina summa pēc TDS summas ir mazāka nekā maksājuma summa, TDS tiek aprēķināts summai, kas pārsniedz rēķina summu.

3. Lapas **Žurnālu dokuments**, cilnē **Pārskats**, laukā **TDS grupas** pārskatiet vai mainiet noklusējuma TDS grupu, kas noteikta kreditoram vai debitoram. TDS, kas ir aprēķināts žurnāla rindās, ir balstīta uz formulu, kas ir definēta TDS nodokļu kodiem, kas uzskaitīti TDS grupā.

    > [!NOTE]
    > TDS tiek aprēķināts tikai tad, ja opcija **Aprēķināt ieturēto nodokli** ir iestatīta uz **Jā** kreditoram lapā **Kreditori**.

4. Cilnē **Informācija par nodokļiem**, sadaļā **Informācija par uzņēmumu**, laukā **Nosaukums** varat atlasīt uzņēmuma nosaukumu alternatīvām adresēm, kas ir iestatītas uzņēmumam.

    Sadaļā **Ieturētais nodoklis** lauks **Vērtētāja raksturs** rāda kreditora vai debitora vērtētāja kategorijas raksturu. Lauks **Nodokļu konta numurs (TAN)** rāda atlasītā uzņēmuma nodokļu konta numuru (TAN).

5. Atlasiet **Ieturētā nodokļa poga \> Ieturētais nodoklis**, lai atvērtu lapu **Ieturētā nodokļa pagaidu darījumi**. Šīs lapas augšējai daļai ir šādi lauki:

    - **Ieturētā nodokļa kopsumma** - TDS kopsumma, kas tika aprēķināta darījumam TDS grupai.
    - **Vērtība** - kopējā procentuālā vērtība, kas tika izmantota darījuma TDS aprēķinam. Kopējā procentuālā vērtība ir balstīta uz formulu, kas noteikta TDS nodokļu kodiem un pievienota TDS grupai.
    - **Koriģētā ieturētā nodokļa kopsumma** - kopējā koriģētā TDS summa visiem nodokļu kodiem TDS grupā.
    - **TDS** - atlasītā izvēles rūtiņa norāda, ka TDS grupa ir pievienota darījumam.

    Lauki cilnēs **Pārskats**, **Vispārīgi** un **Korekcija** parāda aprēķināto TDS summu un pielāgoto TDS summas informāciju par katru TDS nodokļa kodu, kas pievienots TDS grupai.

6. Atlasiet **Slieksni**, lai atvērtu lapu **Slieksnis**, kur varat pārskatīt sliekšņa ierobežojumu, kas ir definēts TDS nodokļu komponentam, kas ir piesaistīts konkrētam TDS nodokļa kodam.
7. Select **Formulas veidotāju**, lai atvērtu **Formulas veidotāja** lapu, kurā varat pārskatīt noteiktam TDS nodokļa kodam definēto formulu.
8. Aizveriet lapas **Formulas veidotājs** un **Pagaidu ieturētā nodokļa darījumi**, lai atgrieztos **Žurnāla dokumentu** lapā.
9. Apstipriniet un grāmatojiet šo žurnālu. TDS summa, kas tika aprēķināta, tiek grāmatota kreditoru kontā, kas katram TDS nodokļu kodam ir definēts TDS grupā. TDS nodokļu kodu debitoru konti ir definēti **Ieturētā nodokļa kodu** lapā.
10. Atlasiet **Grāmatoto ieturēto nodokli**, lai atvērtu **Ieturētā nodokļa darījumu** lapu. **Vērtība** - lauks parāda kopējo procentuālo vērtību, kas tika izmantota darījuma TDS aprēķinam.

    Cilnes **Pārskats**, **Vispārīgi** un **Summa** lauki rāda TDS summas, kas tika aprēķinātas darījumam piesaistītajai TDS grupai.

11. Pārskatiet TDS aprēķina informāciju par katru TDS nodokļu kodu, kas ir pievienots TDS grupai.

## <a name="generate-payments"></a>Izveidot maksājumus

Lai ģenerētu maksājumus, rīkojieties šādi.

1. Izpildiet kādu no šīm darbībām:

    - Dodieties uz **Kreditori \> Maksājumi \> Kreditora maksājumu žurnāls**.
    - Dodieties uz **Debitori \> Maksājumi \> Debitora maksājumu žurnāls**.
    - Dodieties uz **Kreditori \> Maksājumi \> Parādzīmes \> Parādzīmju izrakstīšanas žurnāls**.
    - Dodieties uz **Debitori \> Maksājumi \> Vekselis \> Izrakstīto vekseļu žurnāls**.
    - Dodieties uz **Debitori \> Maksājumi \> Vekselis \> Atkārtoti izrakstīto vekseļu žurnāls**.

2. Atlasiet **Rindas**.
3. Atlasiet **Funkcijas \> Ģenerēt maksājumus**.
