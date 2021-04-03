---
title: GETENUMVALUEBYNAME ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota GETENUMVALUEBYNAME elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bfc173130a9fc57385826f77443ec28946ef68fd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570594"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME ER funkcija

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME` funkcija meklē konkrētu *Enum* vērtību norādītajā uzskaitījuma datu avotā, izmantojot uzskaitījuma nosaukumu, kas ir norādīts kā *Virknes* vērtība. Ja tiek tiek atrasta *Enum* vērtība, funkcija to atgriež. Pretējā gadījumā funkcija atgriež uzskaitījuma vērtību **null**.

## <a name="syntax"></a>Sintakse

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumenti

`enumeration data source path`: *Uzskaitījums*

Derīgs datu avota atsauces ceļš vienam no šādiem uzskaitījumu tipiem:

- Elektronisko pārskatu (ER) modeļu uzskaitījums
- ER formāta uzskaitījums
- Microsoft Dynamics 365 Finance uzskaitījums

`enumeration value text`: *Virkne*

Virknes vērtība, kas apzīmē vienas uzskaitījuma vērtības nosaukumu.

## <a name="return-values"></a>Atgrieztās vērtības

Nullējama *Enum*

Iegūtā uzskaitījuma vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Netiek rādīts izņēmums, ja *Enum* vērtība nav atrasta, izmantojot uzskaitījuma vērtības nosaukumu, kas ir norādīts kā *Virknes* vērtība.

## <a name="example-1"></a>1. piemērs

Tālāk esošajā attēlā ir parādīts datu modelī ieviests uzskaitījums **ReportDirection**. Ņemiet vērā, ka etiķetes ir definētas uzskaitījumu vērtībām.

![Pieejamās datu modeļu uzskaitījuma vērtības](./media/ER-data-model-enumeration-values.PNG)

Tālāk esošajā attēlā parādīta tālāk uzskaitītā informācija.

- **$Direction** datu avots ir konfigurēts ER pārskatā. Šis datu avots ir konfigurēts, pamatojoties uz modeļa uzskaitījumu **ReportDirection**.
- Izteiksme `$IsArrivals` ir izveidota ar mērķi lietot modeļa uzskaitījumā bāzētu datu avotu **$Direction** kā šīs funkcijas parametru.
- Šīs salīdzinājuma izteiksmes vērtība ir **TRUE**.

![Datu modeļu uzskaitījuma piemērs](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>2. piemērs

`GETENUMVALUEBYNAME` un [`LISTOFFIELDS`](er-functions-list-listoffields.md) funkcijas sniedz iespēju ienest atbalstīto uzskaitījumu vērtības un etiķetes kā teksta vērtības. (Atbalstītie uzskaitījumi ir programmu uzskaitījumi, datu modeļu uzskaitījumi un formātu uzskaitījumi.)

Tālāk esošajā attēlā ir parādīts modeļa kartējumā ieviests datu avots **TransType**. Šis datu avots attiecas uz programmu uzskaitījumu **LedgerTransType**.

![Modeļa kartējuma datu avots, kas attiecas uz programmu uzskaitījumu](./media/er-functions-text-getenumvaluebyname-example2-1.png)

Tālāk esošajā attēlā ir parādīts modeļa kartējumā konfigurēts datu avots **TransTypeList**. Šis datu avots ir konfigurēts, pamatojoties uz programmu uzskaitījumu **TransType**. Funkcija `LISTOFFIELDS` tiek izmantota, lai atgrieztu visas uzskaitījuma vērtības kā ierakstu sarakstu ar laukiem. Šādā veidā tiek atklāta informācija par katra uzskaitījuma vērtību.

> [!NOTE]
> Lauks **EnumValue** ir konfigurēts **TransTypeList** datu avotam, izmantojot `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` izteiksmi. Šis lauks atgriež uzskaitījuma vērtību katram šī saraksta ierakstam.

![Modeļa kartējuma datu avots, kas atgriež visas atlasītās uzskaitījuma vērtības kā ierakstu sarakstu](./media/er-functions-text-getenumvaluebyname-example2-2.png)

Tālāk esošajā attēlā ir parādīts modeļa kartējumā konfigurēts datu avots **VendTrans**. Šis datu avots atgriež kreditora transakciju ierakstus no **VendTrans** programmas tabulas. Katras transakcijas virsgrāmatas veids ir definēts, izmantojot lauka **TransType** vērtību.

> [!NOTE]
> Lauks **TransTypeTitle** ir konfigurēts **VendTrans** datu avotam, izmantojot `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` izteiksmi. Šis lauks atgriež pašreizējās transakcijas uzskaitījuma vērtības etiķeti kā tekstu, ja šī uzskaitījuma vērtība ir pieejama. Pretējā gadījumā šī izteiksme atgriež tukšu virknes vērtību.
>
> Lauks **TransTypeTitle** ir saistīts ar datu modeļa lauku **LedgerType**, kas iespējo šīs informācijas izmantošanu katrā elektroniskā pārskata formātā, kas izmanto datu modeli kā datu avotu.

![Modeļa kartējuma datu avots, kas atgriež kreditoru transakcijas](./media/er-functions-text-getenumvaluebyname-example2-3.png)

Tālāk esošajā attēlā ir parādīts, kā varat izmantot [datu avota atkļūdotāju](er-debug-data-sources.md), lai pārbaudītu konfigurēto modeļa kartējumu.

![Datu avota atkļūdotāja izmantošana, lai pārbaudītu konfigurēto modeļa kartējumu](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

Datu modeļa lauks **LedgerType** parāda transakciju veida etiķetes kā paredzēts.

Ja plānojat izmantot šo pieeju lielam transakciju datu apjomam, ir jāapsver izpildes veiktspēja. Papildinformāciju skatiet [Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)

[Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md)

[LISTOFFIELDS ER funkcija](er-functions-list-listoffields.md)

[FIRSTORNULL ER funkcija](er-functions-list-firstornull.md)

[WHERE ER funkcija](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]