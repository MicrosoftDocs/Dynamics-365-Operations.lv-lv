---
title: Kredīta pārvaldības parametru iestatīšana
description: Šajā tēmā aprakstītas opcijas, kuras var izmantot, lai konfigurētu kredīta pārvaldību atbilstoši jūsu biznesa vajadzībām.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02d7e2238e58098428397121de848a1947a991ad
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015312"
---
# <a name="credit-management-parameters-setup"></a>Kredīta pārvaldības parametru iestatīšana

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā aprakstītas opcijas, kuras var izmantot, lai konfigurētu kredīta pārvaldību atbilstoši jūsu biznesa vajadzībām. Lai sāktu izmantot kredīta pārvaldības līdzekļus, iestatiet parametrus lapā **Kredīta pārvaldības parametri** (**Kredīta pārvaldība \> Iestatījumi \> Kredīta pārvaldības parametri**).

## <a name="credit-parameters"></a>Kredīta parametri

Ir četras kopsavilkuma cilnes, kurās varat mainīt parametrus, kas kontrolē kredīta pārvaldību: **kredīt aizturēšanas gadījumi**, **Kredīta pārvaldības kontrolpunkts**, **Kredīta pārvaldības statistikas** un **Kredīta limiti**. Tālāk esošajās sadaļās aprakstīti iestatījumi, kas ir pieejami katrā kopsavilkuma cilnē.

### <a name="credit-holds"></a>Kredītu aiztures

- Iestatiet opciju **Atļaut rediģēt pārdošanas pasūtījumus pēc pasūtījuma aizturēšanas palaišanas** uz **Jā**, lai pieprasītu, ka grāmatošanas kārtulas atkal tiek pārbaudīti, ja pārdošanas pasūtījuma vērtība (pilna cena) ir mainīta kopš pārdošanas pasūtījuma palaišanas no aizturēšanas saraksta. .
- Laukā **Atcelto pasūtījumu iemesli** atlasiet palaišanas iemeslu, kas tiks izmantots pēc noklusējuma, kad pārdošanas pasūtījums, kas bija kredīta pārvaldības aizturēšanā, tiks atcelts.
- Lai pārbaudītu debitora kredīta grupas kredīta limitu, kad pārdošanas pasūtījuma debitors pieder debitoru kredīta grupai, iestatiet opciju **Pārbaudīt debitora kredīta grupas kredīta līmeni** uz **Jā**. Tiek pārbaudīts grupas kredīta limits un pēc tam, ja tas ir pietiekams, tiks pārbaudīts debitora kredīta limits.
- Iestatiet opciju **Pārbaudīt kredīta limitu, kad ir palielināti apmaksas nosacījumi** uz **Jā**, lai pārbaudītu apmaksas nosacījumu klasifikāciju, lai noteiktu, vai maksājuma nosacījumi pārdošanas pasūtījumā atšķiras no apmaksas nosacījumiem pārdošanas pasūtījumā. Ja jaunajiem apmaksas nosacījumiem ir augstāks rangs nekā sākotnējiem apmaksas nosacījumiem, pasūtījums tiek nodots kredīta pārvaldības aizturēšanai.
- Iestatiet opciju **Pārbaudīt kredīta limitu, kad ir palielināta norēķinu atlaide** uz **Jā**, lai pārbaudītu norēķinu atlaides klasifikāciju, lai noteiktu, vai norēķinu atlaide pārdošanas pasūtījumā atšķiras no norēķinu atlaides pārdošanas pasūtījumā. Ja jaunajai termiņatlaidei ir augstāks rangs nekā sākotnējai termiņatlaidei, pasūtījums tiek nodots kredīta pārvaldības aizturēšanai.
- Laukā **Modificēto pasūtījumu palaišanas iemesls**, atlasiet palaišanas iemeslu, kas tiks izmantots pēc noklusējuma, kad modificētie pasūtījumi tiek automātiski palaisti no kredīta pārvaldības aizturēšanas.
- Iestatiet opciju **Ignorēt kredīta limita termiņa aizturēšanas kārtulu, ja beigu datums nav ievadīts** uz **Jā**, lai varētu kontrolēt **Kredīta limita termiņa** kārtulas darbību. Iestatiet opciju uz **Nē**, lai aizturētu pasūtījumu, ja beigu datums nav ievadīts.
- Noliktavas pārvaldībā noslodzes var izveidot pārdošanas pasūtījuma izveides laikā. Ievadiet opciju **Noņemt aizturētās noslodze rindas** uz **Nē**, lai pārdošanas pasūtījuma rindas tiktu atstātas noslodzei, kad pārdošanas pasūtījums tiek aizturēts. Kad pārdošanas pasūtījums ir aizturēts, noslodzi nevar apstrādāt. Iestatiet opciju uz **Jā**, lai noņemtu pārdošanas pasūtījuma rindas no noslodzes, kad pārdošanas pasūtījums ir aizturēts. Pēc tam noslodzi var apstrādāt.
- Pārdošanas pasūtījumus var automātiski nodot kredīta pārvaldības pārskatam. Laukā **Automātiskās palaišanas iemesls** atlasiet laidiena iemeslu, kas tiks izmantots pēc noklusējuma, kad pārdošanas pasūtījumi tiks automātiski palaisti.
- Pārdošanas pasūtījumus var automātiski nodot kredīta pārvaldības pārskatam. Laukā **Automātiski palaist** atlasiet **Bez grāmatošanas**, lai palaistu pasūtījuma aizturēšanu. Jums ir manuāli jāpalaiž process, kas veic pasūtījuma aizturēšanu. Atlasiet **Ar iegrāmatošanu**, lai grāmatotu pasūtījumu, izmantojot to pašu grāmatošanas procesu, kas tika veikts, kad pārdošanas pasūtījums tika aizturēts.

