---
title: "Asennus ja käyttöönotto paikallisissa ympäristöissä"
description: "Tässä ohjeaiheessa on tietoja paikallisen ympäristön suunnittelusta, määrittämisestä ja käyttöönotosta."
author: sarvanisathish
manager: AnnBe
ms.date: 08/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations, Unified Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d100f6dbcbdf8f4c12ab04670fb598a88d48d84b
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: fi-fi
ms.lasthandoff: 08/10/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>Asennus ja käyttöönotto paikallisissa ympäristöissä

Tässä asiakirjassa kerrotaan, miten käyttöönotto suunnitellaan, infrastruktuuri määritetään ja Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (paikallinen) otetaan käyttöön.

## <a name="finance-and-operations-components"></a>Finance and Operationsin komponentit

Finance and Operations -sovelluksessa on kolme tärkeää osaa:

- Application Object Server (AOS)
- BI (Business Intelligence)
- Talousraportointi ja Management Reporter

Nämä komponentit tarvitsevat seuraavan järjestelmän ohjelmiston:

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 SP1, jossa on seuraavat ominaisuudet:

    - Teksti-indeksihaku on otettu käyttöön.
    - SQL Server Reporting Services (SSRS).
    - SQL Server Integration Services (SSIS).
    
     > [!NOTE]
     > Sovellusta ei voi käyttää, jos tekstihakua ei ole otettu käyttöön.

