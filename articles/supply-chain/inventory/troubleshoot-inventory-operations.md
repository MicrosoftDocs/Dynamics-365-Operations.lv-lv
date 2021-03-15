---
title: Krājumu problēmu novēršanas operācijas
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar krājumu darbībām.
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3a22229106753d265a90f0ef05f5ac82dc745bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967159"
---
# <a name="troubleshoot-inventory-operations"></a>Krājumu problēmu novēršanas operācijas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar krājumu darbībām.

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Nevar atrast nolaižamo dialoglodziņu Darbplūsma krājumu žurnāliem.

### <a name="issue-description"></a>Problēmas apraksts

Žurnāla lapā nevar atrast **Darbplūsmas** nolaižamo dialoglodziņu, vai arī saistītās darbplūsmas operācijas nav pieejamas.

Šī problēma var rasties trīs iemeslu dēļ, kā aprakstīts tālāk aprakstītajās apakšsadaļās.

### <a name="issue-resolution-1"></a>1. problēmas risinājums

Ja problēma attiecas uz visiem lietotājiem, var rasties, jo apstiprināšanas darbplūsma nav piešķirta žurnāla nosaukumam. Lai novērstu problēmu, izpildiet šīs darbības.

1. Dodieties uz **Krājumu pārvaldība &gt; Iestatīšana &gt; Žurnālu nosaukumi &gt; Krājumi**.
1. Atlasiet žurnāla nosaukumu no saraksta kolonnas, lai atvērtu tās iestatījumu lapu.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Darbplūsmas apstiprināšana** uz *Jā*. Atlasiet **Jā**, ja jums tiek piedāvāts apstiprināt izmaiņās.
1. Laukā **Darbplūsma** atlasiet izdevumu pārskatītāju konfigurāciju, kuru vēlaties izmantot šim atlasītajam žurnāla nosaukumam.

### <a name="issue-resolution-2"></a>2. problēmas risinājums

Ja darbplūsma izmanto pielāgotu kodu, pēc sistēmas jaunināšanas var rasties problēmas. Piemēram, žurnāla darbplūsmā poga **Iesniegt** var būt pelēkota, tāpēc jūs nevarat to atlasīt, lai apstiprinātu iesniegšanu.

Ja poga **Iesniegt** ir iepelēkota, iespējams, ka darbplūsma ir pielāgota, kas nozīmē darbplūsmas metodi, sadaļā `canSubmitToWorkflow()`ir `FormDataUtil`paplašināta. Lai novērstu šo problēmu, mainiet veidu, kā paplašināt metodes `canSubmitToWorkflow()`struktūras izmantošanai šajā piemērā.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>3. problēmas risinājums

Ja problēma attiecas tikai uz dažiem specifiskiem lietotājiem, iespējams, šiem lietotājiem nav drošības privilēģiju, kas nepieciešamas darbplūsmas operāciju palaišanai krājumu žurnālos. Pārbaudiet, vai katram ietekmētam lietotājam ir drošības privilēģija *Uzturēt krājumu žurnāla darbplūsmu*. Pēc noklusējuma šī privilēģija tiek piešķirta pienākumam ar tādu pašu nosaukumu un šis pienākums tiek attiecināts uz lomām *Noliktavas darbinieks* un *Noliktavas vadītājs*.

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>Mans krājumu žurnāls paliek sistēmas bloķētā statusā un darbplūsmas pakešuzdevums nedarbojas.

### <a name="issue-description"></a>Problēmas apraksts

Kādu no jūsu krājumu žurnāliem ir bloķējusi kāda operācija un tā nav nodota izpildei. Piemēram, ja grāmatošanas laikā rodas nezināma kļūda (kas ir sistēmas bloķēšanas operācija), žurnālam var būt sistēmas bloķēts statuss. Šajā gadījumā darbplūsmas darba vienuma apdarinātājam rodas kļūda, bloķējot validāciju.

### <a name="issue-resolution"></a>Problēmas risinājums

