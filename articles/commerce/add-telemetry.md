---
title: Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi
description: Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: dfebc6616186a3a8859b00e90c178129feaa324b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980154"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.

## <a name="overview"></a>Yleiskatsaus

Web Analytics on tärkeä työkalu, kun halutaan ymmärtää, miten asiakkaat käyttävät sivustoa ja miten he tekevät päätöksiä. Tämä mahdollistaa muuntokokemuksen optimoinnin ja muunnon maksimoinnin. Käytettävissä on useita Web Analytics -paketteja, joiden avulla tavoitteet voidaan saavuttaa. Paketteja ovat esimerkiksi Google Analytics, Clicky, Moz Analytics ja KISSMetrics. Useimmat Web Analytics -paketit edellyttävät, että lisäät asiakaspuolen komentosarjakoodin HTML:n **\<head\>**-elementtiin kaikille sivuston sivuille.

> [!NOTE]
> Tämän ohjeaiheen ohjeet koskevat myös muita mukautettuja asiakaspuolen toimintoja, joita Microsoft Dynamics 365 Commerce ei tarjoa suoraan.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Uudelleenkäytettävän osan luominen komentosarjakoodia varten

Osan avulla voit käyttää uudelleen sisäistä tai ulkoista komentosarjakoodia kaikilla sivuston sivuilla käytettävästä mallista riippumatta.

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>Uudelleenkäytettävän osan luominen sisäistä komentosarjakoodia varten

Voit luoda uudelleenkäytettävän osan sisäistä komentosarjakoodia varten sivuston luontiohjelmassa seuraavasti:

1. Siirry kohtaan **Fragmentit** ja valitse sitten **Uusi**.
1. Valitse **Uusi osa** -valintaikkunassa **Sisäinen komentosarja**.
1. Kirjoita **Osan nimi** -kohtaan osan nimi ja valitse sitten **OK**.
1. Valitse luomasi osan **Oletusarvoinen sisäinen komentosarja** -moduuli.
1. Kirjoita oikealla olevan ominaisuusruudun **Sisäinen komentosarja** -kohtaan asiakaspuolen komentosarjasi. Määritä sitten muut asetukset tarpeen mukaan.
1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Valitse **Julkaise**.

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>Uudelleenkäytettävän osan luominen ulkoista komentosarjakoodia varten

Voit luoda uudelleenkäytettävän osan ulkoista komentosarjakoodia varten sivuston luontiohjelmassa seuraavasti:

1. Siirry kohtaan **Fragmentit** ja valitse sitten **Uusi**.
1. Valitse **Uusi osa** -valintaikkunassa **Ulkoinen komentosarja**.
1. Kirjoita **Osan nimi** -kohtaan osan nimi ja valitse sitten **OK**.
1. Valitse luomasi osan **Oletusarvoinen ulkoinen komentosarja** -moduuli.
1. Lisää ulkoisen komentosarjalähteen ulkoinen tai suhteellinen URL-osoite **Komentosarjan lähde** -kohdan oikealla puolella olevaan ominaisuusruutuun. Määritä sitten muut asetukset tarpeen mukaan.
1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Valitse **Julkaise**.

> [!NOTE]
> Jos sisällön suojauskäytäntö (CSP) on otettu sivustossa käyttöön, varmista, että ulkoiset URL-osoitteet on lisätty **script-src**-CSP-direktiiviin Commercen sivustonmuodostimessa. Lisätietoja on kohdassa [Sisällön suojauskäytännön hallinta](manage-csp.md).

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>Komentosarjakoodia sisältävän osan lisääminen malliin

Voit lisätä osan, joka sisältää komentosarjan koodin malliin sivuston luontiohjelmassa noudattamalla näitä vaiheita.

1. Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.
1. Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML:n pääpaikka** tulee näkyviin.
1. Valitse kolmen pisteen painike (**...**) **HTML:n pääpaikassa** ja valitse sitten **Lisää osa**.
1. Valitse komentosarjakoodille luomasi osa.
1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Valitse **Julkaise**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Ulkoisen komentosarjan tai sisäisen komentosarjan lisääminen suoraan malliin

Jos haluat lisätä sisäisen tai ulkoisen komentosarjan suoraan yhden mallin hallitsemille sivuille, sinun ei tarvitse ensin luoda osaa.

### <a name="add-an-inline-script-directly-to-a-template"></a>Sisäisen komentosarjan lisääminen suoraan malliin

Voit lisätä sisäisen komentosarjan suoraan sivustonmuodostimen malliin noudattamalla seuraavia ohjeita.

1. Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.
1. Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML:n pääpaikka** tulee näkyviin.
1. Valitse kolmen pisteen painike (**...**) **HTML:n pääpaikassa** ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Sisäinen komentosarja**.
1. Kirjoita oikealla olevan ominaisuusruudun **Sisäinen komentosarja** -kohtaan asiakaspuolen komentosarjasi. Määritä sitten muut asetukset tarpeen mukaan.
1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Valitse **Julkaise**.

### <a name="add-an-external-script-directly-to-a-template"></a>Ulkoisen komentosarjan lisääminen suoraan malliin

Voit lisätä ulkoisen komentosarjan suoraan sivustonmuodostimen malliin noudattamalla seuraavia ohjeita.

1. Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.
1. Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML:n pääpaikka** tulee näkyviin.
1. Valitse kolmen pisteen painike (**...**) **HTML:n pääpaikassa** ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Ulkoinen komentosarja**.
1. Lisää ulkoisen komentosarjalähteen ulkoinen tai suhteellinen URL-osoite **Komentosarjan lähde** -kohdan oikealla puolella olevaan ominaisuusruutuun. Määritä sitten muut asetukset tarpeen mukaan.
1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Valitse **Julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Logon lisääminen](add-logo.md)

[Sivuston teeman valitseminen](select-site-theme.md)

[CSS-ohitustiedostojen parissa työskentely](css-override-files.md)

[Favicon-kuvakkeen lisääminen](add-favicon.md)

[Tervetuloviestin lisääminen](add-welcome-message.md)

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)
