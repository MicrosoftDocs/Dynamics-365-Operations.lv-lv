---
title: Brīdinājumu kārtulu veidošana
description: Šajā rakstā ir sniegta informācija par brīdinājumiem un skaidrots, kā veidot brīdinājuma noteikumus.
author: RichdiMSFT
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: a420c5b2a036ac63a1a179f93462d152c3941fda
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124230"
---
# <a name="create-alert-rules"></a>Brīdinājumu kārtulu veidošana

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Darba sākšana

Pirms brīdinājuma kārtulas iestatīšanas padomājiet, kad un kādās situācijās vēlaties saņemt brīdinājumus. Kad zināt, par kuru notikumu vēlaties saņemt paziņojumus, atrodiet lapu, kurā ir redzami dati, kas izraisa šo notikumu. Notikums var būt datums, kas iestājas, vai noteiktas izmaiņas, kuras ir veiktas. Tāpēc ir jāatver lapa, kur ir norādīts datums vai kur ir redzams lauks, kur tiek parādītas izmaiņas vai jaunais ieraksts, kurš tiek izveidots. Kad šī informācija ir iegūta, var izveidot brīdinājuma kārtulu.

Izveidojot brīdinājuma kārtulu, tiek definēti kritēriji, kuri ir jāizpilda, lai tiktu aktivizēts brīdinājums. Kritēriji pēc būtības ir atbilstība starp notikuma iestāšanos un noteiktu apstākļu sakritību. Pēc notikuma sistēma sāk pārbaudi saskaņā ar iestatītajiem nosacījumiem.

## <a name="ensure-the-alert-batch-jobs-are-running"></a>Pārliecinieties, ka tiek izpildīti brīdinājuma pakešuzdevumi

Pakešuzdevumi datu maiņai un termiņa brīdinājumiem ir jāpalaiž, lai tiktu apstrādāti brīdinājuma nosacījumi un nosūtīti paziņojumi. Lai palaistu pakešuzdevumus, dodieties uz **Sistēmas administrēšana** > **Periodiski uzdevumi** > **Brīdinājumi** un pievienojiet jaunu pakešuzdevumu opcijai **Izmaiņu brīdinājumi** un/vai **Termiņa brīdinājumi**. Ja vajadzīgs ilgs un bieži palaists pakešuzdevums, atlasiet **Periodiskums** un iestatiet **Nav beigu datuma** ar **Periodiskuma shēmu** **Minūtes** un **Skaitu** **1**.

## <a name="events"></a>Notikumi

Notikums — notikums, kas aktivizē brīdinājuma kārtulu var būt datums, kas iestājas, vai noteiktas izmaiņas, kas ir veiktas. Ar notikumiem saistītie aktivizēšanas elementi tiek definēti dialoglodziņa **Izveidot brīdinājumu kārtulu** kopsavilkuma cilnē **Brīdināt, ja**. Konkrētajā laukā pieejamie notikumi ir atkarīgi no atlasītā aktivizēšanas elementa.

Piemēram, ja tiek iestatīta lauka **Sākuma datums** brīdinājuma kārtula, piemēroti ir izpildes datuma notikumi. Tādējādi šim laukam ir pieejams `is due in` notikuma veids. Tomēr, piemēram, laukam **Izmaksu centrs**, izpildes datuma notikums nav piemērots. Tāpēc `is due in` notikuma veids nav pieejams. Tā vietā ir pieejams notikuma veids `has changed`.

## <a name="event-types"></a>Notikumu tipi

Rasties var trīs notikumu veidi.

- **Izveides veida un dzēšanas veida notikumi** — šie notikumi aktivizē brīdinājumu, ja tiek izveidots vai dzēsts ieraksts.
- **Atjaunināšanas veida notikumi** — šie notikumi aktivizē brīdinājumu, ja tiek mainīti konkrēta lauka dati.
- **Izpildes datuma veida notikumi** — šie notikumi aktivizē brīdinājumu, ja ir iestājies datums.
    
Veiktās izmaiņas var aktivizēt lietotājs. Piemēram, lietotājs maina pirkuma pasūtījuma piegādes datumu. Vai arī izmaiņas var tikt veiktas procesa robežās. Piemēram, izmaiņas lapas laukā **Statuss** notiek, lai norādītu dažādu procesu dzīves ciklu sistēmā.

## <a name="conditions"></a>Nosacījumi

Lai kontrolētu brīdinājuma par notikumiem saņemšanas laiku, var izmantot nosacījumus dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt par**.

Piemēram, var norādīt, ka sistēmai ir jānosūta brīdinājums, ja tiek mainīts pirkšanas pasūtījumu statuss, bet tikai tad, ja statuss atbilst noteiktam nosacījumu kopumam. Piemēram, jūs vēlaties saņemt brīdinājumu, ja tiek iestatīts pirkuma pasūtījuma statuss **Saņemts**. Šīs statusa izmaiņas ir notikums, kas aktivizē brīdinājumu.

Pēc tam jūs vēlaties saņemt brīdinājumu par konkrētiem pirkšanas pasūtījumiem. Piemēram, atlasīt var no vienu no tālāk norādītajām opcijām. Šīs opcijas definē brīdinājuma kārtulas nosacījumus.

