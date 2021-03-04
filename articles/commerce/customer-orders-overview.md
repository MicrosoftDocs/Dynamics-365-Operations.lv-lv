---
title: Debitoru pasūtījumi Pārdošanas punktā (POS)
description: Šajā tēmā ir sniegta informācija par debitoru pasūtījumiem Pārdošanas punktā (POS). Debitoru pasūtījumi tiek saukti arī par īpašajiem pasūtījumiem. Šajā tēmā ir iekļauta diskusija par saistītajiem parametriem un transakciju plūsmām.
author: josaw1
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9e5770de82638e6cef6d4c1dffd1dc85549fb11f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414036"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Debitoru pasūtījumi Pārdošanas punktā (POS)

[!include [banner](includes/banner.md)]

Šajā tēmā ir sniegta informācija par to, kā izveidot un pārvaldīt debitoru pasūtījumus Pārdošanas punktā (POS). Debitoru pasūtījumus var izmantot, lai notvertu tos pārdošanas gadījumus, kad pircēji vēlas saņemt preces vēlākā datumā, saņemt preces no citas atrašanās vietas vai arī, lai preces tiktu nosūtītas viņiem. 

Visaptveroša kanāla tirdzniecības pasaulē daudzi mazumtirgotāji nodrošina iespēju izmantot debitoru pasūtījumus jeb īpašos pasūtījumus, lai izpildītu dažādas preču un izpildes prasības. Tālāk uzskaitīti daži tipiski scenāriji.

- Debitors vēlas, lai preces tiek piegādātas uz konkrētu adresi konkrētā datumā.
- Debitors preces vēlas saņemt tādā veikalā vai atrašanās vietā, kas atšķiras no veikala vai atrašanās vietas, kur debitors šīs preces iegādājās.
- Debitors krātuvē vēlas pasūtīt preces šodien un paņemt tās no tās pašas krātuves vēlākā datumā.

Mazumtirgotāji debitoru pasūtījumus var izmantot ar mērķi mazināt pārdošanas zudumus, kurus pretējā gadījumā izraisītu krājumu deficīts, jo preces var piegādāt vai izdot dažādos laikos vai vietās.

## <a name="set-up-customer-orders"></a>Iestatīt debitoru pasūtījumus
Pirms mēģināt punktā POS izmantot debitora pasūtījumu funkcionalitāti, pārliecinieties, ka esat paveicis visas nepieciešamās konfigurācijas programmā Commerce Headquarters.

### <a name="configure-modes-of-delivery"></a>Piegādes veidu konfigurēšana

