---
title: Tāda pieprasījuma izveide, kas lieto PP
description: Šajā rakstā skaidrots, kā pievienot cenas un kreditora informāciju pirkšanas pieprasījumam no PP procesa.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecde250e3517464611b68fe3c960bfbfdf06319
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846016"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Tāda pieprasījuma izveide, kas lieto PP

[!include [banner](../../includes/banner.md)]

Šajā rakstā skaidrots, kā pievienot cenas un kreditora informāciju pirkšanas pieprasījumam no PP procesa. Šajā ceļvedī parādīto piemēru var izmantot paraugdatu uzņēmumā USMF, un jums ir jāpiesakās kā administratoram, lai izpildītu visas darbības. Šajā ceļvedī aprakstītos uzdevumus parasti veiktu sagādes speciālisti.


## <a name="create-a-requisition"></a>Izveidot pieprasījumu
1. Navigācijas rūtī ejiet uz **Moduļi > Iepirkumi un ārpakalpojumi > Pirkšanas pieprasījumi > Manis sagatavotie pirkšanas pieprasījumi**.
2. Atlasiet **Jauns**.
3. Laukā **Nosaukums** ierakstiet kādu vērtību.
4. Laukā **Pieprasītais datums** ievadiet datumu.
5. Laukā **Uzskaites datums** ievadiet datumu.
6. Atlasiet **Labi**.
7. Laukā **Iemesls** ievadiet vai atlasiet vērtību.
8. Atlasiet **Pievienot rindu**.
9. Laukā **Iepirkuma kategorija**, atlasiet kategoriju kokā, tad atlasiet **Labi**.
10. Laukā **Preces nosaukums** ierakstiet vērtību.
11. Laukā **Daudzums** ierakstiet kādu skaitli.
12. Laukā **Vienība** ievadiet vai atlasiet kādu vērtību.
13. Atlasiet **Saglabāt**.
14. Atlasiet **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu.
15. Atlasiet **Iesniegt**.
16. Aizvērt lapu.
17. Atlasiet **Iesniegt**.

## <a name="reassign-a-workflow-task"></a>Darbplūsmas uzdevuma piešķires maiņa
Nākamais uzdevums ir izveidot IP, lai no kreditoriem saņemtu piedāvājumus par preci. USMF paraugdatos pieprasījuma darbplūsma ir iestatīta ar kārtulu, tāpēc, ja nav atlasīts kreditors vai ja vienības cena kādai rindai ir 0, konkrētam nodarbinātajam tiek piešķirts uzdevums izveidot IP. Lai turpinātu ar šo ceļvedi, šis uzdevums ir jāpiešķir citam lietotājam (sev). To varat izdarīt tikai tad, ja esat pieteicies kā Administrators.  

1. Atlasiet **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu.
2. Atlasiet **Skatīt vēsturi**.
3. Atsvaidziniet lapu.
4. Izvērsiet **Izsekošanas detaļas** sadaļu
5. Kokā atlasiet rindu, kas sākas ar "Rindas darbplūsma aktivizēta".
6. Atlasiet **Skatīt darbplūsmas detaļas**.
7. Izvērsiet sadaļu **Darba vienumi**.
8. Atlasiet **Atkārtoti piešķirt**.
9. Laukā **Lietotājs** atlasiet **Administrators**.
10. Atlasiet **Atkārtoti piešķirt**.
11. Aizveriet abas lapas.

## <a name="create-an-rfq"></a>Izveidot PP

1. Atsvaidziniet lapu.
2. Atlasiet **Piedāvājuma pieprasījums**.
3. Lauka **Pērkošā juridiskā persona** atlasiet **USMF**. Jums ir jāatlasa tā pati juridiskā persona, kas ir norādīta pieprasījuma rindā.  
4. Sarakstā atzīmējiet atlasīto rindu. Ja jūsu pirkšanas pieprasījumā bija vairākas rindas, atlasiet visas tās rindas, kuras vēlaties pievienot šim IP.  
5. Atlasiet **Labi**.
6. Atsvaidziniet lapu.
7. Pārliecinieties, ka ir atvērti Notikumi, tad izvērsiet sadaļu **Saistīti dokumenti**.
8. Atlasiet saiti laukā **Piedāvājuma pieprasījums**, lai atvērtu tikko izveidoto piedāvājuma pieprasījumu.
9. Atlasiet **Galvene**.
10. Atlasiet **Pievienot**.
11. Laukā **Kreditora konts** ievadiet vai atlasiet vērtību.
12. Atlasiet **Pievienot**.
13. Laukā **Kreditora konts** ievadiet vai atlasiet vērtību.
14. Atlasiet **Nosūtīt**.
15. Atlasiet **Labi**.
16. Atlasiet **Ievadīt atbildi**.
17. Darbību rūtī atlasiet **Atbilde**.
18. Atlasiet **Kopēt datus uz atbildi**. Šādi no IP uz atbildi tiek kopēti dati, piemēram, daudzums un datumi.  
19. Laukā **Vienības cena** ievadiet kādu skaitli. Šī ir cena, ko saņēmāt no kreditora. Iespējams, vēlaties arī ievadīt papildinformāciju no kreditora.  
20. Atlasiet **Pieņemt**.
21. Atlasiet **Labi**.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Pārliecinieties, ka uz pieprasījumu ir pārsūtīts kreditors un cena
1. Aizvērt lapu.
2. Atlasiet **Rindas**.
3. Atlasiet **Saistītā informācija**.
4. Atlasiet **Pirkšanas pieprasījums**.
5. Atlasiet rindu, kura tika pārsūtīta uz IP. Pārliecinieties, ka uz pieprasījumu ir pārkopēta cena un kreditors.  
6. Atlasiet **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu.
7. Atlasiet Pabeigt.
8. Atlasiet lapu.
9. Atlasiet Pabeigt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]