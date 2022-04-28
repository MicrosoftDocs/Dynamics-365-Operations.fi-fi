---
title: Tuki ja uusimiset
description: Tässä aiheessa kerrotaan, miten myyntitilausten tuki- ja prosessi määritetään ja kuinka sitä käytetään myyntitilausten laskutusaikataulun luomiseen.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d59eee6e858c4f0051ec103adc4e1e99e79feec9
ms.sourcegitcommit: 4d7bc52e6cdf6afce3793893ba2aa07176302314
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/11/2022
ms.locfileid: "8560478"
---
# <a name="support-and-renewals"></a>Tuki ja uusimiset 

Tässä ohjeaiheessa kerrotaan, kuinka tuki- tai uusimistuotteet syötetään, kun syötät myyntitilauksia. Näiden nimikkeiden avulla lasketaan alkuperäisen tukisopimuksen kulusumma ja/tai laskutusaikataulun luomisessa käytettävä laskutusaikataulu ylläpitosopimuksen laskutuksen yhteydessä. Yritys esimerkiksi myy palvelimen asiakkaalle ja tarjoaa tietojen varmuuskopiosopimuksen ensimmäiseksi vuodeksi sekä mahdollisuuden uusia tilaussopimuksen joka vuosi. *Tukinimike* on tilaus ensimmäiselle vuodelle ja *uusimisnimike* on uusiminen jokaiselle peräkkäiselle vuodelle.

Voit kirjoittaa tukisopimuksen, uusimisen tai molempien tiedot. Kun lisäät tukisopimuksen tiedot, myyntitilaukseen lisätään vain tukinimike. Kun kirjoitat sopimustiedot, nimikkeelle luodaan laskutusaikataulu.

## <a name="support-and-renewal-setup"></a>Tuen ja uusimisen määritys

**Tuki- ja rahoitustasot** -sivulla voit määrittää eri tukitasot tuki- ja apunimikkeille. Tuki tai uusiminen voi olla prosenttiosuus alkuperäisen nimikkeen summasta, tai se voi olla vakiosumma.

Voit valita oletustukitasot **Toistuvan sopimuksen laskutusparametrit** -sivulla.

Yritys voi esimerkiksi tarjota seuraavia tuki- ja määrätasoja.

| Tukitaso | Tukiprosentti | Uusimisprosentti |
|---|---|---|
| Ei rajoitettu | 40 % | 30 % |
| Kulta | 25 % | 18 % |
| Hopea | 20 % | 14 % |
| Pronssi | 15 % | 10 % |

Voit luoda tuki- tai rahoitustasot, noudattamalla seuraavia vaiheita.

1. Valitse **Tuki ja rahoitustasot** -sivulla **Uusi**.
2. Anna **Tukitaso**-kentässä yksilöivä nimi.
3. Syötä **Kuvaus**-kenttään kuvaus.
4. Valitse **Tuen laskentatapa** -kentästä tuen laskentatapa. Jos valitset **Prosentti**-kentästä prosenttiosuuden, määritä tukiprosentti **Tukiprosentti**-kenttään.
5. Valitse **Uudistamisen laskentatapa** -kentästä uudistamisen laskentatapa. Jos valitset **Prosentti**-kentästä prosenttiosuuden, määritä uudistusprosentti **Uudistusprosentti**-kenttään.
6. Valitse **Tallenna**.

### <a name="fields"></a>Kentät

**Tuki- ja rahoitustasot** -sivu sisältää seuraavat kentät.

| Kenttä | Kuvaus |
|---|---|
| Tukitaso | Tuki- tai rahoitustason yksilöivä tunnus (esimerkiksi **Kulta** tai **Hopea**). |
| Kuvaus | Yksityiskohtainen kuvaus tuki- tai apupalvelutasosta. |
| Tuen laskentamenetelmä | Valitse tason, **prosentin** tai **vakiosumman**, tuen laskentamenetelmä. |
| Tukiprosentti | Jos olet valinnut tuen laskentatavaksi **prosenttiosuuden**, määritä prosenttiosuus, jota käytetään tukinimikkeen hinnan laskennassa. Jos valitsit laskentatavaksi **Vakiosumman**, summa määritetään tapahtuman luomisen yhteydessä. |
| Uusimisen laskentamenetelmä | Valitse tason, **prosentin** tai **vakiosumman**, uudistuksen laskentamenetelmä. |
| Uusimisprosentti | Jos olet valinnut uudistuksen laskentatavaksi **prosenttiosuuden**, määritä prosenttiosuus, jota käytetään uudistusnimikkeen hinnan laskennassa. Jos valitsit laskentatavaksi **Vakiosumman**, summa määritetään tapahtuman luomisen yhteydessä. |

