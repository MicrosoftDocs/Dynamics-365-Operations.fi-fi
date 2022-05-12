---
title: Commerce-kirjausparametrit
description: Tässä aiheessa kuvataan parametrit, jotka liittyvät taloudellisten ja fyysisten tapahtumien kirjaamiseen Microsoft Dynamics 365 Commercessa.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 1b49c893567d39f05e16cefee47407a424b7e139
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649196"
---
# <a name="commerce-posting-parameters"></a>Commerce-kirjausparametrit

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä aiheessa kuvataan parametrit, jotka liittyvät taloudellisten ja fyysisten tapahtumien kirjaamiseen Microsoft Dynamics 365 Commercessa. Commerce-kirjausparametrit sijaitsevat Commerce headquarters -sovelluksessa kohdassa **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Commerce-parametrit \> Kirjaus**.

## <a name="periodic-discount-parameters"></a>Kausialennuksen parametrit

Seuraavassa taulukossa on luetteloitu kausialennuksen parametrit, jotka liittyvät taloudellisten ja fyysisten tapahtumien kirjaamiseen.

| Parametri | Kuvaus |
|-----------|-------------|
| Kirjaa kausialennus | Tämä asetus määrittää kirjataanko kausialennukset kirjanpitotileille. Kausialennuksia ovat yhdistelmä- ja määräalennukset sekä alennustarjoukset. Kun tämä parametri on käytössä, **Kausialennukset**-osaan voidaan määrittää lisäkenttiä. |
| Kirjanpitotilityyppi | <p>Valitse tilin tyyppi, jota käytetään kausialennuksien kirjaamiseen:</p><ul><li>**Vakio** – Järjestelmä ei käytä tämän sivun alennuksiin liittyviä kenttiä. Sen sijaan se käyttää tilejä, jotka on määritetty Commerce headquartersissa **Kirjaus**-sivulla (**Inventoinnin- ja varastonhallinta \> Määritys \> Kirjaus \> Kirjauslomakkeet**).</li><li>**Kausittainen** – Järjestelmä käyttää Commerce-alennustilejä, jotka on määritetty tämän sivun alennuksiin liittyvissä kentissä. Jos valitset tämän asetuksen, on määritettävä kirjanpitotili erityyppisiin tarjouksiin (alennus, yhdistelmäalennus, määräalennus ja raja-alennus). Kun määrität kunkin alennuksen, voit määrittää tilin. Kun alennustilien kirjaustoimintoa käytetään alennuksen asetussivulla, debet-kirjaus ja kredit-kirjaus luokittelevat alennuskirjauksen uudelleen Commercen alennuksen kirjanpitotililtä alennuksen kirjanpitotilille. Lisätietoja on kohdassa [Vähittäismyynnin alennukset](retail-discounts-overview.md).</li></ul> |
| Kirjaa alennuksen tietokoodi | Tätä vaihtoehtoa ei enää käytetä Commerce-vakioratkaisussa, ja se on vanhentunut. |
| Kirjaa tilausten kausialennus | Tämä asetus määrittää, kirjataanko vähittäismyynnin kausialennukset asiakastilausten ja puhelinkeskustilausten kirjanpitoon. |

## <a name="inventory-update-parameters"></a>Varaston päivitysparametrit

Seuraavassa taulukossa on luetteloitu varaston päivityksen parametrit, jotka liittyvät taloudellisten ja fyysisten tapahtumien kirjaamiseen.

| Parametri | Kuvaus |
|-----------|-------------|
| Käytä oletuserätunnusta, kun eränumeroita ei löydy | Tämä asetus määrittää, käytetäänkö oletuserätunnusta erään määritetyille nimikkeille, kun nimikkeiden eränumeroita ei löydy ja negatiivinen varasto sallitaan. |
| Oletuserätunnus | Eränumero, jota käytetään, kun nimikkeiden eränumeroita ei löydy ja **Käytä oletuserätunnusta, kun eränumeroita ei löydy** -parametri on käytössä. |

## <a name="aggregation-parameters"></a>Koosteparametrit

Seuraavassa taulukossa on luetteloitu koosteparametrit, jotka liittyvät taloudellisten ja fyysisten tapahtumien kirjaamiseen.

