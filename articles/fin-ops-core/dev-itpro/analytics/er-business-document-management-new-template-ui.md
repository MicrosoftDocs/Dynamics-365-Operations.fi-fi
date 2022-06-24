---
title: Microsoft Office -tyylin käyttöliittymä liiketoiminta-asiakirjan hallinnassa (sisältää videon)
description: Tässä artikkelissa kerrotaan, kuinka uutta käyttöliittymää käytetään sähköisen raportoinnin (ER) kehyksen yritysasiakirjojen hallintatoiminnossa.
author: v-anamir
ms.date: 01/05/2022
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
ms.openlocfilehash: bcc464a17e27393c5904c59b8439de6ca000d57a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892222"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Microsoft Office -tyylin käyttöliittymä liiketoiminta-asiakirjan hallinnassa

[!include [banner](../includes/banner.md)]

Liiketoiminta-asiakirjojen hallinnan avulla yrityskäyttäjät voivat muokata liiketoiminta-asiakirjamalleja Microsoft Office 365 -palvelun tai asianmukaisen Microsoft Office -työpöytäsovelluksen avulla. Muokkauksia voivat olla esimerkiksi suunnittelumuutoksia tai uusia käyttöönottoja. Käyttäjät voivat myös lisätä paikkamerkkejä tietojen lisäämiseksi ilman lähdekoodin muuttamista. Lisätietoja liiketoiminta-asiakirjojen hallinnan käyttämisestä on kohdassa [Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md).

