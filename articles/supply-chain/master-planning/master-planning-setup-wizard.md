---
title: Pääsuunnittelun asetusten ohjattu toiminto
description: Tässä ohjeaiheessa käsitellään erilaisia pääsuunnittelun määrittämisessä käytettäviä tärkeitä strategioita ja parametreja.
author: t-benebo
manager: tfehr
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 2f2ec94b8d3bce9ca9fb565fe06b268f5c7458fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005024"
---
# <a name="master-planning-setup-wizard"></a>Pääsuunnittelun asetusten ohjattu toiminto

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on opas **pääsuunnittelun asetusten ohjattuun toimintoon**. Se selittää, miten parametriehdotukset lasketaan, ja sisältää myös esimerkkejä, jotka näyttävät, miten eri yritykset määrittävät pääsunnittelun liiketoimintatarpeidensa perusteella.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

[Pääsuunnittelun asetusten ohjattu toiminto Dynamics 365 Supply Chain Managementissa](https://youtu.be/c-e6n-8rZb4) -video (näkyy ylempänä) sisältyy [Finance and Operations -soittolistaan](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavilla YouTubessa.


## <a name="specific-requirements-of-your-company"></a>Yrityksesi erityisvaatimukset

Ohjatun toiminnon ensimmäisellä sivulla kysytään yrityksesi erityisistä vaatimuksista. Vastauksia näihin kysymyksiin ei tarvitse olla tarkka, mutta sinun pitäisi pystyä tarjoamaan karkea arvio nimikkeiden määrästä ja suunnitelluista tilauksista yrityksessä. Vastauksia käytetään määrittämään parametreja, jotka koskevat yritystä, ei vain pääsuunnitelmaa, jonka valitsit. Seuraavissa osissa kuvataan parametrit, jotka on laskettu ja kaavat, joita käytetään.

### <a name="number-of-threads"></a>Säikeiden määrä

- **Jos valmistat mitä tahansa nimikkeitä:** säikeiden määrä = suunniteltujen tilausten määrä ÷ 1 000
- **Jos et valmista nimikkeitä:** säikeiden määrä = nimikkeiden määrä ÷ 1 000

Jos laskettujen säikeiden määrä ylittää 75 prosenttia käytettävissä olevasta säikeiden määrästä, se on rajattu 75 prosenttiin kunkin asiakkaan käytettävissä olevien säikeiden määrästä. (Kullekin asiakkaalle määritetään käytettävissä olevien säikeiden määrä.)

Katso lisätietoja kohdasta [Säikeiden määrä](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).

### <a name="bundle-size"></a>Myyntirakenteen koko

Nipun kooksi asetetaan arvo **1**. Tämä arvo on usein paras arvo, koska se auttaa parantamaan pääsuunnittelun suorituskykyä.

Lisätietoja on kohdassa [Lisätyöaseman tehtävänipun tehtävien määrä](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).

### <a name="firming-bundle-size"></a>Vahvistavan nipun koko

- **Jos valmistat mitä tahansa tuotetta:** vahvistavan nipun koko asetetaan suuremmalle näistä kahdesta arvosta: **10** ja nipun laskenta.
- **Jos et valmistat nimikkeitä:** vahvistavan nipun koko asetetaan suuremmalle näistä kahdesta arvosta: **50** ja nipun laskenta.

Nipun laskenta = (suunniteltujen tilausten määrä × (vahvistuksen aikaraja ÷ kattavuuden aikaraja) ÷ säikeiden määrä) ÷ 10

### <a name="cache-size"></a>Välimuistin koko

Välimuistin kooksi asetetaan arvo **Maksimi**. Tämä arvo on usein paras arvo, koska se auttaa parantamaan pääsuunnittelun suorituskykyä.

Lisätietoja on kohdassa [Ajan kohdistaminen työnipun töihin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).

### <a name="manufacturing-setup"></a>Valmistuksen asetukset

Jos valmistat nimikkeitä, **Valmistuksen asetukset** -sivu tulee myöhemmin näkyviin ohjatussa toiminnossa.

## <a name="scope-of-the-current-plan"></a>Nykyisen suunnitelman laajuus

Ohjatun toiminnon **Nykyisen suunnitelman laajuus** -sivulla vastaat kysymyksiin, jotka liittyvät siihen, kuinka pitkälle tulevaisuudessa eri tarpeet otetaan huomioon ja lasketaan pääsuunnittelussa. Jokainen kysymys kysyy, haluatko käyttää ominaisuutta ja miten haluat määrittää sen.

Jos kyseessä on esimerkiksi ennustesuunnitelmatoiminto, ohjattu toiminto kysyy: "Haluatko käyttää ennustesuunnitelmaa pääsuunnittelussa, jotta suunniteltuja tilauksia ehdotetaan ennakoidun kysynnän täyttämiseksi?".

Käytettävissä ovat seuraavat asetukset:

- **Ei** – Pääsuunnittelu ei ehdota suunniteltuja tilauksia ennusteen täyttämiseksi. **Pääsuunnitelmat**-sivun **Aikarajat**-välilehdessä (**Pääsuunnittelu \> Asetukset \> Suunnitelmat \> Pääsuunnitelmat**) ohjattu toiminto määrittää **Ennustesuunnitelma (aikaraja)** -asetukseksi **Kyllä** ja määrittää päivien määräksi **0** (nolla). Tämä asetus ohittaa kattavuusryhmässä määritetyn aika rajan. Koska päivien määrän arvoksi on määritetty **0** (nolla), ominaisuutta ei käytetä.
- **Kyllä, kuten määritetty tässä pääsuunnitelmassa** – kenttä tulee käyttöön, johon voit syöttää päivien lukumäärän, jonka pääsuunnittelu ehdottaa suunniteltuja tilauksia, jotka täyttävät ennustetun kysynnän. Ohjattu toiminto määrittää **Ennustesuunnitelma (aikaraja)** -asetukseksi **Kyllä** ja määrittää päivien määräksei sen päivien määrän, joka syötetään **Ennustesuunnitelma**-kenttään **Pääsuunnitelmat**-sivun **Aikarajat**-välilehdessä. Nämä asetukset korvaavat kattavuusryhmissä asetetut arvot.
- **Kyllä, kuten määritetty kattavuudessa** – ohjattu toiminto määrittää **Ennustesuunnitelma (aikaraja )** -asetukseksi **Ei**. Aikarajat, jotka on määritetty kattavuusryhmässä käytetään määrittämään, kuinka kauan aiot suunnitella ennusteelle.

Tämän sivun jäljellä olevat kysymykset ja niiden vastaukset noudattavat samaa rakennetta:

- **Ei** – **Ennustesuunnitelma (aikaaja)** -asetukseksi määritetään **Kyllä**, ja päivien lukumääräksi **0** (nolla).
- **Kyllä, kuten määritetty tässä pääsuunnitelmassa** – **Ennustesuunnitelma (aikaraja )** -asetukseksi määritetään **Kyllä**. Päivien määrä, jonka syötät, käytetään ja se ohittaa arvot, jotka on määritetty kattavuusryhmissä.
- **Kyllä, kuten määritetty kattavuusryhmässä** – **Ennustesuunnitelma (aikaraja )** -asetukseksi määritetään **Ei**.

Lisätietoja kohdassa [Töiden ajoitus](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="scheduling-options"></a>Aikataulutusvaihtoehdot

**Aikataulutusvaihtoehdot**-sivu tulee näkyviin vain, jos vastasit **Kyllä** kohdassa "Valmistat mitä tahansa suunnitelluista nimikkeistä?". kysymys ohjatun toiminnon ensimmäisellä sivulla.

Vastauksesi ensimmäiseen kysymykseen tällä sivulla ("Pitääkö ajoittaa yksittäisiin töihin jaettuja toimintoja?") määrittää ajoitusmenetelmän **Yleiset**-välilehdessä **Pääsuunnitelmat**-sivulla.

- **Kyllä** – työn aikataulutusta käytetään.
- **Ei** – työvaiheiden ajoitusta käytetään.

Lisätietoja: [Työvaiheiden ajoitus](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) ja [Töiden ajoitus](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="updates-of-demand-and-supply"></a>Kysynnän ja tarjonnan päivitykset

**Kysynnän ja tarjonnan päivitykset** -sivun kysymykset liittyvät vahvistuksiin, toimintoviesteihin ja viivytyksiin.

Pääsuunnittelun asetukset päivitetään vastausten perusteella saman skeeman mukaan, joka on kuvattu edellisessä osassa:

- **Ei** – **Aikaraja** -asetukseksi määritetään **Kyllä** **Pääsuunnitelmat**-sivulla, ja päivien lukumääräksi **0** (nolla).
- **Kyllä, kuten määritetty tässä pääsuunnitelmassa** – **Aikaraja** -asetukseksi määritetään **Kyllä**. Päivien määrä, jonka syötät, käytetään ja se ohittaa arvot, jotka on määritetty kattavuusryhmissä.
- **Kyllä, kuten määritetty kattavuusryhmässä** – **Aikaraja**-asetukseksi määritetään **Ei**.

Lasketuissa viiveissä vastaukset ohjatun toiminnon kysymyksiin päivittävät vastaavat parametrit **Pääsuunnitelmat** -sivun **Lasketut viiveet** -välilehdessä.

## <a name="summary-of-your-changes"></a>Yhteenveto tekemistäsi muutoksista

Ohjatun toiminnon viimeisellä sivulla näkyvät muutokset, joita suositellaan vastausten perusteella. Se näyttää sekä asetusten arvon (**nykyiset asetukset**) että ohjatun toiminnon suositteleman arvon (**Uusi kokoonpano**).

Voit myös muokata uuden konfiguraation parametreja. Parametrit erotetaan parametreihin, jotka koskevat yritystä ja parametreja, jotka koskevat vain valitsemaasi pääsuunnitelmaa. Jos haluat tarkastella kaikkia asetusparametreja, joita voidaan muuttaa ohjatun toiminnon avulla, valitse sivun alareunasta **Näytä kaikki parametrit**. Tämän jälkeen voit muuttaa parametreja.

Lopuksi, kun valitset **Valmis**, uusi konfiguraatio on käytössä. Jos valitset **Peruuta**, mitään muutoksia ei käytetä.

## <a name="examples"></a>Esimerkkejä

Tässä osassa kuvataan kahden fiktiivisen yrityksen määrittäminen näyttämään, miten asetukset voivat muuttua kunkin yrityksen tarpeiden mukaan.

### <a name="example-1-contoso-manufacturer"></a>Esimerkki 1: Contoso Manufacturer

Contoso Manufacturer on valmistava yritys, joka valmistaa kaiuttimia. Se ostaa eri toimittajilta erilaisia raaka-aineita ja komponentteja, joita käytetään lopullisten kaiuttimiin. Tässä muutamia ominaisuuksia sen hankinnasta ja valmistuksesta:

- Lopullisilla nimikkeillä, jotka yritys valmistaa, on tuoterakenne.
- Kaikki lopulliset nimikkeet ja komponentit suunnitellaan pääsuunnittelun avulla. Manuaalista suunnittelua ei ole tehty.
- Kunkin lopullisen nimikkeen tuotannolle määritetään työreitti.
- Valmistuslaitos tuottaa lopulliset nimikkeet. Siinä on määritelty määrä jyrsintä- ja porauskoneita, joita käytetään komponenttien käsittelyyn. Näiden koneiden on käsiteltävä eri komponentteja.
- On monia toimittajia. Nimikkeiden keskimääräinen läpimenoaika on yksi viikko. Saman toimittajan nimikkeiden ryhmän läpimenoaika on seitsemän viikkoa.

Ohjatussa toiminnossa seuraavat arvot syötetään Contoso Manufacturerille:

- **Kattavuus:**

    - **Kysymys:** "Haluatko määrittää suunnitteluhorisontin päivien lukumäärän?"
    - **Vastaus:** "Kyllä, kuten kattavuusryhmissä on määritelty".

    Koska nimikkeiden läpimenoaika on hyvin erilainen, Contoson ei tarvitse suunnitella kaikkia nimikkeitä samalle kaudelle tulevaisuudessa. Nimikkeiden kattavuusryhmät luodaan. Nimikkeet, joilla on samanlainen läpimenoaika, määritetään samalle kattavuusryhmälle. Kunkin kattavuusryhmän (eli kattavuuden aikarajan) suunnitteluhorisontti on suunnilleen läpimenoaika sekä yhden viikon marginaali. Pääsuunnittelu varmistaa, että nimikkeet suunnitellaan etukäteen niiden läpimenoajan perusteella.

    Tämän vuoksi tässä esimerkissä luodaan kaksi kattavuusryhmää. Yhdellä kattavuusryhmällä on kattavuuden aikaraja kahden viikon, ja toisella on kattavuuden aikaraja kahdeksan viikkoa.

    Jos valitaan vastaus **Kyllä, kuten määritetty tässä pääsuunnitelmassa**, päivien määrän tulee ylittää kaikkien nimikkeiden pisin toimitusaika. Koska monia nimikkeitä ei kuitenkaan tarvitse suunnitella niin paljon etukäteen, monet suunnitellut tilaukset lasketaan, mutta niitä ei käytetä koskaan. Tämän vuoksi pääsuunnittelun ajoaika pitenee.

- **Aikatauluttaminen:**

    - **Kysymys:** "Pitääkö ajoittaa yksittäisiin töihin jaettuja toimintoja?"
    - **Vastaus:** "Kyllä."

    Contoson Manufacturingin on suunniteltava ja aikataulutettava yksittäiset työt, jotka suoritetaan tuotantotiloissa. Siksi se käyttää töiden ajoitusta.

- **Kapasiteetti:**

    - **Kysymys:** "Haluatko ajoittaa resurssien kapasiteetin avulla?"
    - **Vastaus:** "Kyllä, kuten tässä pääsuunnitelmassa on määritelty". Syötetään **10 päivää**.

    Jyrsin- ja porauskoneiden määrä on rajallinen. Tuotannonsuunnittelussa on otettava tämä rajoitus huomioon ja järjestettävä työt ajoissa resurssien kapasiteetin mukaan. Toisin sanoen ajoitetut työt suunnitellaan uudelleen resurssien rajoitusten perusteella. Suunnittelussa käytetään läpimenoaikaa määritetyn kauden lisäksi. (Suunnitellut tuotantotilaukset voivat olla päällekkäisiä.) Koska nimikkeiden tuotannon läpimenoaika on seitsemän päivää, pääsuunnittelun resurssien kapasiteettia tarkastellaan 10 päivän kuluessa.

- **Järjestys:**

    - **Kysymys:** "Haluatko järjestää suunnitellut tilaukset käyttämällä tuotteen järjestysarvoja?"
    - **Vastaus:** "Kyllä, kuten kattavuusryhmissä on määritelty".

    Kunkin lopullisen nimikkeen tuotannolle määritetään reitti. Tämän vuoksi pääsuunnittelu ajoittaa tilaukset ajoissa määritettyjen reittien mukaan.

- **Hajotus:**

    - **Kysymys:** "Haluatko suunnitella kaikkien tuoterakenteen elementtien tilaukset (ylätason ja kaikkien alatason nimikkeiden suunnittelu)?"
    - **Vastaus:** "Kyllä, kuten kattavuusryhmissä on määritelty".

    Kaikki nimikkeet, joita käytetään tuotannossa, on suunniteltava. Koska nimikkeiden läpimenoajat ovat hyvin erilaiset, pääsuunnittelun suorituskyky paranee, kun se käyttää kattavuusryhmiä. Jälleen yhden viikon marginaali voidaan syöttää, ja hajotus voidaan tehdä samaan aikaan kuin kattavuus.

### <a name="example-2-contoso-retailer"></a>Esimerkki 2: Contoso Retailer

Contoso Retailer on muotialan jakeluyritys. Se käyttää pääsuunnittelua laskeakseen, milloin osto tilaukset tulisi sijoittaa sen ennustetun myynnin perusteella. Tässä muutamia sen ominaisuuksista:

- Contoso Retailer ennustaa myyntiä kysynnän ennusteen avulla. Ostotilaukset suunnitellaan ennusteen mukaan.
- Liikkeet käyttävät täydennysehdotuksia.
- Kaikkien nimikkeiden läpimenoaika päävarastosta kuhunkin myymälään on noin kaksi viikkoa.

Ohjatussa toiminnossa seuraavat arvot syötetään Contoso Retailerille:

- **Ennustettu kysyntä:**

    - **Kysymys:** "Haluatko käyttää ennustesuunnitelmaa pääsuunnittelussa, jotta suunniteltuja tilauksia ehdotetaan ennakoidun kysynnän täyttämiseksi?"
    - **Vastaus:** "Kyllä, kuten tässä pääsuunnitelmassa on määritelty".

    Contoso on sisällyttänyt kysynnän ennusteen myynnin ennustamiseksi. Siksi pääsuunnittelun on suositeltava suunniteltuja tilauksia ennusteen täyttämiseksi.

- **Vahvistus:**

    - **Kysymys:** "Haluatko, että pääsuunnittelu vahvistaa automaattisesti suunnitellut tilaukset tilausasiakirjoihin, esimerkiksi tuotanto- tai ostotilauksiin?"
    - **Vastaus:** "Kyllä, kuten tässä pääsuunnitelmassa on määritelty". Syötetään **1 päivä**.

    Koska Contoso Retailer luo ostotilaukset suoraan suunnitelluista ostotilauksista, on hyödyllistä, jos suunnitellut ostotilaukset vahvistetaan automaattisesti. Koska yritys suorittaa pääsuunnittelun joka päivä, yhden päivän vahvistuksen aikaraja vahvistaa automaattisesti kaikki tilaukset, joita tarvitaan seuraavana päivänä.

- **Hyväksytyt ehdotukset:**

    - **Kysymys:** "Haluatko sisällyttää kysyntää hyväksytyistä ehdotuksista vähittäismyymälöiden täydentämiseksi?"
    - **Vastaus:** "Kyllä, kuten tässä pääsuunnitelmassa on määritelty". Syötetään **1 päivä**.

    Contoso käyttää liikkeiden hyväksyttyjä ehdotuksia luodakseen suunniteltuja ostotilauksia näiden myymälöiden täydentämiseksi. Koska pääsuunnittelu suoritetaan joka päivä, edellisen päivän ehdotukset sisällytetään suunnitteluun.
