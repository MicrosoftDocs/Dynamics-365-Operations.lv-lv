---
title: Izpēte/izņēmumu novēršana
description: Kreditoru rēķinu politikas tiek palaistas, kad kreditora rēķinu grāmatojat, izmantojot lapu Kreditora rēķins un kad atverat kreditora rēķinu lapu Ierobežojumu pārkāpumi.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2f2e7d401e97aeab9dbc74f65e1a0c03eb0c880
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189342"
---
# <a name="researchresolve-exceptions"></a>Izpēte/izņēmumu novēršana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kreditoru rēķinu politikas tiek palaistas, kad kreditora rēķinu grāmatojat, izmantojot lapu Kreditora rēķins un kad atverat kreditora rēķinu lapu Ierobežojumu pārkāpumi. Varat arī konfigurēt kreditora rēķina darbplūsmu, lai kreditoru rēķinu ierobežojumi tiktu palaisti katru reizi, kad darbplūsmā iesniedzat kādu rēķinu. 

Kreditoru rēķinu ierobežojumi neattiecas uz rēķiniem, kas tika izveidoti rēķinu reģistrā vai rēķinu žurnālā. 

Rēķinu salīdzināšanas pārbaudes neizmanto kreditoru rēķinu ierobežojumus, bet tā vietā ir iestatītas lapā Kreditoru moduļa parametri.

Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums. Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs. Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Sagatavoties kreditoru rēķinu ierobežojumu izveidošanai
1. Pārejiet uz sadaļu Kreditori > Iestatījumi > Kreditoru parametri.
2. Noklikšķiniet uz cilnes Rēķinu validēšana.
3. Atzīmējiet vai notīriet izvēles rūtiņu Automātiski atjaunināt rēķina virsraksta statusu.
4. Noklikšķiniet uz Labi.
5. Laukā Grāmatot rēķinu ar neatbilstībām atlasiet kādu opciju.
6. Aizvērt lapu.
7. Pārejiet uz sadaļu Kreditori > Politikas iestatīšana > Kreditora rēķina ierobežojumi.
8. Noklikšķiniet uz Parametri.
9. Noklikšķiniet uz btnAdd.
10. Aizvērt lapu.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Izveidot ierobežojuma nosacījumu tipus kreditora rēķiniem
1. Pārejiet uz sadaļu Kreditori > Politikas iestatīšana > Kreditora rēķina ierobežojumu nosacījumu veidi.
2. Noklikšķiniet uz Jauns.
3. Laukā Kārtulas nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Vaicājuma nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Noklikšķiniet uz Saglabāt.
9. Aizvērt lapu.

## <a name="define-a-vendor-invoice-policy"></a>Definēt kreditora rēķina ierobežojumu
1. Pārejiet uz sadaļu Kreditori > Politikas iestatīšana > Kreditora rēķina ierobežojumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Izvērsiet vai sakļaujiet sadaļu Politikas organizācijas.
6. Koka struktūrā atlasiet “Contoso Entertainment System USA”.
7. Noklikšķiniet uz Pievienot.
8. Izvērsiet vai sakļaujiet sadaļu Ierobežojuma nosacījumi.
9. Noklikšķiniet uz Izveidot politikas kārtulu.
10. Laukā Ierobežojuma nosacījumi ierakstiet kādu vērtību.
11. Noklikšķiniet uz Filtrēt.
12. Noklikšķiniet uz Pievienot.
13. Sarakstā atzīmējiet atlasīto rindu.
14. Laukā Tabula noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
15. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
16. Laukā Atveidotā tabula noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
17. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
18. Laukā Lauks noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
19. Laukā Lauks ierakstiet kādu vērtību.
20. Aizvērt lapu.
21. Laukā Kritēriji ierakstiet kādu vērtību.
22. Noklikšķiniet uz OK.
23. Noklikšķiniet uz OK.
24. Aizvērt lapu.
25. Aizvērt lapu.
