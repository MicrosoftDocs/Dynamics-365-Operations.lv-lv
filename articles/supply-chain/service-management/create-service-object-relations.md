---
title: Pakalpojumu objekta attiecību veidošana
description: Šajā tēmā aprakstīts, kā izveidot pakalpojumu objektu attiecības pakalpojumu līgumam un pakalpojuma pasūtījumam.
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
ms.openlocfilehash: 4178132b03cd146aacbcbb8bf8e1e774a161726c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677231"
---
# <a name="create-service-object-relations"></a>Pakalpojumu objekta attiecību veidošana 

[!include [banner](../includes/banner.md)]


Šajā tēmā aprakstīts, kā izveidot pakalpojumu objektu attiecības pakalpojumu līgumam un pakalpojuma pasūtījumam. Kad tiek izveidotas pakalpojumu objektu relācijas, pakalpojuma līgumam vai pakalpojuma pasūtījumam ir jāpiesaista pakalpojuma objekts. Kad debitors pieprasa pakalpojumu krājumam, kas ir pakalpojuma objekts, varat atlasīt pakalpojuma objektu pakalpojumu objektu attiecību sarakstā.

## <a name="create-a-service-object-relation-for-a-service-agreement"></a>Pakalpojumu objektu attiecību izveide pakalpojumu līgumam

Lai izveidotu pakalpojumu objektu attiecības pakalpojumu līgumam, veiciet tālāk norādītās darbības:

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.

2.  Sarakstā **Pakalpojumu līgumi** atlasiet esošu pakalpojumu līgumu vai noklikšķiniet uz **Jauns**, lai izveidotu jaunu pakalpojumu līgumu.

3.  Veidlapas **Pakalpojumu līgumi** **Darbību rūts** cilnē **Pakalpojumu līgums** grupā **Relācijas** noklikšķiniet uz **Pakalpojumu objekti**.

4.  Veidlapā **Pakalpojumu objekti** noklikšķiniet uz **Jauns** un pēc tam atlasiet pakalpojuma objektu šim pakalpojumu līgumam.

5.  Lai pakalpojumu līgumam piešķirtu veidnes materiālu komplektu (MK), noklikšķiniet uz **Funkcijas** un pēc tam atlasiet **Pievienot veidnes MK**. Veidlapas **Veidnes MK atlasīšana** laukā **Veidnes MK** atlasiet veidni. 

## <a name="create-a-service-object-relation-for-a-service-order"></a>Pakalpojumu objektu attiecību izveide pakalpojuma pasūtījumam

Lai izveidotu pakalpojumu objektu attiecības pakalpojuma pasūtījumam, veiciet tālāk norādītās darbības:

1.  Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.

2.  Sarakstā **Pakalpojumu pasūtījumi** atlasiet esošu pakalpojuma pasūtījumu vai izveidojiet jaunu pakalpojuma pasūtījumu.

3.  Veidlapas **Pakalpojumu pasūtījumi** **Darbību rūts** cilnē **Pakalpojuma pasūtījums** grupā **Relācijas** noklikšķiniet uz **Pakalpojumu objekti**.

4.  Veidlapā **Pakalpojumu objekti** noklikšķiniet uz **Jauns** un pēc tam atlasiet pakalpojuma objektu šim pakalpojuma pasūtījumam.

5.  Lai pakalpojumu līgumam piešķirtu veidnes MK, noklikšķiniet uz **Funkcijas** un pēc tam atlasiet **Pievienot veidnes MK**. Veidlapas **Veidnes MK atlasīšana** laukā **Veidnes MK** atlasiet veidni. 


## <a name="see-also"></a>Skatiet arī

[Pakalpojumu objektu pārskats](service-objects.md)

[Pakalpojumu objektu relācijas](service-object-relations.md)

[Veidnes MK](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]