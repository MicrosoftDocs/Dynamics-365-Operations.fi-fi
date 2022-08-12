---
title: Yleinen vianmääritys
description: Tässä artikkelissa on yleisiä vianetsintätietoja kaksoiskirjoituksen integroinnista talous- ja toimintosovellusten sekä Dataversen välillä.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f263e331d23ce0ddf60a4abc2467513aa342445
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112361"
---
# <a name="general-troubleshooting"></a>Yleinen vianmääritys

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa on yleisiä vianetsintätietoja kaksoiskirjoituksen integroinnista talous- ja toimintosovellusten sekä Dataversen välillä.

> [!IMPORTANT]
> Jotkin tämän artikkelin osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoft Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Ota käyttöön laajennuksena toimiva jäljitysloki Dataversessä virheen tietojen tarkastelemiseksi

Jäljityslokit voivat olla hyödyllisiä kaksoiskirjoituksen reaaliaikaisen synkronoinnin ongelmien vianmäärityksessä talous- ja toimintosovellusten ja Dataversen välillä. Lokit voivat antaa yksityiskohtaisia tietoja ryhmille, jotka tarjoavat teknisen ja tietotekniikkaan liittyvän tuen Dynamics 365:lle. Tässä artikkelissa kerrotaan, miten jäljityslokit otetaan käyttöön ja miten niitä voi tarkastella. Seurantalokeja hallitaan Dynamics 365 -asetukset -sivulla, ja ne edellyttävät järjestelmänvalvojan tason oikeuksia muuttaa ja tarkastella tietoja. 

**Jäljityslokin ottaminen käyttöön ja virheiden tarkasteleminen:** järjestelmän hallintarooli

### <a name="turn-on-the-trace-log"></a>Jäljityslokin käyttöönottaaminen
Jäljitysloki otetaan käyttöön seuraavasti.

1.  Kirjaudu Dynamics 365:een ja valitse yläreunan siirtymispalkissa **Asetukset**. Napsauta Järjestelmät-sivulta **Hallinta**.
2.  Napsauta Hallinta-sivulla **Järjestelmäasetukset**.
3.  Valitse **Mukauttaminen**-välilehti ja laajennus ja vaihda sitten mukautetun työnkulun toimintojen seuranta -osiossa avattava valikko muotoon **Kaikki**. Tämä seuraa kaikki tehtävät ja antaa kattavan joukon tietoja ryhmille, joiden on tarkistettava mahdolliset ongelmat.

> [!NOTE]
> Jos avattavan asetuksen asetukseksi määritetään **Poikkeus**, jäljitystiedot ovat käytettävissä vain, kun poikkeuksia (virheitä) tapahtuu.

Kun avain on otettu käyttöön, jäljityslokit kerätään edelleen, kunnes ne on poistettu manuaalisesti käytöstä palaamalla tähän sijaintiin ja valitsemalla **Pois**.

### <a name="view-the-trace-log"></a>Näytä seurantaloki
Jäljitysloki näytetään seuraavasti.

1. Valitse Dynamics 365:n asetussivulla yläreunan siirtymispalkissa **Asetukset**. 
2. Valitse **Jäljityslokin laajennus** -sivun **Mukautukset**-osiossa.
3. Jäljityslokien luettelossa on merkintöjä, jotka perustuvat tyypin nimeen ja/tai sanoman nimeen.
4. Avaa haluamasi merkintä koko lokia varten. Suoritus-osan sanomalohko antaa tietoa laajennuksesta. Poikkeustiedot ovat myös käytettävissä, jos ne ovat saatavilla. 

Voit kopioida jäljityslokien sisällön ja liittää ne toiseen sovellukseen, kuten Muistioon tai muihin työkaluihin, jotta voit tarkastella lokeja tai tekstitiedostoja helpommin koko sisällössä. 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Virheenkorjaustilan käyttöönotto talous- ja toimintosovellusten live-synkronointiongelmien vianmäärityksessä

**Virheiden tarkastelemiseen tarvittava rooli:** Järjestelmänvalvoja

Sovellukseen perustuvat kaksoiskirjoitusvirheet Dataversessä voivat näkyä talous- ja toimintosovelluksessa. Virheiden sanatarkka kirjaaminen otetaan käyttöön seuraavasti:

1. Kaikissa talous- ja toimintosovelluksen projektimäärityksissä on **IsDebugMode**-merkintä **DualWriteProjectConfiguration**-taulukossa.
2. Avaa **DualWriteProjectConfiguration** käyttämällä Excel-apuohjelmaa. Apuohjelman käyttöä varten on otettava käyttöön suunnittelutila talous- ja toimintosovelluksen Excel-apuohjelmassa ja lisättävä **DualWriteProjectConfiguration** taulukkoon. Lisätietoja on kohdassa [Yksikön tietojen näyttäminen ja päivittäminen Excelissä](../../office-integration/use-excel-add-in.md).
3. Määritä projekti **IsDebugMode**-asetukseksi **Kyllä**.
4. Suorita virheitä tuottava skenaario.
5. Sanatarkat lokit tallennetaan **DualWriteErrorLog**-taulukossa.
6. Taulukon tietoja haetaan käyttämällä selaimessa linkkiä `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog` ja korvaamalla `999` tarvittaessa.
7. Päivitys tehdään uudelleen päivityksen [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe) jälkeen, ja se on saatavana platform update 37- ja sen jälkeisissä päivityksissä. Jos tämä korjaus on asennettu, virheenkorjaustilalla siepataan lisää lokeja.Jos olet asentanut tämän korjauksen, virheenkorjaustila kerää enemmän lokeja.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Talous- ja toimintosovelluksen näennäiskoneen synkronointivirheiden tarkistaminen

