---
title: Monikanavamaksujen yleiskatsaus
description: Tässä artikkelissa on yhteenveto Omni-Channel-maksuista Dynamics 365 Commercessa.
author: BrianShook
ms.date: 09/17/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom:
- "141393"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: d850e532a764d22bc926f5649f4ad2907b49d1a0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881706"
---
# <a name="omni-channel-payments-overview"></a>Monikanavamaksujen yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yhteenveto Omni-Channel-maksuista Dynamics 365 Commercessa. Se sisältää kattavan luettelon tuetuista skenaarioista, tietoja toiminnoista, asetuksista ja vianmäärityksestä sekä joidenkin tavallisten ongelmien kuvauksia.

## <a name="key-terms"></a>Tärkeimmät termit

| Kausi | Kuvaus |
|---|---|
| Tunnus | Tietomerkkijono, jonka maksukäsittelijä antaa viitteenä. Tunnukset voivat edustaa maksukorttien numeroita, maksujen varmennuksia ja aiempia maksuja. Tunnukset ovat tärkeitä, koska ne auttavat pitämään luottamukselliset tiedot poissa myyntipisteen (POS) järjestelmästä. Niitä kutsutaan joskus myös *viitteiksi*. |
| Kortin tunnus | Tunnus, jota maksujen käsittelytoiminto tarjoaa varastoon myyntipistejärjestelmässä. Korttitunnusta voi käyttää vain sen vastaanottava kauppias. Korttitunnuksia kutsutaan joskus myös *korttiviitteiksi*. |
| Varmennussanake | Yksilöivä tunnus, jota maksuprosessi tarjoaa osana POS-järjestelmään lähettämäänsä vastausta, kun POS-järjestelmä tekee valtuutuspyynnön. Valtuutustietotunnusta voi käyttää myöhemmin, jos suoritinta kutsutaan suorittamaan toimintoja, kuten peruutettaessa tai mitätöidessä valtuutusta. Sitä käytetään kuitenkin useimmiten varojen sieppaamiseen, kun tilaus täyttyy tai tapahtuma viimeistellään. Valtuutuksen tunnuksia kutsutaan joskus myös *Valtuutuksen viitteiksi*. |
| Sieppauksen tunnus | Viite, jonka maksukäsittelijä tarjoaa POS-järjestelmälle, kun maksu viimeistellään tai siepataan. Tämän jälkeen voit käyttää sieppaustunnusta, kun haluat viitata maksun sieppaamiseen seuraavissa toiminnoissa, kuten hyvityspyynnöissä. | 
| Kortti ei ole paikalla | Termi, joka viittaa maksutapahtumiin, joissa fyysistä korttia ei ole esitetty. Tällaisia tapahtumia voivat olla esimerkiksi sähköinen kaupankäynti tai Call Center -skenaariot. Näitä tapahtumia varten maksuun liittyvät tiedot syötetään manuaalisesti sähköisen kaupankäynnin Internet-sivustoon, puhelukeskuksen työnkulkuun tai POS- tai maksupäätteelle. |
| Kortti paikalla | Termi, joka viittaa maksutapahtumiin, joissa fyysinen kortti esitetään ja jota käytetään Microsoft Dynamics 365 POS -järjestelmään liitetyssä maksupäätteessä. |

## <a name="overview"></a>Yleiskuvaus

Yleensä termi *Omni-Channel-maksu* kuvaa mahdollisuutta luoda tilauksen yhdellä kanavalla ja täyttää sen toisella kanavalla. Omni-Channel-tuki tuen avain on, että maksut säilyvät yhdessä muiden tilaustietojen kanssa ja että näitä maksuja koskevia tietoja käytetään, kun tilaus palautetaan tai sitä käsitellään toisessa kanavassa. Klassinen esimerkki on "Osta verkosta, nouda myymälästä" -skenaario. Tässä skenaariossa maksutiedot lisätään, kun tilaus luodaan verkossa. Tämän jälkeen ne palautetaan myyntipisteessä asiakkaan maksukortin veloittamiseksi noutohetkellä. 

