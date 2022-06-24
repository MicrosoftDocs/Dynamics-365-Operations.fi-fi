---
title: Varaston kustannuslaskenta – UKK
description: Tässä artikkelissa on usein kysyttyjä kysymyksiä ja vastauksia Microsoft Dynamics 365 Supply Chain Managementin kustannuslaskennasta.
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 467839b1d0ca6788a92ae60d46686374d0a58046
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850841"
---
# <a name="inventory-costing-faq"></a>Varaston kustannuslaskenta – UKK

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on usein kysyttyjä kysymyksiä ja vastauksia Microsoft Dynamics 365 Supply Chain Managementin kustannuslaskennasta.

## <a name="inventory-close-adjustments-and-recalculation"></a>Varaston sulkeminen, oikaisut ja uudelleenlaskenta

### <a name="is-the-inventory-close-required"></a>Onko varaston sulkeminen tarpeen?

Jos aiot käyttää varaston arkistointitoimintoa, varaston sulkeminen on pakollinen. Jos et aio käyttää varaston arkistointitoimintoa, varaston sulkeminen on edelleen suositeltavaa riippumatta käytetyistä kustannuslaskelmamalleista.

### <a name="how-often-should-the-inventory-close-be-run"></a>Miten usein varaston sulkeminen suoritetaan?

Varaston sulkeminen on suoritettava kirjanpitojaksoa kohden vähintään kerran. Jos kirjanpidon arvoksi on määritetty esimerkiksi kalenterikuukausi, suorita varaston sulkeminen kerran kuukaudessa.

### <a name="is-the-inventory-recalculation-required"></a>Onko varaston uudelleenlaskenta tarpeen?

Ei, varaston uudelleenlaskenta ei ole pakollinen. Jos käytät kausittaista kustannuslaskentamallia, kuten FIFO-mallia, LIFO-mallia tai painotettua keskiarvoa, harkitse tarkkaan, suoritatko varaston uudelleenlaskennan. Se voi tarjota tarkemman kustannuslaskennan valituissa heuristisissa malleissa.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Miten usein varaston uudelleenlaskenta suoritetaan?

Jos aiot suorittaa varaston uudelleenlaskennan, on suositeltavaa suorittaa se päivittäin eräprosessina. Jos organisaatiosi ei tarvitse kausittaisten kustannuslaskelmamallien varastoarvojen toistuvaa raportointia, varastolaskelman ajaminen kannattaa suorittaa mahdollisesti harvemmin.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Milloin pitäisi käyttää käytettävissä olevan varaston oikaisua Sulkeminen ja oikaisut -sivulla?

Käytettävissä oleva varaston oikaisu voidaan suorittaa vain, kun varaston sulkeminen on valmis. Se suoritetaan yleensä viimeisen sulkemispäivän jälkeen. Käytettävissä olevan varaston oikaisu voi oikaista vain varaston, jos sitä on vielä käytettävissä oikaisun suorituksen päivämääränä.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Milloin pitäisi käyttää varastotapahtuman oikaisua Sulkeminen ja oikaisut -sivulla?

Varastotapahtuman oikaisua kannattaa käyttää ennen varaston sulkemista. Sitä käytetään yleensä virheellisen vastaanoton korjaamiseen. Varastotapahtuman oikaisua ei voi kirjata varaston sulkemisen ja tapahtuman selvityksen jälkeen.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Käsitelläänkö ostotilausten palautuksia samoin kuin muita varasto-ottoja varaston sulkemisen aikana?

Kyllä. Ostotilauksen vastaanotto on varasto-otto, joka täsmäytetään nimikkeelle valittavassa heuristisessa mallissa vastaanoton kanssa. Jos käytät kausittaista kustannuslaskelmamallia, voit ohittaa heuristisen kustannuksen merkinnän avulla.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Mitä myyntitilauksen palautuksille tapahtuu, kun varasto suljetaan?

Kun suoritat varaston sulkemisen, myyntitilauksen palautusta käsitellään vastaanottona varastoon. Varasto-otot täsmäytetään varastoa vasten nimikkeelle valittavan heuristisen mallin perusteella.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Mitä kustannushintaa käytetään myyntitilauksen palautuksessa?

Kun luot myyntitilaukseen liittyvän palautuksen, **Yksikköhinta**-kentän arvo kopioidaan alkuperäisestä myyntitilauksesta ja palautuksen **Palautuskustannushinta**-kentän arvoksi tulee oikaistu kustannushinta palautettavan myyntitilausrivin alkuperäisestä varastotapahtumasta. Jos liittyvän varastotapahtuman **Arvo avoin** -asetuksen arvona on *Kyllä*, varaston sulkeminen voi päivittää alkuperäisen myyntitilauksen varasto-ottokustannuksen. **Palautuksen kustannushinta** -kenttää ei päivitetä tässä skenaariossa. Kun kirjaat palautustilauksen pakkausluettelon, järjestelmä kuitenkin tarkistaa kustannushinnan ja käyttää palautuksen varastotapahtuman päivitettyä kustannusta.

Myyntitilaukseen liittyvän standardikustannusnimikkeen palautuksessa järjestelmä käyttää standardikustannusta alkuperäisen myyntitilauksen ajasta alkaen, vaikka nimikkeen uusi standardikustannus olisi aktiivinen.

Kun luot palautuksen, joka ei liity myyntitilaukseen, **Palautuskustannushinta**-kentän arvoksi tulee sen nimikkeen aktiivinen hinta toimipaikassa, jota varten olet luomassa palautustilausta. Jos nimikkeen kustannuslaskelmaversiossa ei ole aktiivista kustannushintaa, arvo on 0 (nolla). Jos jätät arvoksi 0 (nolla), saat varoituksen, jossa todetaan, että palautuserän tunnusta tai palautuksen kustannushintaa ei ole määritetty.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Mikä on varaston sulkemisen odotettu suoritustaso?

Monet tekijät voivat vaikuttaa varaston sulkemisen suorituskykyyn. Tekijät sisältävät nimikkeiden kokonaismäärän, kauden tapahtumien kokonaismäärän, käytettävät varastomallit sekä varaston ja varastonhallinnan parametreissa konfiguroitujen eräavustajien määrän. Voit odottaa, että sulkeminen kestää niin vähän kuin vain muutama minuutti tai jopa useita tunteja. Tarkkoja ohjeita ei ole siitä, kuinka kauan sulkemisaika tulisi kestää. Määritä ei-toiminnalliset liiketoimintavaatimukset varaston sulkemisen suorituskyvylle ja toimi kumppanin kanssa, jotta voit määrittää varaston sulkemisprosessin suoritusaikataulun. Jos varaston sulkemisprosessin suorituskyky on odottamattoman heikko, avaa tukilippu.

## <a name="costing-sheet-and-indirect-costs"></a>Kustannuslaskentalomake ja epäsuorat kustannukset

### <a name="which-costing-models-support-the-costing-sheet"></a>Mitkä kustannuslaskentamallit tukevat kustannuslaskentalomaketta?

Vaikka kustannuslaskentalomaketta käytetään yleensä organisaatioissa, jotka käyttävät vakiokustannuslaskentaa, voit käyttää sitä minkä tahansa Supply Chain Managementissa käytettävissä olevan kustannuslaskelmamallin kanssa.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Voiko eri organisaation osille luoda useita kustannuslaskentalomakkeita?

Ei Yhtä yritystä kohden voi olla vain yksi kustannuslaskentalomake.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Voiko kullekin toimipaikalle määrittää erilaisia kustannuslaskentalomakkeita?

Ei, eri toimipaikoille ei voi määrittää erilaisia kustannuslaskentalomakkeita. Yhtä yritystä kohden voi luoda vain yhden kustannuslaskentalomakkeen. Voit kuitenkin konfiguroida solmujen kokonaismäärän, kustannusryhmät tai epäsuorien kustannusten solmuja toimipaikkaa kohden. Tämä konfigurointi on manuaalinen prosessi, ja kustannuslaskentalomakkeen hierarkia ja nimikemääritykset on säilytettävä, kun organisaation tai toiminnan muutoksia tapahtuu. Jos yksittäinen nimike tuotetaan tai ostetaan useammassa kuin yhdessä toimipaikassa, ei ole mekanismia, jonka avulla nimikettä voidaan käsitellä eri tavalla kunkin toimipaikan kustannuslaskentalomakkeessa. Huomaa myös, että kaikissa epäsuorien kustannusten koodeissa on kustannuslaskelmaversiossa määritetty hinta tai lisämaksu. Määritettävät kustannukset ovat aina toimipaikkakohtaisia.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Voiko kustannuslaskentalomakkeen versiot aktivoida ja niiden aktivointi poistaa?

Vaikka kustannuslaskentalomakkeelle ei säilytetä yksityiskohtaista versiohistoriaa, voit tehdä kustannuslaskentalomakkeeseen muutoksia ja tallentaa ja vahvistaa sen, kun olet valmis. Ei ole mekanismia, jonka avulla voit palata kustannuslaskentalomakkeen vanhaan versioon tai tarkastella kustannuslaskentalomakkeeseen tehtyjä muutoksia. Jos aloitat muutokset etkä halua, että muutokset tulevat voimaan, voit sulkea sivun tallentamatta ja validoimatta muutoksia. Näyttöön tule kehote hylätä muutokset.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Voiko kullekin nimikkeelle luoda epäsuoria kustannuksia?

