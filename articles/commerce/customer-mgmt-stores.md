---
title: Klientu pārvaldība veikalos
description: Šajā tēmā paskaidrots, kā mazumtirgotāji var iespējot klientu pārvaldības iespējas pārdošanas punktā (POS) risinājumā Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 05/25/2021
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
ms.openlocfilehash: dd17593d84a8bf262712a84b11829f8ec6c49049
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097212"
---
# <a name="customer-management-in-stores"></a>Klientu pārvaldība veikalos

[!include [banner](includes/banner.md)]

Šajā tēmā paskaidrots, kā mazumtirgotāji var iespējot klientu pārvaldības iespējas pārdošanas punktā (POS) risinājumā Microsoft Dynamics 365 Commerce.

Ir būtiski, ka veikala asistenti var izveidot un rediģēt klientu ierakstus pārdošanas punktā. Tādējādi viņi var fiksēt jebkādus klienta informācijas atjauninājumus, piemēram, e-pasta adresi, tālruņa numura vai adreses maiņu. Šī informācija noder lejupstraumes sistēmās, piemēram, mārketingā, jo šo sistēmu efektivitāte ir atkarīga no klientu datu precizitātes.

Pārdošanas asistenti var aktivizēt klientu izveides darbplūsmu no diviem POS ievades punktiem. Viņi var atlasīt pogu, kas tiek kartēta uz operāciju **Klienta pievienošana**, vai viņi var lietojumprogrammas joslā meklēšanas rezultātu lapā atlasīt **Izveidot klientu**. Abos gadījumos tiek parādīts dialoglodziņš **Jauns klients**, kurā pārdošanas asistenti var ievadīt nepieciešamos klienta datus, piemēram, klienta vārdu un uzvārdu, e-pasta adresi, tālruņa numuru, adresi un jebkādu papildu informāciju, kura ir saistoša biznesam. Papildu informāciju var fiksēt, izmantojot tos klienta atribūtus, kuri ir saistīti ar klientu. Papildinformāciju par klientu atribūtiem skatiet rakstā [Klienta atribūti](dev-itpro/customer-attributes.md).

Pārdošanas asistenti var arī fiksēt sekundāras e-pasta adreses un tālruņa numurs. Turklāt viņi var tvert klienta preferences attiecībā uz mārketinga informācijas saņemšanu, izmantojot jebkuru no sekundārajām e-pasta adresēm vai tālruņa numuriem. Lai iespējotu šo iespēju, mazumtirgotājiem ir Commerce galvenās pārvaldes darbvietā **Līdzekļu pārvaldība** jāiespējo līdzeklis **Tvert vairākus e-pastus un tālruņa numurus un saņemt piekrišanu mārketingam uz šo kontaktinformāciju** (**Sistēmu pārvaldība\>Darbvietas\>Līdzekļu pārvaldība**).

## <a name="default-customer-properties"></a>Klienta noklusējuma rekvizīti

Mazumtirgotāji var izmantot Commerce galvenās pārvaldes lapu **Visi veikali** (**Retail un Commerce\>Kanāli\>Veikali**), lai saistītu noklusējuma klientu ar katru veikalu. Pēc tam Commerce kopē noklusējuma klientam definētos līdzekļus uz visiem jaunajiem izveidotajiem klienta ierakstiem. Piemēram, dialoglodziņš **Izveidot klientu** rāda rekvizītus, kuri tiek mantoti no noklusējuma klienta, kas tiek saistīts ar veikalu. Šie rekvizīti ietver **klienta veidu**, **klienta grupu**, **rēķina opciju**, **rēķina e-pastu**, **valūtu** un **valodu**. Jebkādas **piederības** (klientu kopas) arī tiek mantotas no noklusējuma klienta. Taču **finanšu dimensijas** tiek mantotas no tās klientu grupas, kura ir saistīta ar noklusējuma klientu, nevis no paša noklusējuma klienta.

> [!NOTE]
> **Rēķina e-pasta** vērtība tiek kopēta no noklusējuma klienta tikai tad, ja jaunizveidotajiem klientiem nav norādīts rēķina e-pasta ID. Tas nozīmē, ka, ja rēķina e-pasta ID ir uz noklusējuma klienta, tad visi klienti, kas izveidoti no e-komercijas vietnes, saņems tādu pašu rēķina e-pasta ID, jo nav lietotāja interfeisa, lai tvertu kvīts e-pasta ID no klienta. Ieteicams saglabāt **rēķina e-pasta** lauku tukšu veikala noklusējuma klientam un izmantot to tikai tad, ja jums ir biznesa process, kas ir atkarīgs no rēķina e-pasta adreses. 

Pārdošanas asistenti var tvert vairākas klienta adreses. Klienta vārds, uzvārds un tālruņa numurs tiek mantots no kontaktinformācijas, kura ir saistīta ar katru adresi. Klienta ieraksta kopsavilkuma cilne **Adreses** ietver lauku **Mērķis**, kuru pārdošanas asistents var rediģēt. Ja klienta veids ir **Persona**, noklusējuma vērtība ir **Mājas**. Ja klients veids ir **Organizācija**, noklusējuma vērtība ir **Bizness**. Citas šī lauka atbalstītās vērtības ietver **Mājas**, **Birojs** un **Pastkaste**. Lauka **Valsts** vērtība adresei tiek mantota no primārās adreses, kura tiek norādīta Commerce galvenās pārvaldes lapā **Pārvaldības struktūrvienība**, dodoties uz **Organizācijas pārvaldība\>Organizācijas\>Pārvaldības struktūrvienības**.

