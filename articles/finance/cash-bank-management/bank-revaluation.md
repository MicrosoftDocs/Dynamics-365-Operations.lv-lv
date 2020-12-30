---
title: Bankas ārvalstu valūtas pārvērtēšana
description: Šajā tēmā ir sniegts pārskats par bankas ārvalstu valūtas pārvērtēšanas procesu. Tajā ir ietverta informācija par iestatīšanu, procesa izpildi, procesa aprēķināšanu un pārvērtēšanas darbību anulēšanu.
author: mikefalkner
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: f99a5ed82fd4d74a5d20620dbe19b4f18e332432
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445686"
---
# <a name="bank-foreign-currency-revaluation"></a>Bankas ārvalstu valūtas pārvērtēšana

[!include [banner](../includes/banner.md)]


Šajā tēmā ir sniegts pārskats par bankas ārvalstu valūtas pārvērtēšanas procesu. Tajā ir izskaidrots, kā iestatīt un izpildīt procesu, un sniegta informācija par procesa aprēķināšanu. Tajā arī izskaidrots, kā anulēt pārvērtēšanas transakcijas, ja anulēšana ir nepieciešama.

Kā daļu no perioda beigām grāmatvedības metodes nosaka, ka bankas kontu bilances, kas ir ārvalstu valūtās, ir nepieciešams pārvērtēt, izmantojot dažādus valūtas maiņas kursa tipus (pašreizējo, vēsturisko, vidējo un citus). Bankas ārvalstu valūtas pārvērtēšanas līdzekli var izmantot, lai pārvērtētu vienu vai vairākus bankas kontus. Šis līdzeklis ir arī globāls līdzeklis. Tādēļ vienā lapā varat pārvērtēt visu to juridisko personu bankas, kurām jums ir piekļuve.

> [!NOTE]
> Palaižot pārvērtēšanas procesu, tiek pārvērtēta bilance katrā bankas kontā, kurš ir grāmatots ārvalstu valūtā. Nerealizētās peļņas vai zaudējumu transakcijas, kas tiek izveidotas pārvērtēšanas procesā, ģenerē sistēma. Var izveidot divas transakcijas — vienu uzskaites valūtai un vienu pārskata valūtai, ja pārskata valūta ir vajadzīga. Katrs uzskaites ieraksts tiks grāmatots nerealizētajā peļņā vai zaudējumos, kā arī galvenajā kontā, kam tiek veikta pārvērtēšana.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Sagatavot ārvalstu valūtas pārvērtēšanas palaišanu

Pirms palaižat pārvērtēšanas procesa, ir nepieciešami tālāk aprakstītie iestatījumi.

- Lapā **Virsgrāmata** norādiet maiņas kursa tipu. Ja galvenajā kontā nav definēts maiņas kursa tips, tad ārvalstu valūtas pārvērtēšanas laikā tiek izmantots šis maiņas kursa tips.
- Valūtas pārvērtēšanai lapā **Virsgrāmata** norādiet realizētās peļņas, realizēto zaudējumu, nerealizētās peļņas un nerealizēto zaudējumu kontus. Realizētās peļņas un realizēto zaudējumu konti tiek izmantoti, kad tiek nokārtotas debitoru un kreditoru transakcijas. Nerealizētās peļņas un nerealizēto zaudējumu konti tiek izmantoti atvērto transakciju un virsgrāmatas galveno kontu pārvērtēšanai.
- Lapā **Valūtas pārvērtēšanas konti** atlasiet atšķirīgus valūtas pārvērtēšanas kontus katrai valūtai un uzņēmumam. Ja neviens konts nav definēts, tiek izmantoti konti no lapas **Virsgrāmata**.

## <a name="enable-foreign-currency-revaluation"></a>Ārvalstu valūtas pārvērtēšanas iespējošana

Pirms ārvalstu valūtas pārvērtēšanas procesu izpildes ir jāieslēdz bankas ārvalstu valūtas pārvērtēšanas līdzeklis.

1. Dodieties uz **Kases un bankas vadība \> Iestatīšana \> Kases un bankas vadības parametri**.
2. Cilnes **Vispārīgi** sadaļā **Ārvalstu valūtas pārvērtēšana** atlasiet opcijas **Iespējot bankas pārvērtēšanu** iestatījumu **Jā**, lai ieslēgtu līdzekli pašreizējai juridiskajai personai. 
3. Cilnē **Numuru sērijas** pievienojiet ārvalstu valūtas pārvērtēšanas numuru sēriju.
4. Atsvaidziniet pārlūku, lai skatītu **Ārvalstu valūtas pārvērtēšana** apgabala lapas sadaļā **Periodiskie uzdevumi**.

Šis līdzeklis ir jāieslēdz katrai juridiskajai personai, kas izmantos ārvalstu valūtas pārvērtēšanu. Ja jums ir piešķirta Sistēmas administratora vai Līdzekļu pārziņa loma, varat izslēgt šo darbību, iespējojot līdzekli **Bankas pārvērtēšanas iespējošana bez parametra** darbvietā **Līdzekļu pārvaldība**.

> [!NOTE]
> Ja juridiskā persona izmanto krievu, poļu vai ungāru valsts/reģiona kodu, varat uzreiz izmantot bankas ārvalstu valūtas pārvērtēšanu. Nav iespējams izmantot ārvalstu valūtas pārvērtēšanu, kas tiek izmantota citām valstīm vai reģioniem.

## <a name="process-foreign-currency-revaluation"></a>Apstrādāt ārvalstu valūtas pārvērtēšanu

