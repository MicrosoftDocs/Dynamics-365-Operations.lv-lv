---
title: "Sistēmas prasības lokālajiem izvietojumiem"
description: "Šajā tēmā ir uzskaitītas sistēmas prasības pašreizējai Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma versijai lokālajiem izvietojumiem."
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 73fefd43c9de917dc6c98b2a6893b36a5c0ccdc5
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>Sistēmas prasības lokālajiem izvietojumiem

[!include[banner](../includes/banner.md)]

Šajā tēmā ir uzskaitītas sistēmas prasības pašreizējai Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma versijai lokālajiem izvietojumiem. Pirms Finance and Operations instalēšanas, ja nepieciešams, pārbaudiet, vai jūsu izmantotā sistēma atbilst minimālajām tīkla, aparatūras un programmatūras prasībām vai pārsniedz tās.

## <a name="network-requirements"></a>Tīkla prasības
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (lokālā versija) darbojas tīklos, kas izmanto Internet Protocol Version 4 (IPv4) vai Internet Protocol Version 6 (IPv6). Plānojot sistēmu, ņemiet vērā tīkla vidi un ievērojiet tālāk norādītās vadlīnijas.

### <a name="network-response-time"></a>Tīkla atbildes laiks
Tālāk esošajā tabulā uzskaitītas minimālās tīkla prasības savienojuma izveidei starp tīmekļa pārlūkprogrammu un Application Object Server (AOS), kā arī savienojuma izveidei starp AOS un datu bāzi lokālā sistēmā.

| Vērtība     | Tīmekļa pārlūkprogramma un AOS                      | AOS un datu bāze |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| Joslas platums | 50 kilobaiti sekundē (KB/s) katram lietotājam | 100 megabaiti sekundē (MB/s) |
| Latentums   | Mazāk nekā 250–300 milisekundes (ms)     | Mazāk nekā 1 ms (tikai lokālais tīkls [LAN]). AOS un datu bāze ir jāizvieto līdzās. |

- Programma Finance and Operations (lokālā versija) ir izstrādāta tīkliem, kuru latentums nepārsniedz 250–300 milisekundes (ms). Tas ir latentums no pārlūkprogrammas klienta līdz datu centram, kurā tiek viesota programma Finance and Operations.
- Joslas platuma prasības programmai Finance and Operations (lokālajai versijai) ir atkarīgas no scenārija. Tipiskos scenārijos starp pārlūkprogrammu un Finance and Operations serveri ir nepieciešams joslas platums, kas ir lielāks par 50 KB/s. Tomēr scenārijiem, kuriem ir augstas lietderīgās slodzes prasības, piemēram, scenārijiem, kuros ir ietvertas darbvietas vai kuru ietvaros tiek veikta plaša pielāgošana, ieteicams izmantot lielāku joslas platumu. Konkrētais joslas platums ir atkarīgs no lietojuma.

Netiek atbalstīti izvietojumi, kuros AOS un Microsoft SQL Server datu bāze atrodas dažādos datu centros. AOS un SQL Server datu bāze ir jāizvieto līdzās. 

Programma Finance and Operations ir optimizēta tā, lai samazinātu ciklu skaitu no pārlūkprogrammas uz serveri. Ciklu skaits no pārlūkprogrammas klienta uz datu centru ir nulle vai viens katrai lietotāja darbībai, un lietderīgā slodze tiek saspiesta.

> [!WARNING]
> Neaprēķiniet nepieciešamo joslas platumu no klienta novietojuma, reizinot lietotāju skaitu ar minimālo nepieciešamo joslas platumu. Noteikta novietojuma vienlaicīgu izmantošanu ir ļoti grūti aprēķināt. Kā labāko veiktspējas mērījumu jūsu specifiskajam gadījumam ieteicams izmantot reāllaika simulāciju Finance and Operations videi, kas nav ražošanas vide. 

### <a name="lan-environments"></a>LAN vides
LAN vidēs savienojuma izveidei ar Finance and Operations nav nepieciešama Microsoft attālā darbvirsma operētājsistēmā Microsoft Windows Server. Tomēr var būt nepieciešama attālā darbvirsma apkalpošanas operācijām virtuālajās mašīnās (VMs), kas veido servera izvietojumus.

### <a name="wan-environments"></a>WAN vides
Plaša apgabala tīkla (WAN) vidēs savienojuma izveidei ar Finance and Operations nav nepieciešama attālā darbvirsma operētājsistēmā Windows Server.

### <a name="internet-connectivity-requirements"></a>Interneta savienojamības prasības
Programmai Finance and Operations (lokālajai versijai) nav nepieciešama interneta savienojamība no lietotāju darba stacijām. Tomēr bez interneta savienojuma nebūs pieejami daži līdzekļi.

