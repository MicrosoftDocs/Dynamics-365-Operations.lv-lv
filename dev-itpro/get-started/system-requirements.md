---
title: "Sistēmas prasības"
description: "Šajā tēmā ir uzskaitītas sistēmas prasības pašreizējai Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma versijai mākoņa un lokālajiem izvietojumiem."
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: lv-lv
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>Sistēmas prasības

[!include[banner](../includes/banner.md)]


Šajā tēmā ir uzskaitītas sistēmas prasības pašreizējai Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma versijai mākoņa un lokālajiem izvietojumiem. Pirms Finance and Operations instalēšanas pārbaudiet, vai jūsu izmantotā sistēma atbilst minimālajām tīkla, aparatūras un programmatūras prasībām vai pārsniedz tās.


## <a name="supported-microsoft-office-applications"></a>Atbalstītās Microsoft Office programmas
Finance and Operations mākoņa un lokālajos izvietojumos tiek atbalstītas tālāk norādītās Office programmas.
-   Lai palaistu Microsoft Excel un Word pievienojumprogrammas, jābūt instalētai programmai Microsoft Office 2016 operētājsistēmai Windows vai Mac. Plašāku informāciju par versijas prasībām skatiet sadaļā [Office integrācijas problēmu novēršana](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Lai skatītu dokumentus, kas izveidoti, izmantojot funkcijas Eksportēt programmā Excel vai Eksportēt programmā Word, ir jābūt instalētai programmai Microsoft Office 2007 vai jaunākai versijai.

# <a name="system-requirements-specific-to-cloud-deployments"></a>Mākoņa izvietojumiem specifiskās sistēmas prasības
## <a name="network-requirements"></a>Tīkla prasības
-   Programma Finance and Operations ir izstrādāta tīkliem, kuru latentums nepārsniedz 250–300 milisekundes (ms). Tas ir latentums no pārlūkprogrammas klienta līdz Microsoft Azure datu centram, kurā tiek viesota programmatūra Finance and Operations. Ieteicams pārbaudīt tīkla latentumu vietnē <http://www.azurespeed.com>.
-   Joslas platuma prasības programmai Finance and Operations ir atkarīgas no scenārija. Tipiskākajiem scenārijiem ir nepieciešams joslas platums, kas ir lielāks par 50 kilobaitiem sekundē (KB/s). Tomēr scenārijiem, kuriem ir augstas lietderīgās slodzes prasības, piemēram, darbvietām, vai scenārijiem, kuru ietvaros tiek veikta plaša pielāgošana, ieteicams izmantot lielāku joslas platumu.

Parasti programmatūra Finance and Operations ir optimizēta internetam. Ciklu skaits no pārlūkprogrammas klienta uz Azure datu centru ir pavisam neliels, un visa lietderīgā slodze tiek saspiesta. 

> [!WARNING]
> Neaprēķiniet nepieciešamo joslas platumu no klienta novietojuma, reizinot lietotāju skaitu ar minimālo nepieciešamo joslas platumu. Noteikta novietojuma vienlaicīgu izmantošanu ir ļoti grūti aprēķināt. Debitoriem, kurus uztrauc joslas platuma prasības, izmantojiet Finance and Operations priekšskatījuma versiju.

## <a name="net-framework-requirements"></a>.NET Framework prasības
Programmai Finance and Operations ir nepieciešama .NET Framework versija 4.6.2 visām viena klikšķa programmām, piemēram, dokumentu maršrutēšanas aģentam. Instalācijas instrukcijas skatiet sadaļā [.NET Framework instalācija](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>Atbalstītās tīmekļa pārlūkprogrammas
Tīmekļa programmu var palaist jebkurā no tālāk uzskaitītajām tīmekļa pārlūkprogrammām, kas darbojas norādītajās operētājsistēmās.


-   Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10
-   Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
-   Google Chrome (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatorā
-   Apple Safari (jaunākā publiski pieejamā versija) operētājsistēmā Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) vai Apple iPad

Lai atrastu katras tīmekļa pārlūkprogrammas visjaunāko laidienu, dodieties uz programmatūras ražotāja vietni. 

> [!NOTE]
> -   Lai uzdevumu ierakstītājam atļautu ekrānuzņēmuma attēlu tveršanu un iekļaušanu ģenerētajos Microsoft Word dokumentos, jāinstalē Chrome paplašinājuma pirmsizlaides versija. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Darbplūsmas redaktors tiek startēts kā ClickOnce programma. ClickOnce programmas atbalsta tikai Microsoft Edge un Internet Explorer (atbalstītā Microsoft Windows versijā). Darbplūsmas redaktora ClickOnce programmai ir nepieciešama 64 bitu saderīga operētājsistēma.
> -   Pārskatu noformētājs finanšu pārskatiem tiek startēts kā ClickOnce programma. Tam ir nepieciešama 64 bitu saderīga operētājsistēma. Ja lietojat pārlūkprogrammu Chrome, lai varētu lejupielādēt pārskatu veidošanas klientu, ir jāinstalē paplašinājums ClickOnce. Ja lietojat pārlūkprogrammu Chrome inkognito režīmā, pārliecinieties, ka paplašinājums ClickOnce ir arī iespējots inkognito režīmā.
> -   Lai priekšskatītu PDF failus, ieteicams izmantot modernas pārlūkprogrammas, piemēram, Microsoft Edge (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10 vai Google Chrome (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatoros.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS atbalstītās tīmekļa pārlūkprogrammas

Retail Cloud POS var palaist jebkurā no tālāk uzskaitītajām tīmekļa pārlūkprogrammām, kas darbojas norādītajās operētājsistēmās.

-   Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10
-   Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
-   Chrome (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10, Windows 8.1 vai Windows 7

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS prasības
### <a name="supported-operating-systems"></a>Atbalstītās operētājsistēmas

-   Retail Modern POS ir 32 bitu programma, taču tā darbojas gan x86, gan x64 arhitektūrā.
-   Programma Retail Modern POS tiek atbalstīta tikai operētājsistēmā Windows 10 Pro, Enterprise un Enterprise Long Term Servicing Branch (LTSB) versijās.

### <a name="minimum-system-requirements"></a>Minimālās sistēmas prasības

-   Minimālā atbalstītā izšķirtspēja ir 1280 × 1024.
-   Datoram, kurā tiek izmantota programma Retail Modern POS, jāatbilst šādām prasībām:
    -   Tam jābūt vismaz divkodolu procesoram, kura takts frekvence ir vismaz 2 gigaherci (GHz).
    -   Tam jābūt vismaz 3 gigabaitiem (GB) RAM.
    -   Tam jābūt piekļuvei internetam.

## <a name="retail-hardware-station-requirements"></a>Retail hardware station prasības
### <a name="supported-operating-systems"></a>Atbalstītās operētājsistēmas

-   Retail hardware station ir 32 bitu programma, taču tā darbojas gan x86, gan x64 arhitektūrā.
-   Programma Retail hardware station tiek atbalstīta šādās operētājsistēmās:
    -   Windows 7 Professional, Enterprise un Ultimate versijas 
    
    > [!NOTE]
    > Operētājsistēma Windows 7 tiek atbalstīta tikai tad, ja sistēmā ir manuāli instalēta pārlūkprogramma Internet Explorer 11.

    -   Windows 8.1 1. atjauninājums Professional, Enterprise un Embedded versijas
    -   Windows 10 Pro, Enterprise un Enterprise LTSB versijas

### <a name="minimum-system-requirements"></a>Minimālās sistēmas prasības

Datoram ir jāatbilst visām sistēmas prasībām tālāk minēto vienumu instalēšanai un izmantošanai:

-   Interneta informācijas pakalpojumi (IIS)
-   Trešās puses aparatūra

## <a name="retail-store-scale-unit-requirements"></a>Retail Store Scale Unit prasības
### <a name="supported-operating-systems"></a>Atbalstītās operētājsistēmas

-   Retail Store Scale Unit ir 32 bitu programma, taču tā darbojas gan x86, gan x64 arhitektūrā.
-   Programma Retail Store Scale Unit tiek atbalstīta šādās operētājsistēmās:
    -   Windows 7 Professional, Enterprise un Ultimate versijas
    -   Windows 8.1 1. atjauninājums Professional, Enterprise un Embedded versijas
    -   Windows 10 Pro, Enterprise un Enterprise LTSB versijas

### <a name="minimum-system-requirements"></a>Minimālās sistēmas prasības

-   4 GB RAM
-   1,6 GHz maksimālais centrālā procesora ātrums katram kodolam (Ir jābūt vismaz diviem kodoliem.)
-   Vismaz 10 GB brīvās vietas (Kanāla datu bāzei var būt nepieciešams lielāks vietas daudzums.)

### <a name="recommended-system-requirements"></a>Ieteicamās sistēmas prasības

-   6 GB RAM
-   2,4 GHz i7 (vai ekvivalents) maksimālais centrālā procesora ātrums katram kodolam (Ieteicami vismaz četri kodoli.)
-   Vismaz 10 GB brīvās vietas (Kanāla datu bāzei var būt nepieciešams lielāks vietas daudzums.)

## <a name="connector-requirements"></a>Savienotāja prasības
### <a name="supported-operating-systems"></a>Atbalstītās operētājsistēmas

-   Microsoft Dynamics AX savienotājam ir divas atsevišķas instalēšanas programmas — **Async Server Connector service** un **Real-time service for Dynamics AX 2012 R3**.
-   Abi komponenti ir 32 bitu programmas, taču tie darbojas gan x86, gan x64 arhitektūrā.
-   Abi komponenti tiek atbalstīti šādas operētājsistēmās:
    -   Windows 7 Professional, Enterprise un Ultimate versijas
    -   Windows 8.1 1. atjauninājums Professional, Enterprise un Embedded versijas
    -   Windows 10 Pro, Enterprise un Enterprise LTSB versijas
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimālās sistēmas prasības

-   Ieteicams ar 2 GB vai 4 GB RAM
-   1,6 GHz maksimālais centrālā procesora ātrums katram kodolam (Ir jābūt vismaz diviem kodoliem.)
-   Vismaz 10 GB brīvās vietas (Kanāla datu bāzei var būt nepieciešams lielāks vietas daudzums.)

## <a name="requirements-for-development-on-local-vms"></a>Prasības izstrādei lokālās virtuālajās mašīnās
Informāciju par prasībām attiecībā uz izstrādi vietējās virtuālajās mašīnās (VM) skatiet sadaļā [VM, kuras darbojas lokāli](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>Sistēmas prasības lokālajiem izvietojumiem

## <a name="network-requirements"></a>Tīkla prasības
Finance and Operations (lokālā versija) var darboties tīklos, kas izmanto interneta protokola versiju 4 (IPv4) vai interneta protokola versiju 6 (IPv6). Plānojot sistēmu, ņemiet vērā tīkla vidi un ievērojiet tālāk norādītās vadlīnijas.

### <a name="network-response-time"></a>Tīkla atbildes laiks
Tālāk esošajā tabulā uzskaitītas minimālās tīkla prasības savienojuma izveidei starp tīmekļa pārlūkprogrammu un Application Object Server (AOS), kā arī savienojuma izveidei starp AOS un datu bāzi lokālā sistēmā.

| Vērtība     | Tīmekļa pārlūkprogramma un AOS | AOS un datu bāze                                            |
|-----------|--------------------|------------------------------------------------------------|
| Joslas platums | 50 KB/s lietotājam   | 100 MB/s                                                   |
| Latentums   | < 250–300 ms       | < 1 ms (tikai LAN). AOS un datu bāze ir jāizvieto līdzās. |

- Programma Finance and Operations (lokālā versija) ir izstrādāta tīkliem, kuru latentums nepārsniedz 250–300 milisekundes (ms). Tas ir latentums no pārlūkprogrammas klienta līdz datu centram, kurā tiek viesota programma Finance and Operations.
- Joslas platuma prasības programmai Finance and Operations (lokālajai versijai) ir atkarīgas no scenārija. Tipiskos scenārijos starp pārlūkprogrammu un Finance and Operations serveri ir nepieciešams joslas platums, kas ir lielāks par 50 kilobaitiem sekundē (KB/s). Tomēr scenārijiem, kuriem ir augstas lietderīgās slodzes prasības, piemēram, darbvietām, vai scenārijiem, kuru ietvaros tiek veikta plaša pielāgošana, ieteicams izmantot lielāku joslas platumu, un joslas platums tajos ir arī atkarīgs no lietojuma.
Netiek atbalstīti izvietojumi, kuros AOS un SQL Server datu bāze atrodas dažādos datu centros. AOS un SQL Server datu bāze ir jāizvieto līdzās. Programma Finance and Operations ir optimizēta tā, lai samazinātu ciklu skaitu no pārlūkprogrammas uz serveri. Ciklu skaits no pārlūkprogrammas klienta uz datu centru ir nulle vai viens katrai lietotāja darbībai, un lietderīgā slodze tiek saspiesta.

> [!WARNING]
> Neaprēķiniet nepieciešamo joslas platumu no klienta novietojuma, reizinot lietotāju skaitu ar minimālo nepieciešamo joslas platumu. Noteikta novietojuma vienlaicīgu izmantošanu ir ļoti grūti aprēķināt. Kā labāko veiktspējas mērījumu jūsu specifiskajam gadījumam ieteicams izmantot reāllaika simulāciju Finance and Operations videi, kas nav ražošanas vide. 

### <a name="lan-environments"></a>LAN vides
Lokālā tīkla (LAN) vidēs savienojuma izveidei ar Finance and Operations nav nepieciešama Microsoft attālā darbvirsma operētājsistēmā Microsoft Windows Server. Tomēr tā var būt nepieciešama apkalpošanas operācijām virtuālajās mašīnās, kas veido servera izvietojumus.

### <a name="wan-environments"></a>WAN vides
Plaša apgabala tīkla (WAN) vidēs savienojuma izveidei ar Finance and Operations nav nepieciešama attālā darbvirsma operētājsistēmā Windows Server.

### <a name="internet-connectivity-requirements"></a>Interneta savienojamības prasības
Programmai Finance and Operations (lokālajai versijai) nav nepieciešama interneta savienojamība no lietotāju darba stacijām. Tomēr bez interneta savienojuma nebūs pieejami daži līdzekļi.

| Pārlūkprogrammas klients | Iekštīkla scenārijs bez interneta savienojamības ir noformēšanas punkts lokālā izvietojuma opcijai. Daži līdzekļi, kam nepieciešami mākoņpakalpojumi, piemēram, palīdzības un uzdevuma ceļvežu bibliotēkas pakalpojumā LCS, nebūs pieejami. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Serveris         | AOS vai Service Fabric pakāpei ir jāspēj sazināties ar LCS. Lokālajam pārlūkprogrammas klientam nav nepieciešama piekļuve internetam.                                                                                |
| Telemetrija      | Ja savienojumā ir ilgi pārtraukumi, var tikt pazaudēti telemetrijas dati. Pārtraukumi savienojumā ar LCS neietekmē lokālās programmas funkcionalitāti.                                                |
| LCS            | Savienojums ar LCS ir nepieciešams izvietošanas, kodu izvietošanas un apkalpošanas operācijām.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemetrijas datu pārsūtīšana uz mākoni
Lielākā daļa telemetrijas datu tiek glabāta lokāli un tai var piekļūt, izmantojot Microsoft Windows notikumu skatītāju. Neliela telemetrijas notikumu apakškopa tiek nosūtīta uz Microsoft telemetrijas konveijeru mākonī diagnostikas nolūkiem. Korporācijai Microsoft nosūtītie telemetrijas dati neietver debitoru datus un lietotājus identificējošus datus. Korporācijai Microsoft tiek nosūtīti VM nosaukumi, lai palīdzētu veikt vides pārvaldību un diagnostiku no LCS portāla.

## <a name="domain-requirements"></a>Domēna prasības
Instalējot Finance and Operations (lokālo versiju), ņemiet vērā tālāk norādītās domēna prasības.

- Virtuālajām mašīnām, kas vieso Finance and Operations (lokālās versijas) komponentus, ir jāpieder Active Directory domēnam. Domēna pakalpojumam Active Directory (AD DS) ir jābūt konfigurētam vietējā režīmā.
- Virtuālajām mašīnām, kas darbina Finance and Operations (lokālās versijas) komponentus, ir jābūt savstarpējai piekļuvei un konfigurētām domēna pakalpojumā Active Directory. 
- Domēna kontrollerim ir jādarbojas operētājsistēmā Microsoft Windows Server 2016.

## <a name="hardware-requirements"></a>Aparatūras prasības
Šajā sadaļā ir aprakstīta aparatūra, kas nepieciešama Finance and Operations (lokālās versijas) darbināšanai.
Faktiskās aparatūras prasības atšķiras atkarībā no sistēmas konfigurācijas, datu salikuma, kā arī programmām un līdzekļiem, ko izlemjat izmantot. Tālāk norādīti daži faktori, kas var ietekmēt programmai Finance and Operations (lokālajai versijai) atbilstošās aparatūras izvēli.

- Transakciju skaits stundā.
- Vienlaicīgo lietotāju skaits.

## <a name="minimum-infrastructure-requirements"></a>Minimālās infrastruktūras prasības
Finance and Operations (lokālā versija) izmanto Microsoft Azure Service Fabric, lai viesotu AOS, partijas, datu pārvaldības, pārvaldības pārskatu sastādītāja un vides vadības moduļa pakalpojumus. Microsoft SQL Server pārskatu izveides pakalpojumi (SSRS) netiek viesoti Service Fabric klasterī.
Programma SQL Server ir jāiestata augstas pieejamības HADRON iestatījumā, kurā ir vismaz divi mezgli ražošanai.
Tālāk esošajā attēlā parādīts minimālais ieteicamais mezglu skaits Service Fabric klasterī.

[![Ieteicamais mezglu skaits Service Fabric klasterim](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Procesora un RAM prasības
Tālāk esošajā tabulā norādīts procesoru skaits un brīvpiekļuves atmiņas (RAM) apjoms, kas nepieciešams katrai šī izvietojuma opcijas darbināšanai nepieciešamajai lomai. Lai iegūtu papildinformāciju, izlasiet minimālo prasību ieteikumus Service Fabrice savrupajam klasterim rakstā [Service Fabric klastera plānošana un sagatavošana](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Ja tajā pašā datorā ir instalēta cita Microsoft programmatūra, sistēmai ir jāatbilst arī šīs programmatūras aparatūras prasībām. Citas servera programmas tajā pašā datorā ieteicams ierobežot kā AOS līdz 1 gigabaitam (GB) RAM.

**Lieluma maiņa pēc lomas un topoloģijas tipa**

| Topoloģija   | Loma (mezgla tips)              | Ieteicamie procesora kodoli | Ieteicamā atmiņa (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| Ražošana | AOS, datu pārvaldība, partija   | 8.                           | 24                      |
|            | Pārvaldības pārskata sastādītājs           | 4.                           | 16.                      |
|            | SQL Server pārskatu izveides pakalpojumi (SSRS) | 4.                           | 16.                      |
|            | Vadības modulis                  | 4.                           | 16.                      |
| Smilškaste    | AOS, datu pārvaldība, partija   | 4.                           | 24                      |
|            | Pārvaldības pārskata sastādītājs           | 4.                           | 16.                      |
|            | SQL Server pārskatu izveides pakalpojumi (SSRS) | 4.                           | 16.                      |
|            | Vadības modulis                  | 4.                           | 16.                      |

**Minimālā lieluma aprēķini ražošanas un smilškastes izvietojumiem**\*

| Topoloģija                                  | Loma                          | Instanču skaits |
|-------------------------------------------|-------------------------------|---------------------|
| Ražošana                                | AOS (datu pārvaldība, partija)  | 3.                   |
|                                           | Pārvaldības pārskata sastādītājs           | 2.                   |
|                                           | SQL Server pārskatu izveides pakalpojumi (SSRS) | 1.                   |
|                                           | Vadības modulis\*\*                | 3.                   |
| Smilškaste                                   | AOS, datu pārvaldība, partija   | 2.                   |
|                                           | Pārvaldības pārskata sastādītājs           | 1.                   |
|                                           | SQL Server pārskatu izveides pakalpojumi (SSRS) | 1.                   |
|                                           | Vadības modulis                  | 3.                   |
| *Kopsavilkuma ražošanas un smilškastes topoloģijas* |                               | 16.                  |

\*Šos skaitļus pārbauda mūsu priekšskatījuma klienti, un tie var tikt koriģēti atbilstoši sniegtajām atsauksmēm.

\*\*Vadības modelis ir izstrādāts kā primārā mezgla tips un tiks izmantots arī Service Fabric pakalpojumu darbināšanai.

**Aizmugursistēmas SQL Server un AD sākotnējie aprēķini**

[![Aizmugursistēmas SQL Server un AD sākotnējie aprēķini](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*SQL Server lielumi ir ļoti atkarīgi no darba slodzēm. Papildinformāciju skatiet sadaļā [Aparatūras lieluma maiņa lokālām vidēm](#Hardware-sizing-for-on-premises-environments).

## <a name="storage"></a>Glabāšana

- **AOS** — Finance and Operations (lokālā versija) nestrukturētu datu glabāšanai izmantos servera ziņojumu bloka (SMB) 3.0 koplietojumu. Papildinformāciju skatiet rakstā [Storage Spaces Direct operētājsistēmā Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** — pieejamās opcijas.
    - Augstas pieejamības cietvielu diska (SSD) iestatījumi.
    - Krātuves apgabala tīkls (SAN), kas optimizēts OLTP caurlaidēm.
    - Augstas veiktspējas tieši pievienotā krātuve (DAS) 
- **SQL un datu pārvaldības IOPS** — gan datu pārvaldības, gan SQL Server krātuvei ir jābūt vismaz 2000 ievades/izvades operācijām sekundē (IOPS). Ražošanas IOPS ir atkarīga no daudziem faktoriem. Papildinformāciju skatiet sadaļā Aparatūras lieluma maiņa lokālām vidēm. 
- **Virtuālās mašīnas IOPS** — katrai virtuālajai mašīnai ir jābūt vismaz 100 rakstīšanas IOPS.

## <a name="virtual-host-requirements"></a>Virtuālā resursdatora prasības
Kad Finance and Operations (lokālās versijas) videi iestatāt virtuālos resursdatorus, skatiet šīs vadlīnijas: [Service Fabric klastera plānošana un sagatavošana](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) un [Service Fabric klastera aprakstīšana](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Katram virtuālajam resursdatoram ir jābūt pietiekamam kodolu skaitam infrastruktūrai, kuras lielums tiek pielāgots. Ir iespējamas vairākas uzlabotas konfigurācijas, kurās SQL Server atrodas fiziskā aparatūrā, bet pārējais ir virtualizēts. Ja programma SQL Server ir virtualizēta, diska apakšsistēmai ir jābūt ātram SAN vai tā ekvivalentam. Visos gadījumos pārliecinieties, vai virtuālā resursdatora pamatiestatījumi ir ar augstu pieejamību un redundanti. Visos gadījumos, kad tiek izmantota virtualizācija, nedrīkst veikt nekādus VM momentuzņēmumus.

## <a name="software-requirements-for-all-server-computers"></a>Programmatūras prasības visiem servera datoriem
Pirms jebkuru Finance and Operations (lokālās versijas) komponentu instalēšanas datorā ir jābūt instalētai tālāk norādītajai programmatūrai.

- Microsoft .NET Framework 4.5.1 vai jaunāka versija
- Papildinformāciju par Service Fabric skatiet rakstā [Service Fabric klastera plānošana un sagatavošana](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Atbalstītās servera operētājsistēmas
Tālāk esošajā tabulā uzskaitītas servera operētājsistēmas, kas tiek atbalstītas Finance and Operations komponentiem.

| Operētājsistēma                                     | Piezīmes                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter vai Standard | Šīs prasības attiecas uz datu bāzi un Service Fabric klasteri, kas vieso AOS. |

## <a name="software-requirements-for-database-servers"></a>Programmatūras prasības datu bāzes serveriem

- Tiek atbalstītas tikai SQL Server 2016 64 bitu versijas.
- Ražošanas vidē ieteicams instalēt jaunāko kumulatīvo atjauninājumu (CU) izmantotajai SQL Server versijai.
- Finance and Operations (lokālā versija) atbalsta unikoda komplektēšanu, kas nav reģistrjutīga, ir izcēlumjutīga, ir kanas rakstzīmju jutīga un nav platumjutīga. Komplektēšanai ir jāatbilst to datoru Windows lokalizācijai, kas darbina AOS instances. Ja iestatāt jaunu instalāciju, ieteicams izvēlēties Windows komplektēšanu, nevis SQL Server komplektēšanu. Papildinformāciju par komplektēšanas izvēli SQL Server datu bāzei skatiet rakstā [SQL Server dokumentācija](/sql/sql-server/sql-server-technical-documentation).
Tālāk esošajā tabulā uzskaitītas SQL Server versijas, kas tiek atbalstītas Finance and Operations datu bāzēm. Lai iegūtu papildinformāciju, skatiet [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016) minimālās aparatūras prasības.

| Vajadzība                                                      | Piezīmes                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition vai Enterprise Edition | SQL Server 2016 aparatūras prasības skatiet rakstā [Aparatūras un programmatūras prasības SQL Server 2016 instalēšanai](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>Programmatūras prasības klienta datoriem
Finance and Operations tīmekļa programma var darboties jebkurā ierīcē, kurā ir ar HTML5.0 saderīga tīmekļa pārlūkprogramma. Tālāk norādītas noteiktas ierīču/pārlūkprogrammu kombinācijas, ko apstiprinājusi korporācija Microsoft.

- Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10
- Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
- Google Chrome (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatorā
- Apple Safari (jaunākā publiski pieejamā versija) operētājsistēmā Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) vai Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Programmatūras prasības Active Directory federācijas pakalpojumam 
Active Directory federācijas pakalpojums (AD FS) vai Windows Server 2016

Domēna kontrollerim ir jābūt Windows Server 2012 R2 vai jaunākai versijai ar domēna funkcionēšanas līmeni 2012 R2 vai lielāku līmeni

Papildinformāciju par domēnu funkcionēšanas līmeņiem skatiet šeit: 
- [Kas ir Active Directory funkcionēšanas līmeņi](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Domēna pakalpojuma Active Directory funkcionēšanas līmeņu izprašana](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Aparatūras un programmatūras prasības Retail komponentiem
Finance and Operations (lokālā versija) pašlaik neietver Retail komponentus.

<a name="see-also"></a>Skatiet arī
--------

[Iegūt Dynamics 365 for Finance and Operations izdevuma Enterprise iepazīšanās kopiju](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

