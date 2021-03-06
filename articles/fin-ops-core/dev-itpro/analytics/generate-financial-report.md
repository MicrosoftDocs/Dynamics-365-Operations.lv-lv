---
title: Ģenerēt finanšu pārskatus
description: Šajā tēmā ir sniegta vispārīga informācija finanšu atskaites ģenerēšanu.
author: jinniew
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: c6cde37124d4a3337bca2a9b445af5fdfd87f453
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750014"
---
# <a name="generate-financial-reports"></a>Ģenerēt finanšu pārskatus

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta vispārīga informācija finanšu atskaites ģenerēšanu.

Lai izveidotu pārskatu, atveriet pārskata definīciju un pēc tam rīkjoslā atlasiet pogu **Ģenerēt**. Tiks atvērta lapa **Pārskata rindas statuss**, kas norādīs jūsu pārskata atrašanās vietu rindā. Pēc noklusējuma ģenerētais pārskats tiks atvērts pakalpojumā Tīmekļa skatītājs.

Pārskatu ģenerēšanai ir pieejamas tālāk norādītās opcijas.

- Iestatiet grafiku, lai automātiski izveidotu pārskatu vai pārskatu grupu
- Pārbaudīt trūkstošus kontus vai datus pārskatā, un apstipriniet pārskata precizitāti

Kad veidojat atskaiti, tiek izmantotas opcijas, kuras jūs norādījāt cilnēs Atskaites definīcija .

## <a name="generate-a-financial-report"></a>Ģenerēt finanšu pārskatu

Lai ģenerētu finanšu pārskatu, pārejiet uz sadaļu **Virsgrāmata** \> **Pieprasījumi un pārskati** \> **Finanšu pārskati**.

- Atlasiet pārskatu, ko vēlaties ģenerēt, un atlasiet **Ģenerēt**.
- Aizpildiet lauku **Pārskata datums** un atlasiet **Labi**.

Pēc pārskata ģenerēšanas šo pārskatu varēs skatīt sadaļā **Pārskati**.

Varat izvēlēties šo pārskatu **Skatīt** vai **Dzēst**.

Lai ģenerētu pārskatu, izmantojot līdzekli **Pārskatu veidotājs**, atveriet pārskata definīciju un pēc tam rīkjoslā atlasiet pogu **Ģenerēt**. Tiks atvērta lapa **Pārskata rindas statuss**, kas norādīs jūsu pārskata atrašanās vietu rindā. Pēc noklusējuma ģenerētais pārskats tiks atvērts pakalpojumā Tīmekļa skatītājs.

## <a name="report-groups"></a>Pārskatu grupas

Pārskatu grupas ir efektīvs veids, kā vienlaicīgi ģenerēt vairākus pārskatus. Piemēram, pieņemsim, ka zināt, ka mēneša beigās lietotāji katru mēnesi ģenerē astoņus pārskatus. Izveidojiet Pārskatu grupu un tā vietā, lai atlasītu **Ģenerēt** katram no astoņiem pārskatiem grupā, varat atlasīt **Ģenerēt** pārskatu grupai, un astoņi pārskati tiks ģenerēti vienā solī. Kad pārskati atlasītajā pārskatu grupā ir ģenerēti, varat atvērt **Finanšu parskati** (**Virsgrāmata > Uzziņas un pārskati >Finanšu pārskati**), lai apskatītu atsevišķus pārskatus. Lai iestatītu pārskatu grupu, izpildiet tālāk aprakstītās darbības.

1. Pārskatu noformētājā atlasiet **Pārskatu grupas**. 
2. Atlasiet esošās pārskata definīcijas, ko iekļaut pārskatu grupā. 
3. Atlasiet uzņēmuma, detalizētās informācijas un datuma iestatījumu pārlabošanu no katra pārskata, kas tiks iekļauti grupā.
   Mēs iesakām katram pārskatam iestatījumu **Uzņēmums**, **Periods**, **Gads** un **Detalizācijas līmenis**. 
4. Saglabājiet pārskatu grupu.

