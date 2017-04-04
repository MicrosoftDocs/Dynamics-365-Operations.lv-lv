---
title: "Avansa turētāji"
description: "Uzziniet par avansa turētāja funkcionalitāti Microsoft Dynamics 365 operācijām."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262574
ms.assetid: 87924785-6032-4125-8279-5b1a758f4d80
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 8cfe98e3859778e4fdc61f22b437cb1b4d004549
ms.lasthandoff: 03/31/2017


---

# <a name="advance-holders"></a>Avansa turētāji

Uzziniet par avansa turētāja funkcionalitāti Microsoft Dynamics 365 operācijām.

*Avansa turētāja* ir darbinieks, uzņēmums, kurš ir atbildīgs par izdevumu summa, ko nodrošina organizācija. Tikai uzņēmuma darbinieks var būt avansa turētāja. Kad notiek iepirkumu, avansa turētāja ziņo uzņēmumam par izdevumiem, kas tika veikti. Uzņēmums pilsonības darbinieks atmaksā par izdevumu summu. Uzņēmums kontrolē līdzsvaru attiecībā uz katra avansa turētāja. Lietotāji juridiskām vienībām, Igaunija, Latvija, Lietuva, Polija, Čehijas Republiku, Ungāriju un Krievija var atspoguļot konkrētas darbības, kas pavada darbības ar uzņēmuma darbiniekus, kuri ir atbildīgi par izdevumu summa, ko nodrošina organizācija.

## <a name="set-up-an-advance-holder"></a>Izveidot avansa turētāja
Lai iestatītu avansa turētāja, jāpabeidz secībā šādus uzdevumus.
1.  Avansa turētāju grupas izveide.
2.  Iestatītu darbinieku grāmatošanas metodi.
3.  Iestatiet kontu kreditoru parametrus.
4.  Izveidot īpašus nosacījumus maksājumu avansa turētāja.
5.  Izveidot avansa turētāja.

### <a name="advance-holder-groups"></a>Avansa turētāju grupas

Izmantojiet **avansa turētāju grupas** lapu, lai izveidotu avansa turētāju grupas. Varat norādīt nosaukumu, aprakstu un avansa turētāju grupas korespondējošais konts.
### <a name="employee-posting-profile"></a>Darbinieku grāmatošanas metode

Izmantojiet **darbinieka grāmatošanas metodes** lapu, lai izveidotu avansa turētāja darbības profilu. Var norādīt šādu informāciju par darbinieka grāmatošanas metodi.
|Lauks |apraksts|
|------|-----------|
|Grāmatošanas metode|Ievadīt avansa turētāja identifikācijas kodu grāmatošanas profilā.|
|apraksts|Ievadiet grāmatošanas metodei īsu aprakstu.|
|Derīgs|Atlasiet vienu no šīm opcijām grupējumu grāmatošanas profilu iestatīšana līmenim: 
**Galda** -šī opcija tiek izmantota, lai iestatītu grāmatošanas metodes vienu avansa turētāja. Avansa turētāja kods ir norādīts laukā atsauce ir jānorāda.
**Grupas** -šī opcija tiek izmantota, lai iestatītu grāmatošanas metodes avansa turētāju grupas. Ir jānorāda grupas kods ir norādīts laukā atsauce.
**Visas** -šī opcija tiek izmantota, lai iestatītu grāmatošanas metodi visiem avansa turētāji. | | Atsauce | Avansa turētāja kods atlasiet, ja derīga laukam tiek atlasīta tabula, vai atlasiet avansa turētāju grupas, ja grupa atlasīta laukā derīgs. | | Summu konts | Atlasiet kopsavilkuma konts transakciju grāmatošanai. |



### <a name="account-payable-parameters"></a>Kreditoru moduļa parametri

Atspoguļojot avansa turētāja darbības ir jāuzstāda šādas darbības ar **konts kreditoru parametrus** lapu **avansa turētāji** sadaļu.
|                                                |                   |
|------------------------------------------------|-------------------|
|  **Field**                                     | **Description**                                                                                                                                                                  |
| **Posting profile**                            | Atlasiet noklusēto profilu, lai pabeigtu darījumu avansa turētāji.                                                                                                         |
| **Advance holder sorting**                     | Ja atlasīts, avansa turētāji tiks rādīts saraksta sākumā **avansa turētāji** lapā.                                                                     |
| **Issue when balance is open**                 | Ja atlasīts, drīkstēs jautājumu par avansu līdz avansa turētāja, kuram ir atvērts pozitīva bilance.                                                                      |
| **Bilances slēgšanas caur naudas lauku grupā pārdošanas pasūtījums: nosaukums** | Izvēlieties kases kvīts žurnāla kods. Šo žurnālu kodu lieto, lai ģenerētu kases izdevumu orderi un ieņēmumu orderi, slēdzot avansa turētāja bilances caur kases. |
| **Cash**                                       | Izvēlieties kases kontu, noteikt dokumentus, kas tiek izmantoti slēguma bilances avansa turētāja.                                                                 |
| **Caur banku lauku grupas noslēguma bilance: nosaukums** | Atlasiet žurnāla kods darījumus slēgt caur banku bilancēm.                                                                                                   |
| **Account type**                               | Atlasiet banku slēgt avansa turētāja caur banku bilancēm.                                                                                                        |
| **Main account**                               | Atlasiet bankas kontu kodu slēgt avansa turētāja caur banku bilancēm.                                                                                           |

