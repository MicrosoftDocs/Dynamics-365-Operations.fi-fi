---
title: RCS:n ja ER:n sovelluskohtaisten metatietojen valmisteleminen
description: Tässä ohjeaiheessa käsitellään Regulatory Configuration Servicen (RCS) ja sähköisen raportoinnin (ER) sovelluskohtaisten metatietojen valmistelua.
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f15b78d3ed5b4df47540f9f89cc69c0b535a7241
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680191"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a>RCS:n ja ER:n sovelluskohtaisten metatietojen valmisteleminen

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa on käytännön esimerkkejä seuraavista tehtävistä:

- [RSC:ssä käytettävien sovelluksen metatietojen valmisteleminen](#prepare-application-metadata-that-can-be-used-in-rcs)
- [Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla](#access-application-metadata-by-using-an-er-configuration)
- [Sovelluksen metatietojen käyttäminen yhdistetyillä sovelluksilla](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>RSC:ssä käytettävien sovelluksen metatietojen valmisteleminen

Seuraavassa menettelyssä osoitetaan, miten käyttäjä, jolla on **Järjestelmänvalvoja**- tai **Sähköisen raportoinnin kehittäjä** -rooli, voi luoda sähköisen raportoinnin ER-konfiguraation, jossa on sovelluksen metatietoja ja jolla suunnitellaan ER-mallin yhdistämismääritykset Regulatory Configuration Servicessä (RCS). Tässä esimerkissä luodulla ER-näytemallin yhdistämismäärityksellä voidaan käyttää ulkomaankauppatapahtumia.

Tässä merkissä käytetään RCS:ää suunnittelemaan sellainen sovelluksen ER-ratkaisu, jolla luodaan ulkomaankaupan liiketoimintatoimialueen tietoja sisältäviä sähköisiä asiakirjoja. Jos haluat määrittää ER-tietomallin ja tarvittavien tietojen lähteiden välisen määrityksen, sinulla on oltava sovelluksen metatietojen käyttöoikeus RCS:ssä. Tämän vuoksi ER-ratkaisun suunnittelun osana on määritettävä uusi ER-metatietokonfiguraatio, joka sisältää kaikki valitun liiketoimintatoimialueen ER-raporttien luontiin tällä hetkellä tarvittavat metatiedot.

> [!NOTE]
> Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

1. Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.
2. Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**. Jos konfiguraation lähde ei ole näkyvissä, suorita menettely [Konfiguraation lähteiden luominen ja niiden merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Valitse **Metatietojen konfiguraatiot**.
4. Valitse **Luo konfiguraatio**.
5. Anna avattavan luettelon **Nimi**-kentässä nimi. Kirjoita tässä esimerkissä **Ulkomaankaupan metatiedot**.
6. Valitse **Luo konfiguraatio**.
7. Valitse **Suunnittelu**.
8. Valitse **Lisää**.

    > [!NOTE]
    > Voit valita joko koko sovelluksen tai valittujen mallien tai moduulien kaikki metatiedot. Muista kummassakin tapauksessa, että seuraavat metatiedot lisätään automaattisesti: tietue-, luettelo- ja laajennetut tietotyyppi (EDT) -taulut. Jos muita metatietoja tarvitaan, ne on lisättävä manuaalisesti.

    Ulkomaankauppatapahtumiin liittyvät metatiedot on lisättävä ja metatietonimikkeen on valittava manuaalisesti.

9. Valitse **Lisää tietolähde \> Taulukkotietueet**.
10. Suodata **Nimi**-kentän **Intrastat**-arvon mukaan.
11. Valitse **Intrastat**-taulukkotietue.
12. Valitse **OK**.

    Intrastat-taulukkotietueen metatiedot on lisättävä.

13. Valitse puussa **Taulukkotietueet Intrastat \> \>Suhteet\> IntrastatCommodity (Taulukkotietueet EcoResCategory)**.
14. Valitse **Lisää metatiedot**.

    > [!NOTE]
    > Valitun taulukkotietueen pakollisten suhteiden metatiedot on lisättävä manuaalisesti.

15. Valitse **Lisää tietolähde**.
16. Valitse **Luettelointi**.
17. Suodata **Nimi**-kentän **IntrastatDirection**-arvon mukaan.
18. Valitse **IntrastatDirection**-luettelointitietue.
19. Valitse **OK**.
20. Valitse **Tallenna**.
21. Sulje sivu.
22. Viimeistele metatietokonfiguraation luonnosversio:

    1. Valitse **Muutoksen tila \> Viimeistele**.
    2. Valitse **OK**.
    3. Valitse valmis versio 1.

23. Vie metatietokonfiguraation valmis versio sovelluksesta XML-tiedostona:

    1. Valitse **Vaihto \> Vie XML-tiedostona**.
    2. Valitse **OK**.

Luotu ER-metatietokonfiguraatio tallennetaan **Ulkomaankaupan metatiedot.xml** -tiedostona. Voit nyt tuoda sen RCS:ään käytettäväksi ulkomaankaupan liiketoimintatoimialueen metatietolähteenä. Voit määrittää näiden tietojen perusteella sovelluksen metatietojen ja ER-tietomallin välisen yhdistämismäärityksen.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla

Seuraava menettely näyttää, miten RCS-käyttäjä, jolla on **Järjestelmänvalvoja**- tai **Sähköisen raportoinnin kehittäjä** -rooli, voi suunnitella uuden ER-mallin yhdistämismäärityksen käyttämällä sovelluksen metatietoja. Sovelluksen metatietoja käytetään ER-metatietokonfiguraatiolla, joka sisältää ulkomaankauppatapahtumien käyttöön tarkoitetun metatietojen näytejoukon.

Ennen kuin suoritat tämän menettelyn, seuraava menettely on viimeisteltävä ensin.

- [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [RSC:ssä käytettävien sovelluksen metatietojen valmisteleminen](#prepare-application-metadata-that-can-be-used-in-rcs)

1. Valitse **Kaikki työtilat \> Sähköinen raportointi**.
2. Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**. Jos konfiguraation lähde ei ole näkyvissä, suorita menettely [Konfiguraation lähteiden luominen ja niiden merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Tuo metatiedot sisältävä sovelluksen ER-metatietokonfiguraatio, joka on määritetty luomaan sähköisiä ulkomaankaupan liiketoimintatoimialueen asiakirjoja. Loit tämän ER-metatietokonfiguraation ja veit sen XML-tiedostona [RSC:ssä käytettävien sovelluksen metatietojen valmisteleminen](#prepare-application-metadata-that-can-be-used-in-rcs) -menettelynä aiemmin tässä ohjeaiheessa.

    1. Valitse **Metatietojen konfiguraatiot**.
    2. Valitse **Vaihto**.
    3. Valitse **Lataa XML-tiedostosta**.
    4. Selaa **Ulkomaankaupan metatiedot.xml** -tiedostoon ja valitse se.
    5. Valitse **OK**.
    6. Sulje sivu.

4. Luo tietomallin konfiguraatio:

    1. Valitse **Raportointikonfiguraatiot**.
    2. Valitse **Luo konfiguraatio**.
    3. Kirjoita avattavan luettelon **Nimi**-kenttään **Ulkomaankauppamalli**.
    4. Valitse **Luo konfiguraatio**.
    5. Valitse **Suunnittelu**.
    6. Avaa valintaikkuna valitsemalla **Uusi**.

        1. Kirjoita **Nimi**-kenttään **Juuri**.
        2. Valitse **Lisää**.
    
    7. Avaa valintaikkuna valitsemalla **Uusi**.

        1. Kirjoita **Nimi**-kenttään **Tapahtuma**.
        2. Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.
        3. Valitse **Lisää**.
 
    8. Avaa valintaikkuna valitsemalla **Uusi**.

        1. Kirjoita **Nimi**-kenttään **Kauppatavarakoodi**.
        2. Valitse **Nimiketyyppi**-kentässä **Merkkijono**.
        3. Valitse **Lisää**.

    9. Avaa valintaikkuna valitsemalla **Uusi**.

        1. Kirjoita Nimi-kenttään **Laskutettu summa**.
        2. Valitse **Nimiketyyppi**-kentässä **Reaaliluku**.
        3. Valitse **Lisää**.

    10. Avaa valintaikkuna valitsemalla **Uusi**.

        1. Kirjoita **Nimi**-kenttään **Päivämäärä**.
        2. Valitse **Nimiketyyppi**-kentässä **Päivämäärä**.
        3. Valitse **Lisää**.
 
    11. Valitse **Lisää \> Juuriviite**.
    12. Valitse **OK**.
    13. Valitse **Tallenna**.
    14. Sulje sivu.
    15. Valitse **Muutoksen tila \> Viimeistele**.
    16. Valitse **OK**.

5. Luo mallin yhdistämismääritys:

    1. Valitse **Luo konfiguraatio**.
    2. Kirjoita avattavan luettelon **Nimi**-kenttään **Mallin yhdistämismääritys perustuu tietomallin ulkomaankauppamalliin**.
    3. Kirjoita **Nimi**-kenttään **Ulkomaankaupan yhdistäminen**.
    4. Valitse **Luo konfiguraatio**.
    5. Valitse **Edellytykset**-pikavälilehdessä **Muokkaa**.
    6. Valitse **Uusi**.
    7. Valitse **Edellytysosan tyyppi** -kentässä **Konfigurointi**.
    8. Valitse **Ulkomaankaupan metatiedot** -määritys.
    9. Valitse **Tallenna**. Huomautus viitteen lisäämisestä **Ulkomaankaupan metatiedot** -määrityksen versioon 1. Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan.
    10. Sulje sivu.
    11. Valitse **Suunnittelu**.
    12. Valitse **Suunnittelu**.
    13. Valitse puussa **Dynamics 365 for Operations \> Taulukkotietueet**.
    14. Valitse **Lisää pääkansio**.
    15. Kirjoita **Nimi**-kenttään **Intrastat**.
    16. Valitse **Intrastat**-taulukkotietueet.
    17. Valitse **OK**.

        > [!NOTE]
        > Valittavana on vain kaksi taulukkoa, sillä tällä hetkellä käytössä olevaan metatietosarjaan lisättiin vain kaksi taulukkoa.

    18. Valitse **Sido**.
    19. Valitse puussa **Intrastat \> AmountMST**.
    20. Valitse puussa **Tapahtuma = Intrastat \> Laskutettu summa**.
    21. Valitse **Sido**.
    22. Valitse puussa **Intrastat \> TransDate**.
    23. Valitse puussa **Tapahtuma = Intrastat \> Date**.
    24. Valitse **Sido**.
    25. Valitse puussa **Intrastat \> \>Suhteet \> IntrastatCommodity \> Koodi**.
    26. Valitse puussa **Tapahtuma = Intrastat \> Kauppatavarakoodi**.
    27. Valitse **Sido**.
    28. Valitse **Tarkista**.

        > [!NOTE]
        > Kun tarkistus on valmis, tietomallin elementtien ja kuvattujen nimikkeiden tietolähteiden sitominen onnistui käyttämällä sovelluksen tietoja viitatuista ER-metatietokonfiguraatiosta.

    29. Valitse **Tallenna**.

Voit tarvittaessa laajentaa aiemmin luotua metatietojoukkoa sovelluksen kanssa. Voit sitten viedä uuden täydellisen ER-metatietokonfiguraation version, tuoda sen RCS:een ja päivittää tuodun metatietokonfiguraation uuteen versioon viittaavan määritetyn mallin yhdistämiskonfiguraation edellytykset.

> [!NOTE]
> Tietojen hankkiminen sovelluksen metatiedoista tällä tavoin on käytettävissä vain paikallisesti käyttöönotetuissa sovelluksissa (kun liiketoimintatietojen paikallista \[LBD\] käyttöönottomallia käytetään sovelluksessa).

## <a name="access-application-metadata-by-using-connected-applications"></a>Sovelluksen metatietojen käyttäminen yhdistetyillä sovelluksilla

Seuraava menettely näyttää, miten RCS-käyttäjä, jolla on **Järjestelmänvalvoja**- tai **Sähköisen raportoinnin kehittäjä** -rooli, voi suunnitella uuden ER-mallin yhdistämismäärityksen käyttämällä sovelluksen metatietoja. Sovelluksen metatietoja käytetään verkossa RCS:n yhdistetyllä sovelluksella. ER-näytemallin yhdistäminen määritetään käyttämään ulkomaankauppatapahtumia.

Menettelyn [Konfiguraation lähteiden luominen ja niiden merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheet on suoritettava ennen tämän menettelyn suorittamista RCS:ssä. Jos et ole vielä viimeistellyt [Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla](#access-application-metadata-by-using-an-er-configuration) -menettelyä aiemmin tässä ohjeaiheessa, siirry [Dynamics 365 for Finance and Operations 8.1:n sähköisen raportoinnin tehtäväoppaat](https://go.microsoft.com/fwlink/?linkid=2082739) -sivulle ja lataa seuraavat ER-konfiguraatiotiedostot etukäteen ja tallenna ne paikallisesti: **Ulkomaankaupan metatiedot.xml**, **Ulkomaankauppamalli.xml** ja **Ulkomaankaupan yhdistäminen.xml**.


### <a name="get-required-er-configurations"></a>Tarvittavien ER-konfiguraatioiden hankkiminen

Jos olet jo suorittanut [Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla](#access-application-metadata-by-using-an-er-configuration) -menettelyn aiemmin tässä vaiheessa, sinulla on jo tarvittavat nykyisen RCS-esiintymän ER-määritykset (ulkomaankaupan metatietojen, mallin ja yhdistämisen määritykset). Voit siinä tapauksessa ohittaa tämän menettelyn.

1. Valitse **Kaikki työtilat \> Sähköinen raportointi**.
2. Valitse **Raportointikonfiguraatiot**.
3. Lataa **Ulkomaankaupan metatiedot.xml**-, **Ulkomaankauppamalli.xml**- ja **Ulkomaankaupan yhdistäminen.xml** -määritystiedostot toistamalla seuraavat peräkkäiset vaiheet kunkin kohdalla:

    1. Valitse **Vaihto**.
    2. Valitse **Lataa XML-tiedostosta**.
    3. Valitse ensin **Selaa** ja sitten tiedosto.
    4. Valitse **OK**.

### <a name="register-the-connection-with-the-application"></a>Rekisteröi yhteys sovellukseen

1. Valitse **Kaikki työtilat \> Sähköinen raportointi**.
2. Valitse **Yhdistetyt sovellukset**.
3. Varmista, että määritetty sovellus perustuu Microsoft Azureen ja että se on yleisesti RCS-käyttäjien käytettävissä. Nykyisellä RCS-käyttäjällä on oltava valitun sovelluksen käyttöoikeus ja hänen on oltava rekisteröitynyt sovelluksen käyttäjäksi roolilla, jolla voi käyttää sovelluksen metatietoja.
4. Valitse **Uusi**.
5. Kirjoita **Nimi**-kenttään **MyConnectedApp** yhdistetyn sovelluksen nimeksi.
6. Määritä sovelluksen URL-osoite **Sovellus**-kentässä.
7. Määritä sovelluksen toimittaja **Vuokraaja**-kentässä.
8. Valitse **Tallenna**. 
9. Voit tarkistaa yhteyden määritettyyn sovellukseen valitsemalla **Yhdistä etäsovellukseen** -sivulla **Muodosta yhteys etäsovellukseen valitsemalla tämä** -linkki. 
10. Tarkista määritetyn sovelluksen käyttöoikeus valitsemalla **Tarkista yhteys**.
11. Valitse **Sulje**.

Kun olet suorittanut tämän menettelyn ja yhteyden tarkistus onnistuu, nykyisen ruudukon määritetyn sovelluksen version ja vuokraajan tiedot päivitetään.

### <a name="review-the-existing-model-mapping-configuration"></a>Aiemmin määritetyn mallin yhdistämismäärityksen tarkasteleminen

1. Valitse **Kaikki työtilat \> Sähköinen raportointi**.
2. Valitse **Raportointikonfiguraatiot**.
3. Valitse puussa **Ulkomaankauppamalli \> Ulkomaankaupan yhdistäminen**.
4. Valitse **Edellytykset**-pikavälilehti.

    > [!NOTE]
    > Tällä hetkellä yhdistämismääritys viittaa metatietomääritykseen. Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan.

4. Valitse **Suunnittelu**.
5. Valitse **Suunnittelu**.
6. Valitse puussa **Dynamics 365 for Operations \> Taulukkotietueet**.
7. Valitse **Lisää pääkansio**.
8. Anna tai valitse **Taulu**-kentässä arvo.

    > [!NOTE]
    > Tällä hetkellä yhdistämismääritys viittaa metatietomääritykseen. Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan.

9. Valitse **Peruuta**.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>Yhdistetyn sovelluksen määrittäminen mallin yhdistämiseen

1. Valitse **Muokkaa**.
2. Valitse **Yhdistetty sovellus** -kentässä **MyConnectedApp**-sovellus.

    > [!NOTE]
    > Tämä yhdistämismääritys viittaa valitun yhdistetyn sovelluksen metatietoihin. Jos yhdistämismääritys viittaa samanaikaisesti metatietojen määritykseen ja yhdistettyyn sovellukseen, yhdistetyn sovelluksen metatietoja käytetään.

3. Valitse **Suunnittelu**.
4. Valitse **Suunnittelu**.
5. Valitse puussa **Dynamics 365 for Operations \> Taulukkotietueet**.
6. Valitse **Lisää pääkansio**.
7. Anna tai valitse **Taulu**-kentässä arvo.

    > [!NOTE]
    > Tällä hetkellä valittavana on nyt enemmän kuin kaksi sovellustaulukkoa, sillä tämä yhdistämismääritys käyttää siihen määritetyn yhdistetyn sovelluksen kaikkia metatietoja.

8. Valitse **Peruuta**.
9. Valitse **Tarkista**.

Tietomallin elementtien ja kuvattujen nimikkeiden tietolähteiden sitominen onnistui käyttämällä tähän yhdistämismääritykseen määritetyn yhdistetyn sovelluksen metatietoja.

Kun tämä malli on arvioitava käyttämällä toisen version sovelluksen metatietoja, rekisteröi toinen yhdistetty sovellus, määritä se tähän mallin yhdistämismääritykseen ja vahvista se käyttämällä uusia metatietoja.

## <a name="additional-resources"></a>Lisäresurssit

Vaihtoehtoisesti voit toistaa **RSC:ssä käytettävien sovelluksen metatietojen valmisteleminen** -tehtäväoppaan sovelluksessa sekä **Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla**- ja **Sovelluksen metatietojen käyttäminen yhdistetyillä sovelluksilla** -tehtäväoppaat RCS:ssä. Tehtäväoppaat voidaan ladata [Dynamics 365 for Finance and Operations 8.1:n sähköisen raportoinnin tehtäväoppaat](https://go.microsoft.com/fwlink/?linkid=2082739) -sivulla.
