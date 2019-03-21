---
title: Piedāvājumu pārvaldības iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt piedāvājumus programmā Talent.
author: josaw
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43cf13d96e345747e06541267d820e17de7c1763
ms.sourcegitcommit: ea17d2e35c24a141c20ab429897eebf9fa186f61
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/26/2019
ms.locfileid: "768886"
---
# <a name="set-up-offer-management"></a>Piedāvājumu pārvaldības iestatīšana 

[!include [banner](includes/banner.md)]

Kad kandidāts tiek pārvietots uz piedāvājuma posmu programmā Dynamics 365 for Talent: Attract, ir jānodrošina, ka var ātri izveidot kandidātam paredzētos piedāvājumus, pēc nepieciešamības tos apstiprināt un nosūtīt attiecīgajam kandidātam. Tā kā lielākā daļa piedāvājumu ir standarta piedāvājumi, tos var izveidot no atkārtoti izmantojamām veidnēm. Programmā Attract visi piedāvājumi tiek apkopoti piedāvājumu paketē, kas ir kolekcija no viena vai vairākiem piedāvājumu dokumentiem. 

Šajā tēmā ir uzskaitītas visas darbības, kas Attract administratoram būtu jāizpilda, lai kā daļu no piedāvājumu pārvaldības iespējām programmā Attract iesaistītu dažādas piedāvājumu pakotņu veidnes. Lietotājiem, kuriem nav administratora lomas, nav piekļuves šīm iespējām.

>[!NOTE]
> Piedāvājumu pārvaldības iespējas ir pieejamas kā daļa no visaptverošās darbā pieņemšanas pievienojumprogrammas.

## <a name="offer-data"></a>Piedāvājuma dati 

Piedāvājuma dati ir vismazākā vienība piedāvājumu pakotnes veidnē. Tipisks piedāvājums sastāv no standarta teksta un vērtību kopas. Vērtību kopas ir vienīgās daļas, kas dažādos piedāvājumos var mainīties. Piedāvājuma izveidošanas laikā vissvarīgākais aspekts, uz ko piedāvājuma izveidotājs var koncentrēties, ir saraksts ar piedāvājuma datu vietturiem, kas atrodas piedāvājumu pakotnes veidnē. Lai iestatītu piedāvājuma datus, izpildiet tālāk aprakstītos norādījumus.

1.  Dodieties uz **Piedāvājumu pārvaldība**.

1.  Kreisajā navigācijas rūtī izvērsiet sadaļu **Bibliotēka** un pēc tam dodieties uz **Piedāvājuma dati**.

    >[!NOTE]
    > Lapā **Piedāvājuma dati** ir sadaļas **Kandidāta informācija** un **Darba informācija**. Attract nodrošina dažus piedāvājuma datu vietturus jau standarta komplektācijā.
    
    > Lapā ir sadaļas, kas ir paredzētas dažādu piedāvājuma datu vietturu sakārtošanai loģiskās grupās. Šīs sadaļas var noderēt saistībā ar piedāvājuma datu uzturēšanu un datu aizpildīšanu piedāvājuma izveidošanas procesa laikā.

1.  Lai izveidotu jaunu piedāvājuma datu sadaļu, noklikšķiniet uz **Pievienot sadaļu** un ievadiet unikālu nosaukumu šai sadaļai.

1.  Lai jebkurai sadaļai pievienotu piedāvājuma datu vietturus, noklikšķiniet uz **Pievienot piedāvājuma datus** un ievadiet unikālu nosaukumu šim vietturim.

1.  Lai rediģētu jebkuras sadaļas nosaukumu, virziet peles kursoru virs sadaļas nosaukuma un atjauniniet nosaukumu.

1.  Lai rediģētu jebkuru esošu piedāvājuma datu viettura nosaukumu, vispirms pārliecinieties, vai šis vietturis vēl neveido daļu no kādas veidnes. Pēc tam virziet peles kursoru virs piedāvājuma datu viettura nosaukuma un pēc nepieciešamības atjauniniet šo nosaukumu.

1. Lai dzēstu esošu piedāvājuma datu vietturi, vispirms pārliecinieties, vai šis vietturis neveido daļu no kādas citas veidnes. Pēc tam virziet peles kursoru virs viettura un, kad kļūst redzama atkritnes ikona, noklikšķiniet uz atkritnes, lai dzēstu šo piedāvājuma datu vietturi.
    >[!NOTE]
    > Varat redzēt, cik veidnēs ietilpst kāds piedāvājuma datu vietturis — šis skaits tiek rādīts blakus katra piedāvājuma datiem. 

