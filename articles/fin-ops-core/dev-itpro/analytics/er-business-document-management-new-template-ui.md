---
title: Microsoft Office -tyylin käyttöliittymä liiketoiminta-asiakirjan hallinnassa (sisältää videon)
description: Tässä ohjeaiheessa kerrotaan, kuinka uutta käyttöliittymää käytetään sähköisen raportoinnin (ER) kehyksen yritysasiakirjojen hallintatoiminnossa.
author: v-anamir
ms.date: 04/12/2021
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
ms.openlocfilehash: b0c481e73daf74803d3582e4089e76dcd383e8a4
ms.sourcegitcommit: ef0dd4245fc499907ffe00e2a32f59a6cd96e45d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/18/2021
ms.locfileid: "7937553"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Microsoft Office -tyylin käyttöliittymä liiketoiminta-asiakirjan hallinnassa

[!include [banner](../includes/banner.md)]

Liiketoiminta-asiakirjojen hallinnan avulla yrityskäyttäjät voivat muokata liiketoiminta-asiakirjamalleja Microsoft 365 -palvelun tai asianmukaisen Microsoft Office -työpöytäsovelluksen avulla. Muokkauksia voivat olla esimerkiksi suunnittelumuutoksia tai uusia käyttöönottoja. Käyttäjät voivat myös lisätä paikkamerkkejä tietojen lisäämiseksi ilman lähdekoodin muuttamista. Lisätietoja liiketoiminta-asiakirjojen hallinnan käyttämisestä on kohdassa [Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md).

Uusi käyttöliittymä on selkeämpi ja mukavampi käyttää. **Liiketoiminta asiakirja** -alueella näkyvät vain ne mallit, jotka ovat käytettävissä kulloisenkin toimittajan osalta. Edellisessä käyttöliittymässä **Malli**-välilehdessä luetellaan kaikki mallit, jotka olivat kaikkien palveluntarjoajien käytettävissä. Lisäksi se on näyttänyt kaikki kaikkien niiden käyttäjien luomat ja muokatut mallit, joilla on sama rooli.

Voit käyttää **Uusi asiakirja** -painiketta luodaksesi ja muokataksesi mallia sähköisen raportoinnin (ER) muotomäärityksessä, joka on peräisin toiselta toimittajalta. Tämän ohjeaiheen esimerkissä toimittaja on Microsoft. Vaihtoehtoisesti voit luoda mallin lataamalla oman mallisi Excel-muodossa.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

