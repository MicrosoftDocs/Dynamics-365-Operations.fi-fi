---
title: Projektinhallinta ja kirjanpito
description: Projektinhallinnan ja kirjanpidon toimintoja voidaan käyttää useilla aloilla palvelu tarjoamiseksi, tuotteen tuottamiseksi tai tuloksen saavuttamiseksi.
author: KimANelson
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable; ProjProjectManagementWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82a2da882ba951c2ff6420b726e0546e9073d2e4
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/12/2019
ms.locfileid: "969397"
---
# <a name="project-management-and-accounting"></a>Projektinhallinta ja kirjanpito

[!include [banner](../includes/banner.md)]

Projektinhallinnan ja kirjanpidon toimintoja voidaan käyttää useilla aloilla palvelu tarjoamiseksi, tuotteen tuottamiseksi tai tuloksen saavuttamiseksi.  

Projekti on tehtäväryhmä, joka on suunniteltu tarjoamaan palvelu, tuottamaan tuote tai tuloksen saavuttamiseksi. Projektit kuluttavat resursseja ja luovat taloudellisia tuloksia tuottojen tai käyttöomaisuuden muodossa.

## <a name="projects-across-industries"></a>Projektit eri aloilla
Projektinhallinnan ja kirjanpidon toimintoja voidaan käyttää useilla aloilla kuvassa esitetyllä tavalla.

