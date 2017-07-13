---
title: "Viivakoodin muotojen määrittäminen"
description: "Tässä aiheessa kuvataan, miten määrität viivakoodin muodon merkit, viivakoodin muodot, ja miten viivakoodin muodot liitetään viivakoodeihin."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 958cac2e85ae7fa514f6f26cbb6178d8fdec9783
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017



---

# Viivakoodin muotojen määrittäminen
<a id="set-up-bar-code-masks" class="xliff"></a>

[!include[banner](includes/banner.md)]


Tässä aiheessa kuvataan, miten määrität viivakoodin muodon merkit, viivakoodin muodot, ja miten viivakoodin muodot liitetään viivakoodeihin.

Viivakoodin muodon merkkien määrittäminen
<a id="set-up-bar-code-mask-characters" class="xliff"></a>
-------------------------------

Viivakoodin muotoja käytetään viivakoodien luomiseen ja tunnistamaan myyntipisteeseen luettavat viivakoodit nopeasti. Muodot koostuvat merkeistä, jotka toimivat paikkamerkkeinä, jotka osoittavat muodon, jossa viivakoodit luodaan. Jotta voisit määrittää viivakoodin muodon, sinun on määritettävä viivakoodin muodon merkit. Mene kohtaan **Vähittäismyynti** &gt; **Varastonhallinta** &gt; **Viivakoodit ja etiketit** &gt; **Muodon merkit**. Luo viivakoodin muotomerkit painamalla **Uusi**-painiketta. Muotomerkit voidaan luoda ilmaisemaan seuraavia viivakooditietoja.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Kenttä**            | **Kuvaus**                                                                                                 |
| **Tuote**          | Tuotetunnuksen paikkamerkki                                                                                     |
| **Mikä tahansa luku**       | Määrittää viivakoodiin kovakoodattavan numeron.                                                  |
| **Tarkistusnumero**      | Ilmaisee, että viivakoodin muodon tyyppi käyttää tarkistusnumeroa, jolla varmistetaan viivakoodin oikeellisuus. |
| **Kokonumero**       | Ilmaisee koon viivakoodissa, joka on luotu koon sisältävälle tuotevariantille.                                 |
| **Värinumero**      | Ilmaisee värin viivakoodissa, joka on luotu värin sisältävälle tuotevariantille.                               |
| **Tyylinumero**      | Ilmaisee tyylin viivakoodissa, joka on luotu tyylin sisältävälle tuotevariantille.                             |
| **EAN-käyttöoikeuskoodi** | Paikkamerkki EAN-käyttöoikeuskoodia koskevalle käyttöoikeudelle.                                                       |
| **Hinta**            | Ilmaisee hinnan viivakoodeissa, johon on upotettu hinta.                                                                   |
| **Määrä**         | Ilmaisee määrän viivakoodeissa, joihin on upotettu määrä/satunnainen paino.                                                |
| **Työntekijä**         | Ilmaisee viivakoodin osan työntekijän tunnusnumerolle, jota käytetään myyntipisteeseen kirjautumisessa viivakoodilla.                                  |
| **Asiakas**         | Ilmaisee asiakastunnuksen osan.                                                                                  |
| **Tietomerkintä**       | *Ei vielä toteutettu.*                                                                                          |
| **Alennuskoodi**    | *Poistettu* Dynamics 365 for Retail kevään 2017 versiosta alkaen. Aiemmin: ilmaisee viivakoodissa alennuskoodin, jota voi käyttää alennuksen lisäämiseen myyntipisteellä.                                                                   |
| **Kuponkikoodi**      | Ilmaisee kuponkikoodin viivakoodille, joka lisää alennuksen vähittäismyyntitilaukseen. Tämä korvaa alennuskoodin.     |
| **Lahjakortti**        | Ilmaisee lahjakortin numeron, kun lahjakortti myönnetään tai sillä tehdään maksu.                                               |
| **Kanta-asiakaskortti**     | Lisää kanta-asiakkaan tapahtumaan; voidaan käyttää kanta-asiakaskortilla maksettaessa.                             |

## Määritä viivakoodin muodot
<a id="define-bar-code-masks" class="xliff"></a>
Kun viivakoodin muotomerkit on määritetty tarvittaville viivakoodin muodoille, siirry kohtaan **Vähittäismyynti** &gt; **Varastonhallinta** &gt; **Viivakoodit ja etiketit** &gt; **Viivakoodin muotoasetukset**. Tällä sivulla voit määrittää viivakoodin muodot, jotka käyttävät aiemmin määritettyjä merkkejä. Näitä viivakoodin muotoja käytetään viivakoodien luonnissa, ja ne helpottavat luettujen viivakoodien tunnistamista myyntipisteellä.

1.  Luo uusi viivakoodin muoto painamalla **Uusi**-painiketta.
2.  Syötä arvot **Muodon tunnus**- ja **Kuvaus**-kenttiin ja valitse viivakoodin muototyyppi **Tyyppi**-kentässä.
3.  Valitse **Yleinen**-osan **Vakioviivakoodi**-kenttään arvo ja määritä viivakoodin etuliite, jos sellaista edellytetään.
4.  Lisää **Viivakoodin muodon segmentti** -osaan viivakoodin muodon segmentit, joita käytetään luotavissa viivakoodeissa.

Voit esimerkiksi luoda viivakoodin muodon, jonka tunnus on "Tuote" seuraavasti:

1.  Luo uusi viivakoodin muoto ja valitse tyypiksi "Tuote".
2.  Valitse vakioviivakoodi, esimerkiksi "Koodi 39".
3.  Anna etuliite, jolla tunnistat viivakoodin helposti. Esimerkiksi "22".
4.  Lisää muodon segmentti. Valittuna on muodon segmentti "Tuote".
5.  Anna tuotesegmentille pituus, esimerkiksi "10". Pituuden tulisi vastata yleisesti liikkeessä käytettävän tuotetunnuksen pituutta. Muodon esikatselu näytetään **Yleinen**-osassa, kohdassa **Muoto**.

## Määritä viivakoodin muodot viivakoodeille
<a id="assign-bar-code-masks-to-bar-codes" class="xliff"></a>
Viivakoodien muodot on määritettävä viivakoodeille ennen, kuin niitä voi käyttää. Jatkaen edellistä esimerkkiä, voit määrittää viivakoodin muodon viivakoodille seuraavasti:

1.  Siirty kohtaan **Organisaation hallinta** &gt; **Asetukset** &gt; **Viivakoodit** Luo uusi viivakoodi valitsemalla **Uusi**.
2.  Anna **Viivakoodi**-, **asetus**- ja **Asetus**-kenttiin arvo.
3.  Valitse **Yleiset**-osan **Viivakoodin tyyppi** -kenttään "Koodi 39". Valitse **Muodon** **tunnus** -kenttään aiemmin luotu muoto, "Tuote".
4.  Syötä **Koko**-kenttään "12".
5.  Valitse **Tallenna**.

Viivakoodin muotoa voi nyt käyttää viivakoodien luomiseen tuotteille. Yllä olevat vaiheet ovat esimerkkejä siitä, kuinka tuotteille voi luoda viivakoodin muotoja, mutta ne kuvaavat myös, viivakoodin muotoja voi luoda mille tahansa muulle viivakoodin tyypille, joka on tuettu. Viivakoodin muodot, tyypit ja pituudet tulisi mukauttaa omaa käyttötarkoitusta ja -ympäristöäsi varten.