Lai lietotu debitoru pasūtījumus, ir jākonfigurē piegādes veidi, ko var izmantot krātuves kanāls. Ir jādefinē vismaz viens piegādes veids, ko var izmantot, kad pasūtījuma rindas tiek nosūtītas debitoram no krātuves. Ir arī jādefinē vismaz viens paņemšanas piegādes veids, ko var izmantot, kad pasūtījuma rindas tiek paņemtas no krātuves. Piegādes veidi ir definēti programmas Commerce Headquarters lapā **Piegādes veidi** . Papildinformāciju par to, kā iestatīt Commerce kanālu piegādes veidus, skatiet rakstā [Piegādes veidu definēšana](https://docs.microsoft.com/dynamics365/commerce/configure-call-center-delivery#define-delivery-modes).

![Piegādes veidu lapa](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Izpildes grupu iestatīšana

Dažas krātuves vai noliktavas var nespēt izpildīt debitoru pasūtījumus. Konfigurējot izpildes grupas, organizācija var norādīt, kuras krātuves un noliktavas tiek rādītas kā opcijas lietotājiem, kas izveido debitoru pasūtījumus POS punktā. Izpildes grupas ir konfigurētas lapā **Izpildes grupas**. Organizācijas var izveidot tik daudz izpildes grupu, cik nepieciešams. Kad izpildes grupa ir definēta, tā ir saistīta ar krātuvi, izmantojot pogu cilnē **Iestatīt** , kas atrodas lapas **Krātuves** darbības rūtī.

Commerce versijā 10.0.12 un vēlākā versijā, organizācijas var noteikt, vai noliktavas vai noliktavas/krātuves kombinācijas, kas definētas izpildes grupās, var tikt izmantotas nosūtīšanai, saņemšanai vai gan piegādei, gan saņemšanai. Tāpēc krātuvei ir papildu elastīgums, lai vadītu noliktavas un krātuves opcijas, kas tiek rādītas lietotājiem, kuri veido saņemšanas pasūtījumu salīdzinājumā ar nosūtīšanas pasūtījumu. Lai izmantotu šīs konfigurācijas opcijas, ir jāieslēdz līdzeklī **Spēja noteikt atrašanās vietas kā "nosūtīšana" vai "saņemšana", kas ir iespējotas izpildes grupās** . Ja noliktava, kas ir saistīta ar izpildes grupu, nav krātuve, to var konfigurēt tikai kā nosūtīšanas vietu. To nevar izmantot, ja saņemšanas pasūtījumi tiek konfigurēti POS punktā.

![Izpildes grupu lapa](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanāla iestatījumu konfigurēšana

Strādājot ar klientu pasūtījumiem POS punktā, ir jāapsver daži krātuves kanāla iestatījumi. Šie iestatījumi ir pieejami programmas Commerce Headquarters lapā **Krātuves** .

- **Noliktava** – Šis lauks norāda noliktavu, kas tiek izmantota, lai izpildītu pasūtījumus, kas ir konfigurēti nosūtīšanai no krātuves.
- **Izpildes grupas piešķire** – Atlasiet šo pogu (cilnē **Iestatīt** darbības rūtī), lai sasaistītu izpildes grupas, uz kurām ir atsauce, lai parādītu saņemšanas vietu vai sūtījuma izcelsmes opcijas, kad debitoru pasūtījumi tiek veidoti POS punktā.
- **Izmantot mērķa nodokli** – Šī opcija norāda, vai piegādes adrese tiek izmantota, lai noteiktu nodokļu grupu, kas tiek lietota pasūtījuma rindām, kas tiek nosūtītas uz debitora adresi.
- **Izmantot uz debitoru balstītu nodokli** – Šī opcija norāda, vai nodokļu grupa, kas ir noteikta klienta piegādes adresei, tiek izmantota debitoru pasūtījumu apmaksai, kas tiek izveidoti POS punktā nosūtīšanai uz klienta mājām.

![Krātuves kanāla iestatīšana lapā Krātuves](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Iestatīt debitora pasūtījuma parametrus

Pirms jūs mēģināt izveidot debitoru pasūtījumus POS punktā, ir jākonfigurē atbilstošie parametri programmā Commerce Headquarters. Šos parametrus var atrast cilnē **Debitoru pasūtījumi** lapā **Commerce parametri** .

- **Noklusējuma pasūtījuma veids** – Varat norādīt pasūtījuma veidu, kas pēc noklusējuma ir piešķirts debitora pasūtījumiem, kas tiek izveidoti POS punktā. Šie debitoru pasūtījumi var būt pārdošanas pasūtījumi vai piedāvājumu pasūtījumi. Neņemot vērā noklusējuma pasūtījuma veidu, lietotāji joprojām var izveidot gan pārdošanas pasūtījumus, gan debitoru pasūtījumus no POS punkta.
- **Noklusējuma depozīts procentos** – Norādiet pasūtījuma kopsummas procentuālo vērtību, kas debitoram ir jāsamaksā kā depozīts, lai pasūtījumu varētu apstiprināt. Atkarībā no viņu privilēģijām, krātuves saistītie dalībnieki, iespējams, var pārlabot summu, izmantojot darbību **Depozīta pārlabošana** POS punktā, ja šī darbība ir konfigurēta darījuma ekrāna izkārtojumam.
- **Saņemšanas piegādes veids** – Norādiet piegādes veidu, kas jālieto pārdošanas pasūtījuma rindām, kas ir konfigurētas saņemšanai POS punktā.
- **Komplektēšanas piegādes veids** – Norādiet piegādes veidu, kas jālieto pārdošanas pasūtījuma rindām, kas tiek uzskatītas kā komplektēšanas pasūtījuma rindas, kad tiek izveidots jaukts grozs, kurā dažas rindas tiks saņemtas vai nosūtītas, un debitoram nekavējoties tiks veiktas citas rindas.
- **Atcelšanas maksa procentos** – Ja debitora pasūtījuma atcelšanas gadījumā ir jāpiemēro maksa, norādiet šīs maksas summu.
- **Atcelšanas maksas kods** – Norādiet debitoru parādu maksas kodu, kas jāizmanto, kad atcelšanas maksa tiek piemērota atceltajiem debitora pasūtījumiem, izmantojot POS punktu. Maksas kods definē atcelšanas maksas finanšu grāmatošanas loģiku.
- **Piegādes maksas kods** – Ja opcija **Izmantot papildu automātiskās maksas** ir iestatīta uz **Jā**, šim parametru iestatījumam nav efekta. Ja šī opcija ir iestatīta uz **Nē**, lietotājiem tiek piedāvāts manuāli ievadīt piegādes maksu, kad tie izveido debitoru pasūtījumus POS punktā. Izmantojiet šo parametru, lai kartētu debitoru parādu maksas kodu, kas tiks lietots pasūtījumiem, kad lietotāji ievada piegādes maksu. Maksas kods definē piegādes maksas finanšu grāmatošanas loģiku.
- **Izmantot papildu automātiskās maksas** – Iestatiet šo opciju uz **Jā** , lai izmantotu sistēmas aprēķinātās automātiskās maksas, kad debitora pasūtījumi tiek izveidoti POS punktā. Šīs automātiskās maksas var izmantot, lai aprēķinātu piegādes maksas vai citus pasūtījuma vai krājuma specifiskās izmaksas. Papildinformāciju par to, kā iestatīt un lietot papildu automātiskās izmaksas, skatiet [Omni-kanālu uzlabotās automātiskās maksas](https://docs.microsoft.com/dynamics365/commerce/omni-auto-charges).

![Cilne Klientu pasūtījumi lapā Commerce parametri](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Atjaunināt transakcijas ekrāna izkārtojumus POS punktā

Pārliecinieties, ka POS punktā [ekrāna izkārtojums](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) ir konfigurēts tā, lai atbalstītu debitoru pasūtījumu izveidi un pārvaldību, un ka visas nepieciešamās POS operācijas ir konfigurētas. Piedāvājam dažas POS operācijas, kas ir ieteicamas, lai pareizi atbalstītu klientu pasūtījumu izveidi un pārvaldību:
- **Nosūtīt visas preces** — Šī operācija tiek izmantota, lai norādītu, ka visas transakciju groza rindas tiks nosūtītas uz galamērķi.
- **Nosūtīt atlasītās preces** — Šī operācija tiek izmantota, lai norādītu, ka atlasītās transakciju groza rindas tiks nosūtītas uz galamērķi.
- **Saņemt visas preces** — Šī operācija tiek izmantota, lai norādītu, ka visas transakciju groza rindas tiks saņemtas no atlasītās krātuves atrašanās vietas.
- **Saņemt atlasītās preces** — Šī operācija tiek izmantota, lai norādītu, ka atlasītās transakciju groza rindas tiks saņemtas no atlasītās krātuves atrašanās vietas.
- **Realizēt visas preces** — Šī operācija tiek izmantota, lai norādītu, ka visas transakciju groza rindas tiks realizētas. Ja šī operācija tiek izmantota POS punktā, debitora pasūtījums tiks pārveidots uz skaidras naudas pārveduma transakciju.
- **Realizēt atlasītās preces** — Šī operācija tiek izmantota, lai norādītu, ka atlasītās transakciju groza rindas debitoram tiek realizētas pirkšanas laikā. Šī operācija ir noderīga tikai [hibrīda pasūtījuma](https://docs.microsoft.com/dynamics365/commerce/hybrid-customer-orders) scenārijā.
- **Atsaukt pasūtījumu** – Šī operācija tiek izmantota, lai meklētu un izgūtu debitoru pasūtījumus tā, lai POS lietotāji pēc vajadzības varētu rediģēt, atcelt vai veikt ar izpildi saistītās operācijas.
- **Mainīt piegādes veidu** – Šo operāciju var izmantot, lai ātri mainītu piegādes veidu rindām, kas jau ir konfigurētas nosūtīšanai, nepieprasot, lai lietotāji no jauna izietu cauri plūsmai "nosūtīt visas preces" vai "nosūtīt atlasītās preces".
- **Depozīta pārlabošana** — Šo operāciju var izmantot, lai izmainītu depozīta summu, ko debitors maksās par atlasīto debitora pasūtījumu.

![Operācijas POS darbības ekrānā](media/customer-order-screen-layout.png)

## <a name="working-with-customer-orders-in-pos"></a>Darbs ar debitoru pasūtījumiem POS punktā

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>Izveidot debitora pasūtījumu precēm, kas tiks nosūtītas debitoram

1. POS transakciju ekrānā pievienojiet debitoru transakcijai.
2. Pievienojiet grozam preces.
3. Atlasiet **Nosūtīt atlasīto** vai **Nosūtīt visu** , lai nosūtītu preces uz adresi debitora kontā.
4. Izvēlieties opciju, lai izveidotu debitora pasūtījumu.
5. Apstipriniet vai mainiet "nosūtīt no" atrašanās vietu, apstipriniet vai mainiet piegādes adresi un atlasiet piegādes metodi.
6. Ievadiet debitora vēlamo pasūtījuma nosūtīšanas datumu.
7. Izmantojiet maksājuma funkcijas, lai samaksātu par visām apmaksājamajām summām, vai izmantojiet operāciju **Depozīta pārlabošana** , lai mainītu maksājamās summas un pēc tam pielietotu maksājumu.
8. Ja pilna pasūtījuma kopsumma netika apmaksāta, ievadiet kredītkarti, kas tiks uztverta bilancei, kurai pasūtījums ir jāizpilda, kad rēķins ir izrakstīts.

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>Izveidot debitora pasūtījumu precēm, ko saņems debitors

1. POS transakciju ekrānā pievienojiet debitoru transakcijai.
2. Pievienojiet grozam preces.
3. Atlasiet opciju **Saņemt atlasīto** vai **Saņemt visu** , lai sāktu pasūtījuma saņemšanas konfigurāciju.
4. Atlasiet krātves atrašanās vietu, kur debitors saņems atlasītās preces.
5. Atlasiet saņemšanas datumu.
6. Izmantojiet maksājuma funkcijas, lai samaksātu par visām apmaksājamajām summām, vai izmantojiet operāciju **Depozīta pārlabošana** , lai mainītu maksājamās summas un pēc tam pielietotu maksājumu.
7. Ja pilna pasūtījuma kopsumma netika apmaksāta, izvēlieties, vai debitors nodrošinās maksājumu vēlāk (saņemšanas laikā), vai arī kredītkarte tiks marķēta tūlīt, un pēc tam tiks izmantota un notverta saņemšanas laikā.

### <a name="edit-an-existing-customer-order"></a>Rediģēt esošu debitora pasūtījumu

Mazumtirdzniecības pasūtījumus, kas ir izveidoti tiešsaistes vai krātuves kanālā, pēc nepieciešamības var atsaukt un rediģēt, izmantojot POS punktu.

> [!IMPORTANT]
> Zvanu centra kanālā izveidotos pasūtījumus nevar rediģēt, izmantojot POS punktu, ja iestatījums [Iespējot pasūtījuma pabeigšanu](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion) ir ieslēgts zvanu centra kanālam. Lai nodrošinātu pareizu maksājuma apstrādi, pasūtījumus, kas radās zvanu centra kanālā un kas izmanto iespējošanas pasūtījuma pabeigšanas funkcionalitāti, ir jārediģē, izmantojot zvanu centra programmu programmā Commerce Headquarters.

Commerce versijā 10.0.13 un vecākā versijā lietotāji var rediģēt atbalstītos debitoru pasūtījumus, izmantojot POS punktu, tikai tad, ja pasūtījumi ir pilnībā atvērti. Ja kāda pasūtījuma rindas jau ir apstrādātas izpildei (saņemšana, sapakošana un tā tālāk), pasūtījums tiek bloķēts rediģēšanai POS punktā.

> [!NOTE]
> Commerce versijā 10.0.14, līdzeklis, kas ir izlaists [publiskajā priekšskatījumā](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms) ļauj POS lietotājiem rediģēt debitoru pasūtījumus, izmantojot POS punktu, pat ja daži no pasūtījumiem jau ir izpildīti. Tomēr pasūtījumus, kas ir pilnībā iekļauti rēķinā, joprojām nevar rediģēt, izmantojot POS punktu. Lai pārbaudītu šo priekšskatījuma līdzekli un sniegtu papildu atsauksmes, ieslēdziet līdzekli **(Priekšskatījums) Rediģēt daļēji izpildītos pasūtījumus Pārdošanas punktā** darbvietā **Līdzekļu pārvaldība** . Debitoru pasūtījumi, kas tika izveidoti zvanu centra kanālā un kas izmanto iespējošanas pasūtījuma pabeigšanas funkcionalitāti, nevar tikt rediģēti pat pēc šīs funkcijas iespējošanas.

1. Atlasiet **Atsaukt pasūtījumu**.
2. Izmantojiet **Meklēt** , lai ievadītu filtrus, lai atrastu pasūtījumu, un pēc tam atlasiet **Pielietot**.
3. Atlasiet pasūtījumu rezultātu sarakstā un pēc tam atlasiet **Rediģēt**. Ja poga **Rediģēt** nav pieejama, pasūtījums atrodas stāvoklī, kurā to nevar rediģēt.
4. No transakciju groza veiciet nepieciešamās izmaiņas debitora pasūtījumā. Dažas izmaiņas var būt aizliegtas rediģēšanas laikā.
5. Pabeidziet rediģēšanas procesu, atlasot maksājuma operāciju.
6. Lai izietu no rediģēšanas procesa, nesaglabājot izmaiņas, varat izmantot operāciju **Anulēt transakcijas** .



### <a name="cancel-a-customer-order"></a>Debitora pasūtījuma atcelšana

1. Atlasiet **Atsaukt pasūtījumu**.
2. Izmantojiet **Meklēt** , lai ievadītu filtrus, lai atrastu pasūtījumu, un pēc tam atlasiet **Pielietot**.
3. Atlasiet pasūtījumu rezultātu sarakstā un pēc tam atlasiet **Atcelt**. Ja poga **Atcelt** nav pieejama, pasūtījums atrodas stāvoklī, kurā to vairs nevar atcelt.
4. Ja anulēšanas izmaksas ir konfigurētas, apstipriniet tās. Ja nepieciešams, atcelšanas maksu varat koriģēt pirms tās apstiprināšanas. 
5. No transakciju groza pabeidziet atcelšanas procesu, atlasot maksājuma operāciju. Ja apmaksātie depozīti pārsniedz atcelšanas maksu, var būt jāmaksā kompensācijas maksājumi.
6. Lai izietu no atcelšanas procesa, nesaglabājot izmaiņas, varat izmantot operāciju **Anulēt transakcijas** .

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Debitora pasūtījuma piegādes vai saņemšanas pabeigšana no POS punkta

Pēc pasūtījuma izveides krājumi tiks saņemti no krātuves atrašanās vietas vai nosūtīti, atkarībā no pasūtījuma konfigurācijas. Plašāku informāciju par šo procesu skatiet [krātuves pasūtījuma izpildes](https://docs.microsoft.com/dynamics365/commerce/order-fulfillment-overview) dokumentācijā.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asinhrona transakciju plūsma debitoru pasūtījumiem

Debitoru pasūtījumus POS punktā var izveidot gan sinhronajā režīmā, gan asinhronajā režīmā. Ja, veidojot debitoru pasūtījumus POS punktā, pamanāt veiktspējas problēmas vai lietotāja kavēšanos, apsveriet iespēju ieslēgt asinhronu pasūtījuma izveidi.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Iespējot debitoru pasūtījumu izveidošanu asinhronajā režīmā

1. Programmā Commerce Headquarters lapā **Funkcionalitātes profili** atlasiet funkcionalitātes profilu, kas atbilst krātuvei, kuru vēlaties konfigurēt.
2. Kopsavilkuma cilnē **Vispārīgi** opcijai **Izveidot debitora pasūtījumu asinhronā režīmā** iestatiet vērtību **Jā**.

Ja ir iestatīta opcijas **Izveidot debitora pasūtījumu asinhronā režīmā** vērtība **Jā**, debitoru pasūtījumi vienmēr tiek izveidoti asinhronajā režīmā pat tad, ja ir pieejams pakalpojums Retail Transaction Service (RTS). Ja šī opcija ir iestatīta uz **Nē**, tad debitoru pasūtījumi vienmēr tiek veidoti sinhronajā režīmā, izmantojot RTS. Kad debitora pasūtījumi tiek izveidoti asinhronā režīmā, tie tiek vilkti un izveidoti kā mazumtirdzniecības darījumi programmā Commerce Headquarters no Commerce Pull (P) darbiem. Kad manuāli vai pakešuzdevuma apstrādes ietvaros tiek palaista funkcija **Sinhronizēt pasūtījumus**, mazumtirdzniecības transakcijām tiek izveidoti atbilstošie pārdošanas pasūtījumi.

## <a name="additional-resources"></a>Papildu resursi

[Hibrīda debitoru pasūtījumi](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]