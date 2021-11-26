---
title: Tuotannon käyttöliittymän tyylin määrittäminen
description: Tässä aiheessa selitetään, miten lomakkeiden ohjausobjekteja määritetään siten, että niihin sovelletaan tuotannon oletusarvoisia toteutustyylejä.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ef39dc6414f0afdadd4a4b5a41e1fb1fe60e4974
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790887"
---
# <a name="style-the-production-floor-execution-interface"></a>Tuotannon käyttöliittymän tyylin määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa selitetään, miten lomakkeiden ohjausobjekteja määritetään siten, että niihin sovelletaan tuotannon oletusarvoisia toteutustyylejä.

## <a name="forms-and-dialogs"></a>Lomakkeet ja valintaikkunat

Tyylejä voidaan soveltaa lomakkeessa tai valintaikkunassa vain, jos seuraavat vaatimukset täyttyvät:

- Jos lomakkeen pitäisi muistuttaa aiemmin luodun raportin edistymislomaketta, lomakkeen tai ikkunan nimen on alussa on oltava `JmgProductionFloorExecutionCustomInputDialog`.
- Lomake tai valintaikkuna voi sisältää tietolomakeosan. Jos siinä halutaan käyttää tyylejä, tietolomakeosan nimen alussa on oltava `JmgProductionFloorExecutionCustomDetailsDialog`.
- Jos lomakkeella tai valintaikkunalla on tarkoitus olla yksinkertainen näkymä, yksinkertaisen näkymän nimen alussa on oltava `JmgProductionFloorExecutionCustomDialog`. Esimerkkejä lomakkeista, joissa on yksinkertainen näkymä, ovat esimerkiksi aloituslomake ja epäsuoran toiminnon lomake.
- Kaikki valintaikkunan ohjausobjektit on määritettävä tässä aiheessa kuvatulla tavalla.

> [!IMPORTANT]
> Tämän luettelon kahdessa ensimmäisessä kohdassa mainitut ominaisuudet vaativat Supply Chain Managementin versiota 10.0.19 tai sitä uudempaa.

Tyylejä voidaan soveltaa **OK**-painikkeessa tai valintaikkunassa vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimen alussa on `OkButtonGroup`.

Tyylejä voidaan soveltaa **Peruuta**-painikkeessa tai valintaikkunassa vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimen alussa on `CancelButtonGroup`.

### <a name="header"></a>Ylätunniste

Seuraavassa kuvassa on tyypillinen lomakkeen tai ikkunan otsikko.

![Tyypillinen lomakkeen tai valintaikkunan otsikko](media/pfe-styles-header.png "Tyypillinen lomakkeen tai valintaikkunan otsikko")

Otsikot luodaan Visual Studiossa käyttämällä rakennetta, jollainen on esimerkiksi seuraavassa kuvassa.

![Otsikon luonnin tyypillinen koodirakenne](media/pfe-styles-header-code-structure.png "Otsikon luonnin tyypillinen koodirakenne")

Lisää tekstiä otsikkoon käyttämällä koodia, kuten seuraavassa esimerkissä.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Otsikon koodia kirjoitettaessa käytetään seuraavia sääntöjä:

- Pääryhmän nimen on oltava `TableRowHeaderGroup`.
- Kunkin (luettelomerkein erotelluin) tekstilohkon alussa on oltava `HeaderFieldWithSeparatorText`.
- Sukunimen alussa on oltava `HeaderFieldText`.
- `CaptionImage` voidaan ohittaa.

### <a name="progress-indicator"></a>Tilanneilmaisin

Jos tilanneilmaisin sisällytetään, se näkyy otsikon oikealla puolella. Seuraavassa kuvassa on tilanneilmaisin

![Tyypillinen tilanneilmaisin](media/pfe-styles-header-progress.png "Tyypillinen tilanneilmaisin")

Näytettävän tilanneilmaisimen tekstikentän nimenä on oltava `ShowProgress`.

## <a name="grid"></a>Ruudukko

Tyylejä sovelletaan automaattisesti. Erillistä määritystä ei tarvita.

