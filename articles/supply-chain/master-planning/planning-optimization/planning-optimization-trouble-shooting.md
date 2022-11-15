---
title: Suunnittelun optimoinnin vianmääritys
description: Tässä artikkelissa käsitellään sellaisten ongelmien korjaamista, joita suunnittelun optimoinnin käytössä voi esiintyä.
author: t-benebo
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 37c38ab9cec8ae3c9d4decf8043b43ea2251083e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739726"
---
# <a name="troubleshoot-planning-optimization"></a>Suunnittelun optimoinnin vianmääritys 

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa käsitellään sellaisten yleisten ongelmien korjaamista, joita suunnittelun optimoinnin käytössä voi esiintyä.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Suunnittelun optimoinnin lisäosa ei asennu loppuun asti

Suunnittelun optimointi edellyttää korkean käytettävyyden ympäristöä, jossa Lifecycle Services (LCS) on käytössä ja jonka taso on 2 tai korkeampi (ei OneBox-ympäristö). Käytössä on lisäksi oltava Dynamics 365 Supply Chain Managementin versio 10.0.7 tai sitä uudempi versio. Jos lisäosa yritetään asentaa OneBox-ympäristöön, asennusta ei suoriteta loppuun.

**Korjaus**: peruuta asennus ja käytä korkean käytettävyyden tason 2 tai sitä korkeampaa ympäristöä (ei OneBox-ympäristöä).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Erätöiden suunnittelu epäonnistuu, kun suunnittelun optimointi on käytössä

Kun suunnittelun optimointi otetaan käyttöön, vanhentunut pääsuunnittelumoduuli poistetaan automaattisesti käytöstä. Vanhentuneelle pääsuunnittelumoduulille luodut pääsuunnittelun erätyöt epäonnistuvat, jos ne ovat käynnistyneet suunnittelun optimoinnin ollessa käytössä. Näkyviin voi tulla esimerkiksi seuraavankaltainen virhesanoma, jonka mukaan *tämä toiminto käynnisti pääsuunnittelun, jota ei tueta, kun suunnittelun optimointi on otettu käyttöön*.

**Korjaus**: Peruuta kaikki pääsuunnittelutyöt, jotka luotiin vanhentuneelle pääsuunnittelumoduulille.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Suunnittelun optimoinnin tulokset poikkeavat aiemmista tuloksista

Suunnittelun optimointi poikkeaa vanhentuneen pääsuunnittelumoduulin rakenteesta joillakin alueilla. Myös odottavat toiminnot voivat aiheuttaa tämän.

**Korjaus**: Suorita suunnittelun optimoinnin kuntoanalyysi ja analysoi sitten tulokset samalla, kun selvität, mikä vaikutus niillä on liittyvän dokumentaation avulla. Lisätietoja on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>Suunnittelun optimointia ei voi ottaa käyttöön

**Yhteystila**-arvon on oltava **Yhdistetty**, ennen kuin **Käytä suunnittelun optimointi** -asetukseksi voi määrittää **Kyllä**. Lisätietoja on kohdassa [Suunnittelun optimoinnin käytön aloittaminen](get-started.md).

**Korjaus**: varmista, että suunnittelun optimoinnin lisäosa asennettiin oikein.

## <a name="error-message-is-shown-during-ctp"></a>Saatavuuden (CTP:n) aikana näkyy virhesanoma

Jos yrittää suorittaa saatavuuden (CTP:n) myyntitilauksesta, kun suunnittelun optimointi on otettu käyttöön, näkyviin tulee seuraava virhesanoma, jonka mukaan *tämä toiminto käynnisti pääsuunnittelun, jota ei tuettu, kun suunnittelun optimointi on käytössä*.

Tämä liittyy odottavaan toimintoon, joka suunniteltu tuotantotilausten tuen osaksi.

**Korjaus:** vältä saatavuuden (CTP:n) laskelmia, kun suunnittelun optimointi on käytössä, kunnes saatavuuden (CTP:n) tuki on saatavana.

## <a name="additional-resources"></a>Lisäresurssit

- [Pääsuunnittelun aloittaminen](get-started.md)
- [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]