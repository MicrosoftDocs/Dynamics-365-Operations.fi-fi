---
title: Yleiskatsaus budjetin seurantaan
description: Tässä artikkelissa esitellään budjetin hallinta. Artikkeli sisältää tietoja, joiden avulla budjetin hallinta voidaan määrittää Microsoft Dynamics 365 for Finance and Operationsissa niin, että taloushallinnon resurssien hallinta onnistuu.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 60493
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b33057bc28c1a03cb7c72e369beec4a78ff2d1a1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834292"
---
# <a name="budget-control-overview"></a>Budjetin hallinnan yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa esitellään budjetin hallinta. Artikkeli sisältää tietoja, joiden avulla budjetin hallinta voidaan määrittää Microsoft Dynamics 365 for Finance and Operationsissa niin, että taloushallinnon resurssien hallinta onnistuu.

<a name="overview"></a>Yleiskuvaus
--------

Microsoft Dynamics 365 for Finance and Operationsin budjetin hallinta tukee organisaation taloudellisten resurssien hallintaa tilikarttojen, työnkulkujen, työryhmien, lähdeasiakirjojen ja -kirjauskansioiden sekä käytettävissä olevien varojen määritettävissä olevan laskelman, budjettijaksojen ja raja-arvojen avulla. Kun ohjausobjektit on määritetty, organisaatio voi suunnitella, mitata, hallita ja ennustaa taloudellisia resursseja tilikauden aikana. 

Kun budjetit on hyväksytty Finance and Operationsissa, voit luoda budjettirekisterimerkinnät budjettisuunnitelmien avulla ja tallentaa organisaation kulubudjetin. Vaihtoehtoisesti budjettirekisterimerkinnät voidaan luoda tai tuoda kolmannen osapuolen ohjelman avulla ilman budjettisuunnittelutoiminnon käyttämistä. 

Kulut voidaan tallentaa päätilien ja taloushallinnon dimensioiden avulla. Koko kulubudjetin hallinta voidaan määrittää vastaamaan organisaation menetelmiä ja vaatimuksia taloushallinnon dimensioiden ja päätilien yhdistelmien ryhmittelyn avulla. 

Seuraavassa kaaviossa esitellään budjetin hallinnan sijainti tavallisen budjettijakson vaiheissa.

