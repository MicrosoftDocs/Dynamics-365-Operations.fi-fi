---
title: Tuoton kohdistus
description: Tässä aiheessa kerrotaan, miten tuoton kohdistusta käytetään tilauslaskutuksessa.
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
ms.openlocfilehash: 2a1bdff364039c6bf0cdfbc11f0979398934c52c
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629419"
---
# <a name="revenue-allocation"></a>Tuoton kohdistus

Tässä aiheessa kerrotaan, miten tuoton kohdistuksen parametrit määritetään laskutusaikataululle. Voit määrittää tuoton kohdistuksen tai muokata sitä, kun luot laskutusaikataulun. Kun avaat aktiivisen tai lopetetun laskutusaikataulun **Tuottojen kohdistus** -sivun, kentät ovat vain luku -kenttiä.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>Määritä tuoton kohdistus laskutusaikataulua varten

Seuraa näitä ohjeita määrittääksesi tuoton kohdistuksen laskutusaikataululle.

1. Valitse laskutusaikataulu tai laskutusaikataulurivi **Kaikki/Aktiiviset laskutusaikataulut** -luettelosivulta.
2. Valitse sivun yläosasta **Tuoton kohdistus** -välilehti ja valitse sitten **Tuoton kohdistus**.
3. Valitse **Järjestelytyyppi, jossa on useita elementtejä** -kentästä useiden elementtien järjestyksen (MEA) tyyppi.
4. Määritä MEA-numero **Useiden elementtien järjestelynumero**-kentässä. Määritä sitten lykätyn sopimuksen tuottotili **Lykätty sopimustuottotili** -kenttään.

    Jos määrität **Järjestelytyyppi, jossa on useita elementtejä** -kentänarvoksi **Yksittäinen**, jokaisella rivillä käytetään samaa **usean elementin järjestelynumeron** ja **lykätyn sopimuksen tuottotilin** arvoja. Jos määrität **Järjestelytyyppi, jossa on useita elementtejä** -kentän arvoksi **Useita**, voit määrittää kullekin riville eri **usean elementin järjestelynumeron** ja **lykätyn sopimuksen tuottotilin** arvot.
    
    MEA-numero voidaan määrittää vain kahdelle tai useammalle nimikkeelle. Yksittäisellä rivillä ei voi olla omaa MEA-numeroa.

5. Valitse **Tallenna**.

### <a name="fields"></a>Kentät

**Järjestelytyyppi, jossa on useita elementtejä** -sivu sisältää seuraavat kentät.

