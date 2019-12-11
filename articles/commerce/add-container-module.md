---
title: Konttimoduuli
description: Tässä ohjeaiheessa on tietoja säilömoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 22a09b61fbe3bd1cca96011d3fb81a12ef1bc844
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697057"
---
# <a name="container-module"></a>Konttimoduuli

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja säilömoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Säilömoduuli on moduuli, joka isännöi muita moduuleja. Se on yleisin säilö, jota käytetään Dynamics 365 Commercessa. Säilömoduulin ensisijainen tarkoitus on määrittää sen sisässä olevien moduulien asettelu sille määritettyjen ominaisuuksien avulla. Nämä moduulit voivat olla rinnakkain esimerkiksi kahden, kolmen, neljän tai kuuden sarakkeen asettelussa. Ne voivat olla säilön levyisiä tai täyttää koko näytön. Jokaiseen säilömoduuliin voidaan lisätä otsikko.

Konttimoduuleja on kolme vakiotyyppiä: säilö, säilö jossa on 2 paikkaa ja säilö jossa on 3 paikkaa. Näihin säilöihin voi sijoittaa minkä tyyppisiä moduuleja tahansa. Olemassa on myös erityisiä säilömoduulityyppejä, kuten karuselli, sisällöntäyteinen lohko, sisällönsijoittelu, ostoskori, kassa, ostoruutu, ylätunniste ja alatunniste. Näillä säilöillä on erityiset tarkoitukset, ja niiden sisään voi asettaa vain tietyn tyyppisiä tuettuja moduuleja.

On suositeltavaa sijoittaa moduulit säilön sisälle. Tällöin niiden leveydeksi voidaan määrittää säilön leveys.

## <a name="examples-of-container-modules-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin säilömoduuleista

- Sivuston tekijä haluaa kolmen sarakkeen asettelun, jossa näytetään kolme moduulia rinnakkain. Tämän vuoksi sivuston tekijä käyttää säilömoduulia, jossa on 3 paikkaa.
- Sivuston tekijä haluaa kuuden sarakkeen asettelun, jossa näytetään kuusi moduulia rinnakkain. Tämän vuoksi sivuston tekijä käyttää säilöä, joka sisältää kuusi saraketta.
- Sivuston tekijä haluaa asettaa moduulin sivulle, mutta ei halua täyttää näyttöä. Tämän vuoksi sivuston tekijä lisää moduulin säilömoduuliin ja määrittää säilön **Leveys**-ominaisuudeksi **Sisällytä säilöön**.

## <a name="container-module-properties"></a>Säilömoduulin ominaisuudet

| Ominaisuuden nimi     | Arvot | Kuvaus |
|-------------------|--------|-------------|
| Otsikko           | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Säilöö varten voidaan antaa valinnainen otsikko. Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta. Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät. |
| Leveys             | **Sisällytä säilöön** tai **Täytä näyttö** | Jos arvoksi on määritetty **Sisällytä säilöön** (oletusarvo), säilön sisällä olevat moduulit ovat korkeintaan säilön levyisiä. Jos arvo on määritetty **Täytä näyttö**, säilö ei rajoita moduulien kokoa, vaan ne voivat täyttää näytön. |
| Sarakkeiden määrä | **1**, **2**, **3**, **4**, **6** tai **12** | Tämä ominaisuus määrittää säilön sarakkeiden määrän. Kontissa voi olla korkeintaan 12 saraketta. |

## <a name="container-with-2-slots"></a>Säiliö, jossa on 2 paikkaa

Kontti, jossa on kaksi paikkaa, on optimoitu kaksi saraketta sisältävälle asettelulle. Tämän tyyppisessä säilössä on kaksi paikkaa. Tämä mahdollistaa sisällä olevien moduulien rinnakkaisen näkymän.

Lisäominaisuuksia voi käyttää asettelun optimoimiseksi eri näkymäportteja (esimerkiksi mobiililaitteita, tabletteja ja tietokoneita) varten. Jokaiselle näkymäportille voidaan määrittää kunkin sarakkeen leveys. Seuraavat sarakkeen leveysasetukset ovat käytettävissä:

- **75 % / 25 %** – Ensimmäisen moduulin sarakkeen leveys on 75 prosenttia ja toisen moduulin sarakkeen leveys 25 prosenttia. Käytettävissä on myös **25 % / 75 %** -vaihtoehto.
- **50 % / 50 %** – Molempien moduulien sarakkeiden leveydet ovat samat.
- **67 % / 33 %** – Ensimmäisen moduulin sarakkeen leveys on 67 prosenttia ja toisen moduulin sarakkeen leveys 33 prosenttia. Käytettävissä on myös **33 % / 67 %** -vaihtoehto.
- **100 %** – Kummankin moduulin sarakeleveys on maksimi. Tämän vuoksi moduulit pinotaan pystysuunnassa yhteen sarakkeeseen. Vaikka tämä yhden sarakkeen asettelu on ristiriidassa kaksipaikkaisen säilötyypin kanssa, se voi olla paras vaihtoehto joissakin näkymäporteissa (esimerkiksi erittäin pienissä näkymäporteissa, kuten mobiililaitteissa).

