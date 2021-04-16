---
title: Perinnän hallinnan keskeiset käsitteet
description: Ohjeaiheessa käsitellään perinnän hallinnan keskeisiä käsitteitä.
author: mikefalkner
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7f23f3668bfc344b2964c1b0062a5ed1174df05c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835385"
---
# <a name="collections-management-key-concepts"></a>Perinnän hallinnan keskeiset käsitteet

[!include [banner](../includes/banner.md)]

Ennen kuin aloitat perinnän määrittämisen tai perinnän käyttämisen, on hyvä ymmärtää seuraavat käsitteet:

- Asiakkaan erääntymistilannevedokset sisältävät erääntyneet saldotiedot tietyltä aikajaksolta.
- Perinnän asiakaspoolit helpottavat työn organisointia.
- Perimisasiamiehet voivat ylläpitää omia asiakaspoolejaan.
- Luettelosivuilla voi järjestää perinnän asiakkaita, tehtäviä ja tapauksia.
- Kaikki asiakkaan perintätiedot yhdellä sivulla, jolta voit ryhtyä toimenpiteisiin.
- Korkojen ja maksujen peruuttaminen, palauttaminen tai kääntäminen yhdellä toiminnolla.
- Poistotapahtumia voidaan luoda yhdessä vaiheessa.
- Ei katetta (NSF) -maksut voidaan käsitellä yhdessä vaiheessa.

Tässä ohjeaiheessa käsitellään kukin käsite.

## <a name="customer-aging-snapshots"></a>Asiakkaan erääntymistilannevedokset

Erääntymistilannevedos sisältää asiakkaan lasketut erääntyneet saldot tiettynä ajankohtana. Nämä tiedot näytetään **Erääntyneet saldot**-luettelosivulla ja **Perintä**-sivulla. Erääntymistilannevedos on luotava, ennen kuin perinnän luettelosivun tietoja voi tarkastella (**Erääntyneet saldot**, **Perintätehtävät** ja **Perintätapaukset**).

Kunkin asiakkaan erääntymistilannevedos sisältää erääntymistilanteen otsikko- ja erittelytietueet, jotka vastaavat kutakin erääntymiskautta erääntymiskauden määrityksessä.

Erääntymistilannevedoksen otsikko sisältää asiakkaan tilillä erääntyneen kokonaissumman, luottorajan, pakkausluettelon summan, myyntitilauksen summan, riitautettujen tapahtumien määrän ja riitautettujen tapahtumien kokonaissumman. Kaikki tämän asiakkaan tapahtumat sisällytetään näiden summien laskentaan. Erääntynyt kokonaissumma, luottoraja, pakkausluettelon summa ja myyntitilauksen summa näytetään **Perintä**-sivun **Luottotiedot**-tietoruudussa.

Erääntymistilannevedoksen erittelytietue luodaan jokaiselle erääntymiskauden määrittelyyn sisältyvälle erääntymiskaudelle. Kukin erittelytietue sisältää erääntymiskauden tunnuksen sekä tapahtumien kokonaissumman erääntymiskauden päivämääriltä. Tapahtumat määritetään erääntymiskaudelle, kuten 30 päivää myöhässä. Päivämäärä on suhteessa **Erääntyy**-päivämäärään, joka määritetään erääntymistilannevedosta luotaessa. Nämä tiedot näytetään **Erääntyneet saldot** -luettelosivulla sekä **Perintä**-sivun **Erääntyneet saldot** -tietoruudussa.

## <a name="collections-customer-pools"></a>Perinnän asiakaspoolit

Asiakaspoolit ovat kyselyjä, jotka määrittävät asiakastietueryhmän. Näiden ryhmitettyjen tietueiden avulla voi tarkastella sisältyvien asiakastilien tietoja sekä hallita niiden perintä- tai erääntymisprosesseja. Voit suodattaa perinnän luettelosivujen tietoja asiakaspoolien avulla. Voit käyttää niitä suodattamaan myös erääntymistilannevedoksen luontiin sisältyneitä asiakastilejä.

## <a name="collections-agents"></a>Perimisasiamiehet

Käyttäjät voivat tarkastella oletusarvoisesti kaikkia asiakastietoja perinnän luettelosivuilla. Perimisasiamiestietueiden avulla voidaan määrittää asiakaspoolit, joiden avulla voi suodattaa tietoja perinnän luettelosivuilla ja **Perintä**-sivulla.

