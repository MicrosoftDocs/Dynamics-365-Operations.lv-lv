---
title: Pievienot jaunus laukus biznesa dokumenta veidnei Microsoft Excel
description: Šajā tēmā sniegta informācija par to, kā pievienot jaunus laukus biznesa dokumenta veidnei Microsoft Excel, izmantojot biznesa dokumentu pārvaldības līdzekli.
author: NickSelin
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 57eebdc38fb3f74690b92c03fa60e10c7610db1fe413320a6d167f05b0658bf1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767246"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Pievienot jaunus laukus biznesa dokumenta veidnei Microsoft Excel

[!include[banner](../includes/banner.md)]

Jūs varat pievienot jaunus laukus veidnei, kas tiek izmantota, lai izveidotu biznesa dokumentus Microsoft Excel formātā. Šos laukus var pievienot kā vietturus, kas tiek izmantoti, lai aizpildītu ģenerētos dokumentus ar nepieciešamo informāciju no programmas. Katram laukam, ko pievienojat, varat arī norādīt saistījumu ar datu avotiem, lai norādītu, kādi programmas dati tiks ievadīti laukā, kad veidne tiek lietota biznesa dokumentu ģenerēšanai.

Lai iegūtu papildinformāciju par šo līdzekli, aizpildiet šajā tēmā sniegto piemēru. Šajā piemērā ir parādīts, kā atjaunināt veidni, lai aizpildītu laukus brīvā teksta rēķina veidlapās, kas tiek veidotas.

## <a name="configure-business-document-management-to-edit-templates"></a>Biznesa dokumentu pārvaldības konfigurēšana veidņu rediģēšanai

Tā kā biznesa dokumentu pārvaldība (BDP) ir veidota papildus [Elektronisko paziņojumu (EP) pārskatu](general-electronic-reporting.md) sistēmai, pirms varat sākt strādāt ar BDP, ir jākonfigurē obligātie EP un BDP parametri.

1.  Piesakieties Microsoft Dynamics 365 Finance instancei kā sistēmas administrators.
2.  Veiciet šādas darbības no piemēra tēmā [Biznesa dokumentu pārvaldības pārskats](er-business-document-management.md):

    1.  Konfigurējiet ER parametrus.
    2.  Ieslēdziet BDP.

Tagad varat sākt izmantot BDP, lai rediģētu biznesa dokumentu veidnes.

## <a name="import-er-solutions-that-contain-a-template"></a>Importēt EP risinājumus, kas satur veidni

Šīs procedūras piemērā tiek izmantots oficiāli publicētais EP risinājums. Jums ir jāimportē šī risinājuma EP konfigurācijas jūsu pašreizējā Finance instancē.

**Brīvā teksta rēķina (Excel)** EP formāta konfigurācija šajā risinājumā ietver biznesa dokumenta veidni Excel formātā, ko var rediģēt, izmantojot BDP. Importējiet šīs EP formāta konfigurācijas jaunāko versiju no Microsoft Dynamics Lifecycle Services (LCS). Atbilstošais EP datu modelis un EP modeļu kartēšanas konfigurācijas tiks importētas automātiski.

Lai iegūtu papildinformāciju par EP konfigurāciju importēšanu, skatiet sadaļu [EP konfigurācijas dzīves cikla pārvaldība](general-electronic-reporting-manage-configuration-lifecycle.md).

