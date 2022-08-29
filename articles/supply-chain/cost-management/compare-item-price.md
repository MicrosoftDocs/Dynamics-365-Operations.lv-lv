---
title: Krājumu cenu uzglabāšanas salīdzināšanas pārskats
description: Uzziniet, kā ģenerēt krājumu cenu uzglabāšanas salīdzinājuma pārskatu un pēc tam pārlūkot un/vai eksportēt rezultātu.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c6373679299b68413d75236ca8cc18ceba03e091
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334991"
---
# <a name="compare-item-prices-storage-report"></a>Krājumu cenu uzglabāšanas salīdzināšanas pārskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā palaist krājumu cenu salīdzināšanas **glabāšanas** pārskatu un padarīt izvadi pieejamu digitāli kā Dynamics 365 Supply Chain Management interaktīvu lapu vai kā eksportētu dokumentu jebkurā vai vairākos formātos.

Skatot pārskatu pārlūkā, kolonnas un uzkrātās bilances tiek dinamiski pielāgotas atkarībā no konfigurētā izkārtojuma. Varat sakārtot rezultātus, filtrēt tos, detalizēt datus un veikts citas darbības.

Pārskata rezultāti tiek uzglabāti datu elementā **Preču cenu salīdzināšana**, kas ļauj filtrēt un eksportēt rezultātus tādos formātos kā, piemēram, CSV vai Microsoft Excel.

Pārskats **Krājumu uzglabāšanas cenu salīdzināšana** noder gadījumos, ja izlaidē ir daudz rindu. Piemēram, izlaide saturēs daudzas rindas, ja jums ir vairāk nekā 40 000 krājumu, kam ir gaidoša krājuma cena izmaksu aprēķināšanas versijā.

## <a name="turn-the-compare-item-prices-storage-feature-on-or-off"></a>Ieslēgt vai izslēgt krājumu cenu salīdzināšanas glabāšanas līdzekli