**Virheiden tarkastelemiseen tarvittava rooli:** Järjestelmänvalvoja

1. Kirjaudu Microsoft Dynamics Lifecycle Servicesiin (LCS).
2. Avaa LCS-projekti, jonka valitsit kaksoiskirjoitustestauksen suorittamista varten.
3. Valitse **Pilvipalveluympäristöt**-ruutu.
4. Voit kirjautua talous- ja toimintosovelluksen näennäiskoneeseen (VM) etätyöpöydän avulla. Käytä LCS:ssä näkyvää paikallista tiliä.
5. Avaa tapahtumien katseluohjelma.
6. Valitse **Sovellusten ja palveluiden lokit \> Microsoft \> Dynamics \> AX -DualWriteSync \> Toiminnassa**.
7. Tarkista viimeaikaisten virheiden luettelo.

## <a name="dual-write-ui-landing-page-showing-blank"></a>Kaksoiskirjoituskäyttöliittymän aloitussivu näkyy tyhjänä
Kun avaat kaksoiskirjoitussivun Microsoft Edge- tai Google Chrome -selaimessa, kotisivu ei lataudu ja näet tyhjän sivun tai virheilmoituksen, kuten "Jotain meni pieleen".
Devtoolissa näet myös virheen konsolin lokissa:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: Failed to read the 'sessionStorage' property from 'Window': Access is denied for this document. at t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860 ) at new t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103 ) at ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115 ) at Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728 ) at jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191 ) at Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692 ) at Or (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076 ) at Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750 ) at vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130 ) at hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151 )

Käyttöliittymä käyttää selaimen istuntojen tallennustilaa joidenkin ominaisuusarvojen tallentamiseen kotisivun lataamista varten. Jotta tämä toimisi, kolmannen osapuolen evästeiden on oltava sallittuja sivuston selaimessa. Virhe johtuu siitä, että käyttöliittymä ei voi käyttää istunnon tallennusta. Tämän ongelman yhteydessä voi kohdata kaksi esimerkkiä:

1.  Avaat käyttöliittymän Edgen/Chromen tuntemattomassa tilassa ja kolmannen osapuolen evästeet tuntemattomassa tilassa estetään.
2.  Olet estänyt kolmannen osapuolen evästeet Edgessä/Chromessa.

### <a name="mitigation"></a>Lievennys
Kolmannen osapuolen evästeet on sallittava selaimen asetuksissa.

### <a name="google-chrome-browser"></a>Google Chrome -selain
1. vaihtoehto:
1.  Siirry asetuksiin syöttämällä osoitepalkkiin chrome://settings/ ja siirtymällä tietosuoja- ja suojaustietoihin > Evästeet ja muut sivustotiedot.
2.  Valitse "Salli kaikki evästeet". Jos et halua tehdä tätä, siirry toiseen vaihtoehtoon.

2. vaihtoehto:
1.  Siirry asetuksiin syöttämällä osoitepalkkiin chrome://settings/ ja siirtymällä tietosuoja- ja suojaustietoihin > Evästeet ja muut sivustotiedot.
2.  Jos Estä kolmannen osapuolen evästeet tuntemattomassa tilassa tai Estä kolmannen osapuolen evästeet on valittuna, siirry kohtaan Sivustot, jotka voivat aina käyttää evästeitä ja napsauta **Lisää**. 
3.  Lisää talous- ja toimintosovellussivuston nimi - https://<your_FinOp_instance>,cloudax.dynamics.com. Varmista, että valitset Vain tämän sivuston kaikki evästeet -valintaruudun. 

### <a name="microsoft-edge-browser"></a>Microsoft Edge -selain
1.  Siirry kohtaan Asetukset -> sivuston käyttöoikeudet - > evästeet ja sivuston tiedot.
2.  Poista Estä kolmannen osapuolen evästeet käytöstä.  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Toisen Dataverse-ympäristön linkityksen poistaminen ja linkittäminen talous- ja toimintosovelluksesta

**Ympäristön linkityksen poistamiseen vaadittu rooli:** Joko talous- ja toimintosovelluksen tai Dataversen järjestelmänvalvoja.

1. Kirjaudu talous- ja toimintosovellukseen.
2. Siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Kaksoiskirjoitus**-ruutu.
3. Valitse kaikki käynnissä olevat yhdistämismääritykset ja valitse sitten **Pysäytä**.
4. Valitse **Poista ympäristön linkitys**.
5. Vahvista toiminto valitsemalla **Kyllä**.

