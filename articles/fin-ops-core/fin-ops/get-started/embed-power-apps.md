---
title: PowerApps-sovellusten upottaminen
description: Tässä ohjeaiheessa käsitellään PowerAppsin upottamista asiakasohjelmaan laajentamaan tuotteen toimintoja.
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
ms.openlocfilehash: 37faf2a7a880c384f6f01d06ef5c9f28055d5006
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191175"
---
# <a name="embed-powerapps-apps"></a>PowerApps-sovellusten upottaminen

[!include [banner](../includes/banner.md)]

Platform update 14 tukee Microsoft PowerApps -integrointia. Se on palvelu, jonka avulla kehittäjät ja muut kuin tekniset käyttäjät voivat luoda mukautettuja liiketoimintasovelluksia mobiililaitteille, tabletteihin ja verkkoon koodia kirjoittamatta. Sinun, organisaatiosi tai laajemman ekosysteemin kehittämä PowerApps voidaan tämän jälkeen upottaa Finance and Operations -sovelluksiin laajentamaan tuotteen toimintoja. Voit esimerkiksi muodostaa PowerAppin täydentämään Finance and Operations -sovelluksia toisesta järjestelmästä haetuilla tiedoilla.

Lisätietoja PowerAppsin upottamisesta on lyhyessä [PowerAppsin upottaminen](https://www.youtube.com/watch?v=x3qyA1bH-NY) -videossa.

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Upotetun PowerApp-sovelluksen lisääminen sivulle

### <a name="overview"></a>Yleiskuvaus

Ennen kuin PowerApp voidaan upottaa asiakasohjelmaan, käyttäjän on ensin etsittävä tai luotava PowerApp, jossa on toivotut visuaaliset elementit ja/tai toiminnot. PowerAppin muodostamisprosessia ei käsitellä tässä yksityiskohtaisesti. Jos olet uusi PowerApps-käyttäjä, ohjeaiheesta [PowerAppsin esittely](https://docs.microsoft.com/powerapps/getting-started) on hyvä aloittaa.

Kun olet valmis upottamaan tietyn PowerAppin, PowerAppia voi käyttää sivulla kahdella tavalla. Voit valita skenaarioosi paremmin sopivan tavan. Ensimmäinen tapa on tavalliseen toimintoruutuun lisätyn PowerApps-painikkeen käyttäminen. Tällä tavoin lisätty PowerApps näkyy valikon vaihtoehtoina PowerApps-valikkopainikkeessa. Valittaessa jokainen näistä valikkovaihtoehdoista avaa upotetun PowerAppin sisältävän sivuruudun. Vaihtoehtoisesti voit näyttää PowerApp-sovelluksen suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana.

Voit valita upotettua PowerAppia määritettäessä yhden kentän, jonka haluat lähettää syötteenä PowerAppiin. Tällä tavoin PowerApp voi reagoida tarkasteltavien tietojen perusteella.

### <a name="details"></a>Yksityiskohdat

Seuraavissa ohjeissa näytetään, miten PowerApp upotetaan verkkoasiakkaaseen.

1. Siirry sivulle, johon haluat upottaa PowerApp-sovelluksen. Tämä on sama sivu, joka sisältää mahdolliset PowerAppiin syötteenä välitettävät tiedot.
2. Avaa **Lisää PowerApp** -ruutu:

    - Valitse **Asetukset** ja valitse sitten **Mukauta tämä lomake**. Valitse **Lisää**-valikossa **PowerApp**. Valitse lopuksi alue, johon haluat lisätä PowerApp-sovelluksen. Jos haluat upottaa PowerAppin PowerApps-valikkopainikkeeseen, valitse Toimintoruutu. Jos haluat upottaa PowerApp-sovelluksen suoraan sivulle, valitse soveltuva välilehti, pikavälilehti, lehti tai osa (jos kyseessä on työtila).
    - Jos PowerAppia käytetään PowerApps-valikkopainikkeella, voit vaihtoehtoisesti valita vakiotoimintoruudun **PowerApps**-valikkopainikkeen ja valita sitten **Lisää PowerApp**.

3. Määritä upotettu PowerApp seuraavasti:

    - **Nimi**-kentässä on sen painikkeen tai välilehden teksti, joka sisältää upotetun PowerAppin. PowerApp-sovelluksen nimi on usein toistettava tässä kentässä.
    - **Sovelluksen tunnus** on PowerApp-sovelluksen upotettava GUID-tunnus. Voit noutaa tämän arvon etsimällä PowerAppin sivustossa [web.powerapps.com](https://web.powerapps.com) ja siirtymällä sitten **Sovelluksen tunnus** -kenttään **Tiedot**-kohdassa.
    - Voit vaihtoehtoisesti valita **Anna PowerApp-sovelluksen tiedot** -kohdan kenttä, joka sisältää PowerApp-sovellukselle syötteenä välitettävät tiedot. Lisätietoja tavoista, joilla PowerApp voi käyttää Finance and Operations -sovelluksista lähetettyjä tietoja, on jäljempänä tässä ohjeaiheessa kohdassa [Finance and Operations -sovellusten tietoja hyödyntävän PowerAppin muodostaminen](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps).
    - Valitse upotettavan PowerApp-sovelluksen tyyppiä vastaava **sovelluksen koko**. Jos PowerApps luodaan mobiililaitteille, valitse **Ohut**. Jos PowerApps luodaan tableteille, valitse **Leveä**. Tämä varmistaa, että upotetulle PowerAppille on varattu riittävästi tilaa.
    - **Yritykset**-pikavälilehdessä voi valita, mitkä yritykset voivat käyttää PowerAppia. PowerApp näytetään oletusarvoisesti kaikille yrityksille.

4. Kun vahvistus on tehty ja määrityksessä on kaikki oikein, lisää PowerApp sivulle valitsemalla **Lisää**. Sinua pyydetään päivittämään selain, jotta upotettu PowerApp tulee näkyviin.

## <a name="sharing-an-embedded-powerapp"></a>Upotetun PowerAppin jakaminen

Kun PowerApp on upotettu sivulle ja kun on vahvistettu, että se toimii oikein kaikkien sivulle välitettyjen tietokontekstien kanssa, upotettu PowerApp on mahdollista jakaa järjestelmän muiden käyttäjien kanssa. Sen voi tehdä kahdella tavalla käyttämällä tuotteen mukauttamisominaisuuksia:

- Suosituksena on pyytää järjestelmänvalvojaa toimittamaan mukautus kaikille käyttäjille tai osalle käyttäjiä.
- Vaihtoehtoisesti voit viedä sivun mukautukset, lähettää ne yhdelle tai usealle käyttäjälle ja näitä käyttäjiä tuomaan kyseiset muutokset. Voit viedä ja tuoda mukautuksia mukauttamisen työkalurivin Hallinta-asetuksella.

Lisätietoja tuotteen mukauttamistoiminnoista ja niiden käytöstä on kohdassa [Käyttökokemuksen mukauttaminen](personalize-user-experience.md).

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps"></a>Finance and Operations -sovellusten lähettämiä tietoja hyödyntävän PowerAppin luominen

Tärkeä osa Finance and Operations -sovelluksiin upotettavan PowerAppin muodostamista on Finance and Operations -sovellusten syöttötietojen käyttäminen. PowerApp-sovelluksen sisäpuolella syöttötietoja käytetään Param("EntityId")-muuttujan avulla.

Esimerkiksi PowerAppin OnStart-toiminnolle voi määrittää syöttötiedot Finance and Operations -sovelluksista muuttujalle seuraavalla tavalla:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-powerapp"></a>Upotetun PowerAppin näyttäminen

Voit tarkastella Finance and Operations -sovelluksien sivulle upotettua PowerAppia siirtymällä kyseiselle sivulle. Muista, että PowerAppsia voi käyttää vakiotoimintoruudun PowerApps-painikkeen avulla. Se voi näkymä myös suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana. Kun käyttäjä yrittää ladata sivulla PowerAppin, käyttäjää pyydetään kirjautumaan PowerAppsiin. Tällä tavoin varmistetaan, että käyttäjällä on soveltuvat PowerAppin käyttöoikeudet.

## <a name="editing-an-embedded-powerapp"></a>Upotetun PowerApp-sovelluksen muokkaaminen

Sivulle upotettu PowerApp saattaa vaatia muutoksia kyseisen PowerApp-sovelluksen määrityksiin. Voit esimerkiksi muokata upotetuun PowerApp-sovellukseen liitettyä otsikkoa. Jos on luotu uusi PowerApp-versio, sovelluksen tunnus on ehkä päivitettävä niin, että se osoittaa uusimpaan PowerApp-versioon.

Muokkaa upotetun PowerApp-sovelluksen konfiguraatiota näiden vaiheiden avulla:

1. Siirry **Muokkaa PowerApp-sovellusta** -ruutuun.

    - Jos upotettua PowerAppia käytetään suoraan PowerApps-valikkopainikkeella, napsauta hiiren kakkospainikkeella PowerApps-valikkopainiketta ja valitse **Mukauta**. Valitse määritettävä PowerApp avattavasta **Valitse PowerApp** -valikosta.
    - Jos upotettu PowerApp näkyy suoraan sivulla, valitse **Asetukset** ja valitse sitten **Mukauta tämä lomake**. Napsauta upotettua PowerAppia **Valinta**-työkalulla.

2. Tee PowerApps-määritykseen tarvittavat muutokset ja valitse sitten **Tallenna**.

## <a name="removing-an-embedded-powerapp"></a>Upotetun PowerApp-sovelluksen poistaminen

Upotetun PowerApp-sovelluksen voi tarvittaessa poistaa sivulta käyttämällä jompaakumpaa seuraavaa tapaa:

- Siirry **Muokkaa PowerApp-sovellusta** -ruutuun aiemmin tässä ohjeaiheessa olleen [Upotetun PowerApp-sovelluksen muokkaaminen](#editing-an-embedded-powerapp) -osan ohjeiden avulla. Vahvista, että ruudussa on sen upotetun PowerApp-sovelluksen tiedot, jonka haluat poistaa, ja valitse sitten **Poista**-painike.
- Koska PowerApp on tallennettu mukautuksen tietoina, sivun mukautuksen tyhjentäminen poistaa myös kaikki sivulle upotetut PowerApps-sovellukset. Huomaa, että sivun mukautukset tyhjennetään pysyvästi. Tyhjennystä ei voi peruuttaa. Voit poistaa sivun mukautukset valitsemalla ensin **Asetukset** ja sitten **Mukauta tämä lomake**. Valitse **Hallinta**-valikossa **Tyhjennä**-painike. Kaikki tämän sivun edelliset mukautukset poistetaan, kun selain päivitetään. Lisätietoja sivujen optimoinnista mukauttamisen avulla on kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md).

## <a name="appendix"></a>Liite

### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Kehittäjä päättää, minne PowerApp voidaan upottaa

Käyttäjät voivat upottaa PowerAppsin oletusarvoisesti mille tahansa sivulle joko PowerApps-valikkopainikkeeseen tai suoraan sivulle välilehtinä, pikavälilehtinä tai työtilan uutena osana. Kehittäjät voivat kuitenkin tarvittaessa määrittää tämän toiminnon niin, että se sallii PowerAppsin upottamisen vain tietyillä sivuilla. Se tehdään seuraavasti:

- **isPowerAppPersonalizationEnabled** – Jos tämä menetelmä palauttaa epätosi-arvon tietylle sivulle, PowerApps-valikkopainike ei ole näkyvissä. Tällöin käyttäjät eivät voi upottaa PowerAppsia sivulle edes välilehtenä.
- **isPowerAppTabPersonalizationEnabled** – Jos tämä menetelmä palauttaa epätosi-arvon tietylle sivulle, käyttäjät eivät voi upottaa PowerAppsia suoraan sivulle välilehtenä, pikavälilehtenä tai panoraamaosana. Käyttäjät voivat edelleen upottaa PowerAppsin PowerApps-valikkopainikkeella, jos sivu sallii upottamisen.

Seuraavassa esimerkissä on uusi luokka ja kaksi menetelmää, jotka tarvitaan määrittämään, minne PowerApps voidaan upottaa.

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