Kaikki tässä artikkelissa kuvatut skenaariot voidaan toteuttaa Kauppa-ohjelmiston vakiomaksuohjelmiston kehityspaketin (SDK) avulla. [Adyen-järjestelmän Dynamics 365 -maksuyhdysliitin](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) sisältää kaikki tässä kuvatut skenaariot. 

### <a name="prerequisites"></a>Edellytykset

Kaikissa tässä artikkelissa kuvatuissa skenaarioissa on määritettävä maksuyhteys, joka tukee Omni-Channel-maksuja. Myös valmiiksi määritettyä Adyen-liitintä voidaan käyttää, koska se tukee skenaarioita, jotka ovat käytettävissä Payments SDK:n kautta. Lisätietoja maksuyhdistimien toteuttamisesta ja Retail SDK:sta yleensä on [IT-ammattilaisten ja -kehittäjien kotisivulla](/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors).

#### <a name="supported-versions"></a>Tuetut versiot

Tässä artikkelissa kuvatut Omni-Channel-maksuominaisuudet on julkaistu osana Microsoft Dynamics 365 for Retail -versiota 8.1.3. 

#### <a name="card-present-and-card-not-present-connectors"></a>Kortti on käytössä ja Kortti ei ole käytössä -yhdistimet

Payments SDK sisältää kaksi maksuille tarkoitettua ohjelmointirajapinta (API) -liittymää. Ensimmäinen ohjelmointirajapinta on nimeltään **iPaymentProcessor**. Sitä käytetään toteuttamaan "kortti ei ole paikalla -maksuyhdistimiä, joita voidaan käyttää Call Center- ja Microsoft Dynamics e-Commerce-alustalla. Lisätietoja **iPaymentProcessor**-käyttöliittymästä on [Toteuta maksuyhteys-ja maksulaite](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf) -valkoisessa kirjassa, joka kattaa maksut. 

Toinen ohjelmointirajapinta on nimeltään **iNamedRequestHandler**. Se tukee Kortti on paikalla maksuintegraatioita, jotka käyttävät maksupäätettä. Lisätietoja **iNamedRequestHandler**-liittymästä on kohdassa [Maksuintegroinnin luominen maksupäätteelle](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension). 

### <a name="setup-and-configuration"></a>Asetukset ja määrittäminen

Seuraavat komponentit ja asetusvaiheet ovat pakollisia:

