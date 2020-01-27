---
title: Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi
description: Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914536"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.

## <a name="overview"></a>Yleiskatsaus

Web Analytics on tärkeä työkalu, kun halutaan ymmärtää, miten asiakkaat käyttävät sivustoa ja miten he tekevät päätöksiä. Tämä mahdollistaa muuntokokemuksen optimoinnin ja muunnon maksimoinnin. Käytettävissä on useita Web Analytics -paketteja, joiden avulla tavoitteet voidaan saavuttaa. Paketteja ovat esimerkiksi Google Analytics, Clicky, Moz Analytics ja KISSMetrics. Useimmat Web Analytics -paketit edellyttävät, että lisäät asiakaspuolen komentosarjakoodin HTML:n **\<head\>**-elementtiin kaikille sivuston sivuille.

> [!NOTE]
> Tämän ohjeaiheen ohjeet koskevat myös muita mukautettuja asiakaspuolen toimintoja, joita Microsoft Dynamics 365 Commerce ei tarjoa suoraan.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Uudelleenkäytettävän osan luominen komentosarjakoodia varten

Kun olet luonut osan komentosarjakoodille, sitä voidaan käyttää uudelleen kaikilla sivuston sivuilla.

1. Siirry kohtaan **Osat \> Uusi sivun osa**.
2. Valitse **Ulkoinen komentosarja**, kirjoita osan nimi ja valitse sitten **OK**.
3. Valitse osahierarkiassa **komentosarjan lisäystoiminto** -moduulin osan alitaso, jonka loit juuri.
4. Lisää asiakaspuolen komentosarja oikealla olevaan ominaisuusruutuun ja määritä muut tarvittavat määritysvaihtoehdot.

## <a name="add-the-fragment-to-templates"></a>Osan lisääminen malleihin

1. Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.
2. Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML Head** -paikka.
3. Valitse kolmen pisteen painike (**...**) **HTML Head** -paikkaa varten ja valitse sitten **Lisää osa**.
4. Valitse komentosarjakoodille luomasi osa.
5. Tallenna malli ja julkaise se.

> [!NOTE]
> Kun olet valmis, sinun on julkaistava osa ja päämalli. 

## <a name="additional-resources"></a>Lisäresurssit

[Logon lisääminen](add-logo.md)

[Sivuston teeman valitseminen](select-site-theme.md)

[CSS-ohitustiedostojen parissa työskentely](css-override-files.md)

[Favicon-kuvakkeen lisääminen](add-favicon.md)

[Tervetuloviestin lisääminen](add-welcome-message.md)

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

