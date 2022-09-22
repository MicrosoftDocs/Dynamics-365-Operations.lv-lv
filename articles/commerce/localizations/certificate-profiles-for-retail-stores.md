---
title: Lietotāja definēti sertifikātu profili mazumtirdzniecības veikaliem
description: Šajā rakstā ir sniegts pieejamo sertifikātu profilu apskats Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558442"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Lietotāja definēti sertifikātu profili mazumtirdzniecības veikaliem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pieejamo sertifikātu profilu apskats Microsoft Dynamics 365 Commerce. Šī funkcionalitāte paplašina līdzekli [Mazumtirdzniecības kanālu noslēpumu pārvaldība](../dev-itpro/manage-secrets.md), pievienojot atbalstu lokālajiem sertifikātiem.

Kamēr pārdošanas punkts (POS) darbojas bezsaistes režīmā, nevar piekļūt sertifikātiem, kas tiek glabāti atslēgas Microsoft Azure Arka. Tā vietā ir jāizmanto lokāls sertifikāts. Tālāk ir norādītas atbalstītās iespējas:

- Lokālo sertifikātu izmantošana atslēgas regresa scenārijos
- Lokālo sertifikātu izmantošana bez atslēgas Lomas (piemēram, telpu instalācijā)
- Pakāpeniska sertifikātu atjaunināšana, kur daži veikali un termināli izmanto jauno sertifikāta versiju, bet citi veikali un termināli turpina izmantot iepriekšējo versiju

Sertifikātu profilu funkcionalitāte ļauj norādīt noklusējuma sertifikātu un iestatīt kārtību, kādā tiek meklēti sertifikāti tajā pašā sertifikāta profilā. Šī funkcionalitāte arī nodrošina līdzīgu iestatīšanas pieeju lokālajiem sertifikātiem un Key Vault sertifikātiem. Varat pievienot uzņēmumam raksturīgos iestatījumus sertifikātiem, bet unikālu starpuzņēmumu identifikatoru katram sertifikātam var izmantot Commerce kanālos.

### <a name="scenarios"></a>Scenāriji

Sertifikātu profilu funkcionalitāte atbalsta šādus scenārijus pakalpojuma Commerce kanālos:

- Lietojiet lokālo sertifikātu Atslēgas lomas regresa scenārijos. Šie ir daži rezerves scenāriju piemēri:

    - Galvenās glabātuves krātuve nav pieejama.
    - Sertifikāts nav atrodams galvenās glabātuves krātuvē.
    - POS darbojas bezsaistes režīmā.

- Lietojiet lokālos sertifikātus, bet nesaglabājot tos atslēgas Tos (piemēram, telpu instalācijā).
- Pakāpeniska sertifikātu atjaunināšana, kur sertifikāta jaunā versija tiek izmantota tikai veikalos vai terminālos, kur jaunā versija jau ir pieejama.
- Viena un tā paša sertifikāta izmantošana vairākos uzņēmumos.

## <a name="set-up-certificate-profiles"></a>Sertifikātu profilu iestatīšana

Šajā procedūrā ir aprakstīts, kā iestatīt sertifikātu profilus.

### <a name="set-up-key-vault"></a>Iestata atslēgu Uzr.

Pirms izmantojat ciparsertifikātu, kas ir saglabāts Atslēgas lomas, ir jāveic tālāk norādītās darbības.

1. Izveidojiet Galvenās noliktavas kontu. Mēs iesakām izvietot glabāšanas kontu tādā pašā ģeogrāfiskā reģionā kā Commerce Scale Unit.
1. Augšupielādējiet ciparsertifikātu atslēgas glabāšanas kontā.
1. Autorizēt programmu Application Object Server (AOS) lasīt slepenos datus no glabāšanas konta Key Saņemšanas.

Papildinformāciju par to, kā strādāt ar atslēgas lomas laikā, skatiet sadaļā [Sākt darbu ar Azure atslēgas lomas](/azure/key-vault/key-vault-get-started).

### <a name="set-up-system-parameters"></a>Iestatīt sistēmas pamatparametrus

Pirms sertifikātu profilu konfigurēšanas Commerce kanālos jāiespējo commerce, lai lietotu abus sertifikātus, kas tiek glabāti Atslēgas Outlook un sertifikātu profilos.

Lai programmā Commerce Headquarters iestatītu sistēmas parametrus, veiciet šos soļus.

1. Lapā Sistēmas **parametri iestatiet** opciju Izmantot papildu **sertifikātu krātuvi** uz **Jā**.
1. Darbvietā **Līdzekļu pārvaldība** ieslēdziet līdzekli **Lietotāja definēti sertifikātu profili mazumtirdzniecības veikaliem**.

### <a name="set-up-key-vault-parameters"></a>Iestatīt atslēgas cogviju parametrus

