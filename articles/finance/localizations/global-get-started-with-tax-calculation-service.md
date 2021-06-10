---
title: Darba sākšana ar nodokļu aprēķinu
description: Šajā tēmā paskaidrots, kā iestatīt Nodokļu aprēķinu.
author: wangchen
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3f8aa791cee1926afe6be347331d47902a3b7304
ms.sourcegitcommit: f4dc09601bceb5cdc88ee184ce7c8f369e3e6e86
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/19/2021
ms.locfileid: "6060567"
---
# <a name="get-started-with-the-tax-calculation-preview"></a>Sākt darbu ar Nodokļu aprēķinu (Priekšskatījums)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šajā tēmā ir sniegta informācija par to, kā sākt darbu ar Nodokļu aprēķinu. Vispirms tas palīdz veikt konfigurācijas darbības programmās Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) un Dynamics 365 Finance, un Dynamics 365 Supply Chain Management. Pēc tam tā pārskata kopējo procesu, kas saistīts ar Nodokļu aprēķina iespēju izmantošanu Finance un Supply Chain Management transakcijās.

Iestatījums sastāv no četrām galvenām darbībam:

1. Sistēmā LCS instalējiet Nodokļu aprēķinu.
2. Sistēmā RCS iestatiet Nodokļu aprēķina līdzekli. Šis iestatījums nav specifisks juridiskajai personai. To var koplietot visas Finance un Supply Chain Management juridiskās personas.
3. Finance un Supply Chain Management iestatiet Nodokļu aprēķina parametrus pēc juridiskās personas.
4. Finance un Supply Chain Management izveidojiet tādus darījumus kā pārdošanas pasūtījumi un izmantojiet Nodokļu aprēķinu, lai noteiktu un aprēķinātu nodokļus.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms varat pabeigt šajā tēmā norādītās procedūras, ir jāievieš šādi priekšnosacījumi:

