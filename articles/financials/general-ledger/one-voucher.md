---
title: Yksi tosite
description: "Talouskirjauskansioiden (kuten yleinen kirjauskansio, käyttöomaisuuden kirjauskansio tai toimittajan maksukirjauskansio) yksi tosite sallii useiden alareskontratapahtumien antamisen yhden tositteen kontekstissa."
author: kweekley
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f996131830f9bd4efd534143b3fb761c5ccc756
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="one-voucher"></a>Yksi tosite

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
>  Tämä toiminto on käytössä Dynamics 365 for Finance and Operationsin versiossa 8.0, joka sisältyy kevään 2018 versioon.   

<a name="what-is-one-voucher"></a>Mikä on yhden tositteen toiminto?
======================

Talouskirjauskansioiden (kuten yleinen kirjauskansio, käyttöomaisuuden kirjauskansio tai toimittajan maksukirjauskansio) aiemmin luotu toiminto sallii useiden alareskontratapahtumien antamisen yhden tositteen kontekstissa. Tätä toimintoa kutsutaan yhden tositteen toiminnoksi. Voit luoda yhden tositteen toiminnon jollakin seuraavista tavoista:

-   Määritä kirjauskansion nimi (**Kirjanpito** \> **Kirjauskansion asetukset** \>**Kirjauskansioiden nimet**) siten, että **Uusi tosite** -kentän valintana on **Vain yksi tositenumero**. * Jokainen kirjauskansioon lisätty rivi sisällytetään nyt samaan tositteeseen. Koska jokainen rivi on lisätty samaan tositteeseen, tosite voidaan syöttää usean rivin tositteena, saman rivin tilinä/vastatilinä tai niiden yhdistelmänä.

[![Yksi rivi](./media/same-line.png)](./media/same-line.png)
 
> [!IMPORTANT] 
> *  Huomaa, että yhden tositteen määritelmä EI sisällä niitä kirjauskansion nimiä, jotka on määritetty **vain yhdeksi tositenumeroksi** ja käyttäjä kirjaa sitten tositteen, joka sisältää vain kirjanpitotilityyppejä.  Tässä asiakirjassa yksi tosite tarkoittaa, että yhdessä tositteessa on enemmän kuin yksi toimittaja, asiakas, pankki, käyttöomaisuuserä tai projekti. 

-   Syötä usean rivin tosite, jossa ei ole vastatiliä.

[![Useita rivejä sisältävä tosite](./media/Multi-line.png)](./media/Multi-line.png)

-   Syötä tosite, jossa sekä tili että vastatili sisältävät alareskontran tilityypin, kuten toimittaja/toimittaja, asiakas/asiakas, toimittaja/asiakas tai pankki/pankki.

[![Alareskontran tosite](./media/subledger.png)](./media/subledger.png)

<a name="issues-with-one-voucher"></a>Yhden tositteen toiminnallisuuden ongelmat
=======================

