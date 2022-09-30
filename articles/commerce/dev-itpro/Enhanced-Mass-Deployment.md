---
title: Plaša apzīmogoto Commerce patstāvīgi izmantojamā pakalpojuma komponentu izvietošana
description: Šajā rakstā ir izskaidrots, kā izmantot struktūru pašapkalpošanās komponentu instalētājiem, lai klusā veidā instalētu un pakalpojumu izvietošanas.
author: jashanno
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: 426473c14cdf9e171810aafd97dbb1afd5988b2f
ms.sourcegitcommit: 24673493d14f2045a08fe7240689bee34e099cb5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2022
ms.locfileid: "9589094"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>Plaša apzīmogoto Commerce patstāvīgi izmantojamā pakalpojuma komponentu izvietošana

[!include [banner](../includes/banner.md)]

Šis raksts attiecas uz aizzīmogoto struktūru, komponentu instalētājiem, kas ir izlaisti katru mēnesi, sākot ar 10.0.18 laidienu un Microsoft Dynamics kas ir pieejami Lifecycle Services (LCS) koplietojamā līdzekļu bibliotēkā. Ņemiet vērā, ka pirmie vairāki šo jauno instalētāju laidieni ir atzīmēti kā **(priekšskatījums)**. Tomēr šī apzīmējuma vienīgais nolūks ir diferencēt jaunos instalētājus, kamēr Korporācija Microsoft nosaka, vai pastāv papildu funkcionālās prasības to lietošanai. Tas nenozīmē, ka instalētāji nav derīgi ražošanai. Pamatojoties uz šo jauno instalētāju laidienu, Microsoft plāno nolietot vecos (mantojuma) instalētājus vai ap 2023. gada oktobris. 

Šajā rakstā ir izskaidrots, kā lietot jaunos instalētājus, lai veiktu kluso instalēšanu un atjauninājumu apkalpošanai, izmantojot komandrindas argumentus. Šie argumenti ļauj jums veikt masveida izvietošanu vairākos dažādos veidos.

> [!NOTE]
> Jaunie pašapkalpošanās aizzīmogotie instalētāji netiks pieejami programmā Headquarters, un tos var lejupielādēt tikai, izmantojot LCS.

## <a name="delimiters-for-mass-deployment"></a>Norobežotāji masveida izvietošanai

Tabulā ir parādīti norobežotāji, kurus var izmantot komandrindas izpildē.


