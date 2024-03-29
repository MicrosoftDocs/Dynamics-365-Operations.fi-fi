---
title: Kaksoiskirjoituksen yleiskatsaus
description: Tässä artikkelissa on kaksoiskirjoituksen yleiskatsaus, joka sisältää lähes reaaliaikaisen vuorovaikutuksen asiakkaiden aktivointisovellusten sekä talous- ja toimintosovellusten välillä.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 943607a3ef28db11b7bc7805257914117e6ae38c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289635"
---
# <a name="dual-write-overview"></a>Kaksoiskirjoituksen yleiskatsaus

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Mikä on kaksoiskirjoitus?

Kaksoiskirjoitus on valmis infrastruktuuri, joka sisältää lähes reaaliaikaisen vuorovaikutuksen asiakasvuorovaikutussovellusten sekä talous- ja toimintosovellusten välillä. Kun asiakkaiden, tuotteiden, henkilöiden ja toimintojen tiedot siirretään sovellusten ulkopuolelle, kaikki organisaation osastot voivat käyttää niitä.

Kaksoiskirjoitus sisältää tiiviisti yhdistetyn, kaksisuuntaisen integroinnin talous- ja toimintosovellusten sekä Dataversen välillä. Kaikki tietojen muutokset talous- ja toimintosovelluksissa aiheuttavat kaksoiskirjoituksia Dataversessä ja Dataversen tietojen muutokset puolestaan kirjoituksia talous- ja toimintosovelluksissa. Tämä automatisoitu tietovirta tarjoaa integroidun käyttökokemuksen eri sovelluksissa.

![Tietojen suhde sovellusten välillä.](media/dual-write-overview.jpg)

Kaksoiskirjoituksissa on eri osaa: *infrastruktuuri* ja *sovellus*.

### <a name="infrastructure"></a>Infrastruktuuri

Kaksoiskirjoituksen infrastruktuuri on laajennettavissa. Se on luotettava infrastruktuuri, joka sisältää seuraavat keskeiset ominaisuudet:

+ Sovellusten välinen synkroninen ja kaksisuuntainen tietovirta
+ Synkronisointi yhdessä toiston, pysäytyksen ja kertymän tilojen kanssa tukee järjestelmää online- ja offline-tilassa sekä asynkronisessa tilassa.
+ Mahdollisuus synkronoida alkuperäiset tiedot sovellusten välillä
+ Yhdistetty näkymä toiminto- ja virhelokeista tietojen järjestelmänvalvojille
+ Mahdollisuus määrittää mukautettuja hälytyksiä ja rajoja sekä tilata ilmoituksia
+ Intuitiivinen käyttöliittymä suodatusta ja muunnoksia varten
+ Mahdollisuus määrittää ja tarkastella taulukoiden riippuvuuksia ja suhteita
+ Laajennettavuus sekä vakioentiteeteille että mukautetuille tauluille ja määrityksille
+ Luotettava sovelluksen elinkaaren hallinta
+ Uusien asiakkaiden valmis määrityskokemus

### <a name="application"></a>Hakemus

Kaksoiskirjoitus luo yhdistämismäärityksen talous- ja toimintosovellusten käsitteiden sekä asiakkaiden aktivointisovellusten käsitteiden välille. Tämä integraatio tukee seuraavia skenaarioita:

+ Integroidut asiakkaan päätiedot
+ Asiakkaan kanta-asiakaskorttien ja palkkiopisteiden käyttöoikeus
+ Yhtenäinen tuotteiden hallinnan kokemus
+ Tietoja organisaatiohierarkiasta
+ Integroidut toimittajan päätiedot
+ Talous- ja veroviitetietojen käyttöoikeus
+ Tarvittaessa käytettävän hinnoitteluohjelman käyttökokemus
+ Integroitu prospektista käteiseksi -käyttökokemus
+ Mahdollisuus sekä sisäisten resurssien että asiakkaan resurssien käyttämiseen kentän edustajien kautta
+ Integroitu hankinnasta maksuun -käyttökokemus
+ Asiakastietojen ja asiakirjojen integroidut aktiviteetit ja huomautukset
+ Mahdollisuus etsiä käytettävissä olevan varaston saatavuutta ja tietoja
+ Projektista käteiseksi -käyttökokemus
+ Mahdollisuus käsitellä useita osoitteita ja rooleja osapuolen käsitteen kautta


## <a name="top-reasons-to-use-dual-write"></a>Yleisimmät syyt kaksoiskirjoittamisen käyttämiseksi

Kaksoiskirjoitus mahdollistaa tietojen integroinnin Microsoft Dynamics 365 -sovelluksissa Tämä luotettava kehys linkittää ympäristöt ja mahdollistaa erilaisten liiketoimintasovellusten käyttämisen yhdessä. Seuraavassa kerrotaan tärkeimmät syyt kaksoiskirjoituksen käyttämiseksi:

