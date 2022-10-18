---
title: Finance Insightsin määritykset
description: Tässä artikkelissa kerrotaan, millaiset määritysvaiheet järjestelmässä on suoritettava, jotta Finance Insightsin ominaisuuksia voi käyttää.
author: ShivamPandey-msft
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 07edea234839a477802e5cd875620509c8f92d69
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644111"
---
# <a name="configuration-for-finance-insights"></a>Finance Insightsin määritykset

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights yhdistää Microsoft Dynamics 365 Financen toiminnot Dataversen, Azuren ja AI Builderin kanssa. Yhdessä nämä tarjoavat tehokkaat ennustetyökalut organisaatiolle. Tässä artikkelissa kerrotaan, millaiset määritysvaiheet järjestelmässä on suoritettava, jotta Finance Insightsin ominaisuuksia voi käyttää. Tämän artikkelin menettelyjen onnistuminen edellyttää, että käytössä on järjestelmänvalvojan ja järjestelmän mukauttajan käyttöoikeudet [Power Portal -hallintakeskuksessa](https://admin.powerplatform.microsoft.com/), järjestelmänvalvojan käyttöoikeus Dynamics 365 Financessa sekä ympäristöjen luontioikeudet Microsoft Dynamics Lifecycle Servicesissa (LCS).

> [!NOTE]
> Seuraavat Finance Insightsin määrittämismenettelyt koskevat Dynamics 365 Financen versiota 10.0.21 ja sitä uudempia versioita.

## <a name="deploy-dynamics-365-finance"></a>Ota käyttöön Dynamics 365 Finance

Määritä ympäristöt näiden ohjeiden avulla.

1. Luo tai päivitä Dynamics 365 Finance -ympäristö LCS-sovelluksessa. Ympäristö edellyttää, että käytössä on sovelluksen versio 10.0.21 tai sitä uudempi versio.

    > [!NOTE]
    > Ympäristön on oltava korkean käytettävyyden ympäristö. (Tämä ympäristötyyppi tunnetaan myös tason 2 ympäristönä.) Lisätietoja on kohdassa [Ympäristön suunnittelu](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

2. Jos Finance Insightsia määritetään eristysympäristössä, tuotantotiedot on ehkä kopioitava tähän ympäristöön, jotta ennusteet toimisivat. Ennustemallissa käytetään useiden vuosien tietoja ennusteiden luomiseen. Contoso-esittelytiedot eivät sisällä riittävästi historiatietoja ennustemallin kouluttamiseen. 

## <a name="configure-your-azure-ad-tenant"></a>Azure AD -vuokraajan konfiguroiminen

Azure Active Directory (Azure AD) on määritettävä niin, että sitä voidaan käyttää Dataversen ja Microsoft Power Platform -sovellusten kanssa. Määritys edellyttää **ympäristön esimiehen** tai **projektin omistajan** roolin määritettynä käyttäjälle LCS:n **Projektin suojausrooli** -kentässä.

Tarkista, että seuraavat asetukset on tehty:

- Sinulla on **järjestelmänvalvojan** ja **järjestelmän mukauttajan** käyttöoikeus Power Portal -hallintakeskuksessa.
- Finance Insights -lisäosan asentavalla käyttäjällä on Dynamics 365 Finance -lisenssi tai vastaava lisenssi.
- Seuraavat Azure AD -sovellukset on rekisteröity Azure AD:ssä.

    |  Hakemus                             | Sovelluksen tunnus                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |

    Jos haluat tarkistaa, että sovellus on rekisteröity Azure AD:hen, tarkista **Kaikki sovellukset** -luettelo. Lisätietoja on kohdassa [Yrityssovellusten tarkasteleminen](/azure/active-directory/manage-apps/view-applications-portal).
  
    Jos sovellusta ei ole rekisteröity Azure AD:hen, ota yhteyttä tukeen.
  
## <a name="configure-dataverse"></a>Määritä Dataverse

Näitä ohjeita noudattamalla voit määrittää Dataversen Finance Insightsille.

- Avaa ympäristösivu LCS:ssä ja tarkista, että **Power Platform -integrointi** -osa on jo asennettu.

    - Dataverse on jo asennettu; Dataverse-ympäristön nimi, joka on linkitetty Finance-ympäristöön, pitäisi olla luettelossa.
    - Jos Dataversea ei ole vielä määritetty, valitse **Määritys**. Dataverse-ympäristön määrittäminen voi kestää tunnin. Kun määritys on valmis, Finance-ympäristöön linkitetyn Dataverse-ympäristön nimen pitäisi olla luettelossa.
    - Jos integrointi on määritetty aiemmin luodussa Microsoft Power Platform -ympäristössä, varmista järjestelmänvalvojalta, ettei linkitetty ympäristö ole poissa käytöstä.

        Lisätietoja on kohdassa [Power Platform -integroinnin käyttöönotto](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Jos haluat käyttää Microsoft Power Platform -hallintasivustoa, siirry osoitteeseen <https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights -lisäosan määrittäminen

Jos olet aiemmin asentanut Finance Insights -apuohjelman, poista se ennen seuraavaa menettelyä.

> [!NOTE]
> Jos Data Lake -apuohjelma on jo asennettu LCS:ään, Finance insights tallentaa sen avulla ennusteisiin tarvittavat tiedot. Jos Data Lake -apuohjelmaa ei ole vielä asennettu LCS:ään, Finance insights -apuohjelma luo hallitun Data Lake -tallennustilan.

Noudattamalla näitä ohjeita voit asentaa Finance Insights -lisäosan.

1. KIrjaudu sisään LCS:ään ja valitse sivun oikealla olevan ympäristön nimen alta **Täydet tiedot**.
2. Valitse **Ympäristöapuohjelmat**-osassa **Asenna uusi apuohjelma**.
3. Valitse **Finance Insights** -lisäosa.
4. Hyväksy käyttöehdot ja valitse sitten **Asenna**.

Apuohjelman asentaminen voi kestää useita minuutteja.

## <a name="one-last-thing"></a>Vielä yksi asia...

Kun apuohjelma on asennettu, voi kestää jopa tunnin, ennen kuin Finance insights -ominaisuudet voidaan ottaa käyttöön Dynamics 365 Financen **Ominaisuuksien hallinta** -työtilassa. Jos tämä on liian pitkä odotusaika, **Merkityksellisten tietojen valmistelutilan tarkistus** -prosessi voidaan suorittaa manuaalisesti. 

1. Valitse Dynamics 365 Financessa **Järjestelmänvalvonta \> Asetukset \> Prosessien automatisointi**.
2. Etsi **Taustaprosessit**-välilehdessä **Merkityksellisten tietojen valmistelutilan tarkistus** ja valitse **Muokkaa**.
3. Määritä **Seuraava suoritus** -kentän asetukseksi aika, joka on 30 minuuttia ennen kuluvaa ajankohtaa.

   Tämä muutoksen pitäisi aiheuttaa se, että **Merkityksellisten tietojen valmistelutilan tarkistus** -prosessi pakotetaan suoritettavaksi heti.

   Kun **Merkityksellisten tietojen valmistelutilan tarkistus** -prosessi on suoritettu, Finance insights -ominaisuudet voidaan ottaa käyttöön **Ominaisuuksien hallinta** -työtilassa.

> [!NOTE]
> Jos **Merkityksellisten tietojen valmistelutilan tarkistus** -prosessia ei suoriteta, siirry kohtaan **Järjestelmän hallinta** > **Kyselyt** > **Erätyöt**. Vaihda **Prosessin automaation kyselyjärjestelmä** -kentän arvoksi **Odottaa** prosessin käynnistämiseksi. 
> 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