| Parametri | Kuvaus |
|-----------|-------------|
| Toimitus kassakaappiin | Ota tämä parametri käyttöön, kun haluat koostaa kaikki tapahtumat laskelman kirjaamisen aikana ja luoda kirjauskansioon yhden rivin kirjausta varten jokaisen osan erillisen rivin sijaan. |
| Toimitus pankkiin | Ota tämä parametri käyttöön, kun haluat koostaa kaikki tapahtumat laskelman kirjaamisen aikana ja luoda kirjauskansioon yhden rivin kirjausta varten jokaisen osan erillisen rivin sijaan. |
| Myyntitapahtumat | Tämän parametrin avulla voit konsolidoida tapahtumat osana tapahtumalaskelman kirjausprosessia. Suosittelemme, että otat tämän parametrin käyttöön. Sen nimi oli aiemmin **Tositetapahtumat**. |
| Älä koosta palautuksia | Jos tämä vaihtoehto on valittuna, kukin palautustapahtuma kirjataan erillisenä myyntitilauksena vähittäismyynnin laskelmia kirjattaessa. |

## <a name="batch-processing-parameters"></a>Eräkäsittelyn parametrit

Seuraavassa taulukossa on luetteloitu eräkäsittelyn parametrit, jotka liittyvät taloudellisten ja fyysisten tapahtumien kirjaamiseen.

| Parametri | Kuvaus |
|-----------|-------------|
| Rinnakkaisten laskelmien enimmäismäärä | Tässä kentässä määritetään usean laskelman kirjaamiseen käytettävä erätehtävien määrä. |
| Säikeiden enimmäismäärä tilausten käsittelyssä laskelmaa kohti | Tämä kenttä edustaa laskelman kirjauksen eräajossa käytettävien säikeiden enimmäismäärää, kun halutaan luoda ja laskuttaa yhden laskelman myyntitilauksia. Laskelman kirjausprosessissa käytettävien säikeiden kokonaismäärä lasketaan tämän parametrin arvon mukaan kerrottuna **Rinnakkaisen laskelman kirjausten enimmäismäärä**-parametrin arvolla. Jos tämän parametrin arvon määritetään liian suureksi, se voi vaikuttaa kielteisesti laskelman kirjausprosessin suorituskykyyn. |
| Suurin mahdollinen tapahtumarivien määrä sisällytetty koosteeseen | Tämä kenttä määrittää, montako tapahtumariviä sisällytetään yksittäiseen yhteenlaskettavaan tapahtumaan ennen uuden tapahtuman luomista. Yhdistetyt tapahtumat luodaan erilaisten koostekriteerien, kuten asiakkaan, liiketoiminnan päivän tai taloushallinnon dimensioiden, perusteella. Huomaa, että yksittäisen tapahtuman rivejä ei jaeta eri yhdistettyjen tapahtumien kesken. Siksi yhdistettyjen tapahtumien rivien määrä saattaa olla hieman suurempi tai pienempi tekijöiden, kuten erillisten tuotteiden määrän, perusteella. |
| Myymälän tapahtumien tarkistuksen säikeiden enimmäismäärä | Tämä kenttä määrittää tapahtumien tarkistuksessa käytettävien säikeiden enimmäismäärän. Tapahtumien vahvistaminen on pakollinen vaihe, joka on suoritettava, ennen kuin tapahtumat voidaan noutaa lausekkeissa. Sinun on myös määritettävä uuden kirjausprosessin aikana lahjakorttituote **Lahjakortti**-pikavälilehdessä **Kaupan parametrit** -sivun **Kirjaus**-välilehdessä, vaikka organisaatio ei käyttäisi lahjakortteja. |

Seuraavassa taulukossa luetellaan edellisen taulukon parametrien suositellut arvot. Nämä arvot on testattava ja räätälöitävä käyttöönoton konfiguraation ja käytettävissä olevan infrastruktuurin mukaan. Suositeltujen arvojen ylittäminen voi vaikuttaa haitallisesti muihin eräkäsittelyihin, ja ne on tarkistettava.

