---
title: E-pasta veidnes
description: "Šajā tēmā ir sniegta informācija par e-pasta veidnēm, kuras varat izveidot un izmantot programmā Microsoft Dynamics 365 for Talent - Attract."
author: josaw
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 8166047a768c47219855c55a1008f3dd24cd5344
ms.openlocfilehash: e02912ad242186fe3e2dd8d7a4cc7312aec6015e
ms.contentlocale: lv-lv
ms.lasthandoff: 01/04/2019

---

# <a name="email-templates"></a>E-pasta veidnes
[!include[banner](../includes/banner.md)]

Izmantojot e-pasta veidņu bibliotēku, administratori var nodrošināt vienotu dizainu un zīmolradi visiem e-pasta ziņojumiem, kas tiek nosūtīti, izmantojot Microsoft Dynamics 365 for Talent: Attract. Administratori arī var pārraudzīt e-pasta satura veidņu kolekciju, ko var izmantot citi lietotāji. Darbā pieņemšanas grupa var izmantot šīs veidnes savā darbplūsmā, lai nosūtītu e-pasta ziņojumus daudz efektīvāk. Daži e-pasta ziņojumi programmā Attract ir konfigurēti automātiskai nosūtīšanai, un administrators var izmantot e-pasta veidņu bibliotēku, lai pielāgotu šādu e-pasta ziņojumu saturu.

> [!NOTE]
> Lai izmantotu e-pasta veidnes, jūsu organizācijai ir jābūt pieejamai visaptverošās darbā pieņemšanas pievienojumprogrammai.

## <a name="global-template-configurations"></a>Globālās veidņu konfigurācijas

Lai nodrošinātu konsekventu zīmolradi visos e-pasta ziņojumos, administratoram vispirms jāiestata globālā galvene un kājene visām e-pasta veidnēm. Administrēšanas centra cilnes **E-pasta veidņu iestatījumi** sadaļā **Galvene** administrators var augšupielādēt attēlu, kas tiks izmantots kā galvene vai reklāmkarogs visos e-pasta ziņojumos. Attēls var būt uzņēmuma logotips, iespiests uzraksts vai cits reprezentatīvs attēls. Ieteicamais platums ir no 25 līdz 800 pikseļiem un augstums — no 25 līdz 150 pikseļiem, jo šie izmēri ir optimāli lielākajai daļai e-pasta klientu, piemēram, Microsoft Outlook. Attēla failam jābūt JPEG, JPG, PNG vai SVG formātā, un faila lielumam jābūt mazākam par 1 megabaitu (MB). Pēc attēla augšupielādes tiek ģenerēts un parādīts galvenes priekšskatījums. Ja ir jānoņem vai jānomaina galvenes attēls, administrators var izmantot opciju **Noņemt** virs priekšskatījuma.

Sadaļā **Kājene** administrators var sniegt saites uz uzņēmuma konfidencialitātes politiku saziņai un uz noteikumiem un nosacījumiem. Šīs saites ir iekļautas kājenē, kas tiek ģenerēta automātiski. Pēc tam tiek parādīts šīs kājenes priekšskatījums.

Pārliecinieties, ka ir saglabātas izmaiņas pirms administrēšanas centra aizvēršanas.

> [!NOTE] 
> Galvene un kājene ir globāli iestatījumi visiem e-pasta ziņojumiem. Tādēļ tā parādīsies visos e-pasta ziņojumos, kas tiek nosūtīti, izmantojot Attract. Ja nav konfigurēti iestatījumi, e-pasta ziņojumos netiks izmantota ne galvene, ne kājene.

## <a name="email-template-library"></a>E-pasta veidņu bibliotēka 

Pēc globālo veidņu konfigurāciju iestatīšanas administrators var sākt izveidot un pārraudzīt veidnes visiem e-pasta ziņojumiem, kas tiek sūtīti no Attract. E-pasta veidņu bibliotēka ir pieejama tikai administratoriem. Lai atvērtu bibliotēku, galvenajā navigācijas izvēlnē atlasiet cilni **E-pasta veidnes**. Bibliotēka tiek iedalīta pēc dažādām aktivitātēm programmā Attract, saistībā ar kurām jāsūta e-pasta ziņojumi, piemēram, plānošana, novērtēšana un darba izveide. Administrators var atlasīt jebkuras kategorijas, lai apskatītu visus e-pasta tipus, kas saistīti ar šo aktivitāti. Piemēram, atlasiet **Plānošana**, lai skatītu dažādus e-pasta ziņojumu tipus, kas tiek nosūtīti plānošanas procesa laikā, un visas veidnes, kas ir pieejamas katram e-pasta ziņojumu tipam. Katra kategorijas apakšsadaļa norāda e-pasta ziņojuma tipu.

