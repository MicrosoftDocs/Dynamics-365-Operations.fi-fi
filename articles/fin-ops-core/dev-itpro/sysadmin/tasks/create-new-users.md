---
title: Uusien käyttäjien luominen
description: Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b994473b4535c255f87551a6d97e197516fc2a9c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745834"
---
# <a name="create-new-users"></a>Uusien käyttäjien luominen

[!include [banner](../../includes/banner.md)]

Ennen kuin Finance and Operations -sovellukset ovat käytettävissä, käyttäjä on lisättävä **Käyttäjät**-sivulle (**Järjestelmän hallinta \> Käyttäjät \> Käyttäjät**). Käyttäjät voivat organisaation sisäisiä työntekijöitä tai ulkoisia asiakkaita ja toimittajia. Käyttäjät voidaan tuoda tai lisätä manuaalisesti. Kaikilla käyttäjillä on oltava oikeanlaiset käyttöoikeudet.

Lisätietoja Finance and Operations -sovellusten käyttöoikeuksien ostamisesta ja myöntämisestä on [Microsoft Dynamics 365:n käyttöoikeusoppaassa](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Käyttöoikeuden määrittäminen käyttäjälle
Järjestelmänvalvojat voivat [määrittää käyttöoikeuksia käyttäjille](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [Microsoft 365 -hallintakeskuksessa](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Ulkoisen käyttäjän lisääminen Azure AD:ssa ja käyttöoikeuden määrittäminen 
Ulkoisien käyttäjien on oltava mukana vuokraajahakemistossa (Azure Active Directory (Azure AD)), jotta heille voidaan määrittää käyttöoikeuksia. Nämä ulkoiset käyttäjät on lisättävä vuokraajalle Azure AD:ssä vieraskäyttäjinä, minkä jälkeen käyttäjille on määritettävä asianmukaiset käyttöoikeudet. Finance and Operations -sovellusten edellytyksenä on, että vieraskäyttäjän yritys käyttää Azure AD:ta. Lisätietoja on kohdassa [Lisää Azure Active Directoryn B2B-yhteistyön käyttäjiä Azure-portaaliin](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="import-new-users-from-azure-ad"></a>Uusien käyttäjien tuominen Azure AD:sta 
1. Valitse **Järjestelmän hallinta** \> **Käyttäjät** \> **Käyttäjät**.
2. Valitse toimintoruudussa **Tuo käyttäjiä**.
3. Valitse tuotavat käyttäjät. Luettelo Azure AD -käyttäjät, jotka eivät ole tällä hetkellä käyttäjiä tässä ympäristössä.
4. Valitse **Tuo käyttäjiä**.
5. Valitse **Sulje**.

> [!NOTE]
> **Yritys**-kentän arvo perustuu järjestelmänvalvojan nykyisen istunnon yritykseen. Tuonnin jälkeen on määritettävä soveltuvat roolit ja organisaatiot. Lisätietoja on kohdassa [Käyttäjien määrittäminen käyttöoikeusrooleille](assign-users-security-roles.md). Ehdollisesti voidaan myös edellyttää, että käyttäjään liitetään **Henkilö** ja että käyttäjän asetukset, kuten kieli, päivitetään.

## <a name="manually-add-a-new-user"></a>Uuden käyttäjän lisääminen manuaalisesti
1. Valitse **Järjestelmän hallinta** \> **Käyttäjät** \> **Käyttäjät**.
2. Valitse toimintoruudussa **Uusi**.
3. Anna käyttäjän yksilöivä tunnus **Käyttäjätunnus**-kenttään.   
4. Kirjoita käyttäjän nimi **Käyttäjän nimi** -kenttään toimittajan nimi.  
5. **Palvelu**-kenttä:
 - Käytä sisäisille käyttäjille oletusarvoa. Esimerkki: Azure AD -vuokraaja, jolla etuliitteenä https://sts.windows.net/.  
 - Anna muille kuin Azure AD -käyttäjille, kuten Palvelusta palveluun -tileille, perustekstiarvo. Esimerkki: Ei saatavana. Tämä arvo auttaa estämään virheelliset todennuskutsut, jotka voivat aiheuttaa virheitä, jos käytetty käyttäjätietopalvelun arvo on virheellinen.  
 - Lisää ulkoisten käyttäjien tai vieraskäyttäjien Azure AD -vuokraajan nimi merkkijonon https://sts.windows.net/ jälkeen.
6. Kirjoita **Sähköpostiosoite**-kenttään täydellinen sähköpostiosoite tai käyttäjätunnus.  
7. Valitse **Yritys**-kentässä käyttäjän oletusaloitusyritys. 
8. Valitse **Tallenna**.

Käyttäjätietopalvelun ja telemetriatunnuksen arvot päivitetään [Microsoft graph](https://docs.microsoft.com/graph/overview) -kutsun perusteella, kun käyttäjätietue tallennetaan. Telemetriatunnus perustuu käyttäjän objektitunnukseen tai suojaustunnukseen (SID) Azure AD:ssa.

> [!NOTE]
> Soveltuvat rooli ja organisaatiot on määritettävä sen jälkeen, kun käyttäjä on lisätty. Lisätietoja on kohdassa [Käyttäjien määrittäminen käyttöoikeusrooleille](assign-users-security-roles.md). Ehdollisesti voidaan myös edellyttää, että käyttäjään liitetään **Henkilö** ja että **Käyttäjän asetukset**, kuten kieli, päivitetään.

## <a name="change-a-user-id"></a>Käyttäjätunnuksen vaihtaminen
Käyttäjätunnuksen vaihtaminen edellyttää, että avain nimetään uudelleen tietokannassa. Kun käyttäjätunnus vaihdetaan tällä menetelmällä, kaikki liittyvät käyttäjän asetukset muokataan käyttämään uutta käyttäjätunnusta. Esimerkiksi **SysLastValue**-taulukon käyttötiedot päivitetään käyttämään uutta käyttäjätunnusta.

> [!NOTE]
> Käyttäjätunnus on käyttäjätietotaulun ensisijainen avain. Aiemmin luotujen käyttäjien ensisijaisen avaimen nimeäminen uudelleen vie jonkin aikaa, koska myös kaikki viittaukset avaimeen päivitetään tietokannassa. 

1. Valitse **Järjestelmänvalvojat \> Käyttäjät \> Käyttäjät**.
2. Valitse ensin käyttäjä luettelossa ja valitse sitten **Vaihtoehdot \> Tietueen tiedot**.
3. Valitse **Nimeä uudelleen**.
4. Anna käyttäjätunnukselle uusi ja yksilöivä arvo ja valitse sitten **OK**: 
5. Vahvista valitsemalla **Kyllä**.

## <a name="additional-resources"></a>Lisäresurssit

Lisätietoja yritystenvälisten käyttäjien käyttöönottovaihtoehdoista on kohdassa [Yritystenvälisten käyttäjien vieminen Azure AD:hen](../implement-b2b.md).

Lisätietoja esimääritetyistä järjestelmätileistä on kohdassa [Esimääritetyt järjestelmätilit](../pre-configured-system-accounts.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]