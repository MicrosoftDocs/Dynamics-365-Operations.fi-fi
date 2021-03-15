---
title: Sarjoitettujen nimikkeiden käyttäminen myyntipisteessä
description: Tässä ohjeaiheessa selitetään, kuinka sarjoitettuja nimikkeitä hallitaan myyntipisteen (POS) sovelluksessa.
author: boycezhu
manager: annbe
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 0431ffa45eceac5c12d8ed991b00730c50ca62f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972552"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Sarjoitettujen nimikkeiden käyttäminen myyntipisteessä

[!include [banner](includes/banner.md)]

Monet jälleenmyyjät myyvät tuotteita, jotka edellyttävät sarjavalvontaa. Näitä tuotteita kutsutaan *sarjoitetuiksi nimikkeiksi*. Jotkin vähittäismyyjät haluavat ehkä ylläpitää sarjanumeroita myymälässä tai varastossa seurantaa varten. Muut jälleenmyyjät saattavat haluta kaapata sarjanumeroita myyntiprosessin aikana huoltoa ja takuuta varten. Tässä ohjeaiheessa selitetään, kuinka voit hallita sarjoitettuja nimikkeitä Microsoft Dynamics 365 Commerce -myyntipisteen (POS) sovelluksessa.

## <a name="serial-number-configurations"></a>Sarjanumerokonfiguraatiot

Nimikettä pidetään sarjoitettuna nimikkeenä, jos sille on määritetty sarjanumeroiden sallimiseksi määritetty seurantadimensioryhmä. Valitse Commerce Headquarters -sovelluksen **Seurantadimensioryhmät**-sivulla **Aktiivinen**-vaihtoehto, jos haluat ottaa käyttöön sarjanumerot varastoprosessissa. Vaihtoehtoisesti voit valita **Aktiivinen myyntiprosessissa** -vaihtoehdon, jos haluat ottaa käyttöön sarjanumerot myyntiprosessissa.

Ota **Tyhjä kuitti sallittu** -vaihtoehto käyttöön **Seurantadimensiot**-pikavälilehdessä. Tällöin sarjanumero on valinnainen syöte sarjoitetun nimikkeen varaston vastaanottoprosessin aikana. Jos tämä parametri poistetaan käytöstä, sarjanumerolle on annettava syöte. Vastaavasti **Tyhjä varasto-otto sallitaan** -parametri ohjaa sarjanumeroiden määrittämistä pakolliseksi varaston lähetysprosessin aikana.

> [!NOTE]
> Jos haluat käyttää **Saapuva varasto**- ja **Lähtevä varasto** -myyntipistetoimintoja sarjanumeroiden rekisteröimisessä tai vahvistamisessa sarjoitetulle nimikkeelle, määritä kyseinen nimike seurantadimensioryhmää varten. Ryhmä on määritettävä sallimaan sarjanumerot **Aktiivinen**-vaihtoehdolle, ei **Aktiivinen myyntiprosessissa** -vaihtoehdolle.

## <a name="serial-number-management-page"></a>Sarjanumeroiden hallinta -sivu

Jos valittu, vastaanotettu tai lähetetty nimike on sarjoitettu nimike **Saapuva varasto**- ja **Lähtevä varasto** -myyntipistetoiminnoissa, **Tiedot**-ruutu sisältää **Hallinnoi sarjanumeroa** -vaihtoehdon, joka sisältää linkin **Sarjanumeroiden hallinta** -sivulle. Sivulla voit rekisteröidä nimikkeen sarjanumerot tai vahvistaa ne. Vaihtoehtoisesti voit avata **Sarjanumeroiden hallinta** -sivun joko valitsemalla tilaustietojen näkymän sovelluspalkin **Sarjanumero**-toiminnon tai valitsemalla **Hallitse sarjanumeroa** -vaihtoehdon valintaikkunassa, joka pyytää käyttäjää vastaamaan vastaanotto- tai lähetysprosessin aikana. 

**Sarjanumeroiden hallinta** -sivulla luetellaan kaikki avoimet sarjanumerorivit, jotka odottavat rekisteröintiä tai vahvistusta. Tällä sivulla voi olla seuraavat kaksi välilehteä: yksi nykyiselle nimikkeelle ja yksi tilauksen sarjoitettuja nimikkeitä varten.

