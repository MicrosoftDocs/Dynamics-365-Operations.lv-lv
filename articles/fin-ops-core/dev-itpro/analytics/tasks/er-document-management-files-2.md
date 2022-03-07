---
title: ER dokumentu pārvaldības faili, ko izmanto formāta izvades datos (2. daļa. Datu modeļa paplašināšana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) formātu dokumentu pārvaldības failu (pielikumu) izmantošanai ER izvadē. (2. daļa)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d20738fbdfd85390870c935576d954d3050029f557fe8b5b690329f9e4a0aab4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733753"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a>ER dokumentu pārvaldības faili, ko izmanto formāta izvades datos (2. daļa. Datu modeļa paplašināšana)

[!include [banner](../../includes/banner.md)]

Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektroniskā pārskata izstrādātājs, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē. Šīs darbības var veikt jebkurā uzņēmumā.

Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti uzdevuma ceļvedī "ER Izmantot dokumentu pārvaldības failus formāta izvadē (1. daļa: Sagatavot datu modeli)".

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Paplašināt datu modeli, lai parādītu tajā dokumentu pārvaldības failus
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
3. Koka struktūrā izvērsiet 'Customer invoice model'.
4. Koka struktūrā atlasiet 'Customer invoice model\Customer invoice model (custom)'.
5. Noklikšķiniet uz Veidotājs.
6. Koka struktūrā atlasiet 'Customer invoice(InvoiceCustomer)'.
    * Mēs paplašināsim šo datu modeli, lai būtu pieejami visi tam pārdošanas pasūtījumam pievienotie faili, kas ir saistīts ar elektroniski apstrādātu rēķinu.  
7. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
8. Laukā Nosaukums ierakstiet 'Invoice attachments'.
    * Rēķinu pielikumi  
9. Laukā Vienuma tips atlasiet "Record list".
10. Noklikšķiniet uz Pievienot.
11. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
12. Laukā Nosaukums ierakstiet 'File content'.
    * Faila saturs  
13. Laukā Vienuma tips atlasiet 'Container'.
14. Noklikšķiniet uz Pievienot.
15. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
16. Laukā Nosaukums ierakstiet 'File name'.
    * Faila nosaukums  
17. Laukā Vienuma tips atlasiet "String".
18. Noklikšķiniet uz Pievienot.

## <a name="map-new-data-model-elements-to-data-sources"></a>Saistīt jauna datu modeļa elementus ar datu avotiem
1. Noklikšķiniet uz Kartēšanas modelis datu avotam.
2. Izmantojiet ātrā filtra funkciju, lai filtrētu lauku Definīcija ar vērtību 'InvoiceCustomer'.
    * InvoiceCustomer  
    * Mēs saistīsim jaunā modeļa elementus ar piemērotiem datu avotiem.  
3. Noklikšķiniet uz Veidotājs.
4. Koka struktūrā atlasiet 'Invoice attachments'.
5. Koka struktūrā izvērsiet 'Invoice attachments'.
6. Koka struktūrā atlasiet 'Invoice attachments\File name'.
7. Noklikšķiniet uz Rediģēt.
8. Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Noklikšķiniet uz Saglabāt.
10. Aizvērt lapu.
11. Koka struktūrā atlasiet 'Invoice attachments\File content'.
12. Noklikšķiniet uz Rediģēt.
13. Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. Noklikšķiniet uz Saglabāt.
15. Aizvērt lapu.
16. Koka struktūrā atlasiet 'Invoice attachments'.
17. Noklikšķiniet uz Rediģēt.
18. Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Noklikšķiniet uz Saglabāt.
20. Aizvērt lapu.
21. Noklikšķiniet uz Saglabāt.
22. Aizvērt lapu.
23. Aizvērt lapu.
24. Aizvērt lapu.
25. Noklikšķiniet uz Mainīt statusu.
26. Noklikšķiniet uz Pabeigt.
27. Noklikšķiniet uz OK.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]