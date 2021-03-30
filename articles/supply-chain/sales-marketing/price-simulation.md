---
title: Hintasimulointi
description: Tässä artikkelissa on tietoja tarjousten hintasimuloinneista. Hintasimulointien avulla voidaan arvioida vähennysten vaikutusta tuleviin myyntihintoihin tarjousprosessin aikana, ennen kuin tietty hinta otetaan käyttöön.
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationPriceSimulation, SalesQuotationsTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8633d6eec788035997c52322c3268b946fb0bfe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218390"
---
# <a name="price-simulation"></a>Hintasimulointi

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja tarjousten hintasimuloinneista. Hintasimulointien avulla voidaan arvioida vähennysten vaikutusta tuleviin myyntihintoihin tarjousprosessin aikana, ennen kuin tietty hinta otetaan käyttöön.

Tarjouksen hintasimulointi näyttää ehdotettuun uuteen hintaan perustuvan uuden kokonaissumman. Hintasimulointi voi näyttää myös aiemmin luodussa tarjouksessa luodun tietyn rivin uuden hinnan. Voit antaa hintasimuloinnin ja käyttää sitä myöhemmin. Voit vaihtoehtoisesti käyttää alkuperäistä tarjousta, jossa ei ole hintasimulointia, ja tehdä muutoksia myyntiprosessin aikana asiakkaan kanssa.  

Hintasimulointi ei muuta tarjouksen hintaa. Jos hintasimulointia käytetään koko tarjouksessa, se käsitellään tarjouksen otsikossa erikoisalennuksena. Jos hintasimulointia käytetään tietyissä nimikkeissä, se käsitellään tarjouksen riveillä erikoisalennuksena. Tarjousriville luotu yksikön myyntihinta ei muutu, kun hintasimulaatiota käytetään. Sen sijaan tarjousrivin hinnanalennusta vastaava alennusprosentti kohdistetaan. Kun hintasimulointia on käytetty, yksikön myyntihinta ja alennusprosentti siirretään tarjousriville tai tarjouksen otsikkoon.  

>[Huomautus!] Kun suoritat hintasimuloinnin, vain nykyistä myyntivaluuttaa käytetään simuloinnin luontiin. Kuitenkin tarjouksen kokonaismäärien katselun yhteydessä näet perusvaluutan ja myyntivaluutan yhdistelmän.  

Tarjousriveille lisätyt lisänimikkeet voivat aiheuttaa rivialennukset tai monirivialennukset. Ne voivat aiheuttaa myös kokonaisalennuksia, jotka muuttavat tarjousrivien katetuottoja ja -prosentteja ja koko alennuksen.  

Voit myös suorittaa useita hintasimulointeja, jos haluat jäljittää hinnanoikaisujen vaikutukset tarjouksen tavoitteisiin. Näiden simulointien suorittaminen mahdollistaa tarjouksen kokonaishinnan tai tarjouksen tiettyjen rivien hinnan oikaisun. Sen jälkeen voit käyttää hintasimulointia, joka avulla kauppa voidaan tehdä.  

Voit määrittää hälytyksen, kun luot tarjouksen. Hälytyksiä voi käyttää esimerkiksi seuraavin tavoin:

-   Pysyt niiden avulla selvillä, missä tilassa tarjoukset ovat organisaatiossa.
-   Ne voivat aiheuttaa tietyn tarjouksen tarkistuksen tai ilmoittaa, milloin alennusrajat ylitetään.

## <a name="price-simulation-and-discounts"></a>Hintasimulointi ja alennukset
Jotta alennukset ja hinnat varmasti lasketaan oikein, alennuksia sisältävien tarjousten hintasimuloinnit on tehtävä erityisen huolellisesti. Koska kaikkia hintasimulointeja käsitellään aktiivisen tarjousrivin tai koko tarjouksen erityisalennuksina, alennusten eroja on seurattava.

### <a name="types-of-discounts-in-trade-agreements"></a>Kauppasopimusten alennustyypit

Supply Chain Managementin kauppasopimuksissa voi olla neljäntyyppisiä hinnanalennuksia. Nämä alennukset voidaan määrittää eri nimikkeille, asiakkaille tai hintaryhmille ja niitä voidaan rajoittaa päivämäärän mukaan. Laskuvirheiden välttämiseksi kauppasopimukset on otettava huomioon hintasimulointeja suoritettaessa. Kauppasopimusten neljä alennustyyppiä:

