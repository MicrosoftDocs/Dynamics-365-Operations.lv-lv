---
title: Elektronisko pārskatu uzlabotās formulas redaktors
description: Šajā tēmā aprakstīts, kā uzlabotās formulas redaktoru var izmantot, lai konfigurētu elektronisko pārskatu (ER) modeļu kartēšanas izteiksmes un formāta komponentus.
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58d7a936f94e1cd453c904ef6404e0db65083c54235c8420b9cfa561bcde1584
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714663"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>Elektronisko pārskatu uzlabotās formulas redaktors

[!include [banner](../includes/banner.md)]

Papildus [Elektronisko pārskatu](general-electronic-reporting.md) [formulas redaktoram](general-electronic-reporting-formula-designer.md) varat izmantot uzlaboto elektronisko pārskatu formulas redaktoru, lai uzlabotu elektronisko pārskatu (ER) izteiksmju konfigurēšanas pieredzi. Uzlabotais redaktors ir pieejams pārlūkprogrammā, un to nodrošina [Monako redaktors](https://microsoft.github.io/monaco-editor). Tālāk apskatītajā tēmā ir aprakstītas visbiežāk izmantotās uzlabota redaktora funkcijas.

- [Kodu autoformatējums](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [Kodu pabeigšana](#CodeCompletion)
- [Kodu navigācija](#CodeNavigation)
- [Kodu strukturēšana](#CodeStructuring)
- [Meklēt un aizvietot](#FindAndReplace)
- [Datu ielīmēšana](#DataPasting)
- [Sintakses iekrāsošana](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">Uzlabotās formulas redaktora aktivizēšana</a>

Veiciet tālāk norādītās darbības, lai sāktu izmantot uzlabotās formulas redaktoru savā Microsoft Dynamics 365 Finance instancē.

1.  Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2.  Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3.  Dialoglodziņā **Lietotāja parametri** sadaļā **Izpildes izsekošana** iestatiet parametru **Iespējot uzlabotās formulas redaktoru** uz **Jā**.

[![Lietotāja parametru dialoglodziņš, Iespējot izcelto papildu formulas redaktora parametru.](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Ņemiet vērā, ka šis parametrs ir lietotājam raksturīgs un uzņēmumam raksturīgs.

Sākot ar Microsoft Dynamics 365 Finance versiju 10.0.19, varat kontrolēt, kurš ER formulas redaktors tiek piedāvāts pēc noklusējuma. Veiciet šīs darbības, lai iespējotu papildu formulas redaktoru visiem pašreizējās Finance instances lietotājiem un uzņēmumiem.

1.  Atveriet darbvietu **Funkcionalitātes pārvaldība**.
2.  Atrodiet sarakstā un atlasiet līdzekli **Iestatīt ER papildu formulas redaktoru kā noklusējuma redaktoru visiem lietotājiem**, pēc tam atlasiet **Aktivizēt tagad**.
3.  Dodieties uz **Organizācijas administrēšana** > **Elektronisko atskaišu veidošana** > **Konfigurācijas**.
4.  Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
5.  Dialoglodziņā **Lietotāja parametri** atrodiet parametru **Atspējot papildu formulas redaktoru** un pārbaudiet, vai tas ir iestatīts uz **Nē**.

[![Lietotāja parametru dialoglodziņš, Atspējot izcelto papildu formulas redaktora parametru.](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)

> [!NOTE]
> Parametru vērtības **Iespējot papildu formulas redaktoru** un **Atspējot papildu formulas redaktoru** tiek paturētas atsevišķi katram lietotājam un tiek piedāvātas dialoglodziņā **Lietotāja parametri** atkarībā no līdzekļa **Iestatīt ER papildu formulas redaktoru kā noklusējuma redaktoru visiem lietotājiem** statusa.

## <a name=""></a><a name="Autoformatting">Kodu autoformatējums</a>

Kad rakstāt kompleksu izteiksmi, kas sastāv no vairākām koda rindām, jaunas ievadītas rindas atkāpe būs atbilstoša iepriekšējās rindas atkāpei. Varat atlasīt rindas un mainīt to atkāpes, ierakstot **Cilne** vai **Shift+Tab**.

[![ER formulas redaktora gif, kas rāda rindu atlasi un atkāpes mainīšanas rādīšanu.](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Izmantojot autoformatēšanu, varat saglabāt visu izteiksmi labi formatētu, kas atvieglos turpmāku uzturēšanu un vienkāršos konfigurētās loģikas izpratni.

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

Redaktors nodrošina vārdu pabeigšanu, kas palīdz ātrāk uzrakstīt izteiksmi un izvairīties no iespiedkļūdām. Kad sākat pievienot jaunu tekstu, redaktors automātiski piedāvā to funkciju sarakstu, kas tiek atbalstītas ER funkcijās, kuras satur ievadītās rakstzīmes. Varat arī jebkurā konfigurētās izteiksmes vietā aktivizēt IntelliSense, ievadot **Ctrl+Atstarpe**.

[![ER formulas redaktora gif, kas rāda trigeru IntelliSense.](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Kodu pabeigšana</a>

Redaktors automātiski nodrošina koda pabeigšanu, veicot tālāk minētās darbības.

- Ievietojot aizverošo iekavu, kad tiek ievadīta atverošā iekava, noturot kursoru iekavās.
- Ievietojot otro pēdiņu simbolu, kad tiek ierakstīts pirmais, paturot kursoru pēdiņās.
- Ievietojot otro dubultpēdiņu simbolu, kad tiek ierakstīts pirmais, paturot kursoru pēdiņās.

[![ER formulas redaktora gif, kas automātiski parāda redaktoru, kas nodrošina koda pabeigšanu.](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Kad norādāt uz ierakstītajam pēdiņām, šī pāra otrā iekava tiek automātiski iezīmēta, lai parādītu konstrukciju, ko tās atbalsta.

## <a name=""></a><a name="CodeNavigation">Kodu navigācija</a>

Izteiksmē nepieciešmos simbolus vai rindas var sameklēt, ievadot komandu **Doties uz**, izmantojot komandu paleti vai konteksta izvēlni.

Piemēram, lai pārlēktu uz **8**. rindu, veiciet tālak norādītās darbības.

- Piespiediet taustiņu kombināciju **Ctrl+G**, ievadiet vēŗtību **8** un pēc tam piespiediet taustiņu **Enter**.

  - vai -

- Piespiediet **F1**, ierakstiet **G**, atlasiet **Doties uz rindu**, ievadiet vērtību **8** un piespiediet **Enter**.

[![ER formulas redaktora gif, kas parāda, kā atrast izteiksmes daļas, izmantojot komandu paleti.](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">Kodu strukturēšana</a>

Dažu funkciju kods, piemēram [IF](er-functions-logical-if.md) vai [CASE](er-functions-logical-case.md), ir automātiski strukturēts. Varat izvērst un sakļaut jebkuru vai visus šī koda saliekamos reģionus, lai samazinātu izteiksmes rediģējamo daļu un koncentrētos tikai uz to koda daļu, kam jāpievērš uzmanība. Šim nolūkam var izmantot pārslēgšanas komandas salocīt/atlocīt.

Piemēram, lai salocītu visus reģionus, veiciet tālāk norādītās darbības.

- Piepiediet **Ctrl+K**

  - vai -

- Piespiediet **F1**, piespiediet **FO**, atlasiet **Salocīt visu** un pēc tam piespiediet **Enter**

Lai salocītu visus reģionus, veiciet tālāk norādītās darbības.

- Piepiediet **Ctrl+J**

  - vai -
  
- Piespiediet **F1**, ierakstiet **UN**, atlasiet **Atlocīt visu** un pēc tam piespiediet **Enter**

[![ER formulas redaktora gif, kas rāda kodu, kas tiek izvērsts.](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">Meklēt un aizvietot</a>

Lai atrastu konkrēta teksta gadījumus, atlasiet izteiksmē tekstu un veiciet tālāk norādītās darbības.

- Piespiediet **Ctrl+F** un pēc tam piespiediet **F3**, lai atrastu nākamo atlasītā teksta gadījumu, vai piespiediet **Shift+F3**, lai atrastu iepriekšējo gadījumu.

  - vai -
  
- Piespiediet **F1**, ievadiet **F** un pēc tam atlasiet nepieciešamo opciju, lai atrastu atlasīto tekstu.

Lai aizvietotu konkrēta teksta gadījumus, atlasiet izteiksmē tekstu un veiciet tālāk norādītās darbības.

- Piepiediet **Ctrl+H**. Ievadiet alternatīvo tekstu un atlasiet aizstāšanas opciju, lai pašreizējā izteiksmē aizstātu atlasīto tekstu vai visus šī teksta gadījumus.

  - vai -
  
- Piespiediet **F1**, ievadiet **R** un pēc tam atlasiet nepieciešamo opciju, lai aizstātu atlasīto tekstu. Ievadiet alternatīvo tekstu un atlasiet aizstāšanas opciju, lai pašreizējā izteiksmē aizstātu atlasīto tekstu vai visus šī teksta gadījumus.

Lai izmainītu visus konkrēta teksta gadījumus, atlasiet izteiksmē tekstu un veiciet tālāk norādītās darbības.

- Piespiediet **Ctrl+F2** un pēc tam ievadiet alternatīvo tekstu.

  - vai -
  
- Piespiediet **F1**, ievadiet **C** un pēc tam atlasiet nepieciešamo opciju, lai izmainītu atlasīto tekstu. Ievadiet alternatīvo tekstu.

[![ER formulas redaktora gif, kas rāda atrast un aizstāt.](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Datu avoti un funkciju ielīmēšana</a>

Varat atlasīt **Pievienot datu avotu**, kas Ielīmē pašreizējā izteiksmē datu avotu, kas pašlaik ir atlasīts **Datu avota** kreisajā panelī. Līdzīgi varat atlasīt **Pievienot funkciju**, kas ielīmē pašreizējā izteiksmē funkciju, kura pašlaik ir atlasīta **Funkciju** labajā panelī. Ja izmantojat ER formulas redaktoru, atlasītā funkcija vai atlasītais datu avots vienmēr tiks ielīmēts konfigurētās izteiksmes beigās. Ja izmantojat uzlabotās ER formulas redaktoru, atlasītā funkcija vai atlasītais datu avots var tikt ielīmēts jebkurā konfigurētās izteiksmes daļā. Lai norādītu, kur vēlaties ielīmēt datus, būs jāizmanto kursors.

[![ER formulas redaktora gif, kas rāda datu avota pievienošanu un funkcijas ielīmētu.](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Sintakses iekrāsošana</a>

Pašlaik tiek lietotas dažādas krāsas, lai iezīmētu tālāk norādītās izteiksmes daļas.

- Teksts dubultiekavās, kas var apzīmēt teksta konstantes etiķetes ID.

[![ER formulas redaktors.](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="limitations"></a>Ierobežojumi

Redaktors pašlaik tiek atbalstīts šādās tīmekļa pārlūkprogrammās:

- Chrome
- Edge
- Firefox
- Opera
- Safari

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)
- [Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)
- [Monako redaktors](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
