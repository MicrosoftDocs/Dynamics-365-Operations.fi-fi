---
title: Ostohyvitysten käsitteleminen, tarkistaminen ja kirjaaminen
description: Tässä aiheessa kuvataan, miten ostohyvitysten hallinnan tarjoukset käsitellään, miten niiden alennukset lasketaan, luodut tapahtumat tarkistetaan, tapahtumat kirjataan ja kirjaukset tarkistetaan.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 53a24866786f209a1d0f6932bb4f782bf936bd21
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819253"
---
# <a name="process-review-and-post-rebates"></a>Ostohyvitysten käsitteleminen, tarkistaminen ja kirjaaminen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä aiheessa kuvataan, miten ostohyvitysten hallinnan tarjoukset käsitellään, miten niiden alennukset lasketaan, luodut tapahtumat tarkistetaan, tapahtumat kirjataan ja kirjaukset tarkistetaan.

## <a name="change-the-status-of-a-deal"></a>Sopimuksen tilan muuttaminen

Voit seurata sopimusta määrittämällä kullekin sopimukselle tilan. Tila on tarkoitettu vain tiedoksi.

1. Valitse sopimus (esimerkiksi [**Kaikki ostohyvityksen hallinnan sopimukset** -sivulla](rebate-management-deals.md)).
1. Valitse toimintoruudun **Ostohyvitysten hallinnan sopimukset**-välilehden **Ylläpidä** -ryhmässä **Muuta tilaa**.
1. Määritä **Muuta tila** -valintaikkunassa **Ostohyvityksen tila** -kentässä uusi tila.
1. Valitse **OK**.

## <a name="calculate-fifo-purchase-prices"></a>FIFO-ostohintojen laskeminen

**Laske FIFO-ostohinta** kausittainen tehtävä on suoritettava, jotta voit laskea niiden [sopimusten](rebate-management-deals.md) ostohyvitykset, joissa **Hintaperuste**-kentän arvoksi on määritetty *FIFO*. Järjestelmä laskee myydyn varaston arvon FIFO (first in, first out) -säännön avulla. Tämän jälkeen käytetään tätä arvoa toimittajien ostohyvitysten laskemiseen.

Siirry kohtaan **Ostohyvitysten hallinta \> Kausittaiset tehtävät \> Laske FIFO-ostohinta**. Suorita laskenta valitsemalla näyttöön tulevassa valintaikkunassa **OK**.

## <a name="process-rebate-management-deals"></a>Käsittele ostohyvitysten hallintasopimukset

Kun sopimukset käsitellään, järjestelmä laskee kaikki asianmukaiset ostohyvitykset ja rojaltit. Vain valitut tarjoukset, joiden laskentakaudet ovat valmiita laskettavaksi ja joiden tila on *Aktiivinen*, käsitellään. Kun käsittely on valmis, järjestelmä luo joukon tapahtumia, jotka voit tarkistaa ja kirjata.

> [!NOTE]
> Ostohyvitykset käsitellään aina tasolla, jonka kunkin sopimuksen **Täsmäytä mennessä** -asetus määrittämää (*Sopimus* tai *Rivi*). Voit tehdä yhden rivin laskelmia vain tarjouksista, joissa **Täsmäytä mennessä** -kentän asetuksena on *Rivi*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Yhden tai useamman sopimuksen kaikkien rivien käsitteleminen

1. Avaa sen sopimustyypin luettelosivu, jota haluat käsitellä, avaamalla asianmukainen [ostohyvitysten sopimusten luettelosivu](rebate-management-deals.md).
1. Valitse kunkin käsiteltävän sopimuksen rivi (tai avaa käsiteltävä sopimus).
1. Valitse toimintoruudun **Ostohyvitysten hallinnan sopimukset** -välilehden **Luo**-ryhmästä jokin seuraavista komennoista:

    - **Käsittele \> Valmistele** – Valmistele jaksotusjoukko kutakin asiaankuuluvaa ostohyvityssopimusta varten, mutta älä kirjaa niitä.
    - **Käsittele \> Ostohyvityksen hallinta** – Käsittele tapahtumasarja, joka antaa ostohyvityksen arvon kullekin sopimukselle.
    - **Käsittele \> Kirjaa pois** – Palauta aiemmin kirjatut tapahtumat ja kirjaa ne pois, jotta uudet ostohyvityksen sopimustapahtumat voidaan laskea.

1. Määritä laskelman päivämääräalue asettamalla näyttöön tulevassa valintaikkunassa **Päivämäärästä**- ja **Päivämäärään**-kentät.
1. Suorita laskenta valitsemalla **OK**.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Valitun sopimuksen yhden tai useamman sopimusrivien käsitteleminen

