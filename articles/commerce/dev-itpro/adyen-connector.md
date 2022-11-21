---
title: Dynamics 365 Payment Connector pakalpojumam Adyen — pārskats
description: Šajā rakstā ir sniegts pārskats par 365 maksājumu savienotāju Microsoft Dynamics Adyen.
author: rassadi
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.openlocfilehash: 6c819e8cf9f5dcb7895ac2633decf0a925c08f2d
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2022
ms.locfileid: "9784997"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Dynamics 365 Payment Connector pakalpojumam Adyen — pārskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par Microsoft Dynamics Adyen 365 maksājumu savienotāju un ietverts visaptverošs atbalstīto līdzekļu un funkcionalitātes saraksts. Saistītie raksti aptver reģistrēšanos Adyen, savienotāja konfigurāciju, bieži uzdotos jautājumus un problēmu novēršanas norādījumus par dažām bieži sastopamām problēmām.

## <a name="key-terms"></a>Galvenie termini

| Termiņš | Apraksts |
|---|---|
| Maksājumu savienotājs | Paplašinājums, kas atvieglo saziņu starp Microsoft Dynamics 365 Commerce (un saistītajiem komponentiem) un maksājumu pakalpojumu. Šajā rakstā aprakstītais savienotājs tika ieviests, izmantojot standarta maksājumu programmatūras izstrādes komplektu (SDK). |
| Karte ir | Attiecas uz maksājumu transakcijām, kurās tiek parādīta un izmantota Dynamics 365 tirdzniecības vietas maksājumu termināļa savienotājā. |
| Kartes nav | Attiecas uz maksājumu transakcijām, kurās nav fiziskas kartes, piemēram, e-komercijas vai zvanu centra scenārijiem. Šādos scenārijos ar maksājumu saistītā informācija tiek ievadīta manuāli vai nu e-komercijas vietnē, zvanu centra plūsmā, tirdzniecības vietā vai maksājumu terminālī. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Atbalstītie līdzekļi, funkcionalitāte, versijas un termināļi

Iebūvētais Dynamics 365 Payment Connector for Adyen izmanto standarta maksājumu SDK. Tāpēc tam nav īpašu iespēju, kas nav pieejamas arī citiem maksājumu savienotājiem.

### <a name="supported-versions"></a>Atbalstītās versijas

#### <a name="microsoft-dynamics-365-supported-versions"></a>Microsoft Dynamics 365 atbalstītās versijas
Pirmās puses iebūvētais Dynamics 365 Payment Connector for Adyen tiek atbalstīts Microsoft Dynamics 365 Finance versijā 8.1.3 (2019. gada janvārī) vai jaunākā versijā un Microsoft Dynamics 365 Retail versijā 8.1.3 vai jaunākā versijā. Tomēr trešās puses joprojām var izstrādāt citus Adyen maksājumu savienotājus vecākām 365 versijām Microsoft Dynamics.

#### <a name="supported-adyen-firmware-versions"></a>Atbalstītās Adyen aparātprogrammatūras versijas