Kustannuslaskentalomakkeessa voit luoda epäsuoria kustannuskoodeja, joissa **Solmutyyppi**-kentän arvoksi on määritetty *Lisämaksu*, *Hinta* tai *Tulostusyksikköperusteinen*. Sen jälkeen voit määrittää hinnan tai lisämaksun niin, että se on nimiketunnuskohtainen. Lisää rivi ruudukkoon **Hinta**- tai **Lisämaksu**-pikavälilehdessä. Määritä  *Taulu*- ja **Suhde**-kenttään **Voimassa kohteelle** -kenttä tiettyyn nimiketunnukseen.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Voinko luoda epäsuoran kustannuksen, joka ei liity tiettyyn nimikkeeseen?

Kyllä. Voit luoda epäsuoran kustannuksen koodin, jos **Solmutyyppi**-kentän arvona on *Tulostusyksikköperusteinen*. **Alatyyppi**-kentän arvoksi voidaan määrittää tuotettavan nimikkeen määrä, paino tai tilavuus valitsemalla *Määrä*, *Paino* tai *Tilavuus*. **Hinta**-pikavälilehdessä määrittämääsi hintaa sovelletaan valitsemasi alatyyppiin. Voit esimerkiksi määrittää **Alatyyppi**-kentän arvoksi *Määrä* ja **Hinta**-kentän arvoksi *1,00 USD*. Luo sitten tuotanto- tai erätilaus määrälle 10. Tällöin valmiille tuotteelle lisättävä epäsuora kustannus on 10,00 USD.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Voiko kustannuslaskentalomakkeen avulla jakaa tuotantokustannukset tuntien ja materiaalien mukaan?

Kyllä. Kustannuslaskentalomakkeeseen voidaan luoda **Yhteensä**-solmuja, jotta kustannukset erotetaan valitsemallasi ryhmittelyllä. Voit esimerkiksi luoda yhden **Yhteensä**-solmun, jonka nimi on *Tunnit*, ja toisen, jonka nimi on *Materiaalit*. Lisää tunteihin liittyvät kaikki koodiryhmät **Tunnit**-solmuun. Lisää materiaaleihin liittyvät kaikki kustannusryhmät **Materiaalit**-solmuun.

## <a name="dimension-groups"></a>Dimensioryhmät

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Voinko hallita kustannuksia erä- tai sarjanumerotasolla?

Kyllä, jos käytät kausittaista kustannuslaskelmamallia, kuten FIFO-, LIFO-, LIFO-päivämäärä-mallia, painotettua keskiarvoa tai painotetun keskiarvon päivämäärää, voit ottaa **Kirjanpitovarasto**-vaihtoehdon käyttöön seurantadimensioryhmän **Erä**- tai **Sarjanumero**-dimensiolle kustannusten seuraamista varten yksityiskohtaisella tasolla.

### <a name="can-i-manage-costs-at-the-location-level"></a>Voinko hallita kustannuksia sijainnin tasolla?

Ei, et voi ottaa **Kirjanpitovarasto**-asetusta käyttöön **Sijainti**-dimensiolle varastodimensioryhmässä. Jos organisaation on jäljitettävä kustannuksia tarkemmin, mieti, voidaanko luoda virtuaalivarastot, ja valitse sitten varastodimensioryhmän **Varasto**-dimensiolle **Kirjanpitovarasto**-vaihtoehto.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Pitäisikö varastonhallintaprosessiasetus ottaa käyttöön varastodimensioryhmälle?

Jos haluat ehkä käyttää varastonhallinnan lisätoimintoja tulevaisuudessa, ota käyttöön **Käytä varastonhallintaprosesseja** -vaihtoehto. Kun olet tallentanut varastodimensioryhmän, et voi enää muuttaa **Käytä varastonhallintaprosesseja** -vaihtoehdon asetusta. Jos päätät myöhemmin käyttää varastonhallintaprosesseja, sinun on luotava uusi varasto, jossa asetus on käytössä. Ei ole automaattista prosessia, jota voi käyttää koko varaston siirtoon varastosta toiseen tai siihen liittyvien konfiguraatioiden kopioimiseen uuteen varastoon.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-advanced-warehousing"></a>Voiko varastonhallinnan prosessit ottaa käyttöön varastodimensioryhmässä, vaikka en olisikaan aikomassa käyttää edistynyttä varastointia?

Kyllä, vaikka et aio käyttää edistyneen varastonhallinnan ominaisuuksia, voit ottaa **Varastonhallintaprosessien käyttö** -vaihtoehdon käyttöön varastodimensioryhmälle. Jotta voit luoda ja käsitellä tapahtumia, sinun on suoritettava vähimmäiskonfiguraatio, kuten varaushierarkiat ja yksikköjärjestysryhmät. Edistyneen varastoinnin asetukset ohitetaan kuitenkin yleensä, kun keräysluetteloita, pakkausluetteloita ja tuotteiden vastaanottoja käsitellään manuaalisesti (esimerkiksi myyntitilaus- ja ostotilaussivuilla).

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Milloin varastotilanne on otettava käyttöön varastolle tai seurantadimensioryhmälle?

**Varastotilanne**-vaihtoehto tulisi ottaa käyttöön varastolle ja seurantadimensioryhmille, kun tähän dimensioon perustuvat tarkat varastotietueet on hyvä säilyttää. Tavallisesti kaikkia aktiivisia dimensioita seurataan fyysisesti. Valittu dimensio seuraa siis varaston vastaanottoa, varasto-ottoa tai siirtoa. Jos dimensio ei ole pakollinen (esimerkiksi rekisterikilpi), voit ottaa **Tyhjä vastaanotto sallitaan**- ja **Tyhjä varasto-otto sallitaan** -asetukset käyttöön, jotta käyttäjät voivat vastaanottaa, ottaa tai siirtää varastoa silloinkin, kun dimensiota ei ole määritetty.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Milloin kirjanpitovarasto on otettava käyttöön varastolle tai seurantadimensioryhmälle?

**Kirjanpitovarasto**-vaihtoehto tulisi ottaa käyttöön varastolle ja seurantadimensioryhmille, kun tähän dimensioon perustuvat tarkat kirjanpitotietueet on hyvä säilyttää. **Toimipaikka**-dimensioita seurataan aina taloudellisesti, kun taas muut dimensiot ovat valinnaisia taloushallinnon seurantaa varten. Jos käytät kausittaista kustannuslaskentamallia, kuten FIFO, LIFO tai painotettua keskiarvoa, dimension **Kirjanpitovarasto**-vaihtoehdon ottaminen käyttöön osoittaa, että tilitys tehdään vain, jos vastaanotolla ja varasto-otolla on samat dimensioarvot. Jos esimerkiksi otat käyttöön **Kirjanpitovarasto**-vaihtoehdon **Varasto**-dimensiolle, jokaisessa varastossa on eri kustannukset, eikä eri varastojen vastaanottoja ja varasto-ottoja voida selvittää.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Voiko tuotteeseen, varastoon tai seurantadimensioryhmään tehdä muutoksia tapahtumien jälkeen?

Kun olet luonut nimikemalliryhmän, voit muuttaa **Kattavuussuunnitelma dimension mukaan**-, **Ostohinnoille**- ja **Myyntihinnoille**-kenttien asetusta, jos nimikemalliryhmän dimension **Aktiivinen**-valintaruutu on valittuna. Muita muutoksia ei sallita. Et esimerkiksi voi ottaa käyttöön tai poistaa käytöstä asetuksia **Aktiivinen**, **Tyhjä varasto-otto sallitaan**, **Tyhjä vastaanotto sallitaan**, **Varastotilanne** ja **Kirjanpitovarasto**.

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Voiko vapautetun tuotteen tuotetta, varastointia tai seurantadimensioryhmää muuttaa?

Jos tuotteen käytettävissä oleva varasto on 0 (nolla) ja kaikkien varastotapahtumien **Arvo avoin** -asetukseksi on asetettu *Ei*, voit muuttaa varastoa ja seurantadimensioryhmiä vapautetun tuotantosivun osalta. Tuotedimensioryhmää ei voi muuttaa, kun tietue on luotu.

## <a name="item-model-groups"></a>Nimikemalliryhmät

### <a name="when-should-i-enable-the-stocked-product-option"></a>Milloin Varastoitu tuote -vaihtoehto tulee ottaa käyttöön?

