---
title: Kreditoru maksājumu priekšlikumu automatizēšana
description: Šajā tēmā ir paskaidrots, kā organizācijas, kas maksā kreditoriem periodiskā grafikā, var automatizēt kreditoru maksājumu priekšlikumu ģenerēšanas procesu.
author: kweekley
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 3418021f7b4c693779833e1c3c31501df02a0c21
ms.sourcegitcommit: c5d0bd90334e259e96df17a217b2eff03c265f07
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2020
ms.locfileid: "3423040"
---
# <a name="automate-vendor-payment-proposals"></a>Kreditoru maksājumu priekšlikumu automatizēšana

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Organizācijas, kas maksā kreditoriem periodiskā grafikā, tagad var automatizēt kreditoru maksājumu priekšlikumu ģenerēšanas procesu. Kreditoru maksājumu priekšlikuma automatizācijas definē tālāk mineto informāciju.

- Kad maksājumu priekšlikumi tiek palaisti
- Kādi kritēriji tiek izmantoti, lai atlasītu rēķinus, kas jāapmaksā
- Kādā kreditoru maksājumu žurnālā iegūtie maksājumi tiek saglabāti

Maksājuma priekšlikuma automatizācijas automātiski negrāmato maksājumus. Tāpēc varat turpināt lietot visus apstiprināšanas un darbplūsmas procesus, ko pašlaik izmantojat, lai apstiprinātu izveidotos maksājumus.

## <a name="define-the-occurrence-of-vendor-payment-proposals"></a>Kreditoru maksājumu priekšlikumu rašanās definēšana

Kreditora maksājuma priekšlikuma automatizācijas izmanto procesu automatizācijas struktūru. Dažādi biznesa procesi izmanto šo struktūru, lai definētu atlasītā procesa atkārtošanos. Kreditoru maksājumu priekšlikumiem automatizācija var piekļūt **Kreditori \> Maksājumu iestatīšana \> Procesa automatizācija**.

Vispirms izmantojiet automatizācijas opciju **Izveidot jaunu procesu** un atlasiet **Kreditora maksājuma priekšlikums**. Pēc tam vednis palīdz iestatīt kreditora maksājuma priekšlikumu.

## <a name="general-page"></a>Vispārīgā lapa

Vedņa lapā **Vispārīgi** ievadiet kreditora maksājuma priekšlikuma nosaukumu, kuru veidojat. Piemēram, ja maksājat visiem vietējiem kreditoriem ar čeku pirmdienā, ievadiet aprakstošu nosaukumu, piemēram, **Iekšzemes\_Čeks**. Ievadītais nosaukums tiek norādīts procesa automatizācijas nedēļas skatījuma darbvietā **Kreditoru maksājumi**.

Pēc tam definējiet izveidotā maksājumu žurnāla īpašnieku. Īpašnieks parasti ir kreditoru (AP) maksājumu darbinieks, kurš ir atbildīgs par maksājumu žurnālu pēc tā izveidošanas.

Pārējie iestatījumi lapā ir vispārēji un tiek izmantoti, lai definētu gadījumu modeli šai kreditora maksājuma priekšlikuma versijai. Piemēram, ja notikums ir čeka maksājums pirmdienā, varat to definēt, lai tas darbotos katru nedēļu, un jūs varat izvēlēties pirmdienu kā nedēļas dienu, kad tā darbojas. Varat ievadīt arī sākotnējo grafika laiku, piemēram, 2:00 AM, tā, lai procesa automatizācija tiktu pabeigta pirms nākamās darba dienas sākuma.

Ir svarīgi, lai jūs saprastu, ka lietojat vedni, lai definētu, kad tiek apstrādāts kreditora maksājuma priekšlikums. Jūs nedefinējat, kad kreditoru maksājumi tiek ģenerēti, izdrukāti un grāmatoti. Nedēļas skatā procesu automatizācija kreditoru maksājumu priekšlikumiem parādīsies dienās, kas atlasītas atkārtošanās modelī.