| Norobežotājs                 | Apraksts |
|---------------------------|-------------|
| –AadTokenIssuerPrefix | Microsoft () marķiera Azure Active Directory Azure AD izsniedzēja prefikss. |
| –AsyncClientAadClientId | Klienta Azure AD ID, kas Async klientam ir jāizmanto, veicot sakarus ar programmu Headquarters. |
| –AsyncClientAppInsokesInstrumentationKey | Async klienta instrumentācijas AppInsights atslēga. |
| –AsyncClientCertFullPath | Pilnībā formatēts UZV ceļš, kas izmanto īssavilkumu kā Async Azure AD klienta identitātes sertifikāta atrašanās vietas meklēšanas metriku, kas jāizmanto, lai autentificētu sakarus programmā Headquarters. Piemēram, ir `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` pareizi formatēts IS. Vērtība tiks **\<MyThumbprint\>** aizstāta ar sertifikāta īssavilkumu, kas jāizmanto. Neizmantojiet šo parametru kopā ar parametru **-AsyncClientCertThumbprint**. |
| –AsyncClientCertThumbprint | Async klienta identitātes sertifikāta īssavilkums, kas ir jāizmanto, lai autentificētu, izmantojot sakarus Azure AD ar programmu Headquarters. Šis īssavilkums tiks izmantots, lai meklētu **LocalMachine/My veikala** atrašanās vietu un nosaukumu, lai atrastu pareizo sertifikātu, ko izmantot. Neizmantojiet šo parametru kopā ar parametru **-AsyncClientCertFullPath**. |
| –ClientAppInsokesInstrumentationKey | Klienta instrumentācijas AppInsights atslēga. |
| –CloudPosAppInsppasInstrumentationKey | Mākoņa POS AppInsights instrumentācijas atslēga. |
| -Config | Konfigurācijas fails, kas jāizmanto instalēšanas laikā. Faila nosaukuma piemērs ir **Contoso.CommerceScaleUnit.xml**. |
| –CposAadClientId | Klienta Azure AD ID, kas Cloud POS ir jāizmanto ierīces aktivizēšanas laikā. Šis parametrs nav nepieciešams lokāliem izvietojumiem. |
| -Ierīci | Ierīces ID, kā norādīts galvenās pārvaldes **lapā** Ierīces. |
| —EnvironmentId; | Vides ID. |
| -HardwareStationAppInsppasInstrumentationKey | Aparatūras stacijas AppInsights instrumentācijas atslēga. |
| Instalēt | Parametrs, kas norāda, vai ir jābūt instalētam komponentam, ko nodrošina šī instalētājs. Šis parametrs ir nepieciešams, lai veiktu instalēšanu, un tam nav sākuma domuzīmes. |
| -InstallOffline | Modern POS šis parametrs norāda, ka ir jāinstalē un jākonfigurē arī bezsaistes datu bāze. Izmantojiet arī **parametru -SQLServerName**. Pretējā gadījumā instalētājs mēģinās atrast noklusējuma instanci, kas atbilst priekšnosacījumi. Ja izmantojat Azure Active Directory (Azure AD) autentifikāciju, POS bezsaiste nedarbojas, jo tiešsaistes savienojums ir nepieciešams vienmēr. |
| -Portu | Ports, kas ir jāsaista ar Retail Server virtuālo direktoriju un jāizmanto tajā. Ja nav iestatīts neviens ports, tiks izmantots noklusējuma ports 443. |
| -Reģistrēties | Kases sistēmas ID, kā norādīts galvenās **pārvaldes kases** sistēmas lapā. |
| -RetailServerAadClientId | Klienta Azure AD ID, kas Retail Server jāizmanto, veicot sakarus ar programmu Headquarters. |
| -RetailServerAadResourceId | Retail servera programmas Azure AD resursa ID, kas ir jāizmanto ierīces aktivizēšanas laikā. Šis parametrs nav nepieciešams lokāliem izvietojumiem. |
| -RetailServerCertFullPath | Pilnībā formatēts UZV ceļš, kas izmanto īssavilkumu kā Retail Server Azure AD identitātes sertifikāta meklēšanas metriku, kas jāizmanto, lai autentificētu sakarus programmā Headquarters. Piemēram, tas `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` ir pareizi formatēts, PARAA! vērtība **\<MyThumbprint\>** tiks nomainīta ar sertifikāta īssavilkumu, kas jāizmanto. Neizmantojiet šo parametru kopā ar parametru **-RetailServerCertThumbprint**. |
| -RetailServerCertThumbprint | Retail Server identitātes sertifikāta īssavilkums, kas ir jāizmanto, lai autentificētu, izmantojot sakarus Azure AD ar programmu Headquarters. Šis īssavilkums tiks izmantots, lai meklētu **LocalMachine/My** veikala atrašanās vietu un nosaukumu, lai atrastu pareizo sertifikātu, ko izmantot. Neizmantojiet šo parametru kopā ar parametru **-RetailServerCertFullPath**. |
| -RetailServerURL | Retail Server vietrādis URL, kas ir jāizmanto instalētājam. (Šis URL ir zināms arī kā Commerce Scale Unit \[CSU\] URL.) Modern POS šī vērtība tiks izmantota ierīces aktivizēšanas laikā. |
| – SkipAadCredentialsCheck| Pārslēgšanās, kas norāda, Azure AD vai akreditācijas datu priekšnosacījumu pārbaudes ir jāizlaiž. Noklusējuma vērtība ir **false**. |
| -SkipCertCheck | Pārslēgšanās, kas norāda, vai ir jāizlaiž sertifikāta priekšnosacījumu pārbaudes. Noklusējuma vērtība ir **false**. |
| –SkipiisCheck | Pārslēgšanās, kas norāda, vai ir jāizlaiž interneta informācijas pakalpojumu (IIS) priekšnosacījumu pārbaudes. Noklusējuma vērtība ir **false**. |
| -SkipNetFrameworkCheck | Switch, kas norāda, vai ir jāizlaiž .NET Framework priekšnosacījumu pārbaudes. Noklusējuma vērtība ir **false**. |
| – SkipScaleUnitCheck | Slēdzis, kas norāda, vai instalēto komponentu veselības pārbaude ir jāizlaiž. Noklusējuma vērtība ir **false**. |
| -SkipsChannelCheck | Slēdzis, kas norāda, vai ir jāizlaiž drošo kanālu priekšnosacījumu pārbaudes. Noklusējuma vērtība ir **false**. |
| -SkipSqlFullTextCheck | Pārslēgs, kas norāda, vai ir jāizlaiž SQL Servera priekšnosacījuma pārbaude, kam nepieciešama pilnteksta meklēšana. Noklusējuma vērtība ir **false**. |
| -SkipSqlServerCheck | Pārslēgšanās, kas norāda, vai ir jāizlaiž SQL servera priekšnosacījumu pārbaudes. Noklusējuma vērtība ir **false**. |
| -SqlServerName | SQL servera nosaukums. Ja nosaukums nav norādīts, instalētājs mēģinās atrast noklusējuma instanci. |
| -SslcertFullPath | Pilnībā formatēts HTML ceļš, kas izmanto īssavilkumu kā sertifikāta atrašanās vietas meklēšanas rādītāju, kas jāizmanto, lai šifrētu HTTP datplūsmu uz mēroga vienību. Piemēram, tas `store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` ir pareizi formatēts, PARAA! vērtība **\<MyThumbprint\>** tiks nomainīta ar sertifikāta īssavilkumu, kas jāizmanto. Neizmantojiet šo parametru kopā ar parametru **-SslCertThumbprint**. |
| -SslCertThumbprint | Tā sertifikāta īssavilkums, kas jāizmanto HTTP trafika šifrēšanai uz mēroga vienību. Šis īssavilkums tiks izmantots, lai meklētu **LocalMachine/My veikala** atrašanās vietu un nosaukumu, lai atrastu pareizo sertifikātu, ko izmantot. Neizmantojiet šo parametru kopā ar parametru **-SslCertFullPath**. |
| -StoreSystemAosUrl | Galvenās pārvaldes (AOS) VIETRĀDIs URL. |
| -StoreSystemChannelDatabaseId | Kanāla datu bāzes ID (nosaukums). |
| -TenantId; | Nomnieka Azure AD ID. |
| -TransactionServiceAzureAuthority | Transaction Service Azure AD iestāde. |
| -TransactionServiceAzureResource | Transaction Service Azure AD resurss. |
| -TrustSqlServerCertificate —TrustSqlServerCertificate; | Pārslēgšanās, kas norāda, vai servera sertifikātam jābūt uzticamam, veidojot savienojumu ar SQL Server. Lai palīdzētu novērst drošības riskus, ražošanas izvietošanai šeit nekad nav jāsniedz **vērtība ar patiesu** vērtību. Noklusējuma vērtība ir **false**. |
| -Runīgums | Reģistrēšanas līmenis, kas tiek pieprasīts instalēšanas laikā. Parasti šī vērtība nav jāizmanto. |
| –WindowsPhoneAppInsppasInstrumentationKey | Aparatūras stacijas AppInsights instrumentācijas atslēga. |

