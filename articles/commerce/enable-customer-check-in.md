---
title: Ota käyttöön asiakkaan sisäänkuittausten ilmoitukset myyntipisteissä
description: Tässä artikkelissa kuvataan, kuinka asiakkaan sisäänkuittausilmoitukset otetaan käyttöön Microsoft Dynamics 365 Commerce -myyntipisteessä (POS).
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ae53657c95128eae793f670bd9dbc31d9fac0fe4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885142"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Ota käyttöön asiakkaan sisäänkuittausten ilmoitukset myyntipisteissä

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka asiakkaan sisäänkuittausilmoitukset otetaan käyttöön Microsoft Dynamics 365 Commerce -myyntipisteessä (POS).

Organisaatiot voivat lähettää sähköpostien "Tilaus valmis noudettavaksi" -sähköpostiviestissä linkin tai painikkeen, jonka avulla asiakkaat ilmoittavat myymälälle, että he ovat paikan päällä ja odottavat paketin tuontia. Tämän jälkeen asiakkaat saavat sisäänkuittausvahvistuksen, ja myymälä saa ilmoituksen tehtävänä myyntipistesovelluksessa. Tämä tehtävä toimii kehotteena myyntiedustajalle toimittaa tilaus asiakkaan ajoneuvoon. Asiakkaan ei siis tarvitse mennä sisään myymälään.

Asiakkaan sisäänkuittaustyönkulun voi myös konfiguroida keräämään asiakkailta lisätietoja, kuten pysäköintipaikan numeron, ajoneuvon mallin ja värin sekä toimitusohjeet. Vähittäismyymälän myyjä voi helpottaa tilausten täyttämistä näiden tietojen avulla.

## <a name="enable-customer-check-in"></a>Asiakkaan sisäänkuittauksen ottaminen käyttöön

Kun asiakkaan sisään sisäänkuittaustoiminto on käytössä, Commerce luo tilausvahvistuksen tunnuksen (tunnetaan myös kanavan viitetunnuksena). Se luo myös tilausvahvistustunnukset tilauksille, jotka on luotu myyntipisteen (POS) tai puhelinkeskuskanavien kautta. 

Ota asiakkaan sisäänkuittausominaisuus käyttöön Commercen pääkonttorisovelluksessa seuraavien ohjeiden mukaan.

1. Valitse **Työtilat \> Ominaisuuden hallinta**.
2. Etsi **Yhdenmukaisen kanavan viitetunnuksen muodon muodostaminen eri kanavissa** -ominaisuutta. 
3. Valitse ominaisuus ja valitse sitten ominaisuusruudusta **Ota käyttöön nyt**. 

## <a name="create-a-check-in-confirmation-page"></a>Sisäänkuittaussivun luominen

