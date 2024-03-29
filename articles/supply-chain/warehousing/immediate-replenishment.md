---
title: Välitön täydennys
description: Tässä artikkelissa käsitellään varaston täydennystä välittömällä täydennyksellä, kun sijaintidirektiivi ei osoita varastoa.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: cf48f2f34f574503bbcae827f8013afe8532fc14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899263"
---
# <a name="immediate-replenishment"></a>Välitön täydennys

[!include [banner](../includes/banner.md)]

Välittömällä täydennyksellä voit täydentää varaston välittömästi sen jälkeen, kun suuntadirektiivirivi ei osoita varastoa. Täydennys perustuu yhteen riviin sijaintidirektiivin asetuksissa. Jos varastoa ei ole käytettävissä siinä kyseisen rivin määrittämässä yksikössä, kyseisen mittayksikön täydennys tapahtuu heti.

Välitön täydennys on vaihtoehtoinen menetelmä, jossa varaston kohdistus perustuu useisiin suuntadirektiivin riveihin ja jossa kysyntä summataan kohdistuksen lopussa ja täydennetään sijaintidirektiivin viimeisellä rivillä määritetyssä mittayksikössä.

Välittömän täydennyksen etuna on, että täydennystä voidaan rajoittaa tiettyihin yksiköihin ja että määrä voidaan ohjata tiettyihin sijainteihin.

## <a name="business-scenario"></a>Liiketoimintaskenaario

Varastossa voi esimerkiksi olla erilliset keräilyalueet mittayksiköille laatikko ja kappale. Haluat optimoida keräilyprosessin keräämällä ensin mahdollisimman monta laatikkoa ja sitten jäljellä olevan laatikkoa pienemmän määrän Kappale-alueelta.

Voit käyttää tässä tapauksessa välitöntä täydennystä. Voit määrittää suuntadirektiivissä välittömän täydennyksen laatikoille, jotta kysynnän täydennystä käytetään heti, kun kysynnän määrään varten kerättäviä laatikoita ei ole tarpeeksi. Voit optimoida tällä tavoin keräilyprosessin siten, että keräily sisältää mahdollisimman monta laatikkoa. Välitön täydennys luo laatikoiden täydennyksen eikä kysyntää siirretä, joten määrät kerätään Kappale-mittayksikössä. Toisin sanoen vain ne määrät, jotka on tarkoitus kerätä Kappale-mittayksikössä (eli laatikkoa pienemmät määrät) kerätään Kappale-alueelta. Jos puute ilmenee Laatikko-alueella, voit kerätä kokonaiskysynnän mukaan mahdollisimman monta laatikkoa. Jäljellä olevat määrät kerätään Kappale-alueelta.

## <a name="where-it-applies"></a>Käyttö

Välitöntä täydennystä käytetään aallon suorituksen aikana, jos kohdistus epäonnistuu sijaintidirektiivin riville, jolle on täydennysmalli on määritetty.

## <a name="set-up-immediate-replenishment"></a>Välittömän täydennyksen määrittäminen

- Valitse ensin **Varastonhallinta** \> **Asetukset** \> **Sijaintidirektiivit** ja sitten **Rivit**-välilehden **Välittömän täydennyksen malli** -luettelossa aaltokysynnän täydennysmalli.

Täydennysmallia käytetään, jos sijaintidirektiivin rivi ei käytä kohdistettua mittayksikköä.

## <a name="troubleshooting"></a>Vianmääritys

Jos sijaintidirektiiviriville valitaan välitön kohdistus mutta mitään täydennystyötä ei luoda, kun käytät kyseisen sijaintidirektiivirivin kysynnän täydennyksen malleja, syy on todennäköisesti jompikumpi seuraavista:

- Varmista, että käytetty kysynnän täydennyksen malli on määritetty käyttämään oikeita **Täydennys**-tyypin sijainti- ja työmalleja.
- Varmista, käytettävissä olevaa varastoa on riittävästi niissä sijainneissa, joissa kysynnän täydennyksen malli hakee käytettävissä olevaa varastoa täydennystä varten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]