**Varastoitu tuote** -asetus kannattaa ottaa käyttöön nimikkeelle, jota seurataan varastossa. Kun tämä vaihtoehto on käytössä, säilytetään yksityiskohtaiset varastotapahtumat, joilla seurataan nimikkeen vastaanottoa ja ottoa. Tämä vaihtoehto on yleensä käytössä esimerkiksi varastossa säilytettävälle aineellisille nimikkeille. Ota tämä vaihtoehto käyttöön myös, jos aiot lisätä ei-aineellisen nimikkeen, kuten huoltonimikkeen tuoterakenteisiin tai kaavoihin. Jos **Varastoitu tuote** -asetusta ei valita, varaston alareskontran varastotapahtumia ei seurata ja nimikkeiden kustannukset kirjataan yleensä kirjanpitoon. Tätä vaihtoehtoa käytetään usein esimerkiksi tuotantotilan tarvikkeille tai huolloille, jotka eivät sisälly tuoterakenteisiin tai kaavoihin.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Milloin Fyysisen varaston kirjaaminen -asetus on otettava käyttöön?

**Fyysisen varaston kirjaaminen** -valinta on tavallisesti käytössä, kun **Varastoitu tuote** -vaihtoehto on käytössä. Kun tämä vaihtoehto otetaan käyttöön, järjestelmä seuraa varastotapahtuman nimikkeen fyysistä päivitystä. Tätä valintaa käytetään yhdessä ostoreskontran, myyntireskontran ja tuotannonhallinnan parametrien kanssa, jotka määrittävät, että fyysinen päivitys luo tositteen. Tämä vaihtoehto on yleensä käytettävissä, kun haluat, että kirjanpito päivitetään aina, kun varasto päivitetään fyysisesti. Jos taloushallinnon tietuejärjestelmä ei ole Supply Chain Management, tämä vaihtoehto kannattaa ehkä poistaa käytöstä.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Milloin Kirjanpitovaraston kirjaaminen -asetus on otettava käyttöön?

**Kirjanpitovaraston kirjaaminen** -valinta on tavallisesti käytössä, kun **Varastoitu tuote** -vaihtoehto on käytössä. Tätä valintaa käytetään yhdessä ostoreskontran, myyntireskontran ja tuotannonhallinnan parametrien kanssa, jotka määrittävät, että kirjanpitopäivitys luo tositteen. Tämä vaihtoehto otetaan yleensä käyttöön, kun haluat, että kirjanpito päivitetään aina, kun varasto päivitetään kirjanpitoon (esimerkiksi laskutettaessa myynti- ja ostotilauksia tai lopetettaessa tuotantotilaus). Jos taloushallinnon tietuejärjestelmä ei ole Supply Chain Management, tämä vaihtoehto kannattaa ehkä poistaa käytöstä.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Milloin Kirjaa lykätyn tuoton tilille myynnin toimituksessa -vaihtoehto tulisi ottaa käyttöön?

**Kirjaa lykätyn tuoton tilille myynnin toimituksessa** -vaihtoehdon avulla voit määrittää, tuloutetaanko tuotto kirjanpitoon, kun myyntitilauksen pakkausluettelo kirjataan. Tätä vaihtoehtoa käytetään yleensä, kun pakkausluettelon ja myyntitilauksen laskun välillä on pitkä viive tai kun kauden kaikkia myyntitilauksia ei voi laskuttaa. Tavallisesti tämä vaihtoehto poistetaan käytöstä, jos myyntitilauslaskut kirjataan heti pakkausluettelon kirjaamisen jälkeen. Näin vältetään ylimääräisiä kirjanpitokirjauksia, jotka palautetaan heti myyntitilausta laskutettaessa.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Milloin Jaksota ostovelka tuotteen vastaanotossa -vaihtoehto pitäisi ottaa käyttöön tuotteen vastaanottoa varten?

Useimmissa organisaatioissa haluat ottaa **Jaksota ostovelka tuotteen vastaanotossa** -vaihtoehdon käyttöön kaikille nimikemalliryhmille riippumatta siitä, onko tuote varastoitu vai ei-varastoitu. Tämän vaihtoehdon avulla kirjataan jaksotus kirjanpitoon tuotteen vastaanottohinnan perusteella. Koska ostotilauksen tuotteen vastaanoton kirjaamisen ja laskun kirjaamisen välillä on yleensä viive, useimpien organisaatioiden täytyy tunnistaa taseessa velka paikallisen lainsäädännön, kuten GAAP (Generally Accepted Accounting Practices) -käytäntöjen mukaisesti. Jos taloushallinnon tietuejärjestelmä ei ole Supply Chain Management, tämä vaihtoehto kannattaa ehkä poistaa käytöstä. Jos organisaatiossa käytetään ostotilauksissa hankintaluokkia, voit hallita jaksotusvaatimusta ottamalla **Ostokäytännöt**-sivulla käyttöön **Jaksota ostokulut vastaanoton yhteydessä** -vaihtoehdon.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Miten estän käyttäjää kirjaamasta ostotilauksen tuotteen vastaanottoa, jos vastaanoton rekisteröintiä ei ole vielä kirjattu?

Voit estää käyttäjää kirjaamasta ostotilauksen tuotteen vastaanottoa, jos ostotilauksen rekisteröintiä ei ole vielä tehty, ottamalla **Rekisteröintivaatimukset**-asetuksen käyttöön nimikemalliryhmälle. Tätä vaihtoehtoa käytetään yleensä organisaatioissa, joissa vastaanottoprosessissa on kaksi vaihetta, tai tilanteissa, joissa erä- tai sarjanumero on rekisteröitävä esimerkiksi vastaanotettavien nimikkeiden yhteydessä. **Rekisteröintivaatimus**-vaihtoehto koskee *kaikkia* nimikkeen varastovastaanottoja, ei vain ostotilauksia. Sitä käytetään esimerkiksi varastokirjauskansiossa, jonka määrä on positiivinen, ja tuotantotilauksen valmiiksi ilmoitettujen kirjauskansiona.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Miten estän käyttäjää kirjaamasta ostotilauksen laskua, jos tuotteen vastaanottoa ei ole vielä kirjattu?

Voit estää käyttäjää kirjaamasta ostotilauksen tuotteen laskua, jos ostotilauksen tuotteen vastaanottoa ei ole vielä tehty, ottamalla **Vastaanoton vaatimukset** -asetuksen käyttöön nimikemalliryhmälle. Tätä vaihtoehtoa käytetään yleensä organisaatioissa, joissa vastaanotot on kirjattava kirjanpitoon jaksotuksia varten. **Vastaanoton vaatimus** -vaihtoehto koskee *kaikkia* nimikkeen varastovastaanottoja, ei vain ostotilauksia. Sitä käytetään esimerkiksi varastokirjauskansiossa, jonka määrä on positiivinen, ja tuotantotilauksen valmiiksi ilmoitettujen kirjauskansiona. Jos organisaatiossa käytetään ostotilauksissa hankintaluokkia, voit hallita vastaanoton vaatimusta ottamalla **Ostokäytännöt**-sivulla käyttöön **Vastaanoton vaatimukset** -vaihtoehdon.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Miten estän käyttäjää kirjaamasta myyntitilauksen pakkausluetteloa, jos myyntitilauksen keräysluetteloa ei ole vielä kirjattu?

Voit estää käyttäjää kirjaamasta myyntitilauksen pakkausluetteloa tai laskua, jos myyntitilauksen keräysluetteloa ei ole vielä tehty, ottamalla **Keräilyn vaatimukset** -asetuksen käyttöön nimikemalliryhmälle. Tätä vaihtoehtoa käytetään yleensä organisaatioissa, jotka suorittavat fyysisen keräilyprosessin varastossa (esimerkiksi keräystä varten käyttämällä varaston mobiililaitetta). **Keräilyn vaatimus** -vaihtoehto koskee *kaikkia* nimikkeen varasto-ottoja, ei vain myyntitilauksia. Sitä käytetään esimerkiksi varastokirjauskansiossa, jonka määrä on negatiivinen, ja tuotantotilauksen keräilyluettelon kirjauskansiossa.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Miten estän käyttäjää kirjaamasta myyntitilauksen laskua, jos myyntitilauksen pakkausluetteloa ei ole vielä kirjattu?

Voit estää käyttäjää kirjaamasta myyntitilauksen laskua, jos myyntitilauksen pakkausluetteloa ei ole vielä tehty, ottamalla **Vähennyksen vaatimukset** -asetuksen käyttöön nimikemalliryhmälle. Tätä vaihtoehtoa käytetään yleensä organisaatioissa, jotka suorittavat fyysisen pakkausprosessin varastossa (esimerkiksi käyttämällä Warehouse Management -mobiilisovellusta pakkaukseen tai luomalla asiakirjan, joka sisällytetään toimitettuihin nimikkeisiin). **Vähennyksen vaatimus** -vaihtoehto koskee *kaikkia* nimikkeen varasto-ottoja, ei vain myyntitilauksia. Sitä käytetään esimerkiksi varastokirjauskansiossa, jonka määrä on negatiivinen, ja tuotantotilauksen keräilyluettelon kirjauskansiossa.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Voinko estää rekisteröityjen nimikkeiden myymisen?

Kun nimike rekisteröidään varastoon Supply Chain Managementissa, määrä on fyysisesti käytettävissä järjestelmässä varasto-ottoa varten. Jos nimikkeitä, jotka on rekisteröity mutta joita ei ole vielä vastaanotettu, *ei* tule käyttää myynti- tai tuotantotilauksille, kannattaa käyttää esimerkiksi varaston tilaa, varaston estoa, laatutilauksia, karanteenitilauksia tai varaustoimintoja liiketoimintaprosessin hallinnassa.