- **Pašreiz atlasītais ieraksts** — brīdinājums tiek nosūtīts, ja tiek nomainīts noteikta pirkšanas pasūtījuma statuss **Saņemts**.
- **Visi ieraksti** — brīdinājums tiek nosūtīts, ja tiek mainīts pašreiz atvērtajā lapā redzamā krājuma pirkšanas pasūtījuma statuss. Lai izveidotu noteiktu ierakstu kopuma kārtulas, var izmantot lapā pieejamo papildu filtrēšanu. Piemēram, var izveidot brīdinājumu, kas tiek aktivizēts par debitoru konkrētā debitoru grupā visiem pirkšanas pasūtījumiem.
    
## <a name="expiry-of-rule"></a>Kārtulas derīguma termiņa beigas

Dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt līdz** var norādīt, cik ilgi brīdinājuma kārtulai jādarbojas.

## <a name="alert-contents"></a>Brīdinājuma saturs

Dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt ar** var norādīt tēmas un ziņojuma tekstu, kurš jāizmanto brīdinājuma ziņojumos.

## <a name="user-id"></a>Lietotāja ID

Dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt ar** var norādīt, kuram lietotājam jāsaņem brīdinājuma ziņojumi. Pēc noklusējuma tiek atlasīts jūsu lietotāja ID. Iespēja mainīt lietotāju, kurš saņem brīdinājumu, ir atļauta tikai organizācijas administratoriem.

## <a name="alerts-as-business-events"></a>Brīdinājumi kā biznesa notikumi

Brīdinājumus var sūtīt ārēji, izmantojot biznesa notikumu ietvaru. Veidojot brīdinājumu, iestatiet **Organizācijas mēroga** uz **Nē** un iestatiet **Sūtīt ārēji** uz **Jā**. Pēc tam, kad brīdinājums izraisījis biznesa notikumu, jūs varat izraisīt plūsmu, Power Automate **kas** veidota, izmantojot Kad biznesa notikums parādās finanšu un operāciju savienotājā, **vai skaidri nosūtīt notikumu biznesa notikumu galapunktam, izmantojot biznesa notikumu katalogu**.

## <a name="create-an-alert-rule"></a>Brīdinājuma kārtulas izveide

0. Pārliecinieties, ka tiek izpildīti brīdinājuma pakešuzdevumi (skatīt iepriekš).
1. Atveriet lapu, kurā atrodas kontrolējamie dati.
2. Darbību rūts cilnes **Opcijas** grupā **Kopīgot** atlasiet **Izveidot brīdinājuma kārtulu**.
3. Dialoglodziņa **Izveidot brīdinājuma kārtulu** laukā **Lauks** atlasiet kontrolējamo lauku.
4. Laukā **Notikums** atlasiet notikuma veidu.
5. Kopsavilkuma cilnē **Brīdināt par** atlasiet vēlamo opciju. Ja vēlaties nosūtīt brīdinājumu kā biznesa notikumu, pārliecinieties, ka opcija **Organizācijas mērogā** ir iestatīta uz **Nē**.
6. Ja brīdinājuma kārtulai jākļūst neaktīvai noteiktā datumā, kopsavilkuma cilnē **Brīdināt līdz** atlasiet beigu datumu.
7. Kopsavilkuma cilnē **Brīdināt ar** laukā **Tēma** apstipriniet e-pasta ziņojuma noklusējuma tēmas virsrakstu vai ierakstiet jaunu tēmu. Šis teksts tiek izmantots kā virsraksta tēma e-pasta ziņojumiem, ko saņemat, kad aktivizējas brīdinājums. Ja vēlaties nosūtīt brīdinājumu kā biznesa notikumu, iestatiet **Sūtīt ārēji** uz **Jā**.
8. Laukā **Ziņojums** ievadiet izvēles ziņojumu. Šis teksts tiek izmantots kā ziņojums, ko saņemat, kad aktivizējas brīdinājums.
9. Lai saglabātu iestatījumus un izveidotu brīdinājuma kārtulu, atlasiet **Labi**.

## <a name="limitations-and-workarounds"></a>Ierobežojumi un aprisinājumi

### <a name="workaround-for-creating-alerts-for-the-secondary-data-sources-of-a-form"></a>Aprisinājums, lai izveidotu brīdinājumus sekundārajiem datu avotiem formā
Dažiem sekundārajiem datu avotiem formās nevar izveidot brīdinājumus. Piemēram, veidojot brīdinājumus debitoru vai kreditoru grāmatošanas metodēs, pieejami ir tikai virsraksta (CustLedger vai VendLedger) lauki, nevis dimensiju konti. Šī ierobežojuma aprisinājums ir izmantot **SysTableBrowser**, lai atvērtu šo tabulu kā primāro datu avotu. 
1. Atveriet tabulu formā **SysTableBrowser**.
    ```
        https://<EnvironmentURL>/?cmp=USMF&mi=SysTableBrowser&TableName=<TableName>
    ```
2. Izveidojiet brīdinājumu no formas SysTableBrowser.

### <a name="change-based-alerts-do-not-work-for-batch-status-changes"></a>Izmaiņās balstīti brīdinājumi nedarbojas attiecībā uz pakešu statusa izmaiņām
Izmaiņās balstīti brīdinājumi nedarbojas ar pakešu statusa izmaiņām, jo tie ir izslēgti ar sniegumu saistītu iemeslu dēļ. Tā vietā jums vajadzētu iestatīt iespēju **Pakešu brīdinājumi**. Papildu informāciju skatiet tēmā [Brīdinājumu iestatīšana pakešu uzlabotām veidlapām](../../dev-itpro/sysadmin/alerts.md#set-up-alerts-for-batch-enhanced-forms).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
