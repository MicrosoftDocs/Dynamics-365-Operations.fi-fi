---
title: Taloushallinnon dimensiot ja päätilit oikealta vasemmalle kirjoitettavilla kielillä
description: Tässä aiheessa käsitellään päätöksiä, joita on tehtävä käytettäessä oikealta vasemmalle kirjoitettavia kieliä, ja kun taloushallinnon dimensioita ja päätilin asetuksia on määritettävä.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2bdf1b99ae7be6c9d9c43c91c9273e18ce9b1093
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127644"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Taloushallinnon dimensiot ja päätilit oikealta vasemmalle kirjoitettavilla kielillä

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään käyttöönottopäätöksiä, jotka koskevat oikealta vasemmalle kirjoitettavien kielien käyttöä määritettäessä taloushallinnon dimensioiden ja päätilin asetuksia.

Taloushallinnon dimensiot ja päätilit ovat tärkeimmät käyttöönoton suunnitteluvaiheen komponentit. Kun taloushallinnon dimensiot ja päätilit on luotu järjestelmään, niitä käytetään **Määritä tilirakenteet**, **Lisäsäännön rakenteet** ja **Integrointisovellusten taloushallinnon dimension määritykset** -sivuilla. Näillä sivuilla määritettyä tilausta käytetään järjestelmässä tietojen antamiseen ja kulutuksen määrittämiseen. Joissakin järjestelmän osissa taloushallinnan dimensiot ja päätilit näkyvät eri kentissä. Muualla, kuten kirjauskansioissa, taloushallinnon dimensiot ja päätilit näkyvät kuitenkin yhtenä merkkijonona.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Parhaat käytännöt taloushallinnon dimensioiden ja päätilien määrittämiseen järjestelmässä oikealta vasemmalle kirjoitettavan kielellä

- Kun valitset tilikartan erotinta, valitse jokin kahden erottimen yhdistelmistä: kaksi peräkkäistä yhdysmerkkiä (`--`), kaksi pystyviivaa (`||`), kaksi peräkkäistä pilkkua (`..`) tai kaksi peräkkäistä alaviivaa (`\\`).
- Kun luot taloushallinnon dimension ja päätilin arvoja, käytä ainoastaan numeroita ja oikealta vasemmalle kirjoitettavan kielen merkkejä.
- Älä käytä valitun tilikartan erotin kirjanpitodimension ja päätilin arvoina.

Näitä toimintaohjeita noudattamalla autat takaamaan, että käyttäjän määrittämä järjestys on yhdenmukainen koko järjestelmässä.