1. Avaa sen sopimustyypin luettelosivu, jota haluat käsitellä, avaamalla asianmukainen [ostohyvitysten sopimusten luettelosivu](rebate-management-deals.md).
1. Avaa sopimus, jonka rivin haluat käsitellä.
1. Valitse oikeassa yläkulmassa oleva **Rivit**-välilehti.
1. Valitse **Ostohyvityksen hallinta** -pikavälilehdessä jokaisen käsiteltävän sopimusrivin rivi.
1. Valitse **Ostohyvityksen hallinta** -pikavälilehden työkaluriviltä jokin seuraavista komennoista. (Nämä komennot ovat käytettävissä vain sopimuksille, joissa **Täsmäytä mennessä** -kentän mukaan arvoksi määritetään *Rivi*.)

    - **Käsittele \> Valmistele** – Valmistele jaksotusjoukko kutakin asiaankuuluvaa sopimusriviä varten, mutta älä kirjaa niitä.
    - **Käsittele \> Ostohyvityksen hallinta** – Käsittele tapahtumasarja, joka antaa ostohyvityksen arvon kullekin sopimusriville.
    - **Käsittele \> Kirjaa pois** – Palauta aiemmin kirjatut tapahtumat ja kirjaa ne pois, jotta uudet ostohyvityksen sopimustapahtumat voidaan laskea.

1. Määritä laskelman päivämääräalue asettamalla näyttöön tulevassa valintaikkunassa **Päivämäärästä**- ja **Päivämäärään**-kentät.
1. Suorita laskenta valitsemalla **OK**.

### <a name="process-deals-using-a-batch-job"></a>Käsittele sopimukset erätyön avulla

Sen sijaan, että käsiteltäisiin tiettyjä sopimuksia tai sopimusrivejä, voit käsitellä useita sopimuksia erätyönä samanaikaisesti. Voit halutessasi käyttää tietuesuodattimia ja/tai määrittää toistuvan aikataulun. Voit käsitellä sopimukset erätyön avulla noudattamalla seuraavia vaiheita.

1. Noudata seuraavia ohjeita:

    - Siirry kohtaan **Ostohyvitysten hallinta \> Kausittaiset tehtävät \> Käsittele \> Valmistele** valmistellaksesi jaksotusjoukon kullekin asiaankuuluvalle sopimukselle kirjaamatta niitä.
    - Siirry kohtaan **Ostohyvityksen hallinta \> Kausittaiset tehtävät \> Käsittele \> Ostohyvityksen hallinta** käsitelläksesi tapahtumasarjan, joka antaa ostohyvityksen arvon kullekin sopimusriville.
    - Siirry kohtaan **Ostohyvityksen hallinta \> Kausittaiset tehtävät \> Käsittele \> Kirjaa pois** palauttaaksesi aiemmin kirjatut tapahtumat ja kirjataksesi ne pois, jotta uudet ostohyvityksen sopimustapahtumat voidaan laskea.

1. Määritä laskelman tapahtumien päivämääräalue valitsemalla **Kausi**-osan **Parametrit**-pikavälilehdellä näkyvässä valintaikkunassa **Päivämäärästä**- ja **Päivämäärään**-kentät.
1. Määritä laskelman takuiden päivämääräalue asettamalla **Takuukausi**-osassa **Päivämäärästä**- ja **Päivämäärään**-kentät.
1. Voit määrittää **Sisällytettävät tietueet** -pikavälilehdessä suodattimia, jotka rajoittavat erätyön käsittelemää sopimusjoukkoa. Nämä asetukset toimivat samalla tavalla kuin muiden erätöiden tyypeissä.
1. **Suorita taustalla** -pikavälilehdessä voit määrittää erätyön käsittelyn ja aikataulutuksen asetukset tarpeen mukaan. Nämä asetukset toimivat samalla tavalla kuin muiden erätöiden tyypeissä.
1. Suorita ja/tai aikatauluta laskennat valitsemalla **OK**.

## <a name="view-and-edit-rebate-management-transactions"></a>Ostohyvitysten hallintatapahtumien tarkasteleminen ja muokkaaminen

Kun käsittelet yhtä tai useita sopimuksia, järjestelmä luo tapahtumia, joita voit tarkastella ja mahdollisesti muokata ennen niiden kirjaamista.