- **eCommerce-integrointi**: Kauppaintegroinnin on tuettava tilanteita, joissa tilauksen lähtöpaikka on online-myymälä. Lisätietoja Retail e-Commerce SDK:sta on kohdassa [Sähköisen kaupankäynnin Platform Software Development Kit (SDK)](/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk). Demo-ympäristössä viitemyymälä tukee Omni-Channel-maksuskenaarioita. 
- **Online-maksun määritys**: Online-kanavan asetusten on sisällettävä maksuyhteys, joka on päivitetty tukemaan Omni-Channel-maksuja. Vaihtoehtoisesti voidaan käyttää käyttövalmista maksuyhdistintä. Lisätietoja Adyen-maksuyhdistimestä verkkokauppojen konfiguroinnissa on kohdassa [Adyen-maksuyhdistin](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce). Tässä artikkelissa kuvattujen verkkokaupan määritysvaiheiden lisäksi **Salli säästö tiedot e-Commerce** -parametrin asetuksen arvoksi on määritettävä **Tosi** Adyen-liittimen asetuksissa. 
- **Omni-Channel-maksujen konfiguraatio**: Siirry taustajärjestelmäsovelluksessa kohtaan **Vähittäismyynti ja kauppa \> Headquarters-sovelluksen asetus \> Parametrit \> Kaupan jaetut parametrit**. Aseta sitten **Omni-Channel-maksujen** -välilehdessä **Käytä Omni-Channel-maksuja** -asetukseksi **Kyllä**. Commercen versiossa 10.0.12 ja uudemmissa versioissa tämä asetus on **Ominaisuuksien hallinta** -työtilassa. Valitse **Monikanavan maksut** -ominaisuus ja valitse sitten **Ota käyttöön nyt**. 
- **Maksupalvelut:** Call center käyttää **Maksupalvelut**-sivun oletusmaksuyhdistintä maksujen käsittelemiseen. Jos haluat tukea skenaarioita, kuten Osta call centeristä, poimi myymälästä, tämän oletusmaksuyhdistimen on oltava Adyen-maksuyhdistin tai maksuyhdistin, joka täyttää Omni-Channel-maksuissa käytettävät toteutusvaatimukset.
- **EFT-palvelu**: Maksupäätteen kautta suoritettavat maksut on määritettävä laitteistoprofiilin **EFT-palvelu**-pikavälilehdessä. Adyen-yhdistin tukee käyttövalmiita Omni-Channel-maksuskenaarioita. Myös muita **iNamedRequestHandler**-maksuyhdistimiä voidaan käyttää, jos ne tukevat Omni-Channel-maksuja.
- **Maksuyhteyden käytettävyys:** Kun tilaus palautetaan, maksuvälineriveihin, jotka palautetaan yhteen tilauksen kanssa, kuuluu sen maksuyhteyden nimi, jota käytettiin tähän tilaukseen liittyvien lupien luomisessa. Kun tilaus on täytetty, maksun SDK yrittää käyttää samaa yhdistintä, jota käytettiin alkuperäisen valtuutuksen luomisessa. Näin ollen on oltava käytettävissä kaappaamiseen myös sellainen maksuyhdistin, jolla on samat kauppiasominaisuudet. 
- **Korttityypit:** Jotta Omni-Channel-skenaariot toimivat oikein, kullakin kanavalla on oltava samat maksuvälinetyyppien määritykset, joita voidaan käyttää Omni-kanavalla. Tämä asetus sisältää maksutapatunnukset ja korttityypin tunnukset. Jos esimerkiksi **Kortti**-maksuvälinetyypin tunnus on **2** Internet-kaupan määrityksissä, sen tunnuksen tulee olla sama kuin vähittäiskaupan määrityksissä. Sama vaatimus koskee korttien tyyppitunnuksia. Jos kortin numero **12** arvoksi on asetettu verkkokaupassa **VISA**, sama tunnus on määritettävä vähittäismyymälälle. 
- Retail Modern POS for Windows tai Android ja sisäänrakennettu laiteasema tai
- Modern POS for iOS tai Cloud POS ja yhdistetty, jaettu laiteasema. 

### <a name="basic-principle-supporting-omni-channel-payments"></a>Omni-Channel-maksuja tukeva perusperiaate

Maksuyhdistimet ja maksuprosessorit käyttävät tunnuksia tai viittauksia korttimaksuihin liittyviin tapahtumiin. Jos esimerkiksi haetaan maksuun liittyvää valtuutusta, annetaan viittaus kyseiseen valtuutuksen. Siksi valtuutukseen voidaan viitata myöhemmin, kun varat on siepattu toteutuman aikaan. Tämä valtuutus on yksilöllinen, kun kyseessä on kauppias, maksun yhdistin ja suoritin. 

Jos online-tilassa luotu tilaus noudetaan kaupasta, saman tilauksen toimitustiedot on muistettava ja niitä on käytettävä. Kun alkuperäiset tiedot toimitetaan osana pyyntöä, jonka mukaan maksu siepataan alkuperäistä valtuutusta vastaan, maksun käsittelijä voi käsitellä pyynnön ja siepata maksun. 

Jotta voisit viitata online-tilaukseen oikein, myös samaa suoritinta tukevan kortti ei ole läsnä -maksuyhdistimen on oltava käytettävissä. Näin myyntipistejärjestelmällä voi olla yksi suoritin Kortti paikalla -maksuja varten, mutta se voi myös käyttää muita maksuyhdistimiä, jotta se voi täyttää muissa kanavissa luodut tilaukset eri maksukäsittelijöiden avulla. 

