---
title: Tilikartan suunnittelu
description: Tässä ohjeaiheessa on tietoja, joiden avulla voit suunnitella organisaation tilikartan.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26f7ca1fa539fb0cf69a7759e92c5e735bd41211
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846772"
---
# <a name="plan-your-chart-of-accounts"></a>Tilikartan suunnittelu

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja, joiden avulla voit suunnitella organisaation tilikartan.

Seuraa ja ylläpidä taloushallinnon tietoja organisaatiossa määrittämällä tilikartta. Se on tilikokoelma, joka määrittää taloudellisen kehikon. Voit parantaa näiden tilien tapahtumien seurantaa lisäämällä segmenttejä. Näitä segmenttejä kutsutaan taloushallinnon dimensioiksi. Kulutili saattaa sisältää esimerkiksi taloushallinnon dimensiot nimeltä osasto, kustannuspaikka ja tarkoitus. Käyttäjän määrittämät säännöt määrittävät, miten nämä taloushallinnon dimensiot liitetään päätileihin ja muihin taloushallinnon dimensioihin sekä miten tapahtumat kirjataan. Käyttäjän määrittämä sääntöjä kutsutaan myös tilirakenteeksi ja lisäsäännöiksi.

Tilikartta on yrityksen kirjanpitotilien rakenteinen luettelo. Luettelon avulla valmistellaan tilinpäätökset viranomaisia ja omistajia varten. Tilit on ryhmitelty ensin tilityyppeihin ja yhdistetty sitten suuremmiksi luokiksi. Yleisimmällä tasolla tilit on ryhmitelty tuotoiksi ja kustannuksiksi (käyttötilit) sekä varallisuudeksi ja veloiksi (tasetilit).

Tilikartta voidaan jakaa käytettäväksi minkä tahansa organisaation yrityksen välillä. Yrityksen käyttämä tilikartta määritetään **Kirjanpito**-sivulla.

Tilikartan rakennetta suunniteltaessa täytyy kiinnittää huomiota esimerkiksi seuraaviin seikkoihin:

- Organisaatiosi toimintamaassa tai toiminta-alueella voimassa olevat raportointivaatimukset
- Oman yrityksen voimassa olevat raportointivaatimukset
- Ulkoisten organisaatioiden ja organisaatiosi tarvitsemien tietojen tarkkuus

Voit luoda tilikarttoja **Tilikartat**-sivulla. Voit luoda päätilejä **Tilikartat**- tai **Päätilit**-sivulla. Päätileillä ei tule käyttää erikoismerkkejä, joita käytetään tilikartoissa erottimina. Muussa tapauksena seurauksena voi olla toiminnan epävakautta tai tilien ja dimensioiden yhdistelmien kirjaamiseen on ehkä aina käytettävä hakua ja valintaikkunaa. Lisätietoja on ohjeaiheessa [Päätilin luominen](tasks/create-main-account.md).

> [!NOTE]
> Voit muokata tilikartan erotinta Microsoft Dynamics for Finance and Operationsin version 8.0 (huhtikuu 2018) **Kirjanpitoparametrit**-sivulla.

Päätilit kannattaa linkittää päätililuokkiin, jolloin oletusraportteja voidaan käyttää ilman muutoksia. Tällöin voit suunnitella ja ylläpitää raportteja nopeasti ja helposti.

Voit luoda tilirakenteita **Määritä tilirakenteet** -sivulla. Tilirakenteet määrittävät sallitut yhdistelmät. Nämä yhdistelmät yhdessä päätilien kanssa muodostavat tilikartan. Lisätietoja on ohjeaiheessa [Tilirakenteen luominen](tasks/create-account-structures.md).

**Yrityksen ohitukset**

Kaikki päätilit eivät kelpaa kaikille yrityksille ja tietty päätili saattaa olla tarpeellinen vain tietyn kauden ajan. Tässä skenaariossa voit määrittää **Yrityksen ohitukset** -osassa yritykset, joissa päätilin käyttö pitäisi keskeyttää, omistajan sekä kauden, jolloin dimensio on aktiivinen. Jaetun tason ohitukset eivät voi olla rajoittavampia kuin yritystason ohitukset.

Lisätietoja on seuraavissa aiheissa:

- [Taloushallinnon dimensiot](financial-dimensions.md)
- [Luo ja määritä lisäsääntörakenteet](tasks/create-assign-advanced-rule-structures.md)
