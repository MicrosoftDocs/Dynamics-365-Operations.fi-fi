---
title: Adventure Works -teeman asentaminen
description: Tässä aiheessa kuvataan, kuinka Adventure Works -teema asennetaan Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 07/21/2021
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9c94dd8ead32f58a25a396376840101d9c2c9b08
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655845"
---
# <a name="install-the-adventure-works-theme"></a>Adventure Works -teeman asentaminen

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan, kuinka Adventure Works -teema asennetaan Microsoft Dynamics 365 Commercessa. 

> [!IMPORTANT]
> Adventure Works -teema ja -moduulit ovat käytettävissä Dynamics 365 Commerce -versiosta 10.0.20 eteenpäin. Ne ovat käytettävissä kohteesta Microsoft AppSource.

## <a name="prerequisites"></a>Edellytykset

Ennen Adventure Works -teeman asennusta sinulla on oltava Dynamics 365 Commerce -ympäristö  (Commerce version 10.0.20 tai myöhempi), joka sisältää Retail Cloud Scale Unitin (RCSU), Commerce online software development kit (SDK) -ohjelman ja Commerce-moduulikirjaston. Lisätietoja Commerce SDK -ohjelman ja moduulikirjaston asentamisesta on kohdassa [SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md). 

## <a name="installation-steps"></a>Asennusvaiheet

### <a name="install-the-adventure-works-theme-in-your-application"></a>Adventure Works -teeman asentaminen sovellukseen

Adventure Works -teemapaketti on käytettävissä **dynamics365-commerce** -syötteessä nimellä **@msdyn365-commerce-theme/adventureworks-theme-kit**. Vaikka Adventure Works -teemapaketti on osa tätä syötettä, sen nimiavaruus on eri. Siksi nimitilaan on lisättävä rekisterimerkinnät seuraavien vaiheiden mukaisesti.

1. Päivitä **.npmrc**-tiedosto niin, että se sisältää seuraavan rekisterimerkinnän (jos merkintää ei ole vielä sisällytetty):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Päivitä **.yarnrc**-tiedosto niin, että se sisältää seuraavan rekisterimerkinnän (jos merkintää ei ole vielä sisällytetty):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Voit asentaa paketin paikalliseen ympäristöön komentokehotteesta suoritettavalla seuraavalla komennolla. Tämä komento päivittää package.json-tiedoston automaattisesti niin, että se sisältää riippuvuuden.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

**Package.json**-tiedostossa on päivitettävä teeman versio tiettyyn versioon.

> [!IMPORTANT]
> - Moduulikirjaston version tulisi olla sama kuin teeman version, jotta kaikki toiminnot toimivat odotetulla tavalla. 
> - Commerce-moduulikirjaston ja SDK:n minimiversion tulee olla 10.0.20 (9.31). 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Adventure Works -teeman fonttitiedostojen lisääminen

Kun Adventure Works -teema on asennettu sovellukseen, siihen on lisättävä tarvittavat fonttitiedostot. Suorita tämä vaihe kopioimalla kaikki fonttitiedostot kohteesta **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** kumppanisovelluksen julkiseen hakemistopolkuun **\public\webfonts**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Adventure Works -teeman resurssien määritys

Seuraava vaihe on teeman vaaditun oletusresurssin päivittäminen. Suorita tämä vaihe kopioimalla global.json-tiedoston sisältö kohteesta **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** kumppanisovelluksen global.json-tiedostoon kohteeseen **\src\resources\modules**. Jos **\src\resources**-kohdehakemistoa ei ole olemassa, se voidaan kopioida kokonaisuudessaan **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks**-lähdehakemistosta **\src**-kohdehakemistoon.

### <a name="pull-updates-and-validate-the-theme"></a>Päivitysten hakeminen ja teeman oikeellisuustarkistus

Lisätietoja uusimman SDK:n, moduulikirjaston ja muiden riippuvuuspäivitysten hakemisesta on [SDK:n ja moduulikirjaston päivitysten](e-commerce-extensibility/sdk-updates.md#pull-updates) "Hae päivitykset" -osassa.

Kun viimeisimmät riippuvuudet on haettu, voit suorittaa **yarn start**-komennon Node-palvelimen käynnistämiseksi kehitysympäristössäsi ja testata uutta Adventure Works -teemaa. Selaa sovellusta paikallisesti kyselyn merkkijonoparametrin `?theme=adventureworks` avulla (esimerkiksi `https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>Lisäresurssit

[Adventure works -teema](adventure-works-theme.md)

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
