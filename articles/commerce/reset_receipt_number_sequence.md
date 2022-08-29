---
title: Atiestatīt kvīšu numurus
description: Šajā rakstā ir aprakstīts, kā atiestatīt ieejas plūsmas numurus, kas tiek izmantoti dažādām darbībām vēlamajā datumā (piemēram, finanšu gadā vai kalendārajā gadā).
author: ShalabhjainMSFT
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Application update 10.0.9
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, Commerce
ms.search.form: ''
ms.openlocfilehash: 3034a1b8f1a9f304b8d8803a7f906418321d81d9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272746"
---
# <a name="reset-receipt-numbers"></a>Atiestatīt kvīšu numurus 

[!include [banner](includes/banner.md)]

> [!NOTE]
> Pirms šīs funkcijas izmantošanas ir nepieciešams atlasīt **Neatkarīgās secības** rekvizītu visiem saņemšanas tipiem funkcionalitātes profilā. Turklāt ierīces sistēmas laika joslai, kur tiek izmantots POS, jāsakrīt ar atbilstošo veikala laika joslu. Šo ierobežojumu dēļ mēs iesakām nelietot šo līdzekli ražošanā, kamēr mēs strādājam, lai atrisinātu šīs problēmas nākamajam izlaidumam. 

Mazumtirgotāji ģenerē kvīšu numurus dažādām darbībām veikalā, piemēram, pārdošanas skaidrā naudā bez piegādes transakcijām, atgriešanas transakcijām, klientu pasūtījumiem, piedāvājumiem un maksājumiem. Lai gan mazumtirgotāji definē savus kvīšu formātus, dažām valstīm vai reģioniem ir noteikumi, kas ierobežo šos kvīšu formātus. Piemēram, šie noteikumi var ierobežot kvīts rakstzīmju skaitu, pieprasīt secīgus saņemšanas numurus, ierobežot dažas speciālās rakstzīmes vai pieprasīt atgriezt saņemšanas numurus gada sākumā. Programma Microsoft Dynamics 365 Commerce padara kvīšu numuru pārvaldību ļoti elastīgu, lai palīdzētu tirgotājiem atbilst normatīvajām prasībām. Šajā rakstā ir skaidrots, kā izmantot kvīšu numuru atiestatīšanas funkcionalitāti.

Pakalpojumā Commerce saņemšanas formāti var būt burtciparu formā. Tajos var ievietot gan statisko saturu, gan dinamisko saturu. Statiskais saturs ietver alfabētisku rakstzīmi, ciparus un speciālās rakstzīmes. Dinamiskajā saturā ir viena vai vairākas rakstzīmes, kas attēlo tādu informāciju kā veikala numurs, termināļa numurs, datums, mēnesis, gads un numuru sērijas, kas tiek automātiski palielinātas. Formāti ir definēti funkcionalitātes profila sadaļā **Kvīts numerācija**. Sekojošajā tabulā ir aprakstītas rakstzīmes, kas attēlo dinamisko saturu.

| Rakstzīmes | Apraksts |
|------------|-------------|
| S          | Veikala numuram tiek izmantota rakstzīme **V**. Piemēram, ja veikals ir numurēts HOUSTON1, formāts **VVV** parāda "ON1" kvītī, Formāts **VVVVV** parāda "STON1" kvītī. |
| T          | Termināla numuram tiek izmantota rakstzīme **T**. Piemēram, ja terminālis ir numurēts ar 0001, formāts **TTTT** parāda "0001" kvītī, |
| K          | Personāla ID tiek izmantota rakstzīme **C**. Piemēram, ja darbiniekam ir ID 000160, formāts **CCCC** parāda "0160" kvītī. |
| ddd        | Rakstzīmes **ddd** atbilst gada dienai no 1 līdz 366. Piemēram, 15. janvārī, formāts **ddd** kvītī parāda "015". |
| MM         | Rakstzīmes **MM** tiek izmantotas divu ciparu mēnesī. Piemēram, janvārī, formāts **MM** kvītī parāda "01". |
| DD         | Rakstzīmes **DD** tiek izmantotas divu ciparu mēneša dienai. Piemēram, 15. janvārī, formāts **DD** kvītī parāda "15". |
| YY         | Rakstzīmes **GG** tiek izmantotas divu ciparu gadā. Piemēram, jebkurā mēnesī 2020. gadā formāts **GG** rāda kvītī "20". |
| \#         | Numura zīme (**\#**) tiek izmantota secīgai numerācijai. Piemēram, formāts **####** kvītī rāda "0001," "0002," "0003," un tā tālāk. |

