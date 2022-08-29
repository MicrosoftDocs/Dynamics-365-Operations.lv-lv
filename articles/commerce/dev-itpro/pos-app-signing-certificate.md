---
title: Parakstīt MPOS .appx failu ar koda parakstīšanas sertifikātu
description: Šajā rakstā skaidrots, kā parakstīt MPOS ar koda parakstīšanas sertifikātu.
author: josaw1
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-09-2019
ms.custom: 28021
ms.openlocfilehash: bcf558b4b375078ed24777417e92b1c852f4c0eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282811"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>Parakstīt MPOS .appx failu ar koda parakstīšanas sertifikātu

[!include [banner](../includes/banner.md)]

Lai instalētu Modern POS (MPOS), jums jāparaksta MPOS programma ar koda parakstīšanas sertifikātu no uzticama nodrošinātāja un jāinstalē tas pats sertifikāts visās datorās, kur MPOS ir instalēts pašreizējā lietotāja uzticamajā saknes mapē.

Lai parakstītu MPOS programmu ar sertifikātu, lietojiet vienu no šīm opcijām failā **Retail SDK\\Build tool\\Customization.settings**:

- Pievienojiet būvējuma darbību drošā faila uzdevuma daļu Azure DevOps un augšupielādējiet sertifikātu, lai nodrošinātu faila uzdevumu. Izmantojiet drošā faila uzdevuma izvades ceļa mainīgo kā parametru failā Customization.settings.

    > [!NOTE]
    > Drošā faila uzdevums neatbalsta ar paroli aizsargātu sertifikātu. Pirms šī uzdevuma augšupielādes jums ir jānoņem parole. Tā kā sertifikāts ir augšupielādēts drošajā failu sistēmas uzdevumā azure, varat noņemt paroli tikai šai darbībai. Tomēr jums vajadzētu apspriest paroles noņemšanu ar drošības ekspertiem, lai noteiktu, vai šī ir pareizā darbība savam projektam. Nenoņemiet sertifikāta paroli citiem scenārijiem.
- Lietojiet sertifikātu, kas ir failu sistēmā. Lai to izdarītu, lejupielādējiet vai ģenerējiet sertifikātu un ievietojiet to failu sistēmā, kur tiek veidots. Microsoft viesotam aģentam vai kompilācijas lietotājam ir nepieciešama piekļuve šim ceļam un failam.
- Izmantojiet īssavilkumu, lai meklētu sertifikātu krātuvē un pieteiktos šajā sertifikātā.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Izmantot droša faila uzdevumu universālās Windows platformas programmas parakstīšanai