- Jums ir piekļuve LCS kontam un esat izvietojis LCS projektu ar 2. pakāpes (vai augstākas) vidi, kurā darbojas Dynamics 365 versija 10.0.18 ar [KB4616360](https://fix.lcs.dynamics.com/Issue/Details?kb=4616360&bugId=568738&dbType=3&qc=1f1c04ff39adad74ef871f539e8d73e14c1893ef7cc4b6e3f7d5c5864ec2781a) vai jaunāka.
- Jums ir piekļuve savam RCS kontam.
- Esat sazinājies ar uzņēmumu Microsoft, lai iespējotu testējumu jūsu izvietotā Finance vai Supply Chain Management vidē.

## <a name="set-up-tax-calculation-in-lcs"></a>Iestatīt Nodokļu aprēķinu sistēmā LCS

1. Pierakstīšanās programmā [LCS](https://lcs.dynamics.com)
2. Pabeidziet Microsoft Power Platform integrācijas iestatīšanu. Papildinformāciju skatiet sadaļā [Pievienojumprogrammas pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Atlasiet vienu no izvietotām vidēm, kas nav ražošanas vides, un pēc tam atlasiet **Instalēt jaunu pievienojumprogrammu**.
4. Atlasīt **Nodokļu aprēķins (priekšskatījums)**.
5. Izlasiet un piekrītiet noteikumiem un nosacījumiem un pēc tam atlasiet **Instalēt**.

## <a name="set-up-tax-calculation-in-rcs"></a>Iestatīt Nodokļu aprēķinu sistēmā RCS

Šīs sadaļas darbības nav saistītas ar noteiktu juridisko personu. Jums ir jāveic šī procedūra tikai vienu reizi, un jūs variet pabeigt to jebkurā juridiskajā persona programmā RCS.

1. Pierakstieties [RCS](https://marketing.configure.global.dynamics.com/).
2. Programmā Finance, darbvietā **Elektronisko pārskatu veidošana** pievienojiet jaunu konfigurācijas nodrošinātāju. Kā nodrošinātāja nosaukumu izmantojiet uzņēmuma nosaukumu. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Atlasiet tikko izveidoto konfigurācijas nodrošinātāju un pēc tam atlasiet **Iestatīt aktīvu**.
4. Atlasiet **Microsoft** konfigurācijas nodrošinātāju, un tad atlasiet **Repozitoriji**.
5. Laukā **Tips** atlasiet **Globāls**.
6. Atlasiet **Atvērt**.
7. Dodieties uz **Nodokļu datu modelis**, izvērsiet failu koku un pēc tam atlasiet **Nodokļu konfigurācija**.
8. Atlasiet jaunāko versiju un pēc tam atlasiet **Importēt**.
9. Atgriezieties darbvietā **Globalizācijas līdzekļi (priekšskatījums)**, atlasiet **Līdzekļi**, atlasiet elementu **Nodokļu aprēķins** un pēc tam atlasiet **Pievienot**.
10. Atlasiet vienu no šiem līdzekļu tipiem:

    - **Jauns līdzeklis** – izveidojiet līdzekļa iestatījumu, kam ir tukšs saturs.
    - **Balstīts uz esošo līdzekli** – izveidojiet līdzekli no esoša līdzekļa un kopējiet saturu no esoša līdzekļa iestatījuma.

11. Ievadiet jaunā līdzekļa nosaukumu un aprakstu un pēc tam atlasiet **Izveidot līdzekli**.

    Pēc līdzekļa izveides automātiski tiek izveidota tā melnraksta versija.

12. Atlasiet līdzekļa melnraksta versiju un pēc tam atlasiet **Rediģēt**. Ir aizpildīta lapa **Nodokļu aprēķina iestatījums**.
13. Atlasiet **Konfigurācijas versija**. 8. darbībā jums vajadzētu redzēt importēto konfigurācijas versiju.

    Microsoft nodrošina nodokļu aprēķina pievienojumprogrammas noklusējuma nodokļu konfigurāciju. Šī konfigurācija sedz lielāko daļu nodokļu aprēķina darbību prasību. Tas tiks atjaunināts, balstoties uz tirgus atsauksmēm. Ja konfigurācija jāpaplašina, lai tā atbilstu noteiktām prasībām, skatiet sadaļu [Kā veidot nodokļu pakalpojumu paplašinājumu](./tax-service-add-data-fields-tax-integration-by-extension.md), lai saņemtu informāciju par to, kā ģenerēt un atlasīt savu nodokļu konfigurāciju.

    Pēc **Konfigurācijas versija** izvēles, tiek parādītas vairākas papildu cilnes:

    - **Nodokļu kodi** – šī cilne ir obligāta. To izmanto nodokļu kodu pamatdatu uzturēšanai. Visi šajā cilnē izveidotie nodokļu kodi automātiski tiek sinhronizēti ar Finance, ja iespējojat pašreizējo juridiskās personas nodokļu līdzekļa iestatījumu versiju.
    - **Nodokļu kodu iespējas** – šī cilne ir obligāta. Tas tiek izmantots, lai definētu matricu, kas nosaka nodokļa kodu, nodokļa grupu un krājuma nodokļa grupu. Noteikto nodokļa kodu izmanto nodokļa summas aprēķināšanai. Lauku **Nodokļa kods**, **Nodokļa grupa** un **Krājuma nodokļa grupa** vērtības tiek atgrieztas programmā Finance.
    - **Klienta nodokļa reģistrācijas numura piemērojamība** – šī cilne nav obligāta. Ja vienam debitoram ir vairāki nodokļa reģistrācijas numuri, Nodokļu aprēķins var automātiski noteikt pareizo nodokļa reģistrācijas numuru. Šīs cilnes matricā definējiet nosacījumus, kurus izmanto, lai veiktu noteikšanu. Pretējā gadījumā Finance un Supply Chain Management turpinās izmantot ar nodokli apliekamo dokumentu noklusējuma nodokļa reģistrācijas numuru pārdošanas darbībām.
    - **Kreditora nodokļa reģistrācijas numura piemērojamība** – šī cilne nav obligāta. Ja vienam kreditoram ir vairāki nodokļa reģistrācijas numuri, Nodokļu aprēķins var automātiski noteikt pareizo nodokļa reģistrācijas numuru. Šīs cilnes matricā definējiet nosacījumus, kurus izmanto, lai veiktu noteikšanu. Pretējā gadījumā Finance un Supply Chain Management turpinās izmantot ar nodokli apliekamo dokumentu noklusējuma nodokļa reģistrācijas numuru pirkšanas darbībām.
    - **Saraksta koda piemērojamība** — šī cilne nav obligāta. Tas var palīdzēt automātiski noteikt lauka **Saraksta kods** vērtību, izmantojot elastīgākus un konfigurējamus noteikumus. Šīs cilnes matricā var definēt nosacījumus, kurus izmanto, lai veiktu noteikšanu. Pretējā gadījumā Finance un Supply Chain Management turpinās izmantot ar nodokli apliekamo dokumentu noklusējuma kodu.

14. Cilnē **Nodokļu kodi** atlasiet **Pievienot** un ievadiet nodokļa kodu un aprakstu.
15. Atlasiet **Nodokļa komponents**. Nodokļa komponents ir metožu grupa, kas definēta atlasītās nodokļu konfigurācijas iepriekšējā versijā. Pieejami tālāk norādītie nodokļu komponenti.

    - Pēc neto summas
    - Pēc bruto summas
    - Pēc daudzuma
    - Pēc rezerves
    - Nodoklis no nodokļa

16. Atlasiet **Saglabāt**. Vairāk lauku kļūst pieejami, balstoties uz atlasīto nodokļu sastāvdaļu.
17. Lai identificētu nodokļa koda būtību, lietojiet šādas opcijas:

    - Ir atbrīvots
    - Ir Importa nodoklis
    - Ir Apgrieztā maksa
    - Neiekļaut pamatsummas aprēķinā

    Importa nodokļu scenārijam iestatiet vienu nodokļa kodu, kam ir pozitīva nodokļu likme, un atzīmējiet to kā **Ir Importa nodoklis**.

    Apgrieztās maksas scenārijam iestatiet divus nodokļu kodus, no kuriem vienam ir pozitīva nodokļu likme, bet otram ir negatīva nodokļu likme, bet tāda pati likmes vērtība. Atzīmējiet negatīvo nodokļa kodu kā **Ir Apgrieztā maksa**. Papildinformāciju par atgrieztās maksas risinājumu programmā Finance skatiet [Apgrieztās maksas mehānisms PVN/GST shēmai](emea-reverse-charge.md).
    
    Dažiem nodokļu tipiem, kas dažās valstīs ir jāizslēdz no nodokļu pamatsummas aprēķina, piemēram, muitas nodoklim dažās valstīs, atlasiet izvēles rūtiņu **Neiekļaut pamatsummas aprēķinā**.

    Uzturējiet nodokļu likmes un nodokļu summas ierobežojumus šim nodokļu kodam.

18. Atkārtojiet 14.-17. darbību, lai pievienotu visus citus nepieciešamos nodokļu kodus.
19. Cilnē **Nodokļu kodu piemērojamība** atlasiet kolonnas, kas ir nepieciešamas pareizā nodokļa koda noteikšanai, un pēc tam atlasiet **Pievienot**.
20. Ievadiet vai atlasiet vērtības katrai kolonnai. Lauki **Nodokļa kods**, **Nodokļa grupa** un **Krājuma nodokļa grupa** būs šīs matricas izvade.
21. Atkārtojiet no 19. līdz 20. darbības, lai iestatītu debitora nodokļu reģistrācijas numuru, kreditora nodokļa reģistrācijas numuru un sarakstu kodu piemērojamību.
22. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.
23. Atlasiet **Mainīt statusu** \> **Pabeigts**. Kad statuss ir mainīts uz **Pabeigts**, versiju vairs nevar rediģēt.
24. Atlasiet **Mainīt statusu** \> **Publicēt**. Šī nodokļu līdzekļa iestatīšanas versija tiks novirzīta uz globālo repozitoriju un būs redzama katrai Finance juridiskajai personai.

## <a name="dynamics-365-setup"></a>Dynamics 365 iestatīšana

Kad būsiet pabeidzis iestatījumu RCS, kā aprakstīts iepriekšējā sadaļā, jums būs nodokļu līdzekļa publicētā versija. Veiciet šīs darbības, lai Finance sistēmā iestatītu Nodokļu aprēķinu.

Iestatījumus šajā sadaļā veic juridiska persona. Jums tas jākonfigurē katrai juridiskajai personai, kurai programmā Finance vēlaties iespējot Nodokļu aprēķinu.

1. Programmā Finance dodieties uz **Nodoklis** \> **Uzstādīšana** \> **Nodokļu konfigurācija** \> **Nodokļu aprēķina iestatījumi (Priekšskatījums)**.
2. Cilnē **Vispārīgi** iestatiet šādus laukus:

    - **Iespējot Nodokļu aprēķinu** — atzīmējiet šo izvēles rūtiņu, lai iespējotu Nodokļu aprēķinu juridiskajai personai. Ja tas nav iespējots pašreizējai juridiskajai personai, juridiskā persona turpinās izmantot esošo nodokļu programmu, lai noteiktu un aprēķinātu nodokli.
    - **Līdzekļa iestatījumi** — atlasiet publicētu nodokļu līdzekļu iestatījumus un juridiskās personas versiju. Papildinformāciju par publicēta nodokļu līdzekļa iestatīšanu un pabeigšanu skatiet šīs tēmas iepriekšējā sadaļā.
    - **Biznesa process** – atlasiet iespējošanai biznesa procesus.
    - **Iespējot nodokļu koda korekciju** — iestatiet šo opciju uz **Jā**, lai iespējotu nodokļu koda korekcijas nodokļu lapā.

3. Cilnē **Aprēķins** definējiet juridiskās personas paredzamo noapaļošanas kārtulu.
4. Cilnē **Kļūdu apstrāde** definējiet juridiskās personas paredzamo kļūdu apstrādes metodi. Katram rezultātu kodam ir pieejamas trīs opcijas:

    - Nr.
    - Brīdinājums
    - Kļūda

5. Saglabājiet iestatījumu.
6. Atkārtojiet 1.-5. darbību katrai papildu juridiskai personai.

## <a name="transaction-processing"></a>Darbību apstrāde

Kad esat pabeidzis visas iestatīšanas procedūras, varat izmantot Nodokļu aprēķinu, lai noteiktu un aprēķinātu nodokli programmā Finance. Darījumu apstrādes darbības paliek tās pašas. Finance versijā 10.0.18 tiek atbalstītas šādi darījumi:

- Pārdošanas process

    - Pārdošanas piedāvājums
    - Pārdošanas pasūtījums
    - Apstiprināšana
    - Izdošanas saraksts
    - Pavadzīme
    - Pārdošanas rēķins
    - Kredīta piezīme
    - Atgriešanas pasūtījums
    - Galvenā maksa
    - Rindas maksa

- Pirkšanas process

    - Pirkuma pasūtījums
    - Apstiprināšana
    - Saņemšanas saraksts
    - Produktu ieejas plūsma
    - Pirkšanas rēķins
    - Galvenā maksa
    - Rindas maksa
    - Kredīta piezīme
    - Atgriešanas pasūtījums
    - Pirkšanas pieprasījums
    - Pirkšanas pieprasījuma rindas maksa
    - Piedāvājuma pieprasījums
    - Piedāvājuma pieprasījuma virsraksta maksa
    - Piedāvājuma pieprasījuma rindas maksa

- Krājumu process

    - Pārvietošanas pasūtījums – nosūtīšana
    - Pārsūtīšanas pasūtījums - saņemšana
