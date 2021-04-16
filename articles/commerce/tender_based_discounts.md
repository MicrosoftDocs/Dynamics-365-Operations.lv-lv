---
title: Uz konkursu balstītas atlaides
description: Šī tēma sniedz apskatu par funkcionalitāti, kas ļauj mazumtirgotājiem konfigurēt atlaides noteiktiem norēķinu veidiem.
author: bebeale
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 482eb8da5777af79c791dd6841315424d101b5d0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795169"
---
# <a name="tender-based-discounts"></a>Uz konkursu balstītas atlaides

[!include [banner](includes/banner.md)]


Tā ir kopīga prakse starp mazumtirgotājiem, lai izlaistu privātas, firmas kredītkartes. Mazumtirgotāju iegūst no tā, jo tie saņem priviliģētas likmes no bankām. Turklāt, tā kā šīs kredītu kartes var rosināt klientus apmeklēt veikalu biežāk, tās palīdz uzlabot mazumtirgotāja apakšējo rindu. Tāpēc mazumtirgotājiem ir motivācija palielināt savu firmas kredītkaršu izmantošanu. Lai sasniegtu šo mērķi, tie bieži nodrošina papildu atlaides debitoriem, kuri lieto šīs kredītkartes.

Alternatīvā gadījumā tirgotāji, kas nesniedz zīmola kredītkartes, varētu vēlēties mudināt klientus maksāt, izmantojot citus norēķinu veidus, piemēram, skaidru naudu, dāvanu kartes vai lojalitātes programmas punktus. Šādā veidā viņi var palīdzēt samazināt kredītkaršu apstrādes maksu izdevumus. Tāpēc mazumtirgotāji var nodrošināt atlaides klientiem, kuri lieto šos alternatīvos norēķinu veidus.

Programmā Microsoft Dynamics 365 Commerce mazumtirgotāji var konfigurēt atlaides procentus, kas tiek piemēroti kvalificētām rindām, ja klients maksā, izmantojot izvēlēto norēķinu veidu. Klients var izlemt, vai veikt daļēju vai pilnu maksājumu, un Commerce nosaka atbilstošo atlaides summu. Ievērojiet, ka atlaides vienmēr tiek dotas par kvalificētu krājumu iepriekšēju nodokļu summu.

Ar norēķiniem balstītās atlaides nekonkurē ar uz krājumu balstītām atlaidēm, piemēram, periodiskām vai manuālām atlaidēm. Tās vienmēr tiek izvirzītas virs krājuma atlaidēm. Tāpēc, pat ja krājumam tiek lietota ekskluzīva periodiska atlaide, uz norēķiniem balstītā atlaide tiek izmantota papildus ekskluzīvajai periodiskajai atlaidei. Turklāt, ja darījumam tiek piemērota sliekšņa atlaide, un uz norēķiniem balstītā atlaide samazina kopsummu zem sliekšņa, sliekšņa atlaide tiek izmantota transakcijai.

Kaut arī uz norēķinu balstītās atlaides samazina transakcijas apakšsummu, netiek ietekmētas automātiskās maksas, kas tiek piemērotas transakcijai. Piemēram, ja pasūtījuma izmaksas tiek aprēķinātas kā $5, jo apakšsumma bija lielāka par $100, un ar norēķinu balstītā atlaide samazina summu tā, lai tā būtu mazāka par $100, saņemšanas maksas joprojām ir $5 par pasūtījumu.


> [!NOTE]
> Uz norēķiniem balstītās atlaides tiek proporcionāli sadalītas uz kvalificētajām pārdošanas rindām un samazina atsevišķu rindu iepriekšēju nodokļu summu. Ja norēķinu tipam (piemēram, skaidrā naudā) ir konfigurētas vairākas atlaides, tiek piemērotas tikai vislabākā atlaide.

Uz norēķinu balstītās atlaides var lietot tikai tām pārdošanas rindām, kurās cenas nav bloķētas. Ja pasūtījumam tiek pievienotas jaunas pārdošanas rindas, uz norēķinu balstītā atlaide tiek piemērota jaunajām pārdošanas rindām tikai maksājuma veikšanas laikā. Kamēr tiek novietots klienta pasūtījums savākšanai vai nosūtīšanai, uz norēķinu balstītā atlaide tiek piemērota tikai depozīta summai. Pēc pasūtījuma veikšanas izpildes laikā pārdošanas rindu cenas ir bloķētas. Tāpēc nevienai uz norēķinu balstītai atlaidei netiek piemērota bilance, kas tiek apmaksāta kravas saņemšanas vai sūtīšanas laikā. Uz norēķinu balstītu atlaidi var piemērot visai klienta pasūtījuma summai tikai tad, ja mazumtirgotājs iekasē visu summu kā depozītu, kamēr tiek veikts pasūtījums.