|                    |   |
|--------------------|---|
| **Pārlūkprogrammas klients** | Iekštīkla scenārijs bez interneta savienojamības ir noformēšanas punkts lokālā izvietojuma opcijai. Daži līdzekļi, kam nepieciešami mākoņpakalpojumi, piemēram, palīdzības un uzdevuma ceļvežu bibliotēkas pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) nebūs pieejami. |
| **Serveri**         | AOS vai Microsoft Azure Service Fabric pakāpei ir jāspēj sazināties ar LCS. Lokālajam pārlūkprogrammas klientam nav nepieciešama piekļuve internetam. |
| **Telemetrija**      | Ja savienojumā ir ilgi pārtraukumi, var tikt pazaudēti telemetrijas dati. Pārtraukumi savienojumā ar LCS neietekmē lokālās programmas funkcionalitāti. |
| **LCS**            | Savienojums ar LCS ir nepieciešams izvietošanas, kodu izvietošanas un apkalpošanas operācijām. |

## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemetrijas datu pārsūtīšana uz mākoni
Lielākā daļa telemetrijas datu tiek glabāta lokāli un tai var piekļūt, izmantojot Microsoft Windows notikumu skatītāju. Neliela telemetrijas notikumu apakškopa tiek nosūtīta uz Microsoft telemetrijas konveijeru mākonī diagnostikas nolūkiem. Korporācijai Microsoft nosūtītie telemetrijas dati neietver debitoru datus un lietotājus identificējošus datus. Korporācijai Microsoft tiek nosūtīti VM nosaukumi, lai palīdzētu veikt vides pārvaldību un diagnostiku no LCS portāla.

## <a name="domain-requirements"></a>Domēna prasības
Instalējot Finance and Operations (lokālo versiju), ņemiet vērā tālāk norādītās domēna prasības.

- Virtuālajām mašīnām, kas vieso Finance and Operations (lokālās versijas) komponentus, ir jāpieder Active Directory domēnam. Domēna pakalpojumam Active Directory (AD DS) ir jābūt konfigurētam vietējā režīmā.
- Virtuālajām mašīnām, kurās darbojas Finance and Operations (lokālās versijas) komponenti, ir nepieciešama savstarpēja piekļuve. Šī piekļuve ir konfigurēta AD DS. 
- Domēna kontrollerim ir jābūt Microsoft Windows Server 2012 R2 vai jaunākai versijai ar domēna funkcionēšanas līmeni 2012 R2 vai lielāku līmeni

## <a name="hardware-requirements"></a>Aparatūras prasības
Šajā sadaļā ir aprakstīta aparatūra, kas nepieciešama Finance and Operations (lokālās versijas) darbināšanai.

Faktiskās aparatūras prasības atšķiras atkarībā no sistēmas konfigurācijas, datu salikuma, kā arī programmām un līdzekļiem, ko izlemjat izmantot. Tālāk norādīti daži faktori, kas var ietekmēt programmai Finance and Operations (lokālā versija) atbilstošās aparatūras izvēli.

- Transakciju skaits stundā
- Vienlaicīgo lietotāju skaits

## <a name="minimum-infrastructure-requirements"></a>Minimālās infrastruktūras prasības
Finance and Operations (lokālā versija) izmanto Service Fabric, lai viesotu AOS, partijas, datu pārvaldības, pārvaldības pārskatu sastādītāja un vides vadības moduļa pakalpojumus. 

Programma SQL Server ir jāiestata augstas pieejamības HADRON iestatījumā, kurā ir vismaz divi mezgli ražošanai.

Tālāk esošajā attēlā parādīts minimālais ieteicamais mezglu skaits Service Fabric klasterī.