**Sarjanumeroiden hallinta** -sivun **tila**-kentässä on tietoja nykyisestä vaiheesta, jossa kukin sarjanumero on:

- **Ei rekisteröity** – Sarjanumeroa ei ole annettu tai esirekisteröityä sarjanumeroa ei ole vielä vahvistettu (vastaanottoprosessissa).
- **Rekisteröityminen** – Sarjanumero on rekisteröity ja tallennettu paikallisesti myymälän kanavatietokantaan tai esirekisteröity sarjanumero on vahvistettu. Vain sarjanumerot, joiden tila on **Rekisteröityminen**, lähetetään Commerce Headquarters -sovellukseen, kun vastaanotto tai täytäntöönpano on valmis.

## <a name="receive-serialized-items"></a>Sarjoitettujen nimikkeiden vastaanottaminen

**Saapuva varasto** -myyntipistetoiminto antaa käyttäjien suorittaa seuraavat sarjoitetuille kohteille tehtävät toimet:

- Rekisteröi sarjanumerot sarjasarjoitettuja nimikkeitä vastaan, kun nimikkeet vastaanotetaan myymälässä ostotilauksen kautta.
- Vahvista ennalta rekisteröidyt sarjanumerot sarjasarjoitettuja nimikkeitä vastaan, kun nimikkeet vastaanotetaan myymälässä ostotilauksen kautta tai siirrä tilaus.

### <a name="register-serial-numbers-against-serialized-items"></a>Sarjanumeroiden rekisteröiminen sarjoitettuja nimikkeitä vasten

Jos kyseessä on ostotilaus, käyttäjälle näytetään valintaikkuna, joka sisältää **Hallinnoi sarjanumeroa** -vaihtoehdon sarjoitetun nimikkeen vastaanottoprosessin aikana. Voit valita tämän vaihtoehdon, kun haluat avata **sarjanumeroiden hallinta** -sivun ja alkaa rekisteröidä sarjanumeroita. Voit myös ohittaa tämän vaiheen vastaanottoprosessin aikana ja antaa syötteen myöhemmin ennen vastaanoton kirjaamista.

Oletusarvon mukaan näytetään nykyisen nimikkeen välilehti. Kaikilla sarjanumeroriveillä on tyhjä sarjanumeroarvo ja tila, jota **ei ole rekisteröity**. Voit skannata sarjanumeroviivakoodeja tai voit määrittää **sarjanumerot** jatkuvasti valitsemalla sarjanumeron sovelluspalkista. Syöttämäsi sarjanumerot näkyvät luettelossa, ja niiden tilaksi tulee **Rekisteröinti**. Luettelossa rekisteröitävien sarjanumeroiden enimmäismäärä on sama kuin vastaanottava määrä. Jos teet virheen, voit tehdä muutoksia syöttämääsi sarjanumeroon valitsemalla **Muokkaa** tai **Tyhjennä** **Tieto**-ruudusta.

Sarjanumerot voi rekisteröidä myös **sarjanumeroiden hallinta** -sivun **kaikki sarjoitetut nimikkeet** -välilehdessä. Valitse luettelosta nimike, jota vastaan haluat rekisteröidä sarjanumerot.

### <a name="validate-serial-numbers-on-serialized-items"></a>Sarjoitetussa nimikkeissä olevien sarjanumeroiden vahvistaminen

Siirtotilauksen lähtevän puolen on suoritettava sarjanumerot sarjoitetussa nimikkeissä lähetysprosessin aikana. Jos kyseessä on ostotilaus, toimittaja voi antaa sarjanumerotiedot ennakkolähetysilmoituksen (ASN) kautta, ja voit määrittää toimitettavien nimikkeiden numerot. Molemmissa tapauksissa sarjanumerot ovat tiedossa ennen vastaanottoa. Siksi saapuvien puolella, sinun täytyy vain vahvistaa, että olet saanut mitä oli tarkoitus saada.

