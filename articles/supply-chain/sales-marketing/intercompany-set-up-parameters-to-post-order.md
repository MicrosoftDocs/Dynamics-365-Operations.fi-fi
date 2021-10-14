---
title: Konsernin sisäisen tilauksen kirjausparametrien määrittäminen
description: Tässä aiheessa käsitellään konsernin sisäisen tilauksen kirjausparametrien määrittämistä
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c728f2f491948ae1c8550396ba4d72f76f46fe85
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548238"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>Konsernin sisäisen tilauksen kirjausparametrien määrittäminen

[!include [banner](../../includes/banner.md)]

Kun konsernin sisäisen myyntilasku kirjataan, sen voi määrittää niin, että sekä konsernin sisäinen ostotilaus että alkuperäinen myyntilasku kirjataan automaattisesti.

> [!NOTE]
> Ennen tämän menettelyn suorittamista on tulostuksen hallinta on määritettävä organisaatiossa osoittamaan oikeaan laskutulostimeen. Näin varmistetaan, että alkuperäisen myyntitilauksen lasku tulostetaan oikeassa tulostimessa.

Seuraavat parametrit on määritettävä:

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**. Valitse käsiteltävä myyntitilaus.
1. Valitse myyntitilauksen toimintoruudussa **Otsikkonäkymä**. Valitse sitten **Konsernin sisäiset asetukset** -pikavälilehti ja avaa se.
1. Siirry toimintoruudussa **Myyntitilaus**-välilehteen ja valitse **Muokkaa**.
1. Palaa **Konsernin sisäiset asetukset** -pikavälilehteen ja valitse **Suoratoimitus**. Tällä tavoin suoratoimitus otetaan käyttöön konsernin koko sisäisessä tilauksessa (kaikki tilaukset).
1. Tallenna myyntitilaus ja uusi asetus valitsemalla **Tallenna**. Sulje myyntitilaus sitten valitsemalla **Sulje**.
1. Valitse **Hankinta \> Toimittajat \> Kaikki toimittajat**. Valitse **Yleiset**-välilehdessä **Konsernin sisäinen**.
1. Valitse **Konsernin sisäinen**-sivulla **Ostotilauskäytännöt**-linkki. Valitse **Konsernin sisäinen ostotilaus (suoratoimitus)** -kenttäryhmässä **Kirjaa lasku automaattisesti** ja poista **Tulosta lasku automaattisesti** -kentän valintamerkki.
1. Valitse **Alkuperäinen myyntitilaus (suoratoimitus)** -kenttäryhmässä **Kirjaa lasku automaattisesti** -kenttä ja **Tulosta lasku automaattisesti** -kenttä.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
