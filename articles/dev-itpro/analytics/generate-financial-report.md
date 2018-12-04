---
title: "Ģenerēt finanšu pārskatus"
description: "Šajā tēmā ir sniegta vispārīga informācija finanšu atskaites ģenerēšanu."
author: aprilolson
manager: AnnBe
ms.date: 09/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a128f326cb89ab00e69be40801553c0ac551446e
ms.openlocfilehash: 70fa1298c3af43f62b8fa0b833fa817f17858c47
ms.contentlocale: lv-lv
ms.lasthandoff: 09/27/2018

---

# <a name="generate-financial-reports"></a>Ģenerēt finanšu pārskatus

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta vispārīga informācija finanšu atskaites ģenerēšanu.

Lai izveidotu pārskatu, atveriet pārskata definīciju un pēc tam rīkjoslā noklikšķiniet pogu Ģenerēt. Tiks atvērts logs Pārskata rindas statuss, un norādīs jūsu pārskata atrašanās vietu rindā. Pēc noklusējuma ģenerētais pārskats tiks atvērts pakalpojumā Tīmekļa skatītājs.

Pārskatu ģenerēšanai ir pieejamas tālāk norādītās opcijas.

- Iestatiet grafiku, lai automātiski izveidotu pārskatu vai pārskatu grupu
- Pārbaudīt trūkstošus kontus vai datus pārskatā, un apstipriniet pārskata precizitāti

Kad veidojat atskaiti, tiek izmantotas opcijas, kuras jūs norādījāt cilnēs Atskaites definīcija .

## <a name="generate-a-financial-report"></a>Finanšu pārskata ģenerēšana

Lai ģenerētu finanšu pārskatu, izmantojot Microsoft Dynamics 365 for Finance and Operations, dodieties uz **Virsgrāmata** \> **Pieprasījumi un pārskati** \> **Finanšu pārskati**.

- Atlasiet pārskatu, ko vēlaties ģenerēt, un noklikšķiniet uz **Ģenerēt**.
- Aizpildiet lauku **Pārskata datums** un noklikšķiniet uz **Labi**.

Pēc pārskata ģenerēšanas šo pārskatu varēs skatīt sadaļā **Pārskati**.

Varat izvēlēties šo pārskatu **Skatīt** vai **Dzēst**.

Lai ģenerētu pārskatu, izmantojot līdzekli **Pārskatu veidotājs**, atveriet pārskata definīciju un pēc tam rīkjoslā noklikšķiniet uz pogas Ģenerēt. Tiks atvērts logs Pārskata rindas statuss, un norādīs jūsu pārskata atrašanās vietu rindā. Pēc noklusējuma ģenerētais pārskats tiks atvērts pakalpojumā Tīmekļa skatītājs.

## <a name="schedule-report-generation"></a>Pārskatu ģenerēšanas ieplānošana
Daudziem uzņēmumiem ir izveidota pamata pārskatu kopa, kas tiek palaisti ieplānotajos intervālos atbilstošo uzņēmuma darbības procesiem. Jūs var ieplānot regulāru pārskatu izveidi, piemēram, katru dienu, katru nedēļu, katru mēnesi vai reizi gadā. Tādā veidā var palaist vienu pārskatu vai vairāku pārskatu grupu, tostarp, ietverot vairākus uzņēmumus. Savi akreditācijas dati ir jāievada visiem norādītajiem uzņēmumiem, piemēram, pārskatu koka definīcijā norādītajiem uzņēmumiem. Ja akreditācijas dati nav derīgi, pārskats parādīs tikai informāciju, kurai jums ir piekļuves tiesības, piemēram, uzņēmums, ko esat reģistrējuši. Vispirms izlasiet izvades informāciju no pārskata grupas, un pēc tam no atsevišķiem pārskatiem.

Kad pārskata grafiki tiek izveidoti un saglabāti, tie tiek parādīti navigācijas rūtī sadaļā Pārskatu grafiki. Lai kārtotu pārskatus, varat izveidot mapes. Ja viens grafikā ietvertais pārskats netiek palaists, visi citi šajā grafikā ietvertie pārskati tiks palaisti.

> [!IMPORTANT]
> Lai izveidotu, modificētu un dzēstu pārskatu grafikus, lietotājam jābūt izstrādātāja vai administratora lomai. Izpildot pārskatu, kura akreditācijas dati tika izmantoti, lai izveidotu grafiku, tiek izmantoti arī lai izveidotu pārskatu.

