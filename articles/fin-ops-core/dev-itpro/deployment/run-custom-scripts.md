---
title: Palaidiet pielāgotus X++ skriptus bez dīkstāves
description: Šajā tēmā ir aprakstīts, kā augšupielādēt un palaist izvietojamas pakotnes, kurās ir pielāgoti X++ skripti, neapturot sistēmu.
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: fcd0a472fa5116ca0b3a59561b6eeb72181a9113
ms.sourcegitcommit: 44e6875e974a3a1b3e1d7a24c1a3cff3d3697cdc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2022
ms.locfileid: "8088348"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Palaidiet pielāgotus X++ skriptus bez dīkstāves

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Šī funkcija ļauj augšupielādēt un palaist izvietojamas pakotnes, kurās ir pielāgoti X++ skripti, bez nepieciešamības tos veikt Microsoft Dynamics Lifecycle Services (LCS) vai apturiet savu sistēmu. Tāpēc jūs varat labot nelielas datu neatbilstības, neradot traucējošu dīkstāvi.

Ieguvums no X++ skripta izmantošanas, lai labotu nelielas datu neatbilstības, ir tāds, ka sistēma automātiski pielāgos visas saistītās tabulas pēc vajadzības, palaižot skriptu. Šī pieeja palīdz nodrošināt korekcijas integritāti un palīdz samazināt risku, ka var rasties jaunas neatbilstības.

> [!IMPORTANT]
> Šī funkcija ir paredzēta tikai nelielu datu neatbilstību labošanai. To nedrīkst izmantot šādiem vai citiem mērķiem:
>
> - Datu vākšana
> - Shēmas izmaiņas
> - Datu migrācija vai citi ilgstoši procesi
> - To datu labošana, kurus var labot, izmantojot citus līdzekļus, piemēram, parastos biznesa procesus, datu konsekvences rīkus vai citus pašapkalpošanās rīkus.
>
> Šī funkcija ļauj pilnvarotajiem lietotājiem tieši mainīt entītijas un to ierakstus, neizmantojot ar šīm entītijām saistīto biznesa loģiku. Šīs izmaiņas var izraisīt datu integritātes problēmas. Tādēļ jūsu organizācija var pieprasīt, lai pirms un/vai pēc skripta palaišanas saņemtu apstiprinājumu un parakstu no iekšējiem un ārējiem auditoriem (vai citām līdzvērtīgām ieinteresētajām personām). Atbilstības apsvērumu dēļ izmaiņas, kas ietekmē dažus raksturlielumus, var būt arī jāatklāj ārējos pārskatos (piemēram, finanšu pārskatos) vai jāziņo valdības iestādēm. Jūsu organizācija ir pilnībā atbildīga par visām izmaiņām, kas veiktas tās datos, izmantojot šo līdzekli, par jebkādu šo izmaiņu apstiprināšanu un parakstīšanu vai izpaušanu, kā arī par atbilstību piemērojamiem tiesību aktiem. Jūs uzņematies visus riskus, kas saistīti ar šīs funkcijas izmantošanu.

Visas izvietojamās pakotnes, kas tiek augšupielādētas sistēmā, iziet obligātu darbplūsmu. Drošības nolūkos un, lai palīdzētu nodrošināt pienākumu nošķiršanu, lietotājs, kurš augšupielādē izvietojamo pakotni, nedrīkst to apstiprināt nākamajām darbplūsmas darbībām. Tas ir jāapstiprina citam lietotājam. Tomēr pēc pakotnes apstiprināšanas lietotājs, kurš to augšupielādējis, varēs veikt atlikušās darbības.

Sistēma pieprasa, lai visas izvietojamās pakotnes tiktu pārbaudītas. Lai skriptu varētu palaist ar ražošanas datiem, lietotājam ir jāapstiprina, vai izvade ir pareiza, atlasot **Pieņemiet pārbaudes žurnālu**. Ja izvade nav pareiza, lietotājam ir jāatzīmē pakotne kā neizdevusies, atlasot **Pamest**. Šajā gadījumā skriptu nevarēs palaist ražošanas datiem.

Katra augšupielādētā pakotne tiek saglabāta sistēmā un tiek veikta noteiktai notikumu darbplūsmai. Katram notikumam sistēma saglabā žurnālu, kurā ir ietverts laikspiedols un tās personas identitāte, kura veica notikumu. Tādā veidā sistēma nodrošina audita izsekojamību.

Kā parādīts nākamajā attēlā, sistēma sniedz detalizētu informāciju par to, kā katra izvietojamā pakotne tika darbināta programmā X++ un kurām entītijām tika pieskarties.

![Skripta informācijas lapa.](media/script-details.png "Detalizēta lapa Par skriptu")

## <a name="assign-duties-to-users-to-control-access"></a>Piešķiriet lietotājiem pienākumus kontrolēt piekļuvi

Šī funkcija nodrošina šādus pienākumus. Administratori var izmantot šos pienākumus, lai palīdzētu kontrolēt piekļuvi funkcijai.

