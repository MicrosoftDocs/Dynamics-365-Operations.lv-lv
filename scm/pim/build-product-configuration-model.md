---
title: "Veidot preču modeļa konfigurācija"
description: "Nepieciešamība konfigurēt produktus tā, lai tie apmierinātu īpašas prasības, kļūst par normu nevis par izņēmumu gan starpuzņēmumu attiecībās, gan uzņēmumu un patērētāju attiecībās."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8353b0bc6601aa38ca3e93d89e33a1f2f4205a60
ms.lasthandoff: 03/31/2017


---

# <a name="build-a-product-configuration-model"></a>Veidot preču modeļa konfigurācija

Nepieciešamība konfigurēt produktus tā, lai tie apmierinātu īpašas prasības, kļūst par normu nevis par izņēmumu gan starpuzņēmumu attiecībās, gan uzņēmumu un patērētāju attiecībās.

Ražotājam, kas atbalsta konfigurācijas atbilstoši pasūtījumam scenārijus, ir iespēja rūpīgāk ievērot klientu vajadzības. Turklāt, uzglabājot nepabeigtas preces vispārēju komponentu formā, nevis gatavās produkcijas formā, ražotājs var samazināt kapitālu, kas ir saistīts ar krājumiem.  

Veiksmīga pāreja no ražošanas krājumu izveidei uz konfigurēšanu atbilstoši pasūtījumam pieprasa rūpīgu preču struktūras analīzi, preču saimju identificēšanu un komponentu sastāvu. Lai samazinātu daļu skaitu un minimizētu procesā esošo preču skaitu, ir ļoti svarīgi saprast preču interfeisus un ka izstrādājat otrreizējas izmantojamības nolūkiem.  

Ir vairāki preču konfigurācijas modelēšanas principi, piemēram, modelēšana atbilstoši nosacījumiem, atbilstoši dimensijām un atbilstoši ierobežojumiem. Pētījumi rāda, ka metodoloģija atbilstoši ierobežojumiem var samazināt koda rindu skaitu modeļos par 50 procentiem, salīdzinot ar citiem modelēšanas principiem. Tāpēc šī metodika var samazināt īpašumtiesību kopējās izmaksas (TCO). Pārceļot no noteikumu modeli, kas ir balstīta uz X + + kodā, lai ierobežojums balstītu modeli, jums vairs nav nepieciešama izstrādātāja licenci, lai uzturētu preču modeļus.

## <a name="product-configuration"></a>Preces konfigurācija
Industrializācijas periods ir novedis pie lieliem sasniegumiem augstas kvalitātes un funkcijām bagāto preču ražošanā par pieņemamām cenām. Apjomradīti ietaupījumi ļāva vairumam cilvēku industrializētā pasaulē iegādāties automašīnas, televizorus, mājsaimniecības preces un citas preces, ko lielākā daļa no mums uzskata par nepieciešamu mūsu ikdienas dzīves sastāvdaļu.  

Kad daudzas preces ir kļuvušās par patēriņa precēm, ir radusies nepieciešamība tās diferencēt. Ražotāju tūlītējā reakcija uz šo problēmu bija veidot vairākus katras preces variantus, lai klientiem būtu vairāk alternatīvu. Šīs stratēģijas rezultātā palielinājās prognozēšanas problēmas, kā arī palielinājās krājumu izmaksas un novecojušo nepārdoto preču skaits.  

Pieņemot konfigurēšanas atbilstoši pasūtījumam filozofiju, ražotājiem ir iespēja apmierināt klientu pieprasījumu pēc unikālam precēm, vienlaikus samazinot vai likvidējot novecojušos noliktavas krājumus. Pārejot no ražošanas krājumu izveidei filozofijas uz konfigurēšanas atbilstoši pasūtījumam filozofiju, viena tiešā problēma būs saistīta ar to, ka nepieciešamība pēc īsa izpildes laika būs jālīdzsvaro ar zemiem krājumu līmeņiem.  

Lai to veiksmīgi nodrošinātu, ir rūpīgi jāanalizē preču portfelis un jāmeklē modeļi gan produkta funkcijās, gan procesos. Mērķis ir noteikt vispārējos komponentus, ko var ražot viena iekārta un ko var izmantot visos variantos.  