### <a name="create-a-report-schedule"></a>Izveidot pārskata grafiku

1. Pārskatu veidotājā izvēlnē Fails, noklikšķiniet uz Jauns, un pēc tam atlasiet Pārskata grafiks. Atveras dialoglodziņš Jauns pārskata grafiks.
2. Sadaļā Iestatījumi, atlasiet atsevišķu pārskatu vai pārskata grupu, lai to ieplānotu. Ir pieejami tikai tā uzņēmuma vai veidošanas bloku atlases pārskati vai pārskatu grupas, kurā pašlaik esat pieteicies.
3. Lai iespējotu pārskatu grafiku, atzīmējiet izvēles rūtiņu Aktīvs. Iespējot vai atspējot pārskatu grafiku var tikai pārskata veidotājs vai administrators.
4. Lai ievadītu uzņēmuma akreditācijas datus, noklikšķiniet uz pogas Atļaujas. Pēc noklusējuma pieteikšanās informācija tiek izmantota uzņēmumam, kurā pašlaik esat pieteicies. Ja ir ietverti arī citi uzņēmumi, piemēram, pārskatu koka definīcijās, atlasiet Izmantot atsevišķus akreditācijas datus un ievadiet visu citu pārskatu grafikā ietverto uzņēmumu akreditācijas datus. Varat atlasīt Windows autentifikācija vai ierakstīt katram uzņēmumam piešķirto lietotājvārdu un paroli. Atlasiet izvēles rūtiņu Akreditācijas datu saglabāšana, lai saglabātu akreditācijas datus šiem uzņēmumiem, un pēc tam noklikšķiniet uz Labi, lai aizvērtu dialoglodziņu.
5. Sadaļā Biežums, laukā Periodiskuma sākšana atlasiet datumu, kad grafiks ir jāsāk. Pēc noklusējuma tiek atlasīts pašreizējais klienta datora sistēmas datums.
6. Laukā Palaist pārskatu atlasiet pārskata palaišanas laiku. Ja ievadīsit laiku, kas ir agrāks par pašreizējo sistēmas laiku, pārskats tiks palaists nākamajā ieplānotajā datumā.
7. Apgabalā Atkārtošanās shēma norādiet, cik bieži pārskati ir jāpalaiž. Pēc noklusējuma tiek atlasīta opcija Katru dienu ar parametra Intervāls (dienas) vērtību 1. Ir pieejamas arī šādas opcijas: Katru nedēļu, Katru mēnesi un Katru gadu.
8. Apgabalā Atkārtošanās diapazons atlasiet, kad jāpārtrauc pārskata ģenerēšana.

    - Bez beigu datuma — pārskata grafiks ir aktīvs nenoteiktu laiku.
    - Iestatīt gadījumu skaitu — pārskata grafiks ir aktīvs noteiktu reižu skaitu. Pēc tam tas tiek deaktivizēts.
    - Beidzas — pārskata grafiks beidzas norādītajā datumā.

9. Rīkjoslā noklikšķiniet uz Saglabāt. Dialoglodziņā Saglabāt kā, ievadiet pārskatu grafika unikālu nosaukumu un aprakstu.

Lai kopētu pārskatu grafiku, ir nepieciešama veidotāja vai administratora loma. Pat tad, ja administrators modificē atskaišu grafiku, pārskats satur tā lietotāja akreditācijas datus, kurš izveidoja pārskatu.

### <a name="copy-a-report-schedule"></a>Kopēt pārskata grafiku

1. Pārskata veidotāja navigācijas rūtī noklikšķiniet uz Pārskatu grafiki, un atveriet pārskata grafiku, kuru nepieciešams nokopēt.
2. Izvēlnē Fails noklikšķiniet uz Saglabāt kā un pēc tam dialoglodziņā Saglabāt kā ievadiet jauno nosaukumu un aprakstu. Noklikšķiniet uz Labi. Tagad jaunais grafiks ir redzams navigācijas rūtī.
3. Jaunajā grafikā, modificējiet laukus un informāciju pēc nepieciešamības, un pēc tam rīkjosla noklikšķiniet uz Saglabāt, vai noklikšķiniet uz Saglabāt izvēlnē Fails.

Lai dzēstu pārskata grafiku, jums ir jābūt atskaišu grafika īpašniekam, vai administratora lomai.

### <a name="delete-a-report-schedule"></a>Dzēst pārskata grafiku

