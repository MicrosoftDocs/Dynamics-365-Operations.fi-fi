---
title: Vahvista lähtevät lähetykset erätöistä
description: Tässä ohjeaiheessa on ohjeita erätyön määrittämiseksi. Erätyö vahvistaa automaattisesti lähtevät siirtotilauslähetykset lähetysvalmiille kuormille.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 69e61e1c04dd72efbe1d2f028c078100e07176f6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838439"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]