![LCS koplietojamo līdzekļu bibliotēkas lapa.](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>Rediģēt EP risinājuma veidni

1.  Pierakstieties kā lietotājs ar piekļuvi darbvietai **Biznesa dokumentu pārvaldība**
2.  Atveriet darbvietu **Biznesa dokumentu pārvaldība**

    ![Biznesa dokumentu pārvaldības darbvieta.](./media/BDM-AddFldExcel-Workspace.png)

3.  Režģī atlasiet veidni **Brīvā teksta rēķins (Excel)**.
4.  Labajā rūtī atlasiet **Jauna veidne**, lai izveidotu jaunu veidni, kas ir balstīta uz atlasīto veidni.
5.  Laukā **Nosaukums** ievadiet **Brīvā teksta rēķins (Excel) Contoso** kā jaunās veidnes nosaukumu.
6.  Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.

Parādīsies BDP veidnes redaktora lapa. Var lietot Microsoft 365, lai rediģētu atlasīto veidni tiešsaistē iegultajā vadīklā.

![BDP veidnes redaktora lapa.](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>Pievienot etiķeti jaunam laukam veidnē

1.  BDP veidņu redaktora lapā, Excel lentē cilnē **Skats** atlasiet rediģējamās Excel veidnes izvēles rūtiņas **Virsraksti un režģlīnijas.**

    ![Atzīmētas izvēles rūtiņas Virsraksti un režģlīnijas.](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  Atlasiet šūnas **E8: F8**.
3.  Excel lentē, cilnē **Sākums** atlasiet **Sapludināt un centrēt**, lai sapludinātu atlasītās šūnas jaunajā sapludinātā **E8: F8** šūnā.
4.  Sapludinātajā šūnā **E8: F8** ievadiet **URL**.
5.  Atlasiet sapludināto šūnu **E7:F7**, atlasiet **Formāta kopētājs**, tad atlasiet sapludināto šūnu **E8:F8** tādā pašā veidā, kā sapludināto šūnu **E7:F7**.

    ![Veidnei pievienota jauna lauka etiķete.](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>Veidnes formatēšana, lai rezervētu vietu jaunam laukam

1.  Lapā BDP veidnes redaktora lapā atlasiet sapludināto šūnu **G8: H8.**
2.  Excel lentē, cilnē **Sākums** atlasiet **Sapludināt un centrēt**, lai sapludinātu atlasītās šūnas jaunajā sapludinātā **G8: H8** šūnā.
3.  Atlasiet sapludināto šūnu **G7:H7**, atlasiet **Formāta kopētājs**, tad atlasiet sapludināto šūnu **G8:H8** tādā pašā veidā, kā sapludināto šūnu **G7:H7**.

    ![Jaunajam laukam rezervētā vieta.](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  Laukā **Nosaukums** atlasiet **CompanyInfo.**

    Pašreizējās **Excel** veidnes CompanyInfo diapazons ietver visus laukus, kas tiek izmantoti, lai aizpildītu ģenerētā pārskata galveni ar detalizētu informāciju par pašreizējo uzņēmumu kā pārdevēja pusi.

    ![Atlasīts CompanyInfo diapazons.](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>Pievienot veidnei jaunu lauku

1.  **BDP veidnes redaktora** lapā, darbības rūtī atlasiet **Rādīt formātu**.
2.  Rūtī **Veidnes struktūra** atlasiet **Pievienot**.

    > [!NOTE]
    > Jums ir jāpielāgo tā veidnes sadaļa, ko vēlaties izmantot kā jaunu lauku. Jūs jau veicāt šo pielāgojumu, formatējot sapludināto šūnu **G8:H8**.

    ![Jauna lauka pievienošana veidnei.](./media/BDM-AddFldExcel-AddCell.png)

3.  Atlasiet **Excel\Cell**, lai pievienotu jaunu lauku kā šūnu veidnē.

    Varat atlasīt **Excel\Range**, ja vēlaties veidnei pievienot jaunu diapazonu. Ievadītajā diapazonā var būt vairākas šūnas. Šīs šūnas var pievienot vēlāk.
    
    Ņemiet vērā, ka **CompanyInfo** veidnes komponents tiek automātiski atlasīts rūtī **Veidnes struktūras**, jo tas ir vispiemērotākais pamatelements pašreizējās veidnes struktūrā laukam, kuru pievienojat.
    
4.  Laukā **Excel diapazons** ievadiet **CompanyURL_Value.**
5.  Atlasiet **Labi**.

    ![Veidnes struktūrai pievienotais CompanyURL_Value lauks.](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  Rūtī **Veidnes struktūras** atlasiet daudzpunktes pogu (...) un pēc tam atlasiet **Rādīt saistījumus**.

    ![Saistījumu atlasīšana parādīta.](./media/BDM-AddFldExcel-ShowBindings.png)

    Tagad rūtī **Veidnes struktūra** ir redzami datu avoti, kas ir pieejami pamata EP formātā.

7.  Atlasiet **CompanyInfo_Value** kā lauku, ko plānojat saistīt ar pamata EP formāta datu avotu.
8.  Rūts **Veidnes struktūra** sadaļā **Datu avoti** izvērsiet **Modelis \> InvoiceBase \> CompanyInfo.**
9.  Elementā **CompanyInfo** atlasiet vienumu **WebsiteURI**.

    ![Atlasīts vienums WebsiteURI.](./media/BDM-AddFldExcel-BindURL.png)

10. Atlasiet **Saistīt**.
11. Rūtī **Veidnes struktūra** atlasiet **Saglabāt** un pēc tam aizveriet BDP veidnes redaktora lapu.

Darbvietā **Biznesa dokumentu pārvaldība**, cilnes **Veidne** cilne labajā rūtī rāda atjaunināto veidni. Režģī ievērojiet, ka rediģētās veidnes lauks **Statuss** ir mainīts **Melnraksts**, un lauks **Pārskatījums** vairs nav tukšs. Šīs izmaiņas nozīmē to, ka šīs veidnes rediģēšanas process ir uzsākts.

![Rediģētā veidne biznesa dokumentu pārvaldības darbvietā.](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>Uzņēmuma iestatījumu pārskatīšana

1.  Dodieties uz **Organizācijas administrēšanas \> Organizācijas \> Juridiskās personas**.
2.  Kopsavilkuma cilnē **Kontaktinformācija** pārbaudiet, vai ir ievadīts uzņēmuma URL.

![Juridiskās personas lapā ievadītais uzņēmuma vietrādis URL.](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>Ģenerēt biznesa dokumentus, lai pārbaudītu atjaunināto veidni

1.  Programmā mainiet uzņēmumu uz **USMF** un dodieties uz **Debitoru parādi \> Rēķini \> Visi brīvā teksta rēķini.**
2.  Atlasiet rēķinu **FTI-00000002** un pēc tam atlasiet **Drukāšanas pārvaldība**.
3.  Kreisajā rūtī izvērtiet **Modulis - debitori \> Parādu dokumenti \> Brīvā teksta rēķins**.
4.  Sadaļā **Brīvā teksta rēķins**, atlasiet līmeni **Sākotnējais dokuments**, lai norādītu rēķinu tvērumu apstrādei.
5.  Labajā rūtī, laukā **Pārskata formāts** atlasiet veidni **Brīvā teksta rēķins (Excel) Contoso** norādītajam dokumenta līmenim.

    ![Atlasīta bezmaksas teksta Contoso veidne (Excel).](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  Nospiediet taustiņu **Esc**, lai aizvērtu pašreizējo lapu.
7.  Atlasīt **Drukāt \> Izvēlēts**.
8.  Lejupielādējiet ģenerēto dokumentu un atveriet to programmā Excel.

    ![Bezmaksas teksta rēķins programmā Excel.](./media/BDM-AddFldExcel-PreviewReport.png)

Modificētā veidne tiek izmantota, lai ģenerētu brīva teksta rēķina pārskatu atlasītajam vienumam. Lai analizētu, kā šo pārskatu ietekmēja jūsu ieviestās izmaiņas veidnē, varat palaist šo pārskatu vienā lietojumprogrammas sesijā uzreiz pēc tam, kad esat mainījis veidni citā lietojumprogrammas sesijā.

## <a name="related-links"></a>Saistītās saites

[Elektronisko ziņojumu (ER) pārskats](general-electronic-reporting.md)

[Biznesa dokumentu pārvaldības pārskats](er-business-document-management.md)

[Izveidot konfigurāciju atskaišu ģenerēšanai formātā OPENXML](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]