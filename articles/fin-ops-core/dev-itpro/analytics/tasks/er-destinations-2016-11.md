---
title: ER Konfigurēt adresātus
description: Šajā procedūrā parādīts, kā iestatīt un izmantot dažādus adresātus elektronisko pārskatu (ER) izvades komponentiem, piemēram, mapēm vai failiem.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7da1f26c4c01b8b71f14b8c5dfd79082baf92157
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567766"
---
# <a name="er-configure-destinations"></a>ER Konfigurēt adresātus

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā iestatīt un izmantot dažādus adresātus elektronisko pārskatu (ER) izvades komponentiem, piemēram, mapēm vai failiem. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF. Juridiskas personas primārās adreses valsts/reģions ir Vācija, tomēr šai procedūrai var izmantot jebkuru juridisko personu. 

Formāts, ko lieto šajā piemērā, ir ISO20022 pārvietošana kredītā, taču var izmantot jebkuru formātu, kas jau ir importēts. Ņemiet vērā, ka šī procedūra ir viena faila un adresāta iestatīšanas piemērs. Papildu informāciju par elektroniskās pārskatu veidošanas adresātu pārvaldību var atrast Dynamics 365 Finance palīdzībā.

1. Dodieties uz Organizācijas administrēšana > Elektroniskie pārskati > Elektroniskās pārskatu veidošanas adresāts.
2. Noklikšķiniet uz Jauns, lai izveidotu jaunu adresātu kopu attiecīgajam formātam.
3. Laukā Atsauce atlasiet formātu, kuram vēlaties konfigurēt adresātus.
    * Ja netiek piedāvātas vērtības atlasīšanai, tas nozīmē, ka nav importēta neviena elektroniskā pārskata formāta konfigurācija. Pirms adresātu iestatīšanas jums ir jāimportē formāta konfigurācija.  
4. Noklikšķiniet uz Jauns, lai izveidotu jaunu faila adresātu.
    * Ņemiet vērā, ka var izveidot vienu faila adresātu katram tāda paša formāta izvades komponentam, piemēram, mapei vai failam. Iestatījumos var atsevišķi iespējot un atspējot adresātus.  
5. Laukā Nosaukums ievadiet lietotājam draudzīgu izvades komponenta nosaukumu.
    * Ieteicams izmantot saprotamus nosaukumus, piemēram, “Maksājuma fails” vai “Kontroles pārskats”. Šie nosaukumi tiks parādīti lietotājiem konfigurācijas izpildlaikā kopā ar adresāta iestatījumiem.  
6. Sadaļā Faila nosaukums atlasiet failu vai mapi, kas ir raksturīga formātam.
7. Noklikšķiniet uz Iestatījumi.
8. Laukā Iespējots atlasiet vērtību Jā.
    * Izvēles rūtiņu Iespējot katrā cilnē iespējo un atspējo katru adresātu atsevišķi. Šajā piemērā tiks iespējota izvades faila nosūtīšana pa elektronisko pastu, kad fails tiks ģenerēts.  
9. Noklikšķiniet uz Rediģēt, lai iestatītu e-pasta adresātus.
10. Noklikšķiniet uz Pievienot.
11. Noklikšķiniet uz Drukāt pārvaldības e-pasta ziņojumu.
12. Laukā E-pasta avota veids atlasiet kādu opciju.
    * Jūs varat atlasīt citus e-pasta avotu tipus, piemēram, debitora vai kreditora tipu. Tas definē argumenta tipu, kuru atgriezīs E-pasta ziņojuma avota konta formula. E-pasta ziņojuma avota konta formulā, kas ir aprakstīta nākamajā solī, tiks piesaistīts e-pasta avots. Atlasiet Kreditors, ja jūsu formula atgriezīs kreditora kontu. Izmantojiet vienumu Debitors, ja jūs lietojat konfigurācijas piemēru ISO 20022 pārvietošana kredītā.  
13. Noklikšķiniet uz pogas Saistīt e-pasta avotu.
14. Sadaļā Formula ievadiet konkrētu dokumenta atsauci uz puses tipu, ko atlasījāt agrāk.
    * Tā vietā, lai rakstītu, jūs varat atrast datu avota mezglu, kas norāda puses kontu, un noklikšķināt uz pogas Pievienot datu avotu, lai atjauninātu formulu. Piemēram, ja izmantojat konfigurāciju ISO 20022 pārvietošana kredītā, mezgls, kas norāda kreditora kontu, ir '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID. Pretējā gadījumā ievadiet jebkuru virknes vērtību, piemēram, “DE-001”, lai saglabātu formulu.  
15. Noklikšķiniet uz Saglabāt.
16. Aizvērt lapu.
17. Noklikšķiniet uz Rediģēt, lai konfigurētu kontaktpersonas informāciju pusei.
18. Atlasiet Jā laukā Primārā kontaktpersona.
    * Jūs varat izmantot dažādas iespējas, lai norādītu, kādu puses kontaktpersonas tipu būtu jāizmanto kā e-pasta adresi šajā mērķī. Šajā piemērā mēs izmantojam primāro kontaktpersonu.  
19. Noklikšķiniet uz OK.
20. Noklikšķiniet uz OK.
21. Ierakstiet vērtību laukā Tēma.
22. Noklikšķiniet uz OK.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]