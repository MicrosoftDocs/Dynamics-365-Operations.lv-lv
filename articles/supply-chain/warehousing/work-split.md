---
title: Darba sadale
description: Šajā tēmā ir sniegta informācija par darba sadales funkcionalitāti. Šī funkcionalitāte ļauj sadalīt lielus darba pasūtījumus vairākos mazākos darba pasūtījumos, kurus pēc tam var piešķirt vairākiem noliktavas darbiniekiem. Tādējādi vienu un to pašu darbu var vienlaikus paņemt vairāki noliktavas darbinieki.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8a530f3887c3c66295177d480a8c486dd0984153
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965531"
---
# <a name="work-split"></a>Darba sadale

Darba sadales funkcionalitāte ļauj sadalīt lielus darba ID (proti, darba pasūtījumus, kuriem ir vairākas rindas) vairākos mazākos darba ID, kurus pēc tam var piešķirt vairākiem noliktavas darbiniekiem. Tādējādi vienu un to pašu darba izveides numuru var vienlaikus paņemt vairāki noliktavas darbinieki.

> [!IMPORTANT]
> Varat sadalīt tikai tādus darba pasūtījumus, kuru statuss ir *Atvērts* vai *Nepabeigts*.

## <a name="turn-on-the-work-split-functionality"></a>Darba sadales funkcionalitātes ieslēgšana

