---
title: ER Jaunināt savu formātu, pieņemot šī formāta jaunu bāzes versiju
description: Šajā tēmā skaidrots, kā uzturēt formāta konfigurāciju elektroniskajiem pārskatiem (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 336551f4e9858269010ec7debd1750a8d8453163
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564246"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a>ER Jaunināt savu formātu, pieņemot šī formāta jaunu bāzes versiju

[!include [banner](../../includes/banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var uzturēt formāta konfigurāciju Elektroniskajos pārskatos (ER). Šī procedūra skaidro kā var izveidot pielāgotu formātu versiju, balstoties uz formātu, kas saņemts no konfigurācijas sniedzēja (CP). Tas arī skaidro, kā pieņemt jaunu, šī formāta bāzes versiju.

Lai veiktu šīs darbības, vispirms jāveic darbības procedūrās "Izveidot konfigurācijas nodrošinātāju un iezīmēt to kā aktīvu" un "Izmantot izveidoto formātu, lai ģenerētu elektroniskos dokumentus maksājumiem". Šīs darbības var veikt uzņēmumā GBSI.

## <a name="select-format-configuration-for-customization"></a>Atlasiet formāta konfigurāciju pielāgošanai
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.

    Šajā piemērā parauga uzņēmums “Litware, Inc.” (https://www.litware.com) ir konfigurācijas nodrošinātājs, kas atbalsta formāta konfigurācijas elektroniskajiem maksājumiem attiecībā uz konkrētu valsti.    Parauga uzņēmums “Proseware, Inc.” (http://www.proseware.com) darbosies kā “Litware, Inc.” nodrošinātās formāta konfigurācijas patērētājs. Proseware, Inc. izmanto formātus noteiktos attiecīgās valsts reģionos.  
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
3. Noklikšķiniet uz Rādīt filtrus.
4. Lietojiet šādus filtrus: Ievadiet “BAKS (UK fiktīvs)” filtra vērtību laukā “Nosaukums”, izmantojot filtra operatoru “sākas ar”.
  
    Atlasītā BAKS (UK fiktīvs) formāta konfigurācija pieder nodrošinātājam Litware, Inc.  

5. Noklikšķiniet uz Rādīt filtrus.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

    Šo formāta versiju ar statusu Pabeigts uzņēmums Proseware, Inc. izmanto pielāgošanai.  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a>Izveidojiet jaunu konfigurāciju jūsu elektroniskā dokumenta pielāgotajam formātam
Proseware, Inc. saņēma BACS (UK fiktīvs) konfigurācijas versiju 1.1, kurā ietverts sākotnējais formāts elektronisko maksājumu dokumentu ģenerēšanai no Litware, Inc. saskaņā ar attiecīgo pakalpojuma abonementu. Proseware, Inc. vēlas sākt lietot šo metodi kā standartu savā valstī, tomēr ir nepieciešama pielāgošana, lai nodrošinātu atbalstu noteiktām reģionālajām prasībām. Proseware, Inc. arī vēlas saglabāt iespēju jaunināt pielāgotu formātu, tiklīdz Litware, Inc. piedāvā jaunu tā versiju (ar izmaiņām, kas nodrošina atbalstu jaunām valstij raksturīgām prasībām), kā arī vēlas veikt jaunināšanu ar pēc iespējas zemākām izmaksām.  

Lai to izdarītu, Proseware, Inc. ir jāizveido konfigurācija, kā bāzi izmantojot Litware, Inc konfigurāciju BACS (UK fiktīvs).  

1. Aizvērt lapu.
2. Atlasiet Proseware, Inc., lai to padarītu par aktīvu nodrošinātāju.
3. Noklikšķiniet uz Iestatīt aktīvu.
4. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
5. Kokā izvērsiet “Maksājumi (vienkāršotais modelis)”.
6. Kokā atlasiet 'Maksājumi (vienkāršotais modelis)\BAKS (UK fiktīvs)'.

    Atlasiet konfigurāciju BACS (UK fiktīvs) no Litware, Inc. Uzņēmums Proseware, Inc. izmantos versiju 1.1. kā pielāgotās versijas bāzi.  

7. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.

    Tas jums ļauj izveidot jaunu konfigurāciju pielāgotam maksājuma formātam.  

8. Jaunajā laukā, ievadiet 'Atvasināt no nosaukuma: BAKS (UK fiktīvs), Litware, Inc.'.

    Atlasiet opciju Atvasināt, lai apstiprinātu BAKS (UK fiktīvs) izmantošanu kā pamatu pielāgotas versijas veidošanai.  

9. Laukā Nosaukums ierakstiet 'BAKS (UK fiktīvs pielāgots)'.
10. Laukā Apraksts ierakstiet “BAKS kreditora maksājums (UK fiktīvs pielāgots)”.

    Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs (Proseware, Inc.). Šis nodrošinātājs varēs uzturēt šo konfigurāciju. Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.  

11. Klikšķiniet Izveidot konfigurāciju.

## <a name="customize-your-format-for-the-electronic-document"></a>Pielāgojiet jūsu elektroniskā dokumenta formātu
1. Noklikšķiniet uz Veidotājs.
2. Noklikšķiniet uz Izvērst/sakļaut.
3. Noklikšķiniet uz Izvērst/sakļaut.
4. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka”.
5. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
6. Kokā atlasiet "XML\Elements".
7. Laukā Nosaukums ierakstiet "IBAN".
8. Noklikšķiniet uz Labi.
9. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\IBAN”.
10. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
11. Kokā atlasiet elementu “Teksts\Virkne”.
12. Noklikšķiniet uz Labi.
13. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums\Virkne”.
14. Ievadiet '60' laukā Maksimālais garums.
15. Noklikšķiniet uz cilnes Kartēšana.
16. Koka struktūrā izvērsiet elementu “modelis”.
17. Kokā izvērsiet sadaļu “modelis\Maksājumi”.
18. Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.
19. Kokā izvērsiet elementu “modelis\Maksājumi\Kreditors\Konts“.
20. Koka struktūrā atlasiet zaru “modelis\Maksājumi\Kreditors\Konts\IBAN”.
21. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums = model.Payments\Kreditors\Banka\IBAN\Virkne”.
22. Noklikšķiniet uz Saistīt.
23. Noklikšķiniet uz Saglabāt.

## <a name="validate-the-customized-format"></a>Pārbaudiet pielāgoto formātu
1. Noklikšķiniet uz Pārbaudīt.

    Pārbaudiet pielāgotā formāta izkārtojumu un datu kartējuma izmaiņas, lai pārliecinātos, ka visi saistījumi ir pareizi.  

2. Aizvērt lapu.

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a>Mainīt pielāgotā formāta konfigurācijas pašreizējās versijas statusu
Izveidotās formāta konfigurācijas statusu no Melnraksts mainiet uz Pabeigts, lai to padarītu pieejamu maksājumu dokumenta ģenerēšanai.  

1. Noklikšķiniet uz Mainīt statusu.

    Ņemiet vērā, ka atlasītās konfigurācijas pašreizējai versijai ir statuss Melnraksts.  

2. Noklikšķiniet uz Pabeigt.
3. Apraksta laukā ierakstiet vērtību.
4. Noklikšķiniet uz OK.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

    Ņemiet vērā, ka izveidotā konfigurācija tiek saglabāta kā pabeigta versija 1.1.1. Tas nozīmē, ka tā ir 1. versija pielāgotajam formātam BAKS (UK fiktīvs pielāgots), kura ir balstīta uz formāta BAKS (UK fiktīvs) 1. versiju, kas ir balstīta uz datu modeļa Maksājumi (vienkāršots modelis) 1. versiju.  

## <a name="test-the-customized-format-to-generate-payment-files"></a>Pārbaudiet pielāgoto formātu, lai ģenerētu maksājuma failus
Paralēlā Finance and Operations sesijā izpildiet procedūrā "Lietot izveidoto formātu, lai ģenerētu elektroniskos dokumentus maksājumiem" norādītās darbības. Atlasiet BAKS (UK fiktīvs pielāgots) formātu elektronisko maksājumu metodes parametros. Pārliecinieties, ka izveidotais maksājuma fails satur nesen ieviesto XML mezglu ar IBAN kodu, saskaņā ar reģionālajām prasībām.  

## <a name="update-the-existing-country-specific-configuration"></a>Atjauniniet esošo valstij specifisko konfigurāciju
Uzņēmumam Litware, Inc. jāveic BACS (UK fiktīvs) konfigurācijas jaunināšana un jāievieš jaunās valstij raksturīgās prasības attiecībā uz elektroniskā dokumenta formāta pārvaldību. Vēlāk, tas tiks ietverts jaunā šīs konfigurācijas versijā, kas tiks piedāvāta pakalpojuma abonentiem, ieskaitot Proseware, Inc.  

Ar reālo pakalpojumu sniegšanu saistītajos procesos katra jauna BACS (UK fiktīvs) versija var tikt importēta uzņēmumā Proseware, Inc. no Litware, Inc. konfigurāciju LCS repozitorija. Šajā procedūrā mēs simulēsim to, atjauninot BAKS (UK fiktīvs) pakalpojuma sniedzēja vārdā.  

1. Aizvērt lapu.
2. Atlasiet pakalpojumu sniedzēju Litware, Inc.
3. Noklikšķiniet uz Iestatīt aktīvu.
4. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
5. Kokā izvērsiet “Maksājumi (vienkāršotais modelis)”.
6. Kokā atlasiet 'Maksājumi (vienkāršotais modelis)\BAKS (UK fiktīvs)'.

    Melnraksta versija BACS (UK fiktīvs), kas pieder Litware, Inc., tiek atlasīta, lai veiktu izmaiņas atbilstoši jaunajām valstij raksturīgajām prasībām.  

## <a name="localize-the-base-format-of-the-electronic-document"></a>Lokalizējiet elektroniskā dokumenta pamatformātu
Pieņemsim, ka pastāv jaunas valstij raksturīgās prasības, kuru atbalsts jānodrošina uzņēmumam Litware:  

- Vērtība, kas paredzēta kreditora bankas SWIFT kodam katrā maksājuma transakcijā.
- Ģenerēšanas failā pastāv 100 rakstzīmju ierobežojums kreditora nosaukuma teksta garumam.  
- Jaunas valstij specifiskas prasības  
- Atlasiet vēlamās konfigurācijas melnraksta versiju, lai ieviestu nepieciešamās izmaiņas.  


1. Noklikšķiniet uz Veidotājs.
2. Noklikšķiniet uz Izvērst/sakļaut.
3. Noklikšķiniet uz Izvērst/sakļaut.
4. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka”.
5. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
6. Kokā atlasiet "XML\Elements".
7. Laukā Nosaukums ierakstiet "SWIFT".
8. Noklikšķiniet uz Labi.
9. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\SWIFT”.
10. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
11. Kokā atlasiet elementu “Teksts\Virkne”.
12. Noklikšķiniet uz Labi.
13. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums\Virkne”.
14. Ievadiet '100' laukā Maksimālais garums.
15. Noklikšķiniet uz cilnes Kartēšana.
16. Koka struktūrā izvērsiet elementu “modelis”.
17. Kokā izvērsiet sadaļu “modelis\Maksājumi”.
18. Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.
19. Kokā izvērsiet elementu “modelis\Maksājumi\Kreditors\Aģents“.
20. Koka struktūrā atlasiet zaru “modelis\Maksājumi\Kreditors\Aģents\SWIFT”.
21. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums = model.Payments\Kreditors\Banka\SWIFT\Virkne”.
22. Noklikšķiniet uz Saistīt.
23. Noklikšķiniet uz Saglabāt.

## <a name="validate-the-localized-format"></a>Validēt lokalizēto formātu
1. Noklikšķiniet uz Pārbaudīt.
2. Aizvērt lapu.

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a>Pamatformāta konfigurācijas pašreizējās versijas statusa maiņa
Nomainiet atjauninātā pamatformāta konfigurācijas statusu no Melnraksts uz Pabeigts, lai to padarītu pieejamu maksājumu dokumentu ģenerēšanai, un formāts konfigurācijas atjauninājumiem, kas izriet no tās.  

1. Noklikšķiniet uz Mainīt statusu.

    Ņemiet vērā, ka atlasītās konfigurācijas pašreizējai versijai ir statuss Melnraksts.  

2. Noklikšķiniet uz Pabeigt.
3. Apraksta laukā ierakstiet vērtību.
4. Noklikšķiniet uz OK.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

## <a name="change-the-base-version-for-the-custom-format-configuration"></a>Mainiet bāzes versiju pielāgota formāta konfigurācijai

Proseware, Inc. tiek informēts, ka ir pieejama jauna BACS (UK fiktīvs) konfigurācijas versija 1.2 elektronisko maksājumu dokumentu ģenerēšanai saskaņā ar nesen izziņotajām valstij raksturīgajām prasībām. Proseware, Inc. vēlas sākt to izmantot kā standartu valstij.  

Lai to izdarītu, uzņēmumam Proseware, Inc. ir jāmaina pielāgotās konfigurācijas BACS (UK fiktīvs, pielāgots) bāzes konfigurācijas versiju. 1.1 BAKS (UK fiktīvs) versijas vietā, izmantojiet jauno 1.2 versiju.  

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Atlasiet nodrošinātāju Proseware, Inc., lai iestatītu to kā aktīvu.
3. Noklikšķiniet uz Iestatīt aktīvu.
4. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
5. Kokā izvērsiet “Maksājumi (vienkāršotais modelis)”.
6. Kokā izvērsiet 'Maksājumi (vienkāršotais modelis)\BAKS (UK fiktīvs)'.
7. Kokā atlasiet 'Maksājumi (vienkāršotais modelis)\BAKS (UK fiktīvs)\BAKS (UK fiktīvs pielāgots)'.

    Atlasiet BACS (UK fiktīvs pielāgots) konfigurāciju, kas pieder Proseware, Inc.  

    Izmantojiet atlasītās konfigurācijas melnraksta versiju, lai ieviestu nepieciešamās izmaiņas.  

8. Noklikšķiniet uz Pārskatīt.

    Atlasiet pamata konfigurācijas jauno 1.2 versiju, lai to lietotu kā jaunu bāzi konfigurācijas atjaunināšanai.  

9. Noklikšķiniet uz OK.

    Ņemiet vērā, ka tika atklāti daži konflikti starp pielāgotas versijas un jaunas bāzes versijas sapludināšanu, kas nozīmē formāta izmaiņas, kuras nevar sapludināt automātiski.  

## <a name="resolve-rebase-conflicts"></a>Atrisiniet pārskatījuma konfliktus
1. Noklikšķiniet uz Veidotājs.
    
    Ņemiet vērā, ka izmaiņas kreditora nosaukuma teksta garuma ierobežojumā nevar tik atrisinātas automātiski. Tāpēc tas ir norādīts konfliktu sarakstā. Katram konfliktam ar tipu Atjauninājums ir pieejamas šādas opcijas: - Lietot iepriekšējo bāzes vērtību (poga virs režģa), lai izmantotu iepriekšējo pamata versijas vērtību (mūsu gadījumā: 0).  - Piemērot bāzes vērtību (poga virs režģa), lai izmantotu jaunu pamata versijas vērtību (100 mūsu gadījumā).  - Paturiet savu (pielāgotu) vērtību (mūsu gadījumā tā ir 60).  Noklikšķiniet uz Lietot bāzes vērtību, lai pielietotu valstij raksturīgo 100 rakstzīmju limitu kreditora nosaukuma teksta garumam.  

    Ņemiet vēra, ka uzņēmumā Proseware, Inc. and Litware, Inc. tiek izmantotas pielāgotas un lokālas šī formāta versijas, izmantojot IBAN un SWIFT kodus ar saistītiem komponentiem, kas automātiski tiek apvienoti pārvaldības formātā.  

2. Noklikšķiniet uz Pievienot bāzes vērtību.

    Noklikšķiniet uz Lietot bāzes vērtību, lai pielietotu valstij raksturīgo 100 rakstzīmju limitu kreditora nosaukumiem.  

3. Noklikšķiniet uz Saglabāt.

    Saglabājot formātu, no konfliktu saraksta tiks noņemti atrisinātie konflikti.  

4. Aizvērt lapu.

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a>Pielāgotā formāta konfigurācijas pašreizējās versijas statusa maiņa
1. Noklikšķiniet uz Mainīt statusu.

    Mainiet atjaunināta, pielāgota formāta konfigurācijas statusu no Melnraksts uz Pabeigts. Tas šo formāta konfigurāciju padara pieejamu maksājumu dokumentu ģenerēšanai. Ņemiet vērā, ka atlasītās konfigurācijas pašreizējai versijai ir statuss Melnraksts.  

2. Noklikšķiniet uz Pabeigt.
3. Apraksta laukā ierakstiet vērtību.
4. Noklikšķiniet uz OK.

    Ņemiet vērā, ka izveidotās konfigurācija ir saglabāta kā pabeigta versija 1.2.2: bāzes BAKS (UK fiktīvs pielāgots) formāta versija 2, kas balstās uz bāzes BAKS (UK fiktīvs) formāta 2 versiju, kas balstās uz maksājumu (vienkāršots modelis) datu modeļa versiju 1.  

## <a name="test-the-customized-format-for-payment-files-generation"></a>Pārbaudiet pielāgoto formātu, lai ģenerētu maksājuma failus
Paralēlā Finance and Operations sesijā izpildiet procedūrā "Lietot izveidoto formātu, lai ģenerētu elektroniskos dokumentus maksājumiem" norādītās darbības. Atlasiet izveidoto 'BAKS (UK fiktīvs pielāgots)' formātu elektronisko maksājumu metodes parametros. Pārliecinieties, vai izveidotais maksājuma fails satur Proseware, Inc. nesen ieviesto XML mezglu ar IBAN konta kodu, saskaņā ar reģionālajām prasībām. Failam arī jāsatur Litware, Inc. nesen ieviestais XML mezgls SWIFT bankas koda uzrādīšanai saskaņā ar valsts prasībām.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]