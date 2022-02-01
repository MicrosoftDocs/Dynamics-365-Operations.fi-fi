---
title: Laskelman kirjaamisen toiminnallisuuden parannukset
description: Tässä aiheessa kuvataan parannuksia, jotka on tehty laskelman kirjaamistoimintoon.
author: analpert
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: analpert
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9a5a7d6394a87eccde8e1c364caaaabdb0297fd2
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982200"
---
# <a name="improvements-to-statement-posting-functionality"></a>Laskelman kirjaamisen toiminnallisuuden parannukset

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan ensimmäinen joukko parannuksia, jotka on tehty laskelman kirjaamistoimintoon. Nämä parannukset ovat käytettävissä Microsoft Dynamics 365 for Finance and Operations7.3.2 -versiossa.

## <a name="activation"></a>Aktivointi

Oletusarvon mukaan Finance and Operations 7.3.2:n käyttöönoton yhteydessä ohjelma määritetään käyttämään vanhaa ominaisuutta laskelman kirjauksia varten. Ottaaksesi käyttöön parannetun laskelman kirjaustoiminnon sinun on otettava käyttöön sen määritysavain.

- Siirry kohtaan **Järjestelmän hallinta** \> **Asetukset** \> **Käyttöoikeuden konfiguraatio**, ja poista sitten **Vähittäismyynti ja kauppa**-solmusta poista **Laskelmat (vanhat)** -valintaruutu ja valitse **Laskelmat**-valintaruutu.

Kun uusi **Laskelmat**-määritysavain on käytössä, uusi valikkokohde nimeltä **Laskelmat** on käytettävissä. Tämän valikkovaihtoehdon avulla voit luoda, laskea ja kirjata laskelmia manuaalisesti. Laskelmat, jotka aiheuttavat virheen eräkirjausprosessia käytettäessä, ovat myös saatavilla tämän valikkokohdan kautta. (Kun **Laskelmat (vanha)** -määritysavain on käytössä, valikkokohteen nimi on **Avoimet laskelmat**.)

Commerce sisältää seuraavat oikeellisuustarkistukset, jotka liittyvät näihin määritysavaimiin:

- Kumpaakin määritysavainta ei voi ottaa käyttöön samanaikaisesti.
- Samoja määritysavaimia on käytettävä kaikkiin toimintoihin, jotka suoritetaan tietyssä laskelmassa sen elinkaaren aikana (Luo, Laske, Tyhjennä, Kirjaa jne.). Et voi esimerkiksi luoda ja laskea laskelmaa, kun **Laskelmat (vanhat)** -määritysavain on käytössä ja yrität kirjata samaa laskelmaa **Laskelmat**-määritysavaimen ollessa käytössä.

> [!NOTE]
> Suosittelemme, että käytät **Laskelmat**-määritysavainta parannettua laskelman kirjaustoimintoa varten, ellei sinulla ole pakottava syytä **Laskelmat (vanhat)** -määritysavaimen käyttämiseksi. Microsoft jatkaa uuden kirjaustoiminnon parantamista, joten on tärkeää, että otat sen käyttöön mahdollisimman pian. Vanhan laskelman kirjaustoiminnon poistaminen käytöstä alkaa versiossa 8.0.

## <a name="setup"></a>Määritys

Laskelman kirjaamistoiminnon parantamisen myötä on otettu käyttöön kolme uutta parametria **Laskelma**-pikavälilehdellä **Kirjaus**-välilehdellä **Kaupan parametrit** -sivulla:

