---
title: Dynamics 365 Human Resources -infrastruktuurin yhdistäminen - Julkaisun 10.0.25 päivitys
description: Tämä ohjeaihe sisältää tietoja Microsoft Dynamics 365 Human Resourcesin versiosta 10.0.25, joka tuo perusinfrastruktuurin yhdistämisen ensimmäiset toiminnot.
author: twheeloc
ms.date: 01/19/2022
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
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec6d47c44136f7a105a702358370dd676d9339c1
ms.sourcegitcommit: 96f936267d3f314f06da6ce6f809eba2ec3b205f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/24/2022
ms.locfileid: "8018345"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources -infrastruktuurin yhdistäminen - Julkaisun 10.0.25 päivitys

Julkaisu 10.0.25 tuo ensimmäistä kertaa infrastruktuurin yhdistämisen toiminnot. Infrastruktuurin yhdistämisen aikana Microsoft Dynamics 365 Human Resources yhdistetään rahoitus- ja toiminta -infrastruktuuriin. Sovellus on kuitenkin edelleen lisensoitu itsenäisiksi sovellukseksi, kuten Dynamics 365 Finance ja Dynamics 365 Supply Chain Management. Lisätietoja infrastruktuurien yhdistämisestä on kohdassa [Dynamics 365 Human Resourcesin infrastruktuurin yhdistämisen UKK](../human-resources/hr-infrastructure-merge-faq.md).

Yhdistämisen avulla Human Resourcesin käyttäjät voivat olla yhdenmukaisia seuraavilla tavoilla:

