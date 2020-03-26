---
title: Videoiden lataaminen
description: Tässä ohjeaiheessa kerrotaan, miten videot ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 98cb4f9049509dd700cf38a5d176447f86e9c824
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097009"
---
# <a name="upload-videos"></a>Videoiden lataaminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten videot ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.

## <a name="overview"></a>Yleiskuvaus

Commerce-sivuston luontiohjelman mediakirjaston avulla voit ladata videoita. Lataa aina sellainen videoversio, jonka jonka bittinopeus ja resoluutio ovat parhaat mahdolliset, koska video muutetaan automaattisesti eri näyttöjen ja niiden keskeytyskohtien mukaisesti.

### <a name="video-information-specified-during-upload"></a>Latauksen aikana määritettävät videon tiedot

Kun lataat videon, seuraavat tiedot voidaan määrittää.

- **Otsikko, kuvaus, avainsanat**: Videon metatiedot.
- **Luo automaattisesti tekstitykset**: Määrittää, luodaanko videolle automaattisesti tekstitykset.
- **Tekstitys**: Määrittää käytettävät tekstitykset.
- **Tavallinen ääni**: Määrittää käytettävän tavallisen ääniraidan.
- **Pikkukuva**: Määrittää videon pikkukuvan. Jos tätä ei ole määritetty, se määritetään automaattisesti.
- **Kuvaava ääni**: Määrittää käytettävän kuvaavan ääniraidan.

## <a name="upload-a-video"></a>Videon lataaminen

Voit ladata videon sivuston luontiohjelmaan seuraavasti.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.
1. Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.
1. Siirry Resurssienhallinnan ikkunaan ja valitse jokin ladattava video. Valitse sitten **Avaa**.
1. Syötä **Lataa medianimike** -valintaikkunaan pakollinen otsikko ja vaihtoehtoinen teksti.
1. Syötä valinnainen kuvaus ja avainsanat. Valitse tarvittaessa luokka. 
1. Jos haluat julkaista kuvat heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu
1. Valitse **OK**.

Jos olet lataamassa useita resurssityyppejä samanaikaisesti (esimerkiksi kuvia ja videoita), **Lataa medianimike** -valintaikkunassa voit vain määrittää avainsanoja. Tiedostot tulee julkaista heti lataamisen jälkeen ja samoin määrittää, luodaanko tekstitykset automaattisesti videotiedostoille. Kaikki resurssit jakavat samat avainsanat.

## <a name="additional-resources"></a>Lisäresurssit

[Digitaalisten resurssien hallinnan yleiskatsaus](dam-overview.md)

[Lataa kuvat](dam-upload-images.md)

[Lataa tiedostot](dam-upload-files.md)

[Rajaa kuvat](dam-crop-images.md)

[Mukauta kuvan keskipisteitä](dam-custom-focal-point.md)
