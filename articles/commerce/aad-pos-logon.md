---
title: Azure Active Directory -todennuksen määrittäminen myyntipistekirjautumisessa
description: Tässä artikkelissa kerrotaan, miten Azure Active Directory määritetään todennusmenetelmäksi Microsoft Dynamics 365 Commerce -myyntipisteessä.
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 47da2c78cef2bbee324fbc2202898fbabd927c4d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853925"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>Azure Active Directory -todennuksen määrittäminen myyntipistekirjautumisessa

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Azure Active Directory (Azure AD) määritetään todennusmenetelmäksi Microsoft Dynamics 365 Commerce -myyntipisteessä.

Vähittäismyyjät, jotka käyttävät Dynamics 365 Commercea yhdessä muiden Microsoftin pilvipalveluiden kanssa, kuten Microsoft Azure, Microsoft 365 ja Microsoft Teams, yleensä haluavat käyttää Azure AD:tä keskitettyä hallintaa varten suojattuun ja sujuvaan kirjautumiseen sovelluksissa. Jotta Azure AD -todennusta voi käyttää Commercen myyntipisteelle, todennusmenetelmäksi on ensin määritettävä Azure AD Commerce-pääkonttorisovelluksessa.

## <a name="configure-pos-authentication-method"></a>Myyntipisteen todennusmenetelmän määrittäminen

Voit määrittää myyntipisteen todennusmenetelmän Commerce-pääkonttorisovelluksessaa seuraavasti.
    
1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit** ja valitse muutettava toimintoprofiili.
1. **Myyntipisteen henkilöstön sisäänkirjaus** -osasta **Toiminnot**-pikavälilehdellä haluamasi todennusmenetelmä avattavasta **Sisäänkirjauksen todennusmenetelmä** -luettelosta.

    **Sisäänkirjauksen todennusmenetelmässä** on kolme vaihtoehtoa:
    
    - **Henkilöstön tunnus ja salasana** - Tämä oletusasetus edellyttää, että myyntipisteen käyttäjät syöttävät henkilöstötunnuksen ja salasanan kirjautuakseen sisään myyntipisteeseen ja käyttääkseen esimiehen ohitustoimintoa.
    - **Azure AD ilman kertakirjausta** - Tämä asetus edellyttää, että myyntipisteen käyttäjät kirjautuvat sisään myyntipisteeseen ja käyttävät esimiehen ohitustoimintoa Azure AD -tunnistetiedoilla. Kun myyntipisteen asiakasohjelma päivitetään tai avataan uudelleen, myyntipisteen käyttäjän on annettava Azure AD -tunnistetiedot kirjautumista varten uudelleen.
    - **Azure AD kertakirjauksella** - Kun tämä vaihtoehto on valittuna, myyntipisteen käyttäjät voivat kirjautua pilvimyyntipisteeseen (CPOS) aktiivisia Azure AD -tunnistetietoja, joita muut verkkosovellukset käyttävät samassa selaimessa, tai kirjautua Modern POS -myyntipisteeseen (MPOS) käyttäen Windowsiin kirjautuneena Azure AD -tunnistetietoja. Molemmat menetelmät sallivat kirjautumisen tarvitsematta syöttää Azure AD -tunnistetietoja myyntipisteen kirjautumisnäytössä. Myyntipisteen esimiehen ohitustoimintojen käyttäminen edellyttää kuitenkin kirjautumista Azure AD -tunnistetiedoilla.

1. Siirry kohtaan **Retail ja Commerce > Retail ja Commerce IT > Jakeluaikataulu** ja synkronoi viimeisimmät toimintoprofiilin asetukset myyntipisteen asiakkaille suorittamalla **1070 (kanavan konfiguraatio)** -työ.

> [!NOTE]
> - **Azure AD ilman kertakirjausta** -todennusmenetelmä korvaa **Azure Active Directory** vaihtoehdon Commerce-versiossa 10.0.18 ja sitä aiemmissa versioissa.
> - Azure AD -todennus edellyttää aktiivista Internet-yhteyttä, eikä se toimi, kun myynti on offline-tilassa.

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Azure AD -tilien liittäminen myyntipisteen käyttäjiin

Jos haluat käyttää Azure AD:tä myyntipisteen todennusmenetelmämä, sinun on liitettävä Azure AD -tilit Commerce-pääkonttorisovelluksen myyntipistekäyttäjiin. 

Voit liittää Azure AD -tilejä Commerce-pääkonttorisovelluksen myyntipistekäyttäjiin noudattamalla seuraavia ohjeita.
    
1. Valitse **Retail ja Commerce > Työntekijät > Työntekijät** ja avaa työntekijätietue.
1. Valitse toimintoruudussa **Kauppa**-välilehti ja sitten **Ulkoinen tunnus** -kohdassa **Liitä aiemmin luotu tunnus**. 
1. Valitse **Käytä aiemmin määritettyä ulkoista tunnusta** -valintaikkunassa **Hae sähköpostiosoitteen avulla**, anna Azure AD -sähköpostiosoite ja valitse **Hae**.
1. Valitse palautettu Azure AD -tili ja valitse sitten **OK**.