Jauna preču konfigurācijas līdzekļu kopa ietver lietotāja interfeisu (UI), kas nodrošina preces konfigurācijas modeļa struktūras vizuālu pārskatu un arī deklaratīvu ierobežojuma sintaksi, kas nav jākompilē. Tāpēc uzņēmumiem, kas vēlas atbalstīt konfigurācijas praksi, ir vieglāk sākt to darīt. Kā paskaidrots nākamajās nodaļās, preces noformētājam vairs nav nepieciešams izstrādātāja atbalsts, lai izveidotu preces konfigurācijas modeli, to pārbaudītu un izlaistu pārdošanas organizācijai.

## <a name="building-a-product-configuration-model"></a>Preces konfigurācijas modeļa izveide
Ir vairākas pieejas, kurus lietotājs var izmantot, lai izveidotu preces konfigurācijas modeli. Viena iespēja ir sekot secīgai plūsmai, vispirms izveidojot visus atsauces datus, piemēram, preces šablonus, atšķirīgas preces un darbības resursus, un pēc tam ietverot tos preces konfigurācijas modelī kā komponentus, materiālu komplekta (MK) rindas, maršruta operācijas un citus elementus. Alternatīvi var izvēlēties iteratīvāku pieeju, vispirms izveidojot modeli un pēc tam, pēc vajadzības, pievienojot atsauces datus.

### <a name="components"></a>Komponenti

Preces konfigurācijas modeli veido viens vai vairāki komponenti, kas ir iesaistīti apakškomponentu attiecībās. Komponenti tiek definēti vienu reizi, un pēc tam tos var izmantot daudzas reizes vienā vai vairākos preces konfigurācijas modeļos. Komponenti ir preces konfigurācijas modeļa galvenie elementi, un gandrīz visa informācija par modeli ir saistīta ar tiem.

### <a name="attributes"></a>Atribūti

Katram komponentam ir viens vai vairāki atribūti, kas identificē tā īpašības. Lietotāji izvēlēsies atribūtus konfigurācijas procesā. Atribūti kontrolē starpkomponentu un iekškomponentu attiecības, kad tos iekļauj ierobežojumos vai aprēķinos. Izmantojot nosacījumus, kas tiek lietoti MK rindas, atribūtus var izmantot, lai noteiktu fiziskās daļas, no kurām sastāvēs konfigurētā prece. Turklāt atribūts var kontrolēt MK rindas rekvizītu ar kartēšanas mehānismu. Līdzīga funkcionalitāte ir maršruta operācijām attiecībā uz iekļaušanu un rekvizītu iestatījumiem.

### <a name="expression-constraints"></a>Izteiksmes ierobežojumi

Preces konfigurācijas modeļa atbilstoši ierobežojumam izmantošana paredz, ka daži ierobežojumi pastāv, lietotājam atlasot dažādu atribūtu vērtības. Šos ierobežojumus var ieviest kā izteiksmes ierobežojumus, izmantojot optimizācijas modelēšanas valodu (OML). Alternatīvi ierobežojumu var īstenot tabulas ierobežojumu formā.

### <a name="table-constraints"></a>Tabulas ierobežojumi

Tabulu ierobežojumi var būt lietotāja definēta vai sistēmas definēta.  

Lietotāja definētu tabulas ierobežojumu veido lietotājs. Lietotājs atlasa atribūtu tipu kombināciju, kas pārstāvēs tabulas kolonnas, un pēc tam ievada vērtības no atlasīto atribūtu tipu domēniem, lai veidotu rindas tabulas ierobežojumā.  

Atlasot kuru Microsoft Dynamics 365 uz operāciju galda, lai izmantotu kā atsauci un pēc tam atlasot laukus no šīs tabulas, lai no kolonnas ierobežojumu definē sistēmas definēta satura ierobežojums. Rindas tabulā ierobežojums ir Dynamics 365 operāciju galda rindas, kas atrodas konfigurācijas laikā.  

Tabulas ierobežojums tiek iekļauts preces konfigurācijas modelī, izmantojot atsauci uz tabulas ierobežojuma definīciju un kartējot attiecīgos atribūtus modelī tabulas ierobežojuma kolonnās.

### <a name="calculations"></a>Aprēķini