Tālāk esošajā sarakstā ir aprakstītas minimālās un maksimālās Adyen aparātprogrammatūras versijas, kas tiek atbalstītas katrai POS versijai Microsoft Dynamics 365 Retail.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail POS versija 10.0.25
| Minimālā Adyen programmaparatūras versija | Maksimālā Adyen programmaparatūras versija |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail POS versija 10.0.26
| Minimālā Adyen programmaparatūras versija | Maksimālā Adyen programmaparatūras versija |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail POS versija 10.0.27
| Minimālā Adyen programmaparatūras versija | Maksimālā Adyen programmaparatūras versija |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail POS versija 10.0.28
| Minimālā Adyen programmaparatūras versija | Maksimālā Adyen programmaparatūras versija |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail POS versija 10.0.29
| Minimālā Adyen programmaparatūras versija | Maksimālā Adyen programmaparatūras versija |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail POS versija 10.0.30
| Minimālā Adyen programmaparatūras versija | Maksimālā Adyen programmaparatūras versija |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Adyen var izlaist mazāksvarīgo versiju atjauninājumus pēc tam, kad Microsoft ir pārbaudījusi galveno versiju. Kamēr tiek atbalstīta galvenā versija, ir labi, ja tajā pašā galvenajā versijā ir mazāksvarīgo versiju atjauninājumi. Šie atjauninājumi parasti ir ļoti mērķtiecīgi labojumi un neatbilst pilnīgas atkārtotas testēšanas joslai, ja vien tā pati galvenā programmaparatūras versija ir iepriekš pārbaudīta. Atjauninājumi nedrīkst pārsniegt maksimālo Adyen aparātprogrammatūras versiju, kas norādīta dokumentācijā. 
>
> Lai migrētu no Adyen aparātprogrammatūras versijas, kas vecāka par 53. versiju, uz 53. versiju ir nepieciešama POS KB 4577957 **ikmēneša** programmas Commerce versiju 10.0.11–10.0.14 atjauninājumiem. Ja kāda no šīm versijām tiek izmantota un tajā nav iekļauts labojumfails, maksājumu termināļa pēcjaunināšanas būs atļauti maksājumi tikai ar NFC starpniecību. Lietojot labojumfailu POS, šī problēma tiek novērsta. Ja POS versija ir vecāka par versiju 10.0.11, iesniedziet atbalsta pieprasījumu, atzīmējot, ka ārpus pakalpojuma esošu MPOS ir nepieciešams KB 4577957 **labojums**.
> 
> Adyen aparātprogrammatūras versijām no 59p7 līdz 62p9 dāvanu kartes izņemšanas **operācija** pieprasa PIN koda ievadi divreiz scenārijos, kad dāvanu karte tiek ievadīta manuāli. Šī problēma netiek atveidota, kad dāvanu karte tiek vilkta. Adyen izmeklē. 

### <a name="supported-payment-terminals"></a>Atbalstītie maksājumu termināļi
Dynamics 365 Payment Connector for Adyen izmanto ierīces agnostikas [Adyen maksājumu termināļa API](https://www.adyen.com/blog/introducing-the-terminal-api) priekšrocības. Tas atbalsta visus maksājumu termināļus, kurus atbalsta šī lietojumprogrammu programmēšanas saskarne (API). Lai iegūtu pilnu atbalstīto maksājumu termināļu sarakstu, apmeklējiet [lapu Adyen POS termināļi](https://www.adyen.com/pos-payments/terminals).

Nākamajā videoklipā aprakstītas Adyen Castles SE1 Android maksājumu termināļa iespējas.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bKeM]

### <a name="supported-payment-instruments"></a>Atbalstītie maksāšanas līdzekļi

#### <a name="supported-debit-and-credit-cards"></a>Atbalstītās debetkartes un kredītkartes

| Zīmols | Variants | Karte ir | E-komercija | Zvanu centrs |
|---|---|:-:|:-:|:-:|
| MasterCard | Kredīts | ✔ | ✔ | ✔ |
| MasterCard | Debets | ✔ | ✔ | ✔ |
| MasterCard | Alfa bankas bonuss | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Maksāt | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro Apvienotā Karaliste | ✔ | ✔ | ✔ |
| VĪZA | Kredīts | ✔ | ✔ | ✔ |
| VĪZA | Debets | ✔ | ✔ | ✔ |
| VĪZA | Alfa bankas bonuss | ✔ | ✔ | ✔ |
| VĪZA | Android Maksāt | ✔ |  |  |
| VĪZA | Apple Pay | ✔ |  |  |
| VĪZA | Samsung Maksāt | ✔ |  |  |
| VĪZA | VISA izrakstīšanās | ✔ | ✔ | ✔ |
| VĪZA | VISA Dankort | ✔ | ✔ | ✔ |
| VĪZA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VĪZA | VISA Aravia karte | ✔ | ✔ | ✔ |
| AMEX | Kredīts | ✔ | ✔ | ✔ |
| AMEX | Debets | ✔ | ✔ | ✔ |
| AMEX | Android Maksāt | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Maksāt | ✔ |  |  |
| AMEX | AMEX komerciāls | ✔ | ✔ | ✔ |
| AMEX | AMEX patērētājs | ✔ | ✔ | ✔ |
| AMEX | AMEX korporatīvie | ✔ | ✔ | ✔ |
| AMEX | AMEX mazie uzņēmumi | ✔ | ✔ | ✔ |
| Atklāt | Standarta | ✔ | ✔ | ✔ |
| Atklāt | Android Maksāt | ✔ |  |  |
| Atklāt | Apple Pay | ✔ |  |  |
| Atklāt | Samsung Maksāt | ✔ |  |  |
| Diners   | Standarta | ✔ | ✔ | ✔ |
| Dineromail | Standarta | ✔ | ✔ | ✔ |
| JCB | Standarta | ✔ | ✔ | ✔ |
| Savienības darba samaksa\* | Standarta | ✔ |  |  |
| Interac debets\* | Standarta | ✔ |  |  |

