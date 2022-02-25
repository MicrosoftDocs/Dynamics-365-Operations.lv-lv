---
title: Pārvaldīt B2B biznesa partnerus, izmantojot debitoru hierarhijas
description: Šajā tēmā ir aprakstīts, kā izmantot debitoru hierarhijas Microsoft Dynamics 365 Commerce, lai pārvaldītu biznesa partnerus "bizness-biznesam" e-komercijas vietnēm.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6e594cbb824a8b823912118e99b819585adc45e
ms.sourcegitcommit: 8bcb9c13eccb14e61c39ca6578d135b64090fad2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2022
ms.locfileid: "8313845"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>Pārvaldīt B2B biznesa partnerus, izmantojot debitoru hierarhijas

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izmantot debitoru hierarhijas Microsoft Dynamics 365 Commerce, lai pārvaldītu biznesa partnerus "bizness-biznesam" e-komercijas vietnēm.

Programmā Commerce headquarters debitora hierarhijas *entītija* tiek izmantota, lai pārstāvētu biznesa partnera organizācijas, kas izmantos jūsu B2B e-komercijas vietni. Pirms varat sākt izmantot debitoru hierarhijas, lai pārvaldītu biznesa partnerus, ir jāiespējo B2B e-komercijas iespējas programmā Commerce Headquarters un pēc tam jādefinē debitoru hierarhijas numuru sērija.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>Iespējot B2B e-commerce līdzekli programmā Commerce Headquarters

Lai izmantotu B2B e-komercijas iespējas, **vispirms ir jāiespējo B2B e-komercijas iespēju** izmantošana programmā Commerce Headquarters.

