---
title: Izņēmumu izpēte vai atrisināšana
description: Kreditoru rēķinu politikas tiek palaistas, kad kreditora rēķinu grāmatojat, izmantojot lapu Kreditora rēķins un kad atverat kreditora rēķinu lapu Ierobežojumu pārkāpumi.
author: abruer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abc8dc112ab577ddcbd208f898a8d4e487bc2998
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827774"
---
# <a name="research-or-resolve-exceptions"></a>Izņēmumu izpēte vai atrisināšana

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]