---
title: Mērvienību pārvaldība
description: Šajā tēmā aprakstīts, kā definēt mērvienību, nodrošināt mērvienības tulkojumus un aprakstu, un definēt pārveidošanas noteikumus saistītām mērvienībām.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d251f90675188426e74b8cbe672856eb4c9ecb8a391f54e735ba19b91b7e3f4a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746943"
---
# <a name="manage-units-of-measure"></a>Mērvienību pārvaldība

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstīts, kā definēt mērvienību, nodrošināt mērvienības tulkojumus un aprakstu, un definēt pārveidošanas noteikumus saistītām mērvienībām.

## <a name="open-the-units-page"></a>Atveriet vienības lapu

Lai izveidotu mērvienības un strādātu ar tām, kas ir pieejamas jūsu sistēmā, dodieties uz **Organizācijas administrēšana \> Iestatījums \> Vienības \> Vienības**.

Pārējās šīs tēmas sadaļās aprakstīts, ko varat darīt lapā **Vienības**.

## <a name="create-standard-units-and-conversions"></a>Standarta vienību un pārveidošanu izveide

Ja sistēmā jau nav iekļautas visbiežāk izmantotās mērvienības metriskajai sistēmai un/vai ASV pielāgotajai sistēmai (USCS), vienību uzstādīšanas vednis var palīdzēt ātri sākt darbu ar pamatvienību definīcijām un pārveidošanām. Lai pabeigtu vedni, darbību rūtī atlasiet **Vienības izveides vednis** un pēc tam izpildiet ekrānā redzamos norādījumus.

## <a name="create-or-edit-a-unit-of-measure"></a>Mērvienības izveide vai rediģēšana

Lai izveidotu vai rediģētu mērvienību, veiciet šādas darbības.

1. Izpildiet kādu no šīm darbībām:

    - Lai rediģētu esošu vienību, atlasiet to saraksta rūtī.
    - Lai izveidotu jaunu vienibu, darbību rūtī atlasiet **Jauns**.

1. Ieraksta galvenē iestatiet tālāk norādītos laukus.

    - **Vienība** - ievadiet ID vai simbolu, ko izmantot, lai atsauktos uz vienību sistēmas valodā. Šis ID vai simbols parasti ir saīsinājums vienībai, piemēram, *kt* katram vai *cm* centimetriem.
    - **Apraksts** - Ievadiet vienības aprakstošo nosaukumu sistēmas valodā. Šis nosaukums parasti ir pilns vienības nosaukums, piemēram, *Katrs* vai *Centimetrs*.

1. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus:<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **Vienību klase** – atlasiet rekvizītu, ko vienība mēra (piemēram, garums, zona, masa vai daudzums).
    - **Mērvienību sistēma** – atlasiet mērvienību sistēmu, kurai pieder vienība (*Metriskās vienības* vai *Amerikas Savienotajās Valstīs lietotās vienības*).
    - **Pamatvienība** – iestatiet šo opciju kā *Jā*, lai izmantotu pašreizējo vienību kā pamatvienību tās vienību klasei. Šajā gadījumā jānorāda tikai pārvēršanas koeficients starp pamatvienību un katru papildu vienību vienību klasē. Pēc tam sistēma var konvertēt starp visām vienībām šajā vienību klasē. Tāpēc pārveidošanas ir vieglāk iestatīt.

        Piemēram, ja galons ir vienību klases *Apjoms* pamatvienība, jāiestata tikai pārveidošanas koeficienti no kvartas uz galonu un no pintas uz galonu. Tad sistēma var konvertēt arī no kvartas uz pinti.

        Vienai mērvienību kategorijai var būt tikai viena pamatvienība.

    - **Sistēmas vienība** – iestatiet šo opciju kā *Jā*, lai izmantotu pašreizējo vienību kā pieņemto vienību visiem nenorādītajiem mērījumiem tās mērvienību kategorijā. Piemēram, ja lauks, kas tiek izmantots daudzuma ievadīšanai, neļauj norādīt vienību (piemēram, ja lietotājs neatlasa vienību), sistēma izmanto vienību, kas ir iestatīta kā sistēmas vienība mērvienību kategorijai *Daudzums*. Vienai mērvienību kategorijai var būt tikai viena sistēmas vienība.
    - **Decimālā precizitāte** – norādiet decimāldaļu vietu skaitu, līdz kuram jānoapaļo vērtības, kas norādītas pašreizējai vienībai konvertētai uz to.

1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="define-unit-translations"></a>Vienību tulkojumu definēšana

Lai definētu ID vai simbola tulkojumus un mērvienības aprakstu, veiciet šādas darbības:

