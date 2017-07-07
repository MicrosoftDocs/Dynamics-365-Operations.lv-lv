---
title: "Jaunināšanas pārslēgšanas testēšana"
description: "Šajā tēmā ir paskaidrots, kā testēt uzdevumus, kas tiek sākti pēc AX 2012 izslēgšanas, bet pirms Dynamics 365 for Finance and Operations izdevuma Enterprise ieslēgšanas."
author: tariqbell
manager: AnnBe
ms.date: 05/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 711ad5cc3aafacf209704349effb4e08019205ac
ms.contentlocale: lv-lv
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-cutover-testing"></a>Jaunināšanas pārslēgšanas testēšana

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

*Pārslēgšana* ir termins, ko mēs lietojam jaunās sistēmas palaišanas gala procesam. Šis pārslēgšanas process sastāv no uzdevumiem, kas tiek sākti pēc Microsoft Dynamics AX 2012 izslēgšanas, bet pirms Dynamics 365 for Finance and Operations izdevuma Enterprise ieslēgšanas. Jaunināšanas pārslēgšanas testēšanas mērķis ir izmēģināt pārslēgšanas procesu, lai palīdzētu nodrošināt gludu pieredzi visiem, kuri ir iesaistīti faktiskajā pārslēgšanas palaišanas procesā.

Pārslēgšanas laikā pastāv divas galvenās darbplūsmas:

- **Tehniskā darbplūsma** — šī darbplūsma ietver datu jaunināšanas izpildes procesu. Jūsu uzņēmumam būs jāievieš atļautā dīkstāves ilguma ierobežojums. Šajā dīkstāves laikā nebūs pieejams ne AX 2012, ne Finance and Operations. Šai darbplūsmai, iespējams, vajadzēs pielāgot datu jaunināšanas procedūru, lai tā atbilstu uzņēmuma dīkstāves ilguma ierobežojumam.
- **Funkcionālā darbplūsma** — šī darbplūsma ietver konfigurācijas uzdevumus, kas tiek veikti pēc datu jaunināšanas pabeigšanas. Visi šie uzdevumi ir jādokumentē, jānorāda to daudzums, kā arī tiem jāpiešķir resurss, jo gan funkcionālajai, gan tehniskajai darbplūsmai ir jāatbilst uzņēmuma dīkstāves ilguma ierobežojumam.

Šajā attēlā parādīts kopējais pārslēgšanas process palaišanai tāds, kāds tas notiks ražošanas vidē.

![Pārslēgšanas process](./media/cutover_1.png)

Šis pārslēgšanas process atšķiras no pamata datu jaunināšanas smilškastes vidē šādos veidos:

- AX 2012 datu bāze netiek kopēta, bet tiek izveidota tikai tās dublējumkopija, un pēc tam tiek modificēta sākotnējā datu bāze. Šī pieeja ir ātrāka, un dublējumkopija nodrošina atriti, ja atrite ir nepieciešama.
- Jo ražošanas vidē Finance and Operations ir ierobežota piekļuve, uzdevumus, kas iepriekš tika veikti Application Object Server (AOS) Smilškastes instancē, tagad tiek veikti, izmantojot Microsoft DSE grupu. Šie uzdevumi ietver lejupielādes un importēšanas bacpac failu, un darbina MajorversionDataUpgrade.zip pakotni.
- Mēs pievienojām šādus uzdevumus:

    - Veikt dūmu testu.
    - Veikt programmas iestatīšanas uzdevumus. Atkarībā no izmantotās funkcionalitātes šī darbība var būt apjomīga. Šīs darbības laikā funkcionālā grupa konfigurē jaunu programmas funkcionalitāti tā, ka tā ir gatava izmantošanai jaunināšanas sistēmā.
    - Atļaut lietotājiem no jauna pieteikties. Paziņot lietotājiem, ka jaunināšana ir pabeigta un viņi var atkal izmantot sistēmu.

## <a name="technical-workstream"></a>Tehniskā darbplūsma

Tehniskā darbplūsma ietver dažādas tehniskās grupas dalībniekus: datu bāzes administratoru (DBA), AX 2012 sistēmas administratoru, servera administratoru un izstrādātājus, kuri pārzina AX 2012 un Finance and Operations. Šajā tēmā ir izskaidrots, kuri uzdevumi ietver lomas un kādas ir šīs lomas.

Pārslēgšanas testa laikā tehniskā komanda uzmanību pievērš datu jaunināšanas procesa veiktspējas un uzticamības testēšanai, lai pārliecinātos, vai tas atbilst biznesa dīkstāves ierobežojumam. Daudzi aparatūras un programmatūras elementi ir iesaistīti šajā procesā. Daži no šiem elementiem ir lokāli, bet citi — Microsoft mākonī. Turklāt ir iesaistīti daudzi pielāgotās programmas koda un standarta koda elementi. Šīs testēšanas rezultātam vajadzētu būt pārliecinātībai par vides pārslēgšanas procesu.

### <a name="turn-off-the-ax-2012-aos-instances"></a>Izslēgt AX 2012 AOS instances

Šis uzdevums ir saistīts ar AX 2012 sistēmas administratoru un serveru administratoriem.

