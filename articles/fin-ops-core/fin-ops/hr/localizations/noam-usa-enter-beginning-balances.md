---
title: Palkanlaskennan alkusaldojen antaminen
description: Tässä ohjeaiheessa käsitellään vaiheet, joilla ansiokoodien, vähennysten, etujen ja verojen alkusaldot annetaan. Kumppanit arvostavat näitä tietoja, sillä niiden avulla tiedot voidaan siirtää toisesta järjestelmästä uuteen käyttöönotettuun palkanlaskentaan.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 209636d6416a784d298bcfb134f5486c1f5cf202
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568542"
---
# <a name="enter-payroll-beginning-balances"></a>Palkanlaskennan alkusaldojen antaminen

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään vaiheet, joilla ansiokoodien, vähennysten, etujen ja verojen alkusaldot annetaan. Kumppanit arvostavat näitä tietoja, sillä niiden avulla he voivat siirtää tiedot toisesta järjestelmästä uuteen käyttöönotettuun palkanlaskentaan. Palkanlaskennan alkusaldojen antamista varten tarkistetaan seuraavat tiedot:

- Työntekijätietueet on viety järjestelmään ja ne ovat käytettävissä.
- Seuraavat tiedot on määritetty työntekijöille:

    - Maksujaksot ja maksukaudet
    - Ansiokoodit
    - Verot
    - Edut ja vähennykset

- Yrityksen on pitänyt valita päivämäärä, johon palkanlaskennat alkusaldot voidaan määrittää.
- Vanhasta järjestelmästä kerättiin tiedot kaikista ansioista, eduista ja vähennyksistä, edun osuuksista, työntekijän verotuksesta sekä työnantajan verotuksesta ja vuoden alusta kertyneistä summista.

Harkitse, kuinka yksityiskohtaisia tietoja tarvitset, kun aloitat alkusaldojen antamisen suunnittelun. Useimmat yritykset ilmoittavat yhden, konsolidoidun vuoden alusta kertyneen summan. Jos tietojen on kuitenkin oltava yksityiskohtaisempia, saldot voidaan ilmoittaa neljännesvuosittain. Tarvittavan tarkkuustason päättäminen määrittää, kuinka monta manuaalista maksuilmoitusta on luotava kullekin työntekijälle. Jos kyse on summasta vuoden alusta, kullekin työntekijälle tarvitaan vain yksi manuaalinen ilmoitus. Voit tehdä tämän käyttämällä edellisen järjestelmän viimeisen maksuilmoituksen vuoden alusta kertynyttä summaa uuteen palkanlaskentajärjestelmään ilmoitettavana summana.

Seuraavassa esimerkissä näytetään, miten työntekijän palkanlaskennan alkusaldot, mukaan lukien ansiokoodit, edut ja vähennykset sekä verot, annetaan. Jos kyse olisi aidosta esimerkistä, jokaiselle ansiokoodille, edun vähennykselle, edun osuudelle sekä työntekijän ja työnantajan verotukselle olisi rivinimike, johon lisätty summa olisi summa vuoden alusta. Käytä tätä koodi- ja summaluetteloa luodessasi ansio- ja maksuilmoituksen manuaalisesti siten, että kirjanpito on poistettu käytöstä, palkanlaskennan alkusaldojen tuontia varten. Kirjanpito poistetaan käytöstä, koska et halua kirjata tätä alkusaldon maksuilmoitusta kirjanpitoon. Se tehtiin vanhassa järjestelmässä ja siirtyy uuteen järjestelmään, kun määrität alkusaldot kirjanpidossa.

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a>A. Palkanlaskennan alkusaldoissa käytettävien ansiokoodien määrittäminen