Uusi käyttöliittymä on selkeämpi ja mukavampi käyttää. **Yritystiedosto** alue näyttää vain nykyisen [aktiivisen](tasks/er-configuration-provider-mark-it-active-2016-11.md) [tarjoajan](general-electronic-reporting.md#Provider) omistamia malleja, jotka sijaitsevat nykyisessä Dynamics 365 Finance -esiintymässä. Edellisessä käyttöliittymässä **Malli**-välilehdessä luetellaan kaikki mallit, jotka olivat kaikkien palveluntarjoajien käytettävissä. Lisäksi se on näyttänyt kaikki kaikkien niiden käyttäjien luomat ja muokatut mallit, joilla on sama rooli.

**Liiketoiminta-asiakirjan hallinta** -työtilan **Uusi tiedosto** -painikkeen avulla voit luoda ja muokata mallia [sähköisen raportoinnin (ER) ](general-electronic-reporting.md) muodon [konfiguraatiossa](general-electronic-reporting.md#Configuration), jonka toinen tarjoaja sijaitsee nykyisessä Finance-esiintymässä, tai lataa uusi malli Excel-työkirjasta. Lisäksi versiossa 10.0.25 ja sitä myöhemmässä versiossa voit luoda ja muokata **Uusi tiedosto** -painikkeen avulla mallia [yleiseen tietovarastoon](general-electronic-reporting.md#Repository) tallennetussa ER-muodossa.

Tämän artikkelin esimerkeissä aktiivinen toimittaja on Contoso ja luot sen avulla mallin, joka perustuu Microsoftin toimittamaan malliin. Vaihtoehtoisesti voit luoda mallin lataamalla oman mallisi Excel-muodossa.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

[Luo uusi liiketoiminta-asiakirja käyttämällä Liiketoimintatiedostojen hallinta](https://youtu.be/gAIYl-mM_pw) -video (näkyy yllä) on lisätty [Taloushallinnon ja toimintojen toistolistalle](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavilla YouTubessa.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Uuden liiketoiminta-asiakirjojen hallinnan asiakirjojen käyttöliittymän käyttöön tarjoaminen

Aloittaaksesi uuden asiakirjojen käyttöliittymän käyttämisen liiketoiminta-asiakirjojen hallinnassa sinun on otettava **Officea muistuttava käyttöliittymäkokemus liiketoiminta-asiakirjojen hallintaan** -toiminto käyttöön **Ominaisuuksien hallinta** -työtilassa.

Noudata seuraavia ohjeita ottaaksesi tämän ominaisuuden käyttöön kaikille yrityksille.

1. Valitse **Ominaisuuksien hallinta** -työtila **Kaikki** -välilehden luettelosta **Officea muistuttava käyttöliittymäkokemus liiketoiminta-asiakirjojen hallintaan** -ominaisuus.
2. Ota valittu toiminto käyttöön valitsemalla **Ota käyttöön nyt**.
3. Voit avata uuden toiminnon päivittämällä sivun.

## <a name="add-or-activate-a-provider"></a>Lisää tai aktivoi toimittaja

Jokainen liiketoimintatiedoston malli tallennetaan ER-muodon konfiguraatiossa, joka on merkitty tietyn konfiguraation tarjoajan omistamaksi. Kun luot uuden mallin, siihen luodaan uusi ER-muotokonfiguraatio. Siksi tätä konfiguraatiota varten on oltava määritetty toimittaja. Tähän tarkoitukseen käytetään ER-kehyksen aktiivista tarjoajaa. Jos ER:ssä ei ole toimittajaa, voit luoda sen. Jos *aktiivista* tarjoajaa ei ole, voit aktivoida yhden olemassa olevista tarjoajista. Näyttöön tulee tarvittaessa valintaikkuna, jossa voit lisätä tai aktivoida palveluntarjoajan, kun aloitat uuden mallin lisäämisen.

### <a name="add-a-new-provider"></a>Lisää uusi palveluntarjoaja

Voit luoda uuden tarjoajan noudattamalla seuraavia **Konfigurointipalvelu**-ikkunan vaiheita:

1.  Kirjoita uuden tarjoajan nimi **Valitse konfiguraatiopalvelu** -välilehden **Nimi**-kenttään.
2.  Kirjoita **Internet-osoite**-kenttään uuden toimittajan verkkopalveluosoite (URL). 
3.  Valitse **OK**.

    ![Uuden tarjoajan luominen liiketoiminta-asiakirjan hallinnassa.](./media/bdm_create_provider.png)

Lisätty tarjoaja aktivoidaan automaattisesti.

### <a name="activate-a-provider"></a>Tarjoajan aktivoiminen

Voit aktivoida tarjoajan noudattamalla seuraavia **Konfigurointipalvelu**-ikkunan vaiheita:

1.  Valitse tarjoaja **Valitse konfiguraatiopalvelu** -välilehden **Konfiguraatiopalvelu**-kentässä.
2.  Valitse **OK**.

    ![Tarjoajan aktivoiminen liiketoiminta-asiakirjan hallinnassa.](./media/bdm_choose_provider.png)

Valittu tarjoaja aktivoidaan.

> [!NOTE]
> Kukin liiketoimintatiedostojen hallintamalli sijaitsee ER-muotokonfiguraatiossa, joka viittaa toimittajaan konfiguraation tekijänä. Siksi kussakin mallissa tarvitaan aktiivista toimittajaa.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Muokkaa toisen toimittajan omistamaa mallia

Tässä esimerkissä kerrotaan, miten voit **Liiketoiminta-asiakirjan hallinta** -työtilan **Uusi tiedosto** -painikkeen avulla luoda ja muokata mallia ER-muotokonfiguraatiossa, jonka toinen tarjoaja sijaitsee nykyisessä Finance-esiintymässä. Tässä esimerkissä aktiivinen toimittaja on Contoso, joka käyttää Microsoftin toimittamaa ER-muotokonfiguraatiota. Kun olet valinnut **Uusi tiedosto**, **Luo uusi malli** -sivun **Valitse**-välilehdessä näkyvät kaikki nykyisen Finance-instanssin mallit, jotka nykyinen tarjoaja ja muut toimittajat omistavat. Avaa malli valitsemalla se. Tämän jälkeen voit luoda mallista uuden muokattavan kopion. Muokattu malli tallennetaan uuteen ER-muotokonfiguraatioon, joka luodaan automaattisesti.

1. Valitse **Liiketoiminta-asiakirjan hallinta** -työtilassa **Uusi asiakirja**.

    ![Liiketoiminta-asiakirjojen hallinnan työtila.](./media/BDM_overview_new_template1.png)

2. Valitse **Luo uusi malli** -sivun **Valitse**-välilehdestä tiedosto, jota haluat käyttää mallina, ja valitse sitten **Luo tiedosto**.

    ![Liiketoiminta-asiakirjojen valintaruutu.](./media/BDM_overview_new_template2.png)

3. Vaihda otsikkoa uuden valintaruudun **Otsikko**-kentässä tarpeesi mukaan. Otsikkotekstin avulla voit nimetä automaattisesti luotavan uuden ER-muotomäärityksen. Huomaa, että tämän määrityksen luonnosta (**Asiakkaan FTI-raportti (GER) Copy**), joka sisältää muokatun mallin, käytetään suorittamaan tämä ER-muoto nykyiselle käyttäjälle. ER-perusmuotomäärityksen alkuperäistä mallia käytetään tämän ER-muodon suorittamiseen kaikille muille käyttäjälle.
4. Vaihda **Nimi** -kenttään automaattisesti luotavan muokattavan mallin ensimmäisen version nimi.
5. Päivitä huomautukset **Kommentti**-kenttään automaattisesti luotavan muokattavan mallin uuden version huomautukset.
6. Vahvista muokkausprosessin aloittaminen valitsemalla **OK**.

    ![Tiedoston luonnin valintaruutu.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Aiemmin luotua Excel-työkirjaa käyttävän mallin lataaminen

Tässä esimerkissä kerrotaan, miten voit **Liiketoiminta-asiakirjan hallinta** -työtilan **Uusi tiedosto** -painikkeen avulla luoda ja muokata mallia ER-muotokonfiguraatiossa perustuen käytettävissä olevaan Excel-työkirjaan. Tässä esimerkissä aktiivinen toimittaja on Contoso ja käytät Microsoftin toimittamaa ER-[tietomallia](er-overview-components.md#data-model-component) ja ER-[mallimääritysten](er-overview-components.md#model-mapping-component) konfiguraatiota. Kun olet valinnut **Uusi tiedosto**, valitse **Lataa**-välilehti **Luo uusi malli** -sivulla. Siinä voit määrittää Excel-työkirjan lataamisen tiedot. Kun olet ladannut Excel-työkirjan, se muunnetaan muokattavaksi liiketoimintatiedostomalliksi. Muokattu malli tallennetaan uuteen ER-muotokonfiguraatioon, joka luodaan automaattisesti.

Noudata näitä ohjeita, kun haluat antaa tarvittavat tiedot ennen mallin lataamista.

1. Valitse **Liiketoiminta-asiakirjan hallinta** -työtilassa **Uusi asiakirja**.
2. Valitse **Luo uusi malli** -sivun **Palvelimeen lataaminen** -välilehden **Malli**-välilehdestä **Etsi selaamalla** ja valitse malliksi käytettävä Excel-tiedosto. **Malli**-osan **Otsikko**- ja **Kuvaus**-kentät täytetään automaattisesti. Ne määrittävät uuden automaattisesti luotavan ER-muotokonfiguraation nimen ja kuvauksen. Voit muokata näitä kenttiä tarpeen mukaan.
3. Määritä **Tiedostotyyppi**-osan **Nimi**-kenttään liiketoimintatiedoston tyyppi. Tätä arvoa käytetään oikean tietolähteen haussa (ER-mallin konfiguraatiossa).

    ![Malli-välilehti Luo uusi malli -sivun Lataa-välilehdessä.](./media/BDM_overview_new_UI_import_21.jpg)

4. Valitse **Tietolähde**-välilehden **Suodatin**-pikavälilehdestä **Käytä suodatinta**. **Tietolähde**-osassa **Nimi**-kenttä täytetään automaattisesti. Voit myös valita arvon manuaalisesti. Voit etsiä tietolähteen nimeä nimen, kuvauksen, maa-/aluekoodin ja liiketoimintatiedostotyypin perusteella suodattimen avulla.

    ![Tietolähde-välilehti Luo uusi malli -sivun Lataa-välilehdessä.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > **Suodatin**-pikavälilehteä käytetään oikean tietolähteen haussa (ER-mallin konfiguraatiossa). Voit etsiä lataatavalle tiedostolle sopivimman tietolähteen muokkaamalla kaikkia suodatinkenttiä.
    > 
    > **Suodata**-pikavälilehden ehtoja käytetään **TAI**-ehtona.

5. Valitse **Yhdistämismääritys**-välilehdessä **Automaattinen havainnointi**. **Juurimääritys**-kenttä täytetään automaattisesti. Voit myös valita arvon manuaalisesti. Tässä välilehdessä näytetään mallin ja mallin elementtien lopetusmääritys.

    ![Yhdistämismääritys-välilehti Luo uusi malli -sivun Lataa-välilehdessä.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > **Mallirakenne**-osan määrityksessä käytetään täysin tietolähteen otsikoita tai kuvauksia käyttäjän kielellä ja mallin matkapuhelinnimessä.

6. Valitse **Luo tiedosto**, kun haluat vahvistaa, että haluat luoda mallin, ja aloittaa muokkausprosessin.

Lisätietoja on kohdassa [Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Mallin lataaminen yleisestä säilöstä

Tässä esimerkissä kerrotaan, miten voit **Liiketoiminta-asiakirjan hallinta** -työtilan **Uusi tiedosto** -painikkeen avulla luoda ja muokata mallia ER-muotokonfiguraatiossa, jonka tarjoaja on Microsoft ja joka sijaitsee nykyisessä yleisessä säilössä. Tässä esimerkissä aktiivinen toimittaja on Contoso, joka käyttää Microsoftin toimittamaa ER-muotokonfiguraatiota. Kun olet valinnut **Uusi tiedosto**, **Luo uusi malli** -sivun **Tuo yleisestä säilöstä** -välilehdessä näkyvät kaikki liiketoimintatiedostomallit, jotka on tallennettu yleistietovarastoon mutta puuttuvat nykyisestä Finance-instanssista. Kun olet valinnut mallin, se tuodaan yleistietovarastosta nykyiseen Finance-esiintymään ja uusi muokattavissa oleva kopio luodaan. Muokattu malli tallennetaan uuteen ER-muotokonfiguraatioon, joka luodaan automaattisesti.

1. Valitse **Liiketoiminta-asiakirjan hallinta** -työtilassa **Uusi asiakirja**.
2. Valitse **Luo uusi malli** -sivun **Tuon yleisestä säilöstä**-välilehdestä tiedosto, jota haluat käyttää mallina, ja valitse sitten **Luo tiedosto**.

    ![Luo uusi malli -sivun Tuo yleisestä säilöstä -välilehti.](./media/BDM_overview_new_template22.png)

3. Vahvista sanomaruudussa **Kyllä**, että haluat tuoda valitun tiedoston yleistietovarastosta nykyiseen Finance-esiintymään. Jos järjestelmä pyytää lupaa, noudata näyttöön tulevia ohjeita.
4. Vaihda otsikkoa uuden valintaruudun **Otsikko**-kentässä tarpeesi mukaan. Otsikkotekstin avulla voit nimetä automaattisesti luotavan uuden ER-muotomäärityksen. Huomaa, että tämän määrityksen luonnosta (**Maksukehotus (Excel) Copy**), joka sisältää muokatun mallin, käytetään suorittamaan tämä ER-muoto nykyiselle käyttäjälle. ER-perusmuotomäärityksen alkuperäistä mallia käytetään tämän ER-muodon suorittamiseen kaikille muille käyttäjälle.
5. Vaihda **Nimi** -kenttään automaattisesti luotavan muokattavan mallin ensimmäisen version nimi.
6. Päivitä huomautukset **Kommentti**-kenttään automaattisesti luotavan muokattavan mallin uuden version huomautukset.
7. Vahvista muokkausprosessin aloittaminen valitsemalla **OK**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
