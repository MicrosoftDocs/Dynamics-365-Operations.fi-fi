---
title: "Tietojen päivitys eristysympäristössä"
description: "Tässä ohjeaiheessa käsitellään tietojen päivityksen suorittamista AX 2012:sta Dynamics 365 Finance and Operationsiin eristysympäristössä."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: fi-fi
ms.lasthandoff: 06/15/2017

---

# Tietojen päivitys eristysympäristössä
<a id="data-upgrade-in-a-sandbox-environment" class="xliff"></a>

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

Tämän tehtävän tulos on päivitetty tietokanta, jota voit käyttää eristysympäristössä. Eristysympäristössä yrityskäyttäjät ja toimintotiimin jäsenet voivat vahvistaa sovelluksen toimivuuden. Tämä toiminto sisältää mukautuksia ja tietoja, jotka on siirretty Microsoft Dynamics AX 2012:sta.

Suosittelemme, että suoritat tietojen päivitysprosessin kehitysympäristössä ennen kuin käytät sitä jaetussa eristysympäristössä, koska tämä lyhentää kokonaisaikaa, jota onnistunut tietojen päivitys edellyttää. Lisätietoja on kohdassa [Tietojen päivitys kehitysympäristössä](prepare-data-upgrade.md).

## Eristysympäristössä tehtävän päivitysprosessin yhteenveto
<a id="overview-of-the-sandbox-data-upgrade-process" class="xliff"></a>

Ennen kuin aloitat tietojen päivityksen eristysympäristössä, olet päivittänyt tiedot kehitysympäristössä kohdan [Tietojen päivitys kehitysympäristössä](prepare-data-upgrade.md) mukaisesti. Nämä kaksi prosessia ovat hyvin samanlaisia. Niiden suurin ero on se, että eristysympäristössä käytetään Azure Microsoft SQL -tietokantaa tietojen tallentamiseen ja kehitysympäristö käyttää Microsoft SQL Serveriä. Tämä tekninen ero tietokannan tasolla edellyttää tietojen päivitysmenettelyä muuttamista hieman eristysympäristössä, koska AX 2012:n tietokannan esiintymän varmuuskopiota ei voida pelkästään palauttaa SQL Databaseen.

![Eristysympäristön tietojen päivitysprosessi](./media/data-upgrade-sandbox.png)

Seuraavassa on päivitysprosessin ylätason vaiheet.

1. Luo AX 2012 -tietokannan kopio. On erittäin suositeltavaa käyttää kopiota, koska vietävästä kopiosta pitää poistaa joitain objekteja.
2. Vie kopioitu tietokanta bacpac-tiedostoon maksuttomalla SQL Server-työkalulla, jonka nimi on SQLPackage.exe. Tämän työkalun avulla saadaan erikoistyyppinen tietokannan varmuuskopio, jotka voidaan tuoda SQL-tietokantaan.
3. Lataa bacpac-tiedosto Azure-tallennustilaan.
4. Lataa bacpac-tiedosto Application Object Server (AOS) -tietokoneeseen eristysympäristössä ja tuo se SQLPackage.exen avulla. Palauta SQL-tietokannan käyttäjät suorittamalla komentosarja tuodusta tietokannasta.
5. Suorita tietojen päivitys tuodusta tietokannassa suorittamalla MajorVersionDataUpgrade.zip-paketti.

## Luo AX 2012 -tietokannan kopio
<a id="create-a-copy-of-the-ax-2012-database" class="xliff"></a>

AX 2012: n tietokannasta on luotava kopio, kun päivität, koska tietokannasta pitää poistaa joitain objekteja. Näihin objekteihin kuuluu mitä tahansa Microsoft Windows-todennuksen käyttäjiä. Nämä muutokset tekevät muunnetusta tietokannasta käyttökelvottoman AX 2012:ssa. Tässä vaiheessa luot kopion tietokannasta ja poistat nämä objektit.

Tämän vaiheen suorittaa tietokannan järjestelmänvalvoja (DBA) tai henkilö, jolla on vastaavat tiedot ja kokemus.

Jotta tietokannasta voidaan luoda kopio, tee alkuperäisen tietokannan varmuuskopio ja palauta se uudella nimellä. Varmista, että tilaa on riittävästi molemmille tietokannoille. Voit luoda kopion toiselle palvelimelle. SQL-palvelininstanssin versio, joka suorittaa tietokannan, ei ole merkityksellinen.

Tässä on esimerkki koodista, joka luo tietokannasta kopion. Tätä esimerkkiä pitää muokata vastaamaan omia tietokantanimiä.

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

Kun kopio on luotu, suorita seuraavat Transact SQL-(T SQL) -komentosarjat sille.
TEHTÄVÄ 

### Vie kopioitu tietokanta bacpac-tiedostoon
<a id="export-the-copied-database-to-a-bacpac-file" class="xliff"></a>

Vie kopioitu tietokanta bacpac-tiedostoon maksuttomalla SQL Server-työkalulla. Tämän vaiheen suorittaa järjestelmänvalvoja tai tiimijäsen, jolla on vastaavat tiedot.

On tärkeää, että asennat uusimman SQL Server Management Studion version ennen kuin aloitat tämän vaiheen. Vaikka SQLPackage on käytössä Management Studiossa aiemmissa versioissa, mutta se ei toimi oikein tässä vaiheessa, ellet ensin asenna uusinta versiota.

