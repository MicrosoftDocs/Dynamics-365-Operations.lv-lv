---
title: Saskaņošanas datuma scenāriji
description: Šajā rakstā sniegti piemēri, kas parāda, kā līdzinājuma datumi darbojas abonementa rēķinos.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 102e3a104be5be287f914172160e95aff65d0b18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872620"
---
# <a name="alignment-date-scenarios"></a>Saskaņošanas datuma scenāriji

Šajā rakstā sniegti piemēri, kas parāda, kā līdzinājuma datumi darbojas abonementa rēķinos.

Šiem piemēriem norēķinu grafika norēķinu detalizētai informācijai ir 2019. gada 31. oktobris. Pirmā norēķinu informācija rindai beidzas 2019. gada 31. oktobris un tiek atbilstīgi ģenerēta. Rinda tiek automātiski atjaunota, izmantojot atjaunošanas sākuma datumu 11. novembrī.

> [!NOTE]
> Gads ir būtisks, jo tas var izraisīt līdzinājuma datumu, kas ir lielāks vai mazāks par gadu. Šajos piemēros parametrs lapā Periodiskie līguma norēķinu parametri **tiek** **iestatīts uz Mēnesis**. Ja iestatījums ir Ikdienas **, dažas** daļējas summas atšķiras.

## <a name="scenario-1-no-alignment"></a>1. scenārijs: bez līdzinājuma

Norēķinu grafikam ir iestatīti šādi dati:

- **Sākuma datums:** 2019. gada 1. maijs
- **Beigu datums:** 2024. gada 31. decembris
- **Summa:** $1,000

| Norēķinu sākuma datums | Norēķinu beigu datums | Iepriekšējais rādījums | Pašreizējais rādījums | Ievadītais daudzums | Brīvais daudzums | Apmaksājamais daudzums | Vienības cena |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 30.04.2020. | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2020 | 4/30/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2021 | 4/30/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2022 | 4/30/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2023 | 4/30/2024 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>2. scenārijs: saīsināts līdzinājums

Norēķinu grafikam ir iestatīti šādi dati:

- **Sākuma datums:** 2019. gada 1. maijs
- **Beigu datums:** 2024. gada 31. decembris
- **Summa:** $1,000
- **Līdzināšanas datums:** 2019. gada 31. decembris

Pirmā atjaunošanas summa ir mazāka par vienu gadu.

| Norēķinu sākuma datums | Norēķinu beigu datums | Iepriekšējais rādījums | Pašreizējais rādījums | Ievadītais daudzums | Brīvais daudzums | Apmaksājamais daudzums | Vienības cena |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 01.01.2020. | 31.12.2020. | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2022. | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>3. scenārijs: paplašināts līdzinājums

Norēķinu grafikam ir iestatīti šādi dati:

- **Sākuma datums:** 2019. gada 1. maijs
- **Beigu datums:** 2024. gada 31. decembris
- **Summa:** $1,000
- **Līdzināšanas datums:** 2020. gada 31. decembris

Pirmā atjaunošanas summa ir vairāk nekā vienam gadam.

| Norēķinu sākuma datums | Norēķinu beigu datums | Iepriekšējais rādījums | Pašreizējais rādījums | Ievadītais daudzums | Brīvais daudzums | Apmaksājamais daudzums | Vienības cena |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 31.12.2020. | | | 1.00 | | 1.00 | 1,666.67 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2022. | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>4. scenārijs: līdzinājums ar citu beigu mēnesi

Norēķinu grafikam ir iestatīti šādi dati:

- **Sākuma datums:** 2019. gada 1. maijs
- **Beigu datums:** 2024. gada 31. oktobris
- **Summa:** $1,000
- **Līdzināšanas datums:** 2019. gada 31. decembris

> [!NOTE]
> Šis scenārijs nav izplatīts.

| Norēķinu sākuma datums | Norēķinu beigu datums | Iepriekšējais rādījums | Pašreizējais rādījums | Ievadītais daudzums | Brīvais daudzums | Apmaksājamais daudzums | Vienības cena |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 01.01.2020. | 31.12.2020. | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2022. | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>5. scenārijs: viens daļējs gads

Norēķinu grafikam ir iestatīti šādi dati:

- **Sākuma datums:** 2019. gada 1. maijs
- **Beigu datums:** 2019. gada 31. decembris
- **Summa:** $1,000
- **Līdzināšanas datums**: 2019. gada 31. decembris

