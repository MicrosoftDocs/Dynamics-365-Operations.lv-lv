---
title: Līdzekļu veidi
description: Šajā tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot līdzekļu veidus. Tajā ir aprakstīti arī elementi, kas ir saistīti ar līdzekļu veidiem.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288dac77f9d999012ec930ef2bca5c0921c2955f
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783438"
---
# <a name="asset-types"></a>Līdzekļu veidi

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šajā tēmā ir paskaidrots, kā izveidot līdzekļu veidus. Tajā ir aprakstīti arī elementi, kas ir saistīti ar līdzekļu veidiem. Līdzekļu veidi tiek izmantoti kā vispārīgas līdzekļu kategorijas. Piemēri ietver CNC mašīnas, mērīšanas iekārtas un kravas automašīnu dzinējus. Līdzekļu veidus izmanto, lai pārvaldītu darba veidus (uzturēšanas uzdevumus), līdzekļu dzīves cikla stāvokļus, līdzekļu mērus, līdzekļu atribūtus, nosacījumu novērtēšanas veidnes un līdzekļu modeļus, kurus var atlasīt līdzeklim. Kad izveidojat līdzekli, ir jānorāda līdzekļa veids.

Katram līdzekļa veidam var izveidot līdzekļa veida iestatījuma variantus. Piemēram, ja jums ir līdzekļa veids ar nosaukumu **Kravas automašīnas**, varat izveidot šī līdzekļa veida variantus dažādiem līdzekļu ražotājiem un līdzekļu modeļiem. Katram līdzekļa veida iestatījumam varat pievienot nepieciešamās rezerves daļas un uzturēšanas plānus.

Vispirms iestatiet nepieciešamos līdzekļu veidus. Pēc tam izveidojiet līdzekļu modeļus, kas ir saistīti ar līdzekļu veidiem. Visbeidzot lapā **Līdzekļa veida noklusējumi** izveidojiet visus līdzekļa veidu variantus, kas ir nepieciešami jūsu aprīkojumam.

## <a name="create-an-asset-type"></a>Līdzekļa veida izveide

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļa veidi** \> **Līdzekļa veidi**.
2. Atlasiet **Jauns**, lai izveidotu līdzekļa veidu.
3. Laukā **Līdzekļa veids** ievadiet līdzekļa veida ID.
4. Laukā **Nosaukums** ievadiet nosaukumu.
5. Laukā **Līdzekļa dzīves cikla modelis** atlasiet līdzekļa dzīves cikla modeli. Plašāku informāciju par līdzekļa dzīves cikla stāvokļiem un līdzekļa dzīves cikla modeļiem skatiet nodaļā [Līdzekļa dzīves cikla stāvokļi](object-stages.md).
6. Iestatiet opciju **Kopsumma** uz **Jā**, ja summētās galvenā veiktspējas indikatora (KPI) vērtības jāaprēķina līdzekļiem, kuriem ir šis līdzekļa veids.
7. Atlasiet **Saglabāt**.
8. Kopsavilkuma cilnē **Darba veidi** atlasiet darba veidus, kam jābūt saistītiem ar līdzekļa veidu:

    - Lai atlasītu darba veidu, laukā **Atlikušie darba veidi** un pēc tam atlasiet bultiņas pa labi pogu ![Bultiņas pa labi poga](media/29-setup-for-objects.png), lai pārvietotu to uz sadaļu **Atlasītie darba veidi**.
    - Lai atlasītu visus pieejamos darba veidus, atlasiet pogu ![Bultiņa Pārsūtīt visu](media/30-setup-for-objects.png). Visi darba veidi tiek pārsūtīti no lauka **Atlikušie darba veidi** uz lauku **Atlasītie darba veidi**.
    - Lai atceltu darba veida atlasi, atlasiet to laukā **Atlasītie darba veidi** un pēc tam atlasiet bultiņas pa kreisi pogu ![Bultiņas pa kreisi poga](media/31-setup-for-objects.png), lai pārvietotu to uz lauku **Atlikušie darba veidi**.

