---
title: Poistetut tai vanhentuneet Dynamics 365 Commerce -ominaisuudet
description: Tässä artikkelissa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Commercesta.
author: josaw
ms.date: 07/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a59d62ad846eed659fa4e70390ebafc40127df0f
ms.sourcegitcommit: ef56b5d0ed26e373add5dec63168e08ade40573e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/12/2022
ms.locfileid: "9138583"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Poistetut tai vanhentuneet Dynamics 365 Commerce -ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Commercesta.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi. 

> [!NOTE]
> Seuraavissa raporteissa on lisätietoja talous- ja toimintosovellusten objekteista: [Tekniset viitetiedot](/dynamics/s-e/). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin talous- ja toimintosovellusten versiossa.

## <a name="feature-deprecation-effective-july-2022"></a>Heinäkuussa 2022 vanhentuvat ominaisuudet

### <a name="commerce-analytics-preview"></a>Commercen analytiikka (esiversio)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Dynamics 365 Commerce -tiimi on analysoinut Commerce analytiikka (esiversio) -ominaisuuden käyttöä ja käyttöönottoa sekä päättänyt, että ominaisuuden kehittämistä ei jatketa yleiseen saatavuuteen.   |
| **Onko toinen ominaisuus korvannut?**   | Commerce-analytiikka (esiversio) -ominaisuutta ei tällä hetkellä korvata toisella ominaisuudella tai ratkaisulla. Tapahtumien raakatietoja ja päätietojen vienti talous- ja toimintosovelluksista Azure Data Lakeen on edelleen saatavana, mistä on lisätietoja kohdassa [Vienti Data Lakeen talous- ja toimintosovelluksissa](../../fin-ops-core/dev-itpro/data-entities/finance-data-azure-data-lake.md). Kumppanit ja asiakkaat voivat hyödyntää kyseistä tietovirtaa liiketoiminatarpeita vastaavien analyysiraporttien laatimiseen.
| **Tuotealueet, joihin vaikutetaan**         | Commercen analytiikka (esiversio) |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Tämä ominaisuus on tarkoitus poistaa käytöstä 30. elokuuta 2022 mennessä.  Kyseisen päivämäärän jälkeen nykyisiä Commerce-analytiikan (esiversio) tuottamia Power BI -raportteja ei päivitetä.     |


## <a name="features-removed-or-deprecated-in-the-commerce-10025-release"></a>Commercen version 10.0.25 poistetut tai vanhentuneet ominaisuudet

### <a name="modern-point-of-sale-mpos"></a>Modern Point of Sale (MPOS)

Modern Point of Sale (MPOS) -sovellus vanhentuu Commerce-versiossa 10.0.25 ja se korvataan Store Commerce -sovelluksella.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Myymäläsovellukset ovat Dynamics 365 Commercen monikanavaisen tarjonnan kulmakivi. Kehitämme jatkuvasti innovaatioita tarjotaksemme nykyaikaisen ja älykkään myymäläkokemuksen. Tämän lisäksi nykyaikaistamme ratkaisuamme ottamalla käyttöön uusia muutoksia, jotka parantavat IT-toimintojen ja käyttäjien kokemusta merkittävästi Windows-myymäläsovelluksissamme. Uusi Store Commerce -sovellus on olemassa olevan MPOS-sovelluksen tekniikkapäivitys. Se parantaa suorituskykyä, luotettavuutta ja pitkäaikaista tukea Windows-alustalla, eikä sovellusta tarvitse pakata uudelleen kullakin päivityksellä. |
| **Onko toinen ominaisuus korvannut?**   |  [Store Commerce](../dev-itpro/store-commerce.md) |
| **Tuotealueet, joihin vaikutetaan**         | Modern Point of Sale |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Commerce-versiosta 10.0.25 alkaen MPOS-asennusohjelma, joka lähetetään LCS-virtuaalikoneiden kautta, poistetaan lokakuussa 2023. |

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Commercen version 10.0.21 poistetut tai vanhentuneet ominaisuudet

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Commercen parametrien päällekkäisten alennusten käsittelyasetus

