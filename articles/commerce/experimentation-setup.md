---
title: Eksperimenta iestatīšana
description: Šajā rakstā ir aprakstīts, kā iestatīt eksperimentu trešās puses pakalpojumā.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946170"
---
# <a name="set-up-an-experiment"></a>Eksperimenta iestatīšana

Kad esat [definējis hipotēzi un noteicis, kādus panākumu rādītājus vēlaties izmantot](experimentation-identify.md), jums ir jāiestata eksperiments trešās puses pakalpojumā. Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce. Papildu soļi ir ietverti atsevišķos rakstos.

[ ![Eksperimenta lietotāja maršruts – iestatīšana.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Eksperimenta iestatīšana trešās puses pakalpojumā
Jums ir jāizvēlas trešās puses pakalpojums, lai varētu izpildīt un pārraudzīt jūsu eksperimentu un iestatīt eksperimenta savienotāju. Šie priekšnosacījumi ir uzskaitīti  [Eksperimentēšana pakalpojumā Dynamics 365 Commerce](experimentation-overview.md).

Izpildiet nepieciešamās darbības, lai izveidotu eksperimentu trešās puses pakalpojumā. Ja savienotājs ir konfigurēts pareizi, pilns trešās puses pakalpojumā iestatīto eksperimentu saraksts tiks parādīts Commerce vietņu veidotājā apmēram 5 minūšu laikā.

## <a name="set-up-your-success-metrics"></a>Panākumu rādītāju iestatīšana
Katram eksperimentam ir nepieciešami rādītāji, lai noteiktu variantu ietekmi un pārbaudītu hipotēzi. Veiciet tālāk norādītās darbības, lai iespējotu rādītāju aprēķināšanu trešās puses pakalpojumā, izmantojot tiešsaistes telemetrijas notikumus no Dynamics 365 Commerce.

Lai iestatītu jūsu veiksmes rādītājus kases moduļiem, sekojiet šiem soļiem.

1. Commerce vietņu veidotājā atlasiet **Lapas** kreisajā navigācijas rūtī un pēc tam atlasiet lapu, kuras rādītājus vēlaties apkopot. 
1. Dodieties uz sadaļu **Izsekojamie notikumu ID**, kas atrodas lapas labās puses rekvizītu rūtī vai modulī, kuru vēlaties izsekot.
1. Atlasiet **Skatīt**. Tiek parādīts visu klikšķa notikumu ID saraksts. Kopējiet notikumu, kuru vēlaties izsekot, un ielīmējiet notikuma atslēgu nozīmētajā vietā trešās puses pakalpojumā. Ja ir nepieciešams vairāk nekā viens notikums, kopējiet atslēgas pa vienai. 
1. Lapas skatiem izmantojiet lapas SHA-256 jaukšanas vērtību lapas nosaukumam, kas pievienots vietas veidotājam `.PageView`. Piemēram, notikuma ID.`Homepage.PageView``e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`
1. Citas darbības, lai izsekotu rādītājus, veiciet pēc nepieciešamības trešās puses pakalpojumā.

Noklikšķinot uz pielāgotajiem moduļiem, izpildiet šīs darbības, lai klikšķa notikumiem sekotu:

1. Sagatavojiet **TelemetryContent** objektu modulim, izmantojot tālāk esošo funkciju. Šī funkcija kā ievades veic lapas nosaukumu, moduļa nosaukumu un SDK nodrošināto telemetrijas objektu.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Piemērs ir šāds: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Izveidojiet lietderīgās slodzes datus, kas satur informāciju par to, kas ir jānotver. Pogām un citām statiskām vadīklām varat iekļaut etext **,** piemēram, "Iepirkties tagad" vai "Meklēt". Komponentiem ar klikšķiem, piemēram, noklikšķinot uz preču kartes, varat nosūtīt recId **,** kas ir preces vai preces ID ieraksta ID.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    Kā statisko vadīklu piemērs padot pogas teksta virkni, kā parādīts zemāk:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    Kā preču klikšķiem veiciet preces recordId kā parādīts zemāk:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Izsaukt onClick **funkciju**, lai reģistrētu notikumu.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Piemērs ir šāds:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Iepriekšējā darbība
[Hipotēzes identificēšana un eksperimenta rādītāju noteikšana](experimentation-identify.md) 


## <a name="next-step"></a>Nākamā darbība
[Eksperimenta pievienošana un rediģēšana](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