Lai piekļūtu **atslēgas** noliktavas atslēgai, Ir jānorāda šādi parametri:

- **Atslēgas** **Bankas** glabāšanas konta nosaukums un apraksts.
- **Atslēgas Url —** Atslēgas Glabātavas konta URL.
- **AtslēgasFaila** klients – interaktīvā Azure Active Directory klienta ID programmā Azure AD, kas ir saistīta ar Atslēgas Noliktavas kontu autentifikācijas nolūkiem. Šim klientam ir jābūt piekļuvei, lai nolasītu noslēpumus no glabāšanas konta.
- **Atslēga Klienta slepenā** atslēga – slepenā Azure AD atslēga, kas ir saistīta ar lietojumprogrammu, kas tiek izmantota autentifikācijai Key Ganta glabāšanas kontā.
- **Vārds**, **apraksts** un slepenā **atsauce** – sertifikāta vārds, apraksts un slepenā atsauce.

Papildinformāciju skatiet Azure [atslēgas lomas klienta iestatīšana](../../finance/localizations/setting-up-azure-key-vault-client.md).

### <a name="configure-a-certificate-profile"></a>Konfigurēt sertifikāta profilu

Lai konfigurētu sertifikāta profilu programmā Commerce Headquarters, izpildiet šīs darbības.

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Sertifikātu profili**.
1. Lai izveidotu ierakstu, darbību rūtī atlasiet **Jauns**.
1. Ievadiet vērtības **laukos Sertifikāta profils** **·**, Nosaukums **un** Apraksts.

    > [!NOTE]
    > Sertifikāta profils ir unikāls sertifikāta identifikators visos uzņēmumos un Commerce komponentos.

1. Kopsavilkuma cilnē **Juridiskās** personas atlasiet **Pievienot**, lai pievienotu rindu.
1. Zem **Juridiskā persona** atlasiet juridisko personu (uzņēmumu), kam jāizmanto pašreizējais sertifikāta profils.

    Ja sertifikāta profils jālieto vairākām juridiskajām personām, atkārtojiet 4. un 5. darbību, lai pievienotu rindu katrai papildu juridiskajai personai.

