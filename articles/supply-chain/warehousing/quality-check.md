---
title: Laaduntarkistus
description: Tässä artikkelissa on tietoja laaduntarkistusominaisuudesta. Tämän ominaisuuden avulla varaston työntekijät voivat tehdä nopeita laaduntarkistuksia samalla, kun nimikkeitä vastaanotetaan laiturialueelle.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ceb01205edc269690fda306bc90f465dbccc563b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855054"
---
# <a name="quality-check"></a>Laaduntarkistus

[!include [banner](../includes/banner.md)]

*Laaduntarkistusominaisuuden* avulla varaston työntekijät voivat tehdä nopeita laaduntarkistuksia samalla, kun nimikkeitä vastaanotetaan laiturialueelle. Nämä nopeat tarkistukset ovat hyödyllisiä silloin, kun työntekijät tarkastavat pakkauksia tai nimikkeen muuten helposti tunnistettavissa olevia osia. Ominaisuuden avulla työntekijät voivat katsoa nopeasti, onko jokin selvästi viallinen tai vioittunut, ennen kuin he varastoivat nimikkeet hyllytyssijaintiin.

Tämä ominaisuus on vakiolaaduntarkastusprosessin vaihtoehto. Se on aiempaa joustavampi ja nopeampi.

Jos tämä ominaisuus on käytössä, saapumis- ja laaduntarkistus tapahtuvat seuraavasti:

1. Kun lähetys saapuu, varastotyöntekijä rekisteröi saapumisen. Työntekijä myös skannaa rekisterikilven ja rekisteröi sijainnin.
1. Työntekijä tekee nopean laaduntarkistuksen ja tallentaa rekisterikilven tuloksen (hyväksytty tai hylätty).
1. Yksi seuraavista toiminnoista tapahtuu:

    - Jos laaduntarkistus on hyväksytty, rekisterikilpi hyväksytään ja saatetaan vastaanottosijaintiin tavalliseen tapaan.
    - Jos laaduntarkistus epäonnistuu, rekisterikilpi hylätään ja sen olemassa oleva hyllytystyö ohjataan uudelleen vaihtoehtoiseen sijaintiin lisätarkastusta varten. Uusi laatutilaus luodaan. Jos haluat tarkastella laatutilausta, joka on luotu epäonnistuneesta laaduntarkistuksesta, siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.

Tämä prosessi voidaan määrittää myös siten, että kaikki skannatut rekisterikilvet ohjataan välittömästi laaduntarkistussijaintiin.

## <a name="turn-the-quality-check-feature-on-or-off"></a>Laaduntarkistusominaisuuden ottaminen käyttöön tai käytöstä poistaminen

Tässä artikkelissa kuvatun toiminnon käyttäminen edellyttää, että *Laaduntarkistus* -toiminto on käytössä järjestelmässäsi. Supply Chain Managementin versiosta 10.0.25 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.25, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Laaduntarkistus* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

## <a name="set-up-the-feature-for-the-example-scenario"></a>Määritä ominaisuus tälle esimerkkiskenaariolle

Tässä ohjeaiheessa on ohjeita ja esimerkki, jossa kerrotaan *laaduntarkistustoiminnon* määrityksestä ja tässä artikkelissa myöhemmin olevan esimerkkiskenaarion näytetietojen valmistelemisesta.

### <a name="make-sample-data-available"></a>Ota mallitiedot käyttöön

