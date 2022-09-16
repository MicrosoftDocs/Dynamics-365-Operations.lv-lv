---
title: Uz konkursu balstītas atlaides
description: Šajā rakstā ir aprakstīta norēķinu atlaižu funkcionalitāte, kas ļauj mazumtirgotājiem konfigurēt atlaides noteiktiem norēķinu veidiem sadaļā Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/19/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: b11145c0c12f973b437ebf87921a5686d217d327
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473826"
---
# <a name="tender-based-discount"></a>Atlaide atbilstoši norēķiniem

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīta norēķinu atlaižu funkcionalitāte, kas ļauj mazumtirgotājiem konfigurēt atlaides noteiktiem norēķinu veidiem sadaļā Microsoft Dynamics 365 Commerce.

Tā ir kopīga prakse starp mazumtirgotājiem, lai izlaistu privātas, firmas kredītkartes. Mazumtirgotāju iegūst no tā, jo tie saņem priviliģētas likmes no bankām. Turklāt, tā kā šīs kredītu kartes var rosināt klientus apmeklēt veikalu biežāk, tās palīdz uzlabot mazumtirgotāja apakšējo rindu. Tāpēc mazumtirgotājiem ir motivācija palielināt savu firmas kredītkaršu izmantošanu. Lai sasniegtu šo mērķi, tie bieži nodrošina papildu atlaides debitoriem, kuri lieto šīs kredītkartes.

Alternatīvā gadījumā tirgotāji, kas nesniedz zīmola kredītkartes, varētu vēlēties mudināt klientus maksāt, izmantojot citus norēķinu veidus, piemēram, skaidru naudu, dāvanu kartes vai lojalitātes programmas punktus. Šādā veidā viņi var palīdzēt samazināt kredītkaršu apstrādes maksu izdevumus. Tāpēc mazumtirgotāji var nodrošināt atlaides klientiem, kuri lieto šos alternatīvos norēķinu veidus.

## <a name="tender-based-discount"></a>Atlaide atbilstoši norēķiniem

Commerce atbalsta uz *norēķiniem* balstītu atlaidi, kas ļauj mazumtirgotājiem konfigurēt atlaides procentus, kas tiek piemēroti darbībai, ja darbības kopsumma pārsniedz noteiktu summu un debitors maksā, izmantojot vēlamo maksājuma veidu. Uz norēķiniem balstīta atlaide ir balstīta uz pakāpēm, tādējādi dažādās atlaides procentu likmes var saistīt ar dažādiem summas sliekšņiem. Debitors var izlemt, vai veikt daļēju maksājumu vai pilnu maksājumu, un cenu noteikšanas programma nosaka atbilstošu atlaides summu. Uz norēķiniem pamatota atlaide vienmēr tiek dota pārdošanas rindu pirmsnododošanas summai.

No norēķiniem balstīts atlaide var tikt piemērota tikai pārdošanas rindām, kurās cenas nav bloķētas, un tā ir proporcionāli sadalīta kvalificētajām rindām. Ja pasūtījumam tiek pievienotas jaunas pārdošanas rindas, atlaide, kas pamatota uz norēķiniem, maksājuma laikā tiek piemērota tikai jaunajām pārdošanas rindām. Kad tiek izvietots debitora pasūtījums par savākšanu vai piegādi, uz norēķiniem balstītā atlaide tiek piemērota tikai deponēšanas summai. Pēc pasūtījuma veikšanas izpildes laikā pārdošanas rindu cenas ir bloķētas. Uz norēķiniem balstīta atlaide netiek piemērota nevienai bilancei, kas tiek maksāta sūtīšanas laikā vai autorizēta nosūtīšanas laikā. Uz norēķinu balstītu atlaidi var piemērot visai klienta pasūtījuma summai tikai tad, ja mazumtirgotājs iekasē visu summu kā depozītu, kamēr tiek veikts pasūtījums.

Uz norēķiniem balstītas atlaides nesakrīt ar krājuma atlaidēm, piemēram, vienkāršas atlaides, daudzuma atlaides, sliekšņa atlaides, komplekta atlaides un manuālas atlaides. Atlaides, kas pamatotas uz norēķiniem, vienmēr tiek saliktas virs atlaidēm, kas pamatotas uz krājumiem. Tāpēc, pat ja precei tiek piemērota ekskluzīvā atlaide, atlaides, kuru pamatā ir norēķini, joprojām var piemērot papildus ekskluzīvajai atlaidei. Turklāt, ja darījumam tiek piemērota sliekšņa atlaide, un uz norēķiniem balstītā atlaide samazina kopsummu zem sliekšņa, sliekšņa atlaide tiek izmantota transakcijai.