Ruudukon tyylinä on oltava `TabularView` ja mukautetun lomakkeen `run()`-menetelmä on korvattava, koska uutta ruudukkoa ei vielä tueta. Lisää seuraava koodi.

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Päälomakkeen tietojen päivittämisessä voi olla käytössä `this.parmParentForm().updateLayout();` (tai jotain vastaavaa) toiminnon `click`-menetelmässä. (Esimerkkinä `JmgProductionFloorExecutionReportFeedbackAction`-luokka.) Varmista kuitenkin, että `parmDataSource` on määritetty uuden lomakkeen (`formCaller.parmDataSource(this.dataSource(1));`) `init`-menetelmässä. Esimerkkinä `JmgProductionFloorExecutionMainGrid`-lomake.

## <a name="card-view"></a>Korttinäkymä

Tyylejä voidaan soveltaa korttinäkymän ohjausobjekteihin vain, jos seuraavat vaatimukset täyttyvät:

- Kukin korttinäkymä kuuluu lomakeryhmään.
- Ryhmän nimen alussa on `CardGroup` (esimerkki `CardGroupJobsView`).

Seuraavassa kuvassa on korttinäkymä, jossa ei ole ohjausobjekteja.

![Korttinäkymä ilman elementtejä.](media/pfe-styles-empty-card.png)

Seuraavissa kuvissa on korttinäkymiä, joissa on ohjausobjekteja.

![Kortti, jossa Hz:t näyttäviä elementtejä.](media/pfe-styles-elements.png)

