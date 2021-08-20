---
title: Konfigurēt preču filtrus noliktavas darījumiem
description: Šajā tēmā ir aprakstīts, kā konfigurēt produktu filtrus un filtru kodus, lai noliktavā krājumu vienības iedalītu kategorijās. Filtrus varat arī izmantot, lai norādītu, kuri debitori var pasūtīt noteiktu krājumu, un norādītu krājumus, ko iespējams iegādāties no konkrēta kreditora.
author: Mirzaab
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 6302d596245e058ae0c25fbd91333dbf050e21db5b48f6893131ec1a561e046d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768550"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a>Konfigurēt preču filtrus noliktavas darījumiem

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā konfigurēt produktu filtrus un filtru kodus, lai noliktavā krājumu vienības iedalītu kategorijās. Filtrus varat arī izmantot, lai norādītu, kuri debitori var pasūtīt noteiktu krājumu, un norādītu krājumus, ko iespējams iegādāties no konkrēta kreditora.

Turklāt varat iestatīt un izmantot filtru kodus, lai noliktavā esošās krājumu vienības automātiski sakārtotu un filtrētos vienumus kombinētu filtru grupās. Filtrus var izmantot, lai ievietotu krājumus kategorijās apstrādes, pirkšanas un pārdošanas procesiem. Ja vēlaties grupēt krājumus kopā vai atdalīt tos vienu no otra, ja to apstrādes veids ir atkarīgs no svara vai apstrādes ierobežojumiem. Varat arī norādīt, no kuriem debitoriem vai kreditoriem krājumu var iegādāties vai pārdot.

## <a name="prerequisites"></a>Priekšnosacījumi

Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darba sākšanas.

| Priekšnoteikumi | Instrukcijas |
|---|---|
| Pirms sākat konfigurēt preces lapā **Izlaistās preces informācija**, ir jāiespējo noliktavas apstrāde process preces noliktavas dimensiju grupai. | Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Iestatījumi \> Dimensijas un variantu grupas \> Noliktavas dimensiju grupas** un atlasiet vai izveidojiet noliktavas dimensiju grupu, kur opcija **Izmantot noliktavas pārvaldības procesus** ir iestatīta uz *Jā*. |
| Ja izmantosiet debitoru filtrus un/vai kreditoru filtrus, to lietošana ir jāiespējo noliktavas pārvaldības parametros. | Doties uz **Noliktavas vadība \> Iestatīšana \> Noliktavas vadības parametri**. Cilnē **Preču filtri** iestatiet opciju **Iespējot debitoru filtrus** un/vai **Iespējot kreditoru filtrus** uz *Jā*. |

## <a name="set-up-product-filters"></a>Iestatiet preču filtrus

Preču filtri nodrošina līdz 10 **Filtra nosaukuma** raksturlielumiem, kas ir uzskaitījuma (uzskaitījuma) vērtības. Šīs uzskaitījuma vērtības ir pieejamas atlasei, veidojot preču filtru. Uzskaitījuma vērtības no *1. koda* līdz *10. kodam* ir sistēmas definēts un parāda noteiktu krājuma īpašību vai atribūtu. Piemēram, *1. kods* varētu atbilst krājumiem, kam ir bīstamu materiālu klasifikācija. *2. kods* var norādīt krājumus, kurus var iegādāties tikai kreditori. Preču filtri tad definē īpašu **Filtra koda** vērtību, kas ir saistīta ar **Filtra nosaukuma** vērtību.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Preces filtri \> Preces filtri**.
1. Lai režģim pievienotu preču filtru, darbību rūtī atlasiet **Jauns**.
1. Laukā **Filtra nosaukums** atlasiet vērtību.
1. Laukā **Filtra kods** ierakstiet kādu vērtību.

    ![Preču filtra iestatīšana.](media/Product_Filters10.png "Preču filtra iestatīšana")

