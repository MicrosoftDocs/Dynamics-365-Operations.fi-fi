---
title: Toimittajamaksujen luominen maksuehdotuksen avulla
description: "Tässä aiheessa on yleiskatsaus maksuehdotusvaihtoehdoista. Artikkeli sisältää myös esimerkkejä maksuehdotusten toiminnasta. Maksuehdotuksia käytetään usein toimittajan maksujen luomiseen, koska kyselyn avulla on nopeaa valita toimittajan laskuja maksuun esimerkiksi eräpäivän ja käteisalennuksen mukaan."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: b46037b9509f329e18f0da69d530f6b1f88c8888
ms.lasthandoff: 03/31/2017


---

# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Toimittajamaksujen luominen maksuehdotuksen avulla

Tässä aiheessa on yleiskatsaus maksuehdotusvaihtoehdoista. Artikkeli sisältää myös esimerkkejä maksuehdotusten toiminnasta. Maksuehdotuksia käytetään usein toimittajan maksujen luomiseen, koska kyselyn avulla on nopeaa valita toimittajan laskuja maksuun esimerkiksi eräpäivän ja käteisalennuksen mukaan. 

Organisaatiot käyttävät usein maksuehdotuksia luodakseen toimittajan maksuja, koska maksuehdotuskyselyn avulla on nopeaa valita toimittajan laskuja maksuun, eräpäivään, käteisalennukseen ja muihin ehtoihin perustuen. 

Maksuehdotuskysely sisältää useita välilehtiä, joista jokaisella on eri asetuksia maksettavien laskujen valinnalle. **Parametri** -välilehti sisältää vaihtoehdot, jotka suurin osa organisaation eniten. - **Sisällytettävät tietueet** -pikavälilehdessä voit määrittää mitkä laskut tai toimittajien sisällytettävät alueet ominaisuuksia määrittämällä maksun. Jos haluat maksaa vain tietyn alueen toimittajat, voit määrittää suodattimen toimittajan alueelle. Tätä toimintoa käytetään usein laskuja, tietyn maksutavan. Jos suodatin määrittää missä **maksutapa** = **Tarkista**, vain laskuille, joilla on tämä maksutapa valitaan maksettavaksi, jos ne täyttävät muut ehdot, jotka on määritetty kysely. **Lisäparametrit**-välilehti lisäasetuksia, joista kaikki eivät ole aiheellisia organisaatiosi kannalta. Tämä välilehti sisältää esimerkiksi asetukset laskujen keskitettyä maksamista varten.

## <a name="parameters"></a>Parametrit
-   **Laskuja,** – laskut, jonka määrittää päivämääräalueen **päivästä** ja **asti** kenttiin valittavissa eräpäivän, käteisalennuksen päivämäärän tai molemmat. Jos käteisalennuksen päivämäärän, järjestelmä etsii ensin laskut, joilla käteisalennuksen päivämäärä päivämäärä- ja päättymispäivä. Järjestelmä määrittää, onko lasku oikeutettu käteisalennukseen käyttämällä istunnon päivämäärää varmistaakseen, että käteisalennuksen päivämäärä ei ole jo mennyt.
-   **Aloituspäivämäärä** ja **Lopetuspäivämäärä** – Maksut, joiden eräpäivä tai käteisalennuksen päivämäärä ovat määritetyssä päivämäärävälissä valitaan maksuun.
-   **Maksupäivä** – Jos päivämäärä on määritetty, kaikki maksut luodaan tänä päivänä. **Aikaisin maksupäivä** -kenttä ohitetaan.
-   **Aikaisin maksupäivä** – Kirjoita aikaisin maksupäivä. Esimerkiksi **päivästä** ja **mennessä** kentät määrittää vaihdella välillä 1 päivänä syyskuuta syyskuun 10 ja Aikaisin maksupäivä on syyskuun 5. Tässä tapauksessa kaikki laskut, joiden eräpäivä 1 päivänä syyskuuta ja 5 päivänä syyskuuta on maksupäivä, syyskuun 5. Kuitenkin kaikki laskut, joiden eräpäivä syyskuun 5-syyskuu 10, on maksupäivämäärä, joka vastaa kunkin laskun eräpäivä.
-   **Summaraja** – Syötä suurin kokonaissumma kaikille maksuille.
-   **Luo maksuja ilman laskun esikatselun** – Jos tämä vaihtoehto on **Kyllä**, maksut luodaan heti **toimittajamaksut** sivulla. **Maksuehdotuksen** sivu ohitetaan. Maksujen luonti on siis nopeampaa. Maksuja voi edelleen muokata **Toimittajan maksut** -sivulla. Vaihtoehtoisesti voit palata **Maksuehdotus**-sivulle **Muokkaa valitun maksun laskuja** -painikkeella.

