---
title: Parādu piedziņas procesa automatizācija
description: Šajā tēmā aprakstīts parādu piedziņas procesa stratēģiju iestatīšanas process, kas automātiski identificē debitoru rēķinus, kas pieprasa e-pasta atgādinājumu, parādu piedziņas aktivitātes (piemēram, tālruņa zvanu) vai parādu piedziņas vēstuli, kas jānosūta debitoram.
author: panolte
manager: AnnBe
ms.date: 08/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: a63058904df72a7fda5a67ed1e6a846eed393ce0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969705"
---
# <a name="collections-process-automation"></a>Parādu piedziņas procesa automatizācija

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts parādu piedziņas procesa stratēģiju iestatīšanas process, kas automātiski identificē debitoru rēķinus, kas pieprasa e-pasta atgādinājumu, parādu piedziņas aktivitātes (piemēram, tālruņa zvanu) vai parādu piedziņas vēstuli, kas jānosūta debitoram. 

Uzņēmumi pavada ievērojamu laiku, pētot vecus bilances pārskatus, klientu kontus un atvērtos rēķinus, lai noteiktu, ar kuriem klientiem jāsazinās par atvērtu rēķinu vai konta bilanci. Šis pētījums taupa parādu piedziņas aģenta laiku, kas pavadīts sazinoties ar debitoriem, lai apkopotu nokavētās bilances vai atrisinātu strīdus par rēķiniem. Parādu piedziņas procesu automatizācija ļauj iestatīt uz stratēģiju balstītu pieeju jūsu parādu piedziņas procesam. Tas palīdz konsekventi veikt parādu piedziņas darbības, nodrošinot pielāgotus e-pasta atgādinājumus vai ieprogrammētu atgādinājuma vēstuļu sūtīšanas procesu. 

## <a name="collections-process-setup"></a>Parādu piedziņas procesa iestatīšana
Varat izmantot lapu **Parādu piedziņas procesa iestatīšana** (**Kredīts un parādu piedziņa > Iestatīšana > Parādu piedziņas procesa iestatīšana**), lai izveidotu automatizētu parādu piedziņas procesu, kas plāno aktivitātes, sūta e-pasta ziņojumus un veido un grāmato debitoru parādu piedziņas vēstules. Procesa darbības pamatā ir sākuma vai vecākais atvērtais rēķins. Katra darbība izmanto šo rēķinu, lai noteiktu, kādai saziņai vai aktivitātei ir jānotiek ar noteiktu debitoru.  

### <a name="process-hierarchy"></a>Procesa hierarhija
Katru debitoru kopu var piešķirt tikai vienai procesu hierarhijai. Šīs darbības hierarhijas rangs identificē, kurš process būs prioritārs, ja debitors ir iekļauts vairāk nekā vienā kopā, kam ir piešķirta procesu hierarhija. Kopas ID nosaka, kuri debitori tiks piešķirti procesam. 

Klusās dienas tiek izmantotas, lai nodrošinātu, ka automatizētais process nesazinās ar debitoru pārāk bieži.  Piemēram, ja klusās dienas ir iestatītas uz divi, tad automatizētais process nesazināsies ar debitoru vismaz divas dienas, pat ja sākotnējais sākuma rēķins ir pilnībā nokārtots. 

Lai izslēgtu debitorus no procesu automatizācijas, ja konta bilance vai rēķina bilance ir mazāka nekā definētā vērtība, iestatiet lauku **Izslēgt no procesa** uz **Jā** un ievadiet summas vērtību.

## <a name="process-details"></a>Apstrādāt datus
**Apraksts** tiek izmantots, lai noteiktu darbības mērķi vai nosaukumu hierarhijā.

**Darbības veids** definē, vai šī darbība izveidos aktivitāti, nosūtīs e-pastu vai izveidos parādu piedziņas vēstuli.

**Biznesa dokuments** definē veidni, kas tiek izmantota darbības veida izveidei.  Tas var būt aktivitātes veidne, e-pasta veidne vai parādu piedziņas vēstule katram debitoram. 

Darbību veidus var izveidot vai nu pirms, vai pēc rēķina apmaksas datuma, pamatojoties uz iestatījumiem, kas tiek parādīti kolonnā **Dienās saistībā ar rēķina apmaksas datumu** .

Atlasot e-pasta darbības veidu, saņēmējs tiks izmantots, lai definētu, vai tas ir debitora, pārdošanas grupas vai parādu piedziņas aģenta kontakts. Vērtība laukā **Biznesa nolūka kontaktpersona** tad nosaka, kura kontaktpersona no debitora konta saņems šo paziņojumu.

