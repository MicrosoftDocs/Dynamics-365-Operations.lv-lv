---
title: Atvēlētie maksājumu termināļi un uzvednes printerim un skaidras naudas atvilknei
description: Šajā tēmā ir sniegta informācija par iespēju izveidot īpašu maksājumu termināli un pieprasīt lietotājam atlasīt skaidras naudas atvilkni un kvīts printeri.
author: BrianShook
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: b955e55271471ac43ff4c2b217c6448b30536e06
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779774"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>Atvēlētie maksājumu termināļi un uzvednes printerim un skaidras naudas atvilknei

[!include [banner](includes/banner.md)]

Šajā tēmā ir sniegta informācija par iespēju izveidot īpašu maksājumu termināli un pieprasīt lietotājam atlasīt skaidras naudas atvilkni un kvīts printeri.

## <a name="overview"></a>Pārskats

Mūsdienu mazumtirgotāji meklē veidus, kā racionalizēt izrakstīšanās no tiešsaistes veikala pieredzi. Jaunākās tendences virzībā uz elektronisku izrakstīšanos, izmantojot elektroniskos maksājumus, ne tikai palīdz padarīt iepirkšanas pieredzi raitāku, bet arī samazināt nepieciešamību pēc visām perifērijas ierīcēm, kas pieejamas katram saistītajam veikalam.

Programma Microsoft Dynamics 365 Commerce atbalsta šīs tendences, iespējojot scenāriju, kurā pārdošanas punkta (POS) ierīcei ir piešķirts atvēlēts maksājumu terminālis, kas tai ir visu laiku, bet tam nav sava kvīts printera vai skaidras naudas atvilknes. Kad saistītajiem veikaliem ir jāizdrukā kvīts vai jāpieņem skaidras naudas maksājums, viņiem tiek piedāvāts atlasīt aparatūras staciju, kurā šīs ierīces ir konfigurētas.

## <a name="key-terms"></a>Galvenie termini

| Termiņš | apraksts |
|---|---|
| Reģistrs | Elements, kas tiek izmantots, lai konfigurētu POS reģistra instanci. |
| Ierīce | POS reģistra fiziskas instances atveidojums un moderna POS programma, kas tai piešķirta. |
| Atvēlēta aparatūras stacija | Aparatūras stacijas biznesa loģika, kas ir iebūvēta programmā Modern POS operētājsistēmai Windows un Modern POS operētājsistēmai Android. |
| Skaidras naudas atvēršanas (d/k) ports | Tradicionālā metode, lai skaidras naudas atvilkni savienotu ar kvīts printeri. |
| Tīkla perifērās ierīces | Iebūvēts atbalsts tīklā iespējotiem maksājumu termināļiem, kvīšu printeriem un skaidras naudas atvilknēm. |

## <a name="supported-pos-clients-and-devices"></a>Atbalstītie POS klienti un ierīces

Šajā tēmā aprakstīto funkcionalitāti atbalsta Modern POS sistēmai Windows un Modern POS Android POS klientiem.

Šī funkcionalitāte atbalsta tīklā iespējotus maksājumu termināļus un kvīšu printerus. Varat nodrošināt skaidras naudas atvilknes atbalstu, savienojot skaidras naudas atvilkni ar tīklā iespējoto kvīts printeri, izmantojot d/k portu.

Šīs funkcionalitātes standarta atbalstu nodrošina [Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3). Taču citus maksājumu savienotājus var atbalstīt, izmantojot Commerce programmatūras izstrādes komplektu (SDK) maksājumiem. Atbalstītie kvīts printeri ietver tīklā iespējotus kvīts printerus no Star Micronics un Epson.

Star Micronics kvīšu printeru iestatīšanai izmantojiet Star Micronics printera utilītu, lai konfigurētu ierīci tā, ka to var izmantot tīklā. Šī utilīta arī nodrošinās ierīces IP adresi.

Epson kvīšu printeru iestatīšanai izmantojiet Epson ePOS-Print utilītu, lai iestatītu ierīci tīkla protokolu izmantošanai.

Papildinformāciju par to, kā iestatīt tīkla perifērās ierīces, skatiet [Tīkla perifēro ierīču atbalsta pārskats](./dev-itpro/network-peripherals.md).

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>Atvēlētā maksājumu termināļa un uzvednes printerim un skaidras naudas atvilknei iestatīšana

### <a name="set-up-hardware-profiles"></a>Aparatūras profilu iestatīšana

