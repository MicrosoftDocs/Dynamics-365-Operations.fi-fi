---
title: Hyväksytty kokonaismäärä -virhe tilausta päätettäessä
description: Kun yrität päättää tuotantotilauksen ja ilmoittaa sen valmiiksi, näyttöön saattaa tulla tuotteen kokonaismäärävirhe. Tällä sivulla selitetään, mistä se johtuu ja miten ongelma korjataan.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476218"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>Hyväksytty kokonaismäärä -virhe tuotantotilausta päätettäessä

## <a name="symptoms"></a>Oireet

Kun raportti yritetään tuotantotilauksessa valmiiksi ilmoitettujen kirjauskansioon, seuraava virhesanoma avautuu:

> Tuotannon valmiiksi ilmoitettujen hyväksytty määrä on %1. Palaute viimeistä toimintoa varten on yhteensä 0,00.

## <a name="cause"></a>Syy

Tämä ongelma esiintyy, jos viimeisissä toiminnoissa kirjatut määrät olivat virheellisiä. Jos tuotanto esimerkiksi aloitettiin mutta aloitettavaa määrää ei kohdistettu, reitityskortin kirjauskansio kirjataan ilman rivejä. Tarkista tilanne avaamalla tuotantotilaus ja valitsemalla sitten toimintoruudun **Näytä**-välilehdessä **Reitityskortti**.

## <a name="resolution"></a>Ratkaisu

Voit korjata ongelma kirjaamalla lisäkirjauskansiot niille toiminnoille, joiden kirjauskansioita ei kirjattu oikein. Käynnistä tuotantotilaus uudelleen ja valitse lisäkirjauskansioiden kirjaaminen. Tämä toiminto ei käynnistä tuotantotilausta vaan kirjaa kirjauskansiot. Kirjattujen määrien pitäisi näkyä sitten reitityskortissa ja tuotantotilausten lopettaminen pitäisi olla mahdollista.