## <a name="support-and-renewal-process"></a>Tuki- ja uusimisprosessi

Tuki- ja apupalvelutoiminnot voivat käyttää eri tukitasoja nimikkeisiin ja päivittää allekirjoitusten laskutusta koskevat päivitystiedot.

Ennen kuin käytät tuki- ja uudistustoimintoa, seuraavat tehtävät on suoritettava.

1. Luo **Tuki- ja uudistustaso** -sivulla ainakin yksi tuki- tai alitaso.
2. **Nimikkeen asetukset** -sivulla liittää nimikkeen, jolla on tuki- ja uudistusnimikkeitä. Tämä tehtävä on pakollinen vain, jos haluat määrittää oletusarvot tukinimikkeille ja/tai apunimikkeille.
3. Määritä **Toistuvat sopimuksen laskutusparametrit** -sivulla uusien laskutusaikataulujen oletustukeen ja laskutusaikatauluihin liittyvät laskutusasetukset.

Noudata seuraavia ohjeita, kun haluat käyttää nimikkeille eri tukitasoja ja päivittää yhteystietoja.

1. Valitse **Kaikki myyntitilaukset** -sivulla myyntitilaus.
2. Valitse **Myyntitilausrivit**-pikavälilehdessä Lisää nimike.
3. Valitse **Lasku**-välilehdestä **Tuki ja uudistus \> Lisää tuki ja uudistus**.
4. **Tuki- ja uusimisprosessi** -sivun otsikko-osio päivitetään **Toistuvan sopimuksen laskutusparametrit** -sivun asetuksilla. Nämä arvot koskevat kaikkia tuki- ja apunimikkeitä. (Esimerkiksi jos laskutusväliksi on määritetty **Vuosittain** kaikilla luoduilla myyntiriveillä, jotka on luotu nimikkeellä on vuosittainen toistumistiheys.) Voit liittää myyntitilauksen aiemmin luotuun laskutusaikatauluun valitsemalla arvon **Laskutusaikataulun numero** -kentästä.
5. Jos haluat muuttaa tuki- tai ohitusaikapäivämäärää, määritä **Aloituspäivämäärän ohitus** -asetuksen arvoksi **Kyllä**.
6. Voit lisätä tukinimikkeen tai muokata sitä valitsemalla **Tuki**-valintaruudun ja kirjoittamalla sitten tukinimikkeen **Tukinimike**-kenttään. Nimike lisätään myyntitilaukseen.
7. Voit lisätä uudistusnimikkeen tai muokata sitä valitsemalla **Uudistus**-valintaruudun ja kirjoittamalla sitten uudistusnimikkeen **Uudistusnimike**-kenttään. Kun myyntitilaus laskutetaan, luodaan nimikkeen laskutusaikataulu.
8. Valitse **OK**.
9. Valitse **Luo**-välilehdessä **Lasku**. Kun myyntitilaus kirjataan, luodaan laskutusaikataulu. Viestin tietoihin tulee ilmoitus, joka sisältää laskutusaikataulun tiedot.
10. Valitse **Kaikki/Aktiiviset laskutusaikataulut** -luettelosivulta laskutusaikataulun numero, niin voit tarkastella laskutusaikataulun tietoja **Laskutusaikataulut**-sivulla.
11. Tarkista luodut rivit valitsemalla **Laskutusaikataulun rivit** -pikavälilehdillä **Tuki ja uudistus**.

