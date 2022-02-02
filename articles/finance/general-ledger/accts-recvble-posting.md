---
title: Debitoru parādu grāmatošana
description: Šajā tēmā skaidrots, kā grāmatojumi tiek konfigurēti debitoru parādos un sniegti konfigurāciju grāmatošanas piemēri.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustPaymMode, CustCashDiscount, CommissionPosting, MarkupTable\_Cust, CustPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e664c42461e4f2995cac9a747d85d0f2a0fdf85
ms.sourcegitcommit: 96f936267d3f314f06da6ce6f809eba2ec3b205f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/24/2022
ms.locfileid: "8021590"
---
# <a name="accounts-receivable-posting"></a>Debitoru parādu grāmatošana

[!include [banner](../includes/banner.md)]

Primārā grāmatošanas metode debitoru **parādu** modulim ir debitora grāmatošanas metode. Šī grāmatošanas metode nosaka summu kontu, kas tiek izmantots, grāmatojot debitoru bilances Virsgrāmatā. Summu konts ir galvenais konts. To sauc arī par debitoru parādu tirdzniecības kontu.

Plašāku informāciju skatiet šeit: [Debitoru grāmatošanas profili](../accounts-receivable/customer-posting-profiles.md).

Debitora modulī ir pieejamas vairākas grāmatošanas konfigurācijas, kas atrodas blakus debitora grāmatošanas metodei. Šajās sadaļās sniegta plašāka informācija par šīm citām grāmatošanas konfigurācijām.

## <a name="posting-accounts-for-methods-of-payment"></a>Grāmatošanas konti maksāšanas metodēm

Maksāšanas metodes nosaka, kā maksājums tiks grāmatots Virsgrāmatā. Tās arī kontrolē maksājuma izvades darbību. Parasti tiek izveidots viens maksāšanas veids katram maksājuma veidam, ko jūsu organizācija pieņem (piemēram, skaidra nauda, identifikators, kredītkarte, naudas pasūtījums un pārdošanas pārskaitījums).

Lauki Kopsavilkuma cilnes Vispārīgi sadaļā Grāmatošana kontrolē, kā maksājums **tiks** **grāmatots** Virsgrāmatā. Vispirms laukā Konta tips **jāatlasa** vērtība. Atlasītais konta tips kontrolē maksājuma konta **lauka** darbību. Ieteicams atlasīt Banku **konta** tipa **laukā un pēc tam atlasīt bankas** kontu **laukā Maksājuma** konts. Šīs pieejas priekšrocība ir tā, ka sistēma grāmatos maksājumus bankas apakšgrāmatai, kas atbalsta saskaņošanas un citus ar skaidrās naudas procesus saistītus procesus. Ja lietojat kases un bankas vadības moduli, tālāk sniegtajā tabulā ir parādīts **grāmatošanas metodes konfigurācijas** piemērs.

| Grāmatošanas tips | Konta veids | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Banka | Banka | Contoso banka | Ar pamatlīdzekli saistīts bankas konts | Kredītkarte | Nē | Katrai maksājuma metodei ievadiet galveno kontu **laukā Maksājumu** konts. |

Ja neplānosit izmantot skaidras naudas un bankas pārvaldību, jums ir jāatlasa Virsgrāmata laukā Konta veids un pēc tam jāatlasa galvenais **konts** **·** **laukā Maksājumu** konts. Ja neizmantojat kases un bankas pārvaldību, tālāk sniegtajā tabulā ir parādīts grāmatošanas metodes konfigurācijas piemērs.

| Grāmatošanas tips | Konta veids | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Contoso banka | Līdzeklis | Kredītkarte | Nē | Katrai maksājuma metodei ievadiet galveno kontu **laukā Maksājumu** konts. |

## <a name="bridging-accounts"></a>Pagaidu konti

Pagaidu grāmatošana ir divu soļu process, kas tiek izmantots, grāmatojot maksājumus. Tā ir izvēles funkcija, ko, piemēram, var izmantot ar nulles bilances bankas kontiem. Tas var palīdzēt nodrošināt vienmērīgāku un ātrāku bankas darbību saskaņošanas procesu. Pirmajā solī maksājums tiek grāmatots pagaidu kontā (pagaidu konts). Otrajā solī grāmatotais ieraksts tiek atgriezts un grāmatots bankas kontā, kad maksājums nodīra banku. Tabulā parādīts grāmatošanas metodes konfigurācijas piemērs pagaidu grāmatošanai.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Virsgrāmatas žurnāls | 130725 | Nenosti darbinieks skaidrā naudā | Saistības | Debetkarte | Jā | Katrai maksājuma metodei ievadiet galveno kontu **laukā Pagaidu** konts. |

Papildinformāciju skatiet sadaļā [Pagaidu maksājumu iestatīšana un apstrādāšana.](../accounts-receivable/set-up-and-process-bridged-payments.md)

## <a name="posting-accounts-for-customer-cash-discounts"></a>Debitoru termiņatlaižu grāmatošanas konti

Ja jūsu organizācija piedāvā termiņatlaides debitoriem atgriešanai ātram maksājumam, jums jākonfigurē termiņatlaižu kodi un jānorāda, kā atlaides jāgrāmato Virsgrāmatā. Ir pieejamas vairākas opcijas, lai norādītu galveno kontu, kas tiek izmantots, lai grāmatotu debitora termiņatlaidi.