1. Pārskata veidotājā, navigācijas rūtī noklikšķiniet uz Pārskatu grafiki.
2. Atlasiet dzēšamo pārskatu grafiku un pēc tam noklikšķiniet uz Dzēst vai nospiediet taustiņu Delete.
3. Dzēšanas apstiprināšanas dialoglodziņā noklikšķiniet uz Jā, lai neatgriezeniski dzēstu pārskata grafiku. Ja jums nav atļaujas dzēst šo grafiku, tiks parādīts ziņojums un pārskats netiks dzēsts.

### <a name="credentials-and-report-schedules"></a>Akreditācijas dati un pārskatu grafiki

Neievadot akreditācijas datus, kas ir nepieciešami visiem uzņēmumiem, kas ir iekļauti pārskatos, saglabājot pārskata grafiku, tiek parādīts šāds ziņojums: "Ievadiet akreditācijas datus uzņēmumiem, kuri ir iekļauti šajā pārskata grafikā. Lai ievadītu savus akreditācijas datus, atlasiet pogu Atļaujas.”

Piemēram, Paula pieteicās uzņēmumā A, izmantojot savu lietotājvārdu un paroli. Viņa izveido grafiku pārskatam, kas izmanto pārskata koka definīciju, lai apkopotu datus no vairākiem uzņēmumiem. Saglabājot pārskatu grafiku, Paulai tiek parādīta uzvedne, kurā jāievada citu pārskatu koka definīcijā norādīto uzņēmumu akreditācijas dati. Kad jūsu akreditācijas datu derīguma termiņš beidzas, ietekmētie pārskati atskaišu grafikā netiek izveidoti līdz akreditācijas dati netiek atjaunināti. Pārskata rindā tiek parādīts ziņojums, lai norādītu, ka nepieciešams atjaunināt atļaujas. Pārskata grafiks neizdodas, ja notiek jebkurš no šiem scenārijiem (jo tiem ir nepieciešami akreditācijas dati):

- Pārskatu kokam tika pievienots jauns uzņēmums atsevišķam pārskatam.
- Pārskatu grupā ietvertais pārskats tika modificēts.
- Pārskatu grupā ir pievienots jauns pārskats papildu uzņēmumam.

Lai turpinātu, noklikšķiniet uz pogas Atļaujas dialoglodziņā Pārskatu plānošana, un pēc tam ievadiet atbilstošos akreditācijas datus.

## <a name="missing-account-analysis-feature"></a>Trūkstošo kontu analīzes līdzeklis
Jūs varat meklēt finanšu kontus un dimensijas, kas, iespējams, nav norādītas visās rindu definīcijās, pārskata koka definīcijās un pārskatu definīcijas veidošanas bloka grupā. Tas ir noderīgi, ja izveidojat vai atjaunināt vairākus kontu vai veidošanas blokus īsā laika periodā, un vēlaties pārbaudīt, vai visa jaunā informācija tiek iekļauta jūsu pārskatos.

Trūkstošie konti tiek noteikti, izmantojot mazāko un lielāko vērtību no rindas definīcijas vai atskaites koka definīcijas, un pēc tam parāda sarakstu ar kontiem, kas nav rindas definīcijas vai atskaites koka definīcijā, bet kas atrodas finanšu datos. Ja trūkstošā konta vērtība ir lielāka vai mazāka par rindas definīcijā norādītajām vērtībām, šis konts netiek rādīts trūkstošo kontu sarakstā.

> [!TIP]
> Lai pārbaudītu datu pareizību, šo procesu ir ieteicams veikt ikreiz pirms mēneša pārskatu izveides, kā arī jaunu veidošanas bloku izveides laikā.

Pārskatos, kuros ir vērtību diapazoni, ir mazāka trūkstošu kontu varbūtība. Ja iespējams, izmantojiet diapazonus veidošanas blokos, lai iekļautu jaunus kontus, kad tie tiek izveidoti. Ja jebkura pārskata definīcijā kā uzņēmums ir iestatīts @ANY, varat pieteikties noteiktā uzņēmumā un izpildīt trūkstošo kontu analīzi šim uzņēmumam.

> [!NOTE]
> Ja tika pievienots jauns uzņēmums, jums šis jaunais uzņēmums ir jāpievieno atskaišu kokiem jebkurā esošā atskaitē, citādi šis uzņēmums netiks iekļauts trūkstošo kontu analīzē.

