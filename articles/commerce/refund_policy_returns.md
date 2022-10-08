---
title: Izveidot un atjaunināt kanāla atgriešanas un atmaksas politiku
description: Šajā rakstā ir izskaidrots, kā iestatīt atgriešanas un atmaksas politiku kanālam.
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: d01ad490301dd2f4103b8bd3f702db12b93a45a8
ms.sourcegitcommit: bd7b1ffe90b25eb4c68d6aaebd063bf33e09d9cd
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/05/2022
ms.locfileid: "9627501"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Izveidot un atjaunināt kanāla atgriešanas un atmaksas politiku

[!include [banner](includes/banner.md)]

Kanāla atgriešanas politika Dynamics 365 Commerce ļauj mazumtirgotājiem iestatīt izpildi attiecībā uz to, kurus maksājumu norēķinus var izmantot atgriešanas apstrādei pārdošanas punkta (POS) ierīcē.  

Šajā rakstā ir aprakstītas darbības, lai iestatītu atgriešanas un atmaksas politiku kanālam.

Politikas darbības sfēra pašlaik ir ierobežota, nosakot maksājuma norēķinus, ko var atļaut kanālam. "Atļauto" saraksts ir balstīts uz maksājuma metodēm, kas izmantotas, lai veiktu pirkumu. Piemēram:

- Ja pirkums tika veikts, izmantojot dāvanu karti, veikala politika ir apstrādāt atmaksu tikai uz jaunu dāvanu karti vai sniegt veikala kredītu. 
- Ja pārdošana ir veikta, izmantojot skaidru naudu, atmaksai atļautās opcijas ir skaidra nauda, dāvanu kartes un debitora konts, taču ne kredītkarte. 

## <a name="enable-return-policy"></a>Atgriešanas politikas iespējošana

Šī funkcija pēc noklusējuma ir ieslēgta. To var atrast līdzekļu pārvaldības **darbvietā**, meklējot iespējot **kanāla atgriešanas politikas** līdzekļu nosaukumu sarakstā.


## <a name="configure-return-policy"></a>Atgriešanas politikas konfigurēšana

Veiciet šīs darbības, lai konfigurētu atgriešanas politiku mazumtirdzniecības veikalam vai tiešsaistes mazumtirdzniecības kanālam.

1. Dodieties uz **Retail un Commerce** \> **Kanāla iestatīšana** \> **Atgriešana** \> **Kanāla atgriešanas politika**.

1. Atlasiet **Jauns**, lai izveidotu atgriešanas politikas veidni. Lai izmantotu esošu veidni, atlasiet veidni kreisajā rūtī. Jaunām veidnēm pievienojiet nosaukumu un aprakstu, kas palīdzēs identificēt politiku, kad tā tiek piemērota kanālam.

   ![Pievienot jaunu atgriešanas politiku.](media/Return-policy-page1.png)
     
   
1. Sadaļā **Atļautās atmaksas maksājumu metodes** definējiet **atļautos** atgriešanas maksājumu norēķinus, kas ir specifiski katrai maksājuma metodei.
   ![Iestatīt atļautās maksājuma metodes maksājuma veidam.](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - Maksāšanas metodes tiek atvasinātas no organizācijai iestatītajām maksāšanas metodēm.
    > - Pievienojot atļauto atgriešanas norēķinu tipu katrai uzskaitītajai maksāšanas metodei, tiek nodrošināts, ka atgriešanu var veikt atļautajam atgriešanas norēķinu veidam.
    
1. Saistiet atgriešanas politikas veidni ar veikaliem, kur tā tiks izmantota. Atlasiet **Pievienot** cilnē **Mazumtirdzniecības kanāli** un saistiet pieejamos kanālus. 

    - Dialoglodziņā **Izvēlēties organizācijas mezglus**, atlasiet veikalus, reģionus un organizācijas, ar kurām veidne jāsaista.
    - Ar katru veikalu var saistīt tikai vienu atgriešanas politikas veidni.
    - Izmantojiet bulttaustiņus, lai atlasītu veikalus, reģionus vai organizācijas.
    - Politikas Spēkā stāšanās datumsir datums, kurā politika tiek piemērota kanāliem un tiek izpildīti kanāla darbi. 

    ![Izvēlēties organizācijas zaru dialoglodziņu.](media/Return-policy-page3.png)

1. Lapā **Sadales grafiks** palaidiet **1070** darbu, lai kanāla atgriešanas politika būtu pieejama POS.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Priekšskatīt kanāla atgriešanas politiku POS

Lai skatītu atļautos atgriešanas norēķinu tipus POS, veiciet kādā no nākamajiem piemēriem norādītās darbības.

1. Piesakieties POS kā kasieris vai menedžeris.
1. Sadaļā **Maiņa un atvilktne** atlasiet **Rādīt žurnālu.**
1. Atlasiet transakciju, kas ir daļa no atgriešanas. 
1. Atlasiet atgriežamos krājumus un izvēlieties maksājuma metodi.  
    - Ja izvēlētais maksājuma norēķins ir atļauto atgriešanas norēķinu tipu sarakstā, kasieris var pabeigt darbību.
    - Ja atlasītais maksājuma norēķins nav atļauts, tiek parādīts kļūdas ziņojums.
    - Izvēlieties **Summa apmaksai**, lai parādītu sarakstu ar visiem atļautajiem atgriešanas norēķinu veidiem.

- vai -

1. Piesakieties POS kā kasieris vai menedžeris.
1. Atlasiet **Atgriešanas transakcija** un ievadiet saņemšanas ID, izmantojot svītrkoda skenēšanu vai manuālu ievadi. 
1. Atlasiet transakciju, kas ir daļa no atgriešanas. 
1. Atlasiet atgriežamos krājumus un izvēlieties maksājuma metodi.  
    - Ja izvēlētais maksājuma norēķins ir atļauto atgriešanas norēķinu tipu sarakstā, kasieris var pabeigt darbību.
    - Ja atlasītais maksājuma norēķins nav atļauts, tiek parādīts kļūdas ziņojums.
    - Izvēlieties **Summa apmaksai**, lai parādītu sarakstu ar visiem atļautajiem atgriešanas norēķinu veidiem.

![Atmaksas veids nav atļauts.](media/Return-policy-page6.png)



![Atļautie atmaksas veidi.](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
