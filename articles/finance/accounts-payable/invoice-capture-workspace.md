---
title: Invoice Capture -ratkaisun työtila
description: Tässä artikkelissa on tietoja Invoice Capture -ratkaisun työtilasta.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691153"
---
# <a name="invoice-capture-solution-workspace"></a>Invoice Capture -ratkaisun työtila

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Invoice Capture -ratkaisun rinnakkaisen katselun ohjelma

Laskujen syöttäminen järjestelmään on aina ollut aikaa vievä prosessi, jossa on helppo tehdä virheitä. Tämä johtuu siitä, että kirjanpitäjien on siirryttävä useiden liitetiedostojen ja ikkunoiden välillä kerätäkseen oikeat tiedot. Rinnakkaisen asiakirjojen katseluohjelman avulla on helpompi työskennellä laskujen parissa. Sen avulla prosessi on aiempaa helpompi, tehokkaampi ja tarkempi.

Rinnakkaisten asiakirjojen katseluohjelman avulla käyttäjät voivat nähdä alkuperäisen asiakirjan ja laskun avoinna rinnakkain samassa ikkunassa. Laskusivulle lisätään tiedot, jotka saadaan alkuperäisestä asiakirjasta. Katseluohjelma muodostaa yhteyden laskusivun kenttien ja alkuperäisen laskuasiakirjan välille. Katseluohjelma myös auttaa käyttäjiä löytämään laskusivun mahdolliset virheet.

### <a name="open-the-side-by-side-viewer"></a>Rinnakkaisen katseluohjelman avaaminen

Microsoft Dynamics 365 Financessa voit avata rinnakkaisen katseluohjelman yhteenvetosivun luettelossa tai laskuluettelosivulla. Voit avata sen myös kaksoisnapsauttamalla (tai kaksoisnapsauttamalla) tietuetta tai valitsemalla laskun numeron.

### <a name="using-the-side-by-side-viewer"></a>Rinnakkaisen katseluohjelman käyttäminen

#### <a name="manually-review-an-invoice"></a>Laskun manuaalinen tarkistaminen

Tuotu laskuasiakirja saattaa vaatia manuaalisen tarkistamisen virheiden tai varoitusten vuoksi. Rinnakkaisessa katseluohjelmassa asiakirjan ylätunnisteessa näkyy **Tuotu**-tila ja nykyinen versio on **Alkuperäinen versio**.

Aloita laskun tarkistaminen valitsemalla **Aloita tarkistus**. Kaikkia kenttiä voi nyt muokata. **Tila**-kenttään päivitetään arvo **Tarkistuksessa** ja **Nykyinen versio** -kenttään arvo **Muokattu versio**.

#### <a name="view-and-work-with-messages"></a>Viestien tarkasteleminen ja käsitteleminen

Käyttäjien on aloitettava tarkistusprosessi sanomaruudusta. Virhesanomat on merkitty punaisella X:llä, varoitussanomat kolmiolla ja tietosanomat ympyrällä. Luotettavuuspisteisiin liittyvät sanomat voidaan luokitella varoituksiksi tai virheiksi riippuen konfiguraatioryhmälle määritetystä rajasta. Lisätietoja on kohdassa [Invoice Capture -ratkaisun konfiguraatioryhmät](invoice-capture-config-group.md).

Varoitus- ja virhesanomat voidaan ohittaa sanomaruudussa, laskun otsikossa tai laskuriveillä. Kun sanoma ohitetaan, se ei enää näy virheenä tai varoituksena eikä laskun vahvistus epäonnistu.

- Jos haluat ohittaa sanomat sanomaruudussa, valitse **Ohita**. Jos haluat palauttaa ohitetun sanoman, valitse uudelleen **Ohita**. Tyyppi muutetaan tämän jälkeen virheestä tai varoituksesta tiedoksi.
- Jos haluat ohittaa sanomia laskun otsikossa tai laskurivillä, valitse kentässä **Ohita**. Sanomasymboli häviää näkyvistä. Sanoma tulee kuitenkin näkyviin uudelleen, jos se palautetaan sanomaruudussa.

Jos sanomat liittyvät laskun otsikon kenttiin ja valitset sanoman sanomaruudussa, kohdistin siirretään otsikko-osan vastaavaan kenttään.

#### <a name="proofread-and-edit-fields"></a>Kenttien oikolukeminen ja muokkaaminen

Jos kentän arvo luetaan alkuperäisestä laskusta OCR-tekstintunnistuksen avulla, kentässä näkyy symboli. Jos valitset symbolin, asiakirjan katseluohjelma lähentää kohtaan, josta kentän arvo luetaan, ja korostaa sen. Tämä auttaa laskun tietojen tarkistamisessa.

Jos haluat palauttaa asiakirjan katseluohjelman alkuperäiseen kokoon, noudata seuraavia ohjeita:

- Valitse aiemmin valitsemasi symboli.
- Valitse painike asiakirjan katseluohjelman oikeassa yläkulmassa.

