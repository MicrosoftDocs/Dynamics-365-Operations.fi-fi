---
title: Poistetut tai vanhentuneet Platform-ominaisuudet
description: Tässä artikkelissa käsitellään toimintoja, jotka on poistettu tai joiden poistoa suunnitellaan talous- ja toimintosovellusten ympäristöpäivityksissä.
author: sericks007
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 6283e07b87dc169d3cbaa71a371839ab9b2d6150
ms.sourcegitcommit: ee13b854cbd52a3aa33e2449a296aed775862594
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/21/2022
ms.locfileid: "9799033"
---
# <a name="removed-or-deprecated-platform-features"></a>Poistetut tai vanhentuneet Platform-ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään toimintoja, jotka on poistettu tai joiden poistoa suunnitellaan talous- ja toimintosovellusten ympäristöpäivityksissä.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi. 

Seuraavissa raporteissa on lisätietoja talous- ja toimintosovellusten objekteista: [Tekniset viitetiedot](/dynamics/s-e/global/axtechrefrep_61). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin talous- ja toimintosovellusten versiossa.

## <a name="feature-deprecation-effective-august-2022"></a>Elokuussa 2022 poistettavat ominaisuudet

### <a name="lifecycle-services-lcs-features-deprecated-in-august-2022"></a>Lifecycle Servicesin (LCS) elokuussa 2022 vanhentuneet ominaisuudet

Seuraavat LCS-ominaisuudet on poistettu käytöstä osana [One Dynamics One Platform](/dynamics365-release-plan/2022wave2/finance-operations/finance-operations-crossapp-capabilities/one-dynamics-one-platform) -alustan kehitystä.

| Toiminnon nimi | Käytetäänkö AX 2012:n kanssa? | Käytetäänkö talous- ja toimintosovellusten kanssa? | Onko toinen ominaisuus korvannut? |
|--------------|--------------------|----------------------------------------|------------------------------|
| Ilmoitukset | Kyllä | Kyllä | Kyllä: Ilmoituksille on bannerit yksittäisillä projekti- ja ympäristösivuilla. |
| Määritystenhallinta | Kyllä | En | En |
| Kaatumisvedosanalyysi | Kyllä | En | En |
| Palaute ja virheet | Kyllä | Kyllä | En |
| Ylläpitosopimukseni | Kyllä | Kyllä | En |
| Office 365 | Kyllä | Kyllä | Kyllä: Azure Active Directory- tai Microsoft-hallintaportaali. |
| Vaikutusanalyysi | En | Kyllä | En |
| Taloudellisten kokonaisvaikutusten arviointityökalu | En | Kyllä | En |
| Palvelupyynnöt | En | Kyllä | Kyllä: [Itsepalvelukäyttöönotot](../deployment/infrastructure-stack.md) |
| SharePoint -integrointi | Kyllä | Kyllä | En |
| Määritysten ja tietojen hallinta | En | Kyllä | En |
| Prosessitietopaketit | En | Kyllä | Kyllä: [Tietojen tuonti- ja vientiympäristö (DIXF)](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job) |
| Ympäristön päivitys | En | Kyllä | Kyllä: [One Version](../lifecycle-services/oneversion-overview.md) -palvelupäivitykset ovat käytettävissä. |
| Infrastruktuurin arviointityökalu | Kyllä | En | En |
| Käyttöoikeuksien määrän arviointi | Kyllä | En | En |
| Käytön määritys | Kyllä | En | En |
| Mukautusten analyysi | Kyllä | En | En |
| Järjestelmän diagnostiikka | Kyllä | Kyllä | En |
| Liiketoimintaprosessien mallintajan Visio-hallinta | Kyllä | Kyllä | En |
| AX 2012 -pilviympäristöjen hallinta | Kyllä | En | En |
| RDFE Azure -yhdistimet | Kyllä | Kyllä | En |
| AX 2012 -versiot | Kyllä | En | En |
| LCS-tallennustilaan tallennetut työnimikkeet | Kyllä | Kyllä | En |
| Hotfix-pyynnöt | Kyllä | Kyllä | En |


