---
title: Resurssin vuokrauksen maksuaikataulujen vahvistaminen eräprosessina
description: Tässä artikkelissa kerrotaan, kuinka useita maksuaikatauluja vahvistetaan eräprosessina.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd75e22f6407d6bc25a78c1dfeacf70022238e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895048"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Resurssin vuokrauksen maksuaikataulujen vahvistaminen eräprosessina

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, kuinka useita maksuaikatauluja vahvistetaan eräprosessina. Maksuaikataulut vahvistetaan joko vuokrasopimuksittain tai vahvistuseräprosessin avulla. Kirjauskansiovienti voidaan kirjata vain vuokrasopimukselle, jolla on vahvistettu maksuaikataulu. Maksuaikataulun vahvistainen toimii vuokrasopimuksen taloustietojen lopullisena hyväksyntänä. Kaikkia vuokrasopimuksen taloudellisten tietojen tulevia muutoksia, kuten maksuja ja vuokra-aikoja, pidetään vuokrasopimuksen oikaisuina. Ne on käsiteltävä oikaisuina.

Voit vahvistaa useita maksuaikatauluja noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Resurssin vuokraus \> Kausittainen \> Vahvistuserä**.
2. Valitse **Vahvistuserä**-sivulla **Vahvistuserä**.
3. Suodata näkyviin tulevassa valintaikkunassa ne kirjat, jotka haluat vahvistaa.

    - Voit vahvistaa kaikki tietyn vuokraryhmän kirjat valitsemalla ryhmän **Vuokraryhmä**-kentässä.
    - Vahvista tietyt kirjat valitsemalla kirjat **Kirjan tunnus**-kentästä.
    - Vahvista kaikki kirjat ottamalla käyttöön **Kaikille kirjoille** -parametri.

Juuri vahvistettujen kirjojen tiedot näkyvät **Vahvistetut kirjat** -sivulla. Kun maksuaikataulut on vahvistettu, alkuperäiset tuloutuksen kirjauskansioviennit voidaan kirjata vuokrauksille.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