![Kortti, joka sisältää elementtejä ylläpitopyyntöä varten.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Käyntikortti

Tyylejä voidaan soveltaa käyntikortin ohjausobjekteihin vain, jos seuraavat vaatimukset täyttyvät:

- Kukin käyntikortti kuuluu lomakeryhmään.
- Ryhmän nimen alussa on `BusinessCardGroup` (esimerkki `BusinessCardGroupJobsList`).

Määritä käyntikortin seuraavat ominaisuudet:

- **Tyyli:** *list*
- **Laajennettu tyyli:** *cardList*
- **Monivalinta:** *Ei*
- **Näytä sarakeotsikot:** *Ei*

![Käyntikortti.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Valintanappi

Tyylejä voidaan soveltaa valintanappeihin vain, jos seuraavat vaatimukset täyttyvät:

- Kukin valintanappi kuuluu lomakeryhmään.
- Ryhmän nimen alussa on `RadioTextBelow` tai `RadioTextRight` sen mukaan, missä tekstin on tarkoitus tulla näkyviin.

Määritä valintanapin seuraavat ominaisuudet:

- **Vaihtopainike:** *Tarkistus*
- **Vaihtopainikkeen arvo:** *Käytössä*, jos valintapainike on tarkoitus valita, muuten *Pois*

Seuraavassa kuvassa näkyy esimerkki, jossa teksti näkyy valintanappien alapuolella.

![valintanapit, joissa teksti on alla.](media/pfe-styles-radio-text-below.png)

Seuraavassa kuvassa näkyy esimerkki, jossa teksti näkyy valintanappien oikealla puolella.

![Valintanapit, joissa teksti on oikealla puolella.](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Valintanapit Internet Explorerissa

Internet Explorer ei tue valintanappien tyylejä. Seuraava kuva osoittaa, miltä valintanapit näyttävät Internet Explorerissa.

![Valintanapit Internet Explorerissa.](media/pfe-styles-browser.png)

## <a name="buttons"></a>Napit

Tyylejä voidaan soveltaa painikkeisiin vain, jos seuraavat vaatimukset täyttyvät:

- Kukin painikeryhmä kuuluu lomakeryhmään. Kaikilla ryhmän painikkeilla on sama tyyli.
- Ryhmän nimeen ei kohdistu vaatimuksia.

Määritä painikkeiden seuraavat ominaisuudet:

- **Painikenäyttö:** *TextWithImageLeft*
- **Normaali kuva:** Tämä ominaisuus ei voi olla tyhjä. Käytä esimerkiksi *CoffeeScript*-komentosarjaa.
- **Teksti:** Tämä ominaisuus ei voi olla tyhjä. Käytä esimerkiksi arvoa *Aloita tauko*.
- **Leveys:** *Auto* tai *SizeToContent*
- **Korkeus:** *Auto* tai *SizeToContent*

### <a name="primary-button"></a>Ensisijainen painike

Tyylejä voidaan soveltaa ensisijaiseen painikkeeseen vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimen alussa on `DefaultButtonGroup` tai `PrimaryButtonGroup` (esimerkiksi `DefaultButtonGroup10`).

![Ensisijainen painike.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Toissijainen painike

Tyylejä voidaan soveltaa toissijaiseen painikkeeseen vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimi on **Oikea paneeli** tai ryhmän nimen alussa on `SecondaryButtonGroup`.

![Toissijainen painike.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Kolmannen ryhmän painike

Tyylejä voidaan soveltaa kolmannen ryhmän painikkeeseen vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimi on **Vasen paneeli** tai ryhmän nimen alussa on `ThirdButtonGroup`.

![Kolmannen ryhmän painike.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Neljännen ryhmän painike

Tyylejä voidaan soveltaa neljännen ryhmän painikkeeseen vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimen alussa on `FourthButtonGroup`.

Määritä painikkeen seuraavat ominaisuudet:

- **Painikenäyttö:** *TextOnly*
- **Normaali kuva:** Tämän ominaisuuden on oltava tyhjä.
- **Teksti:** Tämä ominaisuus ei voi olla tyhjä. Käytä esimerkiksi arvoa *Näytä* tai *Muokkaa*.
- **Leveys:** *Automaattinen*
- **Korkeus:** *Automaattinen*

![Neljännen ryhmän painike.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Litteä painike

Tyylejä voidaan soveltaa litteään painikkeeseen vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimen alussa on `FlatButtonGroup`.

Määritä painikkeen seuraavat ominaisuudet:

- **Painikenäyttö:** *ImageOnly*
- **Normaali kuva:** Tämä ominaisuus ei voi olla tyhjä. Käytä esimerkiksi *CoffeeScript*-komentosarjaa.
- **Teksti:** Tämän ominaisuuden on oltava tyhjä.
- **Leveys:** *Auto* tai *SizeToContent*
- **Korkeus:** *Auto* tai *SizeToContent*

![Litteä painike.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Jatka-painike

Tyylejä voidaan käyttää jakamispainikkeessa vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimen alussa on `ContinueButtonGroup`.

Määritä painikkeen seuraavat ominaisuudet:

- **Painikenäyttö:** *ImageOnly*
- **Normaali kuva:** *Eteenpäin*
- **Teksti:** Tämän ominaisuuden on oltava tyhjä.
- **Leveys:** *Auto* tai *SizeToContent*
- **Korkeus:** *Auto* tai *SizeToContent*

![Jatka-painike.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Yhdistelmäruutu

Yhdistelmäruutu on kolmen ohjausobjektin eli syötön ohjausobjektin, syötön ohjausobjektin tyhjentävän painikkeen ja haun suorittavan painikkeen yhdistelmä.

Tyylejä voidaan soveltaa yhdistelmäruutuun vain, jos seuraavat vaatimukset täyttyvät:

- Yhdistelmäruutu kuuluu lomakeryhmään.
- Ryhmän nimen alussa on `Combobox`.
- Ryhmän sisällä ensimmäinen ohjausobjekti `AxFormStringControl`. Tämä ohjausobjekti näyttää nykyisen arvon, ja käyttäjä syöttää vaaditun arvon siihen.
- Toinen ohjausobjekti on `CommonButton`, ja sen nimen alussa on `ClearButton`. Tämän painikkeen on sisällettävä koodi, jossa `enable`-ominaisuutta käytetään painikkeen näyttämiseen tai piilottamiseen. Jos esimerkiksi haluat näyttää tai piilottaa **Tyhjennä**-painikkeen, kun käyttäjä kirjoittaa tietoja syöttöohjausobjektiin, voit käyttää seuraavaa koodia.

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    Sinulla on oltava yksi menetelmä, jossa tiedot määritetään syöttöohjausobjektissa. Ota **Tyhjennä**-painike käyttöön tässä menetelmässä. Esimerkki:

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    Käytä seuraavaa koodia **Tyhjennä**-painikkeen `clicked`-menetelmään.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Määritä syöttöohjausobjektin `AxFormStringControl` arvo, kun lomake alustetaan `init`-menetelmällä. Jos arvo ei ole tyhjä, ota **Tyhjennä**-painike käyttöön. Jos arvo on tyhjä, poista **Tyhjennä**-painike käytöstä.

- Kolmas ohjausobjekti on `CommonButton`, ja sen nimen alussa on `SearchButton`.

Seuraavassa kuvassa on kaksi yhdistelmäruutuohjausobjektia. Vasemmanpuoleinen yhdistelmäruutu sisältää tyhjän tekstiruudun, ja **Tyhjennä**-painike on pois käytöstä. Oikeanpuoleisen yhdistelmäruudun tekstiruudussa on tekstiä, ja **Tyhjennä**-painike on käytössä.

![Yhdistelmäruudut Tyhjennä-painikkeella ja ilman sitä.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Pikasuodatin

Pikasuodatinohjausobjekti lisää sivulle hakukentän. Voit käyttää tyylejä pikasuodattimessa, jos seuraavat vaatimukset täyttyvät:

- Pikasuodatin kuuluu lomakeryhmään.
- Ryhmän nimen alussa on `SearchInputGroup`.
- Ryhmän sisällä ensimmäinen ohjausobjekti `QuickFilter`. (Käyttäjä syöttää tässä ohjausobjektissa hakumerkkijonon.)
- Toinen ohjausobjekti on `FormStaticTextControl`, jonka nimi on `NumberOfResults`. (Tämä ohjausobjekti on valinnainen. Jos sitä käytetään, siinä näkyy löydettyjen kohteiden määrä.)
- Kolmas ohjausobjekti on `CommonButton`, ja sen nimen alussa on `ClearButton`.

Seuraavassa kuvassa on kaksi pikasuodatinohjausobjektia. Vasemmanpuoleisessa pikasuodattimessa on tyhjä pikasuodatin, ja tulosten määrä ei ole näkyvissä. Oikeanpuoleinen pikasuodatin sisältää hakumerkkijonon ja näyttää tulosten määrän.

![Esimerkki pikasuodatinohjausobjektista hakumerkkijonon kanssa ja ilman sellaista.](media/pfe-styles-quick-filter.png "Esimerkki pikasuodatinohjausobjektista hakumerkkijonon kanssa ja ilman sellaista")

## <a name="center-align-elements-on-a-tab"></a>Välilehden elementtien keskittäminen

Elementtien kohdistaminen välilehden keskelle edellyttää, että ryhmän nimen alussa on `TabContentGroup` ja että ryhmässä on seuraavat ominaisuudet:

- **Leveystila:** `SizeToAvailable`
- **Korkeustila:** `SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Ruudukon tieto-osan ja pikasuodattimen kohdistaminen

Kun mukautettu ruudukko, tieto-osa ja pikasuodatin järjestetään muistuttamaan vakiorakennetta, seuraavat seikat on muistettava niitä yhdistettäessä:

- Jos ruudukossa on pikasuodatin, sekä ruudukon että pikasuodattimen on oltava sen ryhmän sisällä, jonka nimen alussa on oltava `GridGroup`.
- Jos tieto-osassa halutaan käyttää tyylejä, ryhmän nimen alussa on oltava `DetailInformationGroup`.

Seuraavassa kuvassa on tyypillinen ruudukko, jossa on pikasuodatin ja tieto-osa oikealla.

![Tyypillinen pikasuodattimen ja tieto-osan sisältävä ruudukko](media/pfe-styles-align-grid.png "Tyypillinen pikasuodattimen ja tieto-osan sisältävä ruudukko")

Ruudukko, tieto-osa ja pikasuodatin voidaan luoda Visual Studiossa käyttämällä rakennetta, jollainen on esimerkiksi seuraavassa kuvassa.

![Tyypillinen ruudukon, tieto-osan ja pikasuodattimen kohdistava koodirakenne](media/pfe-styles-header-code-structure2.png "Tyypillinen ruudukon, tieto-osan ja pikasuodattimen kohdistava koodirakenne")

## <a name="additional-resources"></a>Lisäresurssit

- [Tuotannon käyttöliittymän mukauttaminen](production-floor-execution-customize.md)
- [Tuotannon käyttöliittymän suunnitteleminen](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
