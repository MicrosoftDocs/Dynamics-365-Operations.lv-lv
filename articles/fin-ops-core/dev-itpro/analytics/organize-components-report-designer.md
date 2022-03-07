---
title: Pārskatu komponentu organizēšana pārskatu noformētājā
description: Šajā rakstā ir paskaidrots, kā sakārtot esošas atskaites, veidošanas blokus un objektus atskaišu veidotājā.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6b30e7e480edb50bb9509e270806224755f98e38111cda0c1cae86a0f56eb193
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763528"
---
# <a name="organize-report-components-in-report-designer"></a>Organizēt atskaites komponentus atskaišu veidotājā

[!include [banner](../includes/banner.md)]

Kad esat izveidojuši veidošanas blokus un ģenerējuši atskaites, ir noderīgi šos objektus sakārtot, lai lietotāji tos varētu vienkāršāk atrast. Šajā rakstā ir paskaidrots, kā sakārtot esošas atskaites, veidošanas blokus un objektus atskaišu veidotājā.

Atskaišu veidotājā varat pārdēvēt mapes, atskaites, veidošanas blokus un citus objektus, lai palīdzētu kārtot savus failus. Atkarībā no pārdēvētā objekta tipa, iespējams, ir nepieciešams atjaunināt saistības ar šo objektu.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Pārdēvējiet mapi vai veidošanas bloku Pārskata veidotājā
Pārskatu veidotājā varat pārdēvēt mapes, pārskatu definīcijas, rindu definīcijas, kolonnu definīcijas un pārskatu koku definīcijas.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Mapes vai veidošanas bloka pārdēvēšana pārskatu veidotājā

1. Pārskatu veidotājā izmantojiet navigācijas rūti, lai atrastu pārdēvējamo mapi vai objektu.
2. Ar peles labo pogu noklikšķiniet uz mapes vai objekta, un pēc tam noklikšķiniet uz **Pārdēvēt**. Lauks **Nosaukums** navigācijas rūtī kļūst pieejams.
3. Ierakstiet jauno nosaukumu, un tad nospiediet taustiņu Enter.
4. Ja veidošanas bloks ir rindas definīcija, kolonnas definīcija vai atskaišu koka definīcija, tad jums ir nepieciešams atjaunināt pārējos veidošanas blokus, kas ar to ir saistīti. Ar peles labo pogu noklikšķiniet uz veidošanas bloka, kuru pārdēvēt 3. darbībā, atlasiet vienumu **Saistības** un pēc tam sarakstā atlasiet vienumu, lai to atjauninātu.
5. Atkārtojiet 4. soli, līdz visi saistītie krājumi tiks atjaunināti.

## <a name="create-and-manage-report-groups"></a>Izveidojiet un pārvaldiet pārskatu grupas.
Pārskatu definīcijas iespējams grupēt, lai vienlaicīgi izveidotu vairākus pārskatus. Lai izveidotu, modificētu, dzēstu un ģenerētu atskaišu grupas, ir nepieciešama veidotāja vai administratora loma. Lietotāji, kam ir ģeneratora loma, var ģenerēt atskaišu grupas, kā arī atskaišu grupām var modificēt lietotāju atskaišu definīciju iestatījumus.

### <a name="create-a-report-group"></a>Pārskata grupas izveidošana

1. Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.
2. Izvēlnē **Fails** noklikšķiniet uz **Jauns** &gt; **Pārskatu grupas definīcija**, lai skatītāja logā atvērtu jaunu pārskatu grupu. Varat arī noklikšķināt uz rīkjoslas pogas **Pārskatu grupa** ![Pārskatu grupa.](media/report-group.gif "Pārskatu grupa") rīkjoslā.
3. Noklikšķiniet uz cilnes **Pārskatu grupa**. Lai šī pārskata izveidošanai ignorētu informāciju par atsevišķu pārskatu definīcijām, atzīmējiet izvēles rūtiņu **Ignorēt uzņēmuma, detalizētas informācijas un datuma iestatījumus no atsevišķām pārskatu definīcijām**. Uzņēmuma nosaukums, detalizētības līmenis, provizoriskie iestatījumi un datuma informācija tiek ievadīta automātiski, bet jūs varat veikt atjauninājumus.
4. Lai ģenerētu vairākas atskaites, kurās ir redzamas atskaišu valūtas, atzīmējiet izvēles rūtiņu **Ietvert visas atskaišu valūtas**. Pēc tam varat piekļūt vairākiem skatiem, tīmekļa skatītājā noklikšķinot uz pogas **Valūta**, kas skatāt šo atskaiti.
5. Laukā **Atskaites grupā** noklikšķiniet uz **Pievienot**, lai atlasītu atskaites, ko iekļaut atskaišu grupā. Lai dialoglodziņā **Pievienot** atlasītu vairākas atskaites, atskaišu atlasīšanas laikā turiet nospiestu taustiņu Ctrl. Kad esat beidzis atlasīt atskaites, noklikšķiniet uz **Labi**.
6. Noklikšķiniet uz **Fails** &gt; **Saglabāt**, lai saglabātu jauno pārskatu grupu.

### <a name="modify-a-report-group"></a>Modificēt pārskata grupu

1. Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.
2. Veiciet dubultklikšķi uz pārskata grupas, lai modificētu to.
3. Cilnē **Atskaišu grupa** veiciet nepieciešamās izmaiņas.
4. Izvēlnē **Fails** noklikšķiniet uz **Saglabāt**, lai saglabātu modificēto pārskatu grupu, vai arī noklikšķiniet uz rīkjoslas pogas **Saglabāt** ![Saglabāt.](media/save.gif "Saglabāt") rīkjoslā.