## <a name="production-costing"></a>Tuotannon kustannuslaskenta

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Voiko käyttää yhtä kustannuslaskentamallia raaka-aineille ja eri kustannuslaskentamallia valmiille tavaroille?

Kyllä, voit käyttää kullekin nimikkeelle erilaisia kustannuslaskentamalleja. Valmistajat usein käyttävät kausittaista kustannuslaskentamallia raaka-aineille sekä puolivalmiiden ja valmiiden tuotteiden standardikustannuksia.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Kuinka voin vähentää yleiskustannukset konekustannuksista?

Voit poistaa yleiskustannukset konekustannuksista luomalla kullekin koneelle resursseja ja resurssiryhmiä liiketoimintavaatimusten mukaan. Kustannusluokkiin voi liittää kunkin resurssin tai resurssiryhmän ohjaamaan koneen kustannuksia. Kukin kustannusluokka voidaan linkittää kustannusryhmään, ja kutakin kustannusryhmää voidaan käyttää epäsuorien kustannusten laskennan perustana kustannuslaskentalomakkeessa.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Miten tunnistan kustannuslaskentalomakkeessa energiankulutukseen (esimerkiksi vesi-, sähkö- tai vesikulutukseen) liittyvät kustannukset?

Voit tunnistaa energiankulutuksen kustannukset kahdella eri tavalla:

- Luo rivi tuoterakenteeseen tai kaavaan. Yleensä tämä rivi luodaan huoltonimikkeenä ja voit määrittää mittayksikön, jota käytetään suhteessa tuotettavaan määrään. Näin käyttäjä voi kuluttaa tuotantoprosessin aikana eri määrän. Nimikkeet voi kuluttaa automaattisesti **Materiaaliottoperuste**-kentässä valitsemallasi arvolla.
- Luo kustannuslaskentalomakkeeseen epäsuora kustannus. Yleensä tätä menetelmää käytetään, kun haluat kohdistaa koko tuotantoprosessin energiankulutuksen kokonaiskustannukset. Voit käyttää kustannusryhmää ja kustannusperustaa esimerkiksi kulutuksen skaalaamiseen reitin materiaalien tai työn perusteella.

Valitse paras vaihtoehto raportointi-, täsmäytys- ja toiminnallisten vaatimusten perusteella.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Voiko resurssin tiedot siepata tuoterakenteessa tai kaavassa?

Resurssin tiedot voi siepata vain reititystoiminnossa. Vaikka voit luoda huoltonimikkeen, joka edustaa resurssia, ja määrittää kustannuksen kasvattaaksesi lopputuotteen kustannuslaskentaa, tätä lähestymistapaa ei yleensä suositella. Sen sijaan on suositeltavaa luoda yksinkertainen reititys, jolla on yksi rivi resurssikustannusten seuraamista varten, ja konfiguroida toiminto niin, että se kulutetaan automaattisesti tuotantotilauksen alussa tai lopussa.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Voinko tarkastella laskelman tietoja, jos kustannus syötetään manuaalisesti?

Ei Jos määrität hinnan manuaalisesti **Nimikkeen hinta** -sivulla,**Näytä laskelman tiedot**- ja **Raportin laskennan tiedot** -painikkeet eivät ole käytettävissä. Jos valitset manuaalisesti syötettävälle kustannushinnalle **Kustannusten koonti kustannusryhmien mukaan** -painikkeen, tässä näkyy yhteenvetorivi ja kaikki kustannukset kootaan valmiiseen tavaranimikkeeseen.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Laskeeko järjestelmä tuotantotilauksen varianssit, kun määritän kustannukset manuaalisesti?

Kyllä, järjestelmä laskee varianssit, kun määrität vakiokustannuksen manuaalisesti. Jos kuitenkin syötät vakiokustannuksen manuaalisesti sen sijaan, että laskisit sen, kaikki tuotantotilauksen materiaali-, reititys- ja epäsuorat kustannuskulutukset käsitellään korvausvarianssina. Jos on lisävariansseja, kuten ylimääräisten materiaalien tai työn kulutus, ne kirjataan myös varianssina tuotannon tuoterakenteesta. Siksi on suositeltavaa suorittaa laskelma aina nimikkeille, joissa on tuoterakenne, reititys tai epäsuorat kustannukset.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Miten varianssit voidaan siirtää osatuotantotilauksesta ja päätuotantotilaukseen?

Kun käytät kausittaista kustannuslaskentamallia, kuten FIFO, LIFO tai painotettua keskiarvoa, osatuotannon kustannukset tunnistetaan nimikkeille valitussa heuristisessa mallissa. Jos tarvitset todellista kustannuslaskelmaa, kannattaa merkintäperiaatteen avulla määrittää, mikä osatuotanto on määritetty päätuotantotilausta varten. Vaihtoehtoisesti kannattaa käyttää esimerkiksi seurantadimensioryhmän **Erä**- tai **Sarjanumero**-dimension **Kirjanpitovarasto**-asetusta.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Miten materiaaliottoperiaate vaikuttaa kulutukseen?

Tuoterakenteen, kaavan tai reititysrivin materiaaliottoperiaate ohjaa nimikkeen tai työn kulutukseen käytettävää ajoitusta ja menetelmää. Jos valitset *Aloita*, nimike tai työ kulutetaan automaattisesti, kun tuotantotilaus aloitetaan. Jos valitset *Lopeta*, nimike tai työ kulutetaan automaattisesti, kun tuotantotilaus ilmoitetaan valmiiksi. Jos valitset *Manuaalinen*-vaihtoehdon, käyttäjän on poimittava materiaalit manuaalisesti tai kirjattava aika työhön tai reitityskorttikirjauskansioon. Tuoterakenteissa ja kaavoissa on myös *Käytettävissä sijainnissa* -vaihtoehto. Jos valitset tämän vaihtoehdon, nimikkeet kulutetaan automaattisesti, kun ne on siirretty tuotantotilan sijaintiin.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Miten kustannuslaskelmat suoritetaan, jos minulla on monitasoiset tuoterakenteet tai kaavat?

On suositeltavaa aloittaa tuoterakenteiden tai reseptien alimmalla tasolla laskentaa varten. Voit helpottaa suodatusta kustannuslaskelmien joukkosuorituksessa ja erotella tuotteet laskentaryhmien avulla. On myös suositeltavaa suorittaa kausittainen *Laske tuoterakenteen tasot uudelleen* -työ, ennen kuin aloitat kustannuslaskennan joukkosuoritukset. Kunkin organisaation tulisi ottaa huomioon tuotteiden yhdistelmä ja määrittää strategia, joka vastaa tuotteen ja tuoterakenteen tai kaavarakenteiden tarpeita.

## <a name="transfer-order-costing"></a>Siirtotilauksen kustannuslaskenta

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Onko mahdollista kohdistaa rahti siirtotilauksen kustannukseen?

Voit lisätä kustannuksia lisäämällä siirtotilaukseen kuluja. Kulukoodi määrittää lisättävän kulun veloituksen ja hyvityksen. Kulukoodit on luotava ensin **Varastonhallinta**-moduulissa. Voit lisätä siirtotilauksen kulut valitsemalla **Kulut** siirtotilausriviltä, johon haluat lisätä kulut.

## <a name="variances"></a>Varianssit

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Voiko varianssit käsitellä eri tavoin toimipaikan tai varaston perusteella?

Varianssitilejä ei voi konfiguroida toimipaikan mukaan. Kun käytät vapautetun tuotteen vakiokustannuslaskentaa, voit valita **Kirjaus**-sivulla päätilin, jota käytetään standardikustannusten varianssin kirjauksia varten. Voit määrittää tilit yhdelle nimikkeelle, nimikeryhmälle tai kaikille nimikkeille. Voit myös konfiguroida yhden kustannusryhmän, kustannusryhmien ryhmän tai kaikki kustannusryhmät.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Voinko erottaa varianssit, jotka ovat valuutan vaihtokurssien tulos, muun tyyppisistä variansseista?

Jos varianssi on tuloksena ostotilauksen hinnan ja nimikkeen standardikustannusten välisen valuuttakurssierosta, vaihtokurssieroa ei voi erottaa muista variansseista.

## <a name="reporting"></a>Raportointi

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Kuinka monta varastoarvoraporttikonfiguraatiota voidaan luoda ja käyttää?

Varaston arvoraportin konfiguraatioiden määrää ei ole rajoitettu. Arvioi erityiset raportointivaatimuksesi ja luo niiden konfiguraatioiden määrä, jotka tarvitaan näiden vaatimusten täyttämiseen. Raportin tai raportin varastointivaihtoehdon suorittamiseen tarvitaan vähintään yksi varastoarvoraportin konfiguraatio.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Voiko varaston arvoraportin avulla analysoida nimikkeen kustannuksia kussakin varastossa?

