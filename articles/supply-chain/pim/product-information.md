---
title: "Preču informācijas pārskats"
description: "Šajā tēmā ir sniegta informācija par preču informācijas pārvaldību. Preču informācijas pārvaldība darbojas ar kopīgoto preču definīciju, kategoriju un identifikatoriem visās juridiskajās personās, kā arī ar noteiktām preču konfigurācijām, lai ietilptu biznesa procesos."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: cvocph
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: db8a9666518b58b6b32bb4a14933095dd9416aa0
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017

---

# <a name="product-information-overview"></a>Preču informācijas pārskats

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Šajā tēmā ir sniegta informācija par preču informācijas pārvaldību. Preču informācijas pārvaldība darbojas ar kopīgoto preču definīciju, kategoriju un identifikatoriem visās juridiskajās personās, kā arī ar noteiktām preču konfigurācijām, lai ietilptu biznesa procesos. 

Preču informācija ir piegādes ķēžu un mazumtirdzniecības programmu pamats visās nozarēs. Tas attiecas uz procesiem un tehnoloģijām, kas fokusējas uz centralizētu preču informācijas pārvaldību (piemēram, piegādes ķēdēs). Ir svarīgi izmantot kopīgotas preču definīcijas, dokumentāciju, atribūtus un identifikatorus. Dažādos biznesa risinājumu moduļos preču informācija un konfigurācija ir vajadzīga, lai pārvaldītu biznesa procesus, kas ir saistīti ar īpašām precēm, preču saimēm vai kategorijām.

## <a name="product-definition"></a>Preču definīcija

Preces galvenokārt nosaka pēc preces numura, nosaukuma un apraksta. Lai aprakstītu preci vai pakalpojumu, tomēr ir nepieciešami arī citi dati.

- Preces veids: krājums vai pakalpojums
- Preces apakšveids: atšķirīgas preces vai preču šabloni
- Preces varianta modeļa definīcija

     - Preču dimensijas un dimensiju grupas
     - Preču nomenklatūra
     - Preču konfigurācijas modeļi

- Preces saistība ar vienu vai vairākām kategorijām
- Preces un kategorijas atribūtu definīcija
- Preces attēli
- Pielikumi
- Mērvienības un saistītās pārveides
- Visu nosaukumu un aprakstu tulkojumi

## <a name="distribution-export-and-import-of-product-data"></a>Preces datu izplatīšana, imports un eksports

Preces definīciju var izveidot programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise. Tas var arī importēt no šādām sistēmām: preces dzīves cikla pārvaldība (PLM), preču datu pārvaldība (PDM) vai preces informācijas pārvaldība (PIM). Ja tiek izmantotas vairākas Finance and Operations instances, viena instance parasti tiek izmantota kā visu pārējo instanču preču datu šablons. Šo pieeju atbalsta liela datu elementu kopa, kas ļauj eksportēt un importēt preču definīcijas datus no vienas instances uz citu.

Lai atbalstītu preces datu izplatīšanu vairākās instancēs, Finance and Operations ļauj izmantot pakalpojumu Common Data Service. Preču definīcijas var eksportēt no Finance and Operations instances pakalpojumā Common Data Service. Preču definīcijas pēc tam var izmantot, lai nodrošinātu citas biznesa programmas, piemēram, Microsoft Dynamics 365 for Sales, ar preces datiem.

Ņemiet vērā, ka dinamiskās un elastīgās organizācijās, preču informācijas dati mainās katru dienu. Tādēļ precīzu un aktuālu preču datu uzturēšana ir būtisks biznesa process.

## <a name="product-masters-and-product-variants"></a>Preču šabloni un varianti

Elastīgā pasaulē, ja preces ir ātri jāpielāgo klienta prasībām, preču definīcijas jānorāda kā preču kopa nevis atšķirīgas preces. Programmatūrā Microsoft Dynamics 365 for Finance and Operations šīs vispārīgās preces tiek dēvētas par *preču šabloniem*. Preču šabloni satur definīciju un kārtulas, kas norāda, kā atšķirīgas preces tiek aprakstītas un darbojas biznesa procesos. Pamatojoties uz šīm definīcijām, var tikt ģenerētas atšķirīgas preces. Šīs atšķirīgās preces tiek sauktas par *preces variantiem*.

Programmatūrā Finance and Operations preces šablons tiek saistīts ar preču dimensiju grupu un konfigurācijas tehnoloģiju, lai norādītu biznesa kārtulas. Preču dimensijas (krāsa, izmēri, stils un konfigurācija) ir specifiskas atribūtu kopas, ko var izmantot visā programmā, lai definētu un izsekotu noteiktu saistīto preču izturēšanos. Šīs dimensijas arī palīdz lietotājiem meklēt un identificēt preces.