Papildinformāciju par citiem laukiem lapā **Vispārīgi** skatiet procesa automatizācijas dokumentācijā.

## <a name="vendor-payment-proposal-page"></a>Kreditora maksājumu priekšlikumu lapa

Nākamā vedņa lapa ir lapa **Kreditora maksājuma priekšlikums**. Tā tiek izmantot, lai definētu kritērijus to kreditoru rēķinu atlasīšanai, kuri jāapmaksā. Parasti tās pašas opcijas ir atrodamas maksājumu priekšlikumā kreditoru maksājumu žurnālā. Taču ir daži izņēmumi. Piemēram, visiem šīs lapas datumiem jābūt definētiem kā relatīviem datumiem, jo maksājuma priekšlikuma datums mainās katru reizi, kad priekšlikums tiek palaists.

### <a name="journal-name"></a>Žurnāla nosaukums

Lauks **Žurnāla nosaukums** nosaka žurnāla nosaukumu, kuru tiek veidoti kreditoru maksājumi. Kreditora maksājuma priekšlikuma rezultātu automatizācija radīs maksājumus definētajā žurnālā, bet žurnāls netiek grāmatots.

### <a name="from-date-and-to-date"></a>Sākuma datums/beigu datums

Tā vietā, lai definētu sākuma datumu un beigu datumu, lai atlasītu rēķinus, pamatojoties uz apmaksas datumu vai termiņatlaides datumu, jāizmanto opcija **Definēt beigu datuma kritērijus** un lauks **Dienu skaita korekcija beigu datumam**, lai definētu beigu datumu. Maksājuma priekšlikuma automatizācijā nav norādīts sākuma datuma jēdziena.

Pēc noklusējuma opcija **Definēt kā datuma kritēriju** ir iestatīta uz **Nē**. Ja izmantojat šo noklusējuma vērtību, process atlasa visus maksājumu rēķinus, kad process tiek palaists, jo nav definēts beigu datums.

Ja iestatāt opciju **Definēt beigu datuma kritērijus** uz **Jā**, izmantojiet lauku **Koriģēto dienu skaitu līdz beigu datumam**, lai definētu datumu, kad rēķini tiek atlasīti kā norādītais dienu skaits pirms vai pēc procesa palaišanas. Skaitlis var būt pozitīvs, negatīvs vai 0 (nulle). Pēc tam sistēma apmaksās rēķinus, kuros apmaksas datumi vai termiņatlaides datumi ir norādītais dienu skaits pirms vai pēc procesa palaišanas. Piemēram, visiem rēķiniem, kas apmaksājami piektdienā vai pirms piektdienas, maksājumu sērija izveido maksājumus visiem kreditoriem pēc pārbaudes trešdienā. Šajā gadījumā iestatiet lauku **Dienu skaita pielāgojums beigu datumam** uz **2**. Ja maksājuma priekšlikuma notikšana tiek izpildīta trešdien, 25. martā, maksājumam tiks atlasīti visi rēķini, kam ir izpildes datums vai termiņatlaides datums ir 27. marts vai agrāk.

### <a name="minimum-payment-date"></a>Agrākais maksājuma datums

Agrākais maksājuma datums definē agrāko datumu, kas tiek izmantots, izveidojot maksājumus. Vispirms ir jāiestata opcija **Definēt agrākā maksājuma datuma kritēriju** uz **Jā**. Šis iestatījums ļauj izmantot agrākā maksājuma datuma funkcionalitāti. Ja šī opcija ir iestatīta uz **Jā**, izmantojiet lauku **Dienu skaita pielāgojums agrākajam maksājuma datumam**, lai definētu agrāko maksājuma datumu kā konkrētu dienu skaitu pirms vai pēc procesa palaišanas. Skaitlis var būt pozitīvs, negatīvs vai 0 (nulle). Piemēram, maksājumu sērija ģenerē maksājumus trešdien, lai iekļautu visus maksājumus, kuru agrākais maksājuma datums ir pirms iepriekšējās pirmdienas. Šajā gadījumā iestatiet lauku **Dienu skaita pielāgojums agrākajam maksājuma datumam** uz **-2**.

