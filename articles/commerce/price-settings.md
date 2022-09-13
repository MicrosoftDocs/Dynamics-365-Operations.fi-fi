---
title: Hinnoitteluasetukset
description: Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Commerce headquarters -sovelluksen hinnoittelun ja alennusten hallinnan erilaisista asetuksista.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-11
ms.openlocfilehash: 4bc8cb16e7960d26adbb9590b4ad83cf46b02838
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410759"
---
# <a name="pricing-settings"></a>Hinnoitteluasetukset

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Commerce headquarters -sovelluksen hinnoittelun ja alennusten hallinnan erilaisista asetuksista. Näiden asetusten avulla organisaatiot voivat määrittää Commerce-ratkaisun hinnoittelutoiminnan vastaamaan tiettyjä liiketoimintatarpeita.

## <a name="company-level-pricing-settings"></a>Yritystason hinnoitteluasetukset

Useimmat hinnoitteluasetukset ovat yritystasolla Commerce headquartersissa kohdassa **Commercen parametrit \> Hinnat ja alennukset**.

### <a name="best-price-and-compound-concurrency-control-model"></a>Parhaan hinnan ja yhdistelmän samanaikaisuuden hallintamalli

**Parhaan hinnan ja yhdistelmän samanaikaisuuden hallintamalli** -asetus määrittää, miten hinnoittelumoduuli käsittelee useita alennuksia **paras hinta**- tai **yhdistelmä**-samanaikaisuustilassa. 

Jos parametrin arvoksi on määritetty **Paras hinta ja yhdistelmä vain prioriteetissa, useissa prioriteeteissa ei koskaan yhdistelmä**, yhdistetään kaikki **yhdistelmä**-alennukset, joilla on sama hinnoitteluprioriteetti. Yhdistetty tulos kilpailee tämän jälkeen minkä tahansa **paras hinta** -alennuksen kanssa, jolla on sama hinnoitteluprioriteetti. Käytetään parasta hintaa ja kaikki alennukset, joilla on tätä alhaisempi hinnoitteluprioriteetti, ohitetaan.

Jos parametrin arvoksi määritetään **Paras hinta vain yhdessä prioriteetissa, useissa prioriteeteissa aina yhdistelmä**, kaikkia **yhdistelmä**-alennuksia käsitellään **paras hinta** -alennuksina. Hinnoitteluprioriteetissa vain yksi alennus voittaa. Jos kyseinen yksittäinen alennus on **paras hinta**- tai **yhdistelmä**-alennus, se yhdistetään kaikkiin **paras hinta**- tai **yhdistelmä**-alennuksiin, joilla on alhaisempi hinnoitteluprioriteetti.

### <a name="discount-compound-behavior"></a>Alennusyhdistelmän käyttäytyminen

**Alennusyhdistelmän käyttäytyminen** -asetus määrittää, miten hinnoittelumoduuli laskee useat yhdistelmäasennukset.

Jos parametriksi on määritetty **Yhdistelmä**, yksi alennus kohdistetaan toisen päälle kumulatiivisesti. Jos arvoksi on määritetty **Alkuperäisen hinnan yhdistelmä**, kaikkia alennuksia käsitellään yksitellen. Ne kohdistetaan samaan alkuperäiseen hintaan.

Tässä esimerkissä yhdistetään 10 prosentin ja 20 prosentin alennukset tuotteessa, jonka alkuperäinen hinta on 100 $. Jos määrität **Alennusyhdistelmän käyttäytyminen** -parametrin arvoksi **Yhdistelmä**, lopullinen hinta on 72 $ (100 $ &times; 90 % &times; 80 %). Jos määrität arvoksi **Alkuperäisen hinnan yhdistelmä**, lopullinen hinta on 70 $ (100 $ – 10 $ – 20 $).

### <a name="enable-competition-between-exclusive-threshold-and-other-periodic-discounts"></a>Salli kilpailu yksinomaisen raja-arvon ja muiden säännöllisten alennusten välillä

