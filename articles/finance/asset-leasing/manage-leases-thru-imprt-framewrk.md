---
title: Vuokrausten hallinta vuokrauksen tuonnin kehyksen kautta
description: Tässä ohjeaiheessa kerrotaan, miten vuokrauksen tuonnin kehystä käytetään useiden vuokrausten muokkaamisessa kerralla.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 26fb195ff18dc0c86d3546b782265043c2c78bf4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819791"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Vuokrausten hallinta vuokrauksen tuonnin kehyksen kautta

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten vuokrauksen tuonnin kehystä käytetään useiden vuokrausten muokkaamisessa yhdessä vaiheessa. Tämän ominaisuuden käyttäminen säästää aikaa, ja voit myös varmistaa tarkat oikaisut vähentämällä inhimillisten virheiden mahdollisuutta. Lisäksi tämä ominaisuus voi yhdistää Microsoft Dynamics 365 Financen ulkoisiin tietoentiteetteihin. Näin voit ladata tietoja tehokkaasti.

Seuraavia tietoentiteettejä voidaan käyttää resurssin vuokrauksen yhdistämisessä ulkoisiin järjestelmiin:

- Vuokran valmistelu
- Maksusopimusten valmistelu
- Toimeenpantava sopimusten valmistelu

Tuontiprosessin avulla voit oikaista vuokrasopimusta, päivittää muita kuin taloudellisia tietoja ja lisätä uusia vuokrasopimuksia. Voit tarkastella ja muokata vuokraustietoja ennen tuontia.

Järjestelmä voi suorittaa seuraavat kolme prosessia vuokrauksen tuontiohjelman kautta.

| Käsittelyn tyyppi  | kuvaus |
|---------------|-------------|
| Tietueen lisääminen    | Siirretyt vuokrasopimukset, joilla on tämä prosessityyppi, luovat vuokrasopimuksen järjestelmään. Aikataulu on vahvistettava manuaalisesti, ja alkuperäisen tuloutuksen kirjauskansiovienti on kirjattava manuaalisesti siirron jälkeen. |
| Päivitä tietue | Siirretyt vuokrasopimukset, joilla tämä prosessityyppi, päivittävät järjestelmässä jo olevan vuokrasopimuksen kenttien arvot. Vain kentät, jotka on valittu **Kenttien valinnan päivittäminen** -sivulla, päivitetään. Muut kuin taloushallinnon kentät kannattaa valita **Kenttien valinnan päivittäminen** -sivulla, koska tämä prosessityyppi ei oikaise vuokrasopimusta. |
| Säädä tietuetta | Siirretyt vuokrasopimukset, joilla on tämä prosessityyppi, muokkaavat vuokrasopimusta. Tämä oikaisu aiheuttaa vuokrasopimuksen rahoitusleasingsopimuksen muokkauksen. Kun vuokrasopimus on käsitelty, järjestelmä luo uuden maksuaikataulun käyttämällä vuokrasopimuksen tuontiohjelman uusia tietoja. Järjestelmä ei vahvista maksuaikataulua tai kirjaa oikaisukirjauskansiovientiä. |

Kun tiedot on ladattu **Tietojen hallinta** -työtilan avulla, avaa **Tuonnin otsikko** -sivu (**Resurssin vuokraus \> Vuokrauksen tuonnin kehys \> Tuonnin otsikko**). Tällä sivulla luetellaan kaikki kolmen aiemmin mainitun tietoentiteetin tuonnit.

Jos haluat tarkastella vuokrasopimuksen väliaikaisia tietoja ennen käsittelyn suorittamista, valitse **Väliaikaiset tiedot**.

Vertailutoiminnon avulla voit vertailla tuotavaa tietuetta vastaavaan järjestelmän tietueeseen. Jos haluat verrata yksittäisen vuokrasopimuksen tietuetta, valitse vuokrasopimus ja valitse sitten **Vertaa**. Tee tämä vaihe, jos haluat luoda **Erot**-raportin ennen vuokrasopimustietueiden siirtoa. Vertailutoiminto vertaa väliaikaisten tietojen arvoja järjestelmässä olevien vuokrasopimusten arvoihin.

