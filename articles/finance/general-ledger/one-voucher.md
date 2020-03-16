---
title: Yksi tosite
description: Talouskirjauskansioiden (kuten yleinen kirjauskansio, käyttöomaisuuden kirjauskansio tai toimittajan maksukirjauskansio) yksi tosite sallii useiden alareskontratapahtumien antamisen yhden tositteen kontekstissa.
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 68ec3cb028462865e914cbcb25ff28dbaf9a4f01
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3058014"
---
# <a name="one-voucher"></a>Yksi tosite

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a>Mikä on yhden tositteen toiminto?

Talouskirjauskansioiden (kuten yleinen kirjauskansio, käyttöomaisuuden kirjauskansio tai toimittajan maksukirjauskansio) aiemmin luotu toiminto sallii useiden alareskontratapahtumien (asiakas, toimittaja, käyttöomaisuuserät, projekti ja pankki) antamisen yhden tositteen kontekstissa. Microsoft kutsuu tätä toimintoa *yhden tositteen* toiminnoksi. Voit luoda yhden tositteen toiminnon jollakin seuraavista tavoista:

- Määritä kirjauskansion nimi (**Kirjanpito** \> **Kirjauskansion asetukset** \> **Kirjauskansioiden nimet**) siten, että **Uusi tosite** -kentän valintana on **Vain yksi tositenumero**. Jokainen kirjauskansioon lisätty rivi sisällytetään nyt samaan tositteeseen. Tämän vuoksi tosite voidaan kirjata usean rivin tositteena, saman rivin tilinä/vastatilinä tai niiden yhdistelmänä.

    [![Yksi rivi](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > Yhden tositteen määritelmä **ei** koske tapauksia, joissa kirjauskansion nimet on määritetty **vain yhdeksi tositenumeroksi** mutta käyttäjä kirjaa sitten tositteen, joka sisältää vain kirjanpitotilityyppejä. Tässä ohjeaiheessa yksi tosite tarkoittaa, että yhdessä tositteessa on enemmän kuin yksi toimittaja, asiakas, pankki, käyttöomaisuuserä tai projekti.

- Syötä usean rivin tosite, jossa ei ole vastatiliä.

    [![Useita rivejä sisältävä tosite](./media/Multi-line.png)](./media/Multi-line.png)

- Syötä tosite, jossa sekä tili että vastatili sisältävät alareskontran tilityypin, kuten **toimittaja**/**toimittaja**, **asiakas**/**asiakas**, **toimittaja**/**asiakas** tai **pankki**/**pankki**.

    [![Alareskontran tosite](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Yhden tositteen toiminnallisuuden ongelmat

Yhden tositteen toiminto aiheuttaa ongelmia esimerkiksi tilityksen, arvonlisäveron laskennan, tapahtuman peruutuksen, alareskontran kirjanpitoon tehtävän täsmäytyksen ja raportoinnin aikana. (Lisätietoja tilityksen aikana mahdollisesti tapahtuvista varasto-otoista on esimerkiksi kohdassa [Yksi tosite useille asiakas- tai toimittajatietueille](https://docs.microsoft.com/dynamics365/finance/accounts-payable/single-voucher-multiple-customer-vendor-records).) Jotta työ ja raportointi sujuu oikein, näille prosesseille ja raporteille on annettava tapahtuman tiedot. Vaikka jotkin skenaariot voivat yhä toimia oikein, useiden tapahtumien syöttäminen yhteen tositteeseen aiheuttaa usein ongelmia organisaation asetusten vuoksi.

Voit esimerkiksi kirjata seuraavan useita rivejä sisältävän tositteen.

[![Esimerkki](./media/example.png)](./media/example.png)

Voit sitten luoda **Toimittajakohtaiset kulut** -raportin **Taloushallinnon tiedot** -työtilassa. Tässä raportissa kulutilin saldot ryhmitetään toimittajaryhmän ja sitten toimittajan mukaan. Raporttia luotaessa järjestelmä ei voi määrittää, mitkä toimittajaryhmät tai toimittajat aiheuttivat kulun 250,00. Koska tapahtuman tiedot puuttuvat, järjestelmä olettaa, että koko kulu 250,00 on tositteen ensimmäisen toimittajan aiheuttama. Tämän vuoksi Päätilin 600120 saldoon sisältyvä kulu 250,00 näytetään kyseisen toimittajaryhmän tai toimittajan kohdalla. On kuitenkin todennäköistä, että tositteen ensimmäinen toimittaja ei ole oikea toimittaja. Tämän vuoksi raportti on todennäköisesti virheellinen.

[![Kulut](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>Yksi tosite jatkossa

Aiemmin mainituista ongelmista johtuen yhden tositteen toiminnallisuus on vanhentunut. Toimintoa ei poisteta käytöstä kerralla, koska jotkin toiminnalliset aukot saattavat olla riippuvaisia tästä toiminnosta. Sen sijaan käytetään seuraavaa aikataulua:

- **Kevään 2018 versio** – Oletusarvoisesti toiminto poistetaan käytöstä **Kirjanpitoparametrit**-sivun **Yleiset**-välilehden **Salli useita tapahtumia yhdessä tositteessa** -parametrilla. Voit ottaa toiminnon käyttöön, jos organisaatiossa on skenaario, joka toteuttaa myöhemmin tässä ohjeaiheessa käsitellyn toiminnallisen aukon.

    - Jos asiakkailla on liiketoimintaskenaario, jossa ei tarvita yhden tositteen toiminnallisuutta, toimintoa ei kannata ottaa käyttöön. Microsoft ei korjaa myöhemmin tässä ohjeaiheessa mainituilla alueilla esiintyviä virheitä, jos tätä toimintoa käytetään vaikka käytettävissä on myös toinen ratkaisu.
    - Lopeta yhden tositteen käyttö integrointien yhteydessä, elleivät toiminnalliset aukot edellytä toiminnon käyttöä.

- **Myöhemmät versiot** – Kaikki toiminnalliset aukot täytetään. **Kun toiminnalliset aukot on täytetty ja uudet ominaisuudet on toimitettu, kestää ainakin vuoden, ennen kuin yhden tositteen toiminto poistetaan pysyvästi käytöstä**, sillä asiakkailla ja riippumattomilla ohjelmistotoimittajilla on oltava riittävästi aikaa reagoida uuteen toimintoon. Heidän on ehkä esimerkiksi päivitettävä liiketoimintaprosessit, yksiköt ja integroinnit.

> [!IMPORTANT]
> Huomaa, että **Vain yksi tositenumero** -asetusta **ei** ole poistettu kirjauskansion nimen asetuksista. Tätä asetusta tuetaan edelleen, kun tosite sisältää vain kirjanpitotilityyppejä. Asiakkaiden on oltava huolellinen tätä asetusta käytettäessä, sillä tositetta ei kirjata, jos he käyttävät **Vain yksi tositenumero** -asetusta mutta kirjaavat useamman kuin yhden asiakkaan, toimittajan, pankin, käyttöomaisuuserän tai projektin. Asiakkaat voivat edelleen kirjata alareskontran tilityyppejä, kuten maksun yhdellä tositteella, joka sisältää **Toimittaja**/**pankki**-tilityyppejä.

## <a name="why-use-one-voucher"></a>Yhden tositteen käytön syitä

Asiakaspalautteen perusteella Microsoft on kääntänyt seuraavat skenaariot, joissa asiakkaat voivat käyttää skenaarioissa yhden tositteen toiminnallisuutta, tai syyt niiden käyttämiselle. Jotkin näistä liiketoiminnan tarpeista voidaan toteuttaa vain käyttämällä yhtä tositetta. Vaihtoehdot voivat kuitenkin täyttää samat liiketoimintavaatimukset useissa skenaarioissa.

### <a name="scenarios-that-require-one-voucher"></a>Yhtä tositetta edellyttävät skenaariot

Seuraavat skenaariot voidaan toteuttaa vain käyttämällä yhden tositteen toiminnolla. Jos organisaatiossa on jokin näistä skenaariosta, tositteessa on otettava käyttöön useiden tapahtumien kirjaaminen muuttamalla **Salli useita tapahtumia yhdessä tositteessa** -parametrin asetusta **Kirjanpitoparametrit**-sivulla. Nämä toiminnalliset aukot täytetään muilla toiminnoilla myöhemmissä versioissa.

> [!Note]
> [Kussakin seuraavassa skenaariossa **Salli useita tapahtumia yhdessä tositteessa** -kentän asetuksiksi on valittava Kyllä **Kirjanpidon parametrit** -sivun **Yleiset**-pikavälilehdessä.]

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>Kirjaa yhteenvetolomakkeen toimittaja- tai asiakasmaksut pankkitilille

**Skenaario** Organisaatio käyttää toimittajien ja summien luetteloa pankin tietoissa. Pankki käyttää tätä luetteloa, kun se maksaa toimittajalle organisaation puolesta. Pankki kirjaa maksujen summan yhtenä pankkitilin ottona.

Toimittajamaksujen yhteenvetoa tuetaan vain yhden tositteen avulla. Jokainen toimittaja kirjataan erillisenä rivinä, jotta ostoreskontran alareskontran tietoja voidaan ylläpitää. Kaikkien maksujen yhteenlaskettu summa vastakirjataan yhdelle pankkitilin riville. Otto näytetään tämän vuoksi yhtenä yhteenlaskettuna summana pankin alareskontrassa.

**Skenaario** Organisaatio tallettaa asiakasmaksut tai pankki tallettaa ne organisaation puolesta, jolloin talletus näkyy kokonaissummana pankkitilillä.

Asiakasmaksujen yhteenvetoa tuetaan yleensä talletustoiminnon avulla. Jos käytössä on kuitenkin maksutavan välitiliöinti, tätä skenaariota tuetaan vain yhden tositteen toiminnallisuuden kautta. Asiakasmaksut annetaan toimittajamaksujen yhteenvedossa kuvatulla tavalla.

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>Menetelmä, jonka avulla liiketoimintatapahtuman tapahtumat ryhmitellään

**Skenaario** Organisaatiolla on yksi liiketoimintatapahtuma, joka käynnistää useita tapahtumia. Kirjanpito-osasto haluaa kuitenkin tarkastella kirjanpitotapahtumia yhdessä, jolloin tarkastettavuus on parempi kuin muuten.

Jos organisaatiossa on tarkasteltava kirjanpitotapahtumia liiketoimintatapahtumassa yhdessä, yhden tositteen toiminnallisuuden on oltava käytössä. 

### <a name="country-specific-features"></a>Maakohtaiset erityispiirteet

**Skenaario** Puolan SAD (Single Administrative Document) -ominaisuus edellyttää tällä hetkellä yhden tositteen käyttöä. Yhden tositteen toimintoa on käytettävä siihen saakka, että ryhmittelyasetus on valittavana tässä ominaisuudessa. Tietyt maakohtaiset ominaisuudet voivat edellyttää yhden tositteen toiminnon käyttöä.

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>Asiakkaan ennakkomaksun maksukirjauskansio, joka sisältää veroja useilla riveillä

Tässä skenaariossa yhden tositteen asiakkaat ovat samoja, koska tapahtuma simuloi asiakastilauksen rivejä. Ennakkomaksu on annettava yhdessä tositteessa, sillä vero on laskettava asiakkaan tekemän yhden maksun riveillä.

### <a name="customer-reimbursement"></a>Asiakkaan hyvitys

**Skenaario** Asiakas tekee tilaukselle ennakkomaksun. Tilauksen riveillä on eri verosummat, jotka on tallennettava ennakkomaksua varten. Asiakkaan maksun ennakkomaksu on yksi tapahtuma, joka simuloi tilauksen rivit, jotta kunkin rivin summalle voidaan kirjata soveltuva vero.

Jos hyvityksen kausittainen tehtävä suoritetaan myyntireskontramoduulista, se luo saldon siirtotapahtuman asiakkaalta toimittajalle. Tässä skenaariossa hyvitys asiakkaalle on tehtävä yhden tositteen toiminnolla.

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>Käyttöomaisuuden ylläpito: Poiston kertymä, käyttöomaisuuden jako, poiston laskeminen luovutuksen yhteydessä
Myös seuraavat käyttöomaisuustapahtumat luovat useita tapahtumia yhteen tositteeseen:

- Käyttöomaisuudelle tehdään lisähankinta ja kertynyt poisto lasketaan.
- Käyttöomaisuus jaetaan.
- Parametri, jota käytetään luovutuksen poistossa, on käytössä. Käyttöomaisuus poistetaan.
- Käyttöomaisuuden käyttöottopäivämäärä on ennen hankintapäivämäärää. Tämän vuoksi kirjataan poisto-oikaisu.

> [!Note]
> Varmista tapahtumia kirjattaessa, että tapahtumat kohdistetaan samaan käyttöomaisuuteen. Tositetta ei kirjata, jos siinä enemmän kuin yksi käyttöomaisuus, vaikka **Uusi tosite** -kentän asetuksena on Vain yksi tositenumero **Kirjauskansioiden nimet** -sivulla kirjanpidossa. Jos tositteessa on useampi kuin yksi käyttöomaisuus, sanoma **Tositetta kohden voi olla vain yksi käyttöomaisuustapahtuma** avautuu etkä voi kirjata tositetta.  

### <a name="bills-of-exchange-and-promissory-notes"></a> Vekselit ja velkakirjat
Vekselit ja velkakirjat edellyttävät yhden tositteen käyttöä, koska tapahtumat siirtävät asiakkaan tai toimittajan saldon yhdeltä myyntireskontran/ostoreskontran kirjanpitotililtä toiselle maksun tilan perusteella.

## <a name="scenarios-that-dont-require-one-voucher"></a>Skenaariot, joissa ei edellytetä yhtä tositetta

Seuraavat skenaariot voidaan toteuttaa muilla tavoin eikä yhden tositteen toimintoja pitäisi käyttää.

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>Kirjaa yhteenvetolomakkeen asiakasmaksut pankkitilille

Organisaatio tallettaa asiakasmaksut ai pankki tallettaa ne organisaation puolesta, jolloin talletus näkyy kokonaissummana pankkitlillä.

Asiakasmaksujen yhteenvetoa tuetaan talletustoiminnolla, kun välitiliöintiä ei käytetä maksutapana.

### <a name="netting"></a>Nettoutus

Nettoutuksessa toimittajan ja asiakkaan saldot nettoutetaan toisiinsa, koska toimittaja ja asiakas kuuluvat samaan osapuoleen. Tämä vähentää organisaation ja asiakas- tai toimittajaosapuolen välillä tapahtuvaa rahan käsittelyä.

Netottaminen voidaan tehdä syöttämällä lisäys ja vähennys erillisiin tositteisiin ja kirjaamalla sitten vastakirjaus selvityksen kirjanpitotilille.

### <a name="post-in-summary-to-the-general-ledger"></a>Kirjaa yhteenveto kirjanpitoon

Organisaatiot haluavat usein kirjata kirjanpitoon yhteenvetomuodossa, jolloin tietojen määrä on pieni. Tällaiset organisaatiot kuitenkin yleensä edellyttävät, että tapahtuman tietoja ylläpidetään. Kun kirjaus tehdään yhteenvetomuodossa yhden tositteen kautta, tapahtuman tietoja ei tiedetä eikä niitä voida ylläpitää.

- Koska tapahtuman tietoja ei voi tällä hetkellä ylläpitää, yhden tositteen toiminnallisuutta **ei** suositella käytettäväksi yhteenvetomuodon kirjauksissa.
- Kun yhden tositteen tuki on poistettu, lähdeasia- ja kirjanpitiokehikot voidaan ottaa käyttöön kirjauskansioissa. Nämä kehikot ylläpitävät sitten tapahtumien tietoja ja tukevat yhteenvetoa kirjanpitoon.


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>Tilitä useita kirjaamattomia maksuja samaan laskuun

Tämä skenaariossa esiintyy yleensä organisaatioissa, joissa asiakkaat käyttävät ostojen maksamiseen useita maksutapoja. Tässä skenaariossa organisaation on voitava tallentaa useita kirjaamattomia maksuja ja tilittää ne myyntilaskua vastaan.

Uusi toiminto, joka lisättiin Microsoft Dynamics 365 for Operationsin versioon 1611 (marraskuu 2016), mahdollistaa useiden kirjaamatomien maksujen tilityksen yhteen laskuun. Useita asiakasmaksuja ei enää tarvitse syöttää yhteen tositteeseen.

### <a name="import-bank-statement-transactions"></a>Tuo tiliotteen tapahtumat

Pankit usein maksavat ja vastaanottavat maksuja organisaation puolesta. Nämä tapahtumat tallennetaan Financessa pankilta saadun tiedoston kautta. Organisaatiot haluavat usein ryhmitellä nämä tapahtumat tiedostossa olevan tiliotteen numeron avulla. Koska kaikkien tapahtumien yksityiskohdat näytetään tiliotteella, pankin alareskontralle ei vaadita yhteenvetoa.

Tapahtumat voidaan ryhmitellä käyttämällä kirjauskansion muita kenttiä, kuten kirjauskansion eränumeroa tai asiakirjanumeroa.


### <a name="transfer-balances"></a>Siirrä saldot

Organisaation on ehkä siirrettävä saldo toimittajalta toiselle toimittajalle virheen vuoksi tai siksi, että toinen toimittaja on ottanut velan itselleen. Tämän tyyppisiä siirtoja voi tehdä myös tilityypeille, kuten **Asiakas** ja **Pankki**.

Saldojen siirrot yhdeltä tililtä (esimerkiksi toimittaja, asiakas tai pankki) toiselle tilille voidaan tehdä erillisten tositteiden kautta. Siirtymän voi kirjata selvityksen kirjanpitotilille.

### <a name="enter-beginning-balances"></a>Anna alkusaldot

Organisaatiot syöttävät usein aloitussaldot alareskontran tileille (esimerkiksi toimittajat, asiakkaat ja käyttöomaisuus) yhden tositteen tapahtumana. Kunkin alareskontran tilin aloitussaldot voidaan syöttää erillisinä tositteina. Vastakirjauksen voi kirjata selvityksen kirjanpitotilille.

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>Korjaa asiakkaan tai toimittajan kirjatun asiakirjan kirjanpitomerkintä

Organisaatiolla voi olla oikea myynti- tai ostoreskontran kirjanpitotili kirjatun laskun kirjanpitomerkintää varten, mutta kyseistä laskua ei voi peruuttaa tai korjata toisen mekanismin avulla.

Jos myynti- tai ostoreskontran kirjanpitotiliin on tehtävä korjaus, oikaisu on tehtävä suoraan kirjanpitotiliin. Oikaisua ei voi tehdä asiakkaan tai toimittajan kautta tehdyllä kirjauksessa. Tämä edellyttää, että oikaisu tehdään käyttökatkon aikana, jotta kirjanpitotili sallii väliaikaisesti manuaalisen kirjauksen.

### <a name="the-system-allows-it"></a>Mahdollista järjestelmässä"

Organisaatiot käyttävät usein yhden tositteen toiminnallisuutta vain, koska järjestelmä mahdollistaa sen käytön, vaikka toiminnallisuuden vaikutuksia ei tunneta.
