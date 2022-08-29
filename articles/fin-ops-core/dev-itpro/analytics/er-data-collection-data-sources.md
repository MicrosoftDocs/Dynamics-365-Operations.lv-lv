---
title: DATU APKOPOŠANAS datu avotu izmantošana Elektronisko pārskatu formātos
description: Šajā rakstā skaidrots, kā izmantot DATU APKOPOŠANAS datu avotus Elektronisko pārskatu (ER) formātos.
author: kfend
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.custom: 58771
ms.assetid: ''
ms.search.form: EROperationDesigner
ms.openlocfilehash: 221cefc1880cdd88a952140424daf24975a575aa
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286185"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>DATU APKOPOŠANAS datu avotu izmantošana Elektronisko pārskatu formātos

[!include [banner](../includes/banner.md)]

Elektronisko pārskatu ([ER)](general-electronic-reporting.md) struktūras operāciju veidotāju varat izmantot, lai konfigurētu ER risinājuma formāta komponentu, kas tiek izmantots izejošo dokumentu ģenerēšanai dažādos formātos. Konfigurētā formāta komponenta hierarhisko struktūru veido dažādu tipu formātu elementi. Šos formāta elementus izmanto, lai izpildlaikā aizpildītu izveidotos dokumentus ar nepieciešamo informāciju. Pēc noklusējuma, palaižot ER formātu, formāta elementi tiek palaisti tādā pašā secībā, kādā tie atrodas formāta hierarhijā: pa vienam, no augšas uz leju.

Ja ER izpilda formāta elementu, kas ietver saistījumu, šī saistīšanas formula tiek izpildīta un formāta elements pievieno vērtību ģenerētam dokumentam. Piemēram, saistīšana var nodot datu modeļa lauka vērtību formāta elementam. DATU APKOPOŠANAS datu avotu var konfigurēt, lai apkopotu datu modeļa lauku vērtības izpildlaikā, veiktu vērtību summēšanu un aizpildītu ģenerēto dokumentu ar apkopotajām vērtībām. Lai izmantotu šo pieeju, mainiet sākotnējo saistīšanu tā, lai konfigurētais DATU APKOPOŠANAS datu avots tiek lietots, lai datu modeļa lauka vērtību nodotu formāta elementam. Nododot vērtības, izmantojot DATU APKOPOŠANAS datu avotu, varat apkopot nepieciešamo informāciju turpmākai lietošanai.

Konfigurējot DATU APKOPOŠANAS datu avotu, norādiet vērtības veidu, kas tiks pārvaldīts datu avotā. Pašlaik vērtību apkopošanai tiek atbalstīti tālāk norādītie [datu veidi](er-formula-supported-data-types-primitive.md).

- Būla
- Datums
- Datums un laiks
- GUID
- Int64
- Vesels skaitlis
- Reāls
- Virkne
- Laiks

Varat izmantot `Collect(Value)` DATU APKOPOŠANAS datu avota metodi, lai nodotu vērtību datu avotam apkopošanai. Šajā metodē arguments `Value` ir vai nu konstants, vai arī derīgs atbilstošā datu veida datu avota lauka ceļš.

