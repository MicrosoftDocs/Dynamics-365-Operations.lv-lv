---
title: "Kreditoru pievienošana"
description: "Šajā tēmā ir aprakstīts jaunu kreditoru pievienošanas process. Tajā ir izskaidrotas darbības, kas šī procesa gaitā ir jāveic lietotājiem ar dažādām lomām."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests,SysUserRequestListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 1bd23b6e87c95d2c3d2131ec1ee9548bc4fe10cb
ms.openlocfilehash: 2816fb094504bb5d0b595f812764620d480da401
ms.contentlocale: lv-lv
ms.lasthandoff: 03/04/2018

---

# <a name="onboard-vendors"></a>Kreditoru pievienošana
[!include[banner](../includes/banner.md)]
---

Jaunus kreditorus var pievienot un reģistrēt kā kreditorus programmatūrā Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, pamatojoties uz informāciju, ko ieguvāt no personas, kura šo kreditoru pārstāv.

Šis process sastāv no tālāk aprakstītajām darbībām, kuras sistēmā veic lietotāji ar dažādām lomām.

1. **Datu pārvaldība OData** — elementa importēšana — sākotnējais pieprasījums ir potenciālā piegādātāja reģistrācijas pieprasījums. Parasti šis pieprasījums nāk no kāda avota, piemēram, no debitora viesotas vietnes, kas pieļauj anonīmu piekļuvi. Kreditori var reģistrēties, norādot pamatinformāciju, piemēram, kreditora nosaukumu, pamatojumu, organizācijas numuru un kontaktpersonas vārdu un e-pasta adresi. Šie pieprasījumi tiek importēti, izmantojot datu pārvaldības interfeisu.
2. **Potenciālo piegādātāju reģistrācijas pieprasījumu saraksta lapa** — pamatojoties uz potenciālā piegādātāja reģistrācijas pieprasījumā sniegto informāciju, sagādes speciālists izlemj, vai šis kreditors ir jāpievieno. Sagādes speciālists apskata ienākošo pieprasījumu programmas Finance and Operations saraksta lapā **Potenciālo piegādātāju reģistrācijas pieprasījumi**.
3. **Lietotāja nodrošināšanas darbplūsma** — kad sagādes speciālists ir pārbaudījis ienākošajā pieprasījumā norādīto informāciju un ir izlēmis turpināt pievienošanas procesu, lietotāja pieprasījuma darbplūsma nodrošina jauno lietotāju un nosūta uzaicinājuma e-pasta ziņojumu, lai šo kontaktpersonu pieņemtu kā autentificētu Microsoft Dynamics 365 lietotāju.
4. **Kreditora reģistrācijas vednis** — piegādātāja kontaktpersonas pierakstās programmā Finance and Operations, izmantojot jauno lietotāja kontu. Šī kontaktpersona izpilda kreditora reģistrācijas vedņa norādījumus, lai sniegtu tādu informāciju kā, piemēram, adreses, biznesa informācija, sagādes kategorijas un atbildes uz aptaujas jautājumiem.
5. **Apstiprinājuma darbplūsma** — tiek izveidots piegādātāja pieprasījums, kurā ir šī reģistrācijas informācija. Šis piegādātāja pieprasījums tiek iesniegts darbplūsmā un tiek novirzīts pārskatīšanai un apstiprināšanai.
6. **Kreditora pamatdatu izveidošana un lietotāja lomas modificēšana** — kad piegādātāja pieprasījums ir apstiprināts, tiek izveidots kreditora ieraksts. Kreditora kontaktpersonas lietotāja kontam tiek piešķirtas tiesības uz kreditoru sadarbību, vai šis konts tiek deaktivizēts.

Nākamajā tabulā ir parādītas šajā procesā iesaistītās darbības un lomas.

| Loma un “process”       | Datu pārvaldība OData — elementa importēšana | Potenciālo piegādātāju reģistrācijas pieprasījumu saraksta lapa | Lietotāja nodrošināšanas darbplūsma | Kreditora reģistrācijas vednis | Apstiprinājuma darbplūsma | Kreditora pamatdatu izveidošana un lietotāja lomas modificēšana |
|--------------------------|---|---|---|---|---|---|
| Sistēma                   | Jauna piegādātāja pieprasījums tiek importēts. | | | | | Pēc piegādātāja pieprasījuma pieņemšanas tiek izveidots kreditora ieraksts. |
| Sagādes speciālists | | Sākt pievienošanas procesu. | | | Pārskatīt un pieņemt vai noraidīt piegādātāja pieprasījumu. | |
| Administrators            | | | Izveidot lietotāju programmā Finance and Operations un Microsoft Azure. | | | |
| Kreditora kontaktpersona    | | | Sūtīt e-pasta ziņojumu kontaktpersonai. | Reģistrēt kreditora informāciju. | | |

