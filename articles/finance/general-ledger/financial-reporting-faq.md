---
title: Taloushallinnon raportoinnin usein kysytyt kysymykset
description: Tämä ohjeaihe sisältää vastauksia eräisiin usein kysyttyihin talousraportoinnin kysymyksiin.
author: jiwo
ms.date: 07/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3690a541b503281f204221a72bfb5a371984d9e4
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605276"
---
# <a name="financial-reporting-faq"></a>Taloushallinnon raportoinnin usein kysytyt kysymykset

Tämä ohjeaihe sisältää vastauksia usein kysyttyihin talousraportoinnin kysymyksiin.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Miten rajoitan raportin käyttöoikeuksia puurakenteen suojauksen avulla?

Seuraavassa esimerkissä kerrotaan, miten raportin käyttöoikeuksia rajoitetaan puurakenteen suojauksen avulla.

USMF-esittely-yrityksellä on **taseraportti**, johon kaikilla taloushallinnon raportoinnin käyttäjillä ei pitäisi olla käyttöoikeuksia. Voit rajoittaa yksittäisen raportin käyttöoikeutta puurakenteen suojauksen avulla siten, että vain tietyt käyttäjät voivat käyttää sitä.

1. Kirjaudu Financial Reporter Report Designer -palveluun.
2. Luo uusi puumääritys valitsemalla **Tiedosto \> Uusi \> Puumäritys**.
3. Kaksoisnapauta (tai kaksoisnapsauta) **Yhteenveto**-riviä **Yksikkösuojaus**-sarakkeessa.
4. Valitse **Käyttäjät ja ryhmät**.
5. Valitse käyttäjät tai ryhmät, joiden on voitava käyttää tätä raporttia.
6. Valitse **Tallenna**.
7. Lisää uusi puumäärityksesi raportin määritykseen.
8. Valitse puumäärityksessä **Asetus**. Valitse sitten **Raportointiyksikön valinta** -kohdassa **Sisällytä kaikki yksiköt**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Miten tunnistan tilit, jotka eivät täsmää saldojeni kanssa?

Jos sinulla on raportti, jossa ei ole täsmääviä saldoja, käytä seuraavia toimia tilien ja niiden varianssien tunnistamiseksi.

### <a name="in-financial-reporter-report-designer"></a>Financial Reporter Report Designer -palvelussa

1. Luo uusi rivimääritys.
2. Valitse **Muokkaa \> Lisää rivit dimensioista**.
3. Valitse **MainAccount**.
4. Valitse **OK**.
5. Tallenna rivimääritys.
6. Luo uusi sarakemääritys.
7. Luo uusi raportin määritys.
8. Valitse **Asetukset** ja poista tämän vaihtoehdon valinta.
9. Luo raportti. 
10. Vie raportti Microsoft Exceliin.

### <a name="in-dynamics-365-finance"></a>Dynamics 365 Financessa

1. Mene kohtaan **Pääkirja \> Kyselyt ja raportit \> Pääkirja**.
2. Määritä seuraavat kentät:

    - **Aloituspäivä** – syötä tilikauden alkamispäivä.
    - **Päättymispäivämäärä** – syötä päivämäärä, jolle raportti luodaan.
    - **Taloushallinnon dimensio** – aseta tämän kentän arvoksi **Asetettu päätili**.

3. Valitse **Laske**.
4. Vie raportti Exceliin.

Nyt sinun pitäisi pystyä kopioimaan tiedot Financial Reporterin Excel-raportista **Pääkirja**-raporttiin, jotta voit verrata **Loppusaldo**-sarakkeita.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Kun suunnittelen raportin Report Designerissa tai kun luon talousraportin, näyttöön tulee seuraava sanoma: "Työvaihetta ei voitu suorittaa loppuun tietopalvelun kehikossa olevan ongelman vuoksi." Miten reagoin?

Sanoma ilmaisee, että virhe tapahtui, kun järjestelmä yritti hakea taloushallinnon metatietoja tietovaraston osajoukosta käyttäessäsi talousraportointia. Tähän ongelmaan voi reagoida kahdella tavalla:

- Tarkista tietojen integroinnin tila menemällä Report Designerin kohtaan **Työkalut \> Integroinnin tila**. Jos integrointi on kesken, odota sen valmistumista. Yritä sen jälkeen uudelleen sitä, mitä teit saadessasi sanoman.
- Ota yhteyttä tukeen, jotta ongelma voidaan tunnistaa ja käsitellä. Järjestelmässä saattaa olla epäyhtenäisiä tietoja. Tuki-insinöörit auttavat palvelimella olevan ongelman tunnistamisessa ja etsivät erityiset tiedot, jotka saattavat vaatia päivittämistä.

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>Miten historiallisten vaihtokurssien muunnokset vaikuttavat raportin suorituskykyyn?

Historiallista korkoa käytetään tyypillisesti kertyneiden voittovarojen, omaisuuden, käyttöomaisuuden ja oman pääoman kanssa. Historiallinen kurssi saattaa olla pakollinen Yhdysvaltain tilinpäätösstandardeista vastaavan elimen (FASB) ohjeiden tai yleisesti hyväksyttyjen kirjanpitoperiaatteiden (GAAP) perusteella. Lisätietoja on kohdassa [Valuuttaominaisuudet taloushallinnon raportoinnissa](financial-reporting-currency-capability.md).

