---
title: Līdzekļu veidi
description: Šajā tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot līdzekļu veidus. Tajā ir aprakstīti arī elementi, kas ir saistīti ar līdzekļu veidiem.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectJobType, EntAssetObjectType, EntAssetObjectTypeDefaultSparePart, EntAssetObjectTypeDefaultSparePartApprove, EntAssetObjectTypeDefaultCreateCombinations, EntAssetObjectTypeDefault, EntAssetObjectTypeDefaultCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b493c6993ebd466c153e999fa2592105b78d0f2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825714"
---
# <a name="asset-types"></a>Līdzekļu veidi

[!include [banner](../../includes/banner.md)]



Šajā tēmā ir paskaidrots, kā izveidot līdzekļu veidus. Tajā ir aprakstīti arī elementi, kas ir saistīti ar līdzekļu veidiem. Līdzekļu veidi tiek izmantoti kā vispārīgas līdzekļu kategorijas. Piemēri ietver CNC mašīnas, mērīšanas iekārtas un kravas automašīnu dzinējus. Līdzekļu veidus izmanto, lai pārvaldītu uzturēšanas darba veidus (uzturēšanas uzdevumus), līdzekļu dzīves cikla stāvokļus, skaitītājus, līdzekļu atribūtus, nosacījumu novērtēšanas veidnes un līdzekļu modeļus, kurus var atlasīt līdzeklim. Kad izveidojat līdzekli, ir jānorāda līdzekļa veids.

Katram līdzekļa veidam var izveidot līdzekļa veida iestatījuma variantus. Piemēram, ja jums ir līdzekļa veids ar nosaukumu **Kravas automašīnas**, varat izveidot šī līdzekļa veida variantus dažādiem līdzekļu ražotājiem un līdzekļu modeļiem. Katram līdzekļa veida iestatījumam varat pievienot nepieciešamās rezerves daļas un uzturēšanas plānus.

Vispirms iestatiet nepieciešamos līdzekļu veidus. Pēc tam izveidojiet līdzekļu modeļus, kas ir saistīti ar līdzekļu veidiem. Visbeidzot lapā **Līdzekļa veida noklusējumi** izveidojiet visus līdzekļa veidu variantus, kas ir nepieciešami jūsu aprīkojumam.

## <a name="create-an-asset-type"></a>Līdzekļa veida izveide

1. Atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļa veidi** > **Līdzekļa veidi**.
2. Atlasiet **Jauns**, lai izveidotu līdzekļa veidu.
3. Laukā **Līdzekļa veids** ievadiet līdzekļa veida ID.
4. Laukā **Nosaukums** ievadiet nosaukumu.
5. Laukā **Līdzekļa dzīves cikla modelis** atlasiet līdzekļa dzīves cikla modeli. Plašāku informāciju par līdzekļa dzīves cikla stāvokļiem un līdzekļa dzīves cikla modeļiem skatiet nodaļā [Līdzekļa dzīves cikla stāvokļi](object-stages.md).
6. Iestatiet opciju **Kopsumma** uz **Jā**, ja summētās galvenā veiktspējas indikatora (KPI) vērtības jāaprēķina līdzekļiem, kuriem ir šis līdzekļa veids.
7. Atlasiet **Saglabāt**.
8. Kopsavilkuma cilnē **Uzturēšanas darbu veidi** atlasiet uzturēšanas darbu veidus, kurus vajadzētu saistīt ar līdzekļu veidu.

    - Lai atlasītu uzturēšanas darba veidu, laukā **Atlikušie uzturēšanas darba veidi** un pēc tam atlasiet bultiņas pa labi pogu ![Bultiņas pa labi poga](media/29-setup-for-objects.png), lai pārvietotu to uz sadaļu **Atlasītie uzturēšanas darba veidi**.
    - Lai atlasītu visus pieejamos uzturēšanas darba veidus, atlasiet pogu ![Bultiņa Pārsūtīt visu](media/30-setup-for-objects.png). Visi uzturēšanas darba veidi tiek pārsūtīti no lauka **Atlikušie uzturēšanas darba veidi** uz lauku **Atlasītie uzturēšanas darba veidi**.
    - Lai atceltu uzturēšanas darba veida atlasi, atlasiet to laukā **Atlasītie uzturēšanas darba veidi** un pēc tam atlasiet bultiņas pa kreisi pogu ![Bultiņas pa kreisi poga](media/31-setup-for-objects.png), lai pārvietotu to uz lauku **Atlikušie uzturēšanas darba veidi**.

