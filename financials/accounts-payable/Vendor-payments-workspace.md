---
title: "Toimittajan maksujen työtila"
description: "Tässä ohjeaiheessa on tietoja toimittajamaksujen työtilasta. Toimittajamaksujen työtilassa näkyy toimittajan maksujen käsittelyyn liittyviä tietoja."
author: twheeloc
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: 
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 3abf4b151b177095b71d44e9a6c9fd8541eaa64e
ms.openlocfilehash: 4011a2383fe4556b730fa0b6353ba0b9773a4eec
ms.contentlocale: fi-fi
ms.lasthandoff: 06/14/2017

---

# <a name="vendor-payments-workspace"></a>Toimittajan maksujen työtila

[!include[banner](../includes/banner.md)]

**Toimittajamaksut** -työtilassa näkyy toimittajan maksujen käsittelyyn liittyviä tietoja. Työtilassa on **Oma työ** -näkymä ja **Analytiikka**-sivu. **Oma työ** -näkymä näyttää yhteenvetoruudut, toimittajatapahtumaruudukot ja liittyvän toimittajan tiedot. **Analytiikka**-sivu käyttää Microsoft Power BI:n ominaisuuksien avulla toimittajan maksuihin liittyviä visuaalisia tietoja.

## <a name="my-work-view"></a>Oma työ -näkymä

### <a name="summary-tiles"></a>Yhteenvetoruudut

**Yhteenveto**-osan ruudut antavat yleiskuvan maksutietojesi tilasta. Voit tarkastella maksukirjauskansioista, joita ei ole vielä kirjattu, laskuja, joiden eräpäivä on ohitettu, ja kaikki toimittajat, jotka ovat pidossa. **Yhteenveto**-osassa voit luoda uuden maksuajon.

**Yhteenveto**-osan tiedot on tarkoitettu yritykselle, johon olet kirjautunut.

### <a name="vendor-transactions-grids"></a>Toimittajatapahtumaruudukot

**Toimittajatapahtumat**-osa sisältää ruudukot, joissa näkyvät laskut, jotka ovat erääntyneet, ja maksut, joita ei ole maksettu. **Erääntyneet laskut** -ruudukossa voit tarkastella valitun laskun maksuhistoriaa. **Maksamattomat laskut** -ruudukossa voit tarkastella valitun laskun maksuhistoriaa ja maksaa laskun.

Keskitettyjen maksujen kirjanpitäjät voivat käyttää suodatinta, joka näkyy kunkin ruudukon yläosassa, yrityksen valintaa. Ruudukko suodatetaan siten, että siinä näkyy vain yrityksiä, jotka on määritetty keskitettyjen maksujen organisaatiohierarkiassa, jota keskitettyjen maksujen kirjanpitäjällä on oikeus tarkastella.

**Toimittajatapahtumat**-osan **Etsi tapahtumia** -välilehden avulla voit etsiä toimittajatapahtumaa.

### <a name="related-information"></a>Aiheeseen liittyviä tietoja

Voit tarkastella **Ostoreskontran erääntyminen** -raporttia ja **Maksuyhteenveto päivän mukaan** -raporttia työtilan **Liittyviä tietoja** linkkien avulla.

## <a name="analytics-page"></a>Analytiikka-sivu

**Analytiikka**-sivulla on tärkeitä mittareita, kuten erääntyneet toimittajalaskut ja toimittajalaskuja, jotka erääntyvät myöhemmin. Tällä sivulla on yhdeksän raporttisivua. Yksi sivu sisältää yhteenvedon ja kahdeksalla muulla sivulla on tietoja ostoreskontran maksumittareista.

Seuraavassa taulukossa on näkyvissä kullakin raporttisivulla käytettävissä olevat visualisoinnit.

| Raporttisivu | Visualisointi |
|-------------|---------------|
| Toimittajan maksujen yleiskatsaus | <ul><li>Erääntyneet laskut</li><li>Tänään erääntyvät laskut</li><li>Saadut alennukset / annetut alennukset</li><li>Tulevaisuudessa erääntyvät laskut käteisalennuspäivämäärän mukaan</li><li>Tulevaisuudessa erääntyvät laskut eräpäivämäärän mukaan</li><li>Myöhässä maksetut laskut / ajoissa maksetut laskut</li><li>Maksun työnkulun määritys</li><li>Toimittaja-/asiakassaldo</li><li>Avoimet laskut, joiden maksu on pidossa</li></ul> |
| Erääntyneet laskut | <ul><li>Erääntyneet laskut</li><li>Erääntyneiden laskujen tiedot</li><li>Avoimien laskujen yhteissumma</li><li>Erääntyneet laskut toimittajaryhmittäin</li><li>Erääntyneet laskut yrityksen mukaan</li></ul> |
| Tänään erääntyvät laskut | <ul><li>Tänään erääntyvät laskut</li><li>Tänään erääntyvien laskujen tiedot</li><li>Tänään erääntyvät laskut yrityksen mukaan</li><li>Tänään erääntyvät laskut toimittajaryhmittäin</li></ul> |
| Saadut alennukset / annetut alennukset | <ul><li>Saadut alennukset / annettu alennus</li><li>Saadut alennukset / annettu alennus -tiedot</li><li>Saadut alennukset / annettu alennus yrityksittäin</li><li>Saadut alennukset / annettu alennus toimittajaryhmittäin</li></ul> |
| Tulevaisuudessa erääntyvät laskut | <ul><li>Tulevaisuudessa erääntyvät laskut</li><li>Tulevaisuudessa erääntyvien laskujen tiedot</li><li>Tulevaisuudessa erääntyvät laskut yrityksittäin</li><li>Tulevaisuudessa erääntyvät laskut toimittajaryhmittäin</li><li>Tulevaisuudessa erääntyvät laskut käteisalennuspäivämäärän mukaan</li><li>Tulevaisuudessa erääntyvät laskut eräpäivämäärän mukaan</li></ul> |
| Myöhässä maksetut laskut | <ul><li>Eräpäivän jälkeen maksetut laskut</li><li>Eräpäivän jälkeen maksettujen laskujen tiedot</li><li>Eräpäivän jälkeen maksettujen laskujen tiedot yrityksittäin</li><li>Eräpäivän jälkeen maksettujen laskujen toimittajaryhmittäin</li><li>Myöhässä maksetut laskut vs. ajoissa maksetut laskut</li></ul> |
| Maksun työnkulku | <ul><li>Toimittajamaksujen työnkulkuesiintymät</li><li>Toimittajamaksujen työnkulkuesiintymät / hyväksyjä</li><li>Toimittajamaksujen työnkulkuesiintymät / yritys</li><li>Työnkulun keskimääräinen pituus (päiviä) / hyväksyjä</li></ul> |
| Toimittaja-/asiakassaldo | <ul><li>Toimittaja-/asiakassaldo</li><li>Toimittaja-/asiakassaldo yrityksittäin</li><li>Toimittaja-/asiakassaldon tiedot</li></ul> |
| Laskun pidossa oleva maksu | <ul><li>Laskun pidossa oleva maksu</li><li>Laskun pidossa oleva maksu -yksityiskohdat</li><li>Laskun pidossa oleva maksu yrityksittäin</li><li>Laskun pidossa oleva maksu toimittajaryhmittäin</li></ul> |