Pat ja uz norēķinu bāzētās atlaides samazina darbības apakšsummu, netiek ietekmētas automātiskas maksas, kas tiek piemērotas darbībai. Piemēram, ja piegādes maksas tiek aprēķinātas kā $5, jo apakšsumma bija lielāka par $100 un uz norēķiniem balstītā atlaide samazina summu tā, lai tā būtu mazāka par $100, piegādes maksas pasūtījumam paliek $5.

Uz norēķiniem balstīta atlaide pašlaik ir ierobežota līdz diviem maksājumu veidiem: kredītkartes un skaidra nauda. Ja maksājuma veidam ir konfigurētas vairākas uz norēķiniem balstītas atlaides, tiek lietota tikai vislabākā no norēķinu veida atlaide.

## <a name="pos-user-experience"></a>POS lietotāju pieredze

Ja skaidrai naudai ir iestatīta uz norēķinu balstīta atlaide un kasieris pārdošanas punktā (POS) atlasa pogu Maksāt skaidrā naudā, lai paņemtu skaidras **naudas** un pārnešanas darbību, darbībai automātiski tiek piemērota no norēķinu atkarīga atlaide. Pēc tam samazinātā summa tiek rādīta kā bilance. Tomēr, ja kasieris maksājuma ekrānā atlasa pogu **Atpakaļ**, atlaide tiek noņemta, un darbības ekrānā tiek rādīta sākotnējā summa. Uz norēķinu balstītā atlaide tiek noņemta, ja maksājuma rinda ir anulēta.

Kredītkaršu maksājumiem mazumtirgotāji var iestatīt uz norēķiniem balstītu atlaidi vienam vai vairākiem kredītkaršu veidiem. Tomēr sistēma nevar verificēt izmantoto kredītkartes tipu, ja vien karte nav autorizēta. Ja atlaide tiek piemērota pēc autorizācijas, maksājuma autorizācija tiks piešķirta lielākai summai, bet maksājuma uztveršana būs mazākai summai. Lai novērsīsiet šo situāciju, ja debitors maksā ar kredītkarti, kasieris tiek parādīts dialoglodziņā, kurā uzskaitītas vēlamās kredītkartes, kas debitoram izdos papildu atlaidi. Tad kasieris var jautāt, vai klients vēlas izmantot vienu no vēlamajām kartēm, lai saņemtu papildu atlaidi. Ja kasieris izvēlas vēlamo karti, darbībai tiek piemērota atlaide, pamatojoties uz norēķiniem, un samazinātā summa tiek parādīta maksājuma ekrānā. Autorizācija tiks piešķirta samazinātajai summai. Ja klients ievieto karti, kas atšķiras no tās, ko kasieris atlasījis, tiek parādīts kļūdas ziņojums, un autorizācija ir anulēta.

## <a name="call-center-user-experience"></a>Zvanu centra lietotāja pieredze

Ja zvanu centra lietotājs zvanu centra **pasūtījuma** laikā atlasa Pabeigt, tiek parādīts **kopsummas** ekrāns. Sākumā kopsummas neiekļauj uz norēķinu balstītās atlaides šajā ekrānā, jo vēl nav atlasīta maksāšanas metode. Ja lietotājs ekrānā **Pievienot maksājumu** atlasa maksājuma metodi, kas ir konfigurēta uz norēķina balstītu atlaidi, maksājuma summa tiek automātiski koriģēta, lai tā atspoguļotu atlaides summu. Tāpat kā POS klients zvanu centra debitors var izlemt, vai apmaksāt pilnu maksājumu vai daļējo maksājumu. Balstoties uz apmaksāto summu, pārdošanas pasūtījumam tiek piemērota uz norēķinu balstīta atlaide.

> [!NOTE]
> Zvanu centra pasūtījumiem netiek veikta kartes validācija. Piemēram, ja zvanu centra lietotājs atlasa Visa kā kredītkarti, bet klients izmanto Mastercard, sistēma joprojām lieto atlaidi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
