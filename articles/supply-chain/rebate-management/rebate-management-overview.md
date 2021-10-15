---
title: Atlaižu pārvaldības moduļa pārskats
description: Šajā tēmā ir sniegts pārskats par Atlaižu pārvaldības moduli Microsoft Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b6b986128961a77ba641cf4642c99578484b28e8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573517"
---
# <a name="rebate-management-module-overview"></a>Atlaižu pārvaldības moduļa pārskats

[!include [banner](../includes/banner.md)]

Jūs varat izmantot **Atlaižu pārvaldības** moduli, lai izveidotu līgumus, darījumus vai līgumus starp jūsu uzņēmumu un tā debitoriem vai kreditoriem, tādējādi varat aprēķināt atlaides, atvilkumus un atlaides. Atlaižu pārvaldība izseko un uztur atlaižu un ieturējumu darījumus centrālajā vietā, kur lietotāji var efektīvi izveidot, pārskatīt un apstrādāt tos.

Atlaižu pārvaldība atbalsta *atlaižu* izveidošanu, uzturēšanu un apstrādi. Atlaide ir pārdevēja vai pircēja atpakaļatdošanas daļa no pirkuma cenas. Atlaides parasti pamatotas uz noteikta daudzuma vai preču vērtības iegādi konkrētā periodā. Atšķirībā no atlaidēm atlaides tiek veiktas pēc tam, kad pirkšanas summa ir pilnībā iekļauta rēķinā.

Atlaižu pārvaldība atbalsta arī *ieturējumus*. Ieturējumi ir kompensācija, apsvērumi vai maksa, kas tiek maksāta vai nu par licenci, vai privilēģija izmantot intelektuālo īpašumu, piemēram, zīmolu, autortiesības vai patentu, vai privilēģiju izmantot dabas resursus nolūkiem, piemēram, nolūkiem, piemēram, nolūkiem, apmaksai vai iegūšanai. Ieturējumus parasti aprēķina kā ieņēmumu procentus vai peļņu no faktiskās izmantošanas. Jo vairāk tiek izmantots intelektuālais īpašums vai dabas resursi, jo lielāks ir realizētais ieturējums.

Turklāt atlaižu pārvaldība atbalsta debitoru *patentmaksas*. Patentmaksas ir maksājumi, ko viena puse piešķir licences vai franšīzes tiesības izmantot pamatlīdzekli.

Atlaižu pārvaldība ļauj definēt grāmatošanas metodes uzkrājumiem, atlaidēm un norakstīšanām. Turklāt grāmatojumus var definēt noteiktam debitoram vai kreditoram. Šādā veidā darījumus, kas neattiecas uz visiem debitoru vai kreditoru scenārijiem, var izsekot, izmantojot grāmatojumus.

Atlaižu darījumi tiek ģenerēti automātiski, pamatojoties uz aprēķina metodi, kas ir atlasīta un plānota pakešuzdevumos. Papildus varat iestatīt darbplūsmas, lai pārvaldītu, pārskatītu un apstiprinātu līgumus.

## <a name="basis-calculation"></a>Pamata aprēķins

Debitora atlaides, debitora patentmaksas un kreditora atlaides var izmantot dažādas bāzes atkarībā no uzņēmuma prasībām:

- Debitora atlaides var balstītās uz pārdošanas pasūtījumiem, piegādes pavadzīmēm vai rēķiniem.
- Debitora patentmaksas var balstītās uz pārdošanas pasūtījumiem, piegādes pavadzīmēm vai apmaksātajiem rēķiniem.
- Kreditora atlaides var balstītās uz pirkšanas pasūtījumiem vai pārdošanas pasūtījumiem. Tos var aprēķināt, balstoties uz precēm, kas iegādātas no atlaides kreditora un pārdotas debitoriem caur pārdošanas rēķiniem.

## <a name="flexible-calculations"></a>Elastīgi aprēķini

Atlaides aprēķina periodi ir pieejami gan debitoru darījumiem, gan kreditora darījumiem. Aprēķina periods nosaka darījuma garumu, aprēķina biežumu un aprēķina periodu. Atlaides var uzkrāt, pamatojoties uz pārdošanas pasūtījuma daudzumiem vai kvalificēto produktu summām atlaides periodā.

Katram līguma aprēķinam var tikt iestatīts jebkurš no šiem periodiem:

- Rēķins
- diena;
- Nedēļa
- mēnesis;
- Ceturksnis
- Gads
- Pielāgots periods
- Jebkurš jebkura iepriekš uzskaitītā perioda dalāmais