Sähköisen kaupankäynnin sivustossa luo uusi sivu, jota käytetään sisäänkuittauksessa. Lisäkonfiguraation avulla sivu voi myös sisältää lomakkeen, joka kerää asiakkailta lisätietoja tilausten täyttämistä varten. Lisätietoja sivun ja moduulin määrittämisestä on kohdassa [Asiakkaan sisäänkuittausmoduuli](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>Tapahtumasähköpostimallin konfiguroiminen

Lisää tapahtumasähköpostimalliin **Olen paikalla** -linkki tai -painike, jonka asiakkaat saavat, kun heidän tilauksensa on valmis noudettavaksi. Tämän linkin tai painikkeen avulla asiakkaat voivat ilmoittaa myymälälle, että he ovat saapuneet noutamaan tilauksen. 

Lisää linkki tai painike malliin, joka on yhdistetty **Pakkaus valmis** -ilmoituksen tyyppiin ja toimitustapaan, jota käytät tien vierestä noudettavan tilauksen täyttämisessä. Luo mallissa HTML-linkki tai -painike, joka osoittaa luomasi sisäänvahvistussivun URL-osoitteeseen ja joka sisältää parametrien nimet ja arvot seuraavan esimerkin mukaisesti.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

Lisätietoja sähköpostimallien määrittämisestä on kohdassa [Tapahtumasähköpostien mukauttaminen toimitustilan mukaan](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>Sisäänkuittaustehtävä luodaan myyntipisteessä

Kun asiakas on ilmoittanut myymälälle, että he ovat paikalla noutoa varten, näyttöön tulee vahvistussanoma ja valinnainen QR-koodi, joka sisältää asiakkaan tilausvahvistustunnuksen. Samalla tehtävä luodaan myyntipisteen tehtäväluetteloon myymälälle, jossa asiakas kerää tilauksen. Tämä tehtävä sisältää kaikki tilauksen täyttämisen edellyttämät asiakas- ja tilaustiedot. Tehtävän ohjeet-kentässä näkyvät kaikki asiakkaalta lisätietolomakkeella kerätyt tiedot.

## <a name="end-to-end-testing"></a>Päästä päähän -testaus

Asiakkaan kirjautuminen edellyttää, että tietyt parametrit ja arvot välitetään sisäänkirjautumissivulle ja sitten asiakkaan sisäänkirjautumisohjelmointirajapintaan. Helpoin tapa on testata ympäristössä, jossa voidaan luoda ja pakata testitilaus. Näin voidaan luoda sähköposti "tilaus, joka on valmis noutoa varten" ja jolla on URL-osoite, joka sisältää vaaditut parametrien nimet ja arvot.

Voit testata asiakkaan sisään sisäänkirjautumisominaisuuden noudattamalla seuraavia ohjeita.

1. Luo asiakkaan sisäänkirjautumissivu ja lisää ja konfiguroi sitten asiakkaan sisäänkirjautumismoduuli. Lisätietoja on [Sisäänkirjautuminen noutomoduuliin](check-in-pickup-module.md) -kohdassa. 
1. Kirjaa sivu sisään, mutta älä julkaise sitä.
1. Lisää seuraava linkki sähköpostimalliin, jonka pakkaus on valmis -ilmoitustyyppi kutsuu noutotavalle. Lue lisätietoja kohdasta [Tapahtuman tapahtumien sähköpostimallien luominen](email-templates-transactions.md).

    - **Esituotantoympäristöihin (UAT):** Lisää koodin katkelma aiemmin tässä artikkelissa kuvatusta [Tapahtumasähköpostimallien määrittäminen](#configure-the-transactional-email-template) -osasta.
    - **Tuotantoympäristöissä:** Lisää seuraava huomautuskoodi, jotta asiakkaalla ei ole vaikutusta aiemmin luotuihin asiakkaisiin.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Luo tilaus, jossa on määritetty noutotapa.
1. Kun vastaanotat sähköpostiviestin, jonka on käynnistänyt pakkaus valmis -ilmoitustyyppi, testaa sisäänkirjautuminen avaamalla sisäänkirjautumissivu, jolla on aiemmin lisäämäsi URL-osoite. Koska URL-osoite sisältää `&preview=inprogress`-merkinnän, järjestelmä pyytää todentamaan, ennen kuin voit tarkastella sivua.
1. Syötä kaikki lisätiedot, joita tarvitaan moduulin määrittämiseen.
1. Tarkista, että vahvistusnäkymä on oikein.
1. Avaa sen myymälän kassapääte, josta tilaus noudetaan.
1. Valitse **Noudettavat tilaukset** -ruutu ja tarkista, että tilaus tulee näyttöön.
1. Varmista, että sisääntarkistusmoduuliin määritetyt lisätiedot näkyvät tietoruudussa.

Kun olet varmistanut, että asiakkaan sisään sisäänkirjautumistoiminto toimii päästä päähän, noudata seuraavia ohjeita.

1. Julkaise sisäänkirjautumissivu.
1. Jos testaat tuotantoympäristössä, poista sähköpostimallin "Tilauksen nouto valmis" -URL-osoite, niin näkyviin tulee **Olen tässä** -linkki tai -painike. Lataa sitten malli uudelleen.

## <a name="additional-resources"></a>Lisäresurssit

[Noutomoduulin sisäänkuittaus](check-in-pickup-module.md)

[Tapahtumasähköpostien mukauttaminen toimitustilan mukaan](customize-email-delivery-mode.md)

[Tapahtuman tapahtumien sähköpostimallien luominen](email-templates-transactions.md)
