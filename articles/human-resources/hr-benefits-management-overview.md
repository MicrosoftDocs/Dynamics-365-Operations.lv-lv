---
title: Atvieglojumu pārvaldības pārskats
description: Šajā rakstā ir sniegts pārskats par atvieglojumu pārvaldības līdzekli sistēmā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/06/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f008c273a3088353c33ae8c4b0b3cbc6b274fbcf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901152"
---
# <a name="benefits-management-overview"></a>Atvieglojumu pārvaldības pārskats


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Lai saglabātu konkurētspēju, jāpiedāvā bagātīgs atvieglojumu kopums, lai piesaistītu un saglabātu labākos darbiniekus. Papildus standarta atvieglojumiem, piemēram, ārstniecības un zobārstniecības apdrošināšanai, varat arī piedāvāt tādus paplašinātos pakalpojumus kā palīdzība ar adopciju, atpūtas programmas un pabalsts apģērbam. Microsoft Dynamics 365 Human Resources atvieglojumu pārvaldība nodrošina elastīgu risinājumu, kas atbalsta plaša spektra atvieglojumu opcijas. Human Resources ietver arī ērti lietojamu darbinieku pieredzi, kas demonstrē jūsu piedāvājumus.

- Uzlabotie atvieglojumu plāni ļauj izveidot un pārvaldīt unikālus atvieglojumu plānus, kā arī atbalstīt kompleksas atvieglojumu apjoma tabulas un ligzdotos līmeņus. Ērtākai darbinieku pieredzei varat viegli izveidot atvieglojumu programmas, komplektus un automātiskas reģistrācijas kārtulas.
- Brīvā režīma kredīta programmas ļauj jums proporcionāli atbalstīt pensionēšanos un citus dzīves notikumus.
- Plašie piemērotības kārtulas nodrošina vajadzīgā atvieglojuma pieejamību attiecīgajiem darbiniekiem.
- Tiešsaistes atvieglojumu reģistrācija sniedz darbiniekiem ērtu pieredzi.
- Kvalificēta dzīves notikumu apstrāde atbalsta turpmākos dzīves notikumus.

Ja vēlaties piekļūt demonstrācijas datiem, būs nepieciešams atkārtoti izvietot savu smilškastes vidi.

