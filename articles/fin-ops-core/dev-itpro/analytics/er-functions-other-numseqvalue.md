---
title: NUMSEQVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NUMSEQVALUE elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 53040d1f4b3c8089fab264a524309df909a90ed5e617bd86658704b286fabb34
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758244"
---
# <a name="numseqvalue-er-function"></a>NUMSEQVALUE ER funkcija

[!include [banner](../includes/banner.md)]

`NUMSEQVALUE` funkcija atgriež *Virknes* vērtību, kas apzīmē jauno numuru sērijas ģenerēto vērtību, pamatojoties uz norādīto numuru sēriju, tvērumu un tvēruma ID. Tvēruma ID ir vienāds ar uzņēmuma kodu, ko nodrošina konteksts, kurā tiek palaists elektroniskā pārskata (ER) formāts.

## <a name="syntax-1"></a>Sintakse 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Sintakse 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>Argumenti

`number sequence code`: *Virkne*

Teksta vērtība, kas apzīmē kodu numuru sērijai, kurai ir nepieciešama jauna vērtība.

`number sequence record ID`: *Int64*

*Int64* vērtība, kas attēlo ieraksta ID ierakstu tabulā NumberSequenceTable, kas ietver numuru sērijas definīciju, kurai ir nepieciešama jauna vērtība.

`scope type`: *Uzskaitījuma vērtība*

Uzskaitījuma vērtība **ERExpressionNumberSequenceScopeType**, kas definē tās numuru sērijas tvērumu, kurai ir nepieciešama jauna vērtība. Pieejamie tvērumu tipi ir **Kopīgots**, **Juridiska persona** un **Uzņēmums**.

`scope ID`: *Virkne*

*Virknes* vērtība, kas identificē tvērumu, pamatojoties uz norādīto tvēruma tipu.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Tvēruma tipam **Koplietots** kā tvēruma ID ir jānorāda tukša virkne.

Tvēruma tipiem **Uzņēmums** un **Juridiskā persona** kā tvēruma ID ir jānorāda uzņēmuma kods. Ja šiem tvērumu tipiem ka tvēruma ID norādāt tukšu virkni, tiek izmantots pašreizējais uzņēmuma kods.

Lietojot 1. sintaksi, numuru sērija tiek pieprasīta **Uzņēmuma** tvēruma tipam, un uzņēmuma kodu nodrošina konteksts, kurā tiek palaists ER formāts.

## <a name="example-1"></a>1. piemērs

Savā ER formātā jūs definējat tipa *Lietotāja ievades parametrs* datu avotu **AskNumSeq**. Šis datu avots attiecas uz paplašināto datu tipu (EDT) **Apraksts**. Pēc tam definējat tipa **Aprēķinātais lauks** datu avotu *NumSeq*. Šajā datu avotā ir izteiksme `NUMSEQVALUE (AskNumSeq)`. Kad tiek izsaukts datu avots **NumSeq**, tas atgriež jaunu ģenerēto numuru sērijas vērtību, kas tika norādīta izpildlaikā, ievadot tās kodu dialoglodziņā. Numuru sērija tiek pieprasīta **Uzņēmuma** tvēruma tipam. Uzņēmuma kodu nodrošina konteksts, kurā tiek palaists ER formāts.

## <a name="example-2"></a>2. piemērs

Savā modeļa kartēšanā jūs tiek definēti šādi datu avoti:

- **Tabulas** veida datu avots *LedgerParms*. Šis datu avots attiecas uz LedgerParameters tabulu.
- **Aprēķinātā lauka** veida datu avots *NumSeq*. Šajā datu avotā ir izteiksme `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.

Kad tiek izsaukts datu avots **NumSeq**, tas atgriež jauno vērtību, kas ir ģenerēta ar numuru sēriju, kura ir konfigurēta virsgrāmatas parametros tam uzņēmumam, kas nodrošina kontekstu, kurā tiek darbināts ER formāts. Šī numuru sērija unikāli identificē žurnālus un darbojas kā partijas numurs, kas sasaista transakcijas.

## <a name="example-3"></a>3. piemērs

Savā modeļa kartēšanā jūs tiek definēti šādi datu avoti:

- **enumScope** datu avots Microsoft Dynamics 365 Finance *uzskaitījuma* tipam. Šis datu avots attiecas uz uzskaitījumu **ERExpressionNumberSequenceScopeType**.
- **Aprēķinātā lauka** veida datu avots *NumSeq*. Šajā datu avotā ir izteiksme `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.

Kad tiek izsaukts datu avots **NumSeq**, tas atgriež jauno vērtību, kas ir ģenerēta ar numuru sēriju **Gene\_1**, kura ir konfigurēta uzņēmumam, kas nodrošina kontekstu, kurā tiek darbināts ER formāts.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]