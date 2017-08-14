---
title: "Käyttöomaisuuden hallinnan työtila"
description: "Tässä ohjeaiheessa on tietoja käyttöomaisuuden hallinnan työtilasta. Työtilassa on järjestelmään vietyyn käyttöomaisuuteen liittyviä tietoja. Siinä on yhteenvetonäkymä ja analytiikkanäkymä."
author: saraschi
manager: AnnBe
ms.date: 06/06/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 69f728c5b5897d7210941643d2c7d0d7abf054fa
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---

# <a name="fixed-asset-management-workspace"></a>Käyttöomaisuuden hallinnan työtila

[!include[banner](../includes/banner.md)]

**Käyttöomaisuuden hallinnan** työtilassa on järjestelmään vietyyn käyttöomaisuuteen liittyviä tietoja. Työtilassa on yhteenvetonäkymä ja analytiikkanäkymä. **Oma työ** -välilehdessä on yhteenvetoruutuja, tietoja käyttöomaisuudesta ja nykyisen yrityksen käyttöomaisuuteen liittyviä tietoja. Voit lisätä työtilassa analyysitietoja myös suoraan Power BI:n analytiikkaosaan. **Analytiikka – kaikki yritykset** -välilehti näyttää Microsoft Power BI:n ominaisuuksien avulla kaikkien yritysten käyttöomaisuuteen liittyviä visualisointeja.

## <a name="my-work"></a>Oma työ

### <a name="summary"></a>Yhteenveto

**Yhteenveto**-osan ruuduista saa yleiskatsauksen käyttöomaisuudesta. Tietoja on esimerkiksi vielä ostamattoman käyttöomaisuuden, kuluvan vuoden aikana ostetun käyttöomaisuuden ja kuluvan vuoden aikana poistetun käyttöomaisuuden mittareista. **Yhteenveto**-osasta pääsee myös siirtymään nopeasti **Käyttöomaisuus**-luettelosivulle, erän poistoehdotukseen ja käyttöomaisuuden kirjauskansioon.

### <a name="find-fixed-assets"></a>Etsi käyttöomaisuus

Voit hakea **Etsi käyttöomaisuus** -osassa nopeasti käyttöomaisuuseriä antamalla käyttöomaisuuden numeron, ryhmän, nimen, sijainnin tai vastuuhenkilön. Kaikki hakua vastaavat käyttöomaisuuserät näkyvät luettelossa.

Voit tarkastella luettelosta seuraavia sivuja:

 - Käyttöomaisuuden **Tiedot**-sivu
 - Kaikkien käyttöomaisuuteen liitettyjen kirjojen **Kirjat**-sivu
 - **Käyttöomaisuuden arvostukset** -sivu

### <a name="valuations"></a>Arvostukset

**Käyttöomaisuuden arvostukset** -sivun avulla näet yhdellä sivulla tärkeimmät käyttöomaisuutta koskevat tiedot sekä tiedot kaikista käyttöomaisuuteen liitetyistä kirjoista. Sivun vasemman yläkulman **Saldot**-vaihtoehto näyttää kunkin käyttöomaisuuteen liitetyn kirjan nykyisen arvostuksen. Voit porautua arvoista taaksepäin tarkistamaan, mistä tapahtumista yhteenvetoarvo tarkkaan ottaen koostuu. Sivun vasemman yläkulman **Profiili**-vaihtoehto näyttää kunkin käyttöomaisuuteen liitetyn kirjan poistoaikataulun.

Voit käyttää **Käyttöomaisuuden arvostukset** -sivua **Käyttöomaisuuden hallinta** -työtilasta tai **Käyttöomaisuus**-luettelosivulta.

### <a name="related-information"></a>Aiheeseen liittyviä tietoja

Voi siirtyä suoraan **Kirjojen asetukset** -sivulle, **Käyttöomaisuustapahtumien kysely** -sivulle ja useisiin raportteihin työtilan **Liittyvät tiedot** -osan linkeistä.

### <a name="analytics--all-companies"></a>Analytiikka – kaikki yritykset

**Analytiikka**-sivulla on tärkeitä kaikkia järjestelmän yrityksiä koskevia käyttöomaisuuden mittareita. Tämän välilehden käyttöä hallitaan Näytä kaikkien yritysten käyttöomaisuuserien analytiikka -suojausoikeuksilla.

Seuraavassa taulukossa on näkyvissä kullakin raporttisivulla käytettävissä olevat visualisoinnit.

| Raporttisivu            | Visualisointi        |
|------------------------|----------------------|
| Käyttöomaisuuden arvostukset | Nettokirjanpitoarvo yhteensä |
| Käyttöomaisuuden arvostukset | Nettokirjanpitoarvo käyttöomaisuusryhmän mukaan |
| Käyttöomaisuuden arvostukset | Hankinta-arvot |
| Käyttöomaisuuden arvostukset | Käytöstäpoiston arvot |
| Käyttöomaisuuden arvostukset | Käyttöomaisuustiedot |
| Arvostuskartat        | Nettokirjanpitoarvo yhteensä |
| Arvostuskartat        | Käyttöomaisuuserien sijainnit |
| Arvostuskartat        | Käyttöomaisuustiedot |

Voit tarkastella analytiikkaa tietoihin päivittämällä ensin AssetTransactionMeasure-koostemitan **Yksikkösäilö**-sivulla.