> [!NOTE]
> Jos muutat laskutusaikataulun rivin julkaisupäivän, voit muokata **Laskutusaikataulut**-sivulla olevan rivin **aloituspäivämäärän** arvoa. Kun avaat rivin **Näytä laskutustiedot** -sivun, **Laskutuksen aloituspäivämäärä** -kenttään päivitetään uusi päivämäärä. **Laskutuksen päättymispäivän** arvo lasketaan uudelleen laskutustiheyden mukaan. Rekisteröinnin alkamispäivämäärä voidaan päivittää vain, jos laskutusaikataulun ensimmäistä laskua ei ole luotu ja kirjattu. Ensimmäisen laskun luomisen ja kirjaamisen jälkeen aloituspäivämäärää ei voi muokata.

Vain myyntitilauksen tuki- ja apuprosessi on saatavana. Kun lisäät myyntitilaukseen tuki- ja uudistusnimikkeitä, voit luoda uuden laskutusaikataulun tai lisätä sen aiemmin luotuun laskutusaikatauluun.

## <a name="support-and-renewal-audit"></a>Tuen ja uusimisen tarkistus

**Tuki- ja uusintatarkastus** -sivulla voit tarkastella laskutusaikataulurivien tietoja, jotka on luotu myyntitilauksen uusintanimikkeestä. Tämä valinta on käytettävissä, kun laskutusaikataulun rivinimike on uudistusnimike.

Noudata seuraavia ohjeita, kun haluat muokata laskutusaikataulurivin tuki- ja uudistustietoja.

1. Valitse **Kaikki laskutusaikataulut** -sivulla laskutusaikataulun numero.
2. Valitse **Laskutusaikataulun rivit** -osassa poistettava rivi ja valitse sitten **Tuki ja uudistus**.
3. Tarkista kaikki tuki- tai uudistusnimikkeen tiedot.
4. Tee tarvittavat muutokset tukitasoon tai prosenttiosuuteen tai summaan ja kirjoita sitten arvo **Muutoksen syy** -kenttään.
5. Valitse **Prosessi**.

### <a name="fields"></a>Kentät

**Tuki- ja rahoitustarkastus** -sivu sisältää seuraavat kentät.

| Kenttä | Kuvaus |
|-------|-------------|
| Nimiketunnus | Laskutusaikataulurivin nimikenumero. |
| Tuotteen nimi | Tuotteen nimi. |
| Tuen palvelupaketin taso | Tarkastele tai muuta uusintakohteen tukitasoa. |
| Uusimisprosentti | Kirjoita prosenttiosuus, jota käytetään, kun yksikköhinta lasketaan laskutusaikataulussa nimikkeelle, joka on laskutusaikataulussa valmistunut. |
| Uusimissumma | Kirjoita uudistusmäärä, jota käytetään, kun yksikköhinta lasketaan laskutusaikataulussa nimikkeelle, joka on laskutusaikataulussa valmistunut. |
| Muutoksen syy | Lisää syysi tukitietojen ja uudistustietojen muuttamiselle. Syy on kirjoitettava, kun muutat **Uudistuksen prosenttilukua**, **uudistuksen summaa** tai **tukisuunnitelman tason** arvoa. |
| Alkuperäinen myyntinimike | Alkuperäinen myyntinimikkeen numero myyntitilauksesta. |
| Alkuperäinen nettosumma | Alkuperäinen nimikkeen nettosumma. |
| Alkuperäinen tukitaso | Alkuperäinen nimikkeen tukitaso. |
| Alkuperäinen uusimisprosentti | Tuotteen alkuperäinen uudistamisprosentti. |
| Alkuperäinen uusimissumma | Tuotteen alkuperäinen uudistamismäärä. |
| **Ruudukko** | |
| Alkuperäinen tukitaso | Edellinen tukitaso. |
| Alkuperäinen uusimisprosentti | Edellinen uudistamisprosentti. |
| Alkuperäinen uusimissumma | Edellinen uudistamismäärä. |
| Muokannut | Muutoksen tehneen käyttäjän käyttäjänimi. |
| Muokkauksen päivämäärä ja aika | Muutoksen päivämäärä. |
| Syy | Muutoksen syy. |
