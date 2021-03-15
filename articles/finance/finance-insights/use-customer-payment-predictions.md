---
title: Debitora maksājumu prognožu izmantošana (priekšskatījums)
description: Šī tēma izskata priekšnosacījumus un vispārējās darbības, kas ir nepieciešamas, lai izmantotu finanšu ieskatu izmēģinājuma versiju.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: e0445046d8016dfa2c02c1ff1a05bdd148f9409a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969257"
---
# <a name="use-customer-payment-predictions-preview"></a>Debitora maksājumu prognožu izmantošana (priekšskatījums)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā ir paskaidrots, kā izmantot debitoru maksājumu prognozes. Pirms izmantojat šo līdzekli, pārliecinieties, vai esat pabeidzis tā uzstādīšanas darbības. Plašāku informāciju skatiet šeit: [Debitoru maksājumu prognozēšanas iespējošana](enable-cust-paymnt-prediction.md).

Varat skatīt debitoru maksājumu prognozes, kas atrodas darbvietā **Debitoru kredīta un kolekcijas pārvaldība** un divās jaunās saraksta lapās, **Maksājumu prognozes katram darījumam** un **Maksājumu prognozes katram debitoram**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Darbvieta Debitora kredīta un iekasēšanas pārvaldība

Darbvietā **Debitora kredīta un iekasēšanas pārvaldība** ietver divus jaunus elementus, **Maksājumu prognozes katram darījumam** un **Debitori ar prognozētajām augstajām kavējuma bilancēm**.

- Elements **Maksājumu prognoze katram darījumam** rāda atvērto debitora darījumu skaitu, kam ir iespējamība, ka maksājums tiks saņemts **Laicīgi**, ir mazāka par 50 procentiem. Varat atlasīt šo elementu, lai atvērtu saraksta lapu **Maksājumu prognozes katram darījumam**.
- Elements **Debitori ar prognozētajām augstajām kavējuma bilancēm** parāda to klientu skaitu, kuriem tiek prognozēts, ka vairāk nekā puse (50 procenti) no kopējās bilances tiks apmaksāta novēloti un/vai ļoti novēloti. Varat atlasīt šo elementu, lai atvērtu saraksta lapu **Maksājumu prognoze katram debitoram**.

