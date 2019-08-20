---
title: Kreditoru rēķinu politiku iestatīšana
description: Šajā tēmā ir paskaidrots, kā iestatīt kreditora rēķinu politikas programmā Dynamics 365 for Finance and Operatoins.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 328aafd16496fdbb963c9aa40a5c13005be7a382
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842813"
---
# <a name="set-up-vendor-invoice-policies"></a>Kreditoru rēķinu politiku iestatīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt kreditora rēķinu politikas programmā Dynamics 365 for Finance and Operatoins. Kreditoru rēķinu politikas tiek palaistas, kad kreditora rēķinu grāmatojat, izmantojot lapu Kreditora rēķins un kad atverat kreditora rēķinu lapu Ierobežojumu pārkāpumi. Varat arī konfigurēt kreditora rēķina darbplūsmu, lai kreditoru rēķinu ierobežojumi tiktu palaisti katru reizi, kad darbplūsmā iesniedzat kādu rēķinu. 

- Kreditoru rēķinu ierobežojumi neattiecas uz rēķiniem, kas tika izveidoti rēķinu reģistrā vai rēķinu žurnālā.  
- Rēķinu salīdzināšanas pārbaudes neizmanto kreditoru rēķinu ierobežojumus, bet tā vietā ir iestatītas lapā Kreditoru moduļa parametri.  
- Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums. Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs. Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Sagatavoties kreditoru rēķinu ierobežojumu izveidošanai
1. Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Kreditori > Iestatīšana > Kreditoru parametri**.
2. Atlasiet cilni **Rēķinu validēšana**.
3. Atzīmējiet vai notīriet izvēles rūtiņu **Automātiski atjaunināt rēķina virsraksta statusu**.
4. Atlasiet **Labi**.
5. Laukā **Grāmatot rēķinu ar neatbilstībām** atlasiet kādu opciju.
6. Aizvērt lapu.
7. Pārejiet uz **Navigācijas rūts > Moduļi > Kreditori > Politikas iestatīšana > Kreditora rēķina politikas**.
8. Atlasiet **Parametri**.
9. Atlasiet **Pievienot**.
10. Aizveriet lapu, lai atgrieztos lapā sākuma lapā.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Izveidot ierobežojuma nosacījumu tipus kreditora rēķiniem
1. Pārejiet uz **Navigācijas rūts > Moduļi > Kreditori > Politikas iestatīšana > Kreditora rēķina ierobežojuma nosacījumu veidi**.
2. Atlasiet **Jauns**.
3. Ievadiet vērtības laukos **Noteikumu nosaukums** un **Apraksts**.
4. Laukā **Vaicājuma nosaukums** atlasiet nolaižamo pogu, lai atvērtu uzmeklēšanu, pēc tam atlasiet vēlamo ierakstu.
5. Atlasiet **Saglabāt**.
6. Aizveriet lapu, lai atgrieztos lapā sākuma lapā.

## <a name="define-a-vendor-invoice-policy"></a>Definēt kreditora rēķina ierobežojumu
1. Pārejiet uz **Navigācijas rūts > Moduļi > Kreditori > Politikas iestatīšana > Kreditora rēķina politikas**.
2. Atlasiet **Jauns**.
3. Ievadiet vērtības laukos **Nosaukums** un **Apraksts**.
4. Izvērsiet vai sakļaujiet sadaļu **Politikas organizācijas**.
5. Koka struktūrā atlasiet **Contoso Entertainment System USA**.
6. Atlasiet **Pievienot**.
7. Izvērsiet vai sakļaujiet sadaļu **Ierobežojuma nosacījumi**.
8. Atlasiet **Izveidot ierobežojuma nosacījumu**.
9. Laukā **Ierobežojuma nosacījumu apraksts** ierakstiet kādu vērtību.
10. Atlasiet **Filtrēt**.
11. Atlasiet **Pievienot**. Atlasīt vēlamo ierakstu.
12. Laukā **Tabula**, **Atvasinātāstabula** un **Lauks** atlasiet vai ievadiet opcijas no nolaižamajām izvēlnēm.
13. Aizvērt lapu.
14. Laukā **Kritēriji** ierakstiet kādu vērtību.
15. Atlasiet **Labi**.
16. Atlasiet **Labi**.
17. Aizveriet lapas, lai atgrieztos lapā sākuma lapā.

