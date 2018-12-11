---
title: Jaettu tilausten hallinta (JTH)
description: "Tässä aiheessa kuvataan Microsoft Dynamics 365 for Retailin jaetun tilausten hallinnan (JTH) toimintoja."
author: josaw1
manager: AnnBe
ms.date: 11/15/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 8f1b07243ec2d42e47073d8d90f00ea563020d82
ms.contentlocale: fi-fi
ms.lasthandoff: 12/04/2018

---
# <a name="distributed-order-management-dom"></a>Jaettu tilausten hallinta (JTH)

[!include [banner](includes/banner.md)]

Vähittäismyynnin uudella aikakaudella myyjät pyrkivät tarjoamaan mukautettuja asiakkaan aktivointitoimia, monikanavaisia käyttökokemuksia ja sujuvaa vuorovaikutusta. Koska valinnanmahdollisuudet ovat lähes rajattomat, kuluttajat ostavat sieltä, mistä he saavat miellyttävimmän ostokokemuksen. Pelkät hinnat ja tuotteet eivät välttämättä enää ole tärkeimpiä perusteita kuluttajille.

Asiakaskokemuksen parantamiseksi vähittäismyyjillä on oltava näkyvyys varastoon reaaliaikaisesti ja kaikissa eri kanavissa. Yksi kokonaisvaltainen näkymä varastoon voi auttaa optimoimaan tilausten toteuttamisen, kohdistamisen ja jakelun. Siksi jaetun tilausten hallinnan (JTH) järjestelmän käyttöönotto on muuttumassa entistä tärkeämmäksi vähittäismyyjille.

JTH optimoi tilausten toteutuksen järjestelmien ja prosessien monimutkaisessa verkostossa. Se perustuu yhteen yhtenäiseen varastonäkymään kaikkialla organisaatiossa, jotta tilauksia voitaisiin hallita ja toteuttaa entistä tarkemmin ja kustannustehokkaammin. Parantamalla vähittäismyyjän toimitusketjun tehokkuutta JTH auttaa vähittäismyyjää vastaamaan asiakkaiden odotuksiin.

Seuraavassa kuvassa näkyy myyntitilauksen elinkaari JTH-järjestelmässä.

![Myyntitilauksen elinkaari JTH-kontekstissa](./media/flow.png "Myyntitilauksen elinkaari JTH-kontekstissa")

## <a name="set-up-dom"></a>JTH:n määrittäminen

1. Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.
2. Laajenna **Konfigurointiavaimet**-välilehdessä **Vähittäismyynti**-solmu ja valitse **Jaettu tilausten hallinta** -valintaruutu.
3. Siirry kohtaan **Vähittäismyynti \> Jaettu tilausten hallinta \> Asetukset \> JTH-parametrit**.
4. Määritä **Yleiset**-välilehdessä seuraavat arvot:

    - **Ota jaettu tilausten hallinta käyttöön** – Määritä tähän arvoksi **Kyllä**.
    - **Vahvista Bing Maps -palvelun käyttö JTH:ssa** – Määritä tähän arvoksi **Kyllä**.

        > [!NOTE]
        > Voit määrittää tähän arvoksi **Kyllä** vain, jos **Ota Bing Maps käyttöön** -asetuksen arvo **Bing Maps** -välilehdessä **Vähittäismyynnin yhteiset parametrit** -sivulla (**Vähittäismyynti \> Pääkonttorin asetukset \> Parametrit \> Vähittäismyynnin yhteiset parametrit**) on myös **Kyllä** ja jos **Bing Maps -avain** -kenttään annetaan kelvollinen avain.

    - **Pidätyskausi päivinä** – Määritä, kauanko JTH-ajojen luomia täyttämistilauksia säilytetään järjestelmässä. **JTH-täyttämistietojen poistotyön asetukset** -eräyö poistaa kaikki täyttämissuunnitelmat, jotka ovat tässä määritettyä päivien määrää vanhempia.
    - **Hylkäämiskausi (päivinä)** – Määritä, kuinka paljon aikaa pitää kulua, ennen kuin hylätty tilausrivi voidaan määrittää samaan sijaintiin.

