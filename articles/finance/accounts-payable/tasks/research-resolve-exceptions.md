---
title: Izņēmumu izpēte vai atrisināšana
description: Kreditoru rēķinu politikas tiek palaistas, kad kreditora rēķinu grāmatojat, izmantojot lapu Kreditora rēķins un kad atverat kreditora rēķinu lapu Ierobežojumu pārkāpumi.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32ff53198f61e1d1af3c437e9488c2a246cf820a
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2022
ms.locfileid: "8110023"
---
# <a name="research-or-resolve-exceptions"></a>Izņēmumu izpēte vai atrisināšana

[!include [banner](../../includes/banner.md)]

Kreditora rēķina politikas tiek palaistas, kad grāmatojat **kreditora** rēķinu, izmantojot kreditora rēķina lapu un atverot kreditoru rēķinu politikas **pārkāpumu** lapu. Varat arī konfigurēt kreditora rēķina darbplūsmu, lai kreditoru rēķinu ierobežojumi tiktu palaisti katru reizi, kad darbplūsmā iesniedzat kādu rēķinu. 

Kreditora rēķinu politikas neattiecas uz rēķiniem, kas izveidoti rēķinu **reģistrā vai** rēķinu **žurnālā**. 

Rēķinu salīdzināšanas apstiprināšana neizmanto kreditora rēķinu ierobežojumus, bet ir iestatīta kreditoru **parametru** lapā.

Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums. Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs. Pirms sākat, pārliecinieties, ka **ir atlasīta rēķinu salīdzināšanas** konfigurācijas atslēga.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Sagatavoties kreditoru rēķinu ierobežojumu izveidošanai
1. Dodieties uz **Parādi kreditoriem > Iestatīšana > Kreditoru moduļa parametri**.
2. Noklikšķiniet uz **cilnes Rēķina** pārbaude.
3. Atzīmējiet vai notīriet **izvēles rūtiņu Automātiski atjaunināt rēķina** virsraksta statusu.
4. Noklikšķiniet uz **Labi**.
5. Laukā **Grāmatot rēķinu ar neatbilstībām** atlasiet kādu opciju.
6. Aizvērt lapu.
7. Pārejiet uz **sadaļu Kreditoru > ierobežojumu > kreditora rēķinu politikām**.
8. Noklikšķiniet uz **Parametri**.
9. Noklikšķiniet uz **Pievienot**.
10. Aizvērt lapu.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Izveidot ierobežojuma nosacījumu tipus kreditora rēķiniem
1. Pārejiet uz **sadaļu Kreditoru > ierobežojumu > kreditoru rēķinu ierobežojumu nosacījumu tipiem**.
2. Klikšķiniet **Jauns**.
3. Laukā **Noteikuma nosaukums** ierakstiet vērtību.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Laukā **Vaicājuma nosaukums** noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Noklikšķiniet uz **Saglabāt**.
9. Aizvērt lapu.

## <a name="define-a-vendor-invoice-policy"></a>Definēt kreditora rēķina ierobežojumu
1. Pārejiet uz **sadaļu Kreditoru > ierobežojumu > kreditora rēķinu politikām**.
2. Klikšķiniet **Jauns**.
3. Laukā **Nosaukums** ierakstiet kādu vērtību.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Izvērsiet vai sakļaujiet sadaļu **Politikas organizācijas**.
6. Koka struktūrā atlasiet “Contoso Entertainment System USA”.
7. Noklikšķiniet uz **Pievienot**.
8. Izvērsiet vai sakļaujiet sadaļu **Ierobežojuma nosacījumi**.
9. Noklikšķiniet uz **Izveidot ierobežojuma nosacījumus**.
10. Laukā **Ierobežojuma nosacījumu apraksts** ierakstiet kādu vērtību.
11. Noklikšķiniet uz **Filtrēt**.
12. Noklikšķiniet uz **Pievienot**.
13. Sarakstā atzīmējiet atlasīto rindu.
14. Laukā **Tabula** noklikšķiniet uz nolaižamās pogas, lai atvērtu uzmeklēšanu.
15. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
16. Laukā **Atvasinātā** tabula noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
17. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
18. Laukā **Lauks** noklikšķiniet uz nolaižamās pogas, lai atvērtu uzmeklēšanu.
19. **Laukā Lauks** ierakstiet vērtību.
20. Aizvērt lapu.
21. Laukā **Kritēriji** ierakstiet kādu vērtību.
22. Noklikšķiniet uz **Labi**.
23. Noklikšķiniet uz **Labi**.
24. Aizvērt lapu.
25. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
