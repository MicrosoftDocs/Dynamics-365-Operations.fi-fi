---
title: Määritä Dataverse -integraatio
description: Voit ottaa integroinnin Microsoft Dataversen ja Dynamics 365 Human Resourcesin välillä käyttöön tai poistaa sen käytöstä. Voit myös tarkastella synkronointitietoja, tyhjentää seurantatiedot ja synkronoida taulukon uudelleen, mikä helpottaa näiden kahden ympäristön välisten tieto-ongelmien vianmääritystä.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf406a954f5bb8b49627b58a901d0721cdad407b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890025"
---
# <a name="configure-dataverse-integration"></a>Määritä Dataverse -integraatio

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit ottaa integroinnin Microsoft Dataversen ja Dynamics 365 Human Resourcesin välillä käyttöön tai poistaa sen käytöstä. Voit myös tarkastella synkronointitietoja, tyhjentää seurantatiedot ja synkronoida taulukon uudelleen, mikä helpottaa näiden kahden ympäristön välisten tieto-ongelmien vianmääritystä.

> [!NOTE]
> Lisätietoja Dataversesta (aiemmin Common Data Service) ja terminologiapäivityksistä on kohdassa [Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Kun poistat integroinnin käytöstä, käyttäjät voivat tehdä muutoksia Human Resourcesissa tai Dataversessä, mutta näitä muutoksia ei synkronoida näiden kahden ympäristön välillä.

Oletusarvoisesti Human Resourcesin ja Dataversen tietojen integrointi on poistettu käytöstä.

Integrointi voi kannattaa poistaa käytöstä seuraavissa tilanteissa:

- Olet täyttämässä dataa tietojen hallintakehyksen kautta ja sinun on tuotava tiedot useita kertoja, jotta saat ne oikeaan tilaan.

- Tietoihin liittyy ongelmia joko Human Resourcesissa tai Dataversessä. Jos poistat integroinnin käytöstä, voit poistaa tietueen yhdestä ympäristöstä poistamatta sitä toisessa ympäristössä. Kun otat integroinnin takaisin käyttöön, sen ympäristön tietue, josta sitä ei poistettu, synkronoidaan siihen ympäristöön, josta se poistettiin. Synkronointi alkaa seuraavan kerran, kun **Dataversen integroinnin toteutumattoman pyynnön synkronointi** -erätyö suoritetaan.

> [!WARNING]
> Kun poistat tietojen integroinnin käytöstä, varmista, ettet muokkaa samaa tietuetta molemmissa ympäristöissä. Kun otat integroinnin takaisin käyttöön, viimeksi muokattu tietue synkronoidaan. Näin ollen, jos et tehnyt samoja muutoksia tietueeseen molemmissa ympäristöissä, tietoja voidaan menettää.

## <a name="access-the-dataverse-integration-page"></a>Dataversen integrointisivun käyttö

1. Valitse siinä Human Resources -esiintymässä, jossa haluat tarkastella tai määrittää Dataversen kanssa integroinnin asetuksia, **Järjestelmän hallinta** -ruutu.

    [![Järjestelmän hallinta -ruutu](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Valitse **Linkit**-välilehti.

    [![Linkit-välilehti](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Valitse **Integroinnit**-kohdassa **Dataversen määritys**.

    [![Dataversen määrityslinkki](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Human Resourcesin ja Dataversen tietojen integroinnin käyttöönotto ja käytöstä poistaminen

- Ota integrointi käyttöön asettamalla **Ota Dataverse -integrointi käyttöön** -asetuksen arvoksi **Kyllä** **Microsoft Dataverse -integrointi** -sivulla.

    > [!NOTE]
    > Kun otat integroinnin käyttöön, tiedot synkronoidaan seuraavan kerran, kun **Dataversen integroinnin toteutumattoman pyynnön synkronointi** -erätyö suoritetaan seuraavan kerran. Kaikkien tietojen pitäisi olla käytettävissä, kun erätyö on valmis.

- Voit poistaa integroinnin käytöstä määrittämällä asetukseksi **Ei**.

[![Dataverse -integroinnin käyttöönotto tai käytöstä poisto](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> On suositeltavaa, että Dataverse -integrointi poistetaan käytöstä, kun tiedonsiirtotehtäviä suoritetaan. Suurten tietomäärien lataaminen voi vaikuttaa suorituskykyyn paljon. Esimerkiksi 2 000 työntekijän tietojen lataaminen voi kestää useita tunteja, jos integrointi on käytössä. Jos se ei ole käytössä, aikaa voi kulua alle tunti. Tässä esimerkissä annetut numerot ovat vain esittelytarkoituksia varten. Tietojen tuomiseen kuluvat tarkka aikamäärä voi vaihdella paljon. Se riippuu useista tekijöistä.

## <a name="view-data-integration-details"></a>Integrointitietojen tarkastelu

**Microsoft Dataverse** -integroinnin -sivun **Ylläpito**-pikavälilehdessä voit nähdä, miten rivit linkittyvät yhteen Human Resourcesin ja Dataversen välillä.

- Voit tarkastella taulun rivejä valitsemalla taulun **Dataverse-taulu** -kentästä. Ruudukossa näkyvät kaikki valittuun taulukkoon linkitetyt rivit.

> [!NOTE]
> Kaikkia Dataverse-taulukoita ei tällä hetkellä ole luettelossa. Ruudukossa näkyvät vain ne taulukot, jotka tukevat mukautettujen kenttien käyttöä. Uusia taulukoita tulee saataville jatkuvien Human Resources -julkaisujen myötä.

Ruudukko sisältää seuraavat kentät:

- **Dataverse-taulukko** – Dataverse-taulukon nimi.
- **Dataverse-taulukkoviite** – Tunnus, jota Dataverse käyttää tietueen tunnistamiseen. Tämä arvo vastaa Human Resourcesin **RecId**-arvoa. Löydät tunnuksen, kun avaat Dataverse-taulukon Microsoft Excelissä.
- **Human Resources -yksikön nimi** – Human Resources -yksikkö, joka viimeksi synkronoi tietoja Dataverseen. Yksiköllä voi olla joko Dataverse -etuliite tai muu etuliite.
- **Human Resources -viite** – **RecId**-arvo, joka tietueelle on määritetty Human Resourcesissa.
- **Poistettu Dataversestä** – Arvo, joka ilmaisee, onko rivi poistettu Dataversestä.

> [!NOTE]
> Human Resources -tietueet vastaavat rivejä Dataversessä.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Poista Human Resources -tietueen liitos Dataverse-rivistä

Jos kohtaat ongelmia Human Resourcesin ja Dataversen välisen tietojen synkronoinnin aikana, voit ehkä ratkaista ne tyhjentämällä seurannan ja sallimalla seurantataulukon uudelleensynkronoinnin. Jos poistat liitoksen ja muutat tai poistat rivin Dataversessä, muutoksia ei synkronoida Human Resourcesiin. Jos teet muutoksia Human Resourcesissa, uusi seurantatietue luodaan ja rivi päivitetään Dataversessä.

- Jos haluat poistaa liitoksen Human Resources -tietueen ja Dataverse-rivin väliltä, valitse taulukko **Dataverse-taulukko** -kentästä ja valitse sitten **Tyhjennä seurantatiedot**.

[![Seurantatietojen tyhjennys](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

Katso seuraava menettely, jos haluat suorittaa taulukolle täydellisen synkronoinnin seurannan tyhjentämisen jälkeen.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Synkronoi taulukko Human Resourcesin ja Dataversen välillä

Käytä tätä menetelmää seuraavissa tilanteissa:

- Dataversen muutokset näkyvät liian hitaasti henkilöstöhallinnossa.

- Seurantataulukko on päivitettävä seurannan poistamisen jälkeen.

Voit suorittaa täyden synkronoinnin taulukolle Human Resourcesin ja Dataversen välillä:

1. Valitse taulukko **Dataverse-taulukko** -kentästä.

2. Valitse **Synkronoi nyt**.

[![Täyden synkronoinnin suoritus](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>Lisätietoja

[Dataverse-taulut](hr-developer-entities.md)<br>
[Määritä Dataverse -virtuaalitaulukot](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resourcesin virtuaalitaulut – usein kysytyt kysymykset](hr-admin-virtual-entity-faq.md)<br>
[Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologiapäivitykset](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]