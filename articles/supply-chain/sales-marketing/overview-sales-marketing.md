---
title: Myynnin ja markkinoinnin yleiskuvaus
description: Voit käyttää myyntiä ja markkinointia myyntivirran erityyppisten tietojen hankkimiseen, tallentamiseen ja käyttämiseen. Näitä tietoja ovat alkuperäinen myyntitoimenpide, tulevaisuuden seurantatoiminto ja lisämyynnit.
author: kfend
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 92303
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b079e560f006c7dc9df1cb6e4642f6bff0e1417
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218414"
---
# <a name="sales-and-marketing-overview"></a>Myynnin ja markkinoinnin yleiskuvaus

[!include [banner](../includes/banner.md)]

Voit käyttää myyntiä ja markkinointia myyntivirran erityyppisten tietojen hankkimiseen, tallentamiseen ja käyttämiseen. Näitä tietoja ovat alkuperäinen myyntitoimenpide, tulevaisuuden seurantatoiminto ja lisämyynnit.

<a name="marketing"></a>Markkinointi
---------

Voit etsiä markkinointikampanjoihin ja -toimintoja avulla mahdollisiin asiakkaisiin ja luoda heihin suhteita niin, että ensimmäiset yhteydenotot muuttuvat myyntisuhteiksi. Seuraava prosessikuva näyttää markkinoinnin liiketoimintaprosessin. [![Markkinoinnin liiketoimintaprosessi](./media/marketing01.jpg)](./media/marketing01.jpg)

### <a name="relationships"></a>Suhteet

Myynnissä ja markkinoinnissa ensikosketus mahdollisiin asiakkaisiin voi tapahtua monenlaisissa tilanteissa. Voit löytää mahdollisen asiakkaan esimerkiksi messuilla tai asiakas voi muuttua mahdolliseksi liidiksi organisaation massapostituskampanjan jälkeen. On erittäin tärkeää tiedostaa osapuolen yksikkö, ennen kuin yksiköstä tulee asiakas. Seuraavassa kuvassa on yksikkösuhteet, kun mahdollisesta asiakkaasta tulee varsinainen asiakas. [![SalesandMarketing01](./media/salesandmarketing01.jpg)](./media/salesandmarketing01.jpg)

### <a name="campaigns"></a>Kampanjat

Kampanjan kohteena ovat ne prospektien, liidien, mahdollisuuksien ja asiakkaiden yhteyshenkilöt, jotka on valittu osallistumaan kampanjaan. Voit luoda Supply Chain Managementissä monenlaisia kampanjoita, kuten puhelinmarkkinointi-, postitus- ja sähköpostikampanjoita, joilla asiakaspotentiaali voidaan maksimoida. Kun kampanja etenee ja saat positiivisia vastauksia, voit aloittaa myyntiprosessin niiden vastaajien kanssa, jotka vastasivat myönteisesti kampanjaan.

## <a name="sales"></a>Myynti
Myyntitoimintoa käytetään tarjousten, lisämyynnin ja ristiin myynnin luomiseen uusille ja nykyisille asiakkaille, myyntitilausten luomiseen ja asiakkaiden myyntilaskujen luomiseen. Seuraava prosessikuva näyttää myynnin liiketoimintaprosessin. [![Myynnin liiketoimintaprosessi](./media/sales01.jpg)](./media/sales01.jpg)

### <a name="sales-quotations"></a>Myyntitarjoukset

Voit tarjota asiakkaille toimittamiasi hyödykkeitä tai palveluja luomalla myyntitarjouksia. Asiakas voi pyytää tarjousta tai voit luoda tarjouksen vastauksena mahdollisen tai nykyisen asiakkaan pyyntöön. Kun asiakas hyväksyy myyntitarjouksen, voit muuntaa sen myyntitilaukseksi.

### <a name="up-sellcross-sell"></a>Lisämyynti / liittyvien tuotteiden myynti

Lisä- ja ristiinmyynti ovat tuotteiden myyntitekniikoita, kun tilaus on merkitty asiakkaalle. Lisämyynnissä nykyisen tuotteen tilalle ehdotetaan toista tuotetta. Ristiinmyynnissä tuotetta ehdotetaan nykyisen tuotteen lisäksi. Kun määrität tuoteluetteloita, voit luoda erityissääntöjä ilmaisemaan, milloin tuotetta ehdotetaan ristiin- tai lisämyyntituotteeksi.

