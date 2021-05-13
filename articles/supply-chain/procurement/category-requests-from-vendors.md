---
title: Kategorijas pieprasījumi no kreditoriem
description: Šajā tēmā aprakstīts, kā kreditori savā kontā var pieprasīt sagādes kategorijas. Šeit aprakstīts arī iepirkuma aģentu pabeigtais apstiprināšanas process.
author: kamaybac
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fb3555e6d923fe37479c3204f0b78f7cdf510118
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938508"
---
# <a name="category-requests-from-vendors"></a>Kategorijas pieprasījumi no kreditoriem

[!include [banner](../includes/banner.md)]

Kategorijas pieprasījuma process ļauj kreditoriem pieprasīt, lai ar to kontu tiktu saistītas jaunas sagādes kategorijas. Šīs sagādes kategorijas pēc tam var izmantot saistītie sagādes un plānošanas procesi. (Papildinformāciju skatiet rakstā, [Sagādes katalogu apskats](procurement-catalogs.md).)

Kategoriju pieprasījumus kreditori inicializē darbvietā **Kreditora informācija**. Pēc tam tie tiek iesniegti jūsu aģentūrai pārskatīšanai un apstiprināšanai. Apstiprinātās kategorijas tiek pievienotas kreditora konta sagādes kategoriju sarakstam.

## <a name="turn-on-the-feature-in-your-system"></a>Līdzekļa ieslēgšana sistēmā

Ja sistēmā vēl nav ietverts šajā tēmā aprakstītais līdzeklis, pārejiet uz sadaļu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet līdzekli *Atļaut kreditoriem pieteikties iepirkumu kategorijām, izmantojot kreditoru sadarbību*.

Kad līdzeklis ir ieslēgts, kreditora kontiem joprojām var pievienot sagādes kategorijas manuāli. Informāciju skatiet [Kreditoru apstiprināšana noteiktām sagādes kategorijām](tasks/approve-vendors-specific-procurement-categories.md).

## <a name="vendor-collaboration-requirements"></a>Kreditoru sadarbības pieprasījumi

Pirms kreditors var mijiedarboties ar kategoriju pieprasījumiem, tas jāiestata kreditoru sadarbības vajadzībām.

Kreditoram jābūt vismaz vienam kreditora sadarbības lietotājam. Kategorijas pieprasījumus var izveidot un iesniegt tikai kreditora lietotāji, kuriem ir viena vai abas šīs drošības lomas:

- Kreditora kontaktpersona (ārēja)
- Kreditora administrators (ārējs)

Papildinformāciju skatiet šeit: [Kreditoru sadarbības iestatīšana un uzturēšana](set-up-maintain-vendor-collaboration.md).

## <a name="set-up-the-vendor-category-request-workflow"></a>Kreditora kategorijas pieprasījuma darbplūsmas iestatīšana

Darbplūsma *Kreditora kategorijas pieprasījums* ir jāiestata sagādes un plānošanas darbplūsmās. Kreditori iesniegs jaunus kategoriju pieprasījumus, ko varat pārskatīt un apstiprināt. Pieprasītās sagādes kategorijas tiek pievienotas kreditora kontam pēc kategorijas pieprasījuma apstiprināšanas.

Šajā piemērā parādīts, kā iestatīt vienkāršu darbplūsmu *Kreditora kategorijas pieprasījums*, kam ir viens apstiprinātājs. Jums jāpārskata iekšējie procesi, lai noteiktu jūsu aģentūras piemēroto darbplūsmas iestatījumu.