| Parametri | Suositeltava arvo | Yksityiskohtaiset tiedot |
|-----------|-------------------|---------|
| Rinnakkaisten laskelmien kirjaamisen enimmäismäärä | <p>Määritä tämän parametrin arvoksi niiden erätöiden määrä, joka on käytettävissä eräryhmälle, joka suorittaa **Laskelma**-työn.</p><p>**Yleinen sääntö:** Kertomalla Application Object Serverin (AOS) virtuaalipalvelinten määrän AOS-virtuaalipalvelimessa käytettävissä olevien erätehtävien lukumäärällä.</p> | Tätä parametria ei voi käyttää, kun **Vähittäismyyntilaskelmat – vähittäinen syöttö** -ominaisuus on käytössä. |
| Säikeiden enimmäismäärä tilausten käsittelyssä laskelmaa kohti | Aloita testaamaan arvoilla kohdasta **4**. Yleensä arvo ei saa ylittää arvoa **8**. | Tämä parametri määrittää myyntitilausten luomiseen ja kirjaamiseen käytettyjen säikeiden määrän. Se edustaa säikeiden määrää, jonka avulla voidaan kirjata laskelmaa kohti. |
| Suurin mahdollinen tapahtumarivien määrä sisällytetty koosteeseen | Aloita testaamaan arvoilla kohdasta **1000**. Commerce headquarters -konfiguraation mukaan pienemmät luvut voivat olla tehokkaammin suorituskyvylle hyödyllisiä. | Tämä parametri määrittää kuhunkin myyntitilaukseen sisällytettävien rivien määrän laskelman kirjaamisen yhteydessä. Kun tämä numero on saavutettu, rivit jaetaan uuteen tilaukseen. Myyntirivien määrä ei vastaa tarkasti määrittämääsi lukua, koska jako tapahtuu myyntitilauksen tasolla. Luku on kuitenkin lähellä määritettyä numeroa. Tätä parametria käytetään, kun luodaan myyntitilauksia vähittäismyyntitapahtumille, joissa ei ole nimettyä asiakasta. |
| Myymälän tapahtumien tarkistuksen säikeiden enimmäismäärä | Suosittelemme tämän parametrin arvoksi **4** ja korotusta vain, jos et saavuta hyväksyttävää suorituskykyä. Tämän prosessin käytössä olevien säikeiden määrä ei voi ylittää eräpalvelimen käytettävissä olevien suorittimien määrää. Jos säikeiden määrä on liian suuri, se voi vaikuttaa muihin eräkäsittelyihin. | Tämä parametri ohjaa niiden tapahtumien määrää, jotka voidaan vahvistaa tietyn myymälän osalta samanaikaisesti. |

> [!NOTE]
> Kaikki asetukset ja parametrit, jotka liittyvät laskelman kirjauksiin ja jotka on määritetty vähittäismyymälöissä ja **Commerce-parametrit**-sivulla, liittyvät parannettuun laskelman kirjaustoimintoon.

## <a name="invoice-parameters"></a>Laskuparametrit

Seuraavassa taulukossa on luetteloitu laskuparametrit, jotka liittyvät taloudellisten ja fyysisten tapahtumien kirjaamiseen.

| Parametri | Kuvaus |
|-----------|-------------|
| Kirjauskansion nimi | Maksukirjauskansion nimi, jota käytetään, kun asiakkaan myyntitilausmaksujen maksukirjauskansiot luodaan. Tämä asetus koskee kaikkia myyntipisteen, puhelinkeskuksen ja sähköisen kaupankäynnin kanavan tilauksiin kirjattuja tilausmaksuja. |
| Tilin nimi | Maksutilin nimi. |
| Priorisoi dimensiot maksutavasta | Kun tämä merkintä on käytössä, maksukirjauskansiossa on priorisoitu dimensioita maksutavasta myymälän dimensioiden sijaan. |
| Verojen laskentatapa | Tämä parametri määrittää toiminnan, jota käytetään, kun laskelman kirjaamisen aikana luodut myyntitilaukset laskutetaan:<ul><li>**Laske uudelleen** – Laske verot uudelleen.</li><li> **Älä laske uudelleen** – Käytä myyntipisteessä laskettuja verosummia.</li></ul> |
| Kirjauskansion nimi | Kirjauskansion nimi, jota käytetään, kun asiakkaan palautusten maksukirjauskansio luodaan. Tämä asetus koskee kaikkia myyntipisteen, puhelinkeskuksen ja sähköisen kaupankäynnin kanavan tilauksiin kirjattuja tilausmaksuja. |