## <a name="general-overview"></a>Vispārējs apskats

Jaunajā pašapkalpošanās instalētāju struktūrā ir dažādi līdzekļi un uzlabojumi. Jaunā struktūra pašlaik izveido instalētājus tikai Modern POS, aparatūras stacijai un CSU (pašapkalpošanās). Ir svarīgi izprast aizzīmogoto instalētāju pamata komandrindas lietojumu, kam vajadzētu izskatīties līdzīgi tam, kas lietots šajā piemērā. 
 
```Console
<Component Installer Name>.exe install -<Parameter Name> "<Parameter Information>"
```

Instalētājam ir nepieciešams instalēt **parametru** (vai **atinstalēt,** lai noņemtu instalāciju) un visi parametri, kas attiecas uz šo instalāciju. **Parametra** nosaukumā jāietver visi parametri, kas ir nepieciešami, piemēram, reģistrs, CSU URL vai sertifikāta informācija. **Parametra informācijā** jāiekļauj jebkāda papildinformācija par parametriem.

Aizzīmogotā struktūra ir izveidota, lai atļautu šādas kļūdas:
- **Aizzīmogots** — jaunā instalētāja struktūra pilnībā atdala Microsoft sadalītos bāzes komponentu instalētājus no uz paplašināmību pamatotiem pielāgojumiem. Pēc tam pielāgojumi tiks instalēti, bet pēc tam vairs netiks pielāgoti attiecībā uz atjauninājumiem (lai atjauninājumus atļautu tikai Microsoft pamata komponentam, tikai pielāgojumiem vai abiem).
- **GUI- mazāk** – vairs nav lietotāja interfeisa (UI). Tā vietā katram komponentu instalētājam ir pilnībā uz komandrindu balstīta izpildāma darbība. Šīs izmaiņas ir viena no vairākām galvenajām izmaiņām vai līdzekļiem, kas tiek izmantoti, lai fokusu jaunās instalēšanas programmas struktūru izmantotu masveida izvietošanai.
- **Agrāka reģistrēšana** - uzlaboto instalēšanas programmu žurnāli ļauj labāk validēt instalēšanas pabeigšanu vai kļūmi, veicamos soļus un visus brīdinājumus vai ģenerētās kļūdas.
- **Tīrīšana —** jaunajā struktūrā komponentu instalētāji strādā daudz stingrāk, lai uzturētu instalācijas direktoriju tīrīšanas iespējas, nodzēšot pilnu komponentu mapes saturu un tikai pēc tam instalējot jaunākus komponentus. Šī tīrīšana nodrošina, ka nav palikušie faili, kas var izraisīt problēmas un novērst sekmīgu instalēšanu.

