---
title: Pielāgotu X++ skriptu palaišana ar nulles dīkstāves laiku
description: Šajā rakstā ir aprakstīts, kā augšupielādēt un palaist izvietojamas pakotnes, kurās ir pielāgoti X++ skripti bez nepieciešamības aizturēt sistēmu.
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
ms.openlocfilehash: ff01e2ff8ec105603bb91e0b555301f36e8985b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867334"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Pielāgotu X++ skriptu palaišana ar nulles dīkstāves laiku

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Šis līdzeklis ļauj jums augšupielādēt un palaist izvietojamas pakotnes, kurās ir pielāgoti X++ skripti bez nepieciešamības Microsoft Dynamics izmantot Lifecycle Services (LCS) vai bloķēt sistēmu. Tāpēc jūs varat labot nelielas datu nesakritības, neizraisot jebkādus traucējošus dīkstāves laikus.

X++ skripta izmantošanas ieguvums, lai koriģētu nelielas datu nekonsekvences, ir tāds, ka sistēma automātiski koriģēs visas saistītās tabulas, kā pieprasīts, kad tā palaiž skriptu. Šī pieeja palīdz nodrošināt korekcijas integritāti un palīdz minimizēt jaunas neatbilstības risku.

> [!IMPORTANT]
> Šī funkcija ir paredzēta tikai nelielas datu neatbilstības labošanai. To nedrīkst izmantot šādiem nolūkiem vai jebkādam citam nolūkam:
>
> - Datu vākšana
> - Shēmu izmaiņas
> - Datu migrācija vai citi ilgtermiņa procesi
> - Datu labojumi, ko var labot ar citiem līdzekļiem, piemēram, regulāri biznesa procesi, datu konsekvences rīki vai citi pašapkalpošanās rīki
>
> Šis līdzeklis ļauj autorizētiem lietotājiem tieši mainīt entītijas un to ierakstus bez nepieciešamības palaist biznesa loģiku, kas ir saistīta ar šīm entītijām. Šīs izmaiņas var izraisīt datu integritātes problēmas. Tāpēc jūsu organizācija var prasīt, lai pirms un/vai pēc skripta izpildes saņemtu apstiprinājumu un izrakstītu no iekšējiem un ārējiem auditoriem (vai citiem ekvivalentiem ekvivalentiem). Saskaņotības iemeslu dēļ izmaiņas, kas ietekmē dažus raksturlielumus, var būt nepieciešams nodot ārējos pārskatos (piemēram, finanšu pārskatos) vai ziņot valsts iestādēm. Jūsu organizācija ir tikai atbildīga par visām izmaiņām, kas tās datiem tiek veiktas, izmantojot šo funkciju, jebkuru apstiprinājumu un nozīmību vai šo izmaiņu izpaušanu un atbilstību piemērojamajiem likumiem. Jūs uzņemat visus šīs funkcijas lietošanas riskus.

Visas izvietojamās pakotnes, kas tiek augšupielādētas sistēmā, tiek izmantojot obligāto darbplūsmu. Kā drošības priekšapstrāde un lai palīdzētu nodrošināt pienākumu sadales, lietotājam, kurš augšupielādē izvietojamu pakotni, nav atļauts to apstiprināt nākamajās darbplūsmas darbībās. Citam lietotājam tas ir jāapstiprina. Tomēr pēc pakotnes apstiprināšanas lietotājs, kurš to augšupielādējis, varēs veikt atlikušos soļus.

Sistēmā ir nepieciešams, lai visas izvietojamās pakotnes izietu cauri testa palaišanai. Pirms skripta palaišanas ražošanas datiem lietotājam ir jāapstiprina, ka izvade ir pareiza, **atlasot Pieņemt testa žurnālu**. Ja izvade nav pareiza, lietotājam ir jāatzīmē pakotne kā neizdevās, atlasot **Pārtraukts**. Šajā gadījumā skriptu nevarēs palaist ražošanas datos.

Katra augšupielādētā pakotne tiek saglabāta sistēmā un tiek izieta cauri noteiktai notikumu darbplūsmai. Katram notikumam sistēma uztur žurnālu, kas ietver laikspiedolu un personas identitāti, kura veica notikumu. Šādā veidā sistēma nodrošina, ka ir auditācijas pieraksti.

Kā redzams šajā ilustrācijā, sistēma sniedz detalizētu informāciju par to, kā katra izvietojamā pakotne tika palaista X++ un kuras entītijas tika piestaustas.

![Skripta detalizētas informācijas lapa.](media/script-details.png "Skripta detalizētas informācijas lapa")

## <a name="assign-duties-to-users-to-control-access"></a>Piešķirt pienākumus lietotājiem, lai kontrolētu piekļuvi

Šī funkcija sniedz šādus pienākumus. Administratori var izmantot šos pienākumus, lai palīdzētu kontrolēt piekļuvi funkcijai.