> [PIEZĪME] Ja esat ieplānojis atskaites, lai tās tiktu ģenerētas noteiktos intervālos, varat ignorēt šos iestatījumus un ģenerēt atskaiti nekavējoties.

### <a name="generate-a-report-group-report"></a>Izveidot pārskata grupu pārskatu

1. Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.
2. Atveriet pārskata grupu, lai izveidotu.
3. Noklikšķiniet uz pogas **Ģenerēt pārskatu** ![Ģenerēt pārskatu.](media/generate-report.gif "Ģenerēt pārskatu") lai ģeņerētu pārskatus.

### <a name="delete-a-report-group"></a>Grupas pārskata dzēšana

1. Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.
2. Ar peles labo pogu noklikšķiniet uz dzēšamās atskaišu grupas un pēc tam atlasiet vienumu **Dzēst**.
3. Kad tiek parādīts apstiprinājuma ziņojums, noklikšķiniet uz **Jā**.

## <a name="report-group-tab-controls"></a>Atskaišu grupas cilnes vadīklas
Nākamajā tabulā ir aprakstītas vadīklas cilnē **Atskaišu grupa**.

<table>
<thead>
<tr>
<th>Kontrole</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr>
<td>Atsevišķu pārskatu definīcijās ignorēt uzņēmuma, detalizētas informācijas un datuma iestatījumus</td>
<td>Atlasiet šo izvēles rūtiņu, lai ignorētu atsevišķu pārskatu definīcijas šajā pārskata grupā, tikai šo pārskatu veidošanai.</td>
</tr>
<tr>
<td>Uzņēmuma nosaukums</td>
<td>Atlasiet kompāniju, kas jāizmanto pārskatos.</td>
</tr>
<tr>
<td>Detalizācijas līmenis</td>
<td>Norādiet detalizētības līmeni, kāds ir iekļauts atskaitēs.
<ul>
<li><strong>Finanšu</strong> — augstākā līmeņa kopsavilkuma pārskats. Nevara&#39;t detalizēti skatīt kontus un dimensijas, izņemot tos kontus un dimensijas, kas ir pievienoti, izmantojot pārskatu koku.</li>
<li><strong>Finanšu &amp; Konts</strong> — pārskats, kas satur augsta līmeņa kopsavilkumu un detalizētu informāciju par kontu.</li>
<li><strong>Finanšu, Konts, &amp; Transakcija</strong> — pārskats, kas satur augsta līmeņa kopsavilkumu un detalizētu informāciju par transakciju.</li>
</ul></td>
</tr>
<tr>
<td>Provizorisks</td>
<td>Norādiet aktivitāšu tipus, kas ir iekļauti atskaitēs.
<ul>
<li><strong>Tikai grāmatotās darbības</strong> — ietverti tikai darījumi un bilances, kas ir grāmatoti jūsu finanšu datos.</li>
<li><strong>Grāmatotās un negrāmatotās darbības</strong> — ietverti visi darījumi un bilances, kas ir ievadīti un grāmatoti jūsu finanšu datos.</li>
<li><strong>Tikai negrāmatotās darbības</strong> — ietverti tikai tie darījumi, kuri ir ievadīti, bet vēl nav iegrāmatoti jūsu finanšu datos.</li>
</ul></td>
</tr>
<tr>
<td>Iekļaut visas pārskatu veidošanas valūtas</td>
<td>Šeit ir norādītas visas papildu pārskatu valūtas, kas ir konfigurētas jūsu Microsoft Dynamics ERP sistēmā. Atzīmējiet šo izvēles rūtiņu, lai ģenerētu papildu atskaites norādītajās valūtās. Lai skatītu šos pārskatus, pakalpojumā Tīmekļa skatītājs noklikšķiniet uz pogas <strong>Valūta</strong> un pēc tam atlasiet valūtu.</td>
</tr>
<tr>
<td>Datuma informācija netiek saglabāta ar pārskata definīciju</td>
<td><ul>
<li>Bāzes periods</li>
<li>Bāzes gads</li>
<li>Ietvertais periods</li>
</ul>
Ar atskaites definīciju tiek saglabāti tikai noklusējuma bāzes perioda iestatījumi.</td>
</tr>
<tr>
<td>Datuma informācija tiek saglabāta ar pārskata definīciju</td>
<td><ul>
<li>Pārskata datums</li>
<li>Noklusējuma bāzes periods</li>
</ul></td>
</tr>
<tr>
<td>Pārskati grupā</td>
<td>Pievienot, noņemt un atkārtoti pasūtīt pārskatus pārskata grupā.
<ul>
<li>Lai pārskatu grupai pievienotu pārskatu definīcijas, atveriet pārskatu grupu, veicot dubultklikšķi uz tās, un pēc tam noklikšķiniet uz <strong>Pievienot</strong>. Atlasiet pārskatu grupai pievienojamos pārskatus un pēc tam noklikšķiniet uz <strong>Labi</strong>.</li>
<li>Lai no pārskatu grupas noņemtu pārskatu, atlasiet vēlamo pārskatu un pēc tam noklikšķiniet uz <strong>Noņemt</strong>.</li>
<li>Lai mainītu secību, kādā atskaites tiek ģenerētas, sarakstā atlasiet kādu atskaiti un pēc tam noklikšķiniet uz <strong>Pārvietot uz augšu</strong> vai <strong>Pārvietot uz leju</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Papildu resursi

[Finanšu pārskatu veidošana](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]