5. Määritä **Selvitys**-välilehdessä seuraavat arvot:

    - **Automaattisten täyttämisyritysten enimmäismäärä** – Määritä, kuinka monta kertaa JTH-moduuli yrittää välittää tilausrivin valittuun sijaintiin. Jos JTH-moduuli ei voi välittää tilausriviä sijaintiin määritetyillä yrityskerroilla, se merkitsee tilausrivin poikkeukseksi. Tämän jälkeen rivi ohitetaan tulevissa suorituksissa, kunnes tila nollataan manuaalisesti.
    - **Paikallisen myymälän alueen säde** – Kirjoita arvo. Tämän kentän avulla määritetään, miten sijainnit ryhmitellään ja määritetään tasaveroisiksi etäisyyden osalta. Jos esimerkiksi annat arvon **100**, jokaista myymälää ja jakelukeskusta 100 mailin säteellä täyttämistilauksen osoitteesta pidetään tasaveroisena etäisyyden osalta.
    - **Selvityksen tyyppi** – Valitse arvo. Retailissa vapautetaan kaksi selvityksen tyyppiä: **Tuotannon selvitys** ja **Yksinkertaistettu selvitys**. Kaikille koneille, jotka suorittavat JTH:n (siis kaikki palvelimet, jotka kuuluvat DOMBatch-ryhmään), on valittava **Tuotannon selvitys**. Tuotannon selvitys edellyttää erityisen lisenssiavaimen, joka oletusarvoisesti lisensoidaan ja otetaan käyttöön tuotantoympäristöissä. Muille kuin tuotantoympäristöille tämä lisenssiavain on otettava käyttöön manuaalisesti. Voit ottaa lisenssiavaimen käyttöön manuaalisesti toimimalla seuraavasti:

        1. Avaa Microsoft Dynamics Lifecycle Servicesissa jaettu omaisuuskirjasto, valitse omaisuustyypiksi **Malli** ja lataa **JTH-lisenssi**-tiedosto.
        2. Käynnistä Microsoft IIS -palveluiden hallinta, napsauta hiiren kakkospainikkeella **AOSService-verkkosivusto**, ja valitse sitten **Selaa**. Windowsin resurssienhallintaikkuna avautuu kansiossa **\<AOS-palvelun pääkansio\>\\webroot**. Merkitse muistiin polku \<AOS-palvelun pääkansio\>, sillä sitä käytetään seuraavassa vaiheessa.
        3. Kopioi konfiguraatiotiedosto kansioon **\<AOS-palvelun pääkansio\>\\PackagesLocalDirectory\\DOM\\bin**.
        4. Siirry Retail-pääkonttorin asiakasohjelmaan ja avaa **JTH-parametrit**-sivu. Valitse **Selvitys**-välilehden **Selvityksen tyyppi** -kentässä **Tuotannon selvitys** ja varmista, ettei virhesanomia ole näkyvissä.

        > [!NOTE]
        > Yksinkertaistettu selvitys on vaihtoehto silloin, kun vähittäismyyjä haluaa kokeilla JTH-ominaisuutta ottamatta käyttöön erityistä lisenssiä. Organisaatioiden ei tulisi käyttää yksinkertaistettua selvitystä tuotantoympäristöissä.
        >
        > Vaikka yksinkertaistettu selvitys sisältää samat toiminnot kuin tuotannon selvitys, siinä on rajoituksia suorituskyvyn suhteen (tilauksien ja tilausrivien määrä, joka voidaan käsitellä yhden suorituksen aikana) ja tulosten yhdistämisen suhteen (tilauserä ei ehkä tuota parhaita tuloksia joissakin tilanteissa).
     
6. Siirry takaisin kohtaan **Vähittäismyynti \> Jaettu tilausten hallinta \> Asetukset \> JTH-parametrit**.
7. Määritä **Numerosarjat**-välilehdessä tarvittavat numerosarjat eri JTH-yksiköille.

    > [!NOTE]
    > Ennen kuin numerosarjat voidaan määrittää näille yksiköille, ne on määritettävä **Numerosarjat**-sivulla (**Organisaation hallinto \> Numerosarjat \> Numerosarjat**).

