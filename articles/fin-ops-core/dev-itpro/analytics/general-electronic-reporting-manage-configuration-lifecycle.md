---
title: Elektronisko pārskatu veidošanas (ER) konfigurāciju dzīves cikla pārvaldība
description: Šajā tēmā ir aprakstīts, kā pārvaldīt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurāciju Dynamics 365 Finance.
author: NickSelin
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8b61082cf17707c952b6e07613769a671c349bb8fa92c21e3fe8524ef62dcb2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767783"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Elektronisko pārskatu veidošanas (ER) konfigurācijas dzīves cikla pārvaldība

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pārvaldīt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurāciju Dynamics 365 Finance.

## <a name="overview"></a>Pārskats

Elektronisko pārskatu izveide (ER) ir programma, kas nodrošina ar likumu noteikto un valstij raksturīgo elektronisko dokumentu atbalstu. Kopumā ER spēj veikt šādus uzdevumus attiecībā uz vienu elektronisko dokumentu. Papildinformāciju skatiet tēmā [Pārskats par elektronisko pārskatu (EP) veidošanu](general-electronic-reporting.md).

- Izveidot elektroniskā dokumenta veidni:

    - Identificēt nepieciešamos datu avotus, ko var prezentēt šajā dokumentā:

        - Pamata dati, piemēram, datu tabulas, datu ieraksti un klases.
        - Procesam specifiskie rekvizīti, piemēram, izpildes datums un laiks, laika josla.
        - Lietotāja ievadītie parametri, ko lietotājs norāda izpildes laikā.

    - Definēt nepieciešamos dokumenta elementus un to topoloģiju, lai norādītu galīgā dokumenta formātu.
    - Konfigurēt vēlamo datu plūsmu no atlasītajiem datu avotiem definētajiem dokumenta elementiem (izmantojot datu avota saistījumus dokumenta formāta komponentiem) un norādīt procesa kontroles loģiku.

- Padarīt veidni pieejamu, lai to varētu izmantot citās instancēs:

    - Pārveidot dokumenta veidni, kas izveidota programmā Dynamics AX, par ER konfigurāciju un eksportēt konfigurāciju no pašreizējās programmas instances kā XML pakotni, kuru var glabāt lokāli vai Lifecycle Services (LCS).
    - Pārveidot ER konfigurāciju par programmas dokumenta veidni.
    - Importēt XML pakotni, kas tiek glabāta lokāli vai LCS pašreizējā instancē.

- Pielāgot elektroniskā dokumenta veidni:

    - Pārnest veidni no LCS uz pašreizējo instanci kā ER konfigurāciju.
    - Izveidot ER konfigurācijas pielāgotu versiju un saglabāt atsauci uz tās bāzes versiju.

- Integrēt veidni noteiktā biznesa procesā, lai tā būtu pieejama programmā:

    - Konfigurēt iestatījumus, lai programma sāktu izmantot ER konfigurāciju, atsaucoties uz attiecīgo konfigurāciju ar procesu saistītā parametrā. Piemēram, ietveriet atsauci uz ER konfigurāciju noteiktā kreditoru parādu maksājumu metodē, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu.

- Izmantot veidni noteiktā biznesa procesā:

    - Izpildīt ER konfigurāciju konkrētā biznesa procesā. Piemēram, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu, ja ir atlasīta maksājumu metode ar atsauci uz ER konfigurāciju.

## <a name="concepts"></a>Koncepcijas
Ar ER konfigurācijas dzīves ciklu ir saistītas tālāk norādītās lomas un saistītās darbības.

| Loma                                       | Aktivitātes                                                      | Apraksts |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Elektronisko pārskatu veidošanas funkcionālais konsultants | Izveidojiet un pārvaldiet ER komponentus (modeļus un formātus).           | Biznesa procesos iesaistīta persona, kura izstrādā ER domēnam specifiskos datu modeļu, izstrādā nepieciešamās elektronisko dokumentu veidnes un atbilstoši tās saista. |
| Elektroniskā pārskata izstrādātājs             | Izveidojiet un pārvaldiet datu modeļu kartējumus.                          | Dynamics AX speciālists, kurš atlasa nepieciešamos Finance datu avotus un saista tos ar ER domēnam specifiskiem datu modeļiem. |
| Uzskaites supervizors                      | Konfigurēt ar procesu saistītos iestatījumus, kam ir atsauce uz ER artefaktiem. | Piemēram, loma **Uzskaites supervizors**, kas sniedz iespēju ER konfigurācijas iestatījumus izmantot noteiktā kreditoru parādu maksājumu metodē, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu. |
| Kreditoriem maksājamo rēķinu darbinieks            | Izmantot ER artefaktus noteiktā biznesa procesā.                | Piemēram, loma **Kreditoriem maksājamo rēķinu darbinieks**, kas sniedz iespēju ģenerēt rēķinu apstrādes elektroniskos maksājumu ziņojumus, pamatojoties uz ER formātu, kas ir konfigurēts noteiktai maksājumu metodei. |

## <a name="er-configuration-development-lifecycle"></a>ER konfigurācijas izstrādes dzīves cikls
Tālāk minēto ar ER saistīto apsvērumu dēļ ER konfigurācijas ir ieteicams veidot izstrādes vidē kā atsevišķā Finance and Operations instancē:

