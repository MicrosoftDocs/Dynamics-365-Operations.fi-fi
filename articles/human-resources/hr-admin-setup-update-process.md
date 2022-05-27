---
title: Päivitysprosessi
description: Microsoft Dynamics 365 Human Resourceson todellinen ohjelmisto palveluna (SaaS), joka tarjoaa jatkuvia ja kosketusvapaita palvelupäivityksiä sovellus- ja ympäristömuutoksille.
author: twheeloc
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1b9ab27b443e5ec675ea03e13aa7be4ea84bfb45
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722238"
---
# <a name="update-process"></a>Päivitysprosessi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Microsoft Dynamics 365 Human Resourceson todellinen ohjelmisto palveluna (SaaS), joka tarjoaa jatkuvia ja kosketusvapaita palvelupäivityksiä. Nämä päivitykset sisältävät sekä sovellus -että ympäristömuutoksia, jotka usein tarjoavat tärkeitä parannuksia palveluun, lakisääteiset päivitykset mukaan luettuna.

## <a name="update-policy"></a>Päivityskäytäntö

Päivitykset julkaistaan säännöllisesti kaikkiin ympäristöihin. Human Resourcesia tuetaan [Microsoftin elinkaarikäytännön](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) mukaisesti. Se tarjoaa johdonmukaisia ja ennakoitavia ohjeita tuen saatavuudesta.

## <a name="release-cadence"></a>Päivitysväli 

Human Resources -päivitykset tehdään kaikissa ympäristöissä automaattisesti. Human Resourcesiin liittyy kahdenlaisia julkaisuja:

- **Palvelupäivitykset**: Kahden viikon välein ilmestyvät päivitykset, joissa on virheiden korjauksia ja uusia toimintoja. Palvelupäivityksiin kuuluvat myös soveltuvat Platformin päivitykset, kun ne julkaistaan. Lisätietoja ympäristön julkaisuista esitetään kohdassa [Käyttöympäristöpäivitysten uudet ja muuttuneet ominaisuudet](../fin-ops-core/dev-itpro/get-started/whats-new-home-page.md). Kahdesti viikossa ilmestyvillä päivityksillä on vaiheittainen maailmanlaajuinen käyttöönotto alueiden välillä. Lisätietoja kahdesti viikossa ilmestyvistä päivityksistä esitetään kohdassa [Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md).

    Kaikki tuetut palvelinkeskukset päivittyvät kahden viikon välein, ellei muuta mainita. Alueet Yhdysvallat, Australia, Eurooppa, Yhdistynyt kuningaskunta ja Kanada kuuluvat kahdesti viikossa ilmestyvien päivitysten piiriin. 

- **Dataverse -ratkaisujen päivitykset**: Nämä päivitykset suoritetaan noin kuuden viikon välein tarpeen mukaan. Niihin kuuluu uusia yksikköjä ja muutoksia olemassa oleviin yksikköihin Dataversessä. Nämä päivitykset julkaistaan samoilla alueilla kuin kahdesti viikossa ilmestyvät päivitykset, ja niiden replikointi kaikissa palvelinkeskuksissa kestää noin kuusi viikkoa. Ratkaisupäivitykset saattavat olla linjassa kahdesti viikossa ilmestyvien palvelupäivitysten kanssa.

> [!NOTE]
> Ratkaisupäivitykset ovat käytettävissä kaikissa palvelinkeskuksissa, kun ne on julkaistu. Jos et halua odottaa päivitysten automaattista replikointia, voit suorittaa nämä päivitykset manuaalisesti minkä tahansa palvelinkeskuksen missä tahansa ympäristössä.

Tarvittaessa Human Resources tarjoaa myös seuraavanlaisia korjauksia:

- **Aliversio (hotfix)**: Ohjelmakorjauksia, jotka voidaan suorittaa joko kahdesti viikossa ilmestyvien palvelupäivitysjulkaisun yhteydessä tai erillään siitä

- **Hätäkorjaus**: ennakoivia ja reaktiivisia hotfix-korjauksia, jotka ovat luonteeltaan erillisiä, voivat sisältää vain määritykseen tai koodiin kohdistuvia muutoksia käytössä olevan sivun ongelmien ratkaisemiseksi ja voidaan suorittaa erillään kahdesti viikossa ilmestyvistä palvelupäivitysjulkaisuista