[![Ieteicamais mezglu skaits Service Fabric klasterim](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Procesora un RAM prasības
Tālāk esošajā tabulā norādīts procesoru skaits un brīvpiekļuves atmiņas (RAM) apjoms, kas nepieciešams katrai šī izvietojuma opcijas darbināšanai nepieciešamajai lomai. Lai iegūtu papildinformāciju, izlasiet minimālo prasību ieteikumus Service Fabric savrupajam klasterim rakstā [Service Fabric klastera plānošana un sagatavošana](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Ja tajā pašā datorā ir instalēta cita Microsoft programmatūra, sistēmai ir jāatbilst arī šīs programmatūras aparatūras prasībām. Ja tajā pašā datorā, kurā ir instalēts AOS, ir instalētas citas servera programmas, ieteicams ierobežot šādas servera programmas līdz 1 gigabaitam (GB) RAM.

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

**Minimālā lieluma aprēķini ražošanas un smilškastes izvietojumiem\***

| Topoloģija                                        | Loma                          | Instanču skaits |
|-------------------------------------------------|-------------------------------|---------------------|
| Ražošana                                      | AOS (datu pārvaldība, partija)  | 3.                   |
|                                                 | Pārvaldības pārskata sastādītājs           | 2.                   |
|                                                 | SQL Server pārskatu izveides pakalpojumi (SSRS) | 1.                   |
|                                                 | Vadības modulis\*\*              | 3.                   |
| Smilškaste                                         | AOS, datu pārvaldība, partija   | 2.                   |
|                                                 | Pārvaldības pārskata sastādītājs           | 1.                   |
|                                                 | SQL Server pārskatu izveides pakalpojumi (SSRS) | 1.                   |
|                                                 | Vadības modulis                  | 3.                   |
| *Kopsavilkuma ražošanas un smilškastes topoloģijas* |                               | *16*                |

\*Šajā tabulā sniegtos rādītājus apstiprina mūsu priekšskatījuma klienti, un tie var tikt koriģēti, pamatojoties uz šo klientu sniegtām atsauksmēm.

\*\* Vadības modelis ir izstrādāts kā primārā mezgla tips un tiks izmantots arī Service Fabric pakalpojumu darbināšanai.

**Aizmugursistēmas SQL Server un AD sākotnējie aprēķini**

<table>
<thead>
<tr>
<th></th>
<th>Loma</th>
<th>Virtuālās mašīnas/instances</th>
<th>Kodoli</th>
<th>Kopējais kodolu skaits</th>
<th>Atmiņa vienā instancē (GB)</th>
<th>Kopējā atmiņa (GB)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Koplietojamā infrastruktūra</strong></td>
<td>SQL Server*</td>
<td>2.</td>
<td>8.</td>
<td>16.</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>Failu serveris/Krātuves apgabala tīkls/Īpaši pieejama krātuve</td>
<td colspan="5"><p>Aizmugursistēmas krātuves pamatā jābūt cietvielu diskiem (SSDs) izpildlaika krātuves apgabala tīklā (SAN).</p>
<p>Izmēra un ievades/izvades darbību skaita sekundē (IOPS) caurlaidspējas pamatā ir darba noslodzes apjoms.</p></td>
</tr>
<tr>
<td>Active Directory</td>
<td>3.</td>
<td>4.</td>
<td>12.</td>
<td>16.</td>
<td>48</td>
</tr>
<tr>
<td><em>Kopsavilkums par koplietojamo infrastruktūru</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\*SQL Server lielumi ir ļoti atkarīgi no darba slodzēm. Papildinformāciju skatiet šeit: [Aparatūras lieluma maiņa lokālām vidēm](hardware-sizing-on-premises-environments.md).

## <a name="storage"></a>Glabāšana

- **AOS** — Finance and Operations (lokālā versija) nestrukturētu datu glabāšanai izmanto servera ziņojumu bloka (SMB) 3.0 koplietojumu. Papildinformāciju skatiet rakstā [Storage Spaces Direct operētājsistēmā Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** — Pieejamas šādas opcijas:

    - Augstas pieejamības SSD iestatījumi
    - SAN, optimizēts tiešsaistes transakciju apstrādes (OLTP) caurlaidēm
    - Augstas veiktspējas tieši pievienotā krātuve (DAS) 

- **SQL Server un datu pārvaldības IOPS** — gan datu pārvaldības, gan SQL Server krātuvei ir jābūt vismaz 2000 ievades/izvades operācijām sekundē (IOPS). Ražošanas IOPS ir atkarīga no daudziem faktoriem. Papildinformāciju skatiet šeit: [Aparatūras lieluma maiņa lokālām vidēm](hardware-sizing-on-premises-environments.md).
- **VM IOPS** — katrai virtuālajai mašīnai nepieciešami vismaz 100 rakstīšanas IOPS.

## <a name="virtual-host-requirements"></a>Virtuālā resursdatora prasības
Kad Finance and Operations (lokālā versija) videi iestatāt virtuālos resursdatorus, skatiet šīs vadlīnijas: [Service Fabric klastera plānošana un sagatavošana](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) un [Service Fabric klastera aprakstīšana](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Katram virtuālajam resursdatoram ir jābūt pietiekamam kodolu skaitam infrastruktūrai, kuras lielums tiek pielāgots. Ir iespējamas vairākas uzlabotas konfigurācijas, kurās SQL Server atrodas fiziskā aparatūrā, bet pārējais ir virtualizēts. Ja programma SQL Server ir virtualizēta, diska apakšsistēmai ir jābūt ātram SAN vai tā ekvivalentam. Visos gadījumos pārliecinieties, vai virtuālā resursdatora pamatiestatījumi ir ar augstu pieejamību un redundanti. Visos gadījumos, kad tiek izmantota virtualizācija, nedrīkst veikt nekādus VM momentuzņēmumus.

## <a name="software-requirements-for-all-server-computers"></a>Programmatūras prasības visiem servera datoriem
Pirms jebkuru Finance and Operations (lokālās versijas) komponentu instalēšanas datorā ir jābūt instalētai tālāk norādītajai programmatūrai.

- Microsoft .NET Framework versija 4.5.1 vai jaunākas versijas
- Service Fabric

Papildinformāciju par skatiet rakstā [Service Fabric klastera plānošana un sagatavošana](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Atbalstītās servera operētājsistēmas
Tālāk esošajā tabulā uzskaitītas servera operētājsistēmas, kas tiek atbalstītas Finance and Operations komponentiem.

| Operētājsistēma                                     | Piezīmes |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Datacenter vai Standard | Šīs prasības attiecas uz datu bāzi un Service Fabric klasteri, kas vieso AOS. |

## <a name="software-requirements-for-database-servers"></a>Programmatūras prasības datu bāzes serveriem

- Tiek atbalstītas tikai SQL Server 2016 64 bitu versijas.
- Ražošanas vidē ieteicams instalēt jaunāko kumulatīvo atjauninājumu (CU) izmantotajai SQL Server versijai.
- Finance and Operations (lokālā versija) atbalsta unikoda komplektēšanu, kas nav reģistrjutīga, ir izcēlumjutīga, ir kanas rakstzīmju jutīga un nav platumjutīga. Komplektēšanai ir jāatbilst to datoru Windows lokalizācijai, kas darbina AOS instances. Ja iestatāt jaunu instalāciju, ieteicams izvēlēties Windows komplektēšanu, nevis SQL Server komplektēšanu. Papildinformāciju par komplektēšanas izvēli SQL Server datu bāzei skatiet rakstā [SQL Server dokumentācija](/sql/sql-server/sql-server-technical-documentation).

Tālāk esošajā tabulā uzskaitītas SQL Server versijas, kas tiek atbalstītas Finance and Operations datu bāzēm. Lai iegūtu papildinformāciju, skatiet [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016) minimālās aparatūras prasības.

| Vajadzība                                                      | Piezīmes |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard Edition vai Enterprise Edition | SQL Server 2016 aparatūras prasības skatiet rakstā [Aparatūras un programmatūras prasības SQL Server 2016 instalēšanai](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-application-object-server-aos"></a>Programmatūras prasības programmas objektu serverim (AOS) 
- SQL Server integrācijas pakalpojumi (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>Programmatūras prasības pārskata serverim (BI)
- SQL Server pārskatu izveides pakalpojumi (SSRS)

## <a name="software-requirements-for-client-computers"></a>Programmatūras prasības klienta datoriem
Finance and Operations tīmekļa programma var darboties jebkurā ierīcē, kurā ir ar HTML 5.0 saderīga tīmekļa pārlūkprogramma. Tālāk norādītas noteiktas ierīču/pārlūkprogrammu kombinācijas, ko apstiprinājusi korporācija Microsoft.

- Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10
- Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
- Google Chrome (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatorā
- Apple Safari (jaunākā publiski pieejamā versija) operētājsistēmā Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) vai Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Programmatūras prasības Active Directory federācijas pakalpojumam 
Nepieciešams Active Directory federācijas pakalpojums (AD FS) vai Windows Server 2016

Domēna kontrollerim ir jābūt Windows Server 2012 R2 vai jaunākai versijai ar domēna funkcionēšanas līmeni 2012 R2 vai lielāku līmeni Papildinformāciju par domēnu funkcionēšanas līmeņiem skatiet šajās lapās:

- [Kas ir Active Directory funkcionēšanas līmeņi](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Domēna pakalpojuma Active Directory funkcionēšanas līmeņu izprašana](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>Atbalstītās Microsoft Office programmas
Finance and Operations mākoņa un lokālajos izvietojumos tiek atbalstītas tālāk norādītās Microsoft Office programmas.

-   Lai palaistu Microsoft Excel un Microsoft Word pievienojumprogrammas, jābūt instalētai programmai Microsoft Office 2016 operētājsistēmai Windows vai Mac. Plašāku informāciju par versijas prasībām skatiet sadaļā [Office integrācijas problēmu novēršana](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Lai skatītu dokumentus, kas izveidoti, izmantojot funkcijas Eksportēt programmā Excel vai Eksportēt programmā Word, ir jābūt instalētai programmai Microsoft Office 2007 vai jaunākai versijai.
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Aparatūras un programmatūras prasības Retail komponentiem
Finance and Operations (lokālā versija) pašlaik neietver Retail komponentus.

