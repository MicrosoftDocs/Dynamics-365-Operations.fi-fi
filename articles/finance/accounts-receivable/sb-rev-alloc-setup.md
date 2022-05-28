---
title: Määritä useiden elementtien tuoton kohdistus
description: Tässä aiheessa kuvataan, kuinka useiden elementtien tuoton kohdistuksen parametrit määritetään tilauslaskutuksen yhteydessä.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: bb5b220dd941cbb9f1fda5d0eb821a86a9135309
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685796"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Määritä useiden elementtien tuoton kohdistus

Useiden elementtien tuoton kohdistuksen avulla voit määrittää erilaisia malleja, joita käytetään tuoton laskemiseen ja kohdistamiseen useista nimikkeistä. Tämä ominaisuus auttaa noudattamaan kirjanpidon standardien kirjaamisen ohjeaihetta 606 (ASC 606) ja/tai kansainvälisen tilinpäätösraportoinnin standardia 15 (IFRS 15).

## <a name="multiple-element-revenue-allocation-parameters"></a>Useiden elementtien tuoton kohdistusparametrit

**Usean elementin tuoton kohdistusparametrit** -sivulla voit määrittää useiden elementtien tuoton kohdistuksen parametrit.

### <a name="standalone-selling-price-origin"></a>Erillismyyntihinnan alkuperä

**Erillisen myyntihinnan alkuperä** -kenttä määrittää, mistä erillinen myyntihinta on peräisin. Voit päivittää **nimikkeen erillinen myyntihinta** -sivun ja tapahtuman arvon. Valittavissa ovat seuraavat vaihtoehdot.

| Vaihtoehto | Kuvaus |
|--------|-------------|
| Määrä | Erillinen myyntihinta on summa, jonka määrität olevan suurempi kuin 0 (nolla). Summa muunnetaan toimintojen ja alkuperävaluuttojen välillä tarpeen mukaan. |
| Perusmyyntihinta | Erillinen myyntihinta vastaa nimikkeen perusmyyntihintaa. |
| Laskun hinta | Erillinen myyntihinta vastaa nimikkeen laskutushintaa. |
| Prosenttia nimikkeestä | Erillinen myyntihinta määritetään prosenttiarvona, ja se lasketaan nimikkeen hinnan mukaan. Jos valitset tämän vaihtoehdon, määritä oletusprosenttimäärä. |
| Kohdista jäännössumma | <p>Erillisen myyntihinnan alkuperä lasketaan *päänimikkeen sopimuksen kokonaisarvona* – *Alinimikkeiden erillinen kokonaismyyntihinta*:</p><ul><li>*Päänimikkeen sopimuksen kokonaisarvo* on nettosumma tai laskutettu summa.</li><li>*Alinimikkeiden erillinen myyntihinta* on kaikkien alinimikkeiden laajennettu tai itsenäinen myyntihinta lukuun ottamatta alinimikettä, joka käyttää tätä itsenäistä myyntihinnan alkuperää.</li></ul><p>Jos laskettu summa on negatiivinen arvo, summaksi määritetään 0 (nolla).</p><p>**Huomautus:** Tämä vaihtoehto voidaan valita vain yhdelle alinimikkeelle tuottojen jakamisen yhteydessä.</p> |
| Ei mikään | Erillisen myyntihinnan alkuperä perustuu alinimikkeisiin. Tämä asetus koskee nimikkeitä, jotka on määritetty tuottojen jakomallin päänimikkeiksi. Jos **Tuottojen jako** -valintaruutu on valittuna, tämä vaihtoehto on automaattisesti valittuna eikä asetusta voi muuttaa. |
| Prosenttia päälaskun hinnasta | Erillisen myyntihinnan alkuperä on prosenttiosuus päänimikkeen laskun hinnasta. Voit vaihtaa oletusarvon. Tämä valinta on käytettävissä vain tuottojakomallin alinimikkeiden osalta. |
| Prosenttia päälaskun vakiohinnasta | Erillisen myyntihinnan alkuperä on prosenttiosuus päänimikkeen vakiohinnasta. Voit vaihtaa oletusarvon. Tämä valinta on käytettävissä vain tuottojakomallin alinimikkeiden osalta. Se on alinimikkeiden oletusvaihtoehto. Kun alituotteen vaihtoehto muutetaan arvosta **prosentti ylätason vakiohinnasta** **prosenttiin ylätason laskun hinnasta** tai **prosenttiosuudesta ylätason laskun hinnasta** arvoon **prosentti ylätason laskun hinnasta vakiohinta**, myös lasketut arvot päivitetään. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Tuoton kohdistuksen pyöristyserojen tili

