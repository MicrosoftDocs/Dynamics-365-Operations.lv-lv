---
title: Preču iepakojumu izveide pirkšanas pasūtījumiem
description: Šajā procedūrā ir aprakstīts, ka izveidot preču pakotni un izmantot to pirkšanas pasūtījumā.
author: josaw1
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c84c829ca1344d70dee294da35b659299d6fa37
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802723"
---
# <a name="create-product-packages-for-purchase-orders"></a>Preču iepakojumu izveide pirkšanas pasūtījumiem

[!include [banner](../includes/banner.md)]

Šajā procedūrā ir aprakstīts, ka izveidot preču pakotni un izmantot to pirkšanas pasūtījumā. Pirkšanas pasūtījums tiks izmantots, lai izveidotu pasūtījumu iepriekš definētai preču kopai. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.


## <a name="create-a-product-package"></a>Preču pakotnes izveide
1. Pārejiet uz sadaļu Mazumtirdzniecība un tirdzniecība > Krājumu pārvaldība > Papildināšana > Preču pakotnes.
2. Noklikšķiniet uz Jauns.
3. Laukā Pakotnes numurs ierakstiet vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Noklikšķiniet uz Pievienot.
8. Laukā Krājuma kods ierakstiet 0160.
9. Laukā Lielums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Laukā Daudzums ievadiet skaitli.
12. Noklikšķiniet uz Pievienot.
13. Laukā Krājuma kods ierakstiet 0160.
14. Laukā Varianta numurs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
15. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
16. Laukā Daudzums ievadiet skaitli.
17. Noklikšķiniet uz Pievienot.
18. Laukā Krājuma kods ierakstiet 0175.
19. Laukā Daudzums ievadiet skaitli.
20. Noklikšķiniet uz Saglabāt.
21. Aizvērt lapu.

## <a name="add-package-to-purchase-order"></a>Iepakojuma pievienošana pirkšanas pasūtījumam
1. Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atlasiet to pašu kreditoru, kam iepriekš tika izveidota preču pakotne, ja kreditors tika atlasīts.
5. Pārslēdziet sadaļas Vispārīgi paplašinājumu.
6. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
10. Noklikšķiniet uz Labi.
11. Pārslēdziet sadaļas Detalizēta rindas informācija paplašinājumu.
12. Noklikšķiniet uz cilnes Preču pakotnes.
13. Noklikšķiniet uz Pirkšanas pasūtījuma rinda.
14. Noklikšķiniet uz Izveidot rindas, izmantojot pakotni.
15. Sarakstā atrodiet un atlasiet preču pakotni, kas tika izveidota iepriekšējā darbībā.
16. Laukā Daudzums ierakstiet kādu skaitli.
17. Noklikšķiniet uz Izveidot.
18. Noklikšķiniet uz Saglabāt.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]