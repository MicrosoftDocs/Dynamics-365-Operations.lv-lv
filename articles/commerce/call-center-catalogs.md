---
title: Zvanu centra katalogi
description: Šajā tēmā ir aprakstīta zvanu centram raksturīgā katalogu funkcionalitāte programmā Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 05/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 259b68aa28aa0c84699fc6d2e691bae0af135ab7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997804"
---
# <a name="call-center-catalogs"></a>Zvanu centra katalogi

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīta zvanu centram raksturīgā funkcionalitāte, kas ir saistīta ar katalogu iespējām programmā Dynamics 365 Commerce.

Programmā Commerce pieejamos katalogu līdzekļus var izmantot dažādiem nolūkiem. Sākotnēji katalogu līdzekļi tika izveidoti ar mērķi atbalstīt trešo pušu e-komercijas integrācijas. Katalogu iestatīšana uzņēmumiem ļāva izveidot preču un atribūtu grupējumus, kurus varēja publicēt ārēji, lai tos izmantotu ar trešās puses e-komercijas risinājumu.

Kad programmai tika pievienots zvanu centra kanāla atbalsts, kataloga jēdziens tika paplašināts, lai pievienotu papildu atbalsta un pārvaldības līdzekļus saistībā ar tradicionālajiem tieši uz patērētajiem orientētajiem mārketinga katalogiem. Uzņēmums, kas strādā tieši ar patērētājiem, bieži vien izveido drukātus katalogus, kuri pēc tam tiek nosūtīti vienam vai vairākiem klientu segmentiem. Šajos katalogos parasti ir noteikti veicināšanas pasākumi vai piedāvājumi, kas ir spēkā tikai tad, ja pasūtījuma izveidošanas laikā klients norāda kataloga identifikācijas kodu.

Tieši uz patērētāju vēstas mārketinga kampaņas ir ļoti koncentrētas uz izsekošanu, kāda ir reakcija uz šiem katalogiem, lai pārliecinātos, ka attaisnojas to ražošanas un sūtīšanas izmaksas. Lai izsekotu reakciju, kataloga aizmugurē parasti tiek drukāts kods, un pēc tam šis kods tiek pieprasīts un lietots, kad kataloga saņēmējs zvana, lai veiktu pasūtījumu pa tālruni (vai — tagad tas notiek biežāk — šo kodu var ievadīt, kad klients veic pasūtījumu tiešsaistē). Lai gan pastāv dažādi nozares termini, ar kuriem tiek apzīmēts šis kataloga izsekošanas kods (tostarp atslēgas kods, veicināšanas kods, kataloga kods, avota kods), programmā Commerce šis kods tiek saukts par **Avota koda ID**.

## <a name="basic-catalog-setup"></a>Pamata kataloga iestatīšana

Dodieties uz **Retail un Commerce** \> **Katalogi un preču klāsti** \> **Visi katalogi**, lai konfigurētu savu katalogu.

