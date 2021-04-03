---
title: Maksājuma atlaižu apstrāde
description: Šajā procedūrā parādīts, kā pārvērst apstiprinātas un apstrādātas debitora atlaides par kredīta notām.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617b5d99973e630cca2973227c2e54a63bd1ec4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263304"
---
# <a name="process-rebates-for-payment"></a>Maksājuma atlaižu apstrāde

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā pārvērst apstiprinātas un apstrādātas debitora atlaides par kredīta notām. Šo ceļvedi var lietot ar demonstrācijas uzņēmumu USMF. Šajā ceļvedī priekšnoteikums ir viena vai vairākas atlaides prasības ar statusu Atzīmēt. Ja izmantojat USMF, pirms šī ceļveža izpildes ieteicams palaist ceļvedi "Debitora atlaižu ģenerēšana un apstrāde".


## <a name="convert-rebate-claims-to-credit-note"></a>Atlaides prasības pārveidošana kredīta notā
1. Dodieties uz Visi debitori.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Darbību rūtī noklikšķiniet uz Iekasēt.
5. Noklikšķiniet uz Transakciju nosegšana.
6. Noklikšķiniet uz Funkcijas.
7. Noklikšķiniet uz Atlaižu programma.
    * Lapā Atlaide uzskaitītas atlaižu prasības, kuras esat apstrādājis debitora atlaižu rīkā un kurām ir statuss Atzīmēt.    
8. Noklikšķiniet uz Rediģēt.
    * Iestatiet atzīmes laukā Atzīmēt prasībām, ko vēlaties iekļaut kredīta notā.   
9. Noklikšķiniet uz Funkcijas.
10. Noklikšķiniet uz Izveidot kredīta notu.
    * Tiek parādīts ziņojums, lai paziņotu, ka žurnāls ir iegrāmatots (tas ir Debitoru parādu patēriņa žurnāls, kā norādīts lapā Debitoru moduļa parametri). Šī iemesla dēļ reāla pasīvu (kredīta) summa tiek pārvietota uz debitora bilanci. Tas nozīmē, ka klients konts tika debetēts un Atlaižu uzkrājumu konts tiek kreditēts.  
11. Aizvērt lapu.
12. Noklikšķiniet uz Atcelt.
    * Tas atsvaidzina lapu, lai varētu redzēt atjauninājumus.  
13. Darbību rūtī noklikšķiniet uz Iekasēt.
14. Noklikšķiniet uz Transakciju nosegšana.
    * Ņemiet vērā, ka transakcija ar negatīvu summu, kas atspoguļo kopējo atlaižu summu, bez rēķina atsauces tika pievienota debitora bilancei.   
15. Noklikšķiniet uz Atcelt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]