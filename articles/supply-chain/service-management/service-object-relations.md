---
title: Pakalpojumu objektu saistības
description: Ir iespējams izveidot pakalpojuma objekta relāciju starp pakalpojuma objektu un pakalpojumu līgumu vai pakalpojuma pasūtījumu.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 913b3c30bf972de7cc3dde73280e4f2f2be38507
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974339"
---
# <a name="service-object-relations"></a>Pakalpojumu objektu saistības 

[!include [banner](../includes/banner.md)]

Ir iespējams izveidot pakalpojuma objekta relāciju starp pakalpojuma objektu un pakalpojumu līgumu vai pakalpojuma pasūtījumu. Kad tiek izveidota relācija, pakalpojumu līgumam vai pakalpojuma pasūtījumam ir jāpievieno pakalpojuma objekts.

Pēc relācijas izveidošanas jebkurai pakalpojumu līguma vai pakalpojuma pasūtījuma rindai var pievienot pakalpojuma objektu.

## <a name="template-boms"></a>Veidnes MK

Objektu relācijai ir arī iespējams noteikt veidnes MK. Veidnes MK ir materiālu komplekts objektam, kuram tiem veikts pakalpojums. Ja apkopes laikā tiek nomainīta kāda pakalpojumu objekta sastāvdaļa, šo nomaiņu iespējams reģistrēt pakalpojuma MK, izmantojot veidlapu Pakalpojumu objekti.

## <a name="example"></a>Paraugs

Tiek izveidots pakalpojumu līgums divu celtņu apkalpošanai klienta būvlaukumā.
Pakalpojumu līguma identifikators ir ID SAL-001.

Veidlapā Pakalpojumu objekti celtņi tikuši uzstādīti kā objekti EL-S/1000 un EL-L/1000.

Pakalpojuma objekti (EL-S/1000 un EL-L/1000) tiek pievienoti pakalpojumu līgumam.

Lietotājs vēlas reģistrēt pakalpojuma objekta izmaiņas MK, jo tikusi nomainīta kāda objekta sastāvdaļa, tad pakalpojuma objekta relācijai tiek pievienots pakalpojuma MK kā aprakstīts sekojošajā tabulā.

| Pakalpojumu objekts | Relācija – Pakalpojumu līgums | Pakalpojumu MK   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | BOM-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | BOM-EL-L/1000 |

Pateicoties tam, ka līgumam ir pakalpojumu objekts, tagad var izveidot pakalpojumu līguma rindas ar šiem objektiem kā parādīts tālāk esošajā tabulā.

| Darbības veids | Kategorija           | Pakalpojumu objekts |
|------------------|--------------------|----------------|
| Stunda             | Pārbaude         | EL-S/1000      |
| Stunda             | Ātrumkārbas tīrīšana  | EL-S/1000      |
| Krājums             | Tīrīšanas materiāli | EL-S/1000      |
| Stunda             | Pārbaude         | EL-L/1000      |
| Stunda             | Ātrumkārbas tīrīšana   | EL-L/1000      |
| Krājums             | Tīrīšanas materiāli | EL-L/1000      |

Apkopes veikšanas laikā tikusi nomainīta celtņa EL-S/1000 ātrumkārba. Lai nomainītu objekta sastāvdaļu, ir iespējams piekļūt BOM Designer izmantojot pakalpojumu objekta relāciju, kura tika iestatīta pašreizējam pakalpojumu līgumam.

Piekļūstiet BOM Designer ar pakalpojumu objektu relācijas palīdzību.

1. Pakalpojumu līgumi
2. Veiciet dubultklikšķi uz pakalpojumu līguma, vai noklikšķiniet uz Pakalpojumu līgums, lai izveidotu pakalpojumu līgumu.
3. Noklikšķiniet uz cilnes Iestatījumi.
4. Lai pakalpojumu līgumam pievienotu veidnes MK, nokliksķiniet uz Pakalpojumu objekti.
5. Veidlapā Pakalpojumu objekti noklikšķiniet uz Noformētājs, lai atvērtu veidotāja veidlapu un modificētu veidnes MK.

## <a name="automatically-created-service-orders"></a>Automātiski izveidoti pakalpojumu pasūtījumi

Ja pakalpojumu līgumam tiek automātiski izveidoti pakalpojuma pasūtījumi, tad pakalpojumu objektu relācijas līgumā tiek izveidotas arī pakalpojumu pasūtījumos.