### <a name="sales-orders"></a>Myyntitilaukset

Kun uusi myyntitilaus luodaan, valitse luotavan myyntitilauksen tyyppi. Vaihtoehtoja on viisi. **Huomautus:** kun olet luonut myyntitilauksen, mitä tahansa tilaustyyppiä voidaan muuttaa. Poikkeuksena on kuitenkin **nimikkeiden vaatimustyyppi**, jos myyntitilauksen tila on **Toimitettu**.

| Myyntitilauksen tyyppi  | Kuvaus                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kirjauskansio           | Käytä tätä tyyppiä myyntitilauksen luonnoksena. Tämä tyyppi se ei vaikuta varastomääriin eikä luo nimiketapahtumia.                                                                                                                                                                    |
| Ylläpitosopimus      | Tätä tyyppiä käytetään toistuville tilauksille. Kun tilaus laskutetaan, tilauksen tilaksi tulee automaattisesti avoin tilaus. Laskutettu toimitusmäärä ja jäljelle jääneet toimitukset päivitetään. Et voi käyttää tätä myyntitilaustyyppiä, jos käytät varastonhallintatoimintoa. |
| Myyntitilaus       | Tätä tyyppiä käytetään, kun asiakas on tehnyt tai vahvistanut tilauksen.                                                                                                                                                                                                                                        |
| Palautettu tilaus    | Tyyppiä käytetään, kun asiakas palauttaa nimikkeen. Palautusnumero määritetään automaattisesti.                                                                                                                                                                                            |
| Nimiketarpeet | Tämä tyyppi luodaan automaattisesti, kun nimike myydään projektin kautta.                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>Myyntisopimukset

Myyntisopimus on sopimus, jolla asiakas vahvistaa ostavansa tuotetta tietyn määrän tai tietyn summan tietyssä ajassa saadakseen erikoishinnan ja alennuksia. Myyntisopimuksen hinnat ja alennukset korvaavat kaikki kauppasopimuksissa määritetyt hinnat ja alennukset. Myyntisopimus on voimassa määritetyn ajan. Myynnille **Myyntitilaus**-sivulla määritettävän pyydetyn lähetyspäivämäärän on oltava voimassaolokaudella. Oletusarvon mukaan myyntisopimus on pidossa. Voit tilata myyntisopimuksesta vain, kun sen asetuksena on **Voimassa** .

### <a name="backorders"></a>Jälkitoimitukset

Tilausten tallentaminen ja vahvistaminen edellyttää ehkä jälkitoimitusten ja poikkeusten hallintaa, ennen kuin myynti on valmis. Jälkitoimitukset ovat joko ostotilauksia, joita toimittaja ei ole vielä toimittanut, tai myyntitilauksia, joita ei ole vielä toimitettu asiakkaalle. Jälkitoimitusten seuranta on tärkeää. Jos esimerkiksi toimittajien tuotetoimitukset myöhästyvät, asiakastoimituksen päivämäärää voidaan joutua lykkäämään ja ilmoittamaan asiakkaille viivästyksestä. Voit tarkastella jälkitoimituksia nimikkeen, asiakkaan tai toimittajan mukaan.

#### <a name="viewing-backorders-by-item"></a>Nimikekohtaisten jälkitoimitusten tarkasteleminen

Kun tarkastelet jälkitoimituksia nimikekohtaisesti, voit seurata tietyn tuotteen tulevien tapahtumien odotettua kulkua. Voit esimerkiksi tarkistaa seuraavat tiedot.

-   Nimikkeestä tehtyjen myyntitilausten määrä
-   Mahdollisesti puuttuvat nimiketoimitukset toimittajalta
-   Nimikkeen mahdolliset lisätilaukset, jotta kaikki myyntitilaukset voidaan toimittaa ajallaan

Tekemällä tämä tarkistuksen voit vastata asiakkaiden pyyntöihin nimiketoimituksen ajoittamisesta. Lisäksi myyntitilauksille voi määrittää prioriteetteja ja jakaa varastossa olevat nimikkeet tilausten kesken.

#### <a name="viewing-backorders-by-customer"></a>Asiakaskohtaisten jälkitoimitusten tarkasteleminen

Asiakaskohtaisia jälkitoimituksia tarkastelemalla voit tarkastella asiakkaan jäljellä olevia tilauksia. Tämä tarkistus on kätevä, kun sinun vastattava viivästyneitä nimikkeitä odottaville asiakkaille.