1. Atlasiet **Iestatījumi**, lai atvērtu lapu **Sertifikāta profila iestatījumi**, kurā varat ievadīt uzņēmumam raksturīgos sertifikāta profila iestatījumus. Norādiet, kurus sertifikātus var izmantot, pašreizējā sertifikāta profila izsaukšanas komercijas kanālos. Pievienojiet tik daudz sertifikātu, cik nepieciešams, un iestatiet tiem prioritātes. Ja sertifikāts ar augstāku prioritāti nav pieejams, tiek izmantots nākamais sertifikāts, balstoties uz prioritāti. Papildinformāciju skatiet sadaļā [Darbplūsma: tiek meklēti sertifikāti Commerce Runtime](#workflow-searching-certificates-in-the-commerce-runtime) sadaļā.

    > [!NOTE]
    > Lauks **Prioritāte** tiek iestatīts automātiski. Vērtība **1** norāda augstāko prioritāti. Kad lapā **Sertifikāta profila iestatījumi** tiek pievienota jauna rinda, tās prioritāte tiek iestatīta uz skaitli, kas ir lielāks par iepriekšējās rindas prioritāti. Lai mainītu konkrētas rindas prioritāti, atlasiet rindu un pēc tam atlasiet **Pārvietot uz augšu**, lai palielinātu prioritāti, vai **Pārvietot uz leju**, lai samazinātu prioritāti.

1. Kad sertifikātu profila iestatījumu lapā pievienojat **jaunu rindu**, iestatiet šādus laukus:

    - **Atrašanās vietas tips** – atlasiet atrašanās vietu, kur sertifikāts ir saglabāts. Šim laukam ir divas iespējamās vērtības: **Lokāls sertifikāts** un **Key Vault**.
    - **Key Vault sertifikāts** – šis lauks ir obligāts, ja lauks **Atrašanās vietas tips** tiek iestatīts uz **Key Vault**. Izmantojiet to, lai norādītu Key Vault sertifikāta noslēpumu.
    - **Veikala nosaukums** – šis lauks ir neobligāts, un tas ir pieejams tikai iestatot lauku **Atrašanās vietas tips** uz **Lokāls sertifikāts**. Izmantojiet to, lai norādītu noklusējuma veikala nosaukumu, kas jāizmanto lokālo sertifikātu meklēšanai.
    - **Veikala atrašanās vieta** – šis lauks ir neobligāts, un tas ir pieejams tikai iestatot lauku **Atrašanās vietas tips** uz **Lokāls sertifikāts**. Izmantojiet to, lai norādītu noklusējuma veikala atrašanās vietu, kas jāizmanto lokālo sertifikātu meklēšanai.

        > [!NOTE]
        > Noklusējuma veikala nosaukums un veikala atrašanās vieta tiek pievienota, lai vienkāršotu lokālo sertifikātu meklēšanas procesu Commerce Runtime. X509StoreProvider satur sarakstu ar mapēm, kur tiek glabāti sertifikāti. Ja noklusējuma veikala nosaukums un noklusējuma krātuves atrašanās vieta nav norādītas, X509StoreProvider mēģina atrast sertifikātu citās saraksta mapēs. Papildinformāciju par pieejamām veikala nosaukuma un veikala atrašanās vietas vērtībām skatiet storeName [Enum](/dotnet/api/system.security.cryptography.x509certificates.storename) un [StoreLocation Enum](//dotnet/api/system.security.cryptography.x509certificates.storelocation).

    - **Īssavilkums** – šis lauks ir nepieciešams un ir pieejams tikai tad, ja novietojuma **tipa lauku** iestatāt uz **Lokālais sertifikāts**. Izmantojiet to, lai norādītu sertifikāta īssavilkumu.

        > [!IMPORTANT]
        > Jums jānodrošina, lai lietotājam, kurš darbina programmu, kam ir jāizmanto lokālais sertifikāts (piemēram, Modern POS bezsaistes režīmā), ir vismaz lasāma piekļuve sertifikāta privātai atslēgai.

    - **Komentāri** – šis lauks ir neobligāts, un tas ļauj lietotājiem ievadīt piezīmes.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Darbplūsma: sertifikātu meklēšana Commerce Runtime

Šī ir pamata darbplūsma, kas tiek izmantota, meklējot sertifikātu, kad sertifikāta profils tiek izsaukts Commerce Runtime.

1. Sistēma nosaka, vai sertifikāta profilā ir uzņēmumam raksturīgie iestatījumi pašreizējai juridiskajai personai.
1. Sistēma mēģina atrast sertifikātu, izmantojot vērtības, kas norādītas lapas **Sertifikāta profila iestatījumi** rindai, kur lauks **Prioritāte** ir iestatīts uz **1**.

    - Ja lauks **Atrašanās vietas tips** ir iestatīts uz **Key Vault**, tad lauka **Key Vault sertifikāta noslēpums** vērtība tiek izmantota, lai meklētu sertifikātu lapā **Galvenās glabātuves parametri**. Pēc tam sertifikāts tiek meklēts galvenās glabātuves krātuvē.
    - Ja lauks **Atrašanās vietas tips** ir iestatīts uz **Lokāls sertifikāts**, tad X509StoreProvider vispirms meklē sertifikātu, izmantojot noklusējuma veikala nosaukumu un veikala atrašanās vietu, ja šie parametri ir norādīti. Pēc tam tas meklē visās citās mapēs, kas atrodas mapju sarakstā.

1. Ja sertifikāts netiek atrasts, process tiek atkārtots ar rindu, kurā lauks **Prioritāte** ir iestatīts uz **2**, un tā tālāk.

> [!NOTE]
> Sertifikāts netiek atrasts, ja sertifikāta profilam nav iestatījumu pašreizējai juridiskajai personai, vai ja sertifikāta meklēšana ir neveiksmīga visām rindām lapā **Sertifikāta profila iestatījumi**.

### <a name="caching-the-results-of-certificate-searches"></a>Sertifikātu meklēšanas rezultātu kešdarbe

Sertifikātu meklēšanas rezultāti tiek saglabāti kešatmiņā. Kešatmiņas noklusējuma derīguma termiņš ir viena stunda. Tomēr šo termiņu var pielāgot un iestatīt uz maksimālo 24 stundu vērtību.

## <a name="gradual-update"></a>Pakāpeniska atjaunināšana

Ja tiek ieviesta jauna sertifikāta versija, ko nevar atjaunināt visos veikalos vienlaicīgi, sertifikātu profilu funkcionalitāte ļauj sertifikātu atjaunināt pakāpeniski.

1. Atrodiet sertifikāta profilu un rindu, kas jāatjaunina, un pēc tam atlasiet **Iestatījumi**.
1. Pievienojiet rindu un norādiet iestatījumus, kas saistīti ar jaunāko sertifikāta versiju.
1. Palieliniet jaunās rindas **Prioritāte** vērtību. Izmantojiet pogu **Pārvietot uz augšu**, lai pārvietotu rindu tā, lai tā būtu virs tā paša sertifikāta iepriekšējās versijas rindas.
> [!NOTE]
> Vispirms jaunā sertifikāta versija tiks izsaukta Commerce Runtime. Ja sertifikāts vēl nav atjaunināts noteiktā veikalā vai noteiktā terminālī, tiks izsaukta iepriekšējā versija.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
