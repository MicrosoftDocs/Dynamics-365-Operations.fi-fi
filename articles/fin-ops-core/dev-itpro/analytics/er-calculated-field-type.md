---
title: Laskettu kenttä -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki
description: Tässä ohjeaiheessa käsitellään ER-tietolähteiden Laskettu kenttä -tyypin käyttöä.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f331401f8d191243f72961333e4f1dbe84d0be5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771326"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>Laskettu kenttä -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään sähköisen raportoinnin (ER) tietolähteiden suunnittelua **Laskettu kenttä** -tyypin avulla. Tietolähteessä voi olla ER-lauseke, jota voidaan suoritettaessa hallita niiden parametriargumenttien arvoilla, jotka on määritetty tätä tietolähdettä kutsuvassa sidonnassa. Jos kyseisen tietolähteelle määritetään parametrisoidut kutsut, voit käyttää yhtä tietolähdettä useissa sidonnoissa, mikä vähentää ER-mallimäärityksissä tai ER-muodoissa määritettävien tietolähteiden kokonaismäärää. Se myös yksinkertaistaa määritettyä ER-komponenttia, mikä puolestaan vähentää ylläpitokustannuksia ja muiden kuluttajien käyttökustannuksia.

## <a name="prerequisites"></a>Edellytykset
Tämän aiheen esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:

- Jonkin seuraavan roolin käyttöoikeus:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

- Sellaisen Regulatory Configuration Servicesin (RCS) käyttöoikeus, joka on valmisteltu samalle vuokralaiselle kuin Finance and Operations yhdessä seuraavista rooleista:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