Uz jauno struktūru netika migrēti trīs komponenti: virtuālais perifērijas simulators, Async servera savienotāja pakalpojums (izmantots Dynamics AX 2012 R3 atbalstam) un reāllaika pakalpojuma aizvietošana (tiek izmantota Dynamics AX 2012 R3 atbalstam).

> [!NOTE]
> Instalētāji tiek saglabāti lokāli un saglabāti.  Laika gaitā ir svarīgi pārvaldīt vai dzēst saglabātos instalētājus, lai neiztērētu vietu diskā. Ir ieteicams saglabāt pašreizējo instalētāju pamata komponentiem un visiem paplašinājuma instalētājiem jaunākajām versijām, lai veiktu ārkārtas situāciju atkopšanu.

## <a name="migration"></a>Migrācijas

Lai veikt migrēšanu no vecās pašapkalpošanās struktūras komponentu instalēšanas programmas uz jaunajām struktūras komponentu instalētājiem, ir jāatinstalē vecie komponenti.

- **Modern POS** — jaunā instalēšanas programmas struktūra liks programmai saņemt jaunu programmas paraksta ID. Tāpēc pirms jaunā struktūras Modern POS komponenta instalēšanas ir nepieciešama veco komponentu pilnīga atinstalēšana. Tā kā šī prasība ir pilnīga atinstalēšana, ierīces aktivizēšana būs nepieciešama vēlreiz. (Šī ierīces atkārtota aktivizēšana ir vienreizējs nosacījums, ar nosacījumu, ka atinstalēšana atkārtoti neparādās.)
- **Aparatūras** stacija - kā IIS vietni, jaunajai instalētāja struktūrai ir nepieciešams, lai atkārtoti tiktustrādāta pamatmapes struktūra. Tāpēc pirms tiek instalēts jaunais struktūras aparatūras stacijas komponents, ir pilnībā jāatinstalē vecie komponenti.
- **Commerce Scale Unit (CSU, pašmitēta)** — kā IIS vietņu sērijai jaunajai instalēšanas struktūrai ir atkārtoti jāveic pamatmapes struktūras darba izveide.  Tāpēc pirms jaunā struktūras CSU (pašapkalpošanās) komponenta instalēšanas ir nepieciešama veco komponentu pilnīga atinstalēšana.

## <a name="modern-pos"></a>Modern POS

### <a name="before-you-begin"></a>Pirms sākšanas