- **Poista laskelman tyhjentäminen käytöstä** – tämä vaihtoehto on käytettävissä vain vanhassa laskelman kirjaamistoiminnossa. Suosittelemme, että määrität tämän asetuksen arvoksi **Ei** estääksesi käyttäjiä tyhjentämästä laskelmia, jotka ovat osittain kirjatussa tilassa. Jos käyttäjät poistavat laskelmia, jotka ovat osittain kirjatussa tilassa, niiden tiedot korruptoituvat. Määritä tämän asetukseksi **Kyllä** vain poikkeustapauksissa.
- **Varaston varaaminen laskennan aikana** – Suosittelemme, että käytät **Kirjaa varasto** -erätyötä varaston varaamiseen ja määrität tämän asetuksen arvoksi **Ei**. Kun tämä vaihtoehto on **Ei**, parannettu laskelman kirjaustoiminto ei luoda varaston varaustapahtumia laskennan aikana (jos tapahtumia ei ole jo luotu **Kirjaa varasto** -erätyöllä). Sen sijaan toiminto luo varaston varaustapahtumat vain kirjauksen yhteydessä. Tämän toteutustapa on valittu sillä perusteella, että laskenta- ja kirjausprosessin välinen aikaikkuna on yleensä pieni. Js haluat varata varaston laskennan yhteydessä, voit määrittää asetukseksi **Kyllä**.

    Vanha laskelman kirjaustoiminto varaa aina varaston laskelman laskentaprosessissa (jos varausta ei ole jo tehty **Kirjaa varasto** -erätyöllä) riippumatta tästä asetuksesta.

- **Poista pakollinen laskenta käytöstä** – kun asetukseksi on määritetty **Kyllä**, laskelma jatkuu kirjausprosessin aikana, vaikka ero lasketun summan ja transaktion summan välillä ylittää rajan, joka on määritetty myymälöiden **Laskelma**-pikavälilehdessä.

Lisäksi seuraavat parametrit on esitelty **Eräkäsittely**-pikavälilehdellä **Kirjaus**-välilehdellä **Kaupan parametrit** -sivun kirjausvälilehden eräkäsittelypikavälilehdessä: 

- **Rinnakkaisen laskelman kirjauksen enimmäismäärä** – Tämä kenttä määrittää useiden laskelmien kirjaamiseen käytettävien erätehtävien määrän. 
- **Tilausten käsittelyn enimmäissäie** – Tämä kenttä edustaa laskelman kirjauksen eräajossa käytettävien säikeiden enimmäismäärää, kun halutaan luoda ja laskuttaa yhden laskelman myyntitilauksia. Laskelman kirjaus prosessissa käytettävien säikeiden kokonaismäärä lasketaan tämän parametrin arvon mukaan kerrottuna **Rinnakkaisen laskelman kirjausten enimmäismäärä**-parametrin arvolla. Tämän parametrin arvon määrittäminen liian suureksi voi vaikuttaa kielteisesti laskelman kirjausprosessin suorituskykyyn.
- **Koontia varten sisällytettyjen tapahtuma rivien enimmäismäärä** – Tämä kenttä määrittää, montako tapahtumariviä sisällytetään yksittäiseen yhteenlaskettavaan tapahtumaan ennen uuden luomista. Yhdistetyt tapahtumat luodaan erilaisten koostekriteerien, kuten asiakkaan, liiketoiminnan päivän tai taloushallinnon dimensioiden, perusteella. On tärkeää huomata, että yksittäisen tapahtuman rivejä ei jaeta eri yhdistettyjen tapahtumien kesken. Tämä tarkoittaa, että on mahdollista, että yhdistettyjen tapahtumien rivien määrä on hieman suurempi tai pienempi niiden tekijöiden perusteella, kuten erillisten tuotteiden määrä.
- **Säikeiden enimmäismäärä varastotapahtumien tarkistamista varten** – Tämä kenttä määrittää tapahtumien vahvistamiseen käytettävien säikeiden määrän. Tapahtumien vahvistaminen on pakollinen vaihe, joka on suoritettava, ennen kuin tapahtumat voidaan noutaa lausekkeissa. Sinun on myös määritettävä uuden kirjausprosessin aikana **Lahjakorttituote** **Lahjakortti**-pikavälilehdessä **Kaupan parametrit** -sivun **Kirjaus**-välilehdessä. Tämä on määritettävä myös silloin, kun organisaatio ei käytä lahjakortteja.

