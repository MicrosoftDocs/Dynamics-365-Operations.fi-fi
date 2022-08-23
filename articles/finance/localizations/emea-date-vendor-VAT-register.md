---
title: Toimittajan ALV-rekisterin päivämäärä
description: Tässä artikkelissa on tietoja toimittajan alv-rekisterin käyttöönottopäivämäärän ominaisuudesta
author: AdamTrukawka
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: global
ms.author: atrukawk
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.custom: intro-internal
ms.openlocfilehash: 4af770427f5b19eaf2a129b26d54aeacc6c2f148
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278275"
---
# <a name="date-of-vendor-vat-register"></a>Toimittajan ALV-rekisterin päivämäärä

Microsoft Dynamics 365 Financen version 10.0.24 uusi **toimittajan ALV-rekisterin kentän päivämäärä** on käytettävissä toimittajalaskuissa. Tämä kenttä määrittää oston verotettavan toimituksen päivämäärän.

Voit ottaa uuden kentän käyttöön siirtymällä **ominaisuudenhallinnan** työtilaan, etsi ja valitse **Toimittajan alv-rekisterin käyttöönottopäivämäärä toimittajan laskuissa** -toiminnolla ja valitsemalla sitten **Ota käyttöön nyt**.

Toimittajien saapuvilla laskuilla voi olla kaksi päivämäärää: päivämäärä, jolloin toimittaja on tehnyt laskun, ja verotettavan toimituksen päivämäärä (jolloin toimittaja veloitti arvonlisäveron [ALV], maksettava). Joissakin tilanteissa nämä kaksi päivämäärää voivat olla erilaiset.

Voit vähentää ostolaskun saapuvan arvonlisäveron summan ja sisällyttää laskun alv-raportteihin myöhemmin päivämääränä, joka eroaa molemmista aiemmin mainituista päivämääristä. Tätä päivämäärää ohjaa joidenkin skenaarioiden saapuvien alv-vähennysten lykkäystä koskevat paikalliset säännöt. Tämä riippuu maasta tai alueesta.

Joissakin ALV-raporteissa, kuten [ALV-valvontalausunnon raporteissa](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) Tšekin tasavallassa, vaaditaan, että verotettavan toimituksen päivämäärä raportoidaan ostoasiakirjassa. Tämä päivämäärä on raportoitava, jotta veroviranomaiset voivat täsmäyttää vastapuolten välisen alv-raportoinnin.

Talousosaston päivämäärät voidaan määrittää seuraaviin kenttiin:

- **Laskun päivämäärä** – Päivämäärä, jolloin toimittaja on antanut laskun.
- **ALV-rekisterin päivämäärä** – Ostolaskun ALV-summan vähennyksen päivämäärä.
- **Toimittajan ALV-rekisterin päivämäärä** – Toimittajan verotettavan toimituksen päivämäärä.
- **Vastaanota asiakirjan päivämäärä** – Päivämäärä, jolloin vastaanotit laskun.

Kentät sijaitsevat seuraavilla sivuilla:

- Toimittajan lasku
- Toimittajan laskurekisteri
- Toimittajan laskun hyväksyntä
- Toimittajan laskun kirjauskansio

Kun toimittajan lasku on kirjattu, voit tarkistaa **laskukirjauskansio**- ja **toimittajatapahtuma**-sivujen päivämäärät.
