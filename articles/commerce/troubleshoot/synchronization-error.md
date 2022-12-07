---
title: Asinhronās pasūtījumu sinhronizācijas problēmas
description: Šajā rakstā ir sniegti asinhronas pasūtījumu Microsoft Dynamics 365 Commerce izveides kļūmes kopējie iemesli, kā arī sniegti traucējummeklēšanas soļi, lai sistēmas lietotāji un partneri saprastu, kas radās nepareizi.
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815761"
---
# <a name="asynchronous-order-synchronization-issues"></a>Asinhronās pasūtījumu sinhronizācijas problēmas

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti asinhronas pasūtījumu Microsoft Dynamics 365 Commerce izveides kļūmes kopējie iemesli, kā arī sniegti traucējummeklēšanas soļi, lai sistēmas lietotāji un partneri saprastu, kas radās nepareizi.

## <a name="symptom"></a>Simptoms

Asinhroni pasūtījumi, kas tiek izveidoti Dynamics 365 Commerce no e-commerce vai pārdošanas punkta (POS), netiek atspoguļoti programmā Commerce Headquarters.

## <a name="troubleshooting"></a>Problēmu novēršana

Pasūtījuma izveide galvenajā birojā var neizdoties dažādu iemeslu dēļ atkarībā no stadijas, kurā pasūtījuma izveides process neizdodas. Šīs traucējummeklēšanas darbības iziet cauri iespējamajiem saknes iemesliem.

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>Pārbaudīt, vai ar asinhrono pasūtījumu saistītā transakcija ir sasniegusi galveno biroju

E-komercijas pasūtījumiem galvenajā birojā dodieties uz sadaļu **Mazumtirdzniecības un Commerce \> uzziņas un pārskati par \> interneta veikala darbībām**. Ja pasūtījumam ir apstiprinājuma numurs, filtrējiet darbības, ievadot apstiprinājuma numuru kanāla **atsauces ID** laukā. Ja apstiprinājuma numurs nav norādīts, filtrējiet darbības, ievadot debitora konta numuru.

Sistēmā POS pasūtījumi atveriet lapu **Veikala** darbības un filtrējiet ierakstus pēc kvīts numura vai debitora konta numura. Ja nav atrasta transakcija, palaidiet **P-0001 kanāla** transakciju darbu, kas sinhronizē darbības no kanāliem uz galveno biroju. Ja P-0001 **darbs neizdodas**, atveriet atbalsta biļeti darba kļūmei. Ja P-0001 **darbs** ir veiksmīgs, bet darbības joprojām neparādās galvenajā birojā, atveriet atbalsta biļeti, kurā ietverta atbilstošā informācija.
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>Pārbaudīt sinhronizācijas statusu, ja darbība atrodas galvenajā birojā, bet nav saistīta ar pārdošanas pasūtījumu.

Ja darbība atrodas galvenajā birojā, bet pārdošanas pasūtījums nav izveidots, **atveriet lapu Tiešsaistes veikala darbības**  **un atlasiet kopsavilkuma cilni Sinhronizācijas** statuss. Ja Sinhronizēšanas **pasūtījumu** darbs mēģināja sinhronizēt šo transakciju, **laukam** Gaidošs pasūtījuma statuss jābūt ar statusu Izdevās **vai** Neizdevās **·**. Ja statuss ir **Veiksmīgs**, šajā darbībā jābūt pārdošanas pasūtījuma laukam. Ja statuss ir **Neizdevās**, detalizētu informāciju par kļūdu var skatīt **detalizētas informācijas par pasūtījumu**  **laukā kopsavilkuma cilnē Sinhronizācijas** statuss. Ja netiek rādīts neviens no šiem statusiem, nav veikts mēģinājums apstrādāt darbību. Šādā gadījumā, lai palaistu **sinhronizācijas** darbu, lapas augšpusē var atlasīt Sinhronizēt pasūtījumu.

Nodrošiniet, lai **pasūtījumu sinhronizēšanas** darbs tiktu ieplānots periodiskai izpildei, tādējādi asinhronās darbības var izveidot kā pasūtījumus galvenajā birojā.

Šajās sadaļās sniegta informācija par dažām parastām kļūdām un to ieteiktajiem labojumiem.

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>Pasūtījuma kļūdas informācijas lauks rāda šādu kļūdas ziņojumu: "Numuru sērija ir pārsniegta"

Numuru sērijas tiek izmantotas, lai izveidotu pārdošanas pasūtījumus galvenajā birojā. Ja visi numuru sērijai atļautie numuri ir saplūduši, sistēma ģenerē šo kļūdas ziņojumu. Numuru sēriju, kas tiek izmantota pārdošanas pasūtījumu veidojiet, var atrast debitoru **parādu parametru numuru \> sērijās \> Pārdošanas pasūtījumā**. Lai novērstu šo kļūdu, novērsiet esošo numuru sēriju vai aizstājiet to ar jaunu numuru sēriju.

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>Pasūtījuma kļūdas informācijas lauks rāda šādu kļūdas ziņojumu: "Lai apstrādātu kredītkaršu darījumus, jābūt noklusējuma maksājumu pakalpojumam.

Lai novērstu šo kļūdu, apstipriniet, ka galvenais birojs ir definēts noklusējuma maksājums. Ja noklusējuma maksājums nav definēts, tas ir jādefinē. Dodieties uz **debitoru \> parādu maksājumu iestatīšanas \>** maksājumu pakalpojumiem un nodrošiniet **, lai noklusējuma procesors**  **jaunām** kredītkartēm opcijai vienam maksājumu pakalpojumam būtu iestatīts uz Jā.
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>Pasūtījuma kļūdas detalizētās informācijas lauks rāda konta struktūras kļūdas ziņojumu

Konta struktūras kļūdas ziņojuma teksts var mainīties, kā redzams tālākajos piemēros. Tomēr kļūdām ir kopīgs saknes iemesls, kas saistīts ar konta struktūras konfigurāciju.

- "Grāmatošanas rezultāti žurnāla pakešuzdevuma numuram 0009656328 dokumenta ARP-000959899 1,00 dokumenta ARP-000959899 uzņēmuma usrt tiks grāmatoti kā pārmaksa vai nepilna samaksa"
- "Grāmatošanas rezultāti žurnāla partijas numuram 0009656328 dokumenta ARP-000959899 dokumenta ARP-000959901 konta struktūra kombinācijai 618160 nav derīgi Virsgrāmatas korporatīvajam galvenajam kontam Koplietots"
- "Grāmatošanas rezultāti žurnāla pakešuzdevuma numuram 0009656328 Dokumenta ARP-000959899 dokumentsARP-000959901 ziņots no uzņēmuma kontu usrt"
- "Grāmatošanas rezultāti žurnāla pakešuzdevuma numuram 0009656328 dokumentsARP-000959899 grāmatošana atcelta"
    
Lai novērstu šīs kļūdas, pārskatiet konta struktūras precizitāti. Papildinformāciju skatiet konta [struktūru konfigurēšana](/dynamics365/finance/general-ledger/configure-account-structures).
    
Kad kļūda ir novērsta, atlasiet neizdevušos darbību un **pēc** tam atlasiet Sinhronizēt pasūtījumu lapas augšpusē, lai palaistu sinhronizācijas darbu.
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>Citu veidu kļūdas, kuru dēļ, iespējams, nepieciešami darbības datu labošanai

Lai labotu cita veida kļūdas, kas var pieprasīt, lai darbības dati tiktu fiksēti, varat izmantot iespēju "rediģēt un audita darbības". Papildinformāciju skatiet labošanas [un audita darbības](../edit-order-trans.md).
