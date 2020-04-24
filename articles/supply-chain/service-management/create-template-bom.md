---
title: Mallituoterakenteen luominen
description: Mallituoterakenteen voi luoda monella eri tavalla.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 815b6b726e9a76a9294995bc5689b030cf623ec0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202580"
---
# <a name="create-a-template-bom"></a>Mallituoterakenteen luominen   

[!include [banner](../includes/banner.md)]


Mallituoterakenteen voi luoda millä tahansa seuraavista menetelmistä. Kaikissa menetelmissä **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kentät ovat valinnaisia ja vain tiedoksi.

## <a name="create-a-template-bom-manually"></a>Mallituoterakenteen luominen manuaalisesti

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.

2.  Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.

3.  Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Manuaalinen**-vaihtoehto.

4.  Syötä **Nimikenumero**-kenttään **Tuoterakenne**-tyyppinen nimike.

5.  Kirjoita **Nimi**-kenttään mallin nimi.

6.  Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.

7.  Napsauta **OK**.

Järjestelmä luo uuden tyhjän mallituoterakenteen.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Mallituoterakenteen luominen toisen mallituoterakenteen perusteella

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.

2.  Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.

3.  Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Mallituoterakenne**-vaihtoehto.

4.  Valitse **Viitenumero**-kentässä aiemmin luotu mallituoterakenne, jonka haluat kopioida uuteen mallituoterakenteeseen.

5.  Kirjoita **Nimi**-kenttään mallin nimi.

6.  Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.

7.  Napsauta **OK**.

Järjestelmä luo uuden mallituoterakenteen käyttämällä rivejä, jotka vastaavat alkuperäistä mallituoterakennetta.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Mallituoterakenteen luominen nimikkeen tuoterakenteen perusteella

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.

2.  Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.

3.  Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Tuoterakenne**.

4.  Valitse **Viitenumero**-kentässä tuoterakenteen versio. Tuoterakenne-tyyppinen nimike kopioidaan kohtaan **Nimikenumero**.

5.  Kirjoita **Nimi**-kenttään mallin nimi.

6.  Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.

7.  Napsauta **OK**.

Uusi mallituoterakenne luodaan käyttämällä rivejä, jotka vastaavat **Tuoterakenteet**-kohdassa mainitun tuoterakenteen rivejä.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Mallituoterakenteen luominen tuotannon tuoterakenteen perusteella

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.

2.  Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.

3.  Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Tuotanto**.

4.  Valitse **Viitenumero**-kentässä tuotannon tuoterakenne.

5.  Kirjoita **Nimi**-kenttään mallin nimi.

6.  Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.

7.  Napsauta **OK**.

Uusi mallituoterakenne luodaan käyttämällä rivejä, jotka vastaavat **Tuoterakenne**-kohdassa mainitun tuoterakenteen rivejä.

## <a name="see-also"></a>Lisätietoja

[Mallituoterakenteet ](template-boms.md)

  