Tālāk ir minēts piemērs, kas parāda, kā kopīgi darbojas lauki "beigu datums" un agrākais maksājuma datums. Maksājuma priekšlikuma automatizācija ir iestatīta izpildei trešdienā. Lauks **Dienu skaita pielāgojums beigu datumam** ir iestatīts uz **1**, lai definētu beigu datumu, pamatojoties uz izpildes datumu. Lauks **Dienu skaita pielāgojums agrākajam maksājuma datumam** ir iestatīts uz **-2**. Ja maksājumu procesa automatizācija sākas trešdien, 25. martā, visi rēķini, kas apmaksājami 26. martā vai pēc tam, tiks iekļauti maksājuma priekšlikumā. Maksājumu priekšlikumi tiks ģenerēti tālāk minētajā veidā.

- Visiem rēķiniem, kuru apmaksas termiņš ir 23. marts vai agrāk, apmaksas datums būs 23. marts.
- Rēķiniem, kuru apmaksas termiņš ir 24. marts vai agrāk, apmaksas datums būs 24. marts.
- Rēķiniem, kuru apmaksas termiņš ir 25. marts vai agrāk, apmaksas datums būs 25. marts.
- Rēķiniem, kuru apmaksas termiņš ir 26. marts vai agrāk, apmaksas datums būs 26. marts.

### <a name="summarized-payment-date"></a>Apkopotā maksājuma datums

Apkopotā maksājuma datumu izmanto tikai tad, ja lauks **Periods** ir iestatīts uz **Kopsumma** rēķinu apmaksas metodei. Ja lauks **Periods** ir iestatīts uz **Kopsumma** jūsu maksājuma metodēm, opcija **Definēt apkopotu maksājuma datuma kritēriju** ir jāiestata uz **Jā**. Ja šī opcija ir iestatīta uz **Jā**, izmantojiet lauku **Dienu skaita pielāgojums apkopotam maksājuma datumam**, lai definētu apkopotu maksājuma datumu kā konkrētu dienu skaitu pirms vai pēc procesa palaišanas. Skaitlis var būt pozitīvs, negatīvs vai 0 (nulle). Piemēram, sērija ģenerē maksājumus trešdien, un uzņēmums vēlas izveidot apkopotu maksājumu trešdien. Šajā gadījumā iestatiet lauku **Dienu skaita pielāgojums apkopotam maksājuma datumam** uz **0**.

### <a name="records-to-include"></a>Iekļaujamie ieraksti

Maksājuma priekšlikumjoprojām var definēt filtra opcijas. Ja filtrs ir definēts, filtra kritēriji netiek parādīti vedņa lapā. Taču tos var skatīt, atkārtoti atverot filtru.

Atlikušie priekšlikuma lauki darbojas tieši tāpat, kā tie darbojas maksājuma priekšlikumam kreditoru maksājumu žurnālā. Informāciju par citiem laukiem skatiet [Kreditoru maksājumu izveide, izmantojot maksājuma priekšlikumu](create-vendor-payments-payment-proposal.md).

> [!NOTE]
> Daži valstij/reģionam specifiski lauki un daži sabiedriskā sektora lauki vēl nav pieejami kreditora maksājuma priekšlikuma automatizācijā.

Iesakām novērtēt, vai automatizācija būs izdevīga jūsu organizācijai, pamatojoties uz jūsu prasībām.

## <a name="view-the-results-of-a-vendor-payment-proposal-automation"></a>Kreditora maksājumu priekšlikuma automatizācijas rezultātu skatīšana

Pēc kreditora maksājuma priekšlikuma automatizācijas sērijas izveidošanas katra maksājuma notikumi tiek parādīti procesa automatizācijas nedēļas skatā. Kreditoru maksājumiem tiek pievienots procesu automatizācijas iknedēļas skats darbvietai **Kreditoru maksājumi** un lapai **Procesu automatizācija**.