Kyllä. Voit ottaa varastoarvoraportin konfiguroinnissa käyttöön kullekin **Varasto**-dimensiolle **Näytä**- tai **Summa**-vaihtoehdon. Raportti näyttää kuitenkin vain niiden dimensioiden arvot, joissa **Kirjanpitovarasto**-asetus on otettu käyttöön varastodimensioryhmälle. Muissa dimensioissa näkyy vain tyhjiä sarakkeita. Lisätietoja on kohdassa [Varaston arvoraportin esimerkkejä ja logiikka](inventory-value-report-examples.md).

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Miten varastomäärää voi tarkastella tietystä päivämäärästä alkaen, kun käytössä on painotettu keskiarvo?

Voit käyttää **Varaston erääntyminen** -raporttia, joka sisältää **Keskimääräinen yksikkökustannus** -sarakkeen, jossa varaston arvo näkyy tiettynä päivämääränä. Lisätietoja on kohdassa [Varaston erääntymisraportin esimerkkejä ja logiikka](inventory-aging-report.md).

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Miten voin tarkastella, mitkä vastaanottotapahtumat on täsmäytetty varasto-ottotapahtumaa vasten?

Voit tarkastella varastotapahtuman täsmäytyksiä valitsemalla **Täsmäytykset** tai **Kustannusten hallinta** **Varasto**-välilehdessä **Varastotapahtuma**- tai **Varastotapahtumatiedot**-sivun toimintoruudussa. Jos valitset vastaanoton, kun haluat tarkastella tapahtumaan liittyviä varasto-ottoja, kustannusten hallinta ei näytä tietoja. Tiedot näkyvät vain, jos valitset varasto-ottotapahtuman.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Miten varastoarvoraportti näyttää nimikkeet, joissa on positiivinen fyysinen määrä ja negatiivinen taloudellinen arvo?

Varastoarvoraportti erottaa fyysiset ja taloudelliset summat ja määrät erillisiin sarakkeisiinsa. Raportissa näkyvät arvot ovat raportin suorittamisen aikana valitsemasi päivämäärävälin arvoja. Summaustaso, joka näytetään, riippuu valitsemistasi asetuksista. Jos nimikkeellä on tapahtumia, jotka on vastaanotettu fyysisesti ja otettu varastosta taloudellisesti, määrät ja arvot lasketaan yhteen riippumattomasti. Jos olet valinnut erittelytason näkymään tapahtumina, kunkin vastaanoton ja varasto-oton rivit näytetään erikseen ja vastaavasti fyysiset ja taloudelliset määrät sekä summat näytetään. Lisätietoja on kohdassa [Varaston arvoraportin esimerkkejä ja logiikka](inventory-value-report-examples.md).

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Mikä on varasto- ja seurantadimensioryhmien vaikutus varastoarvoraporttiin?

Jos otat **Kirjanpitoarvo**-vaihtoehdon käyttöön varasto- tai seurantadimensioryhmässä olevalle dimensiolle, voit valita dimension **Näytä**- tai **Yhteensä**-vaihtoehdon varastoarvoraportin konfiguraation dimensiolle. Jos valitset sen dimension **Näytä**- tai **Yhteensä**-vaihtoehdon, jonka **Kirjanpitoarvo** -vaihtoehto ei ole valittuna, sarake on tyhjä raportin tulosteessa. Jos olet ottanut dimension **Kirjanpitoarvo**-asetuksen käyttöön varasto- tai seurantadimensioryhmässä etkä valitse varastoarvoraportin konfiguraation **Näytä**- tai **Yhteensä**-asetusta, järjestelmä luo yhteenvedon niiden valittujen dimensioiden arvoista, joita seurataan taloudellisesti.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Voinko mukauttaa upotettuja Power BI -raportteja kustannuslaskentaa varten?

Kyllä, käyttäjät, joilla on oikeat suojauskäyttöoikeudet, voivat päivittää raportin suunnittelukaaviota mille tahansa upotetulle Power BI -raportille Supply Chain Managementissa. Lisätietoja: [Upotettujen raporttien mukauttaminen analyysityötiloissa](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md).

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Missä varianssin analyysilausuntoa voi tarkastella?

Varianssin analyysin raporttia kohdassa **Kustannusten hallinta \> Kyselyt ja raportit \> Varaston kirjanpito – analyysiraportit** tai **Kustannusten hallinta \> Kyselyt ja raportit \> Valmistuksen kirjanpito – analyysiraportit**. Molemmat vaihtoehdot avaavat saman raportin, ja raportin toiminta on samanlainen.

## <a name="item-prices-and-default-costs"></a>Nimikehinnat ja oletuskustannukset

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Voinko ylläpitää kunkin tuotevariantin kustannusta?

Kyllä. Voit ottaa **Käytä kustannushintaa variantin mukaan** -vaihtoehdon **käyttöön Vapautettu tuote** -sivun **Kustannusten hallinta** -pikavälilehdessä, jos haluat ottaa käyttöön hinnoittelun tuotevariantin mukaan. (Tämä vaihtoehto on käytettävissä vain päätuotteille.) Sitten **Nimikehinta**-sivulla (jonka voit avata **Kustannusversio**- tai **Vapautettu tuote** -sivulta), voit valita **Dimensionäyttö** määrittääksesi, haluatko näyttää **Määritys**-, **Koko**-, **Väri**- tai **Tyyli**-dimension. Jos haluat tallentaa asetukset ja käyttää valittuja dimensioita aina, kun avaat sivun, ota **Tallenna asetukset**-asetus käyttöön ja valitse sitten **OK**. Voit syöttää dimensiot vain nimikkeille, joilla dimensiot ovat aktiivisia tuotedimensioryhmässä.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Voinko ylläpitää kunkin varaston kustannusta?

Ei, et voi ylläpitää nimikkeen hintaa varaston mukaan. Voit kuitenkin ylläpitää kauppasopimuksia osto- tai myyntihinnoille varaston mukaan. Valitse ensin **Ostohinnoille**- tai **Myyntihinnoille**-vaihtoehto **Varastodimensioryhmä**-sivun dimensiolle. Kun sitten luot kauppasopimuskirjauskansion ja avaat dimensioiden rivit, valitse **Varasto \> Näytä dimensiot** valitaksesi, mikä dimensio näytetään ruudukossa. Jos haluat tallentaa asetukset ja käyttää valittuja dimensioita aina, kun avaat sivun, ota **Tallenna asetukset**-asetus käyttöön ja valitse sitten **OK**. Voit syöttää dimensiot vain nimikkeille, joilla dimensiot ovat aktiivisia tuotedimensioryhmässä.

### <a name="what-are-price-charges"></a>Mitä ovat hinnan kulut?

Hintakulujen avulla voit lisätä kiinteän summan nimikkeen hinnan tai kauppasopimuksen yksikköhintaan. Kun lisäät summan **Hintakulut**-kenttään, voit syöttää arvon myös **Kulujen määrä** -kenttään. Hintakuluista kuoletetaan määritetty kulujen määrä. Ota **Sisällytä yksikköhinta** -vaihtoehto käyttöön, jos haluat sisällyttää hintakulut nimikkeen yksikköhintaan. Tämä vaihtoehto on aina käytössä standardikustannusta varten.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Kuinka pitäisi eri valuuttoina hankituille nimikkeille määrittää hinnat?

Jos määrität oletushinnan **Vapautettu tuote** -sivun **Ostohinta**-kenttään, sen oletetaan olevan sen yrityksen kirjanpitovaluuttana, johon kuulut. Samoin jos määrität kustannuslaskelmaversioon ostohinnan, jonka **Hintatyyppi**-kentän arvo on *Osto*, hinnan oletetaan olevan yrityksen kirjanpitovaluuttana. Kun luot ostotilauksen toimittajalle, jolla on eri valuutta, järjestelmä muuntaa valuutan automaattisesti kirjanpitovaluutan summan tapahtumavaluutaksi käyttäen **Kirjanpitovaluutan vaihtokurssin tyyppi** -kentässä määritettyä vaihtokurssia.

Kun luot kauppasopimuskirjauskansion, voit määrittää valuutan, jona hinta ilmoitetaan kullakin rivillä. Voit luoda kauppasopimuksia useille valuutoille, tietyille toimittajille ja monille muille tekijäyhdistelmille. Jos luot ostotilauksen, jossa on kauppasopimus on olemassa valitulle valuutalle, järjestelmä käyttää kauppasopimusta, jonka valuutta on vastaava. Kun kirjaat tapahtumia, kuten tuotteiden vastaanottoja tai laskuja, summa muunnetaan kirjanpidon kirjanpitovaluutaksi kirjanpitoon määritettyä kirjanpidon valuutan vaihtokurssia käyttäen.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Kuinka pitäisi eri valuuttoina hankituille nimikkeille määrittää kustannukset?

Kustannuksia ei voi konfiguroida useammassa kuin yhdessä valuutassa. **Vapautettu tuote** -sivun **Kustannuksen hallinta** -välilehden **Hinta**-kenttään syötetyt nimikehinnan tai oletuskustannusten kustannukset ilmaistaan aina valitun yrityksen kirjanpitovaluuttana.