## <a name="business-document-details"></a>Detalizētā informācija par biznesa dokumentu
Detalizētā informācija par biznesa dokumentu var atšķirties atkarībā no darbības veida, kas atlasīts procesa detalizētajā informācijā.  Kad darbības veids ir aktivitāte, tiks parādīti aktivitātes veidnes dati.  Šīs detaļas ietver aktivitātes veidnes nosaukumu, izveidotas aktivitātes veidu, aktivitātes mērķi, dienu skaitu, kas paredzētas aktivitātes pabeigšanai, un detalizētu informāciju par aktivitāti.  Šī aktivitāte tad būs saistīta ar sākum rēķinu, kas informē saņēmēju par darbību, kas nepieciešama, lai pabeigtu aktivitāti.

Ja darbības veids ir e-pasta ziņojums procesa detalizētajā informācijā, šajā sadaļā būs ietvertas divas kopsavilkuma cilnes.  Pirmā tiek izmantota, lai definētu veidnes ID, e-pasta aprakstu, noklusējuma valodu, lietotāja vārdu, kas tiks piešķirts automātiski nosūtītajiem e-pasta ziņojumiem, un saistīto sūtītāju e-pasta adresi. Otrā ļaus izveidot e-pasta pamattekstu, kad vērtības laukos **Valoda** un **Tēma** tiek saglabātas, atlasot **Rediģēt**.  Tādējādi tiks atvērts logs, kas ļauj augšupielādēt HTML saturu. Varat arī ierakstīt ziņojumu, kas izveidots manuāli loga apakšējā kreisajā lodziņā.  

> [!Note]
> Outlook e-pastu var saglabāt ar vēlamo komunikācijas pamattekstu HTML formātā. Pēc tam to var augšupielādēt, lai ieviestu veidni. <br> <br> Ja ir atlasīts parādu piedziņas vēstules darbības veids, tad iestatīšanas veidlapā nebūs biznesa dokumentu detalizētas informācijas sadaļas.


## <a name="fasttab-reference"></a>Kopsavilkuma cilnes atsauce
Šajās tabulās ir uzskaitītas lapas un lauki, kuriem var piekļūt no norādītajām kopsavilkuma cilnēm, kā arī šīs cilnes informācijas apraksts. 

### <a name="process-hierarchy"></a>Procesa hierarhija

|     Lapa                                                  |     Lauks                         |     Apraksts                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     Parādu piedziņas procesa iestatīšana <br> Procesu automatizācija       |                                   |     Izveidot un pārvaldīt parādu piedziņas procesus, pamatojoties uz debitoru kopas piešķirēm.                                                                                                                             |
|     Parādu piedziņas procesa iestatīšana <br> Procesu automatizācija       |     Hierarhija                     |     Nosaka procesu automatizācijas prioritāti, lai piešķirtu debitoru, ja tie pieder vairākām kopām.                                                                                                   |
|     Parādu piedziņas procesa iestatīšana <br> Procesu automatizācija       |     Kopas ID                       |     Vaicājumi, kas nosaka debitoru ierakstu grupu.                                                                                                                                                        |
|     Parādu piedziņas procesa iestatīšana <br> Procesu automatizācija       |     Klusās dienas                    |     Ierobežojiet, cik bieži var izpildīt procesa darbību. Piemēram, ja tiek iestatītas divas klusas dienas, nākamā procesa darbība nenotiks vismaz divas dienas, ja sākuma rēķins mainīsies.     |
|     Parādu piedziņas procesa iestatīšana <br> Procesu automatizācija       |     Izslēgt no Procesa        |     Atlasot **Debitora vecuma bilance, kas mazāka par** vai **Rēķina summa, kas mazāka par** , debitors tiek izslēgts no procesa automatizācijas, ja vērtības kritērijs nav ievērots.                                   |

