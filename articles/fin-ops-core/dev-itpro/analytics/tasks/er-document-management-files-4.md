---
title: ER izmantot dokumentu pārvaldības failus formātu izvades datos (4. daļa - Palaist formātu)
description: Šajā rakstā ir aprakstīts, kā konfigurēt elektronisko pārskatu formātu dokumentu pārvaldības failu izmantošanai ER izvadē. (4. daļa)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
ms.openlocfilehash: 3d4e26d15ea287c99cac85bf383e09c15729d37a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290970"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a>ER izmantot dokumentu pārvaldības failus formātu izvades datos (4. daļa - Palaist formātu)

[!include [banner](../../includes/banner.md)]

Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē. Šīs darbības var veikt uzņēmumā DEMF.

Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Izmantot dokumentu pārvaldības failus formāta izvadē (3. daļa: Izveidot formātu)".

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Pievienojiet viena rēķina nepieciešamos pielikumus pārdošanas pasūtījumam.
1. Pārejiet uz sadaļu Debitori > Rēķini > Atvērtie debitoru rēķini.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet lauku Rēķins ar vērtību 'CIV-000148'.
    * CIV-000148  
3. Noklikšķiniet, lai atvērtu atlasīto rēķina saiti.
    * CIV-000148  
4. Noklikšķiniet, lai atvērtu saiti laukā Pārdošanas pasūtījums.
    * 000148  
5. Laukā rindas vai virsrakstw, atlasiet Virsraksta opciju.
    * Atlasiet Virsraksts, lai norādītu, ka šis ir pielikumu pievienošanas mērķis.  
6. Noklikšķiniet uz Pievienot.
    * Pievienojiet šim pārdošanas pasūtījumam dažus failus kā pielikumus. Izmantojiet tādu dokumentu tipu failus, ko atbalsta dokumentu pārvaldība (ar faila paplašinājumu DOCX, DPF, XML, JPG u. c.). Pārlūkojiet un atlasiet failus, kas jāpievieno un papildus jāapstrādā kopā ar attiecīgo rēķinu ER elektroniskajā ziņojumā.  
7. Noklikšķiniet uz Jauns.
8. Noklikšķiniet uz Fails.
9. Noklikšķiniet uz Jauns.
10. Noklikšķiniet uz Fails.
11. Aizvērt lapu.
12. Aizvērt lapu.
13. Aizvērt lapu.
14. Aizvērt lapu.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Atlasītajam rēķinam noformētas atskaites palaišana
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Koka struktūrā izvērsiet 'Customer invoice model'.
3. Kokā izvērsiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)".
4. Kokā atlasiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)\Elektronisks rēķina parauga ziņojums".
5. Noklikšķiniet uz Palaist.
6. Izvērsiet sadaļu Iekļaujamie ieraksti.
7. Noklikšķiniet uz Filtrēt.
8. Atlasiet rindu no debitora rēķinu žurnāla un pārdošanas pasūtījuma lauka.
9. Laukā Kritēriji ierakstiet '000148'.
    * Kritērija laukā "Pārdošanas pasūtījums" ierakstiet pasūtījuma numuru 000148.  
10. Noklikšķiniet uz Labi.
11. Noklikšķiniet uz Labi.
    * Pārskatiet ģenerēto izvadi. Ņemiet vērā, ka katram pielikumam ir izveidots atsevišķs XML mezgls. Pielikuma saturs tiek aizpildīts XML izvadē MIME (base64) teksta formātā.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