8. JTH-ominaisuus tukee erilaisia JTH-sääntöjen määrityksiä, ja organisaatiot voivat määrittää useita sääntöjä liiketoiminnan tarpeiden mukaan. JTH-säännöt voidaan määrittää sijaintiryhmälle tai yksittäiselle sijainnille sekä tietylle tuoteluokalle, tuotteelle tai variantille. Voit luoda JTH-säännöissä käytettävät sijaintien ryhmittelyt seuraavasti:

    1. Siirry kohtaan **Vähittäismyynti \> Kanavan asetukset \> Täytäntöönpanoryhmät**.
    2. Valitse **Uusi** ja kirjoita uuden ryhmän nimi ja kuvaus.
    3. Valitse **Tallenna**.
    4. Voit lisätä ryhmään yksittäisen sijainnin valitsemalla **Lisää rivi**. Vaihtoehtoisesti voit lisätä useita sijainteja valitsemalla **Lisää rivejä**.

9. Voit määrittää säännöt kohdassa **Vähittäismyynti \> Jaettu tilausten hallinta \> Asetukset \> Sääntöjen hallinta**. Tällä hetkellä tuetaan seuraavia JTH-sääntöjä:

    - **Vähimmäisvarastosääntö** – Tämäntyyppisen säännön avulla organisaatiot voivat merkitä tuotteen tietyn määrän erityiseksi muihin tarkoituksiin kuin tilauksen täytäntöönpanoon. Esimerkiksi organisaatiot eivät ehkä halua JTH-ajon kohdistavan myymälässä saatavilla olevan varaston koko määrää tilausten täytäntöönpanoon. Sen sijaan voidaan haluta varata osa saldosta fyysiseen kauppaan tuleville asiakkaille. Kun käytetään tämäntyyppistä sääntöä, voidaan määrittää vähimmäisvarasto, jota täytyy ylläpitää tietylle tuoteluokalle, yksittäiselle tuotteelle tai tuotevariantille yhtä sijaintia tai sijaintiryhmää kohden.
    - **Täyttämissijainnin prioriteettisääntö** – Tämäntyyppisen säännön avulla organisaatiot voivat määrittää sijaintihierarkian JTH-moduulin priorisointia varten, kun se yrittää tunnistaa tiettyjen tuotteiden täyttämissijainnit. Prioriteettien arvot voivat olla välillä on 1–10, jossa 1 on suurin prioriteetti ja 10 on pienin prioriteetti. Suuren prioriteetin sijainteja käytetään ennen sijainteja, joilla on alhaisempi prioriteetti. Jos sääntö määritetään kovana rajoitussääntönä, tilaukset välitetään vain sijainteihin, joille on määritetty prioriteetti.
    - **Osittaistilausten sääntö** – Tämän säännön avulla organisaatiot voivat määrittää, voidaanko tilaus tai tilausrivit toteuttaa vain osittain. Seuraavat parametrit ovat käytettävissä:

        - **Täytetäänkö osittaistilaukset?** – Jos tämä asetus on **Kyllä**, JTH voi täyttää vain osan tilausrivin määrästä. Osittainen täyttäminen saavutetaan jakamalla tilausrivi.
        - **Täytetäänkö osittaiset rivit?** – Jos tämä asetus on **Kyllä**, JTH voi täyttää vain osan tilausrivien määristä. Osittainen täyttäminen saavutetaan jakamalla tilausrivi.
        - **Täytä tilaus vain yhdestä sijainnista** – Jos tämä asetus on **Kyllä**, JTH varmistaa, että tilauksen kaikki rivit täytetään yhdestä sijainnista.

        Seuraavassa taulukossa kuvataan toimintaa, kun määritetään näiden parametrien yhdistelmiä.

        |      | Täytä osittaistilaukset | Täytä osittaiset rivit | Täytä tilaus vain yhdestä sijainnista | Kuvaus |
        |------|------------------------|-----------------------|--------------------------------------|-------------|
        | 1    | Kyllä                    | Kyllä                   | Kyllä                                  | Tilauksesta voidaan täyttää vain muutama rivi ja yksittäiset rivit voidaan täyttää osittain, mutta kaikki rivit tulee täyttää samasta sijainnista JTH-suoritusesiintymän yhteydessä. (Tätä yhdistelmää ei tueta tällä hetkellä.) |
        | 2    | Kyllä                    | Ei                    | Kyllä                                  | Tilauksesta voidaan täyttää vain muutama rivi, mutta yksittäisiä rivejä ei voida täyttää vain osittain, ja kaikki täytetyt rivit tulee täyttää samasta sijainnista JTH-suoritusesiintymän yhteydessä. (Tätä yhdistelmää ei tueta tällä hetkellä.) |
        | 3    | Kyllä                    | Kyllä                   | Ei                                   | Tilauksesta voidaan täyttää vain muutama rivi, yksittäiset rivit voidaan täyttää vain osittain, ja kukin rivi voidaan täyttää useammasta kuin yhdestä sijainnista JTH-suoritusesiintymän yhteydessä. |
        | 4\*  | Ei                     | Ei käytettävissä        | Ei                                   | Kaikki tilausrivit on täytettävä, yksittäisiä rivejä ei voida täyttää vain osittain ja kukin tilausrivi voidaan täyttää eri sijainnista. |
        | 5\*  | Ei                     | Ei käytettävissä        | Kyllä                                  | Kaikki tilausrivit on täytettävä, yksittäisiä rivejä ei voida täyttää vain osittain ja kaikki tilausrivit voidaan toimittaa vain yhdestä sijainnista. |
        | 6\*  | Ei                     | Ei käytettävissä        | Ei                                   | Tämä yhdistelmä toimii samalla tavalla kuin yhdistelmä 4, koska **Täytä osittaiset rivit** -asetukseksi ei voi määrittää **Kyllä**, kun **Täytä osittaistilaukset** -asetuksella on arvo **Ei**. |
        | 7\*  | Ei                     | Ei käytettävissä        | Kyllä                                  | Tämä yhdistelmä toimii samalla tavalla kuin yhdistelmä 5, koska **Täytä osittaiset rivit** -asetukseksi ei voi määrittää **Kyllä**, kun **Täytä osittaistilaukset** -asetuksella on arvo **Ei**. |
        | 8    | Kyllä                    | Ei                    | Ei                                   | Tilauksesta voidaan täyttää vain muutama rivi, mutta yksittäisiä rivejä ei voida toteuttaa vain osittain, ja eri tilausrivit voidaan täyttää useammasta kuin yhdestä sijainnista JTH-suoritusesiintymän yhteydessä. |
        | 9\*  | Ei                     | Ei käytettävissä        | Kyllä                                  | Kaikki tilausrivit on täytettävä ja ne on täytettävä vain yhdestä sijainnista. |

        \*Jos **Täytä osittaistilaukset** -asetukseksi määritetään **Ei**, **Täytä osittaiset rivit** -asetuksen arvona pidetään aina arvoa **Ei** riippumatta siitä, mikä arvo asetukseen on määritetty.

    - **Offline-täyttämisen sijaintisääntö** – Tämän säännön avulla organisaatiot voivat määrittää sijainnin tai sijaintiryhmän offline-sijainniksi tai JTH:n ulkopuolelle, jotta tilauksia ei voi määrittää täytettäväksi kyseisestä sijainnista.
    - **Hylkäysten enimmäismäärän sääntö** – Tämän säännön avulla organisaatiot voivat määrittää hylkäyksille raja-arvon. Kun raja-arvo saavutetaan, JTH-käsittelijä merkitsee tilauksen vai tilausrivin poikkeukseksi ja jättää sen jatkokäsittelyn ulkopuolelle.

        Sen jälkeen, kun tilausrivit on määritetty sijaintiin, sijainti voi hylätä määritetyn tilausrivin, koska se ei jostakin syystä pysty täyttämään tilausriviä. Hylätyt rivit merkitään poikkeukseksi ja palautetaan takaisin pooliin seuraavaa suorituskertaa varten. Seuraavan ajon aikana JTH yrittää määrittää hylätyn rivin toiseen sijaintiin. Myös uusi sijainti voi hylätä määritetyn tilausrivin. Tämä määrittämisen ja hylkäämisen sykli voi tapahtua useita kertoja. Kun hylkäysten määrä ylittää määritetyn raja-arvon, JTH merkitsee tilausrivin pysyväksi poikkeukseksi eikä enää ota kyseistä tilausriviä määritettäväksi. JTH ottaa tilausrivin uudelleen määritettäväksi vain, jos käyttäjä nollaa tilausrivin tilan manuaalisesti.

    - **Enimmäisetäisyyssääntö** – Tämä säännön avulla organisaatiot voivat määrittää enimmäisetäisyyden tilauksen täyttävälle sijainnille tai sijaintiryhmälle. Jos sijainnille on määritetty päällekkäisiä enimmäisetäisyyssääntöjä, JTH käyttää pienintä sijainnille määritettyä enimmäisetäisyyttä.
    - **Tilausten enimmäismäärän sääntö** – Tämän säännön avulla organisaatiot voivat määrittää tilausten enimmäismäärän, jonka sijainti tai sijaintiryhmä voi käsitellä kalenteripäivän aikana. Jos sijainnille määritetään tilausten enimmäismäärä yhden päivän aikana, JTH ei määritä uusia tilauksia kyseiseen sijaintiin kyseisen kalenteripäivän aikana.

    Seuraavassa on lueteltu yleisiä määritteitä, joita voidaan määrittää edellä esitellyille sääntötyypeille:

    - **Aloituspäivä** ja **Päättymispäivä** – Jokaiselle säännölle voidaan määrittää päivämääräväli voimassaoloajaksi näiden kenttien avulla.
    - **Ei käytössä** – Vain ne säännöt, joiden arvo tässä kentässä on **Ei**, otetaan huomioon JTH-suorituksessa.
    - **Tiukka rajoitus** – Sääntö voidaan määrittää tiukaksi rajoitukseksi tai ei-tiukaksi rajoitukseksi. Kukin JTH-suoritus käy läpi kaksi toistoa. Ensimmäisessä toistossa jokaista sääntöä pidetään tiukkana rajoituksena riippumatta tämän kentän arvosta. Toisin sanoen kaikki säännöt ovat käytössä. Ainoa poikkeus on **Sijainnin prioriteetti** -sääntö. Toisessa toistossa säännöt, joita ei ole määritetty tiukoiksi rajoituksiksi, poistetaan, ja tilauksille tai tilausriveille, joille ei määritetty sijaintia kaikkia sääntöjä käytettäessä, määritetään sijainnit.

