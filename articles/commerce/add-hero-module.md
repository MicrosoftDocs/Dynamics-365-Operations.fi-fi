---
title: Sisältölohkomoduuli
description: Tässä artikkelissa on tietoja sisältölohkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
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
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: dc6d728f49befd0c156340379dba05f592ca7919
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276997"
---
# <a name="content-block-module"></a>Sisältölohkomoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja sisältölohkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Sisältölohkomoduulia käytetään tuotteiden tai kampanjoiden markkinoinnissa yhdistämällä kuvia ja tekstiä. Jälleenmyyjä voi lisätä sisältölohkomoduulin esimerkiksi sähköisen kaupankäynnin sivuston aloitussivulle mainostamaan uutta tuotetta ja houkuttelemaan asiakkaita.

Sisällönhallintajärjestelmän (CMS) tiedot ohjaavat sisältölohkomoduulia. Se on itsenäinen moduuli, joka ei ole riippuvainen sivun muista moduuleista. Sisältölohkomoduuli voidaan sijoittaa mille tahansa sivuston sivulle, jossa jälleenmyyjä haluaa markkinoida tai mainostaa jotakin (esimerkiksi tuotteita, myyntiä tai ominaisuuksia).

## <a name="examples-of-content-block-module-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin sisältölohkomoduuleista

- Sisältölohkomoduulia voidaan käyttää sähköisen kaupankäynnin sivuston aloitussivulla kampanjoiden ja uusien tuotteiden esittelyssä.
- Sisältölohkomoduulia voi käyttää tuotetietosivulla tuotetietojen esittelyssä.
- Karusellimoduulin sisään voi asettaa useita sisältölohkomoduuleita, joilla voidaan esitellä useita tuotteita tai kampanjoita.

## <a name="content-block-modules-and-themes"></a>Sisältölohkomoduulit ja teemat

Sisältölohkomoduulit voivat tukea erilaisia teemaan perustuvia asetteluja ja tyylejä. Esimerkiksi Fabrikam-teema tukee kolmea sisältölohkomoduulin asetteluversiota: hero, ominaisuus ja ruutu. Hero-asettelu näyttää taustalla kuvan ja sen päällä tekstin. Ominaisuusasettelussa kuva ja teksti näytetään rinnakkain. Ruutuasettelu mahdollistaa useiden sisältölohkojen käytön ruutumuodossa.

Teema voi lisäksi tuoda esille kunkin asettelun erilaisia ominaisuuksia. Teeman kehittäjä voi muodostaa sisältölohkomoduulin avulla lisää asetteluja ja tyylejä.

Seuraavassa kuvassa on esimerkki hero-asettelua käyttävästä sisältölohkomoduulista.

![Esimerkki hero-moduulista.](./media/Hero.PNG)

Seuraavassa kuvassa on esimerkki ominaisuusasettelua käyttävästä sisältölohkomoduulista.

![Esimerkkejä ominaisuusmoduuleista.](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>Sisältölohkomoduulin ominaisuudet

| Ominaisuuden nimi  | Arvot | kuvaus |
|----------------|--------|-------------|
| Kuva          | Kuvatiedosto | Kuvan avulla voidaan esitellä tuotetta tai kampanjaa. Kuvan voi ladata kuvavalikoimaan. Myös olemassa olevaa kuvaa voi käyttää. |
| Otsikko        | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Jokaisella hero-moduulilla voi olla otsikko. Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta. Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät. |
| Kappale      | Kappaleen teksti | Hero-moduulit tukevat kappaleen tekstiä RTF-muodossa. Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus, kursiivi ja hyperlinkit. Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista. |
| Linkitä           | Linkin teksti, URL-osoite, ARIA (Accessible Rich Internet Applications) -otsikko ja **Avaa linkki uudessa välilehdessä** | Hero-moduulit tukevat vähintään yhtä toimintokutsulinkkiä. Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia. ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia. Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen. |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Fabrikam-teeman näyttämät sisältölohkomoduulin ominaisuudet 

| Ominaisuuden nimi  | Arvot | Kuvaus |
|----------------|--------|-------------|
| Tekstin sijoittelu | **Vasen**, **Oikea**, **Keskitys** | Tämä ominaisuus määrittää kuvan päällä olevan tekstin sijainnin. Se koskee vain hero-asettelua. |
| Tekstin teema     | **Vaalea** tai **tumma** | Tekstille voi määrittää väriteeman taustakuvan perusteella. Jos kuvalla on esimerkiksi tumma tausta, voidaan käyttää vaaleampaa teemaa. Näin teksti näkyy paremmin ja helppokäyttötoimintojen värikontrastisuhde otetaan huomioon. Se koskee vain hero-asettelua.|
| Kuvan sijoittelu       | **Vasen**, **Oikea** | Tämä ominaisuus määrittää, onko kuvan oltava tekstin vasemmalla vai oikealla puolella. Se koskee vain ominaisuusasettelua.  |

## <a name="add-a-content-block-module-to-a-new-page"></a>Sisältölohkomoduulin lisääminen uudelle sivulle

Voit lisätä hero-moduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Valitse **Mallit** ja luo sivumalli, jonka nimi on **Sisältölohkomalli**.
1. Lisää hero-moduuli oletussivun **pääpaikkaan**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Luo **Sisältölohkosivu**-niminen sivu käyttämällä juuri luotua hero-mallia.
1. Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa hero-moduuli ja valitse sitten **OK**.
1. Valitse vasemmanpuoleisen jäsennyspuun sisältölohkomoduuli.
1. Valitse oikeanpuoleisessa ominaisuusruudussa **Lisää kuva**. Valitse joko olemassa oleva kuva tai lataa uusi kuva.
1. Valitse **Otsikko**.
1. Lisää **Otsikko**-valintaikkunaan otsikon teksti. Valitse otsikkotaso ja valitse sitten **OK**.
1. Lisää **Rich Text** -kohtaan haluamasi teksti.
1. Valitse **Lisää linkki**.
1. Lisää **Linkki**-valintaikkunaan linkin teksti, linkin URL-osoite ja linkin ARIA-otsikko. Valitse sitten **OK**.
1. Valitse **Hero**-asettelu.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen. 

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Promopalkkimoduuli](add-alert.md)

[Karusellimoduuli](add-carousel.md)

[Tekstilohkomoduuli](add-content-rich-block.md)

[Videotoistinmoduuli](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
