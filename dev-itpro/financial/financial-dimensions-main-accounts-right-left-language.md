---
title: "Taloushallinnon dimensiot ja päätilit oikealta vasemmalle kirjoitettavalla kielellä"
description: "Tässä aiheessa esitellään käyttöönottopäätöksiä, jotka koskevat oikealta vasemmalle kirjoitettavien kielien käyttöä Microsoft Dynamics 365 for Operations -järjestelmässä määritettäessä taloushallinnon dimensioiden ja päätilin asetuksia."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b1f196d2a13bba49647dd4f008cd39b7417940f1
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a>Taloushallinnon dimensiot ja päätilit oikealta vasemmalle kirjoitettavalla kielellä

[!include[banner](../includes/banner.md)]


Tässä aiheessa esitellään käyttöönottopäätöksiä, jotka koskevat oikealta vasemmalle kirjoitettavien kielien käyttöä Microsoft Dynamics 365 for Operations -järjestelmässä määritettäessä taloushallinnon dimensioiden ja päätilin asetuksia.

Taloushallinnon dimensiot ja päätilit ovat tärkeimmät käyttöönoton suunnitteluvaiheen komponentit. Kun taloushallinnon dimensiot ja päätilit on luotu järjestelmään, niitä käytetään **Määritä tilirakenteet**, **Lisäsäännön rakenteet** ja **Integrointisovellusten taloushallinnon dimension määritykset** -sivuilla. Näillä sivuilla määritettyä tilausta käytetään järjestelmässä tietojen antamiseen ja kulutuksen määrittämiseen. Joissakin järjestelmän osissa taloushallinnan dimensiot ja päätilit näkyvät eri kentissä. Muualla, kuten kirjauskansiossa, taloushallinnon dimensiot ja päätilit näkyvät kuitenkin yhtenä merkkijonona.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Parhaat käytännöt taloushallinnon dimensioiden ja päätilien määrittämiseen järjestelmässä oikealta vasemmalle kirjoitettavan kielellä

-   Kun valitset tilikartan erotinta, valitse jokin kahden erottimen yhdistelmistä: kaksi peräkkäistä yhdysmerkkiä (--), kaksi pystyviivaa (||), kaksi peräkkäistä pilkkua (..) tai kaksi peräkkäistä alaviivaa (\_\_).
-   Kun luot taloushallinnon dimension ja päätilin arvoja, käytä ainoastaan numeroita ja oikealta vasemmalle kirjoitettavan kielen merkkejä.
-   Älä käytä valitun tilikartan erotin kirjanpitodimension ja päätilin arvoina.

Näitä toimintaohjeita noudattamalla autat takaamaan, että käyttäjän määrittämä järjestys on yhdenmukainen koko järjestelmässä.