-   **Myyntihinta** – Nimikkeille voidaan määrittää eri myyntihinta. Kun tarjousrivit luodaan, ohjelma hakee nimikkeelle oikean hinnan ja siirtää sen tarjousriveille. Tämän vuoksi kauppasopimus, jossa on tällainen alennus, ei vaikuta hintasimulointiin. Tarjousrivillä käytettävä myyntihinta vastaa kauppasopimusta.
-   **Rivialennus** – Nimikkeille määritetään erikoisalennukset tilatun määrän mukaan. Rivialennus vähennetään tavallisesti rivisummista ennen hintasimuloinnin suorittamista. Tämän vuoksi kauppasopimus, jossa on tällainen alennus, vaikuttaa hintasimulointiin.
-   **Monirivialennus** – Jos yhdistetyt määrät ylittävät määrittämäsi rajan, tilattujen nimikkeiden ennalta määritetyt yhdistelmät aiheuttavat alennuksen koko tilaukseen. Rivialennus vähennetään tavallisesti rivisummista ennen hintasimuloinnin suorittamista. Tämän vuoksi kauppasopimus, jossa on tällainen alennus, vaikuttaa hintasimulointiin.
-   **Kokonaisalennus** – Jos yhdistetyt summat ylittävät määrittämäsi rajan, ennalta määrityt tilattujen nimikkeet aiheuttavat alennuksen koko tilaukseen. Tarjousrivit muodostavat kokonaisalennuksen. Koska kokonaisalennusta käytetään tarjouksen kokonaissumman alennuksena, se pienentää tarjouksen kokonaissummaa. Tämän vuoksi kauppasopimus, jossa on tällainen alennus, vaikuttaa hintasimulointiin.

### <a name="quotation-lines-and-trade-agreements"></a>Tarjousrivit ja kauppasopimukset

Kun luot tarjousriviä tai muokkaat sitä, rivialennukset lasketaan automaattisesti. Nimikkeen myyntihinta etsitään kauppasopimuksen perusteella.

## <a name="price-simulation-examples"></a>Esimerkkejä hintasimuloinnista
Seuraavissa esimerkeissä käytetään hintasimulointia tarjouksen otsikoihin ja yhden rivin nimikkeisiin.

### <a name="price-simulation-for-quotation-headers"></a>Tarjouksen otsikoiden hintasimulointi

Luot tarjouksen, jossa on seuraavat rivit:

-   10 yksikköä nimikettä BR-12 (kustannushinta/yksikkö 9,52 USD ja myyntihinta/yksikkö 15,32 USD).
-   12 yksikköä nimikettä BR-14 (kustannushinta/yksikkö 7,48 USD ja myyntihinta/yksikkö 13,75 USD).

Tarjousrivit näkyvät seuraavassa taulukossa.

|    &nbsp;                  | Laskenta                          | Tulos   |
|----------------------------|--------------------------------------|----------|
| Myyntimäärä             | 10 yksikköä + 12 yksikköä                  | 22 yksikköä |
| Myyntiarvo Yhdysvaltain dollareina         | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Kustannusarvo Yhdysvaltain dollareina          | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Katetuotto Yhdysvaltain dollareina | 318,20 – 184,96                      | 133,24   |
| Kateprosentti         | (\[318.20 - 184.96\] ÷ 318.20) × 100 | 41,87%   |

Suoritat hintasimuloinnin ja sovellat 15 prosentin kokonaisalennusta koko tarjoukseen tai tarjouksen otsikkoon. Seuraavassa taulukossa on esitetty tarjouksen uudet kokonaissummat hintasimuloinnin suorittamisen jälkeen.

|     &nbsp;                                           | Laskenta                               | Tulos   |
|------------------------------------------------------|-------------------------------------------|----------|
| Myyntimäärä                                       | 10 yksikköä + 12 yksikköä                       | 22 yksikköä |
| Vanha myyntiarvo Yhdysvaltain dollareina                               | (10 × 15,32) + (12 × 13,75)               | 318,20   |
| Vanha kustannusarvo Yhdysvaltain dollareina                                | (10 × 9,52) + (12 × 7,48)                 | 184,96   |
| Vanha katetuotto Yhdysvaltain dollareina                       | 318,20 – 184,96                           | 133,24   |
| Vanha kateprosentti                               | (\[318.20 - (10 × 9.52)\] ÷ 318.20) × 100 | 41,87%   |
| Hintasimulointi, 15 prosentin kokonaisalennus Yhdysvaltain dollareina | (15 × 318,2) ÷ 100                        | 47,73    |
| Uusi myyntiarvo Yhdysvaltain dollareina                               | 318,20 – 47,73                            | 270,47   |
| Uusi katetuotto Yhdysvaltain dollareina                       | 270,47 – 184,96                           | 85,51    |
| Uusi katetuottoprosentti                               | \[(270.47 - 184.96) ÷ 270.47\] × 100      | 31,61 %   |