> [!NOTE]
> Tagad varat pielāgot Atvieglojumu pārvaldības lapas. Tagad varat pievienot pielāgotos laukus, kas saistīti ar seguma likmēm, lapai **Seguma opcija** atvieglojumu plāniem. Lai iegūtu papildinformāciju par darbu ar pielāgotiem laukiem, skatiet rakstā [Pielāgotie lauki](hr-developer-custom-fields.md).
>
> ![Atvieglojumu pārvaldības pielāgotie lauki](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Atvieglojumu pārvaldības iespējošana

Šis raksts apraksta, kā Personāla vadībā ieslēgt priekšskatījuma līdzekļus. Tajā arī norādīts, kādus pastāvošos Human Resources līdzekļus aizstāj šī Atvieglojumu pārvaldība, vai kādi līdzekļi tiek atspējoti, ieslēdzot atvieglojumu pārvaldību.

> [!IMPORTANT]
> Pēc tam, kad iespējojat Atvieglojumu pārvaldību **Ražošanas** vidē, to nevar atspējot. Iesakām iespējot un testēt Atvieglojumu pārvaldību **Smilškastes** vidē pirms tās iespējošanas **Ražošanas** vidē. Pastāv būtiskas atšķirības starp mantoto Atvieglojumu funkcionalitāti un jauno Atvieglojumu pārvaldības funkcionalitāti, kam nepieciešami papildu iestatījumi, un tie ir jāpārbauda pirms ielaišanas ražošanā.

Papildinformāciju skatiet tēmā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

## <a name="process-overview"></a>Procesa apskats

Atvieglojumu konfigurēšanas process ietver sekojošos uzdevumus:

1.  Iestatiet nepieciešamo atvieglojumu informāciju.
2.  Iestatiet neobligāto atvieglojumu informāciju.
3.  Iestatīt atvieglojumu plānus.
4.  Iestatīt brīvā režīma kredīta programmas (neobligāti).
5.  Konfigurējiet nepieciešamo darbinieka informāciju.
6.  Konfigurējiet neobligāto darbinieka informāciju.
7.  Apstrādā darbiniekus, lai noteiktu piemērotību.
8.  Darbinieki izvēlas plānus, izmantojot darbinieku pašapkalpošanos (pēc izvēles).
9.  Apstipriniet darbinieka plāna atlases.
10. Dzīves notikumu apstrāde (neobligāti).
11. Likmes atjaunināšana (neobligāti).

## <a name="set-up-required-benefit-information"></a>Iestatiet nepieciešamo atvieglojumu informāciju

Pirms darbiniekus var reģistrēt plānos, jāiestata vairāki komponenti:

- **Atvieglojumu pārvaldības parametri** – šie iestatījumi tiek koplietoti uzņēmumu dažādos uzņēmumos. Varat iestatīt noklusējuma pamatojuma kodus, iespējot opciju **Atvieglojumi gada alga**, iestatīt noklusējuma maksājumu biežumu jaunām nolīgšanas un aktivizēt dzīves notikumus. Plašāku informāciju skatiet [Iestatiet atvieglojumu pārvaldības parametrus](hr-benefits-setup-parameters.md).
- **Personas kontaktu piemērotības opcijas** – Personīgie kontakti ir personas, kas būs uzstādītas vai nu apgādājamām, vai saņēmēju no iestatītajiem plāniem. Parasti tie ir bērni, laulātie vai uzticības organizācijas. Papildinformāciju skatiet rakstā [Konfigurēt personīgo kontaktu piemērotības opcijas](hr-benefits-setup-contact-eligibility-options.md).
- **Vajadzības opcijas** – iestatiet vajadzību tipus, kas būs pieejami plānam. It īpaši norādiet, kurš ir jāsedz vai cik daudz seguma ir pieejams. Papildu informāciju skatiet sadaļā [Izveidojiet seguma iespējas](hr-benefits-setup-coverage-options.md).
- **Plānu tipi** – iestatiet plānu tipus, kas būs pieejami, kad veidojat atvieglojumu plānu. Plānu tipu piemēri ietver **Zobu**, **Redze** un **Uzkrājumi**. Daži svarīgi plāna tipa iestatījumi nosaka iestatījumus, kas ir pieejami atvieglojumu plānā. Papildu informāciju skatiet sadaļā [Plānu veidu izveide](hr-benefits-setup-plan-types.md).
- **Piemērotības nosacījumi** – piemērotības nosacījumus izmanto, lai noteiktu, vai darbinieks ir piemērots plānam. Vismaz vienam piemērotības nosacījumam jābūt saistītam ar katru atvieglojumu plānu. Papildinformāciju skatiet rakstā [Konfigurēt piemērotības noteikumus un opcijas](hr-benefits-setup-eligibility-rules.md).
- **Maksājumu biežums** – maksājumu biežums ir nepieciešams, konfigurējot atvieglojumu likmes. Kursam izmantotais maksājumu biežums palīdz noteikt summu, ko darbinieks un/vai darba devējs ir parādā katru nedēļu, katru mēnesi vai ik gadu. Papildinformācijai skatiet [Iestatīt maksājumu biežumu](hr-benefits-setup-payment-frequencies.md).
- **Likmes** – likmes definē, cik daudz atvieglojums maksās darbiniekam vai darba devējam. Ja nauda ir jāatdala atpakaļ darbiniekam (piemēram, kredīts uz sporta zāles dalību), tiek ievadīta negatīva likme. Papildinformāciju skatiet sadaļā [Konfigurēt likmes](hr-benefits-setup-rates.md).
- **Pakāpju likmes** - pakāpju likmes tiek izmantotas, kad likmei ir jāmainās, balstoties uz dažiem kritērijiem. Parastākā pakāpju likme ir viena pakāpe, pamatojoties uz vecumu. Tomēr dubulto pakāpju likmes var arī iestatīt, kur likme var tikt mainīta atkarībā no dzimuma, vecuma vai citiem kritērijiem.
- **Ieturējumi** – ieturējumi pamatā ir virsraksta informācija/kodi, kas tiks nodoti algas sistēmai, lai identificētu atvieglojumu atvilkumus. Šie ieturējumi ir jāiestata, jo tie tiks pieprasīti atvieglojumu plānā. Papildinformāciju skatiet sadaļā [Konfigurēt ieturējumus](hr-benefits-setup-deductions.md).
- **Atvieglojumu periodi** – atvieglojumu periods ir periods, kurā darbiniekiem būs atvieglojumu segums. To sauc arī par plāna gadu. Šeit tiek iestatīti arī atvērtie reģistrācijas periodi.

## <a name="set-up-optional-benefit-information"></a>Iestatiet neobligāto atvieglojumu informāciju

Lai izveidotu atvieglojumu plānu, nav jāiestata šādi komponenti:

- **Programmas** – programma ir atvieglojumu kopa, ko nosaka tie paši noteikumi tiesībām tikt izvēlētam. Piemēram, ikviens pārdošanas nodaļā var saņemt mobilo tālruni.
- **Komplekti** – komplekts ir atvieglojumu grupa, kurā pirms opcijas atlasīt papildu plānus ir jāatlasa viens plāns. Piemēram, augstu ieturējumu medicīniskās sistēmas plāns var būt sasaistīts ar veselības uzkrājumu kontu (HSA) plānu.
- **Dzīves notikumu tipi** – dzīves notikumi ir notikumi, kas ļauj mainīt darbinieka segumu. Dzīves notikumu tipi ir saistīti ar plāna tipu. Piemēram, medicīniskā plāna tips var pieļaut izmaiņas plānos dzimšanas vai ģimenes stāvokļa maiņas dēļ vai ģimenes stāvokļa maiņas dēļ. Tomēr apdrošināšanas plāna tips var neatļaus veikt nekādas izmaiņas dzīves notikumu dēļ. Papildinformāciju skatiet sadaļā [Dzīves notikumu tipu konfigurēšana](hr-benefits-setup-life-event-types.md).
- **Gaidīšanas dienas un gaidīšanas periodi** – vajadzību gaidīšanas periodu var iestatīt atvieglojumu plānā. Piemēram, nesen nolīgšanas darbinieks var reģistrēties 401(k) tikai pēc trīs darba mēnešiem. Šajā gadījumā gaidīšanas periods ir trīs mēneši. Gaidīšanas dienas tiek izmantotas gaidīšanas periodā, ja jaunas reģistrācijas var apstrādāt un iesniegt nodrošinātājam tikai noteiktā mēneša dienā. Piemēram, ja 401(k) reģistrāciju var apstrādāt tikai mēneša piecpadsmitajā dienā, pēc trīs nodarbinātības mēnešiem, iestatītais gaidīšanas periods ir trīs mēneši, un gaidīšanas diena ir piecpadsmitā diena. Papildinformāciju skatiet [Gaidīšanas dienu konfigurēšana](hr-benefits-setup-waiting-days.md) un [Gaidīšanas periodu konfigurēšana](hr-benefits-setup-waiting-periods.md).
- **Pamatojuma kodi** – pamatojuma kodi tiek izmantoti, lai skaidrotu, kāpēc atvieglojums varētu tikt mainīts darbiniekam. Plašāku informāciju skatiet tēmā [Iemeslu kodu iestatīšana](hr-benefits-setup-reason-codes.md).

## <a name="set-up-benefit-plans"></a>Iestatīt atvieglojumu plānus

Iestatot atvieglojumu plānu, ir jāveic tālāk norādītās darbības, pirms darbiniekus var reģistrēt:

- Piešķirt atvieglojumu periodu.
- Pievienot vajadzību opcijas.
- Cilnē **Vispārīgi** iestatiet datumu derīgs no un līdz.
- Piešķiriet vismaz vienu piemērotības nosacījumu.
- Iestatiet lauku **Atļaut/turpināt reģistrāciju** cilnē **Iestatījumi**.

Plašāku informāciju par to, kā iestatīt atvieglojumu plānus, skatiet tēmā [Atvieglojumu plānu iestatīšana](hr-benefits-plans-setup.md).

## <a name="set-up-flex-credit-programs-optional"></a>Iestatīt brīvā režīma kredīta programmas (neobligāti)

Varat izmantot brīvā režīma kredīta programmas, lai reģistrētu darbiniekus atvieglojumos atbilstoši iepriekš noteiktam brīvā režīma kredītu skaitam. Darbinieki var izvēlēties, kā sadalīt savus brīvā režīma kredītus. Piemēram, ja darbinieki jau ir segti saskaņā ar viņu dzīvesbiedra veselības apdrošināšanas plānu, viņiem nav jāizmanto kredīti veselības nodrošinājumam. Tāpēc viņi varētu vēlēties tos izmantot citiem atvieglojumiem. Papildinformāciju par brīvā režīma kredīta programmām skatiet sadaļā [Brīvā režīma kredīta programmu iestatīšana](hr-benefits-plans-flex-credit-programs.md).

## <a name="configure-required-employee-information"></a>Konfigurējiet nepieciešamo darbinieka informāciju

Pirms varat reģistrēt darbiniekus atvieglojumos, jānorāda viņiem vajadzīgā informācija. 

Darbiniekam jābūt piešķirtam **amatam**. Amatu **var** piešķirt darbiniekam lapā Darbinieks **vai** **Amats,** atjauninot Darbinieka **piešķiri**. 

Pēc tam darbiniekiem jābūt reģistrētiem fiksētās atlīdzības plānā to sākuma datumā vai jābūt ikgadējā atvieglojumu **algas summai**. Pirms fiksētās atlīdzības **piešķiršanas** darbiniekam ir **jāpiešķir** amats. 

> [!NOTE] 
> Fiksētās **atlīdzības sākuma** datums nedrīkst būt agrāks par pozīcijas **piešķiršanas datumu**.

Vai arī, ja ir darbinieks, kurš saņem papildu atlīdzību kā komisijas, **varat** pievienot darbinieka ieraksta atvieglojumu ikgadējās algas summu. Personāla vadība izmantos atvieglojumu **gada algas summu**, kad tiek noteiktas seguma summas, nevis Fiksētās atlīdzības **gada** summa. Lauks **Atvieglojumi gada algai** ir jābūt derīgam no darbinieka sākuma datuma vai atvieglojumu perioda sākuma, atkarībā no tā, kurš ir vēlāks. Tomēr amatam nav jāpiešķir atvieglojumu gada **alga**. Lai iespējotu **atvieglojumu ikgadējās algas** līdzekli, dodieties uz **lapu Personāla** vadības kopīgie parametri, kas atrodas **cilnē Atvieglojumu** pārvaldība. Šī funkcija pēc noklusējuma ir izslēgta.

> [!IMPORTANT]
> Ja darbiniekam **tiek ievadīta** gan fiksētā **atlīdzība**, gan atvieglojumu gada algas summa, **atvieglojumu** gada alga tiks izmantota, lai noteiktu nodrošinājuma summas. Lapas Darbinieks **sadaļā** Detalizēta informācija par **nodarbinātību** jums ir jāatlasa **vērtība laukā Atvieglojumu algas** biežums.

## <a name="configure-optional-employee-information"></a>Konfigurējiet neobligāto darbinieka informāciju
Kad izveidojat atvieglojumu plānu, kas izmanto likmes, kas balstītas uz dzimumu vai vecumu, jums jāievada darbinieka dzimšanas datums un dzimums, lai aprēķinātu atvieglojumu izmaksas.

## <a name="process-employees-to-determine-eligibility"></a>Apstrādā darbiniekus, lai noteiktu piemērotību
Pirms darbiniekus var reģistrēt plānos, tiesību tikt izvēlētam, lai noteiktu, kuriem plāniem viņi ir piemēroti. Jūs varat skatīt atbilstības procesa rezultātus Procesa rezultātu **skatītājā**. Plašāku informāciju skatiet tēmā [Procesa uzņemšanas atbilstība](hr-benefits-process-enrollment-eligibility.md).

## <a name="employees-select-plans-using-employee-self-service-optional"></a>Darbinieki izvēlas plānus, izmantojot **Darbinieku pašapkalpošanās pakalpojumu** (pēc izvēles)

Kad notiek atvērta reģistrācija, darbinieki tiek nesen nolīgti vai notiek dzīves notikums, darbinieki var atlasīt vai atjaunināt savus atvieglojumus, izmantojot **Darbinieku pašapkalpošanās**. Plašāku informāciju skatiet [Konfigurējiet darbinieku pašapkalpošanos](hr-benefits-setup-employee-self-service.md).

## <a name="confirm-employee-plan-selections"></a>Apstipriniet darbinieka plāna atlases

Darbinieku atlasāmie atvieglojumi ir jāapstiprina, pirms darbinieki tiek uzskatīti par reģistrētiem tiem. Atvieglojumus var atlasīt arī darbinieka vārdā. Lai atlasītu vai apstiprinātu atvieglojumus, lapas **Darbinieks** cilnē **Atvieglojumi** atlasiet **Darbinieka atvieglojumu plāni**. Lai atlasītu vai apstiprinātu atvieglojumus vairākiem darbiniekiem, izmantojiet lapu **Darbinieku atvieglojumu plānu lielapjoma atjaunināšana**.

## <a name="life-event-processing-optional"></a>Dzīves notikumu apstrāde (neobligāti)

Darbinieka dzīves cikla laikā katrs darbinieks var gūt pieredzi dažādos dzīves notikumos, piemēram, laulība, izmaiņas nodarbinātībā vai apgādājamo vai pabalsta saņēmēju izmaiņas. Lai lietotu dzīves notikumus, tie ir jāiespējo lapā **Cilvēkresursu kopīgie parametri**. Iestatiet plānu tipu dzīves notikumu tipus un dzīves notikumu opcijas.

Lai varētu apstrādāt dzīves notikumus, vismaz vienu reizi darbā pieņemšanas laika periodā ir jābūt jau izpildītai atvērtai reģistrācijai. Savienotajās Valstīs atvērta reģistrācija parasti notiek reizi gadā. Ārpus Savienotajām Valstīm atvērtā reģistrācija var notikt darbā pieņemšanas laikā. Dzīves notikumu apstrādē nav nepieciešams, lai darbinieki atlasītu atvieglojumu plānu. Tomēr darbiniekiem jābūt iekļautiem atvērtajā reģistrācijas apstrādē. Papildinformāciju skatiet tālāk norādītajās tēmās.

- [Apstrādāt dzīves notikumus](hr-benefits-process-life-events.md)
- [Apstrādāt dzīves notikumu izmaiņas](hr-benefits-process-life-event-changes.md)
- [Apstrādāt dzīves notikumu piemērotību](hr-benefits-process-life-event-eligibility.md)

## <a name="rate-updates-optional"></a>Likmes atjaunināšana (neobligāti)

Dažkārt atvieglojumu likme plāna periodā mainās. Lai atjauninātu likmes darbiniekiem, kas jau ir reģistrējami sistēmai, jums ir jāapstrādā likmes izmaiņas. Plašāku informāciju skatiet tēmā [Procesu likmju izmaiņas](hr-benefits-process-rate-changes.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
