---
title: Power Appsin kaavasovellusten upottaminen
description: Tässä ohjeaiheessa käsitellään Microsoft Power Appsin kaaviosovellusten upottamista asiakasohjelmaan laajentamaan tuotteen toimintoja.
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 18146ce5ab081b3a6376bf412805016b04da6a11
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944676"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Power Appsin kaavasovellusten upottaminen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Microsoft Power Apps on palvelu, joka sallii kehittäjien ja muiden kuin teknisten käyttäjien muokata yrityssovelluksia mobiililaitteille, tableteille ja verkkoon ilman, että heidän tarvitsee kirjoittaa koodia. Finance and Operations -sovellukset tukevat integrointia Power Appsiin. Sinun, organisaatiosi tai laajemman ekosysteemin kehittämät kaaviosovellukset voidaan upottaa Finance and Operations -sovelluksiin laajentamaan tuotteen toimintoja. Voit esimerkiksi luoda Power Apps -kaaviosovelluksen, joka täydentää Finance and Operations -sovellusta toisesta järjestelmästä haetuilla tiedoilla.

Lisätietoja kaaviosovellusten upottamisesta on lyhyessä videossa [Kaaviosovellusten upottaminen](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Upotetun Power Apps -kaaviosovelluksen lisääminen sivulle

### <a name="overview"></a>Yleiskuvaus

Ennen kuin Power Apps -kaaviosovellus voidaan upottaa asiakasohjelmaan, käyttäjän on ensin etsittävä tai luotava sovellus, jossa on toivotut visuaaliset elementit tai toiminnot. Tässä ohjeaiheessa ei ole yksityiskohtaista kuvausta sovellusten luontiprosessista. Jos Power Apps ei ole tuttu, tutustu [Power Apps -dokumentaatioon](/powerapps/).

On kaksi tapaa käyttää tiettyä kaaviosovellusta sivulla, kun olet valmis upottamaan sovelluksen. Voit valita, kumpi tapa sopii paremmin tilanteeseen. Ensimmäinen tapa on tavalliseen toimintoruutuun lisätyn **Power Apps** -painikkeen käyttäminen. Tämän menetelmän avulla lisäämäsi sovellukset näkyvät nimikkeinä **Power Apps** -valikkopainikkeessa. Kun valitset jonkin näistä nimikkeistä, näkyviin tulee upotettavan sovelluksen sisältävä sivuruutu. Vaihtoehtoisesti voit upottaa sovelluksen suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana.

Voit valita upotettua kaaviosovellusta määritettäessä yhden kentän, jonka haluat lähettää kontekstina sovellukseen. Tälölin sovellus voi reagoida tarkasteltavien tietojen perusteella.

> [!NOTE]
> Tätä menetelmää ei tällä hetkellä voi käyttää mallipohjaisten sovellusten upottamiseen.  

### <a name="details"></a>Lisätietoja

Seuraavassa menettelyssä esitetään, miten Power Apps -kaaviosovellus upotetaan verkkoasiakkaaseen.

1. Siirry sivulle, johon haluat upottaa kaaviosovelluksen. Tämä on se sivu, joka sisältää mahdolliset sovellukseen syötteenä välitettävät tiedot.
2. Avaa **Lisää Power Apps -sovellus** -ruutu:

    - Valitse **Asetukset** ja valitse sitten **Mukauta tämä sivu**. Valitse **Lisää**-valikossa **Power Apps**. Valitse lopuksi alue, johon haluat lisätä sovelluksen. Jos haluat upottaa sovelluksen Power Apps -valikkopainikkeeseen, valitse toimintoruutu. Jos haluat upottaa sovelluksen suoraan sivulle, valitse soveltuva välilehti, pikavälilehti, lehti tai osa (jos kyseessä on työtila).
    - Jos sovellusta käytetään Power Apps -valikkopainikkeella, voit vaihtoehtoisesti valita vakiotoimintoruudun **Power Apps** -valikkopainikkeen ja valita sitten **Lisää sovellus**.

3. Määritä upotettu sovellus seuraavasti:

    - **Nimi**-kentässä on sen painikkeen tai välilehden teksti, joka sisältää upotetun sovelluksen. Sovelluksen nimi on usein toistettava tässä kentässä.
    - **Sovellustunnus**-kenttä ilmaisee upotettavan kaaviosovelluksen GUID-tunnuksen. Voit noutaa tämän arvon etsimällä sovelluksen sivustossa [make.powerapps.com](https://make.powerapps.com) ja siirtymällä sitten **Sovelluksen tunnus** -kenttään **Tiedot**-kohdassa.
    - Voit vaihtoehtoisesti valita **Lisää sovellukselle konteksti** -kohdassa kentän, joka sisältää sovellukselle syötteenä välitettävät tiedot. Lisätietoa tavoista, joilla sovellus voi käyttää Finance and Operations -sovelluksista lähetettyjä tietoja on jäljempänä tässä ohjeaiheessa kohdassa [Finance and Operations -sovelluksien lähettämiä tietoja hyödyntävän sovelluksen kehittäminen](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps). 
        - Versiosta 10.0.19 alkaen nykyinen yritys välitetään myös kaaviosovellukselle kontekstina **cmp**-URL-parametrin kautta. Tällä ei ole vaikutusta kohdekaaviosovellukseen, ennen kuin sovellus käyttää näitä tietoja. 
    - Valitse upotettavan sovelluksen tyyppiä vastaava **sovelluksen koko**. Jos sovellus luodaan mobiililaitteille, valitse **Ohut**. Jos se luodaan tableteille, valitse **Leveä**. Tämä varmistaa, että upotetulle sovellukselle on varattu riittävästi tilaa.
    - **Yritykset**-pikavälilehdessä voi valita, mitkä yritykset voivat käyttää sovellusta. Oletusarvona on sovelluksen antaminen käyttöön kaikille yrityksille. Tämä vaihtoehto on käytettävissä vain, kun [Tallennetut näkymät](saved-views.md) -toiminto on poistettu käytöstä. 

4. Kun vahvistus on tehty ja määrityksessä on kaikki oikein, lisää Power App sivulle valitsemalla **Lisää**. Sinua pyydetään päivittämään selain, jotta upotettu sovellus tulee näkyviin.

## <a name="sharing-an-embedded-app"></a>Upotetun sovelluksen jakaminen

Kun kaaviosovellus on upotettu sivulle ja kun on vahvistettu, että se toimii oikein kaikkien sivulle välitettyjen tietokontekstien kanssa, upotettu sovellus on mahdollista jakaa järjestelmän muiden käyttäjien kanssa. Voit jakaa upotetun kaaviosovelluksen seuraavasti.

1. [Jaa kaaviosovellus ](/powerapps/maker/canvas-apps/share-app) asianmukaisten käyttäjien kanssa, jotta he voivat käyttää sovellusta Power Appsissa. 

2. Varmista, että näillä käyttäjillä on tarvittavat mukautukset, jotta upotettu sovellus tulee näkyviin, kun käyttäjät avaavat sivun. Voit käyttää kumpaa tahansa seuraavista menetelmistä:

    - Suositus: Käytä [Tallennetut näkymät](saved-views.md) -toimintoa, kun haluat luoda ja julkaista näkymän, joka sisältää upotetun sovelluksen. Tämä menetelmä varmistaa, että kaikki käyttäjät, joilla on julkaistun näkymän kohteena olevat käyttöoikeusroolit, näkevät sovelluksen Finance and Operations -sovelluksissa. 
    - Jos Tallennetut näkymät-toiminto ei ole käytössä, voit pyytää järjestelmänvalvojaa työntämään kaikille käyttäjille tai käyttäjien alijoukolle mukautuksen, joka sisältää upotetun sovelluksen. Voit myös viedä sivusi mukautukset ja lähettää ne yhdelle tai useammalle käyttäjälle. Kukin näistä käyttäjistä voi tämän jälkeen tuoda mukautukset. Mukauttamisen työkalurivi sisältää toimintoja, joiden avulla voit viedä ja tuoda mukautuksia. 
    
> [!NOTE]
> Jos kaaviosovellus on jaettu ulkoisten käyttäjien kanssa, kyseiset käyttäjät eivät voi käyttää upotettua sovellusta Finance and Operations -sovelluksissa. He voivat kuitenkin käyttää sovellusta suoraan Power Appsissa. Ulkoiset käyttäjät ovat vieraita ja käyttäjiä, jotka eivät kuulu siihen Microsoft 365:n Azure-hakemistoon, jossa Finance and Operations -sovellus on otettu käyttöön.

Lisätietoja tuotteen mukauttamistoiminnoista ja niiden käytöstä on kohdassa [Käyttökokemuksen mukauttaminen](personalize-user-experience.md).

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Finance and Operations -sovelluksista lähetettyjä tietoja käyttävän kaaviosovelluksen luominen

Kun luot kaaviosovelluksen, joka upotetaan Finance and Operations -sovellukseen, tärkeä osa prosessia on käyttää kyseisen Finance and Operations -sovelluksen syöttötietoja. Power Apps -kehityskokemuksessa Finance and Operations -sovelluksesta välitettyjä tietoja voidaan käyttää käyttämällä muuttujaa **Param("EntityId")**. Lisäksi versiosta 10.0.19 alkaen nykyinen yritys välitetään myös kaaviosovellukselle **Param("cmp")**-muuttujan kautta. 

Esimerkiksi sovelluksen OnStart-toiminnolle voi määrittää syöttötiedot Finance and Operations -sovelluksista muuttujalle seuraavalla tavalla:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsInput, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Kaaviosovelluksen tarkasteleminen

Voit tarkastella Finance and Operations -sovelluksien sivulle upotettua kaaviosovellusta siirtymällä sivulle, jolla on upotettu sovellus. Muista, että sovelluksia voi käyttää vakiomuotoisen toimintoruudun **Power Apps** -painikkeen avulla. Vaihtoehtoisesti ne voivat tulla näkyviin suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana. Kun käyttäjät yrittävät ladata sovelluksen sivulla ensimmäistä kertaa, heitä kehotetaan kirjautumaan sisään. Tällä vaiheella varmistetaan, että käyttäjillä on tarvittavat käyttöoikeudet sovelluksen käyttämiseen.

## <a name="editing-an-embedded-app"></a>Upotetun sovelluksen muokkaaminen

Sivulle upotettu sovellus saattaa vaatia muutoksia kyseisen sovelluksen määrityksiin. Voit esimerkiksi muokata upotettuun sovellukseen liitettyä otsikkoa. Jos on luotu uusi sovellus, sovelluksen tunnus on ehkä päivitettävä niin, että se osoittaa uusimpaan versioon.

Muokkaa upotetun sovelluksen konfiguraatiota näiden vaiheiden avulla:

1. Siirry **Muokkaa sovellusta** -ruutuun.

    - Jos upotettua sovellusta käytetään suoraan Power Apps -valikkopainikkeella, napsauta hiiren kakkospainikkeella Power Apps -valikkopainiketta ja valitse **Mukauta**. Valitse määritettävä sovellus avattavasta **Valitse sovellus** -valikosta.
    - Jos upotettu sovellus näkyy suoraan sivulla, valitse ensin **Asetukset** ja sitten **Mukauta tämä sivu**. Napsauta upotettua sovellusta **Valinta**-työkalulla.

2. Tee sovelluksen määritykseen tarvittavat muutokset ja valitse sitten **Tallenna**.

## <a name="removing-an-app"></a>Sovelluksen poistaminen

Upotetun sovelluksen voi tarvittaessa poistaa sivulta käyttämällä jompaakumpaa seuraavaa tapaa:

- Siirry **Muokkaa sovellusta** -ruutuun tämän ohjeaiheen aiemmin käsitellyn osan [Upotetun sovelluksen muokkaaminen](#editing-an-embedded-app) ohjeiden avulla. Vahvista, että ruudussa on sen upotetun sovelluksen tiedot, jonka haluat poistaa, ja valitse sitten **Poista**-painike.
- Koska upotettu sovellus on tallennettu mukautuksen tietoina, sivun mukautuksen tyhjentäminen poistaa myös kaikki sivulle upotetut sovellukset. Huomaa, että sivun mukautukset tyhjennetään pysyvästi. Tyhjennystä ei voi peruuttaa. Voit poistaa sivun mukautukset valitsemalla ensin **Asetukset**, sitten **Mukauta tämä sivu** ja lopuksi **Tyhjennä**-painike. Kaikki tämän sivun edelliset mukautukset poistetaan, kun selain päivitetään. Lisätietoja sivujen optimoinnista mukauttamisen avulla on kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md).

## <a name="appendix"></a>Liite

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Kehittäjä] Kaaviosovelluksen mallinnus lomakkeelle

Vaikka tämä ohjeaihe keskittyy kaaviosovelluksen upottamiseen räätälöinnin kautta, kehittäjillä on myös mahdollisuus lisätä kaaviosovellus lomakkeeseen Visual Studio -kehityskokemusta käyttäen. Voit tehdä tämän lisäämällä lomakkeeseen PowerAppsHostControlin. Ohjausobjektin käytettävissä olevat metatietojen ominaisuudet tarjoavat samat ominaisuudet kuin personointikokemuskin.


### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Kehittäjä] Määrittää, minne sovellus voidaan upottaa

Käyttäjät voivat upottaa sovellukset oletusarvoisesti mille tahansa sivulle joko Power Apps -valikkopainikkeeseen tai suoraan sivulle välilehtinä, pikavälilehtinä tai työtilan uutena osana. Kehittäjät voivat kuitenkin tarvittaessa määrittää tämän toiminnon niin, että se sallii sovellusten upottamisen vain tietyillä sivuilla. Se tehdään seuraavasti:

- **isPowerAppPersonalizationEnabled** – Jos tämä menetelmä palauttaa epätosi-arvon tietylle sivulle, Power Apps -valikkopainike ei ole näkyvissä. Tällöin käyttäjät eivät voi upottaa sovelluksia sivulle edes välilehtenä.
- **isPowerAppTabPersonalizationEnabled** – Jos tämä menetelmä palauttaa epätosi-arvon tietylle sivulle, käyttäjät eivät voi upottaa sovelluksia suoraan sivulle välilehtenä, pikavälilehtenä tai panoraamaosana. Käyttäjät voivat edelleen upottaa sovelluksia Power Apps -valikkopainikkeella, jos sivu sallii upottamisen.

Seuraavassa esimerkissä on uusi luokka ja kaksi menetelmää, jotka tarvitaan sovellusten upottamista varten.

```powerapps
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