Papildinformāciju skatiet [termiņatlaides.](../cash-bank-management/cash-discounts.md)

## <a name="posting-accounts-for-payment-fees"></a>Komisijas maksājumu kontu grāmatošana

Maksājumu komisijas ļauj jums automātiski pievienot papildu maksu debitora maksājumam, kad tiek piemērots nosacījumu komplekts. Komisijas maksājumi var tikt pieprasīti klientam vai arī tos var grāmatot jūsu bankas kontā kā izdevumus. Daži piemēri:

- Debitori iekasē 3 procentus no maksājuma kopsummas, ja tie maksā, izmantojot kredītkarti.
- Jūsu banka maksā jums $1.00 par katru jūsu apstrādāto pārskaitījumu, un šī papildmaksa tiek izdevumu segšana.

Konfigurējot debitora komisijas maksu, ja lauks Maksa iestatīts uz Debitors, lauks Galvenais konts kļūst pieejams, un sistēma izmanto debitora grāmatošanas metodi **papildmaksas** **·** **grāmatošanai**. Iestatot lauku **Maksa virsgrāmatā, galvenā konta lauks ir jāiestata uz galveno kontu, kur** **maksājuma** **papildmaksa** tiks grāmatota. Parasti šis galvenais konts būs izdevumu konts. Tabulā parādīts grāmatošanas metodes konfigurācijas piemērs komisijas maksājumu grāmatošanai.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Virsgrāmatas žurnāls | 618190 | Izdevumi bankas papildmaksām | Izdevumi | Debetkarte | Nē |  Ja **laukā** Papildmaksa **ir** atlasīta Virsgrāmata, komisijas maksājumam **atlasiet šo kontu** laukā Galvenais konts. |

Plašāku informāciju skatiet šeit: [Debitoru maksājumu papildu maksas noteikšana](../accounts-receivable/tasks/establish-customer-payment-fees.md).

## <a name="posting-accounts-for-charges-codes"></a>Grāmatošanas konti izmaksu kodiem

Ja papildus rindas krājumiem ir jāizseko pārdošanas summas, varat izmantot maksu kodus. Piemēram, jūs variet iekasēt maksu par kravas transportēšanu un apstrādes maksām jūsu klientiem, vai arī jūs variet izdevumi dažām kravām un apstrādes maksām iekšēji. Var norādīt, vai šīs summas tiek grāmatotas izdevumu kontos vai pievienotas krājumu izmaksām.

Var izveidot maksu kodus debitoriem un kreditoriem. Konfigurējot izmaksu kodu, grāmatošana ir jādefinē. Grāmatošana kontrolē gan debeta kontu, gan kredīta kontu. Katram izveidotajiem izmaksu kodiem var atlasīt grāmatošanas tipu, kas tiek lietots. Tālāk sniegtajā tabulā parādīti debitoru parādu izmaksu kodu tipiski piemēri.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Komisijas maksa | 411400 | Ieņēmumi – papildmaksas | Ieņēmumi | Kredītkarte | Nē | **Piemērs nepietiekamiem naudas līdzekļiem:** debitora/kreditora debeta un Kredīta Virsgrāmatas konts |
| Pasūtījums, piegādes izmaksas | 403500 | Ieņēmumi – kravas pārvadāšana | Ieņēmumi | Kredītkarte | Nē | **Piemēram, par transportēšanu, kuru sedz debitors:** debitora/kreditora debeta konts un kredīta Virsgrāmatas konts |
| Atlaide\* | 403200 | Atlaide | Ieņēmumi | Debetkarte | Nē | **Debitora atlaides piemērs: Virsgrāmatas** debeta konts un debitors/kreditors |

\* Atlaides piemērā grāmatošana tiek izmantota tikai tad, ja pirkšanas pasūtījuma galvenei vai rindai tiek pievienots maksas kods. Uzlabotās atlaides funkcionalitāte, kas ir pieejama programmā Dynamics 365 Supply Chain Management Microsoft, nodrošina plašāku atlaižu kontroli un automatizāciju. Papildinformāciju skatiet [sadaļā Debitoru](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md) atlaides.

Iepriekšējā tabulā norādīti trīs tipiski grāmatošanas tipu piemēri, kurus var izmantot izmaksu kodiem. Tas būtu jāizmanto kā vadlīnija un paraugs. Tas nesniedz vispārēju sarakstu ar visām iespējamām kombinācijām vai grāmatošanas tipiem, ko var izmantot.

Papildinformāciju skatiet sadaļā [Maksas koda](../accounts-receivable/create-charges-codes.md) izveide.

## <a name="posting-accounts-for-commissions"></a>Komisijas grāmatošanas konti

Pēc izvēles varat konfigurēt sistēmu, lai aprēķinātu komisijas maksājumus pārdošanas pārstāvjam vai pārdošanas pārstāvju grupai noteiktā pārdošanas pasūtījumā. Ja iespējojat šo funkcionalitāti, jākonfigurē grāmatošanas konts, kas tiek izmantots komisijas jāaprēķina. Šī konfigurācija tiek veikta Komisijas **grāmatošanas** lapā Pārdošanas **un mārketinga** modulī.

Papildinformāciju skatiet [pārdošanas komisijas noteikumu](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md) iestatīšana.
