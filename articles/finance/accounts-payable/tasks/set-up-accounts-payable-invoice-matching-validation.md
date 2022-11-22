---
title: Ostoreskontran laskujen täsmäytyksen vahvistuksen asetukset
description: Tässä artikkelissa on tietoja ostoreskontran laskujen täsmäytyksen vahvistamisen määrittämisestä.
author: abruer
ms.date: 02/14/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c93ba4a13dee32427f33fe9f33fda5d783501a7
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775323"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Ostoreskontran laskujen täsmäytyksen vahvistamisen määrittäminen

[!include [banner](../../includes/banner.md)]

Varmista ennen aloittamista, että laskun täsmäytyksen konfigurointiavain on valittuna. Jos oma yrityksesi seuraa kuluja, kuten rahtia, veloituksien avulla, varmista että kulujen konfigurointiavain on valittuna. Ostoreskontran laskujen täsmäytys on prosessi, jossa täsmäytetään toimittajan laskun, ostotilauksen ja tuotteen vastaanoton tiedot. Näissä asiakirjoissa olevia eroja kutsutaan ristiriidoiksi. Täsmäytysristiriitoja verrataan määritettyihin toleransseihin. Jos täsmäytysristiriita ylittää toleranssin prosentin tai summan, täsmäytyksen varianssin kuvakkeet näkyvät **Toimittajan lasku**-sivulla ja **Laskun täsmäytyksen tiedot** -sivulla.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Käytettävän laskun täsmäytyksen vahvistamisen määrittäminen
Täsmäyksen vahvistamistyyppejä on neljä. 

- **Rivitason täsmäytys** – Yleisin täsmäytystapa on rivitäsmäytys. Rivitason täsmäytys voi olla kaksisuuntainen tai kolmisuuntainen. Rivitason oletustäsmäytys voidaan määrittää yritykselle **Ostoreskontran parametrit** -sivulla. Kaksisuuntaisessa täsmäytyksessä laskun yksikköhintaa verratun ostotilauksen yksikköhintaan. Kolmisuuntaisessa täsmäytyksessä verrataan lisäksi laskun määrä täsmäytetyn tuotteen vastaanoton määrään.
- **Laskusummien täsmäytys** – Laskun kokonaissummat täsmäytetään ostotilauksen kokonaissummiin. Tämä laskun täsmäytystyyppi sisältää vähiten tietoja, joten voit määrittää tällä asetuksella ohjausobjektit, jotka minimoivat henkilökunnalta laskujen täsmäytystietojen tarkistamiseen kuluvan ajan. Verrattavia summia on kuusi: välisumma, kokonaisalennus, kulut, arvonlisävero, pyöristys ja laskun summa. Järjestelmä tarkistaa, poikkeaako jokin näistä laskun arvoista odotetuista summista hyväksyttyä varianssia enemmän.
- **Kulujen täsmäytys** – laskun kulutiedot (summat) täsmäytetään ostotilauksen kulutietoihin (summiin).
- **Rivinimikkeen täsmäytyksen kokonaishinnat** – Tämä täsmäytystyyppi on kätevä yrityksille, jotka saavat useita laskuja ostotilauksen yhdelle riville. Jos kullekin ostotilausriville saadaan yleensä vain yksi lasku, tällaista täsmäytystä ei tarvita. Tämä täsmäytys edellyttää kaksi- tai kolmisuuntaisen täsmäytyksen käyttöönottoa. Se toimii myös toleranssiprosentteihin ja -summiin perustuvana ei saa ylittää -nettosumman tarkistuksena. Tässä täsmäytyksessä verrataan laskun kunkin rivin nettosummien sekä kaikkien odottavien ja aiemmin kirjattujen laskurivien hintatietoja vastaavan ostotilausrivin nettosummaan. Nettosumma määritetään seuraavalla kaavalla: (yksikköhinta * rivimäärä) + rivin kulut vähennettynä rivialennuksilla. Kun kokonaishintoja täsmäytetään prosenttiosuuden mukaan, arvoja vertaillaan tapahtumavaluutan avulla. Kun kokonaishintoja täsmäytetään summan mukaan, järjestelmä vertaa arvoja kirjanpitovaluutan avulla.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>Laskujen täsmäytyksen vahvistuksen mahdollistavien parametrien määrittäminen
1. Valitse **Ostoreskontra > Asetukset > Ostoreskontran parametrit**.
2. Valitse **Laskun oikeellisuustarkistus** -välilehti.
3. Valitse **Ota käyttöön laskujen täsmäytyksen vahvistus** -valintaruutu tai poista sen valinta.
    * Määritä, onko hyväksyntä pakollinen, ennen kuin laskun vastaavuuden ristiriitoja sisältävä lasku voidaan kirjata. Jos arvoksi on määritetty **Salli varoituksella**, kuvallinen osoitin näyttää, kun laskun täsmäytyksen ristiriita ylittää toleranssin. Voit kuitenkin kirjata laskun. Voit käyttää työnkulkuja yhdessä laskun täsmäytyksen tarkistuksen kanssa, kun varmistat, että **Kirjaa lasku, jossa on ristiriitoja** -kentän arvoksi on määritetty **Salli varoituksella**. Tällöin hyväksyntää ei tehdä useita kertoja.  
    * Valitse **Päivitä laskun otsikon täsmäytyksen tila automaattisesti** -kentässä, suoritetaanko täsmäytys automaattisesti laskun tietojen syötön aikana. Suositeltu asetus on **Kyllä**, jos tietojen kirjaamisessa ei ole ongelmia. Automaattisten päivityksen poistaminen käytöstä voi parantaa järjestelmän suorituskykyä, koska laskujen täsmäytyksen tarkistus ohitetaan tietojen syötön aikana. Jos tämän kohdan arvoksi on määritetty **Ei**, tietojen syöttäjän on päivitettävä laskun täsmäytyksen tila manuaalisesti, jotta laskun täsmäytyksen tarkistustulokset näkyvät.  