## <a name="supported-scenarios"></a>Tuetut skenaariot

Seuraavia Omni-Channel-tukiskenaarioita tuetaan:

- Tee ostoksia verkossa, nouda myymälästä
- Osta puhelinkeskuksesta, nouda myymälästä
- Osta myymälästä A, nouda myymälästä B
- Osta myymälästä A, toimita asiakkaalle

    > [!NOTE]
    > Puhelinkeskuksessa suoritetut maksut, jotka yhdistyvät Normaali-maksutoimintoon, on merkittävä muotoon **Ennakkomaksu** = **Kyllä**, jotta ne otetaan huomioon veloitettavassa summassa, kun tilaus kumotaan myyntipisteessä. Normaali-tyypin muita kuin ennakkomaksuja ei tunnisteta, kun tilaus kumotaan myyntipisteessä. 

Näiden skenaarioiden muunnelmia tuetaan myös. Esimerkiksi online-tilauksessa voi olla sekä rivejä, jotka lähetetään asiakkaalle, että rivejä, jotka noudetaan myymälästä. Kaikkia tilauksen toteutusvaihtoehtoja tuetaan Omni-Channel-maksuissa. 

Seuraavissa osissa kuvataan kunkin skenaarion vaiheet ja näytetään, miten skenaario suoritetaan demotietojen avulla. 

### <a name="buy-online-pick-up-in-store"></a>Tee ostoksia verkossa, nouda myymälästä

Varmista ennen alkamista, että seuraavat edellytykset ovat olemassa:

- Sinulla on viitemyymälä, jossa Adyen-yhdistin on määritetty.
- **Commercen jaetut parametrit** -sivun **Omni-Channel-maksun** vaihtoehdoksi on asetettu **Tosi**. Myöhemmissä versioissa tämä asetus siirretään **Ominaisuuksien hallinta** -työtilaan. Siellä voit valita **Monikanavan maksut** -toiminnon ja valita **Ota käyttöön nyt**. 
- Adyen-maksuyhdistin on määritetty Houston POS -rekisteriin.
- Retail Modern POS for Windows tai Android ja sisäänrakennettu laiteasema tai
- Modern POS for iOS tai Cloud POS ja yhdistetty, jaettu laiteasema. 

Noudata seuraavia vaiheita, jos haluat suorittaa skenaarion:

1. Luo viitemyymälään noutotilaus. Muista valita **Houston**-myymälä. 
2. Käy läpi kassaan liittyvät vaiheet ja maksa käyttämällä testiluottokortin numeroa. Voit etsiä testiluottokorttien numeroita [Adyen-testikorttien numerot -sivulta](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description).
3. Commerce-ohjelmassa voit luoda **Synkronoi tilaukset** -eräajon taustajärjestelmässä **P-001**-jakeluaikataulun avulla.
4. Valitse myyntipisteen aloitussivulla **Noudettavat tilaukset** -toiminto, jotta voit tarkastella myymälän noudettavia tilauksia. 
5. Valitse yksi tai useita rivejä viitteenä luodusta tilauksesta ja valitse **Nouda**.

    Tilaus haetaan taustajärjestelmästä. 

6. Kun tilausrivin tiedot haetaan taustajärjestelmästä ja järjestelmä havaitsee korttimaksun, jota voidaan käyttää Omni-kanavalla, sinulle ilmoitetaan, että maksutapa on käytettävissä.
7. Valitse **Käytä käytettävissä olevaa maksutapaa**, kun haluat suorittaa tapahtuman käyttämällä viitteenä myymälän korttitietoja.

    Tilausrivit ladataan tapahtumasivulle, ja erääntyvä saldo on 0 (nolla). 

8. Valitse **Maksut**-välilehti ja tarkastele online-tilauksesta vedettynä maksuvälineriviä. 
9. Valitse mikä tahansa maksutapa tapahtuman suorittamista varten. 

