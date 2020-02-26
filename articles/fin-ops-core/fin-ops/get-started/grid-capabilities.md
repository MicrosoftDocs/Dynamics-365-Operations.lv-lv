---
title: Režģa iespējas
description: Šajā tēmā ir aprakstīti vairāki ietekmīgi režģa kontroles līdzekļi. Lai piekļūtu šīm iespējām, ir jābūt iespējotam jaunajam režģa līdzeklim.
author: jasongre
manager: AnnBe
ms.date: 01/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b49d7823f48bcc9cdbb56b87d5fa72d46ddfa15c
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019891"
---
# <a name="grid-capabilites"></a>Režģa iespējas

[!include [banner](../includes/banner.md)]

Jaunā režģa kontrole piedāvā daudzas noderīgas un jaudīgas iespējas, ko var izmantot, lai uzlabotu lietotāju produktivitāti, izveidotu vairāk interesantu jūsu datu skatu un iegūtu izsmeļošu ieskatu datos. Šajā rakstā ir apskatītas tālāk norādītās iespējas 

-  Aprēķina kopsummu
-  Datu grupēšana
-  Rakstīšana pirms sistēmas
-  Matemātisko izteiksmju novērtēšana 

## <a name="calculating-totals"></a>Aprēķina kopsummu
Programmatūrā Finance and Operations lietotājiem ir iespēja redzēt kopsummas režģos ciparu kolonnu lejasdaļā. Šīs kopsummas tiek rādītas kājenes sadaļā režģa apakšdaļā. 

### <a name="showing-the-grid-footer"></a>Režģa kājenes parādīšana
Katram programmatūras Finance and Operations tabulārajam režģim režģa apakšsaļā ir kājenes apgabals, kas var parādīt vērtīgu informāciju, kas saistīta ar parādītajiem datiem. Šajā informācijā ietilpst tālāk norādītie elementi. 
-  Atlasīto rindu skaits tabulā (ja ir atlasīts vairāk nekā viens ieraksts)
-  Kopsummas, kas atrodas konfigurēto skaitlisko kolonnu lejasdaļā
-  Datu kopā ietverto rindu skaits 

Šī kājene pēc noklusējuma ir paslēpta, bet to var viegli ieslēgt. Lai parādītu režģa kājeni, noklikšķiniet ar peles labo pogu režģī uz kolonnas galvenes un atlasiet opciju **Rādīt kājeni**. Pēc tam, kad kājene ir ieslēgta noteiktam režģim, šis iestatījums tiks saglabāts, kamēr lietotājs izvēlas slēpt kājeni, ko var izdarīt, ar peles labo pogu noklikšķinot uz kolonnas galvenes un atlasot **Paslēpt kājeni**.  Ievērojiet, ka turpmākā atjauninājumā plānots pārvietot darbības **Rādīt kājeni/paslēpt kājeni** novietojumu. 

### <a name="specifying-columns-with-totals"></a>Kolonnu ar kopsummām norādīšana
Pašlaik kolonnas netiks konfigurētas kopsummu rādīšanai pēc noklusējuma. Tā tiek uzskatīta par vienreizējas iestatīšanas darbību, kas ir līdzīga kolonnu platumu pielāgošanai režģos. Kad esat norādījis, ka vēlaties redzēt kolonnas kopsummas, šis iestatījums tiek saglabāts nākamajai reizei, kad apmeklēsiet lapu.  

Ir divi veidi, kā konfigurēt kolonnu, lai parādītu kopsummu. 
1.  Ar peles labo pogu noklikšķiniet uz kolonnas, kurai vēlaties redzēt kopsummu, un atlasiet **Aprēķināt šīs kolonnas kopsummu**. Šī darbība nodrošinās trīs citas darbības. Vispirms tā aktivizēs kājenes redzamību. Otrkārt, tas saglabās izvēli redzēt kopsummu šajā kolonnā. Treškārt, ar šo darbību tiks uzsākta kopsummas aprēķināšana šai kolonnai un citām, ko iepriekš esat konfigurējis, lai skatītu kopsummas. Laiks, kas ir nepieciešams, lai parādītu kopsummu, ir tieši saistīts ar tās datu kopas lielumu, kurai vēlaties uzzināt kopsummu.  

2.  Kad kājene ir parādīta, varat arī noklikšķināt uz pogas **Rādīt kopsummu** kājenes apgabalā, kas atrodas tās kolonnas apakšā, kurai jūs vēlaties redzēt kopsummu. Ja nav nevienas konfigurētas kolonnas, tad visām skaitliskajām kolonnām būs redzama poga **Rādīt kopsummu**. Ja ir vismaz viena kolonna, kas konfigurēta kopsummām, pogas **Rādīt kopsummu** būs pieejamas tikai uzvirzot kursoru vai fokusējot. Šī darbība saglabā jūsu izvēli redzēt šīs kolonnas kopsummu turpmākos šīs lapas apmeklējumos, un šis stāvoklis tiek apzīmēts ar svītru, kas šajā kolonnā tiek parādīta kājenē (vai, ja datu kopa ir pietiekami maza, kopsumma tiks parādīta nekavējoties).

