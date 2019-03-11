---
title: Kulunhallinnan työnkulkujen määrittäminen
description: Voit määrittää työnkulkuprosessin, jota matka- ja kuluasiakirjojen tarkistamiseen ja hyväksyntään.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8294aaa344e3cb6b79fa4f33f368258ca19c8205
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "355722"
---
# <a name="set-up-workflows-for-expense"></a>Kulunhallinnan työnkulkujen määrittäminen

[!include [banner](../includes/banner.md)]

 Voit määrittää työnkulkuprosessin, jota matka- ja kuluasiakirjojen tarkistamiseen ja hyväksyntään. Asiakirjat, joille työnkulun voi määrittää, ovat muun muassa kuluraportteja, matkustusehdotuksia ja käteisennakkopyyntöjä.

Työnkulku vastaa liiketoimintaprosessia. Se määrittää, miten asiakirja "kulkee" järjestelmässä, ja osoittaa, kenen on saatettava tehtävä valmiiksi tai hyväksyttävä asiakirja. Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:

-   **Yhdenmukaiset prosessit** — Voit määrittää hyväksyntäprosessin tietyille asiakirjoille kuten ostoehdotuksille ja kuluraporteille. Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.

-   Prosessin näkyvyys — Voit seurata tietyn työnkulun esiintymän tilaa, historiaa ja suorituskykyarvoja. Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.

-   Keskitetty työluettelo — Käyttäjät voivat tarkastella keskitettyä työluetteloa, joka sisältää työnkulun tehtävät ja niille annetut hyväksynnät. 

**Voit luoda seuraavat työnkulkutyypit**

Seuraavassa taulukossa on esitetty erityyppisiä työnkulkuja, joita voit luoda **kulunhallinnassa**.


|              <strong>Tyyppi</strong>              |                   <strong>Käytä tätä tyyppiä</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Kuluraportti</strong>         |            Kuluraporttien hyväksyntätyönkulkujen luominen.             |
|  <strong>Kuluraportin automaattinen kirjaaminen</strong>   |        Luo automaattisen kirjaamisen työnkulut kuluraportteja varten.        |
|       <strong>Kulurivin nimike</strong>        |     Kuluraporttien rivinimikkeiden hyväksyntätyönkulkujen luominen.      |
| <strong>Kulurivinimikkeen automaattinen kirjaaminen</strong> | Kuluraporttien rivinimikkeiden automaattisten kirjaustyönkulkujen luominen. |
|       <strong>Matkahankinta</strong>       |          Luo matkustusehdotusten hyväksyntätyönkulkuja.           |
|      <strong>Käteisennakkopyyntö</strong>      |         Luo hyväksyntätyönkulkuja käteisennakkopyynnöille.          |
|        <strong>Arvonlisäveron palautus</strong>        | Luo arvonlisäveron (ALV) palautuksen hyväksyntätyönkulkuja.  |

