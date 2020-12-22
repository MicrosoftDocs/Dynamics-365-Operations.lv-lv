---
title: Ieņēmumu atzīšana pārdošanas pasūtījumos
description: Šajā tēmā aprakstīta pamata funkcionalitāte ieņēmumu atzīšanai pārdošanas pasūtījumos un rēķinos. Ieņēmumu atzīšana ir pieejama pārdošanas pasūtījumā un attiecīgajā rēķinā, kas tiek izveidots no pārdošanas pasūtījuma.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 6e2eafc6785aaf9bc7421bc80c90fa4a7f98a2d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459458"
---
# <a name="revenue-recognition-on-sales-orders"></a>Ieņēmumu atzīšana pārdošanas pasūtījumos

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Ieņēmumu atzīšanas līdzekli nav iespējams ieslēgt, izmantojot līdzekļu pārvaldību. Pašlaik jāizmanto konfigurācijas atslēgas, lai to ieslēgtu.

Šajā tēmā aprakstīta pamata funkcionalitāte ieņēmumu atzīšanai pārdošanas pasūtījumos un rēķinos. Ieņēmumu atzīšana ir pieejama pārdošanas pasūtījumā un attiecīgajā rēķinā, kas tiek izveidots no pārdošanas pasūtījuma. Pārdošanas pasūtījumu var arī izveidot, izmantojot laika un materiālu projektu.

> [!NOTE]
> Attēlos šajā tēmā kolonnas ir paslēptas vai pievienotas režģiem, lai labāk attēlotu koncepcijas. Tādēļ lapas un dati attēlos var atšķirties no tā, ko redzat risinājumā.

## <a name="enter-a-sales-order"></a>Pārdošanas pasūtījuma ievade

Tālāk norādītais pārdošanas pasūtījums ir ievadīts un tajā ir iekļauti trīs krājumi, kas iestatīti ieņēmumu atzīšanai.

