---
title: Commerce kanālu finanšu integrācijas apskats
description: Šajā tēmā ir sniegts apskats par finanšu integrācijas iespējām, kas ir pieejamas programmā Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 01/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 82913eaca1d56a5b0609480d8825717278eca132
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077196"
---
# <a name="overview-of-fiscal-integration-for-commerce-channels"></a>Commerce kanālu finanšu integrācijas apskats

[!include [banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Šajā tēmā ir sniegts apskats par finanšu integrācijas iespējām, kas ir pieejamas programmā Dynamics 365 Commerce. 

Finanšu integrācija ietver integrāciju ar dažādām finanšu ierīcēm un pakalpojumiem, kas nodrošina tirdzniecības pārdošanas darbību finanšu reģistrāciju saskaņā ar vietējiem likumiem par nodokļiem, kuru mērķis ir novērst ar nodokļiem saistītu krāpniecību mazumtirdzniecības nozarē. Tālāk ir norādīti daži tipiski scenāriji, kuros var izmantot finanšu integrāciju.

- Reģistrējiet tirdzniecības pārdošanas darbību finanšu ierīcē, kas ir savienota ar programmu Point of Sale (POS), piemēram fiskālo printeri, un izdrukājiet debitoram paredzētu finanšu dokumentu.
- Drošā veidā iesniedziet ar programmā Retail POS veiktajām pārdošanas un atgriešanas darbībām saistīto informāciju ārējā tīmekļa pakalpojumā, kura darbību nodrošina nodokļu iestāde.
- Palīdziet nodrošināt pārdošanas transakciju datu nemaināmību, izmantojot ciparparakstus.

Finanšu integrācijas funkcionalitāte ir struktūra, kas nodrošina kopēju risinājumu tālākai programmas Retail POS un finanšu ierīču un pakalpojumu integrācijas izstrādei un pielāgošanai. Funkcionalitātē ir ietverti arī finanšu integrācijas paraugi, kas atbalsta pamata scenārijus noteiktās valstīs vai reģionos un darbojas ar noteiktām finanšu ierīcēm vai pakalpojumiem. Finanšu integrācijas paraugu veido vairāki programmas Commerce komponentu paplašinājumi, un tas ir iekļauts programmatūras izstrādes komplektā (SDK). Plašāku informāciju par finanšu integrācijas paraugiem skatiet tēmā [Finanšu integrācijas paraugi programmā Commerce SDK](#fiscal-integration-samples-in-the-commerce-sdk). Papildinformāciju par to, kā instalēt un izmantot komplektu Commerce SDK, skatiet rakstā [Retail programmatūras izstrādes komplekta (SDK) arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Lai nodrošinātu tādu scenāriju atbalstu, kurus neatbalstīta finanšu integrācijas paraugs, integrētu programmu Retail POS ar citām finanšu ierīcēm vai pakalpojumiem, vai izpildītu citās valstīs vai reģionos spēkā esošās prasības, ir jāpaplašina kāds no esošajiem finanšu integrācijas paraugiem vai jāizveido jauns paraugs, kā piemēru izmantojot esošu paraugu.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Fiskālās reģistrācijas process un fiskālās integrācijas paraugi fiskālajām ierīcēm un pakalpojumiem

Finanšu reģistrācijas process programmā Retail POS var sastāvēt no vienas vai vairākām darbībām. Katra darbība ietver noteiktu transakciju vai notikumu finanšu reģistrāciju vienā finanšu ierīcē vai pakalpojumā. Fiskālā ierīcē vai pakalpojumā fiskālā reģistrācijā piedalās šādi risinājuma komponenti:

- **Fiskālo dokumentu nodrošinātājs** – Šis komponents serializē darījumu/notikumu datus formātā, kas tiek izmantots arī mijiedarbībai ar fiskālo ierīci vai pakalpojumu, parsē atbildes no fiskālās ierīces vai pakalpojuma un saglabā atbildes kanāla datu bāzē. Šis paplašinājums nosaka arī konkrētās transakcijas un notikumus, kas ir jāreģistrē.
- **Fiskālais savienotājs** – Šis komponents inicializē saziņu ar fiskālo ierīci vai pakalpojumu, nosūta pieprasījumus vai tiešas komandas uz fiskālo ierīci vai pakalpojumu, pamatojoties uz darījuma/notikuma datiem, kas iegūti no fiskālā dokumenta, un saņem atbildes no fiskālās ierīces vai pakalpojuma.

Fiskālās integrācijas paraugā var būt ietverts Commerce izpildlaiks (CRT), Aparatūras stacija un POS paplašinājumi fiskālo dokumentu nodrošinātājam un fiskālajam savienotājam. Tajā ir ietvertas arī tālāk norādītās komponentu konfigurācijas.

- **Finanšu dokumentu nodrošinātāja konfigurācija** — šajā konfigurācijā ir definēta izvades metodi un finanšu dokumentu formāts. Tajā ir ietverta arī nodokļu un maksājumu metožu datu kartēšana, lai dati no mazumtirdzniecības POS būtu saderīgi ar vērtībām, kas iepriekš noteiktas fiskālā ierīcē vai pakalpojuma programmaparatūrā.
- **Fiskālā savienotāja konfigurācija** – Šī konfigurācija nosaka fizisko saziņu ar konkrēto fiskālo ierīci vai pakalpojumu.

Noteiktas POS kases sistēmas finanšu reģistrācijas process tiek definēts, izmantojot atbilstošo iestatījumu POS funkcionalitātes profilā. Papildinformāciju par to, kā konfigurēt fiskālo reģistrācijas procesu, augšupielādēt fiskālo dokumentu nodrošinātāja un fiskālā savienotāja konfigurācijas un mainīt konfigurācijas parametrus, skatiet sadaļā [Iestatiet fiskālās reģistrācijas procesu](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Tālāk norādītā tipiskā fiskālā reģistrācijas plūsma sākas ar notikumu POS (piemēram, pārdošanas darījuma pabeigšanu) un ievieš iepriekš noteiktu darbību secību, kas ietver citus Commerce komponentus (piemēram,CRT un aparatūras stacija).

1. POS pieprasa fiskālo dokumentu no fiskālās integrācijas ietvara (FIF).
1. FIF nosaka, vai aktuālajam notikumam ir nepieciešama fiskālā reģistrācija.
1. Pamatojoties uz fiskālās reģistrācijas procesa iestatījumiem, FIF identificē fiskālo savienotāju un atbilstošo fiskālo dokumentu nodrošinātāju, ko izmantot fiskālajai reģistrācijai.
1. FIF vada fiskālo dokumentu nodrošinātāju, kas ģenerē fiskālo dokumentu (piemēram, XML dokumentu), kas atspoguļo darījumu vai notikumu.
1. FIF atdod ģenerēto fiskālo dokumentu POS.
1. POS pieprasa, lai FIF iesniedz fiskālo dokumentu fiskālā ierīcei vai pakalpojumam.
1. FIF vada fiskālo savienotāju, kas apstrādā fiskālo dokumentu un iesniedz to fiskālajai ierīcei vai pakalpojumam.
1. FIF atgriež fiskālo atbildi (tas ir, fiskālā ierīces vai pakalpojuma atbildi) POS.
1. POS analizē fiskālo reakciju, lai noteiktu, vai fiskālā reģistrācija bija veiksmīga. Ja nepieciešams, POS pieprasa, lai FIF apstrādā visas radušās kļūdas. 
1. POS pieprasa, lai FIF apstrādātu un saglabātu fiskālo atbildi.
1. Fiskālā dokumenta nodrošinātājs apstrādā fiskālo atbildi. Šīs apstrādes ietvaros fiskālā dokumenta nodrošinātājs parsē atbildi un izvelk no tās paplašinātos datus.
1. FIF saglabā atbildi un paplašinātos datus kanālu datu bāzē.
1. Ja nepieciešams, POS izdrukā kvīti, izmantojot parasto kvīšu printeri, kas ir pievienots aparatūras stacijai. Kvīts var saturēt nepieciešamos datus no fiskālās atbildes.
 
Šajos piemēros ir parādītas fiskālās reģistrācijas izpildes plūsmas tipiskām fiskālajām ierīcēm vai pakalpojumiem.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Fiskālā reģistrācija tiek veikta, izmantojot ierīci, kas savienota ar aparatūras staciju

Šī konfigurācija tiek izmantota, ja aparatūras stacijai ir pievienota fiziska fiskālā ierīce, piemēram, fiskālais printeris. Tas ir piemērojams arī tad, ja saziņa ar fiskālo ierīci vai pakalpojumu tiek veikta, izmantojot programmatūru, kas ir instalēta aparatūras stacijā. Šajā gadījumā fiskālo dokumentu nodrošinātājs atrodas vietnē CRT, un fiskālais savienotājs atrodas aparatūras stacijā.

![Fiskālā reģistrācija tiek veikta, izmantojot ierīci, kas savienota ar aparatūras staciju.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Fiskālā reģistrācija tiek veikta, izmantojot ārpakalpojumu

Šī konfigurācija tiek izmantota, ja fiskālā reģistrācija tiek veikta, izmantojot ārēju pakalpojumu, piemēram, tīmekļa pakalpojumu, ko nodrošina nodokļu iestāde. Šajā gadījumā gan fiskālā dokumenta nodrošinātājs, gan fiskālais savienotājs atrodas uz CRT.

![Fiskālā reģistrācija tiek veikta, izmantojot ārpakalpojumu.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Fiskālā reģistrācija tiek veikta iekšēji CRT

Šī konfigurācija tiek izmantota, ja fiskālajai reģistrācijai nav nepieciešama ārēja fiskālā ierīce vai pakalpojums. Piemēram, to izmanto, ja fiskālā reģistrācija tiek veikta, izmantojot pārdošanas darījumu digitālo parakstu. Šajā gadījumā gan fiskālā dokumenta nodrošinātājs, gan fiskālais savienotājs atrodas uz CRT.

![Fiskālā reģistrācija tiek veikta iekšēji CRT.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Fiskālā reģistrācija tiek veikta, izmantojot ierīci vai pakalpojumu lokālajā tīklā

Šī konfigurācija tiek izmantota, ja veikala lokālajā tīklā atrodas fiziska fiskālā ierīce vai fiskālais pakalpojums un nodrošina HTTPS lietojumprogrammu saskarni (API). Šajā gadījumā fiskālo dokumentu nodrošinātājs atrodas vietnē CRT, un fiskālais savienotājs atrodas POS.

![Fiskālā reģistrācija tiek veikta, izmantojot ierīci vai pakalpojumu lokālajā tīklā.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Kļūdu apstrāde

Finanšu integrācijas struktūra nodrošina tālāk norādītās opcijas kļūmju apstrādei finanšu reģistrācijas laikā.

- **Mēģināt vēlreiz** — operatori var izmantot šo opciju gadījumā, ja kļūmi var ātri novērst un var atkārtoti izpildīt finanšu reģistrāciju. Piemēram, šo opciju var izmantot gadījumā, ja finanšu ierīce nav pievienota vai fiskālajā printerī ir beidzies vai iesprūdis papīrs.
- **Atcelt** — šī opcija sniedz operatoriem iespēju atlikt pašreizējās transakcijas vai notikuma finanšu reģistrāciju, ja tā neizdodas. Pēc reģistrācijas atlikšanas operators var turpināt strādāt ar POS sistēmu un veikt jebkuru operāciju, kam nav nepieciešama finanšu reģistrācija. Kad POS sistēmā notiek notikums, kam ir nepieciešama finanšu reģistrācija (piemēram, tiek atvērta jauna transakcija), tiek automātiski parādīts kļūdu apstrādes dialoglodziņš, kurā operatoram tiek paziņots, ka iepriekšējā transakcija netika pareizi reģistrēta, un tiek norādītas kļūdu apstrādes iespējas.
- **Izlaist** — operatori var izmantot šo opciju gadījumā, ja finanšu reģistrāciju var izlaist noteiktos apstākļos un POS sistēmā var turpināt veikt parastās operācijas. Piemēram, šo opciju var izmantot gadījumā, ja pārdošanas transakciju, kuras finanšu reģistrācija neizdevās, var reģistrēt īpašā papīra žurnālā.
- **Atzīmēt kā reģistrētu** — operatori var izmantot šo opciju gadījumā, ja transakcija ir reģistrēta finanšu ierīcē (piemēram, ir izdrukāts finanšu dokuments), taču, saglabājot finanšu atbildi kanāla datu bāzē, ir radusies kļūme.
- **Atlikt** – Operatori var izmantot šo opciju, ja darījums nav reģistrēts, jo reģistrācijas pakalpojums nebija pieejams. 

> [!NOTE]
> The **Izlaist**, **kā reģistrētu**, un **Atlikt** opcijas ir jāaktivizē fiskālās reģistrācijas procesā, pirms tās tiek izmantotas. Turklāt operatoriem ir jāpiešķir atbilstošās atļaujas.

The **Izlaist**, **kā reģistrētu**, un **Atlikt** opcijas ļauj informācijas kodiem tvert noteiktu informāciju par kļūmi, piemēram, kļūmes iemeslu vai fiskālās reģistrācijas izlaišanas pamatojumu vai darījuma atzīmēšanu kā reģistrētu. Papildinformāciju par to, kā iestatīt kļūdu apstrādes parametrus, skatiet rakstā [Kļūdu apstrādes iestatījumu veikšana](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Neobligāta finanšu reģistrācija

Finanšu reģistrācija var būt obligāta dažām operācijām, bet neobligāta citām. Piemēram, regulāras pārdošanas un atgriešanas finanšu reģistrācija var būt obligāta, bet ar klienta iemaksām saistītu operāciju finanšu reģistrācija var būt neobligāta. Šajā gadījumā finanšu reģistrācijas neveikšana pārdošanas darījumam bloķē turpmāku pārdošanu, bet finanšu reģistrācijas neveikšana attiecībā uz klienta iemaksu nebloķē turpmāku pārdošanu. Lai nodalītu obligātas un neobligātas operācijas, ieteicams tās apstrādāt, izmantojot dažādus dokumentu nodrošinātājus un iestatīt atsevišķus soļus finanšu reģistrācijas procesā šiem nodrošinātājiem. Parametram **Kļūdas gadījumā turpināt** ir jābūt iespējotam visiem soļiem, kas saistīti ar papildu finanšu reģistrāciju. Papildinformāciju par to, kā iestatīt kļūdu apstrādes parametrus, skatiet rakstā [Kļūdu apstrādes iestatījumu veikšana](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Manuāli atkārtoti veiciet fiskālo reģistrāciju

Ja darījuma vai notikuma finanšu reģistrācija ir atlikta pēc kļūmes (piemēram, ja operators atlasīja **Atcelt** kļūdu apstrādes dialoglodziņā), varat manuāli atkārtoti izpildīt finanšu reģistrāciju, izsaucot atbilstošu operāciju. Papildinformāciju skatiet tēmā [Atliktas finanšu reģistrācijas manuālas izpildes iespējošana](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="postpone-option"></a>Atlikt iespēju

The **Atlikt** opcija ļauj turpināt fiskālās reģistrācijas procesu, ja pašreizējā darbība neizdodas. To var izmantot, ja ir fiskālās reģistrācijas rezerves opcija.

### <a name="fiscal-registration-health-check"></a>Finanšu reģistrācijas darbspējas pārbaude

Finanšu reģistrācijas darbspējas pārbaudes procedūra pārbauda finanšu ierīces vai pakalpojuma pieejamību noteiktu notikumu gadījumā. Ja pašlaik nevar izpildīt finanšu reģistrāciju, operators saņem iepriekšēju paziņojumu.

POS veic darbspējas pārbaudi šādu notikumu gadījumā:

- Tiek atvērts jauns darījums.
- Tiek veikta aizturēta darījuma atsaukšana.
- Tiek pabeigts pārdošanas vai atgriešanas darījums.

Ja darbspējas pārbaude neizdodas, POS rāda darbspējas pārbaudes dialoglodziņu. Minētajā dialoglodziņā ir pieejamas šādas pogas:

- **Labi** — šī poga ļauj operatoram ignorēt darbspējas pārbaudes kļūdu un turpināt, lai apstrādātu darījumu. Operatori var atlasīt šo pogu tikai tad, ja tiem ir iespējota atļauja **Atļaut izlaist darbspējas pārbaudes kļūdu**.
- **Atcelt** — ja operators izvēlas šo pogu, POS atceļ pēdējo darbību (piemēram, krājums nav pievienots jaunam darījumam).

> [!NOTE]
> Veselības pārbaude tiek veikta tikai tad, ja pašreizējai darbībai ir nepieciešama fiskālā reģistrācija un ja **Turpiniet ar kļūdu** parametrs ir atspējots pašreizējam fiskālās reģistrācijas procesa posmam. Plašāku informāciju skatiet tēmā [Kļūdu apstrādes iestatījumu veikšana](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Finanšu atbildes saglabāšana finanšu transakcijā

Ja transakcijas vai notikuma finanšu reģistrācija ir veiksmīga, kanāla datu bāzē tiek izveidota finanšu transakcija, kas tiek saistīta ar sākotnējo transakciju vai notikumu. Līdzīgi gadījumā, ja neveiksmīgai finanšu reģistrācijai tiek atlasīta opcija **izlaist** vai **Atzīmēt kā reģistrētu**, šī informācija tiek saglabāta finanšu transakcijā. Finanšu transakcijā ir ietverta finanšu ierīces vai pakalpojuma finanšu atbilde. Ja finanšu reģistrācijas process sastāv no vairākām darbībām, katrai procesa darbībai, kuras rezultāts ir veiksmīga vai neveiksmīga reģistrācija, tiek izveidota finanšu transakcija.

Finanšu transakcijas kopā ar transakcijām tiek pārsūtītas uz Headquarters, izmantojot funkciju *P darbs*. Lapas **Veikalu transakcijas** kopsavilkuma cilnē **Finanšu transakcijas** varat skatīt finanšu transakcijas, kas ir saistītas ar transakcijām.

Finanšu transakcijā ir saglabāta tālāk norādītā detalizētā informācija.

- Detalizēta informācija par finanšu reģistrācijas procesu (par procesu, savienotāju grupu, savienotāju utt.). Turklāt laukā **Kases sistēmas numurs** tiek glabāts finanšu ierīces sērijas numurs, ja šī informācija ir ietverta finanšu atbildē.
- Finanšu reģistrācijas statuss: **Pabeigts veiksmīgai reģistrācijai, Izlaists**, **ja operators atlasiet** opciju Izlaist **neveiksmīgai reģistrācijai, Atzīmēts kā reģistrēts**, **ja operators izvēlējās** opciju Atzīmēt kā reģistrētu **, vai** Atlikts, ja operators atlasījis **opciju** Atlikt **.**
- Informācijas koda transakcijas, kas ir saistītas ar atlasīto finanšu transakciju. Lai skatītu informācijas koda darbības, **kopsavilkuma cilnē Finanšu darbības** atlasiet finanšu darbību, kuras statuss **ir Izlaists**, **Atzīmēts kā reģistrēts** vai **Atlikts**, un pēc tam atlasiet **Informācijas koda darbības**.

Atlasot opciju **Paplašinātie dati**, var skatīt arī dažus finanšu transakciju rekvizītus. Skatāmo rekvizītu saraksts ir raksturīgs finanšu reģistrācijas funkcionalitātei, kas ģenerēja finanšu transakciju. Piemēram, varat skatīt ciparparakstu, sērijas numuru, sertifikāta nospiedumu, jaucējalgoritma identifikāciju un citus finanšu transakciju rekvizītus ciparparaksta funkcionalitātei Francijā.

## <a name="fiscal-texts-for-discounts"></a>Atlaižu finanšu teksts

Dažās valstīs vai reģionos ir spēkā īpašas prasības attiecībā uz papildu tekstu, kas ir jādrukā finanšu dokumentos gadījumā, ja tiek lietotas dažāda veida atlaides. Finanšu integrācijas funkcionalitāte sniedz iespēju iestatīt atlaidei īpašu tekstu, kas tiek drukāts pēc atlaides rindas finanšu dokumentā. Manuālām atlaidēm varat konfigurēt finanšu tekstu informācijas kodam, kas POS funkcionalitātes profilā ir norādīts kā informācijas kods **Preces atlaide**. Papildinformāciju par to, kā iestatīt atlaižu finanšu tekstu, skatiet rakstā [Atlaižu finanšu teksta iestatīšana](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Finanšu X un Z pārskatu drukāšana

Finanšu integrācijas funkcionalitāte atbalsta tādu dienas beigu pārskatu ģenerēšanu, kas ir raksturīgi integrētajai finanšu ierīcei vai pakalpojumam.

- POS ekrāna izkārtojumam ir jāpievieno jaunas pogas, kas nodrošina atbilstošo operāciju izpildi. Papildinformāciju skatiet rakstā [Finanšu X/Z pārskatu iestatīšana POS sistēmā](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Finanšu integrācijas paraugā šīs operācijas ir jāsaskaņo ar atbilstošajām finanšu ierīces operācijām.

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>Finanšu integrācijas paraugi komplektā Commerce SDK

Pašlaik komplektā Commerce SDK ir pieejami tālāk norādītie finanšu integrācijas paraugi.

- [Fiskālā printera integrācijas piemērs Itālijai](./emea-ita-fpi-sample.md)
- [Fiskālā printera integrācijas paraugs Polijai](./emea-pol-fpi-sample.md)
- [Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Austrijai](./emea-aut-fi-sample.md)
- [Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Čehijas Republikai](./emea-cze-fi-sample.md)
- [Vadības ierīces integrācijas paraugs izmantošanai Zviedrijā](./emea-swe-fi-sample.md)
- [Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Vācijai](./emea-deu-fi-sample.md)
- [Fiskālā printera integrācijas paraugs Krievijai](./rus-fpi-sample.md)

Tālāk norādītā finanšu integrācijas funkcionalitāte arī tiek ieviesta, izmantojot finanšu integrācijas struktūru, taču tā ir pieejama darbgatava un nav iekļauta komplektā Commerce SDK.

- [Finanšu reģistrācija Brazīlijai](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Ciparparaksts izmantošanai Francijā](./emea-fra-cash-registers.md)

Komplektā Commerce SDK ir pieejama arī tālāk norādītā fiskālās integrācijas funkcionalitāte, taču pašlaik tai netiek izmantota finanšu integrācijas struktūra. Nākamajos atjauninājumos ir plānota šīs funkcionalitātes migrēšana uz finanšu integrācijas struktūru.

- [Ciparparaksts izmantošanai Norvēģijā](./emea-nor-cash-registers.md)

Šāda mantotās fiskālās integrācijas funkcionalitāte, kas ir pieejama komplektā Commerce SDK, neizmanto finanšu integrācijas struktūru un līdz ar vēlākiem atjauninājumiem būs novecojusi.

- [Vadības ierīces integrācijas paraugs izmantošanai Zviedrijā (mantots)](./retail-sdk-control-unit-sample.md)
- [Ciparparaksts izmantošanai Francijā (mantots)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
