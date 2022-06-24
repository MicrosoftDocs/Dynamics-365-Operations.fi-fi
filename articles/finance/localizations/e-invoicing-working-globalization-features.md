---
title: Globalisaatio-ominaisuuskomponentit
description: Tässä artikkelissa on yleiskuvaus globalisaatio-ominaisuuskomponenteista.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5525332fe3f1a3ea96da630dc34bab82e4117f99
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891485"
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
