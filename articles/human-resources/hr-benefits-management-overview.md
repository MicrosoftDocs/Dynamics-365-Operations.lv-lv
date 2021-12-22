---
title: Atvieglojumu pārvaldības pārskats
description: Šajā tēmā ir sniegts apskats par Atvieglojumu pārvaldības līdzekli programmā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc06fd2ef4992b4ef2e20ace4f5c6bcc0bffb9d2
ms.sourcegitcommit: e06b7d4de6d5ee7ae491d437d6c0365608a5380b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2021
ms.locfileid: "7892506"
---
# <a name="benefits-management-overview"></a>Atvieglojumu pārvaldības pārskats

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

Šī tēma apraksta, kā ieslēgt Human Resources priekšskatījuma līdzekļus. Tajā arī norādīts, kādus pastāvošos Human Resources līdzekļus aizstāj šī Atvieglojumu pārvaldība, vai kādi līdzekļi tiek atspējoti, ieslēdzot atvieglojumu pārvaldību.

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

Darbiniekam ir jābūt **piešķirtam** amatam. **Amatu** darbiniekam var piešķirt **lapās Darbinieks** vai **Amats**, atjauninot darbinieka **piešķiri**. 

Pēc tam darbiniekiem ir jābūt reģistrētiem fiksētas atlīdzības plānā sākuma datumā vai arī viņiem ir jābūt **gada pabalstu algas** summai. Pirms fiksētas atlīdzības piešķiršanas **darbiniekam ir jāpiešķir** **amats**. 

> [!NOTE] 
> **Fiksētās atlīdzības sākuma datums** nevar būt pirms pozīcijas piešķiršanas **datuma**.

Vai arī, ja jums ir darbinieks, kurš saņem papildu atlīdzību, piemēram, komisijas, varat pievienot **Pabalstu gada algas summu no darbinieka** ieraksta. Cilvēkresursi **izmantos Pabalstu gada algas** summu, nosakot seguma summas, nevis **fiksētās kompensācijas gada** summu. Lauks **Atvieglojumi gada algai** ir jābūt derīgam no darbinieka sākuma datuma vai atvieglojumu perioda sākuma, atkarībā no tā, kurš ir vēlāks. Tomēr amats nav nepieciešams, lai piešķirtu **Pabalstu gada algu**. Lai iespējotu **pabalstu gada algas** funkciju, dodieties **uz lapu Personāla vadības koplietojamie parametri** cilnē Priekšrocību **pārvaldība**. Šis līdzeklis pēc noklusējuma ir izslēgts.

> [!IMPORTANT]
> Ja darbiniekam tiek ievadīta gan **fiksētā** atlīdzība, gan **Pabalstu gada algas** summa, pabalstu gada alga **tiks izmantota seguma summu** noteikšanai. Lapas **Darbinieka sadaļā Detalizēta informācija par nodarbinātību** **ir** jāatlasa vērtība **laukā Atvieglojumu apmaksas** biežums.

## <a name="configure-optional-employee-information"></a>Konfigurējiet neobligāto darbinieka informāciju
Kad izveidojat atvieglojumu plānu, kas izmanto likmes, kas balstītas uz dzimumu vai vecumu, jums jāievada darbinieka dzimšanas datums un dzimums, lai aprēķinātu atvieglojumu izmaksas.

## <a name="process-employees-to-determine-eligibility"></a>Apstrādā darbiniekus, lai noteiktu piemērotību
Pirms darbiniekus var reģistrēt plānos, tiesību tikt izvēlētam, lai noteiktu, kuriem plāniem viņi ir piemēroti. Atbilstības procesa rezultātus var skatīt **procesu rezultātu skatītājā**. Plašāku informāciju skatiet tēmā [Procesa uzņemšanas atbilstība](hr-benefits-process-enrollment-eligibility.md).

## <a name="employees-select-plans-using-employee-self-service-optional"></a>Darbinieki atlasa plānus, izmantojot **darbinieku pašapkalpošanos** (neobligāti)

Kad notiek atvērta reģistrācija, darbinieki tiek tikko pieņemti darbā vai notiek dzīves notikums, darbinieki var atlasīt vai atjaunināt savas priekšrocības, izmantojot **darbinieka pašapkalpošanos**. Plašāku informāciju skatiet [Konfigurējiet darbinieku pašapkalpošanos](hr-benefits-setup-employee-self-service.md).

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
