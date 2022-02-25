---
title: Kreditoru rēķinu politiku iestatīšana
description: Šajā tēmā ir izskaidrots, kā iestatīt kreditora rēķina politiku.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f9707c7b283f42729126efa57e890e0df65ca8b
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109760"
---
# <a name="set-up-vendor-invoice-policies"></a>Kreditoru rēķinu politiku iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir izskaidrots, kā iestatīt kreditora rēķina politiku. Kreditora rēķina politikas tiek palaistas, kad grāmatojat **kreditora** rēķinu, izmantojot kreditora rēķina lapu un atverot kreditoru rēķinu politikas **pārkāpumu** lapu. Varat arī konfigurēt kreditora rēķina darbplūsmu, lai kreditoru rēķinu ierobežojumi tiktu palaisti katru reizi, kad darbplūsmā iesniedzat kādu rēķinu. 

- Kreditoru rēķinu ierobežojumi neattiecas uz rēķiniem, kas tika izveidoti rēķinu reģistrā vai rēķinu žurnālā.  
- Rēķinu salīdzināšanas apstiprināšana neizmanto kreditora rēķinu ierobežojumus, bet gan iestatīta kreditoru **parametru** lapā.  
- Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums. Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs. Pirms sākat, pārliecinieties, ka **ir atlasīta rēķinu** salīdzināšanas konfigurācijas atslēga.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
