---
title: Tietojen kyseleminen Warehouse Management ‑mobiilisovelluksen kiertoteillä
description: Tässä artikkelissa kuvataan, kuinka tietoja kyselevät mobiililaitteen valikkovaihtoehdot määritetään ja kuinka niitä käytetään osana kiertoteitä.
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 39677ebfb9babeb7246ece4d27ab1813435ca12e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427845"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Tietojen kyseleminen Warehouse Management ‑mobiilisovelluksen kiertoteillä

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Ominaisuuden esittely

Warehouse Management -mobiilisovelluksen viivakoodien skannaamistoiminto mahdollistaa tietojen taltioimisen helposti ja tarkasti osana varastoprosesseja. Joskus viivakoodit kuitenkin vahingoittuvat ja muuttuvat lukukelvottomiksi, tai vaadittuja tietoja ei välttämättä ole viivakoodimuodossa liiketoimintaprosessien työnkuluissasi. Tällöin tietojen manuaalinen syöttäminen voi kestää kauan ja johtaa jopa virheellisten tietojen taltioimiseen. Tämä voi heikentää tuottavuutta ja palvelutasoa.

Tietojen joustavan kyselyprosessin avulla työntekijät voivat hakea tarvitsemansa tiedot helposti osana Warehouse Management -mobiilisovelluksen upotettuja työnkulkuja ja käyttää suodatusvaihtoehtoja nähdäkseen vain asiaankuuluvat tiedot. Näin manuaalinen valikoiminen on nopeampaa ja tarkempaa.

Oletetaan esimerkiksi, että ostotilauksen numeron täytyy vastata saapuvaa varastoa ostotilaukset vastaanottavassa työnkulussa. Voit määrittää tälle prosessille helposti valikkovaihtoehtoja tarjotaksesi korttiluettelonäkymän, joka näyttää asiaankuuluvien ostotilausten numerot. Näin voit jatkaa vastaanottotyönkulkua käyttämällä nopeaa Valitse osoittamalla -menetelmää. Tämä artikkeli sisältää esimerkkiskenaarioita, mutta toimintoja voidaan käyttää myös missä tahansa Warehouse Management -mobiilisovelluksen työkulussa.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>Tietojen kyselytyönkulun ominaisuuden ottaminen käyttöön ja sen edellytykset

Ennen kuin voit käyttää tässä artikkelissa kuvattuja toimintoja, sinun täytyy ottaa vaaditut ominaisuudet käyttöön noudattamalla seuraavia ohjeita.

1. Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**. (Lisätietoja **Ominaisuuksien hallinta** -työtilan käyttämisestä on kohdassa [Ominaisuuksien hallinnan yleiskatsaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Jos käytössä on Supply Chain Managementin versio 10.0.28 tai aiempi versio, tämä toiminto otetaan käyttöön seuraavasti:

    - **Moduuli:** *Varastonhallinta*
    - **Toiminnon nimi:** *Varastosovelluksen vaiheohjeet*

    Tämä ominaisuus on edellytys *Warehouse Management -sovelluksen tietokyselyn kulku* -ominaisuudelle. Supply Chain Managementin versiosta 10.0.29 alkaen se on pakollinen, eikä sitä voi poistaa käytöstä. Lisätietoja *Varastosovelluksen vaiheohjeet*-toiminnosta: [Vaiheotsikkojen ja ohjeiden mukauttaminen Warehouse Management -mobiilisovelluksessa](mobile-app-titles-instructions.md).

1. Ota luettelossa näytetty ominaisuus käyttöön seuraavalla tavalla:

    - **Moduuli:** *Varastonhallinta*
    - **Ominaisuuden nimi:** *Warehouse Management -sovelluksen kiertotiet*

    Tämä ominaisuus on edellytys *Warehouse Management -sovelluksen tietokyselyn kulku* -ominaisuudelle. Supply Chain Managementin versiosta 10.0.29 alkaen se on poistettu oletusarvoisesti käytöstä. Lisätietoja *Warehouse Management -sovelluksen kiertotiet* -ominaisuudesta on kohdassa [Kiertoteiden määritys mobiililaitteiden valikkokohteiden vaiheille](warehouse-app-detours.md).

1. Jos *Warehouse Management -sovelluksen kiertotiet* -ominaisuus ei ole vielä käytössä, päivitä kenttien nimet Warehouse Management -mobiilisovelluksessa valitsemalla **Varastonhallinta \> Asetukset \> Mobiililaite \> Varastosovelluksen kenttien nimet** ja valitsemalla **Luo oletusasetus**. Toista tämä vaihe jokaiselle yritykselle, jossa käytät Warehouse Management -mobiilisovellusta. Lisätietoja: [Varastonhallinnan mobiilisovelluksen kenttien konfigurointi](configure-app-field-names-priorities-warehouse.md).
1. Ota luettelossa näytetty ominaisuus käyttöön seuraavalla tavalla:

    - **Moduuli:** *Varastonhallinta*
    - **Ominaisuuden nimi:** *Warehouse Management -sovelluksen tietokyselyn kulku*

    Tämä ominaisuus kuvataan tässä artikkelissa.

## <a name="example-scenarios"></a>Esimerkkiskenaariot

Tässä artikkelissa käytetään esimerkkiskenaarioita havainnollistamaan, miten voit käyttää *Warehouse Management -sovelluksen tietokyselyn kulku* -ominaisuutta ostotilausten vastaanottotyönkulun parantamiseen. Skenaarioissa käytetään vakiomuotoisia esimerkkitietoja, joihin sisältyy työnkulku nimeltään *Ostotilauksen vastaanotto*. Aluksi tämä työnkulku pyytää työntekijöitä tunnistamaan vastaanottamansa ostotilauksen numeron. Voit parantaa työnkulun ensimmäistä sivua lisäämällä seuraavat kyselyvaihtoehdot [kiertoteinä](warehouse-app-detours.md), jotta työntekijät voivat löytää ostotilauksen helpommin:

- **Hae ostotilauksia toimittajan mukaan** – Avaa sivu, joka pyytää työntekijöitä syöttämään toimittajan nimen tai osan siitä. Yleismerkit sallitaan. Jos työntekijä esimerkiksi odottaa tänään lähetystä toimittajalta, jonka nimi sisältää sanan *Tailspin*, hän voi kirjoittaa **Tail\*** nähdäkseen tämän tekstin sisältävät avoimet ostotilaukset kortteina. Jokaisessa kortissa on useita kenttiä, jotka tarjoavat tietoja kustakin ostotilauksesta. Toimittajan nimen lisäksi voit suunnitella kortit siten, että niissä näytetään toimittajan tilinumero, toimituspäivä ja asiakirjan tila.
- **Hae ostostilaukset tältä päivältä** – Avaa sivu, joka ei pyydä käyttäjiä syöttämään tietoja, vaan näyttää esimääritettyjä suodattimia (kuten tämänhetkinen päivämäärä). Sivulla näytetään suodatinta vastaavien korttien joukko. Työntekijät jatkavat valitsemalla sen ostotilauksen kortin, jolle he haluavat rekisteröidä varastonimikkeitä.
- **Hae ostostilauksia nimikkeen mukaan** – Avaa sivu, joka pyytää työntekijöitä skannaamaan saapuneen varaston minkä tahansa nimikkeen viivakoodin. Tämän jälkeen työnkulku näyttää kaikki avoimet ostotilaukset, jotka sisältävät skannattua nimiketunnusta vastaavat rivit. Voit kattaa tilanteet, joissa viivakoodia ei voi lukea, lisäämällä tälle sivulle kiertotiehaun, jolla työntekijät voivat hakea nimiketunnuksia tietystä ostotilauksesta.

Työntekijä tunnistaa kussakin tapauksessa ostotilauksen valitsemalla kortin, jolloin hänet palautetaan ensimmäiselle sivulle, joka näyttää valitun ostotilauksen numeron. Tämän jälkeen työntekijä voi jatkaa saapuvan varastonimikkeen rekisteröintityönkulkua.

## <a name="enable-sample-data"></a>Mallitietojen ottaminen käyttöön

Jos haluat käydä tämän skenaarion läpi käyttämällä tässä artikkelissa kuvattuja arvoja, sinun täytyy käyttää järjestelmää, johon on asennettu vakiomuotoiset [demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Sinun on myös valittava *USMF*-yritys ennen aloittamista.

## <a name="configure-the-mobile-device-menu-items"></a>Mobiililaitteen valikkovaihtoehtojen määrittäminen

Kun haluat luoda työnkulun ensimmäiselle sivulle lisättäviä uusia kyselyvaihtoehtoja, sinun täytyy määrittää ne mobiililaitteen valikkovaihtoehdoiksi. Myöhemmin sallit *Ostotilauksen vastaanotto* -työnkulun käyttää kyselyvaihtoehtoja kiertoteinä.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>Hae ostotilauksia toimittajan mukaan -valikkovaihtoehdon luominen

Luo **Hae ostotilauksia toimittajan mukaan** -valikkovaihtoehto noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Lisää mobiililaitteen valikkovaihtoehto valitsemalla toimintoruudusta **Uusi**.
1. Määritä uudelle valikkovaihtoehdolle seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Hae ostotilauksia toimittajan mukaan*
    - **Otsikko:** *Hae ostotilauksia toimittajan mukaan*
    - **Tila:** *Epäsuora*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Toimintokoodi:** *Tietokysely*
    - **Käytä prosessiopasta:** *Kyllä* (tämä arvo valitaan automaattisesti).
    - **Taulun nimi:** *PurchTable* (haluat etsiä ostotilausten numeroita tästä taulusta).

1. Valitse toimintoruudusta **Muokkaa kyselyä** määrittääksesi kyselyn, joka perustuu valittuun perustauluun (tässä tapauksessa ostotilausten tauluun).
1. Lisää kyselyeditorin **Alue**-välilehden ruudukkoon seuraavat rivit.

    | Taulukko | Johdettu taulu | Kenttä | Kriteeri |
    |---|---|---|---|
    | Ostotilaukset | Ostotilaukset | Ostotilauksen tila | Avoin tilaus |
    | Ostotilaukset | Ostotilaukset | Toimituspäivä | (dayRange(-10,10)) |
    | Ostotilaukset | Ostotilaukset | Toimittajan nimi | |

1. Valitse **OK**.

    Tässä esimerkissä uusi valikkovaihtoehto on määritetty hakemaan avoimet ostotilaukset, joiden odotetaan saapuvan milloin tahansa edellisen 10 päivän ja tulevan 10 päivän välillä.

    Kyselyssä *Toimittajan nimi* -rivin **Ehdot**-sarake on jätetty tyhjäksi. Tämä tarkoittaa, että työntekijät voivat määrittää tämän arvon käyttäessään Warehouse Management -mobiilisovellusta.

    Jos haluat määrittää luettelon lajittelujärjestyksen, voit määrittää lajitteluasetukset **Lajittelu**-välilehdestä.

1. Kyselyn määrittämisen lisäksi sinun täytyy valita kyselyluettelosivun korteissa näytettävät kentät. Valitse siis toimintoruudusta **Kenttäluettelo**.
1. Määritä **Kenttäluettelo**-sivulla seuraavat arvot:

    - **Näyttökenttä 1:** *PurchId* (tämä kenttä näytetään kunkin kortin otsikkona).
    - **Näyttökenttä 2:** *PurchStatus*
    - **Näyttökenttä 3:** *PurchName*
    - **Näyttökenttä 4:** *OrderAccount*
    - **Näyttökenttä 5:** *DeliveryDate*
    - **Näyttökenttä 6:** *displayDocumentStatus()* (tämä arvo on näyttömetodi, niin kuin lopussa oleva "()" osoittaa).

1. Valitse toimintoruudussa **Tallenna**. Sulje sitten sivu.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>Hae ostostilaukset tältä päivältä -valikkovaihtoehdon luominen

Luo **Hae ostostilaukset tältä päivältä** -valikkovaihtoehto noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Lisää mobiililaitteen valikkovaihtoehto valitsemalla toimintoruudusta **Uusi**.
1. Määritä uudelle vaihtoehdolle seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Hae ostostilaukset tältä päivältä*
    - **Otsikko:** *Hae ostostilaukset tältä päivältä*
    - **Tila:** *Epäsuora*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Toimintokoodi:** *Tietokysely*
    - **Käytä prosessiopasta:** *Kyllä* (tämä arvo valitaan automaattisesti).
    - **Taulun nimi:** *PurchTable* (haluat etsiä ostotilausten numeroita tästä taulusta).

1. Valitse toimintoruudusta **Muokkaa kyselyä** määrittääksesi kyselyn, joka perustuu valittuun perustauluun (tässä tapauksessa ostotilausten tauluun).
1. Lisää kyselyeditorin **Alue**-välilehden ruudukkoon seuraavat rivit.

    | Taulukko | Johdettu taulu | Kenttä | Kriteeri |
    |---|---|---|---|
    | Ostotilaus | Ostotilaus | Ostotilauksen tila | Avoin tilaus |
    | Ostotilaus | Ostotilaus | Toimituspäivä | (Day(0)) |

1. Valitse **OK**.

    Tässä esimerkissä uusi valikkovaihtoehto on määritetty hakemaan kaikki avoimet ostotilaukset, joiden odotetaan saapuvan tänään.

    Jos haluat määrittää luettelon lajittelujärjestyksen, voit määrittää lajitteluasetukset **Lajittelu**-välilehdestä.

1. Kyselyn määrittämisen lisäksi sinun täytyy valita kyselyluettelosivun korteissa näytettävät kentät. Valitse siis toimintoruudusta **Kenttäluettelo**.
1. Määritä **Kenttäluettelo**-sivulla seuraavat arvot:

    - **Näyttökenttä 1:** *PurchName* (tämä kenttä näytetään kunkin kortin otsikkona).
    - **Näyttökenttä 2:** *PurchId*
    - **Näyttökenttä 3:** *PurchStatus*
    - **Näyttökenttä 4:** *DlvMode*
    - **Näyttökenttä 5:** *DlvTerm*
    - **Näyttökenttä 6:** *OrderAccount*
    - **Näyttökenttä 7:** *VendorName()* (tämä arvo on näyttömetodi, niin kuin lopussa oleva "()" osoittaa).

1. Valitse toimintoruudussa **Tallenna**. Sulje sitten sivu.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>Hae ostotilauksia nimikkeen mukaan -valikkovaihtoehdon luominen

Luo **Hae ostotilauksia nimikkeen mukaan** -valikkovaihtoehto noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Lisää mobiililaitteen valikkovaihtoehto valitsemalla toimintoruudusta **Uusi**.
1. Määritä uudelle vaihtoehdolle seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Hae ostotilauksia nimikkeen mukaan*
    - **Otsikko:** *Hae ostotilauksia nimikkeen mukaan*
    - **Tila:** *Epäsuora*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Toimintokoodi:** *Tietokysely*
    - **Käytä prosessiopasta:** *Kyllä* (tämä arvo valitaan automaattisesti).
    - **Taulun nimi:** *PurchLine* (haluat etsiä ostotilausten numeroita nimiketunnuksen perusteella rivitietojen kautta).

1. Valitse toimintoruudusta **Muokkaa kyselyä** määrittääksesi kyselyn, joka perustuu valittuun perustauluun (tässä tapauksessa ostotilausrivien taulu, mutta voit käyttää mitä tahansa otsikkoon liittyvää arvoa yhdistämällä sen *PurchTable*-tauluun).
1. Lisää kyselyeditorin **Alue**-välilehden ruudukkoon seuraavat rivit.

    | Taulukko | Johdettu taulu | Kenttä | Kriteeri |
    |---|---|---|---|
    | Ostotilausrivit | Ostotilausrivit | Rivin tila | Avoin tilaus |
    | Ostotilausrivit | Ostotilausrivit | Toimituspäivä | (dayRange(-10,10)) |
    | Ostotilausrivit | Ostotilausrivit | Nimiketunnus | |

1. Valitse **OK**.

    Tässä esimerkissä uusi valikkovaihtoehto on määritetty hakemaan avoimet ostotilausrivit, joiden odotetaan saapuvan milloin tahansa edellisen 10 päivän ja tulevan 10 päivän välillä.

    Kyselyssä *Nimiketunnus*-rivin **Ehdot**-sarake on jätetty tyhjäksi. Tämä tarkoittaa, että työntekijät voivat määrittää tämän arvon käyttäessään Warehouse Management -mobiilisovellusta.

    Jos haluat määrittää luettelon lajittelujärjestyksen, voit määrittää lajitteluasetukset **Lajittelu**-välilehdestä.

1. Kyselyn määrittämisen lisäksi sinun täytyy valita kyselyluettelosivun korteissa näytettävät kentät. Valitse siis toimintoruudusta **Kenttäluettelo**.
1. Määritä **Kenttäluettelo**-sivulla seuraavat arvot:

    - **Näyttökenttä 1:** *PurchId* (tämän kentän arvoa käytetään kunkin kortin otsikkona).
    - **Näyttökenttä 2:** *VendAccount*
    - **Näyttökenttä 3:** *PurchQty*
    - **Näyttökenttä 4:** *PurchUnit*
    - **Näyttökenttä 5:** *PurchStatus*

1. Valitse toimintoruudussa **Tallenna**. Sulje sitten sivu.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>Uusien mobiililaitteen valikkovaihtoehtojen lisääminen valikkoon

Nyt nämä kolme uutta mobiililaitteen valikkovaihtoa ovat valmiina lisättäväksi mobiililaitteen valikkoon. Tämä tehtävä täytyy suorittaa ennen kuin valikkovaihtoehtoja voidaan käyttää osana kiertotieprosessia. Tässä esimerkissä luot uuden alivalikon ja lisäät siihen uusia valikkovaihtoehtoja.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä uuden tietueen otsikossa seuraavat arvot:

    - **Nimi:** *Kysele*
    - **Kuvaus:** *Kysele*

1. Etsi ja valitse **Käytettävissä olevat valikot ja valikkovaihtoehdot** -luettelosta ensimmäinen juuri luomistasi mobiililaitteen valikkovaihtoehdoista. Siirrä sitten valittu vaihtoehto **Valikon rakenne** -luetteloon oikealla nuolipainikkeella.
1. Toista edellinen vaihe kahdelle muulle uudelle valikkovaihtoehdolle.
1. Valitse vasemmanpuoleisesta luetteloruudusta **Päävalikko**.
1. Siirry **Käytettävissä olevat valikot ja valikkovaihtoehdot** -luettelossa **Valikot**-osioon ja valitse uusi **Kysele**-valikko. Siirrä sitten valittu vaihtoehto **Valikon rakenne** -luetteloon oikealla nuolipainikkeella.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Kiertoteiden määrittäminen mobiililaitteiden vaiheille

Jotta voisit viimeistellä määritykset, sinun täytyy nyt käyttää **Mobiililaitteen vaiheet** -sivulla olevaa kiertotiekokoonpanoa lisätäksesi kolme uutta mobiililaitteen valikkovaihtoehtoa *Ostotilauksen vastaanotto* -työnkulun nykyiseen ostostilausten tunnistusvaiheeseen.

1. Valitse **Varastonhallinta \> Asetukset > Mobiililaite \> Mobiililaitteen vaiheet**.
1. Kirjoita **Suodatin**-kenttään *PONum*. Valitse sitten avattavasta luettelosta *Vaihetunnus: "PONum"*.
1. Kun löytynyt tietue on valittuna ruudukossa, valitse toimintoruudusta **Lisää vaihemääritys**. Määritä avautuvassa valintaikkunassa **Valikkovaihtoehto**-kentän arvoksi *Ostotilauksen vastaanotto*. Sulje sitten valintaikkuna valitsemalla **OK**.
1. Valitse uuden vaihemäärityksen (**Ostotilauksen vastaanotto : PONum**) tietosivun **Käytettävissä olevat kiertotiet (valikon vaihtoehdot)** -pikavälilehden työkaluriviltä **Lisää**.
1. Etsi ja valitse **Lisää kiertotie** -valintaikkunasta aiemmin luomasi **Hae ostotilauksia toimittajan mukaan** -valikkovaihtoehto.
1. Sulje valintaikkuna valitsemalla **OK** ja lisää valittu valikkovaihtoehto kiertoteiden luetteloon.
1. Valitse uusi kiertotie ja valitse sitten työkaluriviltä **Lähetettävien kenttien valitseminen**.
1. Älä lisää **Lähetettävien kenttien valitseminen** -valintaikkunan **Lähetä ostotilauksesta** -osioon mitään tietoja, koska et halua välittää mitään arvoja kiertoteiden valikkovaihtoehtoon. Määritä kuitenkin **Tuominen takaisin kohteesta Hae ostotilauksia toimittajan mukaan** -osiossa seuraavat arvot tyhjälle riville, joka on jo lisätty sinne:

    - **Kopioi kohteesta Hae ostotilauksia toimittajan mukaan** *Ostotilaus*
    - **Liittäminen kohteeseen Ostotilauksen vastaanotto:** *Ostotilaus*

1. Sulje valintaikkuna valitsemalla **OK**.
1. Toista vaiheet 4–9 kahdelle muulle uudelle valikkovaihtoehdolle (**Hae ostostilaukset tältä päivältä** ja **Hae ostotilauksia nimikkeen mukaan**). Kuten **Hae ostotilauksia toimittajan mukaan** -valikkovaihtoehdossa, et halua lähettää mitään tietoja näihin kiertoteihin, mutta haluat palauttaa ostotilauksen numeron.
1. Sulje sivu.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Kokeile ostotilausten vastaanottotyönkulkua, jolla on tietokysely osana kiertotietä

Testaa mobiilisovelluksesi uusia asetuksia noudattamalla seuraavia ohjeita.

1. Luo useita ostotilauksia, joissa on rivejä varastolle 51.
1. Siirry mobiililaitteeseen tai emulaattorille, joka käyttää varastonhallinnnan mobiilisovellusta, ja kirjaudu varastoon 51 käyttämällä lukua *51* käyttäjätunnuksena ja lukua *1* salasanana.
1. Valitse mobiilisovelluksen valikosta **Saapuva** ja sitten **Ostotilauksen vastaanotto**.

    Sinun tulisi nähdä seuraava sivu, joka sisältää kolme uutta valikkovaihtoehtoa.

    ![Ostotilauksen vastaanotto käyttämällä ostotilauksen numeroa.](media/wma-purchase-receive-po-num-with-detours.png "Ostotilauksen vastaanotto käyttämällä ostotilauksen numeroa")

1. Kokeilemalla eri ominaisuuksia huomaat, että voit lähettää ostotilauksen numeron takaisin valitsemalla jonkin luettelon korteista.

    ![Ostotilauksen vastaanotto hakemalla ostostilaus toimittajan perusteella, esimerkki 1.](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Ostotilauksen vastaanotto hakemalla ostostilaus toimittajan perusteella, esimerkki 1")

    ![Ostotilauksen vastaanotto hakemalla ostostilaus toimittajan perusteella, esimerkki 2.](media/wma-purchase-receive-lookup-po-vendor-detours.png "Ostotilauksen vastaanotto hakemalla ostostilaus toimittajan perusteella, esimerkki 2")

> [!TIP]
> Sen sijaan, että suorittaisit vastaanottotyönkulun tekemällä haun **Ostotilauksen vastaanotto** -valikkovaihtoehdosta, voit aloittaa kyselytyönkulusta (**Päävalikko \> Kysele \> Hae ostotilauksia toimittajan mukaan**) ja kutsua kiertotietä käynnistämään haluamasi työnkulku valitsemalla kortin luettelosta. Jos haluat käyttää tätä lähestymistapaa, voit määrittää **Mobiililaitteen vaiheet** -sivulla kiertotien vaiheelle, jonka **Vaihetunnus**-arvo on *GenericDataInquiryList*. Jos [*Monitasoiset kiertotiet Warehouse Management ‑mobiilisovelluksessa*](warehouse-app-detours.md) -ominaisuus on otettu käyttöön järjestelmässä, voit myös lisätä kiertotien tarvittaessa (tämä ominaisuus lisää tuen enintään kahdelle kiertotien tasolle, ja sitä voi muokata lisätasojen tukemiseksi).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
