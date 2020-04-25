---
title: Yleiskuvaus
description: Dynamics 365 Human Resourcesissa Loma ja poissaolo -työtila tarjoaa joustavan kehyksen uusien lomasuunnitelmien luomiseen, pyyntöjen hallinnan työnkulkuja sekä intuitiivisen itsepalvelusivun, jonka avulla työntekijät voivat pyytää lomaa.
author: andreabichsel
manager: AnnBe
ms.date: 04/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f7ba32b31a67d81ee5be568b0e64842f343f96b
ms.sourcegitcommit: 9940ca772807d3c4e1ff3bf47f45b7251c4469ac
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/04/2020
ms.locfileid: "3226227"
---
# <a name="overview"></a>Yleiskuvaus

Dynamics 365 Human Resources auttaa sinua tarjoamaan hienoja lomaetuuksia työntekijöillesi. **Loma ja poissaolo** -työtila tarjoaa joustavan kehyksen uusien lomasuunnitelmien luomiseen, pyyntöjen hallinnan työnkulkuja sekä intuitiivisen itsepalvelusivun, jonka avulla työntekijät voivat pyytää lomaa. Analyysi auttaa organisaatiotasi mittaamaan ja seuraamaan lomasuunnitelmien saldoja ja käyttöä.

## <a name="set-up-leave-and-absence"></a>Loman ja poissaolon määrittäminen

Ennen lomasuunnitelmien luomista työntekijöillesi, sinun on tehtävä muutama asetusvaihe:

- [Loma- ja poissaoloparametrien määrittäminen](hr-leave-and-absence-parameters.md)
- [Työaikakalenterin luominen](hr-leave-and-absence-working-time-calendar.md)
- [Luo lomapyyntötyönkulku](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Luo ja hallitse lomasuunnitelmia

Ennen kuin luot lomasuunnitelmia työntekijöille, sinun on luotava loma- ja poissaolotyypit. Kun olet luonut lomasuunnitelman, voit rekisteröidä työntekijät suunnitelmaan. Voit myös suorittaa jaksotusprosessin, luoda hälytyksiä ja tarkastella suunnitelmiasi koskevia analyyseja.

- [Määritä loman ja poissaolon tyypit](hr-leave-and-absence-types.md)
- [Loma- ja poissaolosuunnitelman luominen](hr-leave-and-absence-plans.md)
- [Työntekijöiden liittäminen lomasuunnitelmaan](hr-leave-and-absence-enroll.md)
- [Jaksota loma- ja poissaolosuunnitelmia](hr-leave-and-absence-accrue.md)
- [Loma- ja poissaoloanalyysien tarkasteleminen](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Pyydä lomaa ja hallitse pyyntöjä

Työntekijät voivat lähettää lomapyyntöjä ja hallita niitä **Työntekijän itsepalvelu** -työtilassa.

- [Pyydä vapaata](hr-employee-self-service-request-time-off.md)
- [Loma- ja poissaolopyyntöjen hallinta](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>Lomien ja poissaolojen tunnetut ongelmat

### <a name="rounding-precision"></a>Pyöristystarkkuus

**Pyöristystarkkuutta** ei voi määrittää, kun määrität **Pyöristystyypin**. Voit määrittää **Pyöristystarkkuuden** vain **Loma- ja poissaolotyyppi** -yksikön avulla. 

1. Avaa **Loma- ja poissaolotyyppi** -yksikkö valitsemalla **Avaa Excelissä** avataksesi **Loma- ja poissaolotyyppi** -yksikön.

2. Kun tiedosto avautuu ja on käytössä, valitse **Suunnittelu**.

3. Valitse **Loma- ja poissaolotyyppi** -taulukosta muokattava kynäasetus.

4. Valitse **pyöristystarkkuus** ja **pyöristystyyppi** ja lisää sitten kenttä luetteloon valitsemalla **Lisää**.

5. Valitse **Päivitä** ja valitse sitten **Valmis**.

6. Kirjoita tai valitse **Pyöristystyyppi** kullekin lomatyypille, jos niitä ei ole vielä määritetty. 

7. Syötä **Pyöristystarkkuus** asianmukaisille tyypeille.

8. Valitse **Julkaise**, jos haluat työntää muutokset henkilöstöhallintoon.

## <a name="leave-and-absence-preview-features"></a>Lomien ja poissaolojen esikatseluominaisuudet

Voit kokeilla uusia loman ja poissaolon esikatselutoimintoja **Eristys**-ympäristössä. Lisätietoja esikatseluominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md). Esikatselutoimintoja ovat esimerkiksi seuraavat:

- **Loman keskeytys** - Voit keskeyttää työntekijän loman ja poissaolon henkilöstöhallinnossa. Loman keskeyttäminen pysäyttää valittujen lomatyyppien lomajaksotukset. Jos keskeytys tapahtuu jaksotusprosessien jälkeen, loman keskeyttäminen luo suhteutetun oikaisun työntekijän lomasaldoon. 

- **Siirtosäännöt** - Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään. Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi. 