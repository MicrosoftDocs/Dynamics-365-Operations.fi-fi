---
title: Sisällönsijoittelumoduuli
description: Tässä ohjeaiheessa on tietoja sisällönsijoittelu- ja sisällönsijoittelunimikemoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
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
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785297"
---
# <a name="content-placement-module"></a>Sisällönsijoittelumoduuli

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja sisällönsijoittelu- ja sisällönsijoittelunimikemoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Sisällönsijoittelumoduuli on esikoissäilö, jonka muut moduulit voivat sijoittaa tietyn asettelun sisälle. Sisällönsijoittelumoduulit tukevat seuraavia moduulityyppejä alimoduuleina: sisällönsijoittelunimike, tilin tervetulonimike, tilin tilausnimike, tilin toivomuslistanimike ja tilin profiilinimike.

Sisällönsijoittelumoduulit saavat tietoja alimoduuleista, joita ne tukevat. Siksi sisällönsijoittelumoduuleja voidaan käyttää eri tavoin siihen lisättyjen moduulien perusteella.

Sisällönsijoittelunimikemoduulit käyttävät sekä kuvia että tekstiä kampanjoiden, käytäntöjen ja tuoteominaisuuksien esittelyssä. Esimerkiksi sisällönsijoittelunimikemoduulia voi käyttää aloitussivulla myymälän käytäntöjen ja toimitustietojen näyttämisessä. Sisällönsijoittelunimikemoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Ne voidaan sijoittaa mille tahansa sivulle. Niitä voidaan kuitenkin käyttää vain sisällönsijoittelumoduulin sisällä.

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin sisällönsijoittelumoduuleista

* Sisällönsijoittelumoduuleja, jotka sisältävät sisällönsijoittelunimikemoduuleja, voidaan käyttää aloitussivulla tai markkinointisivuilla, kun kuvien että tekstin avulla halutaan esitellä tuotteen toimintoja, kampanjoita, myymälän käytäntöjä, toimitustietoja ja muita tietoja.
* Sisällönsijoittelumoduuleja, jotka sisältävät sisällönsijoittelunimikemoduuleja, voidaan käyttää tuotetietosivuilla tuoteominaisuuksien esittelyssä.
* Sisällönsijoittelumoduuleja, jotka sisältävät tilin tervetulonimike- tai tilin tilausnimikemoduulin, voidaan käyttää tilinhallintasivuilla.

## <a name="content-placement-module-properties"></a>Sisällönsijoittelumoduulin ominaisuudet

| Ominaisuuden nimi | Arvo | Kuvaus |
|---------------|-------|-------------|
| Leveys         | **Sisällytä säilöön** tai **Täytä näyttö** | Jos arvoksi on määritetty **Sisällytä säilöön**, sisällönsijoittelumoduulin sisällä olevat nimikkeet ovat korkeintaan sisällönsijoittelumoduulin levyisiä. Jos arvoksi on määritetty **Täytä näyttö**, sisällönsijoittelumoduulin leveys ei rajoita leveyttä, vaan nimikkeet voivat olla koko näytön levyisiä. |

## <a name="content-placement-item-module-properties"></a>Sisällönsijoittelunimikemoduulin ominaisuudet

| Ominaisuuden nimi | Arvo | Kuvaus |
|---------------|-------|-------------|
| Otsikko       | Otsikkoteksti ja -tunnukset (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Jokaisella sisällönsijoittelunnimikemoduulilla voi olla otsikko. **Otsikko**-ominaisuus tukee otsikkotunnuksia. Oletusarvoisesti käytetään **H2**-otsikkotunnusta. Otsikkotunnuksen voi kuitenkin muuttaa tarvittaessa, jotta se täyttää helppokäyttötoimintojen vaatimukset. |
| Kappale     | Kappaleen teksti | Sisällönsijoittelunimikemoduulit tukevat kappaleen tekstiä RTF-muodossa. Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus, kursiivi ja hyperlinkit. Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista. |
| Kuva         | Kuvatiedosto | Kuvaan voi liittää tekstiä. |
| Linkitä          | Linkin URL-osoite ja linkin teksti | Tekstiin voidaan lisätä linkki, jonka avulla käyttäjät ohjataan tietylle sivulle. |
| Ruudun koko     | Numero väliltä **1**–**12** | Tämä ominaisuus määrittää kunkin sisällönsijoittelunimikkeen niiden paikkojen määrän, jotka nimikkeen tulee täyttää sisällönsijoittelumoduulissa. Sisällönsijoittelumoduulin enimmäiskoko on 12 paikkaa. Jos sisällönsijoittelumoduulin ensimmäisten *n* -nimikkeen ruutujen kokonaiskoko on yli 12 paikkaa, nimikkeet rivitetään seuraavalle riville. |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>Sisällönsijoittelunimikemoduulin sisältävän sisällönsijoittelumoduulin lisääminen sivulle

Voit lisätä uudelle sivulle sisällönsijoittelumoduulin, joka sisältää sisällönsijoittelunimikemoduulin, ja määrittää vaaditut ominaisuudet seuraavasti.

1. Luo malli, jonka nimi on **Sisällönsijoittelumalli**.
1. Lisää sisällönsijoittelumoduuli oletussivun **pääpaikkaan**.
1. Lisää sisällönsijoittelumoduulissa sisällönsijoittelunimikemoduuli.
1. Kirjaa malli sisään ja julkaise se.
1. Käytä juuri luotua sisällönsijoittelumallia, kun haluat luoda sivun nimeltä **Sisällönsijoittelusivu**.
1. Lisää sisällönsijoittelumoduuli uuden sivun **pääpaikkaan**.
1. Lisää sisällönsijoittelumoduulissa sisällönsijoittelunimikemoduuli.
1. Valitse sisällönsijoittelunimikemoduulin ominaisuusruudussa kuva ja lisää otsikko, kappale sekä linkki. Määritä linkin URL-osoite ja määritä ruudun kooksi **6**.
1. Toista vaiheet 7 ja 8 ja lisää toinen sisällönsijoittelunimikemoduuli, jolla on sama ruudun koko.
1. Tallenna ja esikatsele sivu. Näkyviin pitäisi tulla kaksi sisällönsijoittelunimikettä vierekkäin. Voit muokata kunkin sisällönsijoittelunimikemoduulin **Ruudun koko** -ominaisuutta tai lisätä moduuleja, jotta saat haluamasi asettelun.
1. Kirjaa sivu sisään ja julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Hälytysmoduuli](add-alert.md)

[Karusellimoduuli](add-carousel.md)

[Sisällöntäyteinen lohkomoduuli](add-content-rich-block.md)

[Omaisuusmoduuli](add-feature-module.md)

[Hero-moduuli](add-hero-module.md)

[Videotoistinmoduuli](add-video-player.md)