Vajadzētu pārbaudīt tālāk minētos apgabalus.

- **Pakešuzdevumi, kas tiek izpildīti pārslēgšanas laikā** — ilglaicīgi pakešuzdevumi, kuru izpilde jau ir sākta, kavēs sistēmas apstāšanos. Plānojiet uz priekšu, lai varētu pārtraukt AOS instanču darbību vēlamajā brīdī. Iespējams, jums jāplāno partijas tā, lai tās tiktu pabeigtas kādu laiku pirms izslēdzat AX 2012.
- **Integrētas sistēmas** — jums var būt arī citas sistēmas, kas ir integrētas AX 2012 vidē. Šīs sistēmas ir jāiekļauj savā plānā, lai izslēgtu AX 2012. Piemēram, integrētās sistēmas ieteicams izslēgt kādu laiku pirms AX 2012 izslēgšanas, lai varētu pabeigt atlikušās sāktās darbības. Integrētas sistēmas prasības atšķiras atkarībā no konkrētā uzņēmuma vajadzībām. Tāpēc ekspertu komandai šis scenārijs jāplāno neatkarīgi.

### <a name="create-a-backup-of-the-ax-2012-database"></a>Izveidot AX 2012 datu bāzes dublējumkopiju.

Šis uzdevums ietver DBA. Dublējumkopija tiks izmantota, ja būs nepieciešama atrite. Tas tiks izmantots arī kā atsauces punkts, kas tiks uzturēts periodam, un parādīs sistēmas stāvokli pārslēgšanas brīdī.

Vajadzētu pārbaudīt tālāk minētos apgabalus.

- Konkrētu dublēšanas procesu laiku iegūšana.
- Pielāgojiet lietotās dublējuma opcijas (piemēram, saspiešanu salīdzinājumā nesaspiešanu), lai palīdzētu nodrošināt ātrāko iespējamo dublējumkopiju.

### <a name="export-the-database-to-bacpac"></a>Datu bāzes eksportēšana bacpac failā

Šis uzdevums ietver DBA. Šī uzdevuma izvade ir eksporta fails, kas tiks augšupielādēts Microsoft Azure lietošanai jaunajā sistēmā.

Vajadzētu pārbaudīt tālāk minētos apgabalus.

- Konkrētu dublēšanas procesu laiku iegūšana.
- Optimizējiet eksporta procesu, lai palīdzētu nodrošināt ātrāko iespējamo pieredzi. Optimizācijai var būt nepieciešami šādi uzdevumi:

    - Eksportēšanas laikā, piemēram, uz CPU, diska ievadizvadi un atmiņu, nosakiet sistēmas resursus.
    - Ja tiek atrastas resursa sastrēgums, izveidojiet plānu, lai to novērstu. Parasti šie sastrēgumi tiek novērsti, piešķirot vairāk nepieciešamo resursu.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Bacpac faila augšupielāde Azure krātuvē

Šis uzdevums ir saistīts ar DBA vai servera administratoru. Šī uzdevuma izpildes laikā bacpac fails tiek pārvietots uz Azure.

Vajadzētu pārbaudīt tālāk minētos apgabalus.

- Atlasiet iekārtu, kas tiks izmantota augšupielādei, un pārliecinieties, vai Azure krātuves pārlūkošanas rīks ir konfigurētas un gatavs lietošanai.
- Iegūstiet konkrētus laikus augšupielādes procesam, nosakot to vairākas reizes. Augšupielādes laiki var atšķirties, pamatojoties uz interneta savienojuma ātrumu un Azure datu centra ģeogrāfisko atrašanās vietu attiecībā pret jūsu atrašanās vietu.

### <a name="download-and-import-the-bacpac-file-to-the-azure-sql-database"></a>Bacpac faila lejupielāde un importēšana Azure SQL datu bāzē

Ja šis uzdevums tiek izpildīts tiešsaistē, to veikts Microsoft DSE grupa. Tomēr pārslēgšanas testa laikā tas ir saistīts ar jūsu DBA. Šī uzdevuma rezultāts ir eksporta fails, kas tiks augšupielādēts Azure lietošanai jaunajā sistēmā.

Vajadzētu pārbaudīt tālāk minētos apgabalus.

- Konkrētu importēšanas procesu laiku iegūšana.
- Optimizējiet eksporta procesu, lai palīdzētu nodrošināt ātrāko iespējamo pieredzi. Optimizācijai var būt nepieciešami šādi uzdevumi:

    - Eksportēšanas laikā nosakiet sistēmas resursus. Daži piemēri:

        - **AOS iekārtā:** CPU, diska ievadizvade un atmiņa
        - **Azure SQL datu bāzes instancē:** SQL datu bāzes caurlaide (DTU). Varat pārraudzīt Azure SQL DTU no Microsoft SQL Server Management Studio AOS iekārtas, apskatot sys.dm_resource_stats sistēmas skatu.

    - Ja tiek atrastas resursa sastrēgums, izveidojiet plānu, lai to novērstu. Parasti šie sastrēgumi tiek novērsti, piešķirot vairāk nepieciešamo resursu. Šī iekārta tiek viesota korporācijā Microsoft, tādēļ ir jāiesniedz pieprasījums korporācijai Microsoft, lai palielinātu resursus, ja konstatējat, ka tie ir izraisa sastrēgumu.

