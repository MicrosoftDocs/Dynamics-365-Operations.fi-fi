---
title: Kustannuslaskentapalvelun käytön aloittaminen (yksityinen esiversio)
description: Tässä ohjeaiheessa on kustannuslaskentapalvelun käyttöoikeustiedot ja asennusohjeet.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: a82af9e8ec1806f470103897389d0316d33a4a06
ms.sourcegitcommit: 7fec9dc5297ed6e687d4a0dff099922d59d6a830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/13/2020
ms.locfileid: "3372733"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a>Kustannuslaskentapalvelun käytön aloittaminen (yksityinen esiversio)

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> Tässä ohjeaiheessa kuvatut toiminnot ovat saatavilla käyttöön yksityisen ennakkoversion osana. Tämän ohjeaiheen sisältö ja sen kuvaamien toimintojen muutokset saattavat muuttua. Lisätietoja ennakkojulkaisusta on kohdassa [Yhden version palvelupäivitysten usein kysytyt kysymykset](../../fin-ops-core/fin-ops/get-started/one-version.md).

Kustannuslaskentapalvelun avulla voit suorittaa useita varastokirjanpitoja määrittämissäsi kustannuslaskentarekistereissä. Kukin kustannuslaskentatapahtuma liitetään *käytäntöön*. Yleissopimus on kokoelma seuraavantyyppisiä kirjanpitokäytäntöjä:

- Kustannusobjekti
- Syötteen mittaperuste
- Kustannusvirran oletus
- Kustannustaso

> [!NOTE]
> Vaikka olet ottanut kustannuslaskentapalvelun käyttöön, voit silti tehdä varastokirjanpidon Microsoft Dynamics 365 Supply Chain Management -ohjelmassa tavalliseen tapaan.

Kustannuslaskentapalvelu on apuohjelma. Jos haluat käyttää sen toimintoja, sinun on asennettava se Microsoft Dynamics Lifecycle Servicesistä (LCS). Tämän vuoksi voit valita, että se arvioidaan testiympäristössä, ennen kuin otat sen käyttöön tuotantoympäristöissä.

Kustannuslaskentapalvelu ei tällä hetkellä tue kaikkia Dynamics 365 Supply Chain Managementin sisäänrakennettuja kustannustenhallintatoimintoja. Tämän vuoksi on tärkeää arvioida, vastaako tällä hetkellä käytössä oleva toimintojoukko tarpeitasi.

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a>Kustannuslaskentapalvelun hankkiminen (yksityinen esiversio)

> [!IMPORTANT]
> Kustannuslaskentapalvelun käyttäminen edellyttää, että käytössä on LCS-yhteensopiva korkean käytettävyyden ympäristö (ei OneBox-ympäristö) ja että käytössä on Dynamics 365 Supply Chain Managementin versio 10.0.11 tai uudempi.

Kustannuslaskentapalvelun yksityiseen esiversioon kirjaudutaan lähettämällä LCS-ympäristön tunnus sähköpostitse [kustannuslaskentapalveluun (yksityinen esikatselu)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29). Kun sinut hyväksytään ohjelmaan, saat seurantasähköpostin, jossa on kustannuslaskentapalvelun beeta-avain. Kun olet saanut beeta-avaimen, voit jatkaa [lisäosan asentamiseen](#install).

## <a name="licensing"></a>Käyttöoikeudet

Kustannuslaskentapalvelu on lisensoitu yhdessä Supply Chain Managementin käytettävissä olevien varastokirjanpidon vakiotoimintojen kanssa. Sinun ei tarvitse ostaa lisäkäyttöoikeutta, jotta voisit käyttää kustannuslaskentapalvelua.

## <a name="install-the-add-in"></a><a name="install"></a>Lisäosan asentaminen

Jos haluat käyttää kustannuslaskentapalvelua, asenna kustannuslaskentapalvelun apuohjelma Supply Chain Managementia varten seuraavassa kuvatulla tavalla.

1. [Kirjaudu](#sign-up) kustannuslaskentapalveluun (yksityinen esiversio).

1. Kirjaudu sisään LCS:ään.

1. Mene kohtaan **Toimintojen hallinnan esiversio**.

1. Valitse plusmerkki (**+**).

1. Syötä **Koodi**-kenttään kustannuslaskentapalvelun apuohjelman beeta-avain. (Sinun olisi pitänyt vastaanottaa avaimesi sähköpostilla.)

1. Valitse **Poista esto**.

1. Avaa LCS-ympäristö, johon haluat lisätä palvelun.

1. Valitse **Kaikki tiedot**.

1. Vieritä alas **Ympäristön lisäosat** -pikavälilehteen.

1. Valitse **Asenna uusi lisäosa**.

1. Valitse **Kustannuslaskentapalvelu**.

1. Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.

1. Valitse **Asenna**.

1. **Ympäristön apuohjelmat** -pikavälilehdessä näkyy, että kustannuslaskentapalvelua asennetaan. Muutaman minuutin kuluttua tilan pitäisi muuttua tilasta **Asennetaan** tilaan **Asennettu**. (Sivu on ehkä päivitettävä, jotta näet tämän muutoksen.) Tässä vaiheessa kustannuslaskentapalvelu on valmis käytettäväksi.

## <a name="set-up-the-integration"></a>Määritä integraatio

Voit määrittää kustannuslaskentapalvelun ja Dynamics 365 Supply Chain Managementin integroinnin seuraavasti:

1. Siirry kohtaan **Järjestelmänhallinta > Ominaisuuksien hallinta**.

1. Valitse **Tarkista päivitysten saatavuus**.

1. Avaa **Kaikki**-välilehti ja etsi toiminto, jonka nimi on *Kustannuslaskentapalvelu*.

1. Valitse **Ota käyttöön nyt**.

1. Siirry kohtaan **Kustannusten hallinta > Kustannuslaskentapalvelu > Asetukset > Kustannuslaskentapalvelun parametrit > Integrointien parametrit**.

1. Syötä **Sovellustunnus**-kenttään seuraava koodi:<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. Kirjoita **Tietopalvelun päätepiste** -kenttään seuraava URL-osoite:<br>https://operationsdataservice.operations365.dynamics.com/

1. Kirjoita **Kustannuslaskentapalvelun päätepiste** -kenttään seuraava URL-osoite:<br>https://costaccountingservice.operations365.dynamics.com/

1. Kustannuslaskentapalvelu on nyt valmis käytettäväksi.

## <a name="related-resources"></a>Liittyvät resurssit

[Kustannuslaskentapalvelun aloitussivu](cost-accounting-service-home.md)