[Esimerkkiskenaarion](#example-scenario) käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon [vakiodemotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

### <a name="quality-check-template"></a><a name="quality-template"></a>Laaduntarkistusmalli

Laaduntarkistusmalli määrittää laadun nopeiden tarkistusten säännöt vastaanoton yhteydessä.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Laaduntarkistusmallit**.
1. Valitse **Uusi** lisätäksesi mallin ruudukkoon.
1. Määritä uusi malli määrittämällä seuraavat arvot:

    - **Laaduntarkistusmallin nimi:** *Laituritarkistus*

        Kirjoita nimi, joka määrittää tässä mallissa käytetyt käytännöt.

    - **Hyväksymiskäytäntö:** *Kehote käyttäjälle*

        Määritä, pyydetäänkö käyttäjiä hyväksymään tai hylkäämään varaston laatu työn käsittely yhteydessä vai hylätäänkö laatu automaattisesti. Käytettävissä olevat vaihtoehdot ovat *Automaattinen hylkääminen* ja *Kehote käyttäjälle*.

    - **Laadun käsittelykäytäntö:** *Luo laatutilaus*

        Valitse käytäntö, jota käytetään varaston laadun hylkäyksen yhteydessä. Käytettävissä ovat seuraavat asetukset:

        - *Luo vain työ* – Luo vain työ varastosiirtoja varten.
        - *Luo laatutilaus* – Luo laatutilaus laatutestejä varten.

    - **Testiryhmä:** *Kehys*

        Määritä testiryhmä, jota käytetään luotavassa laatutilauksessa. Testiryhmät määritetään **Varastonhallinta**-moduulissa.

        Ota testiryhmän **Destruktiivinen teksti** -vaihtoehto pois käytöstä. Tämä vaihtoehto määrittää, tuhotaanko näytteet osana testiryhmän testejä. Jos käytetään destruktiivista testiä, järjestelmä luo varastotapahtuman, kun laatutilaus luodaan nimikkeelle. Uusi varastotapahtuma ennustaa testimäärän aiheuttaman varastovähennyksen. Varastonvähennys tapahtuu, kun laatutilaus viimeistellään vahvistusvaiheessa. Varastotapahtuma määritetään laatutilaukseksi.

### <a name="work-class--quality-check"></a><a name="work-class"></a>Työluokka – laaduntarkistus

Työluokilla ohjataan ja/tai rajoitetaan työtilausrivityyppejä, joita varastotyötekijät voivat käsitellä mobiililaitteessa.

1. Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.
1. Luo työluokka valitsemalla **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Työluokan tunnus:** *QC-tarkistus*

        Anna työluokalle nimi.

    - **Kuvaus:** *QC-tarkistus*

        Anna lyhyt kuvaus, joka osoittaa käytettävän työluokan.

    - **Työtilauksen tyyppi:** *Laaduntarkistuksen laatu*

        Valitse työluokan luoma työtilaustyyppi. Kun määrität laadunvalvontatyön, valitse aina *Laaduntarkistuksen laatu*.

1. Jätä **Sallitut hyllytyssijainnit** -pikavälilehden **Sijaintityyppi**-kenttä tyhjäksi.

    Jos valitset sijaintityypin, rajoitat niitä sijainteja, joissa nimikkeet voidaan hyllyttää keräilyn jälkeen. Tätä kenttää käytetään, kun sijaintidirektiivi yrittää ratkaista sijainnin tai jos varastotyöntekijä määrittää manuaalisesti sijainnin mobiililaitteen valikkosijainnin valikon vaihtoehdossa.

Lisätietoja työluokista ja niiden luomisesta on kohdassa [Työluokan luominen](tasks/create-work-class.md).

### <a name="work-template"></a>Työmalli

Työmallen avulla voit määrittää työtoiminnot, jotka on suoritettava varastossa. Yleensä varastotyötoiminnot kostuvat toimintopareista: varaston työntekijä keräilee käsillä olevan varaston yhdessä sijainnissa ja asettaa sitten keräillyt varastotuotteet toiseen paikkaan. Laadunvalvonnan työmalli määrittää laaduntarkistusten työtoiminnot.

#### <a name="purchase-orders"></a>Ostotilaukset

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Määritä otsikossa **Työtilaustyyppi**-kentän arvoksi *Ostotilaukset*.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse työmalli, jonka tulee sisältää laaduntarkistusvaihe. Valitse **Yleiskatsaus**-osan **Työmalli**-kentässä *51 - ostotilauksen vastaanotto*.
1. Huomaa, että **Työmallin tiedot** -osan ruudukossa on kaksi riviä. Toinen rivi on *keräilyä* ja toinen *hyllytystä* varten.
1. Valitse **Työmallin tiedot** -osassa **Uusi**, jos haluat lisätä ruudukkoon laadunvalvonnan rivin. Huomaa, että uuden rivin **Rivinumero**-kentän arvoksi on määritetty *3*.
1. Määritä uudelle riville seuraavat arvot. Hyväksy jäljellä olevien kenttien oletusarvot.

    - **Työtyyppi:** *Laaduntarkistus*
    - **Työluokan tunnus:** *Osto*
    - **Laaduntarkistusmallin nimi:** *Laituritarkistus*

        Valitse työluokan yksilöivä tunniste. Voit käyttää tätä arvoa mobiililaitteen valikkokohteiden määrittämiseen ja sen tyyppiseen työhön, jota valikkokohteet voivat käsitellä.

1. Valitse toimintoruudussa **Tallenna**, jos haluat tallentaa tähänastisen työn.

    Näyttöön tulee seuraava sanoma: "Virheellinen - Laaduntarkistus on tehtävä heti keräilyn jälkeen." Tämän vuoksi juuri lisätyn rivin **Rivinumero**-arvo on muutettava.

1. Muuta uuden rivin **Rivinumero**-arvoa seuraavasti:

    1. Valitse **Työmallin tiedot** -osassa rivi, jonka **Työtyyppi**-kentän arvoksi on määritetty *Laaduntarkistus*.
    2. Valitse **Siirry ylös**- tai **Siirry alas** -painike, jos haluat siirtää *Laaduntarkistus*-riviä niin, että se on *Keräily*-rivin jälkeen.

1. Valitse toimintoruudussa **Tallenna**.

#### <a name="quality-in-quality-check"></a>Laatu laaduntarkistuksessa

Luo seuraavaksi työmalli laaduntarkistukselle.

1. Muuta **Työmallit**-sivulla **Työtilaustyyppi**-kentän arvoksi *Laaduntarkistuksen laatu*.
1. Lisää **Yleiskatsaus**-osan ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Aseta uudelle riville seuraavat arvot:

    - **Työmalli:** *51 - laaduntarkistus*

        Anna mallille nimi.

    - **Työmallin kuvaus:** *51 - laaduntarkistus*

1. Valitse toimintoruudussa **Tallenna**, jos haluat, että **Työmallin tiedot** -osa on käytettävissä.
1. Kun uusi malli on vielä valittuna **Yleiskatsaus**-osassa, valitse **Uusi** **Työmallin tiedot** -osassa ja lisää ruudukkoon rivi.
1. Aseta uudelle riville seuraavat arvot:

    - **Työtyyppi:** *Poiminta*
    - **Työluokan tunnus:** *QC-tarkistus*

        Valitse aiemmin laadunvalvontatyölle luodun [työluokan](#work-class) nimi.

1. Valitse **Työmallin tiedot** -osassa uudelleen **Uusi** ja lisää toinen rivi.
1. Aseta uudelle riville seuraavat arvot:

    - **Työtyyppi:** *Aseta*
    - **Työluokan tunnus:** *QC-tarkistus*

        Valitse aiemmin laadunvalvontatyölle luodun [työluokan](#work-class) nimi.

1. Valitse toimintoruudussa **Tallenna**.

Katso lisätietoja työmalleista artikkelista [Varastotyön hallinta työmallien ja sijaintidirektiivien avulla](control-warehouse-location-directives.md).

### <a name="location-directive--quality-failures"></a>Sijaintidirektiivi – laadun virheet

Sijaintidirektiivit ovat sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa. Esimerkiksi myyntitilaustapahtumassa sijaintidirektiivi määrittää, mistä nimikkeet kerätään, ja minne kerätyt nimikkeet sijoitetaan. Sinun on määritettävä sijaintidirektiivin sääntö, jotta voit määrittää, miten epäonnistuneita laaduntarkistuksia käsitellään.

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Määritä vasemmanpuoleisessa ruudussa **Työtilaustyyppi**-kentän arvoksi *Ostotilaukset*, jos haluat käsitellä tämäntyyppisiä direktiivejä.
1. Luo laaduntarkistusten sijaintidirektiivi valitsemalla toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Järjestysnumero:** Hyväksy oletusarvo.
    - **Nimi:** *51 - kohdelaatu*

1. Määritä **Sijaintidirektiivit**-pikavälilehdessä seuraavat arvot. Hyväksy jäljellä olevien kenttien oletusarvot.

    - **Työtyyppi:** *Aseta*
    - **Toimipaikka:** *5*
    - **Varasto**: *51*

1. Valitse toimintoruudussa **Tallenna**, jos haluat tallentaa direktiivin ja määrittää **Rivit**-pikavälilehden käytettäväksi.
1. Lisää uusi rivi ruudukkoon **Rivit**-pikavälilehdessä **Uusi**.
1. Määritä uudelle riville seuraavat arvot. Hyväksy jäljellä olevien kenttien oletusarvot.

    - **Määrästä:** *1*
    - **Määrälle:** *1000000*

1. Valitse toimintoruudussa **Tallenna**, jos haluat tallentaa uuden rivin ja määrittää **Sijaintidirektiivin toiminnot** -pikavälilehden käytettäväksi.
1. Kun uusi rivi on yhä valittuna **Rivit**-pikavälilehdessä, valitse **Uusi** **Sijaintidirektiivin toiminnot** -pikavälilehdessä ja lisää siellä ruudukkoon uusi rivi. Tämän jälkeen voit määrittää riville toiminnon.
1. Määritä uuden rivin **Nimi**-kentän arvoksi *Laatu*. Hyväksy jäljellä olevien kenttien oletusarvot.
1. Valitse toimintoruudussa **Tallenna**, jos haluat, että **Sijaintidirektiivin toiminnot** -pikavälilehden **Muokkaa kyselyä** -painike on käytettävissä.
1. Kun juuri lisäämäsi rivi on yhä valittuna **Sijaintidirektiivin toiminnot** -pikavälilehdessä, valitse **Muokkaa kyselyä** ja avaa valintaruutu, jossa voit muokata toiminnon kyselyä.
1. Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin kyselyyn.
1. Aseta uudelle riville seuraavat arvot:

    - **Taulu:** *Sijainnit*
    - **Johdettu taulu:** *Sijainnit*
    - **Kenttä:** *Sijainti*
    - **Kriteerit:** *QMS*

    *QMS*-sijainti on laadun varastosijainti.

1. Sulje valintaikkuna valitsemalla **OK**.
1. Nyt sinun on muutettava ostotilauksen sijaintidirektiivien järjestystä varastolle *51*. Tallenna uusi *51 - kohdelaatu* -sijaintidirektiivi, päivitä sivu ja valitse sijaintidirektiivi luettelosta. Käytä sitten toimintoruudun **Siirrä ylös**- ja **Siirrä alas** -painikkeita, jos haluat sijoittaa sijaintidirektiivin varastoon *51* alla mainitussa järjestyksessä. (Ennen kuin valitset **Siirrä ylös**- tai **Siirrä alas** -painikkeen, valitse sijaintidirektiivi luettelosta.)

    1. 51 - kohdelaatu
    2. 51 - ostotilaus, suora
    3. 51 QMS

### <a name="mobile-device-menu-items"></a>Mobiililaitteen valikkovaihtoehdot

Määritä valikkonimike niin, että mobiililaitteet voivat suorittaa **Laaduntarkistus**-toiminnon.

#### <a name="purchase-putaway"></a>Oston hyllytys

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse luettelosta e **Oston hyllytys** -mobiililaitevalikkovaihtoehto.
1. Valitse toimintoruudussa **Muokkaa**.
1. Lisää uusi rivi ruudukkoon **Työluokat**-osassa valitsemalla **Uusi**.
1. Aseta uudelle riville seuraavat arvot:

    - **Työluokan tunnus:** *QC-tarkistus*

        Anna aiemmin laadunvalvontatyölle luodun [työluokan](#work-class) nimi.

    - **Työtilauksen tyyppi:** *Laaduntarkistuksen laatu*

1. Valitse toimintoruudussa **Tallenna**.

#### <a name="purchase-order-line-receiving"></a>Ostotilausrivin vastaanotto

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Valikkokohteen nimi:** *Ostotilausrivien vastaanotto*
    - **Otsikko:** *Ostotilausrivien vastaanotto*
    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Ei*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot. Hyväksy jäljellä olevien kenttien oletusarvot.

    - **Työn luomisprosessi:** *Ostotilausrivien vastaanotto ja hyllytys*
    - **Luo rekisterikilpi:** *Kyllä*
    - **Työmalli:** *51 - ostotilauksen vastaanotto*

1. Valitse toimintoruudussa **Tallenna**.

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Lisää valikkovaihtoehto mobiililaitteen valikkoon

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse vasemmanpuoleisessa ruudussa **Saapuvat**-valikko.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse **Käytettävissä olevat valikot ja valikon vaihtoehdot** -sarakkeessa uusi **Ostotilausrivien vastaanotto** -valikon vaihtoehto.
1. Siirrä **Ostotilausrivin vastaanotto** oikealla nuolipainikkeella **Valikon rakenne** -sarakkeeseen.
1. Valitse **Valikon rakenne** -sarakkeessa **Ostotilausrivien vastaanotto** ja valitse sitten ylös- tai alasnuolipainike ja siirrä valikon vaihtoehto haluttuun kohtaan mobiililaitteen valikossa.
1. Valitse toimintoruudussa **Tallenna**.

## <a name="example-scenario"></a><a name="example-scenario"></a>Esimerkkiskenaario

Kun olet tehnyt kaikki edellä mainitut näytetiedot käytettäviksi ja määrittänyt ne, voit käyttää tätä skenaariota ja kokeilla *Laaduntarkistus*-toimintoa. Tämän skenaarion arvoissa oletetaan, että käsittelet vakionäytetietoja, valittuna on **USMF**-yritys ja että aiemmin tässä artikkelissa kuvatut näytetietueet on valmisteltu. Tämä skenaario on myös esimerkki siitä, miten ominaisuutta voidaan käyttää tuotannon määrityksessä.

### <a name="create-a-purchase-order"></a>Ostotilauksen luominen

1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:

    - **Toimittajan tili:** *104*
    - **Varasto**: *51*

1. Valitse **OK**, jos haluat sulkea valintaikkunan ja avata uuden ostotilauksen.
1. **Ostotilausrivit**-pikavälilehden ruudukko sisältää uuden, tyhjän rivin. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** *M9203*
    - **Määrä** *3*
    - **Yksikkö:** *PL*

1. Valitse toimintoruudussa **Tallenna**.

### <a name="process-quality-check-receiving"></a>Käsittele vastaanoton laaduntarkistus

Kun ostotilaus on luotu, se voidaan vastaanottaa käyttämällä **Ostotilausrivin vastaanotto** -valikon vaihtoehtoa ja *Laaduntarkistus*-ominaisuuden toimintoja.

#### <a name="receive-pallet-1"></a>Vastaanota kuormalava 1

1. Kirjaudu varastonhallinnan mobiilisovellukseen käyttäjänä varastolle *51*. (Anna käyttäjätunnukseksi *51* ja salasanaksi *1*.)
1. Siirry kohtaan **Saapuvat \> Ostotilausrivin vastaanotto**.
1. Syötä **PONUM**-kenttään ostotilauksen numero.
1. Vahvista ostotilausnumero.
1. Anna **LINENUM**-kenttään vastaanotettavan ostotilausrivin numero. Koska tilauksella on tässä skenaariossa vain yksi rivi, anna **LINENUM**-kenttään arvo *1* jokaisessa vastaanottovaiheessa.
1. Vahvista rivinumero.
1. Syötä vastaanottomäärä **MÄÄRÄ**-kenttään. Koska ostotilaus koskee kolmea kuormalavaa (*PL*) tässä skenaariossa ja vastaanottovaiheita on kolme, jokaisessa vastaanottovaiheessa annetaan **MÄÄRÄ**-kentän arvoksi *1*.
1. Vahvista määrä.

    Näkyviin tulevalla **Laaduntarkistus**-sivulla ei ole syöttökenttiä. Se sisältää vain vahvistuksen (valintamerkin) painikkeen sivun alaosassa ja valikkopainikkeen (**≡**) sivun yläosassa. (Valikkopainiketta kutsutaan joskus neljän viivan painikkeeksi tai hampurilaispainikkeeksi.) Laaduntarkistusprosessin nopeuttamiseksi käyttäjä voi vahvistaa **Laaduntarkistus**-sivun kuormalavan läpäistyä laaduntarkistuksen.

    ![Laaduntarkistus-sivu.](media/quality-check.png "Laaduntarkistus-sivu")

1. Valitse vahvistuspainike, jos haluat hyväksyä rivin 1 kuormalavan 1 laaduntarkistuksen.

    Näkyviin tulevalla **Ostotilaukset: Hyllytys** -sivulla ovat seuraavat hyllytystyön tiedot:

    - **SIJAINTI:** Järjestelmän määrittämä sijainti

        Tämä sijainti on ostotilauksen vastaanotolle määritetty hyllytyssijainti.

    - **RK:** Järjestelmän luoma rekisterikilpitunnus
    - **Nimike:** *M9203*
    - **Määrä:** *1 KL: 100 kpl*

    Nimikkeen kuvaus näytetään myös.

1. Vahvista hyllytystyö.

    Ostotilausrivin vastaanoton **Tehtävä**-sivulla on Työ valmis -sanoma. **LINENUM**-kenttä on käytettävissä, joten voit aloittaa seuraavan kuormalavan vastaanoton.

#### <a name="receive-pallet-2"></a>Vastaanota kuormalava 2

Tässä skenaariossa kuormalava 2 hylätään.

1. Anna **LINENUM**-kenttään *1* ja vahvista rivinumero.
1. **MÄÄRÄ**-kenttä on nyt käytettävissä. Anna arvo *1* ja vahvista määrä.

    **Laaduntarkistus**-sivu tulee näkyviin. Tässä vastaanotossa kuormalava hylätään laadun osalta. Kuormalava asetetaan *QMS*-laatusijaintiin.

1. Valitse valikkopainike (**≡**) sivun yläosassa ja valitse sitten valikosta **Hylkää**.
1. Anna näkyviin tulevalla **Tehtävä**-sivulla **QMS** *hyllytyssijainniksi* ja lähetä kuormalava lisätarkastukseen.

    Näkyviin tulevalla **Laaduntarkistuksen laatu: Hyllytys** -sivulla ovat seuraavat hyllytystyön tiedot:

    - **SIJAINTI:** *QMS*

        Tämä sijainti on hylätyn laadun vastaanotolle määritetty hyllytyssijainti.

    - **RK:** Järjestelmän luoma rekisterikilpitunnus
    - **Nimike:** *M9203*
    - **Määrä:** *1 KL: 100 kpl*

    Nimikkeen kuvaus näytetään myös.

1. Vahvista hyllytystyö.

    Ostotilausrivin vastaanoton **Tehtävä**-sivulla on Työ valmis -sanoma. **LINENUM**-kenttä on käytettävissä, joten voit aloittaa seuraavan kuormalavan vastaanoton.

Olet nyt tehnyt laatutarkistuksen ja luonut hylätyn kuormalavan laatutilauksen. Jos haluat tarkastella luotua laatutilausta, siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.

Laatutilauksen testausta voidaan nyt käsitellä. Tässä artikkelissa ei käsitellä laatutestausta.

Lisätietoja laadunhallinnasta on kohdassa [Laadunhallinnan yleiskuvaus](../inventory/enable-quality-management.md)

#### <a name="receive-pallet-3"></a>Vastaanota kuormalava 3

Tässä skenaariossa kuormalava 3 hyväksytään.

1. Anna **LINENUM**-kenttään *1* ja vahvista rivinumero.
1. **MÄÄRÄ**-kenttä on nyt käytettävissä. Anna arvo *1* ja vahvista määrä.

    **Laaduntarkistus**-sivu tulee näkyviin. Tässä vastaanotossa kuormalava hyväksytään laadun osalta. Kuormalava asetetaan joukkohyllytyssijaintiin.

1. Valitse vahvistuspainike, jos haluat hyväksyä laaduntarkistuksen.

    Näkyviin tulevalla **Ostotilaukset: Hyllytys** -sivulla ovat seuraavat hyllytystyön tiedot:

    - **SIJAINTI:** Järjestelmän määrittämä sijainti

        Tämä sijainti on ostotilauksen vastaanotolle määritetty hyllytyssijainti.

    - **RK:** Järjestelmän luoma rekisterikilpitunnus
    - **Nimike:** *M9203*
    - **Määrä:** *1 KL: 100 kpl*

    Nimikkeen kuvaus näytetään myös.

1. Vahvista hyllytystyö.

    Ostotilausrivin vastaanoton **Tehtävä**-sivulla on Työ valmis -sanoma. **LINENUM**-kenttä on käytettävissä, joten voit aloittaa seuraavan kuormalavan vastaanoton.

1. Valitse valikkopainike (**≡**) sivun yläosassa ja valitse sitten valikosta **Peruuta**, jos haluat palata valikkoon.

Voit nyt sulkea mobiilisovelluksen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]