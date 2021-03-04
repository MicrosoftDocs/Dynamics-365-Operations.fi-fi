---
title: Yksinkertaistettu työntekijöiden lisääminen ja navigointi
description: Työntekijöiden tietomerkinnät Dynamics 365 Talentissa on laajennettu sallimaan kaikkien työntekijöiden (entiset, aktiiviset ja tulevat) merkinnät. Yksinkertaistettu/konsolidoitu siirtymismalli on päivitetty etsimään nopeasti aiheeseen liittyviä tietoja sekä näyttämään ja tekemään tarvittavat päivitykset.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: b73b420c2eb75077814fbfeb6cd17404c7efc11e
ms.sourcegitcommit: 436731d8b3889bebfe6f17922b0a31b1994f6796
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/26/2020
ms.locfileid: "4461104"
---
# <a name="streamlined-employee-entry-and-navigation"></a>Yksinkertaistettu työntekijöiden lisääminen ja navigointi

Dynamics 365 Talentissa työntekijä- ja työsuhdemerkinnät voidaan tehdä tehokkaasti. Voit päivittää nopeasti entisten, aktiivisten ja tulevien työntekijöiden ja alihankkijoiden työhistoriatiedot.

Voit myös ottaa käyttöön yksinkertaistetun siirtymiskokemuksen, jolla liittyvät tiedot löydetään ja tarvittavat muutokset voidaan tehdä nopeasti. Tämä toiminto on nyt käytettävissä kaikissa ympäristöissä. Voit ottaa tämän ominaisuuden käyttöön siirtymällä kohtaan **Järjestelmänhallinta > Ominaisuuksienhallinta > Uusi > Virtaviivaistettu työntekijämerkintä > Ota käyttöön**. Nämä muutokset otetaan nyt käyttöön kaikille käyttäjille. Voit poistaa tämän asetuksen käytöstä milloin tahansa.

## <a name="view-options"></a>Näytä asetukset

Voit valita työntekijälomakkeen **Näytä asetukset** -asetuksen avulla minkä tahansa samassa luettelossa olevien työntekijöiden ja alihankkijoiden yhdistelmän. Voit tarkastella näiden asetusten avulla eri yritysten työntekijöitä tai sen yrityksen työntekijöitä, johon olet kirjautuneena. Voit tarkastella myös aktiivisia, odottavia ja lopettaneita työntekijöitä sekä rajoittaa tuloksia työntekijän tyypin (työntekijä tai alihankkija) mukaan. Jos lisäsuojaus on otettu käyttöön, näet vain niiden yritysten työntekijät ja alihankkijat, joiden käyttöoikeus sinulla on.

Luettelonäkymän sarakkeet muuttuvat valintojen mukaan. Esimerkiksi lopettaneita työntekijöitä tarkasteltaessa työsuhteen loppumispäivä ja syykoodit näkyvät luettelossa ylimääräisinä sarakkeina. 

[![Näytä asetukset](./media/Worker-view-option.png)](./media/worker-view-option.png)

## <a name="navigation-and-banner"></a>Siirtyminen ja ilmoituspalkki

Ilmoituspalkissa näkyy avaintietoja kustakin työntekijästä. Aktiivisten työntekijöiden ilmoituspalkissa on seuraavat kentät:

- **Titteli**
- **Osasto**
- **Toimityyppi**
- **Työntekijätyyppi**
- **Esimies**
- **Oikeushenkilö**

Lopettaneiden työntekijöiden ilmoituspalkissa on seuraavat kentät:

- **Lopettamispäivä**
- **Syy**

Odottavien työntekijöiden ilmoituspalkissa on seuraavat kentät:

- **Titteli**
- **Osasto**
- **Toimityyppi**
- **Esimies**
- **Aloituspäivämäärä**
- **Oikeushenkilö**

Työntekijäsivun toimintoruutu on järjestetty uudelleen ja siinä on vähemmän asetuksia. Tiedot on nyt järjestetty seuraaviin luokkiin: 

- Työ
- Henkilö
- Loma
- Kompensaatio
- Edut
- Yhteensopivuus

Lisäksi työntekijän pääsivun uuden **Linkit**-välilehden avulla käyttäjät voivat käyttää keskitetysti työntekijän kaikkia liittyviä tietoja.

Näiden muutosten vuoksi tiedot näkyvät nyt eri paikassa kuin aiemmin. Esimerkiksi aiemmin työntekijälomakkeessa näkyneet palkanlaskentatiedot näkyvät nyt toimintoruudussa kohdassa **Kompensaatio > Palkanlaskenta**, ja **Henkilökohtaiset tiedot** -välilehdessä on nyt **Lisätietoja**-painike, jolla voi piilottaa harvoin käytetyt kentät.

[![Banneri](./media/Banner.png)](./media/Banner.png)

## <a name="work-history"></a>Työhistoria

**Työhistoria**-välilehdessä näkyy nyt työhistoria kaikissa yrityksissä, ja nämä tiedot ovat käytettävissä lopettaneiden, aktiivisten ja odottavien työntekijöiden ja alihankkijoiden osalta. Voit nyt tarkastella kerralla kaikkien niiden yritysten koko työhistoriaa, joiden käyttöoikeus sinulla on. Voit lisäksi muokata kunkin työhistoriamerkinnän tietoja tietokontekstia muuttamatta. Voit päivittää kaikki tiedot suoraan sivulla. 

[![Työhistoria](./media/Worker-work-history.png)](./media/Worker-work-history.png)

## <a name="position-history"></a>Toimen historiatiedot

Työntekijän pääsivun **Toimet**-välilehdessä on täydellinen näkymä kaikissa organisaatiossa olevista toimista mukaan lukien entiset, nykyiset ja tulevat tehtävät. Voit edelleen siirtyä suodaan työntekijän toimihistoriaan myös toimintoruudussa.

[![Toimet](./media/Worker-position-history.png)](./media/Worker-position-history.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]