Lai piekļūtu apkopoto vērtību sarakstam, izmantojiet DATU APKOPOŠANAS datu avota rekvizītu `Result`. Ar šo rekvizītu tiek atgriezts [ierakstu saraksts](er-formula-supported-data-types-composite.md#record-list). Ierakstu saraksta ieraksti ietver lauku `Value`, ko var izmantot, lai piekļūtu apkopotajām vērtībām.

Pēc noklusējuma DATU APKOPOŠANAS datu avots apkopo tikai unikālas vērtības.

Lai apkopotu visas vērtības, iestatiet konfigurētā DATU APKOPOŠANAS datu avota lauku **Apkopot visas vērtības** uz **Jā**. Ja lauks **Apkopot visas vērtības** ir iestatīts uz **Jā**, ir pieejams parametrizēts rekvizīts `Sum(Flag)`. Šo rekvizītu var izmantot, lai iegūtu visu pašlaik apkopoto vērtību kopsummu. Šajā rekvizītā arguments `Flag` ir [Būla](er-formula-supported-data-types-primitive.md#boolean) vērtība, kas tiek izmantota, lai norādītu, vai kopējā vērtība ir jāatiestata.

- Ja tiek norādīta vērtība **Aplams**, summēšana tiek turpināta no iepriekš apkopotās summas.
- Ja tiek norādīta vērtība **Patiess**, tiek sākta jauna summēšana.

Pašlaik summēšanai tiek atbalstīti tālāk norādītie datu veidi.

- Int64
- Vesels skaitlis
- Reāls

Lai uzzinātu vairāk par šo līdzekli, izpildiet tālāk norādīto piemēru.

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>Piemērs: ER formāta konfigurēšana, lai skaitītu un summētu, izmantojot DATU APKOPOŠANAS datu avotu

Šis piemērs parāda, kā lietotājs sistēmas administratora vai elektronisko pārskatu funkcionālā konsultanta lomā var konfigurēt ER formātu, kam ir DATU APKOPOŠANAS datu avots, kas tiek izmantots, lai aprēķinātu pašreizējās kopsummas un apkopotu summētās vērtības.

Šajā piemērā procedūras iespējams izpildīt USMF uzņēmumā Microsoft Dynamics 365 Finanses.

### <a name="upload-and-use-the-provided-er-solution"></a>Augšupielādēt un izmantot sniegto ER risinājumu

1. [Importēt ER konfigurāciju failu paraugu](er-defer-sequence-element.md#import-the-sample-er-configurations).
2. [Aktivizēt konfigurāciju nodrošinātāju](er-defer-sequence-element.md#activate-a-configurations-provider).
3. [Importētā modeļa kartējuma pārskatīšana](er-defer-sequence-element.md#review-the-imported-model-mapping).
4. [Pārskatīt importēto formātu](er-defer-sequence-element.md#review-the-imported-format).
5. [Importētā formāta palaišana](er-defer-sequence-element.md#run-the-imported-format).

### <a name="run-the-format-of-the-provided-er-solution"></a>Palaist sniegtā ER risinājuma formātu

1. Lapā **Formāta veidotājs** atlasiet **Palaist**.
2. Dialoglodziņā **Elektroniskā pārskata parametri** atlasiet **Labi**.
3. Lejupielādējiet un pārskatiet failu, ko piedāvā tīmekļa pārlūkprogramma.

    ![Lejupielādētais fails, kas satur sākotnējās formāta izpildes rezultātus](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>Modificēt ER risinājuma formātu, lai aprēķinātu pašreizējo nodokļu kopsummu

Ja transakciju apjoms ir daudz plašāks par apjomu šajā piemērā, laiks, kas nepieciešams summēšanai, var palielināties un izraisīt veiktspējas problēmas. Formāta iestatījumu maiņa var palīdzēt novērst šīs veiktspējas problēmas. Tā kā jūs piekļūstat nodokļu vērtībām, lai tās iekļautu ģenerētajā pārskatā, varat atkārtoti izmantot šo informāciju nodokļu vērtību summēšanai.

1. Lapā **Formāta veidotājs** cilnē **Kartēšana** atlasiet **Pievienot sakni**.
2. Dialoglodziņā **Pievienot datu avotu** atlasiet **Funkcijas** \> **Datu apkopošana**.
3. Dialoglodziņā **Datu apkopošanas datu avota rekvizīti** veiciet tālāk norādītās darbības.

    1. Laukā **Nosaukums** ievadiet **CollectedTaxValues**.
    2. Laukā **Vienuma veids** atlasiet **Reāls**.
    3. Laukā **Apkopot visas vērtības** atlasiet **Jā**.
    4. Atlasiet **Labi**.

4. Atlasiet skaitliskā formāta elementu **Pārskats\\Rindas\\Ieraksts\\TaxAmount**.

    > [!NOTE]
    > Pašlaik šim elementam ir konfigurēta saistīšana `@.Value`. Tādēļ ģenerētais dokuments tiek aizpildīts ar lauka `model.Data.List.Value` nodokļu vērtībām.

5. Atlasiet **Rediģēt formulu**.
6. Lapā **Formulas noformētājs** izpildiet tālāk norādītās darbības.

    1. Laukā **Formula** aizstājiet `@.Value` ar `CollectedTaxValues.Collect(@.Value)`.
    2. Saglabājiet izmaiņas un aizveriet lapu.

    > [!NOTE]
    > Jaunā saistīšana nodos tās pašas nodokļu vērtības ģenerētajam dokumentam. Tomēr šīs vērtības arī tiks apkopotas datu avotā **CollectedTaxValues**.

7. Atlasiet skaitliskā formāta elementu **Pārskats\\Rindas\\Ieraksts\\RunningTotal**.
8. Atlasiet **Rediģēt formulu**.
9. Lapā **Formulas noformētājs** izpildiet tālāk norādītās darbības.

    1. Laukā **Fomula** ievadiet `CollectedTaxValues.Sum(false)`.
    2. Saglabājiet izmaiņas un aizveriet lapu.

    > [!NOTE]
    > Jaunā saistīšana nodos ģenerētajam dokumentam jau ievadīto nodokļu vērtību kopējo summu.

    ![Skaitliskie elementi, kas ir atjauninājuši saistījumus formāta noformētāja lapā](./media/er-data-collection-data-sources-02.png)

10. Atlasiet **Saglabāt** un pēc tam atlasiet **Palaist**.
11. Dialoglodziņā **Elektroniskā pārskata parametri** atlasiet **Labi**.
12. Lejupielādējiet un pārskatiet failu, ko piedāvā tīmekļa pārlūkprogramma.

    ![Lejupielādētais fails, kas satur modificētās formāta izpildes rezultātus](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>Formāta modificēšana, lai novērtētu apkopoto nodokļu vērtību sarakstu

1. Lapā **Formāta noformētājs** cilnē **Formāts** atlasiet skaitliskā formāta elementu **Pārskats\\Rindas\\Ieraksts\\RunningTotal** un pēc tam veiciet tālāk norādītās darbības.

    1. Laukā **Skaitliskais tips** mainiet vērtību no **Reāls skaitlis** uz **Vesels skaitlis**.
    2. Laukā **Skaitliskais formāts** mainiet vērtību no **F2** uz **F0**.

3. Cilnē **Kartēšana** atlasiet **Rediģēt formulu**.
4. Lapā **Formulas noformētājs** izpildiet tālāk norādītās darbības.

    1. Laukā **Fomula** ievadiet `COUNT(CollectedTaxValues.Result)`.
    2. Saglabājiet izmaiņas un aizveriet lapu.

    > [!NOTE]
    > Jaunā saistīšana ģenerētajam dokumentam nodots ierakstu skaitu sarakstā, kurā tiek apkopotas nodokļu vērtības.

5. Atlasiet **Saglabāt** un pēc tam atlasiet **Palaist**.
6. Dialoglodziņā **Elektroniskā pārskata parametri** atlasiet **Labi**.
7. Lejupielādējiet un pārskatiet failu, ko piedāvā tīmekļa pārlūkprogramma.

    ![Lejupielādētais fails, kas satur citas modificētās formāta izpildes rezultātus](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>Ja jāaprēķina pašreizējās kopsummas un jāapkopo dati, kāda ir atšķirība starp DATU APKOPOŠANAS datu avota izmantošanu un iebūvēto DATU APKOPOŠANAS funkciju izmantošanu?

Gan DATU APKOPOŠANAS datu avotu, gan iebūvētās funkcijas [DATU APKOPOŠANA](er-functions-category-data-collection.md) var izmantot datu apkopošanai, summēšanai un uzskaitei, balstoties uz informāciju, kas tiek nodota ģenerētam izejošajam dokumentam. Tomēr, mēģinot izdarīt izvēli par tehnikas izmantošanu, ir jāņem vērā tālāk norādītie aspekti.

| Datu avots | Iebūvētās funkcijas |
|-------------| ------------------ |
| Tiek apkopotas tikai vērtības. | <p>Tiek apkopotas nosauktās vērtības. Tāpēc kopsummas var aprēķināt atsevišķām vērtību grupām.</p><p>Turklāt grupas var izvilkt kā sarakstu.</p><p>Var apkopot arī teksta vērtības.</p> |
| Unikālas vērtības tiek apkopotas automātiski. | Lai no apkopotajām vērtībām izgūtu unikālu vērtību sarakstu, ir nepieciešami papildu iestatījumi. |
| Veiktspēja ir atkarīga no apkopoto vērtību apjoma. | Praksē veiktspēja nav atkarīga no apkopoto vērtību apjoma. |
| Šī tehnika ir piemērota visu veidu izejošajiem dokumentiem. | Šī tehnika ir piemērota tikai teksta un XML dokumentiem. |

## <a name="additional-resources"></a>Papildu resursi

- [Konfigurēt formātu, lai veiktu uzskaiti un summēšanu](./tasks/er-format-counting-summing-1.md)
- [Secības elementu izpildes atlikšana elektronisko pārskatu formātos](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