1. Noudata seuraavia ohjeita:

    - Valitse sopimus, jonka tapahtumia haluat tarkastella (esimerkiksi [**Kaikki ostohyvitysten hallinnan sopimukset** -sivulla](rebate-management-deals.md)). Valitse toimintoruudun **Ostohyvityksen hallinnan sopimukset** -välilehden **Tapahtumat**-ryhmässä **Tapahtumat** tai **Takuutapahtumat** sen mukaan, minkä tyyppistä tapahtumaa haluat tarkastella.
    - Avaa sopimus (esimerkiksi [**Kaikki ostohyvitysten hallinnan sopimukset** -sivulla](rebate-management-deals.md)) tarkastellaksesi sen tietoja. Valitse sopimusrivi **Ostohyvityksen hallinta** -pikavälilehdestä tapahtumien tarkastelua varten. Valitse sitten työkaluriviltä **Tapahtumat** tai **Takuutapahtumat** sen mukaan, minkä tyyppisiä tapahtumia haluat tarkastella. (Nämä painikkeet ovat käytettävissä vain sopimuksille, joissa **Täsmäytä mennessä** -kentän mukaan arvoksi määritetään *Rivi*.)

1. Näkyviin tulee **Ostohyvityksen hallinnan päivämäärätapahtumat**- tai **Ostohyvitysten hallinnan takuutapahtumat** -sivu. Se sisältää ruudukon, jossa kukin rivi edustaa tapahtumakokoelmaa yksittäisestä ostohyvityksestä tai takuujaksosta. Valitse rivi ruudukosta ja valitse sitten toimintoruudusta **Lähdetapahtumat**, jos haluat tarkastella riviin kuuluvia tapahtumia.
1. Näyttöön tulevalla sivulla on luettelo valitulle riville kuuluvista valitun tyypin tapahtumista. Jokainen tapahtuma sisältää tapahtumatyypin mukaan merkitykselliset tiedot. Takuutapahtumille voi tarkastella vain luetteloa. Voit suorittaa muuntyyppisille tapahtumille tällä sivulla seuraavat toimenpiteet:

    - Voit tarkistaa sivun kaikkien vaadittujen tapahtumien kokonaisarvon **Vaadittu summa** -kentässä.
    - Voit tarkastella lisätietoja mistä tahansa tapahtumasta valitsemalla sen ja valitsemalla sitten **Yleiset**-, **Taloushallinnon dimensio**- tai **Dimensio**-välilehden.
    - Voit tarkastella kaikkia käytetteäviä vähennyksiä valitsemalla toimintoruudusta **Vähennystapahtumat**. Lisätietoja on [ostohyvitysten vähennysperiaatteissa](rebate-reduction-principle.md).
    - Jos haluat merkitä tapahtumat joko vaadituiksi tai ei-vaadituiksi, jos käytät vaatimusprosessia, valitse haluamasi rivit ja valitse sitten toimintoruudusta jokin seuraavista komennoista. (Vaatimusprosessit otetaan käyttöön [**Ostohyvitysten hallinnan parametrit** -sivulla](rebate-management-parameters.md).)

        - **Määritä vaadituiksi \> Kaikki** – Merkitse kaikki tapahtumat vaadituiksi.
        - **Määritä vaadituiksi \> Valitut** – Merkitse valitut tapahtumat vaadituiksi.
        - **Määritä ei-vaadituiksi \> Kaikki** – Merkitse kaikki tapahtumat ei-vaadituiksi.
        - **Määritä ei-vaadituiksi \> Valitut** – Merkitse valitut tapahtumat ei-vaadituiksi.

    - Voit kirjata yhden tai useita rivejä koskevat vaatimuksesi valitsemalla haluamasi rivit ja valitsemalla sitten toimintoruudusta **Kirjaa**. (**Kirjaa**-painike on käytettävissä vain ostohyvitystapahtumissa. Sitä ei voi käyttää valmistelu- ja poiskirjaustapahtumia varten.) **Kirjaa**-valintaikkunan **Päivämäärästä**- ja **Päivämäärään**-kentät määritetään automaattisesti. Määritä **Kirjauspäivämäärä** ja valitse sitten **OK**.
    - Voit oikaista minkä tahansa avoimen tai kirjaamattoman tapahtuman summan valitsemalla tapahtuman ja toimimalla seuraavasti:

        - Muokkaa **Korjattu summa** -kentän arvoa.
        - Valitse toimintoruudussa **Määritä korjaus**. Syötä sitten arvo **Korjattu summa** -kenttään näyttöön avatuvassa valintaikkunassa.

> [!NOTE]
> Kun käsittelet seuraavaa kautta, tapahtumaluettelossa ovat aiemman kirjauksen jälkeen käsittelemättömät tapahtumat sekä valitun kauden kaikki uudet tapahtumat.