1. Dodieties uz **Sagāde un avoti \> Iestatīšana \> Sagādes un avotu darbplūsmas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā atlasiet **Kreditora kategorijas pieprasījuma darbplūsma**, lai atvērtu darbplūsmas redaktoru.
1. Piesakieties darbplūsmas redaktorā.
1. Darbību rūtī atlasiet **Rekvizīti**.
1. Darbplūsmas lapā **Rekvizīti**, laukā **Iesniegšanas instrukcijas** ievadiet instrukcijas tekstu. Kad kreditori būs iesnieguši kategorijas pieprasījumu, instrukcijas būs redzamas kreditoriem.
1. Aizveriet lapu **Rekvizīti**.
1. Pārvelciet darbplūsmas elementu **Jaunās kategorijas pieprasījums** uz kanvu.
1. Velciet saiti no darbplūsmas elementa **Sākums** uz darbplūsmas elementu **Apstiprināt jaunu kategorijas pieprasījumu**.
1. Velciet saiti no darbplūsmas elementa **Apstiprināt jaunu kategorijas pieprasījumu** uz darbplūsmas elementu **Beigas**.
1. Veiciet dubultklikšķi uz pogas darbplūsmas elementu **Apstiprināt jaunas kategorijas pieprasījumu**.
1. Atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) darbplūsmas elementu **1. darbība** un pēc tam atlasiet **Rekvizīti**.
1. Darbplūsmas elementa lapā **Rekvizīti**, laukā **Darba vienuma tēma** ievadiet tēmas tekstu. Šis teksts tiks parādīts kā lauka **Tēma** vērtība lapā **Darba vienumi, kas piešķirti man**.
1. Laukā **Darbplūsmas elementa instrukcijas** ievadiet instrukcijas tekstu. Instrukcijas būs redzamas apstiprinātājiem, kad kategorijas pieprasījuma darbību rūtī tiks atlasīts **Darbplūsma**.
1. Kreisajā rūtī atlasiet **Piešķire**.
1. Cilnē **Piešķires veids** iestatiet **Piešķirt lietotājus šim darbplūsmas elementam** uz *Lietotājs*.
1. Cilnē **Lietotājs** sarakstā **Pieejamie lietotāji** atlasiet apstiprinātāju. Piemēram, sagādes nodaļā atlasiet lietotāju.
1. Atlasiet labas bultiņas pogu (**\>**), lai pārvietotu apstiprinātāju uz sarakstu **Atlasītie lietotāji**.
1. Aizveriet lapu **Rekvizīti**.
1. Atlasiet **Saglabāt un aizvērt**.
1. Laukā **Versiju piezīmes** ievadiet piezīmes par darbplūsmu.
1. Atlasiet **Labi**, lai saglabātu darbplūsmu.
1. Ja esat gatavs sākt darbplūsmas pārbaudi, atlasiet **Aktivizēt jauno versiju**. Pretējā gadījumā atlasiet **Neaktivizēt jauno versiju**.
1. Atlasiet **Labi**, lai pabeigtu darbplūsmas iestātījumu.

> [!TIP]
> Ja jūsu aģentūra nepieprasa kategoriju pieprasījumu apstiprināšanu, darbplūsma jākonfigurē automātiskai apstiprināšanai.

