---
title: ER izmantot dokumentu pārvaldības failus formātu izvades datos (3. daļa - Izveidot formātu)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) formātu dokumentu pārvaldības failu (pielikumu) izmantošanai ER izvadē. (3. daļa)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0cb052e2895cd0eb7f5c3bea9f33d988ef54dfb11e2e31c4212706b7fdaada79
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766389"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a>ER izmantot dokumentu pārvaldības failus formātu izvades datos (3. daļa - Izveidot formātu)

[!include [banner](../../includes/banner.md)]

Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē. Šīs darbības var veikt jebkurā uzņēmumā.

Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Izmantot dokumentu pārvaldības failus formāta izvadē (2. daļa: Paplašināt datu modeli)".

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="create-a-format-to-process-invoices"></a>Izveidot rēķinu apstrādes formātu
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
3. Koka struktūrā izvērsiet 'Customer invoice model'.
4. Koka struktūrā atlasiet 'Customer invoice model\Customer invoice model (custom)'.
    * Tiks izveidots formāts, lai ģenerētu elektroniskos ziņojumus ar informāciju par visiem failiem, kas ir pievienoti ar elektroniski apstrādāto rēķinu saistītajam pārdošanas pasūtījumam.  
5. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
6. Laukā Jauns ievadiet 'Format based on data model Customer invoice model (custom)'.
7. Laukā Nosaukums ierakstiet 'Electronic invoice sample message'.
    * Elektronisks rēķina parauga ziņojums  
8. Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.
    * InvoiceCustomer  
9. Klikšķiniet Izveidot konfigurāciju.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Izstrādāt pielikumu aizpildīšanas formātu, ģenerējot ziņojums MIME formātā
1. Noklikšķiniet uz Veidotājs.
2. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
3. Kokā atlasiet "XML\Elements".
4. Laukā Nosaukums ierakstiet 'Invoice'.
    * Rēķins  
5. Noklikšķiniet uz OK.
6. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
7. Kokā atlasiet "XML\Atribūts".
8. Laukā Nosaukums ierakstiet 'SalesOrder'.
    * SalesOrder  
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz Pievienot atribūtu.
11. Laukā Nosaukums ierakstiet 'InvoiceNumber'.
    * InvoiceNumber  
12. Noklikšķiniet uz OK.
13. Noklikšķiniet uz Pievienot atribūtu.
14. Laukā Nosaukums ierakstiet 'InvoiceAmount'.
    * InvoiceAmount  
15. Noklikšķiniet uz OK.
16. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
17. Kokā atlasiet "XML\Elements".
18. Laukā Nosaukums ierakstiet 'EnclosedDocs'.
    * EnclosedDocs  
19. Noklikšķiniet uz OK.
20. Koka struktūrā atlasiet 'Invoice\EnclosedDocs'.
21. Noklikšķiniet uz Pievienot elementu.
22. Laukā Nosaukums ierakstiet 'Document'.
    * Attaisnojuma dokuments  
23. Noklikšķiniet uz OK.
24. Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document'.
25. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
26. Kokā atlasiet "XML\Atribūts".
27. Laukā Nosaukums ierakstiet 'FileName'.
    * FileName  
28. Noklikšķiniet uz OK.
29. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
30. Kokā atlasiet "XML\Elements".
31. Laukā Nosaukums ierakstiet 'FileContent'.
    * FileContent  
32. Noklikšķiniet uz OK.
33. Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document\FileContent'.
34. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
35. Koka struktūrā atlasiet 'Text\Base64'.
36. Noklikšķiniet uz OK.

## <a name="map-format-elements-to-data-model-as-data-source"></a>Saistīt formāta elementus ar datu modeli kā datu avotu
1. Koka struktūrā atlasiet 'Invoice\SalesOrder'.
2. Noklikšķiniet uz cilnes Kartēšana.
3. Koka struktūrā izvērsiet elementu “modelis”.
4. Koka struktūrā atlasiet 'model\Sales order number(SalesId)'.
5. Noklikšķiniet uz Saistīt.
6. Koka struktūrā atlasiet 'Invoice\InvoiceNumber'.
7. Koka struktūrā izvērsiet 'model\Base invoice(InvoiceBase)'.
8. Koka struktūrā izvērsiet 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.
9. Noklikšķiniet uz Saistīt.
10. Koka struktūrā atlasiet 'Invoice\InvoiceAmount'.
11. Koka struktūrā atlasiet 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.
12. Noklikšķiniet uz Saistīt.
13. Koka struktūrā izvērsiet 'model\Invoice attachments'.
14. Koka struktūrā atlasiet 'model\Invoice attachments\File content'.
15. Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document\FileContent\Base64'.
16. Noklikšķiniet uz Saistīt.
17. Koka struktūrā atlasiet 'model\Invoice attachments\File name'.
18. Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document\FileName'.
19. Noklikšķiniet uz Saistīt.
20. Koka struktūrā atlasiet 'model\Invoice attachments'.
21. Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document'.
22. Noklikšķiniet uz Saistīt.
23. Noklikšķiniet uz Saglabāt.
24. Aizvērt lapu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]