### <a name="buy-in-call-center-pick-up-in-store"></a>Osta puhelinkeskuksesta, nouda myymälästä

1. Kirjoita Commercessa **Asiakaspalvelu**-sivun hakupalkkiin **Karen Berg** ja valitse sitten **Hae**. 
3. Valitse hakutuloksista **Karen Berg**.
4. Kun Karen on ladattu **Asiakaspalvelu**-sivulle, valitse **Uusi myyntitilaus**.
5. Voit tarkastella tilauksen otsikkoa valitsemalla **Otsikko** uudella myyntitilaussivulla. 
6. Määritä **Tilauksen otsikko** -sivulla toimipaikaksi **Keski** ja varastoksi **Houston**.
7. Määritä **Toimitus**-välilehdellä **Toimitustapa**-kentän arvoksi **60** asiakkaan noutoa varten.
8. Valitse **Rivit** ja lisää tilaukseen vähintään yksi rivi. 
9. Määritä tilauksen valmistumisvirta valitsemalla **Valmis**.
10. Vieritä alas maksut-osaan, valitse **Lisää** ja valitse sitten rivi, jolla maksutapatyypiksi on määritetty **Kortit**. 
11. Lisää korttimaksu valitsemalla plusmerkki (**+**). 
12. Kirjoita [Adyen-testikorttien numerot -sivulta](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description)löytyneen testiluottokortin numeron tiedot ja valitse sitten **OK**.

    > [!NOTE]
    > Jos syöttämäsi kortin numero eroaa tuotemerkistä, joka valittiin maksun aloittamisen yhteydessä, maksu menee silti läpi. Se kirjataan kuitenkin tileille, jotka on liitetty vaiheessa 10 valitsemaasi korttimerkkiin.

12. Valitse uudelleen **OK** sulkeaksesi **Tilauksen loppuunmaksu** -valintaikkunan.
13. Valitse **Myyntitilauksen yhteenveto** -sivulla **Lähetä**.
14. Valitse myyntipisteen aloitussivulla **Noudettavat tilaukset** -toiminto, jotta voit tarkastella myymälän noudettavia tilauksia. 
15. Valitse yksi tai useita rivejä viitteenä luodusta tilauksesta ja valitse **Nouda**.

    Tilaus haetaan taustajärjestelmästä. 

16. Kun tilausrivin tiedot haetaan taustajärjestelmästä ja järjestelmä havaitsee korttimaksun, jota voidaan käyttää Omni-kanavalla, sinulle ilmoitetaan, että maksutapa on käytettävissä.
17. Valitse **Käytä käytettävissä olevaa maksutapaa**, kun haluat suorittaa tapahtuman käyttämällä viitteenä myymälän korttitietoja.

    Tilausrivit ladataan tapahtumasivulle, ja erääntyvä saldo on 0 (nolla).

18. Valitse **Maksut**-välilehti ja tarkastele online-tilauksesta vedettynä maksuvälineriviä. 
19. Valitse mikä tahansa maksutapa tapahtuman suorittamista varten. 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>Osta myymälästä A, nouda myymälästä B

1. Aloita myyntipiste Houston Storessa.
2. Lisää **Tapahtuma**-sivulla Karen Berg tapahtumaan ja kirjoita **2001** käyttämällä numeronäppäimistöä.
3. Lisää tapahtumaan vähintään yksi rivi.
4. Valitse **Tilaukset**, jos haluat nähdä tilausvaihtoehdot.
5. Valitse **Nouda kaikki** ja valitse sitten pyydettäessä **Asiakastilaus**.
6. Kirjoita hakupalkkiin **Seattle** ja valitse sitten noutopaikaksi **Seattle**-myymälä. 
7. Valitse **OK**, jos haluat hyväksyä kuluvan päivän noutopäiväksi.
9. Valitse **Maksa kortilla** jos haluat aloittaa maksun.
10. Tarjoa korttimaksu määrästä, joka on maksettava talletuksesta. 
11. Suorita talletusmaksu maksupäätteessä. 
12. Kun talletus on maksettu, valitse mahdollisuus käyttää samaa korttia toteumaa varten ja odota, kunnes tilaus on tehty. 
13. Aloita myyntipiste Seattle Storessa.
14. Valitse myyntipisteen aloitussivulla **Noudettavat tilaukset** -toiminto, jotta voit tarkastella myymälän noudettavia tilauksia. 
15. Valitse yksi tai useita rivejä viitteenä luodusta tilauksesta ja valitse **Nouda**.

    Tilaus haetaan taustajärjestelmästä. 