> [!NOTE]
> Kaikki asetukset ja parametrit, jotka liittyvät laskelman kirjauksiin ja jotka on määritetty vähittäismyymälöissä ja **Commerce-parametrit**-sivulla, liittyvät parannettuun laskelman kirjaustoimintoon.

## <a name="processing"></a>Käsittely

Laskelmat voidaan laskea ja kirjata eränä valikkovaihtoehtojen **Laskelmien laskenta eräajona** ja **Laskelmien kirjaaminen eräajona** avulla. Vaihtoehtoisesti laskelmat voidaan laskea manuaalisesti ja kirjata käyttämällä parannetun laskelman kirjaustoiminnon **Laskelmat**-valikkokohteella.

Prosessi ja vaiheet ja laskelmien eräkirjaamista varten ovat samat kuin vanhassa laskelman kirjaustoiminnossa. Laskelmien käsittelyn taustajärjestelmään on tehty kuitenkin merkittäviä parannuksia. Nämä parannukset tekevät prosessista luotettavamman ja ne parantavat tilojen ja virhetietojen näkyvyyttä. Käyttäjät voivat siten korjaa virheiden ensisijaiset syyt ja jatkaa kirjausprosessia ilman tietojen turmeltumista ja tietojen korjailua.

Seuraavissa osissa kuvataan laskelmien kirjaustoiminnon tärkeimmät parannukset, jotka näkyvät laskelmien ja kirjattujen laskelmien käyttöliittymässä.

### <a name="status-details"></a>Tilan tiedot

Uusi tilamalli on otettu käyttöön laskelman kirjausmenettelyn laskenta- ja kirjausprosesseissa.

Seuraavassa taulukossa kuvataan eri tilat ja niiden järjestys laskennan aikana.

| Tilajärjestys | Alue      | kuvaus |
|-------------|------------|-------------|
| 1           | Aloitettu    | Laskelma on luotu ja valmis laskettavaksi. |
| 2           | Merkitty     | Tapahtumat, jotka ovat laskelman alueella, on määritetty laskelman parametrien perusteella ja merkitty laskelman tunnuksella. |
| 3           | Laskettu | Laskelman rivit lasketaan ja näytetään. |

Seuraavassa taulukossa kuvataan eri tilat ja niiden järjestys kirjauksen aikana.

| Tilajärjestys | Alue                   | kuvaus |
|-------------|-------------------------|-------------|
| 1           | Tarkistettu                 | Useita oikeellisuustarkistuksia suoritetaan liittyen parametreihin (esimerkiksi käsittelyn kuluihin) sekä laskelmaan ja laskelman riveihin (esimerkiksi lasketun summan ja transaktion summan ero). |
| 2           | Koottu              | Nimettyjen ja nimettömien asiakkaiden myyntitapahtumat koostetaan konfiguraation mukaan. Lopulta jokainen koottu transaktio muunnetaan myyntitilaukseksi. |
| 3           | Asiakastilaus luotu  | Myyntitilaukset luodaan järjestelmässä kootun transaktion perusteella. |
| 4           | Asiakastilaus laskutettu | Myyntitilaukset on laskutettu. |
| 5           | Kirjatut alennukset        | Kausialennuksen kirjauskansiot kirjataan konfiguraation mukaan. |
| 6           | Kirjattu tuotto/kulu   | Tulo-/ kulutransaktiot kirjataan tositteina. |
| 7           | Linkitetyt tositteet         | Maksukirjauskansiot luodaan ja linkitetään vastaavaan laskuun. |
| 8           | Kirjatut maksut         | Maksukirjauskansiot on kirjattu. |
| 9           | Lahjakortit on kirjattu       | Lahjakorttitransaktiot kirjataan tositteina. |
| 10          | Julkaistut                  | Laskelma merkitään kirjatuksi. |

