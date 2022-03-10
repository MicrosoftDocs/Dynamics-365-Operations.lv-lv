---
title: Tehnisko izmaiņu pārvaldības līdzekļa pārskats
description: Šajā tēmā ir sniegts pilns pārskats, kas parāda, kā strādāt ar tehnisko izmaiņu pārvaldību.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4c1c67559a8f2e9d0abb512f4231aea495d1957c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573997"
---
# <a name="engineering-change-management-feature-walkthrough"></a>Tehnisko izmaiņu pārvaldības līdzekļa pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts pilns pārskats, kas parāda, kā strādāt ar tehnisko izmaiņu pārvaldību. Tas apskata katru no svarīgākajiem scenārijiem:

- Pamata līdzekļu konfigurācija
- Kā inženiertehniskais uzņēmums izveido jaunu tehnisko produktu
- Kā inženiertehniskais uzņēmums izlaid tehnisko produktu vietējam uzņēmumam
- Kā vietējais uzņēmums var pārskatīt un pieņemt produktu, ko tai izlaidis inženiertehniskais uzņēmums
- Kā vietējais uzņēmums var izmantot tehnisko produktu standarta darījumos
- Kā pievienot tehnisko produktu pārdošanas pasūtījumam
- Kā pieprasīt izmaiņas tehniskajā produktā, izveidojot tehnisko izmaiņu pieprasījumu
- Kā ieplānot un ieviest pieprasītās izmaiņas, izveidojot tehnoisko izmaiņu pasūtījumu
- Kā izlaist produktu, kas ir mainīts

Visi šīs tēmas uzdevumi izmanto standarta parauga datus, kas ir sniegti korporācijai Microsoft Dynamics 365 Supply Chain Management. Turklāt katrs uzdevums ir balstīts uz iepriekšējo uzdevumu. Tādēļ mēs iesakām strādāt ar uzdevumiem no sākuma līdz beigām, it īpaši, ja iepriekš nekad neesat izmantojis tehnisko izmaiņu pārvaldības līdzekli. Šādā veidā jūs gūsiet pilnīgu izpratni par šo līdzekli.

## <a name="set-up-for-the-sample-scenario"></a>Iestatiet scenārija paraugu

Lai sekotu parauga scenārijam, kas ir sniegts šajā tēmā, vispirms ir jāsagatavo līdzeklis, padarot demonstrācijas datus pieejamus un pievienojot dažus pielāgotus ierakstus.

Pirms mēģināt veikt kādu no šajā tēmā norādītajiem uzdevumiem, sekojiet instrukcijām visās sekojošajās sadaļās. Šīs apakšsadaļas arī satur vairākas svarīgas iestatījumu lapas, kuras tiks izmantotas, iestatot tehnisko izmaiņu pārvaldību jūsu organizācijai.

### <a name="make-standard-demo-data-available"></a>Padarīt standarta demonstrācijas datus pieejamus

