---
title: Talousraportin komponentit
description: Tässä artikkelissa käsitellään raportin määritysten osia tai rakenneosia käytetään talousraportoinnissa.
author: aprilolson
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.form: FinancialReports
ms.openlocfilehash: 180b3c64b9eb506f162071a67b1fa9b728a569ce
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831607"
---
# <a name="financial-report-components"></a>Taloushallinnon raportin komponentit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään raportin määritysten osia tai rakenneosia käytetään talousraportoinnissa. Näitä rakenneosia ovat rivi-, sarake- ja raportointipuun määritykset. Tässä artikkelissa kerrotaan, miten rakenneosat järjestetään ja lukitaan.

Talousraporttien suunnittelutoiminnon suunnitteluperiaate on hajottaa tiedot mahdollisimman pieniksi osiksi tai rakenneosiksi. Tämän jälkeen näitä voi sitten yhdistellä tarpeen mukaan. Tällä tavoin raporttimuotoilu on erillään taloustiedoista ja voit muuttaa raportin muotoa ilman, että taloustietoja on muokattava Microsoft Dynamics 365 Financessa. Tämän rakenneosatoiminnon avulla voit yhdistää tekstiä, summia ja laskelmia sekä muodostaa niiden avulla tarvittavia raportteja. Lisäksi joustavat toiminnot kannustavat myös luovuuteen, koska toimintojen tarkasteleminen eri tavoilla on helppoa. Raportin määrityksen yksittäiset rakenneosat ovat samanlaisia kuin kolmiulotteiset laskentataulukot, mutta ne ovat laskentataulukkoja tehokkaampia. Raportin määritys määrittää raportissa käytettävän rivin, sarakkeen ja valinnaisesti myös raportointipuun määrityksen. Se sisältää myös tietoja luodun raportin tallennuspaikasta ja sen muotoilusta.

## <a name="building-blocks-of-a-report"></a>Raportin rakenneosat

| Rakenneosa            | kuvaus | Lisätietoja |
|---------------------------|-------------|----------------------|
| Rivimääritys            | Rivin määritys määrittää raportin kuvaavat rivit (esimerkiksi palkalle tai myynnille). Siinä on myös luettelo segmenttiarvoista tai dimensioista, jotka sisältävät kunkin rivinimikkeen arvot. Myös rivin muotoilun ja laskelmat ovat mukana. | [Rivimääritykset](row-definitions-financial-reporting.md) |
| Sarakemääritys         | Sarakkeen määritys määrittää kauden, jota käytetään taloushallinnon dimensioiden tietojen purkamisessa. Se sisältää myös sarakkeen muotoilun ja laskelmat. | [Sarakkeiden määritykset](column-definitions-financial-reports.md) |
| Raportointipuun määritys | Raportointipuun määritys muistuttaa organisaatiokaaviota. Se sisältää yksittäisiä raportointiyksiköitä, jotka edustavat kaavion kutakin ruutua. Yksiköt voivat olla joko taloushallinnon tietojen yksittäisiä osastoja tai korkeamman tason yksiköitä, jotka sisältävät muiden raportointiyksiköiden yhteenvetotietoja. | [Raportointipuiden määritykset](financial-reporting-tree-definitions.md) |
| Raportin määritys         | Raportin määritys käyttää raportin muodostuksessa rivin, sarakkeen ja valinnaisesti myös raportointipuun määritystä. Se sisältää myös raportin muokkaamisessa käytettäviä lisäasetuksia. | [Raportin määritys](design-financial-report-definitions.md) |

Jos et ole aiemmin suunnitellut raportteja, ohjatun raporttien luontitoiminnon avulla voit luoda nopeasti raportin määrityksen, jota voit mukauttaa myöhemmin. Jos raporttien suunnitteleminen on tuttua ja haluat suunnitella raportin joustavasti, voit luoda uuden raportin määrityksen yhdistämällä uusia tai aiemmin luotuja rakenneosia. Laadukkaita raportteja voi muodostaa, vaikka kaikki käytettävissä olevat raportin määrityksen asetukset eivät olisikaan tuttuja. Voit laajentaa raporttien määrityksiä ja ottaa enemmän toimintoja käyttöön, kun tutustut raporttien suunnittelemiseen paremmin. Kun olet luonut perusraportin, voit mukauttaa raportin määritystä ja mitä tahansa raportin määrityksen rakenneosaa.

