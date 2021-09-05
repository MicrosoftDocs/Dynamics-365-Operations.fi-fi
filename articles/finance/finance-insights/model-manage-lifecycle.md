---
title: Mallien hallinnan elinkaari
description: Tässä ohjeaiheessa kuvataan tapoja ylläpitää organisaation koneoppimismalleja niiden luomien ennusteiden optimoimiseksi.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 28a5451f4932669fb66d5e47fd2f574eb3648428
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386335"
---
# <a name="model-management-lifecycle"></a>Mallien hallinnan elinkaari

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan tapoja ylläpitää organisaation koneoppimismalleja niiden luomien ennusteiden optimoimiseksi.

Suosittelemme, että koulutat tekoälymallia eristysympäristössä ja käytät sitten hallittuja ratkaisuja ottaaksesi sen käyttöön tuotantoympäristössä. Tämä lähestymistapa auttaa varmistamaan, että oikeat ohjausobjektit ovat paikallaan mallin elinkaaren hallintaa varten.

Koska tekoälymalli perustuu käytettävissä oleviin lasku- ja asiakastietoihin, on tärkeää, että eristysympäristössä on tuore kopio tuotantotiedoista. Voit aloittaa mallisi kouluttamisen noudattamalla kohdassa [Asiakkaan maksuennusteiden käyttäminen](use-customer-payment-predictions.md) kuvattuja ohjeita. Kun malli on koulutettu uudelleen, arvioi tulokset kohdassa [Asiakkaan alkuperäisen maksuennustemallin arvioiminen](evaluate-payment-prediction.md) kuvatulla tavalla. Käytä kohdassa [Ennustemallin parantaminen](improve-model.md) kuvattuja tietoja kokeillaksesi ominaisuuksien ja suodattimien yhdistelmiä, jotka voivat auttaa parantamaan mallia.

Kun olet tyytyväinen koulutuksen tuloksiin, noudata kohdassa [Tekoälymallin jakaminen](https://docs.microsoft.com/ai-builder/distribute-model) kuvattuja ohjeita siirtääksesi mallin tuotantoympäristöösi.
