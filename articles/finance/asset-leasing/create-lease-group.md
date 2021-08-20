---
title: Vuokraryhmän luominen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää vuokraryhmät. Vuokraryhmät ovat pakollisia uusien vuokrasopimusten luomiseksi.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5ff4892408aa87214231762452c195274192447512525ae9c1f08dad8e318076
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728100"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