Jos organisaatiossa käytetään vakiokustannuslaskentaa, määritä strategia kustannusten määrittämiseksi, kun valuuttoja on useita. Määritä myös prosessi, jonka avulla kustannukset päivitetään säännöllisesti. Tämä vähentää kirjattujen varianssien määrää.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Voiko myyntihinnat laskea Kustannusryhmä-sivun Voitto-asetuksen avulla?

Kyllä, voit käyttää **Kustannusryhmä**-sivun **Voitto**-asetusta, kun haluat lisätä prosenttiosuuden, kun myyntihinnat lasketaan kustannuslaskennan avulla. Lisätietoja on kohdassa [Tuoterakenteen laskenta](bom-calculations.md).

## <a name="marking"></a>Merkintä

### <a name="how-does-marking-affect-periodic-costing-models"></a>Miten merkintä vaikuttaa kausittaisiin kustannuslaskelmamalleihin?

Jos käytät kausittaista kustannuslaskentamallia, kuten FIFO, LIFO tai painotettua keskiarvoa ja olet merkinnyt vastaanottotapahtuman varasto-ottotapahtumaa vasten, nimikkeen heuristista mallia ei oteta huomioon varaston sulkemisprosessin aikana. Sen sijaan järjestelmä käyttää varasto-oton kustannuksissa vastaanoton toteutuneita kustannuksia.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>Mitä varaston sulkemisen yhteydessä tapahtuu, kun käytetään merkintää?

Kun merkitset vastaanottoja ja varasto-ottoja, varaston sulkeminen selvittää yhdessä merkityt tapahtumat. Kun tilityksen luomiseen käytetään merkintää, **Tilitys**-sivun **Periaate**-kentän arvoksi tulee *Merkintä*. Jos tapahtuma merkitään ennen sen fyysistä tai taloudellista päivitystä, varasto-otto käyttää merkityn vastaanoton kustannusta käyttökeskiarvokustannuksen asemesta. Jos tapahtumat merkitään kirjanpitopäivityksen jälkeen, varaston sulkemis- ja oikaisuprosessi oikaisee varasto-oton kustannuksen siten, että se vastaa vastaanoton kustannusta.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Voiko tapahtumat merkitä manuaalisesti, kun käytössä on vakiokustannuslaskelma tai liukuva keskiarvo?

Ei, vastaanottoja tai varasto-ottoja ei voi merkitä manuaalisesti, kun käytetään vakiokustannuslaskentaa tai liukuvaa keskiarvoa. Jos tapahtumat (esimerkiksi suoratoimitus tai konsernin sisäiset tilaukset) merkitään automaattisesti, merkintätietue jää jäljelle ja toimii sitovana varauksena. Jos kuitenkin käytät vakiokustannuslaskentaa tai liukuvaa keskiarvoa, tietueiden merkinnällä ei ole vaikutusta nimikkeiden kustannuksiin.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>Miten merkintä vaikuttaa tuloslaskelmaan?

Kun merkitset varasto-ottotapahtuman vastaanottoa vasten, varasto-oton kustannus vastaa valittua vastaanottoa. Kun varasto-otto kirjataan fyysisesti ja taloudellisesti, kirjaus vaikuttaa **Toimitettujen myytyjen tuotteiden kustannukset**- ja **Myytyjen tuotteiden kustannukset – laskutettu** -tileihin, jotka on määritetty varaston kirjausprofiilissa. Jos tapahtuma merkitään fyysisen tai taloudellisen päivityksen jälkeen, *varaston sulkemis- ja oikaisuprosessi* luo oikaisun, jolla on vastaava tosite, joka oikaisee **Myytyjen tuotteiden kustannukset – laskutettu** -tilin ja vastakirjaukset tilille, jonka määrität kohteelle **Yksiköiden kustannukset – laskutettu** (varasto).

### <a name="how-does-marking-affect-master-planning"></a>Miten merkintä vaikuttaa pääsuunnitteluun?

**Pääsuunnittelunparametrit** -sivun **Vakiopäivitys**-välilehdessä on kenttä, jonka nimi on **Päivitä merkintä**. Tässä valittua vaihtoehtoa käytetään, kun vahvistat pääsuunnittelun luoman suunnitellun tilauksen. Käytettävissä ovat seuraavat asetukset:

- *Ei* – Järjestelmä ei tee merkintää.
- *Vakio* – Järjestelmä merkitsee vastaanotot varasto-ottoja vasten tarvekohdistuksen mukaan. Tarvetilaus merkitään täyttötilauksen mukaan. Jos täyttötilaukseen jää jäljelle jokin osa määrästä, täyttötilausta ei merkitä.
- *Laajennettu* – Järjestelmä merkitsee sekä tarvetilaukset että täyttötilaukset riippumatta siitä, jääkö täyttötilaukseen jäljelle jokin avoin määrä.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Negatiivinen varasto

### <a name="when-should-i-allow-physical-negative-inventory"></a>Milloin fyysinen negatiivinen varasto sallitaan?

On suositeltavaa, että fyysistä negatiivista varastoa ei sallita, koska varastossa ei voi olla pienempi määrä kuin 0 (nolla) aineellista nimikettä. Joidenkin alojen ja liiketoimintaskenaarioiden liiketoimintaprosessit voivat kuitenkin rajoittaa toimintoja, jotka edellyttävät, että varasto saa olla fyysisesti negatiivinen. Vähittäismyyjät eivät ehkä esimerkiksi halua estää kassaan rekisteröityä nimikkeen myyntiä, vaikka järjestelmä olisikin ilmoittanut, ettei nimikkeitä ole saatavilla. Prosessivalmistajat tarjoavat toisen esimerkin. Näille valmistajille kulutettava määrä voi ylittää kaavassa suositeltavan määrän. Vaihtoehtoisesti kulutus voi olla arvioitu tarkan määrityksen asemesta siten, että kulutus ylittää määrän tietyssä sijainnissa, kuten säiliössä.

Aina kun mahdollista, arvioi liiketoimintaprosessi ja yritä parantaa sitä, jotta varasto ei voi olla negatiivinen. Jos negatiivinen varasto on sallittava, negatiivisen varaston korjausprosessi tulisi määrittää selkeästi, koska se voi vaikuttaa heikentävästi kustannuslaskentaan.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Milloin negatiivinen kirjanpitovarasto sallitaan?

On suositeltavaa, että useimmat organisaatiot sallivat negatiivisen kirjanpitovaraston. (Useimmissa tapauksissa ostotilauslaskuja ei käsitellä ennen nimikkeiden lähetystä.) Tämä vaihtoehto on otettava käyttöön, kun käytössä on tiettyjä liiketoimintaprosesseja, jotka edellyttävät, että myyntihinta vastaa ostotilauksen lopullista kustannusta. Tämä vaatimus voi koskea esimerkiksi tilaukselle valmistavia aloja tai tiettyjä alueita, joilla se on lain mukaan määräytynyt.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Mitä varasto-oton kustannuksille tapahtuu, kun varasto on negatiivinen?

Kun nimikkeen varasto on negatiivinen ja varastosta otetaan enemmän nimikkeitä kuin niitä on fyysisesti, järjestelmä laskee juoksevan keskiarvon oletusnimikehinnan avulla, jos käytät kausittaista kustannuslaskelmamallia, kuten FIFO, LIFO tai painotettua keskiarvoa. Jos nimikkeelle ei ole määritetty oletushintaa, järjestelmä suorittaa varasto-oton arvolla 0 (nolla). Tämä toiminta voi aiheuttaa sen, että juoksevan keskiarvon laskennat tai liukuvan keskiarvon laskennat ovat epätarkkoja tulevaisuudessa.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Voiko estää nimikkeiden keräilyn, pakkaamisen tai myymisen myyntitilauksissa ja tuotantotilauksissa, jos käytettävissä olevaa varastoa ei ole tarpeeksi?

Kyllä. On suositeltavaa poistaa nimikemalliryhmän **Fyysinen negatiivinen** -asetus käytöstä, jotta nimikkeitä ei keräillä, pakata tai myydä myyntitilauksissa ja tuotantotilauksissa.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Voinko estää nimikkeen laskutuksen myyntitilauksessa, jos samalle nimikkeelle ei ole laskutettu ostotilauksia?

Kyllä. On suositeltavaa poistaa nimikemalliryhmän **Rahoituksellinen negatiivinen** -asetus käytöstä, jotta nimikkeitä ei laskuteta myyntitilauksessa, jos samalle nimikkeelle ei ole laskutettu ostotilauksia.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Miten negatiivinen varasto vaikuttaa bruttokäyttökatteeseen tai muihin taloudellisiin suhdelukuihin?

