---
title: ER-muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja
description: Tässä ohjeaiheessa käsitellään sähköisen raportoinnin (ER) muotojen määrittämistä siten, että ne käyttävät yrityskohtaisesti määritettyjä parametreja.
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 629662d274d88d59c9b73a9d6b0d5c178331fe73
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351911"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>ER-muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Yleiskatsaus

Monissa suunniteltavissa sähköisen raportoinnin (ER) muodoissa tiedot on suodatettava käyttämällä esiintymän yrityskohtaista arvojoukkoa (kuten verokoodijoukkoa verotapahtumien suodattamiseen). Jos tällainen suodatustyyppi on määritetty ER-muodossa, yrityksestä riippuvaisia arvoja (kuten verokoodeja) käytetään tällä hetkellä ER-muodon lausekkeissa määrittämään tiedon suodatussäännöt. Niinpä ER-muoto on yrityskohtainen ja tarvittavien raporttien muodostaminen edellyttää, että alkuperäisestä ER-muodosta luodaan johdettu kopio kullekin yritykselle, jossa ER-muoto on suoritettava. Niinpä kutakin johdettua ER-muotoa on muokattava yrityskohtaisten arvojen tuontia varten, sen perusta on uusittava aina, kun alkuperäisinen (perus)versio on päivitetty, se on vietävä testiympäristöstä ja tuotava tuotantoympäristöön, jossa on otettava tuotantokäyttöön, ja niin edelleen. Tämän vuoksi on useita syitä, miksi tällaisen määritetyn ER-ratkaisun ylläpito on monimutkaista ja vie paljon aikaa:

-   Mitä useampia yrityksiä on, sittä useampia ER-muotomäärityksiä on ylläpidettäviä.
-   ER-määritysten ylläpito edellyttää yrityskäyttäjät osaavat käyttää sähköistä raportointia.

Sovelluskohtaisten ER-parametrien avulla tehokäyttäjät voivat määrittää ER-muodon tietojen suodattamisen abstraktin sääntöjoukon perusteella. Tämä sääntöjoukko voidaan määrittää käyttämään ER-muodossa käytettävissä olevia tietolähteitä. Yrityskäyttäjät voivat sitten määrittää ER-kehyksen ulkopuolelle ulottuvia todellisia sääntöjä käyttöliittymässä, joka muodostetaan automaattisesti. Se perustuu vastaavan ER-muodon asetuksiin ja niihin valitun yrityksen tietoihin, joita ER-muodon tietolähteet käyttävät. ER-muodolle määritetty sääntöjoukko voidaan viedä Dynamics 365 Finance (Finance) -esiintymän nykyisestä yrityksestä. Se voidaan sitten tuoda joko saman Finance-esiintymän toiseen yritykseen tai toiseen esiintymään saman ER-muodon sääntöjoukkona.

## <a name="prerequisites"></a>Edellytykset

Tämän ohjeaiheen esimerkkien käyttämistä varten tarvitset Regulatory Configuration Services (RCS) -esiintymän, joka on valmisteltu samalle vuokraajalle kuin Finance ja jossa roolina on jokin seuraavista:

- Sähköisen raportoinnin kehittäjä
- Sähköisen raportoinnin toiminnallinen konsultti
- Järjestelmänvalvoja

Ohjeaiheen [LASKETTU KENTTÄ -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki](er-calculated-field-type.md) vaiheiden suorittaminen on suositeltavaa. Jos olet jo tehnyt kyseiset vaiheet, voit ohittaa seuraavan osan, **ER-määritysten tuonti RCS:ään**, vaiheet.

## <a name="import-er-configurations-into-rcs"></a>ER-määritysten tuonti RCS:ään

Lataa ja tallenna seuraavat ER-konfiguraatiot paikallisesti.