Jos **Salli kilpailu yksinomaisen raja-arvon ja muiden säännöllisten alennusten välillä** -parametrin arvoksi on määritetty **Kyllä**, hinnoittelumoduuli tekee eksklusiiviset alennukset rajan ylittyessä täysin sellaisten eksklusiivisten alennusten kanssa, jotka toteutuvat muulloin kuin rajan ylittyessä. Hinnoitteluprioriteetti on yhä voimassa. **Parhaan hinnan** ja **yhdistelmän** alennukset rajan ylittyessä pysyvät entisellään. Toisin sanoen he eivät kilpaile niiden alennusten kanssa, jotka toteutuvat muulloin kuin rajan ylittyessä.

### <a name="manual-line-discount-and-system-discount"></a>Manuaalinen rivialennus ja järjestelmäalennus

**Manuaalinen rivialennus ja järjestelmäalennus** -asetus määrittää, miten hinnoittelumoduuli käyttää manuaalista rivi- ja järjestelmäalennusta samalla rivillä. Manuaalinen rivialennus voidaan lisätä järjestelmän alennuksen päälle tai se voi korvata järjestelmäalennuksen. Kun manuaalinen rivialennus ja järjestelmäalennus yhdistetään, laskelmalogiikassa käytetään **Alennusyhdistelmän käyttäytyminen** -asetusta. Koko tilauksessa käytettävässä manuaalisessa kokonaisalennuksessa ei käytetä tätä asetusta.

### <a name="keep-items-on-the-same-sales-line-for-discount-price-rounding"></a>Säilytä nimikkeet samalla myyntirivillä alennushinnan pyöristystä varten

Joskus määräalennussumma ei jakaudu tasan määrällä, josta alennus annetaan (esimerkiksi jos kolmen ostetun yksikön alennussumma on 10 $). Näissä tapauksissa **Säilytä nimikkeet samalla myyntirivillä alennushinnan pyöristystä varten** -asetus määrittää, miten hinnoittelumoduuli kohdistaa ja jakaa alennussumman. Jos parametrin arvoksi määritetään **Kyllä**, alennussumma kohdistetaan kokonaan jakamatta sitä. Jos arvoksi määritetään **Ei**, alennussumma jaetaan määrällä, josta alennus annetaan, ja se pyöristetään. Esimerkiksi kolmen yksikön alennussumman 10 $ jakamisen jälkeen ensimmäiselle yksikölle jää alennukseksi 3,33 $, toiselle yksikölle 3,33 $ ja kolmannelle yksikölle 3,34 $.

### <a name="apply-discounts-to-key-in-price-products"></a>Käytä alennuksia Näppäile hinta -tuotteisiin

**Käytä alennuksia Näppäile hinta -tuotteisiin** -asetus määrittää, voiko alennuksia käyttää yhdessä Näppäile hinta -tuotteissa, jotka syötetään myyntipisteessä. Tuotteen määrityksen **Näppäile hinta** -asetus määrittää, tukeeko tuote Näppäile hinta -toimintoa ja miten se sitä tukee.

### <a name="apply-discounts-to-price-overrides"></a>Käytä alennuksia hinnan ohituksissa

**Käytä alennuksia hinnan ohituksissa** -asetus määrittää, voiko alennuksia käyttää yhdessä hinnan ohitusten kanssa.

### <a name="distribute-discounts-for-least-expensive-discounts"></a>Jaa alennukset vähiten kalleimman alennukselle

Vähiten kallis -laskelmatyyppiä käyttävien yhdistelmäalennusten **Jaa alennukset vähiten kalleimman alennukselle** -asetus määrittää, jakaako hinnoittelumoduuli alennuksen riveille.

Jos parametrin arvoksi on määritetty **Ei**, alennusta käytetään vain halvimmilla riveillä. Esimerkiksi Osta 2, saat 1 ilmaiseksi -yhdistelmäalennuksessa vähiten kallis nimike on ilmainen. Kaksi muuta nimikettä myydään täydellä hinnalla. Tällöin asiakas, joka palauttaa molemmat täysihintaset nimikkeet, saa kolmannen nimikkeen ilmaiseksi. Tämä tilanne saattaa aiheuttaa tappiota jälleenmyyjälle.

