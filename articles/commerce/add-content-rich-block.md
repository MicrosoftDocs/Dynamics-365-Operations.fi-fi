---
title: Tekstilohkomoduuli
description: Tässä ohjeaiheessa on tietoja tekstilohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 20a2e0bc46e182172ccd96f556fd398e8bffc34b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347539"
---
# <a name="text-block-module"></a>Tekstilohkomoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja tekstilohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Tekstilohkomoduuli on moduuli, jolla lisätään tekstisisältöä. Tämä sisältö voi olla tiedottavaa sisältöä tai kampanjasisältöä.

Tekstilohkomoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle. Ne ovat itsenäisiä moduuleja, jotka eivät ole riippuvaisia sivun kontekstista tai muista moduuleista.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin tekstilohkomoduuleista

Tekstilohkomoduuleja voi käyttää seuraavasti:

* Tuotteiden ominaisuuksien esittely tuotetietosivulla
* Tiedoksi millä tahansa sivulla. Ne voivat esimerkiksi selittää kanta-asiakasohjelmien etuja, kuvailla toimitus- ja palautuskäytäntöjä, vastata usein kysyttyihin kysymyksiin ja kertoa yrityksestä.
* Voit lisätä mukautettuja sanomia tuotetietosivulle. (esimerkiksi Ilmainen tilaus uli 50 $ arvoisille tilauksille).
* Tuotetieto-, ostoskori-, kassa- ja muiden sivujen vastuuvapauslausekkeet ja yhteystiedot (esimerkiksi Myymälän käytännöt koskevat toimituksia ja palautuksia).

Seuraavassa kuvassa näkyy esimerkki tekstilohkomoduulista, jota käytetään kotisivulla.

![Esimerkki tekstilohkomoduulista.](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Tekstilohkomoduulin ominaisuudet

| Ominaisuuden nimi     | Arvo                                            | kuvaus |
|-------------------|--------------------------------------------------|-------------|
| Muotoiltu teksti         | Muotoiltu teksti                                        | Kappaleen teksti. Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus ja kursiivi. |
| Mukautetun luokan nimi | CSS-tyylisivujen luokan nimi        | Mukautetun CSS-luokan nimi, jonka kehittäjä antaa moduulin muotoiluun. Luokan nimi on määritettävä teemapaketissa. |
| Fontin koko         | **Pieni**, **Keskisuuri**, **Suuri** tai **Erittäin suuri** | Sisällön fontin koko. |

## <a name="add-a-text-block-module-to-a-page"></a>Tekstilohkomoduulin lisääminen sivulle

Voit lisätä tekstilohkomoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Sisältömalli**.
1. Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa **Sisältömalli**. Kirjoita **Sivun nimi** -kohtaan **Sisältösivu** ja valitse sitten **OK**.
1. Valitse uudella sivulla **Pää**-paikka. Valitse kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Määritä säilömoduulin ominaisuusruudun **Leveys**-ominaisuudeksi **Täytä säilö**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Tekstilohko**-moduuli ja valitse sitten **OK**. 
1. Lisää tekstiä tekstilohkomoduulin ominaisuusruudun **RTF**-kenttään.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Promopalkkimoduuli](add-alert.md)

[Karusellimoduuli](add-carousel.md)

[Sisältölohkomoduuli](add-hero-module.md)

[Videotoistinmoduuli](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]