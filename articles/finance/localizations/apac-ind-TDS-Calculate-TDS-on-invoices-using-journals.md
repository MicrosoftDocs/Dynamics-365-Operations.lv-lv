---
title: Aprēķināt TDS rēķinos, izmantojot žurnālus
description: Šajā tēmā ir uzskaitīti soļi, lai aprēķinātu No kopējo ienākumu summas atskaitīto nodokli (TDS) žurnālos.
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
ms.openlocfilehash: cfe473f39ee729957924fd7c161aed01138cd507eea56766af35177891676f65
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778897"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>Aprēķināt TDS rēķinos, izmantojot žurnālus

[!include [banner](../includes/banner.md)]

Šajā tēmā ir uzskaitīti soļi, lai aprēķinātu No kopējo ienākumu summas atskaitīto nodokli (TDS) žurnālos.

Sāciet, atverot **Virsgrāmatas žurnāla** lapu (**Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli**).

[![Virsgrāmatas žurnāli.](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. Izveidojiet žurnāla rindas, izmantojot tabulā uzskaitītās žurnāla formas. Atlasiet konta tipu un korespondējošā konta tipu un ievadiet darījuma summu. 

   > [!NOTE]
   > Lapā **Rēķinu apstiprināšanas žurnāls** atlasiet **Meklēt dokumentus** un atlasiet rēķinus, kuros aprēķināt TDS. Apskatiet rēķinus, kas izveidoti **Rēķinu reģistra** lapā vai **Meklēt dokumentus** lapā.  

2. Lapas **Žurnālu dokuments** cilnē **Vispārīgi** skatiet vai modificējiet noklusējuma TDS grupu, kas noteikta kreditoram vai debitoram laukā **TDS grupa**. TDS summa, kas tiek aprēķināta žurnāla rindās, ir balstīta uz formulu, kas definēta TDS nodokļu kodiem, kas uzskaitīti **TDS grupas** laukā. 

   > [!NOTE]
   > Lauks **Ieturētā nodokļu grupa**  un lauks **TCS grupa** kļūst pieejams, ja atlasāt TDS grupu laukā **TDS grupa**. **Ieturēto nodokļu grupas** lauks ir pieejams tikai **Virsgrāmatas žurnāla** lapā. TDS tiek aprēķināts tikai tad, ja izvēles rūtiņa **Aprēķināt ieturēto nodokli** ir atzīmēta kreditoram vai debitoram lapās **Visi kreditori** vai **Visi debitori**.   

3. Atlasiet cilni **Informācija par nodokļiem**. Ja nepieciešams, atlasiet uzņēmuma alternatīvās adreses, kas šajā laukā iestatītas uzņēmumam. Uzņēmuma nosaukumu varat skatīt laukā **Nosaukums**, kas atrodas lauku grupā **Uzņēmuma informācija**. 

4. Skatiet kreditora vai debitora ar nodokli saņēmēja kategorijas būtību laukā **Vērtētāja raksturs**, kas atrodas zem lauka grupas **Ieturētais nodoklis**. Laukā **Nodokļu konta numurs** (**TAN**) skatiet atlasītā uzņēmuma parādītais nosaukuma TAN.  

5. Atlasiet **Ieturēto nodokli** **Ieturētā nodokļa** izvēlnē, lai atvērtu lapu **Ieturētā nodokļa pagaidu darījumi**. Šie lauki tiek parādīti lapas **Ieturētā nodokļa pagaidu darījumi** augšējā rūtī.

   - **Ieturētā nodokļa kopsumma** - TDS kopsumma, kas aprēķināta darījumam TDS grupai.

   - **Vērtība** - kopējā procentuālā vērtība, kas tika izmantota darījuma TDS aprēķinam. Kopējā procentuālā vērtība ir balstīta uz formulu, kas noteikta TDS nodokļu kodiem un pievienota TDS grupai.

   - **Koriģētā ieturētā nodokļa kopsumma** - kopējā koriģētā TDS summa visiem nodokļu kodiem TDS grupā.

   - **TDS** – ja atlasīts, TDS grupa tiek pievienota darījumam.

  Lauki cilnēs **Pārskats**, **Vispārīgi** un **Korekcija** lapā **Pagaidu ieturētā nodokļa darījumi** parāda aprēķināto TDS summu un pielāgoto TDS summas informāciju par katru TDS nodokļa kodu, kas pievienots TDS grupai.

6. Atlasiet **Slieksnis**, lai atvērtu lapu **Slieksnis**. Skatiet sliekšņa ierobežojumu un izņēmuma sliekšņa ierobežojumu, kas definēts TDS nodokļa komponentam, kurš pievienots konkrētam TDS nodokļa kodam šajā lapā.

   Atlasiet **Formulas veidotāju**, lai atvērtu **Formulas veidotāja** formu. Skatiet šajā lapā specifisku TDS nodokļa kodu definēto formulu. Aizveriet lapas **Formulas veidotājs** un **Pagaidu ieturētā nodokļa darījumi**, lai atgrieztos **Žurnāla dokumentu** lapā.

8. Ievadiet pārējo nepieciešamo informāciju. Apstipriniet un grāmatojiet šo žurnālu. TDS summa, kas ir aprēķināta pirkšanas rēķiniem, tiek grāmatota kreditora kontā. TDS summa, kas tiek aprēķināta pārdošanas rēķinos, tiek grāmatota debitoru kontā, kas katrai TDS nodokļu kodam ir definēts TDS grupā. TDS nodokļu kodu kreditoru vai debitoru konti ir definēti **Ieturētā nodokļa kodu** lapā.

9. Atlasiet **Grāmatoto ieturēto nodokli**, lai atvērtu **Ieturētā** **nodokļa** **darījumu** lapu. Laukā **Vērtība** tiek parādīta kopējā procentuālā vērtība, kas tiek izmantota darījuma TDS aprēķinam.

   Lauki cilnēs **Pārskats**, **Vispārīgi** un **Summa** ieturētā nodokļa darījuma lapā parāda aprēķināto TDS summu un pielāgoto TDS summas informāciju par katru TDS nodokļa kodu, kas pievienots TDS grupai.
