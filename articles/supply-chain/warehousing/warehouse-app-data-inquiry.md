---
title: Vaicājumu dati, izmantojot noliktavas pārvaldības mobilās programmas datus
description: Šajā rakstā ir aprakstīts, kā konfigurēt datu pieprasījuma mobilās ierīces izvēlnes vienumus un izmantot tos kā daļu no atvēsēm.
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cc013e962b4da803764f16e451b1d433666e75c2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336611"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Vaicājumu dati, izmantojot noliktavas pārvaldības mobilās programmas datus

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Līdzekļu ievads

Nodrošinot svītrkoda skenēšanas iespēju, mobilā programma Noliktavas pārvaldība ļauj jums viegli un precīzi iegūt datus, kā daļu no noliktavas procesiem. Tomēr dažkārt svītrkodi tiek bojāti un kļūst nelasāmi, vai arī pieprasītā datu informācija var nebūt kā svītrkods biznesa procesu plūsmās. Šādos gadījumos datu manuāla ievade var aizņemt ilgāku laiku un var pat izraisīt nepareizu datu tveršanu. Rezultāti var samazināt spēkāspēju un zemāku pakalpojuma līmeni.

Izmantojot elastīgu datu uzziņu procesu, darbinieki var viegli atrast nepieciešamo informāciju kā daļu no iegultajām mobilās programmas noliktavas pārvaldībai un izmantot filtrēšanas opcijas, lai būtu redzami tikai attiecīgie dati. Tāpēc manuāla atlase ir ātrāka un precīzāka.

Piemēram, pirkšanas pasūtījuma saņemšanas plūsmā ir nepieciešams pirkšanas pasūtījuma numurs, lai saskaņotu saņemšanas krājumu. Kā daļu no šī procesa jūs viegli varat konfigurēt izvēlnes elementus, lai sniegtu karšu saraksta skatījumu par atbilstošajiem pirkšanas pasūtījumu numuriem. Šādā veidā varat turpināt saņemšanas plūsmu, izmantojot ātro pieeju ''atlasīt'. Šajā rakstā ir sniegti piemēru scenāriji, taču funkcionalitāti var izmantot arī jebkurā vai visās jūsu noliktavas pārvaldības mobilās programmas plūsmās.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>Ieslēgt datu uzziņu plūsmas līdzekli un tā priekšnosacījumus