Varmista palkanlaskennan alkusaldoja annettaessa, että Salli ansioilmoitushintojen muokkaus -vaihtoehto otettiin käyttöön, kun käytettävät ansiokoodit määritettiin. Kun vaihtoehto on käytössä, voit antaa summat manuaalisesti vanhasta järjestelmästä. 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a>B. Alkusaldon sisältävän ansioilmoituksen luominen työntekijälle

Tässä vaiheessa kullekin työntekijälle luodaan manuaalisesti vanhan järjestelmän viimeisen maksukauden ansioilmoitus, joka luo ansioilmoitusrivit uuteen palkanlaskentajärjestelmään. Lisää yksi rivi kullekin ansiokoodille sekä summalle vuoden alusta ja tunneille. Mallivaiheet ovat seuraavat:

1. Avaa **Kaikki ansioilmoitukset** -sivu ja valitse **Uusi**.

    Kirjoita seuraavasti: 

    | Kenttä      | Arvo                 |
    |------------|-----------------------|
    | Työntekijä     | Michael Redmond       |
    | Maksujakso  | sm                    |
    | Maksukausi | 16.6.2017–30.6.2017 |

2. Anna **Ansioilmoitusrivi**-välilehdessä seuraavat arvot:

    Rivi 1: **Ansioilmoitusrivi**-välilehti

    | Kenttä            | Arvo       |
    |------------------|-------------|
    | Ansiokoodi    | Normaali palkka |
    | Määrä         | 1.00        |
    | Osuus             | 30,000      |
    | Rivin erittely -välilehti |             |
    | Manuaalinen           | (merkitty)    |

    Rivi 2: **Ansioilmoitusrivi**-välilehti

    | Kenttä            | Arvo    |
    |------------------|----------|
    | Ansiokoodi    | Bonus    |
    | Määrä         | 1.0000   |
    | Osuus             | 4250.00  |
    | Rivin erittely -välilehti |          |
    | Manuaalinen           | (merkitty) |

    Rivi 3: **Ansioilmoitusrivi**-välilehti

    | Kenttä           | Arvo      |
    |-----------------|------------|
    | Ansiokoodi   | Provisio |
    | Määrä        | 1.0000     |
    | Osuus            | ! 299,00   |
    | Osuus            | 1,299.00   |
    | Rivin erittely -välilehti |            |
    | Manuaalinen          | (merkitty)   |

    > [!NOTE]
    > **Manuaalinen**-liukusäätimen asetukseksi on määritettävä **Kyllä** jokaisen ansioilmoitusrivin **Rivin erittely** -välilehdessä, jotta palkanlaskennan alkusaldot annetaan jokaiselle työntekijälle.

3. Valitse **Toiminto**-ruudussa **Vapauta ansioilmoitus** USA-FED-ER-FICA.
4. Avaa **Luo maksuilmoitukset** -sivulla valitsemalla **Toiminto**-ruudussa **Maksuilmoitus** ja määritä seuraavat arvot:

    | Kenttä              | Arvo     |
    |--------------------|-----------|
    | Maksupäivä       | 6/30/2017 |
    | Maksusuorituksen tyyppi   | Manuaalinen    |
    | Poista kirjanpito käytöstä |   Kyllä     |

    > [!NOTE] 
    > Tämä on käytettävissä vain, kun maksusuoritustyyppi on manuaalinen ja kun käyttäjä haluaa poistaa maksusuorituksen kirjanpidon käytöstä.

    Valitse **OK** ja sulje **Infoloki**.

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a>Miksi Poista kirjanpito käytöstä -liukusäätimen asetuksiksi on valittava Kyllä maksuilmoituksia luotaessa?

Kun liukusäätimen asetuksena on **Kyllä**, maksuilmoituksen rivin jakaminen ja vienti kirjanpitoon estetään. Kirjanpidon summat päivitettiin aiemmin, kun vanhan järjestelmän tilien saldot vietiin. Palkanlaskennan alkusaldojen viennin avulla voit luoda raportteja, jotka sisältävät aiempien vuosien tiedot sekä tunnistusrajat etuja ja verotusta varten.