Kun varaston käyttö sallitaan negatiiviseksi, taseen varastoarvo ja tuloslaskelmassa myytyjen tuotteiden kustannukset voidaan alittaa erityisesti silloin, kun nimikkeille ei ole konfiguroitu oletushintaa. Näin ollen voidaan ylittää taloudelliset raportit ja suhdeluvut, kuten bruttokäyttökatteet, koska kustannukset ovat virheelliset. Jos käytät kausittaista kustannuslaskentamallia, kuten FIFO, LIFO tai painotettua keskiarvoa, varasto-ottojen arvo voidaan oikaista, kun suoritat varaston sulkemis- ja oikaisuprosessin negatiivisten varastomäärien korjaamisen jälkeen. Jos kuitenkin käytät liukuvaa keskiarvoa, yksittäisiä tapahtumia ei voi uudelleenarvostaa.

### <a name="how-should-i-correct-negative-inventory"></a>Miten negatiivinen varasto korjataan?

On suositeltavaa seurata ja korjata negatiivista varastoa säännöllisesti, kun organisaatio tai liiketoimintavaatimukset määräävät, että varasto voi olla negatiivinen. Voit korjata varastoarvoja suorittamalla inventoinnin, kirjaamalla oikaisun tai kirjaamalla siirtotapahtumien kirjauskansion. Jos sinun on otettava huomioon tietyn kirjanpitotilin odottamattomat varastovoitot, suunnittele siirtotapahtumien kirjauskansion käyttöä. Muutoin, kun käytät inventointi- tai varasto-oikaisuprosessia, järjestelmä kirjaa varaston oikaisun **Varaston vastaanotto** -tilille ja vastakirjauksen **Varastomeno – voitto** -tilille, jonka määrität varaston kirjausprofiilissa.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Onko uusi nimike luotava, jos varastoni on muuttunut negatiiviseksi ja kun käytössä on liukuva keskiarvo?

