---
title: ER dokumentu pārvaldības faili, ko izmanto formāta izvades datos (5. daļa. Formāta modificēšana un darbināšana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) formātu dokumentu pārvaldības failu (pielikumu) izmantošanai ER izvadē. (5. daļa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f96189163d5ecac47ade9f713b3fd689e41352d0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092492"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a>ER dokumentu pārvaldības faili, ko izmanto formāta izvades datos (5. daļa. Formāta modificēšana un darbināšana)

[!include [banner](../../includes/banner.md)]

Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē. Šīs darbības var veikt uzņēmumā DEMF.

Lai veiktu šīs darbības, vispirms pabeidziet darbības procedūrā "ER izmantot dokumentu pārvaldības failus formāta izvadēs (4. daļa: Formatēšanas izpilde)".

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Modificējiet formātu, lai aizpildītu pielikumus, ģenerējot ziņojumus binārā formātā
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Koka struktūrā izvērsiet 'Customer invoice model'.
3. Kokā izvērsiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)".
4. Kokā atlasiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)\Elektronisks rēķina parauga ziņojums".
5. Noklikšķiniet uz Veidotājs.
    * Jūs aizpildīsiet rēķina ziņojumu, veidojot ražojumu kā XML failu, izmantojot unikoda kodējumu.  
6. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
7. Kokā atlasiet "Vispārīgi\Fails".
8. Laukā Nosaukums ierakstiet 'Xml ziņojums'.
    * Xml ziņojums  
9. Laukā Kodēšana ierakstiet "UTF-8".
    * UTF-8  
10. Noklikšķiniet uz OK.
    * Konfigurējiet ražojuma veidošanu kā arhivēto failu.  
11. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
12. Kokā atlasiet "Vispārīgi\Mape".
13. Laukā Nosaukums ierakstiet 'Arhivēta izvade.
    * Zip izvade  
14. Noklikšķiniet uz OK.
15. Kokā atlasiet 'Arhivēta izvade'.
    * Pievienojiet pielikumus veidošanas arhivētajam failam kā failus ar sākotnējiem nosaukumiem un paplašinājumiem.  
16. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
17. Kokā atlasiet "Vispārīgi\Fails".
18. Laukā Nosaukums, ierakstiet 'Pievienotais fails'.
    * Pievienotais fails  
19. Noklikšķiniet uz OK.
20. Kokā atlasiet 'Arhivēta izvade\Pievienotais fails'.
21. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
22. Koka struktūrā atlasiet 'Text\Base64'.
23. Noklikšķiniet uz OK.

## <a name="map-new-format-elements-to-data-model"></a>Kartējiet jaunus formatēšanas elementus datu modelī
1. Noklikšķiniet uz cilnes Kartēšana.
2. Koka struktūrā izvērsiet elementu “modelis”.
3. Koka struktūrā izvērsiet 'model\Invoice attachments'.
4. Kokā atlasiet 'Arhivēta izvade\Pievienotais fails\Base64'.
5. Koka struktūrā atlasiet 'model\Invoice attachments\File content'.
6. Noklikšķiniet uz Saistīt.
7. Kokā atlasiet 'Arhivēta izvade\Pievienotais fails'.
8. Noklikšķiniet uz rediģēt faila nosaukumu.
9. Koka struktūrā izvērsiet elementu “modelis”.
10. Koka struktūrā izvērsiet 'model\Invoice attachments'.
11. Koka struktūrā atlasiet 'model\Invoice attachments\File name'.
12. Noklikšķiniet uz Pievienot datu avotu.
13. Klikšķiniet Saglabāt.
14. Aizvērt lapu.
15. Koka struktūrā atlasiet 'model\Invoice attachments'.
16. Noklikšķiniet uz Saistīt.
17. Noklikšķiniet uz Saglabāt.
18. Aizvērt lapu.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Atlasītajam rēķinam noformētas atskaites palaišana
1. Noklikšķiniet uz Palaist.
2. Izvērsiet sadaļu Iekļaujamie ieraksti.
3. Noklikšķiniet uz Filtrēt.
4. Atlasiet rindu no debitora rēķinu žurnāla un pārdošanas pasūtījuma lauka.
5. Laukā Kritēriji, kritērija laukā "Pārdošanas pasūtījums" laukā ierakstiet pasūtījuma numuru 000148.
    * 000148  
6. Noklikšķiniet uz Labi.
7. Noklikšķiniet uz Labi.
    * Pārskatiet ģenerēto izvadi. Ņemiet vērā, ka papildus rēķina ziņojumam XML formātā, viens fails tika izveidots katram pielikumam. Pielikumu faili tiek aizpildīti ar arhivētu izvadi binārā formātā.  

