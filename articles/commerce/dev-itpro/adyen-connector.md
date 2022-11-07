---
title: Dynamics 365 Payment Connector pakalpojumam Adyen — pārskats
description: Šajā rakstā ir sniegts pārskats par Microsoft Dynamics 365 Maksājumu savienotāju, kas paredzēts Amaksānei.
author: rassadi
ms.date: 10/27/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 931fc69cda8daa2e06b6f1155fbf0369fd2bca55
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728296"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Dynamics 365 Payment Connector pakalpojumam Adyen — pārskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par Microsoft Dynamics 365 Maksājumu savienotāju Aenoen un ietver vispārēju atbalstīto funkciju un funkciju sarakstu. Saistītie priekšmeti aptver pierakstīšanu ar Ahaen, savienotāja konfigurāciju, bieži uzdotiem jautājumiem un traucējumnovēršanas norādes par dažiem bieži uzdotiem jautājumiem.

## <a name="key-terms"></a>Galvenie termini

| Termiņš | Apraksts |
|---|---|
| Maksājumu savienotājs | Paplašinājums, kas atvieglo sakarus Microsoft Dynamics 365 Commerce starp (un saistītajiem komponentiem) un maksājumu pakalpojumu. Šajā rakstā aprakstītais savienotājs tika ieviests, izmantojot standarta maksājumu programmatūras izstrādes komplektu (SDK). |
| Karte ir | Attiecas uz maksājumu darbībām, kur ir uzrādīta un izmantota Dynamics 365 pārdošanas punkta maksājumu termināļa savienotājā. |
| Kartes nav | Attiecas uz maksājumu darbībām, kurās nav fiziskas kartes, piemēram, e-komercijas vai zvanu centra scenāriji. Šajos scenārijos ar maksājumiem saistītā informācija tiek ievadīta manuāli e-Commerce vietnē, zvanu centra plūsmā vai pārdošanas punktā vai maksājumu terminālī. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Atbalstītie līdzekļi, funkcionalitāte, versijas un termināļi

Dynamics 365 maksājumu savienotājs, kas atrodas izvēles rūtiņai Amaksājoten, izmanto standarta maksājumu SDK. Tāpēc tai nav īpašas iespējas, kas nav pieejamas arī citiem maksājumu savienotājiem.

### <a name="supported-versions"></a>Atbalstītās versijas

#### <a name="microsoft-dynamics-365-supported-versions"></a>Microsoft Dynamics 365 atbalstītās versijas
Pirmā puses programma Dynamics 365 Payment Connector for A papildmaksai Microsoft Dynamics tiek atbalstīta 365 Finanšu versijā 8.1.3 (2019. gada janvāris) vai vēlāk un Microsoft Dynamics 365 Retail versijā 8.1.3 vai vēlāk. Tomēr trešās puses vēl aizvien var izstrādāt citus Amaksājoten maksājumu savienotājus agrākām Microsoft Dynamics 365 versijām.

#### <a name="supported-adyen-firmware-versions"></a>Atbalstītās Ahaen jaunākas versijas

Tālāk redzamajā sarakstā ir aprakstītas minimālās un maksimālās Ahaen šo versiju versijas, kas tiek atbalstītas katrai POS versijai Microsoft Dynamics 365 Retail.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail POS versija 10.0.25
| Minimālā Ahas ēnkopas versija | Maksimālā Ahaen transportlīdzekļu versija |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail POS versija 10.0.26
| Minimālā Ahas ēnkopas versija | Maksimālā Ahaen transportlīdzekļu versija |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail POS versija 10.0.27
| Minimālā Ahas ēnkopas versija | Maksimālā Ahaen transportlīdzekļu versija |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail POS versija 10.0.28
| Minimālā Ahas ēnkopas versija | Maksimālā Ahaen transportlīdzekļu versija |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail POS versija 10.0.29
| Minimālā Ahas ēnkopas versija | Maksimālā Ahaen transportlīdzekļu versija |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail POS versija 10.0.30
| Minimālā Ahas ēnkopas versija | Maksimālā Ahaen transportlīdzekļu versija |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Ahaen var izlaist papildversija atjauninājumus pēc tam, kad Microsoft testē galveno versiju. Kamēr tiek atbalstīta galvenā versija, ir labi, ka papildversija atjaunina vienu galveno versiju. Šie atjauninājumi parasti ir ļoti mērķtiecīgi labojumi un neatbilst svītrkodam pilnīgai atkārtotai pārbaudei, kamēr tā pati galvenā Produkta versija tika iepriekš testēta. Atjauninājumi nedrīkst pārsniegt dokumentācijā norādīto maksimālo Ahaen vērtība versiju. 
>
> Migrējot no A pār 53. versijas uz versiju 53, ir nepieciešama POS KB **4577957** Commerce ikmēneša atjauninājumiem versijās 10.0.11 līdz 10.0.14. Ja viena no šīm versijām tiek izmantota un tajā nav iekļauts labojumfails, maksājumu termināļa grāmatošana ļaus veikt tikai maksājumus, izmantojot NFC. Piemērojot labojumfailu POS, tiek atrisināta šī problēma. Ja POS versija ir vecāka par versiju 10.0.11, fails atbalsta pieprasījumu, kas norāda, ka, lai ārpus pakalpojuma MPOS būtu nepieciešams labojums KB **4577957**.
> 
> Audeen par versijām 59p7 līdz 62p9, dāvanu kartes iztēršanas operācija pieprasa PIN ierakstu divreiz scenārijos, **kuros** dāvanu karte tiek ievadīta manuāli. Šī problēma netiek pavairota, kad tiek lasīta dāvanu karte. Darbinieks tiek pētīts. 