[![Automatizācijas nedēļas skatu apstrāde kreditoru maksājumu darbvietā](./media/vendor-payment-proposal-1.png)](./media/vendor-payment-proposal-1.png)

Procesa automatizācijas nedēļas skats darbvietā **Kreditoru maksājumi** rāda tikai kreditoru maksājumu priekšlikumu automatizācijas. Tas parāda visus maksājumu gadījumus pašreizējai nedēļai par visām juridiskajām personām, kurām lietotājam, kurš ir pierakstījies, ir drošības atļaujas. Piemēram, ja kreditoru maksājumu darbinieks ir atbildīgs par maksājumiem USMF un USSI uzņēmumos, viņš redzēs kreditora maksājuma priekšlikuma automatizāciju šiem diviem uzņēmumiem, bet ne citiem uzņēmumiem.

[![Procesu automatizācijas nedēļas skats USMF un USSI uzņēmumiem](./media/vendor-payment-proposal-2.png)](./media/vendor-payment-proposal-2.png)

Katrs gadījums rāda uzņēmumu, kuram tika vai tiks izveidots maksājumu žurnāls. Ja maksājumi tiek veidoti, izmantojot centralizētus maksājumus, uzņēmums, kas tiek norādīts, ir uzņēmums, kurā tiks izveidoti maksājumi. Notikums ne vienmēr parāda, kuri uzņēmuma rēķini tiks apmaksāti.

Tiek rādīta arī katra gadījuma nosaukums, lai palīdzētu noteikt maksājuma priekšlikumu.

Turklāt tiek rādīts katra gadījuma statuss. Izmanto šādus statusus:

- **Ieplānots** — maksājuma priekšlikums ir ieplānots, bet tas vēl nav palaists.
- **Kļūda** — maksājuma priekšlikums ir palaists, bet radās kļūda. Varat apskatīt kļūdas, atlasot pogu **Skatīt rezultātus**.
- **Pabeigts** — maksājuma priekšlikums ir veiksmīgi palaists. Varat apskatīt maksājumus, atlasot saiti **Skatīt maksājumus**. Šī saite atver maksājumu žurnālu, ko izveidoja gadījumi.

Kad maksājumi ir izveidoti, varar skatīt maksājumu summas žurnālā. Summas ir norādītas uzņēmuma transakcijas valūtās. Piemēram, ja maksājumu žurnālā ir maksājumi gan ASV dolāros, gan Kanādas dolāros, tiek parādīti kopējie maksājumi katrai valūtai. 

Maksājumu žurnālu var dzēst pēc tam, kad tas ir izveidots, izmantojot procesu automatizāciju. Ja maksājums ir pilnībā dzēsts, notiek tālāk minētie notikumi.

- Procesa automatizācijas statuss nedēļai paliek **Pabeigts**.
- Process noņem maksājuma kopsummu, un saite **Skatīt maksājumus** tiek aizstāta ar pogu **Skatīt rezultātus**.
- Skatot rezultātus, jūs saņemat ziņojumu, kurā teikts, ka sākotnējais žurnāls ir dzēsts.

Pēc maksājuma dzēšanas rēķini tiks atkal atvērti maksājumam. Pēc tam var izveidot jaunu gadījumu, lai apmaksātu rēķinus vēlreiz.

## <a name="edit-a-vendor-payment-proposal-automation"></a>Kreditoru maksājumu priekšlikuma automatizēšanas rediģēšana

Procesu automatizācijas struktūra ļauj rediģēt maksājumus, sērijas un gadījumus, kas izveidoti maksājuma priekšlikumam. Sērijas var rediģēt lapā **Procesa automatizācija** vai arī procesu automatizācijas nedēļas skatā. Piemēram, ja kreditoru vadītājs nolemj ģenerēt visas iekšzemes kreditoru pārbaudes trešdien, nevis pirmdien, viņš var atrast notikumu nedēļas skatā un izvēlēties **Skatīt/rediģēt – sērijas**. Ja rediģējat sērijas, sistēma prasa norādīt, vai jāveic izmaiņas visiem esošajiem atkārtojumiem vai tikai jauniem atkārtojumiem. Vēsturiski notikumi, kam jau ir statuss **Pabeigts** vai kas beidzās statusā **Kļūda**, netiks mainīti.