- **Uzturiet pielāgotus skriptus** - Šis pienākums nodrošina iespēju augšupielādēt, pārbaudīt, pārbaudīt un palaist pielāgotus X++ skriptus vidēs (lietotāja pieņemšanas pārbaude\[ UAT\] un ražošana).
- **Apstipriniet pielāgotos skriptus** – Šis pienākums nodrošina iespēju apstiprināt augšupielādētu pielāgotu X++ skriptu. Apstiprināšana ir obligāta darbība, pirms jebkuru skriptu var pārbaudīt, pārbaudīt un palaist.

Lai palīdzētu samazināt ļaunprātīgas darbības risku, katrs skripts ir skaidri jāapstiprina lietotājam, kas nav lietotājs, kurš to augšupielādēja. Lai varētu izmantot šo līdzekli savā organizācijā, administratoram ir jāpiešķir iepriekšējie pienākumi vismaz diviem atbilstošiem un ļoti uzticamiem lietotājiem. Lai gan vienam lietotājam var būt abi pienākumi, šis lietotājs joprojām nevarēs apstiprināt savus skriptus.

## <a name="create-a-deployable-package"></a>Izvietojamas pakotnes izveide

Funkcijai ir nepieciešama parasta izvietojama pakotne, kurā var izveidot Visual Studio. Norādījumus sk [Izveidojiet izvietojamas modeļu pakotnes](../deployment/create-apply-deployable-package.md).

Izvietojamajā pakotnē ir jāietver tieši viena izpildāma X++ klase. Citiem vārdiem sakot, tai ir jābūt vienai klasei, kas ietver metodi, kurai ir šāds paraksts.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Galvenās metodes nosaukumam jābūt ar mazajiem burtiem.

## <a name="code-example"></a>Koda piemērs

Šis koda piemērs parāda, kā var strukturēt izvietojamu pakotni.

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>Paraugprakses

Šajā sarakstā ir aprakstīti daži paraugprakses piemēri veiksmīgai skripta rakstīšanai, ieviešanai un palaišanai. Saraksts nav pilnīgs, un tas ir jāuzskata tikai par norādījumiem.

- **Darīt** rakstiet veiksmes ziņojumu skripta beigās. Tādā veidā jūs varēsiet redzēt, ka skripts darbojās bez izņēmumiem.
- **Darīt** pievienojiet skaidru darījumu jomas apstrādi.
- **Darīt** izmantot esošo biznesa loģiku, piemēram`update()` metodes, bet **ne** apiet biznesa loģiku, izmantojot`doUpdate()`,`doInsert()`, un`doDelete()` metodes. Šī pieeja palīdzēs nodrošināt, ka atkarīgie dati tiek pareizi apstrādāti. Tas arī ievērojami samazinās turpmāku datu neatbilstību risku.
- **Darīt** aizstāvēt uzņēmuma kontekstu. Šī pieeja atklās bieži sastopamās kļūdas skripta izpildes laikā. Piemēram, tas atklās, vai skripts tiek palaists nepareizā uzņēmumā.
- **Darīt** apstipriniet, ka ietekmēto ierakstu skaits atbilst jūsu cerībām. Šī pieeja atklās, vai dati negaidīti mainījās sistēmā skripta sagatavošanas laikā.
- **Darīt** izmantojiet unikālus klases nosaukumus katram skriptam (piemēram, iekļaujot nosaukumā atsauci uz darba vienumu). Šī pieeja novērsīs nosaukumu sadursmes problēmas, augšupielādējot skriptu. Ja ir nepieciešama jauna skripta iterācija, noteikti piešķiriet tam jaunu nosaukumu.
- **Darīt** vispirms pārbaudiet katru skriptu ar ražošanu nesaistītā vidē. Pārbaudiet paredzēto triecienu un nejaušas blakusparādības saistītajos datos. Nodrošiniet, lai visi biznesa procesi, kas varētu tikt ietekmēti, pēc tam tiktu veiksmīgi un pilnībā pabeigti.

## <a name="upload-and-run-a-deployable-package"></a>Augšupielādējiet un palaidiet izvietojamo pakotni

Lai augšupielādētu un palaistu skriptu, izmantojiet tālāk norādīto procedūru.

1. Programmā Finance and Operations dodieties uz **Sistēmas administrēšana \> Periodiski uzdevumi \> Datu bāze \> Pielāgoti skripti**.
1. Atlasiet **Augšupielādēt**.
1. Atlasiet izvietojamo pakotni, kuru izveidojāt, kā aprakstīts iepriekš šajā tēmā. Jums tiks piedāvāts norādīt skripta mērķi.
1. Tagad skripts ir jāapstiprina citam lietotājam, nevis lietotājam, kurš to augšupielādēja. Apstiprinātājam jāveic šādas darbības:

    1. Iet uz **Sistēmas administrēšana \> Periodiski \> Datu bāze \> Pielāgoti skripti**.
    1. Atlasiet apstiprināmo skriptu un pēc tam atlasiet **Detalizēti**.
    1. Darbību rūts **cilnes Apstrādāt darbplūsma** grupā Sākt **atlasiet** Apstiprināt **vai** Noraidīt **·**. Ja atlasāt **Apstiprināt**, skripts tiek atzīmēts kā apstiprināts un tiek atbloķēts testēšanai. Ja atlasāt **Noraidīt**, skripts ir bloķēts. Abos gadījumos notikums tiek reģistrēts, un skripta kopija tiek saglabāta sistēmā.

