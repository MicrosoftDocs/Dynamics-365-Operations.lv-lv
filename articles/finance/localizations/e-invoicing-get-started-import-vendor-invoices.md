---
title: Izmantot elektronisko rēķinu izrakstīšanas pakalpojumu, lai importētu kreditora rēķinus
description: Šajā tēmā ir sniegta informācija, kā importēt kreditoru rēķinus, izmantojot Elektronisko rēķinu izrakstīšanas pakalpojumu.
author: gionoder
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 434bf1f6a5a727a71592493b85ab166cbeff2f0980c2c968c99973a03f4dc660
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751256"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Izmantot elektronisko rēķinu izrakstīšanas pakalpojumu, lai importētu kreditora rēķinus

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu importēšanu, izmantojot elektronisko rēķinu pakalpojumu. Tas jūs vadīs caur konfigurācijas soļiem Regulatory Configuration Services (RCS), Dynamics 365 Finance un Dynamics 365 Supply Chain Management, kas jums ir jāievēro, lai saņemtu elektroniskos kreditoru rēķinus no kreditoriem.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Kreditoru rēķinu importa iestatīšana RCS
Lai iestatītu kreditora rēķina importu RCS, sekojiet šiem soļiem:

1. Skatiet [vispārīgi pieejamo elektronisko rēķinu izrakstīšanas funkciju](e-invoicing-configuration-rcs.md#generally-available-features) sarakstu.
2. Atlasiet un importējiet elektronisko rēķinu izrakstīšanas līdzekli. Papildinformācija: skatiet [Importēt Elektronisko rēķinu izrakstīšanas līdzekli no Microsoft konfigurācijas nodrošinātāja](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
3. Izveidojiet Elektronisko rēķinu izrakstīšanas līdzekli jūsu organizācijā. Papildinformācija: skatiet [Izveidojiet Elektronisko rēķinu izrakstīšanas līdzekli jūsu organizācijas nodrošinātājā](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider).

## <a name="configure-an-email-account-channel"></a>Konfigurēt e-pasta konta kanālu

Konfigurējiet e-pasta konta kanālu, ja jūs izveidojāt Elektronisko rēķinu izrakstīšanas līdzekli, importē elektroniskos kreditora rēķinus no pievienotajiem failiem, kas tiek saņemti ar e-pastu.

1. RCS atlasiet jūsu izveidoto elektronisko rēķinu izrakstīšanas līdzekli. Pārliecinieties, vai ir atlasīta versija ar statusu **Melnraksts**.
2. Režģa cilnē **Iestatījumi** atlasiet funkcijas iestatījumus un pēc tam atlasiet **Rediģēt**.
3. Cilnē **Datu kanāls** lauku grupā **Parametri** atlasiet **Servera adrese** un ievadiet e-pasta konta nodrošinātāju.
4. Atlasiet **Servera portu** un ievadiet portu, ko izmanto e-pasta konta nodrošinātājs.
5. Atlasiet **Lietotājvārda noslēpumu** un ievadiet atslēgas noslēpuma vārdu, kas satur e-pasta lietotāja konta ID.
6. Atlasiet **Lietotāja paroles noslēpumu** un ievadiet atslēgas noslēpuma vārdu, kas satur e-pasta lietotāja konta paroli.
7. Atlasiet **Tēmu filtru**. Pārskatiet un atjauniniet virkni, kas ietver noklusējuma e-pasta tēmu, lai identificētu e-pastu, kas satur importējamā elektroniskā kreditora rēķinu.
8. Cilnē **Piemērojamības noteikumi** pārskatiet un atjauniniet kritērijus, ja nepieciešams. Papildinformāciju skatiet sadaļā [Piemērojamības noteikumi](e-invoicing-configuration-rcs.md#applicability-rules).
9. Atlasiet **Saglabāt** un aizveriet lapu.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Konfigurējiet Microsoft SharePoint kanālu

Konfigurējiet Microsoft SharePoint kanālu, ja elektronisko rēķinu izrakstīšanas līdzeklis importē elektroniskos kreditora rēķinus no SharePoint mapēs ievietotajiem failiem.

1. RCS atlasiet jūsu izveidoto elektronisko rēķinu izrakstīšanas līdzekli. Pārliecinieties, vai ir atlasīta **Versija** ar statusu **Melnraksts**.
2. Režģa cilnē **Iestatījumi** atlasiet funkcijas iestatījumus un pēc tam atlasiet **Rediģēt**.
3. Cilnē **Datu kanāls** lauku grupā **Parametri** atlasiet **SharePoint** adrese un ievadiet SharePoint URL.
4. Atlasiet **Servera portu** un ievadiet portu, ko izmanto e-pasta konta nodrošinātājs.
5. Atlasiet **Programmas ID** un ievadiet atslēgas noslēpuma vārdu, kas satur SharePoint lietotāja ID.
6. Atlasiet **Programmas noslēpums** un ievadiet atslēgas noslēpuma vārdu, kas satur SharePoint lietotāja paroli.
7. Atlasiet **Faila filtrs**. Pārskatiet un atjauniniet masku, lai filtrētu failus, kas ietver importējamu elektronisko kreditoru rēķinu.
8. Cilnē **Piemērojamības noteikumi** pārskatiet un atjauniniet kritērijus, ja nepieciešams. Papildinformāciju skatiet sadaļā [Piemērojamības noteikumi](e-invoicing-configuration-rcs.md#applicability-rules).
9. Atlasiet **Saglabāt** un aizveriet lapu

### <a name="deploy-an-electronic-invoicing-feature"></a>Elektronisko rēķinu izrakstīšanas funkcijas izvietošana

Lai izvietotu Elektronisko rēķinu izrakstīšanas līdzekli Pakalpojuma vidē, skatiet sadaļu [Sākt darbu ar Elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-and-supply-chain-management"></a>Kreditoru rēķinu importa iestatījumi programmās Finance un Supply Chain Management
Lai iestatītu dažādu veidu kreditora rēķinu importu, veiciet tālāk norādītās divas sadaļās norādītās darbības.

### <a name="import-vendor-invoices-from-email"></a>Importēt kreditora rēķinus no e-pasta ziņojuma

1. Piesakieties Finance vai Supply Chain Management instancēs un pārbaudiet, vai esat pareizajā juridiskajā personā.
2. Dodieties uz **Organizācijas pārvaldība** > **Iestatīšana** > **Elektronisko dokumentu parametri**.
3. Cilnē **Līdzekļi** pārliecinieties, ka ir atlasīts **NF-e Federal - Brazīlijas elektroniskais rēķins**.
4. **Ārējo kanālu** cilnē **Kanālu** lauku grupā atlasiet **Pievienot**.
5. **Kanāla** laukā ievadiet **NFe** (kanāla nosaukums, kas dots datu kanāla konfigurācijā elektronisko rēķinu izrakstīšanas līdzeklim RCS).
6. Ievadiet aprakstu laukā **Apraksts**. Laukā **Uzņēmums** atlasiet juridisko personu.
7. Laukā **Dokumenta konteksts** atlasiet **Debitora rēķina konteksta modelis – Finanšu dokumenta konteksts**.
8. Lauku grupā **Avotu importēšana** atlasiet **Pievienot**.
9. **Nosaukuma** laukā ievadiet **XmlFile** (**Pievienojuma filtra** nosaukums, kas dots datu kanāla konfigurācijā elektronisko rēķinu izrakstīšanas līdzeklim RCS).
10. Laukā **Apraksts** ievadiet aprakstu un **Datu elementa nosaukuma** laukā atlasiet **Saņemtie NF-e XML dokumenti**.
11. **Modeļa kartēšanas** laukā atlasiet **NF-e-pasta importēšana — NF e-pasta importēšana (BR)** un pēc tam atlasiet **Saglabāt**.
12. Cilnes **Elektronisks dokuments** **Elektronisko pārskatu** lauku grupā atlasiet **Pievienot** un laukā **Tabulas nosaukums** atlasiet **Saņemtais NF-e XML dokuments**.
13. Laukā **Dokumenta konteksts** atlasiet **Debitora rēķina konteksts – Uzziņas par finanšu dokumenta kontekstu**.
14. Laukā **Elektronisko dokumentu modeļu kartēšana** atlasiet **Uzziņas par kartēšanu — finanšu dokumentu kartēšana**.
15. Atlasiet **Atbilžu veidi** un pēc tam atlasiet **Jauns**.
16. Laukā **Atbildes tips** ievadiet **Atbilde**. Laukā **Iesniegšanas statuss** atlasiet **Plānots**.
17. Laukā **Modeļa kartēšana** atlasiet **Atbildes ziņojuma importēšanas formāts — Modeļa kartēšana no atbildes ziņojuma**.
18. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

### <a name="import-peppol-electronic-vendor-invoices"></a>PEPPOL importa kreditoru rēķini

1. Pārejiet uz darbvietu **Elektroniskie pārskati** un atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
2. Atlasiet **Debitora rēķina konteksta modeli** un izveidojiet atvasinātu konfigurāciju.
3. **Melnraksta** versijā atlasiet **Veidotājs**.
4. **Datu modeļa** kokā atlasiet **Debitora rēķins** un pēc tam atlasiet **Kartēt modeli par datu avotu**.
5. **Definīciju** kokā atlasiet **CustomerInvoice** un pēc tam atlasiet **Veidotājs**.
6. Kokā **Datu avoti** atlasiet **Context\_Channel**. Laukā **Vērtība** atlasiet **PEPPOL**. Šis ir kanāla nosaukums, kas ir elektronisko rēķinu funkcijas datu kanāla nosaukums RCS. 
7. Atlasiet **Saglabāt** un aizveriet lapu.
8. Aizvērt lapu.
9. Atlasiet **Debitora rēķina konteksta modeli** un kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu** > **Pabeigts**.
10. Dodieties uz **Organizācijas administrēšana** > **Iestatījumi** > **Elektronisko dokumentu parametri** un cilnē **Līdzekļi** pārliecinieties, ka ir atlasīti **PEPPOL globālie elektroniskie rēķini**. 
11. **Ārējo kanālu** cilnē **Kanālu** lauku grupā atlasiet **Pievienot**.
12. **Kanāla** laukā ievadiet **PEPPOL**. Ievadiet aprakstu laukā **Apraksts**.
13. Laukā **Uzņēmums** atlasiet juridisko personu. Laukā **Dokumenta konteksts** atlasiet **Debitora rēķina konteksts – Debitoru rēķina konteksta modelis**.
14. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.


## <a name="receive-electronic-invoices"></a>Elektronisko rēķinu saņemšana
Lai saņemtu elektroniskos rēķinus, veiciet šādus soļus:

1. Dodieties uz **Organizācijas administrēšana** > **Periodiskais** > **Elektroniskie dokumenti** > **Saņemt elektroniskos dokumentus**.
2. Atlasiet **Labi** un pēc tam aizveriet lapu.

## <a name="view-receive-logs-for-electronic-invoices"></a>Skatīt elektronisko rēķinu saņemšanas žurnālus

Lai skatītu elektronisko rēķinu saņemšanas žurnālus, dodieties uz **Organizācijas administrēšana** > **Periodiskais** > **Elektroniskie dokumenti** > **Elektronisko dokumentu saņemšanas žurnāls**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