Jos parametrin arvoksi määritetään **Kyllä**, hinnoittelumoduuli jakaa alennuksen kaikille soveltuville riveille. Tämä asetus voi vähentää palautusten tappioita.

### <a name="manually-calculate-multi-line-prices-and-discounts"></a>Laske manuaalisesti usean rivin hinnat ja alennukset

**Laske manuaalisesti usean rivin hinnat ja alennukset** -asetus määrittää, käyttääkö hinnoittelumoduuli viivytettyä hinnan ja alennuksen laskemista myyntipistesovelluksessa ja puhelinkeskuskanavassa. Jos parametrin arvoksi on määritetty **Kyllä**, hinnoittelumoduuli ei laske heti useiden rivien alennuksia (kuten määräalennuksia, alennuksia rajan ylittyessä ja yhdistelmäalennuksia), jos myyntitilaus on luotu myyntipistesovelluksessa tai puhelinkeskuskanavassa tai jos sitä on muokattu niissä.

> [!NOTE]
> Commercen versiossa 10.0.30 tai aiemmassa versiossa **Laske manuaalisesti usean rivin hinnat ja alennukset** -asetus määrittää toiminnan vain puhelinkeskuskanavassa. Erillinen **Laske manuaalisesti moninimikealennukset** -asetus toimintoprofiili määrittää hinnan laskennan toimintatavan myyntipistesovelluksessa. Commercen versiossa 10.0.31 nämä kaksi asetusta yhdistetään yhdeksi yritystason asetukseksi.

### <a name="retention-period-in-days"></a>Pidätyskausi päivinä

**Pidätyskausi päivinä** -asetus osoittaa, miten monta päivää vanhenemispäivän (jos se on määritetty) tai käytöstäpoistopäivän (jos vanhenemispäivää ei ole määritetty) jälkeen alennus tulee poistaa järjestelmällisesti. Jos parametrin arvoksi on määritetty **0** (nolla), automaattista poistoa ei tehdä.

> [!NOTE]
> Commercen versiossa 10.0.30 ja vanhemmissa versioissa asetuksen nimi on **Niiden päivien määrä, joiden jälkeen vanhentuneet alennukset poistetaan**.

### <a name="coupon-bar-code"></a>Kupongin viivakoodi

**Kupongin viivakoodi** -asetus määrittää, mitä erityistä viivakoodia käytetään kupongin viivakoodien luomisessa. Käyttäjät voivat valita yhden ennalta määritetyistä viivakoodeista, jotka on määritetty **Viivakoodiasetukset**-sivulla. Lisätietoja viivakoodeista ja viivakoodien muotoiluista on kohdassa [Viivakoodien määrittäminen](set-up-bar-codes.md) ja [Viivakoodin muotojen määrittäminen](set-up-bar-code-masks.md).

### <a name="coupon-code-must-be-manually-applied-to-return-transactions"></a>Kuponkikoodi on otettava käyttöön manuaalisesti palautustapahtumissa

**Kuponkikoodi on otettava käyttöön manuaalisesti palautustapahtumissa** -asetusta käytetään vain niissä palautustapahtumissa, joista ei ole myyntikuittia. Määritä parametrin arvoksi **Ei**, jos kuponki on otettava automaattisesti käyttöön tapahtumassa. Määritä arvoksi **Kyllä**, jos kuponki on liitettävä tapahtumaan manuaalisesti.

### <a name="use-sales-agreements-set-up-for-the-organization"></a>Käytä organisaatiolle määritettyjä myyntisopimuksia

