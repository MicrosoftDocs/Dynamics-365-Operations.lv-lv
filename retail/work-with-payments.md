---
title: "Maksājumu metodes zvanu centrā"
description: "Šajā tēmā ir aprakstītas dažādās maksājumu metodes, ko mazumtirdzniecībā un komercijā varat izmantot zvanu centrā."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 636d83ecc7732a164924352853603588cded0db4
ms.lasthandoff: 03/31/2017


---

# <a name="payment-methods-in-a-call-center"></a>Maksājumu metodes zvanu centrā

[!include[banner](includes/banner.md)]


Šajā tēmā ir aprakstītas dažādās maksājumu metodes, ko mazumtirdzniecībā un komercijā varat izmantot zvanu centrā.

Maksājumu metodes, kuras programmatūras Microsoft Dynamics AX modulī Mazumtirdzniecība un komercija tiek izmantotas citos kanālos, piemēram, skaidru naudu, čekus, kredītkartes un dāvanu kartes, var izmantot arī zvanu centros. Pēc zvanu centra maksājuma metodes iestatīšanas tā tiek rādīta zvanu centra lietotājiem kā viena no opcijām lapas **Pārdošanas pasūtījums** sadaļā **Maksājumi**. Turklāt varat iestatīt kuponus, lai piedāvātu atlaides debitoriem, kas veic pasūtījumu jūsu organizācijas zvanu centrā. Kuponi var būt par fiksētas summas atlaidi vai par procentiem no krājuma cenas vai pasūtījuma kopsummas. Piemēram, no summas atkarīgs kupons var debitoriem piedāvāt atlaidi 75,00, ja debitors iztērē vismaz 750,00. Varat izveidot dažādus kuponu tipus, iestatīt pamata/pakārtotos kuponus, un kuponus kopēt vai anulēt. Lai izveidotu kuponus, izmantojiet nākamajā tabulā aprakstītas opcijas.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Atribūts**             | Laukā **Izpirkšanas ātrums ** ievadiet paredzēto kupona izpirkšanas ātruma vērtību procentos un pēc tam atlasiet, vai šo kuponu var izmantot kā vienreizējas izmantošanas kuponu, vai tas automātiski tiks izdots atkārtoti un vai tas attiecas uz noteiktu debitoru.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Derīgs**                 | Laukos **Sākuma datums** un **Beigu datums** ievadiet pirmos un pēdējos datumus, kad kupons ir derīgs.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Ietvert/izslēgt kārtulas** | Laukos **Katalogi** un **Krājumi** atlasiet, vai kuponā ietvert vai izslēgt jebkādus katalogus vai krājumus. Ja atzīmējat **Ietvert** vai **Izslēgt**, noklikšķiniet uz **Iestatīt**, atlasiet vienumu **Ietvert/izslēgt katalogus** vai **Ietvert/izslēgt preces** un ievadiet informāciju par šo katalogu vai krājumu. Ja šajos laukos atlasāt **Nav**, kuponā tiek iekļauti visi katalogi vai krājumi.                                                                                                                                                                                                                          |
| **Dažādi**         | Ja šo kuponu nevar izmantot kopā ar citām atlaidēm, atzīmējiet izvēles rūtiņu **Ekskluzīvs**. Pēc tam laukā **Izcelsme** atlasiet, kur šo kuponu var izmantot. Ja šis kupons ir ražotāja kupons, atzīmējiet izvēles rūtiņu **Ražotāja kupons**.                                                                                                                                                                                                                                                                                                                                                                |
| **Nākotnē izmantojams kupons**         | Ja šis kupons tiks saistīts ar citiem kuponiem kā pamata kupons, atzīmējiet izvēles rūtiņu **Pamata kupons**. Ja šis kupons ir jāsaista ar esošu kuponu kā pakārtots kupons, atlasiet pamata kuponu laukā **Pamata kupona ID**. Piemēram, izveidojiet kuponu gaidāmajam pavasara katalogam. Visi pārējie kuponi, ko izveidojat pavasara katalogam, būs pavasara kataloga kupona pakārtotie kuponi. Pakārtotajos kuponos var ietvert 20 procentu atlaidi jauniem debitoru pasūtījumiem, 10 procentu atlaidi nesen izdotam krājumam vai atlaidi 95,00 apmērā pasūtījumiem par 1000,00 vai lielāku summu. |

Ja iesniedzat kredītkartes maksājumu lapā **Pārdošanas pasūtījums** un saņemt ziņojumu, kurā norādīts, ka karte nebija autorizēta, šo autorizāciju varat apstrādāt manuāli. Kredītkartes transakciju varat autorizēt, noraidīt vai iesniegt atkārtoti, izmantojot lapu **Autorizācijas pārvaldība**. Zvanu centra parametru lapu jūs izmantojat, lai konfigurētu papildu maksājumu apstrādes iespējas:

-   Čeku aizturējumi ļauj finanšu personālam apstrādāt pasūtījumus, kas ir aizturēti, jo kā maksāšanas metode tika izmantots čeks un tika pārsniegta čeka aizturēšanas sliekšņa summa. Šo aizturēšanu var manuāli atbrīvot, vai tās derīgums automātiski beidzas konfigurētā perioda beigās.
-   Varat iestatīt sliekšņus, virs kuriem ir manuāli jāapstiprina tādas atmaksas, kas tiek izsniegtas, izmantojot čekus un kredītkartes. Jebkura kompensācija, kas pārsniedz sliekšņa summu, tiek pievienota apstiprināšanas rindai. Kad atmaksa ir apstiprināta, par atgriešanas pārdošanas pasūtījumu var izrakstīt rēķinu.





