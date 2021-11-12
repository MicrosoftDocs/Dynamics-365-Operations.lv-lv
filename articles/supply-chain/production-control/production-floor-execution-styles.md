---
title: Ražošanas izpildes interfeisa stila veidošana
description: Šajā tēmā skaidrots, kā konfigurēt formu vadīklas, lai tiem tiktu pielietoti noklusējuma ražošanas izpildes stili.
author: johanhoffmann
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 32e49458f6ea7c484bc4200e414d930381b31891
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652033"
---
# <a name="style-the-production-floor-execution-interface"></a>Ražošanas izpildes interfeisa stila veidošana

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā konfigurēt formu vadīklas, lai tiem tiktu pielietoti noklusējuma ražošanas izpildes stili.

## <a name="forms-and-dialogs"></a>Formas un dialogi

Stilus formai vai dialogam var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Ja formai ir jābūt līdzīgai esošajai pārskata norises formai, tad formas vai dialoga nosaukumam ir jāsākas ar **JmgProductionFloorExecutionCustomInputDialog**.
- Formā vai dialogā var būt detaļu formas daļa. Lai pielietotu tai stilus, detaļu formas daļas nosaukumam ir jāsākas ar **JmgProductionFloorExecutionCustomDetailsDialog**.
- Ja formai vai dialogam ir jābūt vienkāršam skatam, vienkāršā skata nosaukumam ir jāsākas ar **JmgProductionFloorExecutionCustomDialog**. Formu, kurām ir vienkāršs skatījums, piemēri ietver sākuma formu un netiešo aktivitāšu formu.
- Visām vadīklām dialogā jābūt konfigurētām tā, kā tas ir aprakstīts šajā tēmā.

> [!IMPORTANT]
> Līdzekļiem, kas ir minēti šī saraksta pirmos divos aizzīmju punktos, nepieciešama Supply Chain Management versija 10.0.19 vai jaunāka.

Stilus pogai **Labi** vai dialogam var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar **OkButtonGroup**.

Stilus pogai **Atcelt** dialoglodziņā var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar **CancelButtonGroup**.

## <a name="grid"></a>Režģis

Stili tiek lietoti automātiski. Nav nepieciešama īpaša konfigurācija.

## <a name="card-view"></a>Kartes skats

Stilus karšu skata vadīklām var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Katrs kartes skats ir ietverts formu grupā.
- Grupas nosaukums sākas ar **CardGroup** (piemēram, **CardGroupJobsView**).

Šajā ilustrācijā parādīts karšu skats, kurā nav vadīklu.

![Kartes skats bez elementiem.](media/pfe-styles-empty-card.png)

Šajās ilustrācijās parādīts karšu skats, kurā nav vadīklu.

![Karte ar elementiem, kas rāda Hz.](media/pfe-styles-elements.png)