Lataa [Microsoft Download Centerissä](https://go.microsoft.com/fwlink/?linkid=874684) pakattu zip-tiedosto **Laskettu kenttä -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki**. Se sisältää seuraavat ER-kokoonpanot, jotka on purettava ja tallennettava paikallisesti.

| **Sisältö**                           | **Tiedostonimi**                                        |
|---------------------------------------|------------------------------------------------------|
| Esimerkin ER-tietomallin konfigurointi    | Model to learn parameterized calls.version.1.xml     |
| Esimerkin ER-metadatan konfigurointi      | Metadata to learn parameterized calls.version.1.xml  |
| Esimerkin ER-mallikartoituksen konfigurointi | Mapping to learn parameterized calls.version.1.1.xml |
| Esimerkin ER-format-konfigurointi        | Format to learn parameterized calls.version.1.1.xml  |

## <a name="sign-in-to-your-rcs-instance"></a>Kirjautuminen RCS-esiintymään
Tällä esimerkissä luodaan määritys malliyritykselle Litware, Inc. Ensiksi on kuitenkin suoritettava RCS:ssä [Konfiguraation lähteiden luominen ja niiden merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet.

1. Valitse oletuskoontinäytössä **Sähköinen raportointi**.
2. Valitse **Raportointikonfiguraatiot**.
3. Tuo ladatut kokoonpanot RCS:ään seuraavassa järjestyksessä: tietomalli, metatiedot, mallin määritys, muoto. Tee seuraavat vaiheet kussakin ER-kokoonpanossa:

    1. Valitse **Vaihto**.
    2. Valitse **Lataa XML-tiedostosta**.
    3. Valitse ensin **Selaa** ja sitten tarvittava XML-muotoinen ER-kokoonpano.
    4. Valitse **OK**.

## <a name="review-the-provided-er-solution"></a>Annetun ER-ratkaisun tarkastelu

### <a name="review-model-mapping"></a>Mallin määrityksen tarkastelu

1. Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.
2. Valitse **Mapping to learn parameterized calls**.
3. Valitse **Suunnittelu**.
4. Valitse **Suunnittelu**.  
   
    Tämä ER-mallimääritys on suunniteltu seuraavia toimia varten:

    - **TaxTable**-taulussa olevan verokoodiluettelon (**Tax**-tietolähde) noutaminen.
    - **TaxTable**-taulussa olevan verotapahtumaluettelon (**Trans**-tietolähde) noutaminen:
    
        - Noudetun tapahtumaluettelon ryhmittely (**Gr**-tietolähde) verokoodin mukaan.
        - Ryhmitettyjen tapahtumien laskeminen verokoodikohtaisten koostettujen arvojen mukaan:

            - Veron perusarvojen summa.
            - Veroarvojen summa.
            - Käytetyn veroprosentin vähimmäisarvo.

    Tässä kokoonpanossa mallin yhdistäminen käyttää tälle mallille luotujen ja Finance and Operationsissa suoritettujen ER-muotojen perustietomallia. Tämän vuoksi **Tax**- ja **Gr**-tietolähteiden sisältö näkyy ER-muodoissa abstrakteina tietolähteinä.

    ![Tax- ja Gr-tietolähteet näkyvät mallimäärityksen suunnittelusivulla](media/er-calculated-field-type-01.png)

5.  Sulje **Mallimäärityksen sunnittelun** sivu.
6.  Sulje **Mallimääritys**-sivu.

### <a name="review-format"></a>Muodon tarkastelu

1. Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.
2. Valitse **Parametrisoitujen kutsujen oppimismuoto**.
3. Valitse **Suunnittelu**. Tämä ER-muoto on suunniteltu seuraavia toimia varten:

    - XML-muotoisen veroilmoituksen luominen.
    - Seuraavien verotustasojen näyttäminen veroilmoituksessa: normaali, alennettu ja ei mitään.
    - Useiden tietojen näyttäminen kustakin verotustasosta siten, että kunkin tason tiedoilla on eri numero.

    ![Muodon suunnittelutoiminto -sivu](media/er-calculated-field-type-02.png)

4. Valitse **Määritys**.
5. Laajenna **Malli**, **Tiedot** ja **Yhteenveto**. 

    Laskettu **Model.Data.Summary.Level** -kenttä sisältää lausekkeen, joka palauttaa verotustason koodin (**Normaali**, **Alennettu**, **Ei mitään** tai **Muu**) sellaisen verokoodin tekstiarvona, joka voidaan suorituksenaikaisesti noutaa **Model.Data.Summary**-tietolähteestä.

    ![Model to learn parameterized calls -tietomallin tiedot muodon suunnittelusivulla](media/er-calculated-field-type-03.png)

6. Laajenna **Model**.**Data2**.
7. Laajenna **Model**.**Data2.Summary2**.
   
    **Model**.**Data2.Summary2**-tietolähde on määritetty ryhmälle, jonka **Model.Data.Summary**-tietolähdetapahtuma erittelee verotustason mukaan (joka saadaan lasketusta **Model.Data.Summary.Level**-kentästä) ja laskee koosteet.

    ![Model.Data2.Summary2-tietolähteen tiedot muodon suunnittelusivulla](media/er-calculated-field-type-04.png)

8. Tarkista lasketut **Model**.**Data2.Level1**, **Model**.**Data2.Level2**- ja **Model**.**Data2.Level3**-kentät. **Model**.**Data2.Summary2**-tietueluettelo suodatetaan näiden laskettujen kenttien avulla palauttamaan vain tiettyä verotustasoa vastaavat tietueet.
9. Sulje **Muodon suunnittelija** -sivu.

## <a name="create-a-derived-format"></a>Johdetun luominen
Voit parantaa annettua muotoa lisäämällä yhden lasketun kentän suodattamaan tarvittavan verotustason sen sijaan, että käyttäisit kolmea aiemmin luotua kenttää: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ja **Model**.**Data2.Level3**. Tarvittava verotustaso voidaan määrittää sijainnissa, josta tämä uusi laskettu kenttä kutsutaan.

1. Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.
2. Valitse **Parametrisoitujen kutsujen oppimismuoto**.
3. Valitse **Luo konfiguraatio**.
4. Valitse **Johdettu nimestä: Parametrisoitujen kutsujen oppimismuoto, Microsoft**.
5. Anna **Nimi**-kentässä **Parametrisoitujen kutsujen oppimismuoto (mukautettu)**.
6. Valitse **Luo konfiguraatio**.

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>Tietueluettelon palauttavan parametrisoidun lasketun kentän luominen

### <a name="start-adding-a-new-calculated-field"></a>Aloittaminen lisäämällä uusi laskettu kenttä

1. Valitse **Suunnittelu**.
2. Laajenna kaikki muotokohteet valitsemalla **Laajenna/tiivistä**.
3. Valitse **Määritys**.
4. Laajenna **Malli**.
5. Valitse **Model.Data2**.
6. Valitse **Lisää**.
7. Valitse **Toiminnot\\Lasketut kentät**.
8. Kirjoita **Nimi**-kenttään **Tasot**.
9. Valitse **Muokkaa kaavaa**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Parametrin määrittäminen lasketun kentän lisäämistä varten

1. Valitse **Parametrit**.
2. Valitse **Uusi**.
3. Kirjoita **Nimi**-kenttään **Verotustaso**.
4. Kirjoita **Tyyppi**-kenttään **Merkkijono**.

    Parametrin argumenttityypin määrittämisessä voidaan käyttää vain primitiivisiä tietotyyppejä. Niissä tähän tarkoitukseen ei voi käyttää **Tietueluettelo**-, **Tietue**- ja **Valintalista**-tyyppejä.

    Yhdelle lasketulle kentälle voi määrittää enintään 8 parametria.

    ![Parametrin tietolähdeluettelo](media/er-calculated-field-type-05.png)

5. Valitse **OK**.

Tämän parametrin lisääminen määrittää ehdon, joka on oltava käytössä, jotta tämän lasketun kentän voi kutsua. Tämän lasketun kentän kutsuminen edellyttää, että **Verotustaso**-parametrin argumentti määritetään arvoksi **Merkkijono**-muodossa.

   Varmista, että määrität parametrit vain säilössä oleville lasketuille kentille (joko **Tietueluettelo**, **Tietue** tai **Säilö**).

   Määritetty parametri on käytettävissä tämän lasketun kentän tietolähdeluettelossa. Voit lisätä parametrin määritettyyn lausekkeeseen valitsemalla **Lisää tietolähde**.

   ![Tietolähdekentät](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Lasketun kentän lisäämän lausekkeen määrittäminen

1. Kirjoita **Resepti**-kenttään: 

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level =**
    
2. Valitse tietolähdeluettelossa **Verotustaso**-parametri.
3. Valitse **Lisää tietolähde**.
4. Viimeistele lauseke **Resepti**-kentässä muotoon:  

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Verotustaso')**

5. Valitse **Tallenna**.

    ![Tietolähdekentän tiedot](media/er-calculated-field-type-07.png)

6. Sulje **Reseptien suunnittelu** -sivu.

### <a name="finish-adding-a-new-calculated-field"></a>Uuden lasketun kentän lisäämisen viimeistely

- Valitse **OK**.

**Reseptien suunnittelu** -sivulla oleva määritetty parametrisoitu laskettu **Tasot**-kenttä edellyttää **Merkkijono**-argumenttia.

![Laajennettu lasketun kentän tasoluettelo](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a>Muodon elementtien sitominen määritetyn lasketun kentän avulla

1. Valitse laskettu kenttä valitsemalla **Model.Data2.Levels**.
2. Valitse **Statement.Taxation.Regular**-muotoelementti.
3. Valitse **Sido**.
4. Valitsemalla **Kyllä** voit vahvistaa käytössä olevan tietolähteen **Taso1** korvaamisen uudella tietolähteellä **Tasot** kaikissa valitun muotoelementin sisäkkäisissä muotoelementeissä.

    Kohdistettu sidonta on muodostettu parametrisoidun lasketun kentän kutsuna. Sidotun muotoelementin nimeä käytetään oletusarvoisesti parametrisoidun lasketun kentän argumenttina seuraavien ehtojen mukaisesti:

      - Laskettu kenttä on määritetty käyttämään yhtä parametria.
      - Kyseisen parametrin tietotyypiksi on määritetty **merkkijono**.

    Jos sidotun muotoelementin nimi on tyhjä, kyseisen elementin tietolähteen nimeä käytetään kohdistetussa sidonnassa.

5. Valitse **Statement.Taxation.Reduced**-muotoelementti.
6. Valitse **Sido**.
7. Valitsemalla **Kyllä** voit vahvistaa käytössä olevan tietolähteen **Taso2** korvaamisen uudella tietolähteellä **Tasot** kaikissa valitun muotoelementin sisäkkäisissä muotoelementeissä.
8. Valitse **Statement.Taxation.None**-muotoelementti.
9. Valitse **Sido**.
10. Valitsemalla **Kyllä** voit vahvistaa käytössä olevan tietolähteen **Taso3** korvaamisen uudella tietolähteellä **Tasot** kaikissa valitun muotoelementin sisäkkäisissä muotoelementeissä.

   Jos määrität verotustasoon viittaavan XML-elementin (kuten **Model.Data2.Levels("Alennettu")** tekstiarvona) parametrisoidun lasketun kentän argumentin, samaa ei tarvitse tehdä sisäkkäisille XML-määritteille, sillä niiden sidonnat perivät automaattisesti päätasolla määritetyn argumentin arvon (**Model.Data2.Levels.aggregated.Base**, ei siis **Model.Data2.Levels("Alennettu").aggregated.Base**).

Parametrisoidun lasketun kentän toistuvia kutsuja ei tueta.

Voit valita **Muokkaa reseptiä** ja muuta valitussa sidonnassa olevan parametrisoidun lasketun kentän oletusarvoista kohdistusta. Jos tämä argumentti puuttuu, seurauksena voi olla suorituksenaikaisia virheitä; käyttäjille ilmoitetaan tällaisesta tilanteesta, kun nykyinen muoto vahvistetaan.

![Vahvistuksen varoitusilmoitus](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a>Tietueen palauttavan parametrisoidun lasketun kentän luominen
Kun parametrisoitu laskettu kenttä palauttaa tietueen, tämän tietueen yksittäisten kenttien tukemista muotoelementteihin on tuettava. Tällaisissa tapauksissa ei ole pääsidontaa, joka sisältää parametrisoidun lasketun kentän kutsuvan argumentin arvon. Tämä arvo on määritettävä yksittäisen tietuen kentässä.

### <a name="start-adding-a-new-calculated-field"></a>Aloittaminen lisäämällä uusi laskettu kenttä

1. Valitse **Model.Data2**.
2. Valitse **Lisää**.
3. Valitse **Toiminnot\\Lasketut kentät**.
4. Kirjoita **Nimi**-kenttään **LevelRecord**.
5. Valitse **Muokkaa kaavaa**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Parametrin määrittäminen lasketun kentän lisäämistä varten

1. Valitse **Parametrit**.
2. Valitse **Uusi**.
3. Kirjoita **Nimi**-kenttään **Verotustaso**.
4. Kirjoita **Tyyppi**-kenttään **Merkkijono**.
5. Valitse **OK**.

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Lasketun kentän lisäämän lausekkeen määrittäminen

1. Kirjoita **Resepti**-kenttään  
    
    **FIRSTORNULL(\@.Levels(**

2. Valitse **Verotustaso**-parametri.
3. Valitse **Lisää tietolähde**.
4. Liitä **Resepti**-kentässä **'Verotustaso'))** tekstiin, jonka kirjoitit vaiheessa 1. Lauseke viimeistellään muotoon:  
    
    **FIRSTORNULL(\@.Levels('Verotustaso'))**

5. Valitse **Tallenna**.
6. Sulje **Reseptien suunnittelu** -sivu.

### <a name="finish-adding-a-new-calculated-field"></a>Uuden lasketun kentän lisäämisen viimeistely

-   Valitse **OK**.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>Muodon elementtien sitominen määritetyn lasketun kentän avulla

1. Valitse määritetty laskettu kenttä laajentamalla **Model.Data2.LevelRecord**.
2. Laajenna määritetyn lasketun kentän **Model.Data2.LevelRecord.aggregated**-säilö.
3. Valitse **Model.Data2.LevelRecord.aggregated.Base**-kenttä.
4. Valitse **Statement.Taxation.None**-muotoelementti.
5. Valitse **Poista sidonta**.
6. Valitse **Statement.Taxation.None.Base**-muotoelementti.
7. Valitse **Sido**.
8. Valitse **Muokkaa kaavaa**.
9. Muuta lauseke muotoon **Model.Data2.LevelRecord("Ei mitään").aggregated.Base**.

![Päivitetty lauseke](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>Käyttämättömien laskettujen kenttien poistaminen

1. Valitse **Model.Data2.Level1**.
2. Valitse **Poista**.
3. Valitse **Model.Data2.Level2**.
4. Valitse **Poista**.
5. Valitse **Model.Data2.Level3**.
6. Valitse **Poista**.
7. Valitse **Tallenna**.

  > [!NOTE]
  > Käytit samaa laskettua **Model.Data2.Levels**-kenttää useita kertoja muodon sidonnoissa. Yhden lasketun kentän käyttäminen ja ylläpitäminen on paljon helpompaa kuin useiden samankaltaisten kenttien käyttö ja ylläpito.

8. Sulje **Muodon suunnittelija** -sivu.

## <a name="complete-adjusted-version-of-a-derived-format"></a>Johdetun muodon korjatun version viimeisteleminen

1. Valitse **Versiot**-pikavälilehdessä **Muuta tila**.
2. Valitse **Valmis**.

## <a name="export-completed-version-of-a-derived-format"></a>Johdetun muodon valmiin version vieminen

1. Valitse kokoonpanopuussa **Parametrisoitujen kutsujen oppimismuoto (mukautettu)**.
2. Valitse **Version**-pikavälilehdessä valmis versio 1.1.1.
3. Valitse **Vaihto**.
4. Valitse **Vie XML-tiedostona**.
5. Tallenna ladattu kokoonpano paikallisesti XML-muodossa.

## <a name="test-er-formats"></a>ER-muotojen testaaminen 
Voit suorittaa alkuperäiset ja parannetut ER-muodot ja varmistaa tällä tavoin, että määritetyt parametrisoidut lasketut kentät toimivat oikein.

### <a name="import-er-configurations"></a>ER-konfiguraatioiden tuominen
Voit tuoda tarkistetut kokoonpanot RCS:stä käyttämällä **RCS**-tyyppistä ER-säilöä. Jos olet jo suorittanut ohjeaiheen [Sähköisen raportoinnin (ER) konfiguraatioiden tuonti Regulatory Configuration Services (RCS) -palvelusta](rcs-download-configurations.md) vaiheet, tuo aiemmin tässä aiheessa käsitellyt määritykset ympäristöön määritetyn ER-säilön avulla. Toimi muussa tapauksessa seuraavasti:

1. Valitse **DEMF**-yritys ja valitse oletuskoontinäytössä **Sähköinen raportointi**.
2. Valitse **Raportointikonfiguraatiot**.
3. Tuo kokoonpanot Microsoft Download Centeristä seuraavassa järjestyksessä: tietomalli, mallin määritys, muoto. Tee seuraavat vaiheet kussakin ER-kokoonpanossa:

    1. Valitse **Vaihto**.
    2. Valitse **Lataa XML-tiedostosta**.
    3. Valitse ensin **Selaa** ja sitten tarvittava XML-muotoinen ER-kokoonpano.
    4. Valitse **OK**.

4. Tuo RCS:stä viety **Parametrisoitujen kutsujen oppimismuoto (mukautettu)** -muodon valmis versio 1.1.1:

    1. Valitse **Vaihto**.
    2. Valitse **Lataa XML-tiedostosta**.
    3. Valitse ensin **Selaa** ja sitten paikallisesti tallennettu XML-muotoinen **Format to learn parameterized calls (mukautettu)** -tiedosto.
    4. Valitse **OK**.

### <a name="run-er-formats"></a>ER-muotojen suorittaminen

1. Laajenna kokoonpanopuussa **Model to learn parameterized calls** -tiedoston sisältö.
2. Valitse **Parametrisoitujen kutsujen oppimismuoto**.
3. Valitse ylimmässä valintanauhassa **Suorita**.
4. Tallenna paikallisesti luotu tuotos.
5. Valitse **Parametrisoitujen kutsujen oppimismuoto (mukautettu)**.
6. Valitse ylimmässä valintanauhassa **Suorita**.
7. Tallenna luotu tuotos paikallisesti. 
8. Vertaa luotujen tuotosten sisältöä.

## <a name="additional-resources"></a>Lisäresurssit
[Sähköisen raportoinnin (ER) kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)
