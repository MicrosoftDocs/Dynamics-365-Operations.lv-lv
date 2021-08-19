---
title: Novietojuma dimensijas ierobežojumi
description: Šī tēma apraksta novietojuma dimensijas ierobežojumu funkcionalitāti.
author: perlynne
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 239b9fa8d8e34a92d453d3387881cff7b0a11f28a3c3b1e19891ea3bd78c3d7c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714166"
---
# <a name="location-stocking-limits"></a>Novietojuma dimensijas ierobežojumi

[!include [banner](../includes/banner.md)]

Varat izmantot lapu **Novietojuma dimensijas ierobežojumi** (**Noliktavas pārvaldība \> Uzstādīšana \> Noliktava \>Novietojuma dimensijas ierobežojumi**), lai kontrolētu kravas noslodzi noliktavas atrašanās vietās bez nepieciešamības izmantot uzlabotās apstrādes procesus fizisko preču tilpuma aprēķiniem.

Novietojuma dimensijas ierobežojumu nolūks ir novērtēt maksimālo daudzumu, ko atrašanās vieta var saturēt. Varat iestatīt funkciju jebkurā no trim līmeņiem, un katrai no tām ir sava cilne lapā **Novietojuma dimensijas ierobežojumi**:

- Produkti
- Preces varianti
- Konteineru veidi

Katram līmenim var definēt dažādas lauku vērtības. Pēc tam sistēma novērtēs konkrētas vietas noslodzi, pamatojoties uz katras rindas **Daudzuma** un **Vienības** vērtībām. Vispirms tas atlasa visdetalizētāko salīdzināšanas ierakstu. Piemēram, rinda ar vērtību laukā **Novietojuma profila ID** tiks novērtēta pirms rindas, kuras vērtība ir tikai **Noliktavas** laukā. Atlikusī noslodze tiks novērtēta arī, pamatojoties uz **Daudzuma** vērtību izmantotajam novietojuma dimensiju ierobežojumu ierakstam.

Lapas sadaļā **Produkti** varat definēt šādas lauka vērtības novietojuma dimensiju ierobežojumu meklēšanai:

- Noliktava
- Atrašanās vietas profila ID
- Novietojums
- Pakas lieluma kategorijas ID
- Krājums
- Vienība

> [!NOTE]
> Nav jādefinē **Vienības** vērtība katram novietojuma dimensiju ierobežojumu ierakstam. Vietas noslodzes aprēķini tiks balstīti uz krājumu vienību daudzumiem. Ja vērtībai, kas tiek izmantota, nav definēta vienības pārveidošana, novietojuma dimensiju ierobežojumu ieraksts tiks izlaists, it kā tam būtu definēta cita **Krājuma numura** vērtība.

## <a name="example--purchase-order-receiving"></a>Piemērs - pirkšanas pasūtījuma saņemšana

Šis piemērs ir balstīts uz tīro *USMF* demo datu komplektu, kur lapas **Novietojuma dimensiju ierobežojumi** cilnē **Preces varianti** ir iestatītas šādas vērtības.

| Noliktava | Atrašanās vietas profila ID | Krājums | izmērs | Daudzums | Vienība |
|-----------|---------------------|-------------|------|----------|------|
| 24        | STĀVS               | D0013       | P    | 300      | gab.   |
| 24        | STĀVS               | D0013       | L    | 240      | gab.   |
| 24        | STĀVS               | D0013       | S    | 360      | gab.   |

Precēm ir iestatīti dažādi mērvienību preču varianti. Šie varianti ir saskaņoti ar novietojuma dimensiju ierobežojumiem trijām paletēm (PL):

- **M izmērs:** 1 PL = 100 katrs (Ea)
- **L izmērs:** 1 PL = 80 Ea
- **S izmērs:** 1 PL = 120 Ea

