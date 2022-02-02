---
title: Parādu kreditoriem grāmatojumi
description: Šajā tēmā skaidrots, kā grāmatojumi tiek konfigurēti sadaļā Parādi kreditoriem, un sniedz konfigurāciju grāmatošanas piemērus.
author: rachel-profitt
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting, VendPaymMode, VendCashDiscount, MarkupTable\_Vend, VendPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb3ebad31c9f41e405b9fc31a0f71df05fa1cc60
ms.sourcegitcommit: 10b85a09e8a550155a69aa2a8877a7c88b887242
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/20/2022
ms.locfileid: "8014486"
---
# <a name="accounts-payable-posting"></a>Parādu kreditoriem grāmatošana

[!include [banner](../includes/banner.md)]

Primārā grāmatošanas metode kreditoru **modulim** ir kreditora grāmatošanas metode. Šī grāmatošanas metode nosaka summu kontu, kas tiek izmantots, kad kreditoru bilances tiek grāmatotas Virsgrāmatā. Summu konts ir galvenais konts. To sauc arī par parādu kreditoriem tirdzniecības kontu.

Plašāku informāciju skatiet Kreditora [grāmatošanas profilos](../accounts-payable/vendor-posting-profiles.md).

Kreditoriem ir pieejamas vairākas grāmatošanas konfigurācijas papildus kreditora grāmatošanas metodei. Šajās sadaļās sniegta plašāka informācija par šīm citām grāmatošanas konfigurācijām.

## <a name="methods-of-payment-posting-accounts"></a>Maksājumu grāmatošanas kontu metodes

Maksāšanas metodes nosaka, kā maksājums tiks grāmatots Virsgrāmatā. Tās arī kontrolē maksājuma izvades darbību. Parasti tiek izveidota viena maksājuma metode katram maksājumu veidam, ko veic jūsu organizācija (piemēram, skaidra nauda, identifikators, kredītkarte, naudas pasūtījums un uzņēmuma).

Lauki cilnes Grāmatošana sadaļā Vispārīgi, lapā Maksāšanas veidi (Parādi kreditoriem > Maksājumu iestatījumi > Maksājumu veidi) kontrolē, kā maksājums tiks grāmatots **virsgrāmatā**. **·** **·** **·** Vispirms laukā Konta tips **jāatlasa** vērtība. Atlasītais konta tips kontrolē maksājuma konta **lauka** darbību. Ieteicams atlasīt Banku **konta** tipa **laukā un pēc tam atlasīt bankas** kontu **laukā Maksājuma** konts. Šīs pieejas priekšrocība ir tā, ka sistēma grāmatos maksājumu bankas apakšgrāmatai, kas atbalsta saskaņošanas un citus ar skaidrās naudas procesus saistītus procesus. Ja lietojat kases un bankas vadības moduli, tālāk sniegtajā tabulā ir parādīts **grāmatošanas metodes konfigurācijas** piemērs.

| Grāmatošanas tips | Konta veids | Maksājuma konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Banka | Banka | Amerikas Banka | Ar pamatlīdzekli saistīts bankas konts | Debetkarte | Nē | Katrai maksājuma metodei ievadiet galveno kontu **laukā Maksājumu** konts. |

Ja neplānosit izmantot skaidras naudas un banku pārvaldību, jums ir jāatlasa Virsgrāmata laukā Konta veids un pēc tam jāatlasa galvenais **konts** **·** **laukā Maksājumu** konts. Ja kases un bankas pārvaldību nelieto, tālāk sniegtajā tabulā **ir** parādīts grāmatošanas metodes konfigurācijas piemērs.

| Grāmatošanas tips | Konta veids |Maksājuma konta piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Amerikas Banka | Līdzeklis | Debetkarte | Nē | Katrai maksājuma metodei ievadiet galveno kontu **laukā Maksājumu** konts. |

## <a name="bridging-accounts"></a>Pagaidu konti

Pagaidu grāmatošana ir divu soļu process, kas tiek izmantots, grāmatojot maksājumus. Tā ir izvēles funkcija, ko, piemēram, var izmantot ar nulles bilances bankas kontiem. Tas var palīdzēt nodrošināt vienmērīgāku un ātrāku bankas darbību saskaņošanas procesu. Pirmajā solī maksājums tiek grāmatots pagaidu kontā (pagaidu konts). Otrajā solī grāmatotais ieraksts tiek atgriezts un grāmatots bankas kontā, kad maksājums nodīra banku. Tabulā parādīts grāmatošanas metodes konfigurācijas piemērs pagaidu grāmatošanai.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Virsgrāmatas žurnāls | 130725 | Nenosti darbinieks skaidrā naudā | Saistības | Debetkarte | Jā | Katrai maksājuma metodei ievadiet galveno kontu **laukā Pagaidu** konts. |

Papildinformāciju skatiet sadaļā [Pagaidu maksājumu iestatīšana un apstrādāšana.](../accounts-receivable/set-up-and-process-bridged-payments.md)

## <a name="customer-cash-discounts-posting-accounts"></a>Debitoru termiņatlaižu grāmatošanas konti

