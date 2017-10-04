---
title: Talousraportin komponentit
description: "Tässä artikkelissa käsitellään raportin määritysten osia tai rakenneosia käytetään talousraportoinnissa. Näitä rakenneosia ovat rivi-, sarake- ja raportointipuun määritykset. Artikkelissa käsitellään rakenneosien järjestämistä ja lukitsemista sekä rakenneosaryhmien käyttöä."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 5c09b1fc061f95cd78e9f18c2bdf846fdbfc7cf1
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="financial-report-components"></a>Talousraportin komponentit

[!include[banner](../includes/banner.md)]


Tässä artikkelissa käsitellään raportin määritysten osia tai rakenneosia käytetään talousraportoinnissa. Näitä rakenneosia ovat rivi-, sarake- ja raportointipuun määritykset. Artikkelissa käsitellään rakenneosien järjestämistä ja lukitsemista sekä rakenneosaryhmien käyttöä. 

Talousraporttien suunnittelutoiminnon suunnitteluperiaate on hajottaa tiedot mahdollisimman pieniksi osiksi tai rakenneosiksi. Tämän jälkeen näitä voi sitten yhdistellä tarpeen mukaan. Tällä tavoin raporttimuotoilu on erillään taloustiedoista ja voit muuttaa raportin muotoa ilman, että taloustietoja on muokattava Microsoft Dynamics ERP -järjestelmässä. Tämän rakenneosatoiminnon avulla voit yhdistää tekstiä, summia ja laskelmia sekä muodostaa niiden avulla tarvittavia raportteja. Lisäksi joustavat toiminnot kannustavat myös luovuuteen, koska toimintojen tarkasteleminen eri tavoilla on helppoa. Raportin määrityksen yksittäiset rakenneosat ovat samanlaisia kuin kolmiulotteiset laskentataulukot, mutta ne ovat laskentataulukkoja tehokkaampia. Raportin määritys määrittää raportissa käytettävän rivin, sarakkeen ja valinnaisesti myös raportointipuun määrityksen. Se sisältää myös tietoja luodun raportin tallennuspaikasta ja sen muotoilusta. Uudelleenkäytettävyyden ja jakamisen helpottamiseksi voidaan luoda rakenneosaryhmiä, jotka ovat yritykseen liitettyjen aiemmin luotujen raporttien, rivien, sarakkeiden ja raportointipuiden määritysten sekä dimensioyhdistelmien yhdistelmiä.

## <a name="building-blocks-of-a-report"></a> Raportin rakenneosat
| Rakenneosa            | Kuvaus                                                                                                                                                                                                                                                                              | Lisätietoja                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Rivimääritys            | Rivin määritys määrittää raportin kuvaavat rivit (esimerkiksi palkalle tai myynnille). Siinä on myös luettelo segmenttiarvoista tai dimensioista, jotka sisältävät kunkin rivinimikkeen arvot. Myös rivin muotoilun ja laskelmat ovat mukana.                                                    | [Rivimääritykset](row-definitions-financial-reporting.md)                       |
| Sarakemääritys         | Sarakkeen määritys määrittää kauden, jota käytetään taloushallinnon dimensioiden tietojen purkamisessa. Se sisältää myös sarakkeen muotoilun ja laskelmat.                                                                                                                                 | [Sarakkeiden määritykset](column-definitions-financial-reports.md)         |
| Raportointipuun määritys | Raportointipuun määritys muistuttaa organisaatiokaaviota. Se sisältää yksittäisiä raportointiyksiköitä, jotka edustavat kaavion kutakin ruutua. Yksiköt voivat olla joko taloushallinnon tietojen yksittäisiä osastoja tai korkeamman tason yksiköitä, jotka sisältävät muiden raportointiyksiköiden yhteenvetotietoja. | [Raportointipuiden määritykset](financial-reporting-tree-definitions.md) |
| Raportin määritys         | Raportin määritys käyttää raportin muodostuksessa rivin, sarakkeen ja valinnaisesti myös raportointipuun määritystä. Se sisältää myös raportin muokkaamisessa käytettäviä lisäasetuksia.                                                                    | [Raportin määritys](design-financial-report-definitions.md)                  |