Darbs sistēmā, kur [ir instalēti standarta demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Standarta demonstrācijas dati pievieno datus vairākām demonstrācijas juridiskajām personām (uzņēmumiem un organizācijām). Strādājot ar uzdevumiem, navigācijas joslas labajā pusē ir jāizmanto uzņēmuma atlasītāju, lai pārslēgtos starp vienu uzņēmumu (*DEMF*), kas ir iestatīts kā *inženiertehniskā organizācija* un citu uzņēmumu (*USMF*), kas iestatīts kā *operacionālā organizācija*.

### <a name="set-up-an-engineering-organization"></a>Inženiertehniskās organizācijas iestatīšana

Inženiertehniskajai organizācijai pieder tehniskie dati, un tā ir atbildīga par produktu dizainu un izmaiņām. Lai iestatītu inženiertehnisku organizāciju, veiciet tālāk norādītās darbības.

1. Dodieties uz **Tehniskā izmaiņu pārvaldība &gt; Iestatīšana &gt; Inženiertehniskās organizācijas**.
1. Vēlreiz atlasiet **Jauns**, lai režģim pievienotu rindu, un iestatiet tai šādas vērtības:

    - **Inženiertehniskā organizācija:** *DEMF*
    - **Organizācijas nosaukums:** *Contoso Entertainment System Germany*

    ![Inženiertehniskās organizācijas pievienošana.](media/engineering-org.png "Inženiertehniskās organizācijas pievienošana")

### <a name="set-up-the-version-product-dimension-group"></a>Versijas produktu dimensiju grupas iestatīšana

1. Dodieties uz **Produkta informācijas pārvaldība &gt; Iestatīšana &gt; Dimensijas un variantu grupas &gt; Produktu dimensiju grupas**.
1. Atlasiet **Jauns**, lai izveidotu produktu dimensiju grupu.
1. Iestatiet lauku **Nosaukums** uz *Versija*.
1. Atlasiet **Saglabāt**, lai saglabātu jauno dimensiju un ielādētu vērtības kopsavilkuma cilnē **Produktu dimensijas**.
1. Kopsavilkuma cilnē **Produktu dimensijas** iestatiet **Versija** kā aktīvu produkta dimensiju.

    ![Produkta dimensiju grupas pievienošana.](media/product-dimension-groups.png "Produkta dimensiju grupas pievienošana")

### <a name="set-up-product-lifecycle-states"></a>Produkta dzīves cikla iestatīšana

Ir svarīgi, ka jūs varat kontrolēt, kuri darījumi ir atļauti katram dzīves cikla stāvoklim, jo ​​tehniskā prece iziet tā dzīves ciklu. Lai iestatītu produkta dzīves cikla stāvokļus, veiciet šīs darbības.

1. Dodieties uz **Tehnisko izmaiņu pārvaldība &gt; Iestatīšana &gt; Produkta dzīves cikla stāvoklis**.
1. Vēlreiz atlasiet **Jauns**, lai pievienotu dzīves cikla stāvokli, un iestatiet tai šādas vērtības:

    - **Stāvoklis:** *Operacionāls*
    - **Apraksts:** *Operacionāls*

1. Atlasiet **Saglabāt**, lai saglabātu jauno dzīves cikla stāvokli un ielādētu vērtības kopsavilkuma cilnē **Iespējoti biznesa procesi**.
1. Kopsavilkuma cilnē **Iespējotie biznesa procesi** atlasiet biznesa procesus, kas ir pieejami. Šim piemēram, atstājiet lauku **Politika** iestatītu uz *Iespējots* visiem biznesa procesiem.

    ![Biznesa procesu aktivizēšana dzīves cikla stāvoklī.](media/product-lifecycle-states-1.png "Biznesa procesu aktivizēšana dzīves cikla stāvoklī")

1. Vēlreiz atlasiet **Jauns**, lai pievienotu vēl vienu dzīves cikla stāvokli, un iestatiet tai šādas vērtības:

    - **Stāvoklis:** *Prototips*
    - **Apraksts:** *Prototips*

1. Atlasiet **Saglabāt**, lai saglabātu jauno dzīves cikla stāvokli un ielādētu vērtības kopsavilkuma cilnē **Iespējoti biznesa procesi**.
1. Kopsavilkuma cilnē **Iespējotie biznesa procesi** atlasiet biznesa procesus, kas ir pieejami. Šim piemēram, iestatiet lauku **Politika** uz *Iespējots ar brīdinājumu* visiem biznesa procesiem.

    ![Biznesa procesu aktivizēšana (ar brīdinājumiem) dzīves cikla stāvoklī.](media/product-lifecycle-states-2.png "Biznesa procesu aktivizēšana (ar brīdinājumiem) dzīves cikla stāvoklī")

### <a name="set-up-a-version-number-rule"></a>Versijas numura kārtulas iestatīšana

1. Dodieties uz **Tehnisko izmaiņu pārvaldība &gt; Iestatīšana &gt; Produkta versijas numura kārtula**.
1. Vēlreiz atlasiet **Jauns**, lai pievienotu kārtulu, un iestatiet tai šādas vērtības:

    - **Nosaukums:** *Automātiski*
    - **Numura kārtula:** *Automātiski*
    - **Format** *V-\#\#*

    ![Produkta versijas numura kārtulas pievienošana.](media/version-number-rule.png "Produkta versijas numura kārtulas pievienošana")

### <a name="set-up-a-product-release-policy"></a>Iestatīt produkta izlaides politiku

1. Dodieties uz **Tehnisko izmaiņu pārvaldība &gt; Iestatīšana &gt; Produkta izlaides politikas**.
1. Vēlreiz atlasiet **Jauns**, lai pievienotu izlaides politiku, un iestatiet tai šādas vērtības:

    - **Nosaukums:** *Komponenti*
    - **Apraksts:** *Komponenti*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Produkta veids:** *Elements*
    - **Lietot veidnes:** *Vienmēr*
    - **Aktīvs:** *Jā*

1. Kopsavilkuma cilnē **Visi produkti** atlasiet **Pievienot**, lai pievienotu rindu, un iestatiet tai šādas vērtības:

    - **Uzņēmums:** *DEMF*
    - **Veidnes izlaistais produkts:** *D0006*

1. Atlasiet **Pievienot**, lai pievienotu citu rindu, un iestatiet šādas vērtības:

    - **Uzņēmuma kontu ID:** *USMF*
    - **Veidnes izlaistais produkts:** *D0006*
    - **Saņemt MK:** Atlasiet šo izvēles rūtiņu.
    - **Kopēt MK apstiprināšanu:** Atzīmējiet šo izvēles rūtiņu.
    - **Kopēt MK aktivāciju:** Atzīmējiet šo izvēles rūtiņu.
    - **Saņemt maršrutu:** Atlasiet šo izvēles rūtiņu.
    - **Kopēt maršruta apstiprināšanu:** Atzīmējiet šo izvēles rūtiņu.
    - **Kopēt maršruta aktivāciju:** Atzīmējiet šo izvēles rūtiņu.

    ![Produkta izlaides politikas pievienošana.](media/product-release-policy.png "Produkta izlaides politikas pievienošana")

### <a name="set-up-an-engineering-product-category"></a>Iestatīt tehnisko produktu kategoriju 

Tehnisko produktu kategorijas sniedz pamatu tehnisko produktu izveidei (tas ir, produktu, kas tiek veidoti un kontrolēti, izmantojot tehnisko izmaiņu pārvaldību). Lai iestatītu tehnisko produktu kategorijas, veiciet tālāk norādītās darbības.

1. Dodieties uz **Tehniko izmaiņu pārvaldība &gt; Tehniko produktu kategoriju detalizēta informācija**.
1. Atlasiet **Jauns**, lai izveidotu kategoriju.
1. Kopsavilkuma cilnē **Detalizēta informācija** iestatiet šādas vērtības:

    - **Nosaukums:** *Komponenti*
    - **Inženiertehniskā organizācija:** *DEMF*
    - **Produkta veids:** *Elements*
    - **Izsekošanas versija darījumos:** *Jā*
    - **Produkta dimensiju grupa:** *Versija*
    - **Produktu dzīves cikla stāvoklis izveides laikā:** *Operacionāls*
    - **Versijas numura kārtula:** *Automātiski*
    - **Īstenot efektivitāti:** *Nē*
    - **Izmantot numuru kārtulas nomenklatūru:** *Nē*
    - **Izmantot nosaukuma kārtulas nomenklatūru:** *Nē*
    - **Izmantot apraksta kārtulas nomenklatūru:** *Nē*

1. Kopsavilkuma cilnē **Izlaides politika** iestatiet lauku **Produkta izlaides politika** uz *Komponenti*.
1. Atlasiet **Saglabāt**.

    ![Pievienot tehnisko produktu kategoriju.](media/product-category-details.png "Pievienot tehnisko produktu kategoriju")

### <a name="set-up-product-acceptance-conditions"></a>Iestatīt produktu pieņemšanas nosacījumus

1. Izmantojiet uzņēmuma atlasītāju navigācijas joslas labajā pusē, lai pārslēgtos uz *USMF* juridisko personu (uzņēmums).
1. Dodieties uz **Tehniskā izmaiņu pārvaldība &gt; Iestatīšana &gt; Tehnisko izmaiņu pārvaldības parametri**.
1. Cilnē **Izlaides kontrole** sadaļā **Produktu akceptēšana** iestatiet lauku **Produktu akceptēšana** uz *Manuāli*.

    ![Produktu pieņemšanas nosacījumu iestatīšana.](media/engineering-change-management-parameters.png "Produktu pieņemšanas nosacījumu iestatīšana")

## <a name="create-a-new-engineering-product"></a>Jauna tehniskā produkta izveide

Tehniskais produkts ir produkts, kas darbojas un tiek kontrolēts, izmantojot tehnisko izmaiņu pārvaldību. Citiem vārdiem, var kontrolēt izmaiņas tā dzīves laikā, un izmaiņu informācija tiks saglabāta, izmantojot tehniskos izmaiņu pasūtījumus. Lai izveidotu tehniskos produktus, veiciet tālāk aprakstītās darbības.

1. Pārliecinieties, ka atrodaties savā inženiertehniskās organizācijas juridiskajā personā (*DEMF* šim piemēram). Pēc nepieciešamības izmantojiet uzņēmuma atlasītāju navigācijas joslas labajā pusē.
1. Atvēriet lapu **Izlaistie produkti** veicot vienu no tālāk norādītajām darbībām:

    - Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.
    - Dodieties uz **Tehnisko izmaiņu pārvaldība &gt; Kopējais &gt; Izlaistie produkti**.

1. Darbību rūts grupas **Jauns** cilnē **Produkts** atlasiet **Tehniskais produkts**.
1. Dialoglodziņā **Jauns produkts** iestatiet sekojošus laukus:

    - **Tehnisko produktu kategorija:** *Komponenti*
    - **Produkta numurs:** *Z0001*
    - **Produkta nosaukums:** *Skaļruņu kopa*

    ![Pievienot tehnisko produktu.](media/new-product-dialog.png "Pievienot tehnisko produktu")

    Ņemiet vērā, ka lauks **Versija** tiek automātiski iestatīts, izmantojot produkta versijas numura kārtulu, ko iestatījāt agrāk.

1. Atlasiet **Labi**, lai izveidotu preci un aizvērtu dialoglodziņu.
1. Tiek atvērta jaunā produkta detalizētas informācijas lapa. Ievērojiet, ka dažu lauku, piemēram, **Noliktavas dimensiju grupa**, **Izsekošanas dimensiju grupa** un/vai **Krājumu modeļu grupa**, vērtības jau ir aizpildītas. Šie lauki tika iestatīti automātiski, jo produkts tiek izlaists *DEMF* juridiskajā personā, un tas izmanto produktu izlaides politiku *Komponenti*, kas saistīta ar tehnisko produktu kategoriju *Komponenti*. Tā kā jūs iepriekš izmantojāt krājumu *D0006* kā veidni, lai iestatītu rindas *DEMF* juridiskajai personai, vērtības, kas tika aizpildītas, tika ņemtas no krājuma *D0006*.

    ![Nodoto preču papildinformācija.](media/product-details.png "Nodoto preču papildinformācija")

1. Darbības rūtī, cilnē **Inženieris**, kas atrodas grupā **Tehnisko izmaiņu pārvaldība**, atlasiet **Tehniskās versijas**, lai apskatītu produkta versijas.

    ![Tehniskās versijas.](media/engineering-versions-list.png "Tehniskās versijas")

1. Lapā **Tehniskās versijas** ievērojiet, ka produktam ir tikai viena versija, un tas ir aktīvs.
1. Atlasiet versiju, lai skatītu tās detalizētu informāciju.

    ![Detalizēta informācija par tehnisko versiju.](media/engineering-version-details.png "Detalizēta informācija par tehnisko versiju")

1. Lapā **Tehniskā versija** kopsavilkuma cilnē **Materiālu komplekts** atlasiet **Izveidot MK**.
1. Dialoglodziņā **Izveidot MK** iestatiet tālāk norādītās vērtības:

    - **MK numurs:** Z0001
    - **Nosaukums:** Skaļruņu kopa
    - **Vieta:** 1

    ![BOM izveide.](media/create-bom.png "BOM izveide")

1. Atlasiet **Labi**, lai pievienotu MK un aizvērtu dialoglodziņu.
1. Kopsavilkuma cilnē **Materiālu komplekts** atlasiet **Materiāla komplekts**.
1. Lapā **Materiālu komplekts** kopsavilkuma cilnē **Materiālu komplekta rindas** pievienojiet trīs rindas, pa vienai krājuma numuriem *D0001*, *D0003* un *D0006*.

    ![MK rindu pievienošana.](media/bom.png "MK rindu pievienošana")

1. Atlasiet **Saglabāt**.
1. Aizvērt lapu.
1. Lapā **Tehniskā versija** kopsavilkuma cilnē **Materiālu komplekts** atlasiet **Apstiprināt**.
1. Parādītajā dialoglodziņā atlasiet **Labi**.

    ![MK apstiprināšana.](media/approve-dialog.png "MK apstiprināšana")

1. Lapā **Tehniskā versija** kopsavilkuma cilnē **Materiālu komplekts** atlasiet **Aktivizēt**.
1. Ievērojiet, ka MK ir atzīmētas izvēles rūtiņas **Aktīvais** un **Apstiprinātais**.

    ![Aktīvais un apstiprinātais MK.](media/approved-bom.png "Aktīvais un apstiprinātais MK")

1. Aizvērt lapu.

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a>Izlaist tehnisko produktu vietējam uzņēmumam

Produkts tagad ir izstrādāts, izmantojot inženierzinātņu nodaļu. Šim piemēram produkts ir prototips, kas ir projektēts klientam. Tā kā klients ir *USMF* juridiskās personas klients, produkts ir jānodod šai juridiskajai personai.

1. Uzturēt juridisko personu iestatītu uz *DEMF*. (Pēc nepieciešamības izmantojiet uzņēmuma atlasītāju navigācijas joslas labajā pusē.)
1. Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.
1. Atlasiet produktu *Z0001*.
1. Darbības rūtī, cilnē **Produkts** grupā **Uzturēt** atlasiet **Izlaist produkta struktūru**, lai atvērtu vedni **Izlaist produktus**.
1. Lapā **Atlasīt tehniskos produktus izlaišanai**, atzīmējiet izvēles rūtiņu **Atlasīt** produktam *Z0001*.

    ![Izvēloties tehniskos produktus izlaišanai.](media/select-eng-product-to-release.png "Izvēloties tehniskos produktus izlaišanai")

1. Atlasiet **Informācija par laidienu**.
1. Tiek parādīta lapa **Produkta izlaides informācija**, kur varat pārskatīt informāciju par produktu, kas tiks izlaists, un tā produkta struktūru. Ievērojiet, ka opcija **Nosūtīt MK** ir iestatīta uz *Jā*. Tāpēc tiks izlaistas gan produkts *Z0001*, gan visi tā atvasinātie krājumi no MK.

    Kreisajā rūtī varat atlasīt jebkuru atvasinātu vienumu, lai pārskatītu tā detaļas. Ja kādam atvasinātam krājumam ir MK, varat arī izvēlēties, lai tiktu izlaists šī atvasinātā krājuma MK.

    ![Preču izlaides detalizētas informācijas pārskatīšana.](media/product-release-details.png "Preču izlaides detalizētas informācijas pārskatīšana")

1. Aizveriet lapu, lai atgrieztos pie vedņa **Izlaist produktus**.
1. Atlasiet **Tālāk**, lai atvērtu lapu **Atlasīt produktus izlaišanai**. Ja esat atlasījis visus standarta (ne tehniskos) produktus, tie parādīsies šajā lapā. Ievērojiet, ka, izlaižot standarta produktu, atlasot **Izlaist produkta struktūru**, tiek izlaisti arī tās MK un maršruts.

    ![Izvēloties standarta produktus izlaišanai.](media/select-std-product-to-release.png "Izvēloties standarta produktus izlaišanai")

1. Atlasiet **Tālāk**, lai atvērtu lapu **Atlasīt produktu variantus izlaišanai**. Šajā piemērā nav neviena varianta.
1. Atlasiet **Tālāk**, lai atvērtu lapu **Atlasīt uzņēmumus**.
1. Atlasiet uzņēmumus, kam produkts ir jāizlaiž. Šajā piemērā atlasiet **USMF** izvēles rūtiņu.

    ![To uzņēmumu izvēle, kuros jāizlaiž.](media/select-release-companies.png "To uzņēmumu izvēle, kuros jāizlaiž")

1. Atlasiet **Tālāk**, lai atvērtu lapu **Apstiprināt atlasi**.
1. Atl. **Pabeigt**.

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a>Pārskatiet un akceptējiet produktu, pirms to izlaidīsiet vietējā uzņēmumā

Tehniskā nodaļa tagad ir laidusi klajā šo informāciju vietējiem uzņēmumiem, kuros tiks izmantots produkts. Šajā piemērā lokāls uzņēmums ir *USMF*.

Tā kā lauks **Produktu apstiprināšana** ir iestatīts uz *Manuāli* lapā **Tehnisko izmaiņu pārvaldības parametri** uzņēmumam *USMF*, produkti ir jāpieņem manuāli, pirms tie tiek izlaisti šim uzņēmumam. Citiem vārdiem, tie ir jāpārskata un jāapstiprina, pirms tie kļūst par izlaistiem produktiem.

Lai pārskatītu produktu un to izlaistu *USMF* uzņēmumā, sekojiet šīm darbībām.

1. Iestatiet juridisko personu uz *USMF*. (Izmantojiet uzņēmuma atlasītāju navigācijas joslas labajā pusē.)
1. Dodieties uz **Tehnisko izmaiņu pārvaldība &gt; Kopējais &gt; Produktu laidieni &gt; Atvērtie produktu laidieni**.

    Lapa **Atvērtie produktu laidieni** parāda produktu *Z0001*, kuram ir statuss *Gaida pieņemšanu*.

    ![Atvērt preču laidienus.](media/open-product-releases.png "Atvērt preču laidienus")

1. Atlasiet vērtību kolonnā **Produkta numurs**, lai atvērtu lapu **Produkta izlaides informācija**. Pievērsiet uzmanību šādām detaļām:

    - Kopsavilkuma cilnē **Vispārēji** tiek parādīta informācija par produkta izlaišanu, piemēram, izlaides uzņēmumu (*DEMF* šim piemēram), izlaišanas vietu (*1*) un saņemšanas vietu (*1*). Tā kā vednī **Izlaides produkti** netika norādīta saņemšanas vieta, izlaišanas vietas vērtība tiek kopēta uz saņemšanas vietu.
    - Kopsavilkuma cilne **Detalizēta informācija par laidienu** rāda informāciju par produktu un versiju, kas tika izlaista. Šeit var modificēt tādus iestatījumus kā, piemēram, efektivitātes datumus.
    - Kopsavilkuma cilne **Maršruts** rāda produkta maršrutu. Tomēr šim piemēram, jūs neizlaižāt maršrutus.

    ![Preces izlaišanas informācija.](media/product-release-details-2.png "Preces izlaišanas informācija")

1. Kad esat beidzis pārskatīt informāciju, esat gatavs pieņemt produktu un šādā veidā to izlaist *USMF* uzņēmumā. Darbību rūtī atlasiet **Darbības &gt; Pieņemt**.
1. Produkts tagad ir izlaists *USMF* uzņēmumā. Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt;Produkti &gt; Izlaistie produkti**. Ir jāredz krājumu *Z0001*.

## <a name="use-the-product-in-transactions-in-the-local-company"></a>Izmantot produktu darījumos vietējā uzņēmumā

Uzņēmuma *USMF* pamatdatu pārvaldnieks vēlas pārliecināties, vai produkts ir stāvoklī *Prototips*, lai nodrošinātu, ka lietotāji tiks brīdināti, ja nejauši pievieno to procesiem, kuros tie strādā.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.
1. Atlasiet produktu *Z0001*, lai atvērtu tā informācijas lapu. (Šo filtru var izmantot, lai atrastu produktu.)
1. Darbību rūtī cilnē **Inženieris** grupā **Tehnisko izmaiņu pārvaldība** atlasiet **Tehniskās versijas**.
1. Lapā **Tehniskās versijas** atlasiet versijas numuru *V-01*, lai atvērtu tā informācijas lapu.
1. Darbību rūts grupas **Dzīves cikla stāvoklis** cilnē **Produkts** atlasiet **Mainīt dzīves cikla stāvokli**.
1. Nolaižamajā dialoglodziņā **Mainīt dzīves cikla stāvokli** iestatiet lauku **Stāvoklis** uz *Prototips* un pēc tam atlasiet **Labi**.

    ![Dzīves cikla stāvokļa maiņa.](media/change-lifecycle-state.png "Dzīves cikla stāvokļa maiņa")

## <a name="add-the-engineering-product-to-a-sales-order"></a>Pievienot tehnisko produktu pārdošanas pasūtījumam

Produktu tagad var pārdot klientam. Lai pievienotu produktu pārdošanas pasūtījumam, rīkojieties šādi.

1. Dodieties uz **Pārdošana un mārketings &gt; Pārdošanas pasūtījumi &gt; Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Pārdošanas pasūtījuma izveide** iestatiet lauku **Klienta konts** uz *US-0002* un pēc tam atlasiet **Labi**.
1. Jaunais pārdošanas pasūtījums ir atvērts. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet rindu un iestatiet tai lauku **Krājuma numurs** uz *Z000*.
1. Darbību rūtī atlasiet **Saglabāt**.

    Jūs saņemat brīdinājuma ziņojumu, kas informē, ka krājumam ir statuss *Prototips*. Tomēr, tā kā ziņojums ir tikai brīdinājums, pārdošanas pasūtījums joprojām ir izveidots.

    ![Tehniskā produkta pārdošanas pasūtījums.](media/sales-order-eng-product.png "Tehniskā produkta pārdošanas pasūtījums")

## <a name="request-changes-in-the-engineering-product"></a>Pieprasīt izmaiņas tehniskajā produktā

Produkts tika nosūtīts klientam, bet klients nav pilnībā apmierināts un sniedz atsauksmes, kas ietver uzlabojumu ieteikumus. Kamēr klients sarunājas ar pārdevēju pa telefonu, pārdevējs var pieprasīt izmaiņas, kuras klients apraksta.

1. Dodieties uz **Pārdošana un mārketings &gt; Pārdošanas pasūtījumi &gt; Visi pārdošanas pasūtījumi**.
1. Meklējiet un atveriet pārdošanas pasūtījumu, ko izveidojāt iepriekšējā uzdevumā.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Tehnisko izmaiņu pārvaldība &gt; Jauns tehnisko izmaiņu pieprasījums**.

    ![Tehnisko izmaiņu pieprasījuma izveide no pārdošanas pasūtījuma.](media/sales-order-eng-change-request.png "Tehnisko izmaiņu pieprasījuma izveide no pārdošanas pasūtījuma")

1. Aizpildiet tehnisko izmaiņu pieprasījumu, pamatojoties uz klienta atsauksmēm. Šajā piemērā iestatiet šādas vērtības:

    - **Izmainīt pieprasījumu:** *555*
    - **Nosaukums:** *Z0001 klienta maiņa*
    - **Prioritāte:** *zema*
    - **Kategorija:** iestatīt izmaiņas
    - **Stingrība:** *Vidēja*

1. Kopsavilkuma cilnē **Informācija** atlasiet **Jauna &gt; Piezīme**, lai pievienotu režģim piezīmi.
1. Jaunas piezīmes laukā **Apraksts** norādiet, ka krājumu *D0003* ir jādzēš no MK. Ja ir jāpievieno papildu informācija par šo piezīmi, varat ievadīt tekstu laukā **Piezīmes**.

    ![Tehnisku izmaiņu pieprasījums.](media/eng-change-request.png "Tehnisku izmaiņu pieprasījums")

1. Darbību rūtī atlasiet **Saglabāt**.
1. Ievērojiet, ka krājums ir automātiski pievienots kopsavilkuma cilnei **Produkti** un ka tehnisko izmaiņu pieprasījuma (pārdošanas pasūtījuma) avots ir pievienots kopsavilkuma cilnē **Avots**.

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a>Veikt izmaiņas produktā, izmantojot tehnisko izmaiņu pasūtījumu

Pārdevējs zina, ka produkts ir svarīgs un tika izstrādāts īpaši klientam. Tādēļ pārdevējs aicina inženieri *DEMF* uzņēmumā, lai paziņotu par izmaiņu pieprasījumu. Šādā veidā inženieris var paātrināt procesu.

Inženieris tagad pārskata klienta pieprasījumu un izveido produkta izmaiņu pasūtījumu.

1. Tā kā inženieris strādā *DEMF* uzņēmumā, iestatiet juridisko personu kā *DEMF*. (Izmantojiet uzņēmuma atlasītāju navigācijas joslas labajā pusē.)
1. Dodieties uz **Tehnisko izmaiņu pārvaldība &gt; Kopējais &gt; Tehnisko izmaiņu pieprasījumi**.
1. Atvērt izmaiņu pieprasījumu: *555*.
1. Pārskatiet informāciju un pēc tam apstipriniet izmaiņas. Darbību rūtī cilnē **Izmaiņu pieprasījums** grupā **Maiņas statuss** atlasiet **Apstiprināt**.
1. Dodieties uz **Tehnisko izmaiņu pārvaldība &gt; Kopējais &gt; Tehnisko izmaiņu pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu izmaiņu pasūtījumu, un iestatiet šādas vērtības:

    - **Izmaiņu pasūtījums:** *555*
    - **Nosaukums:** *Z0001 klienta maiņa*
    - **Kategorija:** *Klienta maiņa*
    - **Prioritāte:** *Zema*
    - **Stingrība:** *Vidēja*

1. Kopsavilkuma cilnē **Ietekmētie produkti** atlasiet **Jauns &gt; Pievienot esošu produktu**, lai pievienotu rindu režģim, un iestatiet tai šādas vērtības:

    - **Produkts:** *Z0001*
    - **Ietekme:** *Jauna versija*

    ![Tehnisko izmaiņu pasūtījuma izveide.](media/eng-change-order.png "Tehnisko izmaiņu pasūtījuma izveide")

1. Ievērojiet, ka, tā kā lauks **Ietekme** tiek iestatīts uz *Jauna versija*, lauks **Jauna versija** kopsavilkuma cilnes **Informācija par produktu** cilnē **Detalizēta informācija** rāda, kāds būs jaunais versijas numurs (*V-02* šim piemēram).

    ![Informācija par produktu tehnisko izmaiņu pasūtījumam.](media/eng-change-order-product-details.png "Informācija par produktu tehnisko izmaiņu pasūtījumam")

1. Darbību rūtī atlasiet **Saglabāt**.
1. Kopsavilkuma cilnā **Informācija par produktu**, kas atrodas cilnē **Materiālu komplekts**, atlasiet **Rindas**, lai atvērtu MK versijai *V-01* produktam *Z0001*.

    ![Tehnisko produktu MK rindas.](media/eng-product-bom-lines.png "Tehnisko produktu MK rindas")

1. Atlasiet rindu krājuma numuram *D0003* un pēc tam darbību rūtī atlasiet **Dzēst**. Lauka **Izmaiņu veids** vērtība šai rindai mainās uz *Dzēsts*.
1. Darbību rūtī atlasiet **Saglabāt**.

    ![Modificētas tehniskā produkta MK rindas.](media/eng-product-bom-lines-modified.png "Modificētas tehniskā produkta MK rindas")

1. Aizveriet lapu **MK rinda**, lai atgrieztos lapā **Tehnisko izmaiņu pasūtījums**.
1. Kopsavilkuma cilnē **Informācija par produktu** cilnē **Materiālu komplekts** ievērojiet, ka lauka **Izmaiņu veids** MK vērtība *Z0001* tagad ir *Mainīta*.

    ![Tehnisko izmaiņu pasūtījums, kas ietver mainītu MK.](media/eng-change-order-changed-bom.png "Tehnisko izmaiņu pasūtījums, kas ietver mainītu MK")

    Lai izmaiņas varētu apstrādāt, pasūtījums ir jāapstiprina. Kad izmaiņas tiek apstrādātas, produkti tiek atjaunināti ar izmaiņām, kas iekļautas tehnisko izmaiņu pasūtījumā. Šajā piemērā persona, kas izveido tehnisko izmaiņu pasūtījumu, ir norādīta kā apstiprinātājs.

1. Darbību rūtī cilnē **Izmaiņu pasūtījums** grupā **Maiņas statuss** atlasiet **Apstiprināt**.
1. Atlasiet **Process**, lai atjauninātu produkta informāciju.

## <a name="release-the-changed-product"></a>Izlaist mainīto produktu

Produktu tagad var izlaist atkārtoti *USMF* uzņēmumam un pēc tam to var nosūtīt klientam. Lai izlaistu produktu tieši no tehnisko izmaiņu pasūtījuma, veiciet šīs darbības.

1. Atvērt iepriekšējā vingrinājumā izveidoto tehnisko izmaiņu pasūtījumu, ja tas vēl nav atvērts.
1. Darbību rūtī cilnē **Izmaiņu pasūtījums** grupā **Produkta laidieni** atlasiet **Meklēt**.
1. Meklēšanas rezultāti rāda, kuriem uzņēmumiem ir nodotas ietekmētos produktus. Aizvērt meklēšanas rezultātus.
1. Darbību rūts cilnē **Mainīt pasūtījumu** grupā **Produktu laidieni** atlasiet **Skatīt**,lai atvērtu dialoglodziņu **Laidieni**, kur var apskatīt iepriekšējās meklēšanas rezultātus.
1. Atlasiet katru uzņēmumu, kuram vēlaties nodot produktus.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Laidieni** un atgriezieties izmaiņu pasūtījumā.
1. Darbības rūtī, cilnē **Mainīt pasūtījumu**, grupā **Produktu laidieni** atlasiet **Process**, lai izlaistu ietekmētos produktus atlasītajiem uzņēmumiem. Varat arī atlasīt **Izlaist produkta struktūru**, lai sāktu laidiena procesu.

## <a name="complete-the-change-order"></a>Pabeigt izmaiņu pasūtījumu

Lai atzīmētu izmaiņu pasūtījumu kā pabeigtu, kas norāda, ka turpmākas darbības netiek saglabātas, darbību rūtī atlasiet **Pabeigt**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
