---
title: Konfiguraatioiden käsittely
description: Tämä artikkeli sisältää yleiskatsauksen sähköisen raportoinnin (ER) konfiguraatioiden käsittelyn pääskenaariosta Globalisaatio-ominaisuudet -työtilassa.
author: gionoder
ms.date: 01/26/2022
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
ms.openlocfilehash: d87559405d2490c314eb2c8b88268af0dc0dfaca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283052"
---
# <a name="work-with-configurations"></a>Konfiguraatioiden käsittely

[!include [banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) konfiguraatiot ovat yksi sähköisen laskutuksen ominaisuuksien pääkomponenttien joukoista. ER-konfiguraatio sisältää tiedostorakenteen asetukset sekä muunnossäännöt tietojen muunnosta varten kahdella tavalla:

- **Vie ER-muodon konfigurointi** – Tämä konfigurointi muuntaa tiedot yhdistetystä sisäisestä rakenteesta (ER-mallista) sähköiseen tiedostomuotoon.
- **Tuo ER-muodon konfigurointi** – Tämä konfigurointi muuntaa tiedot sähköisestä tiedostomuodosta yhdistettyyn sisäiseen rakenteeseen (ER-malliin).

Lähtevien sähköisten tiedostojen ennalta määritetyssä muodossa luomisen lisäksi ER-konfiguraatioita käytetään paljon ulkoisten Internet-palveluiden saapuvien viestien jäsentämiseen vastauksina. Tämä ominaisuus auttaa luomaan konfiguroitavaa logiikkaa, jonka avulla voidaan saada tulokset ulkoisten kanavien kanssa kommunikoitaessa, muuntaa tulokset (koodit, sanomat ja lokit) käyttäjän luettavaksi rakenteeksi ja siirtää sitten tiedot asiakasohjelmasovellukseen.

Jos haluat aloittaa ER-konfiguraatioiden käytön sähköisessä laskutusominaisuudessa, linkitä ne toimintoon ja määritä ne käyttöön nykyisen toimintoversion **Konfiguroinnit**-välilehdessä. Voit käyttää linkitettyä ER-konfiguraatiota valitsemalla **Lisää**, **Poista**, **Muokkaa** tai **Näytä**.

Ennen kuin voit lisätä linkin ER-konfiguraatioon, konfiguraation on oltava olemassa Regulatory Configuration Service (RCS) -tietovarastossa. Noudattamalla seuraavia ohjeita voit tarkistaa RCS-tietovarastossa käytettävissä olevat ER-konfiguraatiot.

1. Kirjaudu RCS-tilille.
2. Valitse **Sähköinen raportointi** -työtilan **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.

Lisätietoja uuden ER-konfiguraation luomisesta tai aiemmin luodun ER-konfiguraation tuomisesta yleisistä tietovarastoista on kohdassa [Sähköinen raportointi](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Voit muokata linkitettyä ER-konfiguraatiota valitsemalla nykyisen sähköisen laskutusominaisuuden **Konfiguroinnit**-välilehdestä **Muokkaa**. Järjestelmä luo automaattisesti version ER-konfiguraatiosta. Jos aktiivinen konfigurointipalvelu ei ole luonut nykyistä versiota, järjestelmä luo johdetun version, joka käyttää konfiguraatiopalveluasi. Jos aktiivinen konfigurointipalvelu on luonut nykyisen version, järjestelmä luo uuden version. Molemmissa tapauksissa voit muokata luotua versiota ja tehdä sitten automaattisesti kaikki tarvittavat päivitykset.
