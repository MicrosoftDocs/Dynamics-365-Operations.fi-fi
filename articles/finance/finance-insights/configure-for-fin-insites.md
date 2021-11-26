---
title: Finance Insightsin määritykset
description: Tässä ohjeaiheessa kerrotaan, millaiset määritysvaiheet järjestelmässä on suoritettava, jotta Finance Insightsin ominaisuuksia voi käyttää.
author: ShivamPandey-msft
ms.date: 1/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5668d3ddff777645b4f1c6608f025d0c5a63208a
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752975"
---
# <a name="configuration-for-finance-insights"></a>Finance Insightsin määritykset

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights yhdistää Microsoft Dynamics 365 Financen toiminnot Dataversen, Azuren ja AI Builderin kanssa. Yhdessä nämä tarjoavat tehokkaat ennustetyökalut organisaatiolle. Tässä ohjeaiheessa kerrotaan, millaiset määritysvaiheet järjestelmässä on suoritettava, jotta Finance Insightsin ominaisuuksia voi käyttää. Tämän aiheen menettelyjen onnistuminen edellyttää, että käytössä on järjestelmänvalvojan ja järjestelmän mukauttajan käyttöoikeudet [Power Portal -hallintakeskuksessa](https://admin.powerplatform.microsoft.com/), järjestelmänvalvojan käyttöoikeus Dynamics 365 Financessa sekä ympäristöjen luontioikeudet Microsoft Dynamics Lifecycle Servicesissa (LCS).

> [!NOTE]
> Seuraavat Finance Insightsin määrittämismenettelyt koskevat Microsoft Dynamics 365 Financen versiota 10.0.21 ja sitä uudempia versioita.

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Financen käyttöönotto

Määritä ympäristöt näiden ohjeiden avulla.

1. Luo tai päivitä Dynamics 365 Finance -ympäristö LCS:ssä. Ympäristö edellyttää, että käytössä on sovelluksen versio 10.0.21 tai sitä uudempi versio.

    > [!NOTE]
    > Ympäristön on oltava korkean käytettävyyden ympäristö. (Tämä ympäristötyyppi tunnetaan myös tason 2 ympäristönä.) Lisätietoja on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Jos Finance Insightsia määritetään eristysympäristössä, tuotantotiedot on ehkä kopioitava tähän ympäristöön, jotta ennusteet toimisivat. Ennustemallissa käytetään useiden vuosien tietoja ennusteiden luomiseen. Contoso-esittelytiedot eivät sisällä riittävästi historiatietoja ennustemallin kouluttamiseen. 

## <a name="configure-dataverse"></a>Määritä Dataverse

Näitä ohjeita noudattamalla voit määrittää Dataversen Finance Insightsille.

- Avaa ympäristösivu LCS:ssä ja tarkista, että **Power Platform -integrointi** -osa on jo asennettu.

    - Jos se on jo asennettu, Dataverse-ympäristön nimi, joka on linkitetty Finance-ympäristöön, pitäisi olla luettelossa.
    - Jos sitä ei ole vielä määritetty, valitse **Määritys**. Dataverse-ympäristön määrittäminen voi kestää tunnin. Kun ympäristö on määritetty, Finance-ympäristöön linkitetyn Dataverse-ympäristön nimen pitäisi olla luettelossa.

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

## <a name="feedback-and-support"></a>Palaute ja tuki

Lähetä sähköpostiviesti [Finance Insights (esiversio) -tiimille](mailto:fiap@microsoft.com), jos haluat antaa palautetta tai tarvitset tukea.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
