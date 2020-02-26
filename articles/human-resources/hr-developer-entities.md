---
title: Common Data Service elementi
description: Microsoft Dynamics 365 Human Resources izmanto Common Data Service, lai iespējotu paplašināšanas un integrācijas scenārijus.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85dd95e8209fff28f214986f7960372db200351b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009855"
---
# <a name="common-data-service-entities"></a>Common Data Service elementi

Microsoft Dynamics 365 Human Resources izmanto Common Data Service, lai iespējotu paplašināšanas un integrācijas scenārijus.

Plašāku informāciju par Common Data Service skatiet [Kas ir Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Common Data Service ir pieejami šādas cilvēkresursu entitījas.

## <a name="benefit-entities"></a>Atvieglojumu elementi

**Atvieglojumu aprēķina biežums**

| **Lauki**        | **Datu tips** | **Obligāts** | **Meklējams** |
|-------------------|---------------|--------------|----------------|
| Apraksts       | Teksts          |              | X              |
| Biežuma kontrole | Opciju kopa    | X            | X              |
| Ir nemainīga      | Divas opcijas   |              | X              |
| Vārds/nosaukums              | Teksts          | X            | X              |


**Atvieglojumu aprēķina likme**

| **Lauki**  | **Datu tips** | **Obligāts** | **Meklējams** |
|-------------|---------------|--------------|----------------|
| Apraksts | Teksts          |              | X              |
| Vārds/nosaukums        | Teksts          | X            | X              |
| TierType    | Opciju kopa    | X            | X              |


**Atvieglojumu aprēķina likmes informācija**

| **Lauki**                             | **Datu tips**  | **Obligāts** | **Meklējams** |
|----------------------------------------|----------------|--------------|----------------|
| Atvieglojumu aprēķina likmes informācijas numurs | Teksts           | X            | X              |
| Aprēķina likmes ID                    | Pārlūkošana         | X            | X              |
| Seguma metode                    | Opciju kopa     | X            | X              |
| Ir spēkā                              | Vienīgi datums      | X            | X              |
| Darba devēja ieguldījums                  | Decimālskaitlis |              | X              |
| Termiņa beigas                             | Vienīgi datums      | X            | X              |
| WorkerDeduction                        | Decimālskaitlis |              | X              |


**Atvieglojumu tips**

| **Lauki**           | **Datu tips** | **Obligāts** | **Meklējams** |
|----------------------|---------------|--------------|----------------|
| ConcurrentEnrollment | Opciju kopa    |              | X              |
| Apraksts          | Teksts          |              | X              |
| Vārds/nosaukums                 | Teksts          | X            | X              |
| PayrollCategory      | Opciju kopa    |              | X              |


**Atvieglojumu plāns**

| **Lauki**                               | **Datu tips**  | **Obligāts** | **Meklējams** |
|------------------------------------------|----------------|--------------|----------------|
| Iekavēto maksājumu ierobežojuma metode                      | Opciju kopa     |              | X              |
| Atvieglojumu veids                             | Pārlūkošana         | X            | X              |
| Seguma ierobežojuma metode                | Opciju kopa     |              | X              |
| Seguma metode                      | Opciju kopa     |              | X              |
| Valūta                                 | Pārlūkošana         |              | X              |
| Ieturējuma prioritāte                       | Vesels skaitlis   |              | X              |
| Noklusējuma seguma ierobežojuma summa        | Valūta       |              | X              |
| Noklusēto segumu ierobežojuma summa (pamata) | Valūta       |              | X              |
| Noklusējuma seguma ierobežojuma periods        | Opciju kopa     |              | X              |
| Noklusējuma ieturējuma ierobežojuma summa           | Valūta       |              | X              |
| Noklusētā ieturējuma ierobežojuma summa (pamata)    | Valūta       |              | X              |
| Noklusējuma ieturējuma ierobežojuma periods           | Opciju kopa     |              | X              |
| Apraksts                              | Teksts           |              | X              |
| Valūtas kurss                            | Decimālskaitlis |              | X              |
| Ir papildu izmaksas izpilde                | Divas opcijas    |              | X              |
| Ir pārskatā norādāmais Pieejamās aprūpes akts        | Divas opcijas    |              | X              |
| Iekavētais maksājums ir ģenerēts                      | Divas opcijas    |              | X              |
| Ir bruto                              | Divas opcijas    |              | X              |
| Ir primārais                               | Divas opcijas    |              | X              |
| Vārds/nosaukums                                     | Teksts           | X            | X              |
| Algas ietekme                           | Opciju kopa     |              | X              |
| Pensionēšanās veids                          | Opciju kopa     |              | X              |


**Nodarbinātības elements**

| **Lauki**                     | **Datu tips**  | **Obligāts** | **Meklējams** |
|--------------------------------|----------------|--------------|----------------|
| Nodarbinātā koriģētais pieņemšanas datums     | Datums un laiks  |              | X              |
| Uzņēmums                        | Pārlūkošana         | X            | X              |
| Darba devēja paziņojuma vienības summa | Decimālskaitlis |              | X              |
| Darba devēja paziņojuma vienība        | Opciju kopa     |              | X              |
| Nodarbinātības beigu datums            | Datums un laiks  |              | X              |
| Nodarbinātības numurs              | Teksts           | X            | X              |
| Darba attiecību uzsākšanas datums          | Datums un laiks  |              | X              |
| Pēdējās darbdienas datums              | Datums un laiks  |              | X              |
| Pārcelšanas datums                | Datums un laiks  |              | X              |
| Derīgs no                     | Datums un laiks  | X            | X              |
| Derīgs līdz                       | Datums un laiks  |              | X              |
| Nodarbinātais                         | Pārlūkošana         | X            | X              |
| Nodarbinātā paziņojuma summa           | Decimālskaitlis |              | X              |
| Nodarbinātā pieņemšanas datums             | Datums un laiks  |              | X              |
| Nodarbinātā tips                    | Opciju kopa     | X            | X              |
| Nodarbinātā paziņojuma vienība          | Opciju kopa     |              | X              |

## <a name="worker-entities"></a>Nodarbinātā elementi

**Etniskā izcelsme**

| **Lauki**         | **Datu tips** | **Obligāts** | **Meklējams** |
|--------------------|---------------|--------------|----------------|
| Apraksts        | Teksts          |              | X              |
| Etniskās izcelsmes nosaukums | Teksts          | X            | X              |


**Valoda**

| **Lauki**    | **Datu tips** | **Obligāts** | **Meklējams** |
|---------------|---------------|--------------|----------------|
| Apraksts   | Teksts          |              | X              |
| Valodas nosaukums | Teksts          | X            | X              |


**Veterāna statuss**

| **Lauki**           | **Datu tips** | **Obligāts** | **Meklējams** |
|----------------------|---------------|--------------|----------------|
| Apraksts          | Teksts          |              | X              |
| Ir aizsargāts veterāns | Divas opcijas    |              | X              |
| Valodas nosaukums        | Teksts          | X            | X              |


**Nodarbinātais**

| **Lauki**                | **Datu tips** | **Obligāts** | **Meklējams** |
|---------------------------|---------------|--------------|----------------|
| Dzimšanas datums                 | Vienīgi datums     |              | X              |
| Apraksts               | Teksts          |              | X              |
| E-pasta adrese 1           | E-pasta adrese         |              | X              |
| E-pasta adrese 2           | E-pasta adrese         |              | X              |
| Facebook identitāte         | Teksts          |              | X              |
| Vārds                | Teksts          |              | X              |
| Pilnais vārds un uzvārds                 | Teksts          |              | X              |
| Dzimums                    | Opciju kopa    |              | X              |
| Ģenerēšana                | Teksts          |              | X              |
| Vai e-pasta kontaktpersona ir atļauta  | Divas opcijas   |              | X              |
| Vai tālruņa kontaktpersona ir atļauta  | Divas opcijas   |              | X              |
| Uzvārds                 | Teksts          |              | X              |
| LinkedIn identitāte         | Teksts          |              | X              |
| Vadītājs                   | Pārlūkošana        |              | X              |
| Otrais vārds               | Teksts          |              | X              |
| Mobilais tālrunis              | Tālruņa numurs         |              | X              |
| Office Graph identifikators   | Teksts          |              | X              |
| Primārā e-pasta adrese     | E-pasta adrese         |              | X              |
| Primārais tālrunis         | Tālruņa numurs         |              | X              |
| Profesija                | Teksts          |              | X              |
| Sociālais tīkls 1          | Opciju kopa    |              | X              |
| Sociālais tīkls 2          | Opciju kopa    |              | X              |
| 1. sociālā tīkla identitāte | Teksts          |              | X              |
| 2. sociālā tīkla identitāte | Teksts          |              | X              |
| Modulis                    | Opciju kopa    | X            | X              |
| Statuss                    | Opciju kopa    | X            | X              |
| 1. tālrunis               | Tālruņa numurs         |              | X              |
| 2. tālrunis               | Tālruņa numurs         |              | X              |
| 3. tālrunis               | Tālruņa numurs         |              | X              |
| Twitter identitāte          | Teksts          |              | X              |
| Lietotājs                      | Pārlūkošana        |              | X              |
| Tīmekļa vietnes URL               | URL           |              | X              |
| Nodarbinātā numurs             | Teksts          | X            | X              |
| Nodarbinātā tips               | Opciju kopa    | X            | X              |
| Yomi vārds           | Teksts          |              | X              |
| Yomi pilnais vārds            | Teksts          |              | X              |
| Yomi uzvārds            | Teksts          |              | X              |
| Yomi otrais vārds          | Teksts          |              | X              |


**Nodarbinātā adrese**

| **Lauki**           | **Datu tips**  | **Obligāts** | **Meklējams** |
|----------------------|----------------|--------------|----------------|
| Adreses numurs       | Teksts           | X            | X              |
| Adreses veids         | Opciju kopa     | X            | X              |
| Pilsēta                 | Teksts           |              | X              |
| Valsts vai reģions    | Teksts           |              | X              |
| Apgabals               | Teksts           |              | X              |
| Fakss                  | Tālruņa numurs          |              | X              |
| Ir vēlams         | Divas opcijas    |              | X              |
| Ģeogrāfiskais platums             | Decimālskaitlis |              | X              |
| 1. rinda               | Teksts           |              | X              |
| 2. rinda               | Teksts           |              | X              |
| 3. rinda               | Teksts           |              | X              |
| Ģeogrāfiskais garums            | Decimālskaitlis |              | X              |
| Pasta indekss          | Teksts           |              | X              |
| Pasta kastīte      | Teksts           |              | X              |
| Piegādes metodes kods | Vesels skaitlis   |              | X              |
| Novads    | Teksts           |              | X              |
| 1. tālrunis          | Tālruņa numurs          |              | X              |
| 2. tālrunis          | Tālruņa numurs          |              | X              |
| 3. tālrunis          | Tālruņa numurs          |              | X              |
| UPS zona             | Teksts           |              | X              |
| UTC korespondējošais konts           | Vesels skaitlis   |              | X              |
| Nodarbinātais               | Pārlūkošana         | X            | X              |


**Nodarbinātā personas dati**

| Lauki                             | Datu tips    | Pieprasīts | Meklējams |
|------------------------------------|--------------|----------|------------|
| Dzimtā pilsēta                         | Teksts         |          | X          |
| Dzimtā valsts/reģions            | Opciju kopa   |          | X          |
| Dzimšanas datums                          | Vienīgi datums    |          | X          |
| Valsts/reģiona pavalstniecība      | Opciju kopa   |          | X          |
| Miršanas datums                      | Vienīgi datums    |          | X          |
| Atspējots veterāna pārbaudes datums | Vienīgi datums    |          | X          |
| Izglītība                          | Teksts         |          | X          |
| Etniskā izcelsme                     | Pārlūkošana       |          | X          |
| ExpatriateEndDate                  | Vienīgi datums    |          | X          |
| ExpatriateStartDate                | Vienīgi datums    |          | X          |
| Tēva dzimtā valsts/reģions     | Opciju kopa   |          | X          |
| Dzimums                             | Opciju kopa   |          | X          |
| Ir atspējots                        | Divas opcijas  |          | X          |
| Ir kara invalīds                | Divas opcijas  |          | X          |
| Vai ekspatriantu pārvaldīšana ir piemērojama    | Divas opcijas  |          | X          |
| Ir pilna laika students               | Divas opcijas  |          | X          |
| Ģimenes stāvoklis                     | Opciju kopa   |          | X          |
| Karadienesta beigu datums          | Vienīgi datums    |          | X          |
| Karadienesta sākuma datums        | Vienīgi datums    |          | X          |
| Mātes dzimtā valsts/reģions     | Opciju kopa   |          | X          |
| Tautības valsts vai reģions      | Opciju kopa   |          | X          |
| Dzimtā valoda                    | Pārlūkošana       |          | X          |
| Apgādājamo skaits               | Vesels skaitlis |          |            |
| Veterāna statuss                     | Pārlūkošana       |          | X          |
| Nodarbinātais                             | Pārlūkošana       | X        | X          |
| Deleģētā nodarbinātā personas kods      | Teksts         | X        | X          |


**Nodarbinātā bankas konts**

| **Lauki**                 | **Datu tips** | **Obligāts** | **Meklējams** |
|----------------------------|---------------|--------------|----------------|
| Konta īpašnieks             | Teksts          |              | X              |
| Konta kods     | Teksts          |              | X              |
| Adreses apraksts        | Teksts          |              | X              |
| Bankas konta tips          | Opciju kopa    |              | X              |
| Bankas novietojuma kods         | Teksts          |              | X              |
| Filiāles nosaukums                | Teksts          |              | X              |
| Filiāles numurs              | Teksts          |              | X              |
| Pilsēta                       | Teksts          |              | X              |
| Valsts vai reģions          | Teksts          |              | X              |
| Apgabals                     | Teksts          |              | X              |
| Apraksts                | Teksts          |              | X              |
| Rajona nosaukums              | Teksts          |              | X              |
| E-pasta adrese                      | Teksts          |              | X              |
| Paplašinājums                  | Teksts          |              | X              |
| Fakss                        | Teksts          |              | X              |
| IBAN                       | Teksts          |              | X              |
| 1. rinda                     | Teksts          |              | X              |
| 2. rinda                     | Teksts          |              | X              |
| 3. rinda                     | Teksts          |              | X              |
| Mobilais tālrunis               | Teksts          |              | X              |
| Personas vārds             | Teksts          |              | X              |
| Pasta indekss                | Teksts          |              | X              |
| Pasta kastīte            | Teksts          |              |                |
| Reģistrācijas numurs             | Teksts          |              | X              |
| Reģistrācijas numura tips        | Opciju kopa    |              | X              |
| Novads          | Teksts          |              | X              |
| SWIFT kods                 | Teksts          |              | X              |
| Tālrunis                  | Teksts          |              | X              |
| Teleksa numurs               | Teksts          |              | X              |
| Tīmekļa vietnes URL                | Teksts          |              | X              |
| Nodarbinātais                     | Pārlūkošana        | X            | X              |
| Nodarbinātā bankas konta numurs | Teksts          |              | X              |
| Nodarbinātā bankas konta numurs | Teksts          | X            | X              |

**Nodarbinātā fiksētā atlīdzība**

| Lauki                                | Datu tips      | Pieprasīts | Meklējams |
|---------------------------------------|----------------|----------|------------|
| Uzņēmums                               | Pārlūkošana         | X        | X          |
| Atlīdzības veids                     | Opciju kopa     |          | X          |
| Valūta                              | Pārlūkošana         |          | X          |
| Spēkā stāšanās datums                        | Vienīgi datums      |          | X          |
| Notikums                                 | Pārlūkošana         | X        | X          |
| Valūtas kurss                         | Decimālskaitlis |          | X          |
| Beigu datums                       | Vienīgi datums      |          | X          |
| Rindas numurs                           | Decimālskaitlis |          | X          |
| Algas izmaksas biežums                         | Pārlūkošana         | X        | X          |
| Maksājuma kurss                              | Valūta       |          | X          |
| Maksājuma likme (bāze)                       | Valūta       |          | X          |
| Plāns                                  | Pārlūkošana         | X        | X          |
| Ieņemamais amats                              | Pārlūkošana         | X        | X          |
| Procesu tips                          | Opciju kopa     | X        | X          |
| Atsauces punkta iestatījuma rinda            | Pārlūkošana         |          | X          |
| Nodarbinātais                                | Pārlūkošana         | X        | X          |
| Nodarbinātā fiksētās atlīdzības numurs      | Teksts           | X        | X          |

**Nodarbinātās personas identifikācijas numurs**

| Lauki                 | Datu tips   | Pieprasīts | Meklējams |
|------------------------|-------------|----------|------------|
| Apraksts            | Teksts        |          | X          |
| Ieraksta veids             | Teksts        |          | X          |
| Beigu datums        | Vienīgi datums   |          | X          |
| Identifikācijas numurs  | Teksts        | X        | X          |
| Identifikācijas tips    | Pārlūkošana      | X        | X          |
| Ir primārais             | Divas opcijas |          | X          |
| Izsniegšanas datums             | Vienīgi datums   |          | X          |
| Izdevējiestāde         | Pārlūkošana      | X        | X          |
| Nodarbinātais                 | Pārlūkošana      | X        | X          |


## <a name="position-entities"></a>Pozīcijas entītijas

**Amats**

| **Lauki**               | **Datu tips**  | **Obligāts** | **Meklējams** |
|--------------------------|----------------|--------------|----------------|
| Aktivizēšana               | Datums un laiks  |              | X              |
| Pieejams piešķirei | Datums un laiks  |              | X              |
| Nodaļa               | Pārlūkošana         |              | X              |
| Apraksts              | Teksts           |              | X              |
| Pilnas slodzes ekvivalents     | Decimālskaitlis |              | X              |
| Darbs                      | Pārlūkošana         | X            | X              |
| Amata numurs      | Teksts           | X            | X              |
| Vecāka amats      | Pārlūkošana         |              | X              |
| Amata veids            | Pārlūkošana         |              | X              |
| Aiziešana pensijā               | Datums un laiks  |              | X              |
| Virsraksts                    | Opciju kopa     |              | X              |
| Derīgs no               | Datums un laiks  | X            | X              |
| Derīgs līdz                 | Datums un laiks  |              | X              |


**Amata veids**

| **Lauki**         | **Datu tips** | **Obligāts** | **Meklējams** |
|--------------------|---------------|--------------|----------------|
| Klasifikācija     | Opciju kopa    |              | X              |
| Apraksts        | Teksts          |              | X              |
| Amata veida nosaukums | Teksts          | X            | X              |


**Amatā nodarbinātā piešķire**

| **Lauki**                        | **Datu tips** | **Obligāts** | **Meklējams** |
|-----------------------------------|---------------|--------------|----------------|
| Amats                      | Pārlūkošana        | X            | X              |
| Amata nodarbinātā piešķires numurs | Teksts          | X            | X              |
| Derīgs no                        | Teksts          | X            | X              |
| Derīgs līdz                          |               |              | X              |
| Nodarbinātais                            |               | X            | X              |

## <a name="job-entities"></a>Darba elementi

**Darbs**

| **Lauki**                   | **Datu tips**  | **Obligāts** | **Meklējams** |
|------------------------------|----------------|--------------|----------------|
| Atļaut neierobežotus amatus    | Divas opcijas    |              | X              |
| Noklusējuma pilnas slodzes ekvivalents | Decimālskaitlis |              | X              |
| Apraksts                  | Teksts           |              | X              |
| Pienākumu apraksts              | Teksts           |              | X              |
| Darba funkcija                 | Pārlūkošana         |              | X              |
| Darba tips                     | Pārlūkošana         |              | X              |
| Maksimālais pozīciju skaits  | Vesels skaitlis   |              | X              |
| Vārds/nosaukums                         | Teksts           | X            | X              |
| Virsraksts                        | Opciju kopa     |              | X              |
| Derīgs no                   | Datums un laiks  | X            | X              |
| Derīgs līdz                     | Datums un laiks  |              | X              |


**Darba funkcija**

| **Lauki**        | **Datu tips** | **Obligāts** | **Meklējams** |
|-------------------|---------------|--------------|----------------|
| Apraksts       | Teksts          | X            | X              |
| Darba funkcijas nosaukums | Teksts          | X            | X              |


**Darba tips**

| **Lauki**    | **Datu tips** | **Obligāts** | **Meklējams** |
|---------------|---------------|--------------|----------------|
| Apraksts   | Teksts          | X            | X              |
| Nodokļu atvieglojumu statuss | Opciju kopa    | X            | X              |
| Darba tipa nosaukums | Teksts          | X            | X              |

## <a name="leave-and-absence-entities"></a>Atvaļinājumu un kavējumu elementi

**Atvaļinājuma reģistrācija**

| **Lauki**            | **Datu tips** | **Obligāts** | **Meklējams** |
|-----------------------|---------------|--------------|----------------|
| Uzkrāšanas datuma pamats    | Vienīgi datums     | X            | X              |
| Uzkrāšanas sākuma datums    | Vienīgi datums     | X            | X              |
| Pielāgots datums           | Vienīgi datums     | X            | X              |
| Vai uzkrāšana ir aizturēta  | Divas opcijas   |              | X              |
| LeaveEnrollmentNumber | Teksts          | X            | X              |
| Atvaļinājumu plāns            | Pārlūkošana        | X            | X              |
| Sākuma datums            | Vienīgi datums     | X            | X              |
| Pakāpes pamats            | Opciju kopa    | X            | X              |
| Nodarbinātais                | Pārlūkošana        | X            | X              |


**Atstāt bankas transakciju**

| **Lauki**                    | **Datu tips**  | **Obligāts** | **Meklējams** |
|-------------------------------|----------------|--------------|----------------|
| Apjoms                        | Decimālskaitlis | X            | X              |
| Uzņēmums                       | Pārlūkošana         | X            | X              |
| Atstāt bankas transakcijas numuru | Teksts           | X            | X              |
| Atvaļinājumu plāns                    | Pārlūkošana         |              | X              |
| Atvaļinājuma tips                    | Pārlūkošana         | X            | X              |
| Transakcijas datums              | Vienīgi datums      | X            | X              |
| Darījuma numurs            | Decimālskaitlis | X            | X              |
| Transakcijas veids              | Opciju kopa     | X            | X              |
| Nodarbinātais                        | Pārlūkošana         | X            | X              |


**Atvaļinājumu plāns**

| **Lauki**        | **Datu tips** | **Obligāts** | **Meklējams** |
|-------------------|---------------|--------------|----------------|
| Uzkrāšanas biežums | Opciju kopa    | X            | X              |
| Uzņēmums           | Pārlūkošana        | X            | X              |
| Apraksts       | Teksts          |              | X              |
| Atvaļinājuma tips        | Pārlūkošana        | X            | X              |
| Vārds/nosaukums              | Teksts          | X            | X              |
| Sākuma datums        | Vienīgi datums     | X            | X              |


**Atvaļinājuma pieprasījums**

| **Lauki**           | **Datu tips** | **Obligāts** | **Meklējams** |
|----------------------|---------------|--------------|----------------|
| Komentārs              | Teksts          | X            | X              |
| Uzņēmums              | Pārlūkošana        | X            | X              |
| Atvaļinājuma pieprasījuma numurs | Teksts          |              | X              |
| Pieprasījuma datums         | Datums un laiks | X            | X              |
| Statuss               | Opciju kopa    | X            | X              |
| Nodarbinātais               | Pārlūkošana        | X            | X              |


**Atvaļinājuma pieprasījuma informācija**

| **Lauki**                  | **Datu tips**  | **Obligāts** | **Meklējams** |
|-----------------------------|----------------|--------------|----------------|
| Apjoms                      | Decimālskaitlis | X            | X              |
| Atvaļinājuma datums                  | Datums un laiks  | X            | X              |
| Atvaļinājuma pieprasījums               | Pārlūkošana         | X            | X              |
| Atvaļinājuma pieprasījuma informācijas numurs | Teksts           | X            | X              |
| Atvaļinājuma tips                  | Pārlūkošana         | X            | X              |


**Atvaļinājuma veids**

| **Lauki**      | **Datu tips** | **Obligāts** | **Meklējams** |
|-----------------|---------------|--------------|----------------|
| Uzņēmums         | Pārlūkošana        | X            | X              |
| Apraksts     | Teksts          |              | X              |
| Ienākumu veida kods    | Pārlūkošana        |              | X              |
| Atvaļinājuma tipa nosaukums | Teksts          | X            | X              |


**Darba kalendārs**

| **Lauki**  | **Datu tips** | **Obligāts** | **Meklējams** |
|-------------|---------------|--------------|----------------|
| Uzņēmums     | Pārlūkošana        | X            | X              |
| Apraksts | Teksts          |              | X              |
| Vārds/nosaukums        | Teksts          | X            | X              |


**Darba kalendāra diena**

| **Lauki**               | **Datu tips** | **Obligāts** | **Meklējams** |
|--------------------------|---------------|--------------|----------------|
| Kalendārais datums            | Vienīgi datums     | X            | X              |
| Uzņēmums                  | Pārlūkošana        |              | X              |
| Statuss                   | Teksts          |              | X              |
| Darba kalendārs            | Pārlūkošana        | X            | X              |
| Darba kalendāra dienas numurs | Teksts          | X            | X              |


**Brīvdienas darba kalendārā**

| **Lauki**  | **Datu tips** | **Obligāts** | **Meklējams** |
|-------------|---------------|--------------|----------------|
| Vārds/nosaukums        | Teksts          |              | X              |
| Apraksts | Teksts          | X            | X              |


**Brīvdienu rinda darba kalendārā**

| **Lauki**                        | **Datu tips** | **Obligāts** | **Meklējams** |
|-----------------------------------|---------------|--------------|----------------|
| Brīvdienas datums                      | Vienīgi datums     | X            | X              |
| Vārds/nosaukums                              | Teksts          |              | X              |
| Brīvdienas darba kalendārā             | Pārlūkošana        | X            | X              |
| Brīvdienu rindas numurs darba kalendārā | Teksts          | X            | X              |


**Darba kalendāra laika intervāls**

| **Lauki**                         | **Datu tips** | **Obligāts** | **Meklējams** |
|------------------------------------|---------------|--------------|----------------|
| Uzņēmums                            | Pārlūkošana        |              | X              |
| Beigu laiks                           | Vesels skaitlis  |              | X              |
| Sākuma laiks                         | Vesels skaitlis  |              | X              |
| Darba kalendārs                      | Pārlūkošana        | X            | X              |
| Darba kalendāra diena                  | Pārlūkošana        | X            | X              |
| Darba kalendāra laika intervāla numurs | Teksts          | X            | X              |

## <a name="organization-entities"></a>Organizācijas entītijas

**Uzņēmums**

| **Lauki**   | **Datu tips** | **Obligāts** | **Meklējams** |
|--------------|---------------|--------------|----------------|
| Uzņēmuma kods | Teksts          | X            | X              |
| Vārds/nosaukums         | Teksts          | X            | X              |


**Nodaļa**

| **Lauki**        | **Datu tips** | **Obligāts** | **Meklējams** |
|-------------------|---------------|--------------|----------------|
| Nodaļas numurs | Teksts          | X            | X              |
| Apraksts       | Teksts          |              | X              |
| Vārds/nosaukums              | Teksts          | X            | X              |
| Pamata departaments | Pārlūkošana        |              | X              |


**Valūta**

| **Lauki**         | **Datu tips**  | **Obligāts** | **Meklējams** |
|--------------------|----------------|--------------|----------------|
| Valūtas kods      | Teksts           | X            | X              |
| Valūtas nosaukums      | Teksts           | X            | X              |
| Valūtas precizitāte | Vesels skaitlis   | X            | X              |
| Valūtas simbols    | Teksts           | X            | X              |
| Elementa attēls       | Attēls          |              |                |
| Valūtas kurss      | Decimālskaitlis | X            | X              |
| Organizācija       | Pārlūkošana         | X            | X              |
| Statuss             | Opciju kopa     |              | X              |

## <a name="payroll-entities"></a>Algas elementi

**Apmaksas cikls**

| **Lauki**  | **Datu tips** | **Obligāts** | **Meklējams** |
|-------------|---------------|--------------|----------------|
| Apraksts | Teksts          | X            | X              |
| Biežums   | Opciju kopa    | X            | X              |
| Vārds/nosaukums        | Teksts          | X            | X              |


**Apmaksas periods**

| **Lauki**           | **Datu tips** | **Obligāts** | **Meklējams** |
|----------------------|---------------|--------------|----------------|
| Noklusējuma maksājuma datums | Vienīgi datums     |              | X              |
| Apraksts          | Teksts          |              | X              |
| Izmaksu cikls            | Skatīties          | X            | X              |
| Izmaksas perioda numurs    | Teksts          | X            | X              |
| Perioda beigu datums      | Vienīgi datums     | X            | X              |
| Perioda sākuma datums    | Vienīgi datums     | X            | X              |
| Statuss               | Opciju kopa    |              | X              |


**Algas ienākumu veida kods**

| **Lauki**              | **Datu tips** | **Obligāts** | **Meklējams** |
|-------------------------|---------------|--------------|----------------|
| Apraksts             | Teksts          | X            | X              |
| Iekļaut maksājuma veidā | Opciju kopa    | X            | X              |
| Ir produktīvs           | Divas opcijas   | X            | X              |
| Vārds/nosaukums                    | Teksts          |              | X              |
| Daudzuma vienība           | Opciju kopa    |              | X              |
| Izsekot FMLA stundas        | Divas opcijas   |              | X              |


**Nodokļu reģions**

| **Lauki**        | **Datu tips** | **Obligāts** | **Meklējams** |
|-------------------|---------------|--------------|----------------|
| Pilsēta              | Teksts          |              | X              |
| Valsts vai reģions | Teksts          |              | X              |
| Apgabals            | Teksts          |              | X              |
| Vārds/nosaukums              | Teksts          | X            | X              |
| Novads | Teksts          |              | X              |


**Atvieglojumu aprēķina biežuma izmaksas periods**

| **Lauki**                                      | **Datu tips** | **Obligāts** | **Meklējams** |
|-------------------------------------------------|---------------|--------------|----------------|
| Atvieglojumu aprēķina biežums                   | Pārlūkošana        | X            | X              |
| Atvieglojumu aprēķina biežuma izmaksas perioda numurs | Teksts          | X            | X              |
| Apmaksas periods                                      | Pārlūkošana        | X            | X              |


**Bankas konta izdevumi**

| **Lauki**                       | **Datu tips**  | **Obligāts** | **Meklējams** |
|----------------------------------|----------------|--------------|----------------|
| Apjoms                           | Valūta       |              | X              |
| Summa (pamatvalūta)                    | Valūta       |              | X              |
| Bankas konts                     | Pārlūkošana         | X            | X              |
| Bankas konta izdevumu numurs | Teksts           | X            | X              |
| Uzņēmums                          | Pārlūkošana         | X            | X              |
| Valūta                         | Pārlūkošana         |              | X              |
| Valūtas kurss                    | Decimālskaitlis |              | X              |
| Ir atlikums                     | Divas opcijas    |              | X              |
| Prioritāte                         | Vesels skaitlis   |              | X              |

**Personas identifikācijas dokumenta izdevējiestāde**

| **Lauki**           | **Datu tips** | **Obligāts** | **Meklējams** |
|----------------------|---------------|--------------|----------------|
| Adreses apraksts  | Teksts          |              | X              |
| Adreses 1. rinda       | Teksts          |              | X              |
| Adreses 2. rinda       | Teksts          |              | X              |
| Adreses 3. rinda       | Teksts          |              | X              |
| Pilsēta                 | Teksts          |              | X              |
| Valsts vai reģions    | Opciju kopa    |              | X              |
| Apgabals               | Teksts          |              | X              |
| Apraksts          | Teksts          |              | X              |
| E-pasta adrese                | Teksts          |              | X              |
| Paplašinājums            | Teksts          |              | X              |
| Fakss                  | Teksts          |              | X              |
| Izdevējiestādes nosaukums  | Teksts          | X            | X              |
| Mobilais tālrunis         | Teksts          |              | X              |
| Lapa                 | Teksts          |              | X              |
| Pasta indekss          | Teksts          |              | X              |
| Pasta kastīte      | Teksts          |              | X              |
| Īsziņa                  | Teksts          |              | X              |
| Novads    | Teksts          |              | X              |
| Tālrunis            | Teksts          |              | X              |
| Telekss                | Teksts          |              | X              |
| Tīmekļa vietnes URL          | Teksts          |              | X              |

**Nodarbinātās personas identifikācijas veids**

| **Lauki**                        | **Datu tips**  | **Obligāts** | **Meklējams** |
|-----------------------------------|----------------|--------------|----------------|
| Pieļaujamas vērtības                    | Opciju kopa     |              | X              |
| Valsts vai reģions                 | Teksts           |              | X              |
| Apraksts                       | Teksts           |              | X              |
| Fiksētais garums                      | Vesels skaitlis   |              | X              |
| Identifikācijas numura formāts      | Teksts           |              | X              |
| Tips                              | Opciju kopa     |              | X              |
| Nodarbinātās personas identifikācijas veids | Teksts           | X            | X              |

## <a name="fixed-compensation-entities"></a>Fiksētas atlīdzības elementi

**Atlīdzības fiksētā sistēma**

| **Lauki**                  | **Datu tips** | **Obligāts** | **Meklējams** |
|-----------------------------|---------------|--------------|----------------|
| Uzņēmums                     | Pārlūkošana        | X            | X              |
| Atlīdzības režģis           | Pārlūkošana        |              | X              |
| Valūta                    | Pārlūkošana        | X            | X              |
| Apraksts                 | Teksts          | X            | X              |
| Spēkā stāšanās datums              | Vienīgi datums     | X            | X              |
| Beigu datums             | Vienīgi datums     | X            | X              |
| Nomas noteikums                   | Opciju kopa    | X            | X              |
| Vārds/nosaukums                        | Teksts          | X            | X              |
| Tolerance ārpus diapazona      | Opciju kopa    | X            | X              |
| Algas izmaksas biežums               | Pārlūkošana        | X            | X              |
| Rekomendēšana atļauta      | Divas opcijas   | X            | X              |
| Atsauces punkta iestatījums  | Pārlūkošana        |              | X              |
| Tips                        | Opciju kopa    | X            | X              |

**Atlīdzību režģis**

| **Lauki**                  | **Datu tips** | **Obligāts** | **Meklējams** |
|-----------------------------|---------------|--------------|----------------|
| Uzņēmums                     | Pārlūkošana        | X            | X              |
| Valūta                    | Pārlūkošana        |              | X              |
| Apraksts                 | Teksts          | X            | X              |
| Spēkā stāšanās datums              | Vienīgi datums     |              | X              |
| Beigu datums             | Vienīgi datums     |              | X              |
| Vārds/nosaukums                        | Teksts          | X            | X              |
| Atsauces punkta iestatījums       | Pārlūkošana        | X            | X              |
| Tips                        | Opciju kopa    | X            | X              |

**Atlīdzības līmenis**

| **Lauki**      | **Datu tips** | **Obligāts** | **Meklējams** |
|-----------------|---------------|--------------|----------------|
| Apraksts     | Teksts          |              | X              |
| Vārds/nosaukums            | Teksts          | X            | X              |
| Tips            | Opciju kopa     | X            | X              |

**Atlīdzības algas biežums**

| **Lauki**                  | **Datu tips**   | **Obligāts** | **Meklējams** |
|-----------------------------|-----------------|--------------|----------------|
| Gada pārrēķināšanas koeficients    | Decimālskaitlis  |              | X              |
| Uzņēmums                     | Pārlūkošana          | X            | X              |
| Apraksts                 | Teksts            |              | X              |
| Stundas pārveidošanas koeficients    | Decimālskaitlis  |              | X              |
| Ikmēneša pārveidošanas koeficients   | Decimālskaitlis  |              | X              |
| Vārds/nosaukums                        | Teksts            | X            | X              |
| Periods                      | Opciju kopa      |              | X              |
| Nedēļas pārveidošanas koeficients    | Opciju kopa      |              | X              |


**Atlīdzības atsauces punktu iestatīšana**

| **Lauki**          | **Datu tips**   | **Obligāts** | **Meklējams** |
|---------------------|-----------------|--------------|----------------|
| Uzņēmums             | Pārlūkošana          | X            | X              |
| Atlīdzības veids   | Opciju kopa      | X            | X              |
| Apraksts         | Teksts            | X            | X              |
| Vārds/nosaukums                | Teksts            | X            | X              |

**Atlīdzības raksturojuma punktu iestatīšanas rinda**

| **Lauki**            | **Datu tips**   | **Obligāts** | **Meklējams** |
|-----------------------|-----------------|--------------|----------------|
| Uzņēmums               | Pārlūkošana          | X            | X              |
| Apraksts           | Teksts            | X            | X              |
| Rindas numurs           | Decimālskaitlis  | X            | X              |
| Vārds/nosaukums                  | Teksts            | X            | X              |
| Atsauces punkta iestatījums | Pārlūkošana          | X            | X              |

**Atlīdzības reģions**

| **Lauki**      | **Datu tips** | **Obligāts** | **Meklējams** |
|-----------------|---------------|--------------|----------------|
| Apraksts     | Teksts          | X            | X              |
| Vārds/nosaukums            | Teksts          | X            | X              |

**Kompensācijas struktūra**

| **Lauki**                    | **Datu tips**   | **Obligāts** | **Meklējams** |
|-------------------------------|---------------  |--------------|----------------|
| Apjoms                        | Valūta        |              | X              |
| Pamatsumma                   | Valūta        |              | X              |
| Uzņēmums                       | Pārlūkošana          | X            | X              |
| Kompensācijas struktūras numurs | Teksts            | X            | X              |
| Valūta                      | Pārlūkošana          |              | X              |
| Valūtas kurss                 | Decimālskaitlis  |              | X              |
| Režģis                          | Pārlūkošana          | X            | X              |
| Līmenis                         | Pārlūkošana          | X            | X              |
| Atsauces punkts               | Pārlūkošana          | X            | X              |
| Atsauces punkta iestatījums    | Pārlūkošana          | X            | X              |

**Fiksētas atlīdzības notikums**

| **Lauki**            | **Datu tips**   | **Obligāts** | **Meklējams** |
|-----------------------|-----------------|--------------|----------------|
| Uzņēmums               | Pārlūkošana          | X            | X              |
| Apraksts           | Teksts            | X            | X              |
| Notikuma veids            | Opciju kopa      | X            | X              |
| Ir aktīvs             | Divas opcijas     | X            |                |
| Vārds/nosaukums                  | Teksts            | X            | X              |

## <a name="entity-relationship-models"></a>Entitījas attiecību modeļi

### <a name="worker"></a>Nodarbinātais
![Nodarbinātais](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Darbs un amats
![Darbs un amats](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Priekšrocības
![Priekšrocības](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensācija
![Kompensācija](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Pamest
![Pamest](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Darba kalendārs
![Darba kalendārs](./media/HCMCommon-work-calendar-entity-diagram.png)
