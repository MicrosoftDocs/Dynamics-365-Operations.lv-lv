---
title: Bīstamo materiālu pieprasījumi un pārskati
description: Šajā tēmā skaidrots, kā strādāt ar dažādiem pārskatiem, kas saistīti ar bīstamiem materiāliem. Daudzi no šiem pārskatiem ir nepieciešami, lai nosūtīšanai un uzglabāšanai tiktu ievēroti dažādi bīstamo materiālu noteikumi.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 14de281927fa3e6410627839005c6b81a93d89bc
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347024"
---
# <a name="hazardous-materials-inquiries-and-reports"></a>Bīstamo materiālu pieprasījumi un pārskati

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management sniedz dažādus pārskatus, kas saistīti ar bīstamiem materiāliem. Daudzi no šiem pārskatiem ir nepieciešami, lai nosūtīšanai un uzglabāšanai tiktu ievēroti dažādi bīstamo materiālu noteikumi.

Visi šie pārskati, izņemot **Vairākveidu bīstamu preču** pārskatu, izmanto piegādes veidu, kas definēts sūtījumam, lai atrastu regulu, kas jāizmanto, lai izdrukātu krājumu nosūtīšanas tekstu. Piegādes veids ir saistīts arī ar nosūtīšanas pārvadātāju un pārvadātāja servisu. Tāpēc ir jāiestata nosūtīšanas pārvadātāja un pārvadātāja pakalpojums, un tie jāpiesaista piegādes režīmam. Piegādes veids ir saistīts ar bīstamo materiālu regulu.

Sekojošajā attēlā parādīta aktivitāšu secība, kas notiek, kad sistēma izveido bīstamu materiālu pārskatus.

![Darbību secība bīstamo materiālu pārskatiem.](media/hazmat-report-sequence.png "Darbību secība bīstamo materiālu pārskatiem")

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a>Bīstamo materiālu ziņojumu iestatīšana

Parasti, ja tiek nosūtītas preces, kas satur bīstamus materiālus, jums ir jāģenerē īpaši pārskati, lai palīdzētu uzturēt drošību un atbilstu bīstamo materiālu prasībām. Lai iestatītu jūsu ziņojumus, rīkojieties šādi.

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**.
2. Atveriet cilni **Pārskati**. **Bīstamo materiālu pārskata parametru** kopsavilkuma cilnē iestatiet šādus laukus.

    | Sadaļa | Lauks | Apraksts |
    |---|---|---|
    | Multimodālas bīstamās preces | Noteikumu kods | Atlasiet regulu, kas jāizmanto, kad tiek ģenerēts **Vairākveidu bīstamo preču** pārskats. |
    | Bīstamo materiālu krājumu ierobežojumi | Noteikumu kods | Atlasiet regulu, kas jāizmanto, novērtējot krājumu ierobežojumus. |
    | Preču pārvadājumi pa autoceļiem | CMR grupas prece | CMR nozīmē "kancerogēnas, mutagēnas un reprotoksiskās vielas". Iestatiet šo opciju uz **Jā**, lai konfigurētu sistēmu, lai izdrukātu noteiktus brīdinājumus un ziņojumus, kas ir saistīti ar šo vielu apstrādi. |
    | Preču pārvadājumi pa autoceļiem | Bīstamo materiālu grupas apraksts | Ievadiet specifisku brīdinājumu tekstu, kas ir saistīti ar CMR un preču pārvadāšanu pa autoceļiem. Šis teksts būs ietverts šajā atskaitē. |
    | Nosūtītāja deklarācija | Brīdinājums | Ievadiet brīdinājuma ziņojuma tekstu, kas jādrukā nosūtītāja deklarācijas formā (piemēram, "Brīdinājums: bīstamas preces, viegli uzliesmojošs"). |
    | Nosūtītāja deklarācija | Kājenes uzskaite | Ievadiet ziņojuma tekstu, kas jādrukā kravas deklarācijas dokumenta apakšpusē. |
    | Bīstamo preču pārskata valoda | Bīstamo preču vietējā tirgus pārskata valoda | Atlasiet noklusējuma valodu bīstamo materiālu ziņojumiem, kas ir saistīti ar iekšzemes sūtījumiem. |
    | Bīstamo preču pārskata valoda | Bīstamo preču eksporta pārskata valoda | Atlasiet noklusējuma valodu bīstamo materiālu ziņojumiem, kas ir saistīti ar starptautiskajiem sūtījumiem. |

