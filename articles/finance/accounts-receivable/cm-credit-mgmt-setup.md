---
title: Kredīta pārvaldības parametru iestatīšana
description: Šajā rakstā aprakstītas opcijas, kuras var lietot, lai konfigurētu Kredīta pārvaldību atbilstoši jūsu uzņēmuma prasībām.
author: JodiChristiansen
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8955518e7b5c0200d3827c1c22b7d150a09be244
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799550"
---
# <a name="credit-management-parameters-setup"></a>Kredīta pārvaldības parametru iestatīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā aprakstītas opcijas, kuras var lietot, lai konfigurētu Kredīta pārvaldību atbilstoši jūsu uzņēmuma prasībām. Lai sāktu izmantot kredīta pārvaldības līdzekļus, iestatiet parametrus lapā **Kredīta un iekasēšanas parametri** (**Kredīts un iekasēšana \> Iestatījumi \> Kredīta un iekasēšanas parametri**).

## <a name="credit-parameters"></a>Kredīta parametri

Sadaļā **Kredīts** ir četras kopsavilkuma cilnes, kurās varat mainīt parametrus, kas kontrolē kredīta pārvaldību: **Kredīta aizturēšanas gadījumi**, **Kredīta pārvaldības kontrolpunkts**, **Kredīta pārvaldības statistika** un **Kredīta limiti**. Tālāk esošajās sadaļās aprakstīti iestatījumi, kas ir pieejami katrā kopsavilkuma cilnē.

### <a name="credit-holds"></a>Kredītu aiztures

- Iestatiet opciju **Atļaut rediģēt pārdošanas pasūtījumus pēc pasūtījuma aizturēšanas palaišanas** uz **Nē**, lai pieprasītu, ka grāmatošanas kārtulas atkal tiek pārbaudīti, ja pārdošanas pasūtījuma vērtība (pilna cena) ir palielināta kopš pārdošanas pasūtījuma palaišanas no aizturēšanas saraksta.
- Laukā **Atcelto pasūtījumu iemesli** atlasiet palaišanas iemeslu, kas tiks izmantots pēc noklusējuma, kad pārdošanas pasūtījums, kas bija kredīta pārvaldības aizturēšanā, tiks atcelts.
- Lai pārbaudītu debitora kredīta grupas kredīta limitu, kad pārdošanas pasūtījuma debitors pieder debitoru kredīta grupai, iestatiet opciju **Pārbaudīt debitora kredīta grupas kredīta līmeni** uz **Jā**. Tiek pārbaudīts grupas kredīta limits un pēc tam, ja tas ir pietiekams, tiks pārbaudīts debitora kredīta limits.
- Iestatiet opciju **Pārbaudīt kredīta limitu, kad ir palielināti apmaksas nosacījumi** uz **Jā**, lai pārbaudītu apmaksas nosacījumu klasifikāciju, lai noteiktu, vai maksājuma nosacījumi pārdošanas pasūtījumā atšķiras no noklusējuma apmaksas nosacījumiem klientiem. Ja jaunajiem apmaksas nosacījumiem ir augstāks rangs nekā sākotnējiem apmaksas nosacījumiem, pasūtījums tiek nodots kredīta pārvaldības aizturēšanai.
- Iestatiet opciju **Pārbaudīt kredīta limitu, kad ir palielināta norēķinu atlaide** uz **Jā**, lai pārbaudītu norēķinu atlaides klasifikāciju, lai noteiktu, vai norēķinu atlaide pārdošanas pasūtījumā atšķiras no noklusējuma norēķinu atlaides klientam. Ja jaunajai termiņatlaidei ir augstāks rangs nekā sākotnējai termiņatlaidei, pasūtījums tiek nodots kredīta pārvaldības aizturēšanai.
- Laukā **Modificēto pasūtījumu palaišanas iemesls**, atlasiet palaišanas iemeslu, kas tiks izmantots pēc noklusējuma, kad modificētie pasūtījumi tiek automātiski palaisti no kredīta pārvaldības aizturēšanas.
- Iestatiet opciju **Ignorēt kredīta limita termiņa aizturēšanas kārtulu, ja beigu datums nav ievadīts** uz **Jā**, lai varētu kontrolēt **Kredīta limita termiņa** kārtulas darbību. Iestatiet opciju uz **Nē**, lai aizturētu pasūtījumu, ja beigu datums nav ievadīts.
- Noliktavas pārvaldībā noslodzes var izveidot pārdošanas pasūtījuma izveides laikā. Ievadiet opciju **Noņemt aizturētās noslodze rindas** uz **Nē**, lai pārdošanas pasūtījuma rindas tiktu atstātas noslodzei, kad pārdošanas pasūtījums tiek aizturēts. Kad pārdošanas pasūtījums ir aizturēts, noslodzi nevar apstrādāt. Iestatiet opciju uz **Jā**, lai noņemtu pārdošanas pasūtījuma rindas no noslodzes, kad pārdošanas pasūtījums ir aizturēts. Pēc tam noslodzi var apstrādāt.
- Pārdošanas pasūtījumus var automātiski nodot kredīta pārvaldības pārskatam. Laukā **Automātiskās palaišanas iemesls** atlasiet laidiena iemeslu, kas tiks izmantots pēc noklusējuma, kad pārdošanas pasūtījumi tiks automātiski palaisti.
- Pārdošanas pasūtījumus var automātiski nodot kredīta pārvaldības pārskatam. Laukā **Automātiski palaist** atlasiet **Bez grāmatošanas**, lai palaistu pasūtījuma aizturēšanu. Jums ir manuāli jāpalaiž process, kas veic pasūtījuma aizturēšanu. Atlasiet **Ar iegrāmatošanu**, lai grāmatotu pasūtījumu, izmantojot to pašu grāmatošanas procesu, kas tika veikts, kad pārdošanas pasūtījums tika aizturēts.

