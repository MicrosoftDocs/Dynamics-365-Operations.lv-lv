---
title: Noliktavas darba atliktā apstrāde
description: Šajā tēmā ir aprakstīta funkcionalitāte, kas padara noliktavas darba izvietot operāciju atlikto apstrādi pieejamu programmā  Dynamics 365 Supply Chain Management.
author: josaw1
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f6e35e52aea389d90dd140a4f85fe21e335704cad4cbab4ea26bcad1fd6774eb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735876"
---
# <a name="deferred-processing-of-warehouse-work"></a>Noliktavas darba atliktā apstrāde

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta funkcionalitāte, kas padara izvietošanas operāciju noliktavas darbam atlikto apstrādi pieejamu programmā Dynamics 365 Supply Chain Management.

Atliktās apstrādes funkcionalitāte ļauj noliktavas darbiniekiem turpināt darīt citu darbu, kamēr izvietošanas operācija tiek apstrādāta fonā. Atliktā apstrāde ir noderīga, ja ir jāapstrādā daudzas darba rindas un darbinieks var ļaut šo darbu apstrādāt asinhroni. Tas noder arī tad, ja serverim var būt ad hoc vai neplānoti palielinājumi apstrādes laikā, un palielinātais apstrādes laiks var ietekmēt lietotāja produktivitāti.

Fona apstrāde tiek panākta, izmantojot SysOperation platformu. Papildinformāciju skatiet rakstā [SysOperation platformas apskats](/dynamicsax-2012/developer/sysoperation-framework-overview).

## <a name="configuring-the-work-processing-policies"></a>Darba apstrādes politiku konfigurēšana

Lai izmantotu atlikto apstrādi, ir jākonfigurē un jāizmanto darba apstrādes politika.

Politikas tiek konfigurētas lapā **Darba apstrādes politikas**. Nākamajā tabulā ir aprakstīti lauki šajā lapā.

| Lauks                           | Apraksts |
|---------------------------------|-------------|
| Darba apstrādes politikas nosaukums     | Darba apstrādes politikas nosaukums. |
| Darba pasūtījuma veids                 | Darba pasūtījuma veids, uz kuru attiecas politika. |
| Operācija                       | Operācija, kas tiek apstrādāta, izmantojot politiku. |
| Darba apstrādes metode          | Metode, kas tiek izmantota, lai apstrādātu darbu rindu. Ja metode ir iestatīta uz **Tūlītēju**, darbība atgādina darbību, kad nav darba apstrādes politikas, ko izmanto rindas apstrādāšanai. Ja metode ir iestatīta uz **Atliktu**, tiek izmantota atliktā apstrāde, kas izmanto partijas struktūru. |
| Atliktās apstrādes slieksnis   | Vērtība **0** (nulle) norāda, ka nav sliekšņvērtības. Šādā gadījumā, ja to var izmantot, tiek izmantota atliktā apstrāde. Ja konkrētās sliekšņvērtības aprēķins ir zemāks par sliekšņvērtību, tiek izmantota tūlītējā metode. Pretējā gadījumā izmanto atlikto metodi, ja to var izmantot. Ar pārdošanu un pārsūtīšanu saistītiem darbiem sliekšņvērtību aprēķina kā saistīto avota noslodzes rindu skaitu, kuras tiek apstrādātas attiecīgajam darbam. Papildināšanas darbiem sliekšņvērtība tiek aprēķināta kā darba rindu skaits, ko darbs papildina. Iestatot sliekšņvērtību, piemēram, **5** pārdošanai, mazāki darbi, kam ir mazāk nekā piecas sākotnējā avota noslodzes rindas, neizmantos atlikto apstrādi, bet lielāki darbi to izmantos. Sliekšņvērtība ir spēkā tikai tad, ja darba apstrādes metode ir iestatīta uz **Atliktu**. |
| Atliktās apstrādes partijas grupa |Partijas grupa, ko izmanto apstrādei. |

Atliktās izvietošanas apstrādei tiek atbalstīti šādi darba pasūtījumu veidi: pārdošanas pasūtījums, pārsūtīšanas pasūtījuma izdošana un papildināšana.

## <a name="assigning-the-work-creation-policy"></a>Darba izveides politikas piešķiršana

Darba izveides politiku var piešķirt noliktavas pārvaldības parametros. To var piešķirt arī atsevišķu noliktavu līmenī. Ja noliktavai ir piešķirta politika, tā tiek attiecināta tikai uz darbu, kas ir izveidots šai noliktavai. Ja noliktavas līmenī nav piešķirta neviena politika, tiek lietota politika no noliktavas pārvaldības parametriem.

## <a name="viewing-the-deferred-put-processing-tasks"></a>Atliktās izvietošanas apstrādes uzdevumu skatīšana

Varat apskatīt atliktās izvietošanas apstrādes uzdevumus lapā **Atliktās izvietošanas apstrādes uzdevumi**.

Pēc noklusējuma tiek parādīti **Pabeigtie** uzdevumi.

| Lauks            | Apraksts |
|------------------|-------------|
| Statuss           | Uzdevuma statuss. |
| Pakešuzdevuma statuss | Saistītā pakešuzdevuma statuss. Ja pakešuzdevums ir apstrādāts, partijas vēsturē ir žurnāls un informācija no pakešuzdevuma. |

