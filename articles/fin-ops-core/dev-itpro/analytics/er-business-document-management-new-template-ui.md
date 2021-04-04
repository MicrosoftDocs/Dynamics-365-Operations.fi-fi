---
title: Uusi asiakirjojen käyttöliittymä liiketoiminta-asiakirjojen hallinnassa
description: Tässä aiheessa on tietoja uuden asiakirjojen käyttöliittymän käyttämisestä sähköisen raportoinnin liiketoiminta-asiakirjojen hallintatoiminnossa.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f8099f2f6872c34c30de918a6fc5fd27bcde958
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565707"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Uuden asiakirjan käyttöliittymä liiketoiminta-asiakirjan hallinnassa

[!include [banner](../includes/banner.md)]

Liiketoiminta-asiakirjojen hallinnan avulla yrityskäyttäjät voivat muokata liiketoiminta-asiakirjamalleja Microsoft 365 -palvelun tai asianmukaisen Microsoft Office -työpöytäsovelluksen avulla. Muokkauksia voivat olla esimerkiksi suunnittelumuutoksia tai uusia käyttöönottoja. Käyttäjät voivat myös lisätä paikkamerkkejä tietojen lisäämiseksi ilman lähdekoodin muuttamista. Lisätietoja liiketoiminta-asiakirjojen hallinnan käyttämisestä on kohdassa [Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md).

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]