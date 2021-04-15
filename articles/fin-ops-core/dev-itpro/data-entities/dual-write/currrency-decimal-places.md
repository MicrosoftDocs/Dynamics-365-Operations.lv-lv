---
title: Valūtas datu tipa migrācija duālajai rakstīšanai
description: Šajā tēmā aprakstīts, kā mainīt decimāldaļu skaitu, ko duālā rakstīšana atbalsta valūtai.
author: RamaKrishnamoorthy
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: c4f663ae36f7d4ea3db9888e618f2fe3bf8c3256
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748951"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Valūtas datu tipa migrācija duālajai rakstīšanai

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Varat palielināt decimāldaļu skaitu, kas tiek atbalstītas ne vairāk kā 10 valūtas vērtībām. Noklusējuma ierobežojums ir četras decimāldaļas. Palielinot decimāldaļu skaitu, jūs palīdzēsiet novērst datu zudumu, kad izmantojat duālo rakstīšanu, lai sinhronizētu datus. Decimāldaļu skaita pieaugums ir izvēles izmaiņa. Lai to īstenotu, jums ir jāpieprasa palīdzība no Microsoft.

Decimāldaļu skaita maiņas procesam ir divi soļi:

1. Pieprasīt migrāciju no Microsoft.
2. Mainīt decimāldaļu skaitu Dataverse.

Finance and Operations programmai un Dataverse ir jāatbalsta tas pats decimāldaļu skaits valūtas vērtībās. Pretējā gadījumā datu zudums var rasties gadījumā, kad šī informācija tiek sinhronizēta starp programmām. Migrācijas process pārkonfigurē valūtas un maiņas kursa vērtību saglabāšanas veidu, bet nemaina nekādus datus. Kad migrācija ir pabeigta, valūtas kodu un izcenojumu decimāldaļu skaits var tikt palielināts, un datiem, ko lietotāji ievada un skata, var būt vairāk decimāldaļas precizitātes.

Migrācija nav obligāta. Ja jums varētu būt noderīgs atbalsts vairāk decimāldaļām, mēs iesakām jums apsvērt migrāciju. Organizācijas, kurām nav nepieciešamas vērtības, kurām ir vairāk nekā četras decimāldaļas, nav jāmigrē.

## <a name="requesting-migration-from-microsoft"></a>Migrācijas pieprasīšana no Microsoft

Esošo valūtas lauku glabāšana programmā Dataverse nevar atbalstīt vairāk par četrām decimāldaļām. Tāpēc migrācijas procesa laikā valūtas vērtības tiek pārkopētas uz jaunajiem iekšējiem laukiem datu bāzē. Šis process notiek nepārtraukti, līdz visi dati ir migrēti. Iekšēji migrācijas beigās jaunie glabāšanas tipi aizvieto vecos glabāšanas tipus, bet datu vērtības netiek mainītas. Valūtas lauki var atbalstīt līdz 10 decimāldaļām. Migrācijas procesa laikā Dataverse var turpināt tikt izmantots bez pārtraukumiem.

Tajā pašā laikā valūtas maiņas kursi tiek modificēti tā, lai tie atbalstītu līdz 12 decimāldaļām pašreizējo 10 vietā. Šī izmaiņa ir nepieciešama, lai abās programmās ir vienāds decimāldaļu skaits gan Finance and Operations programmā, gan Dataverse.

Migrācija nemaina nekādus datus. Kad valūtas un maiņas kursu lauki ir pārveidoti, administratori var konfigurēt sistēmu, lai izmantotu līdz 10 decimāldaļām valūtas laukiem, norādot katras darījuma valūtas un cenu decimāldaļu skaitu.

### <a name="request-a-migration"></a>Pieprasīt migrāciju

Lai padarītu šo līdzekli pieejamu, nosūtiet ziņojumu uz e-pastu **CDSExpandDecimal@microsoft.com** un iekļaujiet sekojošo informāciju:

+ **Tēma:** pieprasīt iespējot paplašinātu decimālo atbalstu \<organizationID\>
+ **Pamatteksts:** es vēlos iespējot izvērstu decimālo atbalstu manai organizācijai \<organizationID\>.