Ja uzņēmums saņem termiņatlaides no kreditoriem atgriešanas pasūtījumā, jums jākonfigurē termiņatlaižu kodi un jānorāda, kā atlaides jāgrāmato Virsgrāmatā. Ir pieejamas vairākas opcijas, lai norādītu galveno kontu, kas tiek izmantots, lai grāmatotu debitora termiņatlaidi.

Papildinformāciju skatiet [termiņatlaides.](../cash-bank-management/cash-discounts.md)

## <a name="payment-fee-posting-accounts"></a>Komisijas maksu grāmatošanas konti

Maksājumu komisijas ļauj jums automātiski pievienot papildu maksu kreditora maksājumam, kad tiek piemērots nosacījumu komplekts. Maksājuma papildmaksas var maksāt kreditoram vai arī tās var grāmatot jūsu bankas kontā kā izdevumus. Daži piemēri:

- Kreditors maksā jums 3 procentus no maksājuma kopsummas, ja maksājat, izmantojot kredītkarti.
- Jūsu banka izraksta maksu $1.00 par katru jūsu apstrādāto pārskaitījumu, un maksa par kursiem tiek ieturēta.

Konfigurējot kreditora maksājuma papildmaksu, iestatot lauku Maksa kreditoram, lauks Galvenais konts kļūst pieejams, un sistēma izmanto kreditora grāmatošanas metodi **papildmaksas** **·** **grāmatošanai**. Iestatot lauku **Maksa virsgrāmatā, galvenā konta lauks ir jāiestata uz galveno kontu, kur** **maksājuma** **papildmaksa** tiks grāmatota. Parasti šis galvenais konts būs izdevumu konts. Tabulā parādīts grāmatošanas metodes konfigurācijas piemērs komisijas maksājumu grāmatošanai.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| Virsgrāmatas žurnāls | 618190 | Izdevumi bankas papildmaksām | Izdevumi | Debetkarte | Nē | Ja **laukā** Papildmaksa **ir** atlasīta Virsgrāmata, atlasiet **šo kontu** laukā Galvenais **konts, kas atrodas komisijas maksājumu** lapā. |

Plašāku informāciju skatiet šeit: [Kreditora maksājumu papildmaksu definēšana](../accounts-payable/tasks/define-vendor-payment-fees.md).

## <a name="charges-code-posting-accounts"></a>Izmaksu koda grāmatošanas konti

Ja papildus rindas krājumiem jāizseko pirkšanas summas, varat izmantot maksu kodus. Piemēram, jūsu piegādātājs var iekasēt maksu par kravu un apstrādes maksām jums, vai arī tas var izdevumties dažas kravas pārvadāšanas un apstrādes maksas iekšēji. Var norādīt, vai šīs summas tiek grāmatotas izdevumu kontos vai pievienotas krājumu izmaksām.

Var izveidot maksu kodus debitoriem un kreditoriem. Konfigurējot izmaksu kodu, grāmatošana ir jādefinē. Grāmatošana kontrolē gan debeta kontu, gan kredīta kontu. Veidojot maksu kodus, varat atlasīt grāmatošanas tipu, kas tiek izmantots katram maksas kodam. Šajā tabulā parādīti tipisko maksājumu kodu piemēri kreditoru parādiem maksu **kodu** lapā.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Pirkuma izmaksas segšana | Atstājiet šo lauku tukšu. | Nav attiecināms | Krājums | Debetkarte | Nē | **Krājuma pirkuma maksas piemērs:** </p><ul><li>**Debeta** tipa lauks = **krājums**</li><li>  **Kredīta tipa** lauks = **Debitors/Kreditors**.</li><li> Krājuma grāmatošana izmanto galveno kontu no krājumu grāmatošanas metodes. |
| Pasūtījums, piegādes izmaksas | 600120 | Kravas pārvadāšana | Ieņēmumi | Debetkarte | Nē | **Piemērs par kravas transportēšanu, kas tiek maksāta kreditoram:** </p><ul><li>**Debeta** tipa lauks = Virsgrāmatas **konts**</li><li> **Kredīta tipa** lauks = **Debitors/Kreditors** |
| Atlaide\* | 503160 | Kreditora atlaide (Plkst. COGS)| Izdevumi | Kredītkarte | Nē | **Kreditora atlaides piemērs:**</p><ul><li>**Debeta** tipa lauks = **debitors/kreditors**</li><li>**Kredīta tipa** lauks = **Virsgrāmatas konts** |

\* Atlaides piemērā grāmatošana tiek izmantota tikai tad, ja pirkšanas pasūtījuma galvenei vai rindai tiek pievienots maksas kods. Uzlabotās atlaides funkcionalitāte, kas ir pieejama programmā Dynamics 365 Supply Chain Management Microsoft, nodrošina plašāku atlaižu kontroli un automatizāciju. Papildinformāciju skatiet [sadaļā Kreditora](../../supply-chain//procurement/vendor-rebates.md) atlaides.

Iepriekšējā tabulā norādīti trīs tipiski grāmatošanas tipu piemēri, kurus var izmantot izmaksu kodiem. Tas būtu jāizmanto kā vadlīnija un paraugu atlase. Tas nesniedz vispārēju sarakstu ar visām iespējamām kombinācijām vai grāmatošanas tipiem, ko var izmantot.

Papildinformāciju skatiet sadaļā [Maksas koda](../accounts-receivable/create-charges-codes.md) izveide.