1. Laukā **Apraksts** ievadiet koda nosaukumu. Piemēram, *2. kods* varētu atainot kreditorus. Pēc tam varat veidot produktu filtru noteiktam kreditoram vai kreditoru grupai. Papildinformāciju skatiet šīs tēmas nākamajā sadaļā [Kreditoru filtra kodu iestatīšana](#vendor-product-filters).

    ![Preču filtru kopums.](media/Product_Filters.png "Preču filtru kopums")

## <a name="set-up-product-filter-groups"></a>Iestatiet preču filtru grupas

Filtru kodu grupēšanai var izmantot filtru grupas. Tas ir noderīgi, ja grupa tiek izmantota atrašanās vietas direktīvas vaicājumam, un vēlaties meklēt kodu grupu, nevis kodu sēriju. Katra filtru grupa tiek saistīta ar krājumu grupu.

> [!IMPORTANT]
> Ne visas preču filtru grupas ir pieejamas filtru kodiem, kas pārsniedz *4. kodu* (t.i., *5. kodu*, izmantojot *10. kodu*). Piemēram, izlaistajām precēm, kaut arī tiks pievienoti visi preču filtru kodi, filtru kodu grupēšana netiks atjaunināta. Šī funkcionalitāte var tikt atjaunināta vēlākos laidienos.

Lai iestatītu filtru grupas, veiciet šādas darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Preces filtri \> Preces filtru grupas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukos **1. grupa** un **2. grupa** ievadiet nosaukumus, kas tiks izmantoti krājumu kārtošanai kategorijās.
1. Kopsavilkuma cilnē **Žurnāla rindas** atlasiet **Jauns**, lai pievienotu rindu.
1. Laukos **Sākuma datums/laiks** un **Beigu datums/laiks** ievadiet filtra grupas sākuma un beigu datumus.
1. Laukā **Krājumu grupa** atlasiet krājumu grupu, uz kuru attiecas preču filtrs.
1. Laukos no **1. koda** līdz **10. kodam** pēc vajadzības atlasiet filtru kodus, ko iekļaut grupā.

    ![Krājumu grupa.](media/ProdFilterGroup.png "Krājumu grupa")

> [!NOTE]
> Ja, aizverot formu, saņemat kļūdas ziņojumu, iespējams, trūkst kodu iestatījumi. Lapā **Krājumu grupas** kodus krājumu grupai var padarīt obligātus, atzīmējot izvēles rūtiņas **Piešķirt filtra 1. kodu krājumu grupai**, **Piešķirt filtra 2. kodu krājumu grupai** utt.

## <a name="set-up-filter-codes-on-item-groups"></a>Filtru kodu iestatīšana krājumu grupām

Krājumu grupai iestatot filtru kodus, krājumu grupā ietilpstošajām precēm varat šos kodus noteikt kā obligātus.

Lai krājumu grupai iestatītu filtru kodus, izpildiet šādas darbības.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Krājumi \> Inventarizācijas grupas**.
1. Lai izveidotu krājumu grupu, darbību rūtī atlasiet **Jauns**.
1. Ievadiet nosaukumu laukā **Krājumu grupa**.
1. Laukā **Nosaukums** ievadiet aprakstu.
1. Kopsavilkuma cilnes **Noliktava** sadaļā **Nepieciešamais filtrs** atzīmējiet atbilstošās izvēles rūtiņas, lai definētu vienu vai vairākus filtru kodus, kas ir jānorāda ar krājumu grupu saistītajām precēm.

    Lai atjauninātu izlaisto preci, atveriet lapu **Izlaistās preces informācija** un pēc tam darbību rūtī atlasiet **Rediģēt**. Pēc tam ar kodiem saistītie filtri kļūst pieejami kopsavilkuma cilnē **Noliktava**.

    ![Krājumu grupas.](media/ItemGroup10.png "Krājumu grupas")

1. Sadaļā **Krājumu grupas filtrs** atzīmējiet to filtru izvēles rūtiņas, kuriem jāatbilst filtru grupai, lai tie būtu krājuma noklusējuma filtru grupa.

    Piemēram, ja ir atlasīta izvēles rūtiņa **Izmantot filtra 1. kodu** un **Izmantot filtra 2. kodu** , tad gan krājumu filtra 1. kodam, gan 2. kodam ir jāatbilst šīs krājumu grupas filtru grupas iestatījumam, lai varētu atlasīt šo filtru grupu. Izveidojot jaunu krājumu, atlasītā filtru grupa būs noklusējuma filtru laukos **1. grupa** un **2. grupa** kopsavilkuma cilnē **Noliktava** detalizētai informācijai par **Izpildei nodoto preci**.

> [!IMPORTANT]
> Preču filtru kodi ir iespējoti tikai krājumiem, kas izmanto papildu noliktavas pārvaldību.

## <a name="specify-filter-codes-for-released-products"></a>Filtru kodu norādīšana izlaistajām precēm

Izpildiet šīs darbības, lai norādītu filtru kodus izlaistajām precēm. Piemēram, var izmantot filtru kodus, lai grupētu bīstamas preces, ko iegādājas noteiktas kreditori.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Lai izveidotu produktu, darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Jauna izlaistā prece** ievadiet datus, kas nepieciešami jaunas preces pamata izveidošanai, un pēc tam atlasiet **Labi**.

    Preču filtru kodi nav iespējoti, ja vien precei piesaistītā krājumu grupa nav konfigurēta filtru kodiem.

    Papildinformāciju skatiet sadaļā [Jaunas preces izveide](../pim/tasks/create-new-product.md).

1. Kopsavilkuma cilnē **Noliktava** sadaļā **Preču filtru kodi** atlasiet filtru kodus laukiem no **1. koda** līdz **10. kodam**, lai norādītu produkta filtru kodus.

## <a name="set-up-generally-available-items"></a>Vispārīgi pieejamu krājumu iestatīšana

Konkrētas krājumu vienības varat padarīt pieejamas tikai debitoriem vai kreditoriem, vai gan debitoriem, gan kreditoriem.

> [!NOTE]
> Debitoru filtri un kreditoru filtri neattiecas uz krājumiem, ko iestatāt kā vispārīgi pieejamus.

Lai iestatītu vispārīgi pieejamus krājumus, izpildiet šīs darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Preces filtri \> Vispārīgi pieejamās preces**.
1. Lai izveidotu ierakstu, darbību rūtī atlasiet **Jauns**.
1. Laukā **Debitors vai kreditors** atlasiet *Debitors*, *Kreditors* vai *Visi*, lai padarītu krājumus pieejamus debitoriem, kreditoriem vai abiem.
1. Laukā **Sākuma datums/laiks** ievadiet datumu un laiku, kad krājums kļūs pieejams.
1. Atlasiet grupu laukā **Krājumu grupa**.
1. Laukos no **1. koda** līdz **10. kodam** atlasiet filtru kodus, lai ierobežotu vispārīgi pieejamos krājumus.

    Kad atlasāt kādu krājumu grupu, jūs šo krājumu grupu iestatāt kā vispārīgi pieejamu. Šajos laukos atlasot filtru kodus, jūs ierobežojat pieejamos krājumus.

## <a name="set-up-customer-product-filters"></a>Iestatīt debitoru preču filtrus

Šajā procedūrā ir aprakstīts, kā norādīt debitoriem pieejamus krājumus papildus tiem krājumiem, kuri ir padarīti pieejami, izmantojot filtru iestatījumus lapā **Vispārīgi pieejamie krājumi**. Vienam debitoram varat iestatīt vairākus filtrus.

Lai iestatītu debitoru filtru kodus, izpildiet šīs darbības.

1. Dodieties uz **Pārdošana un mārketings \> Debitori \> Visi debitori**.
1. Atlasīt debitoru.
1. Darbību rūtī cilnes **Produkts** grupā **Iestatījumi** atlasiet **Produktu filtri**.
1. Lapas **Preču filtru kodi** darbību rūtī atlasiet **Jauns**.
1. Laukos **Sākuma datums/laiks** un **Beigu datums/laiks** ievadiet atlasītās krājumu grupas sākuma un beigu datumus.
1. Atlasiet grupu laukā **Krājumu grupa**.
1. Laukos no **1. koda** līdz **10. kodam** atlasiet filtru kodus, lai izmantotu kā kritēriju, lai ierobežotu krājumus, kas ir pieejami debitoriem atlasītajā krājumu grupā. Atlase jāveic katram filtru kodam, kas ir iestatīts krājumu grupai.

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a>Iestatīt kreditoru preču filtrus

Šajā procedūrā ir aprakstīts, kā norādīt kreditoriem pieejamus krājumus papildus tiem krājumiem, kuri ir padarīti pieejami, izmantojot filtru iestatījumus lapā **Vispārīgi pieejamie krājumi**. Vienam kreditoram varat iestatīt vairākus filtrus.

Lai iestatītu kreditoru filtru kodus, izpildiet šīs darbības.

1. Pārejiet uz sadaļu **Sagāde un avoti \> Kreditori \> Visi kreditori**.
1. Atlasiet kreditoru.
1. Darbību rūtī cilnes **Produkts** grupā **Iestatījumi** atlasiet **Preču filtri**.
1. Lapas **Preču filtru kodi** darbību rūtī atlasiet **Jauns**.
1. Laukos **Sākuma datums/laiks** un **Beigu datums/laiks** ievadiet atlasītās krājumu grupas sākuma un beigu datumus.
1. Atlasiet grupu laukā **Krājumu grupa**.
1. Laukos no **1. koda** līdz **10. kodam** atlasiet filtru kodus, lai izmantotu kā kritēriju, lai ierobežotu krājumus, kas ir pieejami kreditoriem atlasītajā krājumu grupā. Atlase jāveic katram filtru kodam, kas ir iestatīts krājumu grupai.

> [!NOTE]
> Kreditora preču filtru iestatījums attiecas uz izlaistajām precēm, kur noliktavas vadības procesi ir iespējoti saistītai noliktavas dimensiju grupai. Filtru kodi tiek izmantoti, lai noteiktu, vai sistēma ļaus lietotājiem iegādāties norādīto krājumu no konkrētā kreditora, kad tie izveido pirkšanas pasūtījuma rindas. Microsoft Dynamics 365 Supply Chain Management ir divas metodes, kā rīkoties ar kreditora apstiprinājumu. Ja pastāv viena vai vairākas izlaistās preces, kur lauks **Apstiprinātais kreditors** ir iestatīts uz *Tikai brīdinājums* vai *Nav atļauts*, šiem krājumiem var iespējot abas kreditora apstiprinājuma metodes. Šī situācija var radīt problēmas, kad lietotāji izveido pirkšanas pasūtījuma rindas.

## <a name="see-also"></a>Skatiet arī

[Papildinformāciju skatiet wMS-Warehouse Filtru kodu rakstu](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]