Ir jābūt divu veidu aparatūras profiliem. Pirmais tiek piešķirts reģistram. Otrais tiek piešķirts aparatūras stacijai veikala līmenī, un to izmanto, lai loģiski grupētu tīkla kvīšu printerus un skaidras naudas atvilknes.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>Aparatūras profila iestatīšana reģistram

Lai iestatītu aparatūras profilu, kas piešķirts reģistram, veiciet tālāk norādītās darbības.

1. Programmā Dynamics 365 Commerce meklējiet **Aparatūras profils**.
2. Atlasiet **Jauns**.
3. Piešķiriet aparatūras profila numuru un pēc tam ievadiet aprakstu. Šis aparatūras profils tiks piešķirts reģistram. Tāpēc pietiks ar tādu aprakstu kā **Atvēlēts ar regresu**.
4. Dažādiem ierīču veidu kopsavilkuma cilnēs iestatiet tālāk minētos ierīču veidus.

    | Ierīce | tips | Ierīces nosaukums | Papildu informācija |
    |---|---|---|---|
    | Printeris | Tīkls | *Jebkurš* | Ierīces nosaukums ir reģistrjutīgs. **Kvīts profila ID** ir jābūt tādam pašam kā **Kvīts profila ID**, kas ir kartēts uz tīkla printeri, kurš ir iestatīts aparatūras profilā, kas piešķirts aparatūras stacijai kanāla līmenī. |
    | Naudas kaste | Tīkls | *Jebkurš* | Ierīces nosaukums ir reģistrjutīgs. Iestatiet opciju **Lietot koplietoto maiņu** uz **Jā**. |
    | EFT pakalpojums | Adyen | Nav attiecināms | Informāciju par to, ka iestatīt standarta Adyen savienotāju, skatiet [Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3). Citus maksājumu savienotājus var atbalstīt, izmantojot [Commerce programmatūras izstrādes komplektu (SDK) maksājumiem](./dev-itpro/end-to-end-payment-extension.md). |
    | PIN bloks | Tīkls | **MicrosoftAdyenDeviceV001** | Nav. |

5. Sistēmā Dynamics 365 Commerce meklējiet **Reģistri**.
6. Atlasiet reģistru, atlasot reģistra numuru un pēc tam atlasiet **Rediģēt**.
7. Piešķiriet reģistram tikko izveidoto aparatūras profilu, kam jāizmanto atvēlētais maksājumu terminālis. Ierīcei, kas ir kartēta ar šo reģistru, jāizmanto Modern POS operētājsistēmai Windows vai Modern POS operētājsistēmai Android.
8. Atlasiet **Saglabāt**.
9. Darbību rūts cilnē **Reģistri** atlasiet **Konfigurēt IP adreses**.
10. Kopsavilkuma cilnē **PIN bloks** ievadiet maksājumu termināļa IP adresi. Informāciju par to, kā iegūt maksājumu termināļa IP adresi, izmantojot Adyen savienotāju, skatiet [Adyen Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3).
11. Atlasiet **Saglabāt**.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>Aparatūras profila kvīšu printerim un skaidras naudas atvilknei iestatīšana

Lai iestatītu aparatūras profilu, kas tiek izmantots tīkla kvīšu printera un skaidras naudas atvilknes grupēšanai, izpildiet tākāk minētās darbības.

1. Programmā Dynamics 365 Commerce meklējiet **Aparatūras profils**.
2. Atlasiet **Jauns**.
3. Piešķiriet aparatūras profila numuru un pēc tam ievadiet aprakstu. Šis aparatūras profils tiks izmantots kvīšu printera un skaidras naudas atvilknes grupēšanai. Tāpēc pietiks ar tādiem aprakstiem kā **Tīkla printeris un skaidras naudas atvilkne**.
4. Dažādiem ierīču veidu kopsavilkuma cilnēs iestatiet tālāk minētos ierīču veidus.

    | Ierīce | tips | apraksts | Papildu informācija |
    |---|---|---|---|
    | Printeris | Tīkls | **Epson** vai **Star** | Ierīces nosaukums ir reģistrjutīgs. **Kvīts profila ID** ir jābūt tādam pašam kā **Kvīts profila ID**, kas ir kartēts uz printeri, kurš ir iestatīts aparatūras profilā, kas piešķirts reģistram. |
    | Naudas kaste | Regress | **Epson** vai **Star** | Ierīces nosaukums ir reģistrjutīgs. Iestatiet opciju **Lietot koplietoto maiņu** uz **Jā**. |

5. Atlasiet **Saglabāt**.

### <a name="set-up-hardware-stations"></a>Iestatīt aparatūras stacijas

