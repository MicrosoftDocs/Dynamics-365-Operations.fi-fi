---
title: Jaettu tilausten hallinta (DOM)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commercen jaetun tilausten hallinnan (DOM) toimintoja.
author: josaw1
ms.date: 11/16/2022
ms.topic: index-page
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.openlocfilehash: cfb89544580141ed397d27886f51fd0f1ac138d2
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785177"
---
# <a name="distributed-order-management-dom"></a>Jaettu tilausten hallinta (DOM)

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commercen jaetun tilausten hallinnan (DOM) toimintoja.

Jaettu tilausten hallinta on monikanavainen tilausten täyttämisen optimointiratkaisu, joka auttaa maksimoimaan tilausten täyttämisen toimitusketjuverkostossa. Jaettu tilausten hallinta auttaa varmistamaan, että asiakkaille toimitetaan oikea määrä tuotteita oikeista lähteistä oikea-aikaisesti. Jaettu tilausten hallinta auttaa myös maksimoimaan voitot ja minimoimaan kustannukset, minkä lisäksi se auttaa vastaamaan palvelutasovaatimuksiin.

Jaettu tilausten hallinta käyttää sekalukuohjelmointia (MIP) ja ennakoivia analyysimalleja optimointien suorittamiseen sekä erätasoalla että yksittäisten tilausten tasolla. Tämän ominaisuuden avulla vähittäismyyjät voivat määrittää sääntöjä tasapainottamaan monia ristiriitaisia tilausten täyttämistarpeita. Modernissa toimitusverkostossa tuotteiden täyttämiseen voidaan käyttää useita kanavia, minkä vuoksi organisaatioiden on voitava mukautua nopeasti tilausta koskeviin muutoksiin, toimittajien saatavuusongelmiin ja kysyntäpiikkeihin. Jaettu tilausten hallintaa auttaa maksimoimaan tilauksen täyttämisen ja etsimään oikeat tuotteen toimituslähteet ottamalla huomioon liiketoimintarajoitteet ja tavoitteet, kuten kustannusten minimoinnin täyttämällä tilaukset lähimmistä lähteistä. Jaettu tilausten hallinta optimoi tilausten täyttämisen ottamalla huomioon seuraavat seikat: etäisyys tuotteen täyttämislähteiden ja toimituskohteiden välillä, optimointitavoitteina määritetyt kustannuskertoimet sekä rajoitteina määritetyt säännöt, kuten varasto täyttämissolmuissa. Jaettu tilausten hallinta antaa mahdollisuuden useiden sellaisten profiilien määrittämiseen, joiden avulla yritykset voivat määrittää optimointistrategioita liiketoimintatyypin tai kuluttajasegmentin mukaan. 

Seuraavassa kuvassa on myyntitilauksen elinkaari jaetussa tilauksen hallintajärjestelmässä.

![Myyntitilauksen elinkaari jaetun tilausten hallinnan kontekstissa](./media/flow.png "Myyntitilauksen elinkaari jaetussa tilauksen hallintakontekstissa")

Seuraava video antaa yleiskuvan Dynamics 365 Commercen jaetun tilausten hallinnan ominaisuuksista


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bRYl]

## <a name="set-up-dom"></a>Jaetun tilausten hallinnan määrittäminen

1. Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.
2. Laajenna **Konfigurointiavaimet**-välilehdessä **Commerce**-solmu ja valitse **Jaettu tilausten hallinta** -valintaruutu.
3. Siirry kohtaan **Retail ja Commerce \> Jaettu tilausten hallinta \> Asetukset \> DOM-parametrit**.
4. Määritä **Yleiset**-välilehdessä seuraavat arvot:

    - **Ota jaettu tilausten hallinta käyttöön** – Määritä tähän arvoksi **Kyllä**.
    - **Vahvista Bing Maps -palvelun käyttö DOM:ssa** – Määritä tähän arvoksi **Kyllä**.

        > [!NOTE]
        > Voit määrittää tähän arvoksi **Kyllä** vain, jos **Ota Bing Maps käyttöön** -asetuksen arvo **Bing Maps** -välilehdessä **Commercen yhteiset parametrit** -sivulla (**Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Commercen yhteiset parametrit**) on myös **Kyllä** ja jos **Bing Maps -avain** -kenttään annetaan kelvollinen avain.
        >
        > [Bing Mapsin kehityskeskusportaalin](https://www.bingmapsportal.com/) avulla voit rajoittaa Bing Mapsin ‑ohjelmointirajapinnan avaimia niin, että ne ovat käytettävissä vain määrittämiltäsi toimialueilta. Tämän ominaisuuden avulla asiakkaat voivat määrittää tiukat viittaaja-arvot tai IP-osoitealueet, joiden mukaan avain vahvistetaan. Sallittujen IP-osoitteiden luettelosta peräisin olevat pyynnöt käsitellään normaalisti, kun taas luettelon ulkopuolelta tulevat pyynnöt palauttavat Käyttö estetty ‑vastausten. Toimialueen suojauksen lisääminen ohjelmointirajapinta-avaimeen on valinnaista, ja entiselleen jätetyt avaimet toimivat edelleen. Avaimen sallittujen IP-osoitteiden luettelo ei ole riippuvainen muista avaimistasi, joten voit määrittää erilliset säännöt kullekin avaimellesi. Jaettu tilausten hallinta ei tue toimialueella viitattujen ominaisuuksien määrittämistä.

    - **Pidätyskausi päivinä** – määritä, kauanko DOM-suoritusten luomia täyttämistilauksia säilytetään järjestelmässä. **DOM-täyttämistietojen poistotyön asetukset** -erätyö poistaa kaikki täyttämissuunnitelmat, jotka ovat tässä määritettyä päivien määrää vanhempia.
    - **Hylkäämiskausi (päivinä)** – Määritä, kuinka paljon aikaa pitää kulua, ennen kuin hylätty tilausrivi voidaan määrittää samaan sijaintiin.

5. Määritä **Selvitys**-välilehdessä seuraavat arvot:

    - **Automaattisten täyttämisyritysten enimmäismäärä** – Määritä, kuinka monta kertaa DOM-moduuli yrittää välittää tilausrivin valittuun sijaintiin. Jos DOM-moduuli ei voi välittää tilausriviä sijaintiin määritetyillä yrityskerroilla, se merkitsee tilausrivin poikkeukseksi. Tämän jälkeen rivi ohitetaan tulevissa suorituksissa, kunnes tila nollataan manuaalisesti.
    - **Paikallisen myymälän alueen säde** – Kirjoita arvo. Tämän kentän avulla määritetään, miten sijainnit ryhmitellään ja määritetään tasaveroisiksi etäisyyden osalta. Jos esimerkiksi annat arvon **100**, jokaista myymälää ja jakelukeskusta 100 mailin säteellä täyttämistilauksen osoitteesta pidetään tasaveroisena etäisyyden osalta.
    - **Selvityksen tyyppi** – Valitse arvo. Commercessa vapautetaan kaksi selvityksen tyyppiä: **Tuotannon selvitys** ja **Yksinkertaistettu selvitys**. Kaikille koneille, jotka suorittavat DOM:n (siis kaikki palvelimet, jotka kuuluvat DOMBatch-ryhmään), on valittava **Tuotannon selvitys**. Tuotannon selvitystä varten tarvitaan erityinen käyttöoikeusavain, joka oletusarvoisesti lisensoidaan ja otetaan käyttöön tuotantoympäristöissä. Tuotannon selvitys on jo otettu käyttöön uusissa tason 2+ ympäristöissä. Muissa kuin tuotantoympäristöissä tämä käyttöoikeusavain on otettava käyttöön manuaalisesti. Voit ottaa käyttöoikeusavaimen käyttöön manuaalisesti toimimalla seuraavasti:

        1. Avaa Microsoft Dynamics Lifecycle Servicesissa jaettu omaisuuskirjasto, valitse omaisuustyypiksi **Malli**, ja lataa **DOM-käyttöoikeus**-tiedosto.
        1. Käynnistä Microsoft IIS -palveluiden hallinta, valitse hiiren kakkospainikkeella **AOSService-verkkosivusto** ja valitse sitten **Selaa**. Windowsin resurssienhallintaikkuna avautuu kansiossa **\<AOS service root\>\\webroot**. Kirjoita muistiin hakemiston \<AOS Service root\> polku, sillä sitä käytetään seuraavassa vaiheessa.
        1. Kopioi määritystiedosto hakemistoon **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        1. Siirry Headquarters-asiakasohjelmaan ja avaa **DOM-parametrit**-sivu. Valitse **Selvitys**-välilehden **Selvityksen tyyppi** -kentässä **Tuotannon selvitys** ja varmista, ettei virhesanomia ole näkyvissä.

        > [!NOTE]
        > Yksinkertaistettu selvitys on vaihtoehto silloin, kun vähittäismyyjä haluaa kokeilla DOM-ominaisuutta ottamatta käyttöön erityistä lisenssiä. Organisaatioiden ei tulisi käyttää yksinkertaistettua selvitystä tuotantoympäristöissä.
        >
        > Tuotannon selvitys parantaa suorituskykyä (kuten tilauksien ja tilausrivien määrää, joka voidaan käsitellä yhden suorituksen aikana) ja tulosten yhdistämistä (koska tilauserä ei ehkä tuota parhaita tuloksia joissakin tilanteissa). **Osittaistilaukset**-sääntö edellyttää tuotannon selvitystä.

6. Siirry takaisin kohtaan **Vähittäiskauppa ja kaupankäynti \> Jaettu tilausten hallinta \> Asetukset \> DOM-parametrit**.
7. Määritä **Numerosarjat**-välilehdessä tarvittavat numerosarjat eri DOM-yksiköille.

    > [!NOTE]
    > Ennen kuin numerosarjat voidaan määrittää näille yksiköille, ne on määritettävä **Numerosarjat**-sivulla (**Organisaation hallinto \> Numerosarjat \> Numerosarjat**).

8. DOM-ominaisuus tukee erilaisia DOM-sääntöjen määrityksiä, ja organisaatiot voivat määrittää useita sääntöjä liiketoiminnan tarpeiden mukaan. DOM-säännöt voidaan määrittää sijaintiryhmälle tai yksittäiselle sijainnille sekä tietylle tuoteluokalle, tuotteelle tai variantille. Voit luoda DOM-säännöissä käytettävät sijaintien ryhmittelyt seuraavasti:

    1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Täytäntöönpanoryhmät**.
    2. Valitse **Uusi** ja kirjoita uuden ryhmän nimi ja kuvaus.
    3. Valitse **Tallenna**.
    4. Voit lisätä ryhmään yksittäisen sijainnin valitsemalla **Lisää rivi**. Vaihtoehtoisesti voit lisätä useita sijainteja valitsemalla **Lisää rivejä**.

    > [!NOTE]
    > Commerce 10.0.12:ssa ja sitä uudemmassa versiossa **Mahdollisuus määrittää sijainniksi Lähetys tai Nouto on otettu käyttöön täyttämisryhmässä** -vaihtoehto on oltava otettuna käyttöön **Ominaisuuden hallinta** -työtilassa.
    >
    > Tämä ominaisuus lisää uudet määritykset **Täyttämisryhmä**-sivulla, joten voit määrittää, käytetäänkö varastoa lähetykseen vai käytetäänkö varastoa ja myymälää yhdessä lähetykseen, noutoon tai molempiin. 
    >
    > Jos otat ominaisuuden käyttöön, sijainnin valintavaihtoehdot päivitetään, kun nouto- tai toimitustilauksia luodaan myyntipisteessä.
    >
    > Kun ominaisuus otetaan käyttöön, myyntipisteen sivut päivitetään, kun valitaan kaikkien tai valittujen toimitus.

9. Voit määrittää säännöt valitsemalla **Retail ja Commerce \> Jaettu tilausten hallinta \> Asetukset \> Sääntöjen hallinta**. Tällä hetkellä tuetaan seuraavia DOM-sääntöjä:

    - **Vähimmäisvarastosääntö** – Tämäntyyppisen säännön avulla organisaatiot voivat merkitä tuotteen tietyn määrän erityiseksi muihin tarkoituksiin kuin tilauksen täytäntöönpanoon. Esimerkiksi organisaatiot eivät ehkä halua DOM-suorituksen kohdistavan myymälässä saatavilla olevan varaston koko määrää tilausten täytäntöönpanoon. Sen sijaan voidaan haluta varata osa saldosta fyysiseen kauppaan tuleville asiakkaille. Kun tätä sääntötyyppiä käytetään, voidaan määrittää sijainti- tai sijaintiryhmäkohtainen tietylle tuoteluokalle, yksittäiselle tuotteelle tai tuotevariantille ylläpidettävä vähimmäisvarasto. Vähimmäisvarasto voidaan määrittää myös lisäluokkahierarkian avulla. Jos tuote sijoittuu useisiin luokkiin, lisäluokalle annetaan suurin tärkeys kaikissa säännöissä, joissa voidaan käyttää luokkia.
    - **Täyttämissijainnin prioriteettisääntö** – Tämän sääntötyypin avulla organisaatiot voivat määrittää sijaintihierarkian priorisointi, jonka DOM-moduuli ottaa huomioon, kun se yrittää tunnistaa tiettyjen tuotteiden täyttämissijainnit. Prioriteettien arvot voivat olla välillä on 1–10, jossa 1 on suurin prioriteetti ja 10 on pienin prioriteetti. Suuren prioriteetin sijainteja käytetään ennen sijainteja, joilla on alhaisempi prioriteetti. Jos sääntö määritetään tiukkana rajoitussääntönä, tilaukset välitetään vain sijainteihin, joille on määritetty prioriteetti. Jaetussa tilausten hallinnassa ensisijainen valinta on tilausten toimittaminen kokonaisuudessaan yhdestä sijainnista. Niinpä jos koko tilaus ja sen rivit eivät ole saatavana sijainnista, jonka prioriteetti on 1, jaettu tilausten hallinta yrittää täyttää sen sijainnista, jonka prioriteetti on 2.
    - **Osittaistilausten sääntö** – Retail 10.0.5:ssä **Täytä tilaus vain yhdestä sijainnista** -parametrin arvoksi muutettiin **Täyttämissijaintien enimmäismäärä**. Vanha parametri antoi käyttäjille mahdollisuuden määrittää, täytetäänkö tilaukset vain yhdestä sijainnista vai mahdollisimman monesta sijainnista. Uusi parametri antaa käyttäjille mahdollisuuden määrittää, tehdäänkö täyttäminen määritetystä sijaintijoukosta (enintään viisi sijaintia) tai mahdollisimman monesta sijainnista. Jaettu tilausten hallinta jakaa rivin kaikissa muissa vaihtoehtoissa paitsi yhdestä sijainnista täytettäessä, koska tilaus käsitellään riveittäin. Tämä sääntö toimii vain tuotannon selvityksen yhteydessä.
    - **Offline-täyttämisen sijaintisääntö** – tämän säännön avulla organisaatiot voivat määrittää sijainnin tai sijaintiryhmän offline-sijainniksi tai jaetun tilausten hallinnan ulkopuolelle, jotta tilauksia ei voi määrittää täytettäväksi näistä sijainneista.
    - **Hylkäysten enimmäismäärän sääntö** – Tämän säännön avulla organisaatiot voivat määrittää hylkäyksille raja-arvon. Kun raja-arvo saavutetaan, DOM-käsittelijä merkitsee tilauksen tai tilausrivin poikkeukseksi ja jättää sen jatkokäsittelyn ulkopuolelle. Jaettu tilausten hallinta varmistaa suorituskyvyn siten, ettei se tarkastele kaikkien hylkäysten historiaa. 

        Sen jälkeen kun tilausrivit on määritetty sijaintiin, sijainti voi hylätä määritetyn tilausrivin, koska se ei jostakin syystä pysty täyttämään tilausriviä. Hylätyt rivit merkitään poikkeukseksi ja palautetaan takaisin pooliin seuraavaa suorituskertaa varten. Seuraavan ajon aikana DOM yrittää määrittää hylätyn rivin toiseen sijaintiin. Myös uusi sijainti voi hylätä määritetyn tilausrivin. Tämä määrittämisen ja hylkäämisen sykli voi tapahtua useita kertoja. Kun hylkäysten määrä ylittää määritetyn raja-arvon, DOM merkitsee tilausrivin pysyväksi poikkeukseksi eikä enää ota kyseistä tilausriviä määritettäväksi. DOM ottaa tilausrivin uudelleen määritettäväksi vain, jos käyttäjä nollaa tilausrivin tilan manuaalisesti.

    - **Enimmäisetäisyyssääntö** – Tämä säännön avulla organisaatiot voivat määrittää enimmäisetäisyyden tilauksen täyttävälle sijainnille tai sijaintiryhmälle. Jos sijainnille on määritetty päällekkäisiä enimmäisetäisyyssääntöjä, DOM käyttää pienintä sijainnille määritettyä enimmäisetäisyyttä.
    - **Tilausten enimmäismäärän sääntö** – Tämän säännön avulla organisaatiot voivat määrittää tilausten enimmäismäärän, jonka sijainti tai sijaintiryhmä voi käsitellä. Järjestelmä ottaa optimointiprosessin aikana huomioon tilaukset, joita ei ole toimitettu näistä sijainnista. Tämä tarkistus koskee kaikkia profiileja. Niinpä jos tilauksen limittäinen enimmäismäärä määritetään samassa sijainnissa oleviin profiileihin, järjestelmä ottaa huomioon kaikkiin profiileihin määritettyjen tilausten enimmäismäärän. 

    Seuraavaksi käsitellään yleisiä määritteitä, joita voidaan määrittää edellä mainituille sääntötyypeille:

    - **Aloituspäivä** ja **Päättymispäivä** – kullekin säännölle voidaan määrittää päivämääräväli voimassaoloajaksi näiden kenttien avulla.
    - **Ei käytössä** – vain ne säännöt, joiden arvo tässä kentässä on **Ei**, otetaan huomioon jaettua tilausten hallintaa suoritettaessa.
    - **Tiukka rajoitus** – Sääntö voidaan määrittää tiukaksi rajoitukseksi tai ei-tiukaksi rajoitukseksi. Kukin DOM-suoritus käy läpi kaksi toistoa. Ensimmäisessä toistossa jokaista sääntöä pidetään tiukkana rajoituksena riippumatta tämän kentän arvosta. Toisin sanoen kaikki säännöt ovat käytössä. Ainoa poikkeus on **Sijainnin prioriteetti** -sääntö. Toisessa toistossa säännöt, joita ei ole määritetty tiukoiksi rajoituksiksi, poistetaan, ja tilauksille tai tilausriveille, joille ei määritetty sijaintia kaikkia sääntöjä käytettäessä, määritetään sijainnit.

10. Täyttämisprofiileja käytetään sääntökokoelmien, yritysten, myyntitilausten alkuperien ja toimitustapojen ryhmittelyyn. Jokainen DOM-suoritus on tiettyä täyttämisprofiilia varten. Näin organisaatiot voivat määrittää ja suorittaa sääntöjoukkoja yritysjoukossa sellaisille tilauksille, joilla on tietyt myyntitilauksen alkuperät ja toimitustavat. Jos siis pitää suorittaa eri sääntöjoukkoja myyntitilausten alkuperän tai toimitustavan mukaan, täyttämisprofiilit voidaan määrittää vastaavasti. Voit määrittää täyttämisprofiileita noudattamalla seuraavia ohjeita:  

    1. Siirry kohtaan **Retail ja Commerce \> Jaettu tilausten hallinta \> Asetukset \> Täyttämisprofiilit**.
    2. Valitse **Uusi**.
    3. Kirjoita arvot **Profiili**- ja **Kuvaus**-kenttiin.
    4. Määritä **Automaattinen tuloksen käyttö** -asetus. Jos määrität tämän asetuksen arvoksi **Kyllä**, profiilin DOM-suorituksen tulokset kohdistetaan automaattisesti myyntitilauksen riveille. Jos määrität arvoksi **Ei**, tuloksia voi tarkastella vain täyttämissuunnitelmassa. Niitä ei kohdisteta myyntitilausriveille.
    5. Jos haluat, että DOM-profiili suoritetaan tilauksille, joilla on kaikki myyntitilausten alkuperät (mukaan lukien tilaukset, joissa myyntitilauksen alkuperää ei ole määritetty), määritä **Käsittele tilaukset, joilla on tyhjä myynnin alkuperä** -asetuksen arvoksi **Kyllä**. Voit suorittaa profiilin vain joillekin myyntitilauksen alkuperille määrittämällä ne **Myynnin alkuperät** -sivulla jäljempänä esitetyllä tavalla.

        > [!NOTE]
        > Commerce 10.0.12:ssa ja sitä uudemmissa versioissa **Mahdollisuus määrittää täyttämisryhmä täyttämisprofiiliin** -ominaisuus on oltava otettuna käyttöön **Ominaisuuden hallinta** -työtilassa. Tämän ominaisuuden avulla voidaan määrittää varastoluettelo, jota jaettu tilausten hallinta käyttää, kun täyttämisprofiilin sisältävä optimointi suoritetaan. Jos tätä varastoluetteloa ei ole määritetty, jaettu tilausten hallinta tarkastelee kaikkia yrityksen profiilissa määritettyjä varastoja.
        >
        > Tämä toiminto lisää **Täyttämisprofiili**-sivulle uuden profiilin, joka voidaan liittää yhteen täyttämisryhmään. 
        >
        > Jos valitset täyttämisryhmän, kyseisen täyttämisprofiilin DOM-säännöt voidaan suorittaa täyttämisryhmään sisältyvissä toimitusvarastoissa. 
        > 
        > Tämän toiminnon käyttö tehokkaasti edellyttää, että yksi täyttämisryhmä sisältää kaikki toimitusvarastot ja että kyseinen täyttämisryhmä liitetään sitten täyttämisprofiiliin.

    6. Valitse **Yritykset**-pikavälilehdessä **Lisää** ja sitten sopiva yritys.
    7. Valitse **Säännöt**-pikavälilehdessä **Lisää** ja sitten profiiliin linkitettävä sääntö.
    8. Toista kahta edellistä vaihetta, kunnes kaikki tarvittavat säännöt on liitetty profiiliin.
    9. Valitse **Tallenna**.
    10. Valitse toimintoruudun **Asetukset**-välilehdessä **Toimitustavat**.
    11. Valitse **Toimitustavat**-sivulla **Uusi**.
    12. Valitse yritys kentässä **Yritys**. Yritysten luettelossa on vain aikaisemmin lisätyt yritykset.
    13. Valitse **Toimitustapa**-kentässä tähän profiiliin liitettävä toimitustapa. Toimitustapaa ei voi liittää useisiin aktiivisiin profiileihin.
    14. Toista kahta edellistä vaihetta, kunnes kaikki tarvittavat toimitustavat on liitetty profiiliin.
    15. Sulje **Toimitustavat**-sivu.
    16. Valitse toimintoruudun **Asetukset**-välilehdessä **Myyntitilauksen alkuperät**.
    17. Valitse **Myynnin alkuperät** -sivulla **Uusi**.
    18. Valitse yritys kentässä **Yritys**. Yritysten luettelossa on vain aikaisemmin lisätyt yritykset.
    19. Valitse **Myynnin alkuperä** -kentässä tähän profiiliin liitettävä myynnin alkuperä. Myynnin alkuperää ei voi liittää useisiin aktiivisiin profiileihin.
    20. Toista kahta edellistä vaihetta, kunnes kaikki tarvittavat myynnin alkuperät on liitetty profiiliin.
    21. Sulje **Myynnin alkuperät** -sivu.
    22. Määritä **Ota profiili käyttöön** -asetukseksi **Kyllä**. Jos asetuksissa on virheitä, saat varoitussanoman.

## <a name="dom-processing"></a>DOM-käsittely

DOM suoritetaan vain erätyönä. Voit määrittää DOM-suoritusten erätyön seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Jaettu tilausten hallinta \> Eräkäsittely \> DOM-käsittelijän työasetukset**.
1. Valitse **Parametrit**-pikavälilehden **Täyttämisprofiili** -kentässä profiili, jota varten DOM suoritetaan.
1. Valitse **Suorita taustalla** -pikavälilehden **Eräryhmä**-kentässä määritetty eräryhmä.
1. Kirjoita **Tehtävän kuvaus** -kenttään erätyön nimi.
1. Määritä **Toistuminen**-kohdassa erätyön toistuminen.
1. Valitse **OK**.

Käsittelyn aikana DOM ottaa huomioon seuraavassa kuvatut tilaukset ja tilausrivit:

- Myyntitilauksen alkuperään, toimitustapaan ja yritykseen liittyvät DOM-profiilissa määritetyt ehdot täyttävät tilausrivit, jotka täyttävät myös jonkin seuraavista ehdoista:

    - Ne on luotu Commerce-kanavista.
    - DOM ei ole koskaan välittänyt niitä
    - DOM on välittänyt niitä aiemmin, mutta ne on merkitty poikkeuksiksi ja ovat yritysten määrän raja-arvon alapuolella.
    - Toimitustapa ei ole nouto tai sähköinen toimitus.
    - Niitä ei ole merkitty toimitusta varten.
    - Niitä ei ole manuaalisesti poissuljettu.

- Tilaukset,jotka eivät ole pidossa.

Sen jälkeen, kun jaettu tilausten hallinta on käyttänyt sääntöjä, varaston rajoituksia ja optimointia, jaettu tilausten hallinta valitsee lähinnä asiakkaan toimitusosoitetta olevan sijainnin. Jaettu tilausten hallinta muuntaa **Toimitus**-tyypin osoitteet leveys- ja pituusastearvoiksi. Tämän jälkeen se muuntaa myyntitilauksen toimitusosoitteen leveys- ja pituusastearvoksi sekä päivittää osoitteen leveys- ja pituusastearvot tulevaa käyttöä varten. Jaettu tilausten hallintaa määrittää Bing Maps -palvelun avulla tarkat leveys- ja pituusastearvot osoite-, paikkakunta- ja postinumerotietojen perusteella.

Jaettu tilausten hallintaa laskee Bing Maps -ohjelmointirajapinnan avulla etäisyyden linnuntietä tai teitä pitkin määritettyjen asetusten mukaan. Se käyttää sitten näitä tietoja toimituskustannusten määrittämiseen. Optimointimalli priorisoi koko tilauksen täyttämisen yhdestä sijainnista. Vaikka osa tilauksesta olisi saatavana saman paikkakunnan tai postinumeron alueella, malli on optimoitu pienentämään lähetysten määrää. 

Jaettu tilausten hallinta hakee saatavana olevaa varastoa tarkastelemalla käytettävissä olevaa varastoa varaston V2-entiteeteissä. Jaettu tilausten hallinta erittelee tilauksen eriksi kunkin erän suorittamisen aikana profiilissa määritettyjen tehtävien **DOM-käsittelijä**-parametrin arvon mukaan. Tämän parametrin oletusarvo on **2 000**. Jos suorituksessa optimoidaan esimerkiksi 10 000 tilausriviä ja **DOM-käsittelijä**-parametrin asetuksena on oletusarvo **2 000**, jaettu tilausten hallinta luo viisi samanaikaisesti käsiteltävää erää. Tämän jälkeen täyttämissuunnitelmat hankitaan optimointitoiminnosta ja ne kohdistetaan riville. Jos tilausrivi on jaettava kahteen sijaintiin, jaettu tilausten hallinta varmistaa, että hinnat ja verot jaetaan riveille oikein.

![Myyntitilausten ehdot](./media/ordercriteria.png "Myyntitilausten ehdot")

## <a name="results-of-dom-runs"></a>Jaetun tilausten hallinnan suoritusten tulokset

Jos täyttämisprofiiliksi valitaan **Automaattinen käyttö**, suorituksen tulokset kohdistetaan automaattisesti myyntitilausriveille ja täyttämissuunnitelmaa voidaan tarkastella erikseen. Jos täyttämisprofiiliksi ei kuitenkaan ole määritetty **Automaattinen käyttö**, ajon tulokset näkyvät vain täyttämissuunnitelman näkymässä. 

Näet kaikki luodut täyttämissuunnitelmat seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Jaettu tilausten hallinta \> Jaettu tilausten hallinta**.
2. Valitse **Jaettu tilausten hallinta** -työtilassa **Täyttämissuunnitelmat**-ruutu.
3. Voit tarkastella haluttua täyttämissuunnitelmaa valitsemalla sen tunnuksen.

    Täyttämissuunnitelman tilaustietojen osassa näkyvät alkuperäiset myyntitilausrivit, jotka kuuluivat ajoon. Normaalien myyntitilausrivien kenttien lisäksi tilaustietojen osassa on myös seuraavat kolme DOM-kenttää:

    - **Täyttämistyyppi** – Kenttä ilmaisee, onko myyntitilausrivi kokonaan vai osittain välitetty vai onko sitä ollenkaan välitetty sijaintiin.
    - **Jako** – Tämä kenttä ilmaisee, onko jokin myyntitilausrivi jaettu ja välitetty eri sijainteihin.
    - **Täyttämissijaintien määrä** – Tämä kenttä ilmaisee, kuinka monta täyttämisriviä luotiin yhdelle myyntitilausriville (perustuen niiden sijaintien määrään, joihin alkuperäinen myyntitilausrivi välitettiin).

    Tilauksen täyttämistiedoissa näkyy alkuperäisten myyntitilausrivien määritys eri sijainteihin sekä niiden määrät.

## <a name="order-line-actions-and-statuses"></a>Tilausrivin toiminnot ja tilat

Seuraavassa kuvataan tilausrivin asetukset. Voit avata tilausrivin siirtymällä kohtaan **Retail ja Commerce \> Asiakkaat \> Kaikki myyntitilaukset**.

- Jos määrität **Jätä pois DOM-käsittelystä** -asetuksen (myyntitilausrivin **Yleiset**-välilehdessä) arvoksi **Kyllä**, tilaus tai tilausrivi jätetään pois DOM-käsittelystä.
- **DOM-tila**-kenttään (myyntitilausrivin **Yleiset**-välilehdessä) voidaan määrittää jokin seuraavista arvoista:

    - **Ei mitään** – tilausriviä ei ole koskaan välitetty.
    - **Valmis** – tilausrivi on onnistuneesti välitetty ja määritetty sijaintiin.
    - **Poikkeus** – Tilausrivi on välitetty, mutta sitä ei voi määrittää sijaintiin. Poikkeuksia on useita alatyyppejä, joita voidaan tarkastella DOM-työtilassa:

        - **Ei käytettävissä olevaa määrää** – ei ole olemassa käytettävissä olevaa varastoa tilauksen määrittämiseksi sijainteihin.
        - **Hylkäysten enimmäismäärä** – tilausrivi on saavuttanut hylkäysten määrän ylärajan.
        - **Tietojen muutoksen ristiriita** – myyntitilausriviä on muutettu tilauksen välittämisen jälkeen. Siksi täyttämissuunnitelmaa ei voi käyttää tilaukseen.
        - **Tilausrivikohtainen poikkeus** – tilausrivillä on useita poikkeuksia.

- Myyntitilausta syötettäessä DOM voidaan suorittaa vuorovaikutteisessa tilassa. Kun olet syöttämässä tilausriviä ja olet määrittänyt tuotteen ja määrän, voit valita **Päivitä rivi** ja sitten (kohdassa **DOM**) **Ehdota täyttämissijaintia**. Tällöin näet sijaintiluettelon, joka perustuu DOM-sääntöihin, jotka voivat täyttää tilausrivin määrän. Tämä luettelo on lajiteltu etäisyyden mukaan. Valitse sijainti määrittääksesi asianmukaisen toimipisteen ja varaston myyntitilausrivillä. Jotta tätä toimintoa voisi käyttää, on oltava olemassa aktiivinen täyttämisprofiili, joka vastaa myyntirivin myynnin alkuperää ja toimitustapaa.
- Voit tarkastella DOM-suoritusten myyntitilausriviä koskevia lokeja valitsemalla **Myyntitilausrivi** ja sitten kohdassa **DOM** **Näytä DOM-lokit**. DOM-lokeissa näkyvät kaikki DOM-suorituksen luomat tapahtumat ja lokit. Lokien avulla voit selvittää, miksi tietty sijainti määritettiin tietylle tilausriville ja mitä sääntöjä ja rajoituksia määrityksessä otettiin huomioon. **Hallinta**-välilehdessä DOM-lokeja voi tarkastella myös myyntitilauksen otsikon tasolla.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>DOM-täyttämissuunnitelmien puhdistustyö

DOM-käsittelyn aikana luodaan täyttämissuunnitelmia. Ajan kuluessa järjestelmään kertyy paljon täyttämissuunnitelmia. Voit hallita järjestelmän säilyttämien täyttämissuunnitelmien määrää määrittämällä erätyön, joka poistaa vanhoja täyttämissuunnitelma **Pidätyskausi päivinä** -arvon perusteella.

1. Siirry kohtaan **Retail ja Commerce \> Jaettu tilausten hallinta \> Eräkäsittely \> DOM-täyttämistietojen poistotyön asetukset**. 
1. Valitse määritetty eräryhmä **Eräryhmä**-kentässä.
1. Määritä **Toistuminen**-kohdassa erätyön toistuminen.
1. Valitse **OK**.

## <a name="more-information"></a>Lisätietoja

Seuraavat asiat on hyvä huomioida DOM-ominaisuutta käytettäessä:

- Tällä hetkellä DOM tarkastelee vain Commerce-kanavissa luotuja tilauksia. Myyntilaukset tunnistetaan vähittäismyynnin myyntitilauksiksi, kun **Commerce-myynti**-asetukseksi on määritetty **Kyllä**.
- Microsoft ei ole testannut jaettua tilausten hallintaa edistyneen varastonhallinnan ominaisuuksien kanssa. Niinpä asiakkaiden ja kumppanien on huolellisesti selvitettävä, onko jaettu tilausten hallinta yhteensopiva käytössä olevien edistyneen varastonhallinnan ominaisuuksien ja prosessien kanssa. Edistynyt varastointi ottaa käyttöön sellaiset määritettävissä olevat dimensiot, kuten varaston tilan, jotka eivät anna tarkkoja tietoja käytettävissä olevasta varastosta. Jaettu tilausten hallinta laajentaa tapaa, jolla käytettävissä oleva varasto voidaan määrittää edistynyttä varastointia käyttäviin toteutuksiin. Sitä voidaan käyttää varaston tilan ja muiden dimensioiden mukautettujen arvojen kanssa.

    Jaetun tilausten hallinnan laajennettavuus on rajallista, koska optimointi tapahtuu valmiissa optimoinnin ja sen rajoituksen huomioonottavassa MIP-mallissa. Varaston ja jälkikäsittelyn optimoinnin määrittämiseen on jo saatavana useita laajennettavia kohtia. Jaetun tilausten hallinnan profiileissa voi olla eroja myynnin alkuperän ja toimitustilan mukaan. Myyntitilauksen alkuperä voidaan määrittää tilauksen käsittelyn aikana, ja näiden arvojen perusteella voidaan käyttää erilaisia optimointistrategioita. Jaettu tilausten hallinta tukee myös sellaisten mukautettujen erätöiden luontia, jotka käyttävät DOM-käsittelijän tehtävää syötteenä ja antavat mahdollisuuden profiilin siirtämiseen parametrina. Niinpä erilaisia liiketoimintaskenaarioita voidaan tukea suorittamalla optimointi toisensa jälkeen.

- Jaettu tilausten hallinta on saatavana vain Commercen pilvipalveluversiossa. Sitä ei tueta paikallisissa ympäristöissä


[!INCLUDE[footer-include](../includes/footer-banner.md)]
