---
title: Izejošā procesa pārskats
description: Šajā rakstā sniegts pārskats par nosūtīšanas procesu Krājumu vadībā.
author: yufeihuang
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "274363"
- intro-internal
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 4e3c97862858e219d98b4ef9a81b52c6ab1623ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852481"
---
# <a name="outbound-process-overview"></a>Izejošā procesa pārskats

[!include [banner](../includes/banner.md)]

Šajā rakstā sniegts pārskats par nosūtīšanas procesu Krājumu vadībā.

## <a name="output-orders"></a>Izdošanas pasūtījumi

Izdošanas pasūtījumi tiek lietoti, lai pārdošanas pasūtījumu rindas un pārsūtīšanas pasūtījumu rindas saistītu ar izejošajiem izdošanas procesiem, kuros tiek izmantoti izdošanas saraksti.

Kad izdošanas saraksti tiek ģenerēti no pārdošanas pasūtījumiem vai pārsūtīšanas pasūtījumiem, tad izdošanas pasūtījumi un sūtījumi tiek izveidoti automātiski. Izdošanas sarakstam ar sūtījumu ir relācija “viens pret vienu”. Pārsūtīšanas pasūtījuma sūtījumu vai pārdošanas pasūtījuma pavadzīmi var apstrādāt no sūtījuma. 

Nākamajā diagrammā ir parādīts apskats par izejošo pasūtījumu apstrādi. 

[![Apskats par izejošo pasūtījumu apstrādi.](./media/outbound-order.png)](./media/outbound-order.png)

Varat iestatīt izejošās kārtulas, lai definētu, kā programmai ir jāapstrādā izejošais process. Šīs kārtulas varat izmantot, lai kontrolētu nosūtīšanas procesu. Šīs kārtulas jūs it īpaši varat izmantot, lai kontrolētu, kurā nosūtīšanas procesa posmā var veikt nosūtīšanu. Nākamie iestatījumi nosaka veidu, kā tiek apstrādāti izejošie procesi.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Izdošanas maršruta statuss pārdošanas un pārsūtīšanas pasūtījumiem 

Dodieties uz **Debitoru parādi** \> **Iestatījumi** \> **Debitoru parādu parametri** un pēc tam cilnē **Atjauninājumi** atlasiet kādu vērtību laukā **Izdošanas maršruta statuss**.

[![Izdošanas maršruta statusa lauks pārdošanas pasūtījumiem.](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Ja lauks **Izdošanas maršruta statuss** ir iestatīts uz **Pabeigts**, tad šis izdošanas process tiek automātiski izpildīts kā daļa no izdošanas sarakstu ģenerēšanas procedūras. Ja šis lauks ir iestatīts uz **Aktivizēts**, tad izdošanas saraksta rindas ir jāatjaunina manuāli.

Tāda pati iestatīšana attiecas uz pārsūtīšanas pasūtījumiem. Dodieties uz **Krājumu vadība** \> **Iestatījumi** \> **Krājumu un noliktavas vadības parametri** un pēc tam cilnē **Transports** atlasiet kādu vērtību laukā **Izdošanas maršruta statuss**.

[![Izdošanas maršruta statusa lauks pārsūtīšanas pasūtījumiem.](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Beigt izdošanas krājumu pasūtījumus

Dodieties uz **Krājumu vadība** \> **Iestatījumi** \> **Krājumu un noliktavas vadības parametri** un pēc tam cilnē **Vispārīgi** iestatiet opciju **Beigt izdošanas krājumu pasūtījumu**.

[![Opcija Beigt izdošanas krājumu pasūtījumu.](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Ja noliktavas darbinieks samazina izdošanas sarakstā ietvertos daudzumus, no sūtījuma tiek noņemti attiecīgie krājumu pasūtījumā ietvertie daudzumi. Ja noteiktā brīdī tiek atjaunināts izdošanas saraksts un ir iestata opcijas **Beigt krājumu izdošanas pasūtījumu** vērtība **Jā**, atlikušie daudzumi tiek ietverti atpakaļ pasūtījumā. Ja ir iestatīta opcijas **Beigt krājumu izdošanas pasūtījumu** vērtība **Nē**, atlikušie daudzumi tiek saglabāti kā atvērta izdošanas pasūtījuma daudzums un tie ir jāpievieno jaunam izdošanas sarakstam, izmantojot funkcionalitāti **Atvērt izdošanas pasūtījumus**. 

[![Komanda Atvērt izdošanas pasūtījumus izvēlnē Funkcijas.](./media/open-output-order.png)](./media/open-output-order.png)

[![Izvēlne Funkcijas lapā Atvērt izdošanas pasūtījumus.](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Samazināt daudzumu

Trešais parametrs, ko varat izmantot kā daļu no izdošanas sarakstu ģenerēšanas procesa, ir parametrs **Samazināt daudzumu**. Šī parametra iestatījums darbojas kopā ar iestatījumu **Rezervācija**, kas kā daļu no pārvietošanas uz noliktavu izsauc rezervēšanas procesu.

[![Parametrs Samazināt daudzumu.](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Izejošā procesa piemērs pārdošanas pasūtījumam

Šajā piemērā pastāv pārdošanas pasūtījums par diviem krājumiem. Izdošanas saraksta ģenerēšanas laikā jūs atlasāt parametru **Samazināt daudzumu**. Tāpēc izlaišana un izdošanas rindu izveidošana notiek tikai pieejamajiem rīcībā esošajiem krājumiem. Izdošanas ir jāziņo, izmantojot reģistrācijas procesu izdošanas sarakstiem (**Izdošanas maršruta statuss** = **Aktivizēts**).

Krājumi, kas vēl nav rezervēti, tiek rezervēti izdošanas saraksta ģenerēšanas laikā. Nepieejamos krājumus var noņemt no pārdošanas pasūtījuma vai pārvietot uz noliktavu vēlākai izejošajai apstrādei, kad krājumi ir pieejami izdošanai.

[![Atjaunināt izdošanas sarakstu.](./media/update-picking-list.png)](./media/update-picking-list.png)

Tiklīdz visas izdošanas rindas lapā **Izdošanas saraksta reģistrācija** ir izdotas, saistītais sūtījums tiek pabeigts. Pēc tam var uzsākt procesu pārdošanas pasūtījumu pavadzīmēm, pamatojoties uz izdotajiem krājumiem.

[![Atjaunināt izejošos sūtījumus.](./media/outbound-shipments.png)](./media/outbound-shipments.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]