16. Kun tilausrivin tiedot haetaan taustajärjestelmästä ja järjestelmä havaitsee korttimaksun, jota voidaan käyttää Omni-kanavalla, sinulle ilmoitetaan, että maksutapa on käytettävissä.
17. Valitse **Käytä käytettävissä olevaa maksutapaa**, kun haluat suorittaa tapahtuman käyttämällä viitteenä myymälän korttitietoja.

    Tilausrivit ladataan tapahtumasivulle, ja erääntyvä saldo on 0 (nolla).

18. Valitse **Maksut**-välilehti ja tarkastele online-tilauksesta vedettynä maksuvälineriviä. 
19. Valitse mikä tahansa maksutapa tapahtuman suorittamista varten. 

### <a name="buy-in-store-a-ship-to-customer"></a>Osta myymälästä A, toimita asiakkaalle

1. Aloita myyntipiste Houston Storessa.
2. Lisää **Tapahtuma**-sivulla Karen Berg tapahtumaan ja kirjoita **2001** käyttämällä numeronäppäimistöä.
3. Lisää tapahtumaan vähintään yksi rivi.
4. Valitse **Tilaukset**, jos haluat nähdä tilausvaihtoehdot.
5. Valitse **Lähetä kaikki** ja valitse sitten pyydettäessä **Asiakastilaus**.
6. Valitse lähetystapasivulla **Vakio yön yli** ja hyväksy sitten kuluva päivämäärä lähetyspäiväksi valitsemalla **OK**. 
7. Valitse **OK**, jos haluat hyväksyä kuluvan päivän noutopäiväksi.
8. Valitse **Maksa kortilla** jos haluat aloittaa maksun.
9. Tarjoa korttimaksu määrästä, joka on maksettava talletuksesta. 
10. Suorita talletusmaksu maksupäätteessä. 
11. Kun talletus on maksettu, valitse mahdollisuus käyttää samaa korttia toteumaa varten ja odota, kunnes tilaus on tehty.

Kun tilaus kerätään, pakataan ja laskutetaan taustajärjestelmässä, myyntipisteessä olevia maksutietoja käytetään, kun ne keräävät asiakkaalle toimitettavien tuotteiden varat. 

## <a name="scenario-details"></a>Skenaarion tiedot

Juuri kuvattujen perusskenaarioiden lisäksi maksujen SDK:hon on tehty useita lisäparannuksia, jotka tukevat Omni-Channel-maksuja. 

### <a name="pos"></a>Myyntipiste

#### <a name="single-swipedip-for-customer-orders"></a>Yksi pyyhkäisy/lukeminen asiakkaan tilauksille

Ennen kuin Omni-Channel-maksutoiminto otettiin käyttöön, asiakastilaukset, jotka sisälsivät talletuksia, luotiin myyntipistesovelluksessa. Asiakkaiden oli pyyhkäistävä (tai luettava) korttinsa päätteessä kaksi kertaa: kerran maksaakseen talletuksen ja yhden kerran, jotta kortti voidaan määrittää myöhemmin tilauksen toteuttamiseksi. Kun Omni-Channelin tunnusten määrittämisominaisuus on käytössä, asiakkaiden on pyyhkäistä korttinsa vain kerran, jotta molemmat maksavat talletuksen, ja sallivat myöhemmin erääntyvien tuotteiden summan. Toteutuksen hetkellä hyväksytyt varat otetaan talteen. Ennen kuin Omni-Channel tunnusten määritysominaisuus on toteutettu, vain toistuvan kortin tunnussanoma on luotu seuraavaa tilausten täyttämistä varten. Näin ollen vireillä olevan toteuman varoja ei hyväksytty, ja koska näitä varoja ei ole pidätetty kyseisen oston yhteydessä, on vähemmän todennäköistä, että ne voidaan siepata myöhemmin.