Jos **Käytä organisaatiolle määritettyjä myyntisopimuksia** -parametrin arvoksi on määritetty **Kyllä** yritysten välisissä tilauksissa, hinnoittelumoduuli käyttää organisaatiolle käyttäjän asiakashierarkiassa määritettyjä myyntisopimuksia sopimuspohjaisen hinnan määrittämiseksi. Jos parametrin arvoksi on määritetty **Ei** tai jos asiakashierarkiaa ei ole määritetty, hinnoittelumoduuli etsii käyttäjälle määritetyt myyntisopimukset sopimuspohjaisen hinnan määrittämiseksi. Lisätietoja yritystenvälisen sähköisen kaupankäynnin asiakashierarkioista on kohdassa [Yritystenvälisten liikekumppanien hallinta asiakashierarkioiden avulla](b2b/partners-customer-hierarchies.md).

## <a name="channel-level-pricing-settings"></a>Yritystason hinnoitteluasetukset

Seuraavien asetusten avulla organisaatiot voivat ohjata tiettyjen myyntikanavien hinnoittelutapaa.

### <a name="enable-order-price-control"></a>Ota käyttöön hintasäätely

**Ota käyttöön hintasäätely** -parametri sijaitsee **Puhelinkeskuksen määritys** -sivun **Yleistä**-pikavälilehdessä. Asetus määrittää, soveltaako hinnoittelumoduuli hinnanohitustoiminnon rajoitusta puhelinkeskuskanavassa. Se toimii yhdessä tuotetason **Salli hinnan oikaisu**-asetuksen kanssa.

Jos tilauksen hintasäätely on poistettu käytöstä, kuka tahansa puhelinkeskuksen käyttäjä voi tehdä hinnanmuutoksia myyntiriveille puhelinkeskuskanavassa riippumatta siitä, sallitaanko hinnan oikaisu vastaavissa tuotteissa.

Jos tilauksen hintasäätely on otettu käyttöön, vain tuotteet, joissa **Salli hinnan oikaisu** -parametrin arvoksi on määritetty **Kyllä**, sallivat hinnan ohitukset puhelinkeskuskanavan myyntitilauksissa. Tällöin vastaaville myyntiriveille on annettava syykoodi. Puhelinkeskuksen käyttäjä voi muuttaa myyntihintaa vain **Kustannuksen lisäprosentti** -arvon verran. Se määritetään kohdassa **Vähittäismyynti ja kaupankäynti \> Kanavan asetukset \> Puhelinkeskuksen asetukset \> Ohitusoikeudet**. Jos hinnan ohitus ylittää kyseisen prosenttiluvun, käyttäjän on lähetettävä pyyntö. Se käsitellään ennalta määritetyssä Commerce-työnkulussa tarkistusta ja hyväksyntää varten. Lisätietoja Commerce-työnkuluista on kohdassa [Työnkulkujärjestelmän yleiskatsaus](/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system).

## <a name="product-level-pricing-settings"></a>Tuotetason hinnoitteluasetukset

Seuraavat asetukset ottavat käyttöön hinnoittelusäännöt tuotetasolla. Ne ovat organisaation **Tuotemääritys**-sivulla.

### <a name="allow-price-adjust"></a>Salli hinnan oikaisu

Jos **Salli hinnan oikaisu** -parametrin arvoksi on määritetty **Kyllä**, hinnan ohitusta voi käyttää tuotteelle puhelinkeskuskanavan myyntitilauksissa.

### <a name="key-in-price"></a>Näppäile hinta

**Näppäile hinta** -asetus määrittää, onko näppäilty hinta pakollinen, jos tuote lisätään myyntitapahtumaan myyntipisteessä. Se määrittää myös vastaavat hinta-arvon rajoitukset.

### <a name="zero-price-valid"></a>Nollahinta sallittu

**Nollahinta sallittu** -asetus määrittää, voiko tuotteen ennalta määritetty, järjestelmän laskema tai manuaalisesti oikaistu myyntihinta olla 0 (nolla). Määritä parametrin arvoksi **Kyllä**, jos nollahinta on sallittu. Tämä asetus voidaan määrittää myös Commerce-tuotehierarkian luokkatasolla.

### <a name="prevent-all-discounts"></a>Estä kaikki alennukset

Määrittämällä **Estä kaikki alennukset** -parametrin arvoksi **Kyllä** estät kaikkien alennustyyppien (myös manuaalisten alennusten) kohdistamisen tuotteeseen. Tämä asetus voidaan määrittää myös Commerce-tuotehierarkian luokkatasolla.

