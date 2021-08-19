---
title: Mazumtirdzniecības transakciju konsekvences pārbaudītājs
description: Šajā tēmā ir aprakstīta transakciju konsekvences pārbaudītāja funkcionalitāte programmā Dynamics 365 Commerce.
author: josaw1
ms.date: 10/07/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8ba0f99743984860119deb96c889f5d62e1728c8772b9e6786d371690b61489
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741736"
---
# <a name="retail-transaction-consistency-checker"></a>Mazumtirdzniecības transakciju konsekvences pārbaudītājs

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīta transakciju konsekvences pārbaudītāja funkcionalitāte programmā Microsoft Dynamics 365 Commerce. Konsekvences pārbaudītājs identificē un izolē nekonsekventas transakcijas, pirms tās ir uzņemtas pārskatu grāmatošanas procesā.

Kad pārskats tiek grāmatots, grāmatošana var būt nesekmīga, jo tirdzniecības transakciju tabulās pastāv nekonsekventi dati. Šādu datu kļūmi var izraisīt neparedzētas problēmas pārdošanas punkta (point of sale — POS) programmā, kā arī tā var rasties tad, ja transakcijas tiek nepareizi importētas no trešās puses POS sistēmām. Tālāk ir uzskaitīti daži no šādas nekonsekvences potenciālās rašanās piemēriem. 

- Transakcijas kopsumma virsraksta tabulā neatbilst transakcijas kopsummai rindās.
- Rindu skaits virsraksta tabulā neatbilst rindu skaitam transakcijas tabulā.
- Nodokļi virsraksta tabulā neatbilst nodokļu summai rindās. 

Kad pārskatu grāmatošanas process uzņem nekonsekventas transakcijas, tiek izveidoti nekonsekventi pārdošanas rēķini un maksājumu žurnāli, līdz ar to viss pārskata grāmatošanas process ir nesekmīgs. Lai atkoptu pārskatus no šāda stāvokļa, ir jāizmanto sarežģīti datu labojumi vairākās transakciju tabulās. Transakciju konsekvences pārbaudītājs neļauj šādu problēmu rašanos.

Nākamajā diagrammā ir parādīts grāmatošanas process ar transakciju konsekvences pārbaudītāju.

![Pārskatu grāmatošanas process ar darījumu konsistences pārbaudītāju.](./media/validchecker.png "Pārskatu grāmatošanas process ar mazumtirdzniecības transakciju konsekvences pārbaudītāju")

Pakešveida apstrādes process **Pārbaudīt veikala transakcijas** pārbauda tirdzniecības transakciju tabulu konsekvenci tālāk norādītajos scenārijos.