## <a name="hazardous-materials-report"></a>Bīstamo materiālu pārskats

**Bīstamo materiālu** pārskatā ir parādīts visu to preču saraksts, kas ir iestatīts un definēts tā, ka tam ir informācija par bīstamām precēm. Šo pārskatu var izmantot, lai pārraudzītu un pārskatītu informāciju, kas jāsaglabā. Pārskata lappuse rāda ierobežotu lauku atlasi no bīstamo materiālu iestatījumiem. Tomēr varat to personalizēt, lai pievienotu papildu laukus, cik nepieciešams.

Lai skatītu šo pārskatu, dodieties uz **Preces informācijas pārvaldība \> Vaicājumi un pārskati \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamie materiāli**.

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a>Bīstamo materiālu krājumu ierobežojumi

**Bīstamo materiālu krājumu ierobežojumu** pārskats ļauj pārraudzīt bīstamo materiālu krājumu ierobežojumus jūsu noliktavas atrašanās vietās, lai pārliecinātos, ka tie paliek šeit noteiktajos drošos ierobežojumos. Šie ierobežojumi ir no ierobežojumiem, kas definēti katrai izlaistajai precei.

Lai skatītu šo pārskatu, dodieties uz **Preces informācijas pārvaldība \> Vaicājumi un pārskati \> Bīstamo materiālu nosūtīšanas dokumentācija \> Bīstamo materiālu krājumu ierobežojumi**.