Kad veidojat jaunu katalogu, vispirms šis katalogs ir jāsaista ar vienu vai vairākiem kanāliem. Tas tiek darīts kopsavilkuma cilnē **Commerce kanāli**, kas atrodas formā **Kataloga iestatīšana**. Noklikšķiniet uz **Pievienot** un atlasiet vienu vai vairākus kanālus. Veidojot katalogu, var izmantot tikai vienumus, kas ir saistīti ar jūsu atlasītā kanāla [preču klāstiem](https://docs.microsoft.com/dynamics365/unified-operations/retail/assortments).

Lai katalogam pievienotu preces, ir jāizvēlas navigācijas hierarhija. Navigācijas hierarhija atbalsta attiecīgā kataloga kategoriju struktūru. Jums ir jāizvēlas viena no navigācijas hierarhijām, kas ir saistītas ar lapas **Katalogs** kopsavilkuma cilnē **Commerce kanāli** atlasītajiem mazumtirdzniecības kanāliem. Ja navigācijas kanāls iepriekš nebija saistīts ar kanālu, dodieties uz **Retail un Commerce** \> **Kanāla iestatīšana** \> **Kanālu kategorijas un preču īpašības**, lai navigācijas hierarhijas noklusējumu saistītu ar katru no jūsu mazumtirdzniecības kanāliem.

Izvēlnes cilnē **Katalogi**, lapā **Katalogu iestatīšana** noklikšķiniet uz **Pievienot preces**, lai konfigurētu katalogam pievienojamās preces, vai atlasiet zaru navigācijas hierarhijā (zara atlasīšana maina ekrāna izskatu un ļauj jums pievienot preces tieši kādai kategorijai attiecīgajā katalogā).

Noklikšķiniet uz kataloga hierarhijas augšējā līmeņa zara, lai atgrieztos galvenā kataloga virsrakstu skatā. Spēkā stāšanās un beigu datumus pēc nepieciešamības konfigurējiet kopsavilkuma cilnē **Vispārīgi**.

Lai katalogs kļūtu pieejams lietošanai, tas ir jāpublicē. Lai apstrādātu validēšanu, izvēlnē **Katalogi** noklikšķiniet uz **Validēt katalogu**. Šī darbība ir obligāta, un ar to tiek validēts, vai nepieciešamā iestatīšana ir pareiza. Lai apskatītu detalizētu informāciju par validēšanu, noklikšķiniet uz **Skatīt rezultātus**. Ja tiek konstatētas kļūdas, izlabojiet datus un izpildiet validēšanu vēlreiz, līdz validēšana ir sekmīga.

Kad validēšana ir apstiprināta, izvēlnē noklikšķiniet uz **Darbplūsma**, lai sāktu apstiprināšanas darbplūsmu. Lai izpildītu šo procesu, izvēlnē **Darbplūsma** noklikšķiniet uz **Iesniegt**. Konfigurējiet darbības un autorizējiet lietotājus darbplūsmai no sadaļas **Retail un Commerce** \> **Headquarters iestatīšana** \> **Mazumtirdzniecības darbplūsmas**. Darbplūsma definē darbības, kas ir nepieciešamas, lai katalogam iegūtu statusu **Apstiprināts**. Kad kataloga statuss ir **Apstiprināts**, izvēlnē **Katalogi** varat klikšķināt uz opcijas **Publicēt**, lai pabeigtu šo procesu. Kad kataloga statuss ir **Publicēts**, to var izmantot zvanu centra pasūtījumu izveides un katalogu sūtīšanas procesos.

## <a name="use-catalogs-to-drive-sales-order-pricing-and-promotions"></a>Katalogu izmantošana pārdošanas pasūtījumu cenu noteikšanas un veicināšanas pasākumu virzīšanai

Būtisks iemesls zvanu centrā izmantojamā kataloga definēšanai ir spēja šim katalogam konfigurēt noteiktas cenas un veicināšanas pasākumus. Klienti, kas kaut ko pasūta no šī kataloga, zvanu centra pasūtījuma izveidē saņem šīs cenas un veicināšanas pasākumus, ja pasūtījuma virsrakstam vai rindām tiek lietots kataloga **Avota koda ID**.

Lai konfigurētu katalogam raksturīgas cenas, cilnē **Katalogi** atlasiet opciju **Cenu grupas**, lai katalogam piesaistītu vienu vai vairākas cenu grupas. Kad klienti veic pasūtījumus no šī kataloga, tiek izmantoti visi ar to pašu cenu grupu saistītie tirdzniecības līgumi, cenu korekciju žurnāli un detalizētās (sliekšņa, daudzuma, komplekta) atlaides.

Kopsavilkuma cilnē **Avota kodi** noklikšķiniet uz **Pievienot**, lai šim katalogam pievienotu vienu vai vairākus **Avota koda ID** identifikatorus. Šis ir kods, kas zvanu centra pasūtījuma izveides laikā tiek lietots pārdošanas pasūtījuma virsrakstā (un rindās). Šis kods tiek izmantots, lai pārdošanas pasūtījumu saistītu ar katalogu un visbeidzot ar cenu grupām, kā arī visām konfigurētajām īpašajām cenām un veicināšanas pasākumiem.

## <a name="use-the-source-id-to-track-costs-and-response-rates"></a>Avota ID izmantošana, lai izsekotu izmaksu un reakciju koeficientus

Kad definējat identifikatoru **Avota koda ID**, ja vēlaties, šo ID varat saistīt ar identifikatoru **Mērķa tirgus ID**. Identifikatoru **Mērķa tirgus ID** var definēt sadaļā **Retail un Commerce** \> **Klienti** \> **Mērķa tirgus**. Mērķa tirgus ir saraksts ar klientiem un/vai potenciālajiem klientiem, kuri pieder lietotāja definētam segmentam. Klienta vai potenciālā klienta datu saistīšana ar avota koda ID ļauj uzlabotu pārskatāmību par kataloga saņēmējiem. Ja klients ir saistīts ar kādu mērķa tirgu un šis mērķa tirgus ir saistīts ar aktīvu avota koda ID/katalogu, zvanu centra lietotāji var redzēt, kādus katalogus klients ir saņēmis, lapas **Klientu apkalpošana** izvēlnes cilnē **Klienti** atlasot izvēlnes opciju **Avota kodi**. Pasūtījuma izveides laikā pārdošanas pasūtījuma virsraksta nolaižamajā sarakstā **Avots** zvanu centra lietotāji var redzēt arī konkrētos katalogus, kas klientam tika nosūtīti. Filtru no **Visi** mainot uz **Mērķēts**, lietotājs var redzēt konkrētos aktīvos katalogus, kas klientam tika nosūtīti. Tas ir noderīgi gadījumos, kad klients var būt aizmirsis savu katalogu vai nevar atrast vai nolasīt kataloga kodu, kad zvana, lai izveidotu pārdošanas pasūtījumu.

Ar vienu katalogu var saistīt vairākus avota koda ID. Tas bieži ir nepieciešams, ja uzņēmums vēlas izsekot reakcijas koeficientu pēc dažādiem segmentiem. Uzņēmums piešķir unikālu kataloga kodu dažādiem klientu segmentiem, tādējādi noteiktā kataloga notikumā ļaujot izsekot reakcijas koeficientu līdz segmenta līmenim.

Kopsavilkuma cilnē **Avota kodi** atlasot konkrētu ierakstu **Avota koda ID** un noklikšķinot uz opcijas **Detalizēta informācija**, tiek nodrošināti papildu lauki, kur var ierakstīt pārdošanas projekcijas, sūtīšanas izmaksas un sūtīšanas datumus. Šie dati ir noderīgi detalizētas analīzes veikšanai par kataloga efektivitāti. Lietotāji laika gaitā var atgriezties šajā lapā un izmantot pogu **Avota koda analīze** un pogu **Salīdzināt veicināšanas pasākumus**, lai aktivizētu analītisku pārskatu izveidi, pamatojoties uz pašreizējiem pārdošanas datiem, un izmaksas un budžetu salīdzinātu ar faktiskajām vērtībām.

## <a name="configure-catalog-specific-order-and-item-scripts"></a>Katalogam raksturīgo pasūtījumu un krājumu skriptu konfigurēšana

Kad zvanu centra lietotājs veido pārdošanas pasūtījumu, viņi var izmantot ekrānā rādītus skriptus. Šie teksta skripti var nodrošināt papildinformāciju, kas lietotājam būtu jāsaka klientam, vai tie varētu būt iekšējās piezīmes/atgādinājumi, kas zvanu centra lietotājam būtu jāpārskata un uz ko viņam būtu jāreaģē, veidojot pārdošanas pasūtījumu.

Bieži vien ir noderīgi dažādiem katalogiem izmantot dažādas skriptu kopas. Kopsavilkuma cilnē **Skripti** iepriekš definētus skriptus var saistīt ar katalogu. Izmantojiet lauku **Hronometrāža**, lai noteiktu, vai skripts ir jāparāda pasūtījuma sākumā (līdzko pasūtījuma virsrakstā ir ievadīts avota kods ID) vai pasūtījuma beigās (pārdošanas pasūtījuma kopsavilkuma formā).

Atlasot zaru kataloga hierarhijā un strādājot ar datiem kopsavilkuma cilnē **Preces**, lietotāji var arī piesaistīt katalogiem vai krājumiem raksturīgus skriptus, izmantojot darbību **Skripti**.

## <a name="configure-catalog-specific-up-sell-and-cross-sell-items"></a>Katalogam raksturīgu papildu pārdošanas un šķērspārdošanas krājumu konfigurēšana

Papildu pārdošanas/šķērspārdošanas ieteikumu piesaistīšanu krājumam var veikt no preču iestatīšanas, bet reizēm uzņēmums var vēlēties veicināt īpašus papildu pārdošanas/šķērspārdošanas krājumus klientiem, kas pasūta noteiktu preci no noteikta kataloga. Kopsavilkuma cilnē **Preces** atlasiet kādu krājumu un noklikšķiniet uz **Papildu pārdošanas/šķērspārdošanas krājumi**, lai konfigurētu preces, kurām veikt papildu pārdošanu vai šķērspārdošanu tādiem klientiem, kas iegādājās atlasīto krājumu no šī kataloga. Zvanu centra pasūtījuma izveides laikā ekrānā ir redzami katalogam raksturīgie papildu pārdošanas/šķērspārdošanas krājumi, nevis standarta papildu pārdošanas/šķērspārdošanas produkti, kas var būt konfigurēti šim krājumam, izmantojot parasto preču konfigurāciju.

Papildu pārdošanas/šķērspārdošanas krājumiem var izmantot arī skriptu līdzekļus, lai rādītu noteiktus paziņojumus, ko lietotājs redz, kad pasūtījuma izveides laikā tiek rādīts papildu pārdošanas/šķērspārdošanas krājums. Skripti, kas ir piesaistīti papildu pārdošanas/šķērspārdošanas precēm, kuras ir konfigurētas noteiktai kataloga precei, tiek parādīti tikai tad, kad zvanu centra pasūtījuma izveides laikā tiek lietots kataloga avota kods.

## <a name="catalog-page-analysis"></a>Kataloga lapas analīze

Cilnē **Katalogi** ir pieejamas opcijas, lai konfigurētu **Kataloga lapas**. Šis līdzeklis ļauj jums definēt īpašas lapas un lapu tipus drukātajam katalogam un ar to saistītajām izmaksām.

Konfigurējot katalogā ietvertās preces, izmantojiet darbību **Preču lapas izkārtojums**, lai krājumam definētu noteiktās lapas, lapas procentuālo daudzumu un lapas detalizētās informācijas pozīciju. Šo datu konfigurēšana ļauj lietotājiem izmantot pārskatu **Kataloga zonas analīzes pārskats**. Šis pārskats ir atrodams, pārejot uz **Retail un Commerce** \> **Zvanu centra pārskati** \> **Kataloga zonas analīzes pārskats**. Šajā pārskatā tiek analizēta katalogam veiktā pārdošana (pārdošanas pasūtījumi, kur ar pasūtījuma virsrakstu vai rindu ir saistīts attiecīgā kataloga avota ID) un ar to saistītais lapas procentuālais daudzums un izmaksas, iegūstot tradicionālā tiešā mārketinga pārskatu **Kvadrātcollu analīze**.

## <a name="catalog-requests"></a>Kataloga pieprasījumi

Kad programmā Commerce ir konfigurēti un publicēti katalogi, var izmantot līdzekli **Sūtīt katalogu**. Šis līdzeklis ir pieejams lapā **Klientu meklēšana** un lapā **Klientu apkalpošana**. Pēc klienta ieraksta atlasīšanas, izmantojot lapu **Klientu meklēšana** vai skatot atlasītā klienta kontu no lapas **Klientu apkalpošana**, lietotāji var atlasīt opciju **Sūtīt katalogu**, kas atver dialoglodziņu, ļaujot lietotājam izvēlēties no visu publicēto un aktīvo katalogu saraksta. Lietotājs var atlasīt sūtīšanai katalogu un daudzumu, kā arī konkrētu avota koda ID. Pēc noklikšķināšanas uz pogas **Sūtīt** tiek saglabāts pieprasījums, kuru pēc tam var pārvaldīt, izdrukājot pārskatu **Kataloga pieprasījumi**. Šis pārskats ir atrodams, pārejot uz **Retail un Commerce** \> **Zvanu centra pārskati** \> **Kataloga pieprasījumu pārskats**. Tajā ir uzskaitīti visi kataloga pieprasījumi, tostarp informācija par klienta vārdu un adresi tam klientam, kurš šo katalogu pieprasīja. Šo pārskatu var izmantot iekšēji vai datus var pārsūtīt trešajai pusei, kas atbalsta ārējās procedūras fiziskai kataloga nosūtīšanai klientam.

## <a name="additional-features"></a>Papildu līdzekļi

Cilnē **Katalogi** ir pieejamas arī opcijas vērtību **Maksājumu grafiks** un **Bezmaksas preces** konfigurēšanai. Ja zvanu centra pasūtījuma izveides laikā tiek lietots ar katalogu saistīts avota koda ID, klientam ir tiesības saņemt bezmaksas preces vai izmantot noteiktā kataloga maksājumu grafikus definētajā veidā. Ja ir nepieciešams klientam noteikt ierobežojumus, lai klients varētu atlasīt tikai no savam katalogam piesaistītajiem maksājumu grafikiem, nevis no visiem sistēmā esošajiem aktīvajiem maksājumu grafikiem,var atzīmēt izvēles rūtiņu **Atļaut tikai kataloga plānus** vienam vai vairākiem definētajiem avota koda ID, lai liktu ievērot šo ierobežojumu.

## <a name="additional-notes"></a>Papildu piezīmes

Pašlaik, ja pārdošanas pasūtījumam zvanu centrā tiek lietots kāds avota koda ID, tas tiek izmantots, lai vadītu katalogam raksturīgās cenas, veicināšanas pasākumus, skriptus un papildu pārdošanas/šķērspārdošanas. Sistēma neaizliedz un nenovērš iespēju pārdošanas pasūtījumā pasūtīt preci, kas nav ietverta katalogā. Ja tiek pasūtīts kāds krājums, kas neietilpst katalogā, sistēma vispirms izmanto vērtību **Cenu grupa**, kas krājuma cenai vai veicināšanas pasākumiem ir definēta attiecīgajā zvanu centra kanālā (**Retail un Commerce** \> **Kanāli** \> **Zvanu centri** \> **Visi zvanu centri**). Ja netiek atrasta neviena raksturīgā kanāla cena, šim krājumam tiek izmantota pārdošanas pamatcena.