## <a name="advanced-options"></a>Lisäasetukset
-   **Tarkista toimittajan saldo** – Jos tämä asetus on **Kyllä**, järjestelmä varmistaa, että toimittajalla ei ole saatavien saldoa ennen, kuin yksikään lasku maksetaan. Jos toimittaja on debet-saldo, ei maksu luodaan. Toimittaja voi olla esimerkiksi hyvityslaskut tai maksuja, jotka on kirjattu mutta ei ole vielä selvitetty. Näissä tapauksissa toimittajalle ei tule maksaa. Hyvityslaskut tai maksut tulee sen sijaan selvittää jäljellä oleviin laskuihin.
-   **Poista negatiiviset maksut**: Tämä asetus on erilainen sen mukaan, suoritetaanko maksut yksittäisille laskuille vai niiden laskujen summalle, jotka vastaavat maksuehtoja. Tämä toiminta määritellään maksutavassa.
-   **Maksu jokaiselle laskulle** – Jos **Poista negatiiviset maksut** asetukseksi on määritetty **Kyllä**, ja toimittajalla on selvittämätön lasku ja maksu, ainoastaan lasku valitaan maksuun. Aiempaa maksua ei selvitetä laskua vastaan. Jos **Poista negatiiviset maksut** asetukseksi on määritetty **Ei**, ja sekä lasku ja maksu ovat selvittämättä, molemmat valitaan maksuun. Suoritukselle luodaan maksu, ja maksulle luodaan palautus (negatiivinen suoritus).
-   **Maksu laskujen summalle** – Jos **Poista negatiiviset maksut** -asetukseksi on määritetty **Kyllä** ja toimittajalla on selvittämätön lasku ja maksu, molemmat valitaan maksuun ja summat lisätään yhteen maksun kokonaissummaan. Ainoa poikkeus on, jos kokonaissumma johtaisi palautukseen. Tässä tapauksessa laskua eikä maksua valita. Jos ** Poista negatiiviset maksut ** asetukseksi on määritetty **ei**, laskua ja maksua ei ole selvitetty, maksua varten valitut sekä laskun maksu ja summat lisätään yhdessä tuottamaan maksusumma.
-   **Tulosta vain raportti** – Aseta tämän asetuksen arvoksi **Kyllä** voidaksesi tarkastella maksuehdotuksen tuloksia raportissa luomatta maksuja.
-   **Sisällytä toimittajan laskut muilta oikeushenkilöiltä** – Jos organisaatiossasi käytetään keskitettyä maksuprosessia ja maksuehdotuksen hakuehtojen tulee sisältää laskuja muista yrityksistä, aseta tämän asetuksen arvoksi **Kyllä**.
-   **Ehdota erillistä toimittajan maksua oikeushenkilökohtaisesti** – Jos tämä asetus on **Kyllä**, kunkin yrityksen kullekin toimittajalle luodaan erilliset laskut. Maksulla oleva toimittaja on kunkin yrityksen vastaanottaman laskun toimittaja. Jos asetuksen arvo on **Ei** ja samalla toimittajalla on laskuja maksettavanaan useassa yrityksessä, yksi maksu luodaan kaikkien valittujen yritysten valittujen laskujen yhteenlasketulle summalle. Maksun toimittaja on nykyisen yrityksen toimittaja. Jos nykyisessä yrityksessä ei ole toimittajatiliä, käytetään ensimmäisen maksettavan laskun toimittajatiliä.
-   **Maksuvaluutan** – kenttä määrittää valuutta, jota kaikki maksut on luotu. Valuuttaa ei ole määritetty, jos lasku maksetaan laskun valuuttana.
-   **Maksuviikonpäivä** – Anna viikonpäivä, jona maksu tulee suorittaa. Tätä kenttää käytetään vain, jos maksutapa on määritetty summaamaan maksettavat laskut tiettynä viikonpäivänä.
-   **Vastatilin tyyppi** ja **vastatili** – Määritä nämä kentät määrittääksesi tietyn tilin tyypin (kuten **kirjanpidon** tai **pankin**) ja vastatili (esimerkiksi pankkitilin tietyn). Oletusvastatilin tyyppi ja vastatili määritetään maksutavan lasku, mutta näiden kenttien avulla voit ohittaa oletusarvot.
-   **Lisää suodattimia** – edelleen **sisällytettävät tietueet** -pikavälilehdessä voit määrittää ehtoja muita alueita. Jos haluat maksaa toimittajien alue, voit määrittää suodattimen toimittajan alueelle. Tätä toimintoa käytetään usein laskuja, tietyn maksutavan. Jos suodatin määrittää missä **maksutapa** = **Tarkista**, vain laskuille, joilla on tämä maksutapa valitaan maksettavaksi, jos ne täyttävät muut ehdot, jotka on määritetty kysely.

## <a name="scenarios"></a>Skenaariot
| Toimittaja | Lasku | Laskun päivämäärä | Laskun summa | Eräpäivä | Käteisalennuksen päivämäärä | Käteisalennussumma |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15. kesäkuuta      | 500,00         | 15. heinäkuuta  | 29. kesäkuuta            | 10,00                |
| 3050   | 1002    | 20. kesäkuuta      | 600,00         | 20. heinäkuuta  | 4. heinäkuuta             | 12,00                |
| 3075   | 1003    | 15. kesäkuuta      | 250,00         | 29. kesäkuuta  |                    | 0,00                 |
| 3100   | 1004    | 17. kesäkuuta      | 100,00         | 17. heinäkuuta  | 1. heinäkuuta             | 1,00                 |