Tālāk sniegts iespējamo statusu skaidrojums.

- **Gaida** — saistītais pakešuzdevums gaida apstrādi pakešapstrādes serverī.
- **Neizdevās** — apstrāde neizdevās. Uzdevumu var apstrādāt atkārtoti, izmantojot darbību **Apstrādāt atlikto izvietošanu**, vai to var atcelt, izmantojot darbību **Atcelt atlikto izvietošanu** .
- **Pabeigts** — darbs ir pabeigts.

## <a name="impact-on-closed-work-dates"></a>Ietekme uz slēgtiem darba datumiem

Ja tiek izmantota atliktās izvietošanas apstrāde, slēgtā darba datums ir iestatīts kā atliktās izvietošanas apstrādes uzdevumu izveidotais datums/laiks. Slēgto darba datumu izmanto, jo tas ir labākais novērtējums, kad izvietošanas operācija tika pabeigta.

## <a name="reprocessing-a-failed-task"></a>Neveiksmīga uzdevuma atkārtota apstrāde

Neizdevušos uzdevumu var atkārtoti apstrādāt, atlasot to lapā un pēc tam atlasot **Apstrādāt atlikto izvietošanu**. Atkārtota apstrāde atbilst situācijai, kad lietotājs pabeidz izvietošanu no mobilās ierīces tā, it kā tā būtu iestatīta tūlītējai apstrādei.

## <a name="canceling-failed-tasks"></a>Neizdevušos uzdevumu atcelšana

Var atcelt tikai neveiksmīgo uzdevumu izpildi. Atceļot uzdevumu, to var piešķirt jaunam lietotājam. Vai arī uzdevums var palikt piešķirts lietotājam, kurš apstrādājis darbu. Atcelšana atbilst situācijai, kad darbs tiek atgriezts uz mobilo ierīci tā, it kā pēdējā izdošanas darbība būtu tikko pabeigta un darbs ir jāizvieto. Tomēr lietotājs var noteikt, ka darbs ir "atšķirīgs", jo tam būs tikai izvietošanas darbība, un atrašanās vieta atbildīs tai atrašanās vietai, kas pirmajam lietotājam, kurš apstrādājis darbu, bija gala izvietošanas vieta.

Kad uzdevums ir atcelts, darbu vairs nebloķē atliktā izvietošanas apstrādes bloķēšanas iemesls. To var atkārtoti apstrādāt, izmantojot mobilo ierīci.

Kad uzdevums ir atcelts, uzdevuma ieraksts tiek dzēsts.

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Mobilās ierīces izvēlnes konfigurēšana, lai izlaistu atliktās apstrādes politiku

Mobilās ierīces izvēlnes vienumu var konfigurēt tā, lai atliktās apstrādes politika netiek izmantota. Tad darbs tiek apstrādāts, kā tas ir tad, kad netiek izmantota atliktās apstrādes politika. Šī funkcionalitāte ļauj supervizoram izmantot noteiktu izvēlnes vienumu, kur netiek izmantots atliktā izvietošana. Lai to konfigurētu, iestatiet lauku **Atliktās izvietošanas apstrādes politika** uz **Ignorēt iestatījumus un apstrādāt izvietošanu sinhroni**. 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>Ierobežojumi, kad netiek piemērota atliktā izvietošanas apstrāde

Ir vairāki scenāriji, kuros atliktā izvietošanas apstrāde netiek lietots pat tad, ja politika ir konfigurēta. Daži piemēri:

- Tiek izmantota manuāla darba pabeigšana.
- Darbs ir pabeigts, izmantojot automātisko pabeigšanu.
- Tiek izmantotas audita veidnes.


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>Atliktās apstrādes uzdevumu pārraudzība no izejošo darbu pārraudzības darbvietas

**Izejošo darbu pārraudzības** darbvietai ir divi elementi, kas palīdz pārraudzīt atliktās izvietošanas apstrādes uzdevumus:

- **Neveiksmīgie atliktās izvietošanas apstrādes uzdevumi** — šis elements parāda neveiksmīgo uzdevumu skaitu. Ja ir neveiksmīgi uzdevumi, noliktavas pārvaldniekam tie jāapstrādā atkārtoti vai jāatceļ, jo tie netiks automātiski apstrādāti atkārtoti.
- **Gaida atliktās izvietošanas apstrādes uzdevumus** — šis elements parāda to uzdevumu skaitu, kuri atrodas statusā **Gaida** vairāk nekā 10 minūtes. Ja elementā tiek rādīts skaitlis, tas var norādīt, ka pakešveida apstrādes laikā radusies problēma. **Gaidošos** uzdevumus var apstrādāt manuāli. Ja pakešuzdevums uzdevumam tiek apstrādāts vēlāk, tas vienkārši neizdosies, jo tas jau ir apstrādāts. Nebūs nekādas ietekmes.

## <a name="deleting-completed-tasks"></a>Pabeigto uzdevumu dzēšana

Jūs varat dzēst atliktās izvietošanas apstrādes uzdevumus, kas ir pabeigti, atlasot tos un dzēšot tos lapā.

## <a name="additional-resources"></a>Papildu resursi

- [Krājumu manuālas pārvietošanas operācijas atliktā apstrāde](deferred-processing-manual-inventory-movement.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]