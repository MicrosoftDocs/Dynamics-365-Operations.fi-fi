---
title: Jaettu tilausten hallinta (DOM)
description: Tässä aiheessa kuvataan Dynamics 365 Commerce -ohjelman jaetun tilausten hallinnan (DOM) toimintoja.
author: josaw1
ms.date: 01/08/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 442a7449e0b28e1086d50ab68dbaf85370fce8ea6e178dd91ad972a2b47d7de3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717694"
---
# <a name="distributed-order-management-dom"></a>Jaettu tilausten hallinta (DOM)

[!include [banner](includes/banner.md)]

Kaupankäynnin uudella aikakaudella myyjät pyrkivät tarjoamaan mukautettuja asiakkaan aktivointitoimia, monikanavaisia käyttökokemuksia ja sujuvaa vuorovaikutusta. Koska valinnanmahdollisuudet ovat lähes rajattomat, kuluttajat ostavat sieltä, mistä he saavat miellyttävimmän ostokokemuksen. Pelkät hinnat ja tuotteet eivät välttämättä enää ole tärkeimpiä perusteita kuluttajille.

Asiakaskokemuksen parantamiseksi vähittäismyyjillä on oltava näkyvyys varastoon reaaliaikaisesti ja kaikissa eri kanavissa. Yksi kokonaisvaltainen näkymä varastoon voi auttaa optimoimaan tilausten toteuttamisen, kohdistamisen ja jakelun. Siksi jaetun tilausten hallinnan (DOM) järjestelmän käyttöönotto on muuttumassa entistä tärkeämmäksi vähittäismyyjille.

DOM optimoi tilausten toteutuksen järjestelmien ja prosessien monimutkaisessa verkostossa. Se perustuu yhteen yhtenäiseen varastonäkymään kaikkialla organisaatiossa, jotta tilauksia voitaisiin hallita ja toteuttaa entistä tarkemmin ja kustannustehokkaammin. Parantamalla vähittäismyyjän toimitusketjun tehokkuutta DOM auttaa vähittäismyyjää vastaamaan asiakkaiden odotuksiin.

Seuraavassa kuvassa näkyy myyntitilauksen elinkaari DOM-järjestelmässä.

![Myyntitilauksen elinkaari DOM-kontekstissa.](./media/flow.png "Myyntitilauksen elinkaari DOM-kontekstissa")

## <a name="set-up-dom"></a>DOM:n määrittäminen

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
    - **Selvityksen tyyppi** – Valitse arvo. Commercessa vapautetaan kaksi selvityksen tyyppiä: **Tuotannon selvitys** ja **Yksinkertaistettu selvitys**. Kaikille koneille, jotka suorittavat DOM:n (siis kaikki palvelimet, jotka kuuluvat DOMBatch-ryhmään), on valittava **Tuotannon selvitys**. Tuotannon selvitys edellyttää erityisen lisenssiavaimen, joka oletusarvoisesti lisensoidaan ja otetaan käyttöön tuotantoympäristöissä. Muille kuin tuotantoympäristöille tämä lisenssiavain on otettava käyttöön manuaalisesti. Voit ottaa lisenssiavaimen käyttöön manuaalisesti toimimalla seuraavasti:

        1. Avaa Microsoft Dynamics Lifecycle Servicesissa jaettu omaisuuskirjasto, valitse omaisuustyypiksi **Malli**, ja lataa **DOM-käyttöoikeus**-tiedosto.
        1. Käynnistä Microsoft IIS -palveluiden hallinta, valitse hiiren kakkospainikkeella **AOSService-verkkosivusto** ja valitse sitten **Selaa**. Windowsin resurssienhallintaikkuna avautuu kansiossa **\<AOS service root\>\\webroot**. Kirjoita muistiin hakemiston \<AOS Service root\> polku, sillä sitä käytetään seuraavassa vaiheessa.
        1. Kopioi määritystiedosto hakemistoon **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        1. Siirry Headquarters-asiakasohjelmaan ja avaa **DOM-parametrit**-sivu. Valitse **Selvitys**-välilehden **Selvityksen tyyppi** -kentässä **Tuotannon selvitys** ja varmista, ettei virhesanomia ole näkyvissä.


        > [!NOTE]
        > Yksinkertaistettu selvitys on vaihtoehto silloin, kun vähittäismyyjä haluaa kokeilla DOM-ominaisuutta ottamatta käyttöön erityistä lisenssiä. Organisaatioiden ei tulisi käyttää yksinkertaistettua selvitystä tuotantoympäristöissä.
        >
        > Tuotannon selvitys parantaa suorituskykyä (kuten tilauksien ja tilausrivien määrää, joka voidaan käsitellä yhden suorituksen aikana) ja tulosten yhdistämistä (koska tilauserä ei ehkä tuota parhaita tuloksia joissakin tilanteissa). Jotkin säännöt, kuten **Osittaistilaukset**-sääntö ja **Sijaintien enimmäismäärä** -sääntö, edellyttävät tuotannon selvitystä.
     
