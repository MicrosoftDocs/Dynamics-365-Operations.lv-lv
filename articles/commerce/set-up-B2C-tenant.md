---
title: B2C nomnieka iestatīšana programmā Commerce
description: Šajā tēmā aprakstīts, kā iestatīt Azure Active Directory (Azure AD) biznesa-patērētāju (B2C) nomniekus lietotāja vietas autentifikācijai sistēmā Dynamics 365 Commerce.
author: BrianShook
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: dcd5c022c00070922e287a6b8750810ff76bc26f
ms.sourcegitcommit: 39f1455215e0363cd1449bbc6bdff489097f9ded
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092463"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>B2C nomnieka iestatīšana programmā Commerce

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā iestatīt Azure Active Directory (Azure AD) biznesa-patērētāju (B2C) nomniekus lietotāja vietas autentifikācijai sistēmā Dynamics 365 Commerce.

Dynamics 365 Commerce izmanto Azure AD B2C, lai atbalstītu lietotāja akreditācijas datus un autentifikācijas plūsmas. Lietotājs var pieteikties, pierakstīties un atiestatīt savu paroli, izmantojot šīs plūsmas. Azure AD B2C saglabā lietotāja sensitīvo autentifikācijas informāciju, piemēram, lietotāja vārdu un paroli. Lietotāja ieraksts B2C nomniekā saglabās vai nu B2C lokālā konta ierakstu, vai arī B2C sociālā identitātes nodrošinātāja ierakstu. Šie B2C ieraksti tiks saistīti ar klienta ierakstu tirdzniecības vidē.