Īsu kreditoru pievienošanas procesa demonstrāciju varat skatīties šajā īsaja YouTube video: 
> [!Video https://www.youtube.com/embed/0KUc3AGaTKk]

## <a name="importing-the-prospective-vendor-registration-request"></a>Potenciālā piegādātāja reģistrācijas pieprasījuma importēšana

Potenciālā piegādātāja reģistrācijas pieprasījums ir elements programmā Finance and Operations. Sistēmu varat iestatīt datu importēšanai, izmantojot šo elementu. 

Nākamajā tabulā ir parādīta informācija, kas ir ietverta šajā elementā un ko var importēt.

| Lauks                        | Apraksts |
|------------------------------|-------------|
| Kreditora nosaukums                  | Kreditora nosaukums. |
| Pieprasījuma pamatojums       | Piegādātāja pieprasījuma iemesls vai iemesli. |
| Organizācijas numurs          | Oficiāli zināms reģistrācijas numurs. |
| Biznesa nozare             | Biznesa nozare, kurā kreditors darbojas. |
| Kontaktpersonas vārds  | Tās personas vārds, kura tiks aicināta reģistrēt kreditora informāciju. |
| Kontakta otrais vārds | Tās personas otrais vārds, kura tiks aicināta reģistrēt kreditora informāciju. |
| Kontaktpersonas uzvārds   | Tās personas uzvārds, kura tiks aicināta reģistrēt kreditora informāciju. |
| Kontaktpersonas e-pasta adrese       | E-pasta adrese, kas tiks izmantota, lai izveidotu jaunu lietotāju programmā Finance and Operations, un kas tiks reģistrēta nomnieka Azure Active Directory (Azure AD) kontā. |
| Iesniegšanas datums               | Datums, kad pieprasījums tika izveidots ārējā sistēmā. |
| Juridiska persona                 | Juridiskā persona, kurā kreditors pieprasa kļūt par kreditoru. Šai vērtībai ir jābūt juridiskās personas kodam, kas ir reģistrēts programmā Finance and Operations. Ja importēšanas procesa gaitā nav saņemta nekāda vērtība, tiek lietota vērtība no sagādes un avotu parametriem. |
| Kreditora tips                  | Kreditors var būt organizācija vai persona. Kreditora tips nosaka veidu, kādā kreditors visbeidzot tiek izveidots. |

Kad potenciālā piegādātāja reģistrācijas pieprasījums ir importēts, tas ir redzams saraksta lapā **Potenciālā piegādātāja reģistrācijas pieprasījums**. No šīs saraksta lapas sagādes speciālists var uzaicināt šo lietotāju. Lietotāja pieprasījums pēc lietotāja pieprasīšanas tiek nosūtīts uz darbplūsmu.

## <a name="submitting-a-prospective-vendor-user-request"></a>Potenciālā piegādātāja lietotāja pieprasījuma iesniegšana

Potenciālā piegādātāja lietotāja pieprasījuma mērķis ir nodrošināt personu, kas iesniedza sākotnējo pieprasījumu, lai šī persona varētu pierakstīties sistēmā Finance and Operations, izmantojot e-pasta kontu, kas tiek nodrošināts potenciālā piegādātāja reģistrācijas pieprasījumā.

Potenciālā piegādātāja lietotāja pieprasījums tiek apstrādāts ar lietotāja pieprasījuma darbplūsmu. Šī darbplūsma sazinās, izmantojot Azure AD B2B sadarbību. Tā izveido lietotāju sistēmā Finance and Operations, kam ir atbilstošie drošības iestatījumi.

Jauniestatītajiem lietotājiem ir tālāk norādītās drošības lomas.

- Sistēmas ārējais lietotājs
- Piegādātājs potenciālais (ārējais)

Jaunais lietotājs saņems lietotāja pieprasījuma darbplūsmas ģenerētu e-pasta ziņojumu. Šis e-pasta ziņojums aicina lietotāju pierakstīties sistēmā.

Informāciju par e-pasta ziņojuma konfigurēšanu un šo darbplūsmu vispār skatiet lietotāja pieprasījuma darbplūsmas aprakstā šeit: [Kreditoru sadarbības iestatīšana un uzturēšana](set-up-maintain-vendor-collaboration.md).

## <a name="vendor-registration"></a>Piegādātāja reģistrācija

Potenciālā piegādātāja lietotājs, kurš pierakstās sistēmā Finance and Operations, redz kreditora reģistrācijas vedņa pirmo lapu, kur šis lietotājs var ievadīt piegādātāja informāciju.

Vednis atspoguļo piegādātāja pieprasījuma konfigurāciju. Vednī pieprasīto informāciju un informāciju, kas ir jānorāda obligāti, nosaka valsts vai reģions, kur kreditors veic uzņēmējdarbību.

Papildinformāciju par piegādātāja pieprasījuma konfigurāciju skatiet šeit: [Kreditoru sadarbības iestatīšana un uzturēšana](set-up-maintain-vendor-collaboration.md). Nākamajā tabulā ir sniegts apskats par vedņa lapām un katras lapas mērķi.

| Lapa                       | Apraksts |
|----------------------------|-------------|
| Valsts/reģions             | Valsts vai reģions nosaka piegādātāja pieprasījuma konfigurāciju, kas tiek lietota atlikušajās vedņa lapās. Šī lapa nosaka arī vērtības uzmeklēšanā **Nodokļa valsts**. |
| Noteikumi un nosacījumi       | Šī lapa var būt pieejama atkarībā no piegādātāja pieprasījuma konfigurācijas. Ja tā ir pieejama, lietotājam ir jāapliecina piekrišana noteikumiem un nosacījumiem, lai varētu turpināt. |
| Piegādātāja informācija         | Šajā lapā ir kreditora nosaukums, kas tiek automātiski ievadīts no sākotnējā potenciālā piegādātāja reģistrācijas pieprasījuma. Tajā ir arī organizācijas numurs, kreditora tālruņa numurs, faksa numurs un e-pasta adrese, kā arī kreditora adreses dažādiem nolūkiem. |
| Kontaktpersonas informācija | Šajā lapā ir kontaktpersonas vārds un uzvārds, kas tiek automātiski ievadīti no sākotnējā potenciālā piegādātāja reģistrācijas pieprasījuma. Tajā ir arī kontaktpersonas tālruņa numurs un e-pasta adrese, un kontaktpersonas adreses dažādiem nolūkiem. |
| Biznesa informācija       | Šajā lapā ir nodokļu reģistrācijas numuri (dažādām valstīm vai reģioniem) un darbinieku numuri. Tajā ir arī norādīts, vai uzņēmums pieder minoritātei. |
| Sagādes kategorijas     | Šajā lapā ir sagādes kategorijas, attiecībā uz kurām kreditors pieprasa apstiprinājumu. Lietotājs kategorijas var atlasīt sagādes kategoriju hierarhijā. Hierarhijā rādīto līmeņu skaitu varat konfigurēt šeit: **Sagādes un avotu parametri** &gt; **Kreditoru sadarbība**, sadaļā **Sagāde un avoti** &gt; **Iestatīšana**. |
| Anketas             | Vednī var būt kreditoram paredzētu anketu kopa. Vednī redzamās anketas ir konfigurētas pēc piegādātāja pieprasījuma vai pēc sagādes kategorijas. Ja anketas ir konfigurētas pēc sagādes kategorijas, vednī redzamās anketas nosaka sagādes kategorijas, kurām piegādātājs pieprasa apstiprinājumu. Lapā **Sagādes kategorijas** pie atbilstošās kategorijas varat pievienot anketu un aktivitātes veidu iestatīt uz **Kreditora pievienošana**. |

Kad potenciālā piegādātāja lietotājs izpilda kreditora reģistrācijas vedņa norādījumus, tiek izveidots piegādātāja pieprasījums.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Piegādātāja pieprasījuma iesniegšana manuāli vai automātiski

Piegādātāja pieprasījumu var izveidot kā melnrakstu un iesniegt darbplūsmā manuāli. Alternatīvi piegādātāja pieprasījumu var iesniegt darbplūsmā automātiski, kad ir izpildīti kreditora reģistrācijas vedņa norādījumi. Pieprasījumu var iesniegt manuāli, ja, piemēram, sagādes speciālists vēlas izvērtēt, vai pirms iesniegšanas darbplūsmā attiecīgo pieprasījumu ir nepieciešams novirzīt caur apstiprinājuma procesu.

- Lai piegādātāja pieprasījumu konfigurētu tā, ka tas tiek iesniegts darbplūsmā automātiski, ja ir izpildīti piegādātāja reģistrācijas vedņa norādījumi, atlasiet **Sagādes un avotu parametri** &gt; **Kreditoru sadarbība** un pēc tam atlasiet **Potenciālo piegādātāju reģistrāciju automātiski iesniegt darbplūsmai**.

## <a name="vendor-requests"></a>Piegādātāja pieprasījumi

Piegādātāju pieprasījumi ir pieejami lapā **Kreditoru sadarbības lietotāju pieprasījumi**.

Piegādātāja pieprasījumā ir informācija, ko potenciālā piegādātāja lietotājs ievadīja kreditora reģistrācijas vednī.

Pieprasījums jums ļauj pārskatīt piegādātāja informāciju un izlemt, vai šim piegādātājam ir jākļūst par reģistrētu kreditoru programmā Finance and Operations.

Piegādātāja pieprasījums ir jāiesniedz darbplūsmā, un to ir nepieciešams novirzīt atbilstošajiem pārskatītājiem un apstiprinātājiem. Pamatinformāciju par veidu, kā iestatīt darbplūsmas, skatiet šeit: [Sagādes un avotu darbplūsmas](procurement-sourcing-workflows.md).

Nākamajā tabulā ir parādīti piegādātāju pieprasījumu iespējamie statusi.

| Statuss                     | Apraksts |
|----------------------------|-------------|
| Melnraksts                      | Piegādātāja pieprasījums vēl nav iesniegts. |
| Pieprasījums iesniegts          | Piegādātāja pieprasījums ir iesniegts, un tiek apstrādāta darbplūsmas pirmā darbība. |
| Gaida pārskatīšanu             | Ja kādā darbplūsmas uzdevumā ir vairāki pārskatītāji, kāds pārskatītājs var pieņemt piegādātāja pieprasījuma pārskatīšanas uzdevumu un pēc tam izpildīt pārskatīšanu. Ja ir tikai viens pārskatītājs, šis dalībnieks var izpildīt pārskatīšanu, darbplūsmas darbībā atlasot **Pabeigts**. Šim lietotājam nav nepieciešams vispirms pieņemt šo darbplūsmas vienumu. |
| Pieprasījums gaida apstiprināšanu   | Piegādātāja pieprasījums ir novirzīts dalībniekiem apstiprināšanai, un ir opcija papildinformācijas pieprasīšanai. Papildinformācijas pieprasījums izraisa darbplūsmas elementa novirzīšanu atpakaļ uz iesniedzēja. Piegādātāja pieprasījumu var arī apstiprināt vai noraidīt, kamēr tas atrodas šajā statusā. |
| Pieteikuma izmaiņu pieprasījums | Apstiprinātājs ir pieprasījis papildinformāciju, un piegādātāja pieprasījums ir novirzīts uz personu, kas iesniedza šo piegādātāja pieprasījumu. Iesniedzējs var pievienot nepieciešamo informāciju un pēc tam šo piegādātāja pieprasījumu iesniegt vēlreiz. Ja piegādātāja pieprasījums tiek iesniegts atkārtoti, tā statuss atkal mainās uz **Pieprasījums gaida apstiprināšanu**. |
| Pieprasījums apstiprināts           | Šis statuss ir galīgais stāvoklis. |
| Pieprasījums noraidīts           | Šis statuss ir galīgais stāvoklis. |

## <a name="approving-a-vendor-request"></a>Piegādātāja pieprasījuma apstiprināšana

Kad piegādātāja pieprasījums ir apstiprināts, tiek izveidots kreditora konts un gan sākotnējā potenciālā piegādātāja reģistrācijas pieprasījumā, gan piegādātāja pieprasījumā ir redzams statuss **Apstiprināts**.

Pirms apstiprināt piegādātāja pieprasījumu, lapā **Jauns piegādātājs**, kopsavilkuma cilnē **Vispārīgi** atlasiet **Kreditoru grupa**, lai atlasītu kādu kreditoru grupu.

Ja potenciālā piegādātāja lietotājam ir nepieciešama piekļuve sistēmai Finance and Operations kā kreditoru sadarbības lietotājam, kas pārstāv šo piegādātāju, kreditoru sadarbības piekļuves atļauju iestatiet uz **Jā**. Lai deaktivizētu lietotāja kontu, kuru potenciālais piegādātājs izmantoja, lai reģistrētos, iestatiet šo atļauju uz **Nē**.

Ja kreditoru sadarbības piekļuves atļauja ir iestatīta uz **Jā**, kad piegādātāja pieprasījums ir apstiprināts, tiek iesniegts pieprasījums modificēt lietotāju lomas, lai šim lietotājam būtu lomas, kas iestatījumā **Ārējās lomas** ir definētas veidam **Kreditors**. Ja šī atļauja ir iestatīta uz **Nē**, kad piegādātāja pieprasījums ir apstiprināts, tiek iesniegts pieprasījums deaktivizēt šo lietotāju. Šajā gadījumā ir jāiestata darbplūsma lietotāja pieprasījuma deaktivizēšanai.

Lai pēc piegādātāja pieprasījuma apstiprināšanas tiktu izveidots kreditora konts, numuru sērija kreditoru izveidošanai no piegādātāju pieprasījumiem ir jāiestata uz **Automātiski**.

Apskatu par kreditoru sadarbības lietotāja piekļuves atļaujām skatiet šeit: [Kreditoru sadarbības iestatīšana un uzturēšana](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Piegādātāja pieprasījuma noraidīšana

Ja piegādātāja pieprasījums tiek noraidīts, šajā piegādātāja pieprasījumā ir jāatlasa noraidīšanas iemesls.

Kad piegādātāja pieprasījums tiek noraidīts, tiek iesniegts pieprasījums par lietotāja deaktivizēšanu. Šajā gadījumā ir jāiestata darbplūsma lietotāja pieprasījuma deaktivizēšanai. Papildinformāciju skatiet šeit: [Kreditoru sadarbības iestatīšana un uzturēšana](set-up-maintain-vendor-collaboration.md).

Kad piegādātāja pieprasījums ir noraidīts, gan sākotnējā potenciālā piegādātāja reģistrācijas pieprasījumā, gan piegādātāja pieprasījumā ir redzams statuss **Noraidīts**.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Potenciālā piegādātāja reģistrācijas pieprasījuma dzēšana dažādos statusos

Potenciālā piegādātāja reģistrācijas pieprasījuma dažādie statusi sniedz apskatu par pieprasījuma izpildes gaitu.

Potenciālā piegādātāja reģistrācijas pieprasījumam izmantojot darbību **Dzēst**, varat iztīrīt un noņemt izveidotās ierakstu ķēdes un varat deaktivizēt lietotāja kontu. Darbības **Dzēst** rezultāts ir atkarīgs no potenciālā piegādātāja reģistrācijas pieprasījuma statusa, kā parādīts nākamajā tabulā.

| Statuss                   | Statusa apraksts | Darbības Dzēst rezultāts |
|--------------------------|--------------------|-----------------------------------|
| Jauns                      | Ar pieprasījumu nav veiktas nekādas darbības. | Potenciālā piegādātāja reģistrācijas pieprasījums ir izdzēsts. |
| Lietotājs pieprasīja           | Kad atlasāt **Uzaicināt lietotāju**, statuss mainās uz **Lietotājs pieprasīja**, tiek izveidots potenciālā lietotāja pieprasījums, un tas tiek iesniegts lietotāja reģistrācijas darbplūsmā. | Potenciālā piegādātāja reģistrācijas pieprasījumu ar šādu statusu nevar izdzēst, jo lietotāja pieprasījuma darbplūsma nav beigusies. |
| Lietotājs uzaicināja             | Lietotāja pieprasījuma darbplūsma ir apstiprināta, un lietotājs ir izveidots. | Tiek izveidots pieprasījums deaktivizēt lietotāju, un potenciālā piegādātāja reģistrācijas pieprasījums tiek izdzēsts. |
| Notiek reģistrēšana | Jaunais lietotājs ir pierakstījies un ir palaidis kreditora reģistrācijas vedni. | Tiek izveidots pieprasījums deaktivizēt lietotāju, un tiek izdzēsts potenciālā piegādātāja reģistrācijas pieprasījums un kreditora reģistrācijas vednī ievadītie dati. |
| Piegādātāja pieprasījums ir izveidots   | Kreditora reģistrācijas vednis ir pabeigts. | Tiek izveidots pieprasījums deaktivizēt lietotāju, un tiek izdzēsts potenciālā piegādātāja reģistrācijas pieprasījums, kreditora reģistrācijas vednī ievadītie dati un piegādātāja pieprasījums.<blockquote>[!NOTE]<br>Darbību **Dzēst** nevar lietot, kad piegādātāja pieprasījumam darbplūsmā notiek pārskatīšanas process.</blockquote> |
| Apstiprināts                 | Piegādātāja pieprasījums ir apstiprināts. | Tiek izdzēsts potenciālā piegādātāja reģistrācijas pieprasījums, kreditora reģistrācijas vednī ievadītie dati un piegādātāja pieprasījums. |
| Noraidīts                 | Piegādātāja pieprasījums ir noraidīts. | Tiek izdzēsts potenciālā piegādātāja reģistrācijas pieprasījums, kreditora reģistrācijas vednī ievadītie dati un piegādātāja pieprasījums. |

