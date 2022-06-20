---
title: Pārskats par veidnēm un izkārtojumiem
description: Šajā rakstā ir ietvertas veidnes un izkārtojumi sadaļā Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 12/12/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: adf1585e418ca2d09065db03de72cb1bbfb3e614
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844624"
---
# <a name="templates-and-layouts-overview"></a>Pārskats par veidnēm un izkārtojumiem


[!include [banner](includes/banner.md)]

Veidnes ir Microsoft Dynamics 365 Commerce lapas modeļa pamata elements. Ja jūsu mērķis ir palielināt vietnes autorēšanas darbplūsmu efektivitāti un konsekvenci, ir svarīgi zināt, kā izmantot veidnes priekšrocības jūsu vietnei. Pirmie lēmumi par veidņu struktūru ir svarīgi, un tie var būtiski ietekmēt ikdienas, sezonālās un vietnes zīmola atjauninājumu izmaksas un dinamiskumu. Labi strukturētām veidnēm ir arī citas priekšrocības. Piemēram, tās palīdz uzlabot vietnes meklēšanas programmas optimizācijas (SEO) rezultātus un samazināt kļūdu skaitu.

Labs veids, kā sākt strādāt ar veidnēm, ir izprast veidņu un izkārtojumu funkcionālās priekšrocības, atšķirības starp tām un to hierarhiju.

Tālāk esošajā attēlā redzama lapas modeļa hierarhija aiz atveidotas lapas.

![Lapas modeļa diagramma.](../commerce/media/page-model-diagram.png)

| Entītija        | Pamata funkcija |
|---------------|----------------|
| Veidne      | Veidnes nosaka moduļu opcijas un pamata sastatnes, lai izveidotu izkārtojumus un lapas instances. |
| Izkārtojums        | Izkārtojumi definē moduļu gala atlasi un izkārtojumu lapai vai lapu kopai. |
| Lapas instance | Lapas instances nosaka datus un saturu noteiktām lapām. |

## <a name="templates"></a>Veidnes

Veidnes atrodas Dynamics 365 Commerce lapas modeļa hierarhijas augšdaļā un norāda svarīgu sākuma darbību vietnes konfigurācijai. Konceptuāli veidnes palīdz kontrolēt konsekvenci starp pakārtotajiem izkārtojumiem un lapām, definējot pamatstruktūru un autorēšanas opcijas lejupstraumes izkārtojuma izveidei un lapu izveidei darbplūsmās. Veidnes var palīdzēt vienkāršot satura autorēšanas procesu, izmantojot iepriekš definētus, centrāli pārvaldītus elementus (piemēram, galvenes un kājenes) un vadītas autorēšanas plūsmas, kas palīdz nodrošināt to, ka moduļu konfigurācijas izvēles ir ar zīmolu.

### <a name="controlling-consistency"></a>Konsekvences kontrolēšana

Noformējot veidni, lielākais uzņēmuma lēmums, kas jāpieņem, ir, cik daudz kontroles ir jāpiešķir veidnēm attiecībā uz lapas izveides procesu. Veidne, kas atstāj visu atvērtu lejupstraumes autoram, ir vienkāršākais veidņu veids, ko izveidot, bet tā var radīt ilgtermiņa sekas attiecībā uz to lapu uzturēšanu, kas izveidotas no tās. Labi uzrakstīta veidne sniedz vadlīnijas un racionalizētu autorēšanas pieredzi, bet tā autoriem sniedz arī pietiekamu elastību, lai viņi varētu pabeigt savu uzdevumu. Visi šie aspekti ir atkarīgi no kontroles līmeņa, ko izpilda veidne.

Veidnes var palīdzēt satura autoriem būt efektīvākiem un uzturēt zīmolu tālāk norādītajos veidos.

- Ierobežot moduļus, kurus var izmantot lapā.
- Piedāvāt noklusējuma moduli un konfigurācijas izvēles.
- Skaidri izveidot dažus moduļa un konfigurācijas variantus, kas tiek kontrolēti veidnes līmenī. Šis process tiek saukts arī par iestatījuma *bloķēšanu*.

Šajā piemērā ir parādīts, kā var konfigurēt pamata veidni (veidne X).

