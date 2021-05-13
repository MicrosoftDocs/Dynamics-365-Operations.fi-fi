---
title: Toimittajien luokkapyynnöt
description: Tässä aiheessa kuvataan, kuinka toimittajat voivat pyytää tililleen hankintaluokkia. Siinä kuvataan myös hankinta-agenttien hyväksyntäprosessia.
author: kamaybac
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fb3555e6d923fe37479c3204f0b78f7cdf510118
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938459"
---
# <a name="category-requests-from-vendors"></a>Toimittajien luokkapyynnöt

[!include [banner](../includes/banner.md)]

Luokkapyyntöprosessin avulla toimittajat voivat pyytää, että tiliin liitetään uusia hankintaluokkia. Liittyvät hankintaprosessit voivat tämän jälkeen käyttää näitä hankintaluokkia. (Lisätietoja on kohdassa [Hankintaluettelojen yleiskatsaus](procurement-catalogs.md).)

**Toimittajatiedot**-työtilan toimittajat tekevät aloitteen luokkapyyntöihin. Sen jälkeen ne lähetetään toimistollesi tarkistettavaksi ja hyväksyttäväksi. Hyväksytyt luokat lisätään toimittajan tilin hankintaluokkien luetteloon.

## <a name="turn-on-the-feature-in-your-system"></a>Toiminnon ottaminen käyttöön järjestelmässä