6. Siirry takaisin kohtaan **Retail ja Commerce \> Jaettu tilausten hallinta \> Asetukset \> DOM-parametrit**.
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

    - **Vähimmäisvarastosääntö** – Tämäntyyppisen säännön avulla organisaatiot voivat merkitä tuotteen tietyn määrän erityiseksi muihin tarkoituksiin kuin tilauksen täytäntöönpanoon. Esimerkiksi organisaatiot eivät ehkä halua DOM-suorituksen kohdistavan myymälässä saatavilla olevan varaston koko määrää tilausten täytäntöönpanoon. Sen sijaan voidaan haluta varata osa saldosta fyysiseen kauppaan tuleville asiakkaille. Kun käytetään tämäntyyppistä sääntöä, voidaan määrittää vähimmäisvarasto, jota täytyy ylläpitää tietylle tuoteluokalle, yksittäiselle tuotteelle tai tuotevariantille yhtä sijaintia tai sijaintiryhmää kohden.
    - **Täyttämissijainnin prioriteettisääntö** – Tämäntyyppisen säännön avulla organisaatiot voivat määrittää sijaintihierarkian DOM-moduulin priorisointia varten, kun se yrittää tunnistaa tiettyjen tuotteiden täyttämissijainnit. Prioriteettien arvot voivat olla välillä on 1–10, jossa 1 on suurin prioriteetti ja 10 on pienin prioriteetti. Suuren prioriteetin sijainteja käytetään ennen sijainteja, joilla on alhaisempi prioriteetti. Jos sääntö määritetään kovana rajoitussääntönä, tilaukset välitetään vain sijainteihin, joille on määritetty prioriteetti.
    - **Osittaistilausten sääntö** – Tämän säännön avulla organisaatiot voivat määrittää, voidaanko tilaus tai tilausrivit toteuttaa vain osittain. Seuraavat parametrit ovat käytettävissä:

        - **Täytetäänkö osittaistilaukset?** – Jos tämä asetus on **Kyllä**, DOM voi täyttää vain osan tilausrivin määrästä. Osittainen täyttäminen saavutetaan jakamalla tilausrivi.
        - **Täytetäänkö osittaiset rivit?** – Jos tämä asetus on **Kyllä**, DOM voi täyttää vain osan tilausrivien määristä. Osittainen täyttäminen saavutetaan jakamalla tilausrivi.
        - **Täytä tilaus vain yhdestä sijainnista** – Jos tämä asetus on **Kyllä**, DOM varmistaa, että tilauksen kaikki rivit täytetään yhdestä sijainnista.


        Seuraavassa taulukossa kuvataan toimintaa, kun määritetään näiden parametrien yhdistelmiä.

        | Yhdistelmänumero | Täytä osittaistilaukset | Täytä osittaiset rivit | Täytä tilaus vain yhdestä sijainnista | Kuvaus |
        |------|------------------------|-----------------------|--------------------------------------|-------------|
        | 1    | Kyllä                    | Kyllä                   | Kyllä                                  | Tilauksesta voidaan täyttää vain muutama rivi ja yksittäiset rivit voidaan täyttää osittain, mutta kaikki rivit tulee täyttää samasta sijainnista DOM-suoritusesiintymän yhteydessä. (Tätä yhdistelmää ei tueta tällä hetkellä.) |
        | 2    | Kyllä                    | Ei                    | Kyllä                                  | Tilauksesta voidaan täyttää vain muutama rivi, mutta yksittäisiä rivejä ei voida täyttää vain osittain, ja kaikki täytetyt rivit tulee täyttää samasta sijainnista DOM-suoritusesiintymän yhteydessä. (Tätä yhdistelmää ei tueta tällä hetkellä.) |
        | 3    | Kyllä                    | Kyllä                   | Ei                                   | Tilauksesta voidaan täyttää vain muutama rivi, yksittäiset rivit voidaan täyttää vain osittain, ja kukin rivi voidaan täyttää useammasta kuin yhdestä sijainnista DOM-suoritusesiintymän yhteydessä. |
        | 4\*  | Ei                     | Ei käytettävissä        | Ei                                   | Kaikki tilausrivit on täytettävä, yksittäisiä rivejä ei voida täyttää vain osittain ja kukin tilausrivi voidaan täyttää eri sijainnista. |
        | 5\*  | Ei                     | Ei käytettävissä        | Kyllä                                  | Kaikki tilausrivit on täytettävä, yksittäisiä rivejä ei voida täyttää vain osittain ja kaikki tilausrivit voidaan toimittaa vain yhdestä sijainnista. |
        | 6\*  | Ei                     | Ei käytettävissä        | Ei                                   | Tämä yhdistelmä toimii samalla tavalla kuin yhdistelmä 4, koska **Täytä osittaiset rivit** -asetukseksi ei voi määrittää **Kyllä**, kun **Täytä osittaistilaukset** -asetuksella on arvo **Ei**. |
        | 7\*  | Ei                     | Ei käytettävissä        | Kyllä                                  | Tämä yhdistelmä toimii samalla tavalla kuin yhdistelmä 5, koska **Täytä osittaiset rivit** -asetukseksi ei voi määrittää **Kyllä**, kun **Täytä osittaistilaukset** -asetuksella on arvo **Ei**. |
        | 8    | Kyllä                    | Ei                    | Ei                                   | Tilauksesta voidaan täyttää vain muutama rivi, mutta yksittäisiä rivejä ei voida toteuttaa vain osittain, ja eri tilausrivit voidaan täyttää useammasta kuin yhdestä sijainnista DOM-suoritusesiintymän yhteydessä. |
        | 9\*  | Ei                     | Ei käytettävissä        | Kyllä                                  | Kaikki tilausrivit on täytettävä ja ne on täytettävä vain yhdestä sijainnista. |

        \* Jos **Täytä osittaistilaukset** -asetukseksi määritetään **Ei**, **Täytä osittaiset rivit** -asetuksen arvona on aina arvo **Ei** riippumatta siitä, mikä arvo asetukseen on määritetty.

        > [!NOTE]
        > Retail-sovelluksen versiossa 10.0.5 **Täytä tilaus vain yhdestä sijainnista** -parametrin arvoksi muutettiin **Täyttämissijaintien enimmäismäärä**. Sen sijaan, että käyttäjä voisi määrittää tilausten täyttämisen vain yhdestä sijainnista tai niin useasta sijainnista kuin mahdollista, käyttäjät voivat nyt määrittää, voidaanko tilaus täyttää tietystä sijaintijoukosta (enintään 5 sijaintia) tai niin useasta sijainnista kuin on mahdollista. Tämä mahdollistaa aiempaa joustavamman tilauksen täyttämissijaintien määrän määrittämisen. Tämä sääntö toimii vain tuotannon selvityksen kanssa. 

   - **Offline-täyttämisen sijaintisääntö** – tämän säännön avulla organisaatiot voivat määrittää sijainnin tai sijaintiryhmän offline-sijainniksi tai DOM:n ulkopuolelle, jotta tilauksia ei voi määrittää täytettäväksi näistä sijainneista.
    - **Hylkäysten enimmäismäärän sääntö** – Tämän säännön avulla organisaatiot voivat määrittää hylkäyksille raja-arvon. Kun raja-arvo saavutetaan, DOM-käsittelijä merkitsee tilauksen vai tilausrivin poikkeukseksi ja jättää sen jatkokäsittelyn ulkopuolelle.

        Sen jälkeen, kun tilausrivit on määritetty sijaintiin, sijainti voi hylätä määritetyn tilausrivin, koska se ei jostakin syystä pysty täyttämään tilausriviä. Hylätyt rivit merkitään poikkeukseksi ja palautetaan takaisin pooliin seuraavaa suorituskertaa varten. Seuraavan ajon aikana DOM yrittää määrittää hylätyn rivin toiseen sijaintiin. Myös uusi sijainti voi hylätä määritetyn tilausrivin. Tämä määrittämisen ja hylkäämisen sykli voi tapahtua useita kertoja. Kun hylkäysten määrä ylittää määritetyn raja-arvon, DOM merkitsee tilausrivin pysyväksi poikkeukseksi eikä enää ota kyseistä tilausriviä määritettäväksi. DOM ottaa tilausrivin uudelleen määritettäväksi vain, jos käyttäjä nollaa tilausrivin tilan manuaalisesti.

   - **Enimmäisetäisyyssääntö** – Tämä säännön avulla organisaatiot voivat määrittää enimmäisetäisyyden tilauksen täyttävälle sijainnille tai sijaintiryhmälle. Jos sijainnille on määritetty päällekkäisiä enimmäisetäisyyssääntöjä, DOM käyttää pienintä sijainnille määritettyä enimmäisetäisyyttä.
    - **Tilausten enimmäismäärän sääntö** – Tämän säännön avulla organisaatiot voivat määrittää tilausten enimmäismäärän, jonka sijainti tai sijaintiryhmä voi käsitellä kalenteripäivän aikana. Jos sijainnille määritetään tilausten enimmäismäärä yhden päivän aikana, DOM ei määritä uusia tilauksia kyseiseen sijaintiin kyseisen kalenteripäivän aikana.

   Seuraavassa on lueteltu yleisiä määritteitä, joita voidaan määrittää edellä esitellyille sääntötyypeille:

   - **Aloituspäivä** ja **Päättymispäivä** – Jokaiselle säännölle voidaan määrittää päivämääräväli voimassaoloajaksi näiden kenttien avulla.
   - **Ei käytössä** – Vain ne säännöt, joiden arvo tässä kentässä on **Ei**, otetaan huomioon DOM-suorituksessa.
   - **Tiukka rajoitus** – Sääntö voidaan määrittää tiukaksi rajoitukseksi tai ei-tiukaksi rajoitukseksi. Kukin DOM-suoritus käy läpi kaksi toistoa. Ensimmäisessä toistossa jokaista sääntöä pidetään tiukkana rajoituksena riippumatta tämän kentän arvosta. Toisin sanoen kaikki säännöt ovat käytössä. Ainoa poikkeus on **Sijainnin prioriteetti** -sääntö. Toisessa toistossa säännöt, joita ei ole määritetty tiukoiksi rajoituksiksi, poistetaan, ja tilauksille tai tilausriveille, joille ei määritetty sijaintia kaikkia sääntöjä käytettäessä, määritetään sijainnit.

