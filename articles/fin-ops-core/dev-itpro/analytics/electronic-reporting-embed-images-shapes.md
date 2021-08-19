---
title: Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER
description: Šajā tēmā skaidrots, kā izmantot Elektronisko pārskatu rīku, lai ģenerētu biznesa dokumentus, kam ir iegulti attēli un formas.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 550ecca31af48e624e292b342d909abd6eb3e87af122f736eb388524b42f1e05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730639"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER

[!include [banner](../includes/banner.md)]

Jūs varat izmantot Elektronisko pārskatu veidošanas (ER) rīku, lai projektētu pārskatus, ko varat palaist, lai izveidotu nepieciešamos elektroniskos dokumentus. Var izmantot Microsoft Excel vai Microsoft Word dokumentus, lai noteiktu pārskata izkārtojumu. ER operāciju veidotājs ļauj jums pievienot Excel vai Word dokumentu kā veidni pārskatam. Pievienotajā veidnē, nosauktie elementi ir saistīti ar pārskata elementiem. Pārskata formāta elementi ir saistīti ar datu avotiem. Šie elementi norāda datus, kas izpildlaikā tiks ievadīti ģenerētajos dokumentos.

Šī jaunā funkcionalitāte pārsniedz esošās ER iespējas dokumentu izveidošanai Microsoft Office formātos. Lai iegūtu papildinformāciju, atskaņojiet šīs uzdevumu rokasgrāmatas. Šīs uzdevumu ceļvežus varat atrast biznesa 7.5.4.3 Iegūt/izstrādāt IT pakalpojumu/risinājumu komponentus (10677).

- ER Izveidot konfigurāciju atskaišu ģenerēšanai formātā OPENXML
- ER Konfigurācijas noformēšana atskaišu ģenerēšanai formātā Microsoft WORD

## <a name="embed-an-image-in-an-excel-document"></a>Attēla iegults Excel dokumentā

### <a name="embed-an-image-in-an-excel-worksheet"></a>Attēla iegults Excel darblapā

Vispirms Excel dokumentā attēlam ir jāpievieno vietturis. Atveriet Excel darbgrāmatu un pievienojiet attēlu kā tā attēla vietturi, kuru pievienosiet vēlāk. Pēc tam izmantojiet ER rīku, lai pievienotu jaunu ER formāta konfigurāciju un ietvertu pārskatu, kuru izprojektējat. Pievienojiet Excel darbgrāmatu kā veidni pārskata formātam un pēc tam importējiet darbgrāmatas saturu ER formātā. Formāta definīcija tiks izveidota automātiski. Pievienotais attēla vietturis tiks iekļauts ER formāta definīcijā kā elements **ŠŪNA**.

> [!NOTE]
> Varat manuāli norādīt formāta definīciju, nevis importēt to. Saglabājot izmaiņas, formāts tiks validēts.