Perimisasiamies työskentelee asiakkaiden kanssa varmistaakseen, että maksut peritään ajoissa. He ovat työtekijöitä, jotka on määritetty käyttäjille **Käyttäjän määritys** -sivulla.

## <a name="collections-list-pages"></a> Perinnän luettelosivut 

Seuraavat luettelosivut ovat hyödyllisiä perintätietojen järjestämisessä:

- **Erääntyneet saldot** – tämän luettelosivun sarakkeet näyttävät asiakkaan saldot ja erääntyneet summat erääntymiskauden mukaan. Nämä tiedot on tallennettu erääntymistilannevedokseen. Erääntymiskaudet on määritelty käytetyn erääntymiskauden määritelmän mukaan. Erääntymiskauden määritelmä on otettu asiakaspoolista, jos poolikyselyyn on määritetty asiakaspooli. Jos asiakaspoolilla ei ole erääntymiskausimääritelmää, käytetään **Myyntireskontran parametrit** -sivulla määritettyä oletuserääntymiskauden määritelmää. Jos oletuserääntymiskauden määritystä ei ole määritetty, käytetään **Erääntymiskausien määritykset** -sivun ensimmäistä erääntymiskausimääritystä.
- **Perintätehtävät** – Tämä luettelosivun sarakkeissa näytetään tehtävät, jotka on tunnistettu perintätehtäviksi. Nämä tehtävät luodaan **Perintä**-sivulla. Aktiviteettien avulla seurataan perintään liittyvää työtä.
- **Perintätapaukset** – tämän luettelosivun sarakkeissa näytetään tietoja tapauksista, jotka kuuluvat **Perintä**-tapaustyypin sisältävään tapausluokkaan.

### <a name="aging-snapshots"></a>Erääntymistilannevedokset

Erääntymistilannevedos on luotava ennen kuin voit tarkastella perinnän luettelosivujen tietoja. Näkyvissä ovat vain niiden asiakkaiden tiedot, joille on luotu erääntymistilannevedos. Luettelosivulla näkyviä tietueita voi lisäksi suodattaa seuraavasti:

- Oletusarvoisesti käyttäjällä on käyttöoikeus kaikkiin asiakkaisiin, joilla on erääntymistilannevedos.
- Jos järjestelmässä on asiakaspooleja, käyttäjä on määritettävä perimisasiamieheksi voidakseen käyttää pooleja perinnän luettelosivun tietojen suodattamiseen. Tiedot rajoitetaan asiakkaisiin, jotka kuuluvat valittuun asiakaspooliin.
- Jos käyttäjä on määritetty perimisasiamieheksi, ainoastaan kyseiselle perimisasiamiehelle valitut poolit ovat saatavilla perinnän luettelosivuilla. Jos **Anna edustajan tarkastella kaikkia asiakaspooleja** -asetus on valittuna perimisasiamiehen **Perimisasiamies**-sivulla, kyseinen edustaja voi käyttää kaikkia pooleja.

## <a name="collections-page"></a> Perintä-sivu

**Perintä**-sivulla voit tarkastella ja hallita asiakkaan perintätietoja, tehtäviä ja tapauksia sekä suorittaa niille toimenpiteitä.

Sivun yläosassa on valitun asiakkaan tapaukset, keskiosassa asiakkaan tapahtumat ja alaosassa asiakkaan tehtävät. Voit luoda perintätapauksia seurataksesi yhden tai useamman tapahtuman ja tehtävän perintätietoja. Ylä- ja alaosien tietoja voidaan suodattaa tapauskohtaisesti.

Valitun asiakkaan erääntyneet saldot ja luottorajatiedot näkyvät tietoruuduissa. Nämä tiedot on tallennettu erääntymistilannevedokseen. Voit päivittää erääntymistilannevedoksen tiedot nykyisillä tiedoilla tarvittaessa.

Toimintoruutu sisältää painikkeita, joilla voit tarkastella valittuun asiakkaaseen, tapaukseen, tapahtumaan tai tehtävään liittyviä tietoja. Voit myös suorittaa yleisiä toimintoja, kuten tapahtuman perintätilan muuttaminen, sähköpostiviestien lähettäminen integroidun sähköpostipalvelun välityksellä, asiakkaiden hyvittäminen, NSF-maksujen käsittely ja perintäkelvottomien saldojen poiskirjaaminen.

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a>Korkojen ja kulujen peruuttaminen, palauttaminen tai kääntäminen