### <a name="run-the-majorversiondataupgradezip-package"></a>Pakotnes MajorVersiondataUpgrade.zip palaišana

Ja šis uzdevums tiek izpildīts tiešsaistē, to veikts Microsoft DSE grupa. Tomēr pārslēgšanas testa laikā tas ir saistīts ar izstrādātājiem. Šī uzdevuma laikā vecā datu bāzes struktūra tiek pārveidota uz jaunās sistēmas struktūru.

Datu bāzes sinhronizācijas process tiek izpildīts kā daļa no šī uzdevuma. Datu bāzes sinhronizēšana var aizņemt ievērojamu laiku dažās situācijās, piemēram, kad sagrupēts indekss ir mainījies uz tabulu, jo SQL vidē šī darbība ir dārga.

Ieteicams vispirms veikt analīzi un atkļūdošanas procesu izstrādes vidē. Smilškastes vidē atkļūdošanas un analīzes opcijas ir vairāk ierobežotas. Mērķis: tikai dažas vai neviena problēma, kas ir jāatrisina, kad tiek veikta pārslēgšanas testēšana.

Vajadzētu pārbaudīt tālāk minētos apgabalus.

- Konkrētu importēšanas procesu laiku iegūšana.
- Optimizējiet procesu, lai palīdzētu nodrošināt ātrāko iespējamo pieredzi. Optimizācijai var būt nepieciešami šādi uzdevumi:

    - Pārraugiet atsevišķu jaunināšanas skriptu veiktspēju, izmantojot ReleaseUpdateScriptsExecution tabulu.
    - Pielāgojiet skriptus, lai optimizētu veiktspēju. Šim uzdevumam var būt nepieciešams, lai pielāgotu skripta X++ kodu un optimizētu to datu kopai.
    - Pārraugiet Azure SQL DTU, izmantojot Microsoft Dynamics Lifecycle Services (LCS) pārraudzību vai Management Studio sistēmas skatu sys.dm_resources_stats system. Ja resursi ir izsmelti, iespējams, jums ir jāpieprasa augstāks datu bāzes līmenis no Microsoft DSE grupas.

### <a name="roll-back-to-ax-2012"></a>Atritināšana uz AX 2012

Šī uzdevuma mērķis ir atjaunot datu bāzi, izmantojot dublējumkopiju, kas izveidota, kad AX 2012 tika izslēgta un pēc tam atkal ieslēgta. Integrēto sistēmu stāvokli arī var būt nepieciešams atjaunot. Tomēr integrētas sistēmas atšķiras atkarībā no uzņēmuma, tādēļ vispirms atsevišķi plānojiet šo scenāriju, pamatojoties uz konkrētajiem apstākļiem. Lai gan maz ticams, ka būs jāveic atrite, ir ļoti svarīgi, ka jums ir pārbaudīts process gadījumā, ja tas ir nepieciešams.

## <a name="functional-workstream"></a>Funkcionālā darbplūsma

Pēc datu jaunināšanas jaunajā vidē būs nepieciešami vairāki konfigurācijas uzdevumi. Šīs darbplūsmas mērķis ir dokumentēt visus konfigurācijas uzdevumus un noteikt to skaitu, kā arī piešķirt resursus katram uzdevumam, lai palīdzētu nodrošināt, ka šos uzdevumus var veikt kopā ar tehnisko darbplūsmu dīkstāves loga laikā.

Parasti funkcionālie uzdevumi ir saistīti ar noteiktu sistēmas parametru vērtību vai citu konfigurācijas datu mainīšanu. Šie uzdevumi tiek identificēti, izmantojot pilnu funkcionālo testa procesu, kas ir tiek izpildīts atsevišķi no pārslēgšanas testēšanas. Ja šī veida uzdevums tiek identificēts, tas ir jāpārskata kopā ar funkcionālo resursu un izstrādātāju.

Lielāku izmaiņu gadījumā var būt nepieciešams jauns pielāgotu datu jaunināšanas skripts, lai datu jaunināšanas procesa laikā atjauninātu datus. Tomēr funkcionālais resurss var manuāli palaist mazākas izmaiņas, izmantojot jauno sistēmu pēc datu atjaunināšanas.

Lielākas izmaiņas, kam ir jauni datu jaunināšanas skripti, ir jātestē. Tāpēc būs jāizpilda viena vai vairākas papildu pakotnes MajorVersionDataUpgrade.zip atkārtošanas. Ir svarīgi vēlreiz aprēķināt pakotnes palaišanas izmaksas salīdzinājumā ar manuālas datu ievades izmaksām.

Katras manuāli veiktas izmaiņas pārslēgšanas plāna dokumentam ir jāpievieno uzdevums. Šajā uzdevumā jānorāda tālāk minētā informācija.

-   Kāds ir uzdevums un kas ir jādara?
-   Kam tas ir jādara?
-   Cik ilgs laiks nepieciešams tā izpildei?