9. Varat arī atlasīt skaitītājus, kam jābūt saistītiem ar līdzekļa veidu. Kopsavilkuma cilnē **Skaitītāji** veiciet atlasi, izmantojot metodes, kas 8. darbībā aprakstītās uzturēšanas darba veidiem. Papildinformāciju par skaitītāju iestatīšanu, skatiet [Skaitītāji](counters.md).
10. Varat arī atlasīt atribūtu veidus, kam jābūt saistītiem ar līdzekļa veidu. Kopsavilkuma cilnē **Atribūtu veidi** veiciet atlasi, izmantojot metodes, kas 8. darbībā aprakstītās uzturēšanas darba veidiem. Pēc tam, lai izveidotu vēlamo atribūtu veidu secību, atlasiet atribūta veidu laukā **Atlasītie atribūtu veidi** un izmantojiet augšupvērstās un lejupvērstās bultiņas pogas, lai to pārvietotu. Atribūtu veidu secība tiks parādīta līdzekļiem, kas izmanto šo līdzekļa veidu. Plašāku informāciju par līdzekļu atribūtiem skatiet sadaļā [Uzturēšanas atribūtu veidi](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Pievienojot jaunus atribūtu veidus kopsavilkuma cilnē **Atribūtu veidi**, esošie līdzekļi tiek automātiski atjaunināti ar šo informāciju.

11. Varat arī atlasīt nosacījumu novērtējuma veidnes, kam jābūt saistītiem ar līdzekļa veidu. Kopsavilkuma cilnē **Nosacījumu novērtējumi** veiciet atlasi, izmantojot metodes, kas 8. darbībā aprakstītās uzturēšanas darba veidiem. Papildinformāciju par nosacījumu novērtēšanas veidnēm un reģistrācijām skatiet nodaļā [Nosacījumu novērtējums](../setup-for-objects/condition-assessment.md).
12. Kopsavilkuma cilnē **Līdzekļu modelis** ir parādītas visas līdzekļu ražotāju un modeļu kombinācijas, kas ir iestatītas atlasītajam līdzekļa veidam. Lai skatītu kombinācijas, kas sadalītas atbilstoši ražotājam, atlasiet **Līdzekļa modelis**, lai atvērtu lapu **Līdzekļa modelis**.

    Lapā **Līdzekļa modelis** varat pievienot līdzekļu modeļa – līdzekļu veida relācijas. Turklāt lapā **Līdzekļu veidi** varat pievienot līdzekļu ražotāju – līdzekļu modeļu relācijas tieši līdzekļa veidam. Visbeidzot lapā **Līdzekļa modelis** (**Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Līdzekļa modelis**) var izveidot jaunas līdzekļu ražotāju – līdzekļa modeļa – līdzekļa veida relācijas. Tādēļ ir trīs veidi, kā iestatīt un rediģēt līdzekļu ražotāju – līdzekļu modeļu – līdzekļu veidu relācijas. Visas pieejamās kombinācijas ir parādītas no dažādām perspektīvām, un, strādājot ar iestatījumiem, varat atlasīt vēlamo ieejas punktu.

> [!NOTE]
> - Atlasot skaitītājus līdzekļa vaidā, atlases tiek automātiski atjauninātas lapā **Skaitītāji** (**Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļi** > **Līdzekļu veidi** > **Skaitītāji**).
> - Lauki **Detalizēta informācija** sadaļā, kas atrodas kopsavilkuma cilnē **Vispārīgi**, rāda uzturēšanas darbu veidu skaitu, skaitītājus, atribūtus un tā tālāk, kuri ir iestatīti atlasītajam līdzekļa veidam.

Parasti darba pasūtījumi, kas tiek izveidoti manuāli, ir saistīti ar koriģējošo uzturēšanu, bet automātiski izveidotie darba pasūtījumi ir saistīti ar profilaktisko uzturēšanu. Manuāli izveidojot darba pasūtījumus, var izmantot tikai tos uzturēšanas darba veidus, kas atlasīti kopsavilkuma cilnē **uzturēšanas darba veidi** lapā **Līdzekļu veidi**. Taču automātiski izveidotie darba pasūtījumi var izmantot visus uzturēšanas darba veidus, ko izveidojat lapā **Uzturēšanas darba veidi** (**Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darbi** \> **Uzturēšanas darba veidi**).

## <a name="create-asset-type-setup-lines"></a>Līdzekļu veida iestatījuma rindu izveide

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Līdzekļa veidi** \> **Līdzekļa veida iestatīšana**. Vai arī atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Līdzekļa veidi** \> **Līdzekļa veidi**, atlasiet līdzekļa veidu un pēc tam atlasiet **Līdzekļa veida iestatīšana**.
2. Pirmo reizi izmantojot lapu **Līdzekļa veida iestatīšana** noderīga var izrādīties poga **Izveidot kombinācijas**. Šo pogu var izmantot, lai ātri izveidotu visas līdzekļa modeļa kombinācijas līdzekļa veidam. Atlasiet **Izveidot kombinācijas**, atlasiet līdzekļa veidu, kuram izveidot kombinācijas, un pēc tam atlasiet **Labi**.

    > [!NOTE]
    > Ja neizmantosit visas automātiski izveidotās līdzekļa veida iestatījuma kombinācijas, iestatījumu var izdzēst, atlasot to un pēc tam atlasot **Dzēst**.

3. Atlasiet **Jauns**, lai manuāli izveidotu līdzekļa veida iestatījumu.
4. Atkarībā no tā, cik specifiskam jābūt līdzekļa veida iestatījumam, veiciet atlasi laukos **Līdzekļa veids**, **Ražotājs** un **Modelis**.
5. Ja garantijas līgums ir saistīts ar līdzekļa veidu, atlasiet līgumu laukos **Kreditora garantija** un **Debitora garantija**. 
6. Kopsavilkuma cilnē **Rezerves daļas** atlasiet **Pievienot**, lai pievienotu rezerves daļas atlasītajam līdzekļa veida iestatījumam.
7. Lai apstiprinātu rezerves daļu, atlasiet rezerves daļas rindu un pēc tam atlasiet **Apstiprināt**. Apstiprināšanai var atlasīt vairākas rindas.
8. Lai skatītu, vai rezerves daļa tiek izmantota citur Līdzekļu pārvaldībā (piemēram, saistībā ar līdzekļiem un darba pasūtījumiem), atlasiet rezerves daļas rindu un pēc tam atlasiet **Kur vienība izmantota**, lai atvērtu lapu **Kur vienība izmantota**. Lai skatītu visas aktīvās rezerves daļas sarakstā, atzīmējiet izvēles rūtiņu **Aktīvs**. Lai skatītu tikai apstiprinātas rezerves daļas, atzīmējiet izvēles rūtiņu **Apstiprināts**.
9. Kopsavilkuma cilnē **Uzturēšanas plāni** atlasiet **Pievienot**, lai pievienotu uzturēšanas plānus atlasītajam līdzekļa veida iestatījumam.
10. Lai kopētu līdzekļa veida iestatījumu uz citu iestatījumu, varat izmantot kopēšanas funkciju. Atlasiet līdzekļa veida iestatījumu, uz kuru kopēt iestatījumu, atlasiet **Kopēt iestatījumu** un atlasiet līdzekļa veida iestatījumu, no kura iestatījums jākopē. Dažādu opciju iestatījumi nosaka, cik daudz informācijas tiek iekļauts. Kad esat pabeidzis, atlasiet **Labi**, lai kopētu iestatījumu.

> [!NOTE]
> Ja jums ir daudzas rezerves daļu rindas un uzturēšanas plānu rindas, kuras jūs atkārtoti lietosit, kopēšanas funkcija ļauj ātri un vienkārši iestatīt datus daudzām līdzekļu tipa iestatījumu kombinācijām.

## <a name="spare-parts-on-the-asset-type-setup"></a>Rezerves daļas līdzekļa veida iestatījumos

Kā tika aprakstīts sadaļā "Izveidot līdzekļa veida iestatījuma rindas", rezerves daļas tiek iestatītas līdzekļu modeļos lapā **Līdzekļa veida iestatīšana**. Tāpēc, atverot lapu **Līdzekļa veida iestatīšana**, ir redzamas tikai tās rezerves daļas, kas ir saistītas ar atlasīto līdzekļa veida, līdzekļu ražotāja un līdzekļu modeļa kombināciju. Lai skatītu visu rezerves daļu ierakstu sarakstu, atveriet lapu **Rezerves daļas** (**Līdzekļu pārvaldība** \> **Uzziņas** \> **Rezerves daļas**).

Lapā **Rezerves daļas** varat arī izveidot jaunas rezerves daļas esošajām līdzekļa veida, līdzekļu ražotāja un līdzekļu modeļa kombinācijām. Varat izlemt, vai vēlaties izveidot rezerves daļu ierakstus lapā **Līdzekļa veida iestatīšana** vai lapā **Rezerves daļas**. Lapā **Līdzekļa veida iestatīšana** ir sniegts datu pārskats par atlasīto līdzekļa veida, līdzekļu ražotāju un līdzekļa modeļu kombināciju, bet lapā **Rezerves daļas** ir sniegts pilnīgs pārskats par visām līdzekļa veida iestatījuma rindām. Ja lapā **Rezerves daļas** ir daudz ierakstu, iespējams, ka lapa **Līdzekļa veida iestatīšana** sniedz labāku pārskatu.

Lai skatītu, vai rezerves daļa atlasītajā rindā tiek izmantota jebkurā vietā Līdzekļu pārvaldībā (piemēram, saistībā ar līdzekļiem un darba pasūtījumiem), atlasiet rezerves daļas rindu un pēc tam atlasiet **Kur vienība izmantota**, lai atvērtu lapu **Kur vienība izmantota**. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]