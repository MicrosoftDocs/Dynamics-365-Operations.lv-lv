---
title: "Lokālu vižu iestatīšana un izvietošana"
description: "Šajā tēmā ir sniegta informācija par lokālās vides plānošanu, iestatīšanu un izvietošanu."
author: sarvanisathish
manager: AnnBe
ms.date: 08/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations, Unified Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d100f6dbcbdf8f4c12ab04670fb598a88d48d84b
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: lv-lv
ms.lasthandoff: 08/10/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>Lokālu vižu iestatīšana un izvietošana

Šajā dokumentā ir aprakstīts, kā plānot izvietojumu, iestatīt infrastruktūru un izvietot Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu (lokālo versiju).

## <a name="finance-and-operations-components"></a>Finance and Operations komponenti

Finance and Operations programmu veido trīs galvenie tālāk norādītie komponenti.

- Programmas objektu serveris (AOS)
- Biznesa informācija (BI)
- Finanšu pārskati/pārvaldības pārskatu sastādītājs

Šie komponenti ir atkarīgi no tālāk norādītās sistēmas programmatūras.

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 SP1 ar tālāk norādītajiem līdzekļiem.

    - Ir iespējota pilnteksta indeksa meklēšana.
    - SQL Server pārskatu izveides pakalpojumi (SSRS).
    - SQL Server integrācijas pakalpojumi (SSIS).
    
     > [!NOTE]
     > Programma darbosies tikai tad, ja būs iespējota pilnteksta meklēšana.

