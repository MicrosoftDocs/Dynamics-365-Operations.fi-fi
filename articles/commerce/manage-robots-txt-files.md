---
title: Robots.txt-tiedostojen hallinta
description: Tässä ohjeaiheessa kerrotaan, miten robots.txt-tiedostoja hallitaan Microsoft Dynamics 365 Commercella.
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9b832d6714447f8957095c8c87d48527087f12d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794232"
---
# <a name="manage-robotstxt-files"></a>Robots.txt-tiedostojen hallinta

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten robots.txt-tiedostoja hallitaan Microsoft Dynamics 365 Commercella.

Robottien poissulkemisstandardi tai robots.txt on standardi, jonka avulla sivustot kommunikoivat Web-robottien kanssa. Se ohjeistaa Web-robotteja kaikista verkkosivuston alueista, joilla ei pitäisi käydä. Hakukoneet käyttävät usein robotteja indeksoidakseen verkkosivustoja.

Jos haluat sulkea robotit pois palvelimelta, luo tiedosto palvelimelle. Tässä tiedostossa määritetään robots-sovelluksen käyttöoikeuskäytäntö. Tiedoston on oltava käytettävissä HTTP-protokollan kautta paikallisessa URL-osoitteessa **/robots.txt**. Robots.txt-tiedosto auttaa hakukoneita indeksoimaan sivustosi sisällön.

Dynamics 365 Commerce auttaa sinua lataamaan robots.txt-tiedoston toimialueellesi. Voit ladata kullekin Commerce Environment -verkkotunnukselle yhden robots.txt-tiedoston ja liittää sen toimialueeseen.

Lisä tietoja robots.txt-tiedostosta on [Web Robots-sivuilla](https://www.robotstxt.org/).

## <a name="upload-a-robotstxt-file"></a>Robots.txt-tiedoston lataaminen

Kun olet luonut ja muokannut robots.txt-tiedostoasi [robottien poissulkemisstandardin](https://www.robotstxt.org/orig.html) mukaisesti, varmista, että tiedosto on käytettävissä tietokoneessa, jossa käytät Commercen luontityökaluja. Tiedoston on oltava nimeltään **robots.txt**. Parhaan tuloksen saamiseksi sen on oltava standardissa mainitussa muodossa. Jokainen Commerce-asiakas on vastuussa robots.txt-tiedoston sisällön validoinnista ja ylläpitämisestä. Ladataksesi robots.txt -tiedoston, sinun on oltava kirjautuneena sisään Commercen järjestelmänvalvojana.

Jos haluat ladata robots.txt-tiedoston sivustoon Commerce-sivustossa, toimi seuraavasti.

1. Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.
2. Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).
3. Valitse **Vuokraajan asetukset** -kohdasta **Robots.txt**. Luettelo kaikista ympäristöön liittyvistä toimialueista näkyy ikkunan pääosassa.
4. Valitse **Hallitse**, jos haluat ladata robots. txt-tiedoston ympäristösi toimialueelle.
5. Valitse oikealla olevasta valikosta robots.txt-tiedostoon liitetyn toimialueen viereinen **lähetys**-painike (ylöspäin osoittava nuoli). Näyttöön tulee tiedostoselainvalintaikkuna.
6. Etsi ja valitse valintaikkunassa robots.txt-tiedosto, jonka haluat ladata liitettyä toimialuetta varten, ja valitse sitten **Avaa**, niin lataus on valmis.

> [!NOTE] 
> Latauksen aikana Commerce tarkistaa, että tiedosto on tekstitiedosto, mutta se ei vahvista tiedoston sisältöä.

## <a name="download-a-robotstxt-file"></a>Robots.txt-tiedoston lataaminen

Jos haluat ladata robots.txt-tiedoston sivustoon Commerce-sivustossa, toimi seuraavasti.

1. Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.
2. Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).
3. Valitse **Vuokraajan asetukset** -kohdasta **Robots.txt**. Luettelo kaikista ympäristöön liittyvistä toimialueista näkyy ikkunan pääosassa.
4. Valitse **Hallitse**, jos haluat ladata robots. txt-tiedoston ympäristösi toimialueelle.
5. Valitse oikealla olevasta valikosta robots.txt-tiedostoon liitetyn toimialueen viereinen **Lataus**-painike (alaspäin osoittava nuoli). Näyttöön tulee tiedostoselainvalintaikkuna.
6. Siirry valintaikkunassa haluamaasi sijaintiin paikallisessa asemassa, vahvista tai kirjoita tiedoston nimi ja viimeistele lataaminen valitsemalla **Tallenna**.

> [!NOTE]
> Tämän toiminnon avulla voidaan ladata vain robots.txt-tiedostoja, jotka on aiemmin ladattu Commerce authoring toolsin kautta.

## <a name="delete-a-robotstxt-file"></a>Robots.txt-tiedoston poistaminen

Jos haluat poistaa robots.txt-tiedoston sivustoon Commerce-sivustossa, toimi seuraavasti.

1. Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.
2. Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).
3. Valitse **Vuokraajan asetukset** -kohdasta **Robots.txt**. Luettelo kaikista ympäristöön liittyvistä toimialueista näkyy ikkunan pääosassa.
4. Valitse **Hallitse**, jos haluat poistaa robots.txt-tiedoston ympäristösi toimialueelle.
5. Valitse oikealla olevasta valikosta robots.txt-tiedostoon liitetyn toimialueen viereinen **Poista**-painike (roskakorikuvake). Näyttöön tulee tiedostoselainikkuna.
6. Etsi ja valitse tiedostoselainikkunassa robots.txt-tiedosto, jonka haluat poistaa liitettyä toimialuetta varten, ja valitse sitten **Avaa**, niin lataus on valmis. Näyttöön tulee varoitussanomaruutu.
7. Vahvista robots.txt-tiedoston **Poistaminen** valitsemalla viestiruudusta Poista.

> [!NOTE] 
> Tämän toiminnon avulla voidaan poistaa vain robots.txt-tiedostoja, jotka on aiemmin ladattu Commerce authoring toolsin kautta.

## <a name="additional-resources"></a>Lisäresurssit

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](deploy-ecommerce-site.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Dynamics 365 Commerce -sivuston liittäminen online-kanavaan](associate-site-online-store.md)

[URL-uudelleenohjausten joukkolataus palveluun](upload-bulk-redirects.md)

[Kuluttajakaupan vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-B2C-tenants.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
