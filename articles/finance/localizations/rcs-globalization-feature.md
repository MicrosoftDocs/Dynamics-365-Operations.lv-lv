---
title: Regulatory Configuration Services (RCS) — globalizācijas līdzekļi
description: Šajā tēmā ir paskaidrots, kā izmantot Microsoft Regulatory Configuration Services (RCS) un globālo repozitāriju, lai izveidotu un lieto globalizācijas līdzekļus.
author: JaneA07
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: cbb1d9a53a7a09ab525532f08553898c4e40223a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822785"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Services (RCS) — globalizācijas līdzekļi

[!include [banner](../includes/banner.md)]

Varat izmantot Microsoft Regulatory Configuration Services (RCS), lai izveidotu globalizācijas līdzekli, ko var izmantot globalizācijas pakalpojumos, piemēram, e-rēķina pakalpojumā. RCS ļauj veikt tālāk minētos uzdevumus.

- Definēt līdzekļa saistītos komponentus.
- Pārvaldīt līdzekļa dzīves ciklu, izmantojot līdzekļa statusu.
- Padarīt līdzekli pieejamu definētām vidēm.
- Koplietot līdzekli ar citām organizācijām.

Tālāk minētajās procedūrās ir izskaidrots, kā lietotājs RCS var pievienot globalizācijas līdzekli un saistītos komponentus, atjaunināt līdzekļa statusu un padarīt šo līdzekli pieejamu, lai to varētu izmantot globalizācijas pakalpojumos.

Pirms procedūru pabeigšanas ir jāveic darbības, kas saistītas ar tālāk minētajiem uzdevumiem.

- Piekļūšana RCS instancei.
- Konfigurācijas nodrošinātāja izveide un aktivizēšana. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Savā programmas Finance and Operations instancē veiciet tālāk minētās darbības.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Ja jūsu uzņēmumā nav nodrošināta neviena RCS vide, atlasiet **Regulatory services — Configuration** un izpildiet norādījumus, lai tādu nodrošinātu.

> [!NOTE]
> Ja RCS vide jūsu uzņēmumam jau ir nodrošināta, izmantojiet lapas vietrādi URL, lai piekļūtu videi, atlasot pierakstīšanās opciju.

## <a name="turn-on-the-globalization-features"></a>Globalizācijas līdzekļu ieslēgšana