10. Täyttämisprofiileja käytetään sääntökokoelmien, yritysten, myyntitilausten alkuperien ja toimitustapojen ryhmittelyyn. Jokainen JTH-suoritus on tiettyä täyttämisprofiilia varten. Näin organisaatiot voivat määrittää ja suorittaa sääntöjoukkoja yritysjoukossa sellaisille tilauksille, joilla on tietyt myyntitilauksen alkuperät ja toimitustavat. Jos siis pitää suorittaa eri sääntöjoukkoja myyntitilausten alkuperän tai toimitustavan mukaan, täyttämisprofiilit voidaan määrittää vastaavasti. Voit määrittää täyttämisprofiileita noudattamalla seuraavia ohjeita:  

    1. Siirry kohtaan **Vähittäismyynti \> Jaettu tilausten hallinta \> Asetukset \> Täyttämisprofiilit**.
    2. Valitse **Uusi**.
    3. Kirjoita arvot **Profiili**- ja **Kuvaus**-kenttiin.
    4. Määritä **Automaattinen tuloksen käyttö** -asetus. Jos määrität tämän asetuksen arvoksi **Kyllä**, profiilin JTH-ajon tulokset kohdistetaan automaattisesti myyntitilauksen riveille. Jos määrität arvoksi **Ei**, tuloksia voi tarkastella vain täyttämissuunnitelmassa. Niitä ei kohdisteta myyntitilausriveille.
    5. Jos haluat, että JTH-profiili suoritetaan tilauksille, joilla on kaikki myyntitilausten alkuperät (myös tilauksille, joissa myyntitilauksen alkuperää ei ole määritetty), määritä **Käsittele tilaukset, joilla on tyhjä myynnin alkuperä** -asetuksen arvoksi **Kyllä**. Voit suorittaa profiilin vain joillekin myyntitilauksen alkuperille määrittämällä ne **Myynnin alkuperät** -sivulla jäljempänä esitetyllä tavalla.
    6. Valitse **Yritykset**-pikavälilehdessä **Lisää** ja sitten haluttu yritys.
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