Lai iegūtu vairāk informācijas par to, kā iestātīt darbplūsmas, skatiet [Darbplūsmas sistēmas apskats](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

## <a name="create-and-submit-a-category-request"></a>Izveidot un iesniegt kategorijas pieprasījumu

Šajā sadaļā ir aprakstīts, kā kreditori var izmantot darbvietu **Kreditora informācija**, lai izveidotu, rediģētu, skatītu un iesniegtu kategoriju pieprasījumus.

### <a name="start-a-new-request"></a>Sākt jaunu pieprasījumu

Lai sāktu jaunu kategorijas pieprasījumu, veiciet šādas darbības.

1. Darbvietā **Kreditora informācija** atlasiet elementu **Kategoriju pieprasījumi**.
1. Lapā **Kategorijas pieprasījumi** darbību rūtī atlasiet **Jauns kategorijas pieprasījums**.
1. Dialoglodziņā **Jauns kategorijas pieprasījums** atrodiet kategoriju, kurai vēlaties pieteikties, pārvietojot koku un/vai lietojot filtru saraksta sākumā. Atzīmējiet izvēles rūtiņu katrai atbilstošai kategorijai.

    Ņemiet vērā šādus punktus:

    - Kategorijas, kas pašlaik ir aktīvas jūsu kreditora kontā, tiek rādītas kā atlasītas, un tās nevar noņemt.
    - Vienā kategorijas pieprasījumā var pieprasīt vairākas sagādes kategorijas.

1. Atlasiet **Labi**, lai izveidotu melnraksta pieprasījumu.

    Jaunais melnraksta pieprasījums tagad ir redzams lapā **Kategorijas pieprasījumi**.

1. Atveriet jaunu melnraksta pieprasījumu, lai pārskatītu un rediģētu to, kā nepieciešams.

    - Lai skatītu to kategoriju sarakstu, kas pašlaik ir iekļautas pieprasījumā, atlasiet kopsavilkuma cilni **Pieprasītās kategorijas**.
    - Lai skatītu aktīvās kategorijas, atveriet papildinformāciju **Aktīvās kategorijas** lapas labajā pusē.
    - Lai pieprasījumam pievienotu kategoriju, kopsavilkuma cilnes **Pieprasītās kategorijas** rīkjoslā atlasiet **Pievienot**.
    - Lai noņemtu kategoriju no pieprasījuma, atlasiet kategoriju kopsavilkuma cilnē **Pieprasītās kategorijas** un pēc tam rīkjoslā atlasiet **Noņemt**.
    - Lai pieprasījumam pievienotu dokumentu, atlasiet **Pielikumi** darbību rūtī. Pievienotie dokumenti būs pieejami apstiprinātājiem, kad tie pārskatīs kategorijas pieprasījumu.
    - Lai no pieprasījuma izņemtu pievienotu dokumentu, atlasiet **Pielikumi** darbību rūtī. Atlasiet noņemamo dokumentu un pēc tam darbību rūtī atlasiet **Dzēst**.

1. Ja esat gatavs iesniegt pieprasījumu, darbību rūtī atlasiet **Iesniegt**. Pretējā gadījumā aizveriet lapu un izlaidiet šīs procedūras atlikušās darbības. Pēc tam varat atgriezties pie pieprasījuma vēlāk.
1. Izlasiet visas parādītās iesniegšanas instrukcijas un pēc tam atlasiet **Iesniegt**.
1. Rūtī **Komentārs** ievadiet papildu informāciju, kas nepieciešama precei. Tad atlasiet **Iesniegt**, lai pabeigtu pieprasījumu.

### <a name="edit-a-draft-or-recalled-request"></a>Rediģēt melnrakstu vai atsaukto pieprasījumu

Lai rediģētu melnraksta vai atsauktās kategorijas pieprasījumu, veiciet šīs darbības.

1. Darbvietā **Kreditora informācija** atlasiet elementu **Kategoriju pieprasījumi**.
1. Atlasiet melnrakstu vai atsaukto pieprasījumu, lai to atvērtu.
1. Rediģējiet pieprasījumu pēc vajadzības un pēc tam aizveriet vai iesniedziet to, kā aprakstīts iepriekšējā procedūrā.

### <a name="submit-a-draft-or-recalled-request"></a>Iesniedziet melnrakstu vai atsaukto pieprasījumu

Lai iesniegtu melnraksta vai atsauktās kategorijas pieprasījumu, veiciet šīs darbības.

1. Darbvietā **Kreditora informācija** atlasiet elementu **Kategoriju pieprasījumi**.
1. Atlasiet melnrakstu vai atsaukto pieprasījumu, kuru vēlaties iesniegt.
1. Darbību rūtī atlasiet **Iesniegt**.
1. Izlasiet visas parādītās iesniegšanas instrukcijas un pēc tam atlasiet **Iesniegt**.
1. Rūtī **Komentārs** ievadiet papildu informāciju, kas nepieciešama precei. Tad atlasiet **Iesniegt**, lai pabeigtu pieprasījumu.

    Kategorijas pieprasījuma statuss tiek mainīts uz kādu no šīm vērtībām:

    - _Gaida atsauksmju sniegšanu_ – pieprasījums ir darbplūsmā.
    - _Gaida apstiprinājumu_ – nepieciešams apstiprinājums.

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a>Atsauciet iesniegto pieprasījumu, kas vēl nav apstiprināts

Lai atsauktu kategorijas pieprasījumu, kas ir iesniegts, bet vēl nav apstiprināts, izpildiet šīs darbības.

1. Darbvietā **Kreditora informācija** atlasiet elementu **Kategoriju pieprasījumi**.
1. Atlasiet gaidošo pieprasījumu, kuru vēlaties atsaukt.
1. Darbību rūtī atlasiet **Atsaukt**.
1. Rūtī **Ievadīt komentāru** ievadiet papildu informāciju, kas nepieciešama precei. Tad atlasiet **Iesniegt**, lai pabeigtu pieprasījumu.

    Kategorijas pieprasījuma statuss ir nomainīts uz _Atcelts_. Pieprasījums paliks šajā statusā, līdz to izdzēsīsit vai atkārtoti iesniegsit.

### <a name="delete-a-draft-or-recalled-request"></a>Dzēst melnrakstu vai atsaukto pieprasījumu

Lai dzēstu melnraksta vai atsauktās kategorijas pieprasījumu, veiciet šīs darbības.

1. Darbvietā **Kreditora informācija** atlasiet elementu **Kategoriju pieprasījumi**.
1. Atlasiet melnrakstu vai atsaukto pieprasījumu, kuru vēlaties dzēst.
1. Darbību rūtī atlasiet **Dzēst**.
1. Atlasiet **Jā**, lai apstiprinātu dzēšanu.

### <a name="view-completed-requests"></a>Skatīt pabeigtos pieprasījumus

Lai skatītu pabeigtos pieprasījumus, atveriet darbvietu **Kreditora informācija** un atlasiet elementu **Kategorijas pieprasījumi**. Kategorijas pieprasījumiem, kas ir pabeigti, būs viens no šiem statusiem:

- _Apstiprināts_ - pieprasījums tika apstiprināts. Lai skatītu jaunizveidotās kategorijas, atgriezieties pie darbvietas **Kreditora informācija**, kreisajā rūtī atveriet nolaižamo sarakstu **Papildinformācija** un pēc tam atlasiet **Kategorijas**.
- _Noraidīts_ – pieprasījums tika noraidīts. Ja nepieciešams, varat izveidot jaunu kategorijas pieprasījumu.

## <a name="review-category-requests"></a>Pārskatīt kategorijas pieprasījumus

Šajā sadaļā ir paskaidrots, kā apstiprināt, noraidīt un deleģēt kreditoru iesniegtos kategoriju pieprasījumus un kā skatīt pabeigtos pieprasījumus. Šīs darbplūsmas darbības ir visam kategorijas pieprasījumam.

### <a name="view-category-requests"></a>Skatīt kategorijas pieprasījumus

Lai skatītu kategorijas pieprasījumus, veiciet šādas darbības.

1. Atveriet **Sagāde un avoti \> Kreditori \> Kreditoru sadarbības pieprasījumi \> Kategoriju pieprasījumi**.

    Tiek parādīta lapa **Kategorijas pieprasījumi**. Noklusējuma lapas skatā ir parādīti kategoriju pieprasījumi ar statusu *Gaidoša darbība*.

1. Lai skatītu visus pieprasījumus, laukā **Rādīt pieprasījumus** atlasiet *Visi*.
1. Atveriet pieprasījumu, lai pārskatītu un rediģētu to, kā nepieciešams.

    - Lai skatītu to kategoriju sarakstu, kas pašlaik ir iekļautas pieprasījumā, atlasiet kopsavilkuma cilni **Pieprasītās kategorijas**.
    - Lai skatītu aktīvās kategorijas, atveriet papildinformāciju **Aktīvās kategorijas** lapas labajā pusē.
    - Ja dokumenti iesniegti, poga (papīra saspraude)  **Pielikumi** darbību rūtī rāda pievienoto dokumentu skaitu. Lai skatītu pievienotos dokumentus, atlasiet pogu **Pielikumi**. Pēc tam atlasiet apskatāmo dokumentu un atlasiet **Atvērt**, lai to skatītu.
    - Lai pieprasījumam pievienotu dokumentu, atlasiet **Pielikumi** darbību rūtī. Pievienotie dokumenti būs pieejami apstiprinātājiem, kad tie pārskatīs kategorijas pieprasījumu.
    - Lai no pieprasījuma izņemtu pievienotu dokumentu, atlasiet **Pielikumi** darbību rūtī. Atlasiet noņemamo dokumentu un pēc tam darbību rūtī atlasiet **Dzēst**.
    - Lai skatītu darbplūsmas vēsturi, darbību rūtī atlasiet **Darbplūsma**. Darbplūsmas opcijās atlasiet **Vairāk** un pēc tam **Darbplūsmas vēsture**. Parādās lapa **Darbplūsmas vēsture**.

### <a name="approve-a-pending-category-request"></a>Gaidošā kategorijas pieprasījuma apstiprināšana

Lai apstiprinātu gaidošo kategorijas pieprasījumu, veiciet šīs darbības.

1. Atveriet **Sagāde un avoti \> Kreditori \> Kreditoru sadarbības pieprasījumi \> Kategoriju pieprasījumi**.
1. Atlasiet gaidošo pieprasījumu apstiprināšanai.
1. Pārskatīt kategorijas pieprasījumu.
1. Nav obligāti: kopsavilkuma cilnē **Vispārīgi** laukā **Iemesla kods** atlasiet pamatojuma kodu. Pēc tam laukā **Pamatojuma komentārs** ievadiet komentāru par pamatojuma kodu.
1. Darbību rūtī atlasiet **Darbplūsma**.
1. Darbplūsmas opcijās atlasiet **Apstiprināt**.
1. Laukā **Komentārs** ievadiet papildu informāciju, kas nepieciešama precei. Tad atlasiet **Apstiprināt**, lai pabeigtu pieprasījumu.

    Kategorijas pieprasījuma statuss tiek mainīts uz _Apstiprināts_, un sagādes kategorijas tiek pievienotas kreditora kontam.

### <a name="reject-a-pending-category-request"></a>Gaidošā kategorijas pieprasījuma noraidīšana

Lai noraidītu gaidošo kategorijas pieprasījumu, veiciet šīs darbības.

1. Atveriet **Sagāde un avoti \> Kreditori \> Kreditoru sadarbības pieprasījumi \> Kategoriju pieprasījumi**.
1. Atlasiet gaidošo pieprasījumu noraidīšanai.
1. Pārskatīt kategorijas pieprasījumu.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Vispārīgi** laukā **Iemesla kods** atlasiet pamatojuma kodu. Pēc tam laukā **Pamatojuma komentārs** ievadiet komentāru par pamatojuma kodu.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Darbplūsma**.
1. Darbplūsmas opcijās atlasiet **Vairāk** un pēc tam **Noraidīt**.
1. Laukā **Komentārs** ievadiet papildu informāciju, kas nepieciešama precei. Tad atlasiet **Noraidīt**, lai pabeigtu pieprasījumu.

    Kategorijas pieprasījuma statuss ir nomainīts uz _Noraidīts_. Pašlaik kreditors var izveidot jaunu kategorijas pieprasījumu pēc vajadzības.

### <a name="delegate-a-pending-category-request"></a>Gaidošā kategorijas pieprasījuma deleģēšana

Lai deleģētu gaidošas kategorijas pieprasījumu citam lietotājam, izpildiet šīs darbības.

1. Atveriet **Sagāde un avoti \> Kreditori \> Kreditoru sadarbības pieprasījumi \> Kategoriju pieprasījumi**.
1. Atlasiet gaidošo pieprasījumu, kuru vēlaties apstiprināt.
1. Darbību rūtī atlasiet **Darbplūsma**.
1. Darbplūsmas opcijās atlasiet **Vairāk** un pēc tam **Deleģēt**.
1. Laukā **Lietotājs** atlasiet lietotāju, kam piešķirt kategorijas pieprasījumu pārskatīšanai.
1. Laukā **Komentārs** ievadiet papildu informāciju, kas nepieciešama precei.
1. Lai pabeigtu deleģēšanu, atlasiet **Deleģēt**. Atlasītais lietotājs tagad var pārskatīt kategorijas pieprasījumu.

### <a name="view-procurement-categories-for-a-vendor"></a>Skatīt kreditora sagādes kategorijas

Lai skatītu sagādes kategorijas kreditoram pēc kategorijas pieprasījuma apstiprināšanas, veiciet šīs darbības.

1. Pārejiet uz sadaļu **Sagāde un avoti \> Kreditori \> Visi kreditori**.
1. Lapā **Visi kreditori** atlasiet kreditoru, kuram vēlaties skatīt sagādes kategorijas.
1. Darbību rūtī atveriet cilni **Visparīgi** un grupā **Iestatīšana** atlasiet **Kategorijas**.

    Tiek atvērta lapa **Kategorijas**. Kopsavilkuma cilne **Sagāde** parāda sagādes kategorijas, kas tika pievienotas, izmantojot kategoriju pieprasījumu.

1. Kopsavilkuma cilnē **Sagāde** varat veikt izmaiņas, ja nepieciešams. Piemēram, jūs varat iestatīt lauku **Kreditora kategorijas statuss** uz _Vēlamais_.