Ja kļūdāties un nevēlaties redzēt kopsummu noteiktā kolonnā, ar peles labo pogu noklikšķiniet uz kolonnas un atlasiet **Paslēpt kopsummu**, vai arī atlasiet pogu **Paslēpt kopsummu** šīs kolonnas kājenē. Šī izvēle tiks saglabāta arī turpmākiem lapas apmeklējumiem. 

### <a name="calculating-totals"></a>Aprēķina kopsummu
Ja, atnākot uz lapu, kājene ir redzama un kolonnas jau ir konfigurētas kopsummām, tās var tikt rādītas kājenē vai arī var netikt rādītas. Šī darbība ir atkarīga no datu kopas izmēra lapā. Ja datu kopa ir pietiekami maza, kopsummas tiks rādītas automātiski vienlaikus ar rindu skaitu datu kopā. Ja kājenē zem kolonnām, ko konfigurējāt kopsummām, ir svītras, tad datu kopa ir pārāk liela, lai sistēma uzreiz parādītu kopsummas, un kopsummu aprēķināšanai vajadzīga tieša darbība. Lai to izdarītu, noklikšķiniet kājenē uz pogas **Aprēķināt** vai ar peles labo pogu noklikšķiniet uz kolonnas, kurai vēlaties kopsummu, un atlasiet **Aprēķināt šīs kolonnas kopsummu**.  

Ja aprēķināsana notiek pārāk ilgi, varat atcelt operāciju, atlasot pogu **Atcelt**. Tomēr dažkārt datu kopa būs pārāk liela, lai aprēķinātu kopsummas (ierobežojums, ko nosaka jūsu organizācija), un jūs tiksiet informēts, lai vairāk filtrētu savus datus.

Kopsummas tiks automātiski atjauninātas, datu kopā atjauninot, dzēšot vai izveidojot rindas.  

## <a name="grouping-data"></a>Datu grupēšana
Biznesa lietotājiem bieži jāveic datu ekspromtanalīze. Lai gan to var izdarīt, eksportējot datus uz Microsoft Excel un izmantojot pivot tabulas, **Grupēšanas** iespēja tabulārajā režģī ļauj lietotājiem programmās Finance and Operations organizēt savus datus interesantākos veidos. Līdzīgi kā šis līdzeklis paplašina līdzekli **Kopsumma**, arī **Grupēšana** ļauj iegūt izsmeļošu ieskatu datos, sniedzot apakšsummas grupas līmenī.

Lai izmantotu šo funkciju, ar peles labo pogu noklikšķiniet uz kolonnas, pēc kuras vēlaties grupēt, un atlasiet **Grupēt pēc šīs kolonnas**. Veicot šo darbību, dati tiks šķiroti pēc atlasītās kolonnas, režģa sākumā tiks pievienota jauna Grupa pēc kolonnas un katras grupas sākumā tiks ievietotas “virsraksta rindas”. Šīs virsraksta rindas sniedz tālak norādīto informāciju par katru grupu. 
-  Grupas datu vērtība 
-  Kolonnas etiķete. Tas būs īpaši noderīgi, ja tiek atbalstīti vairāki grupēšanas līmeņi.  
-  Datu rindu skaits šajā grupā
-  Kolonnu, kas konfigurētas kopsummu rādīšanai, apakšsummas

Kad ir aktivizēti [Saglabātie skati](saved-views.md), šo grupēšanu var saglabāt ar personalizāciju kā daļu no skata, lai nākamreiz, kad apmeklēsiet šo lapu, nodrošinātu ātru piekļuvi.  

Ja izvēlaties **Grupēt pēc šīs kolonnas** citā kolonnā, sākotnējā grupēšana tiks aizstāta, jo 10.0.9/Platform Update 33 tiek atbalstīts tikai grupēšanas līmenis.

Lai režģī atceltu grupēšanu, ar peles labo pogu noklikšķiniet uz grupēšana kolonnas un atlasiet **Atgrupēt**.  


## <a name="evaluating-math-expressions"></a>Matemātisko izteiksmju novērtēšana
Lietotājs var darboties kā produktivitātes palielinātājs, ievadot matemātiskas formulas režģa skaitliskajās šūnās, nevis veicot aprēķinus programmā, kas atrodas ārpus sistēmas. Piemēram, varat ievadīt **= 15\*4** un iziet no lauka. Sistēma novērtēs izteiksmi un saglabās laukam vērtību "60".

Lai sistēma atpazītu vērtību kā izteiksmi, sāciet vērtību ar vienādības zīmi (**=**). Plašāku informāciju par atbalstītajiem operatoriem un sintaksi skatiet [Atbalstītie matemātiskie simboli](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols).  
