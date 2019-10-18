---
title: Apskats par mazumtirdzniecības kanālu finanšu integrāciju
description: Šajā tēmā ir sniegts apskats par finanšu integrācijas iespējām, kas ir pieejamas programmā Dynamics 365 Retail.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: 647ef586b64699a891bd3b6702ac93bc5ee8292e
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025411"
---
# <a name="overview-of-fiscal-integration-for-retail-channels"></a>Apskats par mazumtirdzniecības kanālu finanšu integrāciju

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Ievads

Šajā tēmā ir sniegts apskats par finanšu integrācijas iespējām, kas ir pieejamas programmā Dynamics 365 Retail. Finanšu integrācija ietver integrāciju ar dažādām finanšu ierīcēm un pakalpojumiem, kas nodrošina mazumtirdzniecības pārdošanas darbību finanšu reģistrāciju saskaņā ar vietējiem likumiem par nodokļiem, kuru mērķis ir novērst ar nodokļiem saistītu krāpniecību mazumtirdzniecības nozarē. Tālāk ir norādīti daži tipiski scenāriji, kuros var izmantot finanšu integrāciju.

- Reģistrējiet mazumtirdzniecības pārdošanas darbību finanšu ierīcē, kas ir savienota ar programmu Retail Point of Sale (POS), piemēram fiskālo printeri, un izdrukājiet debitoram paredzētu finanšu dokumentu.
- Drošā veidā iesniedziet ar programmā Retail POS veiktajām pārdošanas un atgriešanas darbībām saistīto informāciju ārējā tīmekļa pakalpojumā, kura darbību nodrošina nodokļu iestāde.
- Palīdziet nodrošināt pārdošanas transakciju datu nemaināmību, izmantojot ciparparakstus.

