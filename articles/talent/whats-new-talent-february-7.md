---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (7. helmikuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 002dcd8253a0ab753ac9002e7027441db6d0b858
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461063"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-7-2019"></a>Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (7. helmikuuta 2019)

Tässä ohjeaiheessa käsitellään Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

### <a name="interview-scheduling-enhancements"></a>Haastattelujen aikataulutuksen parannukset
Kattavaan haastattelujen aikataulutuskokemukseen on tehty parannuksia. Näkyvissä on nyt sisäisen hakijan kalenterin käytettävyystiedot, ja sisäisen hakijan kalenteria voi käyttää aikataulusuosituksiin. Lisätietoja on kohdassa [Haastattelujen aikataulutus ja palaute](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>Työpaikan julkaiseminen LinkedInin – yrityksen vastaavuusongelma korjattu
Ongelma, jossa Attractista LinkedIniin julkaistut työpaikat näkyivät väärän yrityksen kohdalla, on korjattu. Lisätietoja on kohdassa [Työpaikkojen luominen, hyväksyminen ja julkaiseminen Attractissa](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>Järjestelmänvalvojan asetuksissa näytettävä urasivuston URL-osoite
Urasivuston aloitussivun URL-osoite näkyy nyt **järjestelmänvalvojan asetuksissa** **Urasivuston hallinta** -kohdassa.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

**Koontiversio 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>Töissä tuetaan useita kompensaatiotasoja
Tämän muutoksen ansiosta työpaikkaan voidaan määrittää useita kompensaatiotasoja, joten samaa työpaikkaa käytettäessä voidaan ottaa käyttöön työntekijän kiinteä kompensaatio, joka voi olla erilainen eri suunnitelmissa. 

Esimerkki:    
*Työ* – Asiakaspäällikköön *liitetyt kompensaatiotasot:* B1 ja B2 – Kullekin tasolle on määritetty arvoalue. B1 = pieni 50 000, keski 60 000, suuri 75 000 ja B2 = pieni 65 000, keski 74 000, suuri 85 000. Kun työntekijöille luodaan kiinteää kompensaatiota määritettyjen kelpoisuussääntöjen perusteella, jokainen kiinteä suunnitelma voi nyt osoittaa samaan työhön ja työn eri tasoihin. Tällä tavoin suunnitelmat voidaan määrittää eri alueille tai yrityksille ja osoittamaan samaan työhön mutta eri alueille ilman, että töiden kaksoiskappale olisi luotava tilille näitä eroja varten.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>Kompensaatiotason kenttä on lisätty työntekijän kiinteän kompensaation yksikköön 
Tämän päivityksen ansiosta työntekijän kiinteän kompensaation yksikkö on päivitetty sisältämään **Kompensaatiotaso**-kenttä. Tämä lisäys helpottaa työntekijän kiinteiden kompensaatiosuunnitelmien päivittämistä. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>Työluokan päivittäminen uusia toimia päivitettäessä ja luotaessa
Kun toimen työtä muutetaan, **työluokka** palautuu oletusasetukseen valitun työn perusteella.

### <a name="performance-improvements-when-rendering-workspaces"></a>Suorituskyvyn parannukset työtiloja hahmonnettaessa
Työtilojen analytiikkavälilehdet latautunut nyt vain kyseisiä sivuja käytettäessä. Ilmaisin näkyy sivun ensimmäisen hahmonnuksen aikana sivun vasemmassa yläkulmassa.