1. Savā RCS instancē atlasiet elementu **Līdzekļu pārvaldība**.
2. Darbvietā **Līdzekļu pārvaldība** sarakstā atlasiet **Globalizācijas līdzekļi** un pēc tam atlasiet **Iespējot tūlīt**.

    ![Globalizācijas līdzekļi līdzekļu pārvaldībā](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Globalizācijas līdzekļi

Lai izmantotu globalizācijas līdzekli, vispirms tas ir jāimportē no globālā repozitorija un jāizveido tā sava versija. Ir divi veidi, kā pievienot globalizācijas līdzekļus.

- Pievienot atvasinātu līdzekli, kas ir balstīts uz esošu līdzekli, kurš ir publicēts vai koplietots.
- Pievienot jaunu līdzekli, ko esat izveidojis pilnībā izveidojis pats.

## <a name="access-globalization-features"></a>Piekļuve globalizācijas līdzekļiem

1. Pārliecinieties, ka līdzeklis **Globalizācijas līdzekļi** ir ieslēgts līdzekļu pārvaldībā, kā aprakstīts iepriekš šajā tēmā.
2. Atveriet jauno darbvietu **Globalizācijas līdzekļi** un pēc tam sadaļā **Līdzekļi** atlasiet elementu **e-rēķinu izrakstīšana**.

    ![Globālo līdzekļu darbvieta](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    Tiek atvērta lapa **Elektroniskās rēķinu izrakstīšanas līdzekļi**.

    ![E-rēķinu izrakstīšanas līdzekļu lapa](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Atvasināta globalizācijas līdzekļa pievienošana

Varat pievienot jaunu globalizācijas līdzekli, atvasinot to no esoša līdzekļa, kas ir publicēts vai koplietots.

1. Atlasiet **Importēt**, lai atvērtu lapu **Importēšanas līdzeklis no globālā repozitorija**.

    ![Līdzekļa importēšana no globālā repozitorija lapas](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. Atlasiet **Sinhronizēt**, lai iegūtu jaunākos līdzekļus.

    Sinhronizētajā sarakstā ir iekļauti līdzekļi, kas ir pieejami tāpēc, ka tos ir publicējusi korporācija Microsoft, vai arī tie tikuši koplietoti ar citu konfigurācijas nodrošinātāju.

    ![Līdzekļu sinhronizētais saraksts](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. Sarakstā atlasiet importējamos līdzekļus un pēc tam atlasiet **Importēt**. Jūs saņemsit ziņojumu, kad atlasītie līdzekļi ir sekmīgi importēti.

    ![Ziņojums par sekmīgu importēšanu](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. Atlasiet **Pievienot** un pēc tam nolaižamajā dialoglodziņā atlasiet opciju **Pamatojoties uz esošu versiju**.
5. Ievadiet līdzekļa nosaukumu un aprakstu.
6. Pieejamo līdzekļu sarakstā atlasiet līdzekļa pamatversiju un pēc tam atlasiet **Izveidot līdzekli**.

    ![Atvasināta līdzekļa pievienošana](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    Pievienotais līdzeklis ir izveidots, un tam ir statuss **Melnraksts**.

    ![Atvasinātais līdzeklis, kam ir melnraksta statuss](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Pārskatiet līdzekļa komponentus, lai noteiktu, vai ir nepieciešami atjauninājumi.

    - Pārskatiet konfigurācijas, ja ir jāpielāgo elektronisko pārskatu (ER) formāti un to saistījums ar formāta kartējumiem līdzekļa versijai.
    - Pārskatiet iestatījumus gadījumā, ja līdzekļa versijai ir jāpielāgo cilne **Darbības**, cilne **Piemērojamības kārtulas** vai cilne **Mainīgie**.

8. Cilnē **Versijas** atlasiet datumu **Spēkā no** un ievadiet aprakstu, ja lauks **Apraksts** ir tukšs.
9. Atlasiet **Mainīt statusu**, lai pabeigtu līdzekli. Pabeigtos līdzekļus var padarīt pieejamus noteiktai videi, lai tos varētu izmantot globalizācijas pakalpojumos, vai arī tos var publicēt globālajā repozitorijā.

> [!NOTE]
> Līdzekļi, kuriem ir vērtība **Līdzekļa versijas statuss** sadaļā **Publicēts**, var tikt koplietoti ar ārējām organizācijām.

## <a name="add-a-new-globalization-feature"></a>Jauna globalizācijas līdzekļa pievienošana

Varat pievienot jaunu globalizācijas līdzekli, izveidojot to pilnībā pats.

1. Lapā **Importēt no globālā repozitorija** atlasiet **Pievienot** un pēc tam nolaižamajā dialoglodziņā atlasiet opciju **Jauns līdzeklis**.
2. Ievadiet līdzekļa nosaukumu un aprakstu.
3. Atlasiet **Izveidot līdzekli**.

    ![Jauna līdzekļa pievienošana](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. Cilnē **Versijas** atlasiet datumu **Spēkā no** un pēc tam atlasiet **Mainīt statusu**, lai pabeigtu līdzekli. Pabeigtos līdzekļus var padarīt pieejamus noteiktai videi, lai tos varētu izmantot globalizācijas pakalpojumos, vai arī tos var publicēt globālajā repozitorijā.

> [!NOTE]
> Līdzekļi, kuriem ir vērtība **Līdzekļa versijas statuss** sadaļā **Publicēts**, var tikt koplietoti ar ārējām organizācijām.

## <a name="feature-component-overview"></a>Līdzekļu komponentu pārskats

Globalizācijas līdzekļiem ir vairāki komponenti.

- **Versija** — šis komponents atbalsta līdzekļu dzīves cikla pārvaldību un ļauj lietotājiem pārvaldīt statusu dažādām līdzekļa versijām.
- **Konfigurācijas** — šis komponents ļauj lietotājiem pārvaldīt, skatīt un rediģēt saistītos ER formātus un formatēt kartējumus.
- **Iestatījumi** — šis komponents ļauj globalizācijas pakalpojumu lietotājiem, piemēram, e-rēķinu pakalpojumam, pārvaldīt saistītā līdzekļa versijas iestatīšanu. Tādēļ tas atbalsta elastīgu komunikācijas uzbūvi un atbildes noteikumus.
- **Vide** — šis komponents ļauj globalizācijas pakalpojumu lietotājiem, piemēram, e-rēķinu izsniegšanas pakalpojumam, pārvaldīt vidi, kurā tiek izmantots līdzekļu versijas iestatījums, un piešķirt autorizāciju lietotājiem, kuriem tai būs piekļuve.
- **Organizācijas** — šis komponents ļauj lietotājiem koplietot šo līdzekli ar ārējām organizācijām.

## <a name="configuring-feature-components"></a>Līdzekļu komponentu konfigurēšana

### <a name="version-and-status"></a>Versija un statuss

Versija tiek izmantota, lai pārvaldītu globalizācijas līdzekļa dzīves ciklu.

Statusu var mainīt cilnes **Versija** laukā **Statuss**. Ir pieejami tālāk minētie statusi.

- **Melnraksts** — līdzekli var rediģēt tikai tad, ja tas ir šajā statusā.
- **Pabeigts** — līdzeklis un visi saistītie komponenti ir finalizēti (pabeigti), un tos nevar rediģēt.
- **Publicēts** — līdzeklis un visi saistītie komponenti ir publicēti globālajā repozitorijā.
- **Koplietots** — līdzeklis un visi saistītie komponenti ir koplietoti ar ārējām organizācijām.
- **Iespējots** — līdzeklis un visi saistītie komponenti ir iespējoti izmantošanai globalizācijas pakalpojumā, piemēram, e-rēķinu izrakstīšanas pakalpojumā.

> [!NOTE]
> Līdzekļi ir secīgi jāpārvieto, izmantojot dažus no šiem statusiem. Tāpēc ne katrs statuss var būt pieejams visos dzīves cikla posmos.

### <a name="configurations"></a>Konfigurācijas

Konfigurēšanai ir pieejamas tālāk minētās darbības.

- **Skatīt** — skatīt pakārtoto līdzekļu konfigurācijas, kurām nav nepieciešams atjauninājums.
- **Rediģēt** — izveidojiet atlasītās konfigurācijas melnraksta versiju, lai varētu rediģēt formātu vai formatēt kartējumu formāta noformētājā.
- **Dzēst** — dzēst atlasīto konfigurāciju no līdzekļa.
- **Pārskatīt** — pārskatīt līdzekli. Papildinformāciju skatiet šīs tēmas nākamajā sadaļā [Atvasināto globalizācijas līdzekļu pārskatīšana](#rebase).

### <a name="setups"></a>Iestatījumi

Līdzekļa iestatīšanai ir pieejamas tālāk minētās darbības.

- **Pievienot** — izveidot jaunu līdzekļa iestatījumu. Šo līdzekļa iestatījumu var atvasināt no esoša līdzekļu iestatījuma vai izveidot to no nulles.
- **Dzēst** — dzēst atlasīto līdzekļa iestatījumu.
- **Skatīt** — skatīt pakārtoto līdzekļa iestatījumu, kam nav nepieciešamas izmaiņas.
- **Rediģēt** — izveidot, dzēst vai modificēt līdzekļa iestatījuma trīs galveno komponentu atribūtus.

    - Darbības un to parametri
    - Piemērojamības kārtulas
    - Mainīgie

![Līdzekļa versijas iestatīšanas lapa](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Vides

Vidēm ir pieejamas tālāk minētās darbības.

- **Iespējot** — atlasītajai līdzekļa versijai atlasiet publicēto vidi un atlasiet datumu **Spēkā no**, kad tam jābūt pieejamam. Papildinformāciju skatiet šīs tēmas nākamajā sadaļā [Vižu konfigurēšana iespējošanai](#configureenvironment).
- **Atcelt** — noņemt vidi līdzekļa iestatījumam.

### <a name="organizations"></a>Organizācijas

Izpildiet tālāk minētās darbības, lai koplietotu globalizācijas līdzekli ar ārēju organizāciju.

1. Lapā **e-rēķina līdzekļi** atlasiet līdzekli un līdzekļa versiju, kuru koplietot.
2. Cilnē **Organizācijas** atlasiet **Koplietot ar** un pēc tam nolaižamajā dialoglodziņā ievadiet organizācijas domēna nosaukumu.
3. Atlasiet **Koplietot**.

    ![Līdzekļa koplietošana ar organizāciju](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

Līdzeklis tiek koplietots ar atlasīto organizāciju un ir pieejams šai organizācijai globālajā repozitorijā. No turienes līdzekli var importēt RCS organizācijas instancē vai Dynamics 365 Finance tā, lai to varētu izmantot.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Atvasināto globalizācijas līdzekļu pārskatīšana

Atvasināto globalizācijas līdzekli varat pārskatīt uz jaunu vai atjauninātu bāzes līdzekļu versiju. Šādā veidā izmaiņas, kas notikušas bāzes versijā, var tikt automātiski atjauninātas. Atjaunināto bāzes līdzekļa versiju izveido sākotnējais konfigurācijas nodrošinātājs, un tā tiek publicēta vai koplietota.

![Atjauninātā bāzes līdzekļa versija](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Piemēram, ja vēlaties pārskatīt jūsu izveidotā līdzekļa atvasināto versiju, vispirms iegūstiet līdzekļa jaunāko versiju, importējot to no globālā repozitorija.

1. Lapā **e-rēķina līdzekļi** atlasiet **Importēt**.
2. Atlasiet **Sinhronizēt**, lai iegūtu jaunākos līdzekļus.
3. Līdzekļu sarakstā atlasiet importējamos līdzekļus un pēc tam atlasiet **Importēt**.

    ![Līdzekļa jaunākās versijas importēšana](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. Līdzekļu sarakstā atlasiet līdzekli, kas jāpārskata.
5. Cilnē **Versija** atlasiet **Jauns**, lai izveidotu melnraksta versiju.

    ![Izveidota jauna melnraksta versija](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. Atlasiet **Pārskatīt**.
7. Dialoglodziņā **Pārskatīt** atlasiet jaunāko līdzekļa versiju, uz kuru to pārveidot.

    ![Dialoglodziņš Pārskatīt](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. Atlasiet **Labi**.
9. Pārskatiet līdzekļa komponentus un veiciet nepieciešamās izmaiņas.
10. Atlasiet **Mainīt statusu**, lai pabeigtu pārskatīto līdzekli. Kad pārskatīšana ir pabeigta, varat veikt papildu darbības. Piemēram, varat publicēt līdzekli un padarīt to pieejamu izmantošanai globalizācijas pakalpojumos.

    ![Līdzekļa statuss atjaunināts uz Pabeigts](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Vižu konfigurēšana globalizācijas līdzekļiem

Globalizācijas pakalpojumu lietotāji var pārvaldīt vidi, lai iestatītu globalizācijas līdzekli un piešķirtu autorizāciju citiem lietotājiem, kuriem tam būs piekļuve.

1. Darbvietā **Globalizācijas līdzekļi** zem **Vides** atlasiet elementu **e-rēķinu izrakstīšana**.

    ![Globalizācijas līdzekļu darbvieta](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. Atlasiet **Key Vault parametrus** un pēc tam atlasiet **Jauns**, lai izveidotu Azure Key Vault noslēpumu.
3. Ievadiet Key Vault aprakstu un pēc tam laukā **Key Vault URI** ievadiet vietrādi URL, kas identificē Key Vault resursu Azure.
4. Kopsavilkuma cilnē **Sertifikāti** atlasiet **Pievienot**, lai pievienotu sertifikātu, un ievadiet katra sertifikāta nosaukumu un aprakstu.

    ![Sertifikāts pievienots](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Atlasiet **Jauns**, lai izveidotu jaunu vidi.
6. Ievadiet krātuvei nepieciešamo nosaukumu, aprakstu un koplietojamo piekļuves paraksta marķieri.
7. Kopsavilkuma cilnā **Lietotāji** atlasiet **Jauns**, lai pievienotu lietotāju, kuram būs atļauja piekļūt šai videi.
8. Ievadiet lietotāja ID un e-pasta adresi.
9. Atkārtojiet 7. un 8. darbību, lai pievienotu vairāk lietotāju.
10. Atlasiet **Publicēt**, lai publicētu vidi.

    ![Publicētā vide](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]