### <a name="process-details"></a>Apstrādāt datus
|     Lapa                                                  |     Lauks                                         |      Apraksts                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     Parādu piedziņas procesa iestatīšana <br> Procesu automatizācija       |                                                   |     Definējiet darbības, kas veiktas, pamatojoties uz sākuma rēķinu.                                                                                                |
|                                                           |     Apraksts                                   |     Brīvā teksta lauks, ko izmanto, lai norādītu darbības nosaukumu un/vai aprakstu.                                                                           |
|                                                           |     Darbības tips                                   |     Aktivitāte, e-pasts vai parādu piedziņas vēstule, kas tiks izveidota ar procesa darbību.                                                                     |
|                                                           |     Biznesa dokuments                           |     Definē aktivitāti vai e-pasta veidni, kas tiek izmantota procesa darbības laikā.                                                                        |
|                                                           |     Kad                                          |     Nosaka, vai procesa darbība notiks pirms vai pēc sākuma rēķina apmaksas datuma kopā ar lauku **Dienas, kas saistītas ar rēķina apmaksas datumu** .        |
|                                                           |     Dienas attiecībā pret rēķina samaksas termiņu        |     Kopā ar lauku **Kad** tas identificē procesa darbības hronometrāžu.                                                                          |
|                                                           |     Saņēmējs                                     |     Norāda, vai e-pasta ziņojums tiks nosūtīts debitoram, pārdošanas grupai vai parādu piedziņas aģenta kontaktpersonai.                                                   |
|                                                           |     Biznesa nolūka kontaktpersona                    |     Nosaka, kura saņēmēja e-pasta adrese tiek izmantota e-pasta komunikācijā.                                                                                 |

### <a name="business-process-activity-template-details"></a>Biznesa procesu aktivitātes veidnes detalizēta informācija 
|     Lapa                                                  |     Lauks                     |      Apraksts                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     Parādu piedziņas procesa iestatīšana <br> Procesu automatizācija       |                               |     Iestatīšanas procesa sadaļa, kas identificē aktivitātes veidnes detalizēto informāciju.                                                                      |
|     Parādu piedziņas procesa iestatīšana <br> Procesu automatizācija       |     Aktivitātes veidne       |     Norāda veidu, nolūku, dienu skaitu, ko pabeigt, un sniedz detalizētu informāciju par aktivitāti, kas tiks izveidota aktivitātes procesa darbības laikā.       |

### <a name="business-document-email-template-details"></a>Detalizēta informācija par biznesa dokumenta e-pasta veidni 
|     Lapa                                                  |     Lauks     |      Apraksts                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     Parādu piedziņas procesa iestatīšana <br> Procesu automatizācija       |               |     Identificē e-pasta aprakstu, noklusējuma valodu, sūtītāja vārdu un e-pasta adresi, kas tiks izveidota e-pasta procesa darbības laikā.        |


### <a name="collections-history"></a>Iekasēšanas vēsture 
|     Lapa                              |     Lauks     |      Apraksts                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     Parādu piedziņas procesa iestatīšana       |               |     Aplūkojiet atlasītās procesu hierarhijas neseno vēsturi.     |

### <a name="collection-process-assignment"></a>Parādu piedziņas procesa piešķire
|     Lapa                              |     Lauks     |      Apraksts                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     Parādu piedziņas procesa iestatīšana       |               |     Skatīt debitorus, kas piešķirti parādu piedziņas procesam.  
|     Manuāla piešķire               |               |     Skatiet debitorus, kas ir manuāli piešķirti procesam, vai atlasiet debitorus, lai tos piešķirtu procesam. |
|     Priekšskatījuma procesa piešķire      |               |     Priekšskatiet debitorus, kas tiks piešķirti stratēģijai, kad tā tiek palaista.   |
|     Priekšskatīt debitora piešķiri     |               |     Skatiet stratēģiju, kas piešķirta noteiktam debitoram.    |
 
### <a name="parameters"></a>Parametri
|     Lapa                                                                  |     Lauks                                             |      Apraksts                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     Debitoru parametri > Parādu piedziņas procesu automatizācija     |     Debitoru procentuālā attiecība katrā partijas uzdevumā          |     Iestatījumi, lai noteiktu pakešveida uzdevumu skaitu vienā automatizācijas procesā.                                          |
|     Debitoru parametri > Parādu piedziņas procesu automatizācija     |     Automātiski grāmatot parādu piedziņas vēstules           |     Parādu piedziņas vēstules darbības veidi iegrāmatos vēstuli automatizācijas laikā.                                      |
|     Debitoru parametri > Parādu piedziņas procesu automatizācija     |     Aktivitāšu izveide automātizācijai                |     Izveidojiet un aizveriet aktivitātes darbību veidiem, kas nav saistīti ar aktivitātēm, lai skatītu visas automatizētās darbības, kas veikti kontā.        |
|     Debitoru parametri > Parādu piedziņas procesu automatizācija     |     Dienas, lai saglabātu parādu piedziņas procesu automatizāciju     |     Nosaka parādu piedziņas vēstures glabāšanas dienu skaitu.                                                       |
