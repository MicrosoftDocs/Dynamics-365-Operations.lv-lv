---
title: Ieteicamā grāmatošanas metožu prakse
description: Šajā tēmā aprakstīta grāmatošanas profilu konfigurēšanas ieteicamā prakse.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 211dc42b80089eb1f59a435f09d6e9d9f956736b
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734280"
---
# <a name="recommended-practices-for-posting-profiles"></a>Ieteicamā grāmatošanas metožu prakse

Ir vairākas ieteiktās prakses, kas jāievēro, konfigurējot grāmatošanas metodes visā sistēmā. Šajā tēmā aprakstīti dažādi scenāriji un atbilstošās ieteicamās prakses.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>Iestata karodziņu Atļaut manuālu ievadi

Lapā Galvenie **konti visiem** galvenajiem kontiem, **kas tiek** izmantoti grāmatošanas metodei, ir jāatzīmē izvēles rūtiņa Neatļaujiet manuālu ierakstu. Šis iestatījums neļauj lietotājiem manuāli grāmatot žurnāla ierakstu galvenajā kontā. Tāpēc tas palīdz nodrošināt, ka apakšgrāmata paliek bilances attiecībā pret virsgrāmatu un palīdz atvieglotu saskaņošanas procesu.

Ja konta korekcijas ir nepieciešamas, ko kontrolē sistēma un kas tiek grāmatots automātiski, var izmantot vienu no šīm pieejām:

- Izveidojiet sekundāro galveno kontu, kur var grāmatot korekcijas. Pēc tam izmantojiet Kopsummas kontu vai īpašu rindu no saviem finanšu pārskatiem, lai grupētu un summētu kontus kopā.
- Atsauciet sākotnējos darījumus atbilstošajā apakšgrāmatā, veiciet nepieciešamās korekcijas un pēc tam atkārtoti grāmatot darījumu ar to pašu apakšvirsgrāmatas starpniecību.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Grāmatošanas metožu maiņa pēc darbību pastāv

Ja maināt grāmatošanas metodi pēc transakciju izveidošanas, saskaņošana var neizdoties un jūsu apakšgrāmata un Virsgrāmata var kļūt ārpus bilances. Ieteicams ieteicams nemaināt grāmatošanas **metodi** pēc darbību izveidošanas.

Ja nepieciešamas izmaiņas, izmantojiet šādas vadlīnijas, lai palīdzētu nodrošināt sistēmas integritāti:

- Veiciet izmaiņas perioda slēgšanas laikā.
- Veiciet izmaiņas, kad sistēmā netiek veiktas citas darbības.
- Pārbaudiet Virsgrāmatu un saskaņojiet to ar apakšgrāmatu pirms un pēc izmaiņu veikšanas.
- Ja tiek mainīta grāmatošanas metode, grāmatotās darbības netiek atjauninātas. Rūpīgi apsveriet, vai jūsu maiņai nepieciešami visi pielāgošanas ieraksti.
- Ja maināt krājumu grāmatošanas metodes, ņemiet vērā, kā izmaiņas ietekmēs rīcībā esošo krājumu un Virsgrāmatas bilances. Dažām izmaiņām var būt nepieciešams, lai krājums novietotu 0 (nulle), aizvērtu krājumu un pēc tam pēc izmaiņu veikšanas atnestu krājumu atpakaļ.
- Pirms veicat izmaiņas ražošanā, vienmēr pārbaudiet izmaiņas vidē, kas nav ražošanas vidē.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Datu bāzes reģistrēšanas izmantošana grāmatošanas profilu audita izmaiņām

Apsveriet iespēju iestatīt datu bāzes reģistrāciju katrai grāmatošanas metodei un parametru tabulām, kas kontrolē grāmatošanu. Tad, ja tiek mainīts parametrs vai profils, jums būs pilns audita ieraksts par to, kāda vērtība tika mainīta, kurš to ir mainījis, kad tas tika mainīts un kāda bija iepriekšējā vērtība. Šī informācija var būt kritiska saskaņošanas procesa laikā, un jūsu auditoram var būt nepieciešama atbalsta dokumentācija.

