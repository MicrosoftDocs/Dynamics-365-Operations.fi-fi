---
title: Taloushallinnon dimensiot ja päätilit oikealta vasemmalle kirjoitettavilla kielillä
description: Tässä aiheessa käsitellään päätöksiä, joita on tehtävä käytettäessä oikealta vasemmalle kirjoitettavia kieliä, ja kun taloushallinnon dimensioita ja päätilin asetuksia on määritettävä.
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 26fd186415db0adf01b8c53b188171fcf86fbc88
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111659"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]