### <a name="credit-management-checkpoint"></a>Kredīta pārvaldības kontrolpunkts

Varat iestatīt laiku, kas tiek izmantots, lai pārbaudītu, vai pārdošanas pasūtījumiem nav kredīta problēmu. Kopsavilkuma cilne **Kredīta pārvaldības kontrolpunkts** nosaka dokumentu grāmatošanas procesus, kas ietver kredīta pārvaldības kārtulu apstrādi. Jūs varat arī pārbaudīt kredīta kārtulas, kad veicat vai nu pro formas grāmatošanu vai pilnīgu grāmatošanu pārdošanas pasūtījumā. Atzīmējiet izvēles rūtiņas, lai definētu grāmatošanas procesus, kam būtu jātur pasūtījums, ja izdošana tiek atrasta pēc kredīta pārvaldības bloķēšanas noteikumu apstrādes.

Varat arī norādīt pagarinājuma dienu skaitu pirms kredīta kārtulas tiek pārbaudītas atkārtoti. Lai gan varat norādīt, ka kredīta pārvaldības kārtulas tiek pārbaudītas grāmatošanas procesā, kārtulas netiks pārbaudītas noteiktam pagarinājuma dienu skaitam. Piemēram, jūs apstiprināt pārdošanas pasūtījumu pirmajā dienā un apstiprināšanas solim norādāt divas pagarinājuma dienas. Šajā gadījumā kredīta noteikumi netiks pārbaudīti nākamajā grāmatošanas solī (piemēram, pavadzīmes izveide vai pasūtījuma rēķina izrakstīšana) līdz četrām dienai. Četras dienas vai pēc tās noteikumi tiks atkal pārbaudīti, kad notiks grāmatošana, un pagarinājuma dienu skaits tiks mainīts uz vērtību, kas ir norādīta nākamajam grāmatošanas kontrolpunktam.

Ja nenorādāt pagarinājuma dienu skaitu, kredīta kārtulas tiks pārbaudītas visos grāmatošanas posmos, kas iestatīti kredīta pārvaldības kārtulu izpildei. Ja pārdošanas pasūtījums tiek nodots bez grāmatošanas un pēc tam tiek palaista tāda pati pasūtījuma apstrādes darbība, kredīta kārtulas tiks pārbaudītas vēlreiz. Piemēram, pasūtījums tiek aizturēts pēc apstiprinājuma, un tas tiek palaists ar vai bez grāmatošanas. Šādā gadījumā pasūtījums atkal tiks aizturēts, ja apstiprināsiet to vēlreiz. Izmantojiet pagarinājuma dienas, ja pasūtījumam ir jāpāriet uz nākamo apstrādes darbību, neveicot atkārtotu aizturēšanu.

> [!Note]
> Ja vienam grāmatošanas kontrolpunktam ir ievadīta pagarinājuma diena, visiem kontrolpunktiem, kas atzīmēti grāmatošanai, nepieciešamas pagarinājuma dienas.