## <a name="dom-processing"></a>JTH-käsittely

JTH suoritetaan vain erätyönä. Voit määrittää JTH-ajojen erätyön seuraavasti.

1. Siirry kohtaan **Vähittäismyynti \> Jaettu tilausten hallinta \> Eräkäsittely \> JTH-käsittelijän työasetukset**.
1. Valitse **Parametrit**-pikavälilehden **Täyttämisprofiili** -kentässä profiili, jota varten JTH suoritetaan.
1. Valitse **Suorita taustalla** -pikavälilehden **Eräryhmä**-kentässä määritetty eräryhmä.
1. Kirjoita **Tehtävän kuvaus** -kenttään erätyön nimi.
1. Määritä **Toistuminen**-kohdassa erätyön toistuminen.
1. Valitse **OK**.

Käsittelyn aikana JTH ottaa huomioon seuraavassa kuvatut tilaukset ja tilausrivit:

- Myyntitilauksen alkuperään, toimitustapaan ja yritykseen liittyvät JTH-profiilissa määritetyt ehdot täyttävät tilausrivit, jotka täyttävät myös jonkin seuraavista ehdoista:

    - Ne on luotu vähittäismyyntikanavista.
    - JTH ei ole koskaan välittänyt niitä
    - JTH on välittänyt niitä aiemmin, mutta ne on merkitty poikkeuksiksi ja ovat yritysten määrän raja-arvon alapuolella.
    - Toimitustapa ei ole nouto tai sähköinen toimitus.
    - Niitä ei ole merkitty toimitusta varten.
    - Niitä ei ole manuaalisesti poissuljettu.