#### <a name="viewing-backorders-by-vendor"></a>Toimittajakohtaisten jälkitoimitusten tarkasteleminen

Kun tarkastelet toimittajakohtaisia jälkitoimituksia, voit seurata puuttuvia toimituksia ja odotettuja toimituspäiviä. Tämä tarkistus auttaa myös priorisoimaan jälkitilaukset, kun tuotteet saapuvat toimittajilta ja myyntitilaukset on kerättävä toimitettavaksi.

### <a name="invoices"></a>Laskut

Myyntiprosessin aikana voi luoda kolmenlaisia laskuja:

-   Myyntilasku
-   Vapaatekstilasku
-   Proformalasku

#### <a name="customer-invoice"></a>Myyntilasku

Myyntilasku on lasku, jonka organisaatio antaa asiakkaalle myynnin yhteydessä. Voit luoda tällaisen myyntilaskun otsikon sisältävän myyntitilauksen sekä vähintään yhden nimike- tai palvelurivin perusteella. Myyntilasku päättää myyntitilauksen, pakkausluettelon ja myyntilaskujakson.  

Voit kirjata ja tulostaa yhden myyntilaskun joko myyntitilauksen tai pakkausluettelon ja päivämäärän perusteella. Voit myös kirjata ja tulostaa useita myyntilaskuja yhdessä pakkausluettelojen ja päivämäärien perusteella. Kun kirjaat yhden myyntilaskun myyntitilauksen avulla, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen myyntitilausten laskujen kokonaismäärän mukaiseksi.  

Jos myyntitilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), myyntitilauksen tilaksi muutetaan **Laskutettu**. Jos kummankaan kentän määrä ei ole 0, myyntitilauksen tilaa ei muuteta ja voit merkitä lisälaskuja. Jos aiot kirjata ja tulostaa vähintään yhden myyntilaskun pakkausluettelojen perusteella, kullekin myyntitilaukselle on jo oltava kirjattuna vähintään yksi pakkausluettelo. Myyntilasku perustuu pakkausluetteloihin ja vastaa niiden luettelossa olevia määriä.  

Voit luoda myyntilaskun niiden pakkausluettelon rivinimikkeiden perusteella, jotka on toimitettu tähän mennessä, vaikka kaikkia tietyn myyntitilauksen nimikkeitä ei olisi vielä toimitettu. Näin kannattaa tehdä esimerkiksi silloin, kun yritys lähettää asiakkaalle kuukaudessa yhden laskun, joka sisältää kaikki kuukauden aikana tehdyt toimitukset. Jokainen pakkausluettelo edustaa myyntitilauksen nimikkeiden osatoimitusta tai täydellistä toimitusta.  

Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen pakkausluetteloiden toimitusten kokonaismäärällä. Jos myyntitilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), myyntitilauksen tilaksi muutetaan **Laskutettu**. Jos määrä ei ole 0, myyntitilauksen tilaa ei muuteta ja voit merkitä lisälaskuja. Varastotapahtumat päivitetään laskun numerolla ja myyntitilausrivin tilaksi muutetaan **Laskutettu**.

#### <a name="free-text-invoice"></a>Vapaatekstilasku

Vapaatekstilasku on lasku, joka ei liity myyntitilaukseen. Sen tilausriveillä on kirjanpitotilit, vapaatekstikuvaukset ja myyntisumma. Tällaiseen laskuun ei ovi antaa nimiketunnusta. Lisäksi soveltuvat arvonlisäverotiedot on annettava. Myynnin päätilin ilmaistaan jokaisella laskurivillä. Asiakkaan saldo kirjataan vapaatekstilaskussa käytetystä kirjausprofiilista yhteenvetotilille.

#### <a name="pro-forma-invoice"></a>Proformalasku

Proformalasku on lasku, joka laaditaan todellisen laskusumman ennusteena ennen laskun kirjaamista. Proformalaskun voi tulostaa joko myyntilaskulle tai vapaatekstilaskulle.

### <a name="additional-resources"></a>Lisäresurssit

#### <a name="blogs"></a>Blogit

Myyntiprosessin yleiskatsaus on kirjoituksessa [Myynnin toiminta Dynamics 365 for Finance and Operationsissa](https://financefunction.tech/2018/05/15/how-sales-work-in-dynamics-365-for-finance-and-operations).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]