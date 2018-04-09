---
title: "Brīdinājumu izveide"
description: "Šajā tēmā ir sniegta informācija par brīdinājumiem un izskaidrots, kā izveidot brīdinājuma kārtulu tā, lai varētu saņemt paziņojumu par notikumiem, piemēram, par datumu, kas iestājas, vai noteiktām izmaiņām, kuras ir veiktas."
author: tjvass
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 454368ab5a467002ebf973db97fd98e31885dfe0
ms.openlocfilehash: 5bcd02e08a4ce5b601615b39bf95362cf92d3fec
ms.contentlocale: lv-lv
ms.lasthandoff: 03/23/2018

---

# <a name="create-alerts"></a>Brīdinājumu izveide

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/pre-release.md)] 

## <a name="getting-started"></a>Darba sākšana
Pirms brīdinājuma kārtulas iestatīšanas padomājiet, kad un kādās situācijās vēlaties saņemt brīdinājumus. Kad ir zināms, par kuriem notikumiem vēlaties saņemt paziņojumus, programmā Microsoft Dynamics 365 for Finance and Operations atveriet lapu, kurā tiek parādīti dati, kas izraisa šo notikumu. Notikums var būt datums, kas iestājas, vai noteiktas izmaiņas, kuras ir veiktas. Tāpēc ir jāatver lapa, kur ir norādīts datums vai kur ir redzams lauks, kur tiek parādītas izmaiņas vai jaunais ieraksts, kurš tiek izveidots. Kad šī informācija ir iegūta, var izveidot brīdinājuma kārtulu.

Izveidojot brīdinājuma kārtulu, tiek definēti kritēriji, kuri ir jāizpilda, lai tiktu aktivizēts brīdinājums. Varat domāt par tādiem kritērijiem kā atbilstība starp notikuma iestāšanos un noteiktu apstākļu sakritību. Ja rodas notikums, sistēma sāk pārbaudi saskaņā ar programmā Finance and Operations iestatītajiem nosacījumiem.

## <a name="events"></a>Notikumi
Notikums — notikums, kas aktivizē brīdinājuma kārtulu var būt datums, kas iestājas, vai noteiktas izmaiņas, kas ir veiktas. Ar notikumiem saistītie aktivizēšanas elementi tiek definēti dialoglodziņa **Izveidot brīdinājumu kārtulu** kopsavilkuma cilnē **Brīdināt, ja**. Konkrētajā laukā pieejamie notikumi ir atkarīgi no atlasītā aktivizēšanas elementa.

Piemēram, ja tiek iestatīta lauka **Sākuma datums** brīdinājuma kārtula, piemēroti ir izpildes datuma notikumi. Tāpēc šim laukam ir pieejams notikuma veids **izpildes datums**. Tomēr, piemēram, laukam **Izmaksu centrs**, izpildes datuma notikums nav piemērots. Tāpēc notikuma veids **izpildes datums** nav pieejams. Tā vietā ir pieejams notikuma veids **ir mainījies**.

## <a name="event-types"></a>Notikumu tipi
Rasties var trīs notikumu veidi.

- **Izveides veida un dzēšanas veida notikumi** — šie notikumi aktivizē brīdinājumu, ja tiek izveidots vai dzēsts ieraksts.
- **Atjaunināšanas veida notikumi** — šie notikumi aktivizē brīdinājumu, ja tiek mainīti konkrēta lauka dati.
- **Izpildes datuma veida notikumi** — šie notikumi aktivizē brīdinājumu, ja ir iestājies datums.
    
Veiktās izmaiņas var aktivizēt lietotājs. Piemēram, lietotājs maina pirkuma pasūtījuma piegādes datumu. Vai arī izmaiņas var tikt veiktas procesa robežās. Piemēram, izmaiņas lapas laukā **Statuss** notiek, lai norādītu dažādu procesu dzīves ciklu sistēmā.

## <a name="conditions"></a>Nosacījumi
Lai kontrolētu brīdinājuma par notikumiem saņemšanas laiku, var izmantot nosacījumus dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt par**.

Piemēram, var norādīt, ka sistēmai ir jānosūta brīdinājums, ja tiek mainīts pirkšanas pasūtījumu statuss, bet tikai tad, ja statuss atbilst noteiktam nosacījumu kopumam. Piemēram, jūs vēlaties saņemt brīdinājumu, ja tiek iestatīts pirkuma pasūtījuma statuss **Saņemts**. Šīs statusa izmaiņas ir notikums, kas aktivizē brīdinājumu.

Pēc tam jūs vēlaties saņemt brīdinājumu par konkrētiem pirkšanas pasūtījumiem. Piemēram, atlasīt var no vienu no tālāk norādītajām opcijām. Šīs opcijas definē brīdinājuma kārtulas nosacījumus.

- **Pašreiz atlasītais ieraksts** — brīdinājums tiek nosūtīts, ja tiek nomainīts noteikta pirkšanas pasūtījuma statuss **Saņemts**.
- **Visi ieraksti** — brīdinājums tiek nosūtīts, ja tiek mainīts pašreiz atvērtajā lapā redzamā krājuma pirkšanas pasūtījuma statuss. Lai izveidotu noteiktu ierakstu kopuma kārtulas, var izmantot lapā pieejamo papildu filtrēšanu. Piemēram, var izveidot brīdinājumu, kas tiek aktivizēts par debitoru konkrētā debitoru grupā visiem pirkšanas pasūtījumiem.
    
## <a name="expiry-of-rule"></a>Kārtulas derīguma termiņa beigas
Dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt līdz** var norādīt, cik ilgi brīdinājuma kārtulai jādarbojas.

## <a name="alert-contents"></a>Brīdinājuma saturs
Dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt ar** var norādīt tēmas un ziņojuma tekstu, kurš jāizmanto brīdinājuma ziņojumos.

## <a name="user-id"></a>Lietotāja ID
Dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt ar** var norādīt, kuram lietotājam jāsaņem brīdinājuma ziņojumi. Pēc noklusējuma tiek atlasīts jūsu lietotāja ID. Šī opcija attiecas tikai uz organizācijas administratoriem.

## <a name="create-an-alert-rule"></a>Brīdinājuma kārtulas izveide
1. Atveriet lapu, kurā atrodas kontrolējamie dati.
2. Darbību rūts cilnes **Opcijas** grupā **Kopīgot** atlasiet **Izveidot brīdinājuma kārtulu**.
3. Dialoglodziņa **Izveidot brīdinājuma kārtulu** laukā **Lauks** atlasiet kontrolējamo lauku.
4. Laukā **Notikums** atlasiet notikuma veidu.
5. Kopsavilkuma cilnē **Brīdināt par** atlasiet opciju.
6. Ja brīdinājuma kārtulai jākļūst neaktīvai noteiktā datumā, kopsavilkuma cilnē **Brīdināt līdz** atlasiet beigu datumu.
7. Kopsavilkuma cilnē **Brīdināt ar** laukā **Tēma** apstipriniet e-pasta ziņojuma noklusējuma tēmas virsrakstu vai ierakstiet jaunu tēmu. Šis teksts tiek izmantots kā virsraksta tēma e-pasta ziņojumiem, ko saņemat, kad aktivizējas brīdinājums.
8. Laukā **Ziņojums** ievadiet izvēles ziņojumu. Šis teksts tiek izmantots kā ziņojums, ko saņemat, kad aktivizējas brīdinājums.
9. Lai saglabātu iestatījumus un izveidotu brīdinājuma kārtulu, atlasiet **Labi**.

