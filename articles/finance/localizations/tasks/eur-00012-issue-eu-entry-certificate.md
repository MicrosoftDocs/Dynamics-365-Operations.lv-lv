---
title: EUR-00012 ES ieraksta sertifikāta izsniegšana
description: Šajā procedūrā ir izklāstīts, kā iespējot ES ieraksta sertifikātu, konfigurēt debitora kontu ierakstu sertifikātu izmantošanai un sertifikātu izsniegšanai.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0091af30b917aab3b8c4572a72a20d8d2d5d52e2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408254"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a>EUR-00012 ES ieraksta sertifikāta izsniegšana

[!include [banner](../../includes/banner.md)]
Šajā procedūrā ir izklāstīts, kā iespējot ES ieraksta sertifikātu, konfigurēt debitora kontu ierakstu sertifikātu izmantošanai un sertifikātu izsniegšanai. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma DEMF dati.


## <a name="enable-entry-certificate-management"></a>Iespējot ieraksta sertifikāta pārvaldību
1. Pārejiet uz sadaļu Debitori > Iestatījumi > Debitoru parametri.
2. Noklikšķiniet uz cilnes Sūtījumi.
3. Izvērsiet sadaļu Ieraksta sertifikāts.
4. Atlasiet Jā laukā Iespējot ieraksta sertifikāta pārvaldību.
5. Atlasiet Jā laukā Iespējot ieraksta sertifikāta izsniegšanu.
6. Noklikšķiniet uz cilnes Numuru sērijas.
7. Sarakstā atrodiet un atlasiet rindu Ieraksta sertifikāts.
8. Laukā Numuru sērijas kods ievadiet vai atlasiet kādu vērtību.

## <a name="set-up-a-customer"></a>Debitora iestatīšana
1. Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Konts vērtības DE-015.
3. Atveriet debitora konta detaļas.
4. Noklikšķiniet uz Rediģēt.
5. Izvērsiet sadaļu Rēķins un piegāde.
6. Atlasiet Jā laukā Nepieciešams ieraksta sertifikāts.
7. Atlasiet Jā laukā Izsniegt ieraksta sertifikātu.
8. Noklikšķiniet uz Saglabāt.

## <a name="create-an-eu-entry-certificate-automatically"></a>ES ieraksta sertifikāta automātiskā izveide
1. Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
4. Noklikšķiniet uz Labi.
5. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
6. Noklikšķiniet uz Saglabāt.
7. Darbību rūtī noklikšķiniet uz Izdot un iepakot.
8. Noklikšķiniet uz Grāmatot pavadzīmi.
9. Izvērsiet sadaļu Parametri.
10. Laukā Daudzums atlasiet vērtību Visi.
11. Notīriet izvēles rūtiņu Izsniegt ieraksta sertifikātu.
    * Ieraksta sertifikātu var izsniegt pavadzīmes grāmatošanas laikā vai pasūtījuma rēķina izrakstīšanas laikā. Neatzīmējiet izvēles rūtiņu Izsniegt ieraksta sertifikātu, lai to izsniegtu vēlāk.  
12. Noklikšķiniet uz OK.
13. Noklikšķiniet uz OK.
14. Darbību rūtī noklikšķiniet uz Rēķins.
15. Noklikšķiniet uz Rēķins.
    * Pārbaudiet, vai sadaļā Pārskats ir atzīmētas izvēles rūtiņas Nepieciešams ieraksta sertifikāts un Izsniegt ieraksta sertifikātu.  Var arī atzīmēt izvēles rūtiņu Drukāt ieraksta sertifikātu, lai atļautu veikt sertifikāta izdrukas.  
16. Noklikšķiniet uz OK.
17. Noklikšķiniet uz OK.
18. Darbību rūtī noklikšķiniet uz Rēķins.
19. Noklikšķiniet uz Rēķins.
20. Darbību rūtī noklikšķiniet uz Rēķins.
21. Noklikšķiniet uz Skatīt izsniegtos ierakstu sertifikātus.
22. Klikšķiniet Drukāt.
23. Aizvērt lapu.
24. Noklikšķiniet uz Mainīt statusu.
25. Laukā Jauns statuss atlasiet kādu opciju.
26. Noklikšķiniet uz OK.
27. Aizvērt lapu.

## <a name="create-an-eu-entry-certificate-manually"></a>ES ieraksta sertifikāta manuālā izveide
1. Darbību rūtī noklikšķiniet uz Rēķins.
2. Noklikšķiniet uz Izveidot ieraksta sertifikātu.
3. Noklikšķiniet uz Labi.
4. Darbību rūtī noklikšķiniet uz Rēķins.
5. Noklikšķiniet uz Skatīt izsniegtos ierakstu sertifikātus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]