Kad iestatīšana ir pabeigta, izmantojiet kases un bankas pārvaldības lapu **Ārvalstu valūtas pārvērtēšana**, lai pārvērtētu viena vai vairāku bankas kontu bilances visām juridiskajām personām. Varat palaist procesu reāllaikā vai ieplānot tā palaišanu, izmantojot pakešuzdevumu.

Lapā **Ārvalstu valūtas pārvērtēšana** ir redzama katra pārvērtēšanas procesa vēsture. Tajā ir parādīts, kad process tika palaists un kādi kritēriji tika noteikti, kā arī nodrošināta saite uz dokumentu, kas tika izveidots pārvērtēšanai. Tajā arī norādīts, vai iepriekšējā pārvērtēšana tika anulēta. Lai palaistu pārvērtēšanas procesu, darbību rūtī atlasiet **Ārvalstu valūtas pārvērtēšana**, lai atvērtu dialoglodziņu **Banka — ārvalstu valūtas pārvērtēšana**.

Laukā **Pārvērtēšanas datums** ir noteikts pārvērtējamās ārvalstu valūtas bilances aprēķina robeždatumu. Tiek pārvērtēta visu līdz šim datumam veikto bankas transakciju summa.

Laukā **Maiņas kursa datums** ir noteikts maiņas kursa datums, kas tiks lietots, lai pārvērtētu valūtas bilances. Piemēram, varat pārvērtēt bilances, sākot no 31. janvāra, bet izmantot maiņas kursu, kas definēts 1. februārī.

Pārvērtēšanas procesu var izpildīt vienai vai vairākām juridiskajām personām. Uzmeklēšanas sarakstā ir redzamas tikai tās juridiskās personas, kurām varat piekļūt. Atlasiet juridiskās personas, kurām vēlaties atlasīt bankas kontu, kas ir piemēroti ārvalstu valūtas pārvērtēšanai. Visi šo juridisko personu bankas konti tiks rādīti režģī.

Atlasiet opcijai **Priekšskatīt pirms grāmatošanas** iestatījumu **Jā**, ja vēlaties priekšskatīt pārvērtēšanas rezultātus pirms grāmatošanas. Ārvalstu valūtas pārvērtēšanai ir priekšskatījums, ko var grāmatot. Pārvērtēšanas process nav jāveic atkārtoti. Varat eksportēt priekšskatījuma rezultātus uz programmu Microsoft Excel, lai saglabātu summu aprēķināšanas vēsturi. Ja vēlaties priekšskatīt pārvērtēšanas rezultātus, nevar izmantot pakešapstrādi.

Atlasiet **Labi**, lai veiktu ārvalstu valūtas pārvērtēšanas procesu. Lai izsekotu katras palaišanas vēsturi, tiek izveidots ieraksts. Katrai juridiskajai personai un grāmatošanas līmenim tiek izveidots atsevišķs ieraksts.

## <a name="calculate-unrealized-gainloss"></a>Aprēķināt nerealizēto peļņu/zaudējumus

Kases un bankas pārvaldības sadaļā bankas valūta tiek uzskatīta par pamatvalūtu un netiek pārvērtēta. Bankas konta bilance uzskaites valūtā tiek pārvērtēta, izmantojot maiņas kursus starp bankas valūtu un uzskaites valūtu **maiņas kursa datumā**. Bankas konta bilance pārskata valūtā tiek arī pārvērtēta, izmantojot maiņas kursus starp bankas valūtu un pārskata valūtu **maiņas kursa datumā**.

Atšķirībai starp bankas konta bilanci un jauno bilanci, kas aprēķināta uzskaites valūtai, tiek izveidota transakcija. Atšķirībai starp bankas konta bilanci un jauno bilanci, kas aprēķināta pārskata valūtai, tiek izveidota cita transakcija. Šo transakciju ieraksti tiek atzīmēti kā saskaņoti. 

Neviens ieraksts netiek izveidots uzskaites valūtai, ja bankas valūta atbilst uzskaites valūtai. Tāpat neviens ieraksts netiek izveidots pārskata valūtai, ja bankas valūta atbilst pārskata valūtai.

Ārvalstu valūtas pārvērtēšanas transakcija ir arī sadalīta starp dimensijām, kas atrodamas bankas transakcijās. Sadalījums ir balstīts uz katras dimensijas bilanci. Piemēram, kopējā bankas bilance ir 10 000, bet biznesa vienības 001 bilance ir 4000, savukārt biznesa vienības 002 bilance ir 6000. Šajā gadījumā 40 procenti no pārvērtējamās summas tiek grāmatota biznesa vienības 001 pārvērtēšanas kontā, un 60 procenti tiek grāmatoti biznesa vienības 002 pārvērtēšanas kontā. Ja konta struktūra neietver biznesa vienību, pilnā summa tiek grāmatota pārvērtēšanas kontā.

## <a name="reverse-foreign-currency-revaluation"></a>Atgriezt ārvalstu valūtas pārvērtēšanu

Ja ir nepieciešams anulēt pārvērtēšanas transakciju, atlasiet pogu **Anulēt transakciju** lapas **Ārvalstu valūtas pārvērtēšana** darbību rūtī. Tiek izveidots jauns ārvalstu valūtas pārvērtēšanas vēsturiskais ieraksts, lai uzturētu vēsturiskos auditācijas pierakstus par to, kad pārvērtēšana notika vai tika anulēta.

Lai anulētu vairākas pārvērtēšanas, vispirms jāanulē jaunākā pārvērtēšana. Pēc tam turpiniet anulēt vecākas pārvērtēšanas datumu secībā. Pēc tam varat apstrādāt jaunas pārvērtēšanas anulētajiem periodiem.