- Tilaukset,jotka eivät ole pidossa.

Sen jälkeen, kun JTH on käyttänyt sääntöjä, varaston rajoituksia ja optimointia, JTH valitsee sijainnin, joka on lähinnä asiakkaan toimitusosoitetta.

![Myyntitilauksen ehdot](./media/ordercriteria.png "Myyntitilauksen ehdot")

## <a name="results-of-dom-runs"></a>JTH-suoritusten tulokset

Jos täyttämisprofiiliksi valitaan **Automaattinen käyttö**, ajon tulokset kohdistetaan automaattisesti myyntitilausriveille ja täyttämissuunnitelmaa voi tarkastella erikseen. Jos täyttämisprofiiliksi ei kuitenkaan ole määritetty **Automaattinen käyttö**, ajon tulokset näkyvät vain täyttämissuunnitelman näkymässä. 

Näet kaikki luodut täyttämissuunnitelmat seuraavasti.

1. Siirry kohtaan **Vähittäiskauppa \> Jaettu tilausten hallinta \> Jaettu tilausten hallinta**.
2. Valitse **Jaettu tilausten hallinta** -työtilassa **Täyttämissuunnitelmat**-ruutu.
3. Voit tarkastella haluttua täyttämissuunnitelmaa valitsemalla sen tunnuksen.

    Täyttämissuunnitelman tilaustietojen osassa näkyvät alkuperäiset myyntitilausrivit, jotka kuuluivat ajoon. Normaalien myyntitilausrivien kenttien lisäksi tilaustietojen osassa on myös seuraavat kolme JTH-kenttää:

    - **Täyttämistyyppi** – Kenttä ilmaisee, onko myyntitilausrivi kokonaan vai osittain välitetty vai onko sitä ollenkaan välitetty sijaintiin.
    - **Jako** – Tämä kenttä ilmaisee, onko jokin myyntitilausrivi jaettu ja välitetty eri sijainteihin.
    - **Täyttämissijaintien määrä** – Tämä kenttä ilmaisee, kuinka monta täyttämisriviä luotiin yhdelle myyntitilausriville (perustuen niiden sijaintien määrään, joihin alkuperäinen myyntitilausrivi välitettiin).

    Tilauksen täyttämistiedoissa näkyy alkuperäisten myyntitilausrivien määritys eri sijainteihin sekä niiden määrät.

## <a name="order-line-actions-and-statuses"></a>Tilausrivin toiminnot ja tilat