Yllä olevien määritysvaiheiden jälkeen työntekijän tietosivun **Alias**, **Täydellinen käyttäjätunnus**- ja **Ulkoinen alitunnus** -kentät **Kauppa**-välilehdessä täytetään.

Suorita **1060 (Henkilökunta)** -työ kohdassa **Retail ja Commerce > Retail ja Commerce IT > Jakeluaikataulu** synkronoidaksesi viimeisimmät myyntipisteen käyttäjän ja Azure AD -tilin tiedot kanavaan.

> [!NOTE]
> Parhaan käytännön mukaisesti on suositeltavaa, että kun työntekijätiedot, kuten salasana, myyntipisteen käyttöoikeus, liittyvä Azure AD -tili tai työntekijän osoitekirja, on päivitetty Commerce-pääkonttorisovelluksessa, on suositeltavaa suorittaa **1060 (Henkilökunta)** -työ viimeisimpien työntekijätietojen synkronoimiseksi kanavaan. Näin myyntipisteen asiakasohjelma voi hakea oikeat tiedot käyttäjän valtuutusta ja valtuutuksen tarkistusta varten.

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>Myyntipisteen lukitusrekisteri ja uloskirjautuminen Azure AD -todennuksen avulla

Kun myynti on määritetty käyttämään Azure AD -todennusmenetelmää, tapahtuu seuraavaa:

- **Lukitusrekisteri**-toiminto ei ole käytettävissä myyntipistesovelluksessa. 
- **Automaattinen lukitus** -toiminto toimii samoin kuin **Automaattinen uloskirjaus** -toiminto.
- Jos myyntipisteen käyttäjä valitsee **Kirjaudu ulos**, käyttäjää pyydetään kirjautumaan sisään Azure AD -tunnistetiedoilla kun myyntipiste käynnistetään seuraavan kerran riippumatta siitä, onko kertakirjautuminen käytössä.

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Ohitustoimintojen hallinta Azure AD -todennuksella

Kun myyntipiste on määritetty käyttämään Azure AD -todennusta, esimiehen ohitustoiminto avaa valintaikkunan, jossa pyydetään esimiehen käyttäjän Azure AD -käyttöoikeudet. Kun esimiehen kirjautuminen on hyväksytty, esimiehen Azure AD -tunnistetiedot poistetaan ja edellisen käyttäjän Azure AD -tunnistetietoja käytetään myöhemmissä myyntipistetoiminnoissa.

> [!NOTE]
> - Commerce-versioissa 10.0.18 ja sitä aiemmissa versioissa esimiehen ohitustoiminto ei tue Azure AD:tä. Henkilöstötunnus ja salasana ovat pakollisia, vaikka myyntipiste olisi määritetty käyttämään Azure AD -todennusmenetelmää.
> - Kun käytät CPOS:ää Safari-selaimessa Apple iOS -laitteella, sinun on ensin poistettava **Estä ponnahdusikkunat** käytöstä Safari-asetuksissa, jotta esimiehen ohitustoiminto voi käyttää Azure AD -todennusta. 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>Suojauksen parhaat käytännöt Azure AD -pohjaiselle myyntipisteen todentamiselle jaetuissa laitteissa

Useat vähittäismyyjät ovat määrittäneet vähittäismyyntiympäristönsä niin, että useiden käyttäjien on tarpeen käyttää myyntipistesovellusta jaetusta fyysisestä laitteesta. Samalla kun kertakirjaus tarjoaa kätevän ja sujuvan todennusmenetelmän, se voi myös luoda aukon suojauksessa, koska nykyinen myyntipisteen käyttäjä ei välttämättä huomaa, että toisen käyttäjän tunnistetietoja käytetään tapahtumien tai toimintojen suorittamiseen myyntipisteessä. Ennen kuin määrität myyntipisteen käyttämään Azure AD -todennusmenetelmää, on suositeltavaa tarkistaa suojauskäytäntösi ja jaetun laitteen kirjautumisasetukset ja päättää, mikä vaihtoehto sopii parhaiten.

- Jos vähittäismyyntiympäristö käyttää fyysistä kirjautumista varten jaettua tiliä (esimerkiksi paikallista tiliä), on suositeltavaa käyttää **Azure AD ilman kertakirjausta** -vaihtoehtoa. Näin varmistetaan, että kukin myyntipisteen käyttäjä antaa Azure AD -tunnistetietonsa kirjautuessaan myyntipisteeseen.
- Jos vähittäismyyntiympäristö edellyttää, että työntekijät kirjautuvat sisään myyntipisteeseen omalla Azure AD -tilillään ja käytössä on fyysinen laite, on suositeltavaa käyttää **Azure AD kertakirjautuksella** -vaihtoehtoa.

## <a name="additional-resources"></a>Lisäresurssit

[Työntekijän konfiguroiminen](tasks/worker.md)

[Vähittäismyynnin toimintoprofiilin luominen](retail-functionality-profile.md)


[Laajennetun MPOS- ja pilvimyyntipistekirjautumisen määrittäminen](extended-logon.md)

[Suojauksen parhaat käytännöt pilvimyyntipisteelle jaetuissa ympäristöissä](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