Aprēķinu var piemērot atsevišķiem debitoriem un precēm, debitoru un preču grupām vai visiem debitoriem un precēm. Atlaidēm, kurām ir vairākas detaļu rindas, var būt atšķirīgi kvalifikācijas datumu diapazoni. Uzkrājumu un prasības periodi var atšķirties. Piemēram, uzkrājumi var tikt apstrādāti katru dienu, turpretī prasības tiek apstrādātas reizi mēnesī.

Atlaides var konfigurēt, pamatojoties uz daudziem dažādiem parametriem. Piemēram, tos var konfigurēt kā procentus, likmi vai fiksētu summu. Pastāv četras galvenās aprēķina metodes:

- Pakāpenisks
- Kumulatīvs
- Secīgs
- Kopsumma

Atlaižu aprēķina rezultātus var samazināt arī ar citām atlaidēm, atkarībā no tā, vai atlaide ir iestatīta aprēķinam, pamatojoties uz neto summu.

Kreditora pusē atlaides,kuru pamatā ir pārdošanas pasūtījumi, var aprēķināt cenu, pamatojoties uz "pirmais ārā" (first in, first out – FIFO) noteikumu, jaunāko pirkšanas cenu, vidējo pirkšanas cenu vai pārdošanas cenu.

## <a name="rebate-target-transactions"></a>Atlaides mērķa darījumi

Rezultāts, ko ģenerē atlaides darījums vai līgums, var būt finanšu darījums vai krājumi.

Finanšu izvade tiek noteikta pēc maksājuma tipa, kas piešķirts līgumam no grāmatošanas metodes. Šīs izvades var ietvert debitoru ieturējumu žurnālus, brīvā teksta rēķinus un kreditora rēķinus. Auditēšanas nolūkos finanšu atlaides mērķa darījumi ietver atsauci uz sākotnējās atlaides līgumu.

Krājuma izvade izveido bezmaksas krājumu pārdošanas pasūtījumu debitora atlaidēm un pirkšanas pasūtījumu kreditora atlaidēm. Krājuma atlaides mērķa darījumi ietver opcijas, lai noteiktu, kura atlaides atsauce ir jāievada brīva krājuma pārdošanas pasūtījumā vai pirkšanas pasūtījumā.

## <a name="accurate-rebate-calculations"></a>Precīzi atlaižu aprēķini

Saistīto darījumu kombinācija, aprēķinu biežums, aprēķina pamats un atlasītā aprēķinu metode nosaka atlaižu aprēķinu precizitāti un precizitāti. Atlaižu nosacījumus var izmantot, lai uzkrātu grāmatotās un pieprasītās vērtības.

Uzkrājumus var pārvaldīt katru dienu, reizi nedēļā, reizi mēnesī vai atbilstoši pielāgotajam periodam. Tomēr funkcionalitāte var piešķirt vai apmaksāt atlaidi vai saņemt tās maksājumu jebkurā definētā frekvencē, kas ir vienāda ar rezervju frekvenci vai lielāka par to. Norakstīšanas frekvence ir tāda pati kā atlaidei. Lietotāji var viegli pielāgot plāna vai maksājumu summas jebkurā laikā izmaksas laikā.

Lietotājiem vairs nav jārīkojas ar darījumiem vai uzkrājumiem divos soļos. Uzkrājumi un norakstīšanas tiek grāmatoti tieši Virsgrāmatā. Turklāt kredīta notas var izveidot automātiski. Tāpēc ir pilnīga integrācija ar kreditoriem un debitoriem. Apstrādes laikā aprēķini var ņemt vērā segšanas atlaides, apmaksātos rēķinus, tirdzniecības atlaides un esošās kredīta notas, lai nodrošinātu, ka summas un vērtības ir precīzi aprēķinātas.

Kad atlaides tiek aprēķinātas, process izveido transakcijas, ko var pārskatīt pirms grāmatošanas. Atsevišķs process grāmato atlaides pārvaldības darījumus. Pēc tam var izveidot žurnālu, kredīta notu vai debeta darījumu, grāmatojot piedāvātos darījumus. Pārskatu pārskatus un darbību sarakstus var iegūt, lai nodrošinātu atbilstību, efektivitāti un pārskatāmību.

## <a name="guaranteed-royalty-payments"></a>Nodrošinātie patentmaksu maksājumi

Atlaižu pārvaldībā automātiskā maksājumu ģenerēšana ļauj ātri un viegli apstrādāt patentmaksas, pat ja tiek lietots nodrošinātais minimums.

## <a name="maximizing-spend-versus-rebates"></a>Palielināt tēriņus pret atlaidēm

Kreditorus un preces var grupēt pēc teritorijas, un atkarībā no darbības valsts vai reģiona var tikt nodrošināti dažādi piedāvājumi. Kad lietotāji izvēlas preces, viņi var definēt iekļautās preces un krājumus, kas tiks izmantoti atlaides segšanai.
