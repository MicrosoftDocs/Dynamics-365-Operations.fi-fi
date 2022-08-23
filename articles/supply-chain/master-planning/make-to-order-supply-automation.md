---
title: Tilauksesta valmistukseen -tarjonnan automatisointi
description: Tässä artikkelissa kuvataan, kuinka Tilauksesta valmistukseen -tarjonnan automatisointiominaisuuden lisäämät parannukset määritetään ja kuinka niitä käytetään.
author: t-benebo
ms.date: 07/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-27
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9044acb472548a797ed387b08ca6892459785793
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220554"
---
# <a name="make-to-order-supply-automation"></a>Tilauksesta valmistukseen -tarjonnan automatisointi

[!include [banner](../includes/banner.md)]

*Tilauksesta valmistukseen -tarjonnan automatisointi* -ominaisuus lisää useita parannuksia Microsoft Dynamics 365 Supply Chain Managementiin. Nämä parannukset sallivat sinun suorittaa seuraavia tehtäviä:

- Tarkastele resurssin kapasiteetin kuormitusta käyttäjän määrittämänä jaksona ja ota käyttöön kapasiteetin kuormituksen pitkäaikainen arviointi.
- Paranna joustavuutta ohjaamalla viivetoleranssia (negatiiviset päivät) kussakin pääsuunnitelmassa.
- Pidä tuotteet saatavilla viime hetken tilauksia varten ja optimoi olemassa olevan tarjonnan käyttö. Tämä saavutetaan käyttämällä viimeisintä mahdollista tarjontaa kysyntää varten sen sijaan, että käytettäisiin ensimmäistä mahdollista tarjontaa.
- Pidä komponenttien määritys joustavana tuotantotilauksissa vahvistuksen jälkeen. Tämän jälkeen järjestelmä voi optimoida viime hetken muutokset kysynnässä. Toisin sanoen rajoita merkintää vain yhdellä tasolla.
- Ohjaa jokaisen myyntitilauksen täyttämiskäytäntöä. Oletusasetukset saadaan asiakkaan määrityksestä.
- Paranna konsernin sisäistä tiedonkulkua. Ostotilaukset päivitetään sisältämään toimitustavan, toimitusehtojen ja ulkoisen nimikenumeron kentät. Tämä muutos varmistaa, että kysynnän yksityiskohtaiset tiedot siirretään toimittavalle yritykselle.

Tässä artikkelissa kuvataan, kuinka parannukset määritetään ja kuinka niitä käytetään.

> [!NOTE]
> Kaikki tässä artikkelissa kuvatut parannukset koskevat järjestelmiä, jotka käyttävät sisäistä pääsuunnittelua. Myös Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin apuohjelma tukee seuraavaa kahta parannusta:
>
> - Pääsuunnitelmien viivetoleranssi
> - Pääsuunnittelun aikana käytetyn tarvekohdistusjärjestyksen hallinta

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Tilauksesta valmistukseen -tarjonnan automatisointiominaisuuden ottaminen käyttöön