Muokkaa kenttiä tarvittaessa. Muokkaukset tallennetaan automaattisesti, kun kohdistin lähtee kentästä. Kentän oikealla puolella oleva symboli ilmaisee, että kenttä on päivitetty manuaalisesti. Kun sivu päivitetään, symboli poistetaan.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>Laskun tarkistaminen päivitettyjen sanomien hakemiseksi

Kun muokkaat kenttää, kentän arvo päivitetään, mutta uusia vahvistussanomia ei luoda. Jos haluat hakea päivitetyt vahvistussanomat, valitse **Tarkista**. Sanomaruudun, laskun otsikon ja laskurivien sanomat päivitetään.

#### <a name="complete-the-review"></a>Tarkistuksen tekeminen valmiiksi

Voit tehdä tarkistuksen loppuun valitsemalla **Tee tarkistus valmiiksi**. Laskut vahvistetaan. Jos virheitä löytyy, asiakirjan tilaksi jää **Tarkistuksessa** ja näyttöön tulee sanomapalkki. Kaikki sanomaruudun, laskun otsikon ja laskurivien sanomat päivitetään automaattisesti niin, että järjestelmä antaa tietoja epäonnistuneen vahvistuksen syistä.

Kun kaikki estovirheet on korjattu, tarkistus voidaan tehdä valmiiksi. Tiedoston tilaksi päivitetään **Tarkistettu**, eikä kenttiä ei voi enää muokata. Voit käynnistää tarkistuksen uudelleen valitsemalla uudelleen **Aloita tarkistus**.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Odottavan toimittajalaskun luominen Financessa

Jos haluat lähettää laskuasiakirjan yhdistettyyn Finance-ympäristöön, valitse **Luo**. Jos laskun luominen epäonnistuu, sanomapalkkiin tulee virhesanoma.

#### <a name="void-an-invoice"></a>Laskun mitätöiminen

Voit mitätöidä laskun valitsemalla **Mitätöi**. Mitätöityjä laskuja ei voi tarkistaa, eivätkä ne näy **Manuaalista tarkistusta vaativat laskut** -luettelossa.

### <a name="validation-logic"></a>Vahvistuksen logiikka

Jotkin avainkentät eivät ole olemassa laskun väliaikaisen tallennuksen tiedoissa rinnakkaisessa katseluohjelmassa, mutta ne on luotava odottavien laskujen luomiseksi Financessa. Nämä kentät johdetaan nykyisen laskun väliaikaisen tallennuksen tietojen ja Financen päätietojen yhdistelmästä.

Kentät, jotka johdetaan, ovat **Yritys**, **Toimittajatili** ja **Nimikkeen numero**. Ne on johdettava seuraavassa järjestyksessä. Jos kentän johtaminen epäonnistuu, prosessi pysähtyy.

1. **Yritys** – Yritys johdetaan ensin. Jos yritykselle löytyy aktiivinen vastaavuusmäärityksen sääntö, yritys johdetaan yrityksen nimen ja yrityksen osoitteen perusteella.
2. **Toimittajatili** – Seuraavaksi johdetaan toimittajatili aktiivisen vastaavuusmäärityksen säännön ja johdetun yrityksen sekä toimittajan nimen ja osoitteen yhdistelmän perusteella.
3. **Nimikkeen tunnus** – Lopuksi johdetaan nimikkeen nimi väliaikaisesta tallennuksesta seuraavien kolmen tietotyypin perusteella:

    - Määritetty vastaavuusmäärityksen sääntö
    - Johdettu yritys
    - Johdettu toimittajatili

Jos haluat suorittaa vahvistuksen, valitse rinnakkaisessa katseluohjelmassa **Tarkista**. Tällä hetkellä vahvistus suorittaa seuraavat toiminnot:

- **Pakollinen tarkistus** – Tämä tarkistus vahvistaa pakolliset kentät rinnakkaisessa katseluohjelmassa. Käyttäjät voivat valita, minkä kenttien on oltava pakollisia **Määrityksen asetukset** -sivulla.
- **Luotettavuuspisteet** – Käyttäjät voivat määrittää varoituksen ja virheen raja-arvon luotettavuuspisteille. Tässä tarkistuksessa keskitytään OCR-tekstintunnistuksen luotettavuuspisteisiin, jotka ovat näiden raja-arvojen alapuolella. Virhe- tai varoitussanomat näytetään vahvistustuloksen perusteella.
- **Yritys** – Tämä tarkistus vahvistaa, että yritys on Financessa. Jos yritystä ei ole Finance-ympäristössä, vahvistus epäonnistuu.

Kun rinnakkaista katseluohjelmaa käytetään ensimmäisen kerran ja käyttäjä valitsee **Tarkista**, suoritetaan johtamis- ja vahvistusprosessit. Jos laskut ovat oikein, vahvistusprosessi suoritetaan, kun käyttäjä valitsee **Tee tarkistus valmiiksi**. Se suoritetaan myös silloin, kun käyttäjä valitsee **Luo toimittajan lasku** -kohdan.

Johtamisprosessi tehdään ennen vahvistusprosessia. Kaikki varoitukset ja virheet saadaan vahvistusprosessista. Varoitukset ja virheet kirjataan Financeen.
