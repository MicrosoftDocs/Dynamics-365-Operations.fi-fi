---
title: Asiakkaan sisäänkuittausilmoitusten ottaminen käyttöön myyntipisteessä
description: Tässä aiheessa kuvataan, kuinka asiakkaan sisäänkuittausilmoitukset otetaan käyttöön Microsoft Dynamics 365 Commerce -myyntipisteessä (POS).
author: bicyclingfool
ms.date: 04/23/2021
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
ms.openlocfilehash: cf9331e1da54520787686a3f190e2ef6d150c0c10bd521919407f5e6c74551d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774580"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Asiakkaan sisäänkuittausilmoitusten ottaminen käyttöön myyntipisteessä

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan, kuinka asiakkaan sisäänkuittausilmoitukset otetaan käyttöön Microsoft Dynamics 365 Commerce -myyntipisteessä (POS).

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

Lisää linkki tai painike malliin, joka on yhdistetty **Pakkaus valmis** -ilmoituksen tyyppiin ja toimitustapaan, jota käytät tien vierestä noudettavan tilauksen täyttämisessä. Luo mallissa HTML-linkki tai -painike, joka osoittaa luomasi sisäänkuittaussivun URL-osoitteeseen. Esimerkki:

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
Lisätietoja sähköpostimallien määrittämisestä on kohdassa [Tapahtumasähköpostien mukauttaminen toimitustilan mukaan](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>Sisäänkuittaustehtävä luodaan myyntipisteessä

Kun asiakas ilmoittaa myymälälle, että hän on paikalla noutoa varten, hän saa kuittausvahvistusilmoituksen ja tehtävä luodaan myyntipisteen tehtäväluetteloon myymälälle, josta asiakas noutaa tilauksen. Tehtävä sisältää kaikki tilauksen täyttämisen edellyttämät asiakas- ja tilaustiedot. Tehtävän ohjeet-kentässä näkyvät kaikki asiakkaalta lisätietolomakkeella kerätyt tiedot. 

## <a name="additional-resources"></a>Lisäresurssit

[Noutomoduulin sisäänkuittaus](check-in-pickup-module.md)
