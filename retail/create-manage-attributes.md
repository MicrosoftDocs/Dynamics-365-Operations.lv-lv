---
title: "Izveidot un pārvaldīt atribūtus"
description: "Šajā rakstā ir aprakstīts Microsoft Dynamics 365 operācijām atribūtus. Atribūti ļauj aprakstīt preci un tās raksturīgās iezīmes, izmantojot lietotāja definētos laukus."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 26c628e10aaa5f47bc87d7510ca8f41ab3630204
ms.lasthandoff: 03/31/2017


---

# <a name="create-and-manage-attributes"></a>Izveidot un pārvaldīt atribūtus

Šajā rakstā ir aprakstīts Microsoft Dynamics 365 operācijām atribūtus. Atribūti ļauj aprakstīt preci un tās raksturīgās iezīmes, izmantojot lietotāja definētos laukus.

Atribūti ļauj aprakstīt preci un tās raksturīgās iezīmes, izmantojot lietotāja definētos laukus. Piemēram, jūs varat norādīt produkta atmiņas lielumu un cietā diska jaudu, un norādīt, vai prece ir atbilstoša Energy star programmai. Atribūtus var saistīt ar dažādām mazumtirdzniecības vienībām, piemēram, preču kategorijām un mazumtirdzniecības kanāliem, tiem var iestatīt noklusētās vērtības. Preces pārmanto to atribūtus un atribūtu noklusējuma vērtības, ja tie ir saistīti ar preču kategorijām vai mazumtirdzniecības kanāliem. Noklusējuma vērtības var būt ignorētas individuālas preces līmenī, mazumtirdzniecības kanāla līmenī vai mazumtirdzniecības katalogā.

#### <a name="examples"></a>Piemēri

Kategorija

Atribūts

Pieļaujamās vērtības

Noklusējuma vērtība

TV un Video

Zīmols

Jebkura derīga **Zīmola** vērtība

Nav

TV

Ekrāna izmērs

**20"**–**80"**

Nav

Vertikālā izšķirtspēja

**480i**, **720p**, **1080i**, vai **1080p**

**1080p**

Ekrāna atsvaidzes intensitāte

**60 Hz**, **120 Hz**, vai **240 Hz**

**60 Hz**

HDMI ievades

**0**–**10**

**3**

DVI ievades

**0**–**10**

**1**

Kompozītie ievadi

**0**–**10**

**2**

Komponentās ievades

**0**–**10**

**1**

LCD

3D gatavs

**Jā** vai **Nē**

**Jā**

3D iespējots

**Jā** vai **Nē**

**Nē**

Plazmas

Ekspluatācijas temperatūra no

**32**–**110** grādiem

**32**

Ekspluatācijas temperatūra līdz

**32**–**110** grādiem

**100**

Projekcijas

Kineskopa garantija

**6**, **12**, vai **18** mēneši

**12**

\#Projekcijas caurules

**1**–**5**

**3**

## <a name="attribute-type"></a>Atribūta tips
  [![atribūtu fiksēta kopija](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) atribūti ir balstīti uz atribūta tipu. Atribūta veidi norāda datu veidu, ko var ievadīt noteiktam atribūtam. Šobrīd Microsoft Dynamics 365 operāciju atbalsta šādus atribūtu veidus:

-   **Valūta** – šī atribūta veids atbalsta valūtas vērtības. Tas var būt saistīts (var atbalstīt vērtību diapazonu), vai tas var palikt atklāts.
-   **DateTime** – šī atribūta veids atbalsta datuma un laika vērtības. Tas var būt saistīts (var atbalstīt vērtību diapazonu), vai tas var palikt atklāts.
-   **Decimāls** – šī atribūta veids atbalsta skaitliskās vērtības, kas ietver decimāldaļskaitļu vietas. Tas atbalsta arī mērvienības. Tas var būt saistīts (var atbalstīt vērtību diapazonu), vai tas var palikt atklāts.
-   **Vesels skaitlis** – šī atribūta veids atbalsta skaitliskas vērtības. Tas atbalsta arī mērvienības. Tas var būt saistīts (var atbalstīt vērtību diapazonu), vai tas var palikt atklāts.
-   **Teksts** – šī atribūta veids atbalsta teksta vērtības. Tā atbalsta arī iepriekš definētu iespējamo vērtību kopu (uzskaitījums).
-   **Būla** – šī atribūta tips atbalsta binārām vērtībām (**patieso**/**viltus**).
-   **Atsauce**.

## <a name="attribute"></a>Atribūts
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) papildus nosaukumu, draudzīgo nosaukumu, aprakstu un palīdzības teksts, viens vai vairāki no šādiem informācijas veidiem var skenēt atribūta:

-   Noklusējuma vērtība
-   Atribūta metadati, piemēram, metadati, kas norāda, vai atribūtu var meklēt, precizēt vai kārtot

## <a name="attribute-group"></a>Atribūtu grupa
  [![createandmanageattribute 10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) pēc tam, kad ir definēti atribūti, tās var iedalīt atribūtu grupām. Atribūtu grupas norāda atsevišķu atribūtu grupējumus un var būt piešķirtas mazumtirdzniecības kategorijām vai mazumtirdzniecības kanāliem.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Atribūtu grupu piešķiršana mazumtirdzniecības kategorijām
  [![createandmanageattribute 12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) viens vai vairāki atribūtu grupām var būt saistīta ar mazumtirdzniecības preču kategorijas hierarhijas kategorijā zaros. Kad preces ir sadalītas kategorijās, tās manto atribūtus, kas ir iekļautas atribūtu grupās.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Atribūtu grupu piešķiršana mazumtirdzniecības veikaliem
  [![createandmanageattribute 13 1024 x 576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) viens vai vairāki atribūtu grupām var būt saistīta ar viena vai vairāku mazumtirdzniecības veikalu mazumtirdzniecības veikali hierarhijā. Kad preces ir bagātinātas noteiktiem mazumtirdzniecības veikaliem, tās manto atribūtus, kas ir iekļauti atribūtu grupās.

## <a name="overriding-attribute-values"></a>Atribūta vērtību ignorēšāna
### <a name="at-the-product-level"></a>Preču līmenī

  [![createandmanageattribute 14 1024 x 576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) atribūtu noklusējuma vērtības var ignorēt produktu līmenī (t.i., atsevišķiem produktiem).

### <a name="in-a-retail-catalog"></a>Mazumtirdzniecības katalogā

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) atribūtu noklusējuma vērtības var ignorēt atsevišķiem produktiem, īpaši katalogos, kas paredzēti specifiskiem mazumtirdzniecības kanāliem.

### <a name="at-the-retail-channel-level"></a>Mazumtirdzniecības kanāla līmenī

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) atribūtu noklusējuma vērtības var ignorēt atsevišķiem produktiem, īpaši katalogos, kas paredzēti specifiskiem mazumtirdzniecības kanāliem.