Varat atiestatīt kvītis secīgu numerāciju noteiktā datumā. Pēc tam pirmajai transakcijai, kas notiek pēc 12:00 atlasītajā atiestatīšanas datumā, sistēma atiestata kvīts numuru sēriju uz 1. Varat arī norādīt, vai atiestatīšana notiks tikai vienu reizi, vai tā atkārtosies katru gadu. Ja ir norādīta ikgadējā atkārtošanās, atiestatīšana automātiski notiek katru gadu, līdz mazumtirgotājs izvēlas to apturēt. 

Lai aktivizētu atiestatīšanu, veiciet tālāk minētās darbības.

1. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**.
1. **Kvīts numerācijas** kopsavilkuma cilnē atlasiet **Atiestatīt numura atiestatīšanas datumu**.
1. Nolaižamajā dialoglodziņā laukā **Atiestatīt datumu** atlasiet nākotnes datumu, kad jāveic atiestatīšana.
1. Laukā **Atiestatīt kvīts veidu** atlasiet **Tikai vienu reizi** vai **Katru gadu**.
1. Atlasiet **Labi**.

![Kvīts atiestatīšanas datuma atlasīšana.](media/Enable_receipt_reset.png "Kvīts atiestatīšanas datuma atlasīšana")

Pēc datuma atlasīšanas tas parādās kolonnā **Nākamais kvīts numura atiestatīšanas datums**, Atiestatīšanas datums ir piemērojams visiem kvīšu darījumu tipiem. Tāpēc kvīts numuru sērija tiks atiestatīta visiem kvīšu veidiem.

Kad pienāk atiestatīšanas datums, kvīts numurs tiek atiestatīts pirmajai katra veida darbībai. Turklāt funkcionalitātes profilā atiestatīšanas datums ir pārvietots no **Nākamās kvīts numura atgriešanas datuma** kolonnas uz **Pašreizējā kvīts numura atgriešanas datuma** kolonnu. Šīs izmaiņas norāda, ka, ja reģistrs netiek lietots atiestatīšanas datumā, kvīts numurs tiks atiestatīts nākamreiz, kad reģistrs *tiek* izmantots. Piemēram, 2019. gada 3. decembrī atlasāt **1. janvāri, 2020**, kā atiestatīšanas datumu. 1. janvārī, kad reģistri veic savu pirmo transakciju, kvīts numurs tiek atiestatīts. Tomēr viens reģistrs netiek lietots decembrī un janvārī, bet pēc tam tiek lietots februārī. Šādā gadījumā, tā kā tika definēta atiestatīšanas darbība, šī reģistra kvīts numurs tiks atiestatīts, ja reģistrs pirmo transakciju veic februārī.

Lai dzēstu turpmākos atiestatīšanas datumus, varat izmantot funkcionalitāti **Notīrīt atiestatīšanas datumu**. Tomēr, ja atgriešanas datums bijis pagātnē, to nevar atsaukt. Tāpēc atiestatīšana joprojām notiks visiem reģistriem, kuros atiestatīšana vēl nav notikusi.

> [!NOTE]
> Atkarībā no atlasītā atiestatīšanas datuma un kvīts formāta, iespējams, ir dublēti kvīšu numuri. Kaut arī pārdošanas punkta (POS) sistēma var tikt galā ar šīm situācijām, tās palielina laika daudzumu, kas nepieciešams, lai apstrādātu atgriešanu, jo pārdošanas partneriem ir jāatlasa no dublētajām kvītīm. Citi sarežģījumi, kas saistīti ar datu tīrīšanu, var rasties, ja dublētās kvītis nebija plānotas sekas. Tāpēc ir ieteicams lietot dinamisko datumu rakstzīmes (piemēram, **ddd**, **MM**, **DD** un **YY**), lai pēc atiestatīšanas palīdzētu novērst dublētus kvīšu numurus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