Papildinformāciju skatiet sadaļā Datu [bāzes reģistrēšanas konfigurēšana](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Izmantojiet šo tabulu kā atsauci kopējiem tabulu nosaukumiem, kas ir saistīti ar grāmatošanas metodēm un saistītiem grāmatošanas parametriem.

| Lapas nosaukums | Navigācijas ceļš | Tabulas nosaukums |
|-----------|-----------------|------------|
| Kreditoru parādu parametri | Kreditoru iestatīšanas &gt;&gt; parādi kreditoriem parametri | VendParm (Francija) |
| Kreditoru grāmatošanas metode | Kreditoru iestatīšanas &gt; kreditora &gt; grāmatošanas metode | VendPosting (Kreditorugrāmatošana) |
| Maksas kods | Parādu kreditoriem &gt; iestatījuma &gt; Izmaksu kods vai Debitoru maksu &gt; iestatījuma &gt; izmaksu kods | Markuptable |
| Maksāšanas veids | Kreditoru maksājumu &gt; iestatīšanas &gt; apmaksas metodes | VendPaymMode |
| Termiņatlaides | Kreditoru maksājumu &gt; iestatīšanas termiņatlaides &gt; vai debitoru maksājumu &gt; iestatījumu termiņatlaides &gt; | Skaidras naudas norēķini |
| Komisijas maksājums (kreditors) | Kreditoru maksājumu &gt; iestatīšana Maksājumu &gt; apmaksas | VendPaymFee (francija) |
| Debitoru parādu parametri | Debitoru parādu iestatīšanas &gt;&gt; debitoru moduļa parametri | CustParm (lielākā daļa) |
| Debitoru grāmatošanas metodes | Debitoru parādu iestatīšanas &gt;&gt; debitora grāmatošanas metode | Custposting |
| Maksāšanas veids | Debitoru maksājumu &gt; iestatīšanas &gt; maksājuma metodes | CustPaymMode |
| Komisijas maksa (Debitors) | Debitoru maksājumu &gt; iestatīšanas &gt; maksājumu metodes | CustPaymFee |
| Līdzekļa nomas parametri | Līdzekļu izlaižšanas &gt; iestatīšanas &gt; līdzekļu nolaižamās nolaižamās darbības parametri | AssetLeasePostingAccounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| Banku konti | Skaidras naudas un bankas vadība &gt; Bankas konti &gt; Bankas konti | Tabula BankAccountsTable |
| Bankas darbību tipi | Skaidras naudas un bankas pārvaldības &gt; iestatīšanas &gt; bankas darbību tipi | BankTransType |
| Korekcijas kārtulas | Konsolidācijas iestatījumu &gt;&gt; korekcijas nosacījums | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Izdevumu kategorijas | Avansa norēķinu &gt; iestatīšanas &gt; vispārīgās &gt; izdevumu kategorijas | ProjCategories |
| Pamatlīdzekļu parametri | Pamatlīdzekļu iestatīšanas &gt;&gt; pamatlīdzekļa parametri | Parametri AssetParameters |
| Pamatlīdzekļu grāmatošanas metodes | Pamatlīdzekļu iestatīšanas &gt; pamatlīdzekļa &gt; grāmatošanas metodes | AssetLedgerAccounts<br>Parametri AssetDisposalParameters |
| Valūtas pārvērtēšanas konti | Virsgrāmatas valūtas &gt; valūtas pārvērtēšanas &gt; konti | CurrencyLedgerGainLossAccount |
| Automātisko darījumu konti | Virsgrāmatas grāmatošanas &gt; iestatījumu &gt; konti automātiskām darbībām | LedgerSystemAccounts |
| Starpuzņēmuma uzskaite | Virsgrāmatas grāmatošanas &gt; iestatīšana &gt; Starpuzņēmuma kontiem | Virsgrāmatas starpuzņēmums |
| Darījuma grāmatošanas definīcijas | Virsgrāmatas grāmatošanas &gt; iestatījumu &gt; darbību grāmatošanas definīcijas | Žurnāla žurnālsDefinitionTrans |
| Grāmatošanas definīcijas | Virsgrāmatas grāmatošanas &gt; iestatījumu &gt; grāmatošanas definīcijas | JournalizingDefintion |
| Grāmatošana (Krājumi) | Krājumu vadības iestatījumu &gt; grāmatošanas &gt;&gt; grāmatošana | Krājumupostēšana |
| Izmaksu veida kodi | Kopējās izmaksas izmaksu &gt; iestatīšanas izmaksu &gt; veidu kodi | ItmCostTypeTable |
| Resursi | Ražošanas kontroles iestatīšanas &gt;&gt; resursu &gt; resursi | Wrkctrtable |
| Resursu grupas | Ražošanas kontroles &gt; iestatīšanas &gt; resursu &gt; resursu grupas | WrkCtrResourceGroup; |
| Ražošanas uzdevumu grupas | Ražošanas kontroles &gt; iestatīšanas &gt; ražošanas &gt; uzdevumu grupa | ProdGroup datu grupa |
| Izmaksu kategorijas | Ražošanas kontroles iestatīšanas &gt;&gt; maršrutu &gt; izmaksu kategorijas | ProjCategory |
| Projektu grupas | Projektu vadības un uzskaites iestatījumu &gt; grāmatošanas &gt;&gt; projektu grupas | ProjGroup (grupa) |
| Grāmatošanas iestatījumi Virsgrāmatā (projekti) | Projektu vadības un uzskaites iestatījumu &gt; grāmatošanas &gt; Virsgrāmatas &gt; grāmatošanas iestatījumi | ProjPosting |
| Noklusētais korespondējošais izmaksu konts | Projektu vadības un uzskaites iestatījumu grāmatošanas &gt;&gt; noklusējuma &gt; korespondējošie konti izdevumiem | ProjDefaultOffsetSetup |
| Atlaižu pārvaldības grāmatošanas profili | Atlaižu pārvaldības &gt; atlaižu pārvaldības grāmatošanas iestatījumu &gt; atlaižu pārvaldības grāmatošanas profili | TAMRebatePosting<a2/& |
| Virsgrāmatas grāmatošanas grupa (nodoklis) | Pvn &gt; iestatījumu &gt; PVN Virsgrāmatas &gt; grāmatošanas grupa | Grupa TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>Grupas tiek mainītas pēc darbību pastāv.

Uzmanies, mainot grupas pamatdatos. Ja lietojat grupas, lai definētu grāmatošanas metodes, jebkuras izmaiņas grupā galvenajā ierakstā var negatīvi ietekmēt iespēju saskaņot Virsgrāmatu ar apakšvirsgrāmatu. Piemēram, varat konfigurēt noliktavas grāmatošanas metodi pārdošanas pasūtījuma ieņēmumiem, lai katrai krājumu grupai būtu izmantots cits ieņēmumu konts. Ja maināt krājuma grupu, kas piešķirta krājumam pēc darbību eksistē, ieņēmumi no jaunām darbībām tiks grāmatoti atjauninātajā kontā. Tomēr visi ieņēmumi, kas grāmatoti pirms izmaiņu grāmatošanas, paliek sākotnējā kontā.

## <a name="testing-posting-profiles"></a>Grāmatošanas metožu testēšana

Pirms darbības veikšanas un pēc izmaiņu vai papildinājumu veikšanas grāmatošanas profilos vai saistītajos parametros ir jātestē katrs scenārijs. Ir jāpārbauda vismaz katrs grāmatošanas tips, lai pārbaudītu, vai grāmatošana darbojas pareizi. Tomēr ieteiktā pieeja ir pārbaudīt katru grāmatošanas metodes darbību un kombināciju.

Piemēram, jums ir divas debitora grāmatošanas metodes, no kurām katrai ir trīs ieraksti, kas raksturīgi debitoru grupām. Šādā gadījumā jātestē katrs darbības tips.

**Grāmatošanas metodes:**

- **GEN** – vispārējā grāmatošanas metode, kurā ir viena grupa darbiniekiem, viena debitoriem un viena starpuzņēmumu grāmatošanas metode. Katra grupa norāda uz citu debitoru parādu tirdzniecības kontu.
- **PRIEKŠAPMAKSA** – priekšapmaksas grāmatošanas metode, kurā ir viens ieraksts visām priekšapmaksām, kas norāda uz debitora priekšapmaksas kontiem.

### <a name="testing-scenarios"></a>Testēšanas scenāriji

- Brīva teksta rēķins debitoram darbinieku grupā **,** kas izmanto GEN grāmatošanas **metodi**
- Brīva teksta rēķins debitoram darbinieku grupā **,** kas izmanto pirmsgrāmatošanas **metodi**
- Pārdošanas pasūtījuma rēķins debitoram darbinieku grupā **,** kas izmanto ĢN **grāmatošanas** metodi
- Pārdošanas pasūtījuma rēķins debitoram darbinieku grupā **,** kas izmanto PIRMSgrāmatošanas **metodi**
- Debitoru maksājumu žurnāls debitoram darbinieku grupā **, kas izmanto ĢN grāmatošanas** **metodi**
- Debitoru maksājumu žurnāls debitoram darbinieku grupā **, kas izmanto pirmsgrāmatošanas** **metodi**

Iepriekš minētajiem piemēriem atkārtojiet vienu testēšanas scenāriju katrai debitoru grupai un atkārtojiet katru testēšanas scenāriju grupu katram papildu darbības tipam (piemēram, projekta rēķiniem un pakalpojumu pārvaldībai).

## <a name="reconciling-the-ledger-to-the-subledger"></a>Virsgrāmatas saskaņošana ar apakšgrāmatu

Virsgrāmata ir jāsaskaņo ar apakšgrāmatu visos periodos. Daudzos moduļos ir iekļauti sagatavoti pārskati, ko var izmantot, lai palīdzētu veikt šo saskaņošanu. Tomēr atkarībā no lokālām prasībām, iespējams, būs jāizveido pielāgoti pārskati vai jāpaplašina esošie pārskati, lai atbilstu jūsu atskaišu prasībām.

Ir ieteicams noslēgt un saskaņot katru apakšvirsgrāmatu ar virsgrāmatu pirms ierašanās virsgrāmatā. Iesakām arī veikt visu atvērto bilanču un atvērto darbību kluču pārslēgšanu pirms sākotnējās darbības uz vietas. Kā daļa no šī procesa ir jāveic pilnīga saskaņošana, lai nodrošinātu, ka tiek migrācija par bilancēm un atvērtajām darbībām ar mantojuma sistēmām un ka visas apakšgrāmatas bilances ar Virsgrāmatu pirms jaunu darbību izveides.
