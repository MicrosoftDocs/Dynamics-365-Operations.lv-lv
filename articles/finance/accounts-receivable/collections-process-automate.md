---
title: Parādu piedziņas procesa automatizācija
description: Šajā tēmā aprakstīts, kā tiek iestatītas parādu piedziņas procesa stratēģijas, kuras automātiski nosaka klientu rēķinus, kuriem ir nepieciešams e-pasta atgādinājums, parādu piedziņa vai vēstule par parādu piedziņu, kas jānosūta klientam.
author: JodiChristiansen
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 59db852024faf457db7ac145b67619b31555aaf2
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/10/2021
ms.locfileid: "7486873"
---
# <a name="collections-process-automation"></a>Parādu piedziņas procesa automatizācija

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts parādu piedziņas procesa stratēģiju iestatīšanas process, kas automātiski identificē debitoru rēķinus, kas pieprasa e-pasta atgādinājumu, parādu piedziņas aktivitātes (piemēram, tālruņa zvanu) vai parādu piedziņas vēstuli, kas jānosūta debitoram. 

Organizācijām bieži vien paiet daudz laika, pārskatot novecojušas bilanču atskaites, klientu grāmatvedību un atvērtos rēķinus, lai uzzinātu, ar kuriem klientiem vajadzētu sazināties par atvērtu rēķinu vai konta bilanci. Šis pētījums taupa parādu piedziņas aģenta laiku, kas pavadīts sazinoties ar debitoriem, lai apkopotu nokavētās bilances vai atrisinātu strīdus par rēķiniem. Parādu piedziņas procesu automatizācija ļauj iestatīt uz stratēģiju balstītu pieeju jūsu parādu piedziņas procesam. Tas palīdz konsekventi veikt parādu piedziņas darbības, nodrošinot pielāgotus e-pasta atgādinājumus vai ieprogrammētu atgādinājuma vēstuļu sūtīšanas procesu. 

## <a name="collections-process-setup"></a>Parādu piedziņas procesa iestatīšana
Varat izmantot lapu **Parādu piedziņas procesa iestatīšana** (**Kredīts un parādu piedziņa > Iestatīšana > Parādu piedziņas procesa iestatīšana**), lai izveidotu automatizētu parādu piedziņas procesu, kas plāno aktivitātes, sūta e-pasta ziņojumus un veido un grāmato debitoru parādu piedziņas vēstules. Procesa darbības pamatā ir sākuma vai vecākais atvērtais rēķins. Katra darbība izmanto šo rēķinu, lai noteiktu, kādai saziņai vai aktivitātei ir jānotiek ar noteiktu debitoru.  

Parādu piedziņas darba grupas parasti izsūta savlaicīgu brīdinājumu saistībā ar neapmaksātu rēķinu, lai klientu informētu par to, ka drīz beigsies rēķina apmaksas termiņš. Ir iespējams iestatīt atlasi **Iepriekšēju atgādinājumu**, lai katrā procesa hierarhijā varētu katram rēķinam izpildīt vienu darbību, kad rēķina termiņš sasniedz šo darbību.

### <a name="process-hierarchy"></a>Procesa hierarhija
Katru debitoru kopu var piešķirt tikai vienai procesu hierarhijai. Šīs darbības hierarhijas rangs identificē, kurš process būs prioritārs, ja debitors ir iekļauts vairāk nekā vienā kopā, kam ir piešķirta procesu hierarhija. Kopas ID nosaka, kuri debitori tiks piešķirti procesam. Katru iestatīto hierarhiju var piešķirt tikai vienai procesa automatizācijai.

Klusās dienas tiek izmantotas, lai nodrošinātu, ka automatizētais process nesazinās ar debitoru pārāk bieži. Piemēram, ja klusās dienas ir iestatītas uz divi, tad automatizētais process nesazināsies ar debitoru vismaz divas dienas, pat ja sākotnējais sākuma rēķins ir pilnībā nokārtots. 

Lai izslēgtu debitorus no procesu automatizācijas, ja klienta vecumstruktūras bilance vai rēķina summa ir mazāka nekā definētā vērtība, laukā **Izslēgt no procesa** atlasiet **Klientu vecumstruktūras bilance mazāka par** vai **Rēķina summa mazāka par**.

Atzīmējiet **Lietot prognozi**, lai izveidotu kolekciju darbības, izmantojot Klientu maksājumu prognozes. Izveidotās aktivitātes izmantos Darbību veidni no **Maksājumu prognozēm** lapā **Debitoru parametri**, cilnē **Kolekciju procesa automatizācija**. 

