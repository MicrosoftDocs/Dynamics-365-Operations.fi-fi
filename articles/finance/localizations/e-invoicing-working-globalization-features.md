---
title: Globalisaatio-ominaisuuskomponentit
description: Tässä artikkelissa on yleiskuvaus globalisaatio-ominaisuuskomponenteista.
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 94e2d118c332a15f41f33184f5e44b0fdaccd000
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275223"
---
# <a name="globalization-feature-components"></a>Globalisaatio-ominaisuuskomponentit

[!include [banner](../includes/banner.md)]

Globalisaatio-ominaisuus on komponenttijoukko, joka määrittää säännöt sähköisen raportoinnin (ER) konfiguraatioiden tietojen muunnosta varten. Nämä komponentit sisältävät sähköisten tiedostojen käsittelyohjeet ja niiden lähettämiseen ulkoisiin kanaviin tai niiden vastaanottamiseen. Ne sisältävät myös ehtoja, jotka määrittävät, milloin saapuville yritystiedoille suoritetaan toiminto.

Kaikki komponentit riippuvat toisistaan. Globalisaatio-ominaisuuksien avulla voit luoda ja ylläpitää tätä riippuvuutta sekä tukea komponenttijoukon elinkaaren hallintaa ja versiointia.

## <a name="access-electronic-invoicing-feature-components"></a>Sähköisen laskutuksen ominaisuuksien komponenttien käyttö 

1. Kirjaudu sisään Regulatory Configuration Service (RCS) -tilillesi.
2. Valitse **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.

    Globalisaatio-ominaisuuksilla on useita komponentteja. **Sähköisen laskutuksen toiminnot** -sivulla on erillinen välilehti kutakin komponenttia varten.

    - **Versio** – Tämä komponentti tukee ominaisuuden elinkaaren hallintaa. Sen avulla voit hallita ominaisuuden eri versioiden tilaa.
    - **Konfiguroinnit** – Tämän komponentin avulla voit hallita, tarkastella ja muokata käsittelyputkessa käytettyjä liittyviä ER-muotoja ja muotomäärityskonfiguraatioita.
    - **Asetukset** – Tämän osan avulla voit hallita järjestelmän palveluiden, kuten sähköisen laskutuspalvelun käyttäjien hallintatoimintoja. Näin ollen se tukee viestintä- ja vastaussääntöjen joustavaa rakentamista.
    - **Ympäristöt** – Tämän komponentin avulla voit käyttää globalisointipalveluja, kuten sähköistä laskutuspalvelua, hallita ympäristöä, jossa toiminnon version asetuksia käytetään. Sen avulla voit myös myöntää käyttöoikeuden käyttäjille, joilla on ominaisuusversion asetusten käyttöoikeus.
    - **Organisaatiot** – Tämän osan avulla käyttäjät voivat jakaa ominaisuuden ulkoisten organisaatioiden kanssa.
    - **Tunnisteet** – Tämän komponentin avulla voit merkitä tunnisteella toimintoja, joita voidaan käyttää viitteenä globalisaatiomallissa.
