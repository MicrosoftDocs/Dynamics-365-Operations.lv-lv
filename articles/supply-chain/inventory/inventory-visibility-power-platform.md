---
title: Krājumu redzamības programma
description: Šajā rakstā ir aprakstīts, kā izmantot krājumu redzamības programmu.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 674adb70cc4372a8c5ca8c75ed3ef840d8ec7b79
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520869"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility programmas lietošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izmantot krājumu redzamības programmu.

Krājumu redzamība nodrošina modeļa vadītas programmas vizualizēšanu. Programmā ir trīs lapas: **Konfigurācija**, **Operāciju redzamība** un **Krājumu kopsavilkums**. Tam ir tālāk minētās vērtības:

- Tā nodrošina lietotāja interfeisu (UI) rīcībā esošo konfigurāciju un vieglās rezervēšanas konfigurāciju.
- Tas atbalsta reāllaika rīcībā esošo krājumu vaicājumus par dažādām dimensiju kombinācijām.
- Tas sniedz UI rezervāciju pieprasījumu grāmatošanai.
- Tajā sniegts rīcībā esošo krājumu skats precēm ar visām dimensijām.
- Tajā sniegts rīcībā esošo krājumu saraksta skats precēm ar iepriekš definētām dimensijām.


## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat darbu, uzinstalējiet un iestatiet Inventory Visibility pievienojumprogrammu, kā aprakstīts rakstā [Inventory Visibility instalēšana un iestatīšana](inventory-visibility-setup.md).

## <a name="open-the-inventory-visibility-app"></a>Atveriet Inventory Visibility lietojumprogrammu

Lai atvērtu Inventory Visibility lietojumprogrammu, pierakstieties Power Apps vidē un atveriet **Inventory Visibility**.

## <a name="configuration"></a><a name="configuration"></a>Konfigurācija

Pakalpojuma lapa **Konfigurācijas** Inventory Visibility programmā palīdz iestatīt rīcībā esošo konfigurāciju un vieglās rezervācijas konfigurāciju. Pēc lietojumprogrammas pievienošanas noklusējuma konfigurācija ietver Microsoft Dynamics 365 Supply Chain Management (`fno` datu avots) noklusējuma iestatījumu. Varat pārskatīt noklusēto iestatījumu. Turklāt, pamatojoties uzņēmuma prasībās un ārējās sistēmas krājumu grāmatošanas prasībās, varat pārveidot konfigurāciju, lai standartizētu veidu, kādā var vairākās sistēmās grāmatot, organizēt un vaicātas krājumu izmaiņas.