## <a name="organize-the-building-blocks"></a>Rakenneosien järjestäminen
Järjestä rakenneosat Report Designerissa kansioiden avulla. Kaikki kansiot liittyvät niihin rakenneosatyyppeihin, joita ne sisältävät. Esimerkiksi kaikki rivien määrityksiä sisältävät kansiot sijaitsevat Report Designerin **Rivien määritykset** -ruudussa.

### <a name="create-a-folder"></a>Kansion luominen

1. Valitse Report Designerissa rakenneosan tyyppi, kun haluat järjestää siirtymisruudun. Voit lajitella esimerkiksi rivin määrityksen valitsemalla **Rivien määritykset**.
2. Valitse siirtymisruudussa aiemmin luotu kansio, jonne uusi kansio luodaan. Tee sitten jonkin seuraavista toiminnoista:

    - Napsauta pääkansiota hiiren kakkospainikkeella ja valitse sitten **Uusi kansio**.
    - Valitse ensin pääkansiossa **Tiedosto** ja sitten **Uusi kansio**.

3. Kun uusi kansio tulee näkyviin, anna sille nimi ja paina **Enter**-näppäintä.

## <a name="lock-a-building-block"></a> Rakenneosan lukitseminen
Voit suojata ja lukita rakenneosan luomalla sille salasanan. Voit nostaa tällä tavoin raportin osan suojaustasoa ilman, että koko järjestelmän suojaus nousee. Salasana auttaa suojaamaan tärkeitä rakenneosan tietoja, joita tarvitaan kuukauden lopussa tehtävässä raportointiprosessissa. Rakenneosan lukitseminen on mahdollista kaikilla käyttäjärooleilla. Muilla käyttäjillä on kuitenkin aina lukitun osan lukuoikeus. Käyttäjät voivat avata lukitun osan, muuttaa sitä sekä tallentaa sen uudella nimellä. Järjestelmänvalvojan roolin omaava käyttäjä voi aina käyttää ja muuttaa lukittua rakenneosaa.

1. Avaa raportin osa Report Designerissa, kun haluat lukita esimerkiksi rivin, sarakkeen, raportin tai raportointipuun määrityksen.
2. Valitse **Työkalut**-valikossa **Suojaus tai poista suojaus**. Voit myös napsauttaa työkalurivillä **Suojaus tai poista suojaus** -kuvaketta (lukkokuvake).
3. Anna salasana ja vahvista se **Suojaus**-valintaikkunassa ja valitse sitten **OK**. Työkalurivin lukituskuvake näkyy korostettuna, kun avoinna oleva rakenneosa on lukittu.

Voit poistaa rakenneosan lukituksen avaamalla rakenneosan ja valitsemalla sitten työkalurivillä **Suojaus tai poista suojaus**. Vaihtoehtoisesti voi valita **Työkalut**-valikossa **Poista suojaus**.

## <a name="building-block-groups"></a>Rakenneosaryhmät

Rakenneosat ovat raporttia varten luotavia rivien, sarakkeiden, raportointipuiden ja raporttien määrityksiä. Rakenneosaryhmät ovat määritysten ja dimensioarvoyhdistelmien kokoelmia.

### <a name="view-a-building-block-group"></a>Rakenneosaryhmän katseleminen

Voit tarkastella kaikkia rakenneosaryhmään liitettyjä rakenneosia. Voit myös viedä tai tuoda rakenneosaryhmän.

1. Valitse raporttien suunnitteluohjelman **Yritys**-valikosta **Rakenneosaryhmät**.
2. Valitse **Rakenneosaryhmät**-valintaikkunassa tarkasteltava rakenneosaryhmä.
3. Avaa **Näytä rakenneosaryhmä**-valintaruutu valitsemalla **Näytä**. Voit tarkastella ikkunassa rakenneosaryhmän sisältöä.
4. Sulje valintaikkunat valitsemalla **Sulje**.

### <a name="export-a-building-block-group"></a>Rakenneosaryhmän vieminen

Voit viedä rakenneosan ryhmän tai tietyn raportin rakenneosia rakenneosan ryhmässä. Voit käyttää vietyä rakenneosan ryhmää varmuuskopiona. Voit myös kopioida viedyt tiedot asennusten välillä. Report Designer ja rakenneosaryhmä sisältävät yhdessä viitatut fonttityylit ja dimensioarvoyhdistelmät.

