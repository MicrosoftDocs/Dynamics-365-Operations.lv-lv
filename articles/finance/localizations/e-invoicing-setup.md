---
title: Elektronisko rēķinu izrakstīšanas pievienojuma iestatīšana
description: Šajā tēmā ir paskaidrots, kā iestatīt elektronisko rēķinu izrakstīšanas pievienojumu programmās Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 5821a512b2beaf7ba2b8015355f04562f7b3b38a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209950"
---
# <a name="set-up-the-electronic-invoicing-add-on"></a>Elektronisko rēķinu izrakstīšanas pievienojuma iestatīšana

[!include [banner](../includes/banner.md)]


Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa iestatīšana ir process, kurā ir nepieciešama konfigurācija, izmantojot regulatīvo konfigurācijas pakalpojumu (Regulatory Configuration Services - RCS) vidi un publicējot šo konfigurāciju elektronisko rēķinu izrakstīšanas pievienojuma serverim. Iestatīšana ļauj izveidot konfigurējamus noteikumus, kas iespējo elektronisko rēķinu izrakstīšanas pievienojumu, lai internetā izmantotu drošu protokolu, lai sazinātos un veiktu datu apmaiņu ar trešās puses elementu, izmantojot tīmkļa pakalpojumus.

Konfigurējamība ir atkarīga no elektroniskās ziņošanas (Electronic reporting — ER) formāta konfigurācijas, jo tā ir veids, kā izveidot saturu, kas tiek nosūtīts un saņemts, izmantojot digitālos failus. Tā arī paļaujas uz saziņas darbību saskaņu, lai nosūtītu pieprasījumus un saņemtu atbildes no trešās puses tīmekļa pakalpojumiem, neprasot ievadīt kodu.

## <a name="overview"></a>Pārskats

"Elektronisko rēķinu izrakstīšanas pievienojuma līdzeklis" ir vispārējs nosaukums resursam, kas ir konfigurēts un publicēts, lai varētu patērēt elektronisko rēķinu izrakstīšanas pievienojuma serveri. Līdzekļa iestatījums apvieno, cita starpā, elektroniskās ziņošanas ER konfigurāciju formātus, lai izveidotu konfigurējamas eksporta un importa failus, un darbību un darbību plūsmu izmantošanu, lai iespējotu konfigurējamu noteikumu izveidi, lai nosūtītu pieprasījumus, importētu atbildes un parsētu atbildes saturu.

Sekojošajā attēlā ir parādīts, elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa galvēnos komponentus.

