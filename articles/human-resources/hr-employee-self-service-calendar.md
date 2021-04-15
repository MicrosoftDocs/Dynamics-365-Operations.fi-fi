---
title: Ryhmän kalenterin luominen
description: Tarkastele ja luo ryhmän kalentereita Dynamics 365 Human Resourcesissa.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 07c7f1303238fe61d70be26ec5a198f1ac489090
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790761"
---
# <a name="view-team-and-company-calendars"></a>Ryhmä- ja yrityskalenterien tarkasteleminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit tarkastella ryhmä- ja yrityskalentereita Dynamics 365 Human Resourcesissa. Ryhmän kalentereissa näkyvät vain suorat raportit, jotka on määritetty rivihierarkiassa.

## <a name="view-your-team-calendar-as-an-employee"></a>Työryhmän kalenterin tarkasteleminen työntekijänä

1. Valitse **Työntekijän itsepalvelu** -työtilassa **Tiimin poissaolokalenteri** **Yhteenveto**-kohdassa.

## <a name="view-your-team-calendar-as-a-manager"></a>Työryhmän kalenterin tarkasteleminen esimiehenä

1. Valitse **Työntekijän itsepalvelu** -työtilassa **Oma tiimi**.

2. Valitse **Loma ja poissaolo** ja valitse sitten **Näytä esimiehen poissaolokalenteri**.

Esimiehet voivat myös käyttää tiimikalenteria **Tiimin odottavista lomapyynnöistä**, **Hyväksytyistä lomista** ja **Lomapyynnöistä**. 

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

Loma- ja poissaoloparametrien kalenterimääritykset määrittävät käytettävissä olevat näkymäasetukset.

Voit myös suodattaa kalentereita esimiehen tai osaston mukaan. Ensisijainen toimen määritys määrittää näytettävät työntekijät, kun nämä suodattimet on määritetty. 

>[!IMPORTANT]
>Loman ja poissaolon tarkasteleminen yrityksissä tapahtuu nyt esikatselussa. Se on otettava käyttöön **eristysympäristössä**. Lisätietoja esiversio-ominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).<br><br>
>Tämän jälkeen ominaisuus on otettava käyttöön **Human Resourcesin jaetut parametrit** -kohdassa, jos haluat näyttää yrityksen suodattimen kalentereissa. Lisätietoja on kohdassa [Loma- ja poissaoloparametrien määrittäminen](hr-leave-and-absence-parameters.md).<br><br>
>Voit suodattaa kalenterin yrityksen mukaan. Jos haluat nähdä kaikki työntekijät riippumatta yrityksestä, yyhjennä suodatinruutu ja valitse Enter-näppäin. 

Lisätietoja kalenteriasetuksista on ohjeaiheessa [Kalenteriparametrien määrittäminen](hr-leave-and-absence-parameters.md?configure-calendar-parameters).



[!INCLUDE[footer-include](../includes/footer-banner.md)]