> [!NOTE]
> Yksittäinen pyyhkäisy ei ole tuettu Retail-versiossa 8.1.3. Asiakkaan tilaukset versiossa 8.1.3 käyttävät samaa virtausta, jota käytettiin, ennen kuin Omni-Channel-tunnusten määritysominaisuus toteutettiin. 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>Kortit, jotka eivät voi antaa toistuvia korttitunnuksia

Joitakin kortteja ei voi käyttää Omni-Channel-maksuissa, koska ne eivät tue toistuvaa korttitunnusten antamista. Kun tilaus luodaan myyntipisteessä, jos talletus maksetaan kortilla, joka ei tue toistuvia kortti tunnuksia, käytetään aiempaa korttimerkintävirtatoimintoa. Näin ollen asiakkaan, joka haluaa tarjota seuraavassa tilauksessa käytettävän suorituksen, on esitettävä toinen kortti. Jos toinen kortti ei tue toistuvia korttitunnuksia, korttimerkintätoiminto hylätään, ja kassanhoitaja pyytää asiakasta antamaan toisen kortin. 

### <a name="using-a-different-card"></a>Toisen kortin käyttäminen

Tilauksen noutoa varten myymälässä olevalla asiakkaalla on mahdollisuus käyttää toista korttia. Kun kassanhoitaja saa käyttöönsä **Käytettävissä olevan maksutavan** kehotteen tilauksen noutoa varten, hän voi kysyä, haluaako asiakas käyttää samaa korttia. Jos asiakas on kadottanut tilauksen luomisessa käytetyn kortin ja haluaa maksaa tilauksen toisen kortin avulla, kassanhoitaja voi valita **Käytä eri maksutapaa.** Jos asiakas palaa myöhemmin hakemaan useampia nimikkeitä samalle tilaukselle ja alkuperäisen kortin valtuutus on edelleen voimassa, kassanhoitaja voi kysyä, haluaako asiakas käyttää kyseistä korttia.

### <a name="invalid-authorizations"></a>Virheelliset valtuutukset

Jos tilauksen luonnissa käytetty kortti ei ole enää voimassa, kun tuotteet valitaan noutoa varten, suorituksen sieppauspyyntö epäonnistuu. Myyntipistemaksuyhteys yrittää luoda uuden valtuutuksen ja siepata käyttämällä samoja korttitietoja. Jos uusi valtuutus tai sieppaus epäonnistuu, kassanhoitaja saa tiedon siitä, että maksuja ei voitu käsitellä. Kassan on tällöin saatava asiakkaalta uusi maksuerä. 

### <a name="multiple-available-payments"></a>Useita käytettävissä olevia maksuja

Kun tilaus, jolla on useita tarjouksia ja useita rivejä, on noudettavissa, kassanhoitaja saa ensin käyttöön **Käytettävissä olevan maksutavan** kehotteen. Jos on useita kortteja ja kassanhoitaja valitsee **Käytä käytettävissä olevaa maksutapaa**, olemassa olevat korttimaksuvälinerivit siepataan, kunnes saldo täyttyy parhaillaan kerättävissä tavaroissa. Kassanhoitajilla ei ole mahdollisuutta valita korttia, jota käytetään noudettavissa tuotteissa. 

## <a name="related-articles"></a>Liittyvät artikkelit

- [Maksut – usein kysytyt kysymykset](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Dynamics 365 -maksuyhdistin Adyenia varten](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
- [BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä](./cpe-bopis.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]