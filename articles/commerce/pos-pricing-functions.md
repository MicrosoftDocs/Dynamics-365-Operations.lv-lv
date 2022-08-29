---
title: Cenu noteikšanas funkcijas POS
description: Šajā rakstā ir aprakstītas dažādas cenu un atlaižu funkcijas Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) programmā.
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 92bbc3b81b889f106dc113528afbdc37d1106ff3
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2022
ms.locfileid: "9293656"
---
# <a name="pricing-functions-in-pos"></a>Cenu noteikšanas funkcijas POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā rakstā ir aprakstītas dažādas cenu un atlaižu funkcijas Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) programmā.

POS Dynamics 365 Commerce programma nodrošina bagātinātas iespējas, kas ļauj pirmās rindas darbiniekiem veikt veikala Commerce operācijas. Tabulā ir parādītas cenas un atlaides funkcijas, kas pašreiz pieejamas programmā.

| Funkcija                       | POS operācijas |
|--------------------------------|----------------|
| Skatiet cenas                    | [Cenas pārbaude](#price-check) |
| Skatīt atlaides                 | [Skatīt visas atlaides](#view-all-discounts)<br>[Skatīt pieejamās atlaides](#view-available-discounts) |
| Ignorēt cenas                | [Cenas ignorēšana](#price-override) |
| Lietot vai noņemt atlaides      | [Rindas atlaides summa](#line-discount-amount)<br>[Rindas atlaide procentos](#line-discount-percent)<br>[Beigu atlaides summa](#total-discount-amount)<br>[Beigu atlaides procenti](#total-discount-percent)<br>[Noņemt sistēmas atlaides no darījuma](#remove-system-discounts-from-transaction)<br>[Atkārtoti lietot sistēmas atlaides](#reapply-system-discounts) |
| Lietot vai noņemt kuponus        | [Pievienot kupona kodu](#add-coupon-code)<br>[Noņemt kupona kodu](#remove-coupon-code) |
| Aprēķināt cenas un atlaides | [Pārrēķināt](#recalculate) |

Informāciju par to, kā iepriekšējās operācijas var konfigurēt POS programmā un vai tās atbalsta bezsaistes režīmu, [skatiet tiešsaistes un bezsaistes pārdošanas punkta (POS) operācijām](pos-operations.md).

## <a name="price-check"></a>Cenas pārbaude

Izmantojot **cenu pārbaudes** operāciju, POS lietotāji var atrast iepriekš konfigurētas cenas noteiktai precei.

## <a name="view-all-discounts"></a>Skatīt visas atlaides

Izmantojot **visu atlaižu operāciju**, POS lietotāji var skatīt visus efektīvos veicināšanas pasākumus, kas pašlaik tiek darbināti veikala kanālā. Šajā operācijā ir uzskaitītas visas atlaides, kas atbilst jebkuriem šiem nosacījumiem:

- Atlaides cenu grupa atbilst veikala cenu grupai.
- Atlaides cenu grupa tiek kartēta uz piederības vai lojalitātes programmu.
- Atlaides cenu grupa tiek kartēta uz katalogu, kas ir saistīts ar veikalu.

Operācijā **Skatīt visas atlaides ir redzamas** tikai tās atlaides, kas neceno ar jau piemērotām atlaidēm. Šī darbība palīdz nodrošināt, ka, ja pārdošanas asistents informē klientu par atlaidi un klients veic nepieciešamo darbību (piemēram, klients pērk vēl vienu preci, lai iegūtu 10 procentu atlaidi), transakcijai tiek piemērota atlaide. Kuponam pamatotas atlaides tiek rādītas tikai tad, ja ir **ieslēgts parametrs** Lietot bez kupona koda.

Veicot darbību **Skatīt visas atlaides**, POS lietotāji var meklēt atlaides pēc nosaukuma un apraksta, kā arī var filtrēt atlaides, balstoties uz to, vai lietotājam ir nepieciešams kupons.

## <a name="view-available-discounts"></a>Skatīt pieejamās atlaides

Izmantojot **pieejamo atlaižu operāciju**, POS lietotāji var skatīt visas atlaides, kas attiecas uz atlasīto darbības vai visas darbības rindu. Atlaides, kas ir piemērojamas atlasītajai rindai, ietver atlaides, kas jau ir piemērotas, un atlaides, kas vēl nav piemērotas, bet kuras var lietot (piemēram, komplekta atlaides, kurām nepieciešamas papildu preces). **Ja** piemērojamā atlaide ir saistīta ar kuponu, kur ir ieslēgts parametrs Lietot bez kupona koda, POS lietotājs var arī izmantot kuponu **funkciju** šīs operācijas laikā, lai izpirktu kuponu tieši bez nepieciešamības ievadīt vai skenēt kuponu kodus vai kuponu svītrkodus.

## <a name="price-override"></a>Cenas ignorēšana

Cenas **ignorēšanas** operācija pos lietotājiem ļauj ignorēt darbībā lietotās preces pārdošanas cenu. Šī operācija darbojas tikai precēm, kas ir konfigurētas cenu ignorēšanai.

## <a name="line-discount-amount"></a>Rindas atlaides summa

Izmantojot **rindas atlaides summas** operāciju, POS lietotāji var ievadīt rindas preces atlaides summu darbībā. Šī operācija attiecas tikai uz krājumiem, kuriem var piešķirt atlaidi, un tajā tiek ievērota maksimālā rindas **atlaides** summas vērtība, kas lietotājam ir norādīta POS atļauju grupā.

## <a name="line-discount-percent"></a>Rindas atlaide procentos

Rindas **atlaides procentuālās** vērtības operācija pos lietotājiem ļauj ievadīt darbībā lietotās rindas krājuma atlaides procentus. Šī operācija attiecas tikai uz krājumiem, kuriem var piešķirt atlaidi, un tajā tiek ievērota **maksimālā** rindas atlaides procentuālā vērtība, kas lietotājam ir norādīta POS atļauju grupā.

## <a name="total-discount-amount"></a>Beigu atlaides summa

Operācija **Kopējās atlaides summa** pos lietotājiem ļauj ievadīt darbības atlaižu summu. Šī operācija attiecas tikai uz krājumiem, kuriem var piešķirt atlaidi, un tajā tiek ievērota maksimālā kopējās **atlaides** summas vērtība, kas lietotājam ir norādīta POS atļauju grupā. Ja ievadītā atlaides summa pārsniedz maksimālo beigu atlaides summu, operācija tiek bloķēta un atļaujas ignorēšanas plūsma netiek izraisīta. Pašlaik kopējo atlaides summu nevar piemērot grozam, kurā ir pārdošanas krājumu un atgriezto krājumu kombins.

## <a name="total-discount-percent"></a>Beigu atlaides procenti

Operācija **"Beigu atlaides procenti** " ļauj POS lietotājiem ievadīt darbības atlaides procentus. Šī operācija attiecas tikai uz krājumiem, kuriem var piešķirt atlaidi, un tajā tiek ievērota **maksimālā** kopējā atlaides procentuālā vērtība, kas lietotājam ir norādīta POS atļauju grupā. Ja ievadītā atlaides procentuālā vērtība pārsniedz maksimālo kopējo atlaidi procentos, operācija tiek bloķēta un netiek izraisīta atļauju ignorēšanas plūsma. Pašlaik kopējo atlaides procentuālo vērtību nevar piemērot grozam, kurā ir pārdošanas krājumu un atgriezto krājumu kombins.

## <a name="remove-system-discounts-from-transaction"></a>Noņemt sistēmas atlaides no darījuma

Izmantojot **darbību operācijas Noņemt sistēmas** atlaides, POS lietotāji var nodzēst visas piemērotās sistēmas atlaides (tostarp kupona atlaides) no darbības. Pēc šīs operācijas veikšanas cenu noteikšanas programma sāk izslēgt sistēmas atlaides no atlaižu aprēķināšanas tvēruma. Operācijai **Noņemt sistēmas atlaides no darbības** netiek noņemtas manuālas atlaides.

## <a name="reapply-system-discounts"></a>Atkārtoti lietot sistēmas atlaides

Izmantojot **sistēmas atlaižu atkārtotas** izmantošanas darbību, POS lietotāji var atkārtoti lietot sistēmā aprēķinātās atlaides darbībai, ja atlaides tika noņemtas, izmantojot darbības operācijas **sistēmas atlaižu** noņemšanas iespēju. Pēc šīs operācijas veikšanas cenu noteikšanas programma sāk iekļaut visas sistēmas atlaides atlaižu aprēķināšanas tvērumā.

## <a name="add-coupon-code"></a>Pievienot kupona kodu

Izmantojot **operāciju Pievienot kupona** kodu, POS lietotāji var darījumam pievienot kuponu, ievadot kupona kodu. Pos lietotāji var arī skenēt kupona svītrkodu vai ievadīt to, izmantojot ciparu tastatūru darbību **ekrānā**.

## <a name="remove-coupon-code"></a>Noņemt kupona kodu

Izmantojot **operāciju Kupona koda** noņemšana, POS lietotāji var atlasīt un noņemt vienu vai vairākus kuponus, kas pašlaik tiek piemēroti darbībai.

## <a name="recalculate"></a>Pārrēķināt

Izmantojot **pārrēķina** operāciju, POS lietotāji var aktivizēt cenas aprēķināšanu pēc pieprasījuma. Šī operācija ir nepieciešama, kad ir iespējota cenu bloķēšana un/vai aizkavēta cenu aprēķināšana un POS lietotājs vēlas pārrēķināt cenas un atlaides pēc groza vai pasūtījuma maiņas. Pārrēķina **operācija** vienmēr pārrēķina visu pasūtījumu. To nevar izmantot atlasīto pārdošanas rindu pārrēķinam. Lai POS bloķētai pārdošanas rindai piemērotu manuālas atlaides, POS **lietotājiem vispirms ir jāizmanto operācija Pārrēķins**, lai atbloķētu visas pārdošanas rindas.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
