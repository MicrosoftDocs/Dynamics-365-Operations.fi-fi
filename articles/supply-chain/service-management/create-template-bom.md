---
title: Mallituoterakenteen luominen
description: Mallituoterakenteen voi luoda monella eri tavalla.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 169b54a0509a2e11ce2e888404da10fd81db475e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678203"
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