Lai izmantotu šo funkciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir obligāta, un to nevar izslēgt. Ja lietojat versiju, kas vecāka par 10.0.29, administratori šo funkcionalitāti var ieslēgt vai izslēgt, *·*[meklējot glabāšanas līdzekli Salīdzināt krājuma cenu līdzekļu pārvaldības darbvietā.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="generate-a-compare-item-prices-storage-report"></a>Ģenerēt pārskatu Krājumu cenu uzglabāšanas salīdzināšana

Veiciet šīs darbības, lai ģenerētu un uzglabātu pārskatu **Krājumu cenu glabāšanas salīdzināšana**:

1. Dodieties uz **Izmaksu pārvaldība > Vaicājumi un atskaites > Iepriekš noteikti izmaksu pārskati > Krājumu cenu glabāšanas salīdzināšana**.

1. Atlasiet **Jauns**, lai atvērtu rūti **Salīdzināt krājumu cenas**. Iestatiet šādas opcijas, lai definētu, kuras cenas salīdzināt savā pārskatā:

    - Kopsavilkuma cilnē **Parametri** piešķiriet pārskatam unikālu **Nosaukumu** un lietojiet laukus sadaļās **Gaidošās salīdzināmās cenas** un **Salīdzinājumam izmantotās cenas**, lai noteiktu, kuras cenas un datumus salīdzināt.
    - Kopsavilkuma cilnē **Iekļaujamie ieraksti** iestatiet filtrus un ierobežojumus, lai noteiktu, kurus datus iekļaut pārskatā.
    - Kopsavilkuma cilnē **Palaist fonā** iestatiet kā, kad un cik bieži vēlaties ģenerēt pārskatu.
    > [!NOTE]
    > Šis pārskats vienmēr tiek izpildīts kā daļa no pakešuzdevuma.

1. Atlasiet **Labi**, lai iestatījumus piemērotu un aizvērtu rūti.

1. Kad pakešuzdevums ir pabeigts, tas tiks uzskaitīts lapā **Krājumu cenu glabāšanas salīdzināšana**. Lai skatītu jaunāko pārskatu, lapu var nākties atsvaidzināt.

## <a name="explore-the-compare-item-prices-storage-report"></a>Krājumu cenu uzglabāšanas salīdzināšanas pārskata izpēte

Pēc pārskata izveidošanas to var apskatīt un izpētīt jebkurā laikā šādā veidā:

1. Dodieties uz **Izmaksu pārvaldība > Vaicājumi un atskaites > Iepriekš noteikti izmaksu pārskati > Krājumu cenu glabāšanas salīdzināšana**.

1. No saraksta atlasiet pārskatu.

1. Veiciet vienu no tālāk norādītajām darbībām.

    - Atlasiet **Apskats**, lai apskatu par sava pārskata rezultātiem.
    - Atlasīt **Skatīt informāciju**, lai iegūtu detalizētāku pārskata skatu

1. Pēc tam, kad ir atvērts atlasītais skats, varat veikt šādas darbības:

    - Atlasiet gandrīz jebkuru kolonnas virsrakstu, lai kārtotu vai filtrētu tabulu pēc vērtībām šajā kolonnā, tāpat kā vairumam standarta veidlapu pakalpojumā Supply Chain Management. Ņemiet vērā, ka nevarat filtrēt kolonnu **Neto izmaiņu cenas %**, jo tas ir aprēķinātais lauks.
    - Atlasiet **Parādāmās dimensijas**, lai atvērtu rūti, kurā var izvēlēties, kuru dimensijas kolonnu iekļaut veidlapā. Iestatiet **Saglabāt iestatījumus** uz **Jā**, ja vēlaties saglabāt šos iestatījumus, lai tie tiktu saglabāti nākamreiz, kad atvērsit pārskatu. Atlasiet **Labi**, lai iestatījumus piemērotu un aizvērtu.
    - Atlasiet jebkuru rindu veidlapā un pēc tam atlasiet **Skatīt detalizētu informāciju**, lai skatītu vairāk informācijas par atlasīto krājumu. No turienes varēsit skatīt datus detalizētāk.
    - Atlasiet jebkuru rindu veidlapā un pēc tam atlasiet **Skatīt salīdzinājuma diagrammu**, lai redzētu savu rezultātu interaktīvo grafisku attēlojumu, rezultātiem saistoties ar jūsu atlasīto krājumu. Šos rezultātus var izpētīt, atlasot dažādus grafiskos elementus diagrammā un diagrammas apzīmējumos.
    - Atlasiet jebkuru rindu veidlapā un pēc tam atlasiet **Skatīt aprēķina detalizētu informāciju**, lai skatītu vairāk informācijas par aprēķiniem, kas saistīti ar atlasīto krājumu. No turienes varēsit skatīt datus detalizētāk.

## <a name="export-the-compare-item-prices-storage-report"></a>Krājumu cenu uzglabāšanas salīdzināšanas pārskata eksportēšana

Katrs pārskats, ko izveidojat, tiek saglabāts datu elementā **Salīdzināt krājuma cenas**. Varat izmantot Supply Chain Management standarta datu pārvaldības līdzekļus, lai eksportētu datus no šīs entītijas uz jebkuru atbalstīto datu formātu, tostarp CSV vai Microsoft Excel.

Tālāk ir sniegts piemērs, kā eksportēt **Krājuma cenu glabāšanas salīdzināšanas** pārskatu:

1. Dodieties uz **Sistēmas administrēšana > Darbvietas > Datu pārvaldība**.

1. Atlasiet pogu **Eksportēt** sadaļā **Datu pārvaldība**.

1. Tiek atvērta lapa **Eksports**, kuru izmantosit, lai iestatītu eksportēšanas darbu. Sāciet, piešķirot darbam **Grupas nosaukumu**.

1. Sadaļā **Atlasītie elementi** atlasiet **Pievienot elementu**, lai atvērtu dialoglodziņu, kurā var iestatīt šādas opcijas:

    - **Elementa nosaukums** — atlasiet **Salīdzināt krājumu cenas**.
    - **Mērķa datu formāts** — izvēlieties formātu, uz kuru vēlaties eksportēt.

1. Atlasiet **Pievienot**, lai pievienotu jaunu rindu, un pēc tam atlasiet **Aizvērt**, lai dialoglodziņu aizvērtu.

1. Parasti katru reizi tiks eksportēts viens pārskats. Lai to izdarītu, iestatiet **Filtru** rindai, kuru tikko pievienojāt rūtij **Pieprasījums**. Tas ļaus jums definēt, kurus pārskatu no elementa **Krājumu cenu salīdzināšana** vēlaties iekļaut savā eksportā. Iestatiet šādas filtra opcijas, lai eksportētu vienu pārskatu:

    - Cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu jaunu rindu.
    - Iestatiet **Tabula** uz **Salīdzināt krājumu cenas**.
    - Iestatiet **Atveidotā tabula** uz **Salīdzināt krājumu cenas**.
    - Iestatiet **Lauks** uz lauku, pēc kura vēlaties filtrēt. Parasti jūs izmantosit **Izpildes nosaukums** vai **Izpildes laiks**.
    - Iestatiet **Kritērijus** vērtībai atlasītajā laukā, ko vēlaties meklēt (vai nu pārskata nosaukums, vai pārskata izveides laiks).
    - Ja nepieciešams, pievienojiet tabulai **Diapazons** papildu rindas, līdz esat unikāli identificējis pārskatu, kuru meklējat.

1. Atlasiet **Labi**, lai saglabātu iestatījumus un aizvērtu.

1. Atlasiet **Saglabāt**, lai saglabātu eksporta iestatījumus.

1. Atveriet cilni **Eksporta opcijas** un atlasiet **Eksportēt tūlīt**, lai ģenerētu eksporta failu.

1. Tiek atvērta lapa **Izpildes kopsavilkums**, kurā ir redzams eksportētā darba statuss un eksportēto elementu saraksts. Atlasiet elementu **Krājuma cenu salīdzināšana**, kas ir uzskaitīts apgabalā **Elementa apstrādes statuss**, un pēc tam atlasiet **Lejupielādēt failu**, lai no šī elementa lejupielādētu eksportētos datus.

Papildinformāciju par to, kā izmantot datu pārvaldību, lai eksportētu datus, skatiet šeit: [Datu importēšanas un eksportēšanas darbu apskats](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]