- SQL Server Management Studio
- Erillinen Microsoft Azure Service Fabric
- Windows PowerShell 5.0 tai uudempi
- Active Directory -liittoutumispalvelut (AD FS) Windows Server 2016:ssa

  Toimialueen ohjaimen on oltava vähintään Windows Server 2012 R2, jossa toimialueen toimintataso on vähintään 2012 R2

  Lisätietoja toimialueiden toimintatasosta: 
  - [Active Directoryn toimintatasojen selitys](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Active Directoryn -toimialueen palvelujen toimintatasot](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Käyttöikäpalvelut

Finance and Operations -osat jaetaan Microsoft Dynamics Lifecycle Servicesin (LCS) kautta. Ennen käyttöönottoa on ostettava käyttöoikeusavaimet [Enterprise Agreements](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) -kanavan kautta ja määritettävä paikallinen projekti LCS:ssä. Käyttöönotot voidaan käynnistää vain LCS:stä. Lisätietoja paikallisten LCS-projektien määrittämisestä on ohjeaiheessa [Paikallisen Lifecycle Services -projektin luominen](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>Todennus

Paikallista sovellusta voi käyttää AD FS:n kanssa. LCS:n käyttöä varten on määritettävä myös Azure Active Directory (Azure AD).

## <a name="standalone-service-fabric"></a>Erillinen Service Fabric

Finance and Operations käyttää erillistä Service Fabric -ympäristöä. Lisätietoja on ohjeaiheessa [Service Fabric -ohjeistus](/azure/service-fabric/).

## <a name="infrastructure"></a>Infrastruktuuri

Finance and Operations on suunniteltu toimimaan hyperkonvergenssissa arkkitehtuurissa. Laitemääritys sisältää seuraavat osat:

- Erillinen Windows Server 2016 virtuaalikoneisiin (VM) perustuva Service Fabric -klusteri
- SQL Server (sekä klusteroitua että aina käytössä olevaa SQL:ää tuetaan)
- AD FS -todennus
- Tallennuksena Server Message Block (SMB) versio 3:n jaettu tiedostoresurssi
- Valinnainen: Microsoft Office Server 2017

Lisätietoja on kohdissa [Järjestelmävaatimukset](../get-started/system-requirements.md) ja Koon määritysohjeet.

### <a name="hardware-layout"></a>Laitteistoasettelu

Suunnittele infrastruktuuri ja Service Fabric -klusteri ohjeaiheen [Laitteiston koon määrittäminen paikallisissa ympäristöissä](../get-started/hardware-sizing-on-premises-environments.md) kokosuositusten perusteella. Lisätietoja Service Fabric -klusterin suunnittelusta on ohjeaiheessa [Erillisen Service Fabric -klusterikäyttöönoton suunnittelu ja valmistelu](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

Seuraavassa taulukossa on esimerkki laitteistoasettelusta. Tätä esimerkkiä käytetään koko ohjeaiheessa asennusesimerkkinä.

> [!NOTE]
> Service Fabric -klusterin ensisijaisessa solmussa on oltava vähintään kolme solmua. Tässä esimerkissä **OrchestratorType** on määritetty ensisijaiseksi solmutyypiksi.

| Laitteen tarkoitus                                 | Laitteen nimi    | IP-osoite    |
|-------------------------------------------------|-----------------|---------------|
| Toimialueen ohjain                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Tiedostopalvelin                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL-klusteri aina päällä                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| Asiakas                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Service Fabric -klusteri / AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Service Fabric -klusteri / AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Service Fabric -klusteri / AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Service Fabric -klusteri / Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Service Fabric -klusteri / Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Service Fabric -klusteri / Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Service Fabric -klusteri / Management Reporter -solmu | SQLAOSMR1       | 10.179.108.18 |
| Service Fabric -klusteri / SSRS-solmu                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Asennus

### <a name="prerequisites"></a>Edellytykset

Seuraavien edellytysten on oltava kunnossa ennen asennuksen aloittamista. Näiden edellytysten määrittämistä ei käsitellä tässä asiakirjassa.

- Active Directory -toimialueen palvelut (AD DS) on asennettu ja määritetty verkossa.
- AD FS on otettu käyttöön.
- SQL Server, SSRS ja Management Studio on asennettu.

### <a name="overview"></a>Yleiskuvaus

Finance and Operationsin infrastruktuurin asennusta varten suoritettava seuraavat vaiheet:

1. Toimialuenimen ja DNS-vyöhykkeiden suunnitteleminen
2. Varmenteiden suunnitteleminen ja hankkiminen
3. Käyttäjä- ja palvelutilien suunnitteleminen
4. DNS-vyöhykkeiden luominen ja A-tietueiden lisääminen
5. VM-koneiden liittäminen toimialueeseen
6. Edellytyksenä olevien ohjelmistojen lisääminen VM-koneisiin
7. Asennuskomentosarjojen lataaminen LCS:stä
8. Määritysten kuvaus
9. Varmenteiden asentaminen
10. Erillisen Service Fabric -klusterin asentaminen
11. Vuokraajan LCS-yhteyksien määrittäminen
12. Tiedostojen tallennustilan asentaminen
13. SQL Serverin asentaminen
14. Tietokantojen määrittäminen
15. Tunnistetietojen salaaminen
16. Aseta SSRS
17. AD FS -määritykset

### <a name="plan-your-domain-name-and-dns-zones"></a>Toimialuenimen ja DNS-vyöhykkeiden suunnitteleminen

AOS-tuotantoasennuksessa kannattaa käyttää julkisesti rekisteröityä toimialuenimeä. Tällöin tavoin sitä voidaan käyttää verkon ulkopuolelta, jos ulkoinen käyttö on välttämätöntä.

Jos yrityksesi toimialue on esimerkiksi contoso.com, Finance and Operationsin (paikallinen) vyöhyke voi olla d365ffo.onprem.contoso.com ja isäntänimet ovat seuraavanlaiset:

- ax.d365ffo.onprem.contoso.com – AOS-koneet
- sf.d365ffo.onprem.contoso.com – Service Fabric -klusteri

### <a name="plan-and-acquire-your-certificates"></a>Varmenteiden suunnitteleminen ja hankkiminen

Secure Sockets Layer (SSL) -varmenteet ovat pakollisia Service Fabric -klusterin ja kaikkien käyttöönotettujen sovellusten suojaamiseksi. Tuotanto- ja eristysympäristökuormitusten varmenteet kannattaa hankkia varmenteiden myöntäjältä (CA), kuten [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) tai [GlobalSign](https://www.globalsign.com/en/ssl/). Jos toimialue määritetään [Active Directory -varmennepalvelujen](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS) avulla, voit luoda varmenteita AD CS:n kautta. Jokaisessa varmenteessa on oltava avainten vaihtoa varten luotu yksityinen avain, joka on voitava viedä .pfx (Personal Information Exchange) -tiedostona.

Itse allekirjoitettuja varmenteita voi käyttää vain testauksessa. Asennuskomentosarjat sisältävät käteviä komentosarjoja, jotka luovat ja vievät itse allekirjoitettuja varmenteita. Kuten edellä jo mainittiin, näitä varmenteita saa käyttää vain testauksessa.

| Tarkoitus                                      | Selitys | Lisävaatimukset |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL -varmenne                   | Tällä varmenteella salataan SQL Server -esiintymän ja asiakassovelluksen välillä verkossa lähetettävät tiedot. | <p>Varmenteen toimialuenimen on vastattava SQL Server -esiintymän tai -kuuntelutilan täydellistä toimialuenimeä (FQDN).</p><p>Jos esimerkiksi SQL-kuuntelutilan isäntä on kone DAX7SQLAOSQLA, varmenteen DNS-nimi on DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| Service Fabric -palvelimen varmenne            | Tämä varmenne auttaa suojaamaan solmusta solmuun tapahtuvan tiedonsiirron Service Fabric -solmujen välillä. Tätä varmennetta käytetään myös klusteriin yhteyden muodostavalle asiakasohjelmalle esitettävänä palvelinvarmenteena. | <p>Varmenteen toimialuenimen on vastattavana DNS-vyöhykettä, joka on AOS:n ja Service Fabricin isäntä.</p><p>Varmenteen toimialuenimi voi olla esimerkiksi \*.onprem.contoso.com tai \*.contoso.com.</p><p>Jos käytät yleismerkkivarmennetta, yleismerkki koskee vain yhtä tasoa. Varmenteessa on käytettävä alitoimialuetta eli hakijan vaihtoehtoista nimeä (SAN), jos siinä on useita tasoja. Tällainen on esimerkiksi edellisen esimerkin \*.contoso.com.</p> |
| Service Fabric -asiakasohjelman varmenne            | Asiakasohjelmat käyttävät tätä varmennetta Service Fabric -klusterin tarkastelemiseen ja hallintaan. | |
| Salakoodausvarmenne                     | Tällä varmenteella salataan arkaluonteisia tietoja, kuten SQL Serverin salasana ja käyttäjätilien salasanat. | <p>Varmenneavaimen käyttöön on sisällyttävä tiedon salakoodaus (10) eikä siihen saa sisältyä palvelimen tai asiakasohjelman todennusta.</p><p>Lisätietoja on ohjeaiheessa [Salaisuuksien hallinta Service Fabric -sovelluksissa](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| AOS SSL -varmenne                          | <p>Tätä varmennetta käytetään AOS-sivuston asiakasohjelmalle esitettävänä palvelinvarmenteena. Sillä otetaan myös käyttöön Windows Communication Foundation (WCF)- ja Simple Object Access Protocol (SOAP) -varmenteet.</p><p>Service Fabric -palvelimen varmennetta voi käyttää tässä, jos se on yleismerkkivarmenne.</p> | <p>Varmenteen toimialuenimen on vastattavana DNS-vyöhykettä, joka on AOS:n ja Service Fabricin isäntä.</p><p>Varmenteen toimialuenimi voi olla esimerkiksi \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com tai \*.contoso.com.</p><p>Jos käytät yleismerkkivarmennetta, yleismerkki koskee vain yhtä tasoa. Varmenteessa on käytettävä alitoimialuetta eli SAN-nimeä, jos siinä on useita tasoja. Tällainen on esimerkiksi edellisen esimerkin \*.contoso.com.</p> |
| Istunnon todennusvarmenne           | AOS suojaa tällä varmenteella käyttäjän istuntotiedot. | Se on myös **Jaettu tiedostoresurssi** -varmenne, jota käytetään LCS:stä tapahtuvan käyttöönoton aikana. |
| Tietojen salauksen ja tietojen allekirjoituksen varmenteet | AOS salaa arkaluonteiset tiedot näillä varmenteilla. | |
| Talousraportoinnin asiakasohjelman varmenne       | Tämä varmenne auttaa suojaamaan talousraportointipalvelujen ja AOS:n välisen tiedonsiirron. | |
| Raportointivarmenne                        | Tämä varmenne auttaa suojaamaan SSRS:n ja AOS:n välisen tiedonsiirron. | |
| Paikallisen agentin varmenne           | <p>Tämä varmenne auttaa suojaamaan paikallisesti isännöidyn paikallisen agentin ja LCS:n välisen tiedonsiirron.</p><p>Tämä varmenne auttaa paikallista agenttia toimimaan Azure AD -vuokraajan puolesta sekä järjestelemään ja valvomaan käyttöönottoja LCS:n kanssa tapahtuvan tiedonsiirron avulla.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Käyttäjä- ja palvelutilien suunnitteleminen

Jotta Finance and Operations (paikallinen) toimisi, sinun on luotava useita käyttäjä- tai palvelutilejä. Sinun on luotava yhdistelmä ryhmän hallitsemia palvelutilejä (gMSA-tilit), toimialuetilejä ja SQL-tilejä. Seuraava taulukko sisältää käyttäjätilit, niiden käyttötarkoituksen ja tässä ohjeaiheessa käytettävät nimiesimerkit.

| Käyttäjätili                                            | Laji           | Tarkoitus | Käyttäjänimi |
|---------------------------------------------------------|----------------|---------|-----------|
| Taloushallinnon raportointisovellusten palvelutili         | gMSA           |         | Contoso\\svc-FRAS$ |
| Taloushallinnon raportointiprosessin palvelutili             | gMSA           |         | Contoso\\svc-FRPS$ |
| Taloushallinnon raportoinnin yhden napsautuksen suunnittelutyökalun palvelutili | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS-palvelutili                                     | gMSA           | Tämä käyttäjä on luotava tulevaa käyttöä varten. AOS-käytön on tarkoitus on mahdollista tulevissa gMSA-julkaisuissa. Kun tämä käyttäjä luodaan asennuksen yhteydessä, gMSA:han siirtyminen tulee tapahtumaan sujuvasti. | Contoso\\svc-AXSF$ |
| AOS-palvelutili                                     | Toimialuetili | AOS käyttää tätä käyttäjää GA-julkaisussa. | Contoso\\AXServiceUser |
| AOS SQL -tietokannan järjestelmänvalvoja                                   | SQL-käyttäjä       | Finance and Operations suorittaa tällä käyttäjällä SQL-todennuksen\*. gMSA-käyttäjä korvaa tämän käyttäjän tulevissa versioissa. | AXDBAdmin |
| Paikallisen käyttöönottoagentin palvelutili                  | gMSA           | Paikallinen agentti käyttää tätä tiliä käyttöönoton järjestelemiseen eri solmuissa. | Contoso\\Svc LocalAgent$ |

\* SQL-todennuksen SQL-käyttäjänimi ja -salasana ovat suojattuja, koska ne on salattu ja tallennettu jaettuun tiedostoresurssiin.

### <a name="create-dns-zones-and-add-a-records"></a>DNS-vyöhykkeiden luominen ja A-tietueiden lisääminen

DNS on integroitu AD DS:n kanssa ja voit järjestää, hallita ja etsiä resursseja sen avulla verkossa. Luo DNS-järjestelmän edelleenlähetyshakujen alue ja A-tietueet AOS-isäntänimille ja Service Fabric -klusterille. Tässä esimerkkiasennuksessa DNS-vyöhykkeen nimi on d365ffo.onprem.contoso.com ja A-tietueiden tai isäntien nimet ovat seuraavat:

- **ax**.d365ffo.onprem.contoso.com – AOS-koneet
- **sf**.d365ffo.onprem.contoso.com – Service Fabric -klusteri

#### <a name="add-a-dns-zone"></a>DNS-vyöhykkeen lisääminen

Lisää DNS-vyöhyke seuraavien ohjeiden mukaan.

1. Kirjaudu toimialueen ohjauskoneeseen, valitse **Aloita** ja käynnistä DNS-hallinta kirjoittamalla **dnsmgmt.msc**.
2. Napsauta hiiren kakkospainikkeella toimialueen ohjauskonetta ja valitse sitten **Uusi vyöhyke** \> **Seuraava**.
3. Valitse **Ensisijainen vyöhyke**.
4. Älä valitse **Tallenna vyöhyke Active Directoryyn (käytössä vain, jos DNS-palvelin on kirjoitettava toimialueen ohjain** -valintaruutua ja valitse sitten **Seuraava**.
5. Valitse ensin **Kaikkien tämän toimialueen toimialueen ohjaimissa käytössä oleviin DNS-palvelimeen: Contoso.com** ja sitten **Seuraava**.
6. Valitse ensin **Edelleenlähetyshakujen alue** ja sitten **Seuraava**.
7. Anna asennukselle vyöhykenimi ja valitse **Seuraava**. Anna esimerkiksi **d365ffo.onprem.contoso.com**.
8. Valitse ensin **Älä salli dynaamisia päivityksiä** ja sitten **Seuraava**.

#### <a name="set-up-an-a-record-for-aos"></a>AOS:n A-tietueen määrittäminen

Luo uudella DNS-vyöhykkeellä yksi **ax.d365ffo.onprem.contoso.com**-niminen A-tietue **jokaiselle** **AOSNodeType**-tyypin Service Fabric -klusterisolmulle. Älä luo A-tietueita muille solmutyypeille.

1. Napsauta uutta vyöhykettä hiiren kakkospainikkeella ja valitse sitten **Uusi isäntä**.
2. Anna Service Fabric -solmun nimi ja IP-osoite (kuten 10.179.108.12) ja valitse sitten **Lisää isäntä**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Orchestrator-toiminnon A-tietueen määrittäminen

Luo uudella DNS-vyöhykkeellä yksi **sf.d365ffo.onprem.contoso.com**-niminen A-tietue **jokaiselle** **OrchestratorType**-tyypin Service Fabric -klusterisolmulle. Älä luo A-tietueita muille solmutyypeille.

1. Napsauta uutta vyöhykettä hiiren kakkospainikkeella ja valitse sitten **Uusi isäntä**.
2. Anna Service Fabric -solmun nimi ja IP-osoite (kuten 10.179.108.15) ja valitse sitten **Lisää isäntä**.

#### <a name="join-vms-to-the-domain"></a>VM-koneiden liittäminen toimialueeseen

Liitä jokainen VMs toimialueeseen ohjeaiheessa [Windows Server 2016:n liittäminen Active Directory -toimialueeseen](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html) annettujen ohjeiden mukaisesti. Voit vaihtoehtoisesti käyttää Windows PowerShell -komentosarjaa.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
Kun VM:t on liitetty toimialueeseen, lisää AOS-palvelutilit (Contoso\svc-AXSF$ , Contoso\svc-AXSF$ ) paikalliseen järjestelmänvalvojaryhmään. Artikkelissa [Jäsenen lisääminen paikalliseen ryhmään](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx) kerrotaan, miten se tapahtuu.

#### <a name="disable-user-access-control"></a>Käytönvalvonnan poistaminen käytöstä 

Poista käytönvalvonta käytöstä **kaikissa** Service Fabric -solmuissa suorittamalla seuraava komentosarja.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> Solmu on käynnistettävä uudelleen, kun komentosarjan on valmis.

#### <a name="add-prerequisite-software-to-vms"></a>Edellytyksenä olevien ohjelmistojen lisääminen VM-koneisiin

Seuraavassa taulukossa on luettelo ohjelmistoista, jotka on otettava käyttöön kunkin solmutyypin koneissa.

> [!NOTE]
> Tietokone on käynnistettävä uudelleen komponentin asentamisen jälkeen.

| Solmutyyppi | Komponentti | Komento |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC-ohjain | Katso [Microsoft ODBC Driver 13.1 for SQL Server – Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Microsoft .NET Framework versio 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Framework versio 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | IIS (Internet Information Services) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013 | Katso [Microsoft Visual C++ Redistributable Packages for Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | Microsoft Access Database Engine 2010 Redistributable | Katso [Microsoft Access Database Engine 2010 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | .NET Framework versio 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Framework versio 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | SQL Server Reporting Services 2016 **alkuperäistilassa** | |
| MR        | .NET Framework versio 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework versio 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual C++ Redistributable Packages for Visual Studio 2013 | Katso [Microsoft Visual C++ Redistributable Packages for Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>Asennuskomentosarjojen lataaminen LCS:stä

Asennuskokemuksen parantamista varten käytettävissä on useita komentosarjoja. Lataa asennuksen komentosarjat LCS:stä seuraavasti:

1. Kirjaudu LCS:ään (<https://lcs.dynamics.com/v2>).
2. Valitse koontinäytössä **Jaettu omaisuus -kirjasto** -ruutu.
3. Napsauta **Malli**-välilehteä.
4. Valitse ruudukossa **Dynamics 365 for Operations – paikallisen käyttöönoton komentosarjat** -rivi.
5. Valitse **Versiot** ja lataa komentosarjojen uusin versio.

### <a name="describe-your-configuration"></a>Määritysten kuvaus

Tässä osassa on tietoja suoritettavista komentosarjoista. Komentosarjat käsitellään siinä järjestyksessä, jossa ne on suoritettava. Suorita komentosarjat täyttämällä mallitiedosto kohteessa $(downloadPath)\\ConfigTemplate.xml. ConfigTemplate.xml-tiedostossa on kuvaus Service Fabric -klustereista, niiden määrittämisessä käytettävistä varmenteista ja tileistä, joiden on myönnettävä käyttöoikeus soveltuville varmenteille. Annetussa esimerkissä arvot täytetään tässä ohjeaiheessa käsiteltyyn esimerkki-infrastruktuuriin. Mallitiedostoa käytetään seuraavassa osassa.

#### <a name="create-the-domain-account-for-a-service-user"></a>Palvelukäyttäjän toimialuetilin luominen

Luo toimialuekäyttäjän tili suorittamalla seuraava komento: contoso\\AXServiceUser.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>gMSA-tilien luominen

1. Vaihda hakemistoksi **$(DownloadPath)** ja suorita seuraava Windows PowerShell -komento.

    > [!NOTE]
    > Komentosarja ei luo käyttäjiä. Sen sijaan se tulostaa komennot, jotka on suoritettava manuaalisesti toimialueen ohjauskoneessa.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Kopioi komentotuloste Windows PowerShell -ikkunaan. Varmista, että rivinvaihdot on poistettu, ja suorita rivit Active Directoryn toimialueen ohjauskoneessa käyttämällä laajettuja oikeuksia (napsauta hiiren kakkospainikkeella ja valitse sitten **Suorita järjestelmänvalvojana**).
3. Suorita seuraava komentosarja Active Directoryn toimialueen ohjauskoneessa. Sillä tarkistetaan, että tilien luonti onnistui. Varmista, että suoritat komentosarjan sen jälkeen, kun olet korvannut palvelutilien nimeämiskäytäntöä vastaavan mallin.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Suorita komentosarja Export-AddGMSAsONVMScript.ps1 asiakasohjelman tietokoneessa. Komentosarja luo komentosarjat, jotka suoritetaan kussakin Service Fabric VM -koneessa, ja lisää ne kutakin VM-nimeä vastaavaan kansioon.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>Pysäytä IIS

Muodosta yhteys kuhunkin Service Fabricin VM-koneeseen RDP-etäkäyttöprotokollan avulla ja tee sitten ohjeaiheen [Verkkopalvelimen (IIS 7) käynnistäminen tai pysäyttäminen](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx) mukaiset manuaaliset vaiheet. Voit vaihtoehtoisesti käyttää seuraavaa Windows PowerShell -komentosarjaa muodostamalla yhteyden RDP-etäkäyttöprotokollan avulla kuhunkin Service Fabricin VM-koneeseen.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_IIS-toiminnon on oltava asennettuna mutta poistettuna käytöstä, sillä tuotteessa on joitakin riippuvuuksia IIS dll -tiedostoihin._

### <a name="install-certificates"></a>Varmenteiden asentaminen

1. Jos hankit aiemmin tässä aiheessa mainitut varmenteet hyväksytyltä varmenteiden myöntäjältä, täytä .pfx-tiedoston nimi ja allekirjoitus ConfigTemplate.xml-tiedoston varmenteisiin. Valitse **generateSelfSignedCert**-määritteen arvoksi **Epätosi** ja **exportable**-määritteen arvoksi **Epätosi**. Kopioi .pfx-tiedostot $(DownloadPath)\\InfrastructureScripts\\Certs-kansioon.
2. Jos käytät itseallekirjoitettuja varmenteita (joita saa käyttää vain testauksessa), suorita seuraava komentosarja: Voit luoda itseallekirjoitettuja varmenteita varmistamalla, että ConfigTemplate.xml-tiedoston **generateSelfSignedCert**-arvoksi on valittu **Tosi** ja **exportable**-arvoksi **Tosi**. Komentosarja päivittää XML-tiedostoon varmenteiden allekirjoituksen.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Vie uudet varmenteet yksityiseen avaimeen (.pfx-tiedostoon). Luo ja suorita vientikomennot Windows PowerShellissä seuraavalla komentosarjalla: .pfx-tiedostot asetetaan Certs-kansioon.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Varmenteiden on oltava asennettuna ja sisällyttävä varmenteeseen:\\CurrentUser\\My. Varmenteet on myös voitava viedä.

    Jos käytät itseallekirjoitettuja varmenteita, siirry seuraavaan osaan. Sinun ei tarvitsee suorittaa tätä menettelyä.

4. Kun olet vienyt tai kopioinut .pfx-tiedostot $(DownloadPath)\\InfrastructureScripts\\Certs-kansioon, suorita komentosarjat, joilla luodaan VM-koneita vastaaviin kansioihin asetettavat komentosarjat.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Kopioi kunkin kansion komentosarjat kansion nimeä vastaavaan VM-koneeseen.
6. Suorita komentosarjat kussakin VM-koneessa siinä järjestyksessä, kun ne ovat.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Erillisen Service Fabric -klusterin määrittäminen

1. Luo ClusterConfig.json-tiedosto suorittamalla seuraava komento:

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Lisätietoja on ohjeaiheissa [Vaihe 1B: Monta konetta sisältävän klusterin luominen](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Erillisen klusterin suojaaminen Windowsissa X.509-varmenteilla](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) ja [Windows Serverissä käytettävän erillisen klusterin luominen](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. Lataa [erillinen Service Fabric -asennuspaketti](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) yhteen Service Fabric -solmuun. Kun zip-tiedosto on ladattu, avaa zip-tiedosto napsauttamalla sitä hiiren kakkospainikkeella ja valitsemalla sitten **Ominaisuudet**. Valitse valintaikkunassa, **Kumoa esto** -valintaruutu oikeassa alakulmassa.
3. Kopioi zip-tiedosto yhteen Service Fabric -klusterin solmuun ja pura se.
4. Luo saapuvan liikenteen palomuurisääntö kaikkien solmujen portteihin 443 ja 445 seuraavilla komennoilla:

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Luo saapuvan liikenteen palomuurisääntö vain SSRS-solmun porttiin 80 seuraavilla komennoilla:

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. Kopioi ClusterConfig.json-tiedosto erillisen Service Fabricin purkamattomaan asennussijaintiin.
7. Siirry Windows PowerShellin purkamattomaan asennussijaintiin laajennetuilla oikeuksilla ja testaa ClusterConfig suorittamalla seuraava komento:

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Jos testi onnistuu, ota klusteri käyttöön suorittamalla seuraava komento:

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. Kun klusteri on luotu, tarkista asennus avaamalla Service Fabricin resurssienhallinta jossakin asiakasohjelmakoneessa:

    1. Asenna Service Fabric -asiakasohjelman varmenne kansioon CurrentUser\\My, jos sitä ei ole vielä asennettu.
    2. Valitse **IE-asetukset** \> **Yhteensopivuustila** ja poista **Näytä intranet-sivustot yhteensopivuustilassa** -valintaruudun valinta.
    3. Siirry osoitteeseen `https://sf.d365ffo.onprem.contoso.com:19080`, jossa sf.d365ffo.onprem.contoso.com on vyöhykkeellä määritetyn Service Fabric -klusterin isäntänimi. Jos DNS-nimen selvitystä ei ole määritetty, käytä koneen IP-osoitetta.
    4. Valitse asiakasohjelman varmenne. **Service Fabricin resurssienhallinta** -sivu avautuu.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>Vuokraajan LCS-yhteyksien määrittäminen

Finance and Operationsin käyttöönotto ja huolto järjestellään LCS:n kautta käyttämällä paikallista agenttia. Yhteyksien muodostaminen LCS:stä Finance and Operationsin vuokraajaan edellyttää sen varmenteen määrittämistä, jonka avulla paikallinen agentti voi toimia Azure AD -vuokraajan (kuten Contoso.Onmicrosoft.comin) puolesta.

Käytä varmenteen myöntäjältä saatua paikallisen agentin varmennetta tai komentosarjoilla muodostettua itseallekirjoitettua varmennetta.

Vain käyttäjätilit, joilla on yleisen järjestelmänvalvojan hakemistorooli, voivat lisätä varmenteita LCS:n valtuuttamiseen. Hakemiston yleinen järjestelmänvalvoja on oletusarvoisesti henkilö, joka rekisteröi organisaation Microsoft Office 365:n.

> [!NOTE]
> Varmenteen saa määrittää kullekin vuokraajalle vain kerran. Kaikki paikalliset ympäristöt muodostavat LCS-yhteyden samalla varmenteella.

1. Lataa ja asenna uusin Azure PowerShell -versio asiakastietokoneeseen. Lisätietoja on ohjeaiheessa [Azure PowerShellin asentaminen ja määrittäminen](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Kirjaudu [asiakkaan Azure-portaaliin](https://portal.azure.com) ja varmista, että sinulla on yleisen järjestelmänvalvojan hakemistorooli.
3. Suorita seuraava komentosarja kansiosta $(DownloadPath)\\InfrastructureScripts.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Tiedostojen tallennustilan määrittäminen

Sinun on määritettävä kaksi erittäin käytettävissä olevaa jaettua SMB 3.0 -tiedostoresurssia. Lisätietoja SMB 3.0:n käyttöönotosta on ohjeaiheessa [SMB-suojausparannukset](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
Suojattua kielioppineuvottelua ei voi havaita tai estää, kun ohjelmistoversiosta SMB 2.0 tai 3.0 siirrytään versioon SMB 1.0. Tämän vuoksi SMB-salauksen kaikkien ominaisuuksien hyödyntämiseksi SMB 1.0 -palvelin on syytä poistaa käytöstä.

> [!NOTE]
> Voit varmistaa, että ympäristön lepäävät tiedot on suojattu, ottamalla BitLocker-asemansalauksen käyttöön kaikissa koneissa. Lisätietoja BitLockerin ottamisesta käyttöön on ohjeaiheessa [BitLocker: käyttöönotto Windows Server 2012:ssa ja uudemmissa versioissa](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- AOS-palvelimeen ladatut jaetut tiedostoresurssit, joihin käyttäjän asiakirjat on tallennettu (esimerkki: \\\\DAX7SQLAOFILE1\\aos-storage).
- Jaettu tiedostoresurssi, johon on tallennettu uusimmat koontiversio- ja määritystiedostot käyttöönoton järjestelemistä varten (esimerkki: \\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > Tämä tiedostopolku kannattaa pitää mahdollisimman lyhyenä, jotta jaettuun tiedostoresurssiin sijoitettavien tiedostojen tiedostopolun pituus ei ylity.

1. Suorita seuraava komento koneessa, jossa jaettu tiedostoresurssi on:

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>Määritä \\\\DAX7SQLAOFILE1\\aos-storage jaetuksi tiedostoresurssiksi

2. Valitse Server Managerissa **Tiedosto- ja tallennuspalvelimet** \> **Jaetut resurssit**.
3. Valitse **Tehtävät** \> **Uusi jaettu resurssi** ja luo uusi jaettu resurssi, jonka nimi on **aos-storage**.
4. Myönnä **Muokkaa**-käyttöoikeudet kaikille muille Service Fabric -klusterin koneille paitsi **OrchestratorNodeType**.
5. Myönnä **Muokkaa**-käyttöoikeudet AOS-toimialuekäyttäjän käyttäjälle (contoso\\AXServiceUser) ja gMSA-käyttäjälle (contoso\\svc-AXSF).

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>Määritä \\\\DAX7SQLAOFILE1\\agent jaetuksi tiedostoresurssiksi

6. Palaa Server Manageriin ja valitse **Tiedosto- ja tallennuspalvelimet** \> **Jaetut resurssit**.
7. Valitse **Tehtävät** \> **Uusi jaettu resurssi** ja luo uusi jaettu resurssi, jonka nimi on **agent**.
8. Myönnä **Täydet oikeudet** -käyttöoikeudet paikallisen käyttöönottoagentin gMSA-käyttäjälle (contoso\\svc-LocalAgent$).

### <a name="set-up-sql-server"></a>SQL Serverin asentaminen

1. Asenna erittäin käytettävä SQL Server 2016 SP1 joko tallennusalueverkon (SAN) sisältävänä SQL-klusterina tai aina päällä -määrityksenä.  Varmista, että **Database Engine, Reporting Services, tekstihaku** ja **hallintatyökalut** on jo asennettu.
> [!NOTE]
> Varmista, että SQL aina päällä on määritetty ohjeaiheen [Tietojen ensimmäisen synkronointi -sivun valinta (Aina päällä -käytettävyysryhmän ohjatut toiminnot)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) mukaisesti ja noudata ohjeaihetta [Toissijaisten tietokantojen valmistelu manuaalisesti](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. Suoritta SQL-palvelu toimialuekäyttäjänä.
3. Määritä Finance and Operations hakemalla SSL-varmenne varmenteen myöntäjältä. Voit luoda testausta varten itse allekirjoitetun varmenteen.

**Klusteroidun SQL -esiintymän itse allekirjoitettu varmenne**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Aina päällä SQL -esiintymän itse allekirjoitettu varmenne**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. Määritä SSL SQL Serverissä varmenteen avulla käyttämällä ohjeaiheen [SQL Server -esiintymän SSL-salauksen ottaminen käyttöön Microsoft Management Consolessa](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) ohjeita.
5. Noudata seuraavia ohjeita klusterin jokaisessa solmussa. Varmista, että teet muutokset ei-aktiivisessa solmussa ja siirryt siihen sen jälkeen, kun muutokset siihen.

    1. Tuo varmenne kohteeseen LocalMachine\\My.
    2. Myönnä varmenteen käyttöoikeudet palvelutilille, jolla SQL-palvelu suoritetaan. Napsauta varmennetta (certlm.msc) Microsoft Management Consolessa (MMC) hiiren kakkospainikkeella ja valitse sitten **Tehtävät** \> **Yksityisten avainten hallinta**.
    3. Lisää allekirjoitus kansioon HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.
    4. Määritä Microsoft SQL Serverin määritystenhallinnassa **ForceEncryption**-asetukseksi **Kyllä**.

6. Vie varmenteen (.cer-tiedosto) julkinen avain ja asenna se kunkin Service Fabric -solmun luotettuun pääkansioon.

### <a name="configure-the-orchestratordata-database"></a>OrchestratorData-tietokannan määrittäminen

1.  Luo tyhjä tietokanta ja anna sen nimeksi **OrchestratorData**. Paikallinen agentti käyttää tätä tietokantaa käyttöönottojen järjestelemiseen.
2.  Myönnä tietokannassa paikallisen agentin gMSA (svc-LocalAgent$) **db\_owner** -käyttöoikeudet:

    1. Laajenna palvelimen nimi hierarkiapuussa, laajenna **Suojaus** \> **Kirjautumiset**, napsauta sitten hiiren kakkospainikkeella ja valitse **Uusi kirjautuminen**.

        ![Uusi kirjautuminen -komento](./media/OPSetup_01_NewLogin.png)


    2. Etsi **svc-LocalAgent$**-palvelutili. Valitse ensin **Sijainnit** ja **Koko hakemisto** ja sitten **Objektityypit** ja **Palvelutili**.

        ![Valitse Käyttäjä-, Palvelutili- tai Ryhmä-valintaruutu](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. Valitse **Määritä ServerRole** -asetukseksi **Julkinen**.
    4. Määritä **db\_owner**-tietokantarooli käyttöoikeudet OrchestratorData-tietokannalle.

### <a name="configure-the-finance-and-operations-database"></a>Finance and Operationsin tietokannan määrittäminen

1. Kirjaudu LCS:ään (<https://lcs.dynamics.com/v2>).
2. Valitse koontinäytössä **Jaettu omaisuus -kirjasto** -ruutu.
3. Napsauta **Malli**-välilehteä. 
4. Lataa sovellus napsauttamalla **Paikallinen Dynamics 365 for Operations Enterprise Edition – esittelytiedot** -riviä.
5. Zip-tiedosto sisältää tyhjiä tiedostoja ja esittelytietojen .bak-tiedostot. Valitse sopiva .bak-tiedosto. Jos esimerkiksi tarvitset esittelytiedot, palauta AxBootstrapDB_Demodata.bak-tiedosto. 
6. Palauta AxBootstrapDB_DemoData.bak-tietokanta.
7. Vaihda tietokannan nimeksi **AXDBRAIN**.
8. Suorita seuraavat kyselyt palautetussa tietokannassa.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Päivitä tietokantatiedostot:

    1. Napsauta tietokantaa hiiren kakkospainikkeella ja valitse sitten **Ominaisuudet**.
    2. Muuta tietokantatiedoston ominaisuuksia valitsemalla **Tiedostot**.
    3. Anna **Alkuperäinen koko (Mt)** -kenttään arvo, joka on suurempi kuin 5 120.

        ![Tietokannan ominaisuudet -valintaikkuna](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. Määritä **AXDBBuild\_Data**-kohdassa **Automaattinen kasvu tai suurenna** -kentän arvoksi **200** megatavua (Mt).
    5. Määritä **AXDBBuild\_Log**-kohdassa **Automaattinen kasvu tai suurenna** -kentän arvoksi **500** Mt.

        ![Muuta automaattinen kasvu -valintaikkuna.](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. Luo uusi käyttäjä, jolle on otettu käyttöön SQL-todennus (axdbadmin).
6. Yhdistä käyttäjät ja tietokantarooli seuraavan taulukon tietojen mukaisesti.

    | Käyttäjä             | Laji    | Tietokantarooli |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. Anna svc-AXSF$-käyttäjälle ja axdbadmin SQL -käyttäjälle seuraavien roolien käyttöoikeus tempdb-tietokannassa:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. Suorita Management Studiossa seuraavat Transact SQL (T-SQL) -komennot:

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Suorita seuraava komento:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>Taloushallinnon raportointitietokannan määrittäminen

1.  Luo tyhjä tietokanta ja anna sen nimeksi **FinancialReporting**.
2.  Yhdistä käyttäjät ja tietokantarooli seuraavan taulukon tietojen mukaisesti.

    | Käyttäjä             | Laji | Tietokantarooli |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>Tunnistetietojen salaaminen

1. Asenna salauskoodausvarmenne missä tahansa koneessa kansioon LocalMachine\\My certificate store.
2. Myönnä nykyiselle käyttäjälle tämän varmenteen lukuoikeus.
3. Luo tässä näkyvä Credentials.json-tiedosto.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** on AOS-toimialuekäyttäjän (contoso\\axserviceuser) salattu toimialuekäyttäjän salasana.
    - **SqlUser** on salattu SQL-käyttäjä (axdbadmin), jolla on Finance and Operations -tietokannan (AXDBRAIN) käyttöoikeus, ja **SqlPassword** on salattu SQL-salasana.

4. Kopioi .json-tiedosto jaettuun SMB-tiedostoresurssiin \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. Päivitä Credentials.json-tiedosto salatuilla arvoilla.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. Korvaa **\<encryptedDomainUserPassword\>** Credentials.json-tiedostossa salatulla toimialueen salasanalla.
    2. Korvaa **\<encryptedSqlUser\>** salatulla Finance and Operationsin SQL-käyttäjällä.
    3. Korvaa **\<encryptedSqlPassword\>** salatulla Finance and Operationsin SQL-salasanalla.
    
### <a name="set-up-ssrs"></a>Aseta SSRS

1.  Varmista ennen aloittamista, että tämän ohjeaiheen alussa mainitut ennakkovaatimukset toteutuvat.
2.  Noudata ohjeaiheen [SQL Server Reporting Servicesin määrittäminen paikallisessa käyttöönotossa](../analytics/configure-ssrs-on-premises.md) ohjeita.

### <a name="configure-ad-fs"></a>AD FS -määritykset

AD FS on otettava käyttöön Windows Server 2016:ssa ennen tätä toimenpidettä. Lisätietoja AD FS:n käyttöönotosta on ohjeaiheessa [Windows Server 2016:n käyttöönotto-opas ja 2012 R2 AD FS:n käyttöönotto-opas](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Finance and Operations edellyttää valmiin AD FS -oletusmäärityksen lisäksi lisämäärityksiä. Windows PowerShelliä käytetään seuraavissa vaiheissa koneessa, johon AD FS -palvelu on asennettu. Käyttäjätilillä on oltava riittävät käyttöoikeudet AD FS -palvelun hallintaan. Käyttäjällä on esimerkiksi oltava toimialueen järjestelmänvalvojan tili.

1. Määritä AD FS -tunniste siten, että se vastaan AD FS -tunnuksen myöntäjää.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Poista intranet-todennusyhteyksien Windows Integrated Authentication (WIA) käytöstä, ellet ole määrittänyt AD FS -palvelua yhdistelmäympäristöihin. Lisätietoja WIA:n määrittämisestä siten, että sitä voidaan käyttää AD FS -palvelun kanssa, on ohjeaiheessa [Selaimien määrittäminen käyttämään Windows Integrated Authentication (WIA) -todennusta AD FS -palvelun kanssa](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. Kirjautumista varten käyttäjän sähköpostiosoitteen on oltava hyväksytyssä todennusmuodossa.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

AD FS luottaa Finance and Operationsiin todennusvaihdossa, kun erilaiset sovellusmerkinnät on rekisteröity AD FS -sovellusryhmän AD FS -palvelussa. Seuraavan komentosarjan käyttö rekisteröinnissä nopeuttaa määritysprosessia ja vähentää virheitä. Kopioi Publish-ADFSApplicationGroup.ps1-komentosarja ja D365FO-OP-hakemisto koneeseen, johon AD FS -roolipalvelu on asennettu. Suorita komentosarja sitten käyttäjätilillä, kuten järjestelmänvalvojan tilillä, jonka käyttöoikeudet riittävät AD FS -palvelun hallintaan. Lisätietoja komentosarjan käytöstä on komentosarjassa mainitussa dokumentaatiossa. Kirjoita muistiin tulosteessa määritetyt asiakasohjelman tunnukset, koska LCS kysyy näitä tietoja myöhemmässä vaiheessa.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

AD FS -hallintakonsolin pitäisi muistuttaa seuraavassa kuvassa olevaa konsolia. Avaa Server Manager valitsemalla ensin **Työkalut** \> **AD FS:n hallinta** ja sitten vasemmalla puunäkymän alareunasta **Sovellusryhmät**. Saat lisätietoja kaksoisnapsauttamalla sovellusryhmää.

![Sovellusryhmän ominaisuudet](./media/OPSetup_05_ApplicatioGroupProperties.png)

Varmista vielä lopuksi, että voit käyttää AD FS -palvelun OpenID-määrityksen URL-osoitetta **AOSNodeType**-tyypin Service Fabric -solmua siirtymällä `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` selaimeen. Jos näyttöön avautuva sanoma ilmoittaa, että sivusto ei ole turvallinen, et ole lisännyt AD FS SSL -varmennetta Luotetut varmenteiden päämyöntäjät -säilöön. Tämä vaihe käsitellään AD FS -käyttöönotto-oppaassa. Jos URL-osoitteen käyttö onnistuu, palautettava JavaScript Object Notation (JSON) -tiedosto sisältää AD FS -määrityksen ja näet, että AD FS -palvelun URL-osoite on luotettava.

Tämän vaiheen myötä infrastruktuuri on määritetty. Seuraavissa osissa käsitellään, miten siirrytään [LCS:ään](https://lcs.dynamics.com) määrittämään yhdistin ja ottamaan Dynamics 365 for Finance and Operations -ympäristö käyttöön.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Yhdistimen määrittäminen ja asentaminen paikallisesti paikalliseen agenttiin

1. Kirjaudu [LCS:ään](https://lcs.dynamics.com/) ja avaa paikallinen käyttöönottoprojekti.
2. Valitse valikossa **Projektin asetukset**.

    ![Projektiasetukset-komento](./media/OPSetup_06_ProjectSettings.png)

3. Valitse **Paikalliset yhdistimet**
4. Luo uusi yhdistin valitsemalla **Lisää**.
5. Lataa agentin asennusohjelma **Määritä isäntäinfrastruktuuri** -välilehdessä.

    ![Agentin asennusohjelman latauspainike Määritä isäntäinfrastruktuuri -välilehdessä](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Varmista, zip-tiedoston esto on kumottu. Napsauta tiedostoa hiiren kakkospainikkeella, valitse **Ominaisuudet** ja valitse lopuksi **Kumoa esto**.
7. Pura agentin asennusohjelman zip-tiedosto yhdessä **OrchestratorType**-tyyppisessä Service Fabric -solmussa.
8. Anna määritysasetukset **Määritä agentti** -välilehdessä.
9. Tallenna määrity ja lataa sitten localagent-config.json-määritystiedosto valitsemalla **Lataa määritykset**.

    ![Määritä agentti -välilehden Lataa määritykset -painike](./media/OPSetup_08_DownloadConfigurations.png)

10. Kopioi localagent-config.json-tiedosto koneeseen, jossa agentin asennuspaketti on.
11. Suorita seuraava komento komentokehoteikkunassa siirtymällä kansioon, jossa agentin asennusohjelma on.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > Tämän komennon suorittavalla käyttäjällä on oltava OrchestratorData-tietokannan **db\_owner**-käyttöoikeudet.
    
12. Kun paikallinen agentti on asennettu, siirry takaisin paikalliseen yhdistimeen LCS:ssä.
13. Napsauta **Vahvista asetukset**-välilehdessä **Sanoma-agentti**-painiketta. Tällä voidaan testata LCS-yhteydet paikalliseen agenttiin. Kun yhteys on muodostettu, sivu muistuttaa alla olevaa kuvaa.

     ![Tarkista agentti](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Dynamics 365 for Finance and Operations (paikallinen) -ympäristön käyttöönotto

1. Siirry LĆS:ssä paikalliseen projektiin, valitse ensin **Ympäristö**, sitten **Eristysympäristö** ja lopuksi **Määritä**.
2. Valitse **Ympäristötopologia** ja käynnistä käyttöönotto ohjatun toiminnon ohjeiden mukaan.
3. Paikallinen agentti poimii käyttöönottopyynnön, käynnistää käyttöönoton ja ilmoittaa LCS:lle, kun se on valmis.

