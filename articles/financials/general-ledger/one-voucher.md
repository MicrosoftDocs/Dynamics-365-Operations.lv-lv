---
title: Viens dokuments
description: "Viens dokuments ļauj finanšu žurnālos (virsgrāmatas žurnālā, pamatlīdzekļu žurnālā, kreditoru maksājumu žurnālā u. c. žurnālos) ievadīt vairākas apakšgrāmatas transakcijas saistībā ar vienu dokumentu."
author: kweekley
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f996131830f9bd4efd534143b3fb761c5ccc756
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="one-voucher"></a>Viens dokuments

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
>  Šī funkcionalitāte būs pieejama 2018. gada pavasara laidiena Dynamics 365 for Finance and Operations versijā 8.0.   

<a name="what-is-one-voucher"></a>Kas ir “Viens dokuments”?
======================

Šī funkcionalitāte ļauj finanšu žurnālos (virsgrāmatas žurnālā, pamatlīdzekļu žurnālā, kreditoru maksājumu žurnālā u. c. žurnālos) ievadīt vairākas apakšgrāmatas transakcijas saistībā ar vienu dokumentu. Mēs šīs funkcionalitātes apzīmēšanai izmantojam nosaukumu “Viens dokuments”. Vienu dokumentu var izveidot, izmantojot vienu no tālāk aprakstītajām metodēm.

-   Iestatiet žurnāla nosaukumu (**Virsgrāmata** \> **Žurnāla iestatīšana** \>**Žurnālu nosaukumi**), laukam **Jauns dokuments** atlasot iestatījumu **Tikai 1 dokumenta numurs**. * Tagad visas rindas, ko pievienosit žurnālam, tiks iekļautas tajā pašā dokumentā. Tā kā visas rindas tiek pievienotas vienam dokumentam, dokumentu var ievadīt kā vairāku rindu dokumentu, kā vienas rindas kontu/korespondējošo kontu vai kā kombināciju.

[![Atsevišķas rindas](./media/same-line.png)](./media/same-line.png)
 
> [!IMPORTANT] 
> *  Ņemiet vērā, ka “Viena dokumenta” definīcija NEIETVER žurnālu nosaukumus, kuri ir iestatīti kā **Tikai 1 dokumenta numurs**, un pēc tam lietotājs ievada dokumentu, kurā ietverti tikai virsgrāmatas kontu tipi.  Šajā dokumentā “Viens dokuments” nozīmē, ka pastāv viens dokuments, kas ietver vairāk nekā vienu kreditoru, debitoru, banku, pamatlīdzekli vai projektu. 

-   Ievadiet vairāku rindu dokumentu, kurā nav norādīts korespondējošais konts.

[![Vairāku rindu dokuments](./media/Multi-line.png)](./media/Multi-line.png)

-   Ievadiet dokumentu, kurā kontam un korespondējošajam kontam ir apakšgrāmatas konta tips, piemēram, kreditors/kreditors, debitors/debitors, kreditors/debitors vai banka/banka.

[![Apakšgrāmatas dokuments](./media/subledger.png)](./media/subledger.png)

<a name="issues-with-one-voucher"></a>Funkcionalitātes “Viens dokuments” problēmas
=======================