1. Dodieties uz **Darbvietas \> Līdzekļu pārvaldība**.
1. Cilnē Visi **izmantojiet** filtra lodziņu, lai meklētu moduli **: Mazumtirdzniecība un Komercija**.
1. Atrodiet iespēju **Iespējot B2B e-komercijas** iespēju lietošanu, **atlasiet** to un pēc tam apakšējā labajā stūrī atlasiet Iespējot tūlīt.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>Definēt numuru sēriju debitoru hierarhijai

Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus identifikatorus pamatdatu ierakstiem un transakciju ierakstiem, kam ir nepieciešami identifikatori. Jādefinē numuru sērija, kas tiks izmantota debitoru hierarhijas ID ģenerēšanas laikā. Papildinformāciju par numuru sērijām skatiet nodaļā [Numuru sēriju pārskats](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Lai definētu numuru sēriju debitoru hierarhijai programmā Commerce Headquarters, sekojiet šiem soļiem.

1. Pārejiet uz **sadaļu Mazumtirdzniecības un \> Commerce \> Headquarters iestatīšanas numuru sērijas \> Numuru sērijas**.
1. Izveidojiet jaunu numuru sēriju vai atlasiet esošu numuru sēriju tās atkārtotai izmantošanai.
1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**.
1. Cilnē Numuru **sērijas pievienojiet iepriekš izveidoto vai atlasīto numuru sēriju debitoru hierarhijas** **ID atsaucei**.

![Numuru sērija, kas pievienota debitora hierarhijas ID atsaucei.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>Kā darbojas apstiprināšanas process

Kad biznesa partneris pieprasa pievienoties B2B e-komercijas vietnei, sistēma saglabā pieprasījumu kā potenciālo *klientu*. Commerce headquarters persona, piemēram, mazumtirdzniecības operāciju pārvaldnieks, var apstiprināt vai noraidīt partnera pieprasījumus. Papildinformāciju par to, kā pārvaldīt biznesa partnera pieprasījumus un potenciālo klientu apstiprinājumus, [skatiet sadaļā Biznesa partnera lietotāju pārvaldība B2B e-komercijas vietnēs](manage-b2b-users.md).

Kad potenciālais klients ir apstiprināts, sistēma izveido divus jaunus debitoru ierakstus:

- Viens debitora ieraksts ar **organizācijas** tipu pārstāv organizāciju, kas pieprasa kļūt par biznesa partneri.
- Viens debitora ieraksts ar personas **tipu** pārstāv personu, kas iesniedza pieprasījumu.

Turklāt mazumtirdzniecības un commerce debitoru hierarhijās tiek izveidots jauns **\> debitoru hierarhijas \> ieraksts**. Šim debitora hierarhijas ierakstam ir šādi rekvizīti:

- **Debitoru hierarhijas ID** – debitoru hierarhijas unikālais ID. Šis ID izmanto numuru sēriju, ko definējiet Commerce koplietojamie parametri.
- **Nosaukums** – biznesa partnera organizācijas nosaukums, kā norādīts uzņēmuma pieprasījumā. Šo lauku var labot.
- **Mērķis** – šis rekvizīts ir iestatīts uz iepriekš definētu vērtību **B2B organizācijai**.
- **Organizācija** – biznesa partnera organizācijas debitora ID.

Persona, kas iesniedzaboarding pieprasījumu, tiek pievienota kopsavilkuma **cilnē** Hierarhija, un **administratora** loma tiem ir piešķirta. Kad administrators pievieno vairāk lietotāju biznesa partnera organizācijai B2B vietnē, katram lietotājam tiek izveidots jauns klienta ieraksts. Klienta ieraksts tiek pievienots arī atbilstošajam biznesa partnera debitoru hierarhijas ierakstam, un **tam** tiek piešķirta lietotāja loma.

### <a name="examples"></a>Piemēri

Persona, kuras nosaukums ir Sems J. iesniedz uzņēmuma pieprasījumu Microsoft organizācijas vārdā. Kad pieprasījums ir apstiprināts, tiek izveidoti divi jauni klientu konti: **viens** no Personas tipa Semam J. **un viens no** Organizācijas transportlīdzekļa tipa — Microsoft.

Kā parādīts šajā ilustrācijā piemērā, tiek izveidots arī jauns debitoru hierarhijas ieraksts. Šim ierakstam ir tāds pats nosaukums kā organizācijai (**Microsoft**), un **Administratora loma** ir piešķirta Semam J. Sems J. kā administrators pievieno šai hierarhijai jebkurus citus B2B vietas Microsoft lietotājus un **piešķir tiem** lietotāju. Šajā piemērā Sush R. ir pievienots kā lietotājs.

![Debitoru hierarhijas ieraksta piemērs.](../media/CustomerHierarchy2.png)

Lai noteiktu, vai debitors ir saistīts ar debitoru hierarhiju, atveriet debitora ierakstu. Šajā ilustrācijā parādīts piemērs. **Debitoru hierarhijas ID** **lauks Kopsavilkuma cilnes Retail** sadaļā B2B **parāda**, vai debitors ir daļa no debitoru hierarhijas, **un B2B administratora** opcija norāda, vai klients ir šīs hierarhijas administrators.

![Piemērs B2B sadaļai Klienta ieraksta Retail FastTab, kur debitors ir saistīts ar hierarhiju un norādīts kā administrators.](../media/CustomerHierarchyMapping2.png)

Vairākumā gadījumu visu hierarhijas debitoru ierakstu rekvizītu vērtībām ir jāsakrīt. Piemēram, tā kā visiem biznesa partneru lietotājiem ir jāsaņem līdzīgas preču cenas, to cenu grupai un saistītajām konfigurācijām ir jāatbilst. Tomēr sistēma šo konsekvenci neievieš. Tāpēc attiecīgie Commerce Headquarters lietotāji ir atbildīgi nodrošināt, ka rekvizītu vērtības un konfigurācijas atbilst visiem attiecīgās hierarhijas klientiem.

Commerce Headquarters lietotāji var pārbaudīt rekvizītu vērtības visiem debitoru ierakstiem hierarhijā līdzās skatā. Šajā ilustrācijā parādīts piemērs, varat izmantot opciju Vispārīgi kopsavilkuma cilnes Hierarhija nolaižamajā sarakstā un pēc tam atlasīt jebkuru debitora ieraksta sadaļu, **·** **lai** parādītu saistītos rekvizītus. Lietotāji rekvizītu vērtības var labot tieši šajā skatā. Lai kopētu visas vērtības no administratora debitora ieraksta uz visiem lietotājiem, atlasiet **Ignorēt** kopsavilkuma **cilnē** Hierarhija.

![Debitora hierarhijas ieraksta piemērs, kas rāda pogu Ignorēt un nolaižamā saraksta opciju.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