- **Uzturēt pielāgotos skriptus** – šis pienākums sniedz iespēju augšupielādēt, pārbaudīt, pārbaudīt un palaist pielāgotus X++ skriptus vidēs (lietotāju \[pieņemšanas pārbaude UAT\] un ražošana).
- **Apstiprināt pielāgotos skriptus** – šis pienākums sniedz iespēju apstiprināt augšupielādētu pielāgotu X++ skriptu. Apstiprināšana ir obligāts solis, pirms jebkuru skriptu var testēt, pārbaudīt un palaist.

Lai samazinātu ļaunprātīgas darbības risku, katram skriptam jābūt skaidri apstiprinātam citam lietotājam, nevis lietotājam, kas to augšupielādējis. Pirms varat izmantot šo funkciju savā organizācijā, administratoram jāpiešķir iepriekšējie pienākumi vismaz diviem būtiskiem un ļoti uzticamiem lietotājiem. Kaut arī vienam lietotājam var būt abi pienākumi, šis lietotājs vēl aizvien nevarēs apstiprināt savus skriptus.

## <a name="create-a-deployable-package"></a>Izvietojamas pakotnes izveide

Šis līdzeklis pieprasa regulāru izvietojamu pakotni, kurā var izveidot Visual Studio. Norādījumus skatiet sadaļā Modeļu [izvietojamo pakotņu izveide](../deployment/create-apply-deployable-package.md).

Izvietojamajā pakotnē ir jābūt precīzi vienai darbinātai X++ klasei. Citiem vārdiem sakot, tai ir nepieciešama viena klase, kas ietver metodi, kam ir šāds paraksts.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Galvenās metodes nosaukumam jābūt mazo burtu nosaukumam.

## <a name="code-example"></a>Koda piemērs

Tālāk redzamajā koda piemērā ir parādīts, kā iespējams strukturēt izvietojamu pakotni.

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

Tālāk sniegtajā sarakstā ir aprakstītas dažas labākās prakses skripta veiksmīgai rakstīšanai, ieviešanas un palaišanai. Saraksts nav pilnīgs, un tas ir jāuzskata tikai par vadlīnijām.

- **Rakstīt** veiksmīgu ziņojumu skripta beigās. Šādā veidā varēsiet redzēt, ka skripts tika izpildīts bez izņēmumiem.
- **Pievienojiet** precīzi formulētu darbību sfēras apstrādi.
- **Izmantojiet** esošo biznesa loģiku, piemēram `update()`, metodes, **bet nevadiet** biznesa loģiku, izmantojot `doUpdate()`, `doInsert()` un `doDelete()` metodes. Šī pieeja palīdzēs nodrošināt, ka pakārtotie dati tiek apstrādāti pareizi. Tas arī būtiski samazinās tālāko datu nekonsekvences risku.
- **Aplieciniet** uzņēmuma kontekstu. Šī pieeja atklāt parastās kļūdas skripta izpildes laikā. Piemēram, tas atklāts, vai skripts tiek palaists nepareizā uzņēmumā.
- **Aplieciniet**, ka ietekmēto ierakstu skaits atbilst jūsu prognozēm. Šī pieeja atklāt, vai dati tika neparedzēti mainīti sistēmā skripta apstrādes laikā.
- **Izmantojiet** unikālus klašu nosaukumus katram skriptam (piemēram, iekļaujot nosaukums atsauci uz darba elementu). Šī pieeja neļaus nosaukuma slīpsvītras problēmas, augšupielādējot skriptu. Ja nepieciešams jauns skripta atkārtojums, noteikti piešķiriet tam jaunu nosaukumu.
- **Vispirms** pārbaudiet katru skriptu ārpus ražošanas vidē. Paredzētās ietekmes un ne nejaušiem blakusefektiem pārbaude saistītajiem datiem. Nodrošiniet, lai visi ietekmētie biznesa procesi pēc tam varētu tikt veiksmīgi un pilnībā pabeigti.

## <a name="upload-and-run-a-deployable-package"></a>Augšupielādēt un palaist izvietojamu pakotni

Izmantojiet šo procedūru, lai augšupielādētu un palaistu skriptu.

1. Finanšu un operāciju programmā dodieties uz sadaļu Sistēmas administrēšanas periodiskie **uzdevumi, datu \>\> bāzes pielāgotie skripti \>.**
1. Atlasiet **Augšupielādēt**.
1. Atlasiet izvietojamo pakotni, kuru izveidojāt, kā aprakstīts iepriekš šajā rakstā. Jums tiks piedāvāts norādīt skripta nolūku.
1. Skriptu tagad jāapstiprina citam lietotājam, nevis lietotājam, kas to augšupielādēja. Apstiprinātājam ir jāveic šādas darbības:

    1. Dodieties uz **sadaļu Sistēmas administrēšanas \>\> periodiskie datu \> bāzes pielāgotie skripti**.
    1. Atlasiet skriptu apstiprināšanai un pēc tam atlasiet **Detaļas**.
    1. Darbību rūts cilnes Apstrādāt darbplūsmu grupā Sākt **atlasiet** Apstiprināt **vai** **Noraidīt.** **·** Atlasot **Apstiprināt**, skripts tiek atzīmēts kā apstiprināts un atbloķēts testēšanai. Ja atlasāt **Noraidīt**, skripts ir bloķēts. Abos gadījumos tiek pieteikts notikums un skripta kopija tiek glabāta sistēmā.