\* Interac un Union Pay periodisko karšu žetonus Adyen nenodrošina, tāpēc tos nevar atbalstīt darījumiem ar karti, kurā nav klāt.

#### <a name="supported-gift-cards"></a>Atbalstītās dāvanu kartes
| Shēma | Karte ir | Kartes nav |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

Lai atbalstītu šīs ārējās dāvanu karšu shēmas, izmantojot Dynamics 365 Payment Connector for Adyen, ir jāveic papildu darbības. Papildinformāciju skatiet sadaļā [Atbalsts ārējām dāvanu kartēm](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Atbalstītie maki

| Shēma | Karte ir | Kartes nav |
|---|---|---|
| Alipay | Atbalsts tiks pievienots nākamajā laidienā. | Nē |
| WeChat | Atbalsts tiks pievienots nākamajā laidienā. | Nē |

#### <a name="supported-card-present-input-methods"></a>Atbalstītās kartes ievades metodes
| Ievades metode | Tiek atbalstīts | Piezīmes |
|---|:-:|---|
| Dip | ✔ | |
| Lasīt karti | ✔ | |
| Krāns | ✔ | |
| Manuāla ievadīšana, izmantojot POS lietotāja interfeisu. |  | Šobrīd netiek atbalstīts |
| Manuāla ievadīšana, izmantojot maksājumu termināli. | ✔ | Atbalsta kredītkaršu, debetkaršu un dāvanu karšu manuālu ievadīšanu ar PIN koda ievadīšanu. | 


#### <a name="supported-card-present-countries"></a>Atbalstītās kartes nodrošinājuma valstis/reģioni

Šajās valstīs ir pieejami Commerce komponenti un karšu prezentācijas atbalsts no Adyen. Lai skatītu pašreizējo tirdzniecības starptautisko pieejamību, apmeklējiet [lapu](/dynamics365/get-started/availability) Starptautiskā pieejamība.

| Valsts/reģions | Tiek atbalstīts |
| --- | :-: |
| Austrālija | ✔ |
| Austrija | ✔ |
| Beļģija | ✔ |
| Kanāda | ✔ |
| Čehijas Republika | ✔ |
| Dānija | ✔ |
| Igaunija | ✔ |
| Somija | ✔ |
| Francija | ✔ |
| Vācija | ✔ |
| Īpašais administratīvais reģions Honkonga | ✔ |
| Ungārija | ✔ |
| Islande | ✔ |
| Īrija | ✔ |
| Itālija | ✔ |
| Japāna | Turpmākais laidiens |
| Latvija | ✔ |
| Lietuva | ✔ |
| Malaizija | ✔ |
| Nīderlande | ✔ |
| Jaunzēlande | ✔ |
| Norvēģija | ✔ |
| Polija | ✔ |
| Singapūra | ✔ |
| Šveice | ✔ |
| Spānija | ✔ |
| Zviedrija | ✔ |
| Šveice | ✔ |
| Apvienotā Karaliste | ✔ |
| Amerikas Savienotās Valstis | ✔ |
| Brazīlija | Turpmākais laidiens |

#### <a name="supported-card-not-present-countries"></a>Atbalstītā karte, kas nav pieejama valstīs

Tālāk minētajām valstīm/reģioniem tiek nodrošināts Adyen atbalsts kartei, kurai nav darījumu. [Sazinieties ar Adyen](https://www.adyen.com/contact/sales), lai iegūtu sīkāku informāciju par atbalstu konkrētai valstij. Lai skatītu pašreizējo tirdzniecības starptautisko pieejamību, apmeklējiet [lapu](/dynamics365/get-started/availability) Starptautiskā pieejamība.

| Valsts/reģions | 
| --- |
| Argentīna |
| Armēnija |
| Austrālija |
| Austrija |
| Bahreina |
| Beļģija |
| Brazīlija |
| Bulgārija |
| Kanāda |
| Čīle |
| Ķīna |
| Kolumbija |
| Horvātija |
| Kipra |
| Čehijas Republika  |
| Dānija |
| Ēģipte |
| Igaunija |
| Somija |
| Francija |
| Gruzija |
| Vācija |
| Gibraltārs |
| Grieķija |
| Gērnsija |
| Īpašais administratīvais reģions Honkonga |
| Ungārija |
| Islande |
| Indija |
| Indonēzija |
| Īrija |
| Mena |
| Izraēla |
| Itālija |
| Japāna |
| Džērsija |
| Koreja |
| Kuveita |
| Latvija |
| Lietuva |
| Luksemburga |
| Malaizija |
| Malta |
| Meksika |
| Maroka |
| Nīderlande |
| Jaunzēlande |
| Norvēģija |
| Peru |
| Polija |
| Portugāle |
| Katara |
| Rumānija |
| Saūda Arābija |
| Serbija |
| Singapūra |
| Slovākija |
| Slovēnija |
| Dienvidāfrikas Republika |
| Spānija |
| Zviedrija |
| Šveice |
| Taivāna |
| Tanzānija |
| Taizeme |
| Turcija |
| Apvienotie Arābu Emirāti (AAE) |
| Apvienotā Karaliste |
| Amerikas Savienotās Valstis, tostarp Puertoriko  |

#### <a name="supported-dynamics-365-payment-features"></a>Atbalstītie Dynamics 365 maksājumu līdzekļi

Tālāk esošajā tabulā ir parādīta līdzekļu kopa, ko atbalsta Dynamics 365 Payment Connector for Adyen. Šajās funkcijās tiek izmantoti uzlabojumi, kas tika ieviesti maksājumu SDK un dažos komponentos 2018. gada decembrī. Tie nav ekskluzīvi Dynamics 365 Payment Connector for Adyen. Papildinformāciju par to, kā ieviest šos uzlabojumus citam maksājumu savienotājam, skatiet rakstā [Maksājumu termināļa pilnīga maksājumu integrācijas izveide](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Shēma | Karte ir | Kartes nav |
|---|:-:|:-:|
| [Izņemt dāvanu kartes atlikumu](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Dublēta maksājumu aizsardzība](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Omni kanāla tokenizācija | ✔ | ✔ |
| Saistītās atmaksas | ✔<br>(Sākot ar 10.0.1) | ✔<br>(Sākot ar 10.0.1) |
| [Tiešsaistes maksājumu saglabāšana](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Sākot ar 10.0.2) | 
| [Ārējās dāvanu kartes zvanu centram un e-komercijai](./gift-card.md) | ✔<br>(Sākot ar 10.0.10) | 
| [SCA maksājumu novirzīšana](../adyen_redirect.md) | | ✔<br>(Sākot ar 10.0.12) |
| [Atvēlētie maksājumu termināļi un uzvednes printerim un skaidras naudas atvilktnei](../pos-multi-hws.md) | ✔<br>(Sākot ar 10.0.12) | |
| [SDK līmeņa dzeramnaudas atbalsts, izmantojot Adyen savienotāju](tipping.md) | ✔<br>(Sākot ar 10.0.14) | |
| [Inkrementāla tveršana pasūtījumu rēķinu izrakstīšanai](incremental-capture.md) |  | ✔<br>(Sākot ar 10.0.18) |
| [Maka maksājumi](../wallets.md) |  | ✔<br>(Sākot ar 10.0.20) |
| [Google Pay ar Adyen](google-pay-adyen.md) |  | ✔<br>(Sākot ar 10.0.27) |

## <a name="next-steps"></a>Turpmākās darbības

Informāciju par reģistrēšanos Dynamics 365 Payment Connector for Adyen un tā konfigurēšanu skatiet rakstā [Dynamics 365 Payment Connector for Adyen iestatīšana](adyen-connector-setup.md).

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Payment Connector pakalpojumam Adyen — iestatīšana](adyen-connector-setup.md)

[Dynamics 365 Payment Connector pakalpojumam Adyen — bieži uzdotie jautājumi](adyen-connector-faq.md)

[Dynamics 365 Payment Connector pakalpojumam Adyen — problēmu novēršana](adyen-connector-troubleshoot.md)

[Bieži uzdotie jautājumi par maksājumiem](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
