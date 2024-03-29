---
title: B2B-verkkokauppasivustojen laskujenhallinta
description: Tässä artikkelissa kuvataan Microsoft Dynamics 365 Commercen yritysten välisten (B2B) verkkokauppasivustojen laskujenhallintaominaisuudet.
author: ShalabhjainMSFT
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: c1f3533eb711bf87fe226f5c61678b6939f35e13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274425"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>B2B-verkkokauppasivustojen laskujenhallinta

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan Microsoft Dynamics 365 Commercen yritysten välisten (B2B) verkkokauppasivustojen laskujenhallintaominaisuudet.

B2B-tapahtumia käsittelevillä yrityksillä on yleinen käytäntö hyväksyä tilauksia asiakasluotolla ja sitten lähettää asiakkaalle lasku, kun yritys on täyttänyt tilauksen. Asiakkaille määritetään maksuehdot ja alennuksia saadaan käyttää asiakkaan motivoimiseksi maksamaan ajallaan tai ennakkoon. B2B-verkkosivustoilla asiakkaat voivat tarkastella kaikkia laskujaan, millä parannetaan mahdollisuuksia maksujen saamiseen ajallaan. Asiakkaat voivat helposti suodattaa laskuja tarkastellakseen maksettuja, maksamattomia ja osittain maksettuja laskuja määräpäivineen.

![Laskusivu B2B-verkkosivustolla.](../media/ViewInvoices.png)

> [!NOTE]
> Kirjautunut käyttäjä voi tarkastella ja maksaa vain omia laskujaan. Jos Commerce headquarters -sovelluksen asiakastietueen **Lasku ja toimitus** -pikavälilehden avattavassa **Laskutustili**-valikossa on määritetty organisaatiotili, käyttäjä voi tarkastella ja maksaa organisaatiotilin laskuja.

B2B-sivuston **Laskut**-sivulla käyttäjä voi maksaa maksamattoman tai osittain maksetun laskun ja valita sitten **Maksa lasku**. Valittu lasku lisätään koriin, minkä jälkeen käyttäjä voi jatkaa maksutapahtumaa. Tämän jälkeen käyttäjä voi päättää, maksaako hän laskun koko saldon vai osittaisen saldon. Käyttäjä ei voi käyttää tilimaksumenetelmää laskujen maksamiseen.

> [!NOTE]
> Laskuja voi lisätä koriin vain, jos siinä ei ole nimikkeitä. Samoin nimikkeitä voi lisätä koriin vain, jos siinä ei ole laskuja. Microsoft aikoo poistaa tämän rajoituksen tulevissa Commerce-versioissa.

![Korisivu B2B-sivustolla.](../media/PayInvoice.png)

**Laskut**-sivulla käyttäjä voi valita myös **Pyydä laskua** -vaihtoehdon laskun vierestä. Tällöin käyttäjä voi pyytää, että laskun tiedot lähetetään hänen rekisteröityyn sähköpostiosoitteeseensa.

![Laskupyynnon valintaruutu.](../media/RequestInvoice2.png)

Kun käyttäjä on pyytänyt laskua, pyyntö siirretään **Oma tili** -sivun **B2B-pyynnöt**-osaan. Kun työt **P-0001** ja **Synkronoi tilaukset ja kanavoi pyynnöt** on suoritettu Commerce Headquarters -sovelluksessa, laskusähköposti käynnistetään ja B2B-pyynnön tila merkitään valmiiksi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
