---
title: Ostojen cXML-parannukset
description: Ostojen cXML-parannusten ominaisuus perustuu aiemmin luotuun ulkoiseen PunchOut-luettelotoimintoon, jota käytetään ostoehdotuksissa.
author: dasani-madipalli
manager: tfehr
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatCXMLParameters, CatCXMLPurchRequest
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: d7184f14ab67d646451c8c2b1313336d47e59316
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427504"
---
# <a name="purchasing-cxml-enhancements"></a>Ostojen cXML-parannukset

[!include [banner](../includes/banner.md)]

_Ostojen cXML-parannusten_ ominaisuus perustuu [aiemmin luotuun ulkoiseen luettelotoimintoon](set-up-external-catalog-for-punchout.md), jota käytetään ostoehdotuksissa. Olemassa oleva toiminto on nimeltään _PunchOut_. Vaikka ostotilauksen ei tarvitse olla peräisin ostoehdotuksesta, ostotilauksen toimittajan ja ostotilausasiakirjan lähettämiseen käytettävien parametrien välillä on oltava yhteys.

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>Ostojen cXML-parannusten toiminnon käyttöönotto

Voit ottaa toiminnon käyttöön avaamalla **[Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** -sivun ja etsimällä toiminnon, jonka nimi on *Ostojen cXML-parannukset*. Valitse toiminto ja ota se käyttöön valitsemalla **Ota käyttöön nyt**.

Kun olet ottanut toiminnon käyttöön, sinun kannattaa määrittää asetukset kolmella seuraavalla alueella:

- **[cXML-parametrit](#cxml-parameters)** – Näillä asetuksilla voi määrittää ostotilausten lähettämisen toiminnolle yleisiä parametreja.
- **[toimittajamääritys](#vendor-setup)** – Jos tarkoituksena on käyttää oletusarvoisesti kieltä commerce eXtensible Markup Language (cXML) kaikille uusille ostotilauksille, jotka luodaan mille tahansa toimittajalle, määritä asetuksen **Lähetä ostotilaus cXML:llä** arvoksi _Kyllä_ kyseisen toimittajan osalta.
- **[Ulkoiset luettelot](#external-catalog-setup)** – Käytä uusia **Määritä tilauksen ominaisuudet** -asetuksia määrittääksesi ostotilausasiakirjan muodon ja sen, miten se lähetetään.

Seuraavassa kuvassa on yhteenveto tästä määrityksestä.

![cXML-toimintojen määritysalueet](media/cxml-settings-areas.png "cXML-toimintojen määritysalueet")

Lisäksi on määritettävä [Ostotilauspyynnön erätyö](#po-batch). Tätä erätyötä käytetään vahvistettujen ostotilausten lähettämiseen.

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>Yleisten cXML-parametrien määrittäminen

**cXML-parametrit**-sivulla voit määrittää joitakin yleisiä asetuksia, joita sovelletaan ostotilausten lähettämisen toimintoon.

![cXML-parametrien sivu](media/cxml-parameters.png "cXML-parametrien sivu")

Siirry kohtaan **Ostot ja hankinnat \> Määritys \> cXML-hallinta \> cXML-parametrit** ja määritä seuraavat parametrit:

- **cXML-testitila** – Tämä yleinen parametri vaikuttaa tapaan, jolla ostotilaukset lähetetään fyysisesti erätyöstä. Valitse jokin seuraavista:

    - **Testaus** – Tässä tilassa erätyö voi olla käynnissä ja sanoman XML-asiakirja luodaan, mutta sitä ei lähetetä. Sen sijaan se tallennetaan ostotilauspyyntöön tarkastelutarkoituksia varten. Tämä tila on hyödyllinen, kun käynnissä on alustava toteutus ja haluat nähdä, miten tietoja lisätään cXML-sanomaan. Voit myös luoda mallisanomia, jotka voit lähettää toimittajille alustavaa vahvistamista varten.
    - **Live** – Tässä tilassa toiminto käyttää [ulkoisen luettelon asetuksia](#external-catalog-setup) lähettääkseen kunkin asiakirjan fyysisesti toimittajalle.

- **Lähetä ostopyyntöpäivityksiä** – Määritä asetukseksi *Kyllä*, jos haluat lähettää ostotilausten päivityssanoman. Määritä arvoksi *Ei*, jos haluat estää sanoman lähettämisen. Useimmat toimittajat eivät halua vastaanottaa päivityssanomia. Sen sijaan ne vaativat, että asiakas ottaa heihin yhteyttä puhelimitse tai sähköpostitse, jos ostotilausta on tarkoitus muuttaa. Tämä parametri on yleinen parametri, eikä yksittäisille toimittajille voi määrittää ohittamista ulkoisessa luettelossa. Osto tilaus merkitään päivitetyksi, jos kirjaat ostotilaukseen toisen vahvistuksen, mutta toimittaja on jo lähettänyt ensimmäisen vahvistuksen ja kuitannut sen. Jos tehdään toinen vahvistus, mutta ensimmäistä vahvistusta ei ole lähetetty, toinen vahvistus käsitellään uutena asiakirjana. Voit vahvistaa ostotilauksen niin monta kertaa kuin haluat, kunnes yksi vahvistus lähetetään. Seuraava vahvistus katsotaan sitten päivityssanomaksi.
- **Lähetä ostopyyntöjen poistoja** – Määritä asetukseksi *Kyllä*, jos haluat lähettää ostotilausten poistosanoman. Määritä arvoksi *Ei*, jos haluat estää sanoman lähettämisen. Useimmat toimittajat eivät halua vastaanottaa poistosanomia. Sen sijaan ne vaativat, että asiakas ottaa heihin yhteyttä puhelimitse tai sähköpostitse, jos ostotilaus on lähetetty vahingossa. Tämä parametri on yleinen parametri, eikä yksittäisille toimittajille voi määrittää ohittamista ulkoisessa luettelossa. Ostotilaus merkitään poistetuksi, jos peruutat ostotilauksen toimitusketjun hallinnassa.
- **Arkistotiedosto** – Määritä tiedostopolku, johon haluat viedä ja tallentaa arkistoidut cXML-tiedostot. Polkua käytetään, kun suoritat tyhjennystoiminnon **Ostotilauspyyntö**-sivulla.
- **Katurivin merkkien enimmäismäärä** – Määritä enimmäismäärä merkkejä, joita voi käyttää cXML-asiakirjan osoitteiden katukentässä. Tämä yleinen parametri vaikuttaa kaikkiin toimittajiin, ellei ulkoisen luettelon ominaisuuksissa ole määritetty ohitusta.

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>Toimittajan ostotilastojen määrittäminen käyttämään cXML:ää

Aina kun vahvistat ostotilauksen, jossa **Lähetä ostotilaus cXML:llä** -valinnan arvona on _Kyllä_, järjestelmä luo cXML-sanoman automaattisesti ja toimittaa sen toimittajalle, joka liittyy kyseiseen ostotilaukseen. Ostotilausten tätä asetusta voi hallita kahdella tavalla:

- Jos haluat määrittää toimittajan siten, että se käyttää automaattisesti cXML:ää kaikissa uusissa ostotilauksissa, jotka luodaan ostoehdotuksesta, siirry kohtaan **Ostot ja hankinnat \>Toimittaja \> Kaikki toimittajat** ja avaa toimittajan tietosivu valitsemalla tai luomalla toimittaja. Määritä sitten **Ostotilausten oletusarvot** -pikavälilehdellä asetuksen **Lähetä ostotilaus cXML:llä** arvoksi _Kyllä_. Jos cXML:ää käytetään automaattisesti myös uusissa ostotilauksissa, joita **ei** luoda ehdotuksesta, sinun on myös määritettävä liittyvän ulkoisen luettelon **ENABLEMANUALPO**-tilausominaisuuden arvoksi _Tosi_, kuten myöhemmin tämän aiheen osassa [Määritä tilauksen ominaisuudet](#set-order-properties) kuvataan.
- Yksittäisten ostotilausten tietosivuja voit avata valitsemalla tai luomalla ostotilauksen kohdassa **Ostot ja hankinnat \> Ostotilaukset \> Kaikki ostotilaukset**. Siirry **Otsikko**-näkymään ja määritä sitten **Määritys**-pikavälilehdessä asetus **Lähetä ostotilaus cXML:llä** tarpeen mukaan.

![Toimittajien ostotilausten oletusasetukset](media/cxml-order-defaults.png "Toimittajien ostotilausten oletusasetukset")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>Ulkoisen luettelon määrittäminen käyttämään cXML:ää

Voit määrittää PunchOut-toiminnon ja ostotilausten lähetystoiminnon kunkin luettelon **Ulkoiset luettelot** -sivulla. Tähän liittyvät asetukset ovat kohdassa **Ostot ja hankinnat \> Luettelot \> Ulkoiset luettelot**. Aloita [määrittämällä kukin luettelo tavalliseen tapaan](set-up-external-catalog-for-punchout.md). Tähän prosessiin kuuluu toimittajan määrittäminen, niiden luokkien määrittäminen, joita toimittaja saa toimittaa, sekä luettelon aktivointi. Määritä tämän jälkeen tässä osassa kuvatut lisäasetukset.

> [!NOTE]
> Kun vahvistat ostotilauksen, joka voidaan lähettää cXML:llä, järjestelmä hakee ostotilaukseen liittyvän toimittajan ja hakee sitten ensimmäisen aktiivisen ulkoisen luettelon, joka on määritetty kyseiselle toimittajalle. Tämän jälkeen järjestelmä käyttää kyseisen ulkoisen luettelon asetuksia ostotilauksen lähettämiseen. Jos useita ulkoisia luetteloita on määritetty, järjestelmä käyttää vain ensimmäistä löytämäänsä ulkoista luetteloa ostotilauksen toimittajan perusteella. Siksi on suositeltavaa luoda kullekin toimittajalle vain yksi ulkoinen luettelo.

![Ulkoisen luettelon asetukset](media/cxml-supplier-catalog.png "Ulkoisen luettelon asetukset")

### <a name="set-the-punchout-protocol-type"></a>PunchOut-toiminnon protokollatyypin määrittäminen

Määritä **Yleistä**-pikavälilehdessä **Ulkoiset luettelot** -sivulla **PunchOut-protokollatyyppi** -kentän arvoksi _cXML_. Tämä vaihtoehto on ainoa käytettävissä oleva vaihtoehto, ellei kumppani ole laajentanut toimintoa ja tarjoa lisävaihtoehtoa laajennuksessa.

Jos käytät luetteloa myös PunchOut-toiminnossa, sinun myös [määritettävä sanoman muoto](set-up-external-catalog-for-punchout.md). Sanomamuotoa käytetään toimittajayhteyden luomiseen ehdotukseen perustuvassa PunchOut-tapahtumassa. Kun ostotilaus lähetetään, tilauksen ominaisuuksia käytetään toimittajayhteyden luomiseen.

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>Tilauksen ominaisuuksein määrittäminen

_Ostojen cXML-parannukset_-toiminto lisää uuden **Tilausominaisuudet**-pikavälilehden ulkoisia luetteloja varten. Tässä pikavälilehdessä on ruudukko, jossa voit määrittää tilauksen ominaisuudet. Se sisältää myös työkalurivin. Tämä työkalurivi sisältää seuraavat kolme painiketta, joiden avulla voit hallita tilauksen ominaisuuksia:

- **Oletusominaisuudet** – Kun määrität uutta luetteloa, valitse tämä painike, jos haluat lisätä ruudukkoon esimääritetyn, yleisesti käytettyjen ominaisuuksien kokoelman.
- **Uusi** – Lisää ruudukkoon uusi ominaisuus.
- **Poista** – Poista valittuna oleva ominaisuus ruudukosta. Jos poistat oletusominaisuuden vahingossa, palauta puuttuvat ominaisuudet valitsemalla **Oletusominaisuudet**.

Aina kun lisäät vähintään yhden ominaisuuden ruudukkoon, määritä kullekin niistä arvo oikeanpuoleisessa sarakkeessa.

Käytä oletusominaisuuksia seuraavalla tavalla:

- **BUYER\_COOKIE** – Tällä seurantakentällä voidaan ilmaista tiettyjä tietoja yrityksellesi. Jos sinulla ei ole toimittajan kanssa sopimusta tämän ominaisuuden käytöstä, sillä ei ole paljoakaan merkitystä ostotilausta lähetettäessä. Siksi se kannattaa määrittää yksinkertaiseksi arvoksi.
- **DELIVERTO** – Kun toimitusosoite syötetään asiakirjaan ostotilauksesta **Huomautustiedot**-kenttää käytetään **DeliverTo**-kentän täyttämiseen XML-sanomassa. Jos haluat, että tämä arvo on pyynnön lähettäjän nimi, ja määrität ostotilauksen otsikon pyynnön lähettäjä -kentän, syötä tämän ominaisuuden _REQUESTER_ -arvo, jotta pyynnön lähettäjän nimi lisätään XML:n **DeliverTo**-kenttään. Tässä tapauksessa käytetään ensisijaisena sähköpostiosoitteena ja puhelinnumerona pyynnön lähettäjän eikä tilaajan sähköpostiosoitetta ja puhelinnumeroa.
- **DEPLOYMENTMODE** – Määritä tämä ominaisuus toimittajan pyynnön mukaisesti. Arvona on yleensä _TUOTANTO_ tai _TESTI_. Määritä arvo toimittajan kanssa käydyn viestinnän perusteella. Yleensä sen täytyy vastata suunniteltua järjestelmää toimittajan testi- tai tuotantojärjestelmäksi ilmoittaman **ORDERCHECKURL**-arvon taustalla.
- **FIXEDBILLADDRESSID** – Kun XML-sanoman **addressID**-kenttä määritetään, se poimii osoitteessa määritetyn sijainnin. Jos toimittajalle ilmoittamasi tunnusarvo eroaa jostain syystä osoitesijainnin arvosta, voit pakottaa ohituksen määrittämällä arvon tässä. Oletuksena on, että käytät vain yhtä osoitetta toimittajan kanssa ja että osoite määritetään toimittajan järjestelmässä. Laskutusosoite on ensisijainen laskutusosoite, joka on yritykselle on määritetty Supply Chain Managementissa.
- **FIXEDSHIPADDRESSID** – Kun XML-sanoman **addressID**-kenttä määritetään, se poimii osoitteessa määritetyn sijainnin. Jos toimittajalle ilmoittamasi tunnusarvo eroaa jostain syystä osoitesijainnin arvosta, voit pakottaa ohituksen määrittämällä arvon tässä. Oletuksena on, että käytät vain yhtä osoitetta toimittajan kanssa ja että osoite määritetään toimittajan järjestelmässä. Toimitusosoite on osoite, joka on määritetty ostotilauksen otsikossa. Useimmat toimittajat hyväksyvät vain otsikko-osoitteet, eivät riviosoitteita. Vaikka XML-tiedostossa on kenttiä riviosoitteille, ne määritetään otsikko-osoitteeksi.
- **FROM\_DOMAIN** – Syötä arvo, jota käytetään ostotilausasiakirjojen lähettämiseen. Toimittaja toimittaa tämän arvon.
- **FROM\_IDENTITY** – Syötä arvo, jota käytetään ostotilausasiakirjojen lähettämiseen. Toimittaja toimittaa tämän arvon.
- **ORDERCHECKURL** – Syötä URL-osoite, johon ostotilausasiakirjat lähetetään. Tämä URL-osoite alkaa `https://`, ja toimittaja toimittaa sen.
- **PAYLOAD\_ID** – Syötä tietotunnukselle etuliitearvo niiden liiketoimintaprosessien tarpeiden mukaan, jotka ovat käytössä kulloisenkin toimittajan osalta.
- **SENDER\_DOMAIN** – Syötä arvo, jota käytetään ostotilausasiakirjojen lähettämiseen. Toimittaja toimittaa tämän arvon.
- **SENDER\_IDENTITY** – Syötä arvo, jota käytetään ostotilausasiakirjojen lähettämiseen. Toimittaja toimittaa tämän arvon.
- **SHARED\_SECRET** – Syötä arvo, jota käytetään ostotilausasiakirjojen lähettämiseen. Toimittaja toimittaa tämän arvon.
- **STREETLENGTH** – Syötä numero, joka ilmaisee merkkien enimmäismäärän, jonka toimittaja hyväksyy kadun nimeksi. Jos tähän syötetään arvo, se on ensisijainen **cXML-parametrit**-sivulla määritettyyn arvoon nähden. Järjestelmä poistaa rivinvaihdot ja välilyönnit yrittääkseen sovittaa Supply Chain Managementin vakio-osoitteet tässä määritettyyn merkkien enimmäismäärään. Kaikki ylimääräiset merkit katkaistaan.
- **TO\_DOMAIN** – Syötä arvo, jota käytetään ostotilausasiakirjojen lähettämiseen. Toimittaja toimittaa tämän arvon.
- **TO\_IDENTITY** – Syötä arvo, jota käytetään ostotilausasiakirjojen lähettämiseen. Toimittaja toimittaa tämän arvon.
- **USERAGENT** – Syötä arvo, joka ilmoittaa käyttämäsi järjestelmän. Syötä esimerkiksi _Dynamics 365 Supply Chain Management_.
- **VERSION** – Syötä cXML-versionumero, jos toimittaja pyytää tätä tietoa. Oletusversio on *1.2.008*. Tämä versio on vakaa, ja useimmat toimittajat hyväksyvät sen.
- **RESPONSETEXT** – Syötä mikä tahansa mukautettu teksti, jonka odotat toimittajan palauttavan cXML-vastaussanomassa, kun tilaus on lähetetty. Tällä tavoin järjestelmä voi merkitä viestin _kuitatuksi_. Jos vastaus ei vastaa vakiotekstiä tai tähän syöttämääsi asiakastekstiä, pyyntö merkitään _virheeksi_.
- **RESPONSETEXTSUB** – Määritä tämän ominaisuuden arvoksi _TOSI_, jos haluat etsiä toimittajan vastaustekstin arvoille, jotka on määritetty **RESPONSETEXT**-kentässä. Toimittaja voi esimerkiksi palauttaa pitkän merkkijonon, jonka vastaus sisältää merkit "OK". Tällöin voit syöttää _OK_ **RESPONSETEXT**-kenttään ja määrittää **RESPONSETESTSUB**-arvoksi _TOSI_, jolloin merkkejä "OK" etsitään mistä tahansa kohdasta vastausta. Tällöin tilaus voidaan määrittää _kuitatuksi_.
- **CONTENTTYPE** – Tyypillisessä luettelomäärityksessä ei ole tätä ominaisuutta. Jos vastaanotat palvelinvirheen 500 toimittajan järjestelmästä, kun lähetät ostotilauksen, voit suorittaa testauksen määrittämällä tämän ominaisuuden arvoksi _EPÄTOSI_. Tämä arvo muuttaa määrityksen verkkopyynnössä ja saattaa mahdollistaa sanoman lähetyksen joissakin ympäristöissä.
- **ENABLEHEADERS** – Määritä tämän ominaisuuden arvoksi _TOSI_, jotta otsikot lähetään yhdessä ostotilauksen kanssa. Tämän ominaisuuden tarvitsee määrittää vain, jos toimittaja edellyttää sitä. Jos määrität tämän ominaisuuden arvoksi _TOSI_, lisää mukautettuja ominaisuuksia, jotka perustuvat toimittajien ilmoittamiin nimiin, ja määritä niille etuliite _H\__. Tyypillisiä esimerkkejä ovat **H\_USERID**, **H\_PASSWORD**, **H\_RECEIVERID** ja **H\_ACTIONREQUEST**. Seuraavat mukautetut ominaisuudet sisältyvät oletusominaisuuksiin:

    - **H\_USERID** – Jos kauppakumppani edellyttää käyttäjätunnuksen lähettämistä osana ostotilauksen lähettämisen URL-osoitetta, syötä arvo tähän.
    - **H\_PASSWORD** – Jos kauppakumppani edellyttää salasanan lähettämistä osana ostotilauksen lähettämisen URL-osoitetta, syötä arvo tähän.

- **ENABLEMANUALPO** – Jos tämän ominaisuuden arvona on _TOSI_, kun käyttäjät luovat ostotilauksia manuaalisesti (eli kun pohjana ei käytetä ehdotusta), kyseisten ostotilausten **Lähetä ostotilaus cXML:llä** -asetuksen arvo tulee toimittajalta. Jos tätä ominaisuutta ei ole määritetty tai jos sen arvo on _EPÄTOSI_, **Lähetä ostotilaus cXML:llä** -asetusta ei määritetä manuaalisesti luotujen ostotilausten otsikossa. Ehdotuksen perusteella luoduissa ostotilauksissa, **Lähetä ostotilaus cxML:llä** -asetus tulee aina toimittajalta ominaisuuden arvosta riippumatta. Lisätietoja on tämän aiheen aiemmassa [Toimittajan ostotilastojen määrittäminen käyttämään cXML:ää](#vendor-setup) -osassa.
- **PUNCHOUTPOONLY** – Jos tämän ominaisuuden arvoksi määritetään _TOSI_, vain PunchOut-prosessissa luodut ostoehdotuksen rivit määrittävät ostotilauksen otsikon **Lähetä ostotilaus cXML:llä** -asetuksen. Lisäksi kaikkien ostotilausten rivien ostoehdotusrivien tyypin on oltava _Ulkoinen luettelonimeke_. Muussa tapauksessa cXML-ostotilausta ei voi luoda.
- **PUNCHOUTSHIPTO** – Jos tämän ominaisuuden arvoksi on määritetty _TOSI_, yrityksen oletusosoite lisätään PunchOut-määrityspyyntösanomaan, kun käyttäjä avaa ulkoisen luettelon. Tämä osoite lisätään **ShipTo**-osoitteeksi. Toimittajat käyttävät **ShipTo**-osoitetta näyttääkseen yrityksen sijaintiin perustelevaa hinnoittelua.
- **TRACEPUNCHOUT** – Määritä tämän ominaisuuden arvoksi _TOSI_, jos saat virhesanoman, kun yrität siirtyä ehdotuksesta ulkoiseen luetteloon. Tämän jälkeen täytetään Supply Chain Managementin ja toimittajan sivuston välillä lähetettävien **PunchOutSetupRequest**- ja **PunchOutResponse**-sanomien jäljitystiedot. Voit tarkastella näitä tietoja **cXML-ostoskorisanomaloki**-sivulla, jonka voit avata ongelmia aiheuttavan toimittajan tueteluettelon **Ulkoisen luettelon määritys** -sivulta. Tämän ominaisuuden arvoksi pitäisi määrittää _TOSI_ vain, kun olet suorittamassa vianmääritystä, sillä vaatii merkittävästi suorituskykyä tietokannalta kunkin PunchOut-toiminnon osalta. Lisätietoja on myöhemmin tämän aiheen osassa [Ulkoisen luettelon PunchOut-toiminnon cXML-ostoskorisanomalokin tarkastelu](#message-log).
- **REPLACENEWLINE** – Määritä tämän ominaisuuden arvoksi _TOSI_, jos sinulla on siitä johtuva ongelma, että toimittajan järjestelmä lähettää **PunchOutResponse**-sanoman, joka sisältää rivinvaihtomerkkejä (\\n). toimittajaTämä ongelma voi ilmetä, jos toimittajan sanomat jäsennetään väliohjelmiston tai hankintakeskuksen kautta. Jos sinulla on ongelmia uuden toimittajan määritysten kanssa, määritä **TRACEPUNCHOUT**-ominaisuuden arvoksi _TOSI_ tarkasetllaksesi **PunchOutResponse**-sanomaa ja sen määrittämiseksi, erottavatko rivinvaihtomerkit XML-tunnisteita.
- **POCOMMENTS** – Määritä tämän ominaisuuden arvoksi _TRUE_, jos haluat cXML-asiakirjan sisältävän muistiinpanot, jotka lisätään ostotilaukseen Supply Chain managementissa. Liiteteksti lisätään tilaussanoman otsikkokommentteihin. Lisä tietoja siitä, miten järjestelmä valitsee ja käsittelee nämä liitteet on jäljempänä tässä aiheessa osassa [Muistiinpanojen lisääminen ostotilaukseen](#attach-po-notes).
- **VENDCOMMENTS** – Määritä tämän ominaisuuden arvoksi _TRUE_, jos haluat cXML-asiakirjan sisältävän muistiinpanot, jotka lisätään ostotilaukseen Supply Chain managementissa. Liiteteksti lisätään tilaussanoman otsikkokommentteihin. Lisä tietoja siitä, miten järjestelmä valitsee ja käsittelee nämä liitteet on osassa [Muistiinpanojen lisääminen ostotilaukseen](#attach-po-notes).
- **CLEANAMP** – Määritä tämän ominaisuuden arvoksi _TOSI_, jos saat virhesanoman yrittäessäsi suorittaa PunchOut-toimintoa toimittajalle ja toimittajan palauttama URL sisältää virheellisesti koodattuja et-merkkejä (\&).
- **PUNCHOUTTZ** – Määritä tämän ominaisuuden arvoksi _TOSI_, jos toimittajasi käyttää International Organization for Standardizationin (ISO) standardia 8601 suorittaakseen erityisen tarkistuksen PunchOut-pyyntösanoman päivämäärälle/ajalle. Supply Chain Management käyttää Coordinated Universal Time (UTC) -päivämäärää **PunchOutSetupRequest**-sanomassa. Siksi päivämäärä-/aikamuotoon lisätään *+00:00*, kun määrität tämän ominaisuuden arvoksi _TOSI_.
- **WMSADDRESSID** – Määritä tämän ominaisuuden arvoksi _TOSI_, kun haluat käyttää ostotilauksen osoitteen varastonumeroa **addressID**-arvona **ShipTo**-osoitteessa sen ostotilausehdotuksen osalta, joka lähetetään toimittajalle. Jos määrität arvon **FIXEDSHIPADDRESSID**-ominaisuudelle, kyseinen arvo on ensisijainen tähän arvoon nähden. Siksi kannattaa käyttää yhtä ominaisuutta tai toista **addressID**-arvon määrittämisessä asiakirjan **ShipTo**-osoitteessa.
- **PUNCHOUTSHIPTOUSER** – Tämä ominaisuus toimii yhdessä **PUNCHOUTSHIPTO**-omaisuuden kanssa. Jos **PUNCHOUTSHIPTO**-ominaisuuden arvoksi määritetään _TOSI_, yrityksen osoite poimitaan. **PUNCHOUTSHIPTOUSER**-ominaisuuden arvoksi määritetään _TOSI_, PunchOut-käyttäjän ensisijaista osoitetta käytetään yrityksen osoitteen sijaan.

### <a name="activate-the-external-catalog"></a>Ulkoisen luettelon aktivointi

Kun olet määrittänyt kaikki ominaisuudet ja ulkoisen luettelon muut asetukset, siirry takaisin **Ulkoiset luettelot** -sivun **Yleistä**-pikavälilehteen ja määritä **Aktiivinen**-asetuksen arvoksi *Kyllä*.

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>Muistiinpanojen liittäminen ostotilaukseen

Kuten [Tilausten ominaisuuksien määrittäminen](#set-order-properties) -osassa mainitaan, voit määrittää ominaisuuden **POCOMMENTS** ja/tai ominaisuuden **VENDCOMMENTS** arvoksi _TOSI_ ulkoisen luettelon määrityksissä, jos haluat, että toimitettu cXML sisältää tekstiä siihen liittyvästä ostotilauksesta ja/tai toimittajatietueista. Tässä osassa on lis tietoja siitä, miten järjestelmä valitsee ja käsittelee nämä liitteet, jos niitä käytetään.

Voit määrittää kaikki järjestemlän etsimät muistiinpanotyypit kohdassa **Ostot ja hankinnat \> Määritys \> Lomakkeet \> Lomakkeen määritys**. Määritä sitten **Ostotilaus** välilehdessä **Sisällytä tämäntyyppiset asiakirjat** kentän arvoksi niiden muistiinpanojen tyypit, joita haluat voida sisällyttää. Vain tekstihuomautukset sisällytetään, ei asiakirjaliitteitä.

![Lomakkeen määrityssivu](media/cxml-form-setup.png "Lomakkeen määrityssivu")

Ostotilaukset lisätään ostotilaukseen, vain, jos niiden **Tyyppi**-kentän arvona on se arvo, jonka valitset **Sisällytä tämäntyyppiset asiakirjat** -kentässä, ja niiden **Rajoitus**-kentän arvona on _Ulkoinen_. Voit luoda, tarkastella tai muokata ostotilauksen liitteitä siirtymällä kohtaan **Ostot ja hankinnat \> Kaikki ostotilaukset**, valitsemalla tai luomalla ostotilauksen ja sitten valitsemalla **Liitteet**-painikkeen (paperiliitinsymboli) oikeassa yläkulmassa.

![Liitetty muistiinpano, joka on määritetty toimittajalle lähetettäväksi](media/cxml-note-to-vendor.png "Liitetty muistiinpano, joka on määritetty toimittajalle lähetettäväksi")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>Ulkoisen luettelon PunchOut-toiminnon cXML-ostoskorisanomalokin tarkastelu

Kun **PunchOut-protokollatyyppi**-kenttä määritetään ulkoisen luettelon osalta arvoon _cXML_, järjestelmä tallentaa sanomalokin niistä ostoskoreista, jotka palautetaan toimittajilta. Tätä lokia voidaan käyttää vianmääritykseen ja muihin tietotarkoituksiin.

Jos haluat avata ulkoisen luettelon lokin, valitse haluamasi luettelo ja valitse sitten toimintoruudussa **cXML-ostoskorin sanomaloki**. **cXML-ostoskorin sanomaloki** -sivulla näkyy luettelo palautetusta ostoskoreista, näihin ostoskoreihin liittyvän XML-tiedoston sekä rivit, jotka on luotu asiaan liittyvässä ostoehdotuksessa.

![cXML-ostoskorin sanomalokisivu](media/cxml-cart-message-log.png "cXML-ostoskorin sanomalokisivu")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>Ulkoisen luettelon PunchOut-tominnon ulkoisten elementtien määrittäminen

Kun määrität **PunchOut-protokollattyypi**-kentän arvoksi *cXML* ulkoisen luettelon osalta, voit lisätä mukautettuja ulkoisia elementtejä, jotka lisätään oikeaan paikkaan puunnön XML-sanomassa.

Voit lisätä ulkoisia elementtejä ulkoiseen luetteloon seuraavasti.

1. Siirry kohtaan **Ostot ja hankinnat \> Luettelot \> Ulkoiset luettelot**.
1. Valitse haluamasi luettelo.
1. Valitse **Ulkoiset**-osan **Sanoman muoto** -pikavälilehdessä **Lisää** lisätäksesi rivin kunkin sellaisen ulkoisen elementin ruudukkoon, jonka haluat lisätä. Määritä kullakin rivillä seuraavat kentät:

    - **Nimi** – Syötä elementille nimi. Tästä arvosta tulee kullekin riville luotavan **Ulkoinen**-XML-elementin **Nimi**-määrite. Yleensä pyrit sopimaan kunkin ulkoisen elementin nimestä toimittajasi kanssa.
    - **Arvo** – Valitse elementin arvo. Tästä arvosta tulee kullekin riville luotavan Ulkoinen-XML-elementin Nimi-määrite. Käytettävissä ovat seuraavat arvot:

        - **Käyttäjänimi** – Käytä PunchOut-toimintoa käyttävän käyttäjän nimeä. Tämä on kirjautumisnimi Supply Chain Managementia varten.
        - **Käyttäjän sähköposti** – Käytä PunchOut-toimintoa käyttävän käyttäjän sähköpostiosoitetta. Tämä osoite on osoite, jonka käyttäjä on määrittänyt **Käyttäjäasetukset**-sivun **Tili**-välilehdessä.
        - **Satunnaisarvo** – Käytä yksilöllistä satunnaisarvoa.
        - **Käyttäjän koko nimi** – Käytä ulkoista luetteloa käyttävälle käyttäjälle määritetyn yhteyshenkilön koko nimeä.
        - **Firstname** – Käytä ulkoista luetteloa käyttävälle käyttäjälle määritetyn yhteyshenkilön etunimeä.
        - **Lastname** – Käytä ulkoista luetteloa käyttävälle käyttäjälle määritetyn yhteyshenkilön sukunimeä.
        - **Puhelinnumero** – Käytä ulkoista luetteloa käyttävälle käyttäjälle määritetyn yhteyshenkilön ensisijaista puhelinnumeroa.

![Ulkoisten elementtien asetukset](media/cxml-extrinsics.png "Ulkoisten elementtien asetukset")

Käyttäjä tai järjestelmänvalvoja ei näe ulkoisia elementtejä, koska niitä ei lisätä, ennen kuin käyttäjä suorittaa PunchOut-toiminnon. Ne lisätään automaattisesti cXML-määritysmyyntösanoman elementtien **BuyerCookie** ja **BrowserFromPost** väliin. Siksi niitä ei tarvitse määrittää manuaalisesti XML-tidostossa, kun määrität ulkoista luetteloa.

![Ulkoiset elementit lisätään XML-tiedostoon](media/cxml-extrinsics-xml.png "Ulkoiset elementit lisätään XML-tiedostoon")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>Ostotilauksen luonti ja käsittely

Kun luot toimittajalle ostotilauksen, siinä käytetään kyseisen toimittajan **Lähetä ostotilaus cXML:llä** -asetuksen määritystä. Asetus on kuitenkin edelleen kätettävissä ostotilauksen **Otsikko**-näkymän **Määritys**-pikavälilehdessä, joten voit muuttaa sitä myöhemmin tarpeen mukaan.

![Ostotilaus määritetään käyttämään cXML:ää](media/cxml-purchase-order.png "Ostotilaus määritetään käyttämään cXML:ää")

Kun luot ostotilauksen ostoehdotuksesta, joka on peräisin PunchOut-työnkulusta, kaikki pakolliset rivitiedot täytetään. Tämän jälkeen voit lisätä ostotilausrivejä manuaalisesti tai kopioida niitä muista ostotilauksista. Muista määrittää kaikki pakolliset kentät. Näihin pakollisiin kenttiin kuuluu ulkoinen viitenumero, joka on cXML-sanomassa käytettävä toimittajanumero.

![Esimerkki ulkoisesta viitenumerosta](media/cxml-line-details.png "Esimerkki ulkoisesta viitenumerosta")

Kun olet täyttänyt kaikki ostotilauksen tiedot, muista vahvistaa se. Sanomaa ei lähetetä, ellei ostotilausta ole vahvistettu. Valitse toimintoruudussa **Osto**-välilehdellä **Toiminnot**-ryhmässä **Vahvista** vahvistaaksesi ostotilauksen. 

Kun ostotilaus on vahvistettu, voit tarkastella vahvistuksen tilaa **Ostotilausvahvistukset** -kirjauskansioiden avulla. Napsauta toimintoruudussa **Osto**-välilehdellä **Kirjauskansiot**-ryhmässä **Ostotilausvahvistukset**.

Kullakin ostotilauksella voi olla useita vahvistuksia. Kukin vahvistus merkititään lisänumerolla. Seuraavassa kuvassa ostotilaus on *00000275* ja vahvistus *00000275-1*. Tämä numerointi vastaa Supply Chain Managementin vakiotoimintoa, jossa ostotilauksen muutokset ja siten toimittajalle lähetettävän cXML-sanoman tyyppi tunnistetaan vahvistuksen perusteella. Kuten kuvassa näkyy, **Ostotilausvahvistukset**-sivu sisältää myös kentät **Tilauksen lähetystila** ja **Tilauspyynnön toimittajan tila**. Lisätietoja tällä sivulla mahdollisesti näkyvistä eri tila-arvoista esitetään myöhemmin tämän aiheen osassa [Ostotilauspyynöjen seuranta](#monitor-po-requests).

![Ostotilausvahvistusten sivu](media/cxml-po-confirmations.png "Ostotilausvahvistusten sivu")

Jos haluat tarkastella lisätietoja asaikirjasta, valitse ruudukon yläpuolelta **Ostotilauspyyntö**.

**Ostotilauspyyntö**-sivulla on kaksi ruudukkoa. Sivun yläosassa olevalla ruudukolla on yksi tietue kutakin lähetettäväksi merkittyä ostotilausta varten. Sivun alaosan **Ostotilauspyyntöjen historia** -välilehden ruudukossa voi olla useita tietueita valitulle ostotilaukselle, jotta kunkin vahvistuksen tila ilmaistaisiin. Seuraavassa kuvassa näkyy ostotilaus 00000275 yläruudukossa ja tiedosto 00000275-1 **Ostotilauspyyntöjen historia** -välilehden ruudukossa.

![Ostotilauspyyntöjen sivu](media/cxml-po-request.png "Ostotilauspyyntöjen sivu")

Jos erätyö on määritetty ja sitä suoritetaan, asiakirja lähetetään. Voit tarkastella tilan muutosta, kun asiakirja on lähetetty. Seuraavassa kuvassa **Tilauksen lähetysarvo**-kentän arvona on _Lähetetty_. **Tilauspyynnön toimittajan tila** -kentän arvona on _Kuitattu_, millä ilmaistaan, että toimittaja on saanut asiakirjan ja on pystynt lukemaan sen ja tallentamaan sen järjestelmään. **Ostotilauspyyntöjen historia** -välilehdessä näkyy aika, jona asiakirja lähetettiin. Lisätietoja tällä sivulla mahdollisesti näkyvistä eri tila-arvoista esitetään osassa [Ostotilauspyynöjen seuranta](#monitor-po-requests).

![Tilasanomat ostotilauspyyntöjen sivulla](media/cxml-po-request-2.png "Tilasanomat ostotilauspyyntöjen sivulla")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>Ostotilauspynnön erätyön ajoittaminen

Voit aktivoida ostotilauspyyntöjen lähettämisen erätyön siirtymällä kohtaan **Ostot ja hankinnat \> Määritys \> cXML-hallinta \> Ostotilauspyyntö** ja valitsemalla sitten toimintouudussa **Ostotilauspyyntö**-välilehdessä **Erä**-ryhmän ja sitten **Lähetä työ**, jolloin **Ostotilauksen valmsitelu ja lähetys** -valintaikkuna aukeaa. Tämän valint ikkunan avulla voit määrittää toistumisen samalla tavalla kuin yleensä tehdään erätöille Supply Chain Managementissa. Valitse toistoväli tilausmäärän perusteella. Vaikka voit suorittaa erätyön joka minuutti, lienee parasta lähettää eriä koko työpäivän ajan toimittajien aikatauluja vastaavien tilausten vastaanottoikkunoiden perusteella.

Toimittajalla voi esimerkiksi olla käytäntö, jonka mukaan kaikki tilaukset, jotka vastaanotetaan klo 13.00 mennessä, lähetetään samana päivänä. Tällöin saatat joutua suorittamaan erän vain muutaman kerran aamulla ilmoittaksesi kaikki tilauksesi. Jäljelle jäävät tilaukset lähetetään seuraavana päivänä. Tämä päätös on puhtaasti liiketoiminnallinen päätös. Voit tarkistaa sen ja määrittää parametrit tarkistuksen mukaisesti.

Prosessi etsii osto tilauspyyntöasiakirjoja, joiden tila on *Odottaa*. Jos sinulla on tilaus, joka on lähetettävä toimittajalle heti, voit valita **Lähetä työ** ja määrittää **Eräkäsittely**-asetukseksi *Ei*.

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>Ostotilauspyyntöjen seuranta

### <a name="view-the-status-of-a-purchase-order"></a>Ostotilauksen tilan tarkasteleminen

Kun cXML:llä lähetettävissä olevat tilaukset vahvistetaan, ne siirtyvät _Odottaa_-tilaan. Kuten esitimme [Ostotilauksen luominen ja käsitteleminen](#create-po) -osassa, voit tarkastella ostotilauksen tilaa **Ostotilauspyyntö**-sivulla. Kullakin ostotilauspyynnöllä voi olla yksi useista tiloista sen parametreista ja tiedoista riippuen. Tässä osassa kuvataan eri tila tyyppejä ja arvoja, joita niillä voi olla. Näiden tietojen avulla voit hallita ongelmia ja ymmärtää ostotilausten tilan.

![Ostotilauksen tila ostotilauspyyntöjen sivulla](media/cxml-monitor-po-request.png "Ostotilauksen tila ostotilauspyyntöjen sivulla")

**Ostotilauspyyntö**-sivun yläosan ruudukossa voivat näkytä seuraavat tila-arvot:

- **Tilauksen lähetystila** – Tällä kentällä voi olla jokin seuraavista arvoista:

    - **Odottaa** – Asiakirja odottaa lähettämistä.
    - **Lähetetty** – Asiakirja on lähetetty.
    - **Pysäytetty** – Asiakirja on merkitty tilaan _Pysäytetty_ ennen lähettämistään. (Asiakirja merkitään _Pysäytetty_-tilaan valitsemalla **Pysäytä** **Ostotilauspyyntö**-sivulla.)
    - **Arkisto** – Asiakirja on tyhjennetty. (Asiakirja ttyhjennetään valitsemalla **Tyhjennä** **Ostotilauspyyntö**-sivulla.)

- **Tilauspyynnön toimittajan tila** – Tällä kentällä voi olla jokin seuraavista arvoista:

    - **Odottaa** – Asiakirja odottaa lähettämistä.
    - **Kuitattu** – Asiakirja on kuitattu toimittajan vastaanottamaksi. Voit tarkistaa toimittan palauttaman yksityiskohtaisen XML-sanoman valitsemalla **Vastaus-XML**-välilehden sivun alaosasta.
    - **Virhe** – Asaikirja lähetettiin toimittajalle, mutta tapahtui virhe. Voit tarkistaa virhesanoman valitsemalla **Vastaus-XML**-välilehden sivun alaosasta.

**Ostotilauspyyntö**-sivun alaosan ruudukossa **Ostotilauspyyntöjen historia** -välilehdessä voi olla jokin seuraavista arvoista:

- **Tilauspyynnön tyyppi** – Tällä kentällä voi olla jokin seuraavista arvoista:

    - **Uusi** – Rivi merkitään uudeksi heti, kun ostotilaus on vahvistettu.
    - **Päivitys** – Jos vahvistus on jo lähetetty ja toimittaja on kuitannut sen, seuraavan vahvistuksen arvoksi merkitään _Päivitetty_. Päivitykset lähetetään vain, jos **Lähetä ostopyyntöpäivityksiä** -asetuksen arvoksi on määritetty *Kyllä* [Yleisissä cXML-parametreissa](#cxml-parameters).
    - **Poista** – Jos vahvistus on jo lähetetty ja toimittaja on vahvistanut sen, mutta ostotilaus perutaan, odottavan vahvistuksen arvona on _Poista_. Poistot lähetetään vain, jos **Lähetä ostopyyntöpoistoja** -asetuksen arvoksi on määritetty *Kyllä* [Yleisissä cXML-parametreissa](#cxml-parameters).

- **Pyynnön aika** – Aika, jolloin tilausvahvistus on luotu. Voit verrata pyynnön aikaa tilauksen tilan aikaan ja määrittää vahvistuksen ja toimittajan kuittauksen välisen ajan sen perusteella.
- **Tilauksen lähetystila** – Tämä kenttä on sama kuin **Tilauksen lähetystila** -kenttä sivun yläosassa. Se toistuu tässä, jotta sitä voidaan helpommin tarkastella vahvistuksen tasolla. Jos **Tilauspyynnön tyyppi** -kentän arvona on *Uusi* ja ostotilaus on vahvistettu uudelleen ennen vahvistuksen lähettämistä, **Tilausksen lähetystila**-kentän arvona on *Arkisto*.
- **Tilauksen tilan aika** – Aika, jolloin ostotilauspyynnön historiatietue on viimeksi päivitetty. (Tilamuutokset lasketaan päivityksiksi.)
- **Tilauspyynnön toimittajan tila** – Tämä kenttä on sama kuin **Tilauspyynnön toimittajan tila** -kenttä sivun yläosassa. Se toistuu tässä, jotta sitä voidaan helpommin tarkastella vahvistuksen tasolla.
- **Uudelleenlähetyksen aika** – Aika, jolloin tietue on lähetetty uudelleen.
- **Uudelleenlähetysten määrä** – Se, kuinka usein tietue on lähetetty uudelleen. Suuri määrä viittaa useisiin virheisiin ja siten mahdolliseen ongelmaan joko sinun tai toimittajan tietomäärityksessä.

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>Ostotilauspyyntösanoman XML-tiedoston tarkasteleminen

Voit tarkastella ostopyyntösanoman XML-tiedostao valitsemalla **Pyydä XML-teksti** -välilehti **Ostotilauspyyntö**-sivun alaosasta. Tämän välilehden tiedoista voi olla hyötyä testauksen tai virheiden tarkistamisen yhteydessä. Jos haluat helpottaa tietojen lukemista, voit tarkastella sitä muotoiltuna sanomana. Kopioi välilehden sisältö tekstitiedostoon ja avaa se sitten XML-editorissa.

![XML-tekstin pyytämisen välilehti](media/cxml-request-xml-text.png "XML-tekstin pyytämisen välilehti")

### <a name="view-the-details-of-the-vendor-response"></a>Toimittajan vastauksen tietojen tarkastelu

Voit tarkastella toimittajan kuittauksen tai virhevastauksen valitsemalla **Vastaus-XML** -välilehden **Ostotilauspyyntö**-sivun alaosasta.

![Vastau-XML-välilehti](media/cxml-response-xml.png "Vastau-XML-välilehti")

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköiseen hankintaan siirtymisessä käytettyjen ulkoisten luetteloiden määrittäminen](set-up-external-catalog-for-punchout.md)
- [Siirtyminen sähköiseen hankintaan ulkoisten luetteloiden avulla](use-external-catalogs-for-punchout.md)
