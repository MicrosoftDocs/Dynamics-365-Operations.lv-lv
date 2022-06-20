---
title: Customer Voice integrācija e-komercijas vietnes lapās
description: Šajā rakstā ir aprakstīts, kā integrēt Microsoft Dynamics 365 Customer Voice Dynamics 365 Commerce e-komercijas vietnes lapās.
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: c8c67ecf4950c92fc91c8d119e06e5e8afff0ddf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850334"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>Customer Voice integrācija e-komercijas vietnes lapās

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā integrēt Microsoft Dynamics 365 Customer Voice Dynamics 365 Commerce e-komercijas vietnes lapās.

Jūs varat integrēt Debitora [debitora debitora](https://dynamics.microsoft.com/customer-voice/overview/) informāciju savā e-komercijas vietnē, lai apkopotu, analizētu un izsekotu reāllaika klientu atsauksmes. Lai uzsāktu integrāciju, ir jāizveido konts un jāatlasa debitora projekta veidne tā atsauksmju tipam, ko vēlaties apkopot.

## <a name="integrate-the-customer-voice-service"></a>Integrēt klientu debitora debitora pakalpojumu

Lai izveidotu debitora debitora debitora kontu, dodieties uz debitora [debitoram](https://dynamics.microsoft.com/customer-voice/overview/) un sekojiet uzvedēm.

Pēc debitora debitora debitora konta izveidošanas un pieteikšanās, nākamais solis ir atlasīt projekta veidni atsauksmju tipam, ko vēlaties apkopot.

Lai atlasītu debitora debitora projekta veidni, sekojiet šiem soļiem.

1. Dodieties uz [debitora debitora debitora debitora projekta veidnes lapu](https://customervoice.microsoft.com/Pages/ProjectPage.aspx).
1. Atlasiet **Sākt**.
1. Atlasiet projekta veidni atsauksmju tipam, ko vēlaties apkopot un pēc tam atlasiet **Tālāk**.
1. Cilnes Sūtīt **sadaļā** Izvēlēties iegultu **formātu** atlasiet iegulto formātu. Iegultā **koda lauks** rāda kodu, kas ir iegults Commerce Site Builder.

Šajā rakstā sniegti piemēri izmanto periodisko klientu **aptaujas projekta** veidni un Pogas iegulto **formātu**.

Šajā piemērā ir redzama **periodisko** klientu aptaujas projekta veidnes lapa, **kur** ir atlasīta pogas iegulta formāta opcija un **iegults kods šai opcijai tiek parādīts laukā Iegults** kods. Ir nepieciešamas trīs atsevišķas darbības, lai iegultu norādīto kodu jūsu vietnes lapās, kā aprakstīts šādās sadaļās.

![Debitora Periodisku klientu aptaujas lapa ar atlasītu pogas opciju.](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>Iegult ārējā skripta URL

Visās vietnes lapās, kurās ir jābūt debitora Debitora Debitora debitora aptaujai, ir jāie iegults ārējā skripta URL, kuru iegultā kodā norāda debitors Vai. Labākais veids, kā iegult skriptu vairākās vietnes lapās, ir izveidot fragmentu vietas veidotājā, kas satur ārēju skripta URL, un tad pievienot fragmentu atbilstošajām lapas veidnēm. Pēc atjauninātas veidnes publicēšanas iegultais ārējā skripta kods ir līdzīgs ietekmēto vietņu lapu piemēram.

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

Papildinformāciju par fragmentiem skatiet sadaļā [Darbs ar fragmentiem](work-with-fragments.md).

> [!NOTE]
> Fragmentam ir jāpievieno tikai vietrādis URL. Ārējais skripta modulis pievienos citu skripta kodu.

Lai iegultu ārējā skripta URL fragmentā, izpildiet šīs darbības.

1. Vietas veidotājā izveidojiet fragmentu, kas ir balstīts uz [ārējā skripta moduli](script-module.md).
1. Jaunajā fragmentā atlasiet noklusējuma ārējā **skripta slotu**.
1. Noklusējuma ārējā **skripta rekvizītu** rūts **laukā** Skripta avots ievadiet ārējā skripta URL, kā parādīts šajā piemēra attēlā.

    ![Ārējā skripta URL skripta avota laukā jaunajam fragmentam.](media/customer-voice-integration-2.png)

1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet Publicēt **,** lai publicētu fragmentu.

Jaunais fragments, kas satur iegultos ārējos skriptu blokus, tagad ir gatavs pievienošanai atbilstošai lapas veidnei.

### <a name="embed-the-external-style-sheet-code"></a>Iegult ārējā stila lapas kodu

Pēc tam visās vietnes lapās, kurās ir jābūt debitora Debitora Tola aptaujai, ir jāie iegults ārējā stila lapas kods, kuru debitors Ir sniedzis iegultā kodā. Tāpat kā iepriekšējā sadaļā, labākais veids, kā iegult ārējās stila lapas kodu vairākās vietnes lapās, ir izveidot fragmentu vietas veidotājā, kas satur stila lapas kodu, un pēc tam pievienot šo fragmentu atbilstošajām lapu veidnēm. Iegultais ārējās stila lapas kods būs līdzīgs šim piemēra kodam.

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

Lai iegultu ārējā stila lapas kodu fragmentā, veiciet šīs darbības.

1. Vietas veidotājā izveidojiet fragmentu, kas ir balstīts uz [metatags moduli](metatags-module.md).
1. Fragmentā atlasiet noklusējuma metadatu **slotu**.
1. **Noklusējuma metadatu rekvizītu rūtī** **metadatu** tagu laukā ievadiet stila lapas kodu, kā parādīts šajā piemēra attēlā.

    ![Ārējā stila lapas kods jaunā fragmenta metadatu tagu laukā.](media/customer-voice-integration-3.png)

1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet Publicēt **,** lai publicētu fragmentu.

Jaunais fragments, kas satur iegulto ārējās stila lapas kodu, tagad ir gatavs pievienošanai atbilstošai lapas veidnei.

### <a name="embed-the-inline-script-code"></a>Iegult iekļauto skripta kodu 

Pēc tam visās vietnes lapās, kurās jābūt debitora Debitora Debitora debitora aptaujai, ir jāieietu tajā skripta kods, kuru debitors Ir sniedzis iegultā kodā. Tāpat kā iepriekšējās sadaļās, labākais veids, kā iegult inline skripta kodu vairākās vietnes lapās, ir izveidot fragmentu vietas veidotājā, kas satur iekļauto skripta kodu, un tad pievienot fragmentu atbilstošajām lapas veidnēm.

Tālāk sniegtajā inline skripta koda piemērā APTAUJAS **ATSLĒGA\_ ir** vietturis. APSKAta atslēgas **vērtībai\_** jāatbilst faktiskajai apskata atslēgai, ko debitoram Debitoram ir norādīts iegultā kodā. Pēdējā rinda izsauks kodu, lai atveidotu apskata pogu pēc vienas otrās, lai nodrošinātu, ka skriptiem ir pietiekami daudz laika, lai to varētu ielādēt. Atkarībā no atlasītās aptaujas, iespējams, ir jāpievieno vai jāatjaunina citi metadati, piemēram, uzņēmuma nosaukums.

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

Lai iegultu iekļauto skripta kodu fragmentā, veiciet šīs darbības.

1. Vietas veidotājā izveidojiet fragmentu, kas ir balstīts uz [Inline skripta moduli](script-module.md).
1. Fragmentā atlasiet noklusējuma iekļauto **skripta slotu**.
1. Noklusējumaline **skripta rekvizītu** rūtī, **kas atrodas laukā Inline skripts**, ievadiet iekļauto skripta kodu, kā parādīts šajā piemēra attēlā.

    ![Inline skripta kods jaunā fragmenta inline skripta laukā.](media/customer-voice-integration-4.png)

1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet Publicēt **,** lai publicētu fragmentu.

Jaunais fragments, kas satur iegulto iekļauto skripta kodu, tagad ir gatavs pievienošanai atbilstošai lapas veidnei.

## <a name="add-fragments-to-a-template"></a>Pievienot veidnei fragmentus

Kad esat beidzis veidot fragmentus, kas ietver debitora Embedded kodu, tos jāpievieno lapu veidnēm, kas ir saistītas ar vietnes lapām, kuras vēlaties tās izmantot. Šajā piemēra piemērā trīs piemēra fragmenti ir pievienoti preces informācijas lapai (PDP) veidnei.

![Piemēram, fragmenti, kas pievienoti PDP veidnei.](media/customer-voice-integration-5.png)

Kad atjauninātā veidne ir publicēta, debitora debitora aptauja tiks parādīta visās lapās, kuras kontrolē veidne.

Papildinformāciju par veidnēm skatiet [sadaļā Darbs ar veidnēm](work-with-templates.md).

## <a name="configure-content-security-policy"></a>Konfigurēt satura drošības politiku

Pēc noklusējuma satura drošības politika (MAKS) neļauj veikt zvanus uz citiem pakalpojumiem, izņemot gadījumus, kad tiek veikta papildu konfigurācija. Tādēļ pēc atjaunināto veidņu publicēšanas ir iespējams, ka aptauja netiks ielādēta attiecīgajās vietņu lapās. Lai apskatītu ar ATVĒRI saistītas kļūdas, atveriet web pārlūkprogrammas izstrādātāja rīkus (F12) un tad dodieties uz lapu, kurā atrodas aptauja. AR KOLONNU saistītās kļūdas tiks parādītas konsoles izvadē.

Lai vietas veidotājā konfigurējiet MANUĀLI, lai labotu kļūdas, veiciet šos soļus.

1. Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.
1. **Cilnē Satura drošības** politika pievienojiet `https://customervoice.microsoft.com/` bērnu **drošības direktīvai**.
1. Pievienojiet `https://customervoice.microsoft.com/` rāmja **un riksa direktīvai**.
1. Pievienojiet `https://mfpembedcdnmsit.azureedge.net` un **azureedge.net** pie **img-src** direktīvas.

Papildinformāciju skatiet [Satura drošības politika](manage-csp.md).

## <a name="additional-resources"></a>Papildu resursi

[Ārējā skripta modulis](script-module.md)

[Metatagu modulis](metatags-module.md)

[Iekļauto skriptu modulis](script-module.md)

[Satura drošības politika](manage-csp.md)

[Darbs ar fragmentiem](work-with-fragments.md)

[Darbs ar veidnēm](work-with-templates.md)
