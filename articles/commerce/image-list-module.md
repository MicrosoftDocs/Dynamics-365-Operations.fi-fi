---
title: Kuvaluettelomoduuli
description: Tässä artikkelissa kerrotaan kuvaluettelomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
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
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: e89624a98d3cbdd861391e994386ae57d2c38aa0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269832"
---
# <a name="image-list-module"></a>Kuvaluettelomoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan kuvaluettelomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Kuvaluettelomoduulin avulla kuvien kokoelmia (taulukoita) voidaan lisätä helposti sivuston sivuille. Jokaiseen taulukon sisältämään kuvaan voidaan lisätä kappaletekstiä ja URL-linkkejä. Kuvaluettelomoduuli sopii parhaiten logojen tai logoja sisältävän luettelon esittämiseen.

> [!IMPORTANT]
> - Kuvaluettelomoduuli on käytettävissä Commerce-moduulikirjastossa Dynamics 365 Commerce -versiosta 10.0.20 eteenpäin.
> - Kuvaluettelomoduuli on esillä Adventure Works -teemassa.

Seuraavassa kuvassa on esimerkki kuvaluettelomoduulista, joka näyttää logoja sisältävän tekstiluettelon Adventure Works -teeman B2C-sivustojen sivuilla.

![Esimerkki kuvaluettelomoduulista, jossa näyttää logoja sisältävän tekstiluettelon](./media/Image_list.PNG)

Seuraavassa kuvassa on esimerkki kuvaluettelomoduulista, joka näyttää tuotemerkkien logoja Adventure Works -teeman B2B-sivustojen sivuilla.

![Esimerkki kuvaluettelomoduulista, joka näyttää tuotemerkkien logoja](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>Kuvaluettelomoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Otsikko       | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Kuvaluettelomoduulin tekstiotsikko. |
| Kuvaluettelo    | Kuvat, teksti ja URL-osoitteet | Jokainen taulukossa oleva nimike on kuva, johon liittyy kappaleteksti ja URL-osoite. |

## <a name="add-an-image-list-module-to-a-new-page"></a>Kuvaluettelomoduulin lisääminen uudelle sivulle

Voit lisätä kuvaluettelomoduulin uudelle sivulle ja määrittää sen vaaditut ominaisuudet Commerce-sivuston luontiohjelmassa noudattamalla seuraavia ohjeita.

1. Valitse **Mallit** ja avaa sivustosi aloitussivun markkinointimalli (tai luo uusi markkinointimalli).
1. Valitse oletussivun **pääpaikassa** kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kuvaluettelo**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Valitse **Sivut** ja avaa sivuston aloitussivu (tai luo uusi aloitussivu käyttämällä markkinointimallia).
1. Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kuvaluettelo**-moduuli ja valitse sitten **OK**.
1. Lisää otsikko kuvaluettelomoduulin ominaisuusruudussa (esimerkiksi **Tuotemerkkimme**).
1. Lisää kuvaluettelon nimike ja määritä kuva, kappaletekstiä ja uudelleenohjauksen URL-osoite.
1. Lisää ja määritä lisää kuvaluettelon nimikkeitä tarpeen mukaan.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Adventure Works -teema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