> [!WARNING] 
> Azure AD B2C atiestata veco (mantojuma) lietotāju plūsmas uz 2021. gada 1. augustu. Tādēļ jums jāplāno migrēt savas lietotāja plūsmas uz jauno ieteicamo versiju. Jaunā versija nodrošina līdzekļu pārību un jaunas funkcijas. Ar ieteiktajām B2C lietotāju plūsmām ir jāizmanto Commerce versijas 10.0.15 vai jaunāka moduļa bibliotēka. Papildinformāciju skatiet sadaļā [Lietotāju darbplūsmas Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Commerce novērtēšanas vidēs ir iepriekš ielādēts Azure AD B2C nomnieks demonstrācijas nolūkiem. Paša Azure AD B2C nomnieka ielādēšana, izmantojot tālāk aprakstītās darbības, nav nepieciešama novērtēšanas vidēm.

> [!TIP]
> Jūs varat turpmāk aizsargāt savus vietas lietotājus un uzlabot savu Azure AD B2C nomnieku drošību ar Azure AD identitātes aizsardzību un nosacījuma piekļuvi. Lai pārskatītu Azure AD B2C Premium P1 un Premium P2 nomniekiem pieejamās iespējas, skatiet [Pakalpojuma Azure AD B2C identitātes aizsardzība un nosacījuma piekļuve](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>Dynamics vides priekšnosacījumi

Pirms sākat, nodrošiniet, lai jūsu Dynamics 365 Commerce vide un e-komercijas kanāls tiktu atbilstoši konfigurēti, izpildot tālāk norādītos priekšnosacījumus.

- Iestatiet POS operāciju vērtību **AllowAnonymousAccess** uz "1" programmā Commerce Headquarters:
    1. Pārejiet uz **POS operācijām**.
    1. Operāciju režģī noklikšķiniet ar peles labo pogu un atlasiet **Personalizēt**.
    1. Atlasiet **Pievienot lauku**.
    1. Pieejamo kolonnu sarakstā atlasiet kolonnu **AllowAnonymousAccess**, lai to pievienotu.
    1. Atlasiet **Atjaunināt**.
    1. Operācijai **612** "Debitora pievienošana" mainiet **AllowAnonymousAccess** uz "1."
    1. Izpildiet darbu **1090 (Reģistri)**.
- Programmā Commerce Headquarters iestatiet numuru sērijas debitora konta **Manuālo** atribūtu uz **Nē**:
    1. Dodieties uz **Retail un Commerce \> Headquarters iestatīšana \> Parametri \> Debitoru parametri**.
    1. Atlasīt **Numuru sērijas**.
    1. Rindā **Debitora konts** veiciet dubultklikšķi uz vērtības **Numura sērijas kods**.
    1. Numuru sērijas kopsavilkuma cilnē **Vispārīgi** iestatiet **Manuāli** uz **Nē**.

Pēc vides Dynamics 365 Commerce izvietošanas ir ieteicams arī [Inicializēt sākumdatus](enable-configure-retail-functionality.md) vidē.

## <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Izveidojiet vai izveidojiet saiti uz esošu Azure AD B2C nomnieks Azure portālā

Šajā sadaļā ir aprakstīta e-pasta izveide vai saistīšana Azure AD B2C nomnieks lietošanai jūsu tirdzniecības vietnē. Papildinformāciju skatiet [Apmācība: izveidojiet Azure Active Directory B2C īrnieks](/azure/active-directory-b2c/tutorial-create-tenant).

1. Pierakstieties [Azure portālā](https://portal.azure.com/).
1. No Azure portāla izvēlnes atlasiet **Izveidot resursu**. Noteikti izmantojiet abonementu un direktoriju, kas tiks savienots ar jūsu komercijas vidi.

    ![Resursa izveide Azure portālā.](./media/B2CImage_1.png)

1. Doties uz **Identitātes \> Azure Active Directory B2C**.
1. Kad atrodaties lapā **Izveidot jaunu B2C nomnieku vai saistīt uz esošo nomnieku**, izmantojiet vienu no zemāk norādītajām opcijām, kas vislabāk atbilst jūsu uzņēmuma vajadzībām:

    - **Izveidojiet jaunu Azure AD B2C īrnieks** : izmantojiet šo opciju, lai izveidotu jaunu Azure AD B2C īrnieks.
        1. Atlasiet **Izveidot jaunu Azure AD B2C nomnieku**.
        1. Sadaļā **Organizācijas nosaukums** ievadiet organizācijas nosaukumu.
        1. Sadaļā **Sākotnējais domēna nosaukums** ievadiet sākotnējo domēna nosaukumu.
        1. Sadaļā **Valsts vai reģions** atlasiet valsti vai reģionu.
        1. Atlasiet **Izveidot**, lai izveidotu nomnieku.

     ![Izveidot jaunu Azure AD nomnieku.](./media/B2CImage_2.png)

     - **Saistīt esošu Azure AD B2C nomnieku uz manu Azure abonementu**: lietojiet šo opciju, ja jums jau ir Azure AD B2C nomnieks, ar kuru vēlaties veidot saiti.
        1. Atlasiet **Saistīt esošu Azure AD B2C nomnieku uz manu Azure abonementu**.
        1. Sadaļā **Azure AD B2C nomnieks** atlasiet atbilstošo B2C nomnieku. Ja atlasīšanas lodziņā tiek parādīts ziņojums "Nevar atrast piemērotus B2C nomniekus", jums nav esoša piemērota B2C nomnieka, un jums būs jāizveido jauns.
        1. Sadaļā **Resursu grupa** atlasiet **Izveidot jaunu**. Ievadiet **Nosaukumu** resursu grupai, kurā būs nomnieks, atlasiet **Resursu grupas atrašanās vietu** un pēc tam atlasiet **Izveidot**.

    ![Saistīt esošu Azure AD B2C nomnieku uz Azure abonementu.](./media/B2CImage_3.png)

1. Kad tiek izveidots jauns Azure AD B2C direktorijs (tas var ilgt kādu brīdi), saite uz jauno direktoriju parādīsies informācijas panelī. Šī saite novirzīs jūs uz lapu "Laipni lūdzam Azure Active Directory B2C".

    ![Saite uz jauno Azure AD Direktorija](./media/B2CImage_4.png)

> [!NOTE]
> Ja jūsu Azure kontā ir vairāki abonementi vai arī esat iestatījis B2C nomnieku, neveidojot saiti uz aktīvu abonementu, reklāmkarogs **Problēmu novēršana** jūs novirzīs, lai palīdzētu saistīt nomnieku ar abonementu. Atlasiet problēmu novēršanas ziņojumu un izpildiet norādījumus, lai atrisinātu abonementa problēmu.

Šis attēls rāda Azure AD B2C **Problēmu novēršanas** reklāmkaroga piemēru.

![Brīdinājumam, kas rāda direktoriju, nav aktīva abonementa.](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>Izveidot B2C pieteikumu

Kad B2C nomnieks ir izveidots, jūs izveidosiet B2C pieteikumu jaunajā Azure AD B2C nomniekā, lai mijiedarbotos ar tirdzniecības darbībām.

Lai izveidotu B2C pieteikumu, izpildiet tālāk aprakstītās darbības.

1. Azure portālā atlasiet **Lietotnes reģistrācijas**, tad atlasiet **Jauna reģistrācija**.
1. Sadaļā **Nosaukums** ievadiet nosaukumu, kas jāpiešķir Azure AD šai B2C programmai.
1. Zem **Atbalstītie kontu tipi** atlasiet **Konti jebkurā identitātes nodrošinātājā vai organizācijas direktorijā (autentifikācijai lietotājiem ar lietotāju plūsmām)**.
1. Lai **Novirzītu URI**, ievadiet atvēlētos atbildes vietrāžus URL kā **Web** veidu. Skatiet zemāk [Atbildes vietrāži URL](#reply-urls), lai iegūtu informāciju par atbildes vietrāžiem URL un to formatēšanu. Lai iespējotu novirzīšanu no, ir jāievada novirzīšanas URI/atbildes URL Azure AD B2C atpakaļ uz jūsu vietni, kad lietotājs autentificējas. Atbildes URL var pievienot reģistrācijas procesa laikā vai to var pievienot vēlāk, atlasot **Pievienojiet novirzīšanas URI** saite no **Pārskats** izvēlne B2C lietojumprogrammā **Pārskats** sadaļā.
1. **Atļaujām** atlasiet **Piešķirt administratoru atļauju openid un offline_access atļaujas**.
1. Atlasiet **Reģistrēt**.
1. Atlasiet jaunizveidoto lietojumprogrammu un dodieties uz **Autentifikācija** izvēlne. 
1. Ja ir ievadīts atbildes URL, sadaļā **Netiešās dotācijas un hibrīdās plūsmas** atlasiet abus **Piekļuves marķieri** un **ID marķieri** opcijas, lai tās iespējotu lietojumprogrammai, un pēc tam atlasiet **Saglabāt**. Ja reģistrācijas laikā atbildes URL netika ievadīts, to var pievienot arī šajā lapā, atlasot **Pievienojiet platformu**, izvēloties **Web** un pēc tam ievadiet lietojumprogrammas novirzīšanas URI. The **Netiešās dotācijas un hibrīdās plūsmas** sadaļa būs pieejama, lai atlasītu abus **Piekļuves marķieri** un **ID marķieri** iespējas.
1. Dodieties uz **Pārskata** izvēlni portālā Azure un nokopējiet **Programmas (klienta) ID**. Ievērojiet šo ID vēlākām uzstādīšanas darbībām (vēlāk norādīts kā **Klienta GUID**).

Lai iegūtu papildu atsauci uz Programmu reģistrācijām Azure AD B2C, lūdzu, skatiet [Jauno programmas reģistrāciju pieredzi Azure Active Directory B2C](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Atbilžu vietrāži URL

Atbilžu vietrāži URL ir svarīgi, jo tie nodrošina atgriešanās domēnus iekļaut sarakstā, kad jūsu vietne Azure AD B2C pieprasa autentificēt lietotāju. Tas ļauj atgriezt autentificētu lietotāju atpakaļ domēnā, no kura tie piesakās sistēmā (jūsu vietnes domēns). 

Lodziņā **Atbilžu vietrāži URL** ekrānā **Azure AD B2c - Applications \> Jauna programma** jums ir jāpievieno atsevišķas rindas gan jūsu vietnes domēnam, gan (tiklīdz jūsu vide ir nodrošināta) komercijas ģenerētajam vietrādim URL. Šiem URL vienmēr ir jāizmanto derīgs URL formāts, un tiem ir jābūt tikai pamata URL (bez slīpsvītrām vai ceļiem). Pēc tam ``/_msdyn365/authresp`` virkne ir jāpievieno pamata URL, kā tas ir sekojošajos piemēros.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Domēnam ir pilnībā jāatbilst e-komercijas domēnam. Ja izmantojat vairākus domēnus, šis URL ir jāpievieno katram domēnam.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a>Lietotāja plūsmas izveide

Lietotājas plūsmas ir politika, ko Azure AD B2C izmanto, lai nodrošinātu drošu pieteikšanos sistēmā, pierakstītos, rediģētu profilu un aizmirstas paroles gadījumos. Dynamics 365 Commerce izmanto šīs plūsmas, lai veiktu politikas darbības, lai mijiedarbotos ar Azure AD B2C nomnieku. Kad lietotājs mijiedarbojas ar šīm politikām, tās tiek novirzītas uz Azure AD B2C nomnieku, lai veiktu darbības.

Azure AD B2C sniedz trīs pamata lietotāju plūsmas tipus:
- Pierakstīties un pieteikties
- Profila labošana
- Paroles atiestatīšana

Varat izvēlēties izmantot noklusējuma lietotāju plūsmas, ko nodrošina Azure AD, kurā tiks parādīta lapa, ko mitina Azure AD B2C. Līdzīgi varat izveidot HTML lapu, lai kontrolētu šo lietotāju plūsmas pieredzes izskatu un iespaidu. 

Lai pielāgotu lietotāja politikas lapas Dynamics 365 Commerce, skatiet sadaļu [Pielāgotu lapu iestatīšana lietotāju pieteikšanās tiesībām](custom-pages-user-logins.md). Papildinformāciju skatiet sadaļā [Lietotāja pieredzes interfeisa pielāgošana Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Izveidot pierakstīšanos un pieteikties lietotāja plūsmas politikā

Lai izveidotu Parakstīšanos un pierakstīšanos lietotāja plūsmā politiku, veiciet tālāk minētās darbības.

1. Azure portālā kreisajā navigācijas rūtī atlasiet **Lietotāju plūsmas (politikas)**.
1. Lapā **Azure AD B2C — lietotāja plūsmas (politikas)** atlasiet **Jauna lietotāja plūsma**.
1. Atlasiet **Pierakstīšanās un reģistrācijas** politiku, tad atlasiet versiju **Ieteikts**.
1. Sadaļā **Nosaukums** ievadiet politikas nosaukumu. Pēc tam šis nosaukums tiks parādīts ar prefiksu, kuru portāls piešķir (piemēram, "B2C_1_").
1. Zem **Identitātes nodrošinātāji**, iekš **Vietējie konti** sadaļu, atlasiet **E-pasta pierakstīšanās**. E-pasta autentifikācija tiek izmantota visbiežāk sastopamajos Commerce scenārijos. Ja izmantojat arī sociālās identitātes nodrošinātāja autentifikāciju, tos var atlasīt arī šobrīd.
1. Saskaņā ar **Daudzfaktoru autentifikāciju** atlasiet atbilstošo jūsu uzņēmuma izvēli. 
1. Sadaļā **Lietotāja atribūti un prasības** atlasiet opcijas, lai apkopotu atbilstošos atribūtus vai atgriešanas prasības. Izvēlieties **Parādīt vairāk...** lai iegūtu pilnu atribūtu un pretenziju opciju sarakstu. Commerce ir nepieciešamas šādas noklusējuma opcijas:

    | **Savākt atribūtu** | **Atgriešanas prasība** |
    | ---------------------- | ----------------- |
    | E-pasta adrese          | E-pasta adreses   |
    | Norādītais nosaukums             | Norādītais nosaukums        |
    |                        | Identitātes nodrošinātājs |
    | Uzvārds                | Uzvārds           |
    |                        | Lietotāja objekta ID  |

1. Atlasiet **Izveidot**.

Tālāk minētais attēls ir Azure AD B2C reģistrācijas un pieteikšanās piemērs lietotāja plūsmā.

![Parakstīšanās un pieteikšanās politikas iestatījumi.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Izveidot profila rediģēšanas lietotāja plūsmas politiku

Lai izveidotu profila rediģēšanas lietotāja plūsmas politiku, veiciet tālāk minētās darbības.

1. Azure portālā kreisajā navigācijas rūtī atlasiet **Lietotāju plūsmas (politikas)**.
1. Lapā **Azure AD B2C — lietotāja plūsmas (politikas)** atlasiet **Jauna lietotāja plūsma**.
1. Atlasiet **Profila rediģēšana** un pēc tam atlasiet **Ieteicamo** versiju.
1. Sadaļā **Nosaukums** ievadiet profila rediģēšanas lietotāja plūsmu. Pēc tam šis nosaukums tiks parādīts ar prefiksu, kuru portāls piešķir (piemēram, "B2C_1_").
1. Zem **Identitātes nodrošinātāji**, iekš **Vietējie konti** sadaļu, atlasiet **Pierakstīšanās pa e-pastu**.
1. Sadaļā **Lietotāja atribūti** atlasiet kādu no tālāk norādītajām izvēles rūtiņām:
    
    | **Savākt atribūtu** | **Atgriešanas prasība** |
    | ---------------------- | ----------------- |
    |                        | E-pasta adreses   |
    | Norādītais nosaukums             | Norādītais nosaukums        |
    |                        | Identitātes nodrošinātājs |
    | Uzvārds                | Uzvārds           |
    |                        | Lietotāja objekta ID  |
    
1. Atlasiet **Izveidot**.

Sekojošajā attēlā parādīts piemērs ar Azure AD B2C profila rediģēšanas lietotāja plūsmu.

![Piemērs Azure AD B2C profila rediģēšanas lietotāju plūsma](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Izveidot paroles atiestatīšanas lietotāja plūsmas politiku

Lai izveidotu paroles atiestatīšanas lietotāja plūsmas politiku, veiciet tālāk minētās darbības.

1. Azure portālā kreisajā navigācijas rūtī atlasiet **Lietotāju plūsmas (politikas)**.
1. Lapā **Azure AD B2C — lietotāja plūsmas (politikas)** atlasiet **Jauna lietotāja plūsma**.
1. Atlasiet **Profila rediģēšana** un pēc tam atlasiet **Ieteicamo** versiju.
1. Sadaļā **Nosaukums** ievadiet paroles atiestatīšanas lietotāja plūsmas nosaukumu.
1. Sadaļā **Identitātes nodrošinātāji** atlasiet **Atiestatīt paroli, izmantojot e-pasta adresi**.
1. Atlasiet **Izveidot**.
1. Sadaļā **Pieteikumu prasības** atlasiet kādu no tālāk norādītajām izvēles rūtiņām:
    - **E-pasta adreses**
    - **Norādītais nosaukums**
    - **Uzvārds**
    - **Lietotāja objekta ID**
1. Atlasiet **Izveidot**.

Sekojošajā attēlā parādīts, kur iestatīt **Atiestatīšanas paroli, izmantojot pasta adresi** Azure AD B2C paroles atiestatīšanas lietotāja plūsmā.

![Iestatiet "Atiestatīt paroli, izmantojot pasta adresi" paroles atiestatīšanas politikā](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a>Pievienot sociālās identitātes sniedzējus (pēc izvēles)

Sociālās identitātes nodrošinātāji ļauj lietotājiem izmantot savu sociālā konta autentifikāciju. Sociālās identitātes nodrošinātāja autentifikācijas pievienošana nav obligāta risinājumā Dynamics 365 Commerce. 

Ja nav pievienota sociālā identitātes nodrošinātāja autentifikācija, noklusējuma Azure AD B2C profili būs galvenie profili jūsu lietotāja bāzei. Lietotāji atlasīs savu lietotājvārdu (viņu vēlamo e-pasta adresi) un iestatīs paroli. Azure AD B2C lietotājiem tiks autentificēti tieši. 

Ja tiek pievienota sociālā identitātes nodrošinātāja autentifikācija un lietotājs izvēlas vienu no piedāvātajiem sociālās identitātes nodrošinātājiem, tas joprojām ir izveidots ar Azure AD B2C nomniekā. Pēc tam Azure AD B2C autentificēs lietotāja akreditācijas datus ar sociālās identitātes nodrošinātāju.

> [!NOTE]
> Identitātes nodrošinātāja žurnāls izveido ierakstu B2C nomniekā, bet citā formātā, nekā Lokālais konts, jo tas izsauc ārējās sociālās identitātes sniedzēja atsauci autentifikācijai. Lietotājs var izmantot vienu un to pašu e-pasta adresi sociālo identitātes nodrošinātāju starpā, kas nozīmē, ka Autentifikācijai izmantotais e-pasta lietotājvārds var nebūt unikāls nomniekam. Azure AD B2C tikai realizēs to, ka lietotājiem ir unikāla e-pasta adrese vietējos B2C kontos.

Pirms jūs varat pievienot sociālās identitātes nodrošinātāju autentifikācijai, jums ir jādodas uz identitātes nodrošinātāja portālu un jāiestata identitātes nodrošinātāja programma, kā norādīts Azure AD B2C dokumentācijā. Tālāk ir sniegts saraksts ar saitēm uz dokumentāciju.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Viens nomnieks)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft konts](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Pievienot un iestatīt sociālās identitātes nodrošinātāju

Lai pievienotu un iestatītu sociālās identitātes nodrošinātāju, veiciet šīs darbības.  

1. Azure portālā dodieties uz **Identitātes nodrošinātājiem**.
1. Atlasiet **Pievienot**. Parādās ekrāns **Pievienot identitātes nodrošinātāju**.
1. Sadaļā **Nosaukums** ievadiet nosaukumu, kas jāparāda lietotājiem jūsu pieteikšanās ekrānā.
1. Sadaļā **Identitātes nodrošinātāja tips** no saraksta atlasiet identitātes nodrošinātāju.
1. Atlasiet **Labi**.
1. Atlasiet **Iestatīt šo identitātes nodrošinātāju**, lai piekļūtu ekrānam **Iestatīt sociālās identitātes nodrošinātāja**.
1. Sadaļā **Klienta ID** ievadiet klienta ID, kas iegūts no identitātes nodrošinātāja programmas uzstādīšanas.
1. Sadaļā **Klienta slepenā atslēga** ievadiet klienta slepeno atslēgu, kas iegūts no identitātes nodrošinātāja programmas uzstādīšanas.
1. Pievienojiet lietotāja plūsmu žurnālam piesakieties politikām:
1. Doties uz **Azure AD B2C — lietotāja plūsmas (politikas) \> {jūsu pierakstīšanās/pieteikšanās politika} \> identitātes nodrošinātāji**.
1. Lai pievienotu pieteikšanos/pierakstīšanos lietotāja plūsmas politikai, atlasiet katru identitātes nodrošinātāju, ko esat iestatījis savam kontam. Lai pārbaudītu tos, atlasiet **Palaist lietotāja plūsmu** katram identitātes nodrošinātājam. Jauna cilne parādīs pieteikšanās lapu, parādot jauno identitātes nodrošinātāju atlases lodziņu.

Sekojošajā attēlā ir redzami **Pievienot identitātes nodrošinātāju** un **Uzstādīt sociālo identitātes nodrošinātāju** ekrāna piemēri Azure AD B2C.

![Sociālās identitātes nodrošinātāja pievienošana jūsu aplikācijai.](./media/B2CImage_14.png)

Sekojošajā attēlā parādīts piemērs, kā atlasīt identitātes nodrošinātājus Azure AD B2C **Identitātes nodrošinātāju** lapā.

![Atlasiet katru Sociālā identitātes nodrošinātāju, lai iespējotu politiku.](./media/B2CImage_16.png)

Sekojošajā attēlā parādīts noklusējuma pierakstīšanās ekrāna piemērs, kurā ir parādīts sociālās identitātes nodrošinātāja pierakstīšanās poga.

> [!NOTE]
> Ja jūsu lietotāju plūsmām izmantojat sistēmā Commerce iebūvētās pielāgotās lapas, pogas sociālās identitātes nodrošinātājiem jāpievieno, izmantojot Commerce moduļu bibliotēkas paplašināmības līdzekļus. Turklāt, iestatot programmas ar īpašu sociālās identitātes nodrošinātāju, dažos gadījumos URL vai konfigurācijas virknes var būt reģistrjutīgas. Plašākai informācijai meklējiet sava sociālās identitātes nodrošinātāja savienojuma norādījumus.
 
![Tiek parādīts noklusētais pieteikšanās ekrāns ar sociālās identitātes nodrošinātāja pierakstīšanās pogu.](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Atjaunināt Commerce Headquarters ar jauno Azure AD B2C informāciju

Pēc tam, kad iepriekšminētās Azure AD B2C nodrošināšanas darbības ir pabeigtas, Azure AD B2C lietojumprogrammai ir jābūt reģistrētai jūsu Dynamics 365 Commerce vidē.

Lai atjauninātu programmu Headquarters ar jauno Azure AD B2C informāciju, veiciet sekojošās darbības.

1. Programmā Commerce dodieties uz **Commerce koplietotie parametri** un atlasiet **Identitātes nodrošinātāji** kreisajā izvēlnē.
1. Sadaļā **identitātes nodrošinātāji** veiciet sekojošās darbības:
    1. Lodziņā **Izdevējs** ievadiet identitātes nodrošinātāja izdevēja URL. Lai atrastu savu izdevēja URL, zemāk skatiet [Iegūt izdevēja URL](#obtain-issuer-url).
    1. Lodziņā **Nosaukums** ievadiet izdevēja ieraksta nosaukumu.
    1. Lodziņā **Veids** ievadiet **Azure AD B2C (id_token)**.
1. Sadaļā **Pārbaudītāji** ar iepriekš atlasīto B2C identitātes nodrošinātāja vienumu rīkojieties šādi:
    1. Lodziņā **ClientID** ievadiet savu B2C programmas ID. To varat atrast jūsu B2C programmas rekvizītu lapas lodziņā **Programmas ID**.
    1. Lodziņā **Veids** ievadiet **Publisks**.
    1. Lodziņā **Lietotāja veids** ievadiet **Pircējs**.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Lodziņā Commerce Search meklējiet **Sadales grafiku**
1. Lapas **Sadales grafiki** kreisajā navigācijas izvēlnē atlasiet darbu **1110 globālā konfigurācija**.
1. Darbību rūtī atlasiet **Palaist tagad**.

### <a name="obtain-issuer-url"></a>Iegūt izdevēja URL

Lai iegūtu identitātes nodrošinātāja izdevēja URL, rīkojieties šādi.
1. Azure Azure AD portāla B2C lapā dodieties uz **Pierakstīšanās un reģistrēšanās** lietotāju plūsmu.
1. Kreisajā navigācijas izvēlnē atlasiet **Lapas izkārtojumi** sadaļā **Izkārtojuma nosaukums** atlasiet **Unificētā pierakstīšanās vai pieteikšanās lapa** un pēc tam atlasiet **Palaist lietotāju plūsmu**.
1. Pārliecinieties, ka programma ir iestatīta uz iepriekš izveidoto paredzēto Azure AD B2C programmu, un pēc tam atlasiet saiti galvenē **Palaist lietotāja plūsmu**, kurā ir ietverts ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``.
1. Jūsu pārlūka cilnē tiek parādīta metadatu lapa. Kopējiet identitātes nodrošinātāja izsniedzēja URL ( **"izsniedzēja"** vērtību).
   - Piemērs: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**VAI**: Lai manuāli izveidotu to pašu metadatu URL, veiciet šādas darbības.

1. Izveidot metadatu adreses URL šādā formātā, izmantojot B2C nomnieku un politiku: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Piemērs: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Ievadiet metadatu adreses URL pārlūkprogrammas adreses joslā.
1. Metadatos kopējiet identitātes nodrošinātāja izdevēja URL ( **"izdevēja"** vērtība).
    - Piemērs: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Konfigurējiet savu B2C nomnieku Commerce vietņu veidotājā

Kad jūsu Azure AD B2C nomnieka iestatīšana ir pabeigta, jums ir jākonfigurē B2C nomnieks Commerce vietņu veidotājā. Konfigurēšanas soļi ietver B2C lietojumprogrammas informācijas vākšanu no Azure portāla, ievadot šo B2C lietojumprogrammas informāciju vietņu veidotājā un pēc tam asociējot B2C programmu ar jūsu vietni un kanālu.

### <a name="collect-the-required-application-information"></a>Apkopot nepieciešamo programmas informāciju

Lai apkopotu nepieciešamo informāciju par programmu, veiciet šīs darbības.

1. Portālā Azure dodieties uz **Mājas \>Azure AD B2C — lietotņu reģistrācija**.
1. Atlasiet savu lietojumprogrammu un pēc tam kreisajā navigācijas rūtī atlasiet **Pārskats** lai iegūtu informāciju par pieteikumu.
1. No **Lietojumprogrammas (klienta) ID** atsauci, apkopojiet B2C lietojumprogrammas ID, kas izveidota jūsu B2C nomniekā. Tas vēlāk tiks ievadīts kā **Klienta GUID** vietņu veidotājā.
1. Izvēlieties **Novirzīt URI** un apkopojiet jūsu vietnei parādīto atbildes URL (atbildes URL, kas tika ievadīts iestatīšanas laikā).
1. Iet uz **Mājas \>Azure AD B2C — lietotāju plūsmas** un pēc tam apkopojiet katras lietotāja plūsmas politikas pilnus nosaukumus.

Nākamajā attēlā ir parādīts piemērs **Azure AD B2C — lietotņu reģistrācija** pārskata lapa.

![Azure AD B2C — lietotņu reģistrāciju pārskata lapa ar izceltu lietojumprogrammas (klienta) ID](./media/ClientGUID_Application_AzurePortal.png)

Sekojošajā attēlā ir parādīts lietotāja plūsmas politikas piemērs, kas norādīts **Azure AD B2C — lietotāja plūsmas (politikas)** lapā.

![Apkopot katras B2C politikas plūsmas nosaukumus.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Ievadiet savu Azure AD B2C īrnieka pieteikuma informācija Commerce

Jums jāievada Azure AD B2C nomnieka informācija Commerce vietņu veidotājā, pirms asociējat B2C nomnieku ar jūsu vietnēm.

Lai pievienotu savu Azure AD B2C nomnieka pieteikuma informācija Commerce, veiciet šīs darbības.

1. Piesakieties kā administrators Commerce vietņu veidotājā jūsu videi.
1. Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi**, lai to izvērstu.
1. Sadaļā **Nomnieka iestatījumi** atlasiet **B2C iestatījumi**. 
1. Galvenajā logā blakus **B2C lietojumprogrammas** atlasiet **Pārvaldīt**. (Ja jūsu nomnieks parādās B2C lietojumprogrammu sarakstā, tad administrators to jau ir pievienojis. Pārbaudiet, vai vienumi 6. solī atbilst jūsu B2C lietojumprogrammai.)
1. Atlasiet **Pievienot B2C lietojumprogrammas**.
1. Veidlapā ievadiet tālāk norādītos pieprasītos vienumus, izmantojot vērtības no jūsu B2C nomnieka un lietojumprogrammas. Lauki, kas nav nepieciešami (bez zvaigznītes), var tikt atstāti tukši.

    - **Lietojumprogrammas nosaukums**: jūsu B2C lietojumprogrammas nosaukums, piemēram, "Fabrikam B2C".
    - **Nomnieka nosaukums**: jūsu B2C nomnieka nosaukums (piemēram, izmantot "fabrikam", ja domēns parādās kā "fabrikam.onmicrosoft.com" B2C nomniekam). 
    - **Aizmirstas paroles politikas ID**: aizmirstas paroles lietotāja plūsmas politikas ID, piemēram, "B2C_1_PasswordReset".
    - **Pierakstīšanās pieteikšanās politikas ID**: pierakstīšanās un pieteikšanās lietotāja plūsmas politikas ID, piemēram, "B2C_1_signup_signin".
    - **Klienta GUID**: B2C lietojumprogrammas ID, piemēram, "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".
    - **Rediģēt profila politikas ID**: profila rediģēšanas lietotāja plūsmas politikas ID, piemēram, "B2C_1A_ProfileEdit".

1. Atlasiet **Labi**. Tagad jums ir jāredz jūsu B2C lietojumprogrammas nosaukums, kas parādās sarakstā.
1. Atlasiet **Saglabāt**, lai saglabātu izmaiņas.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Saistīt B2C lietojumprogrammu ar jūsu vietni un kanālu

> [!WARNING]
> Ja jūsu vietne jau ir saistīta ar B2C lietojumprogrammu, pārejot uz citu B2C programmu, tiks noņemtas pašreizējās atsauces, kas izveidotas lietotājiem, kas jau ir reģistrējušies šajā vidē. Ja tas tiks mainīts, visi akreditācijas dati, kas ir saistīti ar pašlaik piešķirto B2C lietojumprogrammu, lietotājiem nebūs pieejami. 
> 
> Atjauniniet tikai B2C lietojumprogrammu, ja kanāla B2C lietojumprogrammu iestatāt pirmo reizi vai vēlaties, lai lietotāji atkārtoti pierakstītos ar jauniem akreditācijas datiem šajā kanālā ar jauno B2C lietojumprogrammu. Esiet piesardzīgs, saistot kanālus ar B2C lietojumprogrammām, un skaidri nosauciet lietojumprogrammas. Ja kanāls nav saistīts ar B2C programmu tālāk norādītajās darbībās, lietotāji, kas piesakās šajā kanālā jūsu vietnei, tiks ievadīti B2C programmā, kas tiek parādīta kā **Noklusējums** **Nomnieka iestatījumi \> B2C iestatījumi** B2C lietojumprogrammu saraksts.

Lai saistītu B2C lietojumprogrammu ar jūsu vietni un kanālu, sekojiet šīm darbībām,

1. Dodieties uz savu vietni Commerce vietņu veidotājā.
1. Kreisās puses navigācijas rūtī atlasiet **Vietnes iestatījumi**, lai to izvērstu.
1. Zem **Vietas iestatījumiem** atlasiet **Kanāli**.
1. Galvenajā logā zem **Kanāli** atlasiet kanālu.
1. Kanāla rekvizītu rūtī labajā pusē atlasiet savas B2C lietojumprogrammas nosaukumu **Atlasiet B2C lietojumprogrammu** nolaižamā izvēlne.
1. Atlasiet **Aizvērt** un pēc tam atlasiet **Saglabāt un publicēt**.

## <a name="additional-b2c-information"></a>B2C papildinformācija

### <a name="customer-migration"></a>Klientu migrācija

Ja apsverat iespēju migrēt klientu ierakstus no iepriekšējas identitātes nodrošinātāja platformas, lūdzu, sazinieties ar Dynamics 365 Commerce grupu, lai pārskatītu jūsu klientu migrācijas vajadzības.

Lai iegūtu papildu Azure AD B2C dokumentāciju par klientu migrāciju, skatiet sadaļu [Migrēt lietotājus uz Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Pielāgotas politikas

Lai iegūtu papildu informāciju par Azure AD B2C mijiedarbību un politikas plūsmu pielāgošanu, kas pārsniedz B2C standarta politiku piedāvāto, skatiet sadaļu [Pielāgotas Azure Active Directory B2C politikas](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Sekundārais administrators

Papildu administratora kontu var pievienot jūsu B2C nomnieka **Lietotāji** sadaļā. Tas var būt tiešais konts vai vispārējais konts. Ja ir jākopīgo konts grupas resursos, var tikt izveidots arī kopīgs konts. Izmantojot Azure AD B2C uzglabāto datu sensivitāti, kopējais konts ir rūpīgi jākontrolē atbilstoši jūsu uzņēmuma drošības praksei.

## <a name="additional-resources"></a>Papildu resursi

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Jauna e-tirdzniecības nomnieka izvietošana](deploy-ecommerce-site.md)

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu](associate-site-online-store.md)

[Failu robots.txt pārvaldība](manage-robots-txt-files.md)

[Novirzīšanas URL lielapjoma augšupielāde](upload-bulk-redirects.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)

[Vairāku B2C nomnieku konfigurēšana Commerce vidē](configure-multi-B2C-tenants.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