Jos et ole aiemmin suunnitellut raportteja, ohjatun raporttien luontitoiminnon avulla voit luoda nopeasti raportin määrityksen, jota voit mukauttaa myöhemmin. Jos raporttien suunnitteleminen on tuttua ja haluat suunnitella raportin joustavasti, voit luoda uuden raportin määrityksen yhdistämällä uusia tai aiemmin luotuja rakenneosia. Laadukkaita raportteja voi muodostaa, vaikka kaikki käytettävissä olevat raportin määrityksen asetukset eivät olisikaan tuttuja. Voit laajentaa raporttien määrityksiä ja ottaa enemmän toimintoja käyttöön, kun tutustut raporttien suunnittelemiseen paremmin. Kun olet luonut perusraportin, voit mukauttaa raportin määritystä ja mitä tahansa raportin määrityksen rakenneosaa.

## <a name="organize-the-building-blocks"></a>Rakenneosien järjestäminen
Järjestä rakenneosat Report Designerissa kansioiden avulla. Kaikki kansiot liittyvät niihin rakenneosatyyppeihin, joita ne sisältävät. Esimerkiksi kaikki rivien määrityksiä sisältävät kansiot sijaitsevat Report Designerin **Rivien määritykset** -ruudussa.

### <a name="create-a-folder"></a>Kansion luominen

1.  Valitse Report Designerissa rakenneosan tyyppi, kun haluat järjestää siirtymisruudun. Voit lajitella esimerkiksi rivin määrityksen valitsemalla **Rivien määritykset**.
2.  Valitse siirtymisruudussa aiemmin luotu kansio, jonne uusi kansio luodaan. Tee sitten jonkin seuraavista toiminnoista:
    -   Napsauta pääkansiota hiiren kakkospainikkeella ja valitse sitten **Uusi kansio**.
    -   Valitse ensin pääkansiossa **Tiedosto** ja sitten **Uusi kansio**.

3.  Kun uusi kansio tulee näkyviin, anna sille nimi ja paina Enter-näppäintä.

## <a name="lock-a-building-block"></a> Rakenneosan lukitseminen
Voit suojata ja lukita rakenneosan luomalla sille salasanan. Voit nostaa tällä tavoin raportin osan suojaustasoa ilman, että koko järjestelmän suojaus nousee. Salasana auttaa suojaamaan tärkeitä rakenneosan tietoja, joita tarvitaan kuukauden lopussa tehtävässä raportointiprosessissa. Rakenneosan lukitseminen on mahdollista kaikilla käyttäjärooleilla. Muilla käyttäjillä on kuitenkin aina lukitun osan lukuoikeus. Käyttäjät voivat avata lukitun osan, muuttaa sitä sekä tallentaa sen uudella nimellä. Järjestelmänvalvojan roolin omaava käyttäjä voi aina käyttää ja muuttaa lukittua rakenneosaa.
1.  Avaa raportin osa Report Designerissa, kun haluat lukita esimerkiksi rivin, sarakkeen, raportin tai raportointipuun määrityksen.
2.  Valitse **Työkalut**-valikossa **Suojaus tai poista suojaus**. Voit myös napsauttaa työkalurivillä **Suojaus tai poista suojaus** -kuvaketta (lukkokuvake).
3.  Anna salasana ja vahvista se **Suojaus**-valintaikkunassa ja valitse sitten **OK**. Työkalurivin lukituskuvake näkyy korostettuna, kun avoinna oleva rakenneosa on lukittu.

Voit poistaa rakenneosan lukituksen avaamalla rakenneosan ja valitsemalla sitten työkalurivillä **Suojaus tai poista suojaus**. Vaihtoehtoisesti voi valita **Työkalut**-valikossa **Poista suojaus**.

## <a name="building-block-groups"></a>Rakenneosaryhmät

Rakenneosat ovat raporttia varten luotavia rivien, sarakkeiden, raportointipuiden ja raporttien määrityksiä. Rakenneosaryhmät ovat yritykseen liitettyjen määritys- dimensioyhdistelmien kokoelmia. Rakenneosaryhmät voivat olla yrityskohtaisia, mutta sama rakenneosajoukko voi olla myös usean yrityksen käytössä. Jos joillakin yrityksillä on eri tilikartta, yrityksissä kannattaa ehkä käyttää eri rakenneosaryhmiä. Vaihtoehtoisesti voit nimetä kaikki yksittäiset rakenneosat niin, että ne vastaavat rakenneosien kanssa yhteensopivaa yritystä.
### <a name="create-a-building-block-group"></a>Rakenneosaryhmän luominen

