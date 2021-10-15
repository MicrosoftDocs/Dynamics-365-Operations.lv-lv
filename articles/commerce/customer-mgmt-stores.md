---
title: Klientu pārvaldība veikalos
description: Šajā tēmā paskaidrots, kā mazumtirgotāji var iespējot klientu pārvaldības iespējas pārdošanas punktā (POS) risinājumā Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4fd6039843be09ec706e45746d5724faa99a95e6
ms.sourcegitcommit: 3f59b15ba7b4c3050f95f2b32f5ae6d7b96e1392
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563065"
---
# <a name="customer-management-in-stores"></a>Klientu pārvaldība veikalos

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā paskaidrots, kā mazumtirgotāji var iespējot klientu pārvaldības iespējas pārdošanas punktā (POS) risinājumā Microsoft Dynamics 365 Commerce.

Ir būtiski, ka veikala asistenti var izveidot un rediģēt klientu ierakstus pārdošanas punktā. Tādējādi viņi var fiksēt jebkādus klienta informācijas atjauninājumus, piemēram, e-pasta adresi, tālruņa numura vai adreses maiņu. Šī informācija noder lejupstraumes sistēmās, piemēram, mārketingā, jo šo sistēmu efektivitāte ir atkarīga no klientu datu precizitātes.

Pārdošanas asistenti var aktivizēt klientu izveides darbplūsmu no diviem POS ievades punktiem. Viņi var atlasīt pogu, kas tiek kartēta uz operāciju **Klienta pievienošana**, vai viņi var lietojumprogrammas joslā meklēšanas rezultātu lapā atlasīt **Izveidot klientu**. Abos gadījumos tiek parādīts dialoglodziņš **Jauns klients**, kurā pārdošanas asistenti var ievadīt nepieciešamos klienta datus, piemēram, klienta vārdu un uzvārdu, e-pasta adresi, tālruņa numuru, adresi un jebkādu papildu informāciju, kura ir saistoša biznesam. Papildu informāciju var fiksēt, izmantojot tos klienta atribūtus, kuri ir saistīti ar klientu. Papildinformāciju par klientu atribūtiem skatiet rakstā [Klienta atribūti](dev-itpro/customer-attributes.md).

Pārdošanas asistenti var arī fiksēt sekundāras e-pasta adreses un tālruņa numurs. Turklāt viņi var tvert klienta preferences attiecībā uz mārketinga informācijas saņemšanu, izmantojot jebkuru no sekundārajām e-pasta adresēm vai tālruņa numuriem. Lai iespējotu šo iespēju, mazumtirgotājiem ir Commerce galvenās pārvaldes darbvietā **Līdzekļu pārvaldība** jāiespējo līdzeklis **Tvert vairākus e-pastus un tālruņa numurus un saņemt piekrišanu mārketingam uz šo kontaktinformāciju** (**Sistēmu pārvaldība\>Darbvietas\>Līdzekļu pārvaldība**).

## <a name="default-customer-properties"></a>Klienta noklusējuma rekvizīti

Mazumtirgotāji var izmantot Commerce galvenās pārvaldes lapu **Visi veikali** (**Retail un Commerce\>Kanāli\>Veikali**), lai saistītu noklusējuma klientu ar katru veikalu. Pēc tam Commerce kopē noklusējuma klientam definētos līdzekļus uz visiem jaunajiem izveidotajiem klienta ierakstiem. Piemēram, dialoglodziņš **Izveidot klientu** rāda rekvizītus, kuri tiek mantoti no noklusējuma klienta, kas tiek saistīts ar veikalu. Šie rekvizīti ietver **klienta veidu**, **klienta grupu**, **rēķina opciju**, **rēķina e-pastu**, **valūtu** un **valodu**. Jebkādas **piederības** (klientu kopas) arī tiek mantotas no noklusējuma klienta. Taču **finanšu dimensijas** tiek mantotas no tās klientu grupas, kura ir saistīta ar noklusējuma klientu, nevis no paša noklusējuma klienta.