**Tili tulojen kohdentamisen pyöristyseroihin** -kenttä määrittää tilin, jota käytetään mahdollisten sopimustulojen summan pyöristysoikaisujen kirjaamiseen. Se on käytettävissä, kun toistuvaa laskutusta käytetään.

## <a name="item-standalone-selling-price"></a>Nimikkeen erillismyyntihinta

**Nimikkeen erillinen myyntihinta** -sivulla voit määrittää nimikkeen alkuperän ja erillisen myyntihinnan. Tällä sivulla määritettyjä arvoja käytetään **tulojen kohdistus** -sivun oletusarvoina usean elementin tuoton kohdistuksissa ja toistuvan sopimuksen laskuttamisen yhteydessä.

### <a name="specify-item-standalone-selling-price"></a>Määritä nimikkeen erillismyyntihinta

Voit määrittää nimikkeelle erillisen hinnan noudattamalla seuraavia ohjeita.

1. Valitse erillisen myyntihinnan alkuperä **Tuotteen erillinen myyntihinta** -sivulla **Erillisen myyntihinnan alkuperä** -kentässä.
2. Noudata yhtä näistä vaiheita sen arvon mukaan, jonka valitsit **Itsenäinen myyntihinnan alkuperä** -kentässä:

    * Jos valitsit **nimikkeen prosentin**, määritä prosentti **Prosentti**-kenttään.
    * Jos valitsit **Summa**-kentästä summan, määritä summa **Erillisen myyntihinnan** kentässä.

2. Valitse jokaiselle listalle lisättävälle kohteelle **Lisää**.
3. Valitse **Nimikekoodi**-kentässä nimikkeen koodi. Valitse **Nimikesuhde**-kentässä nimikkeen suhde. Niiden nimikkeiden osalta, joissa **tuottojen jako** -valintaruutu ei ole valittuna, nimikekoodin ja nimikesuhteen valitun yhdistelmän on oltava yksilöivä.
4. Muuta **erillisen myyntihinnan alkuperän**, **erillisen myyntihinnan** tai **prosentti**-kentän oletusarvoa tarpeen mukaan.
5. Valitse jokaiselle listalle lisättävälle päänimikkeelle **Lisää**.
6. Valitse **Nimikekoodi**-kentässä nimikkeen koodi. Valitse **Nimikesuhde**-kentässä nimikkeen suhde.
7. Valitse **Tuottojen jako** -valintaruutu.
8. Valitse **Nimikesuhde**-kentässä nimikkeen suhde. Luetteloon päivitetään päänimike ja kaikki alinimikkeet.
9. Muuta alinimikkeen oletusarvoa **Erillinen myyntihinnan alkuperä**, **Prosentti päähinnasta**, **Prosentti päälaskuhinnasta** tai **Määritä jäännössumma** -kenttää tarpeen mukaan.
10. Voit lisätä useita nimikkeitä kerralla valitsemalla **Lisää nimikkeitä**.
11. Päivitä kysely valitaksesi nimikkeiden valikoiman, jotka haluat lisätä.
12. Valitse **OK**, tarkista lisää luetteloon lisäämäsi nimikkeet ja valitse **OK**.

### <a name="fields"></a>Kentät

**Nimikkeen erillinen myyntihinta** -sivu sisältää seuraavat kentät.