### <a name="run-missing-account-analysis"></a>Palaist trūkstošo kontu analīzes līdzekli

1. Pārskatu veidotājā noklikšķiniet Rīki, un pēc tam noklikšķiniet uz Trūkstošo kontu analīze.
2. Laukā Uzņēmumu filtrs atlasiet uzņēmumu, atbilstoši kuram ir jāfiltrē rezultāti, vai atlasiet Visi (bez filtra), lai skatītu visu pieejamo uzņēmumu rezultātus.
3. Laukā Dimensiju filtrs atlasiet dimensiju, atbilstoši kurai ir jāfiltrē rezultāti, vai atlasiet Visas (bez filtra), lai skatītu visu pieejamo dimensiju informāciju.
4. Laukā Grupēt pēc atlasiet rezultātu kārtošanas opciju. Rezultātus var kārtot pēc izmantotā veidošanas bloka, kā arī pēc dimensijas un vērtību kopas.
5. Pārskatiet parādāmos rezultātus. Atlasot vienumu augšējā rūtī, apakšējā rūtī tiek rādīta papildu informācija par izņēmumu. Šajā informācijā ir ietverti dati par saistītajām dimensijām, vērtībām un pārskatiem.
6. Lai atvērtu iesaistīto vienumu, noklikšķiniet uz saistīto ikonu, kas tiek parādīts saraksta rūtī vai ar peles labo pogu noklikšķiniet uz vienuma, un atlasiet Atvērt. Lai atlasītu vairākus vienumus, turiet nospiestu taustiņu Ctrl, atlasot vienumus apakšējā rūtī.
7. Ja jebkuri vienumi, veidošanas bloki vai pārskati tiek atgriezti, jo tie nav jāiekļauj analīzē, noklikšķiniet ar peles labo pogu uz vienuma, un atlasiet Izslēgt, vai atlasiet izvēles rūtiņu Izslēgt blakus vienumam, lai noņemtu to no saraksta. Neiekļautie vienumu netiek iekļauti sarakstā, kad tas tiek atsvaidzināts. Lai atlasītu vairākus vienumus, nospiediet un turiet taustiņu Ctrl, kamēr atlasāt vienumus apakšējā rūtī. Lai skatītu visus vienumus, tostarp rezultātus, ko iepriekš neiekļāvāt analīzē, atzīmējiet izvēles rūtiņu Rādīt neiekļautos veidošanas blokus un vērtības un pēc tam noklikšķiniet uz Atsvaidzināt.
8. Noklikšķiniet uz Atsvaidzināt, lai atsvaidzinātu izņēmumus, ko norādījāt. Noklikšķiniet uz Jā, lai atsvaidzinātu visus rezultātus (pilnīgā atsvaidzināšana), vai noklikšķiniet uz Nē, lai atsvaidzinātu norādītos vienumus (daļējā atsvaidzināšana).

    > [!NOTE]
    > Forma tiek automātiski atsvaidzināta atvēršanas brīdī, ja vien tā netika atvērta pēdējo 15 minūšu laika.

9. Kad šīs problēmas ir novērstas, noklikšķiniet uz Labi, lai aizvērtu dialoglodziņu.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Tastatūras saīsnes trūkstošu kontu analīzei
Kad palaižat trūkstošo kontu analīzi, ir pieejami tālāk norādītie īsinājumtaustiņi.

| Lai izpildītu šo darbību                           | Izmantojiet šo tastatūras saīsni |
|--------------------------------------|----------------------------|
| Filtrēt pēc uzņēmuma                    | Alt+C                      |
| Filtrēt pēc dimensijas                  | Alt + D                      |
| Atlasīt lauku Grupēt pēc            | Alt+G                      |
| Rādīt neiekļautos veidošanas blokus un vērtības      | Alt+S                      |
| Atsvaidzināt rezultātus                      | Alt+R                      |
| Neiekļaut atlasīto veidošanas bloku  | Alt+X                      |
| Neiekļaut atlasīto rindas definīciju  | Ctrl+B                     |
| Neiekļaut atlasīto dimensijas vērtību | Ctrl+D                     |
| Atvērt atlasīto pārskata definīciju  | Ctrl+R                     |
| Atvērt atlasīto rindas definīciju     | Ctrl+O                     |


## <a name="additional-resources"></a>Papildu resursi

[Finanšu pārskati](financial-reporting-intro.md)

[Pārskatu noformētāja interfeiss](report-designer-interface.md)

