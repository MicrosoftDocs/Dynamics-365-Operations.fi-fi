---
title: Varastotapahtumatiedot
description: Tämä artikkeli sisältää yhteenvedon tapahtumatietosivusta, jossa näkyvät valitun varastotapahtuman tiedot.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 55e29d5804f57cd86fb5ddac5d6c5576b7ea5f61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859384"
---
# <a name="inventory-transaction-details"></a>Varastotapahtumatiedot

Voit tarkastella valitun varastotapahtuman tietoja **Tapahtuman tiedot** -sivulla.

## <a name="open-the-transaction-details-page"></a>Tapahtuman tietosivun avaaminen

Avaa **Tapahtuman tiedot** -sivu seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Kyselyt ja raportit \> Tapahtumat**.
1. Valitse tarkastettava tapahtuma.
1. Valitse toimintoruudussa **Tapahtuman tiedot**.

## <a name="fasttabs-overview"></a>Pikavälilehtien yleiskuvaus

**Tapahtuman tiedot** -sivu on jaettu useisiin pikavälilehtiin. Seuraavassa taulukossa kuvataan kunkin pikavälilehden tarkoitusta.

| Pikavälilehti | Kuvaus |
|---|---|
| Yleiset | Tässä pikavälilehdessä näkyvät valitun varastotapahtuman perustiedot. **Varastotapahtumat**-sivulla näkyvien kenttien lisäksi sivulla on lisäkenttiä, jotka on kuvattu jäljempänä tässä artikkelissa. |
| Päivitykset | Tässä pikavälilehdessä näkyvät valitun varastotapahtuman fyysisiin, kirjanpidollisiin ja tilitystapahtumiin liittyvät tiedot. Jotkin kentät saattavat olla tyhjiä tapahtuman nykyisestä tilasta riippuen. Nämä kentät määritetään kuitenkin automaattisesti tapahtumien kirjaamista varten. **Varastotapahtumat**-sivulla näkyvien kenttien lisäksi pikavälilehdessä on lisäkenttiä, jotka on kuvattu jäljempänä tässä artikkelissa. |
| Kirjanpidon kirjaukset | Tässä pikavälilehdessä näkyy kirjaustyyppi ja kirjanpitotili, joita käytetään valittuun varastotapahtumaan liittyviin fyysiseen päivitykseen, kirjanpitopäivitykseen, fyysiseen tuottoon, fyysisiin kuluihin, kirjanpitotuottoihin ja kirjanpitokuluihin. |
| Viitteet | Tässä pikavälilehdessä on lisätietoja valitun varastotapahtuman luomasta lähdetapahtumasta. Nämä tiedot voivat sisältää esimerkiksi ostotilauksen tai myyntitilauksen tietoja. |
| Aiheeseen liittyviä tietoja | Tässä pikavälilehdessä näkyvät valitun varastotapahtuman lisätiedot. Kenttiä ei ehkä voi määrittää, jos jotkin toiminnot, kuten hankintaluokat tai projektit, eivät ole käytössä. |
| Taloushallinnon dimensiot - fyysinen | Tässä pikavälilehdessä näkyvät taloushallinnon dimensioarvot, joita käytettiin fyysisen päivityksen kirjaamisen aikana. Jos fyysistä päivitystä ei ole kirjattu, kentät ovat tyhjiä. |
| Taloushallinnon dimensiot - taloudellinen | Tässä pikavälilehdessä näkyvät taloushallinnon dimensioarvot, joita käytettiin kirjanpidon päivityksen kirjaamisen aikana. Jos kirjanpidon päivitystä ei ole kirjattu, kentät ovat tyhjiä. |
| Varastodimensiot | Tällä pikavälilehdellä näkyvät varastodimensioarvot, jotka on liitetty valittuun varastotapahtumaan. Näitä arvoja ovat toimipaikka, varasto, koko, väri, kokoonpano, sijainti, eränumero, sarjanumero, varaston tila, rekisterikilpi ja omistaja. |

## <a name="fields-on-the-general-fasttab"></a>Yleinen-pikavälilehden kentät

Seuraavassa taulukossa kuvataan **Yleiset**-pikavälilehden kentät, jotka eivät näy myös **Varastotapahtumat**-sivulla.