April maksaa toimittajien laskut 1. heinäkuuta. Hän käyttää maksuehdotusta tehtävän tehokkaampaan suorittamiseen.

### <a name="option-1-by-cash-discount"></a>Vaihtoehto 1: Käteisalennuksen mukaan

April valitsee **käteisalennuksen** ehdotustyypiksi. Hän kirjoittaa päivä alue, kesä-26 10 päivänä heinäkuuta. Seuraavat laskut sisällytetään ehdotukseen:

-   1002, koska alennuspäivämäärä, 4.7., on maksupäivien välissä
-   1004, koska alennuspäivämäärä, 1.7., on maksupäivien välissä

Seuraavat laskut eivät sisälly ehdotukseen:

-   1001, koska alennuspäivämäärä, 29.6., on vanhentunut. eikä lasku siis ole enää oikeutettu käteisalennukseen
-   1003, koska laskulla ei ole alennuspäivämäärää.

### <a name="option-2-by-due-date"></a>Vaihtoehto 2: Eräpäivän mukaan

April valitsee ehdotustyypiksi **Eräpäivän mukaan**. Hän kirjoittaa päivä alue, kesä-26 10 päivänä heinäkuuta. Seuraavat laskut sisällytetään ehdotukseen:

-   1003, koska eräpäivä, 29. kesäkuuta, on maksupäivämäärien välissä.

Seuraavat laskut eivät sisälly ehdotukseen:

-   1001, koska eräpäivä, 15. heinäkuuta, ei ole maksupäivämäärien välissä.
-   1002, koska eräpäivä, 20. heinäkuuta, ei ole maksupäivämäärien välissä.
-   1004, koska eräpäivä, 17. heinäkuuta, ei ole maksupäivämäärien välissä.

### <a name="option-3-by-due-date-and-cash-discount"></a>Vaihtoehto 3: Eräpäivän ja käteisalennuksen mukaan

April valitsee ehdotustyypiksi **Eräpäivän ja käteisalennus**. Hän kirjoittaa päivä alue, kesä-26 10 päivänä heinäkuuta. Seuraavat laskut sisällytetään ehdotukseen:

-   1003, koska eräpäivä, 29. kesäkuuta, on maksupäivämäärien välissä.
-   1002, koska alennuspäivämäärä, 4.7., on maksupäivien välissä
-   1004, koska alennuspäivämäärä, 1.7., on maksupäivien välissä

Seuraavat laskut eivät sisälly ehdotukseen:

-   1001, koska alennuspäivä, 29. kesäkuuta, on vanhentunut, eikä lasku ole enää oikeutettu käteisalennukseen; lisäksi eräpäivä, 15. heinäkuuta on päivämäärävälin ulkopuolella.

## <a name="country-specific-considerations"></a>Maa-/aluekohtaisia huomioita
### <a name="norway"></a>Norja

#### <a name="dimension-control"></a>Dimension ohjaus

Dimension ohjauksen avulla voit hallita maksuehdotuksen luotujen rivien ryhmittelyä ja määrittää oletusdimensioita taloushallinnon dimensioiden perusteella laskuissa käytettäväksi. Norjan maakontekstissa on kullekin maksutavalle taloushallinnon dimensio -välilehti, jossa voidaan ottaa käyttöön dimension valvonta ja dimensioiden ryhmittely. Mahdolliset vaihtoehdot ovat:

-   **Dimension ohjaus** -kenttä ei ole käytettävissä. Maksuehdotus toimii kuten kaikissa muissa maissa.
-   **Dimension ohjaus** -kenttä on aktivoitu määrittämättä dimensioita. Maksuehdotus luodaan ottamatta huomioon dimensioita. Luotu tapahtuma ei peri dimensioita käytetystä tietueesta.
-   **Dimension ohjaus** -kenttä on aktivoitu ja lisädimensioita on aktivoitu. Määritä nyt, miten dimensiot kopioidaan kirjauskansioon. Esimerkiksi: • Valitse **liiketoimintayksikön** kohti liiketoimintayksikön maksuehdotuksen maksutavalle • Valitse valintaruutu **CostCenter** haluat luoda kustannuspaikkakohtaisen maksuehdotuksen maksutavalle

**Huomaa:** Jos valitset kolmannessa vaihtoehdossa useita dimensioita, maksuehdotus luodaan dimensioiden yhdistelmälle.

#### <a name="bank-account-selection"></a>Pankkitilin valitseminen

Voit määrittää vakioveloitusten maksutilin jokaiselle laskentayksikölle riippumatta maakontekstista. Tämä määritetään ehdotuksen luomille maksuriveille. Pankkitili-toiminnolla voit määrittää useita veloitettavia pankkitilejä, joita hallitaan dimension ja valuutan tai näiden yhdistelmien mukaan käyttämään eri veloitettavia pankkitilejä yhdistelmästä riippuen.. Voit määrittää näiden yhdistelmiä **maksutapojen** sivua käyttämällä **Pankkitilit** painike käytettävissä kullekin maksutavalle kanssa **tilin kirjaustapa** = **pankin**.