### <a name="container-with-2-slots-properties"></a>Kontti, jossa on kahden paikan ominaisuudet

| Ominaisuuden nimi                   | Arvot | Kuvaus |
|---------------------------------|--------|-------------|
| Otsikko                         | Otsikkoteksti ja -tunnus | Konttia varten voidaan antaa valinnainen asetus. |
| Erittäin pienen näkymäportin määritys | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** tai **100 %** | Tämä ominaisuus määrittää erityisen pienten näkymäporttien asettelun. |
| Pienen näkymäportin määritys   | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** tai **100 %** | Tämä ominaisuus määrittää pienten näkymäporttien, kuten mobiililaitteiden, asettelun. |
| Keskikokoisen näkymäportin määritys  | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** tai **100 %** | Tämä ominaisuus määrittää keskikokoisten näkymäporttien, kuten tablettien, asettelun. |
| Suuren näkymäportin määritys   | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** tai **100 %** | Tämä ominaisuus määrittää suurten näkymäporttien, kuten tietokoneiden, asettelun. |

## <a name="container-with-3-slots"></a>Säiliö, jossa on 3 paikkaa

Kontti, jonka moduuleissa on kolme paikkaa, on optimoitu kolme saraketta sisältävälle asettelulle.

Lisäominaisuuksien avulla voidaan optimoida eri näkymäporttien asettelu. Jokaiselle näkymäportille voidaan määrittää kunkin sarakkeen leveys. Seuraavat sarakkeen leveysasetukset ovat käytettävissä:

- **33 % / 33 % / 33 %** – Kaikkien kolmen moduulin sarakkeiden leveydet ovat samat.
- **50 % / 25 % / 25 %** – Ensimmäisen moduulin sarakkeen leveys on 50 prosenttia ja kahden muun moduulin sarakkeiden leveys on 25 prosenttia. **25 % / 50 % / 25 %**- ja **25 % / 25 % / 50 %** -vaihtoehdot ovat myös käytettävissä.
- **16 % / 16 % / 67 %** – Kahden ensimmäisen moduulin sarakkeiden leveys on 16 prosenttia ja kolmannen moduulin sarakkeen leveys on 67 prosenttia. **16 % / 67 % / 16 %**- ja **67 % / 16 % / 16 %** -vaihtoehdot ovat myös käytettävissä.

### <a name="container-with-3-slots-properties"></a>Kontti, jossa on kolmen paikan ominaisuudet

| Ominaisuuden nimi                   | Arvot | Kuvaus |
|---------------------------------|--------|-------------|
| Otsikko                         | Otsikkoteksti ja -tunnus | Konttia varten voidaan lisätä valinnainen otsikko. |
| Erittäin pienen näkymäportin määritys | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** tai **67 % / 16 % / 16 %** | Tämä ominaisuus määrittää erityisen pienten näkymäporttien asettelun. |
| Pienen näkymäportin määritys   | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** tai **67 % / 16 % / 16 %** | Tämä ominaisuus määrittää pienten näkymäporttien, kuten mobiililaitteiden, asettelun. |
| Keskikokoisen näkymäportin määritys  | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** tai **67 % / 16 % / 16 %** | Tämä ominaisuus määrittää keskikokoisten näkymäporttien, kuten tablettien, asettelun. |
| Suuren näkymäportin määritys   | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** tai **67 % / 16 % / 16 %** | Tämä ominaisuus määrittää suurten näkymäporttien, kuten tietokoneiden, asettelun. |

## <a name="add-a-container-module-to-a-page"></a>Konttimoduulin lisääminen sivulle

Voit lisätä säilön toistinmoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo sivumalli, jonka nimi on **Konttimalli**.
1. Lisää säilömoduuli oletussivun **pääpaikkaan**.
1. Lisää säilömoduulissa ominaisuusmoduuli.
1. Kirjaa malli sisään ja julkaise se.
1. Käytä juuri luotua säilömallia, kun haluat luoda sivun nimeltä **Kontin sivu**.
1. Lisää säilömoduuli uuden sivun **pääpaikkaan**.
1. Määritä säilömoduulin ominaisuusruudussa **Sarakkeiden määrä** -ominaisuuden arvoksi **1** ja **Leveys**-ominaisuuden arvoksi **Sisällytä säilöön**.
1. Lisää säilömoduulissa ominaisuusmoduuli.
1. Määritä otsikko ominaisuusmoduulin ominaisuusruudussa.
1. Tallenna ja esikatsele sivu. Näkyvissä on yksi säilömoduulin levyinen ominaisuusmoduuli.
1. Muuta säilömoduulin ominaisuusruudussa **Sarakkeiden määrä** -ominaisuuden arvoksi **3**.
1. Lisää säilömoduuliin kaksi ominaisuusmoduulia.
1. Tallenna ja esikatsele sivu. Nyt näkyviin tulee kolme ominaisuusmoduulia, jotka näkyvät vierekkäin.
1. Kun asettelu on haluttu, kuittaa sivu sisään ja julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Karusellimoduuli](add-carousel.md)

[Sisällöntäyteinen lohkomoduuli](add-content-rich-block.md)

[Sisällönsijoittelumoduuli](add-content-placement-modules.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
