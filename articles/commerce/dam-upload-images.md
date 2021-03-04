---
title: Lataa kuvat
description: Tässä ohjeaiheessa kerrotaan, miten kuvat ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.
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
ms.openlocfilehash: f562d3376fde6a24e6a1e1a3f7f4192cf290ae90
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594281"
---
# <a name="upload-images"></a>Lataa kuvat

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten kuvat ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.

## <a name="overview"></a>Yleiskuvaus

Commerce-sivuston luontiohjelman mediakirjasto sallii kuvien lataamisen yksittäin tai joukkona kansioiden avulla. Lataa aina sellainen kuvaversio, jonka jonka resoluutio ja laatu ovat parhaat mahdolliset, koska kuvan kokoa muuttava osa optimoi kuvan automaattisesti eri näyttöjen ja niiden keskeytyskohtien avulla.

### <a name="image-information-specified-during-upload"></a>Latauksen aikana määritettävät kuvan tiedot

Kun lataat kuvan, seuraavat tiedot voidaan määrittää.

- **Otsikko, vaihtoehtoinen teksti, kuvaus, avainsanat**: Kuvan tai kuvien metatiedot. Otsikko ja vaihtoehtoinen teksti ovat pakolliset arvot.
- **Valitse luokka**:
    - **Ei mitään**: Käytetään sähköisen kaupankäynnin tarinoiden kuvassa tai kuvissa.
    - **Tuote, luokka, asiakas, työntekijä, luettelo**: Käytetään Dynamics 365 Commercen monikanavan kuvassa tai kuvissa.
- **Julkaise resurssit lataamisen jälkeen**: Kun tämä valintaruutu on valittu, kuva tai kuvat julkaistaan heti lataamisen jälkeen.

> [!NOTE]
> Kuvaresurssit, joihin on liitetty luokka, merkitään automaattisesti luokkaan avainsanana. Tämä auttaa tietyn luokan resurssien hakemisessa.

### <a name="naming-conventions-for-omni-channel-images"></a>Monikanavan kuvien nimeämiskäytännöt 

Jos olet määrittänyt mediakirjaston monikanavan kuvan taustalle, voit käyttää kuvaluokkia määrittäessäsi luokan, johon ladattu kuva kuuluu. On olemassa myös nimeämiskäytäntö, jota on noudatettava. Se varmistaa, että kuvat haetaan oikein muissa kanavissa, kuten myyntipisteessä.

Oletusnimeämiskäytäntö vaihtelee luokan mukaan seuraavasti:
- Luettelon kuvat on nimettävä seuraavasti: "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"
- Luokan kuvat on nimettävä seuraavasti: "**/Categories/\{CategoryName\}.png**"
- Asiakkaan kuvat on nimettävä seuraavasti: "**/Customers/\{CustomerNumber\}.jpg**"
- Työntekijän kuvat on nimettävä seuraavasti: "**/Workers/\{WorkerNumber\}.jpg**"
- Tuotekuvat on nimettävä seuraavasti: "**/Products/\{ProductNumber\}_000_001.png**"
    - 001 on kuvan järjestysluku. Se voi olla 001, 002, 003, 004 tai 005
- Tuotevariantin kuvat on nimettävä seuraavasti: "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"

## <a name="upload-an-image"></a>Kuvan lataaminen

Voit ladata kuvan sivuston luontiohjelmaan seuraavasti.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.
1. Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.
1. Siirry Resurssienhallinnan ikkunaan ja valitse jokin ladattava kuva. Valitse sitten **Avaa**.
1. Syötä **Lataa medianimike** -valintaikkunaan pakollinen otsikko ja vaihtoehtoinen teksti.
1. Syötä valinnainen kuvaus ja avainsanat. Valitse tarvittaessa luokka. 
1. Jos haluat julkaista kuvat heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.
1. Valitse **OK**.

## <a name="upload-a-folder-of-images"></a>Kuvakansion lataaminen

Voit joukkoladata kuvakansion sivuston luontiohjelmaan seuraavasti.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.
1. Valitse komentopalkissa **Lataa \> Lataa kansio**.
1. Siirry Resurssienhallinnan ikkunaan ja valitse ladattava kansio. Valitse sitten **Avaa**.
1. Anna **Lataa medianimikkeet** -valintaikkunaan vaihtoehtoiset avainsanat ja valitse tarvittaessa luokka. 
1. Jos haluat julkaista kansion kuvat heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.
1. Valitse **OK**.

## <a name="additional-resources"></a>Lisäresurssit

[Digitaalisten resurssien hallinnan yleiskatsaus](dam-overview.md)

[Videon lataaminen palveluun](dam-upload-video.md)

[Lataa tiedostot](dam-upload-files.md)

[Kuvien rajaaminen](dam-crop-images.md)

[Kuvien tarkennuspisteiden mukauttaminen](dam-custom-focal-point.md)

[Staattisten tiedostojen lataaminen ja käyttäminen](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]