Šajā scenārijā nav nepieciešams līdzināšanas datums. Šis scenārijs ir izplatīts automātiskai atjaunošanai.

| Norēķinu sākuma datums | Norēķinu beigu datums | Iepriekšējais rādījums | Pašreizējais rādījums | Ievadītais daudzums | Brīvais daudzums | Apmaksājamais daudzums | Vienības cena |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>6. scenārijs: aprēķinātie datumi

Atbalsts un atjaunošana ir iestatīta ar šādiem datiem:

- **Ignorēt sākuma datumu:** Nē
- **Atbalstīt un atjaunot sākuma datumus:** nākamā mēneša sākums
- **Rēķina grāmatošanas datums:** 2019. gada 22. jūnijs
- **Līdzināšanas datums:** 2020. gada 31. decembris

| Norēķinu sākuma datums | Norēķinu beigu datums | Iepriekšējais rādījums | Pašreizējais rādījums | Ievadītais daudzums | Brīvais daudzums | Apmaksājamais daudzums | Vienības cena |
|---|---|---|---|---|---|---|---|
| 7/1/2019 | 7/31/2019 | | | 1.00 | | 1.00 | 297.60 |
| 8/1/2019 | 31.12.2020. | | | 1.00 | | 1.00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>7. scenārijs: aprēķinātie datumi un grāmatošana nākotnē

Atbalsts un atjaunošana ir iestatīta ar šādiem datiem:

- **Ignorēt sākuma datumu:** Nē
- **Atbalstīt un atjaunot sākuma datumus:** nākamā mēneša sākums
- **Rēķina grāmatošanas datums:** 2019. gada 22. jūnijs
- **Līdzināšanas datums:** 2020. gada 31. decembris

Šajā scenārijā līdzinājuma datums tiek mainīts uz 2021. gada 31. decembri.

| Norēķinu sākuma datums | Norēķinu beigu datums | Iepriekšējais rādījums | Pašreizējais rādījums | Ievadītais daudzums | Brīvais daudzums | Apmaksājamais daudzums | Vienības cena |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 8/1/2019 | 31.12.2020. | | | 1.00 | | 1.00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>8. scenārijs: manuālie datumi un vairāki gadi

Atbalsts un atjaunošana ir iestatīta ar šādiem datiem:

- **Ignorēt sākuma datumu:** Jā
- **Atjaunošanas sākuma datums:** 2020. gada 1. jūlijs
- **Atjaunošanas beigu datums:** 2024. gada 31. decembris
- **Līdzināšanas datums:** 2021. gada 31. decembris

| Norēķinu sākuma datums | Norēķinu beigu datums | Iepriekšējais rādījums | Pašreizējais rādījums | Ievadītais daudzums | Brīvais daudzums | Apmaksājamais daudzums | Vienības cena |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 1.1.2022. | 12/31/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 250,00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>9. scenārijs: manuālie datumi, vairāki gadi un cits beigu mēnesis

Atbalsts un atjaunošana ir iestatīta ar šādiem datiem:

- **Ignorēt sākuma datumu:** Jā
- **Atjaunošanas sākuma datums:** 2020. gada 1. jūlijs
- **Atjaunošanas beigu datums:** 2024. gada 31. oktobris
- **Līdzināšanas datums:** 2021. gada 31. decembris

| Norēķinu sākuma datums | Norēķinu beigu datums | Iepriekšējais rādījums | Pašreizējais rādījums | Ievadītais daudzums | Brīvais daudzums | Apmaksājamais daudzums | Vienības cena |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 1.1.2022. | 12/31/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>10. scenārijs: līdzinājums bez prorācijas

Atbalsts un atjaunošana ir iestatīta ar šādiem datiem:

- **Ignorēt sākuma datumu:** Nē
- **Rēķina grāmatošanas datums:** 2019. gada 22. jūnijs
- **Līdzināšanas datums:** 2019. gada 31. decembris

Atjaunošanas sākuma datums un līdzinājuma datumi tiek pielāgoti, lai abi sākuma datumi būtu pēc grāmatošanas datuma.

- **Atjaunošanas sākuma datums:** 2020. gada 1. janvāris
- **Atjaunošanas beigu datums:** 2020. gada 31. decembris