Nyt voit linkittää uuden ympäristön.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Myyntitilausrivin tietolomaketta ei voi tarkastella 

Kun luot myyntitilauksen Dynamics 365 Salesissa, + **Lisää tuotteet** -vaihtoehdon napsauttaminen saattaa ohjata sinut Dynamics 365 Project Operationsin tilausrivilomakkeeseen. Kyseisessä lomakkeessa ei ole mitään tapaa tarkastella myyntitilausrivin **Tieto**-lomaketta. **Tietoja**-vaihtoehto ei näy **Uuden tilausrivin** alla olevassa avattavassa valikossa. Näin tapahtuu, koska Project Operations on asennettu ympäristöösi.

Voit ottaa **Tieto**-lomakevaihtoehdon uudelleen käyttöön seuraavasti:

1. Siirry **Tilausrivi**-taulukkoon.
2. Etsi **Tieto**-lomake lomakkeet-solmussa.
3. Valitse **Tieto**-lomake ja valitse **Ota käyttöön käyttöoikeusroolit**.
4. Muuta suojausasetukseksi **Näytä kaikille**.

## <a name="how-to-ensure-data-integration-is-using-the-most-current-finance-and-operations-schema"></a>Uusimman talous- ja toimintosovellusten rakenteen käytön varmistaminen tietojen integroinnissa

Tietojen integroinnissa saattaa kohdata tieto-ongelmia, jos ajan tasalla olevaa skeemaa ei käytetä. Seuraavien vaiheiden avulla voit päivittää talous- ja toimintosovellusten entiteettiluettelon ja tietojen integroijan entiteetit.

### <a name="refresh-entity-list-in-finance-and-operations-environment"></a>Talous- ja toimintosovellusympäristön entiteettiluettelon päivittäminen
1.  Kirjaudu talous- ja toimintosovellusympäristöön.
2.  Valitse **Tietojen hallinta**.
3.  Valitse Tietojen hallinta -kohdassa **Kehyksen parametrit**.
4.  Valitse **Tietojen tuonti- ja vientiympäristön parametrit** -sivulla **Yksikön asetukset** -välilehti ja valitse sitten **Päivitä yksikköluettelo**. Päivitys saattaa kestää yli 30 minuuttia sen mukaan, kuinka monta yksikköä on mukana.
5.  Siirry **Tietojen hallinta** -kohtaan ja tarkista odotetut entiteetit valitsemalla **Tietoyksiköt**. Jos odotetut entiteetit eivät ole luettelossa, tarkista, että entiteetit näkyvät talous- ja toimintosovellusympäristössä, ja palauta puuttuvat entiteetit tarpeen mukaan.

#### <a name="if-the-refresh-fails-to-resolve-the-issue-delete-and-re-add-the-entities"></a>Jos päivitys ei ratkaise ongelmaa, poista entiteetit ja lisää ne uudelleen.

> [!NOTE]
> Sinun on ehkä pysäytettävä kaikki käsittelyryhmät, jotka käyttävät yksiköitä aktiivisesti ennen poistoa.

1.  Valitse talous- ja toimintosovellusympäristössä **Tietojen hallinta** ja valitse sitten **Tietoyksiköt**.
2.  Hae ongelmallisia entiteettejä ja kirjoita muistiin kohdeyksikön, valmistelutaulun, yksikön nimen ja muiden asetusten tiedot. Poista entiteetti tai entiteetit luettelosta.
3.  Valitse **Uusi** ja lisää entiteetti tai entiteetit uudelleen vaiheen 2 tietoja käyttäen. 

#### <a name="refresh-entities-in-data-integrator"></a>Entiteettien päivittäminen tietojen integroijassa
Kirjaudu Power Platform -hallintakeskukseen ja valitse **Tietojen integrointi**. Avaa projekti, jossa ongelmat esiintyvät, ja valitse **Päivitä entiteetit**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Verkkojäljityksen ottaminen käyttöön ja tallentaminen siten, että jäljitys voidaan liittää tukipalvelupyyntöihin

Tukitiimin on ehkä tarkistettava verkkojäljitykset ongelmien vianmääritystä varten. Verkkoseuranta luodaan seuraavasti:

### <a name="google-chrome-browser"></a>Google Chrome -selain

1. Avaa kehittäjän työkalut painamalla avoimessa välilehdessä **F12**-näppäintä tai valitsemalla **Kehittäjän työkalut**.
2. Avaa **Verkko**-välilehti ja kirjoita **integ** suodatinruutuun.
3. Suorita skenaario ja tarkkaile lokiin kirjattavia pyyntöjä.
4. Napsauta merkintöjä hiiren kakkospainikkeella ja valitse **Tallenna kaikki HAR-tiedostona, jossa on sisältöä**.

### <a name="microsoft-edge-browser"></a>Microsoft Edge -selain

1. Avaa kehittäjän työkalut painamalla avoimessa välilehdessä **F12**-näppäintä tai valitsemalla **Kehittäjän työkalut**.
2. Avaa **Verkko**-välilehti.
3. Suorita skenaario.
4. Vie tulokset HAR-tiedostona valitsemalla **tallenna**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