10. Täyttämisprofiileja käytetään sääntökokoelmien, yritysten, myyntitilausten alkuperien ja toimitustapojen ryhmittelyyn. Jokainen DOM-suoritus on tiettyä täyttämisprofiilia varten. Näin organisaatiot voivat määrittää ja suorittaa sääntöjoukkoja yritysjoukossa sellaisille tilauksille, joilla on tietyt myyntitilauksen alkuperät ja toimitustavat. Jos siis pitää suorittaa eri sääntöjoukkoja myyntitilausten alkuperän tai toimitustavan mukaan, täyttämisprofiilit voidaan määrittää vastaavasti. Voit määrittää täyttämisprofiileita noudattamalla seuraavia ohjeita:  

    1. Siirry kohtaan **Retail ja Commerce \> Jaettu tilausten hallinta \> Asetukset \> Täyttämisprofiilit**.
    2. Valitse **Uusi**.
    3. Kirjoita arvot **Profiili**- ja **Kuvaus**-kenttiin.
    4. Määritä **Automaattinen tuloksen käyttö** -asetus. Jos määrität tämän asetuksen arvoksi **Kyllä**, profiilin DOM-suorituksen tulokset kohdistetaan automaattisesti myyntitilauksen riveille. Jos määrität arvoksi **Ei**, tuloksia voi tarkastella vain täyttämissuunnitelmassa. Niitä ei kohdisteta myyntitilausriveille.
    5. Jos haluat, että DOM-profiili suoritetaan tilauksille, joilla on kaikki myyntitilausten alkuperät (mukaan lukien tilaukset, joissa myyntitilauksen alkuperää ei ole määritetty), määritä **Käsittele tilaukset, joilla on tyhjä myynnin alkuperä** -asetuksen arvoksi **Kyllä**. Voit suorittaa profiilin vain joillekin myyntitilauksen alkuperille määrittämällä ne **Myynnin alkuperät** -sivulla jäljempänä esitetyllä tavalla.

    > [!NOTE]
    > Commerce 10.0.12:ssa ja sitä uudemmassa versiossa **Mahdollisuus määrittää täyttämisryhmä täyttämisprofiiliin** -vaihtoehto on oltava otettuna käyttöön **Ominaisuuden hallinta** -työtilassa. 
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

