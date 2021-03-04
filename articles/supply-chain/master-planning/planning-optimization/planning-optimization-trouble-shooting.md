---
title: Suunnittelun optimoinnin vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita suunnittelun optimoinnin käytössä voi esiintyä.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c3dd0bf262f65aac2359c05ff954bdfbd294353f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426853"
---
# <a name="troubleshoot-planning-optimization"></a>Suunnittelun optimoinnin vianmääritys 

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita suunnittelun optimoinnin käytössä voi esiintyä.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Suunnittelun optimoinnin lisäosa ei asennu loppuun asti

Suunnittelun optimointi edellyttää korkean käytettävyyden ympäristöä, jossa Lifecycle Services (LCS) on käytössä ja jonka taso on 2 tai korkeampi (ei OneBox-ympäristö). Käytössä on lisäksi oltava Dynamics 365 Supply Chain Managementin versio 10.0.7 tai sitä uudempi versio. Jos lisäosa yritetään asentaa OneBox-ympäristöön, asennusta ei suoriteta loppuun.

**Korjaus**: peruuta asennus ja käytä korkean käytettävyyden tason 2 tai sitä korkeampaa ympäristöä (ei OneBox-ympäristöä).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Erätöiden suunnittelu epäonnistuu, kun suunnittelun optimointi on käytössä

Kun suunnittelun optimointi otetaan käyttöön, sisäinen pääsuunnittelumoduuli poistetaan automaattisesti käytöstä. Supply Chain Managementin sisäiseen suunnittelumoduuliin luodut pääsuunnittelun erätyöt epäonnistuvat, jos ne ovat käynnistyneet suunnittelun optimoinnin ollessa käytössä. Näkyviin voi tulla esimerkiksi seuraavankaltainen virhesanoma, jonka mukaan *tämä toiminto käynnisti pääsuunnittelun, jota ei tueta, kun suunnittelun optimointi on otettu käyttöön*.

**Korjaus**: peruuta kaikki pääsuunnittelutyöt, jotka luotiin Supply Chain Managementin sisäiseen suunnittelumoduuliin.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Suunnittelun optimoinnin tulokset poikkeavat aiemmista tuloksista

Suunnittelun optimointi poikkeaa sisäisestä pääsuunnittelun rakenteesta joillakin alueilla. Myös odottavat toiminnot voivat aiheuttaa tämän.

**Korjaus**: Suorita suunnittelun optimoinnin kuntoanalyysi ja analysoi sitten tulokset samalla, kun selvität, mikä vaikutus niillä on liittyvän dokumentaation avulla. Lisätietoja on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a>Pääsuunnittelu ei ota huomioon kattavuuden aikarajaa

Tämä johtuu suunnittelun optimoinnin odottavasta toiminnosta.

**Korjaus**: poista kattavuuden aikarajan ulkopuoliset toimitusehdotukset suodattamalla tai poistamalla suunnitellut tilaukset, kunnes odottava toiminto on saatavana.

## <a name="cant-enable-planning-optimization"></a>Suunnittelun optimointia ei voi ottaa käyttöön

**Yhteystila**-arvon on oltava **Yhdistetty**, ennen kuin **Käytä suunnittelun optimointi** -asetukseksi voi määrittää **Kyllä**. Lisätietoja on kohdassa [Suunnittelun optimoinnin käytön aloittaminen](get-started.md).

**Korjaus**: varmista, että suunnittelun optimoinnin lisäosa asennettiin oikein.

## <a name="error-message-is-shown-during-ctp"></a>Saatavuuden (CTP:n) aikana näkyy virhesanoma

Jos yrittää suorittaa saatavuuden (CTP:n) myyntitilauksesta, kun suunnittelun optimointi on otettu käyttöön, näkyviin tulee seuraava virhesanoma, jonka mukaan *tämä toiminto käynnisti pääsuunnittelun, jota ei tuettu, kun suunnittelun optimointi on käytössä*.

Tämä liittyy odottavaan toimintoon, joka suunniteltu tuotantotilausten tuen osaksi.

**Korjaus:** vältä saatavuuden (CTP:n) laskelmia, kun suunnittelun optimointi on käytössä, kunnes saatavuuden (CTP:n) tuki on saatavana.

## <a name="additional-resources"></a>Lisäresurssit

[Suunnittelun optimoinnin aloittaminen](get-started.md)

[Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]