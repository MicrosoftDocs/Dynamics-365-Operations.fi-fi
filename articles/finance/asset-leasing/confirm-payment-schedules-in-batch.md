---
title: Resurssin vuokrauksen maksuaikataulujen vahvistaminen eräprosessina
description: Tässä ohjeaiheessa kerrotaan, kuinka useita maksuaikatauluja vahvistetaan eräprosessina.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9c680ea16e9f64107fde081c7e7763697356dcc1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971375"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Resurssin vuokrauksen maksuaikataulujen vahvistaminen eräprosessina

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka useita maksuaikatauluja vahvistetaan eräprosessina. Maksuaikataulut vahvistetaan joko vuokrasopimuksittain tai vahvistuseräprosessin avulla. Kirjauskansiovienti voidaan kirjata vain vuokrasopimukselle, jolla on vahvistettu maksuaikataulu. Maksuaikataulun vahvistainen toimii vuokrasopimuksen taloustietojen lopullisena hyväksyntänä. Kaikkia vuokrasopimuksen taloudellisten tietojen tulevia muutoksia, kuten maksuja ja vuokra-aikoja, pidetään vuokrasopimuksen oikaisuina. Ne on käsiteltävä oikaisuina.

Voit vahvistaa useita maksuaikatauluja noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Resurssin vuokraus \> Kausittainen \> Vahvistuserä**.
2. Valitse **Vahvistuserä**-sivulla **Vahvistuserä**.
3. Suodata näkyviin tulevassa valintaikkunassa ne kirjat, jotka haluat vahvistaa.

    - Voit vahvistaa kaikki tietyn vuokraryhmän kirjat valitsemalla ryhmän **Vuokraryhmä**-kentässä.
    - Vahvista tietyt kirjat valitsemalla kirjat **Kirjan tunnus**-kentästä.
    - Vahvista kaikki kirjat ottamalla käyttöön **Kaikille kirjoille** -parametri.

Juuri vahvistettujen kirjojen tiedot näkyvät **Vahvistetut kirjat** -sivulla. Kun maksuaikataulut on vahvistettu, alkuperäiset tuloutuksen kirjauskansioviennit voidaan kirjata vuokrauksille.
