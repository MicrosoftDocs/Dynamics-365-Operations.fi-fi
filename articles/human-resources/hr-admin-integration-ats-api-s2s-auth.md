---
title: Palvelimien välinen todennus ATS-integroinnin ohjelmointirajapinnalle
description: Tässä ohjeaiheessa kuvataan, miten palvelimien välinen todennus määritetään integraatioille Dynamics 365 Human Resourcesin hakijoiden seurantajärjestelmän (ATS) integraation ohjelmointirajapinnalle.
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aabe2cd9fd962c8f1c5bbf7fe911e7c6ceeae082f61fc4359aaf7bf197531eff
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778076"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>Palvelimien välinen todennus ATS-integroinnin ohjelmointirajapinnalle

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa kuvataan, miten palvelimien välinen todennus määritetään sovellusintegraatioille Dynamics 365 Human Resourcesin hakijoiden seurantajärjestelmän (ATS) integraation ohjelmointirajapinnalle. On olemassa muutama suojaustaso, joita täytyy hallita, jotta palveluobjekti voi käyttää Microsoft Dataverse -virtuaalitaulukkoa ja siihen liittyviä tietoja. Käyttäjälle on myönnettävä Dataverse-virtuaalitaulukon käyttöoikeus Microsoft Power Platformissa sekä Dynamics 365 Human Resources -tietojen käyttöoikeus.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Käyttöoikeuden myöntäminen Dataverse-virtuaalitaulukoihin Power Platformissa

