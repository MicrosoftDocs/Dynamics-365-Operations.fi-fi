---
title: Yleiskuvaus
description: Dynamics 365 Human Resourcesissa Loma ja poissaolo -työtila tarjoaa joustavan kehyksen uusien lomasuunnitelmien luomiseen, pyyntöjen hallinnan työnkulkuja sekä intuitiivisen itsepalvelusivun, jonka avulla työntekijät voivat pyytää lomaa.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec72d2d741f7f8428a7daa97bb982e9fc00b8c3f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428964"
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

Voit kokeilla uusia loman ja poissaolon esikatselutoimintoja **Eristys**-ympäristössä. Lisätietoja esikatseluominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md). 

[!include [banner](includes/preview-feature.md)]

Esikatselutoimintoja ovat esimerkiksi seuraavat:

- **Loman jaksotus yritystä tai suunnitelmaa kohden** - Voit suorittaa jaksotusprosessin joko kaikkien yritysten tai yksittäisen yrityksen osalta. Voit myös suorittaa jaksotusprosessin tiettyä yritystä varten määrätyn loma- ja poissaolosuunnitelman osalta. 

- **Osta loma** - Voit ottaa käyttöön ja luoda osta loma -käytäntöjä työntekijöille ostopyyntöjen lähettämistä varten. Työntekijät voivat lähettää ostopyyntöjä, ja niiden saldot päivitetään automaattisesti pyynnön mukaiseksi.  

- **Liitteiden lisääminen hyväksyttyihin loma pyyntöihin** - Voit lisätä liitteen lomapyyntöön, joka on jo hyväksytty. 