Jokainen edeltävien taulujen tila on luonteeltaan riippumaton, ja vaiheiden välille luodaan hierarkkinen riippuvuus. Tämä riippuvuus kulkee ylhäältä alaspäin. Jos järjestelmä havaitsee virheitä, kun se käsittelee tilaa, laskelman tila palautetaan aiempaan tilaan. Kaikki myöhemmät prosessin uudelleenyritykset jatkavat epäonnistuneesta tilasta eteenpäin. Tämä vaihtoehto tarjoaa seuraavat edut:

- Käyttäjä näkee koko tilan, jossa virhe on esiintynyt.
- Tietojen turmeltuminen vältetään. Esimerkiksi vanhassa laskelman kirjaamistoiminnossa oli tapauksia, joissa jotkin myyntitilaukset laskutettiin, mutta toiset jätettiin avoimiksi. Joissain maksukirjauskansioissa oli myös tapauksia, joissa täsmäytettävää laskua ei löytynyt laskun kirjausvirheen vuoksi.
- Käyttäjät voivat tarkastella laskelman nykyistä tilaa käyttämällä **Tilan tiedot** -painiketta laskelman **Suorituksen tiedot** -ryhmässä. Tilan tiedot -sivussa on kolme osaa:

    - Ensimmäisessä osassa esitetään laskelman nykyinen tila yhdessä mahdollisen virhekoodin ja virhesanoman kanssa.
    - Toinen osa näyttää laskentaprosessin eri tilat. Visuaaliset tehosteet näyttävät tilat, jotka on suoritettu onnistuneesti, joita ei voitu suorittaa virheiden vuoksi ja joita ei ole vielä suoritettu.
    - Kolmas osa näyttää kirjausprosessin eri tilat. Visuaaliset tehosteet näyttävät tilat, jotka on suoritettu onnistuneesti, joita ei voitu suorittaa virheiden vuoksi ja joita ei ole vielä suoritettu.

Lisäksi toisen ja kolmannen osan otsikko näyttää asianmukaisen prosessin kokonaistilan.

### <a name="event-logs"></a>Tapahtumalokit

Laskelma käy läpi eri työvaiheet (esimerkiksi Luo, Laske, Tyhjennä ja Kirjaa) ja laskelman elinkaaren aikana voidaan kutsua samaa toimintoa useita kertoja. Esimerkiksi, kun laskelma luodaan ja lasketaan, käyttäjä voi tyhjentää laskelman ja laskea sen uudelleen. **Tapahtumalokit**-painike laskelman **Suorituksen tiedot** -ryhmässä tarjoaa täydellisen kirjausketjun eri toiminnoille, joita on kutsuttu laskelmassa, sekä tiedot toimintojen kutsujen ajankohdasta.

### <a name="aggregated-transactions"></a>Kootut tapahtumat

Kirjaamisen aikana käteis- ja siirtotapahtumat yhdistetään asiakkaan ja tuotteen mukaan. Näin ollen myyntitilausten ja luotujen rivien määrä pienenee. Kootut transaktiot tallennetaan järjestelmässä ja niitä käytetään myyntitilausten luomiseen. Jokainen koottu transaktio luo vastaavan myyntitilauksen järjestelmässä. 

Jos laskelmaa ei ole kirjattu kokonaan, voit tarkastella laskelman koostettuja tapahtumia. Valitse toimintoruudun **Laskelma**-välilehden **Suorituksen tiedot** -ryhmässä **Koostetut tapahtumat**.

![Koostettu tapahtuma -painike laskelmalle, jota ei ole kirjattu kokonaan.](media/aggregated-transactions.png)

Kirjattujen tiliotteiden osalta voit tarkastella koottuja tapahtumia **Kirjatut tiliotteet** -sivulla. Valitse toimintoruudussa **Kyselyt** ja valitse sitten **Koostetut tapahtumat**.