### <a name="c-create-pay-statements-for-employees"></a>C. Työntekijöiden maksuilmoitusten luominen

Kun olet luonut alkusaldot sisältävät maksuilmoitukset, sinun on tarkistettava, että maksuilmoitukset vastaavat palkanlaskennan tietoja. Sinun on myös päivitettävä etu- ja verotustiedot manuaalisesti vastaamaan aiemman palkanlaskentajärjestelmän tietoja. Kun olet tarkistanut, että aiemman palkkalaskentajärjestelmään summat vastaavat nykyisten maksuilmoitusten summia, maksuilmoitukset on viimeisteltävä.

1. Avaa **Kaikki maksuilmoitukset** -sivu.
2. Korosta Michael Redmondin viimeksi luotu maksuilmoitus
3. Avaa **Maksuilmoitus**-sivu valitsemalla **Muokkaa**.
4. Avaa **Edun vähennykset** -välilehti ja anna seuraavat arvot:

    | Kenttä             | Arvo            |
    |-------------------|------------------|
    | Etu           | Vähennyssumma |
    | Lisäeläkemaksut (Yhdysvalloissa 401K)              | Liity      |
    | Hammashuolto            | SubSp            |
    | Huolettavien kulut | Liity      |
    | Näkö            | SupSp            |

5. Anna **Edun osuudet** -välilehdessä seuraavat arvot:

    | Kenttä   | Arvo               |
    |---------|---------------------|
    | Etu | Osuussumma |
    | Lisäeläkemaksut (Yhdysvalloissa 401K)    | Liity         |
    | Hammashuolto  | SubSp               |
    | Näkö  | SubSp               |

6. Anna **Verovähennykset** -välilehdessä seuraavat arvot:

    | Kenttä           | Arvo            |
    |-----------------|------------------|
    | Alv-koodi        | Vähennyssumma |
    | USA-FED-ER-FICA | 1600.00          |
    | USA-FED-ER-MEDI | 825.75           |

7. Anna **Vero-osuudet** -välilehdessä seuraavat arvot:
8. Valitse **Laske**.

    > [!IMPORTANT] 
    > Tarkista, että työntekijän maksuilmoituksen loppusumma vastaa vanhan järjestelmän vuoden alusta kertynyttä summaa. Seuraavan vaiheen viimeistelyn voit jättää odottamaan, kunnes yleiset tarkistukset voi tehdä koostetusti kaikille palkkailmoituksille. Kun kaikki on maksuilmoitukset on tarkistettu voit viimeistellä ne.

Samaa prosessi voidaan toistaa tarvittaessa erikseen kullekin edellisen vuoden vuosineljänneksille. Se on tarpeellista vain, jos asiakas haluat nähdä tiedot neljännesvuosittain ilman, että tiedot olisi tarkistettava vanhasta järjestelmästä.

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a>Työntekijän alkusaldoa antaessa tapahtuu virhe

Tapahtumat voidaan peruuttaa ja antaa uudelleen. Voit peruuttaa tapahtuman suorittamalla seuraavat vaiheet **Kaikki maksuilmoitukset** -sivulla.

1. Valitse **Palauta**.
2. Valitse **Kyllä**, kun sanoma "Kun palautat tämän maksuilmoituksen, maksuilmoitukselle luodaan vastakirjauksena palautusmaksuilmoitus. Kumpaakaan maksuilmoitusta ei voi muokata. Haluatko palauttaa tämän maksuilmoituksen?" avautuu näyttöön. 

Kun olet peruuttanut maksuilmoitukset, voit luoda työntekijälle uuden maksuilmoituksen aiemmin luodusta ansioilmoituksesta. Muista korjata kaikki ansioilmoituksen virheelliset rivit ennen uuden maksuilmoituksen luontia ja luo sitten uudet maksuilmoitukset oikeilla summilla. 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]