Ennen kuin voit käyttää tässä artikkelissa kuvattua ominaisuutta, sinun täytyy ottaa sen käyttöön järjestelmällesi. Järjestelmänvalvojat voivat käyttää [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilaa, jossa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Pääsuunnittelu*
- **Toiminnon nimi:** *Tilauksesta valmistukseen -tarjonnan automatisointi*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Kapasiteetin kuormitus -sivulla näytettävien päivien määrän asettaminen

Voit tarkistaa resurssin saatavilla olevan kapasiteetin **Kapasiteetin kuormitus** -sivulta. *Tilauksesta valmistukseen -tarjonnan automatisointi* -ominaisuus parantaa **Kapasiteetin kuormitus** -sivua lisäämällä siihen **Päivien määrä** -kentän. Voit käyttää tätä kenttää rajoittaaksesi **Yleiskuvaus**-ruudukossa näytettävien päivien määrää. Määrittämäsi arvo tallennetaan muistiin. Jos siis poistut sivulta ja palaat sille myöhemmin, **Yleiskuvaus**-ruudukko näyttää edelleen määrittämäsi määrän päiviä.

Noudata seuraavia ohjeita avataksesi **Kapasiteetin kuormitus** -sivun, josta voit tarkastaa yksittäisen resurssin kapasiteetin.

1. Siirry kohtaan **Organisaation hallinto \> Resurssit \> Resurssit**.
1. Valitse tarkastettava resurssi.
1. Valitse toimintoruudun **Resurssi**-välilehden **Näytä**-ryhmästä **Kapasiteetin kuormitus**.
1. Käytä **Päivien määrä** -suodatinta rajoittaaksesi **Yleiskuvaus**-ruudukossa näytettävien päivien määrää.

Noudata seuraavia ohjeita avataksesi **Kapasiteetin kuormitus** -sivun, josta voit tarkastaa resurssiryhmän kapasiteetin.

1. Siirry kohtaan **Organisaation hallinto \> Resurssit \> Resurssiryhmät**.
1. Valitse tarkastettava resurssiryhmä.
1. Valitse toimintoruudun **Resurssiryhmä**-välilehden **Näytä**-ryhmästä **Kapasiteetin kuormitus**.
1. Käytä **Päivien määrä** -suodatinta rajoittaaksesi **Yleiskuvaus**-ruudukossa näytettävien päivien määrää.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Yhden merkintätason käyttäminen suunniteltujen tilausten vahvistamisessa

*Merkintää* käytetään linkittämään kysyntä ja tarjonta. Se muistuttaa *tarvekohdistusta*, joka ilmaisee, miten pääsuunnittelun odotetaan kattavan kysynnän. Merkintä on kuitenkin pysyvämpi kuin tarvekohdistus. *Tilauksesta valmistukseen -tarjonnan automatisointi* -ominaisuus sallii varastomerkinnän rajoittamisen yhteen tasoon, kun suunniteltuja tilauksia vahvistetaan. Se lisää **Vahvistaminen**-valintaikkunan **Päivitä merkintä** -kenttään seuraavat uudet vaihtoehdot, kun olet vahvistamassa suunniteltua tilausta:

- *Yksitasoinen vakio* – Käytetään yksitasoista merkintää. Yksitasoinen merkintä merkitsee vain päänimikkeen, ei sen tuoterakennekomponentteja (BOM). Näin ollen voit pitää tuotantotilausten komponenttien määrityksen joustavana vahvistuksen jälkeen. Yksitasoinen merkintä sallii järjestelmän optimoida viime hetken muutokset kysynnässä. Kun yksitasoisen merkinnän tyyppi on *vakio*, tarvetilaukset merkitään niiden täyttämistilausten mukaan, mutta täyttämistilauksia ei merkitä, jos niillä on jäljellä oleva määrä.
- *Yksitasoinen laajennettu* – Käytetään yksitasoista merkintää. Kun yksitasoisen merkinnän tyyppi on *laajennettu*, tarvetilaukset merkitään niiden täyttämistilausten mukaan ja täyttämistilaukset merkitään aina riippumatta jäljellä olevasta määrästä.

Nämä vaihtoehdot ovat käytettävissä myös **Pääsuunnittelun parametrit** -sivun **Vakiopäivitys**-välilehden **Päivitä merkintä** -kentässä, kun määrität oletusvalintaa **Vahvistus**-valintaikkunalle.

Lisätietoja on kohdassa [Varaston merkintä suunnittelun optimoinnin avulla](planning-optimization/marking.md).

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>Viivetoleranssin (negatiivisten päivien) asettaminen pääsuunnitelman tasolla

*Tilauksesta valmistukseen -tarjonnan automatisointi* -ominaisuus lisää mahdollisuuden määrittää viivetoleranssi (negatiiviset päivät) pääsuunnitelman tasolla. Asetusta voi käyttää myös nimikkeen kattavuuden ja kattavuusryhmän tasoilla. Jos negatiiviset päivät on määritetty useammalla kuin yhdellä tasolla, järjestelmä määrittää käytettävän asetuksen seuraavan hierarkian mukaan:

- Jos **Pääsuunnitelmat**-sivulla on määritetty negatiivisia päiviä, kyseinen asetus ohittaa kaikki muut negatiivisten päivien asetukset, kun suunnitelma suoritetaan.
- Jos negatiiviset päivät on määritetty **Nimikkeen kattavuus** -sivulla, kyseinen asetus korvaa kattavuusryhmän asetuksen.
- **Kattavuusryhmät**-sivulla määritetyt negatiiviset päivät ovat voimassa vain, jos asiaankuuluvalle nimikkeelle tai pääsuunnitelmalle ei ole määritetty negatiivisia päiviä.

Noudata näitä ohjeita määrittääksesi negatiiviset päivät pääsuunnitelmalle.

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse luetteloikkunasta pääsuunnitelma tai luo uusi.
1. Määritä **Aikarajat päivissä** -pikavälilehden **Negatiiviset päivät** -asetukseksi *Kyllä*.
1. Syötä viereiseen kenttään negatiivisten päivien sallittu määrä.

Lisätietoja negatiivisten päivien käytöstä on kohdassa [Viivetoleranssi (negatiiviset päivät)](planning-optimization/delay-tolerance.md).

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>Pääsuunnittelun aikana käytetyn tarvekohdistusjärjestyksen hallinta

Pääsuunnittelu käyttää *tarvekohdistusjärjestystä* määrittääkseen, mikä tarjonta kattaa minkäkin kysynnän. *Tilauksesta valmistukseen -tarjonnan automatisointi* -ominaisuus lisää uuden **Käytä viimeisintä mahdollista toimitusta** -vaihtoehdon, jolla voit hallita tarvekohdistusjärjestystä tarkemmin. Tämä uusi vaihtoehto sallii sinun pitää tuotteet saatavilla viime hetken tilauksia varten ja optimoida olemassa olevan tarjonnan käytön. Tämä saavutetaan käyttämällä viimeisintä mahdollista tarjontaa kysyntää varten sen sijaan, että käytettäisiin ensimmäistä mahdollista tarjontaa.

Voit määrittää tarvekohdistusjärjestyksen pääsuunnitelman, nimikkeen kattavuuden tai kattavuusryhmän tasolla. Jos tarvekohdistusjärjestys on määritetty useammalla kuin yhdellä tasolla, järjestelmä määrittää käytettävän asetuksen seuraavan hierarkian mukaan:

- Jos tarvekohdistusjärjestys on määritetty **Pääsuunnitelmat**-sivulla, kyseinen asetus korvaa kaikki muut tarvekohdistusjärjestyksen asetukset, kun suunnitelma suoritetaan.
- Jos tarvekohdistusjärjestys on määritetty **Nimikkeen kattavuus** -sivulla, kyseinen asetus korvaa kattavuusryhmän asetuksen.
- **Kattavuusryhmät**-sivulla määritetty tarvekohdistusjärjestys on voimassa vain, jos tarvekohdistusjärjestyksen asetuksia ei ole määritetty asiaankuuluvalle nimikkeelle tai pääsuunnitelmalle.

Jos haluat määrittää tarvekohdistuksen kattavuusryhmän tasolla, noudata seuraavia ohjeita.

1. Siirry kohtaan **Pääsuunnittelu \> Määritys \> Kattavuus \> Kattavuusryhmät**.
1. Valitse luetteloikkunasta ryhmä tai luo uusi.
1. Määritä tarvekohdistusjärjestys käyttämällä **Yleiset**-pikavälilehden **Tarvekohdistusjärjestys**-osion **Kuluta käytettävissä olevaa varastoa**- ja **Käytä viimeisintä toimitusta** -kenttiä. Tämän osion myöhemmässä taulukossa näytetään, miten nämä asetukset yhdistetään tarvekohdistusjärjestyksen määrittämiseksi.

Jos haluat määrittää tarvekohdistuksen nimikkeen kattavuuden tasolla, noudata seuraavia ohjeita.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse ruudukosta tuote tai luo uusi.
1. Valitse toimintoruudun **Suunnitelma**-välilehdessä **Nimikekattavuus**.
1. **Nimikkeen kattavuus** -sivulla on rivejä, joiden avulla voit määrittää nimikettä koskevat kattavuussäännöt kussakin varastossa. Valitse ruudukosta rivi tai luo uusi.
1. Valitse **Yleiset**-välilehdestä **Ohita tarvekohdistusjärjestys** -valintaruutu.
1. Määritä tarvekohdistusjärjestys käyttämällä **Kuluta käytettävissä olevaa varastoa**- ja **Käytä viimeisintä toimitusta** -kenttiä. Tämän osion myöhemmässä taulukossa näytetään, miten nämä asetukset yhdistetään tarvekohdistusjärjestyksen määrittämiseksi.

Jos haluat määrittää tarvekohdistuksen pääsuunnitelman tasolla, noudata seuraavia ohjeita.

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse luetteloikkunasta pääsuunnitelma tai luo uusi.
1. Määritä **Yleiset**-pikavälilehdessä **Ohita tarvekohdistusjärjestys** -asetukseksi *Kyllä*.
1. Määritä tarvekohdistusjärjestys käyttämällä **Kuluta käytettävissä olevaa varastoa**- ja **Käytä viimeisintä toimitusta** -kenttiä. Tämän osion myöhemmässä taulukossa näytetään, miten nämä asetukset yhdistetään tarvekohdistusjärjestyksen määrittämiseksi.

Seuraava taulukko näyttää, miten **Kuluta käytettävissä olevaa varastoa**- ja **Käytä viimeisintä toimitusta** -asetukset yhdistetään tarvekohdistusjärjestyksen määrittämiseksi.

| | Käytä viimeisintä toimitusta = Kyllä | Käytä viimeisintä toimitusta = Ei |
|---|---|---|
| **Kuluta käytettävissä olevaa varastoa** = *Ennen kaikkia toimituksia* | <ol><li>Käytettävissä oleva</li><li>Nykyinen toimitus, joka vastaa kysyntäpäivää</li><li>Nykyinen toimitus, joka ei vastaa kysyntäpäivää, mutta joka on silti negatiivisten päivien sisällä</li><li>Luo uusi toimitus (suunniteltu tilaus)</li></ol> | <ol><li>Käytettävissä oleva</li><li>Nykyinen toimitus, joka vastaa kysyntäpäivää</li><li>Nykyinen toimitus, joka ei vastaa kysyntäpäivää, mutta joka on silti negatiivisten päivien sisällä</li><li>Luo uusi toimitus (suunniteltu tilaus)</li></ol> |
| **Kuluta käytettävissä olevaa varastoa** = *Kaikkien toimitusten jälkeen* | <ol><li>Nykyinen toimitus, joka vastaa kysyntäpäivää</li><li>Käytettävissä oleva</li><li>Nykyinen toimitus, joka ei vastaa kysyntäpäivää, mutta joka on silti negatiivisten päivien sisällä</li><li>Luo uusi toimitus (suunniteltu tilaus)</li></ol> | <ol><li>Nykyinen toimitus, joka vastaa kysyntäpäivää</li><li>Nykyinen toimitus, joka ei vastaa kysyntäpäivää, mutta joka on silti negatiivisten päivien sisällä</li><li>Käytettävissä oleva</li><li>Luo uusi toimitus (suunniteltu tilaus)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Kutakin myyntitilausta koskevan täyttämiskäytännön tarkistaminen ja määrittäminen

Täyttämiskäytännöt ohjaavat tilauksen kokonaishintaa tai määrää, joka on varattava fyysisesti ennen kuin voit vapauttaa myyntitilauksen varastoon. Voit määrittää yleisen oletustäyttämiskäytännön ja korvata sen sitten yksittäisille asiakkaille tarpeen mukaan. *Tilauksesta valmistukseen -tarjonnan automatisointi* -ominaisuus lisää mahdollisuuden tarkastaa, mikä oletuskäytäntö koskee mitäkin tilausta, ja määrittää tilauskohtaisen käytännön tarvittaessa.

- Jos haluat määrittää myyntitilauksille yleisen oletustäyttämiskäytännön, siirry kohtaan **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**. Määritä sitten **Varastonhallinta**-välilehden **Myyntitilauksen toteuttamiskäytäntö** -kentän arvoksi haluamasi käytännön nimi. 
- Jos haluat määrittää myyntitilauksille asiakaskohtaisen täyttämiskäytännön, siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**. Määritä sitten **Varastonhallinta**-välilehden **Toteuttamiskäytäntö**-kentän arvoksi haluamasi käytännön nimi.

Noudata seuraavia ohjeita tarkastaaksesi minkä tahansa tilauksen oletuskäytännön ja korvataksesi käytännön tilauskohtaisesti.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Avaa myyntitilaus, jota haluat tarkastella tai muokata.
1. Valitse **Otsikko**-näkymä.
1. Tarkastele ja muokkaa seuraavia kenttiä **Varastonhallinta**-pikavälilehdessä tarvittaessa:

    - **Tilauksen täyttämiskäytäntö** – Valitse valitulle tilaukselle käytettävä täyttämiskäytäntö. Oletuskäytäntö korvataan. Jos haluat käyttää **Täyttämisen oletuskäytäntö** -kentässä näytettyä täyttämiskäytäntöä, jätä tämä kenttä tyhjäksi.
    - **Täyttämisen oletuskäytäntö** – Tämä kenttää näyttää täyttämisen oletuskäytännön, joka on voimassa, jos **Tilauksen täyttämiskäytäntö** -kenttä on tyhjä. Kenttää ei voi muokata. Jos kenttä on tyhjä, asiakaskohtaista täyttämiskäytäntöä tai yleistä oletustäyttämiskäytäntöä ei ole määritetty.

    Jos **Tilauksen täyttämiskäytäntö**- ja **Täyttämisen oletuskäytäntö** -kentät ovat molemmat tyhjiä, mikään täyttämiskäytäntö ei ole voimassa. Voimassa voi kuitenkin olla muita rajoituksia, jotka saattavat edellyttää, että varaukset tai muut ehdot täyttyvät ennen kuin myyntitilaus voidaan vapauttaa.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>Toimitustavan ja -ehtojen määrittäminen yksittäisille ostotilausriveille

Kaikki ostostilaukset sisältävät **Toimitusehdot**- ja **Toimitustapa**-asetukset tilausotsikossa. *Tilauksesta valmistukseen -tarjonnan automatisointi* -ominaisuus lisää nämä asetukset jokaiselle tilausriville. Voit siis tarvittaessa määrittää korvaavat **Toimitusehdot**- ja/tai **Toimitustapa**-arvot mille tahansa riville tai kaikille riveille. Jos riveille ei ole määritetty korvaavaa arvoa, käytetään otsikon arvoa. Voit määrittää, tulisiko toisen tai molempien näiden kenttien muuttaminen tilausotsikossa päivittää myös kaikki rivit.

Noudata seuraavia ohjeita määrittääksesi, mitä rivien asetuksille tulisi tapahtua, jos käyttäjä muuttaa **Toimitusehdot**- ja/tai **Toimitustapa**-arvoa tilausotsikossa.

1. Siirry kohtaan **Hankkiminen ja hankinta \> Asetukset \> Hankkiminen ja hankinta -parametrit**.
1. Valitse **Yleinen**-välilehden **Oletusarvot ja parametrit** -pikavälilehdestä **Päivitä tilausrivit** -linkki.
1. Valitse **Päivitä tilausrivit** -valintaruudun **Päivitetään toimitusehtoja**- ja **Päivitä toimitustila** -kentille jokin seuraavista arvoista:

    - *Ei koskaan* – Älä koskaan päivitä tilausrivejä, kun asetuksia muutetaan tilausotsikossa.
    - *Aina* – Päivitä kaikki tilausrivit aina, kun asetuksia muutetaan tilausotsikossa.
    - *Kehote* – Jos käyttäjä muuttaa toista asetusta tai molempia asetuksia tilausotsikossa, avaa valintaikkuna, jossa kysytään, haluaako käyttäjä päivittää kaikki rivit siten, että ne vastaavat asetusten muutoksia.

Voit määrittää toimitustiedot ostotilauksen otsikossa noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Avaa ostotilaus, jota haluat muokata.
1. Valitse **Otsikko**-näkymä.
1. Määritä **Toimitus**-pikavälilehden **Toimitustapa**- ja **Toimitusehdot**-kentät tarpeidesi mukaan.
1. Riippuen **Hankintaparametrit**-sivun asetuksista, sinulta saatetaan kysyä, haluatko ottaa muutokset käyttöön kaikille tilausriveille.

Voit määrittää ostotilauksen riville korvaavia arvoja seuraavia ohjeita.

1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Avaa ostotilaus, jota haluat muokata.
1. Valitse **Rivit**-näkymä.
1. Valitse muokattava rivi **Ostotilausrivit**-pikavälilehdestä.
1. Määritä **Rivin erittely**-pikavälilehden **Toimitus**-välilehden **Toimitustapa**- ja **Toimitusehdot**-kentät tarpeidesi mukaan. Tyhjennä toinen kenttä tai molemmat kentät käyttääksesi otsikon vastaavia asetuksia.

Konsernien sisäisten tilausten kaikkien ostotilausrivien **Toimitustapa**- ja **Toimitusehdot**-kenttien arvot synkronoidaan ostotilauksen ja siihen liittyvän myyntitilauksen välillä.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Konsernin sisäisten tilausten ulkoisten nimiketunnusten ja kuvausten synkronoiminen

*Tilauksesta valmistukseen -tarjonnan automatisointi* -ominaisuus mahdollistaa konsernin sisäisten tilausten ostotilausrivien ulkoisten nimiketunnusten ja tekstikuvausten synkronoinnin konsernin sisäisten myyntitilausrivien kanssa riippumatta siitä, voiko ostotilauksen toimittaa suoraan. Ominaisuus mahdollistaa myös lopullisen ulkoisen asiakastilin määrittämisen konsernin sisäiselle ostotilaukselle. Järjestelmä noutaa tämän jälkeen ulkoiset nimiketunnukset ja tekstikuvaukset automaattisesti ulkoisesta asiakastietueesta konsernin sisäisen toimittajatietueen sijaan.

Jos haluat määrittää konsernin sisäinen toimittajan synkronoimaan ulkoiset nimiketunnukset ja nimikkeiden nimet konsernin sisäisten ostotilausten ja niihin liittyvien konsernin sisäisten myyntitilausten välillä, noudata seuraavia ohjeita.

1. Valitse **Hankinta \> Toimittajat \> Kaikki toimittajat**.
1. Valitse konsernin sisäinen toimittaja, jonka haluat määrittää.
1. Valitse toimintoruudun **Yleiset**-välilehden **Määritä**-ryhmästä **Konsernin sisäinen**.
1. Valitse **Konsernin sisäinen** -sivun **Ostotilauskäytännöt**-välilehden **Konsernin sisäinen ostotilaus -\> Konsernin sisäinen myyntitilaus** -osiosta **Ulkoinen nimikkeen tunnus ja nimikkeen nimi** -valintaruutu.

Jos haluat määrittää lopullisen ulkoisen asiakastilin konsernin sisäiselle ostotilaukselle, noudata näitä ohjeita. **Asiakastili**-kenttä koskee vain konsernin sisäisiä ostotilauksia. Käytä sitä määrittääksesi tilinumeron asiakkaalle, joka lopulta vastaanottaa tuotteet. Kun tämä kenttä on määritetty, ostotilausrivit saavat ulkoiset nimikekuvaukset ja -numerot määritetyltä asiakastililtä ostotilauksessa määritetyn konsernin sisäisen toimittajan sijaan. Jos muutat asiakastiliä myöhemmin, ulkoiset nimikekuvaukset ja -tunnukset päivitetään vastaamaan uuden tilin arvoja. Kunkin rivin ulkoiset nimikekuvaukset ja -tunnukset synkronoidaan myös vastaavaan konsernin sisäiseen myyntitilaukseen.

1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Avaa määritettävä ostotilaus tai luo uusi.
1. Valitse **Otsikko**-näkymä.
1. Määritä **Viite**-osion **Asiakastili**-kentän arvoksi asiaankuuluva ulkoinen asiakastili.

Jos haluat määrittää konsernin sisäisen tilauksen ostotilausrivin ulkoiset nimiketunnukset ja tekstikuvaukset, noudata seuraavia ohjeita. Määrittämäsi arvot synkronoidaan asiaan liittyvien konsernin sisäisten myyntitilausrivien kanssa riippumatta siitä, voidaanko ostotilaus toimittaa suoraan.

1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Avaa määritettävä ostotilaus tai luo uusi.
1. Valitse **Rivit**-näkymä.
1. Valitse muokattava rivi **Ostotilausrivit**-pikavälilehdestä.
1. Syötä **Rivin erittely** -pikavälilehden **Yleiset**-välilehden **Tilausrivi**-osion **Teksti**-kenttään ulkoinen kuvaus valitulla tilausrivillä määritetylle nimikkeelle. Tämä arvo synkronoidaan asiaan liittyvän konsernin sisäisen myyntitilausrivin kanssa.
1. Syötä **Viite**-osion **Ulkoinen**-kenttään ulkoinen nimiketunnus valitulla tilausrivillä määritetylle nimikkeelle. Tämä arvo synkronoidaan asiaan liittyvän konsernin sisäisen myyntitilausrivin kanssa.

Lisätietoja on kohdassa [Konsernin sisäisen myyntitilauksen luominen ja laskuttaminen ulkoiselle asiakkaalle](../sales-marketing/intercompany-sales-order-for-external-customer.md).