Visu informāciju par to, kā konfigurēt risinājumu, skatiet sadaļā [Inventory Visibility konfigurēšana](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Darbības redzamība

Lapa **Darbības redzamība** sniedz reāllaika rīcībā esošo krājumu vaicājuma rezultātus, kas pamatoti uz dažādām dimensiju kombinācijām. Ja ir ieslēgta funkcija *OnHandReservation*, varat arī grāmatot rezervēšanas pieprasījumus no lapas **Operāciju redzamība**.

### <a name="on-hand-query"></a>Rīcībā esošie vaicājumi

Cilnē **Rīcībā esošie vaicājumi** tiek rādīti reāllaika rīcībā esošo krājumu vaicājuma rezultāti.

Atverot lapas **Operāciju** **redzamība** cilni Rīcībā esošo vaicājums, sistēma pieprasa savus akreditācijas datus, lai varētu iegūt uzrādītāja marķieri, kas ir nepieciešams, lai vaicātu par krājumu redzamības pakalpojumu. Variet tikai ielīmēt uzrādītāja marķieri laukā **BearerToken** un aizvērt dialoglodziņu. Pēc tam varat iegrāmatot rīcībā esošo vaicājumu pieprasījumu.

Ja uzrādītāja marķieris nav derīgs vai arī tā derīgums ir beidzies, pievienojiet jaunu laukā **BearerToken**. Ievadiet pareizo **Klienta ID**, **Nomnieka ID**, **Klienta slepeno informāciju** un pēc tam atlasiet **Atsvaidzināt**. Sistēma automātiski saņems jaunu, derīgu uzrādītāja marķieri.

Lai grāmatotu rīcībā esošo vaicājumu, ievadiet pieprasījuma pamattekstā. Izmantojiet Modeli, kas aprakstīts [Vaicājumā, izmantojot grāmatošanas metodi](inventory-visibility-api.md#query-with-post-method).

![Rīcībā esošie vaicājumu iestatījumi](media/inventory-visibility-query-settings.png "Rīcībā esošie vaicājumu iestatījumi")

### <a name="reservation-posting"></a>Rezervāciju grāmatošana

Lai grāmatotu **rezervēšanas** pieprasījumu, izmantojiet **lapas Rezervācija** grāmatošana cilni Darbības redzamība. Pirms rezervēšanas pieprasījuma grāmatošanas ir jāslēdz funkcija *OnHandReservation*. Plašāku informāciju par šo funkciju un to, kā to ieslēgt, skatiet krājumu [redzamības rezervēšanu](inventory-visibility-reservations.md).

Lai grāmatotu rezervēšanas pieprasījumu, pieprasījuma pamattekstā ir jāievada vērtība. Izmantojiet modeli, kas ir aprakstīts sadaļā [Izveidot vienu rezervācijas notikumu](inventory-visibility-api.md#create-one-reservation-event). Pēc tam atlasiet **Grāmatot**. Lai skatītu pieprasījuma atbildes informāciju, atlasiet **Rādīt informāciju**. Atbildes informācijā varat arī iegūt `reservationId` vērtību.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Krājumu kopsavilkums

Krājumu **kopsavilkuma lapa** sniedz krājuma kopsavilkumu precēm kopā ar visām dimensijām. Tas ir pielāgots skats elementam Rīcībā *esošo krājumu* summa. Krājumu kopsavilkuma dati tiek periodiski sinhronizēti no krājumu redzamības.

Lai iespējotu **lapu Krājumu kopsavilkums** un iestatītu sinhronizācijas biežumu, rīkojieties šādi:

1. Atveriet lapu **Konfigurācija**.
1. Atveriet cilni **Līdzekļu pārvaldība &** iestatījumi.
1. Iestatiet pārslēgšanās pārslēgšanos līdzeklim **OnHandMostSpecificBackgroundService** uz *Jā*.
1. Kad funkcija ir aktivizēta, **·** **pakalpojuma konfigurācijas sadaļa kļūst pieejama un ietver rindu līdzekļa OnHandMostSpecificBackgroundService konfigurēšanai.** Šis iestatījums ļauj izvēlēties biežumu, kādā tiek sinhronizēti krājumu kopsavilkuma dati. Izmantojiet pogas **Augšupvērstais** **un** Lejupvērstais **kolonnā** Vērtību, lai mainītu laiku starp sinhronizācijām (kas var būt tik zema, kā 5 minūtes). Pēc tam atlasiet **Saglabāt**.

    ![Iestatījums OnHandMostSpecificBackgroundService](media/inventory-visibility-ohms-freq.png "Iestatījums OnHandMostSpecificBackgroundService")

1. Atlasiet **Atjaunināt konfigurāciju,** lai saglabātu visas izmaiņas.


> [!NOTE]
> Funkcija *OnHandMostSpecificBackgroundService* izseko tikai rīcībā esošo krājumu izmaiņas, kas notikušas pēc ieslēgts līdzeklis. To preču dati, kuras nav mainītas kopš ieslēgts līdzeklis, netiks sinhronizēti no krājumu pakalpojuma kešatmiņas vidē Dataverse. **Ja** jūsu Krājumu kopsavilkuma lapā nav parādīta visa jūsu sagaidāmā rīcībā esošo informāciju, atveriet piegādes ķēdes pārvaldību, dodieties uz krājumu pārvaldība > Periodiskie uzdevumi > Krājumu **redzamības integrācija, atspējojiet pakešuzdevumu unaktivizējiet to**. Tas veiks sākotnējo virzību, un visi dati nākamo *15 minūšu laikā tiks sinhronizēti* ar elementu Krājumu rīcībā summa. Ja vēlaties izmantot *funkciju OnHandMostSpecificBackgroundService*, **ieteicams** to ieslēgt pirms rīcībā esošo izmaiņu izveides un iespējot krājumu redzamības integrācijas pakešuzdevumu.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-the-inventory-visibility-onhand-query"></a> Ielādēt racionalizētu rīcībā esošo vaicājumu

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Piegādes ķēdes pārvaldība saglabā lielu informācijas daudzumu par jūsu pašreizējiem rīcībā esošajiem krājumiem un padara to pieejamu dažādiem nolūkiem. Tomēr daudzām ikdienas operācijām un trešās puses integrācijai nepieciešama tikai neliela šo detaļu apakškopa, un vaicājumi par visām no tām var radīt lielas datu kopas, kas prasa laiku, lai izveidotu un pārsūtītu. Tāpēc krājumu redzamības pakalpojums var periodiski saņemt un uzglabāt racionalizētu rīcībā esošo krājumu datu kopu, lai pastāvīgi būtu pieejama optimizēta informācija. Informācija par rīcībā ajiem krājumiem tiek filtrēta, balstoties uz konfigurējamiem biznesa kritērijiem, lai nodrošinātu, ka tiek iekļauta tikai atbilstošākā informācija. Tā kā filtrētie rīcībā esošo krājumu saraksti krājumu redzamības pakalpojumā tiek saglabāti lokāli, un tie tiek regulāri atjaunināti, tie atbalsta ātro piekļuvi, pieprasījuma datu eksportēšanu un racionalizētu integrāciju ar ārējām sistēmām.

> [!NOTE]
> Šī līdzekļa pašreizējā priekšskatījuma versija var nodrošināt tikai iepriekš ielādētus rezultātus, kas ietver vietu un atrašanās vietu. Paredzams, ka līdzekļa beigu versija ļaus jums atlasīt citas dimensijas iepriekšēja ielādei ar rezultātiem.

Krājumu **redzamības kopsavilkuma lapas iepriekšēja ielāde** sniedz skatu rīcībā *esošo indeksu vaicājuma pirmsielādes rezultātu elementam*. Atšķirībā no krājumu *kopsavilkuma elementa*, *rīcībā esošo krājumu indeksa vaicājuma pirmsielādes* rezultātu elements nodrošina rīcībā esošo krājumu sarakstu precēm ar atlasītajām dimensijām. Krājumu redzamība sinhronizē iepriekš ielādētos kopsavilkuma datus ik pēc 15 minūtēm.

Lai skatītu **datus cilnē Krājumu redzamības kopsavilkums pirmsielādē,** ir jāslēdz funkcija *OnHandIndexQueryPreloadBackgroundService* **·** **·** **cilnes Līdzekļu pārvaldība lapā Konfigurācija un pēc tam jāatlasa Atjaunināt konfigurāciju (** skatiet arī krājumu redzamības konfigurāciju).[...](inventory-visibility-configuration.md)

> [!NOTE]
> Tāpat kā ar *līdzekli OnhandMostSpecificBackgrkrautService*, funkcija OnHandIndexQueryPreloadBackgroundService *izseko tikai rīcībā esošo krājumu izmaiņas,* kas notikušas pēc funkcijas ieslēgtšanas. To preču dati, kuras nav mainītas kopš ieslēgts līdzeklis, netiks sinhronizēti no krājumu pakalpojuma kešatmiņas vidē Dataverse. **Ja** jūsu Krājumu kopsavilkuma lapā nav parādīta visa pieejamā informācija, ko plānojat, **pārejiet uz sadaļu Krājumu pārvaldība > Periodiskie uzdevumi >** Krājumu redzamības integrācija, atspējojiet pakešuzdevumu un ataktivizējiet to. Tādējādi tiks veikts sākotnējais pašpiegādes darbs, *un* visi dati nākamo 15 minūšu laikā tiks sinhronizēti ar rīcībā esošo datu indeksa vaicājuma pirmsielādes rezultātu elementu. Ja vēlaties izmantot šo funkciju, **ieteicams to ieslēgt pirms jebkādu rīcībā esošo izmaiņu veikšanas un iespējot pakešuzdevumu Krājumu** redzamība integrācija.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a> Filtrēt un pārlūkot krājumu kopsavilkumus

Lietojiet Dataverse sniegto **Detalizēto filtru**, varat izveidot personalizētu skatu, kurā rādītas jums svarīgākās rindas. Papildu filtra opcijas ļauj izveidot plašu skatījumu klāstu no vienkāršiem uz kompleksiem. Tie arī ļauj pievienot filtriem grupētus un ligzdotus nosacījumus. Papildinformāciju par to, kā izmantot papildu filtru, skatiet sadaļā Rediģēt [vai izveidot personālos skatus, izmantojot papildu režģa filtrus](/powerapps/user/grid-filters-advanced).

Krājumu **kopsavilkuma lapa sniedz** trīs laukus virs režģa (**Noklusējuma** dimensija, **Pielāgota** dimensija un Mērs), ko varat izmantot, lai kontrolētu, **kuras** kolonnas ir redzamas. Var atlasīt arī jebkuru kolonnas virsrakstu, lai filtrētu vai kārtotu pašreizējo rezultātu pēc šīs kolonnas. Šajā ekrānuzņēmumā ir redzama krājumu kopsavilkuma lapā pieejamo dimensiju, filtrēšanas, **rezultātu** skaita un noslodzes papildu lauki.

![Krājumu kopsavilkuma lapa.](media/inventory-visibility-onhand-list.png "Krājumu kopsavilkuma lapa")

Tā kā būsiet iepriekš definētas dimensijas, kas tiks izmantotas kopsavilkuma datu ielādei, **pirmsielādē krājumu redzamības kopsavilkuma lapā** tiek parādītas ar dimensijām saistītās kolonnas. *Dimensijas nav pielāgojamas, jo&mdash; sistēma atbalsta tikai vietas un atrašanās vietas dimensijas iepriekš ielādētajiem rīcībā ajiem sarakstiem.* Lapā **Krājumu redzamības kopsavilkuma pirmsielāde ir** nodrošināti **filtri**, kas ir līdzīgi lapā Krājumu kopsavilkums atlasītajiem filtriem, izņemot jau atlasītās dimensijas. Šajā ekrānuzņēmumā ir izcelti filtrēšanas lauki, kas ir pieejami **lapā Krājumu redzamības kopsavilkuma lapa pirmsielādē**.

![Tiek iepriekšēja ielādēta kopsavilkuma lapa Krājumu redzamība.](media/inventory-visibility-preload-onhand-list.png "Tiek iepriekšēja ielādēta kopsavilkuma lapa Krājumu redzamība")

Pirmsielādējiet **·** **krājumu** redzamības kopsavilkumu un krājumu kopsavilkuma lapas, varat atrast tādu informāciju kā "50 ieraksti (izvēlēti 29)" vai "50 ieraksti". Šī informācija attiecas uz ierakstiem, kas pašlaik ielādēti no **Detalizētā filtra** rezultāta. Teksts "atlasīts 29" attiecas uz ierakstu skaitu, kas ir atlasīti, ielādētajiem ierakstiem izmantojot kolonnas virsraksta filtru. Ir arī poga Ielādēt **vairāk,** ko varat izmantot, lai ielādētu vairāk ierakstu Dataverse. Ielādēto ierakstu noklusējuma skaits ir 50. Ja atlasīsiet **Ielādēt** vairāk, skatā tiks ielādēti nākamie 1000 pieejamie ieraksti. Skaits pogā **Ielādēt vēl** norāda pašlaik ielādētos ierakstus un kopējo ierakstu skaitu **Detalizētā filtra** rezultātā.
