---
title: Aprēķināt TDS rēķinus, izmantojot pirkšanas pasūtījuma formu un pārdošanas pasūtījuma formu
description: Šajā tēmā ir uzskaitīti soļi, lai aprēķinātu Ieturēto nodokli avotā (TDS) dažādu veidu rēķinos.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023408"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>Aprēķināt TDS rēķinus, izmantojot pirkšanas pasūtījuma formu un pārdošanas pasūtījuma formu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir uzskaitīti soļi ieturētā nodokļa aprēķināšanai avotā (TDS) dažādiem rēķinu tipiem, izmantojot **Pirkšanas pasūtījumu**, **Pirkšanas žurnālu**, **Virspasūtījumu** un **Pārdošanas pasūtījumu** lapas.

1. Veidojiet pirkšanas pasūtījumu, pirkšanas žurnālu, virspasūtījumu vai pārdošanas pasūtījumu, izmantojot norādīto lapu. Ievadiet nepieciešamo informāciju.

2. Atlasiet cilni **Iestatīšana**, lai skatītu kreditora vai debitora vērtētāja raksturu. Šī informācija ir uzskaitīta laukā **Vērtētāja raksturu** lauka grupā **Ieturēto nodokļu grupa**.

3. **TDS grupas** laukā skatiet vai modificējiet noklusējuma TDS grupu, kas noteikta kreditoram vai debitoram.

   > [!NOTE]
   > **TCS grupas** lauks nav pieejams, ja atlasāt TDS grupu laukā **TDS grupa**. TDS tiek aprēķināts tikai tad, ja izvēles rūtiņa **Aprēķināt ieturēto nodokli** ir atzīmēta kreditoram vai debitoram lapā **Visi kreditori** vai **Visi debitori**.  

4. Cilnē **Rindas** izveidojiet krājuma rindas un ievadiet nepieciešamo informāciju.

5. Atlasiet cilni **Iestatījumi** (rindas līmenis), lai apskatītu vai mainītu TDS grupu, kas definēta virsraksta līmenī. TDS grupa tiek rādīta laukā **TDS grupa**, kas atrodas **Ieturēto nodokļu grupas** lauku grupā.

6. Atlasiet cilni **Informācija par nodokļiem** un atlasiet alternatīvās adreses, kas ir iestatīti uzņēmuma nosaukumam, kas tiek parādīts šajā laukā. Uzņēmuma nosaukums ir parādīts laukā **Nosaukums**, kas atrodas lauku grupā **Uzņēmuma informācija**. 

   Atlasītā uzņēmuma nosaukuma TAN tiek parādīts laukā **Nodokļu konta numurs** (**TAN**) lauku grupā **Ieturētais nodoklis**. 

7. Atlasiet **Ieturētais nodokli**, lai atvērtu **Pagaidu ieturētā nodokļa darījumu** lapu. Skatīt sekojošos laukus augšējā rūtī lapā **Ieturētā nodokļa pagaidu darījumi**.

   - **Ieturētā** **nodokļa** **kopsumma** - TDS kopsumma, kas aprēķināta darījumam TDS grupai.

   - **Vērtība** - kopējā procentuālā vērtība, kas tika izmantota darījuma TDS aprēķinam. Kopējā procentuālā vērtība ir balstīta uz formulu, kas noteikta TDS nodokļu kodiem un pievienota TDS grupai.

   - **Koriģētā ieturētā nodokļa kopsumma** - kopējā koriģētā TDS summa visiem nodokļu kodiem TDS grupā.

   - **TDS** – ja atlasīts, TDS grupa tiek pievienota darījumam.

Lauki cilnēs **Pārskats**, **Vispārīgi** un **Korekcija** lapā **Pagaidu ieturētā nodokļa darījumi** parāda aprēķināto TDS summu un pielāgoto TDS summas informāciju par katru TDS nodokļa kodu, kas pievienots TDS grupai.

8. Atlasiet **Slieksnis**, lai atvērtu lapu **Slieksnis**. Skatiet sliekšņa ierobežojumu, kas definēts TDS nodokļa komponentam, kurš pievienots konkrētam TDS nodokļa kodam šajā lapā.

9. Atlasiet **Formulas veidotāju**, lai atvērtu **Formulas veidotāja** lapu. Skatiet šajā lapā specifisku TDS nodokļa kodu definēto formulu. 

10. Grāmatot rēķinu. TDS summa, kas aprēķināta pirkšanas rēķinos, tiek grāmatota maksājumu kontā, un TDS summa, kas aprēķināta pārdošanas rēķinos, tiek grāmatota debitoru kontā, kas ir definēts katram TDS nodokļu kodam TDS grupā. TDS nodokļu kodu kreditoru vai debitoru konti ir definēti **Ieturētā nodokļa kodu** lapā.

11. Atlasiet **Vaicājuma** pogu **> Rēķins > Grāmatots ieturētais nodoklis**, lai atvērtu lapu **Ieturētā nodokļa darījumi**. Varat skatīt kopējo procentuālo vērtību, kas tiek izmantota darījuma TDS aprēķinam laukā **Vērtība**.

Cilnes **Pārskats**, **Vispārīgi** un **Summa** lauki lapā **Ieturētā nodokļa darījumi** tiek parādīta darījumam aprēķinātā TDS informācija. Skatiet TDS aprēķina informāciju par katru TDS nodokļu kodu, kas ir pievienots TDS grupai.