1.  Valitse Report Designerin **Yritys**-valikossa **Rakenneosaryhmät**.
2.  Valitse **Rakenneosaryhmät**-valintaikkunassa **Uusi**.
3.  Syötä rakenneosaryhmälle yksilöivä nimi ja kuvaus. Kussakin kentässä voi olla enintään 256 merkkiä. (Välilyönnit sisältyvät tähän lukuun.)
4.  Luo uusi rakenneosaryhmä valitsemalla **OK**.

### <a name="assign-a-building-block-group"></a>Rakenneosaryhmän liittäminen

Kun olet luonut rakenneosaryhmän, määritä se ainakin yhteen yritykseen. Voit luoda sitten raportin, rivin, sarakkeen ja raportointipuun määritykset ja tallentaa ne rakenneosaryhmään. Kaikki rakenneosat on suljettava ennen seuraavan menettelyn aloittamista.
1.  Valitse Report Designerin **Yritys**-valikossa **Yritykset**.
2.  Valitse **Yritykset**-valintaikkunassa yritys, johon rakenneosaryhmä liitetään.
3.  Valitse **Muokkaa**.
4.  Valitse **Muokkaa yritystä** -valintaikkunan **Rakenneosaryhmä**-kentässä rakenneosa, johon yritys liitetään, tai luo uusi rakenneosaryhmä valitsemalla **Uusi**.
5.  Liitä rakenneosaryhmä valitsemalla **OK**.
6.  Sulje **Yritykset**-valintaikkuna valitsemalla **Sulje**. Valitsemasi rakenneosaryhmä on nyt liitetty yritykseen. Nyt kaikki juuri luodut rivien, sarakkeiden jne. määritykset ovat tähän yritykseen liitetyn rakenneosaryhmän osia. Voit myös tuoda .tdbx-tiedoston tai -raportin toisesta järjestelmästä.

### <a name="view-a-building-block-group"></a> Rakenneosaryhmän tarkasteleminen

Kun rakenneosaryhmä on luotu ja sitä käytetään, voit tarkastella kaikkia siihen liitettyjä rakenneosia. Voit myös viedä tai tuoda rakenneosaryhmän. Voit myös suorittaa rakenneosaryhmissä muita ylläpitotoimia.
1.  Valitse Report Designerin **Yritys**-valikossa **Rakenneosaryhmät**.
2.  Valitse **Rakenneosaryhmät**-valintaikkunassa tarkasteltava rakenneosaryhmä.
3.  Avaa **Näytä rakenneosaryhmä**-valintaruutu valitsemalla **Näytä**. Voit tarkastella ikkunassa rakenneosaryhmän sisältöä.
4.  Sulje valintaikkunat valitsemalla **Sulje**.

### <a name="save-a-building-block-group-under-a-new-name"></a>Tallenna rakenneosaryhmä uudella nimellä

Voit tallentaa aiemmin luodun rakenneosaryhmän uudella nimellä. Voit sitten muokata uutta rakenneosaryhmää niin, että alkuperäinen rakenneosaryhmä ei muutu.
1.  Valitse Report Designerin **Yritys**-valikossa **Rakenneosaryhmät**.
2.  Valitse **Rakenneosaryhmät**-valintaikkunassa uudella nimellä tallennettava rakenneosaryhmä.
3.  Valitse **Tallenna nimellä**.
4.  Syötä rakenneosaryhmälle uusi nimi ja kuvaus.
5.  Napsauta **OK**. Uusi rakenneosaryhmä näkyy **Rakenneosaryhmät**-valintaikkunassa.

### <a name="export-a-building-block-group"></a> Rakenneosaryhmän vieminen

