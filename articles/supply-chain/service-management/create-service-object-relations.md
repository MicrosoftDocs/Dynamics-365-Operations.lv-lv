---
title: Pakalpojumu objekta attiecību veidošana
description: Šajā rakstā ir aprakstīts, kā izveidot pakalpojumu objektu relācijas pakalpojumu līgumam un pakalpojuma pasūtījumam.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4d9424b5678a6f37d46203e5d4e359b020fda7a
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016975"
---
# <a name="create-service-object-relations"></a>Pakalpojumu objekta attiecību veidošana 

[!include [banner](../includes/banner.md)]


Šajā rakstā ir aprakstīts, kā izveidot pakalpojumu objektu relācijas pakalpojumu līgumam un pakalpojuma pasūtījumam. Kad tiek izveidotas pakalpojumu objektu relācijas, pakalpojuma līgumam vai pakalpojuma pasūtījumam ir jāpiesaista pakalpojuma objekts. Kad debitors pieprasa pakalpojumu krājumam, kas ir pakalpojuma objekts, varat atlasīt pakalpojuma objektu pakalpojumu objektu attiecību sarakstā.

## <a name="create-a-service-object-relation-for-a-service-agreement"></a>Pakalpojumu objektu attiecību izveide pakalpojumu līgumam

Lai izveidotu pakalpojumu objektu attiecības pakalpojumu līgumam, veiciet tālāk norādītās darbības:

1.  Noklikšķiniet **uz Pakalpojumu pārvaldības** \> **pakalpojumu līgumi** \> **Pakalpojumu līgumi**.

2.  Sarakstā **Pakalpojumu līgumi** atlasiet esošu pakalpojumu līgumu vai noklikšķiniet uz **Jauns**, lai izveidotu jaunu pakalpojumu līgumu.

3.  Veidlapas **Pakalpojumu līgumi** **Darbību rūts** cilnē **Pakalpojumu līgums** grupā **Relācijas** noklikšķiniet uz **Pakalpojumu objekti**.

4.  Veidlapā **Pakalpojumu objekti** noklikšķiniet uz **Jauns** un pēc tam atlasiet pakalpojuma objektu šim pakalpojumu līgumam.

5.  Lai pakalpojumu līgumam piešķirtu veidnes materiālu komplektu (MK), noklikšķiniet uz **Funkcijas** un pēc tam atlasiet **Pievienot veidnes MK**. Veidlapas **Veidnes MK atlasīšana** laukā **Veidnes MK** atlasiet veidni. 

## <a name="create-a-service-object-relation-for-a-service-order"></a>Pakalpojumu objektu attiecību izveide pakalpojuma pasūtījumam

Lai izveidotu pakalpojumu objektu attiecības pakalpojuma pasūtījumam, veiciet tālāk norādītās darbības:

1.  **Klikšķiniet Pakalpojumu pārvaldības** \> **Pakalpojumu pasūtījumi** \> **Pakalpojumu pasūtījumi**.

2.  Sarakstā **Pakalpojumu pasūtījumi** atlasiet esošu pakalpojuma pasūtījumu vai izveidojiet jaunu pakalpojuma pasūtījumu.

3.  Veidlapas **Pakalpojumu pasūtījumi** **Darbību rūts** cilnē **Pakalpojuma pasūtījums** grupā **Relācijas** noklikšķiniet uz **Pakalpojumu objekti**.

4.  Veidlapā **Pakalpojumu objekti** noklikšķiniet uz **Jauns** un pēc tam atlasiet pakalpojuma objektu šim pakalpojuma pasūtījumam.

5.  Lai pakalpojumu līgumam piešķirtu veidnes MK, noklikšķiniet uz **Funkcijas** un pēc tam atlasiet **Pievienot veidnes MK**. Veidlapas **Veidnes MK atlasīšana** laukā **Veidnes MK** atlasiet veidni. 


## <a name="see-also"></a>Skatiet arī

[Pakalpojumu objektu pārskats](service-objects.md)

[Pakalpojumu objektu relācijas](service-object-relations.md)

[Veidnes MK](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]