---
title: Kuvien lataaminen palveluun
description: Tässä ohjeaiheessa kerrotaan, miten kuvat ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmaan.
author: psimolin
ms.date: 12/03/2021
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
ms.openlocfilehash: 3b99aeff7eafd788c19204e22dbfc61f45b25408
ms.sourcegitcommit: 5f5a8b1790076904f5fda567925089472868cc5a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891519"
---
# <a name="upload-images"></a>Kuvien lataaminen palveluun

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten kuvat ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmaan.

Commerce-sivuston luontiohjelman mediakirjasto sallii kuvien lataamisen yksittäin tai joukkona kansioiden avulla. Lataa aina sellainen kuvaversio, jonka jonka resoluutio ja laatu ovat parhaat mahdolliset, koska kuvan kokoa muuttava osa optimoi kuvan automaattisesti eri näyttöjen ja niiden keskeytyskohtien avulla.

### <a name="image-information-specified-during-upload"></a>Latauksen aikana määritettävät kuvan tiedot

Kun lataat kuvan, seuraavat tiedot voidaan määrittää.

- **Otsikko, vaihtoehtoinen teksti, kuvaus, avainsanat**: Kuvan tai kuvien metatiedot. Otsikko ja vaihtoehtoinen teksti ovat pakolliset arvot.
- **Valitse luokka**:
    - **Ei mitään**: Käytetään sähköisen kaupankäynnin tarinoiden kuvassa tai kuvissa.
    - **Tuote, luokka, asiakas, työntekijä, luettelo**: Käytetään Dynamics 365 Commercen monikanavan kuvassa tai kuvissa.
- **Julkaise resurssit lataamisen jälkeen**: Kun tämä valintaruutu on valittu, kuva tai kuvat julkaistaan heti lataamisen jälkeen.

> [!NOTE]
> - Kuvaresurssit, joihin on liitetty luokka, merkitään automaattisesti luokkaan avainsanana. Tämä auttaa tietyn luokan resurssien hakemisessa.
> - Tuotetietosivut luovat **alt-tekstin** dynaamisesti tuotenimeä käyttäen, joten tuotteen kuvan **Alt-tekstin** muuttaminen ei vaikuta muodostettuun kuvaan.

### <a name="naming-conventions-for-omni-channel-images"></a>Monikanavan kuvien nimeämiskäytännöt 

Jos olet määrittänyt mediakirjaston monikanavan kuvan taustalle, voit käyttää kuvaluokkia määrittäessäsi luokan, johon ladattu kuva kuuluu. On olemassa myös nimeämiskäytäntö, jota on noudatettava. Se varmistaa, että kuvat haetaan oikein muissa kanavissa, kuten myyntipisteessä.

Oletusnimeämiskäytäntö vaihtelee luokan mukaan seuraavasti:
- Luettelon kuvat on nimettävä seuraavasti: "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"
- Luokan kuvat on nimettävä seuraavasti: "**/Categories/\{CategoryName\}.png**"
- Asiakkaan kuvat on nimettävä seuraavasti: "**/Customers/\{CustomerNumber\}.jpg**"
- Työntekijän kuvat on nimettävä seuraavasti: "**/Workers/\{WorkerNumber\}.jpg**"
- Tuotekuvat on nimettävä seuraavasti: **/Products/\{ProductNumber\}\_000_001.png**
    - 001 on kuvan järjestysluku. Se voi olla 001, 002, 003, 004 tai 005
- Tuotevariantin kuvat on nimettävä seuraavasti: "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"
    - Esimerkki: 93039 \^ &nbsp;\^ 2 \^ Black \^\_000_001.png
- Tuotevarianttikuvat ja määritysdimension nimenä on oltava **/Products/\{ProductNumber\} \^ \{Configuration\}\_000_001.png**
    - Esimerkki: 93039 \^ LB8017_000_001.png

> [!NOTE]
> Jos dimensioarvo on tyhjä tuotevarianttikuvissa, tiedoston nimessä on oltava kaksi välilyöntiä sirkumfleksien välissä.

Edellä olevissa esimerkeissä käytetään oletusmääritystä. Erotinmerkki ja dimensiot voidaan määrittää, ja tarkka nimeämistapa voi vaihdella eri käyttöönotoissa. Yksi tapa tunnistaa tarvittava täsmällinen nimeämiskäytäntö on käyttää selaimen kehittäjäkonsolia ja tarkastella tuotevarianttikuvan pyynnöt, kun tuotedimensioita muutetaan myymälän tuotetietosivulla (PDP).

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