Sen jälkeen, kun DOM on käyttänyt sääntöjä, varaston rajoituksia ja optimointia, DOM valitsee sijainnin, joka on lähinnä asiakkaan toimitusosoitetta.

![Myyntitilausten ehdot.](./media/ordercriteria.png "Myyntitilausten ehdot")

## <a name="results-of-dom-runs"></a>DOM-suoritusten tulokset

Jos täyttämisprofiiliksi valitaan **Automaattinen käyttö**, suorituksen tulokset kohdistetaan automaattisesti myyntitilausriveille ja täyttämissuunnitelmaa voi tarkastella erikseen. Jos täyttämisprofiiliksi ei kuitenkaan ole määritetty **Automaattinen käyttö**, ajon tulokset näkyvät vain täyttämissuunnitelman näkymässä. 

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
- Microsoft ei ole testannut DOM-ominaisuutta edistyneen varastonhallinnan ominaisuuksien kanssa. Asiakkaiden ja kumppanien on huolellisesti selvitettävä, onko DOM yhteensopiva heille tärkeiden edistyneen varastonhallinnan ominaisuuksien ja prosessien kanssa.
- DOM on saatavissa vain Commerce-ratkaisun pilvipalveluversioon. Sitä ei tueta paikallisissa käyttöönotoissa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]