| Kenttä | Kuvaus |
|---|---| 
| Järjestelytyyppi, jossa on useita elementtejä | <p>Valitse tapahtuman MEA-tyyppi:</p><ul><li>**Useita** – Tapahtuman rivinimikkeet ovat osa MEA-järjestelyä tai on olemassa useita järjestelyitä.</li><li>**Ei mitään** – Tapahtuma on vakiotapahtuma, jolla ei ole tuoton kohdistusta.</li><li>**Yksittäinen** – Kaikki tapahtuman nimikkeet kuuluvat yhteen MEA-järjestelyyn.</li></ul> |
| Useiden elementtien järjestelynumero | <p>Rivin MEA-numero. Tämä kenttä on käytettävissä, kun **Järjestelytyyppi, jossa on useita elementtejä** -kentän arvoksi on valittu **Useita**.</p><p>Jos tämä kenttä on tyhjä ja määrität MEA-numeron, **Erillismyyntihinnan alkuperä**- ja **Erillismyyntihinta**-kentät päivitetään automaattisesti **Nimikkeen erillismyyntihinta** -sivun arvojen perusteella. Vain myyntitilauksen muille riveille määritetyt MEA-numerot ovat käytettävissä.</p> |
| Lykätty sopimuksen tuottotili | Määritä tili, jota käytetään kirjauskansiomerkinnöissä, kun MEA-sopimuslasku luodaan. Tämä kenttä on käytettävissä vain, kun toistuvaa sopimuslaskutusta käytetään. |
| **Rivit** | |
| Muuttujan numero | Myyntitilauksen varianttinumero. |
| Nimiketunnus | Myyntitilauksen nimikenumero. |
| Laskutustiheys | Valitse tuoton kohdistuksen tiheys: **Päivittäin**, **Kuukausittain**, **Neljännesvuosittain**, **Puolivuosittain** tai **Vuosittain**. |
| Määrä | Arvo myyntitilauksesta. |
| Sopimuksen arvo | Sopimuksen arvo. |
| Useiden elementtien järjestelynumero | <p>Rivin MEA-numero. Tämä kenttä on käytettävissä, kun **Järjestelytyyppi, jossa on useita elementtejä** -kentän arvoksi on valittu **Useita**.</p><p>Jos tämä kenttä on tyhjä ja määrität MEA-numeron, **Erillismyyntihinnan alkuperä**- ja **Erillismyyntihinta**-kentät päivitetään automaattisesti **Nimikkeen erillismyyntihinta** -sivun arvojen perusteella. Vain myyntitilauksen muille riveille määritetyt MEA-numerot ovat käytettävissä. Jos näitä arvoja ei ole määritetty nimikkeelle, käytetään **Useiden elementtien tuoton kohdistusparametrit** -sivun arvoja.</p> | 
| Erillismyyntihinnan alkuperä | <p>Erillismyyntihinnan alkuperä:</p><ul><li>**Summa** – Erillinen myyntihinta on summa, jonka määrität olevan suurempi kuin 0 (nolla). Summa muunnetaan toimintojen ja alkuperävaluuttojen välillä tarpeen mukaan.</li><li>**Perusmyyntihinta** – Erillinen myyntihinta vastaa nimikkeen perusmyyntihintaa.</li><li>**Laskutushinta** – Erillinen myyntihinta vastaa nimikkeen laskutushintaa.</li><li>**Nimikkeen prosenttiarvo** – Erillinen myyntihinta määritetään prosenttiarvona, ja se lasketaan nimikkeen hinnan mukaan. Jos valitset tämän vaihtoehdon, määritä oletusprosenttimäärä.</li><li>**Määritä jäännösmäärä** – Itsenäisen myyntihinnan alkuperä lasketaan seuraavasti: *Päätuotteen sopimusarvo yhteensä* – *Alinimikkeiden erillinen myyntihinta yhteensä*:</p><ul><li>*Päänimikkeen sopimuksen kokonaisarvo* on nettosumma tai laskutettu summa.</li><li>*Alinimikkeiden erillinen myyntihinta* on kaikkien alinimikkeiden laajennettu tai itsenäinen myyntihinta lukuun ottamatta alinimikettä, joka käyttää tätä itsenäistä myyntihinnan alkuperää.</li></ul><p>Jos laskettu summa on negatiivinen arvo, summaksi määritetään 0 (nolla).</p><p>**Huomautus:** Tämä vaihtoehto voidaan valita vain yhdelle alinimikkeelle tuottojen jakamisen yhteydessä.</p></li><li>**Ei mitään** – Erillisen myyntihinnan alkuperä perustuu alinimikkeisiin. Tämä asetus koskee nimikkeitä, jotka on määritetty tuottojen jakomallin päänimikkeiksi. Jos **Tuottojen jako** -valintaruutu on valittuna, tämä vaihtoehto on automaattisesti valittuna eikä asetusta voi muuttaa.</li><li>**Päänimikkeen laskun prosenttiosuus** – Erillisen myyntihinnan alkuperä on prosenttiosuus päänimikkeen laskun hinnasta. Tämä valinta on käytettävissä vain tuottojakomallin alinimikkeiden osalta.</li><li>**Päänimikkeen vakioprosenttiosuus** – Erillisen myyntihinnan alkuperä on prosenttiosuus päänimikkeen vakiohinnasta. Tämä valinta on käytettävissä vain tuottojakomallin alinimikkeiden osalta. Kun alituotteen vaihtoehto muutetaan arvosta **prosentti ylätason vakiohinnasta** **prosenttiin ylätason laskun hinnasta** tai **prosenttiosuudesta ylätason laskun hinnasta** arvoon **prosentti ylätason laskun hinnasta vakiohinta**, myös lasketut arvot päivitetään.</li></ul> |
| Erillismyyntihinta | <p>Rivin erillismyyntihinta tapahtumavaluuttana.</p><p>**Summa**-kentän arvo joko syötetään tai lasketaan.</p> |
| Sopimuksen erillismyyntihinta | Sopimuksen erillismyyntihinta. |
| Jäljellä oleva sopimuksen tuotto | Sopimuksen jäljellä oleva tuoton summa. Tämä summa on niiden rivien summa, joille ei ole vielä luotu laskua. |
| Sopimuksen kokonaistuotto | Rivin sopimuksen koko tuoton summa. Tämä summa on kaikkien rivien summa riippumatta siitä, onko niille luotu laskua. |
| Lykätty sopimuksen tuottotili | <p>Määritä tili, jota käytetään kirjauskansiomerkinnöissä, kun MEA-sopimuslasku luodaan.</p><p>Tämä kenttä on käytettävissä vain, kun toistuvaa sopimuslaskutusta käytetään.</p> |
| Virhe | Kaikki tuottokohdistusvirheet. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Tuoton kohdistuksen käyttö myyntitilauksessa

Voit käyttää myyntitilauksessa tuoton kohdistustoimintoa noudattamalla seuraavia ohjeita.

1. Valitse **Kaikki myyntitilaukset** -sivulla myyntitilaus, jossa on nimikkeitä.
2. Valitse **Lasku**-välilehden **Tuoton kohdistus** -kohdasta **Tuoton kohdistus**.
3. Määritä MEA-tyyppi **Järjestelytyyppi, jossa on useita elementtejä**-kentässä.
4. Määritä MEA-numero **Useiden elementtien järjestelynumero**-kentässä.
5. Jos **Järjestelytyyppi, jossa on useita elementtejä**  -kentän arvoksi on määritetty **Useita**, valitse haluamasi rivit ja valitse sitten **Käytä valittuun**.
6. Valitse **Tallenna**.

Jos käytät tuottojen ja kulujen lykkäyksiä, järjestelmä luo automaattisesti lykkäysaikataulun. Näet sen **Kaikki lykkäysaikataulut** -sivulla.