1. Lai dzēstu jebkuru sadaļu, virziet peles kursoru virs tās nosaukuma. Ja neviens no sadaļā esošajiem piedāvājuma datu vietturiem nav redzams nevienā veidnē, varat noklikšķināt uz atkritnes ikonas, lai to dzēstu. 
    >[!NOTE]
    > Dzēšot sadaļu, tiek dzēsti arī visi piedāvājuma datu vietturi šajā sadaļā.

Pēc piedāvājuma datu vietturu iestatīšanas tos varat izmantot jebkurā dokumenta veidnē. Piedāvājuma datu vietturi nav ierobežoti tikai noteiktā veidnē — to pašu kopu var izmantot visās veidnēs.

## <a name="offer-data-rules"></a>Piedāvājuma datu kārtulas

Vairumam organizāciju ir kārtulas, kas nosaka piedāvājumu izveidošanu. Piemēram, organizācija var vēlēties pieprasīt, lai maksimālās gada algas piedāvājums noteiktai atrašanās vietas un darba stāža līmeņa kombinācijai būtu noteiktā diapazonā vai lai būtu iespējamas tikai dažas konkrētas vērtības piedāvājuma līmenim attiecībā uz nesen nolīgtu darbinieku. Pašlaik Attract atbalsta visas šādas datu kārtulas, izmantojot CSV failu.

Lai sagatavotu datu kārtulu CSV failu, izpildiet tālāk aprakstītos norādījumus.

1.  Nosakiet piedāvājuma datu vietturi kārtulu kopai. Piemēram, **Gada alga**.

1.  Identificējiet pakārtoto piedāvājuma datu vietturu vērtības. Piemēram, **Darba atrašanās vieta** un **Līmenis**.

1.  Norādiet 1. un 2. kolonnu kā **Darba atrašanās vieta** un **Līmenis**.

1.  Lai augšupielādētu diapazona vērtību, nosaukumu **Gada alga** piešķiriet gan 3., gan 4. kolonnai. Lai augšupielādētu konkrētu vērtību, nevis diapazonu, nosaukumu **Gada alga** piešķiriet tikai 3. kolonnai.

1.  Aizpildiet Microsoft Excel failu, pamatojoties uz nepieciešamajām lomām.

1.  Pārliecinieties, vai katrā rindā ir unikāla kombinācija no visām vērtībām kopā.

1.  Saglabājiet failu kā CSV formāta failu.

Lai augšupielādētu piedāvājuma datu kārtulu failu, izpildiet tālāk aprakstītos norādījumus.

1.  Dodieties uz **Piedāvājumu pārvaldība**.

1.  Kreisajā navigācijas panelī izvērsiet sadaļu **Bibliotēka** un pēc tam dodieties uz **Piedāvājuma dati kārtulas**.

1.  Noklikšķiniet uz **Jauna datu kopa**, lai parādītu dialoglodziņu **Augšupielādēt**.

1.  Norādiet unikālu nosaukumu šai kārtulu kopai un pēc tam augšupielādējiet saglabāto CSV failu.

1.  Noklikšķiniet uz **Pievienot**.
    Kārtulu kopa tiks apstrādāta fonā, un pēc apstrādes pabeigšanas jums tiks paziņots programmā un pa e-pastu.

    Jums tiks paziņots, ja augšupielādes apstrādāšanas laikā būs radušās kļūdas. Pēc tam varat lejupielādējiet kļūdu žurnālfailu, izlabot failu un augšupielādēt to vēlreiz.

1.  Izmantojiet daudzpunktes pogas (**...**) opciju, ja vēlaties lejupielādēt kārtulu kopu un atjaunināt šo vērtību kopu. Pēc atjaunināšanas varat šo failu augšupielādēt vēlreiz.

1.  Esošu kārtulu kopas augšupielādi varat dzēst, ja definētais vietturis netiek izmantots nevienā citā dokumenta veidnē.

>[!NOTE]
> - Katram vietturim var būt tikai viena unikāla kolonnu kopa, no kuras tas ir atkarīgs. Piemēram, ja vietturis **Gada alga** ir atkarīgs no vērtības kolonnā **Darba atrašanās vieta** un kolonnā **Līmenis**, jūs nevarat augšupielādēt citu kārtulu kopu, kur vietturis **Gada alga** ir atkarīgs no citas kolonnu kopas.

> - Lapas **Piedāvājuma datu kārtulas** cilnē **Paraugi** varat lejupielādēt piedāvājuma datu kārtulu kopu paraugus.