Voit vahvistaa sarjanumerot avaamalla **Sarjanumeroiden hallinta** -sivun joko vastaanottavan prosessin aikana tai milloin tahansa ennen vastaanoton kirjaamista. Kaikille sarjanumeroille määritetään automaattisesti alkutila, jota **ei ole rekisteröity** tällä sivulla, kullekin sarjoitetun nimikkeen sarjanumerolle. Voit tarkistaa sarjanumerot skannaamalla tai kirjoittamalla ne. Kun sarjanumero on määritetty, sovellus tarkistaa, vastaavatko ne ennalta rekisteröityjä sarjanumeroita. Jos ne täsmäävät, niiden tilaksi muutetaan **Rekisteröityminen**. Muussa tapauksessa näyttöön avautuu virhesanoma. Vaihtoehtoisesti voit valita sarjanumeron suoraan ja valita sitten **Vahvista sarjanumero** -vaihtoehdon **Tiedot**-ruudussa. Näin voit merkitä sarjanumeron nopeasti vahvistetuksi. Luettelossa vahvistettavien sarjanumeroiden enimmäismäärä on sama kuin vastaanottava määrä.

Sarjanumerot voi vahvistaa myös **sarjanumeroiden hallinta** -sivun **kaikki sarjoitetut nimikkeet** -välilehdessä. Valitse luettelosta nimike, jota vastaan haluat vahvistaa sarjanumerot.

## <a name="ship-serialized-items"></a>Sarjoitettujen nimikkeiden lähettäminen

**Lähtevä varasto** -myyntipistetoiminnon avulla käyttäjä voi rekisteröidä sarjanumeroita sarjoitetuille nimikkeille, kun niitä lähetetään nykyisestä myymälästä siirtotilauksen kautta.

### <a name="register-serial-numbers-against-serialized-items"></a>Sarjanumeroiden rekisteröiminen sarjoitettuja nimikkeitä vasten

Jos kyseessä on siirtotilaus, käyttäjälle näytetään valintaikkuna, joka sisältää **Hallinnoi sarjanumeroa** -vaihtoehdon sarjoitetun nimikkeen lähetysprosessin aikana. Voit valita vaihtoehdon, kun haluat avata **Sarjanumeroiden hallinta** -sivun ja alkaa rekisteröidä sarjanumeroita. Voit myös ohittaa tämän vaiheen lähetysprosessin aikana ja antaa syötteen myöhemmin ennen lähetyksen kirjaamista.

Oletusarvon mukaan näytetään nykyisen nimikkeen välilehti. Kaikilla sarjanumeroriveillä on tyhjä sarjanumeroarvo ja tila, jota **ei ole rekisteröity**. Voit skannata sarjanumeroviivakoodeja tai voit määrittää **sarjanumerot** jatkuvasti valitsemalla sarjanumeron sovelluspalkista. Syöttämäsi sarjanumerot näkyvät luettelossa, ja niiden tilaksi tulee **Rekisteröinti**. Luettelossa rekisteröitävien sarjanumeroiden enimmäismäärä on sama kuin lähetysmäärä. Jos teet virheen, voit tehdä muutoksia syöttämääsi sarjanumeroon valitsemalla **Muokkaa** tai **Tyhjennä** **Tieto**-ruudusta.

Sarjanumerot voi rekisteröidä myös **Sarjanumeroiden hallinta** -sivun **Kaikki sarjoitetut nimikkeet** -välilehdessä. Valitse luettelosta nimike, jota vastaan haluat rekisteröidä sarjanumerot.

Vaihtoehtoisesti voit ottaa sarjanumeroiden käytettävyyden vahvistuksen käyttöön sarjanumeroiden rekisteröinnissä lähtevälle siirtotilaukselle. Kun tämä tarkistus on käytössä ja yrität lähettää sarjanumeron, joka ei ole käytettävissä lähettävän myymälän varastossa, näyttöön tulee virhesanoma. Anna tämän jälkeen toinen numero.

Jotta tämä vahvistus voidaan ottaa käyttöön edellytyksenä, seuraavat työt on aikataulutettava suoritettavaksi toistuvasti:

- **Vähittäismyynti ja kauppa** > **Vähittäismyynnin ja kaupan IT** > **Tuotteet ja varasto** > **Tuotteiden saatavuus ja seurantadimensiot**
- **Vähittäismyynti ja kauppa** > **Jakeluaikataulut** > **1130** (**Tuotteen saatavuus**)

## <a name="sell-serialized-items-in-pos"></a>Sarjoitettujen nimikkeiden myynti myyntipisteessä

Vaikka myyntipistesovellus on aina tukenut sarjoitettujen nimikkeiden myymistä, organisaatiot voivat käyttää Commercen versiossa 10.0.17:ssä ja sitä myöhemmissä versioissa toimintoa, jotka parantavat liiketoimintalogiikkaa, joka käynnistyy sarjanumeron seurantaa varten konfiguroituja tuotteita myytäessä.