## <a name="statement-parameters"></a>Laskelmaparametrit

Seuraavassa taulukossa on luetteloitu laskelmaparametrit, jotka liittyvät taloudellisten ja fyysisten tapahtumien kirjaamiseen.

| Parametri | Kuvaus |
|-----------|-------------|
| Varaston varaaminen laskennan aikana | Kun tämä parametri on käytössä, laskelman laskenta varaa varaston väliaikaisesti, kunnes laskelma kirjataan. Tämä parametri on oletusarvon mukaan poissa käytöstä laskelman laskennan suorituskyvyn parantamiseksi. Päivitetyt varastotiedot voidaan laskea käyttämällä **Kirjaa varasto** -erätyötä. Huomaa, että **Kirjaa**-varastoerätyötä ei enää käytetä, kun [vähittäisiin syötteisiin](trickle-feed.md) perustuva tilausten luonti on käytössä vähittäismyynnin myymälätapahtumille. |
| Poista pakollinen laskenta käytöstä | Tämä merkki poistaa laskennan käytöstä Commerce headquartersin kirjauksen aikana. |
| Laske taloushallinnon dimensiot uudelleen virheen tapahtuessa | Kun tämän parametri on käytössä, taloushallinnon dimensiot voidaan arvioida uudelleen myöhemmissä laskelmakirjauksissa, jos laskelmien kirjaaminen epäonnistuu. |
| Käytä palautuskaupan taloushallinnon dimensioita | Kun tämä parametri on käytössä, linkitetyt palautusmyyntitilaukset voidaan luoda käyttämällä myymälän taloushallinnon dimensioita alkuperäisen tapahtuman taloushallinnon dimensioiden sijaan. |
| Poista palautusten linkitys | Kun tämä parametri on käytössä, laskelma voi luoda kirjaamattoman myynnin palautuksia sokkopalautuksina. Tämä parametri on oletusarvon mukaan poissa käytöstä. Suosittelemme, että pidät parametrin pois käytöstä. |
| Poista pyöristyseron kirjaus käytöstä | Tämä parametri poistaa käytöstä pyöristyseron kirjaustapahtuman maksun ja bruttosumman välillä maksujen käsittelyn aikana. |
| Täsmäytä asiakastalletukset automaattisesti | Kun tämä parametri on käytössä, se määrittää, täsmäytetäänkö vähittäismyynnin tiliotteen käsittelyn aikana kirjatut asiakkaan talletukset asiakkaan avointen tapahtumien perusteella. |
| Ota käteisvarojen hallinnan täsmäytys käyttöön ja käytä sitä myyntipisteessä | Kun tämä parametri on käytössä, kassanhallinnan täsmäytys tehdään myyntipisteessä ja arvot siirretään vähittäismyynnin tilinpäätöksen kirjauksen kautta laskelmarivien luontia varten. |
| Kirjanpitotositteen erittelytaso | Tämä parametri määrittää kirjanpitotositteeseen sisällytettävän erittelytason valituille myyntipisteestä peräisin oleville tapahtumille. Tapahtumalajeja ovat tulot, kulut ja alennukset. Alennusten osalta tämä parametri otetaan huomioon vain, kun kausialennuksen tilinumero ja tavallisen alennuksen tilinumero eivät ole samat. Jos tietoja ei edellytetä, **Yhteenveto** on suositeltava arvo näille kirjauksille. Kun yhteenvetotason kirjaus määritetään, **TransactionDiscountTrans.RecID**-tunnusta ei täytetä. Commerce 10.0.27 -versiossa tämä merkintä nimettiin uudelleen ja siirrettiin. Nimi oli aiemmin **Erittelytaso** ja se oli **Varaston päivitys** -osassa. |
