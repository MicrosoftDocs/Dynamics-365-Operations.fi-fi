---
title: Yleiskatsaus budjetin seurantaan
description: Tässä artikkelissa esitellään budjetin hallintatoiminto ja tietoja, joiden avulla voit määrittää budjetin hallinnan organisaation taloudellisten resurssien hallinnan optimoimiseksi.
author: panolte
ms.date: 03/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27eb31919937e7f43a785616b547e3d6952eaaf2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898295"
---
# <a name="budget-control-overview"></a>Yleiskatsaus budjetin seurantaan

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa esitellään budjetin hallintatoiminto ja tietoja, joiden avulla voit määrittää budjetin hallinnan organisaation taloudellisten resurssien hallinnan optimoimiseksi.

Budjetin hallinta tukee organisaation taloudellisten resurssien hallintaa tilikarttojen, työnkulkujen, työryhmien, lähdeasiakirjojen ja -kirjauskansioiden sekä käytettävissä olevien varojen määritettävissä olevan laskelman, budjettijaksojen ja raja-arvojen avulla. Kun ohjausobjektit on määritetty, organisaatio voi suunnitella, mitata, hallita ja ennustaa taloudellisia resursseja tilikauden aikana. 

Kun budjetit on hyväksytty järjestelmässä, voit luoda budjettirekisterimerkinnät budjettisuunnitelmien avulla ja tallentaa organisaation kulubudjetin. Vaihtoehtoisesti budjettirekisterimerkinnät voidaan luoda tai tuoda kolmannen osapuolen ohjelman avulla ilman budjettisuunnittelutoiminnon käyttämistä. 

Kulut voidaan tallentaa päätilien ja taloushallinnon dimensioiden avulla. Koko kulubudjetin hallinta voidaan määrittää vastaamaan organisaation menetelmiä ja vaatimuksia taloushallinnon dimensioiden ja päätilien yhdistelmien ryhmittelyn avulla. 

Seuraavassa kaaviossa esitellään budjetin hallinnan sijainti tavallisen budjettijakson vaiheissa.

