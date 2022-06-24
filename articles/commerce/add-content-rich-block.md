---
title: Tekstilohkomoduuli
description: Tässä artikkelissa on tietoja tekstilohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: 48714f172b12bbc10f1f682a9dec8be710748e6b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869221"
---
# <a name="text-block-module"></a>Tekstilohkomoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja tekstilohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

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
1. Valitse **Valitse moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Syötä **Luo uusi sivu** -dialogiruudussa, kohdan **Sivun nimi** alla, **Sisältösivu** ja valitse sitten **Seuraava**.
1. Valitse **Valitse malli** -kohdan alla **Sisältömalli** ja valitse sitten **Seuraava**.
1. Valitse **Valitse asettelu** -kohdassa sivun asettelu (esimerkiksi **Joustava asettelu**) ja valitse sitten **Seuraava**.
1. Tarkista sivun konfigurointi kohdassa **Tarkista ja viimeistele**. Jos haluat muokata sivun tietoja, valitse **Takaisin**. Jos sivun tiedot ovat oikein, valitse **Luo sivu**. 
1. Valitse uudella sivulla **Pää**-paikka. Valitse kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Määritä säilömoduulin ominaisuusruudun **Leveys**-ominaisuudeksi **Täytä säilö**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Tekstilohko**-moduuli ja valitse sitten **OK**. 
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
