---
title: Datu agnostiskā testēšana, izmantojot Regression Suite Automation Tool
description: Šajā rakstā ir apskatīti ieteikumi datu diagnostikai, izmantojot Regression Suite Automation Tool.
author: FrankDahl
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.custom: 21761
ms.openlocfilehash: f4322cb76d1d83c02ec9d4dcb997a1cd4730d090
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269597"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Datu agnostiskā testēšana, izmantojot Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

Lai gan ERP lietojumprogrammas funkcionālā validācija nevar būt pilnībā datu agnostika, ir vairāki testēšanai paredzēti posmi un pieejas. Šīs testēšanas fāzes ietver:  

- SysTest struktūra
- ATL struktūra
- Regression Suite Automation Tool (RSAT)

[![Testa klasifikācijas piramīda.](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>Pārskats
-   **SysTest struktūra** — SysTest struktūra ir uzticama vienību testu rakstīšanai. Tā kā vienību testi parasti pārbauda metodi vai funkciju, tiem vienmēr ir jābūt datiem agnostiskiem, un tie ir atkarīgi tikai no ievadītajiem datiem, kas tiek sniegti kā daļa no testa.
-   **ATL struktūra** -Microsoft ir ATL struktūra, kas ir SysTest struktūras abstrakcija un padara funkcionālu testu rakstīšanu daudz vienkāršāku un uzticamāku. Šī struktūra jāizmanto, lai rakstītu komponentu testus vai vienkāršus integrēšanas testus.
-   **RSAT** – RSAT izmanto integrācijas testiem un biznesa cikla testiem. Biznesa cikla testi, ko sauc arī par regresijas validācijas testiem, ir atkarīgi no esošajiem datiem. Tomēr šie testi var kļūt par datu agnostiskiem, ja tiek ņemti vērā papildu faktori. 

    - Ja vienību un komponentu testi ir zemā līmenī un var pilnībā būt datu agnostiski (neatkarīgi no esošas datu kopas), biznesa cikla vai regresijas pārbaudes testi ir atkarīgi no dažiem esošajiem datiem. Šie dati ietver iestatījumus, konfigurācijas iestatījumus (parametrus) un pamatdatus (klients, kreditori, krājumi utt.), bet ne darbību datus. Pārliecinieties, ka testa laikā, ja kāds no tiem tiek mainīts, tie tiek atgriezti atpakaļ kā daļa no galīgā testa.
    - Atlasiet pamatdatus, pamatojoties uz noteiktiem kritērijiem, nevis pēc konkrēta ieraksta atlases. Piemēram, ja vēlaties atlasīt preci, pamatojoties uz tā dimensijas vērtībām un krājumu pieejamību, filtrējiet produktu sarakstu ar šīm vērtībām, atlasiet pirmo preci un kopējiet numuru, ko izmantosiet turpmākām pārbaudēm. Ja tā ir vienkārša pamatdatu rinda, piemēram, klientu, piegādātāju vai preču rinda, to var izveidot kā daļu no automatizācijas un izmantot turpmākajās pārbaudēs ar ķēžu metodes palīdzību. 
    - Ievadiet unikālos identifikatorus, piemēram, rēķina numurus ar numuru sēriju vai izmantojot tādas Microsoft Excel funkcijas kā =TEXT(NOW(),"yyyymmddhhmm"). Šī funkcija nodrošinās unikālu numuru katru minūti, kas ļauj izsekot, kad darbība notikusi. To var izmantot mainīgajiem, piemēram, produktu ieejas plūsmas numuriem un piegādātāju rēķinu numuriem. Šie testi turpina nemainīgi strādāt ar to pašu datu bāzi bez nepieciešamības to atjaunot.
    - Vienmēr iestatiet vides **Rediģēšanas režīmu**, lai to varētu **Lasīt** vai **Rediģēt** kā pirmo pārbaudes gadījumu, jo noklusētā opcija ir **Automātiski**. Opcija **Automātiski** vienmēr izmanto iepriekšējos iestatījumus un var izraisīt neuzticamus testus. 
 
    [![Iespēju lapa, veiktspējas cilne.](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - Apstipriniet tikai pēc tam, kad izfiltrējat noteiktu darbību, nevis veicat vispārēju pārbaudi. Piemēram, ierakstu skaitam filtrējiet darbības numuru vai darbības datumu, lai validācija neiekļautu visas citas darbības. 
    - Ja pārbaudāt klientu bilanci vai budžetu, vispirms saglabājiet vērtību un pēc tam pievienojiet savu darbību vērtību, lai apsiprinātu gaidāmo rezultātu, nevis pārbaudītu fiksēto paredzamo vērtību. 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