> [!NOTE]
> **Rēķina e-pasta** vērtība tiek kopēta no noklusējuma klienta tikai tad, ja jaunizveidotajiem klientiem nav norādīts rēķina e-pasta ID. Tas nozīmē, ka, ja rēķina e-pasta ID ir uz noklusējuma klienta, tad visi klienti, kas izveidoti no e-komercijas vietnes, saņems tādu pašu rēķina e-pasta ID, jo nav lietotāja interfeisa, lai tvertu kvīts e-pasta ID no klienta. Iesakām atstāt lauku **kvīts e-pasts** tukšu veikala noklusējuma klientam un to izmantot vienīgi tad, ja jums ir biznesa process, kurš ir atkarīgs no tā, vai ir klātesoša kvīts e-pasta adrese. 

Pārdošanas asistenti var tvert vairākas klienta adreses. Klienta vārds, uzvārds un tālruņa numurs tiek mantots no kontaktinformācijas, kura ir saistīta ar katru adresi. Klienta ieraksta kopsavilkuma cilne **Adreses** ietver lauku **Mērķis**, kuru pārdošanas asistents var rediģēt. Ja klienta veids ir **Persona**, noklusējuma vērtība ir **Mājas**. Ja klients veids ir **Organizācija**, noklusējuma vērtība ir **Bizness**. Citas šī lauka atbalstītās vērtības ietver **Mājas**, **Birojs** un **Pastkaste**. Lauka **Valsts** vērtība adresei tiek mantota no primārās adreses, kura tiek norādīta Commerce galvenās pārvaldes lapā **Pārvaldības struktūrvienība**, dodoties uz **Organizācijas pārvaldība\>Organizācijas\>Pārvaldības struktūrvienības**.

## <a name="sync-customers-and-async-customers"></a>Klientu sinhronizēšana un asinhronizēšana

> [!IMPORTANT]
> Katru reizi, kad POS ir bezsaistē, sistēma automātiski izveido klientu asinhroni pat, ja ir atspējots asinhronas klientu izveidnes režīms. Tāpēc, neatkarīgi no tā, vai izvēlaties sinhrono vai asinhrono klientu izveidi, Commerce galvenās pārvaldes administratoriem ir jāizveido un jāieplāno atkārtots pakešuzdevums **P-darbam**, uzdevumam **Sinhronizēt klientus un biznesa partnerus no asinhronā režīma** (iepriekš zināms kā uzdevums **Sinhronizēt klientus un biznesa partnerus no asinhronā režīma**) un uzdevumam **1010**, lai jebkādi asinhronie klienti Commerce galvenajā pārvaldē tiktu konvertēti par sinhronajiem klientiem.

Risinājumā Commerce ir divi klientu izveides režīmi: sinhronā un asinhronā. Klienti pēc noklusējuma tiek izveidoti sinhroni. Citiem vārdiem sakot, tos izveido Commerce galvenajā pārvaldē reāllaikā. Sinhronizētais klientu izveides režīma priekšrocība ir tas, ka jaunos klientus var nekavējoties meklēt visos kanālos. Taču šim režīmam ir arī trūkums. Tā kā tas uz Commerce galveno pārvaldi ģenerē zvanus [Commerce Data Exchange: Reāllaika pakalpojums](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service), var tikt ietekmēts sniegums, ja secīgi tiek veikti vairāki klientu izveides zvani.

Ja opcija **Izveidot klientu asinhronajā režīmā** ir iestatīta uz **Jā** veikala funkcionalitātes profilā (**Retail un Commerce\>Kanāla iestatīšana\>Tiešsaistes veikala iestatīšana\>Funkcionalitātes profili**), reāllaika pakalpojuma zvani netiek izmantoti klientu ierakstu izveidei kanāla datu bāzē. Asinhronais klientu izveides režīms neietekmē Commerce galvenās pārvaldības sniegumu. Katram jaunajam asinhronajam klienta ierakstam tiek piešķirts vispārēji unikāls identifikators (GUID), kuru izmanto kā klienta konta ID. Šis GUID netiek rādīts POS lietotājiem. Tā vietā šie lietotāji kā klienta konta ID redzēs **Gaida sinhronizāciju**. 

### <a name="convert-async-customers-to-sync-customers"></a>Asinhrono klientu konvertēšana par sinhronajiem

