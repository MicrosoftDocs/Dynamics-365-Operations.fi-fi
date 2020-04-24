---
title: Määritä Common Data Service -integraatio
description: Voit ottaa integroinnin Common Data Servicen ja Dynamics 365 Human Resourcesin välillä käyttöön tai poistaa sen käytöstä. Voit myös tarkastella synkronointitietoja, tyhjentää seurantatiedot ja synkronoida yksikön uudelleen, mikä helpottaa näiden kahden ympäristön välisten tieto-ongelmien vianmääritystä.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: 04280aa0908ed6dab86ef87b6c1843e4b4348e08
ms.sourcegitcommit: c9657b44adb9c1a77c7c2f6ab63a58cc848974ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198419"
---
# <a name="configure-common-data-service-integration"></a>Määritä Common Data Service -integraatio

Voit ottaa integroinnin Common Data Servicen ja Dynamics 365 Human Resourcesin välillä käyttöön tai poistaa sen käytöstä. Voit myös tarkastella synkronointitietoja, tyhjentää seurantatiedot ja synkronoida yksikön uudelleen, mikä helpottaa näiden kahden ympäristön välisten tieto-ongelmien vianmääritystä.

Kun poistat integroinnin käytöstä, käyttäjät voivat tehdä muutoksia Human Resourcesissa tai Common Data Servicessä, mutta näitä muutoksia ei synkronoida näiden kahden ympäristön välillä.

Oletusarvoisesti Human Resourcesin ja Common Data Servicen tietojen integrointi on poistettu käytöstä.

Integrointi voi kannattaa poistaa käytöstä seuraavissa tilanteissa:

- Olet täyttämässä dataa tietojen hallintakehyksen kautta ja sinun on tuotava tiedot useita kertoja, jotta saat ne oikeaan tilaan.

- Tietoihin liittyy ongelmia joko Human Resourcesissa tai Common Data Servicessä. Jos poistat integroinnin käytöstä, voit poistaa tietueen yhdestä ympäristöstä poistamatta sitä toisessa ympäristössä. Kun otat integroinnin takaisin käyttöön, sen ympäristön tietue, josta sitä ei poistettu, synkronoidaan siihen ympäristöön, josta se poistettiin. Synkronointi alkaa seuraavan kerran, kun **Common Data Servicen integroinnin toteutumattoman pyynnön synkronointi** -erätyö suoritetaan.

> [!WARNING]
> Kun poistat tietojen integroinnin käytöstä, varmista, ettet muokkaa samaa tietuetta molemmissa ympäristöissä. Kun otat integroinnin takaisin käyttöön, viimeksi muokattu tietue synkronoidaan. Näin ollen, jos et tehnyt samoja muutoksia tietueeseen molemmissa ympäristöissä, tietoja voidaan menettää.

## <a name="access-the-common-data-service-integration-page"></a>Common Data Servicen integrointisivun käyttö

1. Valitse siinä Human Resources -esiintymässä, jossa haluat tarkastella tai määrittää Common Data Servicen kanssa integroinnin asetuksia, **Järjestelmän hallinta** -ruutu.

    [![Järjestelmän hallinta -ruutu](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Valitse **Linkit**-välilehti.

    [![Linkit-välilehti](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Valitse **Integroinnit**-kohdassa **Common Data Servicen määritys**.

    [![Common Data Servicen määrityslinkki](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Human Resourcesin ja Common Data Servicen tietojen integroinnin käyttöönotto ja käytöstä poistaminen

- Ota integrointi käyttöön asettamalla **Ota integrointi Common Data Serviceeen** -asetuksen arvoksi **Kyllä**.

    > [!NOTE]
    > Kun otat integroinnin käyttöön, tiedot synkronoidaan seuraavan kerran, kun **Common Data Servicen integroinnin toteutumattoman pyynnön synkronointi** -erätyö suoritetaan seuraavan kerran. Kaikkien tietojen pitäisi olla käytettävissä, kun erätyö on valmis.

- Voit poistaa integroinnin käytöstä määrittämällä asetukseksi **Ei**.

[![Common Data Service -integroinnin käyttöönotto tai käytöstä poisto](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>Integrointitietojen tarkastelu

**Common Data Service** -integroinnin -sivun **Ylläpito**-pikavälilehdessä voit nähdä, miten tietueet linkittyvät yhteen Human Resourcesin ja Common Data Servicen välillä.

- Jos haluat tarkastella yksikön tietueita, valitse yksikkö **CDS-yksikön nimi** -kentässä. Ruudukossa näkyvät kaikki valittuun yksikköön linkitetyt tietueet.

[![Yksikön tietueen tarkasteleminen](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> Kaikkia Common Data Service -yksikköjä ei tällä hetkellä ole luettelossa. Ruudukossa näkyvät vain ne yksiköt, jotka tukevat mukautettujen kenttien käyttöä. Uusia yksikköjä tulee saataville jatkuvien Human Resources -julkaisujen myötä.

Ruudukko sisältää seuraavat kentät:

- **CDS-yksikön nimi** – Yksikön nimi Common Data Servicessä.
- **CDS-yksikköviite** – Tunnus, jota Common Data Service käyttää yksikön tunnistamiseen. Tämä arvo vastaa Human Resourcesin **RecId**-arvoa. Löydät tunnuksen, kun avaat Common Data Service -yksikön Microsoft Excelissä.
- **Human Resources -yksikön nimi** – Yksikkö, joka viimeksi synkronoi tietoja Common Data Serviceen. Yksiköllä voi olla joko Common Data Service -etuliite tai muu etuliite.
- **Human Resources -viite** – **RecId**-arvo, joka tietueelle on määritetty Human Resourcesissa.
- **Poistettiin CDS:stä** – Arvo, joka ilmaisee, onko tietue poistettu Common Data Servicestä.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Poista Human Resourcesissa olevan tietueen liitos Common Data Servicestä

Jos kohtaat ongelmia Human Resourcesin ja Common Data Servicen välisen tietojen synkronoinnin aikana, voit ehkä ratkaista ne tyhjentämällä seurannan ja sallimalla seurantataulukon uudelleensynkronoinnin. Jos poistat liitoksen ja muutat tai poistat tietueen Common Data Servicessä, muutoksia ei synkronoida Human Resourcesiin. Jos teet muutoksia Human Resourcesissa, uusi seurantatietue luodaan ja päivitetään Common Data Servicessä.

- Jos haluat poistaa tietueen liitoksen Human Resourcesin ja Common Data Servicen väliltä, valitse yksikkö **CDS-yksikön nimi** -kentästä ja valitse sitten **Tyhjennä seurantatiedot**.

[![Seurantatietojen tyhjennys](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

Katso seuraava menettely, jos haluat suorittaa yksikölle täydellisen synkronoinnin seurannan tyhjentämisen jälkeen.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Synkronoi yksikkö Human Resourcesin ja Common Data Servicen välillä

Käytä tätä menetelmää seuraavissa tilanteissa:

- Common Data Servicen muutokset näkyvät liian hitaasti henkilöstöhallinnossa.

- Seurantataulukko on päivitettävä seurannan poistamisen jälkeen.

Voit suorittaa täyden synkronoinnin yksikölle henkilöstöhallinnon ja Common Data Servicen välillä:

1. Valitse yksikkö **CDS-yksikkönimi** -kentässä.

2. Valitse **Synkronoi nyt**.

[![Täyden synkronoinnin suoritus](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