- Lietotāji, kam ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var rediģēt konfigurācijas un palaist tās testēšanas nolūkos. Šis scenārijs var izraisīt klašu un tabulu metožu izsaukumus, kas var kaitēt biznesa datiem un instances izmantošanas veiktspējai.
- Klašu un tabulu metožu kā ER konfigurāciju ER datu avotu izsaukumus neierobežo ieejas punkti un reģistrēts uzņēmuma saturs. Tādēļ lietotāji, kuriem ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var piekļūt konfidenciāliem uzņēmuma datiem.

Izstrādes vidē izstrādātās ER konfigurācijas var [augšupielādēt](#data-persistence-consideration) testēšanas vidē konfigurācijas novērtēšanai (pareiza procesu integrācija, pareizi rezultāti un veiktspēja) un kvalitātes nodrošināšanai (pareizas lomu piekļuves tiesības un pienākumu sadale). Šim nolūkam var izmantot ER konfigurāciju apmaiņas līdzekļus. Apstiprinātās ER konfigurācijas var augšupielādēt LCS, lai tās koplietotu ar pakalpojumu abonentiem, vai tās var [importēt](#data-persistence-consideration) ražošanas vidē iekšējai izmantošanai.

![ER konfigurācijas dzīves cikls.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Datu noturības apsvērumi

Dažādas ER [konfigurācijas](general-electronic-reporting.md#Configuration) [versijas](general-electronic-reporting.md#component-versioning) var [importēt](tasks/er-import-configuration-lifecycle-services.md) atsevišķi uz Finance instanci. Kad tiek importēta jauna ER konfigurācijas versija, sistēma kontrolē šīs konfigurācijas melnraksta versijas saturu:

- Kad importētā versija ir zemāka nekā visaugstākā šīs konfigurācijas versija pašreizējā Finance instancē, šīs konfigurācijas melnraksta versijas saturs paliek nemainīgs.
- Kad importētā versija ir augstāka nekā jebkura cita šīs konfigurācijas versija pašreizējā Finance instancē, importētās versijas saturs tiek kopēts šīs konfigurācijas melnraksta versijā, lai ļautu turpināt rediģēt pēdējo pabeigto versiju.

Ja šī konfigurācija pieder pašlaik aktivizētām konfigurācijas [nodrošinātājam](general-electronic-reporting.md#Provider), šīs konfigurācijas melnraksta versija ir redzama lapas **Konfigurācijas** kopsavilkuma cilnē **Versijas** (**Organizācijas administrēšana** > **Elektronisko pārskatu veidošana** > **Konfigurācijas**). Varat atlasīt konfigurācijas melnraksta versiju un [modificēt](er-quick-start2-customize-report.md#ConfigureDerivedFormat) tās saturu, izmantojot atbilstīgo ER veidotāju. Kad esat rediģējis ER konfigurācijas melnraksta versiju, tās saturs vairs neatbilst šīs konfigurācijas augstākās versijas saturam pašreizējā Finance instancē. Lai novērstu jūsu izmaiņu zudumus, sistēma parādā kļūdu, ka imports nevar turpināties, jo šīs konfigurācijas versija ir augstāka par augstāko šīs konfigurācijas versiju pašreizējā Finance instancē. Kad tā notiek, piemēram, ar formāta konfigurāciju **X**, tiek rādīta kļūda **Formāta 'X' versija nav pabeigta**.

Lai atsauktu melnraksta versijā ieviestās izmaiņas, atlasiet visaugstāko pabeigto vai koplietojamo jūsu ER konfigurācijas versiju pakalpojumā Finance, kopsavilkuma cilnē **Versijas** un pēc tam atlasiet opciju **Iegūt šo versiju**. Atlasītās versijas saturs tiek kopēts melnraksta versijā.

## <a name="applicability-consideration"></a>Piemērojamības apsvērumi

Veidojot jaunu ER konfigurācijas versiju, var definēt tās [atkarību](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) no citiem programmatūras komponentiem. Šis solis tiek uzskatīts par priekšnoteikumu, lai kontrolētu šīs konfigurācijas versijas lejupielādi no ER repozitorija vai ārēja XML faila un jebkādu turpmāku šīs versijas izmantošanu. Mēģinot importēt jaunu ER konfigurācijas versiju, sistēma izmanto konfigurētos priekšnosacījumus, lai kontrolētu, vai šo versiju var importēt.

Dažos gadījumos var būt nepieciešams, lai sistēma ignorētu konfigurētos priekšnosacījumus, kad importējat jaunas ER konfigurāciju versijas. Lai importa laikā sistēma ignorētu priekšnosacījumus, veiciet šīs darbības.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Iestatiet **Izlaist produkta atjauninājumus un versijas priekšnosacījumu pārbaudi importēšanas laikā** uz **Jā**.

    > [!NOTE]
    > Šis parametrs ir lietotājam raksturīgs un uzņēmumam raksturīgs.

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)

[Elektronisko pārskatu konfigurāciju atkarības no citiem komponentiem definēšana](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