+ Kaksoiskirjoitus mahdollistaa tiiviisti yhdistetyn ja lähes reaaliaikaisen kaksisuuntaisen integroinnin taloushallinnon toimintojen sovellusten ja asiakasvuorovaikutussovellusten välillä. Tämä integraatio tekee Microsoft Dynamics 365:stä yhden pysähdyksen kaupan kaikille liiketoimintasovelluksille. Asiakkaat, jotka käyttävät Dynamics 365 Financea ja Dynamics 365 Supply Chain Managementia, mutta jotka käyttävät asiakkuudenhallintaan (CRM) jotain muuta kuin Microsoftin ratkaisua, siirtyvät kohti Dynamics 365:ttä sen kaksoiskirjoitustuen vuoksi.
+ Asiakkaiden, tuotteiden, toimintojen, projektien ja esineiden internetin tiedot siirtyvät automaattisesti Dataverseen kaksoiskirjoituksen kautta. Tämä yhteys on hyödyllinen yrityksille, jotka ovat kiinnostuneita Power Platform -laajennuksista.
+ Kaksoiskirjoitusinfrastruktuuri noudattaa kooditonta / vähäisen koodin periaatetta. Vakiomuotoisten taulukosta taulukkoon -määritysten ja mukautettujen määritysten laajentamisessa ei tarvita paljon kehitystyötä.
+ Kaksoiskirjoitus tukee sekä online- että offline-tilaa. Microsoft on ainoa yritys, joka tarjoaa tukea online-ja offline-tilassa.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Mitä kaksoiskirjoitus tarkoittaa asiakkaiden aktivointisovellusten kehittäjille ja arkkitehdeille?

Kaksoiskirjoitus automatisoi tietovirran talous- ja toimintosovellusten sekä asiakkaiden aktivointisovellusten välillä. Kaksoiskirjoitus sisältää kaksi AppSource-ratkaisua, jotka on asennettu Dataverseen. Ratkaisut laajentavat taulukon rakennetta, laajennuksia ja työnkulkuja Dataversessa niin, että ne voidaan ottaa käyttöön ERP:ssä. Käyttöönotto onnistuu, jos asiakkaiden aktivointisovellusten kehittäjät ja arkkitehdit ymmärtävät nämä muutokset ja tekevät yhteistyötä talous- ja toimintosovellusten vastaavien henkilöiden kanssa.

Jos haluat luoda pariteetin talous- ja toimintosovellusten kanssa, kaksoiskirjoitus tekee joitakin tärkeitä muutoksia Dataverse -rakenteeseen. Voit välttää suunnittelu- ja kehitystyön toistoja tulevaisuudessa, jos ymmärrät tämän suunnitelman.

+ Kun kaksoiskirjoituksen AppSource-paketti on asennettu, Dataverse sisältää uusia käsitteitä, kuten yritys ja osapuoli. Näiden käsitteiden avulla Dataversen pohjalta luodut sovellukset, kuten Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service ja Dynamics 365 Field Service voivat toimia saumattomasti yhdessä talous- ja toimintosovellusten kanssa.

+ Toiminnot ja huomautukset ovat yhtenäisiä ja laajenevat tukemaan sekä C1 (järjestelmän käyttäjät)- että C2 (järjestelmän asiakkaat) -kohteita.

+ Voit estää tietojen menettämisen talous- ja toimintosovellusten sekä Dataversen välisessä tiedonsiirrossa laajentamalla desimaalien määrää asiakkaiden aktivointisovellusten valuuttatietotyypissä. Ominaisuus muuntaa automaattisesti olemassa olevat taulut uuteen laajennettuun tilaan metatietotasolla. Tämän prosessin aikana valuutta-arvo muunnetaan desimaalidataksi, ei rahamääräiseksi dataksi. Valuutta-arvo tukee 10 desimaalia. Tämän ominaisuuden käyttäminen edellyttää suostumusta. Organisaatiot, joilla ei ole tarvetta yli 4 desimaalin tarkkuudelle, eivät tarvitse ominaisuutta. Lisätietoja on kohdassa [Valuutan tietotyypin siirto kaksoiskirjoitusta varten](currrency-decimal-places.md).

+ [Voimassaolopäivä](../../dev-tools/date-effectivity.md) lisätään Dataverseen. Se tukee mennyttä, nykyistä ja tulevaa päivämäärää samassa taulukossa.

+ Tuotteen [yksikkömuunnoksia](../../../../supply-chain/pim/tasks/manage-unit-measure.md) tuetaan tuotteissa, tarjouksissa, tilauksissa ja laskuissa.

Lisätietoja tulevista muutoksista on kohdassa [Kaksoiskirjoituksen uudet ja muuttuneet ominaisuudet](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