| Kenttä | Kuvaus |
|-------|-------------|
| Erillismyyntihinnan alkuperä | <p>Valitse erillismyyntihinnan alkuperä:</p><ul><li>**Summa** – Erillinen myyntihinta on summa, jonka määrität olevan suurempi kuin 0 (nolla). Summa muunnetaan toimintojen ja alkuperävaluuttojen välillä tarpeen mukaan.</li><li>**Perusmyyntihinta** – Erillinen myyntihinta vastaa nimikkeen perusmyyntihintaa.</li><li>**Laskutushinta** – Erillinen myyntihinta vastaa nimikkeen laskutushintaa.</li><li>**Nimikkeen prosenttiarvo** – Erillinen myyntihinta määritetään prosenttiarvona, ja se lasketaan nimikkeen hinnan mukaan. Jos valitset tämän vaihtoehdon, määritä oletusprosenttimäärä.</li></ul>**Määritä jäännösmäärä** – Itsenäisen myyntihinnan alkuperä lasketaan seuraavasti: *Päätuotteen sopimusarvo yhteensä* – *Alinimikkeiden erillinen myyntihinta yhteensä*:</p><ul><li>*Päänimikkeen sopimuksen kokonaisarvo* on nettosumma tai laskutettu summa.</li><li>*Alinimikkeiden erillinen myyntihinta* on kaikkien alinimikkeiden laajennettu tai itsenäinen myyntihinta lukuun ottamatta alinimikettä, joka käyttää tätä itsenäistä myyntihinnan alkuperää.</li></ul><p>Jos laskettu summa on negatiivinen arvo, summaksi määritetään 0 (nolla).</p><p>**Huomautus:** Tämä vaihtoehto voidaan valita vain yhdelle alinimikkeelle tuottojen jakamisen yhteydessä.</p></li><li>**Ei mitään** – Erillisen myyntihinnan alkuperä perustuu alinimikkeisiin. Tämä asetus koskee nimikkeitä, jotka on määritetty tuottojen jakomallin päänimikkeiksi. Jos **Tuottojen jako** -valintaruutu on valittuna, tämä vaihtoehto on automaattisesti valittuna eikä asetusta voi muuttaa.</li><li>**Päänimikkeen laskun prosenttiosuus** – Erillisen myyntihinnan alkuperä on prosenttiosuus päänimikkeen laskun hinnasta. Voit vaihtaa oletusarvon. Tämä valinta on käytettävissä vain tuottojakomallin alinimikkeiden osalta.</li><li>**Päänimikkeen vakioprosenttiosuus** – Erillisen myyntihinnan alkuperä on prosenttiosuus päänimikkeen vakiohinnasta. Voit vaihtaa oletusarvon. Tämä valinta on käytettävissä vain tuottojakomallin alinimikkeiden osalta. Se on alinimikkeiden oletusvaihtoehto. Kun alituotteen vaihtoehto muutetaan arvosta **prosentti ylätason vakiohinnasta** **prosenttiin ylätason laskun hinnasta** tai **prosenttiosuudesta ylätason laskun hinnasta** arvoon **prosentti ylätason laskun hinnasta vakiohinta**, myös lasketut arvot päivitetään.</li></ul> |
| Erillismyyntihinta | Määritä nimikkeen erillismyyntihinta. Tämä kenttä on käytettävissä vain, jos **Erillismyyntihinnan alkuperä** -kentän arvoksi on valittu **Summa**. |
| Prosenttia | Määritä erillisen myyntihinnan prosenttiosuus. Tämä kenttä on käytettävissä, kun **erillisen myyntihinnan alkuperä** -kentän arvoksi määritetään **Prosenttia nimikkeestä**, **päälaskun hinnan prosentti** tai **Päätason vakiohinta prosenttina**. |
| Tuoton jako | <p>Määritä, käytetäänkö rivin tuottojen jakoa:</p><ul><li>**Valittu** – Vain nimikkeet, joita varten on määritetty tuottojen jakomalli, voidaan valita **Nimikesuhde**-kentässä. Voit valita tämän valintaruudun vain tulonjakomallin ylätason kohteille.</li><li>**Tyhjä** – Nimike on vakionimike, joka ei käytä tuottojen jakoa.</li></ul> |
| Suhde | Symboli ilmaisee, onko nimike tuottojen jakamisen pää- vai alinimike. |
| Nimikekoodi | <p>Valitse nimikekoodi: **Taulukko** tai **Ryhmä**.</p><p>Jos **Tuottojen jako** -valintaruutu on valittuna, tämän kentän arvoksi on asetettu **Taulukko**, eikä arvoa voi muuttaa.</p> |
| Nimikkeen suhde | <p>Valitse nimikenumero.</p><p>Jos **tuottojen jako** -valintaruutu on valittuna, valittavissa ovat vain ne nimikkeet, jotka ovat päänimikkeitä, jolle on määritetty tuottojen jakomalli. Kun päänimike on valittuna, luettelo päivitetään automaattisesti kyseisen päänimikkeen alinimikkeillä.</p> |
| Päänimike | Päänimikkeen tässä kentässä näkyy nimiketunnus. Tuottojen jaon alinimikkeissä näkyy päänimikkeen nimiketunnus. |

## <a name="mea-templates"></a>MEA-mallit

**MEA-mallien** sivulla voit luoda ja muokata useita elementtien järjestelyjä (MEA) -mallitunnuksia. Näitä tunnuksia käytetään **tulojen kohdistus** -sivulla nimikkeiden ryhmittelyssä yhteen.

### <a name="create-a-template"></a>Luo malli

Määritä MEA-malli noudattamalla seuraavia ohjeita.

1. Valitse **MEA-mallit**-sivulla **Uusi**.
1. Kirjoita **MEA-mallin tunnus** -kenttään yksilöivä tunnus.
1. Syötä **Kuvaus**-kenttään kuvaus.
1. Valitse **Lykätty sopimuksen tuottotili** -kentässä tili, jota haluat käyttää kirjauskansiomerkinnöissä, kun MEA-sopimuslasku luodaan. Tämä kenttä on käytettävissä, kun toistuva sopimuslaskutus otetaan käyttöön ja sitä käytetään.
1. Valitse **Tallenna**.
