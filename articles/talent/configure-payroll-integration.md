---
title: Algu aprēķina integrācijas konfigurēšana pakalpojumos Talent un Dayforce
description: Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 for Talent un Ceridian Dayforce integrāciju, lai varētu apstrādāt maksājuma izpildi.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 204e4554e409c39fbbf7b273ad138ce2809931a8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/26/2019
ms.locfileid: "898448"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a>Talent un Dayforce algu aprēķina integrācijas konfigurēšana

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 for Talent un Ceridian Dayforce integrācijai tiek izmantotas vairākas konfigurācijas darbības, kas ir aprakstītas šajā tēmā. Pirms maksājuma izpildes apstrādes vispirms ir jākonfigurē integrācija gan pakalpojumā Talent, gan pakalpojumā Dayforce.

Ja maksājumu izpildei izmantojat tādu pakalpojumu kā Dayforce, jums ir jāiespējo integrācija pakalpojumā Talent. Integrācijai ir nepieciešami noteikti Talent dati. Tādēļ ir jāpārliecinās, vai uz Dayforce kartētie dati pakalpojumā Talent ir konfigurēti veidā, kas atbalsta integrāciju. Integrācija izmanto tālāk norādītās vispārējās datu kategorijas.

- Personāla vadības dati
- Atlīdzības dati
- Algu dati, piemēram, apmaksas cikli, apmaksas periodi un ienākumu veidu kodi
- Nodarbināto dati

Šajā tēmā ir aprakstītas darbības, kas jāveic, lai iespējotu integrāciju. Tajā ir arī izskaidrots, kādu veidu dati un konfigurācijas informācija ir nepieciešama integrācijai.

## <a name="enable-the-integration"></a>Integrācijas iespējošana

Lai izveidotu savienojumu ar Dayforce, pakalpojumā Talent ir jāieslēdz integrācija un jāievada konfigurācijas informācija. Ja vēlaties, lai izveidotā Virsgrāmatas transakcija tiktu importēta programmā Microsoft Dynamics 365 for Finance and Operations, ir jāiestata arī Microsoft Azure krātuves konts un programmā Finance and Operations jāievada Azure krātuves savienojuma virkne.

Lai pakalpojumā Talent ieslēgtu integrāciju, veiciet tālāk norādītās darbības.

1. Lapā **Sistēmas administrēšana** atlasiet opciju **Integrācijas konfigurēšana**.
2. Ievadiet drošo failu pārsūtīšanas protokola (FTP) galapunktu un drošo FTP mapes ceļu.
3. Ievadiet tā lietotāja lietotājvārdu un paroli, kurš piekļūs drošajam FTP galapunktam un mapes ceļam.
4. Pārbaudiet savienojumu, kā nepieciešams, un opciju **Iespējot algu aprēķina integrāciju** iestatiet uz **Jā**.

Kad integrācija ir ieslēgta, tiek izveidota datu eksportēšanas pakotne un faili, kā arī iestatīts biežums. Biežumu varat mainīt atbilstoši vajadzībām.

Papildinformāciju par Azure krātuves kontiem un Azure krātuves savienojuma virknēm skatiet tālāk sniegtajās Azure tēmās.