1. Izveidojiet vai atlasiet vienību, kurai jāizveido tulkojumi.
1. Darbību rūtī atlasiet **Vienības teksti**.

    Tiek parādīta lapa **Vienības teksti**. Šī lapa tiek izmantota, lai definētu atlasītās vienības ID vai simbola tulkojumus. Šos tulkojumus pēc tam var izmantot ārējiem dokumentiem debitoram vai kreditoram raksturīgās valodās.

1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Valoda** atlasiet valodu, ko izmantot, uz kuru tulkot vienības ID vai simbolu.
1. Laukā **Teksts** ievadiet vienības ID vai simbola tulkojumu atlasītajā valodā.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Aizvērt lapu.
1. Tad **Darbību rūtī** atlasiet **Tulkotie vienību apraksti**.

    Tiek parādīta lapa **Tulkotie vienību apraksti**. Jūs izmantojat šo lapu, lai atlasītajai vienībai definētu valodai raksturīgus aprakstus.

1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Valoda** atlasiet valodu, ko izmantot, uz kuru tulkot vienības aprakstu.
1. Laukā **Apraksts** ievadiet vienības apraksta tulkojumu atlasītajā valodā.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Aizvērt lapu.

## <a name="define-unit-conversion-rules"></a>Vienību pārveidošanas noteikumu definēšana

Lai definētu konvertēšanas noteikumus starp mērvienībām, veiciet šādas darbības.

1. Izveidojiet vai atlasiet vienību, kurai jādefinē konvertēšanas noteikumi.
1. Darbību rūtī atlasiet **Vienības konvertēšanas**.

    Tiek paradīta lapa **Mērvienību konvertēšana**. Izmantojiet šo lapu, lai definētu noteikumus atlasītas vienības konvertēšanai uz citām vienībām un no citām vienībām mērvienību kategorijā.

1. Atlasiet vienu no šīm cilnēm atkarībā no konvertēšanas tipa, ko vēlaties iestatīt:

    - **Standarta pārveidošana** – iestatiet standarta konvertēšanas noteikumus visām precēm.
    - **Kategoriju iekšējās konvertēšanas** – iestatiet produktam specifiskus konvertēšanas noteikumus vienībām šajā mērvienību kategorijā.
    - **Starpkategoriju konvertēšanas** – iestatiet produktam specifiskus konvertēšanas noteikumus vienībām vienībām pa mērvienību kategorijām.

1. Izpildiet kādu no šīm darbībām:

    - Lai izveidotu jaunu konvertēšanu, rīkjoslā atlasiet **Jauns**.
    - Lai rediģētu esošo konvertēšanu, atlasiet režģī esošo konvertēšanu un pēc tam rīkjoslā atlasiet **Rediģēt**.

1. Parādītajā nolaižamajā dialoglodziņā iestatiet sekojošus laukus:

    - **Prece** – atlasiet noteiktu preci, uz kuru attiecas konvertēšana. Šis lauks ir pieejams tikai kategoriju iekšējām konvertēšanām un starpkategoriju konvertēšanām.
    - **Formulas izkārtojums** – atstājiet šo lauku iestatītu uz *Vienkāršs*, lai norādītu vienkāršu konvertēšanu, kam ir viens faktors. Iestatiet to kā *Uzlabots*, lai iestatītu sarežģītāku vienādojumu. Uzlaboto vienādojumu formāts atšķiras atkarībā no mērvienību kategorijas.
    - **No vienības** – šis lauks rāda atlasīto vienību. Parasti vērtību nedrīkst mainīt. (Ja maināt vērtību, jāatver lapa **Vienību konvertēšana** atlasītajai vienībai, lai pēc tās saglabāšanas skatītu jauno konvertēšanu.)
    - **Uz vienību** – atlasiet vienību, uz kuru konvertēt.
    - **Noapaļošana** – atlasiet, kā noapaļot daļskaitļus, pamatojoties uz atlasītās vienības vērtību **Decimāldaļas precizitāte** (*Līdz tuvākajam*, *Uz augšu* vai *Uz leju*).
    - **Konvertēšanas formula** – izmantojiet atlikušos laukus nolaižamā dialoglodziņa augšpusē, lai norādītu formulu konvertēšanai starp divām vienībām. Pieejamie lauki atšķiras atkarībā no atlasītās mērvienību kategorijas un formulas izkārtojuma.

1. Atlasiet **Labi**.
1. Aizvērt lapu.

> [!TIP]
> Varat arī iestatīt vienību konvertēšanu katram preces variantam. Papildinformāciju skatiet [Mērvienību konvertēšana katram preces variantam](../uom-conversion-per-product-variant.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