- Visiem veidnes X pakārtotajiem izkārtojumiem ir jāietver galvenes konteiners, pamatteksta konteiners un kājenes konteiners.
- Veidnē X virsraksta konteinera konfigurācija ir bloķēta, un to var mainīt tikai pašā veidnē X. Visiem pakārtotajiem izkārtojumiem un lapām vienmēr ir šī galvene.
- Pamatteksta konteineram ir nepieciešams vismaz viens modulis un ne vairāk kā 10 moduļi. Šos moduļus definē lejupstraumes izkārtojumi un lapas.
- Pamatteksta konteineram ir pieejams centrālais, līdzekļa, karuseļa un reklāmkarogu modulis.
- Kājenes konteiners ir konfigurēts veidnē X, bet to var ignorēt, izmantojot lejupstraumes izkārtojumus un lapas.

Šajā piemērā veidne definē vienkāršu struktūru un opciju kopu lejupstraumes satura autoriem. Ievērojiet, ka dažas lapas daļas (šajā gadījumā galvene) ir pilnībā definētas un bloķētas veidnē, un lejupstraumes autori tās nevar mainīt. Citas daļas (šajā gadījumā pamatteksts) lejupstraumes autori var definēt noteiktās vadlīnijās (šajā gadījumā minimālo un maksimālo specifisko tipu moduļu skaitu). Un citas daļas (šajā gadījumā kājene) tiek definētas veidnē, bet lejupstraumes autori tās var ignorēt.

Svarīga sākotnējā darbība vietnes un zīmola administratoriem ir noteikt pareizo līdzsvaru starp ierobežojumu un elastību attiecībā uz pakārtoto izkārtojumu un lapu autoriem. Lietojot veidnes, šis līdzsvars ir pilnībā konfigurējams. Tas ietekmē, vai lapas elementi tiek centralizēti atjaunināti (bloķēti veidnē) vai atstāti atsevišķiem pakārtotajiem līmeņiem, kas ir zemāk lapas hierarhijā.

Lai sāktu izmantot veidnes, skatiet sadaļu [Darbs ar veidnēm](work-with-templates.md).

## <a name="layouts"></a>Izkārtojumi

Izkārtojumi ir nākamais līmenis lapas modeļa hierarhijā, zem veidnēm. Tā kā veidne definē visus moduļus, kas ir atļauti lapai, izkārtojums ir tieša moduļu atlase un izkārtošana. Lapas ir nākamais līmenis lapas modeļa hierarhijā, zem izkārtojumiem. Tās definē lokalizēto saturu moduļiem, kas atlasīti izkārtojumā.

Šis piemērs tiek veidots, pamatojoties uz iepriekšējās sadaļas veidnes paraugu, un parāda, kā var konfigurēt pamata izkārtojumu.

- Izkārtojuma pamata veidnei nepieciešams, lai pamatteksta konteiners būtu starp vienu un desmit moduļiem. Šie moduļi var būt tikai centrālais, līdzekļa, karuseļa un reklāmkarogu modulis. Tāpēc izkārtojums var definēt tālāk norādīto moduļu atlasi un izkārtojumu.

    - Pirmais modulis pamatteksta konteinerā ir reklāmkaroga modulis, un tam seko centrālais modulis un divi līdzekļa moduļi.
    - Pirmais līdzekļa modulis ir līdzināts pa kreisi, un otrs līdzekļa modulis ir līdzināts pa labi.

- Lai gan noklusējuma kājene ir pārmantota no pamata veidnes, tās autors ir atstājis kājeni atbloķētu. Tāpēc izkārtojums var ignorēt to, definējot citu kājenes fragmentu.

Izkārtojums šajā piemēra definē, kā tiek noteikts pakātotu lapu moduļu gala izkārtojums. Tāpat kā veidne, izkārtojums var definēt noklusējuma vai bloķēta moduļa rekvizītus, ko vienmēr pārmantos pakārtotās lapas (piemēram, līdzekļu moduļu līdzinājums). Faktiskais saturs vai dati katram modulim izkārtojumā pēc tam tiek definēti tālāk hierarhijā, katrā pakārtotās lapas instancē. Nozīmīga atšķirība ir tāda, ka izkārtojumi neietver tiešu saturu, turpretī to pakārtotās lapas ietver. Izkārtojuma primārā funkcija ir definēt gala izkārtojumu un noklusējuma konfigurāciju moduļiem tā pakārtotajām lapām.