Ir jābūt divām aparatūras stacijām. Pirmais tiks kartēts uz reģistru. Otrais tiks atlasīts pēc vajadzības, kad ir jāizdrukā kvīts vai jāatver skaidrās naudas atvilkne.

#### <a name="register-a-hardware-station"></a>Aparatūras stacijas reģistrēšana

1. Programmā Dynamics 365 Commerce meklējiet **Visi veikali**.
2. Atlasiet veikalu, atlasot tā vērtības **Mazumtirdzniecības kanāla ID** un pēc tam atlasiet **Rediģēt**.
3. Kopsavilkuma cilnē **Aparatūras stacijas** atlasiet **Pievienot**.
4. Iestatiet lauku **Aparatūras stacijas veids** uz **Atvēlēts**.
5. Ievadiet aprakstu, bet neiestatiet citas vērtības šai aparatūras stacijai. Šī aparatūras stacija tiks izmantota reģistram visu laiku. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>Aparatūras stacijas kvīšu printerim un skaidras naudas atvilknei iestatīšana

1. Programmā Dynamics 365 Commerce meklējiet **Visi veikali**.
2. Atlasiet veikalu, atlasot tā vērtības **Mazumtirdzniecības kanāla ID** un pēc tam atlasiet **Rediģēt**.
3. Kopsavilkuma cilnē **Aparatūras stacijas** atlasiet **Pievienot**.
4. Iestatiet lauku **Aparatūras stacijas veids** uz **Atvēlēts**.
5. Ievadiet aprakstu. Šī aparatūras stacija tiks izmantota kvīšu printerim un skaidras naudas atvilknei.
6. Laukā **Aparatūras profils** atlasiet aparatūras profilu, ko iepriekš izveidojāt kvīšu printerim un skaidrās naudas atvilknei.
7. Atlasiet **Saglabāt**.
8. Kamēr aparatūras stacija kvīšu printerim un skaidrās naudas atvilknei joprojām ir atlasīta, atlasiet **Konfigurēt IP adreses**.
9. Iegūstiet printera IP adresi un ievadiet to kā IP adresi gan kvīšu printerim, gan skaidrās naudas atvilknei.
10. Atlasiet **Saglabāt**
11. Meklējiet **Sadales grafiki**.
12. Atlasiet sadales grafiku **1090** un pēc tam atlasiet **Palaist tūlīt**.
13. Atlasiet sadales grafiku **1070** un pēc tam atlasiet **Palaist tūlīt**.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>Iestatiet sistēmu, lai brīdinātu par kvīšu printeri un skaidrās naudas atvilknes atlasi pēc vajadzības

1. Atbalstītajā POS klientā aizveriet pašreizējo maiņu, ja maiņa ir atvērta.
2. Pierakstieties un pēc tam atlasiet **Ar atvilkni nesaistītas atvilknes operācijas**.
3. Imantojiet operāciju **Aparatūras staciju pārvaldība**, lai ieslēgtu aparatūras staciju.
4. Atlasiet aparatūras staciju, kuru izveidojāt reģistram, lai to aktivizētu.
5. Izrakstieties no POS un pēc tam atveriet maiņu.

Maksājuma terminālis, kas piešķirts aparatūras profilam, tagad vienmēr būs aktīvs, un jums tiks vaicāts, vai ir jānorāda kvīšu printeris vai skaidrās naudas atvilkne.

Daudzi tirgotāji, kas pieprasījuši šo līdzekli, ir ieinteresēti samazināt atkritumus, izsniedzot e-pasta kvītis un veicinot elektroniskos maksājumus. Atkarībā no POS konfigurācijas saistītajiem veikaliem tiek parādīts aicinājums atlasīt kvīšu printeri vai skaidrās naudas atvilkni tikai tad, ja debitors vēlas saņemt fizisku kvīti vai vēlas maksāt skaidrā naudā.

Saistītie veikali saņem aicinājumu atlasīt aparatūras staciju tikai vienu reizi transakcijas laikā, izņemot gadījumus, kad ir jāizdrukā kvīts un maksājumam tiek izmantota skaidra nauda, bet aparatūras profils, kas sākotnēji tika atlasīts, neietver abas ierīces. Šādā gadījumā saistītajiem veikaliem atkal tiks piedāvāts atlasīt aparatūras staciju, ko var izmantot transakcijas pabeigšanai.

## <a name="related-articles"></a>Saistītie raksti

- [POS hibrīdprogrammas iestatīšana operētājsistēmā Android un iOS](./dev-itpro/hybridapp.md)
- [Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3)
- [Tīkla perifēro ierīču atbalsta pārskats](./dev-itpro/network-peripherals.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
