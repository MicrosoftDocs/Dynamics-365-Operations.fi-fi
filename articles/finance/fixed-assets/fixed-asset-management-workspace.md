---
title: Käyttöomaisuuden hallinnan työtila
description: Tässä artikkelissa on tietoja käyttöomaisuuden hallinnan työtilasta. Työtilassa on järjestelmään vietyyn käyttöomaisuuteen liittyviä tietoja. Siinä on yhteenvetonäkymä ja analytiikkanäkymä.
author: moaamer
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetWorkspace
audience: Application User
ms.reviewer: kfend
ms.assetid: ''
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 95b45a91cd201a6d3a4817c315053e98a7693e05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894052"
---
# <a name="fixed-asset-management-workspace"></a>Käyttöomaisuuden hallinnan työtila

[!include [banner](../includes/banner.md)]

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

**Analytiikka**-sivulla on tärkeitä kaikkia järjestelmän yrityksiä koskevia käyttöomaisuuden mittareita. Tämän välilehden käyttöä hallitaan Näytä kaikkien yrityksen käyttöomaisuuserien analytiikka -suojausoikeuksien avulla.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