Lai varētu izmantot darba sadales funkcionalitātiu, sistēmā ir jāieslēdz līdzeklis un tā priekšnosacījuma līdzeklis. Administratori var izmantot [līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļu statusu un tos ieslēgtu pēc vajadzības.

Vispirms ieslēdziet priekšnosacījuma *Organizācijas mēroga darba aizturēšana* līdzekli, ja tas vēl nav ieslēgts. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Organizācijas līmeņa darba aizturēšana*

> [!NOTE]
> Kad šis līdzeklis ir aktivizēts, datu jaunināšana tiek automātiski piemērota pēc tam, kad līdzeklis ir ieslēgts visām juridiskajām personām.

Pēc tam ieslēdziet līdzeli *Darba sadale*, kas ir norādīts tālāk norādītajā veidā.

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Darba sadale*

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a>Darba detalizētas informācijas un Visi darbi lapu uzlabojumi

*Darba sadales* līdzeklis pievieno tālāk minētās divas pogas cilnei **Darbs**, kas atrodas darbības rūtī **Darba detalizēta informācija** un lapās **Visi darbi**.

- **Sadalīt darbu** – sadala pašreizējā darba ID vairākos mazākos darba ID, kurus var apstrādāt atsevišķi darbinieki.
- **Atcelt darba sadales sesiju** — atceļ darba sadales sesiju un padara darbu pieejamu apstrādei.

![Pogas Darba sadale un Atcelt darba sadales sesiju](media/Work_split_buttons.png "Pogas Darba sadale un Atcelt darba sadales sesiju")

> [!IMPORTANT]
> Poga **Darba sadale** nav pieejama, ja ir izpildīts kāds no tālāk minētajiem nosacījumiem.
>
> - Darba statuss ir cits, nevis *Atvērts* vai *Nepabeigts*.
> - Konteinera ID ir saistīts ar darba ID. (Konteineru nevar sistemātiski sadalīt, jo tam ir nepieciešamas fiziskas darbības.)
> - Darbs ir saistīts ar klasteri.
> - Darba pasūtījuma veids ir cits, nevis viens no tālāk minētajiem veidiem.
>
>    - Pārdošanas pasūtījumi
>    - Izejmateriālu izdošana
>    - Pārsūtīt izejas plūsmu
>
> - Pašlaik darbu sadala cits lietotājs. Ja mēģināt atvērt sadalīšanas lapu darbam, ko jau ir sadalījis cits lietotājs, tiek parādīts šāds kļūdas ziņojums: "Darbs ar ID \#\#\#\# pašlaik tiek sadalīts. Pēc dažām minūtēm mēģiniet vēlreiz. Ja turpināt saņemt šādu paziņojumu, sazinieties ar vadītāju."

Jauns darba aizturēšanas iemesls *Sadalīt darbu* norāda, kad darba ID atrodas sadalīšanas procesā. Tas ir redzams gan lapā **Sadalīt darbu** lapā, gan noliktavas programmā, ja lietotājs mēģina palaist darbu. Ja tiek izmantoti aizturēšanas iemesli, lauka nosaukums **Aizturēts kopums** no darba ID tiek mainīts uz **Aizturēts**.

## <a name="initiate-a-work-split"></a>Sākt darba sadali

Līdzeklis pievieno jaunu **Darba sadales** lapu, kas ļauj lietotājiem sadalīt darba rindas no darba ID. Kad lapa tiek atvērta pirmo reizi, tā parāda rindas, kuru darba statuss ir *Atvērts* un kuras ir pieejamas sadalei. Darbības rūtī atlasiet **Sadalīt darbu**, lai apstrādātu atlasīto darbu.

Lai sadalītu darbu, veiciet tālāk norādītās darbības.

1. Atveriet kādu no tālāk minētajām darba lapām.

    - **Darba informācija** (**Noliktavas pārvaldība \> Darbs \> Darba informācija**)
    - **Viss darbs** (**Noliktavas pārvaldība \> Darbs \> Viss darbs**)

1. Režģī atlasiet darba ID, kuru sadalīt. Laukam **Darba pasūtījuma veids** jābūt iestatītam uz vienu no tālāk minētajām vērtībām.

    - Pārdošanas pasūtījumi
    - Izejmateriālu izdošana
    - Pārsūtīt izejas plūsmu

1. Darbību rūts cilnē **Darbs** grupā **Darbs** atlasiet **Sadalīt darbu**.

    Tiek parādīta lapa **Sadalīt darbu** un parādītas darba rindas, kas ir atvērtas un pieejamas sadalīšanai. Pēc noklusējuma tiek parādītas tikai pieejamās darba rindas. Lai skatītu visas darba ID rindas (piemēram, rindas ar darba veidu *Izvietot*), virs režģa atzīmējiet izvēles rūtiņu **Rādīt visas rindas**.

    Tiek parādīts šāds paziņojums: "Lietotāji nevar apstrādāt darba rindas, līdz pabeidzat sadalīšanu un aizverat šo lapu."

    Lauks pašreizējam darbam **Darba aizturēšanas iemesls** tiks iestatīts uz *Sadalīt darbu*, un darbs tiks aizturēts.

    ![Aizturēšanas iemesls](media/Blocking_reason.png "Aizturēšanas iemesls")

1. Atlasiet rindas, kas jānoņem no pašreizējā darba ID un jāpievieno jaunā darba ID. Notiek tālāk aprakstītie notikumi:

    - Kad sadalāt darbu, atlasītā rinda vai rindas no sākotnējā darba ID tiek atceltas un pēc tam kopētas jaunā darba ID.
    - Esošā darba veidnes struktūra un izvietojuma atrašanās vieta (un arī turpmākie izdošanas/izvietošanas pāri) tiek saglabāti. Tālāk minēto darba ID lauku vērtības tiek kopētas no oriģinālā darba uz jauno darbu.

        - Kravas ID
        - Sūtījuma ID
        - Darba pasūtījuma veids
        - Pasūtījuma numurs
        - Vieta
        - Noliktava
        - Darba prioritāte
        - Darbu pūla ID
        - Kopuma ID
        - Darba izveides numurs

    - Tālāk minētie lauki netiek iekopēti jaunajā darba ID.

        - **Darba ID** — no attiecīgās numuru secības tiek ģenerēts jauns darba ID.
        - **Darba statuss** — šis lauks ir iestatīts uz *Atvērts*.
        - **Aizturējis** — šis lauks sākotnēji ir iestatīts uz tukšu.
        - **Mērķa numura zīmes ID** — šis lauks tiek atstāts tukšs.
        - **Izveides datums un laiks** — šis lauks tiek iestatīts uz pašreizējo datumu un laiku.
        - **Aizturēts kopums/iesaldēts** — šis lauks tiek pārrakstīts oriģinālajam darba ID un jaunajam darba ID.

1. Darbību rūtī atlasiet **Sadalīt darbu**.

Kamēr darbs tiek sadalīts, tiek parādīts šāds paziņojums: "Darbības apstrāde — sadalīt darbu". Kamēr šis ziņojums ir redzams, varat atcelt operāciju, ziņojuma lodziņā atlasot **Atcelt**.

Ja izvēles rūtiņa **Rādīt visas rindas** ir notīrīta, rinda, kas tika nodalīta un atcelta, režģī vairs netiks rādīta. Ja izvēles rūtiņa ir atzīmēta, jums būtu jāredz, ka šīs rindas vērtība **Darba statuss** ir mainīta uz *Atcelts*.

Tiek norādīts tālāk redzamais paziņojums, kas norāda, ka jaunais darba ID ir izveidots: "Darbs \#\#\#\# ir izveidots, nodalot no sākotnējā darba \#\#\#\# ."

Citas darba rindas no sākotnējā darba ID (piemēram, *Izvietošanas* rindas) tiks koriģētas pēc nepieciešamības, lai atspoguļotu tās darba rindas, kas ir atceltas. Piemēram, ja oriģinālajam darba ID bija 15 rindu skaits *Nodot* un *Izdošanas* rindas ar kopējo daudzumu 10 tika atceltas, jaunais *Nodot* krājumu daudzums oriģinālajā darba ID tagad būs 5.

Jaunais darbs netiks nekavējoties piešķirts nevienam lietotājam. Tomēr pēc nepieciešamības varat to piešķirt lietotājam, izmantojot lapas **Darba informācija** standarta funkcionalitāti.

> [!IMPORTANT]
> Varat sadalīt tikai tādus darba ID, kas satur divas vai vairākas pieejamās darba rindas. Ja atlasāt **Sadalīt darbu**, kurā ir tikai viena darba rinda, tiek parādīts šāds kļūdas ziņojums: "Vismaz vienai darba rindai ir jāpaliek sākotnējā darbā." Šādā gadījumā sadalīšana netiks veikta.

## <a name="finish-a-work-split"></a>Pabeigt darba sadali

Lai pabeigtu darba sadali, ir jānoņem *Sadalīt darbu* aizturēšanas iemesls. Šo darbību var paveikt divos veidos.

- Lietotājs, kurš sadala darbu, aizver lapu **Sadalīt darbu**, augšējā labajā stūrī atlasot pogu **Aizvērt** (**X**). Kad lapa tiek aizvērta, *Sadalīt darbu* aizturēšanas iemesls tiks noņemts. Šā darba stāvoklis *Aizturēts* tiks pārrēķināts, un, ja šim darbam nav neviena aizturēšanas iemesla, darbs tiks atjaunots.
- Katrs lietotājs atver darba ID un darbību rūtī atlasa pogu **Atcelt darba sadales sesiju**. *Sadalīt darbu* aizturēšanas iemesls tiks noņemts, un šā darba *Aizturēts* stāvoklis tiks pārrēķināts tāpat kā tad, kad lapa **Sadalīt darbu** tiek aizvērta.

Kad *Sadalīt darbu* aizturēšanas iemesls ir noņemts, darbu var palaist mobilajā ierīcē, ar nosacījumu, ka stāvoklis **Aizturēts** darba ID ir iestatīts uz *Nē*.

## <a name="user-blocking-on-the-warehouse-app"></a>Lietotāja aizturēšana noliktavas programmā

Ja mēģināt izmantot noliktavas programmu, lai palaistu saņemšanas darbu darba ID, kas jau ir sadalīts, saņemsit šādu kļūdas ziņojumu: "Darbs ar ID \#\#\#\# pašlaik tiek sadalīts." Ja saņemat šo ziņojumu, atlasiet **Atcelt**. Pēc tam varat turpināt apstrādāt citu darbu.

## <a name="other-blocked-operations"></a>Citas aizturētās operācijas

Visas operācijas, kas pārveido darba rindas, darba krājumu darbības vai papildināšanas saites, kas saistītas ar sadalāmo darbu, neizdosies, un tiks parādīts šāds kļūdas ziņojums: "Darbs ar ID \#\#\#\# pašlaik tiek sadalīts."


[!INCLUDE[footer-include](../../includes/footer-banner.md)]