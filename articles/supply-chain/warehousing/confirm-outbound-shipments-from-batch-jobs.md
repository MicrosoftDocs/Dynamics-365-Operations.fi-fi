---
title: Vahvista lähtevät lähetykset erätöistä
description: Tässä ohjeaiheessa on ohjeita erätyön määrittämiseksi. Erätyö vahvistaa automaattisesti lähtevät siirtotilauslähetykset lähetysvalmiille kuormille.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652229"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Vahvista lähtevät lähetykset erätöistä

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on ohjeita erätyön määrittämiseksi. Erätyö vahvistaa automaattisesti lähtevät siirtotilauslähetykset lähetysvalmiille kuormille. Tässä kuvattu erätyö koskee vain siirtotilauslähetyksiä, ei myyntitilauksia.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Lähtevien lähetysten vahvistaminen erätöistä -ominaisuuden käyttöönotto

Ennen kuin käytät tätä toimintoa, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sivua ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa. Ominaisuus näkyy seuraavasti:

- **Moduuli** - *Varastonhallinta*
- **Ominaisuuden nimi** - *Lähtevien lähetysten vahvistaminen erätöistä*

## <a name="process-outbound-shipments"></a>Käsittele lähtevät lähetykset

Voit määrittää ajoitetun erätyön, joka suorittaa lähtevän lähetyksen vahvistuksen kuormille, jotka ovat valmiita lähetettäviksi seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Käsittele lähtevät lähetykset**.
1. **Vahvista lähetys** -valintaikkuna aukeaa. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.
1. Kyselyeditorin valintaikkuna avautuu. Valitse **Alue**-välilehdessä rivi, jolla on seuraavat arvot:
    - **Taulu** - *Kuormat*
    - **Johdettu taulu** - *Kuormat*
    - **Kenttä** - *Kuorman tila*
    - **Ehdot** - *Lastattu*
1. Valitse **OK**, jos haluat palata **Vahvista lähetys** -valintaikkunaan.
1. Määritä **Suorita taustalla** -pikavälilehdessä **Erän käsittely** -kohdan arvoksi **Kyllä**.
1. Valitse **Suorita taustalla** -pikavälilehdessä **Toistuminen**.
1. **Määritä toistuminen** -valintaikkuna aukeaa. Määritä yritykselle ajon aikataulu tarvittaessa.
1. Valitse **OK**, jos haluat palata **Vahvista lähetys** -valintaikkunaan.
1. Valitse **OK** **Vahvista lähetys** -valintaikkunassa, jos haluat lisätä erätyön eräjonoon.

Lisätietoja on kohdassa [Eräkäsittelyn yleiskatsaus](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).