Pēc tam saistiet ER formāta **ŠŪNA** binārajā formātā. Ja ER datu modelis tiek izmantots kā formāta datu avots, lauka datu tipam ir jābūt [Konteiners](er-formula-supported-data-types-composite.md#container). Pašlaik ER datu modeļa lauks, kam ir datu tips [Konteineris](er-formula-supported-data-types-composite.md#container), var tikt piesaistīts vairākiem datu avotu tipiem, kas atgriež attēlus binārajā formātā. Jūs varat piekļūt laukam datu tabulā un failam, kas ir pievienots datu tabulas ierakstam, izmantojot Dokumentu vadības struktūru.

> [!IMPORTANT]
> - Ja vēlaties aizpildīt attēla vietturi dokumentā, kuru veidojat, izmantojot Excel veidni, ER formātā ir jāietver elements **ŠŪNA**, kas attiecas uz nosaukto attēla elementu Excel veidnē. Pretējā gadījumā pārskata izvadē netiks rādīts attēla vietturis. Ja **ŠŪNA** elementa saistīšana izpildlaikā atgriež nekādus datus, izveidotais dokuments rādīs attēla vietturi no veidnes. Lai paslēptu attēlu dokumentu, ko ģenerējiet, definējiet elementu **ŠŪNA** un norādiet, ka izteiksmei izteiksmei **Iespējošana** jāatgriež vērtība **NEPATIESS**.
> - Excel veidnē katram elementam izmantojiet unikālu nosaukumu. Šie elementi ietver attēlus un šūnas. Ja elementa nosaukuma dublikāts, ģenerētā pārskata saturs būs neskaidrs un neskaidrs.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Iegult attēlus Excel darblapas galvenē un kājenē

Izmantojiet Excel darbgrāmatas dokumentu kā veidni, lai norādītu pārskata izkārtojumu. Darbgrāmatā var būt vairākas darblapas, katra no tām var būt veidota tā, lai tai būtu virsraksts un kājene. Excel atbalsta līdz trim attēliem katras darblapas galvenē un kājenē. Attēlus var izlīdzināt pa kreisi, pa labi vai centrēt.

Finanšu laidienā 10.0.21 varat pārvaldīt virsrakstu un kājenes attēlus, kas tiek ģenerēti ar ER risinājumu, kam ir Excel veidne.

Ja vēlaties, lai ģenerētā dokumenta galvenē vai kājenē tiktu parādīts noklusējuma attēls, varat pievienot attēlu ER veidnes darblapas galvenei vai kājenei. Lai piekļūtu šim attēlam ER formātā, jāpievieno komponents **Attēls** formāta [Virsraksta](er-fillable-excel.md#header-component) vai [Kājenes](er-fillable-excel.md#footer-component) komponentam. Pēc vajadzības konfigurējiet komponenta **Attēls** līdzinājumu. 

Varat izmantot arī komponentu **Attēls**, lai izveidotu attēlu izpildlaikā ģenerētā dokumenta galvenē vai kājenē, pat ja veidnē nav noklusējuma attēla. Lai norādītu multivides saturu, kas jāliek ģenerētā dokumenta galvenē vai kājenē vai nu kā jauns attēls, vai kā noklusējuma attēla aizstājējs, jums ir jāpiesaista komponents **Attēls** tā [Konteinera](er-formula-supported-data-types-composite.md#container) tipa datu avotam, kas attēlo attēlu binārajā formātā.

Katram **Virsraksta** vai **Kājenes** komponentam var būt viens **Attēla** komponents katram atbalstītais līdzinājums: **Pa kreisi**, **Centrs** un **Pa labi**.

Komponenta **Attēls** rekvizīts **Augstuma mērogs** ļauj izmantot konfigurēto saistīšanu, lai kontrolētu attēla lielumu:

- Atlasiet **Sākotnējais**, lai saglabātu attēla sākotnējo lielumu.
- Atlasiet attiecībā pret attēla augstuma skalu **Proporcionāli** virsraksta vai kājenes augstumam, kas ietver šo attēlu.

    - Šādā gadījumā attēla augstums jādefinē kā vecākelementa galvene vai kājenes procentuālā vērtība.
    - Ja mērogošanas vērtība pārsniedz 100 procentus, attēls var pārklāties ar atbilstošās darblapas datu apgabalu.
    - Ja, izmantojot mērogošanu, tiek mainīts attēla augstums, tiek mainīts arī platums, lai uzturētu attēla sākotnējo proporcijas koeficientu.

- Atlasiet **Absolūts**, lai mainītu attēla izmēru atbilstoši augstuma un platuma vērtībām (pikseļos), kas tiek nodrošināti izstrādes laikā.

    - Ja norādītais augstums pārsniedz pamata virsraksta vai kājenes augstumu, attēls var pārklāties ar attiecīgās darblapas datu apgabalu.

Lai kontrolētu tā attēla redzamību, kas ievietots ģenerētajā dokumentā, izmantojot šo komponentu, var izmantojot arī komponenta **Attēls** rekvizītu **Iespējots**.

> [!NOTE]
> Lai rediģējamam ER formātam pievienotu komponentu **Attēls**, jālieto ER formāta veidotājs. Komponentu nevar pievienot, ja izmantojat darbvietu [Biznesa dokumentu pārvaldība](er-business-document-management.md), lai rediģētu biznesa dokumenta veidni.

Lai uzzinātu vairāk par šo funkcionalitāti, izpildiet darbības sadaļā [ER formāta izstrāde, lai izveidotu pārskatu Excel formātā ar iegultiem attēliem lapas galvenēs vai kājenēs](er-embed-images-header-footer-excel-reports.md).

## <a name="embed-a-shape-in-an-excel-document"></a>Iegult figūru Excel dokumentā

Vispirms Excel dokumentā figūrai ir jāpievieno vietturis. Atveriet Excel darbgrāmatu un izvēlieties **Figūra**, **Teksta lodziņš** vai **WordArt** kā vietturi fugūrai. Pēc tam izmantojiet ER rīku, lai pievienotu jaunu ER formāta konfigurāciju un ietvertu pārskatu, kuru izprojektējat. Pievienojiet Excel darbgrāmatu kā veidni pārskata formātam un pēc tam importējiet darbgrāmatas saturu ER formātā. Formāta definīcija tiks izveidota automātiski. Jūsu pievienotais vietturis tiks iekļauts ER formāta definīcijā kā elements **ŠŪNA**, kas attiecas uz nosaukto Excel formu elementu.

> [!NOTE]
> Varat manuāli norādīt formāta definīciju, nevis importēt to. Saglabājot izmaiņas, formāts tiks validēts.

Pēc tam saistiet elementu **ŠŪNA** ER formātā laukam no formāta datu avota, kas nodrošina datus izpildes laikā. Šos datus var konvertēt teksta virknē. Ja elements **ŠŪNA** ER formātā attiecas uz formu elementu Excel veidnē, kas atbalsta tekstu, teksts, kas ir nodrošināts, izpildlaikā izmantojot šo saistīšanu, tiks rādīts formā, kas ir ģenerētajādokumentā.

> [!IMPORTANT]
> - Ja vēlaties izmantot Excel veidni, kas ietver formu vietturi, lai ģenerētu jaunu dokumentu, ER formātam jāsatur elements **ŠŪNA**, kas attiecas uz Excel formu elementu. Pretējā gadījumā pārskata izvadē netiks rādīts figūras vietturis. Ja elementa **ŠŪNA** saistīšana, kas attiecas uz nosaukto Excel formu elementu, izpildlaikā neatgriež datus, ģenerētais dokuments parādīs formu viettura tekstu no Excel veidnes. Lai paslēptu figūras dokumentu, ko ģenerējiet, definējiet elementu **ŠŪNA**, kas attiecas uz nosaukto Excel figūras elementu, un norādiet, ka izteiksmei izteiksmei **Iespējošana** jāatgriež vērtība **NEPATIESS**.
> - Excel veidnē katram elementam izmantojiet unikālu nosaukumu. Šie elementi ietver figūras un šūnas. Ja elementa nosaukuma dublikāts, ģenerētā pārskata saturs būs neskaidrs un neskaidrs.

## <a name="embed-an-image-in-a-word-document"></a>Attēla iegults Word dokumentā
> [!IMPORTANT]
> Varat atkārtoti izmantot ER formātu, kas izmanto Excel veidni, lai izveidotu dokumentus, kas ietver iegultos attēlus. ER formātā pārliecinieties, vai elementam **ŠŪNA**, kas attiecas uz nosauktu attēla elementu programmā Excel, ir norādīts nosaukums un tas ir piesaistīts datu avotam, kas izpildlaikā atgriež attēlu.

Vispirms jākonfigurē Word dokumenta izkārtojums. Izmantojiet vadīklu **Attēla saturs**, lai iegultam attēlam izveidotu vietturi. Lai piekļūtu šai kontrolei, Word lentes vispirms jāredz cilne **Izstrādātājs**.

Pēc tam dzēsiet Excel veidni no ER formāta un pievienojiet Word veidnes dokumentu. Atjauniniet atsauci uz veidni un saglabājiet izmaiņas. Pašreizējā ER formāta struktūra tiek saglabāta uz Word dokumenta veidni kā jauna pielāgota XML daļa ar nosaukumu **Pārskats**.

Pēc tam saglabājiet Word veidni pašreizējam ER formātam lokālajā datorā. Atveriet veidni un atveriet rūti **XML kartēšana**. Atrodiet pielāgoto XML daļu ar nosaukumu **Pārskats** un pēc tam norādiet uz elementu **ŠŪNA** ER pārskatā, kas ir piesaistīts datu avotam, kas atgriež attēlu binārā formātā. Kartējiet šīs XML daļas elementu ar atlasīto vadīklu **Attēla satura** un saglabājiet izmaiņas.

[![iegult attēlus.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Visbeidzot izdzēsiet Word veidni no ER formāta un pievienojiet Word dokumentu, kas ietver kartētās pielāgotās XML daļas. Atjauniniet formāta atsauci uz veidni un saglabājiet izmaiņas, ko veicāt šajā ER formātā.

## <a name="more-information"></a>Papildinformācija
Lai uzzinātu šīs funkcijas detaļas, jumiet uzdevumu ceļvežu kopas, **ER Veidot pārskatus MS Office formātos ar iegultiem attēliem**. Šīs uzdevumu ceļveži parāda, kā var iegult uzņēmuma logotipa un pilnvarotas personas paraksta attēlus maksājumu čekā, kas tiek ģenerēti, izmantojot ER rīku Excel un Word dokumentos.

Šajā tabulā uzskaitīti faili, kas nepieciešami, lai pabeigtu **ER Veidot pārskatus MS Office formātos ar iegultiem attēliem** uzdevumu ceļvežiem. Lejupielādējiet un saglabājiet failu vietējā datorā.

| Apraksts                                          | Faila nosaukums                   |
|------------------------------------------------------|-----------------------------|
| ER datu modeļa konfigurācija                          | [cheques.xml modelis](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER formāta konfigurācija                              | [Čeku drukāšanas formāts.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Uzņēmuma logo attēls                                   | [Uzņēmuma logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Paraksta attēls                                      | [Paraksta attēls.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternatīva paraksta attēls                          | [Paraksta attēls 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word veidne maksājumu čeku drukāšanai  | [Čeka veidne Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| Microsoft Excel veidne maksājumu čeku drukāšanai | [Čeka veidne.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

Šajā grafikā sniegts no Excel veidnes ģenerēta maksājuma pārbaudes izdrukas piemērs.

[![Maksājuma pārbaudes testa izdruka.](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