Šī hierarhija ir spēcīga divu iemeslu dēļ. Pirmkārt, izkārtojumi, kas kopīgo vienu un to pašu pamata veidni, tiek uzskatīti par saderīgiem ar izkārtojuma pārslēgšanas scenārijiem. Tāpēc jebkuras lapas izkārtojumu var mainīt uz citu izkārtojumu no tās pašas veidnes hierarhijas, nepieprasot, lai lapas līmeņa saturs tiktu atkārtoti autorēts. Varat izmantot šo priekšrocību, lai veiktu sezonas dizaina atjauninājumus, eksperimentētu vai veiktu pastāvīgu vietnes pārbūvi. Otrkārt, izkārtojumi sniedz citu veidu, kā centralizēti modificēt koplietojamos elementus lapu grupai, neprasot atjaunināt atsevišķas lapas. Piemēram, ja preču kategorijā ir 1000 lapas ar vienu un to pašu izkārtojumu, moduļus var pārkārtot izkārtojumā, un šīs izmaiņas nekavējoties tiks atainotas visās 1000 pakārtotajās lapās.

Izprotot šo hierarhiju, varat nodrošināt dinamisku un efektīvu vietnes struktūru, kas palīdz ietaupīt izmaksas, ir mērogojams un nodrošina labākus rezultātus, jo vietne attīstās laika gaitā.

### <a name="preset-and-custom-layouts"></a>Iepriekš iestatītie un pielāgotie izkārtojumi

Izkārtojumi jūsu vietnē var būt *iepriekš iestatīti* vai *pielāgoti*.

- **Iepriekš iestatītie izkārtojumi** ļauj lapas izveides darbplūsmu, kur visi moduļi ir jau atlasīti un sakārtoti, un ir jānorāda tikai datu ievade. Šī pieeja palīdz ietaupīt laiku, kad ir jāautorē daudzas lapas, kurām ir vienādas izkārtojuma prasības. Iepriekš iestatītajiem izkārtojumiem ir relācija viens pret daudziem ar to pakārtotajām lapām. Tāpēc vienu iepriekš iestatītu izkārtojumu var izmantot, lai centralizēti kontrolētu moduļu sakārtojumu simtiem vai tūkstošiem pakārtotu lapu.
- **Pielāgotie izkārtojumi** būtībā ir vienreizējās lietošanas izkārtojumi, kas ir iegulti vienā lapā. Tie netiek piedāvāti kā opcija, kad tiek veidotas citas jaunas lapas vai izkārtojuma pārslēgšanas scenārijos. Šīs pieejas priekšrocība ir tāda, ka autors var eksperimentēt, autorējot lapu, kurā tiek izmantots pielāgots izkārtojums. Pēc tam, ja autors vēlas atkārtoti izmantot izkārtojumu citām lapām, to var viegli pārvērst par iepriekš iestatītu izkārtojumu. Jaunais iepriekš iestatītais izkārtojums tiek parādīts kā opcija lapu izveides darbplūsmās un izkārtojuma pārslēgšanas scenārijos lapām no tās pašas veidnes hierarhijas. Savukārt iepriekš iestatītos izkārtojumus var sazarot ar pielāgotiem izkārtojumiem. Šādā veidā autors var pārtraukt lapas noņemšanu no iepriekš iestatītā izkārtojuma un izveidot jaunu vienreizējas izmantošanas pielāgotu izkārtojumu. (Šis jaunais pielāgotais izkārtojums joprojām ir saistīts ar visiem ierobežojumiem pamata veidnē.)

Iepriekš iestatītais izkārtojums un pielāgotie izkārtojumi tiek rediģēti dažādās autorēšanas rīku kopās. Tā kā pielāgotajiem izkārtojumiem nav atkarību no citām lapām, tie tiek rediģēti tieši lapas redaktorā. Šādā gadījumā izkārtojuma esamība lielākoties ir caurskatāma lietotājam un tiek atklāta tikai lapas līmeņa rekvizītos un darbības izkārtojuma opcijās. Tomēr, ņemot vērā, ka iepriekš iestatīto izkārtojumu izmaiņas var ietekmēt daudzas pakārtotās lapas, tās ir jārediģē izkārtojuma redaktorā, kur publicētās darbības ņem vērā visu lejupstraumes ietekmi uz pakārtotajām lapām.

Tālāk esošajos attēlos ir parādīti iepriekš iestatītu un pielāgotu izkārtojumu scenāriji.

![Iepriekš iestatītu un pielāgotu izkārtojumu scenāriji.](../commerce/media/template-figure1.png)

Lai sāktu izmantot iepriekš iestatītus izkārtojumus, skatiet sadaļu [Darbs ar iepriekš iestatītiem izkārtojumiem](work-with-layouts.md).

## <a name="additional-resources"></a>Papildu resursi

[Darbs ar veidnēm](work-with-templates.md)

[Darbs ar iepriekš iestatītiem izkārtojumiem](work-with-layouts.md)

[Darbs ar publicēšanas grupām](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]