---
title: Ostohyvitysten käsitteleminen, tarkistaminen ja kirjaaminen
description: Tässä artikkelissa kuvataan, miten ostohyvitysten hallinnan tarjoukset käsitellään, miten niiden alennukset lasketaan, luodut tapahtumat tarkistetaan, tapahtumat kirjataan ja kirjaukset tarkistetaan.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e63f02e5e93ec2ce8c321a20c2a0c5886edcbe42
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901934"
---
# <a name="process-review-and-post-rebates"></a>Ostohyvitysten käsitteleminen, tarkistaminen ja kirjaaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten ostohyvitysten hallinnan tarjoukset käsitellään, miten niiden alennukset lasketaan, luodut tapahtumat tarkistetaan, tapahtumat kirjataan ja kirjaukset tarkistetaan.

## <a name="change-the-status-of-a-deal"></a>Sopimuksen tilan muuttaminen

Voit seurata sopimusta määrittämällä kullekin sopimukselle tilan. Tila on tarkoitettu vain tiedoksi.

1. Valitse sopimus (esimerkiksi [**Kaikki ostohyvityksen hallinnan sopimukset** -sivulla](rebate-management-deals.md)).
1. Valitse toimintoruudun **Ostohyvitysten hallinnan sopimukset**-välilehden **Ylläpidä** -ryhmässä **Muuta tilaa**.
1. Määritä **Muuta tila** -valintaikkunassa **Ostohyvityksen tila** -kentässä uusi tila.
1. Valitse **OK**.

## <a name="calculate-fifo-purchase-prices"></a>FIFO-ostohintojen laskeminen

**Laske FIFO-ostohinta** kausittainen tehtävä on suoritettava, jotta voit laskea niiden [sopimusten](rebate-management-deals.md) ostohyvitykset, joissa **Hintaperuste**-kentän arvoksi on määritetty *FIFO*. Järjestelmä laskee myydyn varaston arvon FIFO (first in, first out) -säännön avulla. Tämän jälkeen käytetään tätä arvoa toimittajien ostohyvitysten laskemiseen.

Siirry kohtaan **Ostohyvitysten hallinta \> Kausittaiset tehtävät \> Laske FIFO-ostohinta**. Suorita laskenta valitsemalla näyttöön tulevassa valintaikkunassa **OK**.

## <a name="create-source-transactions"></a>Lähdetapahtumien luominen

Voit luoda myynti- tai ostotilauksia, joissa on lähdetapahtumia joko ennen sovellettavien ostohyvitystenhallintasopimuksen luontia tai sen jälkeen.