## <a name="schedule-report-generation"></a>Pārskatu ģenerēšanas ieplānošana
Daudziem uzņēmumiem ir izveidota pamata pārskatu kopa, kas tiek palaisti ieplānotajos intervālos atbilstošo uzņēmuma darbības procesiem. Jūs var ieplānot regulāru pārskatu izveidi, piemēram, katru dienu, katru nedēļu, katru mēnesi vai reizi gadā. Tādā veidā var palaist vienu pārskatu vai vairāku pārskatu grupu, tostarp, ietverot vairākus uzņēmumus. Savi akreditācijas dati ir jāievada visiem norādītajiem uzņēmumiem, piemēram, pārskatu koka definīcijā norādītajiem uzņēmumiem. Ja akreditācijas dati nav derīgi, pārskats parādīs tikai informāciju, kurai jums ir piekļuves tiesības, piemēram, uzņēmums, ko esat reģistrējuši. Vispirms izlasiet izvades informāciju no pārskata grupas, un pēc tam no atsevišķiem pārskatiem.

Kad pārskata grafiki tiek izveidoti un saglabāti, tie tiek parādīti navigācijas rūtī sadaļā Pārskatu grafiki. Lai kārtotu pārskatus, varat izveidot mapes. Ja viens grafikā ietvertais pārskats netiek palaists, visi citi šajā grafikā ietvertie pārskati tiks palaisti.

> [!IMPORTANT]
> Lai izveidotu, modificētu un dzēstu pārskatu grafikus, lietotājam jābūt izstrādātāja vai administratora lomai. Izpildot pārskatu, kura akreditācijas dati tika izmantoti, lai izveidotu grafiku, tiek izmantoti arī lai izveidotu pārskatu.

### <a name="create-a-report-schedule"></a>Izveidot pārskata grafiku

1. Pārskatu veidotājā izvēlnē **Fails**, atlasiet **Jauns**, un pēc tam atlasiet **Pārskata grafiks**. Atveras dialoglodziņš **Jauns pārskata grafiks**.
2. Sadaļā **Iestatījumi** atlasiet atsevišķu pārskatu vai pārskatu grupu, lai to ieplānotu. Ir pieejami tikai tā uzņēmuma vai veidošanas bloku atlases pārskati vai pārskatu grupas, kurā pašlaik esat pieteicies.
3. Atlasiet izvēles rūtiņu **Aktīvs**, lai ieslēgtu pārskatu grafiku. Iespējot vai atspējot pārskatu grafiku var tikai pārskata veidotājs vai administrators.
4. Atlasiet pogu **Atļaujas**, lai ievadītu uzņēmuma akreditācijas datus. Pēc noklusējuma pieteikšanās informācija tiek izmantota uzņēmumam, kurā pašlaik esat pieteicies. Ja citi uzņēmumi ir iekļauti, piemēram, pārskata koka definīcijās, atlasiet **Izmantot atsevišķus akreditācijas datus**, un pēc tam ievadiet jebkura cita uzņēmuma, kas ir iekļauts pārskata grafikā, akreditācijas datus. Varat atlasīt **Windows autentifikācija** vai katram uzņēmumam ievadīt lietotāja vārdu un paroli. Atlasiet izvēles rūtiņu **Akreditācijas datu saglabāšana**, lai saglabātu akreditācijas datus šiem uzņēmumiem, un pēc tam atlasiet **Labi**, lai aizvērtu dialoglodziņu.
5. Sadaļas **Biežums** laukā **Periodiskuma sākšana** atlasiet datumu, kad grafiks ir jāsāk. Pēc noklusējuma tiek atlasīts pašreizējais klienta datora sistēmas datums.
6. Laukā **Pārskata izpilde** izvēlieties laiku, kad pārskats jāizpilda. Ja ievadīsit laiku, kas ir agrāks par pašreizējo sistēmas laiku, pārskats tiks palaists nākamajā ieplānotajā datumā.
7. Apgabalā **Periodiskuma modelis** norādiet, cik bieži pārskats tiek izpildīts. Pēc noklusējuma tiek atlasīta opcija **Katru dienu** ar parametra Intervāls (dienas) vērtību 1. Ir pieejamas arī šādas opcijas: Katru nedēļu, Katru mēnesi un Katru gadu.
8. Apgabalā Atkārtošanās diapazons atlasiet, kad jāpārtrauc pārskata ģenerēšana.

    - **Nav beigu datuma** — pārskata grafiks darbojas nenoteiktu laiku.
    - **Iestatīt gadījumu skaitu** — pārskata grafiks tiek izpildīts noteiktu reižu skaitu un pēc tam tiek deaktivizēts.
    - **Beidzas** — pārskatu grafiks beidzas norādītajā datumā.

9. Atlasiet **Saglabāt**. Dialoglodziņā **Saglabāt kā** ievadiet pārskatu grafika unikālu nosaukumu un aprakstu.

