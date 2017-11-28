---
title: Suunnittele tilikarttasi
description: "Tässä artikkelissa on tietoja, joiden avulla voit suunnitella organisaation tilikartan."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 038886f0a6e1c133a33ee34725eb20352e64341a
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="plan-your-chart-of-accounts"></a>Suunnittele tilikarttasi

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja, joiden avulla voit suunnitella organisaation tilikartan.

Seuraa ja ylläpidä taloushallinnon tietoja organisaatiossa määrittämällä tilikartta. Se on tilikokoelma, joka määrittää taloudellisen kehikon. Näillä tileillä olevien tapahtumien lisäseurantaa varten voi lisätä segmenttejä, joita kutsutaan taloushallinnon dimensioiksi. Kulutili saattaa sisältää esimerkiksi taloushallinnon dimensiot nimeltä osasto, kustannuspaikka ja tarkoitus. Käyttäjän määrittämät säännöt, joita kutsutaan tilirakenteiksi ja lisäsäännöksi, määrittävät, miten nämä taloushallinnon dimensiot liitetään päätileihin ja muihin taloushallinnon dimensioihin, ja miten tapahtumia voidaan syöttää. 

Tilikartta on yrityksen kirjanpitotilien rakenteinen luettelo. Luettelon avulla valmistellaan tilinpäätökset viranomaisia ja omistajia varten. Tilit on ryhmitelty tilityyppeihin ja yhdistetty suuremmiksi luokiksi. Yleisimmällä tasolla tilit on ryhmitelty tuotoiksi ja kustannuksiksi (käyttötilit) sekä varallisuudeksi ja veloiksi (tasetilit). 

Tilikartta voidaan jakaa käytettäväksi minkä tahansa organisaation yrityksen välillä. Yrityksen käyttämä tilikartta määritetään **Kirjanpito**-sivulla. 

Tilikartan rakennetta suunniteltaessa täytyy kiinnittää huomiota esimerkiksi seuraaviin seikkoihin:

-   Organisaatiosi toimintamaassa tai toiminta-alueella voimassa olevat raportointivaatimukset
-   Oman yrityksen voimassa olevat raportointivaatimukset
-   Ulkoisten organisaatioiden ja organisaatiosi tarvitsemien tietojen tarkkuus

Voit määrittää tilikartat **Tilikartat**-sivulla. Päätilit voidaan luoda **Tilikartat**- tai **Päätilit**-sivulla. Päätileillä ei tule käyttää erikoismerkkejä, joita käytetään tilikartoissa erottimina. Jos päätilillä on erikoismerkki, jota käytetään tilikartan erottimena, toiminta saattaa olla epävakaata tai tilien ja dimensioiden yhdistelmien syöttämisessä on käytettävä jatkuvasti arvohakuja tai lisätietoikkunoita. Lisätietoja on ohjeaiheessa [Päätilin luominen](tasks/create-account-structures.md).


Päätilit kannattaa linkittää päätililuokkiin, jolloin oletusraportteja voidaan käyttää ilman muutoksia. Tällöin voit suunnitella ja ylläpitää raportteja nopeasti ja helposti. 

**Määritä tilirakenteet** -sivun avulla voit luoda tilirakenteita. Tilirakenteet määrittävät sallitut yhdistelmät. Yhdistelmät yhdessä päätilien kanssa muodostavat tilikartan.  Lisätietoja on ohjeaiheessa [Tilirakenteen luominen](tasks/create-main-account.md).

**Yrityksen ohitukset** 

Kaikki päätilit eivät kelpaa kaikille yrityksille, ja jotkin päätilit saattavat olla olennaisia vain tietyn ajanjakson ajan. Tässä skenaariossa Yrityksen ohitukset -osan avulla määritetään yritykset, joilta päätilin käyttö keskeytetään, omistaja sekä ajanjakso, jolloin dimensio on aktiivinen. Jaetun tason ohitukset eivät voi olla rajoittavampia kuin yritystason ohitukset.

Lisätietoja on seuraavissa ohjeaiheissa: [Taloushallinnon dimensiot](financial-dimensions.md)
[Lisäsääntörakenteiden luominen ja määrittäminen](tasks/create-assign-advanced-rule-structures.md)