[![Tyypillinen budjetointijakso.](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Voit määrittää budjetin hallinnan useiden eri tekijöiden perusteella:

- **Taloushallinnon dimensiot** – Mitä taloushallinnan dimensioita on käytettävä budjetin ja toteutuneiden arvojen raportoinnissa ja mitä taloushallinnon dimensioita vaaditaan budjettien hallintaan? Vaativatko tietyt dimensioyhdistelmät tai päätilit erityishuomiota? Onko budjetin ja toteutuneiden arvojen seuraaminen kustannuspaikan ja ohjelman perusteella pakollista? Vaativatko matkakulut erityishuomiota?
- **Aika** – Millaista ajanjaksoa (tilikausi, tilikausi tähän päivään saakka jne.) käytettävissä olevien budjettivarojen arvioinnissa käytetään?
- **Lähdeasiakirjat** – Mitkä lähdeasiakirjat on arvioitava budjetin hallinnassa? Onko asiakirjat arvioitava rivikohtaisesti vai asiakirjakohtaisesti?
- **Käytettävissä olevien varojen laskelma** – Otetaanko asiakirjat, kuten ostoehdotukset (alustavat varaukset) ja ostotilaukset (varaukset) huomioon käytettävissä olevien varojen laskelmassa? Otetaanko luonnostilaiset asiakirjat huomioon laskelmassa?
- **Ohita käyttöoikeus** – Kuka voi ylittää käytettävissä olevan budjetin?

Budjetin seuranta on täysin integroitu sovellukseen. Tämän vuoksi sekä suunniteltujen että toteutuneiden ostojen budjetin arviointi on mahdollista. Budjettikyselyt ja -raportit ovat käytettävissä. Tämän vuoksi käyttäjät voivat arvioida budjettia koko budjettijakson aikana ja tehdä tarvittaessa oikaisuja budjetin versioiden ja siirtojen muodossa. Budjettipäällikkö voi myös viedä budjetin ja toteutuneet arvot Microsoft Exceliin, jossa voidaan suorittaa paremmat analyysit ja ennusteet.

## <a name="configuring-budget-control"></a>Budjetin hallinnan konfiguroiminen

### <a name="budget-cycle-time-span"></a>Budjettijakson aikaväli

Kun perusbudjetointi on konfiguroitu, voit määrittää budjetoinnin ja budjetin hallinnan ajan tai aloitus- ja lopetuskauden **Budjettijakson aikaväli** -sivulla. Budjettijaksot vastaavat usein kirjanpidon vuosikalentereita, mutta ne voivat ulottua myös tilikausille.

Määrityksen seuraavat vaiheet suoritetaan **Budjetin hallinnan määritys** -sivulta avatuissa välilehdissä.

### <a name="define-parameters"></a>Määritä parametrit

Budjetin hallinnassa voidaan käyttää käytössä olevista budjetin taloushallinnon dimensioista riippuen kaikkia taloushallinnon dimensioita tai niiden osajoukkoa. 

Vaihtoehtoisesti voit määrittää oletusaikavälin (esimerkiksi **Tilivuosi**, **Tilikausi pvm asti**, **Tilikausi** tai **Neljännesvuosittain**) jonka mukaan budjetin hallinta suoritetaan liittyvälle budjettijakson aikavälille. Voit määrittää myös oletusbudjettipäällikön ja raja-arvon, jonka mukaan käyttäjille lähetetään ilmoitus raja-arvon saavuttamisesta. Näiden kenttien arvoja käytetään oletusarvoina uusissa budjettien hallintasäännöissä tai budjettiryhmissä, joita luodaan. Yksittäisten ryhmien tai sääntöjen oletusarvoja voidaan kuitenkin muuttaa. 

Budjettirekisterin budjettien luonti- ja tallennustavat auttavat määrittämään aikavälin, joka valitaan käytettävissä olevien budjettivarojen arvioinnin yhteydessä. Jos käytössä on dimension arvojen yhdistelmän vuosittainen summa, kannattaa ehkä käyttää tilikautta tai tilikautta tähän päivään saakka. Jos organisaatiossa, jossa luodaan budjetti tilikauden mukaan tai kohdistus tehdään tilikausille, halutaan yksityiskohtaisempaa hallintaa, aikaväliksi kannattaa harkita tilikautta tähän päivään saakka tai neljännesvuotta. 

Myös organisaation kulttuuri auttaa määrityksessä, koska se vaikuttaa budjetointiin ja budjetin hallintaan.

### <a name="over-budget-permissions"></a>Budjetin ylitysoikeudet

Seuraavaksi määritetään käyttäjäryhmät **Budjetin ylitysoikeudet** -välilehdessä. Voit määrittää myös, onko käyttäjillä, jotka ovat ryhmän jäseniä, oikeus ylittää budjetti. Voit estää käyttäjiä ylittämästä **Budjettiparametrit**-sivulla määritettyä budjetin raja-arvoa tai voit estää käyttäjiä ylittämästä budjettia millään summalla raja-arvosta huolimatta. Nämä käyttöoikeudet voiva auttaa organisaation taloushallinnon resurssien hallinnassa, jos organisaatiossa hallitaan kulutusta ennakoivasti. 

### <a name="budget-funds-available"></a>Käytettävissä olevat budjettivarat

**Käytettävissä olevat budjettivarat** -välilehdessä voit määrittää seuraavaksi kaavan, jota käytetään käytettävissä olevien budjettivarojen laskennassa. Laskelma voi sisältää luonnoksia tai kirjaamattomia asiakirjoja riippuen siitä, miten konservatiivisesti organisaatiossa hallitaan taloushallinnon resursseja tai millaiset säädökset tai toimialan vaatimukset ovat. 

> [!NOTE]
> Jos tätä laskelmaa muokataan budjettijakson aikana, muutokset eivät vaikuta budjetin hallinnan tarkistuksissa hyväksyttyihin tai aiemmin kirjattuihin tai valmistuneisiin asiakirjoihin. Ominaisuuden nimeltä **Seuraa vain summia käytettävissä olevien budjettivarojen laskennassa** avulla voit muuttaa BudgetSourceTracking-taulujen seurattavia tietoja. Kun tämä toiminto on käytössä, summat tallennetaan vain, jos ne on valittu käytettävissä olevan budjettivaran laskennassa käytettäviksi. Lisätietoja on kohdassa [Saatavilla olevat budjettivarat](budget-funds-available.md).

### <a name="documents-and-journals"></a>Tiedostot ja kirjauskansiot

Valitaan **Tiedostot ja kirjauskansiot** -välilehdessä budjetin hallinnan tarkistuksiin mukaan otettavat lähdeasiakirjat ja -kirjauskansiot ja se, tehdäänkö tarkistus rivimerkinnän tasolla vai asiakirjalle kokonaisuutena. Lisäksi uusi **Budjetin hallinta-asiakirjan suodatuksen parannus** -toiminto, joka on käytettävissä Microsoft Dynamics 365 Finance -versiosta 10.0.27 alkaen, sisältää kyselypohjaisen suodatusvaihtoehdon jokaiselle budjetin hallintaan sisältyvälle tiedostolle. Näin ollen voit määrittää, mistä budjetin hallinta-asiakirjoista budjetti tarkistetaan. Näin toiminnon avulla voi tarkistaa vain tiedostotyypin osajoukon. Voit esimerkiksi tarkistaa vain ostotilaukset, joissa **Pooli**-kentän arvoksi on määritetty **01**. Uusi **Asiakirjat ja kirjauskansiot** -välilehteen lisätty sarake ilmaisee, onko valitulle tiedostotyypille määritetty kysely. Lisäksi tiedostoruudukon yläpuolella olevalle työkaluriville lisätyn kahden uuden painikkeen avulla voit lisätä, muokata tai poistaa suodatusta. 

Sinun tulisi täsmätä valitut lähdeasiakirjat niiden saldojen valintaruutujen kanssa, jotka on valittu käytössä olevien budjettivarojen laskelmaan. Jos valittuna on esimerkiksi **Varausten budjettivaraukset**, valittava asetus on **Ostotilaukset**. Kun budjetin tarkistus suoritetaan ostorivin summille ja tileille, varaukseen määritetty budjetin hallinnan luokka on **Varaus** Kun budjetin tarkistus suoritetaan ostoehdotuksen summille ja tileille, varaukseen määritetty budjetin hallinnan luokka on **Alustava varaus** 

Jos **Rasitteen budjettivaraukset** ja/tai **Alustavien rasitteiden budjettivaraukset** sisällytetään käytettävissä olevien budjettivarojen laskelmaan ja jos niiden on muututtava kirjanpidon kirjausten mukaisesti, kyseiset valinnat on merkittävä **Sitoumusten kirjanpito** -ryhmässä sivulla **Kirjanpidon parametrit**.

### <a name="assign-budget-models"></a>Määritä budjettimallit

Seuraavaksi liitetään budjetin hallintaan sisällytettävät budjettimallit budjettijakson aikaväleihin **Liitä budjettimallit** -välilehdessä.

### <a name="define-budget-control-rules"></a>Määritä budjetin hallintasäännöt

Seuraavaksi luodaan tietyt säännöt **Määritä budjetin hallintasäännöt** -välilehdessä budjetin hallinnan käytössä olevien taloushallinnan dimensioiden perusteella. Jos kohdistus tehdään esimerkiksi osaston menon tai menovälin perusteella, menot voidaan määrittää ja arvioida tämän välilehden asetusten avulla. Voit määrittää kullekin budjetin hallintasäännölle eri raja-arvot. 

> [!Important]
> Budjetin hallinta voidaan ottaa käyttöön mille tahansa **Voitto ja tappio**-, **Meno**-, **Tuotto-, Tase-, Velat-, Oma pääoma-** tai **Käyttöomaisuus**-tyypin päätilille. Jos **Määritä budjetinhallinnan säännöt** -välilehti sisältää säännön, jonka ehdot ovat tyhjät, budjetin hallinta otetaan käyttöön **kaikille** taloushallinnon dimension yhdistelmille, jotka sisältävät kyseisen tyyppisiä päätilejä. Tämän vuoksi on tärkeää luoda budjetin hallinnan säännöt, joissa määritetään taloushallinnon dimensioiden yhdistelmien arvovälit vain silloin, kun budjetin hallinnan käyttäminen on tärkeää.

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
Kun budjetin hallinta on otettu käyttöön, vastaanotetaan niiden asiakirjojen ja kirjauskansioiden budjetin hallinnan varoituksia ja virhesanomia, joille on konfiguroitu budjetin hallinta. Muista, että voit määrittää budjetin hallinnan niin, että vaikka käyttäjille lähetetään varoitus budjetin varojen ylittämisestä, he voivat silti jatkaa tapahtumien vahvistamista tai kirjaamista. Epäonnistuneiden budjettitarkistusten tietoja voidaan taskastella **Budjetin hallinnan virheet ja varoitukset** -sivulla.

Tältä sivulta käyttäjät voivat porautua **Budjetin hallinnan tilasto kausittain** -sivulle ja tarkastella budjetin käytettävyystietoja ja varauksia tietyn budjetin ohjausdimensioyhdistelmän osalta. Käyttäjät voivat porautua myös **Budjetin hallinnan tilastot**-sivulle ja tarkastella budjetin käytettävyyttä kaikkien budjetin hallinnassa käytettävien taloushallinnon dimensioiden yhdistelmien osalta. 

Jos budjetin hallinta on otettu käyttöön ostotilauksille, budjettipäällikkö voi tarkastella **Kirjanpitobudjetit ja ennusteet** -työtilan avulla kaikkien niiden vahvistamattomien ostotilausten jonoa, joilla on budjetin tarkistuksen varoituksia ja virheitä. Jos budjettipäälliköllä on budjetin ylitysoikeudet, ostotilaukset voidaan vahvistaa suoraan työtilassa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
