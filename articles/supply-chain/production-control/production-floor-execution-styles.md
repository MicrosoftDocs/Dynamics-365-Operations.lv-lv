---
title: Ražošanas izpildes interfeisa stila veidošana
description: Šajā rakstā ir izskaidrots, kā konfigurēt formu kontroles, lai tiem pielietoti noklusējuma ražošanas izpildes stili.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ad6ecd591353fe8ddc1a5b9049d65491fb58e98a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859145"
---
# <a name="style-the-production-floor-execution-interface"></a>Ražošanas izpildes interfeisa stila veidošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā konfigurēt formu kontroles, lai tiem pielietoti noklusējuma ražošanas izpildes stili.

## <a name="forms-and-dialogs"></a>Formas un dialogi

Stilus formai vai dialogam var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Ja formai ir jābūt līdzīgai esošajai pārskata norises formai, formas vai dialoga nosaukumam jāsākas ar `JmgProductionFloorExecutionCustomInputDialog`.
- Formā vai dialogā var būt detaļu formas daļa. Lai pielietotu tai stilus, detaļu formas daļas nosaukumam ir jāsākas ar `JmgProductionFloorExecutionCustomDetailsDialog`.
- Ja formai vai dialogam ir jābūt vienkāršam skatam, tad vienkāršā skata nosaukumam jāsākas ar `JmgProductionFloorExecutionCustomDialog`. Formu, kurām ir vienkāršs skatījums, piemēri ietver sākuma formu un netiešo aktivitāšu formu.
- Visām vadīklām dialogā jābūt konfigurētām tā, kā tas ir aprakstīts šajā rakstā.

> [!IMPORTANT]
> Līdzekļiem, kas ir minēti šī saraksta pirmos divos aizzīmju punktos, nepieciešama Supply Chain Management versija 10.0.19 vai jaunāka.

Stilus pogai **Labi** vai dialogam var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar `OkButtonGroup`.

Stilus pogai **Atcelt** dialoglodziņā var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar `CancelButtonGroup`.

### <a name="header"></a>Galvene

Šajā ilustrācijā parādīts parasts formas vai dialoga virsraksts.

![Tipisks formas vai dialoga virsraksts.](media/pfe-styles-header.png "Tipisks formas vai dialoga virsraksts")

Virsraksti Visual Studio tiek veidoti, izmantojot struktūru, kā parādīts šajā ilustrācijā.

![Tipiska kodu struktūra virsraksta struktūrai.](media/pfe-styles-header-code-structure.png "Tipiska kodu struktūra virsraksta struktūrai")

Lai pievienotu tekstu virsrakstam, izmantojiet kodu, piemēram, šādu piemēru.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Uzrakstot virsraksta kodu, lietojiet šādus noteikumus:

- Ir jābūt galvenās grupas nosaukumam `TableRowHeaderGroup`.
- Ar katru teksta bloku (kas atdalīts ar biļeteniem) jāsākas `HeaderFieldWithSeparatorText`.
- Pēdējā teksta nosaukumam ir jāsākas ar `HeaderFieldText`.
- `CaptionImage` var izlaist.

### <a name="progress-indicator"></a>Norises indikators

Var iekļaut progresa indikatoru, kas tiek rādīts virsraksta labajā pusē. Šajā attēlā parādīts progresa indikators.

![Tipisks norises indikators.](media/pfe-styles-header-progress.png "Parasts norises indikators")

Lai rādītu progresa indikatoru, teksta laukam jābūt nosauktam `ShowProgress`.

## <a name="grid"></a>Režģis

Stili tiek lietoti automātiski. Nav nepieciešama īpaša konfigurācija.

Režģim ir `TabularView` nepieciešams stils, `run()` un pielāgotajā formā ir jāpārraksta metode, jo vēl netiek atbalstīts jauns režģis. Pievienojiet šādu kodu.

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Lai atsvaidzinātu datus galvenajā skatījumā, iespējams, vēlēsieties izmantot kaut ko `this.parmParentForm().updateLayout();` citu, `click` ko vēlaties izmantot darbības metodē. (Piemēram, skatiet klasi `JmgProductionFloorExecutionReportFeedbackAction` .) Pārliecinieties, `parmDataSource` kas ir iestatīts `init` jaunās formas metodē (`formCaller.parmDataSource(this.dataSource(1));`). Piemēram, skatiet `JmgProductionFloorExecutionMainGrid` formu.

## <a name="card-view"></a>Kartes skats

Stilus karšu skata vadīklām var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Katrs kartes skats ir ietverts formu grupā.
- Grupas nosaukums sākas ar `CardGroup` (piemēram, `CardGroupJobsView`).

Šajā ilustrācijā parādīts karšu skats, kurā nav vadīklu.

![Kartes skats bez elementiem.](media/pfe-styles-empty-card.png)

Šajās ilustrācijās parādīts karšu skats, kurā nav vadīklu.

![Karte ar elementiem, kas rāda Hz.](media/pfe-styles-elements.png)

