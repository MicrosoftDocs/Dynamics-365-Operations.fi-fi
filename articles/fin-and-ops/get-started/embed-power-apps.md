---
title: PowerApps-sovellusten muokkaaminen
description: "Tässä ohjeaiheessa käsitellään PowerAppsin upottamista Finance and Operations -asiakasohjelmaan laajentamaan tuotteen toimintoja."
author: jasongre
manager: AnnBe
ms.date: 04/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 07224faabcf2b183d4c8da0ba4588c33ec140d03
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="embed-powerapps"></a>PowerApps-sovellusten muokkaaminen

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [banner](../includes/pre-release.md)]

Ympäristöpäivityksen versiossa 14 Microsoft Dynamics 365 for Finance and Operations tukee Microsoft PowerApps -integrointia, palvelua, jonka avulla kehittäjät ja muut kuin tekniset käyttäjät voivat luoda mukautettuja liiketoimintasovelluksia mobiililaitteille, tabletteja ja verkkoa ilman koodin kirjoittamista. Sinun, organisaatiosi tai laajemman ekosysteemin muodostama PowerApps voidaan tämän jälkeen upottaa Finance and Operations -asiakasohjelmaan. Tämä laajentaa tuotteen toimintoja. Voit esimerkiksi luoda PowerApp-sovelluksen ja täydentää Finance and Operations -sovellusta toisesta järjestelmästä haetuilla tiedoilla. 

