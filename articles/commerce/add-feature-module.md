---
title: Omaisuusmoduuli
description: Tässä ohjeaiheessa on tietoja ominaisuusmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785280"
---
# <a name="feature-module"></a>Omaisuusmoduuli 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja ominaisuusmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Ominaisuusmoduulia käytetään tuotteiden tai kampanjoiden markkinoinnissa kuvien ja tekstin yhdistelmän avulla. Esimerkiksi jälleenmyyjä voi lisätä ominaisuusmoduulin tuotetietosivulle ja näin korostaa tuotteen ominaisuuksia.

Ominaisuusmoduulia ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Se on itsenäinen moduuli, joka ei ole riippuvainen sivun muista moduuleista. Ominaisuusmoduuli voidaan sijoittaa mille tahansa sivuston sivulle, jossa jälleenmyyjä haluaa markkinoida tai mainostaa jotakin (esimerkiksi tuotteita, myyntiä tai ominaisuuksia).

## <a name="examples-of-feature-modules-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin ominaisuusmoduuleista

Ominaisuusmoduulia voi käyttää seuraavilla sivuilla:

- Tuotetietosivu, jossa esitellään tuotteen ominaisuuksia
- Aloitussivu, jolla mainostetaan tuotteita
- Luokkasivu, jolla kerrotaan tuoteluokista

## <a name="feature-module-properties"></a>Ominaisuusmoduulin ominaisuudet

| Ominaisuuden nimi     | Arvot | Kuvaus |
|-------------------|--------|-------------|
| Kuva             | Kuvatiedosto | Kuvan avulla voidaan markkinoida tuotetta tai kampanjaa. Kuvan voi ladata kuvavalikoimaan. Myös olemassa olevaa kuvaa voi käyttää. |
| Otsikko           | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Jokaisella ominaisuusmoduulilla voi olla otsikko. Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta. Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät. |
| Kappale         | Kappaleen teksti | Ominaisuusmoduulit tukevat kappaleen tekstiä RTF-muodossa. Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus, kursiivi ja hyperlinkit. Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista. |
| Linkitä              | Linkin teksti, URL-osoite, ARIA (Accessible Rich Internet Applications) -otsikko ja **Avaa linkki uudessa välilehdessä** | Ominaisuusmoduulit tukevat vähintään yhtä toimintokutsulinkkiä. Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia. ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia. Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen. |
| Kuvan sijoittelu   | **Oikea**, **vasen**, **yläosa** tai **alaosa** | Tämä ominaisuus määrittää kuvan sijainnin suhteessa tekstiin. Jos valittuna on esimerkiksi **oikea**, kuva näkyy tekstin oikealla puolella. |
| Kuvasarakkeen koko | Arvo väliltä **1**–**12** | Tämä ominaisuus määrittää kuvan koon suhteessa tekstiin. Koko ilmaistaan sivulla olevien sarakkeiden määränä. Sivulla on 12 saraketta. Kuvan ja tekstin koko on sama oletusarvoisesti (kuusi saraketta kummallakin). Kokoa voi kuitenkin muuttaa tarvittaessa. |

## <a name="add-a-feature-module-to-a-new-page"></a>Ominaisuusmoduulin lisääminen uudelle sivulle 

Voit lisätä ominaisuusmoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Mallit**ja luo sivumalli, jonka nimi on **Ominaisuusmalli**.
1. Lisää ominaisuusmoduuli oletussivun **pääpaikkaan**.
1. Kirjaa malli sisään ja julkaise se.
1. Käytä juuri luotua ominaisuusmallia, kun haluat luoda sivun nimeltä **Ominaisuussivu**.
1. Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunan **Valitse moduulit** -kohdassa ominaisuusmoduuli ja valitse sitten **OK**.
1. Valitse vasemmanpuoleisen jäsennyspuun ominaisuusmoduuli.
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

[Hero-moduuli](add-hero-module.md)

[Videotoistinmoduuli](add-video-player.md)