Finanšu integrācijas funkcionalitāte ir struktūra, kas nodrošina kopēju risinājumu tālākai programmas Retail POS un finanšu ierīču un pakalpojumu integrācijas izstrādei un pielāgošanai. Funkcionalitātē ir ietverti arī finanšu integrācijas paraugi, kas atbalsta pamata mazumtirdzniecības scenārijus noteiktās valstīs vai reģionos un darbojas ar noteiktām finanšu ierīcēm vai pakalpojumiem. Finanšu integrācijas paraugs sastāv no vairākiem programmas Retail komponentu paplašinājumiem un ir iekļauts programmatūras izstrādes komplektā (SDK). Plašāku informāciju par finanšu integrācijas paraugiem skatiet tēmā [Finanšu integrācijas paraugi programmā Retail SDK](#fiscal-integration-samples-in-the-retail-sdk). Papildinformāciju par to, kā instalēt un izmantot komplektu Retail SDK, skatiet rakstā [Retail SDK apskats](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Lai nodrošinātu tādu scenāriju atbalstu, kurus neatbalstīta finanšu integrācijas paraugs, integrētu programmu Retail POS ar citām finanšu ierīcēm vai pakalpojumiem, vai izpildītu citās valstīs vai reģionos spēkā esošās prasības, ir jāpaplašina kāds no esošajiem finanšu integrācijas paraugiem vai jāizveido jauns paraugs, kā piemēru izmantojot esošu paraugu.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>Finanšu reģistrācijas process un finanšu integrācijas paraugi finanšu ierīcēm

Finanšu reģistrācijas process programmā Retail POS var sastāvēt no vienas vai vairākām darbībām. Katra darbība ietver noteiktu mazumtirdzniecības transakciju vai notikumu finanšu reģistrāciju vienā finanšu ierīcē vai pakalpojumā. Finanšu reģistrācijai finanšu ierīcē, kas ir savienota ar aparatūras staciju, tiek izmantoti tālāk norādītie risinājuma komponenti.

- **Commerce runtime (CRT) paplašinājums** — šis komponents nodrošina mazumtirdzniecības transakcijas/notikuma datu serializēšanu formātā, kas tiek izmantots arī mijiedarbībai ar finanšu ierīci, no finanšu ierīces saņemto atbilžu parsēšanu un atbilžu saglabāšanu kanāla datu bāzē. Šis paplašinājums nosaka arī konkrētās transakcijas un notikumus, kas ir jāreģistrē. Šis komponents bieži tiek saukts par *finanšu dokumentu nodrošinātāju*.
- **Aparatūras stacija paplašinājums** — šis komponents nodrošina saziņas ar finanšu ierīci inicializāciju, pieprasījumu un tiešu komandu sūtīšanu uz finanšu ierīci, pamatojoties uz mazumtirdzniecības transakcijas/notikuma datiem, kas ir izgūti no finanšu dokumenta, un atbilžu saņemšanu no finanšu ierīces. Šis komponents bieži tiek saukts par *finanšu savienotāju*.

Finanšu ierīces finanšu integrācijas paraugā ir ietverti CRT un aparatūras stacijas paplašinājumi attiecīgi finanšu dokumentu nodrošinātājam un finanšu savienotājam. Tajā ir ietvertas arī tālāk norādītās komponentu konfigurācijas.

- **Finanšu dokumentu nodrošinātāja konfigurācija** — šajā konfigurācijā ir definēta izvades metodi un finanšu dokumentu formāts. Tajā ir ietverta arī nodokļus un maksājuma metožu datu kartēšana, lai padarītu no programmas Retail POS saņemtos datus saderīgus ar finanšu ierīces programmaparatūrā iepriekš definētajām vērtībām.
- **Finanšu savienotāja konfigurācija** — šajā konfigurācijā ir definēta fiziskā saziņa ar konkrēto finanšu ierīci.

Noteiktas POS kases sistēmas finanšu reģistrācijas process tiek definēts, izmantojot atbilstošo iestatījumu POS funkcionalitātes profilā. Papildinformāciju par to, kā konfigurēt finanšu reģistrācijas procesu, augšupielādēt finanšu dokumentu nodrošinātāju un finanšu savienotāju konfigurācijas un mainīt to parametrus, redzēt rakstā [Finanšu reģistrācijas procesa iestatīšana](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Tālāk sniegtajā piemērā ir aprakstīta tipiska finanšu reģistrācijas izpildes plūsma finanšu ierīcei. Plūsma sākas ar notikumu POS sistēmā (piemēram, pārdošanas transakcijas pabeigšanu), un tajā ir ietverta tālāk norādītā darbību secība.

1. POS sistēma pieprasa finanšu dokumentu no programmas CRT.
2. CRT nosaka, vai pašreizējam notikumam ir nepieciešama finanšu reģistrācija.
3. Pamatojoties uz finanšu reģistrācijas procesa iestatījumiem, programma CRT nosaka finanšu savienotāju un atbilstošo finanšu dokumentu nodrošinātāju, kas ir jāizmanto finanšu reģistrācijai.
4. CRT izpilda finanšu dokumentu nodrošinātāju, kas ģenerē finanšu dokumentu (piemēram, XML formāta dokumentu), kurš atbilst mazumtirdzniecības transakcijai vai notikumam.
5. POS sistēma nosūta programmas CRT sagatavoto finanšu dokumentu uz aparatūras staciju.
6. Aparatūras stacija izpilda finanšu savienotāju, kas apstrādā finanšu dokumentu un pārsūta to uz finanšu ierīci vai pakalpojumu.
7. POS sistēma analizē no finanšu ierīces vai pakalpojuma saņemto atbildi, lai noteiktu, vai finanšu reģistrācija ir bijusi veiksmīga.
8. CRT saglabā atbildi kanāla datu bāzē.

![Risinājuma shēma](media/emea-fiscal-integration-solution.png "Risinājuma shēma")

## <a name="error-handling"></a>Kļūdu apstrāde

Finanšu integrācijas struktūra nodrošina tālāk norādītās opcijas kļūmju apstrādei finanšu reģistrācijas laikā.

- **Mēģināt vēlreiz** — operatori var izmantot šo opciju gadījumā, ja kļūmi var ātri novērst un var atkārtoti izpildīt finanšu reģistrāciju. Piemēram, šo opciju var izmantot gadījumā, ja finanšu ierīce nav pievienota vai fiskālajā printerī ir beidzies vai iesprūdis papīrs.
- **Atcelt** — šī opcija sniedz operatoriem iespēju atlikt pašreizējās transakcijas vai notikuma finanšu reģistrāciju, ja tā neizdodas. Pēc reģistrācijas atlikšanas operators var turpināt strādāt ar POS sistēmu un veikt jebkuru operāciju, kam nav nepieciešama finanšu reģistrācija. Kad POS sistēmā notiek notikums, kam ir nepieciešama finanšu reģistrācija (piemēram, tiek atvērta jauna transakcija), tiek automātiski parādīts kļūdu apstrādes dialoglodziņš, kurā operatoram tiek paziņots, ka iepriekšējā transakcija netika pareizi reģistrēta, un tiek norādītas kļūdu apstrādes iespējas.
- **Izlaist** — operatori var izmantot šo opciju gadījumā, ja finanšu reģistrāciju var izlaist noteiktos apstākļos un POS sistēmā var turpināt veikt parastās operācijas. Piemēram, šo opciju var izmantot gadījumā, ja pārdošanas transakciju, kuras finanšu reģistrācija neizdevās, var reģistrēt īpašā papīra žurnālā.
- **Atzīmēt kā reģistrētu** — operatori var izmantot šo opciju gadījumā, ja transakcija ir reģistrēta finanšu ierīcē (piemēram, ir izdrukāts finanšu dokuments), taču, saglabājot finanšu atbildi kanāla datu bāzē, ir radusies kļūme.

> [!NOTE]
> Opcijas **Izlaist** un **Atzīmēt kā reģistrētu** pirms lietošanas ir jāaktivizē finanšu reģistrācijas procesa ietvaros. Turklāt operatoriem ir jāpiešķir atbilstošās atļaujas.

Izmantojot opcijas **Izlaist** un **Atzīmēt kā reģistrētu**, tiek iespējoti informācijas kodi, lai reģistrētu noteiktu informāciju par kļūmi, piemēram, kļūmes iemeslu vai pamatojumu finanšu reģistrācijai vai transakcijas reģistrācijas atzīmēšanai. Papildinformāciju par to, kā iestatīt kļūdu apstrādes parametrus, skatiet rakstā [Kļūdu apstrādes iestatījumu veikšana](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Neobligāta finanšu reģistrācija

Finanšu reģistrācija var būt obligāta dažām operācijām, bet neobligāta citām. Piemēram, regulāras pārdošanas un atgriešanas finanšu reģistrācija var būt obligāta, bet ar klienta iemaksām saistītu operāciju finanšu reģistrācija var būt neobligāta. Šajā gadījumā finanšu reģistrācijas neveikšana pārdošanas darījumam bloķē turpmāku pārdošanu, bet finanšu reģistrācijas neveikšana attiecībā uz klienta iemaksu nebloķē turpmāku pārdošanu. Lai nodalītu obligātas un neobligātas operācijas, ieteicams tās apstrādāt, izmantojot dažādus dokumentu nodrošinātājus un iestatīt atsevišķus soļus finanšu reģistrācijas procesā šiem nodrošinātājiem. Parametram **Kļūdas gadījumā turpināt** ir jābūt iespējotam visiem soļiem, kas saistīti ar papildu finanšu reģistrāciju. Papildinformāciju par to, kā iestatīt kļūdu apstrādes parametrus, skatiet rakstā [Kļūdu apstrādes iestatījumu veikšana](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-running-fiscal-registration"></a>Manuāla finanšu reģistrācijas izpilde

Ja darījuma vai notikuma finanšu reģistrācija ir atlikta pēc kļūmes (piemēram, ja operators atlasīja **Atcelt** kļūdu apstrādes dialoglodziņā), varat manuāli atkārtoti izpildīt finanšu reģistrāciju, izsaucot atbilstošu operāciju. Papildinformāciju skatiet tēmā [Atliktas finanšu reģistrācijas manuālas izpildes iespējošana](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="fiscal-registration-health-check"></a>Finanšu reģistrācijas darbspējas pārbaude

Finanšu reģistrācijas darbspējas pārbaudes procedūra pārbauda finanšu ierīces vai pakalpojuma pieejamību noteiktu notikumu gadījumā. Ja pašlaik nevar izpildīt finanšu reģistrāciju, operators saņem iepriekšēju paziņojumu.

POS veic darbspējas pārbaudi šādu notikumu gadījumā:

- Tiek atvērts jauns darījums.
- Tiek veikta aizturēta darījuma atsaukšana.
- Tiek pabeigts pārdošanas vai atgriešanas darījums.

Ja darbspējas pārbaude neizdodas, POS rāda darbspējas pārbaudes dialoglodziņu. Minētajā dialoglodziņā ir pieejamas šādas pogas:

- **Labi** — šī poga ļauj operatoram ignorēt darbspējas pārbaudes kļūdu un turpināt, lai apstrādātu darījumu. Operatori var atlasīt šo pogu tikai tad, ja tiem ir iespējota atļauja **Atļaut izlaist darbspējas pārbaudes kļūdu**.
- **Atcelt** — ja operators izvēlas šo pogu, POS atceļ pēdējo darbību (piemēram, krājums nav pievienots jaunam darījumam).

> [!NOTE]
> Darbspējas pārbaude tiek izpildīta tikai tad, ja pašreizējai operācijai obligāti jāveic finanšu reģistrācija un ja parametrs **Kļūdas gadījumā turpināt** ir atspējots pašreizējam finanšu reģistrācijas procesa solim. Plašāku informāciju skatiet tēmā [Kļūdu apstrādes iestatījumu veikšana](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Finanšu atbildes saglabāšana finanšu transakcijā

Ja transakcijas vai notikuma finanšu reģistrācija ir veiksmīga, kanāla datu bāzē tiek izveidota finanšu transakcija, kas tiek saistīta ar sākotnējo transakciju vai notikumu. Līdzīgi gadījumā, ja neveiksmīgai finanšu reģistrācijai tiek atlasīta opcija **izlaist** vai **Atzīmēt kā reģistrētu**, šī informācija tiek saglabāta finanšu transakcijā. Finanšu transakcijā ir ietverta finanšu ierīces vai pakalpojuma finanšu atbilde. Ja finanšu reģistrācijas process sastāv no vairākām darbībām, katrai procesa darbībai, kuras rezultāts ir veiksmīga vai neveiksmīga reģistrācija, tiek izveidota finanšu transakcija.

Finanšu darījumi tiek pārsūtīti uz moduli Retail Headquarters kopā ar mazumtirdzniecības darījumiem, izmantojot funkciju *P darbs*. Lapas **Mazumtirdzniecības veikala transakcijas** kopsavilkuma cilnē **Finanšu transakcijas** varat skatīt finanšu transakcijas, kas ir saistītas ar mazumtirdzniecības transakcijām.

Finanšu transakcijā ir saglabāta tālāk norādītā detalizētā informācija.

- Detalizēta informācija par finanšu reģistrācijas procesu (par procesu, savienotāju grupu, savienotāju utt.). Turklāt laukā **Kases sistēmas numurs** tiek glabāts finanšu ierīces sērijas numurs, ja šī informācija ir ietverta finanšu atbildē.
- Finanšu reģistrācijas statuss: **Pabeigta**, ja reģistrācija ir bijusi veiksmīga; **Izlaista**, ja operators neveiksmīgai reģistrācijai ir atlasījis opciju **Izlaist**; vai **Atzīmēta kā reģistrēta**, ja operators ir atlasījis opciju **Atzīmēt kā reģistrētu**.
- Informācijas koda transakcijas, kas ir saistītas ar atlasīto finanšu transakciju. Lai skatītu informācijas koda transakcijas, kopsavilkuma cilnē **Finanšu transakcijas** atlasiet finanšu transakciju, kuras statuss ir **Izlaista** vai **Atzīmēta kā reģistrēta**, un pēc tam atlasiet vienumu **Informācijas koda transakcijas**.

## <a name="fiscal-texts-for-discounts"></a>Atlaižu finanšu teksts

Dažās valstīs vai reģionos ir spēkā īpašas prasības attiecībā uz papildu tekstu, kas ir jādrukā finanšu dokumentos gadījumā, ja tiek lietotas dažāda veida atlaides. Finanšu integrācijas funkcionalitāte sniedz iespēju iestatīt atlaidei īpašu tekstu, kas tiek drukāts pēc atlaides rindas finanšu dokumentā. Manuālām atlaidēm varat konfigurēt finanšu tekstu informācijas kodam, kas POS funkcionalitātes profilā ir norādīts kā informācijas kods **Preces atlaide**. Papildinformāciju par to, kā iestatīt atlaižu finanšu tekstu, skatiet rakstā [Atlaižu finanšu teksta iestatīšana](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Finanšu X un Z pārskatu drukāšana

Finanšu integrācijas funkcionalitāte atbalsta tādu dienas beigu pārskatu ģenerēšanu, kas ir raksturīgi integrētajai finanšu ierīcei vai pakalpojumam.

- POS ekrāna izkārtojumam ir jāpievieno jaunas pogas, kas nodrošina atbilstošo operāciju izpildi. Papildinformāciju skatiet rakstā [Finanšu X/Z pārskatu iestatīšana POS sistēmā](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Finanšu integrācijas paraugā šīs operācijas ir jāsaskaņo ar atbilstošajām finanšu ierīces operācijām.

## <a name="fiscal-integration-samples-in-the-retail-sdk"></a>Finanšu integrācijas paraugi komplektā Retail SDK

Pašlaik komplektā Retail SDK ir pieejami tālāk norādītie finanšu integrācijas paraugi.

- [Fiskālā printera integrācijas piemērs Itālijai](emea-ita-fpi-sample.md)
- [Fiskālā printera integrācijas piemērs Polijai](emea-pol-fpi-sample.md)
- [Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Austrijai](emea-aut-fi-sample.md)
- [Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Čehijas Republikai](emea-cze-fi-sample.md)

Komplektā Retail SDK ir pieejama arī tālāk norādītā fiskālās integrācijas funkcionalitāte, taču pašlaik tai netiek izmantota finanšu integrācijas struktūra. Nākamajos atjauninājumos ir plānota šīs funkcionalitātes migrēšana uz finanšu integrācijas struktūru.

- [Ciparparaksts izmantošanai Francijā](emea-fra-cash-registers.md)
- [Ciparparaksts izmantošanai Norvēģijā](emea-nor-cash-registers.md)
- [Vadības ierīces integrācijas paraugs izmantošanai Zviedrijā](./retail-sdk-control-unit-sample.md)