Seuraavassa kuvataan tilausrivin asetukset. Voit avata tilausrivin siirtymällä kohtaan **Vähittäismyynti \> Asiakkaat \> Kaikki myyntitilaukset**.
- Jos määrität **Jätä pois JTH-käsittelystä** -asetuksen (myyntitilausrivin **Yleiset**-välilehdessä) arvoksi **Kyllä**, tilaus tai tilausrivi jätetään pois JTH-käsittelystä.
- **JTH-tila**-kenttään (myyntitilausrivin **Yleiset**-välilehdessä) voidaan määrittää jokin seuraavista arvoista:

    - **Ei mitään** – tilausriviä ei ole koskaan välitetty.
    - **Valmis** – tilausrivi on onnistuneesti välitetty ja määritetty sijaintiin.
    - **Poikkeus** – Tilausrivi on välitetty, mutta sitä ei voi määrittää sijaintiin. Poikkeuksia on useita alatyyppejä, joita voidaan tarkastella JTH-työtilassa:

        - **Ei käytettävissä olevaa määrää** – ei ole olemassa käytettävissä olevaa varastoa tilauksen määrittämiseksi sijainteihin.
        - **Hylkäysten enimmäismäärä** – tilausrivi on saavuttanut hylkäysten määrän ylärajan.
        - **Tietojen muutoksen ristiriita** – myyntitilausriviä on muutettu tilauksen välittämisen jälkeen. Siksi täyttämissuunnitelmaa ei voi käyttää tilaukseen.
        - **Tilausrivikohtainen poikkeus** – tilausrivillä on useita poikkeuksia.

- Myyntitilausta syötettäessä JTH voidaan suorittaa vuorovaikutteisessa tilassa. Kun olet syöttämässä tilausriviä ja olet määrittänyt tuotteen ja määrän, voit valita **Päivitä rivi** ja sitten (kohdassa **JTH**) **Ehdota täyttämissijaintia**. Tällöin näet sijaintiluettelon, joka perustuu JTH-sääntöihin, jotka voivat täyttää tilausrivin määrän. Tämä luettelo on lajiteltu etäisyyden mukaan. Valitse sijainti määrittääksesi asianmukaisen toimipisteen ja varaston myyntitilausrivillä. Jotta tätä toimintoa voisi käyttää, on oltava olemassa aktiivinen täyttämisprofiili, joka vastaa myyntirivin myynnin alkuperää ja toimitustapaa.
- Voit tarkastella JTH-ajojen myyntitilausriviä koskevia lokeja valitsemalla **Myyntitilausrivi** ja sitten kohdassa **JTH** **Näytä JTH-lokit**. JTH-lokeissa näkyvät kaikki JTH-ajon luomat tapahtumat ja lokit. Lokien avulla voit selvittää, miksi tietty sijainti määritettiin tietylle tilausriville ja mitä sääntöjä ja rajoituksia määrityksessä otettiin huomioon. **Hallinta**-välilehdessä JTH-lokeja voi tarkastella myös myyntitilauksen otsikon tasolla.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>JTH-täyttämissuunnitelmien puhdistusajo

JTH-käsittelyn aikana luodaan täyttämissuunnitelmia. Ajan kuluessa järjestelmään kertyy paljon täyttämissuunnitelmia. Voit hallita järjestelmän säilyttämien täyttämissuunnitelmien määrää määrittämällä erätyön, joka poistaa vanhoja täyttämissuunnitelma **Pidätyskausi päivinä** -arvon perusteella.

1. Siirry kohtaan **Vähittäismyynti \> Jaettu tilausten hallinta \> Eräkäsittely \> JTH-täyttämistietojen poistotyön asetukset**. 
1. Valitse määritetty eräryhmä **Eräryhmä**-kentässä.
1. Määritä **Toistuminen**-kohdassa erätyön toistuminen.
1. Valitse **OK**.

## <a name="more-information"></a>Lisätietoja

Seuraavat asiat on hyvä huomioida JTH-ominaisuutta käytettäessä:

- Tällä hetkellä JTH tarkastelee vain vähittäismyynnin kanavissa luotuja tilauksia. Myyntilaukset tunnistetaan vähittäismyynnin myyntitilauksiksi, kun **Vähittäismyynti** -asetukseksi on määritetty **Kyllä**.
- Microsoft ei ole testannut JTH-ominaisuutta edistyneen varastonhallinnan ominaisuuksien kanssa. Asiakkaiden ja kumppanien on huolellisesti selvitettävä, onko JTH yhteensopiva heille tärkeiden edistyneen varastonhallinnan ominaisuuksien ja prosessien kanssa.
- JTH on saatavissa vain Retail-ratkaisun pilvipalveluversioon. Sitä ei tueta paikallisissa käyttöönotoissa.

