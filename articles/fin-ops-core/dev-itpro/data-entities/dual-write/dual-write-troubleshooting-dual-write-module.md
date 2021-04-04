---
title: Finance and Operations -sovellusten kaksoiskirjoituksen ongelmien vianmääritys
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata Finance and Operations -sovellusten kaksoiskirjoitusmoduulin ongelmia.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 9bff8ad0c5716648dec6eadfb21412a2b17f155e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561223"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Finance and Operations -sovellusten kaksoiskirjoituksen ongelmien vianmääritys

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä. Erityisesti se tarjoaa vianmääritystietoja, joiden avulla voit korjata Finance and Operations -sovellusten **kaksoiskirjoitusmoduulin** ongelmia.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Kaksoiskirjoitusmoduulia ei voi ladata Finance and Operations -sovellukseen

Jos **Kaksoiskirjoitus**-sivua ei voi avata valitsemalla **Tietojen hallinta** -työtilassa **Kaksoiskirjoitus**-ruutu, tietojen integrointipalvelu ei todennäköisesti ole toiminnassa. Luo tukipyyntö, joka pyytää tietojen integrointipalvelun uudelleenkäynnistystä.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Virhe yritettäessä luoda uutta taulukon yhdistämismääritystä

**Tarvittavat tunnistetiedot ongelman korjaamiseksi:** Sama käyttäjä, joka määrittää kaksoiskirjoituksen.

Seuraava virhesanoma voi avautua, kun yrität määrittää uuden taulukon kaksoiskirjoittamista varten. Ainoa käyttäjä, joka voi luoda yhdistämismäärityksen, on käyttäjä, joka määrittää kaksoiskirjoituksen yhteyden.

*Vastauksen tilakoodi ei tarkoita onnistumista: 401 (Luvaton)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Virhe avattaessa kaksoiskirjoituskäyttöliittymää

Näyttöön saattaa tulla seuraavan kaltainen virhesanoma, kun yrität käyttää **Tietojen hallinta** -työtilan kaksoiskirjoittamista:

*login.microsoftonline.com kieltäytyi muodostamasta yhteyttä.*

Jos haluat korjata ongelman, kirjaudu sisään käyttämällä InPrivate-ikkunaa Microsoft Edgessä, tuntemattoman käyttäjän ikkunaa Chromiumissa tai tuntemattoman käyttäjän ikkunaa Google Chromessa. Sinun on myös avattava kolmannen osapuolen evästeet tai poistettava niiden valinta.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Virhe yhdistettäessä ympäristöä kaksoiskirjoittamista tai uuden taulun yhdistämismääritystä varten

**Ongelman korjaava rooli:** Järjestelmän ylläpitäjä sekä Finance and Operations -sovelluksissa ja Dataversessä.

Saatat kohdata seuraavan virheen linkittäessäsi tai luodessasi karttoja:

*Vastauksen tilakoodi ei ilmaise onnistumista: 403 (tokenexchange).<br> Istunnon tunnus: \<your session id\><br> Päätehtävän tunnus: \<your root activity id\>*

Tämä virhe voi ilmetä, jos sinulla ei ole riittäviä oikeuksia yhdistää kaksoiskirjoitukseen tai luoda karttoja. Tämä virhe voi ilmetä myös, jos Dataverse -ympäristö nollautuu ilman kaksoiskirjoituksen linkityksen poistamista. Kuka tahansa käyttäjä, jolla on järjestelmänvalvojan rooli sekä Finance and Operations-sovelluksissa että Dataversessä voi linkittää ympäristöt. Vain kaksoiskirjoitusyhteyden asetusten luonut käyttäjä voi lisätä uusia taulujen yhdistämismäärityksiä. Asennuksen jälkeen kuka tahansa järjestelmänvalvoja, jolla on järjestelmänvalvojan rooli, voi valvoa tilaa ja muokata yhdistämismäärityksiä.

## <a name="error-when-you-stop-the-table-mapping"></a>Virhe yritettäessä pysäyttää taulun yhdistämismääritystä

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität pysäyttää taulujen yhdistämismääritystä:

*\[Kielletty\], \[{"status": 403, "lähde":"","sanoma":"Virhe tunnuksen vaihdossa: Käyttäjällä ei ole oikeutta käyttää yhteyttä dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Etäpalvelin palautti virheen: (403) kielletty.*

Tämä virhe ilmenee, kun linkitetty Dataverse -ympäristö ei ole käytettävissä.

Voit korjata ongelman luomalla pyynnön tietojen integrointitiimille. Liitä verkon jäljitys, jotta tietojen integrointiryhmä voi merkitä karttojen tilaksi **Ei käynnissä** taustalla.

## <a name="error-while-trying-to-start-a-table-mapping"></a>Virhe yritettäessä käynnistää taulun yhdistämismääritystä

Näyttöön voi tulla seuraavankaltainen virhesanoma, kun yrität määrittää yhdistämismäärityksen tilaksi **Käytössä**:

*Tietojen alkuperäistä synkronointia ei voi suorittaa loppuun. Virhe: kaksoiskirjoitusvirhe - laajennuksen rekisteröiminen epäonnistui: kaksoiskirjoitushaun metatietoja ei voi muodostaa. Virheen objektin viitettä ei ole määritetty objektin esiintymälle.*

Tämän virheen korjaus määräytyy virheen syyn mukaan:

+ Jos yhdistämismääritykset ovat riippuvaisia määrityksistä, varmista, että otat käyttöön tämän taulun yhdistämismäärityksen sidonnaiset määritykset.
+ Yhdistämismäärityksestä saattaa puuttua lähde- tai kohdesarakkeet. Jos Finance and Operations -sovelluksen sarake puuttuu, noudata [Puuttuvien taulukkosarakkeiden ongelma yhdistämismäärityksissä](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) -kohdan ohjeita. Jos Dataversen sarake puuttuu, valitse yhdistämismäärityksessä **Päivitä taulut** -painike, jotta sarakkeet täytetään automaattisesti takaisin yhdistämismääritykseen.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]