### <a name="transport-layer-security-tls-rsa-cipher-suites"></a>Transport Layer Security (TLS) RSA -salausohjelmistot

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Poistamme seuraavat salausohjelmistot noudattaaksemme nykyisiä tietoturvaprotokolliamme.<br><br>TLS_RSA_WITH_AES_256_GCM_SHA384<br>TLS_RSA_WITH_AES_128_GCM_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA256<br>TLS_RSA_WITH_AES_128_CBC_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA<br>TLS_RSA_WITH_AES_256_CBC_SHA  |
| **Onko toinen ominaisuus korvannut?**   | Asiakkaat voivat käyttää vain  [standardisalausohjelmistoja](/power-platform/admin/server-cipher-tls-requirements) tammikuusta 2023 alkaen. Tämä muutos vaikuttaa asiakkaisiisi ja palvelimiisi, jotka kommunikoivat meidän palvelimemme kanssa. Se voi vaikuttaa esimerkiksi kolmansien osapuolten integraatioihin, jotka eivät noudata standardisalausohjelmistojemme vaatimuksia. |
| **Tuotealueet, joihin vaikutetaan**         | Taloushallinnon ja toimintojen sovellukset |
| **Käytön asetukset**              | Pilvikäyttöönotot |
| **Tila**                         | Vanhentunut. Asiakkaiden täytyy päivittää palvelimensa ennen tammikuuta 2023. Lisätietoja TLS-salausohjelmistojärjestyksen määrittämisestä on kohdassa  [Transport Layer Securityn (TLS) hallinta](/windows-server/security/tls/manage-tls).  |


## <a name="feature-deprecation-effective-june-2022"></a>Kesäkuussa 2022 poistettavat ominaisuudet

### <a name="finance-and-operations-dynamics-365-mobile-application-and-mobile-platform"></a>Talous- ja toimintosovellusten (Dynamics 365) mobiilisovellus ja mobiiliympäristö 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Talous- ja toimintosovellusten (Dynamics 365) mobiilisovellus ja mobiiliympäristö poistetaan yhteen mobiiliympäristöön, Power Appsiin, konsolidointia varten. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, talous- ja toimintosovellusten tietojen mobiilikokemukset voidaan muodostaa Power Platform -integraation avulla. Katso lisätietoja [blogikirjoituksesta](https://cloudblogs.microsoft.com/dynamics365/it/2022/06/03/finance-and-operations-dynamics-365-mobile-app-to-be-deprecated/) ja [Mobiilikokemusten kehittäminen](../power-platform/build-mobile-experiences.md) -kohdasta. |
| **Tuotealueet, joihin vaikutetaan**         | Taloushallinnon ja toimintojen sovellukset |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut. Tuen päättymisajankohdaksi on suunniteltu lokakuuta 2024. |


## <a name="platform-updates-for-version-10029-of-finance-and-operations-apps"></a>Talous- ja toimintosovellusten version 10.0.29 ympäristöpäivitykset

### <a name="panorama-tab-style"></a>Panoraamavälilehtityyli

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Vaakasuunnassa vieritettävät sivut perustuvat vanhentuneisiin asettelumalleihin, joilla tiedetään olevan käytettävyys- ja helppokäyttöisyysongelmia.  |
| **Onko toinen ominaisuus korvannut?**   | Ei, mutta muut välilehtityylit ovat silti käytettävissä. |
| **Tuotealueet, joihin vaikutetaan**         | WWW-asiakasohjelma |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut. |


## <a name="feature-deprecation-effective-april-2022"></a>Huhtikuussa 2022 poistettavat ominaisuudet

### <a name="xml-url-resolution-in-data-management"></a>XML:n URL-selvitys tietojenhallinnassa 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Poistamme XML URL -ratkaisun tuen, koska se on määritetty mahdolliseksi tietoturvariskiksi. Tämä tarkoittaa, että XML-tiedostoihin liittyviä ulkoisia resursseja ei enää ratkaista.  |
| **Onko toinen ominaisuus korvannut?**   | Ei |
| **Tuotealueet, joihin vaikutetaan**         | Taloushallinnon ja toimintojen sovellukset |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut. |

## <a name="feature-deprecation-effective-march-14-2022"></a>14.3.2022 poistettavat ominaisuudet

### <a name="xslt-scripting-in-data-management"></a>XSLT-komentosarjat tiedonhallinnassa

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | XSLT-komentotiedoston tuki tietojenhallinnassa on vanhentunut, jotta talous- ja toimintosovellusten tietoturvaa ja tietosuojaa voidaan parantaa.  |
| **Onko toinen ominaisuus korvannut?**   | Ei Asiakkaiden ja ISVs:n tulisi harkita X++-kielisten ratkaisujensa ostamista XSLT-komentotiedoston paikalla. |
| **Tuotealueet, joihin vaikutetaan**         | Taloushallinnon ja toimintojen sovellukset |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut <br><br>**Poikkeus:** Asiakkaat, jotka käyttävät tällä hetkellä XLST-komentosarjoja. He voivat yhä käyttää sitä, kunnes ne päivittyvät versioon 10.0.30 tai sitä myöhemmäksi. Aiemmissa versioissa poikkeus vanhenee 31.1.2023. Tätä poikkeusta lukuun ottamatta asiakkaat ovat saaneet ilmoituksen Microsoft 365 järjestelmänvalvojan keskuksessa käytettävissä olevassa sanomakeskuksessa. |

