---
title: Konsernin sisäiset kulut
description: Organisaation yhdessä yrityksessä työskentelevä työntekijä voi tehdä työtä saman organisaation toiselle yritykselle. Tässä tilanteessa työntekijän kulut voidaan määrittää työn vastaanottaneelle yritykselle konsernin sisäisten kulujen toiminnolla.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390881"
---
# <a name="intercompany-expenses"></a>Konsernin sisäiset kulut

[!include [banner](../includes/banner.md)]

Organisaation yhdessä yrityksessä työskentelevä työntekijä voi tehdä työtä saman organisaation toiselle yritykselle. Tässä tilanteessa työntekijän kulut voidaan määrittää työn vastaanottaneelle yritykselle konsernin sisäisten kulujen toiminnolla. Yritystä, joka työllistää työntekijän, kutsutaan lainaajayritykseksi. Yritystä, jolle työntekijä aiheuttaa kuluja, kutsutaan lainaavaksi yritykseksi. 

Ennen kuin työntekijä voi luoda ja lähettää kuluja töistä, jotka on suoritettu toiselle yritykselle, valitse lainaavan yrityksen **Kulujenhallinnan parametrit** -sivulla **Salli konsernin sisäiset kulurivit** -vaihtoehto. 

## <a name="tax-posting-for-intercompany-expenses"></a>Konsernin sisäisten kulujen verojen kirjaus

[!include [banner](../includes/banner.md)]

Jos haluat käyttää kuluraportissa lainaajayritykseen (lähteeseen) liitettyjä veroryhmiä lainaavan yrityksen (kohteen) sijaan, se on määritettävä kirjanpidon arvonlisäveroasetuksissa. Kun kirjanpidon **Konsernin sisäisen verokirjauksen yritys** -parametrin arvoksi on määritetty **Lähde** ja **Käytä arvonlisäveron verotussäännöt** -arvona on **Ei**, lainaajayrityksen veroyhdistelmää käytetään. Kun saman parametrin asetuksena on **Kohde**, lainaavan yrityksen veroyhdistelmää käytetään. Kun yhdysvaltalaisen yrityksen parametrin asetuksena on **Lähde**, myös **Saatava arvonlisävero** -kenttä on määritettävä uudella **Kirjanpidon kirjausryhmät** -sivulla. Kirjanpitomoduuli käyttää tämän kentän tietoja veroihin liittyvässä kirjanpitomerkinnässä.   
Toiminta on yhdenmukainen riippumatta siitä, onko kulurivit projektin yhteydessä tai ilman sitä.  