- [Par Azure krātuves kontiem](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [Azure krātuves savienojuma virkņu konfigurēšana](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a>Datu konfigurēšana 

Lai apstrādātu algas, pakalpojumā Talent ir jākonfigurē personāla vadības dati. Jums ir jāiestata organizācijas dati, piemēram, darbi un amati, kā arī informācija par atvieglojumiem un atlīdzību. Šie dati nodrošina informāciju par nodarbinātību, samaksu un ieturējumiem, kas nepieciešama darbinieka algas ģenerēšanai.

### <a name="human-resource-data"></a>Personāla vadības dati

#### <a name="benefits"></a>Atvieglojumi 

Personāla vadība nodrošina rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, ieturējumus un nodarbināto atlīdzības plānus, ko organizācija piedāvā vai apstrādā saviem nodarbinātajiem.

Kad veidojat atvieglojumus, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.

##### <a name="benefit-plans"></a>Atvieglojumu plāni

- Plāns (obligāti)
- Tips (obligāti)
- Algas ietekme (obligāti)
- Atgūt nokavētos maksājumus
- Ieturējuma metode
- Ieturējuma prioritāte
- Ierobežojuma periods
- Ierobežojuma summa

##### <a name="benefits"></a>Atvieglojumi

- Plāns (obligāti)
- Tips (obligāti)
- Opcija (obligāti)
- Atvieglojumu ID (obligāti)
- Biežums
- Pamats
- Summa vai likme
- Ienākumu veida kods

##### <a name="supported-frequencies"></a>Atbalstītās biežuma vērtības 

- Katru nedēļu
- Katru otro nedēļu
- Pusmēneša
- Mēnesis

##### <a name="supported-bases"></a>Atbalstītās pamata vērtības 

- Fiksēta summa
- Ienākumu procentuālais daudzums
- Produktīvās stundas

Dayforce izveido tālāk norādītos ieturējumus, pamatojoties uz atvieglojumu plānā definēto algas ietekmi.

| Atlase pakalpojumā Talent        | Rezultāts pakalpojumā Dayforce                            |
|----------------------------|-----------------------------------------------|
| Neviens                       | Nav izveidots neviens ieturējums.                      |
| Tikai ieturējums             | Ir izveidots darbinieka ieturējums.             |
| Tikai segums          | Ir izveidots darba devēja ieturējums.             |
| Ieturējums un segums | Ir izveidots darbinieka un darba devēja ieturējums. |

Papildinformāciju par atvieglojumu programmas definēšanu un pārvaldību skatiet tālāk sniegtajās tēmās.

- [Darbinieku atvieglojumu programmas nodrošināšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [Jauna atvieglojuma izveide](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [Atvieglojumu reģistrēšana un noņemšana nodarbinātajiem](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>Atlīdzība 

Atlīdzību pārvaldība tiek izmantota, lai kontrolētu pamatalgas un prēmiju izsniegšanu. Darbinieka fiksētā pamatalga un nopelnu palielinājumi tiek kontrolēti, izmantojot fiksētas atlīdzības plānus. Veicināšanas maksājumu izsniegšana, piemēram, prēmiju maksājumi, apbalvojumi par sasniegumiem, uzņēmuma akciju iegādes iespējas un dotācijas, kā arī vienreizējas piemaksas, tiek kontrolētas ar mainīgās atlīdzības plāniem.

Dayforce izmanto atlīdzības informāciju, lai aprēķinātu darbinieka stundas vai gada likmi. Ir jānorāda fiksētās atlīdzības plāni un apmaksas likmes konvertēšanas gadījumi. Darbiniekiem ir jābūt saistītiem ar fiksētās atlīdzības plānu.

Papildinformāciju par atlīdzības plāniem skatiet tālāk sniegtajās tēmās.

- [Fiksētās atlīdzības plānu izveidošana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [Mainīgās atlīdzības plānu izveidošana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [Algas/atlīdzības organizācijas un plānu izstrāde](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [Procesa kompensācija](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [Atlīdzības procesa definēšana un rezultātu aprēķināšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [Darbinieka reģistrēšana fiksētās atlīdzības plānā](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [Darbinieka reģistrēšana mainīgās atlīdzības plānā](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>Darbi 

Darbs ir uzdevumu un atbildības jomu kopums, kas ir jāizpilda personai, kura veic darbu. Lai iegūtu papildu informāciju, skatiet šādas tēmas:

- [Darba komponentu iestatīšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [Jaunu darbu definēšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>Amati

Pozīcija ir atsevišķa darba instance. Piemēram, amats Pārdošanas daļas vadītājs (austrumu reģions) ir tikai viens no amatiem, kas ir saistīti ar darbu Pārdošanas daļas vadītājs. Amats pastāv nodaļā. Ar katru amatu var būt saistīts tikai viens nodarbinātais.

Iestatot jaunus amatus, ņemiet vērā tālāk norādītos datus un konfigurāciju.

- Amats (obligāti)
- Apraksts (obligāti)
- Darbs (obligāti)
- Nodaļa (obligāti)
- Amata veids (obligāti)
- Pilnas slodzes ekvivalents
- Ikgadējās parastās stundas (obligāti)
- Apmaksātāja juridiskā persona (obligāti)
- Apmaksas cikls (obligāti)
- Noklusējuma finanšu dimensija — izmaksu centrs (obligāti)
- Nodarbinātā piešķire — nodarbinātais, piešķires sākums, piešķires beigas, iemesla kods

Ja vienā nodaļā ar to pašu darbu ir saistīti vairāki amati, tie pakalpojumā Dayforce tiek apvienoti vienā amatā.

Lai iegūtu papildu informāciju, skatiet šādas tēmas:

- [Organizēt darbaspēku, izmantojot nodaļas, darbus un amatus](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [Amatu iestatīšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>Nodaļas

Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu. Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību. Nodaļas var izmantot, lai ziņotu par funkcionālām jomām. Nodaļām var būt peļņas un zaudējumu atbildība.

Lai iegūtu papildu informāciju, skatiet šādas tēmas:

- [Nodaļas izveide un tās saistīšana ar nodaļu hierarhiju](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [Jaunu nodaļu definēšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>Apmaksas cikli un apmaksas periodi

Apmaksas cikls nosaka, cik bieži tiek veikts algu aprēķins, kā arī konkrētās dienas, kurās nodarbinātie saņem samaksu. Apmaksas cikls var būt, piemēram, ikmēneša, un darbinieki samaksu var saņemt mēneša pēdējā dienā. Vai arī apmaksas cikls var būt iknedēļas, un darbinieki samaksu var saņemt otrdienā pēc apmaksas perioda beigām. Apmaksas cikli tiek piešķirti amatiem, lai kontrolētu to, kad nodarbinātie šajos amatos saņems samaksu.

Pēc apmaksas ciklu izveides katram ciklam varat ģenerēt apmaksas periodus. Katrā apmaksas periodā ir ietverts noklusējuma maksājuma datums, kura pamatā ir jūsu sniegtā informācija. Taču varat modificēt apmaksas perioda noklusējuma maksājuma datumu izņēmumu iestatīšanai, piemēram, kad maksājuma datums ir brīvdienā.

Dayforce izmanto tālāk norādīto informāciju.

- Apmaksas cikls (obligāti)
- Apmaksas cikla biežums (obligāti)
- Perioda sākuma datums (ir jānorāda pirmais apmaksas periods)
- Noklusējuma maksājuma datums (ir jānorāda pirmais apmaksas periods)

Šī informācija pakalpojumā Dayforce ir integrēta kā apmaksas grupas, un katram apmaksas ciklam to atdala valsts vai reģions. Pirms integrācijas ir jābūt ģenerētam vismaz vienam apmaksas periodam. Dayforce ģenerē apmaksas grupu kalendārus un maksājumu datumus atbilstoši pakalpojumā Talent iestatītajam pirmā apmaksas perioda sākuma datumam un noklusējuma maksājuma datumam.

#### <a name="earning-codes"></a>Ienākumu veida kodi

Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie. Kodiem ir dažādi ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.

Dayforce izmanto tālāk norādīto informāciju.

- Ienākumu veida kods (obligāti)
- apraksts
- Mērvienība
- Produktīvs

### <a name="worker-data"></a>Nodarbināto dati

Dažādo veidu nodarbināto ieraksti ir svarīga informācija personāla vadības un algu sistēmās. Ievadīto informāciju var izmantot, lai sekotu nodarbinātajiem un personiskajai informācijai.

Par darbiniekiem var saglabāt tālāk norādīto informāciju.

- **Pamata** — saglabājiet pamata informāciju par darbinieku, piemēram, kontaktinformāciju, demogrāfisko informāciju, identifikācijas informāciju, ģimenes informāciju, karadienesta statusu, ekspatriantu informāciju, kā arī personiskās un ārkārtas kontaktpersonas.
- **Nodarbinātība** — saglabājiet informāciju par darbinieka nodarbinātību, piemēram, informāciju par piederību uzņēmumam vai organizācijai, amata piešķiri, sākuma un beigu datumiem, piemērotību darbam, nodarbinātības noteikumiem, pensiju, atvaļinājumu un pārcelšanu.
- **Atvaļinājumi un kavējumi** — saglabājiet informāciju par nodarbinātā kavējumiem, piemēram, informāciju par darba kalendāriem, kavējumu darbībām un kavējumu iestatījumiem.
- **Atlīdzība un alga** — saglabājiet informāciju par nodarbinātā atlīdzības plāniem un algas informāciju, piemēram, plāna reģistrāciju, piemaksām, sniegumu, komisiju, nodokļu informāciju, pensionēšanos un ieturējumiem no algas.

Ievadot informāciju par nodarbināto, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.

#### <a name="general-information"></a>Vispārīgā informācija

- Personāla numurs (obligāti)
- Vārds (obligāti)
- Uzvārds (obligāti)
- Otrais vārds
- Darba stāža datums
- Zināms kā

#### <a name="personal-information"></a>Personiskā informācija

- Ģimenes stāvoklis (obligāti)
- Dzimšanas datums (obligāti)
- Dzimums (obligāti)
- Persona ar īpašām vajadzībām
- Nacionalitātes valsts/reģions (tikai Meksikai)

#### <a name="address-information"></a>Adreses informācija

- Primārā (obligāti)
- Valsts/reģions (obligāti)
- Pasta indekss (obligāti)
- Ielas numurs (obligāti) (tikai Meksikai)
- Mājas numurs/nosaukums (tikai Meksikai)
- Pilsēta (obligāti)
- Administratīvais apgabals (obligāti)
- Apgabals (obligāti)

#### <a name="contact-information"></a>Kontaktinformācija 

- Primārā (obligāti)
- Kontaktpersonas tālrunis (obligāti)
- Paplašinājums

#### <a name="payroll-information-and-earning-codes"></a>Algas informācija un ienākumu veidu kodi

Darbiniekiem var būt piešķirti konkrēti ienākumu veidi konkrētajā maksājumu biežumā, kā arī var būt norādīta vēlamā maksāšanas metode. Lai palīdzētu nodrošināt, ka šīs preferences un iestatījumi tiek izmantoti, pakalpojumā Dayforce ir tālāk norādītie lauki.

##### <a name="earning-codes"></a>Ienākumu veida kodi

- Amats (obligāti)
- Ienākumu veida kods (obligāti)
- Biežums (obligāti)
- Summa (obligāti)

##### <a name="payroll-information"></a>Algas informācija

- Maksāšanas metode
- Ekonomiskais reģions (obligāti)
- Darbinieka atvieglojumu ID
- Nacionālais ID numurs (obligāti)
- Karadienesta numurs
- Maiņas ID (obligāti)
- Nodokļu numurs (obligāti)
- Arodbiedrības ID (obligāti)
- Darba dienas ID (obligāti)
- Darba atļaujas numurs

> [!NOTE]
> Meksika atbalsta šādas maksāšanas metodes: **Skaidra nauda**, **Čeks** (uzņēmuma fiziskais čeks) un **Elektroniskais maksājums**. Ja nav norādīta neviena maksāšanas metode, pēc noklusējuma tiek izmantota opcija **Čeks**.

#### <a name="employment-details"></a>Nodarbinātības papildinformācija

Nodarbinātības datu vēsture pakalpojumā Dayforce tiek izmantota kā galvenā informācija, no kuras tiek iegūts darbinieka darbā pieņemšanas, darba attiecību izbeigšanas un atkārtotas pieņemšanas darbā statuss. Dayforce vienlaikus atbalsta tikai vienu aktīvu nodarbinātības ierakstu.

- Nodarbinātības sākuma datums (obligāti)
- Nodarbinātības beigu datums
- Pieņemšanas datums
- Koriģētais pieņemšanas datums
- Darba attiecību pārtraukšanas datums (jānorāda, kad tiek pārtrauktas darba attiecības)
- Darba attiecību pārtraukšanas iemesls (jānorāda, kad tiek pārtrauktas darba attiecības)

Darbinieka galvenie datumi tiek iegūti, izmantojot tālāk norādīto informāciju.

| Talent                | Dayforce                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| Pēdējais nomas datums | Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta nodarbinātības sākums                                 |
| Izbeigšanas datums      | Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta darba attiecību pārtraukšanas datums                                 |
| Pieņemšanas datums            | Pašreizējā neaktīvā nodarbinātības vēstures ieraksta koriģētais sākuma datums, sākuma datums vai nodarbinātības sākums |
| Sākotnējais darbā pieņemšanas datums    | Agrākā nodarbinātības vēstures ieraksta nodarbinātības sākums                                               |

#### <a name="compensation"></a>Atlīdzība

Fiksētās atlīdzības plānam ir jābūt saistītam ar katra darbinieka primāro amatu visā nodarbinātības periodā. Šis periods sākas ar datumu, kurā darbinieks tika pieņemts darbā (vai nodarbinātības sākuma datumu), un turpinās līdz darba attiecību pārtraukšanai.

- Spēkā stāšanās datums (obligāti)
- Beigu datums
- Apmaksas likme (obligāti)
- Apmaksas likmes konvertēšanas gadījumi (obligāti)
- Gada ekvivalents (obligāti)
- Stundas ekvivalents (obligāti)

Ja darbiniekam ar stundas likmi ir vairāki amati, pakalpojumā Dayforce kā darbinieka līmeņa pamatlikme/alga tiek importēta primārā amata fiksētā atlīdzība. To amatu, kas nav primārie, stundas likme tiek saglabāta pakalpojumā Dayforce attiecīgajā amatā.

Ja darbiniekam, kurš saņem algu, ir vairāki amati, kā darbinieka līmeņa pamatlikme/alga tiek iegūta un izmantota visu aktīvo amatu kopējā stundas likme un gada alga.

#### <a name="identification-numbers"></a>Identifikācijas numuri

##### <a name="social-security-identifier"></a>Sociālās apdrošināšanas numurs 

Katram darbiniekam ir jābūt vienam primārajam numuram. Šī numura identifikācijas tipam ir jābūt **SAN**. Pakalpojumā Dayforce tas tiek automātiski iegūts kā darbinieka sociālās apdrošināšanas numurs, kas ir jānorāda, kad darbinieks tiek pieņemts darbā.

- Primārais (obligāti)
- Identifikācijas tips = SAN
- Izdošanas datums
- Beigu datums

Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **SAN**. Taču pakalpojumā Dayforce tiek integrēts tikai ieraksts, kas ir atzīmēts kā **Primārais**, neatkarīgi no tā, vai šis numurs ir aktīvs vai tam ir beidzies derīgums.

#### <a name="bank-accounts-and-disbursements"></a>Banku konti un izdevumi

Jebkuram darbiniekam, kurš samaksu izvēlējies saņemt bankas konta pārskaitījuma veidā, ir jāievada derīga bankas konta informācija.

| Talent                         | Dayforce                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| Bankas konta numurs (obligāti) |                                                                                                             |
| SWIFT kods (obligāti)          | Lauku **Bankas ID** izmanto, apstrādājot algas Meksikā.                                                             |
| Filiāles numurs (obligāti)       |                                                                                                             |
| Bankas konta tips (obligāti)   | Lauku **Konta tips** izmanto, apstrādājot algas Meksikā. Atbalstītās vērtības ir, piemēram, **Norēķini** un **Algas**. |

> [!NOTE]
> Darbiniekiem, kuri samaksu izvēlas saņemt bankas konta pārskaitījumu veidā, ir jāsniedz saite uz juridiskās personas, kuras primārā adrese ir Meksikā, atlikumu kontu, kas ir saistīts ar derīgu Meksikas bankas kontu. Visi pārējie konti, kas nav atlikumu konti, tiek ignorēti.

#### <a name="address-information"></a>Adreses informācija

Katram darbiniekam ir jābūt vienai primārajai vietai. Pakalpojumā Dayforce šī vieta tiek izmantota, lai nodokļu piemērošanas nolūkos noteiktu darbinieka primāro dzīvesvietu.

- Primārā (obligāti)
- Valsts/reģions (obligāti)
- Pasta indekss (obligāti)
- Iela (obligāti)
- Ielas numurs (obligāti)
- Mājas numurs/nosaukums
- Pilsēta (obligāti)
- Administratīvais apgabals (obligāti)
- Apgabals (obligāti)

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>Datu konfigurēšana algu ģenerēšanai Amerikas Savienotajās Valstīs un Kanādā

Ja ģenerējat algas darbiniekiem Amerikas Savienotajās Valstīs un Kanādā, ir jākonfigurē tālāk norādītie elementi.

- Amatiem ir jānorāda nodaļas.
- Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.

> [!NOTE] 
> Varat konfigurēt Talent, lai amatiem būtu jānorāda nodaļa. Lai to izdarītu, pārejiet uz **Personāla vadības kopīgotie amati > Amati > Pieprasīt amatiem nodaļas**. Ieteicams piemērot šo iestatījumu integrācijai.

### <a name="job-types"></a>Darba tipi

Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās. Darbu veidi ir nepieciešami, lai apstrādātu algas Amerikas Savienotajās Valstīs un Kanādā. Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs. Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.

Ir jānorāda tālāk norādītie darbu veidi un apraksti.

| Darba veids   | apraksts |
|------------|-------------|
| Ik stundu     | Ik stundu      |
| Algots   | Algots    |

### <a name="position-types"></a>Amatu veidi 

Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs. Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.

Ir jānorāda tālāk norādītie amatu veidi un apraksti.

| Amata tips   | apraksts        |
|-----------------|--------------------|
| Pilna laika       | Pilna laika darbinieks |
| Nepilna laika       | Nepilna laika darbinieks |

### <a name="reason-codes"></a>Iemeslu kodi

Iemeslu kodi sniedz informāciju par darbinieka statusu. Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.

Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.

| Iemeslu kodi    | apraksts      | Piemērojamie scenāriji |
|----------------|------------------|----------------------|
| RESIGNATION    | Atlūgums      | Pārtraukt darba attiecības ar nodarbināto     |
| TERMINATION    | Izbeigšana      | Pārtraukt darba attiecības ar nodarbināto     |
| RETIREMENT     | Aiziešana pensijā       | Pārtraukt darba attiecības ar nodarbināto     |
| CITI          | Citi iemesli    | Pārtraukt darba attiecības ar nodarbināto     |
| DEATH          | Nāve            | Pārtraukt darba attiecības ar nodarbināto     |
| LEAVEOFABSENCE | Atvaļinājums | Pārtraukt darba attiecības ar nodarbināto     |
| CONTRACTEND    | Līguma beigas  | Pārtraukt darba attiecības ar nodarbināto     |
| SALARYCHANGE   | Algas izmaiņas | Atlīdzība         |

### <a name="marital-status"></a>Ģimenes stāvoklis

Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.

Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.

| Talent                 | Dayforce             |
|------------------------|----------------------|
| Precējies (-usies)                | Precējies (-usies)              |
| Neprecējies (-usies)                 | Neprecējies (-usies)               |
| Atraitnis                | Atraitnis              |
| Šķīries (-usies)               | Šķīries (-usies)             |
| Reģistrētas attiecības | Dzīvesbiedrs |
| Neviens                   | Neviens                 |
| Kopdzīve             | Kopdzīve           |

### <a name="gender"></a>Dzimums

Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.

Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.

| Talent       | Dayforce        |
|--------------|-----------------|
| Vīrietis         | Vīrietis            |
| Sieviete       | Sieviete          |
| Nav specifisks | *Netiek atbalstīts* |

### <a name="earning-codes"></a>Ienākumu veida kodi

Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie. Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja. Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.

#### <a name="supported-frequencies"></a>Atbalstītās biežuma vērtības

- Visus
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH–1N2N3N4OFMTH
- 2N3N4N5OFMth–2N3N4N5OFMth
- 1OFQTR–1OFQTR
- LASTOFQTR–LASTOFQTR
- LASTMTHOFQTR–LASTMTHOFQTR
- 1OFYEAR–1OFYEAR
- LASTOFYEAR–LASTOFYEAR
- NOVNDECOFYEAR–NOVNDECOFYEAR

### <a name="addresses"></a>Adreses

Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji. Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.

| Talent          | Dayforce              |
|-----------------|-----------------------|
| Valsts/reģions  | Valsts kods          |
| Pasta indekss | Pasta indekss           |
| Administratīvais apgabals           | Administratīvā apgabala kods            |
| Pilsēta            | Pilsēta                  |
| Apgabals          | Apgabals (pašvaldība) |
| Iela          | Adreses 1. rinda        |

### <a name="tax-regions"></a>Nodokļu reģioni

Nodokļu reģionus izmanto, lai noteiktu atbilstošos nodokļus, kas jāpiemēro, ģenerējot algu aprēķinus. Nodokļu reģioni tiek kartēti uz pakalpojumu Dayforce kā vietas adreses. Noklusējuma nodokļu reģionam ir jābūt saistītam ar nodarbinātā aktīvo amatu. 

- Nodokļu reģions (obligāti)
- Valsts/reģions (obligāti)
- Administratīvais apgabals (obligāti)
- Apgabals 
- Pilsēta (obligāti)

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>Datu konfigurēšana algu aprēķina ģenerēšanai Meksikā

Ja ģenerējat algas darbiniekiem Meksikā, ir jākonfigurē tālāk norādītie elementi.

- Amatiem ir jānorāda nodaļas.
- Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.

### <a name="job-types"></a>Darba tipi

Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās. Lai apstrādātu algas Meksikā, ir nepieciešami darbu veidi. Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs. Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.

Ir jānorāda tālāk norādītie darbu veidi un apraksti.

| Darba veids   | apraksts |
|------------|-------------|
| Ik stundu     | Stundu (MX)   |
| Algots   | Algots (MX) |

### <a name="position-types"></a>Amatu veidi 

Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs. Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.

Ir jānorāda tālāk norādītie amatu veidi un apraksti.

| Amata tips   | apraksts        |
|-----------------|--------------------|
| Pilna laika       | Pilna laika darbinieks |
| Nepilna laika       | Nepilna laika darbinieks |

### <a name="reason-codes"></a>Iemeslu kodi

Iemeslu kodi sniedz informāciju par darbinieka statusu. Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.

Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.

| Iemeslu kodi            | apraksts                    | Piemērojamie scenāriji |
|------------------------|--------------------------------|----------------------|
| DEPARTUREBEFOREPAYMENT | Aiziešana no amata pirms pirmās algas | Pārtraukt darba attiecības ar nodarbināto     |
| RESIGNATION            | Atlūgums                    | Pārtraukt darba attiecības ar nodarbināto     |
| PENSION                | Pensija                        | Pārtraukt darba attiecības ar nodarbināto     |
| TERMINATION            | Izbeigšana                    | Pārtraukt darba attiecības ar nodarbināto     |
| RETIREMENT             | Aiziešana pensijā                     | Pārtraukt darba attiecības ar nodarbināto     |
| ABSENTEE               | Darba kavētājs                       | Pārtraukt darba attiecības ar nodarbināto     |
| CITI                  | Citi iemesli                  | Pārtraukt darba attiecības ar nodarbināto     |
| CLOSURE                | Uzņēmuma slēgšana               | Pārtraukt darba attiecības ar nodarbināto     |
| DEATH                  | Nāve                          | Pārtraukt darba attiecības ar nodarbināto     |
| LEAVEOFABSENCE         | Atvaļinājums               | Pārtraukt darba attiecības ar nodarbināto     |
| CONTRACTEND            | Līguma beigas                | Pārtraukt darba attiecības ar nodarbināto     |
| SALARYCHANGE           | Algas izmaiņas               | Atlīdzība         |

### <a name="terms-of-employment"></a>Nodarbinātības noteikumi

Nodarbinātības noteikumus izmanto, lai izveidotu nodarbinātības noteikumu kategorijas. Noteikumi tiek kartēti uz pakalpojumu Dayforce kā nodarbinātības rādītāju vērtības.

Ir nepieciešami tālāk norādītie nodarbinātības noteikumi un apraksti.

| Nodarbinātības noteikumi   | apraksts |
|-----------------------|-------------|
| Regulārs               | Regulārs     |
| Tieši                | Tieši      |
| Štažēšanās            | Štažēšanās  |
| Pastāvīga             | Pastāvīga   |

### <a name="marital-status"></a>Ģimenes stāvoklis

Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.

Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.

| Talent                 | Dayforce                  |
|------------------------|---------------------------|
| Precējies (-usies)                | Precējies (-usies)                   |
| Neprecējies (-usies)                 | Neprecējies (-usies)                    |
| Atraitnis                | Atraitnis                   |
| Šķīries (-usies)               | Šķīries (-usies)                  |
| Reģistrētas attiecības | Dzīvesbiedrs      |
| Neviens                   | *Netiek atbalstīts Meksikā* |
| Kopdzīve             | *Netiek atbalstīts Meksikā* |

### <a name="gender"></a>Dzimums

Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.

Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.

| Talent       | Dayforce                  |
|--------------|---------------------------|
| Vīrietis         | Vīrietis                      |
| Sieviete       | Sieviete                    |
| Nav specifisks | *Netiek atbalstīts Meksikā* |

### <a name="payment-method"></a>Maksājumu metode

Maksāšanas metodes darbiniekam un uzņēmumam ļauj aprakstīt, kā darbinieki saņems samaksu. Maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.

Tālāk esošajā tabulā ir parādīts, kā maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce.

| Talent             | Dayforce                  |
|--------------------|---------------------------|
| Kase               | Kase                      |
| Elektronisks maksājums | Pārsūtījums                  |
| Atzīmēt              | Čeks                    |
| Bankas vekselis         | *Netiek atbalstīts Meksikā* |
| Citi              | *Netiek atbalstīts Meksikā* |

### <a name="bank-account-type"></a>Bankas konta tips

Bankas kontu tipus izmanto darbiniekiem sūtāmajiem elektroniskajiem maksājumiem. Bankas kontu tipi tiek kartēti uz pakalpojumu Dayforce kā pārsūtīšanas konta informācija. Bankas kontu tipi integrācijas laikā tiek atbilstoši tulkoti uz apstiprinātajām vērtībām.

| Talent            | Dayforce                  |
|-------------------|---------------------------|
| Kontroles konts  | CheckingAccount           |
| Algu konts   | PayrollAccount            |
| Uzkrājumu konts   | *Netiek atbalstīts Meksikā* |
| BankGirot konts | *Netiek atbalstīts Meksikā* |
| PlusGirot konts | *Netiek atbalstīts Meksikā* |

### <a name="earning-codes"></a>Ienākumu veida kodi

Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie. Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja. Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.

#### <a name="supported-frequencies"></a>Atbalstītās biežuma vērtības

- Visus
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH–1N2N3N4OFMTH
- 2N3N4N5OFMth–2N3N4N5OFMth
- 1OFQTR–1OFQTR
- LASTOFQTR–LASTOFQTR
- LASTMTHOFQTR–LASTMTHOFQTR
- 1OFYEAR–1OFYEAR
- LASTOFYEAR–LASTOFYEAR
- NOVNDECOFYEAR–NOVNDECOFYEAR

### <a name="addresses"></a>Adreses

Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji. Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.

| Talent              | Dayforce              |
|---------------------|-----------------------|
| Valsts/reģions      | Valsts kods          |
| Pasta indekss     | Pasta indekss           |
| Administratīvais apgabals               | Administratīvā apgabala kods            |
| Pilsēta                | Pilsēta                  |
| Apgabals              | Apgabals (pašvaldība) |
| Iela              | Adreses 1. rinda        |
| Ielas numurs       | Adreses 2. rinda        |
| Mājas numurs/nosaukums | Adreses 5. rinda        |

### <a name="passport-number"></a>Pases numurs

Darbinieki var sniegt pases informāciju. Šīs informācijas identifikācijas tips ir **Pase**, un tā tiek integrēta pakalpojumā Dayforce kā daļa no darbinieka Meksikai specifiskās informācijas.

- Identifikācijas tips = Pase
- Izdošanas datums
- Beigu datums

Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **Pase**. Taču pakalpojumā Dayforce tiek integrēts tikai pašreizējais aktīvais pases ieraksts. Ja visiem pases ierakstiem ir beidzies derīgiem, pakalpojumā Dayforce tiek integrēta pēdējā izdotā pase.
