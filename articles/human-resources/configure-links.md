---
title: Linkkien luominen kohteesta Human Resources toiseen ympäristöön
description: Tässä artikkelissa kerrotaan, miten linkki luodaan Microsoft Dynamics 365 Human Resources -ohjelmasta toiseen Dynamics 365 -ympäristöön.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0c9efae1061e96c0c42d5ca6a100bb36889ce56b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859663"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Linkkien luominen kohteesta Human Resources toiseen Finance-ympäristöön

Asiakkaalla voi olla kaksi Dynamics 365 -ympäristöä, joissa hän työskentelee. Esimerkiksi asiakkaalla saattaa olla Finance-infrastruktuurin Dynamics 365 Human Resources-ympäristö ja asiakkaan on muodostettava yhteys toiseen Dynamics 365 Finance -ympäristöön. 

Tämä ominaisuus sallii linkit henkilöstöhallinnon sivulta toisen Finance-ympäristön tietylle sivulle. Kun linkit on konfiguroitu, voit määrittää, missä kohtaa linkki on käytettävissä Human Resourcesissa, ja kohdesivun, joka avataan toisessa ympäristössä.

> [!Note] 
> **Henkilöstöresurssien käyttökokemusten parannukset** on otettava käyttöön **Ominaisuuksien hallinnassa**, jotta tämän ominaisuuden saa käyttöön.

## <a name="configure-target-systems"></a>Kohdejärjestelmien määrittäminen

Human Resourcesissa järjestelmänvalvojat voivat määrittää linkkejä, jotka ovat **Human Resources** -sivuilla. Määrityksen osan muodostavat Finance-ympäristöt, joihin haluat siirtyä linkin kohteena. 

Määritä kohdejärjestelmä:
1. Valitse **Määritä linkit** -sivulla **Määritä kohdejärjestelmä**.  
2. Nimeä kohdejärjestelmä ja anna Finance-ympäristön URL-osoite. Kun olet määrittänyt kohdejärjestelmät, voit määrittää linkit.

## <a name="configure-links"></a>Määritä linkit

Jokaiseen luotavaan linkkiin on määritettävä seuraavat tiedot:
 - **Linkki**: linkin nimi. Käytetään vain tunnistamiseen.
 - **Ota tämä linkki käyttöön**: valitse **Kyllä**, jos haluat näyttää linkin Human Resources -käyttäjille.
 - **Näyttönimi**: Anna nimi, joka näkyy toissijaiseen ympäristöön vievänä linkkinä. 
 - **Surface-linkki lomakkeessa**: valitse sivu, jolla haluat linkin näkyvän. Linkit voidaan määrittää päälle vain **Työntekijän itsepalvelu** -työtilassa sekä **Työ**-, **Toimi**-, **Työntekijä**- ja **Virtaviivaistettu työntekijä** -sivuilla.
 - **Ryhmä**: Voit järjestää linkit ryhmiä käyttämällä. Valitse aiemmin luotu ryhmä tai luo uusi **Ryhmä**-sarakkeessa.
 - **Kohdejärjestelmä**: Valitse kohderyhmä, joka luotiin **Määritä kohdejärjestelmä** -asetuksella. Se on toissijainen ympäristö, jota käytetään siirryttäessä linkin avulla.
 - **Käytä käyttäjän nykyistä yritystä**: Valitse **Kyllä**, jos haluat käyttää käyttäjän nykyistä yritystä Financeen siirryttäessä. Jos valitset **Ei**, voit valita käytettävän yrityksen.
 - **Kohde**-valikkovaihtoehto: Anna Finance-ympäristön valikkovaihtoehto, jota linkin on käytettävä siirryttäessä. Käytettävissä on ne valikkotoiminnot, joihin voi siirtyä suoraan. 

   Voit etsiä tarvittavan valikon vaihtoehdon seuraavasti:
   1. Siirry Finance-ympäristöön ja avaa sitten sivu, johon siirrytään. 
   2. Kopioi valikkotoiminto URL-osoitteesta. Jos esimerkiksi haluat, että linkki vie Finance and Operationsin työntekijäluetteloon, anna arvo, joka URL-osoitteessa &mi-kohdan jälkeen. 
   3. Tässä esimerkissä valikkotoiminto, johon työntekijäluettelosivulla siirrytään on HcmWorkerListPage_Employees.

 - **Linkki tietolähteeseen**: Valitse tietolähde, johon linkki viittaa. Käytettävissä on tavallisimmat lähteet, kuten **Työntekijä** ja **Toimi**.

### <a name="access-to-links"></a>Linkkien käyttöoikeus

Järjestelmänvalvojat näkevät juuri luodut linkit määritetyillä sivuilla, vaikka **Ota tämä linkki käyttöön** -asetuksena olisi **Ei**. Tämä mahdollistaakin linkkien testaamisen, ennen kuin ne ovat muiden työntekijöiden käytössä. Kaikki muut roolit näkevät määritetyt linkit vasta, kun **Ota tämä linkki käyttöön** -asetuksena on **Kyllä**. Työntekijät, joilla on linkit sisältävien sivujen käyttöoikeus, on myös linkkien käyttöoikeus.

Käyttäjillä on oltava myös toissijaisen ympäristön käyttöoikeudet, jotta tämän ympäristön sivuja voidaan käyttää. Jos heillä ei niitä ole, linkkiä käytettäessä avautuu suojauksen valintaikkuna.

