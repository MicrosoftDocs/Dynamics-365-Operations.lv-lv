---
title: Novietojuma produkta dimensijas sajaukšana
description: Šajā rakstā ir sniegta informācija par vietas preču dimensiju jaukšanu. Šī novietojuma profila funkcionalitāte palīdz uzlabot novietojumu pārvaldību, izmantojot produkta variantus vai produktus ar dimensijām, piemēram, modes industrijā. Tas ļauj jums izlemt, vai konfigurācijas, krāsas, stilus un izmērus var kombinēt noteiktam novietojuma profilam, vai arī tikai vienu no šīm dimensijām, vai to kombināciju var pievienot tam pašam novietojumam.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 9daf6061d56ef004753114aaffa8eb580cea1186
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885730"
---
# <a name="location-product-dimension-mixing"></a>Novietojuma produkta dimensiju sajaukšana

[!include [banner](../includes/banner.md)]

Novietojuma produkta dimensiju kombinēšana ir novietojuma profila funkcionalitāte, kas palīdz uzlabot novietojumu pārvaldību, izmantojot produkta variantus vai produktus ar dimensijām, piemēram, modes industrijā. Tas ļauj jums izlemt, vai konfigurācijas, krāsas, stilus un izmērus var kombinēt noteiktam novietojuma profilam, vai arī tikai vienu no šīm dimensijām, vai to kombināciju var pievienot tam pašam novietojumam.

## <a name="turn-the-location-product-dimension-mixing-feature-on-or-off"></a>Ieslēgt vai izslēgt novietojuma preču dimensiju jaukšanas līdzekli

