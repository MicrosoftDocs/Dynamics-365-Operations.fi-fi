---
title: Staattisten tiedostojen lataaminen ja käyttäminen
description: Tässä aiheessa kuvataan, miten voit ladata staattisen tiedoston Microsoft Dynamics 365 Commerce -sivuston muodostimeen ja miten voit luoda mukautetun URL-osoitteen ja tiedostonimen, joita voidaan käyttää tiedoston pyytämisessä.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1d709d99737ad05af1fb19d9f3ef7b87a8db80d3
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031817"
---
# <a name="upload-and-serve-static-files"></a>Staattisten tiedostojen lataaminen ja käyttäminen

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan, miten voit ladata staattisen tiedoston Microsoft Dynamics 365 Commerce -sivuston muodostimeen ja miten voit luoda mukautetun URL-osoitteen ja tiedostonimen, joita voidaan käyttää tiedoston pyytämisessä.

Jotkin kolmannen osapuolen liittimet edellyttävät, että tiedostoa isännöidään ja tarjoillaan verkkokauppasivustosta. Nämä liittimet odottavat, että tiedosto palautetaan pyynnöillä tiettyyn takaisinkutsun URL-polkuun ja tiedostonimeen. Tämän vuoksi tässä ohjeaiheessa kerrotaan, kuinka voit ladata ja käyttää staattista tiedostoa, jonka URL-osoite ja tiedostonimi ovat käyttäjän määritettävissä Dynamics 365 Commerce -verkkokauppasivustossa.

## <a name="create-a-site-url-that-returns-a-static-file"></a>Staattisen tiedoston palauttavan sivuston URL-osoitteen luominen

Jos haluat luoda sivuston URL-osoitteen, joka palauttaa staattisen tiedoston Commerce-sivuston muodostimessa, toimi seuraavasti.

1. Siirry sivustosi mediakirjastoon ja lataa palvelimeen tiedosto, jonka haluat saataville URL-osoitteesta, jonka määrität. Jos olet jo ladannut tiedoston, voit ohittaa tämän vaiheen.
1. Siirry sivuston **URL-osoitteet** -kohtaan.
1. Valitse **Uusi \> Uusi URL-soite**.
1. Valitse **Uusi URL-osoite** -valintaikkunassa **Mediakirjaston resurssi**.
1. Kirjoita URL-polku **URL-polku** -kenttään. Lisää tiedoston nimi polkuun.
1. Valitse **Seuraava**. Mediakirjasto avataan ja siinä näkyvät kaikki lataamasi **tiedostotyypin** mediaresurssit.
1. Valitse tiedosto, joka on tarkoitettu vaiheessa 5 määritettyyn URL-osoitteeseen.
1. Valitse **Tallenna**.

Tässä vaiheessa luomasi URL-osoite on luonnostilassa. Tiedostoa, johon URL-osoite osoittaa, ei palauteta, ennen kuin julkaiset URL-osoitteen. Ennen kuin julkaiset URL-osoitteen, voit vahvistaa, että se palauttaa oikeat tiedot.

## <a name="validate-and-publish-a-url"></a>URL-osoitteen tarkistaminen ja julkaisu

Voit vahvistaa URL-osoitteen ennen sen julkaisua tekemällä seuraavat toimet.

1. Siirry sivuston kohtaan **URL-osoitteet** ja valitse esikatseltava URL-osoite.
2. Valitse oikealla olevan Ominaisuudet-ruudun **Muokkaa**-painikkeen alapuolelta oikea URL-linkki. Uusi selainikkuna avautuu ja näyttöön tulee virhe 404.
3. Liitä kyselymerkkijono **?preview=inprogress** URL-osoitteeseen (esimerkiksi `https://yoursite.com/callback.html?preview=inprogress`) ja lataa sivu uudelleen. Mediakirjastoon lataamasi tiedosto palautetaan vastauksessa.