[Luo uusi liiketoiminta-asiakirja käyttämällä edellä kuvattua Liiketoimintatiedostojen hallinta](https://youtu.be/gAIYl-mM_pw) -videoa (näkyy yllä) on lisätty [Finance and Operations -soittolistalle](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavilla YouTubessa.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Uuden liiketoiminta-asiakirjojen hallinnan asiakirjojen käyttöliittymän käyttöön tarjoaminen

Aloittaaksesi uuden asiakirjojen käyttöliittymän käyttämisen liiketoiminta-asiakirjojen hallinnassa sinun on otettava **Officea muistuttava käyttöliittymäkokemus liiketoiminta-asiakirjojen hallintaan** -toiminto käyttöön **Ominaisuuksien hallinta** -työtilassa.

Noudata seuraavia ohjeita ottaaksesi tämän ominaisuuden käyttöön kaikille yrityksille.

1. Valitse **Ominaisuuksien hallinta** -työtila **Kaikki** -välilehden luettelosta **Officea muistuttava käyttöliittymäkokemus liiketoiminta-asiakirjojen hallintaan** -ominaisuus.
2. Ota valittu toiminto käyttöön valitsemalla **Ota käyttöön nyt**.
3. Voit avata uuden toiminnon päivittämällä sivun.

## <a name="edit-templates-that-are-owned-by-other-providers"></a>Muokkaa muiden toimittajien omistamia malleja

1. Valitse **Liiketoiminta-asiakirjan hallinta** -työtilassa **Uusi asiakirja**.

    ![Liiketoiminta-asiakirjojen hallinnan työtila.](./media/BDM_overview_new_template1.png)

2. Valitse **Valitse**-valintaruudussa mallina käytettävä asiakirja ja sitten **Luo tiedosto**.

    ![Liiketoiminta-asiakirjojen valintaruutu.](./media/BDM_overview_new_template2.png)

3. Vaihda otsikkoa uuden valintaruudun **Otsikko**-kentässä tarpeesi mukaan. Otsikkotekstin avulla voit nimetä automaattisesti luotavan uuden ER-muotomäärityksen. Huomaa, että tämän määrityksen luonnosta (**Asiakkaan FTI-raportti (GER) Copy**), joka sisältää muokatun mallin, käytetään suorittamaan tämä ER-muoto nykyiselle käyttäjälle. ER-perusmuotomäärityksen alkuperäistä mallia käytetään tämän ER-muodon suorittamiseen kaikille muille käyttäjälle.
4. Vaihda **Nimi** -kenttään automaattisesti luotavan muokattavan mallin ensimmäisen version nimi.
5. Päivitä huomautukset **Kommentti**-kenttään automaattisesti luotavan muokattavan mallin uuden version huomautukset.
6. Vahvista muokkausprosessin aloittaminen valitsemalla **OK**.

    ![Tiedoston luonnin valintaruutu.](./media/BDM_overview_new_template3.png)

**Uusi asiakirja** -painiketta käytetään luomaan ja muokkaamaan mallia toisen toimittajan toimittamassa ER-muotomäärityksessä. Tässä esimerkissä toimittajana on Microsoft. Kun valitset **Uusi tiedosto**, näet kaikki nykyisen toimittajan tai muiden toimittajien omistamat mallit. Kun olet valinnut mallin, se avautuu muokattavaksi. Muokattu malli tallennetaan sen jälkeen uuteen ER-muotokonfiguraatioon, joka luodaan automaattisesti.

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>Aiemmin luotua Excel-muotoa käyttävän mallin lataaminen
Noudata näitä ohjeita, kun haluat antaa tarvittavat tiedot ennen mallin lataamista.

1. Valitse **Liiketoiminta-asiakirjan hallinta** -työtilassa **Uusi asiakirja**.

    ![Liiketoiminta-asiakirjojen hallinnan työtila.](./media/BDM_overview_new_template1.png)
    
2. Valitse **Luo uusi malli** -sivun **Palvelimeen lataaminen** -välilehden **Malli**-välilehdestä **Etsi selaamalla** ja valitse malliksi käytettävä Excel-tiedosto. **Malli**-osan **Otsikko**- ja **Kuvaus**-kentät täytetään automaattisesti. Ne määrittävät uuden automaattisesti luotavan ER-muotokonfiguraation nimen ja kuvauksen. Voit muokata näitä kenttiä tarpeen mukaan.
3. Määritä **Tiedostotyyppi**-osan **Nimi**-kenttään liiketoimintatiedoston tyyppi. Tätä arvoa käytetään oikean tietolähteen haussa (ER-mallin konfiguraatiossa).

    ![Malli-välilehti.](./media/BDM_overview_new_UI_import_21.jpg)

4. Valitse **Tietolähde**-välilehden **Suodatin**-pikavälilehdestä **Käytä suodatinta**. **Tietolähde**-osassa **Nimi**-kenttä täytetään automaattisesti. Voit myös valita arvon manuaalisesti. Voit etsiä tietolähteen nimeä nimen, kuvauksen, maa-/aluekoodin ja liiketoimintatiedostotyypin perusteella suodattimen avulla.

    ![Tietolähde-välilehti.](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > **Suodatin**-pikavälilehteä käytetään oikean tietolähteen haussa (ER-mallin konfiguraatiossa). Voit etsiä lataatavalle tiedostolle sopivimman tietolähteen muokkaamalla kaikkia suodatinkenttiä.
    > 
    > **Suodata**-pikavälilehden ehtoja käytetään **TAI**-ehtona.
    
5. Valitse **Yhdistämismääritys**-välilehdessä **Automaattinen havainnointi**. **Juurimääritys**-kenttä täytetään automaattisesti. Voit myös valita arvon manuaalisesti. Tässä välilehdessä näytetään mallin ja mallin elementtien lopetusmääritys.

    ![Määritys-välilehti.](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > **Mallirakenne**-osan määrityksessä käytetään täysin tietolähteen otsikoita tai kuvauksia käyttäjän kielellä ja mallin matkapuhelinnimessä.

6. Valitse **Luo tiedosto**, kun haluat vahvistaa, että haluat luoda mallin, ja aloittaa muokkausprosessin.

Lisätietoja on kohdassa [Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md).

Jos sähköisessä raportoinnissa ei ole toimittajaa, voit luoda sen. Jos aktiivista palveluntarjoajaa ei ole, voit aktivoida sen.

- Jos haluat luoda tarjoajan, muuta tarjoajan nimi **Nimi**-kentässä, päivitä uuden tarjoajan **Internet-osoite** kenttään ja vahvista valitsemalla **OK**.

    ![Uuden tarjoajan luominen BDM:ssä.](./media/bdm_create_provider.png)
    
- Voit aktivoida aiemmin luodun tarjoajan valitsemalla **Konfigurointipalvelu**-kentästä tarjoajan nimen ja valitsemalla **OK**, jos haluat määrittää tarjoajan aktiiviseksi.

    ![Tarjoajan aktivoiminen BDM:ssä.](./media/bdm_choose_provider.png)

> [!NOTE]
> Kunkin BDM-malli viittaa palveluntarjoajaan kokoonpanon tekijänä. Siksi mallissa tarvitaan aktiivista toimittajaa.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