- SQL Server pārvaldības studija
- Savrups pakalpojums Microsoft Azure Service Fabric
- Windows PowerShell 5.0 vai jaunāka versija
- Active Directory federācijas pakalpojums (AD FS) vai Windows Server 2016

  Domēna kontrollerim ir jābūt Windows Server 2012 R2 vai jaunākai versijai ar domēna funkcionēšanas līmeni 2012 R2 vai lielāku līmeni

  Papildinformāciju par domēnu funkcionēšanas līmeņiem skatiet šeit: 
  - [Kas ir Active Directory funkcionēšanas līmeņi](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Domēna pakalpojuma Active Directory funkcionēšanas līmeņu izprašana](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

Finance and Operations biti tiek izplatīti, izmantojot pakalpojumu Microsoft Dynamics Lifecycle Services (LCS). Pirms izvietošanas jums kanālā [Līgumi Enterprise](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) ir jāiegādājas pirkšanas licences atslēgas un pakalpojumā LCS jāiestata lokāls projekts. Izvietojumus var uzsākt tikai ar pakalpojumu LCS. Papildinformāciju par lokālu projektu iestatīšanu pakalpojumā LCS skatiet rakstā [Lokāla projekta izveide pakalpojumā Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>Autentifikācija

Lokālā programma darbojas ar AD FS. Lai izmantotu LCS, jums ir jākonfigurē arī Azure Active Directory (Azure AD).

## <a name="standalone-service-fabric"></a>Savrups Service Fabric

Finance and Operations izmanto savrupu pakalpojumu Service Fabric. Papildinformāciju skatiet rakstā [Service Fabric dokumentācija](/azure/service-fabric/).

## <a name="infrastructure"></a>Infrastruktūra

Programma Finance and Operations ir izstrādāta darbam hiperkonverģētā arhitektūrā. Aparatūras konfigurācija ietver tālāk norādītos komponentus.

- Savrups Service Fabric klasteris, kura pamatā ir Windows Server 2016 virtuālās mašīnas (VM)
- SQL Server (tiek atbalstīts gan klasterveida SQL, gan AlwaysOn)
- AD FS autentifikācijai
- Servera ziņojumu bloka (SMB) 3. versijas failu koplietošana glabāšanai
- Neobligāti: Microsoft Office Server 2017

Papildinformāciju skatiet sadaļā [Sistēmas prasības](../get-started/system-requirements.md) un lieluma maiņas vadlīnijas.

### <a name="hardware-layout"></a>Aparatūras izkārtojums

Infrastruktūru un Service Fabric klasteri plānojiet, pamatojoties uz ieteikto lieluma maiņas informāciju rakstā [Aparatūras lieluma maiņa lokālām vidēm](../get-started/hardware-sizing-on-premises-environments.md). Papildinformāciju par Service Fabric klastera plānošanu skatiet rakstā [Service Fabric savrupā klastera izvietojuma plānošana un sagatavošana](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

Tālāk esošajā tabulā ir parādīts aparatūras izvietojuma piemērs. Šis piemērs ir izmantots viscaur šajā tēmā, lai ilustrētu iestatīšanas procesu.

> [!NOTE]
> Service Fabric klastera primārajam mezglam ir jābūt vismaz trīs mezgliem. Šajā piemērā **OrchestratorType** ir norādīts kā primārā mezgla tips.

| Mašīnas nolūks                                 | Mašīnas nosaukums    | IP adrese    |
|-------------------------------------------------|-----------------|---------------|
| Domēna kontrolleris                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Failu serveris                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL AlwaysOn klasteris                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| Klients                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Service Fabric klasteris/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Service Fabric klasteris/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Service Fabric klasteris/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Service Fabric klasteris/vadības modulis 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Service Fabric klasteris/vadības modulis 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Service Fabric klasteris/vadības modulis 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Service Fabric klastera/pārvaldības pārskatu sastādītāja mezgls | SQLAOSMR1       | 10.179.108.18 |
| Service Fabric klastera/SSRS mezgls                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Iestatīšana

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat iestatīšanu, ir jāizpilda tālāk norādītie priekšnosacījumi. Šo priekšnosacījumu atbilstošās iestatīšanas procedūras šajā dokumentā nav aplūkotas.

- Domēna pakalpojums Active Directory (AD DS) ir instalēts un konfigurēts jūsu tīklā.
- Ir izvietots pakalpojums AD FS.
- Ir instalēts SQL Server, SSRS un Management Studio.

### <a name="overview"></a>Pārskats

Lai iestatītu Finance and Operations infrastruktūru, ir jāveic tālāk norādītās darbības.

1. Domēna nosaukumu un DNS zonu plānošana
2. Sertifikātu plānošana un iegūšana
3. Lietotāju un pakalpojumu kontu plānošana
4. DNS zonu izveide un A ierakstu pievienošana
5. Virtuālo mašīnu pievienošana domēnam
6. Nepieciešamās programmatūras pievienošana virtuālajām mašīnām
7. Iestatīšanas skriptu lejupielāde no LCS
8. Konfigurācijas aprakstīšana
9. Sertifikātu instalēšana
10. Savrupa Service Fabric klastera iestatīšana
11. LCS savienojamības konfigurēšana nomniekam
12. Failu krātuves iestatīšana
13. SQL Server iestatīšana
14. Datu bāzu konfigurēšana
15. Akreditācijas datu šifrēšana
16. Iestatīt SSRS
17. AD FS konfigurēšana

### <a name="plan-your-domain-name-and-dns-zones"></a>Domēna nosaukumu un DNS zonu plānošana

AOS ražošanas instalācijai ieteicams izmantot publiski reģistrētu domēna nosaukumu. Šādi tai var piekļūt ārpus tīkla, ja ir nepieciešama piekļuve no ārpuses.

Piemēram, ja jūsu uzņēmuma domēns ir contoso.com, jūsu Finance and Operations (lokālās versijas) zona var būt d365ffo.onprem.contoso.com un resursdatoru nosaukumi var būt tālāk norādītie.

- ax.d365ffo.onprem.contoso.com: AOS mašīnām
- sf.d365ffo.onprem.contoso.com: Service Fabric klasterim

### <a name="plan-and-acquire-your-certificates"></a>Sertifikātu plānošana un iegūšana

Lai nodrošinātu Service Fabric klastera un visu izvietoto programmu aizsardzību, ir nepieciešami drošligzdu slāņa (SSL) sertifikāti. Ražošanas un smilškastes darba slodzēm ieteicams iegūt sertifikātus no sertificēšanas iestādes (CA), piemēram, [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) vai [GlobalSign](https://www.globalsign.com/en/ssl/). Ja jūsu domēns ir iestatīts ar [Active Directory sertifikātu pakalpojumu](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS), sertifikātus varat izveidot, izmantojot AD CS. Katram sertifikātam ir jāsatur privātā atslēga, kas tika izveidota atslēgu apmaiņai, un tam ir jābūt eksportējamam uz personiskās informācijas apmaiņas (.pfx) failu.

Pašparakstītus sertifikātus var izmantot tikai testēšanas nolūkos. Ērtības nolūkos iestatīšanas skripti ietver skriptus, kas ģenerē un eksportē pašparakstītus sertifikātus. Kā jau minēts, šos sertifikātus drīkst lietot tikai testēšanas nolūkos.

| Nolūks                                      | Paskaidrojums | Papildu prasības |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL sertifikāts                   | Šo sertifikātu izmanto, lai šifrētu datus, kas tiek pārsūtīti tīklā starp SQL Server instanci un klienta programmu. | <p>Sertifikāta domēna nosaukumam ir jāatbilst SQL Server instances vai uztvērēja pilnajam domēna nosaukumam (FQDN).</p><p>Piemēram, ja SQL uztvērējs tiek viesots mašīnā DAX7SQLAOSQLA, sertifikāta DNS nosaukums ir DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| Service Fabric servera sertifikāts            | Šo sertifikātu izmanto, lai palīdzētu aizsargāt mezgla-mezgla saziņu starp Service Fabric mezgliem. Šo sertifikātu izmanto arī kā servera sertifikātu, kurš tiek norādīts klientam, kas izveido savienojumu ar klasteri. | <p>Sertifikāta domēna nosaukumam ir jāatbilst DNS zonai, kurā tiek viesots AOS un Service Fabric.</p><p>Sertifikāta domēna nosaukums var būt, piemēram, \*.onprem.contoso.com or \*.contoso.com.</p><p>Ja izmantojat aizstājējzīmju sertifikātu, aizstājējzīme attiecas tikai uz vienu līmeni. Ja sertifikātam ir vairāk nekā viens līmenis (kā iepriekšējā piemērā ar \*.contoso.com), tam ir jālieto apakšdomēns, objekta alternatīvais nosaukums (SAN).</p> |
| Service Fabric klienta sertifikāts            | Šo sertifikātu izmanto klienti, lai skatītu un pārvaldītu Service Fabric klasteri. | |
| Šifrējuma sertifikāts                     | Šo sertifikātu izmanto, lai šifrētu sensitīvu informāciju, piemēram, SQL Server paroli un lietotāju kontu paroles. | <p>Sertifikāta atslēgas lietojumam ir jāietver datu šifrējums (10) un tas nedrīkst iekļaut servera autentifikāciju vai klienta autentifikāciju.</p><p>Papildinformāciju skatiet rakstā [Noslēpumu pārvaldība Service Fabric programmās](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| AOS SSL sertifikāts                          | <p>Šo sertifikātu izmanto kā servera sertifikātu, kas tiek norādīts klientam AOS tīmekļa vietnei. To izmanto arī Windows Communication Foundation (WCF)/vienkāršā objektpiekļuves protokola (SOAP) sertifikātu iespējošanai.</p><p>Service Fabric servera sertifikātu var šeit izmantot, ja tas ir aizstājējzīmju sertifikāts.</p> | <p>Sertifikāta domēna nosaukumam ir jāatbilst DNS zonai, kurā tiek viesots AOS un Service Fabric.</p><p>Sertifikāta domēna nosaukums var būt, piemēram, \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com vai \*.contoso.com.</p><p>Ja izmantojat aizstājējzīmju sertifikātu, aizstājējzīme attiecas tikai uz vienu līmeni. Ja sertifikātam ir vairāk nekā viens līmenis (kā iepriekšējā piemērā ar \*.contoso.com), tam ir jālieto apakšdomēns, SAN.</p> |
| Sesijas autentifikācijas sertifikāts           | Šo sertifikātu AOS izmanto, lai palīdzētu aizsargāt lietotāja sesijas informāciju. | Tas ir arī **failu koplietošanas** sertifikāts, kas tiks izmantots izvietošanas no LCS laikā. |
| Datu šifrēšanas un datu parakstīšanas sertifikāts | Šos sertifikātus AOS izmanto sensitīvas informācijas šifrēšanai. | |
| Finanšu pārskatu klienta sertifikāts       | Šo sertifikātu izmanto, lai palīdzētu aizsargāt saziņu starp finanšu pārskatu pakalpojumiem un AOS. | |
| Pārskatu sertifikāts                        | Šo sertifikātu izmanto, lai palīdzētu aizsargāt saziņu starp SSRS un AOS. | |
| Lokāli viesotā lokālā aģenta sertifikāts           | <p>Šo sertifikātu izmanto, lai palīdzētu aizsargāt saziņu starp lokāli viesoto lokālo aģentu un LCS.</p><p>Šis sertifikāts lokālajam aģentam ļauj rīkoties jūsu Azure AD nomnieka vārdā un sazināties ar LCS izvietojumu vadībai un pārraudzībai.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Lietotāju un pakalpojumu kontu plānošana

Lai programma Finance and Operations (lokālā versija) darbotos, jums ir jāizveido vairāki lietotāju vai pakalpojumu konti. Jums ir jāizveido grupas pārvaldīto pakalpojumu kontu (gMSA), domēna kontu un SQL kontu kombinācija. Tālāk esošajā tabulā parādīti lietotāju konti, to nolūks un šajā tēmā piemēros izmantotie nosaukumi.

| Lietotāja konts                                            | tips           | Nolūks | Lietotāja vārds |
|---------------------------------------------------------|----------------|---------|-----------|
| Finanšu pārskatu programmas pakalpojuma konts         | gMSA           |         | Contoso\\svc-FRAS$ |
| Finanšu pārskatu apstrādes pakalpojuma konts             | gMSA           |         | Contoso\\svc-FRPS$ |
| Finanšu pārskatu viena klikšķa noformētāja pakalpojuma konts | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS pakalpojuma konts                                     | gMSA           | Šis lietotājs ir jāizveido turpmākai korektūrai. Tiek plānots nākamajos laidienos AOS iespējot darbam ar gMSA. Šo lietotāju izveidojot iestatīšanas laikā, jūs palīdzēsit nodrošināt vieglu pāreju uz gMSA. | Contoso\\svc-AXSF$ |
| AOS pakalpojuma konts                                     | Domēna konts | AOS šo lietotāju izmanto GA laidienā. | Contoso\\AXServiceUser |
| AOS SQL datu bāzes administratora lietotājs                                   | SQL lietotājs       | Finance and Operations šo lietotāju izmanto autentifikācijai ar SQL\*. Šis lietotājs nākamajos laidienos tiks aizstāts ar gMSA lietotāju. | AXDBAdmin |
| Lokālā izvietojuma aģenta pakalpojuma konts                  | gMSA           | Šo kontu lokālais aģents izmanto, lai vadītu izvietojumu vairākos mezglos. | Contoso\\Svc-LocalAgent$ |

\* SQL autentifikācijas SQL lietotājvārds un parole ir aizsargāti, jo tie tiek šifrēti un glabāti failu koplietojumā.

### <a name="create-dns-zones-and-add-a-records"></a>DNS zonu izveide un A ierakstu pievienošana

DNS ir integrēts ar AD DS un ļauj kārtot, pārvaldīt un atrast resursus tīklā. Izveidojiet DNS turpvērstu meklēšanas zonu un A ierakstus AOS resursdatora nosaukumam un Service Fabric klasterim. Šajā piemērā DNS zonas nosaukums ir d365ffo.onprem.contoso.com un A ieraksti/resursdatoru nosaukumi ir:

- **ax**.d365ffo.onprem.contoso.com: AOS mašīnām
- **sf**.d365ffo.onprem.contoso.com: Service Fabric klasterim

#### <a name="add-a-dns-zone"></a>DNS zonas pievienošana

Lai pievienotu DNS zonu, veiciet tālāk norādīto procedūru.

1. Pierakstieties domēna kontrollera mašīnā, noklikšķiniet uz **Sākt** un startējiet DNS pārvaldnieku, ierakstot **dnsmgmt.msc**.
2. Ar peles labo pogu noklikšķiniet uz domēna kontrollera nosaukuma un pēc tam noklikšķiniet uz **Jauna zona** \> **Tālāk**.
3. Atlasiet vienumu **Primārā zona**.
4. Atstājiet izvēles rūtiņu **Glabāt zonu pakalpojumā Active Directory (šis iestatījums ir pieejams tikai tad, ja DNS serveris ir rakstāms domēna kontrolleris)** atzīmētu un pēc tam noklikšķiniet uz **Tālāk**.
5. Atlasiet vienumu **Visiem DNS serveriem, kas darbojas domēna kontrolleros šajā domēnā: Contoso.com** un pēc tam noklikšķiniet uz **Tālāk**.
6. Atlasiet vienumu **Turpvērsta meklēšanas zona** un pēc tam noklikšķiniet uz **Tālāk**.
7. Ievadiet zonas nosaukumu savam iestatījumam un pēc tam noklikšķiniet uz **Tālāk**. Ievadiet, piemēram, **d365ffo.onprem.contoso.com**.
8. Atlasiet vienumu **Neatļaut dinamiskos atjauninājumus** un pēc tam noklikšķiniet uz **Tālāk**.

#### <a name="set-up-an-a-record-for-aos"></a>A ieraksta iestatīšana serverim AOS

Jaunajā DNS zonā izveidojiet vienu A ierakstu ar nosaukumu **ax.d365ffo.onprem.contoso.com** **katram** tipa **AOSNodeType** Service Fabric klastera mezglam. A ierakstus nedrīkst izveidot citu tipu mezgliem.

1. Ar peles labo pogu noklikšķiniet uz jaunās zonas un pēc tam noklikšķiniet uz **Jauns resursdators**.
2. Ievadiet Service Fabric mezgla nosaukumu un IP adresi (piemēram, 10.179.108.12) un pēc tam noklikšķiniet uz **Pievienot resursdatoru**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>A ieraksta iestatīšana vadības modulim

Jaunajā DNS zonā izveidojiet A ierakstu ar nosaukumu **sf.d365ffo.onprem.contoso.com** **katram** tipa **OrchestratorType** Service Fabric klastera mezglam. A ierakstus nedrīkst izveidot citu tipu mezgliem.

1. Ar peles labo pogu noklikšķiniet uz jaunās zonas un pēc tam noklikšķiniet uz **Jauns resursdators**.
2. Ievadiet Service Fabric mezgla nosaukumu un IP adresi (piemēram, 10.179.108.15) un pēc tam noklikšķiniet uz **Pievienot resursdatoru**.

#### <a name="join-vms-to-the-domain"></a>Virtuālo mašīnu pievienošana domēnam

Pievienojiet katru virtuālo mašīnu domēnam, veicot rakstā [Kā Windows Server 2016 pievienot Active Directory domēnam](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html) norādītās darbības. Vai arī izmantojiet Windows PowerShell skriptu.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
Kad visas virtuālās mašīnas ir pievienotas domēnam, AOS pakalpojuma kontus (Contoso\svc-AXSF$, Contoso\svc-AXSF$) pievienojiet lokālajai administratoru grupai. Informācija par to, kā to izdarīt, pieejama rakstā [Dalībnieka pievienošana lokālai grupai](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx).

#### <a name="disable-user-access-control"></a>Lietotāja piekļuves kontroles atspējošana 

Lai atspējotu lietotāja piekļuves kontroli **katrā** Service Fabric mezglā, izpildiet tālāk norādīto skriptu.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> Pēc veiksmīgas skripta pabeigšanas restartējiet mezglu.

#### <a name="add-prerequisite-software-to-vms"></a>Nepieciešamās programmatūras pievienošana virtuālajām mašīnām

Tālāk esošajā tabulā uzskaitīta nepieciešamā programmatūra, kas jālieto katra mezgla tipa mašīnām.

> [!NOTE]
> Pēc komponentu instalēšanas būs jārestartē dators.

| Zara tips | Komponents | Komanda |
|-----------|-----------|---------|
| AOS       | SNAC — ODBC draiveris | Skatiet rakstu [Microsoft ODBC draiveris 13.1 programmai SQL Server — Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Microsoft .NET Framework versija 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Framework versija 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Interneta informācijas pakalpojumi (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual C++ izplatāmās pakotnes komplektam Microsoft Visual Studio 2013 | Skatiet rakstu [Microsoft Visual C++ izplatāmās pakotnes komplektam Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | Microsoft Access datu bāzes programma 2010, izplatāmā versija | Skatiet rakstu [Microsoft Access datu bāzes programma 2010, izplatāmā versija](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | .NET Framework versija 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Framework versija 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | SQL Server pārskatu izveides pakalpojumi 2016 režīmā **Vietējs** | |
| MR        | .NET Framework versija 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework versija 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual C++ izplatāmās pakotnes komplektam Visual Studio 2013 | Skatiet rakstu [Microsoft Visual C++ izplatāmās pakotnes komplektam Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>Iestatīšanas skriptu lejupielāde no LCS

Esam nodrošinājuši vairākus skriptus, kas palīdz uzlabot iestatīšanas procesu. Lai lejupielādētu iestatīšanas skriptus no LCS, izpildiet tālāk norādītās darbības.

1. Pierakstieties pakalpojumā LCS (<https://lcs.dynamics.com/v2>).
2. Informācijas panelī noklikšķiniet uz elementa **Koplietojamo līdzekļu bibliotēka**.
3. Noklikšķiniet uz cilnes **Modelis**.
4. Režģī atlasiet rindu **Dynamics 365 for Operations — lokālā izvietojuma skripti**.
5. Noklikšķiniet uz **Versijas** un lejupielādējiet jaunāko skriptu versiju.

### <a name="describe-your-configuration"></a>Konfigurācijas aprakstīšana

Šajā sadaļā sniegta informācija par skriptiem, kas jāpalaiž. Skripti ir aplūkoti tādā secībā, kādā tie ir jāpalaiž. Lai palaistu skriptus, aizpildiet veidnes failu: $(downloadPath)\\ConfigTemplate.xml. Fails ConfigTemplate.xml file apraksta Service Fabric klasterus, to konfigurēšanai izmantotos sertifikātus un kontus, kam jāpiešķir piekļuve attiecīgajiem sertifikātiem. Sniegtajā piemērā vērtības ir aizpildītas atbilstoši šajā tēmā aprakstītajai parauga infrastruktūrai. Veidnes fails tiks izmantots nākamajā sadaļā.

#### <a name="create-the-domain-account-for-a-service-user"></a>Domēna konta izveide pakalpojuma lietotājam

Izpildiet tālāk norādīto komandu, lai izveidotu domēna lietotāja kontu contoso\\AXServiceUser.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>gMSA izveide

1. Mainiet direktoriju uz **$(DownloadPath)** un palaidiet tālāk norādīto Windows PowerShell komandu.

    > [!NOTE]
    > Šis skripts neizveido lietotājus. Taču tas izveido komandas, kas ir manuāli jāpalaiž domēna kontrollera mašīnā.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Kopējiet komandas izvadi Windows PowerShell logā. Pārliecinieties, vai ir noņemti rindiņu pārtraukumi, un palaidiet rindas Active Directory domēna kontrollera mašīnā, izmantojot paaugstinātās privilēģijas (noklikšķiniet ar peles labo pogu un pēc tam noklikšķiniet uz **Palaist kā administratoram**).
3. Palaidiet tālāk norādīto skriptu Active Directory domēna kontrollera mašīnā, lai pārbaudītu, vai konti ir veiksmīgi izveidoti. Noteikti skriptu palaidiet tikai pēc tam, kad esat aizvietojis modeli, kas atbilst pakalpojuma kontu nosaukumdošanas metodei.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Palaidiet skriptu Export-AddGMSAsONVMScript.ps1 klienta mašīnā. Šis skripts ģenerē skriptus, kas tiek palaisti katrā Service Fabric virtuālajā mašīnā, un pievieno tos mapei, kas atbilst katras virtuālās mašīnas nosaukumam.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>IIS apturēšana

Izmantojiet attālās darbvirsmas protokolu (RDP), lai izveidotu savienojumu ar katru Service Fabric virtuālo mašīnu, un izpildiet rakstā [Tīmekļa servera startēšana vai apturēšana (IIS 7)](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx) norādītās manuālās darbības. Varat arī izmantot tālāk norādīto Windows PowerShell skriptu, izmantojot RDP savienojuma izveidei ar katru Service Fabric virtuālo mašīnu.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_IIS līdzeklis ir jāinstalē, bet jāatspējo, jo produktā pastāv noteiktas atkarības no IIS DLL._

### <a name="install-certificates"></a>Sertifikātu instalēšana

1. Ja šajā tēmā iepriekš uzskaitītos sertifikātus ieguvāt no derīgas sertificēšanas iestādes, failā ConfigTemplate.xml norādiet sertifikātu .pfx faila nosaukumu un nospiedumu. Atribūtu **generateSelfSignedCert** iestatiet uz **Aplams** un arī atribūtu **exportable** iestatiet uz **Aplams**. Kopējiet .pfx failus mapē $(DownloadPath)\\InfrastructureScripts\\Certs.
2. Ja izmantojat pašparakstītus sertifikātus (tikai testēšanas nolūkos), palaidiet tālāk norādīto skriptu. Lai izveidotu pašparakstītus sertifikātus, pārliecinieties, vai failā ConfigTemplate.xml atribūts **generateSelfSignedCert** ir iestatīts uz **Patiess** un arī atribūts **exportable** ir iestatīts uz **Patiess**. Skripts atjauninās XML ar sertifikātu nospiedumu.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Eksportējiet jaunos sertifikātus ar privāto atslēgu (.pfx failu). Lai ģenerētu un palaistu eksportēšanas komandas čaulā Windows PowerShell, izmantojiet tālāk norādīto skriptu. .pfx faili tiks ievietoti mapē Certs.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Sertifikātiem ir jābūt instalētiem un jāatrodas šeit:\\CurrentUser\\My. Sertifikātiem ir jābūt arī eksportējamiem.

    Ja izmantojat pašparakstītus sertifikātus, pārejiet uz nākamo sadaļu. Jums šī procedūra nav jāveic.

4. Pēc .pfx failu eksportēšanas vai kopēšanas mapē $(DownloadPath)\\InfrastructureScripts\\Certs palaidiet tālāk norādītās komandas, lai ģenerētu skriptus, kas tiks ievietoti virtuālajām mašīnām atbilstošajās mapēs.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Kopējiet katrā mapē esošos skriptus uz virtuālajām mašīnām, kas atbilst mapes nosaukumam.
6. Katrā virtuālajā mašīnā palaidiet tālāk norādītos skriptus tādā secībā, kādā tie ir redzami.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Savrupa Service Fabric klastera iestatīšana

1. Izpildiet tālāk norādīto komandu, lai ģenerētu failu ClusterConfig.json.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Papildinformāciju skatiet rakstos [1B darbība: vairākmašīnu klastera izveide](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Savrupa klastera aizsardzība operētājsistēmā Windows, izmantojot X.509 sertifikātus](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) un [Savrupa klastera, kas darbojas operētājsistēmā Windows Server, izveide](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. Lejupielādējiet [Service Fabric savrupās instalācijas pakotni](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) vienā no Service Fabric mezgliem. Pēc .zip faila lejupielādes atbloķējiet to, ar peles labo pogu noklikšķinot uz .zip faila un pēc tam noklikšķinot uz **Rekvizīti**. Dialoglodziņā atzīmējiet izvēles rūtiņu **Atbloķēt** apakšējā labajā stūrī.
3. Kopējiet .zip failu uz vienu no Service Fabric klastera mezgliem un izgūstiet to no ZIP arhīva.
4. Izpildiet tālāk norādītās komandas, lai visu mezglu portos 443 un 445 izveidotu ienākošā ugunsmūra kārtulu.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Izpildiet tālāk norādītās komandas, lai tikai SSRS mezgla portā 80 izveidotu ienākošā ugunsmūra kārtulu.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. Kopējiet failu ClusterConfig.json uz savrupā Service Fabric no ZIP arhīva neizgūtās instalācijas atrašanās vietu.
7. Pārejiet uz no ZIP arhīva neizgūtās instalācijas atrašanās vietu čaulā Windows PowerShell, izmantojot paaugstinātās privilēģijas, un izpildiet tālāk norādīto komandu, lai testētu ClusterConfig.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Ja tests ir veiksmīgs, izpildiet tālāk norādīto komandu, lai izvietotu klasteri.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. Pēc klastera izveides atveriet Service Fabric pārlūku jebkurā klienta mašīnā, lai pārbaudītu instalāciju.

    1. Ja Service Fabric klienta sertifikāts vēl nav instalēts, instalējiet to mapē CurrentUser\\My.
    2. Atveriet sadaļas **IE iestatījumi** \> **Saderības režīms** un notīriet izvēles rūtiņu **Iekštīkla vietnes rādīt saderības režīmā**.
    3. Atveriet `https://sf.d365ffo.onprem.contoso.com:19080`, kur sf.d365ffo.onprem.contoso.com ir zonā norādītā Service Fabric klastera resursdatora nosaukums. Ja DNS nosaukuma atpazīšana nav konfigurēta, izmantojiet datora IP adresi.
    4. Atlasiet klienta sertifikātu. Tiek parādīta lapa **Service Fabric pārlūks**.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>LCS savienojamības konfigurēšana nomniekam

Finance and Operations izvietošana un apkalpošana tiek vadīta pakalpojumā LCS, izmantojot lokāli viesoto lokālo aģentu. Lai izveidotu LCS savienojamību ar Finance and Operations nomnieku, jums ir jākonfigurē sertifikāts, kas lokālo aģentu iespējo darboties jūsu Azure AD nomnieka vārdā (piemēram, Contoso.Onmicrosoft.com).

Izmantojiet lokālo aģenta sertifikātu, ko ieguvāt no CA, vai pašparakstīto sertifikātu, ko ģenerējāt, izmantojot skriptus.

Tikai lietotāja konti, kuriem ir direktorija loma Globālais administrators, var pievienot sertifikātus LCS autorizēšanai. Pēc noklusējuma direktorija globālais administrators ir persona, kas reģistrējusies programmā Microsoft Office 365 jūsu organizācijai.

> [!NOTE]
> Sertifikāts ir jākonfigurē tieši vienu reizi katram nomniekam. Visas lokālās vides var izmantot vienu sertifikātu savienojuma izveidei ar LCS.

1. Lejupielādējiet un instalējiet jaunāko Azure PowerShell versiju klienta datorā. Papildinformāciju skatiet rakstā [Azure PowerShell instalēšana un konfigurēšana](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Pierakstieties [debitora Azure portālā](https://portal.azure.com), lai pārliecinātos, vai jums ir direktorija loma Globālais administrators.
3. Palaidiet tālāk norādīto skriptu no $(DownloadPath)\\InfrastructureScripts.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Failu krātuves iestatīšana

Jums ir jāiestata divi augstas pieejamības SMB 3.0 failu koplietojumi. Informāciju par SMB 3.0 iespējošanu skatiet rakstā [SMB drošības uzlabojumi](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
Drošā dialekta saskaņošana nevar noteikt vai novērst pazemināšanu no SMB 2.0 vai 3.0 uz SMB 1.0. Šī iemesla dēļ, kā arī tāpēc, lai izmantotu visas SMB šifrēšanas iespējas, ir stingri ieteicams atspējot SMB 1.0 serveri.

> [!NOTE]
> Lai palīdzētu nodrošināt datu aizsardzību, kamēr tie jūsu vidē netiek izmantoti, katrā datorā ir jāiespējo BitLocker diska šifrēšana. Informāciju par BitLocker iespējošanu skatiet rakstā [BitLocker: izvietošana operētājsistēmā Windows Server 2012 un jaunākās versijās](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- Failu koplietojums, kurā tiek glabāti serverī AOS augšupielādētie lietotāju dokumenti (piemēram, \\\\DAX7SQLAOFILE1\\aos-storage).
- Failu koplietojums, kurā tiek glabāti jaunākie būvējuma un konfigurācijas faili izvietojuma vadīšanai (piemēram, \\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > Šim failu koplietojuma ceļam ir jābūt pēc iespējas īsākam, lai nepārsniegtu maksimālo ceļa garumu failiem, kas tiks ievietoti koplietojumā.

1. Failu koplietošanas mašīnā izpildiet tālāk norādīto komandu.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>Failu koplietojuma \\\\DAX7SQLAOFILE1\\aos-storage iestatīšana

2. Servera pārvaldniekā atlasiet **Failu un krātuves pakalpojumi** \> **Koplietojumi**.
3. Noklikšķiniet uz **Uzdevumi** \> **Jauns koplietojums**, lai izveidotu jaunu koplietojumu ar nosaukumu **aos-storage**.
4. Katrai mašīnai Service Fabric klasterī, izņemot **OrchestratorNodeType**, piešķiriet atļauju **Modificēt**.
5. Lietotāja AOS domēna lietotājam (contoso\\AXServiceUser) un gMSA lietotājam (contoso\\svc-AXSF) piešķiriet atļauju **Modify**.

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>Failu koplietojuma \\\\DAX7SQLAOFILE1\\agent iestatīšana

6. Atgriezieties servera pārvaldniekā un atlasiet **Failu un krātuves pakalpojumi** \> **Koplietojumi**.
7. Noklikšķiniet uz **Uzdevumi** \> **Jauns koplietojums**, lai izveidotu jaunu koplietojumu ar nosaukumu **agent**.
8. Lokālā izvietojuma aģenta gMSA lietotājam (contoso\\svc-LocalAgent$) piešķiriet atļauju **Pilna kontrole**.

### <a name="set-up-sql-server"></a>SQL Server iestatīšana

1. Instalējiet SQL Server 2016 SP1 ar augstu pieejamību kā SQL klasterus, kas ietver krātuves apgabala tīklu (SAN), vai AlwaysOn konfigurācijā.  Pārliecinieties, vai **Datu bāzes programma, pārskatu izveides pakalpojumi, pilnteksta meklēšana** un **Pārvaldības rīki** jau ir instalēti.
> [!NOTE]
> Lūdzu, pārliecinieties, vai SQL AlwaysOn ir iestatīts saskaņā ar norādījumiem rakstā [Lapa Sākotnējo datu sinhronizācijas atlase (AlwaysOn pieejamības grupu vedņi)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) un ievērojiet rakstā [Sekundāro datu bāzu manuāla sagatavošana](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs) sniegtos norādījumus.
2. Palaidiet SQL pakalpojumu kā domēna lietotāju.
3. Iegūstiet SSL sertifikātu no CA, lai konfigurētu programmu Finance and Operations. Testēšanas nolūkiem varat izveidot un izmantot pašparakstītu sertifikātu.

**Pašparakstīts sertifikāts klasterveida SQL instancei**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Pašparakstīts sertifikāts AlwaysOn SQL instancei**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. Izmantojot sertifikātu, izpildiet rakstā [SSL šifrēšanas iespējošana SQL Server instancei, izmantojot Microsoft pārvaldības konsoli](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) norādītās darbības, lai konfigurētu SSL serverī SQL Server.
5. Katra klastera mezglam izpildiet tālāk norādītās darbības. Pārliecinieties, vai izmaiņas veicat neaktīvam mezglam un pārlecat tam kļūmi pēc izmaiņu veikšanas.

    1. Importējiet sertifikātu šeit: LocalMachine\\My.
    2. Piešķiriet sertifikātu atļaujas pakalpojuma kontam, kas tiek izmantots SQL pakalpojuma palaišanai. Microsoft pārvaldības konsolē (MMC) ar peles labo pogu noklikšķiniet uz sertifikāta (certlm.msc) un pēc tam noklikšķiniet uz **Uzdevumi** \> **Pārvaldīt privātās atslēgas**.
    3. Pievienojiet sertifikāta nospiedumu: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.
    4. Microsoft SQL Server konfigurācijas pārvaldniekā vienumu **ForceEncryption** iestatiet uz **Jā**.

6. Eksportējiet sertifikāta publisko atslēgu (.cer failu) un instalējiet to katra Service Fabric mezgla uzticamajā saknē.

### <a name="configure-the-orchestratordata-database"></a>Datu bāzes OrchestratorData konfigurēšana

1.  Izveidojiet tukšu datu bāzi un nosauciet to par **OrchestratorData**. Šo datu bāzi lokāli viesotais lokālais aģents izmanto izvietojumu vadīšanai.
2.  Piešķiriet datu bāzei lokālā aģenta gMSA (svc-LocalAgent$) **db\_owner** atļaujas.

    1. Kokā izvērsiet servera nosaukumu, izvērsiet vienumus **Drošība** \> **Pieteikšanās**, noklikšķiniet ar peles labo pogu un noklikšķiniet uz **Jauna pieteikšanās**.

        ![Komanda Jauna pieteikšanās](./media/OPSetup_01_NewLogin.png)


    2. Uzmeklējiet pakalpojuma kontu **svc LocalAgent$**. Noklikšķiniet uz **Atrašanās vietas** un atlasiet **Viss direktorijs**, pēc tam noklikšķiniet uz **Objektu tipi** un atlasiet **Pakalpojuma konts**.

        ![Dialoglodziņš Atlasīt lietotāju, Pakalpojuma konts vai Grupa](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. Vienumu **Assign ServerRole** iestatiet uz **Publisks**.
    4. Datu bāzes lomas atļauju **db\_owner** iestatiet uz datu bāzi OrchestratorData.

### <a name="configure-the-finance-and-operations-database"></a>Finance and Operations datu bāzes konfigurēšana

1. Pierakstieties pakalpojumā LCS (<https://lcs.dynamics.com/v2>).
2. Informācijas panelī noklikšķiniet uz elementa **Koplietojamo līdzekļu bibliotēka**.
3. Noklikšķiniet uz cilnes **Modelis**. 
4. Režģī noklikšķiniet uz rindas **Dynamics 365 for Operations lokālā versija, Enterprise izdevums — demonstrācijas dati**, lai lejupielādētu .zip failu.
5. .zip failā ir ietverti tukši un demonstrācijas datu .bak faili. Izvēlieties .bak failu atbilstoši savām vajadzībām. Piemēram, ja jums ir nepieciešami demonstrācijas dati, atjaunojiet failu AxBootstrapDB_Demodata.bak. 
6. Atjaunojiet datu bāzi AxBootstrapDB_DemoData.bak.
7. Pārdēvējiet datu bāzi kā **AXDBRAIN**.
8. Atjaunotajā datu bāzē palaidiet tālāk norādītos vaicājumus.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Atjauniniet datu bāzes failus.

    1. Ar peles labo pogu noklikšķiniet uz datu bāzes un pēc tam noklikšķiniet uz **Rekvizīti**.
    2. Noklikšķiniet uz **Faili**, lai mainītu datu bāzes failu rekvizītus.
    3. Laukā **Sākotnējais lielums (MB)** ievadiet vērtību, kas ir lielāka par 5120.

        ![Dialoglodziņš Datu bāzes rekvizīti](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. Vienumam **AXDBBuild\_Data** lauku **Automātiskā palielināšana/maksimizēšana** iestatiet uz **200** megabaitiem (MB).
    5. Vienumam **AXDBBuild\_Log** lauku **Automātiskā palielināšana/maksimizēšana** iestatiet uz **500** MB.

        ![Dialoglodziņš Mainīt automātisko palielināšanu](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. Izveidojiet jaunu lietotāju, kuram ir iespējota SQL autentifikācija (axdbadmin).
6. Izmantojiet informāciju tālāk esošajā tabulā, lai kartētu lietotājus un datu bāzu lomas.

    | Lietotājs             | tips    | Datu bāzes loma |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. Piešķiriet lietotājam svc-AXSF$ un SQL lietotājam axdbadmin piekļuvi tālāk norādītajām lomām datu bāzē tempdb.

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. Programmā Management Studio izpildiet tālāk norādītās Transact-SQL (T-SQL) komandas.

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Izpildiet šādu komandu:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>Finanšu pārskatu datu bāzes konfigurēšana

1.  Izveidojiet tukšu datu bāzi un nosauciet to par **FinancialReporting**.
2.  Izmantojiet informāciju tālāk esošajā tabulā, lai kartētu lietotājus un datu bāzu lomas.

    | Lietotājs             | tips | Datu bāzes loma |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>Akreditācijas datu šifrēšana

1. Jebkurā klienta mašīnā instalējiet šifrēšanas sertifikātu krātuvē LocalMachine\\My certificate.
2. Piešķiriet pašreizējam lietotājam lasīšanas piekļuvi šī sertifikāta privātajai atslēgai.
3. Izveidojiet failu Credentials.json, kā parādīts šeit.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** ir šifrētā domēna lietotāja parole AOS domēna lietotājam (contoso\\axserviceuser).
    - **SqlUser** ir šifrētais SQL lietotājs (axdbadmin), kuram ir piekļuve Finance and Operations datu bāzei (AXDBRAIN), un **SqlPassword** ir šifrētā SQL parole.

4. Kopējiet failu .json SMB failu koplietojumā \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. Atjauniniet failu Credentials.json ar šifrētajām vērtībām.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. Failā Credentials.json vienumu **\<encryptedDomainUserPassword\>** aizstājiet ar šifrēto domēna paroli.
    2. Vienumu **\<encryptedSqlUser\>** aizstājiet ar šifrēto Finance and Operations SQL lietotāju.
    3. Vienumu **\<encryptedSqlPassword\>** aizstājiet ar Finance and Operations SQL paroli.
    
### <a name="set-up-ssrs"></a>Iestatīt SSRS

1.  Pirms sākat, pārliecinieties, vai ir instalēti visi elementi, kas ir uzskaitīti priekšnosacījumu sadaļā šīs tēmas sākumā.
2.  Izpildiet rakstā [SQL Server pārskatu izveides pakalpojumu konfigurēšana lokālam izvietojumam](../analytics/configure-ssrs-on-premises.md) norādītās darbības.

### <a name="configure-ad-fs"></a>AD FS konfigurēšana

Lai varētu veikt šo procedūru, operētājsistēmā Windows Server 2016 ir jāizvieto AD FS. Informāciju par AD FS izvietošanu skatiet rakstā [Windows Server 2016 un 2012 R2 AD FS izvietošanas rokasgrāmata](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Programmai Finance and Operations papildus standarta komplektācijā iekļautajai AD FS konfigurācijai ir nepieciešama papildu konfigurācija. Nākamo darbību izpildei Windows PowerShell darbojas mašīnā, kurā ir instalēts AD FS lomas pakalpojums. Lietotāja kontam ir jābūt pietiekamām atļaujām AD FS administrēšanai. Piemēram, lietotājam ir nepieciešams domēna administratora konts.

1. Konfigurējiet AD FS identifikatoru tā, lai tas atbilstu AD FS pilnvaras izsniedzējam.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Windows integrētā autentifikācija (WIA) ir jāatspējo iekštīkla autentifikācijas savienojumiem, ja vien neesat konfigurējis AD FS jauktām vidēm. Papildinformāciju par WIA konfigurēšanu tā, lai to varētu izmantot ar AD FS, skatiet rakstā [Pārlūkprogrammu konfigurēšana Windows integrētās autentifikācijas (WIA) izmantošanai ar AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. Lai pierakstītos, lietotāja e-pasta adresei ir jābūt pieņemamai autentifikācijas ievadei.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

Lai pakalpojums AD FS uzticētos Finance and Operations autentifikācijas apmaiņai, AD FS programmu grupā ir jābūt reģistrētiem dažādiem programmu ierakstiem. Lai paātrinātu iestatīšanas procesu un palīdzētu samazināt kļūdas, reģistrācijai varat izmantot tālāk norādīto skriptu. Kopējiet skriptu Publish-ADFSApplicationGroup.ps1 un direktoriju D365FO-OP mašīnā, kurā ir instalēts AD FS lomas pakalpojums. Pēc tam palaidiet skriptu, izmantojot lietotāja kontu, piemēram, administratora kontu, kam ir pietiekamas atļaujas AD FS administrēšanai. Papildinformāciju par skripta izmantošanu skatiet skriptā norādītajā dokumentācijā. Pierakstiet klienta ID, kas tiek norādīti izvadē, jo pakalpojumā LCS kādā no turpmākajām darbībām jums tiks prasīta šī informācija.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

AD FS pārvaldības konsolei ir jāatbilst tālāk esošajā attēlā redzamajai. Lai atvērtu servera pārvaldnieku, noklikšķiniet uz **Rīki** \> **AD FS pārvaldība** un pēc tam kreisajā pusē esošā koka skata apakšdaļā noklikšķiniet uz **Programmu grupas**. Veiciet dubultklikšķi uz programmu grupas, lai skatītu papildinformāciju.

![Programmu grupas rekvizīti](./media/OPSetup_05_ApplicatioGroupProperties.png)

Beigās pārbaudiet, vai varat piekļūt AD FS OpenID konfigurācijas vietrādim URL Service Fabric **AOSNodeType** tipa mezglā, tīmekļa pārlūkprogrammā dodoties uz `https://<adfs-dns-name>/adfs/.well-known/openid-configuration`. Ja saņemat ziņojumu, kurā teikts, ka vietne nav droša, AD FS SSL sertifikāts nav pievienots uzticamo galveno sertificēšanas iestāžu krātuvei. Šī darbība ir aprakstīta AD FS izvietošanas rokasgrāmatā. Ja jūs veiksmīgi piekļūstat vietrādim URL, tiek atgriezts JavaScript Object Notation (JSON) fails ar jūsu AD FS konfigurāciju un ir redzams, ka jūsu AD FS vietrādis URL ir uzticams.

Ar šo darbību infrastruktūras iestatīšana ir pabeigta. Tālāk esošajās sadaļās aprakstīts, kā pāriet uz [LCS](https://lcs.dynamics.com), lai iestatītu savienotāju un izvietotu Dynamics 365 for Finance and Operations vidi.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Savienotāja konfigurēšana un lokāli viesotā lokālā aģenta instalēšana

1. Pierakstieties pakalpojumā [LCS](https://lcs.dynamics.com/) un atveriet lokālo ieviešanas projektu.
2. Hamburgera izvēlnē noklikšķiniet uz **Projekta iestatījumi**.

    ![Komanda Projekta iestatījumi](./media/OPSetup_06_ProjectSettings.png)

3. Noklikšķiniet uz **Lokālie savienotāji**.
4. Noklikšķiniet uz **Pievienot**, lai izveidotu jaunu savienotāju.
5. Cilnē **Resursdatora infrastruktūras iestatīšana** lejupielādējiet aģenta instalētāju.

    ![Poga Lejupielādēt aģenta instalētāju cilnē Resursdatora infrastruktūras iestatīšana](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Nodrošiniet, ka .zip fails ir atbloķēts. Ar peles labo pogu noklikšķiniet uz faila, noklikšķiniet uz **Rekvizīti** un pēc tam atlasiet **Atbloķēt**.
7. Izgūstiet aģenta instalētāju no ZIP arhīva vienā no Service Fabric **OrchestratorType** tipa mezgliem.
8. Cilnē **Aģenta konfigurēšana** ievadiet konfigurācijas iestatījumus.
9. Saglabājiet konfigurāciju un pēc tam noklikšķiniet uz **Lejupielādēt konfigurācijas**, lai lejupielādētu konfigurācijas failu localagent-config.json.

    ![Poga Lejupielādēt konfigurācijas cilnē Aģenta konfigurēšana](./media/OPSetup_08_DownloadConfigurations.png)

10. Kopējiet failu localagent-config.json mašīnā, kurā atrodas aģenta instalētāja pakotne.
11. Komandu uzvednes logā izpildiet tālāk norādīto komandu, pārejot uz mapi, kurā ir aģenta instalētājs.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > Lietotājam, kurš izpilda šo komandu, datu bāzē OrchestratorData ir jābūt atļaujai **db\_owner**.
    
12. Kad lokālais aģents ir veiksmīgi instalēts, pārejiet atpakaļ uz lokālo savienotāju pakalpojumā LCS.
13. Cilnē **Iestatījumu validēšana** noklikšķiniet uz pogas **Ziņojumu aģents**. Ar šo darbību tiks pārbaudīta LCS savienojamība ar jūsu lokālo aģentu. Pēc veiksmīgas savienojuma izveides lapa izskatīsies, kā norādīts tālāk esošajā attēlā.

     ![Aģenta validēšana](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Dynamics 365 for Finance and Operations (lokālās) vides izvietošana

1. Pārejiet uz lokālo projektu pakalpojumā LCS, atveriet sadaļas **Vide**, **Smilškaste** un noklikšķiniet uz **Konfigurēt**.
2. Atlasiet savu vienumu **Vides topoloģija** un veiciet vedņa darbības, lai sāktu izvietošanu.
3. Lokālais aģents pieņems izvietošanas pieprasījumu, sāks izvietošanu un sazināsies ar LCS, kad būs gatavs.