Pirms varat lietot šajā rakstā aprakstīto funkcionalitāti, ir jāveic tālāk norādītās darbības, lai ieslēgtu nepieciešamās funkcijas.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**. (Plašāku informāciju par to, kā izmantot **Līdzekļu pārvaldības darbvieta**, skatiet Līdzekļu [pārvaldības pārskatu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Ja jūs darbojaties Piegādes ķēdes pārvaldības versija 10.0.28 vai agrāk, grieziet līdzekli, kas uzskaitīts šādā veidā:

    - **Modulis:** *Noliktavas pārvaldība*
    - **Līdzekļa nosaukums:** *Programmas Warehouse darbību norādījumi*

    Šis līdzeklis ir priekšnosacījums noliktavas *pārvaldības programmas datu pieprasījumu plūsmas līdzeklim*. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 tas ir obligāts un to nevar izslēgt. Papildinformāciju par līdzekli *Warehouse programmas darbību norādījumi* skatiet sadaļā [Warehouse Management mobilās lietojumprogrammas darbību nosaukumu pielāgošana un instrukcijas](mobile-app-titles-instructions.md).

1. Slēdziet funkciju, kas ir uzskaitīta šādā veidā:

    - **Modulis:** *Noliktavas pārvaldība*
    - **Līdzekļa nosaukums:** *Warehouse management programmas novirzīšana*

    Šis līdzeklis ir priekšnosacījums noliktavas *pārvaldības programmas datu pieprasījumu plūsmas līdzeklim*. No Piegādes ķēdes pārvaldības versijas 10.0.29 tas ir ieslēgts pēc noklusējuma. Papildinformāciju par noliktavas *pārvaldības programmas de galapunktu* līdzekli skatiet sadaļā [Dimensiju konfigurēšana darbībām mobilās ierīces izvēlnes vienumos](warehouse-app-detours.md).

1. Ja noliktavas *pārvaldības programmas atšifrējumu līdzeklis vēl nebija ieslēgts, atjauniniet lauku nosaukumus mobilajā programmā Noliktavas pārvaldība,* **\>\>\>** noklikšķinot uz Noliktavas pārvaldības iestatījuma mobilās **ierīces programmas lauku nosaukumi un atlasot Izveidot noklusējuma iestatījumus.** Atkārtojiet šo darbību katrai juridiskajai personai (uzņēmumam), kas izmanto mobilo programmu Noliktavas pārvaldība. Lai iegūtu vairāk informācijas, skatiet [Konfigurēt laukus programmai Warehouse Management mobile](configure-app-field-names-priorities-warehouse.md).
1. Slēdziet funkciju, kas ir uzskaitīta šādā veidā:

    - **Modulis:** *Noliktavas pārvaldība*
    - **Līdzekļu nosaukums:** *noliktavas pārvaldības programmas datu pieprasījumu plūsma*

    Šī funkcija ir tā, kas ir aprakstīta šajā rakstā.

## <a name="example-scenarios"></a>Piemēra situācijas

Šajā rakstā tiek izmantoti piemēru scenāriji, *lai parādītu, kā varat izmantot noliktavas pārvaldības programmas datu uzziņu plūsmas* līdzekli, lai uzlabotu pirkšanas ieejas plūsmu. Scenārijos tiek lietoti standarta parauga dati, kas ietver plūsmu ar nosaukumu "Pirkšanas *saņemšana"*. Šī plūsma sākas, jautājot darbiniekiem noteikt pirkšanas pasūtījuma numuru, kam viņi saņems. Lai palīdzētu darbiniekiem vieglāk identificēt pirkšanas pasūtījumu, jūs paaugstināsiet plūsmas pirmo lapu, kā atšifrējumu pievienojot šādas jaunas [vaicājuma opcijas](warehouse-app-detours.md):

- **Uzmeklē PO pēc kreditora** - atveriet lapu, kurā darbiniekiem tiek parādīta uzvedne ar aicinājumu ievadīt kreditora nosaukumu vai daļu no kreditora nosaukuma. Var izmantot aizstājējzīmes. Piemēram, ja darbinieks gaida ienākošo piegādi šodien no kreditora, *kura nosaukumā ir iekļauts Saišu zars, viņi var ievadīt Informāciju par Dāvanu* karti, **lai apskatītu karšu kopu atvērtiem pirkšanas pasūtījumiem, kuros iekļauts\*** šis teksts. Katrai kartei ir vairāki lauki, kas sniedz informāciju par katru pirkšanas pasūtījumu. Papildus kreditora nosaukumam ir iespējams izveidot kartes tā, lai tām tiktu rādīts kreditora konta numurs, piegādes datums un dokumenta statuss.
- **Uzmeklēt PO šodienai** — atvērt lapu, kurā darbiniekiem nav jāievada dati, bet gan iepriekš konfigurēti filtri (piemēram, šodienas datums). Pēc tam lapā ir parādīta karšu kopa, kas atbilst filtram. Darbinieki turpina darbu, atlasot pirkšanas pasūtījuma karti, kurā viņi vēlas reģistrēt krājuma vienības.
- **Uzmeklēt PO pēc krājuma** — atvērt lapu, kurā darbiniekiem tiek parādīta uzvedne ar aicinājumu skenēt saņemtajā krājumos esošo krājumu svītrkodu. Pēc tam plūsma uzskaita visus atvērtos pirkšanas pasūtījumus, kas satur skenētā preces numura rindas. Lai segtu situācijas, kad svītrkodu nevar lasīt, šai lapai varat pievienot citu pārlūkošanu, kas ļauj darbiniekiem meklēt krājumu numurus noteiktā pirkšanas pasūtījumā.

Katrā gadījumā darbinieks identificē pirkšanas pasūtījumu, atlasot karti, un pēc tam tiek atgriezts pirmajā lapā, kurā parādīts atlasītais pirkšanas pasūtījuma numurs. Darbinieks pēc tam var turpināt ienākošo krājumu krājumu reģistrācijas plūsmu.

## <a name="enable-sample-data"></a>Iespējot datu paraugu

Lai strādātu caur šajā rakstā aprakstītajiem piemēra scenārijiem, jums jāatrodas sistēmā, kurā ir instalēti [standarta demonstrācijas](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) dati. Turklāt pirms sākšanas jāatlasa *USMF* juridiskā persona (uzņēmums).

## <a name="configure-the-mobile-device-menu-items"></a>Konfigurēt mobilās ierīces izvēlnes vienumus

Lai izveidotu katru no jaunajām vaicājuma opcijām, kas ir jāpievieno plūsmas pirmajai lapai, tā ir jāiestata kā mobilās ierīces izvēlnes vienums. Vēlāk vaicājuma opcijas kļūs pieejamas kā pirkšanas *saņemšanas plūsmas atšifrējums*.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>Izveidot izvēlnes elementu "Uzmeklt PO pēc kreditora"

Izveidojiet **POS uzmeklšanu pēc kreditora izvēlnes** elementa, veicot šādas darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbību rūtī atlasiet Jauns, lai **pievienotu** mobilās ierīces izvēlnes vienumu.
1. Iestatiet šādas vērtības jaunajam izvēlnes elementam:

    - **Izvēlnes krājuma nosaukums:** *POS uzmeklē pēc kreditora*
    - **Nosaukums:** *pa kreditoriem uzmeklējamie PO*
    - **Režīms:** *Netiešs*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Aktivitātes kods:** *datu pieprasījums*
    - **Izmantojiet procesa ceļvedi: Jā** *·* (Šī vērtība tiek atlasīta automātiski.)
    - **Tabulas nosaukums:** *PurchTable* (jūs vēlaties meklēt pirkšanas pasūtījumu numurus no šīs tabulas.)

1. Darbību rūtī atlasiet vaicājumu Labot **, lai** definētu vaicājumu, kura pamatā ir atlasītā pamatta tabula (šajā gadījumā tā ir pirkšanas pasūtījumu tabula).
1. Vaicājuma redaktorā cilnē Diapazons **režģim** pievienojiet šādas rindas.

    | Tabula | Atveidotā tabula | Lauks | Kritēriji |
    |---|---|---|---|
    | Pirkšanas pasūtījumi | Pirkšanas pasūtījumi | Pirkšanas pasūtījuma statuss | Atvērts pasūtījums |
    | Pirkšanas pasūtījumi | Pirkšanas pasūtījumi | Piegādes datums | (dayRange(-10,10)) |
    | Pirkšanas pasūtījumi | Pirkšanas pasūtījumi | Kreditora nosaukums | |

1. Atlasiet **Labi**.

    Šajā piemērā jaunais izvēlnes vienums ir konfigurēts, lai atrastu atvērtus pirkšanas pasūtījumus, kurus paredzēts saņemt jebkurā laikā no 10 dienām pēdējās un 10 dienās nākotnē.

    Vaicājumā kolonna Kritēriji kreditora **nosaukumam** *ir* atstāta tukša. Tāpēc darbinieki varēs norādīt šo vērtību, kamēr viņi izmanto mobilo programmu Noliktavas pārvaldība.

    Ja vēlaties norādīt, kā saraksts tiks kārtots, kārtošanu var iestatīt cilnē **Kārtošana**.

1. Papildus vaicājuma definēšanai ir jāatlasa, kuri lauki tiks rādīti kartēs pieprasījumu saraksta lapā. Tāpēc Darbību rūtī atlasiet lauku **sarakstu**.
1. Saraksta lapā **Lauks** iestatiet šādas vērtības:

    - **1. rādīšanas lauks:** *PurchId* (šis lauks tiks rādīts kā katras kartes virsraksts.)
    - **2. rādīšanas lauks:** *PurchStatus*
    - **3. rādīšanas lauks:** *PurchName*
    - **4. rādīšanas lauks:** *OrderAccount*
    - **5. rādīšanas lauks:** *DeliveryDate*
    - **6. rādīšanas lauks:** *displayDocumentStatus()* (šī vērtība ir attēlošanas metode, ko beigās norāda "()".)

1. Darbību rūtī atlasiet **Saglabāt**. Tad aizveriet lapu.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>Izveidot izvēlnes elementu "Uzmeklt PO šodienai"

Izveidojiet **POS uzmeklē šodienas izvēlnes** elementu, izpildot šādas darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbību rūtī atlasiet Jauns, lai **pievienotu** mobilās ierīces izvēlnes vienumu.
1. Iestatiet šādas vērtības jaunajam krājumam:

    - **Izvēlnes vienuma nosaukums:** *uzmeklt POS šodienai*
    - **Nosaukums:** *uzmeklt PO šodien*
    - **Režīms:** *Netiešs*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Aktivitātes kods:** *datu pieprasījums*
    - **Izmantojiet procesa ceļvedi: Jā** *·* (Šī vērtība tiek atlasīta automātiski.)
    - **Tabulas nosaukums:** *PurchTable* (jūs vēlaties meklēt pirkšanas pasūtījumu numurus no šīs tabulas.)

1. Darbību rūtī atlasiet vaicājumu Labot **, lai** definētu vaicājumu, kura pamatā ir atlasītā pamatta tabula (šajā gadījumā tā ir pirkšanas pasūtījumu tabula).
1. Vaicājuma redaktorā cilnē Diapazons **režģim** pievienojiet šādas rindas.

    | Tabula | Atveidotā tabula | Lauks | Kritēriji |
    |---|---|---|---|
    | Pirkšanas pasūtījums | Pirkšanas pasūtījums | Pirkšanas pasūtījuma statuss | Atvērts pasūtījums |
    | Pirkšanas pasūtījums | Pirkšanas pasūtījums | Piegādes datums | (Diena(0)) |

1. Atlasiet **Labi**.

    Šajā piemērā jaunais izvēlnes elements ir konfigurēts, lai atrastu atvērtus pirkšanas pasūtījumus, ko plānots saņemt šodien.

    Ja vēlaties norādīt, kā saraksts tiks kārtots, kārtošanu var iestatīt cilnē **Kārtošana**.

1. Papildus vaicājuma definēšanai ir jāatlasa, kuri lauki tiks rādīti kartēs pieprasījumu saraksta lapā. Tāpēc Darbību rūtī atlasiet lauku **sarakstu**.
1. Saraksta lapā **Lauks** iestatiet šādas vērtības:

    - **Ekrāna lauks 1:** *PurchName* (šis lauks tiks rādīts kā katras kartes virsraksts.)
    - **2. rādīšanas lauks:** *PurchId*
    - **3. rādīšanas lauks:** *PurchStatus*
    - **Parādīt 4. lauku:** *DlvMode*
    - **Ekrāna lauks 5:** *DlvTerm*
    - **Parādīt 6. lauku:** *OrderAccount*
    - **7. rādīšanas lauks:** *VendorName()* (šī vērtība ir rādīšanas metode, jo beigās tiek norādīts "()".)

1. Darbību rūtī atlasiet **Saglabāt**. Tad aizveriet lapu.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>Izveidot izvēlnes elementu "Uzmeklt PO pēc vienuma"

Izveidojiet **POS uzmeklšanu pēc krājuma izvēlnes** elementa, veicot šādas darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbību rūtī atlasiet Jauns, lai **pievienotu** mobilās ierīces izvēlnes vienumu.
1. Iestatiet šādas vērtības jaunajam krājumam:

    - **Izvēlnes vienuma nosaukums:** *POs uzmeklē pēc krājuma*
    - **Nosaukums:** *POs uzmeklē pēc krājuma*
    - **Režīms:** *Netiešs*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Aktivitātes kods:** *datu pieprasījums*
    - **Izmantojiet procesa ceļvedi: Jā** *·* (Šī vērtība tiek atlasīta automātiski.)
    - **Tabulas nosaukums:** *PurchLine* (jūs vēlaties meklēt pirkšanas pasūtījuma numurus, pamatojoties uz krājuma kodu, izmantojot rindas datus.)

1. Darbību rūtī atlasiet Labot vaicājumu, lai definētu vaicājumu, kas balstīts uz atlasīto pamattabulu (šajā gadījumā pirkšanas pasūtījuma rindu tabulu, bet var izmantot jebkuru no vērtībām, **kas** saistītas ar virsrakstu, savienojoties *ar PurchTable*).
1. Vaicājuma redaktorā cilnē Diapazons **režģim** pievienojiet šādas rindas.

    | Tabula | Atveidotā tabula | Lauks | Kritēriji |
    |---|---|---|---|
    | Pirkšanas pasūtījuma rindas | Pirkšanas pasūtījuma rindas | Rindas statuss | Atvērts pasūtījums |
    | Pirkšanas pasūtījuma rindas | Pirkšanas pasūtījuma rindas | Piegādes datums | (dayRange(-10,10)) |
    | Pirkšanas pasūtījuma rindas | Pirkšanas pasūtījuma rindas | Krājuma numurs | |

1. Atlasiet **Labi**.

    Šajā piemērā jaunais izvēlnes vienums ir konfigurēts, lai atrastu atvērtas pirkšanas pasūtījuma rindas, kam paredzams, ka tas būs jāierodas laikā no 10 dienām pēdējās un 10 dienās nākotnē.

    Vaicājumā krājuma numura **kolonna** Kritēriji *ir atstāta* tukša. Tādēļ darbinieki varēs norādīt šo vērtību, kamēr viņi izmanto mobilo programmu Noliktavas pārvaldība.

    Ja vēlaties norādīt, kā saraksts tiks kārtots, kārtošanu var iestatīt cilnē **Kārtošana**.

1. Papildus vaicājuma definēšanai ir jāatlasa, kuri lauki tiks rādīti kartēs pieprasījumu saraksta lapā. Tāpēc Darbību rūtī atlasiet lauku **sarakstu**.
1. Saraksta lapā **Lauks** iestatiet šādas vērtības:

    - **1. rādīšanas lauks:** *PurchId* (šī lauka vērtība tiks izmantota kā katras kartes galvene.)
    - **2. rādīšanas lauks:** *VendAccount*
    - **3. rādīšanas lauks:** *PurchQty*
    - **4. rādīšanas lauks:** *PurchUnit*
    - **5. rādīšanas lauks:** *PurchStatus*

1. Darbību rūtī atlasiet **Saglabāt**. Tad aizveriet lapu.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>Pievienot izvēlnei jaunus mobilās ierīces izvēlnes vienumus

Trīs jauni mobilās ierīces izvēlnes vienumi ir gatavi pievienošanai mobilās ierīces izvēlnei. Šis uzdevums ir jāpabeidz pirms izvēlnes elementu lietošanas kā daļa no atstšanas procesa. Šajā piemērā izveidosit jaunu apakšizvēlni un tai pievienos jaunus izvēlnes elementus.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
1. Darbību rūtī atlasiet **Jauns**.
1. Iestatiet jaunas ieraksta virsrakstā šādas vērtības:

    - **Nosaukums:** *uzziņas*
    - **Apraksts:** *uzziņas*

1. Sarakstā Pieejamās **izvēlnes un izvēlnes vienumi** atlasiet pirmo no tikko izveidotiem mobilās ierīces izvēlnes vienumiem. Pēc tam atlasiet labās bultiņas pogu, lai pārvietotu elementu uz sarakstu **Izvēlnes** struktūra.
1. Atkārtojiet iepriekšējo darbību pārējiem diviem jaunajiem izvēlnes elementiem.
1. Saraksta rūtī pa kreisi atlasiet galveno **izvēlni**.
1. Sarakstā Pieejamās **izvēlnes un izvēlnes** vienumi ritināt uz leju **līdz sadaļai Izvēlnes** un atlasiet jauno izvēlnes **Uzziņas**. Pēc tam atlasiet labās bultiņas pogu, lai pārvietotu elementu uz sarakstu **Izvēlnes** struktūra.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Konfigurēt atšifrējus mobilās ierīces soļos

Lai pabeigtu iestatīšanu, tagad jāizmanto **dešifrēšanas** *konfigurācija mobilās ierīces darbību lapā, lai pievienotu trīs jaunus mobilās ierīces izvēlnes vienumus esošajam pirkšanas pasūtījuma identifikācijas solim Pirkumu saņemšanas* plūsmā.

1. Pārejiet uz **sadaļu Noliktavas \> pārvaldības iestatīšana > mobilās ierīces mobilās \> ierīces darbības**.
1. Laukā **Filtrs ievadiet** PONum *·*. Pēc tam *nolaižamajā sarakstā atlasiet Darbības ID: "PONum* ".
1. Kamēr režģī ir atlasīts ieraksts, darbību rūtī **atlasiet** Pievienot darbības konfigurāciju. Parādītajā nolaižamajā dialoglodziņā iestatiet izvēlnes elementa lauku **Uz** Pirkšanas *saņemšana*. Pēc tam **atlasiet** Labi, lai aizvērtu dialoglodziņu.
1. Detalizētās informācijas lapā jaunajai darbību konfigurācijai (**Pirkšanas saņemšana: PONum** **) kopsavilkuma cilnē Pieejamie atslēkļi (izvēlnes vienumi** **)** atlasiet Pievienot rīkjoslā.
1. Dialoglodziņā Add **dešifrēti** atrodiet un atlasiet iepriekš izveidoto **POS** uzmeklšanu pēc kreditora izvēlnes elementa.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu un pievienotu atlasīto izvēlnes elementu sarakstam Dellas.
1. Atlasiet jauno de cilnē un pēc tam atlasiet laukus **, kuri jānosūta** uz rīkjoslas.
1. Dialoglodziņā Atlasīt **laukus**, lai nosūtītu, **nekas** nav jāpievieno sadaļai Nosūtīt no pirkuma saņemšanas, jo nevēlaties pieņemt nevienu vērtību de pirkšanas izvēlnes elementam. Tomēr sadaļā Atgriezt **no POS** uzmeklē pēc kreditora iestatiet tukšu rindu, kas jau ir tai pievienota, šādu vērtību:

    - **Kopēt no POS pēc kreditora: pirkšanas** *pasūtījums*
    - **Ielīmēt pirkšanas saņem: pirkšanas** *pasūtījums*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Atkārtojiet 4. līdz 9. darbību citiem diviem jaunajiem izvēlnes vienumiem (**uzmeklē POS** **šodienai un uzmeklē POS pēc krājuma**). Attiecībā uz **kreditoru izvēlnes elementu Uzmeklt POS**, jūs nevēlaties nosūtīt nekādus datus šiem atšifrētajiem, bet vēlaties atgriezt pirkšanas pasūtījuma numuru.
1. Aizvērt lapu.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Mēģiniet pirkšanas saņemšanas plūsmu, kam ir datu pieprasījums kā daļa no atdošanas

Izpildiet šīs darbības, lai pārbaudītu jaunās mobilās programmas iestatījumus.

1. Izveidojiet vairākus pirkšanas pasūtījumus, kuriem ir noliktavas 51 rindas.
1. Dodieties uz mobilo ierīci vai emulatoru, kas darbina Warehouse Management mobile programmu, un piesakieties noliktavā 51, izmantojot *51* kā lietotāja ID un *1* kā paroli.
1. Mobilās programmas izvēlnē atlasiet Ienākošais **un Pēc tam** — saņemt **pirkumu**.

    Vajadzētu redzēt šo lapu, kas ietver trīs jaunus izvēlnes elementus.

    ![Pirkuma saņemšana, izmantojot PO numuru.](media/wma-purchase-receive-po-num-with-detours.png "Pirkuma saņemšana, izmantojot PP numuru")

1. Izmēģiniet dažādas iespējas un ievērojiet, ka varat nosūtīt atpakaļ pirkšanas pasūtījuma numuru, atlasot sarakstā vienu no kartēm.

    ![Pirkuma saņemšana, izmantojot PP meklēšanu pēc kreditora, 1. piemērs.](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Pirkuma saņemšana, izmantojot PP meklēšanu pēc kreditora, 1. piemērs")

    ![Pirkuma saņemšana, izmantojot PP meklēšanu pēc kreditora, 2. piemērs.](media/wma-purchase-receive-lookup-po-vendor-detours.png "Pirkuma saņemšana, izmantojot PP meklēšanu pēc kreditora, 2. piemērs")

> [!TIP]
> **Tā** vietā, lai palaistu saņemšanas plūsmu, veicot meklēšanu no izvēlnes elementa Pirkšanas saņemšana, varat sākties no pieprasījumu plūsmas (**\>\>** galvenā uzziņu informācija par PO pēc kreditora) un izsaukt dektoru, lai palaistu vēlamo plūsmu, atlasot vienu no sarakstā kartēm. Lai izmantotu šo pieeju, mobilās ierīces darbību lapā varat definēt darbību, **·** **kam ir GenericDataInquiryList darbības ID** *vērtība.* Tā kā šī plūsma ir atplūde, jūs no tās nevarat izsaukt vairāk deturis. Tāpēc, kad būsit pieejams krājuma numura ievades ekrānā, piemēram, pārlūks tajā nebūs pieejams, jo sistēma pašreiz atbalsta tikai vienu de skaitliskās vērtības līmeni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