### <a name="supported-payment-terminals"></a>Atbalstītie maksājumu termināļi
Dynamics 365 maksājumu savienotājs Aagnosen izmanto ierīces diagnostikā Aagnostic [Aagnosen maksājumu termināļa API priekšrocības](https://www.adyen.com/blog/introducing-the-terminal-api). Tas atbalsta visus maksājumu termināļus, ko atbalsta šis programmas programmēšanas interfeiss (API). Lai iegūtu pilnīgu atbalstīto maksājumu termināļu sarakstu, apmeklējiet [lapu Apozitoen POS termināļi](https://www.adyen.com/pos-payments/terminals).

### <a name="supported-payment-instruments"></a>Atbalstītie maksājumu instrumenti

#### <a name="supported-debit-and-credit-cards"></a>Atbalstītās debetkartes un kredītkartes

| Zīmols | Variants | Karte ir | E-komercija | Zvanu centrs |
|---|---|:-:|:-:|:-:|
| MasterCard | Kredīts | ✔ | ✔ | ✔ |
| MasterCard | Debets | ✔ | ✔ | ✔ |
| MasterCard | Alfa bankas prēmija | ✔ | ✔ | ✔ |
| MasterCard | Darba apmaksa | ✔ |  |  |
| MasterCard | Darba apmaksa | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Neapmaksātās algas | ✔ |  |  |
| MasterCard | Maestro Apvienotā Karaliste | ✔ | ✔ | ✔ |
| VĪZU | Kredīts | ✔ | ✔ | ✔ |
| VĪZU | Debets | ✔ | ✔ | ✔ |
| VĪZU | Alfa bankas prēmija | ✔ | ✔ | ✔ |
| VĪZU | Android Maksāt | ✔ |  |  |
| VĪZU | Darba apmaksa | ✔ |  |  |
| VĪZU | Darba apmaksa | ✔ |  |  |
| VĪZU | VISA pārbaude | ✔ | ✔ | ✔ |
| VĪZU | VISA Dankort | ✔ | ✔ | ✔ |
| VĪZU | VISAHitecario | ✔ | ✔ | ✔ |
| VĪZU | VISA Aravia karte | ✔ | ✔ | ✔ |
| AMEX | Kredīts | ✔ | ✔ | ✔ |
| AMEX | Debets | ✔ | ✔ | ✔ |
| AMEX | Android Maksāt | ✔ |  |  |
| AMEX | Darba apmaksa | ✔ |  |  |
| AMEX | Darba apmaksa | ✔ |  |  |
| AMEX | AMEX komerciālais | ✔ | ✔ | ✔ |
| AMEX | AMEX patērētāja | ✔ | ✔ | ✔ |
| AMEX | AMEX korporatīvā | ✔ | ✔ | ✔ |
| AMEX | AMEX mazs uzņēmums | ✔ | ✔ | ✔ |
| Atklāt | Standarta | ✔ | ✔ | ✔ |
| Atklāt | Android Maksāt | ✔ |  |  |
| Atklāt | Darba apmaksa | ✔ |  |  |
| Atklāt | Darba apmaksa | ✔ |  |  |
| Diners   | Standarta | ✔ | ✔ | ✔ |
| Dineromail | Standarta | ✔ | ✔ | ✔ |
| Jcb | Standarta | ✔ | ✔ | ✔ |
| Union Pay\* | Standarta | ✔ |  |  |
| Interakt debets\* | Standarta | ✔ |  |  |

\* Interac un Union Pay periodiskās kartes marķierus nav sniedzis Aharen, tāpēc tos nevar atbalstīt kartēm ar pašreizējām transakcijām.

#### <a name="supported-gift-cards"></a>Atbalstītās dāvanu kartes
| Shēma | Karte ir | Kartes nav |
|---|:-:|---|
| Piešķirt | ✔ | ✔ |
| Svs | ✔ | ✔ |

Lai atbalstītu šīs ārējās dāvanu karšu shēmas, izmantojot Dynamics 365 maksājumu savienotāju A papildmaksai, jums ir jāveic papildu darbības. Papildinformāciju skatiet sadaļā [Atbalsts ārējai dāvanu kartei](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Atbalstītās vietas

| Shēma | Karte ir | Kartes nav |
|---|---|---|
| Alipay (alipay) | Atbalsts tiks pievienots nākamajā laidienā. | Nē |
| We Vēlu | Atbalsts tiks pievienots nākamajā laidienā. | Nē |

#### <a name="supported-card-present-input-methods"></a>Atbalstītās kartes ievades metodes
| Ievades metode | Tiek atbalstīts | Piezīmes |
|---|:-:|---|
| Dip | ✔ | |
| Lasīt karti | ✔ | |
| Pieskarieties | ✔ | |
| Manuāla ievadne, izmantojot POS UI. |  | Pašlaik netiek atbalstīts |
| Manuāla ievadne, izmantojot maksājumu termināli. | ✔ | Atbalsta manuālu kredīta, debeta un dāvanu karšu ievadi ar PIN ierakstu. | 


#### <a name="supported-card-present-countries"></a>Atbalstītās kartes nodrošinājuma valstis/reģioni

Šīm valstīm/reģioniem ir pieejami Commerce komponenti, un kartei tiek nodrošināts Adyen atbalsts. Lai apmeklētu tirdzniecības pašreizējo starptautisko pieejamību, apmeklējiet [lapu Starptautiskā pieejamība](/dynamics365/get-started/availability).

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
| Japāna | Izlaišana nākotnē |
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
| Brazīlija | Izlaišana nākotnē |

#### <a name="supported-card-not-present-countries"></a>Atbalstītajā kartē nav valstu.

Tālāk minētajām valstīm/reģioniem tiek nodrošināts Adyen atbalsts kartei, kurai nav darījumu. [Sazinieties ar Ahaen](https://www.adyen.com/contact/sales), lai iegūtu sīkāku informāciju par atbalstu noteiktai valstij. Lai apmeklētu tirdzniecības pašreizējo starptautisko pieejamību, apmeklējiet [lapu Starptautiskā pieejamība](/dynamics365/get-started/availability).

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

Tabulā ir parādīta līdzekļu kopa, ko atbalsta Dynamics 365 maksājumu savienotājs Aradien. Šie līdzekļi izmanto uzlabojumus, kas tika ieviesti maksājumu SDK un dažiem komponentiem 2018. gada decembrī. Tie nav ekskluzīvi Dynamics 365 maksājumu savienotājam, kas paredzēts Aradien. Papildinformāciju par to, kā uzpildīs šos uzlabojumus dažādiem maksājumu savienotājiem, [skatiet sadaļā Beigu maksājumu integrācijas izveide maksājumu terminālim](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Shēma | Karte ir | Kartes nav |
|---|:-:|:-:|
| [Izmaksas no dāvanu kartes bilance](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Dublēt maksājumu aizsardzību](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Omni Channel Tokenization | ✔ | ✔ |
| Saistītās atmaksas | ✔<br>(Sākas ar 10.0.1) | ✔<br>(Sākas ar 10.0.1) |
| [Saglabāt tiešsaistes maksājumus](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Sākas ar 10.0.2) | 
| [Ārējās dāvanu kartes zvanu centram un e-komercijai](./gift-card.md) | ✔<br>(Sākas ar 10.0.10) | 
| [SCA maksājuma novirzīšana](../adyen_redirect.md) | | ✔<br>(Sākas ar 10.0.12) |
| [Atvēlētie maksājumu termināļi un uzvednes printerim un skaidras naudas atvilktnei](../pos-multi-hws.md) | ✔<br>(Sākas ar 10.0.12) | |
| [SDK līmeņa izmešanas atbalsts, izmantojot A connector](tipping.md) | ✔<br>(Sākas ar 10.0.14) | |
| [Inkrementāla tveršana pasūtījumu rēķinu izrakstīšanai](incremental-capture.md) |  | ✔<br>(Sākas ar 10.0.18) |
| [Veikt maksājumus](../wallets.md) |  | ✔<br>(Sākas ar 10.0.20) |
| [Neapmaksāts ar Adžienu](google-pay-adyen.md) |  | ✔<br>(Sākas ar 10.0.27) |

## <a name="next-steps"></a>Turpmākās darbības

Informāciju par Dynamics 365 maksājumu savienotāja piereģistrēšanos un konfigurēšanu skatiet Dynamics 365 Maksājumu savienotājs Adžien [iestatīšanai](adyen-connector-setup.md).

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Payment Connector pakalpojumam Adyen — iestatīšana](adyen-connector-setup.md)

[Dynamics 365 Payment Connector pakalpojumam Adyen — bieži uzdotie jautājumi](adyen-connector-faq.md)

[Dynamics 365 Payment Connector pakalpojumam Adyen — problēmu novēršana](adyen-connector-troubleshoot.md)

[Bieži uzdotie jautājumi par maksājumiem](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