Jos järjestelmässä ei ole vielä tässä aiheessa kuvattua ominaisuutta, siirry [ominaisuuksien hallintaan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota *Salli toimittajien hakea hankintaluokkia toimittajayhteistyön kautta* -ominaisuus käyttöön.

Kun toiminto on otettu käyttöön, voit edelleen lisätä hankintaluokkia toimittajatileille manuaalisesti. Lisätietoja on kohdassa [Toimittajien hyväksyminen tiettyihin hankintaluokkiin](tasks/approve-vendors-specific-procurement-categories.md).

## <a name="vendor-collaboration-requirements"></a>Toimittajayhteistyön vaatimukset

Ennen kuin toimittaja voi olla vuorovaikutuksessa luokkapyyntöjen kanssa, se on määritettävä toimittajayhteistyötä varten.

Toimittajalla on oltava vähintään yksi toimittajayhteiskäyttökäyttäjä. Vain toimittajakäyttäjät, joilla on yksi tai molemmat seuraavista käyttöoikeusrooleista, voivat luoda ja lähettää luokkapyyntöjä:

- Toimittajakontakti (ulkoinen)
- Toimittajan järjestelmänvalvoja (ulkoinen)

Lisätietoja on kohdassa [Toimittajayhteistyön määrittäminen ja hallinta](set-up-maintain-vendor-collaboration.md).

## <a name="set-up-the-vendor-category-request-workflow"></a>Toimittajan luokkapyynnön työnkulun määrittäminen

*Toimittajan luokkapyyntö* -työnkulku on määritettävä hankintatyönkuluissa. Toimittajat lähettävät uusia luokkapyyntöjä, joita voit tarkastella ja hyväksyä. Pyydetyt hankintaluokat lisätään toimittajatilille, kun luokkapyyntö on hyväksytty.

Seuraavassa esimerkissä kerrotaan, miten määritetään yksinkertainen *Toimittajan luokkapyyntö* -työnkulku, jossa on yksi hyväksyjä. Tarkista sisäiset prosessit ja määritä toimistosi tarvittavat työnkulkuasetukset.

1. Siirry kohtaan **Hankinta \> Asetukset \> Hankinnan työnkulut**.
1. Valitse toimintoruudussa **Uusi**.
1. Avaa työnkulkueditori valitsemalla valintaikkunassa **Toimittajan luokkapyyntö -työnkulku**.
1. Kirjaudu työnkulun editoriin.
1. Valitse toimintoruudussa **Ominaisuudet**.
1. Kirjoita ohjeteksti työnkulun **Ominaisuudet**-sivulla **Lähetysohjeet**-kenttään. Ohjeet näkyvät toimittajille, kun he lähettävät luokkapyynnön.
1. Sulje **Ominaisuudet**-sivu.
1. Vedä **Hyväksy uusi luokkapyyntö** -työnkulun elementti alustalle.
1. Vedä linkki **Aloita**-työnkulun elementistä **Hyväksy uusi luokkapyyntö** -työnkulun elementtiin.
1. Vedä linkki **Hyväksy uusi luokkapyyntö** -työnkulun elementistä **Lopeta**-työnkulun elementtiin.
1. Kaksoisnapsauta (tai kaksoisnapsauta) **Hyväksy uusi luokkapyyntö** -työnkulun elementtiä.
1. Valitse ja pidä valittuna (tai valitse hiiren kakkospainikkeella) **Vaihe 1** -työnkulun elementtiä ja valitse sitten **Ominaisuudet**.
1. Kirjoita aiheteksti työnkulun elementin **Ominaisuudet**-sivulla **Työnimikkeen aihe** -kenttään. Tämä teksti näkyy **Aihe**-kentän arvona **Minulle määritetyt työnimikkeet** -sivulla.
1. Kirjoita ohjeteksti **Työnimikkeen ohjeet** -kenttään. Ohjeet ovat hyväksyjien näkyvissä, kun he valitsevat **Työnkulku**-kohdan luokkapyynnön toimintoruudussa.
1. Valitse vasemmasta ruudusta **Määritys**.
1. Määritä **Määrityksen tyyppi** -välilehdessä **Määritä käyttäjiä tähän työnkulun elementtiin** -kohdan arvoksi *Käyttäjä*.
1. Valitse hyväksyjä **Käyttäjä**-välilehden **Käytettävissä olevat käyttäjät** -luettelosta. Valitse käyttäjä esimerkiksi hankintaosastosta.
1. Paina oikeaa nuolipainiketta (**\>**) siirtääksesi hyväksyjän **Valitut käyttäjät** -luetteloon.
1. Sulje **Ominaisuudet**-sivu.
1. Valitse **Tallenna ja sulje**.
1. Kirjoita **Versiohuomautukset** -kenttään työnkulkuun liittyvät huomautukset.
1. Valitse **OK** tallentaaksesi työnkulun.
1. Jos olet valmis aloittamaan työnkulun testaannin, valitse **Ota uusi versio käyttöön**. Valitse muussa tapauksessa **Älä ota uutta versiota käyttöön**.
1. Viimeistele työnkulun määritys valitsemalla **OK**.

> [!TIP]
> Jos toimistosi ei vaadi luokkapyyntöjen hyväksyntää, työnkulku on määritettävä automaattista hyväksyntää varten.

Lisätietoja työnkulkujen määrittämisestä on kohdassa [Työnkulkujärjestelmän yleiskatsaus](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

## <a name="create-and-submit-a-category-request"></a>Luokkapyynnön luominen ja lähettäminen

Tässä osassa kuvataan, kuinka toimittajat voivat luoda, muokata, tarkastella ja lähettää luokkapyyntöjä **Toimittajatiedot**-työtilan avulla.

### <a name="start-a-new-request"></a>Uuden pyynnön aloittaminen

Voit aloittaa uuden luokkapyynnön noudattamalla seuraavia ohjeita.

1. Valitse **Toimittajatiedot**-työtilassa **Luokkapyynnöt**-ruutu.
1. Valitse **Luokkapyynnöt**-sivun toimintoruudussa **Uusi luokkapyyntö**.
1. Etsi **Uusi luokkapyyntö** -valintaikkunasta luokka, jota haluat käyttää, siirtymällä puussa ja/tai käyttämällä suodatinta luettelon yläosassa. Valitse kunkin asianmukaisen luokan valintaruutu.

    Huomaa seuraavat seikat:

    - Toimittajatililläsi käytössä olevat luokat näytetään valittuna, eikä niitä voi poistaa.
    - Voit pyytää useita hankintaluokkia yhdessä luokkapyynnössä.

1. Luo luonnospyyntö valitsemalla **OK**.

    Uusi luonnospyyntö näkyy nyt **Luokkapyynnöt**-sivulla.

1. Avaa uusi luonnospyyntö ja tarkastele ja muokkaa sitä tarvittaessa.

    - Voit tarkastella pyyntöön tällä hetkellä sisällytettyjen luokkien luetteloa valitsemalla **Pyydetyt luokat** -pikavälilehden.
    - Voit tarkastella aktiivisia luokkia avaamalla **Aktiiviset luokat** -tietoruudun sivun oikealla puolella.
    - Voit lisätä pyyntöön luokan valitsemalla **Lisää** työkalupalkissa **Pyydetyt luokat** -pikavälilehdellä.
    - Jos haluat poistaa luokan pyynnöstä, valitse luokka **Pyydetyt luokat** -pikavälilehdessä ja valitse sitten työkaluriviltä **Poista**.
    - Voit liittää tiedoston pyyntöön valitsemalla **Liitteet** toimintoruudusta. Liitetyt tiedostot ovat hyväksyjien käytettävissä, kun he tarkistavat luokkapyynnön.
    - Voit poistaa liitetyn tiedoston pyynnöstä valitsemalla **Liitteet** toimintoruudusta. Valitse poistettava tiedosto ja valitse sitten toimintoruudusta **Poista**.

1. Jos olet valmis lähettämään pyynnön, valitse **Lähetä** toimintoruudusta. Muussa tapauksessa sulje sivu ja ohita muut tämän menettelyn vaiheet. Voit palata pyyntöön myöhemmin.
1. Lue näyttöön tulevat lähetysohjeet ja valitse **Lähetä**.
1. Kirjoita mahdolliset lisätiedot **Kommentti**-ruutuun. Viimeistele sitten pyyntö valitsemalla **Lähetä**.

### <a name="edit-a-draft-or-recalled-request"></a>Luonnoksen tai peruutetun kutsun muokkaaminen

Voit muokata luonnosta tai peruutettua luokkapyyntöä noudattamalla seuraavia vaiheita.

1. Valitse **Toimittajatiedot**-työtilassa **Luokkapyynnöt**-ruutu.
1. Valitse luonnos tai peruutettu pyyntö avataksesi sen.
1. Muokkaa pyyntöä tarvittaessa ja sitten sulje se tai lähetä se edellisessä menetelmässä kuvatulla tavalla.

### <a name="submit-a-draft-or-recalled-request"></a>Luonnoksen tai peruutetun kutsun lähettäminen

Voit lähettää luonnoksen tai peruutetun luokkapyynnön noudattamalla seuraavia vaiheita.

1. Valitse **Toimittajatiedot**-työtilassa **Luokkapyynnöt**-ruutu.
1. Valitse luonnos tai peruutettu pyyntö, jonka haluat lähettää.
1. Valitse toimintoruudussa **Lähetä**.
1. Lue näyttöön tulevat lähetysohjeet ja valitse **Lähetä**.
1. Kirjoita mahdolliset lisätiedot **Kommentti**-ruutuun. Viimeistele sitten pyyntö valitsemalla **Lähetä**.

    Luokkapyynnön tilaksi tulee jokin seuraavista arvoista:

    - _Odottaa tarkistusta_ – Pyyntö on työnkulussa.
    - _Odottaa hyväksyntää_ – Hyväksyntä on pakollinen.

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a>Lähetetyn pyynnön peruuttaminen, jota ei ole vielä hyväksytty

Noudattamalla seuraavia ohjeita voit peruuttaa luokkapyynnön, joka on lähetetty mutta jota ei ole vielä hyväksytty.

1. Valitse **Toimittajatiedot**-työtilassa **Luokkapyynnöt**-ruutu.
1. Valitse odottava pyyntö, jonka haluat peruuttaa.
1. Valitse toimintoruudussa **Peruuta**.
1. Kirjoita mahdolliset lisätiedot **Kirjoita kommentti**-ruutuun. Viimeistele sitten pyyntö valitsemalla **Lähetä**.

    Luokkapyynnön tila muuttuu ja uusi tila on _Peruutettu_. Pyyntö pysyy tässä tilassa, kunnes poistat sen tai lähetät sen uudelleen.

### <a name="delete-a-draft-or-recalled-request"></a>Luonnoksen tai peruutetun kutsun poistaminen

Voit poistaa luonnoksen tai peruutetun luokkapyynnön noudattamalla seuraavia vaiheita.

1. Valitse **Toimittajatiedot**-työtilassa **Luokkapyynnöt**-ruutu.
1. Valitse luonnos tai peruutettu pyyntö, jonka haluat poistaa.
1. Valitse toimintoruudussa **Poista**.
1. Vahvista poisto valitsemalla **Kyllä**.

### <a name="view-completed-requests"></a>Valmiien pyyntöjen tarkasteleminen

Voit tarkastella valmiita pyyntöjä avaamalla **Toimittajatiedot**-työtilan ja valitsemalla **Luokkapyynnöt**-ruudun. Valmiiden luokkapyyntöjen tila on jokin seuraavista:

- _Hyväksytty_ – Pyyntö hyväksyttiin. Kun haluat tarkastella juuri lisättyjä luokkia, siirry takaisin **Toimittajatiedot**-työtilaan, avaa vasemmassa ruudussa avattava **Lisätiedot**-luettelo ja valitse sitten **Luokat**.
- _Hylätty_ – Pyyntö on hylätty. Voit tarvittaessa luoda uuden luokkapyynnön.

## <a name="review-category-requests"></a>Luokkapyyntöjen tarkasteleminen

Tässä osassa on tietoja toimittajien lähettämien pyyntöjen hyväksymisestä, hylkäämisestä ja delegoinnista sekä valmiiden pyyntöjen tarkastelemisesta. Nämä työnkulkutoiminnot koskevat koko luokkapyyntöä.

### <a name="view-category-requests"></a>Luokkapyyntöjen tarkasteleminen

Voit tarkastella luokkapyyntöjä noudattamalla seuraavia ohjeita.

1. Valitse **Hankinta \> Toimittajat \> Toimittajayhteistyön pyynnöt \> Luokkapyynnöt**.

    Näkyviin tulee **Luokkapyyntö**-sivu. Oletussivunäkymä näyttää luokkapyynnöt, joiden tilana on *Odottaa toimintoa*.

1. Voit tarkastella kaikkia pyyntöjä valitsemalla *Kaikki* **Näytä pyynnöt** -kentässä.
1. Avaa pyyntö ja tarkastele ja muokkaa sitä tarvittaessa.

    - Voit tarkastella pyyntöön tällä hetkellä sisällytettyjen luokkien luetteloa valitsemalla **Pyydetyt luokat** -pikavälilehden.
    - Voit tarkastella aktiivisia luokkia avaamalla **Aktiiviset luokat** -tietoruudun sivun oikealla puolella.
    - Jos tiedostoja on lähetetty, liitettyjen tiedostojen määrä näkyy toimintoruudun **Liitteet** (paperiliitin) -painikkeen avulla. Voit tarkastella liitettyjä tiedostoja valitsemalla **Liitteet**-painikkeen. Valitse sitten haluamasi asiakirja ja valitse **Avaa**, jos haluat tarkastella sitä.
    - Voit liittää tiedoston pyyntöön valitsemalla **Liitteet** toimintoruudusta. Liitetyt tiedostot ovat hyväksyjien käytettävissä, kun he tarkistavat luokkapyynnön.
    - Voit poistaa liitetyn tiedoston pyynnöstä valitsemalla **Liitteet** toimintoruudusta. Valitse poistettava tiedosto ja valitse sitten toimintoruudusta **Poista**.
    - Voit tarkastella työnkulkuhistoriaa valitsemalla **Työnkulku** toimintoruudusta. Valitse työnkulun asetuksista **Lisää** ja sitten **Työnkulkuhistoria**. **Työnkulkuhistoria**-sivu tulee näkyviin.

### <a name="approve-a-pending-category-request"></a>Hyväksy odottava luokkapyyntö

Voit hyväksyä odottavan luokkapyynnön noudattamalla seuraavia vaiheita.

1. Valitse **Hankinta \> Toimittajat \> Toimittajayhteistyön pyynnöt \> Luokkapyynnöt**.
1. Valitse hyväksyntää odottava pyyntö.
1. Tarkastele luokkapyyntöä.
1. Valinnainen: Valitse syykoodi **Yleinen**-pikavälilehden **Syykoodi**-kentässä. Kirjoita sitten **Syyn koodi** -kenttään syykoodia koskeva kommentti.
1. Valitse toimintoruudussa **Työnkulku**.
1. Valitse työnkulun asetuksista **Hyväksy**.
1. Kirjoita mahdolliset lisätiedot **Kommentti**-kenttään. Viimeistele sitten pyyntö valitsemalla **Hyväksy**.

    Luokkapyynnön tilaksi muutetaan _Hyväksytty_ ja hankintaluokat lisätään toimittajatilille.

### <a name="reject-a-pending-category-request"></a>Hylkää odottava luokkapyyntö

Voit hylätä odottavan luokkapyynnön noudattamalla seuraavia vaiheita.

1. Valitse **Hankinta \> Toimittajat \> Toimittajayhteistyön pyynnöt \> Luokkapyynnöt**.
1. Valitse hylkäämistä odottava pyyntö.
1. Tarkastele luokkapyyntöä.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse syykoodi **Yleinen**-pikavälilehden **Syykoodi**-kentässä. Kirjoita sitten **Syyn koodi** -kenttään syykoodia koskeva kommentti.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Työnkulku**.
1. Valitse työnkulun asetuksista **Lisää** ja sitten **Hylkää**.
1. Kirjoita mahdolliset lisätiedot **Kommentti**-kenttään. Viimeistele sitten pyyntö valitsemalla **Hylkää**.

    Luokkapyynnön tila muuttuu ja uusi tila on _Hylätty_. Tässä vaiheessa toimittaja voi tarvittaessa luoda uuden luokkapyynnön.

### <a name="delegate-a-pending-category-request"></a>Delegoi odottava luokkapyyntö

Voit delegoida odottavan luokkapyynnön toiselle käyttäjälle noudattamalla seuraavia ohjeita.

1. Valitse **Hankinta \> Toimittajat \> Toimittajayhteistyön pyynnöt \> Luokkapyynnöt**.
1. Valitse odottava pyyntö, jonka haluat hyväksyä.
1. Valitse toimintoruudussa **Työnkulku**.
1. Valitse työnkulun asetuksista **Lisää** ja sitten **Delegoi**.
1. Valitse **Käyttäjä**-kentästä käyttäjä, jolle haluat määrittää tarkistettavan luokkapyynnön.
1. Kirjoita mahdolliset lisätiedot **Kommentti**-kenttään.
1. Viimeistele delegointi valitsemalla **Delegoi**. Valittu käyttäjä voi nyt tarkistaa luokkapyynnön.

### <a name="view-procurement-categories-for-a-vendor"></a>Toimittajan hankintaluokkien tarkasteleminen

Voit tarkastella toimittajan hankintaluokkia, kun luokkapyyntö on hyväksytty, noudattamalla seuraavia vaiheita.

1. Valitse **Hankinta \> Toimittajat \> Kaikki toimittajat**.
1. Valitse **Kaikki toimittajat** -sivulla toimittaja, jonka hankintaluokkia haluat tarkastella.
1. Avaa toimintoruudussa **Yleinen**-välilehti ja valitse **Asetukset**-ryhmässä **Luokat**.

    **Luokat**-sivu avautuu. **Hankinta**-pikavälilehdessä näkyvät luokkapyynnön kautta lisätyt hankintaluokat.

1. **Hankinta**-pikavälilehdessä voit tarvittaessa tehdä muutoksia. Voit esimerkiksi määrittää **Toimittajaluokan tilaksi** _Ensisijainen_.
