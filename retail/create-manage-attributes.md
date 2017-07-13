---
title: "Izveidot un pārvaldīt atribūtus"
description: "Šajā rakstā ir aprakstīti programmatūrā Microsoft Dynamics 365 for Retail pieejamie atribūti. Atribūti ļauj aprakstīt preci un tās raksturīgās iezīmes, izmantojot lietotāja definētos laukus."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 4493c2f9e9e9dfe990f3b1670d3cd35e3bbaa38d
ms.contentlocale: lv-lv
ms.lasthandoff: 06/20/2017



---

# <a name="create-and-manage-attributes"></a>Izveidot un pārvaldīt atribūtus

[!include[banner](includes/banner.md)]


Šajā rakstā ir aprakstīti programmatūrā Microsoft Dynamics 365 for Retail pieejamie atribūti. Atribūti ļauj aprakstīt preci un tās raksturīgās iezīmes, izmantojot lietotāja definētos laukus.

Atribūti ļauj aprakstīt preci un tās raksturīgās iezīmes, izmantojot lietotāja definētos laukus. Piemēram, jūs varat norādīt produkta atmiņas lielumu un cietā diska jaudu, un norādīt, vai prece ir atbilstoša Energy star programmai. Atribūtus var saistīt ar dažādām mazumtirdzniecības vienībām, piemēram, preču kategorijām un mazumtirdzniecības kanāliem, tiem var iestatīt noklusētās vērtības. Preces pārmanto to atribūtus un atribūtu noklusējuma vērtības, ja tie ir saistīti ar preču kategorijām vai mazumtirdzniecības kanāliem. Noklusējuma vērtības var būt ignorētas individuālas preces līmenī, mazumtirdzniecības kanāla līmenī vai mazumtirdzniecības katalogā.

#### <a name="examples"></a>Piemēri

| Kategorija   | Atribūts                | Pieļaujamās vērtības          | Noklusētā vērtība |
|------------|--------------------------|-----------------------------|---------------|
| TV un Video | Zīmols                    | Jebkura derīga Zīmola vērtība       | Nav          |
| TV         | Ekrāna izmērs              | 20″–80″                     | Nav          |
| TV         | Vertikālā izšķirtspēja      | 480i, 720p, 1080i, vai 1080p | 1080p         |
| TV         | Ekrāna atsvaidzes intensitāte      | 60 Hz, 120 Hz, vai 240 Hz       | 60 Hz          |
| TV         | HDMI ievades              | 0–10                        | 3.             |
| TV         | DVI ievades               | 0–10                        | 1.             |
| TV         | Kompozītie ievadi         | 0–10                        | 2.             |
| TV         | Komponentās ievades         | 0–10                        | 1.             |
| LCD        | 3D gatavs                 | Jā vai Nē                   | Jā           |
| LCD        | 3D iespējots               | Jā vai Nē                   | Nav            |
| Plazmas     | Ekspluatācijas temperatūra no      | 32–110 grādiem              | 32            |
| Plazmas     | Ekspluatācijas temperatūra līdz        | 32–110 grādiem              | 100           |
| Projekcijas | Kineskopa garantija | 6, 12, vai 18 mēneši         | 12.            |
| Projekcijas | Kineskopu skaits    | 1–5                         | 3.             |


## <a name="attribute-type"></a>Atribūta tips
  [![attributes-fixed-copy](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) 
  
Atribūti ir balstīti uz atribūtu tipiem. Atribūta veidi norāda datu veidu, ko var ievadīt noteiktam atribūtam. Pašlaik programmatūra Microsoft Dynamics 365 for Retail atbalsta tālāk norādītos atribūtu tipus.

-   **Valūta** – šī atribūta veids atbalsta valūtas vērtības. Tas var būt saistīts (var atbalstīt vērtību diapazonu), vai tas var palikt atklāts.
-   **DateTime** – šī atribūta veids atbalsta datuma un laika vērtības. Tas var būt saistīts (var atbalstīt vērtību diapazonu), vai tas var palikt atklāts.
-   **Decimāls** – šī atribūta veids atbalsta skaitliskās vērtības, kas ietver decimāldaļskaitļu vietas. Tas atbalsta arī mērvienības. Tas var būt saistīts (var atbalstīt vērtību diapazonu), vai tas var palikt atklāts.
-   **Vesels skaitlis** – šī atribūta veids atbalsta skaitliskas vērtības. Tas atbalsta arī mērvienības. Tas var būt saistīts (var atbalstīt vērtību diapazonu), vai tas var palikt atklāts.
-   **Teksts** – šī atribūta veids atbalsta teksta vērtības. Tā atbalsta arī iepriekš definētu iespējamo vērtību kopu (uzskaitījums).
-   **Būla** – šis atribūta tips atbalsta binārās vērtības (**patiess**/**aplams**).
-   **Atsauce**.

## <a name="attribute"></a>Atribūts
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) Papildus nosaukumam, draudzīgam nosaukumam, aprakstam un palīdzības tekstam, atribūtam var tikt tverti viens vai vairāki no tālāk norādītajiem informācijas tipiem.

-   Noklusējuma vērtība
-   Atribūta metadati, piemēram, metadati, kas norāda, vai atribūtu var meklēt, precizēt vai kārtot

## <a name="attribute-group"></a>Atribūtu grupa
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) Kad atribūti ir definēti, tos var grupēt atribūtu grupās. Atribūtu grupas norāda atsevišķu atribūtu grupējumus un var būt piešķirtas mazumtirdzniecības kategorijām vai mazumtirdzniecības kanāliem.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Atribūtu grupu piešķiršana mazumtirdzniecības kategorijām
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) Vienu vai vairākas atribūtu grupas var saistīt ar kategoriju zariem mazumtirdzniecības preču kategoriju hierarhijā. Kad preces ir sadalītas kategorijās, tās manto atribūtus, kas ir iekļautas atribūtu grupās.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Atribūtu grupu piešķiršana mazumtirdzniecības veikaliem
  [![createandmanageattribute-13-1024x576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) Vienu vai vairākas atribūtu grupas var saistīt ar vienu vai vairākiem mazumtirdzniecības veikalu zariem mazumtirdzniecības veikalu hierarhijā. Kad preces ir bagātinātas noteiktiem mazumtirdzniecības veikaliem, tās manto atribūtus, kas ir iekļauti atribūtu grupās.

## <a name="overriding-attribute-values"></a>Atribūta vērtību ignorēšāna
### <a name="at-the-product-level"></a>Preču līmenī

  [![createandmanageattribute-14-1024x576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) Atribūtu noklusējuma vērtības var ignorēt preces līmenī (t.i., atsevišķām precēm).

### <a name="in-a-retail-catalog"></a>Mazumtirdzniecības katalogā

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) Atribūtu noklusējuma vērtības var ignorēt atsevišķām precēm noteiktos katalogos, kas ir paredzēti specifiskiem mazumtirdzniecības kanāliem.

### <a name="at-the-retail-channel-level"></a>Mazumtirdzniecības kanāla līmenī

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) Atribūtu noklusējuma vērtības var ignorēt atsevišķām precēm noteiktos katalogos, kas ir paredzēti specifiskiem mazumtirdzniecības kanāliem.