![Pārskats par elektronisko rēķinu izrakstīšanas pievienojuma līdzekli](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

Rēķinu formātu un darbības plūsmu izmaiņu dēļ līdzekļa iestatījums var atšķirties atkarībā no valsts vai reģiona, vai atbilstoši biznesa prasībām.

## <a name="set-up-the-electronic-invoicing-add-on-feature"></a>Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa iestatīšana

Iestatīšanas process ir jāpabeidz jūsu RCS vidē. Veiciet šīs darbības, lai izveidotu jaunu elektronisko rēķinu izrakstīšanas pievienojuma līdzekli.

1. Pierakstieties savā RCS vidē.
2. Darbvietā **Globalizācijas līdzekļi** sadaļā **Līdzekli** atlasiet elementu **Elektronisko rēķinu izrakstīšanas pievienojums**.
3. Lapā **Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļi** atlasiet **Importēt**, lai importētu ER datu modeļa konfigurāciju no globālās krātuves.
4. Atlasiet **Pievienot**, lai izveidotu elektronisku rēķinu izrakstīšanas pievienojuma līdzekli. Varat vai nu izveidot līdzekli no fragmenta, vai arī iegūt to no pastāvoša elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa.

    ![Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa pievienošana](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> Kad izveidojat jaunu elektronisko rēķinu izrakstīšanas pievienojuma līdzekli, tam ir versijas numurs, un tā noklusētais statuss ir iestatīts kā **Melnraksts**.

### <a name="configurations"></a>Konfigurācijas

Konfigurācijās ir ER formāta konfigurācijas, kas nepieciešamas transformācijām un lai izveidotu failus, kas tiks apmainīti sakaru laikā ar trešās puses tīmekļa pakalpojumiem. Elektroniskās rēķinu pievienošanas līdzeklim var būt tik daudz ER failu formāta konfigurāciju, cik nepieciešams, pamatojoties uz integrēšanas tehnisko specifikāciju, ko sniedz tīmekļa pakalpojumu sniedzējs.

Veiciet šīs darbības, lai pievienotu ER formātu elektronisko rēķinu izrakstīšanas pievienojuma līdzeklim.

1. Lapā **Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļi** cilnē **Konfigurācijas** atlasiet **Pievienot** ER faila formāta konfigurācijas elektronisko rēķinu izrakstīšanas pievienojuma līdzeklim.

    ![Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa konfigurācijas](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Kad izveidojat elektronisko rēķinu izrakstīšanas pievienojuma līdzekli no nulles, ir manuāli jāpievieno visas ER faila formāta konfigurācijas. Kad izveidojat elektronisko rēķinu izrakstīšanas pievienojuma līdzekli no esoša līdzekļa, ER faila formāta konfigurācijas tiek veidotas automātiski, jo tās tiek pārmantotas no oriģinālā elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa.

2. Atlasiet **Rediģēt**, lai atvērtu lapu **Formāta veidotājs**, kur varat rediģēt ER faila formāta konfigurāciju.

    ![Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa konfigurāciju rediģēšana](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Rediģējot formātu, konfigurācijas versijas statuss tiek iestatīts uz **Melnraksts**.

3. Lai mainītu failu formāta konfigurāciju, izmantojiet lapu **Formāta veidotājs**. Papildinformāciju skatiet tēmā [Elektronisko dokumentu konfigurāciju izveide](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Formāta veidotāja lapa](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>Līdzekļa iestatījumi

Līdzekļa iestatījumi iekļauj sakaru un drošības nosacījumus ar trešās puses tīmekļa pakalpojumu. Elektronisko rēķinu izrakstīšanas pievienojuma līdzeklim var būt tik daudz līdzekļu, cik nepieciešams, balstoties uz biznesa noteikumu, kuru vēlaties sasniegt.

Veiciet šīs darbības, lai pievienotu līdzekļa iestatījumus elektronisko rēķinu izrakstīšanas pievienojuma līdzeklim.

1. Lapā **Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļi** cilnē **Iestatījumi** atlasiet **Pievienot** līdzekļa iestatījumus elektronisko rēķinu izrakstīšanas pievienojuma līdzeklim.

    ![Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa iestatījumu pievienošana](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > Kad izveidojat elektronisko rēķinu izrakstīšanas pievienojuma līdzekli no nulles, ir manuāli jāpievieno visus nepieciešamos līdzekļa iestatījumus. Kad izveidojat elektronisko rēķinu izrakstīšanas pievienojuma līdzekli no esoša līdzekļa, visi līdzekļa iestatījumi tiek veidoti automātiski, jo tie tiek pārmantoti no oriģinālā elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa.

2. Atlasiet **Rediģēt**, lai rediģētu līdzekļa versijas iestatījumu.

    ![Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa iestatījumu rediģēšana](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. Izmantojiet lapu **Līdzekļa versijas iestatīšana**, lai konfigurētu darbības, piemērojamības noteikumi un mainīgos.

    ![Darbības, piemērojamības noteikumi un mainīgie](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>Darbības

Darbības ir iepriekšdefinētais darbību saraksts, kas tiek izpildītas secīgā secībā. Šis saraksts attēlo darbību sadalījumu, kas nepieciešams, lai pilnībā izpildītu elektronisko rēķinu izrakstīšanas pievienojuma līdzekli. Vienā elektronisko rēķinu izrakstīšanas pievienojuma līdzeklī darbības var iekļaut saziņu abos virzienos: adresāta pieprasījumu nosūtīšanu un atbildes saņemšanu, un tā satura parsēšanu.

Katra darbība ietver iepriekš definēto parametru sarakstu, kas nepieciešams darbībai, lai sasniegtu tās mērķi. Pēc izvēles var tikt sniegti papildu parametri.

#### <a name="actions-fasttab"></a>Kopsavilkuma cilne Darbības

Lapā **Līdzekļu versiju iestatīšana** cilnē **Darbības**, kas atrodas kopsavilkuma cilnē **Darbības**, izpildiet vienu vai abus šos soļus, lai pārvaldītu darbības:

- Atlasiet **Jauns** vai **Dzēst**, lai pievienotu jaunas darbības vai dzēstu esošās darbības.
- Atlasiet **Uz augšu** vai **Uz leju**, lai pārvietotu atlasītās darbības režģī uz augšu vai uz leju, un tādējādi mainiet secību, kādā tie tiek izpildīti. Darbības tiek izpildītas tādā secībā, kādā tās parādās režģī, no sākuma līdz beigām.

![Darbību pārvaldība](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Darbības** kopsavilkuma cilnē.

| Lauks        | Apraksts |
|--------------|-------------|
| Darbība       | Ir astoņas iepriekš definētas darbības.<ul><li><strong>Parakstīt dokumentu</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>Transformēt dokumentu</strong></li><li><strong>Apstrādāt atbildi</strong></li><li><strong>Izsaukt REST tīmekļa pakalpojumu</strong></li><li><strong>Izsaukt Meksikas PAC pakalpojumu</strong></li><li><strong>Izsauciet Brazīlijas SEFAZ pakalpojumu</strong></li><li><strong>Izsauciet Itālijas SDI pakalpojumu</strong></li></ul> |
| Darbības nosaukums  | Darbības nosaukums un tās izpildes pasūtījums. |
| Apraksts  | Darbības apraksts. |
| Iespējot atkārtotu mēģinājumu | Atzīmētā izvēles rūtiņa norāda, ka darbību var atkārtoti izmēģināt, ja iepriekšējais mēģinājums ir neveiksmīgs. |
| Atkārtoti mēģināt veikt darbību | Atkārtotā mēģinājuma gadījumā darbība, no kuras tiek sākts atkārtots mēģinājums. Pēc tam atkārtota darbība beidzas ar pašreizējo darbību (ieskaitot mēģinājumu). Darbībām, kurās tie ir, parametri **Minimālā atkāpšanās** un **Maksimālā atkāpšanās** nosaka minimālo un maksimālo atkārtoto mēģinājumu skaitu. |

#### <a name="parameters-fasttab"></a>Kopsavilkuma cilne Parametri

Kopsavilkuma cilne **Parametri** uzskaita parametrus darbībai, kas atlasīta kopsavilkuma cilnē **Darbības**.

![Kopsavilkuma cilne Parametri](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Parametri** kopsavilkuma cilnē.

| Lauks       | Apraksts |
|-------------|-------------|
| Vārds, uzvārds        | Iepriekš definēts parametru saraksts. Papildinformāciju skatiet sadaļā [Parametru saraksts pēc darbības](#list-of-parameters-by-action). |
| Apraksts | Parametra apraksts. |
| Vērtība       | Parametra vērtība. |

#### <a name="list-of-parameters-by-action"></a>Parametru saraksts pēc darbības

Pieejamie parametri atšķiras atkarībā no darbības, kas atlasīta kopsavilkuma cilnē **Darbībās**.

###### <a name="action-sign-document"></a>Darbība: parakstīt dokumentu

| Parametrs                             | Apraksts |
|---------------------------------------|-------------|
| Ievades fails                            | Ievades XML dokumenta fails, kam jābūt parakstītam, izmantojot elektronisko parakstu. |
| Sertifikāta nosaukums                      | Krājumā esošā sertifikāta nosaukums. |
| Paraksta veids                        | Izmantojamā paraksta veids. |
| Paraksta metodes nosaukums                 | Paraksta metodes nosaukums, kas tiek izmantots elektroniskā paraksta ģenerēšanai. |
| Īssavilkuma metodes nosaukums                    | Īssavilkuma metode, kas tiek izmantota, lai elektroniskajā parakstā izveidotu īssavilkuma virkni. |
| Kanonizācijas metodes nosaukums          | Kanonizācijas metode, ko izmanto paraksta jaukšanas aprēķināšanai. |
| Atsauces atribūta nosaukums              | Atribūta nosaukums, kas norāda, kur paraksta elementā jāievieto atsauces ID. |
| Paraksta elementa nosaukums               | XML elementa nosaukums dokumentā, kam jābūt parakstītam, izmantojot elektronisko parakstu. Ja nav norādīts neviens elements, dokumenta sakne ir parakstīta. |
| Paraksta ievietošanai paredzētā elementa nosaukums   | XML elementa nosaukums, kurā jāievieto ģenerētais elektroniskais paraksts. Ja nav norādīts neviens elements, paraksts ir ievietots dokumenta saknē. |
| XLST fails ar īssavilkuma transformāciju       | Paplašināmās stila lapas valodas transformāciju (Extensible Stylesheet Language Transformations - XSLT) fails, kas satur īssavilkuma transformācijas neteikumus, lai ģenerētu īssavilkuma virkni elektroniskajam parakstam. |
| Ceļš uz īssavilkuma virknes ievietošanu          | Ceļš, kas atrodas **\<elementName\> .\<Attribute.Path\>** formāts no vietas, kur ir jāievieto ģenerētā īssavilkuma virkne. |
| Sertifikāta numura atrašanās vieta           | Elementa un atribūta nosaukums, kur jāievieto sertifikāta numurs. |
| Sertifikāta datu atrašanās vieta          | Elementa un atribūta nosaukums, kur jāievieto sertifikāta dati (base64). |
| Sertifikāta numurs ir ASCII formātā | Vērtība, kas norāda, vai sertifikāta numurs ir kodēts ASCII formātā. |

###### <a name="action-filestoreactionname"></a>Darbība: FileStoreActionName

| Parametrs  | Apraksts |
|------------|-------------|
| Ievades fails | Saglabāt ievades failu. |

###### <a name="action-transform-document"></a>Darbība: Transformēt dokumentu

| Parametrs                       | Apraksts |
|---------------------------------|-------------|
| Ievades fails                      | Avota fails, kas nodrošina datus, kas ir jāpalaiž darbībai. |
| Virziens                       | Vērtība, kas norāda, vai jāizmanto importēšanas formāts vai eksportēšanas formāts. |
| Konfigurācijas ID                | Formāts, kas jāizpilda. |
| Konfigurācijas versija           | Ja nav norādīta konfigurācijas versija, tiks izmantota jaunākā versija. |
| Konfigurācijas integrācijas punkts | Avota fails, kas nodrošina datus pārskata izpildlaikam. |

###### <a name="action-process-response"></a>Darbība: Apstrādāt atbildi

| Parametrs                    | Apraksts |
|------------------------------|-------------|
| Ievades fails                   | Atbilde uz analīzi. |
| Pārskatu konfigurāciju saraksts | To konfigurāciju saraksts, kas tiek izmantotas atbilžu parsēšanai. |

###### <a name="action-call-rest-web-service"></a>Darbība: Izsaukt REST tīmekļa pakalpojumu

| Parametrs                   | Apraksts |
|-----------------------------|-------------|
| Tīmekļa pakalpojuma URL             | Vietrādis URL, uz kuru sūtīt pieprasījumus. |
| Tīmekļa pieprasījuma taimauts         | Maksimālais laiks (milisekundēs), lai gaidītu tīmekļa pakalpojuma atbildi. |
| Pieprasījuma operācijas veids      | HTTP pieprasījuma operācijas veids (piemēram, **SAŅEMT**, **GRĀMATOT** vai **DZĒST**). |
| Sertifikāta nosaukumi           | Sertifikāta nosaukumi. |
| Atbildes pamatteksta kodējums      | Paredzamais HTTP atbildes struktūras kodējums, lai to varētu pareizi dekodēt. |
| HTTP pieprasījuma satura veids   | HTTP pieprasījuma satura veida galvenes ievade. |
| HTTP pieprasījuma satura pamatteksts   | HTTP pieprasījuma pamatteksts. (Pamatteksts var būt tukšs.) |
| HTTP parametru vaicājuma vērtības | Parametru vaicājuma vērtības, kas tiek izmantotas, lai aizpildītu vietrādi URL ar mainīgiem parametriem. |
| Pieprasīt maršrutu               | Maršruta ceļš HTTP pieprasījumam. Mainīgo parametrus var rakstīt **\{paramName\}** notācijā. Šeit ir piemērs: **"api/{id}/iesniegt"**. |
| Maršruta parametru saraksts        | Maršruta parametri galvenās vērtības notācijā, kas tiek izmantota, lai maršrutā iespraustu mainīgos. |
| Pielāgotas HTTP galvenes         | Pielāgotas HTTP galvenes, ko ievietot pieprasījumā. |
| HTTP pieprasījuma sīkfaili        | Sīkfailu saraksts galvenajā vērtības notācija, lai to ievietotu HTTP sīkfailu virsraksta pieprasījumā. |
| Drošības protokols           | Drošības protokols, ko izmantot HTTP pieprasījumiem, lai sazinātos ar serveri. (Pēc noklusējuma tiek izmantota transporta slāņa drošība \[TLS\] 1.2.) |

###### <a name="action-call-mexican-pac-service"></a>Darbība: Izsaukt Meksikas PAC pakalpojumu

| Parametrs                | Apraksts |
|--------------------------|-------------|
| Ievades fails               | Fails, kas satur XML datus, kas tiks nosūtīti uz tīmekļa pakalpojumu kā metodes ievades parametrs. |
| URL adrese              | Tīmekļa pakalpojuma adrese (galapunkts). |
| Tīmekļa metodes (darbības) nosaukums | Tās tīmekļa metodes (darbības) nosaukums, kas ir jāpalaiž. |
| Sertifikāti             | Sertifikātu ķēde, kas nepieciešama klienta autentifikācijai, izmantojot tīmekļa pakalpojumu. Klienta sertifikātam jābūt pēdējam sertifikātam ķēdē. Saknes un starpposma sertifikātiem ir jābūt pirmajiem. |
| Tīmekļa pieprasījuma taimauts      | Maksimālais laiks (milisekundēs), lai gaidītu tīmekļa pakalpojuma atbildi. |
| Atkārtošanas intervāls           | Intervāls starp mēģinājumiem izsaukt un saņemt atbildi no tīmekļa pakalpojuma. Ja intervāls nav norādīts, papildu atkārtots mēģinājums netiks veikts pēc tam, kad pirmais izsaukums nav sekmīgs. |
| Atkārtoto mēģinājumu skaits              | Maksimālais atkārtošanas mēģinājumu skaits, lai izsauktu un saņemtu atbildi no tīmekļa pakalpojuma. |
| Mēģināt vēlreiz, līdz               | Maksimālais laiks (milisekundēs), kad var turpināt atkārtotos izsaukumus. |
| Minimālā atkāpšanās         | Minimālās atkāpšanas līmenis atkārtoto mēģinājumu intervālu eksponenciālajam aprēķinam. |
| Maksimālā atkāpšanās         | Maksimālas atkāpšanas līmenis atkārtoto mēģinājumu intervālu eksponenciālajam aprēķinam. |
| Drošības protokols        | Drošības protokols, ko izmantot HTTP pieprasījumiem, lai sazinātos ar serveri. (Pēc noklusējuma tiek izmantots TLS 1.2.) |

###### <a name="action-call-brazilian-sefaz-service"></a>Darbība: Izsaukt Brazīlijas SEFAZ pakalpojumu

| Parametrs                | Apraksts |
|--------------------------|-------------|
| Ievades fails               | Fails, kas satur XML datus, kas tiks nosūtīti uz tīmekļa pakalpojumu kā metodes ievades parametrs. |
| URL adrese              | Tīmekļa pakalpojuma adrese (galapunkts). |
| Tīmekļa metodes (darbības) nosaukums | Tās tīmekļa metodes (darbības) nosaukums, kas ir jāpalaiž. |
| Sertifikāti             | Sertifikātu ķēde, kas nepieciešama klienta autentifikācijai, izmantojot tīmekļa pakalpojumu. Klienta sertifikātam jābūt pēdējam sertifikātam ķēdē. Saknes un starpposma sertifikātiem ir jābūt pirmajiem. |
| Tīmekļa pieprasījuma taimauts      | Maksimālais laiks (milisekundēs), lai gaidītu tīmekļa pakalpojuma atbildi. |
| Atkārtošanas intervāls           | Intervāls starp mēģinājumiem izsaukt un saņemt atbildi no tīmekļa pakalpojuma. Ja intervāls nav norādīts, papildu atkārtots mēģinājums netiks veikts pēc tam, kad pirmais izsaukums nav sekmīgs. |
| Atkārtoto mēģinājumu skaits              | Maksimālais atkārtošanas mēģinājumu skaits, lai izsauktu un saņemtu atbildi no tīmekļa pakalpojuma. |
| Mēģināt vēlreiz, līdz               | Maksimālais laiks (milisekundēs), kad var turpināt atkārtotos izsaukumus. |
| Minimālā atkāpšanās         | Minimālās atkāpšanas līmenis atkārtoto mēģinājumu intervālu eksponenciālajam aprēķinam. |
| Maksimālā atkāpšanās         | Maksimālas atkāpšanas līmenis atkārtoto mēģinājumu intervālu eksponenciālajam aprēķinam. |
| Drošības protokols        | Drošības protokols, ko izmantot HTTP pieprasījumiem, lai sazinātos ar serveri. (Pēc noklusējuma tiek izmantots TLS 1.2.) |

###### <a name="action-call-italian-sdi-service"></a>Darbība: Izsaukt Itālijas SDI pakalpojumu

| Parametrs                | Apraksts |
|--------------------------|-------------|
| Ievades fails               | Fails, kas satur XML datus, kas tiks nosūtīti uz tīmekļa pakalpojumu kā metodes ievades parametrs. |
| URL adrese              | Tīmekļa pakalpojuma adrese (galapunkts). |
| Tīmekļa metodes (darbības) nosaukums | Tās tīmekļa metodes (darbības) nosaukums, kas ir jāpalaiž. |
| Sertifikāti             | Sertifikātu ķēde, kas nepieciešama klienta autentifikācijai, izmantojot tīmekļa pakalpojumu. Klienta sertifikātam jābūt pēdējam sertifikātam ķēdē. Saknes un starpposma sertifikātiem ir jābūt pirmajiem. |
| Tīmekļa pieprasījuma taimauts      | Maksimālais laiks (milisekundēs), lai gaidītu tīmekļa pakalpojuma atbildi. |
| Atkārtošanas intervāls           | Intervāls starp mēģinājumiem izsaukt un saņemt atbildi no tīmekļa pakalpojuma. Ja intervāls nav norādīts, papildu atkārtots mēģinājums netiks veikts pēc tam, kad pirmais izsaukums nav sekmīgs. |
| Atkārtoto mēģinājumu skaits              | Maksimālais atkārtošanas mēģinājumu skaits, lai izsauktu un saņemtu atbildi no tīmekļa pakalpojuma. |
| Mēģināt vēlreiz, līdz               | Maksimālais laiks (milisekundēs), kad var turpināt atkārtotos izsaukumus. |
| Minimālā atkāpšanās         | Minimālās atkāpšanas līmenis atkārtoto mēģinājumu intervālu eksponenciālajam aprēķinam. |
| Maksimālā atkāpšanās         | Maksimālas atkāpšanas līmenis atkārtoto mēģinājumu intervālu eksponenciālajam aprēķinam. |
| Drošības protokols        | Drošības protokols, ko izmantot HTTP pieprasījumiem, lai sazinātos ar serveri. (Pēc noklusējuma tiek izmantots TLS 1.2.) |

### <a name="applicability-rules"></a>Piemērojamības kārtulas

Piemērojamības noteikumi ļauj izveidot loģiskus noteikumus, kas nosaka līdzekļa iestatījuma lietojuma kontekstu. Tādējādi saskaņošana starp kontekstu, ko sniedz biznesa dokuments, kas tiek nosūtīts apstrādei, kopā ar piemērojamības noteikuma kritērijiem, nosaka, kurš elektronisko rēķinu pievienošanas līdzeklis tiek izmantots, lai apstrādātu šo iesniegumu.

#### <a name="set-up-applicability-rules"></a>Piemērojamības noteikumu iestatīšana

1. Lapā **Līdzekļu versijas iestatīšana** cilnē **Piemērojamības noteikumi** atlasiet **Jauns**, lai pievienotu piemērojamības noteikumu.

    ![Piemērojamības noteikumu pārvaldība](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. Režģī atlasiet klauzulas, kas jāsagrupē.
3. Atlasiet **Grupas klauzula**.

    ![Klauzulu grupēšana](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    Kad klauzulas tiek grupētas, režģim tiek pievienota jauna kolonna. Šī kolonna norāda grupēto klauzulu loģisko operatoru.

    ![Grupētu klauzulu loģiskais operators](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

Lai atgrupētu klauzulas, atlasiet grupētās klauzulas atgrupēšanai un pēc tam atlasiet **Atgrupēt klauzulu**.

![Klauzulu atgrupēšana](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> Atgrupējot klauzulu, vienmēr sāciet no iekšējā grupēšanas līmeņa.

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Piemērojamības noteikumi** cilnē.

| Lauks         | Apraksts |
|---------------|-------------|
| Un/vai        | Loģiskais operators. |
| Lauks         | Lauks, ko izmantot, lai veidotu noteikumu. |
| Operatora tips | Operatora veids.<ul><li>Vienāds</li><li>Nav vienāds ar</li><li>Lielāks par/mazāks par</li><li>Lielāks par vai vienāds/mazāks par vai vienāds</li><li>Ietver</li><li>Sākt ar</li></ul> |
| Vērtība         | Kārtulas kritērijs. |

### <a name="variables"></a>Mainīgie

Varat izveidot mainīgos un pēc tam izmantot tos kā ievades vērtību konkrētas darbības parametram. Varat arī tās izmantot, lai apmainītos starp elektronisko rēķinu izrakstīšanas pievienojuma pakalpojumiem un klientu ar informāciju, kas ir rezultāts noteiktai darbībai, kā daļa no iesniegto dokumentu plūsmas.

#### <a name="set-up-variables"></a>Iestatīt mainīgos lielumus

- Lapas **Līdzekļu versijas iestatīšana** cilnē **Mainīgie** atlasiet **Jauns** vai **Dzēst**, lai pārvaldītu mainīgos.

    ![Mainīgo pārvaldība](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Mainīgie** cilnē.

| Lauks       | Apraksts |
|-------------|-------------|
| Vārds, uzvārds        | Mainīgo nosaukums. |
| Apraksts | Īss mainīgo apraksts. |
| tips        | Mainīgo veids.<ul><li><strong>Konstante</strong> – mainīgā saturs ir fiksēts.</li><li><strong>No klienta</strong> – mainīgā saturs tiek iegūts no Microsoft Dynamics 365 klienta iesniegšanas procesa izpildes laikā.</li><li><strong>Klientam</strong> – mainīgā saturs ir pieejams importēšanai Microsoft Dynamics 365 klientam iesniegšanas procesa izpildes laikā.</li></ul> |
| Datu veids   | Mainīgā datu veids:<ul><li>Būla</li><li>Datums</li><li>Skaits</li><li>UUID</li><li>Virkne</li><li>Fails</li></ul> |
| Vērtība       | Mainīgā vērtība vai darbības nosaukums, kas iestata mainīgā vērtību. |

### <a name="validate-the-feature-setup"></a>Validējiet līdzekļu iestatījumu

- Lapā **Līdzekļu versijas iestatīšana**, kas atrodas darbības rūtī, atlasiet **Validēt**, lai validētu līdzekļa versijas iestatījumu.

   ![Pogas Validēt atlasīšana](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

Validācija pārbauda visas konfigurācijas konsekvenci. Piemēram, ja noteikts darbības parametrs ir obligāts, bet tā vērtība paliek tukša, validācija atklāj šo neatbilstību, un jūs saņemat brīdinājumu.

## <a name="environments"></a>Vides

Elektronisko rēķinu izrakstīšanas pievienojuma videi ir jābūt saistītai ar elektronisko rēķinu izrakstīšanas pievienojuma līdzekli, un tam ir jābūt iespējotam. Elektronisko rēķinu izrakstīšanas pievienojuma vide ir jāizveido un jāpublicē iepriekš, izmantojot globalizācijas līdzekļu konfigurāciju jūsu organizācijas RCS kontā.

Lai iespējotu Elektronisko rēķinu izrakstīšanas pievienojuma vidi elektronisko rēķinu izrakstīšanas pievienojuma līdzeklim.

1. Lapā **Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļi** cilnē **Vides** atlasiet **Iespējot** līdzekļa iestatījumus elektronisko rēķinu izrakstīšanas pievienojuma vidi.
2. Laukā **Spēkā no** ievadiet datumu, kad jauna vide stājās spēkā.

![Iespējot elektronisko rēķinu izrakstīšanas pievienojumprogrammas vidi](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>Organizācijas

Elektronisko rēķinu izrakstīšanas pievienojuma līdzekli var koplietot vairākos uzņēmumos.

- Lapā **Elektroniskās rēķinu izrakstīšanas pievienojuma līdzekļi** cilnē **Organizācijas** atlasiet **Kopīgot ar**, lai pievienotu organizāciju, ar kuru vēlaties koplietot elektronisko rēķinu izrakstīšanas pievienojumprogrammu.

Lai apturētu elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa koplietošanu ar organizāciju, atlasiet **Noņemt koplietojumu**.

## <a name="versions"></a>Versijas

Versijas palīdz kontrolēt elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa dzīves ciklu, pārvaldot tā statusu. Varat izveidot jaunu esošā elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa versiju vai arī, ja ir pabeigta visa elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa konfigurācija, varat mainīt līdzekļa statusu uz **Pabeigts** un pēc tam uz **Publicēt**.

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-add-on-feature"></a>Izveidot jaunu esoša elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa versiju

1. Lapā **Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļi** režģī pa kreisi atlasiet elektronisko rēķinu izrakstīšanas pievienojuma līdzekli.
2. Cilnē **Versijas** atlasiet **Jauns**, lai pievienotu jaunu elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa versiju.

### <a name="change-the-status-of-the-electronic-invoicing-add-on-feature"></a>Mainīt elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa statusu

Veiciet šīs darbības, lai pārvaldītu elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa dzīves ciklu.

1. Lapā **Elektronisko rēķinu izrakstīšanas pievienojuma līdzekļi** režģī pa kreisi atlasiet elektronisko rēķinu izrakstīšanas pievienojuma līdzekli.
2. Cilnē **Versijas** atlasiet **Mainīt statusu** un pēc tam mainiet statusu no **Melnraksts** uz **Pabeigts**.
3. Tiek parādīta uzvedne, lai apstiprinātu, ka vēlaties aizpildīt elektronisko rēķinu izrakstīšanas pievienojuma līdzekli un visus tā komponentus. Atlasiet **Jā**, lai apstiprinātu darbību vai **Nē**, lai to atceltu.

    > [!NOTE]
    > Kad atlasāt **Jā**, konfigurācijas versiju, kas ir elektronisko rēķinu izrakstīšanas pievienojuma līdzekļa komponenti, statuss automātiski tiek mainīts no **Melnraksts** uz **Pabeigts**.

4. Atlasiet **Mainīt statusu** un pēc tam mainiet statusu no **Pabeigt** uz **Publicēt**.
5. Tiek parādīta uzvedne, lai apstiprinātu, ka vēlaties publicēt elektronisko rēķinu izrakstīšanas pievienojuma līdzekli un visus tā komponentus globālajā repozitorijā. Atlasiet **Jā**, lai apstiprinātu darbību vai **Nē**, lai to atceltu.

    > [!NOTE]
    > Kad atlasāt **Jā**, konfigurācijas versiju statuss tiek automātiski mainīts no **Pabeigts** uz **Koplietojams**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]