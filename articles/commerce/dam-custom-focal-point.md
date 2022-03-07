---
title: Kuvan keskipisteiden mukauttaminen
description: Tässä ohjeaiheessa kerrotaan, miten kuvan keskipisteitä mukautetaan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fca209c9827192f50c2f1a5bd9e78146214e1e0e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222558"
---
# <a name="customize-image-focal-points"></a>Kuvien tarkennuspisteiden mukauttaminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten kuvan keskipisteitä mukautetaan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.

## <a name="overview"></a>Yleiskuvaus

Kun kuva ladataan Commerce-sivuston luontiohjelman mediakirjastoon, järjestelmä yrittää määrittää kuvan keskipisteen. Jos kuvassa on henkilö, järjestelmä määrittää oletusarvoisesti keskipisteeksi henkilön kasvot. Useimmissa tapauksissa automaattisesti määritetyt keskipisteet toimivat hyvin näytöissä. Joskus on ehkä tarpeen muokata keskipistettä ja varmistaa, että kuvan tietty osa on aina näkyvissä.

### <a name="define-a-custom-focal-point-for-an-image"></a>Kuvan mukautetun keskipisteen määrittäminen

Voit määrittää kuvalle mukautetun keskipisteen seuraavasti.

1. Valitse Commerce-sivuston luontiohjelman vasemmanpuoleisessa ruudussa **Mediakirjasto**.
1. Valitse pääikkunassa kuva, jota haluat muokata.
1. Valitse komentopalkissa **Muokkaa**.
1. Valitse kuva ja syötä **Muokkaustila**.
1. Valitse **Muokkaustila**-kohdassa **Muuta keskipistettä**. Kuvan päälle ilmestyy pyöreä keskipiste.
1. Valitse keskipisteen ohjausobjekti, joka siirretään haluttuun keskipisteeseen.
1. Kun olet valmis, valitse komentopalkissa **Tallenna** ja valitse sitten **Lopeta muokkaus**.

## <a name="additional-resources"></a>Lisäresurssit

[Digitaalisten resurssien hallinnan yleiskatsaus](dam-overview.md)

[Kuvien lataaminen palveluun](dam-upload-images.md)

[Videon lataaminen palveluun](dam-upload-video.md)

[Lataa tiedostot](dam-upload-files.md)

[Kuvien rajaaminen](dam-crop-images.md)

[Staattisten tiedostojen lataaminen ja käyttäminen](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]