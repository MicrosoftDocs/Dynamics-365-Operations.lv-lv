---
title: Rindas definīcijas finanšu atskaišu veidotājā
description: Rindas definīcija ir atskaites komponents jeb veidošanas bloks, kas norāda katras rindas saturu finanšu atskaitē.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.form: FinancialReports
ms.openlocfilehash: 3325f76f991ea6d2a1b6131f299460e529d63d38
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802450"
---
# <a name="row-definitions-in-financial-report-designer"></a>Rindas definīcijas finanšu atskaišu veidotājā

[!include [banner](../includes/banner.md)]

Rindas definīcija ir atskaites komponents jeb veidošanas bloks, kas norāda katras rindas saturu finanšu atskaitē. Rindas definīciju var kombinēt ar kolonnas definīcijām, atskaišu koka definīcijām un atskaites definīcijām, lai izveidotu veidošanas bloku grupu, kuru var izmantot vairāki uzņēmumi.

## <a name="create-a-row-definition"></a>Rindu definīcijas izveide

1. Pārskatu veidotājā navigācijas rūtī noklikšķiniet uz **Rindas definīcijas**.
2. Izvēlnē Fails **noklikšķiniet** uz Jauns **un** pēc tam uz **Rindas definīcija**. Lai iegūtu papildu informāciju par katras šūnas saturu, skatiet [Rindu definīciju šūnu modificēšana](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Rindas definīcijas atvēršana
1. Pārskatu veidotājā navigācijas rūtī noklikšķiniet uz **Rindas definīcijas**.
2. Veiciet dubultklikšķi uz tās rindas definīcijas, kuru vēlaties atvērt.
3. Lai apskatītu veidošanas blokus, kas ir saistīti ar rindas definīciju, ar peles labo pogu noklikšķiniet uz rindas definīcijas un tad atlasiet **Asociācijas**.

## <a name="contents-of-a-row-definition"></a>Rindas definīcijas saturs
Rindas definīcijas var ietvert līdz 20 000 finanšu dimensiju rindu, kā arī tālāk minēto informāciju.

- Aprakstošs teksts, kas pārskatam pievieno nozīmi, izveidojot sadaļu virsrakstus, rindas un atstarpes, piemēram, Skaidra **nauda** vai **Kopējie ieņēmumi**
- Saites uz finanšu datiem, kas 365. finanšu datos Microsoft Dynamics var ietvert dimensiju vērtības

    > [!NOTE]
    > Varat iestatīt, lai katru reizi, kad tiek ģenerēts pārskats, rindu definīcijai tiktu iegūti dati no finanšu dimensiju sistēmas.

- Rindu kopsummas un formulas, kuru pamatā ir saistītie finanšu dati

Parasti katra rinda rindas definīcijā satur vienu no šiem informācijas tipiem:

- Atsauces uz finanšu dimensiju sistēmu
- Kopsummas vai uz datiem balstīti aprēķini
- Formatēšana

Rindas definīcijā informāciju var ievadīt divos veidos:

- Informāciju manuāli ievadīt jaunā rindas definīcijā. Plašāku informāciju skatiet sadaļā [Rindu definīciju šūnu modificēšana](modify-row-definition-cells-financial-reporting.md).
- Izmantot atskaišu veidotāju, lai rindas informāciju izgūtu tieši no finanšu dimensijām. Plašāku informāciju skatiet sadaļā “Saistītās formulas/rindas/vienības”, rakstā [Modificēt rindu definīcijas šūnas](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a>Dimensiju pievienošana rindas definīcijai
Dimensija ir datu un vērtību krustpunkts. Atskaišu veidotājā datus un vērtības varat grupēt. Pēc tam transakcijas varat detalizētāk klasificēt un analizēt. Varat izmantot dialoglodziņu **Ievietot rindas no dimensijām**, lai vienlaicīgi rindas definīcijai pievienotu vairākas rindas. Dialoglodziņā katrai dimensijai attēlo vienu kolonnu. Nākamajā tabulā ir aprakstīta informācija, ko varat norādīt katrai dimensijai.

| Opcija                | Apraksts |
|-----------------------|-------------|
| Dimensija             | Modelis, kas identificē dimensiju, kura jāpievieno rindas definīcijai. Šajā modelī ir ietverta viena zīme & un viena restītes zīme (\#) atbilstoši katrai dimensiju pozīcijai. Parasti visas (&) zīmes tiek izmantotas galvenā konta dimensijai, un visas numura zīmes tiek izmantotas citām dimensijām. |
| Dimensiju diapazona sākums | Pirmā šīs dimensijas vērtība, kas jāpievieno rindas definīcijai. |
| Dimensiju diapazona beigas   | Pēdējā vērtība šai dimensijai, kuru pievienot rindas definīcijai. |

Lai rindas definīcijai pievienotu dimensijas, izpildiet šādas darbības.

1. Pārskatu veidotājā noklikšķiniet uz **Rindas definīcijas un** pēc tam atveriet modificējamās rindas definīciju.
2. Izvēlnē Rediģēt **noklikšķiniet** uz Iespraust rindas **no dimensijām**.
3. Dialoglodziņa Ievietot **rindas no**  **dimensijām** rindā Dimensijas atlasiet šūnu dimensijai, ko pārsūtīt uz rindas definīciju, un pēc tam noklikšķiniet uz **Visi &&>.**
4. Lai ierobežotu rindas definīciju ar noteiktu dimensijas vērtību diapazonu, **ievadiet** sākuma dimensijas vērtību dimensijas diapazona sākuma šūnā un **pēc tam ievadiet dimensijas beigu vērtību dimensiju diapazona beigu** šūnā. Lai iekļautu visas atlasītās dimensijas vērtības, atstājiet šīs šūnas tukšas.

    > [!NOTE]
    > Ja dimensiju diapazonos tiek izmantotas aizstājējzīmes (\* vai ?), atkarībā no tā, kā dati tiek šķiroti ERP datu bāzē, var netikt uzrādīti visi vēlamie rezultāti.

5. Laukā **Sākuma rindas kods** norādiet rindas kodu pirmajai dimensijas vērtībai, kas jāpievieno rindas definīcijai.
6. Laukā **Pieauguma solis katrā rindā** norādiet atstarpi starp secīgiem rindu kodiem. Piemēram, ja pirmās rindas kods ir 100 un pieauguma vērtība ir 30, pirmo jauno rindu kodi ir 100, 130, 160, 190 un 220. Izmantojiet pieauguma vērtību, kas nodrošina pietiekami daudz vietas jaunu formāta un formulas rindu ievietošanai.
7. Noklikšķiniet uz **Labi**. Katrai no atlasītajām dimensijas vērtībām rindas definīcijai tiek pievienota viena rinda.

## <a name="adjust-rounding-in-a-row-definition"></a>Noapaļošanas koriģēšana rindas definīcijā
Ja jums ir bilance, kur summas tiek noapaļotas, tad kopsummas var nesakrist. Šāda problēma var rasties, ja, piemēram, jūs bilances atskaitē izmantojat noapaļošanas opciju un arī atskaites definīcijai ir norādīta noapaļošana. Varat rindas definīcijā izmantot opciju **Noapaļošanas korekcija**, lai sabalansētu bilanču summas. Varat noapaļošanu izslēgt vai to modificēt atskaites definīcijas cilnē **Iestatījumi**. Sekojošajā tabulā redzams, kā šīs summas tiek noapaļotas. Ja noapaļošana ir ieslēgta, šīs tabulas 100. un 200. rindas kopsummas atšķiras.

| Rindas kods | Summas bez noapaļošanas | Summa ar noapaļošanu līdz pilniem tūkstošiem |
|----------|--------------------------|-----------------------------------------|
| 100      | 3600                    | 4.                                       |
| 200      | 3700                    | 4.                                       |
| KOPĀ    | 7300                    | 8.                                       |

Lai koriģētu bilances noapaļošanu, izpildiet šādas darbības.

1. Pārskatu veidotājā noklikšķiniet uz **Rindas definīcijas un** pēc tam atveriet modificējamās rindas definīciju.
2. Izvēlnē Rediģēt **noklikšķiniet** uz Noapaļošanas **pielāgojums**.
3. Dialoglodziņā Noapaļošanas **pielāgojumi** ievadiet šādas vērtības:

    - **Noapaļošanas korekcijas rinda** — rindas kods tai rindai, kura ir jāpielāgo bilances izlīdzināšanai.
    - **Kopējo aktīvu rinda** — rindas kods rindai bilancē, kas satur kopējo aktīvu summu.
    - **Saistību un kapitāla kopsummas rinda** — rindas kods rindai bilancē, kas satur kopējo saistību un kapitāla summu.
    - **Korekcijas summas ierobežojums** — pozitīvs vesels skaitlis, kas norāda automātisko korekciju ierobežojumu. Šī summa tiek salīdzināta ar faktiskās noapaļošanas starpības absolūto vērtību.

    > [!NOTE]
    > Šie rindu kodi ir jāsaista ar finanšu datiem. Tas nozīmē, ka rindai šūnā **Saite uz finanšu dimensijām** ir nepieciešama dimensijas vērtība. **Neatsaucieties** uz apraksta (**DESC**), aprēķina (**CALC**) vai kopsavilkuma (**TOT**) rindu.

Kad noapaļošana ir ieslēgta, jūsu bilances summas tagad tiks izlīdzinātas.

> [!NOTE]
> Korekcijas ierobežojums tiek piemērots, ņemot vērā šī pārskata definīcijai noteikto opciju **Noapaļošanas precizitāte**. Piemēram, ja atskaites summas noapaļojat līdz tūkstošiem un laukā **Korekcijas summas ierobežojums** ievadāt **2**, tad brīdinājuma ziņojums tiek parādīts, kad laukā **Noapaļošanas korekcijas rinda** esošā vērtība tiek palielināta vai samazināta par vairāk nekā 2000.

## <a name="format-row-and-column-text"></a>Rindu un kolonnu teksta formatēšana
Savu pārskatu izskatu varat pielāgot, mainot fontus un izmantojot teksta formatēšanu. Nākamajās sadaļās ir paskaidrots, kā formatēt atskaišu rindu un kolonnu izskatu.

### <a name="manage-font-styles"></a>Fontu stilu pārvaldība

Savai atskaitei varat veidot un modificēt fontu stilus. Pēc tam šos stilus varat lietot dokumentam vai konkrētai atskaites rindai vai kolonnai.

<table>
<tbody>
<tr>
<td><strong>Fonta stila izveide</strong></td>
<td>
<ol>
<li>Pārskatu veidotājā izvēlnē Formāts <strong>noklikšķiniet uz Stili</strong> un formatēšana <strong></strong>.</li>
<li>Dialoglodziņā Stili <strong>un formatēšana noklikšķiniet</strong> uz Jauns <strong></strong> un pēc tam ievadiet unikālu jaunā stila nosaukumu.</li>
<li>Atlasiet fontu un noklikšķiniet uz <strong>Labi</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Fonta stila modificēšana</strong></td>
<td>
<ol>
<li>Pārskatu veidotājā izvēlnē Formāts <strong>noklikšķiniet uz Stili</strong> un formatēšana <strong></strong>.</li>
<li>Dialoglodziņā Stili <strong>un formatēšana atlasiet</strong> modificējamu stilu un pēc tam noklikšķiniet uz <strong>Modificēt</strong>.</li>
<li>Atlasiet fontu un noklikšķiniet uz <strong>Labi</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Fonta stila pielietošana</strong></td>
<td>
<ol>
<li>Pārskatu veidotājā definīciju vai kolonnu definīcijā vai virsrakstos un kājenēs atlasiet vienu vai vairākas šūnas.</li>
<li>Rīkjoslas sarakstā <strong>Stils</strong> atlasiet fonta stilu.</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Rindas teksta formatēšana

Rindas definīcijā norādītais formatējums ignorē visu formatējumu, kas ir norādīts kolonnas definīcijā un atskaites definīcijā. Teksta formātu varat modificēt, izmantojot formatēšanas rīkjoslas vadīklas. Tās ir Microsoft Windows standarta vadīklas.

1. Pārskata veidotājā atveriet modificējamās rindas definīciju.
2. Atlasiet formatējamās šūnas. Lai atlasītu vairākas šūnas, atlasīšanas laikā turiet taustiņu Ctrl.
3. Rīkjoslā noklikšķiniet uz nepieciešamā formāta pogas. Piemēram, lai izveidotu rindas atkāpi, atlasiet rindu un pēc tam noklikšķiniet uz Palielināt atkāpi **Palielināt** ![atkāpi.](media/indent.gif "Palielināt atkāpi") rīkjoslā.

### <a name="adjust-columns-while-you-design-reports"></a>Kolonnu pielāgošana pārskatu veidošanas laikā

Lai atvieglotu iespēju apskatīt kolonnas, ar kurām strādājat rindas definīcijā, varat pielāgot kolonnas platumu, ka arī paslēpt (minimizēt) vai parādīt kolonnas apskates rūtī. Jūsu veiktās modifikācijas ietekmē tikai kolonnu izskatu ekrānā. Tās neietekmē šo kolonnu formatējumu atskaitēs.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Kolonnas platuma maiņa apskates rūtī

1. Pārskata veidotājā atveriet modificējamās rindas definīciju.
2. Izvēlnē Formāts **atlasiet** Kolonnas **platums**.
3. Dialoglodziņā Kolonnas **platums** ievadiet vērtību un pēc tam noklikšķiniet uz **Labi**. Lai mainītu kolonnas platumu, varat arī vilkt kolonnas virsraksta šūnas labo malu.

### <a name="hide-columns-in-the-view-pane"></a>Kolonnu paslēpšana apskates rūtī

1. Pārskata veidotājā atveriet modificējamās rindas definīciju.
2. Atlasiet vienu vai vairākas kolonnas, ko samazināt.
3. Veiciet klikšķi ar peles labo pogu un tad noklikšķiniet uz **Paslēpt**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Visu paslēpto kolonnu rādīšana apskates rūtī

1. Pārskata veidotājā atveriet modificējamās rindas definīciju.
2. Ar peles labo pogu noklikšķiniet uz minimizētās kolonnas, kuru vēlaties parādīt, un pēc tam noklikšķiniet uz **Parādīt**.


## <a name="additional-resources"></a>Papildu resursi

[Finanšu pārskatu veidošana](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