Varat arī pievienot jaunu gadījumu vai mainīt esošu gadījumu. Piemēram, nākamā maksājuma priekšlikuma notikumu ir plānots palaist trešdien, 1. janvārī, bet šis datums ir brīvdiena. Varat mainīt notikumu procesu automatizācijas nedēļas skatā vai lapā **Procesa automatizācija**. Tiek atvērta lapa, kurā parādītas grafika detaļas un maksājuma priekšlikuma kritēriji. Šeit varat labot ieplānoto laiku un datumu. Varat arī rediģēt maksājuma priekšlikuma kritērijus, ja ir nepieciešamas izmaiņas. Piemēram, ja maināt ieplānoto maksājuma gadījuma datumu no 1. janvāra uz 2. janvāri, iespējams, būs jāmaina arī beigu datuma relatīvie datumi.

Varat arī deaktivizēt notikumu vai sēriju. Lai deaktivizētu gadījumu un apturētu tā apstrādi, atlasiet to procesa automatizācijas nedēļas skatā un pēc tam atlasiet opciju **Atspējot**. Varat atspējot sēriju lapā **Procesu automatizācija**.

## <a name="security-for-payment-proposal-automations"></a>Maksājumu priekšlikuma automatizēšanas drošība

Tālāk norādītie nodokļi un privilēģijas ir pievienoti kreditora maksājuma priekšlikuma automatizācijai. Šie pienākumi un privilēģijas ir noklusējuma drošības iestatījumi, bet tos var mainīt, pamatojoties uz jūsu organizācijas prasībām. Piemēram, ja ne tikai AP pārvaldnieks, bet arī AP maksājumu darbinieks var rediģēt un izveidot grafika atkārtošanos, piešķir pienākumu **Uzturēt paredzēto atkārtošanos** personai, kas ir atbildīga par AP maksājuma darbinieka lomu.

| Nodoklis                              | Loma                                                                       | Privilēģijas |
|-----------------------------------|----------------------------------------------------------------------------|------------|
| Grafiku sēriju uzturēšana          | Kreditoriem maksājamo parādu vadītājs                                                   | Šis pienākums piešķir tiesības izveidot un uzturēt maksājuma priekšlikuma automatizācijas sērijas un gadījumus, izmantojot tālāk minētās privilēģijas.<ul><li>Grafika atkārtojumu uzturēšana</li><li>Grafiku sēriju uzturēšana</li><li>ProcessScheduleOccurrenceListMaintain</li><li>Gadījumu nedēļas skata skatīšana</li></ul> |
| Grafika atkārtojumu izskatīšana | Kreditoru maksājumu darbinieks, kreditoru centralizēto maksājumu darbinieks | Šis pienākums piešķir tiesības skatīt maksājuma priekšlikuma automatizācijas sērijas un gadījumus, izmantojot tālāk minētās privilēģijas.<ul><li>Grafika atkārtojumu skatīšana</li><li>Gadījumu nedēļas skata skatīšana</li></ul> |
| Uzziņas par grafika sērijām      | None                                                                       | Šis pienākums piešķir tiesības skatīt sēriju iestatījumus un gadījumus, izmantojot tālāk minētās privilēģijas.<ul><li>Grafika atkārtojumu skatīšana</li><li>Gadījumu saraksta lapas skatīšana</li><li>Gadījumu nedēļas skata skatīšana</li></ul>|
| Grafika atkārtojumu uzturēšana     | None                                                                       | Šis pienākums piešķir tiesības izveidot un uzturēt gadījumus, izmantojot tālāk minētās privilēģijas.<ul><li>Grafika atkārtojumu uzturēšana</li><li>Gadījumu nedēļas skata skatīšana</li></ul> |
