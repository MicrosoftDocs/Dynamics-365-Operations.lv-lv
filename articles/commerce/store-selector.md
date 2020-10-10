---
title: Veikala atlasītāja modulis
description: Šajā tēmā tiek stāstīts par veikala atlasītāja moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4438e46d4653a0cd2060092695f08613cd696f4e
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818254"
---
# <a name="store-selector-module"></a>Veikala atlasītāja modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par veikala atlasītāja moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Klienti var izmantot veikala atlasītāja moduli, lai paņemtu preci atlasītajā veikalā pēc tiešsaistes pirkšanas. Commerce versijā 10.0.13 veikala atlasītāja modulis ietver arī papildu iespējas, kas var parādīt lapu **Atrast veikalu**, kurā redzami tuvumā esošie veikali.

Veikala atlasītāja modulis ļauj lietotājiem meklēt veikalu rādiusu atrašanās vietu (pilsētu, rajonu, adresi utt.). Kad modulis tiek atvērts pirmo reizi, tas izmanto klienta pārlūka atrašanās vietu, lai atrastu veikalus (ja tiek nodrošināta atļauja).

## <a name="store-selector-module-usage-in-e-commerce"></a>Veikala atlasītāja moduļa izmantošana e-komercijā

- Veikala atlasītāja moduli var izmantot preču detalizētās informācijas lapā (PDP), lai atlasītu veikalu preces saņemšanai.
- Veikala atlasītāja moduli var izmantot groza lapā, lai atlasītu veikalu preces saņemšanai.
- Veikala atlasītāja moduli var izmantot savrupā lapā, kurā redzami visi pieejamie veikali.

## <a name="bing-maps-integration"></a>Bing karšu integrācija

