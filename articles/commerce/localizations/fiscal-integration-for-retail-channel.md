---
title: Finanšu integrācijas apskats Commerce kanāliem
description: Šajā rakstā sniegts pārskats par finanšu integrācijas iespējām, kas ir pieejamas Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 0a56df2a463153c6c3986ce84907e25ea7d965b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286504"
---
# <a name="fiscal-integration-overview-for-commerce-channels"></a>Finanšu integrācijas apskats Commerce kanāliem

[!include [banner](../includes/banner.md)]

Šis raksts ir pārskats par finanšu integrācijas iespējām, kas ir pieejamas Dynamics 365 Commerce. 

Finanšu integrācija ietver integrāciju ar dažādām finanšu ierīcēm un pakalpojumiem, kas nodrošina tirdzniecības pārdošanas darbību finanšu reģistrāciju saskaņā ar vietējiem likumiem par nodokļiem, kuru mērķis ir novērst ar nodokļiem saistītu krāpniecību mazumtirdzniecības nozarē. Tālāk ir norādīti daži tipiski scenāriji, kuros var izmantot finanšu integrāciju.

- Reģistrējiet tirdzniecības pārdošanas darbību finanšu ierīcē, kas ir savienota ar programmu Point of Sale (POS), piemēram fiskālo printeri, un izdrukājiet debitoram paredzētu finanšu dokumentu.
- Drošā veidā iesniedziet ar programmā Retail POS veiktajām pārdošanas un atgriešanas darbībām saistīto informāciju ārējā tīmekļa pakalpojumā, kura darbību nodrošina nodokļu iestāde.
- Palīdziet nodrošināt pārdošanas darbību datu nedatību, izmantojot ciparparakstus.

