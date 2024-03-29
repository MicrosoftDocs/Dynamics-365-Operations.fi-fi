---
title: Talous- ja toimintosovellusten kaksoiskirjoitusongelmien vianmääritys
description: Tässä artikkelissa on vianmääritystietoja, joiden avulla voidaan korjata talous- ja toimintosovellusten kaksoiskirjoitusmoduulin ongelmia.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 5678cd38e48eb5226e36851679436d3b6c117cf9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289571"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Talous- ja toimintosovellusten kaksoiskirjoitusongelmien vianmääritys

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa on vianmääritystietoja kaksoiskirjoituksen integroinnista talous- ja toimintosovellusten sekä Dataversen välillä. Erityisesti se sisältää vianmääritystietoja, joiden avulla voidaan korjata talous- ja toimintosovellusten **Kaksoiskirjoitus**-moduulin ongelmia.

> [!IMPORTANT]
> Jotkin tämän artikkelin osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoft Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Kaksoiskirjoitusmoduulia ei voi ladata talous- ja toimintosovellukseen

Jos **Kaksoiskirjoitus**-sivua ei voi avata valitsemalla **Tietojen hallinta** -työtilassa **Kaksoiskirjoitus**-ruutu, tietojen integrointipalvelu ei todennäköisesti ole toiminnassa. Luo tukipyyntö, joka pyytää tietojen integrointipalvelun uudelleenkäynnistystä.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Virhe yritettäessä luoda uutta taulukon yhdistämismääritystä

**Tarvittavat tunnistetiedot ongelman korjaamiseksi:** Sama käyttäjä, joka määrittää kaksoiskirjoituksen.

Seuraava virhesanoma voi avautua, kun yrität määrittää uuden taulukon kaksoiskirjoittamista varten. Ainoa käyttäjä, joka voi luoda yhdistämismäärityksen, on käyttäjä, joka määrittää kaksoiskirjoituksen yhteyden.

*Vastauksen tilakoodi ei tarkoita onnistumista: 401 (Luvaton).*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Virhe avattaessa kaksoiskirjoituskäyttöliittymää

Näyttöön saattaa tulla seuraavan kaltainen virhesanoma, kun yrität käyttää **Tietojen hallinta** -työtilan kaksoiskirjoittamista:

*login.microsoftonline.com kieltäytyi muodostamasta yhteyttä.*

Jos haluat korjata ongelman, kirjaudu sisään käyttämällä InPrivate-ikkunaa Microsoft Edgessä, tuntemattoman käyttäjän ikkunaa Chromiumissa tai tuntemattoman käyttäjän ikkunaa Google Chromessa. Sinun on myös avattava kolmannen osapuolen evästeet tai poistettava niiden valinta.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Virhe yhdistettäessä ympäristöä kaksoiskirjoittamista tai uuden taulun yhdistämismääritystä varten

**Ongelman korjaamisen edellyttämä rooli:** Järjestelmänvalvoja sekä talous- ja toimintosovelluksessa että Dataversessä.

Saatat kohdata seuraavan virheen linkittäessäsi tai luodessasi karttoja:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

Tämä virhe voi ilmetä, jos sinulla ei ole riittäviä oikeuksia yhdistää kaksoiskirjoitukseen tai luoda karttoja. Tämä virhe voi ilmetä myös, jos Dataverse -ympäristö nollautuu ilman kaksoiskirjoituksen linkityksen poistamista. Kuka tahansa käyttäjä, jolla on järjestelmänvalvojan rooli sekä talous- ja toimintosovelluksissa että Dataversessä, voi linkittää ympäristöt. Vain kaksoiskirjoitusyhteyden asetusten luonut käyttäjä voi lisätä uusia taulujen yhdistämismäärityksiä. Asennuksen jälkeen kuka tahansa järjestelmänvalvoja, jolla on järjestelmänvalvojan rooli, voi valvoa tilaa ja muokata yhdistämismäärityksiä.

## <a name="error-when-you-stop-the-table-mapping"></a>Virhe yritettäessä pysäyttää taulun yhdistämismääritystä

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität pysäyttää taulujen yhdistämismääritystä:

*\[Kielletty\], \[{"status": 403, "lähde":"","sanoma":"Virhe tunnuksen vaihdossa: Käyttäjällä ei ole oikeutta käyttää yhteyttä dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Etäpalvelin palautti virheen: (403) kielletty.*

Tämä virhe ilmenee, kun linkitetty Dataverse -ympäristö ei ole käytettävissä.

Voit korjata ongelman luomalla pyynnön tietojen integrointitiimille. Liitä verkon jäljitys, jotta tietojen integrointiryhmä voi merkitä karttojen tilaksi **Ei käynnissä** taustalla.

## <a name="enable-parallel-processing-in-finance-and-operations-apps-to-improve-performance"></a>Rinnakkaiskäsittelyn käyttöönotto talous- ja toimintosovelluksissa suorituskyvyn parantamiseksi

Rinnakkaisen käsittelyn käyttöönotto saattaa lyhentää aikaa, joka tarvitaan tietojen tuontiin Dynamics 365 Customer Engagement -sovelluksista ja Microsoft Dataversesta talous- ja toimintosovelluksiin. 

Rinnakkaiskäsittely otetaan käyttöön seuraavasti talous- ja toimintosovelluksissa.

1. Kirjaudu talous- ja toimintosovellusympäristöön.
2. Valitse **Tietojen hallinta > Kehyksen parametrit**.
3. Valitse **Yksikön asetukset** ja valitse **Konfiguroi yksikön suoritusparametrit**.
4. Lisää rinnakkaiskäsittelyn parametrit:
    - **Tuontikynnysarvotietueiden määrä** – Niiden tietueiden määrä, jotka on täytettävä, ennen kuin rinnakkaiskäsittely on otettu käyttöön.
    - **Tuo tehtävän määrä** – Rinnakkain suoritettavan säikeiden (tehtävien) määrä.
5. Valitse **Tallenna**.


## <a name="errors-while-trying-to-start-a-table-mapping"></a>Virheitä yritettäessä käynnistää taulun yhdistämismääritystä

### <a name="unable-to-complete-initial-data-sync"></a>Tietojen ensimmäistä synkronointia ei voi suorittaa loppuun

Näyttöön saattaa tulla seuraavankaltainen virhe, kun tietojen ensimmäinen synkronointi yritetään suorittaa:

*Tietojen alkuperäistä synkronointia ei voi suorittaa loppuun. Virhe: kaksoiskirjoitusvirhe - laajennuksen rekisteröiminen epäonnistui: kaksoiskirjoitushaun metatietoja ei voi muodostaa. Virheen objektin viitettä ei ole määritetty objektin esiintymälle.*

Tämä virhe voidaan saada, kun yhdistämismäärityksen kyseiseksi tilaksi yritetään määrittää **Käytössä**. Korjaus määräytyy virheen syyn mukaan:

+ Jos yhdistämismääritykset ovat riippuvaisia määrityksistä, varmista, että otat käyttöön tämän taulun yhdistämismäärityksen sidonnaiset määritykset.
+ Yhdistämismäärityksestä saattaa puuttua lähde- tai kohdesarakkeet. Jos talous- ja toimintosovelluksen sarake puuttuu, noudata [Puuttuvien taulukkosarakkeiden ongelma yhdistämismäärityksissä](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) -kohdan ohjeita. Jos Dataversen sarake puuttuu, valitse yhdistämismäärityksessä **Päivitä taulut** -painike, jotta sarakkeet täytetään automaattisesti takaisin yhdistämismääritykseen.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Versioristiriitavirhe ja kaksoiskirjoitusratkaisujen päivittäminen

Seuraavat virheet voidaan saada, kun taulukon yhdistämismääritykset yritetään suorittaa:

+ *Asiakasryhmät (msdyn_customergroups): kaksoiskirjoitusvirhe – Dynamics 365 for Sales -ratkaisulla Dynamics365Company on versioristiriita. Versio: 2.0.2.10 Tarvittava versio: 2.0.133*
+ *Dynamics 365 for Sales -ratkaisussa Dynamics365FinanceExtended on versioristiriita. Versio: 1.0.0.0 Tarvittava versio: 2.0.227*
+ *Dynamics 365 for Sales -ratkaisussa Dynamics365FinanceAndOperationsCommon on versioristiriita. Versio: 1.0.0.0 Tarvittava versio: 2.0.133*
+ *Dynamics 365 for Sales -ratkaisussa CurrencyExchangeRates on versioristiriita. Versio: 1.0.0.0 Tarvittava versio: 2.0.133*
+ *Dynamics 365 for Sales -ratkaisussa Dynamics365SupplyChainExtended on versioristiriita. Versio: 1.0.0.0 Tarvittava versio: 2.0.227*

Ongelmat korjataan päivittämällä kaksoiskirjoitusratkaisut Dataversessa. Päivitys on muistettava tehdä uusimpaan tarvittavaa ratkaisuversiota vastaavaan ratkaisuun.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