Kun **Parannettu sarjanumeroiden tarkistus myyntipisteen tilauksen tallennuksessa ja tilauksen täyttämisessä** -ominaisuus on otettu käyttöön, seuraavat tuotekonfiguraatiot arvioidaan, kun myyntipisteissä myydään sarjoitettuja tuotteita:

- Tuotteen **Sarjatyyppi**-asetukset (**aktiivinen** tai **aktiivinen myynnissä**).
- Tuotteen **Tyhjä varasto-otto sallitaan** -asetukset.
- Tuotteen ja/tai myyntivaraston **Fyysinen negatiivinen varasto** -asetukset.

### <a name="active-serial-configurations"></a>Aktiiviset sarjakonfiguraatiot

Kun nimikkeitä myydään myyntipisteessä, jossa on käytössä **Aktiivinen** sarjanumeron seurantadimensio, myyntipiste käynnistää oikeellisuustarkistuslogiikan, joka estää käyttäjiä suorittamasta myyntiä sarjanumerolle, jonka sarjanumeroa ei löydy myyntivaraston nykyisestä varastosta. Tähän oikeellisuustarkistussääntöön on kaksi poikkeusta:

- Jos nimike on myös konfiguroitu niin, että käytössä on **Tyhjä varasto-otto sallitaan** -asetus, käyttäjät voivat ohittaa sarjanumeron syötön ja myydä nimikkeen ilman sarjanumeroiden määritystä.
- Jos nimike ja/tai myyntivarasto on määritetty niin, että **Fyysinen negatiivinen varasto** on otettu käyttöön, sovellus hyväksyy ja myy sarjanumeron, jota ei voi vahvistaa olevan varastossa, josta nimike myydään. Tämän konfiguroinnin avulla tietyn nimikkeen tai sarjanumeron varastotapahtuma voi olla negatiivinen, joten järjestelmä sallii tuntemattomien sarjanumeroiden myynnin.

> [!IMPORTANT]
> Sen varmistamiseksi, että myyntipistesovellus voi tarkistaa oikein, sijaitsevatko **aktiivisten** sarjatyyppien nimikkeiden sarjanumerot myyntivarastossa, edellyttää, että organisaatiot suorittavat **Tuotteiden saatavuus ja seurantadimensiot** -työn Commerce headquarters -ohjelmassa sekä liittyvän tuotteen saatavuuden jakelun **1130**-työn Commerce headquarters -sovelluksessa säännöllisesti. Koska uusi sarjoitettu varasto vastaanotetaan myytäviin varastoihin, myyntipisteen on tarkistettava myytävien sarjanumeroiden varastosaatavuus, ja tähän päästään siten, että varaston päärekisterin on päivitettävä kanavan tietokantaan viimeisimmät varaston käytettävyystiedot säännöllisesti. **Tuotteiden saatavuus ja seurantadimensiot** -työ ottaa nykyisen vedoksen päävarastosta, mukaan lukien sarjanumerot, kaikille yrityksen varastoille. **1130**-jakelutyö vie tämän varaston tilannevedoksen ja jakaa sen kaikkien konfiguroitujen kanavatietokantojen kanssa.

### <a name="active-in-sales-process-serial-configurations"></a>Aktiivinen myyntiprosessissa -sarjamääritykset

Nimikkeet, joilla on sarjadimensio on **Aktiivinen myyntiprosessissa**, eivät käy läpi varaston oikeellisuustarkistuslogiikkaa, koska tämä konfigurointi tarkoittaa, että varaston sarjanumeroita ei ole esirekisteröity varastoon, ja sarjanumerot siepataan vain myyntihetkellä.  

Jos **Aktiivinen myyntiprosessissa** -konfiguroiduille nimikkeille määritetään myös **Tyhjä varasto-otto sallitaan**, sarjanumeron syöttö voidaan ohittaa. Jos **Tyhjä varasto-otto sallitaan** -asetusta ei konfiguroida, sovellus edellyttää, että käyttäjä antaa sarjanumeron, vaikka sitä ei voida tarkistaa käytettävissä olevan varaston perusteella.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>Sarjanumeroiden kohdistaminen myyntipistetapahtumien luonnin aikana