[![Pārdošanas pasūtījuma ievade](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

Pastāv divas ieņēmumu atzīšanas koncepcijas.

- **Ieņēmumu cenas noteikšana.** Ieņēmumu cena tiek aprēķināta, pamatojoties uz izlaisto preču iestatījumiem. Ieņēmumu cena nekad netiek rādīta debitoram, bet tā tiek izmantota tikai pārdošanas pasūtījuma rēķina uzskaitei. Pārdošanas pasūtījuma rindās un dokumentos, kas tiek drukāti pārdošanas ietvaros, joprojām ir redzama vienības/saraksta cena.
- **Noteikt, kad jāveic ieņēmumu atzīšana.** Ieņēmumu grafiks tiek izmantots, lai noteiktu, kad ieņēmumi ir jāatzīst.

    Šajā piemērā pirmais krājums (S0001) ir piešķirts **1O** (viena gadījuma) ieņēmumu grafikam. Šī rinda norāda atskaites punkta veida scenāriju, kurā ieņēmumi tiks atzīti pēc instalācijas veikšanas nākotnē. Tādēļ ieņēmumi tiks atlikti līdz instalēšanas pabeigšanai.

    Otrais krājums (S0008) ir pakalpojumu krājums, kas ir iestatīts kā krājums, kura līguma atbalsts tiek grāmatots (PCS). Nepārtrauktie inženierijas pakalpojumi tiek sniegti debitoram 12 mēnešu periodā. Tādēļ ieņēmumu grafiks **12M** tiek piešķirts precei pēc noklusējuma. Tā kā šis krājums ir PCS krājums, jādefinē līguma sākuma un beigu datumi. Pēc noklusējuma līguma sākuma un beigu datumi ir atrodami detalizētajā informācijā par krājumu — cilne Iestatījumi. Ieņēmumu grafikā iestatījums elementam **12M** ir definēts tā, lai līguma nosacījumi tiktu aizpildīti automātiski, kā parādīts attēlā tālāk.

    [![Ieņēmumu grafiki](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    Trešais krājums (S0012) ir aparatūra, un ieņēmumu grafiks netiek piešķirts pēc noklusējuma. Ieņēmumi no aparatūras tiek atzīti, tiklīdz krājums ir iekļauts rēķinā.

## <a name="confirm-the-sales-order"></a>Pārdošanas pasūtījuma apstiprināšana

Lai skatītu papildu informāciju par ieņēmumu cenu un ieņēmumu grafiku, izmantojiet pogas grupā **Ieņēmumu atzīšana** cilnē **Pārvaldīt**, kas atrodas pārdošanas pasūtījuma darbību rūtī. Tā kā šajā brīdī pārdošanas pasūtījums nav apstiprināts, pogas, kas tiek izmantotas ieņēmumu atzīšanai, nav pieejamas. Šīs pogas kļūst pieejamas vai nav pieejamas, virzot pārdošanas pasūtījumu cauri posmiem tā izpildei.

[![Pārdošanas pasūtījuma virsraksts](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

Pirmās trīs pogas sniedz detalizētu informāciju par krājumu ieņēmumu cenu pārdošanas pasūtījuma iestatījumos ieņēmumu atzīšanai.

- **Ieņēmumu cenas sadalījums** — šī poga kļūst pieejama pēc pārdošanas pasūtījuma apstiprināšanas vai rēķina iegrāmatošanas. Apstiprinot pārdošanas pasūtījumu un iegrāmatojot rēķinu, tiek aprēķināti ieņēmumi, lai atzītu cenu, kas tiks atzīta vai atlikta uzskaites ierakstā. Atkarībā no iestatījumiem aprēķinātā ieņēmumu cena var atšķirties no vienības cenas, kas tiek rādīta debitoram.
- **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām** — šī poga kļūst pieejama pēc pārdošanas pasūtījuma apstiprināšanas vai rēķina iegrāmatošanas. Atkārtotas sadales process tiek izmantots, lai pārrēķinātu ieņēmumus, kas ir jāatzīst pēc jaunas rindas pievienošanas pašreizējam pārdošanas pasūtījumam, iekļaujot to rēķinā, vai jaunam pārdošanas pasūtījumam. Abos gadījumos jauna krājuma pievienošana izraisa līguma izmaiņas. Tādēļ ieņēmumu cena ir jāsadala atkārtoti.
- **Atjaunināt ieņēmumu cenas sadalījumu** — šī poga kļūst pieejama pēc pārdošanas pasūtījuma apstiprināšanas, bet pēc pārdošanas pasūtījuma iekļaušanas rēķinā tā vairs nav pieejama. Atjaunināšana tiek izmantota, lai atkārtoti palaistu ieņēmumu cenas sadalījumu bez nepieciešamības apstiprināt pārdošanas pasūtījumu. Pēc pārdošanas pasūtījuma iekļaušanas rēķinā ieņēmumu cenu nevar pārrēķināt.

Pēdējās divas pogas sniedz detalizētu informāciju par ieņēmumu grafiku tiem pārdošanas pasūtījumā iekļautajiem krājumiem, kuriem ir ieņēmumu grafiks.

- **Plānotais ieņēmumu atzīšanas grafiks** — šī poga kļūst pieejama pēc pārdošanas pasūtījuma apstiprināšanas, bet pēc pārdošanas pasūtījuma iekļaušanas rēķinā tā vairs nav pieejama. Tiek atvērta lapa, kas attēlo plānoto ieņēmumu grafiku. Galīgais grafiks var mainīties, jo plānotajā grafikā tiek izmantots pieprasītais nosūtīšanas datums, savukārt galīgajā grafikā tiek izmantots faktiskais nosūtīšanas datums.
- **Ieņēmumu atzīšanas grafiks** — šī poga kļūst pieejama pēc pārdošanas pasūtījuma iekļaušanas rēķinā. Galīgais ieņēmumu atzīšanas grafiks netiek izveidots, kad tiek veikta apstiprināšana vai izveidota pavadzīme. Tas tiek izveidots tikai tad, kad pārdošanas pasūtījums ir iekļauts rēķinā.

Tālāk esošajā piemērā ieņēmumu cenas sadalījums tika veikts pēc pārdošanas pasūtījuma apstiprināšanas. Ņemiet vērā, ka pat tad, ja ieņēmumu cenas tiek sadalītas dažādi, kopējai summai laukā **Atzīstamie ieņēmumi** ir jābūt vienādai ar to pārdošanas pasūtījuma rindu summu, kas tiek iekļautas rēķinā debitoram. Piemēram, pārdošanas pasūtījuma rindu summa bez nodokļiem ir 1 499 ASV dol. Tādēļ lauka **Atzīstamie ieņēmumi** vērtībām arī ir jābūt 1 499 ASV dol.

[![Ieņēmumu cenas sadalījums](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

Tiek izveidots arī plānotais ieņēmumu atzīšanas grafiks. Ieņēmumu grafiks izmanto vērtību **Atzīstamie ieņēmumi** kā atliekamo summu. Krājums S0001 atliek 321,21 ASV dol., nevis 300 ASV dol., un krājums S0008 atliek 160,61 ASV dol., nevis 100 ASV dol. Krājums S0012 netiek rādīts plānotajā grafikā, jo ieņēmumi nav atlikti. Kad notiek grāmatošana, krājums S0012 grāmato 1 017,18 ASV dol. tieši ieņēmumu virsgrāmatas kontā.

[![Plānotais ieņēmumu atzīšanas grafiks](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>Pavadzīmes izveide

Pēc tam pārdošanas pasūtījumam var izveidot pavadzīmi. Iegrāmatojot pavadzīmi, ieņēmumi netiek atzīti. Ja pārdošanas pasūtījums netika apstiprināts, pavadzīmes iegrāmatošana neizraisa ieņēmumu cenas aprēķinu. Tas arī neizraisa plānotā vai galīgā ieņēmumu atzīšanas grafika izveidi. Ja krājumu modeļu grupa ir iestatīta ieņēmumu atlikšanai pavadzīmē, grāmatošana tiks turpināta, izmantojot pašreizējās grāmatošanas metodes virsgrāmatas kontus, nevis jaunos atlikto ieņēmumu kontus, kas tiek izmantoti rēķina grāmatošanai.

## <a name="create-the-invoice"></a>Rēķina izveide

Pēdējā darbība ir pārdošanas pasūtījuma iekļaušana rēķinā. Paskatoties uz rēķina dokumentu, jūs redzēsit ka ieņēmumi par krājumiem S0001 un S0008 tika atlikti (321,21 + 160,61 = 481,82 ASV dol.), un atlikusī summa par krājumu S0012 tika iegrāmatota ieņēmumos (1 017,18). Šīs vērtības pievieno 1 499 ASV dol., kas atbilst pārdošanas pasūtījuma rindu summai.

[![Dokumentu transakcijas](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

Pēc rēķina izveides pogas **Ieņēmumu cenas sadalījums**, **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām** un **Ieņēmumu atzīšanas grafiks** ieņēmumu atzīšanai kļūst pieejamas, bet pogas **Atjaunināt ieņēmumu cenas sadalījumu** un **Plānotais ieņēmumu atzīšanas grafiks** nav pieejamas.

[![Pieejamo ieņēmumu atzīšanas pogu pieejamība](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

Poga **Ieņēmumu cenas sadalījums** joprojām ir pieejama, lai jūs varētu skatīt ieņēmumu cenas aprēķinu. Ja pēc pārdošanas pasūtījuma apstiprināšanas nekas tajā nav mainījies, rēķina grāmatošana nemainīs aprēķināto summu laukā **Atzīstamie ieņēmumi**.

Plānotais ieņēmumu atzīšanas grafiks tiek noņemts un aizstāts ar galīgo ieņēmumu atzīšanas grafiku. Katrai pārdošanas pasūtījuma rindai tiek uzturēta detalizēta informācija par ieņēmumu grafiku, un tā tiek izmantota, lai nodotu atliktos ieņēmumus faktiskajiem ieņēmumiem, kad līgumsaistības ir izpildītas.

[![Galīgais ieņēmumu atzīšanas grafiks](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)
