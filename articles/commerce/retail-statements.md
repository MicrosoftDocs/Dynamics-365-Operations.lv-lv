---
title: Mazumtirdzniecības pārskati
description: Šajā rakstā ir aprakstīts, kā izraksti tiek izveidoti un grāmatoti.
author: ashishmsft
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0717c1198171f411e3c52233200ecfcc213dc13f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878461"
---
# <a name="retail-statements"></a>Mazumtirdzniecības pārskati

[!include [banner](includes/banner.md)]

Programmā Dynamics 365 Commerce pārskatu grāmatošanas process tiek izmantots, lai uzskaitītu transakcijas, kas tiek veiktas programmā Cloud Point of Sale (POS) vai Modern POS (MPOS). Pārskatu grāmatošanas process izmanto sadales grafiku, lai POS transakciju kopu ievilktu Headquarters (HQ) klientā. Parametrus, kas ir definēti lapās **Commerce parametri** un **Veikali**, izmanto, lai atlasītu atsevišķos pārskatos ievilktās transakcijas.

Tālāk esošajā attēlā parādīts pārskatu grāmatošanas process. Šajā procesā POS reģistrētās transakcijas tiek pārsūtītas uz klientu, izmantojot Commerce plānotāju. Kad klients ir saņēmis transakcijas, varat izveidot, aprēķināt un grāmatot veikala transakciju pārskatu.

