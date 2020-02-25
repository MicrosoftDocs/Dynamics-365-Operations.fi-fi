---
title: Tekstilohkomoduuli
description: Tässä ohjeaiheessa on tietoja tekstilohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025594"
---
# <a name="text-block-module"></a>Tekstilohkomoduuli


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja tekstilohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Tekstilohkomoduuli on moduuli, jolla lisätään tekstisisältöä. Tämä sisältö voi olla tiedottavaa sisältöä tai kampanjasisältöä.

Tekstilohkomoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle. Ne ovat itsenäisiä moduuleja, jotka eivät ole riippuvaisia sivun kontekstista tai muista moduuleista.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin tekstilohkomoduuleista

Tekstilohkomoduuleja voi käyttää seuraavasti:

* Tuotteiden ominaisuuksien esittely tuotetietosivulla
* Tiedoksi millä tahansa sivulla. Ne voivat esimerkiksi selittää kanta-asiakasohjelmien etuja, kuvailla toimitus- ja palautuskäytäntöjä, vastata usein kysyttyihin kysymyksiin ja kertoa yrityksestä.
* Voit lisätä mukautettuja sanomia tuotetietosivulle. (esimerkiksi Ilmainen tilaus uli 50 $ arvoisille tilauksille).
* Tuotetieto-, ostoskori-, kassa- ja muiden sivujen vastuuvapauslausekkeet ja yhteystiedot (esimerkiksi Myymälän käytännöt koskevat toimituksia ja palautuksia).

## <a name="text-block-module-properties"></a>Tekstilohkomoduulin ominaisuudet

| Ominaisuuden nimi     | Value                                            | Kuvaus |
|-------------------|--------------------------------------------------|-------------|
| Muotoiltu teksti         | Muotoiltu teksti                                        | Kappaleen teksti. Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus ja kursiivi. |
| Mukautetun luokan nimi | CSS-tyylisivujen luokan nimi        | Mukautetun CSS-luokan nimi, jonka kehittäjä antaa moduulin muotoiluun. Luokan nimi on määritettävä teemapaketissa. |
| Fontin koko         | **Pieni**, **Keskisuuri**, **Suuri** tai **Erittäin suuri** | Sisällön fontin koko. |

## <a name="add-a-text-block-module-to-a-page"></a>Tekstilohkomoduulin lisääminen sivulle

Voit lisätä tekstilohkomoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo sivumalli, jonka nimi on **Sisältömalli**. 
1. Lisää **Teksti**-paikkaan **Oletussivu**-moduuli.
1. Kun mallin muokkaus on valmis, julkaise se.
1. Käytä juuri luotua sisältömallia, kun haluat luoda sivun nimeltä **Sisältösivu**.
1. Lisää säilömoduuli uuden sivun **pääpaikkaan**.
1. Määritä säilömoduulin ominaisuusruudun **Leveys**-ominaisuudeksi **Täytä säilö**.
1. Lisää tekstilohkomoduuli säilömoduuliin. 
1. Lisää tekstiä tekstilohkomoduulin ominaisuusruudun **RTF**-kenttään.
1. Kun sivun muokkaus on valmis, julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Kampanjabannerimoduuli](add-alert.md)

[Karusellimoduuli](add-carousel.md)

[Sisältölohkomoduuli](add-hero-module.md)

[Videotoistinmoduuli](add-video-player.md)