Finanšu integrācijas funkcionalitāte ir struktūra, kas nodrošina kopēju risinājumu tālākai programmas Retail POS un finanšu ierīču un pakalpojumu integrācijas izstrādei un pielāgošanai. Funkcionalitātē ir ietverti arī finanšu integrācijas paraugi, kas atbalsta pamata scenārijus noteiktās valstīs vai reģionos un darbojas ar noteiktām finanšu ierīcēm vai pakalpojumiem. Finanšu integrācijas paraugu veido vairāki programmas Commerce komponentu paplašinājumi, un tas ir iekļauts programmatūras izstrādes komplektā (SDK). Plašāku informāciju par finanšu integrācijas paraugiem skatiet tēmā [Finanšu integrācijas paraugi programmā Commerce SDK](#fiscal-integration-samples-in-the-commerce-sdk). Papildinformāciju par to, kā instalēt un izmantot komplektu Commerce SDK, skatiet rakstā [Retail programmatūras izstrādes komplekta (SDK) arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Lai nodrošinātu tādu scenāriju atbalstu, kurus neatbalstīta finanšu integrācijas paraugs, integrētu programmu Retail POS ar citām finanšu ierīcēm vai pakalpojumiem, vai izpildītu citās valstīs vai reģionos spēkā esošās prasības, ir jāpaplašina kāds no esošajiem finanšu integrācijas paraugiem vai jāizveido jauns paraugs, kā piemēru izmantojot esošu paraugu.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Finanšu reģistrācijas procesa un finanšu integrācijas paraugi finanšu ierīcēm un pakalpojumiem

Finanšu reģistrācijas process programmā Retail POS var sastāvēt no vienas vai vairākām darbībām. Katra darbība ietver noteiktu transakciju vai notikumu finanšu reģistrāciju vienā finanšu ierīcē vai pakalpojumā. Finanšu ierīcē vai pakalpojumā finanšu reģistrācijā piedalās šādi risinājuma komponenti:

- **Fiskālā dokumenta nodrošinātājs** - šis komponents serializē darbību/notikumu datus formātā, kas tiek lietots arī mijiedarbībai ar fiskālo ierīci vai pakalpojumu, parsē atbildes no fiskālās ierīces vai pakalpojuma un saglabā atbildes kanāla datu bāzē. Šis paplašinājums nosaka arī konkrētās transakcijas un notikumus, kas ir jāreģistrē.
- **Finanšu savienotājs** - šis komponents inicializē sakarus ar fiskālo ierīci vai pakalpojumu, nosūta pieprasījumus vai tiešas komandas uz fiskālo ierīci vai pakalpojumu, pamatojoties uz darbību/notikumu datiem, kas ir izvilkti no finanšu dokumenta, un saņem atbildes no finanšu ierīces vai pakalpojuma

Finanšu integrācijas paraugs var ietvert Commerce Runtime (CRT), aparatūras staciju un POS paplašinājumus finanšu dokumentu nodrošinātājam un finanšu savienotājam. Tajā ir ietvertas arī tālāk norādītās komponentu konfigurācijas.

- **Finanšu dokumentu nodrošinātāja konfigurācija** — šajā konfigurācijā ir definēta izvades metodi un finanšu dokumentu formāts. Tajā ir iekļauta arī nodokļu un maksājumu metožu datu kartēšana, lai dati no Sistēmas Retail POS būtu savietojami ar vērtībām, kas ir iepriekš definētas finanšu ierīcē vai pakalpojumu budžetā.
- **Fiskālā savienotāja** konfigurācija – šī konfigurācija nosaka fiziskos sakarus ar konkrētu fiskālo ierīci vai pakalpojumu.

Noteiktas POS kases sistēmas finanšu reģistrācijas process tiek definēts, izmantojot atbilstošo iestatījumu POS funkcionalitātes profilā. Papildinformāciju par to, kā konfigurēt finanšu reģistrācijas procesu, augšupielādēt finanšu dokumentu nodrošinātāju un finanšu savienotāja konfigurācijas, kā arī mainīt konfigurācijas parametrus, [skatiet finanšu reģistrācijas procesa iestatīšana](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

> [!NOTE]
> Ja jums ir nepieciešamas ierīces operācijām, kas nav finanšu operācijas, piemēram, preču kataloga meklēšana, debitoru uzmeklēšana vai darbību melnraksta izveide, varat atlasīt tās kā reģistrus ar finanšu procesa ierobežojumiem. Papildinformāciju skatiet sadaļā [Fiskālo reģistrācijas ierobežojumu reģistru iestatīšana](setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions).

Šāda tipiska finanšu reģistrācijas plūsma sākas ar notikumu POS (piemēram, pārdošanas darbības slēgšana) un ievieš iepriekš definētu darbību secību, kas ietver citus Commerce komponentus (CRT piemēram, aparatūras staciju).

1. POS pieprasa fiskālo dokumentu no fiskālās integrācijas struktūras (FIF).
1. FIF nosaka, vai pašreizējam notikumam nepieciešama finanšu reģistrācija.
1. Pamatojoties uz fiskālās reģistrācijas procesa iestatījumiem, FIF identificē finanšu savienotāju un atbilstošu finanšu dokumentu nodrošinātāju, ko izmantot finanšu reģistrācijai.
1. FIF darbina finanšu dokumentu nodrošinātāju, kas ģenerē finanšu dokumentu (piemēram, XML dokumentu), kas pārstāv darbību vai notikumu.
1. FIF atgriež ģenerēto finanšu dokumentu POS.
1. POS pieprasa, lai FIF iesniegtu finanšu dokumentu finanšu ierīcei vai pakalpojumam.
1. FIF darbina finanšu savienotāju, kas apstrādā finanšu dokumentu un iesniedz to finanšu ierīcē vai pakalpojumā.
1. FIF atgriež pos finanšu atbildi (t.i., finanšu ierīces vai pakalpojuma atbildi).
1. POS analizē finanšu atbildi, lai noteiktu, vai finanšu reģistrācija bija veiksmīga. Pos pieprasa, lai FIF apstrādātu visas radušās kļūdas. 
1. POS pieprasa FIF procesu un saglabāt finanšu atbildi.
1. Finanšu dokumenta nodrošinātājs apstrādā finanšu atbildi. Kā daļa no šīs apstrādes finanšu dokumenta nodrošinātājs parsē atbildi un izgūst tai paplašinātos datus.
1. FIF saglabā atbildi un paplašinātos datus kanāla datu bāzē.
1. Ja nepieciešams, POS drukā kvīti, izmantojot regulāru kvīšu printeri, kas ir savienots ar aparatūras staciju. Kvītī var būt iekļauti nepieciešamie dati no finanšu atbildes.
 
Tālākajos piemēros ir parādītas fiskālo reģistrāciju izpildes plūsmas tipiskām finanšu ierīcēm vai pakalpojumiem.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Fiskālā reģistrācija tiek veikta, izmantojot aparatūras stacijai pievienoto ierīci

Šī konfigurācija tiek izmantota, kad aparatūras stacijai tiek pievienota fiziska finanšu ierīce, piemēram, fiskālais printeris. Šo programmu var lietot arī gadījumā, ja komunikācija ar fiskālo ierīci vai pakalpojumu tiek veikta, izmantojot aparatūras stacijā instalēto programmatūru. Šajā gadījumā finanšu dokumenta nodrošinātājs ir novietots aparatūras CRT stacijā, un finanšu savienotājs ir izvietots aparatūras stacijā.

![Fiskālā reģistrācija tiek veikta, izmantojot aparatūras stacijai pievienoto ierīci.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Finanšu reģistrācija tiek veikta, izmantojot ārēju pakalpojumu

Šo konfigurāciju izmanto, ja fiskālo reģistrāciju veic ārējs pakalpojums, piemēram, Web pakalpojums, ko nodrošina nodokļu iestāde. Šajā gadījumā uz atrodas gan fiskālā dokumenta nodrošinātājs, gan finanšu savienotājs CRT.

![Finanšu reģistrācija veikta, izmantojot ārēju pakalpojumu.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Finanšu reģistrācija tiek veikta iekšēji CRT

Šo konfigurāciju izmanto, kad fiskālajai reģistrācijai nav nepieciešama neviena ārējā finanšu ierīce vai pakalpojums. Piemēram, to izmanto, ja fiskālā reģistrācija tiek veikta, izmantojot pārdošanas darbību ciparparakstu. Šajā gadījumā uz atrodas gan fiskālā dokumenta nodrošinātājs, gan finanšu savienotājs CRT.

![Finanšu reģistrācija tiek veikta iekšēji iekšēji.CRT](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Fiskālā reģistrācija tiek veikta, izmantojot ierīci vai pakalpojumu lokālajā tīklā

Šī konfigurācija tiek izmantota, kad fiziska finanšu ierīce vai finanšu pakalpojums ir klātesošs veikala lokālajā tīklā un nodrošina HTTPS programmas programmēšanas interfeisu (API). Šajā gadījumā finanšu dokumenta nodrošinātājs ir novietots CRT sistēmā POS, un finanšu savienotājs ir izvietots POS.

![Fiskālā reģistrācija tiek veikta, izmantojot ierīci vai pakalpojumu lokālajā tīklā.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Kļūdu apstrāde

Finanšu integrācijas struktūra nodrošina tālāk norādītās opcijas kļūmju apstrādei finanšu reģistrācijas laikā.

- **Mēģināt vēlreiz** — operatori var izmantot šo opciju gadījumā, ja kļūmi var ātri novērst un var atkārtoti izpildīt finanšu reģistrāciju. Piemēram, šo opciju var izmantot gadījumā, ja finanšu ierīce nav pievienota vai fiskālajā printerī ir beidzies vai iesprūdis papīrs.
- **Atcelt** — šī opcija sniedz operatoriem iespēju atlikt pašreizējās transakcijas vai notikuma finanšu reģistrāciju, ja tā neizdodas. Pēc reģistrācijas atlikšanas operators var turpināt strādāt ar POS sistēmu un veikt jebkuru operāciju, kam nav nepieciešama finanšu reģistrācija. Kad POS sistēmā notiek notikums, kam ir nepieciešama finanšu reģistrācija (piemēram, tiek atvērta jauna transakcija), tiek automātiski parādīts kļūdu apstrādes dialoglodziņš, kurā operatoram tiek paziņots, ka iepriekšējā transakcija netika pareizi reģistrēta, un tiek norādītas kļūdu apstrādes iespējas.
- **Izlaist** — operatori var izmantot šo opciju gadījumā, ja finanšu reģistrāciju var izlaist noteiktos apstākļos un POS sistēmā var turpināt veikt parastās operācijas. Piemēram, šo opciju var izmantot gadījumā, ja pārdošanas transakciju, kuras finanšu reģistrācija neizdevās, var reģistrēt īpašā papīra žurnālā.
- **Atzīmēt kā reģistrētu** — operatori var izmantot šo opciju gadījumā, ja transakcija ir reģistrēta finanšu ierīcē (piemēram, ir izdrukāts finanšu dokuments), taču, saglabājot finanšu atbildi kanāla datu bāzē, ir radusies kļūme.
- **Atlikšana** – operatori var izmantot šo opciju, ja darbība netika reģistrēta, jo reģistrācijas pakalpojums nebija pieejams. 

> [!NOTE]
> Finanšu **reģistrācijas** **procesā opcijas Izlaist**, Iezīmēt **kā** reģistrētas un Atlikt ir jāaktivizē pirms to lietošanas. Turklāt operatoriem ir jāpiešķir atbilstošās atļaujas.

Opcijas **Izlaist**, **Atzīmēt kā** **reģistrētas** un Atlikt iespējojiet informācijas kodus, lai iegūtu noteiktu informāciju par kļūmi, piemēram, kļūmes iemeslu vai pamatojumu finanšu reģistrācijas izlaišanai vai darbības atzīmēšanai kā reģistrētam. Papildinformāciju par to, kā iestatīt kļūdu apstrādes parametrus, skatiet rakstā [Kļūdu apstrādes iestatījumu veikšana](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Neobligāta finanšu reģistrācija

Finanšu reģistrācija var būt obligāta dažām operācijām, bet neobligāta citām. Piemēram, regulāras pārdošanas un atgriešanas finanšu reģistrācija var būt obligāta, bet ar klienta iemaksām saistītu operāciju finanšu reģistrācija var būt neobligāta. Šajā gadījumā finanšu reģistrācijas neveikšana pārdošanas darījumam bloķē turpmāku pārdošanu, bet finanšu reģistrācijas neveikšana attiecībā uz klienta iemaksu nebloķē turpmāku pārdošanu. Lai nodalītu obligātas un neobligātas operācijas, ieteicams tās apstrādāt, izmantojot dažādus dokumentu nodrošinātājus un iestatīt atsevišķus soļus finanšu reģistrācijas procesā šiem nodrošinātājiem. Parametram **Kļūdas gadījumā turpināt** ir jābūt iespējotam visiem soļiem, kas saistīti ar papildu finanšu reģistrāciju. Papildinformāciju par to, kā iestatīt kļūdu apstrādes parametrus, skatiet rakstā [Kļūdu apstrādes iestatījumu veikšana](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Manuāli atkārtoti izpildīt finanšu reģistrāciju

Ja darījuma vai notikuma finanšu reģistrācija ir atlikta pēc kļūmes (piemēram, ja operators atlasīja **Atcelt** kļūdu apstrādes dialoglodziņā), varat manuāli atkārtoti izpildīt finanšu reģistrāciju, izsaucot atbilstošu operāciju. Papildinformāciju skatiet tēmā [Atliktas finanšu reģistrācijas manuālas izpildes iespējošana](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="postpone-option"></a>Atlikt opciju

Atlikusī **opcija** ļauj jums turpināt finanšu reģistrācijas procesu, ja pašreizējā darbība neizdodas. To var izmantot, kad pastāv fiskālās reģistrācijas dublējuma opcija.

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
> Veselības pārbaude tiek veikta tikai tad, **ja** pašreizējai darbībai nepieciešama fiskālā reģistrācija un ja parametrs Turpināt kļūdu ir atspējots pašreizējam fiskālās reģistrācijas procesa solim. Plašāku informāciju skatiet tēmā [Kļūdu apstrādes iestatījumu veikšana](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Finanšu atbildes saglabāšana finanšu transakcijā

Ja transakcijas vai notikuma finanšu reģistrācija ir veiksmīga, kanāla datu bāzē tiek izveidota finanšu transakcija, kas tiek saistīta ar sākotnējo transakciju vai notikumu. Līdzīgi gadījumā, ja neveiksmīgai finanšu reģistrācijai tiek atlasīta opcija **izlaist** vai **Atzīmēt kā reģistrētu**, šī informācija tiek saglabāta finanšu transakcijā. Finanšu transakcijā ir ietverta finanšu ierīces vai pakalpojuma finanšu atbilde. Ja finanšu reģistrācijas process sastāv no vairākām darbībām, katrai procesa darbībai, kuras rezultāts ir veiksmīga vai neveiksmīga reģistrācija, tiek izveidota finanšu transakcija.

Finanšu transakcijas kopā ar transakcijām tiek pārsūtītas uz Headquarters, izmantojot funkciju *P darbs*. Lapas **Veikalu transakcijas** kopsavilkuma cilnē **Finanšu transakcijas** varat skatīt finanšu transakcijas, kas ir saistītas ar transakcijām.

Finanšu transakcijā ir saglabāta tālāk norādītā detalizētā informācija.

- Detalizēta informācija par finanšu reģistrācijas procesu (par procesu, savienotāju grupu, savienotāju utt.). Turklāt laukā **Kases sistēmas numurs** tiek glabāts finanšu ierīces sērijas numurs, ja šī informācija ir ietverta finanšu atbildē.
- Finanšu reģistrācijas statuss: **Pabeigts veiksmīgai reģistrācijai, Izlaists,** **·** **ja operators atlasīja neveiksmīgas reģistrācijas opciju Izlaist, Atzīmēts kā reģistrēts,** **·** **ja operators atlasīja opciju Atzīmēt kā reģistrēto vai Atlikts,** **·** **ja operators atlasa Atlikts opciju.**
- Informācijas koda transakcijas, kas ir saistītas ar atlasīto finanšu transakciju. Lai skatītu informācijas koda darbības, **kopsavilkuma** cilnē Finanšu darījumi atlasiet finanšu darbību, **kuras** statuss ir Izlaists, **Atzīmēts** kā reģistrēts vai Atlikts **,** **un pēc tam atlasiet Informācijas koda darbības**.

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