Voit viedä rakenneosanryhmän tai rakenneosaryhmän tietyn raportin rakenneosat. Voit käyttää vietyä rakenneosaryhmää varmuuskopiona. Voit myös kopioida viedyt tiedot rakenneosaryhmien tai Finance and Operations -asennusten välillä. Report Designer ja rakenneosaryhmä sisältävät yhdessä viitatut fonttityylit ja dimensioyhdistelmät.
1.  Valitse Report Designerin **Yritys**-valikossa **Rakenneosaryhmät**.
2.  Valitse **Rakenneosaryhmät**-valintaikkunassa vietävä rakenneosaryhmä. Valitse sitten **Vie**.
3.  Valitse **Vie**-valintaikkunassa vietävät raporttien määritykset.
    -   Voit viedä kaikki raporttien määritykset ja liittyvät rakenneosat valitsemalla **Valitse kaikki**.
    -   Voit viedä tiettyjä raportti-, rivi-, sarake-, puu- ja dimensioyhdistelmiä valitsemalla kyseisen välilehden ja valitsemalla sitten vietävät kohteet. Voit valita välilehdessä useita kohteita pitämällä Ctrl-näppäintä alhaalla. **Huomautus:** Kun valitset vietävät raportit, myös liittyvät rivi-, sarake-, puu- ja dimensioyhdistelmät valitaan.

4.  Kun vietävien kohteiden valinta on tehty, valitse **Vie**.
5.  Valitse **Tallenna nimellä** -valintaikkunassa sijainti, jonne rakenneosaryhmä viedään.
6.  Kirjoita **Tiedostonimi**-kenttään tiedoston nimi. Report Designer lisää tiedostolle automaattisesti .tdbx-tunnisteen.
7.  Valitse **Tallenna**. Rakenneosaryhmä tallennetaan määrittämääsi sijaintiin.

### <a name="import-a-building-block-group"></a> Rakenneosaryhmän tuominen

Voit tuoda rakenneosaryhmän aiemmin luotuun rakenneosaryhmään tai voit luoda tiedoille uuden rakenneosaryhmän. Alkuperäiset fonttityylit ja yritysviittaukset säilyvät kaikissa tuoduissa rakenneosaryhmissä, ja ne sisältävät tarvittavat dimensioyhdistelmät.
1.  Valitse Report Designerin **Yritys**-valikossa **Rakenneosaryhmät**.
2.  Valitse **Rakenneosaryhmät**-valintaikkunassa rakenneosa, johon rakenneosaryhmä tuodaan. Valitse sitten **Tuo**.
3.  Valitse **Avaa**-valintaikkunassa tuotava rakenneosaryhmä. Valitse sitten **Avaa**.
4.  Valitse **Tuo**-valintaikkunassa tuotavat raporttien määritykset.
    -   Voit tuoda kaikki raporttien määritykset ja niitä tukevat rakenneosat valitsemalla **Valitse kaikki**.
    -   Voit tuoda tiettyjä raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmiä valitsemalla tuotavat raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmät.

5.  Kun tuotavien kohteiden valinta on tehty, valitse **Tuo**.

### <a name="undo-a-checkout-of-a-building-block"></a> Rakenneosan uloskuittauksen peruuttaminen

Kun käyttäjä avaa rakenneosan, muut käyttäjät voivat käyttää kyseistä rakenneosaa ainoastaan vain luku -tilassa. Joskus käyttäjät saattavat unohtaa sulkea rakenneosan tai he sammuttavat järjestelmän rakenneosan sulkematta. Rakenneosa pysyy siinä tapauksessa uloskuitattuna eivätkä muut käyttäjät voi avata sitä. Näissä tilanteissa talousraportoinnin järjestelmänvalvoja voi kuitata **Uloskuitatut kohteet** -valintaikkunassa sisään rakenneosat, jotka käyttäjät ovat jättäneet uloskuitatuiksi. **Huomautus:** Vain järjestelmänvalvojan roolin omaavat käyttäjät voivat kuitata rakenneosia sisään **Uloskuitatut kohteet** -valintaikkunassa.
1.  Valitse Report Designerin **Työkalut**-valikosta **Uloskuitatut kohteet**.
2.  Valitse **Uloskuitatut kohteet** -valintaikkunassa **Näytä kaikkien käyttäjien kohteet**. Luettelossa näkyvät kaikki rakenneosat, jotka on kuitattu ulos, ne rakenneosat uloskuitanneet käyttäjät.
3.  Valitse rakenneosa ja valitse sitten **Peruuta uloskuittaus**.
4.  Valitse **Kyllä**, kun haluat kuitata rakenneosan sisään.

# <a name="see-also"></a>Lisätietoja

[Taloushallinnan raportointi](financial-reporting-intro.md)