Myyntipistesovellus kehottaa välittömästi käyttäjiä sarjanumeroiden siepaamiseen myytäessä sarjoitettua nimikettä, mutta sovelluksen avulla käyttäjät voivat ohittaa sarjanumeroiden syöttämisen tiettyyn myyntiprosessin vaiheeseen asti. Kun käyttäjä aloittaa maksun siepauksen, sovellus pakottaa ja vaatii sarjanumeron syöttämisen nimikkeille, joita ei ole määritetty täyttämään tulevia lähetyksiä tai noutoja. Kaikki itsepalvelutukkua tai liikkestä noutoa varten määritetyt sarjoitetut nimikkeet edellyttävät, että käyttäjä tallentaa sarjanumeron (tai hyväksyy sen jättämisen tyhjäksi, jos nimikkeen konfiguraatio sallii sen) ennen myynnin viimeistelyä.

Myyntipisteen käyttäjät voivat jättää sarjanumeron syöttämisen väliin alustavasti ja tehdä asiakkaan tilauksen luonnin valmiiksi, kun sarjoitetut nimikkeet myydään tulevaa noutoa tai lähetystä varten.   

> [!NOTE]
> Kun sarjoitettuja tuotteita myydään tai täytetään myyntipistesovelluksessa, määrä "1" pakotetaan myyntitapahtuman sarjoitettuihin nimikkeisiin. Tämä on tulos siitä, miten sarjanumerotietoja seurataan myyntirivillä. Kun myydään tai täytetään tapahtumaa useille sarjoitettuille nimikkeille myyntipisteen kautta, kullekin myyntiriville on määritettävä määräksi "1". 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Sarjanumeroiden kohdistaminen asiakkaan tilauksen täyttämisen tai noudon yhteydessä

Kun sarjoitettujen tuotteiden asiakastilausrivit täytetään myyntipisteen **Tilauksen täyttäminen** -toiminnon avulla, myyntipiste pakottaa sarjanumeron siepauksen ennen lopullista täyttämistä. Jos siis ei ole annettu sarjanumeroa alkuperäisessä tilauksen sieppaamisessa, se on siepattava myyntipisteen nouto-, pakkaus- tai lähetysprosessien aikana. Oikeellisuustarkistus tehdään jokaisessa vaiheessa, ja käyttäjältä pyydetään sarjanumerotiedot vain, jos ne puuttuvat tai eivät enää ole voimassa. Jos käyttäjä esimerkiksi ohittaa nouto- tai pakkausvaiheet ja aloittaa lähetyksen heti eikä riville ole rekisteröity sarjanumeroa, myyntipiste edellyttää sarjanumeron syömistä ennen lopullisen laskuvaiheen valmistumista. Kun pakotetaan sarjanumeron sieppaus myyntipisteen tilauksen täyttämistoimintojen aikana, kaikki edellä tässä ohjeaiheessa mainitut säännöt ovat voimassa. Vain **aktiiviseksi** määritetyt sarjoitetut nimikkeet käyvät läpi sarjanumeron varaston oikeellisuustarkistuksen. **Aktiivinen myyntiprosessissa** -konfiguroituja nimikkeitä ei tarkisteta. Jos **aktiivisten** tuotteiden **Fyysinen negatiivinen varasto** sallitaan, mikä tahansa sarjanumero hyväksytään varaston saatavuudesta riippumatta. Sekä **Aktiivinen**- että **Aktiivinen myyntiprosessissa** -nimikkeille käyttäjä voi jättää sarjanumerot haluttaessa tyhjiksi nouto-, pakkaus- ja lähetysvaiheissa, jos **Tyhjä varasto-otto sallitaan** on määritetty.

Sarjanumeroiden oikeellisuustarkistuksia tehdään myös silloin, kun käyttäjä suorittaa noutotoimintoja myyntipisteen asiakastilauksissa. Myyntipistesovellus ei salli sarjoitettuun tuotteeseen poiminnan viimeistelyä, ennen kuin se läpäisee oikeellisuustarkistukset aiemmin mainitulla tavalla. Oikeellisuustarkistukset perustuvat aina tuotteen seurantadimensioon ja myyntivaraston konfiguraatioihin. 

## <a name="additional-resources"></a>Lisäresurssit

[Myyntipisteen saapuva varastotoiminto](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Myyntipisteen lähtevä varastotoiminto](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)


[!INCLUDE[footer-include](../includes/footer-banner.md)]