> [!IMPORTANT]
> Pakalpojumā Commerce uz norēķinu balstītās atlaides pašlaik ir ierobežotas ar diviem maksājuma veidiem: kredītkartes un skaidrā naudā.

## <a name="pos-user-experience"></a>POS lietotāju pieredze

Ja uz norēķinu balstītā atlaide tiek iestatīta skaidrā naudā un kasieris pārdošanas punktā (POS) atlasa pogu, kas ir kartēta uz skaidras naudas apmaksas operāciju, uz šo transakciju automātiski tiek attiecināta uz norēķinu balstītā atlaide. Pēc tam samazinātā summa tiek rādīta kā bilance. Tomēr, ja kasieris maksājuma ekrānā atlasa pogu **Atpakaļ**, atlaide tiek noņemta, un darbības ekrānā tiek rādīta sākotnējā summa. Uz norēķinu balstītā atlaide tiek noņemta, ja maksājuma rinda ir anulēta.

Attiecībā uz karšu maksājumiem mazumtirgotāji var iestatīt uz norēķinu balstītu atlaidi vienam vai vairākiem kredītkaršu veidiem. Tomēr sistēma nevar verificēt izmantoto kredītkartes tipu, ja vien karte nav autorizēta. Ja atlaide tiek piemērota pēc autorizācijas, maksājuma autorizācija tiks piešķirta lielākai summai, bet maksājuma uztveršana būs mazākai summai.

Lai nepieļautu šo situāciju, kad klients samaksā ar kredītkarti, kasieris redz dialoglodziņu, kurā ir uzskaitītas kredītkartes, kas ļaus klientam papildus ietaupīt. Tad kasieris var jautāt, vai klients vēlas izmantot vienu no vēlamajām kartēm, lai saņemtu papildu atlaidi. Ja kasierim tiek izmantota vēlamā karte, transakcijai tiek piemērota uz norēķinu balstīta atlaide, un samazinātā summa tiek rādīta maksājuma ekrānā. Autorizācija tiks piešķirta samazinātajai summai. Ja klients ievieto karti, kas atšķiras no tās, ko kasieris atlasījis, tiek parādīts kļūdas ziņojums, un autorizācija ir anulēta.


## <a name="call-center-user-experience"></a>Zvanu centra lietotāja pieredze

Kad lietotājs zvanu centra pasūtījuma laikā izvēlas opciju **Pabeigts**, tiek rādīts **Kopsummas** ekrāns. Sākumā kopsummas neiekļauj uz norēķinu balstītās atlaides šajā ekrānā, jo vēl nav atlasīta maksāšanas metode. Ja lietotājs ekrānā **Pievienot maksājumu** atlasa maksājuma metodi, kas ir konfigurēta uz norēķina balstītu atlaidi, maksājuma summa tiek automātiski koriģēta, lai tā atspoguļotu atlaides summu. Tāpat kā klients pie POS, arī zvanu centra klients var izlemt, vai apmaksāt maksājumu pilnībā vai daļēji. Balstoties uz apmaksāto summu, pārdošanas pasūtījumam tiek piemērota uz norēķinu balstīta atlaide.

> [!NOTE]
> Zvanu centra pasūtījumiem netiek veikta kartes validācija. Piemēram, ja zvanu centra lietotājs atlasa Visa kā kredītkarti, bet klients izmanto Mastercard, sistēma joprojām lieto atlaidi.

## <a name="exclude-items-from-discounts"></a>Noņemt atlaidi no precēm

Mazumtirgotāji bieži izvēlas nepiemērot atlaidi dažiem produktiem, piemēram, jaunām precēm vai pieprasītākajām precēm. Tomēr joprojām vēlas piemērot uz norēķinu balstītas atlaides. Piemēram, mazumtirgotājs konfigurē Commerce tā, ka tas nepiemēro uz precēm balstītas vai manuālas atlaides. Tomēr, ja klients maksā, izmantojot vēlamo norēķinu, Commerce joprojām piemēro uz norēķinu balstītu atlaidi. Lai Commerce tiktu iestatīts tādā veidā, mazumtirgotājiem ir jāpāriet uz **Produkta informācijas pārvaldība > Produkti > Izlaistās preces** atlasiet preci un pēc tam kopsavilkuma cilnē **Commerce** iestatiet opcijas **Novērst visas atlaides** un **Novērst norēķinu atlaides** uz **Nē** un opcijas **Novērst mazumtirdzniecības atlaides** un **Novērst manuālās atlaides** uz **Jā**.

> [!NOTE]
> Kad konfigurācija **Novērst visas atlaides** ir ieslēgta uz **Jā**, precei netiks piemērotas atlaides. Netiks piešķirtas pat uz norēķinu balstītās atlaides.


[!INCLUDE[footer-include](../includes/footer-banner.md)]