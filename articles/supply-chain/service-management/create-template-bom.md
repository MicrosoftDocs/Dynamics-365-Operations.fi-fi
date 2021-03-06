---
title: Mallituoterakenteen luominen
description: Mallituoterakenteen voi luoda monella eri tavalla.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 781df7611ec1e3ee9d3013f971232700df38ada0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836299"
---
# <a name="create-a-template-bom"></a>Mallituoterakenteen luominen   

[!include [banner](../includes/banner.md)]


Mallituoterakenteen voi luoda millä tahansa seuraavista menetelmistä. Kaikissa menetelmissä **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kentät ovat valinnaisia ja vain tiedoksi.

## <a name="create-a-template-bom-manually"></a>Mallituoterakenteen luominen manuaalisesti

1.  Avaa **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.

2.  Valitse **Uusi** avataksesi **Luo mallituoterakenne** -lomakkeen.

3.  Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Manuaalinen**-vaihtoehto.

4.  Syötä **Nimikenumero**-kenttään **Tuoterakenne**-tyyppinen nimike.

5.  Kirjoita **Nimi**-kenttään mallin nimi.

6.  Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.

7.  Valitse **OK**.

Järjestelmä luo uuden tyhjän mallituoterakenteen.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Mallituoterakenteen luominen toisen mallituoterakenteen perusteella

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.

2.  Valitse **Uusi** avataksesi **Luo mallituoterakenne** -lomakkeen.

3.  Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Mallituoterakenne**-vaihtoehto.

4.  Valitse **Viitenumero**-kentässä aiemmin luotu mallituoterakenne, jonka haluat kopioida uuteen mallituoterakenteeseen.

5.  Kirjoita **Nimi**-kenttään mallin nimi.

6.  Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.

7.  Valitse **OK**.

Järjestelmä luo uuden mallituoterakenteen käyttämällä rivejä, jotka vastaavat alkuperäistä mallituoterakennetta.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Mallituoterakenteen luominen nimikkeen tuoterakenteen perusteella

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.

2.  Valitse **Uusi** avataksesi **Luo mallituoterakenne** -lomakkeen.

3.  Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Tuoterakenne**.

4.  Valitse **Viitenumero**-kentässä tuoterakenteen versio. Tuoterakenne-tyyppinen nimike kopioidaan kohtaan **Nimikenumero**.

5.  Kirjoita **Nimi**-kenttään mallin nimi.

6.  Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.

7.  Valitse **OK**.

Uusi mallituoterakenne luodaan käyttämällä rivejä, jotka vastaavat **Tuoterakenteet**-kohdassa mainitun tuoterakenteen rivejä.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Mallituoterakenteen luominen tuotannon tuoterakenteen perusteella

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.

2.  Valitse **Uusi** avataksesi **Luo mallituoterakenne** -lomakkeen.

3.  Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Tuotanto**.

4.  Valitse **Viitenumero**-kentässä tuotannon tuoterakenne.

5.  Kirjoita **Nimi**-kenttään mallin nimi.

6.  Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.

7.  Valitse **OK**.

Uusi mallituoterakenne luodaan käyttämällä rivejä, jotka vastaavat **Tuoterakenne**-kohdassa mainitun tuoterakenteen rivejä.

## <a name="see-also"></a>Lisätietoja

[Mallituoterakenteet ](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]