> - Ja piedāvājuma izveidotājs pārraksta piedāvājuma datu kārtulu ieteiktās vērtības, šis piedāvājums tiek atzīmēts ar karodziņu kā nestandarta un tiek atļauta piedāvājuma apstiprināšanas darbplūsma.

## <a name="document-templates"></a>Dokumentu veidnes

Piedāvājuma dokumenta veidne administratoriem var noderēt piedāvājumu vēstuļu izveidošanai. Piedāvājuma dokumenta veidne sastāv no teksta, kas būs daļa no piedāvājuma, un no definētajiem piedāvājuma datu vietturiem. 

Lai izveidotu piedāvājuma dokumenta veidni, izpildiet tālāk aprakstītos norādījumus.

1.  Dodieties uz **Piedāvājumu pārvaldība**.

1.  Kreisajā navigācijas rūtī izvērsiet sadaļu **Bibliotēka** un dodieties uz **Veidnes**.

    Lapā **Veidnes** tiek rādīts saraksts ar jau definētajām dokumentu veidnēm.

1.  Lai izveidotu jaunu dokumenta veidni, noklikšķiniet uz **Jauna veidne**.

1.  Ievadiet unikālu nosaukumu šai veidnei un noklikšķiniet uz **Izveidot**.

1.  Izmantojiet bagātinātā teksta redaktoru, lai ievietotu vai rediģētu piedāvājuma dokumenta saturu. Varat ievietot tabulas, attēlus un hipersaites, izmantojot teksta redaktora augšpusē pieejamās opcijas.

1.  Piedāvājuma veidnes dokumentā varat ievietot piedāvājuma datu vietturus, izmantojot tālāk aprakstītās metodes.

    - Velkot un nometot no labās rūts.

    - Ievietojot piedāvājuma datu viettura atsauces tagu tieši nepieciešamajā pozīcijā. Ierakstiet **\#** un pēc tam sāciet rakstīt piedāvājuma datu viettura nosaukumu. Tiks parādīts nolaižamais saraksts ar opcijām. Noklikšķiniet vai nospiediet taustiņu **Enter**, lai ievietotu piedāvājuma datu vietturi.

    >[!NOTE]
    > - Lai vietturi saistītu ar piedāvājuma dokumenta veidni, neizpaužot tā vērtību kandidātam, virziet peles kursoru virs piedāvājuma datu viettura un noklikšķiniet uz ikonas **Piespraust**. Šādi vietturis tiks pārbīdīts uz piedāvājuma dokumenta veidnes sadaļu **Piespraustie piedāvājuma dati**. Lai atspraustu, izpildiet tās pašas darbības, bet piedāvājuma datu vietturu sarakstā noklikšķiniet uz **Atspraust**.

    > - Lai skatītu sarakstu ar aktīvajiem piedāvājuma datu vietturiem, labajā rūtī pārslēdziet uz cilni **Aktīvs**.

    > - Ja ievietojat vietturi, kas ir atvasināts no kādas piedāvājuma datu kārtulu kopas, varat redzēt šī piedāvājuma datu viettura atkarību no citām vērtībām.

    > - Ja vēlaties, saturu no .docx faila varat **Importēt** savā lokālajā mašīnā un pēc nepieciešamības to rediģēt. Tādējādi jums redaktorā nav jāieraksta viss saturs.

1. Lai priekšskatītu piedāvājuma dokumentu, izmantojiet opciju **Priekšskatīt** lapas augšpusē.

1. Lai kontrolētu, vai piedāvājuma veidotājs var rediģēt piedāvājuma dokumenta saturu, izmantojiet opciju **Pārvaldīt atļauju** lapas augšdaļā. Ja piedāvājuma izveidotājam vēlaties ļaut tikai ievietot vietturu vērtības, nevis rediģēt tekstu, atļaujas vērtība ir jāiestata uz **Nē**.

1. Noklikšķiniet uz **Saglabāt**, lai saglabātu savu progresu. Veidne tiks saglabāta melnraksta stāvoklī.

1. Lai finalizētu un atzīmētu dokumentu kā publicētu, noklikšķiniet uz **Pabeigt**.

1. Varat redzēt, kuras dokumentu veidnes pašlaik ir aktīvas, kuras atrodas melnraksta režīmā, un kuras ir arhivētas un vairs netiek izmantotas dokumentu veidņu bibliotēkas izvietošanas funkcionalitātē.

>[!NOTE]
> Varat dzēst jebkuru piedāvājuma dokumenta veidni, kas neveido daļu no esošas piedāvājuma pakotnes veidnes.


## <a name="offer-package-templates"></a>Piedāvājuma pakotņu veidnes