![Karte ar elementiem uzturēšanas pieprasījumam.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Biznesa karte

Stilus biznesa kartes vadīklām var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Katra biznesa karte ir ietverts formu grupā.
- Grupas nosaukums sākas ar `BusinessCardGroup` (piemēram, `BusinessCardGroupJobsList`).

Iestatiet biznesa kartē šādus rekvizītus:

- **Stils:** *saraksts*
- **Paplašinātais stils:** *cardList*
- **Daudzkārš. atlase:** *Nē*
- **Rādīt sietās iezīmes:** *Nē*

![Biznesa karte.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Radio poga

Stilus radio pogām var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Katra radio poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar `RadioTextBelow` vai `RadioTextRight` atkarībā no tā, kur vēlaties, lai teksts parādās.

Iestatiet radio pogā šādus rekvizītus:

- **Pārslēgšanās poga:** *pārbaude*
- **Pārslēgt vērtību: ja** *ir* jāatlasa radiopoga; pretējā gadījumā *izslēgts*

Šajā attēlā parādīts piemērs, kur teksts parādās zem radiopogām.

![Radiopogas ar tekstu tālāk.](media/pfe-styles-radio-text-below.png)

Šajā attēlā parādīts piemērs, kur teksts parādās pa labi no radiopogām.

![Radiopogas ar tekstu pa labi.](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Radiopogas Internet Explorer

Radio pogu stili netiek atbalstīti Internet Explorer. Nākamajā attēlā ir redzams, kā radiopogas izskatās programmā Internet Explorer.

![Radiopogas Internet Explorer.](media/pfe-styles-browser.png)

## <a name="buttons"></a>Pogas

Stilus pogām var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Katra pogu grupa ir ietverta formu grupā. Visām pogām grupā būs vienāds stils.
- Nav prasību par grupas nosaukumu.

Iestatiet pogās šādus rekvizītus:

- **Pogu displejs:** *TextWithImageLeft*
- **Parastais attēls:** šis rekvizīts nedrīkst būt tukšs. Piemēram, izmantojiet *CoffeeScript*.
- **Teksts:** šis rekvizīts nedrīkst būt tukšs. Piemēram, izmantojiet *Sākuma pārtraukums*.
- **Platums:** *Auto* vai *SizeToContent*
- **Augstums:** *Automātisks* *vai SizeToContent*

### <a name="primary-button"></a>Primārā poga

Stilus primārai pogai var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar `DefaultButtonGroup` vai `PrimaryButtonGroup` (piemēram, `DefaultButtonGroup10`).

![Primārā poga.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Sekundārā poga

Stilus sekundārai pogai var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums ir Labais **panelis** vai grupas nosaukums sākas ar `SecondaryButtonGroup`.

![Sekundārā poga.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Trešās grupas poga

Stilus trešās grupas pogai var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums ir Pa **kreisi vai** grupas nosaukums sākas ar `ThirdButtonGroup`.

![Trešās grupas poga.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Ceturtās grupas poga

Stilus ceturtās grupas pogai var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar `FourthButtonGroup`.

Iestatiet pogā šādus rekvizītus:

- **Pogas displejs:** *TextOnly*
- **Parasts attēls: šim** rekvizītam ir jābūt tukšam.
- **Teksts:** šis rekvizīts nedrīkst būt tukšs. Piemēram, izmantojiet *Skats* vai *Rediģēt*.
- **Platums: Automātisks** *·*
- **Augstums: Automātisks** *·*

![Ceturtās grupas poga.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Plakanā poga

Stilus plakanai pogai var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar `FlatButtonGroup`.

Iestatiet pogā šādus rekvizītus:

- **Pogas displejs:** *ImageOnly*
- **Parastais attēls:** šis rekvizīts nedrīkst būt tukšs. Piemēram, izmantojiet *CoffeeScript*.
- **Teksts: šim** rekvizītam jābūt tukšam.
- **Platums:** *Auto* vai *SizeToContent*
- **Augstums:** *Automātisks* *vai SizeToContent*

![Plakanā poga.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Poga Turpināt

Stilus var izmantot pogai Turpināt tikai tad, ja ir izpildītas tālāk norādītās prasības.

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar `ContinueButtonGroup`.

Iestatiet pogā šādus rekvizītus:

- **Pogas displejs:** *ImageOnly*
- **Parasts attēls: uz** *priekšu*
- **Teksts: šim** rekvizītam jābūt tukšam.
- **Platums:** *Auto* vai *SizeToContent*
- **Augstums:** *Automātisks* *vai SizeToContent*

![Poga Turpināt.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Kombinētais lodziņš

Kombinētais lodziņš ir trīs vadīklu kombinācija: ievades vadīkla, poga, kas notīra ievades vadīklu, un poga, kas palaiž meklēšanu.

Stilus kombinētajam lodziņam var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šis kombinētais lodziņš ir ietverts formu grupā.
- Grupas nosaukums sākas ar `Combobox`.
- Grupā pirmā kontrole ir `AxFormStringControl` kontrole. Šī vadīkla parāda pašreizējo vērtību, un tā ir vieta, kur lietotājs ievada nepieciešamo vērtību.
- Otra kontrole ir kontrole, `CommonButton` un tās nosaukums sākas ar `ClearButton`. Šai pogai ir jāietver kods, kas izmanto rekvizītu `enable`, lai parādītu vai slēptu pogu. Piemēram, lai parādītu vai slēptu pogu **Dzēst**, kamēr lietotājs ievada informāciju ievades vadīklā, varat izmantot šādu kodu.

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    Jums jābūt vienai metodei, kur dati ir iestatīti ievades vadīklā. Iespējojiet šajā metodē pogu **Dzēst**. Tālāk ir minēts piemērs.

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    Izmantojiet tālāk norādīto kodu pogas `clicked` Dzēst **metodei**.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Iestatiet ievades kontroles vērtību, `AxFormStringControl` ja forma tiek inicializēta, izmantojot `init` metodi. Ja vērtība nav tukša, iespējojiet pogu **Notīrīt**. Ja vērtība ir tukša, atspējojiet pogu **Notīrīt**.

- Trešā kontrole ir kontrole, `CommonButton` un tās nosaukums sākas ar `SearchButton`.

Šajā attēlā redzamas divas kombinētā lodziņa vadīklas. Kombinētajam lodziņam kreisajā pusē ir tukšs teksta lodziņš, un poga **Notīrīt** tiek atspējota. Kombinētajam lodziņam labajā pusē lodziņā ir teksts, un poga **Notīrīt** tiek ietspējota.

![Kombinētie lodziņi ar un bez pogas Notīrīt.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Ātrais filtrs

Ātrā filtra vadīkla pievieno lapai meklēšanas lauku. Stilus var izmantot ātram filtram, ja tiek izpildītas tālāk norādītās prasības.

- Šis ātrais filtrs ir ietverts formu grupā.
- Grupas nosaukums sākas ar `SearchInputGroup`.
- Grupā pirmā vadīkla ir `QuickFilter` vadīkla. (Šī kontrole ir vieta, kur lietotājs ievada meklēšanas virkni.)
- Otra kontrole ir nosaukta `FormStaticTextControl``NumberOfResults`. (Šī kontrole nav obligāta. Ja tā ir iekļauta, tā parāda atrasto krājumu skaitu.)
- Trešā kontrole ir kontrole, `CommonButton` un tās nosaukums sākas ar `ClearButton`.

Šajā attēlā redzamas divas ātrā filtra vadīklas. Ātram filtram kreisajā pusē ir tukšs ātrais filtrs, un rezultātu skaits nav redzams. Ātrais filtrs labajā pusē satur meklēšanas virkni un parāda rezultātu skaitu.

![Ātrā filtra kontroles piemēri ar meklēšanas virkni un bez tās.](media/pfe-styles-quick-filter.png "Ātrā filtra kontroles piemēri ar meklēšanas virkni un bez tās")

## <a name="center-align-elements-on-a-tab"></a>Elementu līdzināšana cilnē uz centru

Lai līdzinātu elementus cilnes centrā, grupas nosaukumam jāsākas `TabContentGroup`, un grupai ir jābūt ar šādiem rekvizītiem:

- **Platuma režīms:**`SizeToAvailable`
- **Augstuma režīms:**`SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Režģa, detaļu daļas un ātrās filtra līdzināšana

Lai sakārtotu pielāgotu režģi, detaļu daļu un ātro filtru tā, lai tie būtu līdzīgi standarta dizainam, atcerieties šādus punktus, kad tos visus ievietosiet kopā:

- Ja režģim ir ātrais filtrs, grupā, ar kuru sākas nosaukums, vajadzētu būt gan režģim, gan ātram filtram `GridGroup`.
- Lai detaļu daļai pielietotu stilus, grupas nosaukumam ir jāsākas ar `DetailInformationGroup` šo:

Šajā attēlā parādīts parasts režģis, kurā ir iekļauts ātrais filtrs un detaļu daļa labajā pusē.

![Tipisks režģis, kas ietver ātru filtru un detaļu daļu.](media/pfe-styles-align-grid.png "Tipisks režģis, kas ietver ātru filtru un detaļu daļu")

Visual Studio Režģī, detaļu daļā un ātrajā filtrā var izveidot, izmantojot struktūru, kā parādīts šajā ilustrācijā.

![Tipiska kodu struktūra, kas izlīdzina režģi, detaļu daļu un ātro filtru.](media/pfe-styles-header-code-structure2.png "Tipiska kodu struktūra, kas izlīdzina režģi, detaļu daļu un ātro filtru")

## <a name="additional-resources"></a>Papildu resursi

- [Ražošanas izpildes interfeisa pielāgošana](production-floor-execution-customize.md)
- [Ražošanas izpildes interfeisa noformēšana](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
