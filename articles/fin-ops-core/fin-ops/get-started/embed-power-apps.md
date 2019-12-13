---
title: Power Appsin upottaminen
description: Tässä ohjeaiheessa käsitellään Power Appsin upottamista asiakasohjelmaan laajentamaan tuotteen toimintoja.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
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
ms.openlocfilehash: 755a30f89725ca0a7e1c14252984c617d6ba280e
ms.sourcegitcommit: 4162d9ef4239c9d4e5297b8aaa903dd54f9cafc3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/21/2019
ms.locfileid: "2824490"
---
# <a name="embed-microsoft-power-apps"></a>Microsoft Power Appsin upottaminen

[!include [banner](../includes/banner.md)]

Platform update 14 tukee Microsoft Power Apps -integrointia. Se on palvelu, jonka avulla kehittäjät ja muut kuin tekniset käyttäjät voivat luoda mukautettuja liiketoimintasovelluksia mobiililaitteille, tabletteihin ja verkkoon koodia kirjoittamatta. Sinun, organisaatiosi tai laajemman ekosysteemin kehittämä Power Apps voidaan tämän jälkeen upottaa Finance and Operations -sovelluksiin laajentamaan tuotteen toimintoja. Voit esimerkiksi muodostaa Power Appin täydentämään Finance and Operations -sovelluksia toisesta järjestelmästä haetuilla tiedoilla.