Lai iegūtu vairāk informācijas par to, kā iestatīt krājumu ierobežojumus izlaistai precei, skatiet sadaļu [Bīstamu preču krājumu ierobežojumu iestatīšana](hazmat-items.md#stock-limits).

Regula, kas tiek izmantota krājumu ierobežojumiem, ir noteikta lapā **Noliktavas pārvaldības parametri**. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**, pēc tam cilnē **Pārskati**, kas atrodas sadaļā **Bīstamo materiālu krājumu ierobežojumi**, norādiet regulas kodu. Papildinformāciju skatiet šīs tēmas iepriekšējā sadaļā [Bīstamo materiālu ziņojuma iestatīšana](#set-up).

## <a name="verified-gross-mass-report"></a>Verificētas bruto masas pārskats

**Pārbaudītais bruto masas** pārskats ļauj drukāt informāciju par kravas svaru.

Lai izveidotu un izdrukātu šo pārskatu, dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi** un atveriet atbilstošo sūtījumu. Pēc tam darbības rūtī cilnē **Sūtījumi** grupā **Bīstamo materiālu dokuments** atlasiet **Pārbaudītais bruto svars**.

## <a name="multimodal-dangerous-goods-report"></a>Multimodālo bīstamo preču pārskats

**Vairākveidu bīstamās kravas** pārskats ir paredzēts sūtījumiem, kas ir jāpārvieto, izmantojot transportēšanas metožu kombināciju. Parasti tas tiek izmantots, kad kravu vispirms pārvieto pa autoceļu un vēlāk pa jūru.

Lai izveidotu un izdrukātu šo pārskatu, dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi** un atveriet atbilstošo sūtījumu. Pēc tam darbības rūtī cilnē **Sūtījumi** grupā **Bīstamo materiālu dokuments** atlasiet **Vairākveidu bīstamās kravas**.

Ģenerējot šo pārskatu, informācija tiek saglabāta, lai varētu rediģēt un/vai atkārtoti drukāt pārskatu, ja tas nepieciešams. Lai rediģētu ģenerēto pārskatu, dodieties uz **Noliktavas pārvaldība \> Vaicājumi un pārskati \> Bīstamo materiālu piegādes dokumentācija \> Vairākveidu bīstamās kravas** un atrast atbilstošo pārskatu sarakstā. Pēc tam, kad esat pabeidzis satura rediģēšanu, atlasiet **Drukāt** Darbību rūtī, lai drukātu pārskatu.

## <a name="shippers-declaration-report"></a>Nosūtītāja deklarācijas pārskats

**Nosūtītāju deklarācijas** pārskats ļauj drukāt informāciju, kas attiecas uz kravā iekļauto materiālu deklarāciju.

Lai izveidotu un izdrukātu šo pārskatu, dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi** un atveriet atbilstošo sūtījumu. Pēc tam darbības rūtī cilnē **Sūtījumi** grupā **Bīstamo materiālu dokuments** atlasiet **Nosūtītāju deklarācija**.

## <a name="carriage-of-merchandise-by-road-report"></a>Preču pārvadājumi pa autoceļiem pārskats

**Preču pārvadājumi pa autoceļiem** pārskats ir līdzīgs preču transporta pavadzīmei, bet parasti tā tiek izmantota ceļu transportēšanai Eiropā saskaņā ar Vienošanos par starptautiskiem bīstamo kravu autopārvadājumiem (ADR) regulām. Šis pārskats lieto krājuma piegādes izdrukas tekstu, ja vien nav iestatīts lauks **Bīstamo materiālu grupa apraksts** lapā **Noliktavas pārvaldības parametri**.

Lai izveidotu un izdrukātu šo pārskatu, dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi** un atveriet atbilstošo sūtījumu. Pēc tam darbības rūtī cilnē **Sūtījumi** grupā **Bīstamo materiālu dokuments** atlasiet **Preču pārvadājumi pa autoceļiem**.

Ģenerējot šo pārskatu, informācija tiek saglabāta, lai varētu rediģēt un/vai atkārtoti drukāt pārskatu, ja tas nepieciešams. Lai rediģētu ģenerēto pārskatu, dodieties uz **Noliktavas pārvaldība \> Vaicājumi un pārskati \> Bīstamo materiālu piegādes dokumentācija \> Preču pārvadājumi pa autoceļiem** un atrast atbilstošo pārskatu sarakstā. Pēc tam, kad esat pabeidzis satura rediģēšanu, atlasiet **Drukāt** Darbību rūtī, lai drukātu pārskatu.

## <a name="shipment-summary-report"></a>Sūtījuma kopsavilkuma pārskats

**Kravas kopsavilkuma** pārskats sniedz informāciju, kas tiek apkopota pēc transportēšanas kategorijas, kas saistīta ar izlaistajiem krājumiem.

Lai izveidotu un izdrukātu šo pārskatu, dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi** un atveriet atbilstošo sūtījumu. Pēc tam darbības rūtī cilnē **Sūtījumi** grupā **Bīstamo materiālu dokuments** atlasiet **Kravas kopsavilkumu**.

## <a name="bill-of-lading-report"></a>preču transporta pavadzīmju pārskats

Kad jūsu sistēmā ir ieslēgta bīstamo materiālu funkcija, **preču transporta pavadzīmju** pārskats ietver **Bīstamo materiālu** kolonnu, kas norāda, vai krava ietver bīstamos materiālus. Šis pārskats ir pieejams lapā **Visas kravas**, kā parasti.

## <a name="packing-list-report"></a>Iepakojuma saraksta pārskats

Kad sistēmā ir ieslēgta bīstamo materiālu funkcija, iepakošanas sarakstos ir ietverta papildu informācija, kas saistīta ar preču nosūtīšanas tekstu. Šis pārskats ir pieejams lapā **Visas kravas**, kā parasti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]