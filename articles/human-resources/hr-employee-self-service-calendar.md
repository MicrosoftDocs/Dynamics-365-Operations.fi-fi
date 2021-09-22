---
title: Ryhmän kalenterin luominen
description: Tarkastele ja luo ryhmän kalentereita Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eacf2dc460367ebefb7e9f4d9e301ec719cd2317
ms.sourcegitcommit: a8ac6d9b63eb67d14dd17a086ef4f1eccd7f9fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/27/2021
ms.locfileid: "7431483"
---
# <a name="view-team-and-company-calendars"></a>Ryhmä- ja yrityskalenterien tarkasteleminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit tarkastella ryhmä- ja yrityskalentereita Dynamics 365 Human Resourcesissa. Ryhmän kalentereissa näkyvät vain suorat raportit, jotka on määritetty rivihierarkiassa.

## <a name="view-your-team-calendar-as-an-employee"></a>Työryhmän kalenterin tarkasteleminen työntekijänä

- Valitse **Työntekijän itsepalvelu** -työtilassa **Tiimin poissaolokalenteri** **Yhteenveto**-kohdassa.

## <a name="view-your-team-calendar-as-a-manager"></a>Työryhmän kalenterin tarkasteleminen esimiehenä

1. Valitse **Työntekijän itsepalvelu** -työtilassa **Oma tiimi**.

2. Valitse **Loma ja poissaolo** ja valitse sitten **Näytä esimiehen poissaolokalenteri**.

Esimiehet voivat myös käyttää tiimikalenteria **Tiimin odottavista lomapyynnöistä**, **Hyväksytyistä lomista** ja **Lomapyynnöistä**. 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>Poissaolopäällikön kalenterin tarkasteleminen poissaolopäällikkönä

> [!NOTE]
> Jos haluat tarkastella poissaolopäällikön kalenteria, sinun on ensin otettava käyttöön **(Esiversio) Poissaolopäällikkö hallinnoi poissaoloja**, jotta voit hallita ominaisuutta ominaisuuksien hallinnassa. Lisätietoja esiversio-ominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

Poissaolopäällikkö-roolin käyttäjät voivat tarkastella poissaolopyyntöjä kalenterissaan. Voit käyttää vapaa-aikakalenteria seuraavien ohjeiden mukaisesti.

1. Valitse **Työntekijän itsepalvelu** -työtilassa **Poissaolojen hallinta** ja sitten **Poissaolopäällikön kalenteri**.

2. Syötä **Päivämäärä**-kenttään halutut päivämäärät.

3. Päivitä näkymän asetukset tarpeen mukaan.

Poissaolopäällikön kalenterissa näkyvät kaikki poissaolopäällikölle raportoivien työntekijöiden tietueet Vapaa-hierarkiassa.

## <a name="view-a-company-calendar"></a>Yrityksen kalenterin tarkasteleminen

Henkilöstöhallinnan roolien henkilöt voivat tarkastella yrityksen kalentereita. Yrityksen kalentereissa näkyvät kaikki työntekijät. Oletusarvon mukaan kalenterissa näkyy kuluvan päivän päivämäärä sekä 28 päivää, mutta voit muuttaa päivämääräväliä. Voit myös suodattaa kalenterin **Nimen**, **Henkilöstönumeron** ja **Lomatyypin** mukaan.

1. Valitse **lomat ja poissaolot** -työtilassa **Linkit**.

2. Valitse **Loma- ja poissaolokalenteri**.

Henkilöstöhallinnon roolit voivat myös käyttää yrityksen kalenteria **Loma- ja poissaolopyynnöistä**, **Hyväksytyistä poissaoloista** ja **Poissaolopyynnöistä**. 

Kalenterit sisältävät nyt lisäsuodattimia ja -asetuksia. Kaikkiin kalentereihin sisältyvät seuraavat näkymävaihtoehdot:

- Hyväksytyt pyynnöt
- Odottavat pyynnöt
- Työntekijät, joilla on lomapyyntöjä
- Työntekijät, joilla ei ole lomapyyntöjä
- Työntekijöiden syntymäpäivät
- Poissaolopyynnöt 
- Virkavapaapyynnöt

**Loma- ja poissaoloparametrit** -sivun kalenterimääritys määrittää käytettävissä olevat näkymäasetukset.

Voit myös suodattaa kalentereita esimiehen tai osaston mukaan. Ensisijainen toimen määritys määrittää näytettävät työntekijät, kun nämä suodattimet on määritetty. 

> [!IMPORTANT]
> Voit ottaa **Yritysten välinen lomanäkymä** -ominaisuuden käyttöön ominaisuuksien hallinnassa. Tämän jälkeen ominaisuus on otettava käyttöön **Henkilöstöhallinnon jaetut parametrit** -sivulla, jos haluat näyttää yrityksen suodattimen kalentereissa. Lisätietoja on kohdassa [Loma- ja poissaoloparametrien määrittäminen](hr-leave-and-absence-parameters.md).
> 
> Voit suodattaa kalenterin yrityksen mukaan. Jos haluat nähdä kaikki työntekijät riippumatta yrityksestä, yyhjennä suodatinruutu ja valitse **Enter**-näppäin. 

Lisätietoja kalenteriasetuksista on ohjeaiheessa [Kalenteriparametrien määrittäminen](hr-leave-and-absence-parameters.md?configure-calendar-parameters).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
