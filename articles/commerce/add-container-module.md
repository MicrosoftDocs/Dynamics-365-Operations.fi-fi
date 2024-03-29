---
title: Konttimoduuli
description: Tässä artikkelissa on tietoja säilömoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 58fa222dfef9e559da00fef448c572800651bd63
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272904"
---
# <a name="container-module"></a>Konttimoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja säilömoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Säilömoduuli on moduuli, joka isännöi muita moduuleja. Säilömoduulin ensisijainen tarkoitus on määrittää sen sisässä olevien moduulien asettelu sille määritettyjen ominaisuuksien avulla. Nämä moduulit voivat olla rinnakkain esimerkiksi kahden, kolmen, neljän tai kuuden sarakkeen asettelussa. Ne voivat olla säilön levyisiä tai täyttää koko näytön. Jokaiseen säilömoduuliin voidaan lisätä otsikko.

Tuettuja säilömoduuleja on kolme:: säilö, säilö jossa on 2 paikkaa ja säilö jossa on 3 paikkaa. Näihin säilöihin voi sijoittaa kaikenlaisia moduuleja. 

> [!NOTE] 
> Moduulit kannattaa aina sijoittaa säilömoduulin sisällä, sillä silloin niiden leveydeksi voidaan määrittää säilön leveys.

## <a name="examples-of-container-modules-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin säilömoduuleista

- Sivuston tekijä haluaa kolmen sarakkeen asettelun, jossa näytetään kolme moduulia rinnakkain. Tämän vuoksi sivuston tekijä käyttää säilömoduulia, jossa on 3 paikkaa.
- Sivuston tekijä haluaa kuuden sarakkeen asettelun, jossa näytetään kuusi moduulia rinnakkain. Tämän vuoksi sivuston tekijä käyttää säilöä, joka sisältää kuusi saraketta.
- Sivuston tekijä haluaa asettaa moduulin sivulle, mutta ei halua täyttää näyttöä. Tämän vuoksi sivuston tekijä lisää moduulin säilömoduuliin ja määrittää säilön **Leveys**-ominaisuudeksi **Sisällytä säilöön**.

Seuraavassa kuvassa näkyy esimerkki säilömoduulista, joka sisältää karusellimoduulin Commercen sivustonluontityökalussa. Tässä esimerkissä konttimoduulin **Leveys**-ominaisuuden arvoksi on asetettu **Täytä näyttö**.

![Esimerkki konttimoduulista.](./media/ecommerce-container.PNG)

## <a name="container-module-properties"></a>Säilömoduulin ominaisuudet

| Ominaisuuden nimi     | Arvot | kuvaus |
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

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Konttimalli** ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**. 
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Syötä **Luo uusi sivu** -dialogiruudussa, kohdan **Sivun nimi** alla, **Konttisivu** ja valitse sitten **Seuraava**.
1. Valitse **Valitse malli** -kohdassa luomasi **Konttimalli** ja valitse sitten **Seuraava**.
1. Valitse **Valitse asettelu** -kohdassa sivun asettelu (esimerkiksi **Joustava asettelu**) ja valitse sitten **Seuraava**.
1. Tarkista sivun konfigurointi kohdassa **Tarkista ja viimeistele**. Jos haluat muokata sivun tietoja, valitse **Takaisin**. Jos sivun tiedot ovat oikein, valitse **Luo sivu**. 
1. Valitse uudella sivulla **Pää**-paikka. Valitse kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Määritä säilömoduulin ominaisuusruudussa **Sarakkeiden määrä** -ominaisuuden arvoksi **1** ja **Leveys**-ominaisuuden arvoksi **Täytä säiliö**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Sisältölohko**-moduuli ja valitse sitten **OK**.
1. Määritä sisältölohkomoduulin ominaisuusruudussa otsikko, kuva ja asettelu.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Näkyvissä on yksi säilömoduulin levyinen ominaisuusmoduuli.
1. Muuta säilömoduulin ominaisuusruudussa **Sarakkeiden määrä** -ominaisuuden arvoksi **3**.
1. Lisää konttimoduuliin kaksi muuta sisällönestomoduulia ja määritä ne.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Nyt näkyviin tulee kolme sisältölohkomoduulia, jotka näkyvät vierekkäin.
1. Kun olet saavuttanut haluamasi asettelun, valitse **Viimeistele muokkaus** tarkistaaksesi sivun ja julkaise se valitsemalla **Julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Haitarivalikkomoduuli](add-accordion.md)

[Välilehtimoduuli](add-tab.md)

[Karusellimoduuli](add-carousel.md)

[Tekstilohkomoduuli](add-content-rich-block.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
