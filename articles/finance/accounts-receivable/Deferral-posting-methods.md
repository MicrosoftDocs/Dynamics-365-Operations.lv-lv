---
title: Atlikto maksājumu grāmatošanas metodes
description: Šajā rakstā ir aprakstītas atšķirības starp atlikto maksājumu grāmatošanas metodēm ieņēmumiem un izdevumu atliktajiem rēķiniem abonementa norēķinos.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017476"
---
# <a name="deferral-posting-methods"></a>Atlikto maksājumu grāmatošanas metodes

Šajā rakstā ir aprakstītas atšķirības starp atlikto maksājumu grāmatošanas metodēm ieņēmumiem un izdevumu atliktajiem rēķiniem abonementa norēķinos.

Ieņēmumu un **izdevumu atlikto maksājumu parametru lapā** atlikto maksājumu grāmatošanas metožu opcijas ir Bilance **un** Peļņa **un zaudējumi**. Piemērs šajā rakstā palīdzēs skaidrot atšķirības starp šīm divām metodēm un iemeslus, kāpēc jūs varētu izmantot vienu metodi vai citu.

Bilances **metode** izmanto tikai divus kontus. Tāpēc ir iesaistīti mazāki iestatījumi. Peļņas **un zaudējumu metodei** ir divi papildu konti - **·** **sākotnējā** atzīšana un atzīšanas korespondējošais konts, ienākumiem, atlaidēm un izmaksām atkarībā no darbības tipa. Šie konti ir iestatīti atlikto maksājumu noklusējuma lapā **(Abonementa** rēķinu ieņēmumu **un izdevumu atlikto maksājumu iestatīšana \>\>).** Lai gan piemērs ir vērsts uz atliktajiem ieņēmumiem, to pašu koncepciju var piemērot atliktajām atlaidēm un atliktajām izmaksām.

## <a name="example"></a>Paraugs

1. pārdošanas rēķinā ir kopsumma $3,000 un tam ir atliktie ieņēmumi. Šī pārdošanas rēķina iegrāmatošanas laikā šīs tabulas rāda sadales.

**Bilances metode**

| Veids | Konts | Debets | Kredīts|
|---|---|---|---|
| Debets | Debitoru parādi | 3,000.00 | |
| Kredīts | Atliktie ieņēmumi | | 3,000.00 |

**Peļņas un zaudējumu metode**

| Veids | Konts | Debets | Kredīts |
|---|---|---|---|
| Debets | Debitoru parādi | 3,000.00 | |
| Debets | Ieņēmumu atzīšanas korespondējošais konts | 3,000.00 | |
| Kredīts | Atliktie ieņēmumi | | 3,000.00 |
| Kredīts | Sākotnējā ieņēmumu atzīšana | | 3,000.00 |

2. pārdošanas rēķinā ir kopsumma $2,000 un tam nav atlikto ieņēmumu.

| Veids | Konts | Summa |
|---|---|---|
| Debets | Debitoru parādi | 3,000.00 |
| Kredīts | Ieņēmumi | 3,000.00 |

**Bilances metodes kopsummas 1. un 2. pārdošanas rēķinā kombinētajām rindām**

| Konts | Debets | Kredīts |
|---|---|---|
| Debitoru parādi | 5,000.00 | |
| Ieņēmumi | | 2,000.00 |
| Atliktie ieņēmumi | | 3,000.00 |

**Ja tiek izmantota** metode Bilance, nav tik viegli skatīt perioda bruto ieņēmumus. Daži ieņēmumi tiek grāmatoti atlikto **maksājumu ieņēmumu kontā**. Atcerieties, ka, tā kā ieņēmumi tiek atpazīti katrā periodā, atlikto ieņēmumu kontā ir vairāki **debeti un kredīti**. Bruto ieņēmumi dotajā periodā tiks jaukti ar ieņēmumu atzīšanas ins/outs.

**Peļņas un zaudējumu metodes kopsummas 1. un 2. pārdošanas rēķinā kombinētajām pārdošanas rēķinām**

| Konts | Debets | Kredīts |
|---|---|---|
| Debitoru parādi | 5,000.00 | |
| Ieņēmumi | | 5,000.00 |
| Ieņēmumu korespondējošais konts | 3,000.00 | |
| Atliktie ieņēmumi | | 3,000.00 |

Visi ieņēmumi tiek ņemti vērā peļņas un zaudējumu **ieņēmumu kontā**. Pēc tam atliktie ieņēmumi tiek pārvietoti no peļņas un zaudējumu pārskata uz bilanci. Bruto ieņēmumus var viegli skatīt, jo viss ir grāmatots **ieņēmumu kontā**. Tomēr daži no bruto ieņēmumiem tiek atlikti. Tāpēc tā tiek pārvietota uz atlikto **maksājumu ieņēmumu kontu** un atpazīta vēlāk.

Peļņas un zaudējumu metodē **var skatīt ieņēmumu kontu un ieņēmumu korespondējošo kontu,** **·** **lai skatītu peļņas un $5,000 bruto ieņēmumus (atlikto maksājumu neto) $2,000.** Lai arī **Peļņas un zaudējumu** metode var atvieglot pārskatu sniegšanu, ir jāiestata vairāk kontu.