Ir būtiski noņemt veco, pašapkalpošanās Modern POS komponentu. Papildinformāciju skatiet iepriekš šī raksta migrācijas darbībās.

> [!NOTE]
> Viena datora sistēmā, piemēram, izstrādātāja topoloģijā vai demonstrācijas vidē, vai ja Commerce Scale Unit un Modern POS ir instalēta vienā un tajā pašā datorā, iespējams, ka Store Commerce nevar pabeigt ierīces aktivizēšanu. Šī problēma rodas, jo Store Commerce nevar veikt tīkla zvanus uz vienu datoru (t.i., pašu zvanu). Lai gan ražošanas iestatījumos tas nekad nedrīkst būt scenārijs, problēma var tikt mazināta, iespējojot AppContainer atgriezeniskās cilpas izņēmumu, lai saziņā varētu notikt vienā datorā. Dažādas programmas ir publiski pieejamas, lai palīdzētu iespējot šo atgriezenisko cilpu. Papildinformāciju par atgriezenisko cilpu skatiet sadaļā [Kā iespējot atgriezenisko cilpu un novērst tīkla izolēšanu](/previous-versions/windows/apps/hh780593(v=win.10)). Ir svarīgi izprast, ka atgriezeniskā cilpa var būt drošības risks, tāpēc nav ieteicams izmantot atgriezenisko cilpu, ja vien nav nepieciešams.

### <a name="examples-of-silent-deployment"></a>Klusās izvietošanas piemēri

Šajā sadaļā ir parādīts to komandu piemēri, kas tiek izmantotas Modern POS instalēšanai.

#### <a name="silently-install-modern-pos"></a>Klusi instalēt Modern POS

Šī komanda klusi instalē (vai atjaunina) Modern POS. Tai ir standarta komandu struktūra, kas tiek izmantota pašreiz instalēto komponentu klusajai apkalpošanai. Struktūra izmanto InstallerName.exe **&lt;&gt; pamatvērtības**.

Ja tiek pieprasīta instalēšana, šajā pamata komandā ir redzamas pieejamās opcijas. Ieteicams, lai šī komanda tiek lietota, pirmo reizi testējot vai izmantojot instalētāju.

```Console
CommerceModernPOS.exe -help install
```

> [!NOTE]
> Modern POS nav nepieciešams konfigurācijas fails. Instalēšanas programmai tagad ir parametri (iepriekš šajā rakstā) dažādām vērtībām, kas tiek izmantotas ierīces aktivizēšanas laikā.

Šī komanda norāda visus parametrus, kas ir jāizmanto ierīces aktivizēšanas laikā pēc Modern POS programmas instalēšanas. Šajā piemērā tiek izmantots **Reģistrs-3**, kas ir parasti izmantotā vērtība demonstrācijas Dynamics 365 Commerce datos.

```Console
CommerceModernPOS.exe install -Register "Houston-3" -Device "Houston-3" -RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

Šī komanda norāda parametrus, kas ir jāizmanto, lai instalētu un konfigurētu bezsaistes datu bāzi. SQL Serveris tiek norādīts kopā ar konfigurācijas failu, kas jālieto.

```Console
CommerceModernPOS.exe install -InstallOffline -SQLServerName "SQLExpress" -Config "ModernPOS.Houston-3.xml"
```

Šos konceptus var apvienot un saskaņot, lai sasniegtu vēlamos instalēšanas rezultātus.

## <a name="hardware-station"></a>Aparatūras stacija

### <a name="before-you-begin"></a>Pirms sākšanas

Ir ļoti svarīgi noņemt veco pašapkalpošanās aparatūras stacijas komponentu. Papildinformāciju skatiet iepriekš šī raksta migrācijas darbībās. Vairs nav Tirgotāja konta informācijas rīka. Tā vietā tirgotāja konta informācija tiek instalēta, kad POS terminālis tiek savienots pārī ar aparatūras staciju. Pirmo reizi testējot šo instalētāju, ieteicams darbināt šādu komandu:

```Console
CommerceHardwareStation.exe -help install
```

### <a name="examples-of-silent-deployment"></a>Klusās izvietošanas piemēri

Šajā sadaļā ir parādīts to komandu piemēri, kas tiek izmantotas aparatūras stacijas instalēšanai.

#### <a name="silently-install-hardware-station"></a>Klusā aparatūras stacijas instalēšana

Šī komanda klusi instalē (vai atjaunina) aparatūras staciju. Tai ir standarta komandu struktūra, kas tiek izmantota pakalpojuma komponentiem, kas pašlaik ir instalēti. Struktūra izmanto InstallerName.exe **&lt;&gt; pamatvērtības**.

Šī pamata komanda palaiž izpildāmo failu instalētāju.

```Console
HardwareStation.exe install -Port 443 -StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" -StoreSystemChannelDatabaseID "Houston" -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> Aparatūras stacijai nav nepieciešams konfigurācijas fails. Instalēšanas programmai tagad ir parametri (iepriekš šajā rakstā) dažādām nepieciešamajām vērtībām.

