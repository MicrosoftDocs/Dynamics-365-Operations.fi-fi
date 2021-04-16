---
title: Hinnoitteluprofiilit
description: Tässä aiheessa käsitellään hinnoitteluprofiilien tietojen määrittämisestä.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d359394ee0086edc5c8b9a3a0c48cf5933963ceb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828439"
---
# <a name="rating-profiles"></a>Hinnoitteluprofiilit

Hinnoitteluprofiili muistuttaa logistista sopimusta (mutta ei juridista sopimusta). Sitä käytetään määrittämään kuormien kuljetusmaksut. 

Hinnoitteluprofiilit ovat rahdinkuljettajakohtaisia. Hinnoitteluprofiilissa rahdinkuljettaja liitetään hinnoittelun perustietoihin. Hinnan päätiedot määrittävät hintaperusteen määritykset ja hintaperusteen Hintaperuste määrittää rahdinkuljettajan hinnan.

Voit määrittää hinnoitteluprofiilin käyttämällä yleistä sivua, jossa on yhteenveto kaikista aiemmista luokituksen profiileista. Vaihtoehtoisesti voit määrittää hinnoittelun profiilin suoraan lähetyksen rahdinkuljettajalta. Molemmissa tapauksissa hinnoitteluprofiilille määritetyt tiedot ovat samat.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>Hinnoitteluprofiilin luominen tai muokkaaminen Hinnoitteluprofiilit-sivulla

Voit tarkastella kaikkia käytettävissä olevia hinnoitteluprofiileja **Hinnoitteluprofiilit**-sivulla. Voit myös muokata aiemmin luotuja profiileja ja luoda uusia profiileja.

1. Valitse **Kuljetustenhallinta \> Määritys \> Luokitus \> Hinnoitteluprofiili**.
1. Lisää uusi hinnoitteluprofiili ruudukkoon valitsemalla toimintoruudussa **Uusi** tai muokkaa aiemmin luotua profiilia valitsemalla **Muokkaa**.
1. Määritä seuraavat kentät uuden tai aiemmin luodun hinnoitteluprofiilin rivillä:

    - **Hinnoitteluprofiili** – anna hinnoitteluprofiilin yksilöivä tunniste.
    - **Nimi** – anna hinnoitteluprofiilin kuvaava nimi.
    - **Rahdinkuljettaja** – Valitse rahdinkuljettaja. Määritettävä hinnoitteluprofiili näkyy myös valitun rahdinkuljettajan **Rahdinkuljettajat**-sivulla.
    - **Toimipaikka** ja **Varasto** – valitse toimipaikka ja varasto.
    - **Hinnan laskenta** – valitse hinnoitteluprofiilin hinnan laskenta.
    - **Hinnan päätiedot** – Valitse hinnoitteluprofiilin hinnan päätiedot. Voit käyttää hinnan päätietoja hintaperusteen tyypin ja hintaperusteen määrittämiseen. Lisätietoja on kohdassa [Hinnan päätietojen määrittäminen](set-up-rate-masters.md).
    - **Siirtoajan laskenta** – valitse hinnoitteluprofiilin siirtoajan laskenta.
    - **Rahdinkuljettajan polttoaineindeksi** – valitse hinnoitteluprofiilin rahdinkuljettajan polttoaineindeksi.
    - **Voimaantulon aloituspäivä ja -aika** ja **Voimaantulon päättymispäivä ja -aika** – määritä jakso, jolloin hinnoitteluprofiilin on oltava aktiivinen.

1. Valitse toimintoruudussa **Tallenna**.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>Hinnoitteluprofiilin luominen suoraan Rahdinkuljettajat-sivulla

1. Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Lähetyksen rahdinkuljettajat**.
1. Valitse rahdinkuljettaja luettelossa.
1. Luo hinnoitteluprofiili valitsemalla **Hinnoitteluprofiilit**-pikavälilehdessä **Uusi**.
1. Määritä uuden hinnoitteluprofiilin kentät. Nämä kentät vastaavat **Hinnoitteluprofiilit**-sivun kenttiä tämän aiheen edellisessä osassa kuvatulla tavalla.

> [!NOTE]
> **Rahdinkuljettajat**-sivulla luodut profiilit näkyvät myös **Hinnoitteluprofiilit**-sivulla.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]