1. Valitse raporttien suunnitteluohjelman **Yritys**-valikosta **Rakenneosaryhmät**.
2. Valitse **Rakenneosaryhmät**-valintaikkunassa rakenneosaryhmä, jonka haluat viedä, ja valitse sitten **Vie**.
3. Valitse **Vie**-valintaikkunassa vietävät raporttien määritykset.

    - Voit viedä kaikki raporttien määritykset ja liittyvät rakenneosat valitsemalla **Valitse kaikki**.
    - Voit viedä tiettyjä raportti-, rivi-, sarake-, puu- ja dimensioarvoyhdistelmiä valitsemalla kyseisen välilehden ja valitsemalla sitten vietävät kohteet. Voit valita välilehdessä useita kohteita pitämällä Ctrl-näppäintä alhaalla.

    > [!NOTE]
    > Kun valitset vietävät raportit, niihin liittyvät rivit, sarakkeet, puut ja dimensioarvoyhdistelmät tulevat valituiksi.

4. Kun vietävien kohteiden valinta on tehty, valitse **Vie**.
5. Valitse **Tallenna nimellä** -valintaikkunassa sijainti, jonne rakenneosaryhmä viedään.
6. Kirjoita **Tiedostonimi**-kenttään tiedoston nimi. Report Designer lisää tiedostolle automaattisesti .tdbx-tunnisteen.
7. Valitse **Tallenna**. Rakenneosaryhmä tallennetaan määrittämääsi sijaintiin.

### <a name="import-a-building-block-group"></a> Rakenneosaryhmän tuominen

Voit viedä rakenneosaryhmän aiemmin luotuun rakenneosaryhmään. Alkuperäiset fonttityylit ja yritysviittaukset säilyvät kaikissa tuoduissa rakenneosaryhmissä, ja ne sisältävät tarvittavat dimensioarvoyhdistelmät.

1. Valitse raporttien suunnitteluohjelman **Yritys**-valikosta **Rakenneosaryhmät**.
2. Valitse **Rakenneosaryhmät**-valintaikkunassa rakenneosa, johon haluat tuoda rakenneosaryhmän, ja valitse sitten **Tuo**.
3. Valitse **Avaa**-valintaikkunassa rakenneosaryhmä, jonka haluat tuoda, ja valitse sitten **Avaa**.
4. Valitse **Tuo**-valintaikkunassa tuotavat raporttien määritykset.

    - Voit tuoda kaikki raporttien määritykset ja niitä tukevat rakenneosat valitsemalla **Valitse kaikki**.
    - Voit tuoda tiettyjä raportti-, rivi-, sarake-, puu- tai dimensioarvoyhdistelmiä valitsemalla tuotavat raportti-, rivi-, sarake-, puu- tai dimensioarvoyhdistelmät.

5. Kun tuotavien kohteiden valinta on tehty, valitse **Tuo**.

### <a name="undo-a-checkout-of-a-building-block"></a> Rakenneosan uloskuittauksen peruuttaminen

Kun käyttäjä avaa rakenneosan, muut käyttäjät voivat käyttää kyseistä rakenneosaa ainoastaan vain luku -tilassa. Joskus käyttäjät saattavat unohtaa sulkea rakenneosan tai he sammuttavat järjestelmän rakenneosan sulkematta. Rakenneosa pysyy siinä tapauksessa uloskuitattuna eivätkä muut käyttäjät voi avata sitä. Näissä tilanteissa talousraportoinnin järjestelmänvalvoja voi kuitata **Uloskuitatut kohteet** -valintaikkunassa sisään rakenneosat, jotka käyttäjät ovat jättäneet uloskuitatuiksi.

> [!NOTE]
> Sinulla on oltava järjestelmänvalvojan rooli, jotta voit kuitata rakenneosia sisään **Uloskuitatut nimikkeet** -valintaikkunan avulla.

1. Valitse Report Designerin **Työkalut**-valikosta **Uloskuitatut kohteet**.
2. Valitse **Uloskuitatut nimikkeet** -valintaikkunassa **Näytä kaikkien käyttäjien nimikkeet**. Luettelo päivittyy, ja siinä näkyvät kaikki ne rakenneosat, jotka ovat uloskuitattuina, sekä käyttäjät, jotka ovat kuitanneet ne ulos.
3. Valitse rakenneosa ja valitse sitten **Kumoa uloskuittaus**.
4. Kuittaa rakenneosa sisään valitsemalla **Kyllä**.

## <a name="additional-resources"></a>Lisäresurssit

[Talousraportointi](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