- **Debitora konts** — pārbauda, vai attiecīgais debitora konts pastāv galvenā birojā debitoru pamatfaila transakciju tabulās.
- **Rindu skaits** — pārbauda, vai transakciju virsrakstu tabulā norādītais rindu skaits atbilst pārdošanas transakciju tabulu rindu skaitam.
- **Cenā iekļauts nodoklis** — pārbauda, vai parametrs **Cenā iekļauts nodoklis** ir konsekvents transakciju rindās un cena pārdošanas rindā atbilst konfigurācijai par cenu, kurā iekļauts nodoklis, un nodokļu atvieglojumiem.
- **Maksājuma summa** — pārbauda, vai maksājumu ieraksti atbilst maksājuma summai galvenē, ņemot vērā arī noapaļošanas konfigurāciju Virsgrāmatā.
- **Bruto summa** — pārbauda, vai bruto summa galvenē ir rindu neto summu un nodokļu summa, ņemot vērā arī noapaļošanas konfigurāciju Virsgrāmatā.
- **Neto summa** — pārbauda, vai neto summa galvenē ir rindu neto summa, ņemot vērā arī noapaļošanas konfigurāciju Virsgrāmatā.
- **Nepilnīgs maksājums/pārmaksa** — pārbauda, vai galvenē iekļautās bruto summas un maksājuma summas starpība nepārsniedz maksimālo konfigurēto nepilnīga maksājuma/pārmaksas summu, ņemot vērā arī noapaļošanas konfigurāciju Virsgrāmatā.
- **Atlaides summa** — pārbauda, vai atlaižu tabulās un mazumtirdzniecības transakciju rindu tabulās norādītās atlaides summas ir konsekventas un vai virsrakstā iekļautā atlaides summa un rindās iekļautās atlaižu summas ir konsekventas, ņemot vērā arī noapaļošanas konfigurāciju Virsgrāmatā.
- **Rindas atlaide** — pārbauda, vai transakcijas rindas atlaides summa ir visu atlaižu tabulas rindu summa, kas atbilst transakcijas rindai.
- **Dāvanu kartes krājums** — risinājumā Commerce netiek atbalstīta dāvanu karšu krājumu atgriešana. Tomēr dāvanu kartes atlikums var tikt izmaksāts skaidrā naudā. Visi tie dāvanu kartes krājumi, kas tiek apstrādāti kā atgriešanas rinda, nevis skaidras naudas izņemšanas rinda, netiek iekļauti grāmatošanas procesā. Palaižot dāvanu karšu krājumu pārbaudes procesu, tiek nodrošināts, ka transakciju tabulās tiek atgriezti tikai tie dāvanu karšu rindas krājumi, kuri ir dāvanu karšu skaidras naudas izmaksas rindas.
- **Negatīva cena** — pārbauda, vai nav nevienas transakciju rindas ar negatīvu cenu.
- **Krājums un variants** — pārbauda, vai transakcijas rindas krājumi un varianti pastāv krājumu un variantu pamatfailā.
- **Nodokļu summa** — pārbauda nodokļu ierakstu atbilstību rindās norādītajām nodokļu summām.
- **Sērijas numurs** — pārbauda, vai sērijas numurs atrodas transakciju rindās krājumiem, kas tiek kontrolēti pēc sērijas numura.
- **Zīme** — pārbauda, vai daudzuma un neto summas zīme ir vienāda visās transakciju rindās.
- **Darbadiena** — pārbauda, vai finanšu periodi visām transakciju darbadienām ir atvērti.
- **Maksas** — pārbauda, vai maksas summa galvenē un rindā atbilst cenai, tostarp arī nodokļu un nodokļu atvieglojumu konfigurācijai.

## <a name="set-up-the-consistency-checker"></a>Konsekvences pārbaudītāja iestatīšana

Sadaļā **Retail un Commerce \> Retail un Commerce IT \> POS grāmatošana** konfigurējiet pakešveida apstrādes procesu “Validēt veikala transakcijas” tā, lai tas tiktu palaists regulāri. Pakešuzdevumu var plānot atkarībā no veikala organizācijas hierarhijas, līdzīgi kā tiek iestatīti procesi “Aprēķināt pārskatu partijā” un “Grāmatot pārskatu partijā”. Iesakām šo pakešuzdevumu konfigurēt tā, lai dienas laikā tas tiktu izpildīts vairākas reizes, un to ieplānot tā, lai tas tiktu izpildīts katras P darba izpildes beigās.

## <a name="results-of-validation-process"></a>Validēšanas procesa rezultāti

Šī pakešuzdevuma validēšanas pārbaudes rezultāti tiek atzīmēti atbilstošajā transakcijā. Lauks **Validācijas statuss** transakcijas ierakstā ir iestatīts uz **Sekmīgs** vai **Kļūda**, un pēdējās validēšanas izpildes datums ir redzams laukā **Pēdējās validēšanas laiks**.

Lai redzētu aprakstošāku kļūdas tekstu saistībā ar validēšanas kļūmi, atlasiet attiecīgo veikala transakcijas ierakstu un noklikšķiniet uz pogas **Validācijas kļūdas**.

Uz pārskatiem netiek nogādātas transakcijas, kam validācijas pārbaude ir nesekmīga, un transakcijas, kas vēl nav validētas. Procesa “Aprēķināt pārskatu” laikā lietotājiem tiek ziņots, vai pastāv transakcijas, kas varēja tikt ietvertas pārskatā, bet netika tajā ietvertas.

Ja tiek atrasta kāda validācijas kļūda, vienīgais veids, kā šo kļūdu novērst, ir sazināties ar Microsoft atbalsta dienestu. Turpmākajos laidienos tiks pievienota iespēja lietotājiem izlabot nesekmīgos ierakstus, izmantojot lietotāja interfeisu. Kļūs pieejamas arī reģistrēšanas un auditēšanas iespējas, lai izsekotu modifikāciju vēsturi.

> [!NOTE]
> Kādā no turpmākajiem laidieniem tiks pievienotas papildu validēšanas kārtulas, lai atbalstītu vairāk scenāriju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]