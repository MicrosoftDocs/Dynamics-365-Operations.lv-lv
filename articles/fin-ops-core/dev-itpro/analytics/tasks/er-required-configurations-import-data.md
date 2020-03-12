---
title: ER Izveidot nepieciešamās konfigurācijas, lai importētu datus no ārēja faila
description: Tālāk sniegtajā darbību aprakstā ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izstrādāt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurācijas, lai importētu datus lietojumprogrammā Microsoft Dynamics 365 Finance no ārēja faila.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48a327fc5033a7478d2ae5e401ffdce6e4546ad0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042877"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>ER Izveidot nepieciešamās konfigurācijas, lai importētu datus no ārēja faila

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tālāk sniegtajā darbību aprakstā ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izstrādāt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurācijas, lai importētu datus lietojumprogrammā no ārēja faila. Šajā piemērā jūs izveidosiet nepieciešamās ER konfigurācijas konfigurācijas parauga uzņēmumam Litware, Inc. Lai izpildītu šīs darbības, vispirms ir jāizpilda uzdevuma ceļvedī “ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu” aprakstītās darbības. Šīs darbības var veikt, izmantojot USMF datu kopu. Ir nepieciešams arī lejupielādēt un lokāli saglabāt failus, kuri norādīti tālāk tēmā Elektronisko atskaišu veidošanas pārskats (https://go.microsoft.com/fwlink/?linkid=852550): 1099model.xml, 1099format.xml, 1099entries.xml, 1099entries.xlsx.

ER biznesa lietotājiem sniedz iespēju konfigurēt procesu, kādā ārējo datu faili tabulās tiek importēti formātā .XML vai formātā .TXT. Vispirms ir jāizveido abstrakts datu modelis un ER datu modeļa konfigurācija, kas pārstāv importējamos datus. Pēc tam ir jādefinē importējamā faila struktūra un metode, ko izmantosiet, lai datus no faila pārnestu uz abstrakto datu modeli. Abstraktajam datu modelim ir jāizveido ER formāta konfigurācija, kas kartē uz izveidoto datu modeli. Pēc tam datu modeļa konfigurācija ir jāpaplašina ar kartējumu, kas apraksta veidu, kādā importētie dati tiek saglabāti kā abstrakta datu modeļa dati un kā tie tiek lietoti, lai atjauninātu tabulas .  ER datu modeļa konfigurācijai ir jāpievieno jauns modeļa kartējums, kas apraksta datu modeļa saistījumu ar programmas galamērķiem.  

Nākamajā scenārijā ir parādītas ER datu importēšanas iespējas. Tostarp ietilpst kreditoru transakcijas, kas tiek izsekotas ārēji un pēc tam importētas, lai vēlāk tās iekļautu 1099 pārskatos par kreditora nosegšanu.   

## <a name="add-a-new-er-model-configuration"></a>Pievienot jaunu ER modeļa konfigurāciju
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.

    Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.   

2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.

    Tā vietā, lai veidotu jaunu modeli, kas atbalsta datu importēšanu, varat ielādēt iepriekš lejupielādēto failu 1099model.xml. Šajā failā ir kreditoru transakciju pielāgotais datu modelis. Šis datu modelis ir kartēts uz datu komponentiem, kas atrodas AOT datu elementā.   

3. Noklikšķiniet uz Mainīt.
4. Noklikšķiniet uz Ielādēt no XML faila.

    Noklikšķiniet uz Pārlūkot un dodieties uz iepriekš lejupielādēto failu 1099model.xml.  

5. Noklikšķiniet uz OK.
6. Koka struktūrā atlasiet zaru “1099 Maksājumu modelis”.

## <a name="review-data-model-settings"></a>Pārskatīt datu modeļa iestatījumus
1. Noklikšķiniet uz Veidotājs.

    Šis modelis ir izveidots, lai pārstāvētu kreditora transakcijas no biznesa skatu punkta, un tas neietilpst implementācijā.   

2. Kokā struktūrā izvērsiet zaru “1099-MISC”.
3. Koka struktūrā atlasiet zaru “1099-MISC\Transakcijas”.
4. Koka struktūrā izvērsiet zaru “1099-MISC\Transakcijas”.

    Šī modeļa elements Transakcijas pārstāv atsevišķas transakcijas. Pakārtotie elementi tiek izmantoti, lai katrai transakcijai norādītu nepieciešamo informāciju, piemēram, kreditora kontu un transakcijas datumu.   

5. Aizvērt lapu.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Pievienot jaunu ER formāta konfigurāciju, kas atbalsta datu importēšanu
Ar šajā apakšuzdevumā iekļautajām darbībām jums tiek parādīts, kā var izveidot jaunu formāta konfigurāciju, lai pārvaldītu datu importēšanu no ārējiem failiem.   
1. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Jauns ievadiet “Uz datu modeli 1099 Maksājumu modelis balstīts formāts”.
3. Laukā Atbalsta datu importēšanu atlasiet vērtību Jā.
4. Nospiediet taustiņu ESC, lai aizvērtu šo lapu.

    Tā vietā, lai veidotu jaunu formātu, kas atbalsta datu importēšanu, varat ielādēt iepriekš lejupielādēto failu 1099format.xml. Šajā failā ir importējamā faila definētā struktūra un struktūras kartējums uz kreditoru transakciju pielāgoto datu modeli.   
5. Noklikšķiniet uz Mainīt.
6. Noklikšķiniet uz Ielādēt no XML faila.
    Noklikšķiniet uz Pārlūkot un dodieties uz iepriekš lejupielādēto failu 1099format.xml.  
7. Noklikšķiniet uz OK.
8. Koka struktūrā izvērsiet zaru “1099 Maksājumu modelis”.
9. Koka struktūrā atlasiet zaru “1099 Maksājumu modelis\Formāts kreditoru transakciju importēšanai”.

## <a name="review-format-settings"></a>Pārskatīt formāta iestatījumus
1. Noklikšķiniet uz Veidotājs.
2. Ieslēdziet opciju “Rādīt detalizēti”.
3. Noklikšķiniet uz Izvērst/sakļaut.
4. Noklikšķiniet uz Izvērst/sakļaut.

    Izveidotais formāts pārstāv paredzamo ārējā faila struktūru. Šim failam ir jābūt formātā XML, un tam ir nepieciešams nosegšanas saknes elements. Katra kreditora transakcija tiek attēlota ar transakcijas elementu, kas ir definēts ar kardinalitāti “nulle pret daudziem”. Tas nozīmē, ka ienākošajā failā esošo transakciju skaits var būt no nulles līdz vairākām transakcijām. Šāda “transakcijas” elementa ligzdotie elementi pārstāv vienas transakcijas atribūtus. Ņemiet vērā, ka visi atribūti, izņemot valsti, ir atzīmēti kā obligāti; tas nozīmē, ka tiem ir jābūt importējamajā failā.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>Pārskatīt iestatījumus formāta kartējumam uz datu modeli
1. Noklikšķiniet uz Kartēt formātu uz modeli.

    Kartējums “Kreditoru transakciju importēšanai” satur datu pārsūtīšanas kārtulas no ienākošā XML faila uz atlasīto daļu pielāgotajam datu modelim, kurš tiek definēts, atlasot the1099-MISC definīciju.  

2. Noklikšķiniet uz Veidotājs.
3. Ieslēdziet opciju “Rādīt detalizēti”.
4. Koka struktūrā izvērsiet zaru “formāts: Ieraksts”.
5. Koka struktūrā atlasiet zaru “formāts: Ieraksts”.

    Ņemiet vērā, ka izveidotais formāts šeit tiek radīts kā datu avota komponents.  

6. Koka struktūrā izvērsiet 'format: Record\*settlement: XML Element 1..1 (settlement): Record'.
7. Koka struktūrā izvērsiet 'format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list'.
8. Koka struktūrā izvērsiet 'format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record'.
9. Koka struktūrā izvērsiet 'format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record'.
10. Koka struktūrā atlasiet 'format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record'.

    Ņemiet vērā, ka sākotnēji definētajā “formāta” datu avota komponentā obligāto un neobligāto formāta elementu rādīšana atšķiras.  
11. Koka struktūrā izvērsiet zaru “Transakcijas: Ierakstu saraksts = format.settlement.'$enumerated'”.

    Ņemiet vērā, ka elementi formātā, kas definē importētā faila struktūru, ir saistīti ar pielāgotā datu modeļa elementiem. Atkarībā no šīm saistībām importētā XML faila saturs izpildlaikā tiks saglabāts esošajā datu modelī. Pievērsiet uzmanību valsts elementa saistījumam. Ienākošajos failos, kam nav šāda elementa, datu modelī visiem transakcijas elementiem valsts kods pēc noklusējuma tiks aizpildīts kā “ASV”.  

12. Noklikšķiniet uz cilnes Validācijas.

    Šajā formāta kartējumā var būt lietotāja definēta loģika validēt importēto datu precizitāti no biznesa skatu punkta. Piemēram, pamatojoties uz šo iestatījumu, jebkurai importējamajā failā ietvertajai transakcijai, kam nav definēts valsts kods, informācijas žurnālā tiek ģenerēts brīdinājuma ziņojums, kas lietotāju informē par šo gadījumu un norāda transakcijas kārtas numuru.  

13. Aizvērt lapu.

## <a name="run-the-format-mapping-to-the-data-model"></a>Palaist formāta kartējumu uz datu modeli
Testēšanas nolūkos izpildiet šo formāta kartēšanu. Lietojiet iepriekš lejupielādēto failu 1099entries.xml. Šo failu varat eksportēt no darbgrāmatas 1099entries.xlsx, kas tiek lietota, lai pārvaldītu kreditora transakcijas. Ģenerētā izvade tiks importēta no atlasītā XML faila un reālajā importēšanā aizpildīs pielāgoto datu modeli.  

1. Noklikšķiniet uz Palaist.

    Noklikšķiniet uz Pārlūkot un dodieties uz iepriekš lejupielādēto failu 1099entries.xml.  

2. Noklikšķiniet uz OK.

    Ievērojiet brīdinājuma ziņojumu par trūkstošo valsts kodu attiecībā uz importētajā failā iekļauto transakciju.  
    
    Pārskatiet izvadi formātā XML, kas parāda no atlasītā faila importētos un uz datu modeli pārnestos datus.   

3. Aizvērt lapu.
4. Aizvērt lapu.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>Pārskatīt iestatījumus modeļu kartējumam uz mērķiem
1. Koka struktūrā atlasiet zaru “1099 Maksājumu modelis”.
2. Noklikšķiniet uz Veidotājs.
3. Noklikšķiniet uz Kartēšanas modelis datu avotam.

    Kartējums 1099 manuālai transakciju importēšanai ir definēts ar virziena tipu Uz galamērķi. Tas nozīmē, ka tas ir ievadīts, lai atbalstītu datu importēšanu, un ietver kārtulu iestatījumu par to, ka importētais ārējais fails un abstrakta datu modeļa dati tiek lietoti, lai atjauninātu tabulas programmā.  

4. Noklikšķiniet uz Veidotājs.
5. Koka struktūrā izvērsiet zaru “modelis: Datu modelis 1099 Maksājumu modelis“.
6. Koka struktūrā izvērsiet zaru “modelis: Datu modelis 1099 Maksājumu modelis\Transakcijas: Ierakstu saraksts”.

    Ņemiet vērā, ka izveidotais modelis šeit tiek radīts kā datu avota elements. Izpildlaikā tas ietvers datus, kas tiek importēti no ārējā faila. Kā datu avota elementi tika pievienotas vairākas tabulas, lai pārliecinātos, ka importētie dati atbilst pašreizējās programmas datiem, tostarp pārliecinātos, ka importētās transakcijas kreditora konts ir pieejamas sistēmā, ka pastāv importējamās valsts un novada kodu kombinācija un citi faktori.  

7. Koka struktūrā atlasiet 'model: Data model 1099 Payments model\Transactions: Record list\$failed: Calculated field = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean'.
8. Noklikšķiniet uz Rediģēt.
9. Noklikšķiniet uz Rediģēt formulu.

    Ja kādai importētajai transakcijai vismaz viena validācija ir nesekmīga, tad datu avota atribūts “$failed” šo transakciju atzīmēs kā nesekmīgu.  

10. Aizvērt lapu.
11. Noklikšķiniet uz Atcelt.
12. Koka struktūrā atlasiet zaru “tax1099trans: Tabula 'VendSettlementTax1099' ieraksti = model.Validated”.
13. Noklikšķiniet uz Rediģēt mērķi.

    Šis ER galamērķis tika pievienots, lai norādītu, kā importētie dati atjauninās programmas tabulas. Šajā gadījumā ir atlasīta datu tabula VendSettlementTax1099. Tā kā ir atlasīta ieraksta darbība Ievietot, tad importētas transakcijas tiks ievietotas tabulā VendSettlementTax1099. Ņemiet vērā, ka vienā modeļa kartējumā var būt vairāki galamērķi. Tas nozīmē, ka importētie dati var tikt lietoti, lai atjauninātu vairākas programmas tabulas vienlaicīgi. Kā ER galamērķus var lietot tabulas, skatus un datu elementus.   

    Ja kartējums tiks izsaukts no kāda punkta programmā (piemēram, no pogas vai izvēlnes vienuma), kurš tika īpaši veidots šādai darbībai, tad ER galamērķis ir jāatzīmē kā integrācijas punkts. Šajā piemērā tas ir punkts ERTableDestination#VendSettlementTax1099.  

14. Noklikšķiniet uz Atcelt.
15. Noklikšķiniet uz Rādīt visus.
16. Noklikšķiniet uz Rādīt tikai kartētos.
17. Koka struktūrā izvērsiet zaru “tax1099trans: Tabula 'VendSettlementTax1099' ieraksti = model.Validated”.

    Ņemiet vērā, ka datu avota elements, kas satur vienīgās validētas transakcijas, ir piesaistīts izveidotajam galamērķim. Importētās transakcijas varat filtrēt, lai izlaistu transakcijas, kuras nav saderīgas ar programmas datiem.  

18. Koka struktūrā atlasiet zaru “nesekmīgs: Tabula 'VendSettlementTax1099Entity' ieraksti = model.Failed”.
19. Noklikšķiniet uz cilnes Validācijas.

    Šajā modeļa kartējumā var būt lietotāja definēta loģika validēt importēto datu pareizību no esošajiem programmas datiem. Piemēram, pamatojoties uz pašreizējo iestatījumu, jebkurai importētajā failā ietvertajai transakcijai, kuras kreditora konta sistēmā nav, tiek ģenerēts brīdinājuma ziņojums, kas lietotāju informē un norāda nepareizo kreditora konta kodu.  

    Ņemiet vērā, ka opciju Pēcvalidācijas darbība var izmantot katrai validēšanai, lai norādītu, vai importēšanas process ir jāturpina vai jāaptur, kā arī, vai jau veiktie ievietojumi/atjauninājumi ir jāpatur vai jāatsauc.  

20. Noklikšķiniet uz Rādīt tikai kartētos.
21. Noklikšķiniet uz Rādīt visus.
22. Aizvērt lapu.

    Izpildiet šo modeļa kartējumu, lai pārbaudītu izveidoto formātu un modeļa kartējumus. Lietojiet failu 1099entries.xml. Dati no atlasītā faila tiks importēti sistēmā.  

23. Noklikšķiniet uz Palaist.

    Ņemiet vērā, ka dialoglodziņā nav papildu jautājumu par formātu kartējumu, kas ir jāizmanto, lai parsētu importēto failu un pēc tam datus pārnestu uz datu modeli. Tas ir tāpēc, ka pašlaik ir tikai viens formāts, kas lieto šo modeli, kurš ir atzīmēts kā izveidots ar mērķi atbalstīt datu importēšanu.  
    
    Definējiet dokumenta ID, lai importētās transakcijas atšķirtu no citām transakcijām, kuras jau varētu būt ievadītas manuāli vai importētas.  

24. Laukā Ievadīt dokumenta ID ierakstiet “IMPORT-001”.

    Pārlūkojiet uz failu “1099entries.xml”.  

25. Noklikšķiniet uz OK.

    Ģenerēto brīdinājumu saraksts sniedz informāciju par nepareiziem kreditoru kontiem, nepareizu nodokļu 1099 lodziņa kodu, trūkstošiem valstu kodiem un citām kļūdām. Šo brīdinājumu sarakstu salīdziniet ar saturu, kas ir iekļauts izpildes XML failā.  

26. Aizvērt lapu.
27. Aizvērt lapu.
28. Aizvērt lapu.
29. Aizvērt lapu.
30. Dodieties uz Parādi kreditoriem > Periodiskie uzdevumi > Nodokļi 1099 > Kreditora nodokļa 1099 nosegšana.

    Šajā veidlapā tiek rādītas kumulatīvās transakcijas tabulā Tax1099Summary, kas ir izveidotas, pamatojoties uz importētajām transakcijām.  

31. Laukā No datuma iestatiet datumu 2000-01-01.
32. Noklikšķiniet uz Manuālas 1099 transakcijas.

    Šajā veidlapā ir saraksts ar transakcijām, kas tika pievienotas manuāli, kā arī transakcijām, kuras mēs tikko importējām.  

33. Atveriet kolonnas filtru Dokuments.
34. Laukā “Kreditors” ievadiet filtra vērtību “IMPORT-001”, izmantojot filtra operatoru “sākas ar”.

## <a name="review-the-relationship-between-model-and-format-mappings"></a>Pārskatīt attiecības starp modeļu un formāta kartējumiem
1. Aizvērt lapu.
2. Aizvērt lapu.
3. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
4. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
5. Koka struktūrā atlasiet zaru “1099 Maksājumu modelis”.

    Pieņemsim, ka vēlaties atbalstīt to pašu datu importēšanu, bet no .TXT formāta faila.   

6. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu dialoglodziņu. 
7. Laukā Jauns ievadiet “Uz datu modeli 1099 Maksājumu modelis balstīts formāts”.
8. Laukā Nosaukums ierakstiet “Importēt datus no TXT faila”.
9. Laukā Atbalsta datu importēšanu atlasiet vērtību Jā.
10. Klikšķiniet Izveidot konfigurāciju.
11. Noklikšķiniet uz Veidotājs.
12. Noklikšķiniet uz Kartēt formātu uz modeli.
13. Noklikšķiniet uz Jauns.
14. Laukā Definīcija ievadiet vai atlasiet kādu vērtību.

    Atlasiet opciju “1099-MISC”.  

15. Laukā Nosaukums ierakstiet “Importēt datus no TXT faila”.
16. Laukā Apraksts ierakstiet “Importēt datus no TXT faila”.
17. Noklikšķiniet uz Saglabāt.
18. Aizvērt lapu.
19. Aizvērt lapu.
20. Noklikšķiniet uz Rediģēt.

    Ja ir instalēts labojumfails “KB 4012871 GER modeļu kartējumu atbalsts atdalītās konfigurācijās ar iespēju norādīt atšķirīgus priekšnosacījumu veidus to izvietošanai dažādās programmas Dynamics 365 Finance” (https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 ), izpildiet nākamo darbību “Karodziņa Noklusējums modeļu kartēšanai ieslēgšana” ar ievadīto formāta konfigurāciju. Pretējā gadījumā izlaidiet nākamo darbību.  

21. Modeļa kartējuma noklusējums atlasiet vērtību Jā.
22. Koka struktūrā atlasiet zaru “1099 Maksājumu modelis”.
23. Noklikšķiniet uz Veidotājs.
24. Noklikšķiniet uz Kartēšanas modelis datu avotam.
25. Noklikšķiniet uz Palaist.

    Ja ir instalēts labojumfails “KB 4012871 GER modeļu kartējumu atbalsts atdalītās konfigurācijās ar iespēju norādīt atšķirīgus priekšnosacījumus to izvietošanai dažādās versijās” (https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 ), atlasiet vēlamo modeļu kartējumu uzmeklēšanas laukā. Ja labojumfails vēl nav instalēts, pārejiet uz nākamo darbību, jo kartējums jau ir atlasīts ar noklusējuma formāta konfigurācijas definīciju.  
    
    Ja labojumfails KB 4012871 nav instalēts, tad ņemiet vēra, ka dialoglodziņā ir iekļauts papildu modeļu kartējuma jautājums, kurš tiek izmantots, lai parsētu importējamo failu. Pēc tam dati tiek pārnesti no dialoglodziņa uz datu modeli. Pašlaik varat izvēlēties, kurš formāta kartējums ir jāizmanto atkarībā no importējamā faila tipa.  
    
    Ja šo modeļu kartējumu plānojat izsaukt no kāda punkta programmā, kurš ir īpaši izveidots šai darbībai, tad ER galamērķis un formātu kartējums ir jāatzīmē kā daļa no integrācijas.  

26. Noklikšķiniet uz Atcelt.
27. Aizvērt lapu.
28. Aizvērt lapu.