Julkaisut tarkistetaan, testataan ja vahvistetaan sisäisessä ympäristössä. Kun koontiversiot on hyväksytty, ne otetaan käyttöön tuotannossa.

## <a name="release-cadence-exceptions-in-2021"></a>Vapauta tahtipoikkeukset vuonna 2021

Lomien vuoksi vuoden 2021 marraskuun ja joulukuun julkaisuaikataulu on seuraava:

- Marraskuun julkaisu: 1.11.–14.11.
- Joulukuun julkaisu: 29.11.–12.12.
 
Kahden viikon julkaisuväli jatkuu tavalliseen tapaan 10.1.2022.

## <a name="communications"></a>Viestintä

Tietoa siitä, mitä Human Resourcesin osalta suunnitellaan ja mitä siihen liittyen on julkaistu, saat seuraavista paikoista:

- [Dynamics 365 Human Resourcesin toteutussuunnitelma](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365:n julkaisusuunnitelmat](/dynamics365/release-plans/)

- [Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)

- [Lifecycle Servicesin (LCS) ongelmahaku](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (vain Platformiin liittyvät virheet)

- [Human Resources -blogi](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resourcesin Yammer-yhteisö](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Ominaisuuksien esikatselu eristysympäristössä

Voit varmentaa esikatseluominaisuudet eristysympäristössä, ennen kuin otat ne käyttöön tuotantoympäristössä. Lisätietoja uusien ominaisuuksien käyttöönotosta on kohdassa [ominaisuuksien hallinnan yleiskuvaus](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Kaikki uudet toiminnot pysyvät esiversiossa ainakin 30 päivää ja yleensä 30–60 päivää. Tärkeimmät toiminnot ovat yleensä saatavana kunkin vuoden lokakuussa ja huhtikuussa esiversiojakson jälkeen. Voit ottaa uudet ominaisuudet käyttöön heti, kun näet ne Toimintojen hallinta -työtilassa. Jotkin toiminnot on ehkä otettu käyttöön oletusarvoisesti.

Joskus keskeinen toiminto on otettu käyttöön oletusarvoisesti eikä sitä voi poistaa käytöstä (esimerkiksi Toimintojen hallinta -työtilassa).

Kun toiminto on yleisesti saatavana, se voidaan ottaa käyttöön tai poistaa käytöstä tuotantoympäristöissä. Toimintojen hallinta -työtila ilmaisee, milloin esiversiotoiminto tulee pakolliseksi. Tämä päivämäärä on yleensä 1. lokakuuta tai 1. huhtikuuta eli ne vastaavat puolivuotisia julkaisusuunnitelmia. Pakollisia toimintoja ei voi poistaa käytöstä. Toiminnon voi ottaa käyttöön ja poistaa käytöstä kaikissa ympäristöissä siihen saakka, että muuttuu pakolliseksi.

Suosittelemme vahvasti ominaisuuksien esikatselua eristys- tai kokeiluympäristössä. On parasta luoda kopio nykyisestä tuotantoympäristöstä tai tietokannasta eristetyssä ympäristössä, jotta voit tutustua uusien ominaisuuksien kokonaiskokemukseen tietojasi käyttäen.

Lisä tietoja eristysympäristön valmistelemisesta on kohdassa [Human Resources -projektin valmistelu](hr-admin-setup-provision.md). Katso kokeiluympäristön poistamista varten [Poista esiintymä](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Virheistä ilmoittaminen

Kun testaat esikatseluominaisuuksia tai kokeilet uusia toimintoja, saatat löytää asioita, jotka eivät toimi odotetulla tavalla. Ilmoita kaikista virheistä [Microsoft Dynamics 365 -tuen](https://dynamics.microsoft.com/support/) avulla.

## <a name="see-also"></a>Lisätietoja

[Dynamics 365:n ja Power Platformin julkaisusuunnitelmat](/dynamics365/release-plans)</br>
[Dynamics 365 Human Resourcen uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Ohjelmiston elinkaarikäytäntö](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