Microsoft pārstāvis sazināsies ar jums divu vai trīs darbdienu laikā, lai izklāstītu nākamos soļus.

Kad jūs pieprasāt migrāciju, jums ir jāapzinās šādas detaļas un tās atbilstoši jāplāno:

+ Laiks, kas nepieciešams, lai migrētu datus, ir atkarīgs no datu apjoma sistēmā. Lielu datu bāzu migrācija var ilgt vairākas dienas.
+ Datu bāzes lielums īslaicīgi palielinās, kamēr notiek migrācija, jo indeksiem ir nepieciešama papildu vieta. Lielākā daļa papildu vietas tiek atbrīvotas, kad migrācija ir pabeigta.
+ Migrācijas procesa laikā, ja rodas kļūdas, kas novērš migrācijas pabeigšanu, sistēma veido brīdinājumus Microsoft atbalstam, lai atbalsta personāls varētu iejaukties. Tomēr pat, ja migrācijas laikā rodas kļūdas, Dataverse ir pilnībā pieejams regulārai lietošanai.
+ Migrācijas process nav atgriezenisks.

## <a name="changing-the-number-of-decimal-places"></a>Decimāldaļu skaita mainīšana

Pēc migrācijas pabeigšanas Dataverse var saglabāt skaitļus, kuriem ir vairāk decimāldaļu. Administratori var izvēlēties, cik decimāldaļu tiek izmantotas noteiktiem valūtas kodiem un cenu noteikšanai. Microsoft Power Apps, Power BI un Power Automate lietotāji pēc tam var skatīt un izmantot skaitļus, kuriem ir vairāk decimāldaļu.

Lai veiktu šīs izmaiņas, ir jāatjaunina šādi iestatījumi programmā Power Apps:

+ **Sistēmas iestatījumi: valūtas precizitāte cenu noteikšanai** — lauks **Iestatīt valūtas precizitāti, kas tiek izmantota cenu noteikšanai visā sistēmā** nosaka, kā valūta mainīsies organizācijā, atlasot **Cenu noteikšanas precizitāti**.
+ **Biznesa pārvaldība: valūtas** – lauks **Valūtas precizitāte** ļauj norādīt pielāgotu decimāldaļu skaitu noteiktai valūtai. Ir pieejama alternatīva organizācijas mēroga iestatījumam.

Ir daži ierobežojumi:

+ Nevar konfigurēt elementa valūtas lauku tabulā.
+ Varat norādīt vairāk nekā četras decimāldaļas tikai **Cenu noteikšanai** un **Darījuma valūtas** līmeņos.

### <a name="system-settings-currency-precision-for-pricing"></a>Sistēmas iestatījumi: cenu valūtas precizitāte

Pēc migrācijas pabeigšanas administratori var iestatīt valūtas precizitāti. Dodieties uz **Iestatījumi \> Administrēšana** un atlasiet **Sistēmas iestatījumi**. Pēc tam cilnē **Vispārīgi** mainiet lauka **Iestatīt valūtas precizitāti, kas ir izmantota cenu noteikšanā visā sistēmā** vērtību, kā parādīts sekojošajā ilustrācijā.

![Valūtas sistēmas iestatījumi](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Biznesa pārvaldība: Valūtas

Ja vēlaties, lai konkrētas valūtas precizitātes atšķirtos no valūtas precizitātes, kas tiek izmantota cenu noteikšanai, varat mainīt to. Dodieties uz **Iestatījumi \> Biznesa pārvaldība**, atlasiet **Valūtas** un atlasiet valūtu, ko vēlaties mainīt. Pēc tam iestatiet **Valūtas precizitātes** lauku uz vēlamo decimāldaļu skaitu, kā parādīts sekojošajā ilustrācijā.

![Noteiktas lokalizācijas valūtu iestatījumi](media/specific-currency.png)

### <a name="tables-currency-column"></a>tabulas: valūtas lauks

Decimāldaļu skaits, ko var konfigurēt noteiktiem valūtas laukiem, ir ierobežots līdz četriem.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]