Voit määrittää jokaisen sopimusrivin niin, että se luo automaattisesti ostohyvitysehdotuksen kirjaamalla myyntitilauksen tai ostotilauksen toimituksen tai laskun. Määritä sopimusrivin **tapahtumalajin** kentän arvoksi *Toimitus* tai *Lasku* ja määritä **Kirjausprosessissa**-asetuksen arvoksi *Kyllä*. Jos **Tapahtumalaji**-kentän arvoksi määritetään *Tilaus*, kirjaamisen käsittely poistetaan käytöstä. Lähdetapahtumille, jotka on luotu kaupan aktivoinnin jälkeen, voit silti käsitellä varausta tämän artikkelin myöhemmässä [Prosessihyvitysten hallintasopimukset](#process-deals) -osiossa kuvatulla tavalla.

### <a name="enable-price-details"></a>Ota käyttöön hintatiedot

Ennen kuin voit luoda lähdetapahtumia, sinun on otettava käyttöön myyntireskontran **Hintatietojen käyttöönotto** -vaihtoehto.

1. Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
1. Määritä **Hinnat**-välilehden **Hintatiedot** -pikavälilehdessä **Ota käyttöön hintatiedot** -asetukseksi *Kyllä*.

### <a name="create-a-source-transaction"></a>Lähdetapahtuman luominen

Voit luoda lähdetapahtuman seuraavien ohjeiden avulla.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse **Uusi**.

    Jotta voit jäljitellä alennusvaatimusten luomistapaa, sinun on nyt luotava myyntitilaus, jossa tuote ja määrä täyttävät asiakkaan alennuksen.

1. Lisää tai valitse **Asiakastili**-kentässä asiakas, joka voi tehdä ostohyvityssopimuksen.
1. Luo myyntitilaus valitsemalla **OK**.
1. Lisää **Myyntitilausrivit**-pikavälilehdessä rivi, ja määritä sille seuraavat kentät:

    - **Nimiketunnus** – Määritä nimike, joka oikeuttaa ostohyvitykseen.
    - **Määrä** – Määritä määrä, joka oikeuttaa ostohyvityssopimuksiin. Se sisältää rivin, jonka **Peruste**-kentän arvoksi on määritetty *Määrä*.
    - **Yksikköhinta** – Määritä hinta, joka oikeuttaa ostohyvityssopimuksiin. Se sisältää rivin, jonka **Peruste**-kentän arvoksi on määritetty *Arvo*.
    - **Toimipaikka** – Valitse toimipaikka, jossa tuote on käytettävissä ja joka oikeuttaa ostohyvityssopimuksiin.
    - **Varasto** – Valitse varasto, jossa tuote on käytettävissä ja joka oikeuttaa ostohyvityssopimuksiin.

1. Valitse työkaluriviltä **Myyntitilausrivit**-pikavälilehdestä **Myyntilausrivi \> Hintatiedot**. Tämä komento on käytettävissä vain, jos hintatiedot on otettu käyttöön edellisessä osassa kuvatulla tavalla.
1. Valitse **Hintatiedot**-sivulta **Ostohyvitysten hallinta** -pikavälilehti. Tällä pikavälilehdellä on luettelo kaikista alennuksenhallintasopimuksista, jotka koskevat nykyistä tilausriviä, ja se näyttää arvioidun hyvityksen määrän tilauksen valuutassa. Huomaa, että summat ovat vain arvioita tulevista ostohyvitysvaatimuksista. Todelliset ostohyvityssummat voivat olla erilaiset. Seuraavassa on joitakin tekijöitä, jotka saattavat vaikuttaa toteutuneisiin summiin:

    - Kokonaismyyntimäärä, jonka asiakas on saanut kausittaisen ostohyvityssopimuksen perusteella.
    - Onko asiakas palauttanut kaikki määrät vai osamääriä.
    - Onko myyntitilauksen perusteella saavutettu ostohyvityksen hallintaa varten määritetty tapahtumatyyppi (*Tilaus, Toimitus* vai *Lasku*).
    - Sopimuksen **tuotoksen** arvo. Näkyviin tulee tyhjä ostohyvityssumma tarjouksille, joissa **Toimitus**-kentän arvoksi on määritetty *Nimike*.

1. Huomaa **Tiedot**-pikavälilehdellä, että **Marginaalin arviointi** -osa sisältää seuraavat kentät. Nämä kentät lisätään ostohyvityksen hallinnan avulla. Kaikissa kentissä näkyy yksikkökohtainen arvo (kun taas **Ostohyvityksen hallinta** -pikavälilehden kentissä näkyvät rivin kokonaisarvot).

    - **Ostohyvityksen hallinnan ostohyvityksen summa** (vain myyntitilaukset)
    - **Ostohyvityksen hallinnan rojaltisumma** (vain myyntitilaukset)
    - **Ostohyvityksenhallinnan toimittajan ostohyvityksen summa** (myyntitilaukset ja ostotilaukset)

1. Sulje **Hintatiedot**-sivu.
1. Jos myyntitilaus ei saisi juuri katseltuja alennuksia, poista alennukset noudattamalla näitä ohjeita. (Ostohyvityksiä ei yleensä suljeta pois.)

    1. Valitse oleellinen rivi **Myyntitilausrivit**-pikavälilehdessä.
    1. Määritä **Rivitiedot**-pikavälilehden **Hinta ja alennus** -välilehdessä **Sulje pois ostohyvitysten hallinnasta** -asetuksen arvoksi *Kyllä*. Tämä vaihtoehto ei koske ostotilauksia. Lisäksi vain asiakkaan ostohyvitykset jätetään pois, kun tämän asetuksen arvoksi on määritetty *Kyllä*. Asiakkaan maksuhyvitys ja toimittajan ostohyvitykset ovat yhä voimassa.

1. Valitse Toimintoruudun **Keräys ja pakkaus** -välilehden **Luo**-ryhmästä **Kirjaa pakkausluettelo**.
1. Valitse **Parametrit**-pikavälilehden **Määrä**-kentästä *Kaikki*.
1. Valitse **OK**.
1. Jos järjestelmä pyytää vahvistamaan toiminnon, valitse **OK**.
1. Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.
1. Valitse **Parametrit**-pikavälilehden **Määrä**-kentästä *Kaikki* tai *Pakkausluettelo*.
1. Valitse **OK**.
1. Jos järjestelmä pyytää vahvistamaan toiminnon, valitse **OK**.

## <a name="process-rebate-management-deals"></a><a name="process-deals"></a>Käsittele ostohyvitysten hallintasopimukset

Kun sopimukset käsitellään, järjestelmä laskee kaikki asianmukaiset ostohyvitykset ja rojaltit. Vain valitut tarjoukset, joiden laskentakaudet ovat valmiita laskettavaksi ja joiden tila on *Aktiivinen*, käsitellään. Kun käsittely on valmis, järjestelmä luo joukon tapahtumia, jotka voit tarkistaa ja kirjata.

> [!NOTE]
> Ostohyvitykset käsitellään aina tasolla, jonka kunkin sopimuksen **Täsmäytä mennessä** -asetus määrittämää (*Sopimus* tai *Rivi*). Voit tehdä yhden rivin laskelmia vain tarjouksista, joissa **Täsmäytä mennessä** -kentän asetuksena on *Rivi*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Yhden tai useamman sopimuksen kaikkien rivien käsitteleminen

1. Avaa sen sopimustyypin luettelosivu, jota haluat käsitellä, avaamalla asianmukainen [ostohyvitysten sopimusten luettelosivu](rebate-management-deals.md).
1. Valitse kunkin käsiteltävän sopimuksen rivi (tai avaa käsiteltävä sopimus).
1. Valitse toimintoruudun **Ostohyvitysten hallinnan sopimukset** -välilehden **Luo**-ryhmästä jokin seuraavista komennoista:

    - **Käsittele \> Valmistele** – Valmistele jaksotusjoukko kutakin asiaankuuluvaa ostohyvityssopimusta varten, mutta älä kirjaa niitä. Tämä valikkokohde ei ole käytettävissä tarjouksille, joissa **ostohyvityksen toimitus** -kentän arvoksi on määritetty *Nimike*.
    - **Käsittele \> Ostohyvityksen hallinta** – Käsittele tapahtumasarja, joka antaa ostohyvityksen arvon kullekin sopimukselle.
    - **Prosessi \> Poiskirjaus** – Käsittele kullekin ostohyvityssopimuksen ja määritetyn kauden lähdetapahtumalle varalle kirjattujen summien ja ostohyvitysten hallinnan välinen ero. Tämä valikkokohde ei ole käytettävissä tarjouksille, joissa **ostohyvityksen toimitus** -kentän arvoksi on määritetty *Nimike*.

1. Määritä laskelman päivämääräalue asettamalla näyttöön tulevassa valintaikkunassa **Päivämäärästä**- ja **Päivämäärään**-kentät.
1. Suorita laskenta valitsemalla **OK**.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Valitun sopimuksen yhden tai useamman sopimusrivien käsitteleminen

1. Avaa sen sopimustyypin luettelosivu, jota haluat käsitellä, avaamalla asianmukainen [ostohyvitysten sopimusten luettelosivu](rebate-management-deals.md).
1. Avaa sopimus, jonka rivin haluat käsitellä.
1. Valitse oikeassa yläkulmassa oleva **Rivit**-välilehti.
1. Valitse **Ostohyvityksen hallinta** -pikavälilehdessä jokaisen käsiteltävän sopimusrivin rivi.
1. Valitse **Ostohyvityksen hallinta** -pikavälilehden työkaluriviltä jokin seuraavista komennoista. (Nämä komennot ovat käytettävissä vain sopimuksille, joissa **Täsmäytä mennessä** -kentän mukaan arvoksi määritetään *Rivi*.)

    - **Käsittele \> Valmistele** – Valmistele jaksotusjoukko kutakin asiaankuuluvaa sopimusriviä varten, mutta älä kirjaa niitä. Tämä valikkokohde ei ole käytettävissä tarjouksille, joissa **ostohyvityksen toimitus** -kentän arvoksi on määritetty *Nimike*.
    - **Käsittele \> Ostohyvityksen hallinta** – Käsittele tapahtumasarja, joka antaa ostohyvityksen arvon kullekin sopimusriville.
    - **Prosessi \> Poiskirjaus** – Käsittele kullekin ostohyvityssopimuksen ja määritetyn kauden lähdetapahtumalle varalle kirjattujen summien ja ostohyvitysten hallinnan välinen ero. Tämä valikkokohde ei ole käytettävissä tarjouksille, joissa **ostohyvityksen toimitus** -kentän arvoksi on määritetty *Nimike*. 

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

### <a name="process-deals-by-using-the-rebate-workbench"></a>Käsittelee tarjoukset ostohyvityksen työtilan avulla

Sen sijaan, että käsiteltäisiin tiettyjä sopimuksia tai sopimusrivejä, voit käyttää *ostohyvityksen työtilaa* käsitelläksesi useita sopimuksia samanaikaisesti. Voit halutessasi käyttää tietuesuodattimia ja/tai määrittää toistuvan aikataulun. Rivejä ei tarvitse valita. Järjestelmä käsittelee kaikki rivit, jotka täyttävät asettamasi päivämäärä- ja suodatusvaatimukset.

Voit käsitellä sopimukset ostohyvityksen työtilan avulla noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Ostohyvityksen hallinta \> Ostohyvityksen hallintasopimukset \> Ostohyvityksen työtila**.
1. Valitse toimintoruudun **Ostohyvitysten työtila** -välilehden **Käsittely**-ryhmästä jokin seuraavista komennoista:

    - **Käsittele \> Valmistele** – Valmistele jaksotusjoukko kutakin asiaankuuluvaa sopimusriviä varten, mutta älä kirjaa jaksotuksia.
    - **Käsittele \> Ostohyvityksen hallinta** – Käsittele tapahtumasarja, joka antaa ostohyvityksen arvon kullekin sopimusriville.
    - **Prosessi \> Poiskirjaus** – Käsittele varauksen ja hyvityksen hallinnan välinen ero, joka kirjataan kullekin lähdetapahtumalle alennussopimusta ja tiettyä ajanjaksoa kohti.

1. Määritä laskelman tapahtumien päivämääräalue valitsemalla **Kausi**-osan **Ostohyvitysten hallinta**-valintaikkunassa näkyvässä valintaikkunassa **Päivämäärästä**- ja **Päivämäärään**-kentät.
1. Määritä laskelman takuiden päivämääräalue asettamalla **Takuukausi**-osassa **Päivämäärästä**- ja **Päivämäärään**-kentät.
1. Voit määrittää **Sisällytettävät tietueet** -pikavälilehdessä suodattimia, jotka rajoittavat erätyön käsittelemää sopimusjoukkoa. Nämä asetukset toimivat samalla tavalla kuin muiden erätöiden tyypeissä.
1. **Suorita taustalla** -pikavälilehdessä voit määrittää erätyön käsittelyn ja aikataulutuksen asetukset tarpeen mukaan. Nämä asetukset toimivat samalla tavalla kuin muiden erätöiden tyypeissä.
1. Suorita ja/tai aikatauluta laskennat valitsemalla **OK**.

## <a name="view-and-edit-rebate-management-transactions"></a>Ostohyvitysten hallintatapahtumien tarkasteleminen ja muokkaaminen

Kun käsittelet yhtä tai useita sopimuksia, järjestelmä luo tapahtumia, joita voit tarkastella ja mahdollisesti muokata ennen niiden kirjaamista.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-deals-list-page"></a>Ostohyvitysten hallintatapahtumien tarkasteleminen ja muokkaaminen ostohyvitysten tarjousten luettelosivun avulla

Voit tarkastella ja muokata Ostohyvitysten hallintatapahtumia alennustarjousten luettelosivun avulla seuraavasti.

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

    - Kirjaa vaatimus kaikille asiaankuuluville riveille valitsemalla toimintoruudusta **Kirjaa**. Jos käytät lunastusprosessia (kun **Ostohyvitysten hallinnan parametrit** -sivulla on käytössä **Käytä vaatimusprosessia** -vaihtoehto), vain ne rivit, jotka on merkitty **lunastetuiksi**, kirjataan. Muussa tapauksessa kaikki valitun ostohyvitystapahtuman lähdetapahtumat kirjataan. **Kirjaa**-painike on käytettävissä vain ostohyvitystapahtumissa. Sitä ei voi käyttää varaus- ja alennustapahtumista. **Kirjaa**-valintaikkunan **Päivämäärästä**- ja **Päivämäärään**-kentät määritetään automaattisesti. Määritä **Kirjauspäivämäärä** ja valitse sitten **OK**.
    - Voit oikaista minkä tahansa avoimen tai kirjaamattoman tapahtuman summan valitsemalla tapahtuman ja toimimalla seuraavasti:

        - Muokkaa **Korjattu summa** -kentän arvoa.
        - Valitse toimintoruudussa **Määritä korjaus**. Syötä sitten arvo **Korjattu summa** -kenttään näyttöön avatuvassa valintaikkunassa.

> [!NOTE]
> Jos käytät lunastusprosessia, kun käsittelet seuraavaa kautta, tapahtumaluettelossa ovat aiemman kirjauksen jälkeen käsittelemättömät tapahtumat sekä valitun kauden kaikki uudet tapahtumat.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-workbench"></a>Ostohyvitysten hallintatapahtumien tarkasteleminen ja muokkaaminen ostohyvitysten työtilan avulla

Voit tarkastella ja muokata Ostohyvitysten hallintatapahtumia ostohyvityksen työtilan avulla seuraavasti.

1. Siirry kohtaan **Ostohyvityksen hallinta \> Ostohyvityksen hallintasopimukset \> Ostohyvityksen työtila**.
1. Määritä **Näytä**-kentän arvoksi *Ei kirjattu*.
1. **Ostohyvitystyötila**-sivulla näkyy luettelo tapahtumista. Jokainen tapahtuma sisältää asianmukaiset tiedot. Nämä tiedot vaihtelevat tapahtumatyypin mukaan. Tällä sivulla voi tehdä seuraavia toimenpiteitä:

    - Voit tarkastella lisätietoja mistä tahansa tapahtumasta valitsemalla sen ja valitsemalla sitten **Yleiset**-, **Taloushallinnon dimensio**- tai **Dimensio**-välilehden.
    - Jos käytät vaatimuksia, voit merkitä tapahtumat joko lunastetuiksi tai lunastamattomiksi. Valitse asiaankuuluvat rivit ja valitse sitten toimintoruudussa **Ostohyvitysten työtila** -välilehdellä jokin seuraavista komennoista. (Vaatimusprosessit otetaan käyttöön [**Ostohyvitysten hallinnan parametrit**](rebate-management-parameters.md) -sivulla.)

        - **Määritä lunastetuiksi** – Merkitse valitut tapahtumat lunastetuiksi.
        - **Määritä lunastamattomiksi** – Merkitse valitut tapahtumat lunastamattomiksi.

    - Voit kirjata yhden tai useita rivejä koskevat vaatimuksesi valitsemalla haluamasi rivit. Valitse sitten toimintoruudun **Ostohyvitysten työtila** -välilehdessä **Kirjaa**. **Kirjaa**-painike on käytettävissä varauksia, ostohyvitystä ja alennustapahtumia varten. **Kirjaa**-valintaikkunan **Päivämäärästä**- ja **Päivämäärään**-kentät määritetään automaattisesti. Määritä **Kirjauspäivämäärä** ja valitse sitten **OK**.
    - Voit oikaista minkä tahansa avoimen tai kirjaamattoman tapahtuman summan valitsemalla tapahtuman ja toimimalla seuraavasti:

        - Muokkaa **Korjattu summa** -kentän arvoa.
        - Valitse toimintoruudun **Ostohyvitysten työtila** -välilehdessä **Aseta korjaus**. Syötä sitten arvo **Korjattu summa** -kenttään näyttöön avatuvassa valintaikkunassa.

> [!NOTE]
> Jos käytät lunastusprosessia, kun käsittelet seuraavaa kautta, tapahtumaluettelossa ovat aiemman kirjauksen jälkeen käsittelemättömät tapahtumat sekä valitun kauden kaikki uudet tapahtumat.

## <a name="post-rebates-transactions"></a>Kirjaa ostohyvitystapahtumat

Kirjaa käsiteltyjen varausten, ostohyvitysten hallinnan summan ja alennuksen arvo, kun suoritat kirjausprosessin. Kirjausprosessi merkitsee kirjattavat varaus-, ostohyvitysten tai -hyvitystapahtumien kirjaukset ja luo kohdetapahtuman. Jos kohdetapahtumaa ei tarvitse tarkistaa, nämä tapahtumat voidaan määrittää niin, että ne kirjataan automaattisesti.

### <a name="set-up-the-system-to-post-all-target-transactions-automatically"></a>Määritä järjestelmä kirjaamaan kaikki kohdetapahtumat automaattisesti

Määritä järjestelmäsi kirjaamaan kaikki kohdetapahtumat heti, kun ne on luotu luomalla lähetysvaraus, alennusten hallinta ja poistot, ottamalla käyttöön **Kirjaa kirjauskansiot automaattisesti** ja/tai **Kirjaa vapaatekstilaskut automaattisesti** -asetukset **Ostohyvityksen hallinnan parametrit** -sivulla. Lisätietoja on kohdassa [Ostohyvityksen hallinnan parametrit](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Yhden tai useamman sopimuksen kaikkien rivien tapahtumien kirjaaminen

Sen jälkeen, kun olet käsitellyt asiaankuuluvat sopimukset, tarkista ja kirjaa kaikkien rivien luodut tapahtumat yhdelle tai useammalle sopimukselle.

1. Avaa sen sopimustyypin luettelosivu, jota haluat käsitellä, avaamalla asianmukainen [ostohyvitysten sopimusten luettelosivu](rebate-management-deals.md).
1. Valitse kunkin kirjattavan sopimuksen rivi (tai avaa kirjattava sopimus).
1. Valitse toimintoruudun **Ostohyvitysten hallinnan sopimukset** -välilehden **Luo**-ryhmästä jokin seuraavista komennoista:

    - **Kirjaa \> Valmistele** – Kirjaa luomasi käytettävissä olevat jaksotustapahtumat.
    - **Kirjaa \> Ostohyvitysten hallinta** – Kirjaa luomasi käytettävissä olevat ostohyvitystapahtumat.
    - **Kirjaa \> Kirjaa pois** – Kirjaa luomasi käytettävissä olevat poiskirjaustapahtumat.

1. Määritä näyttöön tulevassa valintaikkunassa **Kirjauspäivämäärä**-kenttä. Määritä kirjattavien tapahtumien päivämääräalue asettamalla **Päivämäärästä**- ja **Päivämäärään**-kentät.
1. Kirjaa tapahtumat valitsemalla **OK**.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Valitun sopimuksen yhden tai useamman sopimusrivien tapahtumien kirjaaminen

Sen jälkeen, kun olet käsitellyt asiaankuuluvat sopimukset, tarkista ja kirjaa kaikkien rivien luodut tapahtumat yhdelle tai useammalle tietylle sopimusriville tietyssä sopimuksessa. Tämä menettely on käytettävissä vain sopimuksille, joissa **Täsmäytä mennessä** -kentän mukaan arvoksi määritetään *Rivi*.

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

### <a name="post-transactions-by-using-the-rebate-workbench"></a>Kirjaa tapahtumat ostohyvityksen työtilan avulla

Kun olet käsitellyt varaus-, ostohyvitys- tai poiskirjaustapahtumia, voit tarkistaa ja kirjata kaikkien tarjousten yhden tai usean tapahtumarivin luodut tapahtumat ostohyvityksen työn perusteella näiden vaiheiden avulla.

1. Siirry kohtaan **Ostohyvityksen hallinta \> Ostohyvityksen hallintasopimukset \> Ostohyvityksen työtila**.
1. Valitse ruudukosta rivi kullekin tapahtumariville, jonka haluat kirjata. Voit valita kirjaamattomia varaus-, ostohyvitys- ja/tai poiskirjaustapahtumia. Seuraavat säännöt pätevät:

    - Järjestelmä kirjaa myös kaikki rivit, joissa on sama **ostohyvitystapahtuman numero** -arvo kuin valitset riveillä.
    - Järjestelmä ei kirjaa *Ostohyvitys*-tapahtuman rivejä, joita ei ole merkitty lunastetuksi.
    - Jos valitset jo kirjattuja rivejä, järjestelmä ohittaa kirjatut rivit.
    - **Kirjaa**-painike on käytettävissä vain, jos valitset vähintään yhden kirjaamattoman rivin.

1. Valitse toimintoruudun **Ostohyvityksen työtila**-välilehden **Käsitellään**-ryhmässä **Kirjaa**.
1. Määritä **Kirjaa**-valintaikkunassa **Kirjauspäivämäärä**-kenttä. **Päivämäärästä**- ja **Päivämäärään**-kentät määritetään automaattisesti valittujen rivien aikaisimman **alkupäivämäärän** ja viimeisimmän **päättymispäivän** arvon perusteella.
1. Kirjaa tapahtumat valitsemalla **OK**.

## <a name="review-rebate-management-journals"></a><a name="review-journals"></a>Ostohyvitysten hallinnan kirjauskansioiden tarkasteleminen

Kun tapahtumat on kirjattu, voit tarkistaa tuloksena olevat kirjauskansiot, asiakirjat tai nimikkeet. Ostohyvitysten ja rojaltin kohdetapahtumat perustuvat maksutyyppiin, joka on määritetty kirjausprofiilissa ja ostohyvityksen tulostyypissä. Jos ostohyvityksen tuotoksen arvoksi määritetään esimerkiksi *Nimike*, asiakkaan ostohyvitykselle luodaan myyntitilaus ja toimittajan ostohyvitykselle luodaan ostotilaus. Näitä tilauksia voi tarkastella tavoitetapahtumien kautta. Jos maksu on määritetty käyttämään ostoreskontraa, asiakkaassa määritetty toimittajalasku toimittajalle luodaan myös asiakkaan ostohyvitystä varten.

### <a name="review-journals-by-using-the-rebate-deals-list-page"></a>Kirjauskansioiden tarkasteleminen ostohyvitysten luettelosivun avulla

Noudattamalla näitä vaiheita voit tarkistaa ostohyvitysten hallinnan sopimukseen liittyvät kirjauskansiomerkinnät.

1. Avaa sen sopimustyypin luettelosivu, jota haluat käsitellä, avaamalla asianmukainen [ostohyvitysten sopimusten luettelosivu](rebate-management-deals.md).
1. Valitse sopimus, jonka kirjauskansioiden kirjaukset tarkastetaan.
1. Valitse toimintoruudun **Ostohyvityksen hallinnan sopimukset** -välilehden **Tapahtumat**-ryhmässä joko **Tapahtumat** tai **Takuutapahtumat** sen mukaan, minkä tyyppistä tapahtumaa haluat tarkastella.
1. Määritä **Näytä**-kentän arvoksi *Kaikki* tai *Kirjattu*.
1. Etsi ja valitse tapahtumakokoelma, jonka haluat tarkastaa, ja valitse sitten toimintoruudusta jokin seuraavista painikkeista. (Nämä painikkeet ovat käytettävissä vain, kun valitulle tapahtumakokoelmalle on olemassa asianmukaisia kirjauksia.)

    - **Kohdetapahtumat** – Tarkastele valitun sopimuksen luomia kirjauskansioita ja muita tiedostotyyppejä.
    - **Nimikkeet** – Tarkastele valitun sopimuksen luomia myynti- tai ostotilauksia.

1. Näyttöön tulee luettelo kirjauskansioista, asiakirjoista tai nimikkeistä. Jos haluat lisätietoja kirjauskansiosta, asiakirjasta tai nimikkeestä, valitse sen rivi ja valitse sitten toimintoruudusta **Näytä tiedot**.

### <a name="review-journals-by-using-the-rebate-workbench"></a>Tarkista kirjauskansiot ostohyvityksen työtilan avulla

Voit tarkastaa kirjauskansiot ostohyvityksen työtilan avulla noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Ostohyvityksen hallinta \> Ostohyvityksen hallintasopimukset \> Ostohyvityksen työtila**.
1. Määritä **Näytä**-kentän arvoksi _Kaikki_ tai _Kirjattu_.
1. Etsi ja valitse tarkastettava rivi. Valitse sitten toimintoruudun **Ostohyvityksen työtila**-välilehden **Näytä**-ryhmässä **Kohdetapahtumat**. Tämä painike on käytettävissä vain, jos valitulle riville on tehty kirjauksia.
1. Näyttöön tulee luettelo kirjauskansioista, asiakirjoista tai nimikkeistä. Jos haluat lisätietoja kirjauskansiosta, asiakirjasta tai nimikkeestä, valitse sen rivi ja valitse sitten toimintoruudusta **Näytä tiedot**.

## <a name="rebate-management-transactions-on-the-deduction-workbench"></a>Ostohyvityksen työtilan ostohyvitysten hallintatapahtumat

Kun kirjaat ostohyvityksen hallintatapahtuman, jolla on jokin seuraavista **maksutyypin** arvoista, järjestelmä luo asiakkaan vähennyskirjauskansion tai vapaatekstilaskun asianmukainen asiakastilille:

- Asiakkaan vähennykset
- Verota laskujen asiakasvähennyksiä
- Kaupankäynnin kulut
- Raportointi

Kun kohdetapahtuma on luotu ja kirjattu, se on käytettävissä avoimena tapahtumana **Vähennyksen työtila** -sivulla (**Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennyksen työtila**). Avointen tapahtumien **Vaatimustyypin** arvona on *Ostohyvitysten hallinta* ja **ostohyvitystapahtuman numeron** arvo on käytettävissä jäljitettävyyden mahdollistamiseksi. Päivämääräksi määritetään ostohyvityksen hallinnan kohdetapahtuman kirjauspäivämäärä. Jos haluat selvittää saman asiakastilin olemassa olevien vähennysten avoimet tapahtumat vähennyksen avulla, valitse toimintoruudusta **Ylläpidä \> Täsmäytys**.

Lisätietoja on kohdassa [Vähennysten hallinta vähennysten työtilaa käyttämällä](deduction-workbench.md).

## <a name="purge-unposted-transactions"></a>Kirjaamattomien tapahtumien tyhjentäminen

Kun olet käsitellyt varaus-, ostohyvitys- tai alennustapahtumia, voit poistaa valitut kirjaamattomat tapahtumat näiden vaiheiden mukaisesti.

1. Siirry kohtaan **Ostohyvityksen hallinta \> Ostohyvityksen hallintasopimukset \> Ostohyvityksen työtila**.
2. Määritä **Näytä**-kentän arvoksi *Ei kirjattu*.
3. Etsi ja valitse poistettavat tapahtumat. Valitse sitten toimintoruudun **Ostohyvityksen työtila**-välilehden **Käsitellään**-ryhmässä **Tyhjennä**.
4. Poista kirjaamattomat tapahtumat napsauttamalla **OK**.

## <a name="cancel-a-posted-provision"></a>Kirjatun varauksen peruuttaminen

Kun olet käsitellyt ja kirjaanut varauksen, voit peruuttaa kirjatut varaustapahtumat noudattamalla näitä vaiheita.

1. Siirry kohtaan **Ostohyvityksen hallinta \> Ostohyvityksen hallintasopimukset \> Ostohyvityksen työtila**.
2. Määritä **Näytä**-kentän arvoksi *Kirjattu*.
3. Etsi ja valitse peruuttaaksesi valmistele tapahtumat. Valitse sitten toimintoruudun **Ostohyvityksen työtila**-välilehden **Käsitellään**-ryhmässä **Peruuta valmistelu**.
4. Peruuta tapahtumat valitsemalla **OK**.

Nämä varausten peruutukset näkyvät myös asiaan liittyvien [Ostohyvitysten hallinnan kirjauskansioissa](#review-journals).