## <a name="configuration-technologies"></a>Konfigurācijas tehnoloģijas

Varat izvēlēties no trim konfigurācijas tehnoloģijām.

- Iepriekš definēti varianti tiek definēti ar iepriekš definētām preču dimensijām. Varianta definīcija ietver noteiktas derīgas dimensiju kombinācijas definīciju, piemēram, krāsu, stilu un izmēru. Katra kombinācija veido atšķirīgu preces variantu.
- Konfigurāciju atbilstoši dimensijām parasti lieto ražošanas scenārijos, un tā ļauj izmantot konfigurācijas dimensiju materiālu komplektu (MK) definīcijā. Ja noteikta konfigurācija ir atlasīta, sistēma izmanto plānošanā un ražošanā to MK rindu apakškopu, kuras ir derīgas attiecīgajai konfigurācijai. Šī koncepcija ir zināma arī kā *globālais MK*, jo viens koplietojams MK tiek izmantots visām preces konfigurācijām.
- Konfigurācijas atbilstoši ierobežojumam preces izmanto konfigurācijas modeli, lai aprakstītu visus iespējamos atribūtus un komponentus, kas nepieciešami, lai vienā modelī aprakstītu visus iespējamos preces variantus. Atribūtu kombināciju ierobežojumus var aprakstīt, izmantojot regulāras izteiksmes vai tabulas ierobežojumus. Konfigurācijas modeļi un konfigurētāji kļūst svarīgāki preču informācijas pārvaldības procesā un tiek izmantoti visās nozarēs.

Plānojot Finance and Operations ieviešanu, ir ļoti svarīgi izvēlēties pareizu biznesa procesa konfigurācijas tehnoloģiju. Preci nevar pārveidot no viena modeļa uz citu pēc ieviešanas.

## <a name="product-variant-model-definition-workspace"></a>Preces varianta modeļa definīcijas darbvieta

**Preces varianta modeļa definīcijas** darbvieta sniedz pārskatu par preču šabloniem. Tas parāda arī šablonu un saistīto variantu izlaišanas statusu konkrētām juridiskām personām.

## <a name="released-products"></a>Izlaistās preces

Preces, kas tiek izlaistas konkrētai juridiskajai personai tiek sauktas par *izlaistajām precēm*. Preces var izlaist lielapjoma vienībās vienai juridiskajai personai vai vienlaicīgi vairākām juridiskajām personām. Juridiskajai personai var pievienot dažādus preču rekvizītus un atribūtus, tādēļ darbvieta **Izlaisto preču uzturēšana** ļauj pārraudzīt un pabeigt katrai juridiskajai personai vai juridiskās personas apakšorganizācijām nesen izlaistās preces.

### <a name="released-product-maintenance-workspace"></a>Izlaisto preču uzturēšanas darbvieta

Darbvietu **Izlaisto preču uzturēšana** varat konfigurēt no izvēlnes vienuma **Konfigurēt manu darbvietu**. Atlasiet mazumtirdzniecības kategoriju hierarhiju un kategoriju, lai filtrētu darbvietu. Lai koriģētu darbvietas preču datus, var arī norādīt, dienās, laika periodus **Pēdējās izlaistās preces** un **Preces, kuru izlaide ir pārtraukta**.

Darbvietu veido elementu un divu sarakstu kopsavilkums. Sarakstā **Atvērtie pieteikumi** tiek rādīti preču izmaiņu gadījumi, kuriem ir preces atlasītajā preču kategoriju hierarhijā, kas nav pabeigtas un slēgtas. Sarakstā **Pēdējās izlaistās** tiek rādītas preces, kas tika izlaistas laika periodā, kas tika iestatīts darbvietas konfigurācijā. Katram saraksta krājumam tiek veikta pārbaude un tiek parādīts pārbaudes statuss. Šis statuss varētu norādīt, ka juridiskajai personai nepieciešamā konfigurācija nav pabeigta. No saraksta varat tieši piekļūt lapai **Nodoto preču papildinformācija**, **Preces īpašību uzturēšana**, **Preces kategorijas uzturēšana**, **Noklusējuma pasūtījuma iestatījumi** un **Teksta tulkojumi**, lai pabeigtu nepieciešamo preču konfigurāciju.

### <a name="manually-creating-a-new-released-product"></a>Manuāla jaunas izlaistās preces izveide

Varat manuāli izveidot izlaistu preci vienā izpildē, atkarībā no organizācijas biznesa procesiem un noteikumiem par to, vai vajadzētu izmantot šo funkciju. Šī funkcija izveido jaunu preci un automātiski atbrīvo to pašreizējai juridiskajai personai. Lai izveidotu jaunu preci, noklikšķiniet uz **Izlaistās preces** darbvietā **Izlaisto preču uzturēšana** vai saraksta lapā **Izlaistā prece**.

