---
title: Tuotannon käyttöliittymän tyylin määrittäminen
description: Tässä aiheessa selitetään, miten lomakkeiden ohjausobjekteja määritetään siten, että niihin sovelletaan tuotannon oletusarvoisia toteutustyylejä.
author: johanhoffmann
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 32e49458f6ea7c484bc4200e414d930381b31891
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651979"
---
# <a name="style-the-production-floor-execution-interface"></a>Tuotannon käyttöliittymän tyylin määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa selitetään, miten lomakkeiden ohjausobjekteja määritetään siten, että niihin sovelletaan tuotannon oletusarvoisia toteutustyylejä.

## <a name="forms-and-dialogs"></a>Lomakkeet ja valintaikkunat

Tyylejä voidaan soveltaa lomakkeessa tai valintaikkunassa vain, jos seuraavat vaatimukset täyttyvät:

- Jos lomakkeen pitäisi muistuttaa olemassa olevaa edistymisen raportointilomaketta, lomakkeen tai valintaikkunan nimen on alettava **JmgProductionFloorExecutionCustomInputDialog**.
- Lomake tai valintaikkuna voi sisältää tietolomakeosan. Jos haluat käyttää siihen tyylejä, tietolomakeosan nimen on alettava **JmgProductionFloorExecutionCustomDetailsDialog**.
- Jos lomakkeella tai valintaikkunalla on tarkoitus olla yksinkertainen näkymä, yksinkertaisen näkymän nimen on alettava **JmgProductionFloorExecutionCustomDialog**. Esimerkkejä lomakkeista, joissa on yksinkertainen näkymä, ovat esimerkiksi aloituslomake ja epäsuoran toiminnon lomake.
- Kaikki valintaikkunan ohjausobjektit on määritettävä tässä aiheessa kuvatulla tavalla.

> [!IMPORTANT]
> Tämän luettelon kahdessa ensimmäisessä kohdassa mainitut ominaisuudet vaativat Supply Chain Managementin versiota 10.0.19 tai sitä uudempaa.

Tyylejä voidaan soveltaa **OK**-painikkeessa tai valintaikkunassa vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimi alkaa **OkButtonGroup**.

Tyylejä voidaan soveltaa **Peruuta**-painikkeessa tai valintaikkunassa vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimi alkaa **CancelButtonGroup**.

## <a name="grid"></a>Ruudukko

Tyylejä sovelletaan automaattisesti. Erillistä määritystä ei tarvita.

## <a name="card-view"></a>Korttinäkymä

Tyylejä voidaan soveltaa korttinäkymän ohjausobjekteihin vain, jos seuraavat vaatimukset täyttyvät:

- Kukin korttinäkymä kuuluu lomakeryhmään.
- Ryhmän nimi alkaa **CardGroup** (esimerkiksi **CardGroupJobsView**).

Seuraavassa kuvassa on korttinäkymä, jossa ei ole ohjausobjekteja.

![Korttinäkymä ilman elementtejä.](media/pfe-styles-empty-card.png)

Seuraavissa kuvissa on korttinäkymiä, joissa on ohjausobjekteja.

![Kortti, jossa Hz:t näyttäviä elementtejä.](media/pfe-styles-elements.png)