[![Pārskatu grāmatošanas process.](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>Pārskatu izveide un grāmatošana

Pārskatu var izveidot manuāli, vai arī varat izmantot pakešveida apstrādi, kas iestatīta periodiskai palaišanai visas dienas garumā. Abos gadījumos pārskatu izveidei un grāmatošanai tiek izmantotas tālāk norādītās darbības.

### <a name="create-the-statement"></a>Pārskata izveide

Šī darbība identificē veikalu, kuram manuāli tiek veidots pārskats. Konfigurējot pakešveida apstrādi, varat automātiski izveidot pārskatus par visiem veikaliem, pamatojoties uz jūsu definēto grafiku.

### <a name="calculate-the-statement"></a>Pārskata aprēķini

Veicot šo darbību, tiek atlasītas transakcijas rindas, pamatojoties uz kritērijiem, kas katram veikalam definēti lapās **Commerce parametri** un **Veikali**. Šajās lapās jūs definējat kritērijus un norādāt, kā tiek veikti transakciju aprēķini. Lai pirms pārskata aprēķinu veikšanas skatītu pārskatā iekļauto transakciju sarakstu, izmantojiet lapu **Transakcijas**.

Pārskata aprēķinos kā aprēķinātā summa tiek izmantotas norēķinu uzskaites no reģistriem. Saskaitīto summu var ievadīt arī manuāli. Pārskatā visām maksāšanas metodēm tiek parādītas transakciju pārdošanas summas un faktiskās saskaitītās summas starpība. Pārskats tiek grāmatots tikai tad, ja šī starpība ir mazāka par veikalam definēto maksimālo grāmatošanas starpību.

> [!NOTE]
> Pārskata aprēķinu procesā tiek izmantota globālo numuru sērija.

Veicot pārskata aprēķinus, aprēķinos tiek ietverti tālāk norādītie uzdevumi.

- Atlasītajam datumu intervālam atzīmējiet transakcijas, kas netika iekļautas iepriekšējā pārskata aprēķinos.
- Aprēķiniet kopsummas, kuru norēķini tika iekļauti atlasītajās transakcijās. Atkarībā no pārskata metodes rezultāti tiek rādīti pārskata rindās.

    - Ja pārskata metode ir **Kopsumma**, katrai atlasītajās transakcijās ietvertajai maksāšanas metodei tiek izveidota rinda.
    - Ja pārskata metode ir **Personāls**, rinda tiek izveidota katrai maksāšanas metodei, kas ietverta atlasītā darbinieka veiktajās transakcijās.
    - Ja pārskata metode ir **POS terminālis**, rinda tiek izveidota katrai maksāšanas metodei, kas ietverta atlasītajā reģistrā veiktajās transakcijās.
    - Ja pārskata metode ir **Maiņa**, rinda tiek izveidota katrai maksāšanas metodei, kas ietverta maiņas laikā veiktajās transakcijās.

Ja lapā **Veikali** ir atzīmēta izvēles rūtiņa **Sadalīt pēc pārskata metodes**, tiek izveidots atsevišķs pārskats atbilstoši laukā **Pārskata metode** atlasītajai vērtībai.

Ja veikala darba laiks sniedzas pāri pusnaktij, varat konfigurēt pārskatu grāmatošanu tā, lai tās pamatā būtu darba dienas beigas, nevis kalendārās dienas beigas.

Lapas **Veikali** kopsavilkuma cilnes FastTab **Izraksts/slēgšana** laukā **Darba dienas beigas** ievadiet laiku, līdz kuram ir jāreģistrē pēdējā transakcija, lai tā tiktu iekļauta darba dienas izrakstā. Atzīmējiet izvēles rūtiņu **Grāmatot kā darba dienu**, lai grāmatotu transakcijas tajā pašā darba dienā. Kad tiek grāmatots pārskats, transakcijas, kas reģistrētas vienas darba dienas laikā, var iekļaut tajā pašā pārdošanas pasūtījumā, pat ja dažas transakcijas ir veiktas pirms pusnakts, bet citas transakcijas — pēc pusnakts.

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>Piemērs: tādas darba dienas pārskata grāmatošana, kas ietver divas kalendārās dienas

Veikals ir atvērts laika posmā no plkst. 8.00 līdz 3.00, un veikala konfigurācijā ir atzīmēta izvēles rūtiņa **Grāmatot kā darba dienu**. 31. maijā tiek reģistrētas veikala transakcijas, kas veiktas laika posmā starp plkst. 8.00 un pusnakti. Tiek reģistrētas arī veikala transakcijas, kas veiktas laika posmā starp plkst. 00.01 un 3.00 1. jūnijā.

Kad, noslēdzot darba dienu, tiek grāmatoti veikala pārskati, tiek ģenerēts pārdošanas pasūtījums, kas ietver visas darba laikā (8.00–3.00) reģistrētās transakcijas, pat ja šīs transakcijas ir veiktas divu dienu laikā: 31. maijā un 1. jūnijā.

Ja šim veikalam ir noņemta atzīme no izvēles rūtiņas **Grāmatot kā darba dienu**, darba dienas beigās grāmatojot veikala pārskatu, tiek ģenerēti atsevišķi pārdošanas pasūtījumi. Viens pārdošanas pasūtījums ietver transakcijas, kas reģistrētas 31. maijā darba laikā no plkst. 8.00 līdz pusnaktij, savukārt otrs pārdošanas pasūtījumu ietver transakcijas, kas reģistrētas 1. jūnijā laika posmā starp plkst. 00.01 un 3.00.

> [!NOTE]
> Lai varētu izveidot pārskatus, pārskata periodā ir jānoslēdz maiņas.

### <a name="post-the-statement"></a>Pārskata grāmatošana

Kad grāmatojat pārskatu, pārskatā tiek izveidoti pārdošanas pasūtījumi un rēķini.

- Pārdošanas transakcijas, kas veiktas skaidrā naudā un bez piegādes, tiek apkopotas vienā pārdošanas pasūtījumā, un to rēķins tiek izrakstīts veikalam piešķirtajam noklusējuma debitoram.
- Transakcijām, kurām programmā ir pievienots debitors, POS sistēmā tiek ģenerēti atsevišķi pārdošanas pasūtījumi un rēķini — pa vienam katram unikālajam debitoram.

Pārskatā iekļautajiem maksājumiem automātiski tiek izveidoti maksājumu žurnāli, un POS veikalā tiek atjaunināti krājumi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]