## <a name="sync-customers-and-async-customers"></a>Klientu sinhronizēšana un asinhronizēšana

Risinājumā Commerce ir divi klientu izveides režīmi: sinhronā un asinhronā. Klienti pēc noklusējuma tiek izveidoti sinhroni. Citiem vārdiem sakot, tos izveido Commerce galvenajā pārvaldē reāllaikā. Sinhronizētais klientu izveides režīma priekšrocība ir tas, ka jaunos klientus var nekavējoties meklēt visos kanālos. Taču šim režīmam ir arī trūkums. Tā kā tas uz Commerce galveno pārvaldi ģenerē zvanus [Commerce Data Exchange: Reāllaika pakalpojums](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service), var tikt ietekmēts sniegums, ja secīgi tiek veikti vairāki klientu izveides zvani.

Ja opcija **Izveidot klientu asinhronajā režīmā** ir iestatīta uz **Jā** veikala funkcionalitātes profilā (**Retail un Commerce\>Kanāla iestatīšana\>Tiešsaistes veikala iestatīšana\>Funkcionalitātes profili**), reāllaika pakalpojuma zvani netiek izmantoti klientu ierakstu izveidei kanāla datu bāzē. Asinhronais klientu izveides režīms neietekmē Commerce galvenās pārvaldības sniegumu. Katram jaunajam asinhronajam klienta ierakstam tiek piešķirts vispārēji unikāls identifikators (GUID), kuru izmanto kā klienta konta ID. Šis GUID netiek rādīts POS lietotājiem. Tā vietā šie lietotāji kā klienta konta ID redzēs **Gaida sinhronizāciju**. Lai gan šī konfigurācija liek klientus izveidot asinhroni, ņemiet vērā, ka klientu ierakstu labojumi vienmēr tiek veikti sinhroni.

### <a name="convert-async-customers-to-sync-customers"></a>Asinhrono klientu konvertēšana par sinhronajiem

Lai asinhronos klientus konvertētu par sinhronajiem, vispirms ir jāpalaiž P-darbs, lai asinhronos klientus nosūtītu uz Commerce galveno pārvaldi. Pēc tam palaidiet darbu **Klientu un biznesa partneru sinhronizēšana no asinhronā režīma**, lai izveidotu klientu kontu ID. Visbeidzot palaidiet darbu **1010**, lai sihnrozinētu jaunos klientu kontu ID kanālos.

### <a name="async-customer-limitations"></a>Asinhrono klientu ierobežojumi

Asinhrono klientu funkcionalitātei pašlaik ir šādi ierobežojumi:

- Asinhrono klientu ierakstus nevar rediģēt, ja vien Commerce galvenajā pārvalde nav izveidots klients un jaunais klienta konta ID nav sinhronizēts atpakaļ kanālā.
- Piederības nevar saistīt ar asinhronajiem klientiem. Tāpēc jaunie asinhronie klienti nemanto piederības no noklusējuma klienta.
- Asinhronajiem klientiem nevar izsniegt lojalitātes kartes, ja vien jaunais klienta konta ID nav sinhronizēts atpakaļ kanālā.
- Nevar tvert asinhrono klientu sekundārās e-pasta adreses un tālruņa numurus.

### <a name="customer-creation-in-pos-offline-mode"></a>Klientu izveide POS bezsaistes režīmā

Ja POS ir bezsaistē, kamēr ir iespējots asinhronā klienta izveides režīms, jaunie klienta ieraksti tiek izveidoti asinhroni. Ja POS ir bezsaistē, kamēr ir atspējots asinhronais klientu izveides režīms, sistēma automātiski pārslēdzas uz asinhrono klienta izveides režīmu. Citiem vārdiem sakot, klienta ierakstus var izveidot asinhroni pat, ja ir atspējots asinhronā klienta izveides režīms. Tāpēc Commerce galvenās pārvaldes administratoriem ir jāizveido un jāplāno periodisks pakešuzdevums P-darbam, darbam **Sinhronizēt klientus un biznesa partnerus no asinhronā režīma** un darbam **1010**, lai asinhronizētie klienti Commerce galvenajā pārvaldē tiktu konvertēti uz sinhronajiem klientiem.

> [!NOTE]
> Ja opcija **Filtra kopīgotās klientu datu tabulas** ir iestatīta uz **Jā** lapā **Commerce kanālu shēma** (**Retail un Commerce\>Galvenās pārvaldes iestatīšana\>Commerce plānotājs\>Kanālu datu bāzes grupa**), klienta ieraksti netiek izveidoti POS bezsaistes režīmā. Papildinformāciju skatiet tēmā [Datu izņemšana bezsaistē](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Papildu resursi

[Debitora atribūti](dev-itpro/customer-attributes.md)

[Datu izslēgšana bezsaistē](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
