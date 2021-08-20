---
title: Videoiden lataaminen
description: Tässä ohjeaiheessa kerrotaan, miten videot ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmaan.
author: psimolin
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f481e5d3f323b0c86d637b67c119d13b956d5714dc0d990004834e2be05b370e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735627"
---
# <a name="upload-videos"></a>Videoiden lataaminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten videot ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmaan.

Commerce-sivuston luontiohjelman mediakirjaston avulla voit ladata videoita. Lataa aina sellainen videoversio, jonka jonka bittinopeus ja resoluutio ovat parhaat mahdolliset, koska video muutetaan automaattisesti eri näyttöjen ja niiden keskeytyskohtien mukaisesti.

### <a name="video-information-specified-during-upload"></a>Latauksen aikana määritettävät videon tiedot

Kun lataat videon, seuraavat tiedot voidaan määrittää.

- **Otsikko, kuvaus, avainsanat**: Videon metatiedot.
- **Luo automaattisesti tekstitykset**: Määrittää, luodaanko videolle automaattisesti tekstitykset (tuki vain englannille). 
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

[Kuvien lataaminen palveluun](dam-upload-images.md)

[Lataa tiedostot](dam-upload-files.md)

[Kuvien rajaaminen](dam-crop-images.md)

[Kuvien tarkennuspisteiden mukauttaminen](dam-custom-focal-point.md)

[Staattisten tiedostojen lataaminen ja käyttäminen](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
