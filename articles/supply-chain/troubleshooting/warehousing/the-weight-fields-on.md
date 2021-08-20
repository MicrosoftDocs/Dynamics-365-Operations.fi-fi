---
title: Kuormarivien painokentät eivät vastaa kuormituksen painokenttiä
description: Kuormarivien painokentät eivät vastaa kuormituksen painokenttiä
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f71ac7b2777cb77fccdf1a4c72a47c9b406bbd68b2d20c41ddc96028d2ffc348
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756700"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>Kuormarivien painokentät eivät vastaa kuormituksen painokenttiä

Virhekoodit: WHSLoadWeightOnLinesDoNotMatchLoadWarning

## <a name="symptoms"></a>Oireet

Järjestelmä näyttää seuraavan virhesanoman:

> Kuormarivien painokentät eivät vastaa kuormituksen %1 painokenttiä. Suorita Varaston kuorman painon yhdenmukaisuustarkistus, jos haluat laskea painokentät uudelleen.

## <a name="cause"></a>Syy

**Nettopaino**- ja **Taarapaino**-kenttien arvona on *0* (nolla) kuormitusrivillä. Tuotteen painomittauksissa painokentiksi ei kuitenkaan ole määritetty *0*. Jos kuormitusrivillä ei ole määritetty painokenttiä, kuormitusrivin määrän korjaukset voivat aiheuttaa kuormituksen virheellisen painon laskennan. Tämä ongelma voi ilmetä, jos tuotteen painot on muutettu kuormitusrivin luomisen jälkeen.

## <a name="resolution"></a>Ratkaisu

Kun kuormitusrivi luodaan, tuotteen painokentät syötetään siihen oletusarvoisesti. Jos paino on nolla, voit laskea sen uudelleen käyttämällä *Varaston kuorman painon yhdenmukaisuustarkistus* -toimintoa.

1. Valitse **Järjestelmän hallinta \> Kausittaiset tehtävät \> Tietokanta \> Yhdenmukaisuustarkistus**.
1. **Yhdenmukaisuustarkistus**-valintaikkunassa aseta **Moduuli**-kentän arvoksi *Varastonhallinta*.
1. Valitse **Tarkista/korjaa**-kentässä *Korjaa virhe*.
1. Valitse valintaruutuluettelosta **Varaston kuorman painon yhdenmukaisuustarkistus** -valintaruutu ja varmista, että vain tämän valintaruudun rivi on korostettuna.
1. Valitse valintaruutuluettelon yläosasta kolmen pisteen painike (**...**) ja valitse valikosta **Valintaikkuna**.
1. **Varaston kuorman painon yhdenmukaisuustarkistus** -valintaikkunassa määritä seuraavat kentät määrittämään ehdot, joiden yhdenmukaisuustarkistuksessa tarkistetaan:

    - **Kuorman tunnus:** Määritä kuorman tunnus. Jätä tämä kenttä tyhjäksi, jotta voit tarkistaa kaikki kuormatunnukset.
    - **Nimiketunnus:** Määritä nimiketunnus. Jätä tämä kenttä tyhjäksi, jotta voit tarkistaa kaikki nimikkeet.
    - **Laske kuorman paino aina uudelleen:** Määritä tämän asetuksen arvoksi *Kyllä*.
    - **Salli painojen korvaaminen kuormariveillä:** Määritä tämän asetuksen arvoksi *Kyllä*.

1. Valitse **OK**, jos haluat sulkea **Varaston kuorman painon yhdenmukaisuustarkistus** -valintaikkunan.
1. Valitse kolmen pisteen painike ja valitse sitten valikosta **Suorita**.

Paino lasketaan uudelleen määrittämiesi ehtojen mukaan. Valitsemalla **Sanoman tiedot** -linkin voit tarkastella yhdenmukaisuustarkistustuloksen tulosta.