1. Skripts ir jāpārbauda, lai pārliecinātos, ka tas dara to, ko tas ir paredzēts darīt. Testētājs var būt tāds pats kā augšupielādētājs vai apstiprinātājs, vai arī tas var būt trešais lietotājs, kuram ir nepieciešamās atļaujas. Testētājam jāveic šādas darbības:

    1. Iet uz **Sistēmas administrēšana \> Periodiski \> Datu bāze \> Pielāgoti skripti**.
    1. Atlasiet pārbaudāmo skriptu un pēc tam atlasiet **Detalizēti**.
    1. Darbību rūts **cilnes** Apstrādāt darbplūsma **grupā Pārbaude** atlasiet **Izpildīt testu**. Skripts tiek palaists pagaidu transakcijā, kuru sistēma automātiski pārtrauks, kamēr tā apkopos dažādus žurnālus un SQL priekšrakstus.
    1. Kad skripts ir beidzis darboties, pārskatiet žurnālus un pārbaudiet, vai rezultāti atbilst jūsu vēlmēm. Izpildiet kādu no šīm darbībām:

        - Ja esat apmierināts ar testa rezultātu, darbību rūts cilnes Apstrādāt darbplūsma grupā Tests atlasiet **Akceptēt testa žurnālu** **, lai atļautu skripta izpildi.** **·** Notikumu žurnāls atspoguļos faktu, ka skripts tika pārbaudīts, un tas norādīs, kas to pārbaudīja un kad.
        - Ja neesat apmierināts ar testa rezultātu, darbību rūts cilnes Procesa darbplūsma grupā Beigt atlasiet **Atteikties** **, lai novērstu skripta izpildi.** **·** Sistēma saglabās skripta kopiju kopā ar tā vēstures žurnālu.

1. Kad esat pārliecināts, vai skripts atbilst jūsu vēlmēm, darbību rūts cilnes Apstrādāt darbplūsma grupā Palaist atlasiet **Palaist** **·**, lai to palaistu.**·** Šī komanda dara to pašu, ko iepriekšējā testa braucienā, bet transakcija tiks veikta beigās.
1. Kad skripts ir beidzis darboties, pārbaudiet rezultātu un apstipriniet, ka skripts darbojās, kā paredzēts. Izpildiet kādu no šīm darbībām:

    - Ja esat apmierināts ar rezultātu, darbību rūts cilnes Apstrādāt darbplūsmu grupā Beigt atlasiet **Nolūks, kas** atrisināts **·**.**·** Notikumu žurnāls atspoguļos faktu, ka skripts darbojās veiksmīgi, un tas norādīs, kurš un kad verificēja skriptu. Skripts ir saglabāts, bet tagad tas ir bloķēts, un to nevar palaist vēlreiz.
    - Ja neesat apmierināts ar rezultātu, darbību rūts cilnes Apstrādāt darbplūsma grupā Beigt atlasiet **Nolūks, kas nav atrisināts** **·**.**·** Notikumu žurnāls atspoguļos faktu, ka skripts nav izpildījis tā paredzēto mērķi, un tas norādīs, kurš un kad vadīja skriptu. Skripts ir saglabāts, bet tagad tas ir bloķēts, un to nevar palaist vēlreiz. Tomēr sistēma automātiski neatsaka skripta darbību. Iespējams, būs jāraksta, jāimportē un jāpalaiž jauns skripts, lai atsauktu neizdevušos skriptu ietekmi uz jūsu sistēmu.

Jūsu atlase pēdējā solī nosaka skripta galīgo stāvokli. Jūs varat atkārtot procesu, kā nepieciešams.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Augšupielādējiet un palaidiet izvietojamu pakotni, izmantojot LCS

Tā vietā, lai izvietotu savu izvietojamo pakotni, izmantojot jūsu finanšu un operāciju lietotnes lietotāja interfeisu, kā aprakstīts iepriekšējā sadaļā, varat to augšupielādēt LCS un izmantot parasto procedūru, lai to izvietotu. Papildinformāciju skatiet rakstā [Izvietojamo pakotņu instalēšana no komandrindas](../deployment/install-deployable-package.md).

Lai gan šai pieejai ir mazāk ierobežojumu, tā nodrošina mazāku kļūdu aizsardzību. Turklāt, tā kā tas prasa visu serveru restartēšanu, tas izraisīs dīkstāvi.
