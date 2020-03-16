---
title: Power Appsin upottaminen
description: Tässä ohjeaiheessa käsitellään Power Appsin upottamista asiakasohjelmaan laajentamaan tuotteen toimintoja.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 90422a34499dab7302ad7722cf84d40e1815991c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042939"
---
# <a name="embed-microsoft-power-apps"></a>Microsoft Power Appsin upottaminen

[!include [banner](../includes/banner.md)]

Finance and Operations tukee Microsoft Power Apps -integrointia. Se on palvelu, jonka avulla kehittäjät ja muut kuin tekniset käyttäjät voivat luoda mukautettuja liiketoimintasovelluksia mobiililaitteille, tabletteihin ja verkkoon koodia kirjoittamatta. Sinun, organisaatiosi tai laajemman ekosysteemin kehittämä Power Apps voidaan tämän jälkeen upottaa Finance and Operations -sovelluksiin laajentamaan tuotteen toimintoja. Voit esimerkiksi luoda Power Apps -sovelluksen, joka täydentää Finance and Operations -sovellusta toisesta järjestelmästä haetuilla tiedoilla.

Lisätietoja Power Appsin upottamisesta on lyhyessä [Power Appsin upottaminen](https://www.youtube.com/watch?v=x3qyA1bH-NY) -videossa.

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>Upotetun Power Apps -sovelluksen lisääminen sivulle

### <a name="overview"></a>Yleiskatsaus

Ennen kuin Power Apps -sovellus voidaan upottaa asiakasohjelmaan, käyttäjän on ensin etsittävä tai luotava sovellus, jossa on toivotut visuaaliset elementit ja/tai toiminnot. Sovellusten kehitysprosessia ei käsitellä tässä yksityiskohtaisesti. Jos olet uusi Power Apps-käyttäjä, ohjeaiheesta [Power Appsin esittely](https://docs.microsoft.com/powerapps/getting-started) on hyvä aloittaa.

Kun olet valmis upottamaan tietyn sovelluksen, sovellusta voi käyttää sivulla kahdella tavalla. Voit valita skenaarioosi paremmin sopivan tavan. Ensimmäinen tapa on tavalliseen toimintoruutuun lisätyn Power Apps-painikkeen käyttäminen. Tällä tavoin lisätty sovellus näkyy valikon vaihtoehtoina Power Apps -valikkopainikkeessa. Valittaessa jokainen näistä valikkovaihtoehdoista avaa upotetun sovelluksen sisältävän sivuruudun. Vaihtoehtoisesti voit upottaa sovelluksen suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana.

Voit valita upotettua sovellusta määritettäessä yhden kentän, jonka haluat lähettää kontekstina sovellukseen. Tällä tavoin sovellus voi reagoida tarkasteltavien tietojen perusteella.

### <a name="details"></a>Yksityiskohdat

Seuraavissa ohjeissa näytetään, miten Power Apps -sovellus upotetaan verkkoasiakkaaseen.

1. Siirry sivulle, johon haluat upottaa sovelluksen. Tämä on sama sivu, joka sisältää mahdolliset sovellukseen syötteenä välitettävät tiedot.
2. Avaa **Lisää Power Apps -sovellus** -ruutu:

    - Valitse **Asetukset** ja valitse sitten **Mukauta tämä sivu**. Valitse **Lisää**-valikossa **Power Apps**. Valitse lopuksi alue, johon haluat lisätä sovelluksen. Jos haluat upottaa sovelluksen Power Apps -valikkopainikkeeseen, valitse toimintoruutu. Jos haluat upottaa sovelluksen suoraan sivulle, valitse soveltuva välilehti, pikavälilehti, lehti tai osa (jos kyseessä on työtila).
    - Jos sovellusta käytetään Power Apps -valikkopainikkeella, voit vaihtoehtoisesti valita vakiotoimintoruudun **Power Apps** -valikkopainikkeen ja valita sitten **Lisää sovellus**.

3. Määritä upotettu sovellus seuraavasti:

    - **Nimi**-kentässä on sen painikkeen tai välilehden teksti, joka sisältää upotetun sovelluksen. Sovelluksen nimi on usein toistettava tässä kentässä.
    - **Sovelluksen tunnus** on upotettavan sovelluksen GUID-tunnus. Voit noutaa tämän arvon etsimällä sovelluksen sivustossa [web.powerapps.com](https://web.powerapps.com) ja siirtymällä sitten **Sovelluksen tunnus** -kenttään **Tiedot**-kohdassa.
    - Voit vaihtoehtoisesti valita **Lisää sovellukselle konteksti** -kohdassa kentän, joka sisältää sovellukselle syötteenä välitettävät tiedot. Lisätietoja tavoista, joilla sovellus voi käyttää Finance and Operations -sovelluksista lähetettyjä tietoja, on jäljempänä tässä ohjeaiheessa kohdassa [Finance and Operations -sovelluksista lähetettyjä tietoja hyödyntävien sovellusten kehittäminen](#building-an-app-that-leverages-data-sent-from-finance-and-operations-apps).
    - Valitse upotettavan sovelluksen tyyppiä vastaava **sovelluksen koko**. Jos sovellus luodaan mobiililaitteille, valitse **Ohut**. Jos se luodaan tableteille, valitse **Leveä**. Tämä varmistaa, että upotetulle sovellukselle on varattu riittävästi tilaa.
    - **Yritykset**-pikavälilehdessä voi valita, mitkä yritykset voivat käyttää sovellusta. Oletusarvona on sovelluksen antaminen käyttöön kaikille yrityksille. Tämä vaihtoehto on käytettävissä vain, kun [Tallennetut näkymät](saved-views.md) -toiminto on poistettu käytöstä. 

4. Kun vahvistus on tehty ja määrityksessä on kaikki oikein, lisää Power App sivulle valitsemalla **Lisää**. Sinua pyydetään päivittämään selain, jotta upotettu sovellus tulee näkyviin.

## <a name="sharing-an-embedded-app"></a>Upotetun sovelluksen jakaminen

Kun sovellus on upotettu sivulle ja kun on vahvistettu, että se toimii oikein kaikkien sivulle välitettyjen tietokontekstien kanssa, upotettu sovellus on mahdollista jakaa järjestelmän muiden käyttäjien kanssa. Sen voi tehdä kahdella tavalla käyttämällä tuotteen mukauttamisominaisuuksia:

- Suosituksena on pyytää järjestelmänvalvojaa toimittamaan mukautus kaikille käyttäjille tai osalle käyttäjiä.
- Vaihtoehtoisesti voit viedä sivun mukautukset, lähettää ne yhdelle tai usealle käyttäjälle ja näitä käyttäjiä tuomaan kyseiset muutokset. Mukauttamisen työkalurivi sisältää toimintoja, joiden avulla voit viedä ja tuoda mukautuksia.

Lisätietoja tuotteen mukauttamistoiminnoista ja niiden käytöstä on kohdassa [Käyttökokemuksen mukauttaminen](personalize-user-experience.md).

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Finance and Operations -sovelluksien lähettämiä tietoja hyödyntävän sovelluksen kehittäminen

Tärkeä osa Finance and Operations -sovellukseen upotettavan Power Apps -sovelluksen kehittämistä on käyttää kyseisen sovelluksen syötetietoja. Power Apps -kehityskokemuksessa Finance and Operations -sovelluksesta välitettyjä tietoja voidaan käyttää käyttämällä muuttujaa Param("EntityId").

Esimerkiksi sovelluksen OnStart-toiminnolle voi määrittää syöttötiedot Finance and Operations -sovelluksista muuttujalle seuraavalla tavalla:

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>Sovelluksen tarkasteleminen

Voit tarkastella Finance and Operations -sovelluksien sivulle upotettua sovellusta siirtymällä sivulle, jolla on upotettu sovellus. Muista, että sovelluksia voi käyttää vakiotoimintoruudun Power Apps -painikkeen avulla. Se voi näkymä myös suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana. Kun käyttäjä yrittää ladata sivulla sovelluksen, käyttäjää pyydetään kirjautumaan iin. Tällä tavoin varmistetaan, että käyttäjällä on soveltuvat sovelluksen käyttöoikeudet.

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

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>Kehittäjä päättää, minne sovellus voidaan upottaa

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