Lisätietoja PowerAppsin upottamisesta on lyhyessä videossa [PowerAppsin upottaminen Dynamics 365 for Finance and Operationsissa](https://www.youtube.com/watch?v=x3qyA1bH-NY).

> [!Video https://www.youtube.com/embed/x3qyA1bH-NY]

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Upotetun PowerApp-sovelluksen lisääminen sivulle
### <a name="overview"></a>Yleiskuvaus
Ennen kuin PowerApp voidaan upottaa Finance and Operations -asiakasohjelmaan, käyttäjän on ensin etsittävä PowerApp, jolla on halutut visuaaliset elementit ja/tai toiminnot tai luotava se. PowerAppin muodostamisprosessia ei käsitellä tässä yksityiskohtaisesti. Ohjeaihe [PowerAppsin esittely](https://docs.microsoft.com/en-us/powerapps/getting-started) on lähtökohta, jos olet uusi PowerAppsin käyttäjä.

Kun olet valmis upottamaan tietyn PowerAppin, PowerAppia voi käyttää sivulla kahdella tavalla. Voit valita skenaarioosi paremmin sopivan tavan. Ensimmäinen tapa tehdään tavalliseen toimintoruutuun lisätyn PowerApps-painikkeen avulla. Tämän mekanismin avulla lisätty PowerApps näkyy valikon vaihtoehtoina PowerApps-valikkopainikkeessa. Valittaessa jokainen näistä valikkovaihtoehdoista avaa upotetun PowerAppin sisältävän sivuruudun. Vaihtoehtoisesti voit näyttää PowerApp-sovelluksen suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana. 

Kun määrität upotettua PowerAppia Finance and Operationsin, voit valita yhden kentän, jonka haluat lähettää syötteenä PowerAppiin. Tällä tavoin PowerApp voi reagoida Finance and Operationsissa katsottavana olevien tietojen perusteella.  

### <a name="details"></a>Erittely
Seuraavissa ohjeissa näytetään, miten PowerApp upotetaan Finance and Operations -verkkoasiakkaaseen.  

1. Siirry sivulle, johon haluat upottaa PowerApp-sovelluksen. Tämä on sama sivu, joka sisältää mahdolliset PowerAppiin syötteenä välitettävät tiedot.  
2. Avaa **Lisää PowerApp** -ruutu:
   - Valitse **Asetukset** ja valitse sitten **Mukauta tämä lomake**. Valitse **Lisää**-valikossa **PowerApp**. Valitse lopuksi alue, johon haluat lisätä PowerApp-sovelluksen. Jos haluat upottaa PowerApp-sovelluksen PowerApps-valikkopainikkeen alle, valitse Toimintoruutu. Jos haluat upottaa PowerApp-sovelluksen suoraan sivulle, valitse soveltuva välilehti, pikavälilehti, lehti tai osa (jos kyseessä on työtila).   
   - Jos PowerApp-sovellusta käytetään PowerApps-valikkopainikkeen avulla, voit vaihtoehtoisesti valita vakiotoimintoruudun **PowerApps**-valikkopainikkeen ja valita sitten **Lisää PowerApp-sovellus**.  
3. Määritä upotettu PowerApp seuraavasti:
   - **Nimi**-kentässä on sen painikkeen tai välilehden teksti, joka sisältää upotetun PowerAppin. PowerApp-sovelluksen nimi on usein toistettava tässä kentässä.  
   - **Sovelluksen tunnus** on PowerApp-sovelluksen upotettava GUID-tunnus. Voit noutaa tämän arvon etsimällä PowerAppin sivustossa [web.powerapps.com](https://web.powerapps.com) ja siirtymällä sitten **Sovelluksen tunnus** -kenttään **Tiedot**-kohdassa.  
   - Voit vaihtoehtoisesti valita **Anna PowerApp-sovelluksen tiedot** -kohdan kenttä, joka sisältää PowerApp-sovellukselle syötteenä välitettävät tiedot. Lisätietoja tavoista, joilla PowerApp voi käyttää Finance and Operationsista lähetettyjä tietoja, on jäljempänä tässä ohjeaiheessa kohdassa [Finance and Operationsin tietoja hyödyntävän PowerAppin muodostaminen](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations).  
   - Valitse upotettavan PowerApp-sovelluksen tyyppiä vastaava **sovelluksen koko**. Jos PowerApps luodaan mobiililaitteille, valitse **Ohut**. Jos se luodaan tableteille, valitse **Leveä**. Tämä varmistaa, että upotetulle PowerAppille on varattu riittävästi tilaa.
   - **Yritykset**-pikavälilehdessä voi valita, mitkä yritykset voivat käyttää PowerAppia. PowerApp näytetään oletusarvoisesti kaikille yrityksille.  
4. Kun vahvistus on tehty ja määrityksessä on kaikki oikein, lisää PowerApp sivulle valitsemalla **Lisää**. Sinua pyydetään päivittämään selain, jotta upotettu PowerApp tulee näkyviin. 

## <a name="sharing-an-embedded-powerapp"></a>Upotetun PowerAppin jakaminen
Kun PowerApp on upotettu sivulle ja kun on vahvistettu, että se toimii oikein kaikkien sivulle välitettyjen tietokontekstien kanssa, upotettu PowerApp on mahdollista jakaa järjestelmän muiden käyttäjien kanssa. Sen voi tehdä kahdella tavalla käyttämällä tuotteen mukauttamisominaisuuksia:

- Suosituksena on pyytää järjestelmänvalvojaa toimittamaan mukautus kaikille käyttäjille tai osalle käyttäjiä. 

- Vaihtoehtoisesti voit viedä sivun mukautukset, lähettää ne yhdelle tai usealle käyttäjälle ja näitä käyttäjiä tuomaan kyseiset muutokset. Voit viedä ja tuoda mukautuksia mukauttamisen työkalurivin Hallinta-asetuksella.

Lisätietoja tuotteen mukauttamistoiminnoista ja niiden käytöstä on kohdassa [Käyttökokemuksen mukauttaminen](personalize-user-experience.md).

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a>Finance and Operations -sovelluksen lähettämiä tietoje hyödyntävän PowerApp-sovelluksen luominen
Tärkeä osa luotaessa PowerApp-sovellusta, joka upotetaan Finance and Operations -sovellukseen ja joka käyttää Finance and Operations -sovelluksen syöttötietoja. PowerApp-sovelluksen sisäpuolella syöttötietoja käytetään Param("EntityId")-muuttujan avulla.  

Esimerkiksi PowerApp-sovelluksen OnStart-toiminnolle voi määrittää syöttötiedot Finance and Operations -sovelluksesta muuttujalle seuraavalla tavalla:

If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, "")); 

## <a name="viewing-an-embedded-powerapp"></a>Upotetun PowerAppin näyttäminen
Voit tarkastella Finance and Operationsin sivulla upotettua PowerAppia siirtymällä kyseiselle sivulle. Muista, että PowerApps-sovellusta voi käyttää vakiotoimintoruudun PowerApps-painikkeen avulla tai se voi olla suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana. Kun käyttäjä yrittää ladata PowerAppin sivulla, häntä pyydetään kirjautumaan PowerAppsiin. Tällä tavoin varmistetaan, että käyttäjällä on soveltuvat PowerAppin käyttöoikeudet.   

## <a name="editing-an-embedded-powerapp"></a>Upotetun PowerApp-sovelluksen muokkaaminen
Sivulle upotettu PowerApp saattaa vaatia muutoksia kyseisen PowerApp-sovelluksen määrityksiin. Voit esimerkiksi muokata upotetuun PowerApp-sovellukseen liitettyä otsikkoa. Jos on luotu uusi PowerApp-versio, sovelluksen tunnus on ehkä päivitettävä niin, että se osoittaa uusimpaan PowerApp-versioon. 

Muokkaa upotetun PowerApp-sovelluksen konfiguraatiota näiden vaiheiden avulla:
1. Siirry **Muokkaa PowerApp-sovellusta** -ruutuun. 
   - Jos upotettua PowerApp-sovellusta käytetään suoraan PowerApps-valikkopainikkeen avulla, napsauta hiiren kakkospainikkeella PowerApps-valikkopainiketta ja valitse **Mukauta**. Valitse määritettävä PowerApp avattavasta **Valitse PowerApp** -valikosta.  
   - Jos upotettu PowerApp näkyy suoraan sivulla, valitse **Asetukset** ja valitse sitten **Mukauta tämä lomake**. Napsauta upotettua PowerAppia **Valinta**-työkalulla.  
2. Tee PowerApps-määrityksen tarvittavat muutokset ja valitse sitten **Tallenna**.  

## <a name="removing-an-embedded-powerapp"></a>Upotetun PowerApp-sovelluksen poistaminen
Upotetun PowerApp-sovelluksen voi tarvittaessa poistaa sivulta käyttämällä jompaakumpaa seuraavaa tapaa: 

- Siirry **Muokkaa PowerApp-sovellusta** -ruutuun aiemmin tässä ohjeaiheessa olleen [Upotetun PowerApp-sovelluksen muokkaaminen](#editing-an-embedded-powerapp) -osan ohjeiden avulla. Vahvista, että ruudussa on sen upotetun PowerApp-sovelluksen tiedot, jonka haluat poistaa, ja valitse sitten **Poista**-painike. 

- Koska PowerApp on tallennettu mukautuksen tietoina, sivun mukautuksen tyhjentäminen poistaa myös kaikki sivun upotetut PowerApps-sovellukset. Huomaa, että sivun mukautukset tyhjennetään pysyvästi. Tyhjennystä ei voi peruuttaa. Voit poistaa sivun mukautukset valitsemalla ensin **Asetukset** ja sitten **Mukauta tämä lomake**. Valitse **Hallinta**-valikossa **Tyhjennä**-painike. Kaikki tämän sivun edelliset mukautukset poistetaan, kun selain päivitetään. Lisätietoja sivujen optimoinnista mukauttamisen avulla on kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md).  

## <a name="appendix"></a>Liite 
### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Kehittäjä päättää, minne PowerApp voidaan upottaa
Käyttäjät voivat upottaa PowerApps-kohteet oletusarvoisesti mille tahansa sivulle joko PowerApps-valikkopainikkeen alla tai suoraan sivulla välilehtinä, pikavälilehtinä tai työtilan uutena osana. Kehittäjät voivat kuitenkin tarvittaessa määrittää tämän toiminnon niin, että se sallii PowerApps-sovellusten upottamisen vain tietyillä sivuilla. Tämä tapahtuu seuraavien menetelmien avulla: 

- **isPowerAppPersonalizationEnabled** - Jos tämä menetelmä palauttaa epätosi-arvon tietylle sivulle, PowerApps-valikkopainike ei ole näkyvissä. Tällöin käyttäjät eivät voi upottaa PowerApps-sovellusta sivulle, mukaan luettuna välilehtenä upottaminen. 

- **isPowerAppTabPersonalizationEnabled** - Jos tämä menetelmä palauttaa epätosi-arvon tietylle sivulle, käyttäjät eivät voi upottaa PowerApps-sovellusta suoraan sivulle välilehtenä, pikavälilehtanä tai panoraamaosana. Käyttäjät voivat edelleen upottaa PowerAppsin PowerApps-valikkopainikkeella, jos sivu sallii upottamisen.  

Seuraavassa esimerkissä on uusi luokka ja kaksi menetelmää, jotka tarvitaan PowerAppsin upottamista varten.  

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{

    public static boolean isPowerAppPresonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPresonalizationEnabled(pageName);
        return true;
    }

    public static boolean isPowerAppTabPresonalizationEnabled(str pageName)   
    {
        var result = next isPowerAppTabPresonalizationEnabled(pageName);
        return true;
    }
    ```

}


