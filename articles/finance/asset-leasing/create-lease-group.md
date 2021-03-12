---
title: Vuokraryhmän luominen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää vuokraryhmät. Vuokraryhmät ovat pakollisia uusien vuokrasopimusten luomiseksi.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2c06f6f943c8a47fbe650a67017b95d799914a0e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971350"
---
# <a name="create-a-lease-group"></a>Vuokraryhmän luominen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää vuokraryhmät. Vuokraryhmät ovat pakollisia uusien vuokrasopimusten luomiseksi. Vuokrasopimuskirjat liittyvät kuhunkin vuokraryhmään. Vuokrasopimusryhmät määrittävät oletuskirjat, jotka jokaiselle vuokrasopimukselle on luotava. Voit määrittää erityistilejä vuokraryhmälle **Vuokrasopimuksen kirjauksen parametrit** -sivulla.

## <a name="create-a-lease-book-and-add-a-lease-group"></a>Vuokrasopimuskirjan luominen ja vuokraryhmän lisääminen

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Vuokraryhmät**.
2. Lisää vuokraryhmä valitsemalla toimintoruudussa **Uusi**. Rivi lisätään ruudukkoon.
3. Syötä **Vuokraryhmä**-kentän uudelle riville arvo.
4. Anna arvo **Kuvaus**-kentässä.

Juuri syöttämäsi tiedot lisätään **Vuokraryhmä**-kenttään **Lisää vuokrasopimus** -sivulla.

## <a name="associate-a-book-with-a-lease-group"></a>Kirjan liittäminen vuokraryhmään

Kun olet luonut vuokraryhmiä, voit liittää kirjoja kuhunkin ryhmään. Kun luot vuokrasopimuksen ja määrität sen vuokraryhmälle, järjestelmä luo kullekin kyseiseen vuokraryhmään liittyvälle kirjalle aikataulujoukon.

> [!NOTE]
> Kirjat on määritettävä, ennen kuin ne voidaan liittää vuokraryhmään.

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Vuokraryhmä**.
2. Valitse vuokraryhmä ja valitse sitten **Kirjat**.
3. Valitse **Uusi** ja valitse sitten **Kirjan tyyppi** -kentässä vuokraryhmään liitettävä kirja. Voit liittää vuokraryhmään useita kirjoja, jos vuokrasopimus on otettava huomioon eri tavoin.