9. Varat arī atlasīt līdzekļa mērus, kam jābūt saistītiem ar līdzekļa veidu. Kopsavilkuma cilnē **Līdzekļa mēri** veiciet atlasi, izmantojot metodes, kas 8. darbībā aprakstītās darba veidiem. Plašāku informāciju par līdzekļu mēru iestatīšanu skatiet sadaļā [Uzturēšanas līdzekļu mēri](counters.md).
10. Varat arī atlasīt atribūtu veidus, kam jābūt saistītiem ar līdzekļa veidu. Kopsavilkuma cilnē **Atribūtu veidi** veiciet atlasi, izmantojot metodes, kas 8. darbībā aprakstītās darba veidiem. Pēc tam, lai izveidotu vēlamo atribūtu veidu secību, atlasiet atribūta veidu laukā **Atlasītie atribūtu veidi** un izmantojiet augšupvērstās un lejupvērstās bultiņas pogas, lai to pārvietotu. Atribūtu veidu secība tiks parādīta līdzekļiem, kas izmanto šo līdzekļa veidu. Plašāku informāciju par līdzekļu atribūtiem skatiet sadaļā [Uzturēšanas atribūtu veidi](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Pievienojot jaunus atribūtu veidus kopsavilkuma cilnē **Atribūtu veidi**, esošie līdzekļi tiek automātiski atjaunināti ar šo informāciju.

11. Varat arī atlasīt nosacījumu novērtējuma veidnes, kam jābūt saistītiem ar līdzekļa veidu. Kopsavilkuma cilnē **Nosacījumu novērtējumi** veiciet atlasi, izmantojot metodes, kas 8. darbībā aprakstītās darba veidiem. Papildinformāciju par nosacījumu novērtēšanas veidnēm un reģistrācijām skatiet nodaļā [Nosacījumu novērtējums](../setup-for-objects/condition-assessment.md).
12. Kopsavilkuma cilnē **Līdzekļu modelis** ir parādītas visas līdzekļu ražotāju un modeļu kombinācijas, kas ir iestatītas atlasītajam līdzekļa veidam. Lai skatītu kombinācijas, kas sadalītas atbilstoši ražotājam, atlasiet **Līdzekļa modelis**, lai atvērtu lapu **Līdzekļa modelis**.

    Lapā **Līdzekļa modelis** varat pievienot līdzekļu modeļa – līdzekļu veida relācijas. Turklāt lapā **Līdzekļu veidi** varat pievienot līdzekļu ražotāju – līdzekļu modeļu relācijas tieši līdzekļa veidam. Visbeidzot lapā **Līdzekļa modelis** (**Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Līdzekļa modelis**) var izveidot jaunas līdzekļu ražotāju – līdzekļa modeļa – līdzekļa veida relācijas. Tādēļ ir trīs veidi, kā iestatīt un rediģēt līdzekļu ražotāju – līdzekļu modeļu – līdzekļu veidu relācijas. Visas pieejamās kombinācijas ir parādītas no dažādām perspektīvām, un, strādājot ar iestatījumiem, varat atlasīt vēlamo ieejas punktu.

> [!NOTE]
> - Ja atlasāt līdzekļa mērus līdzekļa veidam, jūsu atlase tiek automātiski atjaunināta lapā **Līdzekļa mēri** page (**Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Līdzekļu veidi** \> **Līdzekļa mēri**).
> - Lauki **Detalizēta informācija** sadaļā, kas atrodas kopsavilkuma cilnē **Vispārīgi**, rāda darbu veidu skaitu, līdzekļu mērus, atribūtus utt., kuri ir iestatīti atlasītajam līdzekļa veidam.

Parasti darba pasūtījumi, kas tiek izveidoti manuāli, ir saistīti ar koriģējošo uzturēšanu, bet automātiski izveidotie darba pasūtījumi ir saistīti ar profilaktisko uzturēšanu. Manuāli izveidojot darba pasūtījumus, var izmantot tikai tos darba veidus, kas atlasīti kopsavilkuma cilnē **Darba veidi** lapā **Līdzekļu veidi**. Taču automātiski izveidotie darba pasūtījumi var izmantot visus darba veidus, ko izveidojat lapā **Darba veidi** (**Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darbi** \> **Darba veidi**).

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