### <a name="credit-management-checkpoint"></a>Kredīta pārvaldības kontrolpunkts

Varat iestatīt laiku, kas tiek izmantots, lai pārbaudītu, vai pārdošanas pasūtījumiem nav kredīta problēmu. Kopsavilkuma cilne **Kredīta pārvaldības kontrolpunkts** nosaka dokumentu grāmatošanas procesus, kas ietver kredīta pārvaldības kārtulu apstrādi. Jūs varat arī pārbaudīt kredīta kārtulas, kad veicat vai nu pro formas grāmatošanu vai pilnīgu grāmatošanu pārdošanas pasūtījumā. Atzīmējiet izvēles rūtiņas, lai definētu grāmatošanas procesus, kuriem ir nepieciešams aizturēt pasūtījumu, ja pēc kredīta pārvaldības aizturēšanas kārtulu apstrādes tiek atrasta problēma.

Varat arī norādīt pagarinājuma dienu skaitu pirms kredīta kārtulas tiek pārbaudītas atkārtoti. Lai gan varat norādīt, ka kredīta pārvaldības kārtulas tiek pārbaudītas grāmatošanas procesā, kārtulas netiks pārbaudītas noteiktam pagarinājuma dienu skaitam. Piemēram, jūs apstiprināt pārdošanas pasūtījumu 1. dienā un jūs norādāt divas pagarinājuma dienas apstiprināšanas solim. Šādā gadījumā kredīta kārtulas netiks pārbaudītas nākamajā grāmatošanas solī (piemēram, pavadzīmes izveide vai pasūtījuma rēķina izrakstīšana) līdz 4. dienai. 4. dienā vai pēc tam, kad notiek grāmatošana, kārtulas tiks pārbaudītas vēlreiz, un pagarinājuma dienu skaits tiks mainīts uz vērtību, kas norādīta nākamajam grāmatošanas kontrolpunktam.

Ja nenorādāt pagarinājuma dienu skaitu, kredīta kārtulas tiks pārbaudītas visos grāmatošanas posmos, kas iestatīti kredīta pārvaldības kārtulu izpildei. Ja pārdošanas pasūtījums tiek nodots bez grāmatošanas un pēc tam tiek palaista tāda pati pasūtījuma apstrādes darbība, kredīta kārtulas tiks pārbaudītas vēlreiz. Piemēram, pasūtījums tiek aizturēts pēc apstiprinājuma, un tas tiek palaists ar vai bez grāmatošanas. Šādā gadījumā pasūtījums atkal tiks aizturēts, ja apstiprināsiet to vēlreiz. Izmantojiet pagarinājuma dienas, ja pasūtījumam ir jāpāriet uz nākamo apstrādes darbību, neveicot atkārtotu aizturēšanu.

Dažiem grāmatošanas kontrolpunktiem nevar norādīt pagarinājuma dienas. Visi grāmatošanas kontrolpunkti ir jāiestata tā, lai tiem būtu pagarinājuma dienas, vai arī tie ir jāiestata tā, lai tiem nebūtu pagarinājuma dienu.

- Atzīmējiet izvēles rūtiņu **Grāmatošana**, lai palaistu kredīta pārvaldības kārtulas, kad rindā parādās grāmatošanas kontrolpunkts. Ja neatzīmējat šo izvēles rūtiņu, kārtulas tiks pārbaudītas tikai vienreiz visā grāmatošanas procesā.
- Ja atzīmējat izvēles rūtiņu **Grāmatošana**, norādiet pagarinājuma dienu skaitu, kam jāpaiet pirms aizturēšanas kārtulu atkārtotas pārbaudes. Pagarinājuma dienas nevar pievienot, ja nav notīrīta izvēles rūtiņa **Grāmatošana**.
- Atzīmējiet izvēles rūtiņu **Pro forma**, lai palaistu kredīta pārvaldības kārtulas, kad rindā parādās pro forma grāmatošanas kontrolpunkts. Vairākumā gadījumu lauks **Grāmatošana** ir iestatīts uz **Nē** dialoglodziņā, kas parādās, kad pārdošanas pasūtījums tiek grāmatots.
- Ja atzīmējat izvēles rūtiņu **Grāmatošana**, norādiet pagarinājuma dienu skaitu, kam jāpaiet pirms aizturēšanas kārtulu atkārtotas pārbaudes. Pagarinājuma dienas nevar pievienot, ja nav notīrīta izvēles rūtiņa **Grāmatošana**.

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

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Numuru secības un koplietojamie numuru secības parametri

Lai apstrādātu kredīta limita korekcijas, nepieciešams žurnāla ID. Jums ir jāpievieno kredīta limita korekcijas numurs, kas jāizmanto, lai ģenerētu žurnāla ID.