Aprēķini ir aritmētisko operāciju veikšanas mehānisms konfigurācijas modelī. Piemēram, aprēķins var noteikt noteikta izejvielas gabala garumu vai pulēšanas operācijas apstrādes laiku. Aprēķini ir obligāti un iestata mērķa atribūta vērtību, kad būs pieejamas visu atribūtu vērtības, kas ietvertas aprēķina izteiksmē.

### <a name="subcomponents"></a>Apakškomponenti

Apakškomponenti atspoguļo mezglus preču konfigurācijas modeļa struktūrā. Attiecībā uz katru apakškomponentu attiecību jānorāda atsauce uz preces šablonu, kuram varianta konfigurācijas tehnoloģija ir iestatīta uz konfigurāciju atbilstoši ierobežojumam.

### <a name="user-requirements"></a>Lietotāju prasības

Lietotāja pieprasījumā ir visas apakškomponentu sastāvdaļas. Vienīgā atšķirība ir tas, ka lietotāja pieprasījums nav saistīts ar preces šablonu. Šis atšķirības praktiskais efekts ir tāds, ka MK rindas vai maršruta operācijas, kas ir noteiktas lietotāja pieprasījuma kontekstā, ir sakļautas primārā komponenta MK struktūrā vai maršrutā. Šī uzvedība līdzinās fantoma MK uzvedībai.

### <a name="bom-lines"></a>MK rindas

MK rindas ir iekļautas, lai noteiktu katra komponenta ražošanas MK. MK rindā jābūt atsaucei uz krājumu un visus krājuma rekvizītus var iestatīt uz fiksētu vērtību vai kartēt atribūtā.

### <a name="route-operations"></a>Maršruta operācijas

Maršruta operācijas ir ietvertas, lai identificētu ražošanas maršrutu. Maršruta operācijā jābūt atsaucei uz noteiktu operāciju, un visus operācijas rekvizītus var iestatīt uz fiksētu vērtību. Visus rekvizītus, izņemot resursu prasības, var kartēt uz atribūtu nevis vērtību.

## <a name="validating-and-testing-a-product-configuration-model"></a>Preces konfigurācijas modeļa pārbaude un testēšana
Preces konfigurācijas modeļa pārbaude var notikt vairākos līmeņos modelī, un tādēļ dažādās sfērās. Zemākais līmenis ir vienas izteiksmes ierobežojums. Šajā gadījumā pārbaudi parasti veic preces noformētājs, lai pārliecinātos, ka izteiksmes sintakse ir pareiza.  

Tāpat MK rindas vai maršruta operācijas nosacījumu var pārbaudīt atsevišķi.  

Pārbaudi var veikt arī attiecībā uz lietotāja definētu tabulas ierobežojuma definīciju. Šajā gadījumā lietotājs var pārbaudīt, vai vērtības, kas ievadītas katrā laukā, atrodas atbilstošo atribūtu tipu domēnā.  

Visbeidzot, pārbaudi var veikt pilnam preces konfigurācijas modelim, lai pārbaudītu, vai visa sintakse ir pareiza un vai ir ievērotas visas nosaukumdošanas un modelēšanas prasības.

### <a name="testing"></a>Testēšana

Testēšanas paraugu ir līdzīgi darbojas patiesā konfigurācijas sesiju. Lietotājs var staigāt caur konfigurācijas lapu un pārliecinieties, vai modeļa struktūra atbalsta konfigurācijas procesu. Lietotājs var pārbaudīt, vai atribūtu vērtības ir pareizas, un atribūtu apraksti palīdz lietotājam izvēlēties pareizas vērtības. Visbeidzot, pēc testēšanas sesijas pabeigšanas sistēma mēģina izveidot MK un maršrutu, kas atbilst atlasītajām atribūtu vērtībām, un rāda kļūdas ziņojumu, ja kaut kas ir nepareizi.

### <a name="the-configuration-page"></a>Konfigurācijas lapa

Lai pārvietotos starp komponentiem, noklikšķiniet uz **Nākamais**, vai noklikšķiniet uz komponenta preces konfigurācijas modeļa kokā, lai iestatītu fokusu uz to.

## <a name="finalizing-a-model-for-configuration"></a>Konfigurācijas modeļa pabeigšana
Kad preces konfigurācijas modelis ir gatavs izmantošanai konfigurācijas atbilstoši pasūtījumam scenārijos, ir jāizveido versija. Tomēr ir vairākas opcijas, kas uzlabo modelēšanas pieredzi.

