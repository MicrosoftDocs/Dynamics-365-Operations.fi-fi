---
title: Viittaukset alkuperäisiin laskuihin hyvityslaskuissa
description: Tässä aiheessa kerrotaan, miten liittyvissä hyvityslaskuissa määritetään ja tulostetaan alkuperäiset laskunumerot.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d7f32c5d3d29be8d1d2742c4017c1719cbd47a8
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897329"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Viittaukset alkuperäisiin laskuihin hyvityslaskuissa

[!include [banner](../includes/banner.md)]


Joissakin maissa ja joillakin alueilla on lakisääteinen vaatimus, että tulostetut hyvityslaskut sisältävät viittauksia alkuperäisiin laskuihin. Tässä aiheessa kerrotaan, miten liittyvissä hyvityslaskuissa määritetään ja tulostetaan alkuperäiset laskunumerot.

## <a name="prerequisites"></a>Edellytykset

- Ota **Toimintohallinta**-työtilassa **Myynti- ja projektilaskuraporttien hyvityslaskutusasettelu** -ominaisuus käyttöön. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Tarvittavien tiedostojen tulostettavat muodot on konfiguroitava tulostuksenhallinnassa.

Tässä ohjeaiheessa kuvatut toiminnot koskevat seuraavia asiakirjoja:

**Myyntireskontra**

- Vapaamuotoinen hyvityslasku
- Asiakkaan hyvityslasku

**Projektinhallinta ja kirjanpito**

- Projektin hyvityslasku

## <a name="configure-accounts-receivable-parameters"></a>Myyntireskontran parametrien määrittäminen

Seuraavia ohjeita noudattamalla voit määrittää parametrin, joka määrittää, tulostetaanko liittyviin hyvityslaskuihin viitteet alkuperäisiin laskuihin.

1. Valitse **Myyntireskontra** \> **Määritys** \> **Myyntireskontran parametrit**.
2. Määritä **Päivitykset**-välilehden **Lasku**-pikavälilehdessä **Käytä myynti- ja projektilaskuraporteissa hyvityslaskutusasettelua** -asetukseksi **Kyllä**.

![Myyntireskontran parametrien määrittäminen](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Viittausten määrittäminen alkuperäisiin laskuihin

Seuraavien menetelmien avulla voit määrittää viittaukset alkuperäisiin laskuihin tiedostotyypin perusteella.

### <a name="free-text-credit-note"></a>Vapaamuotoinen hyvityslasku

1. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
2. Luo uusi hyvityslasku tai valitse aiemmin luotu hyvityslasku.
3. Avaa lasku.
4. Valitse Toimintoruudun **Laskutus**-välilehden **Toiminnot**-ryhmässä **Hyvityslaskutus**.
5. Kirjoita viittaus alkuperäiseen laskuun ja valitse korjauksen syy.

![Vapaatekstilaskun viitteen määrittäminen](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Asiakkaan hyvityslasku

1. Valitse **Myyntireskontra** \> **Tilaukset** \> **Kaikki myyntitilaukset**.
2. Valitse ja avaa laskutettu myyntitilaus, joka on korjattava.
3. Valitse Toimintoruudun **Myynti**-välilehden **Hyvityslasku**-ryhmässä **Hyvityslasku**.
4. Anna korjauksen syy. Viittaus alkuperäiseen laskuun määritetään automaattisesti.

![Myyntitilauksen viitteen määrittäminen](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Projektin hyvityslasku

1. Valitse **Projektinhallinta ja kirjanpito** \> **Projektin laskut** \> **Projektin laskut**.
2. Valitse ja avaa projektilasku, joka on korjattava.
3. Valitse Toimintoruudun **Projektilasku**-välilehden **Toiminnot**-ryhmässä **Valitse hyvityslaskua varten**.
4. Valitse **Hyvityslaskutus**.
5. Anna korjauksen syy. Viittaus alkuperäiseen laskuun määritetään automaattisesti.

![Projektilaskun viitteen määrittäminen](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Hyvityslaskujen tulostaminen

Kun tulostat vapaateksti-, asiakas- ja projektihyvityslaskuja, ne sisältävät viitteen alkuperäiseen laskuun sekä korjauksen syyn.

![Tulostettu hyvityslasku](media/credit-note-FTI.jpg)

> [!NOTE]
> Varmista, että tiedostojen tulostettavat muodot on määritetty oikein sillä olettamuksella, että viitteet alkuperäisiin laskuihin tulostetaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]