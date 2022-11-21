---
title: Priekšapmaksa Dynamics 365 Commerce
description: Šajā rakstā ir sniegts pārskats par priekšapmaksas transakciju apstrādi pakalpojumā Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780204"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Priekšapmaksa Dynamics 365 Commerce

[!include[banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par priekšapmaksas transakciju apstrādi pakalpojumā Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce apstrādā priekšapmaksas transakcijas šādiem debitoru parādu vai komercijas maksājumu tipiem:

- **Debitora konta depozīta maksājums** — debitors iemaksā depozītu tirdzniecības vietā (POS). Commerce apstrādā depozīta maksājumu kā priekšapmaksas darījumu. Kad grāmatojat darījumu, tiek izveidots maksājumu žurnāls, kas tiek grāmatots **Žurnāla dokumenta** lapā Commerce galvenajā mītnē. Izvēles rūtiņa **Priekšapmaksas** žurnāla kupons **cilnē Maksājums** tiek automātiski atlasīta maksājumu žurnālam. Papildinformāciju, tostarp priekšapmaksas un ar nodokļiem saistītu informāciju, kas attiecas uz mērķa reģionu, skatiet rakstā [Palīdzības saturs par atrašanās vietu Globalizācijas resursi — ar valsti/reģionu saistīts palīdzības saturs](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content).
- **Debitora pasūtījums, kuram ir depozīts** — debitors izveido debitora pasūtījumu POS. Debitors var samaksāt depozītu par pasūtījumu, pamatojoties uz noklusējuma depozīta procentuālo daļu, kas ir konfigurēta **lapā Klientu pasūtījumi galvenajā mītnē (** Komercijas parametri **Klientu pasūtījumi \>**). Commerce apstrādā depozīta maksājumu par debitora pasūtījumu kā priekšapmaksas darījumu. Kad grāmatojat darījumu, tiek izveidots maksājumu žurnāls, kas tiek publicēts **žurnāla dokumenta** lapā. Izvēles rūtiņa **Priekšapmaksas** žurnāla kupons **cilnē Maksājums** tiek automātiski atlasīta maksājumu žurnālam. Maksājums tiek segts, un debitora rēķins tiek automātiski izsniegts, kad pasūtījums tiek saņemts vai piegādāts.
- **Zvanu centra pārdošanas pasūtījums** — zvanu centra klientu apkalpošanas pārstāvis debitora vārdā izveido pārdošanas pasūtījumu, un **priekšapmaksas** atribūts maksājuma tveršanas laikā ir iestatīts uz **Jā**.

Lai apstrādātu priekšapmaksu, komercija veic šādus uzdevumus:

- **Debitora konta depozīta maksājuma** apstrāde — debitora veiktais depozīta maksājums tiek pārskaitīts uz komerciju, izmantojot pakalpojumu, kas sinhronizē datus. Commerce izveido neliela apjoma maksājuma transakciju maksājumam. Kad grāmatojat mazumtirdzniecības darījumu, tiek grāmatots skaidras naudas žurnāls vai debitoru maksājumu žurnāls. Izvēles rūtiņa **Priekšapmaksas žurnāla kupons lapas Žurnāla kupons** **cilnē** Maksājums **galvenajā mītnē Commerce Headquarters tiek automātiski atlasīta** maksājumu žurnālam. Priekšapmaksu nevar apstrādāt, ja maksājuma summa ir negatīva.
- **Apstrādāt debitora pasūtījumu vai pārdošanas pasūtījumu, kuram ir depozīts — debitors maksā nepieciešamo depozītu** par klienta pasūtījumu, izmantojot Commerce Data Exchange: Reāllaika pakalpojums. Commerce izveido debitoru maksājumu žurnālu vai skaidras naudas žurnālu atkarībā no debitora izmantotās maksāšanas metodes. Izvēles rūtiņa **Priekšapmaksas** žurnāla kupons **lapas Žurnāla kupons** cilnē **Maksājums** tiek automātiski atlasīta žurnālam galvenajā mītnē Commerce Headquarters. Ja debitors izmanto vairākus maksājuma veidus, lai veiktu daļējus maksājumus, Commerce apstrādā katru daļējo maksājumu, pamatojoties uz izmantoto maksājuma veidu.

Kredītkartēm un digitālajiem makiem, kuriem ir pamatā esošas kredītkaršu maksājumu metodes, Commerce pēc veiksmīgas autorizācijas nosūta tveršanas pieprasījumu. (Līdzekļi tiek tverti pirms pārdošanas pasūtījuma rēķina izrakstīšanas.)

Ja atceļat debitora pasūtījumu, priekšapmaksas summa tiek atmaksāta un depozīta summai tiek grāmatots atmaksas maksājumu žurnāls. Atmaksas summa tiek aprēķināta un iegrāmatota, pamatojoties uz maksājuma veidu, kuru norādījāt, grāmatojot atmaksas maksājumu. Komercijai var tikt piemērota atcelšanas maksa, pamatojoties uz procentuālo vērtību, ko iestatījāt **lapā Komercijas parametri** galvenajā mītnē Commerce Heads.

Ja atgriežat debitora pasūtījumu, tiek izveidots atgriešanas pasūtījums un atmaksas maksājumu žurnāls. Kad grāmatojat atgriešanas pasūtījumu, Commerce izveido debitora maksājumu žurnālu vai skaidras naudas žurnālu atkarībā no maksājuma metodes, ko debitors izmantoja sākotnējai transakcijai.
