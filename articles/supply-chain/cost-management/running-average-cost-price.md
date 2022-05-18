---
title: Faktiskā vidējo izmaksu cena
description: Krājumu slēgšanas procesa laikā saņemšanas darbības tiek segtas ar izdošanas darbībām, pamatojoties uz krājumu novērtēšanas metodi, kas ir atlasīta vienības krājumu modeļa grupā. Taču pirms krājumu slēgšanas izpildes sistēmā tiek aprēķināta faktiskā vidējo izmaksu cena, kas parasti tiek izmantota, iegrāmatojot izdošanas transakcijas.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d324324312ce9e47b07de8e3de952b8d7c53647
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672183"
---
# <a name="running-average-cost-price"></a>Faktiskā vidējo izmaksu cena

[!include [banner](../includes/banner.md)]

Krājumu slēgšanas procesa laikā saņemšanas darbības tiek segtas ar izdošanas darbībām, pamatojoties uz krājumu novērtēšanas metodi, kas ir atlasīta vienības krājumu modeļa grupā. Taču pirms krājumu slēgšanas izpildes sistēmā tiek aprēķināta faktiskā vidējo izmaksu cena, kas parasti tiek izmantota, iegrāmatojot izdošanas transakcijas.

Sistēma novērtē šo esošo vidējo izmaksu cenu par krājumu, izmantojot šādu formulu:

Novērtētā cena = (Fiziskā summa + Finansiālā summa) ÷ (Fiziskais daudzums + Finansiālais daudzums)

## <a name="default-item-cost"></a>Noklusētās krājuma izmaksas

Izlaistās preces noklusējuma krājumu izmaksas var konfigurēt vienā no diviem veidiem, kā lapā Izlaistās **preces papildinformācija**:

- Izveidojiet standarta izmaksas, **atlasot** **Krājumu cenu grupas** iestatījumos **darbību** rūts cilnē Pārvaldīt izmaksas. Ja izmantojat šo metodi, jāizmanto standarta izmaksu aprēķina versija, un izmaksas ir jāaktivizē.
- Definējiet izlaistās preces krājuma izmaksu noklusējuma cenu, ievadot **vērtību kopsavilkuma** **cilnes Pārvaldīt izmaksas laukā** Cena.

Papildus cenas ievadīšanai vai izveidošanai **lapas** **·** **Izlaistās preces detalizēta informācija cilnē Pārvaldīt izmaksas varat atzīmēt izvēles rūtiņu Izmantot pēdējo izmaksu** cenu. Šādā gadījumā sistēma automātiski atjauninās lauku Cena **,** grāmatojot finanšu atjauninājumu. Piemēram, ja grāmatojat pirkšanas pasūtījuma rēķinu, lauks no šī rēķina tiks iestatīts kā pirkšanas cena.

**Ja** jums ir izmaksu cena aktīvā izmaksu grāmatošanas versijā un jūs ievadāt cenu kopsavilkuma cilnē Pārvaldīt izmaksas, sistēma izmantos cenu no aktīvās izmaksu versijas, **pirms** tā izmanto cenu, kas ir noteikta kopsavilkuma cilnē Pārvaldīt izmaksas.

## <a name="using-the-running-average-cost-price"></a>Faktiskās vidējo izmaksu cenas izmantošana

Tālāk esošajā tabulā ir norādīts, kādos gadījumos sistēmā tiek iegrāmatotas krājumu transakcijas, izmantojot faktisko vidējo izmaksu cenu, un kādos gadījumos tās vietā tiek izmantota izmaksu cena, kas ir definēta krājuma šablona ierakstā.

| Nosacījums | Sistēmā tiek izmantota aprēķinātā faktiskā vidējo izmaksu cena | Sistēma izmanto noklusējuma krājuma izmaksu cenu |
| --- | --- | --- |
| Gan skaitītājs\*, gan saucējs\*\* ir pozitīvs skaitlis. | Jā | Nē |
| Gan skaitītājs\*, gan saucējs\*\* ir negatīvi skaitļi. | Nē | Jā |
| Saucējs ir\*\* 0 (nulle). | Nē | Jā |

\* Skaitītājs = (fiziskā summa + finanšu summa)  
\*\* Saucējs = (fiziskais daudzums + finansiālais daudzums)