[![Projektit eri aloilla](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

Puhelinpalvelukeskuksessa, lipun avulla voidaan kuvata joukko toimenpiteitä, joita puhelun ratkaiseminen edellyttää. Konsulttiyritykset, kuten hallinnolliset tai tekniset konsulttiorganisaatiot tai mainostoimistot, viittaavat toimintoihinsa projekteina. Markkinoinnissa kampanja edustaa työtehtäviä, jotka pitää toimittaa. Projektiin perustuvassa valmistuksessa, tuotantotilaus liittyy eri töihin, jotka on tehtävä valmiiden tuotteiden tuottamiseksi. Mitä nimiä niistä käytetäänkään, näihin projekteihin sisältyy resurssit, aikataulut sekä kustannukset. Projektinhallinta- ja kirjanpito-toiminnot Microsoft Dynamics 365 for Finance and Operationsissa voivat auttaa suunnittelussa, suorituksessa ja projektianalyysissä.

## <a name="project-phases"></a>Projektin vaiheet
Vaikka seuraava prosessinkulku on suunnattu ulkoisiin projekteihin tai projektiin, jotka ovat valmiita yhdelle tai useammalle asiakkaalle, toiminto koskee myös sisäisiä kustannus vain -projekteja. 

![Projektin 3 vaihetta](./media/3-stages-of-a-project.png) 

Kuten edellisessä kuvassa näkyy, projektinhallinta ja kirjanpito voidaan jakaa kolmeen vaiheeseen:

1.  Aloita
2.  Suorita
3.  Analysoi

## <a name="initiate-the-project"></a>Aloita projekti
Projektin aloittamisessa suoritetaan useita keskeisiä prosesseja. Voit lähettää asiakkaalle työmäärän arvion, kulut ja materiaalin projektitarjouksena. Voit tallentaa laskutuksen ehdot, rajoitukset ja sopimukset projektisopimukseen. Voit käyttää työnositus (WBS) suunnitelmaa arvioimaan työtä. Voit määrittää budjetit ja ennusteet ja ohjata projektin suorittamista. Seuraavassa kuvassa näkyy projektin rakenne. [![projektin rakenne](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Luo projektitarjoukset

Projektin myynnin alkuvaiheessa voit projektitarjouksen avulla tarjota asiakkaalle tarjouksen, joka ei ole sitova. Tarjous voi sisältää useita elementtejä, kuten tarjoukseen sisältyvät nimikkeet ja palvelut, perusyhteystiedot, erityiskauppasopimukset ja alennukset sekä mahdolliset verot ja lisämaksut.

Voit myös tehdä organisaatiosi ja asiakkaan välisen takuuasiakirjan projektitarjoustapahtumalle. Kun projektitarjous on luotu, voit luoda asiakkaalle takausasiakirjapyynnön ja lähettää sen pankkiin. Kun pankki on hyväksynyt pyynnön, takausasiakirja myönnetään asiakkaalle. 

Lisätietoja on kohdassa [Projektitarjoukset](project-quotations.md).

### <a name="create-project-contracts"></a>Luo projektisopimukset

Kun saat sopimuksen asiakkaan tai muun rahoituslähteen kanssa viedäksesi projektin loppuun, sinun on ensin luotava projektisopimus. Seuraavaksi, kun luot projektin, sinun on määritettävä se vastaavaan sopimukseen. Se, minkä tyyppisen projektin luot projektisopimukselle, määrittää millä tavalla projektin asiakkaita laskutetaan. Voit muokata projektisopimusta ja siihen liittyvää projektia, mutta et voi muuttaa projektityyppiä. Lisätietoja projektityypeistä kohdassa "Projektien luominen".

Lisätietoa projektisopimuksista kohdassa [Projektisopimukset](project-contracts.md)

### <a name="create-work-breakdown-structures"></a>Luo työrakenteen malleja

Työrakenteen tarkkuus riippuu arvioiden ja arvioissa käytettävien seurantasojen vaaditusta tarkkuustasosta. Projektit, joissa on vähän toleranssia aikataulussa tai hinnassa lipeämiseen, edellyttävät tavallisesti yksityiskohtaisemman työnosituksen (WBS) ja ne myös edellyttävät, että työnkulkua ja kustannuksia seurataan turvallisemmin työnosituksen puitteissa. 

Lisätietoja on kohdassa [Työrakenteet](work-breakdown-structures.md).

### <a name="create-project-forecasts-and-budgets"></a>Projektibudjettien ja ennusteiden luominen

Jos organisaatiossasi on toiminnallinen näkökulma ja keskitytään tuottoihin ja kustannuksiin, jotka ovat peräisin tietyistä tapahtumista, voidaan käyttää ennusteita. Mutta jos organisaatiosi keskittyy enemmän taloushallinnon summiin, voit käyttää budjetointia. Kummallakin menetelmällä on omat etunsa. Lisätietoja on kohdassa [Projektien budjetit ja ennusteet](project-forecasts-budgets.md).

### <a name="create-projects"></a>Luo projektit

Voit luoda kuusi eri projektityyppiä Microsoft Finance and Operationsissa. Kullekin projektityypille on määritetty eri kustannukset ja tuotot tunnistamista varten. Valitsemasi projektityyppi määräytyy projektin tarkoituksen mukaan. Seuraavassa taulukossa kuvataan jokaisen projektityypin tavallinen käyttötarkoitus.
                                                                                                            
<table>
  <tr>
    <td>Projektityyppi</th>
    <td>Kuvaus</th>
  </tr>
  <tr>
    <td>Aika ja materiaali</td>
    <td>Aika- ja materiaaliprojekteissa asiakasta laskutetaan kaikista projektin toteutuneista kustannuksista. Näihin kuluihin sisältyvät tuntien kustannukset, kulut, nimikkeet ja maksut.</td>
  </tr>
  <tr>
    <td>Kiinteä hinta</td>
    <td>Kiinteähintaisten projektien laskut koostuvat ennakkolaskutapahtumista. Kiinteähintainen projekti laskutetaan projektisopimukseen perustuvan laskutusaikataulun mukaisesti. Kiinteähintaisen projektien tuotto voidaan laskea ja kirjata koko projektin ajan käyttämällä valmistumisprosenttimenetelmää. Vaihtoehtoisesti, tuotto voidaan laskea ja kirjata, kun projekti on valmis, käyttämällä valmissopimus-menetelmää. Yritykset voivat usein hyötyä käyttämällä KET-arvoa projektin tai projektien ryhmän valmiusasteen laskentaan.</td>
  </tr>
  <tr>
    <td>Investointi</td>
    <td>Investointiprojektit ovat projekteja, jotka eivät tuota tuloja välittömästi. Niitä käytetään tavallisesti pitkäaikaisissa, sisäisissä projekteissa, joissa kustannukset täytyy aktivoida. Investointiprojektille voidaan tallentaa vain nimikkeiden, tuntien ja kulujen kustannukset. Investointiprojektiin kustannuksia seurataan ja hallitaan käyttämällä arviointitoimintoa. Investointiprojekteille voidaan määrittää valinnainen enimmäisaktivointi. Investointiprojektin edistyessä kirjaat kustannuksia KET-tileille, joilla kustannukset pidetään projektin valmistumiseen saakka. Kun projekti eliminoidaan, KET-arvo siirretään käyttöomaisuuteen, kirjanpitotilille tai uuteen projektiin. <br></br> <strong>HUOMAUTUS:</strong> Investointiprojektien tapahtumia ei näytetä <strong>Kirjaa kustannukset<strong>, <strong>Jaksota tuotot</strong>, tai<strong>Luo laskutusehdotukset</strong> -sivulla.</td>
  </tr>
  <tr>
    <td>Kustannusprojekti</td>
    <td>Vastaavasti kuin investointiprojekteja, kustannusprojekteja käytetään tavallisesti sisäisten projektien seurantaan ja niihin voidaan tallentaa vain tunnit, kulut ja nimikkeet. Kustannusprojektit ovat kuitenkin tavallisesti lyhyempiä kuin investointiprojektit. Lisäksi, investointiprojekteista poiketen, kustannusprojekteja ei voida aktivoida tasetileille. Sen sijaan niiden projektitapahtumat kirjataan vain tulostileihin. <br></br> <strong>HUOMAUTUS:</strong> Kustannusprojektien tapahtumia ei näytetä <strong>Kirjaa kustannukset</strong>-, <strong>Jaksota tuotot</strong> tai <strong>Luo laskutusehdotukset</strong> -sivulla. Kustannusprojekteja käytetään pääasiassa sisäisten projektien valvontaan, joten niiden ei yleensä tarvitse liittyä asiakastiliin. Kuitenkin asetusten vaatiessa nimikevaatimuksien luontia ostotilauksia varten, täytyy kustannusprojekti yhdistää asiakkaan kanssa. Tämä yhdistäminen tarvitaan, koska nimiketarpeita hallitaan myyntitilausriveinä ja järjestelmä edellyttää, että asiakas on määritettävä. Tämä asetus ei kuitenkaan aiheuta nimiketarpeiden automaattista luomista ostotilauksesta. Kustannusprojekteissa <strong>luo nimiketarve</strong>-asetusta ei oteta huomioon. Tarvitessasi nimiketarvetta kustannusprojektissa voit luoda sen manuaalisesti, edellyttäen että asiakas on liitetty projektiin.</td>
  </tr>
  <tr>
    <td>Sisäinen</td>
    <td>Sisäisiä projekteja käytetään kustannusten seurantaan organisaatiosi sisäisessä projektissa. Sisäinen projekti voi tarjota suunnittelutyökalun resurssien kulutuksen hallintaan. <br></br><strong>HUOMAUTUS:<strong> Sisäisten projektien tapahtumia ei näytetä <strong>Jaksota tuotot</strong> tai <strong>Luo laskutusehdotukset</strong> -sivulla.</td>
  </tr>
  <tr>
    <td>Aika</td>
    <td>Aikaprojekteja käytetään seuraamaan aikaa, joka liitetään ei-veloitettaviin ja tuottamattomiin toimintoihin, kuten projektiin, joka seuraa työntekijöiden sairaslomia. Aikaprojektien tapahtumia ei kirjata kirjanpitoon. Sen sijaan ne on sisällytetty työntekijän käyttöasteen raportteihin. Aikaprojekteissa voi tallentaa vain tuntitapahtumia. Voit rekisteröidä nämä tunnit projektiin kirjauskansion tai aikaraportin avulla. Kun tunnit kirjataan, ne näkyvät projektin tapahtumina, joilla ei ole vastaavaa tositetapahtumaa. <br></br><strong>HUOMAUTUS:</strong> Aikaprojektien tapahtumia ei näytetä <strong>Kirjaa kustannukset</strong>, <strong>Jaksota tuotot</strong> tai <strong>Luo laskutusehdotukset</strong> -sivulla.</td>
  </tr>
</table>


### <a name="assign-workers-categories-and-resources"></a>Työntekijöiden, luokkien ja resurssien määrittäminen

Voit ajoittaa työntekijäresurssit, jotka perustuvat joko projektin vaatimuksiin ja aikatauluun, tai työntekijöiden taitoihin ja käytettävyyteen. Resurssin ajoituksen avulla voit ottaa käyttöön oman organisaatiosi työntekijöiden resurssit tehokkaasti. Löydät nopeasti pätevimmät työntekijät, jotka ovat käytettävissä projektiasi varten. Näet myös helposti, miten näitä työntekijöitä voidaan käyttää tehokkaammin projektin aikana. 

Seuraavassa on esimerkkejä siitä, kuinka voit käyttää resurssien ajoitustoimintoa:

-   Käytä työntekijän määritteitä koskevia tietoja kuten koulutus, taidot, varmenteet ja projektikokemus, hakiessasi projektin vaatimuksiin soveltuvaa työntekijää.
-   Käytä työntekijän kalenteria ja saatavuutta koskevia tietoja hakiessasi projektikalenterin kanssa yhteensopivaa työntekijää.
-   Tarkista jokaisen työntekijän kapasiteetti ja määritä, miten sitä käytetään. Esimerkiksi, jos työntekijää ei hyödynnetä täysin, työntekijä voidaan määrittää projektiin, joka sopii hänen käytettävyyteensä ja ominaisuuksiinsa.
-   Tarkastele työntekijän käytettävyyttä varmistaaksesi, että heidän varauksissaan ei ole kalenteriristiriitoja.
-   Tarkastele työntekijän käyttöä joko yhteenvetona (esimerkiksi osaston tai työntekijän mukaan) tai valitse yksityiskohtainen näkymä (kuten osaston työntekijöiden mukaan tai kaikkien työntekijöiden viikoittaisten tietojen mukaan).
-   Muokkaa resurssinmäärityksiä eri aikayksiköille, kuten päivä, viikko tai kuukausi, jotta työntekijöiden käyttö voidaan optimoida.

## <a name="execute-the-project"></a>Projektin suorittaminen
Projektia suoritettaessa ryhmän jäsenet tai esimies tallentavat työmäärä ja aiheutuneet kustannukset, käyttämällä aikaraportteja, kuluraportteja ja muita liikeasiakirjoja. Projektipäälliköillä on työkaluja, joiden avulla he voivat seurata projektin budjetoitujen kokonaissummien käyttöä. Projektipäälliköt voivat myös tilata, kerätä tai hankkia materiaaleja projekteihin käyttämällä ostotilauksia ja muita liiketoiminta-asiakirjoja. Laskut laaditaan ja hyväksytään, niin että asiakkaita laskutetaan käynnissä olevasta työstä. Lopuksi tämän prosessin aikana tuotto hyväksytään vaikuttamaan organisaation myyntitietoja.

### <a name="manage-work-breakdown-structures"></a>Hallitse työrakenteen malleja

WBS on kuvaus työstä, joka on suoritettava projektia varten. WBS on työtehtävien arvojärjestys. Se vastaa ei ainoastaan kuhunkin tehtävään liittyvästä työstä, mutta myös koosta, kustannuksista ja tehtävän kestosta. 

Lisätietoja on kohdassa [Työrakenteet](work-breakdown-structures.md).

### <a name="manage-project-forecasts-and-budgets"></a>Projektibudjettien ja ennusteiden hallinta

Projekteja voidaan hallita ja kontrolloida kahdella tavalla: projektiennusteilla ja projektien budjeteilla. Jos organisaatiossasi on toiminnallinen näkökulma ja keskitytään tuottoihin ja kustannuksiin, jotka ovat peräisin tietyistä tapahtumista, voidaan käyttää ennusteita. Mutta jos organisaatiosi keskittyy enemmän taloushallinnon summiin, voit käyttää budjetointia.

Lisätietoja on kohdassa [Projektien budjetit ja ennusteet](project-forecasts-budgets.md).

### <a name="create-production-orders"></a>Luo tuotantotilauksia

Projekteihin liittyvä tuotantotilaus voidaan yhdistää myyntitilaukseen tai nimiketarpeeseen, joko käyttämällä valmiissa nimike -menetelmää tai kulutettu nimike -menetelmää. Lisäksi jos tuotantotilaus on luotu manuaalisesti, ei ole linkkiä tuotantotilauksen ja myyntitilauksen tai nimikevaatimuksen välillä (ei linkkiä tilaukseen). Mutta jos tuotantotilaus on luotu automaattisesti myyntitilauksen tai nimiketarpeen täyttämiseksi, tuotantotilauksen ja myyntitilauksen tai nimiketarpeen välillä on yhteys (linkki tilaukseen). 

Perustuen näiden tekijöiden yhdistelmiin, käytä yhtä seuraavista tavoista:

- **Valmis nimike / linkki tilaukseen** – yhdistää projektin myyntitilaukseen tai nimiketarpeeseen. Tämän menetelmän avulla voit kirjata toteutuneet projektikustannukset, jotka on jo kirjattu, kun myyntitilaus laskutetaan tai kun nimiketarve päivitetään pakkausluetteloon. Kustannukset kirjataan valmiina nimikkeenä.
- **Valmis nimike / ei linkkiä tilaukseen** – toteutuneita kustannuksia ei voida kirjata ennen kuin nimikkeen tuotannon elinkaaren tila on **Päättynyt**. Valmiin nimikkeen kustannukset kirjataan yhtenä tapahtumana.
- **Käytetty nimike / linkki tilaukseen** – yhdistää projektin nimiketarpeeseen. Tämän menetelmän avulla voit tarkastella toteutuneita projektikustannuksia, kun tuotannon tila on **Aloitettu** tai kun tuotanto raportoidaan valmiiksi. Kustannukset kirjataan useina tuotannossa käytettyjen raaka-aineiden ja tuntien projektinimiketapahtumina. Kun nimiketarve päivitetään pakkausluetteloon, projektikustannuksia ei kirjata. Voit myös määrittää, millä tuoterakennehierarkian tasolla tuotannon projekteja seurataan.
- *<strong><em>Käytetty nimike / ei linkkiä tilaukseen</em></strong>* – yhdistää projektin nimiketarpeeseen. Tämän menetelmän avulla voit tarkastella toteutuneita projektikustannuksia, kun tuotannon tila on <strong>Aloitettu</strong> tai kun tuotanto raportoidaan valmiiksi. Kustannukset kirjataan useina tuotannossa käytettyjen raaka-aineiden ja tuntien projektinimiketapahtumina. Voit myös määrittää, millä tuoterakennehierarkian tasolla tuotannon projekteja seurataan.

### <a name="procure-products-and-services"></a>Hanki tuotteita ja palveluja

Nimikkeiden ostaminen ja myyminen ovat tärkeimpiä tehtäviä monissa projekteihin keskittyneissä yrityksissä.

#### <a name="purchase-orders-for-projects"></a>Projektin ostotilaukset

Ostotilauksen tarkoitus määrittää ostotilauksen kulutusajankohdan ja tämän vuoksi sen, mitkä nimikkeet veloitetaan projektissa.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tapa</th>
<th>Tarkoitus</th>
<th>Nimikkeiden kulutus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Luo ostotilaus suoraan.</td>
<td>Projektissa käytettävien nimikkeiden ostaminen ulkopuoliselta toimittajalta. Voit luoda ostotilaus seuraavilla tavoilla.
<ul>
<li>Itse projektista. Tässä tapauksessa projekti on jo määritetty ostotilaukselle.</li>
<li>Siirtymällä projektin ostotilaukseen. Tällöin on valittava sekä toimittaja että projekti, jolle ostotilaus luodaan.</li>
</ul></td>
<td>Nimikkeet kulutetaan, kun toimittajalasku päivitetään.</td>
</tr>
<tr class="even">
<td>Ostotilauksen luominen myyntitilauksesta</td>
<td>Nimikkeiden ostaminen silloin kun luodaan ostotilaus projektista.</td>
<td>Nimikkeet kulutetaan, kun myyntitilaus laskutetaan asiakkaalta.</td>
</tr>
<tr class="odd">
<td>Ostotilauksen luominen nimiketarpeen perusteella</td>
<td>Nimikkeiden ostaminen silloin kun luodaan nimiketarve projektista.</td>
<td>Nimikkeet kulutetaan, kun nimiketarpeen pakkausluettelo päivitetään.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Projektien myyntitilaukset

Projektinhallinnassa ja kirjanpidossa nimikkeiden kulutus voidaan rekisteröidä usealla eri tavalla. Voit myydä tai ostaa nimikkeitä projektista tai varata nimikkeitä projektia varten. 

Voit tilata projektissa käytettäviä nimikkeitä yrityksen varastosta. Vaihtoehtoisesti, voit ostaa nimikkeitä ulkoiselta toimittajalta. Muissa kuin Aika-tyyppiä olevissa projekteissa voidaan kuluttaa nimikkeitä. 

Nimikkeiden tilaustapa riippuu siitä, mistä niitä tilataan:

-   Jos haluat tilata nimikkeitä yrityksen varastosta, sinun on syötettävä tilaus nimiketarpeena. Jos käytät **Nimiketarpeet**-sivua, voit määrittää tarpeen niin, että vastaanotat nimikkeet osatoimituksina. Tällöin voit siirtää nimikemäärän kulutusta siihen asti kun nimikettä tarvitaan.
-   Tilataksesi nimikkeitä ulkoiselta toimittajalta, sinun on luotava tilaus ostotilauksena **Ostotilaus**-sivulla.

> [!NOTE] 
> Projektiin liittyvän myyntitilauksen pakkausluetteloa ei voi peruuttaa, jos nimikkeet on jo merkitty pakkausta varten. 

Seuraavassa taulukossa kuvataan menetelmät nimikkeiden tilaamiseksi ja kuinka nimikkeet kulutetaan.

| Tapa            | Tarkoitus                                                                                                                                                        | Nimiketapahtumien kulutus                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Myyntitilaus       | Syötä tapahtuma suoraan aika ja materiaaliprojektiin.                                                                                                   | Nimiketapahtumat kulutetaan myyntilaskun kirjaamisen yhteydessä.                                                                               |
| Varastokirjauskansio | Kirjoita ja ylläpidä nimikearkistot nopeasti. Jos haluat esimerkiksi syöttää nimiketarpeen tulostetun luettelon perusteella, varastokirjauskansio voidaan kohdistaa. | Nimiketapahtumat kulutetaan kirjauskansion kirjaamisen yhteydessä.                                                                                        |
| Nimiketarve  | Kirjoita nimikkeet, joita ei kuluteta välittömästi. Tämän menetelmän avulla voidaan seurata yksittäisessä nimiketarvetietueessa kulutettuja nimikemääriä.    | Nimiketapahtumat kulutetaan pakkausluettelon päivityksen yhteydessä. Toisin sanoen nimiketarve luodaan pakkausluettelon kirjaamisen yhteydessä. |
| Ostotilaukset   | Kirjoita tapahtumat yhteen kolmesta sijainnista ostomenetelmästä riippuen.                                                                              | Nimiketapahtumia kulutetaan pakkausluettelon päivityksen yhteydessä, tai asiakkaan tai toimittajan laskutuksen yhteydessä.                                      |

### <a name="process-project-invoices"></a>Projektilaskujen käsittely

Projektityyppi määrittää, mitä laskutusmenettelyä käytetään. Vain kahta ulkoista projektityyppiä (aika- ja materiaaliprojektit sekä kiinteähintaiset projektit) voidaan laskuttaa. Aika- ja materiaaliprojektit sekä kiinteähintaiset projektit liittyvät aina projektisopimukseen. 

Ennen kuin luot projektin myyntilaskun, voit luoda alustavan laskun tai laskuehdotuksen. Voit valita laskuehdotuksessa projektilaskuun sisällytettävät projektitapahtumat. Voit sitten tarkistaa laskun tiedot ennen projektilaskun kirjaamista ja lähettämistä asiakkaalle tai toiselle rahoituslähteelle. 


Lisätietoja projektilaskujen käsittelystä on kohdassa [Projektien laskutus](../accounts-payable/project-invoicing.md).


### <a name="calculate-the-cost-to-complete-a-project"></a>Projektin jäljellä olevien kustannusten laskeminen

Kun luot arvion, voit valita projektin loppuun suorittamiseen tarvittavien kustannusten laskennassa käytettävän menetelmän. Voit valita menetelmän **jäljellä olevat kustannukset**-kentästä **arvion luominen** -sivulla. Valitsemaasi menetelmää käytetään erikseen jokaisessa kustannusrivissä arvioiduissa kustannuksissa. Kun rivin tilana on **luotu**, menetelmä jota käytetään voidaan muuttaa **kustannusarvio**-sivulla. 

Seuraavassa taulukossa kuvataan laskentamenetelmät projektin jäljellä oleville kustannuksille.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tapa</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kokonaiskustannus - toteutunut</td>
<td>Arvioidut kustannukset on syötettävä manuaalisesti. Sen jälkeen kun <strong>kokonaiskustannus-</strong> tai <strong>kokonaismäärä-</strong> sarakkeet <strong>kustannusarvio-</strong>sivulla ovat valmiit, toteutuneet kustannukset vähennetään käyttäjän kirjoittamista loppusummista. Tuloksena saadaan projektin suorittamisen vaatimat kustannukset. Yleensä kustannuksien etenemistä ei jäljitetä esimerkiksi kunkin kauden kirjattujen hotellissa olojen määrällä tai kirjattujen aterioiden määrällä. Sen sijaan. Seuranta perustuu yleensä arvioitujen tuntien kokonaissumman vertailuun. Tämä menetelmä ei vaadi ennustemallia ja lopulliset kustannukset tai lopullinen määrä voidaan muuttaa manuaalisesti. Kun arvo on määritetty <strong>Kokonaiskustannus</strong>- tai <strong>Kokonaismäärä</strong>-sarakkeessa, Finance and Operations vertaa tätä arvoa varsinaisiin tapahtumiin, jotka on kirjattu kyseisellä kaudella, ja sitten arvo pienennetään <strong>Jäljellä oleva määrä</strong>- tai <strong>Jäljellä olevat kustannukset</strong> -sarakkeessa.</td>
</tr>
<tr class="even">
<td>Kokonaisbudjetti – todellinen</td>
<td>Todellisia kustannuksia verrataan ennustemalliin, jonka valitset määrittämään kustannuksia. Tässä menetelmässä käytetään kokonaisbudjettimallia, joka sisältää ennustetut tapahtumat. Saadaksesi projektiin tarkemman näkymän, voit säätää budjettimallia projektin ollessa käynnissä. Jos ennustetta on muutettava, toimi tämän yleisen prosessin mukaisesti:
<ol>
<li>Kopioi ennustetut tapahtumat toiseen ennustemalliin.</li>
<li>Vertaa ennustetapahtumia todellisiin tapahtumiin.</li>
<li>Ylläpidä, pienennä tai suurenna näitä arvioita seuraavalle kaudelle.</li>
</ol>
Finance and Operations ei vähennä ennustettuja arvioita automaattisesti. Siksi on suositeltavaa säilyttää alkuperäinen ennustemalli kiinteähintaisessa projektissa, jotta sitä voi käyttää vertailussa, kun projekti on valmis. 
<br></br> <strong>HUOMAUTUS:</strong> Kun tätä menetelmää käytetään, on käytettävä vähintään kahta ennustemallia. Alkuperäinen ennuste tulee sisältää yhteen malliin. Toista mallia varten sinun on kopioitava ennustetapahtumat toisesta mallista. Tämä kenttä on voimassa oleva vain kiinteähintaisissa projekteissa ja investointiprojekteissa.</td>
</tr>
<tr class="odd">
<td>Jäljellä oleva budjetti</td>
<td>Tässä menetelmässä käytetään jäljellä olevaa budjettimallia laskemaan projektin jäljellä olevat kustannukset. Tätä menetelmää käytettäessä toteutuneiden kustannusten ja jäljellä olevan budjettimallin ennustetut summat lasketaan yhteen. Tuloksena saadaan todelliset kustannukset. Ennen kuin käytät tätä tapaa, jäljellä oleva budjettimalli on määritettävä vähentämään tapahtumia, jotka perustuvat toteutuneisiin järjentelmään kirjattuihin tapahtumiin. <strong>Ennustemallit</strong>-sivulla, varmista että sivut on merkitty <strong>ennusteen automaattinen vähennys</strong> -ryhmään. Yleensä, jäljellä oleva budjetti kopioidaan alkuperäisestä budjetista. Kun tapahtumat syötetään, jäljellä olevan budjetin tapahtumat vähennetään. Projektin edetessä, jos toteat, että jäljellä olevaa budjettia on muutettava, ennustetapahtumat veloitetaan jäljellä olevasta budjetista. <br></br> <strong>HUOMAUTUS:</strong> Menetelmää voi käyttää vain, jos arvioon on liitetty ennustemalli.</td>
</tr>
<tr class="even">
<td>Kuten edellinen arvio</td>
<td>Käytetään samaa arviointitapaa kuin edellisessä kaudessa. Tämä menetelmä vaatii ennustemallin, jos edellinen kausi tarvitsi ennustemallin.</td>
</tr>
<tr class="odd">
<td>Määritä jäljellä olevien kustannusten arvoksi nolla</td>
<td>Tätä menetelmää käytetään tavallisesti ennen arviointiprojektin poistamista. Tämä malli vastaa yhteisarvioita, joissa ovat varsinaiset kirjatut tapahtumat, ja poistaa <strong>jäljellä olevat kustannukset</strong> -sarakkeen. Valmistumisprosentin tuloksena on aina 100 prosenttia. <strong>Ennuste</strong>-kenttää ei ole valittu jokaiselle luomallesi kustannusriville, ja kokonaisennuste kopioidaan edellisestä kustannusarviosta. Arviointikauden todellinen kulutus vähennetään projektin suorittamisessa tarvittavista jäljellä olevista kustannuksista. Tämä menetelmä ei vaadi ennustemallia.</td>
</tr>
<tr class="even">
<td>Kustannusmallin mukaan</td>
<td>Käytetään jäljellä olevien kustannusten menetelmää, joka on määritetty kustannusmallissa, joka liittyy valittuun arviointiprojektiin.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Projektin analysointi
Perustasolla, projektia käytetään ryhmittämään tapahtumat ja kirjaamaan kustannukset, ja sitten kirjaamaan nämä kustannukset kirjanpitoon. 

Yleensä nämä tapahtumat perustuvat asiakirjoihin, kuten aikaraportteihin, kuluraportteihin, toimittajalaskuihin tai varastotapahtumiin. Projektin elinkaari alkaa yleensä arvioista, ennustuksista ja budjeteista, joka auttavat suunnittelemaan ja ennakoimaan projektiin liittyvät työt ja taloudelliset vaikutukset. Kun analysoit projektin, voit arvioida ei vain sellaisia tapahtumia, jotka tapahtuivat projektin aikana, mutta myös ennusteiden sekä arvioiden paikkansapitävyyden, projektin jäsenten käyttöasteen ja yleisen onnistumisen projektin aikana.

### <a name="analyze-cash-flow"></a>Anaysoi kassavirta

Kassavirran seurantatoiminnon avulla voit tarkistaa sekä projektin ennustetun että todellisen kassavirran. Kassavirran voi tarkistaa, kun projekti on meneillään, mutta myös päättyneen projektin kassavirtaa voi tarkastella. 

Kassavirtoja valvomalla voidaan arvioida yksittäisiä projekteja, käyttää raportteja useiden projektien tarkasteluun ja siirtää projektin kassavirtoja kirjanpidon kassavirtaennusteisiin.

#### <a name="cash-inflow-forecasting"></a>Kassavirtauksen ennustaminen

Voit ennustaakassavirtaukset valitulle projektille asetustesi mukaisesti. Esimerkiksi, jos projektipäivämäärä on 5. maaliskuuta 2012 ja laskutat 31. maaliskuuta 2012, näin voit ennustaa eräpäivän ja odotetun myynnin maksupäivän:

-   **Projektin päivämäärä:** 5. maaliskuuta 2012.
-   **Laskutuspäivämäärä** 31. maaliskuuta 2012. Tämä päivämäärä määräytyy laskutusvälin mukaan. Tässä esimerkissä määrität laskutusvälin nykyiselle kuukaudelle. Joten kaikki maaliskuun aikana kirjatut tapahtumat laskutetaan kuukauden viimeisenä päivänä.
-   **Eräpäivä:** 14.4.2012. Tämä päivämäärä määritetään maksuehdoissa, jotka on määritetty projektin mukaan. Tässä esimerkissä olet valinnut maksuehdoiksi 14 vuorokautta. Joten 14 päivää lisätään laskutuspäivämäärään, jotka lisätään eräpäivänä 14. huhtikuuta 2012.
-   **Odotettu myynnin maksupäivä:** 27.4.2012. Tämä päivämäärä lasketaan lisäämällä päivien lukumäärä **Yleiset puskuripäivät** -kentässä **Projektin hallinnan ja kirjanpidon parametrit** -sivulla päivien lukumäärään **Yksittäiset puskuripäivät** -kentässä **Projektisopimukset**-sivulla ja lisäämällä sitten kokonaissumma päivien lukumäärään **Määräpäivä**-kentässä. Tässä esimerkissä syötit numeron **3** **yleiset puskuripäivät** -kenttään ja **10** **yksittäiset puskuripäivät** -kenttään. Joten 13 päivää lisätään eräpäivään, jotka lisätään odotettuna myynnin maksupäivänä 27. huhtikuuta 2012.

Yleiset puskuripäivät voivat korvata joko yksittäiset puskuripäivät tai ne voidaan lisätä yksittäisiin puskuripäiviin:

-   Käyttääksesi yleisiä puskuripäiviä korvaamaan yksittäisiä puskuripäiviä, syötä eräpäivän ja todellisen asiakkaiden maksupäivän välillä oleva keskimääräinen päivien lukumäärä.
-   Lisätäksesi yleiset puskuripäivät yksittäisiin puskuripäiviin **yleiset puskuripäivät** -kentässä, syötä haluamasi arvio päivien lukumäärästä sillä välillä, jona asiakas lähettää maksun ja jona organisaatiosi saa maksun.

Projektisopimuksen mukainen yksittäisten puskuripäivien asettaminen. Päivämäärät lasketaan sekä myynnin eräpäivän perusteella että sen perusteella, mitä organisaatiosi tietää asiakkaan maksutottumuksista.

#### <a name="actual-cash-inflow"></a>Todellinen kassavirta

Todellinen kassavirta sisään on hyvin samankaltainen kuin ennustettu kassavirta, mutta laskutoimitukset voidaan aloittaa ensimmäisestä laskun päivämäärästä. Tässä on esimerkki:

-   **Laskutuspäivämäärä** 2. maaliskuuta 2012.
-   **Eräpäivä:** 16.3.2012. Maksuehdoksi määritetään 14 päivää.
-   **Odotettu myynnin maksupäivä:** 29.3.2012. Laskentaan sisältyy kolme yleistä puskuripäivää ja 10 yksittäistä puskuripäivää.

#### <a name="cost-forecasting"></a>Kustannusennusteiden tekeminen

Määriteltyjen päivien mukaan kustannuksien maksupäivä voi olla eri kuin projektipäivämäärä. Tällöin kustannusten maksupäivä lasketaan lisäämällä päivien lukumäärä projektipäiväyksestä päivien lukumäärään maksuehdoissa. 

Esimerkiksi, tapahtuman projektipäivämäärä on 5. maaliskuuta 2012 ja seuraavat maksuehdot on määritetty:

-   **Tunnit:** Kuluva kuukausi (**M**)
-   **Kulut:** 14 päivää (**D14**)
-   **Nimikkeet:** 30 päivää (**D30**)

Tässä on kustannusten maksupäivä kullekin tapahtumatyypille näiden asetusten perusteella:

-   **Tunnit:** 31. maaliskuuta 2012, joka on valitun kuukauden viimeinen päivä.
-   **Kulut:** 19. maaliskuuta 2012, joka on 14 päivää tapahtuman päivämäärän jälkeen.
-   **Kulut:** 4. huhtikuuta 2012, joka on 30 päivää tapahtuman päivämäärän jälkeen.

> [!NOTE] 
> Ostotilauksen päivämäärä perustuu toimittajatapahtumaan, kun projektin ostotilaus luodaan. Eräpäivää ei määrää mikään oletusasetus. 

Kustannusten maksupäivä ei ole laskettu puskuripäiville. Kun projekti on valmis ja kun kaikki kustannuslaskennat ja laskutukset on tehty, sekä kustannukset että myynti kirjataan tuottotileille. 

Kun kaikki myynti- ja toimittajalaskut ovat valmiita, voit tarkastella kenttien välistä suhdetta **kassavirta**-sivulla ja kentillä **projektin tiliotteet** -sivulla.

:::row:::
    :::column:::
        #### Cash flow page
        - Cash inflows 
        - Cash outflows
        - Net cash flows
    :::column-end:::
    :::column:::
        #### Project statements page
        - Revenue
        - Total cost
        - Gross margin
    :::column-end:::
:::row-end:::

### <a name="review-costs"></a>Tarkista kustannukset

Voit valvoa organisaatiollesi projektin aikana aiheutuvia kustannuksia **kustannusseuranta**-sivulla. Vertaamalla alkuperäisiä projektin budjetoituja kustannuksia projektin nykyisiin toteutuneisiin kustannuksiin ja sidottuihin kustannuksiin voidaan määrittää, onko projekti aikataulussa, meneenkö se budjetin yli tai ali. 

> [!NOTE] 
> Käytettäessä **Kustannusseuranta**-sivua tarkastellaksesi projektikustannuksien nykyistä tilaa, käytä ennustemalleja, jotka valittiin alkuperäiselle sekä jäljellä olevalle budjetille. Jos valitset muita ennustemalleja, kun lasket kustannuksia, laskennan tulokset eivät ole tarkkoja.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Jäljellä olevien budjetoitujen summien tarkasteleminen

Jos **jäljellä oleva budjetti** on valittu kustannuksien hallintamenetelmäksi **projektin hallinta ja kirjanpidon parametrit** -sivulla **kustannusseuranta**-sivu laskee kustannukset, joita ei ole kirjattu toteutuneiksi tai merkitty sidotuiksi. Erityisesti, summat **yleiset**-välilehdessä, alemmassa ruudussa **kustannusseuranta**-sivulla, lasketaan seuraavasti:

-   **Todelliset kustannukset** – kokonaissumma, joka on kulunut valitun kustannusrivin projektiin. Toteutunut kustannussumma lasketaan **kirjanpitopäivitykset**-sivulla.
-   **Sidottu kustannus** – muiden kulujen summa, jonka yritys on sitoutunut maksamaan. Erityiset sidotut kustannukset lasketaan **sidotut kustannukset**-sivulla.
-   **Jäljellä oleva budjetti** – alkuperäisen budjetin summa, joka on yhä käytettävissä valitulla kustannusrivillä. Jäljellä oleva budjettisumma lasketaan **kirjanpidon esikatselu** -sivulla.
-   **Kokonaiskustannussumma** – on toteutuneiden kustannusten, sidottujen kustannusten ja jäljellä olevan budjetin summa.

**Budjetin hallinta** -sivulla, **poikkeama**-välilehdessä voit vertailla odotettua kokonaiskustannusta ja alkuperäistä budjettia. Tässä vertailussa näkyvät kaikki summien väliset erot. Näin näet, kun tiedot eivät vastaa. Poikkeamasummat lasketaan seuraavasti:

-   **Alkuperäinen budjetti** – summa, joka on alun perin budjetoitu valitulle kustannusriville. Alkuperäinen budjettisumma lasketaan **kirjanpidon esikatselu** -sivulla.
-   **Kokonaiskustannus** – toteutuneiden kustannusten, sidottujen kustannusten ja jäljellä olevan budjetin summa, kuten **yleinen**-välilehdessä on raportoitu .
-   **Poikkeama**– kokonaiskustannusten ja alkuperäisten budjetoitujen kustannusten ero.
-   **Määrään perustuva varianssi** – alkuperäisen ennusteen ja kokonaisennusteen summien ero yhteensä. Ero voidaan ilmaista matemaattisesti seuraavasti (ennusteen kokonaismäärä) × (alkuperäinen keskimääräinen hinta - keskimääräinen hinta yhteensä). Tämä laskutoimitus koskee vain projektitunteja.
-   **Hintaan perustuva varianssi** – alkuperäisen ennusteen ja kokonaisennusteen summien ero yhteensä. Ero voidaan ilmaista matemaattisesti seuraavasti (alkuperäinen ennusteen hinta) × (alkuperäinen ennusteen määrä – ennusteen kokonaismäärä). Tämä laskutoimitus koskee vain projektitunteja.

#### <a name="viewing-the-total-budgeted-amounts"></a>Budjetoitujen kokonaissummien tarkasteleminen

Jos **kokonaisbudjetti** on valittu kustannuksien hallintamenetelmäksi **projektin hallinnan ja kirjanpidon parametrit** -sivulla **kustannusseuranta** -sivu laskee projektin todelliset kustannukset ja kokonaiskustannukset, jotta voit määrittää näiden kahden väliset erot. Erityisesti, **Budjetin hallinta**-sivulla, summat alemman ruudun sarakkeissa **yleistä**-välilehdessä, lasketaan seuraavasti:

-   **Budjetoidut kustannukset yhteensä** – valitun kustannusrivin budjetoitu kokonaissumma.
-   **Todelliset kustannukset** – kustannusten kokonaissumma, joka on aiheutunut projektissa valituille kustannusriveille.
-   **Sidotut kustannukset** – kokonaissumma, joka on sidottu valittuun kustannusriviin.
-   **Varianssi** – todellisten ja sidottujen kustannusten summan ero ja kokonaiskustannukset. Varianssista ilmenee tarvitseeko lisäkustannuksia eritellä kokonaisbudjettia varten.

**Kustannusseuranta**-sivulla, **poikkeama**-välilehdessä voit tarkastella kokonaisbudjetin ja alkuperäisen budjetin välistä eroa tarkastelemalla seuraavia kenttiä:

-   **Alkuperäinen budjetti** – summa, joka on alun perin budjetoitu valitulle kustannusriville. Alkuperäinen budjetti on laskettu **kirjanpidon esikatselu** -sivulla.
-   **Kokonaisbudjettikustannukset** – kokonaissumma, joka on alun perin budjetoitu kustannusriville. Kokonaisbudjettikustannukset on laskettu **kirjanpidon esikatselu** -sivulla.
-   **Poikkeama** – kustannusrivin poikkeama. Tämä summa lasketaan vähentämällä kokonaiskustannus alkuperäisestä budjetista.
-   **Määrään perustuva varianssi** – alkuperäisen budjetin ja kokonaisbudjetin summien ero yhteensä. Tämä summa lasketaan vähentämällä kaikki budjetoidut tunnit alkuperäisistä budjetoiduista tunneista ja kertomalla erotus alkuperäisellä budjetoidulla kustannushinnalla. Tämä erotus voidaan ilmaista matemaattisesti (alkuperäinen budjetoitu kustannushinta) × (alkuperäiset budjetoidut tunnit – kaikki budjetoidut tunnit). Tämä laskutoimitus koskee vain projektitunteja.
-   **Hintaan perustuva varianssi** – Tämä summa lasketaan vähentämällä kaikki budjetoidut tunnit alkuperäisistä budjetoiduista tunneista ja kertomalla erotus kulutettujen tuntien kokonaismäärällä. Tämä erotus voidaan ilmaista matemaattisesti (kaikki budjetoidut tunnit) × (alkuperäiset budjetoidut tunnit – kaikki budjetoidut tunnit). Tämä laskutoimitus koskee vain projektitunteja.

### <a name="analyze-utilization"></a>Analysoi käyttö

Käyttöaste on sen ajan prosenttiosuus, jolloin työntekijä tekee laskutettavaa tai tuottavaa työtä tietyllä kaudella. Laskutettavat tunnit ovat työntekijän tunnit, joka veloitetaan tietylle asiakkaalle. 

Työntekijän käyttöaste lasketaan jakamalla laskutettavat tunnit tietyltä kaudelta työtuntien määrällä. Esimerkiksi, jos työntekijällä on 30 laskutettavaa tuntia kaudessa ja työtuntien määrä samassa ajassa on 40, työntekijän käyttöaste on 75 prosenttia. 

Kun lasket työntekijän käyttöasteen, voit laskea joko laskutusasteen tai tehokkuusasteen mukaan:

-   **Laskutusaste** – laskutettavien ja ei-laskutettavien tuntien tai normaalituntien välinen ero.
-   **Tehokkuusaste** – tuottavien ja ei-tuottavien tuntien tai normaalituntien välinen ero. Tuottavat tunnit ovat tunteja, jotka työntekijä käyttää avustaessaan tiettyä projektia. Tuottavat tunnit yleensä veloitetaan asiakkaille, paitsi silloin kun on kyse sisäisistä projekteista. Ei-tuottavia tunteja ei koskaan veloiteta asiakkaalle.

Laske käyttöaste **tuntien käyttö** -sivulla. Laskelmat perustuvat oletusasetuksiin. Nämä asetukset myös määrittävät, miten tunnit lasketaan osoittamalla **"käyttö"** tai **"kuormitus"** kullekin projektityypille. Tämä koskee laskutusaste laskelmia ja tehokkuusaste laskelmia.

-   **Käyttö** – ne tunnit, jotka on ilmoitettu valitulle projektityypille katsotaan aina laskutus- tai tehokkuuskäyttöön.
-   **Kuormitus** – ne tunnit, jotka on ilmoitettu valitulle projektityypille katsotaan aina ei-laskutus- tai ei-tehokkuuskäyttöön.
-   **Rivin ominaisuuden mukaan** – tietyn tuntitapahtuman rivin ominaisuudet määrittävät pidetäänkö tunteja laskutettavina vai tehokkuuskäyttöön.
-   **Ei sisälly** – tunteja ei sisällytetä laskutus- tai tehokkuuskäyttöön.

**Tuntien käyttö** -sivulla, työntekijän tai projektin yleisen käyttöasteen vieressä, voit nähdä kuinka monta tuntia on käytetty käyttöastelaskutoimituksiin jokaiselle seuraavista tuntityypeistä:

-   **Tunnit joita ei sisällytetä** – nämä tunnit eivät sisälly tuntien käyttöasteeseen.
-   **Sisälletyt tunnit** – nämä tunnit lasketaan lisäämällä käyttötunnit ja kuormitustunnit yhteen. Nämä tunnit lisätään käyttöasteeseen.
-   **Kuormitustunnit** – jos lasket laskutettavaa määrää, nämä tunnit ovat samat kuin ei-laskutettavat tunnit. Jos lasket tehokkuusarvoa, nämä tunnit ovat samat kuin tuottamattomat tunnit.
-   **Käyttötunnit** – jos lasket laskutettavaa määrää, nämä tunnit ovat samat kuin laskutettavat tunnit. Jos lasket tehokkuusarvoa, nämä tunnit ovat samat kuin tuottavat tunnit.

Kun lasket työntekijän käyttöastetta, voit käyttää normaalitunteja tai sisällytettyjä tunteja. Käytettäessäsi sisällytettyjä tunteja varmista, että työntekijät kirjaavat kaiken heidän käyttämänsä ajan tuntilomakkeen ajanjaksoihin, sillä laskenta näkyy kirjattujen tuntien prosenttiosuutena. Kun lasket tuntien käyttöastetta projektiin, projektisopimukseen, asiakastietueeseen tai luokkaan, sinun tulee käyttää sisällytettyjä tunteja laskentaan.

### <a name="review-project-statements"></a>Tarkastele projektilaskelmia

Voit luoda projektilaskelman tarkastellaksesi nopeasti projektin tilaa. Kun suoritat projektilaskelman, voit määrittää valitsemasi kriteerit, joita käytetään laskelman luomisessa, tekemällä valintoja **yleiset**-välilehden **projektilaskelmat**-sivulla. Voit valita lisäätkö vai poistatko seuraavat tiedot:

-   Projektityypit
-   Tapahtumatyypit
-   Projektin päivämäärä / kirjanpitopäivämäärä
-   Tiedot

Kun laskelma lasketaan, voit tarkastella eri välilehdissä seuraavat tiedot **projektilaskelmat**-sivulla:

-   **Yleinen** – yleisiä tietoja projektin voittojen ja tappioiden perusrakenteesta.
-   **Voitot ja tappiot** – jaksotetun tuoton tietoja.
-   **KET** – tietoja KET-tilien saldoista.
-   **Kulutus** tietoa tuntien käytöstä, nimikkeistä, kuluista ja palkanlaskentatapahtumista.
-   **Lasku** – tietoja laskuista ja ennakkolaskutuksesta.
-   **Tuntihinta** – tuotto- ja kustannustileille kirjattujen tuntien tuntihinnat.