Tämä vaihe on tärkeä, koska vienti on pitää tehdä uudelleen käyttökatkoaikana ennen käyttöönotto. Seuraavassa on muutamia vinkkejä:

- Bacpac-prosessi on erittäin I/O- ja suoritinintensiivinen. Suorita vienti tehokkaalla tietokoneella.
- SQLPackage on suoritettava paikallisesti tietokoneessa, jossa tietokanta sijaitsee. SQLPackage ei pidä suorittaa paikallisessa kannettavassa tietokoneessa, joka liitetään tietokoneeseen, jossa tietokanta sijaitsee, koska tämä toiminto käyttää paljon verkkoresursseja.

Avaa seuraavaksi **komentokehote**-ikkuna järjestelmänvalvojana ja suorita seuraavat komennot.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

Seuraavassa on selitetty parametrit:

- **ssn** (source server name) – SQL Serverin nimi, josta tiedot viedään. Tehtävää prosessia varten tämä parametrin määrityksenä on aina oltava **localhost**.
- **sdn** (lähdetietokannan nimi) – Vietävän tietokannan nimi.
- **tf** (target file) – Tiedoston, johon tiedot viedään, polku ja nimi. Kansio on jo olemassa, mutta prosessi luo tiedoston.
- **/p:CommandTimeout** – Aikakatkaisuarvo kyselyä kohti. Tämä parametri mahdollistaa suurempien taulukoiden viennin ilman aikakatkaisua.

### Bacpac-tiedoston lataaminen Azure-tallennustilaan
<a id="upload-the-bacpac-file-to-azure-storage" class="xliff"></a>

Lataa bacpac-tiedosto Azure-tallennustilaan. Katso UsingStorageExplorer.docx-TEHTÄVÄ.

### Bacpac-tiedoston tuominen SQL-tiedostoon
<a id="import-the-bacpac-file-into-sql-database" class="xliff"></a>

Tässä vaiheessa tuot viedyn bacpac-tiedoston SQL-tietokantaesiintymään, jota eristysympäristö käyttää. Sinun on asennettava ensin Management Studion uusin versio eristettyyn AOS-tietokoneeseen. Tiedosto tuodaan sitten SQLPackage.exe-työkalun avulla.

Nämä tehtävät suoritetaan suoraan AOS-tietokoneessa eristysympäristössäsi, koska palomuurin säännöt rajoittavat SQL-tietokantaesiintymään pääsyä. Kuitenkin käyttämällä AOS-tietokonetta saat sinne pääsyn.

Vientivaihe puolestaan edellyttää uusinta Management Studio -versiota ennen kuin aloitat tuomisen. Tämä vaihe ei toimi vanhalla versiolla.

Suorituskyvyn parantamiseksi suosittelemme, että sijoitat bacpac tiedoston D-asemaan AOS-tietokoneessa. Azure-virtuaalikoneissa (VM) D on fyysinen levy, jonka suorituskyky on suurempi kuin muilla käytettävissä olevilla levyillä.

Avaa **komentokehote**-ikkuna järjestelmävalvojana ja suorita seuraavat komennot.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

Seuraavassa on selitetty parametrit:

- **tsn** (target server name) – SQL Azure -palvelimen nimi, johon tiedot tuodaan. Nimi löytyy LCS:stä. Lisää sen päätteeksi **.database.windows.net**.
- **tdn** (target database name) – Tietokannan nimi, johon tiedot tuodaan. Tietokanta ei saa vielä olla olemassa. Tuontiprosessi luo sen.
- **sf** (source file) – Tiedostopolku ja -nimi, josta tiedot tuodaan.
- **tp** (target password) – SQL-salasana SQL-kohdetietokantaesiintymässä.
- **tu** (target user) – SQL-käyttäjänimi SQL-kohdetietokantaesiintymälle. Suosittelemme että käytät **sqladmin**. Voit noutaa käyttäjän salasanan LCS-projektista.
- **/p:CommandTimeout** – Aikakatkaisuarvo kyselyä kohti. Tämä parametri mahdollistaa suurempien taulukoiden viennin ilman aikakatkaisua.
- **/p:DatabaseServiceObjective** – Luotavan tietokannan palvelintaso. Voit tarkistaa arvon aiemmin luotua tietokantaa varten Management Studiossa. Napsauta tietokantaa hiiren kakkospainikkeella ja valitse sitten **Ominaisuudet**.

Kun olet suorittanut komennot, näyttöön tulee seuraava varoitus. Voit ohittaa sen.

![Eristyksen virhe](./media/sandbox-2.png)
 
### MajorVersiondataUpgrade.zip-paketin suorittaminen
<a id="run-the-majorversiondataupgradezip-package" class="xliff"></a>

Suorittaa tietojen päivityksen käyttöönottopaketin kohdassa [Tietojen päivittäminen kehitys- tai esittely-ympäristössä](upgrade-data-to-latest-update.md) kuvatulla tavalla.

### Tietokannan kopion päivittäminen kehitysympäristössä
<a id="upgrade-a-copy-of-the-database-in-a-development-environment" class="xliff"></a>

Sama tietokanta kannattaa päivittää kehitysympäristössä. Jos sinulla on käytettävissä kehitysympäristön tietokanta, on helpompi tutkia löytyneitä virheitä päivitetyssä eristysympäristössä.