Ei Jos organisaatiosi sallii varaston mennä fyysisesti negatiiviseksi ja käytät varastomallina liukuvaa keskiarvoa, järjestelmä käyttää **Varasto ja varastonhallinnan parametrit** -sivulla määritettyä varakustannussarjaa, joka määrittää, miten kustannukset määritetään varasto-otoille. On suositeltavaa välttää fyysisen negatiivisten varaston sallimista. Lisätietoja on muissa kysymyksissä tämän artikkelin [Negatiivinen varasto](#negative-inventory)-osassa.

## <a name="not-stocked-products"></a>Ei-varastoitavat tuotteet

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Voinko kirjata myyntitilauksen keräysluetteloita ei-varastoitaville tuotteille?

Kun luot keräysluettelon myyntitilaukselle, joka sisältää nimikkeitä, jotka ovat nimikemalliryhmässä, joka ei ole varastoitu, et näe rivejä näille ei-varastoiduille nimikkeille. Warehouse Management -mobiilisovellusta ei voi käyttää ei-varastoitavien nimikkeiden käsittelyyn.

Kun luot pakkausluettelon myyntitilaukselle, joka sisältää nimikkeitä nimikemalliryhmässä, joka ei ole varastoitu, määritä **Määrä**-kentän arvoksi *Keräilty määrä ja ei-varastoidut tuotteet*, jotta sisällytät ei-varastoitavat nimikkeet asiakirjan luonnissa. Jos valitset *Kaikki*, pakkausluetteloon sisällytetään vain varastoidut nimikkeet.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Tuleeko käyttää ei-varastoitavaa tuotetta vai luokkaa (myyntiluokkaa tai hankintaluokkaa)?

Valinta ei-varastoitavan tuotteen ja luokan välillä määräytyy liiketoimintavaatimusten mukaan. Ei-varastoitavilla tuotteilla on yleensä enemmän oletusarvojen, kuten ostotilausten ja myyntitilausten määrien ja hintojen, hallintaa. Siksi ei-varastoitavia tuotteita suositellaan tilanteissa, joissa samaa tuotetta tai palvelua ostetaan tai myydään useammin kuin kerran. Luokista on hyötyä tilanteissa, joissa hinta, nimikkeet, kuvaukset ja niin edelleen ovat epäyhtenäisiä tapahtumasta toiseen. Luokkia voi käyttää myös missä tahansa tuotteessa, kun haluat luokitella tuotetyypin, jota myydään tai ostetaan.

## <a name="service-items"></a>Palvelunimikkeet

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Mitä eroa on palvelunimikkeen ja ei-varastoitavan tuotteen välillä?

Palvelunimike on tuotteen tyyppi. Kun luot juuri vapautetun tuotteen, voit määrittää **Tuotetyyppi**-kentän arvoksi joko *Nimike* tai *Palvelu*. *Nimike* valitaan yleensä sen merkiksi, että nimike on aineellinen, kun taas *Palvelu* on yleensä valittuna sen merkiksi, että nimike on aineeton.

Kaikki vapautetut tuotteet, riippumatta siitä, onko kyseessä nimike- vai palvelutuote, voi olla varastoitava tai ei-varastoitava. Varastoitava- tai ei-varastoitava-asetusta hallitsee vapautetulle tuotteelle valittava nimikemalliryhmä. Kun valitset nimikeryhmän, joka ei ole varastoitava, järjestelmä ei luo varastotapahtumia esimerkiksi liittyvälle myyntitilaukselle tai ostotilaukselle.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Voiko tuoterakenteeseen sisällyttää ei-varastoitavia nimikkeitä?

Ei, et voi sisällyttää tuoterakenteeseen tai kaavaa vapautettua tuotetta, joka on linkitetty nimikemalliryhmään, jonka **Varastoitu**-asetus on poistettu käytöstä. Ei ole merkitystä, onko **Tuotetyyppi**-kentän arvo *Nimike* vai *Palvelu*. Vain varastoitavat nimikkeet voidaan sisällyttää tuoterakenne- tai kaavariveihin.

## <a name="costing-modelspecific-questions"></a>Kustannuslaskentamallikohtaiset kysymykset

### <a name="which-costing-model-should-i-use"></a>Mitä kustannusmallia tulee käyttää?

Valittavat kustannuslaskelmamallit määräytyvät liiketoimintavaatimusten mukaan. Ennen Supply Chain Managementissa käytettävän kustannuslaskentamallin valintaa on vahvistettava, että paikalliset säädökset sallivat mallin. Valinta on suositeltavaa vahvistaa alueellasi sertifioidun kirjanpitäjän kanssa.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Voiko organisaatiossa käyttää useita kustannuslaskentamalleja?

Kyllä. Nimikemalliryhmien tai kustannuslaskelmamallien määrää ei ole rajoitettu, joka voidaan valita Supply Chain Managementissa.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Voinko käyttää useita kustannuslaskentamalleja kullekin nimikkeelle?

Ei Kullekin vapautettavalle tuotteelle voi valita vain yhden kustannuslaskelmamallin. Nimikemalliryhmä hallitsee tätä toimintaa. Jos varastoarvoja raportoitaessa on käytettävä useita kustannuslaskentamalleja, kannattaa käyttää Yleinen varastokirjanpito -lisäosaa.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Mitä kustannuslaskentamenetelmää tulee käyttää tuotannonohjausta käytettäessä?

Valittavat kustannuslaskelmamallit määräytyvät liiketoimintavaatimusten mukaan. Ei ole erityistä etua tai haittaa käyttää mitä tahansa kustannuslaskentamallia, kun organisaatiossa käytetään myös tuotannonohjausta.

### <a name="when-is-fefo-used"></a>Milloin FEFOa käytetään?

FEFO (First Expired, First Out) ei ole kustannuslaskentamenetelmä. Sen sijaan se on varausmenetelmä, jota käytetään usein tuotanto-organisaatioissa. Voit ottaa FEFO-varaukset käyttöön nimikemalliryhmälle ottamalla käyttöön **Päivämäärän mukaan ohjattu FEFO** -asetuksen ja valitsemalla sitten **Keräilyehto**-kentän.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Onko suorituskykyetuja kustannusmallien välillä?

Nimikkeelle valittavalla kustannuslaskentamallilla on yleensä minimaalinen vaikutus järjestelmän yleiseen suorituskykyyn. Varaston sulkemis- tai uudelleenlaskentaprosessin suorittamiseen tarvittavaan aikaan voi kuitenkin vaikuttaa se, minkä varaston kustannuslaskelmamallin valitset. Jos käytetään esimerkiksi standardikustannusta tai liukuvaa keskiarvoa, varaston sulkemisprosessi vaikuttaa järjestelmään vain vähän, koska se ei päivitä jokaista varastotapahtumaa ja luo täsmäytyksiä. Kausittainen kustannuslaskelmamalli, kuten FIFO, LIFO tai painotettu keskiarvo, voi kuitenkin lisätä varaston sulkemisprosessin suorittamiseen tarvittavaa aikaa. Sulkemisprosessi voi olla pidempi, erityisesti silloin, kun lisäät **Nimikekohtainen iteraatioiden enimmäismäärä** -kenttään suuren luvun tai **Pienin sallittu määrä** -kenttään pienen luvun *Sulje varasto* -prosessissa.

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Milloin kiinteää vastaanottohintaa tulee käyttää?

Kun valitset nimikkeelle **Kiinteän vastaanottohinta** -valintaruudun **Nimikemalliryhmä**-sivulla, järjestelmä käyttää vastaanottohintaa varaston vastaanoton standardikustannuksena. Jos tuotteelle määritetty ostohinta ja nimikkeen oletuskustannushinta eroavat toisistaan, ero kirjataan **Kiinteän vastaanottohinnan voitto**- tai **Kiinteän vastaanottohinnan tappio** -tilille ja vastakirjaus **Kiinteän vastaanottohinnan vastakirjaus** -tilille. (Kaikki nämä tilit on määritetty **Kirjaus**-sivulla.)

Valitse **kiinteän vastaanottohinnan** valintaruutu, kun käytät kausittaista kustannuslaskelmamallia, kuten FIFO, LIFO tai painotettua keskiarvoa, ja edellytät, että ostohinnan varianssia seurataan kirjanpidossa, jos vastaanoton hinta eroaa nimikkeen oletuskustannuksista.

### <a name="moving-average"></a>Liukuva keskiarvo

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Onko liukuva keskiarvo sama kuin kelluva keskiarvo?

Liukuvan keskiarvon, kelluvan keskiarvon ja käyttökeskiarvon termejä käytetään usein synonyymeina. Näistä ehdoista liukuva keskiarvo on ainoa virallinen kustannuslaskentamalli, joka on käytettävissä Supply Chain Managementissa. Vaikka käyttökeskiarvo ei ole virallinen kustannuslaskentamalli, se on tekniikka, jota käytetään käytettäessä kausittaista kustannuslaskelmamallia, kuten FIFO, LIFO tai painotettua keskiarvoa. Termiä kelluva keskiarvo ei ole käytössä Supply Chain Managementissa, ja sillä voi olla erilaisia merkityksiä muissa järjestelmissä.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Miten voin huomioida tuotteen vastaanottohinnan ja laskutushinnan väliseen eron käytettäessä liukuvaa keskiarvoa?

Kun käytetään liukuvaa keskiarvoa, fyysisen kustannuksen (vastaanottohinta) avulla lasketaan kaikkien varasto-ottotapahtumien liukuva keskiarvo. Jos fyysinen kustannus (vastaanottohinta) ja taloudellinen kustannus (laskun hinta) eivät ole samat, järjestelmä kirjaa eron automaattisesti päätilille, joka on määritetty **Varaston kirjausprofiili** -sivun **Varasto**-välilehden **Liukuvan keskiarvon hintaero** -kirjaustyypissä.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Missä kohtaa kirjanpitoa näen liukuvan keskiarvon hintaeron?

Kun fyysisen päivityksen kirjauksen ja vastaanoton taloudellisen päivityksen välillä on hintaero, järjestelmä kirjaa eron automaattisesti päätilille, joka on määritetty **Varaston kirjausprofiili** -sivun **Varasto**-välilehden **Liukuvan keskiarvon hintaero** -kirjaustyypissä. Lisätietoja on kohdassa [Liukuva keskiarvo](moving-average.md).

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Mitä tapahtuu, kun käytetään liukuvaa keskiarvoa, ja varasto-otto on ennen vastaanottoa?

Tavallisesti ennen vastaanottoa voi olla varasto-otto, koska sallit nimikemalliryhmälle fyysisen negatiivisen varaston tai koska varasto-otto on takautuva. Lisätietoja on osassa [Negatiivinen varasto](#negative-inventory) tässä artikkelissa.

Jos teet takautuvia tapahtumia, on suositeltavaa harkita tarkkaan liiketoimintaprosessia ja toimintoja sen selvittämiseksi, miten tämä skenaario voidaan välttää. Jos teet takautuvan tapahtuman nimikkeelle, joka käyttää liukuvaa keskiarvoa, järjestelmä määrittää tapahtumalle nykyisen liukuvan keskiarvon. Myöhempiä varasto-ottoja ei oikaista. Lisätietoja liukuvasta keskiarvosta takautuvissa tapahtumissa on kohdassa [Liukuva keskiarvo](moving-average.md).

### <a name="standard-costing"></a>Vakiokustannuslaskenta

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Mitä eroa on vakiokustannuslaskennan ja kiinteän vastaanottohinnan välillä?

Vakiokustannuslaskelma edellyttää, että määrität nimikkeen hinnan ja aktivoit kustannuksen kustannuslaskelmaversiossa. Tätä kustannusta käytetään kaikissa vastaanotoissa ja varasto-otoissa. Varastovastaanottojen varianssit kirjataan kirjanpitoon käyttämällä **Varaston kirjausprofiili** -sivun **Standardikustannus**-välilehdessä määritettäviä standardikustannusten varianssitilejä.

Jos kuitenkin käytät kiinteää vastaanottohintaa, vain vastaanottojen kustannus on kiinteä ja järjestelmä käyttää **Kustannushallinta**-pikavälilehdessä määritettävää kustannusta **Vapautettu tuote** -sivulla. Oletuskustannusten ja ostotilauksen hinnan väliset erot aiheuttavat ostohinnan varianssin kirjaamisen kiinteän vastaanottohinnan voitto- ja tappiotileille. Varasto-oton yhteydessä ei ole käytössä kiinteää vastaanottohintaa. Sen sijaan varasto-otot arvostetaan kirjauksen yhteydessä käyttökeskiarvon mukaan (jos et käytä merkintää) ja ne uudelleenarvostetaan sen heuristisen mallin mukaan, jonka valitset, kun suoritat varaston sulkemisen.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Voiko standardikustannuslaskelmassa käyttää FEFO-varauksia?

Kyllä, voit käyttää FEFO-varauksia nimikemalliryhmässä, kun valitset vakiokustannuslaskennan. FEFO-varaukset ohjaavat nimikkeiden fyysisessä käsittelyssä käytettävää varauslogiikkaa, kun taas standardikustannuslaskenta ohjaa nimikkeen fyysisiä ja taloudellisia kustannuksia.

### <a name="can-i-upload-pending-prices"></a>Voiko odottavat hinnat ladata palvelimeen?

Kyllä, voit ladata odottavan hinnan Excel-lisäosan tai tietohallintakehyksen avulla. On suositeltavaa käyttää seuraavia yksiköitä:

- Odottavat nimikehinnat (V2)
- Odottavat työreitityksen kustannusluokan yksikkökustannukset
- Kustannuslaskentalomakkeen solmun laskentakertoimet (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Kuinka usein nimikkeen standardikustannukset voidaan päivittää?

Uuden standardikustannuksen aktivointiväliä ei ole rajoitettu. Jos aktivoit nimikkeelle uuden kustannuksen samana päivänä kuin viimeinen kustannus aktivoitiin, järjestelmä käyttää uusissa tapahtumissa tai päivityksissä (esimerkiksi aiemmin luotujen tapahtumien päivityksissä) viimeisintä aktivoitua kustannusta.

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Voiko aktivoidun kustannuksen poistaa tai voiko sen aktivoinnin poistaa?

Ei, aktivoitua kustannusta ei voi poistaa tai sen aktivointia poistaa. Jos olet aktivoinut kustannuksen virheellisesti, voit aktivoida uuden kustannuksen, jossa on oikea kustannus.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Käytetäänkö laskentaryhmiä vakiokustannuslaskennassa?

Laskentaryhmiä voi käyttää minkä tahansa nimikkeen kanssa valitusta nimikemalliryhmästä riippumatta. Laskentaryhmiä käytetään kustannusten koonti- tai kustannuslaskentaprosessin aikana niiden nimikkeiden asetusten määrittämiseen, joille laskenta suoritetaan. Lisätietoa laskentaryhmistä on kohdassa [Tuoterakenteen laskentaryhmät](bom-calculation-groups.md).

### <a name="when-should-i-use-a-planned-costing-version"></a>Milloin suunniteltua kustannuslaskelmaversiota käytetään?

Kustannuslaskelmaversioiden tyyppi voi olla *Vakiokustannus* tai *Suunniteltu kustannus*. *Vakiokustannus*-tyyppiä käytetään kustannuksille, jotka ovat aktiivisia järjestelmässä ja jotka kirjataan tapahtumiin. *Suunniteltu kustannus* -tyyppiä käytetään kustannusten simulointien ajossa, eikä se vaikuta tapahtumien kustannuksiin.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Voiko yhden yksikön kokonaiskustannukset siirtää toiselle yksikölle myyntikustannuksena?

Kustannuksia ei voi kopioida automaattisesti yrityksestä toiseen. Lisäksi kustannuksia ei voi kopioida automaattisesti ostohinnasta myyntihintaan. Jos organisaation on suoritettava jokin näistä tehtävistä, mieti, voitko viedä tiedot kustannuslaskelmaversiosta ulos tietojen hallintakehyksen avulla ja ladata ne eri yritykseen joko kustannuslaskelmaversion myyntihintana tai kauppasopimuksena. Tiedostojen manuaalinen käsittely saattaa olla tarpeen.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Mikä on paras tapa kopioida suunnitellut kustannukset vakiokustannuslaskelmaversioon?

**Kustannuslaskelmaversiot**-sivulla voit kopioida nimikkeen hinnat, kustannusluokkien hinnat tai epäsuorat kustannukset kustannuslaskelmaversiosta toiseen **Kopioi**-painikkeen avulla.
