---
title: Yksinkertaistettu työntekijöiden lisääminen ja navigointi
description: Työntekijöiden tietomerkinnät Dynamics 365 for Talentissa on laajennettu sallimaan kaikkien työntekijöiden (entiset, aktiiviset ja tulevat) merkinnät. Yksinkertaistettu/konsolidoitu siirtymismalli on päivitetty etsimään nopeasti aiheeseen liittyviä tietoja sekä näyttämään ja tekemään tarvittavat päivitykset.
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
ms.openlocfilehash: be0253ffc4396f36050ef02c51a20d378e44473d
ms.sourcegitcommit: 4176c333ce3f88c5c68e95bd47e5791d32365dd2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/22/2019
ms.locfileid: "1918197"
---
# <a name="streamlined-employee-entry-and-navigation"></a>Yksinkertaistettu työntekijöiden lisääminen ja navigointi

[!include [banner](includes/banner.md)]

Dynamics 365 for Talentissa työntekijä- ja työsuhdemerkinnät voidaan tehdä tehokkaasti. Voit päivittää nopeasti entisten, aktiivisten ja tulevien työntekijöiden ja alihankkijoiden työhistoriatiedot.

Voit myös ottaa käyttöön yksinkertaistetun siirtymiskokemuksen, jolla liittyvät tiedot löydetään ja tarvittavat muutokset voidaan tehdä nopeasti. Tämä toiminto on nyt käytettävissä eristysympäristöissä. Ota tämä toiminto käyttöön valitsemalla **Järjestelmän hallinta > Linkit > Asetukset > Järjestelmän parametrit > Esiversio-ominaisuudet**. Valitse **Laajennettu työntekijälomake ja siirtyminen**. Nämä muutokset otetaan nyt käyttöön kaikille käyttäjille. Voit poistaa tämän asetuksen käytöstä milloin tahansa.

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
- Poistu
- Kompensaatio
- Edut
- Yhteensopivuus

Lisäksi työntekijän pääsivulla on uusi **Linkit**-välilehti, jossa käyttäjät voivat keskitetysti käyttää kaikkia työntekijään liittyviä tietoja.

Näiden muutosten vuoksi tiedot näkyvät nyt eri paikassa kuin aiemmin. Esimerkiksi aiemmin työntekijälomakkeessa näkyneet palkanlaskentatiedot näkyvät nyt toimintoruudussa kohdassa**Kompensaatio > Palkanlaskenta**, ja **Henkilökohtaiset tiedot** -välilehdessä on nyt **Lisätietoja**-painike, jolla voi piilottaa harvoin käytetyt kentät.

[![Banneri](./media/Banner.png)](./media/Banner.png)

## <a name="work-history"></a>Työhistoria

**Työhistoria**-välilehdessä näkyy nyt työhistoria kaikissa yrityksissä, ja nämä tiedot ovat käytettävissä lopettaneiden, aktiivisten ja odottavien työntekijöiden ja alihankkijoiden osalta. Voit nyt tarkastella kerralla kaikkien niiden yritysten koko työhistoriaa, joiden käyttöoikeus sinulla on. Voit lisäksi muokata kunkin työhistoriamerkinnän tietoja tietokontekstia muuttamatta. Voit päivittää kaikki tiedot suoraan sivulla. 

[![Työhistoria](./media/Worker-work-history.png)](./media/Worker-work-history.png)

## <a name="position-history"></a>Toimen historiatiedot

Työntekijän pääsivun **Toimet**-välilehdessä on täydellinen näkymä kaikissa organisaatiossa olevista toimista mukaan lukien entiset, nykyiset ja tulevat tehtävät. Voit edelleen siirtyä suodaan työntekijän toimihistoriaan myös toimintoruudussa.

[![Toimet](./media/Worker-position-history.png)](./media/Worker-position-history.png)