Yksi tosite -toiminto aiheuttaa ongelmia esimerkiksi tilityksen, arvonlisäveron laskennan, alareskontran kirjanpitoon tehtävän täsmäytyksen ja raportoinnin aikana. (Lisätietoja tilityksen aikana mahdollisesti tapahtuvista varasto-otoista on kohdassa [Yksi tosite useille asiakas- tai toimittajatietueille](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Jotta työ ja raportointi sujuu oikein, näille prosesseille ja raporteille on annettava tapahtuman tiedot. Vaikka jotkin skenaariot voivat yhä toimia oikein, useiden tapahtumien syöttäminen yhteen tositteeseen aiheuttaa usein ongelmia organisaation asetusten vuoksi.

Voit esimerkiksi kirjata seuraavan useita rivejä sisältävän tositteen.

[![Esimerkki](./media/example.png)](./media/example.png)

Voit sitten luoda **Toimittajakohtaiset kulut** -raportin **Taloushallinnon tiedot** -työtilassa. Raporttiryhmien kulutili täsmäytetään toimittajaryhmässä ja toimittajan kohdalla. Raporttia luotaessa järjestelmä ei voi määrittää, mitkä toimittajaryhmät tai toimittajat aiheuttivat kulun 250,00. Koska tapahtuman tiedot puuttuvat, järjestelmä olettaa, että 250,00 on tositteen ensimmäisen toimittajan aiheuttama. Päätilin 600120 saldoon sisältyvä 250,00 näytetään sitten kyseisen toimittajaryhmän tai toimittajan kohdalla. On todennäköistä, että tositteen ensimmäinen toimittaja ei ole oikea toimittaja, joten raportti on virheellinen.

[![Kulut](./media/expenses.png)](./media/expenses.png)

<a name="the-future-of-one-voucher"></a>Yksi tosite jatkossa
=========================

Aiemmista ongelmista johtuen yhden tositteen toiminnallisuus on vanhentunut. Toiminallisuutta ei poisteta käytöstä kerralla, koska jotkin toiminnalliset aukot saattavat olla riippuvaisia tästä toiminnallisuudesta. Sen sijaan käytetään seuraavaa aikataulua: 

- **Kevään 2018 versio** – Toiminnot poistetaan käytöstä oletusarvoisesti kirjanpidon parametrien avulla. Voit ottaa toiminnallisuuden käyttöön, jos organisaatiossa on skenaario, joka toteuttaa myöhemmin tässä ohjeaiheessa esitellyn liiketoimintaskenaarion aukon.

  -   Jos asiakkaalla on liiketoimintaskenaario, jossa ei tarvita yhden tositteen toiminnallisuutta, älä ota toiminnallisuutta käyttöön. Myöhemmin tässä ohjeaiheessa mainituilla alueilla esiintyviä virheitä ei korjata, jos tätä toimintoa käytetään vaikka käytettävissä on myös toinen ratkaisu.

  -   Lopeta yhden tositteen käyttö Microsoft Dynamics 365 Finance and Operations -integrointien yhteydessä, ellei toiminnallisista aukoista edellytä toiminnon käyttöä.

- **Syksy 2018 ja myöhemmät versiot** – Toiminnalliset aukot täytetään. Kun toiminnalliset aukot on täytetty, yhden tositteen toiminnallisuus poistetaan käytöstä pysyvästi.

- > [!IMPORTANT]
  > Huomaa, että **Vain yksi tositenumero** -asetusta EI ole poistettu kirjauskansion nimen asetuksista.  Tätä asetusta tuetaan edelleen, kun tosite sisältää vain kirjanpitotilityyppejä.  Asiakkaiden on oltava huolellinen tätä asetusta käytettäessä, sillä tositetta ei kirjata, jos he käyttävät **Vain yksi tositenumero** -asetusta mutta kirjaavat useamman kuin yhden asiakkaan, toimittajan, pankin, käyttöomaisuuserän tai projektin.  Asiakkaat voivat edelleen kirjata alareskontran tilityyppejä, kuten maksun yhdellä tositteella, joka sisältää Toimittaja/pankki-tilityyppejä.  

<a name="why-use-one-voucher"></a>Yhden tositteen käytön syitä
====================

Asiakaspalautteen perusteella olemme kääntäneet seuraavat skenaariot, joissa asiakkaat voivat käyttää skenaarioissa yhden tositteen toiminnallisuutta, tai syyt niiden käyttämiselle. Jotkin näistä liiketoiminnan tarpeista voidaan toteuttaa vain käyttämällä yhtä tositetta. Vaihtoehdot voivat kuitenkin täyttää samat liiketoimintavaatimukset useissa skenaarioissa.

<a name="scenarios-that-require-one-voucher"></a>Yhtä tositetta edellyttävät skenaariot
----------------------------------

Seuraavat skenaariot voidaan toteuttaa vain käyttämällä yhden tositteen toiminnolla. Nämä toiminnalliset aukot täytetään muilla toiminnoilla syksyn 2018 ja sitä myöhemmissä versioissa.

-   **Kirjaa yhteenvetolomakkeen toimittaja- tai asiakasmaksut pankkitilille**

    -   Orgamisaatio käyttää toimittajien ja summien luetteloa pankin tietoissa. Pankki käyttää tätä luetteloa, kun se maksaa toimittajalle organisaation puolesta. Pankki kirjaa maksujen summan yhtenä pankkitilin ottona.

>   Toimittajamaksujen yhteenvetoa tuetaan vain yhden tositteen avulla. Kukin toimittaja syötetään erillisenä rivinä, jotta ostoreskontran alareskontraa voidaan ylläpitää. Kaikkien maksujen yhteenvetosumma on kuitenkin pankkitilin yhden rivin vastakirjaus. Otto näytetään tämän vuoksi yhtenä yhteenlaskettuna summana pankin alareskontrassa.

-   Organisaatio tallettaa asiakasmaksut ai pankki tallettaa ne organisaation puolesta, jolloin talletus näkyy kokonaissummana pankkitlillä.

>   Asiakasmaksujen yhteenvetoa tuetaan yleensä talletustoiminnon avulla. Jos käytössä on kuitenkin maksutavan välitiliöinti, tätä skenaariota tuetaan vain yhden tositteen toiminnallisuuden kautta. Asiakasmaksut annetaan toimittajamaksujen yhteenvedossa kuvatulla tavalla.

-   **Menetelmä, jonka avulla liiketoimintatapahtuman tapahtumat ryhmitellään**

    -   Organisaatiolla on yksi liiketoimintatapahtuma, joka käynnistää useita tapahtumia. Kirjanpito-osasto haluaa kuitenkin tarkastella kirjanpitotapahtumia yhdessä, jolloin tarkastettavuus on parempi kuin muuten.

>   Jos organisaatiossa on tarkasteltava kirjanpitotapahtumia liiketoimintatapahtumassa yhdessä, yhden tositteen toiminnallisuuden on oltava käytössä. 

- **Maakohtaiset erityispiirteet**

  -   Puolan SAD (Single Administrative Document) -ominaisuus edellyttää tällä hetkellä yhden tositteen käyttöä. Yhden tositteen toimintoa on käytettävä siihen saakka, että ryhmittelyasetus on valittavana tässä ominaisuudessa. Tietyt maakohtaiset ominaisuudet voivat edellyttää yhden tositteen toiminnon käyttöä.

- **Asiakkaan ennakkomaksun maksukirjauskansio, joka sisältää veroja useilla riveillä**

  -   Asiakas tekee tilaukselle ennakkomaksun. Tilauksen riveillä on eri verosummat, jotka on tallennettava ennakkomaksua varten. Asiakkaan maksun ennakkomaksu on yksi tapahtuma, joka simuloi tilauksen rivit, jotta kunkin rivin summalle voidaan kirjata soveltuva vero.

Tässä skenaariossa yhden tositteen asiakkaat ovat samoja, koska tapahtuma simuloi asiakastilauksen rivejä. Ennakkomaksu on annettava yhdessä tositteessa, sillä vero on laskettava asiakkaan tekemän yhden maksun riveillä.

-   **Käyttöomaisuuden ylläpito: Poiston kertymä, käyttöomaisuuden jako, poiston laskeminen luovutuksen yhteydessä**

Myös seuraavat käyttöomaisuustapahtumat luovat useita tapahtumia yhteen tositteeseen:
-   Käyttöomaisuudelle tehdään lisähankinta ja kertynyt poisto lasketaan.
-   Käyttöomaisuus jaetaan.
-   Parametri, jota käytetään luovutuksen poistossa, on käytössä. Käyttöomaisuus poistetaan.

<a name="scenarios-that-dont-require-one-voucher"></a>Skenaariot, joissa ei edellytetä yhtä tositetta
----------------------------------------

Seuraavat skenaariot voidaan toteuttaa muilla tavoin eikä yhden tositteen toimintoja pitäisi käyttää.

-   **Kirjaa yhteenvetolomakkeen asiakasmaksut pankkitilille**

Organisaatio tallettaa asiakasmaksut ai pankki tallettaa ne organisaation puolesta, jolloin talletus näkyy kokonaissummana pankkitlillä.

Asiakasmaksujen yhteenvetoa tuetaan talletustoiminnolla, kun välitiliöintiä ei käytetä maksutapana.

-   **Nettoutus**

Nettoutuksessa toimittajan ja asiakkaan saldot nettoutetaan toisiinsa, koska toimittaja ja asiakas kuuluvat samaan osapuoleen. Tämä vähentää organisaation ja asiakas- tai toimittajaosapuolen välillä tapahtuvaa rahan käsittelyä.

Netottaminen voidaan tehdä syöttämällä lisäys ja vähennys erillisiin tositteisiin ja kirjaamalla vastakirjaus selvityksen kirjanpitotilille.

-   **Kirjaa yhteenveto kirjanpitoon**

Organisaatiot haluavat usein kirjata kirjanpitoon yhteenvetomuodossa, jolloin tietojen määrä on pieni. Organisaatiot kuitenkin yleensä vaativat, että tapahtuman tietoja ylläpidetään. Kun kirjaus tehdään yhteenvetona yhden tositteen kautta, tapahtumayksityiskohtia ei tiedetä eikä niitä voida ylläpitää.

   -   Koska tapahtuman tietoja ei voi tällä hetkellä ylläpitää, yhden tositteen toiminnallisuutta ei suositella käytettäväksi yhteenvedon kirjauksissa.
   -   Kun yhden tositteen tuki on poistettu, lähdeasia- ja kirjanpitiokehikot voidaan ottaa käyttöön kirjauskansioissa. Nämä kehikot ylläpitävät sitten tapahtumien tietoja ja tukevat yhteenvetoa kirjanpitoon.

-   **Tilitä useita kirjaamattomia maksuja samaan laskuun**

Tämä skenaariossa esiintyy yleensä vähittäismyyntiorganisaatioissa, joissa asiakkaat käyttävät ostojen maksamiseen useita maksutapoja. Tässä skenaariossa organisaation on voitava tallentaa useita kirjaamattomia maksuja ja tilittää ne myyntilaskua vastaan.

Uusi toiminto, joka lisättiin Microsoft Dynamics 365 for Operations -versioon 1611 (marraskuu 2016), mahdollistaa useiden kirjaamatomien maksujen tilityksen yhteen laskuun. Useita asiakasmaksuja ei enää tarvitse syöttää yhteen tositteeseen.

-   **Tuo tiliotteen tapahtumat**

Pankit usein maksavat ja vastaanottavat maksuja organisaation puolesta. Nämä tapahtumat tallennetaan Finance and Operations -sovelluksesessa pankilta saadun tiedoston kautta. Organisaatiot haluavat usein ryhmitellä nämä tapahtumat tiedostossa olevan tiliotteen numeron avulla. Koska kaikkien tapahtumien yksityiskohdat näytetään tiliotteella, pankin alareskontralle ei vaadita yhteenvetoa.

Tapahtumat voidaan ryhmitellä käyttämällä kirjauskansion muita kenttiä, kuten kirjauskansion eränumeroa tai asiakirjanumeroa.

-   **Siirrä saldot**

Organisaation on ehkä siirrettävä saldo toimittajalta toiselle toimittajalle virheen vuoksi tai siksi, että toinen toimittaja on ottanut velan itselleen. Tämän tyyppisiä siirtoja voi tehdä myös tilityypeille, kuten asiakkaille ja pankkitileille.

Saldojen siirrot yhdeltä tililtä (esimerkiksi toimittaja-, asiakas tai pankkitili) toiselle tilille voidaan tehdä erillisten tositteiden kautta. Siirtymän voi kirjata selvityksen kirjanpitotilille.

-   **Anna alkusaldot**

Organisaatiot syöttävät usein aloitussaldot alareskontran tileille (esimerkiksi toimittajat, asiakkaat ja käyttöomaisuus) yhden tositteen tapahtumana. Kunkin alareskontran tilin aloitussaldot voidaan syöttää erillisinä tositteina. Vastakirjauksen voi kirjata selvityksen kirjanpitotilille.

-   **Korjaa asiakkaan tai toimittajan kirjatun asiakirjan kirjanpitomerkintä**

Organisaatiolla voi olla oikea myynti- tai ostoreskontran kirjanpitotili kirjatun laskun kirjanpitomerkintää varten, mutta kyseistä laskua ei voi peruuttaa tai korjata toisen mekanismin avulla.

Jos myynti- tai ostoreskontran kirjanpitotiliin on tehtävä korjaus, oikaisu on tehtävä suoraan kirjanpitotiliin. Oikaisua ei voi tehdä asiakkaan tai toimittajan kautta tehdyllä kirjauksessa. Tämä edellyttää, että oikaisu tehdään käyttökatkon aikana, jotta kirjanpitotili sallii väliaikaisesti manuaalisen kirjauksen.

-   **Mahdollista järjestelmässä"**

Organisaatiot käyttävät usein yhden tositteen toiminnallisuutta vain, koska järjestelmä mahdollistaa sen käytön, vaikka toiminnallisuuden vaikutuksia ei tunneta.

