---
title: Sähköisten allekirjoitusten määrittäminen
description: Määritä sähköiset allekirjoitukset tällä menettelyllä.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ad4ef067841511e235dcf538c720b72283d31c3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177619"
---
# <a name="set-up-electronic-signatures"></a>Sähköisten allekirjoitusten määrittäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Määritä sähköiset allekirjoitukset tällä menettelyllä. Sähköisellä allekirjoituksella vahvistetaan uuden tietojenkäsittelyprosessin aloittavan tai prosessin hyväksynnän aloittavan henkilön henkilöllisyys. Tämän menettelyn luomisessa käytetty esittely-yritys on DAT.


## <a name="enable-the-electronic-signature-configuration-key"></a>Ota sähköisen allekirjoituksen määritysavain käyttöön
1. Valitse Järjestelmän hallinta > Asetukset > Käyttöoikeuden konfiguraatio.
2. Laajenna Hallinto-vaihtoehto puussa.
    * Tarkista, että Sähköinen allekirjoitus -valintaruutu on valittu.  
    * Jos Sähköinen allekirjoitus -valintaruutua ei ole valittu, ota ylläpitotila käyttöön. Ylläpitotila voidaan ottaa käyttöön tässä ympäristössä suorittamalla ylläpitotyö Lifecycle Servicesistä tai käyttämällä paikallisesti Deployment.Setup-työkalua.  
3. Sulje sivu.

## <a name="set-up-electronic-signature-parameters"></a>Sähköisten allekirjoitusten parametrien määrittäminen
1. Valitse Organisaation hallinto > Asetukset > Sähköinen allekirjoitus > Sähköisen allekirjoituksen parametrit.
2. Valitse Muokkaa.
3. Kirjoita Ilmoitus-kenttään arvo.
    * Kirjoita ilmoitus, jonka allekirjoittajat saavat allekirjoitusta pyydettäessä. Voit käyttää mitä tahansa tekstiä. Yleensä tämä teksti kertoo käyttäjälle, mitä tiedoston sähköinen allekirjoitus tarkoittaa.  
    * Jos haluat antaa huomautustekstin muilla kielillä, valitse Käännökset.  
4. Valitse Tallenna.
5. Sulje sivu.

## <a name="set-up-reason-codes-for-electronic-signatures"></a>Syykoodien määrittäminen sähköisille allekirjoituksille
1. Valitse Organisaation hallinto > Asetukset > Sähköinen allekirjoitus > Sähköisen allekirjoituksen syykoodit.
2. Valitse Uusi.
    * Syykoodit on määritettävä ennen sähköisten allekirjoitusten käyttöä. Voimassa oleva syykoodi tarvitaan tiedostoa allekirjoitettaessa.     Allekirjoittaja valitsee syykoodin, joka ilmaisee sähköisen allekirjoituksen syyn. Syykoodin avulla voi ilmaista esimerkiksi virallisen hyväksynnän.  
3. Kirjoita Syykoodi-kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
    * Anna tarvittaessa lisää syykoodeja.  
5. Valitse Tallenna.
6. Sulje sivu.

## <a name="require-electronic-signatures-for-existing-processes"></a>Sähköisten allekirjoitusten edellyttäminen aiemmin luoduissa prosesseissa
1. Valitse Organisaation hallinto > Asetukset > Sähköinen allekirjoitus > Sähköisen allekirjoituksen vaatimukset.
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse prosessi, jossa käytettävä sähköisiä allekirjoituksia.  
3. Valitse Allekirjoitus vaaditaan -valintaruutu tai poista sen valinta.
    * Toista nämä vaiheet jokaisen sähköistä allekirjoitusta edellyttävän prosessin jälkeen.  
4. Valitse Tallenna.

## <a name="create-a-custom-requirement-for-electronic-signatures"></a>Sähköisten allekirjoitusten mukautetun edellytyksen luominen
1. Valitse Uusi.
2. Valitse Allekirjoitus vaaditaan -valintaruutu tai poista sen valinta.
3. Kirjoita sähköistä allekirjoitusta edellyttävän prosessin nimi Nimi-kenttään.
4. Avaa haku napsauttamalla Taulun nimi -kentässä avattavan valikon painiketta.
5. Etsi ja valitse luettelosta taulu, johon allekirjoitusta edellyttävät tiedot on tallennettu.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Avaa haku napsauttamalla Kentän nimi -kentässä avattavan valikon painiketta.
8. Etsi ja valitse luettelossa se taulun kenttä, jota haluat seurata.
9. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Määritä, milloin allekirjoitus vaaditaan.     Valitse Aina, jos allekirjoitus vaaditaan kentän tietojen muuttuessa.     Valitse Vain, jos allekirjoitus vaaditaan vain tietyissä tilanteissa. Jos valitset Vain, sinun on valittava jokin seuraavista vaihtoehdoista: Kun tietue lisätään, Kun tietue päivitetään tai Kun tietue poistetaan.  
10. Valitse Tallenna.
11. Sulje sivu.