Lisätietoja Power Appsin upottamisesta on lyhyessä [Power Appsin upottaminen](https://www.youtube.com/watch?v=x3qyA1bH-NY) -videossa.

## <a name="adding-an-embedded-power-app-to-a-page"></a>Upotetun Power Appin lisääminen sivulle

### <a name="overview"></a>Yleiskuvaus

Ennen kuin Power App voidaan upottaa asiakasohjelmaan, käyttäjän on ensin etsittävä tai luotava Power App, jossa on toivotut visuaaliset elementit ja/tai toiminnot. Power Appin muodostamisprosessia ei käsitellä tässä yksityiskohtaisesti. Jos olet uusi Power Apps-käyttäjä, ohjeaiheesta [Power Appsin esittely](https://docs.microsoft.com/powerapps/getting-started) on hyvä aloittaa.

Kun olet valmis upottamaan tietyn Power Appin, Power Appia voi käyttää sivulla kahdella tavalla. Voit valita skenaarioosi paremmin sopivan tavan. Ensimmäinen tapa on tavalliseen toimintoruutuun lisätyn Power Apps-painikkeen käyttäminen. Tällä tavoin lisätty Power Apps näkyy valikon vaihtoehtoina Power Apps-valikkopainikkeessa. Valittaessa jokainen näistä valikkovaihtoehdoista avaa upotetun Power Appin sisältävän sivuruudun. Vaihtoehtoisesti voit näyttää Power Appin suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana.

Voit valita upotettua Power Appia määritettäessä yhden kentän, jonka haluat lähettää syötteenä Power Appiin. Tällä tavoin Power App voi reagoida tarkasteltavien tietojen perusteella.

### <a name="details"></a>Yksityiskohdat

Seuraavissa ohjeissa näytetään, miten Power App upotetaan verkkoasiakkaaseen.

1. Siirry sivulle, johon haluat upottaa Power Appin. Tämä on sama sivu, joka sisältää mahdolliset Power Appiin syötteenä välitettävät tiedot.
2. Avaa **Lisää Power App** -ruutu:

    - Valitse **Asetukset** ja valitse sitten **Mukauta tämä lomake**. Valitse **Lisää**-valikossa **Power App**. Valitse lopuksi alue, johon haluat lisätä Power Appin. Jos haluat upottaa Power Appin Power Apps -valikkopainikkeeseen, valitse toimintoruutu. Jos haluat upottaa Power Appin suoraan sivulle, valitse soveltuva välilehti, pikavälilehti, lehti tai osa (jos kyseessä on työtila).
    - Jos Power Appia käytetään Power Apps -valikkopainikkeella, voit vaihtoehtoisesti valita vakiotoimintoruudun **Power Apps** -valikkopainikkeen ja valita sitten **Lisää Power App**.

3. Määritä upotettu Power App seuraavasti:

    - **Nimi**-kentässä on sen painikkeen tai välilehden teksti, joka sisältää upotetun Power Appin. Power Appin nimi on usein toistettava tässä kentässä.
    - **Sovelluksen tunnus** on upotettavan Power Appin GUID-tunnus. Voit noutaa tämän arvon etsimällä Power Appin sivustossa [web.powerapps.com](https://web.powerapps.com) ja siirtymällä sitten **Sovelluksen tunnus** -kenttään **Tiedot**-kohdassa.
    - Voit vaihtoehtoisesti valita **Anna Power App -kohteen tiedot** -kohdassa kentän, joka sisältää Power Appille syötteenä välitettävät tiedot. Lisätietoja tavoista, joilla Power App voi käyttää Finance and Operations -sovelluksista lähetettyjä tietoja, on jäljempänä tässä ohjeaiheessa kohdassa [Finance and Operations -sovellusten tietoja hyödyntävän Power Appin muodostaminen](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps).
    - Valitse upotettavan Power Appin tyyppiä vastaava **sovelluksen koko**. Jos Power Apps luodaan mobiililaitteille, valitse **Ohut**. Jos Power Apps luodaan tableteille, valitse **Leveä**. Tämä varmistaa, että upotetulle Power Appille on varattu riittävästi tilaa.
    - **Yritykset**-pikavälilehdessä voi valita, mitkä yritykset voivat käyttää Power Appia. Power App näytetään oletusarvoisesti kaikille yrityksille.

4. Kun vahvistus on tehty ja määrityksessä on kaikki oikein, lisää Power App sivulle valitsemalla **Lisää**. Sinua pyydetään päivittämään selain, jotta upotettu Power App tulee näkyviin.

## <a name="sharing-an-embedded-power-app"></a>Upotetun Power Appin jakaminen

Kun Power App on upotettu sivulle ja kun on vahvistettu, että se toimii oikein kaikkien sivulle välitettyjen tietokontekstien kanssa, upotettu Power App on mahdollista jakaa järjestelmän muiden käyttäjien kanssa. Sen voi tehdä kahdella tavalla käyttämällä tuotteen mukauttamisominaisuuksia:

- Suosituksena on pyytää järjestelmänvalvojaa toimittamaan mukautus kaikille käyttäjille tai osalle käyttäjiä.
- Vaihtoehtoisesti voit viedä sivun mukautukset, lähettää ne yhdelle tai usealle käyttäjälle ja näitä käyttäjiä tuomaan kyseiset muutokset. Voit viedä ja tuoda mukautuksia mukauttamisen työkalurivin Hallinta-asetuksella.

Lisätietoja tuotteen mukauttamistoiminnoista ja niiden käytöstä on kohdassa [Käyttökokemuksen mukauttaminen](personalize-user-experience.md).

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Finance and Operations -sovellusten lähettämiä tietoja hyödyntävän Power Appin luominen

Tärkeä osa Finance and Operations -sovelluksiin upotettavan Power Appin muodostamista on Finance and Operations -sovellusten syöttötietojen käyttäminen. Power Appin sisällä syöttötietoja käytetään Param("EntityId")-muuttujan avulla.

Esimerkiksi Power Appin OnStart-toiminnolle voi määrittää syöttötiedot Finance and Operations -sovelluksista muuttujalle seuraavalla tavalla:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>Upotetun Power Appin näyttäminen

Voit tarkastella Finance and Operations -sovelluksien sivulle upotettua Power Appia siirtymällä kyseiselle sivulle. Muista, että Power Appsia voi käyttää vakiotoimintoruudun Power Apps-painikkeen avulla. Se voi näkymä myös suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana. Kun käyttäjä yrittää ladata sivulla Power Appin, käyttäjää pyydetään kirjautumaan Power Appsiin. Tällä tavoin varmistetaan, että käyttäjällä on soveltuvat Power Appin käyttöoikeudet.

## <a name="editing-an-embedded-power-app"></a>Upotetun Power Appin muokkaaminen

Sivulle upotettu Power App saattaa edellyttää muutoksia kyseisen Power Appin määrityksiin. Voit esimerkiksi muokata upotettuun Power Appiin liitettyä otsikkoa. Jos on luotu uusi Power App -versio, sovelluksen tunnus on ehkä päivitettävä niin, että se osoittaa uusimpaan Power App -versioon.

Muokkaa upotetun Power Appin määritystä seuraavasti:

1. Siirry **Muokkaa Power App -sovellusta** -ruutuun.

    - Jos upotettua Power Appia käytetään suoraan Power Apps -valikkopainikkeella, napsauta hiiren kakkospainikkeella Power Apps -valikkopainiketta ja valitse **Mukauta**. Valitse määritettävä Power App avattavasta **Valitse Power App** -valikosta.
    - Jos upotettu Power App näkyy suoraan sivulla, valitse ensin **Asetukset** ja sitten **Mukauta tämä lomake**. Napsauta upotettua Power Appia **Valinta**-työkalulla.

2. Tee Power Apps-määritykseen tarvittavat muutokset ja valitse sitten **Tallenna**.

## <a name="removing-an-embedded-power-app"></a>Upotetun Power Appin poistaminen

Upotetun Power Appin voi tarvittaessa poistaa sivulta käyttämällä jompaakumpaa seuraavaa tapaa:

- Siirry **Muokkaa Power App -sovellusta** -ruutuun tämän ohjeaiheen aiemmin käsitellyn osan [Upotetun Power Appin muokkaaminen](#editing-an-embedded-powerapp) ohjeiden avulla. Vahvista, että ruudussa on sen upotetun Power Appin tiedot, jonka haluat poistaa, ja valitse sitten **Poista**-painike.
- Koska upotettu Power App on tallennettu mukautuksen tietoina, sivun mukautuksen tyhjentäminen poistaa myös kaikki sivulle upotetut Power Apps -sovellukset. Huomaa, että sivun mukautukset tyhjennetään pysyvästi. Tyhjennystä ei voi peruuttaa. Voit poistaa sivun mukautukset valitsemalla ensin **Asetukset** ja sitten **Mukauta tämä lomake**. Valitse **Hallinta**-valikossa **Tyhjennä**-painike. Kaikki tämän sivun edelliset mukautukset poistetaan, kun selain päivitetään. Lisätietoja sivujen optimoinnista mukauttamisen avulla on kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md).

## <a name="appendix"></a>Liite

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>Kehittäjä päättää, minne Power App voidaan upottaa

Käyttäjät voivat upottaa Power Appsin oletusarvoisesti mille tahansa sivulle joko Power Apps-valikkopainikkeeseen tai suoraan sivulle välilehtinä, pikavälilehtinä tai työtilan uutena osana. Kehittäjät voivat kuitenkin tarvittaessa määrittää tämän toiminnon niin, että se sallii Power Appsin upottamisen vain tietyillä sivuilla. Se tehdään seuraavasti:

- **isPowerAppPersonalizationEnabled** – Jos tämä menetelmä palauttaa epätosi-arvon tietylle sivulle, Power Apps-valikkopainike ei ole näkyvissä. Tällöin käyttäjät eivät voi upottaa Power Appsia sivulle edes välilehtenä.
- **isPowerAppTabPersonalizationEnabled** – Jos tämä menetelmä palauttaa epätosi-arvon tietylle sivulle, käyttäjät eivät voi upottaa Power Appsia suoraan sivulle välilehtenä, pikavälilehtenä tai panoraamaosana. Käyttäjät voivat edelleen upottaa Power Appsin Power Apps-valikkopainikkeella, jos sivu sallii upottamisen.

Seuraavassa esimerkissä on uusi luokka ja kaksi menetelmää, jotka tarvitaan määrittämään, minne Power Apps voidaan upottaa.

```
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
