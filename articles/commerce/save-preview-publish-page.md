---
title: Sivun tallentaminen, esikatseleminen ja julkaiseminen
description: Tässä ohjeaiheessa kerrotaan, miten sivu tallennetaan, miten sitä esikatsellaan ja miten se julkaistaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 68fec8c2ddc05c71394045351cef880361f2e306
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254814"
---
# <a name="save-preview-and-publish-a-page"></a>Sivun tallentaminen, esikatseleminen ja julkaiseminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten sivu tallennetaan, miten sitä esikatsellaan ja miten se julkaistaan Microsoft Dynamics 365 Commerce -sovelluksessa.

## <a name="save-a-page"></a>Sivun tallentaminen

Jos haluat tallentaa sivun, se on kuitattava ulos käyttäjälle ja avattava sivueditorissa. Kuittaa tiedosto ulos valitsemalla komentopalkissa **Muokkaa**. Kun olet muokannut sivua, sinun tulee tallentaa se välittömästi, että tekemäsi muutokset tallennetaan.

Kun tallennat sivun, muutokset näkyvät vain sinulle. Tallennustoiminto on tarkoitettu ensisijaisesti muutosten tallentamista varten silloin, kun sivu ei ole vielä valmis kuitattavaksi sisään. Kun sivun muokkaaminen on tehty, se kannattaa kirjata sisään. Tällöin muutokset näkyvät myös muille. Tässä vaiheessa myös muut käyttäjät voivat kirjata sivun ulos, jos heidän on muokattava sitä.

## <a name="preview-a-page"></a>Sivun esikatseleminen

Muokkaustyökalussa on seuraavat kaksi esikatselutoimintoa: visuaalinen sivustonmuodostin, joka on WYSIWYG-esikatseluruutu sivueditorissa, ja erillinen esikatseluikkuna.

Kun käytät sivueditoria, keskiruudussa näkyy WYSIWYG-esikatselu. Tämä esikatselu päivitetään automaattisesti aina sivun tallentamisen yhteydessä. Voit päivittää sen myös manuaalisesti valitsemalla komentopalkissa **Päivitä**. Esikatselu hahmontaa sivun samanlaiseksi kuin käyttäjän näkymä. Sen päällä näkyvät kuitenkin muokkausavustajat.

Kun sivun muokkaaminen on tehty, haluat ehkä esikatsella sen ja nähdä, millaiselta se näyttää asiakkaille. Voit esikatsella sivua valitsemalla komentopalkissa **Esikatsele**. Esikatselu näkyy erillisessä selainikkunassa. Esikatseluikkunan sivu hahmonnetaan sellaiseksi, jona käyttäjä näkee sen. Voit muuttaa ikkunan kokoa ja varmistaa, että responsiiviset moduulit on hahmonnettu oikein kaikissa näkymäporteissa.

> [!NOTE]
> Julkaisemattoman sisällön esikatselu edellyttää todennuksen ja oikeat oikeudet. Jos siis jaat esikatselun URL-osoitteen jollekin henkilölle, tällä tulee olla oikeat oikeudet sisällön käyttämiseksi.

## <a name="publish-a-page"></a>Sivun julkaiseminen

Kun sivu on valmis, seuraava vaihe on julkaista se. Tämän jälkeen ulkoiset käyttäjät voivat tarkastella sisältöä. Ennen kuin voit julkaista sivun, sinun on tarkistettava se valitsemalla komentopalkissa **Lopeta muokkaus**.

Voit julkaista sivun ja peruuttaa sen julkaisun sivun tarkistusohjelmassa tai sivueditorissa. Sivun tarkistusohjelmassa on sivuluettelo. Se mahdollistaa joukkotoiminnot. Sivueditoria voi käyttää vain yhden sellaisen sivun julkaisemisessa tai sivun julkaisun peruuttamisessa, joka on auki editorissa.

Jos haluat julkaista yhden tai useita sivuja sivun tarkistusohjelmassa, valitse sivut, varmista, että ne on kirjattu sisään ja valitse sitten **Julkaise** komentopalkissa. Sivut julkaistaan. Saat ilmoituksen muokkaustyökalun toiminnosta.

Jos haluat julkaista yhden sivun sivueditorissa, tee samat toiminnot. Kun sivu on avoinna sivueditorissa, varmista, että se on kuitattu sisään, ja valitse sitten **Julkaise** komentopalkissa. Sivu julkaistaan. Saat ilmoituksen muokkaustyökalun toiminnosta.

Kun julkaiset sivun, vain sivun sisältö julkaistaan. Käyttäjät voivat siirtyä sivulle ja tarkastella sitä vasta sen jälkeen, kun siihen on liitetty URL-osoite. URL-osoite on julkaistava erikseen.

> [!IMPORTANT]
> Ennen kuin voit julkaista sivun, kaikkien kuvien ja osien, joihin sivu viittaa, on jo oltava julkaistu.

## <a name="save-preview-and-publish-a-home-page"></a>Aloitussivun tallentaminen, esikatseleminen ja julkaiseminen

Voit tallentaa, esikatsella ja julkaista aloitussivun noudattamalla seuraavia ohjeita.

1. Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.
1. Etsi ja valitse aloitussivu, joka avataan sivueditorissa.
1. Valitse **Muokkaa**.
1. Muokkaa sivua tarpeen mukaan.
1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Kirjoita **Kommentit**-kenttään tekemäsi muutosten huomautukset ja valitse **OK**.
1. Esikatsele sivua valitsemalla **Esikatsele**. Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.
1. Valitse **Julkaise**.

## <a name="publish-a-url"></a>URL-osoitteen julkaiseminen

Julkaise URL-osoite seuraavien ohjeiden avulla.

1. Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **URL-osoitteet**.
1. Etsi ja valitse julkaistava URL-osoite.
1. Valitse komentopalkissa **Julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Aiemmin luodun sivuston sivun muokkaaminen](modify-existing-page.md)

[Uuden sivuston sivun lisääminen](add-new-page.md)

[Sivun asettelujen valitseminen](select-page-layouts.md)

[SEO-metatietojen hallinta](manage-seo-metadata.md)

[Tuotesivun täydentäminen](enrich-product-page.md)

[Luokan saapumissivun täydentäminen](enrich-category-page.md)

[Sivun sisällön helppokäyttöisyyden tarkistaminen](verify-accessibility.md)

[Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]