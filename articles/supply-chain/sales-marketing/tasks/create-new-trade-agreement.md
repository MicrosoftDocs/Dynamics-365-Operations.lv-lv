---
title: Jauna pakalpojumu līguma izveide
description: Šajā procedūrā parādīts, kā izveidot tirdzniecības līgumu, kur reģistrēt jaunu preces pārdošanas cenu, par kuru vienojāties ar noteiktu debitoru.
author: omulvad
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 592b3d0265a3be92a5a823c6aabdd40b4e3f0a27
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919945"
---
# <a name="create-a-new-trade-agreement"></a>Jauna pakalpojumu līguma izveide

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā izveidot tirdzniecības līgumu, kur reģistrēt jaunu preces pārdošanas cenu, par kuru vienojāties ar noteiktu debitoru. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Ja jūs izmantojat savus datus pirms sākat veikt šajā ceļvedī aprakstītās darbības, jums ir jāpārliecinās, ka nosaukums Tirdzniecības līgumu žurnāls eksistē un Noklusējuma relācija ir iestatīta uz "Cena (pārdošana)".

## <a name="create-and-post-a-new-trade-agreement-journal"></a>Jauna tirdzniecības līgumu žurnāla izveide un grāmatošana

1. Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Cenas un atlaides > Tirdzniecības līgumu žurnāli**.
2. Klikšķiniet **Jauns**.
3. Laukā **Nosaukums** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. **Darbību rūtī** noklikšķiniet uz **Rindas**.
6. Laukā **Konta kods** atlasiet “Tabula”.
    
    Šajā piemērā tiek atjaunināta cena noteiktam debitoram, kas nozīmē, ka jums ir jāizvēlas Tabula. Ja veicat preču saraksta cenas atjaunināšanu, jāatlasa “Visi”, lai jaunā cena būtu derīga visiem debitoriem. Ja cenas dažādos debitoru segmentos atšķiras, jāatlasa Grupa. Lai atlasītu Grupa, ir jāiestata Debitoru cenu grupas.  

7. Laukā **Konta atlase** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.
8. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
9. Laukā **Krājuma kods** atlasiet “Tabula”.
    
    Ja ievadāt tirdzniecības līgumu, kura tips ir “Cena (pārdošana)”, laukā **Krājuma kods** ir jāatlasa tikai “Tabula”. Tas ir tāpēc, ka cena ir absolūtā vērtība un nevar būt vienāda visiem produktiem vai produktu grupai.
    
10. Laukā **Krājumu saistība** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.
11. Sarakstā atlasiet preci, ko vēlaties ietvert līgumā. Atzīmējiet, kuru preci atlasījāt.  
12. Laukā **No** ievadiet minimālo daudzumu.
    - Ja debitoram ir jāpasūta minimālais daudzums pirms tas var pretendēt uz jaunu cenu, tad ir jānorāda daudzums šeit.  
    - Ievadiet vērtību laukā **Līdz**, lai norādītu maksimālo daudzumu, kuru pārsniedzot līguma cena vairs nebūs spēkā. Ja piedāvājat cenas un atlaides, pamatojoties uz vairākiem daudzuma sadalījuma variantiem, norādiet katru daudzuma grupu kā minimālā un maksimālā daudzuma pāri attiecīgi laukos **No** un **Līdz**.
13. Laukā **Summa valūtā** ievadiet cenu.
14. Sadaļā **Detalizēta informācija** laukā **Sākuma datums** ievadiet datumu, no kura šis līgums ir spēkā.
15. Noklikšķiniet uz **Saglabāt**.
16. Noklikšķiniet uz **Validēt**.
17. Noklikšķiniet uz **Validēt atlasītās rindas.**
18. Noklikšķiniet uz **Labi**.
19. Noklikšķiniet uz **Grāmatot**.
20. Noklikšķiniet uz **Labi**.

## <a name="view-trade-agreements-for-a-product"></a>Ar preci saistīto tirdzniecības līgumu skatīšana

1. Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.
2. Sarakstā atrodiet un atlasiet preci, kuras cenu tikko atjaunojāt.
3. **Darbību rūtī** noklikšķiniet uz **Pārdošana**.
4. Noklikšķiniet uz **Skatīt tirdzniecības līgumus**.
    
    Pārskatiet detalizētu informāciju par tikko izveidoto cenu tirdzniecības līgumu.

5. Aizvērt lapu.

## <a name="additional-resources"></a>Papildu resursi

### <a name="whitepaper"></a>Tehniskais dokuments

Lai iegūtu plašāku informāciju, lejupielādējiet tālāk norādīto papīru (rakstīts AX 2012 atbalstam, bet joprojām tiek piemērots Dynamics 365 Supply Chain Management)

- [Tirdzniecības līgumi](https://download.microsoft.com/download/0/2/9/02972c8b-0159-4936-a3ef-1e64252b2d2f/TradeAgreementsInAX.pdf)

### <a name="community-blogs"></a>Kopienas emuāri

- [Pārdošanas cenas programmā Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]