### <a name="price-simulation-for-single-line-items"></a>Hintasimulointi yhden rivin nimikkeille

Luot tarjouksen, jossa on seuraavat rivit:

-   10 yksikköä nimikettä BR-12 (kustannushinta/yksikkö 9,52 USD ja myyntihinta/yksikkö 15,32 USD).
-   12 yksikköä nimikettä BR-14 (kustannushinta/yksikkö 7,48 USD ja myyntihinta/yksikkö 13,75 USD).

Tarjousrivit näkyvät seuraavassa taulukossa.

|      &nbsp;                          | Laskenta                          | Tulos   |
|--------------------------------------|--------------------------------------|----------|
| Myyntimäärä                       | 10 yksikköä + 12 yksikköä                  | 22 yksikköä |
| BR-12:n myyntiarvo Yhdysvaltain dollareina         | 10 × 15,32                           | 153,20   |
| BR-14:n myyntiarvo Yhdysvaltain dollareina         | 12 × 13,75                           | 165,00   |
| BR-12:n myyntiarvo Yhdysvaltain dollareina          | 10 × 9,52                            | 95,20    |
| BR-14:n myyntiarvo Yhdysvaltain dollareina          | 12 × 7,48                            | 89,76    |
| BR-12:n katetuotto Yhdysvaltain dollareina | 153,20 - 95,20                       | 58,00    |
| BR-14:n katetuotto Yhdysvaltain dollareina | 165,00 - 89,76                       | 75,24    |
| BR-12:n kateprosentti  | \[(153.20 - 95.20) ÷ 153.20\] × 100  | 37,86    |
| BR-14:n kateprosentti  | \[(165.00 - 89.76) ÷ 165.00\] × 100  | 45,60    |
| Kokonaismyyntiarvo Yhdysvaltain dollareina             | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Kokonaiskustannusarvo Yhdysvaltain dollareina              | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Kokonaiskatetuotto Yhdysvaltain dollareina     | 318,20 – 184,96                      | 133,24   |
| Kokonaiskateprosentti             | \[(318.20 - 184.96) ÷ 318.20\] × 100 | 41,87%   |

Suoritat hintasimuloinnin ja sovellat 10 prosentin kokonaisalennusta BR-12-yksikköihin. Seuraavassa taulukossa on esitetty tarjouksen uudet kokonaissummat, kun hintasimulointi on suoritettu yhdelle rivinimikkeelle.

|    &nbsp;                                         | Laskenta                             | Tulos   |
|---------------------------------------------------|-----------------------------------------|----------|
| Myyntimäärä                                    | 10 yksikköä + 12 yksikköä                     | 22 yksikköä |
| BR-12:n vanha myyntiarvo Yhdysvaltain dollareina                  | 10 × 15,32                              | 153,20   |
| Hintasimulointi 10 prosentin alennus BR-12-yksikölle | (10 × 153,2) ÷ 100                      | 15,32    |
| BR-12:n uusi myyntiarvo Yhdysvaltain dollareina                  | (10 × 15,32) – 15,32                    | 137,88   |
| BR-14:n myyntiarvo Yhdysvaltain dollareina                      | 12 × 13,75                              | 165,00   |
| BR-12:n myyntiarvo Yhdysvaltain dollareina                       | 10 × 9,52                               | 95,20    |
| BR-14:n myyntiarvo Yhdysvaltain dollareina                       | 12 × 7,48                               | 89,76    |
| BR-12:n uusi katetuotto Yhdysvaltain dollareina          | 137,88 - 95,20                          | 42,68    |
| BR-14:n katetuotto Yhdysvaltain dollareina              | 165,00 - 89,76                          | 75,24    |
| BR-12:n uusi kateprosentti           | \[(137.88 - 95.20) ÷ 137.88\] × 100     | 30,95    |
| BR-14:n kateprosentti               | \[(165.00 - 89.76) ÷ 165.00\] × 100     | 45,60    |
| Uusi kokonaismyyntiarvo Yhdysvaltain dollareina                      | \[(10 × 15.32) - 15.32\] + (12 × 13.75) | 302,88   |
| Kokonaiskustannusarvo Yhdysvaltain dollareina                           | (10 × 9,52) + (12 × 7,48)               | 184,96   |
| Uusi kokonaiskatetuotto Yhdysvaltain dollareina              | 302,88 – 184,96                         | 117,92   |
| Uusi kokonaiskateprosentti                      | \[(302.88 - 184.96) ÷ 302.88\] × 100    | 38,93 %   |

Hintasimulointi vaikuttaa vain siihen riviin, johon sitä käytetään, vähentämällä rivin kokonaissummaa.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]