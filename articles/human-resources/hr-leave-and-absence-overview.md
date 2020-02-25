---
title: Yleiskatsaus
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 9a36f6b6ba696fa926ab3d6298568dddfce43a57
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008924"
---
# <a name="overview"></a>Yleiskatsaus

Dynamics 365 Human Resources auttaa sinua tarjoamaan hienoja lomaetuuksia työntekijöillesi. **Loma ja poissaolo** -työtila tarjoaa joustavan kehyksen uusien lomasuunnitelmien luomiseen, pyyntöjen hallinnan työnkulkuja sekä intuitiivisen itsepalvelusivun, jonka avulla työntekijät voivat pyytää lomaa. Analyysi auttaa organisaatiotasi mittaamaan ja seuraamaan lomasuunnitelmien saldoja ja käyttöä.

## <a name="set-up-leave-and-absence"></a>Loman ja poissaolon määrittäminen

Ennen kuin voit luoda lomasuunnitelmia työntekijöillesi, sinun on tehtävä muutama asetusvaihe:

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

- [Pyydä poissaoloaikaa](hr-employee-self-service-request-time-off.md)
- [Virkavapaan ja poissaolopyyntöjen hallinta](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-preview-features"></a>Lomien ja poissaolojen esikatseluominaisuudet

Voit kokeilla uusia loman ja poissaolon esikatselutoimintoja **Eristys**-ympäristössä. Lisätietoja esikatseluominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md). Esikatselutoimintoja ovat esimerkiksi seuraavat:

- **Loma- ja poissaolokalenteri** – Loma- ja poissaoloparametrit siirtyvät kohdasta **Henkilöhallinnon parametrit** uuteen näyttöön nimeltään **Loma- ja poissaoloparametrit**. Uudessa näytössä on uusi **Kalenteri**-välilehti. Tämä esikatselu mahdollistaa vain parametrien osajoukon. Voit käyttää uutta näyttöä **Lomat ja poissaolot** -työtilan **Linkit**-välilehdestä. Kalentereja ovat esimerkiksi:
  - **Yrityksen kalenteri** – Näyttää kaikki työntekijöiden vapaa-aikapyynnöt. Henkilöt, joilla on **Henkilöstöhallinto**-rooli voivat käyttää tätä **Linkit**-välilehdessä **Lomat ja poissaolot** -työtilassa.
  - **Johtajaryhmän kalenteri** – Näyttää kaikkien suorien alaisten vapaa-aikapyynnöt. Johtajat voivat käyttää kalenteria työntekijän itsepalvelun **Lomat ja poissaolot** -kohdan **Oma ryhmä** -välilehdessä. 

- **Lomien ja poissaolojen vapaakalenterit** – Lomatyyppeihin kuuluu nyt **Loma**-vaihtoehto, jota käytetään yhdessä työaikakalenterin kanssa. Lomiksi ja kiinnioloajoiksi määritettyjä päivä kutsutaan nyt työpäivä luotaessa nimellä **Loma**. Kun jaksotuksia käsitellään, työntekijöille, joille kalenteri on määritetty, tehdään muutoksia, jotta otetaan huomiot työpäiville osuvat lomat.

- **Lomien jaksotusten valvonta** – Uuden näytön avulla voit tarkistaa, milloin jaksotukset on käsitelty ja poistettu sekä kaikkien työntekijöiden että yksittäisten työntekijöiden osalta. Voit käyttää tätä uutta näyttöä **Lomat ja poissaolot** -työtilan **Linkit**-välilehdestä.

- **Loman jaksotuksen poisto** – Voit nyt poistaa tiettyjen lomasuunnitelmien jaksotustietueita. Voit käyttää tätä uutta valintaa **Lomat ja poissaolot** -työtilan **Linkit**-välilehdestä. Yksittäisten työntekijöiden osalta tämä valinta näkyy työntekijän profiilin **Lomat ja poissaolot** -ryhmittelyssä. 

- **Lomien jaksotuksen pyöristys** – Uudet **Lomatyypin**asetukset määrittävät, millaista pyöristystä jaksotuksessa käytetään sekä pyöristyksen desimaalitarkkuuden jaksotusprosessin aikana. Kun jaksotuksia käsitellään, pyöristystä ja tarkkuutta sovelletaan jaksotustietueisiin. 

- **Määritä useita lomatyyppejä yksittäisessä lomasuunnitelmassa** – Uudessa lomatyyppien sarakkeessa loman jaksotusaikataulussa voit määrittää loma- ja poissaolosuunnitelmalle useita lomatyyppejä eri jaksotusaikatauluineen. Aiempi **Lomatyyppi**-kenttä poistetaan. Työntekijöiden rekisteröitymisessä lomatyyppien saldot esitetään nyt taulukossa ruudun yläreunan sijaan.

  > [!IMPORTANT]
  > Tätä ominaisuutta ei voi poistaa käytöstä sen jälkeen, kun se on otettu käyttöön.

- **Käytä työntekijän laskennallista kokopäiväisyyttä (FTE) jaksotuksessa** – Uusi loman jaksotusaikataulun sarake, joka mahdollistaa FTE-arvon käytön jaksotuksessa. Kun jaksotuksia käsitellään, sovellus käyttää työntekijän ensisijaista asemaa ja määritettyä FTE-arvoa määrittääkseen suhteellisen jaksotusmäärän.

  > [!NOTE]
  > Tämä ominaisuus on käytössä vain, kun **Määritä useita lomatyyppejä lomasuunnitelmaa kohden** on käytössä. 
