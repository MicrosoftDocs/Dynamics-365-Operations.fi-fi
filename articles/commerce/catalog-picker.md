---
title: Luettelon valitsinmoduuli
description: Tässä artikkelissa käsitellään luettelon valitsinmoduuleja sekä niiden lisäämistä Microsoft Dynamics 365 Commercen yritystenvälisiin sähköisiin kaupankäyntisivustoihin.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136941"
---
# <a name="catalog-picker-module"></a>Luettelon valitsinmoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään luettelon valitsinmoduuleja sekä niiden lisäämistä Microsoft Dynamics 365 Commercen yritystenvälisiin sähköisiin kaupankäyntisivustoihin.

Luettelon valitsinmoduuli on erityissäilö, jonka avulla kaikista yritystenvälisen sivuston käyttäjien ostoksiin käyttämistä tuoteluetteloista muodostetaan luettelo. Useiden luetteloiden käyttöä tuetaan tällä hetkellä vain yritystenvälisissä sivustoissa.

Seuraavassa kuvassa on esimerkki luettelon valitsinmoduulista.

![Esimerkki kolme tuoteluetteloa sisältävästä luettelon valitsinmoduulista](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>Luettelon valitsinmoduulin lisääminen sivustoon

Luettelon valitsinmoduulin voi lisätä sivustoon Commercen sivustonmuodostimessa seuraavasti.

### <a name="create-a-catalog-picker-page"></a>Luettelon valitsinsivun luominen

Luo ensin luettelon valitsinsivu.

1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Anna **Luo uusi sivu** -valintaikkunan **Sivun nimi** -kohdassa **Luettelon valitsin**.
1. Anna **Sivun URL-osoite** -kohdassa sivun URL-osoite ja valitse sitten **Seuraava**.

    ![Luo uusi kirjasto -valintaikkuna](./media/Create-catalog-picker-page.png)

1. Valitse **Valitse malli** -kohdassa **Luo sisältöä** ja valitse sitten **Seuraava**.
1. Valitse **Valitse asettelu** -kohdassa **Joustava asettelu** ja valitse sitten **Seuraava**.
1. Tarkista sivun konfigurointi kohdassa **Tarkista ja viimeistele**. Jos sivun tietoja on muokattava, valitse **Takaisin**. Jos sivun tiedot ovat oikein, valitse **Luo sivu**.
1. Valitse **Luettelon valitsin** -kohdassa **Pää-paikka**, valitse kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.

    ![Moduulin lisääminen Pää-paikkaan luettelon valitsimessa](./media/Author-web-page-catalog-picker-1.png)

1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse **Säilö**-paikassa kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Luettelon valitsin**-moduuli ja valitse sitten **OK**.
1. Valitse **Luettelon valitsin** -ominaisuusruudun **Otsikko**-kohdassa **Luettelot** ja anna siiten luettelon valitsinsivun otsikko.
1. Valitse **Otsikkotaso**-kohdassa otsikkotaso ja valitse sitten **OK**.
1. Kirjoita **Muotoiltu teksti** -kohtaan teksti, joka näkyy luettelon valitsinsivun yläosassa.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

### <a name="add-a-link-on-your-account-page"></a>Tilisivulinkin lisääminen

Lisää seuraavaksi **Oma tili** -sivulla viittaus luettelon valitsinsivulle.

1. Valitse **Sivut**, etsi ja valitse sivuston **Oma tili** -sivu ja valitse lopuksi **Muokkaa**.
1. Valitse sivun **Pää**-paikassa **Tilin yleinen ruutu** -paikka. 
1. Valitse **Tilin yleinen ruutu** -ominaisuusruudun **Linkit**-kohdassa **Lisää toimintolinkki** ja valitse sitten **Toimintolinkki**.
1. Kirjoita **Toimintolinkki**-valintaruudun **Linkin teksti** -kohdassa teksti luettelon valitsinsivulle vievään linkkiin.
1. Valitse **Linkin kohde** -kohdassa **Lisää linkki**.
1. Valitse **Lisää linkki** -valintaikkunassa **Mukautettu sivu** ja valitse sitten **Seuraava**.
1. Valitse **Nimi**-kohdassa luettelon valitsinsivu, valitse sitten **Käytä** ja valitse lopuksi **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

Seuraavassa kuvassa on esimerkki tilisivusta ja viittauksesta luettelosivulle.

![Omat tilit -sivu ja linkki luetteloon](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>Linkin lisääminen otsikosta

Lopuksi lisätään linkki sivuston otsikosta luetteloihin.

1. Valitse **Katkelmat**, etsi ja valitse sivuston otsikko-osa ja valitse lopuksi **Muokkaa**.
1. Valitse **Ylätunniste**-paikka. 
1. Valitse **Otsikko**-ominaisuusruudun **Oman tilin linkit** -kohdassa **Lisää toimintolinkki** ja valitse sitten **Toimintolinkki**.
1. Kirjoita **Toimintolinkki**-valintaruudun **Linkin teksti** -kohdassa teksti luettelon valitsinsivulle vievään linkkiin.
1. Valitse **Linkin kohde** -kohdassa **Lisää linkki**.
1. Valitse **Lisää linkki** -valintaikkunassa **Mukautettu sivu** ja valitse sitten **Seuraava**.
1. Valitse **Nimi**-kohdassa luettelon valitsinsivu, valitse sitten **Käytä** ja valitse lopuksi **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi ylätunnisteen osan, ja julkaise se valitsemalla **Julkaise**.

Seuraavassa kuvassa on esimerkki sähköisen kaupankäyntisivuston otsikosta ja linkistä yritystenväliseen luetteloon.

![Sähköisen kaupankäyntisivuston otsikko ja avattavan luettelon linkki luetteloon](./media/catalog-in-header.png)


## <a name="additional-resources"></a>Lisäresurssit 

[Commerce-luetteloiden luominen B2B-sivustoja varten](catalogs-b2b-sites.md)

[Commerce-luetteloiden laajennettavuusvaikutus B2B-mukautuksia varten](catalogs-b2b-sites-dev.md)

[Usein kysytyt kysymykset B2B-sivustojen Commerce-luetteloista](catalogs-b2b-sites-FAQ.md)

[Tilin hallintasivut ja -moduulit](account-management.md)

[Ylätunnistemoduuli](author-header-module.md)