**Päällekkäisten alennusten käsittely** -asetus **Commercen parametrit** -sivulla on vanhentunut Commercen versiossa 10.0.21. Jatkossa Commercen hinnoittelumoduuli käyttää yhtä algoritmia päällekkäisten alennusten optimaalisen yhdistelmän määrittämiseen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | <p>Commercen parametrien **Päällekkäisten alennusten käsittely** -asetus ohjaa, miten Commerce-hinnoittelumoduuli hakee ja määrittää päällekkäisten alennusten optimaalisen yhdistelmän. Tällä hetkellä käytettävissä on kolme vaihtoehtoa:<p><ul><li> **Paras suorituskyky** – tämä vaihtoehto käyttää edistynyttä heuristista algoritmia ja [raja-arvon luokittelua](../optimal-combination-overlapping-discounts.md) parhaan alennusyhdistelmän priorisointiin, arviointiin ja määrittämiseen oikea-aikaisesti.</li><li>**Tasapainotettu laskenta** – Nykyisessä koodikannassa tämä vaihtoehto toimii samoin kuin **Paras suorituskyky** -vaihtoehto. Niinpä se on käytännössä kaksinkertainen vaihtoehto.</li><li>**Tyhjentävä laskenta** – Tämä vaihtoehto käyttää vanhaa algoritmia, joka käsittelee kaikki mahdolliset alennuslaskelmat hinnanlaskennan aikana. Jos tilauksessa on paljon rivejä ja suuria määriä, tämä vaihtoehto voi aiheuttaa suorituskykyongelmia.</li></ul><p>Määrityksien yksinkertaistamista, suorituskyvyn parantamista ja vanhan algoritmin aiheuttamien tapahtumien vähentämistä varten **Päällekkäisten alennusten käsittely** -asetus poistetaan kokonaan ja Commercen hinnoittelumoduuliin sisäinen logiikka päivitetään siten, se käyttää nyt vain kehittynyttä algoritmia (eli algoritmia, johon **Paras suorituskyky** -vaihtoehto perustuu).</p> |
| **Onko toinen ominaisuus korvannut?**   | Et voi. Organisaatioiden kannattaa käyttää **Tasapainotettu laskenta**- tai **Tyhjentävä laskenta** -vaihtoehto korvataan **Paras suorituskyky** -vaihtoehdolla ennen tämän ominaisuuden poistamista. |
| **Tuotealueet, joihin vaikutetaan**         | Hinnoittelu ja alennukset |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Versiosta 10.0.21 alkaen **Päällekkäisten alennusten käsittely** -asetus poistetaan Commercen parametreista lokakuussa 2022. |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>Retail SDK:n jakelu Lifecycle Servicesin avulla

Retail SDK toimitetaan Lifecycle Servicesin (LCS) mukana. Tämä jakelutapa vanhenee versiossa 10.0.21. Jatkossa Retail SDK -viitepaketit, -kirjastot ja -näytteet julkaistaan GitHubin julkisissa säilöissä.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Retail SDK toimitetaan LCS:n mukana. LCS-prosessin valmistuminen kestää muutaman tunnin, ja tämä prosessi on toistettava kunkin päivityksen yhteydessä. Jatkossa Retail SDK -viitepaketit, -kirjastot ja -näytteet julkaistaan GitHubin julkisissa säilöissä. Laajennusnäytteiden ja viitepakettien käyttäminen on helppoa, ja päivitykset valmistuvat muutamassa minuutissa. |
| **Onko toinen ominaisuus korvannut?**   |  [Retail SDK -näytteiden ja -viitepakettien lataaminen GitHubista ja NuGetista](../dev-itpro/retail-sdk/sdk-github.md) |
| **Tuotealueet, joihin vaikutetaan**         | Retail SDK |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: versiosta 10.0.21 alkaen LCS-virtuaalikoneiden kautta toimitettu SDK poistetaan lokakuussa 2023. |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>Retail-käyttöottopaketti sekä yhdistetyt myyntipisteen, Hardware stationin ja Cloud Scale unitin asennusohjelmat

