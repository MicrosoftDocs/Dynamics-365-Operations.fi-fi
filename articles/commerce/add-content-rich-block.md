---
title: Sisällöntäyteinen lohkomoduuli
description: Tässä ohjeaiheessa on tietoja sisällöntäyteisistä lohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785418"
---
# <a name="content-rich-block-module"></a>Sisällöntäyteinen lohkomoduuli

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja sisällöntäyteisistä lohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Sisällöntäyteinen lohkomoduuli on erityinen säilö, jonka sisään voi asettaa yhden tai useita sisällöntäyteisiä lohkonimikkeitä. Sisällöntäyteisiä lohkomoduuleja käytetään sivun tekstisisällössä. Tämä sisältö voi olla joko tiedottavaa sisältöä tai kampanjasisältöä.

Sisällöntäyteisiä lohkomoduuleja ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Ne voidaan sijoittaa mille tahansa sivulle. Ne ovat itsenäisiä moduuleja, jotka eivät ole riippuvaisia sivun kontekstista tai muista moduuleista.

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin sisällöntäyteisistä lohkomoduuleista

Sisällöntäyteisiä lohkomoduuleja voi käyttää seuraavasti:

* Tuotteiden ominaisuuksien esittely tuotetietosivulla
* Tiedoksi millä tahansa sivulla. Ne voivat esimerkiksi selittää kanta-asiakasohjelmien etuja, kuvailla toimitus- ja palautuskäytäntöjä, vastata usein kysyttyihin kysymyksiin ja kertoa yrityksestä.
* Voit lisätä mukautettuja sanomia tuotetietosivulle. (esimerkiksi Ilmainen tilaus uli 50 $ arvoisille tilauksille).
* Tuotetieto-, ostoskori-, kassa- ja muiden sivujen vastuuvapauslausekkeet ja yhteystiedot (esimerkiksi Myymälän käytännöt koskevat toimituksia ja palautuksia).

## <a name="content-rich-block-module-properties"></a>Sisällöntäyteisen lohkomoduulin ominaisuudet

| Ominaisuuden nimi     | Arvo                                 | Ominaisuus |
|-------------------|---------------------------------------|----------|
| Sarakkeiden määrä | Numero väliltä **1**–**4**     | Sisällöntäyteisen lohkon sarakkeiden määrä. Sarakkeita voi olla enintään neljä. |
| Leveys             | **Täytä säilö** tai **Täytä näyttö** | Jos arvoksi on määritetty **Täytä säilö** säilön sisällä olevat nimikkeet ovat korkeintaan säilön levyisiä. Jos arvoksi on määritetty **Täytä näyttö**, säilön leveys ei rajoita leveyttä, vaan nimikkeet voivat olla koko näytön levyisiä. Voit muuttaa arvoa halutun asettelun saavuttamiseksi. |

## <a name="content-rich-block-item-module-properties"></a>Sisällöntäyteisen lohkonimikemoduulin ominaisuudet

| Ominaisuuden nimi | Arvo          | Kuvaus |
|---------------|----------------|-------------|
| Kappale     | Kappaleen teksti | Kunkin sisällöntäyteisen lohkonimikkeen teksti. Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus ja kursiivi. |

## <a name="add-a-content-rich-block-module-to-a-page"></a>Sisällöntäyteisen lohkomoduulin lisääminen sivulle

Voit lisätä sisällöntäyteisen lohkomoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo sivumalli, jonka nimi on **Sisältömalli**.
1. Lisää sisällöntäyteinen lohkomoduuli oletussivun **pääpaikkaan**.
1. Kirjaa malli sisään ja julkaise se.
1. Käytä juuri luotua sisältömallia, kun haluat luoda sivun nimeltä **Sisältösivu**.
1. Lisää sisällöntäyteinen lohkomoduuli uuden sivun **pääpaikkaan**.
1. Määritä sisällöntäyteisen lohkomoduulin ominaisuuksissa sarakkeiden määräksi **2**.
1. Valitse sisällöntäyteisessä lohkomoduulissa **Lisää moduuli** ja lisää sisällöntäyteinen lohkonimike (esimerkiksi **nimike1**).
1. Lisää uuteen sisällöntäyteiseen lohkonimikkeeseen kappaleen teksti.
1. Valitse sisällöntäyteisessä lohkomoduulissa **Lisää moduuli** ja lisää sisällöntäyteinen lohkonimike (esimerkiksi **nimike2**).
1. Lisää uuteen sisällöntäyteiseen lohkonimikkeeseen kappaleen teksti.
1. Tallenna sivu ja esikatsele muutokset. Kaksisarakkeisessa näkymässä on näkyvissä kaksi sisällöntäyteistä lohkoa.
1. Kirjaa sivu sisään ja julkaise se.

> [!NOTE]
> Jos lisäät kolmannen sisällöntäyteisen lohkonimikkeen, se pinotaan kahden aiemmin lisätyn nimikkeen alle. Jos muutat sarakkeiden ja nimikkeiden määrää säilössä, voit muodostaa erilaisia asetteluita tekstisisällölle.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Hälytysmoduuli](add-alert.md)

[Karusellimoduuli](add-carousel.md)

[Sisällönsijoittelumoduuli](add-content-placement-modules.md)

[Omaisuusmoduuli](add-feature-module.md)

[Hero-moduuli](add-hero-module.md)

[Videotoistinmoduuli](add-video-player.md)