![Kirjattujen lauseiden koostettujen tapahtumien komento.](media/aggregated-transactions-posted-statements.png)

Kootun transaktion **Myyntitilauksen tiedot** -pikavälilehdessä näkyvät seuraavat tiedot:

- **Tietuetunnus** – Kootun transaktion tunnus.
- **Laskelman numero** – Laskelma, johon koottu transaktio kuuluu.
- **Päivämäärä** – Päivämäärä, jolloin koottu tapahtuma luotiin.
- **Myyntitunnus** – Myyntitilauksen tunnus, kun myyntitilaus luodaan kootusta transaktiosta. Jos tämä kenttä on tyhjä, vastaavaa myyntitilausta ei ole luotu.
- **Koostettujen rivien määrä** – Kootun transaktion ja myyntitilauksen rivien kokonaismäärä.
- **Tila** – Kootun transaktion viimeisin tila.
- **Laskun tunnus** – Myyntilaskun tunus, kun kootun transaktion myyntitilaus laskutetaan. Jos tämä kenttä on tyhjä, myyntitilauksen laskua ei ole kirjattu.
- **Virhekoodi** – Tämä kenttä määritetään, jos koostamisen tilana on virhe.
- **Virhesanoma** – Tämä kenttä määritetään, jos koostamisen tilana on virhe. Se sisältää tietoja siitä, mikä on aiheuttanut prosessin epäonnistumisen. Voit korjata ongelman virhekoodin tietojen avulla ja käynnistää prosessin sitten manuaalisesti uudelleen. Koostettu myynti on ehkä poistettava ja käsiteltävä uudella laskelmalla ratkaisutyypin mukaan.

![Yhdistetyn tapahtuman myyntitilausten tiedot -pikavälilehden kentät.](media/aggregated-transactions-error-message-view.png)

Kootun taphtuman **Tapahtuman tiedot** -pikavälilehdessä näkyvät kaikki tapahtumat, jotka on tuotu koottuun tapahtumaan. Kootun tapahtuman kootuilla riveillä näkyvät kaikki tapahtumien kootut tietueet. Kootuilla riveillä näkyy myös tietoja, kuten nimike, malli, määrä, hinta, nettosumma, yksikkö ja varasto. Kukin koottu rivi vastaa yleisesti yhtä myyntitilausriviä.

![Koostettujen tapahtumien tapahtumatiedot -pikavälilehti.](media/aggregated-transactions-sales-details.png)

Joissakin tilanteissa koostettuihin tapahtumiin saattaa epäonnistua konsolidoidun myyntitilauksen kirjaaminen. Näissä tilanteissa laskelman tilaan liittyy virhekoodi. Jos haluat tarkastella vain koostettuja tapahtumia, joissa on virheitä, voit ottaa **Näytä vain epäonnistuneet** -suodattimen käyttöön yhdistettyjen tapahtumien näkymässä valitsemalla valintaruudun. Ottamalla suodattimen käyttöön voit rajoittaa tulokset yhteenlasketuille tapahtumille, joissa on virheitä, jotka edellyttävät ratkaisua. Lisätietoja näiden virheiden korjaamisesta löydät kohdasta [asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen](edit-order-trans.md).

![Näytä vain epäonnistuneet -suodattimen valintaruutu koostettujen tapahtumien näkymässä.](media/aggregated-transactions-failure-view.png)

**Kootut tapahtumat** -sivulla voit ladata tietyn kootun tapahtuman XML:n valitsemalla **Vie kootut tiedot**. Voit tarkastella XML-muotoa missä tahansa XML-muotoilussa, kun haluat nähdä myyntitilauksen luontiin ja kirjaamiseen liittyvät todelliset tiedot. Koottujen tapahtumien XML:n lataustoiminto ei ole käytettävissä laskelmille, jotka on kirjattu.

