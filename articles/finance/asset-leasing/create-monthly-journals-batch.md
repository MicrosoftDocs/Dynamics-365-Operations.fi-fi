---
title: Kuukausittaisten kirjauskansiovientien luominen erätoimintona
description: Tässä ohje aiheessa selitetään, kuinka kirjauskansiovientejä luodaan eräprosessina. Tämä lisää tehokkuutta, kun kuukausittaiset vuokrakulut tallennetaan.
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
ms.openlocfilehash: 7f46f289c58c32c535dd20fb510cf2812625c49c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971325"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>Kuukausittaisten kirjauskansiovientien luominen erätoimintona

[!include [banner](../includes/banner.md)]

Tässä ohje aiheessa selitetään, kuinka kirjauskansiovientejä luodaan eräprosessina. Tämä lisää tehokkuutta, kun kuukausittaiset vuokrakulut tallennetaan. Eräkäsittelyn avulla voidaan luoda kirjauskansiovientejä useista aikatauluista. Näitä kirjauskansiovientejä voivat olla maksut, velan kuoletus, käyttöoikeusomaisuuserän kuoletus ja toimeenpanokustannusten kulut. Eräkäsittelyn avulla voit myös tehdä useiden vuokrasopimusten alkuperäisen tuloutuksen samanaikaisesti tai luoda useita siirtymäoikaisuja useille vuokrasopimuksille samanaikaisesti.

Jos haluat määrittää erätyön tai käsitellä useiden vuokrasopimusten laskut, poistot tai korot, siirry kohtaan **Resurssin vuokraus \> Kausittainen \> Eräkirjauskansion luominen**. Näyttöön tulevassa valintaikkunassa voit valita aikataulun, josta kirjauskansioviennit tulee luoda. Voit myös määrittää, suoritetaanko eräkäsittely tietyille entiteeteille, vuokraryhmille vai vuokrasopimuskirjoille.

> [!NOTE]
> Seuraavat tapahtumat, kuten velan kuoletusaikataulut, maksut, poistot ja kulut, kirjataan vasta, kun vastaavien vuokrasopimusten alkuperäinen tuloutus on kirjattu.
>
> Kirjauskansioviennit luodaan, mutta niitä ei kirjata, ennen kuin valitset **Suorita**-komennon.