Ensimmäinen vaihe Dataverse-virtuaalitaulukoiden käyttöoikeuksien myöntämiseksi Power Platformissa on määrittää sovelluksesi Power Platformissa todennusta varten Dataverse-virtuaalitaulukon päätepisteille. Nämä vaiheet on kuvattu [Microsoft Dataverse -kehittäjän oppaassa](/powerapps/developer/data-platform).

  - Yhden vuokraajan sovelluksen rekisteröinnit: [Yhden vuokraajan palvelimien välisen todennuksen käyttäminen](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - Usean vuokraajan sovelluksen rekisteröinnit: [Usean vuokraajan palvelimien välisen todennuksen käyttäminen](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>Käyttöoikeusroolin luominen ATS-integraatioille

Yksi sovelluskäyttäjän luomisen vaiheista on kohdistaa käyttäjä käyttöoikeusrooliin, joka määrittää päätepisteet sisältävän sovelluksen käyttöoikeudet. Tämä on vaihe 7 [sovelluskäyttäjän luomisessa](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) yhden vuokraajan sovellusrekisteröinnille ja [käyttöoikeusroolin luomisessa sovelluskäyttäjälle](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) usean vuokraajan rekisteröinneissä. 

Roolilla, johon kohdistat sovelluskäyttäjän, tulisi olla pääsy ATS-integraatiollesi käytettyihin tietoyksiköihin. Tätä roolia ei ole valmiina, joten sinun täytyy luoda uusi käyttöoikeusrooli. Uusi rooli voidaan luoda noudattamalla [Käyttöoikeusroolin luominen](/power-platform/admin/create-edit-security-role#create-a-security-role) -osiossa kuvattuja ohjeita.

Uudelle roolille täytyy kohdistaa asiaankuuluvat käyttöoikeudet, vähintäänkin seuraaviin uuden roolin **Mukautetut yksiköt** -välilehdissä oleviin entiteetteihin. Huomaa, että sinun täytyy ehkä lisätä muita yksiköitä, jos integrointi käyttää laajempia sovellustietoja. Kun uusi rooli on luotu, sen voi kohdistaa sovelluskäyttäjälle.

  - Perustyöntekijä (mshr)
  - Palkattava hakija (mshr)
  - Todistettu osaaminen (mshr)
  - Todistuksen tyyppi (mshr)
  - Yhtiö
  - Kompensaatiotyötehtävä (mshr)
  - Kompensaatiotyötyyppi (mshr)
  - Maa/alueet (mshr)
  - Osasto (mshr)
  - Koulutusosaaminen (mshr)
  - Koulutusaste (mshr)
  - Koulutusalat (mshr)
  - Koulutusvaatimukset (mshr)
  - Tunnus (mshr)
  - Tunnustyyppi (mshr)
  - Oppilaitos (mshr)
  - Myöntäjätaho (mshr)
  - Työn kompensaatio (mshr)
  - Työt (mshr)
  - Koulutustaso (mshr)
  - Osapuolen yhteyshenkilöt (mshr)
  - Ihmiset (mshr)
  - Henkilökohtaiset osoitteet (mshr)
  - Henkilön seulonta (mshr)
  - Toimityyppi (mshr)
  - Toimet V2 (mshr)
  - Ammattikokemuksen osaaminen (mshr)
  - Luokitustaso (mshr)
  - Arviointimallit (mshr)
  - Syykoodit (mshr)
  - Työhönottopyyntö (mshr)
  - Työhönottopyynnön sijainti (mshr)
  - Työhönottopyynnön toimi (mshr)
  - Työhönottopyynnön taidot (mshr)
  - Seulontatyyppi (mshr)
  - Taidon osaaminen (mshr)
  - Osaamisalueet (mshr)
  - Tittelit (mshr)
  - Sotaveteraanitila (mshr)
  - Työntekijä (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Sovelluksen käyttöoikeuksien myöntäminen henkilöstöhallinnon tietoihin

Toinen vaihe on varmistaa, että sovellukselle on myönnetty tarvittavat käyttöoikeudet henkilöstöhallinnon tietoihin linkittämällä se käyttäjään Human Resources -sovelluksessa. Sovelluskäyttäjän osalta palvelimien väliset kutsut Dataverse-virtuaalitaulukoiden kautta tehdään Dataversessa toimintoa kutsuvan käyttäjän (sovelluksen) tunnuksen kontekstissa. Virtuaalitaulukoiden sovitinpalvelu etsii sitten liitetyn käyttäjän Human Resources -sovelluksesta ja suorittaa kyselyn käyttäjän kontekstissa. Tämä tarkoittaa, että käyttäjä on luotava Human Resources -sovelluksessa ja hänelle täytyy kohdistaa oikeat roolit, jotta integroitavalle sovellukselle voidaan myöntää käyttöoikeudet sen tarvitsemiin tietoihin.

Human Resources -käyttäjälle täytyy myös kohdistaa oikeat käyttöoikeudet Human Resources -sovelluksen tietoihin. Käytettävissä oleva **Työhönottosovellus** (HcmRecruitingIntegrator) -rooli sisältää ensisijaisten yksiköiden käyttöoikeudet, jotka tarvitaan työhönottotietojen integroinnissa. Tämä rooli voidaan kohdistaa sovelluskäyttäjälle **Käyttäjät**-sivulta tietojen asiaankuuluvien käyttöoikeuksien myöntämiseksi. Lisätietoja Human Resources -käyttöoikeusrooleista on kohdassa [Rooliperustainen suojaus](/fin-ops-core/dev-itpro/sysadmin/role-based-security).

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>Uuden käyttäjän määrittäminen asiaankuuluvilla käyttöoikeuksilla

Määritä uusi käyttäjä asiaankuuluvilla käyttöoikeuksilla noudattamalla seuraavia ohjeita:

  1. Avaa **Käyttäjät**-sivu Human Resources -sovelluksesta ja valitse **Uusi**.
  2. Kirjoita uuden sovelluskäyttäjän **Käyttäjätunnus** ja **käyttäjänimi**. Voit syöttää esimerkiksi "RecruitingIntegration".

      > [!NOTE]
      > Jos sovelluksella ei ole Microsoft Azure Active Directory (Azure AD) -käyttäjätiliä tai sähköpostiosoitetta, voit syöttää käyttäjän Sähköpostiosoite- ja Sähköpostipalvelu-kenttiin esimerkiksi "RecruitingApp".

  3. Valitse **Käyttäjän roolit** -pikavälilehdestä **Määritä roolit** -toiminto.
  4. Valitse **Määritä rooleja käyttäjälle** -ruudusta **Työhönottosovellus** ja valitse **OK**.
  5. Tallenna uusi käyttäjätietue.

### <a name="link-the-new-human-resources-user-to-the-application"></a>Uuden Human Resources -käyttäjän linkittäminen sovellukseen

Kun käyttäjä on luotu, sovellukselle täytyy luoda tietue **Azure Active Directory -sovellukset** -lomakkeesta, jotta sovellus voidaan linkittää Human Resources -käyttäjään.

  1. Avaa **Azure Active Directory -sovellukset** -lomake ja valitse **Uusi**.
  2. Syötä **Asiakastunnus**-kenttään sovellukselle luodun sovelluskäyttäjän asiakastunnus.
  3. Syötä **Nimi**-kenttään integroitavan sovelluksen nimi.
  4. Valitse **Käyttäjätunnus**-kentästä työhönoton integroinnille luotu uusi Human Resources -käyttäjä.
  5. Tallenna uusi tietue.

Nyt sovelluksella on pääsy Human Resources -tietoihin, rajoitettuna vain työhönottosovelluksen integraatioille tarvittaviin tietoihin.

## <a name="see-also"></a>Lisätietoja

[Ehdokkaiden työhönotto](hr-personnel-recruit.md)<br>
[Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse -verkkoliittymän käyttäminen](/powerapps/developer/data-platform/webapi/overview)<br>
[Asetusjoukkojen luominen ja päivittäminen verkkoliittymän avulla](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