![Vie koostetut tiedot -painike Koostetut tapahtumat -sivulla.](media/aggregated-transactions-export.png)

Jos et voi korjata virhettä korjaamalla myyntitilauksen tai myyntitilausta tukevan tiedon, **Asiakkaan tilauksen poistaminen** -painike on käytettävissä. Jos haluat poistaa tilauksen, valitse epäonnistunut koostettu tapahtuma ja valitse sitten **Poista asiakastilaus**. Sekä koostettu transaktio että vastaava myyntitilaus poistetaan. Voit nyt tarkistaa tapahtumat käyttämällä muokkaus- ja kirjaustoimintoja. Vaihtoehtoisesti ne voidaan käsitellä uudelleen uudella laskelmalla. Kun kaikki viat on korjattu, voit jatkaa laskelman kirjaamista suorittamalla laskelman kirjaustoiminnon.

![Poista asiakastilauspainike koostettujen tapahtumien näkymässä.](media/aggregated-transactions-delete-cust-order.png)

Koottujen tapahtumien näkymä tarjoaa seuraavat edut:

- Käyttäjä näkee kootut tapahtumat, jotka epäonnistuivat myyntitilauksen luonnin aikana, sekä myyntitilaukset, jotka epäonnistuivat laskutuksen aikana.
- Käyttäjä näkee, kuinka tapahtumat kootaan.
- Käyttäjällä on täydellinen kirjausketju aina tapahtumista myyntitilauksiin ja myyntilaskuihin. Tätä kirjausketjua ei ollut käytettävissä vanhassa laskelman kirjaamistoiminnossa.
- Koottu XML-tiedosto helpottaa ongelmien tunnistamista myyntitilauksen luonnin ja laskutuksen yhteydessä.

### <a name="journal-vouchers"></a>Kirjaustositteet

**Kirjaustositteet**-painike laskelman **Suorituksen tiedot** -ryhmässä näyttää kaikki eri tositetapahtumat, jotka on luotu laskelmaa varten ja jotka liittyvät alennuksiin, tuotto- ja kulutileihin, lahjakortteihin ja niin edelleen.

Tällä hetkellä ohjelma näyttää nämä tiedot vain kirjattuja laskelmia varten.

### <a name="payment-journals"></a>Maksukirjauskansiot

**Maksukirjauskansiot**-painike laskelman **Suorituksen tiedot** -ryhmässä näyttää kaikki eri maksukirjauskansiot, jotka on luotu laskelmaa varten.

Tällä hetkellä ohjelma näyttää nämä tiedot vain kirjattuja laskelmia varten.

## <a name="other-improvements"></a>Muut parannukset

Laskelman kirjaamistoimintoon on tehty muita taustajärjestelmän parannuksia, jotka ovat näkyvissä käyttäjälle. Seuraavassa on muutamia esimerkkejä:

