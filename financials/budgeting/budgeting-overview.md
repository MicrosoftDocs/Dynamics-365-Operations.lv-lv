---
title: "Budžeta veidošanas sākumlapa"
description: "Šajā tēmā ir sniegts apskats par budžeta veidošanas funkcionalitātes sastāvdaļām, budžeta veidošanas rīkiem, kā arī atskaišu veidošanas iespējām programmatūrā Microsoft Dynamics 365 for Operations."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: index-page
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: dd17842365e357ecb5cb6034ed8878fcd60be5fc
ms.openlocfilehash: aacce0449c9490c4ab66cacb9945ed64fa40de34
ms.contentlocale: lv-lv
ms.lasthandoff: 04/26/2017


---

# <a name="budgeting-home-page"></a>Budžeta veidošanas sākumlapa

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegts apskats par budžeta veidošanas funkcionalitātes sastāvdaļām, budžeta veidošanas rīkiem, kā arī atskaišu veidošanas iespējām programmatūrā Microsoft Dynamics 365 for Operations. 

<a name="components-of-budgeting-functionality"></a>Budžeta veidošanas funkcionalitātes komponenti
-------------------------------------

Resursu plānošanas cikls uzņēmumam parasti sastāv no plānošanas, budžeta veidošanas un prognozēšanas darbībām.
[![Budžeta veidošanas funkcionalitātes komponenti](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg) Gan ilgtermiņa stratēģiskās plānošanas, gan gada budžeta plānošanas procesi tiek atbalstīti, izmantojot budžeta plāna dokumentu. Budžeta plāna dokumenti ir cieši integrēti programmā Microsoft Excel. Lietotāji var konfigurēt neierobežotus naudas un daudzuma scenārijus, kā arī var definēt budžeta plānošanas organizācijas hierarhiju, lai atbalstītu budžeta veidošanu gan no augšas uz leju, gan no apakšas uz augšu. Kad budžets ir izveidots un apstiprināts programmatūrā Microsoft Dynamics 365 for Operations, jūs šo budžeta plānu pārveidojat par budžeta reģistra ierakstu. Budžeta reģistra ieraksti nodrošina rīkus budžeta uzturēšanai un summu izsekojamības saglabāšanai, izmantojot budžeta kodus. Budžeta reģistra ieraksti ļauj pārskatīt sākotnējos budžetus, veikt pārsūtījumus un pārnest budžeta summas no iepriekšējā gada. Pamatojoties uz izveidoto budžetu, uzņēmums var iespējot budžeta kontroli. Kontroles līmenis ir atkarīgs no organizācijas kultūras un organizācijas brieduma līmeņa. Organizācijas, kurām ir zems brieduma līmenis, var atstāt budžetu “tādu, kāds tas ir” un spēt labāk reaģēt, nevis darboties proaktīvi, ja budžets neatbilst gaidītajam. Citas organizācijas var iespējot budžeta kontroles politikas, kas neļauj lietotājiem veikt pirkšanu, ja nav pieejami budžeta līdzekļi. Visbeidzot — ļoti nobriedušām organizācijām var būt izveidota organizācijas kultūra, kurā darbinieki tiek izglītoti par organizācijas mērķiem un cenšas sasniegt šos mērķus, izmantojot tādas politikas kā, piemēram, “apsvērt iespēju tikties tiešsaistē, nevis doties komandējumā”. Programmatūra Dynamics 365 for Operations ietver budžeta kontroles struktūru, kas uzņēmuma vadībai ļauj izvēlēties stingru kontroli (kas liedz veikt grāmatojumus, kuri pārsniegtu budžetu) vai vāju kontroli (kuras ietvaros lietotāji tiek brīdināti, ka viņi pārsniegs pieejamos budžeta līdzekļus, bet var paši pieņemt lēmumu par turpmāku rīcību). Visbeidzot — varat izmantot slīdošās prognozes. Slīdošā prognoze ir regulāra budžeta un faktisko datu salīdzināšana, un tā tiek izmantota, lai definētu, cik labi uzņēmums darbojas, salīdzinot ar budžeta datiem. Slīdošā prognoze tiek izmantota, arī lai noteiktu tendences. Programmatūrā Microsoft Dynamics 365 for Operations slīdošās prognozes tiek atbalstītas ar budžeta plāna dokumenta starpniecību kā sākotnējās plānošanas aktivitātes. Slīdošās prognozes var veikt vienlaicīgi ar plānošanu gaidāmajam budžeta ciklam.

-   [Pamata budžeta veidošana: pārskats un konfigurācija](basic-budgeting-overview-configuration.md)
-   [Budžeta kontrole: pārskats un konfigurācija](budget-control-overview-configuration.md)
-   [Budžeta plānošana: pārskats un konfigurācija](budget-planning-overview-configuration.md)
-   [Pozīciju prognozēšana](position-forecasting.md)
-   [Budžeta plānošanas attaisnojuma dokumenti](budget-planning-justification-docs.md)
-   [Microsoft Excel veidnes budžeta plānošanai](budget-planning-excel-templates.md)

## <a name="budgeting-tools-in-dynamics-365-for-operations"></a>Budžeta veidošanas rīki programmatūrā Dynamics 365 for Operations
[![Budžeta veidošanas rīki](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Papildu plānošanas un budžeta veidošanas iespējas ir pieejamas visā programmatūrā Dynamics 365 for Operations, un tās ir iestrādātas virsgrāmatas budžetos.

-   **Darbaspēka budžeti** — darbaspēka budžeta veidošana ietver detalizētu budžeta izmaksu komponentu plānošanu amatiem, atlīdzības grupām un tā tālāk.
-   **Pamatlīdzekļu budžeti** — pamatojoties uz pamatlīdzekļu informāciju, varat aprēķināt plānoto nolietojumu un reģistrēt citas plānotās transakcijas, kas ir saistītas ar pamatlīdzekļiem.
-   **Projektu budžeti** — projektu modulī varat izveidot detalizētas projekta prognozes. Projektu prognozes ietver detalizētu informāciju par plānotajām stundām, izdevumiem, maksām un krājumiem.
-   **Pieprasījuma prognozēšana** — pamatojoties uz vēsturiskiem transakciju datiem, varat prognozēt turpmāko krājumu pieprasījumu un izveidot pieprasījuma apjoma prognozes.

Papildinformāciju par to, kā plānošanas datus no citiem moduļiem pārnest uz budžeta plāniem, skatiet rakstā [Budžeta plānošanas integrācija ar citiem moduļiem](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Lietotāja interfeiss un pārskatu veidošanas iespējas
Programmatūrā Dynamics 365 for Operations lietotāji var izveidot budžeta plānus tieši Dynamics 365 for Operations klientā (izmantojot konfigurējamu budžeta plāna dokumentu lapu) vai ar programmas Excel starpniecību. Programma Excel nodrošina vairākas papildu iespējas. Piemēram, kā budžeta plāna avotu varat izmantot ārējus datus, veikt pielāgotus aprēķinus un izmantot Microsoft rakurstabulas un diagrammas. Lielāko daļu no mainīgajām vērtībām budžeta plānošanas procesā var konfigurēt. Piemēram, var definēt budžeta veidošanas veicēju, to, kam tiek veidots budžets, kā arī to, kā izskatās process. Lai arī budžeta plānošanai varat izmantot programmu Excel, programmatūra Dynamics 365 for Operations tiek uzskatīta par vienīgo patiesās informācijas avotu un palīdz novērst budžeta kontroles problēmas. Periodiskos procesus var izmantot, lai iekļautu budžeta veidošanas sākotnējos datus budžeta plānā. Pārskatu veidošanai programmatūra Dynamics 365 for Operations piedāvā standarta uzziņas lapu kopumu, kas jums ļauj skatīt un analizēt budžeta veidošanas datus. Budžeta plāna datiem var piekļūt, izmantojot pārvaldības atskaišu sastādītāju, un atsevišķus budžeta plāna scenārijus pārvaldības atskaišu sastādītāja atskaitēs var parādīt kā kolonnas.