Lai izmantotu šajā rakstā aprakstīto funkcionalitāti, jūsu *sistēmai ir* jābūt ieslēgtai preces dimensijas jaukšanas funkcijai. Tāpat kā Piegādes ķēdes pārvaldībai 10.0.25 šī funkcija ir obligāta un to nevar izslēgt. Ja jūs palaižat versiju, kas vecāka par 10.0.25, tad administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot Atrašanās *vietas preču dimensiju jaukšanas*[līdzekli Līdzekļu pārvaldības darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="setup"></a>Iestatīt

Katram novietojumam ir jābūt ar to saistītam novietojuma profilam noliktavā, kas apraksta novietojuma parametrus. Tāpēc visas vietas, kas izmanto vienu novietojuma profilu, pēc tā iestatīšanas varēs atļaut produktu dimensiju jaukšanu.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Konfigurējiet novietojuma profilus, lai atļautu produktu dimensiju jaukšanu

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.
1. Novietojuma profilu sarakstā atlasiet **LIELAPJOMA**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Vispārēji** iestatiet **Iespējot novietojuma produktu dimensiju specifisku sajaukšanas** opciju uz *Jā*.

    > [!NOTE]
    > Varat iestatīt šo opciju kā *Jā* tikai tad, ja opcija **Atļaut jauktus elementus** ir iestatīta uz *Nē*.

1. Kopsavilkuma cilnē **Vispārēji** iestatiet opciju **Iespējot novietojuma produktu dimensiju specifisku jaukšanas** uz *Jā*. Šajā rakstā aprakstītajā scenārijā jaukšanu var veikt tikai precēm ar atšķirīgām izmēru **dimensijām**. Tomēr ir pieejamas arī citas iespējas.
1. Atlasiet **Saglabāt**.

### <a name="create-a-new-product-master-and-product-variants"></a>Izveidojiet jaunu produktu šablonu un produktu variantus

1. Dodieties uz **Preču informācijas pārvaldība \> Produkts \> Produktu šabloni**.
1. Lai izveidotu produktu šablonu, darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Jauns produkts** iestatiet sekojošus laukus:

    - **Produkta veids:** *Elements*
    - **Produkta apakštips:** *Produkta šablons*
    - **Produkta numurs:** *B0001*
    - **Produkta nosaukums:** *B0001 Izmērs*
    - **Produkta dimensiju grupa:** *Izmērs*
    - **Konfigurēšanas tehnoloģija:** *Iepriekš noteikts variants*

1. Atlasiet **Labi**.
1. Lapā **Produkta detaļas**, kas atrodas kopsavilkuma cilnē **Vispārīgi**, iestatiet šādas vērtības:

    - **Automātiski ģenerēt variantus:** *Jā*
    - **Izmēru grupa:** *CASUALDHIR*

1. Lai skatītu iepriekš definētos variantus, darbību rūtī atlasiet **Produktu varianti**.

    Parādās lapa **Produkta varianti** un ataino variantu sarakstu no izmēru grupas konfigurācijas.

### <a name="release-products-to-the-usmf-company"></a>Nodot izpildei produktus USMF kompānijai

1. Darbību rūtī atlasiet **Nodot izpildei produktus**.
1. Lapā **Atlasīt publicējamos produktus** apstipriniet, ka produkta numurs *B0001* ir sarakstā, un pēc tam atlasiet **Tālāk**.
1. Atlasiet **Tālāk**, lai apstiprinātu izpildei nododamos produktu variantus.
1. Lapā **Atlasīt uzņēmumus, lai nodotu tiem izpildei** atlasiet *USMF*, un pēc tam atlasiet **Tālāk**, lai apstiprinātu atlasi.
1. Lapā **Apstiprināt atlasi** atlasiet **Pabeigt**, lai pabeigtu nodošanu izpildei.

    Tiek saņemts ziņojums "Darbība pabeigta".

### <a name="update-a-released-product-in-the-usmf-company"></a>Atjaunināt izlaisto preci USMF uzņēmumā

1. Pārliecinieties, ka esat pierakstīts **USMF** uzņēmumā.
1. Lai pabeigtu izlaistā produkta izveidi, atlasiet **Produktu informācijas pārvaldība \> Produkti \> Izlaistie produkti**.
1. Atrodiet un atlasiet elementu ar kodu *B0001*, lai atvērtu **Izdoto produktu informācijas** lapu.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Vispārīgi** pārliecinieties, ka lauks **Elementu modeļu grupa** ir iestatīts kā *FIFO*.
1. Darbību rūtī cilnes **Produkts** grupā **Iestatījumi**, atlasiet **Dimensiju grupas**.
1. Iestatiet šādas vērtības:

    - **Noliktavas dimensiju grupa:** *Izstrādājumi*
    - **Izsekošanas dimensiju grupa:** *Nav*

1. Atlasiet **Labi**.
1. Darbību rūtī cilnes **Produkts** grupā **Iestatījumi** atlasiet **Rezervācijas hierarhija**.
1. Iestatiet lauku **Rezervācijas hierarhija** pēc *Noklusējuma*, un pēc tam atlasiet **Labi**.
1. Kopsavilkuma cilnes **Vispārīgi** sadaļā **Administrācija** ievērojiet, ka atlases ir atjauninātas.
1. Kopsavilkuma cilnē **Pirkumi** laukā **Cena** ievadiet *10*.
1. Kopsavilkuma cilnes **Pārvaldīt izmaksas** laukā **Elementu grupa** ievadiet *Audio*.
1. Kopsavilkuma cilnē **Pirkumi** laukā **Cena** ievadiet *10*.
1. Kopsavilkuma cilnes **Noliktava** laukā **Vienības secības grupas ID** ievadiet *ea*.
1. Atlasiet **Saglabāt**.

### <a name="create-a-location-directive"></a>Novietojuma direktīvas izveide

1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.
1. Kreisajā rūtī, laukā **Darba pasūtījuma veids** atlasiet *Pirkuma pasūtījumi*.
1. Sarakstā atlasiet novietojuma direktīvu ar nosaukumu *24 PO Direct*.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai pievienotu režģim rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Secības numurs:** *1*

        Jaunajai rindai jābūt pirms iepriekš esošās rindas. Lai veiktu izmaiņas, izmantojiet rīkjoslas pogas **Pārvietot uz augšu** un **Pārvietot uz leju** vai mainiet esošās rindas **Secības numura** vērtību uz *2*.

    - **Nosaukums:** *Likt uz LIELAPJOMA novietojuma profila*
    - **Fiksēta novietojuma lietojums:** *Fiksētas un nefiksētas vietas*
    - **Atļaut negatīvu uzkrājumu:** *Nodzēst šo izvēles rūtiņu (=Nē)*
    - **Pakete aktivizēta:** *Nodzēst šo izvēles rūtiņu (=Nē)*
    - **Stratēģija:** *Nav*

1. Turpinot atlasīt jaunāko rindu, atlasiet **Rediģēt vaicājumu** virs režģa.
1. Vaicājuma redaktora dialoglodziņā cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu režģim.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** *Novietojumi*
    - **Atvasinātā tabula:** *Vietas*
    - **Lauks:** *Atrašanās vietas profila ID*
    - **Kritēriji:** *LIELAPJOMA*

1. Atlasiet **Labi**.
1. Darbības rūts lapā **Atrašanās vietas direktīvas** atlasiet **Saglabāt**.

> [!NOTE]
> Ja izmantojat *Konsolidācijas* atrašanās vietas stratēģiju kopsavilkuma cilnes **Atrašanās vietu direktīvu darbības** laukā **Stratēģija**, tiks ignorēti kopsavilkuma cilnes **Atļautā produkta dimensiju jaukšana** lauka **Atrašanās vietu profili** iestatījumi, un elementi tiks ievietoti turpat, pat ja iestatījumi neļauj veikt šo darbību.

### <a name="create-a-mobile-device-menu-item"></a>Mobilās ierīces izvēlnes elementa izveide

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbības rūtī atlasiet **Jauns**, lai izveidotu izvēlnes elementu, ko izmantot kārtošanai.
1. Galvenē iestatiet šādas vērtības:

    - **Izvēlnes elementa nosaukums:** *PO rindas saņemšana*
    - **Nosaukums:** *PO rindas saņemšana*
    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Nē*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Darba izveides process:** *Pirkšanas pasūtījuma rindas saņemšana un nosūtīšana*
    - **Ģenerēt numura zīmi:** *Jā*

1. Atlasiet **Saglabāt**.

### <a name="configure-the-mobile-device-menu"></a>Konfigurēt mobilās ierīces izvēlni

1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
1. Novietojuma profilu sarakstā atlasiet **Ienākošie**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Sarakstā **Pieejamās izvēlnes un izvēlņu elementi** atrodiet un atlasiet **PO rindas saņemšanas** izvēlnes elementu.
1. Atlasiet labo bultiņu, lai pārvietotu **PO rindas saņemšanas** izvēlnes elementu **Izvēlņu struktūras** sarakstā. Šādā veidā jūs pievienojiet savu jauno izvēlnes elementu atlasītajai izvēlnei.
1. Atlasiet **Saglabāt**.

## <a name="scenario"></a>Scenārijs

Šis demonstrācijas scenārijs parāda, kā divi dažādi produkta varianti var tikt ievietoti vienā un tajā pašā vietā, kad novietojuma profilā nav atļauti jaukti elementi, bet ir iespējota *Novietojuma produktu dimensiju jaukšanas* funkcija. Šādā gadījumā jūs izmantosiet **Izmēra** variantu kā kritēriju.

Pirms sākat, pārliecinieties, ka noliktavā *24* ir tukšas atrašanās vietas, kas izmanto *LIELAPJOMA* atrašanās vietas profilu.

### <a name="create-a-purchase-order"></a>Pirkuma pasūtījuma izveide

Jūs izveidosiet pirkuma pasūtījumu, kam ir trīs rindas: divas rindas satur vienādu produkta numuru, bet dažādus **Izmēra** variantus, bet trešā rinda ir paredzēta citam produktam, kam nav variantu.

1. Dodieties uz **Kreditori \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:

    - **Tirgotāja konts:** *1001*
    - **Noliktava:** *24*

1. Atlasiet **Labi**.
1. Pirkuma pasūtījums ir izveidots, un kopsavilkuma cilnē **Pirkuma pasūtījuma rindas** tiek pievienota jauna rinda. Pierakstiet pirkuma pasūtījuma numuru.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Elementa numurs:** *B0001*
    - **Lielums** *L*
    - **Daudzums:** *2*

1. Atlasiet **Pievienot rindu** virs režģa, lai pievienotu otro pirkuma pasūtījuma rindu, un iestatiet šādas vērtības:

    - **Elementa numurs:** *B0001*
    - **Izmērs** *XL*
    - **Daudzums:** *2*

1. Atlasiet **Pievienot rindu**, lai pievienotu trešo pirkuma pasūtījuma rindu, un iestatiet šādas vērtības:

    - **Elementa numurs:** *A0001*
    - **Daudzums:** *1*

1.Atlasiet **Saglabāt**.

### <a name="receive-purchase-order-lines-in-the-warehouse-management-mobile-app"></a>Saņemt pirkuma pasūtījumu rindas Warehouse Management mobile programmā

1. Pierakstieties Warehouse Management mobile programmā kā lietotājs, kurš ir iespējots noliktavā *24*.
1. Atlasiet izvēlni **Ienākošie**.
1. Atlasiet **PO rindas saņemšana**.
1. Atlasiet lauku **PONUM** un pēc tam ievadiet pirkuma pasūtījuma numuru.
1. Apstipriniet ievadni, atlasot apstiprināšanas pogu (✔) lapas apakšdaļā.
1. Ievadiet rindas numuru no pirkuma pasūtījuma, kas tiek saņemts. Atlasiet lauku **LINENUM** un pēc tam izmantojiet ciparu tastatūru, lai ievadītu *1*.
1. Apstipriniet ievadīto.
1. Ievadiet saņemamo daudzumu. Atlasiet plus zīmi (**+**) divas reizes, lai palielinātu lauka **Daudzums** vērtību par *2*.
1. Reģistrējiet savu ierakstu, lapas apakšdaļā atlasot pogu (✔), un pēc tam apstipriniet ievadni, vēlreiz atlasot pogu (✔).
1. Skatiet informāciju par lapu **Pirkuma pasūtījumiem: Ievietotie**. Šajā lapā ir parādīts darbs, kas tika izveidots izvietošanai (1. darbs).

    Tiek atainota atrašanās vieta, kur tiks izvietoti saņemtie pasūtījumi, numura zīme, elements, lielums un **PO rindas saņemšanas** uzdevumu skaits, ko tikko pabeidzāt.

1. Apstipriniet izvietošanas darbu.
1. Pirkuma pasūtījuma 2.rindai atkārtojiet 4. – 11. soli. Tomēr 8. solī norādiet daudzumu *1*.

    Jauns izvietošanas darbs (2. darbs) ir izveidots tai pašai vietai kā 1. darbs.

1. Pirkuma pasūtījuma 2.rindai vēlreiz atkārtojiet 4. – 11. soli. 8. solī norādiet atlikušo daudzumu *1*.

    Jauns izvietošanas darbs (3. darbs) ir izveidots tai pašai vietai kā 1. un 2. darbs. Šī problēma rodas tāpēc, ka tiek izmantota *Konsolidētās* atrašanās vietas direktīvas stratēģija, un kopsavilkuma cilnes **Atļautā produkta dimensiju jaukšana** uz *LIELAPJOMA*, **Atrašanās vietas profiliem** iestatīšana ļauj mainīt **Izmēru** variantu, kombinējot ar atrašanās vietu.

1. Pirkuma pasūtījuma 3.rindai atkārtojiet 4. – 11. soli. 8. solī norādiet daudzumu *1* elementam ar numuru *A0001*.

    Jauns izvietošanas darbs (4. darbs) ir izveidots citai vietai nekā vieta, kas tiek izmantota pirkuma pasūtījuma 1. un 2. rindai. Šī problēma rodas tāpēc, ka novietojuma profils nenodrošina jauktus produktus, bet tas ļauj sajaukt vienas preces šablona dimensijas.

1. Atlasiet pogu Izvēlne lapas augšmalā (dažreiz saukta par hamburgeru vai hamburgeru pogu) un pēc tam atlasiet **Atcelt**, lai izietu no **PO rindas saņemšanas**.

> [!TIP]
> Varat atkārtot šo scenāriju, bet šoreiz iestatiet **Izmēru** - *Nē* atbilstoši kopsavilkuma cilnes sadaļā **Atļaut produktu dimensiju jaukšanu** uz *LIELAPJOMA*, **Atrašanās vietas profiliem**, lai neviens no preces dimensijām nevarētu sajaukt. Šādā gadījumā, saņemot pirkuma pasūtījumu, katrs produktu variants tiks nosūtīts uz jaunu atrašanās vietu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]