- Atzīmējiet **izvēles rūtiņu** Grāmatošana, lai darbinātu kredīta pārvaldības noteikumus, ja tiek palaists rindā parādītā grāmatošanas kontrolpunkts. Ja izvēles rūtiņa nav atzīmēta, noteikumi tiks pārbaudīti tikai vienu reizi visa grāmatošanas procesa laikā.
- Atlasot izvēles rūtiņu **Grāmatošana**, norādiet pagarinājuma dienu skaitu, kam jāpaiet, pirms bloķēšanas noteikumi tiek pārbaudīti vēlreiz. Nevar pievienot pagarinājuma dienas, ja ir notīrīta **izvēles** rūtiņa Grāmatošana.
- Atzīmējiet **izvēles rūtiņu Pro forma**, lai palaistu kredīta pārvaldības noteikumus, kad tiek palaista rindai parādītā pro forma grāmatošanas izvēles rūtiņa. Vairākumā gadījumu lauks **Grāmatošana** ir iestatīts uz **Nē** dialoglodziņā, kas parādās, kad pārdošanas pasūtījums tiek grāmatots.
- Atlasot izvēles rūtiņu **Grāmatošana**, norādiet pagarinājuma dienu skaitu, kam jāpaiet, pirms bloķēšanas noteikumi tiek pārbaudīti vēlreiz. Nevar pievienot pagarinājuma dienas, ja ir notīrīta **izvēles** rūtiņa Grāmatošana.

### <a name="credit-management-statistics"></a>Kredīta pārvaldības statistika

Vairāki kredīta pārvaldības statistikas dati ir iekļauti papildinformācijas **Debitora kredīta pārvaldības statistika** sadaļā, kas atrodas lapā **Debitors**. Jums ir jānorāda vairākas vērtības, kas nepieciešamas, lai aprēķinātu šo statistiku. Ievadiet mēnešu skaitu, kas tiek izmantots, lai aprēķinātu šādas vērtības papildinformācijas sadaļā **Debitora kredīta pārvaldības statistika**.

1. Vidējais maksājuma saņemšanas laiks 1
2. Vidējais maksājuma saņemšanas laiks 2
3. Vidējā bilance 1
4. Vidējā bilance 2
5. Vidējais kredīta limits %
6. Vidējā pieejamība %

### <a name="credit-limits"></a>Kredīta limiti

- Kredīta pārvaldībā debitora kredīta limits tiek norādīts debitora valūtā. Ir jādefinē valūtas maiņas kursa tips kredīta limitam debitora valūtā. Laukā **Kredīta limita maiņas kursa tips** atlasiet valūtas maiņas kursa tipu, kas jāizmanto, lai konvertētu primāro kredīta limitu uz debitora kredīta limitu.
- Iestatiet opciju **Atļaut manuālu kredīta limitu rediģēšanu** uz **Nē**, lai neļautu lietotājiem rediģēt kredīta limitus lapā **Debitors**. Ja šī opcija ir iestatīta uz **Nē**, debitora kredīta limita izmaiņas var veikt, grāmatojot kredīta limita korekcijas darbības.
- Iestatiet opciju Apiet **krājumu rezervācijas uz** Jā **,** lai ignorētu krājumu rezervācijas, ja ir pārbaudīti kredīta pārvaldības bloķēšanas noteikumi. Šajā gadījumā tiek pārbaudīti daudzumi un iespējoti kontrolpunkta pagarinājuma periodi neatkarīgi no krājumu rezervēšanas daudzuma.
- Kad kredīta pārvaldība ir aktivizēta, iestatījums **Ziņojums, kad tiek pārsniegts kredīta limita** lauks, tiek izmantots tikai brīvā teksta rēķinu apstrādājumam. Kaut arī ziņojumi joprojām tiek pievienoti pārdošanas pasūtījumiem, ja debitori ir pārsnieguši kredīta limitu, šo ziņojumu klātbūtne nebloķē apstiprinājumu, izdošanas sarakstu un pavadzīmju drukāšanu vai rēķinu grāmatošanu.

    Kredīta pārvaldība tiek aktivizēta pēc noklusējuma, bet jūs variet to deaktivizēt. Ja šī opcija ir iespējota, tiek izmantots kredīta pārvaldības bloķēšanas noteikumi un kontrolpunkti, lai noteiktu, kad debitori ir pārsnieguši kredīta limitu. Ja tā ir deaktivizēta, ziņojumi, kas tiek pievienoti pārdošanas pasūtījumiem, balstoties uz ziņojuma iestatījumu, **pārsniedzot** kredīta limita lauku, var palīdzēt identificēt, kad debitori ir pārsnieguši kredīta limitu.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Numuru secības un koplietojamie numuru secības parametri

Lai apstrādātu kredīta limita korekcijas, nepieciešams žurnāla ID. Jums ir jāpievieno kredīta limita korekcijas numurs, kas jāizmanto, lai ģenerētu žurnāla ID.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
