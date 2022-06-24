---
title: Maakontekstista riippuvaisten sähköisen raportoinnin mallimääritysten määrittäminen
description: Tässä artikkelissa käsitellään ER-mallimääritysten määrittämistä siten, että ne määräytyvät sen yrityksen maa- tai aluekontekstista, jonka määrittää niiden käytön.
author: NickSelin
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 771b14662638838ac1f39d85b19ac58a47352c79
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883872"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>Maakontekstin mukaan määräytyvien ER-mallimääritysten määrittäminen

[!include[banner](../includes/banner.md)]

Voit määrittää sähköisen raporttimallin (ER-mallin) määritykset siten, että ne noudattavat yleistä ER-tietomallia mutta koskevat Dynamics 365 Financea. Tässä artikkelissa käsitellä tapaa, jolla ER-tietomalliin määritetään useita ER-mallimäärityksiä. Niiden tarkoituksena on hallita sitä, miten vastaavat ER-muodot käyttävät niitä, kun näitä ER-muotoja suorittavissa yrityksissä ei ole sama maa- tai aluekonteksti.

## <a name="prerequisites"></a>Edellytykset

Tämän artikkelin esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:

- Finance-käyttöoikeudet seuraaville rooleille:
    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

- Sellaisen Regulatory Configuration Services (RCS) -esiintymän käyttöoikeus, joka on valmisteltu samalle vuokraajalle kuin Finance ja jossa on käytössä jokin seuraavista rooleista:
    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

Joissakin tämän artikkelin vaiheissa on suoritettava ER-muoto. Joissakin tapauksissa sen yrityksen maa- tai aluekonteksti, johon olet kirjautuneena, vaikuttaa ER-muodon suorittamiseen. Voit suorittaa ER-muodon nykyisessä RCS-esiintymässä, jos yrityksen, jossa tarvittava maa- tai aluekonteksti on, on käytettävissä RCS:ssä. Muussa tapauksessa Finance-esiintymään on ladattava ER-tietomallia käyttävän ER-mallin määrityksen ja ER-muodon määritysten täydellinen versio ja ER-muoto on sitten suoritettava Finance-esiintymässä. Lisätietoja RCS:n määritysten tuomisesta Finance-esiintymään on kohdassa [Määritysten tuonti RCS:stä](rcs-download-configurations.md).

## <a name="single-model-mapping-case"></a>Yhden mallin yhdistäminen

