---
title: "Tietojen vahvistuksen työtila"
description: "Voit seurata tietojen tarkistuksen tarkistusluettelon työtilassa eri yritysten, alueiden ja henkilöiden tarkistusprosesseja. Tarkistusluettelon voidaan käyttää uudessa käyttöönotossa, päivityksen jälkeen tai siirron jälkeen."
author: bking
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: bking
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 447fd87cb2f71147d7a9f6476f4ed9e12d75640a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="data-validation-workspace"></a>Tietojen vahvistuksen työtila

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa on **tietojen tarkistuksen tarkistusluettelon työtilan** ja liitettyjen määritysten yleiskatsaus.

## <a name="data-validation-checklist-workspace"></a>Tietojen tarkistuksen tarkistusluettelon työtila

Voit seurata **tietojen tarkistuksen tarkistusluettelon** työtilassa eri yritysten, alueiden ja henkilöiden tarkistusprosesseja. Tarkistusluettelon voidaan käyttää uudessa käyttöönotossa, päivityksen jälkeen tai siirron jälkeen. **Tietojen tarkistuksen tarkistusluettelon** työtilan näkymän mukaan näkyvissä on kaikki tietojen tarkistusprojektin tehtävät ja tilat tai vain sinulle määritetyt tehtävät.

Valitse ensin tietojen tarkistuksen tarkistusluettelo työtilan yläosassa. Kaikki työtilassa näkyvät tiedot suodatetaan valitun tietojen tarkistusprojektin mukaan.

### <a name="summary-tiles"></a>Yhteenvetoruudut

**Yhteenveto**-ruudut sisältävät prosessin yleiskuvauksen. Voit seurata mittareiden avulla voit seurata tietojen tarkistusprosessia. Näet prosessin kaikki jäljellä olevat tehtävät, valmiit tehtävät, meneillään olevat tehtävät ja vielä aloittamattomat tehtävät. Nämä tiedot koskevat kaikkia valittuun tietojen tarkistusprojektiin liittyviä yrityksiä.

### <a name="tasks-and-status-section"></a>Tehtävät ja tila -osa

Tietojen tarkistusprojektin kokonaistila näkyy **Tehtävät ja tilat** -osiossa eri tavoin: tila yrityksen, alueen tai tehtäväluettelon mukaan. Voit valita suodattimen, kun haluat tarkastella tietyn yrityksen tilaa. Kukin tilavälilehti sisältää erittelyn sekä valmistuneiden prosenttiosuuden että jäljellä olevien tehtävien määrän mukaan.

Viimeinen välilehti sisältää yksityiskohtaisen kaikki tehtävät sisältävän tehtäväluettelon. Tässä luettelossa on koko tehtäväluettelo.
Tehtäväluettelon voi suodattaa useilla eri tavoilla. Muuta tehtävän tila tai määritä tehtävä valitsemalla **Muokkaa tehtävää**. Tarkastele tehtävän liitteitä valitsemalla **Liitteet**.

Tehtävän nimi on Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition -sivun tai muun sellaisen verkkosivun hyperlinkki, jolla käyttäjä suorittaa työn valmiiksi. Voit määrittää hyperlinkin **Valikkovaihtoehdon nimi** -kentässä, kun muokkaat tehtävää tai luot sen **Konfiguroi tietojen tarkistusprojekti** -lomakkeessa.

Voit liittää tehtäviin tiedostoja, huomautuksia, kuvia ja URL-osoitteita **Liitteet**-toiminnon avulla. Voit liittää esimerkiksi tehtävälle tulostetun raporttitiedoston. Tehtävän **Liite**-sarakkeessa näkyy kuvake, jos liite on määritetty.

**Täyttäjä**-vaihtoehto täytetään automaattisesti tehtävän valmistumisen jälkeen tehtävän suorittaneen työntekijän nimellä. **Valmistumispäivämäärä**-kenttään päivitetään automaattisesti kuluva päivämäärä ja kellonaika.

### <a name="configure-data-validation-project-page"></a>Konfiguroi tietojen tarkistusprojekti -sivu

Ennen kuin **tietojen tarkistuksen tarkistusluettelon** työtilaa voi käyttää, prosessi on määritettävä **Konfiguroi tietojen tarkistusprojekti** -sivulla. (Valitse **Työtilat** \> **Tietojen tarkistuksen tarkistusluettelo** \> **Konfiguroi tietojen tarkistusprojekti**.)

### <a name="task-areas"></a>Tehtäväalueet

Tehtäväalueiden avulla voi ryhmitellä tietojen tarkistustehtäviä loogisiin omistusoikeuden alueisiin organisaatiossa. Tehtäväalueina voidaan käyttää esimerkiksi ostoreskontraa, myyntireskontraa tai kirjanpitoa.

**Valikkovaihtoehdon nimi** liitetään tehtävän työhön. Sitä voidaan käyttää suoraan työtilan tehtävälinkin liittyvältä sivulta. Esimerkiksi tietojen tarkistustehtävä, jolla ostoreskontran **ostoreskontran erääntymisraportti** suoritetaan, voidaan linkittää **Ostoreskontran erääntymisraportti** -sivulle.

