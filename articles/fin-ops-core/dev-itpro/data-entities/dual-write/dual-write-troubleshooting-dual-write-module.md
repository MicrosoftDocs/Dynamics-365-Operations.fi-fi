---
title: Finance and Operations -sovellusten kaksoiskirjoitusmoduulin ongelmien vianmääritys
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata Finance and Operations -sovellusten kaksoiskirjoitusmoduulin ongelmia.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172757"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Finance and Operations -sovellusten kaksoiskirjoitusmoduulin ongelmien vianmääritys

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä. Erityisesti se tarjoaa vianmääritystietoja, joiden avulla voit korjata Finance and Operations -sovellusten **kaksoiskirjoitusmoduulin** ongelmia.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Kaksoiskirjoitusmoduulia ei voi ladata Finance and Operations -sovellukseen

Jos **Kaksoiskirjoitus**-sivua ei voi avata valitsemalla **Tietojen hallinta** -työtilassa **Kaksoiskirjoitus**-ruutu, tietojen integrointipalvelu ei todennäköisesti ole toiminnassa. Luo tukipyyntö, joka pyytää tietojen integrointipalvelun uudelleenkäynnistystä.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>Virhe yritettäessä luoda uutta entiteetin yhdistämismääritystä

**Ongelman korjauksen edellyttämät tunnistetiedot:** Azure AD -vuokralaisten hallinta

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität määrittää uuden entiteetin kaksoiskirjoittamista varten:

*Vastauksen tilakoodi ei tarkoita onnistumista: 401 (Luvaton)*

Tämä virhe ilmenee, koska vain Azure AD -vuokralaisen järjestelmänvalvoja voi lisätä uuden entiteetin yhdistämismäärityksen.

Voit korjata ongelman kirjautumalla Finance and Operations -sovellukseen Azure AD -ylläpitäjänä. Sinun on myös mentävä web.PowerApps. comiin ja vahvistaa yhteys uudelleen.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Virhe avattaessa kaksoiskirjoituskäyttöliittymää

Näyttöön saattaa tulla seuraavan kaltainen virhesanoma, kun yrität käyttää **Tietojen hallinta** -työtilan kaksoiskirjoittamista:

*login.microsoftonline.com kieltäytyi muodostamasta yhteyttä.*

Jos haluat korjata ongelman, kirjaudu sisään käyttämällä InPrivate-ikkunaa Microsoft Edgessä, tuntemattoman käyttäjän ikkunaa Chromiumissa tai tuntemattoman käyttäjän ikkunaa Google Chromessa. Sinun on myös avattava kolmannen osapuolen evästeet tai poistettava niiden valinta.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Virhe yhdistettäessä ympäristöä kaksoiskirjoittamista tai uuden entiteetin yhdistämismääritystä varten

**Ongelman korjauksen edellyttämät tunnistetiedot:** Azure AD -vuokralaisten hallinta

Saatat kohdata seuraavan virheen linkittäessäsi tai luodessasi karttoja:

*Vastauksen tilakoodi ei ilmaise onnistumista: 403 (tokenexchange).<br> Istunnon tunnus: \<istuntosi tunnus\><br> Päätehtävän tunnus: \<päätehtäväsi tunnus\>*

Tämä virhe voi ilmetä, jos sinulla ei ole riittäviä oikeuksia yhdistää kaksoiskirjoitukseen tai luoda karttoja. Sinun on käytettävä Azure AD -vuokralaisen järjestelmänvalvojan tiliä, jotta voit linkittää ympäristöjä ja lisätä uusia kohteiden yhdistämismäärityksiä. Asennuksen jälkeen voit kuitenkin käyttää muuta kuin järjestelmänvalvojan tiliä tilan tarkkailemiseen ja yhdistämismääritysten muokkaamiseen.

## <a name="error-when-you-stop-the-entity-mapping"></a>Virhe yritettäessä pysäyttää entiteetin yhdistämismääritystä

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität pysäyttää entiteetin yhdistämismääritystä:

*\[Kielletty\], \[{"status": 403, "lähde":"","sanoma":"Virhe tunnuksen vaihdossa: Käyttäjällä ei ole oikeutta käyttää yhteyttä dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Etäpalvelin palautti virheen: (403) kielletty.*

Tämä virhe ilmenee, kun linkitetty Common Data Service -ympäristö ei ole käytettävissä.

Voit korjata ongelman luomalla pyynnön tietojen integrointitiimille. Liitä verkon jäljitys, jotta tietojen integrointiryhmä voi merkitä karttojen tilaksi **Ei käynnissä** taustalla.