Veikala atlasītāja modulis ir integrēts ar [Bing karšu REST programmas interfeisu (API)](https://docs.microsoft.com/bingmaps/rest-services/), lai izmantotu Bing ģeogrāfiskās kodēšanas un automātiskās ieteikšanas līdzekļus. Nepieciešama Bing karšu API atslēga, un tā ir jāpievieno kopīgo parametru lapā pakalpojumā Commerce headquarters. Ģeogrāfiskās kodēšanas API tiek izmantots, lai konvertētu novietojumu uz platuma un garuma vērtībām. Integrācija ar Automātiskās ieteikšanas API tiek izmantots, lai parādītu meklēšanas ieteikumus, kad lietotāji meklēšanas laukā ievada atrašanās vietas.

Automātiskā ieteikšanas REST API jums ir jānodrošina, ka ir atļauti šādi vietrāži URL (pazīstami arī kā "baltajā sarakstā") jūsu vietnes satura drošības politikai (CSP). Šis iestatījums tiek veikts Commerce vietnes veidotājā, pievienojot atļautos vietrāžus URL dažādām vietnes CSP direktīvām (piemēram, **img-src**). Papildinformāciju skatiet [Satura drošības politika](manage-csp.md). 

- **connect-src** direktīvai pievienojiet **&#42;.bing.com**.
- **img-src** direktīvai pievienojiet **&#42;.virtualearth.net**.
- **script-src** direktīvai **pievienojiet &#42;.bing.com, &#42;.virtualearth.net**.
- **script style-src** direktīvai pievienojiet **&#42;.bing.com**.
 
## <a name="pickup-in-store-mode"></a>Saņemšana veikalā režīms

Veikala atlasītāja modulis atbalsta **Saņemšanu veikalā** režīmu, kas parāda veikalu sarakstu, kur produkts ir pieejams saņemšanai. Tas arī parāda veikala stundas un preču inventāru katram veikalam sarakstā. Veikala atlasītāja modulim ir nepieciešams preces saturs, kas atveido preces pieejamību un ļauj lietotājam pievienot preci grozam, ja preces piegādes režīms ir iestatīts uz **saņemšanu** atlasītajā veikalā. Papildinformāciju skatiet [Krājumu iestatījumi](inventory-settings.md). 

Veikala atlasītāja moduli var pievienot pirkšanas kastes modulim PDP, lai parādītu veikalus, kuros prece ir pieejama saņemšanai. To var pievienot arī groza modulim. Šādā gadījumā veikala atlasītāja modulis parāda saņemšanas opcijas katram groza rindas elementam. Veikala atlasītāja modulis var arī tikt pievienots citām lapām vai moduļiem, izmantojot paplašinājumus un pielāgojumus.

Lai šis scenārijs darbotos, precēm jābūt konfigurētām lai tiktu izmantots **saņemšanas** piegādes veidu. Pretējā gadījumā modulis netiks uzrādīts preču lapās. Papildinformācijai par piegādes režīma konfigurēšanu skatiet rakstā [Piegādes veidu iestatīšana](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Šajā attēlā redzams veikala atlasītāja moduļa piemērs, kas izmantots PDP.

![Veikala atlasītāja moduļa piemērs, kas izmantots PDP](./media/BOPIS.PNG)

## <a name="find-stores-mode"></a>Atrast veikalu režīms

Veikala atlasītāja modulis atbalsta arī **Atrast veikalu** režīmu. Šo režīmu var izmantot, lai izveidotu veikala atrašanās vietu lapu, kas parāda pieejamos veikalus un to informāciju. Šajā režīmā veikala atlasītāja modulis darbojas bez preces konteksta, un to var izmantot kā savrupu moduli jebkurā vietnes lapā. Turklāt, ja atbilstošie iestatījumi ir ieslēgti modulī, lietotāji var izvēlēties veikalu kā vēlamo veikalu. Kad veikals tiek izvēlēts kā lietotāja vēlamais veikals, veikala ID tiek saglabāts pārlūka sīkfailā. Tāpēc lietotājam ir jāapstiprina sīkfaila piekrišanas ziņojums.

Sekojošajā attēlā redzams veikala atlasītāja moduļa piemērs, kas tiek izmantots kopā ar kartes moduli veikala atrašanās vietu lapā.

![Veikala atlasītāja moduļa un kartes moduļa piemērs veikala atrašanās vietu lapā](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>Atveidot karti

Veikala atlasītāja moduli var izmantot kopā ar kartes moduli, lai parādītu veikala atrašanās vietas kartē. Plašāku informāciju par kartes moduli skatiet [Kartes modulis](map-module.md)

## <a name="store-selector-module-properties"></a>Veikala atlasītāja moduļa rekvizīti

| Rekvizīta nosaukums | Vērtība | apraksts |
|---------------|-------|-------------|
| Virsraksts | Teksts | Moduļa virsraksts. |
| Veids | **Atrast veikalus** vai **Saņemt veikalā** | **Atrast veikalu** režīmā tiek rādīti pieejamie veikali. **Saņemt veikalā** režīms ļauj lietotājiem atlasīt veikalu preces saņemšanai. |
| Stils | **Dialogs** vai **Iekļautais** | Moduli var atveidot vai nu kā iekļautu, vai dialoglodziņā. |
| Iestatīt kā vēlamo veikalu | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, lietotāji var iestatīt vēlamo veikalu. Šim līdzeklim nepieciešams, lai lietotāji pieņemtu sīkfailu piekrišanas ziņojumu. |
| Rādīt visus veikalus | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, lietotāji var apiet rekvizītu **Meklēt rādiusu** un skatīt visus veikalus. |
| Automātiskās ieteikšanas opcijas: maksimālie rezultāti | Skaits | Šis rekvizīts nosaka maksimālo ieteikto rezultātu skaitu, ko var parādīt, izmantojot Bing automātiskās ieteikšanas API. |
| Meklēšanas rādiuss | Skaits | Šis rekvizīts nosaka veikalu meklēšanas rādiusu jūdzēs. Ja nav norādīta vērtība, tiek izmantots noklusētais meklēšanas rādiuss, kas ir 50 jūdzes. |
| Pakalpojuma noteikumi | Vietrādis URL |  Šis rekvizīts norāda pakalpojuma URL nosacījumus, kas nepieciešami Bing karšu pakalpojuma izmantošanai. |

## <a name="add-a-store-selector-module-to-a-page"></a>Veikala atlasītāja moduļa pievienošana lapai

**Saņemt veikalā** režīms moduli var izmantot tikai PDP un groza lapās. Jums ir jāiestata režīms **Saņemt veikalā** moduļa rekvizītu rūtī.

- Lai iegūtu informāciju par to, kā pievienot veikala atlasītāja moduli pirkšanas kastes modulim skatiet rakstu [Pirkšanas kastes modulis](add-buy-box.md). 
- Lai iegūtu informāciju par to, kā pievienot veikala atlasītāja moduli groza modulim skatiet rakstu [Groza modulis](add-cart-module.md)

Lai konfigurētu veikala atlasītāja moduli, lai rādītu veikala atrašanās vietu lapu pieejamos veikalus, kā iepriekš šajā tēmā attēlotajā ilustrācijā, veiciet sekojošās darbības.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet **Mārketinga veidne** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet veidni **Mārketinga veidne**. Sadaļā **Lapas nosaukums** ievadiet **Veikala atrašanās vietas** pēc tam atlasiet **Labi**.
1. Jaunās lapas slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners ar 2 kolonnām** un pēc tam atlasiet **Labi**.
1. Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**.
1. Iestatiet **Ekstra maza skata porta kolonnas konfigurācijas** vērtību uz **100%**.
1. Iestatiet **Maza skata porta kolonnas konfigurācijas** vērtību uz **100%**.
1. Iestatiet **Vidēja skata porta kolonnas konfigurācijas** vērtību uz **33% 67%**.
1. Iestatiet **Liela skata porta kolonnas konfigurācijas** vērtību uz **33% 67%**.
1. Slotā **Konteiners ar 2 kolonnām** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Veikalu atlasītājs** un pēc tam atlasiet **Labi**.
1. Moduļa rekvizītu rūtī iestatiet **Režīma** vērtību, lai **Atrastu veikalus**.
1. Iestatiet **Meklēt rādiusa** vērtību jūdzēs.
1. Pēc nepieciešamības iestatiet citus rekvizītus, piemēram, **Iestatīt kā vēlamo veikalu**, **Rādīt visus veikalus** un **Iespējot automātisko ieteikšanu**.
1. Slotā **Konteiners ar 2 kolonnām** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Karte** un pēc tam atlasiet **Labi**.
1. Moduļa rekvizītu rūtī iestatiet jebkādus papildu rekvizītus, kas nepieciešami.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
 
## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Īss PDP apskats](quick-tour-pdp.md)

[Īss groza un norēķināšanās apskats](quick-tour-cart-checkout.md)

[Iestatiet piegādes veidus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Bing karšu pārvaldība organizācijā](dev-itpro/manage-bing-maps.md)

[Bing karšu REST API](https://docs.microsoft.com/bingmaps/rest-services/)

[Karšu modulis](map-module.md)
