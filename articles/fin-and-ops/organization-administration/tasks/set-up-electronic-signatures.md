--- 
title: "Elektronisko parakstu iestatīšana"
description: "Izmantojiet šo procedūru, lai iestatītu elektroniskos parakstus."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 11fee0b2358e6a2b84c221f8eb06e32c888e5f44
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-electronic-signatures"></a>Elektronisko parakstu iestatīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Izmantojiet šo procedūru, lai iestatītu elektroniskos parakstus. Elektroniskais paraksts apstiprina personas identitāti, kas gatavojas sākt vai apstiprināt skaitļošanas procesu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DAT.


## <a name="enable-the-electronic-signature-configuration-key"></a>Elektroniskā paraksta konfigurācijas atslēgas iespējošana
1. Pārejiet uz sadaļu Sistēmas administrēšana > Iestatījumi > Licences konfigurācija.
2. Kokā izvērsiet sadaļu “Administrēšana”.
    * Pārbaudiet, vai izvēles rūtiņa Elektroniskais paraksts ir atzīmēta.  
    * Ja izvēles rūtiņa Elektroniskais paraksts nav atzīmēta, jums ir jāiespējo uzturēšanas režīms. Uzturēšanas režīmu šajā vidē var iespējot, palaižot uzturēšanas darbu no Lifecycle Services vai lokāli izmantojot rīku Deployment.Setup.  
3. Aizvērt lapu.

## <a name="set-up-electronic-signature-parameters"></a>Elektronisko parakstu parametru iestatīšana
1. Pārejiet uz sadaļu Organizācijas administrēšana > Iestatījumi > Elektroniskais paraksts > Elektroniskā paraksta parametri.
2. Noklikšķiniet uz Rediģēt.
3. Laukā Paziņojums ierakstiet vērtību.
    * Ievadiet paziņojumu, ko parakstītāji saņem, kad tiek pieprasīts paraksts. Var ievadīt jebkādu tekstu. Parasti šis teksts parāda lietotājiem, ko nozīmē elektroniska dokumenta parakstīšana.  
    * Ja vēlaties ievadīt paziņojuma tekstu papildu valodās, noklikšķiniet uz pogas Tulkojumi.  
4. Noklikšķiniet uz Saglabāt.
5. Aizvērt lapu.

## <a name="set-up-reason-codes-for-electronic-signatures"></a>Pamatojuma kodu iestatīšana elektroniskajiem parakstiem
1. Pārejiet uz sadaļu Organizācijas administrēšana > Iestatījumi > Elektroniskais paraksts > Elektroniskā paraksta pamatojuma kodi.
2. Noklikšķiniet uz Jauns.
    * Jums jāiestata pamatojuma kodi, pirms izmantojat elektroniskos parakstus. Parakstot dokumentu, nepieciešams derīgs pamatojuma kods.     Parakstītājs atlasa pamatojuma kodu, lai norādītu elektroniskā paraksta mērķi. Piemēram, pamatojuma kodu var izmantot, lai norādītu uz juridisku apstiprinājumu.  
3. Laukā Pamatojuma kods ierakstiet vērtību.
4. Apraksta laukā ierakstiet vērtību.
    * Ja nepieciešams, ievadiet papildu pamatojuma kodus.  
5. Noklikšķiniet uz Saglabāt.
6. Aizvērt lapu.

## <a name="require-electronic-signatures-for-existing-processes"></a>Elektronisko parakstu pieprasīšana esošajiem procesiem
1. Pārejiet uz sadaļu Organizācijas administrēšana > Iestatījumi > Elektroniskais paraksts > Elektroniskā paraksta prasības.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet procesu, kam nepieciešami elektroniskie paraksti.  
3. Atlasiet vai notīriet izvēles rūtiņu Nepieciešamais paraksts.
    * Atkārtojiet šīs darbības katram procesam, kas prasa elektronisko parakstu.  
4. Noklikšķiniet uz Saglabāt.

## <a name="create-a-custom-requirement-for-electronic-signatures"></a>Pielāgoto elektronisko parakstu prasību izveidošana
1. Noklikšķiniet uz Jauns.
2. Atlasiet vai notīriet izvēles rūtiņu Nepieciešamais paraksts.
3. Laukā Nosaukums ievadiet procesa nosaukumu, kuram nepieciešami elektroniskie paraksti.
4. Laukā Tabulas nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet tabulu, kur saglabāti parakstāmie dati.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Laukā Lauka nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Sarakstā atrodiet un atlasiet tabulas lauku, ko vēlaties uzraudzīt.
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Norādiet, kad pieprasīt parakstus.     Atlasiet Vienmēr, ja paraksts ir nepieciešams katru reizi, kad mainās laukā esošie dati.     Atlasiet Tikai, ja paraksts ir nepieciešams tikai noteiktos apstākļos. Ja atlasāt Tikai, jāatlasa arī viena no šīm opcijām: Ja ir ievietots ieraksts, Kad tiek atjaunināts ieraksts vai Kad ieraksts tiek dzēsts.  
10. Noklikšķiniet uz Saglabāt.
11. Aizvērt lapu.


