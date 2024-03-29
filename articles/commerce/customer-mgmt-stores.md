---
title: Klientu pārvaldība veikalos
description: Šajā rakstā ir izskaidrots, kā mazumtirgotāji var iespējot debitoru pārvaldības iespējas pārdošanas punktā (POS)Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: 2928aa5c4e62611b54799fbe7c1bba25fe186bcd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282246"
---
# <a name="customer-management-in-stores"></a>Klientu pārvaldība veikalos

[!include [banner](includes/banner.md)]

Šajā rakstā ir izskaidrots, kā mazumtirgotāji var iespējot debitoru pārvaldības iespējas pārdošanas punktā (POS)Microsoft Dynamics 365 Commerce.

Ir būtiski, ka veikala asistenti var izveidot un rediģēt klientu ierakstus pārdošanas punktā. Tādējādi viņi var fiksēt jebkādus klienta informācijas atjauninājumus, piemēram, e-pasta adresi, tālruņa numura vai adreses maiņu. Šī informācija noder lejupstraumes sistēmās, piemēram, mārketingā, jo šo sistēmu efektivitāte ir atkarīga no klientu datu precizitātes.

Pārdošanas asistenti var aktivizēt klientu izveides darbplūsmu no diviem POS ievades punktiem. Viņi var atlasīt pogu, kas tiek kartēta uz operāciju **Klienta pievienošana**, vai viņi var lietojumprogrammas joslā meklēšanas rezultātu lapā atlasīt **Izveidot klientu**. Abos gadījumos tiek parādīts dialoglodziņš **Jauns klients**, kurā pārdošanas asistenti var ievadīt nepieciešamos klienta datus, piemēram, klienta vārdu un uzvārdu, e-pasta adresi, tālruņa numuru, adresi un jebkādu papildu informāciju, kura ir saistoša biznesam. Papildu informāciju var fiksēt, izmantojot tos klienta atribūtus, kuri ir saistīti ar klientu. Papildinformāciju par klientu atribūtiem skatiet rakstā [Klienta atribūti](dev-itpro/customer-attributes.md).

Pārdošanas asistenti var arī fiksēt sekundāras e-pasta adreses un tālruņa numurs. Turklāt viņi var tvert klienta preferences attiecībā uz mārketinga informācijas saņemšanu, izmantojot jebkuru no sekundārajām e-pasta adresēm vai tālruņa numuriem. Lai iespējotu šo iespēju, mazumtirgotājiem ir Commerce galvenās pārvaldes darbvietā **Līdzekļu pārvaldība** jāiespējo līdzeklis **Tvert vairākus e-pastus un tālruņa numurus un saņemt piekrišanu mārketingam uz šo kontaktinformāciju** (**Sistēmu pārvaldība\>Darbvietas\>Līdzekļu pārvaldība**).

## <a name="default-customer-properties"></a>Klienta noklusējuma rekvizīti

Mazumtirgotāji var izmantot Commerce galvenās pārvaldes lapu **Visi veikali** (**Retail un Commerce\>Kanāli\>Veikali**), lai saistītu noklusējuma klientu ar katru veikalu. Pēc tam Commerce kopē noklusējuma klientam definētos līdzekļus uz visiem jaunajiem izveidotajiem klienta ierakstiem. Piemēram, dialoglodziņš **Izveidot klientu** rāda rekvizītus, kuri tiek mantoti no noklusējuma klienta, kas tiek saistīts ar veikalu. Šie rekvizīti ietver **klienta veidu**, **klienta grupu**, **rēķina opciju**, **rēķina e-pastu**, **valūtu** un **valodu**. Jebkādas **piederības** (klientu kopas) arī tiek mantotas no noklusējuma klienta. Taču **finanšu dimensijas** tiek mantotas no tās klientu grupas, kura ir saistīta ar noklusējuma klientu, nevis no paša noklusējuma klienta.

> [!NOTE]
> **Rēķina e-pasta** vērtība tiek kopēta no noklusējuma klienta tikai tad, ja jaunizveidotajiem klientiem nav norādīts rēķina e-pasta ID. Tas nozīmē, ka, ja rēķina e-pasta ID ir uz noklusējuma klienta, tad visi klienti, kas izveidoti no e-komercijas vietnes, saņems tādu pašu rēķina e-pasta ID, jo nav lietotāja interfeisa, lai tvertu kvīts e-pasta ID no klienta. Iesakām atstāt lauku **kvīts e-pasts** tukšu veikala noklusējuma klientam un to izmantot vienīgi tad, ja jums ir biznesa process, kurš ir atkarīgs no tā, vai ir klātesoša kvīts e-pasta adrese. 

Pārdošanas asistenti var tvert vairākas klienta adreses. Klienta vārds, uzvārds un tālruņa numurs tiek mantots no kontaktinformācijas, kura ir saistīta ar katru adresi. Klienta ieraksta kopsavilkuma cilne **Adreses** ietver lauku **Mērķis**, kuru pārdošanas asistents var rediģēt. Ja klienta veids ir **Persona**, noklusējuma vērtība ir **Mājas**. Ja klients veids ir **Organizācija**, noklusējuma vērtība ir **Bizness**. Citas šī lauka atbalstītās vērtības ietver **Mājas**, **Birojs** un **Pastkaste**. Lauka **Valsts** vērtība adresei tiek mantota no primārās adreses, kura tiek norādīta Commerce galvenās pārvaldes lapā **Pārvaldības struktūrvienība**, dodoties uz **Organizācijas pārvaldība\>Organizācijas\>Pārvaldības struktūrvienības**.



## <a name="additional-resources"></a>Papildu resursi

[Asinhronā debitora izveides režīms](async-customer-mode.md)

[Asinhrono debitoru pārvēršana par sinhroniem debitoriem](convert-async-to-sync.md)

[Debitora atribūti](dev-itpro/customer-attributes.md)

[Datu izslēgšana bezsaistē](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