Dažiem e-pasta ziņojumu tipiem var būt vairāk par vienu saņēmēju. Piemēram, kategorijā **Plānošana** e-pasta paziņojumi, kas tiek nosūtīti, ja ir nepieciešams interviju grafika kopsavilkumu, tiek nosūtīti gan kandidātiem, gan intervētājiem. Katrā sadaļā ir divas galvenās kolonnas: **Veidnes nosaukums** un **Saņēmējs**. Katra sadaļas rinda norāda vienu veidni noteiktam e-pasta ziņojumu tipam. Sākumā katras veidnes rindā tiks parādīts slēdzenes simbols. Šis simbols norāda, ka veidne ir standarta veidne, kas tiek nodrošināta ar programmu Attract, un ka to nevar dzēst. Jebkurai veidnei administrators var izmantot daudzpunktes pogu (**...**), lai dublētu veidni, iestatītu to kā noklusējuma veidni vai dzēstu to. Kad veidne ir iestatīta kā noklusējuma veidne, var tikt īstenots viens no šādiem režīmiem. Režīmu norāda žetons vai žetoni, kas parādās veidnes rindā:

- **Noklusējums** — šis žetons norāda, ka veidne ir noklusējuma veidne e-pasta ziņojumam, kas ir nosūtīts, un ka tajā tiks ievadīta informācija, kad lietotājs nosūta konkrēto e-pasta ziņojumu tipu.
- **Noklusējums** + **Automātiskā sūtīšana** — šī žetonu kombinācija norāda, ka attiecīgā veidne ir aktīva veidne sistēmas ģenerētiem e-pasta ziņojumiem, kas tiek nosūtīti automātiski.

Lai rediģētu veidni, izvēlieties rindu un veiciet izmaiņas veidnē.

> [!NOTE]
> Katram konkrētā e-pasta ziņojumu tipa adresātam ir noklusējuma veidne. Visas standarta Attract veidnes ir iesaistītas kā noklusējuma veidnes, līdz administrators izveido jaunu veidni konkrētajam e-pasta ziņojumu tipam un iestata to kā noklusējuma veidni.

## <a name="create-a-template"></a>Izveidot veidni

Lai izveidotu veidni, e-pasta veidņu bibliotēkas augšējā labajā stūrī atlasiet **+ jauna veidne**. Lai atlasītu e-pasta ziņojumu tipu, kuram paredzēts izveidot veidni, atlasiet saņēmēju, procesu un notikumu, attiecībā uz kuru ir jānosūta e-pasta ziņojums. Pēc tam atlasiet **Izveidot**.

Veidne tiek atvērta rediģēšanas skatā, un varat nosaukt veidni. Piemēram, ja veidne ir paredzēta kandidātiem no ASV universitātes, bet saturs ir rakstīts franču valodā, kā nosaukumu varat ievadīt **Universitāte\_ASV\_franču**. Jebkuras veidnes nosaukumā, tēmas rindā un pamattekstā papildus angļu valodai tiek atbalstītas arī citas valodas.

Veidnes lauku **Adresāts** nevar rediģēt, jo saņēmējs jau tika atlasīts, izveidojot veidni.

Kopijas (Cc) rindā var pievienot personas, piemēram, **Personāla atlases darbinieks** vai **Par pieņemšanu darbā atbildīgais vadītājs**. Kad e-pasta ziņojums tiek nosūtīts, šīs lomas tiek automātiski aizstātas ar atbilstošajiem lietotājiem, pamatojoties uz darba kontekstu.

Tēmas rinda un pamatteksts atbalsta vietturus. Vietturus var ievietot, ierakstot **\#** un pēc tam atlasot atbilstošu vietturi automātiskās pabeigšanas nolaižamajā sarakstā. Lapas labajā pusē tiek parādīts pieejamo vietturu saraksts. Kad e-pasta ziņojums tiek nosūtīts, vietturi tiek automātiski aizstāti, pamatojoties uz darba kontekstu un saņēmēju. Piemēram, tāda e-pasta veidne, kas tiek nosūtīts kandidātiem, satur vietturi \#{Candidate\_Name}. Nosūtot e-pasta ziņojumu kandidātam, kuru sauc Kamerons, vietturis tiks aizstāts ar vārdu Kamerons.

Pamatteksta redaktors ir bagātinātā teksta redaktors, kas ļauj mainīt teksta stilu un formātu. Tas arī ļauj ievietot hipersaites un enkurus.

Pēc veidnes izveidošanas konkrētam e-pasta ziņojumu tipam atlasiet daudzpunktes pogu (**...**) veidnes rindā un iestatiet to kā noklusējuma veidni.

## <a name="consume-templates"></a>Veidņu izmantošana

Kad darbā pieņemšanas grupa sūta e-pasta ziņojumu, tā var izmantot veidnes, kuras izveidojis administrators. Ja e-pasta ziņojumam, ko lietotājs sūta, ir izveidotas vairākas veidnes, e-pasta salikuma darbplūsmā parādās nolaižamais saraksts. Noklusējuma veidne tiek ievadīta automātiski, bet lietotājs var atlasīt citu veidni.

> [!NOTE] 
> E-pasta ziņojumiem, kas tiek nosūtīti automātiski, var izveidot vairākas veidnes. Tomēr tikai vienu veidni var iestatīt kā aktīvo veidni. Tā kā šo procesu aktivizē notikumi, tikai administrators var noteikt, kura veidne jāizmanto, balstoties uz žetonu **Noklusējums** un **Automātiskā sūtīšana** kombināciju veidņu bibliotēkā.