Lai pārvērstu asinhronos klientus par sinhronajiem klientiem, vispirms ir jāpalaiž **P-darbs**, lai nosūtītu asinhronos klientus uz Commerce galveno pārvaldi. Pēc tam palaidiet uzdevumu **Sinhronizēt klientus un biznesa partnerus no asinhronā režīma** (iepriekš zināms kā uzdevums **Sinhronizēt klientus un biznesa partnerus no asinhronā režīma**), lai izveidotu klientu kontu ID. Visbeidzot palaidiet darbu **1010**, lai sihnrozinētu jaunos klientu kontu ID kanālos.

### <a name="async-customer-limitations"></a>Asinhrono klientu ierobežojumi

Asinhrono klientu funkcionalitātei pašlaik ir šādi ierobežojumi:

- Asinhrono klientu ierakstus nevar rediģēt, ja vien Commerce galvenajā pārvalde nav izveidots klients un jaunais klienta konta ID nav sinhronizēts atpakaļ kanālā. Tāpēc adresi nevar saglabāt asinhronajam klientam, līdz šis klients netiek sinhronizēts ar Commerce galveno pārvaldi, jo iekšēji tiek īstenota klienta adrese kā rediģēšanas darbība klienta profilā. Taču, ja ir iespējots līdzeklis **Iespējot asinhrono klientu adrešu izveidi**, klientu adreses var arī saglabāt asinhronajiem klientiem.
- Piederības nevar saistīt ar asinhronajiem klientiem. Tāpēc jaunie asinhronie klienti nemanto piederības no noklusējuma klienta.
- Asinhronajiem klientiem nevar izsniegt lojalitātes kartes, ja vien jaunais klienta konta ID nav sinhronizēts atpakaļ kanālā.
- Nevar tvert asinhrono klientu sekundārās e-pasta adreses un tālruņa numurus.

Lai gan daži no iepriekš minētajiem ierobežojumiem varētu likt jums izvēlēties klientu sinhronizēšanas opciju, Commerce darba grupa strādā, lai padarītu asinhrono klientu iespējas līdzīgākas sinhrono klientu iespējām. Piemēram, ar Commerce 10.0.22. versijas laidienu jaunais līdzeklis **Iespējos asinhrono klientu adrešu izveidi**, kuru varat iespējot darbvietā **Līdzekļu pārvaldība**, saglabā jaunizveidotās klientu adreses gan sinhronizētajiem, gan asinhronizētajiem klientiem. Lai saglabātu šīs adreses Commerce galvenās pārvaldes klientu profilā, jums ir jāizveido un jāieplāno atkārtots pakešuzdevums **P-darbam**, uzdevumam **Sinhronizēt klientus un biznesa partnerus no asinhronā režīma** (iepriekš zināms kā uzdevums Sinhronizēt klientus un biznesa partnerus no asinhronā režīma) un uzdevumam **1010**, lai jebkādi asinhronie klienti Commerce galvenajā pārvaldē tiktu konvertēti par sinhronajiem klientiem.

### <a name="customer-creation-in-pos-offline-mode"></a>Klientu izveide POS bezsaistes režīmā

Katru reizi, kad POS ir bezsaistē, sistēma automātiski izveido klientu asinhroni pat, ja ir atspējots asinhronas klientu izveidnes režīms. Tāpēc, kā minēts iepriekš, Commerce galvenās pārvaldes administratoriem ir jāizveido un jāieplāno atkārtots pakešuzdevums **P-darbam**, uzdevumam **Sinhronizēt klientus un biznesa partnerus no asinhronā režīma** (iepriekš zināms kā uzdevums Sinhronizēt klientus un biznesa partnerus no asinhronā režīma) un uzdevumam **1010**, lai jebkādi asinhronie klienti Commerce galvenajā pārvaldē tiktu konvertēti par sinhronajiem klientiem.

> [!NOTE]
> Ja opcija **Filtra kopīgotās klientu datu tabulas** ir iestatīta uz **Jā** lapā **Commerce kanālu shēma** (**Retail un Commerce\>Galvenās pārvaldes iestatīšana\>Commerce plānotājs\>Kanālu datu bāzes grupa**), klienta ieraksti netiek izveidoti POS bezsaistes režīmā. Papildinformāciju skatiet tēmā [Datu izņemšana bezsaistē](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Papildu resursi

[Debitora atribūti](dev-itpro/customer-attributes.md)

[Datu izslēgšana bezsaistē](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
