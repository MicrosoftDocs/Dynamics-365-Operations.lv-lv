---
title: Elektronisko pārskatu veidošanas (ER) konfigurācijas dzīves cikla pārvaldība
description: Šajā rakstā ir aprakstīts, kā pārvaldīt Dynamics 365 Finance elektronisko pārskatu (ER) konfigurāciju dzīves ciklu.
author: kfend
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 0209679c9882d87edab68d043fba9e7b3400a2a2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337265"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Elektronisko pārskatu veidošanas (ER) konfigurācijas dzīves cikla pārvaldība

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā pārvaldīt [Dynamics](general-electronic-reporting.md) 365 Finance elektronisko pārskatu (ER) [konfigurāciju](general-electronic-reporting.md#Configuration) dzīves ciklu.

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
Turpmākajiem ar ER saistītajiem iemesliem ir ieteicams izstrādes vidē veidot ER konfigurācijas kā atsevišķu finanšu un operāciju gadījumu:

- Lietotāji, kam ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var rediģēt konfigurācijas un palaist tās testēšanas nolūkos. Šis scenārijs var izraisīt klašu un tabulu metožu izsaukumus, kas var kaitēt biznesa datiem un instances izmantošanas veiktspējai.
- Klašu un tabulu metožu kā ER konfigurāciju ER datu avotu izsaukumus neierobežo ieejas punkti un reģistrēts uzņēmuma saturs. Tādēļ lietotāji, kuriem ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var piekļūt konfidenciāliem uzņēmuma datiem.

Izstrādes vidē izstrādātās ER konfigurācijas var [augšupielādēt](#data-persistence-consideration) testēšanas vidē konfigurācijas novērtēšanai (pareiza procesu integrācija, pareizi rezultāti un veiktspēja) un kvalitātes nodrošināšanai (pareizas lomu piekļuves tiesības un pienākumu sadale). Šim nolūkam var izmantot ER konfigurāciju apmaiņas līdzekļus. Apstiprinātās ER konfigurācijas var augšupielādēt LCS, lai tās koplietotu ar pakalpojumu abonentiem, vai tās var [importēt](#data-persistence-consideration) ražošanas vidē iekšējai izmantošanai.

![ER konfigurācijas dzīves cikls.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Datu noturības apsvērumi

Dažādas ER [konfigurācijas](tasks/er-import-configuration-lifecycle-services.md) [versijas var importēt atsevišķi uz](general-electronic-reporting.md#Configuration) finanšu instanci. Kad tiek importēta jauna ER konfigurācijas versija, sistēma kontrolē šīs konfigurācijas melnraksta versijas saturu:

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

## <a name="dependencies-on-other-components"></a>Citu komponentu atkarības

ER konfigurācijas var konfigurēt, kā atkarīgas [no](er-download-configurations-global-repo.md#import-filtered-configurations) citām konfigurācijām. Piemēram, [varat importēt ER datu modeļa konfigurāciju no globālā repozitorija savā Microsoft regulēšanas konfigurācijas pakalpojumos (RCS)](er-download-configurations-global-repo.md) vai Dynamics 365 finanšu instancē, un pēc tam izveidot jaunu [ER](er-overview-components.md#data-model-component)[...](../../../finance/localizations/rcs-overview.md)[...](er-overview-components.md#format-component)[formāta konfigurāciju, kas ir atvasināta no importētās ER datu modeļa konfigurācijas.](er-quick-start2-customize-report.md#DeriveProvidedFormat) Atvasinātā ER formāta konfigurācija būs atkarīga no bāzes ER datu modeļa konfigurācijas.

![Atvasinātā ER formāta konfigurācija lapā Konfigurācijas.](./media/ger-configuration-lifecycle-img1.png)

Kad formāta izstrāde pabeigta, varat mainīt ER formāta konfigurācijas sākotnējās versijas statusu no Melnraksts **uz** **Pabeigts**. Pēc tam varat kopīgot ER formāta konfigurācijas pabeigto versiju, publicējot [to globālajā](../../../finance/localizations/rcs-global-repo-upload.md) repozitorijā. Pēc tam varat piekļūt globālajai repozitorijai no jebkuras RCS vai Finanšu mākoņa instances. Varat importēt jebkuru ER konfigurācijas versiju, kas lietojumprogrammai ir piemērojama no globālā repozitorija šajā lietojumprogrammā.

![Publicētā ER formāta konfigurācija konfigurācijas repozitorija lapā.](./media/ger-configuration-lifecycle-img2.png)

Balstoties uz konfigurācijas atkarību, kad izvēlaties ER formāta konfigurāciju globālajā repozitorijā, lai importētu to uz jaunizveidotu RCS vai finanšu instanci, bāzes ER datu modeļa konfigurācija automātiski tiek atrasta globālajā repozitorijā un importēta kopā ar izvēlēto ER formāta konfigurāciju, kā bāzes konfigurāciju.

Savu ER formāta konfigurācijas versiju var eksportēt arī no pašreizējās RCS vai finanšu instances un saglabāt to lokāli kā XML failu.

![Eksportē ER formāta konfigurācijas versiju kā XML konfigurācijas lapā.](./media/ger-configuration-lifecycle-img3.png)

**Finanšu versijās pirms versijas 10.0.29**, kad mēģināt importēt ER formāta konfigurācijas versiju no šī XML faila vai no repozitorija, kas nav Globālais repozitorijs jaunā izvietotā RCS vai finanšu instancē, kurā vēl nav nevienas ER konfigurācijas, tiks parādīts šāds izņēmums, lai jūs informētu, ka pamat konfigurāciju nevar iegūt:

> Palikušas neatrisinātas atsauces.<br>
Nevar izveidot objekta '\<imported configuration name\>' atsauci uz objektu 'Bāze' (\<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>).

![Tiek importēta ER formāta konfigurācijas versija konfigurācijas repozitorija lapā.](./media/ger-configuration-lifecycle-img4.gif)

**Ja** pamat konfigurāciju nevar atrast pašreizējā programmas instancē vai avota repozitorijā, ko pašlaik izmantojat (ja piemērojams), ER struktūra automātiski mēģinās atrast trūkstošās bāzes konfigurācijas nosaukumu globālajā repozitorija kešatmiņā. Tad tā piedāvās trūkstošās pamatkonfigurēšanas nosaukumu un globāli unikālo identifikatoru (GUID) izņēmuma, kas tiek izmests, tekstā.

> Palikušas neatrisinātas atsauces.<br>
Nevar izveidot objekta '\<imported configuration name\>' atsauci uz objektu 'Bāze' (\<name of the missed base configuration\>\<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>)

![Izņēmums konfigurācijas repozitorija lapā, ja pamatkonfigurēšanu nevar atrast.](./media/ger-configuration-lifecycle-img5.png)

Varat izmantot šo nosaukumu, lai atrastu pamat konfigurāciju un pēc tam to importētu manuāli.

> [!NOTE]
> Šī jaunā [opcija darbojas tikai tad, kad vismaz viens lietotājs jau ir pieteicies globālajā repozitorijā, izmantojot konfigurācijas repositories](er-download-configurations-global-repo.md#open-configurations-repository)[lapu vai vienu no globālajiem repozitorija uzmeklēšanas](er-extended-format-lookup.md) laukiem pašreizējā finanšu instancē un kad globālā repozitorija saturs ir ierakstīts kešatmiņā.

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)

[Elektronisko pārskatu konfigurāciju atkarības no citiem komponentiem definēšana](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