> [!NOTE]
> Vertailutoiminto ei toimi vuokrasopimuksissa, joiden prosessityyppi on **Lisää tietue**, koska vuokrasopimus ei sisällä vertailtavia kohteita.
>
> Jos haluat vertailla useita vuokrasopimuksia kerralla, siirry kohtaan **Resurssin vuokraus \> Vuokrauksen tuonnin kehys \> Kausittainen \> Vertaa** ja valitse **Vertaa**.

Voit tarkastella kaikkien entiteettien eroja järjestelmässä olevien tietojen ja väliaikaisten taulukoiden tietojen välillä. Valitse kunkin väliaikaisen taulukon entiteetin **Katso erot** -kohta. Näkyviin tulevassa valintaikkunassa näkyy valittu arvo ja ehdotettu väliaikainen arvo.

Voit myös päivittää väliaikaisen arvon muuttamalla sitä **Uusi arvo** -sarakkeessa ja valitsemalla sitten **Päivitä väliaikainen arvo**.

Voit vahvistaa vuokrasopimukset ja varmistaa, että ne tietueet voidaan tuoda järjestelmään ilman virheitä. Ennen kuin vuokrasopimustietue siirretään, järjestelmä suorittaa useita tarkistuksia. Niiden avulla varmistetaan, että tietueen tuonti onnistuu. Voit vahvistaa yksittäisen vuokrasopimuksen valitsemalla **Vahvista**.

> [!NOTE]
> Jos haluat vahvistaa useita vuokrasopimuksia kerralla, siirry kohtaan **Resurssin vuokraus \> Vuokrauksen tuonnin kehys \> Kausittainen \> Vahvista** ja valitse **Vertaa**.

Voit käsitellä yksittäistä vuokrasopimusta valitsemalla **Siirrä vuokrasopimustietueet** **Tuonnin otsikko** -sivulla. Kun vuokrasopimus siirretään, järjestelmä suorittaa toiminnon, joka on määritetty **Prosessityyppi**-kentässä.

> [!NOTE]
> Jos haluat vahvistaa useita vuokrasopimuksia kerralla, siirry kohtaan **Resurssin vuokraus \> Vuokrauksen tuonnin kehys \> Kausittainen \> Vahvista** ja valitse **Vertaa**.

Kun vuokrasopimuksia verrataan, voit tarkastella kunkin tuonnin tunnukseen sisältyvän vuokrasopimuksen erot suorittamalla raportin. Jos haluat suorittaa yhden vuokrasopimuksen raportin, valitse kyseinen vuokrasopimus väliaikaisista tiedoista ja valitse sitten **Vertaile ja tarkastele raporttia \> Erojen raportti**.

> [!NOTE]
> Jos haluat vahvistaa useita vuokrasopimuksia kerralla, siirry kohtaan **Resurssin vuokraus \> Kyselyt ja raportit \> Erojen raportti** ja valitse **Vertaa**.

## <a name="set-up-update-fields"></a>Kenttien päivittämisen määrittäminen

Jos käytät vuokrauksen tuonnin kehystä vuokrasopimusten päivittämisessä ja prosessityyppi on **Päivitä tietue**, voit valita tietyt kentät päivittämistä varten.

1. Siirry kohtaan **Resurssin vuokraus \> Vuokrauksen tuonnin kehys \> Asetus \> Päivitä kenttien valinta**.
2. Valitse näkyviin tulevalla sivulla päivitettävät kentät ja siirrä ne sitten **Valitut kentät** -luetteloon vihreän nuolen avulla. Vain **Valitut kentät** -luettelossa olevat kentät voidaan päivittää käyttämällä vuokrauksen tuonnin ohjelmaa.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]