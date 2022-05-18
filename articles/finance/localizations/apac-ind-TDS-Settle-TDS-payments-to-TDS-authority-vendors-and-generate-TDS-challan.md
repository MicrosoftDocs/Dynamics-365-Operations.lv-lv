---
title: Segt TDS maksājumus TDS iestādes kreditoriem un izveidot TDS challan
description: Šajā tēmā skaidrots, kā nomaksāt No kopējo ienākumu summas atskaitīto nodokļa (TDS) maksājumus TDS iestādes kreditoriem.
author: kailiang
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e9dcf2e9d5fc1a1f9eae9d93050b0831bd42f78c
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725544"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a>Segt TDS maksājumus TDS iestādes kreditoriem un izveidot TDS challan

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā nomaksāt No kopējo ienākumu summas atskaitīto nodokļa (TDS) maksājumus TDS iestādes kreditoriem.

1. Dodieties uz **Kreditori \> Maksājumi \> Kreditora maksājumu žurnāls**.

    [![Kreditora maksājumu žurnāla rinda.](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)

2. Lapā **Kreditoru maksājumu žurnāls** izvēlieties **Jauns**, lai izveidotu žurnāla rindu.
3. Laukā **Konts** atlasiet TDS iestādes kreditoru, kuram veikt TDS maksājumus.
4. Atlasiet **Norēķinu darījumi**, lai atvērtu lapu **Norēķinu darījumi**, kur jūs variet skatīt nosegtos TDS darījumus TDS iestādes kreditoram.

    Norēķinu perioda laikā norēķinātie TDS darījumi tiek parādīti šādi:

    - TDS darījumi, kuros vērtētāja rakstura kategorija ir **Uzņēmums**, tiek parādīti kā viena darījumu rinda.
    - TDS darījumi, kur vērtētāja rakstura kategorija ir **HUF**, **Firma**, **Individuāls**, **AOP**, **BOI**, **Vietējā pašvaldība** vai **Citi**, tiek rādītas kā viena darījuma rinda.
    - Laukā **Summa** ir norādīta kopējā TDS summa, kas jāsamaksā TDS iestādes kreditoram.

5. Atlasiet **Ieturētā nodokļa darījumi**, lai apskatītu dažādus TDS darījumus, kas ir iekļautas norēķinu ierakstam. Varat apskatīt katras TDS darījumu sadalījumu, kas šajā lapā ir iekļauts apmaksas perioda norēķinu procesā.
6. Cilnē **Pārskats** atzīmējiet izvēles rūtiņu **Atzīmēt** TDS darījumiem, lai norēķinātos ar TDS iestādes kreditoru.

    Cilne **Pārskats** parāda šādu informāciju par katru atvērto TDS darījumu:

    - **Datums** – pievienojiet TDS darījuma datumu.
    - **Dokuments** - virsgrāmatas dokumenta numurs.
    - **Avots** - modulis, kurā TDS darījums tiek ievietots.
    - **Kreditors/debitors** - kreditora vai debitora konta numurs, no kura TDS tiek atskaitīts.
    - **Ieturēšanas saņēmēja/puses nosaukums** – kreditora vai debitora nosaukums, no kura TDS tiek atskaitīts.
    - **Vērtētāja raksturs** – vērtētāja rakstura kategorija, kam pieder atskaitāmais.
    - **Summa** – rēķina summa, pēc kuras tika aprēķināta TDS.
    - **Nodokļu summa** – TDS summa, kas tika aprēķināta darījumam.

    > [!NOTE]
    > Notīriet izvēles rūtiņu **Atzīmēt** visiem TDS darījumiem, kas nav jānosedz TDS iestādes kreditoram.

    Cilnē **Vispārīgi** lauks **PAN** parāda atskaitāmā saņēmēja pastāvīgo konta numuru (PAN). Lauks **Datums** parāda TDS aprēķina datumu, un lauks **Vērtība** rāda kopējo procentu likmi, kas tika izmantota TDS aprēķinam.

7. Atlasiet **Dokuments**, lai apskatītu dokumentu ierakstus TDS darījumam.
8. Aizvērt lapu.
10. Atlasiet **Ieturētā nodokļa komponentus**, lai atvērtu lapu **Ieturētā nodokļa komponenti**, kur varat skatīt TDS, kas tika aprēķināti uz TDS nodokļa komponentu noteiktam TDS nodokļa kodam.

    Cilnē **Pārskats** lauks **Nodokļu komponents** rāda TDS nodokļa sastāvdaļu, kas tika izmantota darījumam. Lauks **Summa** rāda TDS summu, kas tika aprēķināta TDS nodokļa komponentam pamatvalūtā. Lauks **Uzkrātā summa** parāda kopējo TDS summu, kas tika aprēķināta TDS nodokļa komponentam visiem nosegtajiem darījumiem.

    Cilnē **Summa** sadaļa **Noklusētā valūta** rāda TDS summu, kas tika aprēķināta TDS nodokļa komponentam noklusētajā valūtā. Sadaļa **Sekundārā valūta** parāda summu sekundārajā valūtā.

11. Aizveriet lapu **Ieturētā nodokļa komponenti**.
12. Lapā **Atvērt darījumu rediģēšanu**, laukā **Summa** ievērojiet, ka ir atjaunināta kopējā norēķinu perioda summa, kas jāsedz TDS iestādes kreditoram.
13. Lai nokārtotu dažādu TDS norēķinu periodu darījumus ar TDS iestādes kreditoru, atzīmējiet izvēles rūtiņu **Atzīmēt** darījumiem.
14. Aizveriet lapu **Atvērt darījumu rediģēšanu**.

    > [!NOTE]
    > Ja norēķinam lapā **Ieturētā nodokļa darījumi** ir atlasīti tikai daži darījumi, atlasīto darījumu kopējā TDS summa tiek atjaunināta laukā **Labošana**, lapā **Atvērt darījumu rediģēšanu**. Labojuma summa tiek atjaunināta žurnāla rindā **Žurnāla dokumenta** lapā, un lapa **Atvērt darījumu rediģēšanu** tiek aizvērta.

    Lapā **Žurnāla dokuments** lauks **Debets** parāda kopējo summu, kas jāapmaksā TDS iestādes kreditoram.

15. Ievadiet detalizētu informāciju par korespondējošo kontu.

    > [!NOTE]
    > Ja TDS darījumiem ir atšķirīgas nodokļa kontu numuri (TAN), žurnāla rindas tiek izveidotas pēc TAN lapā **Žurnāla dokuments**.

16. Cilnē **Papildmaksas**, laukā **Maksas ID** field, atlasiet maksas ID, kura maksas tips ir **Procenti** vai **Citi**, lai iekasētu papildmaksu par aizkavētiem maksājumiem, kas veikti TDS iestādes kreditoram.

    Cilnes **Informācija par nodokļiem** sadaļā **Uzņēmuma informācija** lauks **Nosaukums** parāda uzņēmuma nosaukumu. **Ieturētā nodokļa** sadaļā lauks **Nodokļu konta numurs (TAN)** rāda TAN, kas ir piesaistīts darījuma rindai.

17. Apstipriniet un grāmatojiet šo žurnālu.
18. Atlasiet **Ieturētais nodoklis \> Challan informācija**, lai ievadītu detalizētu informāciju par darījumu.

    **Dokuments** – lauks parāda darījuma dokumenta numuru.
    
19. Atzīmējiet izvēles rūtiņu **TDS, kas deponēti ar grāmatas ierakstu**, ja TDS summa ir deponēta, izmantojot grāmatas ierakstu.
20. Laukā **Challan numurs** ievadiet challan numuru, kas tiek izmantots, lai veiktu maksājumu TDS iestādes kreditoram.
21. Laukā **Datums** ievadiet challan datumu.
22. Laukā **Bankas nosaukums** atlasiet tās bankas nosaukumu, kurai ir jāiemaksā TDS summa, kas jāmaksā TDS iestādes kreditoram. Šajā laukā ir uzskaitīti visi bankas konti, kas tika iestatīti TDS iestādes kreditoram, sadaļā **Kreditori \> Visi kreditori \> Iestatīt \> Bankas konti**.
23. Laukā **BSR kods** ievadiet bankas Pamata statistiskās atgriešanas (BSR) kodu.
24. Aizvērt lapu.

### <a name="example"></a>Paraugs

Periods 01/04/2009 tiek nosegts ar **Nomas** TDS komponentu grupu, izmantojot periodisko TDS norēķinu procesu. Kopējā TDS 141 625,00 summa tiek grāmatota TDS kreditora iestādes kontā TDS norēķinu periodam. Šo summu var skatīt laukā **Summa**, lapā **Atvērt darījumu rediģēšanu** TDS iestādes kreditoram.

Ja jūs izvēlieties **Ieturētā nodokļa darījumi**, lai aplūkotu dažādus TDS darījumus, kas tika nosegti konkrētam periodam, tiek parādīta šāda informācija.

| TDS summa |
|------------|
| 16,995.00  |
| 22,660.00  |
| 28,325.00  |
| 16,995.00  |
| 28,325.00  |
| 16,995.00  |
| 11,330.00  |

Konkrētai TDS summai, varat atlasīt **Ieturētā nodokļa komponentus**, lai skatītu TDS, kas tika aprēķināti uz TDS nodokļa komponentu noteiktam TDS nodokļa kodam. Šajā piemērā jūs atlasāt **Ieturētā nodokļa komponentus** TDS summai 16 995,00. Tiek parādīta nodokļa summa, kas aprēķināta katram darījuma komponentam.

| Nodokļa komponents | Apjoms    | Akumulētā summa |
|---------------|-----------|--------------------|
| TDS           | 1,5000.00 | 125,000.00         |
| Piemaksa     | 1,500.00  | 12,500.00          |
| PE-Cess       | 330.00    | 2,750.00           |
| SHE Cess      | 165.00    | 1,375.00           |

Ja jūs atlasījāt tikai TDS summas 16 995,00, 22 660,00 un 28 325,00 norēķiniem lapā **Ieturētā nodokļa darījumi** page, kopējā norēķinu summa tiek parādīta kā **67 980,00** laukā **Labošana**, lapā **Atvērt darījumu rediģēšanu**. Ja šis darījums ir atzīmēts norēķinam, un lapa **Atvērt darījumu rediģēšanu** ir aizvērta, summa **67 980,00** tiek parādīta laukā **Debets**, lapā **Žurnāla dokuments**.

Tagad varat grāmatot žurnālu un ģenerēt TDS challan maksājumu.

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a>Avansa maksājumu korekcija, kas tiek veikta TDS iestāžu kreditoriem

Lai pielāgotu avansa maksājumu, kas veikts TDS iestādes kreditoram par faktisko maksājumu, dodieties uz sadaļu **Kreditori \> Kreditori \> Visi kreditori \> Darījumu rediģēšana**. Ja faktiskais maksājums, kas ir veikts, pārsniedz avansa maksājumu, darījumam tiek ģenerēti divi challan maksājumu numuri. Tomēr TDS vaicājumā tiek parādīts tikai pirmais challan maksājumu numurs.