### <a name="terms-of-payment-for-advance-holder"></a>Avansa turētāja maksāšanas

Lai pareizi reģistrēt un grāmatotu pirkšanas pasūtījumu, izmantojot avansa turētāja, jāizmanto maksāšanas termiņus, kas tika izveidota ar **no avansa turētāja** iestatīta opcija **patieso**.
### <a name="create-an-advance-holder-creation"></a>Izveidot avansa turētāja izveide

Pirms var izveidot avansa turētāja, jābūt jau uzstādītām darba ņēmējiem. Lai iegūtu papildinformāciju, skatiet [ievadiet darbinieku informēšana (uzdevuma norādījumi).](http://ax.help.dynamics.com/en/wiki/enter-worker-information/) Izmantojiet **avansa turētāji** lapu, lai uzstādītu darba ņēmējs kā avansa turētāja. Darba ņēmējs, lai izmantotu kā avansa turētāja, noklikšķiniet uz atlasīt **rediģēt**, un pēc tam iestatiet **avansa turētāja** iespēju **True**. Jums jāaizpilda šādi lauki.
|                |                                                                                             |
|----------------|---------------------------------------------------------------------------------------------|
| **Field**      | **Description**                                                                             |
| **Group**      | Avansa turētāju grupas atlasiet.                                                             |
| **Series**     | Ievadiet virkni dokumentu, kas tiek izmantots, lai pārbaudītu avansa turētāja identitāti. |
| **Number**     | Ievadiet tā dokumenta numuru, ko izmanto, lai pārbaudītu avansa turētāja identitāti. |
| **Issue date** | Atlasiet vai ievadiet dokumenta izdošanas datuma.                                                    |
| **Issued by**  | Ievadiet informāciju par iestādi vai personu, kas izdeva dokumentu.                       |

## <a name="advance-holder-inquiries-and-reports"></a>Avansa turētāja uzziņās un pārskatos
### <a name="advance-holder-transactions-inquiry"></a>Avansa turētāja darbības izmeklēšanu

Avansa turētāja darbību sarakstu, noklikšķiniet uz **darbības** pogu **avansa turētāji** lapā. Lai redzētu darbības visām avansa turētāji vai izveidot īpašu izmeklēšanas pamatā avansa turētāju darbības, noklikšķiniet uz **kreditoru parādi**&gt;**uzziņās un pārskatos**&gt;**avansa turētāji uzziņās un pārskatos**&gt; darījumiem. Noklikšķiniet uz **dokumentu** atvērt **dokumenta darbības** lapā.
### <a name="advance-holder-balance-inquiry"></a>Avansa turētāja bilance izmeklēšana

Redzēt bilanci avansa turētāja izmantot **avansa turētāji** lapā. Lai redzētu līdzsvaru visiem avansa turētāji vai izveidot īpašu izmeklēšanu, pamatojoties uz avansa turētāji kontus, noklikšķiniet uz **kreditoru parādi**&gt;**uzziņās un pārskatos**&gt;**avansa turētāji uzziņās un pārskatos**&gt;**līdzsvaru.**
### <a name="advance-holder-balance-report"></a>Avansa turētāja bilances pārskats

Priekšskatīt un izdrukāt atskaiti, kas balstīta uz informāciju par avansa turētāji atlikumu, noklikšķiniet uz **kreditoru parādi**&gt;**uzziņās un pārskatos**&gt;**avansa turētāji uzziņās un pārskatos**&gt;**avansa turētāja bilances pārskatu**.
### <a name="advance-holder-transactions-report"></a>Avansa turētāja transakciju pārskats

Priekšskatīt un izdrukāt atskaiti, kas balstīta uz avansa turētāju darbības, noklikšķiniet uz **kreditoru parādi**&gt;**uzziņās un pārskatos**&gt;**avansa turētāji uzziņās un pārskatos**&gt;**avansa turētāja darbības pārskatu**.



<a name="see-also"></a>Skatiet arī
--------

[Advance holder transactions](emea-advance-holders-transactions.md)