Lai kopētu pārskatu grafiku, ir nepieciešama veidotāja vai administratora loma. Pat tad, ja administrators modificē atskaišu grafiku, pārskats satur tā lietotāja akreditācijas datus, kurš izveidoja pārskatu.

### <a name="copy-a-report-schedule"></a>Kopēt pārskata grafiku

1. Pārskata veidotāja navigācijas rūtī atlasiet **Pārskatu grafiki** un atveriet pārskata grafiku, kuru nepieciešams nokopēt.
2. Izvēlnē **Fails** atlasiet **Saglabāt kā** un pēc tam ievadiet grafika jauno nosaukumu un aprakstu dialoglodziņā **Saglabāt kā**. Atlasiet **Labi**, un jaunais grafiks tiks parādīts navigācijas rūtī.
3. Jaunajā grafikā modificējiet laukus un informāciju pēc nepieciešamības, un pēc tam rīkjosla atlasiet **Saglabāt** vai atlasiet **Saglabāt** izvēlnē **Fails**.

Lai dzēstu pārskata grafiku, jums ir jābūt atskaišu grafika īpašniekam, vai administratora lomai.

### <a name="delete-a-report-schedule"></a>Dzēst pārskata grafiku

1. Pārskata veidotāja navigācijas rūtī atlasiet **Pārskatu grafiki**.
2. Atlasiet pārskata grafiku, kuru nepieciešams izdzēst, un pēc tam atlasiet **Dzēst** vai nospiediet pogu **Dzēst**.
3. Dzēšanas apstiprināšanas dialoglodziņā atlasiet **Jā**, lai neatgriezeniski dzēstu pārskata grafiku. Ja jums nav atļaujas dzēst šo grafiku, tiks parādīts ziņojums un pārskats netiks dzēsts.

### <a name="credentials-and-report-schedules"></a>Akreditācijas dati un pārskatu grafiki

Neievadot akreditācijas datus, kas ir nepieciešami visiem uzņēmumiem, kas ir iekļauti pārskatos, saglabājot pārskata grafiku, tiek parādīts šāds ziņojums: "Ievadiet akreditācijas datus uzņēmumiem, kuri ir iekļauti šajā pārskata grafikā. Lai ievadītu savus akreditācijas datus, atlasiet pogu Atļaujas.”

Piemēram, lietotājs pieteicās uzņēmumā A, izmantojot savu lietotājvārdu un paroli. Lietotājs izveido grafiku pārskatam, kas izmanto pārskata koka definīciju, lai apkopotu datus no vairākiem uzņēmumiem. Saglabājot pārskatu grafiku, lietotājam tiek parādīta uzvedne, kurā jāievada citu pārskatu koka definīcijā norādīto uzņēmumu akreditācijas dati. Kad jūsu akreditācijas datu derīguma termiņš beidzas, ietekmētie pārskati atskaišu grafikā netiek izveidoti līdz akreditācijas dati netiek atjaunināti. Pārskata rindā tiek parādīts ziņojums, lai norādītu, ka nepieciešams atjaunināt atļaujas. Pārskata grafiks neizdodas, ja notiek jebkurš no šiem scenārijiem (jo tiem ir nepieciešami akreditācijas dati):

- Pārskatu kokam tika pievienots jauns uzņēmums atsevišķam pārskatam.
- Pārskatu grupā ietvertais pārskats tika modificēts.
- Pārskatu grupā ir pievienots jauns pārskats papildu uzņēmumam.

Lai turpinātu, atlasiet pogu **Atļaujas** dialoglodziņā **Pārskatu plānošana** un pēc tam ievadiet atbilstošos akreditācijas datus.

## <a name="missing-account-analysis-feature"></a>Trūkstošo kontu analīzes līdzeklis
Jūs varat meklēt finanšu kontus un dimensijas, kas, iespējams, nav norādītas visās rindu definīcijās, pārskata koka definīcijās un pārskatu definīcijas veidošanas bloka grupā. Tas ir noderīgi, ja izveidojat vai atjaunināt vairākus kontus vai veidošanas blokus īsā laika periodā, un vēlaties pārbaudīt, vai visa jaunā informācija tiek iekļauta jūsu pārskatos.

Trūkstošie konti tiek noteikti, izmantojot mazāko un lielāko vērtību no rindas definīcijas vai atskaites koka definīcijas, un pēc tam parāda sarakstu ar kontiem, kas nav rindas definīcijas vai atskaites koka definīcijā, bet kas atrodas finanšu datos. Ja trūkstošā konta vērtība ir lielāka vai mazāka par rindas definīcijā norādītajām vērtībām, šis konts netiek rādīts trūkstošo kontu sarakstā.

