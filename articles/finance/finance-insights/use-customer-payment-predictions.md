---
title: Debitoru maksājumu prognožu izmantošana
description: Šis raksts meklē priekšnosacījumus un plašus soļus, kas nepieciešami Finanšu ieskatu izmēģinājuma versijas izmantošanai.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 330642624b55a6772ef149b70873021401a6bd83
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901407"
---
# <a name="use-customer-payment-predictions"></a>Debitoru maksājumu prognožu izmantošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā izmantot debitoru maksājumu prognozes. Pirms izmantojat šo līdzekli, pārliecinieties, vai esat pabeidzis tā uzstādīšanas darbības. Plašāku informāciju skatiet šeit: [Debitoru maksājumu prognozēšanas iespējošana](enable-cust-paymnt-prediction.md).

Debitoru maksājumu prognozes var skatīt **darbvietā Pārvaldīt debitoru kredītu un atgādinājumus**, kā arī divās jaunās saraksta lapās: darbību **maksājumu prognozēšana** un **debitoru maksājumu prognozēšanas**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Darbvieta Debitora kredīta un iekasēšanas pārvaldība

Klienta **kredīta pārvaldīšanas un iekasēšanas darbvietā** ir ietvertas divas jaunas darbības: **darbību maksājumu prognozes un** **debitoru maksājumu prognozēšanas**.

### <a name="transaction-payment-predictions-list-page"></a>Darījuma maksājuma prognožu saraksta lapa

Saraksta lapā **Darbību maksājumu prognozes** **varat** skatīt maksājumu iespējamību atvērtām darbībām laika, **nokavēta** un ļoti **vēlu intervālos.** Katram darījumam režģī kolonna **Iespējamība Laicīgi** parāda iespējamību, ka rēķins tiks apmaksāts apmaksas datumā vai pirms tā. Ja iespējamība, ka ir maksājums notiks laicīgi, ir mazāka par 50 procentiem, blakus procentuālajai vērtībai kolonnā **Iespējamība: laicīgi** tiek parādīts sarkans aplis, lai norādītu novēlota maksājuma risku.

[![Lapa Maksājumu prognoze katram darījumam.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Lapas labajā pusē esošajā rūtī **Saistītā informācija** tiek rādīta detalizēta informācija par prognozēm.

- Darījuma, kas atlasīts režģī, kopsavilkuma cilne **Maksājumu prognozēšana** rāda detalizētu informāciju par maksājuma prognozēm intervālos **Laicīgi**, **Novēloti** un **Ļoti novēloti**. Sadaļā **Galvenie faktori** ir redzami galvenie faktori, kas ietekmēja prognozes. Galvenie faktori ir konkrētā darījuma un/vai debitora atribūti šim darījumam.
- Kopsavilkuma cilnē **Debitora ieskati** redzams pašreizējais rēķina, maksājuma un iekasēšanas statistika par debitoru atlasītajam darījumam.
- Kopsavilkuma cilnē **Debitora vēsture** tiek radīta debitora maksājumu vēsture intervālos **Laicīgi**, **Novēloti** un **Ļoti novēloti**.

Dati sadaļā **Galvenie faktori** un kopsavilkuma cilnēs **Klientu ieskati** un **Klientu vēsture** palīdz izskaidrot maksājumu prognozes. Tas var palīdzēt palielināt jūsu pārliecību par prognožu efektivitāti.

[![Grafiskie indikatori maksājuma prognozēm rūtī Saistītā informācija.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="customer-payment-predictions-list-page"></a>Debitora maksājuma prognožu saraksta lapa

Debitoru **maksājumu prognozēšanas** saraksta lapa parāda kopējo atvērto bilanci un summu, **kas** ir paredzētu apmaksai laikā, **·** **nokavētos un ļoti vēlu laika** intervālos.

[![Lapa Maksājumu prognozes katram debitoram.](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Maksājuma summa katrā grozā tiek aprēķināta kā darījumu bilances svērtā vidējā summa. Šī summa tiek aprēķināta, pamatojoties uz maksājumu iespējamību katrā grozā.

Piemēram, debitoram ir trīs atvērti darījumi, kam katrā grozā ir tālāk minētās maksājumu iespējamības.

| Darbība | Apjoms | Laicīgi veikta maksājuma iespējamība | Novēloti veikta maksājuma iespējamība | Ļoti novēloti veikta maksājuma iespējamība |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10 procenti                  | 50 procenti               | 40 procenti                    |
| T2          | 1000  | 50 procenti                  | 30 procenti               | 20 procenti                    |
| T3          | 10,000 | 1 procenti                   | 4 procenti                | 95 procenti                    |

Šādā gadījumā maksājumi tiek prognozēti katram grozam tālāk norādītajā veidā.

| Grozi   | Darījums T1      | Darījums T2         | Darījums T3            | Summa |
|-----------|---------------------|------------------------|---------------------------|-------|
| Laikā   | 100 × 10 ÷ 100 = 10 | 1000 × 50 ÷ 100 = 500 | 10 000 × 1 ÷ 100 = 100    | 610   |
| Nokavēts      | 100 × 50 ÷ 100 = 50 | 1000 × 30 ÷ 100 = 300 | 10 000 × 4 ÷ 100 = 400    | 750   |
| Ļoti vēlu | 100 × 40 ÷ 100 = 40 | 1000 × 20 ÷ 100 = 200 | 10 000 × 95 ÷ 100 = 9500 | 9,740 |

Lapas labajā pusē esošajā sadaļā **Saistītā informācija** tiek rādīta detalizēta informācija par prognozēm.

- Darījuma, kas atlasīts režģī, kopsavilkuma cilne **Maksājumu prognozes** rāda detalizētu informāciju par maksājuma prognozēm intervālos **Laicīgi**, **Novēloti** un **Ļoti novēloti**.
- Kopsavilkuma cilnē **Debitora ieskati** redzams pašreizējais rēķina, maksājuma un iekasēšanas statistika par debitoru atlasītajam darījumam.
- Kopsavilkuma cilnē **Debitora vēsture** tiek radīta debitora maksājumu vēsture intervālos **Laicīgi**, **Novēloti** un **Ļoti novēloti**.

Dati, kas ir debitoru ieskatu **un** debitoru **vēstures kopsavilkuma** cilnēs, palīdz skaidrot maksājumu prognozes. Tas var palīdzēt palielināt jūsu pārliecību par prognožu efektivitāti.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Maksājumu prognožu precizitātes uzlabošana

Varat skatīt maksājumu prognožu precizitāti, dodoties uz **Kredīti un iekasēšana \> Iestatīšana \> Finanšu ieskati \> Finanšu ieskatu parametri**. Cilnē **Debitoru maksājumu ieskati** sadaļa **Prognozēšanas modelis** parāda prognozēšanas modeļa precizitāti procentos.

Ja neesat apmierināts ar precizitāti, atlasiet saiti **Uzlabot modeļa precizitāti**, lai atvērtu paplašinājumu AI Builder pieredzi. Paplašinājuma AI Builder pieredzi var atlasīt vai atcelt lauku atlasi, līdz esat atlasījis laukus, kurus uzskatāt par vissvarīgākajiem, lai precīzi prognozētu maksājumu iespējamības. Kad esat pabeidzis, varat viegli saglabāt prognozēšanas modeli un publicēt izmaiņas. Jaunais ierobežotais prognozēšanas modelis automātiski tiks saņemts prognozēm Dynamics 365 finansēs.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