### <a name="process-details"></a>Apstrādāt datus
Noklikšķiniet uz **Jauns**, lai hierarhijai pievienotu jaunus procesa datus. **Apraksts** tiek izmantots, lai noteiktu darbības mērķi vai nosaukumu hierarhijā. Atlasiet **Darbības veidu**, lai definētu darbību, kas izveidos aktivitāti, nosūtīs e-pastu vai izveidos parādu piedziņas vēstuli. 

- **Biznesa dokuments** definē veidni, kas tiek izmantota darbības veida izveidei. Dokuments būt aktivitātes veidne, e-pasta veidne vai parādu piedziņas vēstule katram debitoram. Kolekciju procesa automatizācija izveido tikai kolekcijas vēstuli katram klientam neatkarīgi no tā, ka ir iestatīti citi kolekciju parametri.
- **Kad** nosaka, vai procesa darbību, kura notiks pirms vai pēc sākuma rēķina apmaksas (vecākā) datuma, un to lieto kopā ar laukā **Dienas, kas saistītas ar rēķina apmaksas datumu** rādīto skaitu. 
- Atzīmējiet opciju **Iepriekšējs atgādinājums**, lai izveidotu darbību katram rēķinam vienā procesa hierarhijas darbībā. Iepriekšējās brīdināšanas darbības parasti ir iepriekšējs brīdinājums, kas saistīts ar neapmaksātiem rēķiniem, lai klientu varētu informēt par to, ka drīz beigsties rēķina apmaksas termiņš. Iepriekšēju brīdinājumu var atzīmēt tikai vienai katras hierarhijas darbībai. Atlasot e-pasta darbības veidu, saņēmējs tiks izmantots, lai definētu, vai tas ir debitora, pārdošanas grupas vai parādu piedziņas aģenta kontakts, uz kuru tiek sūtīts e-pasta ziņojums. 
- Vērtība laukā **Biznesa nolūka kontaktpersona** tad nosaka, kura kontaktpersona no debitora konta saņems šo paziņojumu.

### <a name="business-document-details"></a>Detalizētā informācija par biznesa dokumentu
Detalizētā informācija par biznesa dokumentu var atšķirties atkarībā no darbības veida, kas atlasīts procesa detalizētajā informācijā. Kad darbības veids ir aktivitāte, tiks parādīti aktivitātes veidnes dati. Šīs detaļas ietver aktivitātes veidnes nosaukumu, izveidotas aktivitātes veidu, aktivitātes mērķi, dienu skaitu, kas paredzētas aktivitātes pabeigšanai, un detalizētu informāciju par aktivitāti. Šī aktivitāte tad būs saistīta ar sākum rēķinu, kas informē saņēmēju par darbību, kas nepieciešama, lai pabeigtu aktivitāti.

Ja darbības veids ir e-pasta ziņojums procesa detalizētajā informācijā, šajā sadaļā būs ietvertas divas kopsavilkuma cilnes. Pirmā tiek izmantota, lai definētu veidnes ID, e-pasta aprakstu, noklusējuma valodu, lietotāja vārdu, kas tiks piešķirts automātiski nosūtītajiem e-pasta ziņojumiem, un saistīto sūtītāju e-pasta adresi. Otrā ļaus izveidot e-pasta pamattekstu, kad vērtības laukos **Valoda** un **Tēma** tiek saglabātas, atlasot **Rediģēt**. Tādējādi tiks atvērts logs, kas ļauj augšupielādēt HTML saturu. 

> [!Note]
> Outlook e-pastu var saglabāt ar vēlamo komunikācijas pamattekstu HTML formātā. Pēc tam to var augšupielādēt, lai ieviestu veidni. <br> <br> Ja ir atlasīts parādu piedziņas vēstules darbības veids, tad iestatīšanas lapā nebūs biznesa dokumentu detalizētas informācijas sadaļas.

Lietojiet pogu **Kolekciju procesa vēsture**, lai skatītu atlasītās procesa hierarhijas jaunāko vēsturi. 

Noklikšķiniet uz darbības **Kolekcijas procesa piešķīrums**, lai skatītu kolekciju procesam piešķirtos klientus. Lietojiet **Priekšskatīt klienta piešķiri**, lai skatītu hierarhiju, kurai ir piešķirts konkrēts klients. Lietojiet **Priekšskatīt procesa piešķiri**, lai priekšskatītu klientus, kuri tiks piešķirti hierarhijai, kad tā tiks palaista. Noklikšķiniet uz **Manuāla piešķire**, lai skatītu debitorus, kas ir manuāli piešķirti procesam, vai atlasiet debitorus, lai tos piešķirtu procesam.

Noklikšķiniet uz darbības **Procesa simulācija**, lai priekšskatītu darbības, kuras tiks izveidotas, ja šajā laikā tiks palaista atlasītā procesa automatizācija. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