Voit peruuttaa, palauttaa tai kääntää kokonaisia korkolaskuja tai niiden osana olevia kuluja ja tapahtumakorkoja. Valitse **Kaikki asiakkaat** -luettelosivun toimintoruudun **Perintä**-välilehdessä **Korkolasku**, **Tapahtumakorko** tai **Kulu**.

Nämä muutokset vaikuttavat vain korkolaskuihin sekä niihin sisältyviin korkoihin ja kuluihin. Lisätietoja asiakkaan velkana olevien kulujen poiskirjaamisesta on tämän ohjeaiheen kohdassa [Poistotapahtumien luominen](#creating-write-off-transactions).

Lisätietoja on ohjeaiheissa Korkoryhmäalueen luominen ja Koron käsittely.

## <a name="creating-write-off-transactions"></a>Poistotapahtumien luominen

Voit kirjata luottotappiot pois valitsemalla **Poisto** **Perinnät**-sivulla ja perinnän luettelosivuilla.

Kun kirjaat pois asiakkaan tapahtumia, kaikki asiakkaan tapahtumat merkitään automaattisesti selvitettäväksi. Poiskirjattava summa riippuu merkittyjen tapahtumien nettosummasta. Poiskirjaustapahtuma luodaan yleisessä kirjauskansiossa ja se voi sisältää enintään kolmen tyyppisiä kirjauskansion rivejä:

- Ensimmäinen kirjauskansiorivi sisältää asiakastapahtuman poiskirjauksen. Jos merkityt tapahtumat sisältävät useita valuuttakoodien, dimensioiden ja kirjausprofiilien yhdistelmiä, kullekin yhdistelmälle luodaan erillinen kirjauskansion rivi.
- Toinen kirjauskansiorivi sisältää kirjanpidon poiskirjauksen. Jos merkityt tapahtumat sisältävät useita valuuttakoodien, dimensioiden ja kirjausprofiilien yhdistelmiä, kullekin yhdistelmälle luodaan erillinen kirjauskansion rivi.
- Kirjauskansiorivin kolmas tyyppi on kirjanpidon poiskirjaustieto arvonlisäveroille. Kirjauskansiorivi luodaan vain, jos **Erillinen arvonlisävero** -asetus on valittuna **Myyntireskontran parametri** -sivulla. Jos merkityt tapahtumat sisältävät useita arvonlisäveron kulutilien, dimensioiden ja arvonlisäverokoodien yhdistelmiä, kullekin yhdistelmälle luodaan erillinen kirjauskansion rivi. Poiskirjaustapahtuma luodaan tapahtuman valuutalla. Lisätietoja on ohjeaiheessa Poiskirjauksen kirjauskansion luominen asiakkaalle.

## <a name="process-nsf-payments"></a>NSF-maksujen käsitteleminen

Voit käsitellä NSF-maksuja valitsemalla **Perintä**-sivulla **NSF-maksu**. Maksu peruutetaan, kun valitset tämän painikkeen. Jos NSF-maksu koskee asiakkaan kuluja, veloitustapahtuma luodaan maksujen kirjauskansioon. Maksun summa perustuu automaattisten veloitusten asetuksiin. NSF-maksuihin sovellettavat automaattiset veloitukset määritetään kuluryhmässä, joka on valittu **Pankkitilit**-sivulla pankkitilille, jota asia koskee.

## <a name="additional-resources"></a>Lisäresurssit

[Asiakkaan luotonhallinnan parametrien määrittäminen](./cm-credit-mgmt-setup.md)

[Asiakkaan luotonhallinnan määritystiedot](./cm-setup-information.md)

[Asiakkaan luotonhallintatietojen lisääminen](./cm-add-credit-mgmt-information-customer.md)

[Asiakasluottoryhmät](./cm-customer-credit-groups.md)

[Asiakkaan luottorajan oikaisut](./cm-credit-limit-adjustments.md)

[Myyntitilausten luottorajapidot](./cm-sales-order-credit-holds.md)

[Asiakkaan luotonhallinnan kausittaiset tehtävät](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]