[![BudgetingCycle](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Voit määrittää budjetin hallinnan useiden eri tekijöiden perusteella:

-   **Taloushallinnon dimensiot** – Mitä taloushallinnan dimensioita budjetin ja toteutuneiden arvojen raportoinnissa? Mitä taloushallinnan dimensioita budjetin hallinnassa on käytettävä? Vaativatko tietyt dimensioyhdistelmät tai päätilit erityishuomiota? Onko budjetin ja toteutuneiden arvojen seuraaminen kustannuspaikan ja ohjelman perusteella pakollista? Vaativatko matkakulut erityishuomiota?
-   **Aika** – Millaista ajanjaksoa (tilikausi, tilikausi tähän päivään saakka jne.) käytettävissä olevien budjettivarojen arvioinnissa käytetään?
-   **Lähdeasiakirjat** – Mitkä lähdeasiakirjat on arvioitava budjetin hallinnassa? Onko asiakirjat arvioitava rivikohtaisesti vai asiakirjakohtaisesti?
-   **Käytettävissä olevien varojen laskelma** – Otetaanko asiakirjat, kuten ostoehdotukset (alustavat varaukset) ja ostotilaukset (varaukset) huomioon käytettävissä olevien varojen laskelmassa? Otetaanko luonnostilaiset asiakirjat huomioon laskelmassa?
-   **Ohita käyttöoikeus** – Kuka voi ylittää käytettävissä olevan budjetin?

Budjetin hallinta on integroitu täysin Finance and Operationsin kanssa. Tämän vuoksi sekä suunniteltujen että toteutuneiden ostojen budjetin arviointi on mahdollista. Budjettikyselyt ja -raportit ovat käytettävissä. Tämän vuoksi käyttäjät voivat arvioida budjettia koko budjettijakson aikana ja tehdä tarvittaessa oikaisuja budjetin versioiden ja siirtojen muodossa. Budjettipäällikkö voi myös viedä budjetin ja toteutuneet arvot Microsoft Exceliin, jossa voidaan suorittaa paremmat analyysit ja ennusteet.

## <a name="configuring-budget-control"></a>Budjetin hallinnan konfiguroiminen
### <a name="budget-cycle-time-span"></a>Budjettijakson aikaväli

Kun perusbudjetointi on konfiguroitu, voit määrittää budjetoinnin ja budjetin hallinnan ajan tai aloitus- ja lopetuskauden **Budjettijakson aikaväli** -sivulla. Budjettijaksot vastaavat usein kirjanpidon vuosikalentereita, mutta ne voivat ulottua myös tilikausille.

Konfiguraation seuraavat vaiheet suoritetaan **Budjetin hallinnan konfiguraatio** -sivun eri välilehdissä.

### <a name="define-parameters"></a>Määritä parametrit

Budjetin hallinnassa voidaan käyttää käytössä olevista budjetin taloushallinnon dimensioista riippuen kaikkia taloushallinnon dimensioita tai niiden osajoukkoa. 

Vaihtoehtoisesti voit määrittää oletusaikavälin (esimerkiksi **Tilikausi**, **Tilikausi pvm asti**, **Tilikausi** tai **Neljännesvuosittain**) jonka mukaan budjetin hallinta suoritetaan liittyvälle budjettijakson aikavälille. Voit määrittää myös oletusbudjettipäällikön ja raja-arvon, jonka mukaan käyttäjille lähetetään ilmoitus raja-arvon saavuttamisesta. Näiden kenttien arvoja käytetään oletusarvoina uusissa budjettien hallintasäännöissä tai budjettiryhmissä, joita luodaan. Yksittäisten ryhmien tai sääntöjen oletusarvoja voidaan kuitenkin muuttaa. 

Budjettirekisterin budjettien luonti- ja tallennustavat auttavat määrittämään aikavälin, joka valitaan käytettävissä olevien budjettivarojen arvioinnin yhteydessä. Jos käytössä on dimension arvojen yhdistelmän vuosittainen summa, kannattaa ehkä käyttää tilikautta tai tilikautta tähän päivään saakka. Jos organisaatiossa, jossa luodaan budjetti tilikauden mukaan tai kohdistus tehdään tilikausille, halutaan yksityiskohtaisempaa hallintaa, aikaväliksi kannattaa harkita tilikautta tähän päivään saakka tai neljännesvuotta. 

Myös organisaation maa-/alueasetukset kannattaa ottaa huomioon, koska ne vaikuttavat budjetointiin ja budjetin hallintaan. Ne myös auttavat konfiguraation määrittämisessä.

### <a name="over-budget-permissions"></a>Budjetin ylitysoikeudet

Seuraavaksi määritetään käyttäjäryhmät **Budjetin ylitysoikeudet** -välilehdessä. Voit määrittää myös, onko käyttäjillä, jotka ovat ryhmän jäseniä, oikeus ylittää budjetti. Voit estää käyttäjiä ylittämästä **Budjettiparametrit**-sivulla määritettyä budjetin raja-arvoa tai voit estää käyttäjiä ylittämästä budjettia millään summalla raja-arvosta huolimatta. Nämä käyttöoikeudet voiva auttaa organisaation taloushallinnon resurssien hallinnassa, jos organisaatiossa hallitaan kulutusta ennakoivasti. 

### <a name="budget-funds-available"></a>Käytettävissä olevat budjettivarat

**Käytettävissä olevat budjettivarat** -välilehdessä voit määrittää seuraavaksi kaavan, jota käytetään käytettävissä olevien budjettivarojen laskennassa. Laskelma voi sisältää luonnoksia tai kirjaamattomia asiakirjoja riippuen siitä, miten konservatiivisesti organisaatiossa hallitaan taloushallinnon resursseja tai millaiset säädökset tai toimialan vaatimukset ovat. 

> [!NOTE] 
> Jos tätä laskelmaa muokataan budjettijakson aikana, muutokset eivät vaikuta budjetin hallinnan tarkistuksissa hyväksyttyihin tai aiemmin kirjattuihin tai valmistuneisiin asiakirjoihin.

### <a name="documents-and-journals"></a>Tiedostot ja kirjauskansiot

Seuraavaksi valitaan **Tiedostot ja kirjauskansiot** -välilehdessä budjetin hallinnan tarkistuksiin mukaan otettavat lähdeasiakirjat ja -kirjauskansiot ja se, tehdäänkö tarkistus rivimerkinnän tasolla vai asiakirjalle kokonaisuutena. 

Sinun tulisi täsmätä valitut lähdeasiakirjat niiden saldojen valintaruutujen kanssa, jotka on valittu käytössä olevien budjettivarojen laskelmaan. Jos valittuna on esimerkiksi **Varausten budjettivaraukset**, valittava asetus on **Ostotilaukset**. Kun budjetin tarkistus suoritetaan ostorivin summille ja tileille, varaukseen määritetty budjetin hallinnan luokka on **Varaus** Kun budjetin tarkistus suoritetaan ostoehdotuksen summille ja tileille, varaukseen määritetty budjetin hallinnan luokka on **Alustava varaus** 

Jos **Varausten budjettivaraukset** ja/tai **Alustavien varausten budjettivaraukset** sisällytetään käytettävissä olevien budjettivarojen laskelmaan ja jos niiden on muututtava kirjanpidon kirjausten mukaisesti, sitoumuksiin perustuva kirjanpito on otettava käyttöön **Kirjanpitoparametrit**-sivulla.  

### <a name="assign-budget-models"></a>Määritä budjettimallit

Seuraavaksi liitetään budjetin hallintaan sisällytettävät budjettimallit budjettijakson aikaväleihin **Liitä budjettimallit** -välilehdessä.

### <a name="define-budget-control-rules"></a>Määritä budjetin hallintasäännöt

Seuraavaksi luodaan tietyt säännöt **Määritä budjetin hallintasäännöt** -välilehdessä budjetin hallinnan käytössä olevien taloushallinnan dimensioiden perusteella. Jos kohdistus tehdään esimerkiksi osaston menon tai menovälin perusteella, menot voidaan määrittää ja arvioida tämän välilehden asetusten avulla. Voit määrittää kullekin budjetin hallintasäännölle eri raja-arvot. 

> [!Important]
> Budjetin hallinta voidaan ottaa käyttöön mille tahansa **Voitto ja tappio**-, **Meno**-, **Tuotto-, Tase-, Velat-, Oma pääoma-** tai **Käyttöomaisuus**-tyypin päätilille. Jos tämä välilehti sisältää säännön, jonka ehdot ovat tyhjät, budjetin hallinta otetaan käyttöön **kaikille** taloushallinnon dimension yhdistelmille, jotka sisältävät tämän tyyppisen päätilin. Tämän vuoksi on tärkeää luoda budjetin hallinnan säännöt, joissa määritetään taloushallinnon dimensioiden yhdistelmien arvovälit vain silloin, kun budjetin hallinnan käyttäminen on tärkeää.  

### <a name="select-main-accounts"></a>Valitse päätilit

Jos **päätiliä** ei ole valittu budjetin hallinnan dimensioksi **Määritä parametrit** -sivulla, mutta tiettyjä menoja hallitaan, nämä menot voidaan valita **Valitse päätilit** -välilehdessä. Jos **päätili** on valittu budjetin hallinnan dimensioksi, merkinnät eivät ole pakollisia.  

### <a name="define-budget-groups"></a>Määritä budjettiryhmät

Seuraavaksi voidaan valita tarvittaessa **Määritä budjettiryhmät** -välilehdessä niiden taloushallinnon dimensioiden yksilöivät yhdistelmät, joissa budjettiresurssit on ryhmitelty toissijaista budjettitarkistusta varten. Voit luoda yhden koko organisaation sisältävän tietueen tai määrittää useita yksittäisiä osastoja tai kustannuspaikkoja edustavia ryhmiä.  

### <a name="define-message-levels"></a>Määritä sanomatasot

Jos budjetin hallinnan varoitussanomat tulee piilottaa joiltakin käyttäjäryhmiltä, voit määrittää ryhmät **Määritä sanomatasot** -sivulla. Käyttäjäryhmien jäsenet saavat edelleen virheilmoituksia, kun käytettävissä olevat budjettivaroja ylitetään budjetin ylityksen oikeuksien perusteella.

### <a name="activate-budget-control"></a>Ota budjetin hallinta käyttöön

Kun budjetin hallinta on määritetty, voit ottaa hallinnan käyttöön ja aktivoida sen **Ota budjetin hallinta käyttöön** -välilehdessä. Luonnosversio tulee tämän jälkeen voimaan.
> [!Important]
> Kun budjetin hallinta on otettu käyttöön ja aktiivinen ja tapahtumia on kirjattu, hallintaa ei voi poistaa käytöstä kesken vuoden. Kun budjetin hallinta poistetaan käytöstä, tehtäviä ei tallenneta budjetin hallintaa varten eikä budjettitarkastuksia enää suoriteta. Tämän vuoksi aiemmin kirjatut asiakirjat eivät ehkä vastaa budjetin hallintaan liittyvien kyselyjen ja raporttien vapautussanomia tai -saldoja. Näitä ovat budjetin hallinnan tilastot missä tahansa tuotantovirrassa tai asiakirjojen ja kirjauskansioiden oikaisu. 

Huomaa myös, että ennen budjetin hallinnan käyttöönottoa kirjattuja tapahtumia, kuten budjettirekisterimerkintöjä, ei oteta huomioon budjetin hallinnassa. Tämän vuoksi on suositeltavaa ottaa budjetin hallinta käyttöön vain uuden budjettijakson alkaessa. Varmista, että budjettirekisterimerkinnät, jotka sisältävät budjetin hallinnan budjetin alkusaldoja, saavat päivitetyt budjettisaldot vasta sen jälkeen, kun budjetin hallinta on otettu käyttöön. Kaikki avoimen asiakirjan (esimerkiksi ostotilaus) käytettävissä olevat budjettivarat tarkistetaan. Se saa budjetin hallinnan budjettivarauksen, kun käyttäjä käynnistää asiakirjassa manuaalisesti budjetin hallinnan tarkistuksen.

## <a name="using-budget-control"></a>Budjetin hallinnan käyttäminen
Kun budjetin hallinta on otettu käyttöön, käyttäjät vastaanottavat niiden asiakirjojen ja kirjauskansioiden budjetin hallinnan varoituksia ja virhesanomia, joille on konfiguroitu budjetin hallinta. Muista, että voit määrittää budjetin hallinnan niin, että vaikka käyttäjille lähetetään varoitus budjetin varojen ylittämisestä, he voivat silti jatkaa tapahtumien vahvistamista tai kirjaamista. Käyttäjät voivat tarkastella epäonnistuneiden budjettitarkistusten tietoja **Budjetin hallinnan virheet ja varoitukset** -sivulla.   

Tältä sivulta käyttäjät voivat porautua **Budjetin hallinnan tilasto kausittain** -sivulle ja tarkastella budjetin käytettävyystietoja ja varauksia tietyn budjetin ohjausdimensioyhdistelmän osalta. Käyttäjät voivat porautua myös **Budjetin hallinnan tilastot**-sivulle ja tarkastella budjetin käytettävyyttä kaikkien budjetin hallinnassa käytettävien taloushallinnon dimensioiden yhdistelmien osalta. 

Jos budjetin hallinta on otettu käyttöön ostotilauksille, budjettipäällikkö voi tarkastella **Kirjanpitobudjetit ja ennusteet** -työtilan avulla kaikkien niiden vahvistamattomien ostotilausten jonoa, joilla on budjetin tarkistuksen varoituksia ja virheitä. Jos budjettipäällikölle on konfiguroitu budjetin ylitysoikeudet, hän voi vahvistaa ostotilaukset suoraan työtilassa.    
