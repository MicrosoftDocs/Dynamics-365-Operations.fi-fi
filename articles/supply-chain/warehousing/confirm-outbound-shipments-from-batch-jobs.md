---
title: Vahvista lähtevät lähetykset erätöistä
description: Tässä artikkelissa on ohjeita erätyön määrittämiseksi. Erätyö vahvistaa automaattisesti lähtevät siirtotilauslähetykset lähetysvalmiille kuormille.
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
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 00749a69b17b0064290d7b41ccb2171386716302
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875098"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Vahvista lähtevät lähetykset erätöistä

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on ohjeita erätyön määrittämiseksi. Erätyö vahvistaa automaattisesti lähtevät siirtotilauslähetykset lähetysvalmiille kuormille. Tässä kuvattu erätyö koskee vain siirtotilauslähetyksiä, ei myyntitilauksia.

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>Lähtevien lähetysten vahvistaminen erätöistä -ominaisuuden käyttöönotto tai käytöstä poisto

Tässä artikkelissa kuvatun toiminnon käyttäminen edellyttää, että *Vahvista lähtevät lähetykset erätöistä* -toiminto on käytössä järjestelmässäsi. Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.25, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Vahvista lähtevät lähetykset erätöistä* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

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