> [!TIP]
> Lai pārbaudītu datu pareizību, šo procesu ir ieteicams veikt ikreiz pirms mēneša pārskatu izveides, kā arī jaunu veidošanas bloku izveides laikā.

Pārskatos, kuros ir vērtību diapazoni, ir mazāka trūkstošu kontu varbūtība. Kad iespējams, veidošanas blokos izmantojiet diapazonus, lai ietvertu jaunus kontus pēc to izveides. Ja pārskata definīcijā uzņēmuma iestatījums ir @ANY, varat pieteikties konkrēta uzņēmuma profilā un izpildīt trūkstošo kontu analīzi šajā uzņēmumā.

> [!NOTE]
> Ja tika pievienots jauns uzņēmums, jums šis jaunais uzņēmums ir jāpievieno atskaišu kokiem jebkurā esošā atskaitē, citādi šis uzņēmums netiks iekļauts trūkstošo kontu analīzē.

### <a name="run-missing-account-analysis"></a>Palaist trūkstošo kontu analīzes līdzekli

1. Pārskatu veidotājā atlasiet **Rīki** un pēc tam atlasiet **Trūkstošo kontu analīze**.
2. Laukā **Uzņēmuma filtrs** atlasiet uzņēmumu, lai filtrētu rezultātus, vai atlasiet **Viss (bez filtra)**, lai parādītu rezultātus no visiem pieejamajiem uzņēmumiem.
3. Laukā **Dimensiju filtrs** atlasiet dimensiju, lai filtrētu rezultātus, vai izvēlieties **Viss (bez filtra)**, lai skatītu visu dimensiju informāciju visām pieejamajām dimensijām.
4. Laukā **Grupēt pēc** atlasiet opciju rezultātu kārtošanai. Rezultātus var kārtot pēc izmantotā veidošanas bloka, kā arī pēc dimensijas un vērtību kopas.
5. Pārskatiet parādāmos rezultātus. Atlasot vienumu augšējā rūtī, apakšējā rūtī tiek rādīta papildu informācija par izņēmumu. Šajā informācijā ir ietverti dati par saistītajām dimensijām, vērtībām un pārskatiem.
6. Lai atvērtu iesaistīto vienumu atlasiet saistīto ikonu, kas tiek parādīts saraksta rūtī vai ar peles labo pogu noklikšķiniet uz vienuma, un atlasiet **Atvērt**. Lai atlasītu vairākus vienumus, turiet nospiestu taustiņu **Ctrl**, atlasot vienumus apakšējā rūtī.
7. Ja jebkuri vienumi, veidošanas bloki vai pārskati tiek atgriezti, jo tie nav jāiekļauj analīzē, noklikšķiniet ar peles labo pogu uz vienuma un atlasiet **Izslēgt**, vai atlasiet izvēles rūtiņu **Izslēgt** blakus vienumam, lai noņemtu to no saraksta. Neiekļautie vienumu netiek iekļauti sarakstā, kad tas tiek atsvaidzināts. Lai atlasītu vairākus vienumus, turiet nospiestu taustiņu **Ctrl**, atlasot vienumus apakšējā rūtī. Lai skatītu visus vienumus, tostarp rezultātus, ko iepriekš neiekļāvāt analīzē, atzīmējiet izvēles rūtiņu **Rādīt neiekļautos veidošanas blokus un vērtības** un vērtības un pēc tam atlasiet **Atsvaidzināt**.
8. Atlasiet **Atsvaidzināt**, lai atsvaidzinātu izņēmumus, kas ir jārisina. Atlasiet **Jā**, lai pilnībā atsvaidzinātu visus rezultātus vai atlasiet **Nē**, lai veiktu risināmo vienumu daļēju atsvaidzināšanu.

    > [!NOTE]
    > Forma tiek automātiski atsvaidzināta atvēršanas brīdī, ja vien tā netika atvērta pēdējo 15 minūšu laika.

9. Kad šīs problēmas ir novērstas, atlasiet **Labi**, lai aizvērtu dialoglodziņu.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Tastatūras saīsnes trūkstošu kontu analīzei
Kad palaižat trūkstošo kontu analīzi, ir pieejami tālāk norādītie īsinājumtaustiņi.

| Darbība                           | Nospiests: |
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