> [!NOTE]
> Tämä asetus ei rajoita hinnan ohitustoimintoa, koska tämä toiminto määrittää hinnan, jota ei pidetä alennuksena.

### <a name="prevent-manual-discounts"></a>Estä manuaaliset alennukset

Määrittämällä **Estä manuaaliset alennukset** -parametrin arvoksi **Kyllä** estät manuaalisten rivi- ja tapahtuma-alennusten kohdistamisen tuotteeseen. Kaikkia muita alennuksia voidaan silti yhä käyttää. Tämä asetus voidaan määrittää myös Commerce-tuotehierarkian luokkatasolla.

> [!NOTE]
> Tämä asetus ei rajoita hinnan ohitustoimintoa, koska tämä toiminto määrittää hinnan, jota ei pidetä alennuksena.

### <a name="prevent-retail-discounts"></a>Estä vähittäismyynnin alennukset

Jos **Estä vähittäismyynnin alennukset** -parametrin arvoksi on määritetty **Kyllä**, **yksinkertaista** alennusta tai **määrä**-, **raja-arvo**-, **yhdistelmä**- ja **lähetysalennusta** ei voi kohdistaa tuotteeseen. Kaikkia muita alennuksia (myös manuaalisia alennuksia) voidaan silti yhä käyttää.

### <a name="prevent-tender-based-discounts"></a>Estä maksuvälinepohjaiset alennukset

Jos **Estä maksuvälinepohjaiset alennukset** -parametrin arvoksi on määritetty **Kyllä**, **maksuvälineperusteista** alennusta ei voi käyttää tuotteessa. Kaikkia muita alennuksia (myös manuaalisia alennuksia) voidaan silti yhä käyttää.

Jälleenmyyjät jättävät usein joitakin tuotteita, kuten uusia tai suosittuja nimikkeitä, pois nimikeperusteisten alennusten (kuten yksinkertaisten alennusten ja määräalennusten) piiristä. Jos asiakas kuitenkin maksaa alennukseen oikeuttavalla maksuvälineellä, myös maksuvälineperusteisia alennuksia voidaan käyttää. Jälleenmyyjät voivat tämän saavuttaakseen määrittää **Estä kaikki alennukset**- ja **Estä maksuvälinepohjaiset alennukset** -parametrien arvoksi **Ei** ja **Estä vähittäismyynnin alennukset**- ja **Estä manuaaliset alennukset** -parametrien arvoksi **Kyllä**.

## <a name="deprecated-or-removed-settings"></a>Vanhentuneet tai poistetut asetukset

Seuraavat hinnoitteluasetukset on poistettu Dynamics 365 Commercesta tai niiden poistoa sovelluksesta suunnitellaan.