Kun olet vahvistanut URL-osoitteen, voit julkaista sen.

1. Siirry sivuston kohtaan **URL-osoitteet** ja valitse URL-osoite.
2. Valitse komentopalkissa **Julkaise**.

## <a name="update-the-file-that-a-url-points-to"></a>Päivitä tiedosto, johon URL-osoite osoittaa

Kun URL-osoite on julkaistu, voit päivittää sen niin, että se osoittaa toiseen tiedostoon. Vaihtoehtoisesti voit päivittää URL-osoitteen niin, että se osoittaa eri tyyppiseen resurssii, kuten seuraavassa osassa on kuvattu. Voit esimerkiksi osoittaa URL-osoitteen sisäiselle sivulle tai uudelleenohjaukseen.

Jos haluat päivittää tiedoston, johon URL-osoite viittaa, toimi seuraavasti.

1. Siirry sivuston kohtaan **URL-osoitteet** ja valitse päivitettävä URL-osoite.
1. Valitse oikeanpuoleisessa ominaisuusruudussa **Muokkaa**.
1. Valitse **URL-osoitteen määritys** -kohdasta **Vaihe 2** -ruutu ja valitse sitten uusi tiedosto mediakirjastosta.
1. Valitse **Käytä**.

## <a name="update-the-asset-type-that-a-url-points-to"></a>Päivitä resurssityyppi, johon URL-osoite osoittaa

Voit myös päivittää URL-osoitteen niin, että se osoittaa erityyppiseen resurssiin, kuten sisäiselle sivulle tai uudelleenohjaukseen.

Jos haluat päivittää resurssityypin, johon URL-osoite viittaa, toimi seuraavasti.

1. Siirry sivuston kohtaan **URL-osoitteet** ja valitse päivitettävä URL-osoite.
1. Valitse oikeanpuoleisessa ominaisuusruudussa **Muokkaa**.
1. Valitse **URL-osoitteen määritys** -kohdan **Vaihe 1** -kohdassa toinen resurssityyppi.
1. Valitse **Vaihe 2** -ruutu ja valitse sitten uusi resurssi.
1. Valitse **Käytä**.

## <a name="change-the-url-path"></a>URL-polun muuttaminen

Kun URL-osoite on luotu, sen polkua ei voi muuttaa. Jos sinun on muutettava URL-polkua, joka tarjoaa tiedoston tai jonkin muun resurssin, luo uusi URL-osoite, yhdistä se olemassa olevaan tiedostoon tai muuhun resurssiin ja sitten peruuta vanhan URL-osoitteen julkaisu ja poista osoite.

Voit muuttaa URL-polkua seuraavasti.

1. Jos haluat luoda uuden URL-osoitteen ja yhdistää sen aiemmin luotuun tiedostoon tai muuhun resurssiin, noudata aiemmin tässä ohjeaiheessa olevan osan [Staattisen tiedoston palauttavan sivuston URL-osoitteen luominen](#create-a-site-url-that-returns-a-static-file) ohjeita.
1. Valitse uusi URL-osoite ja valitse komentopalkissa **Julkaise**. Uusi URL-osoite julkaistaan.
1. Voit peruuttaa vanhan URL-osoitteen julkaisemisen valitsemalla osoitteen ja valitsemalla sitten komentopalkissa **Peruuta julkaisu**. Voit nyt poistaa vanhan URL-osoitteen halutessasi.

## <a name="additional-resources"></a>Lisäresurssit

[Digitaalisten resurssien hallinnan yleiskatsaus](dam-overview.md)

[Kuvien lataaminen palveluun](dam-upload-images.md)

[Videoiden lataaminen](dam-upload-video.md)

[Muiden tiedostojen kuin kuvien ja videoiden lataaminen palveluun](dam-upload-files.md)

[Kuvien rajaaminen](dam-crop-images.md)

[Kuvien tarkennuspisteiden mukauttaminen](dam-custom-focal-point.md)