1. Skripts ir jāpārbauda, lai nodrošinātu, ka tas veic to, ko paredzēts darīt. Pārbaudītājs var būt tāds pats kā augšupielādētājs vai apstiprinātājs, vai arī tas var būt trešais lietotājs, kuram ir nepieciešamās atļaujas. Pārbaudītājam ir jāveic tālāk norādītās darbības.

    1. Dodieties uz **sadaļu Sistēmas administrēšanas \>\> periodiskie datu \> bāzes pielāgotie skripti**.
    1. Atlasiet skriptu pārbaudei un pēc tam atlasiet **Detaļas**.
    1. Darbību rūts cilnes Process **darbplūsma** grupā **Testa** atlasiet Izpildīt **testu**. Skripts tiek palaists pagaidu darbībā, ko sistēma automātiski priekšlaikus pārtrauktu, apkopojot dažādus žurnālus un SQL priekšrakstus.
    1. Kad skripts ir beidzis darbību, pārskatiet žurnālus un pārbaudiet, vai rezultāti atbilst jūsu prognozēm. Izpildiet kādu no šīm darbībām:

        - Ja esat apmierināts ar testa rezultātu, **·** **·** **darbību** rūts cilnes Process darbplūsma grupā Pieņemt testa žurnālu, lai ļautu palaist skriptu. Notikumu žurnāls atspoguļos faktu, ka skripts tika pārbaudīts, un tas norāda, kas to pārbaudīja un kad.
        - Ja neesat apmierināts ar testa rezultātu, **·** **·** **darbību** rūts cilnes Apstrādāt darbplūsmu beigu grupā atlasiet Atcelt, lai neatļautu palaist skriptu. Sistēma saglabās skripta kopiju kopā ar tā vēstures žurnālu.

1. Kad esat pārliecināts, ka skripts atbilst jūsu prognozēm, atlasiet Palaist grupā Palaist, kas atrodas darbību rūts cilnē Apstrādāt darbplūsmu, **·** **·** **lai** to palaistu. Šī komanda ir tāda pati kā iepriekšējā testa palaišanas darbība, bet darbība tiks fiksēta beigās.
1. Kad skripts ir beidzis darbību, pārbaudiet rezultātu un apstipriniet, ka skripts darbojas, kā paredzēts. Izpildiet kādu no šīm darbībām:

    - Ja esat apmierināts ar rezultātu, darbību **rūts** **·** **cilnes** Apstrādāt darbplūsmu beigu grupā atlasīt Mērķis atrisināts. Notikumu žurnāls ataino faktu, ka skripts tika veiksmīgi izpildīts, un tas norādīs, kas pārbaudīja skriptu un kad. Skripts ir saglabāts, bet tagad ir bloķēts, un to nevar palaist vēlreiz.
    - Ja neesat apmierināts ar rezultātu, **·** **·** **darbību** rūts cilnes Apstrādāt darbplūsmu beigu grupā atlasiet Mērķis nav atrisināts. Notikumu žurnāls ataino faktu, ka skripts neatbilda tā paredzētajam nolūkam, un tas norāda, kurš izpildīs skriptu un kad. Skripts ir saglabāts, bet tagad ir bloķēts, un to nevar palaist vēlreiz. Tomēr sistēma automātiski neat atsaukt skripta darbību. Iespējams, ka jums ir jāraksta, jāimportē un jāpalaiž jauns skripts, lai atsauktu ietekmi, kādu jūsu sistēmā bija neizdevies skripts.

Atlase pēdējā solī nosaka skripta beigu stāvokli. Ja nepieciešams, procesu var atkārtot.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Augšupielādēt un palaist izvietojamu pakotni, izmantojot LCS

Tā vietā, lai izvietotu izvietojamo pakotni, izmantojot lietotāja interfeisu jūsu Finanšu un operāciju programmai, kā aprakstīts iepriekšējā sadaļā, varat to augšupielādēt LCS un izmantot regulāru procedūru tās izvietošanai. Papildinformāciju skatiet sadaļā [Izvietoto pakotņu instalēšana no komandrindas](../deployment/install-deployable-package.md).

Lai gan šai pieejai ir mazāk ierobežojumu, tā nodrošina mazāku kļūdu aizsardzību. Turklāt, tā kā tam ir jārestartē visi serveri, tas izraisīs dīkstāves laiku.
