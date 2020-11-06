---
title: Luo toimipaikkadirektiivit
description: Tässä ohjeaiheessa käsitellään sijaintidirektiivien luontia. Sijaintidirektiivit ovat käyttäjän määrittämiä sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa.
author: Mirzaab
manager: tfehr
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-28
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 4f634b7f526fd198b394af6d3870c43ee560813e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016767"
---
# <a name="create-location-directives"></a>Luo toimipaikkadirektiivit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään sijaintidirektiivien luontia. Sijaintidirektiivit ovat käyttäjän määrittämiä sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa. Esimerkiksi myyntitilaustapahtumassa sijaintidirektiivi määrittää, mistä nimikkeet kerätään, ja minne kerätyt nimikkeet sijoitetaan.

> [!NOTE]
> Tämä ohjeaihe koskee **Varastonhallinta** -moduulin ominaisuuksia. Se ei koske [Inventoinnin- ja varastonhallinta](../inventory/inventory-home-page.md) -moduulin ominaisuuksia.

Voit käyttää sijaintidirektiiviä seuraavien tehtävien suorittamiseen:

- Aseta pois saapuvat nimikkeet.
- Kerää ja vaiheista lähteväin tapahtumien nimikkeet.
- Valitse ja sijoita tuotannon raaka-aineet.
- Täydennyssijainnit.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit luoda sijaintidirektiivin, sinun on varmistettava, että edellytykset ovat olemassa, noudattamalla näitä ohjeita.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Varastot**.
1. Luo varasto.
1. Valitse **Varasto** -pikavälilehdellä **Käytä varastonhallintaprosesseja** -vaihtoehdon arvoksi *Kyllä*.
1. Luo toimipaikat, toimipaikkojen tyypit, toimipaikkojen profiilit ja toimipaikkojen muodot. Lisätietoja on kohdassa [Sijaintien määrittäminen VHJ-yhteensopivassa varastossa](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Luo toimipaikkoja, alueita ja vyöhykeryhmiä. Lisätietoja on kohdassa [Varaston määrittäminen](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) ja [Sijaintien määrittäminen VHJ-yhteensopivassa varastossa](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="setup"></a>Luo perustiedot

### <a name="create-location-directives"></a>Luo toimipaikkadirektiivit

Luo sijaintidirektiivi noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Määritä luetteloruudussa **Työtilauksen tyyppi** -kentässä sen varastotapahtuman tyyppi, jolle olet luomassa sijaintidirektiiviä.
1. Valitse toimintoruudussa **Uusi** luodaksesi sijaintidirektiivin.
1. Määritä uuden sijaintidirektiivin kentät seuraavassa taulukossa kuvatulla tavalla.

    | Kenttä | kuvaus |
    |---|---|
    | Järjestysnumero | Määritä kokonaisluku, joka ilmaisee sijaintidirektiivin järjestyspaikan. Järjestyssijainnit määrittävät milloin jokainen sijaintidirektiivi käsitellään valitulle työtilaustyypille. |
    | Nimi | Kirjoita nimi toimipaikkadirektiiville. | 
    | Työtyyppi | Valitse työn tyyppi, joka tulisi suorittaa. Arvoluettelo riippuu valitsemastasi varastotapahtuman tyypistä **Työtilaustyyppi** -kentässä. Arvot, jotka saattavat olla käytettävissä:<ul><li>**Laita** – Sijaintidirektiivi yrittää löytää parhaan sijainnin, joka sijoittaa tai paikantaa varaston, joka tulee järjestelmään vastaanoton, tuotannon tai varaston oikaisujen avulla. Sijaintidirektiivin avulla määritetään myös hyllytyssijainti tai lopullinen ruuman oven lähetyssijainti lähtevässä työnkulussa.</li><li>**Poiminta** – Sijaintidirektiivi pyrkii löytämään parhaat sijainnit, jotta varasto voidaan varata fyysisesti (luoda työ). Kerää-vaihe voidaan suorittaa loppuun (eli Kerää-työlinja voidaan sulkea), vaikka työ ei ole valmis. Käyttäjä voi suorittaa fyysisen keräyksen. Järjestelmässä tämä toimenpide on poimintavaihe. Käyttäjä voi sitten peruuttaa työn mobiililaitteella ja suorittaa työn loppuun (esimerkiksi laiton) myöhemmin. Työn otsikko kuitenkin ensin suljetaan, kun lopullinen Aseta-vaihe on valmis.</li><li>**Inventointi** , **Oikaisut** , **Mukautus** , **Varaston tilan muutos** , **Rekisterikilven luonti** , **Tulostus** , **Tilan muutos** ja **Pakkaa sisäkkäisiin rekisterikilpiin** – Näitä ei voi käyttää missään sijaintidirektiivin määrityksessä.</li></ul> |
    | Toimipaikka | Valitse toimipaikka, jossa työn on valmistuttava. |
    | Varasto | Valitse varaston sijainti, jossa työn on valmistuttava. |
    | Direktiivikoodi | Valitse direktiivikoodi ohjaamaan työmalliin asetettuihin riveihin liittyvien sijaintidirektiivien valintaa, joilla tämä koodi on määritetty. Voit luoda **Direktiivikoodi** -sivulla uusia koodeja, joiden avulla työmalli voidaan liittää sijaintidirektiiviin. Voit käyttää tätä sivua myös linkin luomiseen työmallin rivin ja sijaintidirektiivin välille (kuten lastausovi tai väliaikainen sijainti). Katso lisätietoja siitä, miten määrität direktiivikoodin työmallilla kohdasta [Varastotyön hallinta työmallien ja sijaintidirektiivien avulla](control-warehouse-location-directives.md).<p>Jos direktiivikoodi on määritetty, kun työ täytyy luoda, järjestelmä etsii sijaintidirektiivit direktiivikoodin perusteella järjestyksen sijasta. Tällä tavoin voit olla tarkempi sijaintimallin suhteen, jota käytetään tiettyyn työmallin vaiheeseen, kuten esimerkiksi materiaalien vaiheittaiseen valmisteluun.</p> |
    | Käsittelykoodi | Valitse käsittelykoodi ohjaamaan vastaanotettujen nimikkeiden poispano toimipaikkaan. (Lisätietoja on kohdassa [Määritä käsittelykoodit](tasks/set-up-dispositions-codes.md) -koodit.) Tämä kenttä on käytettävissä vain, kun **Työtilauksen tyyppi** -kentän arvona on *Ostotilaukset* , *palautuksen tilaukset* tai *Valmiit tavarat hyllytetään*. |
    | Useita varastointiyksiköitä | Valitsemalla tämän vaihtoehdon arvoksi *Kyllä* voit käyttää useita varastoyksikköjä (SKU:ta) sijainnissa. Esimerkiksi tämän vaihtoehdon arvoksi on oltava määritetty *Kyllä* lastausovelle.<p>Jos **Usean SKU** -asetuksen arvoksi on määritetty *Kyllä* , hyllytyssijainti määritetään työssä (odotetusti). Varastopaikan sijainti voi kuitenkin käsitellä useita nimikeosia vain, jos työhön kuuluu erilaisia SKU-arvoja, jotka on keräilty ja hyllytetään, ei, jos työhön kuuluu vain yksi SKU, joka on otettava käyttöön.</p><p>Jos **Useita varastointiyksiköitä** -valinnan arvoksi on asetettu *Ei* , Aseta-sijainti määritetään vain, jos Aseta-vaiheessa on vain yhdentyyppinen varastointiyksikkö.</p><p>Molempien lähestymistapojen käyttäminen edellyttää, että määrität kaksi riviä, joilla on sama rakenne ja asetukset, mutta määrität **usean SKU** -asetuksen arvoksi *Kyllä* yhdelle riville ja *Ei* toiselle. Toisin sanoen, Aseta-toimintoja varten sinulla on oltava samanlaiset sijaintidirektiivit, vaikka sinun ei tarvitse tehdä eroa yhden ja useamman varastointiyksikön välillä työn tunnuksessa. Tarvitset myös paikkadirektiivin keräystä varten, jos tilauksessa on useampi kuin yksi nimike.</p><p>**Huomaa:** Jos asetat **Usean SKU:n** -asetukseksi *Kyllä* *Aseta* -työtyypin sijaintidirektiiville, järjestelmä valitsee aina ensimmäisen sijaintidirektiivirivin, riippumatta muista linjoille asetetuista rajoituksista.</p> |

1. Valinnainen: Valitse toimintoruudusta **Muokkaa kyselyä** valitaksesi sijainnit tai määrittääksesi mahdolliset rajoitukset, jotka kohdistetaan, kun valitset tietyn sijaintidirektiivin.
1. Luo **Rivit** -pikavälilehdellä yksi tai useampi rivi yksiköiden määrittämiseksi ja määrän paikallistamiseksi tai varaamiseksi varastossa.
1. Määritä uuden sijaintidirektiivin kentät kullakin uudella rivillä seuraavassa taulukossa kuvatulla tavalla.

    | Kenttä | kuvaus |
    |---|---|
    | Järjestysnumero | Määritä kokonaisluku, joka ilmaisee sijaintidirektiivin järjestyspaikan. Järjestyssijainnit määrittävät milloin jokainen sijaintidirektiivi käsitellään valitulle työtyypille. |
    | Määrästä | Määritä alkava määräalue, kun keskiruudukon järjestys on valittava. Määritä määrä mittayksikössä, joka on valittu **Yksikkö** -kentässä. |
    | Määrälle | Määritä loppuva määräalue, kun keskiruudukon järjestys on valittava. Määritä määrä mittayksikössä, joka on valittu **Yksikkö** -kentässä. |
    | Yksikkö | Valitse nimikkeiden mittayksikkö.<p>Voit määrittää vähimmäismäärän ja enimmäismäärän, jota direktiivi koskee. Voit myös määrittää, että direktiiviä käytetään tietyssä varastoyksikössä. Rivin **yksikkö** -kenttää käytetään vain määrän arviointiin.</p><p>Järjestelmä arvioi määrät käyttäen rivillä määritettyä **yksikkö** -arvoa määrittääksesi, sovelletaanko sijaintidirektiivin riviä. Aina kun direktiivisijainnin riville pääsee, järjestelmä yrittää muuntaa kysynnän yksikön rivillä määritetyksi yksiköksi. Jos yksikkömuunnosta ei ole, järjestelmä siirtyy seuraavalle riville.</p> |
    | Etsi määrä | Tämä kenttä on voimassa vain, kun yrität sijoittaa tai paikantaa määrän varastosta. Toisin sanoen se on voimassa vain *Aseta* -työlle. Valitse menetelmä, jolla voit arvioida, onko määrä **Määrästä** - ja **Määrään** -kenttien määrittämällä alueella. Jos toimipaikkaohjeistus on tulevalle tapahtumalle, valitse jokin seuraavista vaihtoehdoista:<ul><li>**Rekisterikilpien määrä** ─ Käytä vastaanotettavan rekisterikilven määrää arvioidaksesi, onko määrä tavoitellulla määräalueella.</li><li>**Määrä, jolle määrätty yksikkö** ─ Käytä vastaanotettavan rekisterikilven määrää arvioidaksesi, onko määrä määrätty tapahtuman aikana. Esimerkiksi jos voit vastaanottaa varastoon määrän 1 000 ja jakaa sen kymmeneen sadan rekisterikilven joukkoon, voit käyttää määrää 1000 nimikettä 100:n rekisterikilven sijasta.</li><li>**Jäljellä oleva määrä** – Arvioidaksesi, onko määrä tavoitellulla määrialueella, käytä määrää, joka on vielä saatavana ostotilausrivillä, joka on tällä hetkellä kirjautumassa.</li><li>**Odotettu määrä** – Arvioidaksesi, onko määrä tavoitemäärän alueella, käytä ostotilausrivin kokonaismäärää riippumatta jo vastaanotetusta määrästä.</li></ul> |

1. Valinnainen: Voit määrittää seuraavia lisäkenttiä **Rivit** -pikavälilehdellä.

    | Kenttä | kuvaus |
    |---|---|
    | Rajoita yksikön mukaan | Valitse tämä valintaruutu, jos haluat rajoittaa mittayksiköitä, joita pidetään sijaintidirektiivin rivien kelvollisena valintaperusteena. Kun mittayksiköt on määritetty, vain nimikkeet, joiden yksikkö vastaa vähintään yhtä yksikkösarjaryhmälle määritettyä yksikköä, katsotaan kelvolliseksi rivivalintaan.<p>Yksikkö on esimerkiksi rajattu kuormalavoihin, ja nimike on liitetty yksikkösarjaryhmään, joka sisältää *kuormalavat* -yksikön. Tässä tapauksessa nimikkeitä käsitellään sijaintidirektiivin kelvollisena vaihtoehtona.</p><p>**Rajoita yksiköittäin** -valintaruutu ei kuitenkaan vaikuta työriveillä käytössä olevaan yksikköön tai yksiköihin. Yksikkörajoitus koskee vain yksiköitä, jotka on asetettu saataville yksikkösarjaryhmän kautta.</p><p>Esimerkiksi nimike liitetään yksikkösekvenssiryhmään, joka sisältää sekä *kuormalava* - että *kappale* -yksikön. Mittayksikkö on määritetty, jossa 1 kuorma lava = 100 kpl ja sijaintidirektiivissä käytetään **Rajoita yksikön mukaan** -toimintoa vain kuormalavoille. Lisäksi on määritetty työmalli, joka rajoittaa työotsikon luomisen 50 kappaleeseen. Tässä tapauksessa luodaan 50 kappaleen työrivit.</p><p>Voit määrittää rajoituksen mittayksikön noudattamalla seuraavia ohjeita.</p><ol><li>Valitse **Rivit** -pikavälilehdessä **Rajoita yksikkökohtaisesti**. Tämä painike on käytettävissä vain, kun valitset rivin **Rajoita yksiköittäin** -valintaruudun ja valitset sitten **Tallenna**.</li><li>Valitse **Yksikkö** -kentässä mittayksikkö keräily- ja poispanoprosessin rajoittamiseksi.</li></ol> |
    | Kokoa yksikköön | Valitsemalla tämän voit määrittää, tuleeko raaka-aineen keräys pyöristää ylöspäin materiaalin käsittely-yksikön kerrannaiseen, joka on määritetty **Rajoita yksikön mukaan** -kentässä. Tämä kenttä koskee vain raaka-aineen keräämistä ja *Kerää* -tyyppisiä sijaintidirektiivejä. |
    | Etsi pakkausmäärä | Valitse tämä valintaruutu, jos pakkausluettelon määrä on määritetty **Myyntitilaus** -sivulla. Jos valitset tämän valintaruudun, vain sijainnit, joilla on tämän pakkausluettelon määrät ovat valittuina. |
    | Salli jakaminen | Valitse tämä valintaruutu, jos haluat jakaa määrän eri sijainteihin. |
    | Välittömän täydennyksen malli | Muodosta yhteys täydennysmalliin, jotta täydennys voidaan aloittaa välittömästi, jos kohteita ei kohdisteta. Jos jätät kentän tyhjäksi, kohteiden täydennystä ei aloiteta, ennen kuin sijaintidirektiivin kaikki rivit on käsitelty.<p>Tämä kenttä on käytettävissä vain valituissa työtilaustyypeissä, joissa täydennys on sallittu, kuten *myyntitilaukset* ja *raaka-aineiden poiminta*.</p> |

1. Napsauta **Sijaintidirektiivitoiminnot** -pikavälilehdellä **Uusi** valitaksesi sijainnin tai sijaintialueen.
1. **Järjestysnumero** -kentässä näkyy, missä järjestyksessä valitun työtyypin sijaintidirektiivi käsitellään. Voit muuttaa järjestystä. Varo kuitenkin sijaintidirektiivin toimenpiteiden järjestysnumeroita, koska sijaintidirektiivitoimenpiteet suoritetaan aina tässä järjestyksessä.
1. Syötä **Nimi** -kenttään sijaintidirektiivin toiminnon nimi. Ole tarkka, että on selvää, mikä toiminto on.
1. Valinnainen: Valitse **Muokkaa kyselyä** muuttaaksesi varastosijainteja ja muita ehtoja.
1. Valinnainen: Voit määrittää sijainnin direktiiviin seuraavia lisäkenttiä.

    | Kenttä | kuvaus |
    |---|---|
    | Kiinteän sijainnin käyttö | Valitse, mitä sijainteja sijaintidirektiivin tulisi käsitellä:<ul><li>**Kiinteät ja ei-kiinteät sijainnit** – Sijaintidirektiivi harkitsee kaikkia sijainteja.</li><li>**Vain kiinteät sijainnit tuotteelle** – Sijaintidirektiivi harkitsee vain kiinteitä sijainteja tuotteille.</li><li>**Vain kiinteät sijainnit tuotevariantille** – Sijaintidirektiivi harkitsee vain kiinteitä sijainteja tuotevarianteille.</li></ul> |
    | Salli negatiivinen varasto | Valitse tämä valintaruutu, jos haluat sallia negatiivisen varaston määritetyssä varastosijainnissa. |
    | Erä käytössä | Valitse tämä valintaruutu, jos haluat käyttää erästrategioita nimikkeille, joille erä on käytettävissä. Jos tämä valintaruutu on valittuna ja **strategia** -kentän arvoksi on määritetty *ei mitään* , järjestelmä siirtyy seuraavaan toimenpideriviin. |
    | Strategia | Valitse strategia, jota sijaintidirektiivissä tulisi käyttää:<ul><li>**Ei mitään** – Strategiaa ei käytetä.</li><li>**Täsmäytä pakkausmäärä** – Tämä strategia varmistaa, onko keräyssijainnille määritetty pakkausmäärä. Tämä strategia on voimassa vain, kun **työtyyppi** -kentän arvona on *poiminta*.</li><li>**Konsolidoi** – Tämä strategia konsolidoi tietyssä sijainnissa olevia nimikkeitä, kun vastaavat nimikkeet ovat jo käytettävissä.. Tämä strategia on voimassa vain, kun **työtyyppi** -kentän arvona on *Aseta*. Järjestelmän tyypillisessä määrityksessä järjestelmä yrittää konsolidoida ensimmäisellä toimenpiderivillä ja sitten toisen toimenpiderivin se yrittää ottaa käyttöön ilman konsolidointia. Tuotteiden konsolidointi tehostaa keräystä vastaisuudessa.</li><li>**FEFO-erävaraus** – Tätä strategiaa käytetään, kun varasto paikannetaan käyttämällä erän vanhentumispäivää ja se kohdistetaan erävaraukseen. Ensimmäistä erääntymisajankohtaa (FEFO) erävarausstrategiaa käytetään myös silloin, kun varaston sijainti löytyy käyttämällä erän parasta ennen -päivämäärää viimeisen käyttöpäivän lisäksi. Voit käyttää tämän strategian vain eränimikkeissä. Tämä strategia on voimassa vain, kun **työtyyppi** -kentän arvona on *poiminta*. Kun valitset tämän strategian, ohitat käytössä olevien eränumeroiden kyselyn lajittelun.</li><li>**Pyöristä kokonaiseen rekisterikilpeen** – Tämä strategia pyöristää varastomäärän niin, että se vastaa rekisterimerkinnän määrää, joka on osoitettu valittaville tavaroille. Tätä strategiaa voidaan käyttää vain varastopaikkadirektiivien täydennystyypissä ja vain, kun **työtyyppi** -kentän arvoksi on määritetty *poiminta*.</li><li>**Tyhjä sijainti ilman saapuvia töitä** – Tätä strategiaa käytetään tyhjien sijaintien paikantamiseen. Sijainnin katsotaan olevan tyhjä, jos sillä ei ole fyysistä varastoa, eikä odotettuja saapuvia töitä. Tämä strategia on voimassa vain, kun **työtyyppi** -kentän arvona on *Aseta*.</li></ul> |

## <a name="example-of-the-use-of-location-directives"></a>Esimerkki sijaintidirektiivien käytöstä.

Tarkastele tätä esimerkkiä varten ostotilausprosessia, jossa sijaintidirektiivin on löydettävä varastosta vapaata kapasiteettia varastonimikkeille, jotka on juuri rekisteröity vastaanottolaiturilla. Sinun on ensin löydettävä varastosta vapaata kapasiteettia konsolidoimalla nykyiseen käsillä olevaan varastoon. Jos konsolidointi ei ole mahdollista, sinun on löydettävä tyhjä sijainti.

Tätä skenaariota varten sinun on määritettävä kaksi sijaintidirektiivitoimintoa. Sarjan ensimmäisen toiminnon on käytettävä **Konsolidointi** -strategiaa, ja toisen tulisi käyttää **Tyhjä sijainti ilman saapuvia töitä** -strategiaa. Jollet määritä kolmatta toimintoa käsittelemään ylivuotoskenaariota, on mahdollista saada kaksi lopputulosta, kun varastossa ei ole enää kapasiteettia: työ voidaan luoda, vaikka sijainteja ei ole määritetty, tai työn luontiprosessi saattaa epäonnistua. Tulos määrittyy sivun **Sijaintidirektiivivirheet** määrityksistä, joissa voit päättää, valitaanko **Pysäytä työ sijaintidirektiivivirheeseen** -asetus kullekin työtilaustyypille.

## <a name="next-step"></a>Seuraava vaihe

Kun olet luonut sijaintidirektiivit, voit liittää kunkin direktiivikoodin työmallin koodiin työn luomista varten. Lisätietoja on kohdassa [Varastotyön valvonta työmallien ja sijaintidirektiivien avulla](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="technical-information-for-system-admins"></a>Teknisiä tietoja järjestelmänvalvojille

Jos sinulla ei ole niiden sivujen käyttöoikeutta, joita käytetään tämän tehtävän suorittamiseen, ota yhteys järjestelmänvalvojaan ja anna seuraavassa taulukossa näkyvät tiedot.

| Luokka | Edellytys |
|---|---|
| Configuration Keys | Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**. Laajenna **Kaupan** lisenssiavain ja valitse **Varaston- ja kuljetuksenhallinnan** määritysavain. |