[![Darbvieta Debitora kredīta un iekasēšanas pārvaldība](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)

### <a name="payment-predictions-per-transaction-list-page"></a>Saraksta lapa Maksājumu prognozes katram darījumam

Saraksta lapā **Maksājumu prognozes katram darījumam** var skatīt maksājumu iespējamību par atvērtiem darījumiem (**Laicīgi**, **Novēloti** un **Ļoti novēloti**). Katram darījumam režģī kolonna **Iespējamība Laicīgi** parāda iespējamību, ka rēķins tiks apmaksāts apmaksas datumā vai pirms tā. Ja iespējamība, ka ir maksājums notiks laicīgi, ir mazāka par 50 procentiem, blakus procentuālajai vērtībai kolonnā **Iespējamība: laicīgi** tiek parādīts sarkans aplis, lai norādītu novēlota maksājuma risku.

[![Lapa Maksājumu prognoze katram darījumam](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Lapas labajā pusē esošajā rūtī **Saistītā informācija** tiek rādīta detalizēta informācija par prognozēm.

- Darījuma, kas atlasīts režģī, kopsavilkuma cilne **Maksājumu prognozēšana** rāda detalizētu informāciju par maksājuma prognozēm intervālos **Laicīgi**, **Novēloti** un **Ļoti novēloti**. Sadaļā **Galvenie faktori** ir redzami galvenie faktori, kas ietekmēja prognozes. Galvenie faktori ir konkrētā darījuma un/vai debitora atribūti šim darījumam.
- Kopsavilkuma cilnē **Debitora ieskati** redzams pašreizējais rēķina, maksājuma un iekasēšanas statistika par debitoru atlasītajam darījumam.
- Kopsavilkuma cilnē **Debitora vēsture** tiek radīta debitora maksājumu vēsture intervālos **Laicīgi**, **Novēloti** un **Ļoti novēloti**.

Dati sadaļā **Galvenie faktori** un kopsavilkuma cilnēs **Klientu ieskati** un **Klientu vēsture** palīdz izskaidrot maksājumu prognozes. Tas var palīdzēt palielināt jūsu pārliecību par prognožu efektivitāti.

[![Grafiskie indikatori maksājuma prognozēm rūtī Saistītā informācija](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="payment-prediction-per-customer-list-page"></a>Saraksta lapa Maksājumu prognoze katram debitoram

Saraksta lapa **Maksājumu prognoze katram debitoram** parāda kopējo atvērto bilanci un summu, kas tiek prognozēta apmaksai intervālos **Laicīgi**, **Novēloti** un **Ļoti novēloti**.

[![Lapa Maksājumu prognozes katram debitoram](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

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

- Darījuma, kas atlasīts režģī, kopsavilkuma cilne **Maksājumu prognozes** rāda detalizētu informāciju par maksājuma prognozēm intervālos **Laicīgi**, **Novēloti** un **Ļoti novēloti**. Sadaļā **Galvenie faktori** ir redzami galvenie faktori, kas ietekmēja maksājumus. Galvenie faktori ir konkrētā darījuma un/vai debitora atribūti šim darījumam.
- Kopsavilkuma cilnē **Debitora ieskati** redzams pašreizējais rēķina, maksājuma un iekasēšanas statistika par debitoru atlasītajam darījumam.
- Kopsavilkuma cilnē **Debitora vēsture** tiek radīta debitora maksājumu vēsture intervālos **Laicīgi**, **Novēloti** un **Ļoti novēloti**.

Dati sadaļā **Galvenie faktori** un kopsavilkuma cilnēs **Klientu ieskati** un **Klientu vēsture** palīdz izskaidrot maksājumu prognozes. Tas var palīdzēt palielināt jūsu pārliecību par prognožu efektivitāti.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Maksājumu prognožu precizitātes uzlabošana

Varat skatīt maksājumu prognožu precizitāti, dodoties uz **Kredīti un iekasēšana \> Iestatīšana \> Finanšu ieskati \> Finanšu ieskatu parametri**. Cilnē **Debitoru maksājumu ieskati** sadaļa **Prognozēšanas modelis** parāda prognozēšanas modeļa precizitāti procentos.

[![Maksājumu prognožu precizitāte](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Ja neesat apmierināts ar precizitāti, atlasiet saiti **Uzlabot modeļa precizitāti**, lai atvērtu AI Builder paplašinājumu. AI Builder paplašinājumā varat atlasīt vai atcelt lauku atlasi, kamēr jūs esat atlasījis laukus, kas, jūsuprāt, ir vissvarīgākie, lai precīzi prognozētu maksājumu iespējamību. Kad esat pabeidzis, varat viegli saglabāt prognozēšanas modeli un publicēt izmaiņas. Jaunais apmācītais prognozēšanas modelis tiks automātiski izvēlēts prognozēm pakalpojumā Dynamics 365 Finance.

[![AI Builder paplašinājums](./media/ai-builder.png)](./media/ai-builder.png)

## <a name="release-details"></a>Informācija par izlaišanu

Finanšu ieskatu publiskais priekšskatījums izmēģinājuma izvietošanai ir pieejams Amerikas Savienotajās Valstīs, Eiropā un Apvienotajā Karalistē. Korporācija Microsoft pakāpeniski pievieno atbalstu citiem reģioniem.

Publiskā priekšskatījuma līdzekļus var un vajadzētu ieslēgt tikai 2. līmeņa smilškastes vidēs. Iestatīšanas un mākslīgā intelekta modeļus, kas izveidoti smilškastes vidē, nevar migrēt uz ražošanas vidi. Lai iegūtu papildu informāciju, skatiet rakstu [Microsoft Dynamics 365 Previews lietošanas papildu nosacījumi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti

Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]