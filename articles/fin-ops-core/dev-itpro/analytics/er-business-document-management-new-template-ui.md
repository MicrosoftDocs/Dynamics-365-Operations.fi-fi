---
title: Uusi asiakirjojen käyttöliittymä liiketoiminta-asiakirjojen hallinnassa
description: Tässä ohjeaiheessa on tietoja uuden asiakirjojen käyttöliittymän (UI) käyttämisestä sähköisen raportoinnin (ER) kehyksen liiketoiminta-asiakirjojen hallintaominaisuuden käyttämisestä.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4acde9703c721ab7c20d1603299a10dda91b23c4
ms.sourcegitcommit: b8f8ccab2cd9d848e5ecd71caaf0a63237e2236b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2020
ms.locfileid: "2957060"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Uusi asiakirjojen käyttöliittymä liiketoiminta-asiakirjojen hallinnassa

[!include [banner](../includes/banner.md)]

Liiketoiminta-asiakirjojen hallinnan avulla yrityskäyttäjät voivat muokata liiketoiminta-asiakirjamalleja Microsoft Office 365 -palvelun tai asianmukaisen Microsoft Office -työpöytäsovelluksen avulla. Muokkauksia voivat olla esimerkiksi suunnittelumuutoksia tai uusia käyttöönottoja. Käyttäjät voivat myös lisätä paikkamerkkejä tietojen lisäämiseksi ilman lähdekoodin muuttamista. Lisätietoja liiketoiminta-asiakirjojen hallinnan käyttämisestä on kohdassa [Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md).

Uusi asiakirjojen käyttöliittymä on selkeämpi ja mukavampi käyttää. **Liiketoiminta asiakirja** -alueella näkyvät vain ne mallit, jotka ovat käytettävissä kulloisenkin toimittajan osalta.

**Uusi asiakirja** -painikkeen käyttäjät voivat luoda ja muokata mallia sähköisen raportoinnin (ER) muotomäärityksessä, joka on peräisin toiselta toimittajalta. Tämän ohjeaiheen esimerkissä toimittaja on Microsoft.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Uuden liiketoiminta-asiakirjojen hallinnan asiakirjojen käyttöliittymän käyttöön tarjoaminen

Aloittaaksesi uuden asiakirjojen käyttöliittymän käyttämisen liiketoiminta-asiakirjojen hallinnassa sinun on otettava **Officea muistuttava käyttöliittymäkokemus liiketoiminta-asiakirjojen hallintaan** -toiminto käyttöön **Ominaisuuksien hallinta** -työtilassa.

Noudata seuraavia ohjeita ottaaksesi tämän ominaisuuden käyttöön kaikille yrityksille.

1. Valitse **Ominaisuuksien hallinta** -työtila **Uusi** -välilehden luettelosta **Officea muistuttava käyttöliittymäkokemus liiketoiminta-asiakirjojen hallintaan** -ominaisuus.
2. Ota valittu toiminto käyttöön valitsemalla **Ota käyttöön nyt**.
3. Voit avata uuden toiminnon päivittämällä sivun.

### <a name="edit-templates-that-are-owned-by-other-providers"></a>Muokkaa muiden toimittajien omistamia malleja

1. Valitse **Liiketoiminta-asiakirjan hallinta** -työtilassa **Uusi asiakirja**.

    ![Liiketoiminta-asiakirjojen hallinnan työtila](./media/BDM_overview_new_template1.png)

2. Valitse valintaruudussa mallina käytettävä asiakirja ja sitten **Luo tiedosto**.

    ![Liiketoiminta-asiakirjojen valintaruutu](./media/BDM_overview_new_template2.png)

3. Vaihda otsikkoa uuden valintaruudun **Otsikko**-kentässä tarpeesi mukaan. Otsikkotekstin avulla voit nimetä automaattisesti luotavan uuden ER-muotomäärityksen. Huomaa, että tämän määrityksen luonnosta (**Asiakkaan FTI-raportti (GER) Copy**), joka sisältää muokatun mallin, käytetään suorittamaan tämä ER-muoto nykyiselle käyttäjälle. ER-perusmuotomäärityksen alkuperäistä mallia käytetään tämän ER-muodon suorittamiseen kaikille muille käyttäjälle.
4. Vaihda **Nimi** -kenttään automaattisesti luotavan muokattavan mallin ensimmäisen version nimi.
5. Päivitä huomautukset **Kommentti**-kenttään automaattisesti luotavan muokattavan mallin uuden version huomautukset.
6. Vahvista muokkausprosessin aloittaminen valitsemalla **OK**.

    ![Tiedoston luonnin valintaruutu](./media/BDM_overview_new_template3.png)

**Uusi asiakirja** -painiketta käytetään luomaan ja muokkaamaan mallia toisen toimittajan toimittamassa ER-muotomäärityksessä. Tässä esimerkissä toimittajana on Microsoft. Kun valitset **Uusi tiedosto**, näet kaikki nykyisen toimittajan tai muiden toimittajien omistamat mallit. Kun olet valinnut mallin, se avautuu muokattavaksi. Muokattu malli tallennetaan sen jälkeen uuteen ER-muotokonfiguraatioon, joka luodaan automaattisesti.

Lisätietoja on kohdassa [Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md).
