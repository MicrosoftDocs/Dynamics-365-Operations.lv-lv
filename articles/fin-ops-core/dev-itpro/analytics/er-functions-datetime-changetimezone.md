---
title: CHANGETIMEZONE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota FUNKCIJA CHANGETIMEZONE Electronic reporting (ER).
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: d732fd8bd44c4c131f376919b2546a7ecf668495
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286125"
---
# <a name="changetimezone-er-function"></a>CHANGETIMEZONE ER funkcija

[!include [banner](../includes/banner.md)]

`CHANGETIMEZONE` funkcija atgriež *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* vērtību, kas tiek konvertēta no konkrētā datuma vērtības uz datuma/laika vērtību pēc universālā koordinētā laika (Griničas laika \[GMT\]).

## <a name="syntax"></a>Sintakse

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Argumenti

`datetime`: *DateTime*

Datuma/laika vērtība universālajā koordinētajā laika zonā, kas attēlo konvertējamā datuma/laika vērtību.

`base time zone`: *[Virkne](er-formula-supported-data-types-primitive.md#string)*

Tās laika joslas nosaukums, uz kuru pirms pārvēršanas tiek mainīta dotā datuma/laika vērtība.

`target time zone`: *Virkne*

Tās laika joslas nosaukums, uz kuru pārvēršanas laikā tiek mainīta pārvērstā datuma/laika vērtība.

## <a name="return-values"></a>Atgrieztās vērtības

*Datums un laiks*

Iegūtā datuma/laika vērtība universālajā koordinētajā laika zonā.

## <a name="usage-notes"></a>Lietošanas piezīmes

Lai norādītu avota un mērķa laika joslas, varat lietot laika joslu nosaukumus, ko [nodrošina](https://data.iana.org/time-zones/releases/) [Interneta piešķirto numuru iestāde (IANA)](https://www.iana.org/) vai ko [atbalsta](/windows-hardware/manufacture/desktop/default-time-zones) Microsoft Windows.

Izpildlaikā izņēmums "Laika josla '\<time zone name\>' neeksistē" nepastāv" nenotiek, ja tas nav atrasts IANA vai Windows reģistrā.

Laika zonām, kurās ir ievērots ziemas/vasaras laiks, pārvēršana apsver universālajā koordinētajā ziemas/vasaras laika korespondējošo kontu. Konvertēšanas laikā tiek izmantota jaunākā pieejamā informācija par šo korespondējošo kontu.

## <a name="example-1"></a>1. piemērs

Šajā piemērā tiek izmantoti Windows laika joslu nosaukumi.

Jūs konfigurējat **Aprēķinātā lauka** tipa **DSX** datu avotu. Tā ietver šādu izteiksmi.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

Ja konfigurējat **Aprēķinātā lauka** tipa **DSY** datu avota izteiksmi kā `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX** datu avots atgriež tekstu **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Šis teksts parāda, ka laika atšķirība starp divām nodrošinātajām laika joslām 1. jūnijā ir vairāk nekā 24 stundas. Tādējādi konvertētā datuma/laika vērtība ir vienu dienu pirms dotās datuma/laika vērtības, jo bāzes laika josla apsteidz mērķa laika zonu.

Ja konfigurējat **Aprēķinātā lauka** tipa **DSY** datu avota izteiksmi kā `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX** datu avots atgriež tekstu **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Šis teksts parāda, ka laika atšķirība starp divām nodrošinātajām laika joslām 1. decembrī ir mazāk nekā 24 stundas. Tādējādi konvertētā datuma/laika vērtība ir vienāda ar doto datuma/laika vērtību.

> [!NOTE]
> Tā pati izteiksme atgriež atšķirīgu novirenci starp nodrošinātajām un pārveidotajām datuma/laika vērtībām tam pašam laika joslu pārim, jo attiecīgajā datumā/laikā nodrošinātajām laika zonām ir ievērots cits universālais koordinētā laika vasaras laika nobīde.

## <a name="example-2"></a>2. piemērs

Šajā piemērā tiek izmantoti IANA laika joslu nosaukumi.

Jūs konfigurējat **Aprēķinātā lauka** tipa **DSX** datu avotu. Tā ietver šādu izteiksmi.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

Ja konfigurējat **Aprēķinātā lauka** tipa **DSY** datu avota izteiksmi kā `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX** datu avots atgriež tekstu **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Šis teksts parāda, ka laika atšķirība starp divām nodrošinātajām laika joslām 1. jūnijā ir vairāk nekā 24 stundas. Tādējādi konvertētā datuma/laika vērtība ir vienu dienu pirms dotās datuma/laika vērtības, jo bāzes laika josla apsteidz mērķa laika zonu.

Ja konfigurējat **Aprēķinātā lauka** tipa **DSY** datu avota izteiksmi kā `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX** datu avots atgriež tekstu **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Šis teksts parāda, ka laika atšķirība starp divām nodrošinātajām laika joslām 1. decembrī ir mazāk nekā 24 stundas. Tādējādi konvertētā datuma/laika vērtība ir vienāda ar doto datuma/laika vērtību.

## <a name="example-3"></a>3. piemērs

Jūs konfigurējat **Aprēķinātā lauka** tipa **DSX** datu avotu. Tā ietver šādu izteiksmi.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

Ja konfigurējat **Aprēķinātā lauka** tipa **DSY** datu avota izteiksmi kā `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX** datu avots atgriež tekstu **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00'**. Šis teksts parāda, ka laika atšķirība starp divām nodrošinātajām laika joslām 1. jūnijā ir vairāk nekā 24 stundas. Tādējādi konvertētā datuma/laika vērtība ir vienu dienu pēc dotās datuma/laika vērtības, jo mērķa laika josla apsteidz pamata laika zonu.

## <a name="example-4"></a>4. piemērs

Jūs variet saņemt datuma/laika zīmogu no ārēja avota, kā tekstu, kas nesatur laika joslas informāciju. Tomēr, iespējams, zināt laika joslu, kurā avots tiek darbināts. Piemēram, jūs saņemat datuma/laika zīmogu **01/12/2021 12:55:00** no pakalpojuma, kas tiek sniegts Spānijā. Lai pareizi saglabātu šo datuma/laika vērtību datu bāzē, veiciet sekojošo pārveidošanu:

- Konfigurējiet **Aprēķinātā lauka** tipa **DSY** datu avotu, lai datuma/laika zīmogu pārvērstu no teksta uz universālajā koordinētā laika/laika vērtību.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- Konfigurējiet **Aprēķinātā lauka** tipa **DSX** datu avotu, lai pārvērsto datuma/laika vērtību pārveidotu uz universālais koordinētais laiks kā ārējā avota laika joslas datuma/laika vērtību.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> Kad izmantojat `CHANGETIMEZONE` datuma/laika pārvēršanas funkciju, ņemiet vērā, ka jebkura datuma/laika vērtība tiek saglabāta datu bāzē kā vērtība universālajā koordinētajā laika zonā. Pirms šīs vērtības iesniegšanas programmas lapās tā ir pārvērsta. Pārvēršana apsver laika joslu, kas ir [iestatīta](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) kā pašreiz parakstītā programmas lietotāja vēlamā zona.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