Tāpēc katra vieta, kur **Atrašanās vietas profila ID** vērtība ir iestatīta uz *STĀVS* var pārvadāt *3* *PL* krājuma numuram *D0013*.

### <a name="prepare-for-the-example"></a>Sagatavojies piemēram

Šajā piemērā tiks palaista pirkšanas pasūtījuma saņemšanas plūsma divām rindām. Tomēr vispirms ir jāatjaunina demonstrācijas dati, lai nodrošinātu, ka vietas ļauj pārvadāt jauktus krājumus, tiek izmantotas tikai tukšās vietas *FL-002*, izmantojot *FL-004*, un nav atvērts ienākošs darbs.

1. Novietojuma *FL-001* gadījumā **Novietojuma profila** lauka vērtību mainiet no *STĀVS* uz *STĀVS-05*.
1. *GRĪDA* novietojuma profilam iestatiet opciju **Atļaut jauktus krājumus** uz *Jā*.
1. Izveidot pirkšanas pasūtījumu, kam ir sekojošās divas rindas.

    | Noliktava | Krājums | izmērs | Daudzums | Vienība |
    |-----------|-------------|------|----------|------|
    | 24        | D0013       | S    | 4        | PL   |
    | 24        | D0013       | L    | 4        | PL   |

### <a name="process-the-example"></a>Piemēra apstrādāšana

Vispirms tiek saņemts daudzums *4* vienībai *PL*, kuras lielums ir *S*, un pārskatiet izveidotā darba rindas atrašanās vietas. Tad tiek saņemts daudzums *4* vienībai *PL*, kuras lielums ir *L*, un pārskatiet izveidotā darba rindas atrašanās vietas.

1. Warehouse Management mobile programmā piesakieties, izmantojot *24* kā lietotāja ID un *1* kā paroli.
1. Atlasiet **Ienākošie** \> **Pirkumu saņemšana**.
1. Saņemt *4* *PL* ar krājuma numuru *D0013* *S* izmērā.
1. Pārskatiet izveidoto darbu. Vajadzētu tikt parādītiem šādam rezultātam:

    - 3 PL -\> FL-002
    - 1 PL -\> FL-003

1. Saņemt *4* *PL* ar krājuma numuru *D0013* *L* izmērā.
1. Pārskatiet izveidoto darbu. Vajadzētu tikt parādītiem šādam rezultātam:

    - 1 PL -\> FL-003
    - 3 PL -\> FL-004

Balstoties uz rezultātiem, var secināt, ka sistēmai neizdevās piešķirt pareizās gala atrašanās vietas. Pretējā gadījumā, kāpēc sistēma pievienoja tikai *1* *PL* ar lielumu *L* uz atrašanās vietu *FL-003* pēdējā solī, nevis *2* *PL*? T. i., kāpēc kopā nav *3* *PL* šai atrašanās vietai?

Lai izskaidrotu šo acīmredzamo kļūmi, ir jāsaprot atrašanās vietas uzkrājumu novietojuma dimensijas ierobežojumiem. Sistēma atlasa visdetalizētāko salīdzināšanas ierakstu. Šajā piemērā visdetalizētākais salīdzināšanas ieraksts ir rinda, kur **Izmēra** vērtība ir *L*, **Daudzuma** vērtība ir *240* un **Vienības** vērtība ir *Ea*. Tā kā jums jau ir atvērts darbs no iepriekšējā saņemšanas daudzuma *120* *Ea* ar izmēru *S*, atlikusī noslodze tiek aprēķināta kā *240* – *120* = *120* *Ea*. Tāpēc atlikusī noslodze var pārvadāt tikai *1* *PL* *80* *Ea*.

> [!NOTE]
> Nevar izmantot novietojuma dimensijas ierobežojumus, lai kontrolētu, piemēram, to krājumu papildināšanu, kuriem ir dažādi daudzumi vienā un tajā pašā vietā. Šādā gadījumā izmantojiet *papildināšanas veidni*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]