| Asetus | Vanhentumisen tai poiston syy | Vanhentumisen tai poiston syy |
|---------|-----------------------------------|-------------------------------|
| Päällekkäinen alennusten käsittely | Tämä Commercen parametrien asetus määrittää, miten hinnoittelumoduuli hakee ja määrittää parhaan käytettävän alennusyhdistelmän. **Paras alennus** -vaihtoehto käyttää kaikkia mahdollisia alennusyhdistelmiä hinnoittelun laskennan aikana. **Paras suorituskyky** -vaihtoehto käyttää edistynyttä heuristista algoritmia ja raja-arvon luokittelua parhaan alennusyhdistelmän priorisointiin, arviointiin ja määrittämiseen oikea-aikaisesti. **Tasapainotettu laskenta** -vaihtoehto koodikannassa toimii samoin kuin **Paras suorituskyky** -vaihtoehto. Niinpä se on käytännössä kaksinkertainen vaihtoehto. Suorituskuvun parantamiseksi hinnoittelumoduulia on päivitetty niin, että se käyttää vain **Paras suorituskyky** -vaihtoehtoa vakiovaihtoehtona. Siksi tämä asetus ei ole enää käytettävissä. | Vanheni julkaisussa 10.0.21 ja poistetaan lokakuussa 2022. |
| Sallin hinnanoikaisut, jotka nostavat tuotteen hintaa | Tämä asetus määritti, voiko hinnanoikaisutoiminto nostaa tuotteen hintaa. Jos tämä parametri on poistettu käytöstä, organisaatiot käyttävät hinnanoikaisutoimintoa vain tuotteen yksikköhinnan määrittämisessä alemmaksi kuin sen perushinta ja kauppasopimuksen myyntihinta. Tämä asetus vanheni, koska hinnanoikaisutoimintoa on päivitetty niin, että se tukee valmiita kaksisuuntaisia oikaisuja (nosto tai lasku). | Vanheni julkaisussa 10.0.30 ja poistetaan lokakuussa 2023. |
| Ota käyttöön vähittäismyymälän hintaraportti | Tämä asetus määritti, onko **hintaraporttitoiminto** käytettävissä myymälän määrityssivulla. Tämä asetus vanhentui, koska myymälän määrityssivua on päivitetty niin, että **hintaraporttitoiminto** näkyy aina vakiotoimintona. | Vanheni julkaisussa 10.0.31 ja poistetaan lokakuussa 2023. |
| Käytä tämän päivän päivämäärää hintojen laskemiseen | Dynamics 365 Supply Chain Managementin hinnoittelumoduuli tukee hinnoittelun laskemista, joka perustuu pyydettyyn lähetyspäivään tai pyydettyyn vastaanottopäivään yhdessä tämän päivän päivämäärän kanssa. Commercen hinnoittelumoduuli tukee vain hinnoittelun laskentaa, joka perustuu tämän päivän päivämäärään. Jos asiakas käyttää sekä Supply Chain Management- että Commerce-ominaisuuksia, asiakkaiden tulisi määrittää tämän asetuksen arvoksi aina **Kyllä**, jotta kaksi hinnoittelumoduulia voivat toimia yhdessä. Tämä asetus vanheni, koska se ei muuta laskennan toimintaa olennaisesti, vaan oli tarpeeton. | Vanheni julkaisussa 10.0.31 ja poistetaan lokakuussa 2023. |
| Enimmäishinta | Tämä toimintoprofiilissa oleva asetus määrittää, voiko tiettyjen myymälöiden myyntipisteessä myydä vain alle tietyn enimmäishinnan omaavia tuotteita. Tämä asetus vanhentui, koska sitä ei käytetty paljon. | Vanheni julkaisussa 10.0.31 ja poistetaan lokakuussa 2023. |
| Käytä alennuksia yksikköhinnassa | Tämän asetuksen avulla oli tarkoitus määrittää, pyöristetäänkö hinnat ja alennukset yksikköhintatasolla vai myyntirivitasolla hinnoittelun laskennan aikana. Se vanhentui, koska nykyinen koodikanta ei käyttänyt sitä missään. | Vanheni julkaisussa 10.0.31 ja poistetaan lokakuussa 2023. |
| Laske manuaalisesti moninimikealennukset | Tämä asetus määritti, käyttääkö hinnoittelumoduuli viivytettyä hinnanlaskentaa vähittäismyymäläkanavalla. Jos parametrin arvoksi on määritetty **Kyllä**, hinnoittelumoduuli ei laske heti useiden rivien alennuksia (kuten määräalennuksia, alennuksia rajan ylittyessä ja yhdistelmäalennuksia), jos myyntitilaus on luotu myyntipistesovelluksessa tai jos sitä on muokattu siellä. Tämä asetus päätettiin yhdistää Commercen parametrien samanlaisen asetuksen kanssa kaikkikanavaisen hallinnan muodostamiseksi. | Vanheni julkaisussa 10.0.31 ja poistetaan lokakuussa 2023. |

Dynamics 365 Commercen kaikkien poistettujen ja vanhentuneiden ominaisuuksien luettelo on kohdassa [Poistetut tai vanhentuneet Dynamics 365 Commerce -ominaisuudet](get-started/removed-deprecated-features-commerce.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