## <a name="feature-removal-effective-october-2021"></a>Ominaisuuden poistaminen tulee voimaan lokakuussa 2021

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azuren SQL-raportit Lifecycle Servicesissä (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Kaikki toiminnot ja seuranta suoritetaan sisäisesti ympäristön kautta ja automaation avulla. Tämä ei edellytä manuaalista keskeytystä.|
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Käytössä on nyt automaattinen järjestelmä, joiden vuoksi nämä ominaisuudet ovat vanhentuneet. |
| **Tuotealueet, joihin vaikutetaan**         | SQL-raportit: Nykyinen DTU, Nykyisen DTU:n tiedot, Nouda lukituksen tiedot, Nykyisen suunnitteluoppaan luettelo, Nouda kyselytunnusten luettelo, Nouda tietyn suunnitelmatunnuksen SQL-kyselysuunnitelma, Nouda kyselysuunnitelmat ja suoritustila, Nouda rajoitusmääritys, Nouda odotustilastot, Luetteloi kalleimmat kyselyt |
| **Käytön asetukset**              | Pilvikäyttöönotto: vaikuttaa Microsoftin hallitsemiin tuotantoympäristöihin ja tason 2–5 eristysympäristöihin. |
| **Tila**                         | Poistettu |

### <a name="azure-sql-actions-in-lcs"></a>Azure SQL -toiminnot LCS:ssä

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Osa SQL-toiminnoista poistetaan käytöstä LCS:ssä. Kaikki toiminnot ja seuranta suoritetaan sisäisesti ympäristön kautta ja automaation avulla. Tämä ei edellytä manuaalista keskeytystä. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Käytössä on nyt automaattinen järjestelmä, joiden vuoksi nämä ominaisuudet ovat vanhentuneet. |
| **Tuotealueet, joihin vaikutetaan**         | SQL-toiminnot: Luo suunnitelmaopas suunnitelmatunnuksen pakottamiselle, Luo suunnitelmaopas taulukkovinkkien lisäämiselle, Poista suunnitteluopas, Poista käytöstä / ota käyttöön sivulukitukset ja lukitusten eskalointi, Päivitä taulukon tilastot, Muodosta indeksi uudelleen, Luo indeksi |
| **Käytön asetukset**              | Pilvikäyttöönotto: vaikuttaa Microsoftin hallitsemiin tuotantoympäristöihin ja tason 2–5 eristysympäristöihin. |
| **Tila**                         | Poistettu |


## <a name="feature-deprecation-effective-october-2021"></a>Lokakuussa 2021 poistettavat ominaisuudet

### <a name="show-related-document-attachments-feature"></a>Näytä asiaan liittyvät asiakirjaliitteet -ominaisuus

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Toiminto palautti odottamattomia tuloksia. |
| **Onko toinen ominaisuus korvannut?**   | Et voi. Mahdolliset tätä toimintoa koskevat jatkosuunnitelmat ilmoitetaan vakiomuotoisen julkaisuaallosta ilmoittamisen prosessissa. |
| **Tuotealueet, joihin vaikutetaan**         | Verkkoasiakasohjelma – Asiakirjan liittämiskokemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut  |

## <a name="platform-updates-for-version-10023-of-finance-and-operations-apps"></a>Talous- ja toimintosovellusten version 10.0.23 ympäristöpäivitykset

### <a name="ondbsynchronize-event"></a>OnDBSynchronize-tapahtuma

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tämän tapahtuman suorittamiselle ei ole ohjausobjektia. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, siirrä olemassa olevat **OnDBSynchronize**-tapahtuman tilaamat menetelmät SysSetup-laajennusluokkaan. |
| **Tuotealueet, joihin vaikutetaan**         | Tietokannan synkronointi |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut. Poisto on suunniteltu lokakuulle 2022. |


### <a name="systemnotificationsmanageraddnotification-api"></a>SystemNotificationsManager.AddNotification-ohjelmointirajapinta

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Microsoft edellyttää lisäparametreja ilmoitusten lisäämisessä. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, **SystemNotificationsManager.AddSystemNotification()**-ohjelmointirajapinta. Tämä ohjelmointirajapinta edellyttää, että määrität luotujen ilmoitusten arvot ExpirationDateTime ja RuleID nimenomaisesti. |
| **Tuotealueet, joihin vaikutetaan**         | WWW-asiakasohjelma |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut. Poisto on suunniteltu huhtikuulle 2023. |

## <a name="platform-updates-for-version-10021-of-finance-and-operations-apps"></a>Talous- ja toimintosovellusten version 10.0.21 ympäristöpäivitykset

### <a name="skype-for-business-online-support"></a>Skype for Business Online -tuki

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Skype for Business Online on poistettu käytöstä. Lisätietoja on kohdassa [Skype for Business Online -palvelu on poistettu käytöstä](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/the-skype-for-business-online-service-has-retired/ba-p/2596601). |
| **Onko toinen ominaisuus korvannut?**   | Ei tällä hetkellä, mutta Teamsin tavoitettavuuden lisäämistä myöhemmin on harkittu.|
| **Tuotealueet, joihin vaikutetaan**         | WWW-asiakasohjelma |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut. **Skype käytössä** -asetus on poistettu käytöstä versiosta 10.0.21 alkaen. Tämän asetuksen poistaminen on suunniteltu huhtikuuhun 2022. Ominaisuus ei kuitenkaan toimi, kun Skype-ryhmä sammuttaa palvelun. |
 
## <a name="feature-deprecation-effective-august-2021"></a>Elokuussa 2021 poistettavat ominaisuudet

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azuren SQL-raportit Lifecycle Servicesissä (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Kaikki toiminnot ja seuranta suoritetaan sisäisesti ympäristön kautta ja automaation avulla. Tämä ei edellytä manuaalista keskeytystä.|
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Käytössä on nyt automaattinen järjestelmä, joiden vuoksi nämä ominaisuudet ovat vanhentuneet. |
| **Tuotealueet, joihin vaikutetaan**         | SQL-raportit: Nykyinen DTU, Nykyisen DTU:n tiedot, Nouda lukituksen tiedot, Nykyisen suunnitteluoppaan luettelo, Nouda kyselytunnusten luettelo, Nouda tietyn suunnitelmatunnuksen SQL-kyselysuunnitelma, Nouda kyselysuunnitelmat ja suoritustila, Nouda rajoitusmääritys, Nouda odotustilastot, Luetteloi kalleimmat kyselyt |
| **Käytön asetukset**              | Pilvikäyttöönotto: vaikuttaa Microsoftin hallitsemiin tuotantoympäristöihin ja tason 2–5 eristysympäristöihin. |
| **Tila**                         | Vanhentunut: suunniteltu poistopäivä lokakuussa 2021. |

### <a name="azure-sql-actions-in-lcs"></a>Azure SQL -toiminnot LCS:ssä

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Osa SQL-toiminnoista poistetaan käytöstä LCS:ssä. Kaikki toiminnot ja seuranta suoritetaan sisäisesti ympäristön kautta ja automaation avulla. Tämä ei edellytä manuaalista keskeytystä. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Käytössä on nyt automaattinen järjestelmä, joiden vuoksi nämä ominaisuudet ovat vanhentuneet. |
| **Tuotealueet, joihin vaikutetaan**         | SQL-toiminnot: Luo suunnitelmaopas suunnitelmatunnuksen pakottamiselle, Luo suunnitelmaopas taulukkovinkkien lisäämiselle, Poista suunnitteluopas, Poista käytöstä / ota käyttöön sivulukitukset ja lukitusten eskalointi, Päivitä taulukon tilastot, Muodosta indeksi uudelleen, Luo indeksi |
| **Käytön asetukset**              | Pilvikäyttöönotto: vaikuttaa Microsoftin hallitsemiin tuotantoympäristöihin ja tason 2–5 eristysympäristöihin. |
| **Tila**                         | Vanhentunut: suunniteltu poistopäivä lokakuussa 2021. |

## <a name="feature-deprecation-effective-may-2021"></a>Toukokuussa 2021 poistettavat ominaisuudet

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) -globalisoinnin portaali

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Globalisoinnin portaali on poistettu käytöstä LCS:ssä, koska muut LCS-pohjaiset palvelut ovat korvanneet tämän ominaisuuden. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, tämän ominaisuuden korvaa LCS:n [ongelmanhaku](../lifecycle-services/issue-search-lcs.md) ja [Dynamics regulatory alert submission service](../lcs-solutions/submit-localization-alerts.md). |
| **Tuotealueet, joihin vaikutetaan**         | LCS:n globalisoinnin portaali|
| **Käytön asetukset**              | Pilvikäyttöönotto |
| **Tila**                         | Vanhentunut: suunniteltu poistopäivä toukokuussa 2022. |


## <a name="feature-removed-effective-january-28-2021"></a>Toiminto poistettiin 28. tammikuuta 2021

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Erätyö SQL-indeksin eheyttämisen käsittelemistä varten

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tämä toiminto on poistettu, jotta asiakkaiden indeksinhallinnan toiminnan, valvonnan ja ylläpidon yleiskustannuksia voidaan pienentää. |
| **Onko toinen ominaisuus korvannut?**   | Jatkossa Microsoftin palvelut suorittavat indeksin ylläpidon. Sitä tehdään jatkuvasti ilman, että se vaikuttaa käyttäjän työkuormiin. |
| **Tuotealueet, joihin vaikutetaan**         | Taloushallinnon ja toimintojen sovellukset|
| **Käytön asetukset**              | Pilvikäyttöönotto – vaikuttaa Microsoftin hallitsemiin tuotantoympäristöihin ja tason 2–5 eristysympäristöihin. |
| **Tila**                         | Tämä toiminto on poistettu. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Talous- ja toimintosovellusten version 10.0.17 ympäristöpäivitykset


### <a name="visual-studio-2015"></a>Visual Studio2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Uusimpien Visual Studio -versioiden tueksi on tehtävä joitakin muutoksia Visual Studion X + +-laajennuksiin. Nämä muutokset eivät ole yhteensopivia Visual Studio 2015:n kanssa. |
| **Onko toinen ominaisuus korvannut?**   | Visual Studio 2017 korvaa Visual Studio 2015:n käyttöönotettuna ja vaaditussa muodossa. |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -sovelluksen kehitystyökalut |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Päivityksen myötä edelliset X++-työkalut poistetaan Visual Studio 2015:stä eivätkä päivitetyt työkalut asennu Visual Studio 2015:een. Tällä ei ole vaikutusta isännöityihin koontiversioihin. Koontinäennäiskoneissa koontijakso (koontimääritelmä) on päivitettävä manuaalisesti muuttamaan riippuvuus MSBuild 14.0:sta (Visual Studio 2015) to MSBuild 15.0:aan (Visual Studio 2017) kohdassa [Vanhan jakson päivittäminen Azure-jaksoissa](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Käyttäjän avatar 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Siirtymispalkin oikealla puolella näkyvä käyttäjän avatar noudettiin käyttämällä Dynamics 365:n otsikon ohjausobjektin ohjelmointirajapintaa, joka on vanhentunut. |
| **Onko toinen ominaisuus korvannut?**   | Käyttäjät näkevät sen sijaan nimikirjaimessa siirtymispalkissa olevassa ympyrässä. Tämä on sama visualisointi, joita käytetään tällä hetkellä kehittämiskoneissa. |
| **Tuotealueet, joihin vaikutetaan**         | WWW-asiakasohjelma |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Poistettu versiosta 10.0.17 alkaen |

### <a name="enterprise-portal-ep-deprecation"></a>Yritysportaalin (EP) poistaminen  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Dynamics AX 2012 -yritysportaaliin (EP) liitetyt metatietojen artefaktit ovat vanhentuneet, sillä EP:tä ei koskaan tuettu talous- ja toimintosovelluksissa. |
| **Onko toinen ominaisuus korvannut?**   | En |
| **Tuotealueet, joihin vaikutetaan**         | WWW-asiakasohjelma |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Kaikki EP-koodit on ajoitettu poistettavaksi lokakuun 2021 julkaisussa. |

## <a name="deprecation-effective-december-2020"></a>Joulukuussa 2020 poistetut ominaisuudet

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11:n Dynamics 365 -tuki on vanhentunut

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Joulukuusta 2020 alkaen kaikkien Dynamics 365 -tuotteiden ja Dynamics Lifecycle Services (LCS) -palvelun Microsoft Internet Explorer 11 -tuki vanhenee eikä Internet Explorer 11:tä tueta elokuun 2021 jälkeen.<br><br>Tämä vaikuttaa sellaisiin Dynamics 365 -tuotteita tai LCS:ää käyttäviin asiakkaisiin, jotka on suunniteltu käytettäviksi Internet Explorer 11 -liittymässä. Elokuun 2021 jälkeen Internet Explorer 11:tä ei tueta kyseisissä Dynamics 365 -tuotteissa tai LCS:ssä. |
| **Onko toinen ominaisuus korvannut?**   | Asiakkaiden kannattaa siirtyä Microsoft Edgeen.|
| **Tuotealueet, joihin vaikutetaan**         | Kaikki Dynamics 365 -tuotteet ja LCS |
| **Käytön asetukset**              | Kaikki|
| **Tila**                         | Vanhentunut: Internet Explorer 11:tä ei tueta elokuun 2021 jälkeen.|

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Talous- ja toimintosovellusten version 10.0.15 ympäristöpäivitykset

### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio -apuohjelma metatietojen hotfix-korjausten käyttämiseen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Metatietojen hotfix-korjauksia ei enää tueta [One Version](../../fin-ops/get-started/one-version.md) -palvelupäivityksissä, jotka otettiin käyttöön heinäkuussa 2018 versiossa 8.1. |
| **Onko toinen ominaisuus korvannut?**   | Yksittäiset metatietojen hotfix-korjaukset eivät ole saatavana tuettuihin versioihin. Sen sijaan käytetään kumulatiivisia laatupäivityksiä. |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -apuohjelmat |
| **Käytön asetukset**              | Kehityksen virtuaalikoneet |
| **Tila**                         | Versiossa 10.0.15 myötä apuohjelma ei enää sisälly Visual Studio Toolsiin. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Talous- ja toimintosovellusten version 10.0.14 ympäristöpäivitykset

### <a name="online-users-page"></a>Online-käyttäjien sivu 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tämä on vanha sivu, joka on luotu aiemmalle asiakas-/palvelinarkkitehtuurille. Tällä sivulla olevat tiedot eivät aina ole oikein, mikä voi olla hämmentävää ja harhaanjohtavaa. |
| **Onko toinen ominaisuus korvannut?**   | Julkaisemme uuden sivun tulevassa päivityksessä.|
| **Tuotealueet, joihin vaikutetaan**         | Järjestelmän hallinta |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Tämä lomake poistetaan lokakuuhun 2021 mennessä.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Talous- ja toimintosovellusten version 10.0.13 ympäristöpäivitykset


### <a name="custom-code-defined-in-ssrs-report-properties"></a>SSRS-raportin ominaisuuksissa määritetty mukautettu koodi 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Yleensä mukautettu koodi tarjoaa rajoitettuja etuja samaan aikaan ja edellyttää huomattavaa resursointi- ja käsittelytukea. Mukautettua koodia käytetään ensisijaisesti raportin laatijoiden kutsussa julkisiin menetelmiin mukautetusta koodikokoonpanosta. Pilvipohjainen palvelu ei kuitenkaan tue SSRS-raporttien mukautettujen kokoonpanojen viittauksia. |
| **Onko toinen ominaisuus korvannut?**   | Raporttien laatijat voivat halutessaan jatkaa julkisten .NET-API-liittymien vertailemista mistä tahansa tekstiruudun lausekkeesta. Lisätietoja on kohdassa [Koodin lisääminen raporttiin (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs).  |
| **Tuotealueet, joihin vaikutetaan**         | RDL:ssä määritetyn sovellusraporttimallin alijoukko, joka sisältää mukautettua koodia. |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Versiolla 10.0.13, kääntäjä alkaa antaa varoituksen tapauksissa, joissa mukautettua koodia havaitaan SSRS-raportti määritelmässä. Voit korjata ongelman avaamalla raportin rakennemäärityksen ja poistamalla kaikki mukautetut koodiartefaktit. Tämä varoitus korvataan kääntäjän virheellä tulevassa päivityksessä.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Kolmen jQuery-osakirjaston päivitys 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Kolmea jQuery-osakirjastoa päivitetään suojauskorjausten vuoksi ja valuutan ylläpitoa varten.   
| **Onko toinen ominaisuus korvannut?**   | Kyse on seuraavista kirjastoista: jQuery (versioon 3.5.0 versiosta 2.1.4), jQuery UI (versioon 1.12.1 versiosta 1.11.4), jQuery qTip (versioon 3.0.3 versiosta 2.2.1). jQuerylla on verkossa ohjeet siirtoa varten.  |
| **Tuotealueet, joihin vaikutetaan**         | Laajennettavat ohjausobjektit, etenkin vanhentuneita tai poistettuja ohjelmointirajapintoja käyttävä mukautettu JavaScript-koodi |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Versiossa 10.0.13 / Platform update 37:ssä asiakkailla on mahdollisuus siirtyä uusimpiin kirjastoihin ottamalla Kolmen jQuery-osakirjaston päivitys -toiminto käyttöön. Uusiin kirjastoihin siirtyminen tulee pakolliseksi huhtikuun 2021 -version myötä, jotta kyseisten ohjelmointirajapintojen siirtoon jää aikaa.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Olemassa oleva ruudukon ohjausobjekti / forceLegacyGrid()-ohjelmistorajapinta

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Uusi ruudukon ohjausobjekti korvaa aiemmin luodun ruudukon ohjausobjektin. |
| **Onko toinen ominaisuus korvannut?**   | [Uusi ruudukon ohjausobjekti](../..//fin-ops/get-started/grid-capabilities.md) |
| **Tuotealueet, joihin vaikutetaan**         | WWW-asiakasohjelma |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Versiossa 10.0.13 uusi ruudukon ohjausobjekti on yleisesti saatavilla. Asiakkaat voivat halutessaan ottaa ominaisuuden käyttöön. Uusi ruudukonhallinta tulee oletusarvoisesti käyttöön lokakuun 2021 julkaisun myötä, ja nykyisen suunnitelman mukaan siitä tulee pakollinen huhtikuussa 2022. Kun uusi ruudukon ohjausobjekti on pakollinen, **forceLegacyGrid()**-ohjelmointirajapintaa ei enää käytetä. |

### <a name="personalization-without-saved-views"></a>Mukauttaminen ilman tallennettuja näkymiä 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Mukautuksen alijärjestelmä on uudistettu. Se sisältää tallennettujen näkymien ominaisuuden, joten suorituskyky on parempi ja se sisältää uusia ominaisuuksia. |
| **Onko toinen ominaisuus korvannut?**   | Tallennetut näkymät |
| **Tuotealueet, joihin vaikutetaan**         | WWW-asiakasohjelma |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Versiossa 10.0.13 / Platform update 37 tallennettujen näkymien ominaisuus on yleisesti käytettävissä. Asiakkaat voivat halutessaan ottaa tämän ominaisuuden käyttöön. Tallennettujen näkymien ominaisuus on pakollinen lokakuun 2021 julkaisussa. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Talous- ja toimintosovellusten version 10.0.12 ympäristöpäivitykset

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Ruudukko- tai ryhmäohjausobjektin lomakelaajennukset, jotka sisältävät virheellisiä kenttäviittauksia

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Ruudukko- tai ryhmäohjausobjektien tietoryhmäominaisuuden avulla voidaan automaattisesti näyttää kaikki kenttäryhmän kentät. Laajennuksessa lisätty ruudukko tai ryhmäohjausobjekti voi sisältää kenttiä, joita ei ole enää määritetty kenttäryhmässä, tai kenttäryhmään määritettyjä kenttiä ei ehkä löydy. Tämä voi aiheuttaa epäjohdonmukaista käyttäytymistä suorituksen aikana. Talous- ja toimintosovellusten version 10.0.12 ympäristöpäivitykset luokittelevat nyt tämän ongelman kääntäjän *varoitukseksi*. Voit korjata tämän ongelman avaamalla lomakelaajennuksen ja tallentamalla sen.
| **Onko toinen ominaisuus korvannut?**   | Tämä kääntäjän varoitus korvataan kääntäjän virheellä tulevassa päivityksessä. |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -sovelluksen kehitystyökalut |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Kääntäjävaroitus otetaan käyttöön talous- ja toimintosovellusten version 10.0.12 ympäristöpäivityksissä. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Talous- ja toimintosovellusten version 10.0.11 ympäristöpäivitykset

### <a name="explicit-safe-lists-for-self-service-environments"></a>Selkeä turvallisten osoitteiden luettelo itsepalveluympäristöissä

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | IP-osoitteiden turvallisiin osoitteisiin siirtymisprosessi on muuttunut. Itsepalvelu ei enää tue turvallisia IP-osoitteita. |
| **Onko toinen ominaisuus korvannut?**   | Lisätietoja on kohdassa [Azure Active Directoryn ehdollisen käytön konfigurointi](/appcenter/general/configuring-aad-conditional-access).|
| **Tuotealueet, joihin vaikutetaan**         | Suojaus |
| **Käytön asetukset**              | Pilvi |
| **Tila**                         | Vanhentunut: Tämä ominaisuus on täysin vanhentunut itsepalvelukäyttöönotoissa. |

### <a name="visual-studio-2015"></a>Visual Studio 2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Uusimpien Visual Studio -versioiden tueksi on tehtävä joitakin muutoksia Visual Studion X + +-laajennuksiin. Nämä muutokset eivät ole yhteensopivia Visual Studio 2015:n kanssa. |
| **Onko toinen ominaisuus korvannut?**   | Visual Studio 2017 korvaa Visual Studio 2015:n käyttöönotettuna ja vaaditussa muodossa. |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -sovelluksen kehitystyökalut |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Versio 10.0.13 (Alustapäivitys 37) tai uudemmassa versiossa käyttöön otetut virtuaalikoneet sisältävät Visual Studio 2017:n. Versio 10.0.16 (Alustapäivitys 40) on viimeinen julkaisu, joka tukee Visual Studio 2015:ta. Virtuaalikoneita, joissa on vain Visual Studio 2015, ei voi päivittää versioon 10.0.17 (Alustapäivitys 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Virheellisiä kenttäviitteitä sisältävät kenttäryhmät

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Taulun metatietomääritysten kenttäryhmät voivat sisältää kenttäviittauksia, jotka eivät ole kelvollisia. Jos nämä kenttäryhmät otetaan käyttöön, ne voivat aiheuttaa suorituksenaikaisia virheitä talousraportoinnissa ja Microsoft SQL Server Reporting Servicesissa (SSRS). Platform Update 23 sisälsi kääntäjän *varoituksen*, joka mahdollisti tämän metatieto-ongelman käsittelemisen. Talous- ja toimintosovellusten version 10.0.11 ympäristöpäivitykset luokittelevat tämän ongelman kääntäjän *virheeksi*.<p>Korjaa tämä ongelma seuraavien ohjeiden mukaisesti.</p><ol><li>Poista virheellinen kenttäviite taulun kenttäryhmämääritelmästä.</li><li>Käännä uudelleen.</li><li>Varmista, että mahdolliset virheet on korjattu.</li></ol> |
| **Onko toinen ominaisuus korvannut?**   | Tämä kääntäjän virhe korvaa kääntäjän varoituksen pysyvästi.  |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -sovelluksen kehitystyökalut |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Kääntäjän varoitus on nyt kääntäjän virhe talous- ja toimintosovellusten version 10.0.11 ympäristöpäivityksissä. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>SHA1-hajautusalgoritmin avulla luodut ohjelmistotoimittajien lisenssit

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Riippumattoman ohjelmistotoimittajan käyttöoikeuksien luontiprosessi on muuttunut. Lisätietoja on kohdassa [Riippumaton ohjelmistotoimittajien (ISV) lisensointi](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Luo lisenssejä Windows PowerShellin avulla. |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -sovelluksen kehitystyökalut |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Ohjelmistotoimittajien käyttöoikeudet, jotka luotiin SHA1-hajautusalgoritmin avulla. Tämä algoritmi riippui MakeCert-apuohjelman avulla luoduista sertifikaateista, ja tämä apuohjelma on syrjäytetty.<br><br>Vanhentunut: SHA1 käyttösuojaus- tai hajautustarkoituksiin. SHA1 lakkaa toimimasta vuoden 2021 alussa. Siksi sitä ei pitäisi enää käyttää.<br><br>Poistettu: Transport Layer Securityn tuki (TLS) 1.0 ja TLS 1.1 saapuville tai lähteville pyynnöille. |

## <a name="platform-update-32"></a>Ympäristön update 32 -päivitys

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Työnkulun pyynnön muutoksen valintaikkuna ei enää sisällä käyttäjän valinnan avattavaa luetteloa

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tämä oli tietoturvaongelma, koska muutospyyntö voitiin lähettää väärälle käyttäjälle. Tämä oli myös käytettävyysongelma, koska se pakotti käyttäjän määrittämään, kuka työnkulun aloittaja on, ja manuaalisesti valitsemaan tämän.  |
| **Onko toinen ominaisuus korvannut?**   | Ei |
| **Tuotealueet, joihin vaikutetaan**         | Työnkulku |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Käyttäjän valinnan avattava luettelo poistettiin pyynnön muutoksen valintaikkunasta Platform update 32 -päivityksessä. Pyynnön muutospyynnöt lähetetään automaattisesti aloittajalle aiemmin määritetyllä tavalla. Lisätietoja tästä toiminnosta on kohdassa [Toiminnot työnkulun hyväksyntäprosesseissa](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Upotetut porautumiseen käytettäviä linkkejä ei enää tueta sivutetuissa asiakirjoissa, jotka pilvipohjainen palvelu hahmontaa 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Palvelun hahmontamat asiakirjoihin upotetut siirtymisen URL-osoitteet voivat sisältää luottamuksellista liiketoimintatietoa. Kaikkien upotettujen porautumislinkkien tuki asiakirjoissa poistetaan. Näin turvataan asiakastiedot jatkossa. Käyttäjät hyötyvät myös paremmasta suorituskyvystä samalla, kun asiakirjoja tuotetaan interaktiivisesti tämän muutoksen seurauksena.  |
| **Onko toinen ominaisuus korvannut?**   | Ei |
| **Tuotealueet, joihin vaikutetaan**         | Raportointi |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Tämä toiminto poistetaan käytöstä palvelusta.<br><br>Uusi asiakasohjelma tarjoaa useita vaihtoehtoja näkymien tuottamiseen. Se luo myös linkkejä automaattisesti sovelluksessa siirtymistä varten. Palvelun hahmontamia sivutettuja asiakirjoja suositellaan ulkoista viestintää varten sähköpostissa, arkistoinnissa ja vastaanottajien tulostuksissa. Asiakirjojen esikatselua suoraan selaimessa on parannettu. Näin voidaan käyttää paikallisia tulostimia suoraan. Lisätietoja on kohdassa [PDF-asiakirjojen esikatselu upotetussa katseluohjelmassa](../analytics/preview-pdf-documents.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset
Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../migration-upgrade/deprecated-features.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