![Karte ar elementiem uzturēšanas pieprasījumam.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Biznesa karte

Stilus biznesa kartes vadīklām var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Katra biznesa karte ir ietverts formu grupā.
- Grupas nosaukums sākas ar **BusinessCardGroup** (piemēram, **BusinessCardGroupJobsList**).

Iestatiet biznesa kartē šādus rekvizītus:

- **Stils**: **saraksts**
- **Paplašinātais stils**: **cardList**
- **Vairākatlase**: **Nē**
- **Rādīt sietās iezīmes**: **Nē**

![Biznesa karte.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Radio poga

Stilus radio pogām var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Katra radio poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar **RadioTextBelow** vai **RadioTextRight** atkarībā no tā, kur vēlaties, lai teksts parādās.

Iestatiet radio pogā šādus rekvizītus:

- **Pārslēgšanās poga**: **Pārbaude**
- **Pārslēgt vērtību**: **Ieslēgts**, ja ir jāatlasa radiopoga; pretējā gadījumā **Izslēgt**

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

- **Pogu parādīšana**: **TextWithImageLeft**.
- **Parastais attēls**: šis rekvizīts nedrīkst būt tukšs. Piemēram, izmantojiet **CoffeeScript**.
- **Teksts**: šis rekvizīts nedrīkst būt tukšs. Piemēram, izmantojiet **Sākuma pārtraukums**.
- **Platums**: **Automātisks**.
- **Augstums**: **Automātisks**.

### <a name="primary-button"></a>Primārā poga

Stilus primārai pogai var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar **DefaultButtonGroup** vai **PrimaryButtonGroup** (piemēram, **DefaultButtonGroup10**).

![Primārā poga.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Sekundārā poga

Stilus sekundārai pogai var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums ir **Labais panelis** vai grupas nosaukums sākas ar **SecondaryButtonGroup**.

![Sekundārā poga.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Trešās grupas poga

Stilus trešās grupas pogai var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums ir **Kreisais panelis** vai grupas nosaukums sākas ar **ThirdButtonGroup**.

![Trešās grupas poga.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Ceturtās grupas poga

Stilus ceturtās grupas pogai var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar **FourthButtonGroup**.

Iestatiet pogā šādus rekvizītus:

- **Pogas parādīšana**: **TextOnly**.
- **Parastais attēls**: šim rekvizītam jābūt tukšam.
- **Teksts**: šis rekvizīts nedrīkst būt tukšs. Piemēram, izmantojiet **Skats** vai **Rediģēt**.
- **Platums**: **Automātisks**.
- **Augstums**: **Automātisks**.

![Ceturtās grupas poga.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Plakanā poga

Stilus plakanai pogai var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šī poga ir ietverta formu grupā.
- Grupas nosaukums sākas ar **FlatButtonGroup**.

Iestatiet pogā šādus rekvizītus:

- **Pogas parādīšana**: **ImageOnly**.
- **Parastais attēls**: šis rekvizīts nedrīkst būt tukšs. Piemēram, izmantojiet **CoffeeScript**.
- **Teksts**: Šim rekvizītam ir jābūt tukšam.
- **Platums**: **Automātisks**.
- **Augstums**: **Automātisks**.

![Plakanā poga.](media/pfe-styles-flat-button.png)

## <a name="combo-box"></a>Kombinētais lodziņš

Kombinētais lodziņš ir trīs vadīklu kombinācija: ievades vadīkla, poga, kas notīra ievades vadīklu, un poga, kas palaiž meklēšanu.

Stilus kombinētajam lodziņam var lietot tikai tad, ja ir izpildītas tālāk norādītās prasības:

- Šis kombinētais lodziņš ir ietverts formu grupā.
- Grupas nosaukums sākas ar **Kombinētais lodziņš**.
- Grupā pirmā vadīkla ir **AxFormStringControl** vadīkla. Šī vadīkla parāda pašreizējo vērtību, un tā ir vieta, kur lietotājs ievada nepieciešamo vērtību.
- Otra vadīkla ir **CommonButton** vadīkla, un tās nosaukums sākas ar **ClearButton**. Šai pogai ir jāietver kods, kas izmanto rekvizītu **iespējot**, lai parādītu vai slēptu pogu. Piemēram, lai parādītu vai slēptu pogu **Dzēst**, kamēr lietotājs ievada informāciju ievades vadīklā, varat izmantot šādu kodu.

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

    Izmantojiet tālāk norādīto kodu pogas **Dzēst** metodei **noklikšķināts**.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Iestatiet ievades kontroles vērtību **AxFormStringControl**, kad forma tiek inicializēta, izmantojot **init** metodi. Ja vērtība nav tukša, iespējojiet pogu **Notīrīt**. Ja vērtība ir tukša, atspējojiet pogu **Notīrīt**.

- Treša vadīkla ir **CommonButton** vadīkla, un tās nosaukums sākas ar **SearchButton**.

Šajā attēlā redzamas divas kombinētā lodziņa vadīklas. Kombinētajam lodziņam kreisajā pusē ir tukšs teksta lodziņš, un poga **Notīrīt** tiek atspējota. Kombinētajam lodziņam labajā pusē lodziņā ir teksts, un poga **Notīrīt** tiek ietspējota.

![Kombinētie lodziņi ar un bez pogas Notīrīt.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Ātrais filtrs

Ātrā filtra vadīkla pievieno lapai meklēšanas lauku. Stilus var izmantot ātram filtram, ja tiek izpildītas tālāk norādītās prasības.

- Šis ātrais filtrs ir ietverts formu grupā.
- Grupas nosaukums sākas ar **SearchInputGroup**.
- Grupā pirmā vadīkla ir **QuickFilter** vadīkla. (Šeit lietotājs ievada meklēšanas virkni.)
- Otra kontrole ir **FormStaticTextControl** ar nosaukumu **NumberOfResults**. (Tas nav obligāti un parāda atrasto krājumu skaitu, ja tāds ir iekļauts.)
- Treša vadīkla ir **CommonButton** vadīkla ar nosaukumu, kas sākas ar **ClearButton**.

Šajā attēlā redzamas divas ātrā filtra vadīklas. Ātram filtram kreisajā pusē ir tukšs ātrais filtrs, un rezultātu skaits nav redzams. Ātrais filtrs labajā pusē satur meklēšanas virkni un parāda rezultātu skaitu.

![Ātrā filtra kontroles piemēri ar meklēšanas virkni un bez tās.](media/pfe-styles-quick-filter.png "Ātrā filtra kontroles piemēri ar meklēšanas virkni un bez tās")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