Šī komanda norāda visus parametrus, kas ir nepieciešami, lai izlaistu priekšnosacījumu pārbaudes standarta instalācijas laikā. 

> [!NOTE]
> Pārbaužu izlaišana nav ieteicama bez pilnīgas pārbaudes pirms laika vai izstrādes situācijās.

```Console
HardwareStation.exe install -SkipFirewallUpdate -SkipOPOSCheck -SkipVersionCheck -SkipURLCheck -Config "HardwareStation.Houston.xml"
```

Kā parasti parasti ir jaukt un saskaņot šos konceptus, lai sasniegtu vēlamos instalēšanas rezultātus.

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (pašviesota)

Pirmo reizi testējot šo instalētāju, ieteicams darbināt šādu komandu:

```Console
CommerceStoreScaleUnitSetup.exe -help install
```

### <a name="before-you-begin"></a>Pirms sākšanas

Ir būtiski noņemt veco pašapkalpošanās CSU (pašapkalpošanās) komponentu. Papildinformāciju skatiet iepriekš šī raksta migrācijas darbībās.

### <a name="examples-of-silent-deployment"></a>Klusās izvietošanas piemēri

Šajā sadaļā ir parādīts to komandu piemēri, kas tiek izmantotas CSU instalēšanai (viesots).

#### <a name="silently-install-csu-self-hosted"></a>Klusi instalējiet CSU (paš viesots)

Tālāk norādītās komandas klusi instalē (vai atjaunina) CSU (pašapkalpošanās). Tai ir standarta komandu struktūra, kas tiek izmantota pašreiz instalēto komponentu klusajai apkalpošanai. Struktūra izmanto InstallerName.exe **&lt;&gt; pamatvērtības**.

Salīdzinājumā ar citiem pašapkalpošanās instalētājiem Commerce Scale Unit (CSU) ir sarežģītāka, un tai ir nepieciešama diezgan liela papildinformācijas summa. Šī komanda ir minimālā komanda (ar parametriem), kas nepieciešama izpildāmo failu instalēšanas programmas palaišanai, kad nav neviena konfigurācijas faila.

```Console
CommerceScaleUnit.exe install -port 446 -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> Tomēr CSU (pašmitināta) konfigurācijas fails ir nepieciešams.

Šī komanda ir daudz precīzāka komanda, kas darbina izpildāmo failu instalētāju ar dažiem alternatīviem parametriem.

```Console
CommerceScaleUnit.exe install -Port 446 -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Verbosity 0 -Config "Contoso.StoreSystemSetup.xml"
```

Šī komanda norāda parametrus, kas nepieciešami, lai izlaistu priekšnosacījumu pārbaudes standarta instalācijas laikā. 

> [!NOTE]
> Pārbaužu izlaišana nav ieteicama bez pilnīgas pārbaudes pirms laika vai izstrādes situācijās.


```Console
CommerceScaleUnit.exe installer -skipscaleunithealthcheck -skipcertcheck -skipaadcredentialscheck -skipschannelcheck -skipiischeck -skipnetcorebundlecheck -skipsqlservercheck -skipnetframeworkcheck -skipversioncheck -skipurlcheck -Config "Contoso.StoreSystemSetup.xml" -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate
```

Šos konceptus var apvienot un saskaņot, lai sasniegtu vēlamos instalēšanas rezultātus.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