- [Ympäristön hallinta ja integraatiot ovat yhdenmukaisia Human Resources- ja rahoitus- ja toiminta sovellusten välillä.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Ympäristöjen hallinta Microsoft Dynamics Lifecycle Servicesissä, hakujen tekeminen ja Regression Suite Automation Tool.
    - Käytössä on yksi koodiperusta, jonka uudet Human Resourcesin toiminnot vapautetaan osana yhden version vakiopäivitysprosessia.
    - Tapa, jolla parannuksia, päivityksiä ja korjauksia sovelletaan ympäristöihin, on yhdenmukainen.

- [Laajennettavuusvaihtoehtoja parannetaan.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options.md)

    - Voit jatkaa Microsoft Power Platform -työkalujen käyttöä tarpeen mukaan.
    - Toimintoja voi laajentaa lomakkeiden, taulujen, menetelmien ja sovellusohjelmaliittymien avulla.
    - Voit luoda ja laajentaa entiteettejä.

    Lisätietoja käytettävissä olevista laajennusvaihtoehdoista on [Dynamics 365:n laajennettavuuden yleiskatsaus](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) -kohdassa.

- [Luo yksi henkilöstöresurssitoimintojoukko Dynamics 365:ssä.](/dynamics365-release-plan/2021wave2/human-resources/create-one-set-human-resources-capabilities-within-dynamics-365.md)

    10.0.25-versiossa vain Human Resourcesin toiminnot on otettu käyttöön rahoitus- ja toiminta -infrastruktuurissa. Jotta asiakkaat voivat hyödyntää näitä rahoitus- ja toiminta -ympäristön toimintoja, seuraavien Human Resourcesin ominaisuuksien on oltava käytössä ominaisuuksien hallinnassa.

    | Toiminnon nimi | Yleiskuvaus | Vapautustila | 
    |--------------|----------|----------------| 
    | Palveluvuosien laskeminen | Asetusvaihtoehdon avulla voit valita päivämäärän, jota käytetään **Palveluvuosien** laskennassa. | Yleisesti saatavilla | 
    | Työnkulkukokemusten parannukset | Tämä ominaisuus parantaa työnkulkujen lähetysten ja hyväksyntöjen käyttökokemusta. | Yleisesti saatavilla | 
    | Tulosta suorituskykyarviot | Voit tulostaa suorituskykyyn liittyvät vaihtoehdot PDF-muodossa. | Yleisesti saatavilla | 
    | Mukautetut linkit **Esimiehen itsepalvelussa** | Voit luoda mukautettuja linkkejä, jotka näkyvät **Esimiehen itsepalvelun** **Liittyvät linkit** -osassa. | Yleisesti saatavilla | 
    | Yritystenvälinen kompensaationäkymä | Käyttäjät voivat tarkastella kompensaatiosuunnitelmia **Esimiehen itsepalvelussa** kaikkien yritysten välillä ilman, että yrityksiä ei tarvitse vaihtaa. | Yleisesti saatavilla | 
    | Määritä useita kompensaatiotasoja työn mukaan\*&dagger; | Töissä tuetaan nyt useita kompensaatiotasoja. | Yleisesti saatavilla | 
    | Tehtävienhallinta\* | Voit luoda tarkistusluetteloita ja tehtäviä perehdytys-, irtisanomis- ja siirtymisprosessille. | Esikatselu | 
    | Yksinkertaistettu työntekijän lisääminen | Tämä ominaisuus tarjoaa päivitetyn käyttökokemuksen aiemmin luodulla **Työntekijä**-sivulla. | Esikatselu | 
    | Henkilöstöhallinnon käyttäjäkokemuksen parannukset | Katso seuraavan osan taulu.  | Esikatselu | 

\*Tämä ominaisuus on otettava käyttöön, ennen kuin **Human resourcesin käyttäjäkokemusten parannustoiminto** on käytössä.

&dagger; Tätä toimintoa ei voi poistaa käytöstä sen jälkeen, kun ne on otettu käyttöön.

## <a name="human-resource-user-experience-enhancements"></a>Henkilöstöresurssien käyttökokemusten parannukset

| Toiminnon nimi | Yleiskuvaus | 
|--------------|----------| 
| Poista työsuhde | Voit poistaa työntekijän työsuhteen. | 
| Työluokat | Voit seurata ryhmää töitä, jotka vaativat samankaltaista koulutusta, taitoja, tietämystä ja osaamista. | 
| Lisätyökentät | Seuraavat kentät lisättiin: **Työsuhdeluokka**, **Työsuhteen tyyppi** ja **Työsuhteen tila**. | 
| **Työntekijät, joilla ei työsuhdetta** -sivu | Sivulla on luettelo työntekijöistä, joilla ei ole työtietuetta. | 
| Toimidimension käyttäjäkokemuksen päivitys | Käyttäjäkokemus on paranneltu, kun toimidimensiot määritetään oikeushenkilöä kohti. | 
| Osoitteen muutokset **henkilöstöhallinnan** työtilassa | Tämä ominaisuus näyttää kaikkien osoitteenmuutosten lukumäärän, jotka tapahtuivat tietyn päivän aikana **Human resources -parametrit** -sivulla määritetyllä tavalla. | 
| Vanhentuvat tietueet **henkilöstöhallinnan** työtilassa | Tämä ominaisuus sisältää luettelon nimikkeistä, jotka ovat vanhentuneet tai vanhenevat todistuksia, tunnisteita, ehdotuksia, seulontoja tai testejä varten. | 
| **Toimihierarkian oikeellisuustarkistus** -sivu | Kehäviittauksia tehdään tarkistustoimirivin hierarkiassa. | 
| Maa- ja aluekohtaiset palkanlaskentatiedot | **Työntekijän työsuhde** -sivulla on käytettävissä palkanlaskennan lisäkenttiä sen mukaan, missä maassa tai alueella työntekijä työskentelee. | 
| Yhteensopivuusraportoinnin parannukset | Lisäraportointivaihtoehdot ovat saatavilla EEO-1:lle, Vets 4212:lle ja OSHA300a:lle. | 
| Päivitykset **Henkilöstön hallinta** -työtilaan | Päivitykset on tehty osoitemuutosten ja erääntymistietueiden seuraamista varten. Lisäksi uusissa välilehdissä on luettelo työntekijä- ja toimitoiminnoista. | 