### <a name="user-interface"></a>Lietotāja interfeiss

Konfigurācijas UI var modificēt, ieviešot atribūtu grupas vienā vai vairākos apakškomponentos. Šāda grupēšana var izcelt attiecības starp specifiskiem atribūtiem un palīdzēt konfigurācijas lietotājam identificēt preces zonas, kas pašlaik ir fokusā.

### <a name="templates"></a>Veidnes

Viena vai vairākas konfigurācijas veidnes var izveidot, lai paātrinātu konfigurācijas procesu. Alternatīvi veidnes var izveidot, lai veicinātu specifiskas atribūtu kombinācijas, piemēram, kad pārdošanas kampaņa koncentrējas uz noteiktu preču funkciju kopu.

### <a name="translations"></a>Tulkojumi

Ja prece tiks pārdota dažādās valstīs/reģionos, var izveidot visu tekstu tulkojumus, kas tiek parādīti konfigurācijas UI. Šis teksts ietver ne tikai nosaukuma un apraksta laukus, bet arī atribūta teksta vērtības.

### <a name="versions"></a>Versijas

Pēdējais un svarīgākais solis pabeigšanas procesā ir izveidot preces konfigurācijas modeļa versiju. Šī versija attēlo attiecības starp preces šablonu, kuru var atlasīt konfigurācijai pasūtījuma vai piedāvājuma rindā, un preces konfigurācijas modeli. Pirms izmantošanas konfigurācijas sesijā versija ir jāapstiprina un jāaktivizē.

## <a name="extending-a-product-configuration-model-through-the-api"></a>Preces konfigurācijas modeļa paplašināšana, izmantojot API
Atvēlētais lietojumprogrammu programmēšanas interfeiss (API) tiek ieviests, lai partneri un pārējie, kam ir izstrādātāja licence, varētu paplašināt preces konfigurācijas modeļa iespējas. Galvenais mērķis ir izveidot mehānismu, kas pieņemsim, partneriem un klientiem, kas izmanto esošo preču konfiguratorā migrē kodu, kas ir iestrādāta preču konfiguratora modeļiem API. Šādā veidā, viņi var migrēt savus modeļus no preču konfiguratora uz preču konfigurāciju. Tomēr, jauni partneri un klienti var gūt labumu arī no API izmantošanas, lai paplašinātu jaunus preces konfigurācijas modeļus.

### <a name="pcadaptor-class"></a>PCAdaptor klase

API tiek ieviests, izmantojot **PCAdaptor** klašu kopu, kas atklāj preces konfigurācijas modeļu datu struktūru. Gadījums, **PCAdaptor** klases jāveido katram modelim, kas tiks paplašināta. Kad konfigurēšanas sesija ir pabeigta, sistēma pārbauda, piemēram, šajā klasē un darbojas, ja tiek konstatēts.  

Procesu apraksta šī plūsmas diagramma.  

[![Plūsmas diagramma](./media/product_configuration_2.png)](./media/product_configuration_2.png)  

Izstrādājuma konfigurācijas API plūsmas shēma

## <a name="product-configuration"></a>Preces konfigurācija
Preču konfigurāciju var veikt no šādām vietām:

-   Pārdošanas pasūtījuma rinda
-   Pārdošanas piedāvājuma rinda
-   Pirkšanas pasūtījuma rinda
-   Ražošanas pasūtījuma rinda
-   Krājumu vajadzības rinda (projekts)

Konfigurācijas mērķis ir izveidot atšķirīgus preces variantus, kas atbilst klienta vajadzībām. Unikāls konfigurācijas ID tiek izveidots katrai jaunai konfigurācijai. Šis ID ļauj veikt krājumu izsekošanu.

### <a name="multiple-sites-and-intercompany"></a>Vairākas vietas un vairāki uzņēmumi

Ja konfigurācija tiks veikta vietā vai pat uzņēmumā, kas atšķiras no vietas vai uzņēmuma, kurā notiks ražošana, tiks izveidots MK un maršruts un tie tiks nodoti piegādātāja vietai piegādātāja uzņēmumā. Preces variants tiks izlaists visos uzņēmumos, kas piedalās piegādes ķēdē.