Suunnittele tarvittavat ER-osat tämän artikkelin [liitteen 1](#appendix1) ohjeiden mukaan. Sinulla on nyt **Yhdistämismääritys (yleinen)** -mallin yhdistämismääritys, joka sisältää **Aloituskohta 1** -määritelmän mallimäärityksen.

![ER-konfiguraatiot -sivu, Muoto määrityskonfiguraation oppimiseksi.](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>Määritetyn muodon suorittaminen

1.  Valitse **Konfiguroinnit-sivun** **Versiot**-pikavälilehdessä **Suorita**.
2.  Valitse **OK**.

Huomaa, että selain ehdottaa suoritetun ER-muodon muodostaman tekstitiedoston lataamista. Koska tämä muoto määritettiin käyttämään **Aloituskohta 1** -määritelmää ja koska tämän määritelmän sisältävään perusmalliin on tällä hetkellä käytettävissä vain yksi mallimääritys, suoritettu ER-muoto käytti **Yhdistämismääritys (yleinen)** -määrityksen **Yhdistämismääritys (yleinen)** -mallimääritystä tietolähteenä. Tämän vuoksi ladatussa on tiedostossa on **Yleinen toiminto 1** -teksti.

## <a name="multiple-shared-model-mappings-case"></a>Usean jaetun mallin yhdistäminen

Suunnittele tarvittavat ER-osat tämän artikkelin [liitteen 2](#appendix2) ohjeiden mukaan. Sinulla on nyt **Yhdistämismääritys (yleinen)**- ja **Yhdistämismääritys (yleinen), mukautettu** -mallin yhdistämismääritykset, joista kumpikin sisältää **Aloituskohta 1** -määritelmän mallimäärityksen.

![ER-konfiguroinnit -sivu, yleisen mukautetun konfiguraation määritys.](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>Määritetyn muodon suorittaminen

1.  Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Yhdistämismääritysten oppimismuoto**.
2.  Valitse **Versiot**-pikavälilehdessä **Suorita**.
3.  Valitse **OK**.

Huomaa, että valitun ER-muodon suorittaminen epäonnistuu. Virhesanoman mukaan **Yhdistämismääritysten oppimismalli**-mallilla sekä **Yhdistämismääritys (yleinen)**- ja **Yhdistämismääritys (yleinen), mukautettu** -mallimäärityksen määritysten **Aloituskohta 1** -määritelmällä on vähintään kaksi mallimääritystä. Sanoma suosittelee lisäksi, että jonkin kyseisen määrityksen valitsemista oletusmääritykseksi.

![ER-konfiguroinnit -sivu ja virhesanoma.](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>Oletusyhdistämismäärityksen määrittäminen

Määritä **Yhdistämismääritys (yleinen), mukautettu** -mallin yhdistämismääritys seuraavien ohjeiden mukaan oletusmääritykseksi. Tällä tavoin sen yhdistämismäärityksiä käytetään ER-muodon **Yhdistämismääritysten oppimismuoto** tietolähteinä.

1.  Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Yhdistämismääritykset (Yleinen), mukautettu**.
2.  Valmistele valittu sivu muokattavaksi valitsemalla **Muokkaa**.
3.  Määritä **Mallin yhdistämisasetuksen** oletusarvoksi **Kyllä**.
4.  Valitse **Tallenna**.

![ER-konfiguraatiosivu, Mallimäärityksen oletus -liukusäätimen arvoksi on asetettu Kyllä.](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>Määritetyn muodon suorittaminen

1.  Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Yhdistämismääritysten oppimismuoto**.
2.  Valitse **Versiot**-pikavälilehdessä **Suorita**.
3.  Valitse **OK**.

Huomaa, että valitun ER-muodon suorittaminen onnistuu. Selain ehdottaa suoritetun ER-muodon muodostaman tekstitiedoston lataamista. Koska tämä muoto määritettiin käyttämään **Aloituskohta 1** -määritelmää ja **Yhdistämismääritys (yleinen), mukautettu** -mallin yhdistämismääritys valittiin oletusmääritykseksi, suoritettu ER-muoto käytti **Yhdistämismääritys (yleinen), mukautettu** -määrityksen **Yhdistämismääritys (yleinen), mukautettu** -mallimääritystä tietolähteenä. Tämän vuoksi ladatussa on tiedostossa on teksti **Yleinen toiminto 1, mukautettu**.

> [!NOTE]
> Jos vaihdat yritystä, johon olet kirjautuneena, ja suoritat tämän ER-muodon uudelleen, muodostettavassa tiedostossa on sama sisältö, koska ER-mallin oletusyhdistämismäärityksessä ei ole mitään yrityksestä riippuvaisia rajoituksia.

## <a name="multiple-mixed-model-mappings-case"></a>Usean yhdistelmämallin yhdistämismääritykset

Suunnittele tarvittavat ER-osat tämän artikkelin [liitteen 3](#appendix3) ohjeiden mukaan. Sinulla on nyt **Yhdistämismääritys (yleinen)**-, **Yhdistämismääritys (yleinen), mukautettu**- ja **Yhdistämismääritys (FR)** -mallin yhdistämismääritykset, jotka sisältävät **Aloituskohta 1** -määritelmän mallimäärityksen.

Huomaa, että **Yhdistämismääritys (FR)** -mallin yhdistämismäärityksen versio 1 on määritetty siten, että se koskee vain niissä Finance-yrityksissä suoritettavia **Yhdistämismääritysten oppimismalli** -mallin ER-muotoja, joissa on ranskalainen maa- tai aluekonteksti.

![ER-konfiguroinnit -sivu, Mallimäärityksen (FR) konfiguraatio.](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>Määritetyn muodon suorittaminen

1.  Vaihda yritykseksi **FRSI**.
2.  Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Yhdistämismääritysten oppimismuoto**.
3.  Valitse **Versiot**-pikavälilehdessä **Suorita**.
4.  Valitse **OK**.

Huomaa, että valitun ER-muodon suorittaminen onnistuu. Selain ehdottaa suoritetun ER-muodon muodostaman tekstitiedoston lataamista. Koska tämä muoto määritettiin käyttämään **Aloituskohta 1** -määritelmää ja **Yhdistämismääritys (yleinen), mukautettu** -mallin yhdistämismääritys valittiin oletusmääritykseksi, suoritettu ER-muoto käytti **Yhdistämismääritys (yleinen), mukautettu** -määrityksen **Yhdistämismääritys (yleinen), mukautettu** -mallimääritystä tietolähteenä. Tämän vuoksi ladatussa on tiedostossa on teksti **Yleinen toiminto 1, mukautettu**.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>Ranskaa koskevan yhdistämismäärityksen määrittäminen oletusmääritykseksi

Määritä **Yhdistämismääritys (FR)** -mallin yhdistämismääritys seuraavien ohjeiden mukaan oletusmääritykseksi. Huomaa, että koska tämä yhdistämismääritys koskee Ranskaa, sitä pidetään oletusyhdistämismäärityksenä kaikissa niissä mallin yhdistämismäärityksissä, joissa **FR**-maakoodi on määritetty **ISO-maa-/-aluekoodit** -kentässä.

1.  Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Yhdistämismääritys (FR)**.
2.  Valmistele valittu sivu muokattavaksi valitsemalla **Muokkaa**.
3.  Määritä **Mallin yhdistämisasetuksen** oletusarvoksi **Kyllä**.
4.  Valitse **Tallenna**.

![ER-konfiguraatiosivu, Mallimäärityksen (FR) konfiguraatio, Mallimäärityksen oletus -liukusäätimen arvoksi on asetettu Kyllä.](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>Määritetyn muodon suorittaminen

1.  Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Yhdistämismääritysten oppimismuoto**.
2.  Valitse **Versiot**-pikavälilehdessä **Suorita**.
3.  Valitse **OK**.

Huomaa, että valitun ER-muodon suorittaminen onnistuu. Selain ehdottaa suoritetun ER-muodon muodostaman tekstitiedoston lataamista. Koska tämä muoto määritettiin käyttämään **Aloituskohta 1** -määritelmää ja **Yhdistämismääritys (FR)** -mallin yhdistämismääritys valittiin oletusmääritykseksi, suoritettu ER-muoto käytti **Yhdistämismääritys (FR)** -määrityksen **Yhdistämismääritys (FR)** -mallimääritystä tietolähteenä. Tämän vuoksi ladatussa on tiedostossa on teksti **FR-toiminto 1**.

> [!NOTE]
> Jos vaihdat yritystä, johon olet kirjautuneena, ja suoritat tämän ER-muodon uudelleen, tulos määräytyy valitun yrityksen maa- tai aluekontekstin mukaan.

## <a name="other-model-mapping-cases"></a>Muut mallin yhdistämismääritykset

Kuten edellä on huomattu, ER-muodon suorittamiseen valittu mallimääritys toimii seuraavasti:

- ER-muodon käyttämä mallimäärityksen määritelmä määritetään (tämän artikkelin esimerkeissä **Aloituskohta 1**).
- Kaikkia yhdistämismäärityksiä, joissa määritetyn määritelmän sisältämä yhdistämismääritys on ja jotka vastaavat määritettyjä maa- tai aluekohtaisia rajoituksia, on mahdollista käyttää ER-muodon suorittamiseen (tämän artikkelin esimerkeissä **Yhdistämismääritykset (Yleinen)**, **Yhdistämismääritykset (Yleinen), mukautettu** ja **Yhdistämismääritys (FR)**).
- Maa- tai aluekohtaisia rajoituksia sisältävän oletusmallimäärityksen valintaprioriteetti on korkein (tämän artikkelin esimerkeissä **Yhdistämismääritys (FR)**).
- Oletusmallimäärityksellä, jossa ei ole maa- tai aluekohtaisia rajoituksia, on seuraavaksi korkein valintaprioriteetti (tämän artikkelin esimerkeissä **Yhdistämismääritys (Yleinen), mukautettu**).
- Jos mallimäärityksellä on maa- tai aluekohtaisia rajoituksia, sen valintaprioriteetti on korkeampi kuin mallimääritys, jossa ei ole maa- tai aluekohtaisia rajoituksia.

Seuraavassa taulukossa on tietoja mallin määritysvalinnasta kaikissa mahdollisissa mallin määritysasetustilanteissa:

- Sarake 1 ilmaisee, näytetäänkö ensimmäinen mallimääritys, jossa ei ole maa- tai aluekohtaisia rajoituksia (kuten jaettu **Yhdistämismääritys (Yleinen)** -yhdistämismääritys), ja jos näytetään, onko **Mallin oletusmääritys** -asetukseksi määritetty **Kyllä**.
- Sarake 2 ilmaisee, näytetäänkö toinen mallimääritys, jossa ei ole maa- tai aluekohtaisia rajoituksia (kuten jaettu **Yhdistämismääritys (Yleinen), mukautettu** -yhdistämismääritys), ja jos näytetään, onko **Mallin oletusmääritys** -asetukseksi määritetty **Kyllä**.
- Sarake 3 ilmaisee, näytetäänkö ensimmäinen mallimääritys, jossa on maan tai alueen A:n kontekstirajoitukset (kuten Ranskan **Yhdistämismääritys (FR)** -yhdistämismääritys), ja jos näytetään, onko **Mallin oletusmääritys** -asetukseksi määritetty **Kyllä**.
- Sarake 4 ilmaisee, näytetäänkö toinen mallimääritys, jossa on maan tai alueen A:n kontekstirajoitukset, ja jos näytetään, onko **Mallin oletusmääritys** -asetukseksi määritetty **Kyllä**.
- Sarake 5 sisältää mallin määritysvalinnan sen ER-muodon suorittamista varten, jota ohjaavalla yrityksellä on maan tai alueen A konteksti.
- Sarake 6 sisältää mallin määritysvalinnan sen ER-muodon suorittamista varten, jota ohjaavalla yrityksellä on maan tai alueen B konteksti.

Taulukossa plusmerkki (+) ilmaisee mallin yhdistämismäärityksen sen Microsoft Azure -palvelun valitussa esiintymässä, jolla ER-muoto suoritetaan (joko Finance tai RCS).

| Laatikko | Mallin määritys 1 ilman maa- tai aluekontekstia (MM1) | Mallin määritys 2 ilman maa- tai aluekontekstia (MM2) | Mallin määritys 1, jossa on maa- tai aluekonteksti (MM1A) | Mallin määritys 2, jossa on maa- tai aluekonteksti (MM2A) | Suoritus sen yrityksen hallinnassa, jossa on maan tai alueen A konteksti | Suoritus sen yrityksen hallinnassa, jossa on maan tai alueen B konteksti |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | Virhe (puuttuva yhdistämismääritys)   | Virhe (puuttuva yhdistämismääritys)    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | Virhe (useita yhdistämismäärityksiä) | Virhe (useita yhdistämismäärityksiä)  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | Virhe (useita yhdistämismäärityksiä) | MM1                        |
|     6   |     +   | oletus |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | oletus |         | MM1A                      | MM1                        |
|     8   |     +   |         | oletus |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | oletus | oletus | Virhe (useita yhdistämismäärityksiä) | MM1                        |
|    10   | oletus |         |         |         | MM1                       | MM1                        |
|    11   | oletus |    +    |         |         | MM1                       | MM1                        |
|    12   | oletus |         |    +    |         | MM1                       | MM1                        |
|    13   | oletus | oletus |         |         | Virhe (useita yhdistämismäärityksiä) | Virhe (useita yhdistämismäärityksiä)  |
|    14   | oletus |         | oletus |         | MM1A                      | MM1                        |
|    15   | oletus |         | oletus | oletus | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | oletus | oletus | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>ER-muodon suorituksessa käytetyn yhdistämismäärityksen selvittäminen

### <a name="configure-er-user-parameters"></a>ER-käyttäjän parametrien määrittäminen

1.  Valitse **Konfiguroinnit**-sivun toimintoruudun **KONFIGUROINNIT**-välilehdessä **Käyttäjän parametrit**.
2.  Määritä **Suorita virheenkorjaustila** -asetukseksi **Kyllä**.
4.  Valitse **Ok**.

### <a name="run-the-configured-format"></a>Määritetyn muodon suorittaminen

1.  Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Yhdistämismääritysten oppimismuoto**.
2.  Valitse **Versiot**-pikavälilehdessä **Suorita**.
3.  Valitse **Ok**.

### <a name="review-the-er-debug-log"></a>ER-vianmäärityslokin tarkasteleminen

1.  Valitse siirtymisruudussa **Moduulit \> Organisaation hallinto \> Sähköinen raportointi \> Määritysten virheenkorjauslokit**.
2.  Valitse **Lataa tämä sivu uudelleen** -painike.

![ER-suorituslokisivu.](./media/RCS-Context-specific-mapping-DebugLog.PNG)

Huomaa, että uusi tietue on lisätty suoritetun ER-muodon ER-virheenmäärityslokiin. Koska tämän tietueen **Taso**-kentän arvoksi on määritetty **Tiedot**, tietue on tarkoitettu tiedoksi. Koska Muotokomponentti-kentän asetukseksi on määritetty **Yhdistämismääritys**, tietueessa on tietoja mallin määrityksestä, jota käytettiin **Yhdistämismääritysten oppimismuoto** -ER-muodon suorituksen aikana. (Tämä asetus on valittu **Konfiguraation nimi** -kentässä). **Muodostettu teksti** -kentän sisältö ilmaisee, että raportti on suoritettu käytättämällä **Yhdistämismääritys (FR)** -määrityksessä olevaa **Yhdistämismääritys (FR)** -yhdistämisosaa.

## <a name="appendix-1"></a><a name="appendix1"></a> Liite 1

### <a name="configure-a-sample-data-model"></a>Näytetietomallin määrittäminen

Kirjaudu RCS-esiintymään.

Tällä esimerkissä luodaan määritys malliyritykselle Litware, Inc. Näiden vaiheiden suorittamista varten on ensin RCS:ssä [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet.

#### <a name="create-an-er-data-model-configuration"></a>Uuden ER-tietomallin määrityksen luominen

1.  Valitse oletuskoontinäytössä **Sähköinen raportointi**.
2.  Valitse **Raportointikonfiguraatiot**-ruutu.
3.  Valitse **Konfiguroinnit**-sivulla **Luo konfigurointi**.
4.  Kirjoita avattavan luettelon **Nimi**-kenttään **Yhdistämismääritysten oppimismalli**.
5.  Valitse **Luo konfiguraatio**.
6.  Valitse **Määrityksen osat** -pikavälilehti.

Huomaa, että tämän ER-määrityksen luonnosversio 1 on valmis muokattavaksi. Tämä versio sisältää tietomalliosan.

#### <a name="design-a-sample-data-model"></a>Näytetietomallin suunnitteleminen

1.  Valitse **Konfiguraatiot**-sivulla **Suunnittelutoiminto**.
2.  Valitse **Uusi**.
3.  Kirjoita avattavan luettelon valintaikkunan **Nimi**-kenttään **Aloituspiste 1**.
4.  Valitse **Lisää**.
5.  Valitse **Uusi**.
6.  Kirjoita avattavan luettelon **Nimi**-kenttään **Toimintojen kuvaus**.
7.  Valitse **Lisää**.
8.  Valitse **Uusi**.
9.  Valitse avattavan luettelon **Uusi solmu**-kenttäryhmässä **Mallin juuri**.
10. Kirjoita **Nimi**-kenttään **Aloituspiste 2**.
11. Valitse **Aloituspiste 2**.
12. Valitse **Lisää**.
13. Valitse **Uusi**.
14. Kirjoita avattavan luettelon **Nimi**-kenttään **Toimintojen kuvaus**.
15. Valitse **Lisää**.

    ![ER-tietomallin suunnittelutoiminnon sivu.](./media/RCS-Context-specific-mapping-Model.PNG)

16. Valitse **Tallenna**.
17. Sulje sivu.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>Mallimäärityksen muokatun version viimeisteleminen

1.  Valitse **Konfiguroinnit**-sivun **Versiot**-pikavälilehdessä **Muuta tila**.

    > Muuta suunnitellun mallimäärityksen tila **luonnoksesta** **valmiiksi**, jotta sen avulla voidaan suunnitella tarvittavat mallin yhdistämismääritykset ja muodot.

2.  Valitse **Valmis**.
3.  Valitse **OK**.

Huomaa, että luotu konfiguraatio tallennetaan valmiina versiona 1.

### <a name="configure-a-sample-model-mapping"></a>Näytetietomallin yhdistämismäärityksen määrittäminen

#### <a name="create-an-er-model-mapping-configuration"></a>ER-mallin yhdistämismäärityksen luominen

1.  Valitse **Konfiguroinnit**-sivulla **Luo konfigurointi**.
2.  Valitse avattavasta valintaikkunasta **Uusi**-kenttäryhmässä **Yhdistämismääritysten oppimismalli -tietomalliin perustuva mallin määritys**.
3.  Kirjoita **Nimi**-kenttään **Yhdistämismääritys (Yleinen)**.
4.  Valitse **Tietomallin määritelmä** -kentässä **Aloituspiste 1**.
5.  Valitse **Luo konfiguraatio**.

Huomaa, että tämän ER-määrityksen luonnosversio 1 on valmis muokattavaksi. Tämä versio sisältää mallin määritysosan.

#### <a name="design-a-sample-model-mapping"></a>Näytemallin yhdistämismäärityksen suunnitteleminen

1.  Valitse **Määritys**-sivulla **Suunnittelija**.

    Huomaa, että **Malliin**-suuntatyyppi mallin yhdistämismääritys on lisätty automaattisesti tähän osaan **Aloituspiste 1** -määritelmässä.
    
2.  Aloita lisätyn mallin yhdistämismäärityksen muokkaaminen valitsemalla **Suunnittelutoiminto**.
3.  Valitse **Tietomalli**-osassa **Muokkaa**.
4.  Kirjoita **Kaava**-kenttään **Yleinen toiminto 1**.
5.  Valitse **Tallenna**.
6.  Sulje **Reseptien suunnittelu** -sivu.

    ![ER-mallimäärityksen suunnittelusivu, aloituspisteen 1 määritys.](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  Valitse **Tallenna**.
8.  Sulje **Mallimäärityksen sunnittelun** sivu.
9.  Valitse **Uusi**.
10. Valitse **Määritelmä** -kentässä **Aloituspiste 2**.
11. Kirjoita **Nimi**-kenttään **Yhdistämismääritys (Yleinen) 2**.
12. Valitse **Suunnittelu**.
13. Valitse **Tietomalli**-osassa **Muokkaa**.
14. Kirjoita **Kaava**-kenttään **Yleinen toiminto 2**.
15. Valitse **Tallenna**.
16. Sulje **Reseptien suunnittelu** -sivu.

    ![ER-mallimäärityksen suunnittelusivu, aloituspisteen 2 määritys.](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. Valitse **Tallenna**.
18. Sulje **Mallimäärityksen sunnittelun** sivu.

    ![ER-mallimäärityksen suunnittelusivu, jossa aloituspisteiden määritykset.](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. Sulje **Mallimääritykset**-sivu.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Mallin yhdistämismäärityksen muokatun version viimeisteleminen

1.  Valitse **Konfiguroinnit**-sivun **Versiot**-pikavälilehdessä **Muuta tila**.

    > Muuta suunnitellun mallin yhdistämismäärityksen tila **luonnoksesta** **valmiiksi**, jotta ER-muodot voivat käyttää sitä.

2.  Valitse **Valmis**.
3.  Valitse **OK**.

Huomaa, että luotu konfiguraatio tallennetaan valmiina versiona 1.

### <a name="configure-a-sample-format"></a>Näytemuodon määrittäminen

#### <a name="create-an-er-format-configuration"></a>ER-muotokonfiguraation luominen

1.  Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Yhdistämismääritysten oppimismalli**.
2.  Valitse **Luo konfiguraatio**.
3.  Valitse avattavasta valintaikkunasta **Uusi**-kenttäryhmässä **Yhdistämismääritysten oppimismalli -tietomalliin perustuva muoto**.
4.  Anna **Nimi**-kentässä **Yhdistämismääritysten oppimismuoto**.
5.  Valitse **Tietomallin määritelmä** -kentässä **Aloituspiste 1**.
6.  Valitse **Luo konfiguraatio**.

Huomaa, että tämän ER-määrityksen luonnosversio 1 on valmis muokattavaksi. Tämä versio sisältää muoto-osan.

#### <a name="design-a-sample-format"></a>Näytemuodon suunnittelu

1.  Valitse **Määritys**-sivulla **Suunnittelija**.
2.  Valitse **Lisää pääkansio**.
3.  Valitse **Teksti**-ryhmässä **Merkkijono**-kohta.
4.  Valitse **OK**.

#### <a name="bind-format-elements-to-a-data-source"></a>Muotoelementtien sidonta tietolähteiseen

1.  Laajenna mallin tietolähde **Muodon suunnitteluohjelma** -sivun **Yhdistämismääritys**-välilehdessä.
2.  Valitse **Toimintojen kuvaus** -kenttä.
3.  Valitse **Sido**.

    ![ER-muodon suunnittelutoiminnon sivu.](./media/RCS-Context-specific-mapping-Format.PNG)

4.  Valitse **Tallenna**.
5.  Sulje sivu.

## <a name="appendix-2"></a><a name="appendix2"></a> Liite 2

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>Näytemallimäärityksen määrittäminen yleistä muokkausta varten

Haluat ehkä muokata mallimääritystä, jonka olet saanut määrityspalvelusta (kumppanilta) ja käyttää sitten mukautettua versiota ER-muotojen tietolähteenä. Siinä tapauksessa sinun on luotava mukautettu ER-mallin yhdistämismääritys, jolla voi tehdä tarvittavat muutokset aiemmin luoduissa mallimäärityksissä. Tämän liitteen menettelyissä käytetään esimerkkinä **Yhdistämismääritys (Yleinen)** -mallimäärityksenä.

#### <a name="create-an-er-model-mapping-configuration"></a>ER-mallin yhdistämismäärityksen luominen

1.  Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Yhdistämismääritykset (Yleinen)**.
2.  Valitse **Luo konfiguraatio**.
3.  Valitse avattavan valintaikkunan **Uusi**-kenttäryhmässä **Johdettu nimestä: Yhdistämismääritys (Yleinen), Litware, Inc.**.
4.  Kirjoita **Nimi**-kenttään **Yhdistämismääritys (Yleinen), mukautettu**.
5.  Valitse **Luo konfiguraatio**.

Huomaa, että tämän ER-määrityksen luonnosversio 1 on valmis muokattavaksi.

#### <a name="design-a-sample-model-mapping"></a>Näytemallin yhdistämismäärityksen suunnitteleminen

1.  Valitse **Määritys**-sivulla **Suunnittelija**.

    > Huomaa, että perusmäärityksen mallimääritykset on kopioitu automaattisesti tähän määritykseen.

2.  Valitse **Yhdistämismääritys (Yleinen), kopio** -yhdistämismääritys.
3.  Valitse **Suunnittelu**.
4.  Valitse **Tietomalli**-osassa **Muokkaa**.
5.  Kirjoita **Kaava**-kenttään **Yleinen toiminto 1, mukautettu**.
6.  Valitse **Tallenna**.
7.  Sulje sivu.

    ![ER-mallimäärityksen suunnittelusivu, yleisen toiminnon 1 mukautettu kaava.](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  Valitse **Tallenna**.
9.  Sulje sivu.
10. Valitse **Yhdistämismääritys (Yleinen) 2, kopio** -yhdistämismääritys.
11. Valitse **Suunnittelu**.
12. Valitse **Tietomalli**-osassa **Muokkaa**.
13. Kirjoita **Kaava**-kenttään **Yleinen toiminto 2, mukautettu**.
14. Valitse **Tallenna**.
15. Sulje sivu.

    ![ER-mallimäärityksen suunnittelusivu, yleisen toiminnon 2 mukautettu kaava.](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. Valitse **Tallenna**.
17. Sulje sivu.

    ![ER-mallista tietolähteeseen -määrityssivu Määritys (yleinen) – kopioi määritys.](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. Sulje sivu.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Mallin yhdistämismäärityksen muokatun version viimeisteleminen

1.  Valitse **Konfiguroinnit**-sivun **Versiot**-pikavälilehdessä **Muuta tila**.

    > Muuta suunnitellun mallin yhdistämismäärityksen tila **luonnoksesta** **valmiiksi**, jotta ER-muodot voivat käyttää sitä.

2.  Valitse **Valmis**.
3.  Valitse **OK**.

Huomaa, että luotu konfiguraatio tallennetaan valmiina versiona 1.

## <a name="appendix-3"></a><a name="appendix3"></a> Liite 3

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>Näytemallimäärityksen määrittäminen maa- tai aluekohtaista muokkausta varten

Joissakin ER-muodoissa tietojen valmistelulla voi olla maa- tai aluekohtaisia vaatimuksia. Tässä tapauksessa voi hallita erillistä ER-mallin yhdistämismääritystä ja eristää näiden maa- tai aluekohtaisten vaatimusten toteutuksen yleisestä toteutuksesta. Liitteen menettelyissä käytetään esimerkkeinä **Yhdistämismääritysten oppimismuoto** -ER-muotoa ja ranskankielisiä vaatimuksia.

#### <a name="create-an-er-model-mapping-configuration"></a>ER-mallin yhdistämismäärityksen luominen

Luo ensimmäiseksi uusi ER-mallin yhdistämismääritys toteuttamaan maa- tai aluekohtaisia vaatimuksia. Käytä perustana mukautettua ER-mallin yhdistämismääritystä.

1.  Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Yhdistämismääritykset (Yleinen), mukautettu**.
2.  Valitse **Luo konfiguraatio**.
3.  Valitse avattavan valintaikkunan **Uusi**-kenttäryhmässä **Johdettu nimestä: Yhdistämismääritys (Yleinen), mukautettu, Litware, Inc**.
4.  Kirjoita **Nimi**-kenttään **Yhdistämismääritys (FR)**.
5.  Valitse **Luo konfiguraatio**.

Huomaa, että tämän ER-määrityksen luonnosversio 1 on valmis muokattavaksi.

#### <a name="design-a-sample-model-mapping"></a>Näytemallin yhdistämismäärityksen suunnitteleminen

1.  Valitse **Määritys**-sivulla **Suunnittelija**.

    > Huomaa, että perusmäärityksen mallimääritykset on kopioitu automaattisesti tähän määritykseen.

2.  Valitse **Yhdistämismääritys (Yleinen), kopio kopio** -yhdistämismääritys.
3.  Vaihda sen nimeksi **Yhdistämismääritys (FR)**.
4.  Valitse **Suunnittelu**.
5.  Valitse **Tietomalli**-osassa **Muokkaa**.
6.  Kirjoita **Kaava**-kenttään **FR toiminto 1**.
7.  Valitse **Tallenna**.
8.  Sulje sivu.

    ![ER-mallimäärityksen suunnittelusivu, FR-toiminnon 1 kaava.](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  Valitse **Tallenna**.
10. Sulje sivu.
11. Valitse **Yhdistämismääritys (Yleinen) 2, kopio kopio** -yhdistämismääritys.
12. Vaihda sen nimeksi **Yhdistämismääritys (FR) 2**.
13. Valitse **Suunnittelu**.
14. Valitse **Tietomalli**-osassa **Muokkaa**.
15. Kirjoita **Kaava**-kenttään **FR toiminto 2**.
16. Valitse **Tallenna**.
17. Sulje sivu.

    ![ER-mallimäärityksen suunnittelusivu, FR-toiminnon 2 kaava.](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. Valitse **Tallenna**.
19. Sulje sivu.

    ![ER-mallista tietolähteeseen -määrityssivu.](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. Sulje sivu.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>Käytettävien maa- tai aluekohtaisten rajoitusten määrittäminen

1.  Valitse **Konfiguroinnit**-sivulla **ISO-maa-/-aluekoodi**-pikavälilehdessä **Uusi**.
2.  Valitse **ISO**-kentässä **FR**.
3.  Valitse **Tallenna**.

Huomaa, että ER-muodon suorittaminen edellyttää tiettyyn yritykseen kirjautumista Financessa. Tämän vuoksi tätä yritystä voidaan pitää osapuolena, joka hallitsee ER-muodon suorittamista ja oikean ER-perustietomallin ER-mallimäärityksen valintaa. **FR**-maakoodin lisääminen määrittää, että kyseinen mallimääritys on perustietomallin ER-muodon valittavissa vain silloin, kun kyseinen muoto suoritetaan sellaisen yrityksen hallinnassa, jolla on ranskalainen maa- tai aluekonteksti.

Voit lisätä useita maa- tai aluekoodeja yhteen ER-mallin yhdistämismäärityksen versioon. Tällä tavoin kyseisessä mallin yhdistämismäärityksessä olevia mallimäärityksiä voidaan käyttää siinä ER-muodossa, joka suoritetaan eri maa- tai aluekontekstin omaavien yritysten hallinnassa.

Huomaa, että maa- ja aluekoodiluettelo määritetään ER-mallin yhdistämismäärityksen kullekin versiolle, ja se voi vaihdella versioiden välillä.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Mallin yhdistämismäärityksen muokatun version viimeisteleminen

1.  Valitse **Konfiguroinnit**-sivun **Versiot**-pikavälilehdessä **Muuta tila**.

    > Muuta suunnitellun mallin yhdistämismäärityksen tila **luonnoksesta** **valmiiksi**, jotta ER-muodot voivat käyttää sitä.

2.  Valitse **Valmis**.
3.  Valitse **OK**.

Huomaa, että luotu konfiguraatio tallennetaan valmiina versiona 1.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportointimallin kartoituksen hallinta erillisissä sähköisen raportoinnin konfiguraatioissa](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[Maa- tai aluekontekstin ottaminen käyttöön](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>Määritin kaksi jaettua ER-mallin yhdistämismääritystä RCS:ssä ja merkitsin niistä toisten mallin oletusyhdistämismääritykseksi. Testasin mallimäärityksiä suorittamalla ER-muodon, joka luotiin samalle ER-tietomallin perusmääritykselle. Toin sitten koko ER-ratkaisun (ER-tietomalli, kaksi ER-mallin yhdistämismääritystä ja ER-muodon määritys) Financeen. Miksi saan virhesanoman, kun yritän suorittaa saman ER-muodon Financessa?
Mallin oletusmääritysasetus on ympäristökohtainen. Se on määritetty RCS:ssä mutta sitä ei ole viety Financeen. Tämän ER-muodon suorittaminen edellyttää, että merkitset myös toisen ER-mallin yhdistämismäärityksen mallin oletusyhdistämismääritykseksi Financessa.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>Määritin yhden mallimäärityksen jaetuksi mallimääritykseksi ja viimeistelin sen luonnosversion. Lisäsin sitten samaan tietomalliin uuden mallin yhdistämismäärityksen ja määritin sen kontekstiksi Ranskan. Miksi jaettu mallimääritys valitaan, kun suoritan ER-muodon, vaikka tämä ER-muoto käyttää oikeaa juurimääritelmää ja suoritus tehdään sellaisen yrityksen hallinnassa, jonka maa- tai aluekontekstina on Ranska.
Varmista, että jaettua mallin yhdistämismääritystä ei merkitä mallin oletusyhdistämismääritykseksi. Muussa tapauksessa sen prioriteetti on korkeampi yhdistämismääritystä valittaessa. Varmista myös, että ranskalainen mallin yhdistämismääritys otetaan huomioon, kun yhdistämismääritys valitaan ER-muodon suorituksen aikana. ER-mallin yhdistämismäärityksen voi valita vain, kun vähintään yksi seuraavista ehdoista täyttyy:
- Vähintään yhdellä ER-mallin yhdistämismäärityksen version tila on joko **Valmis** tai **Jaettu**. Siinä tapauksessa ER-muodon suorittamiseen käytetään versiota, jonka versionumero on korkein.
- ER-mallin yhdistämismäärityksen **Suorita luonnos** -asetus on otettu käyttöön. Siinä tapauksessa ER-muodon suorittamiseen käytetään versiota, jonka tila on **Luonnos**.
> **Suorita luonnos** -asetus on valittavissa kunkin ER-mallin yhdistämismäärityksen **Konfiguraatiot**-sivulla, kun **Suorita asetus** -ER-käyttäjäparametri on otettu käyttöön.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