- Kooste ei huomioi henkilöstön, päätteen ja vuoron yksiköitä. Koska koosteparametreja on vähemmän, käsiteltäviä myyntitilausrivejä on vähemmän.
- Tapahtumatauluissa esiintyviä lukkiutumisia on vähennetty laajennustauluilla ja tapahtumien taulujen lisäystoiminnoilla päivitystoimintojen sijaan.
- Suoritettavien erätehtävien määrä on parametroitu ja rajoitettu. Tätä määrää voidaan siten hienosäätää asiakkaan ympäristön mukaan. Vanhassa laskelman kirjaustoiminnossa luotiin samalla kertaa rajaton määrä erätehtäviä. Se aiheutti hallitsemattomia kuormia, yleiskustannuksia ja pullonkauloja eräpalvelimessa.
- Laskelmien käsittelyn jonotus hoidetaan tehokkaasti priorisoimalla laskelmat, joissa on suurin määrä tapahtumia.
- Eräprosessit, kuten **Laskelmien laskenta eräajona** ja **Laskelmien kirjaaminen eräajona** suoritetaan vain erätilassa. Vanhassa laskelmien kirjaamistoiminnossa käyttäjät voivat suorittaa näytä eräprosesseja vuorovaikutteisessa tilassa, joka on yksisäikeinen toiminto toisin kuin eräprosessit, jotka ovat monisäikeisiä.
- Vanhassa laskelman kirjaustoiminnossa erätehtävän virheet asettivat koko erätyön virhetilaan. Parannetussa toiminnon erätehtävän virheet eivät aseta erätyötä virhetilaan, jos muut erätehtävät on suoritettu onnistuneesti. Sinun tulee arvioida erän suoritusajon kirjaustila käyttämällä **Laskelmat**-sivua, jossa voit tarkastella kaikkia laskelmia, joita ei ole kirjattu virheiden vuoksi.
- Vanhassa laskelman kirjaustoiminnossa laskelman virheen ensimmäinen esiintymä aiheutti koko erän epäonnistumisen. Jäljellä olevia laskelmia ei käsitelty. Parannetussa toiminnossa eräkäsittely jatkaa kaikken laskelmien käsittelyä, vaikka osa laskelmista epäonnistuu. Yksi etu on, että käyttäjät näkevät tarkasti niiden tiliotteiden määrän, joissa on virheitä. Tällöin käyttäjien ei tarvitse jäädä silmukkaan, jossa virheitä korjataan ja laskelmaprosessi suoritetaan, kunnes kaikki laskelmat on kirjattu.

## <a name="general-guidance-about-the-statement-posting-process"></a>Yleisiä ohjeita laskelman kirjausprosessia varten

- On suositeltavaa suorittaa laskelman kirjausprosessi eränä, koska eräajo hyödyntää monisäikeisen järjestelmän tehokkuutta. Monisäikeisyyttä tarvitaan, jotta voidaan käsitellä valtavia tapahtumamääriä, jotka ovat yleisiä laskelmien kirjauksissa.
- On suositeltavaa, että otat käyttöön negatiivisen fyysisen varaston nimikemalliryhmässä, jotta kirjauskokemus on saumaton. Joissakin tilanteissa negatiivisia laskelmia ei ehkä voi kirjata, ellei negatiivista fyysistä varastoa ole. Esimerkiksi teoriassa, jos varastossa on vain yksi kappale nimikettä ja sille on tehty myyntitapahtuma ja palautustapahtuma, tapahtumaan pitäisi voida kirjata, vaikka negatiivinen varasto ei ole käytössä. Koska laskelman kirjausprosessi ottaa sekä myyntitapahtuman että palautustapahtuman samaan asiakastilaukseen, ei voida kuitenkaan taata, että myyntirivi kirjataan ensin ja palautusrivi sen jälkeen. Tällöin voi ilmetä virheitä. Jos negatiivinen varasto on käytössä tässä tilanteessa, tapahtuman kirjaus ei vaikuta negatiivisesti ja järjestelmä näyttää varaston oikein.
- On suositeltavaa käyttää koostamista laskelmia laskettaessa ja kirjattaessa. Suosittelemme siksi seuraavia asetuksia joitakin koostamisparametreja varten:

    - Siirry kohtaan **Vähittäismyynti ja kauppa** \> **Pääkonttorin asetukset** \> **Parametrit** \> **Kaupan parametrit**. Valitse sitten **Kirjaus**-välilehdellä **Varastopäivitys**-pikavälilehden **Erittelytaso**-kentässä **Yhteenveto**.
    - Siirry kohtaan **Vähittäismyynti ja kauppa** \> **Pääkonttorin asetukset** \> **Parametrit** \> **Kaupan parametrit**. Aseta sitten **Kirjaus**-välilehden **Koostaminen**-pikavälilehdessä **Tositetapahtumat**-asetukseksi **Kyllä**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