4. Määritä **Laskusummien täsmäytys**.
5. Valitse **Täsmäytä laskusummat** -valintaruutu tai poista sen valinta, jos haluat täsmäyttää toteutuneet laskusummat odotettujen summien kanssa.
    * Määritä, näkyykö kuvake, jos ristiriita laskua kohdistettaessa ylittää nettoyksikköhinnan toleranssin. Voit valita, että kuvake voidaan näyttää, kun positiivinen ristiriita ylittää toleranssin, tai kun joko positiivinen tai negatiivinen ristiriita ylittää toleranssin.  
    * Toleranssi on esimerkiksi 5 prosenttia ja ostotilauksen laskun kokonaissumma on 100,00. Tämän vuoksi hintavastaavuuden kuvake näytetään, jos laskun kokonaissumma ylittää 105,00. Jos valitset **Onko suurempi tai pienempi kuin toleranssi** -vaihtoehdon, kuvake näkyy myös, jos laskun summa on pienempi kuin 95,00.  
6. Anna **Laskusummien toleranssiprosentti** -kenttään hyväksyttävä prosentin varianssi. Tämä arvo on yrityksen oletusarvo. Tämä arvo voidaan ohittaa tiettyjen toimittajien osalta **Laskusummien toleranssit** -sivulla. Lisätietoja tietyn toimittajan laskusummien toleranssiprosentin ohittamisesta on jäljempänä tämän artikkelin [Toimittajien laskusummien täsmäytystoleranssien määrittäminen](set-up-accounts-payable-invoice-matching-validation.md#set-up-invoice-totals-matching-tolerance-for-vendors) -osassa.
7. Määritä **Hinnan ja määrän täsmäytys**.
8. Valitse **Rivien vastaavuuskäytäntö** -kentässä arvo, jota käytät oletusarvon mukaisena käytäntönä yritykselle, jonka kanssa työskentelet. **Ei pakollinen** tarkoittaa, että tarkistus yksittäisistä laskurivien hinnoista ostotilauksen hinnoiksi tai laskujen määristä pakkausluettelon määriksi ei ole pakollinen. **Kaksisuuntainen vastaavuus** tarkoittaa, että laskurivien tarkistus on pakollinen, mutta vain ostotilaus ja toimittajan laskuasiakirjat ovat mukana tarkistuksessa. Tuotteen vastaanottoa ei oteta huomioon täsmäytysten tarkistuksissa. **Kolmisuuntainen vastaavuus** tarkoittaa, että laskun nettoyksikköhintaa verrataan ostotilauksen nettoyksikköhintaan ja vastaavaa tuotteen vastaanoton määrää verrataan laskun määrään.
9. Voit sallia eritasoisen täsmäytyksen käytettäväksi nimikkeelle, toimittajalle, toimittajan ja nimikkeen yhdistelmällä tai ostotilausriville valitsemalla arvon **Salli vastaavuuskäytännön ohitus** -kentässä. Yritysrivin yhteensopivuuskäytäntö voidaan ohittaa tietyn toimittajan, nimikkeen tai toimittajan ja nimikkeen yhdistelmän osalta **Vastaavuuskäytäntö**-sivulla.
    * Jos käytössä on rivin **kaksi**- tai **kolmisuuntainen** vastaavuuskäytäntö, voit määrittää **Nimikkeen hintatoleranssi** -sivulla yritykselle, nimikkeille ja toimittajille hintatoleranssin prosenttiosuudet. Yrityksen oletushintatoleranssiksi määritetään yksi- ja kaksisuuntaisessa täsmäytyksessä nolla. Kun toimittajan laskuja verrataan ostotilaustietoihin, järjestelmä etsii sovellettavaa hintatoleranssin prosenttia.   
10. Voit täsmäyttää laskujen rivinimikkeiden kokonaissummat valitsemalla arvon **Täsmäytä kokonaishinnat** -kentässä. Tällainen täsmäytys on hyödyllistä silloin, kun toimittaja lähettää useita samaa ostotilausriviä koskevia laskuja. Voit verrata laskun kunkin rivin nettosummien ja kaikkien odottavien ja aiemmin kirjattujen laskurivien hintatietoja vastaavan ostotilausrivin nettosummaan. Vaihtoehtoja ovat **Ei mitään**, **Prosentti**, **Summa** tai **Prosentti ja summa**.
11. Anna **Ostohinnan kokonaistoleranssiprosentti** -kentässä hyväksyttävä varianssiprosentti. Tämä kenttä on käytettävissä, jos **Täsmäytä kokonaishinnat** -arvoksi on määritetty **Prosentti** tai **Prosentti ja summa**.
12. Anna **Ostohinnan kokonaistoleranssi** -kentän summa kirjanpitovaluuttana. Tämä kenttä on käytettävissä, jos **Täsmäytä kokonaishinnat** -arvoksi on määritetty **Summa** tai **Prosentti ja summa**.
13. Valitse **Näytä kokonaishinnan täsmäytyskuvake** -kentässä milloin kuvake näkyy, jos ristiriita laskua kohdistettaessa ylittää nettoyksikköhinnan toleranssin. Kuvake voidaan näyttää, kun positiivinen ristiriita ylittää toleranssin, tai kun joko positiivinen tai negatiivinen ristiriita ylittää toleranssin.
Toleranssi on esimerkiksi 5 prosenttia ja ostotilauksen rivin kokonaishinta on 10,00. Tämän vuoksi hintavastaavuuden kuvake näytetään, jos laskurivin kokonaishinta ylittää 10,50. Jos valitset **Onko suurempi tai pienempi kuin toleranssi**, kuvake näkyy myös, jos laskurivin kokonaishinta on pienempi kuin 9,50.
13. Määritä **Kulujen täsmäytys**.
14. Vertaa todellisia veloituksia odotettuihin kuluihin ostotilauksen tietoihin perustuen valitsemalla **Täsmäytä kulut** -valintaruutu.

## <a name="set-up-unit-price-tolerance-percentages"></a>Yksikköhintatoleranssin prosenttiosuuksien määrittäminen
Määritä sallitut hintatoleranssiprosentit valitsemalla **Ostoreskontra > Asetukset > Laskun täsmäytyksen asetukset > Hintatoleranssit**. Jos käytössä on rivin **kaksi**- tai **kolmisuuntainen** vastaavuuskäytäntö, voit määrittää yritykselle, nimikkeille ja toimittajille hinnan toleranssiprosentin. Kun toimittajan laskuja verrataan ostotilaustietoihin, järjestelmä etsii sovellettavaa hintatoleranssin prosenttia. Oletushakujärjestys on seuraava:
* Taulu/taulu
* Taulu/ryhmä
* Taulu/kaikki
* Ryhmä/taulu
* Ryhmä/ryhmä
* Ryhmä/kaikki
* Kaikki/taulu
* Kaikki/ryhmä
* Kaikki/kaikki

Yrityksen oletushintatoleranssi on nolla prosenttia, ja tätä hintatoleranssia sovelletaan kaikkiin nimikkeisiin ja tileihin (Kaikki, Kaikki). Et voi poistaa oletusarvoista yrityksen hintatoleranssitietuetta.

Oletusarvon mukaan negatiiviset hintaerot sallitaan. Et voi määrittää negatiivista hintatoleranssin prosenttiosuutta. Voit seurata hinnan negatiivisia toleranssiprosentteja valitsemalla **Onko suurempi tai pienempi kuin toleranssi** -vaihtoehdon **Näytä kulujen täsmäytyskuvake** -kentässä **Ostoreskontran parametrit** -sivulla. Kirjaa sitten hinnan toleranssiprosentit **Hintatoleranssit**-sivulla.

## <a name="set-up-matching-policy-override"></a>Vastaavuuskäytännön ohituksen määrittäminen

Määritä **Ostotilaus**-sivun **Täsmäytyskäytäntö**-kentän oletuskirjaus valitsemalla **Ostoreskontra > Asetukset > Laskun täsmäytyksen asetukset > Täsmäytyskäytäntö**. Tämä on valinnainen asetus. Voit määrittää tällä sivulla nimikkeiden, toimittajien tai nimike- ja toimittajayhdistelmien kaksi- tai kolmesuuntaisen täsmäytyksen. Voit määrittää näillä kirjauksilla täsmäytyskäytännöt, jotka ovat yksityiskohtaisemmat kuin **Ostoreskontran parametrit** -sivulla määritetty yrityksen täsmäytyskäytäntö. Yrityksen oletusarvoista rivitäsmäytyskäytäntöä käytetään kaikissa nimikkeissä ja toimittajissa lukuun ottamatta niitä, jolle määritettiin tällä sivulla erilainen rivin täsmäytyskäytäntö.

Valitse tällä sivulla **Vastaavuuskäytännön taso**. Valitse vastaavuuskäytäntöhierarkiassa taso, jolle rivien vastaavuuskäytäntö on tarkoitettu.

- **Nimike ja toimittaja** – määrittää tietyiltä toimittajilta ostettujen tiettyjen nimikkeiden täsmäytyskäytännön.
- **Nimike** – määrittää joltakin toimittajalta ostetun tietyn nimikkeen täsmäytyskäytännön lukuun ottamatta niitä nimikkeitä, jotka on määritetty nimike- ja toimittajatasolla.
- **Toimittaja** – määrittää tietyiltä toimittajilta ostettujen kaikkien nimikkeiden täsmäytyskäytännön lukuun ottamatta niitä nimikkeitä, jotka on määritetty nimike- ja toimittaja- sekä nimiketasoilla.
  
Käytettävä täsmäytyskäytännöt määritetään seuraavan hierarkian avulla:
  *  Nimike ja toimittaja
  *  Kohde
  *  Toimittaja
  *  Oikeushenkilö
  
## <a name="set-up-invoice-totals-matching-tolerance-for-vendors"></a>Toimittajien laskujen kokonaissummin täsmäystoleranssien määrittäminen

Määritä laskujen kokonaissummien täsmäytyksen toimittajakohtaiset toleranssit valitsemalla **Ostoreskontra > Asetukset > Laskun täsmäytyksen asetukset > Laskusummien toleranssit**. Täsmäytyksen laskenta käyttää toimittajan laskussa tilaustiliksi määritetyn toimittajatilin laskusumman toleranssiprosenttia. Jos toimittajatilillä ei ole määritettyä laskusummien toleranssiprosenttia, käytetään **Ostoreskontran parametrit** -sivulla määritettyä laskusummien toleranssiprosenttia.

1. Voit määrittää yksittäisten toimittajien oletustoleranssin ohittavat toleranssit valitsemalla **Toimittajatili**.
2. Kirjoita tälle toimittajalle hyväksymäsi vaihteluprosentti.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