Piesakieties SQL Server instancē Supply Chain Management un pārbaudiet, vai **InventJournalTable.SystemBlocked** ir iestatīts uz *1*. Pārliecinieties, vai žurnāla statuss nav bloķēts, un pēc tam atiestatiet **InventJournalTable.SystemBlocked** uz *0*.

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>Mana krājumu žurnāla darbplūsma nekad netiek pabeigta, un žurnālu nevar rediģēt vai grāmatot.

### <a name="issue-description"></a>Problēmas apraksts

Kad esat iesniedzis žurnāla apstiprināšanas darbplūsmu, darbplūsmas apstrāde pārstāj reaģēt un jūs nevarat rediģēt vai apstrādāt žurnālus.

### <a name="issue-resolution"></a>Problēmas risinājums

Ir vairāki iemesli, kādēļ darbplūsmas apstrāde var nebūt pabeigta. Pārbaudiet šādas problēmas:

- Dodieties uz **Krājumu pārvaldība &gt; Iestatījumi &gt; Krājumu pārvaldības darbplūsmas** un pārskatiet ietekmētās darbplūsmas konfigurāciju. Papildinformāciju skatiet [Krājumu žurnāla apstiprināšanas darbplūsmas](inventory-journal-workflow.md).
- Darbplūsma, iespējams, var saskarties ar izņēmumu vai kļūdu. Pārskatiet ietekmētās darbplūsmas darba vienuma vēsturi, lai redzētu, vai tā ietver lietojumprogrammas kļūdu, kas pārtrauc darbplūsmu.
- Krājumu žurnālu var atjaunināt vai rediģēt tikai tad, ja tas ir apstiprināts. Ja atsaukšana ir aktīva, varat mēģināt atsaukt žurnālu. Darbplūsmas pakešuzdevuma izpilde var tikt pārtraukta vairāku iemeslu dēļ. Daži no šiem iemesliem, iespējams, ir radušies darbplūsmas struktūras problēma.

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>Krājumu žurnāla darbplūsmas nosacījumi attiecas tikai uz žurnāla līmeni, nevis rindu līmeni

### <a name="issue-description"></a>Problēmas apraksts

Jums var rasties šī problēma, ja, piemēram, mēģināt iestatīt krājumu žurnāla darbplūsmas nosacījumu izmaksu summai. Iestatiet nosacījumu tā, ka 1. solis tiek palaists tikai tad, ja izmaksu summa ir mazāka par 100. Iestatiet nosacījumu tā, ka 2. solis tiek palaists tikai tad, ja izmaksu summa ir lielāka vai vienāda ar 100. Pēc tam, kad darbplūsma darbojas, darbplūsmas vēsture rāda tikai vienu rindu, un pirmais nosacījums vienmēr tiek novērtēts kā *patiess* neatkarīgi no iesniegtās vērtības.

### <a name="issue-workaround"></a>Problēmas aprisinājums

Esošajā laidienā krājumu darbplūsmas nosacījumi attiecas tikai uz žurnāla līmeni, nevis rindu līmeni. Tas tiek darīts ar nolūku. Nosacījuma kritērijus ieteicams iestatīt tikai žurnāla līmeņa atribūtiem.

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>Filtra rūts rīcībā esošo krājumu saraksta lapā nefiltrē rezultātus, kā paredzēts.

### <a name="issue-description"></a>Problēmas apraksts

Filtra rūts filtri **Rīcībā esošo krājumu saraksta** lapā nefiltrē rezultātus, kā paredzēts.

### <a name="issue-resolution"></a>Problēmas risinājums

Tas tiek darīts ar nolūku.

 **Rīcībā esošo krājumu saraksta** lapa tiek apkopota no detalizētas rīcībā esošo krājumu tabulas, kas ietver visas pieejamās dimensijas. Tomēr saraksts šajā lapā ir kopsavilkums. Tāpēc tā var apvienot rindas no avota tabulas, apkopojot vērtības atbilstoši parādītajām dimensijām.