## <a name="post-rebates-transactions"></a>Kirjaa ostohyvitystapahtumat

Ostohyvitysten ja vähennysten arvon kirjaamiseksi on suoritettava kirjausprosessi, ellet ole määrittänyt järjestelmääsi kirjaamaan niitä automaattisesti.

### <a name="set-up-the-system-to-post-all-transactions-automatically"></a>Määritä järjestelmä kitjaamaan kaikki tapahtumat automaattisesti

Voit määrittää järjestelmän kirjaamaan kaikki tapahtumat heti niiden generoinnin jälkeen ottamalla käyttöön **Kirjaa kirjauskansiot automaattisesti** ja/tai **Kirjaa vapaatekstilaskut automaattisesti** -asetukset **Ostohyvityksen hallinnan parametrit** -sivulla. Lisätietoja on kohdassa [Ostohyvityksen hallinnan parametrit](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Yhden tai useamman sopimuksen kaikkien rivien tapahtumien kirjaaminen

Jos et käytä automaattista kirjausta, kun olet käsitellyt asiaankuuluvat sopimukset, tarkista ja kirjaa kaikkien rivien luodut tapahtumat yhdelle tai useammalle sopimukselle.

1. Avaa sen sopimustyypin luettelosivu, jota haluat käsitellä, avaamalla asianmukainen [ostohyvitysten sopimusten luettelosivu](rebate-management-deals.md).
1. Valitse kunkin kirjattavan sopimuksen rivi (tai avaa kirjattava sopimus).
1. Valitse toimintoruudun **Ostohyvitysten hallinnan sopimukset** -välilehden **Luo**-ryhmästä jokin seuraavista komennoista:

    - **Kirjaa \> Valmistele** – Kirjaa luomasi käytettävissä olevat jaksotustapahtumat.
    - **Kirjaa \> Ostohyvitysten hallinta** – Kirjaa luomasi käytettävissä olevat ostohyvitystapahtumat.
    - **Kirjaa \> Kirjaa pois** – Kirjaa luomasi käytettävissä olevat poiskirjaustapahtumat.

1. Määritä näyttöön tulevassa valintaikkunassa **Kirjauspäivämäärä**-kenttä. Määritä kirjattavien tapahtumien päivämääräalue asettamalla **Päivämäärästä**- ja **Päivämäärään**-kentät.
1. Kirjaa tapahtumat valitsemalla **OK**.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Valitun sopimuksen yhden tai useamman sopimusrivien tapahtumien kirjaaminen

Jos et käytä automaattista kirjausta, kun olet käsitellyt asiaankuuluvat sopimukset, tarkista ja kirjaa kaikkien rivien luodut tapahtumat yhdelle tai useammalle valitun sopimuksen tietylle sopimusriville.

1. Avaa sen sopimustyypin luettelosivu, jota haluat käsitellä, avaamalla asianmukainen [ostohyvitysten sopimusten luettelosivu](rebate-management-deals.md).
1. Avaa sopimus, jolla on rivi, jolle haluat kirjata tapahtumia.
1. Valitse oikeassa yläkulmassa oleva **Rivit**-välilehti.
1. Valitse **Ostohyvityksen hallinta** -pikavälilehdessä jokaisen kirjattavan sopimusrivin rivi.
1. Valitse **Ostohyvityksen hallinta** -pikavälilehden työkaluriviltä jokin seuraavista komennoista. (Nämä komennot ovat käytettävissä vain sopimuksille, joissa **Täsmäytä mennessä** -arvoksi määritetään *Rivi*.)

    - **Kirjaa \> Valmistele** – Kirjaa luomasi käytettävissä olevat jaksotustapahtumat.
    - **Kirjaa \> Ostohyvitysten hallinta** – Kirjaa luomasi käytettävissä olevat ostohyvitystapahtumat.
    - **Kirjaa \> Kirjaa pois** – Kirjaa luomasi käytettävissä olevat poiskirjaustapahtumat.

1. Määritä näyttöön tulevassa valintaikkunassa **Kirjauspäivämäärä**-kenttä. Määritä kirjattavien tapahtumien päivämääräalue asettamalla **Päivämäärästä**- ja **Päivämäärään**-kentät.
1. Kirjaa tapahtumat valitsemalla **OK**.

### <a name="post-transactions-using-a-batch-job"></a>Tapahtumien kirjaaminen erätyön avulla

Sen sijaan, että tapahtumat kirjataisiin tietyille sopimuksille tai sopimusriveille, voit kirjata tapahtumia useille sopimuksille erätyönä samanaikaisesti. Voit halutessasi käyttää tietuesuodattimia ja/tai määrittää toistuvan aikataulun. Voit kirjata tapahtumat erätyön avulla noudattamalla seuraavia vaiheita.

1. Noudata seuraavia ohjeita:

    - Kirjaa luomasi käytettävissä olevat jaksotustapahtumat siirtymällä kohtaan **Ostohyvitysten hallinta \> Kausittaiset tehtävät \> Kirjaa \> Valmistele**.
    - Kirjaa luomasi käytettävissä olevat ostohyvitystapahtumat siirtymällä kohtaan **Ostohyvitysten hallinta \> Kausittaiset tehtävät \> Kirjaa \> Ostohyvitysten hallinta**.
    - Kirjaa luomasi käytettävissä olevat poiskirjaustapahtumat siirtymällä kohtaan **Ostohyvitysten hallinta \> Kausittaiset tehtävät \> Kirjaa \> Kirjaa pois**.

1. Määritä **Kirjauspäivämäärä**-kenttä **Kausi**-osan **Parametrit**-pikavälilehdessä näkyvässä valintaikkunassa. Määritä kirjattavien tapahtumien päivämääräalue asettamalla **Päivämäärästä**- ja **Päivämäärään**-kentät. 
1. Määritä kirjattavien takuiden päivämääräalue asettamalla **Takuukausi**-osassa **Päivämäärästä**- ja **Päivämäärään**-kentät.
1. Voit määrittää **Sisällytettävät tietueet** -pikavälilehdessä suodattimia, jotka rajoittavat erätyön käsittelemää sopimusjoukkoa. Nämä asetukset toimivat samalla tavalla kuin muiden erätöiden tyypeissä.
1. **Suorita taustalla** -pikavälilehdessä voit määrittää erätyön käsittelyn ja aikataulutuksen asetukset tarpeen mukaan. Nämä asetukset toimivat samalla tavalla kuin muiden erätöiden tyypeissä.
1. Suorita ja/tai aikatauluta laskennat valitsemalla **OK**.

## <a name="review-rebate-management-journals"></a>Ostohyvitysten hallinnan kirjauskansioiden tarkasteleminen

Kun tapahtumat on kirjattu, voit tarkistaa tuloksena olevat kirjauskansiot, asiakirjat tai nimikkeet. Ostohyvitysten ja rojaltin kohdetapahtumat perustuvat maksutyyppiin, joka on määritetty kirjausprofiilissa ja ostohyvityksen tulostyypissä. Jos ostohyvityksen tuloksen arvoksi määritetään esimerkiksi *Nimike*, myyntitilaus luodaan ja sitä voidaan tarkastella kohdetapahtumien kautta. Jos maksu on määritetty käyttämään ostoreskontraa, asiakkaassa määritetty toimittajalasku toimittajalle luodaan myös asiakkaan ostohyvitystä varten.

Noudattamalla näitä vaiheita voit tarkistaa ostohyvitysten hallinnan sopimukseen liittyvät kirjauskansiomerkinnät.

1. Avaa sen sopimustyypin luettelosivu, jota haluat käsitellä, avaamalla asianmukainen [ostohyvitysten sopimusten luettelosivu](rebate-management-deals.md).
1. Valitse sopimus, jonka kirjauskansioiden kirjaukset tarkastetaan.
1. Valitse toimintoruudun **Ostohyvityksen hallinnan sopimukset** -välilehden **Tapahtumat**-ryhmässä joko **Tapahtumat** tai **Osohyvitystapahtumat** sen mukaan, minkä tyyppistä tapahtumaa haluat tarkastella.
1. Varmista, että **Näytä**-kentän arvoksi on määritetty *Kaikki* tai *Kirjattu*.
1. Etsi ja valitse tapahtumakokoelma, jonka haluat tarkastaa, ja valitse sitten toimintoruudusta jokin seuraavista painikkeista. (Nämä painikkeet ovat käytettävissä vain, kun valitulle tapahtumakokoelmalle on olemassa asianmukaisia kirjauksia.)

    - **Kohdetapahtumat** – Tarkastele valitun sopimuksen luomia kirjauskansioita ja muita tiedostotyyppejä.
    - **Nimikkeet** – Tarkastele valitun sopimuksen luomia nimikkeitä.

1. Näyttöön tulee luettelo kirjauskansioista, asiakirjoista tai nimikkeistä. Jos haluat lisätietoja kirjauskansiosta, asiakirjasta tai nimikkeestä, valitse sen rivi ja valitse sitten toimintoruudusta **Näytä tiedot**.