| **Sisällön kuvaus**                        | **Tiedostonimi**                                        |
|------------------------------------------------|------------------------------------------------------|
| **ER-tietomallin** määritystiedostoesimerkki    | [Model to learn parameterized calls.version.1.xml](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| **ER-metatietojen** määritystiedostoesimerkki      | [Metadata to learn parameterized calls.version.1.xml](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| **ER-mallin yhdistämismäärityksen** määritystiedostoesimerkki | [Mapping to learn parameterized calls.version.1.1.xml](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| **ER-muodon** määritysesimerkki             | [Format to learn parameterized calls.version.1.1.xml](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

Kirjaudu seuraavaksi RCS-esiintymään.

Tässä esimerkissä luodaan määritys esimerkkiyritykselle Litware, Inc. Ennen menettelyn suorittamista sinun on suoritettava RCS:n ohjeaiheen [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheet.

1.  Valitse oletuskoontinäytössä **Sähköinen raportointi**.
2.  Valitse **Raportointikonfiguraatiot**.
3.  Tuo aiemmin RCS:ään ladatut ER-määritykset seuraavassa järjestyksessä: tietomalli, metatiedot, mallin yhdistämismääritys ja muoto. Luo kukin ER-määritys seuraavasti:

    1.  Valitse **Vaihto**.
    2.  Valitse **Lataa XML-tiedostosta**.
    3.  Valitse tarvittava XML-muotoinen ER-määritystiedosto valitsemalla **Selaa**.
    4.  Valitse **OK**.

## <a name="review-the-er-solution-that-is-provided"></a>Annetun ER-ratkaisun tarkastelu

1.  Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.
2.  Valitse **Parametrisoitujen kutsujen oppimismuoto**.
3.  Valitse **Suunnittelu**.
4.  Valitse **Laajenna/kutista**.

    **Parametrisoitujen kutsujen oppimismuoto** -ER-muoto on suunniteltu muodostamaan XML-muotoinen veroilmoitus, joka sisältää useita verotustasoja (normaali, alennettu ja ei mitään). Tasoilla olevien yksityiskohtien määrä vaihtelee.

    ![Useita ER-muodon tasoja, muoto, joka oppii parametrisoituja kutsuja.](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  Laajenna **Yhdistämismääritys**-välilehdessä **Malli**, **Tiedot** ja **Yhteenveto**.

    **Model.Data.Summary**-tietolähde palauttaa verotapahtumien luettelon. Tapahtumien yhteenveto tehdään verokoodin mukaan. Tässä tietolähteessä laskettu **Model.Data.Summary.Level**-kenttä on määritetty palauttamaan kunkin summatun tietueen verotason koodin. Jos verokoodi voidaan noutaa suorituksenaikaisesti **Model.Data.Summary**-tietolähteestä, laskettu kenttä sisältää verotustason koodin (**Normaali**, **Alennettu**, **Ei mitään** tai **Muu**) tekstiarvona. Lasketun **Model.Data.Summary.Level**-kentän avulla suodatetaan **Model.Data.Summary**-tietolähteen tietueet ja annetaan suodatetut tiedot kussakin verotason ilmaisevassa XML-elementissä käyttämällä kenttiä **Model.Data2.Level1**, **Model.Data2.Level2** ja **Model.Data2.Level3**.

    ![Model.Data.Summary-tietolähde – verotapahtumien luettelo.](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    Laskettu **Model.Data.Summary.Level**-kenttä on määritetty sisältämään ER-lauseke. Verokoodit (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** ja **InVAT0**) on koodattu pysyvästi tähän määritykseen. Tämän vuoksi tämä ER-muoto määräytyy sen yrityksen mukaan, jossa nämä verokoodit on määritetty.

    ![Laskettu Model.Data.Summary.Level-kenttä ja kovakoodatut verokoodit.](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    Toimi seuraavasti, jos haluat, että kussakin yrityksessä tuetaan eri verokoodijoukkoa:

    - Luo kullekin yritykselle ER-muodon johdettu versio.
    - Päivitä lasketun **Model.Data.Summary.Level**-kentän verokoodit yrityksen asetuksen perusteella.

6.  Sulje **Muodon suunnittelija** -sivu.

## <a name="create-a-derived-format"></a>Johdetun luominen

Voit sitten tukea samassa ER-muodossa yrityskohtaisia verokoodijoukkoja käyttämällä sovelluskohtaisia ER-parametreja.

1.  Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.
2.  Valitse **Parametrisoitujen kutsujen oppimismuoto**.
3.  Valitse **Luo konfiguraatio**.
4.  Valitse **Johdettu nimestä: Parametrisoitujen kutsujen oppimismuoto, Microsoft** -vaihtoehto.
5.  Kirjoita **Nimi**-kenttään **LE-tietojen haun oppimismuoto**.
6.  Valitse **Luo konfiguraatio**.

## <a name="configure-a-derived-format"></a>Johdetun muodon määrittäminen

### <a name="add-a-format-enumeration"></a>Muodon luetteloinnin lisääminen

Seuraavaksi lisätään uusi ER-muodon luettelointi. Tämän muodon luetteloinnin arvot näytetään yrityskäyttäjille, jotka määrittävät ER-muodossa käytettäville eri verotustasoille yrityskohtaiset verokoodijoukot.

1.  Valitse **Suunnittelu**.
2.  Valitse **Muodon luetteloinnit**.
3.  Valitse **Lisää**.
4.  Kirjoita **Nimi**-kenttään **Verotustasojen luettelo**.
5.  Valitse **Tallenna**.
6.  Valitse **Muodon luettelointiarvot** -välilehdessä **Lisää**.
7.  Kirjoita **Nimi**-kenttään **Normaali verotus**.
8.  Valitse **Lisää** uudelleen.
9.  Kirjoita **Nimi**-kenttään **Alennettu verotus**.
10. Valitse **Lisää** uudelleen.
11. Kirjoita **Nimi**-kenttään **Ei verotusta**.
12. Valitse **Lisää** uudelleen.
13. Kirjoita **Nimi**-kenttään **Muu**.

    ![Uusi tietue Muoto-valintalistasivulla.](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    Koska yrityskäyttäjät voivat käyttää eri kieliä yrityskohtaisten verokoodijoukkojen määrittämiseen, tämän luetteloinnin arvot kannattaa kääntää niille kielille, jotka on määritetty kyseisten käyttäjien ensisijaisiksi kieliksi Financessa.

14. Valitse **Ei verotusta** -tietue.
15. Napsauta **Otsikko**-kenttää.
16. Valitse **Käännä**.
17. Kirjoita **Tekstin käännös** -ruudun **Otsikon tunnus** -kenttään **LBL_LEVELENUM_NO**.
18. Kirjoita **Teksti oletuskielellä** -kenttään **No taxation**.
19. Valitse **Kieli**-kentässä **FI**.
20. Kirjota **Käännetty teksti** -kenttään **Ei verotusta**.
21. Valitse **Käännä**.

    ![Tekstin käännöksen esiin tuleva osa.](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. Valitse **Tallenna**.
23. Sulje **Muodon luetteloinnit** -sivu.

### <a name="add-a-new-lookup-data-source"></a>Uuden haun tietolähteen lisääminen

Seuraavaksi lisätään uusi tietolähde määrittämään, miten yrityskäyttäjät määrittävät yrityskohtaiset säännöt tunnistamaan oikean verotustason kullekin summatulle tapahtumatietueelle.

1.  Valitse **Yhdistämismääritys**-välilehdessä **Lisää**.
2.  Valitse **Muodon luetteloinnit\Haku**.

    Olet juuri määrittänyt, että jokainen sääntö, jonka yrityskäyttäjät määrittävät verotustason tunnistamiseen, palauttaa ER-muodon luetteloinnin arvon. Huomaa, että **Haku**-tietolähdetyypin käyttö on mahdollista **Tietomalli**- ja **Dynamics 365 for Operations** -lohkoissa **Muodon luettelointi** -lohkon lisäksi. Tämän vuoksi ER-tietomallin luettelointeja ja sovelluksen luettelointeja voi käyttää määrittämään niiden arvojen tyypin, joka palautetaan kyseisen tyypin tietolähteiksi. Lisätietoja **haku** tietolähteistä on kohdassa [Määritä hakutietolähteet käyttämään ER-sovelluskohtaisia parametreja](er-lookup-data-sources.md).
    
3.  Kirjoita **Nimi**-kenttään **Valitsin**.
4.  Valitse **Muodon luettelointi** -kentässä **Verotustasojen luettelo**.

    Määritit, että yrityskäyttäjän on valittava kunkin tässä tietolähteessä määritettävän säännön osalta palautetuksi arvoksi jonkin muodon luetteloinnin **Verotustasojen luettelo** -arvon.
    
5.  Valitse **Muokkaa hakua**.
6.  Valitse **Sarakkeet**.
7.  Laajenna **Malli**.
8.  Laajenna **Tiedot**.
9.  Laajenna **Vero**.
10. Valitse **Model.Data.Tax.Code**.
11. Valitse **Lisää**-painike (oikea nuoli).

    ![Sarakkeiden esiin tuleva osa.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    Määritit juuri, että yrityskäyttäjän on valittava yksi verokoodi kunkin tässä tietolähteessä verotustason tunnistukseen määritettävän säännön ehdoksi. **Model.Data.Tax**-tietolähde palauttaa sen verokoodiluettelon, jonka yrityskäyttäjä voi valita. Koska tässä tietolähteessä on **Nimi**-kenttä, verokoodin nimi näytetään jokaiselle verokoodin arvolle, jonka haku näyttää yrityskäyttäjälle.
    
12. Valitse **OK**.

    ![Valintojen suunnittelusivu.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    Yrityskäyttäjät voivat lisätä useita sääntöjä tietueina tähän tietolähteeseen. Kukin tietueen numerona on rivikoodi. Säännöt arvioidaan nousevan rivinumeron perusteella.

    Koska valitsit **Verokoodi**-kentän sääntöjen ehdoksi tässä haun tietolähteessä ja koska **Verokoodi** on määritetty **Merkkijono**-tietotyypin kentäksi, kukin sääntö arvioidaan suorituksenaikana vertaamalla tietolähteeseen välitettyä verokoodia tietolähteen tässä tietueessa määritettyyn verokoodiin.

    Kun määritysehtoa vastaava sääntö löytyy, tietolähde palauttaa **Haun tulos** -kentässä määritetyn säännön hakuarvon. Jos mitään sääntöä ei löydy, tapahtuu poikkeus, joka ilmaisee käyttäjälle, että nykyinen tietolähde ei voi palauttaa oikeaa arvoa.

13. Valitse **Tallenna**.
14. Sulje **Haun suunnittelija** -sivu.
15. Valitse **OK**.

    Huomaa, että lisäämäsi uusi tietolähde palauttaa verotustason muodon luetteloinnin **Verotustasojen luettelo** -arvon mille tahansa tietolähteeseen välitetylle verokoodille **Merkkijono**-tietotyypin **Koodi**-parametrin argumenttina.
    
    ![Muodon suunnittelusivu ja uusi tietolähde.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    Määritettyjen sääntöjen arviointi määräytyy niiden kenttien tietotyypin mukaan, jotka on valittu määrittämään kyseisten sääntöjen ehtoja. Kun valitset kentän, joka on määritetty joko **Numeerinen**- tai **Päivämäärä**-tietotyypin kentäksi, ehdot poikkeavat edellä käsitellyn **Merkkijono**-tietotyypin ehdoista. **Numeerinen**- ja **Päivämäärä**-kenttien säännöt on määritettävä arvoalueena. Säännön ehdon katsotaan sitten toteutuvan, kun tietolähteeseen välitetty arvo on määritetyllä alueella.
    
    Seuraavassa kuvassa on esimerkki tämän tyyppisestä määrityksestä. **Merkkijono**-tietotyypin **Model.Data.Tax.Code**-kentän lisäksi **Reaaliluku**-tietotyypin **Model.Tax.Summary.Base**-kenttää käytetään määrittämään haun tietolähteen ehtoja.
    
    ![Valintojen suunnittelusivu ja lisäsarakkeet.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    Koska tämän haun tietolähteeksi on valittu **Model.Data.Tax.Code**- ja **Model.Tax.Summary.Base**-kentät, jokainen tämän tietolähteen sääntö määritetään seuraavasti:
    
    -   Avautuvassa luettelossa muodon luetteloinnin **Verotustasojen luettelo** -arvo on valittava palautetuksi arvoksi.
    -   Verokoodi on annettava tämän säännön ehdoksi. Vain **Model.Data.Tax**-tietolähteestä saatavat verokoodit hyväksytään.
    -   Veron perusteen vähimmäis-ja enimmäisarvot on annettava tämän säännön ehdoiksi

    Tämän tietolähteen kukin sääntö arvioidaan suorituksen aikana seuraavasti:
    -   Vastasiko tietolähteeseen välitetyn **Merkkijono**-tietotyypin koodi säännön verokoodia?
    -   Sijoittuiko tietolähteeseen välitetyn **Reaaliluku**-tietotyypin arvon määritettyjen vähimmäis- ja enimmäisarvojen väliin?

    Säännön käyttö katsotaan mahdolliseksi, kun kumpikin ehto täyttyy.

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>Lisätyn haun tietolähteen otsikon kääntäminen

Koska yrityskäyttäjät voivat käyttää eri kieliä yrityskohtaisten verokoodijoukkojen määrittämiseen, lisättävän haun tietolähteen otsikko kannattaa kääntää, jota käyttäjät näkevät sen ensisijaisella kielellään kyseisellä sivulla.

1.  Valitse **Model.Data.Selector**-tietolähde.
2.  Valitse **Muokkaa**.
3.  Napsauta **Otsikko**-kenttää.
4.  Valitse **Käännä**.
5.  Kirjoita **Tekstin käännös** -ruudun **Otsikon tunnus** -kenttään **LBL_SELECTOR_DS**.
6.  Kirjoita **Teksti oletuskielellä** -kenttään **Select tax level by tax code**.
7.  Valitse **Kieli**-kentässä **FI**.
8.  Kirjoita **Käännetty teksti** -kenttään **Valitse verotustaso verokoodin perusteella**.
9.  Valitse **Käännä**.
10. Valitse **OK**.

    ![Tietolähteen ominaisuuksien esiin tuleva osa.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Uuden kentän lisääminen käyttämään määritettyä hakua

1.  Laajenna **Model.Data**.
2.  Valitse **Model.Data.Summary**.
3.  Valitse **Lisää**.
4.  Valitse **Toiminnot/Lasketut kentät**.
5.  Kirjoita **Nimi**-kenttään **LevelByLookup**.
6.  Valitse **Muokkaa kaavaa**.
7.  Kirjoita **Kaava**-kenttään **Model.Selector(Model.Data.Summary.Code)**.
8.  Valitse **Tallenna**.

    ![Model.Selector(Model.Data.Summary.Code)-kohteen lisääminen kaavan suunnittelusivulle.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  Sulje **Kaavaeditori**-sivu.
10. Valitse **OK**.

    ![Muodon suunnittelusivu ja uusi lisätty kaava.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    Huomaa, että lisäämäsi laskettu **LevelByLookup**-kenttä palauttaa verotustason kunkin summatun verotapahtumatietueen muodon luetteloinnin **Verotustasojen luettelo** -arvona. Tietueen verokoodi välitetään haun **Model.Selector**-tietolähteeseen, ja oikea verotustaso valitaan kyseisen tietolähteen sääntöjoukon avulla.

### <a name="add-a-new-format-enumeration-based-data-source&quot;></a>Uuden muodon luettelointiin perustuvan tietolähteen lisääminen

Seuraavaksi lisätään uusi tietolähde, joka viittaa aiemmin lisättyyn muodon luettelointiin. Tämän tietolähteen arvoja käytetään myöhemmin ER-muodon lausekkeessa.

1.  Valitse **Lisää pääkansio**.
2.  Valitse **Muodon luetteloinnit\Luettelointi**.
3.  Kirjoita **Nimi**-kenttään **TaxationLevel**.
4.  Valitse **Muodon luettelointi** -kentässä **Verotustasojen luettelo**.
5.  Valitse **Tallenna**.

### <a name=&quot;modify-an-existing-field-to-start-to-use-the-lookup&quot;></a>Aiemmin luodun kentän muokkaaminen aloittamaan haku

Seuraavaksi muokataan aiemmin luotua laskettua kenttää siten, että se käyttää määritettyä haun tietolähdettä palauttamaan oikean verotustason arvon verokoodin mukaisesti.

1.  Valitse **Model.Data.Summary.Level**.
2.  Valitse **Muokkaa**.
3.  Valitse **Muokkaa kaavaa**.

    Huomaa, että **Model.Data.Summary.Level**-kentän nykyinen lauseke sisältää seuraavat pysyvästi koodatut verokoodit:
    
    CASE (@.Code, &quot;VAT19&quot;, &quot;Regular&quot;, &quot;InVAT19&quot;, &quot;Regular&quot;, &quot;VAT7&quot;, &quot;Reduced&quot;, &quot;InVAT7&quot;, &quot;Reduced&quot;, &quot;THIRD&quot;, &quot;None&quot;, &quot;InVAT0&quot;, &quot;None&quot;, &quot;Other")

4.  Lisää **Kaava**-kenttään **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.

    ![ER-toiminnon suunnittelutoiminnon sivu.](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    Huomaa, että **Model.Data.Summary.Level**-kentän lauseke palauttaa nyt verotustason nykyisen tietueen verokoodin ja sen sääntöjoukon perusteella, jonka yrityskäyttäjä määrittää haun **Model.Data.Selector**-tietolähteessä.
    
5.  Valitse **Tallenna**.
6.  Sulje **Reseptien suunnittelu** -sivu.
7.  Valitse **OK**.
8.  Valitse **Tallenna**.
9.  Sulje **Muodon suunnittelutoiminto** -sivu.

## <a name="complete-the-draft-version-of-a-derived-format"></a>Johdetun muodon luonnosversion viimeisteleminen

1.  Valitse **Versiot**-pikavälilehdessä **Muuta tila**.
2.  Valitse **Valmis**.
3.  Valitse **OK**.

## <a name="export-completed-version-of-modified-format"></a>Muokatun muodon valmiin version vieminen

1.  Valitse määrityspuussa **LE-tietojen haun oppimismuoto**.
2.  Valitse **Versiot**-pikavälilehdessä tietue, jonka tila on **Valmis**.
3.  Valitse **Vaihto**.
4.  Valitse **Vie XML-tiedostona**.
5.  Valitse **OK**.
6.  Selain lataa **Format to learn how to lookup LE data.xml**-tiedoston. Tallenna tiedosto paikallisesti.

Toista edellä oleva vaiheet **LE-tietojen haun oppimismuoto** -muodon päänimikkeissä ja tallenna seuraavat tiedostot paikallisesti:

-   Format to learn parameterized calls.xml
-   Mapping to learn parameterized calls.xml
-   Model to learn parameterized calls.xml

Lisätietoja määritetyn **LE-tietojen haun oppimismuoto** -ER-muodon käyttämisestä siten, että sillä määritetään yrityskohtainen verokoodijoukko suodattamaan verotapahtumia eri verotustasoilla, on ohjeaiheen [ER-muodon parametrien määrittäminen yrityskohtaisesti](er-app-specific-parameters-set-up.md) ohjeissa.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin muodon parametrien määrittäminen yrityskohtaisesti](er-app-specific-parameters-set-up.md)

[Haun tietolähteiden määrittäminen ER-sovelluskohtaisten parametrien käyttämiseksi -ominaisuus](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