Funkcionalitāte “Viens dokuments” izraisa problēmas, veicot nosegšanu, aprēķinot nodokļus, saskaņojot apakšgrāmatu ar virsgrāmatu, veidojot finanšu pārskatu un veicot citas darbības. (Piemēram, papildinformāciju par problēmām, kas var rasties, veicot nosegšanu, skatiet rakstā [Viens dokuments ar vairākiem debitoru vai kreditoru ierakstiem](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Pareizai šo procesu un pārskatu darbībai un pārskatu sniegšanai ir nepieciešami transakcijas dati. Kaut arī dažos gadījumos atkarībā no jūsu organizācijas iestatījumiem funkcionalitāte, iespējams, joprojām darbosies pareizi, problēmas bieži rodas, ja vienā dokumentā ir ievadītas vairākas transakcijas.

Piemēram, jūs iegrāmatojat tālāk norādīto vairāku rindu dokumentu.

[![Piemērs](./media/example.png)](./media/example.png)

Pēc tam ģenerējat pārskatu **Izdevumi pēc kreditora** darbvietā **Finanšu ieskati**. Pārskatā izdevumu konta bilances tiek grupētas pie kreditoru grupas un pēc tam pie kreditora. Ģenerējot pārskatu, sistēma nevar noteikt, kuras kreditoru grupas vai kreditori ir radījuši izdevumus 250,00 apmērā. Tā kā trūkst transakcijas datu, sistēma pieņem, ka visus 250,00 ir radījis pirmais dokumentā ievadītais kreditors. Izdevumu summa 250,00, kas ir iekļauta galvenā konta 600120 bilancē, pēc tam tiek parādīta pie attiecīgās kreditoru grupas vai kreditora. Ir ļoti iespējams, ka pirmais dokumentā ievadītais kreditors nav īstais kreditors, un pārskats ir nepareizs.

[![Izdevumi](./media/expenses.png)](./media/expenses.png)

<a name="the-future-of-one-voucher"></a>Funkcionalitātes “Viens dokuments” turpmākais izmantojums
=========================

Ņemot vērā iepriekš minētās problēmas, funkcionalitāte “Viens dokuments” tiks deaktivizēta kā novecojusi. Tomēr šī funkcionalitāte netiks deaktivizēta uzreiz, jo šī funkcionalitāte ir nepieciešama dažu funkcionālo trūkumu novēršanai. Tā vietā mēs izmantosim tālāk norādīto grafiku. 

- **2018. gada pavasara laidiens** — funkcionalitāte tiks izslēgta pēc noklusējuma, izmantojot Virsgrāmatas parametru. Tomēr funkcionalitāti būs iespējams ieslēgt, ja jūsu organizācijā tiek izmantots kāds no tālāk šajā tēmā uzskaitītajiem biznesa scenāriju izņēmumiem.

  -   Ja debitora biznesa scenārijam nav nepieciešama funkcionalitāte “Viens dokuments”, neieslēdziet funkcionalitāti. Mēs nelabosim kļūdas, kas attiecas uz tālāk šajā tēmā norādītajiem gadījumiem, ja šī funkcionalitāte tiek izmantota, kaut arī pastāv cits risinājums.

  -   Pārtrauciet funkcionalitātes “Viens dokuments” izmantošanu integrēšanai risinājumā Microsoft Dynamics 365 Finance and Operations, ja vien šī funkcionalitāte nav nepieciešama kāda funkcionālā trūkuma novēršanai.

- **2018. gada rudens un vēlāki laidieni** — funkcionālie trūkumi būs novērsti. Pēc funkcionālo trūkumu novēršanas, funkcionalitāte “Viens dokuments” tiks neatgriezeniski izslēgta.

- > [!IMPORTANT]
  > Lūdzu, ņemiet vērā, ka opcija **Tikai 1 dokumenta numurs** NAV izņemta no žurnāla nosaukuma iestatījumiem.  Šī opcija joprojām tiek atbalstīta, ja dokuments satur tikai virsgrāmatas kontu tipus.  Klientiem ir jābūt uzmanīgiem, lietojot šo iestatījumu, jo dokumentu nevar grāmatot, ja tie izmanto opciju **Tikai 1 dokumenta numurs**, bet pēc tam ievada vairāk nekā vienu debitoru, kreditoru, banku, pamatlīdzekli vai projektu.  Turklāt klienti joprojām var ievadīt apakšgrāmatas kontu tipu kombināciju, piemēram, maksājumu viena dokumenta ietvaros, kas satur konta tipus Kreditors\Banka.  

<a name="why-use-one-voucher"></a>Kādos gadījumos izmantot funkcionalitāti “Viens dokuments”?
====================

Pamatojoties uz sarunām ar klientiem, tālāk norādītajā sarakstā esam apkopojuši scenārijus, kādos klienti izmanto funkcionalitāti “Viens dokuments”, vai iemeslus, kāpēc viņi šo funkcionalitāti izmanto. Dažas no šīm biznesa darbībām ir izpildāmas, tikai izmantojot funkcionalitāti “Viens dokuments”. Tomēr daudzos scenārijos noteiktas biznesa prasības var izpildīt, izmantojot citus risinājumus.

<a name="scenarios-that-require-one-voucher"></a>Scenāriji, kādos nepieciešams izmantot funkcionalitāti “Viens dokuments”
----------------------------------

Tālāk norādītajos scenārijos noteiktas darbības ir izpildāmas, tikai izmantojot funkcionalitāti “Viens dokuments”. Šie funkcionālie trūkumi tiks novērsti, izmantojot citus līdzekļus, kas būs pieejami 2018. gada rudens un vēlākos laidienos.

-   **Kreditora vai debitora maksājumu grāmatošana bankas kontā kopsavilkuma formā**

    -   Organizācija savā bankā iesniedz sarakstu ar kreditoriem un summām, un banka izmanto šo sarakstu, lai veiktu maksājumus kreditoriem organizācijas vārdā. Banka iegrāmato maksājumu summu bankas kontā kā vienu atvilkumu.

>   Kopsavilkuma izveide par kreditoru maksājumiem tiek atbalstīta tikai funkcionalitātē “Viens dokuments”. Katrs kreditors tiek ievadīts kā atsevišķa rinda, lai saglabātu datus apakšgrāmatā Kreditori, bet visu maksājumu kopsumma tiek ievadīta vienā rindā, kas atbilst bankas kontam. Tādējādi atvilkums bankas apakšgrāmatā tiek parādīts kā viena kopsumma.

-   Organizācija deponē debitoru maksājumus, vai banka deponē debitoru maksājumus organizācijas vārdā, un depozīts bankas kontā tiek rādīts kā vienreizēja izmaksa.

>   Debitoru maksājumu kopsavilkuma izveide parasti tiek atbalstīta, izmantojot depozīta funkcionalitāti. Tomēr, ja jūs maksājuma metodei izmantojat opciju “pagaidu”, šis scenārijs tiek atbalstīts, tikai izmantojot funkcionalitāti “Viens dokuments”. Debitoru maksājumi tiek ievadīti tādā pašā veidā, kā norādīts par kreditoru maksājumu kopsavilkuma izveidi.

-   **Biznesa notikuma transakciju grupēšanas mehānisms**

    -   Organizācijai ir viens biznesa notikums, kas izraisa vairākas transakcijas. Tomēr grāmatvedības nodaļa vēlas skatīt visus uzskaites ierakstus kopā, lai varētu efektīvāk veikt auditu.

>   Ja organizācijai ir nepieciešams skatīt visus biznesa notikuma uzskaites ierakstus kopā, ir jāizmanto funkcionalitāte “Viens dokuments”. 

- **Noteiktās valstīs izmantojami līdzekļi**

  -   Līdzekļa “Vienkāršais administratīvais dokuments (SAD)” darbības nodrošināšanai Polijā pašlaik ir nepieciešams izmantot vienu dokumentu. Jums ir jāturpina izmantot funkcionalitāte “Viens dokuments”, līdz šim līdzeklim būs pieejama grupēšanas opcija. Iespējami arī citi noteiktās valstīs izmantojami līdzekļi, kuriem ir nepieciešams izmantot funkcionalitāti “Viens dokuments”.

- **Debitoru priekšapmaksas maksājumu žurnāls, kurā nodokļi ir norādīti vairākās rindās**

  -   Debitors veic priekšapmaksu par pasūtījumu, un pasūtījuma rindās ir norādīti dažādi nodokļi, kas ir jāreģistrē, veicot priekšapmaksu. Debitora priekšapmaksas maksājums ir viena transakcija, kas simulē pasūtījuma rindas, lai attiecīgo nodokli varētu ierakstīt katrā summas rindā.

Šādā gadījumā vienā dokumentā norādītie debitori atbilst vienam un tam pašam debitoram, jo transakcija simulē debitora pasūtījuma rindas. Priekšapmaksas dati ir jāievada vienā dokumentā, jo nodokļu aprēķināšana ir jāveic debitora veiktā viena maksājuma rindās.

-   **Pamatlīdzekļu uzturēšana: nolietojums ar atpakaļejošu datumu, līdzekļa sadalīšana, nolietojuma aprēķināšana izslēgšanas gadā**

Vairākas transakcijas vienā dokumentā izveido arī tālāk norādītās pamatlīdzekļu transakcijas.
-   Tiek veikta līdzekļa papildu iegāde, un tiek aprēķināts nolietojums ar atpakaļejošu datumu.
-   Tiek veikta līdzekļa sadalīšana.
-   Tiek iespējots parametrs nolietojuma aprēķināšanai izslēgšanas gadā, un pēc tam līdzeklis tiek izslēgts.

<a name="scenarios-that-dont-require-one-voucher"></a>Scenāriji, kādos izmantot funkcionalitāti “Viens dokuments” nav nepieciešams
----------------------------------------

Tālāk norādītos scenārijus var izpildīt, izmantojot citus līdzekļus, tāpēc funkcionalitāte “Viens dokuments” nav jāizmanto.

-   **Debitora maksājumu grāmatošana bankas kontā kopsavilkuma formā**

Organizācija deponē debitoru maksājumus, vai banka deponē debitoru maksājumus organizācijas vārdā, un depozīts bankas kontā tiek rādīts kā vienreizēja izmaksa.

Ja maksājuma metodei netiek izmantota opcija “pagaidu”, debitoru maksājumu kopsavilkuma izveide tiek atbalstīta, izmantojot depozīta funkcionalitāti.

-   **Tīkli**

Tīklā kreditora un debitora bilances tiek salīdzinātas viena ar otru, jo kreditors un debitors ir viena un tā pati puse. Šī pieeja minimizē naudas apmaiņas plūsmu starp organizāciju un debitora/kreditora pusi.

Tīklu var izveidot, ievadot pieaugumu un samazinājumu atsevišķos dokumentos un iegrāmatojot nobīdi norēķinu virsgrāmatas kontā.

-   **Kopsavilkuma grāmatošana virsgrāmatā**

Organizācijas bieži vēlas virsgrāmatā iegrāmatot kopsavilkumu, lai tādējādi samazinātu datu apjomu. Tomēr parasti organizācijām joprojām ir nepieciešams saglabāt transakciju datus. Ja grāmatošana tiek veikta, izveidojot kopsavilkumu vienā dokumentā, transakciju dati netiek norādīti, un tos nevar saglabāt.

   -   Tā kā transakciju datus pašlaik nevar saglabāt, iesakām kopsavilkuma grāmatošanai neizmantot funkcionalitāti “Viens dokuments”.
   -   Pēc atbalsta pārtraukšanas funkcionalitātei “Viens dokuments”, mēs varēsim žurnālos ieviest struktūras Pirmdokuments un Uzskaite. Šīs struktūras nodrošinās transkaciju datu saglabāšanu un kopsavilkuma izveidi virsgrāmatā.

-   **Vairāku neiegrāmatotu maksājumu segšana, izmantojot vienu rēķinu**

Šis scenārijs parasti attiecas uz mazumtirdzniecības organizācijām, kur debitori var izmantot vairākas maksājuma metodes, lai norēķinātos par pirkumiem. Šādā gadījumā organizācijai ir nepieciešams reģistrēt vairākus negrāmatotus maksājumus un segt tos atbilstoši debitora rēķinam.

Microsoft Dynamics 365 for Operations versijā 1611 (2016. gada novembrī) tika pievienots jauns līdzeklis, kas ļauj segt vairākus negrāmatotus maksājumus, izmantojot vienu rēķinu. Vairāki debitoru maksājumi vairs nav jāievada vienā dokumentā.

-   **Bankas izraksta transakciju importēšana**

Bankas bieži veic un saņem maksājumus organizācijas vārdā, un šīs transakcijas tiek reģistrētas programmatūrā Finance and Operations, izmantojot no bankas saņemto failu. Organizācijām bieži ir nepieciešams šādas transakcijas sagrupēt, izmantojot failā norādīto bankas izraksta numuru. Tā kā bankas izrakstā tiek parādīta detalizēta informācija par katru transakciju, bankas apakšgrāmatā nav nepieciešams grāmatot kopsavilkumu.

Transakcijas var tikt sagrupētas, izmantojot citus žurnāla laukus, piemēram, žurnāla pakešuzdevuma numuru vai dokumenta numuru.

-   **Pārsūtīt bilances**

Organizācijai, iespējams, būs nepieciešams pārsūtīt viena kreditora bilanci citam kreditoram, vai nu tāpēc, ka radusies kļūda, vai tāpēc, ka atbildība ir piešķirta citam kreditoram. Šāda veida pārsūtīšana ir iespējama arī starp dažādu veidu kontiem, piemēram, starp debitoriem un banku kontiem.

Bilances pārsūtīšanu no viena konta (kreditora, debitora, bankas konta u. c. kontiem) uz citu kontu var veikt, izmantojot atsevišķus dokumentus, un nobīdi var iegrāmatot norēķinu virsgrāmatas kontā.

-   **Sākuma bilanču ievadīšana**

Organizācijas bieži ievada sākuma bilances apakšgrāmatas kontiem (kreditoriem, debitoriem, pamatlīdzekļiem u. c. kontiem) kā viena dokumenta transakciju. Sākuma bilances katram apakšgrāmatas kontam var ievadīt kā atsevišķus dokumentus, un nobīdi var iegrāmatot norēķinu virsgrāmatas kontā.

-   **Iegrāmatota debitora vai kreditora dokumenta uzskaites ieraksta labošana**

Organizācijai var būt nepieciešams labot debitoru vai kreditoru virsgrāmatas kontā iegrāmatota rēķina uzskaites ierakstu, bet šo rēķinu nevar atsaukt vai labot, izmantojot citu mehānismu.

Ja labojums ir jāveic debitoru vai kreditoru virsgrāmatas kontā, korekcija ir jāveic tieši virsgrāmatas kontā. Korekciju nevar veikt, izmantojot iegrāmatošanu kreditora vai debitora kontā. Izmantojot šo pieeju, korekciju ir iespējams veikt tikai laikā, kamēr sistēma netiek lietota un virsgrāmatas kontā īslaicīgi ir atļauts veikt manuālu ievadi.

-   **Funkcionalitāte ir pieejama sistēmā**

Organizācijas, neizprotot sekas, bieži izmanto funkcionalitāti “Viens dokuments” tikai tāpēc, ka sistēma ļauj to izmantot.