Filtri, ko iestatāt Filtru rūtī, attiecas uz avota tabulu, nevis uz apkopoto sarakstu. Dažreiz šī uzvedība var radīt neparedzētus rezultātus, kā parādīts [šajos piemēros](inventory-on-hand-list.md#examples).

Tomēr  [režģī sniegtie filtri](inventory-on-hand-list.md#grid-filters) *attiecas* uz apkopoto sarakstu. Šie filtri ietver gan QuickFilter režģa augšpusē, gan katra kolonnas virsraksta filtru.

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Krājumu žurnālā mērvienības un mērvienību daudzums nedarbojas pareizi.

### <a name="issue-description"></a>Problēmas apraksts

Strādājot ar mērvienībām un daudzumiem krājumu žurnālā, varat saskarties ar vienu vai abiem šiem jautājumiem:

- Jūs krājuma žurnālā neredzat mērvienības vai vienību daudzumus, kamēr izlaistai precei ir iestatīta pārvēršanas mērvienība, un krājumu žurnālā nevarat mainīt šo mērvienību.
- Krājumu žurnālā ir redzami lauki **Daudzums** un **Mērvienība**, taču nav redzams lauks **Mērvienības daudzums**. Mainot mērvienību, ievadiet daudzumu un grāmatojiet žurnālu, žurnālā joprojām tiek parādīta sākotnējā mērvienība šim daudzumam.

### <a name="issue-resolution"></a>Problēmas risinājums

Lai novērstu šo problēmu, izpildiet sekojošās darbības.

1. **Līdzekļu pārvaldības** darbvietā pārliecinieties, vai krājumu žurnālu līdzekļa funkcija *Izmanto mērvienību un mērvienību daudzumu* ir ieslēgta. Ar šo žurnālam tiek pievienots lauks **Mērvienība** un **Mērvienības daudzums**.
1. Kad funkcija ir ieslēgta, lietojiet lauku **Daudzums**, **Mērvienības daudzums** un **Mērvienība** šādā veidā:

    - **Daudzums** – norādiet daudzumu, izmantojot izpildei nodotai precei noteikto noklusējuma mērvienību. Tomēr noklusētā mērvienība šeit netiek rādīta. Ja ir iestatīta pārvēršana starp noklusējuma mērvienību un laukā **Mērvienība** atlasīto vienību, lauks **Daudzums** tiek automātiski atjaunināts, pamatojoties uz lauku **Mērvienība** un **Mērvienības daudzums** atlasi.
    - **Mērvienības daudzums** - norādiet daudzumu, izmantojot laukā **Mērvienība** atlasīto mērvienību.
    - **Mērvienība** – atlasiet mērvienību, ko piemērot vērtībai laukā **Mērvienības daudzums**.

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Saņemu šādu kļūdas ziņojumu: "Maksimālais decimāldaļu skaits noliktavas mērvienībai ir 0."

### <a name="issue-description"></a>Problēmas apraksts

Mēģinot grāmatot krājumu darbību vai krājumu rezervēšanu, tiek saņemts šāds kļūdas ziņojums: "Maksimālais decimāldaļu skaits noliktavas mērvienībai ir 0."

Šī problēma rodas, ja krājumu darbības daudzums ir norādīts kā decimālskaitļa vērtība, kas ir zem precizitātes līmeņa, ko lauks atbalsta. Piemēram, krājuma darbībai norādīts daudzums *0,5*, bet tiek atbalstīti tikai veseli skaitļi. Tāpēc vērtībai ir jābūt *1*, nevis *0,5*.

### <a name="issue-resolution"></a>Problēmas risinājums

1. Lai krājumu darbībās noapaļotu daudzumus, palaidiet SQL Server instancē šādu skriptu. Šis skripts izlabos vērtības tabulā **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Palaidiet rīcībā esošo konsekvences pārbaudi, ja ir ieslēgta opcija **labot kļūdas**. Šis skripts izlabos vērtības tabulā **inventSum**.

> [!IMPORTANT]
> Ir stingri ieteicams rūpīgi rediģēt skriptu, kā tas nepieciešams jūsu videi, pārbaudīt to pārbaudes vidē un pēc tam pārbaudīt iegūtos datus pirms skripta palaišanas ražošanas vidē.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]