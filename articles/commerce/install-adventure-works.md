---
title: Adventure Works -teeman asentaminen
description: Tässä artikkelissa kuvataan, kuinka Adventure Works -teema asennetaan Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 12/10/2021
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
ms.openlocfilehash: f5c195694633c96a473f0f824c1f182903082bff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274283"
---
# <a name="install-the-adventure-works-theme"></a>Adventure Works -teeman asentaminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka Adventure Works -teema asennetaan Microsoft Dynamics 365 Commercessa. 

> [!IMPORTANT]
> Adventure Works -teema ja -moduulit ovat käytettävissä Dynamics 365 Commerce -versiosta 10.0.20 eteenpäin. Ne ovat käytettävissä kohteesta Microsoft AppSource.

## <a name="prerequisites"></a>Edellytykset

Ennen Adventure Works -teeman asennusta sinulla on oltava Dynamics 365 Commerce -ympäristö  (Commerce version 10.0.20 tai myöhempi), joka sisältää Retail Cloud Scale Unitin (RCSU), Commerce online software development kit (SDK) -ohjelman ja Commerce-moduulikirjaston. Lisätietoja Commerce SDK -ohjelman ja moduulikirjaston asentamisesta on kohdassa [Määritä kehitysympäristö](e-commerce-extensibility/setup-dev-environment.md). 

## <a name="installation-steps"></a>Asennusvaiheet

### <a name="install-the-adventure-works-theme-in-your-application"></a>Adventure Works -teeman asentaminen sovellukseen

Adventure Works -teemapaketti on käytettävissä **dynamics365-commerce** -syötteessä nimellä **@msdyn365-commerce-theme/adventureworks-theme-kit**. Vaikka Adventure Works -teemapaketti on osa tätä syötettä, sen nimiavaruus on eri. Siksi nimitilaan on lisättävä rekisterimerkinnät seuraavien vaiheiden mukaisesti.

1. Päivitä **.npmrc**-tiedosto niin, että se sisältää seuraavan rekisterimerkinnän (jos merkintää ei ole vielä sisällytetty):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Päivitä **.yarnrc**-tiedosto niin, että se sisältää seuraavan rekisterimerkinnän (jos merkintää ei ole vielä sisällytetty):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Jos haluat asentaa paketin paikallisessa ympäristössä, suorita `yarn add THEME_PACKAGE@VERSION`-komento komentokehotteesta, jossa **THEME_PACKAGE** on teemapakkaus (@msdyn365-commerce-theme/adventureworks-theme-kit) ja **VERSION** on käytettävä moduulikirjaston versionumero. On tärkeää, että moduulikirjaston ja teemapaketin versiot vastaavat toisiaan. Voit etsiä oikean käytettävän moduulikirjaston versionumeron avaamalla package.json-tiedoston ja etsimällä **aloituspaketin** arvon **riippuvuudet**-osasta. Seuraavassa esimerkissä package.json-tiedostossa käytetään moduulikirjaston versiota 9.32, joka sisältää Dynamics 365 Commerce version 10.0.22 julkaisun.  

```json
"dependencies": {
    "@msdyn365-commerce-modules/starter-pack": "9.32",
}
```

Seuraavassa esimerkissä kerrotaan, miten Adventure Works -aiheen versio 9.32 lisättiin `yarn add`-komennolla. Komento päivittää package.json-tiedoston automaattisesti niin, että se sisältää riippuvuuden.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit@9.32`

Lue lisätietoja moduulikirjaston version päivittämisestä kohdasta [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md). 

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