## <a name="how-many-types-of-currency-rate-are-there"></a>Kuinka monta valuuttakurssityyppiä on olemassa?

Tyyppejä on kolmenlaisia:

- **Nykyinen kurssi** – Tätä tyyppiä käytetään yleensä tasetileille. Se tunnetaan yleensä *avistakurssina* ja se voi olla kuukauden viimeisen päivän tai toisen ennalta määritetyn päivämäärän kurssi.
- **Keskimääräinen kurssi** – Tätä tyyppiä käytetään yleensä tuloslaskelmatilien (voitto/tappio) yhteydessä. Voit määrittää keskimääräisen koron joko yksinkertaiseksi tai painotetuksi keskiarvoksi.
- **Historiallinen korko** – Tätä tyyppiä käytetään tyypillisesti kertyneiden voittovarojen, omaisuuden, käyttöomaisuuden ja oman pääoman kanssa. Nämä tilit saattavat olla pakollisia FASB- tai GAAP-ohjeiden mukaan.

## <a name="how-does-historical-currency-translation-work"></a>Miten valuutan historiallinen muunnos toimii?

Hinnat määräytyvät tapahtumapäivämäärän mukaan. Näin ollen jokainen tapahtuma muunnetaan yksitellen lähimpään vaihtokurssiin perustuen.

Historiallisen valuuttamuunnon yhteydessä voidaan käyttää ennalta laskettuja kauden saldoja yksittäisten tapahtumatietojen asemesta. Tämä toiminta poikkeaa nykyisen kurssin muunnoskäytännöstä.

## <a name="how-does-historical-currency-translation-affect-performance"></a>Miten valuutan historiallinen muunnos vaikuttaa suorituskykyyn?

Kun raporteissa esitetyt tiedot päivitetään, saattaa esiintyä viivettä, koska summat on laskettava uudelleen tarkistamalla tapahtumatiedot. Viive käynnistyy aina, kun hinnat päivitetään tai uusia tapahtumia kirjataan. Jos esimerkiksi tuhansia tilejä on määritetty historiallista muunnosta varten pari kertaa päivässä, raportin tietojen päivittäminen saattaa kestää jopa tunnin. Toisaalta, jos tiettyjä tilejä on vähemmän, raporttitietojen päivitysten käsittelyajat voidaan lyhentää minuutteihin tai alle minuutiksi.

Niin ikään silloin kun raportteja luodaan käyttämällä valuuttamuunnosta historiatyyppisille tileille, suoritetaan ylimääräisiä tapahtumakohtaisia laskelmia. Raporttien luontiaika voi tilien lukumäärän mukaan yli kaksinkertaistua.

## <a name="what-are-the-estimated-data-mart-integration-intervals"></a>Mitkä ovat arvioidut tietovaraston osajoukon integrointivälit?

Financial Reporter kopioi tiedot Dynamics 365 Financesta Financial Reporter ‑tietokantaan 16 tehtävän avulla. Seuraavassa taulukossa luetellaan nämä 16 tehtävää sekä aikavälit, jotka määrittävät, kuinka usein kukin tehtävä suoritetaan. Näitä aikavälejä ei voi muuttaa.

| Nimi                                                       | Aikaväli | Aikavälin ajoitus |
|------------------------------------------------------------|----------|-----------------|
| AX 2012 -tililuokista tililuokkaan            | 41       | minuuttia         |
| AX 2012 ‑tileistä tiliin                                | 7        | minuuttia         |
| AX 2012 ‑yrityksistä yritykseen                               | 300      | sekuntia         |
| AX 2012 ‑yrityksistä organisaatioon                          | 23       | minuuttia         |
| AX 2012 ‑dimensioyhdistelmistä dimensioyhdistelmään    | 1        | minuuttia         |
| AX 2012 ‑dimensioarvoista dimensioarvoon                | 11       | minuuttia         |
| AX 2012 -dimensioista dimensioon                            | 31       | minuuttia         |
| AX 2012 ‑vaihtokursseista vaihtokurssiin                    | 17       | minuuttia         |
| AX 2012 ‑tilikausista tilikauteen                        | 13       | minuuttia         |
| AX 2012 -kirjanpitotapahtumista tietoon                | 1        | minuuttia         |
| AX 2012 ‑organisaatiohierarkioista puurakenteeseen                   | 3 600    | sekuntia         |
| AX 2012 ‑skenaarioista skenaarioon                              | 29       | minuuttia         |
| AX 2012 ‑tapahtumatyypin tarkenteista tietotyypin tarkenteeseen | 19       | minuuttia         |
| Ylläpitotehtävä                                           | 1        | minuuttia         |
| MR-raportin määrityksistä AX7-talousraportteihin             | 45       | sekuntia         |
| MR-raportin versioista AX-talousraportin versioihin         | 45       | sekuntia         |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