> [!NOTE]
> Ja krājumam **nav** atlasīta opcija Iekļaut fizisko vērtību, sistēma izmanto 0 (nulli) gan fiziskajai summai, gan fiziskajam daudzumam. Informāciju par šo opciju skatiet šeit: [Iekļaut fizisko vērtību](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Paaugstinātas cenas noteikšanas nepieļaušana

Retos gadījumos sistēmā tiek noteikta vairāku izdošanu cena, pirms ir pieejams pietiekams ieejas plūsmu daudzums, pēc kura var noteikt cenu. Šāds scenārijs var izraisīt pārāk augstu faktisko vidējo izmaksu cenas aprēķināšanu. Taču ir pieejamas darbības, kuras var veikt, lai nepieļautu paaugstinātas cenas noteikšanu vai lai samazinātu tās ietekme, ja tas tomēr notiek.

**Scenārijs:** Šādas darbības rodas vienumam, kam esat atlasījis opciju **Iekļaut fizisko** vērtību:

1. Finansiāli tiek saņemts 100 vienību daudzums par cenu USD 100,00.
2. Finansiāli tiek izdots 200 vienību daudzums.
3. Fiziski tiek saņemts 101 vienības daudzums par cenu USD 202,00.

Pārbaudot aprēķināto faktisko krājuma vidējo izmaksas cenu, paredzamā izmaksu cena ir USD 1,51. Tā vietā varat atrast aprēķināto vidējo rādītāju USD 102.00, kas ir balstīta uz šādu formulu:

Novērtētā cena = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102

Šī cenu noteikšana notiek, jo, kad 200 krājumi ir finansiāli izsniegti 2. solī, sistēmai ir jānosaka cena 100 no krājumiem pirms tās saņem jebkādas atbilstošas saņemšanas. Šī situācija izraisa negatīvu krājumu. Pēc tam sistēma novērtē vienības cenu USD 1.00, kādu varat gaidīt. Tomēr, saņemot atbilstošo 100 vienību ieejas plūsmas, to vienas vienības cena ir USD 2,00.

> [!NOTE]
> Lai gan izejas plūsmas izveido negatīvus krājumus, krājumi ir pozitīvi, kad tiek aprēķināta izejas plūsmas cena. Tādēļ tiek izmantota faktiskā vidējo izmaksas cena, nevis krājuma galvenajā ierakstā. Tagad sistēmā krājumu korespondējošā vērtība ir USD 100,00. Kaut arī šī kompensācija tika veidota vairāk par 100 gabaliem, kur bija korespondējošā konta USD 1.00, tagad krājumos ir tikai viens gabals. Tāpēc korespondējošo vērtība USD 100,00 tiek piešķirta šai vienai vienībai. Rezultātā novērtēto izmaksu cena tiek aprēķināta pārāk augsta.
>
> Salīdzinājumam ievērojiet, ka darbības 2 un 3 ir atceltas scenārijā, 200 krājumi tiks izsniegti par vienības cenu USD 1.51 un viens gabals paliks par vienības cenu USD 1.51. Tā kā šis paaugstinātās cenas noteikšanas scenārijs var rasties, ja ir iesaistīti negatīvi krājumi, no tās ir grūti izvairīties tālāk minētajos gadījumos.
>
> - Jānovērtē rīcībā esošo vērtību un daudzumu izejas plūsmas cenas.
> - Jāpielāgo izejas un ieejas plūsmas rīcībā esošās vērtības un daudzumi.
> - Biznesa modelis ļauj izsūtīt vai noteikt cenu vairāk vienībām nekā reāli pastāv.
> - Jāapstiprina visas iesniegtās ienākošās plūsmas vērtības un daudzumi.

Ja biznesa modelis pieļauj tālāk aprakstīto procedūru izmantošanu, tās var palīdzēt izvairīties no daudzuma ar negatīvu vērtību, kas izraisa paaugstinātas cenas noteikšanas scenāriju.

- Ja krājumam atlasāt **opciju Iekļaut** fizisko vērtību, notīriet **izvēles** rūtiņu Fiziski negatīvi krājumi lapā **Krājumu modeļu** grupas.
- Ja krājumam opcija **Iekļaut fizisko vērtību,** **netiek** atlasīta, noņemiet izvēles rūtiņas **Negatīvi finansiālie krājumi** atlasi lapā **Krājuma modeļu grupas**.

Papildus ņemiet vērā, ka fizisko krājumu maksimālo korespondējošo vērtību ierobežo fizisko transakciju skaits un fiziskās un finanšu cenas starpība. Ar nosacījumu, ka visas fiziskās transakcijas tiek finansiāli atjauninātas, fiziskā vērtība nevar paaugstināties līdz ārkārtas līmenim. Visbeidzot, ņemiet vērā, ka paaugstināšanās efekts būtiski samazinās, ja uzkrātā korespondējošā vērtība tiek piemērota vairākām nevis tikai vienai rīcībā esošajai vienībai.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Izvairīties no izejas plūsmas nulles izmaksu cenas

Ja krājumu **modeļu grupas lapā** **nav** atlasīta opcija Iekļaut fizisko vērtību, krājumu izejas plūsmai var būt nulles izmaksu cena, ja krājumos nav finansiāli atjauninātas saņemšanas. Lai no tā izvairītos, apsveriet šādas opcijas:

- Izvēlieties opciju **Iekļaut fizisko** vērtību lapā **Krājumu modeļu** grupa. Šī opcija novērsīs nulles izmaksu cenu izdošanā, ja ieejas plūsma ir fiziski atjaunināta. Ja neļausiet negatīvus fiziskos krājumus, izejas plūsmas aprēķinās tekošo vidējo vērtību no fiziski atjauninātajām darbībām.
- Izveidojiet noklusējuma krājuma izmaksu cenu, aktivizējot izmaksu versiju, kam ir standarta izmaksas, **·** **vai ievadiet cenu kopsavilkuma cilnē Pārvaldīt izmaksas lapā Izlaistās** preces informācija. Šī opcija ir **vislabāk** **·**, kad krājumu modeļu grupas lapā nav atlasīta opcija Iekļaut fizisko vērtību, jo sistēmai vienmēr būs jāizmanto regresa cena.
- Atlasiet opciju **Izmantot pēdējo izmaksu cenu** lapas Izlaisto **preču** informācijas kopsavilkuma cilnē **Pārvaldīt** izmaksas. Šī opcija atjaunina lauku **Cena** katru reizi, kad finansiāli atjaunināsiet saņemšanu. Ja atlasīsiet šo opciju, bet neieiesiet noklusējuma cenu vai neaktivizējat izmaksas standarta izmaksu aprēķināšanas versijā, joprojām būs nulles izmaksas izejas plūsmai.

Ja ir izdošanas darbības ar nulles izmaksām, *krājumu* slēgšanas un koriģēšanas process izlabos izmaksu cenu, izveidojot korekciju pēc tam, kad ieejas plūsmas būs finansiāli atjauninātas. Atcerieties, ka finanšu periods šī atjauninājuma gadījumā var atšķirties no finanšu perioda, kad krājumi tika fiziski saņemti vai izsniegti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