![Kortti, joka sisältää elementtejä ylläpitopyyntöä varten.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Käyntikortti

Tyylejä voidaan soveltaa käyntikortin ohjausobjekteihin vain, jos seuraavat vaatimukset täyttyvät:

- Kukin käyntikortti kuuluu lomakeryhmään.
- Ryhmän nimi alkaa **BusinessCardGroup** (esimerkiksi **BusinessCardGroupJobsList**).

Määritä käyntikortin seuraavat ominaisuudet:

- **Tyyli**: **luettelo**
- **Laajennettu tyyli**: **cardList**
- **Monivalinta**: **Ei**
- **Näytä sarakeotsikot**: **Ei**

![Käyntikortti.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Valintanappi

Tyylejä voidaan soveltaa valintanappeihin vain, jos seuraavat vaatimukset täyttyvät:

- Kukin valintanappi kuuluu lomakeryhmään.
- Ryhmän nimi alkaa **RadioTextBelow** tai **RadioTextRight** sen mukaan, missä tekstin on tarkoitus tulla näkyviin.

Määritä valintanapin seuraavat ominaisuudet:

- **Vaihtopainike**: **Tarkistus**
- **Arvonvaihto**: **Päällä**, jos valintapainike on tarkoitus valita, muuten **Pois**

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

- **Painikenäyttö**: **TextWithImageLeft**.
- **Normaali kuva**: Tämä ominaisuus ei voi olla tyhjä. Käytä esimerkiksi **CoffeeScript**-komentosarjaa.
- **Teksti**: Tämä ominaisuus ei voi olla tyhjä. Käytä esimerkiksi arvoa **Aloita tauko**.
- **Leveys**: **Automaattinen**.
- **Korkeus**: **Automaattinen**.

### <a name="primary-button"></a>Ensisijainen painike

Tyylejä voidaan soveltaa ensisijaiseen painikkeeseen vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimi alkaa **DefaultButtonGroup** tai **PrimaryButtonGroup** (esimerkiksi **DefaultButtonGroup10**).

![Ensisijainen painike.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Toissijainen painike

Tyylejä voidaan soveltaa toissijaiseen painikkeeseen vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimi on **Oikeanpuoleinen paneeli** tai ryhmän nimi alkaa **SecondaryButtonGroup**.

![Toissijainen painike.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Kolmannen ryhmän painike

Tyylejä voidaan soveltaa kolmannen ryhmän painikkeeseen vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimi on **Vasen paneeli** tai ryhmän nimi alkaa **ThirdButtonGroup**.

![Kolmannen ryhmän painike.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Neljännen ryhmän painike

Tyylejä voidaan soveltaa neljännen ryhmän painikkeeseen vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimi alkaa **FourthButtonGroup**.

Määritä painikkeen seuraavat ominaisuudet:

- **Painikenäyttö**: **TextOnly**.
- **Normaali kuva**: Tämän ominaisuuden on oltava tyhjä.
- **Teksti**: Tämä ominaisuus ei voi olla tyhjä. Käytä esimerkiksi arvoa **Näytä** tai **Muokkaa**.
- **Leveys**: **Automaattinen**.
- **Korkeus**: **Automaattinen**.

![Neljännen ryhmän painike.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Litteä painike

Tyylejä voidaan soveltaa litteään painikkeeseen vain, jos seuraavat vaatimukset täyttyvät:

- Painike kuuluu lomakeryhmään.
- Ryhmän nimi alkaa **FlatButtonGroup**.

Määritä painikkeen seuraavat ominaisuudet:

- **Painikenäyttö**: **ImageOnly**.
- **Normaali kuva**: Tämä ominaisuus ei voi olla tyhjä. Käytä esimerkiksi **CoffeeScript**-komentosarjaa.
- **Teksti**: Tämän ominaisuuden on oltava tyhjä.
- **Leveys**: **Automaattinen**.
- **Korkeus**: **Automaattinen**.

![Litteä painike.](media/pfe-styles-flat-button.png)

## <a name="combo-box"></a>Yhdistelmäruutu

Yhdistelmäruutu on kolmen ohjausobjektin eli syötön ohjausobjektin, syötön ohjausobjektin tyhjentävän painikkeen ja haun suorittavan painikkeen yhdistelmä.

Tyylejä voidaan soveltaa yhdistelmäruutuun vain, jos seuraavat vaatimukset täyttyvät:

- Yhdistelmäruutu kuuluu lomakeryhmään.
- Ryhmän nimi alkaa **Combobox**.
- Ryhmän sisällä ensimmäinen ohjausobjekti on tyyppiä **AxFormStringControl**. Tämä ohjausobjekti näyttää nykyisen arvon, ja käyttäjä syöttää vaaditun arvon siihen.
- Toinen ohjausobjekti on **CommonButton**-ohjausobjekti, ja sen nimi alkaa **ClearButton**. Tämän painikkeen on sisällettävä koodi, jossa **ota käyttöön** -ominaisuutta käytetään painikkeen näyttämiseen tai piilottamiseen. Jos esimerkiksi haluat näyttää tai piilottaa **Tyhjennä**-painikkeen, kun käyttäjä kirjoittaa tietoja syöttöohjausobjektiin, voit käyttää seuraavaa koodia.

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

    Käytä seuraavaa koodia **Tyhjennä**-painikkeen **napsautettu**-menetelmään.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Määritä syöttöohjausobjektin **AxFormStringControl** arvo, kun lomake alustetaan **init**-menetelmällä. Jos arvo ei ole tyhjä, ota **Tyhjennä**-painike käyttöön. Jos arvo on tyhjä, poista **Tyhjennä**-painike käytöstä.

- Kolmas ohjausobjekti on **CommonButton**-ohjausobjekti, ja sen nimi alkaa **SearchButton**.

Seuraavassa kuvassa on kaksi yhdistelmäruutuohjausobjektia. Vasemmanpuoleinen yhdistelmäruutu sisältää tyhjän tekstiruudun, ja **Tyhjennä**-painike on pois käytöstä. Oikeanpuoleisen yhdistelmäruudun tekstiruudussa on tekstiä, ja **Tyhjennä**-painike on käytössä.

![Yhdistelmäruudut Tyhjennä-painikkeella ja ilman sitä.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Pikasuodatin

Pikasuodatinohjausobjekti lisää sivulle hakukentän. Voit käyttää tyylejä pikasuodattimessa, jos seuraavat vaatimukset täyttyvät:

- Pikasuodatin kuuluu lomakeryhmään.
- Ryhmän nimi alkaa **SearchInputGroup**.
- Ryhmän sisällä ensimmäinen ohjausobjekti on tyyppiä **QuickFilter**. (Käyttäjä syöttää tähän hakumerkkijonon.)
- Toinen ohjausobjekti on **FormStaticTextControl**, jonka nimi on **NumberOfResults**. (Tämä on valinnainen, ja siinä näkyy löydettyjen kohteiden määrä, jos sitä käytetään.)
- Kolmas ohjausobjekti on **CommonButton**-ohjausobjekti, jonka nimi alkaa **ClearButton**.

Seuraavassa kuvassa on kaksi pikasuodatinohjausobjektia. Vasemmanpuoleisessa pikasuodattimessa on tyhjä pikasuodatin, ja tulosten määrä ei ole näkyvissä. Oikeanpuoleinen pikasuodatin sisältää hakumerkkijonon ja näyttää tulosten määrän.

![Esimerkki pikasuodatinohjausobjektista hakumerkkijonon kanssa ja ilman sellaista.](media/pfe-styles-quick-filter.png "Esimerkki pikasuodatinohjausobjektista hakumerkkijonon kanssa ja ilman sellaista")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