| Kenttä | Kuvaus |
|---|---|
| Osapuoli | Valitun varastotapahtuman osapuolen nimi. Esimerkiksi ostotilaustapahtumassa näkyy ostotilauksen toimittajan nimi, ja myyntitilaustapahtumassa näkyy asiakkaan nimi. Tämä kenttä ei ole käytettävissä kaikille varastotapahtumalajeille. |
| Varastoviite | Jos valittuun varastotapahtumaan liittyy toinen varastotapahtuma, tapahtuman tyyppi. Jos esimerkiksi ostotilaus kohdistetaan myyntitilaukseen, ostotilauksen **Varastoviite**-kenttä asetetaan arvoon *Myyntitilaus* Järjestelmä luo merkinnän automaattisesti suoratoimitustilauksille ja konsernin sisäisille tilauksille. Kun käytät merkintää muissa kustannuslaskentamenetelmissä kuin *vakiokustannusmallissa* ja *liukuvassa keskiarvossa*, järjestelmä luo täsmäytyksen ja oikaisut tarkkoihin tapahtumiin. Näin voidaan saavuttaa "todellinen" kustannuslaskelma, joka ohittaa FIFO (first in, first out)-, last in, first out (LIFO)- tai painotettu keskiarvo -logiikan. |
| Varastonumero | Valittuun varastotapahtumaan liittyvä tapahtuma. Jos esimerkiksi ostotilaus kohdistetaan myyntitilaukseen, ostotilauksen **Varastonumero**-kenttä asetetaan myyntitilauksen numeroksi. |
| Projektitunnus | Jos valittu varastotapahtuma liittyy projektiin, tämän kentän arvoksi tulee projektinumero. |
| Erätunnus | Yksilöivä erätunnus, jonka järjestelmä on määrittänyt valitulle varastotapahtumalle. |
| Viite-erä | Jos valittuun varastotapahtumaan liittyy toinen varastotapahtuma, tapahtuman erätunnus. Jos esimerkiksi ostotilaus kohdistetaan myyntitilaukseen, ostotilauksen **Viite-erä**-kenttä on myyntitilausrivin varastotapahtuman **Erätunnus**-arvo. |
| Dimension numero | Yksilöivä tunnus, joka edustaa kaikkien valittuun varastotapahtumaan liitettyjen varastodimensioarvojen yhdistelmää. |
| Arvo avoin | Arvo, joka ilmaisee, onko valittu varastotapahtuma selvitetty varaston sulkemisprosessilla. Jos kentän arvona on *Kyllä*, tapahtumaa ei ole selvitetty. |
| Odotettu päivämäärä | Vastaanottotapahtumien osalta päivämäärä, jolloin varastovastaanoton odotetaan tapahtuvan. Tässä kentässä voi olla esimerkiksi varastoestotilauksen odotettu vastaanottopäivä tai ostotilausrivin toimituspäivä. |
| Inventointipäivä | Tämä kenttä määritetään, kun vastaanottotilauksen rekisteröintitapahtuma on tehty ennen fyysisen vastaanoton kirjaamista. |
| Muu kuin taloushallinnon siirto | Arvo, joka ilmaisee, onko valittu varastotapahtuma muu kuin taloushallinnon siirto. Muu kuin taloushallinnon siirto suoritetaan, kun varastodimensioiden muutosta ei seurata taloudellisesti **Nimikemalliryhmä**-sivulla. |
| Siirtoerän tunnus | Jos valittu varastotapahtuma on muu kuin taloushallinnonsiirto, tämän kentän arvoksi tulee sen muun varastotapahtuman **erätunnuksen** arvo, jota vasten valittu tapahtuma on selvitetty. |

## <a name="fields-on-the-updates-fasttab"></a>Päivitykset-pikavälilehden kentät

Seuraavassa taulukossa kuvataan **Päivitykset**-pikavälilehden kentät, jotka eivät näy myös **Varastotapahtumat**-sivulla.

| Kenttä | Kuvaus |
|---|---|
| Fyysinen tosite | Kirjanpidon tositenumero, johon valitun varastotapahtuman fyysinen kirjaus luotiin. |
| Reititys | Valittuun varastotapahtumaan liittyvä reitti. Tämä kenttä määritetään vain tuotannon keräysluettelotapahtumista, joissa tuoterakenne tai reseptirivi liittyy tiettyyn nimikkeeseen. |
| Pakkausluettelo | Ostotilauksen tuotteen vastaanottotapahtumalle määritetty pakkausluettelon numero. |
| Fyysinen kustannus | Fyysisen päivityksen summa, joka kirjattiin kirjanpitoon. Standardikustannustuotteen osalta tämä summa vastaa standardikustannusta. Muissa kustannuslaskelmamenetelmissä se vastaa tuotteen painotettua keskiarvoa kirjauksen yhteydessä. |
| Fyysinen tuotto | Fyysisen päivityksen viivästetyn tuoton summa, joka kirjattiin kirjanpitoon. |
| Kuormituksen tunnus | Jos nykyinen tapahtuma liittyy kuljetuksenhallinnan kuormitukseen, tässä kentässä näkyy nimikkeen mukana olevan kuormituksen yksilöivä numero. |
| Fyysisesti kirjattu | Tämä arvo ilmaisee, onko valittu varastotapahtuma kirjattu fyysisesti. Jos nykyinen tapahtuma kirjataan kirjanpitoon, käytössä on myös fyysinen tosite. |
| Rahoituksellisesti kirjattu | Tämä arvo ilmaisee, onko valittu varastotapahtuma kirjattu taloudellisesti. Jos nykyinen tapahtuma kirjataan kirjanpitoon, käytössä on myös taloudellinen tosite. |
| Fyysinen veloitus kirjattu | Tämä arvo ilmaisee, onko valittuun varastotapahtumaan liittyvät fyysiset veloitukset kirjattu. |
| Taloudellinen veloitus kirjattu | Tämä arvo ilmaisee, onko valittuun varastotapahtumaan liittyvät taloudelliset veloitukset kirjattu. |
| Rahoitustosite | Kirjanpidon tositenumero, johon kirjanpitokirjaus on luotu. |
| Lasku | Esimerkiksi ostotilaukselle tai myyntitilaukselle luotu laskun numero. |
| Oikaisu | Varaston sulkemisesta ja oikaisuprosessista valittuun varastotapahtumaan oikaistu summa. |
| Tulostili, kirjattu summa | Tuloslaskelmaan kirjatun valitun varastotapahtuman summa. |
| Kirjaamaton lasku | **Odottava toimittajan lasku** -sivulla näkyvän liittyvän ostotilauksen laskunumero. |
| Rahoitus suljettu | Tapahtuman täydellisen selvityksen päivämäärä. |
| Katettu todellinen paino | Selvityksen kattaman todellisen painon määrä. |
| Selvitetty määrä | Valitun varastotapahtuman selvitetty määrä. |
| Selvitetty arvo | Valitun varastotapahtuman selvitetty arvo. |
