---
title: Hero-moduuli
description: Tässä ohjeaiheessa on tietoja hero-moduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785385"
---
# <a name="hero-module"></a>Hero-moduuli

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja hero-moduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Hero-moduulia käytetään tuotteiden tai kampanjoiden markkinoinnissa kuvien ja tekstin yhdistelmän avulla. Jälleenmyyjä voi lisätä hero-moduulin esimerkiksi sähköisen kaupankäynnin sivuston aloitussivulle ja mainostaa uutta tuotetta sekä houkutella asiakkaita.

Hero-moduulia ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Se on itsenäinen moduuli, joka ei ole riippuvainen sivun muista moduuleista. Hero-moduuli voidaan sijoittaa mille tahansa sivuston sivulle, jossa jälleenmyyjä haluaa markkinoida tai mainostaa jotakin (esimerkiksi tuotteita, myyntiä tai ominaisuuksia).

## <a name="examples-of-hero-module-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin hero-moduulista

- Hero-moduulia voidaan käyttää sähköisen kaupankäynnin sivuston aloitussivulla kampanjoiden ja uusien tuotteiden esittelyssä.
- Hero-moduulia voi käyttää tuotetietosivulla tuotetietojen esittelyssä.
- Karusellimoduulin sisään voi asettaa useita hero-moduuleita. Näin voidaan esitellä useita tuotteita tai kampanjoita.

## <a name="hero-module-properties"></a>Hero-moduulin ominaisuudet

| Ominaisuuden nimi  | Arvot | Kuvaus |
|----------------|--------|-------------|
| Kuva          | Kuvatiedosto | Kuvan avulla voidaan esitellä tuotetta tai kampanjaa. Kuvan voi ladata kuvavalikoimaan. Myös olemassa olevaa kuvaa voi käyttää. |
| Otsikko        | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Jokaisella hero-moduulilla voi olla otsikko. Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta. Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät. |
| Kappale      | Kappaleen teksti | Hero-moduulit tukevat kappaleen tekstiä RTF-muodossa. Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus, kursiivi ja hyperlinkit. Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista. |
| Linkitä           | Linkin teksti, URL-osoite, ARIA (Accessible Rich Internet Applications) -otsikko ja **Avaa linkki uudessa välilehdessä** | Hero-moduulit tukevat vähintään yhtä toimintokutsulinkkiä. Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia. ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia. Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen. |
| Tekstin sijoittelu | **Ylhäällä vasemmalla**, **ylhäällä oikealla**, **ylhäällä keskellä**, **alhaalla vasemmalla**, **alhaalla oikealla**, **alhaalla keskellä**, **keskellä vasemmalla**, **keskellä oikealla** tai **keskellä keskellä** | Tämä ominaisuus määrittää kuvan sijainnin suhteessa tekstiin. Jos valittuna on esimerkiksi **oikea**, kuva näkyy tekstin oikealla puolella. |
| Tekstin teema     | **Vaalea** tai **tumma** | Tekstille voi määrittää väriteeman taustakuvan perusteella. Jos kuvalla on esimerkiksi tumma tausta, voidaan käyttää vaaleampaa teemaa. Näin teksti näkyy paremmin ja helppokäyttötoimintojen värikontrastisuhde otetaan huomioon. |
| Liukuväri       | **Tosi** vai **Epätosi** | Kuvassa voidaan käyttää liukuväriä, jotta helppokäyttötoimintojen kontrastisuhteet otetaan huomioon. |

## <a name="add-a-hero-module-to-a-new-page"></a>Hero-moduulin lisääminen uudelle sivulle

Voit lisätä hero-moduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Mallit**ja luo sivumalli, jonka nimi on **Hero-malli**.
1. Lisää hero-moduuli oletussivun **pääpaikkaan**.
1. Kirjaa malli sisään ja julkaise se.
1. Käytä juuri luotua hero-mallia, kun haluat luoda sivun nimeltä **Hero-sivu**.
1. Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunan **Valitse moduulit** -kohdassa hero-moduuli ja valitse sitten **OK**.
1. Valitse vasemmanpuoleisen jäsennyspuun hero-moduuli.
1. Valitse oikeanpuoleisessa ominaisuusruudussa **Lisää kuva**. Valitse joko olemassa oleva kuva tai lataa uusi kuva.
1. Valitse **Otsikko**.
1. Lisää **Otsikko**-valintaikkunaan otsikon teksti. Valitse otsikkotaso ja valitse sitten **OK**.
1. Lisää **Rich Text** -kohtaan haluamasi teksti.
1. Valitse **Lisää toimintolinkki**.
1. Lisää **Toimintolinkki**-valintaikkunaan linkin teksti, linkin URL-osoite ja linkin ARIA-otsikko. Valitse sitten **OK**.
1. Tallenna sivu ja esikatsele muutokset.
1. Kirjaa sivu sisään ja julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Hälytysmoduuli](add-alert.md)

[Karusellimoduuli](add-carousel.md)

[Sisällöntäyteinen lohkomoduuli](add-content-rich-block.md)

[Sisällönsijoittelumoduuli](add-content-placement-modules.md)

[Omaisuusmoduuli](add-feature-module.md)

[Videotoistinmoduuli](add-video-player.md)