Retail-käyttöottopaketit, jotka luotiin Retail SDK MSBuildin avulla, vanhentuvat versiossa 10.0.21. Jatkossa käytetään Cloud Scale Unit -laajennusten (Commerce Runtime, kanavatietokanta, Commerce headless-ohjelmointirajapinnat, maksut ja Cloud Point of Sale) Cloud Scale Unit (CSU) -pakettia. Vain laajennusten myyntipisteen, Hardware stationiin ja Cloud scale unitin asennusohjelmia käytetään paikallisessa ympäristössä.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Retail-käyttöönottopaketti on yhdistelmäpaketti, joka sisältää kaikki laajennuspaketit ja asennusohjelmat. Tämän yhdistelmäpaketin vuoksi käyttöönotto on monimutkaista, sillä CSU-laajennukset koskevat Cloud scale unitia ja asennusohjelmat otetaan käyttöön myymälöissä. Asennusohjelmat sisältävät laajennuksen ja perustuotteen, mikä hankaloittaa päivityksiä. Kunkin päivityksen yhteydessä on suoritettava koodien yhdistäminen ja paketin luonti. Prosessia yksinkertaistetaan siten, että laajennuspaketit ovat nyt erillisiä osia, mikä helpottaa käyttöönottoa ja hallintaa. Tämän uuden menettelyn ansiosta laajennusten ja perustuotteen asennusohjelmat on erotettu toisistaan, ja niitä voidaan ylläpitää ja päivittää erikseen ilman koodin yhdistämistä tai uudelleenpakkausta.|
| **Onko toinen ominaisuus korvannut?**   | CSU-laajennukset, myyntipistelaajennuksen asennusohjelmat, Hardware station -laajennuksen asennusohjelmat |
| **Tuotealueet, joihin vaikutetaan**         | Dynamics 365 Commerce -laajennus ja käyttöönotto |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: versiosta 10.0.21 alkaen, LCS:n RetailDeployablePackage-käyttöönoton tuki poistetaan lokakuussa 2022. |

Lisätietoja:

+ [Commerce Cloud Scale Unitin (CSU) erillisen paketin luominen](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [Modern POS -laajennuspaketin luominen](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [Myyntipisteen integroiminen uuteen laitteeseen](../dev-itpro/hardware-device-extension.md)
+ Koodimallit
    + [Cloud Scale Unit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [Myyntipiste, CSU and Hardware station](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln and CloudPos.sln Retail SDK:ssa

Myyntipistelaajennuksen kehittäminen ModernPos.sln-, CloudPos.sln-, POS.Extension.csproj-tiedostojen avulla ja myyntipistekansio vanhentuvat versiossa 10.0.21. Jatkossa käytetään itsenäistä myyntipisteen myyntipistelaajennusten pakkaus-SDK:ta.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Jos aiemmissa Retail SDK -versioissa oli myyntipistelaajennuksia, päivittäminen uusimpaan myyntipisteversioon edellytti koodin yhdistämistä ja uudelleenpakkaamista. Koodin yhdistämisen vuoksi päivitysprosessi kesti kauan, minkä lisäksi säilössä oli ylläpidettävä täydellistä Retail SDK:ta. Lisäksi oli käännettä POS.App-ydinprojekti. Itsenäistä pakkausmallia käytettäessä vain laajennusta on ylläpidettävä. Myyntipistelaajennusten uusimpaan versioon päivittämien sujuu kätevästi päivittämällä projektin käyttämä NuGet-paketin versio. Laajennukset voidaan ottaa käyttöön itsenäisesti, ja palvelut käyttävät laajennuksen asennusohjelmia. Perusmyyntipisteet voivaan ottaa käyttöön ja niitä voidaan huoltaa erikseen, eikä koodia tarvitse yhdistää tai pakata uudelleen perusasennusohjelmaan tai koodiin. |
| **Onko toinen ominaisuus korvannut?**   | [Myyntipisteen itsenäinen pakkauksen SDK](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Tuotealueet, joihin vaikutetaan**         | Dynamics 365 Commercen myyntipistelaajennus ja käyttöönotto |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: versiosta 10.0.21 alkaen yhdistettyjen myyntipistepakettien ja laajennusmallin tuki ModernPos.Sln-, CloudPOs.sln- ja POS.Extensons.csproj-tiedostojen käytölle Retail SDK:ssa poistetaan lokakuussa 2023. |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Commercen version 10.0.17 poistetut tai vanhentuneet ominaisuudet

### <a name="full-dataset-generation-interval-is-deprecated"></a>Täyden tietojoukon luonnin aikaväli on vanhentunut

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tästä versiosta lähtien Dynamics 365 headquarters -sovelluksen **Kaupankäynnin ajoitustyökalun parametrit** -lomakkeessa **Täyden tietojoukon luonnin aikaväli päivinä** poistetaan. Tästä versiosta alkaen kenttä poistetaan visuaalisesti, jotta arvoa ei voi muokata. Tämä pysyy arvona **0**. |
| **Onko toinen ominaisuus korvannut?**   | Ei |
| **Tuotealueet, joihin vaikutetaan**         | Dynamics 365 Commerce |
| **Käytön asetukset**              | Kaikki|
| **Tila**                         | Vanhentunut. Älä käytä tätä kenttää tai muuta sen arvoa.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Commercen version 10.0.15 poistetut tai vanhentuneet ominaisuudet

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11:n Dynamics 365 -tuki on vanhentunut

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Joulukuusta 2020 alkaen kaikkien Dynamics 365 -tuotteiden Microsoft Internet Explorer 11 -tuki vanhenee eikä Internet Explorer 11:tä tueta elokuun 2021 jälkeen.<br><br>Tämä vaikuttaa sellaisiin Dynamics 365 -tuotteita käyttäviin asiakkaisiin, jotka on suunniteltu käytettäviksi Internet Explorer 11 -liittymässä. Elokuun 2021 jälkeen Internet Explorer 11:tä ei tueta kyseisissä Dynamics 365 -tuotteissa. |
| **Onko toinen ominaisuus korvannut?**   | Asiakkaiden kannattaa siirtyä Microsoft Edgeen.|
| **Tuotealueet, joihin vaikutetaan**         | Kaikki Dynamics 365 -tuotteet |
| **Käytön asetukset**              | Kaikki|
| **Tila**                         | Vanhentunut. Internet Explorer 11:tä ei tueta elokuun 2021 jälkeen.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Commercen version 10.0.11 poistetut tai vanhentuneet ominaisuudet
### <a name="data-action-hooks"></a>Tietotoiminnon koukut
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tietotoiminnon koukkutoiminto on vanhentunut suorituskykyongelmien vuoksi. |
| **Onko toinen ominaisuus korvannut?**   | Liiketoimintalogiikkaa kannattaa muokata tietotoimintokerroksessa [tietotoiminnon ohitusten](../e-commerce-extensibility/data-action-overrides.md) avulla.|
| **Tuotealueet, joihin vaikutetaan**         | Sähköisen kaupankäynnin laajennettavuuden tietotoiminnot |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: versiosta 10.0.11 alkaen |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Visual Studio 2015:n Retail SDK -tuki, msbuild 14.0 ja Retail SDK\Viitekirjastot ja työkalut
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Visual Studio 2015:n Retail SDK -tuki on vanhentunut, ja se on päivitetty tukemaan versiota VS 2017, msbuild 15.0 sekä kaikki viitekirjastot ja kaupankäynnin välityspalvelimen luontityökalut RetailSDK\References-kansiossa siirrettiin NuGet-paketteihin yksinkertaistamaan laajennusmallia ja SDK-päivitysprosessia.|
| **Onko toinen ominaisuus korvannut?**   | Järjestelmä kannattaa päivittää kohdan [Retail SDK:n siirtäminen Visual Studio 2015:sta Visual Studio 2017:ään](../dev-itpro/retail-sdk/migrate-sdk.md) ohjeiden mukaisesti. |
| **Tuotealueet, joihin vaikutetaan**         | Retail SDK -laajennukset |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: versiosta 10.0.11 alkaen |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Retail Server -laajennuksessa käytössä IEdmModelExtender ja CommerceController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Retail Server -laajennus, jossa on käytössä IEdmModelExtender ja CommerceController, on vanhentunut, jotta yksinkertaistettu laajennusmalli on mahdollinen. Uudessa toteutuksessa on vain ohjainluokka ilman ylimääräistä IEdmModelExtender-luokan toteutusta. Tällä tavoin vältetään myös riippuvuus tietystä OData-versiosta (jos OData-version päivitetään, laajennukset voivat vaurioitua). |
| **Onko toinen ominaisuus korvannut?**   |  IController-luokan laajennusmallia kannattaa käyttää tuomalla NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) -paketti. |
| **Tuotealueet, joihin vaikutetaan**         | Retail Serverin laajennukset |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: versiosta 10.0.11 alkaen |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Laiteasemalaajennus IHardwareStationControllerin avulla
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | IHardwareStationControlleria käyttävä laiteasemalaajennus on vanhentunut, jotta yksinkertaistettu laajennusmalli on mahdollinen. Uudessa toteutuksessa on vain IController-luokka ilman lisäluokkien toteutuksia, jolloin ei myöskään synny riippuvuutta peruslaiteasemakirjastoista, kun aiemmin laajennuksen oli viitattava useisiin kirjastoihin.) |
| **Onko toinen ominaisuus korvannut?**   | IController-luokan laajennusmallia kannattaa käyttää tuomalla NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) -paketti. |
| **Tuotealueet, joihin vaikutetaan**         | Laiteasemalaajennukset |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: versiosta 10.0.11 alkaen |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Commercen version 10.0.10 poistetut tai vanhentuneet ominaisuudet
### <a name="pos-operation-803---picking-and-receiving"></a>Myyntipistetoiminto 803 - Keräys ja vastaanotto
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Keräilyn ja vastaanoton toimintoja ollaan poistamassa, koska uusi uudelleensuunnittelu on käytössä. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Se korvataan kahdella uudella myyntipistetoiminnolla: saapuva työvaihe (804) ja lähtevä työvaihe (805).|
| **Tuotealueet, joihin vaikutetaan**         | Myyntipiste (POS) -sovellus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: kun kyseessä on julkaisuversio 10.0.10, keräily- ja vastaanottotoiminto ei enää vastaanota uusia ominaisuuspäivityksiä. Vain kriittiset ohjelmakorjaukset tehdään tämän toiminnon yhteydessä tulevissa versioissa. Kaikkia asiakkaita kannustetaan siirtymään uusiin [saapuviin työvaiheisiin](../pos-inbound-inventory-operation.md) ja [lähteviin toimintoihin](../pos-outbound-inventory-operation.md), jotka ovat jatkossakin osa pitkän aikavälin tuotesuunnitelmaa. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Commercen version 10.0.7 poistetut tai vanhentuneet ominaisuudet
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities- ja GetAvailableInventoryNearby ohjelmointirajapintaliittymät
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Uudet optimoidut ohjelmointirajapinnat on luotu korvaamaan GetProductAvailabilities- ja GetAvailableInventoryNearby-ohjelmointirajapinnat. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä: sen tilalle tulee GetEstimatedAvailabilty ja GetEstimatedProductWarehouseAvailability -ohjelmointirajapinnat. |
| **Tuotealueet, joihin vaikutetaan**         | e-Commerce-sovellus-SDK |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Julkaisuversiosta 10.0.7 alkaen kohteille GetProductAvailabilities ja GetAvailableInventoryNearby ei tehdä enää teknisiä investointeja. Organisaatiot, jotka käyttävät näitä ohjelmointirajapintaliittymiä verkkokaupan käyttöönotoissa, on muunnettava uuteen GetEstimatedAvailabilty- ja GetEstimatedProductWarehouseAvailability-ohjelmointirajapintaliittymiin ja otettava käyttöön [Optimoitu tuotteen saatavuuden laskentaominaisuus](../calculated-inventory-retail-channels.md).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset
Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