Piedāvājuma pakotnes ir piedāvājuma artefakti, kas tiek koplietoti ar kandidātu un sastāv no vienas piedāvājuma veidnes vai vairāku piedāvājuma veidņu kombinācijas. Lai izveidotu piedāvājuma pakotni, izpildiet tālāk aprakstītos norādījumus.

1.  Dodieties uz **Piedāvājumu pārvaldība**.

1.  No kreisās navigācijas rūts dodieties uz **Pakotnes**.

    Tiek parādīts saraksts ar aktīvajām pakotnes veidnēm, kas piedāvājumu veidotājiem ir pieejamas lietošanai.

1.  Lai izveidotu jaunu piedāvājuma pakotni, noklikšķiniet uz **Jauna pakotne**.

1.  Ievadiet unikālu nosaukumu un noklikšķiniet uz **Izveidot**.

1.  Noklikšķiniet uz **Pievienot veidni**.

    >[!NOTE]
    > - Varat izvēlēties izveidot jaunu veidni vai izvēlēties kādu no esošajām.

    > - Ja izvēlaties pievienot esošu veidni, jums ir jāpārliecinās, vai piedāvājuma dokumenta veidne bija saglabāta, finalizēta un atzīmēta kā aktīva.
    
    > - Varat izvēlēties jebkādu skaitu dokumenta veidņu. 
    
1.  Noklikšķiniet uz **Gatavs**, lai atgrieztos sadaļā **Pakotņu pārvaldība**.

    Varat konfigurēt dokumentu sēriju un varat arī atzīmēt, vai konkrētais piedāvājuma dokuments ir nepieciešams piedāvājuma izveidošanas laikā. Piedāvājumu veidotājam būs opcija dzēst dokumentus, kas ir atzīmēti kā **Nav nepieciešams**.

1. Lai saglabātu piedāvājuma pakotnes veidni tā, ka to var izmantot visi piedāvājumu veidotāji, noklikšķiniet uz **Saglabāt un publicēt**.

   Lai skatītu melnraksta piedāvājuma pakotņu veidnes, dodieties uz cilni **Melnraksti**. Ja piedāvājuma pakotnes veidnē tiek veiktas kādas izmaiņas, tā ir jāsaglabā un jāpublicē atkārtoti.

## <a name="configure-an-offer-process"></a>Piedāvājuma procesa konfigurēšana

Piedāvājuma veidošanas procesā ir vairākas daļas, kuras var konfigurēt Attract administrators.

- **Piedāvājumu apstiprinājumi** — izvēlieties, vai piedāvājumi ir jāapstiprina, pirms tie tiek nosūtīti kandidātam. Kā administrators jūs varat arī izlemt, vai visiem piedāvājumu apstiprinājumiem ir jānotiek secīgā vai paralēlā apstiprināšanas darbplūsmā. Varat arī norādīt, vai piedāvājumu apstiprinātājiem kopā ar savu piedāvājuma apstiprinājumu ir jāpievieno arī komentārs. Piedāvājumu apstiprinājumi ir obligāti visiem nestandarta piedāvājumiem.

- **Kandidāta piedāvājuma pieredze** — kā administrators varat izvēlēties iestatīt, vai visiem piedāvājumiem ir beigu datums un — ja tāds ir — kādai ir jābūt beigu datuma noklusējuma nobīdei. Varat arī konfigurēt to, vai kandidāti var noraidīt kādu piedāvājumu.

- **Elektroniskie paraksti** — kā administrators varat arī izvēlēties metodi, kuru kandidātiem izmantot, lai parakstītu piedāvājumus.
    - Adobe Sign — visas piedāvājumu pakotnes tiks nosūtītas un parakstītas, izmantojot Adobe Sign. Katram piedāvājumu izveidotājam, kurš publicē piedāvājumu, ir nepieciešams programmai Attract piesaistīts Adobe Sign konts. Lai iegūtu Adobe Sign licenci bezmaksas izmēģinājumversiju, noklikšķiniet uz šīs [saites](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).

    - DocuSign — visas piedāvājumu pakotnes tiks nosūtītas un parakstītas, izmantojot DocuSign. Katram piedāvājumu izveidotājam, kurš publicē piedāvājumu, ir nepieciešams programmai Attract piesaistīts DocuSign konts. 
    
    - ESign — šī ir standarta komplektācijā iekļautā noklusējuma opcija, ar kuru lietotājs var parakstīt piedāvājumu, ievadot savu vārdu un iniciāļus.


Plašāku informāciju par piedāvājuma izveidošanas procesu skatiet šeit: [Piedāvājumu izveide, apstiprināšana un parakstīšana](./creating-offers.md).