> [!NOTE]
> Lai saglabātu sertifikātu un lietotu Azure parakstītu Modern POS .appx failu un pašapkalpošanās instalētājus, varat arī izmantot Azure keyReģistrē, lai saglabātu sertifikātu. Parauga konveijera skriptus un papildinformāciju skatiet [sadaļā Būvējuma konveijera Azure DevOps iestatīšana mazumtirdzniecības pašapkalpošanās pakotņu ģenerēšanai](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

Universālajā Windows platformā (UWP) programmas parakstīšanai ieteicams izmantot drošu faila uzdevumu. Papildinformāciju par pakotnes parakstīšanu skatiet sadaļā Pakotnes [parakstīšanas konfigurēšana](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing). Šis process ir parādīts šajā attēlā.

![MPOS programmas parakstīšanas plūsma.](media/POSSigningFlow.png)

> [!NOTE]
> Pašlaik OOB iepakojums atbalsta parakstīšanu tikai .appx failu, dažādas pašapkalpošanās instalētāji, piemēram, MP ATG, MFU un HWS, šajā procesā nav parakstīti. Jums tas ir manuāli jāparaksta, izmantojot SignTool vai citus parakstīšanas rīkus. Sertifikātam, kas tiek izmantots .appx faila parakstīšanai, jābūt instalētam datorā, kurā ir instalēta Modern POS.

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Darbības, lai konfigurētu sertifikātu reģistrēšanai Azure konveijeros

### <a name="certificate-in-the-file-systemsecure-location"></a>Sertifikāts failu sistēmā/drošā vietā

Lejupielādējiet [uzdevumu DownloadFile](/visualstudio/msbuild/downloadfile-task) un pievienojiet to kā pirmo procesa soli. Drošā faila uzdevuma izmantošanas priekšrocība ir tāda, ka fails ir šifrēts un ievietots diskā būvējuma laikā neatkarīgi no tā, vai būvējuma konveijers ir veiksmīgs, neveiksmīgs vai atcelts. Fails tiek dzēsts no lejupielādes vietas pēc būvējuma procesa pabeigšanas.

1. Lejupielādējiet un pievienojiet uzdevumu Drošais fails kā pirmo soli Azure būvējuma konveijerā. Varat lejupielādēt Secure File uzdevumu no [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).
1. Augšupielādējiet sertifikātu drošā faila uzdevumā un iestatiet atsauces nosaukumu zem Izvades mainīgie, kā parādīts šajā attēlā.
    > [!div class="mx-imgBorder"]
    > ![Faila uzdevums ir nodrošināts.](media/SecureFile.png)
1. Izveidojiet jaunu mainīgo Azure konveijerā, cilnē **Mainīgie** atlasot **jaunu** mainīgo.
1. Norādiet mainīgā nosaukumu vērtības laukā, piemēram, **MySigningCert**.
1. Saglabājiet mainīgo.
1. **Atveriet Customization.settings** failu no **RetailSDK\\BuildTools** un atjauniniet **ModernPOSPackageCertificateKeyFile** ar mainīgā nosaukumu, kas izveidots konveijerā (3. darbība). Piemēram:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    Šī darbība ir nepieciešama, ja sertifikāts nav aizsargāts pret paroli. Ja sertifikāts ir aizsargāts pret paroli, veiciet šādas darbības.
    
1. Ja vēlaties laikspiedolu MPOS .appx failam, to parakstot ar sertifikātu, **atveriet Retail SDK\\ build\\ rīka pielāgošana.iestatījumu** **failu un atjauniniet ModernPOSPackageCertificateTimestamp** mainīgo ar laikspiedola nodrošinātāju (piemēram`http://timestamp.digicert.com`).
1. Konveijera mainīgo **cilnē pievienojiet** jaunu drošā teksta mainīgo. Iestatiet vārdu uz **MySigningCert.secret** un iestatiet sertifikāta paroles vērtību. Atlasiet slēga ikonu, lai nodrošinātu mainīgo.
1. Pievienojiet konveijeram **Powershell** skripta uzdevumu (pēc lejupielādes drošā faila un pirms darbības Veidot). Norādiet Parādāmo **nosaukumu** un iestatiet tipu kā **Inline**. Kopējiet un ielīmējiet tālāk norādīto sadaļā skripts.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. Atveriet **Customization.settings** failu no **RetailSDK\\BuildTools** un atjauniniet **ModernPOSPackageCertificateThumbprint** ar sertifikāta īssavilkuma vērtību.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
Detalizētu informāciju par to, kā iegūt sertifikāta īssavilkumu, [skatiet sadaļā sertifikāta īssavilkums](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint). 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>Lejupielādēt vai ģenerēt sertifikātu, lai manuāli parakstītu MPOS programmu, izmantojot msbuild sdk

Ja lejupielādētais vai ģenerētais sertifikāts tiek izmantots, lai parakstītu programmu MPOS, tad atjauniniet **ModernPOSPackageCertificateKeyFile** mezglu failā **BuildTools\\Customization.settings**, lai norādītu pfx faila atrašanās vietu (**$(SdkReferencesPath)\\appxsignkey.pfx**). Piemēram:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

Šajā gadījumā sertifikāta faila nosaukums ir **appxsignkey.pfx**, kas atrodas **Retail SDK\\ atsauces** mapē.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>Izmantojiet īssavilkumu, lai parakstītu MPOS programmu

Ja izmantojat īssavilkumu, lai parakstītu MPOS programmu, pēc tam instalējiet sertifikātu lokāli. Atjauniniet īssavilkuma **vērtību ModernPOSPackageCertificateThumbprint** **mezglā BuildTools\\Customization.settings** failā.

Šī opcija darbosies, ja būvējuma lietotājs ir lokālais lietotājs. Tomēr, ja Azure DevOps jūs izmantojat aģentus, lai ģenerētu būvējumu, tad aģentam var nebūt atļaujas piekļūt sertifikātu krātuvei, lai izmantotu sertifikātu parakstīšanai vai būvējuma datoram nebūs instalēts sertifikāts. Šajā gadījumā ir jāmaina būvējuma lietotājs pret lokālo lietotāju un jāinstalē sertifikāts lodziņā. Tomēr šī opcija nestrādās, ja jums nav administratora piekļuves lodziņam.

> [!NOTE]
> Ja uzdevuma opcija .pfx fails vai Secure File tiek izmantota programmas parakstam, **tad atstājiet ModernPOSPackageCertificateThumbprint** **zaru Customization.settings tukšu**. Ja tiek izmantota īssavilkuma opcija, atstājiet **ModernPOSPackageCertificateKeyFile tukšu**. Ja abas vērtības ir atjauninātas, tad būvējuma nebūs.

### <a name="certification-renewal"></a>Sertifikācijas atjaunošana

### <a name="renew-a-certificate-from-trusted-ca"></a>Sertifikāta atjaunošana no uzticama CA

Sazinieties ar savu sertifikātu izsniegšanas iestādi (CA) sertifikāta atjaunošanas procesam. Uzticamam sertifikātam MPOS pusē nav jāveic darbība.

### <a name="renew-a-self-signed-certificate"></a>Atjaunot paš parakstītu sertifikātu

Neizmantojiet parauga sertifikātu, kas ir pieejams ražošanas vienums Retail SDK. To var lietot tikai attīstības nolūkiem. Parauga Contoso sertifikātu nevar atjaunot, un Parauga sertifikāts, kas ietverts Retail SDK versijā 10.0.16 vai agrāk, beigsies 2020. gada 31. decembrī. Ja šis sertifikāts vai pats parakstīts sertifikāts tiek izmantots, lai parakstītu pielāgoto Modern POS, ir izteikta iespēja, ka Modern POS pēc šī datuma pareizi nefunkcionēs.
 
### <a name="impact"></a>Ietekme
 
Ja iepriekš minētais ir patiess attiecībā uz jums, problēma, ar kuru saskarsieties, ir tāda, ka instalētājs nevarēs darboties pēc 2020. gada 31. decembra. Atkarībā no izmantotās korporatīvās IT politikas Modern POS var nefunkcionēt. Lai noteiktu ietekmi uz jūsu organizāciju, ir būtiski to pārbaudīt, īslaicīgi mainot datumu uz vēlāku datumu.
 
### <a name="steps-to-determine-the-issue"></a>Soļi problēmas noteikšanai
 
1.  Izmantojiet Windows iestatījumus, lai mainītu datora pulksteni uz 2021. gada datumu un laiku.
2.  Pārbaudiet, vai Modern POS var atvērt, pieteikšanās var notikt un darbību var pabeigt.
3.  Pārbaudiet, vai Modern POS pašapkalpošanās instalētājs var tikt palaists un ja tā būs, ka instalēšana tiks veiksmīgi pabeigta.
4.  Atgrieziet Windows pulksteņa iestatījumus uz pareizo datumu un laiku.
 
Ja visas šīs darbības var veikt bez problēmām, tad būs iespējams darboties ar pašreizējo sertifikātu, kas ir pagājis 2020. gada 31. decembrī.  
 
### <a name="steps-going-forward"></a>Turpmākās darbības 

Ieteicams atjaunot iepriekš izmantoto sertifikātu. Ir ieteicams saņemt jaunu sertifikātu. Lai to paveiktu, jāveic kāda no šīm darbībām:
 
- **Vēlamais** — iegūstiet koda parakstīšanas sertifikātu no uzticamas sertifikātu iestādes.

- **Nav vēlamais** - izveidojiet lietošanai paš parakstītu koda parakstīšanas sertifikātu. Parasti tas tiek lietots vienīgi izstrādes nolūkos domēnā un netiek ieteikts ražošanai. 

- **Pieejams kā pagaidu risinājums — izmantojiet** atjaunoto Contoso koda parakstīšanas sertifikātu. Parasti tas tiek izmantots testēšanas nolūkiem, tāpēc to nav ieteicams izvietot ražošanā.
 
Pēc tam ģenerējiet jaunu pielāgoto Modern POS pakotni, kas ir parakstīta, izmantojot šo sertifikātu, kas iegūts no vienas no iepriekš minētajām darbībām. Atkarībā no sertifikāta ir jāveic viens no šiem soļiem:
 
- Ja izmantojat jaunu, uzticamu sertifikātu (vai jaunu, paš parakstītu sertifikātu), katrā ierīcē būs jāinstalē jauns sertifikāts. Pēc tam ir nepieciešams izmantot jaunizveidotu Modern POS pakotni (instalētāju), atinstalēt esošo programmu un pēc tam atkārtoti instalēt jauno Modern POS pakotni. Katrā ierīcē būs jāveic Modern POS ierīces aktivizēšana.

- Ja izmantojat atjaunoto Contoso sertifikātu, jums būs jāinstalē jaunais sertifikāts katrā ierīcē un jāinstalē Modern POS pakotne (instalētājs). Jums nav nepieciešams instalēt atinstalēšanu, tomēr jums ir atkārtoti jāinstalē šī ierīce. Ņemiet vērā, ka Modern POS ierīces aktivizēšana nebūs nepieciešama. Šī opcija ir pagaidu risinājums. Izmantojiet šo opciju tikai, lai izvairītos no atkārtotas aktivizēšanas un atrisinātu problēmu pirms jauna uzticama sertifikāta iegūšanas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
